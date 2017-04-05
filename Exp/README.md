# Expérimentation

## Génération des bases d'apprentissages

### P-Tree

> Personal laptop : CPU => [i5 2,7 x4], RAM => [8Go], HDD => 1TB

| Méthode de construction | nb_nodes | features_size | P-Tree_rank | Time_exe (s) |
| :---------------------: | :------: | :-----------: | :---------: | :------: |
|learning_base_pTree_generation|10|100|[0, 1]|0.028366804122924805|
|pTree_basic_cycle_generation|10|100|[0, 1]|0.5885705947875977|
|pTree_basic_cycle_generation|20|100|[0, 1]|8.300281047821045|
|learning_base_pTree_generation|20|100|[0, 1]|0.04677748680114746|
|pTree_basic_cycle_generation|50|100|[0, 1]|187.5167624950409|
|pTree_basic_cycle_generation|50|500|[0, 1]|3860.4613552093506|
|pTree_basic_cycle_generation|50|1000|[0, 1]|7879.207705497742|
|pTree_basic_cycle_generation|100|100|[0, 1]|1863.496695280075|


> On Jaguar

| Méthode de construction | nb_nodes | features_size | P-Tree_rank | Time_exe(s) |
| :---------------------: | :------: | :-----------: | :---------: | :------: |
|pTree_basic_cycle_generation|20|100|[10, 50, 100]|1.4769604206085205|
|pTree_basic_cycle_generation|20|500|[10, 50, 100]|20.309359312057495|
|pTree_basic_cycle_generation|50|100|[10, 50, 100]|17.231047868728638|
|pTree_basic_cycle_generation|50|500|[10, 50, 100]|121.04586148262024|
|pTree_basic_cycle_generation|100|100|[10, 50, 100]|110.67583847045898|
|pTree_basic_cycle_generation|100|500|[10, 50, 100]|707.7474994659424|
|learning_base_pTree_generation|20|100|[10, 50, 100]|0.2901639938354492|
|learning_base_pTree_generation|20|500|[10, 50, 100]|0.9382717609405518|
|learning_base_pTree_generation|50|100|[10, 50, 100]|0.3848414421081543|
|learning_base_pTree_generation|50|500|[10, 50, 100]|1.7446095943450928|
|learning_base_pTree_generation|100|100|[10, 50, 100]|0.6758086681365967|
|learning_base_pTree_generation|100|500|[10, 50, 100]|3.1134626865386963|

## Descision Tree

> DescionTree

