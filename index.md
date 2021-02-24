## Stock Market Movement Prediction Using Graph Convolutional Network

<img src="photos/stock.jpg" alt="hi" class="inline"/>

### Why the GCN?
Stock market prediction is a lucrative domain to which machine learning methods can be applied, and recent advancements in the field of artificial intelligence are heavilyaiding this prediction.  Powerful new types of neural network models called graph convolutionalnetworks (GCNs) can effectively learn from data contained within a network structure.  GCNs facilitate ML approaches on graphs similarly to the way traditional CNNs conveniently operate onstructured data like images.  Whereas before one might derive features from the graph’s inherent properties and use those for a machine learning task, one now has access to powerful algorithmsthat can learn directly from the graph itself. Stock markets consist of highly self-dependent data andhave an inherent network structure that can be appropriately exploited using these techniques.

### Data
For this project, we collected stock price data from the 30 stocks that comprise the Dow JonesMarket Index over a 12-month period (127 trading days) ranging from January 2020 to January 2021 using Yahoo Finance’s API. We chose this data because we did not want to compare pre-pandemic stock prices to post-pandemic prices, as market conditions varied drastically due to the pandemic,but we still wanted to work with as much data as we possibly could given this constraint. Our modelfeatures consist of opening price, low price, high price, and trading amount.  The features are min-max normalized to deal with discrepancies of scale between stock price (in the 100s) and tradingamount (in the 10000s).  Our labels for each day will be 1 if closing price is greater than that day’sopening price and 0 otherwise. We split the data into a 70-30 train-test split for prediction.

### Baseline Model

##### Fully Connected Network

##### GCN

### Plan for future

Some of the possible additional add-on are mostly around the data. Our model simply has the price movement of the past, which does not entail much about the future. In the future, we may incorporate historical news and financial information once given more budeget and time.
