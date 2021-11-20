![LSTM-Stock-Predictor](https://github.com/chirathlv/LSTM-Stock-Predictor/blob/main/Images/banner.jpg)

# LSTM-Stock-Predictor

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the `Crypto Fear and Greed Index (FNG)` which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency.

Here two deep learning models have been built and evaluated using both the FNG values and historical closing prices for Bitcoin to determine if the FNG indicators provides a better signal for cryptocurrencies than the normal closing price data.

### Problem setup

```diff
One model will use the FNG indicators to predict the closing price while the second model will use a
window prices to predict the nth closing price.
```

### Prepared the data for training and testing

- [x] Data has been splitted as 70% for training and 30% for testing.

- [x] Applied MinMaxScaler to the X and y values to scale the data for the model.

- [x] Reshaped the X_train and X_test values to fit the model's requirment of samples, time steps, and features (example: `X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1))`).

### Built and trained custom LSTM RNNs

- [x] Three LSTM Layers of 30 hidden units with dropout (0.2) used to build the model as below.

- [x] `Input Layer > [LSTM Layer with Dropout] > [LSTM Layer with Dropout Layer] > [LSTM Layer with Dropout] > Output Layer`

### Evaluated the performance of each model

- [x] Used the Testing data to evaluate each model and compared the performances.

> `Which model has a lower loss?`

- [x] Second model with window prices to predict the nth price has the lower loss

> `Which model tracks the actual values better over time?`

- [x] Second model with window prices to predict the nth price has the lower loss

> `Which window size works best for the model?`

- [x] Window size of 3 gave the better results with other hyper-parameters
