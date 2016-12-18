# Introduction to Bitcoin Wallets #

## What is a Bitcoin Wallet? ##
Bitcoin Wallets are for storing bitcoins. In most cases, a 'wallet' is a software app that lets users spend and receive bitcoins. Think of something that works like an online bank account, but is accessible as cash in a regular wallet.

A basic, smartphone-based wallet does just that: send and receive bitcoins. Users send payments by scanning the recipient's QR code (displayed on a phone, web page or in-store terminal) with the phone camera. Your own wallet can display a QR code for others to pay you.

That's all you need to use bitcoin. All mobile wallets can do that much. Beyond that, it gets more complicated. This guide will explain the different kinds of bitcoin wallets out there.

Many wallets have extra features that make them more versatile. They can trade bitcoins for regular currencies on exchanges, they can keep bitcoins in deep and more secure storage. They might be on smartphones or desktop computers. It might be a service you sign up for, or something you make yourself. Wallets might be printed on paper or even wood, and kept offline for secure storage. New forms of bitcoin wallet are being invented all the time.

It isn't necessary to show ID to use a bitcoin wallet. Some wallet services ask you to register with a user name or email address, while others don't require any information from you at all. Users can determine their own levels of privacy by choosing services according to their features.

Some store all your security credentials (passwords, bitcoin private keys) locally on a device; others store them online. If you lose your mobile device, most wallets allow you to recover your account on a different one (though you may have to records the details somewhere safe yourself). Some wallets use the same bitcoin address for every transaction, others change with each transaction (giving you more privacy).

Bitcoin wallet users often have to choose between security and convenience. Some wallets look quite secure, but would be cumbersome to use in daily life with multiple passwords and authentications. Others, while easier and quicker for spending, might not be secure if someone steals your device. Wallets stored entirely on desktop PCs are vulnerable to hackers and disk crashes.

Luckily, wallets are becoming more user-friendly all the time, so that trade-off is becoming less necessary.


# Bitcoin Wallets: Important Terms to Understand #

## Bitcoin (Public) Address ##
This is a string of around 30 alphanumeric characters, starting with 1 or 3, which is used to send and receive bitcoin values. Bitcoin public addresses work in a similar way to email addresses on the surface, though they usually don't have a person's name attached or any other identifier. They are also more disposable – many bitcoin users these days use a different address for every transaction, creating more privacy. If a single address is used repeatedly, deep data analysis may reveal its owner by observing behavioural and spending patterns.

Bitcoin addresses are also sometimes referred to as 'public keys'.

Addresses may exist completely offline and can be printed on physical objects. Even if only used once, every address is permanent and can hold a bitcoin value forever if required. To view the current value of any bitcoin address ever created, use Kaiko's [Blockchain Explorer](https://www.kaiko.com/blockchain)

### How Many Bitcoin Addresses Are There?  ###

