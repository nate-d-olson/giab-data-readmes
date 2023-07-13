This README_RNAseq_Google_HG004_ILL.md was generated on 2023-05-31 by Ummey Jannat.

GENERAL INFORMATION
-------------------

**Title of Dataset**\
Illumina mRNA and long non-coding RNA sequencing for HG004

**Principal Investigator**\
Justin M. Zook\
Institution: National Institute of Standards and Technology (NIST)\
Email: <jzook@nist.gov>

**Dataset Contact(s)**\
Nathan D. Olson\
Institution: National Institute of Standards and Technology (NIST)\
Email: <nolson@nist.gov>

Andrew Carroll\
Institution: Google\
Email: <acarroll@google.com>

**Date of data collection**\
2022-01-10

**Background**\
Illumina stranded mRNA and long non-coding RNA sequencing was contracted
out to Novogene by Google on the HG004 cell line as part of the NIST-GIAB
RNAseq pilot sequencing project.

**Usage**\
Basecalled reads and alignments for RNAseq (mRNA and long-non-conding RNA sequencing).
Fastq and bam files can be processed using any standard transcriptomic pipeline.

SHARING/ACCESS INFORMATION
--------------------------

**Licenses/restrictions placed on the data, or limitations of reuse**\
See NIST license and data use policy at the end of the document.

**Recommended citation for the data**\
Manuscript in development

**Links to other publicly accessible locations of the data**\
Links to publicly accessible locations of the data:

- NIH hosted GIAB ftp site: ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data_RNAseq/AshkenazimTrio/HG004_NA24143_mother/Google_Illumina
- SRA: Will update when submitted

DATA & FILE OVERVIEW
--------------------

```text
.
├── Long_noncoding_RNA
│   ├── alignments
│   │   ├── hg004_gm24631.lncrna.grch38.bam
│   │   ├── hg004_gm24631.lncrna.grch38.bam.bai
│   │   └── md5.in
│   └── reads
│       ├── hg004_gm24631.lncrna.R1.fastq.gz
│       ├── hg004_gm24631.lncrna.R2.fastq.gz
│       └── md5.in
└── mRNA
    ├── alignments
    │   ├── hg004_gm24631.mrna.grch38.bam
    │   ├── hg004_gm24631.mrna.grch38.bam.bai
    │   └── md5.in
    └── reads
        ├── hg004_gm24631.mrna.R1.fastq.gz
        ├── hg004_gm24631.mrna.R2.fastq.gz
        └── md5.in
```

**File Naming Convention**\

- fastq.gz: `[GIAB ID]_[CELL LINE ID].[lncrna|mrnd]_[READ].fastq.gz`
- bam (and bai): `[GIAB ID]_[CELL LINE ID].[lncrna|mrnd].[ref].bam`

**File Descriptions**\

- `*.fastq.gz`: basecall files in gzipped compressed fastq file format
- `*bam`: Aligned reads to a reference genome.

METHODOLOGICAL INFORMATION
--------------------------

A. Library Preparation and Sequencing

From the RNA samples to the final data, each step, including sample test, library preparation, and sequencing, influences the quality of the data, and data quality directly impacts the analysis results. To guarantee the reliability of the data, quality control (QC) is performed at each step of the procedure. The workflow is as follows:

1 Sample Quality Control

Please refer to Novogene’s QC report for methods of sample quality control.

2 Library Construction, Quality Control and Sequencing

Messenger RNA was purified from total RNA using poly-T oligo-attached magnetic beads. After fragmentation, the first strand cDNA was synthesized using random hexamer primers followed by the second strand cDNA synthesis. The library was ready after end repair, A-tailing, adapter ligation, size selection, amplification, and purification. Following is the workflow of library construction:

The library was checked with Qubit and real-time PCR for quantification and bioanalyzer for size distribution detection. Quantified libraries will be pooled and sequenced on Illumina platforms, according to effective library concentration and data amount.

**Read Alignments**
Reads aligned to to reference using the STAR  aligner version 2.6.1d with the following command

