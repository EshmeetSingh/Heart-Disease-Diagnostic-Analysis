# ❤️ Heart Disease Diagnostic Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Complete-green)

## 📄 Overview
Cardiovascular diseases (CVDs) are the leading cause of death globally. This project applies statistical modeling and machine learning to predict the presence of heart disease in patients based on 11 clinical features.

Utilizing a dataset of 918 patients, the analysis identifies critical biomarkers—such as **ST Slope** and **Exercise-Induced Angina**—and deploys a predictive framework achieving **~87% accuracy**.

## 🔗 Dataset
The dataset used in this analysis is publicly available on Kaggle:
* **Source:** [Heart Failure Prediction Dataset](https://www.kaggle.com/fedesoriano/heart-failure-prediction)
* **Original Source:** Combined from 5 different heart datasets (Cleveland, Hungarian, Switzerland, Long Beach VA, and Stalog).

## 🔑 Key Technical Highlights
* **Leakage-Proof Pipeline:** Implemented a robust preprocessing strategy where missing physiological values (e.g., 0 cholesterol) were imputed *after* the train-test split to prevent data leakage.
* **Domain-Driven EDA:** Developed custom reusable functions to analyze risk factors.
    * *Critical Insight:* Discovered that **Asymptomatic (ASY)** chest pain is the strongest predictor of heart disease, contradicting the assumption that "no pain = healthy."
* **Statistical Rigor:** Applied **PowerTransformer (Yeo-Johnson)** to normalize skewed features like `Oldpeak` and `RestingBP` before modeling.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib
* **Machine Learning:** Scikit-Learn (Logistic Regression, Random Forest, SVM, KNN)
* **Workflow:** Jupyter Notebook

## 📊 Model Performance
I benchmarked six different classifiers. **Logistic Regression** and the **Voting Classifier** emerged as the top performers.

| Model | Accuracy | CV Mean Score |
| :--- | :--- | :--- |
| **Logistic Regression** | **86.96%** | **85.15%** |
| SVM | 86.41% | 85.55% |
| Random Forest | 85.87% | 85.28% |
| Naive Bayes | 85.87% | 84.88% |
| Decision Tree | 82.07% | 78.43% |
| KNN | 81.52% | 83.21% |

## 🚀 How to Run Locally

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/EshmeetSingh/Heart-Disease-Diagnostic-Analysis.git](https://github.com/EshmeetSingh/Heart-Disease-Diagnostic-Analysis.git)

2. **Navigate to the project directory:**
   ```bash
   cd Heart-Disease-Diagnostic-Analysis

3. **Install dependencies:**
   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn

4. **Run the Notebook:**
   ```bash
   jupyter notebook Heart_Disease_Prediction_Analysis.ipynb

## 📂 Project Structure
```text
├── Datasets/
│   └── heart.csv                            # Raw dataset
├── Heart_Disease_Prediction_Analysis.ipynb  # Main analysis notebook
├── Heart_Disease_Profile_Report.html        # Automated EDA report (Download to view)
└── README.md                                # Project documentation

```
---
**Author:** [Eshmeet Singh](https://www.linkedin.com/in/EshmeetSingh23)
