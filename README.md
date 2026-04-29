# Capstone Project: Breast Cancer Diagnostic Analysis

**Author:** Arnav Gehlot
**Dataset:** Breast Cancer Wisconsin (Diagnostic) Dataset (Source: UCI Machine Learning Repository)

## 📌 Project Overview
This project performs an Exploratory Data Analysis (EDA) and hypothesis testing on digitized images of fine needle aspirates (FNA) of breast masses. The primary objective is to evaluate the dataset's structural integrity, identify highly predictive cellular features, and prepare the data for supervised machine learning classification algorithms.

## 📊 Key Findings & Business Impact
*   **Target Variable Distribution:** The dataset is mildly imbalanced (62.7% Benign, 37.3% Malignant), establishing a baseline accuracy requirement for future predictive models.
*   **Feature Importance:** Visual and statistical analysis confirms that mathematical measurements of the cell nucleus—specifically `radius_mean` and `texture_mean`—are strong indicators of malignancy. 
*   **Statistical Validation:** An independent two-sample t-test was conducted on cell radius between benign and malignant classes. The resulting p-value ($8.46 \times 10^{-96}$) was virtually zero, firmly rejecting the null hypothesis and mathematically proving that malignant cells are significantly larger.
*   **Multivariate Necessity:** Bivariate analysis revealed an "overlap zone" between benign and malignant profiles, proving that simple threshold rules are insufficient. A multidimensional machine learning model analyzing all 30 variables simultaneously is required for medical-grade diagnostic accuracy.

## 📁 Repository Contents
*   `breast_cancer_analysis.ipynb`: The core Google Colab Jupyter Notebook containing the Python code for data cleaning, visualization (using Pandas, Matplotlib, and Seaborn), and statistical testing (SciPy).
*   `data.csv`: The raw dataset used for the analysis.
*   `Capstone_Breast_Cancer_Analysis.pdf`: The final, presentation-ready stakeholder report detailing methodology, visualizations, and actionable insights.

## 🚀 Next Steps for Predictive Modeling
Having verified the quality of this dataset, the immediate next steps are:
1.  **Feature Scaling:** Apply standardization to numerical features to ensure proper algorithmic weighting.
2.  **Model Selection:** Implement and compare classification models, including Logistic Regression, Support Vector Machines (SVM), and Random Forests.
3.  **Model Evaluation:** Train models using a standard train/test split, prioritizing the **Recall (Sensitivity)** metric to aggressively minimize the risk of false-negative diagnoses.
