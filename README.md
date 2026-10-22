# King's Raid — private Android asset backup

Private integrity backup for Jordan's local historical Android restoration.
Not a public mirror, game release, license grant, or complete-game certification.
No account files, saves, credentials, APKs, or server databases are included.

## Inventory

- 24,047 files under `Android/`, totaling 8,984,024,258 bytes.
- 23,842 files from the retained Android public patch archive, checked by SHA-256.
- 205 additional files from the local Windows corpus, identical to the original
  Android declarations by length, MD5 and CRC; serialized target platform 13
  (Android), with SHA-256 captured and verified during assembly.
- `catalog/available-assets.json` gives every available path, size, SHA-256 and
  source category. No different-platform bundle has been renamed or substituted.
- Largest files remain below 100,000,000 bytes. Files are stored in ordinary Git,
  not Git LFS. History is uploaded in bounded batches.

The historical build-1558 Android manifest declares 32,174 unique asset paths.
24,044 declared assets are available, plus 3 original patch-tracking files.
8,130 declared paths remain absent and are listed in `catalog/missing-assets.json`.
Many absent paths are alternate quality/language variants. Their presence under
another name does not prove that the game will automatically use a fallback.
French-language restoration is currently deferred.

Two explicit English download selections have no missing declared paths:

| Selection | Files | Bytes | Scope of result |
| --- | ---: | ---: | --- |
| Medium assets + Mid videos | 16,974 | 5,216,278,411 | Static path coverage only |
| Original assets + Mid videos | 16,972 | 7,223,982,448 | Static path coverage only |

See `catalog/english-medium-video-mid.json` and
`catalog/english-original-video-mid.json`. Neither catalog proves the client's
actual selection, automatic fallback, exhaustive 4.86.6 compatibility, or play.

## Compatibility and download rules

The target client remains Android ARM 4.86.6. The retained build-1558 corpus has
supported bounded real-device play, but exhaustive version compatibility and all
chapters are not validated. This repository preserves available original bytes;
it does not manufacture missing data or certify full historical completeness.

`Android/patch.bjs` and `Android/PatchInfo/patch.json` are preserved archive
metadata, not assertions that all declared downloads are present. A downloader
must use the available-assets catalog, pin an immutable repository commit, verify
size and SHA-256 before activation, and never treat an absent entry as downloaded.

Private download authentication must be supplied by the owner on the device.
Never embed a GitHub token in an APK, repository, URL or diagnostic log.
The Android downloader is not implemented by this backup alone.

## Sources and preservation

Source archive and Windows files are retained locally unchanged. The assembly
receipt records the pinned integrity-evidence hashes and unchanged source metadata.
Only public game cache paths were read, without mounting or booting the archive.
Proprietary resources remain subject to their owners' rights; private storage does
not grant permission for public redistribution. Do not change repository visibility.
