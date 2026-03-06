# LIFE750_metagenomics

Project Overview
This repository contains the reproducible bioinformatics workflow and data visualization scripts used to generate our scientific poster for the LIFE750 Advanced Genomic Analysis module.

Background & Dataset Description
This project analyzes a shotgun metagenomic dataset derived from stool samples to compare Western and Korean diet. The primary objective is to evaluate the taxonomic composition and ecological differences between these physical matrices, as well as assess anthropogenic impacts on the microbiome. The raw dataset originates from McInnes et al. (2021).

Repository Structure
1) scripts: Contains executable Bash and R scripts for the pipeline.

2) environment: Contains the Conda environment configuration file to ensure software reproducibility.

Bioinformatics Workflow
1) Quality Control: Raw sequence reads are trimmed and filtered for quality to remove adapters and low-quality bases.

2) Taxonomic Classification: Short sequencing reads are queried against a reference database and assigned taxonomic labels using Kraken 2.

3) Abundance Re-estimation: Bracken is utilized downstream of Kraken 2 to probabilistically re-estimate true taxonomic abundance at the species level.

4) Data Visualization: The resulting abundance profiles are imported into R to generate compositional stacked bar charts, differential heat trees, and beta diversity ordinations.

Instructions for Reproducibility
1) Clone this repository to your local machine or the HPC environment.

2) Recreate the computational environment in the envs/ directory.

3) Execute the bash scripts in the scripts/ directory sequentially to perform quality control, Kraken 2 classification, and Bracken re-estimation.

4) Run the R visualization script to generate the final figures from the Bracken outputs.
