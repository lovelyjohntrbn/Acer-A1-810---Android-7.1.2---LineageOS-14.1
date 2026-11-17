# Android 7 for Acer Iconia A1-810

An experimental port of LineageOS 14.1 (Android 7.1.2) to the Acer Iconia A1-810. This repository contains the project website and installation documentation.

[Project website](index.html) · [Installation guide](NAVOD.md)

The guide links to the historical **A1-810 Unlock and CWM** and SP Flash Tool procedure used as a reference when preparing the development device; its third-party downloads and suitability for other tablets have not been verified.

Android, hardware graphics acceleration, Wi-Fi, audio, microphone, Bluetooth, the motion sensor, Google services, and the Play Store have been tested on one tablet. A game was downloaded and played. The camera does not work yet, and VPN has not been tested. These observations do not guarantee the same result on other devices.

## Before publishing a release

- Verify a portable installation package and a successful restore on another device. The existing raw system snapshot was taken from one tablet and has not been restore-tested.
- Never publish private partition dumps, `/data`, NVRAM, PROTECT, serial numbers, MAC addresses, or credentials.
- Establish the rights and licenses for vendor binaries and Google applications before distributing them. Do not host Google packages without the necessary rights.
- Add a real download link only after a release is prepared and verified. Include the version, SHA-256 hashes, and verification instructions.
- Verify the restore procedure and conditions for other tablets, including partition layouts and drivers.

## GitHub Pages

This directory can be used as the root of a standalone repository. In repository settings choose **Pages → Deploy from a branch**, select the branch with these files, and choose `/ (root)`. The site is static and requires no build step.

The site has no download button yet because a public release has not been established. If you would like to support the project, you can [donate via PayPal](https://paypal.me/lovelyjohntrbn).
