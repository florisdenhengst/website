# TODO
* Remove academic theme
  * And all of its posts
* Move profile to 'about' and update
* Search page using Duckduckgo
  * site:<url> searchTerm
* Add page on Msc. thesis supervision
  * How to name it? Tutoring / Mentoring / Students?
* Reading list / books
  * The Circle (Dave Eggers)
  * Dune (all 3)
  * Homo Deus
  * Sapiens
  * A Fire Upon The Deep
* Add post on off-policy policy evaluation
  * How it differs from QLearning
  * https://datascience.stackexchange.com/questions/27311/reinforcement-learning-on-data-only-no-emulators 
  * Use a cart-pole balancing with a random policy from openAI gym
  * How to measure variance of (Weighted) Importance Sampling?
* Claim florisdenhengst.com or some nickname and refer to it
  * Update `baseURL` in ``config.toml``
* Blog post ideas
  * Bitshifting Sudoku Automated Reasoning
  * Route planner project (linked data)
  * PhD in business, experiences
  * Research into mistakes typically made by auditors / regulators
    * Mistakes should reflect situations in ML systems well
    * Do a survey with someone who'd like to work on this
* Random idea snippets page?
  * Learning interpretable reward functions.
    * First learn an explicit (immediate) reward function as in Michal's thesis using a deep
      neural net
    * Then learn a symbolic meta-model of this reward function. This gives insight into what the
      model has learned
    * The insights can be used to inform human decision-makers. We can learn what the model thinks
      is important (e.g. work of Russel on value alignment etc.)
  * Incrementally learning models for RL (incremental GBM?)
    * How to explore ? <- use some model of uncertainty
  * Feature importance estimation using RL?
  * Active Learning for RL -> when rewards need to be collected from a human?
    * When there is a single reward at the end of an episode such as in dialogue systems
      * Other examples?
      * Combine with ongoing rewards
    * Relation to fitness function being human/user-defined in EA's
    * Need to have some sort of
  * A data science project to predict 'negatief reisadvies' based on news / twitter
    * NER to identify news items on countries / regions
    * history of negatief reisadviezen:
      * e.g. [Twitter](https://twitter.com/search?l=&q=Reisadvies%20from%3A247BZ%20until%3A2016-01-01&src=typd)
  * An app that lets you keep track of your phrasings & proposes common mistakes
  * An app that suggests alternative wording in papers
  * An app that analyses your writing and compares it with a target venue
  * An app to keep track of words / sentences you've encountered and liked and used
  * An app/plugin that selects the 'best' google scholar citation e.g. no arxiv etc.
  * Parallelized Dynamic Time Warping
  * Personalized Vocabulary Notebook
  * Parallel Dynamic Time Warping + kNN as a replacement for recurrent nets
    * What is already done on this topic?
    * For example python fastdtw seems to work on Spark
    * https://github.com/MaxBenChrist/Fast-Parallel-DTW-kNN-Python
  * stratified sampling train/test split for off-policy RL -- sample trajectories but stratify by states or state-action pairs.
    This probably requires some optimization to select items -- use an (evolutionary?) optimizer or some other approach
    The goal is for OPE/importance-sampling based approaches to have better coverage of the space during evaluation, hence hopefully have lower variance estimates
  * Weighted model counting for safe RL / RL with constraints. Or even more generally, for any MDP (or even RDP) problem.
  * ...
* Canvas for RL
  * Similar to all types of canvases in project management etc.
  * E.g. Machine Learning Canvas
  * See ReFrame by Phil Winder
* Stabilize tree learning with Conformal Prediction
  * Use a training set to iteratively split the dataset into classes with a greedy heuristic on information gain.
  * Instead of doing a greedy split based on the training set, use a held-out part of the data (calibration set)
  * estimate a lower bound on the information gain using CP within the data-split
  * How different from bagging/boosting?
* PostgreSQL query planning
  * Currently uses genetic algorithm for join plan for large number of joins
  * Could be improved using the data & RL
  * Adaptive setting: https://www.pgcon.org/2017/schedule/events/1086.en.html
  * On Query Optimizers: https://www.vldb.org/pvldb/vol9/p204-leis.pdf
  * HN Thread: https://news.ycombinator.com/item?id=23826295
* parallize largest_number project
* Analogy of read speeds:
  * L1 Cache,1 seconds,grab a piece of paper and look at it
	L2 Cache,14 seconds,pick up a book from nearby shelf
	Memory,4 minutes,walk to coffee machine and get a coffee
	Disk,15 months,travel the world in search of a specific person who happens to know the answer
  * https://manybutfinite.com/post/what-your-computer-does-while-you-wait/
