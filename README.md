# Trac20

A proposal for a gasless p2p token standard on Trac Network. See /contract/contract.js and /contract/protocol.js.

Trac20 defines the most simplistic token standard possible and can be operated in terminal (no special transactions required).

It supports signed and fair mints. Signed mints enable deployers to limit mints for selected wallets.

Inter-contract interaction can be achieved through the use of Trac Features (e.g. for marketplaces like [Hypermall](https://github.com/Trac-Systems/hypermall-downloads)).

This contract is instantly executable, see instructions below.

## Install

Make sure to have git and node installed.

```shell
git clone https://github.com/Trac-Systems/trac20.git
```

```js
cd trac20
npm install -g pear
npm install
pear run . store1
```

## Update

```shell
cd trac20 (if not already done)
git clone https://github.com/Trac-Systems/trac20.git temp
```

```js
cp -fr temp/* .
rm -fr temp
npm update
pear run . store1
```

Use the commands in the Trac20 section to deploy, mint, transfer.

If your peer errors "not writable", just restart to auto-join.

To simulate transactions, append a "--sim 1" to your Trac20 commands.

Chat system is enabled.

To enable log output in the terminal (what's minting), set the following to true in the index.js:

```js
peer_opts.enable_logs = true;
peer_opts.enable_txlogs = false;
```

