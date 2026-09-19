# Awesome A2VERA [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of **Apple II VERA / A2VERA** resources — hardware, emulators, games, converters, and tools for bringing the VERA (Versatile Embedded Retro Adapter) FPGA video & sound card to the Apple II family.

VERA is the FPGA graphics and sound system designed by Frank van den Hoef for the Commander X16, featuring tile and bitmap modes up to 256 colors, 128 hardware sprites, and a 16-voice PSG + PCM audio engine. With the **A2VERA** adapter card, the Apple II, II+, //e, and IIgs can drive a real VERA card in Slot 2 (`$C200`) or Slot 4 (`$C400`) — powering a growing ecosystem of emulators, demos, development tools, and arcade-grade game ports.

## Contents

- [Hardware](#hardware)
- [Emulators](#emulators)
- [Games](#games)
- [Converters & Compilers](#converters--compilers)
- [Tools, Demos & Utilities](#tools-demos--utilities)
- [Documentation](#documentation)
- [Talks, Videos & Media Coverage](#talks-videos--media-coverage)
- [Credits](#credits)
- [Contributing](#contributing)

## Hardware

- [A2VERA — Lectronz (Wavicle)](https://lectronz.com/products/a2vera-apple-ii-vera-video-card-with-fm-audio) — Apple II adapter board (II, II+, //e, IIgs) for the VERA video card with FM audio (also available on [Tindie](https://www.tindie.com/products/wavicle/a2vera-apple-ii-vera-video-card-with-fm-audio/)).
- [Open VERA Module](https://ifilot.github.io/open-vera-module/) — Community-maintained open-source fork of the VERA module, offering KiCad hardware designs, FPGA bitstream firmware, and testing tools for understanding or building VERA cards.
- [OPM2151 Drop-in Replacement for YM2151 — Lectronz (Wavicle)](https://lectronz.com/products/opm2151-drop-in-replacement-for-ym2151) — Pin-compatible, cycle-accurate FPGA replacement for the vintage Yamaha YM2151 FM-synthesis chip, included with the A2VERA kit (also on [Tindie](https://www.tindie.com/products/wavicle/opm2151-drop-in-replacement-for-ym2151/)).
- [VERA 8-Bit Video Card — Tindie (Wavicle)](https://www.tindie.com/products/wavicle/vera-8-bit-video-card/) — The VERA video module itself, featuring dual video outputs and SPI SD card interface.
- [VERA Module](https://github.com/fvdhoef/vera-module) — The original VERA FPGA module design by Frank van den Hoef.
- [VeraBridge](https://github.com/ifilot/VeraBridge) — Arduino Mega-based hardware driver and standalone smoke-test rig for VERA modules; tests VRAM readback, display modes, sprites, tile scrolling, PSG audio, and SPI SD card reading over an 8-bit parallel bus without requiring a host computer.

## Emulators

- [Apple2TS](https://github.com/ct6502/apple2ts) — Modern Apple II emulator in TypeScript featuring comprehensive VERA card emulation on Slot 2 (`$C200`) and Slot 4 (`$C400`), real-time VERA Monitor debugger ([PR #395](https://github.com/ct6502/apple2ts/pull/395)), automated slot URL parameters ([PR #415](https://github.com/ct6502/apple2ts/pull/415), [PR #451](https://github.com/ct6502/apple2ts/pull/451)), rendering performance boosts ([PR #469](https://github.com/ct6502/apple2ts/pull/469)), and native VERA SPI SD card mounting with animated drive UI ([PR #472](https://github.com/ct6502/apple2ts/pull/472)).
- [AppleWin (anomixer fork)](https://github.com/anomixer/AppleWin) — Windows emulator fork with native-speed VERA support, running VERA titles smoothly at 60 FPS.

## Games

- [H.E.R.O. (Mine Rescue)](https://github.com/anomixer/x16-hero-vera) — Apple II + VERA port of the Activision classic, featuring smooth multi-directional scrolling tilemaps, dynamic multi-frame sprites, and an authentic PSG chiptune soundtrack (W.I.P.).
- [Time Pilot (VERA)](https://github.com/anomixer/Time-Pilot) — Full port of Konami's 1982 arcade classic to Apple II + VERA: dual-slot support, 128 hardware sprites with 32-way rotation, VRAM-streamed PCM/PSG audio, and zero-disk runtime; featured in Apple2TS New Releases ([PR #445](https://github.com/ct6502/apple2ts/pull/445)).

## Converters & Compilers

- [aloevera](https://github.com/yeastplume/aloevera) — Command-line graphical asset processing pipeline in Rust that converts modern images into VERA-ready tilesets, tilemaps, sprites, and bitmaps for ca65 assembly or raw binary output.
- [gimp-vera-tileset-plugin](https://github.com/jestin/gimp-vera-tileset-plugin) — GIMP plugin to export indexed images into VERA-compatible tileset and palette binaries.
- [Prog8](https://github.com/irmen/prog8) — A structured, high-level programming language and compiler targeting 6502/65C02 systems. Features first-class support for VERA registers and VeraFX hardware acceleration, making it an excellent development environment for A2VERA software.
- [smb1transpiler](https://github.com/fletto2/smb1transpiler) — Rebuild the Apple II + VERA port of Super Mario Bros. from your own NES and SNES ROMs using standard C compilers; contains no copyrighted Nintendo assets.
- [tmx2vera](https://github.com/jestin/tmx2vera) — Command-line tool that converts Tiled `.tmx` maps into binary tile layers and collision maps directly loadable into VERA VRAM.

## Tools, Demos & Utilities

- [a2vera](https://github.com/misterblack1/a2vera) — 6502 assembly test routines and diagnostics suite for driving the VERA module on a real Apple II, including SD-DIAG, SD-HIRES, and SD-SLIDES.
- [Furnace](https://github.com/tildearrow/furnace) — Multi-system chiptune tracker with first-class native support for both the VERA 16-channel PSG and the YM2151 / OPM2151 FM synthesis chips (Commander X16 / cross-platform VERA tool).
- [veramusic](https://github.com/anomixer/veramusic) — Apple II VERA music demo disk highlighting PSG chiptune playback and multi-voice sound synthesis.
- [verasdedit](https://github.com/anomixer/verasdedit) — Interactive on-screen hexadecimal sector editor and raw inspection utility for VERA SPI SD cards on Apple II.
- [veratest](https://github.com/anomixer/veratest) — Comprehensive graphics and sound test demo disk for real Apple II hardware and Apple2TS, featuring a 32MB 375-image 256-color musical slideshow.
- [ZSound](https://github.com/ZeroByteOrg/zsound) — Standardized audio engine and toolset for VERA PSG, PCM, and YM2151 FM audio, defining the streaming `.ZSM` music format (Commander X16 audio framework).

## Documentation

- [Understanding VERA (BoxLambda)](https://epsilon537.github.io/boxlambda/understanding-vera/) — Deep dive into the VERA architecture: VRAM block layout, scanline rendering pipeline, palette and sprite generation, and the iCE40 UltraPlus 5K FPGA implementation.
- [VERA Programmer's Reference](https://github.com/X16Community/x16-docs/blob/master/VERA%20Programmer's%20Reference.md) — The official and authoritative technical reference covering VERA register maps, video layers, sprite attributes, PSG audio, and SPI controllers.

## Talks, Videos & Media Coverage

- [KansasFest 2026 Session Recording](https://www.youtube.com/watch?v=XbqqLpzCAD4) — A2VERA presentation by Michael Morrison detailing the hardware concept, architecture, and live software demos.

## Credits

- **Adrian Black ([@misterblack1](https://github.com/misterblack1))** — Creator of the `a2vera` hardware test and diagnostic suite (SD-DIAG, SD-HIRES, SD-SLIDES).
- **David Murray (The 8-Bit Guy)** — Creator and visionary of the Commander X16 project.
- **Frank van den Hoef** — Creator and hardware designer of the VERA FPGA system.
- **Michael Morrison ([@code-bythepound](https://github.com/code-bythepound))** — Initiator of the A2VERA emulator project; creator of the VERA TypeScript core port for Apple II emulation in Apple2TS.
- **Michael Steil** — Commander X16 emulator architecture and core implementation.
- **Wavicle** — Hardware designer and creator of the A2VERA adapter board and OPM2151 FM module.

## Contributing

Contributions are welcome! If you have built or found an A2VERA-related project — hardware, emulator support, game port, demo, converter, or utility — please open a pull request or issue to add it to this list.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
