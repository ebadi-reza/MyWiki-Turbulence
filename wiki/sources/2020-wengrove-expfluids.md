---
title: Wengrove 2020 — MW-MIM in separated flows (Exp. Fluids)
type: source
threads:
  - experimental-turbulence-measurement
  - cfd-validation-method
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Wengrove, Ebadi, White & Foster (2020) — Momentum integral method in separated flows

**Full citation.** M.E. Wengrove, A. Ebadi, C.M. White, D.L. Foster, "Evaluation of the momentum integral method to determine the wall skin friction in separated flows," *Experiments in Fluids* **61** (2020) 250. doi:10.1007/s00348-020-03065-8. (Reza = second author; Wengrove Oregon State, White & Foster UNH.)

## One-paragraph summary

Evaluates the **Mehdi–White momentum integral method (MW-MIM)** — the momentum-side
[[triple-integral-identity]] for wall skin friction — in **separated flows** and over **non-flat (curved) geometries**, where a direct `τ_w` measurement is very hard. The MW-MIM is mathematically exact and needs only the wall-normal profiles of **mean velocity and Reynolds shear stress** at a single streamwise station, with no assumption about the boundary-layer shape. Using existing DNS/PIV data of flow over a backward-facing step and a smooth hump, the method is shown to accurately capture the streamwise development of `C_f` through separation — provided the flow-reversal region is adequately resolved — and a simple wall-slope correction extends it to
curved surfaces in Cartesian coordinates. See [[wall-skin-friction]].

## The method (MW-MIM)

Triple-integrating the 2D RANS streamwise momentum equation to a height `n_t` and replacing the streamwise-gradient term `ρI_x` by `∂τ/∂n − ∂p/∂s` (with `τ/ρ = ν ∂u/∂n − u'v'`) gives (Eq. 3):

$$
\tau_w = \underbrace{\frac{2\mu}{n_t^2}\!\int_0^{n_t}\! u\,dn}_{\text{I}}
- \underbrace{\frac{2\rho}{n_t^2}\!\int_0^{n_t}\!(n_t-n)\,\overline{u'v'}\,dn}_{\text{II}}
- \underbrace{\frac{1}{n_t^2}\!\int_0^{n_t}\!(n_t-n)^2\frac{\partial\tau}{\partial n}\,dn}_{\text{III}}
$$

Same three-term structure as the heat-flux method of [[2015-ebadi-ijhmt]]: I mean velocity, II
Reynolds shear stress, III total-stress gradient. `s,n` = surface-following (tangent, wall-normal)
coordinates; for a flat wall `s≡x`, `n≡y`.

## Datasets

- **Backward-facing step:** Le et al. (1997) DNS ("Le97", `Re₀=5100`); Yoshioka et al. (2001) PIV
  ("Yoshioka01", `Re_c=3700`).
- **Smooth hump (curved):** Marquillie et al. (2008) DNS ("Marquillie08", `Re=600`).

## Key results / numbers (cited to this paper)

- MW-MIM accurately captures the `C_f(x)` development through separation — the **zero-crossings and the minimum** of `C_f` — even as near-wall points are removed, **as long as the flow-reversal region is resolved**.
- **Flow-reversal resolution requirement:** to estimate the negative wall stress within 20%, the
  near-wall data must capture **≈35–75%** of the flow-reversal thickness `y_s`  (`y_min ≤ 0.25–0.65 y_s`, dataset/coordinate dependent).
- **Coordinate system:** on curved walls, surface-following `s–n` is more accurate than Cartesian
  `x–y`; but a **wall-slope correction** recovers `x–y` accuracy without redefining coordinates:

$$
C_f = \frac{C_{f,xy}}{\cos\alpha}
$$

  where `α` is the local wall slope. Windward-side `x–y` error up to 14% (uncorrected); <3% in the separation/recovery region.
- **Term contributions** (Marquillie08): **term III (total-stress gradient) dominates** `C_f`
  (≈70–85% on windward side / crest); in the **separation** region terms II and III are large and
  opposite-sign, nearly balancing, with III slightly larger → **negative `τ_w`**.
- Within the separation bubble/recovery region, MW-MIM **monotonically underestimates** `C_f` as the near-wall point is displaced from the wall.
- **Application:** offers the atmospheric-BL / oceanography communities a more accurate route to skin friction in complex flows than far-field methods.

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| `s`, `n` | surface-following tangent, wall-normal | canon `x`, `y` (flat wall) |
| `x`, `y` | Cartesian streamwise, wall-normal | matches canon |
| `C_f = τ_w/(0.5ρU₀²)` | skin-friction coefficient | `C_f`; see [[wall-skin-friction]] |
| `α` | local wall slope (slope correction) | `α` (⚠️ not thermal diffusivity/Womersley here) |
| `y_s` | flow-reversal (separation) thickness | `y_s` |
| `H`, `ER` | step/hump height; channel expansion ratio | descriptive |
| `I_x` | streamwise-gradient term (substituted out) | as in [[triple-integral-identity]] |

## Connections

- Primary thread: [[experimental-turbulence-measurement]] (measuring `τ_w` in complex flows).
- Concepts: [[wall-skin-friction]], [[triple-integral-identity]] (momentum side = MW-MIM),  [[log-law]] (Clauser method it improves on).
- [[cfd-validation-method]] — `C_f` from MW-MIM as a validation target (cites [[2017-pond-compfluids]]).
- Momentum sibling of the heat-flux method [[2015-ebadi-ijhmt]]; both descend from Fukagata et al. (2002) and Mehdi & White (2011, 2014).
- Method: [[piv]], [[dns]].
