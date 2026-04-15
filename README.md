# Team Endurance: Genetic Disorder Multi-Class Classifier

## Problem Statement
Design and develop an Al/ML-driven predictive system that analyzes heterogeneous pediatric medical data to accurately identifying both the type of genetic disorder and its corresponding subclass. Participants are provided with structured clinical and demographic features that may contain missing values, noise, and class imbalance, reflecting real-world healthcare challenges. The objective is to build a robust and generalized model that can effectively preprocess incomplete data, extract meaningful patterns, and deliver reliable multi-class predictions. Solutions should emphasize not only predictive performance but also interpretability, scalability, and the ability to handle data variability, encouraging innovative approaches such as feature engineering, ensemble methods, or advanced learning techniques to improve early detection and support informed medical decision-making.

## Team Members
- Vardaan Grover (Team Lead)
- Shubham Dogra
- Vansh Saini
- Aastha Raj Saini

## What's Done:

- **Data Inspection** — loaded train (22083×45) and test (9465×43), identified 3 disorders, 9 subclasses, 9 unique combinations
- **Data Cleaning** — recovered rows where disorder was missing but subclass existed, dropped unrecoverable rows, created combined 9-class target, dropped 6 identifier columns
- **Null Handling** — added missing_count feature, median-filled numerics, "Missing"-filled categoricals, manually defined num_cols and cat_cols lists
- **Encoding** — label-encoded all categoricals + target, built X_train, X_test, y
- **EDA** — target distribution (both levels), missing value histogram, symptom heatmap by subclass, test results heatmap by subclass

## Not done yet:

- **Feature Engineering** — parent age gap/sum, symptom/test aggregates, blood ratio
- **Model Training** — LightGBM with 5-fold StratifiedKFold, then XGBoost/CatBoost
- **Ensemble** — weighted probability averaging across models
- **Submission** — decode predictions back to disorder + subclass columns
