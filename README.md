# Plenum (PLNM)

A KawPoW GPU proof-of-work chain. 240-second blocks, 52 PLNM to the finder, halving every 288,000 blocks, capped at 29,952,000 PLNM. No premine, no presale, no development fee.

> A plenum is the chamber between a fan and the rooms it feeds. The fan pushes one loud, uneven stream; the chamber turns it into the same pressure at every outlet. One algorithm, one reward, the same pressure on every card.

## Status

| Part | State |
| --- | --- |
| Specification | fixed and public |
| Documents | written, published, MIT |
| Windows wallet | v0.1.0 published, unsigned |
| Node | not running |
| Network | no genesis in public |
| Pool | none |
| Explorer | published, nothing to index |
| Listing | none, none promised |

The site is <https://plenum-core.github.io/plenum/>.

## Parameters

| Parameter | Value |
| --- | --- |
| Algorithm | KawPoW (ProgPoW, Ethash) |
| Block interval | 240 seconds, 360 blocks a day |
| Block reward | 52 PLNM, to the finder |
| Halving | every 288,000 blocks (800 days) |
| Supply cap | 29,952,000 PLNM |
| Epoch length | 7,500 blocks, about 31 days |
| DAG at epoch 0 | about 1.07 GB, about 8 MB growth per epoch |
| P2P / RPC | 19007 / 19008 |
| Address prefix | Z |

The first era pays 360 × 52 = 18,720 PLNM a day, 14,976,000 over 288,000 blocks. Each later era halves, so the series sums to exactly twice the first era.

## Windows build

- Archive: `plenum-win-x64.zip`
- Size: 213,178,812 bytes
- Inside: `plenum-win-x64.exe`, 213,178,642 bytes
- Release: https://github.com/plenum-core/plenum-wallet/releases/tag/v0.1.0
- Download: https://github.com/plenum-core/plenum-wallet/releases/download/v0.1.0/plenum-win-x64.zip
- SHA-256: `9fa75ce4dedfb5c6072dd3651633b6bd38eca6c340c3ff78682777fe4ab2f18e`
- Signature: none, unsigned build

Check it before running:

```
certutil -hashfile plenum-win-x64.zip SHA256
```

The wallet holds and prints keys. It has no chain to synchronise against yet.

## Documents

[Whitepaper](WHITEPAPER.md) · [Mining](MINING.md) · [Wallet](WALLET.md) · [Transparency](TRANSPARENCY.md) · [Changelog](CHANGELOG.md) · [docs/](docs/ARCHITECTURE.md)

## Licence

MIT. See [LICENSE](LICENSE).
