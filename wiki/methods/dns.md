---
title: Direct numerical simulation (DNS)
type: method
threads:
  - non-equilibrium-pulsatile-flow
  - high-Re-analytical-modeling
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Direct numerical simulation (DNS)

**What it is.** Numerical solution of the Navier–Stokes (and, when relevant, energy) equations resolving **all** turbulent scales down to the dissipative range, with no turbulence model. Provides fully-resolved, low-noise fields — used both as a research tool and as ground-truth for validating experimental methods.

## Roles in this wiki

- **Research tool** — Reza's reciprocating-channel-flow studies use DNS to phase-resolve
  the mean momentum balance and identify the [[internal-shear-layer]] ([[2016-ebadi-ictam]], and the fuller Pond/JFM papers).
- **Validation ground-truth** — highly discretized, noise-free DNS datasets are used to test the [[triple-integral-identity]] wall-flux method in the absence of experimental noise ([[2015-ebadi-ijhmt]]: Araya–Castillo, Wu–Moin datasets).

## Where it appears in Reza's threads

- [[non-equilibrium-pulsatile-flow]], [[wall-heat-flux-experimental]], [[cfd-validation-method]] (as the counterpart to the CFD being validated).

*(Stub — expand with the specific codes/resolutions once the Pond and JFM sources are ingested.)*
