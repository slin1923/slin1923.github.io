---
layout: default
title: Linear System Theory
---


<font size="5">Index</font>
- [Linear System Theory](#linear-system-theory)
  - [Definition of Linearity](#definition-of-linearity)
  - [Linear System Definition](#linear-system-definition)

# Linear System Theory

## Definition of Linearity
A function is linear if 

$$\forall ~ \alpha_1, \alpha_2 \in \mathbb{R} , \forall ~ x_1, x_2 \in \mathbb{R}^n$$

$$f(\alpha_1x_1 + \alpha_2x_2) = \alpha_1 f(x_1) + \alpha_2 f(x_2) $$

This is called the principle of superposition.  It is relatively straightforward and no elaboration is needed.  

A quick gotcha: the general equation of a "line" is NOT linear.  

$$f(x) = mx + b$$

Without explicitly proving this, note that the $b$ term is where linearity breaks down.  This just goes to show that linearity is a rather strong property and can be deceiving.  

In practice, almost no real systems are linear, however all of them are linearizeable.  

## Linear System Definition

