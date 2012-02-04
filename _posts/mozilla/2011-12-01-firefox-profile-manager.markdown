---
  layout: post
  title: Le nouveau gestionnaire de profils de Firefox
  published: true
  date: 2011-12-07 23:58:02
  tags:
  - Mozilla
---

Que ce soit lorsqu'on développe des sites Web, ou juste pour surfer avec des réglages différents selon les sites, on peut avoir besoin d'exécuter simultanément plusieurs instances de Firefox, avec des configurations différentes. 

Jusqu'à présent, on pouvait simplement le faire en rajoutant les options `-no-remote` et `-ProfileManager` au lancement du navigateur. La première indique que l'on veut lancer une nouvelle instance, et la seconde affiche au démarrage le gestionnaire de profils, qui permet de choisir sa configuration. Cette solution pourrait bientôt devenir obsolète avec l'arrivée, discrète, d'un nouveau gestionnaire de profils. C'est une application XUL autonome, qui offre quelques nouvelles fonctionnalités intéressantes. La suppression de l'interface de gestion de profils intégrée à Firefox est un débat qui dure depuis des années, [ici][bug] et [là][group] par exemple. Le but n'est pas tant de diminuer le temps de démarrage — l'impact lors de l'utilisation du profil par défaut est quasi nul — que d'externaliser un code ancien et complexe. La sortie du nouveau gestionnaire a été des plus discrètes, et personne ne semble plus travailler dessus actuellement. Ses nouvelles fonctionnalités méritent quand même d'être présentées.

La documentation sur MDN a été traduite deux heures après que j'ai fini ce billet, je vous y renvoie : [le gestionnaire de profils][mdnfr]

[mdnfr]: https://developer.mozilla.org/fr/Profile_Manager

Pour mémoire, ce que j'écrivais hier soir&nbsp;:

## Un peu de doc

### Démarrage

Pour utiliser le nouveau gestionnaire, il suffit de [le télécharger][dl], décompresser l'archive et d'exécuter le programme `profilemanager-bin` (sous GNU/Linux et Moac) ou `profilemanager.exe` (sous Windows). Par défaut, il affichera les profil de Firefox, mais peut également gérer ceux de n'importe quelle autre application qui utilise `xulrunner`, comme **Thunderbird** ou **SeaMonkey**. Il suffit pour cela de préciser le nom de l'application au démarrage, par exemple `profilemanager-bin seamonkey`

### Profils et version des applications

Le nouveau gestionnaire maintient deux listes: l'une de profils, l'autre des différentes versions de l'application qui peuvent être utilisées avec ces profils. Dans le cas par défaut, il va lister toutes les versions de Firefox et tous les profils Firefox qu'il détectera sur le système, et va permettre d'associer les uns aux autres, c'est à dire de choisir avec quelle version de Firefox sera ouvert chaque profil. Cela permet par exemple d'avoir un profil `ancien` pour faire des tests avec Firefox 3.6, un profil `stable` pour la version actuelle et un profil `nocturne` à utiliser avec les compilations *nightlies*.

Au premier démarrage, il va essayer de détecter automatiquement toutes les versions de Firefox installées sur votre système, mais vous pouvez bien sûr lui en indiquer d'autres en cliquant sur `Manage Firefox version…`.

<a href="http://www.flickr.com/photos/clochix/6441106045/" title="The New Profile Manager For Firefox by Clochix, on Flickr"><img src="http://farm8.staticflickr.com/7163/6441106045_b3741bd128_b.jpg" width="711" height="560" alt="The New Profile Manager For Firefox"></a>

Les menus permettent de créer un nouveau profil vierge ou en copiant un profil existant, d'en supprimer un, et, nouveauté intéressante, de gérer des sauvegardes. Le dialogue de création offre une interface similaire à celui du gestionnaire actuel, permettant de choisir un nom et l'emplacement sur le disque où sera stocké le nouveau profil.

La liste des profils affiche par ailleurs deux colonnes supplémentaires, l'une permettant de choisir celui par défaut, la seconde indiquant les profils verrouillés car en cours d'utilisation.

### Options de démarrage

