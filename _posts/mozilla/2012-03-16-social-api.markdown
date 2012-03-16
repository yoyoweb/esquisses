---
  layout: post
  title: Mozilla propose une API sociale
  published: true
  date: 2012-03-17 00:07:00
  tags:
  - Mozilla
  - MozLabs
  - Social API
---

Mozilla, qui suit un peu ce qui se passe en ligne, a remarqué qu'un certain nombre d'internautes utilisent de plus en plus le Web pour interagir entre eux via des sites dits de réseaux sociaux. La Fondation s'interroge naturellement sur les moyens d'améliorer l'expérience des internautes sur ces réseaux, améliorer signifiant pour elle leur donner davantage de contrôle sur ce qu'ils font, leurs données, etc, mais aussi rendre les interactions plus simples et plsu riches. Les réponses en la matière avaient pour l'instant été timides. Les laboratoires ont lancé il y a quelques années [F1](https://addons.mozilla.org/fr/firefox/addon/f1-by-mozilla-labs/), une extension pour partager des liens. Elle devrait bientôt être intégrée nativement à Firefox sous le nom de Share, mais force est de reconnaître qu'elle ne va pas très loin.

Michael Hanson a [annoncé aujourd'hui](http://mozillalabs.com/blog/2012/03/experimenting-with-social-features-in-firefox/) une initiative autrement plus ambitieuse&nbsp;: une proposition d'«&nbsp;[API sociale](https://wiki.mozilla.org/Labs/SocialAPI)&nbsp;» permettant au navigateur et à des réseaux sociaux d'interagir. La proposition est longue et encore à l'état de brouillon, je ne vais donc pas la traduire mais essayer d'en résumer certains points.

## Configurer des fournisseurs de services à intégrer dans le navigateur

Chaque site désirant utiliser l'API décrirait ses fonctionnalités via un fichier similaire au manifeste des application Web. Ce manifeste contiendrait la description du service et les URLs permettant de communiquer avec ses fonctionnalités. Lorsque l'internaute installera un fournisseur de service dans son navigateur, celui-ci considérera que ces URLs sont dignes de confiance. Le navigateur les autorisera à faire davantage de choses, comme par exemple envoyer des notifications qui s'afficheront dans l'interface. Selon la philosophie Mozilla, l'ajout de nouveaux fournisseurs de services, leur activation et leur désactivation, devrait être simple. La liste des services pourrait être affichée en permanence, si l'interface le permet (ie dans les versions de bureau des navigateurs).

Pour chaque service actif, le navigateur maintiendra une connexion permanente dans un espace sécurisé (*sandbox*) (techniquement, cela pourra utiliser les *[shared workers](http://dev.w3.org/html5/workers/#shared-workers-introduction)* en cours de définition dans HTML5). Outre la connexion au service, le processus dédié à chaque fournisseur pourra également stocker des données localement et interagir avec certaines partie de l'interface du navigateur (pour afficher des notifications par exemple).

Si l'écran le permet (navigateurs de bureau ou tablettes), une barre latérale permettra aux fournisseurs d'afficher du contenu à leur guise. Ils pourront également ouvrir des espaces épinglables dans l'interface —&nbsp;pensez à une fenêtre de discussions flottant en permanence dans un coin de votre navigateur. 

## Partager des mises à jour

C'est le suite de Firefox Share&nbsp;: un moyen simple de recommander un contenu. Dans son manifeste, chaque fournisseur indique s'il fournit ce service. Le navigateur propose alors des moyens (boutons, menu contextuel) de partager un contenu, avec la liste des fournisseurs disponibles. 

## Envoyer et recevoir des notifications d'activités

Les services pourront envoyer des notifications que le navigateur affichera à l'internaute. La façon d'afficher ces notifications devra être contrôlable de façon fine.

## Afficher le statut des contacts et permettre de dialoguer avec eux

Les fournisseurs pourront également indiquer qu'ils disposent d'une API de gestion de contacts. On pourra ainsi gérer ses contacts sur les différents réseaux sociaux directement depuis son navigateur —&nbsp;je me souviens que des Labs avaient déjà mené une expérience en ce sens il y a des années, hélas abandonnée comme tant d'autres.

## Interactions avec le reste du Web

Chaque fournisseur sera cantonné à un bac à sable, d'où il ne saura pas ce que fait l'utilisateur. Les pages Web consultées pourront cependant indiquer qu'elles souhaitent interagir avec un réseau social. L'internaute indiquera alors au cas par cas ce que chaque page / site peut faire. Ça part d'une bonne volonté, mais je pense que c'est une protection illusoire. La majorité des gens sera vite lassée des demandes d'autorisations et autorisera par défaut tous les sites à dialoguer avec tous les réseaux activés. 

## Interface

Tout comme pour les fonctionnalités, la réflexion sur l'interface commence juste. Le navigateur intégrera sans doute une zone permanente pour les notifications provenant des réseaux, et des composants comme les popups épinglables ou une barre latérale ou autre, pour afficher des contenus spécifiques, flux de nouvelles ou statut des contacts.

## Enfin le temps perdu qu'on ne rattrape plus

Pour l'instant, cette API sociale reste une annonce des Labs. Elle reprend, au moins en partie, nombre de précédents projets lancés en fanfare et rapidement tombés dans l'oubli. J'ai été suffisamment échaudé pour ne pas m'enthousiasmer trop vite. Cependant, avec la monté en puissance du groupe de travail sur l'identité et les rapports sociaux, et la déferlante d'APIs auxquelles travaille Mozilla en ce moment, peut-être que cette fois-ci sera la bonne et que Firefox se dotera de moyen d'améliorer les interactions avec les réseaux sociaux. Stallman seul le sait.

Comme d'habitude chez Mozilla, la suite des réflexions et de la conception va se faire de façon relativement ouverte. Si le sujet vous intéresse, n'hésitez pas à vous abonner à la liste *ad hoc*, dont je ne donnerai pas l'adresse, c'est un Google Group, il faut donc un compte Google pour s'y inscrire. Grrrr.

