# Kin_TF_net
## Repository structure and usage
```
.
├── Data
│   ├── human_kinases_uniprot.tsv
│   │       # Reference list of human kinases retrieved from UniProt
│   ├── Prodromal_LRRK2 vs healthy control TPM for VIPER.csv
│   │       # TPM-normalized RNA-seq data formatted for VIPER input
│   ├── Prodromal_LRRK2 vs Healthy control_expression_data_from_count.csv
│   │       # Raw gene-level count matrix used for differential expression analysis
│   └── Readme.rtf
│           # Additional dataset usage notes and preprocessing details
│
├── DE
│   ├── 0_kinases_Prodromal_LRRK2 vs Healthy control kinases DE analysis.rmd
│   │       # R Markdown script for differential expression analysis of kinase genes
│   ├── 1_results
│   │       # Output results from DE analysis (tables, plots)
│   └── Readme.rtf
│           # Notes explaining pipeline steps   
│
├── DE
│   ├── 0_Prodromal_LRRK2 vs Healthy control VIPER analysis.rmd
│   │       # R Markdown script performing VIPER analysis to infer TF activity changes
│   ├── 1_results
│   │       # Output results from VIPER analysis (inferred TF activities, plots, tables)
│   └── Readme.rtf
│           # Notes describing the VIPER workflow
│ 
├── LICENSE
└── README.md
```

### Data Availability
Due to data use agreements and patient protection requirements, raw RNA-seq data are not included in this repository. Users who need access to the original raw data should directly request access through the PPMI (https://www.ppmi-info.org/).

### Software Requirements
This project was developed and tested using R (≥ 4.2) with the following packages:
DESeq2, viper, BiocManager, tidyverse, openxlsx, pheatmap. See each `.rmd` file for detailed session information.

### Reproducibility
To reproduce the analysis:
1. Prepare data following instructions in `/Data/Readme.rtf`
2. Run the `.rmd` files in `DE/` to generate differential expression results
3. Run the VIPER analysis `.rmd` to infer TF activity changes

If you use scripts in this repository, please cite:
"Stratified Signaling Network Remodeling of Kinase–Transcription Factors' Interactions in Parkinson's disease", Xiaoyan Zhou, Luca Parisi , Sicen Liu, Ziqi Cheng, Hanwen Liang,
Mansour Youseffi, Farideh Javid and Renfei Ma*
