# Explainable and Optimized Machine Learning for Ransomware Detection and Classification

## Overview

This research project presents a leakage-aware and explainable machine learning framework for ransomware detection and classification using network traffic data. The study focuses on reliable evaluation through leakage investigation, class imbalance handling, model comparison, explainability, robustness testing, and unseen-ransomware-family generalization.

## Dataset

* **Dataset:** UGRansome
* **Domain:** Cybersecurity / Network Traffic
* **Records:** 149,043
* **Classes:** Signature (S), Anomaly (A), Synthetic Signature (SS)

The dataset is not included in this repository.

## Methodology

The project includes:

* Leakage investigation using feature-signature grouping
* Group-aware train/validation/test splitting
* Class balancing using **SMOTENC**
* Categorical feature encoding
* Machine learning model comparison
* **SHAP-based explainability**
* Feature-group ablation analysis
* Gaussian-noise robustness testing
* Unseen-ransomware-family generalization
* Group-aware 5-fold cross-validation

### Models

* XGBoost
* LightGBM
* Random Forest
* Multilayer Perceptron (MLP)

## Results

| Model         | Accuracy | F1-Score | Log Loss |
| ------------- | -------: | -------: | -------: |
| Random Forest |   99.53% |   0.9953 |  0.01315 |
| MLP           |   98.31% |   0.9831 |  0.03476 |
| LightGBM      |   99.65% |   0.9965 |  0.00654 |
| XGBoost       |   99.67% |   0.9967 |  0.00701 |

XGBoost achieved **99.67% accuracy** on the independent test set, while LightGBM achieved the lowest log loss of **0.00654**.

## Explainability & Robustness

The study uses SHAP and feature-importance analysis to investigate model decisions.

Additional experiments evaluate:

* Feature-group ablation
* Gaussian-noise robustness
* Generalization to an unseen ransomware family

XGBoost achieved **89.64% accuracy with 20% Gaussian feature noise** and **83.26% accuracy when the Globe ransomware family was excluded from training**.

## Visualizations

Selected results and analysis figures are available in the [`results`](results/) folder.

* Confusion Matrix
* ROC Curve
* SHAP Analysis
* Feature Importance
* Ablation Study
* Robustness Test
* Cross-Validation

## Research Status

**Manuscript Submitted — Not Yet Published**

The full research manuscript and source code are not publicly included in this repository at the current stage.

## Authors

* **Merina Amdad Taspia**
* **Samia Tasmin Nova**
* **Md. Ziaul Hoque Khasru**

Department of Computer Science and Engineering
International Islamic University Chittagong, Bangladesh
