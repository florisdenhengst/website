---
title: "Symbolic Quantile Regression"
date: 2026-05-20T12:59:21+02:00
draft: false
tags: [publication]
---

Throwback to this [post](/posts/ictopen25/) about ICT.OPEN!

This research with Cas Hoekstra has by now been published by [Transactions on Machine Learning Research](https://openreview.net/forum?id=x9OYbyPJOG).

We introduce Symbolic Quantile Regression (SQR), a framework that bridges the gap between high-performance numerical prediction and human-level interpretability:
* SQR generates concise, closed-form mathematical expressions that explain why a specific quantile (like the median or the 90th percentile) is being predicted. Transparency is built-in.
* In an extensive evaluation of 122 datasets, SQR outperformed existing transparent models and performed comparably to strong black-box baselines. 
* SQR's preference for simpler models helps it to generalize better to out-of-distribution data compared to more complex models. 

We also apply the framework on an airline fuel usage prediction task. Here, the goal was to understand why some flights use much more fuel than others.

We incorporated variety of features that could explain fuel usage and let SQR construct models to predict median (\\(\tau=.5\\)) and extreme (\\(\tau=.9\\)) fuel usage for a partner in the airline industry providing a big dataset spanning multiple flights across several years.

We then studied the resulting models and found that a key difference between the two models is the appearance of the so-called *adjusted speeding factor*, a feature that measures whether a pilot is speeding to make up for lost time during turnaround.
SQR thereby helped identify operations and scheduling as a target for CO2 reductions by providing interpretable and actionable predictive models at various locations of the fuel usage distribution.
