# WORK IN PROGRESS, FILES TO BE UPLOADED

# APOE-Multiomics

## APOE Genotype and Biological Age Impact Inter-Omic Associations Related to Bioenergetics

Ellis et al., preprint doi: https://doi.org/10.1101/2024.10.17.618322  
  
Correspondence to: Noa Rappaport; email: noa.rappaport@isbscience.org  

## Code and content

This repo includes scripts ran in Jupyter Notebook for performing the analyses and generating the figures for the study.  

In this README, each notebook is described, including the necessary input data and output files/figures generated. Note that input data needed for scripts to run must be requested (see "Requesting data" below).

### Code01_Arivale_Indiv_Metab_Analysis.ipynb
Code used to analyze individual metabolite abundance differences across APOE and delta age statuses in Arivale, including stratified by sex and chronological age tertiles.
Inputs:
* Preprocessed Arivale data: Arivale_preprocecessed_indiv_metab_analysis_data.csv
* Metabolomics metadata: Arivale_metabolomics_metadata.csv
Outputs (consolidated into Supplementary Files 1 & 2; included in Supplementary Table 3; used in figure scripts):
* Data files for APOE and delta age GLMs, including sex stratified and chronological age stratified results

### Code02_Arivale_Interaction_Analysis.ipynb
Code for running multi-omic interaction analyses in Arivale. The correct sections need to be commented in/out when running the script to select the correct stratified analysis (out of 11).
Inputs:
* xxx/////////////
Outputs (to be inputs for Code03):
* Log files and txt.gz result files from interaction analyses

### Code03_Arivale_Interaction_Analysis_Tidy_Interpret.ipynb
Code ////  ////
Inputs (from Code02 outputs):
* xxx//////////
Outputs (consolidated into Supplementary File 3; Summarized in Table 2 and Supplementary Table 4; used in circos figure script):
* xxxx/////////////

### Code04_TwinsUK_Indiv_Metab_Analysis.ipynb
Code ////  
Inputs:
* xxx///////////
Outputs (consolidated into Supplementary File 4; Included in Supplementary Table 3; used in figure scripts):
* xxxx/////////

### Code05_TwinsUK_Interaction_Analysis.ipynb
Code ////  
Inputs:
* xxx//////////
Outputs (to be inputs for Code06):
* xxxx//////////

### Code06_Enrichment_Analyses_and_Overlapping_Tables.ipynb
Code ////  
Inputs:
* xxx////////
Outputs:
* Results included in Supplementary Files 1 and 4; Table 3; Supplementary Tables 1 and 2

### Code07_Figure_Script.ipynb
Code used to generate figures, including comments for offline arranging and annotating.
Inputs:
* Arivale individual metabolite abundance analysis results (250217_Arivale_Indiv.csv and 250217_Arivale_Indiv_delage.csv)
* 
Outputs:
* Plots used for Figures 2-4 & S1-S6, data used for Table 1

### Code08_InteractionNetworkVisualization.ipynb
R code used to make the circos plots in Figures 3d and 3e, with sections rearranged in ppt.  
Inputs:
* Organized Arivale Interaction Analysis results (240707_ME2_MBioOld_FBioOld_for_circos_fig.xlsx)
* Metadata/analyte labels (240725_Arivale-APOE-BA_CleanMetadata_analyte-metadata.xlsx and 240819_Arivale-APOE-BA-Microbiome_Gaps_Filled.xlsx)
Outputs:
* Two circos plot figure files (arranged to Figures 3d and 3e)

### Code09_TwinsUK_BA_Fitting.ipynb
Code used to generate multi-omic biological age values for TwinsUK cohort.  
Inputs:
* xxxxx
Outputs:
* xxxx

## Requesting data
Qualified researchers can access the above deidentified input files for research purposes. Requests for the above files or for Arivale data should be sent to data-access@isbscience.org.  
  
Independent TwinsUK datasets used in this study were provided by the Department of Twin Research & Genetic Epidemiology (King’s College London) after the approval of our Data Access Application (project number E1199). Requests for TwinsUK should be referred to their website (http://twinsuk.ac.uk/resources-for-researchers/access-our-data/).

## Software requirements
The following packages/libraries were used in Python (v 3.9.7) and R (v 4.1.1) in Jupyter Notebook to run the scripts:
* statsmodels
* pandas
* numpy
* matplotlib
* scipy
* seaborn
* tidyverse
* readxl
* circlize
* RColorBrewer
* colorspace

## Log
Last update on Mar 31, 2025
* 2025-03-31 Generated this repository on GitHub, uploaded Jupyter Notebooks, drafted README
