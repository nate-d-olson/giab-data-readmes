This README_RNAseq_Baylor_PacBio_HG005.md was generated on 2023-06-05 by Ummey Jannat.

------------------- 
GENERAL INFORMATION
-------------------

**Title of Dataset**\
HG005 PacBio IsoSeq by the Baylor College of Medicine Human Genome Sequencing Center.

**Principal Investigator**\
Justin M. Zook\
Institution: National Institute of Standards and Technology (NIST)\
Email: jzook@nist.gov

**Dataset Contact(s)**\
Nathan D. Olson\
Institution: National Institute of Standards and Technology (NIST)\
Email: nolson@nist.gov

Fritz Sedlazeck\
Institution: Baylor College of Medicine\
Email: Fritz.Sedlazeck@bcm.edu

**Date of data collection**\
2022-01

**Background**\
PacBio IsoSeq by Baylor College of Medicine Human Genome Sequencing Center on three
HG002 cell lines as part of the NIST-GIAB RNAseq pilot sequencing project.

**Usage**\
Consensus basecalled reads for RNAseq, unaligned bam file can be processed using any 
standard transcriptomic pipeline optimized for HiFi IsoSeq data.

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

- NIH hosted GIAB ftp site: ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data_RNAseq/ChineseTrio/HG005_NA24631_son/Baylor_PacBio
- SRA: TODO 

--------------------
DATA & FILE OVERVIEW
--------------------
 
```
.
└── reads
    ├── m64139_220127_180020.hifi_reads.bam
    ├── m64139_220130_061226.hifi_reads.bam
    ├── m64139_220131_122551.hifi_reads.bam
    └── md5.in
```

**Sample IDs**\

| movie_name           | sample_id                 |
| ---------------------|---------------------------|
| m64139_220127_180020 | HG005-NA24385-LCL         |
| m64139_220130_061226 | HG005-NA27730-iPSCfromPBMC|
| m64139_220131_122551 | HG005-NA26105-iPSCfromLCL |  


**File Naming Convention**\
Files are named according to the PacBio movie naming convention. `[instrument id]_[YYMMDD]_[time].hifi_reads.bam`

**File Descriptions**
- `*.hifi_reads.bam`: unaligned consensus basecalled reads.

--------------------------
METHODOLOGICAL INFORMATION
--------------------------

|      RNA     |                   sample-id |                          HG005-NA24385-LCL                         |                     HG005-NA27730-iPSCfromPBMC                     |                      HG005-NA26105-iPSCfromLCL                     |
|:------------:|----------------------------:|:------------------------------------------------------------------:|:------------------------------------------------------------------:|:------------------------------------------------------------------:|
|      QC      |                  date-of-QC |                              1/13/2022                             |                              1/11/2022                             |                              1/11/2022                             |
|      QC      |                         RIN |                                  9                                 |                                 9.5                                |                                 9.5                                |
| LIBRARY-PREP |            date-of-lib-prep |                              1/10/2022                             |                              1/10/2022                             |                              1/10/2022                             |
| LIBRARY-PREP |       library-name-uniqueID |                      PCD_NISTRM.NA24385-1_1sA                      |                      PCD_NISTRM.NA27730-1_1sA                      |                      PCD_NISTRM.NA26105-1_1sA                      |
| LIBRARY-PREP |            library-protocol | Iso-Seq Express Template Preparation protocol.                     | Iso-Seq Express Template Preparation protocol.                     | Iso-Seq Express Template Preparation protocol.                     |
| LIBRARY-PREP |     library-prep-kit-vendor |                             NEB, PacBio                            |                             NEB, PacBio                            |                             NEB, PacBio                            |
| LIBRARY-PREP |       library-prep-kit-name | NEBNext Single Cell/Low Input cDNA Synthsis & Amplification Module | NEBNext Single Cell/Low Input cDNA Synthsis & Amplification Module | NEBNext Single Cell/Low Input cDNA Synthsis & Amplification Module |
|              |                             | Iso-Seq Express Oligo Kit                                          | Iso-Seq Express Oligo Kit                                          | Iso-Seq Express Oligo Kit                                          |
|              |                             | SMRTbell Express Template Prep Kit 2.0                             | SMRTbell Express Template Prep Kit 2.0                             | SMRTbell Express Template Prep Kit 2.0                             |
| LIBRARY-PREP |        library-input-amount |                               500 ng                               |                               500 ng                               |                               500 ng                               |
| LIBRARY-PREP |         number-of-libraries |                                  1                                 |                                  1                                 |                                  1                                 |
|  SEQUENCING  |         sequencing-platform |                         Pacific Biosciences                        |                         Pacific Biosciences                        |                         Pacific Biosciences                        |
|  SEQUENCING  |       sequencing-instrument |                              Sequel II                             |                              Sequel II                             |                              Sequel II                             |
|              | Template Prep Kit           |                      TPK Lxxxxx100938900123199                     |                      TPK Lxxxxx100938900123199                     |                      TPK Lxxxxx100938900123199                     |
|              | Binding Kit                 |                      BDK Lxxxxx101820500123199                     |                      BDK Lxxxxx101820500123199                     |                      BDK Lxxxxx101820500123199                     |
|  SEQUENCING  |              sequencing-kit |                      SQK 123660101826100081222                     |                      SQK 123660101826100081222                     |                      SQK 123660101826100081222                     |
|  SEQUENCING  |        sequencing-selection |                                HIFI                                |                                HIFI                                |                                HIFI                                |

**Quality Assurance**\
TODO

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

