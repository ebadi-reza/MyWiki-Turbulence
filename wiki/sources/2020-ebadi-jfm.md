---
title: Ebadi 2020 — UTZ/TF heat-transfer model (JFM)
type: source
threads:
  - high-Re-analytical-modeling
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Ebadi et al. (2020) — UTZ/TF heat-transfer model of turbulent channel flow

**Full citation.** A. Ebadi, J.C. Cuevas Bautista, C.M. White, G. Chini, J. Klewicki, "A heat transfer model of fully developed turbulent channel flow," *J. Fluid Mech.* **884** (2020) R7 (Rapids). doi:10.1017/jfm.2019.1006. (Reza = first author; White & Chini UNH, Klewicki Melbourne.) The **passive-scalar companion** to the UMZ/VF momentum model of [[2019-bautista-jfm|Cuevas Bautista et al. (2019)]].

## One-paragraph summary

A simple **one-dimensional model of passive-scalar (heat) transport** in high-Reynolds-number turbulent channel flow. Its premise: just as the velocity field is composed of [[uniform-momentum-zones|uniform momentum zones (UMZs)]] separated by thin vortical fissures (VFs), the temperature field is composed of **uniform temperature zones (UTZs)** separated by **thermal fissures (TFs)** — see [[uniform-temperature-zones]]. Informed by the mean-scalar-equation scaling analysis of Zhou, Pirozzoli & Klewicki (2017) and the [[self-similar-hierarchy]] framework, a finite number of TFs are distributed across the channel to form a "master" profile; their positions and temperatures are then perturbed to generate ensembles from which statistical moments are computed. Coupling the UTZ/TF model with the UMZ/VF model reproduces the **streamwise turbulent heat flux**. Validated against DNS over a range of Prandtl numbers.

## Model basis

- **Mean scalar transport equation** (uniform heat generation `Q`, isothermal walls), inner-normalized (Eq. 2.3):

$$
\underbrace{\frac{1}{Pr}\frac{d^2\Theta^+}{dy^{+2}}}_{MD}
  + \underbrace{\frac{dT^+_\theta}{dy^+}}_{GT}
  + \underbrace{\frac{1}{\delta^+}}_{HG} = 0
$$

  MD molecular diffusion, GT gradient of wall-normal turbulent heat flux (`T⁺_θ=−v'θ'⁺`), HG heat generation. Analogous to the mean momentum equation. [source]
- Zhou et al. (2017) showed this balance has a **four-layer structure** (ratio MD/GT), analogous to [[four-layer-structure|Wei et al. (2005)]] for momentum. [source]
- **Self-similar hierarchy:** layer width `W⁺_θ = (−d²Θ⁺/dy⁺²)^{−1/2}`; in the inertial (layer IV) domain `W⁺_θ` is linear in `y⁺`, `dW⁺_θ/dy⁺ = 1/φ_θc`, with scalar von Kármán constant `κ_θ = 1/φ²_θc` → a scalar [[log-law|log law]]. See [[self-similar-hierarchy]]. [source]
- Friction temperature `θ_τ = (α/u_τ)(dΘ/dy)|_w`; heat generation `Q = θ_τ u_τ / h`. [source]

## Key results / numbers (cited to this paper)

- Discrete hierarchy in layer IV: `Δy⁺ ≈ [(φ_θc+1)/φ_θc] y⁺_i`,
  `ΔΘ⁺ ≈ φ²_θc ln[(φ_θc+1)/φ_θc]`. Number of inertial TFs `N_TF ≈ ⌊ln(Pr δ⁺) − 0.8⌋`. [source]
- Inertial/subinertial split at `y⁺ = φ²_c √δ⁺` (momentum) / `2.5√(δ⁺/Pr)` (scalar);
  VF spacing `y⁺_{j+1} ≈ φ_c y⁺_j` with **Fife similarity parameter `φ_c=(1+√5)/2≈1.62`**. [source]
- TF width `f⁺_w = 6` prescribed (results independent of `f⁺_w` in the inertial domain). [source]
- Coupling to UMZ/VF (TF motion tied to VF motion, "case iv") gives streamwise `u'u'⁺/u'θ'⁺ ≈ 2` → surrogate **streamwise turbulent Prandtl number `Pr_t ≈ 2`**
  (cf. Holt & Proctor 2008). [source]
- **Validation:** DNS of Pirozzoli, Bernardini & Orlandi (2016) at **δ⁺ (Re_τ) = 4088**,  **Pr = 0.2, 0.71, 1.0**. Model reproduces mean `Θ⁺`, variance `θ'²⁺`, skewness, kurtosis, and streamwise heat flux `u'θ'⁺`. [source]
- **Pr-dependency:** mean, variance, and heat flux show little Pr-dependency (0.2≤Pr≤1);
  **skewness and especially kurtosis are strongly Pr-dependent** (kurtosis ← small-scale
  variability). [source]

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| `Θ`, `θ'` | mean, fluctuating temperature | canon `Φ`, `φ'` (this paper uses θ) |
| `α` | thermal diffusivity | canon `α` (matches; ≠ Womersley here) |
| `δ⁺` | friction Reynolds number `u_τ h/ν` | canon `Re_τ` |
| `φ_c` | Fife similarity parameter `(1+√5)/2≈1.62` | `φ_c` |
| `κ_θ`, `φ_θc` | scalar von Kármán constant; `κ_θ=1/φ²_θc` | `κ_θ`, `φ_θc` |
| `θ_τ` | friction temperature | `θ_τ` |
| `W_θ` | hierarchy layer width (scalar) | `W_θ` |
| `Pr_t` | (streamwise) turbulent Prandtl number | see [[reynolds-analogy]] |
| UMZ/VF, UTZ/TF | zone/fissure structures | see [[uniform-momentum-zones]], [[uniform-temperature-zones]] |

Note: here `α` = thermal diffusivity and `y` = wall-normal (canon). Coordinate/`α` usage is the opposite of [[2017-pond-compfluids]] — no clash with canon.

## Connections

- Threads: [[high-Re-analytical-modeling]] (primary), [[wall-heat-flux-experimental]].
- Concepts: [[uniform-temperature-zones]], [[uniform-momentum-zones]], [[self-similar-hierarchy]], [[four-layer-structure]], [[log-law]].
- Built on [[2019-bautista-jfm]] (UMZ/VF momentum model) and Zhou et al. (2017) scalar scaling.
- DNS: Pirozzoli et al. (2016).
