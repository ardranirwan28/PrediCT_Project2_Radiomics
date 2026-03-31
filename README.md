# PrediCT Project 2: Radiomics & Phenotyping

## Overview
This repository contains the complete pipeline for **Project 2 of PrediCT GSoC 2026**. The goal is to extract radiomics features from COCA cardiac CT scans and correlate them with **coronary calcium severity** (Agatston scores).

The project is divided into two main stages:
1. **Preprocessing & Feature Extraction**
2. **Analysis & Visualization**


## Instructions

1. Install the required Python packages (if not already installed):
```bash
pip install pyradiomics pydicom SimpleITK pandas numpy matplotlib seaborn scikit-learn

2. Place your COCA scans and masks in a folder of your choice (path should match notebooks).
3. Run 1_preprocessing_and_feature_extraction.ipynb first to extract radiomics features.
4. Run 2_analysis_and_visualization.ipynb to calculate Agatston scores, perform statistical analysis, and generate visualizations.

Features Extracted
- Shape: Sphericity, SurfaceVolumeRatio, Maximum3DDiameter
- GLCM: Contrast, Correlation, InverseDifferenceMoment
- GLSZM: SmallAreaEmphasis, LargeAreaEmphasis, ZonePercentage
- GLRLM: ShortRunEmphasis, LongRunEmphasis, RunPercentage
- Optional: Max/mean calcium HU, total volume

Analysis Performed:

- Correlation of radiomics features with Agatston scores using Spearman correlation
- Comparison across Agatston score categories using Kruskal-Wallis test
- Visualizations: heatmaps, scatter plots, and optional t-SNE/UMAP for phenotype clustering

Notes:

1. The radiomics_features_final.csv contains all extracted features along with Agatston scores for each scan.
2. All visualizations are contained within 2_analysis_and_visualization.ipynb.

