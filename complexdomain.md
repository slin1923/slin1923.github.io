---
layout: default
title: Complex Domain
---
<font size="5">Index</font>
- [Complex Numbers](#complex-numbers)
  - [Euler's Equation](#eulers-equation)
  - [Useful Identities](#useful-identities)
- [Transforms](#transforms)
  - [Laplace Transform](#laplace-transform)
  - [Fourier Transform](#fourier-transform)
  - [Z-transform](#z-transform)

# Complex Numbers
We learn in high school complex numbers are a simple mathematical definition where $j = \sqrt{-1}$.  This seemingly innocuous number has a hidden rotational property to it.  

$$ j = j, \quad j^2 = -1, \quad j^3 = -j, \quad j^4 = 1, \quad j^5 = j$$

Realize that when plotted on a complex plane, the act of multiplying a complex number by $j$ becomes a $90 \degree$ CC rotation. This is an insanely useful property that is leveraged heavily in electrical and controls engineering. 

<figure align="center">
  <img src="/assets/images/j_rotation.png" width="400">
  <figcaption>showing how j can be seen as a rotation operator in complex plane</figcaption>
</figure>

## Euler's Equation
Largely considered the most beautiful equation in math, the Euler Equation is as follows

$$ $$

## Useful Identities

# Transforms

## Laplace Transform

The essence of a Laplace transform lies in how it captures both natural exponentials and frequencies of a system.  The Laplace transform is the cornerstone of dynamical systems and control theory where transients are involved.  It converts a function in the time domain to the complex domain and vice versa through its inverse. 

This is the Laplace Transform $\mathcal{L} \| f(t) \rightarrow F(s)$.  

$$ \mathcal{L}([f(t)])  = \int_0^\infty f(t) e^{-st} dt = F(s)$$

$$ \mathcal{L}^{-1}([F(s)])  = \frac{1}{2\pi}\int_{\sigma -j\omega}^{\sigma + j\omega} F(s) e^{st} ds$$

## Fourier Transform

## Z-transform