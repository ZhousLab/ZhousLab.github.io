---
layout: page
title: Koopman operator:why, what and how
permalink: posts/koopman/
---

## 1. Why we need Koopman operator
Linearity is a desireable prpoperty in many problems. Linearization near a fixed point of a nonlinear system provides a **local** linearization expression, while Koopman operator provides a **global** linearization expression of the system using higher(infinite) number of dimansional nonlinear coordinates.

Under some constrains, **Koopman decomposition** is closely related with and approxiamted by **DMD** and **DFT**.
## 2. What is a Koopman operator
Koopman operator is an infinite-dimension linear system that advances **ANY** observation $g(x)$ one time step forward, e.g. $g(x) = x$ if use the measured observable directly. It's a Markov operator.

$$\kappa_t g = g \circ F_t$$


Where $\kappa_t$ is our Koopman operator, and $F_t$ is the forward operator.

---

For a **discrete-time system** with timestep $\Delta t$, it can be write as

$$\kappa_t g(x_k) = g(F_t(x_k)) = g(x_{k+1})$$

For **continous system**, we have:

$$\frac{d}{dt}g=\kappa g$$

Operator $\kappa$ can be understand from the definition of differential, and linked with Koopman operator $\kappa_t$ by

$\frac{d}{dt}g = \lim_{t \to 0} \frac{g(x_{k+1}-g{x_k})}{t} = \frac{\kappa_t g-g}{t} = \kappa g$

The third term is a function of $g$ and can be denoted as $\kappa g$


## 3. How can I calculate/estimate Koopman eigenfunction?
We can calculate some Koopman eigenvectors if we have known governing equation of some simple forms. Mostly, we apply dynamical mode decomposition(DMD) to **estimate** it.
