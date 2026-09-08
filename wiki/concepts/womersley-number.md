---
title: Womersley number
type: concept
threads:
  - non-equilibrium-pulsatile-flow
  - cfd-validation-method
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Womersley number

## Definition

A dimensionless number for oscillatory / pulsatile flow measuring the **unsteadiness** of
the flow relative to viscous diffusion:
$$Wo = h\sqrt{\frac{\omega}{\nu}}$$
where `h` is a characteristic length (channel half-height), `ω = 2π/T` the angular frequency, and `ν` kinematic viscosity. Its square characterizes the ratio of the **diffusion time scale** `h²/ν` to the **oscillation time scale** `ω⁻¹`:
$$Wo^2 \sim \frac{h^2/\nu}{\omega^{-1}}$$
Large `Wo` → oscillation fast compared to viscous diffusion (thin oscillatory boundary layer, plug-like core); small `Wo` → quasi-steady.

## Relation to the Stokes Reynolds number

With peak Reynolds number `Re_p = 2U_m h/ν` and [[stokes-reynolds-number|`Re_s = U_m l_s/ν`]] (`l_s = √(2ν/ω)`):
$$\frac{Re_p}{Wo} = \sqrt{2}\,Re_s$$
So `Wo` and `Re_p` together fix `Re_s`; increasing `Re_s` (toward turbulence) means **decreasing `Wo` and/or increasing `Re_p`** [[2017-pond-compfluids]]. [source]

## Why it matters

- Primary unsteadiness parameter for the pulsatile/reciprocating thread.
- For `Wo ≳ 0.1` there is a **phase difference between the stress and strain fields**, which most eddy-viscosity models cannot represent — a core reason reciprocating flow is hard for RANS ([[2017-pond-compfluids]]; [[cfd-validation-method]]). [source]

## In Reza's threads

- [[non-equilibrium-pulsatile-flow]] cases: Re_s=648 (Wo=20.47), Re_s=1019 (Wo=17.72). [source]

## ⚠️ Notation note

[[2017-pond-compfluids]] writes the Womersley number as **`α`**. The wiki canon uses **`Wo`** (and reserves `α` for thermal diffusivity). See [[notation]].
