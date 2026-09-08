---
title: Ebadi 2016 — Reciprocating transition (ICTAM)
type: source
threads:
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Ebadi, White, Pond & Dubief (2016) — Transition to turbulence in reciprocating channel flow

**Full citation.** A. Ebadi, C.M. White, I. Pond, Y. Dubief, "Transition to turbulence in reciprocating channel flow," XXIV ICTAM, 21–26 August 2016, Montreal, Canada. (Extended abstract, 2 pp. Reza = first author; White UNH, Pond & Dubief UVM.) **Precursor to** the fuller treatments in [[2017-pond-compfluids]] and the JFM papers [[2019-ebadi-jfm]], [[2020-ebadi-jfm]].

## One-paragraph summary

DNS study of **reciprocating (oscillatory, zero-mean) channel flow** aimed at understanding transition to turbulence in periodic flows. Using the **phase-averaged mean momentum balance**, the authors define the onset of turbulence as the phase at which the leading-term ordering matches the [[four-layer-structure|Wei et al. (2005) four-layer structure]] of canonical wall turbulence. Fully-developed turbulence first emerges in the **early decelerating phases** of the cycle, and the underlying mechanism is an **[[internal-shear-layer]]** that forms in the late accelerating phases and phase-leads the near-wall and core regions. Without this shear layer the flow stays transitional over the whole cycle. See [[stokes-reynolds-number]], [[turbulent-inertia]].

## System and governing balance

- Reciprocating channel flow oscillates at fixed angular frequency `ω` with cycle-averaged
  zero mean velocity: accelerate → decelerate → reverse, repeated.
- Similarity variable: [[stokes-reynolds-number|Stokes Reynolds number]] `Re_s = U_m l_s/ν`, with Stokes-layer thickness `l_s ≡ √(2ν/ω)` and `U_m` the amplitude of the cross-sectional average velocity.
- Phase-averaged momentum equation (Eq. 1):

$$
-\frac{\partial U}{\partial t} + \frac{1}{\rho}\cos(\omega t)
  + \nu\frac{\partial^2 U}{\partial y^2} + \frac{\partial(-\overline{u'v'})}{\partial y} = 0
$$

  terms (i) temporal acceleration, (ii) oscillatory pressure gradient, (iii) viscous, (iv) [[turbulent-inertia|turbulent inertia]] (Reynolds-stress gradient).

## Key results / numbers (cited to this paper)

- Two DNS cases: **Re_s = 648 (type III, self-sustaining transition)** and **Re_s = 1019 (type IV, intermittently turbulent)**. [source]
- For **Re_s = 1019**, a four-layer structure like Wei et al. emerges over `9π/16 ≤ φ ≤ 11π/16` (early deceleration); velocity and temperature profiles agree reasonably with canonical wall turbulence there. For **Re_s = 648** no such behavior at any phase. [source]
- **Mechanism:** near `φ = π/2` (accel→decel), an internal shear layer emerges that **decelerates at a phase-lead** relative to near-wall and core, coincident with a strong **sink-like behavior of the turbulent inertia**; it likely rolls up, triggering transition to a fully-developed turbulent channel. Subsequent acceleration suppresses turbulence → back to transitional. [source]
- **Threshold: Re_s > 750** for the internal shear layer (hence type III→IV  transition) to occur. [source]

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| `Re_s` | Stokes Reynolds number, `U_m l_s/ν` | `Re_s` |
| `l_s` | Stokes-layer thickness, `√(2ν/ω)` | `l_s` |
| `U_m` | amplitude of cross-sectional mean velocity | `U_m` |
| `φ` | phase angle within the cycle | `φ` (phase) — distinct from `φ'` temperature |
| `−u'v'` | Reynolds shear stress; its `y`-gradient = turbulent inertia | `−u'v'` |

⚠️ Symbol clash to watch: this thread uses `φ` for **phase angle**; the heat-transfer thread uses `φ'` for **fluctuating temperature**. Kept distinct in [[notation]].

## Connections

- Thread: [[non-equilibrium-pulsatile-flow]] (Reza's contribution).
- Concepts: [[stokes-reynolds-number]], [[four-layer-structure]], [[internal-shear-layer]],  [[turbulent-inertia]].
- Method: [[dns]].
- References: Wei et al. (2005) four-layer MMB; Akhavan et al. (1991); Ozdemir et al. (2014).
