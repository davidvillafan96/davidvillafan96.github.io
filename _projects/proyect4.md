---
layout: page
title: "Project 4: Genomic Integration for Drug Response Prediction"
description: "Transitioning from Statistical Pharmacogenomics to Genomics-Driven Predictive Modeling"
bg_color: "#0f172a"
icon: "fa-solid fa-dna"
importance: 4
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-slate-900 to-indigo-950 border-l-4 border-emerald-500 p-6 rounded-r-xl mb-8 shadow-sm">
    <h2 class="text-xl font-bold text-white mb-2 flex items-center gap-2">
      <i class="fa-solid fa-bullseye text-emerald-400"></i> Project Objective
    </h2>
    <p class="text-indigo-200/90 leading-relaxed text-sm">
      Advancing from exploratory multi-algorithmic testing into <strong>genomics-driven predictive systems</strong>. This final phase integrates binary mutational matrices from COSMIC into the GDSC drug screening architecture to unlock biological interpretability, isolate context-specific resistance biomarkers, and achieve near-experimental predictive accuracy.
    </p>
    <div class="mt-4 flex flex-wrap gap-2 text-[11px] font-mono text-emerald-300">
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">COSMIC Integration</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">LASSO Regularization</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Epistatic Context Modeling</span>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-4 my-6">
    <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center opacity-60">
      <span class="text-[10px] font-mono text-gray-400 block mb-1">PHASE 2</span>
      <h4 class="font-bold text-gray-700 text-xs">Statistical Inference & EDA</h4>
    </div>
    <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center opacity-60">
      <span class="text-[10px] font-mono text-gray-400 block mb-1">PHASE 3</span>
      <h4 class="font-bold text-gray-700 text-xs">Machine Learning Frameworks</h4>
    </div>
    <div class="bg-slate-900 text-white p-4 rounded-xl text-center shadow-md ring-1 ring-emerald-500/30">
      <span class="text-[10px] font-mono text-emerald-400 font-bold block mb-1">CURRENT MILESTONE</span>
      <h4 class="font-bold text-emerald-100 text-xs">Project 4: Genomic Integration</h4>
    </div>
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-network-wired text-emerald-600"></i> High-Dimensional Feature Engineering Pipeline
  </h2>
  <p class="text-sm text-gray-600 mb-8 leading-relaxed">
    By expanding our tabular matrix with over 750 functional genomic somatic mutation profiles from COSMIC, the framework shifts from predicting drug response based purely on drug classes or tissue origins to uncovering specific genomic alterations that dictate cellular sensitivity or resistance.
  </p>

  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 mb-10">
    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm hover:border-emerald-200 transition-colors">
      <div class="w-8 h-8 rounded-lg bg-emerald-50 flex items-center justify-center text-emerald-600 mb-3 font-mono font-bold text-xs">01</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Multi-Omic Merge</h4>
      <p class="text-[11px] text-gray-500 leading-normal">Programmatic integration of GDSC pharmacological target vectors ($LN(IC_{50})$) with corresponding COSMIC binary mutational catalogs.</p>
    </div>

    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm hover:border-emerald-200 transition-colors">
      <div class="w-8 h-8 rounded-lg bg-emerald-50 flex items-center justify-center text-emerald-600 mb-3 font-mono font-bold text-xs">02</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Feature Pruning</h4>
      <p class="text-[11px] text-gray-500 leading-normal">Filtering sparse and non-informative somatic variants. Down-selecting 750+ candidate markers into 54 high-efficiency predictive features.</p>
    </div>

    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm hover:border-emerald-200 transition-colors">
      <div class="w-8 h-8 rounded-lg bg-emerald-50 flex items-center justify-center text-emerald-600 mb-3 font-mono font-bold text-xs">03</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Dual Core Framework</h4>
      <p class="text-[11px] text-gray-500 leading-normal">Deploying parallel Regularized Linear Models (LASSO) and Non-linear Ensembles (Random Forest) to capture both additive and epistatic effects.</p>
    </div>

    <div class="bg-white border border-emerald-100 bg-emerald-50/10 p-5 rounded-xl shadow-sm">
      <div class="w-8 h-8 rounded-lg bg-emerald-100 flex items-center justify-center text-emerald-600 mb-3 font-mono font-bold text-xs">04</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Contextual Modeling</h4>
      <p class="text-[11px] text-gray-600 leading-normal">Isolating target-gene interaction clusters to distinguish intrinsic single-locus drivers from intricate network-level dependencies.</p>
    </div>
  </div>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[850px] mx-auto mb-10">
    <img src="{{ '/assets/img/gdsc2_ml/project4_workflow.png' | relative_url }}" alt="Genomic Integration Pipeline Workflow" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 4.0: End-to-end data integration, genomic feature filtering, and parallel model execution workflow.
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <div class="flex flex-col md:flex-row md:items-center justify-between mb-6">
    <div>
      <h2 class="text-2xl font-bold text-gray-900 tracking-tight flex items-center gap-2">
        <i class="fa-solid fa-flask-vial text-emerald-600"></i> Biomarker Discovery & Statistical Significance
      </h2>
      <p class="text-xs text-gray-500 mt-1">Isolating high-impact genomic alterations via binomial logit modeling and volcano distribution criteria.</p>
    </div>
  </div>

  <div class="border border-gray-100 rounded-2xl bg-white shadow-sm overflow-hidden my-6">
    <table class="w-full text-left border-collapse">
      <thead>
        <tr class="bg-gray-50 border-b border-gray-100 text-[11px] font-mono font-bold text-gray-500 uppercase tracking-wider">
          <th class="p-4">Candidate Gene</th>
          <th class="p-4">Statistical Weight (P-value)</th>
          <th class="p-4">Odds Ratio (OR)</th>
          <th class="p-4">Functional Biological Interpretation</th>
        </tr>
      </thead>
      <tbody class="divide-y divide-gray-50 text-xs">
        <tr>
          <td class="p-4 font-bold text-slate-900">KRAS</td>
          <td class="p-4 font-mono text-gray-600">~1e-43</td>
          <td class="p-4 font-mono text-gray-600">1.34</td>
          <td class="p-4 text-gray-500"><strong>Statistical giant:</strong> Extremely robust and highly consistent signal across the entire screening dataset regardless of tissue lineage.</td>
        </tr>
        <tr>
          <td class="p-4 font-bold text-slate-900">GLI1</td>
          <td class="p-4 font-mono text-gray-600">~1e-35</td>
          <td class="p-4 font-mono text-gray-600">2.43</td>
          <td class="p-4 text-gray-500"><strong>Effect driver:</strong> Prominent role linked to a strong and systematic therapy escape/resistance phenotype.</td>
        </tr>
        <tr>
          <td class="p-4 font-bold text-slate-900">TPR</td>
          <td class="p-4 font-mono text-gray-600">~1e-35</td>
          <td class="p-4 font-mono text-gray-600">2.30</td>
          <td class="p-4 text-gray-500">High-impact somatic mutation leading to widespread downstream pharmacological response alterations.</td>
        </tr>
        <tr>
          <td class="p-4 font-bold text-slate-900">RBM10</td>
          <td class="p-4 font-mono text-gray-600">~1e-22</td>
          <td class="p-4 font-mono text-gray-600">2.68</td>
          <td class="p-4 text-emerald-700 font-medium"><strong>Strongest overall effect size:</strong> Clear mechanistic driver correlated with highly specialized resistance traits.</td>
        </tr>
        <tr class="bg-emerald-50/10">
          <td class="p-4 font-bold text-emerald-950">TP63 / MUC4 / DCC / MUC16 / RAD51B</td>
          <td class="p-4 font-mono text-emerald-900">~1e-22</td>
          <td class="p-4 font-mono text-emerald-900">~1.96</td>
          <td class="p-4 text-emerald-800"><strong>Co-occurring cluster:</strong> Signals a highly correlated shared genomic event, likely linked to large-scale chromosomal alterations.</td>
        </tr>
      </tbody>
    </table>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-6 max-w-[850px] mx-auto">
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/gdsc2_ml/project4_volcano.png' | relative_url }}" alt="Volcano Plot of Genomic Resistance Biomarkers" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">Biomarcadores de Resistencia Significativos</div>
    </div>
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/gdsc2_ml/project4_volcano_global.png' | relative_url }}" alt="Global Genomic Biomarkers Volcano Distribution" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">Distribución Global (Sensibilidad vs Resistencia)</div>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <div class="flex flex-col md:flex-row md:items-center justify-between mb-6">
    <div>
      <h2 class="text-2xl font-bold text-gray-900 tracking-tight flex items-center gap-2">
        <i class="fa-solid fa-chart-line text-blue-500"></i> Model Optimization & Predictive Metrics
      </h2>
      <p class="text-xs text-gray-500 mt-1">Benchmarking predictive error patterns across progressive integration layers.</p>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-4 my-6">
    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm">
      <span class="text-[10px] font-mono text-gray-400 block mb-1">BASELINE MATRIX</span>
      <h4 class="font-bold text-gray-800 text-sm mb-2">Before Genomic Integration</h4>
      <div class="flex items-baseline gap-2">
        <span class="text-2xl font-extrabold text-gray-400 font-mono">0.98</span>
        <span class="text-xs text-gray-400 font-mono">Test RMSE</span>
      </div>
      <p class="text-[11px] text-gray-500 mt-2">Predictions strictly restricted to generic tissue origins, compound labels, and baseline pathway profiles.</p>
    </div>

    <div class="bg-white border border-emerald-100 p-5 rounded-xl shadow-sm relative overflow-hidden">
      <div class="absolute top-0 right-0 w-16 h-16 bg-emerald-500/5 rounded-full blur-lg"></div>
      <span class="text-[10px] font-mono font-bold text-emerald-600 block mb-1">INTEGRATED MATRIX</span>
      <h4 class="font-bold text-gray-900 text-sm mb-2">With COSMIC Mutations</h4>
      <div class="flex items-baseline gap-2">
        <span class="text-3xl font-extrabold text-slate-900 font-mono">0.89</span>
        <span class="text-xs text-emerald-600 font-mono font-bold">~10% Error Drop</span>
      </div>
      <p class="text-[11px] text-gray-600 mt-2">Significant error reduction, validating somatic variation records as an essential precision layer in biological systems.</p>
    </div>

    <div class="bg-slate-900 text-white p-5 rounded-xl shadow-md relative overflow-hidden">
      <div class="absolute top-0 right-0 w-16 h-16 bg-blue-500/10 rounded-full blur-lg"></div>
      <span class="text-[10px] font-mono text-blue-400 font-bold block mb-1">OPTIMAL SYSTEM CONFIGURATION</span>
      <h4 class="font-bold text-slate-100 text-sm mb-2">With Drug Identity Layer</h4>
      <div class="flex items-baseline gap-2">
        <span class="text-3xl font-extrabold text-blue-400 font-mono">0.52</span>
        <span class="text-xs text-blue-300 font-mono font-semibold">Experimental Level</span>
      </div>
      <p class="text-[11px] text-slate-300 mt-2">Maximum optimization tier capturing full architectural variance within drug-cell screening landscapes.</p>
    </div>
  </div>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[650px] mx-auto my-8">
    <img src="{{ '/assets/img/gdsc2_ml/project4_lasso.png' | relative_url }}" alt="LASSO Feature Coefficients Insights" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 4.1: LASSO regularization path explaining 75.6% ($R^2$) of localized model variance.
    </div>
  </div>

  <div class="bg-blue-50/40 border border-blue-100 rounded-xl p-4 text-xs text-slate-700 leading-relaxed my-6">
    <h5 class="font-bold text-blue-900 mb-1 flex items-center gap-1"><i class="fa-solid fa-circle-info"></i> Machine Learning Behavior & Biological Insights</h5>
    While non-linear architectures like <strong>Random Forest</strong> isolate global feature distributions (identifying <em>KRAS</em> as the apex biological contributor), regularized linear models via <strong>LASSO</strong> reveal complex epistatic links. For instance, LASSO excludes independent <em>KRAS</em> coefficients but selects the <strong>KRAS × MAPK</strong> interaction vector, proving programmatically that <em>KRAS</em> mutations trigger selective sensitivity exclusively within active MAPK pathway networks.
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-chart-gantt text-indigo-600"></i> Prediction Distribution & Mutation-Level Trends
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    Evaluating model outputs against actual screening responses demonstrates a clear positive predictive correlation, confirming the pipeline captures genuine biological signal despite inherent technical screening noise.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-6 max-w-[850px] mx-auto">
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/gdsc2_ml/project4_prediction_trend.png' | relative_url }}" alt="Observed vs Predicted LN_IC50 Trend" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">Observed vs. Predicted Distribution</div>
    </div>
    <div class="border border-gray-100 p-2 rounded-xl bg-white shadow-sm">
      <img src="{{ '/assets/img/gdsc2_ml/project4_kras_effects_2.png' | relative_url }}" alt="Diferencias de Sensibilidad por Mutación y Tejido" class="w-full h-auto rounded-lg">
      <div class="text-[10px] text-gray-400 font-mono mt-1.5 text-center">Comparativa de LN_IC50 por Gen, Estado y Tejido</div>
    </div>
  </div>

  <div class="bg-gray-50 border border-gray-100 rounded-xl p-4 text-xs text-gray-600 leading-relaxed">
    <strong>Distribution Takeaways:</strong> The prediction trend exhibits highly conservative boundaries; it perfectly captures sample rankings and major shifts but displays conservative performance on extreme tail responses due to biological noise. Grouping samples by mutation profile (e.g., <em>KRAS</em> mutant vs. wild-type) reveals a significant, reproducible shift in continuous $LN(IC_{50})$ distributions across multiple distinct tissue origins.
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-link text-teal-600"></i> High-Confidence Gene–Drug Interdependence
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    By mapping statistical significance against effect direction, the following selected interactions represent major discovery avenues isolated by the integrated multi-omic framework:
  </p>

  <div class="border border-gray-100 rounded-2xl bg-white shadow-sm overflow-hidden my-6">
    <table class="w-full text-left border-collapse">
      <thead>
        <tr class="bg-gray-50 border-b border-gray-100 text-[11px] font-mono font-bold text-gray-500 uppercase tracking-wider">
          <th class="p-4">Identified Gene</th>
          <th class="p-4">Associated Compound</th>
          <th class="p-4">Pipeline Functional Insight</th>
        </tr>
      </thead>
      <tbody class="divide-y divide-gray-50 text-xs text-gray-600">
        <tr>
          <td class="p-4 font-semibold text-gray-900">GLI1</td>
          <td class="p-4 font-mono text-indigo-600">Remodelin</td>
          <td class="p-4">Uncovers a potential high-sensitivity therapeutic axis, identifying an actionable target pocket.</td>
        </tr>
        <tr>
          <td class="p-4 font-semibold text-gray-900">KRAS</td>
          <td class="p-4 font-mono text-indigo-600">Mycophenolic acid</td>
          <td class="p-4">Strictly context-specific relationship; therapeutic efficacy depends entirely on broader pathway states.</td>
        </tr>
        <tr>
          <td class="p-4 font-semibold text-gray-900">RBM10</td>
          <td class="p-4 font-mono text-indigo-600">Bicalutamide</td>
          <td class="p-4 text-teal-700 font-medium">Exhibits a highly robust, reproducible statistical association indicating selective resistance patterns.</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-signature text-purple-600"></i> Final Functional Biomarker Signature
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    The integrated discovery pipeline consolidates four critical genomic focal points acting as the core criteria for therapeutic stratification:
  </p>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-6 text-xs">
    <div class="border border-gray-100 p-4 rounded-xl bg-white shadow-sm">
      <span class="font-mono text-purple-600 font-bold block mb-1">01 / MITOSIS PATHWAY ALTERATIONS</span>
      <p class="text-gray-600 leading-relaxed">Acts as a primary structural driver of multi-compound cellular sensitivity across continuous testing models.</p>
    </div>
    <div class="border border-gray-100 p-4 rounded-xl bg-white shadow-sm">
      <span class="font-mono text-purple-600 font-bold block mb-1">02 / KRAS × MAPK INTERACTION</span>
      <p class="text-gray-600 leading-relaxed">Context-specific sensitivity marker showing that oncogenic signaling is highly dependent on neighboring cascade states.</p>
    </div>
    <div class="border border-gray-100 p-4 rounded-xl bg-white shadow-sm">
      <span class="font-mono text-purple-600 font-bold block mb-1">03 / CDH1 EXPRESSION CONTEXT</span>
      <p class="text-gray-600 leading-relaxed">Functions as an independent genomic sensitivity marker, showing robust prediction stability across various lineages.</p>
    </div>
    <div class="border border-gray-100 p-4 rounded-xl bg-white shadow-sm">
      <span class="font-mono text-purple-600 font-bold block mb-1">04 / RBM10 MUTATIONAL INACTIVATION</span>
      <p class="text-gray-600 leading-relaxed">Isolated as a direct, high-impact biomarker for systemic drug resistance across multiple therapeutic compound screenings.</p>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-hospital-user text-teal-600"></i> Translational Impact & Clinical Case
  </h2>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
    <div class="flex flex-col p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-teal-50 flex items-center justify-center text-teal-600 mb-4 shrink-0">
        <i class="fa-solid fa-sliders"></i>
      </div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Clinical Decision Support</h4>
      <p class="text-xs text-gray-600 leading-relaxed">
        Provides an advanced computational screening layer capable of forecasting compound response patterns using pre-treatment patient mutation screenings.
      </p>
    </div>

    <div class="flex flex-col p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-purple-50 flex items-center justify-center text-purple-600 mb-4 shrink-0">
        <i class="fa-solid fa-dna"></i>
      </div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Biomarker Discovery Engine</h4>
      <p class="text-xs text-gray-600 leading-relaxed">
        Systematically discovers underlying escape mutations and network-level resistance mechanics before executing physical drug development protocols.
      </p>
    </div>

    <div class="flex flex-col p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-blue-50 flex items-center justify-center text-blue-600 mb-4 shrink-0">
        <i class="fa-solid fa-flask"></i>
      </div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Drug Screening Accelerator</h4>
      <p class="text-xs text-gray-600 leading-relaxed">
        Enables high-throughput parallel multi-compound runs <em>in silico</em>, drastically lowering physical workspace costs and focusing resources on highly viable matches.
      </p>
    </div>
  </div>
