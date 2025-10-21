---
title: "SHARPIE Tutorial in SIKS course"
date: 2025-10-21T16:38:32+02:00
draft: false
---

We contributed a tutorial on doing real-world experiments involving humans and sequential decision
making agents to a national PhD course on [Reinforcement Learning for Adaptive Hybrid
Intelligence](https://siks.nl/activities/activities/siks-course-rl-for-ahi-2025/). This two-day
course is about making AI agents adapt to humans using reinforcement learning.

We set two goals for our tutorial:
1. Hands-on experience with hybrid RL example
2. Familiarize participants with SHARPIE and a hybrid RL algorithm

# SHARPIE
[SHARPIE](https://github.com/hybrid-intelligence/SHARPIE) is a framework for creating live demo's
and conducting real-world experiments involving humans and RL agents.
It's core idea is to allow researchers to incorporate a human at any point in the RL
agent-environment interface:
![Agent-environment interface with human](/imgs/sharpie-interface.png)

You can read more about the motivation for SHARPIE [on
ArXiv](https://doi.org/10.48550/arXiv.2501.19245) or check out the code base and a demo video [on
GitHub](https://github.com/hybrid-intelligence/SHARPIE).

# Tutorial
In the tutorial, participants were asked to implement a simple tabular version of
[TAMER](https://ieeexplore.ieee.org/abstract/document/4640845) in the FrozenLake environment.
This early-days RLHF algorithm learns an immediate reward model from human feedback and then
derives a policy that maximizes the immediate rewards. This can lead to very fast learning, if the
feedback provided by the human is correct and timely.

The tutorial took only 45 mins and consisted of a plenary introduction (~10mins), a hands-on
break-out part (30 mins), and a brief plenary reflection (~5 mins). The hands-on break-out part
consisted of two tracks:
1. Setting up a TAMER micro-experiment in a locally hosted SHARPIE, by writing code to set the
   experiment and get the algorithm to learn correctly.
2. Participating in a TAMER micro-experiment in an [online hosted](https://sharpie.science.uu.nl/) SHARPIE,
   by interacing with a TAMER agent and answering some analysis and reflection questions.

# Learnings
I hope the participants were inspired to think about different interaction paradigms between
humans and RL agents, but here I focus on what *I* learned from this tutorial.

Firstly, it really helps to formulate and share the learning outcomes for the participants. This
helps to get everyone on the same page quickly.

Secondly, the importance of offering various approaches to meet the learning goals for different
students stood out. The two break-out tracks were both challenging, but in different ways. The
setting-up track had technological challenges whereas the participation track had more
experiential and conceptual challenges.

Another learning is to take enough time for reflection, consolidation and follow-up. Due to delays
in the programme and overall chaos ensuing from helping 25 eager PhD. students to conduct an
exercise involving programming / RL / tech dependencies etc. I failed to focus on the reflection
and follow-up parts of the tutorial. Next time, I will ensure to draw more attention to this
part as it is important to make sure the material solidifies and so that there is an opportunity
for students to continue thinking about the material.

Overall, it was very exciting to see all students interacting with a system I am happy to
contribute to.



