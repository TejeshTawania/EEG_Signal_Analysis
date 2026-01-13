# EEG_Signal_Analysis
# EEG Workload Classification Pipeline

This repository contains a Python-based pipeline for classifying cognitive workload using EEG signals. It compares traditional machine learning (Random Forest, SVM) against manifold-based learning (Riemannian Geometry).

## 📌 Overview

The script implements a full signal processing and classification workflow:
1. **Filtering:** Isolating frequency bands relevant to cognitive load.
2. **Feature Extraction:** Comparing statistical vector features vs. spatial covariance matrices.
3. **Cross-Validation:** Evaluating performance across multiple test sets/sessions.
4. **Classification:** Benchmarking three distinct mathematical approaches.

---

## 🛠 Methodology

### 1. Data Preprocessing
* **Bandpass Filter:** The signal is constrained to **25.8 Hz – 54.2 Hz**. This range captures the **High Beta** and **Gamma** oscillations, which are primary biomarkers for high-level information processing and mental effort.
* **Feature Sets:**
    * **Statistical:** Extraction of mean, variance, etc., from the filtered time series.
    * **Riemannian:** Calculation of Spatial Covariance Matrices (SCM) to capture the connectivity between EEG channels.

### 2. Model Architectures

| Model | Category | Approach |
| :--- | :--- | :--- |
| **Random Forest** | Ensemble | Uses a forest of decision trees to classify statistical feature vectors. |
| **SVM (RBF)** | Kernel Method | Maps features into a high-dimensional space using a Radial Basis Function to find a non-linear separator. |
| **MDM** | Riemannian | **Minimum Distance to Mean**: Classifies covariance matrices based on their geodesic distance on the SPD manifold. |
