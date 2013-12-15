---
  layout: post
  title: Choisir son exposition
  published: true
  date: 2013-10-18 13:27:12
  tags:
  - Mozilla
  - Privacy
---

<section vocab="http://schema.org/" about="https://support.mozilla.org/fr/kb/navigation-privee-naviguer-sans-conserver-infos-sites" typeof="Article" class="cite">
<blockquote property="articleBody" cite="https://support.mozilla.org/fr/kb/navigation-privee-naviguer-sans-conserver-infos-sites">
<div>
Avertissement : La navigation privée n’a pas pour effet de vous rendre anonyme sur Internet. Votre fournisseur d’accès Internet, votre employeur ou les sites eux-mêmes peuvent toujours pister les pages que vous visitez.
</div>
</blockquote>
</section>

Cet avertissement sur la page de [présentation du mode de navigation privée](https://support.mozilla.org/fr/kb/navigation-privee-naviguer-sans-conserver-infos-sites) de Firefox illustre combien ce concept de « [navigation privée](http://fr.wikipedia.org/wiki/Navigation_priv%C3%A9e) » est ambigu, et l’implémentation choisie par les navigateurs probablement en décalage avec les attentes des utilisateurs.

Lorsque je ne suis pas devant mon clavier, il m’arrive d’avoir des activités publiques. Faire une présentation de Webmakers, distribuer des tracts… Je le fais à visage (relativement) découvert et en assume (vaguement) la publicité. D’autres activités se déroulent dans un cadre fermé dont elles n’ont pas vocation à sortir. Ce sont par exemple mes interactions professionnelles, ou des discussions au bistro (lieu public mais conversations privées qui n’ont pas vocation à être diffusées. Et bien sûr, j’ai avec mes chats des relations intimes, relevant uniquement de ma vie privée (ceci dit, je ne limite pas la sphère privée au périmètre de ma grotte, mais y inclus des activités dans un espace public, comme faire mes courses). Ce sont trois sphères distinctes entre lesquelles nous oscillons en permanence, et qui sont plus ou moins garanties par des conventions sociales et des contrats. On essaie de ne pas écouter les conversations des tables voisines ou les bruits quotidiens de nos voisins. De ne pas rendre publiques des informations relevant de notre activité professionnelle.

En ligne aussi, mon activité oscille entre ces trois sphères. Publique lorsque je m’exprime sur Twitter ou ici. À diffusion restreinte lorsque j’écris à mon cercle d’amis. Et strictement privée lorsque je traine sur YouPron^W VoilàPipole^W ploumploumtralalanarchyvaincra.org. Certains réseaux sociaux en ligne ont d’ailleurs adopté cette distinction, qui permettent pour chacune de nos informations de choisir si nous la partageons avec tous les robots des Internets, juste nos connaissances, ou si on préfèrerait qu’elle reste confidentielle (c’est à dire, dans le cas de Facebook, connue uniquement de leurs employés et partenaires commerciaux, une paille).

En fait, cette distinction me semble si naturelle que je rêve qu’elle soit implémentée au cœur des agents que nous utilisons pour interagir en ligne (c’est à dire de Mozilla/Firefox). Que mon navigateur me permette systématiquement de choisir, pour chaque nouvel onglet, si je souhaite que mon activité en son sein soit publique, privée, ou protégée. Publique, j’autoriserais tous les sites qui le souhaitent à me tracer. Privée, elle ne laisserait aucune trace sur mon ordinateur et me protègerait raisonnablement contre le traçage (connexion via un proxy, blocage de [tous les espions](http://en.wikipedia.org/wiki/Evercookie), [brouillage de l’empreinte digitale du navigateur](https://bugzilla.mozilla.org/show_bug.cgi?id=928311)…). Protégée, j’autoriserais les sites à analyser mon comportement pour me faire des propositions pertinentes, mais pas à partager mon profil avec des tiers (cf le prochain [blocage des cookies tiers](http://blog.mozilla.org/privacy/2013/02/25/firefox-getting-smarter-about-third-party-cookies/) dans Firefox.

Je jette en vitesse ici cette idée qui me trotte dans la tête depuis quelques jours, n’hésitez pas à me lancer un pavé ICMP si vous avez des remarques.

