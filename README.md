# Lab 5 – Clustering Techniques Using DBSCAN and Hierarchical Clustering

This repository contains my work for **Lab 5**, where I applied **Agglomerative Hierarchical Clustering** and **DBSCAN** to the Wine dataset.  
The goal was to explore how clustering algorithms and parameter choices affect cluster formation, evaluation metrics, and visual interpretation.

## Summary of Results

### Hierarchical Clustering
- Tested **n_clusters = 2, 3, 4, 5**
- **Best result: 3 clusters** (Silhouette Score = **0.2774**)
- PCA visualizations showed clear separation at 3 clusters
- Dendrogram structure also indicated **three natural clusters**

### DBSCAN
- Parameter sweep:
  - `eps` ∈ {0.3, 0.5, 0.7, 0.9, 1.1}
  - `min_samples` ∈ {3, 5, 7, 10}
- **All points labeled as noise (-1)** for every configuration
- Metrics: Silhouette = NaN, Homogeneity = 0.0, Completeness = 1.0
- PCA visualizations showed no cluster formation

## Key Insights
- **Agglomerative Clustering** successfully identified meaningful structure consistent with known wine classes.
- **DBSCAN** failed to form clusters because the dataset lacks strong density-separated patterns.
- Clustering performance is highly sensitive to parameter choices.
- Hierarchical clustering is better suited to this dataset than DBSCAN.

## Repository Contents
- Jupyter Notebook (`.ipynb`) with all code and analysis  
- `README.md`

