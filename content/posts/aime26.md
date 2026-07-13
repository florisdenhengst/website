---
title: "Best Paper: AI in Medicine 2026"
date: 2026-07-13T14:52:31+02:00
draft: false
tags: [publication]
---

Our paper on ``Addressing Incomplete Data in Survival and Quality of Life Prediction: a Pancreatic Cancer Case Study" won the best paper award at [AIME 2026](https://aime26.aimedicine.info/) (AR ~20%) ! 

In this work, we address the joint prediction of survival and quality-of-life for patients suffering from pancreatic cancer, in the face of various forms of missing data distributed heterogeneously over time.
Focusing on the technical contributions, there are two:
1. we extend random survival forest with a missing-aware component implemented in the split criterium. It penalizes features with many 'missings' so that during tree formation these features are preferred less when forming a new data split node. This yields comparable predictive performance without having to do imputation (introduces bias) or missingness indicator features (increases #features and harms interpretability)
2. we combine two types of conditional generative models based on diffusion for synthesizing a pre-treatment quality-of-life baselines, and longitudinal sequences of quality of life conditioned on the treatment at arbitrary time windows. The predicted quality of life trajectories can be used during treatment planning.

We hope this can help make patients more informed decisions during a critical point in their care journey when they have to balance to "how long?" with "how well?" in choosing their personal treatment plan.

The algorithm for the missing-aware random survival forest is available as a pip package on [Pypi](https://pypi.org/project/masurvival/).

![Conference organizers hand over the award](/imgs/aime26_best_paper.PNG)
