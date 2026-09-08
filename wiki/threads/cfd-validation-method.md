---
title: Thread — Integral validation technique for CFD/RANS models
type: thread
threads:
  - cfd-validation-method
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Thread 5 — Integral validation technique for CFD/RANS models

A method to validate RANS turbulence models that goes beyond comparing profiles or wall
fluxes: it uses the [[triple-integral-identity]] to decompose the wall fluxes into physically meaningful terms and validates the model **term by term**, exposing compensating (cancelling) errors and pinpointing *why* a model fails.

## Reza's contribution

- **Integral validation technique** — [[2017-pond-compfluids|Pond, Ebadi, Dubief & White
  (2017), Computers & Fluids]] (Reza co-author). Builds directly on Reza's heat-flux
  integral method ([[2015-ebadi-ijhmt]]) and the Mehdi–White skin-friction method.
  - **Standard vs integral validation:** the *standard* technique compares modeled mean
    profiles / wall fluxes to a benchmark and judges agreement; it can be fooled by
    cancellation of errors. The *integral* technique compares the three contributing terms
    of `τ_w` and `q″_w`, giving a direct link between wall flux and mean-flow dynamics.
  - **Demonstration:** DNS vs low-Re RANS (Launder–Sharma k-ε, v²-f) for reciprocating
    channel flow with heat transfer. Standard technique → models look "reasonable" (~20%
    on `τ_w`, `Nu`); integral technique → models miss the physics; decent `Nu` is only a
    **cancellation of errors** (term II* under by ~40%, term III* opposite sign / π out of
    phase / >100% error).
  - **Reynolds-analogy breakdown:** `Pr_T` from DNS is not constant in reciprocating flow ⇒
    a key modeling deficiency. See [[reynolds-analogy]].
  - **Value proposition:** identifies false positives, ties errors to specific physics
    (turbulent-flux modeling, unsteady terms, closure assumptions) — actionable guidance
    for improving models.

## Background & references

- **Fukagata, Iwamoto & Kasagi (2002)** — FIK identity underpinning the decomposition.
- **Mehdi & White (2011); Mehdi et al. (2014)** — skin-friction integral method (momentum side).
- **Standard V&V literature** — Oberkampf & Trucano; Bardina et al.; etc.
- **RANS models** — Launder–Sharma k-ε (1974); Durbin v²-f (1995). See [[rans-turbulence-models]].

## Connections to other threads

- [[wall-heat-flux-experimental]] — supplies the heat-flux integral identity used as a metric.
- [[non-equilibrium-pulsatile-flow]] — provides the challenging test flow (reciprocating,
  transitional, unsteady pressure gradient) that breaks standard validation and Reynolds analogy.

## Open items / gap-filler
- The 2016 thesis chapter on this technique may add the fuller derivation and the Reynolds-
  analogy treatment — revisit when mining the thesis.
