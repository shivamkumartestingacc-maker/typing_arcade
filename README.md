# Typing Arcade

An isometric typing defense drawn with the **hairline** kernel
([lucasmarkes/hairline](https://github.com/lucasmarkes/hairline), MIT).
Walkers march down three lanes toward your keep, each carrying a word.
Type the word to fire; spend the ink you earn on turrets.

## How it plays

- **Type to fire.** The target is the walker drawn in the bright line, with a
  dashed ring at its feet. Each correct letter is a bolt from the keep; finish
  the word and the walker breaks apart. At the start of a word, typing another
  walker's first letter switches to it (no two walkers on the field share a
  first letter).
- **Typos fire back.** A wrong letter is marked, the cursor moves on, and that
  walker fires at the keep (−3). No backspace.
- **The line.** A walker that reaches the dashed line stops and batters the
  keep (runner 3, walker/herald 5, brute 9).
- **Ink & turrets.** +1 ink per correct letter, +3 per clean word, a bounty
  per kill, a bonus per wave. Press `1` `2` `3` (or tap the buttons) to build or
  upgrade that lane's turret (25 / 45 / 70 ink). Turrets bite the **last
  letter** off the nearest word in their lane; higher levels fire faster and
  reach further.
- **Clean words.** No-typo words heal +2. Two in a row raise a shield that
  soaks three hits; the first typo drops it. Combo ×1–×5 on letter streaks.
- **Waves.** Short build phase between waves. Brutes from wave 2, heralds
  (signs carrying whole lines — spaces count) from wave 3.
- The keep's ten windows are its health; they go dark as it takes damage.

`Esc` pause · `Enter` start/restart · `⌨ TYPE` opens the touch keyboard ·
theme and sound toggles are remembered.

## Files

| file | what |
|---|---|
| `index.html` | the whole game in one file: page, styles, the hairline kernel (MIT, © Lucas Marques, unchanged), the game, and the menu figure made with the `hairline-create` skill |
| `LICENSE-hairline.txt` | the hairline kernel's MIT licence |

No build step and no other files. Double-click `index.html` to play offline,
or push it to GitHub / Vercel / GitHub Pages as it is.

## Drawing rules kept

Rounded solids only (silhouette + one crease), painted back to front, no
fills or colours of their own, one bright stroke as the only highlight (the
current target, or the keep's pennant at rest), and no words inside the
drawing: every word lives in an HTML bubble laid over it. All motion runs in
the kernel's single frame loop (`HL.register`), springs for aim, tweens for
choices.
