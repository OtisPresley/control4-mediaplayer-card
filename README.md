# Control4 Media Player Card: Home Assistant Plugin

[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-41BDF5?logo=home-assistant&logoColor=white&style=flat)](https://www.home-assistant.io/)
[![HACS Badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg)](https://hacs.xyz)
[![Stars](https://img.shields.io/github/stars/OtisPresley/control4-mediaplayer-card?label=Stars&color=41BDF5)](https://github.com/OtisPresley/control4-mediaplayer-card/stargazers)
[![License: MIT](https://img.shields.io/badge/nse-MIT-e0b416.svg)](https://github.com/OtisPresley/control4-mediaplayer-card/blob/main/LICENSE)
[![HACS](https://img.shields.io/github/actions/workflow/status/OtisPresley/control4-mediaplayer-card/hacs.yaml?branch=main&label=HACS)](https://github.com/OtisPresley/control4-mediaplayer-card/actions/workflows/hacs.yaml)

A gorgeous, **Source-Centric** custom Lovelace Card featuring a Glassmorphism design, built exclusively for the [Control4 Media Player](https://github.com/OtisPresley/control4-mediaplayer) integration for Home Assistant.

---

## Installation

### HACS (recommended) - ⭐ PR Pending

You can install this card directly from HACS:

[![Open your Home Assistant instance and show the repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=OtisPresley&repository=control4-mediaplayer-card)

🚫 **No manual resource configuration is required.**

This card includes its editor automatically, so you do **not** need to add any additional JavaScript resources under  
**Settings → Dashboards → Resources**.

After installation, reload your browser cache. The card will then be available as:

**Custom: Control4 Glass Source Card**

---

### 🔁 Migrating from Manual to HACS Installation (Important)

If you previously installed this card manually using resource URLs, follow these steps to safely migrate to the HACS-managed version:

1. 🗑️ **Remove old resources** from  
   **Settings → Dashboards → Resources**
   - Remove:
     ```
     /local/control4-mediaplayer-card.js
     ```

2. 📂 **Delete the old manually installed files** from: `/config/www/` or wherever you placed them.
3. ✅ **Install the card via HACS** using the HACS button above.

4. 🔄 **Reload your browser cache**

Once complete, everything will be fully managed by HACS and you will continue to receive automatic updates.

---

### Manual installation

1. Download the `control4-mediaplayer-card.js` file from the `dist/` folder and place it in Home Assistant here:
`/config/www/community/control4-mediaplayer-card/`

2. Add **only one** JavaScript resource under  
**Settings → Dashboards → Resources**:

   ```yaml
   url: /local/community/control4-mediaplayer-card/control4-mediaplayer-card.js
   type: module
   ```
   ⚠️ Do NOT add a separate editor resource. The editor is embedded in the card.
   
---

## Features

- 🎯 **Source-Centric Design**: Tie a Home Assistant media player (e.g., Spotify) directly to a Control4 Amplifier Input.
- 🔊 **Dynamic Active Zones**: Automatically detects and displays volume controls for zones currently listening to the selected source.
- 🪟 **Glassmorphism UI**: Sleek, modern design with background blur and frosted glass aesthetics that matches artwork colors!
- 🎨 **Visual Editor**: Full support for the native Home Assistant UI editor—no YAML required!

<img width="32%" alt="image" src="https://github.com/user-attachments/assets/5bb373a9-de7a-4310-bd27-4356ad52330e" />
<img width="32%" alt="image" src="https://github.com/user-attachments/assets/c6709698-3234-470b-8600-a00d8d488685" />
<img width="32%" alt="image" src="https://github.com/user-attachments/assets/b904325e-602a-49d1-9723-17d3d9770549" />

---


## 🚀 Configuration & Usage

### ⚙️ Card Options
When you add the card to your dashboard, you can configure it using the visual editor. Here are the available options:

- **Title**: The title displayed at the top of the card (e.g., "Command Center").
- **Default Zone**: Select the zone that should be active by default when the card loads.
- **Unjoin Default Input**: Specify the input that a zone should switch back to when you "Unjoin" or unlink it from a group (defaults to the first available input if not set).
- **Mappings**: This is where the magic happens! You map your **Amplifier Input Names** to your **Home Assistant Media Players** (e.g., mapping Input `Spotify` to `media_player.spotify`). This allows the card to fetch artwork and control playback!

### ⭐ Managing Favorites
The card allows you to save your favorite inputs or specific media commands for quick recall:
- **Save a Favorite**: Click the ⭐ icon next to the media info.
- **Add Manual Favorite**: Click the `+` icon in the Favorites section to manually define a name, target input, and command (e.g., "Play NPR").
- **Recall**: Click a favorite chip to instantly switch the zone to that input and send the command to the mapped player!
- **Delete**: Click the `x` on a favorite chip to remove it.

### 🔗 Linking & Unlinking Zones (Multi-Room Audio)
Since the legacy amplifier firmware does not support native hardware linking, this card simulates multi-room audio by grouping zones to the same source:
- **Link a Zone**: Click on a grayed-out zone chip in the "Linked Zones (Join)" section. This will switch that zone to the *same input* as your current active zone, and it will now show up with its own volume slider!
- **Unlink a Zone**: Click on a highlighted blue zone chip. This will switch that zone back to its default input (or the first available input), removing it from the group.

---

## Support

- Open an issue on the [GitHub tracker](https://github.com/OtisPresley/control4-mediaplayer-card/issues) if you run into problems or have feature requests.
- Contributions and feedback are welcome!

If you find this card useful and want to support development, you can:

[![Buy Me a Coffee](https://img.shields.io/badge/Support-Buy%20Me%20a%20Coffee-orange)](https://www.buymeacoffee.com/OtisPresley)
[![Donate via PayPal](https://img.shields.io/badge/Donate-PayPal-blue.svg)](https://paypal.me/OtisPresley)

---

## License
This project is licensed under the terms of the [MIT license](LICENSE).
