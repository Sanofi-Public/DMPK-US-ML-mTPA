# mPBPK/mTPA project
We provide a framework for model-based assessment of target engagement response of antibody candidates by integrating a mPBPK with a tree-based machine learning model. We generate a large number of synthetic drug-target candidate pairs with varying properties using the mPBPK/TMDD model. These synthetic drug and target properties are categorized into optimal or non-optimal spaces according to a desired target occupancy percentage. An interpretable decision-tree based algorithm was applied for high-throughput screening of synthetic  drug-target properties such as binding affinity, baseline concentration, target half-life, dose, dosing scheme, and antibody charge to identify the combination of compound properties that are most likely to demonstrate the desired target engagement response. (https://link.springer.com/article/10.1007/s10928-023-09899-z)

# Jupyter notebooks
1. mTPA_local (Ts).ipynb : Binary Decision tree-based ML model based on PK data for soluble receptors. <br />
2. mTPA_local (Tm).ipynb : Binary Decision tree-based ML model based on PK data for membrane-bound receptors. <br />
3. mTPA_local (3-label).ipynb : Three-label Decision tree-based ML classifier based on PK data. <br /> 

# in silico PK data generation
Included mPBPK model scripts to generate PK data based on in silico candidate properties. More information on the mPBPK simulations can be found in the folder - in silico PK data generation. <br />

# Dependencies 
Package dependencies in Python: <br />
Pandas, sklearn, numpy, matplotlib, joblib, pickle, imblearn, scipy <br />

# Instructions for Use
1. Input <br />
Example files to run Jupyter notebooks: <br />

a. In Silico candidates <br />
~ Call "target_candLOG10000.csv" example file as input to ML model. <br />
b. In Silico PK data    <br />
~ Call an PK endpoint (TO%) example file. Each file is named as follows: PK_endpoint_(dose)_(scheme)_(species)_(receptor)10000.csv <br />
~ From PK endpoints, use column "TOplast" as the ML criterion. TOplast: TO% calculated at Cmin in plasma. <br />

Note: To use your own data to run these codes. The ML input data format must same as example input files. Criterion for ML output can be TO% calculated at any PK endpoint (Cmin, Cmax etc.).  <br />

2. Output <br />
a. ML model output includes 
~ Trained decision Tree Model <br />
~ Decision Tree Plot <br />
~ Confusion Matrix <br />
~ Classification Metric <br />
~ Scatter and Kernel Density plots <br />
~ ROC curve <br />
~ Predicted (.csv) file with optimal and non-optimal candidates <br /> 

# Versions
These source codes were written in Python 3 version. <br />
