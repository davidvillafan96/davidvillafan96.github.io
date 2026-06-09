---
layout: page
title: "Project 1: GDSC2 Curation & Integration"
description: "Building an Integrative Dataset for EDA and Predictive Modeling"
bg_color: "#4cc9f0"
icon: "fa-solid fa-laptop-code"
importance: 1
---
# Project 1: GDSC2 Curation and Integration: Building an Integrative Dataset for EDA and Predictive Modeling

# **Project Objective**

To integrate, curate, standardize, and quality-control the GDSC2 pharmacogenomic resources into a single reproducible master dataset, suitable for downstream exploratory analysis and machine learning-based prediction of drug sensitivity across cancer types.

This project aims to transform heterogeneous source files into a harmonized analytical resource that links:

- **drug response**,
- **cell line molecular and clinical annotations**, and
- **compound target information**,

in order to support robust modeling of **ln(IC50)** and related pharmacological response metrics.

# **Business Case**

Cancer drug response is highly heterogeneous across tumor types, molecular backgrounds, and drug mechanisms. Public pharmacogenomic repositories such as GDSC2 contain highly valuable information, but the data are distributed across multiple files, with inconsistencies in naming, missing annotations, replicate measurements, and uneven metadata coverage.

This project addresses a practical and scientific gap:

1. **Data fragmentation** limits reproducibility and slows model development.
2. **Inconsistent annotations** reduce the quality of downstream machine learning workflows.
3. **Poorly standardized response variables** can bias predictive models.
4. **Unresolved duplicate measurements and missing values** can introduce noise and false associations.

By generating a curated master dataset, this project creates a reusable foundation for:

- drug sensitivity prediction,
- biomarker discovery,
- tumor-type stratification,
- model benchmarking,
- and future translational studies in precision oncology.

### **Value proposition**

The resulting dataset can serve as:

- a **model-ready resource** for ML pipelines,
- a **benchmark dataset** for drug response prediction,
- a **reproducible preprocessing framework** for other pharmacogenomic projects,
- and a **publication-grade technical contribution** in cancer data science.

# **Scientific Rationale**

The GDSC2 platform links cancer cell lines with drug response profiles measured under standardized conditions. Because drug sensitivity varies according to both tumor lineage and molecular context, integrating response data with cell line annotations and compound target information enables:

- comparison across cancer types,
- assessment of target-pathway relationships,
- identification of extreme sensitivity or resistance phenotypes,
- and prediction of response using supervised learning.

This work is not limited to cleaning data. It establishes the **analytical infrastructure** needed to move from raw pharmacogenomic tables to a **curated dataset for predictive oncology**.

## **Available Files**

| **File Name** | **Description** |
| --- | --- |
| **GDSC2-dataset.csv** | Contains drug sensitivity data, including **IC50 values** for various drugs tested on cancer cell lines. *(Original source file)* |
| **Cell_Lines_Details.xlsx** | Provides detailed information about cancer cell lines, including **mutations, copy number alterations, and gene expression**. *(Original source file)* |
| **Compounds-annotation.csv** | Contains information about the drugs used in screening, including their **targets and pathways**. *(Original source file)* |

## **Dataset Details**

### **1️ GDSC2-dataset.csv (Drug Sensitivity Data)**

| **Column** | **Description** |
| --- | --- |
| **DATASET** | Identifier for the GDSC dataset version. |
| **NLME_RESULT_ID** | Unique identifier for the **non-linear mixed effects (NLME) model** result. |
| **NLME_CURVE_ID** | Identifier for the dose-response curve fitted by NLME. |
| **COSMIC_ID** | Unique identifier for the **cell line** from the **COSMIC database**. |
| **CELL_LINE_NAME** | Name of the **cancer cell line** used in the experiment. |
| **SANGER_MODEL_ID** | Identifier used by the **Sanger Institute** for the cell line model. |
| **TCGA_DESC** | Cancer type description according to **The Cancer Genome Atlas (TCGA)**. |
| **DRUG_ID** | Unique identifier for the **drug** used in the experiment. |
| **DRUG_NAME** | Name of the **drug** used in the experiment. |
| **PUTATIVE_TARGET** | The presumed **molecular target** of the drug. |
| **PATHWAY_NAME** | The biological **pathway** affected by the drug. |
| **COMPANY_ID** | Identifier for the company that provided the drug. |
| **WEBRELEASE** | Date or version of web release for this data. |
| **MIN_CONC / MAX_CONC** | Minimum and maximum **drug concentrations** used in the experiment. |
| **LN_IC50** | **Natural log of IC50** (half-maximal inhibitory concentration). Lower values indicate higher drug sensitivity. |
| **AUC** | **Area Under the Curve**, a measure of drug effectiveness. |
| **RMSE** | **Root Mean Square Error**, indicating the fit quality of the dose-response curve. |
| **Z_SCORE** | Standardized score of the drug response for comparisons across different drugs and cell lines. |

