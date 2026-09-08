---
title: Wall heat flux
type: concept
threads:
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Wall heat flux

**Definition.** The wall heat flux `q″_w` is the local power per unit area transferred between a fluid and a bounding wall. It is the primary scaling variable for thermal boundary-layer flows and a stringent measure for verifying turbulence heat-transfer models.

At the wall the flux is molecular (no-slip → no turbulent transport at `y=0`):

$$
q''_w = -k_f\left.\frac{\partial \Phi}{\partial y}\right|_{w}
$$

where `k_f` is the fluid thermal conductivity and `Φ` is the mean temperature.

## Why it matters

- Controls performance, efficiency, and life-cycle of thermal systems; drives many geophysical flows.
- An indicator of near-wall dynamics — hence hard to measure well: near-wall temperature data have the largest error (probe interference, optical reflections, limited spatial resolution, exacerbated at high Reynolds/Péclet). See [[2015-ebadi-ijhmt]] §1.

## Ways to measure it

1. **Temperature-difference across a substrate** (analytical / numerical / inverse conduction methods).
2. **Analogy methods** — infer from measured mass or momentum transfer.
3. **Direct near-wall temperature-gradient** measurement / extrapolation to the wall (highly sensitive to wall-position error).
4. **Integral method** — [[triple-integral-identity]], from single-station profiles of mean temperature and turbulent heat flux; robust to noise and wall position. This is Reza's contribution, [[2015-ebadi-ijhmt]].

## Where it appears in Reza's threads

- [[wall-heat-flux-experimental]] — the whole point of the thread.
- Related non-dimensional forms: [[stanton-number]] (`St`), Nusselt `Nu`.

## Notation

`q″_w` wall heat flux · `Φ` mean temperature · `φ'` fluctuating temperature · `v'φ'` turbulent (wall-normal) heat flux · `α` thermal diffusivity · `k_f` conductivity. See [[notation]].
