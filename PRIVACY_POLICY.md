# Privacy Policy — Aerithal

**Effective Date:** November 24, 2026  
**Developer / Publisher:** Keegan Porter / Krise Media  
**Application:** Aerithal for macOS (`com.krisemedia.aerithal`, Apple ID `6838527951`)

---

## Summary

Aerithal is built with privacy first:

- **Zero personal data collected by the developer.** We do not collect, store, sell, rent, or transmit your personal information.
- **No accounts or logins.** You can play immediately without creating an account.
- **No analytics, telemetry, crash reporting, or advertising.** Aerithal includes no tracking SDKs, ad networks, or third-party analytics.
- **100% local saves.** Worlds, character appearance, and settings stay exclusively on your Mac.
- **Same-Wi-Fi LAN co-op only.** Optional multiplayer connects directly over your private local Wi-Fi network—never through internet servers or developer relays.

---

## 1. Data Collected by Krise Media

**None.** Keegan Porter / Krise Media does not collect any data from Aerithal, whether linked to your identity or not. This matches our Apple Privacy Manifest (`PrivacyInfo.xcprivacy`), which declares:

- `NSPrivacyTracking`: `false`
- `NSPrivacyTrackingDomains`: none
- `NSPrivacyCollectedDataTypes`: none

Aerithal makes **no outbound internet connections** during normal solo or local co-op gameplay.

---

## 2. Data Stored Locally on Your Mac

To save your worlds and preferences, Aerithal stores data locally inside your macOS App Sandbox container (`~/Library/Containers/com.krisemedia.aerithal/Data/Library/Application Support/Aerithal/`):

- **World Saves (IndexedDB — `aerithal`):** World names, random seeds, creation and last-played timestamps, time of day, boss progression, world preview thumbnails, voxel block edits across all five realms, chest contents, entities, and player inventory/spawn data for that world.
- **Player Profile (`localStorage` — `aerithal:profile`):** A locally generated random UUID, your chosen in-game display name, and your selected preset or custom character skin.
- **Settings (`localStorage` — `aerithal:settings`):** Audio volume levels, view distance, field of view, mouse sensitivity, invert-Y preference, shader toggle, Wi-Fi Co-op toggle, mount camera preference, and custom keyboard/mouse keybindings.

This data never leaves your Mac except as needed to play an active Same-Wi-Fi co-op session (described in Section 3). We have no access to your local save files.

### Managing or Deleting Your Local Data

- **Delete individual worlds:** On the **Worlds** screen, hover over a world card and press and hold the `×` button until it fills to permanently delete that world and its data.
- **Delete all app data:** Uninstall Aerithal from your Mac and remove its sandbox container directory if you wish to clear all saved worlds, profile data, and settings.

---

## 3. Optional Same-Wi-Fi (LAN) Co-op Networking

Aerithal supports optional co-op play for up to 6 players **strictly on the same local Wi-Fi (LAN) network**. Aerithal does **not** use internet matchmaking servers, public lobbies, or third-party WebRTC relays.

When you use Same-Wi-Fi Co-op:

- **Local Network Permission:** macOS may prompt you to allow Aerithal to find and connect to devices on your local network (`NSLocalNetworkUsageDescription`). Solo play works completely offline even if you decline this permission or turn **Wi-Fi Co-op** off.
- **Hosting a World (`Wi-Fi Co-op` enabled):** While you are actively in a hosted world with **Wi-Fi Co-op** turned on (accessible in **Settings** and the **Pause** menu), Aerithal broadcasts small local-only UDP discovery packets (port `41234`, multicast `239.255.42.99`, and local subnet broadcast) containing your world name, chosen in-game display name, current/maximum player count, app version/build, a random per-launch instance ID, and the host's local TCP port.
- **Discovering & Joining Worlds:** On the Title and Join screens, Aerithal sends a minimal local UDP probe on port `41234` to detect hosted worlds on your Wi-Fi network. Joining connects directly to the host Mac over local TCP.
- **Private Network Restriction:** Aerithal enforces a strict private-network filter in code, permitting connections only to private LAN (RFC 1918), link-local, or loopback IP addresses.
- **What Other Local Players See:** During an active local co-op session, devices on your same Wi-Fi network can see your Mac's local LAN IP address, your chosen in-game display name, your character skin, and your in-game actions (movement, building, inventory/chests, and visual waypoint pings). Aerithal has no text chat or voice chat.
- **Turning Off Co-op:** You can disable **Wi-Fi Co-op** at any time in **Settings** or from the **Pause** menu (globe icon) to stop broadcasting and close incoming local connections immediately.

---

## 4. System APIs & App Sandbox Permissions

Aerithal runs inside the macOS App Sandbox and accesses only the minimal system capabilities required for gameplay:

- **Local Network (`network.client`, `network.server`):** Used exclusively for optional Same-Wi-Fi LAN discovery and co-op gameplay.
- **Game Controllers (`GameController.framework`):** Optional Bluetooth and USB Xbox/PlayStation controller input handled natively by macOS.
- **Required-Reason System APIs (`PrivacyInfo.xcprivacy`):** Standard macOS/Chromium runtime APIs for local user preferences (`UserDefaults`, reason `CA92.1`), frame/simulation timing (`SystemBootTime`, reason `35F9.1`), app bundle and save file timestamps (`FileTimestamp`, reason `C617.1`), and local storage availability (`DiskSpace`, reason `E174.1`). None of these APIs are used for fingerprinting or tracking.
- **No Camera, Microphone, Location, Contacts, or Photos Access:** Aerithal never requests or accesses your camera, microphone, location, contacts, or photo library.

---

## 5. Third-Party Services & External Links

Aerithal does not embed third-party analytics, advertising SDKs, social logins, or external web trackers. All game assets, fonts, and libraries are bundled directly inside the application.

If you contact us by email for support, we receive only the information you choose to send in your email (such as your email address and message), use it solely to respond to your support request, and will delete your support correspondence upon request. Our static legal and support web pages contain no analytics scripts, advertising cookies, or tracking forms (the hosting provider processes standard web requests to deliver the pages).

---

## 6. Children's Privacy

Aerithal does not collect personal information from anyone, including children under the age of 13 (or the applicable age of digital consent in your jurisdiction). Because there are no accounts, no internet servers, no chat features, and no data collection, parents and guardians can also disable **Wi-Fi Co-op** in Settings if they prefer solo-only play.

---

## 7. Changes to This Privacy Policy

If we update Aerithal in a way that changes our privacy practices, we will update this Privacy Policy and revise the Effective Date above.

---

## 8. Contact Us

If you have questions about this Privacy Policy or Aerithal's privacy practices, please contact:

- **Developer:** Keegan Porter / K.Rise.Media
- **Email:** `k.rise.media@gmail.com`
