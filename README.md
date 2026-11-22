# ThoxMini™ release list

[![License](https://img.shields.io/badge/license-Apache--2.0-171719)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/ttracx/thox-mini-releases?color=171719)](https://github.com/ttracx/thox-mini-releases/commits/main)
[![List](https://img.shields.io/badge/list-thoxmini--update--feed%2F1-05A451)](feed.json)
![THOX](https://img.shields.io/badge/THOX-05A451)

The public list of ThoxMini releases: versions, dates, release links and SHA-256 checksums. This
repository holds the list only. It has no source code and no downloads.

Your AI. Your Data. Your Rules.™

## Preview

No product previews yet. See [docs/previews/](docs/previews/) — screenshots are added only when they
reflect the actual shipped product.

## Quick start

```sh
curl -fsSL https://raw.githubusercontent.com/ttracx/thox-mini-releases/main/feed.json
curl -fsSL https://raw.githubusercontent.com/ttracx/thox-mini-releases/main/release-feed.json
```

## The list

[`feed.json`](feed.json), at a stable address:

```
https://raw.githubusercontent.com/ttracx/thox-mini-releases/main/feed.json
```

No ThoxMini update releases are listed yet: `releases` is empty. Entries are added as releases are
published. Format: [docs/FORMAT.md](docs/FORMAT.md).

## Downloads

This repository has no downloads. Each future entry will link to its release page or file, where the
files are. Check every downloaded file against the SHA-256 values in this list. Steps:
[docs/USER_GUIDE.md](docs/USER_GUIDE.md).

| Computer | Newest listed |
| --- | --- |
| Windows | none |
| macOS | none |
| Linux | none |

## The release feed

[`release-feed.json`](release-feed.json) lists what is current for a ThoxMini: models today, and
provisioning artifacts (images, firmware, software) registered from the private provisioning bucket
`Thox-ai/thox-device-thoxmini` as they are published. Each entry gives an address, an exact size and a SHA-256.

```
https://raw.githubusercontent.com/ttracx/thox-mini-releases/main/release-feed.json
```

| Model | Version | Bytes | SHA-256 |
| --- | --- | --- | --- |
| ThoxMini 3B | 1.0.0 | 2019373952 | `3bcfb6e420667731de4f31845fde0e78557e28db8e4ed7ea897832de30776dfa` |
| ThoxMini Phi-4 Mini | 1.0.0 | 2493840576 | `a19e96061d84ca2014d4de98d0c0397e6df4db8f73c2163afa6bcb90d15afedf` |

### Unsigned status

This feed is **unsigned**. No `release-feed.json.sig` is published for this repository yet.
Signing is pending signature by the holder of the THOX release key (`thox-release-2026-11`).
Until a signature is published and verified, consumers must not trust this feed as signed.
Format and the planned signature scheme: [docs/RELEASE-FEED.md](docs/RELEASE-FEED.md).

## Repository layout

- `feed.json` — the update list (`thoxmini-update-feed/1`).
- `release-feed.json` — the release feed (`thoxmini-release-feed/1`), unsigned pending signing.
- `docs/` — format, user guide, quick start and development docs.
- `.agents/HANDOFF.md` — agent handoff.

## Documentation map

- [docs/USER_GUIDE.md](docs/USER_GUIDE.md)
- [docs/QUICKSTART.md](docs/QUICKSTART.md)
- [docs/FORMAT.md](docs/FORMAT.md)
- [docs/RELEASE-FEED.md](docs/RELEASE-FEED.md)
- [docs/DEVELOPMENT.md](docs/DEVELOPMENT.md)

## Releases

Formal releases are on the [Releases page](https://github.com/ttracx/thox-mini-releases/releases).

## Agent handoff

See [.agents/HANDOFF.md](.agents/HANDOFF.md).

## Governance note

Public publishing (social, website, store listings, public repo flips, registries, campaigns)
requires Craig Ross's explicit approval via craig@thox.ai, CC tommy@thox.ai. This repository was
created public, list-only, on Tommy Xaypanya's CTO authority following the ThoxKey release-list
precedent (2026-11-10): versions, dates, links and checksums only, no code and no binaries.
Provisioning artifacts themselves live in the private bucket `Thox-ai/thox-device-thoxmini`, internal access only.

## License and notice

Apache License 2.0, see [LICENSE](LICENSE). [NOTICE.md](NOTICE.md) carries the THOX.ai LLC notice.
