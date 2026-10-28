# Phase-field-for-brittle-fracture

**Phase field modelling of brittle fracture using FreeFEM++**

This repository contains a fully documented implementation of a variational **phase-field model for quasi-static and dynamic brittle fracture** using [FreeFEM++](https://freefem.org). The code is written for serial execution and leverages FreeFEM++'s mesh adaptivity, modular finite element framework, and scripting capabilities.

It accompanies the paper:

> _Phase-field modelling of quasi-static and dynamic brittle fracture: A FreeFEM++ implementation_  
> *https://doi.org/10.1016/j.engfracmech.2026.111846*

---

## 📁 Repository Structure

Each example folder contains a working subset of scripts to reproduce the corresponding numerical benchmark described in the paper.
```
Phase-field-for-brittle-fracture/
├── CODE/ # Main simulation scripts (modular .edp files)
├── Examples/ # Example problems from the paper (Section 4.x)
│ ├── 4.1/Single edge notched tension test
│ ├── 4.2/Single edge notched shear test
│ ├── 4.3/L-shape panel test
│ ├── 4.4/Notched plate with holes
│ ├── 4.5/Dynamic crack branching
├── LICENSE # GNU GPL v3.0 license
└── README.md # Project documentation (this file)
```

## ⚙️ Requirements

To run the code, you need:

- [**FreeFEM++**](https://freefem.org) (version 4.9 or newer recommended)  
  Compatible with **Linux**, **macOS**, and **Windows**

> 📌 No external libraries or parallel tools are required.  
> The code runs in **serial** mode.

---

## 🚀 How to Run an Example

1. Choose the example you want to run from the `Examples/` directory (e.g. `Examples/4.2/`)
2. Copy the `.edp` files from that folder into the `CODE/` directory, replacing existing files
3. Create the corresponding folders for data export and VTU files
4. Open a terminal and navigate to the `CODE/` folder
5. Run the main script:

```bash
FreeFem++ sPF.edp
```
---

## 📖 Citation

If you use this code, please cite:

```bibtex
@article{Galvis2026,
  author  = {Galvis, Andres F.},
  title   = {Phase-field modelling of quasi-static and dynamic brittle fracture: A FreeFEM++ implementation},
  journal = {Engineering Fracture Mechanics},
  volume  = {333},
  pages   = {111846},
  year    = {2026},
  doi     = {10.1016/j.engfracmech.2026.111846}
}
```
