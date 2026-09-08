---
title: Pond, Ebadi, Dubief & White (2017) — An integral validation technique of RANS turbulence models
type: source
threads:
  - cfd-validation-method
  - non-equilibrium-pulsatile-flow
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Pond, Ebadi, Dubief & White (2017) — Integral validation technique of RANS models

**Full citation.** I. Pond, A. Ebadi, Y. Dubief, C.M. White, "An integral validation technique of RANS turbulence models," *Computers and Fluids* **149** (2017) 150–159. doi:10.1016/j.compfluid.2017.02.016. (Reza = second author; Pond & Dubief UVM, White UNH.) Corresponds to the "Integral Validation Technique of RANS Turbulence Models" chapter of the [2016 PhD thesis].

## One-paragraph summary

Introduces an **integral validation technique** for RANS turbulence models: rather than comparing modeled mean profiles / wall fluxes to a benchmark and judging "agreement"
(the *standard technique*), the wall shear stress `τ_w` and wall heat flux `q″_w` are each expressed via the [[triple-integral-identity]] as a sum of **three physically meaningful contributing terms**, and the model is validated **term by term**. Because a wall flux is an integral of the flow dynamics above the wall, matching the flux alone can mask compensating errors; matching the terms tests whether the model captures the physics and pinpoints *why* it fails. Demonstrated on DNS vs two low-Re RANS models for[[non-equilibrium-pulsatile-flow|reciprocating channel flow]] with heat transfer, it shows the models reproduce `Nu` only through a **cancellation of errors**, and that [[reynolds-analogy|Reynolds analogy]] breaks down in this flow.

## Setup

- **Flow / parameters:** reciprocating channel flow (period `T`, `ω=2π/T`). [[womersley-number|Womersley number]] `Wo = h√(ω/ν)` (written `α` in this paper);
  peak Reynolds number `Re_p = 2U_m h/ν`; relation `Re_p/Wo = √2·Re_s` with [[stokes-reynolds-number|`Re_s = U_m l_s/ν`]]. `Wo²` = ratio of diffusion time `h²/ν` to oscillation time `ω⁻¹`. [source]
- **Cases:** Re_s=648 (Wo=20.47; edge of disturbed-laminar/intermittently-turbulent) and
  Re_s=1019 (Wo=17.72; well within intermittently turbulent). Critical `Re_s ≈ 750` for III→IV transition. [source]
- **Temperature:** passive scalar, `Pr=0.7`, isothermal walls (bottom=1, top=0).
- **DNS:** finite-difference code (Dubief et al.), 128³ (checked at 256³), domain 10h×5h×2h; phase-averaged over 10 periods, 32 phases/period.
- **RANS:** OpenFOAM 2.3.0, PISO, 2D, **low-Reynolds-number models** (first grid point
  `z⁺≤1`, near-wall resolved, no wall functions). Two models: **Launder–Sharma k-ε** (with damping functions) and **v²-f** (no damping functions; uses wall-normal velocity variance for near-wall scaling). Heat flux closed with eddy diffusivity + Reynolds analogy,`Pr_T=0.9`. See [[rans-turbulence-models]].

## The integral metrics

Triple-integrating the momentum and (passive-scalar) energy equations and replacing streamwise/unsteady gradients by wall-normal-gradient equivalents (following Fukagata et
al.; Mehdi et al.; [[2015-ebadi-ijhmt|Ebadi et al. 2015]]) gives, for a height `z_t`: `τ_w` = term I (mean velocity) + II (turbulent flux `−u'w'`) + III (total-flux gradient); `q″_w` = I* (mean temperature) + II* (turbulent heat flux `w'θ'`) + III* (total-heat-flux gradient). In reciprocating flow term III is effectively the unsteady-velocity + pressure-gradient term and III* the unsteady-temperature term (Appendix A). For the RANS models the turbulent-flux terms are replaced by the model closures (`−u'w'=ν_T ∂U/∂z`,`−w'θ'=(ν_T/Pr_T)∂Θ/∂z`).

## Key results / numbers (cited to this paper)

- **Standard technique:** both models predict `τ_w` and `Nu` to **within ~20%** of DNS (Eqs. 21–22) → superficially "reasonable." Largest errors at `6π/16≤φ≤11π/16` (accel→decel), where transition occurs; RANS transition occurs at a **phase-lead** vs DNS. [source]
- **Integral technique:** models predict the `τ_w` terms reasonably but the `q″_w` terms **poorly**. Term II* (turbulent heat flux) **underpredicted by ~40%** during deceleration;  term III* (unsteady temperature) **opposite sign, π out of phase, error >100%** (Table 4). The two errors **cancel serendipitously** → decent `Nu` despite wrong physics. [source]
- Term error magnitudes (Eq. 25): II, II* ≈ 20–30%; III ≈ 10–15%; III* > 100%. [source]
- **Reynolds-analogy breakdown:** `Pr_T` computed directly from DNS (Eq. 26) is **highly variable** across the channel and between phases — *not* constant (unlike steady channel flow where `Pr_T≈const`). ⇒ Reynolds analogy is a flawed assumption in reciprocating flow; reliable prediction needs an independent energy-equation solution or a better `Pr_T` representation. [source] See [[reynolds-analogy]].
- **Root causes identified:** (a) turbulent-flux term underpredicted during deceleration;
  (b) unsteady velocity/temperature fields unreliably predicted; (c) Reynolds-analogy
  breakdown. [source]

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| `z` | **wall-normal** direction | canon uses **`y`** for wall-normal ⚠️ |
| `y` | spanwise direction | canon uses `z` for spanwise ⚠️ |
| `α` | **Womersley number** | canon uses **`Wo`**; canon `α` = thermal diffusivity ⚠️ |
| `Re_p` | peak Reynolds number `2U_m h/ν` | `Re_p` |
| `θ`, `Θ` | temperature (fluctuating, mean) | canon uses `φ'`, `Φ` |
| `λ` | fluid thermal conductivity | canon uses `k_f` |
| `Pr_T = ν_T/α_T` | turbulent Prandtl number | `Pr_T` — see [[reynolds-analogy]] |
| `h` | channel half-height | `h` |

⚠️ Three overlapping clashes here: (1) `α` = Womersley vs thermal diffusivity; (2) `z` = wall-normal vs spanwise; (3) `θ` = temperature vs the thread's `φ`=phase. Kept canonical in [[notation]]; this paper's usages recorded above.

## Connections

- Defines [[cfd-validation-method]] (Reza's contribution, co-authored).
- Extends the [[triple-integral-identity]] (heat side [[2015-ebadi-ijhmt]]; momentum side Mehdi & White) into a CFD-validation tool.
- Test flow: [[non-equilibrium-pulsatile-flow]] (reciprocating channel flow); uses  [[stokes-reynolds-number]], [[womersley-number]].
- Concepts: [[reynolds-analogy]], [[stanton-number]] (`Nu` analogue), [[four-layer-structure]].
- Methods: [[rans-turbulence-models]], [[dns]].
- References: Fukagata et al. (2002); Mehdi & White (2011, 2014); Ebadi et al. (2015); Di Liberto & Ciofalo (2011); Launder–Sharma (1974); Durbin v²-f (1995).
