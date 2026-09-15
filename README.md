# Awesome A2VERA [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of **Apple II VERA / A2VERA** resources — hardware, emulators, games, converters and tools for bringing the VERA (Versatile Embedded Retro Adapter) FPGA video & sound card to the Apple II family.

VERA is the FPGA graphics and sound system designed by Frank van den Hoef for the Commander X16, featuring tile and bitmap modes up to 256 colors, 128 hardware sprites, and a 16-voice PSG + PCM audio engine. With the **A2VERA** adapter card, the Apple II, II+, //e and IIgs can drive a real VERA card in Slot 2 (`$C200`) or Slot 4 (`$C400`) — and a growing ecosystem of emulators, demos, and full arcade-grade game ports now targets this configuration.

## Contents

- [Hardware](#hardware)
- [Emulators](#emulators)
- [Games](#games)
- [Converters & Compilers](#converters--compilers)
- [Tools & Utilities](#tools--utilities)
- [Documentation](#documentation)
- [Talks & Videos](#talks--videos)
- [Credits](#credits)
- [Contributing](#contributing)

## Hardware

- [A2VERA — Lectronz (Wavicle)](https://lectronz.com/products/a2vera-apple-ii-vera-video-card-with-fm-audio) — Apple II adapter board (II, II+, //e, IIgs) for the VERA video card, with FM audio
- [A2VERA — Tindie](https://www.tindie.com/products/wavicle/a2vera-apple-ii-vera-video-card-with-fm-audio/) — Alternate store listing for the A2VERA board
- [VERA 8-Bit Video Card — Tindie (Wavicle)](https://www.tindie.com/products/wavicle/vera-8-bit-video-card/) — The VERA video card itself (also used in the OtterX)
- [VERA Module](https://github.com/fvdhoef/vera-module) — The original VERA FPGA module, designed by Frank van den Hoef
- [OPM2151 Drop-in Replacement for YM2151 — Lectronz (Wavicle)](https://lectronz.com/products/opm2151-drop-in-replacement-for-ym2151) — Pin-compatible, cycle-accurate FPGA replacement for the vintage Yamaha YM2151 FM-synthesis chip, included with the A2VERA kit
- [OPM2151 — Tindie](https://www.tindie.com/products/wavicle/opm2151-drop-in-replacement-for-ym2151/) — Alternate store listing for the OPM2151

## Emulators

- [Apple2TS](https://github.com/ct6502/apple2ts) — Apple II emulator in TypeScript; full VERA card emulation on Slot 2 (`$C200`) / Slot 4 (`$C400`) with a VERA Monitor debug tab ([PR #395](https://github.com/ct6502/apple2ts/pull/395)), slot auto-configuration URL params ([PR #415](https://github.com/ct6502/apple2ts/pull/415), [PR #451](https://github.com/ct6502/apple2ts/pull/451)), and VERA performance optimizations ([PR #469](https://github.com/ct6502/apple2ts/pull/469))
- [AppleWin (anomixer fork)](https://github.com/anomixer/AppleWin) — Windows emulator fork with native-speed VERA support; runs VERA titles at a smooth 60 FPS

## Games

- [Time Pilot (VERA)](https://github.com/StewBC/Time-Pilot) — Full port of Konami's 1982 arcade classic to Apple II + VERA: dual-slot support, 128 hardware sprites with 32-way rotation, VRAM-streamed PCM/PSG audio, and zero-disk runtime; featured in Apple2TS New Releases ([PR #445](https://github.com/ct6502/apple2ts/pull/445))
- [H.E.R.O. (Mine Rescue) — Apple II VERA Port](https://github.com/anomixer/x16-hero-vera) — Full port of the Activision classic with scrolling tilemaps, dynamic multi-frame sprites and a PSG chiptune soundtrack (coming soon)

## Converters & Compilers

- [smb1transpiler](https://github.com/fletto2/smb1transpiler) — Rebuild the A2VERA Apple II + VERA port of Super Mario Bros. 1 from your own NES and SNES ROMs, with only a C compiler; ships no Nintendo data

## Tools & Utilities

- [veratest](https://github.com/anomixer/veratest) — VERA graphics & sound test demo disk for real Apple II hardware and Apple2TS, including a 32MB 375-image 256-color musical slideshow
- [veramusic](https://github.com/anomixer/veramusic) — Apple II VERA music demo kit
- [verasdedit](https://github.com/anomixer/verasdedit) — Apple II VERA SD card hex sector editor
- [a2vera](https://github.com/misterblack1/a2vera) — Test programs for driving the VERA module on a real Apple II (assembly)

## Documentation

- [Understanding VERA (BoxLambda)](https://epsilon537.github.io/boxlambda/understanding-vera/) — Deep dive into the VERA architecture: VRAM block layout, scanline rendering, palette and sprite pipeline, and the iCE40 UltraPlus 5K implementation

## Talks & Videos

- [KansasFest 2026 session recording](https://www.youtube.com/watch?v=XbqqLpzCAD4) — A2VERA presentation by Michael Morrison

## Credits

- **Frank van den Hoef** — Creator and hardware designer of the VERA FPGA system
- **Michael Steil** — Commander X16 emulator architecture and core implementation
- **David Murray (The 8-Bit Guy)** — Creator and visionary of the Commander X16 project
- **Michael Morrison ([@code-bythepound](https://github.com/code-bythepound))** — Initiator of the A2VERA project; ported the VERA core to TypeScript and adapted it for Apple II / web emulation

## Contributing

Contributions are welcome! If you have built or found an A2VERA-related project — hardware, emulator support, game port, demo, converter, or utility — please open a pull request or issue to add it to this list.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
