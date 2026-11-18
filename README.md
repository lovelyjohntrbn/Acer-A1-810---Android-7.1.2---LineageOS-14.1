# LineageOS 14.1 for Acer Iconia A1-810

An unofficial Android 7.1.2 Nougat port for the Acer Iconia A1-810.

[GitHub Releases](https://github.com/lovelyjohntrbn/Acer-A1-810---Android-7.1.2---LineageOS-14.1/releases) · [1.1.0-beta release notes and installation guide](RELEASE-NOTES-1.1.0-beta.md) · [Project website](index.html)

## What's new in 1.1.0-beta

- Both cameras support photos and video with sound. The front camera records at up to 640 × 480.
- Wi-Fi scan results use corrected timestamps. The synthetic `NVRAM WARNING` entry is hidden from the network list.
- A startup helper restarts SystemUI once to recover the navigation buttons and notification shade. The interface briefly disappears during the restart.

## Tested on the development tablet

Hardware graphics acceleration, touch, screen rotation, Wi-Fi, Bluetooth file transfer, speaker, microphone, and both cameras work on one A1-810. The camera fixes were also tested after reboot. A clean install of the packaged images and compatibility with other tablets remain untested.

## Installation

Use the package for **Acer Iconia A1-810** with SP Flash Tool in **Download Only** mode. Back up your device and verify the SHA-256 checksum and partition layout before flashing. The [installation guide](RELEASE-NOTES-1.1.0-beta.md) covers the exact partition selections and links to the original unlock and recovery procedure.

Google apps are installed separately. Play Protect certification remains unresolved, and VPN is untested.

[Support development via PayPal](https://paypal.me/lovelyjohntrbn)
