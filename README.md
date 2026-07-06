# TripMeter 🚗⛽

**Know the cost before you turn the key.**

TripMeter is a car mileage and trip-fuel-cost calculator built as a dashboard-styled web app. It helps drivers calculate their real fuel average, estimate trip costs, compare cars side-by-side, and get maintenance tips tuned to their exact car and fuel type — all running client-side, with no backend required.

This is the web companion to a C++ desktop version currently in development.

---

## 🔗 Live Demo

---<img width="959" height="481" alt="image" src="https://github.com/user-attachments/assets/352934ca-6e7d-40e6-8be8-1012eaaff66a" />


## ✨ Features

- **🚙 Garage (Car Profiles)** — Save cars with name, type (hatchback / sedan / SUV / bike), engine cc, and fuel type (petrol / diesel / CNG).
- **📊 Average Calculator** — Enter odometer start/end + fuel filled to get your real km/l, visualized on an animated speedometer-style gauge with red/amber/green efficiency zones.
- **💰 Trip Cost Calculator** — Enter distance + fuel price (or select a saved car) to instantly get fuel needed and total trip cost in PKR.
- **⚖️ Comparison Mode** — Compare 2–3 saved cars for the same trip distance and fuel price to see which one actually costs less, with a visual cost breakdown.
- **💡 Tips Engine** — Contextual, tier-based tips (Excellent / Good / Below Average / Needs Attention) generated from how your average compares to the expected baseline for your car type and fuel — plus a general reference library (tire pressure, driving style, idling, load, servicing, fuel quality).
- **📁 Trip History Log** — Every logged trip is saved locally in the browser and can be exported as `.csv` or `.txt`.
- **📱 Fully Responsive** — Works on desktop, tablet, and mobile.

---

## 🖥️ Tech Stack

- **HTML5** — semantic structure
- **CSS3** — custom design system (CSS variables, no framework), dashboard/gauge-inspired visual identity
- **Vanilla JavaScript** — no dependencies, no build step
- **SVG** — hand-built animated gauge (drawn dynamically, not an image)
- **localStorage** — client-side persistence for car profiles and trip history

No frameworks, no npm install, no build tools — just open `index.html`.

---

## 📂 Project Structure

```
tripmeter/
├── index.html          # Main structure & sections
├── css/
│   └── style.css       # Design tokens, layout, components
├── js/
│   └── script.js        # Calculators, gauge renderer, tips engine, storage
└── README.md
```

*(A single-file version, `tripmeter.html`, is also available with CSS/JS inlined — useful for quick sharing or testing without folder structure.)*

---

## 🚀 Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/ahmadraza2730/tripmeter.git
   ```
2. Open `index.html` in any browser — that's it. No installation, no server required.

To deploy: upload the folder (or the single-file `tripmeter.html`) to any static host — GitHub Pages, Netlify, Vercel, or your own hosting.

---

## 🧠 How the Tips Engine Works

Each car type + fuel combination has an expected baseline average (e.g. a petrol hatchback ≈ 14 km/l). When a user calculates their average, TripMeter compares it against that baseline:

| Ratio to Baseline | Tier | Meaning |
|---|---|---|
| ≥ 110% | Excellent | Beating expectations |
| 90–110% | Good | As expected |
| 75–90% | Below Average | Actionable fixes needed |
| < 75% | Needs Attention | Likely a mechanical issue |

Tips are then matched to both the tier **and** the fuel type, since petrol, diesel, and CNG vehicles have different common failure points.

---

## 🗺️ Roadmap

- [ ] C++ desktop version (Qt GUI) with the same calculation logic
- [ ] Optional AI-powered personalized tips via LLM API (with secure backend proxy)
- [ ] Editable default fuel price setting
- [ ] SQLite-backed history for the desktop version
- [ ] Car-specific baseline overrides (per exact model, not just type)

---

## 👤 Author

**Muhammad Ahmad**
Second-year CS student, freelance C++ developer, and ML enthusiast.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Muhammad%20Ahmad-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/muhammad-ahmad2730/)

---

## 📄 License

This project is open for learning and personal use. Feel free to fork it, but please credit the original author if you reuse significant portions.
