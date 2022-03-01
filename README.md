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
Cost prediction is the very important factor of marketing and business. This project assists new businesses in determining whether or not their customers require specific features. It is difficult for a new company to determine what pricing range to debut their mobile phones in and what features to offer in order to be successful. This concept provides companies with a wider view, allowing them to expand more quickly.
## Data Visualization
### 1) Heatmap
![image](https://user-images.githubusercontent.com/85746056/156106085-e5137a1e-7ecc-4239-9f79-fb109a4b9735.png)
* Feature variable Ram is highly correlated with the dependent variable. The variable Ram has more impact on the dependent variable as compare to other variables.
* The independent variable Front Camera and Primary camera are moderately correlated with each other. Similarly, 3G and 4G are also moderately correlated with each other.
* Screen width and screen height are also moderately correlated with each other. Similarly, pixel width and pixel height are moderately correlated with each other.
* We can see that the except ram the other variables battery_power, px_height, px_width also have some impact on the target variable.
### 2) Relationship between the Price Range and Internal Memory
![image](https://user-images.githubusercontent.com/85746056/156106231-d5602167-3730-49f2-b579-f74a90ff9d10.png)
* We can see from this jointplot of int memory and price range that price range does not steadily grow as internal memory increases. As a result, we can conclude that int memory has little influence on prediction.
### 3) Relation between the Clock Speed and Price Range
![image](https://user-images.githubusercontent.com/85746056/156106310-4a91d05b-af49-43f6-857e-5a5a543e298b.png)
* From this Point plot of clock speed versus price range, we can observe that price range does not progressively increase as clock speed increases. As a result, we can conclude that clock speed had little impact on the prediction.
### 4) The Number of Cores
![image](https://user-images.githubusercontent.com/85746056/156106388-310ddf00-fcdd-402e-9021-a95fde8ffb95.png)
* According to the above countplot, the quadcore(4 cores) category has the most mobiles.
* In comparison to other processors, the number of mobiles that use hexacore(6 core) CPUs is lower.
### 5) Relationship between Mobile_Weight and Price Range
![image](https://user-images.githubusercontent.com/85746056/156106433-182809a7-a01d-4298-8701-684b743b07e1.png)
* According to the boxplot above, the very high price group contains a lighter phone than the other pricing categories.

* The average weight of a mobile phone is close to 140 g.
### 6) Relation between Price Range and Battery Power
![image](https://user-images.githubusercontent.com/85746056/156106665-cba22561-7acb-410b-92e6-1481bd198789.png)
* We can observe from this Boxplot of battery power vs. price range that price range gradually increases as battery power increases. As a result, we can claim that battery power has a positive influence on prediction
* Average battery power is near about 1200 mah.

## Conclusion
* First, we run Data Wrangling on our model to ensure that there are no null or duplicate entries in our dataset. Because there are so few outliers in the independent variable front camera, we can ignore it because it adds no complexity to our model.

* Following the Data Wrangling, we undertake the Exploratory Data Analysis, in which we find the correlation matrix for the dependent and independent variables. According to this correlation matrix, the most essential attributes in terms of mobile pricing range forecasts are Ram, Pixel height, Battery Power, Pixel width, Mobile Weight, and Internal Memory.

* In data visualization, we found that the ram is highly positively correlated with the dependent variable. If ram size increases then the mobile price also increases.

* In the next step, we perform the feature selection using the SelectKbest and take only those features whose score is greater than 9.

* For the prediction, we employ the four models. We chose the support vector machine over all other models since the SVM test accuracy is 98 percent. Even after adjusting, the gradient boosting model may be overfitting because there is no discernible difference in test accuracy when using alternative sets of hyperparameters. With hyperparameter adjustment, overfitting in XGBoost is reduced, although accuracy is lower than in SVM.
