---
layout: page
title: "Project 3: Machine Learning for Drug Response Prediction"
description: "From Statistical Foundations to Multi-Algorithmic Predictive Systems in Tabular Oncology"
bg_color: "#1e1b4b"
icon: "fa-solid fa-brain"
importance: 3
---

<div class="mb-12 border-b border-gray-100 pb-8">
  <div class="bg-gradient-to-r from-indigo-950 to-slate-900 border-l-4 border-violet-500 p-6 rounded-r-xl mb-8 shadow-sm">
    <h2 class="text-xl font-bold text-white mb-2 flex items-center gap-2">
      <i class="fa-solid fa-bullseye text-violet-400"></i> Project Objective
    </h2>
    <p class="text-indigo-200/90 leading-relaxed text-sm">
      Transitioning from exploratory analytics into <strong>predictive modeling</strong>. This phase implements robust machine learning pipelines to map complex multi-lineage molecular patterns into continuous pharmacological response metrics ($LN(IC_{50})$) and stratified clinical classification spaces.
    </p>
    <div class="mt-4 flex flex-wrap gap-2 text-[11px] font-mono text-violet-300">
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Dual-Core Architecture (Reg/Clf)</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Dimensionality Compression (PCA)</span>
      <span class="bg-white/10 px-2.5 py-1 rounded-full border border-white/10">Cross-Validation Tuning</span>
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-4 my-6">
    <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center opacity-60">
      <span class="text-[10px] font-mono text-gray-400 block mb-1">PHASE 1</span>
      <h4 class="font-bold text-gray-700 text-xs">Data Engineering & Integration</h4>
    </div>
    <div class="bg-gray-50 border border-gray-100 p-4 rounded-xl text-center opacity-60">
      <span class="text-[10px] font-mono text-gray-400 block mb-1">PHASE 2</span>
      <h4 class="font-bold text-gray-700 text-xs">Statistical Inference & EDA</h4>
    </div>
    <div class="bg-indigo-950 text-white p-4 rounded-xl text-center shadow-md ring-1 ring-violet-500/30">
      <span class="text-[10px] font-mono text-violet-400 font-bold block mb-1">CURRENT MILESTONE</span>
      <h4 class="font-bold text-indigo-100 text-xs">Project 3: Predictive Modeling</h4>
    </div>
  </div>
</div>

<div class="my-12">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-network-wired text-indigo-600"></i> End-to-End Machine Learning Workflow
  </h2>
  <p class="text-sm text-gray-600 mb-8 leading-relaxed">
    The following methodological blueprint outlines the transformation of the raw master matrix <code class="bg-gray-100 px-1 py-0.5 rounded text-xs font-mono">GDSC_ML_Ready.csv</code>. It showcases variance filtering, orthogonal matrix projection, downsampling, and parallel predictive execution.
  </p>

  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 mb-10">
    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm hover:border-indigo-200 transition-colors">
      <div class="w-8 h-8 rounded-lg bg-indigo-50 flex items-center justify-center text-indigo-600 mb-3 font-mono font-bold text-xs">01</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Feature Cleansing</h4>
      <p class="text-[11px] text-gray-500 leading-normal">Exclusion of non-informative metadata and clinical identifiers. Character variables are programmatically encoded into factors.</p>
    </div>

    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm hover:border-indigo-200 transition-colors">
      <div class="w-8 h-8 rounded-lg bg-indigo-50 flex items-center justify-center text-indigo-600 mb-3 font-mono font-bold text-xs">02</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Dummy Encoding & NZV</h4>
      <p class="text-[11px] text-gray-500 leading-normal">Matrix expansion via <code>model.matrix</code>. Strict variance filtering eliminates near-zero variance features followed by unit scaling.</p>
    </div>

    <div class="bg-white border border-gray-100 p-5 rounded-xl shadow-sm hover:border-indigo-200 transition-colors">
      <div class="w-8 h-8 rounded-lg bg-indigo-50 flex items-center justify-center text-indigo-600 mb-3 font-mono font-bold text-xs">03</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">Dual-Core Partition</h4>
      <p class="text-[11px] text-gray-500 leading-normal">Bifurcated modeling paths: Continuous regression ($LN(IC_{50})$) and binary classification thresholded at the lower quartile (Q25).</p>
    </div>

    <div class="bg-white border border-violet-100 bg-violet-50/10 p-5 rounded-xl shadow-sm">
      <div class="w-8 h-8 rounded-lg bg-violet-100 flex items-center justify-center text-violet-600 mb-3 font-mono font-bold text-xs">04</div>
      <h4 class="font-bold text-gray-900 text-sm mb-1">PCA & Class Balance</h4>
      <p class="text-[11px] text-gray-600 leading-normal">Dimensional reduction through PCA capturing 95% variance. Symmetric downsampling balances the clinical distribution.</p>
    </div>
  </div>

  <div class="border border-gray-100 p-3 rounded-2xl bg-white shadow-md max-w-[850px] mx-auto mb-10">
    <img src="{{ '/assets/img/gdsc2_ml/project3_workflow.png' | relative_url }}" alt="GDSC2 ML Pipeline Execution Diagram" class="w-full h-auto rounded-xl">
    <div class="text-center text-[11px] text-gray-400 mt-2 font-mono">
      Figure 3.0: High-throughput data preprocessing and modeling execution matrix.
    </div>
  </div>

  <div class="border border-gray-200 rounded-xl overflow-hidden bg-[#1e1e1e] shadow-lg font-mono text-xs my-8">
    <div class="bg-[#2d2d2d] px-4 py-2 text-gray-400 flex items-center justify-between border-b border-zinc-800">
      <span class="flex items-center gap-2 text-[11px]"><i class="fa-solid fa-code text-indigo-400"></i> pipeline_preprocessing.R</span>
      <span class="text-[10px] bg-zinc-800 px-2 py-0.5 rounded text-zinc-500">Data Prep Block</span>
    </div>
{% highlight r %}
# Feature Cleansing, One-Hot Encoding, and Near-Zero Variance Filtering
cols_to_discard <- c("DATASET", "NLME_RESULT_ID", "NLME_CURVE_ID", "COSMIC_ID",
                     "CELL_LINE_NAME", "SANGER_MODEL_ID", "DRUG_ID", "DRUG_NAME",
                     "SYNONYMS", "WEBRELEASE", "COMPANY_ID", "PUTATIVE_TARGET", "PATHWAY_NAME")

