# ⚓ Kitty the Pirate

> A steampunk pirate cat platformer — playable in any browser, desktop or mobile.

![HTML5](https://img.shields.io/badge/HTML5-Canvas-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=black)
![No dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)
![Mobile ready](https://img.shields.io/badge/mobile-touch%20controls-blue)

---

## 🎮 Play it

Open `index.html` in any modern browser.  
The launcher **auto-detects your device** and redirects to the right version:

| File | For |
|------|-----|
| `index.html` | Entry point — auto-redirects |
| `game_v4.html` | Desktop (keyboard + mouse) |
| `game_mobile.html` | Mobile (virtual joystick + touch buttons) |

> **GitHub Pages:** enable Pages on the `main` branch and the game will be live at  
> `https://mauriziocoro.github.io/kitty-the-pirate/`

---

## 🐱 Story

**Kitty** is an anthropomorphic steampunk pirate cat sailing the high seas.  
Her ship is under attack — pirate skeletons are boarding in waves!  
Collect all the gold doubloons before the last skeleton reaches you.

```
  /\_____/\
 ( o   o  )   "Arrr, no bones about it!"
 (  =^=   )
 (         )  ⚓ Kitty the Pirate ⚓
 (  )   (  )
```

---

## ⚔️ Gameplay

### Objective
Collect all the doubloons on the ship's platforms.  
The fewer doubloons remain, the faster and more numerous the skeletons become.

### Controls

**Desktop**

| Key | Action |
|-----|--------|
| `A` / `D` or `←` `→` | Move |
| `W` / `↑` | Jump (press twice for double jump) |
| `Space` | Fire blunderbuss (3-pellet spread) |
| `Esc` | Pause / Skin customisation |

**Mobile**

| Control | Action |
|---------|--------|
| Left joystick | Move |
| `SALTA` button | Jump / double jump |
| `🔫` button | Fire blunderbuss |
| `☰` button | Pause |

---

## ✨ Features

### Core mechanics
- **Platformer physics** — one-way platforms (jump through from below)
- **Double jump** — second jump available in mid-air
- **Blunderbuss** — 3-pellet spread shot, fires in the direction Kitty faces

### Enemies
- **Skeleton pirates** — chase Kitty across platforms, can jump to reach higher levels
- **Musketeer skeletons** — every 5th spawn; keep their distance and shoot aimed bullets
- Frozen by the ❄ ice bonus for 3 seconds

### Power-ups (each appears once per game)
| Bonus | Effect |
|-------|--------|
| ⚡ Invincibility | Every 10 doubloons collected → 3 s of immunity |
| ❤ Extra life | +1 life (max 6) |
| ❄ Freeze | All skeletons frozen for 3 s |

### Progression
- **Win streak** — each consecutive victory adds more doubloons to the next game
- Formula: `baseCoins + winsStreak × coinStep`
- Losing resets the streak

### Difficulty presets

| Preset | Base doubloons | +per win | Skeleton HP | Skeleton speed |
|--------|---------------|----------|-------------|----------------|
| Facile | 20 | +3 | ×0.75 | ×0.70 |
| Normale | 30 | +5 | ×1.00 | ×1.00 |
| Difficile | 40 | +8 | ×1.30 | ×1.35 |

---

## 🎨 Customisation (Pause menu — `Esc`)

Available from the pause screen, the start screen, and the game-over screen.

- **Skin colour** — 6 fur tones
- **Clothes colour** — 6 coat colours
- **Accessories**
  - Pirate hat (remove to show full cat ears)
  - Steampunk monocle
  - Eye patch (disables monocle)
  - Parrot on shoulder
- **Day / Night** — toggle the background sky
- **Flag** — 6 designs for the ship's mast flag

| Flag | Description |
|------|-------------|
| Jolly Roger | Classic skull & crossbones |
| Rosa dei Venti | Golden compass rose |
| Serpente | Green snake |
| Tricolore | Italian flag |
| Fiamma | Fire gradient |
| Kraken | Tentacled sea monster |

---

## 📊 Match History

The game stores the last 25 sessions in `localStorage`:

- Date & time
- Win / Loss
- Difficulty
- Doubloons collected
- Skeletons defeated
- Lives remaining
- Invincibility bonuses used
- Play time

---

## 🗂 File structure

```
kitty-the-pirate/
├── index.html          # Device detector & launcher (4 KB)
├── game_v4.html        # Desktop version (55 KB)
├── game_mobile.html    # Mobile version  (58 KB)
└── README.md
```

No build step, no dependencies, no server required.  
Everything runs from a single HTML file per version.

---

## 🛠 Technical notes

- Rendered entirely on an **HTML5 Canvas** (800 × 480 internal resolution)
- All graphics drawn procedurally — **no external assets**
- Mobile version scales via CSS (`width: 100%`) and maps touch coordinates to the internal resolution
- Touch input: virtual joystick (left zone) + action buttons (right zone)
- Persistent history via `localStorage` (key: `ktp_v1`)
- Compatible with Chrome, Firefox, Safari, Edge — desktop and mobile

---

## 📜 License

MIT — do whatever you want with it.

---

*Made with ⚓ and a lot of ☠*
