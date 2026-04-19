<div align="center">

<img src="icons/android-chrome-512x512.png" width="128" alt="Desmos Text I/O" />

# Desmos Text Input/Output Tool

**Import and export Desmos graphs as JSON — in one click.**

[![Firefox](https://img.shields.io/badge/Firefox-Add--on-FF7139?style=flat-square&logo=firefox)](https://addons.mozilla.org/en-US/firefox/addon/desmos-text-input-output)
[![Chrome](https://img.shields.io/badge/Chrome-Web_Store-4285F4?style=flat-square&logo=googlechrome)](https://chromewebstore.google.com/detail/desmos-text-inputoutput-t/hlfkanpboagfaeakfmfbgbmbbfdgmdic)
[![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)](./LICENSE)
[![Manifest](https://img.shields.io/badge/Manifest-V3-brightgreen?style=flat-square)](./manifest.json)

</div>

---

A browser extension for Chrome and Firefox that lets you export any Desmos graph as raw JSON and import it back — useful for backups, sharing, or building on top of someone else's work.

## Features

- **Export graphs** — Save any Desmos calculator state as JSON with one click, copied straight to clipboard
- **Import graphs** — Paste JSON into the editor and load it directly into Desmos
- **Ace editor** — Syntax-highlighted, validated JSON editor built into the popup
- **Dark mode** — Full dark theme support
- **Keyboard shortcuts** — Faster workflow without reaching for the mouse
- **Cross-browser** — Works on both Chrome and Firefox via Manifest V3

---

## Installation

### Firefox

Install from the [Firefox Add-ons store](https://addons.mozilla.org/en-US/firefox/addon/desmos-text-input-output), or load temporarily for development:

1. Download the latest release from the [releases page](https://github.com/jedbillyb/desmos-text-input-output-tool/releases)
2. Open Firefox and go to `about:debugging`
3. Click **This Firefox** → **Load Temporary Add-on**
4. Select `manifest.json` from the downloaded extension folder

### Chrome

Install from the [Chrome Web Store](https://chromewebstore.google.com/detail/desmos-text-inputoutput-t/hlfkanpboagfaeakfmfbgbmbbfdgmdic), or load unpacked for development:

1. Go to `chrome://extensions/`
2. Enable **Developer mode**
3. Click **Load unpacked** and select the extension directory

---

## Usage

1. Navigate to [desmos.com/calculator](https://www.desmos.com/calculator)
2. Click the extension icon in your browser toolbar

**To export:**
- Click **Export** — the graph's JSON is copied to your clipboard

**To import:**
- Paste JSON into the editor
- Click **Import** — the graph loads into Desmos immediately

---

## Development

### Stack

- Manifest V3
- Ace editor (bundled) for JSON editing with syntax highlighting and validation
- Content scripts for Desmos page integration
- `webextension-polyfill` for cross-browser compatibility

### File Structure

```
desmos-text-input-output-tool/
├── icons/                  # Extension icons (16, 32, 48, 64, 128px)
├── manifest.json           # Extension manifest (V3)
├── popup.html              # Popup UI
├── popup.css               # Popup styles
├── popup.js                # Popup logic
├── content.bundle.js       # Content script for Desmos pages
├── injected.js             # Script injected into the Desmos context
├── ace.bundle.js           # Bundled Ace editor
└── webextension-polyfill.js
```

---

## Contributing

Pull requests are welcome. For larger changes, open an issue first to discuss what you'd like to change.

---

## License

MIT — see [LICENSE](LICENSE) for details.

---

<div align="center">
<sub>MIT © <a href="https://github.com/jedbillyb">jedbillyb</a> · Made with ❤️</sub>
</div>
