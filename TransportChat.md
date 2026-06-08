# TransportChat Privacy Policy

**Effective Date:** 2026-06-08  
**Developer:** Alsatian Consulting, LLC  
**Contact:** geoff@alsatian.consulting

---

## Overview

TransportChat is a peer-to-peer encrypted messaging application that operates entirely over your local network or private overlay network (Tailscale, ZeroTier, WireGuard). It requires no internet connection, no accounts, and no servers. This policy explains what data the app uses, where it stays, and what Alsatian Consulting, LLC never does with it.

---

## Data We Do Not Collect

Alsatian Consulting, LLC does **not** collect, receive, store, or process any personal information. Specifically:

- No names, email addresses, phone numbers, or account credentials are ever created or transmitted.
- No messages, files, or call audio/video are ever sent to or stored by Alsatian Consulting, LLC.
- No analytics, telemetry, crash reports, or usage statistics are collected.
- No advertising identifiers or third-party tracking SDKs are present in the app.
- No location data is collected or stored by the developer. Optional location sharing is a user-initiated, peer-to-peer action that is transmitted directly to the recipient only and is never logged or retained.

---

## Data Stored On Your Device

All app data is stored locally on your device and nowhere else:

| Data | Storage | Encryption |
|------|---------|-----------|
| Messages and chat history | On-device SQLite database | AES-256 via SQLCipher |
| Contact identities and trust records | On-device SQLite database | AES-256 via SQLCipher |
| Your cryptographic identity (key pair) | On-device SQLite database | AES-256 via SQLCipher |
| Signal Protocol session state | On-device SQLite database | AES-256 via SQLCipher |
| Received files | Device file storage (user-chosen location) | Filesystem encryption (OS-level) |

Uninstalling the app permanently deletes all locally stored data.

---

## Network Communication

TransportChat communicates only within your local network (LAN) or a private overlay network you have configured. All message content is end-to-end encrypted using the Signal Protocol (AES-256-GCM) before leaving your device.

- **No data is ever transmitted to any server operated by Alsatian Consulting, LLC.**
- Peer discovery uses UDP broadcast and multicast on your local network segment only.
- Voice and video calls use direct WebRTC connections between peers — no STUN, TURN, or cloud relay services are used.

---

## Permissions

The app requests the following Android permissions and uses them solely for the stated purpose:

| Permission | Purpose |
|-----------|---------|
| `INTERNET` | LAN socket communication and WebRTC calls |
| `ACCESS_WIFI_STATE` / `ACCESS_NETWORK_STATE` | Enumerate network interfaces for peer discovery |
| `ACCESS_FINE_LOCATION` | Required by Android OS to read Wi-Fi network details used for peer discovery — location data itself is never used, stored, or shared |
| `RECORD_AUDIO` | Voice calls (WebRTC) |
| `CAMERA` | Video calls (WebRTC) |
| `READ_MEDIA_IMAGES` / `READ_MEDIA_VIDEO` / `READ_MEDIA_AUDIO` | Attach files from device storage for peer-to-peer file sharing |
| `FOREGROUND_SERVICE` | Keep the LAN transport service running in the background so peers can receive messages |
| `RECEIVE_BOOT_COMPLETED` | Restart the background transport service after device reboot |
| `USE_BIOMETRIC` / `USE_FINGERPRINT` | Optional biometric unlock for the app lock screen |
| `VIBRATE` | Message notification feedback |
| `POST_NOTIFICATIONS` | Incoming message notifications |

---

## Biometric Data

The app offers optional biometric authentication (fingerprint or face unlock) for the app lock screen. Biometric matching is performed entirely by the Android operating system via the Android Keystore API. The app never accesses, stores, or transmits raw biometric data.

---

## Children's Privacy

TransportChat is not directed at children under 13. The app does not collect personal information from anyone, including children.

---

## Changes to This Policy

If this policy changes materially, the effective date above will be updated. Continued use of the app after a policy update constitutes acceptance of the revised policy.

---

## Contact

Questions about this privacy policy may be directed to:

**Alsatian Consulting, LLC**  
geoff@alsatian.consulting
