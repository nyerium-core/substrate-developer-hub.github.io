---
title: Interacting with Your Node
---

Now that your node has finished compiling, let's show you how everything works out of the box.

## Starting Your Node

Run the following commands to start your node:

```bash
# Run a temporary node in development mode
./target/release/node-template --dev --tmp
```

You should see something like this if your node is running successfully:

```bash
2021-02-14 07:23:04  Running in --dev mode, RPC CORS has been disabled.    
2021-02-14 07:23:04  Substrate Node    
2021-02-14 07:23:04  ✌️  version 3.0.0-1c5b984-x86_64-linux-gnu    
2021-02-14 07:23:04  ❤️  by Substrate DevHub <https://github.com/substrate-developer-hub>, 2017-2021    
2021-02-14 07:23:04  📋 Chain specification: Development    
2021-02-14 07:23:04  🏷 Node name: longing-beds-6127    
2021-02-14 07:23:04  👤 Role: AUTHORITY    
2021-02-14 07:23:04  💾 Database: RocksDb at /tmp/substratexosljN/chains/dev/db    
2021-02-14 07:23:04  ⛓  Native runtime: node-template-100 (node-template-1.tx1.au1)    
2021-02-14 07:23:04  🔨 Initializing Genesis block/state (state: 0x6595…11bd, header-hash: 0x63db…b743)    
2021-02-14 07:23:04  👴 Loading GRANDPA authority set from genesis on what appears to be first startup.    
2021-02-14 07:23:04  ⏱  Loaded block-time = 6000 milliseconds from genesis on first-launch    
2021-02-14 07:23:04  Using default protocol ID "sup" because none is configured in the chain specs    
2021-02-14 07:23:04  🏷 Local node identity is: 12D3KooWFM5WBY8HRsesRunyPRrR9yQPNoyf16kLkKyWKzrheDJj    
2021-02-14 07:23:04  📦 Highest known block at #0    
2021-02-14 07:23:04  〽️ Prometheus server started at 127.0.0.1:9615    
2021-02-14 07:23:04  Listening for new connections on 127.0.0.1:9944.    
2021-02-14 07:23:06  🙌 Starting consensus session on top of parent 0x63dbec45fb6109f801e5f9d5e2dab8ad236563c46b4544fb7b947b6b90dbb743    
2021-02-14 07:23:06  🎁 Prepared block for proposing at 1 [hash: 0x4cb82fbae832692856022ca716716a57a9c79004d0e3f3868f167820c2bc9f95; parent_hash: 0x63db…b743; extrinsics (1): [0x1034…fd86]]    
2021-02-14 07:23:06  🔖 Pre-sealed block for proposal at 1. Hash now 0x26f12b7e6db4c24ab702930b3772f01dfbb95c4a1bf5ca5cac63e030efa975f7, previously 0x4cb82fbae832692856022ca716716a57a9c79004d0e3f3868f167820c2bc9f95.    
2021-02-14 07:23:06  ✨ Imported #1 (0x26f1…75f7)    
2021-02-14 07:23:06  🙌 Starting consensus session on top of parent 0x26f12b7e6db4c24ab702930b3772f01dfbb95c4a1bf5ca5cac63e030efa975f7    
2021-02-14 07:23:06  🎁 Prepared block for proposing at 2 [hash: 0x672e6f74ed132dfe516dea947221dc594b30d25d7c939944a9f56f8ecfc2e2f1; parent_hash: 0x26f1…75f7; extrinsics (1): [0x14a5…f60e]]    
2021-02-14 07:23:06  🔖 Pre-sealed block for proposal at 2. Hash now 0x710cd4d62654037c49f978ab119aec1517092d5f54ea2453a5cf08dfca7c3d65, previously 0x672e6f74ed132dfe516dea947221dc594b30d25d7c939944a9f56f8ecfc2e2f1.    
2021-02-14 07:23:06  ✨ Imported #2 (0x710c…3d65)    
2021-02-14 07:23:09  💤 Idle (0 peers), best: #2 (0x710c…3d65), finalized #0 (0x63db…b743), ⬇ 0 ⬆ 0    
2021-02-14 07:23:12  🙌 Starting consensus session on top of parent 0x710cd4d62654037c49f978ab119aec1517092d5f54ea2453a5cf08dfca7c3d65    
2021-02-14 07:23:12  🎁 Prepared block for proposing at 3 [hash: 0x692a154b1958be8f3a1ceb3cdf90be251af88e0060ba2f1ace2348f85ba9bf85; parent_hash: 0x710c…3d65; extrinsics (1): [0x3881…9fc2]]    
2021-02-14 07:23:12  🔖 Pre-sealed block for proposal at 3. Hash now 0x372561200b64d05430cda797be1f95fb44169023c0b236cf0a01a08c01223a90, previously 0x692a154b1958be8f3a1ceb3cdf90be251af88e0060ba2f1ace2348f85ba9bf85.    
2021-02-14 07:23:12  ✨ Imported #3 (0x3725…3a90)    
2021-02-14 07:23:14  💤 Idle (0 peers), best: #3 (0x3725…3a90), finalized #1 (0x26f1…75f7), ⬇ 0 ⬆ 0
```

