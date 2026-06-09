---
layout: page
title: Computational Biology & Data Science
permalink: /computational-biology/
---

<div class="mt-4 mb-5 font-jojy text-center" style="width: 100%;">
  <h1 class="fw-bold" style="font-size: 2.8rem; letter-spacing: -1.5px; color: #000000 !important; margin-bottom: 5px; text-align: center !important;">
    Computational Biology & Data Science
  </h1>
</div>

<div class="mb-5 font-jojy" style="color: #000000 !important; max-width: 750px; margin-left: auto; margin-right: auto; text-align: center !important;">
  <h2 class="fw-bold" style="font-size: 1.5rem; letter-spacing: -0.5px; margin-bottom: 15px; color: #000000 !important;">What I Do</h2>
  <p style="font-size: 1.05rem; line-height: 1.6; color: #333333 !important; font-weight: 400;">
    I treat complex, high-dimensional biological landscapes as structured mathematical feature spaces. By leveraging statistical computing best practices, advanced feature engineering, and relational database indexing, I extract subtle biomolecular signals and deploy reproducible Machine Learning classifiers from sparse, zero-inflated multi-omics matrices.
  </p>
</div>

<div class="jojy-dropdown-container mb-5 font-jojy">

  <details class="jojy-dropdown" open>
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">🤖</span> Predictive Modeling & Translational Machine Learning
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Building and deploying validated predictive classifiers to model complex phenotypes and pharmacological actions from multi-omics inputs.
      </p>
      <ul>
        <li><strong>Frameworks:</strong> <code>scikit-learn</code>, <code>XGBoost</code>, <code>RandomForest</code>, <code>caret</code> (R), <code>e1071</code> (SVM), and penalized generalized linear models (<code>glmnet</code>).</li>
        <li><strong>Cancer Drug Sensitivity:</strong> Integrated multi-layered profiles (clinical, mutation arrays, and transcriptomics via GDSC datasets) to screen and predict exact pharmacological sensitivity and IC50 readouts across distinct cancer cell lines.</li>
        <li><strong>Validation Rigor:</strong> Implementation of nested and Stratified K-Fold Cross-Validation loops to prevent data leakage and rigorously handle clinical class imbalances.</li>
        <li><strong>Explainable AI (XAI):</strong> Decoupling black-box algorithms using feature importance scaling and <code>SHAP (SHapley Additive exPlanations)</code> vectors to trace underlying biological biomarkers.</li>
      </ul>
    </div>
  </details>

  <details class="jojy-dropdown">
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">📊</span> Compositional Data Analysis (CoDA) & Statistics
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Applying mathematical transformations to high-throughput biological counts to bypass absolute proportion constraints and library-size biases.
      </p>
      <ul>
        <li><strong>Toolkits:</strong> <code>compositions</code> (R package), <code>SciPy</code>, <code>Statsmodels</code>, and <code>ANCOM-BC</code> differential abundance frameworks.</li>
        <li><strong>Log-Ratio Transformations:</strong> Deploying Centered Log-Ratio (<code>CLR</code>) and Isometric Log-Ratio (<code>ILR</code>) transformations over zero-inflated metagenomic abundance matrices.</li>
        <li><strong>Regularization & Ordination:</strong> High-dimensional feature selection using <code>Lasso</code> and <code>ElasticNet</code> regression paradigms. Multivariate exploration via PCA, PCoA, t-SNE, and UMAP clustering architectures.</li>
      </ul>
    </div>
  </details>

  <details class="jojy-dropdown">
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">🗄️</span> Relational Data Infrastructure & Query Optimization
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Architecting local structures to query, manipulate, and optimize multi-gigabyte genomics arrays seamlessly before feeding modeling matrices.
      </p>
      <ul>
        <li><strong>Data Warehousing & Queries:</strong> Writing optimized <code>SQL</code> scripts to manage deep tabular multi-omics inputs, using <code>PostgreSQL</code> and embedded high-performance analytical engines like <code>DuckDB</code>.</li>
        <li><strong>Feature Merging:</strong> Advanced indexing, relational joins, and Window functions to blend metadata fields, genomic coordinates, and clinical expression variables efficiently.</li>
      </ul>
    </div>
  </details>

  <details class="jojy-dropdown">
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">⚙️</span> Reproducible Pipelines & Containerized Analytics
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Automating end-to-end data processing routines using industry-standard workflow managers to ensure complete traceability from raw files to final features.
      </p>
      <ul>
        <li><strong>Workflow Engines:</strong> Orchestrating multi-step parallel processing routines via <code>Nextflow</code> architectures and rule-based <code>Snakemake</code> pipelines.</li>
        <li><strong>Environment Isolation:</strong> Isolating package dependencies via <code>Docker</code>, <code>Singularity (Apptainer)</code>, and Conda virtual environments to ensure 100% execution parity across distributed HPC clusters.</li>
      </ul>
    </div>
  </details>

