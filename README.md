# ChromaFlow — Animated Background Studio

A modern, dependency-free animated gradient background playground built with **HTML, CSS and vanilla JavaScript**.

> Create a background visually, customize it live, then copy the CSS, embed it as HTML, download a standalone page or render a PNG wallpaper.

## ✨ Features

### Design
- 🎨 2–8 customizable gradient colors
- 🌈 **Linear, radial and conic** gradients
- 🪄 **Palette harmony generator** — analogous, complementary, triadic, tetradic and monochrome palettes from your first color
- 🔀 Reverse and shuffle the palette, one-click random palettes built from color harmonies
- 🌀 Adjustable animation speed, angle and movement scale
- 🎚️ Easing controls
- 🌫️ Background blur and overlay darkness
- ✨ Film-grain/noise effect
- 🎡 **Hue cycling** — continuously rotate the whole palette
- 🌅 8 built-in visual presets

### Workflow
- ↶ **Undo / redo history** (up to 100 steps, `Ctrl/Cmd+Z`)
- 💾 **"My presets" library** — save, re-apply and delete complete designs (stored in your browser)
- 💾 LocalStorage auto-save
- 📊 **FPS monitor** to check animation performance
- ⏸ Pause / resume animation
- 🖥️ Fullscreen preview
- ⌨️ Keyboard shortcuts
- 📱 Responsive mobile layout

### Export & share
- 📋 Copy portable CSS (matches the live preview, including keyframes and grain)
- 🧩 **Copy a ready-to-paste HTML embed**
- 🌐 **Download a standalone HTML page**
- 🖼 **Download a PNG wallpaper** (1080p, 1440p, 4K or phone portrait)
- 📤 Export and import designs as JSON
- 🔗 Share a design through a URL hash

### Quality
- 🛡️ Imported JSON, saved settings and share links are validated and clamped before use
- ♿ Respects `prefers-reduced-motion`; shortcuts keep native Space behaviour on focused controls
- 🚫 Zero runtime dependencies

## 🚀 Run

No build process is required.

1. Clone the repository.
2. Open `index.html` in a modern browser.
3. Start designing.

```bash
git clone https://github.com/arminmehraeen/Animated-Background.git
cd Animated-Background
```

You can also deploy the repository directly with GitHub Pages, Netlify, Vercel, or any static hosting service.

## 🎮 Controls

| Control | Purpose |
|---|---|
| Add color | Add another gradient stop, up to 8 |
| Randomize | Generate a harmonious palette with a new angle and speed |
| Reverse / Shuffle | Reorder the current palette |
| Generate from first color | Build a palette from the selected harmony rule |
| Presets | Apply curated color combinations |
| My presets | Save and restore complete designs |
| Gradient type | Linear, radial or conic |
| Speed | Change animation duration |
| Angle | Change linear direction or conic starting angle |
| Movement scale | Control how far the background shifts |
| Blur | Soften the background |
| Overlay darkness | Improve readability behind foreground content |
| Film grain | Add a subtle texture layer |
| Hue cycling | Continuously rotate the palette's hues |
| FPS monitor | Show the live frame rate in the status bar |
| Undo / Redo | Step through your design history |
| Pause | Freeze the animation |
| Fullscreen | Preview only the background |
| Copy CSS / HTML embed | Copy a portable snippet |
| Download HTML / PNG | Save a standalone page or a static wallpaper |
| Export / Import JSON | Save and restore a configuration |
| Share link | Encode the current configuration into the URL |

### Keyboard shortcuts

- `Space` — pause/resume
- `R` — randomize
- `H` — toggle hue cycling
- `F` — fullscreen
- `Ctrl/Cmd + Z` — undo
- `Ctrl/Cmd + Shift + Z` or `Ctrl/Cmd + Y` — redo

## 🧩 Using the exported code

- **Copy CSS** gives you the full set of rules (`.chromaflow-bg`, keyframes, vignette overlay and a `prefers-reduced-motion` fallback).
- **Copy HTML embed** wraps that CSS in a `<style>` block together with `<div class="chromaflow-bg" aria-hidden="true"></div>`; paste it anywhere in a page.
- **Download HTML** saves a complete standalone page you can open or host immediately.

For a decorative background, keep it behind your content and avoid placing important information only inside the animated layer.

## ♿ Accessibility & performance

The project intentionally uses platform Web APIs and avoids frameworks or external animation libraries. The animation uses CSS keyframes, which keeps the implementation small and easy to embed.

When the browser reports `prefers-reduced-motion: reduce`, ChromaFlow disables the continuous background motion when the corresponding option is enabled. Exported CSS includes the same fallback. This is important for users who prefer less motion.

Large blur values and hue cycling are the most expensive effects — use the FPS monitor to check them on lower-end devices.

For production websites, use moderate color contrast and the overlay control to keep text readable. Decorative background effects should never be required to understand the page.

## 📁 Project structure

```text
Animated-Background/
├── index.html      # Complete application
├── README.md       # Documentation
└── LICENSE         # MIT license
```

## 🛠️ Customization

The application state is kept in one JavaScript object. Presets can be added by extending the `PRESETS` object in `index.html`:

```js
const PRESETS = {
  MyTheme: ['#111827', '#4f46e5', '#06b6d4', '#22c55e']
};
```

Default settings are defined in `DEFAULTS`. Any value loaded from storage, a JSON file or a share link passes through `sanitize()`, so new options should be added there as well.

## 🔮 Roadmap

- [x] Conic gradients
- [x] Saved preset library
- [x] Undo / redo history
- [x] Live CSS/HTML embed snippet
- [x] Export as a standalone background page
- [x] Performance/FPS monitor
- [x] Color harmony palette generator
- [ ] Custom gradient stop positions
- [ ] Multi-layer gradients
- [ ] Full HSL / OKLCH color controls
- [ ] Optional WebGL shader effects
- [ ] Installable PWA mode

## 📜 License

MIT — see [LICENSE](LICENSE).

## 👤 Author

**Armin Mehraeen**

Repository: https://github.com/arminmehraeen/Animated-Background
