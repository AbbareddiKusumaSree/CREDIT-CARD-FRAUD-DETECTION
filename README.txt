Credit Card Fraud Detection

This project focuses on identifying fraudulent credit card transactions using powerful Machine Learning models such as Logistic Regression, Random Forest, and XGBoost. The system includes end-to-end steps like data preprocessing, model training, performance evaluation (ROC-AUC, confusion matrix), and saving models for real-world deployment.

Dataset used: Kaggle Credit Card Fraud Detection
(https://www.kaggle.com/mlg-ulb/creditcardfraud
)

1. Problem Statement

Detecting credit card fraud is difficult because:

The dataset is highly imbalanced, with very few fraud cases.

The system must achieve high accuracy while keeping false positives low.

This project builds, compares, and evaluates multiple ML models to reliably predict fraudulent transactions.

2. Dataset

Features:

V1–V28: PCA-transformed numerical components

Time: Time elapsed between transactions

Amount: Transaction amount

Target Variable:

0 → Genuine Transaction

1 → Fraudulent Transaction

Source: Kaggle Credit Card Fraud Detection
After downloading creditcard.csv, place it inside the data/ folder.

3. Project Structure
credit-card-fraud-detection/
├── data/          # Dataset (creditcard.csv)
├── models/        # Saved models (.pkl)
├── scripts/       # Preprocessing, training, evaluation
├── outputs/       # ROC curve, performance results
├── main.py        # Main pipeline script
├── requirements.txt
├── README.md
└── .gitignore


Outputs:

Trained models → models/

ROC Curve → outputs/roc_curve.png

4. Scripts Overview

preprocess.py → Loads data, scales features, saves scaler.

train.py → Trains Logistic Regression, Random Forest, and XGBoost models.

evaluate.py → Generates accuracy, confusion matrix, classification report, ROC-AUC, and ROC curve visualization.

5. Results

Logistic Regression: Baseline performance.

Random Forest: Improved accuracy and stability.

XGBoost: Highest ROC-AUC score; best-performing model overall.

6. Technologies Used

Python 3

pandas

scikit-learn

xgboost

matplotlib

joblib
