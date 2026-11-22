# ESP32 alarm clock - firmware releases

Firmware images for the ESP32-S3 alarm clock with internet radio. This repository only holds
**releases**; the clock checks the latest one from *Settings → About → Check for update*.

Each release contains:

- `alarmclock-<version>.bin` - the application image
- `manifest.json` - version, download URL, size, SHA-256 and an ECDSA P-256 signature

The clock installs an image only if its signature matches the public key built into the running
firmware. The new firmware goes into the second app slot; if it does not start properly, the clock
returns to the previous version automatically.

Release images never contain Wi-Fi credentials or other personal settings.
