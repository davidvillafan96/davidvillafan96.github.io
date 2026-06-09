---
layout: page
title: "Project 2: GDSC2 EDA & Statistical Learning"
description: "Uncovering Latent Structures, Tissue Specificity, and Target Drivers"
bg_color: "#3f37c9"
icon: "fa-solid fa-diagram-project"
importance: 2
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-indigo-50 to-purple-50 border-l-4 border-indigo-500 p-6 rounded-r-xl mb-8">
    <h2 class="text-xl font-bold text-gray-900 mb-2 flex items-center gap-2">
      <i class="fa-solid fa-bullseye text-indigo-600"></i> Project Objective
    </h2>
    <p class="text-gray-700 leading-relaxed">
      To explore the statistical structure, biological heterogeneity, and inferential patterns of the curated <code class="bg-white/80 px-1.5 py-0.5 rounded text-indigo-700 font-mono text-xs">GDSC2_ReadyForEDA</code> dataset in order to characterize cancer drug sensitivity and establish a robust, interpretable foundation for downstream machine learning.
    </p>
    <div class="mt-4 flex flex-wrap gap-2 text-xs font-semibold text-indigo-800">
      <span class="bg-white/60 px-2.5 py-1 rounded-full border border-indigo-100">Distribution Profiling</span>
      <span class="bg-white/60 px-2.5 py-1 rounded-full border border-indigo-100">Non-parametric Inference</span>
      <span class="bg-white/60 px-2.5 py-1 rounded-full border border-indigo-100">Latent Space Mapping (PCA)</span>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-4 my-6">
    <div class="bg-gray-50 border border-gray-100 p-5 rounded-xl text-center">
      <span class="text-xs font-mono text-gray-400 block mb-1">PREVIOUS</span>
      <h4 class="font-bold text-gray-700 text-sm">Project 1: Data Engineering</h4>
      <p class="text-xs text-gray-500 mt-1">Curation, data-type casting & harmonization.</p>
    </div>
    <div class="bg-indigo-50/50 border border-indigo-100 p-5 rounded-xl text-center shadow-sm ring-1 ring-indigo-500/10">
      <span class="text-xs font-mono text-indigo-500 font-bold block mb-1">CURRENT PHASE</span>
      <h4 class="font-bold text-indigo-900 text-sm">Project 2: Statistical Inference</h4>
      <p class="text-xs text-indigo-700 mt-1">Uncovering biological and mathematical structure.</p>
    </div>
    <div class="bg-gray-50 border border-gray-100 p-5 rounded-xl text-center">
      <span class="text-xs font-mono text-gray-400 block mb-1">UPCOMING</span>
      <h4 class="font-bold text-gray-700 text-sm">Project 3: Predictive Modeling</h4>
      <p class="text-xs text-gray-500 mt-1">Machine Learning & biomarker discovery.</p>
    </div>
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-4 flex items-center gap-2">
    <i class="fa-solid fa-route text-indigo-500"></i> Statistical Learning Workflow
  </h2>
  <p class="text-sm text-gray-600 mb-6">
    Before feeding features into complex architectures, the analytical roadmap steps through validation, hypothesis testing, and coordinate projection to guarantee all patterns capture true cancer cell vulnerabilities.
  </p>

  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 mb-8">
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm flex flex-col justify-between">
      <div>
        <span class="text-xs font-bold text-indigo-500 block mb-1">Phase 2.1</span>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Sanity Sync</h4>
        <p class="text-xs text-gray-500">Categorical factor lock, matrix balancing, and missing value verification.</p>
      </div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm flex flex-col justify-between">
      <div>
        <span class="text-xs font-bold text-indigo-500 block mb-1">Phase 2.2</span>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Inference Testing</h4>
        <p class="text-xs text-gray-500">Kruskal-Wallis and post-hoc Dunn algorithms with BH FDR adjustment.</p>
      </div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm flex flex-col justify-between">
      <div>
        <span class="text-xs font-bold text-indigo-500 block mb-1">Phase 2.3</span>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Decomposition</h4>
        <p class="text-xs text-gray-500">PCA projections to separate resistance and sensitivity phenotypic clusters.</p>
      </div>
    </div>
    <div class="bg-white border border-indigo-100 bg-indigo-50/10 p-4 rounded-xl shadow-sm flex flex-col justify-between">
      <div>
        <span class="text-xs font-bold text-indigo-600 block mb-1">Phase 2.4</span>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Feature Target</h4>
        <p class="text-xs text-indigo-950">One-hot matrix serialization resulting in the production-ready model matrix.</p>
      </div>
    </div>
  </div>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[850px] mx-auto">
    <img src="{{ '/assets/img/gdsc2_eda/workflow_eda.png' | relative_url }}" alt="GDSC2 EDA Pipeline" class="w-full h-auto rounded-xl">
    <div class="text-center text-xs text-gray-400 mt-2 font-mono">
      Figure 2.0: Modular breakdown of the Exploratory and Statistical Learning implementation.
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-4 flex items-center gap-2">
    <i class="fa-solid fa-bezier-curve text-blue-500"></i> Pharmacological Metric Architecture
  </h2>
  <p class="text-gray-700 leading-relaxed mb-6">
    Evaluating cross-metric associations is key to controlling multicollinearity in downstream models. The strong association between $LN(IC_{50})$ and $AUC$ ($r = 0.77$) confirms they monitor the same biological potency signal without collapsing into information redundancy.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 my-6">
  <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
    <img src="{{ '/assets/img/gdsc2_eda/correlation_structure.png' | relative_url }}" alt="Correlation Matrices" class="w-full h-auto rounded-lg">
  </div>
  <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
    <img src="{{ '/assets/img/gdsc2_eda/metrics_consistency.png' | relative_url }}" alt="Metrics Alignment" class="w-full h-auto rounded-lg">
  </div>
