---
  layout: post
  title: Standardiser Markdown, c’est urgent
  published: true
  date: 2013-04-29 21:40:00
---

J’ai gazouillé plus tôt dans la journée que « Un des trucs dont l’Humanité a le plus besoin, c’est d’une normalisation d’un Markdown étendu, prenant en compte les annotations ». Cette forte pensée a suscité quelques réactions et comme 140 caractères sont un peu courts pour répondre, je vais développer ici. Markdown est mon langage de balisage favori, sans doute puisque, comme il s’inspire de conventions ancestrales pour la rédaction de mails, je le trouve assez intuitif.

Malheureusement, il lui manque quelques fonctionnalités pour couvrir l’essentiel de mes besoins, et en particulier une syntaxe pour des annotations ou des notes de pied de page dont je suis très friand. Et John Gruber ne semble pas décidé à faire évoluer la spécification originale qu’il a élaborée avec Aaron Swartz. De ce fait, de nombreuses propositions d’extension ont fleuri, comme par exemple [MultiMarkdown](http://fletcherpenney.net/multimarkdown/) et [PHP Markdown Extra](http://michelf.ca/projects/php-markdown/extra/). Chacune de ces propositions a une implémentation de référence, et plusieurs outils proposent leur propres variantes, comme [Maruku](http://maruku.rubyforge.org/), [Kramdown](http://kramdown.rubyforge.org/syntax.html) et bien entendu le couteau suisse [Pandoc](http://johnmacfarlane.net/pandoc/README.html#pandocs-markdown), l’outil quasi universel de conversion entre langages de balisages. Sans oublier bien sûr Github qui a également ses [propres variations](https://help.github.com/articles/github-flavored-markdown).

Les fonctionnalités proposées par les propositions d’extensions et les divers outils sont globalement les mêmes : notes de bas de page, tableaux, etc. Et les syntaxes similaires, mais avec d’infimes variations qui les rendent incompatibles entre elles. De fait, à moins de se limiter à la syntaxe de base, les documents écrits en Markdown ne sont pas interopérables. J’écris en ce moment cette note en Markdown et Maruku va la transformer en HTML. Mais rien ne me garantit que si demain je choisis un autre convertisseur, je ne vais pas perdre certaines informations, comme les notes de bas de page. C’est pourquoi il est urgent de se mettre d’accord sur une norme pour un Markdown v2 étendu. On pourra ainsi évaluer les différents outils existant à l’aune de leur respect de cette norme.

Le besoin d’une telle norme n’est pas récent, et en Octobre 2012 [un groupe communautaire](http://www.w3.org/community/markdown/) s’est créé au sein du W3C. Malheureusement, si j’en crois la liste de discussion publique, après une activité intense dans les premières semaines de son lancement, le groupe semble aujourd’hui en profonde hibernation (aucun message sur la liste publique depuis plusieurs mois). Sa principale production est un début de [suite de tests](https://github.com/karlcow/markdown-testsuite), rédigés pas Karl. Vu l’engouement continu autour de Markdown depuis des années, je ne m’explique guère ce manque d’empressement à le standardiser. Et ne peut qu’espérer une prochaine standardisation d’une syntaxe pour les notes de pied de page, histoire de garantir l’interopérabilité de mes textes qui en font usage.



