This README_PacBio-CCS_HudsonAlpha_HG005.md was generated on 2020-10-29 by Nate Olson.
Updated: 2021-06-21 by Sierra D. Miller

GENERAL INFORMATION
--------------------------------------------------------------------------------

Title of Dataset: GIAB HG005 PacBio CCS

Author Information
  Principal Investigator: Justin Zook (jzook@nist.gov)
  Nate Olson (nathanael.olson@nist.gov)
  Jennifer McDaniel
  Jane Grimwood, HudsonAlpha
  Jeremy Schmutz, HudsonAlpha

Date of data collection : 03-03-2019 to 07-30-2020

SHARING/ACCESS INFORMATION
--------------------------------------------------------------------------------

Licenses/restrictions placed on the data, or limitations of reuse: CC0,
full NIST data use policy at the end of this document


Recommended citation for the data:
  Zook, J., Catoe, D., McDaniel, J. et al. Extensive sequencing of seven human
  genomes to characterize benchmark reference materials. Sci Data 3, 160025 (2016).
  https://doi.org/10.1038/sdata.2016.25


Links to publicly accessible locations of the data:

- NIH hosted GIAB ftp site: ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data/ChineseTrio/HG005_NA24631_son/HudsonAlpha_PacBio_CCS/
- SRA: Reads accessioned on SRA under PRJNA200694, specific run accession numbers below. 



DATA & FILE OVERVIEW
--------------------------------------------------------------------------------

File List:

```
├── PBmixSequel788_1_A01_PBXX_30hours_19kbV2PD_70pM_HumanHG005_CCS
│   ├── PBmixSequel788_1_A01_PBXX_30hours_19kbV2PD_70pM_HumanHG005.stats
│   ├── m64109_200304_195708.ccs_report.txt
│   └── m64109_200304_195708.fastq.gz
├── PBmixSequel789_1_A01_PBXW_30hours_15kbV2PD_70pM_HumanHG005_CCS
│   ├── PBmixSequel789_1_A01_PBXW_30hours_15kbV2PD_70pM_HumanHG005.stats
│   ├── m64109_200309_192110.ccs_report.txt
│   └── m64109_200309_192110.fastq.gz
├── PBmixSequel789_2_B01_PBXX_30hours_19kbV2PD_70pM_HumanHG005_CCS
│   ├── PBmixSequel789_2_B01_PBXX_30hours_19kbV2PD_70pM_HumanHG005.stats
│   ├── m64109_200311_013444.ccs_report.txt
│   └── m64109_200311_013444.fastq.gz
├── PBmixSequel840_1_A01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS
│   ├── PBmixSequel840_1_A01_PCCD_30hours_15kbV2PD_70pM_HumanHG005.stats
│   ├── m64017_200723_190224.ccs_report.txt
│   └── m64017_200723_190224.fastq.gz
├── PBmixSequel842_1_A01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS
│   ├── PBmixSequel842_1_A01_PCCD_30hours_15kbV2PD_70pM_HumanHG005.stats
│   ├── m64017_200730_190124.ccs_report.txt
│   └── m64017_200730_190124.fastq.gz
├── PBmixSequel842_2_B01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS
│   ├── PBmixSequel842_2_B01_PCCD_30hours_15kbV2PD_70pM_HumanHG005.stats
│   ├── m64017_200801_011415.ccs_report.txt
│   └── m64017_200801_011415.fastq.gz
├── PBmixSequel842_3_C01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS
│   ├── PBmixSequel842_3_C01_PCCD_30hours_15kbV2PD_70pM_HumanHG005.stats
│   ├── m64017_200802_073944.ccs_report.txt
│   └── m64017_200802_073944.fastq.gz
├── README_PacBio-CCS_HudsonAlpha_HG005.md
└── checksum.md5_fq
```


File Types:

* fastq.gz: consensus basecall files
* ccs_report.txt: consensus sequence basecall summary report
* stats: read length distribution for consensus sequence basecall files

Data files are in sub-directories by flowcell.


METHODOLOGICAL INFORMATION
--------------------------------------------------------------------------------

