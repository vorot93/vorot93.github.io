---
layout: post
title:  "ETH is not the center of Ethereum universe"
date:   2020-11-09 23:56:00 +0300
categories: ethereum
---
This topic came up after discussing whether Ethereum is a currency network or a database.

First of all, let’s define the key concepts. ETH is not Ethereum. ETH is a token that’s inbuilt in Ethereum, the only representation of token concept available in Ethereum from genesis block. At the same time, we remember that Ethereum is a database that stores arbitrary state and stored procedures. Thus the brightest people of our community created [ERC20 standard][erc20] that describes a common interface for stored procedures so that they can represent tokens too! And those today are supported by various wallet applications, just like ETH.

There are thousands upon thousands of ERC20 tokens. Their being arbitrary smart contracts united behind a shared interface allows for great flexibility w.r.t. issuance and transfer. The most interesting of them is **DAI** which is automatically pegged to US Dollar at 1:1 ratio. Basically, your bucks on Ethereum without intermediaries.

Now, you may ask, what is the *purpose* of ETH? Why don’t we retire it and just use e.g. DAI whose value is stable and doesn’t fluctuate like a man walking after a night of drinks?

The answer is transaction fees. If you remember, transactions on Ethereum are not free - they can consume considerable computational resources and thus the user has to pay a price so that any spam is expensive. At the same time, transaction fees provide incentive for miners to secure the network and issue new blocks. And the only currency on this fee market is ETH. We don’t have a feasible way to pay for transactions with ERC20 tokens. Yet.

But this is the *only* use case where we need ETH. For everything else there are ERC20 tokens.

Let’s compare this with Bitcoin.

Bitcoin is unremarkable: the network revolves around BTC UTXO and has very limited scripting language. Yes, there are standards like Omni that fit new token creation into that language, but they are really taxing on the network and not quite as powerful as Solidity-based smart contracts. Bitcoin is hollow and doesn’t make sense without its native token.

So, to summarize, ETH is not the center of Ethereum universe, but rather a utility token to pay for transactions. Nothing more. And one day its usefulness will vanish completely.

[erc20]: https://eips.ethereum.org/EIPS/eip-20