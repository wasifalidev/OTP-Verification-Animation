<div align="center">

![Header](https://capsule-render.vercel.app/api?type=waving&color=0:00ADB5,100:00D4FF&height=220&section=header&text=OTP%20Verification%20Animation&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=35&desc=A%20stunning%20open-source%20OTP%20UI%20component%20with%20fluid%20animations&descAlignY=55&descSize=16)

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=20&pause=1000&color=00ADB5&center=true&vCenter=true&width=700&lines=OTP+Verification+UI+%F0%9F%94%90;Fluid+Animations+%26+Smooth+Transitions;Web+Audio+API+%E2%80%94+No+External+Files;Pure+HTML+%2B+CSS+%2B+JavaScript;Open+Source+%E2%80%94+Free+to+Use!" alt="Typing SVG" />

<br/>

[![Live Demo](https://img.shields.io/badge/Live%20Demo-View%20Now-00ADB5?style=for-the-badge&logo=vercel&logoColor=white)](https://wasifalidev.github.io/OTP-Verification-Animation/)
[![GitHub Stars](https://img.shields.io/github/stars/wasifalidev/OTP-Verification-Animation?style=for-the-badge&color=00ADB5&logo=github)](https://github.com/wasifalidev/OTP-Verification-Animation/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/wasifalidev/OTP-Verification-Animation?style=for-the-badge&color=00D4FF&logo=github)](https://github.com/wasifalidev/OTP-Verification-Animation/network)
[![License](https://img.shields.io/badge/License-MIT-00ADB5?style=for-the-badge)](LICENSE)

<br/>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Web Audio API](https://img.shields.io/badge/Web%20Audio%20API-00ADB5?style=for-the-badge&logo=audiomack&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-00ADB5?style=for-the-badge)

</div>

---

## ✨ What Is This?

A **beautiful, open-source OTP (One-Time Password) verification UI component** built with pure HTML, CSS, and JavaScript — no frameworks, no dependencies. It features an immersive, multi-phase animation sequence, synthesized audio effects, a particle celebration system, and a polished dark-mode glassmorphism design.

**Free to use, fork, and embed in your own projects.** ⚡

---

## 🎬 Animation Phases

The verification experience unfolds across **4 cinematic phases**:

| Phase | Name | Description |
|:---:|---|---|
| **1** | 🔢 Input Grid | A sleek horizontal 4-digit input with an animated conic-gradient focus ring |
| **2** | 🌀 Orbital Transition | Digits break free and spiral into an orbital formation |
| **3** | 🔗 Convergence | Orbital elements collapse into a central merge point |
| **4** | 🎉 Celebration | Particle burst, ripple rings, halo effects & a melodic success fanfare |

---

## 🚀 Features

### 🎨 Visual Design
- **Dark glassmorphism** theme with teal/cyan gradient accents
- **Spring-easing CSS animations** for a natural, physical feel
- **Animated conic-gradient focus ring** that spins as you type
- **Canvas particle system** for the success celebration burst
- **Fully responsive** — works on desktop, tablet, and mobile

### 🎵 Synthesized Audio (No External Files)
> All sounds are generated procedurally via the **Web Audio API** — zero file downloads.

- 🖊️ **Digit ticks** — satisfying click per keypress
- 🎶 **Harmonic cascade** — ascending chord on auto-fill
- 💨 **Whoosh transition** — cinematic phase-change sweep
- 💥 **Boom + success melody** — celebratory fanfare on verify
- ❌ **Error tones** — distinct shake + sound for wrong codes
- 🔇 **Mute toggle** — one-click audio on/off button

### ⌨️ Interactivity & Accessibility
- Full **keyboard navigation** (arrows, backspace, tab)
- **Auto-fill demo button** to showcase the full animation flow
- **Countdown timer** for OTP resend logic
- **ARIA labels** on all interactive elements
- `prefers-reduced-motion` support for accessibility compliance
- **Hidden native input** for mobile autofill & OTP suggestions

---

## 🛠️ Tech Stack

```
├── index.html   →  Semantic structure with ARIA support
├── style.css    →  CSS custom properties, keyframes, spring animations
└── script.js    →  SoundEngine class, state machine, particle system
```

**Zero dependencies. Zero build step. Just open and go.**

---

## ⚙️ Getting Started

### Clone & Open
```bash
git clone https://github.com/wasifalidev/OTP-Verification-Animation.git
cd OTP-Verification-Animation
# Open index.html in your browser — done!
```

### Local Dev Server (Recommended for full audio)
```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server

# PHP
php -S localhost:8000
```
Then visit `http://localhost:8000`.

> **Tip:** Modern browsers require a user interaction before playing audio. Click anywhere on the page first if you don't hear sounds.

---

## 🔧 Customization

### Change the OTP Code
```javascript
// script.js
const CORRECT_CODE = '2365'; // ← change to your code
```

### Customize Colors
```css
/* style.css */
:root {
    --bg-color: #07090e;          /* Background */
    --success-color: #2ee6a6;     /* Success / teal accent */
    --error-color: #f87171;       /* Error / red accent */
    --transition-spring: cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
```

### Customize Audio Frequencies
```javascript
// script.js — SoundEngine class
const DIGIT_FREQS = [523.25, 587.33, 659.25, 783.99]; // C5, D5, E5, G5
```

### Add Custom Sounds
```javascript
// Extend SoundEngine with your own sounds
playCustomSound(freq, duration) {
    // Your implementation here
}
```

---

## 🧱 Architecture

### State Machine

```
idle → typing → orbit → verifying → success
                                  ↘ error → idle
```

| State | Trigger |
|---|---|
| `idle` | Initial load / replay |
| `typing` | User begins entering digits |
| `orbit` | All 4 digits filled |
| `verifying` | Orbital convergence complete |
| `success` | Correct OTP submitted |
| `error` | Wrong OTP — shake animation plays |

### Key Components
| File | Feature | Purpose |
|---|---|---|
| `script.js` | `SoundEngine` | Web Audio API procedural sound wrapper |
| `script.js` | `ParticleSystem` | Canvas-based celebration burst |
| `script.js` | State Machine | Controls all animation phase transitions |
| `style.css` | CSS Keyframes | Spring, orbit, and ripple animations |
| `style.css` | CSS Custom Props | Easy theming and color customization |

---

## 🐛 Troubleshooting

| Issue | Solution |
|---|---|
| No audio plays | Click anywhere first — browsers require user interaction for audio |
| Animations seem slow | Check if `prefers-reduced-motion` is enabled in system settings |
| Looks wrong on mobile | Ensure `<meta name="viewport">` tag is present in HTML |
| Audio API not supported | Use a modern browser: Chrome, Firefox, Safari, or Edge |

---

## 🤝 Contributing

Contributions, improvements, and forks are very welcome! This is an **open-source** project — feel free to use this animation in your own apps.

```bash
# 1. Fork the repo on GitHub
# 2. Create your feature branch
git checkout -b feature/your-feature-name

# 3. Commit your changes
git commit -m "feat: add your feature"

# 4. Push to your fork
git push origin feature/your-feature-name

# 5. Open a Pull Request 🚀
```

**Ideas for contributions:**
- 🌈 New color themes
- 📱 Enhanced mobile gestures
- 🔢 6-digit OTP variant
- 🌍 i18n / localization support
- ♿ Additional accessibility improvements

---

## 📄 License

This project is open-source and available under the **MIT License** — use it freely in personal and commercial projects.

---

## 👨‍💻 About the Author

<div align="center">

**Wasif Ali** — Web & App Developer | Founder of Developers Tech

*"Turning Ideas into Real Applications"*

[![Portfolio](https://img.shields.io/badge/Portfolio-00ADB5?style=for-the-badge&logo=vercel&logoColor=white)](https://wasifalidev.netlify.app)
[![Developers Tech](https://img.shields.io/badge/Developers%20Tech-000000?style=for-the-badge&logo=googlechrome&logoColor=00ADB5)](https://developerstech.netlify.app)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mianwasifdev@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/wasifalidev)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/wasifali.dev)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/wasifalidev)

</div>

---

<div align="center">

![Footer](https://capsule-render.vercel.app/api?type=waving&color=0:00ADB5,100:00D4FF&height=120&section=footer)

⭐ **If this helped you, please give it a star — it means the world!** ⭐

*Made with ❤️ by [Wasif Ali](https://github.com/wasifalidev) — Pakistan 🇵🇰*

</div>
