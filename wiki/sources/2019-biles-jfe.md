---
title: Biles, Ebadi, Allard & White (2019) — The Design and Validation of a Thermal Boundary Layer Wall Plate
type: source
threads:
  - experimental-turbulence-measurement
  - wall-heat-flux-experimental
  - non-equilibrium-pulsatile-flow
  - cfd-validation-method
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Biles, Ebadi, Allard & White (2019) — Thermal boundary layer wall plate & NEAT wind tunnel

**Full citation.** D. Biles, A. Ebadi, M.P. Allard, C.M. White, "The Design and Validation of a Thermal Boundary Layer Wall Plate," *ASME J. Fluids Engineering* **141** (2019) 121403. doi:10.1115/1.4043773. (Reza = second author; UNH.)

## One-paragraph summary

Describes and validates the **NEAT (nonequilibrium and thermal) boundary-layer wind tunnel** and its centerpiece, a **feedback-controlled, sectioned thermal wall plate**, designed to study heat transfer in **nonequilibrium** boundary-layer flows. The wall plate can impose a variety of thermal boundary conditions (isothermal, streamwise gradient, temperature step) or hold the wall temperature fixed even when the flow above is unsteady and strongly three-dimensional.
Validated in three cases: ZPG isothermal wall, ZPG with a sharp wall-temperature step (unheated starting length), and flow around a wall-mounted hemisphere. Purpose: generate robust experimental data to develop and validate RANS heat-transfer models for nonequilibrium flows (a direct experimental complement to [[cfd-validation-method]]). See [[neat-wind-tunnel]].

## The apparatus

- **NEAT wind tunnel:** open-circuit indraft; test section 303×111 mm × 2.75 m (plexiglass +BK7 windows for IR/laser); freestream resistive heater (PID/SCR), PIV seeding manifold, turbulence-management screens + honeycomb, 4:1 contraction; superellipse leading edge;
  top wall angled 0.23° for ZPG; rotor-stator downstream; diffuser + centrifugal fan. `U∞ = 1–12 m/s`. [source]
- **Thermal wall plate:** 12 independently controlled sections (aluminum 6061 + Kapton film
  heaters, 1.5 W/cm²; calcium-silicate insulation; Delrin frame). Three embedded J thermocouples per section drive a LabVIEW PID + SCR feedback loop. Range 20–65 °C; holds `T_w` to **±0.5 °C**. Plate lengths grow downstream so plate-to-plate convective heat transfer varies <15%. 3 mm trip rod fixes transition. [source]
- **Rotor-stator assembly:** produces a sinusoidal **pulsatile** freestream (4-hole rotor + 4-slot
  stator; 1–100 Hz; amplitude adjustable 40–100% via 12 air-bleed slots; after Al-Asmi & Castro). Note **pulsatile = non-zero mean** — the experimental counterpart to the DNS **oscillatory** ([[non-equilibrium-pulsatile-flow|OCF]]) work. See [[pulsatile-flow]]. [source]

## Measurement methods

- **PIV** — dual 12-bit Photron SA4 CMOS cameras (opposite sides, different FOVs), 3.6 kHz,
  Nd:YLF laser, 1 μm oil tracers; profiles stitched (Shea et al.). `τ_w` from PIV via the **Mehdi–White skin-friction integral method** (the momentum sibling of the  [[triple-integral-identity]]). See [[piv]]. [source]
- **IR thermography** — FLIR SC645 (7.5–13 μm, 640×480, ±2%) for wall-temperature fields. See
  [[ir-thermography]]. [source]
- **Fine-wire thermocouple** (0.65 mm) on a Velmex traverse (5 μm step); cathetometer (±64 μm) for wall position. [source]

## Key physics / results (cited to this paper)

- **Thermal law of the wall:** `Θ⁺ = (1/κ_T) ln y⁺ + C₂(Pr)` with `Θ = T_w − T(y)`, friction
  temperature `T_τ = q″_w/(ρ c_p u_τ)`, and `κ_T ≈ 0.48` (varies by flow). Companion to the
  velocity [[log-law]] `u⁺=(1/κ)ln y⁺+C₁` (κ≈0.4, C₁≈5). [source]
- **Central motivation:** the **temperature** law-of-the-wall is *much more sensitive* to nonequilibrium / pressure-gradient perturbations than the velocity one — even though pressure gradient does not appear in the temperature transport equation. Equilibrium-based wall functions may therefore fail badly for heat transfer in strong nonequilibrium flows. [source]
- **Colburn analogy** for the isothermal ZPG inner normalization: `St_T = q″_w/[ρ c_p U∞(T_w−T∞)] = Pr^{−2/3}(u_τ/U∞)²`. See [[stanton-number]]. [source]
- **Temperature-step case:** heat transfer downstream of the step follows
  `St(x) = St_T[1−(x_T/x)^{9/10}]^{−1/9}` (Reynolds/Kays); thermal jump ≈0.45 °C/mm. [source]
- **Hemisphere case:** wake vorticity (necklace vortex + loops) drives strong 3D wall-heat-
  transfer variation; multi-controller scheme holds `T_w` uniform within IR uncertainty. [source]
- ZPG validation `Re_θ ≈ 568–2415`; velocity/temperature agree with DNS (Araya–Castillo;
  Wu–Moin); temperature behaves as a passive scalar. [source]

## Notation mapping (this paper vs wiki canon)

| This paper | Meaning | Wiki canon ([[notation]]) |
|---|---|---|
| x, **y**, z | streamwise, **wall-normal**, spanwise | matches canon ✅ |
| `κ`, `C₁` | velocity log-law slope const, intercept | `κ`, `B` |
| `κ_T`, `C₂(Pr)` | **thermal** log-law slope const (≈0.48), intercept | `κ_T` (cf. `κ_θ`; see [[log-law]]) |
| `Θ = T_w−T(y)` | temperature deficit | canon `Φ` is mean temperature |
| `T_τ` (`Ts`) | friction temperature `q″_w/(ρc_p u_τ)` | `θ_τ` |
| `St_T`, `St(x)` | Stanton (Colburn), nonequilibrium modified | `St` |
| `u_τ` (`u_s`) | friction velocity | `u_tau` |

## Connections

- Primary thread: [[experimental-turbulence-measurement]] (facility + measurement techniques).
- [[wall-heat-flux-experimental]] — the thermal wall plate enables direct thermal-BL / wall-heat-
  flux experiments; uses the Mehdi–White integral for `τ_w`.
- [[non-equilibrium-pulsatile-flow]] — rotor-stator generates the experimental pulsatile flow.
- [[cfd-validation-method]] — facility built to produce RANS-validation data for nonequilibrium
  thermal flows.
- Concepts/methods: [[log-law]], [[stanton-number]], [[reynolds-analogy]], [[piv]],  [[ir-thermography]], [[neat-wind-tunnel]].
- Distinct from the (unpublished) [[wind-tunnel-ramp]] apparatus.
