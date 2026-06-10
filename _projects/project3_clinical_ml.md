---
layout: page
title: "Clinical Predictive Modeling for 6-Month Colorectal Cancer Recurrence"
description: "Benchmarking Parametric Logistic Regression (GLM) against Recursive Partitioning Decision Trees (rpart) to Balance Statistical Interpretability and Patient Stratification in Translational Oncology"
bg_color: "#1e1b4b"
icon: "fa-solid fa-brain"
importance: 6
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-indigo-950 to-slate-950 border-l-4 border-indigo-500 p-6 rounded-r-xl mb-8 shadow-sm">
    <h2 class="text-xl font-bold text-white mb-2 flex items-center gap-2">
      <i class="fa-solid fa-bullseye text-indigo-400"></i> Project Objective & Clinical Philosophy
    </h2>
    <p class="text-indigo-200/90 leading-relaxed text-sm">
      In translational medicine, a highly accurate model is useless if clinicians cannot audit how decisions are made. This project implements an end-to-end machine learning and biostatistics workflow in R to predict 6-month tumor recurrence in post-treatment Colorectal Cancer (CRC) patients. By benchmarking <strong>Logistic Regression</strong> against a <strong>Classification Decision Tree (rpart)</strong>, the pipeline demonstrates how to translate raw statistical parameters into clear visual decision pathways optimized for clinical tumor boards.
    </p>
    <div class="mt-4 flex flex-wrap gap-2 text-[11px] font-mono text-indigo-300">
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Logistic Regression (GLM)</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Classification Trees (rpart)</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Clinical Biomarkers (CEA)</span>
    </div>
  </div>

  <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center shadow-sm max-w-[380px] mx-auto mb-6">
    <span class="text-[10px] font-mono text-indigo-600 font-bold block mb-1">HEALTHAI & PRECISION MEDICINE core</span>
    <h4 class="font-bold text-slate-800 text-xs">The Right Model for the Right Clinical Question</h4>
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-database text-indigo-600"></i> Clinical Features & Architecture
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    The predictive pipeline ingests standardized post-treatment oncology records structured across key physiological and laboratory markers:
  </p>

  <div class="grid grid-cols-1 sm:grid-cols-4 gap-4 text-xs font-mono mb-8">
    <div class="bg-white border p-4 rounded-xl shadow-sm border-l-4 border-indigo-500">
      <strong class="text-gray-900 block mb-1">Age</strong>
      Patient's age at evaluation (continuous variable capturing age-associated biological decline).
    </div>
    <div class="bg-white border p-4 rounded-xl shadow-sm border-l-4 border-indigo-500">
      <strong class="text-gray-900 block mb-1">Sex</strong>
      Biological sex structured as a categorical factor (Female / Male) to audit demographic biases.
    </div>
    <div class="bg-white border p-4 rounded-xl shadow-sm border-l-4 border-emerald-500">
      <strong class="text-emerald-700 block mb-1">CEA_level</strong>
      Carcinoembryonic Antigen in ng/mL. A key oncological continuous tumor biomarker.
    </div>
    <div class="bg-white border p-4 rounded-xl shadow-sm border-l-4 border-slate-700">
      <strong class="text-slate-900 block mb-1">Recurrence_6m</strong>
      Ground truth binary label (1 = Recurrence, 0 = Remission/No Recurrence) evaluated post-therapy.
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-calculator text-indigo-600"></i> Model 1: Parametric Rigor via Logistic Regression
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    Implemented using a Generalized Linear Model (GLM) with a binomial logit link. Rather than acting as a black-box classifier, it quantifies precise directional risk variations by exponentiating raw log-odds ($\beta$) into <strong>Odds Ratios (OR)</strong>.
  </p>

  <div class="bg-slate-900 text-white p-4 rounded-xl font-mono text-xs shadow-md mb-6">
    <span class="text-slate-500 block mb-2"># R Execution - Interpretable Parametric Baseline</span>
    log_model <- glm(Recurrence_6m ~ Age + Sex + CEA_level, data = train_data, family = binomial)
  </div>

  <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm max-w-[550px] mx-auto my-6">
    <img src="{{ '/assets/img/clinical_ml/coefficients_table.png' | relative_url }}" alt="R Summary GLM Coefficients Table" class="w-full h-auto rounded-lg">
    <div class="text-center text-[10px] text-gray-400 mt-1 font-mono">
      Figure 3.1: Statistical summary output showing Wald test statistics and p-value significance tiers.
    </div>
  </div>

  <div class="bg-indigo-50/50 border border-indigo-100 rounded-xl p-5 text-xs text-slate-700 leading-relaxed my-6">
    <h4 class="font-bold text-indigo-900 mb-2 font-mono flex items-center gap-1"><i class="fa-solid fa-chart-pie"></i> De-shrouding the R Outputs & Clinically Calibrated Risk</h4>
    <ul class="list-disc pl-5 space-y-2">
      <li><strong>CEA Level ($p < 0.001$, $OR = 2.74$):</strong> Highly significant. Holding other covariates constant, every 1 ng/mL increase in blood CEA levels multiplies the odds of experiencing a 6-month tumor recurrence by <strong>2.74 times</strong>.</li>
      <li><strong>Age ($p = 0.0054$, $OR = 1.047$):</strong> Shows a steady, distinct increment of ~4.6% in recurrence odds per additional year of age.</li>
      <li><strong>Sex ($p = 0.562$):</strong> Displays no statistical significance in this patient cohort, prompting feature elimination parameters.</li>
      <li><strong>The Caret Sorting Trap Audited:</strong> Due to automatic alphabetical sorting during confusion matrix generation, standard packages often evaluate non-recurrence ("0") as the positive class. This pipeline explicitly re-aligns interpretation metrics to prioritize minimizing false negatives—ensuring high-risk relapse trajectories are never missed.</li>
    </ul>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 my-8">
    <div class="border border-gray-100 p-3 rounded-xl bg-white shadow-sm text-center">
      <img src="{{ '/assets/img/clinical_ml/ROC_logistic.png' | relative_url }}" alt="ROC Curve Logistic Regression" class="w-full h-auto rounded-lg mx-auto">
      <span class="text-[10px] text-gray-400 font-mono mt-2 block">Figure 3.2: Logistic Regression ROC curve displaying strong probabilistic discrimination (AUC: 0.9348).</span>
    </div>
    <div class="bg-gray-50 rounded-xl p-5 flex flex-col justify-center text-xs text-gray-600 border">
      <h5 class="font-bold text-gray-900 mb-2 font-mono uppercase tracking-wider">GLM Performance Metrics</h5>
      <table class="w-full text-left font-mono text-[11px]">
        <tr class="border-b"><td class="py-1.5 font-bold">Accuracy:</td><td class="py-1.5 text-indigo-600">0.7750 (77.5%)</td></tr>
        <tr class="border-b"><td class="py-1.5 font-bold">AUC-ROC:</td><td class="py-1.5 text-indigo-600">0.9348</td></tr>
        <tr class="border-b"><td class="py-1.5 font-bold">Cohen’s Kappa:</td><td class="py-1.5 text-indigo-600">0.5545 (Moderate-to-Good agreement)</td></tr>
        <tr class="border-b"><td class="py-1.5 font-bold">Sensitivity:</td><td class="py-1.5 text-indigo-600">0.8947</td></tr>
        <tr><td class="py-1.5 font-bold">Specificity:</td><td class="py-1.5 text-indigo-600">0.6667</td></tr>
      </table>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-diagram-project text-indigo-600"></i> Model 2: Recursive Partitioning Classification Trees
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    To maximize usability during multi-disciplinary tumor board evaluations, a non-parametric recursive partitioning tree (<code>rpart</code>) was trained. This algorithm automatically defines categorical stratification rules that mimic clinical decision trees.
  </p>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[650px] mx-auto my-8">
    <img src="{{ '/assets/img/clinical_ml/Decision_tree.png' | relative_url }}" alt="Oncology Classification Decision Tree Layout" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 3.3: Recursive partitioning tree mapping algorithmic rules for 6-month patient relapse stratification.
    </div>
  </div>

  <div class="bg-slate-900 text-white rounded-2xl p-6 shadow-xl my-8 font-sans">
    <h3 class="text-base font-bold text-emerald-400 mb-3 font-mono flex items-center gap-2">
      <i class="fa-solid fa-network-wired"></i> Algorithmic Rules Parsed from the Tree Topology
    </h3>
    <div class="space-y-3 text-xs leading-relaxed text-slate-300 font-mono">
      <div class="flex items-start gap-2"><i class="fa-solid fa-chevron-right text-emerald-400 mt-0.5"></i> <span><strong class="text-white">High-Risk Stratum A:</strong> CEA level $\ge$ 5.7 ng/mL directly triggers a <span class="text-red-400 font-bold">84% probability of tumor recurrence</span> (comprising 40% of the entire sample size).</span></div>
      <div class="flex items-start gap-2"><i class="fa-solid fa-chevron-right text-emerald-400 mt-0.5"></i> <span><strong class="text-white">High-Risk Subgroup B:</strong> CEA levels between 3.5 and 5.7 ng/mL coupled with an Age $\ge$ 65 years isolates a distinct <span class="text-red-400 font-bold">80% probability of recurrence</span>.</span></div>
      <div class="flex items-start gap-2"><i class="fa-solid fa-chevron-right text-emerald-400 mt-0.5"></i> <span><strong class="text-white">Low-Risk Safe Zone:</strong> Patients presenting a CEA level $<$ 3.5 ng/mL align with a minimal <span class="text-emerald-400 font-bold">4% probability of recurrence</span> (17% of total cohort).</span></div>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 my-8">
    <div class="border border-gray-100 p-3 rounded-xl bg-white shadow-sm text-center">
      <img src="{{ '/assets/img/clinical_ml/ROC-decisionTree.png' | relative_url }}" alt="ROC Curve Decision Tree Classifier" class="w-full h-auto rounded-lg mx-auto">
      <span class="text-[10px] text-gray-400 font-mono mt-2 block">Figure 3.4: Classification Tree ROC curve mapping categorical decision split efficiency (AUC: 0.8835).</span>
    </div>
    <div class="bg-gray-50 rounded-xl p-5 flex flex-col justify-center text-xs text-gray-600 border">
      <h5 class="font-bold text-gray-900 mb-2 font-mono uppercase tracking-wider">Decision Tree Metrics Summary</h5>
      <table class="w-full text-left font-mono text-[11px]">
        <tr class="border-b"><td class="py-1.5 font-bold">Overall Accuracy:</td><td class="py-1.5 text-emerald-600 font-bold">0.8250 (82.5%)</td></tr>
        <tr class="border-b"><td class="py-1.5 font-bold">AUC-ROC:</td><td class="py-1.5 text-slate-600">0.8835</td></tr>
        <tr class="border-b"><td class="py-1.5 font-bold">Cohen’s Kappa:</td><td class="py-1.5 text-emerald-600">0.6535 (Strong Reliability)</td></tr>
        <tr class="border-b"><td class="py-1.5 font-bold">Sensitivity:</td><td class="py-1.5 text-emerald-600">0.9474 (Superior Detection)</td></tr>
        <tr><td class="py-1.5 font-bold">Specificity:</td><td class="py-1.5 text-emerald-600">0.7143</td></tr>
      </table>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-scale-balanced text-indigo-600"></i> Benchmarking Conclusions: Translational Evaluation
  </h2>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-xs text-gray-600">
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm border-t-4 border-indigo-500">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-chart-line text-indigo-600"></i> When to deploy Logistic Regression
      </h4>
      Perfect for epidemiology and pharmacological risk decoding. It provides continuous probability values and mathematically describes how individual continuous variables (such as exact CEA changes) scale risk through strict Odds Ratios.
    </div>
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm border-t-4 border-emerald-500">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-hospital-user text-emerald-600"></i> When to deploy Decision Trees
      </h4>
      Outperformed GLM in raw accuracy (82.5% vs 77.5%) and achieved a massive 94.74% sensitivity. It excels when rapid, strict triage protocols are needed, or when explaining complex patient stratification rules to multidisciplinary medical staff.
    </div>
  </div>
</div>

<div class="my-8 pt-4 border-t border-gray-100 text-xs text-gray-400 font-mono">
  📁 Project Deployment & Reproducibility Core:
  <ul class="list-disc pl-5 mt-2 space-y-1">
    <li>Architecture Core: Evaluated on R Programming Stack (<code>tidyverse</code>, <code>caret</code>, <code>rpart</code>, <code>rpart.plot</code>, <code>pROC</code>).</li>
    <li>Source Code Repositories: <a class="text-indigo-400 hover:underline" href="https://github.com/davidvillafan96/clinical-colorectal-cancer-recurrence_prediction.git" target="_blank">Clinical Colorectal Cancer Recurrence Production Codebase</a></li>
  </ul>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
