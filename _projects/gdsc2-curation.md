---
layout: page
title: "Project 1: GDSC2 Curation & Integration"
description: "Building an Integrative Dataset for EDA and Predictive Modeling"
bg_color: "#4cc9f0"
icon: "fa-solid fa-laptop-code"
importance: 1
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-cyan-50 to-blue-50 border-l-4 border-cyan-400 p-6 rounded-r-xl mb-8">
    <h2 class="text-xl font-bold text-gray-900 mb-2 flex items-center gap-2">
      <i class="fa-solid fa-crosshairs text-cyan-600"></i> Project Objective
    </h2>
    <p class="text-gray-700 leading-relaxed">
      To integrate, curate, standardize, and quality-control the GDSC2 pharmacogenomic resources into a single reproducible master dataset, suitable for downstream exploratory analysis and machine learning-based prediction of drug sensitivity across cancer types.
    </p>
    <p class="text-gray-700 mt-3 font-medium text-sm text-cyan-800">
      Transformed pipeline links: Drug Response • Cell Line Molecular/Clinical Annotations • Compound Targets
    </p>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 my-6">
    <div class="bg-white border border-gray-100 shadow-sm rounded-xl p-6">
      <h3 class="font-bold text-gray-900 mb-3 flex items-center gap-2 text-base">
        <i class="fa-solid fa-circle-exclamation text-amber-500"></i> The Problem / Scientific Gap
      </h3>
      <ul class="space-y-2 text-sm text-gray-600 list-disc list-inside pl-1">
        <li><strong>Data fragmentation</strong> limits reproducibility and slows model dev.</li>
        <li><strong>Inconsistent annotations</strong> reduce downstream ML workflow quality.</li>
        <li><strong>Poorly standardized response variables</strong> bias predictive metrics.</li>
        <li><strong>Unresolved duplicates/missing values</strong> introduce technical noise.</li>
      </ul>
    </div>

    <div class="bg-white border border-gray-100 shadow-sm rounded-xl p-6">
      <h3 class="font-bold text-gray-900 mb-3 flex items-center gap-2 text-base">
        <i class="fa-solid fa-chart-line text-emerald-500"></i> Strategic Value Proposition
      </h3>
      <ul class="space-y-2 text-sm text-gray-600 list-disc list-inside pl-1">
        <li><strong>Model-Ready Resource:</strong> Tailored directly for ML pipelines.</li>
        <li><strong>Benchmark Framework:</strong> Standard for drug response validation.</li>
        <li><strong>Reproducible Engineering:</strong> Reusable architecture for other omics datasets.</li>
        <li><strong>Publication Grade:</strong> Clean, audit-ready data asset.</li>
      </ul>
    </div>
  </div>
</div>

<div class="my-10">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-4 flex items-center gap-2 border-b pb-2">
    <i class="fa-solid fa-dna text-indigo-500"></i> Scientific Rationale
  </h2>
  <p class="text-gray-700 leading-relaxed mb-6">
    The GDSC2 platform links cancer cell lines with drug response profiles measured under standardized conditions. Because drug sensitivity varies according to both tumor lineage and molecular context, integrating response data with cell line annotations and compound target information enables line-specific comparison, target-pathway evaluation, and deep biomarker discovery using supervised algorithms.
  </p>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-database text-purple-500"></i> Available Source Files
  </h2>
  
  <div class="overflow-x-auto border border-gray-200 rounded-xl shadow-sm mb-8">
    <table class="min-w-full divide-y divide-gray-200 text-sm">
      <thead class="bg-gray-50 text-gray-700 font-semibold">
        <tr>
          <th class="px-6 py-3 text-left">File Name</th>
          <th class="px-6 py-3 text-left">Description</th>
        </tr>
      </thead>
      <tbody class="divide-y divide-gray-100 text-gray-600">
        <tr>
          <td class="px-6 py-4 font-mono font-bold text-indigo-600">GDSC2-dataset.csv</td>
          <td class="px-6 py-4">Contains drug sensitivity profiles, including fitted $IC_{50}$ values for screening compounds.</td>
        </tr>
        <tr class="bg-gray-50/50">
          <td class="px-6 py-4 font-mono font-bold text-indigo-600">Cell_Lines_Details.xlsx</td>
          <td class="px-6 py-4">Provides deep multi-omic baseline details (mutations, CNA, expression, methylation, MSI status).</td>
        </tr>
        <tr>
          <td class="px-6 py-4 font-mono font-bold text-indigo-600">Compounds-annotation.csv</td>
          <td class="px-6 py-4">Structural data regarding screened compounds, targeted pathways, and putative mechanisms.</td>
        </tr>
      </tbody>
    </table>
  </div>
</div>

<div class="my-12 pt-4 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-sliders text-cyan-500"></i> Preprocessing & Variable Standardization
  </h2>
  <p class="text-gray-600 mb-6">
    To transform raw spreadsheets into an analytical resource, data types were strictly cast and scaled. Categorical elements (TCGA labels, tissue types, MSI status) were handled as explicit factors, converting implicit missing fields into an audited <code class="bg-gray-100 px-1.5 py-0.5 rounded text-red-600 font-mono text-xs">"Unknown"</code> string factor to retain row availability.
  </p>

  <div class="bg-gray-50 border border-gray-200 rounded-2xl p-6 mb-8">
    <h3 class="font-bold text-gray-900 mb-4 flex items-center gap-2"><i class="fa-solid fa-chart-bar text-sky-500"></i> Pharmacological Scaling</h3>
    <p class="text-sm text-gray-600 mb-4">
      Four core response variables ($LN(IC_{50})$, $AUC$, $RMSE$, and $Z\text{-SCORE}$) were normalized via Z-score scaling ($\mu=0, \sigma=1$) to stabilize feature distribution weights for downstream distance-based models.
    </p>
  </div>
