# Mapping and preparing sequences for analysis 

Trimming adapter sequences from files.  I used a very large adapter file because subsets of this were leaving adapter contamination in my sequences 
Set minimum length to 36 bases. 

[trimming script](./GenomicMapping/trim.sh)


Mapped with BWA to the Drosophila melanogaster v6.23 genome

[mapping script](./GenomicMapping/bwa_map.sh)

I then merged reads from the same biological sample. Samples were sequenced twice to increase read depth. 

[merging biological replicates](./GenomicMapping/merge.sh)

Following mapping, I converted SAM to BAM files (compressing) using SAMtools. This step also sorts the file.
Will also filter for mapping quality less than 20. 

[convert to BAM and sort](./GenomicMapping/samTObam.sh)

# Realigning around indels using GATK 

First I have to add read group information. In the future, I should do this earlier in the pipeline 

[add read groups](./GenomicMapping/addreplacegroups.sh)

Indexing the files 

[GATK index](./GenomicMapping/gatkindex.sh)

This step identifies the indels in the files 

[find intervals](./GenomicMapping/gatkintravals.sh)

Realignment step

[GATK reallign](./GenomicMapping/gatkalign.txt) 

Finally, I removed duplicate reads using Picard 

[remove duplicates](./GenomicMapping/dedup.sh)

At this point, I can calculate the read depth for each sample

[calculate read depth](./GenomicMapping/calcdepth.sh)

I also merged treatments together at this point for the artificial selection experiment 
[merging ee lineages](./GenomicMapping/ee_merging.txt)

At this point, I was able to move on to creating pileup/mpileup files and population genetics analysis.  From here, the next steps are outlined in the [popoolation workflow](popoolation.md)








