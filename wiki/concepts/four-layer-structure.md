---
title: Four-layer structure (Wei et al. 2005)
type: concept
threads:
  - high-Re-analytical-modeling
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Four-layer structure of the mean momentum balance

**What it is.** Wei, Fife, Klewicki & McMurtry (*JFM* 522 (2005) 303–327) showed that in canonical wall-bounded turbulent flows (boundary layer, pipe, channel) the **mean momentum balance (MMB)** organizes the wall-normal direction into **four layers**, distinguished by which terms dominate the balance among the viscous stress gradient, the Reynolds-stress gradient (the [[turbulent-inertia]]), and the pressure-gradient/inertial term. The layer boundaries scale on intermediate variables, not purely inner or outer units.

This is a **[[high-Re-analytical-modeling|scaling/analytical]]** result: it replaces the classical inner/outer + log-law picture with a term-balance-based layer decomposition.

## The four layers (steady flow)

With MMB terms A* (pressure gradient), B* (viscous force), C* ([[turbulent-inertia]]), the ratio `B*/C*` exposes the balance (steady flow: unsteady term D*=0), giving four regions (Wei et al. 2005; [[2019-ebadi-jfm]] Fig. 11):

| Region | Balance                                     |
| ------ | ------------------------------------------- |
| i      | \|A*\|  ≈ \|B*\| ≫ \|C*\|                   |
| ii     | \|B*\| ≈ \|C*\| ≫ \|A*\|                    |
| iii    | \|A*\| ≈ \|B*\| ≈ \|C*\| (all three matter) |
| iv     | \|A*\| ≈ \|C*\| ≫ \|B*\|                    |

In three regions two terms dominate one; in region iii all three balance. The peak Reynolds stress sits near the ii/iii boundary. In **unsteady OCF** a fourth term D* (local acceleration) is present, so a single ratio is insufficient — but a four-layer structure still emerges at the turbulent phases.

### Region scaling (canonical channel, Wei et al. 2005 / [[2019-bautista-jfm]] Table 1)

| Region | Ordering (PG, MV, TI) | Δy scaling | ΔU scaling |
|---|---|---|---|
| I | \|PG\|≈\|MV\|≫\|TI\| | O(ν/u_τ) | O(u_τ) |
| II | \|MV\|≈\|TI\|≫\|PG\| | O(√(νh/u_τ)) | O(U_c) |
| III | \|PG\|≈\|MV\|≈\|TI\| | O(√(νh/u_τ)) | O(u_τ) |
| IV | \|PG\|≈\|TI\|≫\|MV\| | O(h) | O(U_c) |

Mean viscous force becomes sub-dominant beyond `y⁺≈2.6√δ⁺` (region III outer edge) — the start of the inertial domain, the `√δ⁺` position predicted by mean-equation theory. Region IV (inertial) is where the [[uniform-momentum-zones|UMZs/VFs]] live. (The inertial-sublayer onset is often quoted as `y⁺≈3√δ⁺` for ZPG; ~`1.5√δ⁺` for APG, [[2022-romero-jfm]].)

### Extra term under a pressure gradient (APG)

Adding an [[adverse-pressure-gradient-tbl|adverse pressure gradient]] gives a **four-term** MMB (VF + TI + MI + **PG**) instead of three ([[2022-romero-jfm]]). A consequence: the **TI zero-crossing decouples from the inertial-sublayer onset** (they coincide in ZPG/channel) — so peak Reynolds stress is no longer the signature of entering the inertial sublayer, and turbulence need not act as a pure momentum sink there.

## Why it matters

- Provides a **physics-based, term-balance criterion** for wall-turbulence structure rather than an assumed profile shape.
- Used in Reza's thread 3 as an **operational definition of "fully-developed turbulence"**: in [[2016-ebadi-ictam]] and [[2019-ebadi-jfm]], a phase in the oscillatory cycle is deemed turbulent when the ordering of the leading MMB terms matches the Wei et al. four-layer structure — it emerges for Re_s=801, 1009 at exactly the steady-like phases, never for Re_s=648. [[2019-ebadi-jfm]] proposes the four-layer structure as an **excellent metric for whether a wall bounded flow has transitioned to turbulence**.

## Where it appears in Reza's threads

- [[non-equilibrium-pulsatile-flow]] — turbulence-onset criterion for periodic flow.
- [[high-Re-analytical-modeling]] — as the analytical framework it originates from.
- Recurs in [[2017-pond-compfluids]] and the JFM papers.

Reference: T. Wei, P. Fife, J. Klewicki, P. McMurtry, "Properties of the mean momentum balance in turbulent boundary layer, pipe and channel flows," *J. Fluid Mech.* 522 (2005) 303–327.
