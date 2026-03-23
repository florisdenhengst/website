---
title: "HIAL Guest Lecture"
date: 2026-03-19T17:02:26+01:00
draft: false
tags: [teaching,reinforcement learning, sharpie]
---

Today I gave a guest lecture for the course [Human-interactive Agent
Learning](https://research.vu.nl/en/courses/human-interactive-agent-learning-2/).
I presented [SHARPIE](https://sharpie.readthedocs.io/en/latest/), our tool for controlled human-RL experiments.

During the lecture, I showed how SHARPIE can be used to implement a simple evaluative feedback
experiment using
[TAMEr](https://www.cs.utexas.edu/~bradknox/kcap09/Knox_and_Stone,_K-CAP_2009.html) in the MountainCar environment.
Nothing beats putting the pressure on as a bit of live coding does, but then it remains so much
fun when you can actually show how simple it is to implement this experiment with the right tools
at hand.

The group was small but highly engaged, and I received many interesting questions, the most
interesting to me was about limitations of SHARPIE and its client-server architecture when it
comes to doing experiments involving physical robots.

I will give some more thought on this for future SHARPIE development, it would be nice challenge
to see how SHARPIE could be used for this and whether it should be preferred over existing tools.

The key take-away for me, however, was how easy it has become to set up experiments in the recent
version of SHARPIE compared to a [couple of months
ago](https://florisdh.nl/posts/siks-course-sharpie/).
