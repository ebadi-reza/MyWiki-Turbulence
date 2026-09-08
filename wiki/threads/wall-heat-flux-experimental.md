---
title: Wall heat flux (experimental)
type: thread
threads:
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Thread 4 — Experimental determination of wall heat flux

Methods to determine the [[wall-heat-flux]] `q″_w` experimentally in turbulent wall-bounded flows, where near-wall temperature measurements are hardest and least
reliable.

## Reza's contribution

- **Exact integral method for wall heat flux** — [[2015-ebadi-ijhmt|Ebadi, Mehdi & White
  (2015), IJHMT]]. Triple-integrates the RANS energy equation to express `q″_w` (and
  [[stanton-number|St]]) from **single-station** wall-normal profiles of mean temperature and turbulent heat flux, with **no explicit streamwise gradients**. The thermal analogue of the Mehdi–White skin-friction method; see [[triple-integral-identity]].
  - Direct (no analogies/assumptions/calibration), integral (noise-robust), works with
    partial-BL data and ill-defined outer BCs.
  - `St` decomposes into mean-temperature (I, ∝Pe⁻¹), turbulent-heat-flux (II, dominant),
    and total-flux-gradient (III) terms.
  - Validated on DNS (≈0 error) and Tsuji–Nagano natural-convection experiments (6–10%).
  - Robust to wall position (`Δy⁺≤10` → <3% in St); more sensitive to lower than upper
    integration limit; ±2.81% (95% CI) under realistic noise via [[whittaker-smoother]].

## Background & references

- **FIK identity** — Fukagata, Iwamoto & Kasagi (2002): skin-friction decomposition, origin of the integral-identity approach.
- **Mehdi & White (2011); Mehdi et al. (2014)** — skin-friction integral method that Ebadi (2015) extends to heat transfer. *(candidates to ingest as source pages)*
- **DNS thermal BL data** — Araya & Castillo (2012); Wu & Moin (2010).
- **Experimental natural-convection BL** — Tsuji & Nagano (1988, two papers): hot-wire +  cold-wire velocity/temperature measurements over a heated vertical plate.

## Experimental apparatus

- **Thermal wall plate & NEAT wind tunnel** — [[2019-biles-jfe]] (Reza co-author): a feedback-controlled sectioned [[neat-wind-tunnel|thermal wall plate]] that imposes controller  thermal BCs (isothermal / gradient / step) for thermal-BL experiments, with `q″_w` inferred from measured profiles and `τ_w` from the Mehdi–White integral method. Introduces the  thermal [[log-law]] (`κ_T≈0.48`) and its heightened nonequilibrium sensitivity, and the  [[stanton-number|Colburn]] estimate.

## Connections to other threads

- [[cfd-validation-method]] — shares the [[triple-integral-identity]] machinery; measured  wall fluxes become validation targets for CFD.
- [[experimental-turbulence-measurement]] — supplies the near-wall velocity/temperature
  measurement techniques ([[piv]], [[ir-thermography]]) and the facility the method consumes.

## Open items

- Ingest the Mehdi–White skin-friction papers if Reza has copies (the momentum-side  sibling of this thread).
