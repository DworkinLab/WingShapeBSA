# Code and Data for Pelletier et al (2023) Genetics

This is the landing page for the repository for the data and scripts to reproduce the results from:

Pelletier et al. (2023). Complexities of recapitulating polygenic effects in natural populations: replication of genetic effects on wing shape in artificially selected and wild caught populations of *Drosophila melanogaster*. Genetics. Accepted.

This contains work flows and scripts related to this project. 

Please note: All raw sequence data (`.fastq`) is in the process of being uploaded to NCBI SRA. Accession identifiers will be added when the process is completed.

All data is pool sequencing data. Reads are 150 BP paired end sequencing. 

This project consists of two primary "experiments": 

1. Response to selection. Using a synthetic outbred population, lines were selected for 7 generations based on similarity to shape change vector (either *ds* or *emc*). Pools consist of 75 individuals in each of three replicates (A,B,C) for each of the selection treatments (UP, DOWN, CONTROL) 

2. Natural populations. Cohorts were collected from 4 natural populations in Michigan and phenotyped based on similarity to the focal gene (*ds* or *neur*) shape change vector. Pools consist of the most extreme individuals from the corresponding distributions. Pools consist of 75 individuals for each pool, within each of the 4 populations. 

The goal is to identify the regions of the genome selected on in the first project as well as those regions/genes contributing to the phenotypic range.

## Workflow 

[Here](./genomemapping.md) you can find the workflow for the mapping of raw reads to the *D. melanogaster* genome.

[Here](./popoolation.md) you can find the workflow for calculating Fst using Popoolation and Popoolation2.

[Here](./Rworkflow.md) you can find analyses done in R, including morphometrics, and genome analyses. 

## Data Files 

Variables in the data files are explained in the R scripts associated with analyses. 

`BSA_all_wings.csv` contains all procrustes superimposed shape residuals for wild caught populations. Population of origin, sex and block/collection year (1 = 2013, 2 = 2014). See code for specific information about landmark positions. The `selectedshape` files are subsets of these files, including only the individuals used for the BSA pools.

`BothLabs_Wings_28Oct.csv.zip` Contains shape data for the DGRP lines. See Pitchers et al 2019 for more information about data collection. 

`emc_selection_all_lmTransform.csv` contains procrustes superimposed shape residuals for *emc* artificial selection experiment. Centroid size has already been fit as a covariate for these residuals and is not included in this data set. 

`ds_allDat_selection.dat` contains procrustes superimposed shape residuals for *ds* artificial selection experiment.

`Chromosome_Gene.tsv` Is a bed file of *Drosophila* genes with locations, generated using FlyBase.

`artSel_parents` contains an index of the parental DRGRP lines used to create synthetic outbred population.

`.fst` are tab-delimited files that are the outputs of pairwise Fst values between sequencing pools, calculated using PoPoolation2. Window size and associated experiment are indicated in file names. See code for explanation of pool numbers for each file. If `merge` is used in the name, all up selection, down selection control selection lineage, or pools from a wild population have been merged together into a single pool 

All other data files are a result of the analysis in R. See associated R scripts for explanation of analysis to generate files. 







