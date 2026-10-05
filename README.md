# Meditation Timer 🧘‍♂️

![Version](https://img.shields.io/badge/version-1.1-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Active-brightgreen.svg)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-orange.svg)

An essential, smooth, and responsive web application designed to guide meditation sessions using real-time synthesized singing bowls.

Available as a **Progressive Web App (PWA)**, installable on Android, iOS, and Desktop devices for uninterrupted offline use.

📍 **Live Demo:** [https://tagtthespellcaster.github.io/Meditation-Timer/](https://tagtthespellcaster.github.io/Meditation-Timer/)

---

## 📋 Features (v1.1)

- **Real-Time Audio Synthesis:** Singing bowl sounds generated via the Web Audio API (no external audio files or loading delays).
- **Tone Selection:** 6 distinct audio profiles (ranging from deep low gongs to high-resonance bell chimes).
- **Preparation Phase:** Configurable initial warm-up period (adjustable in 10-second increments, capped at a maximum of 20% of total time).
- **Interval Splitting:** Divide session duration into equal periods separated by a half-volume (50%) chime.
- **Settings Persistence:** Automatic saving and loading of current preferences via `localStorage`.
- **Statistics Tracking:** Monitor total accumulated meditation time over time.
- **Offline PWA Support:** Installable directly onto your smartphone or computer home screen via Service Worker.
- **Zen Interface:** High-contrast dark theme featuring a smooth circular progress ring and fluid animations.

---

## 🛠️ Interval Logic Model

The preparation time is **included** within the selected total meditation time.

*Example:*
- **Total Time:** 10 minutes
- **Preparation:** 1 minute
- **Intervals:** 2 periods

**Timeline:**
1. **00:00** — Initial chime (preparation starts)
2. **01:00** — Full-volume chime (preparation ends / main meditation session begins)
3. **05:30** — Midpoint half-volume chime (50%)
4. **10:00** — Final full-volume chime (session completion)

---

## 📦 Project Structure

```text
├── index.html       # Main application file (HTML5, CSS3, JS ES6)
├── manifest.json    # Progressive Web App configuration
├── sw.js            # Service Worker for offline caching
├── icon-192.png     # Application icon (192x192)
├── icon-512.png     # Application icon (512x512)
└── LICENSE          # MIT License
