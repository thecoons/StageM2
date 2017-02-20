# Representation Learning : A Review and New Perspectives

## 11. Building-In Invariance

  >  Pour progresser dans l'apprentissage machine, on a eu besoin d'incorporer des connaissances de domaines d'application à nos modèles pour les rendre plus performant.

  > On a utilisé les connaissances de domaine traité par l'apprentissage machine pour raffiner ( idée de réduction d'espace de représentation) les entrées sur le principe de biais inductifs génériques, pour vulgariser, la technique du rasoir d'Occam ...

  > On aborde une approche fondée sur la connaissance structurelle de l'entrée de données (une image ce représente en 2 dimension).

  ### 11.1 Generating Transformed Examples
  > Une approche a été d'augmenter la performance des modèles en leur fournissant un très grand nombre d'exemples. Pour ce faire, on a appliqué aux entrées de données une variation indépendante des paramètres à discriminer (ex: En OR la rotation n'impacte pas l'objet à reconnaître).
  Appliqué au corpus MINST, cette approche établit un record de performance avec une erreur de classification de 0,32%...

  > __Note__ : en relation avec la théorie probabiliste le fait d'augmenter le nombre d'exemples rend le calcule des intégrales plus fines. Au détriment d'un besoin de puissance de calcul bien plus élevée.

  ### 11.2 Convolution and Pooling

  >
