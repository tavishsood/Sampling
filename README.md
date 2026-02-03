# Credit Card Fraud: Sampling Technique Analysis

This repository contains a complete analysis of how various sampling techniques affect the accuracy of machine learning models when dealing with imbalanced datasets.

## Objective

The goal is to balance a highly imbalanced credit card dataset, apply different sampling strategies, and determine which model-sampling combination yields the highest accuracy.

## Methodology

1. **Data Balancing**: The original dataset was imbalanced. I used manual oversampling to equalize the classes.
2. **Sampling Techniques**:
* **Sampling 1**: Simple Random Sampling
* **Sampling 2**: Systematic Sampling
* **Sampling 3**: Stratified Sampling
* **Sampling 4**: Cluster Sampling
* **Sampling 5**: Bootstrap Sampling


3. **Models Evaluated**: Logistic Regression (M1), Random Forest (M2), SVC (M3), Decision Tree (M4), and KNN (M5).

## Results

The following table summarizes the accuracy (%) for each model and sampling technique:

| Model | Sampling 1 | Sampling 2 | Sampling 3 | Sampling 4 | Sampling 5 |
| --- | --- | --- | --- | --- | --- |
| **M1** | 87.01 | 80.65 | 88.52 | 88.04 | 96.73 |
| **M2** | 98.70 | 100.00 | 100.00 | 100.00 | 100.00 |
| **M3** | 67.53 | 67.74 | 66.39 | 84.78 | 80.07 |
| **M4** | 97.40 | 90.32 | 100.00 | 96.74 | 100.00 |
| **M5** | 97.40 | 93.55 | 95.08 | 97.83 | 99.67 |

## Discussion

* **Best Model**: **Random Forest (M2)** consistently provided the highest accuracy, reaching 100% across multiple sampling techniques.
* **Best Sampling Technique**: **Bootstrap Sampling (Sampling 5)** and **Stratified Sampling (Sampling 3)** proved to be the most effective.
* **Observation**: Ensemble-based models like Random Forest and Decision Trees handled the sampled data much better than SVC.
