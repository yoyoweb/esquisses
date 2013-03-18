---
  layout: post
  title: Un navigateur de contenus personnels
  published: true
  date: 2013-03-17 14:02:03
---

En vrac, trois réflexions que l’annonce de la fermeture prochaine de Google Reader m’a inpiré.

## Un — faire mieux au lieu de geindre

Les gens sont vraiment cons, ils mangent de la merde. En fait ils n'ont que ce qu’ils méritent, ils n’ont qu’à faire leurs courses au marché chez des petits producteurs régionaux, être dans une AMAP, faire la cuisine. Ce n’est quand même pas compliqué de bien manger !

Je fais partie de ces cons qui mangent de la merde. Parce qu’avoir une alimentation saine ne fait pas partie de mes priorités. Cela demande du temps et je préfère consacrer mon temps à des choses que j’estime plus importantes (comme lire Twitter, chacun ses choix). Aussi, je n’adhère plus au discours qui en réponse à la fermeture de Google Reader, appelle à installer sur son serveur un des nombreux lecteurs de flux libre. Arrêtons de penser en geeks. Moi même, tout geek que je sois, je n’installerai pas un clone de Google Reader sur un serveur, parce que j’essaie de réduire le temps que je passe à faire de l’administration système. Question de priorités.

Si nous voulons promouvoir ATOM et compagnie, ce n’est pas avec ce discours que nous y arriverons. Mais en fabriquant des produits au moins aussi bons, beaux, utiles, utilisables, que leurs alternatives privatives. Des logiciels qui seront choisis et utilisés parce qu’ils ne demandent pas d’efforts et améliorent la vie. Encore une fois, le succès de Firefox n’est pas dû à sa philosophie. Seule une petite minorité l’utilise parce qu’il est libre. Je suis persuadé que la grande majorité de ses utilisateurs l’ont choisi parce qu’il est objectivement meilleur, sur un plan ou un autre, que les autres navigateurs. Donc avant de blâmer ces crétins entre la chaise et le clavier qui deviennent prisonniers volontaires de services privateurs, blâmons nous de ne pas créer de logiciels meilleurs que leurs alternatives. Et, pour ceux d’entre-nous qui ne sont pas adeptes de l’auto-flagellation, sortez vous les pouces de la bouche, et au lieu de troller, créez !

## Deux — savoir ce que l’on veut

Je n’ai jamais utilisé Google Reader. Je ne comprends donc pas son succès parmi les geeks et les infovores. Mais de quelques lectures et échanges depuis l’annonce de sa fermeture, j’ai l’impression que ce que ses veufs et veuves regretteront, ce n’est pas tant le lecteur RSS que le logiciel leur permettant de gérer de manière agréable une partie des contenus qu’ils consultent. Et que donc ce qui nous manque, ce n’est pas un nouvel agrégateur RSS, mais un bon système de gestion de contenus personnels. Par contenus personnels, j’entends tous les articles intéressants que nous voyons passer, en surfant ou qui nous arrivent directement via des flux, RSS, Twitter, les partages de marque-pages, etc. Mais aussi les discussions, sur des listes de courrier électronique, Twitter voire IRC. Tous ces articles que nous mettons de côté pour les lire un jour, que nous partageons, que parfois nous annotons ou commentons.

Aujourd’hui, tous ces contenus sont dispersés. Des dizaines de dossiers thématiques dans notre courrielleur, nos lecteurs de groupe de discussions et de flux RSS, des centaines d’onglets ouverts dans notre Firefox, divers gestionnaires de signets, des favoris dans Twitter, les journaux IRC, j’en oublie. Et pourtant, quel que soit le canal par lequel arrivent ces informations, elles sont globalement similaires. Des articles ou des conversations, des métas-données, et parfois des ajouts personnels, catégorisation et commentaires. Il me semblerait pertinent de les agréger dans un seul outil. Techniquement, ce n’est guère compliqué, et je pense qu’avec toutes les briques existantes, on pourrait facilement bricoler ce genre d’outil. Mais le succès de Google Reader me semble lié davantage à son ergonomie qu’à une supériorité technique. Et c’est sur ce point, l’utilisabilité, que se jouera la crédibilité des alternatives.

