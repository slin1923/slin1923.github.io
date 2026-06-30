---
layout: default
title: Classical Dynamics
---
<font size="5">Index</font>
- [Frames of Reference](#frames-of-reference)
  - [Rotational Kinematics](#rotational-kinematics)
    - [Euler Angles](#euler-angles)
    - [Rotation Matrices](#rotation-matrices)
    - [Quaternions](#quaternions)
- [Coriolis Theorem](#coriolis-theorem)
  - [Gyroscopic Forces](#gyroscopic-forces)
- [Inertia Tensors](#inertia-tensors)
- [Lagrangian Mechanics](#lagrangian-mechanics)
  - [Lagrange Multiplier](#lagrange-multiplier)
  - [Holonomic Constraints](#holonomic-constraints)
- [Hamiltonian Mechanics](#hamiltonian-mechanics)

# Frames of Reference

Colloquially, frames of reference simply denote different "perspectives". Frames of reference (cartesian representatoin) differ from one another in their origin and set of basis vectors. Classic aerospace frames include
- Body fixed frame
- Inertial frame
- Wind frame

It is important to distinguish the difference between a frame of reference and a coordinate system: coordinate systems are different ways to represent objects in the same frame of reference.

<figure align="center">
  <img src="/assets/images/FOR-vs-CS.png" width="600">
</figure>

In this figure of a satellite orbiting earth, there are two FORs: one centered on earth and the other centered and moving with the satellite (denoted $ECI$ and $SAT$ respectively).  A stray asteroid is also in orbit, and its position $\vec{r}_a$ can be expressed EITHER in $^{ECI}\vec{r}_a$ or $^{SAT}\vec{r}_a$.  However, each of these vectors can be expressed in, for instanct, cartesian, polar, or spherical coordinate systems in their respective FOR.  

## Rotational Kinematics

Generally, translational motion, regardless of frame of reference, is trivial, because the cartesian coordinate system with which we are used to is well-suited for this already.  

Rotational motion is more complex.  For now we do not consider the dynamics of the rotation.  In the same way that we are able to say an object "translated" by $a$ units in $\hat{x}$, $b$ units in $\hat{y}$, and $c$ units in $\hat{z}$, these are ways to express a rotated orientation in order of increasing usefulness.

### Euler Angles

Unfortunately, the most intuitive way to describe rotational motion that is a natural extension of how we express translational motion is also **easily the worst**. 

Euler angles essentially say we can express any object attitude as a series of rotations about 3 orthoganol axes from its initial orientation.  This seems sensible; 3 numbers to describe an orientation in 3D is efficient, but there are a few key pitifalls to this approach. 

**Intrinsic vs Extrinsic Euler Angles**

**Non-commutativity**

**Singularities**

### Rotation Matrices

### Quaternions

# Coriolis Theorem

## Gyroscopic Forces

# Inertia Tensors

# Lagrangian Mechanics

## Lagrange Multiplier

## Holonomic Constraints

# Hamiltonian Mechanics
