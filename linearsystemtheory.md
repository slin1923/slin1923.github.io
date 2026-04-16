---
layout: default
title: Linear System Theory
---


<font size="5">Index</font>
- [Definition of Linearity](#definition-of-linearity)
- [Linear Systems](#linear-systems)
  - [Definition](#definition)
  - [Linearization from Nonlinear](#linearization-from-nonlinear)
    - [Jacobian Matrix](#jacobian-matrix)
  - [Transfer Functions](#transfer-functions)
    - [Poles and Zeros](#poles-and-zeros)
    - [Root Locus](#root-locus)
    - [Bode-Nyquist Frequency Response](#bode-nyquist-frequency-response)
  - [Properties](#properties)
    - [Controllability and Observability](#controllability-and-observability)

# Definition of Linearity
A function is linear if 

$$\forall ~ \alpha_1, \alpha_2 \in \mathbb{R} , \forall ~ x_1, x_2 \in \mathbb{R}^n$$

$$f(\alpha_1x_1 + \alpha_2x_2) = \alpha_1 f(x_1) + \alpha_2 f(x_2) $$

This is called the principle of superposition.  It is relatively straightforward and no elaboration is needed.  

A quick gotcha: the general equation of a "line" is NOT linear.  

$$f(x) = mx + b$$

Without explicitly proving this, note that the $b$ term is where linearity breaks down.  This just goes to show that linearity is a rather strong property and can be deceiving.  

In practice, almost no real systems are linear, however all of them are linearizeable.  

# Linear Systems

## Definition

## Linearization from Nonlinear

### Jacobian Matrix

## Transfer Functions

### Poles and Zeros

### Root Locus 

### Bode-Nyquist Frequency Response

## Properties

### Controllability and Observability

