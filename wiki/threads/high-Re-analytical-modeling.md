---
title: High-Re analytical modeling
type: thread
threads:
  - high-Re-analytical-modeling
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Thread 2 — Analytical modeling of high-Reynolds-number flows

Theory and reduced-order modeling of equilibrium wall turbulence at high Reynolds number,
built from the **mean equations** and their **self-similar hierarchy** rather than from assumed profile shapes. This thread supplies the equilibrium framework that thread 3
(non-equilibrium/pulsatile) extends and borrows as a turbulence criterion.

## Reza's contribution

- **UTZ/TF heat-transfer model** — [[2020-ebadi-jfm|Ebadi et al. (2020), JFM Rapids]]   (Reza first author). A 1-D model of passive-scalar (heat) transport: the temperature field as [[uniform-temperature-zones|uniform temperature zones separated by thermal fissures]],  built on the [[self-similar-hierarchy]] and the mean-scalar-equation scaling of Zhou et al. (2017). Coupling it to the [[uniform-momentum-zones|UMZ/VF]] momentum model reproduces the streamwise turbulent heat flux; validated vs DNS at δ⁺=4088 for Pr=0.2–1.0. **First** scalar-transport model using the hierarchy/zone-fissure concept and first to couple scalar  and momentum models. Links thread 2 to [[wall-heat-flux-experimental|thread 4]].

- **UMZ/VF momentum model** — [[2019-bautista-jfm|Cuevas Bautista et al. (2019), JFM]] (Reza co-author). A 1-D dynamical model of the streamwise velocity fluctuations from the  [[uniform-momentum-zones|UMZ/VF]] structure: a master profile of discrete VFs placed per the  [[self-similar-hierarchy]] (Fife `φ_c≈1.62`, `φ_c²=1/κ`, `L=⌊1.04 ln δ⁺−2⌋` layers), then perturbed with a momentum-exchange rule → ensembles → moments. Validated vs Lee & Moser DNS (δ⁺≈5200); the **only structure-based model to reproduce the sub-Gaussian** skewness/kurtosis of the inertial domain, and recovers κ≈0.4 from the indicator function. This is the momentum-side model that [[2020-ebadi-jfm]] extends to passive scalars.

## Background & references

- **Wei, Fife, Klewicki & McMurtry (2005)** — [[four-layer-structure|mean momentum balance
  four-layer structure]]; the foundational term-balance analysis.
- **Klewicki (2013); Klewicki et al. (2014)** — [[self-similar-hierarchy|self-similar mean
  dynamics]] in wall turbulence.
- **Zhou, Pirozzoli & Klewicki (2017)** — mean-scalar-equation scaling with uniform heat  generation (the scalar-side analogue used by [[2020-ebadi-jfm]]).
- **Meinhart & Adrian (1995); Priyadarshana et al. (2007)** — evidence for  [[uniform-momentum-zones|UMZs/VFs]].
- **Smits, McKeon & Marusic (2011)** — high-Re wall turbulence review; conditions for the
  [[log-law]].
- **Romero et al. (2022)** — [[2022-romero-jfm]]: extends the inertial-sublayer / scaling-patch
  framework to **[[adverse-pressure-gradient-tbl|adverse-pressure-gradient]]** TBLs (hot-wire data on  Reza's [[wind-tunnel-ramp|FPF ramp]]); shows distance-from-the-wall scaling underlies both a log-law
  (single velocity scale) and a power-law (multiple scales).

## Connections to other threads

- [[non-equilibrium-pulsatile-flow]] — borrows the four-layer/hierarchy framework as a
  transition/turbulence criterion; the [[log-law]] emerges transiently there.
- [[wall-heat-flux-experimental]] — the UTZ/TF model predicts heat transport; the  [[triple-integral-identity]] gives the wall heat flux.

## Open items
- Both flagship modeling papers ([[2019-bautista-jfm]] momentum, [[2020-ebadi-jfm]] scalar)
  are ingested. Consider an analysis page comparing UMZ/VF and UTZ/TF construction side by side.
