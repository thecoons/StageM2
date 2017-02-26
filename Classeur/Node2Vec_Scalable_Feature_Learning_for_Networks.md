# Node2Vec Scalable Feature Learning for Networks

## Abstract

L'apprentissage dans les graphes néscessite un effort considérable en "engineering features". Des progrès ont été fait mais les approches ne sont pas assez expressives. On définit une notion de voisinage flexible via un système de marche pondéré. Ils établissent l'état de l'art pour la labélisation de noeud (clustering) et la prédiction de lien.

## 1. Introduction

On peut appliquer la classification de noeuds et la prédiction à de nombreux domaines d'application, si ce n'est pas tous.
Le problème des approches par expertise, pour exemple les approches spectrales, ont un coup d'utilisation élevé et souvent s'adaptent mal à des structures plus variées et complexes.
Une approche différente est de considérer l'apprentissage de la représentation des entrées de données comme un problème d'optimation. La difficulté est de trouver une __fonction objective__, un modèle, qui fait le meilleur compromis entre précision et complexité.

 On oberves que les voisinage peuvent ce définir par une communauté (un cluster) et un rôle structurel (ex: hub).