The total possible number of bitcoin addresses, using current methods to create them, [is 2^160](https://bitcointalk.org/index.php?topic=24268.0). That is... a lot. So many, in fact, as to almost be infinite (there are only 2^63 grains of sand on all the beaches on Earth). It is possible, even desirable, to create a new bitcoin address for every transaction, no matter how large or small.

## Bitcoin QR Code ##
This is the 2-dimensional, machine-readable 'barcode' that can be scanned and read with a smartphone camera or webcam. Up to now, these have been the most common ways for devices to read and display bitcoin addresses, since a bitcoin address would be cumbersome to enter on a keyboard and difficult to remember.

Bitcoin QR codes used by merchants and payment processors often embed the value of the transaction along with the public address. This makes transactions easier and faster, with just a couple of button-presses needed to complete.

QR codes are used to display both public addresses (keys) and private keys. If you have a private key as a QR code, be careful not to reveal it – especially near cameras, as this TV reporter [found out the hard way](http://www.businessinsider.com/bloomberg-matt-miller-bitcoin-gift-stolen-2013-12).

## Bitcoin Private Key ##
A private key is a cryptographic 'password' linked to an address. These keys are stored securely and in secret by wallet software. Knowing this number gives you the ability to spend whatever bitcoin value exists at that address. If you have your life savings stored at one bitcoin address, guard the private key extremely well. If you lose it you will never be able to recover your balance.

Bitcoin private keys usually begin with the number '5' or '6'. The '5' addresses are unencrypted and vulnerable to theft by anyone who can see them. A private key starting with '6' is encrypted with an additional password. The latter type is safer... provided you remember the password and know how to decrypt it.

Some wallets allow private keys to be remembered and recovered by generating them from a single ‘seed phrase’. See ‘[HD Wallets](https://www.kaiko.com/learn/wallets#bitcoin-hd-wallet)’ on this page for more information.

## Open/Closed-Source Wallet ##
**Open Source**: this means the programming (source) code for the wallet software is published publicly and available for anyone to examine. An advantage is it may be more trustworthy or secure because of this. The disadvantage is: if you are the wallet developer, anyone can copy your product.

**Closed Source**: in this case, the source code is kept secret by the software developer. Creators can keep unique features to themselves for a competitive advantage. The disadvantage is no-one can see what the software is actually doing behind the scenes, which may reduce trust if the developer isn't well-known.

## Bitcoin HD Wallet ##
HD stands for 'Hierarchical Deterministic'. This wallet generates all its public addresses and private keys from a single 'seed' – which is often (but not necessarily) a string of random words.

The advantages of an HD wallet are: they can be recovered on another device, using the seed phrase, if the original device is lost, damaged or replaced, and they can generate new address keys for every transaction, allowing greater privacy – it is far more difficult to connect a user to a single bitcoin address if it's used only once, as there are no spending or behavioural patterns to observe.

## Online Bitcoin Wallet Service ##
This kind of wallet works in a similar way to any other internet-based service, like your bank or Facebook. You log in with a user name and password, and all your information (including account, bitcoin total) is stored on that service's servers in its data center. The advantage is you can access your bitcoin account from a number of different devices and locations. The disadvantages are: if the wallet provider is not secure, there is a risk they could be hacked with the loss of your bitcoins and/or personal information. You need to know the provider is trustworthy, and likely to stay in business. It is generally not advisable to keep large sums of money on an online wallet (though see the '[Multisig Wallet](https://www.kaiko.com/learn/wallets#bitcoin-multisig-wallet)' section for more useful information on this).

## ‘Full Client’ Bitcoin Wallet ##
This is the oldest and most powerful kind of bitcoin client. Usually confined to desktop machines, full clients download the entire bitcoin blockchain (currently around 37GB of information) and keep a full record of every bitcoin transaction, ever. Today they are used by more technically-able users (and those with large hard drives). They help keep the bitcoin network secure by adding one more 'node' to the network that can verify transactions. Examples of full client wallets are [Bitcoin Core](https://bitcoin.org/en/download) and [Armory](https://bitcoinarmory.com/).

Full client wallets also give advanced technical users access to all bitcoin's scripting options, allowing them to create more complicated and customised functions to suit their needs. They can send transactions to multiple recipients, monitor addresses for payments, send transactions according to time or other conditions, plus anything else the scripting language permits.

## 'Thin Client' and SPV Bitcoin Wallets ##
'Thin Client' bitcoin wallets allow a user to keep security credentials (passwords, bitcoin private keys) locally on their desktop or mobile device, without needing to download the entire blockchain. They usually do this by partially downloading transaction data, or by accessing 'trusted nodes' on the bitcoin network that have a full copy of the blockchain. Popular thin client wallets are [MultiBit](https://multibit.org/), [Electrum](https://electrum.org/#home) and [Mycelium](https://mycelium.com/).

SPV stands for 'Simplified Payment Verification', a thin client method that is becoming popular on mobile platforms. SPV wallets also connect to a trusted 'node' which stores the entire blockchain, and sync transaction information from there. The main advantage of SPV wallets is they are more secure and private than online services, which store information centrally. One disadvantage is if you don't open your wallet very often, SPV wallets can sometimes take a while to sync and update with the bitcoin network. Examples of SPV wallets are Android's [Bitcoin Wallet](https://play.google.com/store/apps/details?id=de.schildbach.wallet&hl=en), [bread wallet](http://breadwallet.com/) on iOS and [LUXSTACK](https://luxstack.com/) (both platforms).

## Social/Business Features on Bitcoin Wallets ##
As wallets get more sophisticated and competitive, they are including extra payment features other than just spending and receiving. Some use email addresses or social network information to allow users to send money to each other without QR codes or bitcoin addresses. Some create payment networks for use by businesses, organizations, fundraising campaigns, freelancers, and groups of friends. Feature possibilities here are limited only by developers' imaginations, and are becoming more numerous every month.

## Bitcoin 'Multisig' Wallet ##
Short for 'multiple-signature'. Like nuclear missile launch safeguards, these wallets require more than one private key to release funds. For an online wallet, this usually means the user keeps one key locally, the online service keeps another, and a third key is kept by the user in a different location. This way, funds are safe from hack attacks or an untrustworthy wallet provider, and a user can access funds even if the provider goes out of business.

Multisig wallets are usually better for 'vault' or more secure long-term storage, as the extra verification makes them less convenient for daily spending. Multisig addresses usually begin with the number '3', rather than the standard '1'.

Multisig wallets are also used by groups of people who store funds for a common purpose. No single person can access (or run away with) the money, so they can even be used by groups of people who do not know each other. The number of keys required does not always need to be two out of three – the total number of keys and number required to release the funds can vary according to need (and what the service being used allows).

Examples of multisig bitcoin wallet services are [BitGo](https://www.bitgo.com/) and [Ninki](https://ninkip2p.com/).

## Bitcoin 'Paper Wallet' ##
Yes, a bitcoin wallet can be printed and not exist anywhere electronically. These are usually used for larger amounts of money and for long-term storage. People have used paper, wood, metal and other materials to store bitcoin values. While paper wallets are the preferred option for long-term storage, it is not possible to spend partial amounts from them and keep the rest. To access and spend the funds, it is necessary to 'sweep' the entire contents of a paper wallet into a software-based wallet using its private key. The same paper wallet should not be used again after that, for security reasons.

One very important thing to note is: even a paper wallet address is visible to the bitcoin network. If the computer used to generate the private key (or the key generation process itself) were not secure, the funds can still be stolen.

[Bitcoin Paper Wallet] (https://bitcoinpaperwallet.com/) is an open-source website that allows users to create, encrypt and print physical wallet keys. The site's advice is to download the software and use it to create wallets on a computer that is not on the internet.

## Bitcoin 'Brain Wallet' ##
A 'brain wallet' means you generate your public address and private key from a mnemonic or passphrase you keep only in your head. The benefit is that the wallet does not exist anywhere in the physical or electronic world, so offers the ultimate in privacy. However, brain wallet generators have been less than secure in the past, making their keys still vulnerable to discoverability. Then there are problems with the brain itself – if you forget the mnemonic, or suffer a head injury, your wallet could be gone.

NB: The 'seed' phrase for an HD wallet is essentially a brain wallet, if you believe in your ability to remember it.

##  Bitcoin Hardware Wallet  ##

New kinds of bitcoin wallet hardware devices are emerging that attempt to merge the security of a paper/offline wallet with the spending convenience of a software wallet. These devices vary in features, but usually store their bitcoin keys locally on a device, keeping them off hard drives and the internet. To access or spend the funds, users plug the device into a PC or phone via USB, and sign in with a password and/or other credentials. Examples of hardware wallets in common use today are the [Trezor](http://www.bitcointrezor.com/) and [Ledger](https://www.ledgerwallet.com/) devices.

## &nbsp;

### What's next?

Keep going with our educational pages:
<br>
<a href='/learn/bitcoin-basics'>Bitcoin Basics</a>  &nbsp; &nbsp; -  &nbsp; &nbsp; <a href='/learn/exchanges'>Bitcoin Exchanges</a>  &nbsp; &nbsp; -  &nbsp; &nbsp; <a href='/learn/mempool'>Mempool</a> &nbsp; &nbsp; - &nbsp; &nbsp; <a href='/learn/mining-blockchain'>Mining</a>  &nbsp; &nbsp; -  &nbsp; &nbsp; <a href='/learn/assets'>Assets</a>
Or explore Kaiko's data and charts:
<br>
<a href='/blockchain'>Blockchain Explorer</a>  &nbsp; &nbsp; -  &nbsp; &nbsp; <a href='/exchanges/prices'>Exchanges</a> &nbsp; &nbsp;  - &nbsp; &nbsp; <a href='/bitcoin-price'>Bitcoin Price</a> &nbsp; &nbsp; - &nbsp; &nbsp; <a href='/bitcoin-clock'>Bitcoin Clock</a> &nbsp; &nbsp; - &nbsp; &nbsp; <a href='/assets'>Blockchain Assets</a> - &nbsp; &nbsp; <a href='/mining'>Mining</a>
