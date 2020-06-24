# Machine learning stock prediction model
I'm not desperate or anything, but please, please, please, please hire me. 
All joking aside here is my first real project. 

I'd like to thank sentex's video tutorial on youtube for inspiration and for supplying very useful training data. 
Finding historical data on stocks (for free) that I would use to train my model have proved to be difficult to say the least. 
However, sentex provided a sample dataset, "straight HTML data as if you had parsed Yahoo Finance for over a decade." called intraQuarter.zip. 

Data:

  It turns out, the machine learning part of a machine learning project is by far the easiest part. 
  The hard part is getting your hands on the necessary data. We need three datasets:
  
    1) Historical Stock Statistics and Prices Training Features and labels
   
    2) Historical S&P500 Prices: Benchmark to compare prices with  
    
    3) Current Stock Statistics and Prices: Testing Features and Labels

Historical Stock Statistics:

    Utilizing Beautiful Soup we first scrape intraQuarter.zip for the following features.
    
     'Market Cap'
      Enterprise Value
      Trailing P/E
      Forward P/E
      PEG Ratio
      Price/Sales
      Price/Book
      Enterprise Value/Revenue
      Enterprise Value/EBITDA
      
    Then we do some feature engineering to the data like deleting datapoints lacking data and dimensionality reduction.  
    This data will be stored in a .csv file. in which you input the name. 
    
Historical S&P500 Prices
    
    We will also scrape intraQuarter.zip for s&p500 prices. These prices will be added to the training features. 
    We will be using these prices as a benchmark to compare the ticker stock price. 
    If the change in stock price of a ticker is greater than the change in stock price of the S&P500 then it outperformed the S&P500 and should have been bought. 
    So, our labels aren't actually going to be the stock prices. They will be binary labels of either yes, the stock outperformed, or no, the stock did not. 
    
    
Current Stock Statistics:

    After we have our training data and have trained our model it is time to make some predictions. 
    For each of the tickers in intraQuarter.zip we'll use beautiful soup to scrape yahoo finance for current stock statistics and prices. 
    Then we will predict which tickers will outperform the S7P500 and the program will return the tickers one should buy. 
    




