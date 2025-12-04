# 🕹️ Science Fiction Chess | Cyber Chess

A neon-soaked, responsive web chess experience that fuses classic strategy with futuristic aesthetics.  
Play against a friend, train with the built-in AI (3 difficulty tiers), or practice piece movement in Range Mode — all inside a glowing black-and-glass interface that scales from desktop to mobile.

---

## ✨ Features

| Mode | Description |
|------|-------------|
| **Tutorial Mode** | Step-by-step introduction to piece movement & rules |
| **Range Mode** | Micro-boards that isolate specific pieces to drill tactics |
| **AI Battle** | 1 | 3 | 5 level gradient (Easy → Medium → Hard) |
| **Two-Player Battle** | Pass-and-play on the same device |

### Visual / UX Highlights
- **Neon cyan & magenta glow** with CSS key-frame pulses
- **3-D floating board** (perspective + subtle bob)
- **Smooth piece animations** on every legal move
- **Click-to-move** with valid-move highlights
- **Promotion panel** auto-pops when a pawn reaches the last rank
- **Control panel**: Restart | Undo | Hint
- **Fully responsive** – board scales down to 280 px width for phones
- **PWA-ready** – just add a manifest & service-worker for offline play

---

## 🚀 Quick Start

1. Clone / download this repo  
   ```bash
   git clone https://github.com/your-username/scifi-cyber-chess.git
   cd scifi-cyber-chess
   ```

2. Serve the root folder through any static web server:  
   
```bash
   # Python 3
   python -m http.server 8000
   # Node
   npx serve .
   # VS Code Live Server extension
   ```

3. Open `http://localhost:8000` – no build step required.

---

📁 Project Structure

```
.
├── index.html      # single-file game (HTML + CSS + JS)
├── README.md
└── assets/
    └── preview.webp   # optional screenshot for social preview
```

> The entire game is one self-contained HTML file—drop it anywhere and it runs.

---

🧪 Tech Stack

- Vanilla ES6 JavaScript (no frameworks)
- CSS Grid for the 8×8 board
- CSS 3-D transforms & key-frame animations
- Media queries for responsive scaling
- Web-Fonts for Unicode chess pieces (♔ ♕ ♖ ♗ ♘ ♙ ♚ ♛ ♜ ♝ ♞ ♟)

---

🎮 Game Rules Implemented

- Full FIDE movement & capture
- Turn validation
- En-passant (ready stub – activate with flag)
- Castling (ready stub – activate with flag)
- Pawn promotion prompt (Queen, Rook, Bishop, Knight)
- Check / check-mate detection (v1.1 roadmap)

---

🤖 AI Overview

Level	Search Depth	Strategy	
Easy	1 ply	Random legal move	
Medium	3 ply	Material + mobility eval	
Hard	5 ply	Alpha-beta pruning + basic eval	

> The AI is intentionally lightweight for browser performance; replace `ai.js` with your own engine if you need ELO strength.

---

🔧 Customization

Colors & timing are CSS variables at the top of `index.html`:

```css
:root {
  --neon-cyan: #00ffff;
  --neon-magenta: #ff00ff;
  --anim-speed: 3s;
}
```

Edit them to match your favorite cyber-palette.

---

📱 PWA Upgrade (optional)

1. Add `manifest.json`  
2. Add `service-worker.js` for off-line caching  
3. Increase lighthouse score to 100 % 🎯

---

🧩 Roadmap

- Stockfish WebAssembly integration (hard mode++)
- LAN / online two-player via WebRTC
- Save / load PGN
- Themed piece skins (holographic, binary, etc.)
- Soundtrack & SFX toggle
- Dark / light neon theme switcher

PRs & issues welcome!

---

📄 License

MIT © 2025 – feel free to fork, remix, or bundle in your own projects.

---

🖼️ Preview

![Cyber Chess Screenshot](./assets/preview.webp)

> "Play the future, one square at a time."

```
