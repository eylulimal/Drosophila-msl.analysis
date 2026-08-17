# Project: Chromosome-Level Effects of MSL Knockdown in Drosophila S2 RNA-seq Data

## Background

In male *Drosophila melanogaster*, dosage compensation increases expression from the single X chromosome. This process depends on the MSL complex. In this project, you will analyze RNA-seq data from Drosophila S2 cells in which two MSL-complex components were depleted by RNAi: `msl2` and `mof`.

You will receive processed data tables. You do not need to download FASTQ files or perform read alignment.

## Dataset

The data come from GEO series GSE16344, "Expression in Aneuploid Drosophila S2 Cells".

We will use the following RNA-seq samples:

| GEO sample | Description |
|---|---|
| GSM410195 | Drosophila-S2-RNAseq1 |
| GSM410196 | Drosophila-S2-RNAseq2 |
| GSM410197 | Drosophila-S2-msl2RNAi-RNAseq1 |
| GSM410198 | Drosophila-S2-msl2RNAi-RNAseq2 |
| GSM410199 | Drosophila-S2-mofRNAi-RNAseq1 |
| GSM410200 | Drosophila-S2-mofRNAi-RNAseq2 |

These samples represent:

- control S2 cells
- `msl2` RNAi-treated S2 cells
- `mof` RNAi-treated S2 cells

## Main Scientific Question

How do `msl2` and `mof` knockdown differ in their chromosome-level effect on gene expression?

More specifically:

Does `msl2` or `mof` knockdown affect X-linked gene expression more strongly relative to autosomal gene expression, and by how much?

## Expected Timeline

This is a self-paced project. It is intended to keep you busy for about one week.

I do not expect the complete project before the end of next week. Use the time to understand the biology, learn the analysis methods, write clean code, and prepare a reproducible report.

## Learning Goals

By the end of the project, you should understand:

- what RNA-seq measures
- what a count matrix is
- why normalization is needed
- what TPM or RPKM values mean
- what log2 fold change means
- what the MSL complex does in Drosophila dosage compensation
- how gene-level expression changes can be summarized at the chromosome level
- how to organize a reproducible bioinformatics project in R

Recommended starting points:

- RNA-seq / differential expression: <https://hbctraining.github.io/Intro-to-DGE/>
- `SummarizedExperiment`: <https://bioconductor.org/packages/release/bioc/vignettes/SummarizedExperiment/inst/doc/SummarizedExperiment.html>

## Provided Files

You will receive:

- raw count matrix
- normalized expression matrix, for example TPM or RPKM
- sample annotation table
- gene annotation table
- short README

Use the count matrix for differential-expression-style analysis. Use the normalized expression matrix for exploratory summaries and sanity checks.

## Technical Expectations

Treat this like a real reproducible data analysis project.

Create a GitHub repository containing:

- well-organized project folders
- all analysis code
- an R Markdown or Quarto report: `.Rmd` or `.qmd`
- a rendered HTML or PDF report
- an `renv` environment for reproducible R package versions
- clear documentation
- instructions that allow someone else to rerun your analysis

Within R, use a `SummarizedExperiment` object to store the core project data:

- raw count matrix as an assay
- normalized expression matrix as an assay
- sample annotations as `colData`
- gene annotations as `rowData`

Your repository should make it possible for another person to clone the project, restore the R environment, rerun the analysis, and reproduce your final result.

## Analysis Expectations

You should:

- inspect and document the provided data
- check that sample IDs and gene IDs match across files
- compare `msl2` RNAi with the control condition
- compare `mof` RNAi with the control condition
- connect gene-level expression changes to chromosome annotations
- summarize the effect on the X chromosome relative to the autosomes
- compare the chromosome-level effect between `msl2` RNAi and `mof` RNAi
- report the size of the difference clearly

Keep the analysis focused on the chromosome-level effect. You do not need to produce a long list of individual genes unless it helps explain the chromosome-level result.

## Final Deliverables

Submit:

1. Link to GitHub repository
2. Reproducible R project with `renv`
3. R Markdown or Quarto source file
4. Rendered HTML or PDF report
5. All analysis scripts or helper functions
6. Clear README with setup and rerun instructions
7. Use of `SummarizedExperiment` to organize counts, normalized expression values, sample metadata, and gene metadata
8. Concise numerical answer to the main question
9. Brief biological interpretation

## Final Answer Expected

Your final report should answer:

How different are the chromosome-level effects of `msl2` RNAi and `mof` RNAi?

A good final answer should be quantitative, for example:

> The X-specific expression effect is approximately ___ for `msl2` RNAi and ___ for `mof` RNAi. The difference between the two knockdowns is therefore ___.

Your final answer should be understandable to someone who knows basic genetics but has not seen this dataset before.
