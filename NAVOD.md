# Experimental recovery for the tested Acer Iconia A1-810

**No public, portable installation package is available yet.** The following describes preparing to restore boot and system images captured from the same tablet. This backup has not yet been tested by flashing it back, and it is not known to work on other devices.

## Requirements

- An adequately charged Acer Iconia A1-810, a reliable USB cable, Windows, a working MediaTek VCOM driver, and SP Flash Tool.
- Your own verified backup of the original firmware and device-specific data, plus a verified recovery method. Never use another tablet's NVRAM or other device-specific partitions.
- A matching scatter file, `boot.img`, and `system.img` for that specific tablet. Verify their SHA-256 hashes against a reliable manifest and compare the device's partition layout before use.

The current private backup contains copies of boot and system. It does not contain the full `/data` partition, personal accounts, installed games, game data, or app updates stored in `/data`. The recovery image is a separate backup and should not be selected for a routine system restore.

## Restore with SP Flash Tool

1. Open SP Flash Tool and load the matching scatter file.
2. Uncheck every row. Select **only BOOTIMG** with the verified `boot.img` and **ANDROID** with the verified `system.img`. Double-check that no other rows are selected.
3. Use **Download Only**, start Download, and connect the powered-off tablet using the procedure appropriate to your driver. Do not disconnect it while writing. Wait for the tool's confirmation.
4. Disconnect and start the tablet. The first boot can take longer. Sign-in and user data depend on the existing `/data` partition.

**Do not use Format or Firmware Upgrade.** Do not select preloader, NVRAM, PROTECT, MBR, or EBR; they are not part of this procedure. The green confirmation alone does not prove that Android boots successfully.

## Known status

On one tested tablet, hardware graphics acceleration, Wi-Fi, Bluetooth file transfer, speaker, microphone, screen rotation, and the Play Store worked. The camera does not work yet; VPN has not been tested. The tablet may be temporarily slow after Google sign-in while synchronization and updates finish.

Google services are already present in the specific private system snapshot. This does not grant permission to distribute them publicly. Public instructions for installing Google services separately will be added only after an appropriate package and recovery procedure are verified and available for lawful distribution.
