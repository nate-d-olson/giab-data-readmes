This README_NIST_BGISeq_100x_HG002.md was generated on 2023-07-12 by Ummey Jannat.

GENERAL INFORMATION
-------------------

**Title of Dataset**\
HG002 BGIseq High Coverage (100X) 150bp paired-end.

**Principal Investigator**\
Justin M. Zook\
Institution: National Institute of Standards and Technology (NIST)\
Email: <jzook@nist.gov>

**Dataset Contact(s)**\
Nathan D. Olson\
Institution: National Institute of Standards and Technology (NIST)\
Email: <nolson@nist.gov>

**Date of data collection**\
2021-11

**Background**\
High-coverage (100X) 2X150 bp BGIsequencing of GIAB HG002 RM DNA.
Sequencing was contracted out to BGIseq by NIST and performed using the DNBSEQ platform.

**Usage**\
Fastq and bam files can be used in any standard whole genome short-read bioinformatic pipeline.

SHARING/ACCESS INFORMATION
--------------------------

**Licenses/restrictions placed on the data, or limitations of reuse**\
See NIST license and data use policy at the end of the document.

**Recommended citation for the data**
Manuscript in prep

**Links to other publicly accessible locations of the data**\
Links to publicly accessible locations of the data:

- NIH hosted GIAB ftp site: ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data/AshkenazimTrio/HG002_NA24385_son/NIST_BGIseq_2x150bp_100x
- SRA: Will provide when submitted

DATA & FILE OVERVIEW
--------------------

```
.
├── GRCh37
│   ├── HG002_GRCh37_BGIseq-2x150-100x_NIST_20211126.bam
│   └── HG002_GRCh37_BGIseq-2x150-100x_NIST_20211126.bam.bai
├── GRCh38
│   ├── HG002_GRCh38_BGIseq-2x150-100x_NIST_20211126.bam
│   └── HG002_GRCh38_BGIseq-2x150-100x_NIST_20211126.bam.bai
└── reads
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-606_1.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-606_2.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-607_1.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-607_2.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-608_1.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-608_2.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-609_1.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-609_2.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-610_1.fq.gz
    ├── 211109_M024_V350038332_L01_HUMuarfR092940-610_2.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-606_1.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-606_2.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-607_1.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-607_2.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-608_1.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-608_2.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-609_1.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-609_2.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-610_1.fq.gz
    ├── 211109_M024_V350038332_L02_HUMuarfR092940-610_2.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-606_1.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-606_2.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-607_1.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-607_2.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-608_1.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-608_2.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-609_1.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-609_2.fq.gz
    ├── 211109_M024_V350038332_L03_HUMuarfR092940-610_1.fq.gz
    └── 211109_M024_V350038332_L03_HUMuarfR092940-610_2.fq.gz

3 directories, 34 files
```

**File Naming Convention**\

Files are named according to the High coverage (100X) BGIsequencing of GIAB HG002. `HG002.[instrument id]_[YYMMDD]_[time].fq.gz`

**File Descriptions**\

- `*.fastq.gz`: basecall files in gzipped compressed fastq file format
- `*bam`: Aligned reads to a reference genome.
- `*bam.bai`: index file for aligned reads.

METHODOLOGICAL INFORMATION
--------------------------

## DNBSEQ Short-read library preparation

1. DNA fragmentation
2. Size selection
3. End repair and "A" tailing
4. Adapter ligation
5. Product size selection
6. PCR reaction
7. Library QC
8. Sequencing

Sequencing-derived raw image files were processed by DNBSEQ basecalling Software for base-calling
with default parameters and the sequence data of each individual was generated as paired-end
reads, which was defined as "raw data" and stored in FASTQ format.

## Bioinformatics Analysis Overview

The bioinformatics analysis began with the sequencing data. First, the clean data or clean reads was
produced by data filtering on raw data. Then all clean data of each sample was mapped to the human
reference genome to get initial comparison file in BAM format. Burrows-Wheeler Aligner (BWA)
software was used to do the alignment. To ensure accurate variant calling, we followed recommended
Best Practices for variant analysis with the Genome Analysis Toolkit(GATK). Base quality score
recalibration and duplicate reads marked were performed using GATK . The sequencing depth and
coverage for each individual were calculated based on the alignments.

**Quality Assurance**\
Data analysis quality control system(QC) in the whole pipeline was built to
guarantee qualified sequencing data.

NIST Data Use Policy
--------------------------------------------------------------------------------

​
This data/work was created by employees of the National Institute of Standards and Technology (NIST), an agency of the Federal Government. Pursuant to title 17 United States Code Section 105, works of NIST employees are not subject to copyright protection in the United States.  This data/work may be subject to foreign copyright.
​
The data/work is provided by NIST as a public service and is expressly provided “AS IS.” NIST MAKES NO WARRANTY OF ANY KIND, EXPRESS, IMPLIED OR STATUTORY, INCLUDING, WITHOUT LIMITATION, THE IMPLIED WARRANTY OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT AND DATA ACCURACY. NIST does not warrant or make any representations regarding the use of the data or the results thereof, including but not limited to the correctness, accuracy, reliability or usefulness of the data. NIST SHALL NOT BE LIABLE AND YOU HEREBY RELEASE NIST FROM LIABILITY FOR ANY INDIRECT, CONSEQUENTIAL, SPECIAL, OR INCIDENTAL DAMAGES (INCLUDING DAMAGES FOR LOSS OF BUSINESS PROFITS, BUSINESS INTERRUPTION, LOSS OF BUSINESS INFORMATION, AND THE LIKE), WHETHER ARISING IN TORT, CONTRACT, OR OTHERWISE, ARISING FROM OR RELATING TO THE DATA (OR THE USE OF OR INABILITY TO USE THIS DATA), EVEN IF NIST HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.
​
To the extent that NIST may hold copyright in countries other than the United States, you are hereby granted the non-exclusive irrevocable and unconditional right to print, publish, prepare derivative works and distribute the NIST data, in any medium, or authorize others to do so on your behalf, on a royalty-free basis throughout the world.
​
You may improve, modify, and create derivative works of the data or any portion of the data, and you may copy and distribute such modifications or works. Modified works should carry a notice stating that you changed the data and should note the date and nature of any such change. Please explicitly acknowledge the National Institute of Standards and Technology as the source of the data:  Data citation recommendations are provided at https://www.nist.gov/open/license.
​
Permission to use this data is contingent upon your acceptance of the terms of this agreement and upon your providing appropriate acknowledgments of NIST’s creation of the data/work.