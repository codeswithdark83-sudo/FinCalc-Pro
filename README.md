# FinCalc Pro ⚡

> A sleek, glassmorphism-styled Progressive Web App combining a scientific calculator with live currency conversion — installable on any device, works offline.

![FinCalc Pro](FinCalc Pro Thumbnail.png)

---

## ✨ Features

- **Scientific Calculator** — Supports `sin`, `cos`, `tan`, `log`, parentheses, and chained expressions
- **Live Currency Converter** — Real-time exchange rates via the [Frankfurter API](https://www.frankfurter.app/), with visual up/down indicators
- **PWA Support** — Fully installable on desktop and mobile; works offline via Service Worker caching
- **Glassmorphism UI** — Smooth frosted-glass design with animated background shapes and ripple effects
- **Dark / Light Theme** — Toggled instantly, with persistent visual contrast across both modes
- **Keyboard Support** — Full keyboard input including numbers, operators, `Enter`, `Backspace`, and `Escape`
- **Currency Swap** — One-click swap between source and target currencies with animated button
- **Responsive Design** — Mobile-first layout, optimized for all screen sizes

---

## 📸 Preview

| Light Mode | Dark Mode |
|---|---|
| *(screenshot)* | *(screenshot)* |

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | CSS3 (Custom Properties, Glassmorphism, CSS Grid) |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | [Orbitron](https://fonts.google.com/specimen/Orbitron) via Google Fonts |
| Icons | [Font Awesome 6](https://fontawesome.com/) |
| Exchange Rates | [Frankfurter API](https://www.frankfurter.app/) (free, no key required) |
| PWA | Web App Manifest + Service Worker |

---

## 📁 Project Structure

```
FinCalc-Pro/
├── main.html          # App shell & keypad layout
├── ui.css             # All styles (themes, glassmorphism, grid, responsive)
├── logics.js          # Calculator engine, currency fetching, keyboard & PWA logic
├── manifest.json      # PWA manifest (name, icons, theme colors)
├── service-worker.js  # Offline caching strategy
├── favicon.svg        # Browser tab icon
└── icons/
    ├── icon-192.png   # PWA icon (standard)
    └── icon-512.png   # PWA icon (high-res)
```

---

## 🚀 Getting Started

No build tools or dependencies required — just open the file.

### Option 1 — Open Directly

```bash
# Clone the repo
git clone https://github.com/your-username/fincalc-pro.git
cd fincalc-pro

# Open in browser
open main.html
```

> **Note:** For PWA features (install prompt, Service Worker, offline support) you must serve the app over HTTP/HTTPS — Service Workers don't run on `file://` URLs.

### Option 2 — Local Dev Server

```bash
# Using Python (built-in)
python -m http.server 8080

# Using Node.js (npx)
npx serve .
```

Then visit `http://localhost:8080/main.html` in your browser.

### Option 3 — Deploy (Recommended for PWA)

Host the files on any static server. Recommended platforms:

- [GitHub Pages](https://pages.github.com/)
- [Vercel](https://vercel.com/)
- [Netlify](https://netlify.com/)

---

## 💱 Supported Currencies

| Flag | Code | Currency |
|---|---|---|
| 🇺🇸 | USD | US Dollar |
| 🇮🇳 | INR | Indian Rupee |
| 🇪🇺 | EUR | Euro |
| 🇬🇧 | GBP | British Pound |
| 🇯🇵 | JPY | Japanese Yen |
| 🇦🇺 | AUD | Australian Dollar |
| 🇨🇦 | CAD | Canadian Dollar |

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|---|---|
| `0–9` | Input digit |
| `+ - * /` | Operators |
| `.` | Decimal point |
| `Enter` or `=` | Calculate |
| `Backspace` | Delete last character |
| `Escape` | Clear display |

---

## 📦 PWA Installation

When accessed over HTTPS, browsers will show an **Install** prompt (or click the download icon in the app header). Once installed:

- Launches in standalone mode (no browser chrome)
- Works fully offline using cached assets
- Gets its own home screen / taskbar icon

---

## 🔌 API Reference

Exchange rates are fetched from the **Frankfurter API** — free, no authentication required.

```
GET https://api.frankfurter.app/latest?from=USD&to=INR
```

Rate indicators:
- 🟢 Green + `↑` — rate increased since last fetch
- 🔴 Red + `↓` — rate decreased since last fetch

---

## 🧩 Roadmap

- [ ] More currencies (CHF, CNY, SGD, AED…)
- [ ] Calculation history log
- [ ] Radian / Degree mode toggle for trig functions
- [ ] Percentage-to-decimal auto conversion
- [ ] Share / copy result button

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first.

```bash
# Fork → Clone → Create branch → Commit → Push → PR
git checkout -b feature/your-feature-name
```

---

## 📄 License

© 2026 | All Rights Reserved By Jatin Kr. Koli

---

<p align="center">Built with ❤️ by Jatin Kr. Koli</p>
