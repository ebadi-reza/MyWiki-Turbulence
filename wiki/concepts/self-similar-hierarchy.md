---
title: Self-similar hierarchy (Klewicki–Fife–Wei)
type: concept
threads:
  - high-Re-analytical-modeling
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Self-similar hierarchy (Klewicki–Fife–Wei framework)

**What it is.** An analytical framework for high-Reynolds-number wall turbulence built from the **mean equations** rather than assumed profile shapes. Analysis of the mean momentum(and, for scalars, mean scalar) equation reveals a **hierarchy of internal layers** on which the mean equation can be **continuously rescaled into a single parameter-free form** with all leading terms retaining significance (Wei et al. 2005; Fife et al.; Klewicki 2013; Klewicki et al. 2014). The existence of this self-similar hierarchy is what underlies the [[log-law|logarithmic]] mean profile, and its term-balance signature is the [[four-layer-structure]].

## Key elements

- **Layer width `W`** = the local rescaling length = the size of the turbulent motions responsible for wallward momentum flux (Klewicki et al. 2014). Momentum-side `W⁺` from DNS is invariant with δ⁺ and, on the **inertial domain, linear in y⁺** with slope `1/φ_c`; scalar-side `W⁺_θ = (−d²Θ⁺/dy⁺²)^{−1/2}` (Zhou et al. 2017). [source: [[2019-bautista-jfm]], [[2020-ebadi-jfm]]]
- **Fife similarity parameter** `φ_c = (1+√5)/2 ≈ 1.62` (golden ratio) = inverse of the  asymptotic slope of `W⁺(y⁺)` on the inertial domain, and it satisfies **`φ_c² = 1/κ`**
  (von Kármán constant). It sets the geometric fissure spacing `y⁺_{i+1} = φ_c y⁺_i` and the velocity increment per layer `ΔU⁺ = φ_c² ln φ_c`; inertial/subinertial split at `y⁺=φ_c²√δ⁺`, inertial-domain onset (region III outer edge) at `y⁺≈2.6√δ⁺`. [source]
- **Number of inertial layers** `L = ⌊1.04 ln δ⁺ − 2⌋` — grows logarithmically with δ⁺ (countably infinite as δ⁺→∞). [source]
- **Scalar von Kármán constant** `κ_θ = 1/φ²_θc`. [source]
- "Logarithmically many" internal layers span the inertial region — the conceptual basis for the [[uniform-momentum-zones|UMZ/VF]] and [[uniform-temperature-zones|UTZ/TF]] models.

## Scaling patches → log-law *or* power-law

A **scaling patch** (Fife et al. 2009) is a subdomain where the space variable and the MMB can be rescaled so all terms are `O(1)`; a small parameter `ϵ` (via a modified Reynolds-stress term `T⁺_ϵ`) labels each patch. [[2022-romero-jfm]] extends this to APG TBLs (`T⁺_ϵ = T⁺ + ∫MI dy⁺ + (PG−ϵ)y⁺`) and shows:
- if self-similar mean dynamics hold with a **constant** velocity scale (`λ=1`) → distance-from-the-wall scaling → **logarithmic** mean profile;
- if the velocity scale is **non-constant** (`λ∼ϵ⁻σ`, σ>0) → y-scaling still holds but the mean profile is a **power-law** `U⁺∼(y⁺)^{2σ/(1+σ)}` (σ=1/3 recovers Stratford's half-power law).

So distance-from-the-wall scaling is the deeper invariant; whether it yields a log-law or a power-law depends on the velocity-scale hierarchy — relevant to [[adverse-pressure-gradient-tbl|APG flows]]. [source]

## Why it matters

- The theoretical backbone of Reza's group's high-Re modeling: it justifies the discrete zone/fissure models and links them to the classical log law.
- The same four-layer / hierarchy motif appears as a **turbulence criterion** in the
  oscillatory-flow work ([[2019-ebadi-jfm]]) — connecting threads 2 and 3.

## In Reza's threads

- [[high-Re-analytical-modeling]] (core), with heat-transfer application in [[wall-heat-flux-experimental]].

References: Wei, Fife, Klewicki & McMurtry (2005); Klewicki (2013); Klewicki et al. (2014); Klewicki & Oberlack (2015); Morrill-Winter et al. (2017); Zhou, Pirozzoli & Klewicki (2017); Chini et al. (2017, self-sustaining-process theory). Model realizations in [[2019-bautista-jfm]] (momentum) and [[2020-ebadi-jfm]] (scalar). See [[notation]].
