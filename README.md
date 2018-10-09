JavaScript Multiple Coins Library
=======

A pure and powerful JavaScript Multiple Coins library.

## Principles

Bitcoin is a powerful new peer-to-peer platform for the next generation of financial technology. The decentralized nature of the Bitcoin network allows for highly resilient bitcoin infrastructure, and the developer community needs reliable, open-source tools to implement bitcoin apps and services.

## Get Started

```
npm install mix-lib
```


```js
var lib = require('mix-lib');
var priv = new lib.PrivateKey("GEEK");
console.log(priv);
console.log(priv.toWIF());
console.log(priv.toAddress());
// <PrivateKey: 8f446ab8fa9db83b367bc4d160b7a6f0fc2fa6f390d076c2616ae7dae2ed49ca, network: GeekCash>
// XG68DmUydnkdaj9VoXzD6mzGzc2ABz2jEFcUPAYWnBew3eJtYvWk
// <Address: GPJs2uSCFDjDD9GqS5PcGcixBUs6jB8qL8, type: pubkeyhash, network: GeekCash>
```

```js
var lib = require('mix-lib');
var priv = new lib.PrivateKey("DASH");
console.log(priv);
console.log(priv.toWIF());
console.log(priv.toAddress());
// <PrivateKey: 58af0f84ecc68038f9d4f8ec5658c5bf4bea57fedaaa1ebe6e992ca32b101417, network: Dash>
// XEG2F8raABRoeze7xV4exbg6ji1YYR34qqWQGJ3CZuhdGcZvqGDx
// <Address: XkV5By8ADmr2jzm6bYjkQnUFHqeu9wk1bP, type: pubkeyhash, network: Dash>
```

```js
var lib = require('mix-lib');
var priv = new lib.PrivateKey("BTC");
console.log(priv);
console.log(priv.toWIF());
console.log(priv.toAddress());
// <PrivateKey: 74b35dce79cb9154858615e8cb8b2889f826ec557bb0bcf95d40881d367779af, network: Bitcoin>
// L18ZXoA7z6xJBmE9mvctDzwyg2skLLHhYWmupXdnkHQ7JgtL9kXf
// <Address: 1B7zH2tuXAwqFj9AypBqjMqJiiNKY67os4, type: pubkeyhash, network: Bitcoin>
```

```js
var lib = require('mix-lib');
var transaction = new lib.Transaction()
    .from(utxos)          // Feed information about what unspent outputs one can use
    .to(address, amount)  // Add an output with the given amount of satoshis
    .change(address)      // Sets up a change address where the rest of the funds will go
    .sign(privkeySet)     // Signs all the inputs it can
```

### Import an address via WIF

```js
var lib = require('mix-lib');
var wif = 'XG68DmUydnkdaj9VoXzD6mzGzc2ABz2jEFcUPAYWnBew3eJtYvWk';
var address = new lib.PrivateKey(wif).toAddress();
//<Address: GPJs2uSCFDjDD9GqS5PcGcixBUs6jB8qL8, type: pubkeyhash, network: GeekCash>
```

### Coins
```
GeekCash [GEEK]
Dash [DASH]
Bitcoin [BTC]
PIVX [PIVX]
ColossusXT [COLX]
Aegeus [AEG]
MetaCash [META]
LightPayCoin [LPC]
Northern [NORT]
DeepOnion [ONION]
DigiByte [DGB]
Zcash [ZEC]
Stakenet [XSN]
MMOCoin [MMO]
Stakecube [SCC]
BitcoinCash [BCH]
Alqo [ALQ]
BlockNet [BLOCK]
CommandCoin [CMD]
Transcendence [TELOS]
QubeNet [QUB]
SolarCoin [SLR]
Bettex [BTXC]
```

To get community assistance and ask for help with implementation questions, please join: https://discord.gg/Yq9tFKK

## Examples

* [Generate a random address](docs/examples.md#generate-a-random-address)
* [Generate a address from a SHA256 hash](docs/examples.md#generate-a-address-from-a-sha256-hash)
* [Import an address via WIF](docs/examples.md#import-an-address-via-wif)
* [Create a Transaction](docs/examples.md#create-a-transaction)
* [Sign a Bitcoin message](hdocs/examples.md#sign-a-bitcoin-message)
* [Verify a Bitcoin message](docs/examples.md#verify-a-bitcoin-message)
* [Create an OP RETURN transaction](docs/examples.md#create-an-op-return-transaction)
* [Create a 2-of-3 multisig P2SH address](docs/examples.md#create-a-2-of-3-multisig-p2sh-address)
* [Spend from a 2-of-2 multisig P2SH address](docs/examples.md#spend-from-a-2-of-2-multisig-p2sh-address)


## Security

We're using Bitcore in production, as are [many others](https://geekcash.org), but please use common sense when doing anything related to finances! We take no responsibility for your implementation decisions.

If you find a security issue, please email hello@geekcash.org


## License

Code released under [the MIT license](LICENSE).

Copyright (c) 2018 GeekCash Team (https://geekcash.org)
