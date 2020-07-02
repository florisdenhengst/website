---
title: "Reinforcement Learning for Personalization: A Survey"
date: 2020-04-09T09:22:30+01:00
tags: [reinforcement-learning, publication, personalization, pomdp, media]
draft: false
---

*Update 2020-06-27*: this paper was presented as a `poster'(video) at the [RL for Real Life virtual
Conference](https://sites.google.com/view/RL4RealLife). Read more
[here](/posts/rl-at-workshop/).

Reinforcement learning (RL) is becoming an increasingly popular tool to tackle hairy problems
using data. A nice example of such a hairy problem is *personalization*. Personalization 
refers to a task central to many applications of data science and machine learning: to change a
system so that its personal relevance to an individual or category of individuals is increased.

Although RL is becoming more popular, a clear overview of different RL approaches within
personalization is lacking. The reason for this may be that RL is applied to personalization
problems in different domains which each have their own tasks, terms and events. However,
different fields may find related problems, [solutions](/posts/personalized-dm) and conclusions
with respect to the usage of RL in a personalization setting. This is why I
performed a literature study into the usage of RL for personalizaton problems, together with [Eoin
Grua](https://emgrua.github.io/), [Ali el Hassouni](https://alihassouni.github.io/) and [Mark
Hoogendoorn](https://www.cs.vu.nl/~mhoogen/).

We collected data on papers in a systematic literature review and looked at different aspects
of problem setting, solution and evaluation. The resulting overview serves as an excellent
bibliography for both practitioners and researchers with a personalization problem at hand.
Furthermore, we identify some research gaps, such as efficient usage of data and ensuring safety
of systems. These are interesting for RL researchers looking to contribute to this new field.

As the data collected contains many more insights than those covered in the paper, we also
released the data and an [online tool](/rl4personalization). As a preview,
check out the plot below, which shows the number of papers that report on using RL for a
personalization task over time. Note that data was collected June 1st and only covers the last
year partially. It is clear that RL is becoming more and more popular.

The [paper](https://doi.org/10.3233/DS-200028) can be accessed at [Data Science](https://www.iospress.nl/journal/data-science/) journal.

![Paper volume per year](/imgs/rl-for-pers-survey/paper_volume_per_year.png)
