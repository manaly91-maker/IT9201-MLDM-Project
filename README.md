# IT9201 – MLDM Project

## Predicting Gen Z Purchase Intention Through AI-Powered Digital Marketing Campaigns Using Machine Learning Techniques

---

## Project Overview

This project predicts Gen Z purchase intention using AI-powered digital marketing behavioral features through supervised and unsupervised machine learning techniques.

The project analyzes how influencer recommendations, product-focused marketing, scarcity phrases, repeated exposure, and social media engagement influence purchasing behavior.

The study applies classification and clustering algorithms to identify predictive behavioral patterns and audience segments.

---

## Dataset

### Citation

Alsaadi, H., Wali, A., & Fakieh, B. (2024). *A dataset analysis of digital marketing's influence on purchase intentions of millennials and generation Z in Saudi Arabia*. Data in Brief, 57, 111045. [https://doi.org/10.1016/j.dib.2024.111045](https://doi.org/10.1016/j.dib.2024.111045)

Alsaadi, H., Wali, A., & Fakieh, B. (2025). *Predicting impact of digital ads on purchasing intention using machine learning classification models*. Advances and Applications in Statistics, 92(2), 303–342.

---

## Dataset

| Information     | Details                                         |
| --------------- | ----------------------------------------------- |
| Dataset Name    | Alsaadi et al. (2024) Digital Marketing Dataset |
| Rows            | 520                                             |
| Columns         | 49                                              |
| Missing Values  | 0                                               |
| Target Variable | DM_Impact                                       |
| Classes         | Negative / Neutral / Positive                   |
| Country         | Saudi Arabia                                    |
| Dataset Type    | Structured behavioral survey dataset            |

---

## Machine Learning Techniques Used

| Technique           | Purpose                        |
| ------------------- | ------------------------------ |
| Logistic Regression | Baseline linear classification |
| Decision Tree       | Nonlinear classification       |
| Random Forest       | Ensemble classification        |
| GridSearchCV        | Hyperparameter optimization    |
| K-Means Clustering  | Behavioral segmentation        |

---

## Feature Selection

The following features were selected using Random Forest feature importance analysis:

* SM_Influencers_Recommendations
* Product_Features
* Scarcity_phrases
* Using_product_Results
* SM_Users_Recommendations
* Repeated_Exposure
* SM_Marketing_Campaigns

---

## Evaluation Metrics

* Accuracy
* Precision
* Recall
* Macro F1-Score

Macro F1-score was used because the dataset is moderately imbalanced and requires balanced evaluation across all classes.

---

## Main Findings

* Random Forest achieved the best overall performance.
* Influencer recommendations were the strongest predictor of purchase intention.
* AI-powered personalization strongly influences Gen Z purchasing behavior.
* K-Means clustering identified three behavioral audience segments:

  * Low Influence Users
  * Product-Focused Users
  * High Influence Users

---

## Software Libraries

* pandas
* NumPy
* scikit-learn
* Matplotlib
* Seaborn

---

## Files Included

| File                          | Description                    |
| ----------------------------- | ------------------------------ |
| MDLM_Manal_Talal.ipynb        | Full machine learning notebook |
| MLDM_IT9201_Final_v6.docx     | Final project report           |
| Digital_marketing_dataset.csv | Dataset used for analysis      |
| figures/                      | Visualizations and charts      |

---

## Future Improvements

* Natural Language Processing (NLP)
* Explainable AI (SHAP/LIME)
* Real-time API data collection
* Deep Learning models
* Cross-cultural behavioral analysis

---

## Author

Manal Talal Ameen
MSc in Artificial Intelligence
Bahrain Polytechnic
