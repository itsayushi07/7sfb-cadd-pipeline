# 7sfb-cadd-pipeline

<div align="center">

# 7SFB CADD Pipeline

### AI-Assisted Structure-Based Drug Discovery of SARS-CoV-2 Main Protease (7SFB)

Structure-based computational drug discovery workflow integrating **SwissADME**, **UCSF Chimera**, **DoGSiteScorer**, **ADMETlab 3.0**, **AlphaFold3**, and **PyMOL**.

![Python](https://img.shields.io/badge/Field-Computational%20Biology-black)
![CADD](https://img.shields.io/badge/Workflow-CADD-black)
![Protein](https://img.shields.io/badge/Protein-7SFB-black)
![Status](https://img.shields.io/badge/Status-Completed-success)

</div>

---

## Overview

This repository presents a **structure-based computational drug discovery workflow** performed on the **SARS-CoV-2 Main Protease (Mpro, PDB: 7SFB)** using Computer-Aided Drug Design (CADD) methodologies.

The project integrates **drug-likeness screening**, **protein preparation**, **binding site characterization**, **ADMET profiling**, and **AI-based structural validation** to evaluate ligand suitability and protein structural reliability.

The workflow was designed to simulate a streamlined early-stage **in silico drug discovery pipeline** while applying modern computational biology and structural bioinformatics approaches.

---

## Research Objective

To computationally evaluate selected ligands against **SARS-CoV-2 Main Protease (7SFB)** by integrating:

- Drug-likeness screening
- Protein structure preparation
- Binding pocket prediction
- Pharmacokinetic and toxicity profiling
- AI-driven protein structure validation

---

## Protein Information

| Parameter | Value |
|------------|--------|
| **Protein** | SARS-CoV-2 Main Protease (Mpro / 3CLpro) |
| **PDB ID** | `7SFB` |
| **Experimental Method** | X-Ray Diffraction |
| **Resolution** | `1.90 Å` |
| **Target Relevance** | Viral replication enzyme and antiviral drug target |

---

# Workflow

---

## 1. Drug-Likeness Screening

Ligands were evaluated using **Lipinski’s Rule of Five** through SwissADME to assess oral drug-likeness and pharmacological feasibility.

### Ligands Evaluated

| Compound | PubChem CID |
|----------|-------------|
| Aspirin | 2244 |
| Ibuprofen | 3672 |
| Acetaminophen | 1983 |
| Naproxen | 156391 |
| Diclofenac | 3033 |

### Key Outcome

All five ligands successfully passed **Lipinski’s Rule of Five**, indicating favorable physicochemical properties and potential oral bioavailability.

---

## 2. Protein Preparation

The experimental protein structure (**7SFB**) was prepared using **UCSF Chimera** to generate a docking-ready model.

### Processing Pipeline

- Selection of relevant protein chain
- Removal of water molecules
- Removal of unnecessary heteroatoms
- Hydrogen addition
- Gasteiger charge assignment

### Output

```txt
7SFB_prepared.pdb
```

Prepared structures improve docking reliability by minimizing structural artifacts and improving interaction realism.

---

## 3. Binding Site Prediction

Binding pocket prediction was performed using **DoGSiteScorer** to identify druggable cavities on the protein surface.

### Primary Binding Pocket

| Parameter | Value |
|------------|--------|
| Pocket ID | `P_0` |
| Volume | `642.94 Å³` |
| Surface Area | `776.96 Å²` |
| Druggability Score | `0.75` |

### Key Binding Residues

```txt
THR25
THR26
LEU27
HIS41
VAL42
```

The presence of both hydrophobic and polar residues indicates favorable ligand accommodation and stable intermolecular interactions.

---

## 4. ADMET Profiling

Pharmacokinetic and toxicity predictions were performed using **ADMETlab 3.0**.

### Evaluated Categories

- Absorption
- Distribution
- Metabolism
- Excretion
- Toxicity

### Comparative Findings

- **Aspirin** and **Ibuprofen** demonstrated comparatively balanced ADMET profiles.
- **Acetaminophen** showed efficient clearance but hepatotoxicity considerations.
- **Naproxen** and **Diclofenac** displayed longer half-life and strong plasma protein binding, with elevated toxicity risk.

Critical evaluation parameters included:

```txt
BBB Penetration
hERG Inhibition
Hepatotoxicity (DILI)
CYP Enzyme Interaction
Plasma Protein Binding
```

---

## 5. AlphaFold3 Structure Validation

The protein sequence of **7SFB Chain A** was submitted to **AlphaFold3** for AI-based structure prediction.

The predicted model was structurally aligned against the experimentally prepared protein using **PyMOL**.

### Structural Comparison Metrics

| Metric | Result |
|---------|--------|
| RMSD | `0.616 Å` |
| Structural Agreement | Excellent |
| Atoms Aligned | `1997` |
| Confidence | High |

The predicted structure demonstrated **strong overlap with the experimental structure**, with only minor deviations observed in flexible loop regions.

---

# Key Findings

- All ligands satisfied **Lipinski's Rule of Five**
- Primary binding pocket exhibited **high druggability**
- ADMET profiling highlighted **compound-specific trade-offs**
- AlphaFold3 prediction achieved **excellent structural agreement**
- RMSD of **0.616 Å** demonstrated strong predictive reliability

---

# Repository Structure

```bash
7sfb-cadd-pipeline/
│── README.md
│── LICENSE
│── .gitignore
│
├── data/
│   ├── raw/
│   └── processed/
│
├── structures/
│   ├── experimental/
│   ├── alphafold/
│   └── aligned/
│
├── figures/
│
├── results/
│
└── docs/
```

---

# Tools & Technologies

| Category | Tool |
|----------|------|
| Protein Visualization | PyMOL |
| Protein Preparation | UCSF Chimera |
| Drug-Likeness Screening | SwissADME |
| Binding Site Prediction | DoGSiteScorer |
| ADMET Prediction | ADMETlab 3.0 |
| AI Structure Prediction | AlphaFold3 |

---

## Scientific Relevance

The **SARS-CoV-2 Main Protease (Mpro)** is a critical enzyme involved in viral replication and remains one of the most extensively studied antiviral therapeutic targets.

This repository demonstrates the application of **computational biology, structural bioinformatics, and AI-assisted protein modelling** within a unified early-stage drug discovery workflow.

---

## Author

**Ayushi**  
Computational Biology • Bioinformatics • CADD

---

<div align="center">

### Computational Biology × Structural Bioinformatics × AI

</div>
