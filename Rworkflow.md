# Downstream analysis for genomic and morphometric data 

## Genomic analysis 

A number of functions are needed for genomic plotting and can be found [here](./Code/KP_genomescan_source.R) as well as [here](./Code/fly_to_GO.delim)

The analysis for the *ds* genomic artificial selection, including the plotting of Fst and GO analyses can be found in [this](./Code/ds_FINAL_artselgenome.R) script. There is also a related analysis for [emc](./Code/emc_FINAL_artselgenome.R)

[This](./Code/ds_wild_fst_plottingByPop.R) analysis creates supplemental figure 22 and [this](./Code/neur_wild_byPopFst.R) associated script for supplemental figure 25.

CMH test for pooled data was done using the ACER package. All scripts for this are indicated with `ACER` in the title but a representative can be found here.

[ACER analysis](./Code/ACER_ds.R)


## Morphometric Analysis 

[This](./Code/DGRPfig.R) script will recreate the correlation plot between shape change vectors and DGRP PCs. 

[This](./Code/WildPopulationShapeAnalysis.R) script contains analysis for wild populations, including correlation with shape change vectors and phenotypic variation between populations. 

[This](./Code/dsreponsetosel.R) analysis describes the analysis of the response to selection from ds shape change. There is also a related analysis for [emc](./Code/emc_responsetosel.R) change change selection. 


## Comparing Phenotypic and Genetic distances 

First, the sync file needed to be converted into reference and alternate allele counts using [this](./Code/SyncToCounts.R)

Then genetic distances could be compared with phenotypic distances (calculated in [this](./Code/WildPopulationShapeAnalysis.R) analysis) using vegan [see here](./Code/PCoA_distanceFig.R)


# Misc analysis 

[this](./Code/MAFfig.R) script creates supplemental figure 1

[this](./Code/paperFigures.R) combines multiple analyses into single figures. 

[this](./Code/projectionFigs.R) script creates supplemental figure 5 