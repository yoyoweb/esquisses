---
  layout: post
  title: "VimTip : complétion JavaScript"
  published: true
  date: 2013-01-02 22:33:00
  tags:
  - Vim
---


Lorsque je code en JavaScript avec `node.js` ou le couple [PhantomJs](http://phantomjs.org/) / [CasperJS](http://casperjs.org), l'auto-complétion native de Vim pour JS me laisse un peu sur ma faim. Plusieurs moyens de l'améliorer sont évidemment possibles :

 - utiliser [doctorjs / jsctags](https://github.com/mozilla/doctorjs) pour créer des fichiers de mots clés (`tags`). Malheureusement, mes essais avec `jsctags` ont rarement été concluants. Je n'arrive par exemple pas à extraire les mots-clés de CasperJS ;

 - utiliser des extensions spécifiques comme :
   - [jscomplete-vim](https://github.com/teramako/jscomplete-vim) qui prétend ajouter un meilleur support de la syntaxe native du langage ;
   - [vim-node-jscomplete](https://github.com/myhere/vim-nodejs-complete) qui permet entre autre la complétion sur les modules de l'API native de Node (l'API est générée dynamiquement à partir de la documentation en ligne).

Aucune de ces méthodes ne me satisfaisant vraiment, j'ai décidé d'en tester une autre, via la complétion de mots-clés. Vim dispose en effet de plusieurs types de complétion. La plus « intelligente » est théoriquement l'*Omni Completion*, activée par `Ctrl-X Ctrl-O`. Elle est spécifique à chaque type de fichier et utilise des fonctions censées interpréter le langage. D'autres complétions utilisent des listes de mots clés, extraits d'un fichier spécifique (`Ctrl-X Ctrl-]` pour le fichier `tags`, `Ctrl-X Ctrl-K` pour un dictionnaire, `Ctrl-X Ctrl-T` pour un thesaurus, ne me demandez pas la différence entre ces derniers), ou du fichier courant (`Ctrl-X Ctrl-N`), voire de celui-ci et des fichiers qu'il inclut -`Ctrl-X Ctrl-I`). C'est sur cette dernière que je me suis penché.

Pour déterminer la liste les fichiers inclus à analyser, Vim utilise plusieurs variables définies dans la configuration :

 - `include` : une expression régulière pour extraire d'un fichier les noms des fichiers inclus. La valeur par défaut est adaptée au `C` et au `C++`, pour les `require` des modules CommonJs j'utilise  `set include=require(.\\zs[^'\"]*\\ze` (dans une expression rationnelles Vim, `\zs` et `\ze` permettent de délimiter à l'intérieur du motif la portion à retourner) ;
 - `includeexpr` : une fonction qui permet de transformer le résultat de l'expression régulière précédente en nom de fichier. Par exemple, en `Java`, pour transformer les `.` dans les noms de classes en `/`. Souvent avec Node.js, on utilise `require('toto')`, `toto` étant le nom du dossier contenant le module. À l'intérieur de ce dossier, un fichier `index.js` inclut les fichiers nécessaires, alors que n'existe nul `toto.js`. `includeexpr` permet de gérer ces cas en essayant d'ajouter `/index.js` au chemin du fichier requis ;
 - `suffixesadd` : une liste de suffixes à ajouter aux noms précédents si les fichiers n'existent pas. Dans notre cas : `set suffixesadd=.js` ;
 - `path` est une liste de dossiers où Vim cherchera les fichiers. La chaîne vide correspond au dossier courant, `.` à celui contenant le fichier, et `**` permet de désigner des sous-arborescences complètes. Pour rechercher dans les dossiers `node_modules`, j'utilise donc `set path+=./node_modules/**,node_modules/**`.

Au final, voici les quelques lignes de mon `.vimrc` :


      function! JsIncludeExpr(file)
        if (filereadable(a:file)) 
          return a:file
        else
          let l:file2=substitute(substitute(a:file,'\\.js$','','g'),'$','/index.js','g')
          return l:file2
        endif
      endfunction
      function s:setJSOptions()
        set omnifunc=javascriptcomplete#CompleteJS
        set path+=./node_modules/**,node_modules/**
        set include=require(.\\zs[^'\"]*\\ze
        set includeexpr=JsIncludeExpr(v:fname)
        set suffixesadd=.js
      endfunction
      autocmd FileType javascript call s:setJSOptions()

Ce code nécessite encore des améliorations, mais en l'état il commence à être utilisable. Pour le mettre au point, il est utile de connaître la commande `checkpath!` qui affiche l'ensemble des fichiers à inclure détectés par Vim (`checkpath` sans point d'exclamation n'affiche que les fichiers non trouvés).
