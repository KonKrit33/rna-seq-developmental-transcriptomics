# RNA-seq Developmental Transcriptomics Analysis

This repository contains a reproducible RNA-seq bioinformatics project focused on transcriptional dynamics during mouse tissue development. The analysis uses publicly available RNA-seq data from mouse brain and liver across embryonic and postnatal developmental stages, applying quality control, alignment, gene-level quantification, differential expression analysis, Gene Ontology enrichment, and IGV-based genome-level validation.

## Project Context

The project is based on the study:

Schmitt et al. *High-resolution mapping of transcriptional dynamics across tissue development reveals a stable mRNA–tRNA interface*. Genome Research, 2014.

The original dataset includes mouse developmental RNA-seq samples from brain and liver across six developmental stages: E15.5, E18.5, P0.5, P4, P22, and P29.

## Analysis Workflow

The analysis includes:

- RNA-seq quality control
- Adapter trimming and read preprocessing
- Alignment to the mm10 mouse reference genome using STAR
- Gene-level quantification using featureCounts
- Variance-stabilizing transformation and PCA
- Differential expression analysis using DESeq2
- Gene Ontology Biological Process enrichment analysis
- Genome-level validation using IGV visualization

## Key Results

- PCA showed strong separation by tissue identity, with PC1 explaining 91% of the variance.
- Developmental stage contributed secondary but biologically meaningful variation.
- DESeq2 identified 10,915 significantly differentially expressed genes in the P29 vs E15.5 contrast.
- DESeq2 identified 3,670 significantly differentially expressed genes in the P4 vs E15.5 contrast.
- GO enrichment highlighted cell-cycle, mitotic, metabolic, mitochondrial, and developmental processes.
- IGV snapshots confirmed stage-dependent expression differences at representative gene loci.

## Repository Structure

```text
.
├── GO/
├── IGV/
├── Bio_Project.pdf
├── DE_P29_vs_E15_ALL_GENES.xlsx
├── DE_P29_vs_E15_top20GENES.xlsx
├── DE_P4_vs_E15_ALL_GENES.xlsx
├── DE_P4_vs_E15_top20GENES.xlsx
├── Report_results.xlsx
├── README.md
└── .gitignore
```

## Included Files

- `Bio_Project.pdf`: Full project report with methodology, results, figures, and interpretation.
- `DE_P29_vs_E15_ALL_GENES.xlsx`: Complete differential expression results for P29 vs E15.5.
- `DE_P29_vs_E15_top20GENES.xlsx`: Top differentially expressed genes for P29 vs E15.5.
- `DE_P4_vs_E15_ALL_GENES.xlsx`: Complete differential expression results for P4 vs E15.5.
- `DE_P4_vs_E15_top20GENES.xlsx`: Top differentially expressed genes for P4 vs E15.5.
- `Report_results.xlsx`: Summary tables and analysis outputs.
- `GO/`: Gene Ontology enrichment results and visualizations.
- `IGV/`: IGV snapshots used for genome-level validation.

## Tools and Technologies

- RNA-seq
- STAR
- featureCounts
- DESeq2
- Gene Ontology enrichment
- IGV
- R
- Linux command-line workflow
- Transcriptomics
- Differential gene expression analysis

## Notes

Raw sequencing data, reference genome files, STAR indices, BAM files, and large intermediate files are not included due to size and distribution constraints. The repository includes the final report, processed result tables, enrichment outputs, and genome-browser validation figures.

## Relevance

This project demonstrates practical experience in reproducible bioinformatics workflows, transcriptomics, statistical modelling of RNA-seq data, biological interpretation of differential expression, and visualization of genomic signals.
