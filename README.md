# Heart Disease Prediction

A machine learning project that predicts the presence of heart disease based on 
clinical parameters, comparing four classification algorithms to find the best performer.

---

## Overview

Heart disease is one of the leading causes of death worldwide. Early detection 
significantly improves patient outcomes. This project uses **supervised machine 
learning** to predict whether a patient has heart disease based on 11 clinical 
features.

Four models were trained and evaluated:
- Logistic Regression
- Decision Tree
- **Random Forest** (best performer)
- Support Vector Machine (SVM)

---

## Dataset

- **Source:** [Heart Failure Prediction Dataset — Kaggle](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)
- **Size:** 918 rows × 12 columns
- **Missing values:** None
- **Target variable:** `HeartDisease` (0 = No disease, 1 = Disease)

### Feature Description

| Feature | Description |
|---|---|
| `Age` | Age of the patient (years) |
| `Sex` | M = Male, F = Female |
| `ChestPainType` | ATA, NAP, ASY, TA |
| `RestingBP` | Resting blood pressure (mm Hg) |
| `Cholesterol` | Serum cholesterol (mm/dl) |
| `FastingBS` | Fasting blood sugar (1 if > 120 mg/dl, else 0) |
| `RestingECG` | Resting electrocardiogram (Normal, ST, LVH) |
| `MaxHR` | Maximum heart rate achieved |
| `ExerciseAngina` | Exercise-induced angina (Y/N) |
| `Oldpeak` | ST depression induced by exercise |
| `ST_Slope` | Slope of peak exercise ST segment (Up, Flat, Down) |
| `HeartDisease` | **Target:** 0 = No, 1 = Yes |

---

## Methodology

1. **Data Loading & Inspection** — shape, dtypes, missing values
2. **Exploratory Data Analysis (EDA)** — target distribution, correlations, feature relationships
3. **Outlier Detection** — IQR method (kept outliers since they represent real clinical cases)
4. **Encoding** — `LabelEncoder` for categorical features
5. **Train/Test Split** — 80/20, `random_state=42`
6. **Feature Scaling** — `StandardScaler`
7. **Model Training** — 4 classifiers trained on the same data
8. **Evaluation** — Accuracy, Precision, Recall, F1 Score, Confusion Matrix

---

## Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---|---|---|
| Logistic Regression | 0.848 | 0.907 | 0.822 | 0.863 |
| Decision Tree | 0.826 | 0.879 | 0.813 | 0.845 |
| **Random Forest** | **0.886** | **0.913** | **0.888** | **0.900** |
| SVM | 0.864 | 0.894 | 0.869 | 0.882 |

**Best Model: Random Forest**
- Accuracy: **88.6%**
- F1 Score: **0.900**

---

## Tech Stack

- **Language:** Python 3.13
- **Data:** pandas, numpy
- **ML:** scikit-learn
- **Visualization:** matplotlib, seaborn
- **Environment:** Jupyter Notebook

---

## How to Run

### 1. Clone the repository
```bash
git clone https://github.com/SMgit404/heart-disease-prediction