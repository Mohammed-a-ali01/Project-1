# Project-1
Problem Statement: Detect fraudulent transactions in credit card data.
Datalink: https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction
The above data has been cleansed and presented in a new file. 
The data that is used in this analysis is located in the Resources folder, called clean_data.csv

The aim is to showcase our ability to clean and present data in a manner that is easily understandable. 
The 4 main questions revolve around day, time, state, city, age and category. 
The plan on analyzing these categories is to better explain any correaltion and/or insight.

This code unser Creditcard_age.ipynb will focus on the average age of credit card fraud victim. 
Show the number of fraud happening, show the frequency and perfrom hypothesis testing. 

Section 1: Shows a Bar Chart based on the age distribution
Overall, this segment filters fraudulent transactions, calculates the average age of fraud victims, 
and then visualizes the age distribution of those victims using a histogram. 

Section 2: Shows a Bar Chart based on number of fraudulent transactions per age catagory
Overall, this code segment categorizes the ages of individuals into predefined age groups, 
filters fraudulent transactions in order to count the number of fraudulent transactions in each age category. 
It then visualizes the results using a bar plot.

Section 3: Shows a Bar Chart based on the frequency of fraud based on Age
Overall, this code segment categorizes the ages of individuals into predefined age groups, filters fraudulent transactions, calculates the rate of fraudulent transactions per age category, and visualizes the results using a bar plot.

Section 4: Perform a Char Hypothesis. Overall, this code segment calculates the chi-square statistic and p-value to assess the independence between age categories and fraudulent transactions, providing insights into whether there is a significant association between these variables.



