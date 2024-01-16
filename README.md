This repository contains the code used to process and analyse the data presented in the "Rare CNVs and phenome-wide profiling highlight brain-structural divergence and phenotypical convergencea" paper.

Abstract
Copy number variations (CNVs) are rare genomic deletions and duplications that can affect brain and behavior. Previous reports of CNV pleiotropy imply that they converge on shared mechanisms at some level of pathway cascades, from genes to large-scale neural circuits to the phenome. However, existing studies have primarily examined single CNV loci in small clinical cohorts. It remains unknown how distinct CNVs escalate vulnerability for the same developmental and psychiatric disorders. Here, we quantitatively dissect the associations between brain organization and behavioral differentiation across eight key CNVs. In 534 CNV carriers, we explored CNV-specific brain morphology patterns. CNVs were characteristic of disparate morphological changes involving multiple large-scale networks. We extensively annotated these CNV-associated patterns with ~1000 lifestyle indicators through the UK Biobank resource. The resulting phenotypic profiles largely overlap and have body-wide implications, including the cardiovascular, endocrine, skeletal, and nervous systems. Our population-level investigation established brain structural divergences and phenotypical convergences of CNVs, with direct relevance to major brain disorders.

Figure 1

Resources and Scripts
CNV-specific intermediate phenotypes are saved in Data/CNV_IP folder. LDA classification accuracies are saved in Data/CNV_IP folder. Phenotypic associations are saved in Data/PheWAS folder. Findings from the article are based on the analysis scripts in the Scripts folder.

Scripts/calculate_ip.m is an example of using Linear discriminant to isolate CNV-specific intermediate pehnotypes from raw anatomical data. Bagging and regularization is implemented to safeguard before overfitting.
Scripts/lowdim_projection.py is an analysis script to plot PCA and LDA two-dimensional projection of regional volumes.
Scripts/compare_cohen_ip.m plots and compares derived CNV-specific Cohen's d brain maps with LDA-derived intermediate phenotypes.
Scripts/analyze_ip.py is an analysis scripts to investigate CNV effects on large-scale networks with the use of LDA intermediate phenotypes.
Scripts/compare_simmilarities.py is an analysis script to compute the similarity between the phenome profiles, intermediate phenotypes, and volumetric Cohen's d brain maps.
