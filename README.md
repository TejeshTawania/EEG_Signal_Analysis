# EEG_Signal_Analysis
# EEG Workload Classification Pipeline

This project focuses on classifying mental workload levels using Electroencephalography (EEG) data. It involves loading EEG signals and corresponding workload labels, performing exploratory data analysis in both time and frequency domains, and applying various machine learning models for classification. The goal is to identify distinct patterns in EEG signals that correlate with different workload levels (low, intermediate, high).

The project employs different classification approaches to predict workload levels:

# Statistical Features + Machine Learning Models
Bandpass Filtering: EEG data is filtered within a specific frequency range (25.8-54.2 Hz) to isolate relevant brainwave activity.
Feature Extraction: Statistical features such as mean, variance, standard deviation, skewness, and kurtosis are extracted from the filtered EEG signals for each trial.
Data Splitting: The dataset is split into training and testing sets based on provided testIndices.csv to ensure consistent evaluation across multiple runs.
Models Used:
Random Forest Classifier: An ensemble learning method.
Support Vector Machine (SVM) with RBF Kernel: A powerful non-linear classifier.
Minimum Distance to Mean (MDM) Classifier (Riemannian Geometry): A method that leverages the geometric properties of covariance matrices for classification, often used in EEG analysis.
Evaluation: Models are evaluated using accuracy, precision, recall, and F1-score for each run.
# Statistical + Band Power Features + SVM
Bandpass Filtering: EEG data is filtered within a broader frequency range (4-50 Hz).
Feature Extraction: In addition to the statistical features, band power features (Delta, Theta, Alpha, Beta, Gamma) and their ratios (Beta/Alpha, Theta/Alpha) are extracted.
Model: SVM with RBF kernel is used for classification.
Evaluation: The model's performance is evaluated using the same metrics.
