# Anchor Example: Token Swap AMM

SPL [Token-swap](https://github.com/solana-labs/solana-program-library/tree/master/token-swap) (AMM) implemented in Anchor.

## Build, Deploy and Test

First, install dependencies:

```
$ yarn install
```

Next, we will build and deploy the program via Anchor.

Get the program ID:

```
$ anchor keys list
anchor_amm: J5fjkFW5nrUuzD4eMD6c1ZS765KvMLyk1dpMm6aac2Nf
```

Here, make sure you update your program ID in `Anchor.toml` and `lib.rs`.

Build the program:

```
$ anchor build
```

Let's deploy the program. Notice that `anchor-amm` will be deployed on a [mainnet-fork](https://github.com/DappioWonderland/solana) test validator run by Dappio:

```
$ anchor deploy
...

Program Id: J5fjkFW5nrUuzD4eMD6c1ZS765KvMLyk1dpMm6aac2Nf

Deploy success
```

Finally, run the test:

```
$ anchor test --skip-build --skip-deploy
```
