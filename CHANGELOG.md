# Changelog

All notable changes to this documentation set are logged here (not to be confused with ESP32-COCO firmware changes — those belong in [02-menus-and-shortcuts/firmware-upgrade-menu.md](02-menus-and-shortcuts/firmware-upgrade-menu.md)).

## 2026-07-17 (13)

- **disk-menu.md**: clarified that the Extended menu (**E**, from within the SD card file browser) is specifically what lets you create a new formatted `.DSK` or format the currently-selected `.DSK`. Resolved both the "exact menu path" and "disk sizes/formats" parts of the creating/formatting TODO — produces standard 35-track, single-sided, single-density RDOS images, ~160 KB.
- **features.md**: added the "Hi-Res Interface & CoCo Mouse" row (not supported, possibly future); removed the Debugger row and "Known in-development work" section.
- **overview.md**: removed redundant "(confirmed)" tags from prose (kept as a status label in the features.md capability matrix, where it's contrastive).
- **troubleshooting.md / video-index.md**: removed the debugger section from troubleshooting; kept the related dev-log video in the video index as general interest.
- **hardware-specs.md**: corrected the cassette port — CAS is bidirectional (in and out), CTL is the relay; connecting a real deck needs a 1/8" stereo-to-mono Y-splitter, CTL just needs a plain 1/8" mono-to-mono cable. Added "(1/8")" alongside all "3.5mm" jack mentions.
- **cassette-menu.md**: updated to match the bidirectional CAS correction; noted virtual saving is unreliable (use EXTERNAL/real deck for reliable saves); noted the CoCo ROM here is patched to show real loading progress, unlike a real CoCo. Removed speed-poke considerations (not supported, unstable on real CoCo anyway).
- **sd-card.md**: fact-checked FAT32 filename/path limits and per-folder file limits against real FAT32/VFAT specs (255-char filenames, 260-char paths, no meaningful per-folder cap — the 512-entry limit is FAT16-root-only) and corrected the page accordingly.
- **disk-menu.md / cassette-menu.md**: removed the unfilled "Troubleshooting" placeholder sections (both were empty TODO stubs).
- **firmware-upgrade-menu.md**: resolved the Rollback and Risks TODOs — the ESP32 uses a dual-firmware (A/B) setup, so a failed or power-interrupted update automatically falls back to the previous firmware, keeping bricking risk very low under normal use. Noted this isn't an absolute guarantee — it doesn't cover a physically tampered/compromised device.
- **joystick-menu.md**: removed the "unconfirmed by hands-on testing" caveat from the CoCo Port section.
- **keyboard-shortcuts.md**: removed the "Shifted graphics characters" TODO row from the CoCo key mapping table.
- **keyboard-shortcuts.md**: resolved CLEAR and ALT TODOs — CLEAR maps to PC **DEL**; CTRL and ALT map naturally to PC CTRL/ALT (added a CTRL row too).
- **keyboard-shortcuts.md**: removed the unverified claim that the CoCo keyboard had shifted punctuation/graphics symbols — couldn't confirm this for the CoCo specifically (the doc maintainer, a longtime CoCo owner, doesn't recall it either; it may have been conflated with the MC-10's keyboard, which did have this).
- **keyboard-shortcuts.md**: removed the stray bullet list duplicating F1/F2/CAPS LOCK/ESCAPE info already covered in the tables; added a CAPS LOCK row to the CoCo key mapping table instead.
- **keyboard-shortcuts.md**: expanded "Menu control shortcuts" — was just the DEL-to-eject row. Now covers the F12 main menu jump keys, the shared SD card file browser (arrows, Page UP/DOWN, HOME, BackSpace, **E** for the Extended menu), and per-menu shortcuts for Disk, Cassette, Joystick, and Modem, cross-referenced against each menu's own page.
- **keyboard-shortcuts.md**: reformatted the F12 main menu shortcut list as a table, matching the style of the other menu-control sub-sections.
- **keyboard-shortcuts.md**: removed the "Software-specific shortcuts" section (F1+O) — it's not device-specific and is already fully covered in [modem-menu.md](02-menus-and-shortcuts/modem-menu.md).
- **keyboard-shortcuts.md**: added a cassette-menu.md link under the Cassette menu shortcuts, matching the Modem menu section.
- **keyboard-shortcuts.md**: moved cross-reference links out of table cells (SD card file browser, Disk drive menu, Joystick menu) into standalone "See X.md" lines below each table, matching Cassette/Modem — consistent style across all menu-control sub-sections.
- **joystick-menu.md**: removed the top note that only Digital had been confirmed working end-to-end by the doc maintainer.
- **menu-navigation.md**: removed the Artifact Colors / F10 relationship note entirely — not necessary; the individual descriptions in the menu table and [keyboard-shortcuts.md](02-menus-and-shortcuts/keyboard-shortcuts.md) already make each control's behavior clear on its own.
- **menu-navigation.md**: removed the "Navigating" section (ESC line + cursor-navigation TODO) — the F12 main menu has no cursor/arrow navigation, everything is a direct letter-shortcut jump; the ESC-to-exit behavior is already covered in [keyboard-shortcuts.md](02-menus-and-shortcuts/keyboard-shortcuts.md). Arrow-key navigation only exists in the SD card file browser, which is documented there too.
- **modem-menu.md**: added a "Making a serial cable" section with pinout diagram (`assets/images/serial.jpg`) for wiring a 1/8" TRS serial cable to use the CoCo Hardware port mode — Tip = Receive Data From Other, Ring = Send Data To Other, Sleeve = GND, crossed to the other device's Send/Receive lines.
- **hardware-specs.md**: resolved the "documentation pending" serial port pinout TODO using the same pinout, cross-referenced to modem-menu.md.
- **media-library.md**: added the serial testing `.DSK` image (Cedric's Google Drive) to the disk images table; cross-referenced from the new serial cable section in modem-menu.md.
- **Removed** `03-compatible-hardware/display-and-av.md`: an entirely unfilled TODO stub, with the facts that mattered (VGA on all boards, HDMI on newer boards) already in [hardware-specs.md](01-getting-started/hardware-specs.md). Updated the README contents list and the "Connecting peripherals" list in setup-and-first-boot.md accordingly.
- **storage-devices.md**: removed the unfilled "max card size" and "speed class" TODOs, the "USB storage" section (USB host storage not supported/relevant), the "Known incompatible devices" section, and the top-level "TODO: verify" note — all empty TODO stubs.
- **backup-and-restore.md**: trimmed — removed the top-level TODO note, the "save states/games in progress" TODO bullet, and the entirely unfilled "Restoring" and "Preventing corruption" sections.
- **community-links.md**: clarified the "No confirmed public presence" section — it read as if there was no public presence at all, contradicting the Facebook group already listed above as the primary source. Reworded to "No other confirmed public presence" and dropped the stale GitHub-repo-gap note (long since resolved).
- **video-index.md**: filled in title, date, and notes for all three previously-TODO 8bitsinthebasement videos (info supplied by the doc maintainer directly, since YouTube blocks non-JS metadata fetches from this environment). Confirmed the channel URL is correct; removed that TODO.
- **video-index.md**: removed the empty "Tutorials" section and the closing note about checking video descriptions for links — this repo itself is the tutorial. Trimmed the top description line accordingly.
- **community-links.md**: added the CoCo Discord server (https://discord.com/invite/4J5nHXm, linked from the rSIgg4Kzkj8 video) under Broader CoCo community; removed "Discord server" from the unconfirmed-presence list.
- **Full repo verification sweep**: checked all `.md` files for null-byte padding (none found) and mid-sentence truncation (none found — every file ends on a complete sentence). Checked all 172 relative markdown/image links across the repo (excluding CHANGELOG.md's intentional historical references to old pre-renumbering paths) — found and fixed one genuinely broken link: `keyboards.md` pointed to a nonexistent `function-key-reference.md`, corrected to `keyboard-shortcuts.md`. Zero broken links remain.
- **overview.md**: added a "What's an ESP32?" explainer near the top, per Cedric's suggestion — clarifies the ESP32-S3 is a general-purpose microcontroller chip (the "32" means 32-bit, unrelated to the CoCo's own "32K" memory configs), and that it emulates a full 2 MB CoCo 3, not a stock 32K CoCo. Aimed at dispelling confusion for readers unfamiliar with the ESP32 platform.
- **utilities.md**: added a Notes column to the Joystick configuration table, flagging that Mike Horgan's Joystick Config Editor only works in Chromium-based browsers (Chrome, Edge, Brave, etc.) — not Firefox or Safari.
- **New page**: `03-compatible-hardware/cases-and-enclosures.md`, listing that Cedric hasn't published an official case STL yet, plus a community-made case (ESP32COCO Case with Joystick) that encloses both the board and the joystick expansion module. Cross-referenced from the README contents list and hardware-specs.md's Physical section. URL stripped of tracking params (fbclid, from=search) before adding.
- **README.md**: added `esp32-coco-header.jpg` as a banner image at the top, and `esp32-coco-clean.jpg` (front view showing SD/JOYL/JOYR/KEYB ports) above the "What is the ESP32-COCO?" section. A third supplied image (`esp32-coco-top.jpg`) wasn't used — available in `assets/images/` if needed elsewhere later.

## 2026-07-17 (12)

- **Fixed file corruption**: `01-getting-started/overview.md` and `02-menus-and-shortcuts/menu-navigation.md` had gotten silently truncated mid-sentence at some point, and six other files (`features.md`, `hardware-specs.md`, `sd-card.md`, `cassette-menu.md`, `disk-menu.md`, `README.md`) had trailing null-byte padding. Restored the missing content and stripped the padding; verified against a full repo sweep afterward.
- **hardware-specs.md**: confirmed there's no other enclosure option besides bare board or the 3D-printed case; resolved that TODO.
- **community-links.md**: added the ESP32-COCO Official Facebook group and the general TRS-80 Color Computer (CoCo) Facebook group (filed under broader community, not ESP32-COCO-specific).
- **utilities.md**: removed the ROM/cartridge tools and General CoCo dev tools sections (not applicable / not useful placeholders).
- **backup-and-restore.md**: resolved the "how to back up" TODO — a plain copy of the SD card's FAT32 contents to a PC is sufficient, no imaging tool needed.

## 2026-07-17 (11)

- **Added screenshots** (`assets/screenshots/`) throughout `02-menus-and-shortcuts/`, sourced from the doc maintainer's own device and verified against actual menu behavior.
- **disk-menu.md**: documented the full mount flow (Disk drive menu → SD card browser → `.DSK` preview → mounted path shown) and resolved the "does it auto-boot" TODO — it doesn't; boot via standard DECB `DIR` / `LOAD` / `RUN`.
- **cassette-menu.md**: documented the full mount flow (Cassette menu → browser → mounted WAV shown with tape position) and the `CLOADM` load sequence with progress readout — plain DECB, not device-specific.
- **joystick-menu.md**: substantially rewritten. Item 1 selects which USB port (Left/Right) you're configuring; item 2 cycles Joystick type between Digital, Analog, and CoCo Port, each with its own sub-menu (Digital: D-pad + 2 buttons; Analog: X/Y stick axis selection + 2 buttons; CoCo Port: plug-and-play, unconfirmed by hands-on testing). Only Digital has been confirmed working end-to-end so far.
- **modem-menu.md**: substantially rewritten. Corrected a prior assumption — RS-232 PAK hardware serial and the WiFi/Telnet bridge are **not independent**; item 1 is a 3-way toggle (disabled / routed to CoCo Hardware port / routed to WIFI) on the same menu. Added the full tested Twi-Term + WiFi BBS connection walkthrough (Twi-Term RS232c settings first, then WiFi config, then launch), a guest-WiFi-network recommendation (2.4GHz, simple SSID/password, WPA2-Personal, due to poor CoCo special-character support), and an experimental/instability callout (keyboard disconnects, possible device restarts).
- **menu-navigation.md**: added the F12 main menu screenshot; noted the HW/SW version display and that shortcut letters are visually highlighted on-screen.
- **firmware-changelog.md**: noted that V1.05 exists (shipped on the newest board) but is unpublished, and that future firmware is expected to fork per board revision (V1.2 vs. V1.3) since V1.3 has additional hardware.

## 2026-07-17 (10)

- **Removed** `02-features/audio.md` and `02-features/video-output.md`: both were 100% unfilled TODO placeholders, and the facts that mattered (6-bit DAC audio, mono 3.5mm jack; VGA on all boards with HDMI on newer boards) were already documented in [01-getting-started/overview.md](01-getting-started/overview.md) and [01-getting-started/hardware-specs.md](01-getting-started/hardware-specs.md).
- **Moved & renamed**: `02-features/overview.md` → `01-getting-started/features.md`, resolving the name collision with `01-getting-started/overview.md`.
- **Merged**: `02-features/rs232-wifi-telnet.md` into [02-menus-and-shortcuts/modem-menu.md](02-menus-and-shortcuts/modem-menu.md) — most of its content already lived there. The RS-232 PAK hardware serial mode (which doesn't go through the Modem menu at all) is kept as a clearly separate section at the bottom of that page.
- This emptied out `02-features/`, which was removed, closing the numbering gap: `03-menus-and-shortcuts/` → `02-menus-and-shortcuts/`, `04-compatible-hardware/` → `03-compatible-hardware/`, `05-management/` → `04-management/`, `06-resources/` → `05-resources/`. Updated all cross-references and the README contents list. Also fixed a stale `06-management` link in `setup-and-first-boot.md` left over from before the very first folder-numbering pass.

## 2026-07-17 (9)

- **Corrected**: **F1+O** does not launch Twi-Term — it's an option inside Twi-Term's own main menu once it's already running. Twi-Term is loaded the same way as any other CoCo software (via the Disk or Cassette menu). Fixed in [02-features/rs232-wifi-telnet.md](02-features/rs232-wifi-telnet.md), [03-menus-and-shortcuts/keyboard-shortcuts.md](03-menus-and-shortcuts/keyboard-shortcuts.md), and [03-menus-and-shortcuts/modem-menu.md](03-menus-and-shortcuts/modem-menu.md).

## 2026-07-17 (8)

- **New pages**: `03-menus-and-shortcuts/joystick-menu.md` and `03-menus-and-shortcuts/modem-menu.md`, for consistency with the existing disk/cassette/firmware-upgrade menu pages. Split content out of [04-compatible-hardware/joysticks-and-controllers.md](04-compatible-hardware/joysticks-and-controllers.md) (axis-configuration gotcha moved to joystick-menu.md; hardware compatibility list stays put) and [02-features/rs232-wifi-telnet.md](02-features/rs232-wifi-telnet.md) (WiFi/Telnet configuration and usage moved to modem-menu.md; RS-232 PAK hardware serial background stays put). Did not create separate pages for Artifact Colors, Vsync, or Reboot — these are single-action toggles, not worth their own page. Updated all cross-references and the README contents list.

## 2026-07-17 (7)

- **Moved & renamed**: `05-management/firmware-updates.md` → `03-menus-and-shortcuts/firmware-upgrade-menu.md`. Updated all cross-references and the README contents list accordingly.

## 2026-07-17 (6)

- **Renamed folders**: `06-management/` → `05-management/`, `07-resources/` → `06-resources/`. This closes the numbering gap left by removing `05-loading-media/`. Updated all cross-references and README section headings/numbers accordingly.

## 2026-07-17 (5)

- **Moved & renamed**: `05-loading-media/sd-card-file-management.md` → `01-getting-started/sd-card.md`. This emptied out `05-loading-media/`, which was removed. Updated all cross-references (including "Loading Media" section links, now pointing directly at [Disk Menu](03-menus-and-shortcuts/disk-menu.md) / [Cassette Menu](03-menus-and-shortcuts/cassette-menu.md)) and the README contents list accordingly.

## 2026-07-17 (4)

- **Renamed folder**: `03-controls-and-shortcuts/` → `03-menus-and-shortcuts/`. Updated all cross-references and the README section heading accordingly.

## 2026-07-17 (3)

- **Moved & renamed**: `05-loading-media/dsk-disk-images.md` → `03-controls-and-shortcuts/disk-menu.md`, and `05-loading-media/cassette-wav-files.md` → `03-controls-and-shortcuts/cassette-menu.md`. Updated all cross-references and the README contents list accordingly.

## 2026-07-17 (2)

- **Removed** `05-loading-media/cartridge-rom-images.md`: cartridge/ROM pak emulation isn't supported yet — planned for a future firmware update. Updated references in [02-features/overview.md](02-features/overview.md), [07-resources/media-library.md](07-resources/media-library.md), and [README.md](README.md). Will restore a dedicated page once the feature ships.

## 2026-07-17

- **Removed** `06-management/configuration-settings.md`: there's no separate/editable config file format to document. All settings are changed via the on-device menus and saved to a non-editable binary dump file at the SD card root. Folded this into [03-controls-and-shortcuts/menu-navigation.md](03-controls-and-shortcuts/menu-navigation.md), and updated references in [06-management/backup-and-restore.md](06-management/backup-and-restore.md) and [README.md](README.md).

## 2026-07-16

- **Removed** `02-features/coco2-vs-coco3-modes.md`: there is no separate/explicit CoCo 2 mode. The firmware emulates a CoCo 3, which is backward compatible with CoCo 2 software. Updated references in [01-getting-started/overview.md](01-getting-started/overview.md), [02-features/overview.md](02-features/overview.md), [03-controls-and-shortcuts/keyboard-shortcuts.md](03-controls-and-shortcuts/keyboard-shortcuts.md), and [README.md](README.md) accordingly.
- **Clarified**: CoCo 1 compatibility also confirmed — the difference between CoCo 1 and CoCo 2 was minimal (largely semantic), so ESP32-COCO's CoCo 3 emulation is backward compatible with both. Updated [01-getting-started/overview.md](01-getting-started/overview.md), [02-features/overview.md](02-features/overview.md), [README.md](README.md), and [glossary.md](glossary.md).

## 2026-07-08 (3)

Large content pass from the doc maintainer's own notes:

- **Hardware specs confirmed**: micro-USB power (~0.5A), VGA (some boards HDMI, less stable), SD/FAT32 storage, side expansion port for original CoCo joysticks, USB1-only keyboard/joysticks (2 joystick ports), RS-232-only 3.5mm serial jack, 3.5mm cassette in/out/relay jacks, front LED (red=power, flash green=disk activity), mono 3.5mm audio, ESP32-S3-WROOM-1 (8MB Flash, 8MB PSRAM), 2MB emulated CoCo RAM.
- **New page**: [02-features/rs232-wifi-telnet.md](02-features/rs232-wifi-telnet.md) — RS-232 PAK hardware serial + WiFi/Telnet BBS bridge, WiFi config process, compatible terminal software.
- **New page**: [06-management/firmware-changelog.md](06-management/firmware-changelog.md) — firmware V1.0.2 and V1.04 release notes, flashing file names and download link.
- Updated [06-management/firmware-updates.md](06-management/firmware-updates.md) with the actual flashing process (SD card root + F12 menu).
- Updated [03-controls-and-shortcuts/keyboard-shortcuts.md](03-controls-and-shortcuts/keyboard-shortcuts.md) and [02-features/overview.md](02-features/overview.md) with confirmed shortcuts (F3/F4 save/load state, F9 screenshot, F10 artifact toggle, F11 exit data mode, F12 flash menu, DEL eject disk, LEFT SHIFT lowercase).
- Updated [04-compatible-hardware/joysticks-and-controllers.md](04-compatible-hardware/joysticks-and-controllers.md) with a known-working controller list (Logitech RumblePad 2, Logitech Wingman Action Pad, Rii Game Controller, USB SNES-style joypad, Hyperkin Scout, one AliExpress joystick), axis-configuration tip, and expansion-port note.
- Updated [04-compatible-hardware/keyboards.md](04-compatible-hardware/keyboards.md) and [04-compatible-hardware/storage-devices.md](04-compatible-hardware/storage-devices.md) with USB1 and FAT32/SD tooling notes.
- Updated [05-loading-media/dsk-disk-images.md](05-loading-media/dsk-disk-images.md) and [05-loading-media/cassette-wav-files.md](05-loading-media/cassette-wav-files.md): DSK create/format menu options (V1.04+), DEL eject, write support confirmed, **.CAS not supported — WAV only**.
- Updated [07-resources/video-index.md](07-resources/video-index.md), [07-resources/utilities.md](07-resources/utilities.md), and [07-resources/media-library.md](07-resources/media-library.md) with 3 more creator videos, Mike Horgan's joystick config editor and CAS-to-WAV converter, SD formatter, dot-file remover, and a joystick test DSK.
- 8bitsinthebasement's 3 videos remain logged with TODO titles — could not be fetched automatically (browser tool unavailable this session).

## 2026-07-08 (2)

- Confirmed: keyboard and joystick input is USB-only, and specifically USB 1.1 (USB1) — not USB2/3. Updated [keyboards.md](04-compatible-hardware/keyboards.md) and [joysticks-and-controllers.md](04-compatible-hardware/joysticks-and-controllers.md) accordingly.
- Added first entry to the community-sourced compatible joystick list: an AliExpress USB joystick reported working (title/model TBD).
- Logged 3 videos from creator 8bitsinthebasement in [video-index.md](07-resources/video-index.md) — titles pending (couldn't be pulled automatically).

## 2026-07-08

- Initial scaffold created: full doc tree (getting started, features, controls & shortcuts, compatible hardware, loading media, management, resources), README index, glossary, and contributing guide.
- Seeded [07-resources/video-index.md](07-resources/video-index.md) and [07-resources/community-links.md](07-resources/community-links.md) with findings from initial web research (creator name, two known demo videos, no public GitHub/site found).
- All other pages are `TODO`-marked placeholders pending verified content.
