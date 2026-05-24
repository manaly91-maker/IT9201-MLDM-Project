# IT9201 – Machine Learning and Data Mining
## Predicting Gen Z Purchase Intention Through AI-Powered Digital Marketing Campaigns Using Machine Learning Techniques

**Student:** Manal Talal Ameen | **ID:** 12011218
**Programme:** MSc in Artificial Intelligence | Bahrain Polytechnic
**Lecturer:** Dr. Shomona Gracia Jacob
**Submission:** May 2026

---

## Project Overview

This project predicts Gen Z and Millennial purchase intention using AI-powered digital marketing behavioral features through supervised and unsupervised machine learning techniques. Three classification models are implemented and compared, hyperparameter optimization is applied using GridSearchCV, and K-Means clustering is used to identify distinct behavioral audience segments.

The study applies machine learning to the Alsaadi et al. (2024) Digital Marketing Dataset to move beyond descriptive survey analysis toward predictive modeling of consumer purchasing behavior.

---

## Dataset

| Information | Details |
|---|---|
| Dataset Name | Alsaadi et al. (2024) Digital Marketing Dataset |
| Source | Data in Brief, Elsevier — DOI: 10.1016/j.dib.2024.111045 |
| Rows | 520 |
| Columns | 49 (48 features + 1 target) |
| Missing Values | 0 |
| Target Variable | DM_Impact (1=Negative, 2=Neutral, 3=Positive) |
| Class Distribution | Positive 49.8% · Negative 27.5% · Neutral 22.7% |
| Country | Saudi Arabia |
| Encoding | Pre-encoded integers — no label encoding required |
| License | CC BY 4.0 — Open access |

**Dataset GitHub:** https://github.com/Hana0111/Digital-Marketing

### References
- Alsaadi, H., Wali, A., & Fakieh, B. (2024). *A dataset analysis of digital marketing's influence on purchase intentions of millennials and generation Z in Saudi Arabia*. Data in Brief, 57, 111045. https://doi.org/10.1016/j.dib.2024.111045
- Alsaadi, H., Wali, A., & Fakieh, B. (2025). *Predicting impact of digital ads on purchasing intention using machine learning classification models*. Advances and Applications in Statistics, 92(2), 303–342. https://doi.org/10.17654/0972361725014

---

## Machine Learning Techniques

| Technique | Purpose |
|---|---|
| Logistic Regression | Baseline linear classifier |
| Decision Tree | Nonlinear if-then rule classifier |
| Random Forest | Ensemble classifier — best performer |
| GridSearchCV (cv=3) | Hyperparameter optimization |
| K-Means Clustering (k=3) | Unsupervised behavioral segmentation |

---

## Feature Selection

7 features selected from 48 using Random Forest Gini importance analysis:

| Feature | Importance |
|---|---|
| SM_Influencers_Recommendations | 27.4% |
| Product_Features | 17.5% |
| Scarcity_phrases | 16.7% |
| Using_product_Results | 13.9% |
| SM_Users_Recommendations | 10.2% |
| Repeated_Exposure | 8.9% |
| SM_Marketing_Campaigns | 5.4% |

Binary ad-format and platform columns (avg 1.10%) and demographic variables (avg 2.06%) were excluded due to low predictive signal.

---

## Results

### Model Performance (104-sample held-out test set)

| Model | Accuracy | Macro Precision | Macro Recall | Macro F1 |
|---|---|---|---|---|
| Logistic Regression | 52.88% | 35.09% | 44.39% | 39.15% |
| Decision Tree | 54.81% | 51.23% | 48.28% | 48.22% |
| Random Forest (Default) | 52.88% | 49.99% | 47.13% | 47.45% |
| **Random Forest (Optimized)** | **55.77%** | **60.92%** | **47.61%** | **46.55%** |

- **Best parameters:** n_estimators=100, max_depth=5
- **Best CV Macro F1:** 60.37% (3-fold cross-validation)
- **Improvement over random chance:** +22.5 percentage points above 33.3% baseline

### K-Means Clustering (k=3)

| Cluster | Size | Profile | Purchase Intention |
|---|---|---|---|
| Cluster 0 – Low Influence | 151 | Low engagement across all features | 54% Negative |
| Cluster 1 – Product-Focused | 171 | High product content responsiveness | 51% Positive |
| Cluster 2 – High Influence | 198 | High across all marketing channels | 68% Positive |

### Orange 3 Cross-Validation (5-fold)

| Model | AUC | CA | F1 | Precision | Recall |
|---|---|---|---|---|---|
| Logistic Regression | 0.773 | 0.671 | 0.718 | 0.626 | 0.842 |
| Random Forest | 0.746 | 0.688 | 0.714 | 0.658 | 0.780 |
| Tree | 0.688 | 0.663 | 0.665 | 0.659 | 0.672 |

---

## Evaluation Metrics

- **Accuracy** — overall proportion correct
- **Precision (macro)** — reliability of predictions across all 3 classes
- **Recall (macro)** — coverage of actual positives across all 3 classes
- **F1-Score (macro)** — primary metric; harmonic mean of Precision and Recall, equal weight to all 3 classes regardless of frequency

Macro F1 was chosen as the primary metric because the dataset is moderately imbalanced (Positive 49.8%) — accuracy alone would be misleading.

---

## Software Libraries

| Library | Version | Purpose |
|---|---|---|
| pandas | 2.x | Data loading, column cleaning, feature separation |
| NumPy | 1.x | Numerical operations |
| scikit-learn | 1.x | ML models, GridSearchCV, KMeans, evaluation metrics |
| Matplotlib | latest | Charts, confusion matrices, visualizations |
| Seaborn | latest | Heatmaps, distribution plots |

---

## Files Included

| File | Description |
|---|---|
| MDLM_Manal_Talal.ipynb | Full machine learning pipeline notebook |
| MLDM_IT9201_Final.pdf | Final project report |
| Digital_marketing_dataset.csv | Dataset used for analysis |
| ManalTalal_Orange_Flow_MLDM.ows | Orange 3 no-code validation workflow |

---

## How to Run

1. Upload `Digital_marketing_dataset.csv` to Google Drive under `MyDrive/MLDM/`
2. Open `MDLM_Manal_Talal.ipynb` in Google Colab
3. Click **Runtime → Run all**
4. All figures are saved automatically as PNG files

---

## Future Extensions

- **Explainable AI (SHAP/LIME)** — per-prediction feature contribution scores
- **NLP + Sentiment Analysis** — text signals from social media comments and reviews
- **Real-Time API Data** — replace survey data with TikTok/Instagram behavioral signals
- **Deep Learning (MLP/LSTM)** — capture higher-order nonlinear feature interactions
- **Cross-Cultural Validation** — test generalisability across Bahrain, UAE, Egypt, Europe
- **Deployment (Streamlit/FastAPI)** — real-time prediction dashboard for marketing teams

---

## Author

**Manal Talal Ameen**
MSc in Artificial Intelligence | ICT9010
Bahrain Polytechnic
IT9201 – Machine Learning and Data Mining
Lecturer: Dr. Shomona Gracia Jacob
