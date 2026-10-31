# Wallet notes

## What v0.1.0 is

A Windows x64 build that generates, stores and prints keys and derives `Z` addresses from them. It is a key holder, not a full node: there is no chain to synchronise, no peers to find, and no balance to display.

| Item | Value |
| --- | --- |
| Archive | `plenum-win-x64.zip` |
| Size | 213,178,812 bytes |
| Inside | `plenum-win-x64.exe`, 213,178,642 bytes |
| Signature | none, unsigned |
| Release | https://github.com/plenum-core/plenum-wallet/releases/tag/v0.1.0 |
| SHA-256 | `9fa75ce4dedfb5c6072dd3651633b6bd38eca6c340c3ff78682777fe4ab2f18e` |

## Verify before running

```
certutil -hashfile plenum-win-x64.zip SHA256
```

The output must equal the hash above, character for character. The same value is printed in the release notes, in [CHANGELOG.md](CHANGELOG.md), in [README.md](README.md) and on <https://plenum-core.github.io/plenum/downloads/windows/>.

## Keys

The wallet prints keys so they can be written down. That is the backup method: paper, in your own handwriting, stored where you keep documents you cannot afford to lose. There is no cloud backup, no recovery service, and no support address that can restore anything.

## What it will not do

- Show a balance or a transaction history: there is no chain.
- Send coins: there is nobody to send to and no network to relay a transaction.
- Update itself: the build has no update mechanism and connects to no host on start.

## Later versions

A Linux build and a macOS build do not exist. No date is promised for either.
