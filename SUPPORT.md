# Aerithal — Support & Player Guide

Welcome to the official support guide for **Aerithal** on macOS (by Keegan Porter / Krise Media).

---

## System Requirements

- **Operating System:** macOS 13.0 (Ventura) or later
- **Hardware:** Mac with Apple Silicon (M1 or newer) and Metal/WebGL2-capable GPU
- **Input:** Keyboard & Mouse / Trackpad, or Bluetooth/USB Xbox (Series X|S, One, 360) and PlayStation (DualSense PS5, DualShock 4) controllers via macOS `GameController.framework`
- **Network:** Optional — 100% playable offline in solo mode and over local Wi-Fi (LAN) without internet; an internet connection is required only for **Play-Anywhere 6-Character Join Code** co-op (up to 6 players)
- **Audio / Microphone:** Optional — a Mac microphone or headset is required only if you wish to speak in **In-Game Voice Chat** during co-op (listen-only mode works automatically without a microphone)

---

## Quick Start

1. **Create Your Character:** On first launch, enter a display name and choose either a **Preset** skin or design your own in the **Custom** skin maker, then click the gold checkmark.
2. **Start a World:** Click **Play** → click the **+** card → pick a world name (optional custom seed) → click **Create**. Every new world spawns safely across 14 varied scenic overworld biomes.
3. **Explore & Craft:** Gather wood and stone with **Left Click**, press **`E`** to open Inventory & Crafting, place a **Workbench** with **Right Click**, and build your way through **five realms** and **six bosses**.
4. **Pause, Co-op & Auto-Save:** Press **`Esc`** at any time to pause, copy your world's **6-character Join Code**, toggle **Co-op**, mute your mic, adjust Settings, or return to the Title screen. Aerithal auto-saves when pausing, exiting a world, or closing the window.

---

## Controls & Keybindings

Every keyboard and auxiliary-mouse bind can be remapped under **Settings → Controls** (with a **Reset** button to restore defaults).

### Keyboard & Mouse (Defaults)

| Action | Default Control |
|---|---|
| Move | `W` `A` `S` `D` |
| Look | Mouse |
| Jump / Swim Up / Roc Climb | `Space` |
| Sprint / Roc Boost | `L-Shift` (or double-tap `W`) |
| Crouch / Sneak / Edge-Guard / Roc Descend & Dismount | `F` |
| Prone / Crawl (fit through low gaps) | `L-Ctrl` |
| Dodge Dash | `L-Alt` (`Option`) |
| Mine / Sculpt / Attack | Left Click |
| Place / Use / Interact / Eat / Bow / Board Boat or Roc | Right Click |
| Pick Block (Eyedropper) | Middle Click (`Mouse 3`) |
| Inventory & Crafting | `E` |
| Hotbar Slot | `1`–`9` or Scroll Wheel |
| Drop Held Item | `Q` |
| Sculpting Brush Size | `R` |
| Sculpting Brush Shape (`Cube`, `Sphere`, `Plate`, `Cylinder`, `Hollow`, `Ramp`, `Arch`) | `V` |
| Symmetry Mirror Build Mode (`Off` / `X` / `Z`) | `X` |
| Undo Last Build Stroke | `Z` |
| World Atlas Map (Surface & Subterranean Caverns) | `M` |
| Co-op Waypoint Ping Beacon | `C` |
| Call Nearest Tamed Roc (Whistle) | `G` |
| Mute / Unmute Mic (Co-op Voice Chat) | `U` |
| Push to Talk (when enabled in Settings) | Hold `T` |
| Camera View (1st / 3rd Behind / 3rd Front) | `F5` |
| Player Roster | Hold `Tab` |
| Toggle HUD | `F1` |
| Debug Info | `F3` |
| Pause / Settings (Auto-Saves) | `Esc` |
| Fullscreen Toggle | `Cmd+F` or `F11` |

### Xbox & PlayStation Controllers (Bluetooth & USB)

Pair your controller in **System Settings → Bluetooth** or connect via USB—Aerithal detects it automatically.

| Action | Xbox | PlayStation |
|---|---|---|
| Move / Look | Left Stick / Right Stick | Left Stick / Right Stick |
| Mine / Sculpt / Attack | `RT` | `R2` |
| Place / Use / Interact / Bow / Eat | `LT` | `L2` |
| Jump / Swim Up / Roc Climb | `A` | `✕` (Cross) |
| Sneak / Roc Descend & Dismount | `B` | `○` (Circle) |
| Sprint / Roc Boost | `L3` | `L3` |
| Hotbar Previous / Next | `LB` / `RB` | `L1` / `R1` |
| Inventory & Crafting | `Y` | `△` (Triangle) |
| Brush Size / Brush Shape | `X` / `D-Pad Left` | `□` / `D-Pad Left` |
| Call Tamed Roc / Drop Item / Camera View | `D-Pad Up` / `Down` / `Right` | `D-Pad Up` / `Down` / `Right` |
| Pick Block (Eyedropper) | `R3` | `R3` |
| Pause / Player Roster | `Menu` / Hold `View` | `Options` / Hold `Share`/`Create` |

---

## Gameplay & Realm Progression Tips

