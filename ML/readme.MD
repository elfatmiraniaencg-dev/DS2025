📝 RAPPORT D’ANALYSE — Wine Quality Dataset
1. Introduction

L’objectif de cette analyse est d’étudier les facteurs qui influencent la qualité du vin (rouge et blanc) en utilisant la base de données Wine Quality provenant de l’UCI Machine Learning Repository.

L’étude se déroule en trois parties :

Analyse exploratoire (EDA)

Visualisation et interprétation des relations entre variables

Construction d’un modèle prédictif pour classifier la qualité du vin

La variable cible quality (note de 0 à 10) est transformée en three classes :

Low : qualité ≤ 5

Medium : qualité 6–7

High : qualité ≥ 8

2. Description du dataset

Le dataset contient :

6497 observations

12 variables physico-chimiques (acidité, alcool, sucre, densité ...)

1 variable cible : quality

Les principales variables sont :

fixed acidity

volatile acidity

citric acid

residual sugar

chlorides

free sulfur dioxide

total sulfur dioxide

density

pH

sulphates

alcohol

quality (0–10)

Aucune valeur manquante n'a été détectée.

3. Analyse exploratoire (EDA)
3.1. Distributions univariées

Les histogrammes montrent :

alcohol : distribution asymétrique → certains vins très alcoolisés

volatile acidity : la plupart des vins ont une acidité volatile faible

density : fortement concentrée autour de valeurs légèrement supérieures à 0.99

residual sugar : distribution très asymétrique → certains vins très sucrés (en particulier les blancs)

3.2. Corrélations

La matrice de corrélation révèle les relations suivantes :

🔺 Variables les plus positivement corrélées à quality :

alcohol (+0.48)

sulphates (+0.25)

citric acid (+0.23)

🔻 Variables les plus négativement corrélées à quality :

volatile acidity (–0.39)

density (–0.31)

chlorides (–0.20)

Conclusion importante :

➡️ Plus le vin est alcoolisé, plus il tend à être bien noté.
➡️ Une acidité volatile élevée détériore considérablement la qualité.

4. Relations entre variables et qualité
4.1. Alcohol vs Quality

Le scatter plot montre clairement une augmentation de la qualité avec le degré d'alcool.

4.2. Boxplots

Les variables les mieux corrélées ont été visualisées par classe :

Les vins haut de gamme (high quality) présentent en moyenne :

plus d’alcool

plus de sulphates

davantage de citric acid

Les vins basse qualité (low quality) présentent :

plus d’acidité volatile

une densité plus élevée

5. Préparation des données

Séparation en X (features) et y (quality_label)

Standardisation des variables numériques

Split en train/test : 75% / 25%

6. Modèle de Machine Learning
Algorithme utilisé :

➡️ RandomForestClassifier (200 arbres)

Ce modèle est adapté car :

il capture les interactions entre variables

il gère bien les distributions non linéaires

il donne une importance des variables interprétable

7. Résultats
7.1. Accuracy

Le modèle obtient environ :

🎯 Accuracy ≈ 0.81 (81%)

→ très satisfaisant pour un problème multi-classe avec classes déséquilibrées.

7.2. Classification Report

Classe “medium” : la mieux prédite (classe majoritaire)

Classe “high” : plus difficile à prédire car peu représentée

Classe “low” : bonnes performances globales

7.3. Matrice de confusion

La plupart des confusions se font entre medium et low

Très peu de confusions entre low ↔ high (ce qui est logique).

8. Importance des variables

Le modèle Random Forest donne :

🔝 Top 5 variables les plus importantes

alcohol (de loin la plus influente)

volatile acidity

sulphates

density

total sulfur dioxide

🔍 Interprétation :

L’alcool joue un rôle majeur dans la perception de la qualité.

L’acidité volatile, facteur négatif, est déterminante pour éviter les défauts.

Les sulphates contribuent positivement à la stabilité et au goût.

La densité reflète souvent le sucre résiduel → vins lourds = qualité souvent inférieure.

📌 9. Conclusion générale

Cette analyse permet de conclure que la qualité du vin dépend principalement de quelques paramètres physico-chimiques :

✔ Les variables qui améliorent la qualité :

alcohol

citric acid

sulphates

✘ Les variables qui dégradent la qualité :

volatile acidity

density

chlorides

Le modèle Random Forest atteint env. 81% de précision, ce qui confirme qu’on peut prédire la qualité du vin avec une bonne fiabilité à partir des mesures chimiques.

L’étude met en évidence que les caractéristiques du vin influencent fortement la qualité perçue et qu’il est possible de modéliser cette perception via des outils de machine learning.
