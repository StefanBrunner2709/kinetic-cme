---
permalink: /interface/
title: "Python interface"
---

Here we will describe different ways on how to use generator_class to generate models, set up our tree with initial conditions and run the kinetic-cme code.
For the explanation of the steps we will consider the bax example.

## Model generation

Before we can generate our model, we need to import the necessary libraries and define our Sympy variables.

```python
import numpy as np
import sympy as sp

from src.generator import Model, Partitioning, run, species

S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10 = species(
    "S0, S1, S2, S3, S4, S5, S6, S7, S8, S9, S10"
)
```