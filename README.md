
<!-- README.md is generated from README.Rmd. Please edit that file -->

# GoodFitSBM: Monte Carlo goodness-of-fit tests for Stochastic Blockmodels (SBMs)

<!-- <img src="man/figures/logo.png" align="right" width="150"/> -->

## <!-- [![CRAN_Status_Badge](https://img.shields.io/cran/v/MatchIt?color=952100)](https://cran.r-project.org/package=lmw) [![CRAN_Downloads_Badge](https://cranlogs.r-pkg.org/badges/MatchIt?color=952100)](https://cran.r-project.org/package=lmw) -->

### NEWS

GoodFitSBM (Version 1): `GoodFitSBM` comprises functionality that
performs the *goodness-of-fit* test for an **beta-SBM** (one of the
three variants of SBMs discussed in [Karwa et
al. (2023)](https://doi.org/10.1093/jrsssb/qkad084) used for modelling
network data.

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
SBM* (ER-SBM), *Additive SBM*, and *$\beta-$SBM*, where the main idea
revolves around a *frequentist conditional goodness-of-fit test*
conditioned on a sufficient statistic ([Karwa et
al. (2023)](https://doi.org/10.1093/jrsssb/qkad084) also illustrates its
Bayesian counterpart).

------------------------------------------------------------------------

### Use and Related Functionalities
