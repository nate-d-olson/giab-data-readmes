This README_RNAseq_UNC_HG002.md was generated on 2023-04-14 by Nate Olson.

------------------- 
GENERAL INFORMATION
-------------------

**Title of Dataset**\
Illumina stranded mRNA and total RNA sequencing by Merker lab at UNC performed on three
HG002 cell lines as part of the NIST-GIAB RNAseq pilot sequencing project.

**Principal Investigator**\
Justin M. Zook\
Institution: National Institute of Standards and Technology (NIST)\
Email: jzook@nist.gov

**Dataset Contact(s)**\
Nathan D. Olson\
Institution: National Institute of Standards and Technology (NIST)\
Email: nolson@nist.gov

Jason Merker\
Institution: University of North Carolina at Chapel Hill (UNC)\
Email: jason_merker@med.unc.edu

**Date of data collection**\
2022-09

**Background**\
Illumina stranded mRNA and total RNA sequencing by Lineberger Comprehensive Cancer 
Center Translational Genomics Lab (TGL) at UNC performed on three
HG002 cell lines as part of the NIST-GIAB RNAseq pilot sequencing project.
The stranded mRNA and total RNA libraries were performed in triplicate and 
sequenced together on the same flow cell. 

**Usage**\
Basecalled reads for RNAseq (mRNA and total RNA sequencing). 
Fastq files can be processed using any standard transcriptomic pipeline.

**Limitations**\
[Discuss any known limitations of the data being described by
README. e.g. data is incomplete, assumptions that were made, exclusions, known
issues, etc.]

--------------------------
SHARING/ACCESS INFORMATION
--------------------------

**Licenses/restrictions placed on the data, or limitations of reuse**\
See NIST license and data use policy at the end of the document.

**Recommended citation for the data**\
[Provide citation with DOI]

**Links to other publicly accessible locations of the data**\
Links to publicly accessible locations of the data:

- NIH hosted GIAB ftp site: ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data_RNAseq/AshkenazimTrio/HG002_NA24385_son/Merker_UNC_Illumina/
- SRA: TODO 

--------------------
DATA & FILE OVERVIEW
--------------------
 
