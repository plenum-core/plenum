# Mining notes

Plenum uses KawPoW, the ProgPoW variant with a memory-hard DAG and a per-period math sequence. It is the algorithm Ravencoin uses, so every KawPoW miner already supports it.

## What to expect

| Item | Value |
| --- | --- |
| Algorithm flag in miners | `kawpow` |
| Epoch length | 7,500 blocks |
| Epoch duration | about 31 days at 240 s blocks |
| DAG at epoch 0 | about 1.07 GB |
| DAG growth | about 8 MB per epoch |
| Recommended video memory | 8 GB |
| Minimum that will work today | 4 GB, with shrinking headroom |

For scale: Ravencoin, six years in, runs a 5.79 GB DAG. Plan for growth rather than for the first month.

## The command

```
t-rex -a kawpow -o stratum+tcp://<pool-host>:<port> -u <your Z address> -p x
```

Any KawPoW-capable miner takes the same arguments: lolMiner, GMiner, Team Red Miner and NBMiner all have a `kawpow` mode.

## There is nothing to point it at

No pool exists. No node is running in public. No genesis block has been mined. Running the command today produces connection errors and heat, nothing else.

This file is published early because a miner should be able to see the shape of the work before deciding to buy hardware for it, and because a project that asks you to run a binary against an unnamed host is not one to trust.

## Ports and addresses

- P2P: 19007
- RPC: 19008
- Address prefix: `Z`

If those numbers change, this file changes with them, in the same commit, before anything else is announced.
