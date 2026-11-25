# Privacy Policy — Aerithal

**Effective Date:** November 25, 2026  
**Developer / Publisher:** Keegan Porter / Krise Media  
**Application:** Aerithal for macOS (`com.krisemedia.aerithal`, Apple ID `6838527951`)

---

## Summary

Aerithal is built with privacy first:

- **Zero personal data collected by the developer.** We do not collect, store, sell, rent, or transmit your personal information.
- **No accounts or logins.** You can play immediately without creating an account.
- **No analytics, telemetry, crash reporting, or advertising.** Aerithal includes no tracking SDKs, ad networks, or third-party analytics.
- **100% local saves.** Worlds, character appearance, and settings stay exclusively on your Mac.
- **Play-Anywhere & Same-Wi-Fi P2P co-op.** Optional multiplayer connects peer-to-peer over your local Wi-Fi (LAN) or via encrypted 6-character Join Codes—with zero Krise Media servers or session logs.
- **Optional unrecorded P2P voice chat.** Voice chat activates only when 2 or more players are in the same world, streams live peer-to-peer over encrypted WebRTC, and is never recorded or stored.

---

## 1. Data Collected by Krise Media

**None.** Keegan Porter / Krise Media does not collect any data from Aerithal, whether linked to your identity or not. This matches our Apple Privacy Manifest (`PrivacyInfo.xcprivacy`), which declares:

- `NSPrivacyTracking`: `false`
- `NSPrivacyTrackingDomains`: none
- `NSPrivacyCollectedDataTypes`: none

Aerithal makes **no outbound internet connections** during solo play or Same-Wi-Fi (LAN) co-op. Optional Play-Anywhere remote co-op connects directly peer-to-peer via public relays/STUN servers solely to establish your session, and **never** transmits data to Keegan Porter / Krise Media.

---

## 2. Data Stored Locally on Your Mac

To save your worlds and preferences, Aerithal stores data locally inside your macOS App Sandbox container (`~/Library/Containers/com.krisemedia.aerithal/Data/Library/Application Support/Aerithal/`):

- **World Saves (IndexedDB — `aerithal`):** World names, random seeds, per-world 6-character Join Code metadata, creation and last-played timestamps, time of day, boss progression, world preview thumbnails, voxel block edits across all five realms, chest contents, entities, and player inventory/spawn data for that world.
- **Player Profile (`localStorage` — `aerithal:profile`):** A locally generated random UUID, your chosen in-game display name, and your selected preset or custom character skin.
- **Settings (`localStorage` — `aerithal:settings`):** Audio volume levels (Volume, Music, SFX, and **Voice**), view distance, field of view, mouse sensitivity, invert-Y preference, shader toggle, **Co-op** toggle, **Voice Chat** toggle, **Push to Talk** toggle, mount camera preference, and custom keyboard/mouse keybindings.

This data never leaves your Mac except as needed to play an active co-op session (described in Section 3). We have no access to your local save files.

### Managing or Deleting Your Local Data

- **Delete individual worlds:** On the **Worlds** screen, hover over a world card and press and hold the `×` button until it fills to permanently delete that world and its data.
- **Delete all app data:** Uninstall Aerithal from your Mac and remove its sandbox container directory if you wish to clear all saved worlds, profile data, and settings.

---

## 3. Optional Co-op Networking & In-Game Voice Chat

Aerithal supports optional peer-to-peer co-op play for up to 6 players via **Same-Wi-Fi (LAN)** and **Play-Anywhere 6-Character Join Codes**, along with optional **In-Game Voice Chat**. Solo play works 100% offline with zero network or microphone access.

### Same-Wi-Fi (LAN) Co-op
- **Local Network Permission:** macOS may prompt you to allow Aerithal to find and connect to devices on your local network (`NSLocalNetworkUsageDescription`). Solo play works completely offline even if you decline this permission or turn **Co-op** off.
- **Hosting Discovery:** While you are actively in a hosted world with **Co-op** turned on (accessible in **Settings** and the **Pause** menu), Aerithal broadcasts small local-only UDP discovery packets (port `41234`, multicast `239.255.42.99`, and local subnet broadcast) containing your world name, chosen in-game display name, current/maximum player count, app version/build, a random per-launch instance ID, and the host's local TCP port.
- **Discovering & Joining Locally:** On the Title and Join screens, Aerithal sends a minimal local UDP probe on port `41234` to detect hosted worlds on your Wi-Fi network and connects directly to the host Mac over local TCP. Local LAN connections enforce a strict private-network IP filter (RFC 1918, link-local, and loopback addresses only).

