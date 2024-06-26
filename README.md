mPBPK/mTPA project
We provide a framework for model-based assessment of target engagement response of antibody candidates by integrating a mPBPK with a tree-based machine learning model. We generate a large number of synthetic drug-target candidate pairs with varying properties using the mPBPK/TMDD model. These synthetic drug and target properties are categorized into optimal or non-optimal spaces according to a desired target occupancy percentage. An interpretable decision-tree based algorithm was applied for high-throughput screening of synthetic drug-target properties such as binding affinity, baseline concentration, target half-life, dose, dosing scheme, and antibody charge to identify the combination of compound properties that are most likely to demonstrate the desired target engagement response. Publication Link

Jupyter notebooks
mTPA_local (Ts).ipynb : Binary Decision tree-based ML model based on PK data for soluble receptors.
mTPA_local (Tm).ipynb : Binary Decision tree-based ML model based on PK data for membrane-bound receptors.
mTPA_local (3-label).ipynb : Three-label Decision tree-based ML classifier based on PK data.
in silico PK data generation
Included mPBPK model scripts to generate PK data based on in silico candidate properties. More information on the mPBPK simulations can be found in the folder - in silico PK data generation.

Dependencies
Package dependencies in Python:
Pandas, sklearn, numpy, matplotlib, joblib, pickle, imblearn, scipy

Instructions for Use
Input
Example files to run Jupyter notebooks:
a. In Silico candidates
~ Call "target_candLOG10000.csv" example file as input to ML model.
b. In Silico PK data
~ Call an PK endpoint (TO%) example file. Each file is named as follows: PK_endpoint_(dose)(scheme)(species)_(receptor)10000.csv
~ From PK endpoints, use column "TOplast" as the ML criterion. TOplast: TO% calculated at Cmin in plasma.

Note: To use your own data to run these codes. The ML input data format must same as example input files. Criterion for ML output can be TO% calculated at any PK endpoint (Cmin, Cmax etc.).

Output
a. ML model output includes ~ Trained decision Tree Model
~ Decision Tree Plot
~ Confusion Matrix
~ Classification Metric
~ Scatter and Kernel Density plots
~ ROC curve
~ Predicted (.csv) file with optimal and non-optimal candidates
Versions
These source codes were written in Python 3 version.
