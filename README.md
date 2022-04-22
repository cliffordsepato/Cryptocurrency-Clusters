# Cryptocurrency Clusters

![Hero-image](resources/images/Cryptocurrencies.jpeg)

## About this Project

* A prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. They would like a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.

* The First step will be to pre-process the raw data to fit the machine learning models. Since there is no known classification system, I will need to use unsupervised learning. I will be using several clustering algorithms to explore whether the cryptocurrencies can be grouped together with other similar cryptocurrencies. In the end, I will be making use of data visualization to share my findings with the investment bank.

## Data Preparation

We start by reading `crypto_data.csv` into Pandas. The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

```python
#Read crypto_data.csv into pandas
crypto_data = "resources/data/crypto_data.csv"
crypto_df = pd.read_csv(crypto_data)
crypto_df.head(10)
```

Discard all cryptocurrencies that are not being traded. In others words, filter all currencies that are currently being traded. 
Once this is done, we drop the `IsTrading` column from the dataframe.

```python
#Discard all cryptocurrencies that are not being traded
crypto_df = crypto_df[crypto_df['IsTrading'] == True]
crypto_df.head(10)
```

```python
#Drop IsTrading column from the dataframe
crypto_df.drop(columns=['IsTrading'], inplace=True)
crypto_df
```

```python
```

```python

```
```python
```

```python
```
## Recomendations
Based on my findings, there is not enough features in the dataset to extact a meaningful grouping. Our elbow chart trends downwards with no elbow point,  there is not enough of an 'elbow' in our K-Means plot to signify a meaningful cluster in this dataset. This clustering did not provide much insight into the cryptocurrency trends. More features should be added.

## References

Crypto Coin Comparison Ltd. (2020) Coin market capitalization lists of crypto currencies and prices. Retrieved from [https://www.cryptocompare.com/coins/list/all/USD/1](https://www.cryptocompare.com/coins/list/all/USD/1)
