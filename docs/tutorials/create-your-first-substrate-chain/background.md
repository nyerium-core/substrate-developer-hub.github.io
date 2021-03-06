---
title: Background Information
---

In this section, you will learn a little bit about blockchains and the Substrate blockchain
development framework. The Node Template that you are compiling was built with this framework.

## Background on Blockchains

Blockchain networks are composed of individual **nodes** that are connected by a peer-to-peer (P2P)
network. Nodes are the individual computers on a network running the blockchain software that makes
everything work.

To function, a blockchain node needs:

- Storage
- Peer-to-peer networking
- Consensus capabilities
- Transaction handling
- A runtime
- and more...

These technologies span a wide breadth of computer science, and so blockchains usually require teams
of experts to develop. As a result, most blockchain projects are _not_ developed from the ground up.
Instead, these projects are forked from existing blockchain projects. For instance:

- The Bitcoin repository was forked to create: Litecoin, ZCash, Namecoin, Bitcoin Cash, etc...
- The Ethereum repository was forked to create: Quorum, POA Network, KodakCoin, Musicoin, etc...

![Blockchain Project Repository Forks](assets/tutorials/first-chain/forks.png)

Building blockchains in this way has serious limitations as these existing platforms were not
designed with modification in mind.

## Substrate

Substrate is an **open source**, **modular**, and **extensible** framework for building blockchains.

Substrate has been designed from the ground up to be flexible and allow innovators to design and
build a blockchain network that meets their needs. It provides all the core components you need to
build a customized blockchain node.

### Substrate Developer Hub Node Template

We provide an out-of-the-box working Substrate-based node in the form of the Node Template, which
should be compiling as you read this. Without making any changes, you and your friends could share
this node template and create a working blockchain network with a cryptocurrency and everything!

We will teach you how to use this node in "development" mode, which allows you to run a network with
a single node, and have some pre-configured user accounts with funds.
