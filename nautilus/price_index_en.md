# Kaiko Bitcoin Price Index Information

Kaiko's global bitcoin price index is a live USD-equivalent spot rate for Bitcoin. It is computed from trade and order book data from the following pairs and exchanges:
* BTC/USD: Bitfinex, Bitstamp, Kraken, Coinbase, itBit, BTC-e, Huobi, Okcoin, Gemini
* BTC/CNY: Huobi, Okcoin, BTCC
* BTC/EUR: Kraken, itBit, Coinbase, BTC-e

We also compute currency-specific indices for USD, CNY and EUR to provide spot rates that are not impacted by foreign exchange.

## Data collection

We collect trades and order book data from exchanges
using their APIs. We store all trades and take order book snapshots every minute. Daily foreign exchange reference rates from the [European Central Bank](https://www.ecb.europa.eu/stats/exchange/eurofxref/html/index.en.html) are used to convert amounts from CNY and EUR to USD for our global index.

## Weights Computation

For each (exchange, currency pair), and given a time-window T, we compute:
* the average of the sum of asks from the mid price to the mid price + 1%.
* the average of the sum of bids from the mid price to the mid price - 1%.
* the sum of the volume bought
* the sum of the volume sold
We then apply 35% weights to the liquidity values (sum of asks and bids)
and 15% weights to the volume values. This rewards exchanges that are
actually liquid more than those that boost their volume through zero-fee
trades. This gives each exchange a weight.

## Final Price

We then compute the price by multiplying the mid price of each exchange and
with its weight. If the mid-price is too old, we use the last price.
