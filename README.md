# Morse Key

A single-file, dependency-free Morse key **and** text encoder/decoder that runs entirely in the browser with a smooth audio sidetone, LED/background flash, and persistent settings.

## ✨ Features
- **Hold-to-key** button with mouse/touch/pen; **Space**/**Enter** also work (keys are ignored while a text field is focused).
- **Live capture & decode** (International Morse): shows `·`/`−` stream and decoded text in real time.
- **Text → Morse encoder** (live) with punctuation support.
- **Audio sidetone** at ~650 Hz with gentle attack/release to avoid clicks.
- **LED indicator** and optional **background glow** while keying.
- **Volume & flash intensity** sliders; preferences **persist in localStorage**.
- **No build, no deps** — just open `index.html`.

## 🧭 How to Use
1. Open `index.html` in any modern browser.
2. Press and hold **HOLD TO KEY** (or press **Space/Enter**) to send.
3. Watch **Morse input** (`·`/`−`) and **Decoded** text update live.
4. Type in **Type text to encode** to get **Encoded Morse**.

> **Timing model (WPM-ish):** dot unit ≈ **140 ms**; dash = **3×** dot; **letter gap = 3×**, **word gap = 7×**.

## ⚙️ Settings
- **Vol**: sidetone loudness (0–100%).
- **Flash**: scales LED glow and background-glow intensity.
- **LED**: toggle small indicator.
- **BG Glow**: toggle page-wide glow on key down.
- Settings persist via `localStorage` keys:
  - `morse:lights` (`"1"`/`"0"`), `morse:bg`, `morse:vol` (0–100), `morse:flash` (20–200).

## ⌨️ Shortcuts
- **Space / Enter**: key down/up (when focus is *not* in an input/textarea).
- **Clear**: reset captured stream and decoded text.

## ♿ Accessibility
- Semantic controls with ARIA labels and **status live region**.
- Big target for the key; keyboard operable; visual indicators can be reduced (LED/BG toggles).

## 🔧 Customize (quick hacks)
- **Speed/WPM**: change `UNIT` (ms) in the script (default `140`).
- **Tone**: adjust oscillator frequency (`650` Hz).
- **Alphabet**: extend `MAP` (text→Morse) — `RMAP` is derived automatically.

## 🧪 Browser Support
Modern Chromium, Firefox, and Safari (Web Audio + Pointer Events). No network, service workers, or cookies.

## 📦 Deploy
- **GitHub Pages**: push this repo, then enable Pages (deploy from `main`/`/root`).  
- Any static host works (Netlify, Vercel, Cloudflare Pages, local file).

## 🗺️ Roadmap (good first issues)
- Configurable **WPM** and element/word gap ratios.
- **Playback** of encoded Morse (audio + light).
- **Copy/Share** buttons and export/import sessions.
- **Practice mode** (drills, accuracy, speed stats).
- Optional **dark/light** auto theme.
- Mobile haptics (where supported).

## 🤝 Contributing
PRs welcome. Keep it **single-file** unless a change materially improves UX/maintainability.  
Run basic manual tests across desktop/mobile and at least one non-Chromium engine.

## 🛡️ Privacy
All processing is local; only small preferences are stored in `localStorage`.

## 📄 License
MIT — see `LICENSE`.

---
