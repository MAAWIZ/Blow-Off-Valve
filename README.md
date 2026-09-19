# Blow-Off-Valve
Designing Blow-Off Valve in PTC Creo  
# Complex Blow-Off Valve Body: 3D CAD Design & GD&T

## 📌 Project Overview
This repository contains the complete 3D computer-aided design (CAD) models, detailed manufacturing drawings, and technical documentation for a complex blow-off valve body. In high-performance fluid and pneumatic systems, a blow-off valve is critical for regulating pressure and preventing compressor surge. 

This project demonstrates advanced solid modeling techniques, specifically focusing on multi-section blending and parametric feature generation, alongside a rigorous application of Geometric Dimensioning and Tolerancing (GD&T) standards required for precision manufacturing.

## 🎥 Project Demonstration

### CAD Mechanism & Geometry Animation
![Blow Off Valve Animation](Blow_Off_Valve_GIF.jpg)
*Caption: Animated 3D view of the completed blow-off valve body, highlighting the internal flow geometry and external mounting flanges.*


## ⚙️ Advanced Design Methodology
The 3D modeling process for this part was executed in PTC Creo Parametric, utilizing a structured, feature-based workflow to ensure geometric accuracy and design intent:

* **Primary Base Generation:** The foundational geometry of the valve body was established using a precise revolve feature along the central axis, capturing the core cylindrical and conical profiles.
* **Complex Internal Fluid Pathways:** To optimize fluid dynamics and minimize flow resistance, the internal cavity was constructed using an advanced blend feature. This required drafting three separate, precisely constrained cross-sectional sketches across parallel datum planes and blending them seamlessly to create a smooth, continuous internal surface.
* **Flange Extrusion & Mirroring:** Symmetrical 125mm mounting flanges were extruded on both ends of the valve body. To maintain parametric efficiency, symmetry was utilized through mirroring features across the primary datum planes.
* **Precision Hole Patterning:** Secure assembly mounting is facilitated by accurately positioned hole patterns. This includes M10 tapped standard holes configured on a 110mm Pitch Circle Diameter (PCD) and 18mm clearance holes on a 90mm PCD. The hole features were patterned radially using an axis pattern strategy to ensure perfect angular distribution (45-degree and 90-degree offsets).
* **Filleting and Edge Treatment:** Strategic rounds and fillets (ranging from 4mm to 10mm radii) were applied to all critical internal and external edges to reduce stress concentrations and improve castability.

## 📐 Manufacturing Drawings & GD&T
Translating a 3D model into a physical part requires exact manufacturing instructions. The attached engineering drawing provides all necessary multi-view orthographic projections (Front, Top, Right, and detailed Section Views) to fully define the part geometry.

The drawings incorporate strict Geometric Dimensioning and Tolerancing (GD&T) to communicate allowable variations in form and scale, including:
* Clear datum reference frameworks (Datums A, B, and C) for inspection and machining setups.
* Positional tolerances for the PCD mounting holes to guarantee mating with adjoining pipe assemblies.
* Specific surface finish requirements and diametric tolerances critical for the valve's sealing components.


## 🚀 Future Scope: Finite Element Analysis (FEA)
Future iterations of this repository will focus on structural and thermal validation. The native CAD geometry will be prepared in SpaceClaim and imported into Ansys Student to perform:
* **Transient Thermal Analysis:** To evaluate heat flux and thermal convection gradients across the titanium/steel alloy body during extreme operating conditions.
* **Static Structural Simulation:** Utilizing patch-independent meshing techniques to analyze stress distribution, deformation, and high-stress concentrations around the flanged joints under maximum internal pressure.

## 🛠️ Software & Tools Utilized
* **3D Modeling & Drafting:** PTC Creo Parametric
* **Geometry Preparation (Upcoming):** SpaceClaim
* **Simulation (Upcoming):** Ansys Student
* **Documentation:** Markdown

## 📂 Repository Structure
* `/CAD_Models/` - Contains the native `.prt` part files and associated backup iterations.
* `/Drawings/` - Contains `Blow_Off_Valve_GD&T.pdf` with the fully dimensioned manufacturing views.
* `/Simulation_Data/` - *(Placeholder)* Will contain future Ansys mesh configurations and result sets.
* `README.md` - Primary project documentation.

## 👨‍💻 Author
**Mohammad Maawiz**
