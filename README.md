# Code supplement to the CNV asymmetry study
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)
[![DOI](https://img.shields.io/badge/DOI-10.1101%2F862615-informational
)]([https://doi.org/10.1101/2023.04.17.537199](https://doi.org/10.1101/2023.04.17.537199))

This repository contains the code used to process and analyse the data presented in the "Using rare genetic mutations to revisit structural brain asymmetry" paper. In addition, it also contains isolated asymmetry patterns and associated figures.

## Abstract
<div style="margin-left: 40px;" align="justify">
Asymmetry between the left and right brain is a key feature of brain organization. Hemispheric functional specialization underlies some of the most advanced human-defining cognitive operations, such as articulated language, perspective taking, or rapid detection of facial cues. Yet, genetic investigations into brain asymmetry have mostly relied on common variant studies, which typically exert small effects on brain phenotypes. Here, we leverage rare genomic deletions and duplications to study how genetic alterations reverberate in human brain and behavior. We quantitatively dissected the impact of eight high-effect-size copy number variations (CNVs) on brain asymmetry in a multi-site cohort of 552 CNV carriers and 290 non-carriers. Isolated multivariate brain asymmetry patterns spotlighted regions typically thought to subserve lateralized functions, including language, hearing, as well as visual, face and word recognition. Planum temporale asymmetry emerged as especially susceptible to deletions and duplications of specific gene sets. Targeted analysis of common variants through genome-wide association study (GWAS) consolidated partly diverging genetic influences on the right versus left planum temporale structure. In conclusion, our gene-brain-behavior mapping highlights the consequences of genetically controlled brain lateralization on human-defining cognitive traits.
</div>


<c>![Figure 1](https://github.com/jakubkopal/CNV-asymmetry/blob/main/figures/Fig1.png)</c>


Figure 1

**Eight key CNVs lead to unique effects on brain asymmetry that spotlight the planum temporale**

<div align="justify">
In addition to the deletions at 16p11.2 and 22q11.2 loci, we probed the effects of six additional CNVs on brain asymmetry (duplications at 1q21.1 distal, 15q11.2 BP1-BP2, 16p11.2 proximal, 22q11.2 proximal loci and deletions at 1q21.1 distal, 15q11.2 BP1-BP2 loci). For that purpose, we estimated six additional LDA models encompassing multivariate prediction rules separating respective CNV carriers and healthy controls. a) Significant LDA coefficients across eight key CNVs. The sankey plot depicts all LDA coefficients surpassing the bootstrap significance test. The width of the ribbon corresponds to the coefficient magnitude. Planum temporale and fusiform cortex asymmetries are both significantly associated with three CNVs. b) Overall strongest coefficients across eight LDA models. The boxplots depict LDA coefficients across the 8 CNVs. Planum temporale shows the strongest mean magnitude, followed by lobule VIIIb of the cerebellum and putamen. Lighter symbols represent deletions, while darker symbols represent duplications. Star denotes a significant coefficient based on the bootstrap significance test. c) Detailing the effects on planum temporale. Rain cloud plots summarize the effects of each CNV on the asymmetry of planum temporale. The Y-axis shows raw asymmetry indices (no LDA model), z-scored using control participants. While the 15q11.2 duplication, 16p11.2 deletion, and 22q11.2 deletion increase the asymmetry, 1q21.1 deletion decreases the asymmetry. The color (blue – decrease, red – increase) depicts a significant change in mean asymmetry based on a two-sided t-test with FDR-corrected P < 0.05. d) Comparison of brain-wide asymmetry patterns. We calculated Pearson's correlation to quantify the similarity between every pair of LDA coefficient sets from the eight models. Asterisk denotes FDR-corrected P-values obtained from spin permutation. Hierarchical clustering of model-specific coefficients obtained per CNV display distances (similarities) among studied asymmetry patterns based on Ward’s method. Distinct clusters separating deletions and duplications provide further evidence of their opposing effects. e) Regions separating different CNVs. Region-wise coefficients are plotted along the two leading components of the multiclass LDA model designed to separate between the eight CNVs. CNVs lead to distinct brain asymmetry patterns in which the planum temporale plays a prominent role.
  </div>



## Resources and Scripts
All figures used in the articles are in the `figures` folder. Findings from the article are based on the analysis scripts in the `scripts` folder.

1.   `scripts/extract_asymmetry_pattern.ipynb` is an example of using Linear discriminant to isolate CNV-specific asymmetry patterns from raw anatomical data. Bootstraping is implemented to increase robustness.
2.   `scripts/analyze_single_CNV.ipynb` is an analysis script to examine the asymmetry patterns of each CNV separately.
3.   `scripts/analyze_multiple_CNV.ipynb` uses multi-class LDA to highlight similarities and differences among asymmetry patterns of 8 selected CNVs.
4.   `scripts/planum_temporale_analysis.ipynb` is an analysis script to investigate CNV effects on planum temporale.
5.   `scripts/neurosynth_analysis.ipynb` interrogates the NeuroSynth database to functionally annotate derived asymmetry patterns.
6.   `scripts/genetics_asymmtry.ipynb` plots the annotation of SNPs and genes associated with planum temporale asymmetry in GWAS Catalogue.

