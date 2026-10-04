# AMD Hackintosh — working EFI backup

Built with generous amounts of AI-generated slop, guided by hardware details, logs, and testing — somehow resulting in a working system in about 5 hours.

Hardware:
- ASUS TUF GAMING B550M-PLUS
- RTL8125 2.5GbE
- Ryzen 7 5700G
- Radeon RX 6800

Working system: macOS Tahoe 26.7.1, OpenCore 1.0.8.

This repository contains only the OC directory from the internal EFI.

SMBIOS identifiers SystemSerialNumber, MLB, SystemUUID and ROM are
intentionally empty. Generate and insert your own SMBIOS values before use.
This sanitized configuration is not ready to boot as-is.

The original active EFI was not modified.

The optional VIA PCIe USB card personality (X162) is commented out in
`EFI/OC/Kexts/USBMap.kext/Contents/Info.plist` by default. Remove the surrounding
XML comment only if you have that card and need its optional/unreliable map.
