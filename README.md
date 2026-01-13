# EEG_Signal_Analysis
# EEG Workload Classification Pipeline

This project focuses on classifying mental workload levels using Electroencephalography (EEG) data. It involves loading EEG signals and corresponding workload labels, performing exploratory data analysis in both time and frequency domains, and applying various machine learning models for classification. The goal is to identify distinct patterns in EEG signals that correlate with different workload levels (low, intermediate, high).

The project employs different classification approaches to predict workload levels:

# EEG Feature Extraction & Classification

This repository contains a comparative analysis of two distinct feature engineering and machine learning pipelines for EEG (Electroencephalogram) signal classification.

---

## Pipeline: Statistical Features + Machine Learning Models

This methodology focuses on isolating high-frequency brain activity and applying both traditional and geometric classification techniques.

### Preprocessing & Feature Engineering
* **Bandpass Filtering**: EEG data is filtered between **25.8 Hz and 54.2 Hz** to isolate high-frequency oscillations.
* **Statistical Feature Extraction**: The following features are extracted from the filtered signals for each trial:
    * Mean
    * Variance
    * Standard Deviation
    * Skewness
    * Kurtosis
* **Data Splitting**: Dataset partitioning is managed via `testIndices.csv` to ensure consistent and reproducible evaluation across runs.

### Model Suite
| Model | Algorithm Type | Key Characteristic |
| :--- | :--- | :--- |
| **Random Forest** | Ensemble Learning | Uses bagging to improve robustness. |
| **SVM (RBF Kernel)** | Non-linear Classifier | Effective in high-dimensional feature spaces. |
| **MDM Classifier** | Riemannian Geometry | Classifies via **Minimum Distance to Mean** using covariance matrix geometry. |





