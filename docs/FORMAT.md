# List format (`thoxmini-update-feed/1`)

One JSON object in `feed.json`.

```json
{"schema":"thoxmini-update-feed/1","channel":"preview","published":"2026-11-22",
 "releases":[{"line":"<release line>","version":"0.1.0","published":"2026-11-22","status":"proof of concept",
   "notes":"…","bundle":{"name":"…","bytes":0,"sha256":"<64 hex>"}}],
 "packages":[{"line":"<release line>","id":"…","name":"…","version":"1.0.0","bytes":0,"sha256":"<64 hex>"}],
 "images":[{"line":"<release line>","variant":"…","version":"0.1.0","bytes":0,"sha256":"<64 hex>"}]}
```

| Field | Meaning |
| --- | --- |
| `channel` | `preview` until there is a product release, then `stable` |
| `line` | The release line: the ThoxMini product line a file is for. It never names a part |
| `version` | `major.minor.patch`, optionally `-pre`; a prerelease sorts before its release |
| `status` | What the release is, in plain words. `proof of concept` means exactly that |
| `bundle` | The update file for that version: name, exact size, SHA-256 |
| `packages` | Optional extras a device owner can add: exact size and SHA-256 of each |
| `images` | Whole-card images used to make a new device: exact size and SHA-256 of the file as stored |

Read at most 64 KiB. The list is not signed; it is for people and tools that compare checksums.
