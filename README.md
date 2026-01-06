# Global-Socio-Economic-An-Unsupervised-Learning-Analysis

## Project Overview

This project maps the global socio-economic landscape using a dual-stage unsupervised learning pipeline. By synthesizing **38 indicators across 204 nations**, the study identifies the latent factors driving international disparities. The analysis moves beyond raw GDP to incorporate dimensions like digitalization, human welfare, and demographic transitions.

The methodology follows the **Jaadi (2019) Seven-Step Roadmap** for dimensionality reduction and cluster validation.

---

## Key Features

* **Dimensionality Reduction**: Utilized Principal Components Analysis (PCA) to reduce 38 correlated variables into 14 Principal Components, retaining **89% of the total variance**.
* **Multi-Dimensional Clustering**: Implemented a hybrid approach using **K-Means** and **Ward’s Hierarchical Clustering**.
* **Cluster Validation**: Optimal cluster selection () was determined using the Elbow Method, Silhouette Score, and Gap Statistic.
* **Global Stratification**: Identified four distinct global "Tiers" based on socio-economic maturity rather than just geographic location.

---

## Technical Workflow

### 1. Data Preprocessing

* **Imputation**: Handled missing values using median imputation to preserve global distributions.
* **Standardization**: Applied `StandardScaler` to ensure features with different units (e.g., USD vs. percentages) contribute equally to the covariance matrix.
* **Outlier Handling**: Addressed extreme skewness in variables like Population Density and  emissions.

### 2. PCA & Factor Discovery

The analysis revealed two primary axes of global development:

* **PC1 (33.7% Variance) - The Modernization Axis**: Driven by internet usage, life expectancy, and secondary enrollment.
* **PC2 (14.6% Variance) - The Scale Axis**: Driven by total GDP, land area, and  emissions.

### 3. Clustering Results (The 4-Tier Model)

Using Hierarchical Clustering with Ward's linkage, the world naturally splits into four socio-economic categories:

| Tier | Identity | Primary Characteristics |
| --- | --- | --- |
| **Tier 1** | **Global Super-Powers** | Extreme economic scale, massive industrial output, and large landmass. |
| **Tier 2** | **Advanced Economies** | High social welfare, >61% internet penetration, and service-oriented labor markets. |
| **Tier 3** | **Emerging Markets** | Rapid urbanization, high fertility rates, and transitioning industrial bases. |
| **Tier 4** | **Frontier Economies** | Early demographic transitions, high agricultural employment, and lower secondary enrollment. |

---

## Technologies Used

* **Python 3.x**
* **Data Analysis**: `pandas`, `numpy`
* **Machine Learning**: `scikit-learn` (PCA, KMeans, AgglomerativeClustering)
* **Visualization**: `matplotlib`, `seaborn`
* **Statistics**: `scipy` (Hierarchical linkage and dendrograms)

---

## Conclusions

The research demonstrates that global stratification is a multi-dimensional phenomenon. A nation's "Global Footprint" (Scale) is mathematically distinct from its "Human Development" (Welfare). By separating the **Economic Giants** (Cluster 1) from **High-Welfare States** (Cluster 2), this model provides a more nuanced framework for international development policy than traditional GDP rankings.
