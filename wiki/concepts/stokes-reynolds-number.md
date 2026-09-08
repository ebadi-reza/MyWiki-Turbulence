---
title: Stokes Reynolds number & five regimes
type: concept
threads:
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Stokes Reynolds number & the five flow-regime classification

## Definition

For oscillatory / reciprocating wall-bounded flow, the governing similarity variable is the **Stokes Reynolds number**

$$
Re_s = \frac{U_m\, l_s}{\nu}, \qquad l_s \equiv \sqrt{\frac{2\nu}{\omega}}
$$

where `U_m` is the amplitude of the cross-sectional average velocity, `l_s` is the **Stokes-layer thickness**, `ω` the angular frequency of oscillation, and `ν` the kinematic viscosity. `l_s` is the viscous penetration depth of an oscillating wall/flow.

## The five flow regimes

Reciprocating (and oscillatory Stokes) flow is classified by `Re_s` into five regimes
[Akhavan et al. 1991; Ozdemir et al. 2014, via [[2016-ebadi-ictam]]]:

| Regime | Name | Critical Re_s to enter next regime |
|---|---|---|
| I | laminar | `I→II ≈ 100` |
| II | disturbed laminar (fluctuations, but mean stays laminar) | `II→III ≈ 500` |
| III | self-sustaining transition (mean departs from laminar) | **`III→IV ≈ 750`** |
| IV | intermittently turbulent (turbulent part of the cycle) | `IV→V ≈ 3460` |
| V | fully-developed turbulent (turbulent whole cycle; log law absent only ~10% around reversal) | — |

Critical values compiled in [[2019-ebadi-jfm]] from Hino et al. (1976), Akhavan et al.
(1991a), Ozdemir et al. (2014), Jensen et al. (1989). [source]

> **`Re_s,I→II` — keep both (resolved by Reza):** [[2019-ebadi-jfm]] gives ≈**100**; [[2016-ebadi-thesis]] (Ch. 5) gives ≈**280** (Akhavan et al. 1991a). This is **not an error to reconcile** — the I→II onset (first appearance of velocity fluctuations) is *very sensitive to initial and background disturbances*, so there is genuine, expected scatter in the reported critical value across studies. Both values stand. ✓ confirmed by Reza.

## Transition threshold vs Womersley (Re_c = f(W))

Transition is governed by `Re_s ∝ Re/W`, i.e. a critical Reynolds number `Re_c = f(W)`. For **reciprocating** flow the relationship is **linear and well established: `Re_c = 700 W`** (equivalently `Re_s ≃ 500`). For **pulsatile** flow the `Re_c`–`W` relationship is complicated and transition can be advanced or delayed by `W` ([[2016-ebadi-thesis]] §7.3; see [[pulsatile-flow]]). [source]

## Why it matters

- It is the primary control parameter for transition in periodic flows — the axis along which Reza's reciprocating-channel work is organized.
- In [[2016-ebadi-ictam]]: `Re_s = 648` is type III, `Re_s = 1019` is type IV, and the III→IV transition (emergence of the [[internal-shear-layer]]) requires **Re_s > 750**. [source]

## Where it appears in Reza's threads

- [[non-equilibrium-pulsatile-flow]] — the organizing parameter for the whole thread; recurs in [[2017-pond-compfluids]] and the JFM papers.

See [[notation]].
