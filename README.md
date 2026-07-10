Credit Card Fraud Detection

📌 Overview

This project builds a machine learning pipeline to detect fraudulent credit card transactions. It covers exploratory data analysis of a highly imbalanced dataset, feature scaling, and training/evaluating two classification models — Logistic Regression and Random Forest — using metrics suited to imbalanced classification (precision, recall, confusion matrix, ROC-AUC).

🗂️ Dataset


File: creditcard.csv
Loaded via: Google Colab file upload (google.colab.files.upload())
Target column: Class (0 = legitimate transaction, 1 = fraudulent transaction)
Features: Time, Amount, and anonymized PCA-transformed features (V1–V28, typical of the well-known Kaggle credit card fraud dataset)


🛠️ Tools & Libraries


Language: Python (Jupyter / Google Colab)
Data handling: pandas, numpy
Visualization: matplotlib, seaborn
Machine Learning: scikit-learn

StandardScaler for feature scaling
LogisticRegression
RandomForestClassifier
train_test_split (stratified)
accuracy_score, classification_report, confusion_matrix, roc_auc_score, roc_curve





📊 Project Workflow


Data Loading – Import creditcard.csv into a pandas DataFrame
Initial Inspection – Shape, info, and null-value check
Class Balance Check

Value counts and percentage split of Class (fraud vs. non-fraud)
Count plot of fraud vs. non-fraud transactions



Exploratory Data Analysis

Transaction amount distribution (histogram)
Correlation heatmap across all features



Feature Scaling – Standardize Amount and Time using StandardScaler (other features are already PCA-transformed)
Train/Test Split – 80/20 stratified split (random_state=42) to preserve the fraud/non-fraud ratio
Model Training & Evaluation

Logistic Regression (max_iter=1000) – classification report, accuracy, confusion matrix
Random Forest (n_estimators=100, random_state=42) – classification report, accuracy, confusion matrix



ROC-AUC Analysis – ROC-AUC score and ROC curve for the Random Forest model's predicted probabilities
Model Comparison – Accuracy comparison table and bar chart across both models


🔍 Results

(Fill in with your actual run output)

ModelAccuracyROC-AUCLogistic Regression[add score]—Random Forest[add score][add score]

Note: Because fraud cases are a very small percentage of total transactions, accuracy alone can be misleading — pay close attention to precision, recall, and F1-score for the fraud class (1) in the classification report, not just overall accuracy.

Best performing model: [add which model performed better and why]

📁 Repository Structure

├── creditcard_Fraud_Detection.ipynb   # Main notebook (EDA + preprocessing + modeling)
├── creditcard.csv                     # Dataset (if included in repo)
└── README.md                          # Project documentation

🚀 How to Run


Clone the repository


bash   git clone https://github.com/prince7046/Fraud-Detection.git
   cd Fraud-Detection


Install dependencies


bash   pip install pandas numpy matplotlib seaborn scikit-learn


Open and run the notebook


bash   jupyter notebook creditcard_Fraud_Detection.ipynb


If running in Colab, upload creditcard.csv when prompted by the file upload cell.


✅ Conclusion

This project demonstrates a practical approach to detecting fraudulent transactions in a highly imbalanced dataset. By comparing a linear model (Logistic Regression) against an ensemble model (Random Forest) and evaluating with ROC-AUC alongside standard classification metrics, it identifies which approach better balances catching fraud (recall) against minimizing false alarms (precision).

👤 Author

Prince
🔗 [GitHub Profile](https://github.com/prince7046)

📄 License

This project is licensed under the MIT License.
