# Price index and financial data computation

We compute a global price index using data from various exchanges and
currencies (USD, EUR, CNY). This global index
reflects the general price of bitcoin across the world and is
expressed in US dollars (internally, values in foreign currencies are
converted to USD).

We also compute currency-specific indices, including only exchanges
which trade said currency. These currency-specific indices reflect how
much a bitcoin is worth in just one given currency, so are free of any foreign
exchange rate impact.

## Data collection

We collect trades and order book data from various exchanges
using exchanges' own APIs. We regularly poll data from these APIs,
reformat them in a common format and store them in a database.

We collect and store:

- all trades:
  - exchange's own trade ID
  - price
  - bitcoin amount exchanged
  - trade direction (is it the result of a buy or a sell)
- full order book snapshot taken every minute:
  - date of the snapshot
  - bid or ask status
  - price
  - bitcoin amount
- daily foreign exchange reference rates from the European Central
  Bank
  [feed](https://www.ecb.europa.eu/stats/exchange/eurofxref/html/index.en.html)

## Computed values

### From trades

#### Last price

last known trade price for each exchange/currency. If the volume of
exchanges is small on a given exchange, this value can be quite old
compared to other exchanges and will not reflect the current estimation of
the bitcoin price.

#### Volume over a time window

amount of bitcoins exchanged during a specific time window on a given
exchange. This reflects exchange activity.

#### Volume Weighted Average Price (VWAP) over a time window

this gives a smoother price curve over a time window than using price
values only (excludes huge price variations provoked by very small
trades)

#### Price volatility over a time window

standard deviation of prices every X seconds/minutes on a larger time
window. This shows the historical price move amplitude.

#### Effective spread over a time window

#### Current trend

computed by doing a linear regression between the price and dates.

### From order book snapshot

We use a partial view of the order books, considering only orders
within a certain threshold of the book's mid-point. Thus we exclude
"extreme" orders that have an extremely low chance of being effectively
executed.

#### bid/ask mid and spread at a given time

Best buy and sell price, average price and spread (difference between
buy and sell price)

#### Market depth

amount of available bitcoin at a given "distance" from the mid
point. This metric reflects the amount of bitcoin one can "in theory"
sell or buy at a given time with no impact of more than "distance" %
on the current price.

In reality, it's possible for the order book to change (new orders
appearing or orders being dropped) before a transaction can be fully
completed.

#### Impact of a transaction of a given amount of bitcoins (or fiat currency)

this completes market depth computation. We simulate the impact of
a defined transaction on the order book.

## Price index computation

### VWAP

The logical approach to index computation consists of doing a volume
weighted average price over all exchanges.

### Market depth

Using only VWAP is limited in two ways:

- First, in the rare event that one
  exchange experiences a crash, the result is often a large volume
  increase with a current price inconsistent with those on
  other exchanges. So by using VWAP only, the price index is
  pushed in a direction that does not reflect the price over all
  markets.
- Secondly, due to (some) exchanges' opacity and a tendency to use
  algorithms and other techniques to artificially increase volumes, they
  appear to be far more active trading platforms.

To solve these issues, we use the order books' depth at a certain
distance. This completes the VWAP because on top of weighting the
price by the volumes actually traded, we can weight by the volumes
that can potentially be executed.

### Market mover

The last point concerns identifying a "market mover".

The market mover is the exchange on which the price is "made", as
opposed to other markets where the price is merely the result of
arbitrages based on this market mover.

A good method consists in computing the correlation between the
buy/sell pressure and the price trend (is the price going up or
down?). Unfortunately not all exchanges give the price direction (buy
or a sell) in their trade data (most notably Bitfinex) so we are unable to
integrate this technique yet.

The market mover changes over time and is determined every time we
compute the price index.

### Wrap up

50% of the final index consists of market mover volume and depth
weighted price. The other 50% comes from the volume and depth
weighted prices of other exchanges proportional to this score.
