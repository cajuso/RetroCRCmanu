# RetroCRCmanu
This repository contains software used in the manuscript entitled “Retrotransposon insertions can initiate colorectal cancer and are associated with poor survival” (https://www.biorxiv.org/content/10.1101/443580v1). 

Genomic instability pathways in colorectal cancer (CRC) have been extensively studied, but the role of retrotransposition in colorectal carcinogenesis remains poorly understood. Although retrotransposons are usually repressed, they become active in several human cancers, in particular those of the gastrointestinal tract. Here we characterize retrotransposon insertions in 202 colorectal tumor whole genomes and investigate their associations with molecular and clinical characteristics. We found highly variable retrotransposon activity among tumors and identified recurrent insertions in 15 known cancer genes. In approximately 1% of the cases we identified insertions in APC, likely to be tumor-initiating events. Insertions were positively associated with the CpG island methylator phenotype and the genomic fraction of allelic imbalance. Clinically, high number of insertions was independently associated with poor disease-specific survival.

The scripts included in this repository are: 

* Aaltonen_scripts @ 29fc269: Script utilized to call the polyA/T from the insertion calls. 

* jsva @ d614039: Script utilized to join the structural variant calls and used as an input in the transduction_detection.py

* Manuscript_23012019: R Code utilized to produce Figures 1-3 and 5-6, Multiple Linear model and Cox Proportional Hazards model.

* Transduction_detection.py: The script uses as an input the output from the JSVA script to detect candidate transduction calls. The script will detect transduction calls based on the proximity of JSVA calls to a list of full-length reference L1 elements taking into account their orientation. The JSVA script should be run in the following order:

  1.	merge_sv_event.py
  2.	split_into_breakpoints.sh
  3.	annotate_breakpoints.sh
  4.	unravel.py

