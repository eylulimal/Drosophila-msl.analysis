Project Overview
This project investigates the role of MSL2 and MOF in the dosage compensation mechanism of Drosophila malanogaster.
By analyzing RNA-seq data from S2 cells, we evaluate the impact of these two gene knockdowns on X-chromosome gene 
expression relative to the autosomes.

Analysis Summary
The study focuses on calculating the average log2 fold change of genes on the X chromosome compared to autosomes. Our
findings demonstrate the cooperative role of MSL2 and MOF in regulating X-linked gene expression.

Key Results
MSL2 RNAi effect: Approximately -0.40 (relative to autosomes).

MOF RNAi effect: Approximately -0.42 (relative to autosomes).

Difference: The difference between the two gene knockdowns is 0.024, indicating a comparable impact on dosage compensation.

Repository Contents

drosophila-msl-rnaseq-analysis.qmd: Main analysis report(Quarto document).

data/: Contains the processed datasets (Summarized_experiment.rds) used for the analysis.

01_build_summarized_experiment.R: Script for data preparation.
   