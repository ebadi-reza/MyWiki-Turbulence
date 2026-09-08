---
title: Romero 2022 — APG inertial sublayer (JFM)
type: source
threads:
  - wind-tunnel-ramp
  - experimental-turbulence-measurement
  - high-Re-analytical-modeling
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Romero et al. (2022) — Inertial sublayer of APG turbulent boundary layers

**Full citation.** S. Romero, S. Zimmerman, J. Philip, C. White, J. Klewicki, "Properties of the
inertial sublayer in adverse pressure-gradient turbulent boundary layers," *J. Fluid Mech.* **937**
(2022) A30, doi:10.1017/jfm.2022.6. Open Access (CC-BY). (Melbourne + UNH; C. White = UNH.)**Reza is not an author, but the FPF ramp used for the measurements was built by A. Ebadi & C.J. Klewicki** (paper's acknowledgement) — so this is the published source for [[wind-tunnel-ramp]].
⚠️ Note **two different Klewickis**: **C.J. Klewicki** (J. Klewicki's son) built the ramp, while the
paper's author (and the "Klewicki" of the [[self-similar-hierarchy]] / four-layer framework) is
**Joseph C. Klewicki** — do not conflate them. PDF: `raw/references/2022_Romero_JFM.pdf`.

## One-paragraph summary

Experimental (hot-wire) study of the **inertial sublayer of adverse-pressure-gradient (APG)
turbulent boundary layers** at high Reynolds number (δ⁺≈7100–7770, modest APG β≤1.8), compared to ZPG data at similar Re and to lower-Re LES/DNS. Using mean-momentum-balance (MMB) and stress-balance analyses plus empirical measures, it asks how far the APG inertial sublayer resembles the ZPG one. Main results: the APG streamwise variance does **not** show a logarithmic decay (unlike ZPG) and is not self-similar, yet **both ZPG and APG exhibit distance-from-the-wall scaling** on the inertial sublayer; scaling-patch theory shows y-scaling is consistent with a **single** velocity scale (→ log-law) *or* **multiple** velocity scales (→ power-law, à la Stratford). See [[adverse-pressure-gradient-tbl]], [[self-similar-hierarchy]].

## The ramp & facility (thread 6 source)

- Measurements in the **Flow Physics Facility (FPF)**, UNH — a ZPG wind tunnel, **2.8 m × 6 m**
  cross-section, **72 m fetch** (Vincenti et al. 2013). [source]
- A **ramp structure** (based on Aubertine & Eaton 2005) was **installed on the ceiling** (not the
  floor); measurements taken on the flat floor → **PG effects without wall curvature**. [source]
- Geometry: FPG region (height −0.4 m over 3.1 m) → ZPG relaxation (~7.0 m) → **APG ramp (height +0.5 m over 5.3 m)** → ZPG downstream (~20 m). Ramp insert ~15 m; APG influence −0.5 ≲ x_scaled ≲ 1.6 (x_scaled normalized by the 5.3 m APG length). [source]
- **Built by A. Ebadi (Reza) & C.J. Klewicki at UNH** (acknowledgement — C.J. Klewicki is J.
  Klewicki's son, *not* the author Joseph C. Klewicki). See [[wind-tunnel-ramp]].

## Setup

- **PG parameters:** Clauser `β = tΔ/tPG = (δ*/τ_w) dP/dx`; acceleration parameter `K = (ν/U∞²)dU∞/dx`; Rotta–Clauser length `Δ = ∫u_τ⁻¹(U∞−U)dy ≈ 3.5δ`; `Re_Δ ≡ Δu_τ/ν = Re_τ`. Present cases: β ≈ 0.9–1.8, K ≈ −0.4 to −0.5×10⁻⁷, Re_τ ≈ 7100–7770. [source]
- **Hot-wire** (in-house 3-wire probe: an ×-array for u,v + a single wire for u; 5 μm gold-plated
  tungsten; Kawall–Shokr–Keffer design; `L⁺=17.6`). `u_τ` from Preston tubes cross-checked by a matched-profile (Clauser-like) method (agree within ±8%). See [[hot-wire-anemometry]]. [source]

## Key results (cited to this paper)

- **MMB terms:** ZPG/channel = 3 terms (VF, TI, MI or PG); **APG = 4 terms** (VF, TI, MI, PG). [source]
- **Inertial-sublayer onset** (VF loses leading order): `y⁺≈3√δ⁺` (ZPG), **`y⁺≈1.5√δ⁺` (APG)**. [source]
- In APG the **TI zero-crossing occurs well beyond** where the VF loses leading order (they coincide in ZPG) → the TI zero-crossing / peak-RS is **no longer a signature** of the inertial-sublayer onset; turbulence does not act as a pure momentum sink there. [source]
- **APG streamwise variance `u²⁺` has no logarithmic decay and is not self-similar** (unlike ZPG) → Townsend/Perry attached-eddy arguments don't transfer directly. [source]
- **Distance-from-the-wall (y-) scaling holds for both ZPG and APG** on the inertial sublayer
  (indicator function collapses vs `y⁺/√δ⁺`; spectral peaks at `λ_x/y≈2`). [source]
- `−uv⁺` exceeds 1 in some APG cases even at small β → local `u_τ` may not be the correct velocity scale; a shift toward **pressure-dependent scaling** as β increases; **β effects diminish as Re rises**. [source]
- **Scaling-patch theory** ([[self-similar-hierarchy|Fife et al. 2009]]): self-similar mean dynamics give y-scaling; a **constant** velocity scale (λ=1) → **log-law**; a **non-constant** scale (`λ∼ϵ⁻σ`, σ>0) → **power-law** `U⁺∼(y⁺)^{2σ/(1+σ)}` (σ=1/3 gives Stratford's half-power law). Log-law constants `κ≈0.384` (1/κ=2.6), `B≈4.4`. [source]

## Notation mapping (this paper vs canon)

| This paper | Meaning | Canon ([[notation]]) |
|---|---|---|
| `δ⁺`, `Re_τ`, `Re_Δ` | friction Reynolds numbers | `Re_τ` (`δ⁺=δ99 u_τ/ν`; `Re_Δ` on Rotta–Clauser Δ) |
| `β = (δ*/τ_w)dP/dx` | Clauser PG parameter | `β` (canon: "pressure-gradient/non-equilibrium parameter") |
| `K = (ν/U∞²)dU∞/dx` | acceleration parameter | `K` |
| `Δ ≈ 3.5δ` | Rotta–Clauser length | `Δ` |
| `Ξ = y⁺dU⁺/dy⁺` | log-law indicator function | see [[log-law]] |
| VF, TI, MI, PG | MMB terms | see [[four-layer-structure]] |
| `ϵ`, scaling patch | small parameter locating a hierarchy layer | see [[self-similar-hierarchy]] |
| `κ≈0.384`, `B≈4.4` | log-law constants (this paper's values) | canon κ≈0.40–0.41, B≈5.0–5.2 |

## Connections

- **[[wind-tunnel-ramp]]** — the ramp Reza built; this paper is its published source.
- [[experimental-turbulence-measurement]] — [[hot-wire-anemometry]] in the FPF.
- [[high-Re-analytical-modeling]] — inertial sublayer, [[self-similar-hierarchy]], [[four-layer-structure]],
  [[log-law]], distance-from-the-wall scaling.
- [[non-equilibrium-pulsatile-flow]] — APG is a (spatial) non-equilibrium perturbation, complementing the (temporal) reciprocating/pulsatile work.
- Same research lineage as [[2019-bautista-jfm]]/[[2020-ebadi-jfm]] (Klewicki, White; Fife/Wei framework).
