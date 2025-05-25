Overview

Notebook	                                 Rôle / Objectif	                                        Étapes principales (résumé)

01_bronze_ingest_clean	                     Ingestion et nettoyage initial des données brutes	        - Chargement des fichiers sources
                                                                                                        - Nettoyage basique
                                                                                                        - Harmonisation des schémas


02_bronze_to_table	                        Conversion des données nettoyées en tables bronze	        - Structuration en DataFrames
                                                                                                        - Contrôle et validation
                                                                                                        - Export parquet/csv en bronze


03_silver_transform	                        Transformation avancée et enrichissement des données	    - Jointures opérées
                                                                                                        - Ajout de colonnes dérivées
                                                                                                        - Filtrage, calculs métiers


04_silver_to_table	                        Matérialisation des tables Silver	                        - Sauvegarde/export au format table
                                                                                                        - Contrôles de cohérence supplémentaires


05_gold_star_schema	                        Construction du schéma en étoile de la couche Gold	        - Création des tables de faits et dimensions
                                                                                                        - Structuration finale selon le modèle cible


06_gold_to_table	                        Finalisation et export des tables Gold pour visualisation	- Export définitif Gold
                                                                                                        - Préparation pour BI


07_check_tables	                            Vérifications et contrôle qualité sur l’ensemble des tables	- Checks d’intégrité et de complétude
                                                                                                        - Résumés statistiques
                                                                                                        - Logs d’anomalies ou d’avertissements