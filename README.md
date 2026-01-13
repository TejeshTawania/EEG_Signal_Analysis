# EEG_Signal_Analysis
# EEG Workload Classification Pipeline

This project focuses on classifying mental workload levels using Electroencephalography (EEG) data. It involves loading EEG signals and corresponding workload labels, performing exploratory data analysis in both time and frequency domains, and applying various machine learning models for classification. The goal is to identify distinct patterns in EEG signals that correlate with different workload levels (low, intermediate, high).

The project employs different classification approaches to predict workload levels:

# EEG Feature Extraction & Classification

This repository contains a comparative analysis of two distinct feature engineering and machine learning pipelines for EEG (Electroencephalogram) signal classification.

---

## 1. Pipeline: Statistical Features + Machine Learning Models

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



---

## 2. Pipeline: Statistical + Band Power Features + SVM

This methodology expands the spectral range and incorporates power-based features to capture a more holistic view of the subject's brain state.

### Preprocessing & Feature Engineering
* **Bandpass Filtering**: A broader frequency range of **4 Hz to 50 Hz** is applied.
* **Feature Set**:
    * **Statistical Features**: Mean, Variance, Std Dev, Skewness, and Kurtosis.
    * **Band Power**: Absolute power for **Delta, Theta, Alpha, Beta, and Gamma** bands.
    * **Spectral Ratios**: Calculation of **Beta/Alpha** and **Theta/Alpha** ratios to identify cognitive states.





