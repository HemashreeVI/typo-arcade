<div align="center">

<img src="assets/banner.svg" alt="Typo Arcade: a typing test that plays like an arcade game" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2600&pause=700&color=FFB454&center=true&vCenter=true&width=720&height=44&lines=%E2%8C%A8%EF%B8%8F+Type+fast.+Blast+words.+Level+up.;%F0%9F%8C%A7%EF%B8%8F+Word+Rain%3A+stop+the+words+before+they+land;%F0%9F%91%BB+Race+your+own+ghost;%F0%9F%93%85+One+daily+challenge+for+everyone;%F0%9F%8E%AF+Practice+that+learns+your+weak+keys" alt="Typing animation"/>

<p>
  <a href="https://hemashreevi.github.io/typo-arcade/"><img src="https://img.shields.io/badge/▶_play_now-FFB454?style=for-the-badge&labelColor=1A1833" alt="Play now"/></a>
  <img src="https://img.shields.io/badge/modes-4-6EE7C8?style=for-the-badge&labelColor=1A1833" alt="4 modes"/>
  <img src="https://img.shields.io/badge/themes-8-FF7AD9?style=for-the-badge&labelColor=1A1833" alt="8 themes"/>
  <img src="https://img.shields.io/badge/dependencies-0-4FD1E8?style=for-the-badge&labelColor=1A1833" alt="Zero dependencies"/>
</p>
<p>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5"/>
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/Web_Audio-sound-6A4CFF?style=flat-square" alt="Web Audio"/>
  <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="MIT"/>
</p>

<img src="assets/demo.gif" alt="Typo Arcade demo: typing a 10 word test, then the results screen with a new personal best" width="85%"/>

<sub>A 10-word test: the ghost racer caret, live wpm, a fixed typo, then results with confetti and achievements.</sub>

</div>

---

## 🕹️ What is Typo Arcade?

A typing test that plays like an arcade game. Warm up with a classic speed test, then try **Word Rain**, take on the **Daily** challenge, or let **Weak Keys** drill the letters you keep missing. Every test earns XP, and new personal bests set off confetti.

## 🎮 Modes

<table>
<tr>
<td width="50%" valign="top">

### ⌨️ Classic
Time (**15 / 30 / 60 / 120 s**), word count (**10 / 25 / 50 / 100**), **quote**, **zen** or **your own text**. Turn punctuation and numbers on or off, and pick everyday English, tricky words or code.

</td>
<td width="50%" valign="top">

### 🌧️ Word Rain
Words fall from the sky. Type one and press space to blast it before it lands. Combos multiply your score, the rain speeds up every 8 words, and you have three lives.

</td>
</tr>
<tr>
<td valign="top">

### 📅 Daily
The same 30 words for everyone, every day. Come back tomorrow to keep your streak alive.

</td>
<td valign="top">

### 🎯 Weak Keys
Remembers which letters you miss and builds practice words from your weakest keys.

</td>
</tr>
</table>

## ✨ Features

| | |
| --- | --- |
| 👻 **Ghost racer** | A second caret runs at your personal best or a speed you choose. Try to stay ahead. |
| 🔥 **Combo flame** | Counts correct words in a row and lights up from 10. |
| 🏆 **XP, levels and 12 achievements** | Every test counts, and new bests set off confetti. |
| 📊 **Detailed results** | wpm, accuracy, raw speed, consistency, a speed chart with errors marked, and a heatmap of missed keys. |
| 🧠 **Practise your misses** | Turn the words you got wrong into a new test in one click. |
| 🥋 **Challenge settings** | Expert (a wrong word fails the run), master (a wrong key fails the run), stop on error, no backspace, blind mode. |
| 🎨 **Make it yours** | 8 themes, 6 fonts, text size, 4 caret styles, smooth caret, and focus mode that hides the menus while you type. |
| 🔊 **Sounds** | Click, pop, typewriter or **melody**, where every key plays a note. All synthesised, so there are no audio files. |
| 📱 **Works on phones** | Use your phone's own keyboard. |

## ⌨️ Shortcuts

| Key | Action |
| :---: | --- |
| <kbd>Tab</kbd> | Restart |
| <kbd>Esc</kbd> | Settings |
| <kbd>Ctrl</kbd> + <kbd>Backspace</kbd> | Delete the whole word |
| <kbd>Shift</kbd> + <kbd>Enter</kbd> | Finish a zen session |
| <kbd>Enter</kbd> | Next test (on the results screen) |

## 🚀 Run it

It's one HTML file: no install, no build, no dependencies.

```bash
git clone https://github.com/HemashreeVI/typo-arcade.git
cd typo-arcade
python -m http.server 8000   # open http://localhost:8000
```

You can also just double-click `index.html`.

<details>
<summary><b>🌐 Put it on GitHub Pages</b></summary>

<br>

**Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.**
A minute later it's live at `https://hemashreevi.github.io/typo-arcade/`.

</details>

<details>
<summary><b>🛠️ How it's built</b></summary>

<br>

```mermaid
flowchart LR
    K["⌨️ Keyboard<br/>(desktop or phone)"] --> I["Hidden input"]
    I --> E["Typing engine<br/>letters · caret · combos"]
    E --> R["Results<br/>chart · heatmap · XP"]
    E --> G["👻 Ghost racer"]
    I --> W["🌧️ Word Rain<br/>canvas game loop"]
    R --> S[("💾 Browser storage<br/>bests · history · achievements")]
```

- **Typing engine:** a hidden input catches every key, which is what makes phone keyboards work. Each letter is its own element, and the caret moves by measuring where the next letter sits.
- **Word Rain:** a canvas game loop with exploding-letter particles.
- **Sounds:** generated live with the Web Audio API.
- **Your progress:** stored in your own browser only. Nothing is sent anywhere.

</details>



<div align="center">

**Built by [Hemashree V I](https://hemashreevi.github.io)** ⌨️✨

<a href="https://hemashreevi.github.io"><img src="https://img.shields.io/badge/Portfolio-8B5CF6?style=flat-square&logo=googlechrome&logoColor=white" alt="Portfolio"/></a>
<a href="https://www.linkedin.com/in/hema-shree-373622289"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>

<sub>If you enjoyed it, a ⭐ helps others find it.</sub>

</div>
