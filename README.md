# Copy Number Variation Calling from circulating tumore DNA (ctDNA)
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
- Parameters for QC check and filter

#### Alignment
- Alignment tool: BWA-MEM
- Alignment first will mapped reads from each lane separately
- Then after alignment, data from many lanes of one samples will be merged, deduplicated, and reindexed to provide the final bam output files

### Variant Calling
#### Reference data
- Hg38

#### Germline variation calling
- Germline mutation calling tool: GATK 3.7
- Provide BAF value

### CNV Calling
#### Coverage calculation

#### Constructing Panel of Normal (PoN)
##### Bias correction

##### Build up PoN

#### Copy Number Variation Calling
- Tool: PureCN
- Segmentation algorithm: CBS
##### Single sample process

##### Multiple samples process