</div>

<div class="text-center mt-5 font-jojy">
  <a href="/" class="jojy-back-btn">← Back to Home</a>
</div>

<style>
  .font-jojy {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif !important;
  }
  .jojy-dropdown-container {
    width: 100% !important;
    max-width: 750px !important;
    margin-left: auto !important;
    margin-right: auto !important;
    display: block !important;
    text-align: left !important;
  }
  .jojy-dropdown {
    background: #ffffff !important;
    border: 1px solid #e0e0e0 !important;
    border-radius: 12px !important;
    margin-bottom: 14px !important;
    padding: 0 !important;
    overflow: hidden !important;
    transition: box-shadow 0.2s ease, border-color 0.2s ease !important;
    box-shadow: 0 2px 5px rgba(0,0,0,0.02) !important;
    display: block !important;
    width: 100% !important;
  }
  .jojy-dropdown[open] {
    border-color: #4cc9f0 !important; /* Color de acento de Comp Bio */
    box-shadow: 0 4px 12px rgba(0,0,0,0.04) !important;
  }
  .jojy-dropdown-title {
    font-size: 1.1rem !important;
    font-weight: 600 !important;
    color: #000000 !important;
    padding: 16px 20px !important;
    cursor: pointer !important;
    user-select: none !important;
    display: flex !important;
    align-items: center !important;
    justify-content: flex-start !important;
    list-style: none !important;
    list-style-type: none !important;
    margin: 0 !important;
    outline: none !important;
    text-indent: 0 !important;
  }
  .jojy-dropdown-title::-webkit-details-marker,
  .jojy-dropdown-title::marker {
    display: none !important;
    content: "" !important;
    width: 0 !important;
    height: 0 !important;
  }
  .jojy-dropdown-title::after {
    content: '→' !important;
    margin-left: auto !important;
    font-weight: 400 !important;
    color: #888888 !important;
    transition: transform 0.2s ease !important;
    display: inline-block !important;
  }
  .jojy-dropdown[open] .jojy-dropdown-title::after {
    transform: rotate(90deg) !important;
    color: #000000 !important;
  }
  .jojy-dropdown-emoji {
    margin-right: 12px !important;
    font-size: 1.15rem !important;
    display: inline-block !important;
    line-height: 1 !important;
  }
  .jojy-dropdown-content {
    padding: 20px !important;
    border-top: 1px solid #f5f5f5 !important;
    background-color: #fafafa !important;
    font-size: 0.98rem !important;
    line-height: 1.6 !important;
    color: #333333 !important;
  }
  .jojy-dropdown-content p { margin-top: 0 !important; margin-bottom: 12px !important; }
  .jojy-dropdown-content ul { margin-bottom: 0 !important; padding-left: 20px !important; }
  .jojy-dropdown-content li { margin-bottom: 6px !important; }
  .jojy-back-btn {
    font-size: 0.95rem !important;
    color: #777777 !important;
    text-decoration: none !important;
    font-weight: 500 !important;
    border-bottom: none !important;
    transition: color 0.2s ease !important;
  }
  .jojy-back-btn:hover { color: #000000 !important; border-bottom: none !important; text-decoration: none !important; }
</style>
