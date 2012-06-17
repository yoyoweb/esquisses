---
  layout: post
  title: Le pari du Web
  published: true
  date: 2012-06-16 23:29
---

Ayé, la version Mozilla des applications Web arrive enfin sur GNU/Linux. Youpy. Et zut, car passé le premier enthousiasme lié à la nouveauté, cela signifie que l'heure a aussi sonné d'essayer de jeter un regard critique sur ce concept et de se poser la question : s'y mettre ? Ou pas ? Telle est la question.

Esquisses de réflexion.

## Dark Side of the Web

À vrai dire, les raisons de ne pas sauter le pas sont nombreuses.

Les applications Web sont nées de bidouilles, de détournements, et sont encore aujourd'hui loin d'être des citoyennes de première classe sur la vaste toile mondiale. Si le microcosme s'active en ce moment à réinventer le fil à couper le beurre pour les doter de toutes les capacités des applications *natives*, on est encore loin du compte. Surtout, elles manquent d'un élément essentiel : une bonne bibliothèque d'interface utilisateur. Et c'est une grave lacune que tout le monde semble aujourd'hui avoir acceptée. Les différentes propositions pour créer un langage permettant de décrire une interface utilisateur riche ont toutes été abandonnées. Ne reste plus que HTML, un langage de description de documents. Certes, on lui adjoint quelques composants d'interface supplémentaire, essentiellement pour simplifier la gestion de formulaires. Mais pas d'onglets, d'arbres, de zones redimensionnables… Pour créer l'interface des applications Web, on va devoir rester dans le domaine de la bidouille, du détournement, des lourdes bibliothèques en JavaScript. Triste.

Les limitations techniques sont nombreuses, et certaines ne semblent pas prêtes à sauter. Mais elles ne sont pas les seuls inconvénients de la plate-forme Web. Celle-ci pose également des questions en matière de souveraineté des utilisateurs sur leurs données. Les applications peuvent bien sûr stocker les données localement, sur le terminal où elles s'exécutent. Mais il y a fort à parier que la tentation de tout stocker sur le réseau va être forte. De confier nos données aux sites des éditeurs des applications. Ce qui ne fera que renforcer la fragmentation actuelle, le Web devenant de plus en plus composé d'immenses silos où sera stockée une partie de notre vie, et dont il sera difficile de s'échapper. On stockera tous ses documents chez Google, Facebook, Microsoft, Apple et consorts. Il sera difficile également d'être tranquille quant à la sécurité de nos données. Quid si l'entrepôt se fait cambrioler ? S'il « brûle » ? Si quelqu'un me vole mes clés et prend mes meubles en otage ? Ou si, plus simplement, l'entrepôt décide arbitrairement et soudainement de m'interdire l'accès ? Avec les applications Web, le risque de perte de contrôle sur nos données, voire de perte tout court, est plus élevé qu'avec les applications natives actuelles.

## À moitié plein

Mais, en tant que libriste, je vois également des avantages à l'utilisation du Web pour créer des applications. Le Web

* est **une plate-forme ouverte**, essentiellement bâtie sur des normes décidées en concertation par une partie des acteurs. Tout le monde peut librement consulter ces spécifications et les implémenter;
* est **une plate-forme largement adoptée**. Des centaines de millions de personnes se promènent tous les jours sur le Web en utilisant un navigateur moderne. Une application (bien) écrite pour le Web peut donc être utilisée simplement par des millions de gens, quelle que soit leur matériel et leur façon d'accéder à la toile;
* est **une plate-forme accessible**. Le coût d'entrée est des plus faible, aussi bien financièrement qu'en terme d'apprentissage. On peut facilement utiliser le réseau, on peut également simplement commencer à y créer des applications. Certes à mesure qu'elle gagne en puissance, la plate-forme se complexifie et devient plus difficile à programmer. Mais les connaissances requises pour créer un site ou une application Web basiques sont à la portée de pratiquement tout le monde;
* chaque composant de la plate-forme dispose d'implémentations libres elles aussi largement répandues. Tant sur le serveur (Apache et Nginx par exemple) que côté client (Firefox et le moteur Webkit, malheureusement souvent emprisonné sous des couches privatrices, équipent environ la moitié des internautes). Le Web est donc compatible avec la religion de celles et ceux qui accordent de l'importance à la liberté concédée par les logiciels qu'ils utilisent;
* est **une plate-forme propice à la découverte et à l'expérimentation, à la bidouille**. Nul besoin d'installer des logiciels supplémentaires pour étudier le fonctionnement du Web et commencer à le bidouiller. Les navigateurs contiennent nativement tout ce qu'il faut pour étudier la structure d'une page, écrire ses premières lignes de JavaScript, etc. Quiconque veut comprendre comment ça fonctionne, veut créer sur le Web, peut le faire, il n'y a pratiquement pas de barrière;
* est un cheval de Troie. Les tentatives de verrouiller une plate-forme, de contrôler strictement tout ce que font les utilisateurs, sont légions. Certaines ont plutôt le vent en poupe en ce moment, oui Apple c'est toi et tes sectateurs que je regarde. Mais aussi fermé soit le système d'exploitation, le Web y est toujours accessible. Que vous utilisiez un téléphone sous iOS, une machine de bureau sous Windaube ou un objet bidouillable non identifié sous [Haiku](http://haiku-os.org/), vous pouvez toujours vous connecter au Web, et donc utiliser les applications conçues pour cette plate-forme [^browser];

[^browser]: avec une grosse limitation, il faut disposer d'un navigateur capable d'exécuter de telles applications. Sur iOS par exemple, Apple interdisant tout autre navigateur que Safari, les WebApps ne pourront utiliser que les fonctionnalités HTML5 disponibles dans Safari.

# Boire ou conduire ?

Le Web est une plate-forme. Une fondation. Un jardin. Il n'est ni le fruit que l'on mangera ni la maison que l'on habitera. Il est ce terrain où chacun est libre de faire pousser ce qu'il veut, fruits ou cabane, maison ouverte ou prison. Chacun y est réellement libre. Parce qu'il ne faut demander la permission à personne. Parce que tous les outils sont disponibles. Le reste ne dépend que de nous.

Que faire alors ? Boycotter la plate-forme pour ses limitations techniques et les menaces pour la vie privée qu'elle porte ? Ou l'adopter en jugeant qu'elle offre des opportunités pour promouvoir les valeurs de liberté, d'égalité et de solidarité au cœur de la démarche du Logiciel Libre ? À chacun de trancher. La réponse a tout d'un pari. Le pari du Web.