```
└── read_fastqs
    ├── HG002_GM24385_replicate1_mRNAseq_ILLUMINA_UNC_20220524_AGGTTATA-CAGTTCCG_R1_001.fastq.gz
    ├── HG002_GM24385_replicate1_mRNAseq_ILLUMINA_UNC_20220524_AGGTTATA-CAGTTCCG_R2_001.fastq.gz
    ├── HG002_GM24385_replicate1_totalRNAseq_ILLUMINA_UNC_20220518_ATTGTGAA-TGCATTGC_R1_001.fastq.gz
    ├── HG002_GM24385_replicate1_totalRNAseq_ILLUMINA_UNC_20220518_ATTGTGAA-TGCATTGC_R2_001.fastq.gz
    ├── HG002_GM24385_replicate2_mRNAseq_ILLUMINA_UNC_20220524_GAACCGCG-TGACCTTA_R1_001.fastq.gz
    ├── HG002_GM24385_replicate2_mRNAseq_ILLUMINA_UNC_20220524_GAACCGCG-TGACCTTA_R2_001.fastq.gz
    ├── HG002_GM24385_replicate2_totalRNAseq_ILLUMINA_UNC_20220518_CCTTCACC-GACGCTCC_R1_001.fastq.gz
    ├── HG002_GM24385_replicate2_totalRNAseq_ILLUMINA_UNC_20220518_CCTTCACC-GACGCTCC_R2_001.fastq.gz
    ├── HG002_GM24385_replicate3_mRNAseq_ILLUMINA_UNC_20220524_TCATCCTT-AGCGAGCT_R1_001.fastq.gz
    ├── HG002_GM24385_replicate3_mRNAseq_ILLUMINA_UNC_20220524_TCATCCTT-AGCGAGCT_R2_001.fastq.gz
    ├── HG002_GM24385_replicate3_totalRNAseq_ILLUMINA_UNC_20220518_GCCACAGG-CATGCCAT_R1_001.fastq.gz
    ├── HG002_GM24385_replicate3_totalRNAseq_ILLUMINA_UNC_20220518_GCCACAGG-CATGCCAT_R2_001.fastq.gz
    ├── HG002_GM26105_replicate1_mRNAseq_ILLUMINA_UNC_20220524_ACGCACCT-GGTGAAGG_R1_001.fastq.gz
    ├── HG002_GM26105_replicate1_mRNAseq_ILLUMINA_UNC_20220524_ACGCACCT-GGTGAAGG_R2_001.fastq.gz
    ├── HG002_GM26105_replicate1_totalRNAseq_ILLUMINA_UNC_20220518_AGTACTCC-AACCTGTT_R1_001.fastq.gz
    ├── HG002_GM26105_replicate1_totalRNAseq_ILLUMINA_UNC_20220518_AGTACTCC-AACCTGTT_R2_001.fastq.gz
    ├── HG002_GM26105_replicate2_mRNAseq_ILLUMINA_UNC_20220524_CGCTATGT-TCCGACAC_R1_001.fastq.gz
    ├── HG002_GM26105_replicate2_mRNAseq_ILLUMINA_UNC_20220524_CGCTATGT-TCCGACAC_R2_001.fastq.gz
    ├── HG002_GM26105_replicate2_totalRNAseq_ILLUMINA_UNC_20220518_GACGTCTT-GGTTCACC_R1_001.fastq.gz
    ├── HG002_GM26105_replicate2_totalRNAseq_ILLUMINA_UNC_20220518_GACGTCTT-GGTTCACC_R2_001.fastq.gz
    ├── HG002_GM26105_replicate3_mRNAseq_ILLUMINA_UNC_20220524_GTATGTTC-AACAGGAA_R1_001.fastq.gz
    ├── HG002_GM26105_replicate3_mRNAseq_ILLUMINA_UNC_20220524_GTATGTTC-AACAGGAA_R2_001.fastq.gz
    ├── HG002_GM26105_replicate3_totalRNAseq_ILLUMINA_UNC_20220518_TGGCCGGT-TAGAGCGC_R1_001.fastq.gz
    ├── HG002_GM26105_replicate3_totalRNAseq_ILLUMINA_UNC_20220518_TGGCCGGT-TAGAGCGC_R2_001.fastq.gz
    ├── HG002_GM27730_replicate1_mRNAseq_ILLUMINA_UNC_20220524_CGTCTGCG-TTCACAAT_R1_001.fastq.gz
    ├── HG002_GM27730_replicate1_mRNAseq_ILLUMINA_UNC_20220524_CGTCTGCG-TTCACAAT_R2_001.fastq.gz
    ├── HG002_GM27730_replicate1_totalRNAseq_ILLUMINA_UNC_20220518_ACAGGCGC-CTCTGCCT_R1_001.fastq.gz
    ├── HG002_GM27730_replicate1_totalRNAseq_ILLUMINA_UNC_20220518_ACAGGCGC-CTCTGCCT_R2_001.fastq.gz
    ├── HG002_GM27730_replicate2_mRNAseq_ILLUMINA_UNC_20220524_CTAGCGCT-GTGTAGAC_R1_001.fastq.gz
    ├── HG002_GM27730_replicate2_mRNAseq_ILLUMINA_UNC_20220524_CTAGCGCT-GTGTAGAC_R2_001.fastq.gz
    ├── HG002_GM27730_replicate2_totalRNAseq_ILLUMINA_UNC_20220518_CATAGAGT-TGCCACCA_R1_001.fastq.gz
    ├── HG002_GM27730_replicate2_totalRNAseq_ILLUMINA_UNC_20220518_CATAGAGT-TGCCACCA_R2_001.fastq.gz
    ├── HG002_GM27730_replicate3_mRNAseq_ILLUMINA_UNC_20220524_TACTCATA-CCTGTGGC_R1_001.fastq.gz
    ├── HG002_GM27730_replicate3_mRNAseq_ILLUMINA_UNC_20220524_TACTCATA-CCTGTGGC_R2_001.fastq.gz
    ├── HG002_GM27730_replicate3_totalRNAseq_ILLUMINA_UNC_20220518_TGCGAGAC-CATTGTTG_R1_001.fastq.gz
    ├── HG002_GM27730_replicate3_totalRNAseq_ILLUMINA_UNC_20220518_TGCGAGAC-CATTGTTG_R2_001.fastq.gz
    └── md5.in
```

**File Naming Convention**\
`[GIAB ID]_[CELL LINE ID]_replicate[number]_[Library method]_ILLUMINA_UNC_[sequencing date]_[sequencing barcode]_[READ]_[lane].fastq.gz`

**File Descriptions**
- `*.fastq.gz`: basecall files in gzipped compressed fastq file format

