---
title: Reynolds analogy & turbulent Prandtl number
type: concept
threads:
  - wall-heat-flux-experimental
  - cfd-validation-method
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Reynolds analogy & the turbulent Prandtl number

## Definition

The **Reynolds analogy** assumes that turbulent transport of momentum and of heat are similar, so the turbulent heat flux can be tied to the turbulent momentum flux through a single **turbulent Prandtl number**

$$
Pr_T = \frac{\nu_T}{\alpha_T} = \frac{\overline{u'w'}\,(\partial\Theta/\partial z)}
{\overline{w'\theta'}\,(\partial U/\partial z)}
$$

where `ν_T` is the turbulent (eddy) viscosity and `α_T` the turbulent thermal diffusivity.
In RANS, the heat-flux closure `−w'θ' = (ν_T/Pr_T)·∂Θ/∂z` (eddy-diffusivity) is exactly this analogy, and `Pr_T` is usually taken **constant** (commonly `Pr_T ≈ 0.9`).

## When it holds / breaks

- **Holds (approximately):** steady equilibrium wall flows — `Pr_T` is roughly constant across the layer ([[2017-pond-compfluids]] Fig. 9 shows `Pr_T≈const` in steady channel flow). [source]
- **Breaks down:** non-equilibrium flows. In reciprocating channel flow, `Pr_T` computed directly from DNS is **highly variable in both wall-normal position and phase** — it does not approximate a constant [[2017-pond-compfluids]]. [source]
- **Why:** attributed to (i) intermittent/transitional turbulence and (ii) the unsteady imposed pressure gradient. Per Bradshaw, the analogy can fail under pressure gradients because the **velocity field depends on the pressure field while the temperature field does not** (explicitly). [source]

## Why it matters for Reza's work

- The assumed-constant-`Pr_T` Reynolds analogy is a **key modeling deficiency** exposed by the [[cfd-validation-method|integral validation technique]]: RANS models predict the `τ_w` (momentum) integral terms far better than the `q″_w` (heat) terms, implicating the heat-flux closure. Reliable prediction needs an independent energy-equation solution or a spatially/temporally varying `Pr_T`. [source: [[2017-pond-compfluids]]]
- Contrast: [[2015-ebadi-ijhmt|Ebadi et al. (2015)]] wall-heat-flux method is *direct* and **invokes no transport analogy** — a deliberate strength given the analogy's fragility.

See [[notation]], [[stanton-number]], [[wall-heat-flux]].
