---
layout: page
title: "Project 2: Multivariate Genomic Fingerprinting & LDA-Driven PGPR Performance Evaluation"
description: "A Reproducible AgTech Framework Deploying Linear Discriminant Analysis (MASS) and PCA-Imputation to Profile Functional Strengths and Gaps in Novel Bioinoculant Isolates"
bg_color: "#022c22"
icon: "fa-solid fa-diagram-next"
importance: 2
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-emerald-950 to-teal-950 border-l-4 border-emerald-500 p-6 rounded-r-xl mb-8 shadow-sm">
    <h2 class="text-xl font-bold text-white mb-2 flex items-center gap-2">
      <i class="fa-solid fa-bullseye text-emerald-400"></i> Project Objective
    </h2>
    <p class="text-emerald-200/90 leading-relaxed text-sm">
      Moving from raw omics data to strategic R&D go/no-go product development. This advanced pipeline applies <strong>Linear Discriminant Analysis (LDA)</strong> over high-dimensional genomic feature matrices to quantify the functional strengths, weaknesses, and basal aptitudes of newly isolated bacterial strains against market-leading commercial reference strains, optimizing in silico screening before greenhouse validation.
    </p>
    <div class="mt-4 flex flex-wrap gap-2 text-[11px] font-mono text-emerald-300">
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Linear Discriminant Analysis (LDA)</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Missing Data Imputation (missMDA)</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Functional Biocontrol Profiling</span>
    </div>
  </div>

  <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center shadow-sm max-w-[350px] mx-auto mb-6">
    <span class="text-[10px] font-mono text-emerald-600 font-bold block mb-1">R&D STRATEGIC BIOMINING LAYER</span>
    <h4 class="font-bold text-slate-800 text-xs">PGPR Functional Evaluation Core</h4>
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-gears text-emerald-600"></i> Pipeline Architecture & Mathematical Workflow
  </h2>
  <p class="text-sm text-gray-600 mb-8 leading-relaxed">
    To mathematically map the specialized profile of a novel microbial isolate, the algorithmic framework standardizes quantitative gene frequencies into homogenous comparative distributions.
  </p>

  <div class="grid grid-cols-1 sm:grid-cols-4 gap-4 mb-8 text-center font-mono">
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xs font-bold text-emerald-700 uppercase tracking-wide">01. Annotation</div>
      <div class="text-[11px] text-gray-500 mt-2">Functional blocks mining via PLaBAse interaction databases.</div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xs font-bold text-emerald-700 uppercase tracking-wide">02. Engineering</div>
      <div class="text-[11px] text-gray-500 mt-2">Gene frequency calculation mapped per category.</div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xs font-bold text-emerald-700 uppercase tracking-wide">03. Imputation</div>
      <div class="text-[11px] text-gray-500 mt-2">PCA-based missing data handling using missMDA.</div>
    </div>
    <div class="bg-white border border-gray-100 p-4 rounded-xl shadow-sm">
      <div class="text-xs font-bold text-emerald-700 uppercase tracking-wide">04. Multivariate</div>
      <div class="text-[11px] text-gray-500 mt-2">Linear Discriminant Analysis (LDA) coordinate rendering.</div>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-chart-scatter text-emerald-600"></i> Functional Separation Space (LDA Projections)
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    By projecting 276 genomic categories across Linear Discriminants 1 and 2, the pipeline decodes the biological uniqueness of the target isolate (e.g., <em>Streptomyces sp. N2A</em>) compared to 20 reference elite AgTech strains.
  </p>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[700px] mx-auto my-8">
    <img src="{{ '/assets/img/microbial_genomics/project2_lda_functional_space.png' | relative_url }}" alt="Linear Discriminant Analysis (LDA) of Microbial Functional Fingerprints" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 2.1: Multi-class functional separation via Linear Discriminant Analysis (LDA). Confidence ellipses (68% CI) validate mathematical niche segregation across 276 loci.
    </div>
  </div>

  <div class="bg-slate-900 text-white rounded-2xl p-6 shadow-xl my-8 font-sans">
    <h3 class="text-lg font-bold text-emerald-400 mb-4 flex items-center gap-2 font-mono">
      <i class="fa-solid fa-magnifying-glass-chart"></i> Partitioning the Genomic Fingerprint Space
    </h3>
    
    <div class="space-y-6 text-sm">
      <div class="border-l-4 border-red-500 pl-4">
        <h4 class="font-bold text-red-400 font-mono flex items-center gap-1.5">
          <span class="w-2 h-2 rounded-full bg-red-500"></span> 1. Overrepresented Traits (Red Ellipse | Upper-Right Quadrant)
        </h4>
        <p class="text-slate-300 text-xs mt-1 leading-relaxed">
          Categories with <strong>Z &ge; 1</strong> that drive the specialized high-efficiency capabilities of the target candidate. Apex biomarker features include:
        </p>
        <ul class="list-disc pl-5 mt-2 text-xs text-slate-400 space-y-1">
          <li><strong>Hormonal Cross-Talk & ISR:</strong> Jasmonic and salicylic acid pathways optimizing Induced Systemic Resistance (ISR) and Systemic Acquired Resistance (SAR).</li>
          <li><strong>Phyto-Stimulatory Drivers:</strong> Advanced synthesis of IAA, gibberellins, 2,3-butanediol, biotin, niacin, folate, riboflavin, and lipoic acid.</li>
          <li><strong>Root Colonization Machinery:</strong> Enhanced surface adhesins, active biofilm synthesis components, and highly diverse Glycoside Hydrolases (GH).</li>
          <li><strong>Exclusion & Fitness Loci:</strong> High-affinity iron-capturing siderophores, oxidative stress peroxidases, and complex xenobiotic/pesticide biodegradation pathways.</li>
        </ul>
      </div>

      <div class="border-l-4 border-emerald-500 pl-4">
        <h4 class="font-bold text-emerald-400 font-mono flex items-center gap-1.5">
          <span class="w-2 h-2 rounded-full bg-emerald-500"></span> 2. Basal Housekeeping Programs (Green Ellipse | Central Core)
        </h4>
        <p class="text-slate-300 text-xs mt-1 leading-relaxed">
          Conserved core mechanisms (<strong>-1 < Z < 1</strong>) displaying neutral discriminatory power. These include baseline universal primary metabolic pathways and structural potassium (K) or phosphorus (P) solubilization cassettes shared across most competitive PGPR strains.
        </p>
      </div>

      <div class="border-l-4 border-blue-500 pl-4">
        <h4 class="font-bold text-blue-400 font-mono flex items-center gap-1.5">
          <span class="w-2 h-2 rounded-full bg-blue-500"></span> 3. Underrepresented/Suppressed Functional Gaps (Blue Ellipse | Left Margin)
        </h4>
        <p class="text-slate-300 text-xs mt-1 leading-relaxed">
          Genomic regions showing distinct evolutionary absence (<strong>Z &le; -1</strong>), pointing to ecological strategies typical of alternative microbial guilds:
        </p>
        <ul class="list-disc pl-5 mt-2 text-xs text-slate-400 space-y-1">
          <li><strong>Gram-Negative Standard Traits:</strong> Complete absence of flagellar motility cascades, hydrogen cyanide (HCN) synthesis, and AHL-based Quorum Sensing systems.</li>
          <li><strong>Symbiotic Cassettes:</strong> Atmospheric nitrogen fixation and root nodulation pathways are fully suppressed in these Actinomycetota frameworks.</li>
        </ul>
      </div>
    </div>
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-lightbulb text-emerald-600"></i> R&D Strategic Impact for Bioinoculant Engineering
  </h2>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-xs text-gray-600">
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-shield-halved text-emerald-600"></i> Target Consortia Design
      </h4>
      By mapping functional gaps (e.g., absence of nitrogen fixation), this pipeline allows engineers to logically assemble multi-strain microbial consortia where strains syntrophically complement each other's weaknesses.
    </div>
    <div class="p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <h4 class="font-bold text-gray-900 text-sm mb-2 flex items-center gap-1.5">
        <i class="fa-solid fa-chart-line text-emerald-600"></i> Commercial Benchmarking
      </h4>
      Replaces classical blind phenotypic screening with high-dimensional data, mathematically validating whether a novel isolate possesses the specialized genomic architecture required to equal or outperform market benchmarks.
    </div>
  </div>
</div>

<div class="my-8 pt-4 border-t border-gray-100 text-xs text-gray-400 font-mono">
  📁 Project References & Reproducibility Tracking:
  <ul class="list-disc pl-5 mt-2 space-y-1">
    <li>Developed as part of doctoral research in comparative functional plant-microbe interactions.</li>
    <li>Environment & Architecture: Built on R Framework (<code>MASS</code>, <code>missMDA</code>, <code>ggplot2</code>, <code>dplyr</code>).</li>
    <li>Source Code Repositories: <a class="text-emerald-600 hover:underline" href="https://github.com/davidvillafan96/pgpr-strain-evaluation-pipeline" target="_blank">PGPR Strain Evaluation Pipeline Codebase</a></li>
  </ul>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