</div>

<div class="my-12 pt-6 border-t border-gray-100">
  <h3 class="font-bold text-gray-900 text-xs mb-4 uppercase tracking-wider font-mono text-gray-400">Pipeline Engineering Limitations</h3>
  <div class="flex flex-wrap gap-2 text-[10px] font-mono text-gray-500">
    <span class="bg-gray-100 px-2.5 py-1 rounded border">Binary Mutation Constraints (Absence/Presence Only)</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">Excludes Transcriptomic/Epigenomic Covariates</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">Residual Screen Noise Inherent to High-Throughput Assays</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">Moderate Class Imbalance in Hyper-Sensitive Segments</span>
  </div>
</div>

<div class="my-12 bg-gradient-to-r from-slate-900 to-indigo-950 text-white rounded-2xl p-8 relative overflow-hidden shadow-xl border border-white/5">
  <div class="relative z-10 max-w-2xl">
    <span class="text-[10px] font-bold uppercase tracking-widest text-emerald-400 bg-emerald-950/60 px-2.5 py-1 rounded-full border border-emerald-900">Series Summary Takeaway</span>
    <h3 class="text-2xl font-bold text-white mt-4 mb-2">Genomics is not optional — it is the key layer that unlocks precision modeling.</h3>
    <p class="text-indigo-200/80 text-xs leading-relaxed mb-6">
      This multi-project series successfully traces the path from raw data wrangling and statistical validation to highly structured, machine-learning-driven pharmacogenomic discovery workflows.
    </p>
    <div class="text-xs font-semibold text-emerald-400 flex items-center gap-1">
      Framework Evolution: Raw Integration <i class="fa-solid fa-arrow-right text-[10px]"></i> Tabular ML Systems <i class="fa-solid fa-arrow-right text-[10px]"></i> Genomics-Driven Discovery
    </div>
  </div>
  <div class="absolute right-4 bottom-4 opacity-5 text-9xl pointer-events-none hidden md:block">
    <i class="fa-solid fa-dna"></i>
  </div>
</div>

<div class="my-8 pt-4 border-t border-gray-100 text-xs text-gray-400 font-mono">
  📁 Project References & Series Pipeline Hierarchy:
  <ul class="list-disc pl-5 mt-2 space-y-1">
    <li>Previous Milestone: <a class="text-indigo-600 hover:underline" href="https://davidvillafan96.github.io/projects/project3/">Project 3 — Tabular Machine Learning Core Systems</a></li>
    <li>Source Code Repositories: <a class="text-indigo-600 hover:underline" href="https://github.com/davidvillafan96/gdsc-genomic-biomarker-discovery" target="_blank">Precision Discovery Codebase</a></li>
  </ul>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
