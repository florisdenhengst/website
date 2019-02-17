---
title: "How Reinforcement Learning is Applied to Dialogue Control"
date: 2019-02-15T12:41:16+01:00
tags: [tutorial, dialog systems, reinforcement learning, pomdp]
draft: true
---

The value offering of most contemporary chatbot platforms consists of packaging state-of-art
Automated Speech Recognition (ASR, or 'speech-to-text'), Natural Language Understanding (NLU) and
Voice Synthesis into a comprehensive API. The API typically also includes some programming
model for dialog control such as DialogFlows' [Contexts and follow-up
Intents](https://www.youtube.com/watch?v=-tOamKtmxdY) and Alexa's [Dialog
model](https://developer.amazon.com/docs/custom-skills/define-the-dialog-to-collect-and-confirm-required-information.html).
It's also up to the developer to model relevant dialog flows and craft rules to determine what the
bot should do next. Figure 1 summarizes this in a diagram. Developers can use their experience
and common sense or even turn to [focus
groups](https://ctb.ku.edu/en/table-of-contents/assessment/assessing-community-needs-and-resources/conduct-focus-groups/main)
and A/B tests in optimizing these parts of the bot. Although making all optimization decisions
upfront works well in small systems, it fails to scale to applications where many decisions are
involved such as when a *personalized* chatbot is desired. [Reinforcement
Learning](http://www0.cs.ucl.ac.uk/staff/D.Silver/web/Teaching_files/intro_RL.pdf#page=6) (RL) can
help in such cases. In this blog post, I'll describe the formalism underlying most dialog
management models, explain how this formalism can be generalized to support more flexible dialog
management and finally, how RL can be used to optimize dialog management using data.

<figure style="max-width:70%;">
 <img src="/imgs/rl-for-dialog-management/dm-overview.png"
      alt="Dialog Systems Overview" />
 <figcaption>Figure 1. Overview of components in most commercially available dialog systems. The
 orange components are typically optimized using Machine Learning whereas green components are
 typically hand crafted.
 [<a href="https://docs.google.com/drawings/d/1onFCYv6-NcGCIUuV9GOFhEoAGBSJuVVf4sFQuj62rrc/edit?usp=sharing)">src</a>]
 </figcaption>
</figure>

First, let's consider the following dialog for ordering a drink at Marvin the Paranoid Android:
<figure style="max-width:80%;">
 <img src="/imgs/rl-for-dialog-management/dialog.png"
      alt="Example dialog" />
 <figcaption>Figure 2. Example dialog for ordering a drink with Marvin the Paranoid Android.
 [<a href="https://docs.google.com/drawings/d/173R4ZuTm1vomf2vha0w-UjgVVLiMXfngVrURV_wNYpo/edit?usp=sharing">src</a>]
 </figcaption>
</figure>

Marvin also serves tea in case a nonalcoholic beverage is preferred and can bring users that
aren't thirsty at the moment a towel. When the user doesn't want anything of this, they can end
the interaction and leave Marvin to contemplate life. Finally, let's assume that users don't lie
to Marvin about their preference for alcohol. We can formalize all of these possibilities as a
*finite state machine* in which states are defined in terms of the available information in the
system and transitions are by a system utterance and user response. This yields the following
model in Figure 3, which can be hand coded by Marvin's developer.
<figure style="max-width:80%;">
 <img src="/imgs/rl-for-dialog-management/fsm-dialog.png"
      alt="Finite-state-machine for dialog" />
 <figcaption>Figure 3. Finite State Machine for Marvin's interaction.
 [<a href="https://docs.google.com/drawings/d/12vGvqUOlm1rj5NOdkPS30cCUkhLrlNKFoh36nU4OBqc/edit?usp=sharing">src</a>]
 </figcaption>
</figure>

Now, consider that Marvin's NLU or ASR modules are imperfect and sometimes think that users
without thirst would like a drink. Or consider that users sometimes prefer a tea when they learn
the only alcoholic option is a Pan-Galactic Gargle Blaster. Or that users want both a drink and a
towel. Or that users might order for the entire party aboard their spaceship. Modelling all of
this makes the state machine much bigger and requires making many nontrivial choices. What if we
could learn how the dialog should be structured from data?

For a learning approach to be useable, all states in the state machine must connected first: we do
not know what kind of interactions the data will show and do not want to exclude situations
upfront as the point of the exercise is to use what is shown from real data. Furthermore, we need
some way to model all actions of Marvin. In this example, Marvin can ask whether the user is
thirsty, whether an alcoholic or non-alcoholic beverage is preferred and can propose his three
offerings: Pan-Galactic Gargle Blasters, tea and towels. Finally, in order to model possible
errors in NLU and ASR, we can replace the `yes`/`no` options with values that express the
confidence of the ASR/NLU models in their understanding of the user.

Introduce MDP process and highlight why it's not markovian 

Introduce POMDP.

Link to other posts that deal with policy optimization.


