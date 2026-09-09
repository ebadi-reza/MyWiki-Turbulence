---
title: Internal shear layer
type: concept
threads:
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Internal shear layer

**What it is.** In reciprocating / oscillatory channel flow, an **internal (shear) layer** is a localized region of concentrated mean shear that develops away from the wall during the **late accelerating phases** of the cycle. It **phase-leads** both the near-wall and core regions (it begins to decelerate before they do). [[2016-ebadi-ictam]] identifies it as the **key mechanism of transition** from type III (self-sustaining transition) to type IV (intermittently turbulent) flow.

**Refined picture ([[2019-ebadi-jfm]]).** The internal layer is centred at the **edge of the Stokes layer, `y/l_s≈1`**: on its wallward side the flow **locally accelerates**, on its outer side it **locally decelerates** (a "kink" in the local-acceleration `∂⟨u⟩/∂t` profile). Rationale: outside the Stokes layer the viscous term is small (`~Re_s⁻¹`), so the **unsteady term is the only one that can respond** to the explosive growth of [[turbulent-inertia]]. The kink appears only for the two higher Re_s (801, 1009) — never for Re_s=648.

## Mechanism (per Ebadi et al. 2016)

1. Late acceleration → internal shear layer forms, phase-leading near-wall and core.
2. Its emergence coincides with strong **sink-like [[turbulent-inertia]]** at the same wall-normal location.
3. During deceleration the shear layer likely **rolls up**, triggering instabilities that  transition the flow to a fully-developed turbulent channel (early decelerating phases).
4. Subsequent acceleration suppresses turbulence → flow returns to transitional; cycle repeats.
5. Absent this shear layer (e.g. `Re_s = 648 < 750`), the flow never fully transitions. ([[2019-ebadi-jfm|source]])

## Why it matters

- Provides a concrete, phase-resolved mechanism for transition in periodic flows, tied to the [[stokes-reynolds-number|Stokes Reynolds number]] threshold `Re_s > 750`.

## Where it appears in Reza's threads

- [[non-equilibrium-pulsatile-flow]] — mechanistic centerpiece; expect elaboration in [[2017-pond-compfluids]] and the JFM papers.

See [[notation]].
