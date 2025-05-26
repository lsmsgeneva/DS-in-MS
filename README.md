# DS-in-MS

This repository contains data and scripts for the manuscript:

**"Integrative data science in mass spectrometry: connecting molecular structures with diverse MS behaviours"**

---

## 🔬 Project Overview

This project explores how different ion activation methods—**CID**, **UVPD**, and **EAD**—produce distinct fragmentation profiles for structurally diverse small molecules, with a focus on pesticides. Using cheminformatics, statistical modeling, and quantum chemical calculations, we investigate the link between molecular structure and fragmentation behavior.

A **Google Colab notebook** is provided to:
- Reproduce key results from the manuscript
- Visualize all examined analytes
- Show selected protonation sites
- Demonstrate data loading and modeling

---

## 📁 Repository Contents

This repository contains **three core files**, which are automatically loaded by the Colab notebook:

### `r.feather`
Main tabular dataset containing structural and spectral information for all analytes.

| Column            | Description                                                                 |
|-------------------|-----------------------------------------------------------------------------|
| `Source`          | Internal experiment ID                                                      |
| `name`            | Pesticide name                                                              |
| `Fragmentation mode` | CID, EAD, or UVPD                                                        |
| `method`          | Experimental detail (e.g., CID energy, EAD kinetic energy)                  |
| `spectra`         | MS2 spectra from ProteoWizard, centroided, stored as arrays                |
| `Retention`       | Retention time (min)                                                        |
| `precursor`       | Precursor ion mass                                                          |
| `new_data`        | MS2 spectra extracted using SCIEX converter, stored as arrays              |
| `mol`             | SMILES string of the compound, to be converted to RDKit `mol` objects       |

---

### `mol_prot.txt`
List of atoms (by index) proposed as potential protonation sites, as determined by CREST.

Example:
3-Hydroxycarbofuran , 2 9 7
Acetamiprid , 5 3 9 11 14


These sites are **visualized directly in the Colab notebook** using RDKit.

---

### `MH2+.csv`
Contains thermodynamic and electronic descriptors related to the formation and stability of the **[M+H]²⁺•** radical species.

| Column | Description                                                                 |
|--------|-----------------------------------------------------------------------------|
| `HOMO` | HOMO energy (eV) of the [M+H]⁺                                    |
| `DG`   | Gibbs free energy difference between [M+H]⁺ and [M+H]²⁺• (kcal/mol)           |
| `DE`   | Electronic energy difference between [M+H]⁺ and [M+H]²⁺• (kcal/mol)           |
| `M`    | Molecular mass                                                              |
| `name` | Molecule name                                                               |

---

## ▶️ Getting Started

To explore the data and reproduce the results:

1. Open the [Google Colab notebook](https://colab.research.google.com/) *(this is temporary link!)*  
2. All three files are loaded directly from this repository.  
3. No Google Drive connection is required — data can be saved and downloaded from the session.  
4. Visualizations of molecular structures and protonation sites are rendered with RDKit.

---

## 🧪 Citation

Please cite the manuscript if you use this dataset or code in your work:  
> **[Full citation will be placed here once published]**

---

## 📜 License

This repository is released under an open license for academic use. Please check the `LICENSE` file for details.

---
