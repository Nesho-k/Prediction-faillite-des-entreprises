# Prédiction de la Faillite des Entreprises

## Description du Projet

Ce projet a pour objectif d’analyser les facteurs liés à la faillite des entreprises en exploitant un ensemble de données anonymisées. Grâce à des méthodes statistiques et à des modèles d’apprentissage automatique, nous cherchons à estimer la probabilité qu’une entreprise rencontre des difficultés financières. L’objectif ultime est d’apporter des informations précieuses pour anticiper et prévenir ces situations.

## Étapes de l'analyse 
Le projet suit les étapes suivantes :


### Exploration des Données :
 
![Capture d’écran 2025-02-01 122104](https://github.com/user-attachments/assets/d9e01b83-ef61-41bb-98a1-7fcc662cbfed)

- Chargement et nettoyage des données.
- Analyse descriptive pour identifier les tendances générales.

![Capture d’écran 2025-02-01 122530](https://github.com/user-attachments/assets/1f848a8a-f2d9-4037-8de5-e9000ff51f5d)

Le jeu de données comporte 96 variables quantitatives. La variable à expliquer est quant à elle la variable "Bankrupt?".

### Analyse Statistique :
- Création de graphiques (box plots) pour les variables quantitatives afin d'analyser la répartition de nos données.
- Tests statistiques (Kruskal-Wallis pour les variables quantitatives) afin d'identifier les facteurs significatifs.

### Préparation des Données :
- Division des données en ensembles d'entraînement et de test.

### Modélisation :
- Création d'un modèle de régression logistique pour prédire la dépression.
- Évaluation de la qualité du modèle à l'aide de la courbe ROC.
- Exploration d'autres modèles comme les Random Forest, AdaBoost, SVM et XGBoost.

## Résultats
### Régression Logistique

![Capture d’écran 2025-02-01 122725](https://github.com/user-attachments/assets/e087ebd2-e6bf-4333-9555-a8e8c2338e03)


Le premier modèle utilisé est une régression logistique. Les résultats montrent un AUC (Area Under the Curve) de 0,51 sur l'ensemble d'entraînement et 0,49 sur l'ensemble de test, autrement dit le modèle est très mauvais puisque même le hasard fait mieux.

### Modèles Alternatifs
Plusieurs autres modèles ont été testés :

- Random Forest : Ce modèle présente un surajustement important, le rendant moins efficace.
- SVM : Les performances du modèle sont plutôt médiocres.
- XGBoost : Les performances de ce modèle sont moins bonnes que celle de l'Adaboost.
- Adaboost : C'est le meilleur modèle, car il ne présente pas d'overfitting et est le plus performant, avec une précision globale de 40 %. L'Adaboost a été retenu comme modèle final.


### Optimisation de l'Adaboost

![Capture d’écran 2025-02-01 124306](https://github.com/user-attachments/assets/b3bae354-e993-44eb-8269-a0e36daa83c5)

Un nouveau modèle avec une recherche d'hyperparamètres a été effectuée pour optimiser le modèle Adaboost. Le modèle présente une performance moyenne mais un faible risque d'overfitting ou d'underfitting. 

![Capture d’écran 2025-02-01 124248](https://github.com/user-attachments/assets/71e0f2ff-aae2-49e3-b425-1a772376327a)

En effet, la précision pour la classe 1 est de 54 %, ce qui signifie que, parmi toutes les fois où le modèle a prédit qu'une entreprise allait faire faillite, il avait raison environ 5 fois sur 10.


## Conclusion

L'Adaboost a été retenu comme le meilleur modèle pour prédire la faillite des entreprises, avec un score de précision globale de plus de 40 %. Ce modèle pourrait être utilisé pour identifier les entreprises qui risquent de faire faillite et anticiper ces situations.

## Perspectives d'Amélioration
- Utilisation de modèles plus avancés comme les réseaux de neurones.
- Collecte de données supplémentaires pour affiner les prédictions.

Projet réalisé par Nesho Kanthakumar
