# Synthetic Data Generation For Healthcare

Dataset link: [(https://physionet.org/content/mimiciii/1.4/)]

Read docs for schema. This model uses the following tables cleaned with the cleaners (see cleaners/):

ADMISSIONS
DIAGNOSES_ICD
ICUSTAYS
LABEVENTS
PATIENTS

LABITEMS for reference

cleaners/ - initial cleaning of each table (uses csv.gz data from MIMIC-III) (not included here for privacy reasons)

preprocessing.ipynb - preprocessing of all data, applying log transforms as necessary on selection of lab events
cvae_sp.ipynb - cVAE using standard KL divergence
cvae_wasserstein_sp.ipynb - cVAE using sliced wasserstein distance instead of KL divergence

cvae_outputs/ - contains scalers and weights for models for quick reloading


*I have tried including detailed comments for good comprehension of the notebooks as you go through them.*

Data and Legal Limitations
•	The model is trained on MIMIC-III, which is credentialed data. The trained weights cannot be openly distributed, limiting the system’s shareability.
•	The system generates de-identified synthetic data but has not been formally evaluated for re-identification risk or clinical safety.

