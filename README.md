# LAPTag — Release Feed

This is the **public update-feed** for **LAPTag**, a Windows build of the open-source,
local-first photo manager [Lap](https://github.com/julyx10/lap), extended into a
combined **photo + family-genealogy** system.

This repository holds **only the downloadable release artifacts and the updater
manifest** — there is no source code here. It exists so the app's built-in
auto-updater (and anyone who wants to install it) can reach the installers
anonymously. The application's source lives in a separate private fork.

## Download & install

Grab the latest release from the [Releases page](../../releases/latest):

| File | What it is |
| :-- | :-- |
| `LAPTag_<version>_x64_en-US.msi` | Windows installer (MSI) — recommended |
| `LAPTag_<version>_x64-setup.exe` | Windows installer (NSIS) — also what auto-update runs |

> Windows SmartScreen may warn "unknown publisher" on first run — click **More
> info → Run anyway**. Code-signing (Authenticode) is intentionally not applied,
> matching upstream.

## What LAPTag adds on top of Lap

- **Photo-genealogy fusion** — link photos to people and family events, with a
  Gramps bridge and a family-tree canvas.
- **XMP sidecars as the interface** — metadata and face regions live in
  standards-based sidecar files, so the library can be rebuilt from the photos
  themselves.
- **LAN photo ingest from phones** — a companion Android ingest app and a web
  viewer, served by the desktop app on your local network.
- **Culling & dedup** — visual-similarity grouping with keep-best selection.
- **OCR search** — find text printed inside photos, indexed locally.

Everything runs **on your own machine**: no cloud account, no forced upload.

## Auto-update

Installed LAPTag builds check the manifest in the latest release here
(`latest.json`) and verify each artifact against LAPTag's own signing key. The
release feed must remain public for auto-update to work.

## About this fork

LAPTag is a private fork of [julyx10/lap](https://github.com/julyx10/lap), an
open-source local-first photo manager. It ships the same offline-first,
privacy-focused philosophy, extended for personal and family photo-genealogy
workflows. This repo currently distributes **Windows** installers.
