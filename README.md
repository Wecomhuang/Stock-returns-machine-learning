# Stock-returns-machine-learning
Using various supervised machine learning algorithms to predict stock returns

**In Part 1, raw data was obtained from various sources.** <br>
Tickers of all stocks listed on America's three stock exchanges: NYSE, AMEX and NASDAQ, were obtained from the NASDAQ Stock Screener. <br>
_Refer to nasdaq_screener_1672920378111.csv_

Historical prices and therefore historical returns were obtained from yfinance. <br>
Historical 10-year returns from beginning of Jan2010 to beginning of Jan2020 was chosen as the learning label, noting that these were not peaks or troughs in the business cycle. <br>
_Refer to start_price.csv and end_price.csv_

Fundamental data were downloaded from S&P Capital IQ and used as features to predict effective annual return. These fundamental data are: Total revenue, ROA, ROE, GPM, EDITDAM, NPM, Auditor opinion, Asset turnover, CR, DSO, DIO, DPO, D/E, 1-yr revenue growth, 1-yr net profit growth, 1-yr cash flow from operations growth, 1-yr asset growth, EBITDA, payout ratio, cash and short term investments, net PPE, goodwill, RE, TBV, net debt, contingent liabilities, CFO, cash from investing, net change in cash.

**In Part 2, raw data were organised and cleaned into appropriate data types.** <br>
There are a total of 2,839 stocks to be used in machine learning. <br>
_Refer to cleaned stockdata.csv_

**In Part 3 and 4, exploratory data analysis was performed on the data, offering some insights into the data.**

**For machine learning, classification models were used to predict if returns would be positive or negative.**

**In Part 5, linear regression was performed.** <br>The best linear regression model (with sequential feature selection (forward) (22 features)) had RMSE of 0.15265919047250745, against y_test mean of 0.06442245133568081.

**In Part 6, logistic regression was performed.** <br>The best logistic regression model (with sequential feature selection (backward) (45 features)) had accuracy of 0.82 and weighted avg f1-score of 0.79.

**In Part 7, K nearest neighbors was performed.** <br>The best K nearest neighbors model (K=5, with all 91 features including all dummy variables) had accuracy of 0.80 and weighted avg f1-score of 0.78.

**In Part 8, decision trees and random forests were performed.** <br>The best model (random forest with recursive feature elimination with all dummy variables (45 features)) had accuracy of 0.80 and weighted avg f1-score of 0.78.

**In Part 9, support vector classifier and regressor were used.** <br>
The best support vector classifier model (C=10, gamma=0.1, kernel='poly', with all 91 features including all dummy variables) had accuracy of 0.79 and weighted avg f1-score of 0.76. <br>
The best support vector regressor model (C=0.1, gamma=1, with all 91 features including all dummy variables) had RMSE of 0.14332614018148276, against y_test mean of 0.06442245133568081.

**In Part 10, artificial neural networks regression and classification models were used.** <br>
The best artificial neural networks classification model (adam optimizer, 86 epochs (with early stopping callback), with dropout layers, with all 91 features including all dummy variables) had accuracy of 0.81 and weighted avg f1-score of 0.79. <br>
The best artificial neural networks regression model (adam optimizer, 115 epochs (with early stopping callback), with dropout layers, with all 91 features including all dummy variables) had RMSE of 0.14088905052298825, against y_test mean of 0.06442245133568081.