Pour lancer l'application avec un profil, il suffit de sélectionner le dit profil, préalablement associé à une version de l'application, et de cliquer sur `Start`. Mais le nouveau gestionnaire permet d'aller plus loin en offrant quelques options intéressantes&nbsp;
* la possibilité de démarrer l'application avec un profil temporaire. C'est très utile par exemple lorsqu'on a détecté un bug. Pour s'assurer qu'il est causé par l'application et non un paramètre ou une extension du profil, il est conseillé de tester avec un profil vierge. Cette option crée un nouveau profil temporaire à une session;
* démarrer Firefox en mode non-connecté. Par exemple si vous n'êtes pas connecté mais voulez utiliser des applications Web capables de fonctionner dans ce mode;
* démarrer Firefox en mode sans échec, un mode où toutes les extensions sont désactivées, lorsque l'une d'entre elles empêche Firefox de démarrer normalement;
* démarrer une nouvelle instance, équivalent à l'utilisation de `-no-remote` en ligne de commande, pour faire tourner simultanément plusieurs Firefox avec des profils différents;

### Sauvegarde

Une autre nouveauté intéressante est la possibilité de sauvegarder et restaurer un profil. Deux modes de sauvegarde sont disponibles&nbsp;: des sauvegardes prises en charge par le gestionnaire, et des archives externes. Dans le premier cas, elles s'affichent dans la liste des profils, et un clic suffit à les restaurer. Dans le second, une archive Zip est créée, qui permet par exemple de restaurer le profil sur une autre machine. Le choix du type de sauvegarde ou de restauration se fait via les options du menu `Backup`.

## Et donc&nbsp;?

Je profite de l'occasion pour rappeler l'intérêt des profils de Firefox. Pour les développeurs Web, qui peuvent aisément tester leur site avec différentes versions du navigateur. Mais aussi pour tout internaute. Lorsqu'on surfe, on n'a pas forcément besoin des mêmes réglages, des même outils, selon les sites. Pour faire fonctionner le site de sa banque, mieux vaut généralement autoriser les cookies, Flash et compagnie. Par contre, pour surfer sur des sites commerciaux, vous pouvez avoir envie de bloquer les pubs. À chaque usage correspondent des réglages et des extensions. D'où l'utilité d'utiliser simultanément plusieurs instances de Firefox, avec des profils distincts. Pour ma part j'ai en permanence trois Firefox ouverts, avec trois profils&nbsp;:
* l'un pour développer, avec toutes les extensions qui vont bien, Firebug et sa bande;
* l'un pour surfer, avec les extensions de protection de la vie privée&nbsp;: Adblock Plus, Better Privacy, FlashBlock, Ghostery;
* l'un pour les sites auxquels je me connecte, webmails, réseaux sociaux, etc;

Un avantage de cette solution est que même si je suis connecté à un réseau social, ce n'est pas dans l'instance que j'utilise pour surfer, donc les mécanismes de pistage du réseau, basés sur les cookies, ne peuvent pas me suivre à la trace d'un site à l'autre.

### Pour conclure

J'ai testé ce nouveau gestionnaire, et le trouve bien pratique, malgré quelques défauts de jeunesse. Le principal étant à mes yeux qu'il se ferme après avoir lancé Firefox, obligeant à le relancer pour lancer un autre navigateur avec un autre profil. Le soucis est [signalé][multiple] et ne devrait pas être compliqué à régler. Malheureusement, le projet n'a l'air ni prioritaire, ni très important, et les commits sont rares. Si vous avez envie de commencer à bidouiller le code de Firefox sans vous attaquer à des modules trop complexes, corriger les quelques [bugs][bugs] du bidule ou y ajouter des fonctionnalités manquantes pourrait être un bon point d'entrée.


[bug]: https://bugzilla.mozilla.org/show_bug.cgi?id=214675
[group]: https://groups.google.com/group/mozilla.dev.planning/browse_thread/thread/06900b8b97c2655d
[mdn]: https://developer.mozilla.org/en/Profile_Manager
[dl]: ftp://ftp.mozilla.org/pub/mozilla.org/utilities/profilemanager/1.0/
[multiple]: https://bugzilla.mozilla.org/show_bug.cgi?id=598687
[bugs]: https://bugzilla.mozilla.org/buglist.cgi?resolution=---&query_format=advanced&component=ProfileManager&product=Testing



