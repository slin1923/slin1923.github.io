---
layout: default
title: Linear System Theory
---

<font size="5">Index</font>
- [Limits](#limits)
  - [Fundamental Theorem of Calculus](#fundamental-theorem-of-calculus)
- [Derivatives](#derivatives)
- [Integrals](#integrals)
  - [Leibniz Integral Rule](#leibniz-integral-rule)
- [The Beauty of $e$](#the-beauty-of-e)
  - [Definition of $e$](#definition-of-e)
    - [Infinite Series Definition](#infinite-series-definition)
    - [Calculus-Based Definition](#calculus-based-definition)
    - [What this means](#what-this-means)
  - [Exponential Growth and Decay](#exponential-growth-and-decay)
  - [Logistic Growth and Decay](#logistic-growth-and-decay)

# Limits

## Fundamental Theorem of Calculus

# Derivatives

# Integrals

## Leibniz Integral Rule

The Leibniz Integral rule governs how to take the derivative of a definite integral wrt $x$ when the the integral itself is wrt some other variable $y$ and, but the both the integrand $f(x,y)$ and the bounds of the integral $a(x)$ and $b(x)$ vary in $x$. It is an advanced calculus concept stated below. 

$$ \frac{d}{dx} \left( \int^{b(x)}_{a(x)} f(x,y) dy \right)$$

$$ = f(x, b(x)) \cdot \frac{d}{dx} b(x) - f(x, a(x)) \cdot \frac{d}{dx}a(x) + \int^{b(x)}_{a(x)} \frac{\partial}{\partial x} f(x,y) dy$$

The 3 terms in this rule are intuitively explained as follows.  
- Term 1 covers how the integral changes with changes to the upper integral bound (notice that it is + because increasing values of b(x) extend the range of the integral)
- Term 2 covers how the integral changes with changes to the lower integral bound (notice that it is - because decreasing values of a(x) reduce the range of the integral)
- The last term should be familiar from the fundamental theorem of calculus.  

# The Beauty of $e$

## Definition of $e$

### Infinite Series Definition

### Calculus-Based Definition

### What this means

## Exponential Growth and Decay

## Logistic Growth and Decay