</div>

  <blockquote>
    <strong>Machine learning does not discover structure — it learns it.</strong> If the feature metrics show non-linear saturation patterns here, linear algorithms will fail downstream.
  </blockquote>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-flask-vial text-purple-500"></i> Biological Stratification & Non-Parametric Inference
  </h2>

  <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-8">
    <div class="bg-purple-950 text-white p-4 rounded-xl shadow-sm border border-purple-900">
      <span class="text-xs uppercase tracking-wider text-purple-300 font-mono block">Kruskal-Wallis $\chi^2$</span>
      <div class="text-2xl font-bold font-mono mt-1">11,509</div>
      <p class="text-[10px] text-purple-200 mt-1">Degrees of freedom: 31</p>
    </div>
    <div class="bg-purple-950 text-white p-4 rounded-xl shadow-sm border border-purple-900">
      <span class="text-xs uppercase tracking-wider text-purple-300 font-mono block">Asymptotic P-Value</span>
      <div class="text-2xl font-bold font-mono mt-1">&lt; 2.2e-16</div>
      <p class="text-[10px] text-purple-200 mt-1">Highly significant lineage variation</p>
    </div>
    <div class="bg-purple-950 text-white p-4 rounded-xl shadow-sm border border-purple-900">
      <span class="text-xs uppercase tracking-wider text-purple-300 font-mono block">permANOVA $R^2$</span>
      <div class="text-2xl font-bold font-mono mt-1">0.20</div>
      <p class="text-[10px] text-purple-200 mt-1">~20% variance mapped to lineage/pathway</p>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-8 my-6">
    <div class="space-y-4">
      <h3 class="font-bold text-gray-900 flex items-center gap-2 text-base">
        <i class="fa-solid fa-dna text-pink-500"></i> Pathway Enrichment Signals
      </h3>
      <p class="text-sm text-gray-600 leading-relaxed">
        Aggregating compounds by biological mechanism pointed to <strong>Mitosis, Cell Cycle, and Protein Stability & Degradation</strong> as the primary drivers of extreme sensitivity across screen assays, matching established oncology frameworks.
      </p>
      <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
        <img src="{{ '/assets/img/gdsc2_eda/pathway_analysis.png' | relative_url }}" alt="Pathway Analysis" class="w-full h-auto rounded-lg">
      </div>
    </div>

    <div class="space-y-4">
      <h3 class="font-bold text-gray-900 flex items-center gap-2 text-base">
        <i class="fa-solid fa-building-biomedical text-teal-500"></i> Tissue Specificity (Dunn Test Profiling)
      </h3>
      <p class="text-sm text-gray-600 leading-relaxed">
        Post-hoc contrasts mapped intrinsic resistance fields to solid tumors like <strong>PAAD (Pancreatic Adenocarcinoma)</strong>, while hematological cell lines (<strong>LAML, LCML</strong>) cluster uniformly inside the hyper-sensitive spectrum.
      </p>
      <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
        <img src="{{ '/assets/img/gdsc2_eda/tissue_analysis.png' | relative_url }}" alt="Tissue Analysis" class="w-full h-auto rounded-lg">
      </div>
    </div>
  </div>
