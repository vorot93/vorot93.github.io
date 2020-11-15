---
layout: post
title:  "Boring tech"
date:   2020-10-28 08:42:00 +0300
categories: ethereum
---
If you are a software developer, you probably know what boring code is. Here is a primer for the uninitiated:

https://tech.palatinategroup.com/everyone-should-write-boring-code-a578ed186732

*Boring code, as opposed to smart code, is easier to understand and therefore easier to modify and delete.*

I think we should also introduce the notion of *boring tech*.

Let me talk about how I joined Ethereum core development.

I come from the world of business backends and microservices. OpenWeatherMap, online retail, Moscow Metro Wi-Fi network authorization - all run on the code I wrote over the past few years. I joined Gnosis as full-time Ethereum developer in January 2020.

The first thing that struck me was the number of novel tech in Ethereum space. *RLP*! *devp2p*! custom node *discovery* protocol! Homebrew transport which uses homebrew encoding format! Custom underlying data structure: *Modified Merkle-Patricia Trie*! The whole new world, so much to learn! How exciting!

At the same time, if you remember my previous post, Ethereum is actually just a novel database with some unique properties. But much of all this exciting homebrew tech is not related to database theory. So how relevant is it all to Ethereum again?

It’s not. I had to spend months fixing the oft neglected devp2p stack in OpenEthereum, instead of working on more pressing issues like EVM improvements and database speedup. I just couldn’t offload this to the software industry at large. No one else uses devp2p. No one else cares for RLP. We have to maintain these on our own.

**Exciting homebrew tech is a massive waste of time for Ethereum core developers.**

We work on a database. We are not prophets. We are not revolutionaries. Creating a whole new world/ecosystem is not our job. Our job is to develop our *product*. So why don’t we double down on the core technology and use industry-standard solutions for supporting crutches?

Off the top of my head:
- Drop devp2p and transition to libp2p.
- Kill RLP/SSZ in P2P communication and serialize data with MessagePack/CBOR/bson/whatever. Work on standardizing RLP as a binary format with canonical encoding.
- Transition from Modified Merkle-Patricia Trie to a boring Binary Trie.

Trying to invent everything is akin to trying to hit the target with spread fingers: you will hurt yourself without achieving the goal.

At the same time, there is great potential in Ethereum, as shown by the advances of turbo-geth. Concentrating our resources will allow us to smash the scalability issues in ways no other blockchain network can.