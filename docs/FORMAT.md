# List format (`thoxmini-update-feed/1`)

One JSON object. `releases` holds one entry per published ThoxMini release, oldest first.
It is currently empty: no ThoxMini update releases have been published yet.

```json
{"schema":"thoxmini-update-feed/1","channel":"stable","releases":[]}
```

| Field | Meaning |
| --- | --- |
| `host` | `windows`, `macos` or `linux` |
| `version` | `major.minor.patch`, optionally `-pre`; a prerelease sorts before its release |
| `tag` | The release tag |
| `published` | UTC date the release was published |
| `release_url` | The release page, where the files are |
| `package_sha256` | SHA-256 of the sealed package that release matches |
| `assets` | Every file attached to the release, with its SHA-256 |

Readers should refuse duplicate keys and non-finite numbers, use the newest entry for their own
computer type, and send no account, device or computer details with the request.
