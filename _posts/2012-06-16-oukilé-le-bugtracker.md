---
  layout: post
  title: "Saisis un ticket ! Oussa ???"
  published: true
  date: 2012-06-19 22:41:00
  tags:
  - SemWeb
  - DOAP
  - RDFa
  - microdata
---

Comment signaler un souci technique sur un site Web ? C'est la question que se posent quotidiennement les camarades Karl et "File a bug" Rik. Et dont la réponse pourrait être une « bonne pratique ». La solution la plus simple est bien sûr de ne pas oublier, sur la page de contact du site, les adresses du service technique s'en occupant. Une alternative un peu plus /geek/ serait d'utiliser le fichier [humans.txt](http://humanstxt.org/), qui permet de lister les humains impliqués dans la réalisation du site. Mais ces deux options ne permettent pas d'automatiser la recherche du bon contact, c'est à dire d'avoir par exemple dans son navigateur une extension qui affiche un bouton « Signaler un problème sur ce site ».

La solution est alors peut-être à chercher du côté du Web sémantique. Ajouter au code source de chaque page des informations sémantiques pointant vers un système de gestion de tickets. Le vocabulaire [DOAP — Description Of A Project](https://github.com/edumbill/doap/wiki) semble indiqué pour cette tâche, puisqu'il propose une propriété `bug-database`. Il suffit donc d'ajouter cette information à la page.

Voici trois propositions d'implémentations, utilisant sauf erreur de ma part RDFa, RDFa Lite et les micro-données HTML5. Je précise que j'ai beaucoup de mal avec ces spécifications, donc ne garantis pas la justesse de mes exemples. [Différents outils](http://rdfa.info/tools/) semblent cependant les trouver valides et réussir à en extraire les données.

* en [RDFa](http://www.w3.org/TR/rdfa-syntax/), via les méta-données de la page

      <html lang="fr" >
        <head prefix="doap: http://usefulinc.com/ns/doap#">
          <title>{{ page.title }}</title>
          <meta charset="utf-8" />
          <meta name="description" content="Esquisses, brouillons et notes en vrac d'un apprenti geek intéressé par la liberté" />
          <meta name="author" content="Clochix" />
          <meta property="doap:bug-database" content="https://github.com/clochix/esquisses/issues">

* en [RDFa Lite](http://www.w3.org/TR/2012/REC-rdfa-lite-20120607/)

      <div vocab="http://usefulinc.com/ns/doap#" typeof="Project">
        <a property="bug-database" href="https://github.com/clochix/esquisses/issues">Signaler un problème</a>
      </div>

* avec les [micro-données HTML5](http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html)

      <div itemscope itemtype="http://usefulinc.com/ns/doap#Project">
        <a itemprop="bug-database" href="https://github.com/clochix/esquisses/issues">Signaler un problème</a>
      </div>

Une fois les informations ajoutées à la page, reste à pouvoir les utiliser, par exemple depuis une extension. Et de ce point de vue, bien que préférant RDFa, je dois admettre que les micro-données viennent de prendre un petit avantage avec l'[arrivée dans Firefox](https://bugzilla.mozilla.org/show_bug.cgi?id=591467) de l'[API DOM pour y accéder](http://www.whatwg.org/specs/web-apps/current-work/multipage/microdata.html#microdata-dom-api). Ce petit bout de code devrait être capable d'extraire les données. Je vous laisse l'embarquer dans une /marque-pagette/ ou une extension.

    var items = document.getItems("http://usefulinc.com/ns/doap#Project");
    if (items.length > 0) {
      Array.prototype.forEach.call(items, function (elmt) {
        if (elmt.properties['bug-database']) {
          console.log(elmt.properties['bug-database'].getValues().join(','));
        }
      })
    }

Du côté de RDFa / RDFa Lite, la [spécification d'une API](http://www.w3.org/2010/02/rdfa/sources/rdfa-api/) native semble en sommeil et il faudra utiliser des bibliothèques tierces pour extraire les informations.
