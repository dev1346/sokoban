# Sokoban
version 1.0.0

A classic Sokoban puzzle game with 152 levels of increasing difficulty.

## How to Play

Open `sokoban.html` in any web browser. No installation or server required!

**Goal:** Push all boxes (🟫) onto target squares (). When a box is on a target, it turns green (🟢).

## Controls

### Movement
- **Arrow keys** or **WASD** — Move player
- **Z** — Undo last move
- **R** — Restart current level
- **N** — Next level
- **P** — Previous level
- **Enter** — Advance to next level (when puzzle is solved)

### Go To Level
Use the "Go to:" input field in the controls bar to jump directly to any level (1-152). Type the level number and press Enter or click "Go".

## Level Progression

The game features 152 hand-crafted levels organized by difficulty:

- **Levels 1-22**: Tutorial levels (1-2 boxes) — Learn the basics
- **Levels 23-72**: Easy to medium (2-3 boxes) — Build your skills
- **Levels 73-112**: Medium difficulty (2-4 boxes) — More complex puzzles
- **Levels 113-152**: Hard to very hard (2-12 boxes) — Expert challenges

## Features

- **152 unique levels** — From simple tutorials to brain-bending puzzles
- **Undo system** — Made a mistake? Press Z to undo
- **Move counter** — Track your efficiency with move and push counts
- **Progressive difficulty** — Levels gradually increase in complexity
- **Mobile support** — Touch controls for mobile devices
- **Fully offline** — No internet connection required
- **No dependencies** — Single HTML file, runs anywhere

## Credits

### Game Engine
Custom-built Sokoban engine with canvas rendering and BFS solver verification.

### Level Design
- **Levels 1-22**: Original custom-designed levels
- **Levels 23-152**: Based on David W. Skinner's famous Microban collections
  - Microban I, II, III, and IV
  - Original source: http://www.sneezingtiger.com/sokoban/levels.html
  - Used with permission (freely distributable with attribution)

### Artwork
- Worker icon: Custom top-down view design
- Euro pallet boxes: Realistic warehouse-style crates

## Tips

1. **Plan ahead** — Think before you push. Boxes can only be pushed, not pulled!
2. **Avoid corners** — Don't push boxes into corners unless that's the target
3. **Use undo** — Press Z freely to experiment with different approaches
4. **Count pushes** — Try to solve levels with the minimum number of pushes
5. **Take breaks** — Some levels are genuinely challenging. Come back fresh!

## File Structure

```
sokoban/
├── sokoban.html          ← The game (open this file)
├── worker.png            ← Worker icon source
└── levels/               ← Level data (for modders)
    ├── index.json
    ├── level_01.json
    ├── ...
    ── level_152.json
```

## Modding

Want to create your own levels? Each level is stored as a JSON file in the `levels/` directory:

```json
{
  "id": 1,
  "name": "First Push",
  "difficulty": 1,
  "boxes": 1,
  "optimalMoves": 1,
  "optimalPushes": 1,
  "grid": [
    "#####",
    "#   #",
    "# @ #",
    "# $ #",
    "# . #",
    "#####"
  ]
}
```

**Legend:**
- `#` — Wall
- `@` — Player
- `$` — Box
- `.` — Target
- `*` — Box on target
- `+` — Player on target
- ` ` (space) — Floor

After editing, update `levels/index.json` and the `LEVELS` array in `sokoban.html`.

## License

This game is freely distributable. The Microban level collections by David W. Skinner are included with proper attribution.

---

**Enjoy the puzzle!** 🎮
