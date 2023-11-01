# machine_learning_project-supervised-learning

By: Brigitte Sullivan</br>
Submitted on: Wednesday November 1, 2023</br>
Lighthouse Labs Data Science Program</br>

---
## Project Outcomes

1. Develop two different supervised machine learning models that will predict if a patient has diabetes. One of the models which will use ensemble learning and will use hyperparameter tuning. 
2. Compare the results of the different models and determine the best performing model at predicting whether a patient has diabetes. 


### Project Description:

In this project, I will apply supervised learning techniques to a real-world data set and use data visualization tools to communicate the insights uncovered from the analysis.

The steps performed in this project were

1. EDA - Exploratory Data Analysis
* import and clean data set
* visualize the relationships between variables
* handle missing values and outliers

2. Preprocessing & Feature Engineering
* Scaling the numeric features
* address imbalanced data in the Y variable. 
3. Training ML Model:
* develop two ML models, 
    * logistic regression, 
    * one DecisionTree (as baseline), followed by Random Forrest with hyperparameter tuning using GridSearchCV.
* Compare their performance using appropriate evaluation metrics such as accuracy, precision, recall, F1-score, and ROC-AUC.

4. Conclusion (Summary of Findings)
Here are a few findings from the analysis conducted:
    **1. Finding 1: How to select the best model? And Which model is 'best'?**
* 
    * In this scenario, we want to favour the model that best predicts if someone has diabetes. More specifically, we want the model that best diagnoses diabetes correctly. We are less concerned about corectly predicting if someone does not have diabetes. Since Recall is the metric that measures how often the model correctly predicted that someone did have diabetes. The model with the highest recall value will be the 'best' model. In this case, the random forest model performed slightly beter than the logistic regression model. 
    * A recall score of 58% indicates the model is decent at predicting diabetes. Coupled with a realistic accuracy score of 74%, the optimized Random Forest model performs well for our purposes. Though the baseline Random Forest performs nearly just as well</br>

    **2. Finding 2: Why is precision higher than recall for Outcome = 1**</br>
    * Precision is higher than recall in the logistic regression model for example because it incorrectly predicted someone having diabetes 48 times, compared to 36 correct predictions of diabetes. 
    * Recall completely ignores the "0" class, and only looks at how many times it correctly predicted someone having diabetes. 
    * In the end it incorrectly predicted someone having diabetes more often than correctly, which leads to a low recall. if Recall = 50% this would mean that it's can correctly predict that someone has diabetes and they actually have diabetes 50% of the time. The other 50% it predicts no diabetes when someone actually does have diabetes. 

    **3. Finding 3 - "what is zero?"**</br>
    * Although no missing values were found in the data. Due to low domain knowledge, It's unclear what the meaning of a "0" could be in the data set, and that these "0" may be missing values however would need a subject matter expert to confirm the validity of zeros in the  features like Insulin, Glucose, SkinThickness. I was able to assume that a BMI of zero was impossible and replace those records with the median value, hoever this didn't do much to change the results.

    **4. Finding 4 : Room for improvement with optimization**</br>
    * After performing optimization on Randmom forest, the best model came back almost identical to the baseline RandomForest model. Indicating that the models developped are already optimized since the results are not changing significantly. 


**Data Souce:**</br>
The data set for this project is the "Diabetes" dataset from the National Institute of Diabetes and Digestive and Kidney Diseases 



