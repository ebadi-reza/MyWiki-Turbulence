---
title: Overview
type: overview
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Overview — Wall-Bounded Turbulence & Heat Transfer

Top-level map of this wiki. Six research threads, all rooted in wall-bounded turbulent flow. This page is the starting point; each thread links out to its own page, and from there to the concept, method, and source pages that support it.

Legend: **[Reza]** = Reza's own contribution · everything else = field background.

## The six threads

1. **[[experimental-turbulence-measurement]]**
   Measuring turbulent flow with PIV, Pitot tube, and hot-wire anemometry.
   The experimental backbone — the measurement techniques the other threads rely on.

2. **[[high-Re-analytical-modeling]]**
   Analytical modeling of high–Reynolds-number turbulent flows.
   The theory side — scaling laws and models for equilibrium wall turbulence.

3. **[[non-equilibrium-pulsatile-flow]]**  *(most references)*
   Experimental + analytical work on non-equilibrium turbulence, especially
   pulsatile flow. Extends the equilibrium picture (thread 2) to time-varying,
   non-equilibrium conditions. Deepest reference base.

4. **[[wall-heat-flux-experimental]]**
   Experimental methods to determine wall heat flux.
   The heat-transfer side; connects velocity-field turbulence to thermal transport.

5. **[[cfd-validation-method]]**  **[Reza]**
   A method Reza introduced to validate CFD models.
   Bridges experiment and computation — uses measured data to test simulations.

6. **[[wind-tunnel-ramp]]**  **[Reza]**
   Design and construction of a ramp installed in a wind tunnel.
   Apparatus/instrumentation work enabling the experimental threads.

## How they connect (grounded in the ingested sources)

- **The [[triple-integral-identity]] is the spine linking threads 4, 5, 1.** The same triple-integration idea (Fukagata–Iwamoto–Kasagi → Mehdi–White) gives: the wall **heat-flux**  method ([[2015-ebadi-ijhmt]], thread 4), the wall **skin-friction** method / MW-MIM
  ([[2020-wengrove-expfluids]], thread 1), and the **CFD term-by-term validation** metric
  ([[2017-pond-compfluids]], thread 5).
- **The [[four-layer-structure]] / [[self-similar-hierarchy]] links threads 2 and 3.** The  equilibrium mean-momentum-balance framework (thread 2) is *borrowed as a turbulence criterion  for oscillatory-flow transition ([[2019-ebadi-jfm]], thread 3) and grounds the   [[uniform-momentum-zones|UMZ/VF]] / [[uniform-temperature-zones|UTZ/TF]] models ([[2019-bautista-jfm]], [[2020-ebadi-jfm]], thread 2).
- **Thread 3 has two faces:** DNS **oscillatory** channel flow (zero mean) and experimental
  **pulsatile** flow (non-zero mean, via the [[neat-wind-tunnel]] rotor-stator). Reynolds analogy
  breaks down here ([[reynolds-analogy]]), which is why the analogy-free integral methods matter.
- **Thread 1 (measurement) underpins 3, 4, 5:** [[piv]], [[ir-thermography]], and the  [[neat-wind-tunnel]] supply the data those threads consume.
- **Thread 6 (ramp) now has a source** — the pressure-gradient ramp Reza built (with Klewicki) in the  UNH [[flow-physics-facility|Flow Physics Facility]] is documented in [[2022-romero-jfm]] (Reza not an
  author, but the apparatus is his build); it enabled high-Re [[adverse-pressure-gradient-tbl|APG TBL]]  hot-wire measurements.
- Shared foundation: [[notation]], [[log-law]], [[turbulent-inertia]], [[dns]].

## Status

All **8 papers in `raw/my-work/` are ingested** (2015 IJHMT, 2016 ICTAM, 2017 Pond, 2019 Ebadi
JFM, 2020 Ebadi JFM, 2019 Bautista, 2019 Biles, 2020 Wengrove), plus the **[[2016-ebadi-thesis|2016 PhD thesis]]** (mined for its Ch. 5 lit review, the **unpublished Ch. 7 pulsatile experiments** → [[pulsatile-flow]], and appendices → [[wall-flux-modulation-frequency]] and control/PIV detail).
Thread 6 (ramp) is now sourced via [[2022-romero-jfm]] (`raw/references/`). See [[log]] for the
ingest history and [[index]] for the full page catalog.
