# Disease-Prediction



Step 1: READING DATA AND CONCATENATING TRAIN AND TEST DATA
After Reading my train and test data as a first step, I concatenated both on rows so that I can perform preprocessing and feature engineering on both my test and train sets at the same time.
Step 2: DATA PREPROCESSING AND EDA
•	First, I check for missing values in the training data and found that there are no missing values in the data.
 

•	Then I wanted to check the summary statistics of all my numerical variables and hence used describe method to print summary statistics.
 
•	Now as a third step I wanted to see if my training data is balanced or not and hence, I check the distribution of target variable in the training data. If the data is not balanced, I would have used the under sampling or oversampling techniques accordingly. I found that the data is almost if not perfectly balanced with 50-50 distribution of target variable.
 

Univariate analysis

 l used frequency table or bar plots for categorical features which will calculate the number of each category in a variable. For numerical features, I used probability density plots to look at the distribution of the variables.



Handling Outliers:

•	I wanted to see the outliers of numerical variables in detail and hence I printed the upper bound and lower bound of the box plots of each of the numerical variables along with their maximum value and median. 
•	I tried to compare the maximum value of these variables with median value and see if the difference is high and unusual. 

 
If we observe the above results the median value and maximum value of features height and weight , for height standard deviation is approx. 7, and  the max value is 8 standard deviations more , which is not too bad because there can be some very tall people in our population and these outliers may not be wrong observations. same is the case with feature weight, whose max value is 9 standard deviations more than median which also is possible because some patients may have overweight problem.
But when it comes to High blood pressure, max value is 16020 and median is 120, which is something wrong. a patient cannot have 16000 as his blood pressure value. from box plot we can observe that many outliers ate close to this value of 16000, which means all these values are errors similarly for low blood pressure the max value is 11000 where as median is 80, and from box plot observations many other outliers are close to this max value. even there very high values are errors because humans cannot have such high values as low blood pressures.

Therefore, for both High blood pressure and low pressure i will be treating my outliers by imputing any values more than the upper bound and less than the lower bound by median values of their respective columns
 
Then I plotted boxplots for these two variables to see if everything looks ok.

 
We see from above plot that there are no more outliers in these two variables.

After I have decided to come up with two new features 
1)	BMI: which is nothing but (weight in lbs)/Height in meter square
2)	HBPLBP: Which is nothing but sum of Low blood pressure and High Blood pressure.
After adding these two columns the new data frame looks like:
 
3)	I then dropped Height in meters column which I created for calculating BMI
4)	Then I plotted the corretion matrix between the variables.
I observed that there is significant correlation between
1)	High blood pressure and Low blood pressure 
2)	High blood pressure and Disease
3)	Low Blood Pressure and Disease
4)	Age and Disease
5)	BMI has correlation with height and weight
6)	HBPLBP has correlation with High blood pressure and Low blood pressure

 
ENCODING 
•	I have encoded nominal categorical using one hot encoding
•	I have encoded ordinal categorical variables by creating a numerical order.
 
 


