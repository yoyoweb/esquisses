---
  layout: post
  title: Fils de Pong
  published: true
  date: 2013-05-03-21:53:00
  tags:
  - Mozilla
  - HTML5
  - Jeux
---

_Avertissement : cette note parle de jeux, un secteur auquel je ne connais strictement rien. Elle est donc sans doute bourrée d’erreurs, n’hésitez pas à me les signaler, merci._

Mozilla et Epic Games avaient [créé la sensation](http://blog.mozilla.org/blog/2013/03/27/mozilla-is-unlocking-the-power-of-the-web-as-a-platform-for-gaming/) en Mars en présentant [Epic Citadel](http://www.unrealengine.com/html5/), un jeu qui fonctionne dans le navigateur. Epic Citadel utilise le moteur de rendu Unreal Engine 3, écrit en C++. Le code de celui-ci a été converti en JavaScript via Emscripten, et s’exécute pratiquement sans perte de performances dans les [versions nocturnes de Firefox](http://nightly.mozilla.org/) grâce à son moteur JavaScript optimisé pour [asm.js](http://esquisses.clochix.net/2013/02/19/asmjs/). Cette démonstration est enfin [disponible en ligne](http://www.unrealengine.com/html5/) et vous pouvez la tester. Pour l’instant, du fait de bugs dans les implémentations de WebGL des autres navigateurs, elle ne semble malheureusement fonctionner parfaitement que dans Firefox, mais elle devrait également bientôt tourner dans tous les navigateurs supportant WebGL (Opéra, Chrome, Safari et peut-être même IE dans une dizaine d’années). Pour en savoir plus, n’hésitez pas à aller lire cet [article de Vladimir Vukićević](http://blog.bitops.com/blog/2013/05/01/unreal-javascript/) et l’annonce d’[Epic Games](http://www.unrealengine.com/en/news/epic_games_releases_epic_citadel_on_the_web/).

La sortie d’Epic Citadel n’est pas qu’un épiphénomène, une démonstration de faisabilité, mais un symptôme parmi beaucoup d’autres de l’effervescence qui règne en ce moment dans le monde des jeux en HTML5. Pour preuve ces quelques autres actualités que j’ai vu passer ces derniers jours :

- pour encourager le développement de jeux en HTML, une [catégorie dédiée a été créée sur MDN](https://developer.mozilla.org/en-US/docs/Games). Toute aide pour enrichir cette documentation et la traduire est évidemment la bienvenue ;

- [Turbulenz vient de libérer](http://news.turbulenz.com/post/49430669886/turbulenz-engine-goes-open-source) sous licence MIT le moteur de jeux 2D et 3D qu’ils développent depuis plusieurs années. Le code, très complet, [est sur Github](https://github.com/turbulenz/turbulenz_engine) ;

- Gamua est une société qui développe entre autre Starling et Sparrow, des moteurs 2D libres pour écrire respectivement des jeux Flash en ActionScript et iOS en Objective C. Ils ont annoncé une [version Web de Starling](http://gamua.com/blog/2013/05/a-bird-for-the-modern-web), basée sur TypeScript (un sur-ensemble typé de JavaScript, impulsé par Microsoft) et WebGL. Elle partagera une API commune avec Starling et Sparrow, pour simplifier la création de jeux fonctionnant dans les trois environnements ;

- parmi les autres signes du déclin de Flash, Unity a annoncé il y a peu qu’ils [cessaient le support de cette plate-forme](http://blogs.unity3d.com/2013/04/23/sunsetting-flash/) ;

- les moteurs de jeu en HTML5 se multiplient, un site leur est désormais consacré, [HTML5 Game Engine](http://html5gameengine.com/) ;

- Microsoft a également bien compris l’importance des jeux pour promouvoir ses technologies. Voici par exemple un article de [présentation de Phaser](http://jessefreeman.com/game-dev/building-a-html5-game-with-phaser/), autre moteur de jeu 2D en TypeScript et JavaScript ;

- et enfin si vous voulez des démos, voici les gagnants d’un [concours de développement de jeux HTML5](http://blog.udacity.com/2013/05/html5-game-development-contest-winners.html).

On célèbre ces jours-ci les vingt ans de la libération du Web. Quelques mois après cette libération, et sans aucun rapport, sortait Doom, qui ouvrait une nouvelle étape dans l’univers des jeux vidéos, en commençant à populariser les jeux multi-joueurs en 3D. Ce sont probablement deux des faits marquants de l’informatique en 1993. J’apprécie le clin d’œil de leur mariage vingt ans plus tard.

Dans le domaine techniquement pointu, HTML5 est peu à peu en train d’assoir sa crédibilité. De plus en plus d’outils sont disponibles. Ils vont permettre de créer des jeux qui tourneront sur tous nos écrans, ordinateurs, tablettes, téléphones, télévisions… Les outils sont là, reste à coder les jeux, et ça c’est votre boulot, alors hop ! Moi, je m’en vais réciter des mantras. _Le Web est la plate-forme et Firefox (OS) son prophète. ad libitum_

