---
layout: page
title: Bioinformatics
permalink: /bioinformatics/
---

<div class="mt-4 mb-5 font-jojy text-center" style="width: 100%;">
  <h1 class="fw-bold" style="font-size: 2.8rem; letter-spacing: -1.5px; color: #000000 !important; margin-bottom: 5px; text-align: center !important;">
    Bioinformatics
  </h1>
</div>

<div class="mb-5 font-jojy" style="color: #000000 !important; max-width: 750px; margin-left: auto; margin-right: auto; text-align: center !important;">
  <h2 class="fw-bold" style="font-size: 1.5rem; letter-spacing: -0.5px; margin-bottom: 15px; color: #000000 !important;">What I Do</h2>
  <p style="font-size: 1.05rem; line-height: 1.6; color: #333333 !important; font-weight: 400;">
    I build scalable, production-grade bioinformatics pipelines that process raw sequencing reads into structured, actionable profiles. My architecture paradigms strictly enforce FAIR data principles, leveraging containerization to unlock 100% computational reproducibility across high-performance environments—<strong>structuring and auditing multi-omics features before they ever hit a Machine Learning model</strong>.
  </p>
</div>

<div class="jojy-dropdown-container mb-5 font-jojy">

  <details class="jojy-dropdown" open>
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">🧬</span> Human Genomics: WGS & WES Variant Mapping
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        End-to-end alignment and variant discovery pipelines for Human Whole Genome (WGS) and Whole Exome Sequencing (WES) data, adhering strictly to GATK Best Practices for germline and somatic analysis.
      </p>
      <ul>
        <li><strong>Quality & Preprocessing:</strong> Trimming and adapter removal (fastp), high-throughput alignment (BWA-MEM / BOWTIE2) against GRCh38, and duplicate marking via Picard Tools.</li>
        <li><strong>Variant Calling & Refinement:</strong> SNVs and Indels identification using GATK HaplotypeCaller, Mutect2 (somatic), and DeepVariant. Quality filtering applied through Variant Quality Score Recalibration (VQSR).</li>
        <li><strong>Clinical Annotation & Prioritization:</strong> Functional impact sorting using Ensembl VEP, SnpEff, and Annovar, integrating clinical datasets (ClinVar, gnomAD, OMIM, COSMIC) to filter variants based on ACMG/AMP guidelines.</li>
      </ul>
    </div>
  </details>

  <details class="jojy-dropdown">
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">🦠</span> Shotgun Metagenomics & Microbial Gut Profiling
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Advanced computational characterization of complex microbial ecosystems, heavily optimized for human gut microbiome dynamics and therapeutic biomarker discovery.
      </p>
      <ul>
        <li><strong>Upstream Quality Gates:</strong> Automated quality filtering using fastp, Trimmomatic, and cross-run aggregation via MultiQC.</li>
        <li><strong>Host DNA Decontamination:</strong> Strict elimination of human host contamination reads by mapping raw data against the hg38 genome using Bowtie2 or KneadData prior to downstream profiling.</li>
        <li><strong>Taxonomic Profiling:</strong> Deep read-level profiling via k-mer mapping (Kraken2 + Bracken) and unique clade-specific marker gene tracking (MetaPhlAn).</li>
        <li><strong>Functional Profiling:</strong> Reconstruction of absolute and relative abundances of metabolic and functional pathways against UniRef models using HUMAnN3 (mapping directly to KEGG and MetaCyc global pathways).</li>
      </ul>
    </div>
  </details>

  <details class="jojy-dropdown">
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">🧫</span> De Novo Assembly & MAGs Recovery
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Reconstruction of novel uncultivated genomes from deep metagenomic sequencing data to expand reference catalogs.
      </p>
      <ul>
        <li><strong>Assembly Engines:</strong> Sequence reconstruction using graph-optimized de Bruijn compilers (MEGAHIT and metaSPAdes).</li>
        <li><strong>Advanced Binning & QC:</strong> Co-assembly and single-sample binning strategies utilizing MetaWRAP, MetaBAT2, and MaxBin2.</li>
        <li><strong>ML-Driven Auditing:</strong> Quality assurance audited via machine learning scoring models in CheckM2, targeting high-quality draft status (Completeness >90%, Contamination <5%).</li>
      </ul>
    </div>
  </details>

  <details class="jojy-dropdown">
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">⚙️</span> Pipeline Automation & DevOps Ecosystem
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Engineering reproducible, crash-resilient multi-step infrastructures capable of scaling across cloud architectures and local supercomputers.
      </p>
      <ul>
        <li><strong>Orchestration:</strong> Production-ready workflows developed using Nextflow (including nf-core architectural compliance) and Snakemake.</li>
        <li><strong>Container Isolation & HPC:</strong> Building immutable dockerfiles and compiling them into Singularity (Apptainer) images for secure execution on distributed High-Performance Computing cluster environments (SLURM workloads).</li>
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
    border-color: #0a9396 !important; /* Color de acento de Bioinformatics */
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
