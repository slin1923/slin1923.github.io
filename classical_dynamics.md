---
layout: default
title: Classical Rotational Mechanics
---
<font size="5">Index</font>
- [Frames of Reference](#frames-of-reference)
- [Rotational Kinematics](#rotational-kinematics)
  - [Active vs Passive Rotations](#active-vs-passive-rotations)
    - [Euler Angles](#euler-angles)
    - [Rotation Matrices](#rotation-matrices)
    - [Angle-Axis Vectors](#angle-axis-vectors)
    - [Quaternions](#quaternions)
  - [Active vs Passive Rotations](#active-vs-passive-rotations-1)
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

In this figure of a satellite orbiting earth, there are two FORs: one centered on earth and the other centered and moving with the satellite (denoted $ECI$ and $SAT$ respectively).  A stray asteroid is also in orbit, and its position $\vec{r}_a$ can be expressed EITHER in $^{ECI}\vec{r}_a$ or $^{SAT}\vec{r}_a$.  However, each of these vectors can be expressed in, for instance, cartesian, polar, or spherical coordinate systems in their respective FOR.  

# Rotational Kinematics

There is a fantastic resource from various faculty/alumni of the UC Berkeley Mechanical Engineering Department that covers everything and more of what I am going to hastily summarize about rotations: https://rotations.berkeley.edu/site-information/.  Additionally Arman Golroudbari also offers a strong resoursce: https://armanasq.github.io/tag/attitude/ 

Although "kinematics/dynamics" is the study of how/why things move, rotational motion and attitude is far more complex and intersting than translational motion. Scope is narrowed to rotation only. 

We start with ways to represent attitude.   In the same way that we are able to say an object "translated" by $a$ units in $\hat{x}$, $b$ units in $\hat{y}$, and $c$ units in $\hat{z}$, these are ways to express a rotated orientation in order of increasing usefulness. *all frames of reference are implied to be orthonormal cartesian*. 

## Active vs Passive Rotations

Before covering the various attitude representations, it is important to semantically establish what an Active vs a Passive rotation is.  
- Active rotations rotate the rigid body about a fixed coordinate system
- Passive rotations rotate the coordinate system and keep the rigid body fixed. 

It is super important to define which of these 2 systems you are working with.  In general, you will see that active vs passive rotations will determine whether you are using
- Positive or negative for Euler Angles ($[\phi, \theta, \psi]$ or $[-\phi, -\theta, -\psi]$)
- Tranpose or original of rotation matrix ($R$ or $R^T$)
- The conjugate or the original of your quaternion ($a + bi + cj + dk$ or $a - bi -cj - dk$).  

### Euler Angles

Euler Angles are the most intuitive way to describe rotation.  They are fantastic for human readability or UI purposes (the colloquial usage of "Yaw", "Pitch", and "Roll" are Euler Angles), but **under the hood it is almost never a good idea to use euler angles**. 

Euler angles essentially say we can express any object attitude as a series of rotations about 3 orthoganol axes from its initial orientation.  This seems sensible; 3 numbers to describe an orientation in 3D is minimal and efficient, but there are many complications and pitfalls to this approach. An Euler coordinate usually looks something like $[\phi, \theta, \psi]^T$, where each value represents an angle-rotation about an axis.  But many questions of conventions are begged of this. Below we define the many different conventions for this simple 3-value coordinate system. 

**Intrinsic vs Extrinsic Euler Angles**

1. Intrinsic Euler Angles represent rotations about the body FOR.  This convention is represented by $X-Y'-Z''$. Where the $'$ and $''$ makes clear that you are rotating about a **derived** FOR. 
2. Extrinsic EAs are the opposite and represent rotations about a fixed inertial FOR regardless of the current attitude of the rigid body. This convention looks more like $X-Y-Z$ where $'$s are not necessary.  

The conversion between intrinsic and extrinsic rotations is a simple matter of order reversal.  

$$\begin{bmatrix} \phi \\ \theta \\ \psi \end{bmatrix}_{X - Y' - Z''} = \begin{bmatrix} \psi \\ \theta \\ \phi \end{bmatrix}_{Z - Y - X}$$

This conversion has deceptively nontrivial intuition.  Realize that an intrinsic ACTIVE/PASSIVE rotation is the NOT the same as an extrinsic PASSIVE/ACTIVE rotation. Instead, a rigorous proof is needed, thanks to robit on mathstackexchange: https://math.stackexchange.com/questions/1137745/proof-of-the-extrinsic-to-intrinsic-rotation-transform 

**Proper Euler vs Tait-Bryan Angles**

Next, 

**Non-commutativity**

**Singularities**

### Rotation Matrices



### Angle-Axis Vectors

### Quaternions

## Active vs Passive Rotations

# Coriolis Theorem

## Gyroscopic Forces

# Inertia Tensors

# Lagrangian Mechanics

## Lagrange Multiplier

## Holonomic Constraints

# Hamiltonian Mechanics
