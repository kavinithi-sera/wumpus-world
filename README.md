# The Wumpus World

A feature-complete, interactive browser implementation of the classic Artificial Intelligence benchmark **Wumpus World**. Built using pure HTML5, CSS3, and vanilla JavaScript with zero external dependencies, this project brings the grid-world environment to life with an atmospheric UI, Web Audio API sound synthesis, and a real-time propositional logic inference overlay.

Live Demo:  https://kavinithi-sera.github.io/wumpus-world/

---

## 🎮 Key Features

* **Dynamic Cave Generation**: 4x4 grid dynamically generated per session with randomized hazard distributions (~18% pit density) and guaranteed safe starting tile at `(1,1)`.
* **Real-time Percept Tracking**: Live sensory feedback rendering **Breeze** (adjacent pit), **Stench** (adjacent live Wumpus), and **Glitter** (gold present on current tile).
* **Arsenal & Web Audio**: Single-shot arrow mechanic traveling in straight cardinal trajectories with Web Audio API sound synthesis for Wumpus defeat events.
* **Propositional Logic Overlay**: Integrated inference visualization to track deductive reasoning over explored state space:
  * 🟩 **Provably Safe**: Highlights unvisited tiles proven safe based on existing non-breeze/non-stench percepts.
  * 🟥 **Forced Hazard**: Automatically infers and flags single unvisited neighbors responsible for sensed breeze or stench signals.
* **Keyboard Shortcuts**: Native support for directional arrow keys and single-key interaction (`G` for grab).

---

## 🚀 Quick Start

Since the app is contained within a single HTML file, setup requires no package managers or build processes:

1. Clone the repository:
   ```bash
   git clone https://github.com/kavinithi-sera/wumpus-world.git
   ```
2. Navigate into the folder:
   ```bash
   cd wumpus-world
   ```
3. Open `index.html` directly in any modern web browser.

---

## 📖 Rules & Controls

### Objective
Navigate through the cave system, locate the gold, grab it, and safely navigate back to the cave entrance at `(1,1)`.

### Controls
| Input | Action |
| :--- | :--- |
| `↑` `↓` `←` `→` / Buttons | Move agent to adjacent cell |
| `G` / `GRAB` Button | Grab gold when glitter percept is active |
| `🏹 Aim Arrow` + Direction | Shoot your single arrow along a row or column |
| `Reveal Overlay` | Toggle the logic solver visualization |

### Hazards & Mechanics
* **Pits**: Stepping into a pit results in an immediate game over.
* **Wumpus**: Stepping into a live Wumpus tile results in an immediate game over. Firing an arrow along its row or column kills it, clearing all stench percepts.
* **Breeze**: Sensed on tiles adjacent (north, south, east, west) to one or more pits.
* **Stench**: Sensed on tiles adjacent to a live Wumpus.

---

## 🛠️ Project Structure

```
wumpus-world/
├── index.html      # Complete game logic, styles, audio synthesizer, and UI layout
└── README.md       # Project documentation
```

---

## 📜 License

Distributed under the MIT License. 
