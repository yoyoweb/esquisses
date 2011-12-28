---
  layout: post
  title: Sémantique
  published: true
  date: 2011-12-28 09:45:00
---


Actuellement, je rédige les notes sur ce cahier en utilisant la syntaxe [Markdown][Markdown]. Je suis adepte depuis longtemps de ce type de syntaxes de marquage légère, qui permettent d'ajouter un minimum d'informations sémantiques sans gêner ni la frappe ni la relecture. J'ai choisi Markdown car c'est l'un des formats des plus populaires, pour lequel existent des outils dans la plupart des langages de programmation. Il n'est cependant pas exempt de défauts. En particuliers, sa simplicité se paie par certaines limitations, comme l'absence de gestion de notes de bas de page. Pour y pallier, [différentes extensions][extensions] ont vu le jour. Malheureusement, aucune structure ne gère le format Markdown, aucune extension n'est donc *officielle* et leur implémentation par les bibliothèques varie. Dès lors que l'on sort des balises de base de Markdown, on n'est donc plus sûr que nos marqueurs seront correctement reconnus et traduits, on perd en interopérabilité.

Outre les notes de bas de page, ce qui me manque le plus en Markdown est la possibilité d'ajouter davantage d'informations sémantiques, en utilisant des micro-formats, des micro-datas ou, plutôt, du RDFa (ou sa variante allégée RDFa-Lite).

Pour aller dans ce sens, je vois deux pistes:
* proposer une nouvelle extension à Markdown. Une [proposition][semmark] a été faite pour enrichir le Markdown utilisé par Diaspora, mais elle semble être la fait d'un seul individu et n'avoir pas eu d'écho;
* utiliser la possibilité offerte par le format de mélanger ses balises avec du POH. L'[extension Extra][extra] offre une grande liberté en la matière.

La seconde option est moins élégante, obligeant à alourdir le texte de balises HTML. Mais elle me semble nettement plus pérenne. La première implique en effet de trouver un cadre de définition d'une nouvelle spécification, puis d'espérer que les bibliothèques existantes implémentent cette extension, et le face de manière consistante. Créer une extension sémantique à Markdown me semble donc un bonne idée, mais peu réaliste en pratique. De plus, l'objectif de Markdown est d'être simple. RDFa, même allégé, n'est pas simple. Je ne suis pas sûr qu'en «&nbsp;markdownisant&nbsp;» sa syntaxe, le gain en simplicité d'écriture et en légèreté soit suffisant pour justifie le développement et l'implémentation d'une nouvelle norme.

Mais ce n'est que l'état de ma réflexion ce matin, je ne demande pas mieux qu'à changer d'avis. Si vous voulez en discuter, [David][David] vient d'ouvrir un canal, `#mdlite` sur le serveur `freenode`.

[Markdown]: http://daringfireball.net/projects/markdown/
[extensions]: http://en.wikipedia.org/wiki/Markdown_extensions
[semmark]: https://github.com/diaspora/diaspora/wiki/Semantic-Markdown
[extra]: http://michelf.com/projects/php-markdown/extra/
[David]: https://larlet.fr
*[POH]: Plain Old HTML
