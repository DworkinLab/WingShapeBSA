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

