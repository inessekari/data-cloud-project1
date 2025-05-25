## Architecture du pipeline 

Le projet suit une architecture Data Lake en 3 couches (Bronze, Silver, Gold), 
orchestrée à travers une suite de notebooks, chacun correspondant à une étape dédiée du parcours de la donnée. 

- **Bronze** : Données brutes, faiblement transformées ou nettoyées, stockées après ingestion initiale. 

- **Silver** : Données structurées, enrichies, et nettoyées, via jointures et calculs métiers préparant l’exploitation. 

- **Gold** : Tables analytiques organisées selon un schéma en étoile (Star Schema), prêtes pour la BI, la dataviz ou l’analyse avancée. 


```ascii 
[Sources externes]       
        │ 
01_bronze_ingest_clean.ipynb       
        │ 
02_bronze_to_table.ipynb  →  Bronze tables       
        │ 
03_silver_transform.ipynb       
        │ 
04_silver_to_table.ipynb   →  Silver tables       
        │ 
05_gold_star_schema.ipynb       
        │ 
06_gold_to_table.ipynb     →  Gold tables (faits et dimensions)       
        │ 
07_check_tables.ipynb      →  Contrôle qualité final