---
title: "Personalized Dialogue Management"
date: 2019-10-21T10:31:06+02:00
draft: false 
tags: [publication, dialog systems, personalization, reinforcement learning, pomdp]
---

In a [previous post](/posts/rl-for-dialog-management) I explained how reinforcement
learning (RL) can be used to make chatbots better from its experience with users. RL allows chatbots to learn what to say by interacting with users. This allows for chatbots to tailor their behavior to preferences of groups of individuals, e.g. to *personalize* the interaction. I recently presented our paper on
    this topic, specifically on personalized dialog management at the [Web Intelligence](https://webintelligence2019.com/) conference in Thessaloniki. In this conference, only 19% of all submitted papers were accepted as full paper. I'll briefly describe the main contributions of the paper here.

In many domains, including financial services and banking, some users may be able to express their needs and preferences crisply whereas others have more difficulty in doing so. As an example, consider someone looking to finance their first
home. They will not know much about duration of the mortgages, adjustable and fixed-rate and
associated costs. Compare this to a person who already has a mortgage and is looking for a
mortgage transfer. They will be quite aware of the terminology involved and may already have done
some research on the subject.

Capabilities, desires and preferences of individual chatbot users may differ in many ways and it
may not always be clear upfront how the chatbot should respond to these differences in order to
*personalize* the user experience. In these cases, the only resort is to respond to feedback from
users in order to do so.  In the [paper](/publications/wi19.pdf), we compare two novel approaches
to personalized dialogue management. Both approaches use RL to personalize the user experience
based on experience with individual users. We trained and evaluated the approaches in a large
benchmark of different algorithms.

It turns out that learning approaches can respond to differences in user behavior effectively and
personalize the user experience. What's more, it turns out that these approaches perform equal or
better than a previous hand-coded gold standard. Which of the two learning approaches works best
depends on the complexity of the task and the available data.

Next steps may include an evaluation on more realistic data, ensuring that the chatbots only
makes recommendations after having checked e.g. the [risk
profile](https://www.investopedia.com/terms/r/risk-profile.asp) and check that the
recommendation is understood by the user.

*Update 2020-04-09*: Interested in reinforcement learning and personalization outside of
dialogue management? Have a look at the literature study we did on this in [this
post](/posts/rl-for-pers-survey/).

*Update 2022-03-04*: In [this new paper](/posts/planning-for-potential/) we
learn an optimal dialogue policy under safety constraints.

*Update 2022-06-21*: In [this post](/posts/intro-to-gps/) I dive into the usage of Gaussian processes for (personalized) dialogue management.


![logo Web Intelligence 2019](/imgs/personalized-dm/wi-19-logo.png)
