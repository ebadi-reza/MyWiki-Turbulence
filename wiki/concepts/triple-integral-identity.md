---
title: Triple integral identity
type: concept
threads:
  - wall-heat-flux-experimental
  - cfd-validation-method
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Triple integral identity

A family of **mathematically exact** integral relations for wall fluxes (wall shear stress / skin friction, and wall heat flux) in 2D wall-bounded flows. The governing mean equation (momentum or energy) is **integrated three times** in the wall-normal direction from the wall to an arbitrary height, and the streamwise-gradient terms are replaced by mathematically equivalent wall-normal-gradient terms. The result expresses the wall flux purely in terms of **wall-normal profiles at a single streamwise station**, with **no explicit streamwise gradients**.

## Why it matters

- **Direct**: no a-priori assumptions about the flow/temperature field, no transport analogies (e.g. Reynolds analogy), no calibration constants.
- **Single-station**: needs profiles at one `x` only — useful when multi-station data, full boundary-layer coverage, or clean outer BCs are not available.
- **Integral, not differential**: much less sensitive to near-wall measurement noise than differentiating a profile at the wall (e.g. extrapolating `∂U/∂y|_w` or `∂Φ/∂y|_w`). Robust to wall-position uncertainty.
- **Decomposition**: the terms attribute the wall flux to distinct physical contributions (mean profile, turbulent flux, total-flux gradient), connecting wall transport to the mean-flow dynamics.

## The two flux expressions (three terms each)

Integrating to an arbitrary height `y_t` (`z_t` in some papers' coordinates), both wall
fluxes split into I (mean profile) + II (turbulent flux) + III (total-flux gradient):

**Wall shear stress (momentum side):**

$$
\tau_w = \frac{2\mu}{y_t^2}\!\int_0^{y_t}\! U\,dy
- \frac{2\rho}{y_t^2}\!\int_0^{y_t}\!(y_t-y)\,\overline{u'v'}\,dy
- \frac{\rho}{y_t^2}\!\int_0^{y_t}\!(y_t-y)^2\frac{\partial}{\partial y}\!\Big(\nu\frac{\partial U}{\partial y}-\overline{u'v'}\Big)dy
$$

**Wall heat flux (thermal side):** the same structure applied to the energy equation (see [[2015-ebadi-ijhmt]]), giving the `q″_w` / [[stanton-number|St]] expression.

In unsteady/spatially-developing flow, term III absorbs the unsteady + pressure-gradient (momentum) or unsteady-temperature (thermal) contributions via the exact substitution ([[2017-pond-compfluids]] Appendix A). For fully-developed channel flow the streamwise-gradient part vanishes.

## Lineage

- **FIK identity** — Fukagata, Iwamoto & Kasagi (2002): decomposition of skin friction
  into laminar + turbulent (Reynolds-stress) contributions in wall-bounded flow.
- **Skin-friction integral method** — Mehdi & White (2011); Mehdi, Johansson, White & Naughton (2014): triple-integrated momentum equation → exact `C_f`/`τ_w` from a single-station profile, tailored for experimental data.
- **Wall-heat-flux integral method** — [[2015-ebadi-ijhmt|Ebadi, Mehdi & White (2015)]]: the **thermal analogue**, triple-integrated energy equation → exact `q″_w`/`St`. See [[wall-heat-flux]], [[stanton-number]].
- **CFD-validation application** — [[2017-pond-compfluids|Pond et al. (2017)]]: the term decomposition of `τ_w` and `q″_w` becomes a **term-by-term validation metric** for RANS models. See [[cfd-validation-method]].
- **Separated / curved-wall validation** — [[2020-wengrove-expfluids|Wengrove et al. (2020)]]: the momentum-side method (called the **MW-MIM**, Mehdi–White momentum integral method) is shown to work in separated flows and over curved surfaces. See [[wall-skin-friction]].

## Practical notes (from separated-flow testing)

- The method needs the **flow-reversal region resolved**: to get the negative `τ_w` in separation within 20%, capture ≈35–75% of the reversal thickness `y_s`; displacing the near-wall point outward monotonically **underestimates** `τ_w`. [source: [[2020-wengrove-expfluids]]]
- On **curved walls**, use surface-following `s–n` coordinates, or apply a **wall-slope correction** `C_f = C_{f,xy}/cosα` to a Cartesian computation (α = local wall slope). ([[2020-wengrove-expfluids|source]])
- Term III (total-flux gradient) tends to dominate; in separation, terms II and III are large, opposite-sign and nearly cancel. ([[2020-wengrove-expfluids|source]])

## Where it appears in Reza's threads

- [[wall-heat-flux-experimental]] — the heat-flux version is Reza's contribution.
- [[cfd-validation-method]] — the same identity family gives term-by-term validation
  metrics against which CFD/RANS models are checked ([[2017-pond-compfluids]]).

## Companion practicalities

- Term requiring a wall-normal derivative of the total flux is the noise-sensitive one;
  a [[whittaker-smoother]] is used to differentiate noisy experimental profiles.
