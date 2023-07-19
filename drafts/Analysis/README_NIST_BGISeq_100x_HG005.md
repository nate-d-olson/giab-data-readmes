This README_NIST_BGISeq_100x_HG005.md was generated on 2023-07-12 by Ummey Jannat.

GENERAL INFORMATION
-------------------

**Title of Dataset**\
HG005 BGIseq High Coverage (100X) 150bp paired-end.

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
High coverage (100X) BGIsequencing of GIAB HG005 RM DNA [TODO - add brief method description].

**Usage**\
Variant call files (vcf) can be use in any bioinformatic pipeline or downstream analyses for whole genome seqeuncing variant call analysis.

SHARING/ACCESS INFORMATION
--------------------------

**Licenses/restrictions placed on the data, or limitations of reuse**\
See NIST license and data use policy at the end of the document.

**Links to other publicly accessible locations of the data**\
Links to publicly accessible locations of the data:

- NIH hosted GIAB ftp site: ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data/ChineseTrio/analysis/NIST_BGIseq_2x150bp_100x
- SRA: Will provide when submitted

DATA & FILE OVERVIEW
--------------------
 
```text
.
├── HG005_GRCh37_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz
├── HG005_GRCh37_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz.tbi
├── HG005_GRCh37_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz
├── HG005_GRCh37_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz.tbi
├── HG005_GRCh38_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz
├── HG005_GRCh38_BGIseq-2x150-100x_NIST_20211126_indel.vcf.gz.tbi
├── HG005_GRCh38_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz
├── HG005_GRCh38_BGIseq-2x150-100x_NIST_20211126_snp.vcf.gz.tbi
└── md5.in

0 directories, 9 files
```


**File Naming Convention**\
Files are named according to the High coverage (100X) BGIsequencing of GIAB HG005. `HG005.[instrument id]_[YYMMDD]_[time].vcf.gz.tbi`


**File Descriptions**

- `*vcf.gz`: variant call file

METHODOLOGICAL INFORMATION
--------------------------

Used GATK HaplotypeCaller tool to simultaneously detect SNPs and InDels. The principle is to do
partial denovo assembly of haplotypes in areas with variant signals. The original mutation set is
stored in VCF format, which includes all potential mutation sites. The software information and
command line parameters are as follows: GATK HaplotypeCaller v4.1.4.1
<https://gatk.broadinstitute.org/hc/enus/articles/360037225632-HaplotypeCaller>.

```bash
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

NIST Data Use Policy
--------------------------------------------------------------------------------

This data/work was created by employees of the National Institute of Standards and Technology (NIST), an agency of the Federal Government. Pursuant to title 17 United States Code Section 105, works of NIST employees are not subject to copyright protection in the United States.  This data/work may be subject to foreign copyright.
​
The data/work is provided by NIST as a public service and is expressly provided “AS IS.” NIST MAKES NO WARRANTY OF ANY KIND, EXPRESS, IMPLIED OR STATUTORY, INCLUDING, WITHOUT LIMITATION, THE IMPLIED WARRANTY OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT AND DATA ACCURACY. NIST does not warrant or make any representations regarding the use of the data or the results thereof, including but not limited to the correctness, accuracy, reliability or usefulness of the data. NIST SHALL NOT BE LIABLE AND YOU HEREBY RELEASE NIST FROM LIABILITY FOR ANY INDIRECT, CONSEQUENTIAL, SPECIAL, OR INCIDENTAL DAMAGES (INCLUDING DAMAGES FOR LOSS OF BUSINESS PROFITS, BUSINESS INTERRUPTION, LOSS OF BUSINESS INFORMATION, AND THE LIKE), WHETHER ARISING IN TORT, CONTRACT, OR OTHERWISE, ARISING FROM OR RELATING TO THE DATA (OR THE USE OF OR INABILITY TO USE THIS DATA), EVEN IF NIST HAS BEEN ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.
​
To the extent that NIST may hold copyright in countries other than the United States, you are hereby granted the non-exclusive irrevocable and unconditional right to print, publish, prepare derivative works and distribute the NIST data, in any medium, or authorize others to do so on your behalf, on a royalty-free basis throughout the world.
​
You may improve, modify, and create derivative works of the data or any portion of the data, and you may copy and distribute such modifications or works. Modified works should carry a notice stating that you changed the data and should note the date and nature of any such change. Please explicitly acknowledge the National Institute of Standards and Technology as the source of the data:  Data citation recommendations are provided at https://www.nist.gov/open/license.
​
Permission to use this data is contingent upon your acceptance of the terms of this agreement and upon your providing appropriate acknowledgments of NIST’s creation of the data/work.

