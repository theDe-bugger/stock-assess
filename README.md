# Stock-Assess
LTSM-based machine learning model to predict changes in stock prices for Apple (AAPL)

Check [analysis.ipynb](https://github.com/theDe-bugger/stock-assess/blob/main/analysis.ipynb) for the various graphs, model, and full data analysis.

# Motivation
Wanting to apply my interests in the stock market and machine learning, I decided to learn how to build a mdoel to predict stock prices for Apple. My objective was to learn how this was done, so I followed a tutorial and adjusted different parts to what I wanted.

# Process
## 1. Data Collection
Imported data for the past year for Meta, Apple, Amazon, Netflix, and Google from Yahoo Finance Library, and used pandas to setup data in valid format.


## 2. Exploratory Time Series Analysis
Used matplotlib pyplot to plot several graphs and visualize the various data points for each stock:
* Closing prices of all 5 FAANG stocks
![image](https://user-images.githubusercontent.com/39176231/220396417-d25ff463-e2bd-4bbb-b17a-fe30128c83ee.png)

* Total volume of stock being traded each day
![image](https://user-images.githubusercontent.com/39176231/220396439-e233715b-6b77-4278-9886-1a107bc21a61.png)

* Adjusted Close and Moving average (10 days, 20 days, and 50 days)
![image](https://user-images.githubusercontent.com/39176231/220396617-70943a55-93f6-44e1-94e2-6e5ac05ed683.png)

* Percentage Change for each day
![image](https://user-images.githubusercontent.com/39176231/220396649-62b8cf7e-589e-40ad-981f-6224963a1b63.png)

* Daily Returns
![image](https://user-images.githubusercontent.com/39176231/220396671-6a2a2b31-b396-4460-acbd-56fdb94c076d.png)


## 3. Correlation and Comovement Analysis
* Compared daily returns of each company with others using seaborn pair grid
![image](https://user-images.githubusercontent.com/39176231/220397546-b02489a4-bb9c-4782-8a84-6c7afcc86ab4.png)

* Created heat map to show correlation of stock closing price between companies
![image](https://user-images.githubusercontent.com/39176231/220482390-985e0e52-ed0b-4080-8baa-a657849e8a64.png)

## 4. Risk Assessment
Standardized returns and compared the scaled returns of each company to the level of risk each stock posed. Apple being the least risk, highest reward.
![image](https://user-images.githubusercontent.com/39176231/220482310-4b92145c-771b-40a1-8094-d01285b4616e.png)


## 5. The Machine Learning Model
Achieved a root mean squared error of $6.46 by appyling long short term memory recurrent neural network to better predict stock priced based on historical data. 
Used data from past year(Jan 13 2022) up to 60 days from current day to train the model.
Used past 60 days to test the model predictions.
Calculated root mean squared error to best depict deviation and it turned out to be $6.46 which is very accurate.
![image](https://user-images.githubusercontent.com/39176231/220398540-7ae2cc5b-7092-4a39-a623-573a2ac40e72.png)

# Next Steps
Overall, this was a great learning experience, but going forward, I will attempt to create models that can optimize pricing for products to maximize profits.
