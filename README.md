# 🩺 Diabetic Cases Prediction System
> **A machine learning approach to early diabetes detection focusing on high-recall clinical screening.**

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-blue.svg)
![Visualisation](https://img.shields.io/badge/Data%20Viz-Seaborn%20%7C%20Matplotlib-applegreen.svg)
![Imbalanced-Learn](https://img.shields.io/badge/Handling%20Imbalance-SMOTE-red.svg)

## 🌟 Project Overview
This project addresses the challenge of identifying chronic disease risks using a dataset of clinical health indicators. The core objective is to develop a predictive model that acts as an effective screening tool, prioritizing the identification of at-risk individuals to facilitate early medical intervention.

---

## 🛠️ Technical Methodology

### 1. Data Exploration & Visualization
Using **Seaborn** and **Matplotlib**, a comprehensive EDA was conducted:
* **BMI Analysis:** Identified a median BMI of 27 with significant outliers beyond 40.
* **Risk Factors:** Established strong correlations between older age groups, higher BMI, and diabetic prevalence.
* **Feature Correlation:** Identified BMI, General Health, and High Blood Pressure as the top predictors.

### 2. Data Preparation & Cleaning
* **Duplicate Removal:** Streamlined the dataset for better model integrity.
* **Outlier Handling:** Used the IQR method to filter extreme BMI values.
* **Feature Engineering:** Converted numerical features (Age, Income, Education, Sex, GenHlth) into meaningful categorical ranges and applied **One-Hot Encoding**.
* **Addressing Imbalance:** Implemented **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the target classes, ensuring the model identifies diabetic cases effectively.

### 3. Machine Learning Implementation
Models built and compared using **Scikit-Learn**:
* Logistic Regression
* Decision Tree
* Random Forest
* **AdaBoost (Selected Model)**
* Gradient Boosting
* Linear SVC

---

## 📊 Model Selection & Business Logic
In medical screening, **Recall** is the most critical metric because the cost of a "False Negative" (missing a sick patient) is far higher than a "False Positive."

| Metric (After SMOTE) | AdaBoost | Gradient Boosting |
| :--- | :--- | :--- |
| **Recall (Diabetic Class)** | **0.65** | 0.29 |
| **Decision** | **Selected** | Rejected |

**Conclusion:** Despite a lower overall accuracy, **AdaBoost** was selected because it successfully identifies **65%** of diabetic cases, whereas Gradient Boosting missed **71%** of cases.

---

## 📊 Key Findings & Model Selection
Based on the project requirements for early detection and providing health recommendations, **AdaBoost** was selected as the superior model for this business scenario:

| Metric | AdaBoost | Gradient Boosting |
| :--- | :--- | :--- |
| **Recall (Diabetic Class)** | **0.65** | 0.29 |
| **Selection Logic** | Identified 65% of cases | Missed 71% of cases |

> **Clinical Justification:** In medical screening, the cost of a False Negative (missing a sick person) is much higher than a False Positive. AdaBoost's significantly higher recall makes it the only viable choice for a screening tool in this context.

---

## 🚀 Getting Started

### 1. Prerequisites
* Python 3.8+
* Jupyter Notebook

### 2. Installation & Setup
```bash
# Clone the repository
git clone [https://github.com/yourusername/chronic-disease-prediction.git](https://github.com/yourusername/chronic-disease-prediction.git)
cd chronic-disease-prediction

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn

```
---

### 3. Running the Analysis
To replicate the results, follow these steps within your environment:

1.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
2.  **Open the Project:** Locate and open `244423Q_IT2313_Assignment.ipynb`.
3.  **Process Data:** Run all cells to process diabetes.csv, generate visualizations, and evaluate model performance.

---

## 📂 Project Roadmap
The analysis follows a structured machine learning pipeline:
* **Import & Exploration:** Loading clinical health indicator data, understanding data and verify missing data.
* **EDA:** Visualization of BMI distributions, health trends, and correlation matrices using **MatplotLib** and **Seaborn**.
* **Preparation:** Outlier filtering and categorical encoding.
* **Training/SMOTE:** Training initial models and re-training with balanced data.
* **Model Comparison / Tuning:** Evaluating performance via Confusion Matrix and F1/Recall score to determine the best model for medical screening.
