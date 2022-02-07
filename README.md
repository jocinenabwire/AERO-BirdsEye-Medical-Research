# AERO-BirdsEye-Medical-Research
## 1.0  BUSINESS UNDERSTANDING
### 1.1.  Business Overview 
Health is one of the sectors that is considered important all over the world and drug development is one of the areas that needs to be looked into.It has been noted that there has been waste and inefficiency which have become big problems when it comes to drug development. It is also estimated that quite a number of the trials are not completed, while others are entirely not done. All these can be hard to spot, especially when these companies are in the midst of these processes. 
It is in this view that this study seeks to analyze the records and find out more about the number of trials each sponsor carried out, the conditions that were on trial especially in regards to each sponsor and also the status of trials that were carried out(whether they were completed or not). Our findings will be used by the government  regulatory board to give proper directives to these companies in order to effect change.The impact of this study will help both the government regulators and the pharmaceutical companies in knowing the following;
- Which companies are dragging behind when it comes to the carrying out of the trials.
- Which are the most inefficient trials that companies shouldnt waste their time on.
- The conditions that are worth carrying trials on in order to direct more resources on them.
### 1.2. Business Objective
The main objective of our research is  to find out completed and withdrawn tests done by GSK (GlaxoSmithKline plc).Our other objectives are :
1. To investigate which sponsor had done the most trials.
2. To find which condition was most investigated.
3. To find which sponsor had done the most tests on condition X(which is the most tested condition).
4. To investigate which sponsor had the most successive completion of drug tests.
5. To find out which start year and start month had the most trials been done.
### 1.3. Business Success Criteria
 To figure out what were the completed and withdrawn tests done by GSK, which condition was most investigated and  which sponsor had done the most tests on which is the most tested condition.
### 1.4 Research Questions

1. Which sponsor had done the most tests/ investigation?
2. Which condition was most investigated?
3. Which sponsor had done the most tests on condition X(which is the most tested condition)?
4. Which sponsor had the most successive completion of drug tests?
5. Which start year and start month had the most tests/investigations?
### 1.5. Assessing the situation
#### 1.5.1. Resource Inventory
##### 1.5.1.1.Datasets 
i.Aero Birds Eye Dataset
##### 1.5.1.2.Software used
i.Google Collaboratory
ii.Pandas
iii.Numpy
iv.Trello
v.Git       
#### 1.5.2.Assumptions
The data provided is correct and up to date.
#### 1.5.3.Constraints
There are no constraints.
### 1.6.Data Mining Goals
Our data mining goals for this project are as follows.
1. Which companies are dragging behind when it comes to the carrying out of the trials.
2. Which are the most inefficient trials that companies shouldnt waste their time on.
3. The conditions that are worth carrying trials on in order to direct more resources on them.
### 1.7.   Data Mining Success Criteria.
My success criteria will be measured by the following criteria:
1. To find out completed and withdrawn tests done by GSK (GlaxoSmithKline plc)
2. To investigate which sponsor had done the most trials.
3. To find which condition was most investigated.
4. To find which sponsor had done the most tests on condition X(which is the most tested condition).
5. To investigate which sponsor had the most successive completion of drug tests.
## 2.0 DATA UNDERSTANDING 
### 2.1.Data Understanding Overview
For this project, we are using the available dataset for A Birds’ eye view of clinical trials.
The dataset link for Aero Bird Eye Clinical Trials  is here  link to the dataset.
### 2.2.Data Description
The dataset we chose provides information about different pharmaceutical companies such as  AbbVie, Bayer, Gilead, GSK(GlaxoSmithKline plc), Johnson & Johnson, Merck, Novartis, Pfizer, Roche, and Sanofi — over the past 20 years or so.
### 2.3.Verifying Data Quality
The data we had had null values and some missing data. We performed data cleaning  following the data integrity rules i.e Validity, Accuracy, Completeness, Consistency, Uniformity to ensure the data is ready for analysis. 
## 3.0 	DATA PREPARATION
These are the steps followed in preparing the data: 
### 3.1.Loading Data
Loaded datasets from the csv file.
### 3.2.Cleaning Data
During our cleaning we dropped the summary column since it was not necessary for our analysis.
We checked for outliers - We did not drop the existing outliers as they are true values of the data; the represent real time data

