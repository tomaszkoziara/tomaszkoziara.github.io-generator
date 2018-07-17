---
title: What's a blockchain and how to break it
date: 2018-04-22 17:42:55
comments: true
tags:
- blockchain
- cryptocurrencies
---
A blockchain is simply a chain of blocks in which each block contain information.

Originally it was described in 1991 and was intended to timestamp documents in order to prevent backdating them and tampering. Basically it worked like a notary.

It was rediscovered in 2009 by Satoshi Nakamoto to create Bitcoin and it gained momentum at the end of 2017 with the enormous increase in value of Bitcoin.
<!-- excerpt -->
This is simple memorandum made for the future myself and everyone interested to know in simple words what's behind the new boy on the block in technology landscape.

Let's get started.

# What'a blockchain?

A blockchain is simply a chain of blocks in which each block contain information.

Originally it was described in 1991 and was intended to timestamp documents in order to prevent backdating them and tampering. Basically it worked like a notary.

It was rediscovered in 2009 by Satoshi Nakamoto to create Bitcoin and it gained momentum at the end of 2017 with the enormous increase in value of Bitcoin.

A blockchain works as a distributed ledger public to anyone and is difficult to tamper with by construction.

Let's see it more in detail.

Each block is composed basically by:

* data
* a hash of the block
* a hash of the previous block.

![](Blockchain4.png)

# Data
Data depends on the blockchain, but basically is the information you want to carry. For example Bitcoin blockchain stores information about transaction such as the amount of money moved, the sender and the receiver.
	
![](Blockchain1.png)


# Hash
It's the identifier of the block. It's the result of a function which takes in input the data of the block and the hash of previous block. So if you change something inside the block (for example the amount of money of the receiver on a Bitcoin blockchain) you will get a different hash.

![](Blockchain2.png)

# Hash of previous block
This is what makes the chain in the blockchain, doing so every block is linked to the previous. The only block which doesn't have the hash of the previous block (or has it fake) is the first block.

![](Blockchain3.png)

<!-- image blocks pointing backwards -->

# What you need to break a blockchain

On this basis if you want to temper with a block you're going to break all the chain. Because if you change data in one block you'll have to change the block's hash to make it valid. And if you do so you'll break the backward pointer in the next block the block you modified.

![](Blockchain5.png)

So to make the chain valid again you need to recalculate all the hash and reconstruct the chain.

But there's a mechanism to prevent you from doing so and it's called proof-of-work.

Proof-of-work simply slows down the creation of the new blocks so it would be extremely difficult to reconstruct a whole chain of blocks.

Even if you were able to do so, you changed a single blockchain. But a blockchain is a distributed ledger public to anyone. It is distributed as a P2P network and everyone is allowed to join and when does so gets a full copy of the blockchain and can check if everything is ok.

![](Blockchain6.png)

So for example when a new block is sent to every node and each node checks block validity and if hasn't been tempered with adds it to the blockchain. Doing so nodes create consensus. Technically it is still possible to add a bad block to the chain but you have to make it by creating consensus controlly the majority of the blocks.

![](Blockchain7.png)

# TL;DR;

A blockchain security is given by:

* the use of hashing, that creates a tight chain that can't be tampered with unless you recalculate all the hashes backwards and that would be a lot of work
* the proof-of-work which makes non trivial to calculate a hash
* being distributed, so doesn't matter if an attacker compromises a single ledger, because there has to be consensus among all ledgers.s

