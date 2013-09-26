---
  layout: post
  title: Se préserver
  published: true
  date: 2013-09-15 14:18:11
  tags:
  - privacy
---

Note liminaire : je n’y connais rien ni à l’USB ni aux ondes électromagnétiques, n’hésitez donc pas à me corriger.

Je suis tombé sur un [préservatif à prises USB](http://int3.cc/collections/frontpage/products/usbcondoms). L’idée m’a semblé saugrenue, mais après réflexion et quelques recherches, elle ne l’est pas du tout. Mon FirefoxPhone se recharge via sa prise USB. Il m’arrive donc de le recharger au boulot en le connectant à mon PC. Or, dès qu’il est déverrouillé, il est reconnu par le PC comme un disque externe (ce n’est pas le comportement par défaut, mais le plus pratique, donc je présume ne pas être seul à l’avoir réglé ainsi). Écrire un petit programme qui aspire automatiquement et discrètement le contenu de tout disque connecté en USB est l’affaire de quelques minutes. Chaque fois que je mendie un peu de courant auprès d’une prise que je ne contrôle pas totalement, toutes les photos de vacances qui sont sur ma carte SD pourraient donc être copiées. Le besoin d’interdire physiquement toute transmission de donnée via une prise me parait donc réel. Heureusement, au vu [de la spécification](http://fr.wikipedia.org/wiki/USB#Connectique_et_caract.C3.A9ristiques_.C3.A9lectriques), la parade ne semble pas très compliquée. Les prises USB disposent de quatre connecteurs, deux pour l’électricité, deux pour les données. Il suffit donc de créer un câble USB qui ne relie pas les connecteurs de données. La bidouille ne devrait pas être très compliquée pour qui s’y connait un peu en électronique.

\[ajout du 2013-09-15 14:10\] : padenot [me signale](https://twitter.com/padenot/status/379158579611066368) que « les canaux de donnée sont utilisés pour la négociation de l’ampérage que le chargeur doit fournir. C’est plus ou moins non-standard ». Donc ce préservatif risque fort de ne pas fonctionner :S Plusieurs fils dans les commentaires sur Hackers News [débatent de ce sujet](https://news.ycombinator.com/item?id=6379272).

Plus généralement, Brian Krebs signale que [tous les chargeurs peuvent être piégés](http://krebsonsecurity.com/2011/08/beware-of-juice-jacking/) pour aspirer les données de nos téléphones. À mesure que ceux-ci contiennent de plus en plus d’informations et jusqu’à nos empreintes digitales, charger couvert me semble devenir un précaution qui concerne tout le monde.

Karl de son côté [rapporte](https://twitter.com/karlpro/status/378933153261699072) l’histoire d’un automobiliste qui a découvert que sa [carte de télé-péage était lue un peu partout](http://www.forbes.com/sites/kashmirhill/2013/09/12/e-zpasses-get-read-all-over-new-york-not-just-at-toll-booths/) dans les rues de New-York, permettant de suivre sa voiture à la trace. Des expériences ont prouvé depuis longtemps qu’on peut lire à plusieurs dizaines de mètres que les puces RFID des cartes de transport ou des titres d’identité (votre passeport). Voici une preuve que c’est nos seulement faisable mais que ça se fait. Et pour répondre à Karl, une rapide recherche en ligne permet de trouver nombre de cages de Faraday portables, du simple porte-carte au sac pour ordinateur. Avec l’arrivée des cartes de paiement sans contact, et le nouveau risque qu’elles font courir, j’espère que ce genre de dispositif va très rapidement se généraliser (et surtout qu’on aura des études sur leur fiabilité réelle).

