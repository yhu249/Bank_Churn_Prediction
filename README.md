# Bank_Churn_Prediction

An end-to-end machine learning project for predicting credit card customer churn using exploratory data analysis, feature preprocessing, class balancing, model comparison, and hyperparameter tuning.

## Project Overview

Customer churn is a major concern for financial institutions because retaining existing customers is often more cost-effective than acquiring new ones.

This project analyzes customer demographics, account information, and transaction behavior to predict whether a credit card customer will remain active or leave the bank.

The dataset contains **10,127 customer records** and **23 original variables**, including:

* 8,500 existing customers
* 1,627 attrited customers

Because the target variable is imbalanced, SMOTE is applied to the training data before model training.

## Project Objectives

The main objectives of this project are to:

* Explore customer demographic and transaction patterns
* Identify factors associated with customer churn
* Preprocess numerical and categorical variables
* Address class imbalance using SMOTE
* Compare multiple machine learning models
* Improve model performance through hyperparameter tuning
* Evaluate the model's ability to identify customers likely to churn

## Workflow

1. Load and inspect the dataset
2. Check data types and missing values
3. Remove irrelevant or redundant columns
4. Conduct exploratory data analysis
5. Analyze numerical and categorical features
6. Encode categorical variables
7. Split the data into training and test sets
8. Apply SMOTE to the training data
9. Train multiple classification models
10. Tune model hyperparameters
11. Evaluate model performance

## Models

The following classification models are compared:

* Random Forest Classifier
* Support Vector Machine
* Gradient Boosting Classifier

Random Forest and Gradient Boosting perform better than the Support Vector Machine in the analysis.

After model tuning, the strongest models achieve approximately:

| Metric               | Result |
| -------------------- | -----: |
| Accuracy             |    95% |
| Churn-class recall   |  84.2% |
| Churn-class F1-score |   0.85 |

Recall for attrited customers is particularly important because a false negative represents a customer who is likely to leave but is not identified by the model.

## Key Findings

The exploratory analysis suggests that:

* Customers with higher transaction counts are more likely to remain active.
* Customers with higher total transaction amounts are less likely to churn.
* Customers with longer periods of inactivity show a higher likelihood of churn.
* Transaction behavior is more informative than many demographic variables.
* Customer age and several demographic features have relatively weak relationships with churn.
* Class imbalance must be considered when training and evaluating the models.

## Repository Structure

```text
bank-churn-prediction/
├── README.md
├── Bank_Churn_Prediction.ipynb
├── Bank_Churn_Prediction.html
├── requirements.txt
├── .gitignore
└── data/
    └── BankChurners.csv
```

## File Descriptions

* `Bank_Churn_Prediction.ipynb`: complete exploratory analysis, preprocessing, modeling, tuning, and evaluation
* `Bank_Churn_Prediction.html`: rendered version of the notebook for quick viewing
* `data/BankChurners.csv`: dataset used in the project
* `requirements.txt`: Python packages required to run the notebook
* `.gitignore`: files and folders excluded from Git tracking

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/bank-churn-prediction.git
cd bank-churn-prediction
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment on macOS or Linux:

```bash
source .venv/bin/activate
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Launch the notebook:

```bash
jupyter notebook Bank_Churn_Prediction.ipynb
```

## Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Plotly
* Scikit-learn
* Imbalanced-learn
* SciPy
* Jupyter Notebook

## Evaluation Metrics

The models are evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix

Since the dataset is imbalanced, accuracy alone is not sufficient. Recall and F1-score for the attrited-customer class are also considered when comparing models.

## Notes

* SMOTE is applied only to the training data to reduce the risk of data leakage.
* `Attrited Customer` is treated as the positive churn class.
* The HTML file allows the complete analysis to be viewed without running the notebook.
* Replace `YOUR-USERNAME` with your actual GitHub username in the clone command.

## Future Improvements

Possible future improvements include:

* Add ROC-AUC and precision-recall curve comparisons
* Use stratified cross-validation
* Add feature importance analysis
* Add SHAP explanations
* Build a reusable Scikit-learn pipeline
* Save the final trained model
* Develop a Streamlit application for churn prediction

## Author

**Holly Hu**

Master of Science in Data Science, Brown University
