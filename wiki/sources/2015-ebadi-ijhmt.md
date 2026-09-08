---
title: Ebadi, Mehdi & White (2015) — An exact integral method to evaluate wall heat flux
type: source
threads:
  - wall-heat-flux-experimental
  - cfd-validation-method
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Ebadi, Mehdi & White (2015) — Exact integral method for wall heat flux

**Full citation.** A. Ebadi, F. Mehdi, C.M. White, "An exact integral method to evaluate wall heat flux in spatially developing two-dimensional wall-bounded flows," *International Journal of Heat and Mass Transfer* **84** (2015) 856–861. doi:10.1016/j.ijheatmasstransfer.2014.12.068. (Reza = first author; White group, UNH.)

## One-paragraph summary

Presents a mathematically **exact** integral method to determine the wall heat flux `q″_w` (and Stanton number `St`) in turbulent wall-bounded flows from **wall-normal profiles of mean temperature and turbulent heat flux measured at a single streamwise station**. It is the thermal analogue of the Mehdi–White skin-friction integral method, which in turn follows the Fukagata–Iwamoto–Kasagi (FIK) identity. The RANS energy equation is integrated three times in the wall-normal direction and the streamwise- gradient term is replaced by a mathematically equivalent wall-normal-gradient term, so that **no explicit streamwise gradients remain**. Because it is direct (no a-priori flow or temperature-field assumptions, no transport analogies, no calibration) and integral (hence insensitive to near-wall noise), it is useful when multi-station data, whole-BL coverage, or well-defined outer BCs are unavailable. Validated against DNS and against Tsuji–Nagano natural-convection experiments. See [[triple-integral-identity]], [[wall-heat-flux]], [[stanton-number]].

## The method

For steady, 2D, incompressible turbulent flow (neglecting viscous-dissipation heating), the RANS energy equation is integrated **thrice** in `y` from the wall to an arbitrary height `y_t`. The key move is replacing the lumped streamwise-gradient term `G_x` with its exact wall-normal-gradient equivalent (`G_x = ∂/∂y(α ∂Φ/∂y − v'φ')`). Result:

$$\frac{q''_w}{\rho C_p} = \frac{1}{y_t^2}\left[2\alpha\int_0^{y_t}(\Phi_w-\Phi)\,dy
+ 2\int_0^{y_t}(y_t-y)\,\overline{v'\phi'}\,dy
+ \int_0^{y_t}(y_t-y)^2\frac{\partial}{\partial y}\!\left(\alpha\frac{\partial\Phi}{\partial y}-\overline{v'\phi'}\right)dy\right]$$

Only wall-normal profiles of **mean temperature** `Φ` and **turbulent heat flux** `v'φ'` at **one** streamwise location, up to arbitrary height `y_t`, are needed. Normalizing by `δ`, `U∞`, and `(Φ_w − Φ∞)` gives the Stanton-number form (Eq. 4) with three additive contributions:

- **Term I** — mean-temperature contribution; ∝ `Pe⁻¹`, so it shrinks as Péclet rises.
- **Term II** — turbulent-heat-flux contribution; **dominant term**.
- **Term III** — gradient of the total (molecular + turbulent) heat flux.

This decomposition connects wall transport to the mean-flow dynamics (cited to source).

## Key results / numbers (all cited to this paper)

- **Term contributions to St** (DNS + experimental): II dominates (~60–78%), III next (~9–35%), I smallest (~5–15%) and decreasing with Pe. [source]
- **DNS validation** (Araya–Castillo [27]; Wu–Moin [28]): recovered St ≈ published value, effectively zero difference at integration limit `η_t = 1`. [source]
- **Wall-position robustness:** shifting the wall-normal origin by `Δy⁺ ≤ 10` changes  St by **< 3%** — far more robust than a differential wall-gradient method. [source]
- **Integration-limit sensitivity:** more sensitive to the **lower** limit than the upper. If lower limit `a⁺ < 10`, diminishing return from extending the upper limit; if `a/δ > 0.05`, push the upper limit as high as possible. [source]
- **Noise/sparsity test** (Whittaker-smoothed, 5000 realizations): 95% CI on St is **±2.81%** for the worst case (N = 5000). Term III carries the highest % error (needs the smoothed derivative). [source] See [[whittaker-smoother]].
- **Experimental validation** (Tsuji & Nagano natural-convection BL, hot-wire + cold-wire): **6–10%** difference between computed and reported `q″_w`; % difference falls with increasing outer limit `y_t/δ_T`, rapidly until `y_t/δ_T ≈ 0.3`. [source]
- Statistical error estimates: `ε_Φ/Φ ~ 0.05/√N`; `ε_{v'φ'}/v'φ' ~ 2/√N`. [source]

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| `Φ` | mean temperature | `Φ` (adopted into canon) |
| `φ'` | fluctuating temperature | `φ'` (adopted into canon) |
| `v'φ'` (overbar) | turbulent wall-normal heat flux | `v'φ'` |
| `u_s` (`u_τ`), `s_w` (`τ_w`) | friction velocity, wall stress | `u_tau`, `τ_w` (OCR of paper's `u_s`,`s_w`) |
| `Pe = U∞δ/α` | Péclet number | `Pe` |
| `Gr_x` | Grashof number | `Gr_x` |
| `δ_T` | thermal BL thickness | `δ_T` |

## Connections

- Thermal analogue of the skin-friction integral method → [[triple-integral-identity]].
- Supports [[wall-heat-flux-experimental]] (Reza's contribution) and links to [[cfd-validation-method]] (same integral-identity family used to test CFD).
- Concepts touched: [[wall-heat-flux]], [[stanton-number]], [[triple-integral-identity]].
- Methods: [[whittaker-smoother]].
- Uses DNS data of Araya–Castillo and Wu–Moin; experiments of Tsuji & Nagano.