df_clean <- df_ml %>%
  select(-any_of(cols_to_discard)) %>%
  mutate(across(where(is.character), as.factor)) %>%
  drop_na() %>%
  select(where(~ n_distinct(.) > 1))

# Convert to Dummy Variables & Standardize Matrix Space
df_dummy <- model.matrix(~ . - 1, data = df_clean) %>% as.data.frame()
preproc  <- preProcess(df_dummy, method = c("nzv", "center", "scale"))
df_proc  <- predict(preproc, df_dummy)
{% endhighlight %}
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <div class="flex flex-col md:flex-row md:items-center justify-between mb-6">
    <div>
      <h2 class="text-2xl font-bold text-gray-900 tracking-tight flex items-center gap-2">
        <i class="fa-solid fa-chart-line text-blue-500"></i> Regression Suite: Continuous Efficacy Modeling
      </h2>
      <p class="text-xs text-gray-500 mt-1">Benchmarking state-of-the-art ensemble architectures over continuous IC50 landscapes.</p>
    </div>
    <div class="mt-4 md:mt-0 bg-slate-100 border text-slate-700 font-mono text-[11px] px-3 py-1.5 rounded-lg flex items-center gap-2 self-start md:self-auto">
      <i class="fa-solid fa-database text-slate-400"></i> <strong>Execution Subsample:</strong> 30,000 observations / 56 clean features
    </div>
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6 my-6">
    <div class="bg-gradient-to-br from-white to-slate-50/50 border border-gray-100 p-6 rounded-2xl shadow-sm relative overflow-hidden">
      <div class="absolute top-0 right-0 w-24 h-24 bg-blue-500/5 rounded-full blur-xl"></div>
      <div class="flex items-center justify-between mb-4">
        <span class="text-xs font-mono font-bold text-blue-600 bg-blue-50 px-2.5 py-0.5 rounded-full">Primary Framework</span>
        <h3 class="font-bold text-gray-900 text-sm">XGBoost Regressor</h3>
      </div>
      <div class="flex items-baseline gap-2 mb-2">
        <span class="text-3xl font-extrabold text-slate-900 font-mono">0.881</span>
        <span class="text-xs text-gray-400 font-mono font-semibold">Test RMSE</span>
      </div>
      <p class="text-xs text-gray-600 leading-relaxed">
        Superior predictive power in tabular configurations. It maps subtle variations in pathway activation boundaries into fine-grained response distributions without succumbing to screening technical artifacts.
      </p>
    </div>

    <div class="bg-gradient-to-br from-white to-slate-50/50 border border-gray-100 p-6 rounded-2xl shadow-sm relative overflow-hidden">
      <div class="absolute top-0 right-0 w-24 h-24 bg-emerald-500/5 rounded-full blur-xl"></div>
      <div class="flex items-center justify-between mb-4">
        <span class="text-xs font-mono font-bold text-emerald-600 bg-emerald-50 px-2.5 py-0.5 rounded-full">Baseline Comparison</span>
        <h3 class="font-bold text-gray-900 text-sm">Random Forest</h3>
      </div>
      <div class="flex items-baseline gap-2 mb-2">
        <span class="text-3xl font-extrabold text-slate-900 font-mono">0.882</span>
        <span class="text-xs text-gray-400 font-mono font-semibold">Test RMSE</span>
      </div>
      <p class="text-xs text-gray-600 leading-relaxed">
        Excellent structural stability. The tight alignment between the Random Forest baseline and XGBoost indicates that our pipeline's signal is structurally anchored rather than dependent on stochastic tuning optimizations.
      </p>
    </div>
  </div>

  <div class="bg-blue-50/40 border border-blue-100 rounded-xl p-4 text-xs text-slate-700 leading-relaxed my-6">
    <h5 class="font-bold text-blue-900 mb-1 flex items-center gap-1"><i class="fa-solid fa-circle-info"></i> Bioinformatics Interpretation of RMSE</h5>
    Since the pharmacological target vectors were Z-score standardized ($\sigma = 1$), an <strong>RMSE < 1 (~0.88)</strong> proves that our algorithms capture true biological mechanisms rather than overfitting random technical noise within high-throughput screenings.
  </div>

  <div class="border border-gray-200 rounded-xl overflow-hidden bg-[#1e1e1e] shadow-lg font-mono text-xs my-6">
    <div class="bg-[#2d2d2d] px-4 py-2 text-gray-400 flex items-center justify-between border-b border-zinc-800">
      <span class="flex items-center gap-2 text-[11px]"><i class="fa-solid fa-code text-blue-400"></i> ensemble_regression.R</span>
      <span class="text-[10px] bg-zinc-800 px-2 py-0.5 rounded text-zinc-500">Regression Block</span>
    </div>
{% highlight r %}
# Partition Training and Testing Spaces for Continuous Targets
y_reg <- df_proc$LN_IC50_scaled
idx_reg <- createDataPartition(y_reg, p = 0.8, list = FALSE)
X_train_reg <- X_data[idx_reg, ]; X_test_reg <- X_data[-idx_reg, ]
y_train_reg <- y_reg[idx_reg];     y_test_reg <- y_reg[-idx_reg]

