---
title: Hot-wire anemometry
type: method
threads:
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Hot-wire anemometry

**What it is.** A point measurement of fluid velocity from the convective heat loss of a fine electrically heated wire: as flow speed rises, cooling rises, and (in constant-temperature mode)
the current needed to hold the wire's temperature/resistance tracks the velocity. Very high
temporal resolution and small sensing volume make it the workhorse for turbulence spectra and
high-Reynolds-number wall flows.

## As used in Reza's work ([[2022-romero-jfm]])

- **In-house three-wire probe** (Kawall–Shokr–Keffer design): an **×-array** of two wires resolves
  the streamwise `u` and wall-normal `v` velocities simultaneously, plus a **single wire** for `u`
  alone; the redundant single wire reduces the transverse-velocity sensitivity to per-sensor
  calibration drift (Morrill-Winter et al. 2015). 5 μm gold-plated tungsten wires; single-wire
  `L⁺=17.6`, ×-array projected length `L⁺/√2`. [source]
- Speed response calibrated in the freestream before/after each profile; angular response via an articulating jet.
- **Friction velocity `u_τ`** obtained from Preston tubes and cross-checked with a matched-profile (Clauser-chart-like) method — agreement within ±8% (and ±2.3% vs a corrected Clauser method). [source]
- Sample interval reported as `Δt_s⁺ = (1/f_s) u_τ²/ν`.

## Why it matters

- Resolves turbulence statistics (variance, Reynolds stress, skewness/kurtosis) and spectra needed to test inertial-sublayer / [[self-similar-hierarchy]] theory in [[adverse-pressure-gradient-tbl|APG]]
  and ZPG boundary layers.
- Complements the [[piv|PIV]] and [[ir-thermography]] techniques used elsewhere in the group.

## In Reza's threads

- [[experimental-turbulence-measurement]] (core); the measurements were taken on the
  [[wind-tunnel-ramp|FPF ramp]] Reza built, in the [[flow-physics-facility]].

See [[notation]].
