# ⚔️ SKETCH WARS: Hand-Pose Drawing Battle

A high-octane, competitive split-screen drawing game powered by **MediaPipe Hand Landmarker** and computer vision. Players battle head-to-head directly in their browsers using hand gestures—pinching to draw in real time, matching target shapes, collecting power-ups, and racing against the clock.

The application is styled with the **Vibrant Palette** theme, featuring glassmorphic overlays, vibrant neon player identifiers, high-contrast visual states, and glowing hand cursor elements.

---

## 🎮 How to Play

### 1. Position Yourself in Front of the Camera
Ensure you are in a well-lit environment and your camera is active. The application will mirror your image so left/right moves naturally. 

### 2. Identify Player Lanes
- **Player 1 (Left Side - Blue Accent)**
- **Player 2 (Right Side - Red Accent)**

### 3. Track Your Fingers
Two floating helper dots will be projected over your fingers to confirm detection:
- **`T` (Yellow/Blue/Red)**: Placed on your **Thumb** tip.
- **`I` (Yellow/Blue/Red)**: Placed on your **Index Finger** tip.

These dots serve as visual confirmation of precise hand tracking.

### 4. Pinch to Draw
- To start drawing on your corresponding canvas, **pinch your thumb and index finger close together** (press `T` and `I` together).
- The pointer cursor will glow and expand to indicate active drawing.
- **Separate your thumb and index finger** to lift your brush and stop drawing.

### 5. Follow the Target Shape
A random hollow shape (e.g., triangle, diamond, circle, sword) will be shown in the center container.
- Attempt to trace this shape inside your player canvas as accurately as possible.
- The game will compute your **live path accuracy percentage** in real-time.

### 6. Score & Game Over Actions
At the conclusion of the game, a high-octane podium screen presents the winner with full statistical feedback.
- Click **PLAY AGAIN** to start a new round immediately.
- Click **HOME** to return to the principal start menu.

---

## 🛠️ Key Technical Features

- **MediaPipe Hand Landmark Tracking**: Utilizes state-of-the-art Web-assembly accelerated AI models to detect up to 21 dynamic landmarks per hand.
- **Isotropic Pinch Math**: Custom robust ratio calculations mapped to standard 640x480 pixels to keep pinch activation responsive regardless of modern screen aspect ratio stretches.
- **Dual Live Drawing Canvases**: Independent layered rendering contexts that handle brush widths, high-performance path optimization, and interactive glowing shadows.
- **Responsive Dynamic UI**: Implemented on top of Tailwind CSS for smooth flex/grid layouts and animated transitions between rounds.

---

## 🚀 Development Quick Start

The applet compiles using a fast Node-based development server utilizing Vite.

### Clean Project Compilation
```bash
# Verify type safety and code correctness
npm run lint

# Build production compiled static bundles inside dist/
npm run build
```
