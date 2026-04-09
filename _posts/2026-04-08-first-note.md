---
title: "My First Note - Proximal Point Method under sharp growth"
classes: wide
categories:
  - notes
---

Hello everyone, thanks for visiting my notes page. I’ve long wanted to write down the things I learn and discover, but I never quite got around to starting—until now. This will be officially my first note post, which is a simple proof about the finite time convergence of the proximal point method for a convex function with sharp growth. The main reference is Appendix A from [General Holder Smooth Convergence Rates Follow From
Specialized Rates Assuming Growth Bounds](https://arxiv.org/pdf/2104.10196).



We consider the a convex function $f:\mathbb{R}^n \to :\mathbb{R}$ and the proximal point method which follows the update 
$$
    x_{k+1} = \mathrm{Prox}_{f,\rho}(x_k) := \{\argmin_{y} f(y) + \frac{1}{2\rho}\|y - x_k\|^2 \}, \; \forall k \geq 1,
$$
where $\rho > 0$ is fixed.
We further assume the function $f$ satisfies the sharp groth condition
$$
    \mu \mathrm{Dist}(x,S) \leq  f(x) - f^\star
$$
where $S= \argmin_{s} f(x)$ is the optimal soluiton set.