---
permalink: /about/
title: "About"
---

`kinetic-cme` solves the chemical master equation (CME),

$$\partial_t{P}(t,x) = \sum_{\mu = 1}^{M}\left(a_\mu(x-\nu_\mu)P(t,x-\nu_\mu) - a_\mu(x)P(t,x)\right)$$

according to the algorithm proposed in [https://arxiv.org/abs/2407.11792](https://arxiv.org/abs/2407.11792), which is based on the projector-splitting integrator for Tree Tensor networks.[^fn1]

$P(t,x)\,\mathrm{d}t$ is the probability of finding a population number of $x = (x_1, \dots, x_N)$ molecules of species $S_1, \dots, S_N$ in the time interval $[t,\,t + \mathrm{d}t]$.
The CME describes the time evolution of this probability distribution $P(t,x)$ in a chemical reaction network with $N$ different species $S_1, \dots, S_N$, which can react via $M$ reaction channels $R_1, \dots, R_M$. For a given reaction $\mu$, the stoichiometric vector $\nu_\mu$ denotes the population change by that reaction and the propensity functions $a_\mu(x)$ and $a_\mu(x-\nu_\mu)$ are proportional to the transition probabilities $T(x+\nu_\mu|x)$ and $T(x|x-\nu_\mu)$.

`kinetic-cme` makes use of the low-rank framework [Ensign](https://github.com/leinkemmer/Ensign).[^fn2]

## References
[^fn1]: Ceruti, G., Lubich, C., and Walach, H.: Time integration of Tree Tensor networks", SIAM J. Numer. Anal. **59** (2021)
<!-- Lubich, C., Oseledets, I.: "A projector-splitting integrator for dynamical low-rank approximation", BIT Numerical Mathematics **54** (2014) -->

[^fn2]: Cassini, F., and Einkemmer, L.: "Efficient 6D Vlasov simulation using the dynamical low-rank framework Ensign", Comp. Phys. Comm. **280** (2022)