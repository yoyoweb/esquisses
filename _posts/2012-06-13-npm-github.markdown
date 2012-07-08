---
  layout: post
  title: Add Github infos to npm results
  published: true
  date: 2012-06-13 23:48:00
---

(Version française en dessous)

Too much choices is the same as no choice at all. This is what I say to myself every time I'm looking for a library in Node Packages Registry. Every search with npm return tens of results, most of then being dead or sleeping projects. But for each one I get the URL, and have a look on Github to see if the project is alive and seems a little popular. Waste of time.

Fortunately, both npm and Github have easy to use API. So I just hacked a little mashup that performs a search with npm, eliminates packages not hosted on Github (sorry guys), and then queries Github to display some metrics (number of followers and forks, date of last update…). I can know select only two or three packages that the crowd seems to promote, and have a deeper look at them. I know this is not fair nor objective, but I had to find a way to quickly choose a library, so… 

Enough words, if you're interested just [have a look at the code][code]. Comments welcome :)

## Ajouter des informations de Github aux résultats de recherche npm

Trop de choix tue le choix, c'est la réflexion que je me fais à chaque fois que je cherche une bibliothèque à utiliser dans un projet Node. Chaque recherche avec npm ramène des dizaines de résultats, mais la plupart sont des projets morts ou en hibernation profonde. Pour juger si le projet est encore vivant et jouit d'une certaine popularité, il faut aller faire un tour sur la page de chacun sur Github. Fastidieux.

Heureusement, tant npm que Github proposent des APIs. Bidouiller un script mariant les deux est très simple. Ce script recherche dans le registre de npm puis, pour chaque résultat dont le code est hébergé sur Github (oui, c'est un critère très subjectif), interroge Github pour afficher quelques informations comme le nombre de gens qui suivent le projet et l'ont dérivé ou la date de dernière mise à jour. Ça me permet de sélectionner deux ou trois projets adoubés par les foules, que je vais ensuite regarder de plus près. La méthode n'est certes ni très objective, ni très juste, mais il me fallait trouver quelques critères pour pratiquer un rapide écrémage.

Trêve de bavardages, si ça vous intéresse allez jeter un œil [au code][code]. Commentaires bienvenus :)

[code]: https://github.com/clochix/Config/blob/master/bin/snpg
