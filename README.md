
# 1. Introduction and Data Loading
The diabetes dataset used in this project is sourced from Kaggle. The dataset is originally from the National Institute of Diabetes and Digestive and Kidney Diseases. The objective of the dataset is to predict whether a patient has diabetes based on certain diagnostic measurements. The dataset consists of several medical predictor (independent) variables and one target (dependent) variable, Outcome. Independent variables include the number of pregnancies the patient has had, their BMI, insulin level, and age.


The dataset is loaded using the pandas library. The data file used is "diabetes.csv"


# 2. Understanding the Data
The code provides an overview of the data, including the names of the columns, data types of each column, the total number of records, and the number of columns. This is done using the info() function from pandas.

![Screenshot 2024-01-12 at 2 56 19 PM](https://github.com/Rashesh94263/Diabetes_Analysis_p1/assets/143764641/0e5b26ba-db6f-4ee4-8d34-29ffa5f040f5)



# 3. Observations
The data is then reviewed for any inconsistencies or errors. For example, it is observed that values for Glucose, Blood Pressure, SkinThickness, Insulin are 0, which is not possible in the real world. As part of the data cleansing exercise, all such records are dropped from the data frame.

# Correlation Analysis: 

![Screenshot 2024-01-12 at 3 09 19 PM](https://github.com/Rashesh94263/Diabetes_Analysis_p1/assets/143764641/bfedfa53-56b4-46b2-a527-ac48a614168b)



# 4. Data Analysis and Model Training
The project then proceeds with data analysis, feature selection, model training, and model evaluation steps. Various Python libraries such as pandas, numpy, seaborn, matplotlib, and sklearn are used for data manipulation, visualization, and machine learning.


- Let us draw a simple scatterplot by projecting outcomes based on two features Glucose and Insulin. 

- sns.scatterplot(data=df,x='Insulin',y='Glucose',hue='Outcome')
-  plt.show()

![Screenshot 2024-01-12 at 3 00 38 PM](https://github.com/Rashesh94263/Diabetes_Analysis_p1/assets/143764641/845781a4-94b3-4089-b07d-90ba1480c371)





# 6. Performance Metrics. 

The Diabetes Analysis project in the "Diabetes_analysis.ipynb" file uses several accuracy metrics to evaluate the performance of the machine learning models. These metrics include. 

    1. Accuracy Score: This is the simplest way to measure the performance of a classification model. It is calculated as the number of correct predictions divided by the total number of predictions.

  ![Screenshot 2024-01-12 at 3 03 36 PM](https://github.com/Rashesh94263/Diabetes_Analysis_p1/assets/143764641/c1e80768-9249-4d60-b41e-511289244520)


    2. ROC Curve and AUC: The Receiver Operating Characteristic (ROC) curve is a plot that illustrates the diagnostic ability of a binary classifier as its discrimination threshold is varied. The Area Under the Curve (AUC) provides an aggregate measure of performance across all possible classification thresholds.

    Output: 

  ![Screenshot 2024-01-12 at 3 04 57 PM](https://github.com/Rashesh94263/Diabetes_Analysis_p1/assets/143764641/e7ef199e-69fc-48db-8138-c0df37aade4e)



    3. Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared (R^2): These are typically used for regression models, but they can also provide useful insights for classification models. MSE is the average of the squares of the errors, MAE is the average of the absolute differences between the predicted and actual values, and R^2 is a statistical measure that represents the proportion of the variance for a dependent variable that's explained by an independent variable or variables in a regression model.

    Output:  we got very low MSE,MAE and R2 that clearly says our model got fitted good.

![Screenshot 2024-01-12 at 3 05 45 PM](https://github.com/Rashesh94263/Diabetes_Analysis_p1/assets/143764641/e9928e06-4d36-462f-9227-cddc76d195bd)
 




# 5.  Conclusion
The project concludes with the evaluation of the model's performance and the interpretation of the results.

# Summarize your findings and analysis
- According to our explodatory analysis we found some strong relationship with some features and based on that we tried to remove those featurs in our model training to improve model. 
- We tried different models and tried to check whether which strategy could give us good model accuracy.
- In the begining, simple model could not give us better prediction.
- Then, we tried Principle component anaysis but still we got not luck.
- Feature selection gave us good result so we decided to move forward with that.
- And after that, we used K-fold cross validation but that made our model over fitted.
- We tried GridsearhCV on top of that whehter we can improve model or not and that had been proven good option for us because we were able to achive 91.79% accuracy using random forest classifier.








