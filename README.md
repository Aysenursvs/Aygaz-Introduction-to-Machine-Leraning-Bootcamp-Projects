# 🛡️ Online Payment Fraud Detection
### Supervised vs. Unsupervised Learning Approach

This repository contains two machine learning projects developed during the **Aygaz Machine Learning Bootcamp**. The primary objective was to detect fraudulent transactions in online payments by implementing and comparing **Supervised** and **Unsupervised** learning algorithms.


## 📊 Dataset Overview
The project utilizes a large-scale dataset sourced from Kaggle, simulating mobile money transactions.

* **Source:** [Online Payments Fraud Detection Dataset](https://www.kaggle.com/rupakroy/online-payments-fraud-detection-dataset)
* **Data Points:** ~6.3 Million entries
* **Features:** `step`, `type`, `amount`, `nameOrig`, `oldbalanceOrg`, `newbalanceOrig`, `nameDest`, `oldbalanceDest`, `newbalanceDest`, `isFraud`, `isFlaggedFraud`
* **Target:** `isFraud` (0 = Legitimate, 1 = Fraudulent)

> **Note:** The dataset is highly imbalanced, which is a common characteristic of real-world security logs and fraud data.

## 🛠️ Methodology
The project pipeline includes Exploratory Data Analysis (EDA), Preprocessing, Algorithm Selection, and Hyperparameter Optimization.

### 1. Supervised Learning Approach
* **Algorithm:** K-Nearest Neighbors (K-Neighbors Classifier)
* **Goal:** Classify transactions as "Fraud" or "Not Fraud" based on labeled training data.
* **Notebook:** [View on Kaggle](https://www.kaggle.com/code/ayysenurrr/online-fraud-detection-supervised)

### 2. Unsupervised Learning Approach
* **Algorithm:** K-Means Clustering
* **Goal:** Detect patterns and group transactions to identify anomalies without using the `isFraud` label initially.
* **Notebook:** [View on Kaggle](https://www.kaggle.com/code/ayysenurrr/online-fraud-detection-unsupervised)

## 📈 Results & Analysis

### Supervised Model (K-NN) Performance
The supervised model achieved high accuracy, but the focus was on the Confusion Matrix to understand False Positives and False Negatives.

* **Accuracy Score:** `0.9994`

**Confusion Matrix:**
| | Predicted: Not Fraud (0) | Predicted: Fraud (1) |
| :--- | :---: | :---: |
| **Actual: Not Fraud (0)** | **1,906,054** (TN) | 297 (FP) |
| **Actual: Fraud (1)** | 788 (FN) | **1,647** (TP) |

* **Insight:** The model is extremely successful in identifying legitimate transactions (True Negatives). However, due to the class imbalance, there are missed fraud cases (False Negatives: 788). In a real-world security scenario, reducing False Negatives is crucial to prevent financial loss.

### Unsupervised Model (K-Means) Performance
* **Evaluation Metric:** Silhouette Score
* **Score:** `0.4`
* **Insight:** The model successfully grouped data points with a moderate separation score. However, without labels, strictly separating "Fraud" from "Normal" behavior in such a dense dataset proved more challenging than the supervised approach.

## 🏆 Conclusion: Supervised vs. Unsupervised
Comparing both approaches on this specific dataset:

1.  **Supervised Learning (K-NN)** outperformed K-Means significantly. Since the dataset is labeled (`isFraud`), the algorithm could explicitly learn the patterns of fraudulent behavior.
2.  **Unsupervised Learning** is valuable for discovering unknown attack patterns (Zero-Day), but for this specific task where definitions of fraud are known, classification yielded better results.

---
*Maintained by Ayşenur Sivaslıgil*
