# Kaiko Price Index Information

Kaiko's global price index is a live USD-equivalent spot rate for Bitcoin. It is computed from trade and order book data from the leading exchanges across three trading pairs: BTC/USD, BTC/CNY and BTC/EUR.
We also compute currency-specific indices for USD, CNY and EUR to provide spot rates that are not impacted by foreign exchange.

## Data collection

We collect trades and order book data from exchanges
using their APIs. We store all trades and take order book snapshots every minute. Daily foreign exchange reference rates from the [European Central Bank](https://www.ecb.europa.eu/stats/exchange/eurofxref/html/index.en.html) are used to convert amounts from CNY and EUR to USD for our global index.

## Values Used

### From trades data
* last price for each currency pair for each exchange
* trade volume over a time window, which reflects an exchange's activity
* Volume Weighted Average Price (VWAP) over a time window, in order to smooth spiky price variations
* price volatility over a time window, which reflects historical price movement amplitude
* effective spread over a time window
* current trend, the result of a linear regression between prices and dates

### From order book snapshots
* bid, ask, mid and spread
* book depth at a certain distance from the mid
* book liquidity for a given amount of bitcoins or fiat

## Index Computation

First we compute the VWAP across all exchanges.
VWAP, however, may be limited in two ways:

- exchanges that experience a high volume crash don't necessarily represent the rest of the market.
- exchanges that artificially increase their volume, but don't have correspondingly high liquidity, can appear healthier than warranted.

To solve these issues, we use order book depth "at a certain
distance". This complements the VWAP, which weights by actual trading volume, with additional weighting by potential trading volume.

Finally, we identify a principal market in real-time. The principal market is the exchange on which the price is "made", as
opposed to other markets which are merely followers. We do this by computing the correlation between
buy/sell pressure and the price trend. The principal market changes over time and is determined at each iteration.

### Final Weights

The volume and depth weighted price of the market mover accounts for 50% of the final value. The other 50% is proportionally spread between the volume and depth
weighted prices of the other exchanges.