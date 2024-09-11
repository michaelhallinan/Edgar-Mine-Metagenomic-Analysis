# Metagenomic Analysis of Subsurface Microbial Communities in the Edgar Experimental Mine

## Overview

This repository contains the code, data, and results of a metagenomic analysis project exploring the composition and diversity of microbial communities within the Edgar Experimental Mine in Idaho Springs, CO. The study was conducted to identify dominant and rare taxa, assess community richness, and infer functional roles based on 16S rRNA gene sequencing data collected across different substrates within the mine.

## Background and Motivation

Subsurface environments like the Edgar Experimental Mine harbor unique microbial communities that are integral to biogeochemical cycles. Understanding both the composition and function of these communities is crucial for gaining insights into their ecological roles and potential applications in various fields, including biotechnology and environmental remediation. This study aims to address current knowledge gaps concerning microbial life in extreme environments by characterizing microbial diversity across multiple locations within the mine over time. Specifically, we aim to identify dominant and rare taxa, assess community richness, and infer the functional roles of these organisms. By doing so, we hope to inform future research efforts and applications within the Edgar Experimental Mine, as well as identify unique microbial species that may hold biotechnological potential or be worth further exploration for their novel properties.

## Data Collection

Samples were collected from the Edgar Experimental Mine at two time points: June 2023 and June 2024 in a few various locations such as:
- Cave walls & boreholes 
- Rubber tubing throughout the Mine
- Subterranean water

<div align="center">
  <table>
    <tr>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/20291a35-8ded-42fd-973f-c6d83c50c579" alt="Image 1" width="150"><br>
        <p>Figure 1: Example of cave flooring from 2024 data</p>
      </td>
      <td align="center">
        <img src="https://github.com/user-attachments/assets/3644aaad-1c13-4ce7-a56b-c3e538bf10a9" alt="Image 2" width="150"><br>
        <p>Figure 2: Example of boreholes from 2023 data</p>
      </td>
    </tr>
  </table>
</div>

Both sets of samples were initially processed using the ZymoBIOMICS DNA Miniprep Kit. The DNA was then quantified and analyzed with the Qubit double-stranded DNA (dsDNA) high-sensitivity assay. To amplify the 16S rRNA gene, we employed the AcuuStar II PCR ToughMix and qScript XLT One-Step RT-PCR methodology, ensuring high yield and purity suitable for downstream analysis, as outlined by Parada et al. (2016).

For sequencing, the 2024 samples were processed with the Oxford Mk1B MinION nanopore, while the 2023 samples were sequenced at the Microbiome Core Facility, Duke Center for Genomic and Computational Biology, utilizing Illumina next-generation sequencing (NGS) technology.

# Data Processing and Analysis
### Data Preprocessing
- **Quality filtering and trimming of raw reads** using DADA2.
- **OTU picking and taxonomic assignment** using the SILVA database with the DADA2 pipeline.

### Diversity Analysis
- **Alpha diversity** (e.g., Shannon index) and **beta diversity** (e.g., Bray-Curtis dissimilarity) were calculated using `phyloseq` and `vegan`.
  
### Statistical Analysis

- **Differential abundance analysis** was performed using `DESeq2` to identify taxa significantly associated with different sample types.

### Functional Predictions

- **Functional pathway predictions** were inferred using **PICRUSt** (Phylogenetic Investigation of Communities by Reconstruction of Unobserved States).
  
### Metagenomic Analysis
- For the 2023 data, the DADA2 pipeline was used for 16S rRNA gene analysis, focusing on identifying exact sequence variants (ASVs) and performing taxonomic assignments to characterize microbial communities based on their genetic sequences.
- - For the 2024 data, downstream metagenomic analysis was conducted using EPI2ME What's In My Pot (WIMP).
---

# Tools and Software

- **DADA2**: Used for quality control, trimming, and taxonomic assignment.
- **phyloseq & vegan**: Used for diversity analysis.
- **DESeq2**: Used for differential abundance analysis.
- **PICRUSt**: Used for functional predictions of microbial communities.
- **EPI2ME**: Used for metagenomic analysis and community functional profiling.

---

## Results

### Key Findings
- **Dominant Taxa**: Analysis revealed **Proteobacteria** as the dominant microbial phylum in both the 2023 and 2024 datasets, representing over 77% of the total community composition. Other phyla such as **Actinobacteria**, **Ascomycota**, and **Nitrospirota_A** were detected sporadically.
- **Rare Taxa**: Several rare taxa, including **Chordata** and **Firmicutes_A**, were identified. Notably, **Firmicutes_A** exhibited a statistically significant correlation with temperature (Pearson’s correlation coefficient = 0.51, p = 0.0317), although the small sample size limited the robustness of this conclusion.
- **Community Richness**: Variations in microbial community richness were observed across different substrates (boreholes vs. surface samples) and time points (2023 vs. 2024). The Shannon Index revealed greater diversity in high-count samples from the 2024 data, while 2023 samples demonstrated consistent diversity regardless of read counts.

### Visualizations

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/ccf220a6-aa6b-47eb-8e02-6ae16b39e491" alt="Figure 3: Heatmap of Phylum Abundance by Temperature at all 2024 sites" width="300px">
      <br><b>Figure 3. Heatmap of Phylum Abundance by Temperature at all 2024 sites.</b>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/a15aad1f-6063-4110-b621-8250837795f8" alt="Figure 4: Heatmap describing total log counts for different genera in the 2023 sample" width="300px">
      <br><b>Figure 4: Heatmap describing total log counts for different genera in the 2023 sample.</b>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <img src="https://github.com/user-attachments/assets/7d6bf2fd-cecf-4748-83ad-9fceb30ed559" alt="Figure 5: Graphical representation of the top 10% of all identified pathways" width="600px">
      <br><b>Figure 5: Graphical representation of the top 10% of all identified pathways compared to Average Community-Wide Abundances for 2023 Samples.</b>
    </td>
  </tr>
</table>



## Conclusions

The results of this study offer significant insights into the **microbial ecology** of subsurface environments, particularly within the Edgar Mine. The **dominant taxa**, including **Proteobacteria**, play key roles in the ecological functioning of these habitats. Meanwhile, the detection of **rare taxa** suggests specialized functions that could offer deeper understanding in microbial adaptation to extreme conditions.

The variance in **community richness** and diversity between borehole and surface samples, as well as between the 2023 and 2024 datasets, highlights the potential influence of both **spatial and temporal dynamics**. 

The application of **PICRUSt2** and **EPI2ME What's In My Pot** enabled a broader understanding of microbial functional pathways, with common pathways such as **aerobic respiration** and **glucose degradation** identified alongside specialized pathways like **sulfoglycolysis**.

These findings have potential applications in areas such as **environmental remediation**, where understanding the microbial population's response to specific conditions can inform sustainable practices. Further research will need to expand sample collections, refine analysis techniques, and apply identical sequencing methods to ensure robust, comparable results across datasets.
