# Release process

A build is published the same way every time, so that a replacement is visible.

1. **Hash the archive** with SHA-256 before it goes anywhere.
2. **Upload under the version tag** (`v0.1.0`), keeping the asset name stable.
3. **Re-download it** and compare byte counts and hashes with the original. If they differ, the upload failed; do not describe it as published.
4. **Write the hash into four places**: the release notes, [CHANGELOG.md](../CHANGELOG.md), [WALLET.md](../WALLET.md) and the [Windows page](../downloads/windows/).
5. **Rebuild the site** and check the live page: the hash on the internet must equal the hash of the file the button serves.
6. **Note the replacement** in the changelog if an asset was overwritten, because the URL does not change.

## v0.1.0

- Archive: `plenum-win-x64.zip`
- Size: 213,178,812 bytes
- Inside: `plenum-win-x64.exe`, 213,178,642 bytes
- SHA-256: `9fa75ce4dedfb5c6072dd3651633b6bd38eca6c340c3ff78682777fe4ab2f18e`
- Signed: no
