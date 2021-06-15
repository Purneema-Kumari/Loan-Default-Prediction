# Loan-Default-Prediction
There was a hypothetical bank which was facing the high credit default rate. So the strategy which the bank has come up with is to identify the risky customers. The objective of this project was to identify the characteristics and recommend suitable actions which will help the bank to reduce overall default rate.

**Business Problem:** 
To identify the risky customer using data.
To identify characteristics for default and suitable actions to reduce it.

The data contains 1000 rows and 21 variables. There are 13 categorical variables in these 21 variables. The variable Status is the dependent variable which describes the customers as Good Credit Risk (1) and Bad Credit Risk (2). Rest other variables are numerical variables. 

**Data Preprocessing:**
1. Reading the data in Python File and looking for data summary.
2. Finding missing values in the data.
Since the data do not contain any missing values, so we do not worry about that.
3. To plot boxplot for numerical values to see the presence of outliers.
The outliers were present in duration, amount and age variables.
Since the distribution of all these variables is positively skewed so the outliers were replaced by 75% Quartile + 1.5 IQR.
4. Once the data is free from missing values and outliers, data visualization was done to find insights from the data.
5. The categorical variables were ordinal variables so dummy variables were made for each of the categorical variable.

**Insights:**
1. Customers with num credits equal 2 and dependent equal to 2 are likely to default.
2. Around 1/3 of other debtors with label as 101 are likely to  default.
3. Credit history with label A30 and A31 have high rate of default.
4. Checkin_acc [A11] and foreign worker[A201] has default close to 50%
5. Also checkin_acc[A14] has least default rate despite being the most common account.
6. Installment plans is also a major factor in default.
7. Also it is not clear whether telephone is an important variable or not.
8. Also there is correlation between duration and amount.

**Model Building:**
After pre processing the data for missing values and outliers and creating dummy variables for categorical values.
Initially from the plot of variable status we can see that around 300 customers are defined as Bad Credit Risk or Defaulters.
There are 48 independent variables after encoding categorical variable.
The data was divided into train and test part which accounts for 80% and 20% of the data respectively.
After this I standardized all the variables before fitting the model.

I have used Logistic Regression for model building whose accuracy was 0.74.

**Solution:**
1. Help customers to maximize their cash flows along with streamlining their installment plans.
2. Explain the customers  impact of defaulting on credit score and how it can reduce the chance to receive credit in future.
3. Asking for additional information to better assess their default probability.
4. Negotiating and revising the payment structure and duration if the customer is likely to default.
5. Analyze whether it is the large amount or long duration which result in customer  defaulting on credit card.
6. Creating a basket or segmentation of customers in different groups on basis on age, job and property for better prediction of default.
7. Proper follow up and timely reminders can also reduce the probability of customer being defaulter.