Sequencing and consensus basecalling was performed at the HudsonAlpha Genome Sequencing Center (https://hudsonalpha.org/gsc/).


SAMPLE: HG005 genomic DNA, NIST RM8393 https://www-s.nist.gov/srmors/view_detail.cfm?srm=8393

SEQUENCING METHODS
    Shearing        25 kb with Megaruptor
    Sequencing      Sequel II System with 2.0 chemistry
    Run time        30 hrs per SMRT Cell
    CCS             "Circular Consensus Sequencing" analysis in SMRT Link v8.0 (ccs 4.0.0)

    15 kb Library
        Library prep    TPK 1.0
        Size selection  SageELF Fraction 4 (target: 18 kb)
    20 kb Library
        Library prep    SMRTbell Express 2.0 + Enzyme Clean Up
        Size selection  SageELF Fraction 2 (target: 20 kb)

SEQUENCING RESULTS
    Reads are available on SRA. (Will update README when these are available.)

    15 kb Library
      PBmixSequel789_1_A01_PBXW_30hours_15kbV2PD_70pM_HumanHG005_CCS/m64109_200309_192110.fastq.gz     SRX11174566
      PBmixSequel840_1_A01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS/m64017_200723_190224.fastq.gz     SRX11174567
      PBmixSequel842_1_A01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS/m64017_200730_190124.fastq.gz     SRX11174578
      PBmixSequel842_2_B01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS/m64017_200801_011415.fastq.gz     SRX11174584
      PBmixSequel842_3_C01_PCCD_30hours_15kbV2PD_70pM_HumanHG005_CCS/m64017_200802_073944.fastq.gz     SRX11174585
    20 kb Library
      PBmixSequel788_1_A01_PBXX_30hours_19kbV2PD_70pM_HumanHG005_CCS/m64109_200304_195708.fastq.gz     SRX11174586
      PBmixSequel789_2_B01_PBXX_30hours_19kbV2PD_70pM_HumanHG005_CCS/m64109_200311_013444.fastq.gz     SRX11174587


Quality-assurance procedures performed on the data:
Initial quality assurance was performed as part of the circular consensus
basecalling. Summary statistics are provided by flowcell in the
`[flowcell]_CCS` directories.


NIST Data Use Policy
--------------------------------------------------------------------------------


This data/work was created by employees of the National Institute of Standards
and Technology (NIST), an agency of the Federal Government. Pursuant to title 17
United States Code Section 105, works of NIST employees are not subject to
copyright protection in the United States.  This data/work may be subject to
foreign copyright.


The data/work is provided by NIST as a public service and is expressly provided
â€œAS IS.â€ NIST MAKES NO WARRANTY OF ANY KIND, EXPRESS, IMPLIED OR STATUTORY,
INCLUDING, WITHOUT LIMITATION, THE IMPLIED WARRANTY OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE, NON-INFRINGEMENT AND DATA ACCURACY. NIST does
not warrant or make any representations regarding the use of the data or the
results thereof, including but not limited to the correctness, accuracy,
reliability or usefulness of the data. NIST SHALL NOT BE LIABLE AND YOU HEREBY
RELEASE NIST FROM LIABILITY FOR ANY INDIRECT, CONSEQUENTIAL, SPECIAL, OR
INCIDENTAL DAMAGES (INCLUDING DAMAGES FOR LOSS OF BUSINESS PROFITS, BUSINESS
INTERRUPTION, LOSS OF BUSINESS INFORMATION, AND THE LIKE), WHETHER ARISING IN
TORT, CONTRACT, OR OTHERWISE, ARISING FROM OR RELATING TO THE DATA (OR THE USE
OF OR INABILITY TO USE THIS DATA), EVEN IF NIST HAS BEEN ADVISED OF THE
POSSIBILITY OF SUCH DAMAGES.


To the extent that NIST may hold copyright in countries other than the United
States, you are hereby granted the non-exclusive irrevocable and unconditional
right to print, publish, prepare derivative works and distribute the NIST data,
in any medium, or authorize others to do so on your behalf, on a royalty-free
basis throughout the world.


You may improve, modify, and create derivative works of the data or any portion
of the data, and you may copy and distribute such modifications or works.
Modified works should carry a notice stating that you changed the data and
should note the date and nature of any such change. Please explicitly
acknowledge the National Institute of Standards and Technology as the source of
the data:
Data citation recommendations are provided at https://www.nist.gov/open/license.


Permission to use this data is contingent upon your acceptance of the terms of
this agreement and upon your providing appropriate acknowledgments of NISTâ€™s
creation of the data/work.