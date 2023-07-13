This README_NIST_BGISeq_100x_HG002.md was generated on 2023-07-12 by Ummey Jannat.

------------------- 
GENERAL INFORMATION
-------------------

**Title of Dataset**\
HG002 BGIseq High Coverage (100X) 150bp paired-end.

**Principal Investigator**\
Justin M. Zook\
Institution: National Institute of Standards and Technology (NIST)\
Email: jzook@nist.gov

**Dataset Contact(s)**\
Nathan D. Olson\
Institution: National Institute of Standards and Technology (NIST)\
Email: nolson@nist.gov

**Date of data collection**\
2021-11

**Background**\
High coverage (100X) BGIsequencing of GIAB HG002 RM DNA [TODO - add brief method description].

**Usage**\
[TODO]

**Limitations**\
[TODO - Discuss any known limitations of the data being described by
README. e.g. data is incomplete, assumptions that were made, exclusions, known
issues, etc.]

--------------------------
SHARING/ACCESS INFORMATION
--------------------------

**Licenses/restrictions placed on the data, or limitations of reuse**\
See NIST license and data use policy at the end of the document.

**Recommended citation for the data**
[TODO]

**Links to other publicly accessible locations of the data**\
Links to publicly accessible locations of the data:

- NIH hosted GIAB ftp site: TODO
- SRA: TODO 

--------------------
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


**File Descriptions**
TODO

--------------------------
METHODOLOGICAL INFORMATION
--------------------------
Sequencing read length: PE150

Alignment: In this project, total clean reads per sample were aligned to the human reference genome using Burrows-Wheeler Aligner (BWA)

On average, 99.84% mapped successfully and 95.46% mapped uniquely. The duplicate reads were marked from total mapped reads, resulting in about 1.08% and 117.47-fold mean sequencing depth on the whole genome excluding gap regions. On average per sequencing individual, 99.84% of the whole genome excluding gap regions were covered by at least 1X coverage.

All clean reads were aligned to the human reference genome using Burrows-Wheeler Aligner (BWA
V0.7.17) . We did mapping for each lane separately and also add the read group identifier, which
by lane, into the alignment files. Here we used BWA-MEM method. Below are the BWA information
and commands used for the alignments:
Software Version Link
BWA v0.7.17 http://bio-bwa.sourceforge.net/
Here the 'read_group_tag' need to be provided, e.g. `@RG\tID:GroupID\tSM:SampleID\tPL:illumina\tLB:libraryID`.

Then, use samtools to sort the SAM files according to the mapped position and convert them into
BAM format files. The software information and command line parameters are as follows:
Software Version Link
samtools 1.3.1 http://www.htslib.org/
samtools sort @ 10 o sorted bam O BAM input bam
bwa mem -M -R 'read_group_tag' reference.fasta read1.fq.gz read2.fq.gz > aligned_reads
[1]
[2][3]
22 / 37
samtools sort -@ 10 -o sorted.bam -O BAM input.bam

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

