# Changelog

## [v0.0.3]

### Added

- Pause-menu **Controls** profiles (Auto / Zelda / Mario): natural face map;
  GAME+A/B = L/R; on Mario HW, TIME+A/B = X/Y.

### Changed

- Nothing.

### Fixed

- Double NMI each frame in Soul Blazer (France): `$4200` NMI enable during
  vblank now requires the RDNMI latch still set, so `LDA $4210` / `STA $4200`
  no longer fires a second NMI and the image no longer jumps several times
  per second.


## [v0.0.1] - 2026-08-12

Initial public release.

### Install

- Unzip the release archive onto the SD card root (`cores/snes.bin`).
- Place ROMs under `/roms/snes/`
