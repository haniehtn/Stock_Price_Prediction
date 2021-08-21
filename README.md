# Stock_Price_Prediction

First Part

The purpose of this part is to design and use a model to accurately predict the price of three commodity items (a combination of currency and precious metal) according to their cost over time.
The data set contains information collected every five minutes so that each time, the last 200 records related to the new prices of 3 target items and other statistics are recorded and stored.

The columns of the Market Summary file include the following in order: (The name of this file for item A is A_trades)
1. Maximum order price registered for sale 
2. Maximum order volume registered for sale
3. Maximum order price registered for purchase. 
4. Maximum order volume registered for purchase
5. Price of the last market transaction 
6. Daily trading volume
7. Minimum daily price 
8.Maximum daily price

The columns of the Transaction file include the following in order:
The first column is the time of recording information collected with a resolution of 5 minutes. Each transaction is marked with four numbers. Unique Id for each transaction. Trading time in milliseconds. Transaction volume and transaction price. For each moment, the specifications of 200 transactions have been registered. Therefore, the file contains 4 * 200 columns, and all four columns related to a transaction are listed in order.

The file columns related to registered orders include the following:(The name of this file for commodity A is A_book.) 
The first column is the time of recording information collected with a resolution of 5 minutes. Registered orders are presented as a histogram of the market situation, and the whole histogram is presented as 50 bin (bin 20 up and 20 below the original price). Each bin includes the number of registered orders related to this price and the volume of the registered order associated with this price. Therefore, this file contains 3 * 25 columns, all three columns related to a bin of the registered orders, and are mentioned in the order. When, for any reason, incorrect information is collected for the above information, the value line -1 is entered.
Finally, a model is obtained to predict the price of currency/commodities for the next 5, 10, 15, ..., and 50 minutes.

Second Part

The purpose of this section is to provide a model for predicting market trends. These models are trained for several stocks in the Iranian stock market. This data is collected daily and includes the date, first price, highest price, lowest price, final price, value, volume, opening price, and price of the last transaction.
Finally, this model predicts the increase or decrease of the desired share price for the next day and offered to buy or sell accordingly.

Separate train and test files created for both parts and the trained models saved and read-only for evaluation. Also, the test file reads the input from the CSV file and saves the corresponding output in another CSV file.