- **Five Realms & Six Bosses:** Craft each boss's summoning relic at a **Summoning Altar**, then Right Click an Altar in that realm. Each realm boss drops a heart used to craft the **Keystone** for the next realm (place the Keystone on open ground to raise a **Waystone Sanctuary Pool**):
  1. **The Verdance** — *The Stone Warden* (surface) & *The Crystal Sovereign* (deep Sunken Ancient Vaults).
  2. **The Glowdeep** — *Mycora, the Spore Mother*.
  3. **Ember Reach** — *Pyrrhax, the Cinder Wyrm*.
  4. **Skyreach** — *Tempest, Lord of the Roc* (defeating Tempest unlocks wild Rocs and Golden Rocs to tame and fly!).
  5. **The Hollow** — *The Unmaker*.
- **Wooden Boats:** Craft a Wooden Boat at a Workbench, Right Click water to launch, Right Click to board, steer with `WASD`, press `F` to dismount, or hold `F` + Right Click to pick the boat back up.
- **Taming a Roc:** After defeating Tempest in Skyreach, feed wild Rocs **Roc Treats** (Right Click) until hearts appear, equip a **Saddle**, then Right Click to ride (`Space` climbs, `F` descends/dismounts on ground, `G` whistles your nearest tamed Roc).

---

## Co-op & Voice Chat Troubleshooting

Aerithal supports **1–6 players** (1 host + 5 guests) with zero account creation or server setup—either over your local Wi-Fi or across different networks using a 6-character Join Code.

### Same-Wi-Fi (LAN) Co-op
1. **Same Wi-Fi Network:** Confirm every Mac is connected to the exact same Wi-Fi network/subnet (avoid hotel or campus guest Wi-Fi with "AP/Client Isolation" enabled).
2. **Enable Co-op:** On the host Mac, open **Settings** or the **Pause** menu and confirm **Co-op** (globe icon) is turned **on**.
3. **macOS Local Network Permission:** Open **System Settings → Privacy & Security → Local Network** and make sure **Aerithal** is enabled on both the host and joining Macs.
4. **macOS Firewall:** If the macOS Firewall is enabled (**System Settings → Network → Firewall**), verify that Aerithal is allowed to accept incoming connections.
5. **Matching App Versions:** All players must run the same version and build of Aerithal. Update from the Mac App Store if you see an **Update Required** or **Version Mismatch** notice.

### Play-Anywhere 6-Character Join Codes
1. **Sharing Your Code (Host):** While loaded inside your world with **Co-op** enabled, press **`Esc`** to open the **Pause** menu and click your world's **6-character Join Code** badge to copy it to your clipboard. Each world keeps its own persistent Join Code—share it only with friends you trust.
2. **Joining by Code (Guest):** On the Title screen, open **Join**, paste or type the host's 6-character Join Code, and connect.
3. **"World Offline" Notice:** No active host was found for that Join Code. Make sure the host is currently loaded inside that world (not on the Title screen), has **Co-op** enabled, is connected to the internet, and double-check the 6 characters.
4. **"Connection Failed" Notice:** Your Macs found each other's signaling info, but a direct peer-to-peer WebRTC route could not be completed. Check your internet connection, temporarily disable strict VPNs or corporate/school firewalls that block UDP/WebRTC traffic, and confirm macOS Firewall allows Aerithal. If you are on the same Wi-Fi network, join directly from the automatic Same-Wi-Fi list instead.

### In-Game Voice Chat
1. **Auto-Activates in Co-op Only:** Voice Chat activates automatically when **2 or more players** are in the same world and **Voice Chat** is enabled in **Settings**. Your microphone is never accessed during solo play.
2. **Open Mic vs. Push to Talk:** Open **Settings** to toggle **Voice Chat**, adjust the **Voice** volume slider, or enable **Push to Talk** (hold **`T`** to speak instead of open mic). Press **`U`** anytime (or click the microphone icon in the **Pause** menu) to mute or unmute your microphone.
3. **macOS Microphone Permission:** If friends cannot hear you, open **System Settings → Privacy & Security → Microphone** and make sure **Aerithal** is toggled **on**, then verify your input device in **System Settings → Sound → Input**.
4. **Listen-Only Fallback:** If you decline macOS microphone permission or have no microphone connected, Aerithal automatically switches to **Listen-Only** mode so you can still hear your friends without interruption.

---

## Performance & Mouse Troubleshooting

- **Improving Frame Rate:** Open **Settings** and lower **View** distance (default `11`, adjustable `4`–`16`) or toggle **Shaders** off for older displays or battery play.
- **Mouse Look Not Locked:** Click once inside the game canvas after resuming from the Pause menu to re-engage pointer lock. Press `Esc` anytime to release the cursor.
- **Controller Not Responding:** Ensure the controller is paired in **System Settings → Bluetooth** (or plugged in via USB) and press any face button to switch to controller mode.

---

## Save Data & Backups

- Worlds, player profiles, and settings are stored locally inside your macOS App Sandbox:
  `~/Library/Containers/com.krisemedia.aerithal/Data/Library/Application Support/Aerithal/`
- **Deleting a World:** On the **Worlds** screen, hover over a world card and press and hold the `×` button until it fills.
- **Backups:** Because Aerithal does not use cloud servers, we recommend keeping standard macOS **Time Machine** backups enabled to protect your worlds.

---

## Contact Support

Need help with a bug, crash, or question? Email us with your macOS version, Mac model, and Aerithal version (visible under **Aerithal → About Aerithal**):

- **Email:** `k.rise.media@gmail.com`
- **Developer:** Keegan Porter / K.Rise.Media
- **Legal:** [Privacy Policy](PRIVACY_POLICY.md) · [Terms of Use](TERMS_OF_USE.md)
