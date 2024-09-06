# Main question
Examine and analyze if different variables such as date, time, cardholder and merchant locations, cardholder age, amount, category and merchant are determining factors and can be used to predict credit card fraudulent transactions


# Analysis Subquestions

- What time or month is fraud occurring more
- Relation between cardholder and merchant locations in fraudulent transactions 
- Distribution of the fraudulent transaction amounts
- Average age of credit card fraud victim
- The highest number of frauds occurring in each category
- Compare the amount of fraud per merchant. 

# Data

## Main Data Set:
- Name: Credit Card Fraud Prediction
- Source: Kaggle
- Recency: 2020
- Shape: 555,719 rows and 22 columns
- Column examples: 'merchant', 'category', 'amt', 'state', 'dob', 'merch_lat', 'merch_long', 'is_fraud', 'Date','Time'.
- Data Cleaning/preparation:
Drop column 'unix_time' (wrong data not matching)
Split column 'trans_date_trans_time'
Added calculated column: 'Age'

## Other data sets used:
- Fred Economic Data
## APIs used:
- Geoapify


# Major Findings and Conclusions:

# Time and Date:
(see Notebook: 'Creditcard_time.ipynb')
- Hours 21 - 23 have the most fraud. This seems like an accurate statement as fraudulent transactions take place when people cannot react as quickly to them. 
- August has the most fraud. With over 400+ fraud counts during that amount.
- December has the most amount fraud.


## Summary of Content 
merged.ipynb will be our analysis on what's next, comparing median income against the number of fraud. (NOT COMPLETE, extra step).

## Summary of Ideas
Resources contain: fraud_data (the full dataset), clean_data (the cleaned version), and lastly the kaggle_income (The median income per state).

The goal is to accurately showcase the most active time per fraud in a 24-hour timeframe. The analysis to show which months are most active. ANOVA will be used to see the significance of amount on fraud. Lastly, special holidays will be compared to see if there is most activity during that day.

## Analysis Time 
- Initially tran_data_time was separated to create easier to follow code (date and time).
- To better understand the time analysis we must first compare the time and the Is_fraud columns.
- We can then move forward and gather the format of time as such %H%M.
- What we need lastly is to group both hours and fraud to arrive at a graph. 
- Once we have both columns, we can compare the time (in hours) to Is_fraud (0 = no fraud, 1 = fraud).
- We can deduce that the most fraud happens at night around (10pm - 3am).

![MohammedAli-Line-1](https://github.com/Mohammed-a-ali01/Project-1/assets/81397577/ffc79679-5539-4a08-b507-719ffbee448c)

## Analysis - Months
- Calculating the months is very similar to the hours except we need to change our datetime format to $d%m%y.
- We also need to define our months in a dictionary so we can use them later in our axis.
- Lastly, we want to show our graph with which month has the most impact, and that would be August.
- We can continue to analyze specific dates like Christmas or Halloween (dates: 2020-12-25, 2020-10-31), since the sample size is not large enough (> than 30) we decided not to move forward with it since there would be no significant impact on the results.

![MohammedAli-Bar-1](https://github.com/Mohammed-a-ali01/Project-1/assets/81397577/027ca14b-80f5-4a72-b313-21b0ba1194dd)

## Analysis - Date and Amount 
- Plotly was used to create a simple line chart to show the trend of where the most amount of fraud will be.
- Note that the fraud count and fraud are different, hence there is a difference in both factors.
- Once we compare both date and amt we can deduce that December has the most amt of fraud.

![MohammedAli-pLine](https://github.com/Mohammed-a-ali01/Project-1/assets/81397577/ba852979-fcaf-4a2e-ab72-cd57597b4205)

## Conclusion 
- 10pm - 3pm has the most fraud in time.
- August has the most fraud in months.
- December has the most amount of fraud.

Our aim is to suggest to a bank, customers, and clients that they should be aware of these metrics to protect themselves against everyday fraud.

## Location:
(see Notebook: 'Creditcard_location.ipynb')
- New York (175), followed by Pennsylvania (114) and Texas (113) are the states with the highest number of fraudulent transactions.
- In absolute terms, Alaska and Connecticut may not have many fraudulent transactions, but the fraudulent transactions represent more than 1% of their total number of transactions.
- Around 71% of the fraudulent transactions are performed with merchants located in the same State where the cardholder is located.

# Amount:
(see Notebook 'Creditcard_amount.ipynb)
- For total transactions, the transaction count percentage decreases with purchase amount increases.
- For fraudulent transactions, the transaction count percentage increases comparing to total transactions.
- The percentage of purchase amount count of total transactions decreases when the purchase amount increases especially greater than $400.
- In contrast to total transactions, the percentage of purchase amount count of fraudulent transactions increases with the the purchase amount increases especially at $300-400 and greater than $700.

# Carholder's age:
(see Notebook: 'Creditcard_age.ipynb')
- The average age of credit card fraud victims, shows a left-skewed distribution which suggests that there are relatively few instances of older individuals being victims of credit card fraud, with most victims being younger.
- However, the frequency in transactions is more frequent in elderly fraud victims, suggesting that they are more likely targets.

# Category:
(see Notebook: 'Creditcard_category.ipynb')
- The top 3 categories with the highest incident of fraud is shopping net, grocery pos, misc net.

## Final Conclusion
- We were able to identify how the majority of the fraudulent transactions falls under specific characteristics among the different variables analyzed. Therefore these variables can be used, with further analysis, to create a predictive model. 

# How to run
Simply download the repository.
The csv files are present within the Resources folder.

# Limitations
- Data was limited to the year 2020. This data can be affected by the pandemic.
- Data did not include a whole year of information.
- We did not count with other characteristics of the cardholders such as income or education level.
- There was no data about the purchased item.
=======
# Creditcard Fraud Prediction 
How everyday businesses, customers and clients can be mindful of everday fraud that happens.

## Description 
The main purpose of this project is to educate customers of any bank in America that fraud can happen. It is best to understand the metrics behind them. For our purpose, we will be using the **fraud_test.csv file** to explore the insight behind it. **We will be mainly analyzing the following questions:**

- What time is fraud occurring more at (morning or night)?
- Amount of fraud based on geography.
- Average age of credit card fraud victim.
- The highest number of fraud occurring in each category.
- The fraud per merchant. 

## Getting Started
**Dependencies:**

- pandas
- plotly.express
- scipy.stats
- requests
- json
- matplotlib.pyplot

**Operating System:**
- Windows 10 or 11

## Installing 
Download should be done from the main file. Ideally, file opening should be done from ("Resources/fraud_test") or clean_data.

## Executing the program 
Step-by-step bullets

## Help
Time analysis seems to crash after running the last command on plotly (sometimes it does, sometimes it doesn't).

## Authors:
Kaggle:
Kelvin Kelue: [Kaggle Dataset](https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction/data)

## Version History 
