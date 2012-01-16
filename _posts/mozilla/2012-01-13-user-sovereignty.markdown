---
  layout: post
  title: "Mozilla : pistes pour des services respectueux de nos données"
  published: true
  date: 2012-01-15 13:15:00
  tags:
  - Mozilla
  - identité
  - vie privée
---

Résumé des épisodes précédents&nbsp;: Mozilla  a sauvé le <del>monde</del>Web une première fois en relançant la compétition dans le domaine des navigateurs grâce à Firefox. Mais les super-méchants ne se sont pas découragés et de nouvelles menaces planent sur le <del>monde</del>Web&nbsp;:des systèmes d'exploitation pour téléphones qui empêchent les utilisateurs de faire ce qu'ils veulent, des services en ligne qui phagocytent toutes les données et acquièrent une emprise croissante sur leurs internautes, une inculture qui empêche les gens de comprendre ce qu'est le Web et donc de se l'approprier, de l'utiliser pour créer et non juste pour consommer, *et cœtera*. Heureusement les Forces du Bien ne restent pas inactives et ont décidé d'aller en 2012 défendre leurs valeurs partout où la liberté du Web est menacée. Cela va passer entre autres par la création de services en ligne plus respectueux de leurs utilisateurs (création directe par Mozilla ou soutien à des projets qui vont dans ce sens, via les incubateurs [Drumbeat](http://www.drumbeat.org)[^drumbeat] et [WebFWD](http://webfwd.org)[^webfwd]). Mais qu'est-ce qu'un service Web respectueux de ses utilisateurs&nbsp;? Ben Adida a fourni un premier élément de réponse dans un article où il annonce la création au sein de Mozilla d'un groupe de travail pour réfléchir à offrir la meilleure protection possible aux données que Mozilla hébergera. Il suggère également quelques lignes directrices en la matière que devront suivre tous les projets de Mozilla.

Une des choses que j'aime de Mozilla, c'est sa relative ouverture et transparence. La réflexion sur le sujet est ouverte, tous les avis sont les bienvenus. Dans l'espoir d'aider au débat, j'ai très rapidement traduit l'article de Ben et son introduction par Mitchell. Je pousserai cette traduction sur Github, donc n'hésitez pas si cela vous intéresse à l'améliorer et la reprendre (ping Frenchmoz).

Toutes les notes de bas de page sont de mon fait, et ne figurent pas dans les articles originaux.

Outre la traduction, ces articles appellent des réactions, mais j'ai trop peu de temps libre ce ouikende pour disserter. 
Voici déjà les deux articles, bonne lecture.

[^drumbeat]: Drumbeat se consacrant désormais à la mission d'éduquer à la culture Web, je ne suis pas sûr qu'il continue à soutenir beaucoup d'autres projets, comme il le faisait à ses débuts;
[^webfwd]: ainsi par exemple d'[Open Photo](http://theopenphotoproject.org/), une alternative libre à Flickr ou de [Verese](http://verese.net/) qui gère des micro-paiements au sein d'une communauté;


<section class="cite" vocab="http://schema.org/" about="http://blog.lizardwrangler.com/2012/01/13/user-sovereignty-for-our-data/" typeof="Article">
<header><cite>[User Sovereignty for our Data](http://blog.lizardwrangler.com/2012/01/13/user-sovereignty-for-our-data/)</cite> par <span class="author vcard"><span property="dc:contributor" class="fn">[Mitchell Baker](http://blog.lizardwrangler.com/)</span></span></header>
<blockquote property="articleBody" cite="http://blog.lizardwrangler.com/2012/01/13/user-sovereignty-for-our-data/">
<div markdown="1">
## Être maîtres de nos données

Nos expériences en ligne s'accompagnent de plus en plus de données sur nous. Nous en créons certaines. Parfois ce sont nos amis et nos connaissances qui les créent, et parfois les services que nous utilisons créent des données sur nous. D'un côté, cela rend possible toutes sortes de nouvelles applications excitantes. De l'autre, l'explosion des données personnelles a quelques aspects très troublants. La capacité des fournisseurs de service de *cloud computing* et de traitement des *big data* de surveiller, journaliser, stocker, utiliser, corréler et vendre des informations sur ce que nous sommes et ce que nous faisons a des implications importantes tant pour la société que pour les individus.

À l'heure actuelle, il n'existe pas de moyen me permettant de partager de l'information sur moi et de garder le contrôle de cette information. Je partage l'information à mon sujet en la plaçant quelque part où quelqu'un d'autre décide de toutes les règles. Ce «&nbsp;quelqu'un d'autre&nbsp;» est l'application. La plupart des gens pensent à Facebook ou Google, mais le problème dépasse largement l'un ou l'autre. C'est aujourd'hui un problème de l'architecture des données des utilisateurs, et il concerne l'ensemble du réseau. Pensez aux gros sites où les utilisateurs donnent leur avis sur des produits, ou à n'importe quelle application où vous passez beaucoup de temps. Pensez à n'importe quel réseau social auquel vous êtes connecté. Le seul moyen pratique d'avoir un endroit à soi sur ces sites est de leur apporter nos données et de n'avoir d'autre contrôle que celui que les développeurs de l'application ont décidé de nous donner.

Ces problèmes ont des implications importantes pour Mozilla.

D'abord, cela signifie que nous devrions inventer de nouvelles choses dans le domaine des données utilisateur. Pour réellement aider les gens à gérer et partager leurs données, Mozilla devra également leur offrir le choix de stocker leurs données dans le nuage de façon à ce que d'autres services puissent y accéder avec leur accord. Cela implique de nouveaux défis. C'est important que nous les relevions et y répondions bien. Si nous développons et offrons de quoi gérer correctement les données des utilisateurs dans le nuage, nous aiderons à garantir le choix et la souveraineté de l'utilisateur dans de nouveaux pans de la vie en ligne. Chacun d'entre nous devrait pourvoir choisir en connaissance de cause où et comment nos données sont stockées et gérées. Aucune autre organisation n'a à la fois la capacité de réaliser quelque chose de complètement centré sur la souveraineté des utilisateurs plutôt que sur le profit financier, et la capacité d'avoir un vaste impact. La présence de Mozilla dans le *cloud* nous permettra de remplir notre mission dans de nouvelles dimensions importantes de la vie en ligne.

Ensuite, cela signifie que notre approche de la gestion des données utilisateur doit être différente de la norme actuelle dans l'industrie Web. Elle doit vous placer au centre, disposer vos données tout autour de vous, et vous laisser partager ces données avec les applications que vous choisissez, selon les termes que vous choisissez. Notre approche ne devrait enregistrer les données de l'utilisateur que si cela a un bénéfice mesurable pour lui, plutôt que de tout collecter dans l'espoir que des applications de *data mining* extraient de la valeur utile à quelqu'un d'autre. Elle devrait permettre aux gens de déterminer si leurs données sont accessibles à d'autres. Le principe de [la souveraineté de l'utilisateur](http://blog.lizardwrangler.com/2011/08/04/extending-our-reach-many-layers-of-user-sovereignty/)[^extending] influencera la façon dont nous concevons chaque aspect de nos offres. Les offres de Mozilla doivent incarner les valeurs du [Manifeste de Mozilla](http://www.mozilla.org/about/manifesto.fr.html), et nos [principes de respect de la vie privée](https://wiki.mozilla.org/Privacy/Roadmap_2011#Operating_Principles:).

Mon collègue Ben Adida (responsable technique du domaine de l'identité et de données utilisateur, et un de nos experts en cryptographie) a écrit  [un article](http://blog.mozilla.com/privacy/2012/01/13/mozilla-to-offer-new-user-centric-services-in-2012/) décrivant nos réflexions sur la création de tels produits.
</div>
</blockquote>
<footer><cite>[User Sovereignty for our Data](http://blog.lizardwrangler.com/2012/01/13/user-sovereignty-for-our-data/)</cite> par <span class="author vcard"><span property="dc:contributor" class="fn">[Mitchell Baker](http://blog.lizardwrangler.com/)</span></span></footer>
</section>

Et voici donc l'article de Ben&nbsp;:

<section class="cite" vocab="http://schema.org/" about="http://blog.mozilla.com/privacy/2012/01/13/mozilla-to-offer-new-user-centric-services-in-2012/" typeof="Article">
<header><cite>[Mozilla to Offer New User-Centric Services in 2012](http://blog.mozilla.com/privacy/2012/01/13/mozilla-to-offer-new-user-centric-services-in-2012/)</cite> par <span class="author vcard"><span property="dc:contributor" class="fn">[Ben Adida](http://ben.adida.net/#me)</span></span></header>
<blockquote property="articleBody" cite="http://blog.mozilla.com/privacy/2012/01/13/mozilla-to-offer-new-user-centric-services-in-2012/">
<div markdown="1">
## Mozilla va créer de nouveaux services centrés sur l'utilisateur en 2012
Chez Mozilla, nous nous concentrons depuis longtemps sur le développement de logiciels qui donnent aux utilisateurs la maîtrise de leurs vies en ligne. Cela signifie les concevoir de manière à fournir aux gens une meilleure connaissance de comment fonctionne le Web, des fonctionnalités logicielles uniques pour personnaliser leur expérience en ligne et le contrôle sur leurs données personnelles. Ces derniers temps, nous avons réfléchi à [comment la souveraineté de l'utilisateur s'est étendue pour ne plus dépendre seulement du navigateur](http://blog.lizardwrangler.com/2012/01/13/user-sovereignty-for-our-data/). De nombreux sites Web stockent pour l'utilisateur l'ensemble de ses données et de ses actions. Même si le navigateur est complètement contrôlé par l'utilisateur, beaucoup de services que l'utilisateur apprécie ne le sont pas. Parfois, ces services Web gèrent les données d'une manière dont la valeur est questionnable pour l'utilisateur, et parfois même à son détriment.

Il est clair que Mozilla a besoin de franchir une étape et de fournir, en plus du navigateur Firefox, certains services pour augmenter le contrôle de l'utilisateur sur son expérience en ligne et ses données personnelles. La présidente de Mozilla, Mitchell Baker, [l'a expliqué ainsi&nbsp;](http://blog.lizardwrangler.com/2011/08/04/extending-our-reach-many-layers-of-user-sovereignty/)[^extending]:

[^extending]: [version française sur le blog de FrenchMozila](http://blog.frenchmozilla.org/index/post/2011/08/04/%C3%89tendre-notre-champ-d-action-%3A-le-pouvoir-%C3%A0-l-utilisateur-sur-tous-les-plans) 

> > Je crois qu'il est impératif que nous développions d'autres produits. Nous avons besoin, à plusieurs niveau de notre vie sur Internet, de plateformes ouvertes, au code source libre, interopérables, au service du public et basées sur des standards. Nous choisissons d'emmener nos valeurs là où sont les gens.

Les services que nous imaginons et sur lesquels nous travaillons dur, afin de les lancer dans les prochaines semaines et les prochains mois, incluent&nbsp;: une approche innovante de [l'identité](https://browserid.org/), un [système d'exploitation pour les terminaux mobiles basé sur le Web](https://wiki.mozilla.org/B2G), et une [boutique d'applications](https://developer.mozilla.org/en-US/apps). Pour offrir ces services, nous aurons besoin de stocker des données des utilisateurs sur les serveurs de Mozilla à bien plus grande échelle que nous le faisons actuellement. Cela nécessite beaucoup de soin et de réflexion. Nous avons commencé à chercher comment le faire et avons essayé quelques prototypes. Je voudrais vous dire ce à quoi nous pensons et solliciter votre avis et vos idées.

### Notre approche actuelle —&nbsp;Firefox Sync

Mozilla stocke déjà des données chiffrées dans le cadre de Firefox Sync, qui permet à des millions d'utilisateurs de Firefox de synchroniser entre de multiples installations de Firefox —&nbsp;dont Firefox Mobile&nbsp;— leurs marque-pages, leur historique de navigation et leurs mots de passe. Nous sécurisons ces données en utilisant un chiffrement plus avancé que celui utilisé par les institutions financières. Typiquement, les banques chiffrent les données transférées (SSL)&nbsp;: vous données sont chiffrées entre votre navigateur et les serveurs de la banque. Une fois sur le serveur de la banque, elles sont naturellement déchiffrées. En comparaison, Firefox Sync utilise un chiffrement au niveau de l'application&nbsp;: vos données sont chiffrés par Firefox avant d'être envoyées sur le réseau, et elles restent chiffrées une fois arrivées sur nos serveurs, et lorsqu'elles sont stockées sur nos disques. Seul votre Firefox peut les déchiffrer. Mozilla n'a pas la clé qui permet de les déchiffrer.

Cela signifie que nous ne voyons jamais vos données. Si un de nos serveurs était piraté, ou si quelqu'un réussissait à subtiliser quelques disques dans un de nos *datacenters*, vos données resteraient malgré tout à l'abri des yeux indiscrets. Peu d'autres société en font autant pour assurer la sécurité de vos données.

Les nouveaux services auxquels nous pensons vont, lorsque cela sera possible, continuer à utiliser ce niveau de sécurité des données.

### Les limites du chiffrement au niveau de l'application

Si nous ne pouvons pas voir vos données, alors vous êtes incroyablement à l'abri, mais nous ne pouvons pas non plus faire grand chose pour vous. Le chiffrement au niveau de l'application est comme le coffre-fort que vous cachez dans votre placard&nbsp;: vous pouvez y mettre des objets de valeur et vous pouvez les récupérer si vous êtes là en personne, mais vous ne pouvez pas facilement demander au téléphone à l'un de vos colocataires de vous dire combien de liquide est stocké dans le coffre. En comparaison, c'est facile d'appeler un colocataire et de lui demander de vous lire un numéro de téléphone que vous avez laissé sur la table de la cuisine. Certaines données ont tellement de valeur que vous devez les stocker dans un coffre-fort. D'autres données peuvent ne pas être aussi sensibles, et être un peu plus utiles si vous pouvez obtenir de l'aide pour les gérer, les retrouver et les traiter. Quelque chose d'aussi simple que de vous envoyer des rappels pour les anniversaires de vos amis nécessite que le service puisse accéder à ces données lorsque vous n'êtes pas connecté.

J'ai écrit plus tôt sur [les limitations du chiffrement pour mettre à l'abri les données](http://benlog.com/articles/2011/12/21/encryption-is-mostly-not-magic/)[^encryption]. Le chiffrement n'est pas de la magie. Il n'est pas approprié pour toutes les applications. Si nous voulons pouvoir fournir des services alternatifs réalistes, qui montrent ce que peut signifier la souveraineté de l'utilisateur, cela va nécessiter de stocker des données des utilisateurs sur nos serveurs, même sans chiffrement au niveau de l'application.

[^encryption]: [Version française sur le blog de FrenchMozilla](http://blog.frenchmozilla.org/index/post/2011/12/23/Chiffrer-pour-s%C3%A9curiser%E2%80%AF-%E2%80%94-pas-si-simple%E2%80%A6)

### Principes de conception

Nous proposons quelques principe de conception de départ&nbsp;:

- **un bénéfice clair pour l'utilisateur&nbsp;**: les données que nous collectons devraient toujours offrir à l'utilisateur un bénéfice clair et direct. Le stockage agressif de données «&nbsp;juste au cas où on en aurait besoin plus tard&nbsp;» n'est pas acceptable;
- **un inventaire des données&nbsp;**: nous devrions toujours savoir quelles données nous collectons, où et comment elles sont stockées et pourquoi le stockage de chacune est crucial pour la fonctionnalité pour l'utilisateur final. Nous devrions nous assurer que les utilisateurs puissent facilement accéder à cet inventaire, le comprendre, le mettre à jour ou le supprimer;
- **minimiser les données que le serveur peut consulter&nbsp;**: si nous pouvons implémenter une fonctionnalité donnée sans jamais envoyer de données au serveur, ou en utilisant un chiffrement au niveau de l'application, alors nous le ferons;
- **minimiser la conservation des données&nbsp;**: nous devrions stocker les données pour une durée aussi courte que possible. En particulier, si nous avons besoin de serveurs uniquement pour fournir un point de transit pour des données, alors ces données devraient uniquement transiter par les serveurs, et ne jamais y être stockées;
- **agréger à chaque fois que c'est possible&nbsp;**: nous étudierons si nous pouvons implémenter la fonctionnalité en utilisant des données agrégées à partir d'un nombre significatif d'utilisateurs, plutôt qu'en conservant des données individuelles. (Étant donné la richesse de ces jeux de données, nous ne pouvons pas prétendre que les rendre anonymes est particulièrement utile pour protéger les utilisateurs individuels);

Nous voulons passer en revue chaque fonctionnalité que nous envisageons en utilisant sur les procédures existantes que le projet Mozilla connait déjà bien&nbsp;: Bugzilla. Les questions seront suivies dans Bugzilla, rattachées à un ticket principal que nous appelerons probablement «&nbsp;Sûreté des données&nbsp;».

### Personnes impliquées

Les personnes suivantes se sont rassemblées pour créer une Équipe de Sécurité des Données, afin de développer ces idées et de les inclure dans tous nos produits&nbsp;:
- **Jay Sullivan**, en charge de la définition des produits Mozilla qui incarneront nos valeurs;
- **Sid Stamm**, qui gère l'ingénierie de la gestion de la vie privée dans Firefox et sur la plate-forme Web;
- **Jonathan Nightingale**, chargé du développement de Firefox;
- **Alex Fowler**, qui s'occupe de gestion de la vie privée et des politiques de confidentialité, en se concentrant sur l'amélioration de la gestion des informations;
- **Brendan Eich**, responsable depuis le premier jour de la direction technique du Projet Mozilla;
- **Michael Coates**, qui s'occupe de la securité des infrastructures et supervise les applications, les serveurs et les réseaux;
- **Chris Beard**, chargé des programmes de marketing et d'engagement;
- **David Ascher**, qui mène la réflexion au sein de Mozilla sur comment les utilisateurs découvrent le Web et y partagent;
- **Ben Adida**, c'est moi, je suis responsable des travaux sur l'identité;

Nous savons que cette équipe devrait grossir pour inclure des individus avec des parcours plus divers, des gens de Mozilla et d'ailleurs, et des gens du monde entier. Nous aurons également besoin de nous soucier des différentes législations et usages locaux[^accord] pour concevoir et héberger nos services.

[^accord]: pour le coup, utiliser la «&nbsp;règle de proximité&nbsp;» et accorder avec le nom le plus proche me semble beaucoup plus joli que d'écrire «&nbsp;les différents législations&nbsp;»;

### Au delà de la simple conformité

La sûreté des données nécessite d'être attentif à la conformité avec les lois et les bonnes pratiques, mais notre but est d'aller au delà. Nous allons impliquer nos architectes logiciels et nos experts en sécurité les plus expérimentés pour déterminer comment créer une meilleur protection de la vie privée. Ces discutions et ces itérations, comme toutes celles concernant le sécurité et la vie privée, seront par défaut publiques, afin qu'elles puissent être auditées, tout comme l'est notre code source (à l'exception naturellement de lorsque ces révélations donneraient à des attaquants une longueur d'avance, auquel cas nous conserverons ces informations temporairement secrètes). De plus, comme tous les projets Mozilla, nous impliquerons nos utilisateurs dans le processus de définition de l'architecture qui permettra de leur donner davantage de maîtrise. Il est crucial qu'ils comprennent les solutions que nous proposons, les bénéfices qu'elles apportent, et comment leurs données sont utilisées pour arriver à ces bénéfices.

### Coller à nos principes

La souveraineté de l'utilisateur requiert un excellent navigateur et un certain nombre de services centrés sur l'utilisateur. Nous aimerions créer certains de ces services, et nous avons l'intention de le faire avec autant de dévouement que toujours envers nos [principes de respect de la vie privée&nbsp;](https://blog.mozilla.com/privacy/2011/01/12/mozillas-privacy-data-operating-principles/): pas de surprise, de vrais choix, des réglages sensés, des données limitées et le contrôle par l'utilisateur. Nous ne vendrons ni ne donnerons vos données. Nous expliquerons toujours quelles données nous stockons et pourquoi nous les stockons. Nous vous laisserons toujours partir et emmener vos données avec vous, et nous vous expliquerons toujours quel bénéfice vous obtiendrez de la collecte de ces données.

Vos réactions sont les bienvenues, via des articles, des messages sur la liste [dev.planning](https://lists.mozilla.org/listinfo/dev-planning) ou sur Twitter en utilisant le *hashtag* #mozdatasafety.
</div>
</blockquote>
<footer><cite>[Mozilla to Offer New User-Centric Services in 2012](http://blog.mozilla.com/privacy/2012/01/13/mozilla-to-offer-new-user-centric-services-in-2012/)</cite> par <span class="author vcard"><span property="dc:contributor" class="fn">[Ben Adida](http://ben.adida.net/#me)</span></span></footer>
</section>
