# Deep Learning and Graph Patterns
## Plan
  1. Machine Learning and Deep Learning
  2. Representation Learning
  3. Learning Techniques Apply to Graph Structures

## Articles

### Spectral Graph Theory

1. **Introduction to Spectral Graph Theory**

  > On y découvre les propriétès de la théorie spectral des graphs, ou la connection entre algèbre et graph.

  > On définit la Laplacian d'un graph de manière "constructive". Il ne s'agit que d'une représentation des voisinages de chaque noeud cumulé.

### Machine Learning for Graph

1. **Node2Vec: Scalable Feature Learning For Networks**

  > Algorithme de "Representation Learning" pour clusteriser des noeuds de graph ou faire de la prédiction sur les arrêtes. Ils utilisent une marche paramétrique pour définir une représentation du voisinage d'un noeud de manière "souple" (laplacian trop groumande).

  > Si on recentre avec (MachineLearning 2.), Node2Vec cherche à définir une strategie optimal de parcourt de voisinage de noeuds pour représenter les données afin de pouvoir appliquer des algos de learning.

2. **Laplacian Eigenmaps and Spectral Techniques for Embedding and Clustering**

  > Si je **comprends bien**, l'utilisation de la Laplacian sert à examiner des objets dimensionellement faible dans un espace à grande dimension. En effectuant cette réduction de dimension on peu mettre en évidence des corélation "simple" entre les données.On peu croire que si il n'existe pas de fonction linéaire capable de séparer une **certaine** transformation de l'espace de représentation l'algo est caduc...  Mais putain on y comprends rien, j'ai besoin de plus de technique...

### Machine Learning

1. **Representation Learning: A Review and New Perspectives**

  > On voit que les avancés des dernières années dans le machine learning à été d'effectuer des traitements de représentation sur les données à explorer, que ça soit dans le TALN, OR ou le le Go, c'est un traitement sur l'espace de représentation de la données qui est en cause.

  > La convolution convient aux espaces de grandes dimensions en réduisant les paramètres à des motifs locaux.

  > Le problème, d'appliquer une sucession de convolution et pooling aux graphs, ne serait pas la convolution mais la strategie de pooling utilisée qui engendre une trop grande approximation.




2. **Efficient Estimation of Word Representations in Vector Space**

  > On peut en tirer que la réduire la complexité d'un modèle pour la représentation des entrées de données peut significativement améliorer les résultats.

  > Todo ( mieux comprendre l'apport de leurs nouveaux modèles tout beau tout neuf ... )

## Mémo

1. [TensorFlowOnSpark](https://github.com/yahoo/TensorFlowOnSpark)

  > TensorFlow distribué par Spark, ça sonne bien à voir.

## Note

  _14/02/2017_

  D'après [SGP 1.,MLG (1.,2.)] on voit que le problème de la classification ou de la prédiction dans les graphs ne dépend que de la façon dont on choisie de représenter le voisinage des noeuds, quelle transformation à appliquer. Il est important d'approfondir les tâche de "Representation Learning".

  Au lieu de chercher des méthodes dur comme la diagonalisation de matrice, ou des transformer de Laplace, Fourier ou autre. On peu générer des méthodes d'apprentissage pour déterminer cette transformation.

  _15/02/2017_

  On voit dans [ML 1.] la corélation avec toutes les avancées dans l'IA ces dernière années, la représentation des données. On peu penser qu'il existe au moins une représentation optimal de la données pour un problème de classification ou de prédiction donné dans un espace de représentation donnée. On constate un isomorphisme des modèles utilisé dans le domaine du learning comme le montre [MLG 1.] en utilisant les travaux de TALN de [ML 2.] pour des problèmes de lié aux patterns dans les graphs.

  _16/02/2017_

  Après la réunions deux points à éclaircir sont resortient.

  Est-ce que le modèle à convolution/pooling essaye de préserver l'espace vectoriel de l'input, et est-il pértinent sur des éléments à faible dimensionalité plongé dans des "grands" espaces vecoriels.

  > Je me dis que le problème est extrement similaire aux problèmes de TALN
    1) Les rapport des espaces généré et la dimensionalitée des elements y sont identiques, la cardinalitée des mots d'un corpuce vont former les dimensions de l'espace de représentation quand pour un graph se sera ses noeuds qui le forment.
    2) Les interaction "local" des elements est plongé dans un espace bien plus grand que sa dimensionalité.
    Ils faut penser au problèmes des "hubs"(des singularité à grand degrée) est-ce possible en TALN ou somme nous dans un modèle plus général ou faut il contraindre les degrée du graph ???? (quote: l'interaction des mots d'un corpus peux ce représenter par un graph à "faible" degrée)

  Il faut chercher à comprendre les méchanismes de la convolution et ses répercutions sur la variation des données représentent des graphs.

  > Plusieurs observations, si la dépendances des "features" n'est pas assez importante dans nos graphes cela rend plus compliquée l'exploration de la topologie de l'espace de représentation par les architectures à convolution. De plus les stratégies statiques de "pooling" semble être non adaptées à l'aspect générique de notre problématique. Il faut explorer les approches par apprentissages des stratégies de pooling.  

  Comprendre les enjeux de la reduction de l'espace de représentation des données.

  > C'est assez simple si l'on réduit l'espace de représentation par des "features" de faibles dimensions qui sont très discriminantes pour notre problématique, alors la performance de nos modèles est fortement augmentée

  Definir l'état de l'art sur les techniques d'apprentissages appliqués aux graphs.

  > Question compliquée, si on considére que tout problème de classification ou de prédiction peut être représenter dans un graphe.
  (Images, series temporelles, texte, ... tout peut être représenté dans un graphe...)

  _21/02/2017_

  Il faut établir les différentes approches pour les phases de "pooling" d'une architectures à convolution.

  Il faut s'intéresser aux méthodes d'apprentissages appliqués aux structures moléculaires (chémoinformatique !).

  _22/02/2017_

  Etant dans un domaine formel (théorie des graphes) il serait facile de générer un très grands nombres d'exemples représentatives d'une problématique pour améliorer la pérformance de nos modèles [ML 1.11.1].

  > En tirant parti de [ML 2.],il pourait être pertinant de définir un modèle à compléxité réduite pour pouvoir l'appliquer à de très grands jeux de données. On peut penser que l'on peut combler la complexité structurelle de problématiques liées aux graphes par une telle approche. On se rapproche ainsi des méthodes appliquées en TALN, pour s'accommoder à de grands espaces de représentation.

  