</div>

<div class="grid grid-cols-1 md:grid-cols-2 gap-8 my-12">
  
  <div class="space-y-4">
    <h3 class="font-bold text-lg text-gray-900 flex items-center gap-2">
      <i class="fa-solid fa-triangle-exclamation text-rose-500"></i> Missing Target Annotations
    </h3>
    <p class="text-sm text-gray-600 leading-relaxed">
      Auditing compound catalogs identified <strong>38 drugs lacking an assigned molecular target</strong>. While these compounds remain valuable for empirical phenotypic profiling, they must be treated as flagged anomalies during strict pathway-enrichment downstream analyses.
    </p>
    <div class="border border-gray-100 p-2 rounded-xl shadow-sm bg-white">
      <img src="{{ '/assets/img/gdsc2/target_analysis.png' | relative_url }}" alt="Missing Target Analysis" class="w-full h-auto rounded-lg">
    </div>
  </div>

  <div class="space-y-4">
    <h3 class="font-bold text-lg text-gray-900 flex items-center gap-2">
      <i class="fa-solid fa-shield-halved text-emerald-500"></i> Phenotypic Outlier Detection
    </h3>
    <p class="text-sm text-gray-600 leading-relaxed">
      By applying a sliding threshold of <strong>$\mu \pm 3\sigma$</strong> on drug-specific $LN(IC_{50})$ vectors, observations were clustered into <em>Extreme Sensitivity</em> or <em>Extreme Resistance</em>. These tails represent key target-dependency signals.
    </p>
    <div class="border border-gray-100 p-2 rounded-xl shadow-sm bg-white">
      <img src="{{ '/assets/img/gdsc2/outlier_distribution.png' | relative_url }}" alt="Outlier Detection" class="w-full h-auto rounded-lg">
    </div>
  </div>

</div>

<div class="my-12 p-6 border border-gray-100 rounded-2xl bg-white shadow-sm grid grid-cols-1 md:grid-cols-3 gap-6 items-center">
  <div class="md:col-span-1 space-y-3">
    <h3 class="font-bold text-lg text-gray-900 flex items-center gap-2">
      <i class="fa-solid fa-wave-square text-indigo-500"></i> Response Variable Distribution
    </h3>
    <p class="text-xs text-gray-600 leading-relaxed">
      The log-transformed $LN(IC_{50})$ distribution displays a clear unimodal structure with a slight left-skewness. This proves variance stabilization succeeded, making the resource exceptionally well-suited for regularized linear frameworks and tree ensembles.
    </p>
    <div class="bg-indigo-50 text-indigo-900 p-3 rounded-xl border border-indigo-100 text-xs font-medium">
      💡 The left-tail expansion confirms enriched sensitivity profiles ready for biomarker extraction.
    </div>
  </div>
  <div class="md:col-span-2 border border-gray-100 p-2 rounded-xl bg-white">
    <img src="{{ '/assets/img/gdsc2/ln_ic50_density.png' | relative_url }}" alt="LN_IC50 Density Plot" class="w-full h-auto rounded-lg">
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-4 flex items-center gap-2">
    <i class="fa-solid fa-diagram-project text-blue-500"></i> Internal Metric Consistency
  </h2>
  <p class="text-sm text-gray-600 mb-6">
    Evaluating cross-metric correlations verified the pipeline's sanity. The strong but imperfect link between $LN(IC_{50})$ and $AUC$ ($\approx 0.77$) confirms that both capture co-dependent biological signals while retaining non-redundant properties. Negative correlation vectors for $RMSE$ map uncertainty to weaker tracking signal lines.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
    <div class="border border-gray-100 p-2 rounded-xl shadow-sm bg-white">
      <img src="{{ '/assets/img/gdsc2/correlation_1.png' | relative_url }}" alt="Correlation Matrices" class="w-full h-auto rounded-lg">
    </div>
    <div class="border border-gray-100 p-2 rounded-xl shadow-sm bg-white">
      <img src="{{ '/assets/img/gdsc2/correlation_2.png' | relative_url }}" alt="Metrics Alignment" class="w-full h-auto rounded-lg">
    </div>
  </div>
</div>

<div class="my-12 bg-gray-950 text-white rounded-2xl p-8 relative overflow-hidden shadow-xl">
  <div class="relative z-10 max-w-xl">
    <span class="text-xs font-bold uppercase tracking-widest text-cyan-400 bg-cyan-950/60 px-2.5 py-1 rounded-full border border-cyan-900">Final Audit Status</span>
    <h3 class="text-2xl font-bold text-white mt-4 mb-2">Dataset Ready for Downstream Engineering</h3>
    <p class="text-gray-400 text-sm leading-relaxed mb-6">
      The structural output <code class="bg-gray-900 text-cyan-300 px-1.5 py-0.5 rounded font-mono text-xs">GDSC2_ReadyForEDA.csv</code> stands validated, un-skewed by constant variables, and normalized for exploratory analytics, multi-omic PCA integrations, and supervised predictive pipelines.
    </p>
  </div>
  <div class="absolute right-4 bottom-4 opacity-10 text-9xl pointer-events-none hidden md:block">
    <i class="fa-solid fa-box-open"></i>
  </div>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
