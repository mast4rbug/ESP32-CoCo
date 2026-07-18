# SD Card

> TODO: verify every detail below.

## Filesystem requirements

- **FAT32 is required.**
- If you have formatting trouble (especially on cards that came pre-formatted exFAT, or larger cards), use the [SD Card Formatter tool](https://www.sdcard.org/downloads/formatter/) from the SD Association to force a proper FAT32 format.
- **Mac users**: macOS Finder litters SD cards with hidden `._` metadata files, which can confuse the device's file browser. Use [Remove Dot Files](https://maccrafters.com/apps/Remove-Dot-Files.zip) by Floyd Resler to strip them out before use.

## Folder structure

**No specific folder structure is required.** Files can be loaded from anywhere on the SD card — the on-device file browser (see [Disk Menu](../02-menus-and-shortcuts/disk-menu.md) / [Cassette Menu](../02-menus-and-shortcuts/cassette-menu.md)) lets you navigate to wherever your files live.

That said, naming folders and files clearly and simply is still a good idea for your own convenience when browsing menus on-device — but that's purely for tidiness, not a requirement.

Community collections like the [COCO-SDC archive](https://colorcomputerarchive.com/repo/Disks/Coco%20SDC/Image/) are a good source of inspiration for organizing a card — most regular RDOS `.DSK` files from it work fine.

## Naming conventions

- ESP32-COCO is fairly tolerant of longer filenames, including special characters and spaces.
- Follows standard FAT32/VFAT limits: filenames up to **255 characters**, full path up to **260 characters**.

## Transferring files to the card

Simple: remove the SD card, put it in a card reader on your computer, copy your files onto it, then put the card back in the device and power it on. See [Inserting/removing the SD card](#insertingremoving-the-sd-card) — always power off first.

## Organizing large collections

- No meaningful files-per-folder limit — standard FAT32 directories aren't capped at the old 512-entry FAT16 root-directory limit; a FAT32 directory can hold up to 65,536 32-bit entries (each long filename consumes multiple entries), which works out to many thousands of files per folder in practice.
- TODO: subfolder support / browsing depth in the on-device file picker

## Inserting/removing the SD card

- **Always power off the device before inserting or removing the SD card.**

## Backing up

- See [backup-and-restore.md](../04-management/backup-and-restore.md)

## See also

- [Disk Menu](../02-menus-and-shortcuts/disk-menu.md) — loading/mounting DSK images
- [Cassette Menu](../02-menus-and-shortcuts/cassette-menu.md) — loading/mounting WAV cassette files
