## Stock Market Movement Prediction Using Graph Convolutional Network (GCN)

The purpose of this project is to demonstrate the effectiveness of graph convoutional network on limited data of only price movement in comparison to the other model.

<img src="photos/stock.jpg" alt="hi" class="inline"/>

### Why stock market prediction with GCN?
Stock market prediction is a lucrative domain to which machine learning methods can be applied, and recent advancements in the field of artificial intelligence are heavilyaiding this prediction.  Powerful new types of neural network models called graph convolutional networks (GCNs) can effectively learn from data contained within a network structure.  GCNs facilitate ML approaches on graphs similarly to the way traditional CNNs conveniently operate onstructured data like images.  Whereas before one might derive features from the graph’s inherent properties and use those for a machine learning task, one now has access to powerful algorithmsthat can learn directly from the graph itself. Stock markets consist of highly self-dependent data andhave an inherent network structure that can be appropriately exploited using these techniques.

### Data and objective
For this project, we collected stock price data from the 30 stocks that comprise the Dow JonesMarket Index over a 12-month period (127 trading days) ranging from January 2020 to January 2021 using Yahoo Finance’s API. We chose this data because we did not want to compare pre-pandemic stock prices to post-pandemic prices, as market conditions varied drastically due to the pandemic,but we still wanted to work with as much data as we possibly could given this constraint. Our model features consist of opening price, low price, high price, and trading amount.  The features are min-max normalized to deal with discrepancies of scale between stock price (in the 100s) and tradingamount (in the 10000s).  Our labels for each day will be 1 if closing price is greater than that day’sopening price and 0 otherwise. We split the data into a 70-30 train-test split for prediction.

### Baseline Model

##### Arima Model
Arima model serves as a traditional regression prediction. These types of regression were typically used in the stock market prediction, serving as a perfect baseline in our prediction task.

##### Fully Connected Network
Fully connected network serves as a baseline from a neural network standpoint. Its maturity since its initial creation allow for a decent comparison to GCN.

### Graph Convolutional Network
We used graph convolutional network as it can take advantage of its structural information to gather the feature information from its neighbor to output a prediction. Since our price movement data on a daily basis are not independent from each other,	therefore having meaningful connections between using adjacancy matrix can be leveraged for learning.

Example of our correlation/adjacency matrix:

<img src="photos/heatmap.jpg" alt="hi" class="inline"/>

### Our accuracy result

Arima Model: 60 percent

Fully Connected Network: 60 percent

Graph Convolutional Network: 60 percent

The ARIMA model performs well at 60% accuracy over the test set. The fully connected network performs similarly to the GCN at 60%, perhaps because our original graph was not of very good quality and doesn't add too much to our models' ability to predict stock movement. This is also accuracy averaged over the days and stocks in our test set, and the average varied greatly between them. There may be certain days that have harder prediction tasks than others.

### Limitation, conclusion and plans for future

Our model simply has the price movement of the past, which does not entail much about the future. Some of the possible additional add-on are mostly around the data. In the future, we may incorporate historical news and financial information once given more budeget and time.
