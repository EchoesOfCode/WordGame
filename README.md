# 🔤 Worder — Daily Word Ladder Game

A daily word puzzle game where you transform one word into another by changing **exactly one letter at a time**. Every step must be a real word. Fewer steps = better score.

**[▶ Play Now](https://YOUR-USERNAME.github.io/YOUR-REPO/)**

---

## How to Play

1. You're given a **start word** (purple) and a **target word** (green)
2. Type a word that differs by **exactly one letter** from your current word
3. Every word must be a real English word
4. Reach the target in as few steps as possible
5. A new puzzle drops every day at midnight 🕛

**Example:**

```
COLD  →  start
CORD  →  changed L to R
WORD  →  changed C to W
WARD  →  changed O to A
WARM  →  changed D to M  ✓
```

---

## Features

- 🗓 **Daily puzzle** — same puzzle for everyone, resets at midnight
- 📊 **Stats tracking** — games played, win streak, average steps, personal best
- 🎉 **Confetti** on solve
- 📱 **Share on WhatsApp** — sends an emoji grid of your solution
- ⚡ **Instant word validation** — local word list + dictionary API fallback
- 💾 **No account needed** — stats saved locally in your browser

---

## Deployment (GitHub Pages)

### One-time setup

1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to **Deploy from branch → main → / (root)**
4. Your game will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO/`

### Update your URL

Open `index.html` and update line 2 inside the `<script>` tag:

```js
const SITE_URL = "https://YOUR-USERNAME.github.io/YOUR-REPO/";
```

This makes the WhatsApp share link point to your live game.

---

## Project Structure

```
/
└── index.html      # The entire game — no build step, no dependencies
└── README.md       # This file
```

No npm. No build tools. No frameworks to install. Just a single HTML file using React via CDN.

---

## Tech Stack

| Thing | How |
|---|---|
| UI | React 18 (via CDN) |
| Styling | Plain CSS (in `<style>`) |
| JSX | Babel Standalone (in-browser transpile) |
| Fonts | Space Grotesk + Space Mono (Google Fonts) |
| Word validation | Local word list + [Free Dictionary API](https://dictionaryapi.dev/) fallback |
| State persistence | `localStorage` |
| Hosting | GitHub Pages |

---

## Customisation

### Add your own word pairs
Find the `WORD_PAIRS` array near the top of `index.html`:

```js
const WORD_PAIRS = [
  ["SAND", "TRAP"],
  ["COLD", "WARM"],
  // add your own pairs here — must be same length!
];
```

Rules for adding pairs:
- Both words must be the **same length**
- There must be **a valid path** between them (you can solve it step by step)
- 4-letter words work best

### Change the game title
Search for `Ladder` in `index.html` and replace with your preferred name.

---

## License

MIT — free to use, fork, and modify.

---

*Built with [Claude](https://claude.ai)*
