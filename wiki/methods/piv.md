---
title: Particle image velocimetry (PIV)
type: method
threads:
  - experimental-turbulence-measurement
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Particle image velocimetry (PIV)

**What it is.** A non-intrusive optical technique for measuring a velocity field: the flow is seeded with small tracer particles, a laser sheet illuminates a plane, and a camera captures two successive images; **cross-correlation** of the particle patterns between images gives the particle displacement, and dividing by the known inter-frame time yields the velocity field.

## As used in Reza's work ([[2019-biles-jfe]])

- **Seeding:** ~1 μm oil droplets from a custom honeycomb seeding manifold (uniform seeding is
  harder in an open-circuit tunnel). See [[neat-wind-tunnel]].
- **Illumination/imaging:** Nd:YLF dual-cavity laser + sheet optics; two 12-bit Photron SA4
  CMOS cameras (1024²) on opposite sides imaging the same plane with **different fields of
  view** — high near-wall resolution + full-BL coverage. Acquired at 3.6 kHz.
- **Profile stitching:** the two camera profiles are combined (Shea et al. 2014) into one spanning the whole boundary layer.
- **Wall shear stress** from the mean PIV profile via the **Mehdi–White skin-friction integral
  method** (the momentum-side sibling of the [[triple-integral-identity]]) — robust to near-wall  noise, no wall-gradient extrapolation needed.

## Procedure detail (thesis Appendix C)

A full step-by-step PIV protocol is documented in [[2016-ebadi-thesis]] Appendix C: DaVis
8.3.1/8.0.6 (the older build is more stable near mask edges), dual HighSpeedStar cameras with
two-camera independent 2D calibration, laser at 14 A for acquisition, and an **AOI of 448×1024 px recorded at 7.2 kHz** (full-frame 1024² maxes at 3.6 kHz — smaller AOI buys frame rate). Wall location is estimated from the calibrated image; periodic tunnel oil cleanup is required.

## Why it matters

- Gives full 2D velocity fields (mean + fluctuations, Reynolds stresses) for wall-bounded flows.
- Combined with simultaneous temperature measurement, supports thermal-transport studies.

## In Reza's threads

- [[experimental-turbulence-measurement]] (core), feeding [[wall-heat-flux-experimental]] and
  [[cfd-validation-method]]. Anisotropy structure can be characterized via the
  [[anisotropy-invariant-map]].

See [[notation]].
