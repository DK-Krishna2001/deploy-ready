<p align="center">
  <img src="https://img.shields.io/badge/DEPLOY-READY-00f3ff?style=for-the-badge&labelColor=0f172a&logo=terminal&logoColor=00f3ff" alt="DeployReady Badge"/>
  <img src="https://img.shields.io/badge/SDLC-Framework-00ff87?style=for-the-badge&labelColor=0f172a" alt="SDLC Framework"/>
  <img src="https://img.shields.io/badge/v2.4-Live-b026ff?style=for-the-badge&labelColor=0f172a" alt="Version 2.4"/>
</p>

<h1 align="center">
  ⚡ DeployReady
</h1>
<h3 align="center">The Customizable SDLC Countdown Framework</h3>

<p align="center">
  <em>A dark-mode, terminal-aesthetic SDLC pipeline countdown dashboard with dynamic timelines, interactive milestone gates, and a live 9:16 mobile lock screen preview — all in a single HTML file.</em>
</p>

---

## 🎯 What Is DeployReady?

**DeployReady** is a zero-dependency, single-file web application that transforms your software delivery lifecycle into a visual countdown experience. It gives engineering teams and solo developers a cinematic, terminal-inspired command center to track deployment milestones, set adaptive timelines, and monitor progress — complete with synthesized audio feedback and a live mobile lock screen mockup.

Whether you're shipping a weekend sprint or managing a year-long product roadmap, DeployReady dynamically recalculates every milestone to fit your chosen horizon.

---

## ✨ Core Features

### 🕒 Dynamic Timeline Engine
Switch seamlessly between three deployment horizons — each automatically redistributes all milestone target dates:

| Mode | Horizon | Use Case |
|------|---------|----------|
| **⚡ 1-Week Sprint** | 7 days | Hackathons, rapid prototyping, bug-fix sprints |
| **📅 1-Month Release** | 30 days | Feature releases, iteration cycles |
| **🚀 1-Year Roadmap** | 365 days | Product launches, enterprise delivery plans |

A custom **Deploy Deadline** date picker lets you anchor the countdown to any future date.

### 🔀 End-to-End SDLC Pipeline Gates
Five interactive, checkable milestones map the complete software delivery lifecycle:

| # | Phase | Milestone | Description |
|---|-------|-----------|-------------|
| 1 | **Discovery** | Requirements & Scope Lock | Define features, freeze scope |
| 2 | **Design** | Architecture & DB Schema | System design, data modeling |
| 3 | **Development** | Core Feature Implementation | Build the product |
| 4 | **QA & Audit** | Diagnostics & Integration Testing | Validate quality, run test suites |
| 5 | **Launch** | Production Release Deployment | Ship it 🚀 |

Click any row (or its checkbox) to toggle completion. The master progress bar, status badge, and lock screen all update in real time.

### 📱 9:16 Mobile Lock Screen Preview
A pixel-perfect phone frame mockup renders a **live lock screen widget** that mirrors your pipeline state:
- Real-time clock and date
- T-Minus days-to-launch badge with pulsing indicator
- Per-milestone completion status with T-offset labels
- Responsive — hidden on small screens; accessible via the **Lock Screen** button modal

### 🖥️ Dark-Mode Terminal Aesthetic
Every pixel is designed around a CRT-inspired hacker terminal theme:
- **CRT scanline overlay** for authentic retro texture
- **Neon glow effects** (cyan, green, amber, purple, red) with custom Tailwind tokens
- **JetBrains Mono** monospaced font + **Space Grotesk** for headings
- Dot-grid background, frosted glass headers, and custom neon scrollbars
- Fully dark — `bg-slate-950` base with luminous accent contrasts

### 🔊 Web Audio API Interactive Feedback
A built-in synthesizer provides tactile audio cues for every interaction:

| Action | Sound | Waveform |
|--------|-------|----------|
| ✅ Check milestone | Rising tone (D5→A5) | Sine |
| ⬜ Uncheck milestone | Falling tone (A4→A3) | Triangle |
| 🔀 Switch timeline mode | Quick chirp (E4→E5) | Square |
| 🔄 Reset all tasks | Descending sweep | Sawtooth |

Toggle audio on/off from the header. All sounds gracefully degrade if the browser blocks `AudioContext`.

### 📋 Real-Time Terminal Command Logs
A scrollable terminal log panel records every user action with timestamps:
```
[18:42:07] [EXEC OK] Task Completed: "Core Feature Implementation"
[18:42:09] [MODE SWITCH] Active horizon set to: 1M (1-Month Release)
[18:42:15] [DEADLINE UPDATE] Target set to Fri Dec 25 2026
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| **Markup** | Semantic HTML5 |
| **Styling** | [Tailwind CSS](https://tailwindcss.com/) (CDN) |
| **Icons** | [Font Awesome 6](https://fontawesome.com/) (CDN) |
| **Fonts** | [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) + [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (Google Fonts) |
| **Audio** | Web Audio API (oscillator synthesis) |
| **Logic** | Vanilla JavaScript (zero frameworks, zero build step) |

> **Zero dependencies. No `node_modules`. No build tools. Just one HTML file.**

---

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- That's it. Seriously.

### Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/DK-Krishna2001/deploy-ready.git
   cd deploy-ready
   ```

2. **Open the file**
   ```bash
   # macOS
   open index.html

   # Linux
   xdg-open index.html

   # Windows
   start index.html
   ```

   Or simply **drag `index.html` into your browser**.

3. **Optional: serve with a local server** (for a cleaner URL)
   ```bash
   # Python 3
   python3 -m http.server 8080

   # Then visit http://localhost:8080
   ```

### Quick Start
1. **Pick a timeline horizon** — click 1-Week, 1-Month, or 1-Year
2. **Set your deploy deadline** using the date picker
3. **Check off milestones** as you complete each SDLC phase
4. **Watch the lock screen** update in real time on the right panel
5. **Toggle audio** for satisfying synth feedback on every click

---

## 📂 Project Structure

```
deploy-ready/
├── index.html    # Complete application (markup + styles + logic)
└── README.md     # You are here
```

---

## 🎨 Customization

DeployReady is designed to be forked and modified:

- **Add milestones** — extend the `milestoneTemplates` array in the `<script>` block
- **Change colors** — modify the `neon` and `terminal` color tokens in `tailwind.config`
- **Adjust offsets** — tweak `offsetRatios` per milestone to control timeline distribution
- **Custom sounds** — modify `playSynthSound()` frequencies and waveforms

---

## 📸 Preview

| Desktop Dashboard | Mobile Lock Screen |
|---|---|
| Full SDLC pipeline with timeline controls, progress bar, and terminal logs | 9:16 phone mockup with live countdown widget and milestone status |

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙌 Acknowledgments

- [Tailwind CSS](https://tailwindcss.com/) for utility-first styling
- [Font Awesome](https://fontawesome.com/) for iconography
- [Google Fonts](https://fonts.google.com/) for JetBrains Mono & Space Grotesk
- Built with ❤️ as a Handshake Challenge Project Submission

---

<p align="center">
  <strong>Ship with confidence. Track every milestone. Deploy when ready.</strong>
</p>
<p align="center">
  <img src="https://img.shields.io/badge/Made_with-HTML%20%7C%20CSS%20%7C%20JS-00f3ff?style=flat-square&labelColor=0f172a" alt="Made with HTML CSS JS"/>
</p>
