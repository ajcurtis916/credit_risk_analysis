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

| **RandomOverSampler**  | **SMOTE Oversampler** | **ClusterCentroids Undersampler** | **Combined SMOTEENN** | **BalancedRandom ForestClassifier** | **EasyEnsemble Classifier** |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Accuracy Score: 0.67  | Accuracy Score: .64  |  Accuracy Score: 0.55 |  Accuracy Score: 0.63  |  Accuracy Score: 0.80  |  Accuracy Score: 0.93  |
| Precision (High-Risk): 0.09  | Precision (High-Risk): 0.01  | Precision (High-Risk): 0.01  | Precision (High-Risk): 0.01  |  Precision (High-Risk): 0.03  |  Precision (High-Risk: 0.03)  |
| Precision (Low-Risk): 1.0 | Precision (Low-Risk): 1.0  | Precision (Low-Risk): 1.0  | Precision (Low-Risk): 1.0 |  Precision (Low-Risk): 1.0  |  Precision (Low-Risk): 1.0  |
| Recall (High-Risk): 0.92 | Recall (High-Risk): 0.61  | Recall (High-Risk): 0.67  | Recall (High-Risk): 0.69  |  Recall (High-Risk): 0.71  |  Recall (High-Risk): 0.71  |
| Recall (Low-Risk): 0.95 | Recall (Low-Risk): 0.67  | Recall (Low-Risk): 0.42  | Recall (Low-Risk): 0.57  |  Recall (Low-Risk): 0.88  |  Recall (Low-Risk): 0.88  |

*Confusion matrices and full classification reports can be found in the notebooks for this project*
</br>
</br>

**Accuracy score**: faction of correct predictions (TP+TN)/ (TP+FN+TN+FP)

**Precision (Positive Predictive Value)**: how reliable is a positive classification (TP/TP+FP)

**Recall (Sensitivity)**: ability of the classifier to find all positives of samples (TP/TP+FN)


 
 
</br>

## Summary

When tasked with a building and optimizing a supervised machine learning model, the target of interest and accurancy of model must be considered before determining the most appropriate model.  Different techniques should be employeed to work towards the best model for the given data and features.  However, accuracy is not the only metric to consider when determining the best fit model.  Depending on the problem that needs to be solved, precision may be more important than recall, or vice versa, or one of the target outcomes' precision and/or recall may be more inmportant than another.   

Summarize results above, recommend which model to use, or there is no recommendation with a justification.  Include bit about feature importance.  
