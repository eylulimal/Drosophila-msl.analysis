Drosophila MSL RNA-seq Analysis

This repository investigates the dosage compensation mechanism in  *Drosophila melanogaster*, focusing on the role of
MSL2 and MOF proteins in regulating X-chromosome gene expression relative to autosomes.

 ## Project Structure
 
 * "drosophila-msl-rnaseq-analysis.qmd": The main Quarto document containing the complete workflow, exploratory data
 analysis, PCA, and differential expression analysis.
 * "drosophila-msl-rnaseq-analysis.html": The rendered HTML report with all visualizations and results.
 * "data/": Dependency lockfile ensuring full computational reproducibility.
 
  ## Analysis Overview
  
  1. **Data Preprocessing:** Construction of a "SummarizedExperiment" object using gene expression counts, TPM matrices
  and sample metadata.
  2. **Principal Component Analysis (PCA):** Unsupervised dimensionality reduction to evaluate sample clustering and 
  variance across axperimental conditions (control, mof, msl2).
  3. **Dosage Compensation Evaluation:** Assessing the impact of MSL2 and MOF knockdowns on X-linked genes compared 
  to autosomes.
  
   ## Reproducibility
   
   This project uses "renv" for dependency management. To restore the required R environment on your local machine,
   open the project in RStudio and run:
   
   ```R
   renv::restore()
   