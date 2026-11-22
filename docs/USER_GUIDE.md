# Using the ThoxMini™ release list

## What this is

The public list of ThoxMini releases: versions, dates, release links and SHA-256 checksums.
List data only. It has no source code and no downloads. Provisioning artifacts (OS images,
firmware, software and models) are held in the private THOX bucket `Thox-ai/thox-device-thoxmini` and are
available to internal users only.

## Check what is current

1. Open [`release-feed.json`](../release-feed.json) for the current models and, as they are
   published, provisioning artifacts.
2. Open [`feed.json`](../feed.json) for update releases. It is empty for now: no ThoxMini update
   releases have been published yet.

## Verify a download

1. Download the file from the address the feed lists.
2. Compute its SHA-256 and compare it with the feed entry. Stop if the value differs.
3. Check the file size matches the feed's `bytes` value exactly.

```sh
shasum -a 256 <downloaded-file>
```

## Signature status

The release feed is unsigned. No `release-feed.json.sig` is published yet, and the feed must
not be trusted as signed until the THOX release-key holder signs it. SHA-256 checks above still
protect individual downloads against corruption, but they do not authenticate the list itself.

## Troubleshooting

- **Feed does not load:** use the stable raw addresses in the README.
- **Checksum mismatch:** delete the download and fetch it again from the listed address. Do not
  provision a device from a file whose checksum differs.
- **Bucket access denied:** the provisioning bucket is private by design. Internal users sign in
  with their THOX Hugging Face access; there is no public download from the bucket.
