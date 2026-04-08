---
title: "Finite convergence of proximal point under sharp growth"
date: 2026-04-08
tags:
  - optimization
  - proximal-point
#excerpt: "A short note on why sharp growth can force finite termination."
---

## Main idea

Suppose \(f\) satisfies a sharp growth condition around the solution set.  
Then one can lower bound the step size of the proximal point iterates before termination.

## Sketch

Let
\[
x_{k+1} \in \arg\min_x \left\{ f(x) + \frac{1}{2\rho}\|x-x_k\|^2 \right\}.
\]

Under sharp growth, one can show that if \(x_{k+1}\) is not optimal, then
\[
\|x_{k+1}-x_k\| \ge c
\]
for some constant \(c>0\).

Since the iterates remain in a bounded region, this cannot happen indefinitely.  
Therefore the method terminates in finitely many steps.