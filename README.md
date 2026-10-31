<div align="center">

# ⌨️ Typo Arcade

**A typing test that plays like an arcade game.**
Classic speed tests, a falling-words game, a daily challenge, practice that targets your weakest keys, a ghost racer, themes, sounds, XP and achievements.

**[▶ Play it](https://hemashreevi.github.io/typo-arcade/)** *(once GitHub Pages is on, see below)*

</div>

---

## 🎮 Modes

| Mode | What it is |
| --- | --- |
| **Classic** | Time (15 / 30 / 60 / 120 s), word count (10 / 25 / 50 / 100), quote, zen (type freely) or your own pasted text. Punctuation and numbers on or off. Word lists: everyday English, tricky words, code. |
| **Word Rain** | Words fall from the sky. Type one and press space to blast it before it lands. Combos multiply your score, the rain speeds up every 8 words, three lives. |
| **Daily** | The same 30 words for everyone each day, with a streak counter. |
| **Weak Keys** | Practice words built from the letters you miss most, learned from your past tests. |

## ✨ Features

- **Ghost racer:** a second cursor runs at your personal best or a speed you choose.
- **Combo flame:** a counter for correct words in a row.
- **XP, levels and 12 achievements**, plus confetti when you set a new personal best.
- **Detailed results:** wpm, accuracy, raw speed, consistency, best combo, a speed-over-time chart with errors marked, a keyboard heatmap of missed keys, and one-click practice of the words you got wrong.
- **Challenge settings:** expert (a wrong word fails the run), master (a wrong key fails the run), stop on error, no backspace, blind mode.
- **Look and feel:** 7 colour themes plus one that follows your system, 6 typing fonts, text size, caret style (line, block, underline, off), smooth caret, focus mode that hides the menus while you type.
- **Sound:** click, pop, typewriter, or melody (each key plays a note), with an error sound and volume control.
- **Works on phones** with the on-screen keyboard.
- **Stats card:** recent tests, averages, total time typing, achievements.

## ⌨️ Shortcuts

| Key | Action |
| --- | --- |
| `Tab` | Restart |
| `Esc` | Settings |
| `Ctrl` + `Backspace` | Delete the whole word |
| `Shift` + `Enter` | Finish a zen session |
| `Enter` | Next test (on the results screen) |

## ⚡ Run locally

It's a single HTML file with no build step and no dependencies.

```bash
git clone https://github.com/HemashreeVI/typo-arcade.git
cd typo-arcade
python -m http.server 8000   # then open http://localhost:8000
```

You can also just open `index.html` in a browser.

## 🌐 Deploy to GitHub Pages

**Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)` → Save.**
The game will be live at `https://hemashreevi.github.io/typo-arcade/` a minute later.

## 💾 Your data

Progress (XP, personal bests, history, achievements, missed keys) is saved in your browser's local storage only. Nothing is sent anywhere. **Settings → Data → Reset progress** clears it.

## 🗂️ How it's built

Plain HTML, CSS and JavaScript in `index.html`:

- **Typing engine:** a hidden input captures keys (so phone keyboards work); words are rendered letter by letter, and the caret is positioned by measuring the current letter.
- **Word Rain:** a canvas game loop with particles.
- **Sounds:** synthesised with the Web Audio API, so there are no audio files.
- **Charts and confetti:** drawn on canvas.
- **Fonts:** loaded from Google Fonts, with fallbacks if they don't load.

## 📄 License

MIT © Hemashree V I
