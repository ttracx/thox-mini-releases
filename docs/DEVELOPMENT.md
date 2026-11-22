# Development

## Architecture

Static list repository. Two JSON files at the root are the product:

- `feed.json` — `thoxmini-update-feed/1`, update releases (empty at v1.0.0).
- `release-feed.json` — `thoxmini-release-feed/1`, sequence-numbered release feed.

No build, no code, no CI. Changes are edits to the JSON plus matching documentation.

## Conventions

- Never invent an entry: every `url`, `bytes` and `sha256` must come from a verified published
  artifact. Model entries at v1.0.0 reuse the exact values already published in
  ttracx/thox-key-releases.
- Provisioning artifacts are registered from the private bucket `Thox-ai/thox-device-thoxmini` only after they
  exist in that bucket and are recorded in its manifest.
- Bump `sequence` and set `published` on every release-feed change.
- `release-feed.json` is marked `-text` in `.gitattributes`: never convert its line endings.
- The feed is unsigned until the THOX release-key holder signs it. Do not add a
  `release-feed.json.sig` that was not produced by that key.

## Work log

- 2026-11-22: v1.0.0 created mirroring ttracx/thox-key-releases, unsigned.

## Known limitations

- No update releases listed yet (`feed.json` empty).
- Release feed unsigned (see README).
- No previews yet.

## Roadmap

- Sign the release feed with key `thox-release-2026-11`.
- Register ThoxMini image, firmware and software items from the private bucket as they publish.
