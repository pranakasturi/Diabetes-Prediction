# Diabetes Prediction Using Machine Learning

## Overview

This project aims to predict the likelihood of diabetes using various machine learning algorithms. The analysis incorporates correlation analysis, data normalization using StandardScaler, and a comparative evaluation of several classification models. The key objective is to identify the most effective model for diabetes prediction, considering accuracy, sensitivity, and specificity, which are particularly important in healthcare applications. The Area Under the ROC Curve (AUC) is also considered as an evaluation metric.

## Analysis Steps

The following steps were performed in this analysis:

1.  **Correlation Analysis:** Examining the relationships between different features in the dataset to understand their potential influence on diabetes prediction.
2.  **Data Normalization:** Applying StandardScaler to normalize the feature data, ensuring that all features contribute equally during model training, regardless of their original scale.
3.  **Model Implementation and Evaluation:** Several classification models were implemented and their performance was evaluated:
    * Logistic Regression
    * Decision Tree
    * Random Forest
    * Support Vector Machine (SVM)
    * Naive Bayes
    * K-Nearest Neighbors (KNN)
    * Gradient Boosting

## Model Performance Comparison

The accuracy, sensitivity, and specificity of each model were evaluated, and the results are as follows:

| Model                  | Accuracy | Sensitivity | Specificity |
| :--------------------- | :------- | :---------- | :---------- |
| Logistic Regression    | 0.7359   | -           | -           |
| Decision Tree          | 0.7056   | -           | -           |
| Random Forest          | 0.7489   | 0.9028      | 0.4943      |
| Support Vector Machine | 0.7403   | -           | -           |
| Naive Bayes            | 0.7359   | -           | -           |
| K-Nearest Neighbors    | 0.7403   | 0.8056      | 0.6322      |
| Gradient Boosting      | 0.7792   | 0.8750      | 0.6207      |

The Area Under the ROC Curve (AUC) for the best-performing models was also considered, with a reported AUC value of **0.69851**.

## Findings and Conclusion

Based on the evaluation metrics, the **Gradient Boosting model** achieved the highest accuracy (0.7792). However, in the healthcare domain, where correctly identifying individuals with the condition (high sensitivity) is often paramount, we need to consider this metric alongside accuracy and specificity.

Comparing the sensitivity and specificity of the top contenders:

* **Random Forest:** High sensitivity (0.9028) but lower specificity (0.4943).
* **Gradient Boosting:** High sensitivity (0.8750) and relatively higher specificity (0.6207) compared to Random Forest.
* **K-Nearest Neighbors:** Good sensitivity (0.8056) and the highest specificity (0.6322) among these three.

Considering the trade-off between sensitivity and specificity, and the importance of high sensitivity in minimizing false negatives in a diabetes prediction scenario, the **Random Forest model stands out due to its exceptionally high sensitivity.** While its specificity is lower, the priority in this context is to ensure that individuals with diabetes are correctly identified. The reported AUC value of 0.69851 further supports the predictive capability of the models.

**Conclusion: The Random Forest model is determined to be the most suitable model for this diabetes prediction task due to its very high sensitivity (0.9028), ensuring that a large proportion of individuals with diabetes are correctly identified. While the Gradient Boosting model has the highest accuracy, the emphasis on minimizing false negatives in healthcare makes the high sensitivity of the Random Forest model a critical advantage.**
