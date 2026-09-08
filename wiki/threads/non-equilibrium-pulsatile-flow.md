---
title: Thread — Non-equilibrium & pulsatile turbulent flow
type: thread
threads:
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Thread 3 — Non-equilibrium & pulsatile turbulent flow

Experimental and analytical work on **non-equilibrium** wall turbulence — time-varying flows where the classical equilibrium picture (thread 2) no longer holds. The reciprocating / pulsatile channel-flow line is the core. **This thread has the most references and the
deepest concept coverage.**

## Terminology: oscillatory vs pulsatile

- **Oscillatory / reciprocating (OCF):** cycle-averaged **zero** mean flow rate.
- **Pulsatile:** flow rate oscillates about a **non-zero** mean.
Both are governed by [[stokes-reynolds-number|`Re_s`]] and [[womersley-number|`Wo`]].

## Reza's contribution

- **Transition mechanism in oscillatory channel flow** — seeded in  [[2016-ebadi-ictam|Ebadi et al. (2016, ICTAM)]] and matured in [[2019-ebadi-jfm|Ebadi et al. (2019, JFM)]]. DNS across the III→IV boundary
  (Re_s=648 type III; 801, 1009 type IV). **Central result:** transition occurs when the
  **nonlinear development stage (near-wall streak breakdown) begins during the
  *accelerating* portion** of the cycle (needs Re_s>750). Mechanism, phase by phase:
  1. Early acceleration → near-wall **streaks** form; turbulence approaches one-component
     ([[anisotropy-invariant-map]]).
  2. **Streak breakdown** → explosive growth of near-wall Reynolds stress & its gradient
     ([[turbulent-inertia]]).
  3. **Centreline momentum source** fades; a locally accelerating/decelerating **[[internal-shear-layer|internal layer]]** emerges at `y/l_s≈1`.
  4. Wall-normal **rearrangement of mean forces → [[four-layer-structure]]** appears (steady-turbulence signature); a transient **[[log-law|log region]]** emerges (κ≈0.4, B<5.2).
  5. Deceleration cuts strain rate/TKE production → **reverse transition** to weakly transitional. Repeat. At Re_s=648 streak breakdown comes too late (deceleration) → no four-layer structure, stays weakly transitional. Proposes the four-layer structure as an **excellent metric for transition to turbulence**.

- **CFD/RANS implications** — the same reciprocating flow is the test case for the
  [[cfd-validation-method|integral validation technique]] ([[2017-pond-compfluids]]), a challenging non-equilibrium benchmark that breaks standard validation and  [[reynolds-analogy|Reynolds analogy]].

- **Experimental pulsatile boundary layer (PBL)** — [[2016-ebadi-thesis|thesis Ch. 7]] (**unpublished**). PIV in the [[neat-wind-tunnel|NEAT tunnel]] at three intermediate-regime frequencies (`ω⁺=0.007, 0.014, 0.020`). The highest frequency is **non-equilibrium** (perturbation  wall shear stress leads the freestream ~40°, ≈Stokes), the two lower are in **equilibrium**;  time-averaged flow ≈ ZPGBL (weak mean–oscillatory coupling). Full treatment: [[pulsatile-flow]]. The rotor-stator apparatus is from [[2019-biles-jfe]].
- **Reciprocating vs pulsatile synthesis** — [[2016-ebadi-thesis|thesis §7.3]]: reciprocating phase-fields depend strongly on frequency (transition), pulsatile weakly; `Re_c=f(W)`, reciprocating linear `Re_c=700 W`. See [[pulsatile-flow]], [[stokes-reynolds-number]].
- **Lit review & framework** — [[2016-ebadi-thesis|thesis Ch. 5]] adds the theoretical transition-mechanism context (quasi-steady vs Floquet), the [[log-law|unsteady length scale]]  log-law scenarios, and the [[turbulent-inertia|quadrant-analysis]] redistribution mechanism.

## Background & references

- **Wei, Fife, Klewicki & McMurtry (2005)** — [[four-layer-structure]] of the mean momentum balance; the analytical framework borrowed as the turbulence-onset criterion.
- **Akhavan, Kamm & Shapiro (1991)** — transition in bounded oscillatory Stokes flow (expt).
- **Ozdemir, Hsu & Balachandar (2014)** — DNS of transition in smooth-walled Stokes BL.

## Connections to other threads

- [[high-Re-analytical-modeling]] — supplies the equilibrium MMB / four-layer framework
  that this thread extends to non-equilibrium, time-periodic conditions.
- [[experimental-turbulence-measurement]] — measurement techniques for the experimental
  companion work.

## Open items

- Reza to adjudicate the `Re_s,I→II` conflict (100 vs 280) — see [[stokes-reynolds-number]].
- Verify the conjectured critical `ω⁺` threshold in [[pulsatile-flow]] (thesis flags it as
  needing more work).
