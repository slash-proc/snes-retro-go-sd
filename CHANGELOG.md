# Changelog

## [v0.0.6] - 2026-09-16

### Fixed

- Added a faster Select-key profile without L/R button access.
- Fixed key mapping and startup for Soul Blazer and Pilotwings.

## [v0.0.5] - 2026-09-13

### Changed

- Publish conservative runtime save and savestate support metadata for LFS sizing.

## [Unreleased]

## [v0.0.4] - 2026-09-09

### Changed

- The manifest's `kind` is now `core`, not `emulator`. A core that emulates
  nothing -- Doom -- showed that the old word named a subset rather than the
  set, so the spec took the general term and the SDK and the spec now agree.
  The previous release publishes the old value and no longer validates.


## [v0.0.3] - 2026-09-08

### Added

- Published under the [GWRG distribution
  spec](https://github.com/slash-proc/gwrg-dist-spec): a `manifest.json`
  describing this core and the systems it provides, an offline bundle, and a
  GitHub Pages mirror of `dist/` that a web installer can read without a human
  in the loop.
- `symbols[]` publishes the linked ELF so a crash address from a device can be
  resolved back to a function. It is named by the manifest and mirrored, but is
  not part of the install set and never reaches the card.
- `gwrg.json`, the hand-written half of the manifest: the short console name,
  whether compressed ROMs work, and any BIOS this core needs. Everything else —
  the systems, their folders, extensions and browse mode, the firmware ABI,
  sizes and hashes — is derived from the packed binary at release time.

### Changed

- `scripts/make_manifest.py`, `build_dist.py`, `make_bundle.py` and
  `stage_release.py` are now the shared copies, byte-identical across every
  project. A script that has to be edited on the way in is a script that drifts.
- The launcher tab is now "Super Nintendo" rather than "SNES", with "SNES"
  kept as the short name for narrow places.

### Fixed

- Double NMI each frame in Soul Blazer (France): `$4200` NMI enable during
  vblank now requires the RDNMI latch still set, so `LDA $4210` / `STA $4200`
  no longer fires a second NMI and the image no longer jumps several times
  per second.


## [v0.0.2]

### Added

- Pause-menu **Controls** profiles (Auto / L/R / Face / Mario): GAME+A/B = L/R on Zelda; Mario layout for Mario HW.

### Changed

- Nothing.

### Fixed

- Nothing.

### Install

- Unzip the release archive onto the SD card root (`cores/snes.bin`).
- Place ROMs under `/roms/snes/`
