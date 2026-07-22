# Keyboard Shortcuts

> Confirmed shortcuts below are sourced from firmware release notes (V1.0.2, V1.04) and community reports. Remaining TODOs still need verification.

## System / device shortcuts

| Shortcut | Action |
|---|---|
| **F12** | Open the on-screen menu — Disk drive, Cassette, Joystick, Modem, Firmware Upgrade, Artifact Colors (NTSC CoCo 2), Vsync, and Reboot. See [menu-navigation.md](menu-navigation.md). |
| **ESC** | From the F12 menu: sends BREAK and returns to the CoCo screen |
| **F10** | Toggle artifact mode between BLUE-RED and RED-BLUE (firmware V1.0.2+) |
| **F11** | Exit data mode / return to command mode (WiFi-Telnet mode only) — see [modem-menu.md](modem-menu.md) |
| **F9** | Save a screenshot — incremental `PICTUREXXXX.BMP` written to SD card root (firmware V1.04+) |
| **F3** | Save State — 36 slots available (0–9, A–Z) (firmware V1.04+) |
| **F4** | Load State (firmware V1.04+) |
| **CAPS LOCK** | Toggles upper/lower case |
| **LEFT SHIFT** | Types lowercase during text entry (e.g. WiFi SSID/password configuration) |

## Emulated CoCo keys / PC keyboard mapping

The original CoCo 3 keyboard has keys and combinations with no direct PC equivalent. This section maps physical/USB keyboard input to CoCo key codes.

| CoCo key | PC/USB keyboard equivalent on ESP32-COCO |
|---|---|
| BREAK | ESCAPE |
| CLEAR | DEL |
| CTRL | Same as PC keyboard CTRL |
| ALT | Same as PC keyboard ALT |
| F1 | Same as PC keyboard F1 |
| F2 | Same as PC keyboard F2 |
| CAPS LOCK | Toggles upper/lower case |
| Up-arrow | Sends as `0x53` (also displays an up-arrow on screen) |
| Back-arrow (left) | Sends as `0x08` |
| Down-arrow | Sends as `0x10` |
| Right-arrow | Sends as `0x09` |


## Menu control shortcuts

### F12 main menu

| Shortcut | Action |
|---|---|
| **D** | Jump to the Disk drive menu |
| **C** | Jump to the Cassette menu |
| **J** | Jump to the Joystick menu |
| **M** | Jump to the Modem menu |
| **F** | Jump to the Firmware Upgrade menu |
| **A** | Jump to Artifact Colors |
| **V** | Jump to Vsync |
| **R** | Jump to Reboot |

Full table with descriptions: [menu-navigation.md](menu-navigation.md).

### SD card file browser (Disk menu and Cassette menu)

| Shortcut | Action |
|---|---|
| **Arrow UP/DOWN** | Move selection |
| **Page UP/DOWN** | Scroll by page |
| **HOME** | Jump to SD card root |
| **BackSpace** | Up one folder level |
| **E** | Open the Extended menu — create a new formatted `.DSK` or format the selected `.DSK` (Disk menu only, firmware V1.04+) |
| **ESC** | Exit the browser |

See [disk-menu.md](disk-menu.md) for how the Extended menu is used to create/format disks.

### Disk drive menu

| Shortcut | Action |
|---|---|
| **0 / 1 / 2 / 3** | Select a drive slot to assign/view a mounted `.DSK` |
| **DEL** | Remove/eject a mounted disk from any drive (0–3) (firmware V1.04+) |

See [disk-menu.md](disk-menu.md) for the full mounting/booting walkthrough.

### Cassette menu

| Shortcut | Action |
|---|---|
| **S** | Toggle tape source between VIRTUAL (SD card `.WAV`) and EXTERNAL (real deck via CAS/CTL jacks) |

See [cassette-menu.md](cassette-menu.md) for the full loading/saving walkthrough.

### Joystick menu

| Shortcut | Action |
|---|---|
| **1** | Select LEFT or RIGHT joystick port to configure |
| **2** | Cycle joystick type: Digital, Analog, CoCo Port |
| **3–6** | Type-specific configuration items (D-pad/buttons for Digital; X/Y stick and buttons for Analog) — item numbers vary by type |

See [joystick-menu.md](joystick-menu.md) for per-type configuration details.

### Modem menu

| Shortcut | Action |
|---|---|
| **1** | Cycle RS-232 PAK routing: disabled / CoCo Hardware port / WIFI |
| **2** | Set WiFi SSID |
| **3** | Set WiFi password |
| **R** | Reboot to apply changes (same as F12 main menu Reboot) |
| **ESC** | Return to the F12 main menu |

See [modem-menu.md](modem-menu.md) for the full connection walkthrough.

## Notes

- Keyboard must negotiate at USB Low Speed (1.5 Mbps) for any of these to register — see [keyboards.md](../03-compatible-hardware/keyboards.md)
