# Multivariate Analysis of Resource Interdependencies in HPC Clusters using R-Vine Copulas

This repository contains the R implementation used in the paper:

> **Multivariate Analysis of Resource Interdependencies in HPC Clusters using R-Vine Copulas**

The project investigates dependency structures among computational resources in High-Performance Computing (HPC) systems using Regular Vine (R-Vine) copulas. The analysis is based on SLURM accounting logs collected from the Kabré supercomputer at CeNAT, Costa Rica.

---

## Repository Structure

```
.
├── R Code/
│   └── copula.Rmd          # Complete analysis pipeline
├── Data/
│   └── sacct.csv           # Input dataset (not included)
├── Figures/                # Generated figures
├── README.md
└── LICENSE
```

---

## Features

The R workflow includes:

- Data preprocessing and cleaning of SLURM accounting logs.
- Memory unit conversion and normalization.
- Exploratory statistical analysis.
- Distribution summaries by HPC partition.
- Kernel density estimation.
- Marginal distribution comparison.
- Automatic construction of R-Vine copula models.
- Bivariate copula selection using BIC.
- Multivariate dependence modeling.
- Empirical density visualization.
- Vine tree visualization.
- Copula contour plots.
- Automatic generation of publication-quality PDF figures. :contentReference[oaicite:2]{index=2} :contentReference[oaicite:3]{index=3}

---

## HPC Partitions

The analysis considers the three compute partitions of the Kabré supercomputer:

- Dribe
- Kurá
- Nukwa

Jobs are also separated into:

- Serial jobs
- Parallel jobs :contentReference[oaicite:4]{index=4}

---

## Main Variables

- **CPUTimeRAW**
- **ReqMem**
- **ConsumedEnergyRaw**
- **ReqCPUS** :contentReference[oaicite:5]{index=5}

---

## Required R Packages

```r
VineCopula
copula
fitdistrplus
GGally
ggplot2
dplyr
patchwork
knitr
scales
```

---

## Running the Analysis

1. Place the SLURM accounting dataset (`sacct.csv`) inside the `Data/` directory (or modify the path in the script).
2. Open the R Markdown file located in `R Code/`.
3. Run the complete document.

The script automatically:

- preprocesses the data,
- fits the copula models,
- produces summary tables,
- generates all figures,
- exports publication-ready PDF graphics. :contentReference[oaicite:6]{index=6} :contentReference[oaicite:7]{index=7}

---

## Output

The pipeline generates figures such as:

- Marginal density comparisons
- Boxplots
- Empirical dependence heatmaps
- Vine tree structures
- Copula contour plots
- Summary tables for the selected copula families :contentReference[oaicite:8]{index=8} :contentReference[oaicite:9]{index=9} :contentReference[oaicite:10]{index=10} :contentReference[oaicite:11]{index=11}

---

## Citation

If you use this repository, please cite:

**Dylan Benavides**

*Multivariate Analysis of Resource Interdependencies in HPC Clusters using R-Vine Copulas.*

---

## License

MIT License
