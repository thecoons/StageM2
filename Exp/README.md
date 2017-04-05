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
|pTree_basic_cycle_generation_20_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|26.666666666666668%|0.75|0.7722222222222223|0.7245791245791247|
|pTree_basic_cycle_generation_20_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|3.3333333333333335%|0.9629629629629629|0.9761904761904763|0.9680464778503994|
|pTree_basic_cycle_generation_20_[10, 50, 100]_100|learning_base_to_A3_minus_D|0.0%|1.0|1.0|1.0|
|pTree_basic_cycle_generation_100_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|50.0%|0.4780578898225957|0.4978021978021978|0.4581196581196582|
|pTree_basic_cycle_generation_100_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|30.0%|0.6185185185185186|0.5948051948051948|0.6031347962382445|
|pTree_basic_cycle_generation_100_[10, 50, 100]_100|learning_base_to_A3_minus_D|36.666666666666664%|0.6509157509157509|0.6306397306397307|0.6361111111111111|
|pTree_basic_cycle_generation_20_[0, 1]_500|learning_base_to_vec_adjacency_set|28.000000000000004%|0.7372229760289462|0.7105580088317944|0.7083333333333333|
|pTree_basic_cycle_generation_20_[0, 1]_500|learning_base_to_vec_laplacian_set|20.0%|0.818961818961819|0.7975190076030412|0.7960016319869441|
|pTree_basic_cycle_generation_20_[0, 1]_500|learning_base_to_A3_minus_D|5.0%|0.9489795918367347|0.9553571428571428|0.949753793588584|
|pTree_basic_cycle_generation_50_[0, 1]_500|learning_base_to_vec_adjacency_set|46.0%|0.559177888022679|0.5334133653461385|0.47987336047037543|
|pTree_basic_cycle_generation_50_[0, 1]_500|learning_base_to_vec_laplacian_set|23.0%|0.7827614716825134|0.7740384615384616|0.7688674505074867|
|pTree_basic_cycle_generation_50_[0, 1]_500|learning_base_to_A3_minus_D|23.0%|0.7747474747474747|0.7724358974358975|0.769792813532179|
|pTree_basic_cycle_generation_10_[0, 1]_10|learning_base_to_vec_adjacency_set|50.0%|0.5|0.25|0.3333333333333333|
|pTree_basic_cycle_generation_10_[0, 1]_10|learning_base_to_vec_laplacian_set|50.0%|0.5|0.25|0.3333333333333333|
|pTree_basic_cycle_generation_10_[0, 1]_10|learning_base_to_A3_minus_D|50.0%|0.25|0.5|0.3333333333333333|
|pTree_basic_cycle_generation_20_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|26.0%|0.7421529805250735|0.7488823877457103|0.742730081723411|
|pTree_basic_cycle_generation_20_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|2.666666666666667%|0.9722002635046114|0.9748803827751197|0.9732804232804234|
|pTree_basic_cycle_generation_20_[10, 50, 100]_500|learning_base_to_A3_minus_D|0.0%|1.0|1.0|1.0|
|learning_base_pTree_generation_10_[0, 1]_10|learning_base_to_vec_adjacency_set|33.33333333333333%|0.3333333333333333|0.5|0.4|
|learning_base_pTree_generation_10_[0, 1]_10|learning_base_to_vec_laplacian_set|33.33333333333333%|0.75|0.75|0.6666666666666666|
|learning_base_pTree_generation_10_[0, 1]_10|learning_base_to_A3_minus_D|33.33333333333333%|0.3333333333333333|0.5|0.4|
|pTree_basic_cycle_generation_50_[0, 1]_100|learning_base_to_vec_adjacency_set|70.0%|0.15789473684210525|0.42857142857142855|0.23076923076923078|
|pTree_basic_cycle_generation_50_[0, 1]_100|learning_base_to_vec_laplacian_set|55.00000000000001%|0.43333333333333335|0.44999999999999996|0.41333333333333333|
|pTree_basic_cycle_generation_50_[0, 1]_100|learning_base_to_A3_minus_D|35.0%|0.78125|0.6818181818181819|0.6266666666666667|
|pTree_basic_cycle_generation_50_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|38.0%|0.6037412900800878|0.6014300457024915|0.6007679702594957|
|pTree_basic_cycle_generation_50_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|9.333333333333334%|0.9117625462453048|0.9082080200501252|0.9098150782361308|
|pTree_basic_cycle_generation_50_[10, 50, 100]_500|learning_base_to_A3_minus_D|4.666666666666667%|0.9497354497354498|0.9586390217969165|0.9531380003857067|
|learning_base_pTree_generation_20_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|38.70967741935484%|0.6071428571428571|0.5820512820512821|0.5835294117647059|
|learning_base_pTree_generation_20_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|6.451612903225806%|0.9419191919191919|0.9333333333333332|0.9325971934667588|
|learning_base_pTree_generation_20_[10, 50, 100]_100|learning_base_to_A3_minus_D|3.225806451612903%|0.9722222222222222|0.9743589743589745|0.9721739130434783|
|learning_base_pTree_generation_20_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|28.47682119205298%|0.7009107468123862|0.6960317460317461|0.6978010613707273|
|learning_base_pTree_generation_20_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|3.9735099337748347%|0.9539833189531205|0.9577441077441077|0.9553627157705322|
|learning_base_pTree_generation_20_[10, 50, 100]_500|learning_base_to_A3_minus_D|1.3245033112582782%|0.9869281045751634|0.9869281045751634|0.9866666666666667|
|pTree_basic_cycle_generation_50_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|36.666666666666664%|0.6851851851851852|0.6215488215488215|0.6187739463601533|
|pTree_basic_cycle_generation_50_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|26.666666666666668%|0.7380471380471381|0.7575757575757575|0.7417508417508417|
|pTree_basic_cycle_generation_50_[10, 50, 100]_100|learning_base_to_A3_minus_D|26.666666666666668%|0.7194444444444444|0.7289562289562289|0.7206542927366725|
|learning_base_pTree_generation_50_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|58.27814569536424%|0.4238284827393404|0.40081139790442116|0.40485714285714286|
|learning_base_pTree_generation_50_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|9.933774834437086%|0.9013522012578616|0.9011123680241327|0.9001194237070766|
|learning_base_pTree_generation_50_[10, 50, 100]_500|learning_base_to_A3_minus_D|9.933774834437086%|0.9052231718898386|0.9011715797430083|0.9020886228457036|
|pTree_basic_cycle_generation_20_[0, 1]_100|learning_base_to_vec_adjacency_set|40.0%|0.6274509803921569|0.5656565656565656|0.5238095238095238|
|pTree_basic_cycle_generation_20_[0, 1]_100|learning_base_to_vec_laplacian_set|25.0%|0.8076923076923077|0.7916666666666667|0.7493734335839599|
|pTree_basic_cycle_generation_20_[0, 1]_100|learning_base_to_A3_minus_D|25.0%|0.8529411764705883|0.6875|0.6865203761755485|
|pTree_basic_cycle_generation_20_[0, 1]_1000|learning_base_to_vec_adjacency_set|9.5%|0.9154788301129764|0.8974747474747475|0.9023412402662485|
|pTree_basic_cycle_generation_20_[0, 1]_1000|learning_base_to_vec_laplacian_set|21.5%|0.7928396572827416|0.7873586227604845|0.7843476516462298|
|pTree_basic_cycle_generation_20_[0, 1]_1000|learning_base_to_A3_minus_D|1.0%|0.9906542056074766|0.9894736842105263|0.9899638699317543|
|learning_base_pTree_generation_100_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|61.29032258064516%|0.33465608465608465|0.42777777777777776|0.36668967103749717|
|learning_base_pTree_generation_100_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|48.38709677419355%|0.5063131313131314|0.5198717948717949|0.5123015873015874|
|learning_base_pTree_generation_100_[10, 50, 100]_100|learning_base_to_A3_minus_D|22.58064516129032%|0.7438672438672439|0.7333333333333334|0.7336860670194004|
|pTree_basic_cycle_generation_100_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|47.333333333333336%|0.49958956475889177|0.5523830972757453|0.5091730605285593|
|pTree_basic_cycle_generation_100_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|22.0%|0.7816566626650662|0.7918586789554531|0.7807444541315509|
|pTree_basic_cycle_generation_100_[10, 50, 100]_500|learning_base_to_A3_minus_D|28.000000000000004%|0.7067248546757389|0.7121830361422683|0.709197235513025|
|learning_base_pTree_generation_100_[10, 50, 100]_500|learning_base_to_vec_adjacency_set|57.615894039735096%|0.45476588628762543|0.4394153398390687|0.44017162778224733|
|learning_base_pTree_generation_100_[10, 50, 100]_500|learning_base_to_vec_laplacian_set|28.47682119205298%|0.7015573770491804|0.7145813004463468|0.7052029873390557|
|learning_base_pTree_generation_100_[10, 50, 100]_500|learning_base_to_A3_minus_D|29.80132450331126%|0.7044284025667005|0.7294514062935117|0.7122777185676478|
|learning_base_pTree_generation_50_[10, 50, 100]_100|learning_base_to_vec_adjacency_set|64.51612903225806%|0.31837606837606836|0.3723544973544974|0.33666333666333664|
|learning_base_pTree_generation_50_[10, 50, 100]_100|learning_base_to_vec_laplacian_set|16.129032258064516%|0.8273809523809524|0.8214285714285715|0.8156288156288155|
|learning_base_pTree_generation_50_[10, 50, 100]_100|learning_base_to_A3_minus_D|16.129032258064516%|0.8417508417508417|0.8677248677248678|0.8470588235294118|