# Model 1: Random Forest
rf_reg  <- randomForest(x = X_train_reg, y = y_train_reg, ntree = 100)
pred_rf <- predict(rf_reg, X_test_reg)

# Model 2: eXtreme Gradient Boosting (XGBoost)
dtrain <- xgb.DMatrix(data = as.matrix(X_train_reg), label = y_train_reg)
dtest  <- xgb.DMatrix(data = as.matrix(X_test_reg), label = y_test_reg)
params <- list(objective = "reg:squarederror", eta = 0.1, max_depth = 6, subsample = 0.8)
xgb_reg  <- xgb.train(params = params, data = dtrain, nrounds = 150)
pred_xgb <- predict(xgb_reg, dtest)
{% endhighlight %}
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-2 flex items-center gap-2">
    <i class="fa-solid fa-vial-circle-check text-purple-600"></i> Classification Benchmarking & Clinical Framing
  </h2>
  <p class="text-sm text-gray-600 mb-6 leading-relaxed">
    Moving from continuous scales to actionable clinical choices. By isolating hyper-sensitive cell responses (lower 25th percentile of $LN(IC_{50})$), we tested distinct model topologies across an orthogonal feature space.
  </p>

  <div class="grid grid-cols-1 md:grid-cols-3 gap-6 items-start my-6">
    <div class="md:col-span-1 space-y-4">
      <div class="bg-purple-950 text-white p-5 rounded-2xl shadow-sm border border-purple-900">
        <span class="text-[10px] uppercase tracking-widest text-purple-300 font-mono block">PCA Latent Space</span>
        <div class="text-xl font-bold font-mono mt-1">95% Variance</div>
        <p class="text-[11px] text-purple-200/80 mt-2 leading-relaxed">Optimal principal components are dynamically selected using spectral variance summation criteria to project condensed molecular spaces.</p>
      </div>

      <div class="bg-slate-900 text-white p-5 rounded-2xl shadow-sm border border-slate-800">
        <span class="text-[10px] uppercase tracking-widest text-slate-400 font-mono block">Subsampling Balance</span>
        <div class="text-xl font-bold font-mono mt-1">1:1 Balanced Space</div>
        <div class="mt-2 text-[11px] font-mono text-slate-300 space-y-0.5">
          <div>• Resistant Baseline: 7,500 cells</div>
          <div>• Sensitive Core: 7,500 cells</div>
        </div>
      </div>
    </div>

    <div class="md:col-span-2 border border-gray-100 rounded-2xl bg-white shadow-sm overflow-hidden">
      <table class="w-full text-left border-collapse">
        <thead>
          <tr class="bg-gray-50 border-b border-gray-100 text-[11px] font-mono font-bold text-gray-500 uppercase tracking-wider">
            <th class="p-4">Algorithm Tested</th>
            <th class="p-4">Dimensional Space</th>
            <th class="p-4">Optimization Strategy</th>
          </tr>
        </thead>
        <tbody class="divide-y divide-gray-50 text-xs">
          <tr>
            <td class="p-4 font-semibold text-gray-900">Logistic Regression (GLM)</td>
            <td class="p-4 font-mono text-gray-600">PCA Coordinates</td>
            <td class="p-4 text-gray-500">Asymptotic Binomial Logit Modeling</td>
          </tr>
          <tr>
            <td class="p-4 font-semibold text-gray-900">Support Vector Machines (SVM)</td>
            <td class="p-4 font-mono text-gray-600">PCA Coordinates</td>
            <td class="p-4 text-gray-500">Linear Hyperplane Separation ($C = 1$)</td>
          </tr>
          <tr>
            <td class="p-4 font-semibold text-gray-900">k-Nearest Neighbors (k-NN)</td>
            <td class="p-4 font-mono text-gray-600">PCA Coordinates</td>
            <td class="p-4 text-gray-500">Local Instance Neighborhood Vote ($k = 7$)</td>
          </tr>
          <tr class="bg-violet-50/20">
            <td class="p-4 font-semibold text-indigo-950 flex items-center gap-1.5">
              Random Forest Classifier <i class="fa-solid fa-circle-check text-indigo-600 text-[10px]"></i>
            </td>
            <td class="p-4 font-mono text-indigo-900">PCA Coordinates</td>
            <td class="p-4 text-indigo-700 font-medium">Grid & Random Resampling Hyperparameter Grid Search</td>
          </tr>
        </tbody>
      </table>
      <div class="p-3 bg-gray-50 text-[10px] font-mono text-gray-400 border-t border-gray-100">
        * Every multi-class pipeline architecture underwent rigorous confusion matrix evaluation via stratified test folds.
      </div>
    </div>
  </div>

  <div class="border border-gray-200 rounded-xl overflow-hidden bg-[#1e1e1e] shadow-lg font-mono text-xs my-6">
    <div class="bg-[#2d2d2d] px-4 py-2 text-gray-400 flex items-center justify-between border-b border-zinc-800">
      <span class="flex items-center gap-2 text-[11px]"><i class="fa-solid fa-code text-purple-400"></i> classification_tuning.R</span>
      <span class="text-[10px] bg-zinc-800 px-2 py-0.5 rounded text-zinc-500">Classification & Hyperparameter Tuning</span>
    </div>
{% highlight r %}
# Define Categorical Target (Q25 Thresholding) and Orthogonal PCA Transformation
q25_threshold <- quantile(df_proc$LN_IC50_scaled, 0.25, na.rm = TRUE)
y_clf         <- as.factor(ifelse(df_proc$LN_IC50_scaled <= q25_threshold, 1, 0))

