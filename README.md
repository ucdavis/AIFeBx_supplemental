# Supplemental data for "Artificial intelligence-based quantification of lymphocytes in feline small intestinal biopsies" 
Wulcan, J. M., Giaretta, P. B., Fingerhood, S., de Brot, S., Crouch, E. E. V., Casanova, I., Ruivo, P. R., Bolfa, P., Streitenberger, N., Bertram, C. A., Donovan, T. A., Keel, M. K., Moore, P. F., & Keller, S. M. (2024). Artificial intelligence-based quantification of lymphocytes in feline small intestinal biopsies. Accepted for publication in Veterinary Pathology

## Objective
This repository contains scripts for data analysis and manuscript preparation.
Raw and intermediate data files are available via bioImageArchive (S-BIAD1129) 

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
All input and output data is available via bioImage archive (S-BIAD1129). 
It is recommended to download and organize the data into the intended folder tree
structure (to avoid running computationally intense portions).

## Scripts
- folderTree (sets up the folder hierarchy)
- mergeModels (merges the output from the component mucosal compartment model 
and the lymphocyte object detection model to generate intraepithelial and lamina
propria lymphocyte predictions)
- randomROI (generates random validation regions for test set)
- wsi_assesment (parse WSI quality and origin data, **Figure 3**)
- lymphocyteValidation (compares AI-generated lymphocyte predictions (output 
from mergeModels with pathologists annotations and WSI quality 
(from wsi_assessment), Figures 5-12, Supplemental figures S2-S10)
- parseWSIgrades (parses pathologists grades)
- wsiReproducibility (analyse interobserver agreement between pathologists at 
WSI level (Main Figure 13, Supplemental Figures S11-13))
- wsiAI_vs_Path (compares AI-generated lymphocyte counts (from merge_models) 
with pathologists grades (from parseWSIgrades), Figure 14))

- randomizeAuthors (randomizes order of equally contributing coauthors)