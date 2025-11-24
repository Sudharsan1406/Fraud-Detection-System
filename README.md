# Fraud-Detection-System
Self Project
Credit Card Fraud Detection using Machine Learning
1. Project Overview

This project focuses on detecting fraudulent credit card transactions in a highly imbalanced dataset. The goal is to build a reliable machine learning model that minimizes false negatives while keeping false positives under control.

2. Key Objectives

Analyze the data distribution and handle severe class imbalance

Build a preprocessing pipeline with feature scaling and sampling

Train and compare multiple ML models

Select the most practical model for real-world fraud detection

Evaluate performance using precision, recall, F1-score, and ROC-AUC

3. Dataset Details

Total samples: 284,807

Fraud cases: 492

Fraud ratio: 0.172%

Features: Time, Amount, 28 anonymized PCA features

4. Preprocessing Steps

Robust scaling for Amount and Time

Outlier handling

Stratified train-test split

Downsampling + all-fraud retention for tuning

Threshold tuning for final decision boundary

5. Models Trained

Logistic Regression

KNN

Random Forest

XGBoost (Tuned)

6. Results
Model	Precision (Fraud)	Recall (Fraud)	F1	ROC-AUC
Logistic Regression	0.88	0.66	0.76	0.95
Random Forest (Tuned)	0.49	0.86	0.62	0.98
KNN	0.83	0.10	0.18	0.60
XGBoost (Final)	0.92	0.84	0.88	0.94
7. Why XGBoost Was Selected

XGBoost achieved the strongest balance between precision and recall, reducing false alarms while still catching the majority of fraud cases. Its performance and stability make it suitable for production-level fraud monitoring systems.

8. Final Conclusion

This project demonstrates the importance of selecting model metrics aligned with business risks rather than accuracy alone. The final XGBoost model provides reliable and practical fraud detection. Future improvements may include deployment via FastAPI, model drift handling, and real-time inference.

9. Repository Structure
│── data/
│── notebooks/
│── models/
│── Fraud_Detection.ipynb
│── README.md

10. Technologies

Python, Pandas, NumPy, Scikit-Learn, XGBoost, Matplotlib, Seaborn
