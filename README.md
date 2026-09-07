# Spectral Analysis of the OECD Inter-Country Input-Output System, 1995–2022

Code for my Master's thesis (TFM), *Master in Quantitative Economic Analysis*, Universidad Autónoma de Madrid.

**Author:** Adrián Fernández Ciruelos · **Supervisor:** Sara Cuenda Cuenda

We characterise the structural stability and systemic vulnerability of the global production network
through the full eigenstructure of the Leontief technical coefficients matrix, across 28 annual
cross-sections (1995–2022) of the OECD Inter-Country Input-Output (ICIO) tables covering 85 countries
and 50 sectors.

## What's here

- [`TFM_Adrian_LIMPIO.ipynb`](./TFM_Adrian_LIMPIO.ipynb) — full analysis pipeline, already executed, organised to mirror Section 4 (Methodology) of the thesis.
- [`figures/`](./figures) — every figure cited in the thesis, generated directly by the notebook. File names match the `\includegraphics{figures/...}` calls in the LaTeX source one-to-one.
- `requirements.txt` — Python dependencies.

## Data

This repository does **not** redistribute the OECD ICIO tables (licensing). To reproduce:

1. Download the 2025 edition of the Inter-Country Input-Output tables from the [OECD] (https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html) (free of charge).
2. Place the yearly files in `data/`, named `ICIO2025_{year}.csv` (e.g. `ICIO2025_1995.csv`, ..., `ICIO2025_2022.csv`).
3. Update `DATA_DIR` in Section 0 of the notebook to point to that folder.

## Reproducing

```bash
pip install -r requirements.txt
jupyter notebook TFM_Adrian_reorganizado_LIMPIO.ipynb
```

Run top to bottom; each section writes its figures to `figures/`.

## Structure of the notebook

Mirrors Section 4 of the thesis:

| Section | Content | Thesis reference |
|---|---|---|
| 1 | Data loading, construction of A | §4.1 |
| 2 | Leontief viability | §4.2, §5.1 |
| 3 | Spectral radius ρ(A) | §4.2–4.3, §5.2 |
| 4 | Stochastic perturbation sensitivity | §4.5, §5.3 |
| 5 / 5b | Domestic–international decomposition; first-order perturbation (Ψc, δv_c) | §4.8, §5.4–5.5 |
| 6 | RMT universality breakdown | §4.3, §5.4 |
| 7 | Shapiro–Wilk normality test | §4.4, §5.13 |
| 8 | Pseudo-degeneracy M(t), IPR localisation | §4.6–4.7, §5.6 |
| 9 | Sign structure of secondary eigenvectors | §4.7, §5.7 |
| 10 | Centrality (eigenvector, node strength, Katz–Bonacich) | §4.9, §5.8 |
| 11 | Buyer/seller similarity in GVCs | §4.12, §5.9 |
| 12 | Community detection (Louvain/Leiden) | §4.10, §5.10 |
| 13 | Country-level Laplacian / Fiedler value | §4.11, §5.11 |
| 14 | Fragility–regionalisation correlation, Granger test, robustness | §4.13, §5.12–5.13 |
| 15 | Appendix / abstract exports | — |



## Citation

If you use this code, please cite:

> Fernández Ciruelos, A. (2026). *Spectral Analysis of the OECD Inter-Country Input-Output System,
> 1995–2022*. Master's thesis, Universidad Autónoma de Madrid.

## License

Code released under the MIT License. The ICIO dataset itself is © OECD and subject to its own terms of use.
