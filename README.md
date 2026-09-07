# TFM-MQuEA Spectral Analysis of the OECD Inter-Country Input-Output System (1995–2022)
This repository contains the replication code and data processing pipelines for the Master's thesis: "Spectral Analysis of the OECD Inter-Country Input-Output System, 1995–2022" (Master in Quantitative Economic Analysis, UAM). 
The project applies spectral graph theory to the global production network, characterizing its structural vulnerability, community structure, and eigenvector localization across 28 annual cross-sections of the OECD ICIO tables.
**Repository Structure**
data/: Directory for input data (OECD ICIO tables). Note: Raw data files are not included due to size limits.
src/: Python scripts for data processing, spectral calculations, and network analysis.
figures/: Output directory where generated plots and graphs are saved.
requirements.txt: List of dependencies required to run the code.
**Data Source**
The analysis is based on the OECD Inter-Country Input-Output (ICIO) 2025 edition.
To replicate the results, you must download the underlying data manually:

Visit the OECD ICIO database website. https://www.oecd.org/en/data/datasets/inter-country-input-output-tables.html

Download the files for the 1995–2022 period, 2025 version.

Extract the contents and place the raw matrices into the data/ folder.