pca_res       <- prcomp(X_train_clf, center = TRUE, scale. = TRUE)
var_explained <- cumsum(pca_res$sdev^2) / sum(pca_res$sdev^2)
n_comp        <- which(var_explained >= 0.95)[1]

X_train_pca   <- predict(pca_res, X_train_clf)[, 1:n_comp]
X_test_pca    <- predict(pca_res, X_test_clf)[, 1:n_comp]

# Stratified Cross-Validation & Grid Optimization for Random Forest
control  <- trainControl(method = "cv", number = 5)
tunegrid <- expand.grid(.mtry = c(3, 5, 10))
tuned_rf <- train(x = X_train_bal, y = y_train_bal, method = "rf", 
                  trControl = control, tuneGrid = tunegrid, ntree = 100)
{% endhighlight %}
  </div>
</div>

<div class="my-12 pt-8 border-t border-gray-100">
  <h2 class="text-2xl font-bold text-gray-900 tracking-tight mb-6 flex items-center gap-2">
    <i class="fa-solid fa-hospital-user text-teal-600"></i> Translational Impact & Business Case
  </h2>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
    <div class="flex gap-4 p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-teal-50 flex items-center justify-center text-teal-600 shrink-0">
        <i class="fa-solid fa-sliders"></i>
      </div>
      <div>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Clinical Decision Support Systems (CDSS)</h4>
        <p class="text-xs text-gray-600 leading-relaxed">
          The pipeline serves as an advanced computational gatekeeper. It evaluates complex genomic patient profiles to filter hundreds of anti-cancer compounds down to high-probability matches for targeted oncology.
        </p>
      </div>
    </div>

    <div class="flex gap-4 p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-purple-50 flex items-center justify-center text-purple-600 shrink-0">
        <i class="fa-solid fa-dna"></i>
      </div>
      <div>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Precision Medicine Stratification</h4>
        <p class="text-xs text-gray-600 leading-relaxed">
          Replaces generic empirical prescriptions with data-driven therapeutic protocols. The algorithm uncovers structural molecular resistance profiles before patient treatment cycles ever initiate.
        </p>
      </div>
    </div>

    <div class="flex gap-4 p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-blue-50 flex items-center justify-center text-blue-600 shrink-0">
        <i class="fa-solid fa-flask"></i>
      </div>
      <div>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Accelerated R&D via In Silico Screening</h4>
        <p class="text-xs text-gray-600 leading-relaxed">
          Enables rapid parallel screening of thousands of drug-cell matches in silico. This substantially lowers physical lab operational overhead and shortens the discovery cycles of active compounds.
        </p>
      </div>
    </div>

    <div class="flex gap-4 p-5 rounded-xl border border-gray-100 bg-white shadow-sm">
      <div class="w-10 h-10 rounded-xl bg-violet-50 flex items-center justify-center text-violet-600 shrink-0">
        <i class="fa-solid fa-magnifying-glass-chart"></i>
      </div>
      <div>
        <h4 class="font-bold text-gray-900 text-sm mb-1">Mechanistic Biomarker Extraction</h4>
        <p class="text-xs text-gray-600 leading-relaxed">
          By utilizing feature importance scores, the system moves past opaque black-box predictions. It illuminates specific pathways and biological networks driving localized drug efficacy.
        </p>
      </div>
    </div>
  </div>
