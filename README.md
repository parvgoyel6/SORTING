<div align="center">

# 🕷️ Spider-Sort 3D: Merge Sort Visualizer

### *“With great algorithms comes great time complexity.”*

An interactive, superhero-themed 3D sorting algorithm visualizer built with **Three.js**, **Tailwind CSS**, and procedural **Web Audio API**. Watch Spider-Man organize chaotic arrays using dynamic web lines, physics arcs, and real-time step-by-step code execution.

---

[![Complexity](https://img.shields.io/badge/Time%20Complexity-O(N%20log%20N)-red?style=for-the-badge&logo=codeforces&logoColor=white)](#-algorithm-breakdown)
[![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=for-the-badge&logo=three.js&logoColor=white)](https://threejs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](#)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero%20Install-emerald?style=for-the-badge)](#-getting-started)

</div>

---

## ⚡ What is Spider-Sort?

Instead of boring 2D bar charts, **Spider-Sort** turns learning Divide-and-Conquer into a cinematic superhero experience:

- 🕸️ **Real Web Mechanics**: Spider-Man physically aims his web-shooters, anchoring 3D Catmull-Rom spline webs to holographic energy pillars.
- 🚀 **Parabolic Web-Pulling**: Whenever elements need to shift during in-place merges, Spider-Man lifts them into the air on dual web lines and snaps them down with landing shockwaves.
- 🔊 **100% Synthesized Audio**: Built-in sound effects (web `thwip`, frequency-pitched comparison pings, web tension pulls, and victory fanfare) created purely in real-time via the browser's Web Audio API—zero audio files needed.
- 🎛️ **Full Telemetry & Inspection**: Step-by-step execution, dynamic code tracer, custom array modal, and live "Spidey Sense" HUD comments.

---

## 🎮 Live Interface & Controls

```
+--------------------------------------------------------------------------+
| [🕷️ Spider-Sort]  Comparisons: 14  •  Swaps: 8     [Suit] [Custom] [Audio]|
+--------------------------------------------------------------------------+
|                                                                          |
|                           [ Spider-Man Perch ]                           |
|                                     │                                    |
|                                🕸️  │  🕸️         [ Code Tracer ]        |
|                              ┌──────┴──────┐      ├── mergeSort(...)     |
|                             [42]          [18]    └── thwipSwapAndSlide  |
|                                                                          |
+--------------------------------------------------------------------------+
| Spidey Sense: "THWIP! Target value 18 pulled in-line to index 0!"         |
| [ ▶ SORT ]  [ ⏸ Pause ]  [ ⏭ Step ]  [ 🔀 Shuffle ]  Size: 10  Speed: 2x |
+--------------------------------------------------------------------------+
```

### Control Deck
| Control | Shortcut / Action | Description |
| :--- | :--- | :--- |
| **Sort / Pause** | Primary Action | Starts continuous sorting loop or freezes mid-step |
| **Step** | Micro-debugger | Executes one exact algorithmic sub-operation at a time |
| **Shuffle / Reset** | Array Gen | Shuffles via Fisher-Yates or restores initial state |
| **Custom Array** | Modal (`#btn-custom-array`) | Input your own numbers ($4 \le N \le 20$) or choose presets |
| **Suit Selector** | Customization | Switch between **Nano-Armor**, **Classic Red/Blue**, or **Miles Morales** |
| **Camera Orbit** | Left Click + Drag | Freely rotate camera angle around the rooftop arena |

---

## 🧠 Algorithm Breakdown

Spider-Sort demonstrates **In-Place Merge Sort**:

$$\text{Time Complexity: } \mathcal{O}(N \log N) \quad|\quad \text{Space: In-place pointer shift}$$

```
                [ 42 | 18 | 85 | 29 ]
                        │  (Divide)
           ┌────────────┴────────────┐
       [ 42 | 18 ]               [ 85 | 29 ]
           │                         │
     ┌─────┴─────┐             ┌─────┴─────┐
   [ 42 ]      [ 18 ]        [ 85 ]      [ 29 ]
     └─────┬─────┘             └─────┬─────┘
       [ 18 | 42 ]               [ 29 | 85 ]
           └────────────┬────────────┘
                (Web-Shoot Merge)
                [ 18 | 29 | 42 | 85 ]
```

### Visual State Colors
- 🟡 **Amber Glow**: Elements actively being compared by Spidey's dual web-lines.
- 🟣 **Purple Arc**: Element captured and swinging mid-air to its target slot.
- 🟢 **Emerald Flash**: Subarray partition successfully merged and ordered.
- 🔷 **Cyan Base**: Idle array standing by on the rooftop pad.

---

## 🛠️ Tech Stack & Architecture

- **Rendering Engine**: [Three.js (r128)](https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js) with custom lighting, shadows, and depth fog.
- **Styling**: [Tailwind CSS CDN](https://cdn.tailwindcss.com) + Cyberpunk glassmorphism design tokens.
- **Audio Synthesis**: Native HTML5 `AudioContext` (white-noise bandpass filters for web releases, sine wave frequency modulation for comparisons).
- **Icons**: [FontAwesome 6](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css).
- **Fonts**: Google Fonts (`Outfit` and `JetBrains Mono`).

---

## 🚀 Getting Started

No build tools, bundlers, or `npm install` required!

1. Clone or download this repository:
   ```bash
   git clone https://github.com/your-username/spider-sort-3d.git
   cd spider-sort-3d
   ```
2. Open `sorting.html` in any modern web browser:
   ```bash
   # On macOS
   open sorting.html

   # On Windows
   start sorting.html

   # On Linux
   xdg-open sorting.html
   ```
3. Hit **SORT** and enjoy the web-slinging show! 🕷️✨

---

<div align="center">

Made with ❤️ and webs. Feel free to star ⭐ the repo if this helped you visualize Merge Sort!

</div>