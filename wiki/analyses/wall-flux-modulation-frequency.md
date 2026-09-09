---
title: Wall-flux modulation frequency (τ_w vs 2ω)
type: analysis
threads:
  - non-equilibrium-pulsatile-flow
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Wall shear stress vs heat flux modulation frequency (reciprocating flow)

**Question.** In reciprocating channel flow forced at frequency `ω`, at what frequency do the wall shear stress and the wall heat flux (Nusselt number) modulate?

**Answer (Appendix B toy model, [[2016-ebadi-thesis]]):** the **wall shear stress modulates at the forcing frequency `ω`**, but the **wall heat flux / Nu modulates at twice the forcing frequency,`2ω`**.

## Derivation (centerline, leading order)

Near the channel centerline, viscous forces and advection are negligible, so the momentum balance reduces to

$$
\frac{\partial u}{\partial t} = -\frac{1}{\rho}\frac{\partial P}{\partial x}
$$

With a cosinusoidal pressure gradient `∂P/∂x = cos(ωt)`, integrating gives

$$
u(t) = C_1 \sin(\omega t)
$$

so velocity — and hence **wall shear stress — modulates at `ω`**.

The thermal transport equation near the centerline reduces to

$$
\frac{\partial \Theta}{\partial t} + u\frac{\partial \Theta}{\partial x} = 0
$$

Assuming `∂Θ/∂x` itself modulates with the forcing frequency, the advective product `u·∂Θ/∂x`
carries a `sin(ωt)·(forcing)` structure that integrates to

$$
T(t) = C_2 \cos(2\omega t)
$$

so temperature — and hence **wall heat flux / Nu — modulates at `2ω`**. ([[2016-ebadi-thesis|source]])

## Why it matters

- A clean, quotable consequence of the **advective coupling** in the scalar equation: the thermal field inherits a frequency-doubling that the momentum field does not. Consistent with the
  frequency-doubling of the scalar-transport terms seen in [[2017-pond-compfluids]] (the `Nu` integral terms have half the period of the `τ_w` terms).
- Practical implication for sampling/experiment design in periodic thermal flows: resolve the heat-flux signal at `≥2ω`.

## Caveats

- It is an explicitly labeled **"toy model"** (leading-order, centerline, prescribed `∂Θ/∂x`  modulation) — indicative, not a full solution. [source: [[2016-ebadi-thesis]] Appendix B]

## Connections

- [[non-equilibrium-pulsatile-flow]], [[wall-heat-flux]], [[stanton-number]],  [[2017-pond-compfluids]] (frequency-doubling of scalar terms).
