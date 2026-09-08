---
title: Cuevas Bautista, Ebadi, White, Chini & Klewicki (2019) — A uniform momentum zone–vortical fissure model of the turbulent boundary layer
type: source
threads:
  - high-Re-analytical-modeling
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Cuevas Bautista et al. (2019) — UMZ/VF model of the turbulent boundary layer

**Full citation.** J.C. Cuevas Bautista, A. Ebadi, C.M. White, G.P. Chini, J.C. Klewicki, "A uniform momentum zone–vortical fissure model of the turbulent boundary layer," *J. Fluid Mech.* **858** (2019) 609–633. doi:10.1017/jfm.2018.769. (Reza = second author; White & Chini
UNH, Klewicki Melbourne/UNH.) The **momentum-side** model that [[2020-ebadi-jfm|Ebadi et al.
(2020)]] extended to passive scalars.

## One-paragraph summary

A simple **one-dimensional dynamical model of the streamwise velocity fluctuations** in
high-Reynolds-number wall turbulence, built from the [[uniform-momentum-zones|UMZ/VF]] structure: large uniform momentum zones separated by thin vortical fissures. A "master" velocity profile is constructed by placing a discrete number of VFs across the layer, with number and positions set by the [[self-similar-hierarchy]] derived from the mean momentum equation. The VFs are then randomly displaced (exchanging momentum as they move) to generate instantaneous profiles; ensembles yield statistical moments. The modelled mean, variance, skewness and kurtosis agree remarkably well with DNS, and — uniquely among structure-based models — the model reproduces the **sub-Gaussian** skewness/kurtosis of the inertial domain.

## Theoretical basis

- Mean momentum equation, inner-normalized — boundary layer: MI + MV + TI = 0; channel:
  `1/δ⁺` (PG) + MV + TI = 0, with `T⁺ ≡ −u'v'⁺` the Reynolds stress. Three terms: mean inertia / pressure gradient, mean viscous force (MV), [[turbulent-inertia]] (TI). [source]
- **Four-region structure** (ratio MV/TI; Wei et al. 2005): mean viscous force becomes sub-dominant beyond `y⁺ ≈ 2.6√δ⁺` (outer edge of region III) → inertial domain. Region widths/increments scale on `√(νh/u_τ)`, `u_τ`, `U_c` (Table 1). See [[four-layer-structure]]. [source]
- **Self-similar hierarchy:** the mean equation rescales to a parameter-free invariant form on
  a hierarchy of layers of width `W⁺`; on the inertial domain `W⁺` is **linear in y⁺**, `dW⁺/dy⁺ = 1/φ_c`, with **Fife similarity parameter `φ_c=(1+√5)/2≈1.62`** and `φ_c²=1/κ`. Discrete stacking: `y⁺_{i+1}=φ_c y⁺_i`, `ΔU⁺=φ_c² ln φ_c`. See [[self-similar-hierarchy]]. [source]

## Key results / numbers (cited to this paper)

- **VF thickness** `f_w/δ ≈ 1.3/√δ⁺` (~O(1/√δ⁺)), comparable to the Taylor microscale (~40% of it; Eisma 2015); **velocity jump per fissure slightly exceeds `u_τ`**. [source]
- **Number of inertial hierarchy layers** `L = ⌊1.04 ln δ⁺ − 2⌋` (≈ number of UMZs `N_UMZ` in
  region IV); asymptotic estimates over-predict measured `N_UMZ` (de Silva 2016) — a 0.75  velocity-in-VF correction improves agreement. [source]
- **Model inputs (best):** fissure width `f_w⁺ = 6` (results **independent of `f_w⁺`** in the
  inertial domain, `f_w⁺≲√δ⁺`); VF displacement PDF = **positively skewed Gaussian,  `σ=1.6Δy⁺_i`**; **momentum-exchange** rule (VF gains momentum moving wallward, loses moving outward). ~5000 realizations (~1 min on a PC). [source]
- **Validation** vs Lee & Moser (2015) DNS at **δ⁺ ≈ 5200** (`U_c⁺≈26.5`, ~6 UMZs beyond region III): reproduces mean, variance (inner peak; **log decay of variance from  `y⁺≈2.6√δ⁺`**), skewness, kurtosis — including the **sub-Gaussian** inertial behavior.  Indicator function `Ξ=y⁺dU⁺/dy⁺` shows a pseudo-plateau → `κ=1/Ξ≈0.4`. [source]
- **Discrepancies:** near wall (`y⁺≲10`) and boundary-layer edge — attributed to neglected
  vortex stretching/reorientation and the ill-defined wake boundary condition. [source]
- **Momentum–vorticity link:** `dT/dy = v'ω_z − w'ω_y`; the model's VF repositioning captures
  the `v'ω_z` term (Taylor vorticity transport). `v'ω_z>0` = momentum source (advection away  from wall); `<0` = sink. [source]
- Companion dynamical theory: Chini et al. (2017) self-sustaining-process (SSP) model of the
  inertial layer; predicts VF thickness ~`δ⁺^{−2/5}`. [source]

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| `δ⁺` | friction Reynolds number `δ u_τ/ν` | canon `Re_τ` |
| `φ_c` | Fife similarity parameter `(1+√5)/2≈1.62` | `φ_c` (`φ_c²=1/κ`) |
| `W⁺` | hierarchy-layer width (momentum) | `W` (cf. scalar `W_θ`) |
| `T⁺ = −u'v'⁺` | Reynolds shear stress | `−u'v'` |
| `f_w` | vortical-fissure width | `f_w` |
| `Ξ = y⁺dU⁺/dy⁺` | log-law indicator function | see [[log-law]] |
| MI, MV, TI, PG | mean momentum-eq terms | descriptive |

Coordinates: x streamwise, **y wall-normal**, z spanwise — matches canon.

## Connections

- Thread: [[high-Re-analytical-modeling]] (core).
- Concepts: [[uniform-momentum-zones]] (source of record), [[self-similar-hierarchy]],  [[four-layer-structure]], [[turbulent-inertia]], [[log-law]].
- Extended to passive scalars in [[2020-ebadi-jfm]] ([[uniform-temperature-zones|UTZ/TF]]).
- Method: [[dns]] (validation: Lee & Moser 2015).
- Key references: Meinhart & Adrian (1995); Priyadarshana et al. (2007); Wei et al. (2005);
  Klewicki (2013a,b,c); Klewicki et al. (2014); Chini et al. (2017); de Silva et al. (2016, 2017).