---

### **2️ Cell_Lines_Details.xlsx (Cancer Cell Line Details)**

| **Column** | **Description** |
| --- | --- |
| **Sample Name** | Unique identifier for the **cell line sample**. |
| **COSMIC ID** | Unique ID from the **COSMIC database** for the cell line. |
| **Whole Exome Sequencing (WES)** | **Genetic mutation** data from **whole exome sequencing**. |
| **Copy Number Alterations (CNA)** | Data on **gene copy number** changes in the cell line. |
| **Gene Expression** | Information on **gene expression levels**. |
| **Methylation** | Data on **DNA methylation patterns**. |
| **Drug Response** | Drug sensitivity and resistance data for the **cell line**. |
| **GDSC Tissue Descriptor 1 & 2** | Primary and secondary **tissue type classification**. |
| **Cancer Type (TCGA label)** | Cancer type classification according to **TCGA**. |
| **Microsatellite Instability Status (MSI)** | Indicates whether the cell line has **microsatellite instability**. |
| **Screen Medium** | The growth **medium** used for culturing the cell line. |
| **Growth Properties** | Characteristics of **cell line growth** in culture. |

---

### **3️ Compounds-annotation.csv (Drug Details)**

| **Column** | **Description** |
| --- | --- |
| **DRUG_ID** | Unique identifier for the **drug**. |
| **SCREENING_SITE** | Location where the **drug screening** was performed. |
| **DRUG_NAME** | Name of the **drug compound**. |
| **SYNONYMS** | Alternative names for the **drug**. |
| **TARGET** | The **molecular target(s)** of the drug. |
| **TARGET_PATHWAY** | The **biological pathway(s)** targeted by the drug. |
|  |  |
|  |  |

## **Data Collection**

The data was collected by the **Genomics of Drug Sensitivity in Cancer** project, a collaboration between:

- 🏥 **Sanger Institute (UK)**
- 🏥 **Massachusetts General Hospital Cancer Center (USA)**

**Methodology:**

- Large-scale screening of **human cancer cell lines** with various **anti-cancer drugs**.
- **Cell viability** was measured using **CellTiter-Glo assay** after **72 hours of drug treatment**.
- Data is regularly updated to **expand coverage** and improve **data quality**.

