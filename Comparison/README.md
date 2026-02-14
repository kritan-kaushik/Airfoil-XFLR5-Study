# Airfoil-XFLR5-Study

## Overview

This repository presents a parametric aerodynamic analysis of multiple airfoil profiles using XFLR5 (XFoil viscous solver), with particular focus on low Reynolds number flight regimes relevant to UAVs, RC aircraft, and small-scale aerodynamic applications.

The study investigates lift, drag, aerodynamic efficiency, pitching moment behavior, and boundary layer transition characteristics across multiple Reynolds numbers.

The objective is to compare aerodynamic performance between commonly used airfoils and identify trends in low-Reynolds-number aerodynamics.

---

## Airfoils Studied

- Clark Y
- E423
- NACA 0012
- NACA 4412

These airfoils were selected to compare:

- Cambered vs symmetric airfoils
- Low-Re optimized profiles vs general-purpose airfoils
- Stability and efficiency tradeoffs

---

## Simulation Methodology

### Solver
- Software: XFLR5 (XFoil viscous analysis)
- Mach number: 0.0
- Ncrit: 9

### Reynolds Numbers
- Re = 50,000
- Re = 100,000
- Re = 200,000

### Angle of Attack Sweep
- Range: -5° to +15°
- Step size: 1°

### Panel Discretization
- ~200 panels per airfoil

---

## Repository Structure
airfoils/
├── clarky/
├── e423/
├── naca0012/
├── naca4412/

comparison/
├── Re50000_*.png
├── Re100000_*.png
├── Re200000_*.png

methodology/
├── simulation_settings.md


Each airfoil directory contains individual performance plots and geometry (.dat) files.

The `comparison` folder contains overlay plots comparing all airfoils at identical Reynolds numbers.

---

## Comparison Metrics

The following aerodynamic comparisons are included:

### 1. Lift Coefficient vs Angle of Attack (CL vs α)

Used to evaluate:

- Lift slope
- Zero-lift angle
- Maximum lift coefficient (CLmax)
- Stall onset behavior

Key observation:

- Cambered airfoils generate positive lift at lower angles of attack compared to symmetric airfoils.

---

### 2. Drag Polar (CL vs CD)

Used to compare aerodynamic efficiency envelopes.

Key observation:

- Low-Reynolds-number optimized airfoils demonstrate improved lift-to-drag performance regions.
- Symmetric airfoils exhibit higher drag penalties at low Reynolds numbers.

---

### 3. Aerodynamic Efficiency (L/D vs α)

Identifies:

- Optimal glide angle
- Peak efficiency region

Key observation:

- High-camber airfoils generally achieve higher peak L/D in low-Re regimes.

---

### 4. Pitching Moment (Cm vs α)

Evaluates:

- Longitudinal stability characteristics
- Effect of camber on aerodynamic moments

Observation:

- Increased camber leads to more negative pitching moment.

---

### 5. Boundary Layer Transition Location

Transition location plots illustrate:

- Laminar-to-turbulent transition movement with increasing angle of attack.
- Relationship between airfoil shape and boundary layer behavior.

---

## Reynolds Number Effects

Across increasing Reynolds numbers:

- Lift capability improves.
- Maximum L/D increases.
- Stall behavior becomes smoother.
- Transition occurs earlier along the chord.

Low Reynolds numbers introduce:

- Increased susceptibility to laminar separation.
- Higher drag sensitivity.
- Performance dependence on airfoil camber.

---

## Key Comparative Insights

- Cambered airfoils outperform symmetric airfoils in low-Re conditions due to improved lift generation.
- The E423 airfoil demonstrates strong efficiency characteristics in low Reynolds regimes.
- NACA 0012 shows lower performance at low Reynolds numbers, highlighting limitations of symmetric airfoils for slow flight applications.
- Clark Y provides balanced performance with stable aerodynamic characteristics.

---

## Limitations

- Analysis is two-dimensional (no 3D wing effects).
- XFoil predictions near stall may include numerical uncertainties.
- Real-world surface roughness and turbulence effects are not modeled.

---

## Future Work

- Experimental validation.
- CFD comparison (RANS or LES).
- 3D wing analysis using XFLR5 wing module.
- Reynolds scaling studies beyond 200k.

---

## Purpose

This project aims to provide a structured comparison of airfoil performance for low-speed aerodynamic design and educational research in UAV and RC aircraft applications.




