# Satisfaction des passagers des compagnies aériennes

## Description
Ce projet implémente un pipeline complet pour :
- Nettoyer et prétraiter les données,
- Entraîner un modèle de machine learning optimisé,
- Évaluer ses performances,
- Sauvegarder le modèle dans un fichier pour une utilisation future.

Le modèle utilisé est un **HistGradientBoostingClassifier**, configuré avec des hyperparamètres optimisés.

---

## Prérequis

### Environnement Python
1. Assurez-vous que **Python (version >= 3.7)** est installé. Vérifiez votre version avec :
   ```bash
   python --version
   ```
2. Le fichier `Airline_Dataset.csv` doit être dans le dossier `data`
---

## Configuration de l'environnement

### Création et activation
1. Créez un environnement virtuel :
   ```bash
   python -m venv .venv
   ```
2. Activez l'environnement :
   - Sur **Windows** :
     ```bash
     .venv\Scripts\activate
     ```
   - Sur **Mac/Linux** :
     ```bash
     source .venv/bin/activate
     ```

3. Mettez à jour `pip` :
   ```bash
   pip install --upgrade pip
   ```

---

## Installation des dépendances

Installez les bibliothèques nécessaires au projet :
```bash
pip install -r requirements.txt
```

---

## Exécution du script

### Étapes
1. Le fichier `Airline_Dataset.csv` doit être dans le dossier `data`
2. Activez votre environnement virtuel.
3. Lancez le script avec la commande suivante :
   ```bash
   python pipeline.py
   ```

### Résultats attendus
- Un rapport de classification (précision, rappel, f1-score) s’affichera dans la console.
- Un fichier `optimized_model.pkl` contenant le modèle entraîné sera généré.

---

## Structure du projet

Organisation des fichiers :
```
BRIEF_PLANE/ 
├── app/
│   ├── app.py                   # Application principale Streamlit
│   ├── form_ui.py               # Gestion du formulaire utilisateur
│   ├── auth.py                  # (Optionnel) Système d'authentification
│
├── data/
│   ├── Airline_Dataset.csv      # Données brutes
│   ├── cleaned_data.csv         # Données nettoyées (issue du pipeline) (pas encore créé) 
│   ├── database.db              # Base de données relationnelle (pas encore créé) 
│   ├── analytics.db             # Base de données analytique (pas encore créé) 
│
├── models/
│   ├── pipeline.py              # Script principal du pipeline de ML
│   ├── optimized_model.pkl      # Modèle entraîné et sauvegardé
│   ├── model_comparison.py      # Script pour comparer plusieurs modèles (pas encore créé) 
│
├── tests/
│   ├── test_pipeline.py         # Tests unitaires pour le pipeline
│   ├── test_app.py              # Tests unitaires pour l'application web
│
|├── .github/workflows/
│   ├── ci.yml                   # Configuration des GitHub Actions pour l'intégration continue
|
├── .gitignore                   # Fichiers à ignorer pour Git
├── README.md                    # Documentation principale du projet
├── requirements.txt             # Dépendances du projet
└── trello_screenshot.png        # Capture d'écran du Trello (pour la livraison) (pas encore créé) 
```

---

## Résolution des problèmes

1. **Dataset introuvable** :
   - Vérifiez que `Airline_Dataset.csv` est dans le bon dossier.
2. **Problème d'installation des librairies** :
   - Mettez à jour la bibliothèque concernée avec :
     ```bash
     pip install package_name --upgrade
     ```
3. **Problème avec l'environnement virtuel** :
   - Vérifiez que l'environnement est activé avant d’exécuter les commandes.

---
