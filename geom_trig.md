---
layout: default
title: Geometry
---
<font size="5">Index</font>
- [Trigonometry](#trigonometry)
  - [Triangles](#triangles)
    - [Law of Cosines](#law-of-cosines)
    - [Law of Sines](#law-of-sines)
  - [sin, cos, tan, csc, sec, cot](#sin-cos-tan-csc-sec-cot)
  - [sinh, cosh, tanh](#sinh-cosh-tanh)
- [3D World](#3d-world)
  - [Coordinate Systems](#coordinate-systems)
    - [Cartesian](#cartesian)
    - [Polar](#polar)
    - [Spherical](#spherical)
  - [Operations](#operations)
    - [Dot Products](#dot-products)
    - [Cross Products](#cross-products)
    - [Outer Products](#outer-products)
  - [Vectors and Planes](#vectors-and-planes)
    - [Equation of plane](#equation-of-plane)
    - [Distances cheatsheet](#distances-cheatsheet)
- [Conic Sections](#conic-sections)
    - [General Form](#general-form)
    - [Ellipse/Ellipsoid](#ellipseellipsoid)
    - [Parabola/Paraboloid](#parabolaparaboloid)
    - [Hyperbola/Hyperboloid](#hyperbolahyperboloid)
- [Hypergeometries](#hypergeometries)

# Trigonometry

Probably the most basic concepts covered on this website just fyi. 

## Triangles
The following two laws apply for **ANY** triangle with side lengths and associated opposite angles arbitrarily defined like so. 

<figure align="center">
  <img src="/assets/images/triangle_SA_def.png" width="400">
  <figcaption>Perpendicular bisectors and circumcenter for reference </figcaption>
</figure>


### Law of Cosines

$$ c^2 = a^2 + b^2 - 2ab\cos(C) $$

A few quick thoughts and intuitions: 
- this law reinforces that SAS ($a, C, b$) fully defines a triangle (a rigid angled object is defined). 
- This law is an extension of the Pythagorean theorem but for non-right-triangles. Without a full derivation, quick sanity checkes can be made with $C = 0 \rightarrow c = a-b$ and $C = \pi \rightarrow c^2 = a^2 + b^2$. 

### Law of Sines

$$ \frac{a}{\sin(A)} = \frac{b}{\sin(B)} = \frac{c}{\sin(C)} $$

A few quick intuitions. 
- Will not derive, but should be quick to convince yourself that this circular equality comes from the perpendicular bisectors of any triangle (dotted lines in figure)
- pro tip: given SAS ($a, C, b$), law of cosines gives the remaining side $c$ and law of sines can give the remaining angles $B, A$. 

## sin, cos, tan, csc, sec, cot

I will assume strong familiarity with the definitions for these operators and how they are related to each other.  Keep in mind, these are all related to the unit circle. Here I only present rapid-fire properties and plots that escape my memory. No derivations.

**Plots**

<figure align="center">
  <img src="/assets/images/trig_functions.png" width="700">
  <figcaption>All 6 classic trig functions plotted over $x \in [-2\pi, 2\pi]$ </figcaption>
</figure>

Notes: 
- There is technically no limit to the domain on these functions, but they are all $2\pi$ periodic so any input can and should be wrapped to $x \in [0, 2\pi]$. 
- Vertical lines are discontinuities and should be thought of as asymptotes rather than part of the function (unfortunate byprod of matlab plotting). 
- Only $\sin$ and $\cos$ have a confined range of $[-1,1]$.  

**Pythagorean Identities**

$$
\begin{aligned}
\sin^2\theta + \cos^2\theta &= 1 \\
1 + \tan^2\theta &= \sec^2\theta \\
1 + \cot^2\theta &= \csc^2\theta
\end{aligned}
$$

**Angle-Arithmetic Identities**

$$
\begin{aligned}
\sin(\alpha \pm \beta) &= \sin\alpha\cos\beta \pm \cos\alpha\sin\beta \\
\cos(\alpha \pm \beta) &= \cos\alpha\cos\beta \mp \sin\alpha\sin\beta \\
\tan(\alpha \pm \beta) &= \frac{\tan\alpha \pm \tan\beta}{1 \mp \tan\alpha\tan\beta}
\end{aligned}
$$

**Double Angle Identities**

Here for reference, but sorta redundant when angle-arithmetic identities are already presented. 

$$
\begin{aligned}
\sin(2\theta) &= 2\sin\theta\cos\theta \\
\cos(2\theta) &= \cos^2\theta-\sin^2\theta \\
\cos(2\theta) &= 2\cos^2\theta-1 \\
\cos(2\theta) &= 1-2\sin^2\theta \\
\tan(2\theta) &= \frac{2\tan\theta}{1-\tan^2\theta}
\end{aligned}
$$

**Power Reduction Identities**

$$
\begin{aligned}
\sin^2\theta &= \frac{1-\cos(2\theta)}{2} \\
\cos^2\theta &= \frac{1+\cos(2\theta)}{2} \\
\tan^2\theta &= \frac{1-\cos(2\theta)}{1+\cos(2\theta)}
\end{aligned}
$$

## sinh, cosh, tanh

Hyperbolic trig is an entirely different beast. I'm willing to believe most people either forget, or are entirely unaware, that these exist.  So we start basic this time. 

# 3D World

## Coordinate Systems

### Cartesian

### Polar

### Spherical

## Operations

### Dot Products

### Cross Products

### Outer Products

## Vectors and Planes

### Equation of plane

### Distances cheatsheet

# Conic Sections

### General Form

### Ellipse/Ellipsoid

### Parabola/Paraboloid

### Hyperbola/Hyperboloid

# Hypergeometries