# Loan-default-prediction
Predicting consumer loan default using machine learning (logistic regression, random forest), with class imbalance handling
# Objective
To classify whether a loan will default based on borrower attributes such as income, loan amount, FICO score, debt-to-income ratio, and more.
# Machine Learning models which i used
- Logistic Regression
- Random Forest Classifier
# Other Models
- Train_test_split-- used for model validation
- StandardScaler (from sklearn.preprocessing): Used to scale numeric features to have zero mean and unit variance. This was important because the logistic regression model initially failed to converge using the default max_iter value. Scaling the features ensured faster and stable convergence of the optimization algorithm.
**Libraries**
- pandas – data cleaning, feature engineering
- numpy – numerical operations
- matplotlib – data visualization
- scikit-learn – machine learning models and evaluation metrics
- imblearn – oversampling with SMOTE to handle class imbalance
- statsmodels – statistical regression modeling
  # Challenges faced while doing the project
-Handled missing values and filtered rows with relevant loan status
-Encoded categorical variables using pd.get_dummies()
-Created binary classification target: default (1 = Charged Off, 0 = Fully Paid)
-Applied StandardScaler to scale down numeric observations, which helped resolve convergence issues during logistic regression
# Outcome
-Logistic regression model improved with standardized features and class weighting
=Random forest achieved high accuracy but initially failed to identify defaults until rebalanced with class_weight='balanced'
-ROC AUC improved after addressing class imbalance
-Feature importance identified FICO score, DTI, and loan amount as top predictors
