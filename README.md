# ⌨️ Typing Arcade

A fast, addictive **typing game** that runs in the browser. Words come at you, the clock keeps ticking, and every keystroke counts. Race against the timer, chain combos, and see how high you can push your WPM before the arcade beats you.

> **Status:** early setup — the project skeleton and this README are in place. Game source is being added next.

---

## Table of Contents

- [Why Typing Arcade](#why-typing-arcade)
- [Features](#features)
- [How to Play](#how-to-play)
- [Scoring](#scoring)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

---

## Why Typing Arcade

Most typing tests are boring walls of text. Typing Arcade turns practice into play — arcade-style rounds, instant feedback, and a score that rewards both **speed** and **accuracy**. You get better at typing because you actually want one more round.

## Features

| Feature | Description |
| --- | --- |
| ⏱️ **Timed rounds** | Type as many words as you can before the timer runs out. |
| 🎯 **Live accuracy** | Every correct and incorrect keystroke is tracked in real time. |
| 🔥 **Combo multiplier** | Consecutive clean words build a streak and multiply your score. |
| 📊 **WPM & accuracy stats** | End-of-round summary with words per minute and accuracy percentage. |
| 🧠 **Progressive difficulty** | Word length and speed ramp up as the round goes on. |
| 🎨 **Arcade visuals** | High-contrast, retro-inspired UI built for focus and speed. |
| 📱 **Responsive** | Playable on desktop and mobile keyboards. |

## How to Play

1. Open the game in your browser.
2. Hit **Start** to begin a round.
3. Type the highlighted word and press **Space** to submit it.
4. Keep going until the timer hits zero.
5. Review your WPM, accuracy, and final score — then beat it.

**Controls**

| Key | Action |
| --- | --- |
| `A`–`Z` | Type the current word |
| `Space` | Submit the word / skip |
| `Backspace` | Fix a typo before submitting |
| `Enter` | Start or restart a round |
| `Esc` | Pause |

## Scoring

```
score += word_length × combo_multiplier
```

- A **correct** word adds points and increases your combo.
- A **mistake** resets the combo multiplier back to 1×.
- **Accuracy** = correct keystrokes ÷ total keystrokes.
- **WPM** = (correct characters ÷ 5) ÷ minutes elapsed.

## Tech Stack

Deliberately lightweight — no build step required to play:

- **HTML5** — markup and layout
- **CSS3** — arcade styling, animations, responsive layout
- **Vanilla JavaScript (ES6+)** — game loop, input handling, scoring, state
- **localStorage** — persists your personal best score

## Project Structure

Target layout as the game is built out:

```
typing_arcade/
├── index.html          # Game shell and layout
├── css/
│   └── style.css       # Arcade theme, animations, responsive rules
├── js/
│   ├── main.js         # Entry point, game loop, state machine
│   ├── words.js        # Word lists by difficulty
│   ├── input.js        # Keystroke handling and validation
│   ├── score.js        # WPM, accuracy, combo and score logic
│   └── storage.js      # High-score persistence
├── assets/
│   └── ...             # Fonts, sounds, icons
└── README.md
```

## Getting Started

No dependencies, no install. Clone and open:

```bash
git clone https://github.com/shivamkumartestingacc-maker/typing_arcade.git
cd typing_arcade
```

Then either:

- **Open directly:** double-click `index.html`, or
- **Serve locally** (recommended, so `localStorage` and assets behave normally):

```bash
# Python 3
python3 -m http.server 8000
# → http://localhost:8000
```

```bash
# or Node
npx serve .
```

## Roadmap

- [x] Repository setup and project documentation
- [ ] Core game loop: timed rounds, word queue, input validation
- [ ] Scoring engine: WPM, accuracy, combo multiplier
- [ ] Game UI: arcade theme, animations, end-of-round summary
- [ ] Difficulty scaling and multiple game modes
- [ ] High-score table persisted in `localStorage`
- [ ] Sound effects and keyboard feedback
- [ ] Mobile keyboard support

## Contributing

Ideas, bug reports, and pull requests are welcome:

1. Fork the repo and create a branch: `git checkout -b feature/my-feature`
2. Commit your changes: `git commit -m "Add my feature"`
3. Push and open a pull request.

Please keep the game dependency-free and playable straight from the browser.

## License

No license has been chosen yet. Until one is added, all rights are reserved by the repository owner.