We also checked for duplicates but there were no duplicates.

For uniformity purposes: We changed from object type to date time, we also replaced the month numbers with the exact month names.
We exported our dataframe into a CSV file where we used to_CSV function to create a csv file and export it.
## EDA
### 4.1 Univariate analysis
For the Univariate analysis we calculated measures of central tendencies and dispersion. We also plotted bar graphs and histograms. The findings were as follows:
- Measures of Central tendencies 
- Measures of dispersion - We calculated variance, skewness, Kurtosis and quartiles.
1. Positive value means the distribution is positively skewed,i.e, skewed to the right.(Mean> Mode)
2. Kurtosis value is higher than that of the normal distribution thus leptokurtic,i.e, it is heavily tailed and outliers are present.
### 4.2 Bivariate analysis
On the bivariate analysis we plotted a heat map, scatter plots, line charts and a stacked column chart.
This is a summary analysis of the correlation coefficients in the dataset as below:
1. status and sponsor
correlation coefficient = 0.032792, which is greater than 0 indicating a positive relationship between the two variables. Since the coefficient is close to 0 the two variables have low correlation
2. condition and enrollment
correlation coefficient = 0.023968, which is closer to 0 indicating a positive relationship between the two variables
3. Enrollment and title
correlation coefficient = -0.024749, which is less than 0 thus there isa neagtive relationship between the two variables.
4. start year and start month
correlation coefficient = -0.019964,which is less than 0 thus there is a neagtive relationship between the two variables.
### 4.3 Multivariate analysis
Here, we did Linear Discriminant Analysis because we had a labeled dataset.
## Hypothesis Testing
- Null Hypothesis:  The number of completed tests done by GSK (​GlaxoSmithKline plc )was greater than or equal to the withdrawn tests.
H0 : Number of completed tests => Number of withdrawn tests
- Alternative Hypothesis: The number of completed tests done by GSK was less than the withdrawn tests.
H1 : Number of completed tests < Number of withdrawn tests

To conduct hypothesis testing, we used a z-test and calculated the p-value in order to either reject or accept the null hypothesis. Below are the reasons why I chose to use the z-test as the appropriate test statistic:
·       The sample size is greater than 30.
·       The standard deviation is known.
·       Data points are independent from each other.
·       The sample data has been randomly selected from a population, so each item has an equal chance of being selected.

Stratified sampling was used where grouping was made in regards to their status.
The level of significance used in the hypothesis testing is 0.05 or 5%. Therefore, if the p-value calculated from the test statistic is less than 0.05 then we reject the null hypothesis. If the value is greater than or equal to 0.05, we fail to reject the null hypothesis.

In conclusion of the hypothesis testing ,we found out With a  p value(1.0) is greater than the significance level(alpha=0.05) thus is not statistically significant and indicates strong evidence for the null hypothesis.We therefore fail to reject the null hypothesis thus there the number of completed tests done by GSK (​GlaxoSmithKline plc )was greater than or equal to the withdrawn tests.
## 6.0 CONCLUSION
We were able to find out the following;

GSK  was the sponsor that  had done more tests with a value of 2473.Followed by Novartis and Pfizer
Diabetes Mellitus, Type 2 was the most investigated condition followed by Breast Neoplasms ,Pulmonary Disease, Chronic Obstructive  ,Hypertension in that order.   
Sanofi had done the most tests on the most investigated condition that is Diabetes.
2007 had the most investigations done.
Gsk had the most successive completion of drug tests done followed by Novartis.
  	
## 7.0 RECOMMENDATIONS
The government  regulatory board can use this information to give proper directives to these companies in order to effect change.
More investigations should be made  on companies that are dragging behind when it comes to the carrying out of the trials.
Proper publishing of trials should be made to avoid wastage of resources and time by  the pharmaceutical companies.
More resources should be directed to conditions that affect more people.
