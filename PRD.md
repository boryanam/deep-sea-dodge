# 🌊 Deep Sea Dodge: Deluxe Mobile

**Deep Sea Dodge** is a fast-paced, 2D side-scrolling survival game built in a single HTML5 file. Players must navigate a high-intensity underwater environment, dodging hazardous fish and explosive threats to survive for a full 60 seconds.

---

## 🎮 Game Overview

* **Platform:** Web (Desktop & Mobile Responsive)
* **Genre:** Arcade / Survival
* **Core Objective:** Avoid collisions with enemy entities and survive until the 60-second timer reaches zero.
* **Difficulty Tiers:** Chill (0.7x), Standard (1.0x), Extreme (1.6x).

---

## 🛠️ Key Features

### 1. Dynamic Entities
| Entity | Type | Behavior | Effect |
| :--- | :--- | :--- | :--- |
| **Normal Fish** | Obstacle | Moves R → L at varying speeds. | -1 Life |
| **Golden Fish** | Power-up | Rare spawn, moves slowly. | 8s Invincibility Shield |
| **Bomb Fish** | Hazard | Pulses red for 3s while moving, then detonates. | **Instant KO** (0 Lives) |

### 2. Progression System
The game features a 60-second survival window divided into three intensity levels:
* **Level 1 (0–20s):** Low density, base fish speeds.
* **Level 2 (20–40s):** Increased spawn frequency and speed boost.
* **Level 3 (40–60s):** "Frenzy Mode" – Maximum hazard density.

### 3. Audio-Visual Warning System
* **Shield Warning:** 3 seconds before the Golden Shield expires, the player fish flickers and the system emits three sequential warning beeps.
* **Bomb Primer:** The Bomb Fish pulses bright red and triggers a high-frequency "heartbeat" sound before detonation.
* **Pre-game Countdown:** A 3-second visual and auditory countdown to ensure player readiness.

---

## 🕹️ Controls

| Action | Desktop Keys | Mobile Gesture |
| :--- | :--- | :--- |
| **Swim Up** | `8` or `Up Arrow` | Slide Finger Up |
| **Swim Down** | `2` or `Down Arrow` | Slide Finger Down |
| **Dash** | `Spacebar` | Double-Tap Screen |

*Note: Dashing provides a 3x speed boost for 15 frames and has a 2-second recharge cooldown.*

---

## 📐 Technical Architecture

### Collision Logic
The game utilizes **Circle-to-Circle Collision Detection**. By treating the player and fish as circular bounds rather than squares, the gameplay feels more forgiving and realistic.



### Procedural Animation
Characters are animated using **Time-based Sine Waves**. This moves the tails and fins at a frequency relative to their swimming speed, removing the need for external sprite sheets or GIF files.



### Audio Engine
Built entirely on the **Web Audio API**. All sound effects (Crashes, Fanfares, Beeps, and Explosions) are generated mathematically as oscillators (Sine, Square, and Sawtooth waves) at runtime.

---

## 🚀 Installation & Deployment

Since the game is contained in a single file, it requires no installation:

1.  **Local Play:** Open `index.html` in any modern web browser.
2.  **Hosting:** * **GitHub Pages:** Push to a repository and enable "Pages" in settings.
    * **Netlify:** Drag and drop the folder into Netlify Drop.
    * **Firebase:** Use `firebase deploy` for Google-backed hosting.

---

## 📝 Release Notes (v1.0)
* Initial release with 60s survival logic.
* Added mobile touch-drag support and double-tap dash.
* Implemented "Instant KO" mechanics for Bomb Fish.
* Added synthesized sound warning system for power-up expiration.
* Integrated difficulty selector menu.
