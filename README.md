# Airfoil-XFLR5-Study

## Overview

This repository presents a comparative aerodynamic analysis of multiple airfoil profiles using XFLR5 (XFoil viscous solver). The focus is on low Reynolds number aerodynamics relevant to UAVs, RC aircraft, and small-scale flight applications.

The study evaluates aerodynamic performance through direct comparison of lift, drag, efficiency, pitching moment behavior, and boundary layer transition characteristics across multiple Reynolds numbers.

---

## Airfoils Studied

- Clark Y
- E423
- NACA 0012 (symmetric airfoil)
- NACA 4412 (cambered airfoil)

These airfoils were selected to compare cambered vs symmetric performance and evaluate low-Re optimized geometries.

---

## Simulation Methodology

Software:
- XFLR5 (XFoil viscous analysis)

Parameters:

- Mach number: 0.0
- Ncrit: 9
- Panel count: ~200

Reynolds numbers:

- Re = 50,000
- Re = 100,000
- Re = 200,000

Angle of attack:

- -5° to +15°
- Step size: 1°

---

## Comparison Plots

The repository includes overlay comparisons for each Reynolds number.

### CL vs Alpha (Lift Curve)

Purpose:

- Compare lift generation capability.
- Observe stall behavior and lift slope.

Observations:

- Cambered airfoils generate positive lift at lower angles of attack.
- Symmetric NACA0012 requires higher angle for equivalent lift.

---

### CL vs CD (Drag Polar)

Purpose:

- Evaluate aerodynamic efficiency envelope.

Observations:

- Cambered airfoils show improved lift-to-drag performance.
- NACA0012 shows higher drag penalties in low-Re regimes.

---

### L/D vs Alpha (Efficiency)

Purpose:

- Identify optimal operating angle.
- Compare glide performance.

Observations:

- Efficiency increases with Reynolds number.
- E423 and Clark Y demonstrate strong low-Re efficiency.

---

### Cm vs Alpha (Pitching Moment)

Purpose:

- Evaluate stability characteristics.

Observations:

- Cambered airfoils exhibit more negative pitching moment.

---

### Transition Location

Purpose:

- Observe boundary layer behavior and laminar transition.

---

## Comparison Images

### Reynolds Number = 50,000

![Re50000 Comparison](comparison/Re50000.png)

### Reynolds Number = 100,000

![Re100000 Comparison](comparison/Re100000.png)

### Reynolds Number = 200,000

![Re200000 Comparison](comparison/Re200000.png)

---

## Key Aerodynamic Findings

- Cambered airfoils outperform symmetric airfoils at low Reynolds numbers due to improved lift generation and reduced separation sensitivity.
- E423 demonstrates strong aerodynamic efficiency and higher lift capability, indicating suitability for low-speed applications.
- Clark Y provides balanced performance with stable aerodynamic characteristics.
- NACA0012 exhibits reduced efficiency due to symmetric geometry, resulting in higher drag at equivalent lift.
- Increasing Reynolds number improves aerodynamic efficiency, lift capability, and stall behavior.

---

## Summary Comparison Table

| Airfoil | Best L/D (Approx) | CLmax Trend | Comments |
|---|---|---|---|
| Clark Y | High | Moderate-High | Stable and balanced performance |
| E423 | Very High | High | Optimized for low Reynolds flight |
| NACA 0012 | Lower | Moderate | Symmetric; higher drag at low Re |
| NACA 4412 | High | High | Strong lift and efficiency |

---

## Notation

- CL — Lift coefficient
- CD — Drag coefficient
- Cm — Pitching moment coefficient
- α — Angle of attack (degrees)
- L/D — Lift-to-drag ratio

---

## Limitations

- Analysis is two-dimensional.
- XFoil predictions near stall contain uncertainty.
- Surface roughness and real turbulence effects not included.

---

## Future Work

- CFD validation (RANS analysis)
- Experimental testing
- 3D wing modeling

---

## Repository Structure

```
airfoils/
├── clarky/
├── e423/
├── naca0012/
├── naca4412/

comparison/
├── Re50000.png
├── Re100000.png
├── Re200000.png

methodology/
├── simulation_settings.md
```

Each airfoil directory contains individual performance plots and geometry (.dat) files.

The comparison folder contains overlay plots comparing all airfoils at identical Reynolds numbers.

