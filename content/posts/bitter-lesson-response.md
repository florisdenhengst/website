---
title: "Bitter Lesson Response"
date: 2019-03-20T23:27:28+01:00
draft: false
---

A couple of days ago, RL founding father Rich Sutton posted a [blog
post](http://www.incompleteideas.net/IncIdeas/BitterLesson.html). My reading is as follows:

* Moore's Law has consistently made general, compute-based methods outperform task-specific,
  domain knowledge-based methods for tasks in the AI `sphere of interest'
* This has served as a bitter lesson for many (all?) researchers that have focused on developing
  such domain-specific methods
* General methods will always prevail, especially those that scale with compute

Although I tend to agree with the overall idea that general methods are the way forward for AI, I
feel that some nuance is in order. Specifically, I feel that task-specific methods fullfill an
crucial role by showing what can be accomplished on a narrow task and thus serves like a telescope
into the future and that the role of *data* is not appreciated
by Prof. Sutton. The availability data useful to some task may have natural limits. 

Data has been a huge enabler of recent advances in AI. Prof. Sutton only mentions compute as the
main driver for success in AI but I think availability of high-quality data sets may be equally or
even more important. Curated data is necessary for all approaches in AI. Even unsupervised methods
require curated data sets of evaluation and hyper-parameter tuning. We currently see this in GANs,
which despite being purely unsupervised are still mostly used on data we can easily inspect
ourselves (images and audio) or where labels are available in large quantities. Developing
these methods in a systematic and reliable, e.g. *scientific* way requires a 
data set representative to some realistic problem setting. One could argue that, as AI techniques
become more powerful and general, the datasets to evaluate them by can become equally general.
This may be true in the long run, so I guess that from a decades-long POV the argument holds.

In the meantime, however, we want our research to be useful for society at large. In my view, the
current triumphs of AI are the result of the fields' focus on practical solutions since the mid 90s.
Without AI focusing on very practical applications, such as e.g. the Data Mining and Semantic Web
subfields, we would have neither the datasets nor the support from public nor private funding we
currently enjoy. These domain-specific approaches used e.g. manually crafted features to show how
powerful data-driven computer vision techniques could be and thus served as a `telescope' into the
future. The main point to me is thus not about what to work on (`general' v.s. `task-specific')
but what to work on *now*. 

My vision on the matter is unfortunately a bit more boring than Prof. Sutton's extremist stance:
in determining what to work on, AI researchers should take into account the practical
applicability now while considering implications to general approaches on the long run.