</div>

<div class="my-12 pt-6 border-t border-gray-100">
  <h3 class="font-bold text-gray-900 text-xs mb-4 uppercase tracking-wider font-mono text-gray-400">Core Pipeline Technology Stack</h3>
  <div class="flex flex-wrap gap-2 text-[10px] font-mono text-gray-600">
    <span class="bg-gray-100 px-2.5 py-1 rounded border">R Core Engine</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">caret (Resampling Suite)</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">xgboost</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">randomForest</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">e1071 (SVM Kernels)</span>
    <span class="bg-gray-100 px-2.5 py-1 rounded border">Metrics (RMSE Optimization)</span>
  </div>
</div>

<div class="my-12 bg-gradient-to-r from-slate-900 to-indigo-950 text-white rounded-2xl p-8 relative overflow-hidden shadow-xl border border-white/5">
  <div class="relative z-10 max-w-2xl">
    <span class="text-[10px] font-bold uppercase tracking-widest text-indigo-300 bg-indigo-900/60 px-2.5 py-1 rounded-full border border-indigo-800">Next Horizon</span>
    <h3 class="text-2xl font-bold text-white mt-4 mb-2">Integrating Genomic Variation & Mutation Signatures</h3>
    <p class="text-indigo-200/80 text-xs leading-relaxed mb-6">
      While functional pathway ontologies deliver robust predictive capabilities, capturing the remaining variance demands the inclusion of structural variations. <strong>Project 4</strong> expands this pipeline by integrating targeted mutational variant panels and large-scale mutational signatures.
    </p>
    <div class="text-xs font-semibold text-violet-400 flex items-center gap-1">
      Evolution: Statistical Associations <i class="fa-solid fa-arrow-right text-[10px]"></i> Machine Learning <i class="fa-solid fa-arrow-right text-[10px]"></i> Integrated Multi-Omic Discovery
    </div>
  </div>
  <div class="absolute right-4 bottom-4 opacity-5 text-9xl pointer-events-none hidden md:block">
    <i class="fa-solid fa-dna"></i>
  </div>
</div>

---

### 👤 Author

**David Villafañe, PhD** *Biological Sciences · Genomics · Computational Biology* [<i class="fa-brands fa-linkedin"></i> LinkedIn](https://www.linkedin.com/in/davidvillafanie/) · [<i class="fa-brands fa-github"></i> GitHub](https://github.com/davidvillafan96)
