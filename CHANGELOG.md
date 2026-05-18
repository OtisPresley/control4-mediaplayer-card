# Changelog
All notable changes to this project will be documented in this file.

---

## [0.1.2] - 2026-05-18
### 🐛 Fixed
- 🛡️ **Bulletproof Detection**: Changed platform check to strictly use the `control4_mediaplayer` slug in the card and editor to prevent collision with official or other community Control4 integrations.

## [0.1.1] - 2026-05-17
### 🚀 Added
- 🔍 **Smart Zone Discovery**: Replaced hard-coded entity strings with dynamic source-list matching to auto-discover zones on the same amplifier!
- 🏷️ **Dynamic Prefix Cleanup**: Implemented a "Longest Common Prefix" algorithm to automatically detect and remove device names from zone labels, handling any custom naming scheme!

## [0.1.0] - 2026-05-16
### Added
- 🎉 **Initial Release**: Gorgeous, Source-Centric custom Lovelace Card for the Control4 Matrix Amplifier.
- 🪟 **Glassmorphism Design**: Sleek, modern UI with background blur and frosted glass aesthetics.
- 🎛️ **Dynamic Active Zones**: Automatically detects and displays volume controls for zones listening to the selected source.
- 🎨 **Visual Editor**: Full support for the native Home Assistant UI editor—no YAML required!
