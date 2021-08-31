# Heart-Disease-Prediction
Every year millions of deaths occur all over world due to heart related conditions. If we can predict beforehand whether any given person will have a heart related problem in the near future, it can be easily overcome by changing their lifestyle or by taking other precautionary measures. The goal of this project is to predict all the important factors which leads to diagnosis of heart diseases and how likely the person in question is to suffer from it in the next 10 years.
For data, we have used the Framingham Data set. Framingham Heart study is a long-term and ongoing cardiovascular study of the residents of Framingham city which is located in Massachusetts. The main aim of this project is to develop a working model which will take all the variables given in this dataset and try to predict whether the given person will have a heart disease or not based on the different factors used in the model.

Logistic Regression will be used for prediction as both, the outcome and the structure of data in the dataset, are in binary format. It will have the following steps:
1. Descriptive Data Analysis
2. Logistic Regression Model Creation and Interpretation
3. Model Evaluation
4. Final Prediction


## **Step 1: Descriptive Data Analysis**
- _Data Preparation_: In this step, first we prepare data by checking data types, duplicate values and rows with missing values if any. Missing values were found which constituted 12% of the dataset and hence were removed for better results.
- _Numerical Summary_: [image](https://user-images.githubusercontent.com/25548019/131576336-ad878baf-5477-4608-aaf8-d5c2c1a4dfaa.png)

In Numerical Summary, we check for 50% (mean) values whether they are symmetrical which can suggest that the data is normal and there is no unusuality.
- _Graphical Summary_: [image](https://user-images.githubusercontent.com/25548019/131576556-13e92bea-b3f1-4f80-9309-ce0950a5a68a.png)

The curve of each variable resembles to that of a normalized data, hence we can go ahead with performing Logistic Regression on the data.


## **Step 2: Logistic Regression Model Creation and Interpretation**
- _Baseline Model_: [image](https://user-images.githubusercontent.com/25548019/131576920-b4be90ec-8ea2-4697-b923-c8d3e54a36de.png)

First, we create a model which considers all the variables, regardless of how strongly or weakly they are correlated to developing CHD (Coronary Heart Disease).


- _Backward Selection Model_: [image](https://user-images.githubusercontent.com/25548019/131577022-eb8473f7-7b47-44ec-9313-29110750f1d6.png)

In this model, we only consider variables which contributes to developing the heart disease and eliminate all other nonsignificant variables to make the model more efficient. (Baseline models are only used to create better models and not actually predict something for most of the cases).


- _Interpretation of the model_: [image](https://user-images.githubusercontent.com/25548019/131577135-051d1ac8-d419-478f-acc6-3fdea8512bab.png)

Based on the model interpretation output, we can interpret that:

i. All the changes in the variable noticed are based on the keeping all the other features or variable constant.

ii. From the Odds Ratio of the Male variable it is seen that Males are 78.8% more likely to get a heart disease compared to that of female.

iii. Similarly, every year a person grows older, his/her chances of getting a heart disease rise by 7% (1.067644)

iv. Also, for every extra cigarette a person smokes, his/her odds of getting CHD increase by 2%.

iv. There is minimal increase in the chances of getting a CDH for increase in the variable values of cholesterol, systolic BP and glucose.

v. Also, as we can see after splitting the data into training and test data the accuracy of the model, we created is 0.8696 which means that the model predicts the outcome of
having a CHD accurately 88% of the time.


## **Step 3: Model Evaluation**

[image](https://user-images.githubusercontent.com/25548019/131577444-689edf7f-d5f8-4a8b-9df1-2b4319b856cd.png)

The accuracy of the model is approximately 87% which can be considered a good prediction model. A confusion matrix is also created in order to the evaluate the model more thoroughly. Some terms to keep in mind as we evaluate are:
 - Accuracy: Accuracy is the proportion of cases correctly classified by the model. It ranges
 from 0 to 1 (the higher the better).
 - Specificity (True Negative rate): Correct negative predictions divided total negatives.
 - Sensitivity (True Positive Rate) : Correct positive predictions divided by total positives.
 - Precision: Percent of 1’s predicted as 1 by the model.

_ROC and AUC_: [image](https://user-images.githubusercontent.com/25548019/131577666-026441f3-179c-4003-9b44-2c9548c33261.png)

ROC (Receiver operating characteristic) Curve is just a plot which shows how much more true positives are than false positives, which is a way to interpret that the model is good. In terms of evaluation by numbers, we use AUC (Area under curve) which just shows the are under the ROC Curve (the higher the
better).

The AUC Curve is 0.67 in a 0 to 1 scale which indicates a good model.


## **Step 4: Final Prediction**

![image](https://user-images.githubusercontent.com/25548019/131577762-8946d851-34bb-434e-80f7-a4c0ab94fdb7.png)

This is the final prediction where 0 indicates the probability of not having a heart disease and 1 is the probability of having the heart disease for a particular person in the next 10 years. 

It is important to note that the dataset was initially split into Train(90%), Validate(5%) and Test(5%) dataset. The Final Prediction consists of predictions made from the test dataset.


## **Conclusion**

The **Backward Selection Model** is selected as it produces more accurate output than the Baseline Model. The model can be used on any new data and would be extremely helpful to predict the disease beforehand and act on it in a timely manner to reduce the effects or avoid suffering form it altogether.
