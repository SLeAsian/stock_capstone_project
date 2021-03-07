## Stock Market Movement Prediction Using Graph Convolutional Network (GCN)

The purpose of this project is to demonstrate the effectiveness of graph convoutional network on limited data in comparison to the other model.

<img src="photos/stock.jpg" alt="hi" class="inline"/>

### Why stock market prediction with GCN?
Stock market prediction is a lucrative domain to which machine learning methods can be applied, and recent advancements in the field of artificial intelligence are heavilyaiding this prediction.  Powerful new types of neural network models called graph convolutionalnetworks (GCNs) can effectively learn from data contained within a network structure.  GCNs facilitate ML approaches on graphs similarly to the way traditional CNNs conveniently operate onstructured data like images.  Whereas before one might derive features from the graph’s inherent properties and use those for a machine learning task, one now has access to powerful algorithmsthat can learn directly from the graph itself. Stock markets consist of highly self-dependent data andhave an inherent network structure that can be appropriately exploited using these techniques.

### Data and objective
For this project, we collected stock price data from the 30 stocks that comprise the Dow JonesMarket Index over a 12-month period (127 trading days) ranging from January 2020 to January 2021 using Yahoo Finance’s API. We chose this data because we did not want to compare pre-pandemic stock prices to post-pandemic prices, as market conditions varied drastically due to the pandemic,but we still wanted to work with as much data as we possibly could given this constraint. Our model features consist of opening price, low price, high price, and trading amount.  The features are min-max normalized to deal with discrepancies of scale between stock price (in the 100s) and tradingamount (in the 10000s).  Our labels for each day will be 1 if closing price is greater than that day’sopening price and 0 otherwise. We split the data into a 70-30 train-test split for prediction.

We will predict the price movemnt of S&P500 and DOW30 to output the month to month prediction accuracy.

### Baseline Model

##### Arima Model
Arima model serves as a traditional regression prediction. These types of regression were typically used in the stock market prediction, serving as a perfect baseline in our prediction task.

##### Fully Connected Network
Fully connected network serves as a baseline from a neural network standpoint. Its maturity since its initial creation allow for a decent comparison of how much better a GCN can perform.

### Graph Convolutional Network
- Neural network that can operate on graph data similarly to how CNNs operate on structured image data
- Data are not independent from each other,	but have meaningful connections between them that can be leveraged for learning

### Our accuracy result

Arima Model: 49 percent

Fully Connected Network: 

Graph Convolutional Network: 60 percent

As we can see the two baseline models performed with the performance of right around a coinflip, whereas GCN performed slightly better with the same dataset.

### Limitation, conclusion and plans for future

Our model simply has the price movement of the past, which does not entail much about the future. Some of the possible additional add-on are mostly around the data. In the future, we may incorporate historical news and financial information once given more budeget and time.

For more detail please click on this link for the actual paper.
