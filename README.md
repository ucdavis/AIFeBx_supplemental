#Supplemental data for "Artificial intelligence-based quantification of
lymphocytes in feline small intestinal biopsies" 
(for submission as full manuscript to Veterinary Pathology)

##Objective
This repository contains scripts for data analysis and manuscript preparation.
Raw and intermediate data files will be available via bioImageArchive.

## Folder hierarchy
All the scripts are adjusted to a folder hierarchy, created by the script 
"folderTree". 
The variables "batch" and "top_dir" should be set to the name (batch) and 
location (top_dir) of the local machine on which it is run. 
The folder "input" contains input data (raw predictions coordinates for
AI-models and validation annotations, spreadsheets with pathologists grades,
image names, misprediction assessments and quality assessments)
The folder output contains subfolders of output files for each script/
The folder figure contain figures for the paper (from multiples scripts)
The folder tables contain tabular data used in the paper (from multiple scripts)

## Data
All input and output data will be made available via bioImage archive. 
It is recommended to download and organize the data into the intended folder tree
structure (to avoid running computationally intense portions).

## Scripts

- folderTree (sets up the folder hierarchy)
- mergeModels (merges the output from the component mucosal compartment model 
and the lymphocyte object detection model to generate intraepithelial and lamina
propria lymphocyte predictions)
- randomROI (generates random validation regions for test set)
- wsi_assesment (parses wsi quality and origin data, figure 3)
- lymphocyteValidation (compares AI-generated lymphocyte predictions (output 
from mergeModels with pathologists annotations and WSI quality 
(from wsi_assessment), Figures 5-12, Supplemental figures S2-S10)
- parseWSIgrades (parses pathologists grades)
- wsiReproducibility (analyse interobserver agreement between pathologists at 
WSI level (Main figure 13, Supplemental figures S11-13))
- wsiAI_vs_Path (compares AI-generated lymphocyte counts (from merge_models) 
with pathologists grades (from parseWSIgrades), figure 14))

- randomizeAuthors (randomizes order of equally contributing coauthors)