# Prédiction du prix des véhicules automobiles

Ce projet explore un dataset de véhicules automobiles pour comprendre
quels facteurs influencent le prix de vente (MSRP).
Je compare une régression linéaire et un Random Forest pour voir
laquelle des deux approches prédit le mieux les prix.


## Ce que j'ai fait

Je suis parti d'un dataset brut avec des valeurs manquantes,
des doublons et des prix extrêmes. J'ai nettoyé les données,
exploré les corrélations entre variables, puis modélisé
le prix avec deux algorithmes différents.

Le pipeline de prétraitement garantit qu'aucune information
du jeu de test ne contamine l'entraînement : imputation,
standardisation et encodage sont appris sur le train uniquement.



## Résultats

Le Random Forest surpasse nettement la régression linéaire.
La puissance moteur et le nombre de cylindres sont les variables
les plus importantes pour prédire le prix.

Les résidus sont globalement centrés autour de zéro, avec quelques
erreurs plus élevées sur les modèles haut de gamme — difficiles
à capturer avec les seules caractéristiques techniques.



## Étapes du notebook

Chargement et exploration du dataset  distribution du prix,
types de variables, valeurs manquantes.

Nettoyage  suppression de la colonne Market Category,
doublons, outliers sur le prix par méthode IQR.

Analyse exploratoire  corrélations, répartition
des variables catégorielles.

Préparation  séparation train/test avant tout prétraitement,
pipeline sklearn avec imputation, standardisation
et encodage ordinal.

Modélisation  régression linéaire et Random Forest,
tous deux dans un pipeline complet.

Évaluation — R^2, MAE, RMSE, graphique prédit vs réel,
analyse des résidus, importance des variables.



## Stack

Python, pandas, scikit-learn, matplotlib, seaborn



## Dataset

Le fichier source est un dataset public de véhicules automobiles
disponible sur Kaggle.


