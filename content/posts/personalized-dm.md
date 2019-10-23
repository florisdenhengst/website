---
title: "Personalized Dialogue Management"
date: 2019-10-21T10:31:06+02:00
draft: false 
tags: [publication, dialog systems, personalization, reinforcement learning, pomdp]
---

In a [previous post](/posts/rl-for-dialog-management) I explained how reinforcement
learning (RL) can be used to make chatbots better from its experience with users. RL allows chatbots to learn what to say by interacting with users. This allows for chatbots to tailor their behavior to preferences of groups of individuals. I recently presented our paper on
    personalized dialog management at the [Web Intelligence](http://localhost:1313/posts/rl-for-dialog-management/) in Thessaloniki, a conference where only 19% of all submitted papers were accepted as full paper.

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

Next steps may include an evaluation on more realistic data and ensuring that the chatbots only
makes recommendations after having checked e.g. the [risk
profile](https://www.investopedia.com/terms/r/risk-profile.asp) and ensures that the
recommendation is understood by the user.


![logo Web Intelligence 2019](/imgs/personalized-dm/wi-19-logo.png)
