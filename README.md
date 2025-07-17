# Prédiction du Trafic de Recettes

## Vue d'ensemble du projet

Ce projet utilise l'apprentissage automatique pour prédire quelles recettes généreront un trafic élevé lorsqu'elles seront mises en avant sur la page d'accueil d'un site web culinaire. L'objectif principal est d'atteindre **80% de précision** dans la prédiction des recettes à fort trafic pour optimiser la stratégie de contenu et augmenter les conversions d'abonnements.

## Structure du projet

```
├── recipe_site_traffic_2212.csv    # Jeu de données des recettes (947 recettes)
├── notebook.ipynb                  # Analyse complète et modélisation
├── model_comparison_results.png    # Visualisations des résultats
└── README.md                      # Ce fichier
```

## Données analysées

- **947 recettes** avec 8 caractéristiques nutritionnelles et catégorielles
- **Variables clés** : calories, glucides, sucre, protéines, catégorie, portions
- **Variable cible** : trafic élevé (binaire : 1 = High, 0 = Low)
- **11 catégories** de recettes (incluant une catégorie inattendue "Chicken Breast")

## Méthodologie

### 1. Nettoyage et validation des données
- Traitement de 52 valeurs manquantes dans les colonnes nutritionnelles
- Standardisation de la colonne "portions" (correction des valeurs textuelles)
- Encodage des catégories et normalisation des variables cibles

### 2. Analyse exploratoire

### 3. Modélisation comparative

#### Modèles testés
1. **Régression logistique** (baseline) - Modèle simple et interprétable
2. **Random Forest** (avancé) - Capture les relations non-linéaires

#### Métriques business développées
- **RSAV** (Recipe Selection Accuracy Value) - Valeur de sélection des recettes
- **ETI** (Expected Traffic Increase) - Augmentation de trafic attendue
- **ESCL** (Expected Subscription Conversion Lift) - Impact sur les conversions
- **Business Value Score** - Score global de valeur métier

## Utilisation pratique

Le modèle Random Forest permet de :
1. **Prédire** le potentiel de trafic des nouvelles recettes
2. **Optimiser** la sélection de contenu pour la page d'accueil
3. **Maximiser** l'impact sur les abonnements
4. **Identifier** les caractéristiques nutritionnelles les plus attractives

## Technologies utilisées

- **Python** : Analyse et modélisation
- **Pandas & NumPy** : Manipulation des données
- **Scikit-learn** : Modèles d'apprentissage automatique
- **Matplotlib & Seaborn** : Visualisations
- **Jupyter Notebook** : Environnement de développement

## Prochaines étapes

1. Déploiement du modèle Random Forest en production
2. Collecte de nouvelles données pour validation continue
3. Optimisation des seuils de décision selon les performances réelles
4. Exploration de modèles plus avancés (XGBoost, réseaux de neurones)

---
