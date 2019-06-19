---
title: "Gaussian Processes in Reinforcement Learning"
date: 2019-04-25T20:01:24+02:00
draft: true
---

* Gaussian Processes are a fascinating tool for usage in RL due to modelling uncertainty and data efficiency
* I have briefly introduced GP's and shown how/why they are used in RL and inspire for other
  approaches

Gaussian Processes (GP) are a fascinating tool for regression. Instead of estimating a
distribution of points, they estimate a distribution of *functions*. The estimated distribution
can be used to create point estimates with confidence intervals, so they come with a 'built-in'
estimate of uncertainty. This estimate is useful in settings where points can be sampled
interactively, such as in active learning and reinforcement learning (RL). Another strength of GPs
is that we can specify a *prior* over the functions. This generally makes GPs very data efficient,
a property of interest in both kinds of Machine Learning.

Although GPs are a very generic Machine Learning tool, can be used for both regression and
classification and have been around for a long time, I was first introduced to them when studying
[ways to apply RL to dialogue control](/posts/rl-for-dialogue-management). In this post, I hope to
provide you with some understanding of GPs (or at least some pointers!) and explain how they can
be used in RL. If you won't like them for their mathematical properties, I'm sure you'll like the
visualizations and linked videos throughout this blog post. I will start with a brief introduction
of GPs and then move on to applications in RL.

<figure style="max-width:80%;">
 <img src="/imgs/gp-for-rl/3d-rbf.png"
      alt="3D visualization of the RBF kernel"
      style="max-width:400px;"/>
 <figcaption>Figure 1. A Pretty Pictures!
 </figcaption>
</figure>

Let's inspect the definition of a GP: "A Gaussian Process is a collection of random variables, any
finite number of which have a joint Gaussian distribution."[^1] Formally, some function \\(f(x)\\)
over a set \\(X\\) follows a GP distribution as defined by some mean \\(\mu\\) and a *covariance
function* \\(k(x, x')\\):
    $$f(x) \sim \mathcal{GP}(\mu(x), k(x, x')), \forall xx' \in X \\\\\
      \mu(x) = \mathbb{E}[f(x)]  \\\\\
      k(x, x') = \mathbb{E}[(f(x) - \mu(x))(f(x') - \mu(x'))]
    $$
As a simple example of a GP, consider the data in Figure 2. 
<figure style="max-width:80%;">
 <img src="/imgs/gp-for-rl/MultivariateNormal.png"
      alt="3D visualization of a 2-variable jointly gaussian distribution"
      style="max-width:400px;"/>
 <figcaption>Figure 2. Data sampled from an example GP.
 </figcaption>
</figure>
This data is distributed according to
a multivariate Gaussian with 
$$ \mu = \begin{bmatrix} 0 \\\\ 0 \end{bmatrix},
    K =  \begin{bmatrix} 1 & 3 / 5 \\\\ 3 / 5 & 2 \end{bmatrix}
$$
This distribution is a GP, since it consists of two random variables, \\(X\\) and \\(Y\\), that
are distributed Gaussian together or 'joint'. The random varaiables \\(X\\) and \\(Y\\) are
Gaussian distributed individually as well, so we meet the definitions. Let's move on to some
properties of GPs.

Multivariate Gaussians allow for some manipulations that are useful when doing predictions. For
starters, we have already seen that we can extract single-variable \\(\mu\\)s from joint
distribution. We can do the same for the covariance matrix and obtain the individual distributions:
    $$ \mu = \begin{bmatrix} \mu\_{X} \\\\ \mu\_{Y} \end{bmatrix},
        \Sigma = 
        \begin{bmatrix}
            \Sigma\_{XX} & \Sigma\_{XY} \\\\ \Sigma\_{YX} & \Sigma\_{YY}
        \end{bmatrix}
    $$
Extracting distributions for \\(X\\) and \\(Y\\):
    $$ X \sim \mathcal{N}(\mu\_{X}, \Sigma\_{XX}) \\\\ Y \sim \mathcal{N}(\mu\_{Y}, \Sigma\_{YY}) $$
This manipulation is commonly known as *marginalization*.

Another manipulation that is useful for prediction is *conditioning*. Conditioning boils down to
expressing the distribution one variable in terms of the other. The full derivation is too much
for a blog post, but this is the information you'll need in order to do so:
$$ \begin{align}
    Y | X \sim \mathcal{N}( & \mu\_{Y} + \Sigma\_{YX} \Sigma\_{XX}^{-1}(X - \mu\_X), \\\\\
     & \Sigma\_{YY} - \Sigma\_{YX} - \Sigma\_{YX}\Sigma\_{XX}^{-1}\Sigma\_{XY})
  \end{align}
$$
In supervised prediction settings with target variable \\(Y\\), \\(\Sigma\\) and \\(\mu\_Y\\) can
be estimated based on the training set and predictions on input \\(X\\) can be made.[^2] Note that
here, a prediction is a *distribution* rather than a point estimate.

A third property of GPs is that they can take domain knowledge into account through a *prior* on
the kernel function. We can express some properties of coveriance matrices in some domain and
thus limit the variance of our predicted distribution \\(Y\\). Although finding the right kernel
requires some understanding of the problem at hand, many different kernels have been explored in
various domains.[^3]

Explain how GPs are constructed:
 * treat different points as individual random variables
 * concatenate the train and test set
 * factor & condition
 * profit
 * Step-wise through figures

Some examples:
 * Videos

More on kernels?


*TODO: Link back from rl-for-dialogue-management post*

*TODO: Link from rl for personalization post*

[^1]: CE Rasmussen, CKI Williams, "Gaussian Processes for Machine Learning.", MIT Press, 2006
[^2]: Note that this kind of regression where each random variable denotes a feature of the models
  is more akin to Bayesian Regression than to GPs. In GPs, random variables denote train and test
  points of the model.
[^3]: [The Kernel Cookbook](http://www.cs.toronto.edu/~duvenaud/cookbook/index.html) by David
  Duvenaud
