# Features

## Capability matrix

| Feature | Status | Notes |
|---|---|---|
| CoCo 3 emulation | Confirmed | Emulates a CoCo 3 with 2 MB of RAM, backward compatible with CoCo 1 and CoCo 2 software. There is no separate CoCo 1 or CoCo 2 mode. See [hardware-specs.md](hardware-specs.md). |
| DSK (floppy) loading | Confirmed | see [disk-menu.md](../02-menus-and-shortcuts/disk-menu.md) |
| Cassette loading | Confirmed | Virtual `.WAV` playback from SD card, or a real cassette deck via the CAS/CTL jacks — see [cassette-menu.md](../02-menus-and-shortcuts/cassette-menu.md) |
| Cartridge / ROM pak emulation | Not supported yet — planned for a future firmware update | — |
| Hi-Res Interface & CoCo Mouse | Not supported | No current plan to support it, but possible in a future update |
| Joystick support | Confirmed | 2× USB1 ports, analog + digital; see [joysticks-and-controllers.md](../03-compatible-hardware/joysticks-and-controllers.md) and [joystick-menu.md](../02-menus-and-shortcuts/joystick-menu.md) |
| Keyboard support | Confirmed | USB1 only; see [keyboards.md](../03-compatible-hardware/keyboards.md) |
| SD card storage | Confirmed | FAT32 required |
| On-screen menu / OSD | Confirmed | see [menu-navigation.md](../02-menus-and-shortcuts/menu-navigation.md) |
| Save states | Confirmed (firmware V1.04+) | F3 save / F4 load, 36 slots (0–9, A–Z) |
| Screenshot capture | Confirmed (firmware V1.04+) | F9 saves incremental `PICTUREXXXX.BMP` to SD card root |
| Artifact mode toggle | Confirmed (firmware V1.0.2+) | F10 toggles BLUE-RED / RED-BLUE artifact colors |
| Vsync enable/disable | Confirmed (firmware V1.0.2+) | improves compatibility with Twilight Terminal, reduces flicker |
| RS-232 PAK hardware serial | Confirmed (firmware V1.0.2+) | see [modem-menu.md](../02-menus-and-shortcuts/modem-menu.md) |
| WiFi / Telnet BBS bridge | Confirmed (firmware V1.0.2+) | see [modem-menu.md](../02-menus-and-shortcuts/modem-menu.md) |
| Firmware updates | Confirmed | flashed from SD card via F12 menu; see [firmware-upgrade-menu.md](../02-menus-and-shortcuts/firmware-upgrade-menu.md) |
