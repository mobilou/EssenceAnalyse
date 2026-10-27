# EssenceAnalyse

                        INSEE 

Série SP95-E10 (2019-2026)
identifiant BDM :010596132
Libellé : Prix moyens mensuels de vente au détail en métropole - Supercarburant sans plomb 95-E10 (1 litre)

Téléchargement du fichier csv : valeurs_mensuelles.csv


                        Excel 

    1 - Encodage
Des caractères spéciaux peuvent apparaitrent (comme Ã©) car Excel ouvre le csv sans comprendre que il est encodé en UTF-8

-Ouverture d'un classeur Excel vide
-Get/Data : selection du fichier valeurs_mensuelles.csv
-Next
-vérification qu'il est bien en UTF-8

    2 - Nettoyage des lignes
Dans le fichier, les 4 premieres lignes ne servent à rien car pour l'analyse, on va devoit les supprimer.

-remove row (clique sur le petit cadriage a coter des colonnes)
-entre 4 (pour les 4 premiers lignes)

Ensuite, on va devoir renommer les colonnes

-Column1 = Date
-Column2 = Prix

    3 - Telechargement du fichier
Une fois que les deux étapes sont terminées, il suffit de cliquer sur Close&Load et telecharger le fichier csv nettoyé.



Nettoyage des données : 

-is.null() permet de repérer les valeures Null/NaaN
Aucune valeure n'a été détéctée.

On entre les données dans un dictionnaire afin d'ajouter chaque Date (keys) à son Prix (value)
.item() permet de convertir un float en données standard python. (converti np.float(x) => float)


On inverse les données du df afin de commencer par un ordre croissant


On range chaque prix par mois dans une liste
-8 listes au total
-12 valeurs par liste, sauf pour la derniere (2026)
-9 valeurs pour 2026

On calcul le prix moyen par an
-2019 : 1.4875
-2020 : 1.3541666666666667
-2021 : 1.5408333333333333
-2022 : 1.7774999999999999
-2023 : 1.875
-2024 : 1.7966666666666666
-2025 : 1.7025
-2026 : 1.4475



On calcul les taux de croissances par mois

-2019 : [2.142857142857145, 2.7972027972028, 4.761904761904766, 1.2987012987012998, -3.2051282051282075, -0.6622516556291397, -1.3333333333333344,
0.0, 0.0, 0.6756756756756763, 1.342281879194632]

-2020 : [-2.6143790849673225, -6.71140939597316, -8.633093525179849, -1.5748031496063006, 4.800000000000004, 2.2900763358778646, -0.7462686567164185, 0.0, 0.0, 0.0, 1.5037593984962419]

-2021 : [3.5714285714285747, 3.448275862068969, 0.6666666666666672, 0.0, 1.3245033112582794, 1.960784313725492, 0.6410256410256416, 0.0, 3.8216560509554034, 1.2269938650306762, -2.424242424242413]

-2022 : [4.733727810650891, 10.734463276836156, -10.20408163265306, 7.38636363636363, 10.052910052910063, -6.250000000000005, -9.230769230769226, -14.689265536723164, 7.284768211920537, 3.703703703703693, -1.7857142857142874]

-2023 : [1.612903225806441, 0.5291005291005296, 1.578947368421054, -4.145077720207246, 0.540540540540541, -1.0752688172043021, 4.891304347826079, 1.0362694300518145, -4.102564102564095, -2.1390374331550817, -2.1857923497267775]

-2024 : [2.2346368715083815, 1.6393442622950833, 2.688172043010743, -1.5706806282722525, -3.191489361702119, 0.0, -2.1978021978021998, -4.494382022471914, 1.176470588235295, 0.0, 0.5813953488372098]

-2025 : [0.0, -3.3898305084745792, -1.1695906432748548, -1.1834319526627228, 1.1976047904191627, -0.5917159763313614, 0.5952380952380958, 0.5917159763313614, -1.176470588235295, 1.7857142857142874, -2.3391812865497097]

-2026 : [1.1904761904761916, 11.176470588235292, 5.820105820105825, 2.0000000000000018, -4.901960784313729, 1.546391752577321, 2.0304568527918687, 6.467661691542307]


