---
date created: 2025-01-12T15:56:32-05:00
date modified: 2025-01-12T17:59:49-05:00
---

# AE_544_LecNote01__Particle_Kinematics__Ch01

Kinematics is to use vectors and matrices to describe positions, velocities, and accelerations of
particles and rigid bodies, as viewed from various reference frames.
The key points here are:
- Vector
- Frame
- Coordinate system

*Particle Kinematics* means the physical dimensions and properties are not concerned.

## Particle Position Description

In any give frame, two things are important: magnitude (quantity) and unit.

A coordinate system is defined by two items. First, a coordinate system origin O must be established to specify its position in space. Second, the orien- tation of the coordinate system must be chosen.

Three perpendicular (or orthogonal) right-hand unit vectors are traditionally used to denote unit displacement directions along the orthogonal axes.
The basis triad is $\left\{ \ehat{1}, \ehat{2}, \ehat{3} \right\}$.

![[fig-1-1__Cartesian_frame.png|300]]

More generally, think of a reference frame as a rigid body. Although the Earth is a rigid body, there is an infinite set of coordinate systems that could be embedded in the Earth-fixed reference frame. For the present, we will usually associate only one coordinate system with a reference frame (rigid body).

$$
\bm{r} = x \ehat{1} + y \ehat{2} + z \ehat{3}
\tag{1.1}
$$

$$
^\mathcal{E} \bm{r} = \prescript{\mathcal{E}}{}{\pmatrix{x \\ y \\ z}}
\tag{1.2}
$$

The vector notation is abstract, which doesn't depend on any coordinate system. For vectors $\bm{r}$ and $\bm{p}$ given in the same frame, vector operations can be performed, such as 
$$
\bm{q} = \bm{r} + \bm{p}
$$
which is more useful for theoretical or analytical derivations.

When resolving them to coordinates for numerical calculations, a coordinate system (let's say $EE) must be specified first, then we have
$$
\prescript{\color{blue}\mathcal{E}}{}{\pmatrix{q_{1} \\ q_{2} \\ q_{3}}}
= 
\prescript{\color{blue}\mathcal{E}}{}{\pmatrix{r_{1} \\ r_{2} \\ r_{3}}}
+ 
\prescript{\color{blue}\mathcal{E}}{}{\pmatrix{p_{1} \\ p_{2} \\ p_{3}}}
\tag{correct}
$$


> [!danger] Operating coordinates in different coordinate systems is a common mistake in calculation and coding.
> $$
> \prescript{\color{red}\mathcal{E}}{}{\pmatrix{q_{1} \\ q_{2} \\ q_{3}}}
> = 
> \prescript{\color{red}\mathcal{E}}{}{\pmatrix{r_{1} \\ r_{2} \\ r_{3}}}
> + 
> \prescript{\color{red}\mathcal{B}}{}{\pmatrix{p_{1} \\ p_{2} \\ p_{3}}}
> \tag{{\color{red}WRONG!}}
> $$

Coordinate transformation and matrix operation are naturally induced to solve the above problem, to unify all the vectors in the same coordinate system.



For many situations the Cartesian coordinate system is the most intuitive and straightforward one. 
But for many other times, using different coordinate systems can make the problem easy. 

>[!hint] This is also one motivation that Lagrange mechanics introduces *generalized coordinates* and accommodate constraints. We will discuss this later.






A cylindrical coordinate system $\mathcal{C}$ is shown below:

![[fig-1-2__cylindrical_frame.png|300]]

The basis triad of $\mathcal{C}$ is $\left\{ \chat{d}, \chat{\theta}, \chat{3} \right\}$:
- $\chat{d}$: tracks the heading of the projection of the $\bm{r}$ vector in the plane
- $\chat{\theta}$: always normal to $\chat{d}$
- $\chat{3}$: normal to the plane of $\chat{d}$ and $\chat{\theta}$.

Two unit orientation vectors of the cylindrical coordinate system are varying as seen from $\mathcal{N}$.

The position vector and coordinates in $\mathcal{C}$ are
$$
\begin{aligned}
\bm{r} &= d \chat{d} + z \chat{3} \\
^{\mathcal{C}}\bm{r} &= \prescript{\mathcal{C}}{}{\pmatrix{d \\ 0 \\ z}}
\end{aligned}
\tag{1.3}
$$

For a large number of problems having rotational symmetry of force fields or constraint surfaces, cylindrical coordinates would be an attractive choice.
The second entry of the cylindrical coordinate system column vector in Eq. (1.3) will always be zero. <u>Any particle position vector expressed in a cylindrical coordinate system</u>[^why-zero-2nd-entry] will never have a component along the $\chat{\theta}$ direction. 

[^why-zero-2nd-entry]: It is tricky here because only when a vector $\bm{r}$ is expressed in a $\mathcal{C}$ defined by itself, then it has no second entry. If $\mathcal{C}$ is used to describe another vector $\bm{a}$, $^{\mathcal{C}}\bm{a}$ will have a nonzero second entry in general case.

$$
\begin{alignat}{3}
\hat{c}_d &= & \cos\theta \, \ehat{1} &+ \sin\theta \, \ehat{2} \\
\hat{c}_\theta &= & -\sin\theta \, \ehat{1} &+ \cos\theta \, \ehat{2}
\end{alignat}
\tag{1.4}
$$

>[!question] Do we must define a Cartesian coordinate system first before a Cylindrical Coordinate system?
> Both yes and no.
> ![[fig-1-2__cylindrical_frame.png|300]]
> 
> For no: Seemingly in Fig. 1.2 that we need $\{ \ehat{1}, \ehat{2}, \ehat{3} \}$ to define $\left\{ \chat{d}, \chat{\theta}, \chat{3} \right\}$.
> But in fact, we can directly define $\mathcal{C}$ using $\bm{r}$ by picking an arbitrary $\chat{d}$-$\chat{\theta}$ plane. Then, this $\mathcal{C}$ can be used to describe other vectors.
> 
> For yes: Without a Cartesian system, we cannot specify the $\theta$ angle. 
> Even in the above rationale, a Cartesian system is implied when using $\mathcal{C}$ to describe other vectors.





![[fig-1-3__spherical_frame.png|300]]