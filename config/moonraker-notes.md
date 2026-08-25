# Moonraker and Mainsail notes

- Raspberry Pi Zero 2 W runs the 64-bit Debian/Klipper host.
- Mainsail provides browser control, G-code file management and status.
- MCU communication was changed from the attempted UART arrangement to USB and has remained stable.
- Klipper service restart behaviour was configured for reliable recovery.
- Keep the USB 5 V path deliberate; avoid unintended back-powering between supplies.

## Before publishing configuration files

Remove or redact:

- Wi-Fi network names and passwords.
- API keys and access tokens.
- Publicly unsuitable hostnames or local addresses.
- Unique MCU serial paths unless deliberately supplied as an example.