</div>

<div class="my-12 p-6 border border-gray-100 rounded-2xl bg-white shadow-sm grid grid-cols-1 md:grid-cols-3 gap-6 items-center">
  <div class="md:col-span-1 space-y-3">
    <h3 class="font-bold text-lg text-gray-900 flex items-center gap-2">
      <i class="fa-solid fa-shapes text-indigo-500"></i> Latent Space Mapping (PCA)
    </h3>
    <p class="text-xs text-gray-600 leading-relaxed">
      Principal Component 1 (PC1) captures <strong>~61% of total dataset variance</strong>. Projecting cell line coordinate profiles reveals a structured continuous spectrum going from high sensitivity (left) to established resistance profiles (right).
    </p>
    <div class="bg-indigo-50 text-indigo-950 p-3 rounded-xl border border-indigo-100 text-[11px] font-mono">
      <strong>PC1 Variance:</strong> ~61% <br>
      <strong>Stratification:</strong> Q25 / Median / Q75 <br>
      <strong>Separation Wilcoxon:</strong> p < 2.2e-16
    </div>
  </div>
  <div class="md:col-span-2 border border-gray-100 p-2 rounded-xl bg-white">
    <img src="{{ '/assets/img/gdsc2_eda/pca_latent_space.png' | relative_url }}" alt="PCA Coordinate Space" class="w-full h-auto rounded-lg">
  </div>
</div>

<div class="my-12 pt-6 border-t border-gray-100">
  <h3 class="font-bold text-gray-900 text-sm mb-4">Core Technology Stack</h3>
  <div class="flex flex-wrap gap-2 text-xs font-mono text-gray-600">
    <span class="bg-gray-100 px-2.5 py-1 rounded border">R Language</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">tidyverse</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">factoextra</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">corrplot</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">vegan (permANOVA)</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">fastDummies</span>
  </div>
</div>

<div class="my-12 bg-indigo-950 text-white rounded-2xl p-8 relative overflow-hidden shadow-xl">
  <div class="relative z-10 max-w-xl">
    <span class="text-xs font-bold uppercase tracking-widest text-indigo-300 bg-indigo-900/60 px-2.5 py-1 rounded-full border border-indigo-800">Pipeline Status</span>
    <h3 class="text-2xl font-bold text-white mt-4 mb-2">Matrix Ready for High-Tier Modeling</h3>
    <p class="text-gray-400 text-sm leading-relaxed mb-6">
      The processed artifact <code class="bg-indigo-900 text-indigo-200 px-1.5 py-0.5 rounded font-mono text-xs">GDSC_ML_Ready.csv</code> has been encoded via one-hot procedures, corrected for non-linear saturation traps, and serialized. Ready for ensemble boosting algorithms (XGBoost, LightGBM) and deep neural architectures.
    </p>
  </div>
  <div class="absolute right-4 bottom-4 opacity-10 text-9xl pointer-events-none hidden md:block">
    <i class="fa-solid fa-gears"></i>
  </div>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
