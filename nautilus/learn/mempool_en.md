## What Does the 'Mempool' Line Show? ##

The bitcoin Mempool (memory pool) is a collection of all transaction data in a block that have been verified by bitcoin nodes, but are not yet confirmed. According to the specification that implemented this feature into the bitcoin protocol – [BIP35](https://github.com/bitcoin/bips/blob/master/bip-0035.mediawiki) – knowing what transactions are waiting in the mempool is advantageous to: (a) [SPV Wallet clients](https://www.kaiko.com/learn/wallets#-thin-client-and-spv-bitcoin-wallets) needing to record transactions quickly, and (b) Miners wanting to catch up with transactions as soon as possible after a restart (to avoid missing out on lucrative fees). Mempool data is also used in remote network diagnostics.

You can see exactly which transactions are waiting in the current mempool [here](http://mempool.info/) (external site).

### Mempool and the Bitcoin Block Size Issue ###

Mempool size is shown on Kaiko's [Blockchain Data chart](https://www.kaiko.com/blockchain) as an orange dotted line. It shows how effectively the bitcoin network is clearing transactions by adding them to blocks – if the line is approaching the current 1MB block size maximum limit, there's a chance low-fee transactions will not be included in the next confirmed block. If the line passes 1MB, some transactions will definitely not be included.

The mempool is usually (though not always) completely emptied as miners confirm each block. Our chart shows whether that has happened or not.
