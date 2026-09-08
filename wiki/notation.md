---
title: Notation
type: reference
status: draft — AWAITING REZA'S REVIEW
created: 2026-09-03
updated: 2026-09-08
---

# Notation — Canonical Symbol Table

This is the single authority on notation for the wiki. When a source paper uses different symbols or conventions, record the mapping on that paper's source page — do NOT change the canon here, and never silently convert conventions inside a claim.


## Velocity & wall scaling

| Symbol | Meaning | Notes |
|---|---|---|
| `U`, `u` | mean / instantaneous streamwise velocity | 
| `u'`, `v'`, `w'` | fluctuating velocity components (streamwise, wall-normal, spanwise) |
| `u_tau` | friction velocity, √(τ_w/ρ) | 
| `u+` | velocity in wall units, U/u_tau | 
| `y+` | wall-normal distance in wall units, y·u_tau/ν |
| `δ` | boundary-layer thickness | 
| `δ*` | displacement thickness | 
| `θ` | momentum thickness | 
| `τ_w` | wall shear stress | `μ(∂u/∂y)|_w`; see [[wall-skin-friction]] |
| `C_f` | skin-friction coefficient, `τ_w/(½ρU₀²)` | see [[wall-skin-friction]] |
| `s`, `n` | surface-following tangent / wall-normal coords | flat wall: `s≡x`, `n≡y` ([[2020-wengrove-expfluids]]) |
| `α` (wall slope) | local wall angle for slope correction | ⚠️ context: not thermal diffusivity/Womersley |
| `y_s` | flow-reversal (separation) thickness | [[2020-wengrove-expfluids]] |

## Log law

| Symbol | Meaning | Notes |
|---|---|---|
| `κ` | von Kármán constant (≈0.40–0.41) |  — value varies by study |
| `B` | log-law additive constant (≈5.0–5.2) |  — value varies by study |
| `κ_θ` | scalar von Kármán constant (hierarchy) | `κ_θ = 1/φ²_θc` ([[2020-ebadi-jfm]]); see [[log-law]] |
| `κ_T` | thermal log-law slope constant (empirical, ≈0.48) | ([[2019-biles-jfe]]); ⚠️ distinct from `κ_θ` — see [[log-law]] |
| `C₁`, `C₂` | velocity / temperature log-law intercepts | `C₁`≈`B`; `C₂=C₂(Pr)` |
| `Θ` | temperature deficit `T_w−T(y)` | in [[2019-biles-jfe]]; distinct from mean-temp `Φ` |
| `φ_c` | Fife similarity parameter, `(1+√5)/2 ≈ 1.62` | golden ratio; VF spacing; see [[self-similar-hierarchy]] |
| `φ_θc` | scalar hierarchy similarity parameter | `κ_θ = 1/φ²_θc` |
| `W`, `W_θ` | self-similar hierarchy layer width (momentum, scalar) | scalar: `(−d²Θ⁺/dy⁺²)^{−1/2}`; see [[self-similar-hierarchy]] |
| `f_w` | vortical-/thermal-fissure width | `f_w/δ≈1.3/√δ⁺`; see [[uniform-momentum-zones]] |
| `Ξ` | log-law indicator function, `y⁺dU⁺/dy⁺` | plateau → `κ=1/Ξ`; see [[log-law]] |
| `L` | number of inertial hierarchy layers | `⌊1.04 ln δ⁺ − 2⌋` |
| `ω_z` | spanwise vorticity | concentrated in VFs |

## Reynolds numbers

| Symbol | Meaning | Notes |
|---|---|---|
| `Re_τ` | friction Reynolds number, u_tau·δ/ν | written `δ⁺` in [[2020-ebadi-jfm]] |
| `Re_θ` | momentum-thickness Reynolds number |  
| `Re_x`, `Re_D` | based on streamwise distance / diameter |

## Turbulence quantities

| Symbol | Meaning | Notes |
|---|---|---|
| `-u'v'` (or `⟨u'v'⟩`) | Reynolds shear stress | — sign convention varies |
| `∂(-u'v')/∂y` | turbulent inertia (Reynolds-stress gradient) | see [[turbulent-inertia]] |
| `k` | turbulent kinetic energy |
| `ε` | TKE dissipation rate | 
| `I` | turbulence intensity | 
| `b_ij` | Reynolds-stress anisotropy tensor | `⟨u'ᵢu'ⱼ⟩/q² − δ_ij/3`; see [[anisotropy-invariant-map]] |
| `IIa`, `IIIa` | 2nd & 3rd invariants of `b_ij` | anisotropy invariant map |
| `u'_rms` | rms velocity fluctuation | `⟨u'²⟩^{1/2}` |

## Pulsatile / non-equilibrium (thread 3)