🔗 **Dataset Source:** [GDSC Database](https://www.google.com/url?q=https%3A%2F%2Fwww.cancerrxgene.org%2F)

# 📊 Key Results — GDSC2 Dataset Standardization & Analytical Readiness

After the initial integration and cleaning stages, the dataset underwent a **standardization and analytical validation phase** designed to ensure statistical coherence and compatibility with downstream modeling and exploratory analysis.

This step transforms the dataset from a cleaned table into a **model-ready analytical resource**.

---

# ⚙️ Variable Standardization

To ensure consistent statistical handling across the dataset, key variables were standardized according to their data type.

### Categorical Variables

Several biological descriptors were converted into **explicit categorical factors**, including:

- Cancer type (TCGA mapping)
- Molecular pathway targets
- Tissue descriptors
- Growth properties
- Microsatellite instability (MSI)
- Outlier classification flags

Missing values were explicitly encoded as **"Unknown"** rather than remaining as implicit NA values.

This prevents silent data loss during statistical modeling and ensures all observations remain usable.

---

# 📈 Numerical Scaling of Drug Response Metrics

Four central pharmacological response variables were standardized using **z-score scaling (mean = 0, SD = 1)**:

- **LN_IC50**
- **AUC**
- **RMSE**
- **Z_SCORE**

Scaling these metrics ensures that:

- Variables with different numeric ranges become comparable
- Machine learning algorithms are not biased by magnitude differences
- Multivariate analyses operate on normalized distributions

Density plots confirmed that the transformation successfully centered each variable around zero while preserving their underlying biological variability.

---

# ⚙️ Outlier Detection, Missing Target Analysis & Response Distribution

Following dataset integration and cleaning, a dedicated analytical validation step was performed to assess **data completeness, extreme phenotypes, and response variable behavior**.

---

## 🧬 Missing Target Annotation Analysis

The evaluation of compound annotations revealed that:

- A total of **38 drugs lacked an assigned molecular target** in the integrated dataset.

This highlights an important limitation:

- Incomplete biological annotation may affect **mechanistic interpretation** and **feature engineering** in downstream models.
- These drugs remain usable for predictive modeling, but should be treated cautiously in **pathway-level analyses**.

📊 *Visualization: Proportion of drugs with vs without assigned targets*

![image.png](Project%201%20GDSC2%20Curation%20and%20Integration%20Building%20/image.png)

---

## 🚨 Outlier Detection in Drug Response

To identify biologically relevant extreme phenotypes, outlier detection was performed at the **drug-specific level** using a statistical threshold:

- **Mean ± 3 standard deviations (SD)** on `LN_IC50`

This allowed classification of observations into:

- **Extreme Sensitivity**
- **Extreme Resistance**
- **Normal Range**

### 🔬 Key Insight

This analysis enabled the identification of:

- Cell lines exhibiting **exceptional drug sensitivity**, potentially indicating:
    - target dependency
    - synthetic lethality scenarios
- Cell lines showing **extreme resistance**, which may reflect:
    - intrinsic resistance mechanisms
    - pathway bypass or compensatory signaling

These observations represent **high-value candidates for biomarker discovery**.

📊 *Visualization: Distribution of outlier classes*

![image.png](Project%201%20GDSC2%20Curation%20and%20Integration%20Building%20/image%201.png)

---

## 📈 Distribution of the Response Variable (LN_IC50)

The distribution of the main response variable (`LN_IC50`) was evaluated to assess its suitability for statistical modeling.

### Observations:

- The distribution exhibits a **smooth, unimodal density**, indicating a coherent global response structure
- A **moderate left-skewness** is observed, suggesting a higher prevalence of **high-sensitivity responses (low IC50 values)**
- No evidence of strong multimodality or pathological distortions was detected
- The logarithmic transformation effectively stabilizes variance across observations

### 🧠 Interpretation

- The response variable is **well-suited for regression-based machine learning models**
- The observed skewness reflects **biologically meaningful heterogeneity**, rather than technical bias
- The distribution supports:
    - linear models
    - tree-based models
    - regularized regression approaches

### ⚠️ Important Consideration

This distribution aggregates responses across **multiple drugs and cancer types**, which may mask **subtype-specific sensitivity patterns**.

---

> The enrichment of low LN_IC50 values suggests the presence of highly responsive cell line–drug interactions, which may represent biologically relevant vulnerabilities worth exploring in downstream analyses.
> 

📊 *Visualization: Density plot of LN_IC50*

![image.png](Project%201%20GDSC2%20Curation%20and%20Integration%20Building%20/image%202.png)

---

# 🔗 Correlation Structure of Drug Sensitivity Metrics

To validate internal consistency, correlation analysis was performed across the main pharmacological response variables.

---

## 📊 Key Findings

- **Correlation between LN_IC50 and AUC ≈ 0.77**

### 🧠 Interpretation

This result indicates that:

- Both metrics capture **drug sensitivity behavior**
- They are **strongly associated but not redundant**

This is a critical property:

- A perfect correlation (≈1.0) would indicate duplication of information
- A weak correlation would suggest inconsistency

👉 The observed value reflects a **healthy analytical balance**, where:

- Shared signal exists (true biological response)
- Complementary information is retained

---

## 📉 Additional Correlation Insights

- **RMSE shows negative correlation with response variables**
    - Suggesting that **higher model uncertainty** is associated with **lower sensitivity signals**
- **Z-score aligns with expected sensitivity trends**
    - Confirming correct standardization
    - Supporting dataset internal consistency
    

![image.png](Project%201%20GDSC2%20Curation%20and%20Integration%20Building%20/image%203.png)

![image.png](Project%201%20GDSC2%20Curation%20and%20Integration%20Building%20/image%204.png)

---

# 🧪 Structural Quality Control

A structural audit of categorical variables was conducted to detect **zero-variance or near-constant features**.

This step ensures that:

- Non-informative variables do not enter predictive models
- Dimensionality is controlled
- Statistical assumptions remain valid

This validation step is critical for **robust downstream machine learning workflows**.

---

# 📦 Final Analytical Dataset

The resulting dataset (`GDSC2_ReadyForEDA.csv`) is now:

- Statistically standardized
- Structurally validated
- Free of hidden categorical inconsistencies
- Normalized for multivariate analysis

This dataset is therefore fully prepared for:

- Exploratory Data Analysis (EDA)
- Dimensionality reduction (PCA)
- Drug sensitivity modeling
- Biomarker discovery pipelines

---

# 🚀 Strategic Impact

This phase demonstrates a key principle of high-quality computational biology:

**Data preparation is not a mechanical step — it is an analytical process that directly determines the reliability of downstream discoveries.**

By combining rigorous standardization, statistical validation, and structural quality control, the GDSC2 dataset is now positioned as a **robust foundation for predictive oncology research**.

## 👤 **Author**

**David Villafañe**

PhD in Biological Sciences

Genomics | Bioinformatics | Data Science | Precision Medicine | Pharmacogenomics

Linkedin: [**linkedin.com/in/davidvillafanie**](https://www.linkedin.com/in/davidvillafanie/)

Git-hub: [https://github.com/davidvillafan96](https://github.com/davidvillafan96)