--------------------------
METHODOLOGICAL INFORMATION
--------------------------

RNA Quality Control
Total RNA samples isolated using a Qiagen RNeasy kit were sent by the Coriell Institute to the UNC Lineberger Comprehensive Cancer Center Translational Genomics Lab (TGL). Total RNA quality was analyzed using a RNA ScreenTape (Agilent 5067-5576) and TapeStation 4200 (Agilent G2991AA) and the quantity was measured using a RNA Broad Range kit (Invitrogen Q10211) and Qubit Flex Fluorometer (Thermo Scientific Q33327).

Library Preparation
mRNA sequencing libraries were prepared at TGL from 1000 ng of Total RNA in triplicate using a TruSeq Stranded mRNA Library Prep Kit (Illumina 20020595) following the manufacturer’s protocol (Illumina 1000000040498). Total RNA sequencing libraries were prepared at TGL from 1000 ng of Total RNA in triplicate using a TruSeq Stranded Total RNA Library Prep Gold Kit (Illumina 20020599) following the manufacturer’s protocol (Illumina 1000000040499).

Sequencing
Library QC and sequencing was performed at TGL. mRNA and Total RNA library quality and quantity were measured using a D1000 DNA Screentape (Agilent 5067-5582) and a Qubit 1X dsDNA High Sensitivity Assay Kit (Thermo Fisher Q33231), combined at equal molar ratios in two separate pools (one for mRNA and one for Total RNA), and denatured following the manufacturer’s protocol (Illumina 15039740 for MiSeq or Illumina 1000000106351 for NovaSeq). Pooled libraries were first sequenced on a MiSeq Nano flow cell (Illumina MS-103-1001) to balance the pool before being sequenced on a NovaSeq 6000 S4 flow cell (Illumina 20027466) with an XP kit (Illumina 20021665). Each pool was sequenced on two lanes of the S4 flow cell with a 2x150 bp paired-end configuration following the manufacturer’s protocol (Illumina 1000000019358). The pools were designed to target about 325 million clusters per library on average.

**Quality Assurance**\
See `RNA_QC_report.pdf` for QA/QC information provided by UNC provided QC report provided by Merker Lab.
TODO- add to ftp site https://drive.google.com/file/d/1EImNO8BnzBdooXZIt7oo2S_H1wPobSnv/view?usp=sharing


--------------------------
DATA USE POLICY
--------------------------

This software was developed by employees of the National Institute of Standards
and Technology (NIST), an agency of the Federal Government and is being made
available as a public service. Pursuant to title 17 United States Code Section
105, works of NIST employees are not subject to copyright protection in the
United States. This software may be subject to foreign copyright. Permission in
the United States and in foreign countries, to the extent that NIST may hold
copyright, to use, copy, modify, create derivative works, and distribute this
software and its documentation without fee is hereby granted on a non-exclusive
basis, provided that this notice and disclaimer of warranty appears in all
copies.

THE SOFTWARE IS PROVIDED 'AS IS' WITHOUT ANY WARRANTY OF ANY KIND, EITHER
EXPRESSED, IMPLIED, OR STATUTORY, INCLUDING, BUT NOT LIMITED TO, ANY WARRANTY
THAT THE SOFTWARE WILL CONFORM TO SPECIFICATIONS, ANY IMPLIED WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND FREEDOM FROM
INFRINGEMENT, AND ANY WARRANTY THAT THE DOCUMENTATION WILL CONFORM TO THE
SOFTWARE, OR ANY WARRANTY THAT THE SOFTWARE WILL BE ERROR FREE. IN NO EVENT
SHALL NIST BE LIABLE FOR ANY DAMAGES, INCLUDING, BUT NOT LIMITED TO, DIRECT,
INDIRECT, SPECIAL OR CONSEQUENTIAL DAMAGES, ARISING OUT OF, RESULTING FROM, OR
IN ANY WAY CONNECTED WITH THIS SOFTWARE, WHETHER OR NOT BASED UPON WARRANTY,
CONTRACT, TORT, OR OTHERWISE, WHETHER OR NOT INJURY WAS SUSTAINED BY PERSONS OR
PROPERTY OR OTHERWISE, AND WHETHER OR NOT LOSS WAS SUSTAINED FROM, OR AROSE OUT
OF THE RESULTS OF, OR USE OF, THE SOFTWARE OR SERVICES PROVIDED HEREUNDER.

