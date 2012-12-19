---
  layout: post
  title: Étiqueter ses messages dans Mutt
  published: true
  date: 2012-12-04 21:46:00
  tags:
  - Mutt
  - CLI
---

Certains utilisateurs ardus de courrier électronique aiment à utiliser des étiquettes (tags, labels…) pour s'y retrouver dans leurs messages. Malheureusement il n'existe à ma connaissance pas de format interopérable pour partager cette classification entre plusieurs clients de messagerie accédant au même serveur.

On pourrait peut-être pour enregistrer les étiquettes utiliser l'en-tête `keywords` défini dans la [RFC 680](http://tools.ietf.org/html/rfc680) de 1975, et toujours présent dans [la dernière en date](http://tools.ietf.org/html/rfc5322#section-3.6.5) : <q> The "Keywords:" field contains a comma-separated list of important words and phrases that might be useful for the recipient </q>. Mais je ne connais pas de logiciel l'utilisant, et surtout il est réservé aux mots clés fixés par l'expéditeur. L'usage semble donc être plutôt d'utiliser deux en-têtes non standardisés, `X-Keywords` et `X-Labels`, lesquels contiennent une liste de mots clés séparés par des espaces ou des virgules.

Mutt prend nativement en compte `X-Label` qui peut être utilisé pour :
 - filtrer l'affichage de la liste des messages : `~y expr` n'affiche que les messages dont le champs `X-Label` contient `expr` ;
 - les labels peuvent être affichés dans l'index des messages en utilisant `%y` ou `%Y` dans la variable `$index_format` (`%Y` propose un meilleur affichage lorsqu'on utilise la vue des fils de discussion en arbre) ;

Malheureusement, rien n'est prévu pour modifier cet en-tête (Mutt considère qu'il a été ajouté en amont). On peut bien sûr le gérer à la main, grâce à cette fonctionnalité géniale qui permet de modifier un message avec son éditeur favori et de le ré-enregistrer. Mais c'est un peu laborieux.

Alberto Bertogli propose une solution élégante pour [gérer les en-têtes `X-Label`](http://blitiri.com.ar/p/other/mutt-labels/). Il suffit d'éditer le message via un programme externe dédié. Deux outils similaires existent, `formail`, du projet [procmail](http://procmail.org/) et `reformail` du projet [Courier](http://www.courier-mta.org/). Ils sont disponibles respectivement dans les paquets Debian [procmail](http://packages.debian.org/sid/procmail) et [maildrop](http://packages.debian.org/sid/maildrop). Pour modifier les étiquettes d'un message, il suffit donc de l'éditer en le passant au travers de l'outil de reformatage. Je vous laisse aller lire l'article d'Antonio.

À noter que si le champs `X-label` est pris en charge nativement par Mutt, rien n'empêche d'effectuer une manœuvre similaire avec n'importe quel en-tête. `~h` permet de filtrer sur l'ensemble de l'en-tête (pour que cela fonctionne sur les dossiers IMAP, il faut préciser via le paramètre de configuration [`imap-header`](http://www.mutt.org/doc/devel/manual.html#imap-headers) les champs additionnels à récupérer afin de pouvoir y appliquer le filtre).

Comme je suis un boulet, je n'avais initialement pas trouvé `formail` dans Debian et ai donc [adapté le script](https://github.com/clochix/Config/commit/d8d422b7a4bcadb42be04314ae90e74977e0fd23) d'Alberto pour `reformail`.

Vala, vous avez une raison de moins de ne pas passer à Mutt.
