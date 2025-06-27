AI Job Salary & Role Prediction – Project Summary¶
Dataset: ai_job_dataset.csv Samples: 15,000 rows • Features: 19 columns Language: Python Objectives:

Predict AI job salaries based on features
Classify job types (e.g. remote/hybrid/on-site)
Analyze job requirements using NLP
Step-by-Step Workflow Overview¶
STEP 1 – Dataset Overview & Cleaning
Successfully loaded a clean dataset with 15,000 rows and 19 columns.
No missing values detected.
Converted posting_date and application_deadline to datetime format.
Normalized all categorical fields (lowercase + whitespace stripping).

STEP 2 – Feature Preparation
Dropped irrelevant fields such as job_id, company_name, posting_date.
Encoded categorical columns using LabelEncoder.
Target variable selected: salary_usd.
Final shape for modeling
Feature matrix (X): 14 columns
Target vector (y): salary_usd

STEP 3 – Exploratory Data Analysis (EDA)¶
Created powerful visualizations to identify patterns and trends:

Salary distribution (histogram)
Salary comparison by:

Experience level
Employment type
Remote ratio
Company size
Top 10 most frequent industries

Key Insights:

Executives earn significantly more than juniors.

Remote roles have broader salary ranges.
Large companies offer higher average salaries than small ones.

STEP 4 – Feature Engineering¶
All categorical features encoded numerically.
Used StandardScaler for feature normalization.
Prepared datasets for machine learning (X, y split).

STEP 5 – Salary Prediction Using Regression
Trained 3 different models to predict salary_usd:

Linear Regression:

Random Forest Regressor:

XGBoost Regressor:

Conclusion: XGBoost is the most accurate model for salary prediction in this dataset.

STEP 6 – Visual Model Comparison¶
Plotted model performance metrics:

R² Score
MAE (Mean Absolute Error)
RMSE (Root Mean Squared Error)
XGBoost clearly outperformed both Linear Regression and Random Forest in all metrics.

STEP 7 – Classification: Predicting Remote Work Type
Target: remote_ratio (0 = On-site, 50 = Hybrid, 100 = Remote)

Models Used:

Logistic Regression
Random Forest Classifier

Result: Both models only achieved ~33% accuracy. This indicates that the current features are not strong predictors for remote status.

STEP 8 – NLP Analysis of required_skills
Tokenized skills using CountVectorizer (split by comma).
Counted and visualized the top 20 most frequent skills.

Top Skills Identified:

Python, SQL, TensorFlow, Docker, AWS, Linux, Kubernetes, NLP

This step sets the foundation for building a skill-based job recommender system.
