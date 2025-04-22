Finding signatures on saliva microbiota as a representative of oral microbiome, based on "enterosignature" concept introduced by Frioux et al. "https://linkinghub.elsevier.com/retrieve/pii/S1931312823002172"
1) Download sequence data files using SRA Toolkit: https://www.ncbi.nlm.nih.gov/sra/docs/sradownload/
2) quality control and adaptor trimming using Stag-mwc (https://stag-mwc.readthedocs.io/en/latest/overview.html)
3) bowtie2 > human referenece geneome (hg19) for host reads removal on config.yaml for stag-mwc
4) MetaPhlAn 4 : taxonomic annotation (database index : "mpa_vOct22_CHOCOPhlAnSGB_202212")
5) performing NMF algorithm to break down relative abundance matrix (healthy dataset) to W and H matrices
6) W matrix: representing each genera and their weight assigned to each signature
7) H matrix: proportion of each signature for each sample
8) find optimal number of K for NMF algorithm, finding signatures and perform analysis on the obtained signatures
9) [summary of project](https://github.com/dela-bam/saliva_signature_DB_LH/blob/main/summary_of_project.md) 

