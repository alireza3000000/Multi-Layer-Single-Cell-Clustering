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

---

## Test Dataset

The CITE-seq dataset analyzed in this study is publicly available from 10x Genomics:
- PBMC CITE-seq Dataset (pbmc_10k_protein_v3): https://www.10xgenomics.com/datasets
- PBMC Multiome Dataset: https://www.10xgenomics.com/datasets

The dataset is not redistributed in this repository due to size. Users can download 
it directly from the 10x Genomics website.

---

## Inputs and Outputs

**Input files (required):**
- `rna_norm.npz` — normalized RNA expression matrix (cells × genes)
- `protein_norm.npz` — normalized protein expression matrix (cells × epitopes)
- `glycolysis_score.npy` — glycolysis pathway activity scores per cell
- `oxphos_score.npy` — OXPHOS pathway activity scores per cell

**Output files (generated):**
- `dec_labels.npy` — cluster assignments for each cell (K = 28)
- `dec_latent.npy` — 10-dimensional latent representations
- `dec_metrics.npy` — evaluation metrics: [Silhouette, Calinski-Harabasz, Davies-Bouldin]

---

## Reproducing the Results

1. Install the required packages:
   ```bash
   pip install -r requirements.txt
