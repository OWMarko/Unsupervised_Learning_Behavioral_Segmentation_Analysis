# Unsupervised Learning: Behavioral Segmentation Analysis

## Academic Integrity Notice
> **Note :** The full source code (`.R` scripts) and the dataset are **not included** in this repository. 
> This project is part of an active university curriculum at **Université Côte d'Azur**. To prevent plagiarism and preserve the integrity of the subject for future students, only the methodology and results are presented here.

## Project Overview
This project applies **Data Mining techniques** to a transactional dataset of 2,000 individuals. The goal was to extract hidden structures and identify distinct behavioral profiles without prior labeling (Unsupervised Learning).

From a technical perspective, the challenge lay in handling high-dimensional data (sparse transaction matrices) and validating the optimal number of clusters mathematically.

## Methodology

1.  **Pattern Mining (Association Rules) :**
    * Usage of the **Apriori Algorithm** to detect frequent itemsets.
    * Analysis of antecedents/consequents to map product correlations (e.g., *If X and Y are bought, probability of Z is 80%*).

2.  **Dimensionality Reduction & Visualization :**
    * **PCA (Principal Component Analysis)** for 2D projection.
    * **t-SNE** for 3D non-linear visualization to inspect cluster separation.

3.  **Clustering (K-Means) :**
    * Determination of optimal $K$ using **Elbow Method** and **Silhouette Analysis**.
    * **Sensitivity Analysis:** Compared $K=4$ vs $K=6$ clusters. The analysis proved that $K=6$ introduced noise (over-segmentation), validating $K=4$ as the robust model.

## Key Results
The algorithm successfully partitioned the dataset into 4 distinct, stable clusters based on purchasing behavior and socio-demographic proxies:
* **Cluster 1 (Budget/Students) :** High consumption of low-cost staples.
* **Cluster 2 (Volume/Families) :** Large basket sizes, focused on bulk food items.
* **Cluster 3 (Quality/Seniors) :** High average basket value, focused on fresh/bio products.
* **Cluster 4 (Premium) :** Niche consumption patterns with high income correlation.

## Tech Stack
* **Language :** R
* **Key Libraries :** `arules` (Mining), `factoextra` (Visualization), `cluster` (K-Means), `tsne` (3D projection), `ggplot2`.

---
*For any questions regarding the clustering validation methods or the t-SNE parameters used, feel free to contact me.*
