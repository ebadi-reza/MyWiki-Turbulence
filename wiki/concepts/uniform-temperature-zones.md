---
title: Uniform temperature zones (UTZ/TF)
type: concept
threads:
  - high-Re-analytical-modeling
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Uniform temperature zones & thermal fissures (UTZ/TF)

**What it is.** The passive-scalar analogue of the [[uniform-momentum-zones|UMZ/VF]] structure: at high Reynolds number the temperature (passive scalar) field is composed of large **uniform temperature zones (UTZs)** separated by narrow **thermal fissures (TFs)** of high temperature gradient. This is the field version of the classic **ramp–cliff** signature in temperature time series (long gradual ramp, short steep cliff). Introduced/modelled by [[2020-ebadi-jfm|Ebadi et al. (2020)]].

## The UTZ/TF model (Ebadi et al. 2020)

- Founded on the mean-scalar-equation scaling of Zhou, Pirozzoli & Klewicki (2017): the
  balance of MD (molecular diffusion), GT (turbulent-heat-flux gradient) and HG (heat generation) has a **four-layer structure** analogous to [[four-layer-structure|Wei et al.]], and a [[self-similar-hierarchy]] of layer widths `W⁺_θ = (−d²Θ⁺/dy⁺²)^{−1/2}`.
- In the inertial (layer IV) domain `W⁺_θ` is linear in `y⁺`, giving a scalat  [[log-law|log law]] with scalar von Kármán constant `κ_θ = 1/φ²_θc`.
- **Construction:** distribute a finite number of TFs (inertial per the hierarchy, subinertial empirically) → "master" profile → perturb TF positions/temperatures →ensemble → statistical moments. Coupling TF motion to VF motion (from the UMZ/VF model) gives the **streamwise turbulent heat flux** `u'θ'⁺`.

## Why it matters

- First model of passive-scalar transport using the hierarchy-layer / zone-fissure concept,
  and the first to couple scalar and momentum transport models to predict their correlation
  ([[2020-ebadi-jfm]]).
- Connects high-Re structure (thread 2) to heat transfer (thread 4).

## Key findings

- Reproduces mean `Θ⁺`, variance, skewness, kurtosis, and `u'θ'⁺` vs DNS (δ⁺=4088, Pr=0.2–1.0). Mean/variance/heat-flux are ~Pr-independent; **kurtosis strongly Pr-dependent**. [source]
- Streamwise `u'u'⁺/u'θ'⁺ ≈ 2` (surrogate streamwise `Pr_t≈2`). [source]

See [[notation]].
