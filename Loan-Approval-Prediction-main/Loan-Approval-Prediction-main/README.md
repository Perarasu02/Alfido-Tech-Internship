# Loan-Approval-Prediction
📁 Task 2 — Internship Project

This project focuses on analyzing a Loan Prediction Dataset and building a Machine Learning model to classify whether a loan application should be approved or not.

🚀 Project Overview

Banks receive thousands of loan applications every day.
Manual screening takes time and introduces inconsistency.
This project builds an automated system to:

✔ Clean & preprocess loan applicant data
✔ Perform exploratory data analysis (EDA)
✔ Visualize insights
✔ Train ML models to predict loan approval
✔ Evaluate model performance

The goal: Improve decision-making using data-driven predictions.

📊 Dataset Information

The dataset used: loan_prediction.csv

Common columns include:
Gender
Married
Dependents
Education
Self_Employed
ApplicantIncome
CoapplicantIncome
LoanAmount
Loan_Amount_Term
Credit_History
Property_Area
Loan_Status (Target variable)

🔧 Steps Performed
1. Data Loading
Load the CSV file using pandas.

2. Data Cleaning
Handling missing values
Converting categorical variables
Removing duplicates
Handling outliers

3. Exploratory Data Analysis (EDA)
Visualizations using:
Matplotlib
Seaborn

EDA includes:

📌 Distribution of income
📌 Loan amount analysis
📌 Relationship between credit history and approval
📌 Gender vs approval rates
📌 Education role in approval

4. Data Preprocessing
Label encoding
Scaling numerical features
Train-test split

5. Model Building
Machine learning algorithms tested:
Logistic Regression
Decision Tree
Random Forest
Support Vector Machine
Best model chosen based on accuracy.

6. Model Evaluation
Metrics used:
Accuracy score
Confusion matrix
Classification report

🧠 Final Model

Random Forest Classifier (or whichever performs best) achieves high accuracy and generalizes well on unseen test data.
📈 Project Outcome
This project demonstrates:

✔ End-to-end ML pipeline creation
✔ Business-level interpretation of results
✔ Ability to build predictive models for financial applications

📚 Technologies Used
Python
Google Colab
Panda
NumPy
Scikit-learn
Matplotlib
Seaborn

📦 Repository Structure
|-- loan_prediction.ipynb       # Complete code
|-- loan_prediction.csv         # Dataset
|-- README.md                   # Documentation
|-- images/                     # Plots & Visualizations
