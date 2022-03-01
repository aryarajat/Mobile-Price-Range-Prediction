# **Mobile-Price-Range-Prediction**

## **Problem Statement**
In the competitive mobile phone market companies want to understand sales data of mobile phones and factors which drive the prices. The objective is to find out some relation between features of a mobile phone(eg:- RAM, Internal Memory, etc) and its selling price. In this problem, we do not have to predict the actual price but a price range indicating how high the price is.


In this project, we are going to explore and analyze a dataset which contains specifications of two thousand mobile phones and try to predict optimum price ranges for a list of mobile phones in the market by applying various machine learning algorithms such as support vector machine, xgboost, gradient boosting and k-nearest neighbors(knn).
## **Data Description**
* Battery_power - Total energy a battery can store in one time measured in mAh
* Blue - Has bluetooth or not
* Clock_speed - speed at which microprocessor executes instructions
* Dual_sim - Has dual sim support or not
* Fc - Front Camera mega pixels
* Four_g - Has 4G or not* 
* Int_memory - Internal Memory in Gigabytes
* M_dep - Mobile Depth in cm
* Mobile_wt - Weight of mobile phone
* N_cores - Number of cores of processor
* Pc - Primary Camera mega pixels
* Px_height - Pixel Resolution Height
* Px_width - Pixel Resolution Width
* Ram - Random Access Memory in Mega Bytes
* Sc_h - Screen Height of mobile in cm
* Sc_w - Screen Width of mobile in cm
* Talk_time - longest time that a single battery charge will last when you are
* Three_g - Has 3G or not
* Touch_screen - Has touch screen or not
* Wifi - Has wifi or not
* Price_range - This is the target variable with value of 0(low cost), 1(medium cost), 2(high cost) and 3(very high cost).ld text
## What is the business use case of your project?
Users can verify their trip details (distance, duration) and measure of bodily activities (burnt calories). With this kind of smart technology and convenience, the use of Rental bikes is increasing every day. So, there is a need to manage the bike rental demand and manage the continuous and convenient service for the users. This study proposes a machine learning based approach including weather data to predict whole city public bike demand. A ML model is used to predict the number of rental bikes needed at each hour.

## Conclusion
* First, we run Data Wrangling on our model to ensure that there are no null or duplicate entries in our dataset. Because there are so few outliers in the independent variable front camera, we can ignore it because it adds no complexity to our model.

* Following the Data Wrangling, we undertake the Exploratory Data Analysis, in which we find the correlation matrix for the dependent and independent variables. According to this correlation matrix, the most essential attributes in terms of mobile pricing range forecasts are Ram, Pixel height, Battery Power, Pixel width, Mobile Weight, and Internal Memory.

* In data visualization, we found that the ram is highly positively correlated with the dependent variable. If ram size increases then the mobile price also increases.

* In the next step, we perform the feature selection using the SelectKbest and take only those features whose score is greater than 9.

* For the prediction, we employ the four models. We chose the support vector machine over all other models since the SVM test accuracy is 98 percent. Even after adjusting, the gradient boosting model may be overfitting because there is no discernible difference in test accuracy when using alternative sets of hyperparameters. With hyperparameter adjustment, overfitting in XGBoost is reduced, although accuracy is lower than in SVM.
