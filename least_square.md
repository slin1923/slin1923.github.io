---
layout: default
title: Least Squares
---
<font size="5">Index</font>
- [OLS: ordinary LS](#ols-ordinary-ls)
  - [Formulation:](#formulation)
  - [Solution:](#solution)
- [Flavors](#flavors)
  - [WLS: Weighted LS](#wls-weighted-ls)
  - [IRLS: Iteratively Reweighted LS](#irls-iteratively-reweighted-ls)
  - [NLS: Nonlinear LS](#nls-nonlinear-ls)


# OLS: ordinary LS

## Formulation: 

The standard formulation for a least-squares problem is given a system of linear equations 

$$ Ax = b $$

where $A \in \mathbf{R}^{m \times n}$, $x \in \mathbf{R}^n$, and $b \in \mathbf{R}^m$, solve the following minimization problem: 

$$\argmin_{x} ||b - Ax||_2^{2}$$

It is important to note that $m>n$.  If $m<n$, the minimization problem loses meaning. $m>n$ implies more equations (size of $b$) than unknowns (size of $x$).  If we had more unknowns than equations ($m<n$) there is an infinite solution set. 

Perhaps best driven home via the simplest sample of linear regression. In this figure, blue points are datapoints. Red indicates the LS errors.  Recall that fitting any line on a 2d plane requires only the definition of a slope and a y-intcpt, which is why $n= 2$ unknowns is from. 
<figure align="center">
  <img src="/assets/images/meaningless_LS.jpg" width="600">
</figure>

Note on practicality: in fact, typically $m >> n$ in engineering. If you are trying to say, solve for the unknown of your GPS location ($n \in \mathbf{R}^4$), you can have thousands of GPS satellite measurements within a minute ($m \in \mathbf{R}^{1000}$).

## Solution: 
At face value, the solution to the least-squares problem is

$$x = (A^TA)^{-1}A^Tb$$

Where $(A^TA)^{-1}A^T$ should look familiar as the left-pseudoinverse of $A$.  **This solution is best committed to memory**.  

A few notes
- We see again that if $m<n$, $A^TA$ would not be full rank, and hence we cannot take $(A^TA)^{-1}$; thus further solidifying the meaninglessness of LS with $m<n$
- Although the pseudoinverse can be arrived from very simple alg manipulation, why it works as a solution to the minimazation problem is not evident and merits a proof. 
- for the curious, the right-pseudoinverse also exists for the dual of the Least-Squares problem: the **Least-Norm problem** (which seeks to minimize magnitude $x^Tx$ for the infinitely possible solns $x$.)  perhaps one day this far less common problem finds its way into these notes. 
  
Solution Derivation: 

$$
\begin{align*}
&\argmin_{x} ||Ax - b||^2_2\\
\Rightarrow & \argmin_{x} (Ax - b)^T(Ax - b) \\
\Rightarrow & \argmin_{x} (x^TA^TAx - x^TA^Tb - b^TAx + b^Tb)
\end{align*}
$$


# Flavors

## WLS: Weighted LS

## IRLS: Iteratively Reweighted LS

## NLS: Nonlinear LS