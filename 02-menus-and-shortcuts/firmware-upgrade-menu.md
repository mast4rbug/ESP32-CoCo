# Firmware Upgrade Menu

## Checking your current version

- Firmware V1.04+ added hardware and software revision display in the on-device menu.

## Update methods

- **SD card flash file**, via an on-device menu — no separate USB/serial flashing tool needed for routine updates.
- Firmware files are named like `CC3-BOARDV1-2-FW1-0-2.FLH` (board revision + firmware version encoded in the filename).

## Step-by-step update

1. Download the `.FLH` firmware file for your board revision (see [firmware-changelog.md](../04-management/firmware-changelog.md) for download links per version).
2. Copy the file to the **root of the SD card**.
3. On the device, press **F12** to open the **on-screen menu**, then **F** for the Firmware Upgrade menu (see [menu-navigation.md](menu-navigation.md)).
4. Select the **Flash Firmware** option from that menu and flash the new firmware.

## Release notes / changelog

- Full firmware version history, download links, and per-version release notes: [firmware-changelog.md](../04-management/firmware-changelog.md)
- Track documentation (this repo) changes separately in [../CHANGELOG.md](../CHANGELOG.md)

## Rollback

- No manual rollback should normally be needed. The ESP32 has a **dual-firmware (A/B) setup**, and if an update fails, it automatically falls back to loading the previous firmware — this self-healing is designed to hold even if power is interrupted mid-flash.

## Risks

- Under normal use, bricking risk is very low thanks to the dual-firmware fallback described in [Rollback](#rollback) above. This isn't an absolute guarantee, though — it protects against a failed or interrupted update, not against a device that's been physically tampered with (e.g. modified flash storage/bootloader) or otherwise compromised outside normal operation.
- Known-fixed-in-V1.0.2: a file corruption issue when saving to disk existed in earlier firmware — update if you're on an older version.