If the number after `finalized:` is increasing, your blockchain is producing new blocks and reaching
consensus about the state they describe!

## Start the Front-End

To interact with your local node, we will use
[the Substrate Developer Hub Front-End Template](https://github.com/substrate-developer-hub/substrate-front-end-template),
which is a collection of UI components that have been designed with common use cases in mind.

You already installed the Front-End Template; launch it by executing the following command in the
root directory of the Front-End Template:

```bash
# Make sure to run this command in the root directory of the Front-End Template
yarn start
```

## Interact

Once the Front-End Template is running and loaded in your browser at
[http://localhost:8000/](http://localhost:8000/), take a moment to explore its components. At the
top, you will find lots of helpful information about the chain to which you're connected as well as
an account selector that will let you control the account you use to perform on-chain operations.

![Chain Data & Account Selector](assets/tutorials/first-chain/chain-data.png)

There is also a table that lists
[the well-known test accounts](../../knowledgebase/integrate/subkey#well-known-keys) that you have
access to. Some, like Alice and Bob, already have funds!

![Account Table](assets/tutorials/first-chain/accts-prefunded.png)

Beneath the account table there is a Transfer component that you can use to transfer funds from one
account to another. Take note of the info box that describes the precision used by the Front-End
Template; you should transfer at least `1000000000000` to make it easy for you to observe the
changes you're making.

![Balance Transfer](assets/tutorials/first-chain/apps-transfer.png)

Notice that the table of accounts is dynamic and that the account balances are updated as soon as
the transfer is processed.

### Runtime Metadata

The Front-End Template exposes many helpful features and you should explore all of them while you're
connected to a local development node. One good way to get started is by clicking the "Show
Metadata" button at the top of the template page and reviewing
[the metadata that your runtime exposes](../../knowledgebase/runtime/metadata).

![Metadata JSON](assets/tutorials/first-chain/metadata.png)

### Pallet Interactor & Events

You can use the runtime metadata to discover a runtime's capabilities. The Front-End Template
provides a helpful Pallet Interactor component that provides several mechanisms for interacting with
a Substrate runtime.

![Pallet Interactor & Events](assets/tutorials/first-chain/interactor-events.png)

[Extrinsics](../../knowledgebase/learn-substrate/extrinsics) are the runtime's callable functions;
if you are already familiar with blockchain concepts, you can think of them as transactions for now.
The Pallet Interactor allows you to submit
[unsigned](../../knowledgebase/learn-substrate/extrinsics#unsigned-transactions) or
[signed](../../knowledgebase/learn-substrate/extrinsics#signed-transactions) extrinsics and also
provides a button that makes it easy to invoke an extrinsic by way of
[the `sudo` function from the Sudo pallet](https://substrate.dev/rustdocs/v3.0.0/pallet_sudo/enum.Call.html#variant.sudo).
You will learn more about using the "SUDO" button to invoke privileged extrinsics in the third
tutorial, the [Add a Pallet](../add-a-pallet) tutorial.

You can select Query interactions to read
[the values present in your runtime's storage](../../knowledgebase/runtime/storage). The RPC and
Constant options provide additional mechanisms for runtime interaction.

Like many blockchains, Substrate chains use [events](../../knowledgebase/runtime/events) to report
the results of asynchronous operations. If you have already used the Front-End Template to perform a
balance transfer as described above, you should see an event for the transfer in the Event component
next to the Pallet Interactor.

## Next Steps

This is the end of your journey to launching your first blockchain with Substrate.

You have launched a working Substrate-based blockchain, attached a user interface to that chain, and
made token transfers among users. We hope you'll continue learning about Substrate.

Your next step may be:

- Extend the features of the template node in the [Add a Pallet](../add-a-pallet) tutorial.
- Learn about forkless runtime upgrades in the [Upgrade a Chain](../upgrade-a-chain) tutorial.

If you experienced any issues with this tutorial or want to provide feedback, You can
[ask a question on Stack Overflow](https://stackoverflow.com/questions/tagged/substrate) and use the
`substrate` tag or contact us on
[Element](https://app.element.io/#/room/!HzySYSaIhtyWrwiwEV:matrix.org).
