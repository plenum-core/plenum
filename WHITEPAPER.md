# Plenum — specification

**Ticker:** PLNM · **Algorithm:** KawPoW · **Launch:** no premine, no presale, no ICO.

## 1. The idea

Every fan in every duct pushes an uneven stream. A plenum is the chamber that absorbs that and hands the same pressure to each outlet; it is cheap, it has no moving parts, and without it the room nearest the fan gets everything. Plenum, the chain, is the same idea applied to a proof-of-work reward: one rule, applied without exception, so that the first miner and the ten-thousandth miner are paid by the same arithmetic.

## 2. Parameters

| Parameter | Value | Why |
| --- | --- | --- |
| Block interval | 240 s | 360 blocks a day, an exact division of 86,400 |
| Reward | 52 PLNM | fixed per era, paid to the finder |
| Halving | 288,000 blocks | exactly 800 days at this interval |
| Supply cap | 29,952,000 PLNM | twice the first era, closed by the halving series |
| Epoch | 7,500 blocks | the KawPoW DAG period, about 31 days |
| P2P port | 19007 | fixed in the specification |
| RPC port | 19008 | fixed in the specification |
| Address prefix | Z | distinguishes addresses from hashes |

## 3. Emission

86,400 / 240 = 360 blocks a day. 360 × 52 = 18,720 PLNM a day. 18,720 × 800 = 14,976,000 PLNM in the first era, which is half the cap. Era two pays 26 per block, era three 13, era four 6.5, and the tail closes the series at 29,952,000. The cap is not a policy that can be revised; it is the sum of a geometric series with a first term of 14,976,000 and a ratio of one half.

## 4. Why KawPoW

KawPoW is ProgPoW as deployed by Ravencoin: a memory-hard DAG plus a math sequence regenerated each period, with wider memory reads. The effect is that the fastest machine for the job stays a general-purpose GPU, which is the machine ordinary people already own. A new algorithm would have looked more original and would have had no miners, no audit and no track record.

The cost is DAG size. At epoch zero the DAG is about 1.07 GB and grows about 8 MB per epoch, so 8 GB of video memory is the sensible floor and 4 GB will fall behind.

## 5. What is promised

- The parameters above, unchanged.
- No premine, no presale, no development fee, no treasury address.
- Documents published under MIT, in the repository, editable by anyone.

## 6. What is not promised

- A launch date for the network.
- An exchange listing, a market maker, a price, or a return.
- A foundation, a team token, a governance vote, or a roadmap with dates.
- That the software is free of defects. It has not been audited.

## 7. Current state

The specification is fixed and the documents are public. A Windows wallet (v0.1.0) exists, holds keys, and has nothing to sync against. No node is running in public, so no genesis block has been mined and no coins exist outside the ones this document describes as future.
