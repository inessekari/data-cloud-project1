# Health Data Project - Analyse des données de santé

## Objectif

Ce projet vise à construire une architecture Lakehouse en croisant plusieurs sources de données sur la santé (Kaggle) afin d'étudier l'évolution des comportements, de la prise en charge médicale et de l'impact social ou démographique sur les patients.

## Sources de données

Nous avons sélectionné **quatre sources principales** :

1. **Hospital Triage Data** (Kaggle)  
   ➤ Données anonymisées sur les visites aux urgences, symptômes, diagnostics qui seront divisés en plusieurs datasets (patient, maladie, motif d'admission, médicament)

2. **Icd_code** (Données créees)  
   ➤ Données provenant de ICD-10-CM (Classification internationale des maladies, 10e révision, Modification clinique) qui est un système de codage utilisé pour classifier les diagnostics et les procédures médicales dans le système de santé. Ces données ont été combiné aux diagnostics présents dans Hospital Triage Data ainsi qu'une description du diagnostic puis, à une catégorie médicale textuelle.

3. **meds_cat**  
   ➤ Reprise des données concernant les médicaments administrés durant la prise en charge via Hospital Triage Data. Combinées à une classe thérapeutique et un label précisant la correspondance en français.

 4. **motif_categorie**  
   ➤ Reprise des données concernant les motifs d'admission pour la prise en charge via Hospital Triage Data. Combinées à une déscription du motif et une catégorie médicale.

## Architecture du projet

Le projet est structuré selon une architecture **Lakehouse** avec plusieurs zones :

health-data-project/
│
├── data/
│   ├── raw/                     # Données brutes (Kaggle, API, etc.)
│   ├── staging/                 # Données nettoyées, harmonisées
│   └── warehouse/               # Données finales dans un modèle en étoile (fact/dimensions)
│
├── notebooks/                   # Analyses exploratoires (Fabric)
│
├── docs/                        
│   ├── data_dictionnary.md/     # Dictionnaire de données
│   ├── notebooks_overview.md/   # Table des matières courte des notebooks
│   ├── architecture.md/         # Schéma du process
│
├── mcd/                         # Schémas conceptuels (MCD)
│
├── powerbi/                     # Fichiers Power BI (.pbix, exports)
│
├── reports/                     # Rapport final en PDF
│
├── .gitignore                   # Fichiers ignorés par Git (datasets locaux, .env, etc.)
└── README.md                    # Documentation du projet

---


## Étapes techniques

1. **Création du repository GitHub** avec une structure claire  
2. **Collecte des données** via fichiers CSV  
3. **Stockage cloud** (Fabric Lakehouse)  
4. **Nettoyage & transformation** (Notebooks PySpark)  
5. **Modélisation d’un DataWarehouse en étoile**  
6. **Stockage dans la couche Warehouse**
7. **Visualisation dans Power BI**  
8. **Rédaction d’un rapport final (PDF)**

## Modèle conceptuel

Le projet repose sur **un modèle en étoile** (MCD), représenté dans le dossier `/mcd/`.  

## Technologies utilisées

- Python 3.9
- Fabric
- PySpark
- Power BI
- Git & GitHub

## Auteur

> Inès SEKARI & Malaïka NKUIDA – Projet Data Santé | Mai 2025







