This repository contains the code used to process and analyse the data presented in the "Using rare genetic mutations to revisit structural brain asymmetry" paper.

Abstract
Asymmetry between the left and right brain is a key feature of brain organization. Hemispheric functional specialization underlies some of the most advanced human-defining cognitive operations, such as articulated language, perspective taking, or rapid detection of facial cues. Yet, genetic investigations into brain asymmetry have mostly relied on common variant studies, which typically exert small effects on brain phenotypes. Here, we leverage rare genomic deletions and duplications to study how genetic alterations reverberate in human brain and behavior. We quantitatively dissected the impact of eight high-effect-size copy number variations (CNVs) on brain asymmetry in a multi-site cohort of 552 CNV carriers and 290 non-carriers. Isolated multivariate brain asymmetry patterns spotlighted regions typically thought to subserve lateralized functions, including language, hearing, as well as visual, face and word recognition. Planum temporale asymmetry emerged as especially susceptible to deletions and duplications of specific gene sets. Targeted analysis of common variants through genome-wide association study (GWAS) consolidated partly diverging genetic influences on the right versus left planum temporale structure. In conclusion, our gene-brain-behavior mapping highlights the consequences of genetically controlled brain lateralization on human-defining cognitive traits.


![image](https://github.com/jakubkopal/CNV-asymmetry/assets/60342135/d8065c5c-f97a-4ea8-9b66-cf087091e794)
Figure 1

Resources and Scripts
CNV-specific asymmetry patterns are saved in Data/CNV_AP folder. Findings from the article are based on the analysis scripts in the Scripts folder.

Scripts/calculate_ip.m is an example of using Linear discriminant to isolate CNV-specific intermediate pehnotypes from raw anatomical data. Bagging and regularization is implemented to safeguard before overfitting.
Scripts/lowdim_projection.py is an analysis script to plot PCA and LDA two-dimensional projection of regional volumes.
Scripts/compare_cohen_ip.m plots and compares derived CNV-specific Cohen's d brain maps with LDA-derived intermediate phenotypes.
Scripts/analyze_ip.py is an analysis scripts to investigate CNV effects on large-scale networks with the use of LDA intermediate phenotypes.
Scripts/compare_simmilarities.py is an analysis script to compute the similarity between the phenome profiles, intermediate phenotypes, and volumetric Cohen's d brain maps.
