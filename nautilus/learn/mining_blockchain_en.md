# How Does Bitcoin Work? #

### A Basic Introduction to Bitcoin Mining and the Blockchain  ###
Bitcoin mining is a specialist and technical process, however it is possible to understand the basic concepts and functionality without needing a thorough knowledge.

This guide is intended to be a fairly entry-level introduction to bitcoin mining and its surrounding terminology, though some technical knowledge may be needed.

## What is Bitcoin Mining? ##

The first thing to understand is that the word 'mining' in bitcoin is a metaphor. There is no physical work, process or product involved, other than installing large computer hardware facilities.

Bitcoin mining has two main purposes: (1) it produces new bitcoins, and (2) it keeps the bitcoin network secure by providing the work that validates legitimate transactions.

Both these functions happen about once every 10 minutes. Satoshi Nakamoto coded the 10-minute timing to: (a) minimize the amount of computing power wasted by miners attempting to solve blocks that have already been solved by others (it takes about 1 minute for news of a solved block to propagate throughout the network) and (b) keep confirmation times as fast as possible. 10 minutes was seen as the ideal compromise.

Miners operate around the world, both as solo operators with as little as one mining machine, which [looks like these](http://www.coindesk.com/46k-spent-mining-hardware-final-reckoning/), and [large-scale factory operations with thousands](http://www.coindesk.com/my-life-inside-a-remote-chinese-bitcoin-mine/). The more machines and the faster the hardware, the more profitable mining will be. Other variables that affect cost of operation, such as availability of electricity or natural cooling systems, paying maintenance staff, will also impact profitability.

For these reasons, many large-scale mining operations are located in places such as near the Arctic Circle, rural China, or anywhere with a cheap and ready source of power.

## Can I mine bitcoins on my PC or mobile phone? ##

These days, the simple answer to that question is ‘no’. Bitcoin mining is performed with specialized hardware designed and built specifically for that purpose (see ‘mining hardware’). When the bitcoin network only had a few participants, it was possible to generate new bitcoins on a basic desktop or laptop CPU. But as the number of participants increased and the total power of the network grew, those CPUs generated fewer and eventually no new coins. CPUs that form the core of desktop and mobile systems, no matter how powerful, are not designed to handle the kind of repetitive mathematical tasks bitcoin mining demands (see ‘Proof of Work’).

After CPUs fell away, new bitcoin creation was performed on home-built mining rigs based on video cards (GPUs). In late 2013, though, chipsets optimized for bitcoin mining only came on the market (called ‘ASICs’) and have improved ever since. These days, only ASIC-based machines are capable of doing bitcoin mining in any meaningful way.

For more information on why older machines cannot be used, see ‘Hashrate’ and ‘Bitcoin Mining Difficulty’.

## Is Bitcoin Mining Profitable? ##

This is the million-dollar question, and the answer is based on a number of variables. Overhead costs like electricity, equipment, physical facility, maintenance and staff are all factors. The costs of these depend heavily on location. Perhaps most important of all, however, is the bitcoin price.

Some have estimated that the price of 1 BTC needs to be above $500-600 for a mining operation to break even or be profitable in the short-term. While many of the bitcoins produced need to be sold immediately to pay overheads, others are kept in the hope they will be far more valuable at some point in future.

In the past there have also been issues with access to the latest hardware, with some manufacturers promising unrealistic production and delivery schedules. As with any highly-competitive industry that relies on having the latest technology, an operator needs to be able to weather delays if/when they occur.

## What is a 'Bitcoin Block'? ##

When a bitcoin transaction is made, the system 'broadcasts' it to the global bitcoin network on the internet. Mining operations around the world then collect a list of these transactions and combine them into something called a 'block'. It is up to the miners' software to decide what transactions are included, so transactions that pay higher fees often have an advantage.

The various miners then 'compete' for their block to become the official one for that 10 minute period. They all race to find the correct answer to a complex mathematical problem, devoting vast amounts of time and computing power to the task.

## What do 'Proof-of-Work' and 'Hashing' Mean? ##

The math problem is based on a cryptographic 'hash' function performed on the block's 'header' data (information about a block that appears at the beginning of each one). The result, when expressed as a number, must be lower than a target value the network has set. The machines increment a random number in the hashing equation, in an attempt to get the desired result.

(The header also contains a cryptographic 'fingerprint' from the previous block, ensuring the resulting chain of blocks, or 'blockchain', is made up 100% of valid bitcoin transactions going right back to the beginning.)

This hashing process is called 'proof of work' and is part of bitcoin's backbone. It proves that a significant amount of computing 'work' has gone into performing the block function. Without this work, it would be possible for anyone with a computer to cheat the system, and bitcoin could not function.

The machine that solves the problem is the winner, and the block of transactions it chose are declared official and sealed in bitcoin records forever.

A new block begins and 25 new bitcoins are created. The winning miner receives the new bitcoins, and the process begins its 10-minute cycle again.

(Initially this was 50 new bitcoins every 10 minutes. Every four years that number halves – it became 25 in November 2012, and will halve again to 12.5 bitcoins in July 2016.)

As soon as one block is solved, miners begin working on the next one.

## What Does 'Hashrate' Mean in Bitcoin? ##

When looking at mining statistics, you will see the term 'hashes per second'. This is how many hashing functions the mining network collectively is performing on the block header data every second. Currently, this is measured in the billions ('gigahashes' or GH/s), trillions ('terahashes' or TH/s) or even quadrillions ('petahashes' or PH/s).

The bitcoin mining hashrate is currently around the 360,000 TH/s mark, but fluctuates daily.



## What is Bitcoin Mining Difficulty? ##

In order for transaction blocks to be verified and created around once every 10 minutes, even as mining computing power increases, the difficulty of the math problem is designed to vary. The more hashing power the network has, the more difficult the problem.

The bitcoin network assesses the total hashing power available and adjusts difficulty every 2,016 blocks, or around once every two weeks.

See Kaiko's chart showing [bitcoin mining difficulty](https://www.kaiko.com/mining) for exact data. Difficulty is constantly increasing as technology improves and machines become more powerful.

Looking at an 'all-time' chart for mining difficulty, you can see an exponential increase that began around the end of 2013/start of 2014. This is when the first hardware designed specifically for bitcoin mining, called ASICs, began to appear (see 'Mining Hardware').

There is a constant race to always have the most cutting-edge mining hardware, as this confers an advantage in the race to solve blocks and collect the newly-minted bitcoins. Any advantage is temporary, however, as the new technology soon filters through to everyone on the network.


## What Kind of Hardware is Needed To Mine Bitcoins? ##

In the beginning, it was possible to mine bitcoins on an ordinary desktop or laptop computer. As more joined the network, the competition and thus difficulty increased. Users built purpose-built mining rigs using graphics cards (or GPUs) better suited for the repetitive hashing process.

Seeing both a business opportunity and technological advantage, companies formed to design and manufacture specialist chips that could perform bitcoin mining tasks extremely efficiently and well, and served no other purpose. These chips, called ASICs (application-specific integrated circuits) and the machines that housed them were expensive, but gave their users a massive hashing advantage.

ASIC use caused the hashing difficulty to rise exponentially. By early 2014, most if not all serious bitcoin miners were using ASIC hardware, and those without them were mining miniscule amounts. Faster and more efficient ASICs have been produced ever since – so fine-tuned for bitcoin mining are these chips that, once they are obsolete, they cannot be used for any other purpose. The machines still function, but they will mine only miniscule amounts of bitcoin.


## What Are Bitcoin Mining Pools? ##

A mining pool allows bitcoin block rewards to be shared out over a large group of miners, rather than each one competing individually.

While it is possible to mine bitcoin with just one modern machine, the odds of that machine solving a block (and receiving the new bitcoins) all by itself are very low – just imagine all the other machines out there competing against it.

For this reason, both small and large-scale miners form groups called 'mining pools'. This combines the hashing power of all members into one 'account'. The miners in the pool try to solve the math problem and, if successful, submit the result to a central server.

When that pool's server solves a block, the new bitcoins are distributed evenly among members according to the power they contribute to the network. This guarantees everyone will gain some share of the mining rewards, if small.

There are roughly 10 dominant mining pools currently on the bitcoin network, plus several smaller ones. You can see their share of the hashing power on [these charts](https://www.kaiko.com/mining).

### Mining Pools: Disadvantages  ###

Miners can join and leave pools anytime they like, and several pools have risen and fallen in prominence over the years. The larger the pool, the more money it is likely to make its members.

One concern surrounding mining pools is that one [may become too powerful](http://www.coindesk.com/bitcoin-mining-detente-ghash-io-51-issue/), gaining close to (or over) 50% of the hashing power on the bitcoin network. Such power would enable a group to take control of the network and (with malign intent) invalidate completed transactions, spend bitcoins twice (the 'double-spend') and destroy confidence in the entire bitcoin system.

In the past, when a single pool has come close to that level of hashing power, its members have [voluntarily left to join other pools](http://www.coindesk.com/bitfury-pulls-power-ghash-community-uproar/) and safeguard the network's integrity.


## What is Bitcoin 'Cloud Mining'? ##

'Cloud mining' is where investors buy shares in a larger mining operation located elsewhere, rather than having to buy and operate the hardware themselves.

Well-known companies operating cloud mining operations have included CEX.io, Genesis Mining, ZeusHash, HashNest, and CloudHashing (no longer in operation), plus a range of smaller and independent services. It is recommended to do thorough research into providers' reputations before purchasing any cloud mining contract.

Cloud mining has a number of benefits for both operators and investors: operators can more easily pay overhead costs, and it enables a larger number of people to get involved. Investors can participate in bitcoin mining and share its rewards without having to have any technical knowledge, or take any responsibility for maintaining a physical facility.

Disadvantages to cloud mining have included: some dishonest or incompetent operators, and dissatisfaction with payouts or customer service. There are also the problems that plague both operators and investors: fluctuating bitcoin prices relative to the initial costs laid out, the need to always have the latest bitcoin mining hardware, and the hardships suffered after lengthy delays in delivery of new equipment.


## What is a 'Bitcoin Node'? ##

A bitcoin node is a computer that stores a full copy of the bitcoin blockchain, going all the way back to the network's beginning in 2009. Such a machine is able to validate any bitcoin block from any time, and therefore helps to keep the network secure and decentralized without needing to do any mining.

Full bitcoin nodes may also serve as 'trusted' access points for light bitcoin wallets and clients (see 'wallets' section for more information), so things like mobile bitcoin wallets can communicate with the network without needing to download the entire blockchain.

At the time of writing this is 42GB of data and is always increasing. See Kaiko's [blockchain size chart](https://www.kaiko.com/statistics/blockchain-size) to see its current size.

To operate properly as a bitcoin node, the operator must have a connection open and a machine operating without sleeping at least six hours a day (preferably 24 hours).
They must also allow incoming connections on port 8333, which is not always available to everyone without manual router/firewall configuration.

## &nbsp;

### What's next?

Keep going with our educational pages:
<br>
<a href='https://kaiko.com/learn/exchanges'>Bitcoin Exchanges</a>  &nbsp; &nbsp; -  &nbsp; &nbsp; <a href='https://kaiko.com/learn/wallets'>Bitcoin Wallets</a> &nbsp; &nbsp;  -  &nbsp; &nbsp; <a href='https://kaiko.com/learn/wallets'>Mining</a> &nbsp; &nbsp; - &nbsp; &nbsp; <a href='https://kaiko.com/learn/mempool'>Mempool</a>

Or explore Kaiko's data and charts:
<br>
<a href='/blockchain'>Blockchain Explorer</a>  &nbsp; &nbsp; -  &nbsp; &nbsp; <a href='/exchanges/prices'>Exchanges</a> &nbsp; &nbsp;  - &nbsp; &nbsp; <a href='/bitcoin-price'>Bitcoin Price</a> &nbsp; &nbsp; - &nbsp; &nbsp; <a href='/bitcoin-clock'>Bitcoin Clock</a> &nbsp; &nbsp; - &nbsp; &nbsp; <a href='/assets'>Blockchain Assets</a> - &nbsp; &nbsp; <a href='/mining'>Mining</a>
