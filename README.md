# Kernel PCA for Nonlinear Dimensionality Reduction and AML Classification

This project applies **Kernel Principal Component Analysis (KPCA)**, **Independent Component Analysis (ICA)**, and **Support Vector Machine (SVM)** classification to investigate nonlinear relationships between environmental pollutant exposures and Acute Myeloid Leukemia (AML) outcomes.

The goal is to explore whether complex mixtures of air pollutants exhibit latent structures that can help distinguish between AML-positive and AML-negative cases.

---

## Project Overview

High-dimensional environmental exposure data often contain nonlinear relationships that are not well captured by traditional linear methods. This project addresses that limitation by applying:

- Kernel PCA (nonlinear dimensionality reduction)
- ICA (latent independent signal separation)
- SVM (supervised classification)

---

## Dataset Description

The dataset consists of individual-level exposure measurements to air pollutants:

**Pollutants used as features:**
- PAH
- 1,3-Butadiene
- O-Xylene
- Benzene
- Toluene
- Styrene
- p-dichloro
- Chloroform

**Outcome variable:**
- AMLoutcome  
  - 0 = No AML  
  - 1 = AML

> Note: The dataset is not publicly redistributed. The analysis pipeline is applicable to any similarly structured multivariate exposure dataset.

---

## Methodology

### 1. Data Preprocessing
- Feature selection of pollutant variables
- Z-score standardization to ensure equal scaling across variables

### 2. Kernel PCA (KPCA)
- Applied RBF kernel to capture nonlinear structure
- Reduced high-dimensional exposure space into principal components
- Examined explained variance to determine optimal dimensionality

### 3. Variable Loadings
- Estimated feature contributions to principal components
- Identified pollutants contributing most strongly to latent structure

### 4. SVM Classification
- GridSearchCV used for hyperparameter tuning
- Compared linear and RBF kernels
- Evaluated classification performance in reduced feature space

### 5. Independent Component Analysis (ICA)
- Applied to KPCA-transformed features
- Extracted statistically independent components
- Assessed pollutant contributions via correlation analysis

---

## Key Outputs

- Cumulative explained variance curve (KPCA)
- 2D KPCA projection of samples
- SVM decision boundary visualization
- ICA component scatter plot
- Feature loading and correlation matrices

---

## Key Insight

The workflow demonstrates how nonlinear dimensionality reduction can uncover latent exposure patterns in environmental mixtures that may not be visible through linear methods alone.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## 📁 Repository Structure
