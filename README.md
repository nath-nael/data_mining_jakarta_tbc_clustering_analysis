# Data Mining – Jakarta TBC Clustering Analysis

## 📚 Overview
This project analyzes the distribution of **Tuberculosis (TBC)** cases in **DKI Jakarta** using **Agglomerative Clustering** to identify priority areas for intervention.  
It combines TBC case data with **socio-economic indicators**, **population density**, and **health facility availability** to create meaningful regional groupings that can guide targeted public health strategies.

Conducted as part of the **Data Mining** course at **BINUS University**, the project applies the full data mining pipeline—from preprocessing to model evaluation—to produce actionable insights.

---

## 🎯 Background
- In 2023, Indonesia ranked **2nd worldwide** with **1,060,000 TBC cases** (WHO).
- Jakarta’s **high population density** and diverse socio-economic conditions increase the risk of TBC spread.
- Current prevention efforts are **not optimally targeted**, making **data-driven clustering** valuable for identifying vulnerable regions.

---

## 💡 Problem Statement
- How are TBC cases distributed across DKI Jakarta?
- What strategies are most effective given:
  - Socio-economic complexity.
  - Diverse regional characteristics.
- How can clustering improve intervention targeting?

---

## 🛠 Methodology

### 1. **Data Sources**
- **TBC Cases** per district/subdistrict.
- **Socio-economic indicators** (poverty rate, education level, basic facilities access).
- **Population density**.
- **Health facilities** availability.
- **Air Quality Index (ISPU)**.

### 2. **Preprocessing Steps**
- **Data integration** from multiple sources.
- **Data cleaning** (null handling: replace missing facility counts with 0).
- **Data transformation** with `RobustScaler` to reduce outlier influence.
- **Dimensionality reduction** via **PCA (2 components)** for noise reduction & visualization.

### 3. **Exploratory Data Analysis**
- Correlation matrix & heatmaps.
- Outlier detection with box plots.
- Feature distribution analysis.

### 4. **Clustering Algorithms Tested**
- **KMeans**: Good Silhouette Score (0.85) but poor spatial/socio-economic fit.
- **DBSCAN**: High Silhouette Score (0.86) but excluded many data points as outliers.
- **Agglomerative Clustering**: Best balance of interpretability and performance.

---

## 📊 Final Model
- **Algorithm**: Agglomerative Clustering
- **Parameters**: `distance_threshold=10` → 9 clusters
- **Silhouette Score**: **0.7817** (high cohesion & separation)
- **Result**: Logical regional grouping consistent with socio-economic and facility data.

---

## 🔍 Key Findings
- **Cluster 0**: Most areas, low TBC prevalence, high density, limited facilities.
- **Clusters 6 & 8**: Extremely high TBC prevalence, no specialized hospitals → urgent intervention needed.
- **Clusters 4 & 5**: High cases & prevalence, few/no health facilities.
- **Clusters 2 & 3**: Moderate cases, limited facilities.

---

## 📌 Policy Implications
- **Prioritization**: Direct resources to clusters with high cases & low facility access.
- **Resource Allocation**: Optimize distribution of health staff, medicines, and hospitals.
- **Public Transparency**: Improve awareness and community engagement.

---

## 📈 Visualization
Interactive dashboard (Tableau):  
[**TBC Clustering Distribution**](https://public.tableau.com/app/profile/matthew.nathanael/viz/TBCClusteringDistribution/Sheet1?publish=yes)

---

## 🛠 Tech Stack
- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- **PCA** for dimensionality reduction.
- **Agglomerative Clustering** from Scikit-learn.
- **Tableau** for visualization.

---
