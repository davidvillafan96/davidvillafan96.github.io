---
layout: page
title: "Project 5: Transcriptomic Biomarker Discovery in Colorectal Cancer"
description: "An End-to-End RNA-Seq Processing, Differential Expression (DESeq2), Network Biology (WGCNA), and Predictive Machine Learning Pipeline"
bg_color: "#0f172a"
icon: "fa-solid fa-dna"
importance: 5
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-slate-900 to-indigo-950 border-l-4 border-teal-500 p-6 rounded-r-xl mb-8 shadow-sm">
    <h2 class="text-xl font-bold text-white mb-2 flex items-center gap-2">
      <i class="fa-solid fa-bullseye text-teal-400"></i> Project Objective
    </h2>
    <p class="text-indigo-200/90 leading-relaxed text-sm">
      Translating high-dimensional transcriptomic profiles into clinically actionable discovery assets. This standalone pipeline processes RNA-seq cohorts to map the continuous evolutionary continuum across <strong>Normal tissue, Primary Tumors, and Metastatic lesions</strong> in Colorectal Cancer (CRC) by structurally intersecting statistical significance, network centrality, and machine learning classifiers.
    </p>
    <div class="mt-4 flex flex-wrap gap-2 text-[11px] font-mono text-teal-300">
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">RNA-Seq / DESeq2</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">WGCNA Network Biology</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Random Forest Classifier</span>
    </div>
  </div>

  <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center shadow-sm max-w-[350px] mx-auto mb-6">
    <span class="text-[10px] font-mono text-teal-600 font-bold block mb-1">STANDALONE TRANSLATIONAL STUDY</span>
    <h4 class="font-bold text-slate-800 text-xs">Colorectal Cancer Transcriptomic Core</h4>
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-layer-group text-teal-600"></i> Data Structure & Experimental Design
  </h2>
  <p class="text-sm text-gray-600 mb-8 leading-relaxed">
    To minimize confounding patient-specific germline variations and technical batch artifacts, the framework utilizes a tightly controlled, paired experimental design covering 10,000 deep-sequenced transcript loci across progressive disease boundaries.
  </p>

  <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-8 text-center">
    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm">
      <div class="text-2xl font-bold text-gray-800 font-mono">18</div>
      <div class="text-xs font-semibold text-gray-400 font-mono mt-1 uppercase">Normal Mucosa Samples</div>
    </div>
    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm">
      <div class="text-2xl font-bold text-teal-600 font-mono">18</div>
      <div class="text-xs font-semibold text-teal-500 font-mono mt-1 uppercase">Primary Tumors</div>
    </div>
    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm">
      <div class="text-2xl font-bold text-indigo-600 font-mono">18</div>
      <div class="text-xs font-semibold text-indigo-500 font-mono mt-1 uppercase">Metastatic Lesions</div>
    </div>
  </div>
  
  <p class="text-xs text-gray-500 bg-gray-50 border p-3 rounded-lg leading-relaxed font-mono mb-10">
    ✔ Balanced Cohort Structure (n=54 total samples) derived from paired patient profiles based on GSE50760 architecture to preserve maximum multi-class statistical power.
  </p>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[850px] mx-auto mb-10">
    <img src="{{ '/assets/img/crc_transcriptomics/project5_workflow.png' | relative_url }}" alt="Transcriptomic Discovery Pipeline Workflow" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 5.0: End-to-end transcriptomic pipeline workflow spanning RNA-Seq normalization, exploratory analytics, core network modeling, target ranking, and phenotype classification.
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-compass text-teal-600"></i> Unsupervised Visual Exploration (EDA)
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    Principal Component Analysis (PCA) executed on variance-stabilized expression counts reveals strong, inherent biological signals, cleanly separating samples according to their physiological and oncological phenotypes.
  </p>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[650px] mx-auto my-8">
    <img src="{{ '/assets/img/crc_transcriptomics/project5_pca.png' | relative_url }}" alt="Principal Component Analysis Spatial Separation" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 5.1: PCA projection demonstrating clear, multi-class clustering across physiological boundaries.
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-6 text-xs text-gray-600 leading-relaxed">
    <div class="bg-slate-50 p-4 rounded-xl border">
      <strong>PC1 Variance Explanation (~64%):</strong> Captures the primary transcriptomic shift associated with normal-to-malignant cellular transformation.
    </div>
    <div class="bg-slate-50 p-4 rounded-xl border">
      <strong>PC2 Variance Explanation (~15%):</strong> Effectively tracks secondary evolutionary components, isolating metastatic progress from localized primary masses.
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <div class="flex flex-col md:flex-row md:items-center justify-between mb-6">
    <div>
      <h2 class="text-2xl font-bold text-gray-900 tracking-tight flex items-center gap-2">
        <i class="fa-solid fa-volcano text-teal-600"></i> Differential Expression Landscapes (DESeq2)
      </h2>
      <p class="text-xs text-gray-500 mt-1">Isolating highly dysregulated continuous loci using strict false discovery constraints (FDR < 0.05).</p>
    </div>
  </div>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[650px] mx-auto my-8">
    <img src="{{ '/assets/img/crc_transcriptomics/project5_volcano.png' | relative_url }}" alt="DESeq2 Volcano Plot Tumor vs Normal" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 5.2: Distribution of magnitude (Log2 Fold Change) vs. statistical significance (-Log10 Adjusted P-value).
    </div>
  </div>

  <div class="border border-gray-100 rounded-2xl bg-white shadow-sm overflow-hidden my-6">
    <table class="w-full text-left border-collapse">
      <thead>
        <tr class="bg-gray-50 border-b border-gray-100 text-[11px] font-mono font-bold text-gray-500 uppercase tracking-wider">
          <th class="p-4">Functional Transcript Groups</th>
          <th class="p-4">Representative Identified Biomarkers</th>
          <th class="p-4">Downstream Pathophysiological Mechanistic Link</th>
        </tr>
      </thead>
      <tbody class="divide-y divide-gray-50 text-xs text-gray-600">
        <tr>
          <td class="p-4 font-bold text-slate-900">Extracellular Matrix Remodeling</td>
          <td class="p-4 font-mono text-teal-600">COL11A1, INHBA, COL10A1</td>
          <td class="p-4">Structural disassembly of stromal barriers, facilitating active cell migration patterns.</td>
        </tr>
        <tr>
          <td class="p-4 font-bold text-slate-900">Active Tissue Invasion Layer</td>
          <td class="p-4 font-mono text-teal-600">MMP1, MMP3, MMP7</td>
          <td class="p-4">Proteolytic cleavage of the basement membrane, driving progressive local disease expansion.</td>
        </tr>
        <tr>
          <td class="p-4 font-bold text-slate-900">Epithelial-Mesenchymal Transition</td>
          <td class="p-4 font-mono text-teal-600">CLDN1, KRT17, FOXQ1, WNT2</td>
          <td class="p-4">Loss of stable epithelial cell-cell adhesion, triggering mobile mesenchymal phenotypes.</td>
        </tr>
        <tr>
          <td class="p-4 font-bold text-slate-900">Stromal & Differentiation Drivers</td>
          <td class="p-4 font-mono text-teal-600">FAP, CEMIP</td>
          <td class="p-4">Fibroblast activation and structural reorganization of tumor microenvironment dynamics.</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-chart-violin text-teal-600"></i> Expression Distribution of Candidate Biomarkers
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    Violin plot distributions across key prioritized features highlight tight intra-group variance patterns coupled with clean, definitive multi-class step shifts.
  </p>

  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 my-6 max-w-[900px] mx-auto">
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/crc_transcriptomics/project5_violin_col10a1.png' | relative_url }}" alt="COL10A1 Expression Shift" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">COL10A1 / COL11A1</div>
    </div>
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/crc_transcriptomics/project5_violin_best4.png' | relative_url }}" alt="BEST4 Expression Shift" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">BEST4 Homeostatic Loss</div>
    </div>
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/crc_transcriptomics/project5_violin_mmp.png' | relative_url }}" alt="MMP Expression Shift" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">MMP1 / MMP7 Invasion</div>
    </div>
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/crc_transcriptomics/project5_violin_foxq1.png' | relative_url }}" alt="FOXQ1 Expression Shift" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">FOXQ1 / INHBA / ETV4</div>
    </div>
  </div>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[650px] mx-auto my-8">
    <img src="{{ '/assets/img/crc_transcriptomics/project5_heatmap.png' | relative_url }}" alt="Top DEGs Expression Clustered Heatmap" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 5.3: Unsupervised bidirectional hierarchical clustering of the top differentially expressed genes.
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-diagram-project text-teal-600"></i> Weighted Gene Co-Expression Networks (WGCNA)
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    Moving beyond isolated single-gene variations, the pipeline clusters transcript dynamics into coordinated biological networks linked directly to clinical traits.
  </p>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[650px] mx-auto my-8">
    <img src="{{ '/assets/img/crc_transcriptomics/project5_wgcna_modules.png' | relative_url }}" alt="WGCNA Module-Trait Relationship Heatmap" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 5.4: Module-trait correlation matrix linking co-expression blocks with progressive clinical stages.
    </div>
  </div>

  <div class="bg-blue-50/40 border border-blue-100 rounded-xl p-4 text-xs text-slate-700 leading-relaxed my-6">
    <h5 class="font-bold text-blue-900 mb-1 flex items-center gap-1"><i class="fa-solid fa-circle-info"></i> Functional Network Program Mapping</h5>
    <ul class="list-disc pl-5 space-y-1">
      <li><strong>Meblue (Tumor-Enriched Program):</strong> Strongly correlated with active oncogenic progression traits ($r = 0.86$), packing major structural matrix elements.</li>
      <li><strong>Meturquoise / Megreen (Homeostatic Programs):</strong> Highly correlated with normal tissue preservation frameworks, showing progressive silencing during advanced tumor evolution steps.</li>
    </ul>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-arrow-down-short-wide text-teal-600"></i> Network Centricity & Hub Gene Prioritization
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    To filter passenger genes from authentic core drivers, we implemented a composite ranking function tracking statistical significance, effect size, and intramodular network topology ($kME$):
  </p>

  <div class="bg-slate-900 border-l-4 border-teal-500 p-5 rounded-r-xl my-6 font-mono text-center text-sm text-teal-300 overflow-x-auto">
    $$\text{Hub Score} = |kME| \times |\log_{2}\text{FC}| \times (-\log_{10}(\text{P}_{\text{adj}}))$$
  </div>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[650px] mx-auto my-8">
    <img src="{{ '/assets/img/crc_transcriptomics/project5_hub_prioritization.png' | relative_url }}" alt="Top Prioritized Hub Genes Matrix" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 5.5: Multi-dimensional ranking isolating apex diagnostic hub targets.
    </div>
  </div>

  <div class="bg-teal-50/20 border border-teal-100 rounded-xl p-4 text-xs text-slate-800 my-6">
    <strong>Apex Biomarker Panel Elements:</strong> Top prioritized targets such as <strong>BEST4, OTOP2, OTOP3, SPIB, CA7, and GPAT3</strong> bridge high effect-size magnitude with supreme centrality scores, establishing the foundational input signature for predictive modeling layers.
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-robot text-teal-600"></i> Predictive Machine Learning Framework
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    Deploying a robust multi-class Random Forest architecture trained on the prioritized biomarker signature confirms steady out-of-bag (OOB) error stabilization and near-perfect clinical-grade diagnostic power.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-6 max-w-[850px] mx-auto">
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/crc_transcriptomics/project5_rf_error_stability.png' | relative_url }}" alt="Random Forest Classifier OOB Error Stability" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">OOB Error Optimization (Stabilized @ ~100 Trees)</div>
    </div>
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/crc_transcriptomics/project5_roc_curve.png' | relative_url }}" alt="Multi-Class ROC Performance Curves" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">Multi-Class Classifier ROC Curve (AUC: 0.975)</div>
    </div>
  </div>

  <div class="grid grid-cols-1 sm:grid-cols-4 gap-4 my-6 text-center">
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xl font-bold text-teal-600 font-mono">0.975</div>
      <div class="text-[10px] text-gray-400 font-mono mt-0.5 uppercase tracking-wider">Overall AUC</div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xl font-bold text-slate-800 font-mono">86%</div>
      <div class="text-[10px] text-gray-400 font-mono mt-0.5 uppercase tracking-wider">Classification Accuracy</div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xl font-bold text-slate-800 font-mono">0.83</div>
      <div class="text-[10px] text-gray-400 font-mono mt-0.5 uppercase tracking-wider">Global Sensitivity</div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xl font-bold text-slate-800 font-mono">0.89</div>
      <div class="text-[10px] text-gray-400 font-mono mt-0.5 uppercase tracking-wider">Global Specificity</div>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-briefcase text-teal-600"></i> Translational Business & Industry Impact
  </h2>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-xs text-gray-600">
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-microscope text-teal-600"></i> Precision Diagnostic Panels
      </h4>
      Reduces immense, costly candidate multi-omic gene discovery spaces down to concise, high-efficiency, multi-class biomarker signatures tailored for target multiplex qPCR arrays or enrichment panels.
    </div>
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-sliders text-teal-600"></i> Companion Stratification Core
      </h4>
      Provides a foundational analytical asset to systematically prioritize actionable tumor targets, enrich target clinical trial cohorts, and predict sample-level phenotypic evolution.
    </div>
  </div>
</div>

<div class="my-8 pt-4 border-t border-gray-100 text-xs text-gray-400 font-mono">
  📁 Project References & Series Pipeline Hierarchy:
  <ul class="list-disc pl-5 mt-2 space-y-1">
    <li>Independent Translational Research Asset</li>
    <li>Source Code Repositories: <a class="text-indigo-600 hover:underline" href="https://github.com/davidvillafan96/CRC-Transcriptomic-Biomarker-Discovery" target="_blank">Colorectal Cancer Transcriptomic Discovery Codebase</a></li>
  </ul>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
