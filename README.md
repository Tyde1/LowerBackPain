Back Pain Classification 
This model compares XGBoost with Logistic Regression for back pain classification. The models were fine tuned and evaluated using 5-fold cross validation. Results were examined using confusion matricies. 

Dataset
The dataset used comes from Kaggle's Lower Back Pain Symptoms Dataset. It contains 310 observations (210 - Abnormal, 100 - Normal) and 12 numerical predictors, including pelvic incidence, pelvic tilt, lumbar lordosis angle, and sacral slope. The model uses all 12 features in the dataset and classifies patient spine records as either Abnormal or Normal.

Methods

Preprocessing 
- Remove the extra 'notes column 
- Included mean imputation pipeline for numerical features
- Standardized features for Logistic Regression

Training and Evaluation
- Created a stratified 80/20 train/test split
- Tuned Logistic Regression and XGBoost hyperparameters with 'GridSearchCV' using stratified five-fold cross-validation
- Evaluated select models on the held out test set using accuracy, classification reports, ROC-AUC, and confusion matricies.

Results
Model	Mean five-fold cross-validation accuracy
XGBoost	83.85%
Logistic Regression	84.26%

Logistic Regression had a higher mean crosos-validation accuracywhat a
How to Run

Limitations

Next Steps