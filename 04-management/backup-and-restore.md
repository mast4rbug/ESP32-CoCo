# Backup & Restore

## Why back up

SD card corruption or accidental overwrites can lose configuration, save states, and curated media collections. Regular backups are cheap insurance.

## What to back up

- Config file — a non-editable binary settings dump saved at the SD card root; see [menu-navigation.md](../02-menus-and-shortcuts/menu-navigation.md#settings-storage)
- Media collections (DSK/CAS/ROM libraries) — see [media-library.md](../05-resources/media-library.md)

## How to back up

A simple copy of the SD card's FAT32 contents to a PC (or other storage) is a good way to back up the device — no special imaging tool required. Since the card uses a standard FAT32 filesystem, any card reader and a plain file copy is enough.
