# Credit Card Fraud


## Main Question
Examine and analyze if different variables such as date, time, cardholder and merchant locations, cardholder age, amount, category and merchant are determining factors and can be used to predict credit card fraudulent transactions


## Analysis Subquestions
- What time or month is fraud occurring more
- Relation between cardholder and merchant locations in fraudulent transactions 
- Distribution of the fraudulent transaction amounts
- Average age of credit card fraud victim
- The highest number of frauds occurring in each category
- Compare the amount of fraud per merchant. 


## Data

### Main Data Set:
- Name: Credit Card Fraud Prediction
- Source: Kaggle
- Recency: 2020
- Shape: 555,719 rows and 22 columns
- Column examples: 'merchant', 'category', 'amt', 'state', 'dob', 'merch_lat', 'merch_long', 'is_fraud', 'Date','Time'.

### Data Cleaning/preparation:
- Using our file "cleaningcode.ipynb" we prepared a clean csv file for the analysis.
- Dropped column 'unix_time' (wrong data not matching)
- Split column 'trans_date_trans_time'
- Added calculated column: 'Age'

### Other Data Sets Used:
- Fred Economic Data

### APIs Used:
- Geoapify


## Presentation Link
- https://www.canva.com/design/DAF1wWMLQf8/Zsi6Nod73TdrR8x4kXAScg/edit


## Major Findings:

### Time and Date:
(see Notebook: 'Creditcard_time.ipynb')
- Hours 21 - 23 have the most fraud. This seems like an accurate statement as fraudulent transactions take place when people cannot react as quickly to them. 
- August has the most fraud. With over 400+ fraud counts during that amount.
- December has the most amount fraud.

### Location:
(see Notebook: 'Creditcard_location.ipynb')
- New York (175), followed by Pennsylvania (114) and Texas (113) are the states with the highest number of fraudulent transactions.
- In absolute terms, Alaska and Connecticut may not have many fraudulent transactions, but the fraudulent transactions represent more than 1% of their total number of transactions.
- Around 71% of the fraudulent transactions are performed with merchants located in the same State where the cardholder is located.

### Amount:
(see Notebook 'Creditcard_amount.ipynb)
- For total transactions, the transaction count percentage decreases with purchase amount increases.
- For fraudulent transactions, the transaction count percentage increases comparing to total transactions.
- The percentage of purchase amount count of total transactions decreases when the purchase amount increases especially greater than $400.
- In contrast to total transactions, the percentage of purchase amount count of fraudulent transactions increases with the the purchase amount increases especially at $300-400 and greater than $700.

### Age:
(see Notebook: 'Creditcard_age.ipynb')
- The average age of credit card fraud victims, shows a left-skewed distribution which suggests that there are relatively few instances of older individuals being victims of credit card fraud, with most victims being younger.
- However, the frequency in transactions is more frequent in elderly fraud victims, suggesting that they are more likely targets.

### Category:
(see Notebook: 'Creditcard_category.ipynb')
- The top 3 categories with the highest incident of fraud is shopping net, grocery pos, misc net.


## Final Conclusion
- We were able to identify how the majority of the fraudulent transactions falls under specific characteristics among the different variables analyzed. Therefore these variables can be used, with further analysis, to create a predictive model. 


## How to Run
- Download the repository.
- Create a folder called "Resources" within the repo folder "Project-1-main".
- Download the resources from the google drive https://drive.google.com/drive/folders/1SHJT23DdEPBBs0kaS0cqE71lcLufb2ha?usp=drive_link.
- Save the csv files into the "Resources" folder.


## Limitations
- Data was limited to the year 2020. This data can be affected by the pandemic.
- Data did not include a whole year of information.
- We did not count with other characteristics of the cardholders such as income or education level.
- There was no data about the purchased item.


## Project Execution
- Mohammed Ali: Time and Date Analysis
- Daniel Molina Valencia: Location Analysis
- Michael Elkabas: Age Analysis
- Yi Wen: Amount Analysis
- Olamide Usman: Category Analysis


## Credits Data Set:
- Kaggle: Kelvin Kelue: https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction/data