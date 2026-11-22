# Checking a ThoxMini™ file against this list

1. Find the entry for your release line and version in [`feed.json`](../feed.json).
2. Compute the file's SHA-256:
   - Windows: `Get-FileHash <file> -Algorithm SHA256`
   - macOS: `shasum -a 256 <file>`
   - Linux: `sha256sum <file>`
3. Compare it with the `sha256` in the list. Stop if they differ.

## Which version does my ThoxMini run?

Open ThoxOS™ on the device and go to **Devices, Updates & recovery**. The installed version is shown there.
