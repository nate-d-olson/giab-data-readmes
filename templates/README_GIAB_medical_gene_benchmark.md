This GIAB challenging medically relevant gene benchmark (CMRG) v1.00 README file was generated on 2021-06-04 by Sierra D. Miller




-------------------
GENERAL INFORMATION
-------------------

Title of Dataset: GIAB Challenging Medically Relevant Gene Benchmark


__Author Information:__
Principal Investigator: Justin M. Zook
          Institution: NIST
          Email: jzook@nist.gov
Associate or Co-investigator: Justin Wagner
          Institution: NIST
          Email: justin.wagner@nist.gov
Associate or Co-investigator: Nathan D. Olson
          Institution: NIST
          Email: nathanael.olson@nist.gov
Associate or Co-investigator: Jennifer McDaniel
          Institution: NIST
          Email: jennifer.mcdaniel@nist.gov

Date of data collection: 2021-04-23


__BACKGROUND__
This directory contains v1.00 of a small variant benchmark and structural variant benchmark focused on 273 challenging medically relevant genes for the Genome in a Bottle (GIAB) sample HG002 (aka Ashkenazi son). These benchmarks were generated from a trio-based hifiasm v0.11 (https://rdcu.be/ci3lZ) diploid assembly of HG002 using PacBio HiFi reads for HG002 for assembly and partitioning into phased haplotypes using Illumina reads for the parents, HG003 and HG004. This benchmark contains vcfs for small and structural variants along with corresponding benchmark bed files indicating regions that are homozygous reference if they do not have a variant in the vcf. We extensively curated the variant calls, excluding any found to be questionable or errors. This benchmark helps measure performance in important challenging regions, including challenging segmental duplications, regions with complex variants, regions with structural variants, and regions affected by false duplications in GRCh37 or GRCh38.




__Data Usage__
The benchmark vcf and bed files are intended to be used as a pair to benchmark accuracy of small variant calls. Benchmarking variant calls is a complex process. For small variants we recommend following the best practices for benchmarking small variants published in 2019 by the Global Alliance for Genomics and Health (GA4GH) Benchmarking Team (https://rdcu.be/bqpDT). For structural variants, we only include isolated insertions and deletions because they can generally be reliably benchmarked with existing tools like truvari and svanalyzer. For SVs, we found that some callers represent tandem duplications and tandem repeat expansions as duplications with SVTYPE=DUP (and sometimes incorrectly as translocations or inversions), whereas our benchmark calls these as insertions with the annotation REPTYPE=DUP. These can be counted as true positives by ignoring SVTYPE (--type-ignore -p 0 option in truvari) or by changing SVTYPE from DUP to INS in the query VCF.


__LIMITATIONS__


  - For the reasons below, it is not a random subset of the genome, so performance measured against this benchmark will not be the same as the performance for all genomic regions  
  - It only includes autosomes  
  - It excludes homopolymers >20bp and some indels in highly homozygous regions that are incorrectly resolved by hifiasm v0.11  
  - It only includes medically relevant genes covered <90% by v4.2.1 in HG002 on GRCh37 or GRCh38  
  - It uses gene coordinates as downloaded from ENSEMBL  
  - It excludes genes that were not fully and accurately resolved by the hifiasm v0.11 assembly (e.g., SMN2)  
  - It excludes genes with very large structural or copy number variation, which cause breaks in the assembly-assembly alignment or multiple contigs to align (e.g., LPA, CR1, and KIR genes)  
  - The benchmark bed excludes complex SVs, because no current tools exist to compare these  






--------------------------
SHARING/ACCESS INFORMATION
-------------------------- 


Recommended citations for the data:
  Draft Manuscript (anticipated posting on bioRxiv in June 2021): 
 https://docs.google.com/document/d/17Nc5noza9ElPhw1hh9zKphUDDJAsBV5bWyiLXcaTcII/edit?usp=sharing


Corresponding Data: 
  
HiFi Sequencing Data: Wenger, A.M., Peluso, P., Rowell, W.J. et al. Accurate circular consensus long-read sequencing improves variant detection and assembly of a human genome. Nat Biotechnol 37, 1155–1162 (2019). https://doi.org/10.1038/s41587-019-0217-9


hifiasm assembly: Cheng H, Concepcion GT, Feng X, Zhang H, Li H. Haplotype-resolved de novo assembly using phased assembly graphs with hifiasm. Nature Methods. 2021;18: 170–175. doi:10.1038/s41592-020-01056-5

CHM13v1.0 Reference Assembly: https://www.ncbi.nlm.nih.gov/assembly/GCA_009914755.2


Links to other publicly accessible locations of the data:


GIAB FTP URL: https://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/release/AshkenazimTrio/HG002_NA24385_son/CMRG_v1.00 


Data.nist.gov DOI: Will update when DOI is available




---------------------
DATA & FILE OVERVIEW
---------------------




File list: 


```
.
├── CHM13v1.0
│   ├── SmallVariant
│   │   ├── HG002_CHM13v1.0_CMRG_smallvar_v1.00_draft.bed
│   │   ├── HG002_CHM13v1.0_CMRG_smallvar_v1.00_draft.vcf.gz
│   │   └── HG002_CHM13v1.0_CMRG_smallvar_v1.00_draft.vcf.gz.tbi
│   └── SupplementaryFiles
│           ├── HG002_CHM13_CMRG_smallvar_v1.00_GRCh38-equiv-regions_draft.bed
│           └── HG002v11-align2-CHM13v1.0
│               ├── HG002v11-align2-CHM13v1.0.dip.bed
│               ├── HG002v11-align2-CHM13v1.0.dip.vcf.gz
│               ├── HG002v11-align2-CHM13v1.0.dip.vcf.gz.tbi
│               ├── HG002v11-align2-CHM13v1.0.hap1.bam
│               ├── HG002v11-align2-CHM13v1.0.hap1.bam.bai
│               ├── HG002v11-align2-CHM13v1.0.hap2.bam
│               └── HG002v11-align2-CHM13v1.0.hap2.bam.bai
├── GRCh37
│   ├── SmallVariant
│   │   ├── HG002_GRCh37_CMRG_smallvar_v1.00.bed
│   │   ├── HG002_GRCh37_CMRG_smallvar_v1.00.vcf.gz
│   │   └── HG002_GRCh37_CMRG_smallvar_v1.00.vcf.gz.tbi
│   ├── StructuralVariant
│   │   ├── HG002_GRCh37_CMRG_SV_v1.00.bed
│   │   ├── HG002_GRCh37_CMRG_SV_v1.00.vcf.gz
│   │   └── HG002_GRCh37_CMRG_SV_v1.00.vcf.gz.tbi
│   └── SupplementaryFiles
│           ├── GRCh37_CMRG_benchmark_gene_coordinates.bed
│           └── HG002v11-align2-GRCh37
│               ├── HG002v11-align2-GRCh37.dip.bed
│               ├── HG002v11-align2-GRCh37.dip.vcf.gz
│               ├── HG002v11-align2-GRCh37.dip.vcf.gz.tbi
│               ├── HG002v11-align2-GRCh37.hap1.bam
│               ├── HG002v11-align2-GRCh37.hap1.bam.bai
│               ├── HG002v11-align2-GRCh37.hap2.bam
│               ├── HG002v11-align2-GRCh37.hap2.bam.bai
│               └── HG002v11-align2-GRCh37_report.html
├── GRCh38
│   ├── SmallVariant
│   │   ├── HG002_GRCh38_CMRG_smallvar_v1.00.bed
│   │   ├── HG002_GRCh38_CMRG_smallvar_v1.00.vcf.gz
│   │   ├── HG002_GRCh38_CMRG_smallvar_v1.00.vcf.gz.tbi
│   │   ├── HG002v11-align2-CHM13v1.0.dip.vcf.gz
│   │   └── HG002v11-align2-CHM13v1.0.dip.vcf.gz.tbi
│   ├── StructuralVariant
│   │   ├── HG002_GRCh38_CMRG_SV_v1.00.bed
│   │   ├── HG002_GRCh38_CMRG_SV_v1.00.vcf.gz
│   │   └── HG002_GRCh38_CMRG_SV_v1.00.vcf.gz.tbi
│   └── SupplementaryFiles
│           ├── GRCh38_CMRG_benchmark_gene_coordinates.bed
│           └── HG002v11-align2-GRCh38
│               ├── HG002v11-align2-GRCh38.dip.bed
│               ├── HG002v11-align2-GRCh38.dip.vcf.gz
│               ├── HG002v11-align2-GRCh38.dip.vcf.gz.tbi
│               ├── HG002v11-align2-GRCh38.hap1.bam
│               ├── HG002v11-align2-GRCh38.hap1.bam.bai
│               ├── HG002v11-align2-GRCh38.hap2.bam
│               ├── HG002v11-align2-GRCh38.hap2.bam.bai
│               └── HG002v11-align2-GRCh38_report.html
├── README_GIAB_medical_gene_benchmark.md
├── chksum.md5
└── hifiasm-assembly
        ├── HG002-v0.11.mat.fa.gz
        ├── HG002-v0.11.mat.gff.gz
        ├── HG002-v0.11.pat.fa.gz
        └── HG002-v0.11.pat.gff.gz
```


File Descriptions:  


* `*CMRG_smallvar_v1.00.bed`: bed file with small variant benchmark regions.
* `*CMRG_smallvar_v1.00.vcf.gz`: bgzipped vcf file with benchmark small variants.
* `*CMRG_SV_v1.00.bed`: bed file with structural variant benchmark regions.
* `*CMRG_SV_v1.00.vcf.gz`: bgzipped vcf file with benchmark structural variants.
* `*/SupplementaryFiles/*_CMRG_benchmark_gene_coordinates.bed`: Genomic coordinates for genes included in CMRG benchmark.
* `CHM13v1.0/SupplementaryFiles/HG002_CHM13_CMRG_smallvar_v1.00_GRCh38-equiv-regions_draft.bed`: CMRG benchmark regions for GRCh38 that are subset to regions directly lifting over from the CHM13 draft CMRG benchmark.
* `*/SupplementaryFiles/HG002v11-align2-*/`
   * `*-report.html`: snakemake report with dipcall pipeline run information.
   * `*.dip.bed`: BED file with fully diploid assembled regions generated by dipcall.
   * `*.dip.vcf.gz`: bgzipped vcf with combined phased small and structural variants generated by dipcall
   * `*.dip.vcf.gz.tbi`: index file for `*.dip.vcf.gz`
   * `*.hap1.bam`: dipcall generated BAM file with paternal haplotype aligned to the reference.
   * `*.hap2.bam`: dipcall generated BAM file with maternal haplotype aligned to the reference.
   * `*.bai`: index file for `*.hap1.bam` or `*.hap2.bam`.


--------------------------
METHODOLOGICAL INFORMATION
--------------------------


The basis of this benchmark is an HG002 trio-based assembly from hifiasm v0.11, with paternal and maternal fasta files available under hifiasm-assembly/. In addition, gff files were generated using Liftoff v1.4.0 with default parameters to lift over Ensembl v100 (https://useast.ensembl.org) annotations from GRCh38 onto each haplotype assembly separately. 


_Diploid Assembly Variant Calls and Regions_  
`{GRCh37,GRCh38,CHM13}/SupplementaryFiles/HG002v11-align2-{GRCh37,GRCh38,CHM13v1.0}/HG002v11-align2-*.dip*` were generated using the GIAB diploid assembly benchmarking pipeline (https://github.com/usnistgov/giab-asm-benchmarking) that uses dipcall (v0.1) to align the diploid assembly to a reference genome with minimap2 (mm2), and then  call variants and identify regions covered by both haplotypes. To increase mapping around structural variants and the MHC region, the -z parameter used by mm2 was modified from default to -z200000,10000 in the run-dipcall(v0.1) file (LN40). 


_CMRG Benchmarks_
The files `HG002_{GRCh37,GRCh38,CHM13}_CMRG_{smallvar,SV}_v1.00*` were generated as described in a draft manuscript in preparation which included identifying medical genes, finding the coverage in v4.2.1 compared to the diploid assembly, as well as analysis and manual curation of the assembly-based variant calls to understand the suitability as a benchmark.


_GRCh38 - CHM13 Equivalent_
The draft small variant benchmark covering comparable regions on GRCh38 and CHM13, was generated by creating a separate GRCh38 benchmark bed for this purpose at `CHM13v1.0/SupplementaryFiles/HG002_CHRM13_CMRG_smallvar_v1.00_GRCh38-equiv-regions_draft.bed`. This work will be described in the Aganezov et al T2T paper in preparation.


__Dependencies:__
hifiasm: https://github.com/chhylp123/hifiasm
Dipcall: https://github.com/lh3/dipcall
liftOff: https://github.com/agshumate/Liftoff


__Quality Assurance:__ 
The benchmarks were validated and refined by manually curating small and structural variant call disagreements between the GRCh37 and GRCh38 CMRG benchmark set and a number of variant callsets, see manuscript for details. The CHM13 benchmark was generated using the same process as the GRCh37 and GRCh38 benchmark but some genes and regions were excluded and it was not subjected to the same validation process so is therefore considered a draft benchmark.


-----------------------------------------
DATA-SPECIFIC INFORMATION: 
-----------------------------------------
_Bed file format:_ files are standard 3-field BED files (chromosome, start, end),http://genome.ucsc.edu/FAQ/FAQformat#format1. 
_VCF file format:_ https://samtools.github.io/hts-specs/VCFv4.2.pdf
_FASTA file format:_ https://www.ncbi.nlm.nih.gov/genbank/fastaformat/
_GFF file format:_ http://gmod.org/wiki/GFF3
_BAM file format:_ https://samtools.github.io/hts-specs/SAMv1.pdf


Data Use Policy
--------------------------------------------------------------------------------


This software was developed by employees of the National Institute of Standards and Technology (NIST), an agency of the Federal Government and is being made available as a public service. Pursuant to title 17 United States Code Section 105, works of NIST employees are not subject to copyright protection in the United States. This software may be subject to foreign copyright. Permission in the United States and in foreign countries, to the extent that NIST may hold copyright, to use, copy, modify, create derivative works, and distribute this software and its documentation without fee is hereby granted on a non-exclusive basis, provided that this notice and disclaimer of warranty appears in all copies.


THE SOFTWARE IS PROVIDED 'AS IS' WITHOUT ANY WARRANTY OF ANY KIND, EITHER EXPRESSED, IMPLIED, OR STATUTORY, INCLUDING, BUT NOT LIMITED TO, ANY WARRANTY THAT THE SOFTWARE WILL CONFORM TO SPECIFICATIONS, ANY IMPLIED WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND FREEDOM FROM INFRINGEMENT, AND ANY WARRANTY THAT THE DOCUMENTATION WILL CONFORM TO THE SOFTWARE, OR ANY WARRANTY THAT THE SOFTWARE WILL BE ERROR FREE. IN NO EVENT SHALL NIST BE LIABLE FOR ANY DAMAGES, INCLUDING, BUT NOT LIMITED TO, DIRECT, INDIRECT, SPECIAL OR CONSEQUENTIAL DAMAGES, ARISING OUT OF, RESULTING FROM, OR IN ANY WAY CONNECTED WITH THIS SOFTWARE, WHETHER OR NOT BASED UPON WARRANTY, CONTRACT, TORT, OR OTHERWISE, WHETHER OR NOT INJURY WAS SUSTAINED BY PERSONS OR PROPERTY OR OTHERWISE, AND WHETHER OR NOT LOSS WAS SUSTAINED FROM, OR AROSE OUT OF THE RESULTS OF, OR USE OF, THE SOFTWARE OR SERVICES PROVIDED HEREUNDER.