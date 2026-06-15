# 🏎️ Formula 1 Pit Stop Prediction using Machine Learning

## 📌 Overview

This project predicts whether a Formula 1 driver will make a pit stop on the next lap using race telemetry and strategy-related data. The solution was developed for a Kaggle Playground competition and leverages advanced machine learning techniques to model pit stop decisions based on tyre degradation, race progress, lap performance, and driver behavior.

The problem is formulated as a **binary classification task** where the model predicts the probability of a driver entering the pit lane on the following lap.

---

## 🎯 Problem Statement

Given the current race conditions and driver telemetry, predict:

> **Will the driver pit on the next lap?**

### Target Variable

| Value | Meaning |
|---------|---------|
| 0 | No Pit Stop |
| 1 | Pit Stop |

---

## 📊 Dataset Information

The dataset contains over **439,000 race observations** from Formula 1 race sessions.

### Features

- Pit Stop Status
- Lap Number
- Stint Number
- Tyre Life
- Driver Position
- Lap Time
- Lap Time Delta
- Cumulative Tyre Degradation
- Race Progress
- Position Change
- Tyre Compound Information
- Driver Frequency Encoding
- Race Frequency Encoding

### Dataset Statistics

| Metric | Value |
|----------|----------|
| Total Records | 439,140 |
| Features | 18+ |
| Target Variable | PitNextLap |
| Problem Type | Binary Classification |

---

## ⚙️ Data Preprocessing

### Feature Encoding

- Frequency Encoding for Driver IDs
- Frequency Encoding for Race Names
- One-Hot Encoding for Tyre Compounds

### Feature Engineering

Created additional race strategy indicators:

- DegradationPerLap
- TyreStress
- PositionRisk

### Data Quality Checks

- Missing Value Analysis
- Feature Distribution Analysis
- Correlation Analysis
- Target Distribution Analysis

---

## 🤖 Machine Learning Models Evaluated

### Gradient Boosting Models

- LightGBM
- XGBoost
- CatBoost

### Ensemble Models

- Random Forest
- Extra Trees
- AdaBoost
- Gradient Boosting

---

## 📈 Model Evaluation

### Validation Techniques

- Train-Validation Split
- Stratified K-Fold Cross Validation
- Overfitting Detection
- Feature Importance Analysis

### Evaluation Metric

**ROC-AUC (Receiver Operating Characteristic - Area Under Curve)**

ROC-AUC measures the model's ability to distinguish between pit-stop and non-pit-stop situations.

---

## 🏆 Best Performing Model

### LightGBM Classifier

LightGBM achieved the best balance between performance, speed, and generalization.

### Final Results

| Metric | Score |
|----------|----------|
| Train ROC-AUC | 0.9446 |
| Validation ROC-AUC | 0.9409 |
| Cross Validation ROC-AUC | 0.9393 |
| Overfitting Gap | 0.0038 |

The very small train-validation gap indicates excellent generalization capability.

---

## 🔍 Feature Importance

Top predictive features identified by the model:

1. Race_FE
2. LapTime (s)
3. RaceProgress
4. Cumulative_Degradation
5. LapTime_Delta
6. TyreLife
7. LapNumber
8. Stint
9. TyreStress
10. Driver_FE

These features play a significant role in determining pit-stop strategies.

---

## 🛠️ Tech Stack

### Programming Language

- Python

### Data Analysis

- Pandas
- NumPy

### Machine Learning

- Scikit-Learn
- LightGBM
- XGBoost
- CatBoost

### Visualization

- Matplotlib
- Seaborn

### Model Persistence

- Joblib

---

## 📂 Project Workflow

```text
Data Collection
      │
      ▼
Data Cleaning
      │
      ▼
Feature Engineering
      │
      ▼
Feature Encoding
      │
      ▼
Model Training
      │
      ▼
Cross Validation
      │
      ▼
Performance Evaluation
      │
      ▼
Feature Importance Analysis
      │
      ▼
Prediction Generation
      │
      ▼
Kaggle Submission
```

---

## 🚀 Key Achievements

- Built a complete machine learning pipeline for Formula 1 strategy prediction.
- Processed and analyzed 439K+ race observations.
- Implemented advanced feature engineering and encoding techniques.
- Evaluated multiple boosting and ensemble models.
- Achieved **0.94+ ROC-AUC** on Kaggle leaderboard.
- Developed a scalable and reproducible ML workflow.

---

## 🔮 Future Improvements

- Advanced Target Encoding
- Multi-Seed Ensembling
- Optuna Hyperparameter Optimization
- Pseudo Labeling
- SHAP Explainability
- MLflow Experiment Tracking
- Stacking & Blending Ensembles

---

## 📊 Results Summary

| Model | Validation ROC-AUC |
|---------|---------|
| LightGBM | 0.9409 |
| XGBoost | 0.9459 |
| CatBoost | 0.9430 |
| Extra Trees | Competitive Baseline |
| Random Forest | Competitive Baseline |

---

## 👨‍💻 Author

**Ruchit Sonawane**

Chemical Engineering Undergraduate | Machine Learning Enthusiast | Data Science & AI Projects

---

### Kaggle Competition

**Predicting Formula 1 Pit Stops**

Built a machine learning solution to predict next-lap pit stop decisions using race telemetry, tyre degradation metrics, and race strategy indicators, achieving **0.94+ ROC-AUC** through feature engineering and gradient boosting models.
