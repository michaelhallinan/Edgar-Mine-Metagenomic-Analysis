# Metagenomic Analysis of Subsurface Microbial Communities in the Edgar Experimental Mine

## Overview

This repository contains the code, data, and results of a metagenomic analysis project exploring the composition and diversity of microbial communities within the Edgar Experimental Mine in Idaho Springs, CO. The study was conducted to identify dominant and rare taxa, assess community richness, and infer functional roles based on 16S rRNA gene sequencing data collected across different substrates within the mine.

## Background and Motivation

Subsurface environments like the Edgar Experimental Mine harbor unique microbial communities that are integral to biogeochemical cycles. Understanding both the composition and function of these communities is crucial for gaining insights into their ecological roles and potential applications in various fields, including biotechnology and environmental remediation. This study aims to address current knowledge gaps concerning microbial life in extreme environments by characterizing microbial diversity across multiple locations within the mine over time. Specifically, we aim to identify dominant and rare taxa, assess community richness, and infer the functional roles of these organisms. By doing so, we hope to inform future research efforts and applications within the Edgar Experimental Mine, as well as identify unique microbial species that may hold biotechnological potential or be worth further exploration for their novel properties.

## Data Collection

Samples were collected from the Edgar Experimental Mine at two time points: June 2023 and June 2024. The locations within the mine included:
- Cave walls & boreholes 
- Rubber tubing throughout the Mine
- Subterranean water

These samples were subjected to 16S rRNA gene analysis to explore the microbial diversity and community structure across different substrates and time points.



## Methodology

### Data Processing and Analysis
The following pipeline was used to process and analyze the 16S rRNA gene sequencing data:

1. **Data Preprocessing**
   - Quality filtering and trimming of raw reads using [Tool X].
   - OTU picking and taxonomic assignment using [Tool Y].

2. **Diversity Analysis**
   - Alpha diversity (e.g., Shannon index) and beta diversity (e.g., Bray-Curtis dissimilarity) were calculated using [Tool Z].

3. **Statistical Analysis**
   - Differential abundance analysis was performed using [Tool A] to identify taxa significantly associated with different sample types.

### Tools and Software
- **Tool X**: Used for quality control and trimming.
- **Tool Y**: Used for OTU picking and taxonomic assignment.
- **Tool Z**: Used for diversity analysis.
- **Tool A**: Used for statistical analysis.

## Results

### Key Findings
- **Dominant Taxa**: Identified dominant microbial taxa across the different sample types.
- **Rare Taxa**: Several rare taxa were identified, which may have unique functional roles within the subsurface environment.
- **Community Richness**: Variations in microbial community richness were observed across different substrates and time points.

### Visualizations
- [Link to Figure 1](#) - OTU Distribution Across Sample Types
- [Link to Figure 2](#) - Alpha Diversity Across Time Points

## Conclusions

The results of this study provide valuable insights into the microbial ecology of subsurface environments. The identified taxa and their inferred functional roles contribute to our understanding of how microbial communities adapt to extreme conditions. These findings have potential applications in areas such as environmental remediation and biotechnology.

## Installation and Requirements

To replicate this analysis, follow these steps:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/YourUsername/Edgar-Mine-Metagenomics.git
