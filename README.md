# Credit Risk Analysis
## *Build & Optimize Supervised Machine Learning Models to Predict Credit Risk*
### Project Overview: Employ different techniques to train using the scikit-learn and imbalanced-learn libraries, compare each technique's impact, and evaluate the models for viability to accurately predict high vs. low risk loan applications
---
</br>

Using credit card credit data from LendingClub, a peer-to-peer lending services company, we oversampled the data using RandomOverSampler and SMOTE algorithms, undersampled the data using the ClusterCentroids algorithm, and used a combination approach of over and undersampling using the SMOTEENN algorithm.  After employing each sampling technique we ran the re-sampled data through a logistic regression model, determined the models' accuracy scores, and created confusion matrices and classification reports to determine the strength of each technique.

To continue to strengthen our predictive model, we utilized two ensemble algorithms aimed at reducing bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, then determined the models' accuracy scores and produced confusion matrices and classification reports to determine the strength of each algorithm in accurately predicting credit risk.
</br>
</br>

## Results

| **RandomOver Sampler**  | **SMOTE Oversampler** | **ClusterCentroids Undersampler** | **Combined SMOTEENN** | **BalancedRandom ForestClassifier** | **EasyEnsemble Classifier** |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Accuracy Score: 0.67  | Accuracy Score: .64  |  Accuracy Score: 0.55 |  Accuracy Score: 0.63  |  Accuracy Score: 0.80  |  Accuracy Score: 0.93  |
| Precision (High-Risk): 0.09  | Precision (High-Risk): 0.01  | Precision (High-Risk): 0.01  | Precision (High-Risk): 0.01  |  Precision (High-Risk): 0.03  |  Precision (High-Risk: 0.09)  |
| Precision (Low-Risk): 1.0 | Precision (Low-Risk): 1.0  | Precision (Low-Risk): 1.0  | Precision (Low-Risk): 1.0 |  Precision (Low-Risk): 1.0  |  Precision (Low-Risk): 1.0  |
| Recall (High-Risk): 0.92 | Recall (High-Risk): 0.61  | Recall (High-Risk): 0.67  | Recall (High-Risk): 0.69  |  Recall (High-Risk): 0.71  |  Recall (High-Risk): 0.92  |
| Recall (Low-Risk): 0.95 | Recall (Low-Risk): 0.67  | Recall (Low-Risk): 0.42  | Recall (Low-Risk): 0.57  |  Recall (Low-Risk): 0.88  |  Recall (Low-Risk): 0.95  |

*Confusion matrices and full classification reports can be found in the notebooks for this project*
</br>
</br>

**Accuracy score**: faction of correct predictions (TP+TN)/ (TP+FN+TN+FP)

**Precision (Positive Predictive Value)**: how reliable is a positive classification (TP/TP+FP)

**Recall (Sensitivity)**: ability of the classifier to find all positives of samples (TP/TP+FN)
</br>
</br>

In terms of accuracy, the models performed poorly when utilizing any of the re-sampling techniques.  Precision was 100% for the low-risk predictions, but performed badly in terms of the high-risk predictions.  The model that utilized RandomOverSampler performed well in terms of recall for both high and low risk predictions.  SMOTE, ClusterCentroids and SMOTEENN recall performance was acceptable but still not optimal.

Accuracy scores improved when utilizing the algorithms from the imbalanced-learn library, aimed at balancing datasets which are highly skewed or biased towards some classes.  Precision scores remained similar to those observed by utilizing the re-sampling techniques: perfect precision in predicting low risk loan applications, and very poor precision in predicting high-risk loan applications.  Recall scores improved when utilizing both algorithms for both high and low risk predictions, but performed best with the EasyEnsembleClassifier.  EasyEnsembleClassifer performed best on all metrics.  
</br>
</br>

## Summary

When tasked with a building and optimizing a supervised machine learning model, the target of interest and needed accuracy of the model must be considered before determining the most appropriate model.  Different techniques should be employeed to work towards the best model for the given data, features, and goal.  However, accuracy is not the only metric to consider when determining the best fit model.  Depending on the problem that needs to be solved, precision may be more important than recall, or vice versa, or one of the target outcomes' precision and/or recall may be more important than another.

Assuming the intended goal of determining credit risk is to decline any unfavorable loan applications and reduce liability, and that this goal is more important than precisely predicting low risk loan applications, the precision and recall scores for high risk applicants should be given more consideration than the precision and recall scores for low risk applicants.  However, loan or credit card companies likely do not want to deny valuable customers, so precision and recall scores for low-risk applicants should not be ignored.  If the goal of the company is to strictly deny any high risk applications, recall should be given more weight i.e. there is high sensitivity and little chance of a false positive.

Falling at an accuracy level of just over 50% in correctly predicting risk, the logistic regression models that utilized re-sampling techniques to optimize model performance did not do much better than leaving the predictions to random chance.  Both imbalanced-learn algorithms performed much better at 80% (BalancedRandomForestClassifier) and 93% (EasyEnsembleClassifier).  Precision remained low for predicting high-risk loan applications at 3% (BalancedRandomForestClassifier) and 9% (EasyEnsembleClassifier).  Recall scores showed improvement at 71% (BalancedRandomForestClassifier) and 92% (EasyEnsembleClassifier) for high risk predictions.  Recall was also high for low risk predictions at 88% and 95%, respectively.

We recommend utilizing the EasyEnsembleClassifier model to obtain the most accurate predictions for the intended goal.  This model outperformed or equalled the performance of the other models on all analyzed metrics.  Adding additional data, especially data including high risk outcomes, would increase the precision for high risk predictions and model success overall.  Since the majority of the data included in the dataset belongs to low risk applicants, the machine learning model would get better at predicting high risk outcomes if given more high risk information.  This would lessen the reliance of utilizing the balancing techniques, as the techniques can only help so much.

It is also worth noting the feature importances returned "total principal," "total payment," "total received," and "last payment" to be the most important attributes, and attributes such as "tax liens," "policy code" and "delinquent amount" to bear no significance on the model's predictability. The model could be further optimized by more heavily weighting the features that best predict accurate outcomes and/or dropping some of the insignificant features.  

