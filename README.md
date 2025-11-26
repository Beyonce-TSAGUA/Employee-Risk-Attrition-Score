# 🧠 Employee Risk & Attrition Score

> 🎯 Projet de Data Science appliqué au pilotage RH dans un contexte Assurance / Banque

---

## 📌 Objectif du projet

Anticiper le risque RH à travers un **Employee Risk Score intelligent**, capable de prédire :

* Le risque d’attrition (départ volontaire)
* Le risque d’absentéisme
* La baisse de performance
* L’insatisfaction globale

👉 Finalité métier : permettre aux décideurs RH d’intervenir AVANT que la situation ne dégénère.

Ce projet s’inscrit dans une logique proactive, orientée performance humaine et durabilité sociale.

---

## 🗂️ Données utilisées

Fichier principal :

```
data/employee_risk_attrition_dirty.csv
```

Variables clés exploitées :

* age
* tenure_years
* salary
* satisfaction_level
* performance_score
* absenteeism_days
* overtime_hours
* manager_rating
* job_role
* attrition (cible)

Les données ont été volontairement salies (valeurs manquantes, anomalies) pour simuler un contexte réel d’entreprise.

---

## ⚙️ Déroulé méthodologique

### 1. Data Understanding

* Analyse du schéma des données
* Identification des variables numériques et catégorielles

### 2. Data Cleaning

* Gestion des valeurs manquantes via flags
* Détection des valeurs hors logique métier

### 3. Feature Engineering

* Création de ratios
* Scores composites
* Encodage des variables catégorielles

### 4. Modélisation

Trois modèles testés :

* Logistic Regression (baseline)
* Random Forest
* XGBoost ✅ (meilleur modèle retenu)

Métriques utilisées :

* Accuracy
* F1-score
* ROC-AUC

### 5. Explainability

* Feature Importance
* SHAP Values

### 6. Création du Employee Risk Score

Score final combinant :

```
Risk Score = f(Attrition + Absentéisme + Performance + Satisfaction)
```

---

## 📊 Résultats clés

* XGBoost surpasse les autres modèles en précision et stabilité
* Variables les plus influentes :

  * satisfaction_level
  * absenteeism_days
  * performance_score
  * overtime_hours

Visualisations disponibles :

* Heatmap de corrélation
* Courbe ROC
* Feature importance
* Distribution des scores de risque

---

## 🧪 Comment exécuter le projet ?

### Prérequis

Python 3.9+

Installer les dépendances :

```bash
pip install -r requirements.txt
```

Lancer le notebook :

```bash
jupyter notebook employee_risk_score.ipynb
```

---

## 🧩 Structure du projet

```
Employee-Risk-Score/
│
├── notebook.ipynb
├── README.md
├── data/
│   ├── employee_risk_attrition_dirty.csv
│   └── employee_risk_clean.csv
├── models/
│   └── rl_model.pkl
│   └── rf_model.pkl
│   └── xgb_model.pkl
```

---

## 🏢 Applications métiers

✅ Détection préventive des collaborateurs à risque
✅ Orientation RH ciblée (formation, coaching, charge de travail)
✅ Aide à la décision pour managers et DRH

---

## 🚧 Limites & perspectives

Limites actuelles :

* Données simulées
* Absence de données comportementales fines

Améliorations futures :

* Intégration NLP (analyse de feedbacks employés)
* Dashboard interactif Streamlit / Power BI
* Automatisation via API

---

## 🚀 Vision

Ce projet illustre la transition d’une gestion RH réactive vers une gouvernance prédictive basée sur la performance humaine et la donnée car la technologie ne remplace pas l’humain, elle l’éclaire.

---

## 👨‍💻 Auteur

Projet réalisé dans un objectif de montée en compétences en Data Science RH & Business Intelligence.

---
