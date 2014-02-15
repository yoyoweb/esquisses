---
  layout: post
  title: La mémoire des DNS
  published: true
  date: 2014-01-27 22:00:00
  references:
  - url: http://www.sophiemenart.info/2014/01/eternite-virtuelle/
    title: Éternité virtuelle
  - url: https://larlet.fr/david/blog/2013/testament-numerique/
    title: Testament numérique
  - url: http://www.la-grange.net/2013/01/18/testament
    title: Des scories numériques
  - url: https://n.survol.fr/n/carte-de-donneur-au-domaine-public
    title: Carte de donneur au domaine public !
---

Un [nouvel article](http://www.sophiemenart.info/2014/01/eternite-virtuelle/) signalé par Agnès me ramène à la nécessaire réflexion sur l’avenir de nos données après notre mort. Je réalise que les fameux silos centralisés et privatiseurs de contenus sont probablement plus pérennes que nos solutions auto-hébergées de guicks. Si je meurs demain, ce carnet ne me survivra que quelques semaines. Il est hébergé sur un serveur dont je paie le loyer au fil de l’eau. Sans ré-alimentation du compte chez Gandi, mon serveur et tout ce que j’y héberge disparaitra en moins de deux mois. Mon précédent carnet, associé au nom de domaine `clochix.net` pourrait survivre un peu plus longtemps, je renouvelle généralement le domaine pour plusieurs années.  Probablement pas plus de trois ans. Par contre, les sources de ce carnet, [hébergées sur Github](https://github.com/clochix/esquisses), pourraient bien être plus pérennes. Avec un peu de chance, elles resteront disponibles tant que Github existera et ne fera pas de ménage dans les dépôts inactifs. Mes quelques contributions sur des sites centralisés, Twitter, Google+, Github, pourraient bien être les dernières traces de ma présence en ligne quelques années après la mort de mon être AFK.

Bien sûr, certains d’entre nous mettent en place des testaments numériques où nous confions nos clés à un proche pour qu’il mette de l’ordre dans nos affaires après notre disparition. Mais cela reste à mon avis une solution fragile, peu fiable sur le long terme. Il nous faudrait un service public de cimetière numérique, avec des concessions « perpétuelles ». Où figer et héberger pour quelques temps l’ensemble de nos contributions numériques. Et cela m’amène à la pérennité des noms de domaine. On n’est jamais propriétaire d’un nom de domaine, juste locataire pour quelques années. Serait-il légitime de conserver ces noms après notre mort ? Je ne le pense pas, les NDD sont une ressource commune que nous privatisons temporairement. L’hétéronyme *Clochix* ne m’appartient pas, je ne vois pas au nom de quoi j’interdirais pour l’éternité à d’autres d’utiliser l’adresse `clochix.net`. Et pourtant j’aimerais bien ne pas casser le Web, qu’après ma mort les liens vers mes billets ne se retrouvent pas soudain brisés. Que des redirections amènent les visiteurs vers le cimetière des billets.

Il faudrait pour cela ajouter un historique au DNS. Avoir la possibilité de résoudre une URL à une date précise. Demander la représentation de la ressource `http://clochix.net/toto/titi` en janvier 2014. Les serveurs DNS indiqueraient que les URLs de ce domaine en janvier 2014 sont à présent gérées par le serveur `http://open-cemetery.org`. Lequel aurait toutes les redirections qui vont bien. En fait, ce qu’il faudrait, c’est une sorte de négociation de contenu pour les requêtes DNS. (il existe déjà des services privés comme par exemple DomainTools qui conservent un historique des versions des enregistrements DNS et permettent de retrouver la version valide à une date donnée. Une normalisation de ce type de service serait bienvenue, avec possibilité de ré-écrire l’historique afin de pointer vers un cimetière).

Qu’en pensez-vous ?
