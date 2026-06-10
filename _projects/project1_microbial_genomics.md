---
layout: page
title: "Microbial Genomics Project 1: Comparative Genomics & Functional Feature Profiling for PGPR Candidate Selection"
description: "An Automated Unsupervised Pipeline Intersecting PLaBase Annotation Data, Z-score Feature Matrices, and Hierarchical Clustering to Predict Rhizosphere Colonization Success"
bg_color: "#022c22"
icon: "fa-solid fa-bacterium"
importance: 7
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-emerald-950 to-teal-950 border-l-4 border-emerald-500 p-6 rounded-r-xl mb-8 shadow-sm">
    <h2 class="text-xl font-bold text-white mb-2 flex items-center gap-2">
      <i class="fa-solid fa-bullseye text-emerald-400"></i> Project Objective
    </h2>
    <p class="text-emerald-200/90 leading-relaxed text-sm">
      Translating raw microbial genome annotations into structured feature spaces to identify novel, high-efficiency Plant Growth-Promoting Rhizobacteria (PGPR). This automated computational pipeline benchmark-profiles newly isolated wild strains against an industry-standard matrix of reference commercial biological inputs and control strains, predicting their capacity to successfully colonize diverse botanical niches and exert downstream bio-stimulatory phenotypes.
    </p>
    <div class="mt-4 flex flex-wrap gap-2 text-[11px] font-mono text-emerald-300">
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Comparative Genomics</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">PLaBase Data Mining</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Hierarchical Clustering (R)</span>
    </div>
  </div>

  <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center shadow-sm max-w-[350px] mx-auto mb-6">
    <span class="text-[10px] font-mono text-emerald-600 font-bold block mb-1">AGTECH & SUSTAINABLE AGRICULTURE</span>
    <h4 class="font-bold text-slate-800 text-xs">Microbial Genomics & Bio-Input Discovery Core</h4>
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-layer-group text-emerald-600"></i> Methodological Framework & Analytical Design
  </h2>
  <p class="text-sm text-gray-600 mb-8 leading-relaxed">
    The architecture encodes high-dimensional annotation data derived from the open-access platform <strong>PLaBase</strong> (Plant-Associated Bacteria Database) into scalable quantitative feature matrices, removing technical frequency biases via rigorous normalization boundaries.
  </p>

  <div class="border border-gray-100 rounded-2xl bg-white shadow-sm overflow-hidden mb-8">
    <div class="bg-gray-50 p-4 border-b border-gray-100 flex items-center gap-2">
      <i class="fa-solid fa-gears text-emerald-600 text-sm"></i>
      <span class="text-xs font-mono font-bold text-gray-700 uppercase tracking-wider">Step-by-Step Computational Workflow</span>
    </div>
    <div class="p-6 text-xs text-gray-600 space-y-4 font-mono">
      <div class="flex items-start gap-3">
        <span class="bg-emerald-100 text-emerald-800 font-bold px-2 py-0.5 rounded text-[10px]">01</span>
        <div><strong class="text-gray-900">Batch Interaction File Import:</strong> Automated parsing and ingestion of diverse functional genomic annotation logs across all isolated microbial targets.</div>
      </div>
      <div class="flex items-start gap-3">
        <span class="bg-emerald-100 text-emerald-800 font-bold px-2 py-0.5 rounded text-[10px]">02</span>
        <div><strong class="text-gray-900">Functional Block Aggregation:</strong> Condensing raw structural hits into aggregated biological programs and computing strict frequency summary arrays.</div>
      </div>
      <div class="flex items-start gap-3">
        <span class="bg-emerald-100 text-emerald-800 font-bold px-2 py-0.5 rounded text-[10px]">03</span>
        <div><strong class="text-gray-900">Feature Matrix Construction:</strong> Compiling an unified high-dimensional genomic feature space structured as <em>Functional Blocks &times; Microbial Isolates</em>.</div>
      </div>
      <div class="flex items-start gap-3">
        <span class="bg-emerald-100 text-emerald-800 font-bold px-2 py-0.5 rounded text-[10px]">04</span>
        <div><strong class="text-gray-900">Row-wise Z-Score Normalization:</strong> Scaling and standardizing variable trait occurrences across strains to ensure homoscedasticity and un-biased vector comparison.</div>
      </div>
      <div class="flex items-start gap-3">
        <span class="bg-emerald-100 text-emerald-800 font-bold px-2 py-0.5 rounded text-[10px]">05</span>
        <div><strong class="text-gray-900">Unsupervised Hierarchical Clustering:</strong> Calculating <em>Euclidean distances</em> and applying <em>Complete Linkage</em> algorithms to dynamically segregate architectural similarities.</div>
      </div>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-dna text-emerald-600"></i> Comparative Functional Landscapes (Heatmap Representation)
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    The central discovery engine executes bidirectional unsupervised hierarchical clustering, directly positioning your newly isolated wild candidates against a validated control matrix of prominent commercial strains and non-biostimulatory benchmark references.
  </p>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[750px] mx-auto my-8">
    <img src="{{ '/assets/img/microbial_genomics/project1_clustered_heatmap.png' | relative_url }}" alt="High-Resolution Clustered Genomic Heatmap" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 1.1: High-resolution dual-axis hierarchical clustering matrix demonstrating functional niche partitioning between wild isolates, commercial benchmarks, and negative controls.
    </div>
  </div>

  <div class="bg-emerald-50/40 border border-emerald-100 rounded-xl p-4 text-xs text-slate-700 leading-relaxed my-6">
    <h5 class="font-bold text-emerald-900 mb-1 flex items-center gap-1"><i class="fa-solid fa-circle-info"></i> Decoupling Functional Enrichment Zones</h5>
    <ul class="list-disc pl-5 space-y-1">
      <li><strong>Niche Adaptation Vectors:</strong> Evaluates highly enriched patterns in gene clusters steering root surface attachment, chemotaxis, and flagellar assembly across different host species.</li>
      <li><strong>Industrial Plant Stabilization Loci:</strong> Co-clustering behaviors pinpoint isolates that possess superior competitive fitness to securely survive and replicate within complex soil and tissue textures.</li>
    </ul>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-arrow-down-short-wide text-emerald-600"></i> Agrobiotech Predictive Indicators
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    By mapping statistical co-occurrence profiles, this pipeline serves as an advanced data-driven feature engineering and strain prioritization layer before launching long-term, high-cost greenhouse or field-scale trials.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4 my-6 text-xs text-gray-600 leading-relaxed">
    <div class="bg-slate-50 p-4 rounded-xl border">
      <strong>✔ Advanced Plant-Microbe Interaction Mapping:</strong> Bridges localized genomic structure with macro-level biological success, detecting critical genes tied to induced systemic resistance (ISR), mineral solubilization, and hormone modulation pathways.
    </div>
    <div class="bg-slate-50 p-4 rounded-xl border">
      <strong>✔ Smart In Silico Strain Prioritization:</strong> Eradicates reliance on random screening methods by numerically predicting which wild candidates display an optimal functional genome layout to equal or outperform market-leading biological inputs.
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-briefcase text-emerald-600"></i> Industrial Value & Translational Impact
  </h2>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-xs text-gray-600">
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-microscope text-emerald-600"></i> Next-Gen Bio-Input Pipelines
      </h4>
      Accelerates R&D turnaround times for sustainable agriculture industries by rapidly filtering thousands of candidate genomic reads into clear, functional clusters of high-performing PGPR strains.
    </div>
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-seedling text-emerald-600"></i> Precision Bio-Inoculant Design
      </h4>
      Provides a foundational analytical core to strategically engineer multi-strain microbial consortia designed to successfully settle inside challenging industrial crop lines and variable soil architectures.
    </div>
  </div>
</div>

<div class="my-8 pt-4 border-t border-gray-100 text-xs text-gray-400 font-mono">
  📁 Project References & Reproducibility Tracking:
  <ul class="list-disc pl-5 mt-2 space-y-1">
    <li>Developed as part of doctoral research in functional microbial genomics.</li>
    <li>Environment & Framework Core: Built on R Ecosystem (<code>tidyverse</code>, <code>pheatmap</code>, <code>readxl</code>).</li>
    <li>Source Code Repositories: <a class="text-indigo-600 hover:underline" href="https://github.com/davidvillafan96/genomic-feature-classification-pipeline/tree/main" target="_blank">Genomic Feature Classification Pipeline Codebase</a></li>
  </ul>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
