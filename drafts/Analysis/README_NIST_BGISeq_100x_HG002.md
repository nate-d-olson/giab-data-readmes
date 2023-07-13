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
├── HG002_GRCh37_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz
├── HG002_GRCh37_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz.tbi
├── HG002_GRCh37_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz
├── HG002_GRCh37_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz.tbi
├── HG002_GRCh38_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz
├── HG002_GRCh38_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz.tbi
├── HG002_GRCh38_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz
├── HG002_GRCh38_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz.tbi
└── md5.in
```


**File Naming Convention**\
Files are named according to the High coverage (100X) BGIsequencing of GIAB HG002 `HG002.[instrument id]_[YYMMDD]_[time].vcf.gz.tbi`


**File Descriptions**
TODO

--------------------------
METHODOLOGICAL INFORMATION
--------------------------
DNA Sequencing
DNBSEQ Short-read library preparation：
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

Bioinformatics Analysis Overview
The bioinformatics analysis began with the sequencing data. First, the clean data or clean reads was
produced by data filtering on raw data. Then all clean data of each sample was mapped to the human
reference genome to get initial comparison file in BAM format. Burrows-Wheeler Aligner (BWA)
software was used to do the alignment. To ensure accurate variant calling, we followed recommended
Best Practices for variant analysis with the Genome Analysis Toolkit(GATK). Base quality score
recalibration and duplicate reads marked were performed using GATK . The sequencing depth and
coverage for each individual were calculated based on the alignments.
In addition, the strict data analysis quality control system(QC) in the whole pipeline was built to
guarantee qualified sequencing data.

Variant Calling
Use GATK HaplotypeCaller tool to simultaneously detect SNPs and InDels . The principle is to do
partial denovo assembly of haplotypes in areas with variant signals. The original mutation set is
stored in VCF format, which includes all potential mutation sites. The software information and
command line parameters are as follows:
Software Version Link
GATK
HaplotypeCaller
v4.1.4.1
https://gatk.broadinstitute.org/hc/enus/articles/360037225632-HaplotypeCaller 

```
gatk -T HaplotypeCaller \
-R reference.fasta \
-I bqsr.bam \
-O raw.g.vcf
-ERC GVCF
```

Germline mutation calling is based on the comparison result Bam file, including the detection and
annotation of SNP, InDel, SV and CNV (the latter two are limited to whole-genome sequencing).



**Quality Assurance**\
To ensure accurate variant calling, we followed recommended Best Practices for variant analysis with the Genome Analysis Toolkit(GATK). Base quality score
recalibration and duplicate reads marked were performed using GATK. The sequencing depth and
coverage for each individual were calculated based on the alignments.

In addition, the strict data analysis quality control system(QC) in the whole pipeline was built to
guarantee qualified sequencing data.

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

