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