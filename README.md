# Stress Analysis of Thick-Walled Boiling Water Reactor
### Ansys Static Structural Simulation + Lame's Theoretical Validation

**Course Project | IIITDM Jabalpur**  
**Tools:** Ansys Mechanical 2026 R1 · Hand Calculations (Lame's Equations) · Python (stress-strain plotting)  
**Team:** Siddharth Jain (23BME061) · Aryan Tak (23BME017)  
**Supervisor:** Dr. Shiv Dayal Patel

---

## Objective

To analyse radial, hoop, and longitudinal stress distribution in a thick-walled cylindrical pressure vessel with hemispherical ends (r/t = 10), and validate Ansys simulation results against Lame's theoretical equations.

---

## Problem Statement

A boiling water reactor with the following geometry was analysed:

| Parameter | Value |
|---|---|
| Inner Radius (Rᵢ) | 175 mm |
| Thickness (t) | 21.875 mm |
| Outer Radius (Rₒ) | 196.875 mm |
| Cylindrical Length | 500 mm |
| Internal Pressure (Pᵢ) | 7.5 MPa |
| End Type | Hemispherical |

---

## Methodology

1. **Theoretical Calculations** — Applied Lame's equations to compute radial, hoop, and longitudinal stress at inner radius, outer radius, and mid-wall interface for both cylindrical and hemispherical sections.

2. **Ansys Simulation** — Modelled the geometry in Ansys Mechanical, applied boundary conditions (fixed support + internal pressure), meshed the body, and extracted stress contour plots for all three stress components.

3. **Validation** — Compared simulation results against theoretical values and computed percentage error at each location.

---

## Key Results

### Cylindrical Section

| Location | Radial Stress (MPa) | Hoop Stress (MPa) | Longitudinal Stress (MPa) |
|---|---|---|---|
| Inner Radius (175 mm) | -7.5 (theory) / -7.42 (sim) | 63.97 / 64.18 | 28.23 / 29.06 |
| Outer Radius (196.8 mm) | 0 / -0.1 | 56.47 / 56.22 | 28.23 / 27.64 |
| Interface (186 mm) | -3.39 / -3.59 | 59.86 / 60.18 | 28.23 / 28.31 |

### Hemispherical End

| | Theoretical | Simulation | Error |
|---|---|---|---|
| Hoop/Longitudinal Stress | 30.29 MPa | 30.1 MPa | -0.63% |

### Percentage Error — Cylindrical Section

| Location | Radial (%) | Hoop (%) | Longitudinal (%) |
|---|---|---|---|
| Inner Radius | -1.07 | 0.33 | 2.94 |
| Outer Radius | ~0 | -0.44 | -2.09 |
| Interface | 5.9 | 0.53 | 0.28 |

> All stress values show agreement within **1–5%**, confirming validity of both the simulation setup and Lame's analytical model.

---

## Key Observations

- Hoop stress is **maximum at the inner surface** and decreases towards the outer wall — consistent with Lame's theory
- Radial stress is **significant and non-negligible** in thick cylinders (r/t < 10), unlike thin cylinder assumption
- Thin cylinder theory **underestimates hoop stress** by ~6% and completely ignores radial stress
- Hemispherical ends show **nearly uniform stress distribution**, confirming their design advantage over flat ends
- Higher error in radial stress at the interface (~5.9%) is attributed to **mesh sensitivity**

---

## Simulation Screenshots

> [Model](https://github.com/sidjain24680-lgtm/Stress-Analysis-Thick-Boiling-Water-Reactor-Ansys-Lames-Theory/blob/main/Images/Model.png)
> [Radial Stress](https://github.com/sidjain24680-lgtm/Stress-Analysis-Thick-Boiling-Water-Reactor-Ansys-Lames-Theory/blob/main/Images/Radial%20Stress.png)
> [Longitudinal Stress](https://github.com/sidjain24680-lgtm/Stress-Analysis-Thick-Boiling-Water-Reactor-Ansys-Lames-Theory/blob/main/Images/Longitudinal%20Stress.png)
> [Hoop Stress](https://github.com/sidjain24680-lgtm/Stress-Analysis-Thick-Boiling-Water-Reactor-Ansys-Lames-Theory/blob/main/Images/Hoop%20Stress.png)

---

## Files in this Repository

```
├── Animation/              # Simulation Video
├── Ansys_Project/          # Ansys Workbench project files (.wbpj)
├── Images/                 # Screen capture of simulation
├── Presentation.pdf        # Full project presentation with theory + results
├── Calculations/           # Hand calculations (Lame's equations, boundary conditions)
└── README.md
```

---

## Concepts Demonstrated

`FEA` `Static Structural Analysis` `Pressure Vessel Design` `Lame's Equations` `Thick Cylinder Theory` `Boundary Conditions` `Mesh Sensitivity` `Stress Validation` `Ansys Mechanical`
