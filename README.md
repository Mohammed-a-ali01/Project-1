# Project-1  - Ali 

## Summary of Content 
merged.ipynb will be our analysis on what's next, comparing median income against the number of fraud. 

## Summary of Ideas
Resources contain: fraud_data (the full dataset), clean_data (the cleaned verision), and lastly the kaggle_income (The median income per state).

The goal is to accurately showcase the most active time per fraud in a 24-hour timeframe.
The analysis to show which months are most active. 

ANOVA will be used to see the significance of amount on fraud. 

Lastly, special holidays will be compared to see is there is most actively during that day.

## Analysis Time 
- Initially tran_data_time was seperated to create easier to follow code (date and time).
- To better understand the time analysis we must first compare the time and the Is_fraud columns.
- We can then move forward and gather the format of time as such %H%M.
- What we need lastly is to group both hours and fraud to arrive at a graph. 
- Once we both columns we can compare the time (in hours) to Is_fraud (0 = no fraud, 1 = fraud).
- We can deduce that the most fraud happens at night around (10pm - 3am).
![MohammedAli-Line-1](https://github.com/Mohammed-a-ali01/Project-1/assets/81397577/ffc79679-5539-4a08-b507-719ffbee448c)


## Analysis - Months
-  Calculating the months is very similar to the hours except we need to change our datetime format to $d%m%y.
-  We also need to define our months in a dictionary so we can use them later in our axis.
-  Lastly, we want to show our graph with which month has the most impact, and that would be August.
-  We can continue to analyze specific dates like Christmas or Halloween (dates: 2020-12-25, 2020-10-31), since the sample size is not large enough (> than 30) we decided not to move forward with it since there would be no significant impact on the results. 
-  ![MohammedAli-Bar-1](https://github.com/Mohammed-a-ali01/Project-1/assets/81397577/027ca14b-80f5-4a72-b313-21b0ba1194dd)

## Analysis - Date and Amount 
- Plotly was used to create a simple linechart to show the trend of where the most amount of fraud will be.
- Note that the fraud count and fraud are different, hence there is a difference in both factors.
- Once we compare both date and amt we can deduce that December has the most amt of fraud.
![MohammedAli-pLine](https://github.com/Mohammed-a-ali01/Project-1/assets/81397577/ba852979-fcaf-4a2e-ab72-cd57597b4205)

## Conclusion 
- 10pm - 3pm has the most fraud in time.
- August has the most fraud in months.
- December has the most amount of fraud.

Our aim is to suggest to a bank, customers and clients that they should be aware of these metrics to protect themselves against everyday fraud. 
