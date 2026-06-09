---
layout: page
title: Clinical & Cancer Genomics
permalink: /clinical-genomics/
---

<div class="mt-4 mb-5 font-jojy text-center" style="width: 100%;">
  <h1 class="fw-bold" style="font-size: 2.8rem; letter-spacing: -1.5px; color: #000000 !important; margin-bottom: 5px; text-align: center !important;">
    Clinical & Cancer Genomics
  </h1>
</div>

<div class="mb-5 font-jojy" style="color: #000000 !important; max-width: 750px; margin-left: auto; margin-right: auto; text-align: center !important;">
  <h2 class="fw-bold" style="font-size: 1.5rem; letter-spacing: -0.5px; margin-bottom: 15px; color: #000000 !important;">What I Do</h2>
  <p style="font-size: 1.05rem; line-height: 1.6; color: #333333 !important; font-weight: 400;">
    I bridge the gap between high-throughput raw sequencing datasets and clinical interpretation. I apply standardized regulatory frameworks to look for pathological variations, sort driver alterations from passenger mutations, and discover transcriptomic signatures related to metastasis and cancer progression.
  </p>
</div>

<div class="jojy-dropdown-container font-jojy mb-5">

  <details class="jojy-dropdown" open>
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">🏥</span> Variant Interpretation & Tiering Frameworks
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Rigorous evaluation of somatic and germline clinical variants using international criteria to distinguish pathological mutations from genomic background noise.
      </p>
      <ul>
        <li><strong>Standardized Guidelines:</strong> Deep exposure to variant prioritization applying <code>ACMG/AMP</code> protocols for precise reporting and clinical classification tiers.</li>
        <li><strong>Database Mining:</strong> Querying comprehensive reference frameworks including <code>ClinVar</code>, <code>gnomAD</code>, <code>OMIM</code>, and <code>COSMIC</code> to build data-backed molecular diagnostic criteria.</li>
        <li><strong>Somatic Calling Pipelines:</strong> Processing raw reads using benchmark callers (<code>GATK Mutect2</code>, <code>Strelka2</code>, <code>VarScan</code>) followed by functional prediction tiering and consequence filtering via <code>SnpEff/SnpSift</code>, <code>Ensembl VEP</code>, and <code>Annovar</code>.</li>
      </ul>
    </div>
  </details>

  <details class="jojy-dropdown">
    <summary class="jojy-dropdown-title">
      <span class="jojy-dropdown-emoji">🎗️</span> Transcriptomic Biomarker Discovery (RNA-seq)
    </summary>
    <div class="jojy-dropdown-content">
      <p>
        Mapping raw transcription arrays to decode molecular patterns behind complex tumor microenvironments and tumor evolutionary trajectories.
      </p>
      <ul>
        <li><strong>Expression Profiling:</strong> Building end-to-end alignment-free RNA-seq pipelines mapping transcription patterns using fast, ultra-efficient quantifiers (<code>Salmon</code> / <code>Kallisto</code>).</li>
        <li><strong>Cancer Transitions:</strong> Investigating differential gene expression models via <code>DESeq2</code> and <code>edgeR</code> to build multi-gene expression signatures that distinguish Normal Tissue, Primary Tumor, and Metastatic stages in Colorectal Cancer landscapes.</li>
        <li><strong>Functional Enrichment:</strong> Downstream pathway execution using Gene Set Enrichment Analysis (<code>GSEA</code>), <code>GO/KEGG</code> functional curation, and structural visualization matrices in R.</li>
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
    border-color: #2ec4b6 !important; /* Color de acento de Clinical */
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
