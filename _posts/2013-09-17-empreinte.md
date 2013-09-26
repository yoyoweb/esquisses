---
  layout: post
  title: Monsieur Madame empreinte digitale numérique
  published: true
  date: 2013-09-17 23:18:12
  tags:
  - privacy
---

Je viens de lire, sur [le conseil de David](https://twitter.com/davidbgk/status/377541817488932864), un article sur [PGP, l’identité numérique et les réseaux de confiance](http://bitcoinism.blogspot.nl/2013/09/building-pgp-web-of-trust-that-people.html). Il affirme notamment que si l’utilisation de réseaux de confiance est si peu répandue, c’est en partie parce que les logiciels de cryptographie ne sont pas assez accessibles pour des non-experts. Ça m’a donné une idée pour rendre un tout petit peu plus agréable une minuscule partie en marge du processus, l’identification d’une clé à partir de son empreinte.

Une clé publique ou un certificat sont des signatures numériques certifiant l’identité d’un individu ou d’un objet. Je peux utiliser ma clé pour signer mes message et prouver que j’en suis l’auteur. Lorsqu’on se connecte en SSH à un serveur, SSH affiche la clé de la machine pour prouver qu’on se connecte au bon serveur. Ce mécanisme implique que je sache reconnaitre la signature et l’associer au signataire. Pour cela, on peut imaginer deux mécanismes, l’un centralisé, une sorte d’annuaire officiel faisant le lien entre une entité et sa signature, l’autre décentralisé, où lorsque je ne reconnais pas une signature je demande à mes contacts s’ils la connaissent.

Il existe malheureusement des cas où cette vérification n’est pas possible. Soit parce que la signature n’a pas été publiée dans un annuaire officiel, soit parce que personne parmi mon réseau ne la connait. Il faut alors recourir à un mécanisme moins sûr en cherchant la signature dans des endroits publics. Par exemple vous pouvez récupérer [ma clé publique](http://clochix.net/public.asc) sur mon site. C’est peu sécurisé, car le site ou la communication peuvent avoir été détournés, mais ça vaut mieux que rien. Ces signatures sont de longs fichiers binaires incompréhensibles pour la plupart d’entre nous. On les identifie donc généralement par un résumé automatique créé par un algorithme connu. Ce résumé est appelé [empreinte](http://fr.wikipedia.org/wiki/Hash), *hash* ou *fingerprint*. L’empreinte de ma clé est `FE70 1DEC 5060 0716 D631 7AE6 96DD 4B5C 2060 838F`, celle de mon serveur `12:52:65:81:3e:6e:20:52:ae:31:6e:65:a0:90:0f:90`. Cette empreinte permet de vérifier que la clé publique que vous avez récupérée est bien la bonne. C’est mieux, mais pas encore optimal. Lorsque je me connecte à mon serveur depuis un ordinateur tiers, et que SSH me demande si `12:52:65:81:3e:6e:20:52:ae:31:6e:65:a0:90:0f:90` est bien sa signaturer, j’avoue être parfois un peu en peine pour répondre. Des gens intelligents ont donc eu la bonne idée de [créer une représentation graphique en ASCII Art](http://fr.wikipedia.org/wiki/Key_signing_party) de cette empreinte. Si je me connecte à un serveur en ajoutant l’option kivabien, il va désormais afficher :

      $ ssh -o VisualHostKey=yes toto@toto.com
      The authenticity of host ’toto.com’ can’t be established.
      RSA key fingerprint is 12:52:65:81:3e:6e:20:52:ae:31:6e:65:a0:90:0f:90.
      +--[ RSA 2048]----+
      |oo    .o+.       |
      |E..  ...         |
      |o=. ...          |
      |= +o..o.         |
      |.=o. o..S        |
      |.o    o.         |
      |.    .           |
      |                 |
      |                 |
      +-----------------+

En faisant intervenir la mémoire visuelle d’une forme, la chance de détecter une clé erronée, et donc une tentative d’attaque, augmente. Mais l’ASCII Art reste assez hermétique aux non technophiles.

Pour rendre la vérification de clés plus conviviale, pourquoi ne pas proposer un algorithme transformant l’empreinte en avatar ? Les premiers octets fixant la couleur des cheveux, les suivants le type de chevelure, la forme du visage, etc. À chaque clé pourrait ainsi être associé un avatar. Il me suffirait de publier cet avatar à divers endroits que je contrôle relativement (mon site, mes profils sur des réseaux sociaux…) pour que les gens qui récupèrent ma clé puissent vérifier qu’elle m’identifie bien, de façon un chouïa plus conviviale qu’avec l’empreinte. La méthode est loin d’être infaillible. Une attaque visant spécifiquement une clé est assez simple à mettre en œuvre. Et il est évident que lors des [rencontres de signature mutuelles de clés](http://fr.wikipedia.org/wiki/Key_signing_party), vérifier la signature hexadécimale plutôt que l’avatar de la clé continue à s’imposer. Mais cette solution me semble un bon compromis entre la fiabilité et l’utilisabilité.

Quelqu’un a cinq minutes pour coder une petite preuve du concept, un générateur d’avatar à partir d’un hash ? (en partant par exemple de [ce générateur](http://codepen.io/TimPietrusky/pen/JglCv)).

\[Ajouts du 18 septembre :\]
 - David, encore lui, me signale que Gihub a [mis en place des identicones](https://github.com/blog/1586-identicons) générés automatiquement à partir d’un hash de l’identifiant d’un utilisateur. Ils restent très abstraits, je pense que quelque chose de plus anthropomorphe serait plus convivial ;
 - Sébastien Sauvage m’a indiqué [VizHash GD](https://github.com/sebsauvage/VizHash), qui crée des hashs graphiques. Le [wiki du projet](http://sebsauvage.net/wiki/doku.php?id=php:vizhash_gd) liste d’autres initiatives similaires ;
 - [Kevin Gaudin](https://plus.google.com/105599514712357912650/posts) m’a fait découvrir le projet [MonsterID](http://www.splitbrain.org/projects/monsterid), qui crée un hash sous forme de petit monstre. Kevin en a réalisé une [implémentation en JavaScript](http://kevingaudin.github.io/monsterid.js/). On se rapproche ici beaucoup plus de ce que j’ai en tête.

*Note sur l’article* : une des points intéressants de l’article de Justus Ranvier est qu’il définit l’identité en fonction d’interactions sociales plutôt que d’un bout de plastique délivré par une administration. Malheureusement dans sa proposition finale de réseau social de certification d’identité, il utilise pour ce faire des composants qui pour moi ne font pas forcément partie de l’identité, comme la date de naissance, l’adresse de résidence, etc. Clochix est l’auteur de ce carnet, de réflexions de bistro sur Twitter et de quelques dépôts sur Github. C’est tout. Il n’a ni date de naissance hormis celle d’enregistrement du domaine, ni adresse, hormis l’IP de ce serveur. Ou du moins, la date de naissance et la résidence des doigts qui tapent sur le clavier ne font pas partie de l’identité "Clochix". Et je me demande comment la garantir, certifier que je suis bien Clochix, puisque la quasi totalité des composants de cette identité sont publics, donc aisément usurpables. La gestion de l’identité de ses hétéronymes n’est pas résolue.

PS : l’idée de représentation graphique d’une empreinte n’est évidemment pas nouvelle. Wikipedia date l’invention des [identicones](http://en.wikipedia.org/wiki/Identicon) de 2007, j’ai trouvé un article de 2009 évoquant la conversion de l’empreinte en [code de couleurs](http://blog.bentobako.org/index.php?post/2009/02/02/A-visual-way-to-check-fingerprints) et il existe un outil, [Visprint](http://www.tastyrabbit.net/visprint/) qui crée une fractale à partir d’une empreinte. Quant au site [http://robohash.org/](), il propose de transformer n’importe quel texte en robot.

