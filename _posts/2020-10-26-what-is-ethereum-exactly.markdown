---
layout: post
title:  "What is Ethereum exactly?"
date:   2020-10-26 05:00:00 +0300
categories: ethereum
---
This is the question that comes to mind when you interact with Ethereum for the first time.

Some say it’s the *greatest invention of mankind*. Yet for cynical traders and the clueless it’s a pile of trinkets to make money on. For others, it’s the *heart of uncensorable finance*.

But what *really* is Ethereum without hype and bullshit?

Since we know that Ethereum is based on blockchain, let’s start with that.

Blockchain is a **byzantine-fault-tolerant** database with **high replication factor**.

See? Simple. A database, nothing more, nothing less. A big place for storing data. Yes, it has *high replication factor*: anyone can start a node, sync with other nodes, and keep it updated. Yes, it’s also *Byzantine-fault-tolerant* which means that if a malicious node screws with the network, it will chug along just fine.

But blockchain still is a good old database.

Now what distinguishes Ethereum from the first blockchain, Bitcoin?

Smart contracts. But what are they, in plain developer speak? They are programs that take data from the database, execute on it and store results back in the database, all in the same environment. Sound familiar? Back in SQL world we call them stored procedures.

So to summarize,

**Ethereum is a byzantine-fault-tolerant database with high replication factor, which also supports stored procedures (a.k.a. smart contracts).**

That’s it. Really, that’s all Ethereum is. It’s a boring yet solid database with public access, where anyone can store data and call procedures stored in the database.

If you are a core developer and you start thinking this way, you instantly map all your domain knowledge to working on Ethereum. It stops being a wonder weapon. Instead, you clearly see a novel database in front of you and can abstract away everything that’s built on top of that. I root for Decentralized Finance, but don’t have to think of it every day.

Even more importantly, if you are looking for the next backend for your infrastructure, you can make the right tradeoffs. Specifically, if you want to place your backend on a private network run by trusted parties, then *Ethereum really isn’t for you*. Use Postgres instead, it’s far more scalable than any blockchain can ever be.

But if you want to have an application whose backend *isn't computationally intensive* and which *doesn't depend on any party* to run, then you've come to the right place and with the right mindset.