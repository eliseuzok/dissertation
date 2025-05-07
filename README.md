Overview
This repository accompanies a project focused on identifying **homozygous deletions** in **single-cell DNA sequencing** (scDNA-seq) datasets, with a particular emphasis on breast cancer and osteosarcoma samples. It includes tools to simulate cancer genomes with deletions, develop an algorithm for detection, and apply this algorithm to real datasets.

📌 Project Aims
-Develop a computational method to accurately identify homozygous deletions in scDNA-seq cancer genomes.

-Apply this method to large scDNA-seq datasets to study the frequency and genomic distribution of homozygous deletions.

-Investigate whether tumor suppressor genes (TSGs) are enriched at these deletion sites.

🔬 Methodological Pipeline
1. In-Silico Simulation
Reference Genome (GRCh38): Downloaded and processed to exclude non-canonical chromosomes.

Normal Cell Creation: Simulated diploid genome generated with SNVs (using Mutation Simulator).

Tumour Cell Creation: Chromosome-wide deletions introduced (e.g., Chr2 for homozygous deletion, Chr17 for heterozygous).

Read Simulation: Paired-end sequencing simulated using ArtIllumina and aligned using BWA + Samtools.

Bin Counting: Reads binned at 5Mb, 500kb, and 50kb with Bedtools; RDRs calculated.

Threshold Derivation: Descriptive statistics used to define RDR thresholds indicative of homozygous deletions.

2. Dataset Analysis
Datasets: 6 scDNA-seq datasets (3 breast cancer [3 patients], 3 osteosarcoma [single patient]) processed via CHISEL, covering >17,000 cells.

Clustering & Visualization: Subclones and deletion patterns explored using clustering heatmaps, RDR profiles, and frequency plots.

TSG Enrichment: Deletion hotspots cross-referenced with TSGs using the COSMIC database.
