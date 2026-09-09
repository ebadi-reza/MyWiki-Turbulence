---
title: Pulsatile boundary layer flow
type: concept
threads:
  - non-equilibrium-pulsatile-flow
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Pulsatile boundary layer flow

**What it is.** A wall-bounded flow whose flow rate **oscillates about a non-zero mean** — in contrast to **oscillatory / reciprocating** flow, whose cycle-averaged flow rate is **zero** (see [[non-equilibrium-pulsatile-flow]]). Reza's experimental pulsatile-boundary-layer (PBL) work is **unpublished** — it lives in Chapter 7 of the [[2016-ebadi-thesis|2016 PhD thesis]].

## Decomposition

Triple (Hussain–Reynolds) decomposition of any quantity `A`:

$$
A(y,t) = \overline{A}(y) + \tilde{A}(y,t) + A'(y,t)
$$

with `⟨A⟩ = Ā + Ã` the phase (ensemble) average, `Ā` the time/cycle average, `Ã` the
**perturbation** (oscillatory / coherent) component, and `A'` the turbulent fluctuation. The time-averaged mean flow is (mostly) independent of forcing frequency, so `Ã` is the flow's **response to the imposed periodic forcing**. [source: [[2016-ebadi-thesis]]]

## Frequency regimes (`ω⁺`)

The pulsation frequency is inner-normalized as `ω⁺ = ω/(u_τ²/ν) = Str²/2`, where
`Str = ω/(u_τ/l_s)` is a Strouhal number and `l_s = √(2ν/ω)` the [[stokes-reynolds-number|Stokes layer thickness]]. Four regimes (Ramaprian & Tu; Brereton & Mankbadi 1995) ([[2016-ebadi-thesis|source]]):

| Regime | `ω⁺` range | Perturbation field |
|---|---|---|
| Quasi-steady | `< 0.003` | negligible; flow = steady at instantaneous Re |
| Low frequency | `0.003–0.006` | non-negligible, **in equilibrium**, ~no stress–strain phase lag |
| Intermediate | `0.006–0.02/0.04` | **non-equilibrium**; stress–strain phase diff 0–50° |
| High frequency | `> 0.02/0.04` | asymptotes to Stokes flow (45° phase lead); viscous-governed |

## Reza's experiments (thesis Ch. 7)

PIV in the [[neat-wind-tunnel|NEAT tunnel]] at three **intermediate-regime** frequencies; `u_τ` via the Mehdi–White integral method ([[wall-skin-friction]]); 60 cycles, 18 phase bins. Rotor-stator blockage caps speed (~3.25 m/s) and modulation amplitude (5–11%). ([[2016-ebadi-thesis|source]])

| `f` (Hz) | `ω⁺` | `l_s⁺` | `Re` | `Re_s` | `W` | `u_osc/U∞` |
|---|---|---|---|---|---|---|
| 1.60 | 0.007 | 17 | 7306 | 336 | 30.7 | 11% |
| 3.25 | 0.014 | 12 | 6543 | 228 | 40.6 | 8% |
| 4.95 | 0.020 | 10 | 6805 | 185 | 52.0 | 6% |

### Key findings

- **Perturbation wall shear stress is the equilibrium indicator.** The two lower frequencies (`ω⁺=0.007, 0.014`) are **in equilibrium** — perturbation `τ̃_w` is **in phase** with the freestream (±10°) and its amplitude matches the Stokes solution `|τ_w,s|=√2 μ|Ũ∞,s|/l_s`. The highest frequency (`ω⁺=0.020`) is **non-equilibrium** — `τ̃_w` **leads** the freestream by **40±10°** (≈Stokes 45°) with amplitude slightly above Stokes → it sits at the **onset of the high-frequency regime**, a different regime from the two lower cases. ([[2016-ebadi-thesis|source]])
- A statistically significant **"bump" in `τ̃_w` at φ≈110°** (early deceleration) for the two lower frequencies, absent at the highest. ([[2016-ebadi-thesis|source]])
- Freestream velocity modulation amplitude is **inversely proportional to frequency**; freestream turbulence intensity for the two low frequencies is **180° out of phase** with the highest. ([[2016-ebadi-thesis|source]])
- **Time-averaged** profiles differ only slightly from ZPGBL; a log region at `40≲y⁺≲70` gives`κ = 0.45, 0.42, 0.47` (ω⁺=0.007, 0.014, 0.020) vs ZPGBL `κ≈0.41` (slightly higher). Streamwise turbulence intensity is elevated in the outer layer, **inversely ∝ frequency**. ([[2016-ebadi-thesis|source]])
- **EVMs fail** for the non-equilibrium (highest-frequency) case: the eddy-viscosity closure`r̃ = −C ν_T ∂ũ/∂y` wrongly assumes perturbation stress and strain are in phase. ([[2016-ebadi-thesis|source]])
- **Conjecture:** a critical `ω⁺` exists — below it, periodic forcing modifies the time-averaged flow; above it, the perturbation field departs equilibrium and (at high enough `ω⁺`) asymptotes to the Stokes solution. `0.007, 0.014` below; `0.020` above. [UNVERIFIED — Reza's conjecture,  "more work required"] ([[2016-ebadi-thesis|source]])

## Reciprocating vs pulsatile (thesis §7.3)

- **Reciprocating** (zero mean): phase-averaged fields depend **strongly** on frequency — lower frequency (larger period) transitions to turbulence for part of the cycle, higher frequency stays transitional. Cycle-averaged quantities are zero.
- **Pulsatile** (non-zero mean): cycle-averaged fields are finite and **insensitive** to amplitude and frequency; phase-averaged fields depend **weakly** on frequency, fluctuating about the mean. The most nonlinear behavior (highest frequency) is **confined to the near-wall Stokes layer** and couples weakly to the mean/turbulent fields.
- Transition in both is governed by `Re_s ∝ Re/W`, i.e. `Re_c = f(W)` **Reciprocating: linear, `Re_c = 700 W` (`Re_s ≃ 500`).** Pulsatile: complicated — transition advanced or delayed by `W`. ([[2016-ebadi-thesis|source]])

## Connections

- Thread: [[non-equilibrium-pulsatile-flow]] (the experimental face; DNS face = oscillatory OCF).
- Apparatus/method: [[neat-wind-tunnel]] (rotor-stator), [[piv]], [[wall-skin-friction]] (MW-MIM).
- Concepts: [[stokes-reynolds-number]], [[womersley-number]], [[log-law]], [[reynolds-analogy]].
- Related result: [[wall-flux-modulation-frequency]] (τ_w at ω, q″_w at 2ω).

See [[notation]].