Le remplaçant du défunt lecteur de Google n’est donc peut-être pas à chercher du côté d’autres lecteurs de flux, mais de la création d’un *gestionnaire de contenus personnels* ergonomique. Qui archive tous les contenus que nous voyons passer, avec leurs méta-données. Qui nous permette d’y accéder de partout. En rende la lecture agréable. Le partage simple comme un clic. Et permette de les enrichir. Le tout doté d’une interface agréable à utiliser quelle que soit sa maîtrise de la chose informatique. Le [navigateur de contenus](https://bitbucket.org/david/contentbrowser/) de David est un pas dans cette direction.

Yaplukafokon

## Trois — considération pratique

J’ai beau être conscient du danger des services en ligne comme Google Reader, je dois reconnaître qu’ils sont très pratiques et que leur trouver des alternatives accessibles et crédibles est difficile. Ils sont pratiques car ils offrent un service accessible de partout depuis un simple navigateur. Difficiles à concurrencer car, comme il n’est pas réaliste à court terme d’imaginer qu’une majorité d’internautes auto-héberge ses outils, concurrencer les services de Google et compagnie suppose pour l’instant de mettre en place une architecture technique similaire. C’est à dire une masse de serveurs pour traiter et stocker les données.

L’arrivée des applications Web va probablement modifier une partie du problème. Grâce à HTML5, on peut à présent créer des applications dont tous les traitements s’effectuent dans le navigateur. Les serveurs n’ont plus qu’à fournir des fichiers statiques, et gérer le stockage et la synchronisation des données. De plus en plus d’applications vont je pense adopter un modèle composé d’une applications HTML5 s’exécutant dans le navigateur, et d’une API serveur au dessus du modèle de données. La difficulté logistique à fournir un clone libre à Google Reader s’en trouve largement réduite. Reste la question du stockage des données.

J’ai [proposé de détourner IMAP](http://esquisses.clochix.net/2013/02/26/imap/) et d’utiliser les comptes mails que chacun possède comme entrepôts décentralisés de données, mais mon idée n’a guère suscité de réactions. Les Grands Génies sont rarement reconnus de leur vivant. Je reviens donc à la charge avec une autre proposition : inciter les FAI à soutenir le projet [unhosted](http://unhosted.org). L’idée de ce projet est de découpler le traitement des données de leur stockage. Ce qui permet d’utiliser un service hébergé tout en stockant ses données dans un autre dépôt, soit auto-hébergé, soit chez un prestataire. Il encourage donc entre autre la création de services proposant juste de l’hébergement de données. Ce sont de tels entrepôts dont les applications Web ouvertes ont besoin. Malheureusement, tout cela reste un peu trop technique, et je ne pense pas que les non-geeks soient prêts à trouver et payer un prestataire d’hébergement de données pour leurs applications. Il faudrait qu’un tel service leur soit fourni clé en main, avec leur connexion.

Or, la plupart des fournisseurs d’accès internet assortissent leur offre de services annexes, comme souvent une adresse de messagerie. Jadis, certains proposaient également l’hébergement de quelques pages Web, d’une site personnel. On pourrait imaginer que demain, quelques fournisseurs de qualité proposent, avec tout abonnement à Internet, un entrepôt en ligne où stocker les données de ses applications Web. Ainsi je pourrais partager sur mon compte FDN les données des applications s’exécutant dans mes Firefox.

Faire héberger nos données par notre FAI n’est bien sûr qu’à moitié satisfaisant. Et je doute que beaucoup de fournisseurs d’accès voient un quelconque intérêt à fournir ce service. L’idée ne me semble néanmoins pas complètement irréaliste.

À vous lire.

