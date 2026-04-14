---
title: "My First Note - Proximal Point Method under sharp growth"
classes: wide
categories:
  - notes
---

Hello everyone, thanks for visiting my notes page. I’ve long wanted to write down the things I learn and discover, but I never quite got around to starting—until now. This will be officially my first note post, which is a simple proof about the finite time convergence of the proximal point method for a convex function with sharp growth. The main reference is Appendix A from [General Holder Smooth Convergence Rates Follow From
Specialized Rates Assuming Growth Bounds](https://arxiv.org/pdf/2104.10196).




We consider the a convex function $$f:\mathbb{R}^n \to :\mathbb{R}$$ and the proximal point method (PPM) which follows the update 

$$
\begin{align}
    x_{k+1} = \mathrm{Prox}_{f,\rho}(x_k) := \{\arg \min_{y} f(y) + \frac{1}{2\rho}\|y - x_k\|^2 \}, \; \forall k \geq 1,
\end{align}
$$

where $$\rho > 0$$ is fixed.

We further assume the function $$f$$ satisfies the sharp growth condition

$$
\begin{aligned}
    \mu \mathrm{Dist}(x,S) \leq  f(x) - f^\star
\end{aligned}    
$$

where $$S= \arg \min_{s} f(x)$$ is the optimal soluiton set. Below, we show that the PPM converges to any accuracy in at most a fixed bounded iteration number. 


> **_Theorem._** For any accuracy $$\epsilon \geq 0$$, the PPM applied to a convex function satisfying sharp growhth is able to find the true solution in at most $$\frac{f(x_0) - f^\star}{\frac{\rho \mu }{2}}$$ iterations.


**Proof.**
From the optimality condition of the proximal update, we have 

$$
\begin{aligned}
   v_k := (x_k- x_{k+1} )/\rho \in \partial f(x_{k+1}). 
\end{aligned}
$$

By convexity of $$f$$, we have that 

$$
\begin{aligned}
\|x^\star- x_{k+1} \| \|x_k- x_{k+1} \| /\rho \geq \langle v_k, x^\star- x_{k+1}   \rangle / \rho  \geq f(x_{k+1}) - f^\star   \geq \mu \|x^\star- x_{k+1} \|.
\end{aligned}
$$

Dividing both sides by $$\|x^\star- x_{k+1} \|$$ yields that the step length is always lower bounded by a constant 

$$
\begin{aligned}
    \|x_k- x_{k+1} \|  \geq \rho \mu.  
\end{aligned}
$$

By the defintion of the update, we have that the cost function improvement is also always lower bounded by a constant 

$$
\begin{aligned}
    \frac{\rho \mu }{2} \leq \frac{1}{2\rho}\|x_k- x_{k+1} \|^2 \leq f(x_k) - f(x_{k+1}).
\end{aligned}
$$

From here, one can easily argue that the $$f(x_k)$$ becomes $$f^\star$$ in finite iterations.