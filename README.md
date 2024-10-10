#Galaxy Server Introduction

Galaxy is a free, online platform for analyzing and integrating biological data. 
*It was created by scientists at Penn State, Johns Hopkins, OHSU, and Cleveland Clinic, with contributions from many others. 
*Galaxy has a large and active community of users who provide support and feedback.

#Data Can be uploaded to the Galaxy server using the upload button in the form of .fastq files.

#Quality Control of the Raw RNA Reads

FastQC aims to provide a simple way to do quality control checks on raw sequence data from high throughput sequencing pipelines. It offers a set of analyses that you can use to get a quick impression of whether your data has any problems that you should be aware of before doing any further analysis.
-Reads Quality
-Total GC Content
-Per base sequence content
-adapter sequence
-overrepresented sequence

#Trimming 

fastp is a tool designed to provide fast all-in-one preprocessing for FASTQ files.
-Comprehensive filtering: Removes low-quality, short, and N-rich reads.
-Efficient trimming: Trims low-quality bases and adapters using sliding windows.
-Base correction: Improves accuracy for paired-end reads.
-UMI handling: Prepares data for downstream analysis.
-Flexible output: Generates JSON and HTML reports for easy interpretation and visualization.
-Scalability: Supports parallel processing with multiple output files.
-Versatility: Handles both short and long reads.

#Alignment with the Reference Genome

HISAT is a fast and sensitive spliced alignment program. 
-Input files are the filtered files from fastp.
-Output files are in BAM/SAM format.

#Data Sorting

samtools idxstats is a command-line tool used to extract and display statistical information from a sorted and indexed BAM file. It generates a table with four columns:
-Reference sequence identifier: The unique name of each reference sequence.
-Reference sequence length: The total length of the reference sequence in base pairs.
-Number of mapped reads: The count of reads that have been aligned to the reference sequence.
-Number of placed but unmapped reads: The count of reads that have been assigned to a reference sequence but are not considered mapped (often unmapped pairs of mapped reads).

#Gene Quantification

HTSeq-count is a tool that analyzes alignment files (SAM or BAM format) and feature files (GFF format) to determine how many reads map to each genomic feature. 
It uses the HTSeq Python module to perform this calculation.

#Differential Gene Expression

DESeq2 Analysis was performed using R-Studio packages. DESeq2 is a software package used for analyzing count data, such as RNA sequencing data. 
*It normalizes the data, creates visualizations, and identifies differences between groups. 
*DESeq2 uses a statistical method called empirical Bayes to estimate certain parameters and calculate posterior estimates, which are used to identify significant differences.
-DESeq2
-BiocManager
-Tidyverse
-ggplots2

#Gene Set Enrichment Analysis

GSEA can be performed using various web-based servers.
-Cytoscape
-DAVID
-Enrichr
-ToppGene
