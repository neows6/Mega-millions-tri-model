# Mega Millions Tri-Model Prediction System

Three independent prediction models applied to the full 30-year history of Mega Millions draws — side-by-side comparison with consensus analysis.

## Data
- **Source:** LottoAmerica.com (verified)
- **Coverage:** 3,019 draws · Sep 6, 1996 → Apr 24, 2026
- **Pool:** 1–70 main balls · Mega Ball 1–24 (v7 current matrix)

---

## Model 1 — ⚗ Navier-Stokes Fluid Dynamics
Treats each ball's draw history as a fluid flow field.

| Formula | Equation | Purpose |
|---------|----------|---------|
| Pressure | P = fᵢ / f̄ | Normalized frequency weight |
| Velocity | v = (L/b) / (Δt+1) | Recency — cycling rate |
| Reynolds Number | Re = ρvL/μ | Turbulence indicator |
| Bernoulli Energy | B = P + ½ρv² | Total mechanical energy |
| Vorticity | ω = \|P − 1\| | Deviation from equilibrium |
| NS-Forecast | F = 0.38v + 0.30P + 0.18/ω + 0.09f̂ + Δoverdue | Ensemble score |

---

## Model 2 — 🎯 Smart Play
Designed around improving real-world expected payout, not just frequency.

| Component | Logic |
|-----------|-------|
| Gap-Spring Energy | E = ½k(ago − T)² — compressed spring = overdue = energy stored |
| Split Avoidance | Penalizes birthday numbers (1–31), round numbers, "lucky" numbers |
| Balance Filter | Enforces sum 100–175, 2–3 odd/even, 2–3 low/high (≤35) |
| Frequency Deficit | Rewards balls below their expected historical draw rate |
| EV Signal | Flags jackpots above/below ~$700M break-even threshold |

---

## Model 3 — ⚛ Quantum Entanglement (for fun)
Applies quantum mechanics theory to lottery number phase space.

| Concept | Formula | Description |
|---------|---------|-------------|
| Wave function | ψ(n) = √(f/N) · e^(iθ) | Amplitude and phase for each number |
| Phase angle | θ = 2π · ago / T | Position in quantum return cycle |
| Probability | P(n) = \|ψ\|² · interference | Probability density after interference |
| Tunneling | P_t = e^(−κ·barrier) | Cold numbers can tunnel through barrier |
| Decoherence | D = e^(−λ·recency) | Recently drawn = collapsed state |
| Entanglement | +0.08 boost per correlated pair | All-time common pairs share quantum correlation |

**Quantum States:**
- `RESONANT` — in phase with natural return cycle (constructive interference)
- `COLLAPSED` — just drawn, wave function has collapsed
- `DESTRUCTIVE` — out of phase (destructive interference)
- `SUPERPOSED` — neutral quantum state

---

## Predictions (verified output)
```
Model 1 (NS Fluid):  1 · 7 · 36 · 43 · 49  + MB 8
Model 2 (Smart Play): 14 · 23 · 29 · 46 · 61  + MB 20   [sum=173 ✓ balance ✓]
Model 3 (Quantum):   6 · 10 · 18 · 31 · 46  + MB 10

Consensus: Ball 46 appears in 2 of 3 models
EV at $163M jackpot: -$1.80 per ticket (break-even ~$700M)
```

---

## Usage
```jsx
import TriModelPredictor from './mega-millions-tri-model'
// Drop into any React app — no props required
```

## ⚠️ Disclaimer
For entertainment only. Each lottery draw is a statistically independent random event.
No mathematical model can predict a certified RNG. Jackpot odds: 1 in 302,575,350.

## Files
| File | Description |
|------|-------------|
| `mega-millions-tri-model.jsx` | Main React component — all 3 models |
| `README.md` | This file |
