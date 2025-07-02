# A-smart-framework-to-design-membranes-for-organic-micropollutants-removal
Organic micropollutants; machine  learning; data-mechanisms fusion

This repository contains several Jupyter notebooks related to the Data-Mechanism-Fused Molecular Representation Learning (DMF-MRL) framework, developed for understanding the removal mechanisms of organic micropollutants (OMPs) using polymeric membranes. Below is a description of each core module:
﻿
fragment_statistics.ipynb
This notebook performs functional group analysis for all OMPs in the dataset. Using SMARTS pattern matching via RDKit, it detects and counts the presence of key functional groups (e.g., hydroxyl, carboxyl, amine, sulfonic acid, etc.) across all SMILES-encoded molecular structures.
This provides a chemical basis for subsequent modeling and feature selection. Top 12 most frequent functional groups with their counts and SMARTS patterns.
﻿
correlation_analysis.ipynb
Given the large number of extracted molecular features, many of them exhibit high mutual correlation, which may hinder model interpretability and lead to overfitting.
This notebook computes pairwise Pearson correlation coefficients between all features, visualizes them using a heatmap, and identifies highly correlated feature pairs (|r| > 0.7).
Based on this analysis and chemical domain knowledge, redundant or less informative features are removed from the model input.
﻿
﻿
DMF-MRL.ipynb
This notebook implements the main machine learning pipeline under the DMF-MRL framework. It integrates both data-driven descriptors and mechanism-inspired molecular features to predict OMP removal performance.
It includes feature preprocessing, model training (XGBoost), evaluation metrics (e.g., R², RMSE), and interpretability modules, among others.
﻿
DMF-MRL-secondary substructures.ipynb
This notebook focuses on the secondary substructures within OMP molecules. It expands the DMF-MRL framework.
