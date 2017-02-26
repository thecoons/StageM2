# Node2Vec Scalable Feature Learning for Networks

## Abstract

L'apprentissage dans les graphes néscessite un effort considérable en "engineering features". Des progrès ont été fait mais les approches ne sont pas assez expressives. On définit une notion de voisinage flexible via un système de marche pondéré. Ils établissent l'état de l'art pour la labélisation de noeud (clustering) et la prédiction de lien.

## 1. Introduction

On peut appliquer la classification de noeuds et la prédiction à de nombreux domaines d'application, si ce n'est pas tous.
Le problème des approches par expertise, pour exemple les approches spectrales, ont un coup d'utilisation élevé et souvent s'adaptent mal à des structures plus variées et complexes.

Une approche différente est de considérer l'apprentissage de la représentation des entrées de données comme un problème d'optimation. La difficulté est de trouver une __fonction objective__, un modèle, qui fait le meilleur compromis entre précision et complexité.
Deux approches, soit on cherche un modèle qui vise à trouver une représentation qui augmente les performances, ce qui entraîne une augmentation de la complexité des modèles en fonction de la complexité des structures à discriminer. Et une autre approche, où ont considére que le problème de représentation peut être estimé par un modèle non surpervisé, ce qui rend l'approche générique.

Or les techniques courantes d'apprentissages non supervisés ne fournissent pas de résultat satisfaisant. Les approches classiques, linéaires et non linéaires, optimisent une fonction objective qui maximise la variance de la représentation de la donnée. Ce qui implique une "eigendecomposition" de la matrice de données, laquelle peut se révéler expansive avec la taille des graphes. De plus ces approches ont de pauvres performances sur les problèmes de représentation dans les graphes.

Autrement, on peut créer une fonction objective qui préserve le voisinage local des noeuds. Cette objectif peut être efficacement obtenu par une décente de gradient, par "backpropagation", branché sur un "feadforward neural networks". Les récents travaux sur le sujet ont apporté des résultats intéressants en proposant des algorithmes performants mais fondé sur une représentation du voisinage très rigide.

Spécialement dans les réseaux, les noeuds peuvent être organisé de deux façons. En communauté que l'on peut classifier et en rôle structurel dans le graphe. 
