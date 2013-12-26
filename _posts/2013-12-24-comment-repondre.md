---
  layout: post
  title: Comment répondre
  published: true
  date: 2013-12-24 22:10:00
---

Il n’aura échappé à personne que je développe actuellement une application Web pour lire des articles depuis mon ordiphone. Elle a deux fonctions : stocker des articles pour me permettre de les lire plus tard, et les rendre lisibles sur le minuscule écran de mon téléphone. Pour répondre au premier besoin, enregistrer simplement les pages Web serait suffisant. Mais hélas bien souvent elles ne sont pas adaptées à de petits écrans. Je les passe donc à travers une moulinette, une des nombreuses bibliothèques implémentant un algorithme d’extraction du texte de l’article, et j’enregistre le résultat. De ce fait, je consulte de moins en moins le Web lui-même. Je reçois des liens via divers canaux, en extrait automatiquement le contenu et le lis non plus dans un navigateur, mais dans une application tierce (en l’occurrence une application exécutée à l’intérieur d’un navigateur, mais c’est un hasard).

Je réfléchis également, [à la suite de David](https://larlet.fr/david/blog/2013/outils-conviviaux/), à la convivialité (au sens d’Illich) de mes outils. Ou plus exactement j’essaie de déterminer s’ils me rendent plus autonomes ou m’asservissent.

Mon flux de travail me permet de me concentrer sur l’essentiel, le contenu, en gommant l’accessoire, mises en page et décorations qui pourraient me distraire. Mais il me fait perdre un élément fondamental du Web, la possibilité d’interagir. Lorsque je veux répondre à un article, je ne peux pas le faire depuis mon outil, parce que lui-même ne sait pas comment faire. Il me faut ouvrir la page initiale pour essayer de découvrir les possibilité d’interaction : commentaires, liste de discussion par courriel, ping depuis une réponse hébergée ailleurs…

En fait, il me semble que nous n’avons pas encore de moyen simple d’indiquer à des agents automatiques comment réagir à un contenu. Dans le balisage de ce carnet, j’utilise la propriété `bug-database` du vocabulaire [DOAP](https://github.com/edumbill/doap/wiki) pour indiquer l’URL du gestionnaire de tickets. À partir de cette info, et en identifiant le gestionnaire cible, un agent automatique pourrait proposer de saisir un ticket. Par exemple un navigateur pourrait proposer un bouton « signaler un problème sur ce site ». J’ai [déjà développé ce point](http://esquisses.clochix.net/2012/06/19/oukil%C3%A9-le-bugtracker/).

De manière similaire, il faudrait un vocabulaire décrivant le moyen de répondre à un contenu. Ainsi, un outil comme le mien qui affiche le contenu dans un autre contexte, pourrait proposer un formulaire universel de réponse qui enverrait automatiquement mon commentaire en utilisant le protocole choisi par le contenu initial : requête POST, message électronique, `pingtrackback`…

Bref, il nous faudrait expliciter aux robots comment, non plus seulement lire, mais interagir avec nos contenus.


