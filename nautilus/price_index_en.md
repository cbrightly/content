# Price index and financial data computation

We compute a global price index using data from various exchanges and
currencies (USD, EUR, CNY). This global index
reflects the general price of the bitcoin across the world and is
expressed in US dollars (internally, values in foreign currencies are
converted to USD).

We also compute currency specific indices, including only exchanges
which trade said currency. These currency specific indices reflecs how
much a bitcoin is worth in a given currency so is void of any foreign
exchange rate impact.

## Data collection

We are collect trades and order books data from various exchanges
using exchanges own APIs. We regularly poll data from these APIs,
reformat them in a common format and store them in a database.

We collect and store:

- all trades:
  - exchange's own trade ID
  - price
  - bitcoin amount exchanged
  - trade direction (is it the result of a buy or a sell)
- full order books snapshot every minute:
  - date of the snapshot
  - bid or ask status
  - price
  - bitcoin amount
- daily foreign exchanges reference rates from the European Central
  Bank
  [feed](https://www.ecb.europa.eu/stats/exchange/eurofxref/html/index.en.html)

## Computed values

### From trades

#### Last price

last known trade price for each exchange/currency. If the volume of
exchanges is small on a given exchange, this value can be quite old
compared to other exchanges and not reflect the current estimation of
the bitcoin price.

#### Volume over a time window

amount of bitcoins exchanged during a specific time window on a given
exchange. This reflects the exchange activity.

#### Volume Weighted Average Price (VWAP) over a time window

this gives a smoother price curve over a time window than using price
values only (excludes huge price variation provoked by very small
trades)

#### Price volatility over a time window

standard deviation of prices every X seconds/minutes on a larger time
window. This shows the historical prices move amplitude.

#### Effective spread over a time window

#### Current trend

computed by doing a linear regression between the price and dates

### From order books snapshot

We use a partial view of the order books, only considering orders
within a certain threshold of the book mid point. Thus we exclude
"extreme" orders that have an extremely low chance to be effectively
executed.

#### bid/ask mid and spread at a given time

Best buy and sell price, average price and spread (difference between
buy and sell price)

#### Market depth

amount of available bitcoin at a given "distance" from the mid
point. This metric reflects the amount of bitcoin one can "in theory"
sell or buy at a given time with no impact of more than "distance" %
on the current price.

In reality, it's possible that the order book changes (new orders
appearing or orders being dropped) before the transaction can be fully
completed.

#### Impact of a transaction of a given amount of bitcoins (or fiat currency)

this completes the market depth computation. We simulate the impact of
a defined transaction on the order book.

## Price index computation

### VWAP

The logical approach to index computation consists in doing a volume
weighted average price over all exchanges.

### Market depth

Using only VWAP is limited in two ways:

- First, despite the fact that this event fairly rare, when one of the
  exchanges experience a krach this often results in a large volume
  increase with a current price not consistent with the prices of
  other exchanges. Thus by doing a VWAP only, the price index is
  pushed in a direction that does not reflects the price over all
  markets.
- The second issue is due to (some) exchanges opacity who probably use
  algorithms and other techniques to artificially increase volumes and
  appear to be very active trading platforms

To solve these issues, we use the order books depth at a certain
distance. This completes the VWAP because on top of weighting the
price by the volumes actually traded, we can weight by the volumes
that can potentially be executed

### Market mover

The last point consists in identifying a "market mover".

The market mover is the exchange on which the price is "made", as
opposed to other markets where the price is merely the results of
arbitrages regarding this market mover.

A good method consists in computing the correlation between the
buy/sell pressure and the price trend (is the price going up or
down?). Unfortunately not all exchanges give the price direction (buy
or a sell) in their trade data (most notably Bitfinex) so we couldn't
integrate this technique yet.

The market mover changes over time and is determined every time we
compute the price index.

### Wrap up

50% of the final index consist of market mover volume and depth
weighted price, the other 50% are made from the volume and depths
weighted prices of other exchanges proportionally to this score.
