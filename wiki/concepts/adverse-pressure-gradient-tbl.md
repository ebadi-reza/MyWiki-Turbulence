---
title: Adverse-pressure-gradient TBL
type: concept
threads:
  - high-Re-analytical-modeling
  - experimental-turbulence-measurement
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Adverse-pressure-gradient (APG) TBL & the inertial sublayer

**What it is.** A turbulent boundary layer in which the freestream **decelerates** (`dU∞/dx<0`, `dP/dx>0`) — an adverse pressure gradient. Unlike the canonical ZPG TBL, the mean momentum balance carries an extra pressure-gradient forcing, and the classical log-layer picture needs modification. Studied experimentally on Reza's [[wind-tunnel-ramp|FPF ramp]] in [[2022-romero-jfm]].

## Pressure-gradient parameters

- **Clauser PG parameter** `β = (δ*/τ_w) dP/dx = t_Δ/t_PG` — compares the outer time scale to the PG time scale; `β=O(1)` is where the PG and outer scales interact most strongly. `β=0` ZPG, `β>0` APG, `β<0` FPG. ([[2022-romero-jfm|source]])
- **Acceleration parameter** `K = (ν/U∞²) dU∞/dx`; **Rotta–Clauser length** `Δ ≈ 3.5δ`  (`Re_Δ = Δu_τ/ν = Re_τ`). ([[2022-romero-jfm|source]])
- "Self-preserving" APG TBLs have nominally constant `β` and `Re_τ`.

## Mean momentum balance (4 terms)

For a modest-β APG TBL the inner-normalized MMB is

$$
\underbrace{\frac{\partial^2 U^+}{\partial y^{+2}}}_{VF}
+ \underbrace{\frac{\partial(-\overline{uv}^+)}{\partial y^+}}_{TI}
+ \underbrace{\Big[-U^+\tfrac{\partial U^+}{\partial x^+}-V^+\tfrac{\partial U^+}{\partial y^+}\Big]}_{MI}
+ \underbrace{U_\infty^+\tfrac{\partial U_\infty^+}{\partial x^+}}_{PG} = 0
$$

— **four terms** (VF viscous, TI [[turbulent-inertia]], MI mean inertia, PG pressure gradient), vs three for ZPG/channel (see [[four-layer-structure]]). ([[2022-romero-jfm|source]])

## Inertial-sublayer findings (Romero et al. 2022)

The inertial sublayer is defined by where the **VF term loses leading order** (not by an assumed log region). Key departures from the ZPG TBL:

- **Onset** at `y⁺≈3√δ⁺` (ZPG) but **`~1.5√δ⁺` (APG)**. ([[2022-romero-jfm|source]])
- The **TI zero-crossing decouples from the onset** in APG (they coincide in ZPG) → the TI zero-crossing / peak-Reynolds-stress is no longer the inertial-sublayer signature; turbulence isn't a pure momentum sink there. ([[2022-romero-jfm|source]])
- **Streamwise variance `u²⁺` has no logarithmic decay and isn't self-similar** in APG (it is in ZPG) → attached-eddy (Townsend/Perry) arguments don't transfer directly. ([[2022-romero-jfm|source]])
- Yet **distance-from-the-wall (y-) scaling holds for both** ZPG and APG (indicator function collapses vs `y⁺/√δ⁺`; spectral peaks `λ_x/y≈2`). ([[2022-romero-jfm|source]])
- `−uv⁺` exceeds 1 in some APG cases even at small β → local `u_τ` may not be the right velocity scale; a shift toward **pressure-dependent scaling** as β grows; **β effects diminish as Re rises**. ([[2022-romero-jfm|source]])

## Log-law vs power-law (scaling patches)

Fife-style [[self-similar-hierarchy|scaling-patch]] analysis shows y-scaling is compatible with a **single** velocity scale (`λ=1` → **log-law**) *or* **multiple** velocity scales (`λ∼ϵ⁻σ`, σ>0 → **power-law** `U⁺∼(y⁺)^{2σ/(1+σ)}`; σ=1/3 recovers Stratford's half-power law). So the APG mean profile may be logarithmic or power-law while still respecting distance-from-the-wall scaling. ([[2022-romero-jfm|source]])

## In Reza's threads

- [[high-Re-analytical-modeling]] (inertial sublayer, MMB, scaling patches), [[experimental-turbulence-measurement]] ([[hot-wire-anemometry]]), [[wind-tunnel-ramp]] (the apparatus), [[non-equilibrium-pulsatile-flow]] (spatial non-equilibrium).

See [[notation]], [[log-law]].
