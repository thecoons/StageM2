# Premier Jet

Après avoir lu [SGT 1.], on comprend qu'une approche par la théorie spectral graphes s'avère compliqué du fait de la difficulté à passer à l'echelle.En effet la complexité des graphes analysés est un facteur déterminant dans la complexité des modèles engendrés. Or l'entrée de données peut très vite atteindre une taille conséquente une fois passée à l'échelle.

Et une approche par architecture de convolution semble compromis pour plusieurs raisons
  1. La complexitée du modèle qui passe difficilement à l'échelle sur de très grands jeux de données, ce qui est un atout majeur de notre sujet d'étude [ML 1.11.1].
  2. La phase de pooling est nécessaire pour plusieurs raisons, stabiliser la complexité des modèles à couches superposées et mettre en évidence un invariant dans les facteurs discriminants du sujet d'études(cf [ML 1.11.2]), pour pallier ce problème, on peut imaginer une phase d'apprentissage sur la stratégie de pooling [ML 1.11.2 ref ...].
  3. Et la plus importante, à mon sens, est la perte d'informations engendrée par la méthode qui compromet la discrimination de structures plus complexes. Celle engendrée par une image ou un spectre sonore comporte suffisamment de dépendance entre leurs éléments, pour que la méthode soit bonne. Elle est trop approximative pour des analyses plus fines!!!!!

En lisant [ML 2.], on comprend que la compléxité d'un modèle peu être une problématique majeur pour passage à l'échelle sur des corpus de grand volume. La méthode adaptée par Skip-Gram est de faire une représentation locale du voisinage afin de réduire l'espace de représentation de l'entrée de données(on réduit ainsi les colonnes de la matrice d'entrée, ce qui améliore la mise à l'échelle du modèle en réduisant sa comlplexité).

Pour Node2Vec, je pense qu'ils passent à côté de quelques choses, ils effectuent une marche aléatoire à partir de tous les noeuds. Mais je pense que l'on peut réduire la compléxité du modèles non pas en réduisant la dimensionalité par la taille des marches, mais par un échantillonnage des noeuds sources. Ce qui augmente l'expréssivité des vecteurs pour ainsi représenter, hypothétiquement, plus d'informations dans une matrice plus dense.

Une telle approche est parfaitement adapté à de la clusterisation de noeud et la prédiction de lien dans une structure en treillis, de part ça nature à explorer le graph en profondeur!!!.

Il faut comprendre qu'attaquer le problème de propriété sur les graphes ne peut, ce faire en considérant la globalité des noeuds. Il est plus pertinent d'estimer leurs interactions.
