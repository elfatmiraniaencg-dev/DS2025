## Predicting Loan Payback | Vault
Prédiction de Remboursement de Prêts

## 📊 Vue d'ensemble du projet
Ce projet implémente une stratégie d'ensemble (blending) pour améliorer les prédictions de remboursement de prêts dans le cadre d'une compétition Kaggle. L'approche combine plusieurs modèles de machine learning avec des poids optimisés pour atteindre un score de 0.92775 sur le leaderboard (Rank #23).

## 🎯 Objectif
Prédire la probabilité qu'un emprunteur rembourse son prêt en utilisant une méthode de blending pondéré de plusieurs soumissions.

## 🔧 Méthodologie
Architecture de Blending
Le système utilise une approche de weighted blending qui combine les prédictions de plusieurs modèles en appliquant des poids optimisés à chaque soumission. Cette technique d'ensemble learning permet de capitaliser sur les forces de différents modèles tout en minimisant leurs faiblesses individuelles.

## Principe du Blending Pondéré
Le blending pondéré consiste à calculer une moyenne pondérée des prédictions de plusieurs modèles. Chaque modèle reçoit un poids qui reflète sa performance relative et sa fiabilité. La prédiction finale est obtenue en combinant ces prédictions individuelles selon leurs poids respectifs, puis en normalisant le résultat.
Configuration des Poidscompetition will be used for blending and ensemble experiments.
