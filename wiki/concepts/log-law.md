---
title: Logarithmic law of the wall
type: concept
threads:
  - high-Re-analytical-modeling
  - non-equilibrium-pulsatile-flow
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Logarithmic law of the wall

## Definition

In wall-bounded turbulent flow, over an intermediate region the mean streamwise velocity in wall units follows a logarithmic profile:

$$
\langle u\rangle^+ = \frac{1}{\kappa}\ln(y^+) + B
$$

where `κ` is the **von Kármán coefficient** (slope = 1/κ) and `B` the additive constant (intercept at `y⁺=1`). For steady turbulent flow over hydraulically smooth walls, **κ ≈ 0.40 and B ≈ 5.2** (with documented Reynolds-number variation; Nagib & Chauhan 2008).

The log law is a **dimensional necessity** when the inner (`δ_ν = ν/u_τ`) and outer (`h` or `δ`) length scales are sufficiently separated — i.e. when `h⁺` (or Re_τ) is large enough (Smits, McKeon & Marusic 2011).

## Why it matters

- The hallmark of the overlap/inertial region in canonical wall turbulence, and the anchor of [[high-Re-analytical-modeling|analytical high-Re modeling]].
- Modern theory (Wei et al. 2005; Klewicki, Fife & Wei 2009) links the log law to a **self-similar hierarchy** in the mean momentum balance whose signature is the [[four-layer-structure|four-layer structure]].

## In Reza's threads

- [[non-equilibrium-pulsatile-flow]]: in oscillatory channel flow a **transient log region appears** during the early decelerating phases at the higher Re_s. At Re_s=1009 the slope `1/κ` rapidly reaches ≈2.5 (κ≈0.4), while **B always falls below the steady value 5.2** and depends on (Re_s, phase) [[2019-ebadi-jfm]]. The emergence of the log region coincides with the four-layer structure and the fading of the centreline momentum source.
- Slope typically extracted from the **indicator function** `y⁺ d⟨u⟩⁺/dy⁺` (a plateau marks the log region).

## Thermal / scalar log law

The temperature (passive scalar) field has an analogous logarithmic region:

$$
\Theta^+ = \frac{1}{\kappa_T}\ln(y^+) + C_2(Pr), \qquad \Theta = T_w - T(y)
$$

normalized by the friction temperature `T_τ = q″_w/(ρ c_p u_τ)`. The intercept `C₂` depends on Prandtl number. Reported **`κ_T ≈ 0.48`** (varies by flow) [[2019-biles-jfe]].

From the mean-equation [[self-similar-hierarchy]], the inertial-domain scalar layer width `W⁺_θ` is linear in `y⁺` with slope `1/φ_θc`, integrating to a scalar log law with **scalar von Kármán constant `κ_θ = 1/φ²_θc`** ([[2020-ebadi-jfm]]; Zhou et al. 2017). See[[uniform-temperature-zones]].

> ⚠️ **Two symbols, same concept, watch the difference:** `κ_T≈0.48` is the empirical temperature-log-law slope constant ([[2019-biles-jfe]]); `κ_θ=1/φ²_θc` is the scalar von Kármán constant from the hierarchy analysis ([[2020-ebadi-jfm]]). Both denote a "thermal von Kármán constant" but come from different derivations/values — not conflated here.

### Log law in reciprocating flow — the unsteady length scale

In steady flow the log law is a dimensional necessity when the inner (`δ_ν=ν/u_τ`) and outer (`h`) scales are well separated. Reciprocating flow adds a **third length scale**, the **unsteady length
scale `δ_t = u_τ/ω`** (Akhavan et al. 1991a). Log behavior is expected whenever *at least two* of the three scales are widely separated, giving four scenarios ([[2016-ebadi-thesis]] Ch. 5):

| Case | Scale ordering | Log behavior |
|---|---|---|
| 1 | `δ_t ≫ h ≫ δ_ν` | universal law `U⁺=(1/κ)ln y⁺+B` (κ≈0.4, B≈5) |
| 2 | `δ_t ∼ h ≫ δ_ν` | **modified** log law, intercept `B₁(u_τ/hω) ≠ B` |
| 3 | `h ≫ δ_t ≫ δ_ν` | **no** log behavior expected |
| 4 | `h ≫ δ_t ∼ δ_ν` | modified log law, intercept `B₂(u_τ²/νω) ≠ B₁ ≠ B` |

Reza's reciprocating DNS (Re_s=648, 1019) fall under **Case 2**. ([[2016-ebadi-thesis|source]])

### Sensitivity to nonequilibrium

The **temperature** law of the wall is empirically **much more sensitive** to nonequilibrium / pressure-gradient perturbations than the **velocity** law of the wall — even though pressure gradient does not appear in the temperature transport equation. Equilibrium-based wall functions can therefore fail for heat transfer in strong nonequilibrium flows ([[2019-biles-jfe]]).

### Log law under an adverse pressure gradient

In [[adverse-pressure-gradient-tbl|APG]] flow the mean velocity may or may not stay logarithmic:
some studies find `κ`, `B` preserved with the PG effect showing as a stronger wake (Aubertine & Eaton 2005); others find `κ`, `B` vary with β (Nickels 2004; Nagib & Chauhan 2008), and a **half-power law** (Stratford 1959) can emerge in the outer inertial sublayer. [[2022-romero-jfm]] uses the MMB (not `κ`,`B`) to locate the inertial sublayer, reports `κ≈0.384` (`1/κ=2.6`), `B≈4.4`, and shows the log-law is one outcome of distance-from-the-wall scaling (a power-law is the other — see [[self-similar-hierarchy]]).

## Notation

`κ` von Kármán coefficient (≈0.40–0.41) · `B` additive constant (≈5.0–5.2) ·
`κ_θ` scalar von Kármán constant · `y⁺` wall-normal distance in wall units ·
`u⁺` velocity in wall units. See [[notation]].
