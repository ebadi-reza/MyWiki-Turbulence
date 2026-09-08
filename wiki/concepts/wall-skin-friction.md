---
title: Wall skin friction
type: concept
threads:
  - experimental-turbulence-measurement
  - cfd-validation-method
  - high-Re-analytical-modeling
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Wall skin friction

**Definition.** The **wall shear stress** is the local tangential surface force per unit area from friction between a wall-bounded flow and its surface:

$$
\tau_w = \mu\left.\frac{\partial u}{\partial y}\right|_{y=0}
$$

Non-dimensionalized as the **skin-friction coefficient** `C_f = τ_w/(½ρU₀²)`, and the source of the **friction velocity** `u_τ = √(τ_w/ρ)` — the primary velocity scale for wall turbulence (the
momentum analogue of [[wall-heat-flux|wall heat flux]] and [[stanton-number|Stanton number]]).

## Why it matters

- A primary scaling parameter and stringent measure of near-wall dynamics; controls a large part of drag (target of drag-reduction) and geophysical processes (erosion, sediment transport, ice ablation). [source: [[2020-wengrove-expfluids]]]
- The validation metric for CFD/RANS models (`C_f` comparison) — see [[cfd-validation-method]].

## Ways to determine it

1. **Near-wall velocity gradient** `μ(∂u/∂y)|_w` — direct but needs well-resolved sublayer data;
   fails where the wall position is uncertain.
2. **Clauser / modified Clauser method** — fit the mean profile to the [[log-law]]; **fails near separation** (the log region vanishes in the separation bubble and only slowly re-emerges after reattachment). [source]
3. **Momentum-thickness / multi-station methods** (Brzek et al.; Volino & Schultz) — need profiles at multiple streamwise locations.
4. **Momentum integral method (MW-MIM)** — the [[triple-integral-identity]] momentum side
   (Mehdi & White 2011; Mehdi et al. 2014): exact `τ_w` from single-station mean-velocity +
   Reynolds-shear-stress profiles, **no boundary-layer-shape assumption**. Robust in separated and curved-wall flows if the flow-reversal region is resolved ([[2020-wengrove-expfluids]]).

## Where it appears in Reza's threads

- [[experimental-turbulence-measurement]] — measured from PIV via the MW-MIM ([[2019-biles-jfe]], [[2020-wengrove-expfluids]]).
- [[cfd-validation-method]] — `C_f` (and its term decomposition) as validation metric.
- [[high-Re-analytical-modeling]] — `u_τ` scaling underlies the [[uniform-momentum-zones|UMZ/VF]] model.

## Notation

`τ_w` wall shear stress · `C_f` skin-friction coefficient · `u_τ` friction velocity · `y_s`
flow-reversal thickness. See [[notation]].
