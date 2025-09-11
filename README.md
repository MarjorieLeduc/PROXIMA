# PROXIMA_4.3.R
Make descriptive and statistical analysis using DIA-NN or Maxquant output and generate word and excel reports with PCA, heatmaps, volcanoplots...

# Content
PROXIMA_4.3.R analyses data from Maxquant or DIA-NN or other softwares and generates 4 files :
- a Word file containing report with many plots including PCA, heatmaps, volcanoplot ...
- a Excel file containing protein quantifications, statistic tests results and number of peptides per proteins (if data are fro DIANN or Maxquant).
- a txt file containing the same data as the Excel file
- a .rds file that can be use with Shiny_PROTEOM_IC_viewer script to custom plots.

## Requirements
R4.4.0 or higher
RStudio 2024.04.1 Build 748 or higher

## Required data
To use PROXIMA_4.3.R,

For DIA-NN analysis, folder must contain :
- report.pg_matrix.tsv.txt
- report.log.txt
- report.pr_matrix.tsv
- report.parquet or report.tsv

(the Script is done for .d DIA files from Bruker)

(.d names files must not contain ".")

(In the spectral library, the contaminant proteins' accessions should be preceded by "Conta_" to be detected as Contaminant)

(export from DIANN must be called "report.tsv")
	
For Maxquant analysis, folder must contain :
- proteinGroups.txt
- mqpar.xml
- evidence.txt
- peptides.txt
- #runningTimes.txt (found in "combined/proc/" folder)

For other analysis :
- a file containing proteins intensities.

## Use
In RStudio, open the PROXIMA_4.2.R file, click on "Run app" and follow indication in "Data" sheets. Think to check, only for the first time, if you have all packages.
