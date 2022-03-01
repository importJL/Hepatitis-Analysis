# Hepatitis Analysis
A repository for analysis of patient-drawn blood samples for differentiating patients with various liver diseases ("acute" hepatitis C, fibrosis, cirrhosis).  Data science and machine learning tools used involve `pandas`, `numpy`, `scikit-learn`, and `xgboost` modules.  As samples are heavily biased on patients with normal liver conditions, incorporation of `imblearn` is used to offset these changes using various balance-attenuating algorithms.

You may check with in the browser `Hepatitis_C.ipynb` file or clone this repository: `git clone https://github.com/jedi3nigma/Hepatitis-Analysis/`

Feel free send pull request for further add-ons.

### Outcomes
- Generally, due to imbalances in sample proprotion between different categories of liver disease, accuracy metrics demonstrated biased performance for those that had relatively more training samples provided
- Incorporating sampling balance algorithm to generate and equalize the proportion of samples between categories generally provided a remarkable increase in metric scores across categories
- XGBoost (with sample balancing) demonstrated highest overall accuracy metrics (Precision: 0.94, recall: 0.71, F1: 0.81), specifically on determining Hepatitis among other classifications

### Future improvements
- Utilizing sample balancing algorithms (under/oversampling) does involve intrinsic data distribution assumptions and uncertainty incorporated from their sampling models (nearest neighbours, SVM, etc).  Extracting more data samples would provide an alternative to utilizing sampling techniques.
- PCA was not incorporated though from external research, a subset of clinicially deterministic features were used as primary features used in the models.  Selecting features based on judgement and model-specific methods (such as PCA/LDA) could help to provide a more comprehensive overview of key contributing factors to determiniong hepatitis from other categories

----
### To run notebook for your own use, install Jupyter notebook using Anaconda.  You can download Anaconda at https://www.anaconda.com/products/individual.
