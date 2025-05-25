Data Dictionary – Couche Gold



1. Table : dim_patient
 
Colonne	             Type	         Description
patient_id	         long	         Identifiant unique du patient
age	                 integer	     Âge du patient lors de la consultation/enregistrement
gender	             string	         Sexe du patient
profile_id	         string	         Identifiant du profil technique du patient (concaténation de plusieurs variables)
ethnicity	         string	         Origine ethnique déclarée du patient
race	             string	         Race déclarée du patient (USA: White, Black, Asian, etc.)
lang	             string	         Langue principale parlée par le patient
religion	         string	         Religion déclarée du patient
maritalstatus	     string	         Statut marital du patient (célibataire, marié, etc.)
employstatus	     string	         Statut d’emploi/activité professionnelle
insurance_status	 string	         Type ou statut de couverture assurance/mutuelle


2. Table : dim_maladie

Colonne	             Type	         Description
maladie	             string	         Désignation de la maladie (diagnostic)
Code_CIM-10	         string	         Code standardisé CIM-10 du diagnostic
Catégorie_médicale	 string	         Classification médicale associée
Description	         string	         Description textuelle du diagnostic



3. Table : dim_medicament

Colonne	             Type	         Description
medicament	         string	         Code du médicament
medicament_label	 string	         Libellé/nom complet du médicament
classe_therap...     string	         Classe thérapeutique du médicament



4. Table : dim_motif_admission

Colonne	             Type	          Description
motif_admission	     string	          Motif principal d’admission du patient
Catégorie_motif	     string	          Catégorie thématique du motif (urgence, obstétrique…)
Description_longue	 string	          Description détaillée du motif



16. Dim_hopital

Colonne	                      Type	          Description
hospital_id	                  string	      Identifiant unique de l’hôpital
hospital_name	              string	      Nom de l’hôpital



17. Dim_Temps

Colonne	                      Type	          Description
timestamp_id	              string	      Identifiant unique du timestamp/jour/horaire
year	                      integer	      Année
month	                      integer	      Mois (1-12)
day	                          string	      Jour du mois
weekday	                      integer	      Jour de la semaine (0=Dimanche, 1=Lundi, etc.)
hour_bin_start	              string	      Heure de début de l’intervalle
hour_bin_end	              integer	      Heure de fin de l’intervalle



18. fact_df (Table des faits consultation)
 
Colonne	                       Type	          Description
visit_id	                   integer	      Identifiant unique de la visite/consultation
patient_id	                   long	          Identifiant du patient
hopital_id	                   string	      Identifiant de l’hôpital
date_id	                       string	      Date de la visite (clé sur la table temps)
nb_chirurgies	               integer	      Nombre de chirurgies antérieures
nb_visited_urgences	           integer	      Nombre de passages précédents aux urgences
nb_admissions	               integer	      Nombre d’admissions hospitalières antérieures
 