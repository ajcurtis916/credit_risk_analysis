# Credit Risk Analysis
## *Build, Test & Optimize Supervised Machine Learning Models to Predict Credit Risk*
### Project Overview: Employ different techniques to train using the scikit-learn and imbalanced-learn libraries, compare each technique's impact, and evaluate the models for viability to accurately predict high vs. low risk loan applications
---
</br>

Using credit card credit data from LendingClub, a peer-to-peer lending services company, we oversampled the data using RandomOverSampler and SMOTE algorithms, undersampled the data using the ClusterCentroids algorithm, and used a combination approach of over and undersampling using the SMOTEENN algorithm.  After employing each sampling technique we ran the re-sampled data through a logistic regression model, determined the models' accuracy scores, and created confusion matrices and classification reports to determine the strength of each technique.

To continue to strengthen our predictive model, we utilized two ensemble algorithms aimed at reducing bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, then determined the models' accuracy scores and produced confusion matrices and classification reports to determine the strengh of each algorithms in accurately predicting credit risk.
</br>
</br>

## Results

**RandomOverSampler**

  - Accuracy Score: 0.67
  - Precision
    - High-Risk: 0.09
    - Low-Risk: 1.0
  - Recall
    - High-Risk: 0.92
    - Low-Risk: 0.95
  
**SMOTE**

  - Accuracy Score: .64
  - Precision
    - High-Risk: 0.01
    - Low-Risk: 1.0
  - Recall
    - High-Risk: 0.61
    - Low-Risk: 0.67

**ClusterCentroids**
  
  - Accuracy Score: 0.55
  - Precision
    - High-Risk: 0.01
    - Low-Risk: 1.0
  - Recall
    - High-Risk: 0.67
    - Low-Risk: 0.42
  
**SMOTEENN**
  
  - Accuracy Score: 0.63
  - Precision
    - High-Risk: 0.01
    - Low-Risk: 1.0
  - Recall
    - High-Risk: 0.69
    - Low-Risk: 0.57
  
**BalancedRandomForestClassifier**

  - Accuracy Score: 0.80
  - Precision
    - High-Risk: 0.03
    - Low-Risk: 1.0
  - Recall
    - High-Risk: 0.71
    - Low-Risk: 0.88
 
 **EasyEnsembleClassifier**
 
  - Accuracy Score: 0.93
  - Precision
    - High-Risk: 0.03
    - Low-Risk: 1.0
  - Recall
    - High-Risk: 0.71
    - Low-Risk: 0.88
</br>

## Summary

Summarize results above, recommend which model to use, or there is no recommendation with a justification.  Include bit about feature importance.  
