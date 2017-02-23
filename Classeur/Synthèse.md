# Premier Jet

Après avoir lu [SGT 1.], on comprend qu'une approche par la théorie spectral graphes s'avère compliqué du fait de la difficulté à passer à l'echelle.En effet la compléxité des graph analysé est un facteur déterminant dans la compléxité des modèles engendré. Or l'entrées de données peu très vite atteindre une taille conséquente une fois passé à l'échelle.

Et une approche par architecture de convolution semble compromis pour plusieurs raisons
  1. La compléxitée du modèle qui passe difficilement à l'échelle sur de très grands jeux de données, ce qui est un atout majeur de notre sujet d'étude [ML 1.11.1].
  2. La phase de pooling est nécessaire pour plusieurs raisons, stabiliser la compléxité des modèles à couches superposées et mettre en évidences un invariant dans les facteurs discriminants du sujet d'études(cf [ML 1.11.2]), pour palier ce problème on peu imaginer une phase d'apprentissage sur la stratégie de pooling [ML 1.11.2 ref ...].
  3. Et la plus importante, à mon sense, la perte d'information engendré par la méthode qui compromé la déscrimination de structure plus complexes. Que celle engendré par une image ou un spectre sonore où la méthode excelle. Elle est trop approximative!!!!!