### Play-Anywhere Remote Co-op (6-Character Join Codes)
- **Encrypted Ephemeral Signaling:** When hosting a world with **Co-op** enabled or joining a friend remotely by entering their 6-character Join Code on the **Join** screen, Aerithal exchanges end-to-end **AES-256-GCM encrypted** ephemeral signaling messages (with both the signaling topic and encryption key derived locally from the 6-character Join Code) over public signaling relays (`ntfy.sh` and public MQTT-over-WSS brokers) alongside public STUN servers (`stun.l.google.com`, `stun.cloudflare.com`) solely to discover network routes and establish a direct peer-to-peer **WebRTC** connection (DTLS-encrypted).
- **IP Address Visibility (Standard WebRTC):** During Play-Anywhere remote co-op, your public IP address is visible to the public STUN servers, signaling relays, and the peers you connect with—this is standard to how peer-to-peer WebRTC networking functions.
- **No Developer Servers or Logs:** Keegan Porter / Krise Media operates no game servers, relays, or databases, and receives, inspects, or stores zero networking logs, IP addresses, or session data.

### Optional In-Game Voice Chat
- **Co-op Only — Never Accessed in Solo Play:** Aerithal accesses your Mac's microphone (`NSMicrophoneUsageDescription` / `com.apple.security.device.audio-input`) **only** when **2 or more players** are in the same world and **Voice Chat** is enabled in **Settings**. Your microphone is never opened or accessed during solo play.
- **Live Peer-to-Peer Audio (Never Recorded):** Voice audio streams live directly between connected peers via encrypted WebRTC (**DTLS-SRTP**). Voice audio is **never recorded, stored, logged, transcribed, or routed through developer servers**.
- **Full Player Control:** You can mute or unmute your microphone anytime by pressing `U` (or clicking the microphone icon in the **Pause** menu), enable **Push to Talk** (hold `T`) in **Settings**, adjust **Voice** volume, turn **Voice Chat** completely off in **Settings**, or decline macOS microphone permission to remain in **Listen-Only** mode.

### What Other Players See & Turning Co-op Off
- **Shared Session Info:** During an active co-op session, connected players can see your chosen in-game display name, character skin, in-game actions (movement, building, inventory/chests, visual waypoint pings), and—if **Voice Chat** is enabled—hear live peer-to-peer voice audio. Aerithal has no text chat.
- **Disabling Co-op:** Toggle **Co-op** off anytime in **Settings** or via the globe icon in the **Pause** menu to stop LAN discovery, cease Join Code signaling, and close incoming connections immediately.

---

## 4. System APIs & App Sandbox Permissions

Aerithal runs inside the macOS App Sandbox and accesses only the minimal system capabilities required for gameplay:

- **Network (`com.apple.security.network.client`, `com.apple.security.network.server`, `NSLocalNetworkUsageDescription`):** Used exclusively for optional Same-Wi-Fi LAN discovery/co-op and optional Play-Anywhere peer-to-peer WebRTC co-op.
- **Microphone (`com.apple.security.device.audio-input`, `NSMicrophoneUsageDescription`):** Used exclusively for optional live peer-to-peer co-op voice chat when 2 or more players are in the same world and **Voice Chat** is enabled. Never accessed in solo play.
- **Game Controllers (`GameController.framework`):** Optional Bluetooth and USB Xbox/PlayStation controller input handled natively by macOS.
- **Required-Reason System APIs (`PrivacyInfo.xcprivacy`):** Standard macOS/Chromium runtime APIs for local user preferences (`UserDefaults`, reason `CA92.1`), frame/simulation timing (`SystemBootTime`, reason `35F9.1`), app bundle and save file timestamps (`FileTimestamp`, reason `C617.1`), and local storage availability (`DiskSpace`, reason `E174.1`). None of these APIs are used for fingerprinting or tracking.
- **No Camera, Location, Contacts, or Photos Access:** Aerithal never requests or accesses your camera, location, contacts, or photo library.

---

## 5. Third-Party Services & External Links

Aerithal does not embed third-party analytics, advertising SDKs, social logins, or external web trackers. All game assets, fonts, and libraries are bundled directly inside the application.

When you choose to use optional Play-Anywhere remote co-op (6-character Join Codes), Aerithal contacts standard public STUN servers (`stun.l.google.com`, `stun.cloudflare.com`) and public signaling relays solely to broker encrypted, ephemeral peer-to-peer WebRTC connections. No user accounts, tracking identifiers, or personal profiles are sent to these services.

If you contact us by email for support, we receive only the information you choose to send in your email (such as your email address and message), use it solely to respond to your support request, and will delete your support correspondence upon request. Our static legal and support web pages contain no analytics scripts, advertising cookies, or tracking forms (the hosting provider processes standard web requests to deliver the pages).

---

## 6. Children's Privacy

Aerithal does not collect personal information from anyone, including children under the age of 13 (or the applicable age of digital consent in your jurisdiction). There are no accounts, no analytics, no developer servers, and no personal data collection. Parents and guardians can disable **Co-op** and/or **Voice Chat** in **Settings** at any time for solo-only or silent play.

---

## 7. Changes to This Privacy Policy

If we update Aerithal in a way that changes our privacy practices, we will update this Privacy Policy and revise the Effective Date above.

---

## 8. Contact Us

If you have questions about this Privacy Policy or Aerithal's privacy practices, please contact:

- **Developer:** Keegan Porter / K.Rise.Media
- **Email:** `k.rise.media@gmail.com`
