# Airfoil Comparison Analysis

This section presents direct aerodynamic comparisons between four airfoil profiles:

- Clark Y
- E423
- NACA 0012
- NACA 4412

All comparisons are performed under identical simulation conditions using XFLR5 (XFoil viscous solver).

---

## Simulation Conditions

- Reynolds numbers:
  - Re = 50,000
  - Re = 100,000
  - Re = 200,000

- Angle of attack:
  - Range: -5° to +15°
  - Step size: 1°

- Mach number: 0.0  
- Ncrit: 9

---

## Comparison Plots

Each Reynolds number contains overlay plots comparing all airfoils simultaneously.

---

### 1. Lift vs Drag (CL vs CD)

Purpose:

- Evaluate aerodynamic efficiency envelope.
- Identify which airfoil generates higher lift for lower drag.

Observations:

- Cambered airfoils (Clark Y, NACA4412, E423) generally achieve higher lift compared to symmetric NACA0012.
- E423 demonstrates strong lift performance at low Reynolds numbers.
- NACA0012 shows higher drag for equivalent lift, typical for symmetric airfoils in low-Re regimes.

---

### 2. Lift Curve (CL vs Alpha)

Purpose:

- Compare lift generation capability.
- Observe stall characteristics.

Observations:

- Cambered airfoils produce positive lift at zero angle of attack.
- NACA0012 requires higher angle of attack to generate equivalent lift.
- Increasing Reynolds number increases lift slope and delays stall onset.

---

### 3. Pitching Moment (Cm vs Alpha)

Purpose:

- Evaluate aerodynamic stability characteristics.

Observations:

- Cambered airfoils exhibit more negative pitching moment.
- Symmetric airfoil (NACA0012) shows near-neutral pitching behavior.

---

### 4. Aerodynamic Efficiency (L/D vs Alpha)

Purpose:

- Identify optimal operating angle of attack.

Observations:

- Peak efficiency increases with Reynolds number.
- E423 and Clark Y show strong performance in low-Re flight regimes.
- NACA0012 has reduced efficiency due to higher drag.

---

### 5. Boundary Layer Transition (Xtr Top)

Purpose:

- Study laminar-to-turbulent transition location.

Observations:

- Transition location shifts downstream with increasing Reynolds number.
- Low-Re optimized airfoils maintain longer laminar regions.

---

## Key Insights

- Camber significantly improves low-Re performance.
- Low-Re optimized airfoils outperform symmetric designs in slow flight.
- Reynolds number strongly influences efficiency and stall characteristics.
- E423 shows high lift potential but with strong pitching moment effects.

---

## Notes

XFoil predictions near stall should be interpreted cautiously due to model limitations.
