---
title: RANS turbulence models (k-ε, v²-f)
type: method
threads:
  - cfd-validation-method
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# RANS turbulence models

**What it is.** Reynolds-averaged Navier–Stokes (RANS) modeling solves the phase- or time-averaged equations, with the resulting turbulent (Reynolds) stress `−ρu'ᵢu'ⱼ` and turbulent
heat flux `−u'ᵢθ'` supplied by a **closure model**. Cheap and widely used, but the common
**linear eddy-viscosity models (EVM)** struggle with complex/non-equilibrium flows.

## Eddy-viscosity closure

`−u'ᵢu'ⱼ` modeled via a turbulent viscosity `ν_T` and the mean strain rate; heat flux via eddy diffusivity + [[reynolds-analogy|turbulent Prandtl number]]. Base EVM: `k-ε`, `k-ω`.

## Low-Reynolds-number models used in Reza's work

"Low-Re" here means **no wall functions** — the near-wall region is resolved directly (first grid point at `z⁺≤1`). In [[2017-pond-compfluids]]:

- **Launder–Sharma (LS) k-ε** — transports `k` and `ε`; requires near-wall **damping  functions** (`f_μ`, `f₂`) to avoid unrealistic near-wall values. Constants: `σ_k=1, σ_ε=1.3, C_ε1=1.44, C_ε2=1.92, C_μ=0.09`. [source]
- **v²-f (Durbin)** — adds transport of the wall-normal velocity variance (`v²`/`w²` in the
  paper's coordinates) and an elliptic-relaxation function `f`; the wall-normal variance
  provides correct near-wall damping, so **no damping functions are needed**. [source]

Both were **deliberately chosen as imperfect** for reciprocating flow, to showcase what the
[[cfd-validation-method|integral validation technique]] reveals that the standard technique misses.

## Known difficulties for non-equilibrium flow

- EVMs assume **stress and strain in phase**, but for [[womersley-number|`Wo`≳0.1]] there is a stress–strain phase difference. [source]
- Transition / intermittency is not reliably captured by conventional RANS. [source]

## Where it appears in Reza's threads

- [[cfd-validation-method]] (the models under test), [[non-equilibrium-pulsatile-flow]].
- Solver in [[2017-pond-compfluids]]: OpenFOAM 2.3.0 (PISO), compared against [[dns]].
