#Explaining the Charts Lab Graphs#
* * *

##Average Block Size##

This is the size, in kilobytes, of the bitcoin blocks that are created roughly every 10 minutes [LINK TO 'BLOCKS']. The maximum size of a block is currently 1MB – though this is a controversial topic in the bitcoin community. 1MB limits the number of transactions that may fit into a block, which sometimes means those paying higher transaction fees get priority.

There are movements within bitcoin to increase the block size – to 20MB, 8MB, or an undefined variable amount. There are also many participants who want to keep the block limit at 1MB (in order to establish a more competitive fee market).

With this chart, you can see exactly how much storage space is required for each block and how close each block comes to reaching the 1MB max.


##Average Transaction Fees##

This chart shows the average amount paid (in millibitcoins, or mBTC) by senders in transaction fees to miners, per transaction.

Large spikes in the chart (1 BTC or more) are due to days when the network was especially busy, or errors. Particularly large spikes, such as those seen on the 'All Time' chart, are more likely due to error – several users have accidentally mis-judged decimal places and paid way too much for their transaction. Modern consumer-grade bitcoin wallets usually handle the fees automatically, avoiding such mistakes.

See also: [Transaction Fees chart]() 


##Average Volume Per Transaction##

This chart tells you the average amount of BTC sent in each transaction. Looking at the 'All Time' chart, you can see there were far bigger spikes in earlier years, when bitcoin was worth less in dollars and transactions tended to be larger. There is still, however, the occasional large spike when someone sends an unusually high amount in a transaction. 

It's important to remember this about bitcoin: whether someone sends one dollar to a friend or 10 million to the other side of the world, the network should process either transactions at the same speed and for the same fee. 


##Blockchain Size##

This chart shows the total size (usually in gigabytes) of the bitcoin blockchain. If you are running a full bitcoin node [LINK] or mining operation [LINK], you will need to store the entire blockchain on your machine. It can be downloaded from scratch directly, but is also available as a bittorrent for faster download. 

In the original Bitcoin White Paper, Satoshi Nakamoto acknowledged that the blockchain would be ever-growing and would eventually be huge in size. But this is intended to be proportionate to the cost of large-scale storage, which tends to fall every year.


##Blocks Per Day##

This chart has stayed fairly constant for the past few years. The bitcoin network is designed to confirm a block and produce a new one around once every ten minutes – so the number of blocks per day should always be similar.

Spike?


##Coins In Circulation##

This chart shows the total number of bitcoins in circulation today. Only 21 million bitcoins will ever exist, and this number cannot be changed. The system was designed to mine more bitcoins early in its lifespan and gradually diminish over time, which is why over 2/3 of the 21 million total are already in circulation.

The final block that produces new bitcoins will be #6,929,999 – estimated to happen in the year 2140.

New blocks originally produced 50 BTC. Every four years, that number halves. It is currently 25 BTC. Next 'halving day' that number will drop to 12.5 BTC, and so on. The hope is that bitcoin value will increase over time, so miners can continue to earn money by keeping the network secure.

Although a bitcoin exists, it may not be accessible. Millions of bitcoins have possibly been 'locked forever' due to lost keys and hard drives. Bitcoin inventor Satoshi Nakamoto is estimated to have around 1 million BTC in his wallets – and those bitcoins have never been touched. Therefore the 'real' final total bitcoins in circulation is likely to be far less than 21 million.


##Difficulty##

See also: [Bitcoin Mining](LINK)

As more computing (hashing) power is introduced to the bitcoin network, the difficulty of the cryptographic function required to confirm and mine blocks increases. This is to maintain a steady stream of new bitcoin blocks every 10 minutes or so. 

The bitcoin network assesses total hashing power every 2016 blocks (ideally two weeks) and adjusts the difficulty accordingly depending on how long the previous 2016 blocks took to mine. The unit measured on the y-axis of the chart is target ‘gigahashes’, or 1,000,000,000,000 (1 trillion) single hashes.

Using this chart, you can see how the bitcoin mining difficulty has increased exponentially over time – particularly around the end of 2013. This was when the first machines designed exclusively for bitcoin mining began to appear – called application-specific integrated circuits, or 'ASICs'.

The difficulty can also go down. If a large enough number of miners decide bitcoin mining is not profitable, they will switch off their machines and the overall hashing power of the network goes down.

##Hash Rate##

The Hash Rate chart is related closely to the Difficulty chart. The unit measured here is 'hashes per second' – or, the number of cryptographic hash functions performed by mining hardware on a bitcoin block header every second. 

Given the power of machines now driving the bitcoin network and the sheer number of them, this number is now massive. The chart shows 'petahashes', with one petahash equalling one quadrillion (1,000,000,000,000,000) hashes. The figure '350P' on the y-axis of the chart therefore means the combined worldwide network performs 350 quadrillion (350,000,000,000,000,000) hash functions every second.

This number, while always increasing, can fluctuate up or down by around 100 petahashes in a day.

##Outputs Volume##

###What are bitcoin 'inputs' and 'outputs'?###

Bitcoin 'inputs' and 'outputs' can be difficult to understand at first, but they're vital to the way bitcoin functions. The best way is to imagine a bitcoin wallet as a real physical wallet, full of bills and coins.

**Case 1:** You have to pay someone $50. In your wallet is a $20 bill, a $10 and four $5s. As you hand over all that cash, imagine those bills as your 'outputs'.

Now the person you paid has $50, and those bills become his/her 'inputs'. They may keep them for a while, spend them straight away, or send them to the bank. If kept, they could be called 'unspent outputs'. That's six bills all together, or six outputs, worth a total $50.

**Case 2:** You have to pay someone $10, but you only have one $50 bill. The other person takes the $50, and gives you $40 change. Your 'input' in this case is one $50 bill.

This transaction has different kinds of outputs. One is the $10 you gave to the other person, the other is the $40 they gave you back. 

Bitcoin does not have physical bills. So that means there are 'output' amounts of all different sizes floating around out there, depending on how they were spent in the past. To make sure each transaction is the right amount, bitcoin wallet software needs to either break up large amounts, or combine smaller ones. 

Your bitcoin wallet doesn't actually think in terms of total figures. It thinks about all your combined 'inputs' and 'outputs' and calculates their net worth, which it displays to you as a total. For a human, that's easier to understand.

How did this hit 31 million BTC in one day: 19th September, 2012?

##Transaction Fees##

This chart records the amount, in BTC, that bitcoin users have paid in transaction fees on a daily basis. 

Transaction fees are expected to become more important in future, as the number of bitcoins awarded to mining operations per block is halved every four years. In order to keep the network secure, miners will one day rely on income from these fees as an incentive to keep their machines running.

##Transactions Per Block##

This is simply the total number of bitcoin transactions recorded in each block, with each block representing roughly 10 minutes in bitcoin's lifespan.

Notice that the number begins to take off around late 2012/early 2013, around the point where mainstream media began talking about bitcoin. Around the same time, the price of one bitcoin began to rise noticeably beyond trivial amounts, on its way to several record-breaking highs that year.

The number of transactions per block also has relevance to: the size of transaction fees (higher may be necessary to guarantee prompt inclusion in a block), and the ongoing block size debate. [LINK]


##Transactions Per Day##

This chart matches almost perfectly the 'Transactions per Block' chart, since they effectively measure the same thing on different time scales. 





