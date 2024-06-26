# AirSwap Demo Maker

Reference RFQ and Last Look protocol server for AirSwap.

**Install packages**

```
$ yarn
```

**Quick start on Autonity Piccadilly (Yamuna) Testnet**

Copy `.env.example` to `.env` and update values:

```
PRIVATE_KEY= …
CHAIN_ID=65100003
```

Then start the server (with both RFQ and streaming):

```
$ yarn dev
```

Now you can query the server from the AirSwap CLI:

```
$ npm install -g https://github.com/clearmatics/airswap-cli/releases/download/pcgc-r6.2/airswap-4.3.1-autonity.4.tgz
$ airswap chain
  → set to 65100003
$ airswap account:import (or account:generate)
$ airswap stream
  → ws://localhost:3000
$ airswap order
  → http://localhost:3000
```

**Build and run for production**

```
$ yarn build
$ yarn start
```

Now you can register the server:

```
$ airswap registry:url
  → https://<server-url>
$ airswap metadata:update
$ airswap tokens:add
  → WATN, NTN etc.
```