```bash
STAR   \
    --runThreadN 12   \
    --runRNGseed 0   \
    --genomeDir STARIndex   \
    --readFilesIn [READ 1]   [READ 2]     \
    --readFilesCommand zcat      \
    --outFileNamePrefix [GIAB ID].   \
    --outSAMtype BAM   Unsorted      \
    --outSAMattributes NH   HI   AS   NM   MD      \
    --outSAMattrRGline ID:[GIAB ID]   SM:[GIAB ID]      \
    --outFilterMultimapNmax 20   \
    --alignSJDBoverhangMin 1   \
    --sjdbGTFfile genes.gtf   \
    --quantMode TranscriptomeSAM      \
    --quantTranscriptomeBan Singleend   \
    --twopassMode Basic
```

Reads were then sorted using samtools v 1.15.1.

```bash
samtools sort -@ 6 \
    -o [GIABID].sorted.bam \
    -T [GIABID].sorted \
    [GIABID].Aligned.out.bam
```

Duplicates marked using MarkDuplicates version 2.26.10

```bash
MarkDuplicates \
    INPUT=[GIABID].sorted.bam \
    OUTPUT=HG005.markdup.sorted.bam \
    METRICS_FILE=HG005.markdup.sorted.MarkDuplicates.metrics.txt \
    REMOVE_DUPLICATES=false \
    ASSUME_SORTED=true \
    TMP_DIR=[tmp] \
    VALIDATION_STRINGENCY=LENIENT\ MAX_SEQUENCES_FOR_DISK_READ_ENDS_MAP=50000 \ MAX_FILE_HANDLES_FOR_READ_ENDS_MAP=8000\
    SORTING_COLLECTION_SIZE_RATIO=0.25 \
    TAG_DUPLICATE_SET_MEMBERS=false \
    REMOVE_SEQUENCING_DUPLICATES=false \
    TAGGING_POLICY=DontTag \ 
    CLEAR_DT=true \
    DUPLEX_UMI=false \
    ADD_PG_TAG_TO_READS=true \ DUPLICATE_SCORING_STRATEGY=SUM_OF_BASE_QUALITIES \ PROGRAM_RECORD_ID=MarkDuplicates \
    PROGRAM_GROUP_NAME=MarkDuplicates \
    READ_NAME_REGEX=<optimized capture of last three ':' separated fields as numeric values> \
    OPTICAL_DUPLICATE_PIXEL_DISTANCE=100 \
    MAX_OPTICAL_DUPLICATE_SET_SIZE=300000 \
    VERBOSITY=INFO QUIET=false \
    COMPRESSION_LEVEL=5 \
    MAX_RECORDS_IN_RAM=500000 \
    CREATE_INDEX=false \
    CREATE_MD5_FILE=false \
    GA4GH_CLIENT_SECRETS=client_secrets.json \
    USE_JDK_DEFLATER=false \
    USE_JDK_INFLATER=false
```

**Quality Assurance**\
See `Novogene_methods_and_qc_report.html`

2 Summary of Sequencing Data Information

The total output of data on the sequencer: Raw data 159.7 G.

The detail statistics for the quality of sequencing data are shown in Table 1.

Table 1 Data Quality Summary

| Sample     | Raw reads | Raw data | Effective(%) | Error(%) | Q20(%) | Q30(%) | GC(%) |
|------------|-----------|----------|--------------|----------|--------|--------|-------|
| NA26105_C1 | 198886442 | 29.8     | 87.39        | 0.03     | 97.73  | 93.94  | 48.76 |
| NA27730_B2 | 225918726 | 33.9     | 89.96        | 0.03     | 97.87  | 94.15  | 47.98 |
| NA24385_K2 | 214746836 | 32.2     | 96.04        | 0.03     | 97.76  | 94.12  | 50.03 |
| NA24143_H5 | 215887922 | 32.4     | 95.04        | 0.03     | 97.46  | 93.63  | 51.79 |
| NA24631_F7 | 208909724 | 31.3     | 96.19        | 0.03     | 97.71  | 93.93  | 50.89 |

- Sample: sample name
- Raw reads: total amount of reads of raw data, each four lines taken as one unit. For paired-end sequencing, it equals the amount of read1 and read2.
- Raw data: (Raw read total length), calculating in Gb. Sequencing length equals 150.
- Effective: (Clean reads/Raw reads)*100%
- Error: base error rate
- Q20, Q30: (Base count of Phred value > 20 or 30) / (Total base count)
- GC: (G & C base count) / (Total base count)
  
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
