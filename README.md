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
* Preprocessed data: Arivale_preprocessed_interaction_analysis  
* List of analytes: Arivale_Interaction_Analysis_Analyte_List.json  
* Clinical chem annotations: Arivale_Interaction_Clinical_Annots.json  
* Protein annotations: Arivale_Interaction_Prots_Annots.json  
* Metabolite annotations: Arivale_Interaction_Metabs_Annots.json  
* Microbiome annotations: Arivale_Interaction_Microb_Annots.json  

Outputs (to be inputs for Code03):
* Log files and txt.gz result files from interaction analyses

### Code03_Arivale_Interaction_Analysis_Tidy_Interpret.ipynb
Code for analyzing and taking the txt.gz result files from Code02 and generating csv files to combine to Supplementary File 3.   

Inputs (from Code02 outputs):
* 240427_FE2_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240427_FE4_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240427_Fhealth_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240427_Funhealth_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240427_ME2_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240427_ME4_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240427_Mhealth_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240427_Munhealth_interomic_interact_Arivale_5SD_winsor.txt.gz  
* 240504_E2_allele_dose_interomic_interaction_5SD_winsor.txt.gz  
* 240504_E4_allele_dose_interomic_interaction_5SD_winsor.txt.gz  
* 240504_contin_del_age_interomic_interaction_5SD_winsor.txt.gz  

Outputs (consolidated into Supplementary File 3; Summarized in Table 2 and Supplementary Table 4; used in circos figure script):
* csv result files gathered to Supplementary File 3 

### Code04_TwinsUK_Indiv_Metab_Analysis.ipynb
Code for running individual metabolite abundance analysis in TwinsUK.  

Inputs:
* Preprocessed TwinsUK data: E1199_15122022_1_TwinsUK_Metab_Abundance.csv

Outputs (consolidated into Supplementary File 4; Included in Supplementary Table 3; used in figure scripts):
* Data files for APOE GLMs, including sex stratified and chronological age stratified results

### Code05_TwinsUK_Interaction_Analysis.ipynb
Code for running targeted multi-omic interaction analysis in TwinsUK.  

Inputs:
* Metabolomics metadata (subpathways from Metabolon, Arivale applies to TwinsUK): Arivale_metabolomics_metadata.csv
* Preprocessed TwinsUK data: E1199_15122022_2_TwinsUK_Interaction_Analysis.csv

Outputs:
* Data files organized into Supplementary File 5

### Code06_Enrichment_Analyses_and_Overlapping_Tables.ipynb
Code for performing enrichment analysis on the metabolites identified in Code01 and Code04, as well as constructing an overlapping table.  

Inputs:
* xxx////////  

Outputs:
* Results included in Supplementary Files 1 and 4; Table 3; Supplementary Tables 1 and 2

### Code07_Figure_Script.ipynb
Code used to generate figures, including comments for offline arranging and annotating.  

Inputs:
* xxx
* xxx

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
Code used to fit model and generate multi-omic biological age values for TwinsUK cohort - takes the average of 10 iterations.  

Inputs:
* Intermediate preprocessed TwinsUK data file (TwinsUK_pre_BA_fit.csv)

Outputs:
* Data file with metabolomic biological ages of TwinsUK individuals (TwinsUK_BA_fits.csv)

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
Last update on April 2, 2025
* March 2025 Initialized this repository on Github
* 2025-04-02 Uploaded Jupyter Notebooks to repo, drafted README
