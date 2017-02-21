# Etude des layers de convolution et pooling

## Representation Learning : A Review and New Perspectives

### 11. Building-In Invariance

  >  Pour progresser dans l'apprentissage machine, on a eu besoin d'incorporer des connaissances de domaines d'application à nos modèles pour les rendre plus performant.

  > On a utilisé les connaissances de domaine traité par l'apprentissage machine pour raffiner ( idée de réduction d'espace de représentation) les entrées sur le principe de biais inductifs génériques, pour vulgariser, la technique du rasoir d'Occam ...

  > On aborde une approche fondée sur la connaissance structurelle de l'entrée de données (une image ce représente en 2 dimension).

  #### 11.1 Generating Transformed Examples
  > Une approche a été d'augmenter la performance des modèles en leur fournissant un très grand nombre d'exemples. Pour ce faire, on a appliqué aux entrées de données une variation indépendante des paramètres à discriminer (ex: En OR la rotation n'impacte pas l'objet à reconnaître).
  Appliqué au corpus MINST, cette approche établit un record de performance avec une erreur de classification de 0,32%...

  > __Note__ : en relation avec la théorie probabiliste le fait d'augmenter le nombre d'exemples rend le calcule des intégrales plus fines. Au détriment d'un besoin de puissance de calcul bien plus élevée.

  #### 11.2 Convolution and Pooling

  > Cette approche est fondée sur l'étude de la topologie de l'espace de représentation des entrées de données. Le but est de créer des facteurs discriminants de faible dimension via à un voisinage local de l'entrée de données. Il est important pour la performance de l'approche d'avoir une "forte" dépendence (le voisinage d'un pixel est fortement dépendent de celui-ci dans la majoritée du temps). En ce fondant sur cette dépendance, il est possible de "découvrir" la topologie de l'espace de représentation.
  Cette approche permet une généralisation des concepts extraient, leur localisation spatiale ou leur orientation n'influe pas sur les résultats. On extrait ainsi les concepts invariants et discriminants liés à notre problématique.

  > Une autre caractéristique des architectures de convolutions est la phase de __pooling__. La pratique la plus simple consiste à faire la somme ou à prendre le maximum des valeurs d'un tampon de pooling. Le pooling apporte une amélioration des résultats en créent une invariance du modèle aux translations des entrées de donées. Cette architecture est la base des réseaux de convolution et inspiré de l'architecture du cerveau des mamifère pour la reconnaissance d'objet.

  > Le pooling a permis une amélioration des performances dans les tâches de reconnaissance d'objet. Mais il existe d'autres méthodes de pooling plus fine telles que la "L2 pooling", ou des approches d'apprentissage pour définir quelle caractéristique devrait être "poolé" ensemble pour une représentation plus pertinente.
