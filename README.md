# Project-1


## Location Analysis

### Fraudulent transaction cardholder State

The database was filtered only by the fraud transactions (2145).
Then, the transactions were grouped by the cardholder state.
A choropleth map was created to show how the fraud transactions were distributed among the different states.
The map shows that the state with the highest number of fraudulent transactions is New York (175), followed by Pennsylvania (114) and Texas (113).

A chi-squared analysis was performed to confirm if the fraudulent transactions were not equally distributed among the states.
The p-value confirmed that the number of fraudulent transactions were higher in specific states and not distributed equally.

This result can help the identification and prediction of future frauds, targeting those states where the fraudulent transactions are more likely to happen.

### Fraudulent transaction merchant State

In this case also, only the fraud transactions were used for the analysis.
As the dataset only included merchant's latitude and longitude, the api Geoapify was used to obtain the State.
53 rows were removed from the analysis, as the latitude and longitude were in the middle of the ocean, therefore, no State was identified by the api.
Then the name of the merchant States was replaced by the codes, to make them comparable with the cardholder State on the original data.

The cardholder State was compared with the merchant State. When it was the same it was marked as true, and when different was marked as false.
The results were then counted, and a donut chart was prepared.

The chart shows that around 71% of the fraudulent transactions are performed with merchants located in the same State where the cardholder is located.
This finding can help to understand how that fraudulent transaction are more likely to happen in the cardholder State.
A transaction in a different State cannot be flagged immediately as a fraud and other factors should be taken into consideration. For example, legit transactions perform by the cardholder in that other State.

To take the analysis a bit further, the merchant State was identified for the top 3 cardholder States (New York, Pennsylvania, and Texas)
The bar chart confirms how most of the merchants were the fraudulent transactions happened, were located either in these three States or in States next to them, such as Connecticut, West Virginia, New Jersey, Oklahoma, Ontario, and Ohio.
