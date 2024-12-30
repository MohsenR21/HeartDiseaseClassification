
---

# Classification for the two classes of heart disease dataset
### introduction
This project aims to classify the heart disease dataset using methods such as K-Nearest Neighbors, Logistic Regression, and Decision Tree classifiers. We evaluate each model both before and after tuning using metrics including accuracy, precision, recall, confusion matrix, ROC curve, and AUC. In addition to evaluating the data for imbalances, we applied an ensemble model such as Simple and Hard Ensemble, Random Forest and Gradiand Bossting, because the previous models do not give an answer close to each other. Finally, we interpret that each feature has a greater impact on the model by Shap Values framework.



### Dataset 
This is a multivariate type of dataset which means providing or involving a variety of separate mathematical or statistical variables, multivariate numerical data analysis. It is composed of 14 attributes which are:
+ age
+ sex
+ chest pain type
+ resting blood pressure
+ serum cholesterol
+ fasting blood sugar
+ resting electrocardiographic results
+ maximum heart rate achieved
+ exercise-induced angina
+ oldpeak
+ ST depression induced by exercise relative to rest
+ the slope of the peak exercise ST segment
+ number of major vessels
+ Thalassemia 

### Column Descriptions of the dataset:

+ id(Unique id for each patient)
+ age (Age of the patient in years)
+ origin (place of study)
+ sex (Male/Female)
+ cp (chest pain type) [typical angina, atypical angina, non-anginal, asymptomatic.]
+ trestbps: resting blood pressure (resting blood pressure (in mm Hg on admission to the hospital))
+ chol (serum cholesterol in mg/dl)
+ fbs (if fasting blood sugar > 120 mg/dl)
+ restecg (resting electrocardiographic results)  [normal, stt abnormality, lv hypertrophy]
+ thalach: maximum heart rate achieved
+ exang: exercise-induced angina (True/ False)
+ oldpeak: ST depression induced by exercise relative to rest
+ slope: the slope of the peak exercise ST segment
+ ca: number of major vessels (0-3) colored by fluoroscopy
+ thal:[normal; fixed defect; reversible defect]
+ num: the predicted attribute
### Goal
 One of the major tasks on this dataset is to predict based on the given attributes of a patient that whether that particular person has heart disease or not and other is the experimental task to diagnose and find out various insights from this dataset which could help in understanding the problem more.

## Results Interpretation
### Importance of features
In this project, the impact of various features on the diagnosis of heart disease using the Shap Values module has been examined. The results obtained from the beeswarm plot are presented for two different models, including random forest and gradient boosting classifier. 

In the analysis related to the gradient boosting classifier model, several prominent features have been identified, including 
thalch, oldpeak, cp-atypical angina, chol, cp-non angina, and sex, which significantly affect the model's performance.Specifically, the thalch feature, when increased or decreased, equally impacts the model negatively. This indicates that this feature acts as a negative indicator for the occurrence of heart disease. Conversely, an increase in the oldpeak value has a positive effect on the model and may represent the likelihood of developing heart disease. In contrast, the cp-atypical angina feature has opposing effects on the model, such that low levels of it can be considered a sign of the presence of heart disease.
In the analysis related to the random forest model, the features thalch, oldpeak, cp-atypical angina, chol, age, cp-non angina, and sex have a significant impact on the model. The importance of these features is similar to that of the features in the gradient boosting classifier model, with the exception that the ranking of some features, such as age, has shifted in terms of importance. The same interpretations provided above also apply here.

Overall, this analysis indicates that certain features are significantly important in machine learning-based modeling for predicting heart disease, and understanding these relationships can facilitate improvements in the diagnosis and treatment of these concerning conditions.


