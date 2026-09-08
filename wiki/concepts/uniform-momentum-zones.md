---
title: Uniform momentum zones (UMZ/VF)
type: concept
threads:
  - high-Re-analytical-modeling
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Uniform momentum zones & vortical fissures (UMZ/VF)

**What it is.** At high Reynolds number the turbulent boundary layer is increasingly composed of large **uniform momentum zones (UMZs)** — regions of nearly constant streamwise momentum —separated by thin **vortical fissures (VFs)**: narrow layers of concentrated spanwise vorticity `ω_z` that carry most of the momentum exchange (Meinhart & Adrian 1995; Priyadarshana et al. 2007). Instantaneous streamwise-velocity profiles thus take a **staircase** shape, with the net velocity variation concentrated (intermittently) in the VFs.

## Measured properties

- **VF thickness** `f_w/δ ≈ 1.3/√δ⁺` (order `1/√δ⁺`), comparable to the Taylor microscale (~40% of it); theory (Klewicki 2013) supports the `1/√δ⁺` scaling. [source: [[2019-bautista-jfm]]]
- **Velocity jump** across each fissure is slightly greater than `u_τ`. [source]
- **Number of UMZs** in the inertial region grows ~**logarithmically** with `δ⁺`
  (de Silva et al. 2016). [source]

## The UMZ/VF model (Cuevas Bautista et al. 2019)

Grounded in the [[self-similar-hierarchy]] from the mean momentum equation; each UMZ+VF is one hierarchy layer:
- **Inertial domain** (`y⁺ ≳ φ_c²√δ⁺`): VFs placed by `y⁺_{i+1}=φ_c y⁺_i`, velocity increments `ΔU⁺=φ_c² ln φ_c`, with Fife parameter `φ_c≈1.62`. Number of inertial layers `L=⌊1.04 ln δ⁺−2⌋`.
- **Subinertial domain:** VFs log-spaced; velocity increments from an empirical surrogate `φ̃` (curve-fit of the coordinate-stretching function).
- Build a **master profile**, then **perturb VF positions** (skewed Gaussian `σ=1.6Δy⁺`) with a **momentum-exchange** rule (a VF gains momentum moving wallward, loses it moving outward) → ensemble → statistical moments.
- Prescriptions: fissure width `f_w⁺=6` (results independent of `f_w⁺≲√δ⁺` in the inertial domain); UMZ velocities from VF-edge averages.

**Validation:** vs Lee & Moser (2015) DNS at δ⁺≈5200 — reproduces mean, variance (inner peak + log decay from `y⁺≈2.6√δ⁺`), skewness, kurtosis, and uniquely the **sub-Gaussian** inertial behavior; indicator function → κ≈0.4. Fails near the wall (`y⁺≲10`, no vortex stretching) and at the edge (wake BC). [source]

## Momentum–vorticity connection

The Reynolds-stress gradient decomposes as `dT/dy = v'ω_z − w'ω_y`. The model's VF repositioning captures the `v'ω_z` term (Taylor vorticity transport): `v'ω_z>0` is a momentum source, `<0` a sink. The wall-normal-stretching `w'ω_y` term (near-wall) is not modelled. [source]

## Why it matters

- A physics-based, structure-based alternative to profile-fitting for the inertial region —the momentum backbone of Reza's group's high-Re modeling.
- Extended to the temperature field as [[uniform-temperature-zones|UTZ/TF]] ([[2020-ebadi-jfm]]);
  coupling the two models yields the streamwise turbulent heat flux.

## In Reza's threads

- [[high-Re-analytical-modeling]] — the UMZ/VF model ([[2019-bautista-jfm]]) is the momentum-side model; companion self-sustaining-process theory in Chini et al. (2017).

See [[notation]].
