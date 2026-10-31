# Architecture

Nothing in this file is running yet. It describes the pieces as they are specified, so that a reader can see what a node would consist of and where the numbers live.

## Pieces

| Piece | Job | State |
| --- | --- | --- |
| Node | consensus, mempool, P2P on 19007, RPC on 19008 | specified, not running |
| Miner | KawPoW search over the DAG, submits solutions | third-party software |
| Pool | shares, payouts, stratum | does not exist |
| Wallet | keys, addresses, signing | v0.1.0, key handling only |
| Explorer | index of blocks and transactions | static, nothing to index |

## Consensus parameters

All of them are in [NETWORK.md](NETWORK.md) and in the [whitepaper](../WHITEPAPER.md). The two must agree; if they do not, the whitepaper is authoritative and the network document is a bug.

## Wallet boundary

The wallet deliberately knows nothing about peers. It holds a key, derives an address, and prints the key. Adding a sync client to a build that has nothing to sync with would only create a surface that can be wrong.

## Explorer boundary

The explorer is static HTML. Its search box answers "no chain" for any query because there is no index to search. When an indexer exists, the page becomes a client of it and this paragraph is deleted.
