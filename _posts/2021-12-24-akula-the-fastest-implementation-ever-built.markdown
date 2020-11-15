---
layout: post
title:  "Akula: the fastest Ethereum implementation ever built"
date:   2021-12-24 03:00:00 +0300
categories: ethereum
---
Ethereum is proudly known for its diversity of full node implementations that maintain network state, uphold protocol rules and provide their users a gateway into the world of web3. Diversity makes sure that network only works as intended, and according to protocol, not certain bugs in a single codebase.

Today we are proud to present the preview of new addition to this fine family: **Akula**.

## True innovation meets systems language

Akula grew out of an internal project in Erigon team, where it was originally conceived as a database access library. If you haven’t read about Erigon yet, you definitely should check out [this blog post](https://medium.com/openethereum/gnosis-joins-erigon-formerly-turbo-geth-to-release-next-gen-ethereum-client-c6708dd06dd), which describes how this performant beast of a node lets users get full validation archive on consumer hardware. Consequently, all Erigon’s data model innovations and ideas went into design of Akula as well: flat state, usage of MDBX storage engine, outside preprocessing - all to lower disk footprint and reduce read-write amplification.

On top of this, Akula is written in **Rust**, fast, elegant and safe systems programming language, which keeps a whole class of memory and concurrency bugs at bay. Akula leverages a new Rust EVM interpreter [evmodin](https://github.com/vorot93/evmodin), specifically designed to allow for asynchronous state access.

All of this enables the new standard of performance, not seen in full nodes before.

![Erigon and Akula benchmark, courtesy of Paolo Rebuffo](/assets/img/akula-benchmark.png)

Erigon and Akula benchmark, courtesy of Paolo Rebuffo

Akula beats already fast Erigon by 1.5-2 times on execution performance. Without building additional indexes, we are looking at full validation of Ethereum mainnet from genesis in under 24h.

## WIP, but already works

Akula is available on GitHub: [akula-bft/akula](https://github.com/akula-bft/akula)

In the coming weeks we should gain working download of blocks and headers over devp2p as well as minimal Web3 API. However, Akula can already be run *today*, as companion node connected to Erigon’s database, as both a preview of what’s to come and additional verification of Erigon’s execution.

Please join #akula channel on Erigon Discord or [@akula_bft](https://t.me/akula_bft) group on Telegram if you have any questions about Akula or would like to help with testing and development.

We wish you a Merry Christmas and Happy New Year, and hope that 2022 will bring about even more decentralized Ethereum with Akula enabling it even more.
