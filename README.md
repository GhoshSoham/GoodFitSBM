
<!-- README.md is generated from README.Rmd. Please edit that file -->

# GoodFitSBM: Monte Carlo goodness-of-fit tests for Stochastic Blockmodels (SBMs)

<!-- <img src="man/figures/logo.png" align="right" width="150"/> -->
<!-- [![CRAN_Status_Badge](https://img.shields.io/cran/v/MatchIt?color=952100)](https://cran.r-project.org/package=lmw) [![CRAN_Downloads_Badge](https://cranlogs.r-pkg.org/badges/MatchIt?color=952100)](https://cran.r-project.org/package=lmw) -->

### NEWS

GoodFitSBM (Version 0.0.1): `GoodFitSBM` comprises functionality that
performs the *goodness-of-fit* test for an **beta-SBM** (one of the
three variants of SBMs discussed in [Karwa et
al. (2023)](https://doi.org/10.1093/jrsssb/qkad084) used for modelling
network data.

### Note

### Overview

*Stochastic blockmodels* (SBMs) contributed to the theoretical and
algorithmic developments for analyzing *network* data, which has been
facilitated by the availability of data in diverse fields like *social
sciences*, *web recommender systems*, *protein networks*, *genomics*,
and *neuroscience*. SBMs being the generalization of the Erdős-Rényi
model given by [Erdős and Rényi
(1960)](https://doi.org/10.1515/9781400841356.38) was proposed
originally in context of *social sciences* for directed and undirected
graphs, whereas now it has been vastly extended and utilized in *latent
blocks in undirected graphs*, *latent space models*, *variable degree
distribution*, *dynamically evolving networks*, etc., becoming one of
the more popular approaches to model network data in computer science,
statistics and machine learning.

[Karwa et al. (2023)](https://doi.org/10.1093/jrsssb/qkad084) addresses
a very important aspect of *model fitting* by constructing
goodness-of-fit tests (under finite-sample setting) for three variants
of SBMs respectively used for modeling network data (where model
adequacy procedures are somewhat elusive in general), viz., *Erdős-Rényi
SBM* (ER-SBM), *Additive SBM*, and *beta-SBM*, where the main idea
revolves around a *frequentist conditional goodness-of-fit test*
conditioned on a sufficient statistic ([Karwa et
al. (2023)](https://doi.org/10.1093/jrsssb/qkad084) also illustrates its
Bayesian counterpart).

### Intended Use of the package `GoodFitSBM`

Out of the three variants of the SBMs in ([Karwa et
al. (2023)](https://doi.org/10.1093/jrsssb/qkad084)) to model network
data, `GoodfitSBM` addresses goodness-of-fit test under the framework of
a **beta-SBM**. With a focus on *simple undirected*, and *unweighted*
networks (graphs) having *no self-loop*, the package comprises of four
functions viz., `get_mle()`, `goftest()`, `graphchi()`, and
`sample_a_move()` - among which `goftest()` performs the major
functionality of performing the goodness-of-fit test, in process,
obtains the value of the chi-square test statistic and the corresponding
$p-$value, after proper sampling of the graph (a Markov move or basis) -
done by the function `sample_a_move()` under the beta-SBM framework.
Computation of the chi-square test statistic value under the beta-SBM
framework is done by `graphchi()`, which in turn requires the estimates
(maximum likelihood estimation (MLE) in our case) of the edge
probabilities $q_{ij}$ between block $B_i$ and block $B_j$ as,
$\widehat{q}_{ij}$, which is done by the function `get_mle()`.

The corresponding $p-$value obtained from `goftest()` are further
analysed to examine the extent of fit of the beta-SBM to the given
network (graph) (usual rule applies to reject the null of a good fit
when, $p \leq \alpha$ at level $0< \alpha < 1$). There are other
functions collated, each performing the required functionality in the
process, see [GoodFitSBM Github
Repo](https://github.com/Roy-SR-007/GoodFitSBM/tree/master/R) for
details.

### The beta-SBM and Related Goodness-of-Fit (GoF) Framework

In this section, we outline the theoretical part on which the entire
package `GoodFitSBM` is based.

#### Stochastic Blockmodels (SBMs)

Consider $G$ to be a graph on $n$ nodes, $g$ being its realization. It
is assumed that, all graphs are *unweighted* and *undirected*, and there
are *no self-loops*. Therefore, the graph $G$ can also be referred to by
its $n\times n$ adjacency matrix, $\mathbf{g}$, where $g_{uv} = 1$, if
there is an edge between node $u$ and $v$ in the graph $\mathbf{g}$, and
$0$ otherwise.

An *exponential family random graph model (ERGM)* assumes that the
probability of observing a graph $\mathbf{g}$ depends only on a vector
of sufficient statistics, $T(\mathbf{g})$, i.e., the probability of
observing a given network $G=\mathbf{g}$ is,

\$ \_{}(G=) = \$ where
$\psi(\theta) = \sum_{\mathbf{g}}exp(\langle T(\mathbf{g}), \theta\rangle)$
is the normalizing constant, $\theta \in \Theta$ is a vector of natural
parameters, and $T(\mathbf{g})$ is the vector of minimal sufficient
statistics for the underlying model. Let $p_{uv}$ be the probability of
an edge between node $u$ and node $v$, where it is assumed that,
$g_{uv}\sim \mbox{Bernoulli}(p_{uv})$

### Use and Related Functionalities
