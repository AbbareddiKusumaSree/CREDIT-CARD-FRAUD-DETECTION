Credit Card Fraud Detection
This project detects fraudulent credit card transactions using **Machine Learning models**: Logistic Regression, Random Forest, and XGBoost. It includes data preprocessing, model training, evaluation (ROC-AUC, confusion matrix), and saving models for deployment.

Dataset used: [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud).

 1. Problem Statement
Credit card fraud detection is challenging due to:
- Highly imbalanced dataset (fraudulent transactions are rare).
- Need for high accuracy and low false positives.
This project builds and compares models to predict fraud effectively.

 2. Dataset
- **Features**:
  - V1–V28: PCA-transformed numerical features
  - Time: Time elapsed between transactions
  - Amount: Transaction amount
- **Target**: Class → 0 (Non-Fraud), 1 (Fraud)
- **Source**: [Kaggle - Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
 Download `creditcard.csv` and place it inside the `data/` folder.

 3. Project Structure
credit-card-fraud-detection/
├── data/ # Dataset (creditcard.csv)
├── models/ # Saved models (.pkl)
├── scripts/ # Preprocessing, training, evaluation
├── outputs/ # ROC curve and evaluation results
├── main.py # Pipeline entry point
├── requirements.txt # Dependencies
├── README.md # Project documentation
└── .gitignore # Files to ignore in Git

Outputs:

Trained models saved in models/

ROC curve saved in outputs/roc_curve.png
4. Scripts Overview
preprocess.py → Loads and scales data, saves scaler.

train.py → Trains Logistic Regression, Random Forest, and XGBoost models.

evaluate.py → Evaluates models (Accuracy, Confusion Matrix, Classification Report, ROC-AUC) and generates ROC curve.

5. Results
Logistic Regression → Baseline model.

Random Forest → Better accuracy and robustness.

XGBoost → Typically the best ROC-AUC score.

6. Technologies Used
Python 3
pandas, scikit-learn, xgboost, matplotlib, joblib
