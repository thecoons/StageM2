# Graph Minor Theory

## Abstract

  Dans l'année 2004, la théorie des graphes a vu s'achever une révolution interne. Les travaux de Robertson et Seymour, rejoint plus tard par Thomas, fondent de nouveaux conceptes et une nouvelle vision de la théorie. Motivé par le théorème de Kuratowski, sur la planaritée d'un graphe, la conjecture de Wagner generalise le ce théorème de la façon suivante : Si une famille de graphes est "minor-closed", alors cette famille ce caractérise par un ensemble fini et unique de mineurs.


## Introduction

  Le théorème de Kuratowski,
    > A graph G is embeddable in the plane if and only if it does not contain
    a subgraph homeomorphic to the complete graph K 5 or the complete bipartite graph
    K 3,3 .

  Ainsi, la question fut de savoir si cette propriété été généralisable à toutes les topologies. Autrement dit, peut-on définir qu'un graphe est plongable dans une surface donnée en excluant une liste finie de sousgraphes homeomorphique à celui-ci ?
  La preuve pour les graphes non-orientés fut apporté par Archdeacon et Huneke, et pour le cas général par Robertson et Seymour.

  Klaus Wagner, en 1970, formulera la conjecture fodamentale qui géneralisera ce concepte en une famille de graphes dit fermé par les mineurs, "minor-closed graph". Cette conjecture fut demontré dans une serie de papier publié par Robertson et Seymour, une démonstration de 500 pages publié de 1983 à 2004 dans la revue "Journal of Combinational Theory".

## Minors and Embeddings

  On défini nos graphes comme ne comportent pas de relation réflexive ou prallèle. Avec de telle graphes G, on définie trois moyen de le réduire en un graphe G':
    1. en supprimant une arrête du graphe
    2. en contractant une arrête
    3. en supprimant un noeud isolé

  Tout les graphes G' ainsi produit, et cas particulier G lui même, sont appelés des mineurs de G.

  On peut dresser une, petite, liste des propriétés de graphes fermé par mineurs. La propriété d'un graphe à ne pas contenir de cycles, "cycle-free", en fait partie. Ainsi que "series-parallel" et "series extentions". De nombreuses propriétés topologiques de graphes sont fermé par mineurs, comme la capacité d'un graph d'être plongé dans une surface donnée, la planarité d'un graphe en est un sous cas.

## Wagner's Conjecture

### Excluded minor characterizations

  De nombreux théorémes charactérisent des proprétés fermé par les mineurs via une approche de mineurs excluent, "excluded minors".
  Commencons par un exemple simple, un graphe est une forêt, si et seulment si, il ne contient pas K_3 comme mineur.
  Dirac à prouvé qu'un graphe est "series-parallel" si il ne contient pas K_4 en mineur.
  La conjecture de Sash, prouvé par Robertson, Seymour et Thomas. Un graph est "linklessly embeddable", si et seulment si, il ne contient aucun graphe de la famille de Petersen.

### Statements of the theorem

  On dit qu'une classe F d'une famille de graphes est fermé par mineur si pour tout graphes G appartenant à F, tout les mineurs de G sont aussi des mineurs des graphes de F. Etant donné une famille de graphes Gf = { G1, G2, ...}, on considère la classe F des graphes qui ne contient aucun graphe de Gf comme mineur. Trivialement cette classe est par définition fermé par mineurs, qui sont les éléments de l'ensemble Gf. On dit que l'ensemble Gf caractérise la classe F par exlusion de mineurs. Il aussi facile de montrer que tout classe F fermé par mineurs peut être charactérisé par exclusion de mineurs. La conjecture de Wagner, par la suite le théoreme de Robertson-Seymour, montre que l'ensemble Gf est toujours fini.

  Toutes classe de graphes fermé par mineur peut être charactérisé par une liste fini de mineurs exclut.

  
