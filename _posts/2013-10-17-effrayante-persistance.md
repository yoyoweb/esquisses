---
  layout: post
  title: Effrayante persistance
  published: true
  date: 2013-10-17 13:14:00
---

[« Les URI cools ne changent pas »](http://www.w3.org/Provider/Style/URI.html). Ainsi parla TBL, et sans être dogmatique, je trouve que c’est un conseil qui se tient. Le Web est une fragile toile reliant des contenus les uns aux autres, changer l’URI d’un contenu brise tous les liens qui y menaient, l’exclut de la toile et la fragilise. On ne devrait jamais changer l’URI d’un contenu une fois qu’il est publié.

Mais cela signifie qu’on n’a aucun droit à l’erreur. Toute URI publiée devra rouiller sur place. Cela oblige à la choisir avec soin, à y réfléchir à deux fois. Pour un procrastinateur dans mon genre qui n’ose jamais rien faire de peur de mal faire, c’est réellement bloquant. Je suis censé mettre en ligne depuis des mois un petit site de photos, et remets sans cesse la tâche au lendemain car je n’arrive à me décider ni sur le logiciel à utiliser pour générer les galeries, ni sur le modèle des URI. Des dossiers thématiques ? Une arborescence chronologique ? Savoir que ce choix m’engage pour des années me pétrifie.

Et pourtant, il y a plein de raisons pour lesquelles on voudrait changer une URI. Si par exemple elle contient le titre du contenu et qu’on désire modifier un titre maladroit. Est-on condamné à conserver l’URI avec le premier titre ? Les toiles d’araignées sont de soie, non de verre, et le Web ne devrait pas être si fragile.

Je suis bien sûr excessif, le Web fournit des mécanismes, les redirections, qui donnent le droit à l’erreur. Mais je n’aime guère ces mécanismes, car ils obligent à gérer, en plus des contenus, des méta-données liées au serveur. Le jour où je change de serveur Web, il me faut migrer tous les fichiers contenant les redirections (l’idéal serait de pouvoir inclure cette meta-donnée dans le fichier de contenu, mais c’est un autre débat). Bref, la gestion de redirections me semble fragile et peu pérenne.

Un autre mécanisme, élégant mais bidouilleux, pourrait être de dire, peu importe l’URL, seule l’URN ne devrait pas changer, et être incluse dans l’URL. Nombre de CMS le permettent déjà. Ainsi dans l’URL `http://toto.org/ralerie/1234-titi-est-mechant`, seul compte `1234` que le serveur est capables d’extraire. Je peux modifier l’URL en `http://toto.org/bisoux/1234-titi-est-gentil` de manière transparente.

Tout ça pour dire que parmi les règles de bonne conduite du Web, je trouve certaines légèrement effrayantes et capable de dissuader de publier. Mais c’est juste parce que je suis flippé de nature ;)

Référence : « What is the URI persistence policy of your Web site? » [interroge Karl](https://twitter.com/karlpro/status/390778662129500160)

