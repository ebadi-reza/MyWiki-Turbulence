---
title: Stanton number
type: concept
threads:
  - wall-heat-flux-experimental
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Stanton number

**Definition.** The Stanton number is the non-dimensional wall heat flux, measuring heat transferred to the wall relative to the thermal capacity of the freestream flow:

$$
St \equiv \frac{q''_w}{\rho\, C_p\, U_\infty (\Phi_w - \Phi_\infty)}
$$

where `q″_w` is [[wall-heat-flux]], `ρ` density, `C_p` specific heat, `U∞` freestream velocity, `Φ_w` wall temperature, `Φ∞` freestream temperature.

## Three-term decomposition (Ebadi et al. 2015)

The [[triple-integral-identity]] applied to the energy equation writes `St` as three additive contributions (Eq. 4 of [[2015-ebadi-ijhmt]]):

- **Term I** — mean-temperature contribution; scales as `Pe⁻¹` (shrinks at high Péclet).
- **Term II** — turbulent-heat-flux contribution; **dominant** (~60–78%). ([[2015-ebadi-ijhmt|source]])
- **Term III** — gradient of the total (molecular + turbulent) heat flux; ~9–35%. ([[2015-ebadi-ijhmt|source]])

This ties the wall heat transfer to the mean-flow dynamics.

## Related numbers

- Nusselt `Nu`, Péclet `Pe = U∞δ/α = Re·Pr`, Prandtl `Pr`.
- `Pe` governs the relative weight of the three terms above.

## Colburn analogy (isothermal ZPG)

A common engineering estimate of `St` from skin friction, used for inner-normalizing temperature profiles in [[2019-biles-jfe]]:

$$
St_T = Pr^{-2/3}\left(\frac{u_\tau}{U_\infty}\right)^2
$$

Downstream of a wall-temperature step (unheated starting length `x_T`), the modified Stanton number follows `St(x) = St_T[1 − (x_T/x)^{9/10}]^{−1/9}` (Reynolds–Kays). [source:[[2019-biles-jfe]]]
This is a [[reynolds-analogy|transport-analogy]] estimate — contrast the analogy-free [[triple-integral-identity]] wall-heat-flux method.

## Where it appears in Reza's threads

- [[wall-heat-flux-experimental]] — reported as the primary non-dimensional output of the integral method.

See [[notation]].
