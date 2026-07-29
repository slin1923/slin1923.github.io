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
  - [arcsin, arccos, arctan, arcsec, arccsc, arccot](#arcsin-arccos-arctan-arcsec-arccsc-arccot)
  - [Hyperbolic Trig](#hyperbolic-trig)
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
  - [Ellipse ( $0\<e\<1$ )](#ellipse--0e1-)
  - [Parabola ($e=1$)](#parabola-e1)
  - [Hyperbola ($e\>1$)](#hyperbola-e1)
- [Quadratic Hypergeometries](#quadratic-hypergeometries)

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
- Will not derive, but convince yourself that this circular equality comes from the perpendicular bisectors as a stepping stone (dotted lines in figure)
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

## arcsin, arccos, arctan, arcsec, arccsc, arccot


## Hyperbolic Trig

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

The most intuitive way to understand conic sections is they are the 2-D functions that arise from slicing a **circular** cone with a plane.  

<figure align="center">
  <img src="/assets/images/conic-sections.png" width="500">
  <figcaption>conic slices</figcaption>
</figure>

First let's motivate why we care about how we slice we cones - where do we see conic sections in life (just to name a few)?  

- circles (eccentricity 0 conics) are everywhere
- Orbital Mechanics: All orbits in a 2-body problem are a conic section *see section on orbital mechanics*
- Parabolic Optics: Mirrors, antennas, how a flashlight beam strikes a surface. 
- Cooling Towers and nozzles: use hyperbolic channel geometries.  
- Catenary Curve: The curve formed by a naturally hanging uniform rope and the St. Louis arch are closely related to the hyperbola. 
- Optimization: conic sections make convex sets! (and convexity makes optimization easy)

In general, you will see that the form of conic sections are fundamental, quadratic, and likely to appear as a byproduct in a lot of mathematical modeling.  Thus, a strong intuition is useful.  It's also kind of fun to do an arch-easter-egg hunt.  

## General Form

First, we must define what a **circular** cone is.  

$$x^2 + y^2 = z^2\tan^2(\theta)$$

where $\theta$ is the half-angle subtended by the cone.  

Now, we must define the plane which slices the cone. There is no need to explicitly write out the equation of the plane because only one property of the plane really matters in order to determine which conic section is formed: its angle with the z-axis $\beta$.  Note that by definition of an angle between a plane and a vector, $\beta \in [0, \pi/2]$. 

<figure align="center">
  <img src="/assets/images/conic_slice_planes.png" width="500">
  <figcaption>conic slice planes visualized</figcaption>
</figure>

- For $\beta = \pi/2$ : circle
- For $\beta \in (\pi/2, \theta)$ : ellipse
- For $\beta = \theta$ : parabola
- For $\beta \in (\theta, 0]$ : hyperbola

Finding the intersection between a cone and a general plane of varying $\beta$ is tedious algbebra and yields the general form of conic sections.  

$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

Classically, we like to analyze conics as origin-centered ($D, E = 0$) and un-rotated ($B = 0$).  Yielding the more comforting **general form of a regular conic**

$$\boxed{Ax^2 + Cy^2 + F = 0}$$

And its sister **polar general form**

$$\boxed{r = \frac{p}{1+e\cos(\nu)}}$$

The transformation between polar and cartesian general forms is arduous geometry, so just trust this form works.  The polar form introduces to us the following recurring concepts in all conic sections : $(p, e, \nu)$.  From these, we can define a full set of useful concepts for conics.

- $p$: The semilatus rectum
- $e$: The eccentricity - qualitatively speaking, a measure of oblateness
- $\nu$: The true anomaly - the angle between a location on the conic section and the **focal point, NOT the geometric centroid** 
- $f$: The focal point(s) - locations of geometric importance
- $a$: The semimajor axis
- $b$: The semiminor axis
- directrix: a line of geometric importance

## Ellipse ( $0<e<1$ )

The general cartesian form of an origin-centered ellipse (2D) is 

$$ \frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 $$

And its polar form

$$ r = \frac{p}{1 + e\cos(\nu)} \quad | \quad 0<e<1 $$

<figure align="center">
  <img src="/assets/images/ellipse.png" width="700">
  <figcaption>ellipse and important intrinsic relations</figcaption>
</figure>

Notes 
- $(x, y)$ and $(r, \nu)$ are mere coordinates and $(a,b)$ and $(p, e)$ are the intrinsice properties of the ellipse in cartesian and polar coordinates respectively. 
- Given $(a,b) \Leftrightarrow (p,e)$  
- a circle is just a special ellipse where $a = b$ or $e = 0$. 
- $e$ describes how "oblate" the ellipse is and $p$ defines the scale. 
- At any point on the ellipse, the sum of the distances to the foci are preserved (pairs of pink lines in figure)
- A any point on a single half of the ellipse, the **ratio** of distances to the nearest focus and the nearest directrix (lavendar and cyan lines respectively) is preserved. 

## Parabola ($e=1$)

The general form of an origin-vertexed parabola (2D) is 

$$y^2 = 4ax$$

And its polar form 

$$ r = \frac{p}{1 + \cos(\nu)}$$

<figure align="center">
  <img src="/assets/images/parabola.png" width="500">
  <figcaption>parabola and important intrinsic relations</figcaption>
</figure>

Notes: 
- A parabola is another special case between an ellipse and an hyperbola where $e =1 \Rightarrow \frac{b^2}{a^2} \rightarrow \infty$. 
- To intuitively understand the above point, you can imagine an ellipse where $a$ is infinitely large relative to $b$ and you start to believe how this is an ellipse that can never close up on the other end!  (for the clever who momentarily imagined an ellipse collapsed to a line ($b = 0$), recall that in this case $a = 0$ necessarily lest the object no longer obey the properties of an ellipse. hence this case is degenerate).
- Parabolas, like circles, lose a dimension of intrinsic properties, and can be fully defined by just $a$ or $p$.  
- Any point on a parabola is equidistant from its focus and the directrix (cyan lines in figure)

## Hyperbola ($e>1$)

Finally, the general forms of an origin-centered hyperbola (2D) is

$$ \frac{x^2}{a^2} - \frac{y^2}{b^2} = 1 \quad ; \quad xy = c^2$$

And its polar form

$$ r = \frac{p}{1 + e\cos(\nu)} \quad | \quad e>1 $$

<figure align="center">
  <img src="/assets/images/hyperbola.png" width="700">
  <figcaption>hyperbola and important intrinsic relations</figcaption>
</figure>

Notes 
- *points 1 and 2 under the ellipse section apply here too*
- $e$ describes how "oblate" the imaginary central rectangle is (orange dotted in figure) and $p$ defines the scale. 
- A any point on a half-hyperbola, the **ratio** of distances to the nearest focus and the nearest directrix (lavendar and cyan lines respectively) is preserved. 

As a parting note on conic sections, here is visual on how a conic section evolves as $e: 0\rightarrow\infty$. 

<figure align="center">
  <img src="/assets/images/eccentricities.png" width="500">
  <figcaption>how conic sections evolve with e</figcaption>
</figure>

# Quadratic Hypergeometries