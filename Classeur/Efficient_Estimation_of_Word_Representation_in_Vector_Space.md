# Efficient Estimation of Word Representations in Vector Space

## 1. Introduction

> De nombreuses approches de TALN traître les mots d'un corpus de façon atomique sans considérer de similarité entre eux, et cela pour de nombreuses raisons pratiques.
On constate avec de telles approches une corrélation des performances avec la taille des corpus en entrées pour des problèmatiques de "speech recognition".
Les progrés en apprentissage machine ces dernières années on permit de l'entrainement de modèles complexes sur de large jeu de données dans des temps raisonables (une journée pour le modéle étudié).

### 1.1 Goals of the Paper

> On cherche à définir une représentation des mots du corpus qui dépasse la simple similarité syntaxique. On veut obtenir une représentation vectorielle qui préserve les régularités linéaires entre les mots, afin de pouvoir leur appliquer des opérations algébriques.
On discutera par la suite de la dépendance pour le temps d'apprentissage et sa précision en fonction de la dimensionalité du vecteur de mot et du nombre de données d'entraînement.

### 1.2 Previous Work

> On a déjà appliqué les vecteurs de mots à des modèles d'apprentissages statistiques. Des progrès ont été faits quand on a laissé le soin à un modèle d'apprentissage (NN) de définir la structure du vecteur de mots, pour ensuite le fournir à un modèle (NNLM). Les travaux du papier se fondent sur la partie de représentation du vecteur de mots.

## 2. Model Architectures

> On souhaite estimer une représentation continue des mots. Il est important pour la comparaison des performances entre modèles de définir leur complexité.

<div style="text-align:center">
<img  src="http://latex.codecogs.com/gif.latex?O&space;=&space;E&space;\times&space;T&space;\times&space;Q">
</div>
