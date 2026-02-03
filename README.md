# Credit Card Fraud: Sampling Technique Analysis

This repository contains a complete analysis of how various sampling techniques affect the accuracy of machine learning models when dealing with imbalanced datasets. 

## Objective

The objective is to understand the importance of sampling techniques in handling imbalanced datasets and to analyze how different strategies affect model performance. The task involves balancing a highly imbalanced credit card dataset and evaluating multiple machine learning models. 

## Methodology

1. 
**Dataset**: The credit card dataset was sourced from the specified GitHub repository. 


2. 
**Data Balancing**: The original dataset was imbalanced. I converted it into a balanced class dataset using manual oversampling to equalize the classes. 


3. 
**Sampling Techniques**: Five distinct sampling techniques were applied: 


* **Sampling 1**: Simple Random Sampling
* **Sampling 2**: Systematic Sampling
* **Sampling 3**: Stratified Sampling
* **Sampling 4**: Cluster Sampling
* **Sampling 5**: Bootstrap Sampling


4. 
**Models Evaluated**: Five different ML models were tested: 


* **M1**: Logistic Regression
* **M2**: Random Forest
* **M3**: SVC (Support Vector Classifier)
* **M4**: Decision Tree
* **M5**: KNN (K-Nearest Neighbors)



## Results

The following table summarizes the accuracy (%) achieved for each model and sampling technique: 

| Model | Sampling 1 | Sampling 2 | Sampling 3 | Sampling 4 | Sampling 5 |
| --- | --- | --- | --- | --- | --- |
| **M1** | 87.01 | 80.65 | 88.52 | 88.04 | 96.73 |
| **M2** | 98.70 | 100.00 | 100.00 | 100.00 | 100.00 |
| **M3** | 67.53 | 67.74 | 66.39 | 84.78 | 80.07 |
| **M4** | 97.40 | 90.32 | 100.00 | 96.74 | 100.00 |
| **M5** | 97.40 | 93.55 | 95.08 | 97.83 | 99.67 |

---

## Discussion & Analysis

* 
**Model Performance**: The **Random Forest (M2)** model emerged as the most robust, achieving 100% accuracy across almost all sampling techniques.  This is likely due to its ensemble nature, which effectively captures the patterns in the oversampled minority class.


* **Sampling Efficacy**: **Bootstrap Sampling (Sampling 5)** and **Stratified Sampling (Sampling 3)** provided the most consistent results. Stratified sampling was particularly effective because it ensured that the balanced proportions of the dataset were preserved in the smaller sub-samples.
* **Observation on SVC**: **SVC (M3)** showed the lowest overall performance. This suggests that the high-dimensional nature of the credit card dataset may require more complex parameter tuning for Support Vector Machines compared to tree-based models like Random Forest or Decision Trees.

## Conclusion

For this specific credit card fraud dataset, using an ensemble model (M2) paired with a stratified or bootstrap sampling approach (S3/S5) yields the most reliable classification results.  
