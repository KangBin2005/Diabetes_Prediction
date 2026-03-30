# 🩺 Chronic Disease Prediction System
> **A machine learning approach to early diabetes detection focusing on high-recall clinical screening.**

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-blue.svg)
![Visualisation](https://img.shields.io/badge/Data%20Viz-Seaborn%20%7C%20Matplotlib-applegreen.svg)
![Imbalanced-Learn](https://img.shields.io/badge/Handling%20Imbalance-SMOTE-red.svg)

## 🌟 Project Overview
This project addresses the challenge of identifying chronic disease risks using a dataset of clinical health indicators. The core objective is to develop a predictive model that acts as an effective screening tool, prioritizing the identification of at-risk individuals to facilitate early medical intervention.

---

## 🛠️ Technical Methodology
* **Data Processing:** Exploratory Data Analysis (EDA) and rigorous data cleaning of health indicator variables.
* **Handling Class Imbalance:** Applied **SMOTE** (Synthetic Minority Over-sampling Technique) to ensure the model could accurately learn from the minority class of diabetic cases.
* **Algorithms Used:** Compared **AdaBoost** and **Gradient Boosting** ensemble methods.
* **Optimization Strategy:** Focused on maximizing **Recall** to minimize False Negatives, which are critical in a medical context.

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
3.  **Execute Workflow:** Run all cells to view the EDA visualizations, model training, and final evaluation metrics.

---

## 📂 Project Roadmap
The analysis follows a structured machine learning pipeline:

* **Import & Exploration:** Loading clinical health indicator data and checking distributions using **Seaborn** and **Matplotlib**.
* **Preparation:** Data cleaning and implementing **SMOTE** to address class imbalance between diabetic and non-diabetic cases.
* **Training:** Executing supervised learning classification models.
* **Comparison:** Evaluating models via Confusion Matrix and **Recall** scores to determine the best fit for medical screening.
