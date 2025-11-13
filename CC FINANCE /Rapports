
## Dossiers principaux

- **bank**
  - bank-full.csv : version complète du jeu de données classique sur le marketing bancaire (plus de 41 000 lignes).
  - bank.csv : version échantillonnée, plus petite (~4 500 lignes).
  - bank-names.txt : fichier expliquant toutes les variables (métadonnées).
- **bank-additional**
  - bank-additional-full.csv : version mise à jour et plus détaillée (41 188 lignes, plus de 20 variables).
  - bank-additional.csv : sous-ensemble plus petit (plus de 4 000 lignes).
  - bank-additional-names.txt : documentation décrivant chaque attribut.


## Origine du jeu de données

Ces ensembles de données proviennent de l’UCI Machine Learning Repository. Ils ont été collectés à partir de campagnes marketing téléphoniques menées par une banque portugaise.  
Chaque enregistrement correspond aux résultats d’une campagne visant à convaincre des clients de souscrire à un dépôt à terme.


## Résumé du contenu

- Chaque ligne représente un client contacté durant une campagne.
- Chaque colonne décrit :
  - Les attributs personnels du client : âge, emploi, situation familiale, niveau d’éducation
  - Le contexte socio-économique : taux de variation de l’emploi, indice des prix à la consommation
  - Les détails liés à la campagne : nombre de contacts, jours depuis le dernier contact, etc.
  - La variable d’issue :
    - **y** = si le client a souscrit ou non à un dépôt à terme (oui / non).



## Attributs clés

| Catégorie            | Variables                                                        | Description                                     |
|----------------------|------------------------------------------------------------------|-------------------------------------------------|
| Données client       | age, job, marital, education, default, housing, loan             | Contexte démographique et financier             |
| Campagne             | contact, month, day_of_week, duration                           | Informations sur la méthode de contact et la date |
| Campagne précédente  | campaign, pdays, previous, poutcome                             | Données sur les contacts antérieurs             |
| Contexte économique  | emp.var.rate, cons.price.idx, cons.conf.idx, euribor3m, nr.employed | Indicateurs macroéconomiques                    |
| Variable cible       | y                                                                | Souscription ou non à un dépôt à terme          |


## Différences entre les versions “bank” et “bank-additional”

| Version          | Description                                      | Nombre de lignes | Fonctionnalités supplémentaires                      |
|------------------|--------------------------------------------------|------------------|------------------------------------------------------|
| bank             | Jeu de données original (basique)                | ~45 211          | Sans indicateurs macroéconomiques                    |
| bank-additional  | Version enrichie et mise à jour                  | ~41 188          | Inclut des indicateurs économiques et les jours de la semaine |


## Cas d’usage possibles

- Modélisation prédictive : Régression logistique, Random Forest, etc.
- Segmentation client : Identification des profils les plus susceptibles de souscrire.
- Optimisation marketing : Analyse des stratégies de contact efficaces (mois, canal, durée).
- Analyse des tendances économiques : Étude de l’impact du contexte macroéconomique sur la prise de décision des clients.


