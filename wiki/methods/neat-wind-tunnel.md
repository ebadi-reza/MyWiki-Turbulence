---
title: NEAT wind tunnel & thermal wall plate (apparatus)
type: method
threads:
  - experimental-turbulence-measurement
  - wall-heat-flux-experimental
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# NEAT wind tunnel & thermal wall plate

**What it is.** The **NEAT (Nonequilibrium And Thermal) boundary-layer wind tunnel** — an open-circuit indraft wind tunnel with a feedback-controlled **thermal wall plate** — designed to study heat transfer in nonequilibrium boundary-layer flows ([[2019-biles-jfe]]).

## Tunnel layout

Open-circuit indraft; test section **303×111 mm × 2.75 m** (plexiglass with BK7 glass windows
for IR/laser access). Flow path: freestream resistive heater (PID/SCR, holds freestream T) → PIV **seeding manifold** → turbulence-management screens + honeycomb → **4:1 contraction** → test section (thermal wall plate on floor; superellipse leading edge; top wall angled **0.23°** for ZPG) → **rotor-stator** → diffuser → centrifugal fan. Freestream `U∞ = 1–12 m/s`.

## Thermal wall plate

- **12 independently controlled sections**: aluminum-6061 plate + Kapton film heaters (1.5 W/cm²) + calcium-silicate insulation, in a Delrin frame.
- Three embedded J-thermocouples per section → LabVIEW **PID + SCR** feedback loop.
- Operating range **20–65 °C**; holds `T_w` to **±0.5 °C**; controller time constant ≪ plate thermal time constant.
- Section lengths increase downstream so plate-to-plate convective heat transfer varies <15%.
- Imposes **isothermal, streamwise-gradient, or step** wall-temperature BCs; multiple controllers per plate can hold `T_w` uniform even under strongly 3D flow.

## Rotor-stator (pulsatile-flow generator)

4-hole rotor + 4-slot stator modulate open area → sinusoidal **pulsatile** freestream (non-zero
mean). Rotor 1–100 Hz; amplitude 40–100% via 12 air-bleed slots (after Al-Asmi & Castro).
Removable. The experimental counterpart to the DNS **oscillatory** flow ([[pulsatile-flow]]).

## Control hardware (thesis Appendix A)

Each plate's feedback loop uses an **SCR + NPN-transistor** circuit that isolates the low-current
DAQ from the high-current resistive heaters. The SCR conducts on half the AC cycle (≈60 V DC
effective); the 10 A SCR limit caps the two heaters per plate at ≈7.5 A. Six PCB controller boards
carry 12 active + 6 spare circuits; **Analog Devices AD594** thermocouple amplifiers give 10 mV/°C; everything sits in a Hammond enclosure box with 5 cooling fans. ([[2016-ebadi-thesis]] Appendix A — effectively the controller user manual.) [source]

## Why it matters

- One facility + one measurement suite ([[piv]], [[ir-thermography]], thermocouples) across many
  flow types (ZPG, temperature step, 3D obstacle, pulsatile) — ideal for consistent [[cfd-validation-method|RANS validation]] data.

## Note — distinct apparatus

The NEAT tunnel is **separate** from Reza's [[wind-tunnel-ramp|wind-tunnel ramp]] (unpublished, installed in the UNH Flow Physics Facility tunnel).

See [[notation]].
