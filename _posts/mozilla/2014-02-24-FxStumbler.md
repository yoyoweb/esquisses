---
  layout: post
  title: A Firefox OS client for Mozilla Location Service
  published: true
  date: 2014-02-24 22:34:00
  references:
  tags:
  - Mozilla
---

(french version below)

The best way to get the location of a device is to use GPS. But lot of devices don’t have a GPS chip, and GPS has some limitations. For example, sometimes getting an accurate position may take up to ten minutes, especially in town, or with the low-end chipset. So it’s a common practice to try to locate the device by using other data, like the mobile and Wifi networks around. The device gets the list of surrounding networks and query an online database that stores the position of millions of networks.

Every big mobile carrier owns such a database, but they are not freely accessible. Moreover, query such service has privacy implications: the remote database may identify the device and track its positions.

So [Mozilla decided](https://blog.mozilla.org/services/2013/10/28/introducing-the-mozilla-location-service/) to create its [own free location service](https://location.services.mozilla.com/), and use it to improve geolocation in Firefox and Firefox OS. Mozilla wants to build its own free database of every mobile cell tower and every Wifi access point in the world.

Every Android user can help populate the database by installing an application, [MozStumbler](https://github.com/mozilla/MozStumbler/releases) that collect data about networks surrounding the phone and send them to the Mozilla Location Service.

I found it unfortunate that such an application wasn’t available for Firefox OS, so I decided to write it myself, and created [FxStumbler](https://github.com/clochix/FxStumbler).

Unfortunately, to access mobile network information, the application needs privileges that only carriers can grant for now. So the application cannot be installed from a Marketplace. If you want to try it, you have to put your phone in Developer mode and install the application with the application manager. So for now, installation needs some technical skill. See the [README](https://github.com/clochix/FxStumbler#fxstumbler) for more details on how to install it.

So, if you are the lucky owner of a Firefox Phone and feel adventurous, you give it a try and help feed the location service database. It would be awesome if more and more blue dots enlighten [the map](https://location.services.mozilla.com/map).

Please note that this is only one of my pet project, and I don’t have much time to work on it. So any help would be greatly appreciated, to fix bugs, improve documentation, add translations and, why not, some new feature.

If you have questions, don’t hesitate to contact me, I’m often available on IRC.

---

La meilleure solution pour connaitre la position géographique d’un terminal est d’utiliser le GPS. Mais de nombreux terminaux n’ont pas de puce GPS, et même sur ceux qui en possèdent une, son utilisation a quelques limitations. La puce doit localiser trois satellites et calculer sa position à partir de la leur, ce qui peut prendre une dizaine de minutes si les conditions météo sont mauvaise, ou avec des puces bon marché. Il est dont courant d’essayer de déterminer la position du terminal en analysant d’autres informations de son environnement, les réseaux mobile et Wifi disponibles. Des bases de données existent qui contiennent la position de millions d’antennes téléphoniques et de points d’accès Wifi. Il suffit d’interroger ces bases en leur envoyant la liste des réseaux environnant le terminal.

Tous les gros acteurs de la téléphonie possèdent ce type de base de données, qui permettent d’améliorer la géo-localisation des téléphones. Mais ce système pose des soucis en matière de respect de la vie privée : le service interrogé pourrait identifier le terminal et suivre son propriétaire. Par ailleurs, l’accès à ces bases n’est pas libre, et peut donc être restrient.

Pour pallier ces problèmes, Mozilla [a décidé](https://blog.mozilla.org/services/2013/10/28/introducing-the-mozilla-location-service/) de créer [sa propre base de données](https://location.services.mozilla.com/), évidemment libre, et de l’utiliser pour améliorer la géo-localisation de Firefox et de Firefox OS.

La base est alimentée via une application pour Android, [MozStumbler](https://github.com/mozilla/MozStumbler/releases). Chaque utilisateur d’Android peut l’installer et participer à la collecte pour enrichir le service de Mozilla.

Ironiquement, l’application officielle n’est pas disponible pour Firefox OS. J’ai donc décidé d’écrire une application similaire pour alimenter le service, en utilisant les APIs Web de Firefox OS, et c’est ainsi qu’est né [FxStumbler](https://github.com/clochix/FxStumbler).

Malheureusement, accéder aux informations du réseau mobile auquel le téléphone est connecté demande certains privilèges que seul un opérateur téléphonique peut allouer à une application, en vertu du modèle de sécurité de Firefox OS. Je ne peux donc pas distribuer FxStumbler via l’épicerie de Mozilla. Si vous voulez l’essayer, il faut activer le mode « développeur » sur votre téléphone, et installer l’application via le nouveau gestionnaire d’applications de Firefox. Cela demande donc pour l’instant quelques compétences techniques. Le fichier [lisez-moi](https://github.com/clochix/FxStumbler#fxstumbler) détaille la procédure.

Si vous êtes un heureux possesseur de Firephone, et avez l’esprit aventureux, n’hésitez pas à essayer le bouzin et à contribuer à enrichir la base de données. Ça serait sympa de voir [la carte](https://location.services.mozilla.com/map) se couvrir de points bleus.

J’ai codé ce machin à l’arrache, et n’ai pas beaucoup de temps à lui consacrer, donc il est rustique et bancal. Toute aide est la bienvenue pour corriger les problèmes, améliorer la documentation, ajouter des traductions, ou de nouvelles fonctionnalités si le cœur vous en dit.

Si vous avez des questions, n’hésitez pas à venir me secouer sur l’IRC Mozilla où je traine souvent.
