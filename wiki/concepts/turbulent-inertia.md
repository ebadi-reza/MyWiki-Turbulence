---
title: Turbulent inertia
type: concept
threads:
  - high-Re-analytical-modeling
  - non-equilibrium-pulsatile-flow
status: draft
created: 2026-09-03
updated: 2026-09-08
---

# Turbulent inertia

**Definition.** The wall-normal gradient of the Reynolds shear stress appearing in the mean momentum equation:

$$
\text{TI} \equiv \frac{\partial(-\overline{u'v'})}{\partial y}
$$

It represents the net mean force per unit mass exerted by turbulent motions and is one of the leading terms in the [[four-layer-structure|mean momentum balance]]. Where TI acts as a **source** it accelerates the mean flow; where it acts as a **sink** it decelerates it.

## Source-like and sink-like regions

Viewed as a force in the mean momentum balance, TI has **source-like** (positive, accelerating) and **sink-like** (negative, decelerating) regions, and integrates to zero across the layer:

$$
\int_0^{h^+}\frac{\partial\langle -u'v'\rangle^+}{\partial y^+}\,dy^+ = 0
$$

In **steady** turbulent channel/ZPG flow there is a single near-wall **momentum source** (large, wallward of the peak Reynolds stress) and a single **momentum sink** (weaker, from the peak out to the centreline); net action transports momentum from the outer sink region to the inner source region. [source: [[2019-ebadi-jfm]]]

### Centreline momentum source (unique to OCF)

In oscillatory channel flow a **second momentum source appears near the channel centreline** during acceleration — the "centreline momentum source", alongside the usual "wall momentum source" (the negative region between them being the **"interior momentum sink"**) [[2019-ebadi-jfm]], [[2016-ebadi-thesis]]. When it is of leading order, TI redistributes momentum from the interior to **both** the near-wall and centreline regions. The phase at which the centreline source loses leading-order importance (<10% of the wall source) nearly coincides with the emergence of the [[log-law|log region]] and the [[four-layer-structure]]. [source]

### Quadrant-analysis mechanism

The redistribution is explained by quadrant analysis of `(u',v')` ([[2016-ebadi-thesis]] Ch. 5): Q1 (`u'>0,v'>0`) outward interactions, Q2 (`u'<0,v'>0`) ejections, Q3 (`u'<0,v'<0`) inward interactions, Q4 (`u'>0,v'<0`) sweeps. In canonical flow **ejections + sweeps** (`u'v'<0`) dominate and coincide with the TI source/sink. In some phases of reciprocating flow there are regions of **`u'v'>0`** (Q1/Q3 events), spatially coincident with the interior sink and centreline source — the "outward/inward interactions" that shuttle momentum between them. [source]

## Why it matters

- A central quantity in the term-balance (Wei et al.) view of wall turbulence — its sign and magnitude define the layer structure.
- In Reza's reciprocating-flow work ([[2016-ebadi-ictam]], [[2019-ebadi-jfm]]), the
  explosive growth and wall-normal rearrangement of turbulent inertia — plus the fading of the centreline momentum source — drives the emergence of the [[internal-shear-layer]] and the four-layer structure during transition. [source]

## Where it appears in Reza's threads

- [[non-equilibrium-pulsatile-flow]] — mechanistic driver of transition.
- [[high-Re-analytical-modeling]] — key term in the analytical MMB framework.

See [[notation]].
