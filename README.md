# Somatic Variant Discovery - GATK Pipeline
*This project utilises the new version of GATK4 - The command lines are different from GATK3*

## Pre-processing data
### Raw data
- The sequencing of ctDNA of all patients were designed under the gene panel protocol
- The targeted genes are not provided, then, interval detection will be analysed through the coverage at every base of the whole sequence after finishing the alignment

### Pre-processed data
#### Quality control with QC
- Each samples are sequenced at multiple lanes
- QC will process each lane separately
- Output from QC can be used to check the quality of sequencing

#### Alignment
- Alignment first will mapped reads from each lane separately
- Then after alignment, data from many lanes of one samples will be merged, deduplicated, and reindexed to provide the final bam output files

### Variant Calling
#### Reference data

#### Constructing Panel of Normal (PoN)
##### Individual PoN

##### Import database from multiple PoN

#### 
