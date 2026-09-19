# Blow-Off Valve: Design Calculations & Geometric Specifications

## 📌 Document Overview
This document outlines the core geometric calculations, bolt pattern coordinate mathematics, and Geometric Dimensioning and Tolerancing (GD&T) specifications for the blow-off valve body. The parameters detailed here define the exact sizing, placement, and spatial relationships required to accurately model and manufacture the component.

---

## 1. Primary Volumetric & Dimensional Parameters

The foundational structure of the blow-off valve is defined by a primary revolve feature and subsequent flange extrusions. 

### Core Revolve Profile (Main Body)
* **Maximum Outer Diameter:** 132 mm
* **Primary Internal Bore Length:** 77 mm
* **Throat Depth:** 56 mm
* **Conical Transition Angles:** 10 degrees (measured from the horizontal axis)
* **Sectional Offsets:** 6 mm wall thickness gaps along the blend and transition curves

### Flange Extrusions
* **Flange Outer Diameter (OD):** 125 mm
* **Flange Thickness ($t$):** 10 mm
* **Symmetry:** Mirrored across the central vertical Right Datum Plane to ensure balanced fluid pressure distribution.

---

## 2. Pitch Circle Diameter (PCD) & Hole Positioning

The mounting interfaces rely on precise hole patterns. The positions of these holes can be calculated using standard Cartesian coordinate transformations based on their Pitch Circle Diameters (PCD).

The general formula for finding the exact $X$ and $Y$ center coordinates of a radially patterned hole is:
$$x_i = R \cos(\theta_i)$$
$$y_i = R \sin(\theta_i)$$
*(Where $R$ is the radius of the PCD, and $\theta_i$ is the angle of the specific hole relative to the origin datum).*

### Pattern 1: M10 Standard Tapped Holes (Primary Flange)
These holes are used for securing the valve to adjoining high-pressure piping assemblies.
* **Hole Specification:** M10 (Standard Metric Thread)
* **PCD:** 110 mm
* **Radius ($R$):** 55 mm
* **Angular Spacing:** 4 holes equally spaced at $90^\circ$ intervals ($360^\circ / 4$).
* **Starting Angle:** Offset $45^\circ$ from the primary axis.

**Coordinate Calculations for M10 Holes:**
* **Hole 1 ($\theta = 45^\circ$):** $$x_1 = 55 \cos(45^\circ) \approx 38.89\text{ mm}$$
  $$y_1 = 55 \sin(45^\circ) \approx 38.89\text{ mm}$$
* **Hole 2 ($\theta = 135^\circ$):** $x_2 \approx -38.89\text{ mm}, y_2 \approx 38.89\text{ mm}$
* **Hole 3 ($\theta = 225^\circ$):** $x_3 \approx -38.89\text{ mm}, y_3 \approx -38.89\text{ mm}$
* **Hole 4 ($\theta = 315^\circ$):** $x_4 \approx 38.89\text{ mm}, y_4 \approx -38.89\text{ mm}$

### Pattern 2: 18mm Clearance Holes (Secondary Mounting)
* **Hole Specification:** $\emptyset$ 18 mm Through-Hole
* **PCD:** 90 mm
* **Radius ($R$):** 45 mm
* **Angular Spacing:** 4 holes equally spaced at $90^\circ$ intervals.
* **Starting Angle:** Offset $45^\circ$ from the primary axis.

---

## 3. Blend Feature Mathematics (Internal Fluid Pathway)

The internal cavity designed to mitigate flow resistance requires blending three distinct cross-sections across specific distances.

| Section | Geometry Type | Key Dimensions | Plane Offset Reference |
| :--- | :--- | :--- | :--- |
| **Section 1** | Segmented Profile | $\emptyset$ 56 mm base, 32 mm chord gap | Origin (0 mm) |
| **Section 2** | Circular Profile | $\emptyset$ 50 mm | $90\text{ mm} - 25\text{ mm} = 65\text{ mm}$ |
| **Section 3** | Circular Profile | $\emptyset$ 50 mm | $90\text{ mm}$ |

* **Section 1 Angular Constraints:** The segmented outer profile uses a $10^\circ$ tangency transition.
* **Section 2 & 3 Quadrant Division:** To ensure the blend maps cleanly without twisting, the $50\text{ mm}$ circles are divided into four equal segments starting at $45^\circ$ offsets.

---

## 4. GD&T and Manufacturing Specifications

Based on the provided 2D engineering drawings, exact tolerances and datums must be maintained during machining.

### Datum Reference Frame
* **Datum A:** Primary center axis of the main bore. Establishes concentricity and radial alignment.
* **Datum B:** Vertical datum plane, establishing the longitudinal centerline of the valve.
* **Datum C:** Horizontal center plane intersecting the bore.

### Key Tolerances & Features
* **Section Views:** * `SECTION A-A`: Details the profile of the core bore and transition angles.
  * `SECTION B-B` & `SECTION C-C`: Detail the flange thicknesses and hole penetrations.
* **Critical Diameters:** $\emptyset 32$, $\emptyset 50$, $\emptyset 56$, $\emptyset 90$.
* **Fillets and Edge Treatment:** * Stress relief radii applied to internal corners: `R4`, `R6`, `R10`.
  * Angular transitions denoted at $45^\circ$ and $90^\circ$ to prevent sharp fluid directional changes.