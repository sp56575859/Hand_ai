# 🖐️ Handy AI | Gesture Intelligence Platform

**Handy AI** is a high-performance, browser-based spatial computing interface. It leverages computer vision via **MediaPipe Hands** to transform the human hand into a precise input device. With a dark-synth aesthetic and real-time physics, it explores the intersection of human gesture and generative art.

---

## 🚀 Quick Start
1.  **Open** the `index.html` file in a modern browser (Chrome or Edge recommended).
2.  **Grant** webcam permissions when prompted.
3.  **Click** "Enter Experience" to initialize the neural networks.
4.  **Position** your hands roughly 2–4 feet from the camera for optimal tracking.

---

## 🎮 Interaction Modes

### ▶ Play Mode (Green Accent)
*Focus: Physics and Particle Interaction*
* **Pinch (Thumb + Index):** Spawns a ripple ring and particle burst. Triggers a high-frequency sawtooth zap.
* **Two-Hand Tether:** Connecting matching fingertips between hands creates a gradient bridge.
* **Lightning Bolt:** When matching fingertips get close, the bridge transforms into a jagged lightning arc.
* **Spatial Hum:** A binaural sine wave scales its pitch and volume based on the distance between your palms.

### ♥ Shapes Mode (Pink Accent)
*Focus: Symbol Recognition*
* **Peace (✌):** Hold up index and middle fingers. Displays a glowing peace sign.
* **Heart (♥):** Bring both palms close together with fingers spread. Renders a pulsing parametric heart.
* **Star Burst (💥):** Clench both hands into fists. Triggers a rotating 8-point golden star and heavy particle emission.

### ✏ Write Mode (Blue Accent)
*Focus: Air Drawing & Persistent Canvas*
* **Pen Down:** Extend index finger while keeping the thumb away.
* **Pen Up:** Pinch thumb and index together to stop drawing.
* **Shake to Clear:** Open your palm and shake it rapidly side-to-side. The **Shake Progress Ring** in the corner will fill; once full, the canvas clears with a "pop" sound.

---

## 🛠 Technical Architecture

### **The Stack**
* **Vision Engine:** MediaPipe Hands (via CDN).
* **Rendering:** Quad-layered HTML5 Canvas (Background, FX, persistent Drawing, and UI).
* **Audio:** Web Audio API (real-time oscillators for haptic-like feedback).
* **Styling:** CSS Glassmorphism & SVG Fractal Noise (for the film grain effect).

### **Canvas Layering (Z-Index)**
1.  **Video:** Mirrored and dimmed to serve as a subtle reference.
2.  **bgCanvas:** The "Matrix Rain" layer, which speeds up based on your hand's movement velocity.
3.  **fxCanvas:** Real-time feedback, skeleton tracking, and temporary particles.
4.  **drawCanvas:** A persistent layer that stores your "Air Drawings" in `Write` mode.

---

## ⌨ Controls & Shortcuts
| Action | Gesture |
| :--- | :--- |
| **Change Mode** | Click the Mode Pill in the Top Bar |
| **Pinch** | Thumb & Index tips < 0.055 normalized distance |
| **Reset Drawing** | Shake open palm or click "Clear Canvas" |
| **Optimal Distance** | 0.5m to 1.5m from camera |

---

## ⚠️ Requirements & Troubleshooting
* **Browser:** Chromium-based browsers (Chrome/Edge) are required for stable MediaPipe performance.
* **Lighting:** Front-facing light is preferred. Avoid heavy backlighting (windows), which silhouettes the hand.
* **Performance:** If the FPS drops below 20, close other browser tabs or lower your system's resolution.
