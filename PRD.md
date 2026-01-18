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
Characters are animated using **Time-based Sine Waves**. This moves the tails and fins at a frequency relative to their swimming speed, removing the need for external sprite sheets.


---

## 📝 Detailed Release Notes (v1.0)

### 🚀 Gameplay & Mechanics
* **Difficulty Engine:** Implemented a base-speed multiplier for three distinct modes: Chill, Standard, and Extreme.
* **Extended Survival:** Increased total game time to 60 seconds with a tiered level-up system every 20 seconds.
* **Instant Death Hazards:** Re-tuned the Bomb Fish to trigger an immediate Game Over upon detonation contact, increasing late-game stakes.
* **Shield Warning System:** Added a 3-second "Countdown Beep" and visual flickering to the Golden Shield to prevent unexpected expiration deaths.
* **Dash Cooldown:** Introduced a 2-second recharge timer for the Dash ability, visualized by a stamina bar on the player.

### 📱 Mobile & Accessibility
* **Touch-Drag Engine:** Implemented native touch-event listeners for smooth vertical finger tracking.
* **Gesture Controls:** Added double-tap detection for mobile dashing.
* **Dual-Key Support:** Mapped controls to both Arrow Keys and Numeric keys (8/2) for flexible desktop play.
* **Responsive Canvas:** The game now auto-scales to fit 95% of the mobile viewport width.

### 🎨 Visuals & Sound
* **Sub-Surface Lighting:** Added a "God Ray" shimmer effect to the background using moving alpha-blended gradients.
* **Synthetic Soundscapes:** Switched from static assets to the Web Audio API to generate real-time 8-bit style sound effects.
* **Collision Feedback:** Added screen-shake and specific frequency shifts (Sawtooth waves) when taking damage.

---

## 🚀 Installation & Deployment
1.  **Local Play:** Open `index.html` in any modern web browser.
2.  **Hosting:** * **GitHub Pages:** Push to a repository and enable "Pages" in settings.
    * **Netlify:** Drag and drop the folder into Netlify Drop.
