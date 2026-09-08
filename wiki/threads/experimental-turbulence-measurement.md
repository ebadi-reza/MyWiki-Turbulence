---
title: Experimental turbulence measurement
type: thread
threads:
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Thread 1 — Experimental measurement of turbulent flow

Measuring turbulent wall-bounded flow — velocity and temperature fields — using PIV, Pitot
tube, hot-wire anemometry, IR thermography and thermocouples, plus the facilities that make
those measurements possible. The experimental backbone the other threads rely on.

## Reza's contribution

- **NEAT wind tunnel & thermal wall plate** — [[2019-biles-jfe|Biles, Ebadi, Allard & White
  (2019), JFE]] (Reza co-author). A feedback-controlled sectioned [[neat-wind-tunnel|thermal
  wall plate]] and wind tunnel purpose-built to study heat transfer in **nonequilibrium**
  boundary layers: imposes isothermal / gradient / step thermal BCs, or holds `T_w` fixed
  (±0.5 °C) even under unsteady, strongly 3D flow. Validated (ZPG isothermal, temperature step, hemisphere). Enables the same facility + measurement techniques across many flow types — key for robust [[cfd-validation-method|CFD validation]].
  - Measurement techniques demonstrated: [[piv]] (dual-camera, stitched profiles; `τ_w` via the
    Mehdi–White integral method), [[ir-thermography]], fine-wire thermocouple traversing.
  - Generates the experimental **pulsatile** flow (rotor-stator) — see [[pulsatile-flow]].

- **Momentum integral method in separated flows** — [[2020-wengrove-expfluids|Wengrove, Ebadi, White & Foster (2020), Exp. Fluids]] (Reza co-author). Evaluates the Mehdi–White momentum integral method (MW-MIM) — the momentum side of the [[triple-integral-identity]] — for [[wall-skin-friction|wall skin friction]] in **separated flows and over curved surfaces**  (backward-facing step, smooth hump). Shows `C_f(x)` through separation is captured if the flow-reversal region is resolved (≈35–75% of `y_s` for <20% error), and gives a practical wall-slope correction `C_f = C_{f,xy}/cosα` for curved walls in Cartesian coordinates.

*(Reza's PIV/experimental work also appears in the [2016 PhD thesis] chapters — revisit during
the thesis gap-fill for the pulsatile-BL experiments and ZPGBL validation.)*

- **Hot-wire APG measurements on the FPF ramp** — [[2022-romero-jfm|Romero et al. (2022)]] used the
  [[wind-tunnel-ramp|ramp Reza built]] in the [[flow-physics-facility|FPF]] to acquire [[hot-wire-anemometry|hot-wire]] data in an adverse-pressure-gradient TBL (δ⁺≈7100–7770). Reza is not an author, but the apparatus is his. Physics on [[adverse-pressure-gradient-tbl]].

## Background & references

- **Mehdi & White (2011)** — skin-friction integral method used to get `τ_w` from PIV profiles
  (momentum sibling of the [[triple-integral-identity]]).
- **Shea et al. (2014)** — profile-stitching method for multi-FOV PIV.
- **Al-Asmi & Castro (1993)** — rotor-stator oscillatory-flow generation.
- DNS baselines for validation: Araya & Castillo (2012); Wu & Moin (2010).

## Connections to other threads

- [[wall-heat-flux-experimental]] — thermal wall plate + `τ_w`/`q″_w` measurement.
- [[non-equilibrium-pulsatile-flow]] — the experimental pulsatile counterpart to the DNS
  oscillatory work.
- [[cfd-validation-method]] — measurements feed model validation.

## Open items
- Mine the thesis for PIV details, uncertainty analysis, and ZPGBL validation.
