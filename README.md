# 👋 Hi, I'm Gustav

**MSc student in Industrial Engineering & Management @ Linköping University** · Major in Computer Science, AI & Machine Learning
**Vice President @ LiU Formula Student** — leading 130+ members & building the software the team runs on

I build data-driven software around motorsport: race simulators, live prediction models, and the internal systems behind a Formula Student team.

[🔗 LinkedIn](https://www.linkedin.com/in/gustav-johansson-4318a31a2/) · [🏁 Play Undercut](https://undercut.gjohansson.dev/)

---

## ⭐ Featured projects

### [Undercut](https://github.com/GustavJ02/Undercut) — browser race strategy game · [▶ Play](https://undercut.gjohansson.dev/)
`TypeScript` `React` `Three.js` `Python` `FastAPI` `WebSockets` `Docker`

Run the pit wall in a live race: read timing, gaps and tyres, call the stops and team orders, and handle weather, safety cars and red flags. Play solo against AI teams or with friends who each run a team in the same race.

- **Deterministic simulation engine** in Python (0.5 s ticks, pre-drawn keyed randomness) — every race replays exactly from its event log
- **Data-grounded simulation:** tyre wear, stints, pit loss and safety-car rates started from values fitted on real race data, then rounded and adjusted for the public release
- **Skill vs. luck debrief:** each decision is replayed against 24 alternative futures and scored against what the AI would have done
- **Real-time multiplayer:** FastAPI server with one WebSocket per team and a visibility layer so clients never see hidden tyre or pace values
- 23 circuits, rule-based AI rivals, modding via content packs; ships as a multi-arch Docker image (x86-64 / ARM64) and an offline executable

### [F1-Predict](https://github.com/GustavJ02/F1-Predict) — live race prediction & strategy optimisation
`Python` `Monte Carlo` `Statistical modelling` `Backtesting` `Data pipelines`

Records F1 live timing during a session and turns it into live predictions: the qualifying cutoff and pole, upcoming battles, and the projected finish with win / podium / points probabilities.

- **End-to-end live pipeline:** recorder → parser → hot-reloading model runner → full-screen terminal dashboard, with continuous backup to a central data store
- **Monte Carlo race projection** with priors estimated from past races (tyre wear, stint lengths via Kaplan–Meier, circuit-specific passing); calibrated probabilities and lower rank error than the current-order baseline in leave-one-race-out backtests
- **Battle prediction:** 87% precision when predicting cars coming within 1 s in the next 8 laps (25 races)
- **Strategy optimiser** that finds the best tyre plan and pit windows per driver under each driver's remaining tyre allocation, plus a whole-field equilibrium mode
- Every feature is backtested — ideas that didn't improve held-out results (e.g. temperature effects, rain priors) were measured and left out

---

## 🏎️ LiU Formula Student

As VP responsible for Internal Systems I build and own the team's internal software:

- 🤖 **Apex** — RAG assistant over the team's Wiki.js knowledge base and the FS rulebook
- 📡 **Live telemetry** — streams CAN data from the ER27 car to a server, stored in TimescaleDB
- 👥 **Member Database** — member management with a recruitment pipeline integrated into [liuformulastudent.se](https://liuformulastudent.se/)
- 💸 **FS Finance System** — purchase requests, budgeting and expense reimbursement
- 🌊 [**LiUFS AeroCFD**](https://github.com/LiU-Formula-Student/LiUFS-AeroCFD) — CFD visualisation tool for the aero team

*Optimising what happens off the track to make the car faster on the track.*

---

## 🧪 Other projects

- [**Gusjo**](https://github.com/GustavJ02/Gusjo-Package) — neural network & linear algebra library built from scratch in Ada
- [**SimpleCarSim**](https://github.com/GustavJ02/SimpleCarSim) — minimal car simulator for reinforcement learning experiments

---

## 🧰 Tech stack

**Languages:** Python · TypeScript · JavaScript · SQL · Java · R · Ada · HTML/CSS · C/C++
**Web & backend:** Flask · SQLAlchemy · React · Next.js · Three.js · FastAPI · WebSockets
**Data & ML:** PyTorch · Pandas · Monte Carlo simulation · RAG · Superset
**Infra:** Docker · PostgreSQL · TimescaleDB · GitHub Actions · Apache

**Interests:** MLOps · Data pipelines · System design · Simulation · Motorsport analytics

---

> *Build it simple → make it solid → then make it fast.*
