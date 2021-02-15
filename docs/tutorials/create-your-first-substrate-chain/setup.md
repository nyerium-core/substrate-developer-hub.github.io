---
title: Set Up Your Computer
---

Normally, we would teach you more about the Substrate blockchain development framework, however,
setting up your computer for Substrate development can take a while.

To optimize your time, we will have you start the setup process. While things are compiling, you can
continue to the next section to learn more about Substrate and what we are building.

## Prerequisites

You will probably need to do some set-up to prepare your computer for Substrate development.

### Substrate Development

This tutorial uses the
[Substrate Developer Hub Node Template](https://github.com/substrate-developer-hub/substrate-node-template/tree/v3.0.0),
which serves as a good starting point for building on Substrate.

## Compiling Substrate

Complete these steps to compile the Node Template:

1. Use Git to clone the Node Template (version `v3.0.0`).

    ```bash
    git clone -b v3.0.0 --depth 1 https://github.com/substrate-developer-hub/substrate-node-template
    ```

2. Follow the
   [setup instructions](https://github.com/substrate-developer-hub/substrate-node-template/blob/v3.0.0/doc/rust-setup.md).

3. Compile the Node Template.

    ```bash
    cargo build --release
    ```

The time required for the compilation step depends on the hardware you're using. Don't wait before
moving on.

## Install the Front-End Template

This tutorial uses a ReactJS front-end template to allow you to interact with the Substrate-based
blockchain node that you should have started compiling in the previous step. You can use this same
front-end template to create UIs for your own projects in the future.

To use the front-end template, you need [Yarn](https://yarnpkg.com), which itself requires
[Node.js](https://nodejs.org/). If you don't have these tools, you may install them from these
instructions:

- [Install Node.js](https://nodejs.org/en/download/)
- [Install Yarn](https://yarnpkg.com/lang/en/docs/install/)

Now you can proceed to set up the front-end template with these commands.

```bash
# Clone the code from github
git clone -b v3.0.0 --depth 1 https://github.com/substrate-developer-hub/substrate-front-end-template

# Install the dependencies
cd substrate-front-end-template
yarn install
```
