---
title: "The Book that Predicted AlphaGo"
date: 2018-08-01T21:54:28+01:00
tags: [Reinforcement Learning]
---

Little under three years ago, in March 2016, a Reinforcement Learning (RL) algorithm beat Lee
Sedol, a pro
player in a match of Go. This game had been considered too hard for algorithms due to the
[astronomical](https://en.wikipedia.org/wiki/Go_and_mathematics#Complexity_of_certain_Go_configurations)
number of board game configurations and the AlphaGo team therefore baffled experts in AI with their
accomplishments. Nobody seemed to be aware that techniques were available to make such a win
possible at that time and most experts considered computers beating humanity at Go to be a couple
of decades away. Which is why I was surprised to find a mention of Go in a
'Looking into the Future' chapter of [a
book](https://www.springer.com/us/book/9783642276446) on RL from 2012, which was
written at least four years prior to AlphaGo's triumph:

The quote reads:
```
Some very complex games, such as Go, are currently best played by a computer
that uses Monte-Carlo tree search (Coulom, 2006). RL methods can hardly be
employed well for playing such games.  The reason is that it is very difficult
to accurately represent and learn the value func- tion.  Therefore, a lot of
search and sampling currently works better than knowledge intensive solutions.
The search/knowledge tradeoff (Berliner, 1977) states that more knowledge will
come at the expense of less search, since models containing more parameters
consume more time to evaluate. It would be very interesting to gain un-
derstanding of novel RL methods that can quite accurately learn to approximate
the value function for complex games, but which are still very fast to evaluate.
Some research in this direction was performed for the game of chess (Baxter et
al, 1997; Veness et al, 2009) where linear models trained with RL could be
efficiently used by the search algorithms.
```

In the end, it turned out to be Deep Neural Networks instead of linear models. It took about four
years to get there, roughly equalling the lenght of a PhD in The Netherlands. It makes me wonder
which problems currently considered as 'unsolvable' will be cracked in four years time.
