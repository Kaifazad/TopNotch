# ⬛ TopNotch — Floating Utility Notch & Dynamic Island for Windows

[![Tauri 2.0](https://img.shields.io/badge/Tauri-2.0-24C8DB?logo=tauri&logoColor=white)](https://tauri.app/)
[![Svelte 5](https://img.shields.io/badge/Svelte-5-FF3E00?logo=svelte&logoColor=white)](https://svelte.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Rust](https://img.shields.io/badge/Rust-1.80+-DEA584?logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Windows 11 Fluent](https://img.shields.io/badge/Design-Windows_11_Fluent-0078D4?logo=windows11&logoColor=white)](https://fluent2.microsoft.design/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**TopNotch** is a minimalist, ultra-fast floating utility notch and dynamic shelf designed natively for Windows 11 and 10. Built with **Rust (Tauri 2.0)** and **Svelte 5 Runes**, it brings a clean Apple Dynamic Island-style aesthetic to your PC.

Docked seamlessly to the top bezel of your display, TopNotch rests as a 36px hardware-style notch that reacts instantly to copied text, images, and media playback. On demand (<kbd>Ctrl</kbd> + <kbd>Space</kbd> or <kbd>Alt</kbd> + <kbd>\</kbd>), it blooms into an interactive multi-tool flyout.

---

## 🚀 Quick Download

| Platform | Format | Direct Download |
| :--- | :--- | :--- |
| **Windows 11 / 10 (64-bit)** | Standalone Installer (`.exe`) | [**Download TopNotch v0.1.0 (x64)**](https://github.com/Kaifazad/TopNotch/releases/download/v0.1.0/TopNotch_0.1.0_x64-setup.exe) |

---

## 🌟 Key Features

### 1. 🏝️ Ultra-Minimal Dynamic Island Alerts
- **Single-Line Sleek Notifications**: Instant, unobtrusive Dynamic Island alerts whenever you copy or paste.
- **Universal Content Detection**:
  - 📋 **Text / Code / Links**: Previews snippet, character count, and link tags.
  - ✨ **Images**: Visual thumbnail badge when copying or pasting screenshots and web graphics.
  - 📁 **Files / Folders**: Instant confirmation chip when copying filesystem paths.
  - 🎵 **Media Playback**: Live equalizer bars and track titles.

### 2. 🗄️ Universal Parking Shelf
- **Drag & Drop Anything**: Drag images, files, or selected text directly from your desktop, File Explorer, or web browsers (Chrome, Edge, Firefox) into the shelf.
- **Direct Notch Drop**: Drop files directly onto the resting top notch to automatically park them.
- **Clipboard Paste (`Ctrl + V`)**: Press <kbd>Ctrl+V</kbd> anywhere while the shelf is open, or click the **Paste Clipboard** button to park screenshots and copied text instantly.
- **One-Click Export**: Click any parked image or file to copy it back to your clipboard or download it to disk.

### 3. 🎯 Horizontal Repositioning
- Hover over the right edge of the notch to reveal the **6-dot tactile grip handle**.
- Click and drag horizontally along your top screen bezel to dock TopNotch anywhere—keep it centered or slide it aside so it never obscures browser tabs.

### 4. ⏱️ Focus & Productivity Timers
- **Stopwatch**: Millisecond-accurate precision with split lap recording.
- **Pomodoro Focus Arc**: 25/5 focus and break cycles with progress tracking directly on the notch.
- **Countdown Presets**: Quick-set timers for meetings and breaks.
- **Hydration Reminders**: Periodic gentle nudges to drink water throughout your workday.

### 5. 🎵 Ambient Soundscapes
- Built-in multi-channel Web Audio sound generator:
  - Rain, Thunder, Ocean Waves, White Noise, Campfire, Forest Birds, Coffee Shop, Stream, Wind, and Binaural Alpha Waves.
  - Independent channel volume mixing and instant master mute toggle.

### 6. 🚀 App Hub & Multi-Search
- **Quick Search**: Instant queries routed directly to Google, GitHub, YouTube, Perplexity AI, or StackOverflow.
- **App & Web Bookmarks**: Fast launchers for Spotify, Discord, VS Code, Notion, Terminal, and custom user-defined shortcuts saved to local SQLite.

### 7. 🔒 100% Private & Safe
- **No Administrator Rights Needed**: Runs safely under standard user mode (`asInvoker`).
- **Offline First**: All notes, clipboard items, and settings are stored locally on your device in `%LOCALAPPDATA%\TopNotch\`. Zero data is sent to external servers.
- **Windows Startup**: Optional one-click toggle in Settings to auto-launch TopNotch docked to your top bezel when your PC powers on.

---

## ⌨️ Global Keyboard Shortcuts

| Shortcut | Action |
| :--- | :--- |
| <kbd>Ctrl</kbd> + <kbd>Space</kbd> | Toggle TopNotch Shelf & Control Center |
| <kbd>Alt</kbd> + <kbd>\</kbd> | Alternative Quick Flyout Toggle |
| <kbd>Alt</kbd> + <kbd>P</kbd> | Toggle Pomodoro Focus Timer |
| <kbd>Alt</kbd> + <kbd>B</kbd> | Quick Bookmarks / Battery Status |
| <kbd>Esc</kbd> | Collapse Flyout back into Notch |

---

## 🛠️ Tech Stack & Architecture

- **Backend**: [Rust](https://www.rust-lang.org/) + [Tauri 2.0](https://tauri.app/)
  - Win32 API (`WS_EX_TOPMOST`, `WS_EX_LAYERED`, `RegisterHotKey`)
  - SQLite database with `rusqlite`
  - GSMTC (Global System Media Transport Controls)
- **Frontend**: [Svelte 5](https://svelte.dev/) with Runes (`$state`, `$derived`, `$props`)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **Styling**: Pure Windows 11 Fluent Design System with dark and light theme support.

---

## 💻 Building from Source

### Prerequisites
- [Node.js](https://nodejs.org/) (v18+)
- [Rust & Cargo](https://www.rust-lang.org/tools/install) (1.80+)

### Setup & Run
```bash
# 1. Clone repository
git clone https://github.com/Kaifazad/TopNotch.git
cd TopNotch

# 2. Install dependencies
npm install

# 3. Run in development mode
npm run tauri dev

# 4. Build production installer
npm run tauri -- build --bundles nsis
```
The installer executable will be generated at:
`src-tauri/target/release/bundle/nsis/TopNotch_0.1.0_x64-setup.exe`

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.

Developed by [Kaif Azad](https://github.com/Kaifazad).