# Multi-Layer Single-Cell Integration with Deep Embedded Clustering Reveals Metabolic Heterogeneity in Peripheral Blood Mononuclear Cells

This repository contains a **minimal reproducible version** of the analysis code 
supporting the manuscript:

**Title:** Multi-Layer Single-Cell Integration with Deep Embedded Clustering Reveals 
Metabolic Heterogeneity in Peripheral Blood Mononuclear Cells

**Journal:** Bioinformatics (under review)

---

## Note

This is a **minimal reproducible version** of the analysis pipeline. It illustrates 
the core steps: multi-layer signature construction, dimensionality reduction, 
autoencoder-based deep embedded clustering, and clustering evaluation.

The full implementation, including all preprocessing steps and extended analyses, 
is described in the Methods section of the manuscript.

---

## Contents

- `analysis.py` — minimal reproducible pipeline
- `best_results.csv` — clustering evaluation results
- `cluster_summary.csv` — summary of identified clusters
- `comparison_blood.csv` — comparative analysis results
- `data/` — input data directory

---

## Requirements

- Python 3.x
- numpy
- scipy
- torch
- scikit-learn

Install:

```bash
pip install numpy scipy torch scikit-learn
