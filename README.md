# 🔮 AI Hand-Gesture Particle System

> A real-time, interactive 3D particle simulation controlled by computer vision.

![Banner](asset/demo.gif)

## 📖 Overview

This project combines **Three.js** (WebGL) with **Google MediaPipe** (Computer Vision) to create an immersive 3D experience. It generates a system of 16,000+ particles that form mathematical shapes and react dynamically to your hand gestures via the webcam.

It features advanced post-processing effects like **Light Trails (Afterimage)** and **Neon Glow (Unreal Bloom)** to create a cyberpunk/ethereal aesthetic.

## ✨ Features

* **🖐 AI Hand Tracking**: Detects pinch and spread gestures in real-time using MediaPipe Hands.
* **💠 Mathematical Morphology**: Particles transition smoothly between procedurally generated shapes:
    * Heart
    * Saturn (with rings)
    * Flower (Harmonic Rose)
    * Buddha (Abstract Math Construction)
    * Fireworks (Random Explosion)
* **🎨 Post-Processing VFX**:
    * **Trails**: Smooth motion blur for a fluid look.
    * **Bloom**: High-end neon glow effect.
* **🎛 Real-time UI**: Built-in control panel to adjust physics, colors, and visual effects on the fly.
* **⚡ High Performance**: Uses `BufferGeometry` to render thousands of particles efficiently.

## 🚀 How to Run

Because this project uses the Camera API and ES Modules, **you cannot simply double-click the HTML file**. It must be served via a local web server (HTTPS or Localhost).

### Method 1: VS Code (Recommended)
1.  Open the project folder in **Visual Studio Code**.
2.  Install the **Live Server** extension.
3.  Right-click `index.html` and select **"Open with Live Server"**.

### Method 2: Python
If you have Python installed, open your terminal in the project folder and run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## 🎮 Controls

### Gestures
* **Idle / Relaxed Hand**: Particles drift gently in the selected shape.
* **Pinch (Thumb & Index)**: Particles contract and implode toward the center.
* **Wide Open Hand**: Particles explode and scatter outward with chaotic energy.

### UI Panel
* **Shape Model**: Switch between the 5 mathematical forms.
* **Color**: Change the particle base color.
* **Morph Speed**: Adjust how fast particles fly to their target.
* **Trail Length**: Controls the length of the light trails.
* **Glow Strength**: Adjust the intensity of the neon bloom.

## 🛠️ Tech Stack

* **Three.js**: 3D Rendering Engine.
* **MediaPipe Hands**: Machine Learning Hand Tracking.
* **Lil-gui**: Floating UI controller.
* **EffectComposer**: Post-processing pipeline (Bloom/Afterimage).

## ⚠️ Troubleshooting

**"Camera Access Denied"**
* Ensure you are running on `localhost` or `https`. Browsers block camera access on `file://` paths.
* Check your browser permissions to allow the camera.

**"Black Screen"**
* Open the browser console (F12) to check for errors.
* Ensure your GPU drivers are up to date (WebGL requirement).

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
