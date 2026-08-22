# Changelog

## [Unreleased]

### Added

### Changed

### Fixed

- Double NMI each frame in Soul Blazer (France): `$4200` NMI enable during
  vblank now requires the RDNMI latch still set, so `LDA $4210` / `STA $4200`
  no longer fires a second NMI and the image no longer jumps several times
  per second.


## [v0.0.2]

### Added

- Pause-menu **Controls** profiles (Auto / L/R / Face / Mario): GAME+A/B = L/R on Zelda; Mario layout for Mario HW.

### Changed

- Improved pad logo by eduardofilo

### Fixed

- Bad RDNMI bit 7 management, fix Soul Blazer France hang at start.


## [v0.0.1] - 2026-08-12

Initial public release.

### Install

- Unzip the release archive onto the SD card root (`cores/snes.bin`).
- Place ROMs under `/roms/snes/`