|Jeu de données|Representation|Miss_class (%)|Accuracy|Recall|F-Measure|
|:---------:|:---------:|:---------:|:---------:|:--------:|:--------:|
|pTree_basic_cycle_generation_20_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|73.33333333333333%|0.08888888888888889|0.3333333333333333|0.14035087719298248| 
|pTree_basic_cycle_generation_20_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|76.66666666666667%|0.07777777777777778|0.3333333333333333|0.12612612612612611|
|pTree_basic_cycle_generation_20_[10, 50, 100]_100|learning_base_to_A3_minus_D|80.0%|0.06666666666666667|0.3333333333333333|0.11111111111111112|
|pTree_basic_cycle_generation_100_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|73.33333333333333%|0.08888888888888889|0.3333333333333333|0.14035087719298248|
|pTree_basic_cycle_generation_100_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|76.66666666666667%|0.07777777777777778|0.3333333333333333|0.12612612612612611|
|pTree_basic_cycle_generation_100_[10, 50, 100]_100|learning_base_to_A3_minus_D|76.66666666666667%|0.07777777777777778|0.3333333333333333|0.12612612612612611|
|pTree_basic_cycle_generation_20_[0, 1]_500|learning_base_to_vec_adjacency_set|52.0%|0.24|0.5|0.32432432432432434|
|pTree_basic_cycle_generation_20_[0, 1]_500|learning_base_to_vec_laplacian_set|50.0%|0.25|0.5|0.3333333333333333|
|pTree_basic_cycle_generation_20_[0, 1]_500|learning_base_to_A3_minus_D|55.00000000000001%|0.225|0.5|0.3103448275862069|
|pTree_basic_cycle_generation_50_[0, 1]_500|learning_base_to_vec_adjacency_set|59.0%|0.205|0.5|0.2907801418439716|
|pTree_basic_cycle_generation_50_[0, 1]_500|learning_base_to_vec_laplacian_set|50.0%|0.25|0.5|0.3333333333333333|
|pTree_basic_cycle_generation_50_[0, 1]_500|learning_base_to_A3_minus_D|56.99999999999999%|0.215|0.5|0.30069930069930073|
|pTree_basic_cycle_generation_10_[0, 1]_10|learning_base_to_vec_adjacency_set|50.0%|0.25|0.5|0.3333333333333333|
|pTree_basic_cycle_generation_10_[0, 1]_10|learning_base_to_vec_laplacian_set|100.0%|0.0|0.0|0.0|
|pTree_basic_cycle_generation_10_[0, 1]_10|learning_base_to_A3_minus_D|100.0%|0.0|0.0|0.0|
|pTree_basic_cycle_generation_20_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|69.33333333333334%|0.10222222222222221|0.3333333333333333|0.15646258503401358|
|pTree_basic_cycle_generation_20_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|70.0%|0.09999999999999999|0.3333333333333333|0.15384615384615383|
|pTree_basic_cycle_generation_20_[10, 50, 100]_500|learning_base_to_A3_minus_D|68.0%|0.10666666666666667|0.3333333333333333|0.16161616161616163|
|learning_base_pTree_generation_10_[0, 1]_10|learning_base_to_vec_adjacency_set|66.66666666666666%|0.16666666666666666|0.5|0.25|
|learning_base_pTree_generation_10_[0, 1]_10|learning_base_to_vec_laplacian_set|100.0%|0.0|0.0|0.0|
|learning_base_pTree_generation_10_[0, 1]_10|learning_base_to_A3_minus_D|66.66666666666666%|0.16666666666666666|0.5|0.25|
|pTree_basic_cycle_generation_50_[0, 1]_100|learning_base_to_vec_adjacency_set|55.00000000000001%|0.225|0.5|0.3103448275862069|
|pTree_basic_cycle_generation_50_[0, 1]_100|learning_base_to_vec_laplacian_set|60.0%|0.2|0.5|0.28571428571428575|
|pTree_basic_cycle_generation_50_[0, 1]_100|learning_base_to_A3_minus_D|75.0%|0.125|0.5|0.2|
|pTree_basic_cycle_generation_50_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|74.66666666666667%|0.08444444444444445|0.3333333333333333|0.1347517730496454|
|pTree_basic_cycle_generation_50_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|72.66666666666667%|0.0911111111111111|0.3333333333333333|0.1431064572425829|
|pTree_basic_cycle_generation_50_[10, 50, 100]_500|learning_base_to_A3_minus_D|70.0%|0.09999999999999999|0.3333333333333333|0.15384615384615383|
|learning_base_pTree_generation_20_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|74.19354838709677%|0.08602150537634408|0.3333333333333333|0.13675213675213674|
|learning_base_pTree_generation_20_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|77.41935483870968%|0.07526881720430108|0.3333333333333333|0.12280701754385964|
|learning_base_pTree_generation_20_[10, 50, 100]_100|learning_base_to_A3_minus_D|80.64516129032258%|0.06451612903225806|0.3333333333333333|0.1081081081081081|
|learning_base_pTree_generation_20_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|68.87417218543047%|0.10375275938189844|0.3333333333333333|0.15824915824915822|
|learning_base_pTree_generation_20_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|68.21192052980133%|0.10596026490066225|0.3333333333333333|0.16080402010050251|
|learning_base_pTree_generation_20_[10, 50, 100]_500|learning_base_to_A3_minus_D|69.5364238410596%|0.10154525386313466|0.3333333333333333|0.155668358714044|
|pTree_basic_cycle_generation_50_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|73.33333333333333%|0.08888888888888889|0.3333333333333333|0.14035087719298248|
|pTree_basic_cycle_generation_50_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|70.0%|0.09999999999999999|0.3333333333333333|0.15384615384615383|
|pTree_basic_cycle_generation_50_[10, 50, 100]_100|learning_base_to_A3_minus_D|80.0%|0.06666666666666667|0.3333333333333333|0.11111111111111112|
|learning_base_pTree_generation_50_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|70.86092715231787%|0.09713024282560706|0.3333333333333333|0.15042735042735042|
|learning_base_pTree_generation_50_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|71.52317880794702%|0.09492273730684327|0.3333333333333333|0.14776632302405499|
|learning_base_pTree_generation_50_[10, 50, 100]_500|learning_base_to_A3_minus_D|67.54966887417218%|0.10816777041942605|0.3333333333333333|0.1633333333333333|
|pTree_basic_cycle_generation_20_[0, 1]_100|learning_base_to_vec_adjacency_set|55.00000000000001%|0.225|0.5|0.3103448275862069|
|pTree_basic_cycle_generation_20_[0, 1]_100|learning_base_to_vec_laplacian_set|65.0%|0.175|0.5|0.25925925925925924|
|pTree_basic_cycle_generation_20_[0, 1]_100|learning_base_to_A3_minus_D|70.0%|0.15|0.5|0.23076923076923075|
|pTree_basic_cycle_generation_20_[0, 1]_1000|learning_base_to_vec_adjacency_set|56.49999999999999%|0.2175|0.5|0.30313588850174217|
|pTree_basic_cycle_generation_20_[0, 1]_1000|learning_base_to_vec_laplacian_set|51.0%|0.245|0.5|0.32885906040268453|
|pTree_basic_cycle_generation_20_[0, 1]_1000|learning_base_to_A3_minus_D|55.00000000000001%|0.225|0.5|0.3103448275862069|
|learning_base_pTree_generation_100_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|74.19354838709677%|0.08602150537634408|0.3333333333333333|0.13675213675213674|
|learning_base_pTree_generation_100_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|67.74193548387096%|0.10752688172043011|0.3333333333333333|0.16260162601626016|
|learning_base_pTree_generation_100_[10, 50, 100]_100|learning_base_to_A3_minus_D|77.41935483870968%|0.07526881720430108|0.3333333333333333|0.12280701754385964|
|pTree_basic_cycle_generation_100_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|72.66666666666667%|0.0911111111111111|0.3333333333333333|0.1431064572425829|
|pTree_basic_cycle_generation_100_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|72.0%|0.09333333333333334|0.3333333333333333|0.14583333333333334|
|pTree_basic_cycle_generation_100_[10, 50, 100]_500|learning_base_to_A3_minus_D|72.66666666666667%|0.0911111111111111|0.3333333333333333|0.1431064572425829|
|learning_base_pTree_generation_100_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|66.88741721854305%|0.11037527593818985|0.3333333333333333|0.1658374792703151|
|learning_base_pTree_generation_100_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|69.5364238410596%|0.10154525386313466|0.3333333333333333|0.155668358714044|
|learning_base_pTree_generation_100_[10, 50, 100]_500|learning_base_to_A3_minus_D|67.54966887417218%|0.10816777041942605|0.3333333333333333|0.1633333333333333|
|learning_base_pTree_generation_50_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|70.96774193548387%|0.09677419354838711|0.3333333333333333|0.15000000000000002|
|learning_base_pTree_generation_50_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|80.64516129032258%|0.06451612903225806|0.3333333333333333|0.1081081081081081|
|learning_base_pTree_generation_50_[10, 50, 100]_100|learning_base_to_A3_minus_D|80.64516129032258%|0.06451612903225806|0.3333333333333333|0.1081081081081081|
