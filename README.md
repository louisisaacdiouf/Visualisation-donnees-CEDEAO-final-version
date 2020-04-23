# Visualisation-donnees-CEDEAO-final-version

Ce projet est un travail pratique proposé par nos professeur pour nous permettre d'assimiler les bases de la visualisation et de l'étude des données. Cela a été pour nous une première expérience de collecte de données, de traitement et de représentation. Nous sommes en première année de Master en Sciences des Données et Applications et ce projet est loin d'être achevé ! Nous sommes donc ouverts à toute suggestion et contribution.

## Les outils utilisés

Pour la réalisation de ce projet, nous avons utilisé les données du site https://data.un.org/ qui recense les chiffres sur l'économie des Etats du monde, en particulier, ceux des Etats membres de la CEDEAO sur lesquels porte notre étude. Nous avons également utilisé la bibliothèque https://d3js.org/ pour la représentation des données, un peu de bootstrap et de jQuery lors de nos test, les travaux de Alangrafu (https://github.com/alangrafu/radar-chart-d3) nous ont permis de d'avoir un diagramme radar satisfaisant, nous avons aussi trouvé des informations très utiles dans les forums https://stackoverflow.com/ et https://support.mozilla.org/fr/kb/obtenir-assistance-communaute qui sont des communautés où tout développeur peut facilement trouver la solution à un problème qu'il rencontre, car en programmation, il est très rare de rencontrer un problème qu'aucune autre personne n'a rencontré auparavant.

Pour la réalisation de l'article, nous avons utilisé Sublime Text pour la réalisation du texte au format LaTeX.

## Les données utilisées

Les données fournies par le site https://data.un.org/ sont très riches en informations. Elles nous ont permis d'avoir un aperçu de l'économie des Etats de la CEDEAO durant ces 15 dernières années.

## Types de représentations choisies

Etant donné que les données économiques n'ont pas les mêmes unités, il est très difficile d'en tirer des informations claires si on n'en fait qu'une seule représentation sur un diagramme en barre. Nous avons donc opté pour deux types de visualisation : une visualisation générale avec des diagrammes en barres groupés, et une visualisation comparative pour laquelle nous avons utilisé le diagramme radar ou `Spider Chart`.

## Motifs de ces choix

Le diagramme en barre est un digramme classique qui permet de représenter plusieurs modalités et d'en aprécier les différences ou les ressemblances. Notons qu'elle permet aussi bien de comparer des caractères du même individu de la population aussi bien que des caractères d'individus différents.
Nous avons ensuite choisi le diagramme radar pour une représentation comparative, car sachant que les variables de notre études n'ont pas les mêmes unités de mesure et qu'elles interviennent toutes dans l'économie, il faudrait représenter toutes les variables sur un même diagramme pour comprendre pourquoi un pays est plus développé qu'un autre.

## Avantages et inconvénients des diagrammes

Le diagramme en barres nous permet principalement une représentation globale de toutes les modalités, avec la possibilité de confronter des modalités de plusieurs pays à la fois, et de manière à bien distinguer les niveau de chacun. Par contre, à moins d'uniformiser les données, on a de très grandes irrégularités dans les représentations. Le Spider Chart quand à lui, même s'il ne permet pas la représentation d'une grande quantité d'informations sans perdre de la lisibilité, il a pour avantage principal de voir clairement, pour chaque variable, la différence de niveau entre deux individus.

## Méthodes d'uniformisation

Pour une meilleure lisibilité des données, nous avons effectué une uniformisation des données, en faisant correspondreè à `100%` le maximum de chaque variable. Nous avons donc chaque variable exprimée en pourcentage, et nous pouvons ainsi facilement les comparer, car on réduit considérablement les disparités.
Ensuite, étant donné que certaines variables peuvent être regroupées dans une même catégorie, nous avons procédé à un échantillonnage, en utilisant la moyenne des pourcentages comme estimateur. Nous avons procédé ainsi, de façon progressive, jusqu'à arriver à représenter toute l'économie par une seule variable. Pour cela, nous avons pris le `Nigéria`comme pays de référence. Notons que, comme tout estimateur, ces variables synthétiques seront parfois bien représentatives de séries, mais parfois ils arrivent qu'ils soient très loins de la réalité.

## Méthodes d'intégration des données

Pour ce projet, nous avons utilisé deux méthodes d'intégration des données, à savoir :
* l'appel des données par la fonction d3.csv qui, nous permet d'appeler tous les fichiers CSV contenant les données en même temps, mais malgré beaucoup de recherches, nous n'avons pas trouvé de moyens d'utiliser ses données à l'extérieur de la fonction.
* création des objects JavaScript qui contiennent tous les données des fichiers CSV pour un appels plus rapide et plus simples, notamment avec les diagrammes en barres. Pour cette méthode, nous avons utilisé le site https://www.convertcsv.com/csv-to-json.htm pour convertir nos fichier CSV en JSON que nous pouvons appeler de n'importe où.

## Etapes de réalisation

1. Pour la représentation, nous avons d'abord fusionné l'ensemble des tableaux contenant les données de tous les pays
2. Ensuite, nous avons cherché le maximum de chaque modalité pour procéder à l'uniformisation
3. Après nous avons effectué une première catégorisation qui regroupe les variables en des secteurs d'activités
4. Et pour terminer nous avons utilisé ces données pour faire la représentation.

Notons que la catégorisation permet en même temps d'éliminer les variables absentes chez certains pays, et donc de faire une étude avec un nombre uniforme de variables.

## Images

### Diagrammes en barres groupés

![Vue générale](https://github.com/louisisaacdiouf/Visualisation-donnees-CEDEAO-final-version/blob/master/captures/Capture1.PNG)

![Première catégorisation](https://github.com/louisisaacdiouf/Visualisation-donnees-CEDEAO-final-version/blob/master/captures/Capture2.PNG)

![Première catégorisation](https://github.com/louisisaacdiouf/Visualisation-donnees-CEDEAO-final-version/blob/master/captures/Capture3.PNG)

![Niveau économique](https://github.com/louisisaacdiouf/Visualisation-donnees-CEDEAO-final-version/blob/master/captures/Capture4.PNG)

### Diagrammes en barres groupés

![Comparaison générale](https://github.com/louisisaacdiouf/Visualisation-donnees-CEDEAO-final-version/blob/master/captures/Capture5.PNG)

![Comparaison des secteurs d'activités](https://github.com/louisisaacdiouf/Visualisation-donnees-CEDEAO-final-version/blob/master/captures/Capture6.PNG)


## Conclusion et perspectives

Ce projet nous a permis de mener les recherches qui nous ont fait entrevoir les compétences requises pour les sciences des données. Nous avons trouvé qu'il y avait plusieurs manières de faires les représentations et plusieurs bibliothèques disponibles, ce qui nous montre que c'est un domaine florissant.
Le principal soucis que nous avons rencontré concernant l'étude des données, c'est le fait de ne pas avoir un coefficient ou une indication qui nous montre à quelle point une variable est importante dans l'économie d'un pays car, cela est primordial pour faire la synthèse. En effet, si on arrive à établir un degré de corrélation de chaque variable dans l'économie d'un pays, les représenter après avoir fait les calculs avec leurs coefficients respectifs nous permettraient de voir avec une très grande précision le niveau économique de chaque pays dans l'espace UEMOA.


##### Un grand merci à tous nos professeurs pour la qualité de l'enseignement et nos camarades de classe pour l'entraide.