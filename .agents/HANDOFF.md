# Agent handoff — thox-mini-releases

- Status: v1.0.0 published 2026-11-22. Public, list-only, mirroring ttracx/thox-key-releases.
- Key files: `feed.json` (`thoxmini-update-feed/1`, releases empty), `release-feed.json`
  (`thoxmini-release-feed/1`, sequence 1, 2 model item(s): thoxmini-3b, thoxmini-phi4mini).
- Conventions: verified values only, never invent url/bytes/sha256; bump sequence on feed
  changes; `release-feed.json` is `-text`, never convert line endings.
- Blockers: release feed is UNSIGNED — no release-feed.json.sig exists. Signing is pending the
  holder of Ed25519 key `thox-release-2026-11`; no private key or signing tool was found in the
  workspace or on KnightHub in the checked locations. Consumers must not trust the feed as signed.
- Bucket: `Thox-ai/thox-device-thoxmini` is private (internal only), placeholders only at creation
  (README.md, manifest.json with artifacts: [], .keep files). Registering this feed's repo URL
  in the bucket manifest is a recorded next step, not yet done.
- Next: sign the feed; add image/firmware/software items when they exist in the bucket.
- Last verified: 2026-11-22 by Sadie (subagent lane, device release feeds).