| Symbol | Meaning | Notes |
|---|---|---|
| `Wo` | Womersley number, `h√(ω/ν)` | ⚠️ [[2017-pond-compfluids]] writes this as `α`; see [[womersley-number]] |
| `Re_p` | peak Reynolds number, `2U_m h/ν` | `Re_p/Wo = √2·Re_s` |
| `ω` | angular frequency of pulsation, `2π/T` | 
| `f` | pulsation frequency | 
| `β`  | Clauser pressure-gradient parameter, `(δ*/τ_w) dP/dx` | see [[adverse-pressure-gradient-tbl]] |
| `K`  | acceleration parameter, `(ν/U∞²) dU∞/dx` | favorable/adverse PG |
| `Δ`  | Rotta–Clauser length, `∫u_τ⁻¹(U∞−U)dy ≈ 3.5δ` | `Re_Δ = Δu_τ/ν = Re_τ` |
| `ϵ` (scaling patch) | small parameter locating a hierarchy layer | see [[self-similar-hierarchy]] |
| `Re_s` | Stokes Reynolds number, `U_m l_s/ν` | see [[stokes-reynolds-number]] |
| `l_s` | Stokes-layer thickness, `√(2ν/ω)` | viscous penetration depth |
| `l_s⁺` | inner-normalized Stokes-layer thickness | `l_s/(ν/u_τ)` |
| `δ_t` | unsteady length scale, `u_τ/ω` | 3rd scale for reciprocating log law; see [[log-law]] |
| `ω⁺` | inner-normalized pulsation frequency, `ω/(u_τ²/ν)` | `= Str²/2`; see [[pulsatile-flow]] |
| `Str` | Strouhal number, `ω/(u_τ/l_s)` | pulsatile flow |
| `Ã(y,t)` | perturbation (oscillatory/coherent) component | triple decomposition `A=Ā+Ã+A'` |
| `U_m` | amplitude of cross-sectional average velocity | reciprocating flow |
| `φ` | **phase angle** within the oscillation cycle | ⚠️ distinct from `φ'` (fluctuating temperature) |
| `∂(−u'v')/∂y` | turbulent inertia (Reynolds-stress gradient) | see [[turbulent-inertia]] |

## Heat transfer (thread 4)

| Symbol | Meaning | Notes |
|---|---|---|
| `q″_w` | wall heat flux (power per unit wall area) | canonical; some OCR renders as `q_w` |
| `Φ` | mean temperature | adopted from [[2015-ebadi-ijhmt]] |
| `φ'` | fluctuating temperature | adopted from [[2015-ebadi-ijhmt]] |
| `v'φ'` | turbulent (wall-normal) heat flux | overbar = correlation |
| `α` | thermal diffusivity | `α = k_f/(ρ C_p)` |
| `Nu` | Nusselt number | 
| `Pr` | Prandtl number | 
| `Pe` | Péclet number, `U∞δ/α = Re·Pr` | from [[2015-ebadi-ijhmt]] |
| `Gr_x` | Grashof number, `gβ(Φ_w−Φ∞)x³/ν²` | natural convection |
| `St` | Stanton number, `q″_w/[ρ C_p U∞(Φ_w−Φ∞)]` | see [[stanton-number]] |
| `Pr_T` | turbulent Prandtl number, `ν_T/α_T` | see [[reynolds-analogy]] |
| `ν_T` | turbulent (eddy) viscosity | RANS closure |
| `α_T` | turbulent thermal diffusivity | RANS closure |
| `δ_T` | thermal boundary-layer thickness |
| `T+` | temperature in wall units | 
| `θ+`  | non-dimensional temperature | 
| `θ_τ` | friction temperature, `(α/u_τ)(dΘ/dy)|_w` | thermal analogue of `u_τ` |
| `Pr_t` | turbulent Prandtl number | streamwise `Pr_t≈2` in [[2020-ebadi-jfm]]; see [[reynolds-analogy]] |
| UMZ/VF | uniform momentum zones / vortical fissures | see [[uniform-momentum-zones]] |
| UTZ/TF | uniform temperature zones / thermal fissures | see [[uniform-temperature-zones]] |

## Fluid properties

| Symbol | Meaning | Notes |
|---|---|---|
| `ρ` | density | 
| `ν` | kinematic viscosity | 
| `μ` | dynamic viscosity | [
| `k_f` | thermal conductivity of fluid |note clash with TKE `k` |

## Known conflicts to watch

- `k` is used for both TKE and thermal conductivity — the table uses `k` for TKE and `k_f` for conductivity. [REVIEW] confirm you're OK with that split.
- Reynolds shear stress sign convention (`u'v'` vs `-u'v'`) differs by author. 
- `φ` means **phase angle** in the pulsatile/reciprocating thread but `φ'` means **fluctuating temperature** in the heat-transfer thread — kept distinct, watch context.
- **Coordinate convention:** canon uses `y` = wall-normal, `z` = spanwise (so `v'` =  wall-normal fluctuation, `w'` = spanwise). ⚠️ [[2017-pond-compfluids]] swaps these:  `z` = wall-normal, `y` = spanwise, `w'` = wall-normal fluctuation. Recorded per-source.
- `α` = thermal diffusivity in canon, but = **Womersley number** in [[2017-pond-compfluids]]   (canon uses `Wo`). `θ` = momentum thickness in canon, but = **temperature** in
  [[2017-pond-compfluids]] (canon uses `Φ`/`φ'`); `λ` = conductivity there (canon `k_f`).
