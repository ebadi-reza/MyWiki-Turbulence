---
title: Wiki Index
type: index
status: draft
created: 2026-09-03
updated: 2026-09-03
---

# Index — Wall-Bounded Turbulence & Heat Transfer Wiki

Catalog of every page in the wiki. The agent updates this on every ingest.
Read this first when answering a query, then drill into the relevant pages.

## Overview
- [[overview]] — top-level map of the six research threads and how they connect
- [[notation]] — canonical symbol table (the authority on notation)

## Research threads
- [[experimental-turbulence-measurement]] — PIV, hot-wire, IR measurement of turbulent flow
- [[high-Re-analytical-modeling]] — analytical modeling of high–Reynolds-number flows
- [[non-equilibrium-pulsatile-flow]] — non-equilibrium / pulsatile turbulent flow *(most references)*
- [[wall-heat-flux-experimental]] — experimental determination of wall heat flux
- [[cfd-validation-method]] — method for validating CFD models
- [[wind-tunnel-ramp]] — wind-tunnel PG ramp (built by Reza; source: Romero et al. 2022)

## Concepts
- [[triple-integral-identity]] — exact triple-integration method for wall fluxes (shear & heat)
- [[wall-heat-flux]] — `q″_w`: definition, measurement approaches
- [[wall-skin-friction]] — `τ_w`/`C_f`/`u_τ`: definition, measurement approaches (incl. MW-MIM)
- [[stanton-number]] — `St`: non-dimensional wall heat flux, three-term decomposition
- [[stokes-reynolds-number]] — `Re_s` and the five-regime classification of oscillatory flow
- [[four-layer-structure]] — Wei et al. (2005) mean-momentum-balance layers (turbulence criterion)
- [[turbulent-inertia]] — Reynolds-stress gradient in the mean momentum balance
- [[internal-shear-layer]] — transition mechanism in reciprocating/pulsatile flow
- [[pulsatile-flow]] — pulsatile boundary layer (non-zero mean): frequency regimes, equilibrium
- [[womersley-number]] — `Wo`: unsteadiness parameter for oscillatory/pulsatile flow
- [[reynolds-analogy]] — Reynolds analogy & turbulent Prandtl number `Pr_T` (and its breakdown)
- [[log-law]] — logarithmic law of the wall; von Kármán `κ` and constant `B`
- [[self-similar-hierarchy]] — Klewicki–Fife–Wei mean-equation hierarchy; Fife parameter φ_c≈1.62; scaling patches
- [[adverse-pressure-gradient-tbl]] — APG TBL: Clauser β, 4-term MMB, inertial sublayer, log vs power law
- [[uniform-momentum-zones]] — UMZ/VF binary structure of high-Re wall turbulence
- [[uniform-temperature-zones]] — UTZ/TF passive-scalar analogue of UMZ/VF

## Methods
- [[whittaker-smoother]] — penalized least-squares smoothing for differentiating noisy profiles
- [[dns]] — direct numerical simulation (research tool + validation ground-truth)
- [[rans-turbulence-models]] — RANS/EVM closures; low-Re k-ε (Launder–Sharma) and v²-f
- [[anisotropy-invariant-map]] — Lumley–Newman map of turbulence structure (IIa vs IIIa)
- [[piv]] — particle image velocimetry (dual-camera, stitched profiles)
- [[hot-wire-anemometry]] — hot-wire velocity measurement (in-house 3-wire probe)
- [[ir-thermography]] — infrared surface-temperature imaging
- [[neat-wind-tunnel]] — NEAT wind tunnel & feedback-controlled thermal wall plate (apparatus)
- [[flow-physics-facility]] — UNH Flow Physics Facility & the PG ramp (apparatus)

## Sources
- [[2015-ebadi-ijhmt]] — Ebadi, Mehdi & White (2015, IJHMT): exact integral method for wall heat flux *(threads 4, 5)*
- [[2016-ebadi-ictam]] — Ebadi, White, Pond & Dubief (2016, ICTAM): transition in reciprocating channel flow *(thread 3)*
- [[2017-pond-compfluids]] — Pond, Ebadi, Dubief & White (2017, Comp. Fluids): integral validation technique for RANS models *(threads 5, 3, 4)*
- [[2019-ebadi-jfm]] — Ebadi, White, Pond & Dubief (2019, JFM): mean dynamics & transition in oscillatory channel flow *(thread 3, 2)*
- [[2019-bautista-jfm]] — Cuevas Bautista, Ebadi, White, Chini & Klewicki (2019, JFM): UMZ/VF model of the turbulent boundary layer *(thread 2)*
- [[2020-ebadi-jfm]] — Ebadi, Cuevas Bautista, White, Chini & Klewicki (2020, JFM Rapids): UTZ/TF heat-transfer model *(threads 2, 4)*
- [[2019-biles-jfe]] — Biles, Ebadi, Allard & White (2019, JFE): thermal wall plate & NEAT wind tunnel *(threads 1, 4, 3, 5)*
- [[2020-wengrove-expfluids]] — Wengrove, Ebadi, White & Foster (2020, Exp. Fluids): momentum integral method (MW-MIM) for skin friction in separated flows *(threads 1, 5)*
- [[2016-ebadi-thesis]] — Ebadi (2016) PhD dissertation, UNH: mined Ch. 5 (lit review), Ch. 7 (unpublished pulsatile PIV), appendices *(threads 3, 1, 4)*
- [[2022-romero-jfm]] — Romero, Zimmerman, Philip, White & Klewicki (2022, JFM): APG inertial sublayer; documents Reza's FPF ramp *(threads 6, 1, 2)* *(reference; not Reza-authored)*

## Analyses
- [[wall-flux-modulation-frequency]] — why wall shear stress modulates at `ω` but heat flux at `2ω` (thesis Appendix B)
