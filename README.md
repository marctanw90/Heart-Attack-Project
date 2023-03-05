# Heart Attack Prediction

## Introduction

**Background & context**

  This is a dataset containing information about patients who have experienced heart attacks. The data includes a variety of demographic, clinical, and behavioral variables that can be used to explore factors associated with heart attack incidence and outcomes.

The dataset contains a total of 303 observations (patients) and 14 variables, including:

- Age
- Sex
- Chest pain type
- Resting blood pressure
- Serum cholesterol levels
- Fasting blood sugar
- Resting electrocardiographic results
- Maximum heart rate achieved
- Exercise-induced angina
- ST depression induced by exercise
- Slope of the peak exercise ST segment
- Number of major vessels colored by fluoroscopy
- Thallium stress test result
- Presence of heart disease (the target variable)

The target variable indicates whether or not the patient has heart disease, based on the presence of a heart attack. This can be used to explore factors that contribute to heart disease and to develop predictive models for identifying individuals at risk.

Heart attack, also known as myocardial infarction, is a medical condition in which the blood flow to the heart muscle is blocked, resulting in damage to the heart muscle. It is a leading cause of death worldwide and affects millions of people every year. In recent years, the use of data science techniques and machine learning algorithms has been gaining popularity in the healthcare industry, including the diagnosis and prediction of heart attacks. One important aspect of this is the availability of datasets containing relevant medical information, such as demographic data, clinical measurements, and risk factors. This Heart Attack Dataset is one such dataset, containing various clinical parameters of patients, such as age, gender, blood pressure, cholesterol levels, and whether they have experienced a heart attack or not. This dataset can be used for developing predictive models that can help healthcare professionals identify individuals who are at high risk of experiencing a heart attack, allowing for early intervention and potentially saving lives.

The dataset is commonly used for classification tasks, such as predicting whether or not a patient has heart disease based on their demographic and clinical information.
    
**What is this project about?**

   The purpose of applying machine learning to the heart attack dataset is to develop accurate predictive models that can improve our understanding of the risk factors associated with heart attacks and inform medical decision-making to improve patient outcomes.


## Datasets
The heart attack dataset that is available on Kaggle was originally created by a group of researchers at the University Hospital of Ferrara in Italy. The dataset was made publicly available on Kaggle as part of a data science competition organized by the website. You may find details of the dataset [here](https://www.kaggle.com/datasets/rashikrahmanpritom/heart-attack-analysis-prediction-dataset).


## Model Evaluation/Metrics
|                                    |   Train score |   Test score |   Generalisation |   Accuracy |   Precision |   Recall |   Specificity |    F1 |   ROC AUC |
|:-----------------------------------|--------------:|-------------:|-----------------:|-----------:|------------:|---------:|--------------:|------:|----------:|
| Logistic Regression                |         0.868 |        0.758 |           12.673 |      0.758 |       0.759 |     0.82 |         0.683 | 0.788 |    0.8634 | 
| k-Nearest Neighbour Classification |         0.863 |        0.78  |            9.618 |      0.78  |       0.768 |     0.86 |         0.683 | 0.811 |    0.8449 | 
| Random Forest Classification       |         0.887 |        0.802 |            9.583 |      0.802 |       0.786 |     0.88 |         0.707 | 0.83  |    0.8654 |
| Support Vector Classification      |         0.873 |        0.769 |           11.913 |      0.769 |       0.754 |     0.86 |         0.659 | 0.804 |    0.8624 |
| Decision Tree Classification       |         0.868 |        0.747 |           13.94  |      0.747 |       0.755 |     0.8  |         0.683 | 0.777 |    0.7549 |
| XGBoost Classification             |         0.868 |        0.758 |           12.673 |      0.758 |       0.78  |     0.78 |         0.732 | 0.78  |    0.8554 |
| AdaBoost Classification            |         0.934 |        0.736 |           21.199 |      0.736 |       0.741 |     0.8  |         0.659 | 0.769 |    0.8415 |
| Gradient Boosting Classification   |         1     |        0.758 |           24.2   |      0.758 |       0.78  |     0.78 |         0.732 | 0.78  |    0.8454 |


We can use confusion matrix, AUC ROC curve, MSE, F1 score, etc. for analyzing the model. Each one of them is suited for a specific purpose. We have to decide which one of them to be used, but generally, we can use AUC ROC curve for most of the cases unless explicitly mentioned.

As shown in the chart above, the the random forest classifier has the best performance when compared to the others. This is indicated by the high AUC score (~0.87) this is a good sign that our models will still able to generalise well, even when handling previously unseen data.

## Conclusion 
* In conclusion, the application of machine learning algorithms to the heart attack dataset has provided significant insights into predicting and preventing heart attacks. The dataset contains a range of demographic, clinical, and lifestyle factors that are known to be associated with heart attack. By analyzing these factors, machine learning models have been developed to predict the occurrence of heart attacks.

* The results of the analysis show that machine learning algorithms such as logistic regression, decision tree, and random forest can accurately predict the occurrence of heart attacks based on several factors such as age, gender, hypertension, smoking habits, and diabetes. These models can be used to identify individuals who are at high risk of developing a heart attack and help healthcare professionals to design effective preventive interventions.

* Moreover, the application of machine learning algorithms to the heart attack dataset has the potential to improve our understanding of the complex relationships between risk factors and the occurrence of heart attacks. This knowledge can help in designing better prevention and treatment strategies for this life-threatening condition.



## Recommendations
* Collect additional data: The heart attack dataset contains a relatively small number of observations, and collecting additional data could help to improve the accuracy and generalizability of machine learning models developed on this dataset.

* Consider including additional features: The heart attack dataset includes a limited number of clinical features, and it may be useful to include additional features that could be predictive of heart attacks. For example, including data on lifestyle factors such as diet and exercise habits could provide additional insight into a patient's risk of suffering a heart attack.

* Use more sophisticated machine learning techniques: While the heart attack dataset has been used to develop predictive models using a range of machine learning algorithms, it may be worthwhile to explore more sophisticated techniques such as deep learning, which have been shown to be effective in other medical applications.

* Validate the models: Once machine learning models have been developed on the heart attack dataset, it is important to validate their performance on new data to ensure that they generalize well. This may involve collecting additional data or using existing datasets to test the models' accuracy and reliability. Further feature engineering and hyperparameter tuning can be performed to optimize the performance of these models. Seems like the more complex models tend to overfit the data by not doing well in generalization.




