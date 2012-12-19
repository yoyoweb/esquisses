---
  layout: post
  title: Le Château de Versailles, panneau publicitaire pour Google
  published: true
  date: 2012-08-01 21:48
  tags:
  - Google
  - Mozilla
  - OpenWeb
---

*Mise à jour du 2 Août à 20h00 :* j'ai contacté "le Château de Versailles" via Twitter, [ils m'ont promis de regarder](https://twitter.com/CVersailles/status/231080102237196289). Affaire à suivre donc, mais peut-être que ce billet aura servi à quelque chose. Je mettrai à jour ce billet si j'ai plus d'informations.

J'ai découvert aujourd'hui une excellente initiative qui va permettre à davantage de gens d'accéder à la culture. Le Château de Versailles et Google se sont associés pour créer un site Web de présentation du fameux monument. Le site comporte notamment une reconstitution en 3D de grande qualité d'une partie du Château et de son domaine. On peut s'y promener librement comme dans un monde virtuel. Cette reconstitution utilise [WebGL](http://www.khronos.org/webgl/), une technologie qui permet aux navigateurs Web d'afficher des objets en 3D sans avoir recours à un plugin externe comme Flash. WebGL est un peu le HTML de la 3D, une spécification ouverte que tout le monde peut utiliser librement. À l'exception d'Internet Explorer, tous les navigateurs modernes utilisent, au moins partiellement cette technologie.

J'ai donc tiqué lorsque j'ai lu sur un article de présentation que l'« expérience interactive » ne fonctionnait qu'avec Chrome. Et effectivement, une fois arrivé sur [le site](http://www.versailles3d.com), un message m'informe que mon Firefox ne permet pas d'afficher de contenus en WebGL, et que je dois installer Chrome. Pourtant, il y a quelques semaines Mozilla avait organisé un concours de création d'animations WebGL, et je n'avais eu aucun problème pour afficher les nombreuses réponses. Je vous invite d'ailleurs à aller jeter un œil à ces [superbes démonstrations](https://developer.mozilla.org/fr/demos/tag/tech:webgl?sort=likes) de ce dont le Web est capable aujourd'hui.

Les technologies et leur implémentation dans les navigateurs évoluant vite, il est d'usage, avant d'afficher un contenu utilisant des fonctionnalités récentes, de vérifier si le navigateur est capable de le faire. Si le site du Château de Versailles en 3D m'affiche qu'il n'est pas disponible sous Firefox, c'est sans doute qu'il utilise des parties de WebGL temporairement absentes de mon navigateur. Par curiosité, j'ai jeté un œil au code source de la page, pour essayer de découvrir quelle fonctionnalité manquait. Voici le code de la [fonction JavaScript](http://www.chaostoperfection.com/js/Main.min.js) utilisée pour déterminer si un navigateur est en mesure d'afficher le site :

    function e(b){
        var c=navigator.userAgent.match(/[Cc]hrome\/([0-9]{1,2})/);
        return c?(c=parseInt(c[1]),c<=b):!1
    }

Si vous ne parlez pas encore JavaScript, en voici une traduction : si tu t'appelles « Chrome », tu peux entrer. Sinon, reste dehors. Le site ne contrôle pas du tout les capacités du navigateur, juste son nom. Pour le vérifier, il suffit de demander à son navigateur de prétendre être Chrome. Avec Firefox, on peut par exemple installer l'extension [User Agent Switcher](https://addons.mozilla.org/fr/firefox/addon/user-agent-switcher/). Et en se faisant passer pour Chrome, mon Firefox m'a permis de m'immerger sans aucun problème dans cette jolie reconstitution en 3D du Château. Ironie, le test est si brutal qu'il exclut même Chromium, la version libre de Chrome qui a les même fonctionnalités que lui.

On est donc en présence du site d'un établissement public qui incite ses visiteurs à installer un logiciel spécifique, sans que rien ne le justifie. Si j'en crois Wikipédia, un [établissement public](http://fr.wikipedia.org/wiki/%C3%89tablissement_public) est financé par des fonds publics et remplit une mission d'intérêt général. Est-ce remplir une mission d'intérêt général que d'inciter les internautes à utiliser un logiciel certes de très bonne facture, mais bien peu respectueux de leur vie privée ?

Je ne suis pas naïf, je sais bien que si Google a participé à la réalisation de ce site, ce n'est ni par philanthropie, ni par volonté de rendre une part du patrimoine plus accessible. Je sais bien que les institutions culturelles manquent désespérément de moyens — cf par exemple la série estivale du Canard Enchaîné sur les difficultés du Muséum d'histoire naturelle — et sont fortement incités à faire appel à des financement privés. Et on se retrouve à nouveau dans [le même cas de figure](http://scinfolex.wordpress.com/2012/07/27/comment-la-propriete-intellectuelle-a-transforme-les-jeux-olympiques-en-cauchemar-cyberpunk/) que pour les jeux du cirque londoniens. Là-bas, Coca Cola a payé, la consommation d'autres boissons est interdite. Ici, Google a payé, l'utilisation d'autres navigateurs pour visiter le site est interdite.

Que faire ? Informer, expliquer autour de soi comment faire passer son navigateur pour Chrome afin de profiter de la visite en 3D en restant confortablement dans son Firefox. Interpeller l'établissement public du Château de Versailles en leur demandant si faire de la pub à Google entre réellement dans leurs missions. Et continuer à lutter quotidiennement, pour que le Web reste ouvert et que la culture ne soit pas confisquée par quelques intérêts privés. Lutter. Ou continuer la plongée toujours plus profond dans le cauchemar.

