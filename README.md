# ChromaFlow — Animated Background Studio

A modern, dependency-free animated gradient background playground built with **HTML, CSS and vanilla JavaScript**.

> Create a background visually, customize it live, then copy the CSS or export the design as JSON.

## ✨ Features

- 🎨 2–8 customizable gradient colors
- 🌈 Linear and radial gradients
- 🌀 Adjustable animation speed, angle and movement scale
- 🎚️ Easing controls
- 🌫️ Background blur and overlay darkness
- ✨ Film-grain/noise effect
- 🌅 8 built-in visual presets
- 🎲 One-click random palette generator
- ⏸ Pause / resume animation
- 🖥️ Fullscreen preview
- 💾 LocalStorage auto-save
- 📤 Export and import designs as JSON
- 📋 Generate and copy reusable CSS
- 🔗 Share a design through a URL hash
- ⌨️ Keyboard shortcuts
- 📱 Responsive mobile layout
- ♿ Respects `prefers-reduced-motion`
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
| Randomize | Generate a new palette and animation |
| Presets | Apply curated color combinations |
| Speed | Change animation duration |
| Angle | Change linear gradient direction |
| Movement scale | Control how far the background shifts |
| Blur | Soften the background |
| Overlay darkness | Improve readability behind foreground content |
| Film grain | Add a subtle texture layer |
| Pause | Freeze the animation |
| Fullscreen | Preview only the background |
| Copy CSS | Copy a portable CSS animation snippet |
| Export JSON | Save the current configuration |
| Import JSON | Restore a saved configuration |
| Share link | Encode the current configuration into the URL |

### Keyboard shortcuts

- `Space` — pause/resume
- `R` — randomize
- `F` — fullscreen

## 🧩 Using the generated CSS

The **Copy CSS** action gives you the core animated gradient rules. You can paste them into another project and adapt the selector/keyframe name to your application.

For a decorative background, keep it behind your content and avoid placing important information only inside the animated layer.

## ♿ Accessibility & performance

The project intentionally uses platform Web APIs and avoids frameworks or external animation libraries. The animation uses CSS keyframes, which keeps the implementation small and easy to embed.

When the browser reports `prefers-reduced-motion: reduce`, ChromaFlow disables the continuous background motion when the corresponding option is enabled. This is important for users who prefer less motion.

For production websites, use moderate color contrast and the overlay control to keep text readable. Decorative canvas/background effects should never be required to understand the page.

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

Default settings are defined in `DEFAULTS`.

## 🔮 Roadmap

Potential future releases:

- [ ] Custom gradient stop positions
- [ ] Conic gradients
- [ ] Multi-layer gradients
- [ ] HSL / OKLCH color controls
- [ ] Saved preset library
- [ ] Undo / redo history
- [ ] Live CSS/HTML embed snippet
- [ ] Export as a standalone background component
- [ ] Optional WebGL shader effects
- [ ] Performance/FPS monitor
- [ ] Installable PWA mode

## 📜 License

MIT — see [LICENSE](LICENSE).

## 👤 Author

**Armin Mehraeen**

Repository: https://github.com/arminmehraeen/Animated-Background
