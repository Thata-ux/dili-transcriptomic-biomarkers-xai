# Transcriptomic Biomarker Discovery for Drug-Induced Liver Injury Using Explainable Machine Learning

![Python](https://img.shields.io/badge/Python-3.10-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-XGBoost-orange)
![Explainable AI](https://img.shields.io/badge/XAI-SHAP-red)
![Status](https://img.shields.io/badge/Status-Manuscript%20Submitted-success)

---

## Overview

This repository contains the complete computational workflow accompanying the manuscript:

> **Transcriptomic Biomarker Discovery for Drug-Induced Liver Injury in Rat Liver through Explainable Machine Learning with Independent DrugMatrix Validation**

The project presents an explainable machine learning framework for identifying transcriptomic biomarkers associated with **drug-induced liver injury (DILI)**. Differential gene expression analysis, feature selection, machine learning, explainable artificial intelligence (XAI), biological enrichment analysis, and independent external validation were integrated into a single reproducible workflow.

---

# Abstract

Drug-induced liver injury (DILI) remains one of the major causes of drug development failure and post-marketing withdrawal. Early identification of hepatotoxic compounds is therefore essential for improving drug safety.

This repository provides the complete computational pipeline used to identify transcriptomic biomarkers of hepatotoxicity using the Open TG-GATEs toxicogenomic database and independent validation with DrugMatrix (GSE57815). The workflow integrates differential expression analysis, Random Forest feature selection, XGBoost classification, SHAP explainability, Gene Ontology enrichment, KEGG pathway analysis, and external validation to identify biologically interpretable biomarkers for preclinical drug safety assessment.

---

# Workflow

The complete analysis pipeline consists of the following steps:

```
Open TG-GATEs
        │
        ▼
Data preprocessing
        │
        ▼
Differential Expression Analysis
        │
        ▼
531 Differentially Expressed Genes
        │
        ▼
Random Forest Feature Selection
        │
        ▼
Top 100 Genes
        │
        ▼
Machine Learning Models
(RF • XGBoost • LightGBM)
        │
        ▼
Model Evaluation
        │
        ▼
SHAP Explainability
        │
        ▼
GO & KEGG Enrichment
        │
        ▼
Independent DrugMatrix Validation
        │
        ▼
Validated Biomarker Panel
```

---

# Features

The repository includes:

- Differential gene expression analysis
- Random Forest feature selection
- XGBoost classification
- Random Forest classification
- LightGBM classification
- SHAP explainability
- Gene Ontology enrichment analysis
- KEGG pathway enrichment analysis
- External validation using DrugMatrix
- ROC analysis
- Precision-Recall analysis
- Bootstrap confidence intervals
- Permutation testing
- DeLong statistical comparison
- Supplementary table generation

---

# Datasets

## Discovery Dataset

**Open TG-GATEs**

https://toxico.nibiohn.go.jp/

- Species: Rat
- Tissue: Liver
- Platform: Affymetrix Rat230_2 (GPL1355)

---

## External Validation Dataset

**DrugMatrix**

GEO Accession:

GSE57815

https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE57815

- Species: Rat
- Tissue: Liver
- Platform: GPL1355

---

# Repository Structure

```
dili-transcriptomic-biomarkers-xai
│
├── analysis_pipeline.ipynb
├── requirements.txt
├── README.md
├── LICENSE
├── .gitignore
│
└── supplementary
    ├── Supplementary Table S1.csv
    ├── Supplementary Table S2.csv
    ├── Supplementary Table S3.csv
    ├── Supplementary Table S4.csv
    └── Supplementary Table S5.csv
```

---

# Software Requirements

Python 3.10+

Required packages:

- numpy
- pandas
- scipy
- scikit-learn
- xgboost
- lightgbm
- shap
- matplotlib
- gseapy
- statsmodels
- joblib

Install all dependencies using:

```bash
pip install -r requirements.txt
```

---

# How to Run

1. Clone this repository

```bash
git clone https://github.com/Thata-ux/dili-transcriptomic-biomarkers-xai.git
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Download the Open TG-GATEs dataset.

4. Download the DrugMatrix dataset (GSE57815).

5. Update dataset paths in:

```
analysis_pipeline.ipynb
```

6. Execute all notebook cells sequentially.

---

# Expected Outputs

Running the notebook will generate:

- Differentially expressed genes (DEGs)
- Random Forest feature importance
- Top 100 selected genes
- XGBoost prediction model
- ROC Curve
- Precision-Recall Curve
- Confusion Matrix
- SHAP Summary Plot
- SHAP Feature Importance Plot
- GO enrichment results
- KEGG enrichment results
- DrugMatrix validation results
- Biomarker panel evaluation
- Supplementary tables

---

# Machine Learning Pipeline

Algorithms evaluated:

- Random Forest
- XGBoost
- LightGBM

Evaluation metrics:

- ROC-AUC
- Precision-Recall AUC
- Accuracy
- Balanced Accuracy
- Matthews Correlation Coefficient
- Sensitivity
- Specificity

Statistical evaluation:

- Bootstrap Confidence Interval
- Repeated Stratified Cross Validation
- Permutation Test
- DeLong Test

---

# Reproducibility

This repository contains all scripts required to reproduce the analyses reported in the accompanying manuscript.

To improve reproducibility:

- Random seeds were fixed where applicable.
- Feature selection was performed exclusively on the training data.
- SHAP values were computed on the independent test set.
- External validation was performed using an independent DrugMatrix cohort.

---

# Supplementary Files

The repository includes:

- Supplementary Table S1 – Differentially expressed genes
- Supplementary Table S2 – Top 100 Random Forest features
- Supplementary Table S3 – SHAP biomarker ranking
- Supplementary Table S4 – GO enrichment analysis
- Supplementary Table S5 – KEGG enrichment analysis

---

# Citation

If you use this repository in your research, please cite:

**Tahta Herdian Andika**, Dewi Damayanti Abdul Karim, Joana Freire Gameiro, Ferly Ardhy.

**Transcriptomic Biomarker Discovery for Drug-Induced Liver Injury in Rat Liver through Explainable Machine Learning with Independent DrugMatrix Validation.**

*Archives of Toxicology* (Manuscript submitted).

---

# License

This project is released under the MIT License.

---

# Contact

**Tahta Herdian Andika**

Aisyah University, Indonesia

Email:

tahta.herdian.a@aisyahuniversity.ac.id

---

# Acknowledgements

We acknowledge the Open TG-GATEs consortium and the Gene Expression Omnibus (GEO) for providing publicly available toxicogenomic datasets used in this study.

- Open TG-GATEs
- DrugMatrix (GSE57815)
- SHAP developers
- XGBoost developers

---

⭐ If you find this repository useful, please consider giving it a star.
