---
title: "CICC: Conformal Intent Classification and Clarification"
date: 2024-03-29T21:30:50+01:00
draft: false
tags: [dialog systems, publication]
---

Our work on hashtag#task-oriented dialogue systems has been accepted at ACL's [2024 NAACL](https://2024.naacl.org/) Findings.

Task-oriented dialogue systems help users solve tasks in their daily lives.
In order to do so, these systems have to identify the users intent.

Dialogue systems may be uncertain about the user intent. In these cases, the system can ask the user to clarify, i.e. select from the intents that the system considers likely given the user input.

It is not immediately clear when to ask a clarification question and which intents to include in it.

We propose CICC, a framework for asking clarification questions based on intent sets that contain the true user intent at a high confidence level. These sets are generated with conformal prediction.

An interesting additional application is in out-of-scope detection. This addition to the work was suggested by reviewers, which to me is an important sign of how valuable reviews can be. Many thanks to the anonymous reviewers!

For more information, visit the accompanying [page](https://florisdh.nl/cicc/), check out the [implementation](https://github.com/florisdenhengst/cicc) or see the [preprint](https://arxiv.org/abs/2403.18973).