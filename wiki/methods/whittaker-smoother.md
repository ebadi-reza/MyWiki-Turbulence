---
title: Whittaker smoother
type: method
threads:
  - wall-heat-flux-experimental
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Whittaker smoother

**What it is.** A discrete penalized least-squares smoother (Eilers, *Anal. Chem.* 75 (2003) 3631) that balances two competing factors: **smoothness** of the fitted series and **conformity** to the measured data. It returns a smoothed discrete dataset from a noisy one, well suited to preparing experimental profiles for numerical differentiation.

## Why it is used here

In the [[triple-integral-identity]] wall-flux methods, one term requires a **wall-normal derivative of the total flux** (molecular + turbulent). Differentiating raw noisy experimental profiles amplifies noise, so the profile is smoothed first.

In [[2015-ebadi-ijhmt]] the smoother is applied to the **weighted** total heat flux `(1 − η/η_t)·q̃″_total`; dividing back out by `(1 − η/η_t)` yields a profile suitable for differentiation. The weighting exploits boundary-layer physics: absent a local heat source/sink, the weighted profile must be **monotonically decreasing** (max flux at the wall), which also flags erroneous near-wall data. The same smoothing strategy traces to the Mehdi–White skin-friction method.

## Where it appears in Reza's threads

- [[wall-heat-flux-experimental]] — enabling numerical step in the integral method.

Reference: P.H.C. Eilers, "A perfect smoother," *Anal. Chem.* 75 (2003) 3631–3636 (MATLAB implementation therein).
