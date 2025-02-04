---
date created: 2025-01-12T16:04:10-05:00
date modified: 2025-02-04T00:30:07-05:00
---
# AE_544_LecNote02\__Newtonian_Mechanics__Ch02

![[README#Disclaimers]]

## Newton’s Laws

**Newton's First law**\
Unless acted upon by a force, a particle will maintain a straight line motion with constant inertial velocity.

> [!info] This actually express a belief that there is an ideal and isolated inertial frame.

**Newton's Second law**\
Let the vector $\bm{F}$ be the sum of all forces acting on
a particle having a mass $m$ with the inertial position vector $\bm{r}$. Assume that $\mathcal{N}$
is an inertial reference frame, then
$$
\bm{F} = \ddtN (m \dot{\bm{r}})
\tag{2.1}
$$
*If the mass $m$ is constant*, then this result simplifies to the well known result
$$
\bm{F} = m \ddot{\bm{r}}
\tag{2.2}
$$

> [!info] Note that all derivatives taken in Newton’s second law must be inertial derivatives.

> [!info] Without correctly formulated kinematics, the dynamical system description will be incorrect from the start. *The textbook authors* mention that a large fraction of errors made in practice have their origin in kinematics errors formulating $\ddot{\bm{r}}$ and similar vector derivatives.

**Newton's Third law**\
If mass $m_1$ is exerting a force $\bm{F}_{21}$ on mass $m_2$, then the force $\bm{F}_{12}$ experienced by $m_1$ due to interaction with $m_2$ will be
$$
\bm{F}_{12} = - \bm{F}_{21}
\tag{2.3}
$$

> [!warning] Textbook convention for Free-Body Diagram (FBD)
> The FBD should show all forces and moments acting on the system. We exclude from our FBDs acceleration vectors and so-called inertia forces that are subsets of the $m \ddot{\bm{r}}$ terms in Eq. (2.2) that may arise in rotating coordinate systems.
> (*TL;DR*: Only inertial and real forces/moments; no fictitious ones.)


**Newton’s Law of Universal Gravitation**\
Let the vector $\bm{r}_{12} = \bm{r}_2 - \bm{r}_1$ describe the position of mass $m_2$ relative to mass $m_1$ as shown in Fig. 2.2. Then the mutually attractive gravitational force between the objects will be
$$
\bm{F}_{12} = - \bm{F}_{21} = \frac{G m_1 m_2}{|\bm{r}_{12}|^2} \cdot \frac{\bm{r}_{12}}{|\bm{r}_{12}|}
\tag{2.4}
$$
where $G \approx 6.6732 \times 10^{-11} \,{\rm m^3/(s^2\cdot kg)}$ is the universal gravity constant.


## Example 2.4 Planar pendulum

![[fig-2-6_2d_pendulum.png|300]]

A rotating frame $\Ecal$: $\{\eht{r}, \eht{\theta}\}$

Position vector $\bm{r} = L \eht{r}$

Inertial acceleration $\ddot{\bm{r}} = -L\dot{\theta}^2 \eht{r} + L \ddot{\theta} \eht{\theta}$
> [!note]- Kinematics derivation
> $$
> \begin{align}
> \ddot{\bm{r}} 
> &= \ddt \left( \dot{L} \eht{r} + L \ddt{\eht{r}} \right) \\
> &= \ddt \left( \dot{L} \eht{r} + L (\dot{\theta} \eht{3}) \times \eht{r} \right) \\
> &= \ddt \left( \dot{L} \eht{r} + L \dot{\theta} \eht{\theta}\right) \\
> &= \left( \ddot{L} \eht{r} + \dot{L} \dot{\theta} \eht{\theta} \right) + \left( \dot{L}\dot{\theta}\eht{\theta} + L\ddot{\theta}\eht{\theta} + L \dot{\theta} (-\dot{\theta}\eht{r}) \right) \\
> &= \left( \cancelto{0}{\ddot{L}} \eht{r} + \cancelto{0}{\dot{L}} \dot{\theta} \eht{\theta} \right) + \left( \cancelto{0}{\dot{L}}\dot{\theta}\eht{\theta} + L\ddot{\theta}\eht{\theta} + L \dot{\theta} (-\dot{\theta}\eht{r}) \right) \tag{Constant length $L$}\\
> &= -L\dot{\theta}^2 \eht{r} + L \ddot{\theta} \eht{\theta}
> \end{align}
> $$

FBD gives:
$$
\begin{aligned}
-mL\dot{\theta}^2 &= -F_L + mg \cos \theta \\
mL\ddot{\theta} &= -mg \sin \theta
\end{aligned}
$$

The tension force magnitude $F_L = mL\dot{\theta}^2 +  mg \cos \theta$

The nonlinear differential equations of motion of the spherical pendulum mass $m$ is 
$$
\ddot{\theta} = \frac{-g \sin \theta}{L}
$$

## A system of particles


![[fig-2-8_particle_system.png|300]]

- A system of $N$ particles, a finite number.
- Each has a constant mass $m_i$.
- Don't need to be rigid.

Using Newton's second law, the force acting on $m_i$ can be broken down into two subsets of forces as
$$
\bm{F}_i = m_i \ddot{\bm{R}}_i = \bm{F}_{iE} + \sum_{j=1}^N \bm{F}_{ij}
\tag{2.39 and 2.40}
$$
where $\bm{F}_{iE}$ is the **external forces**, and $\bm{F}_{ij}$ is the **internal force** due to the $j$th masses.

The total force vector $\bm{F}$ acting on the entire system of these $N$ particles is given as
$$
\bm{F} = \sum_{i=1}^{N} \bm{F}_i = \sum_{i=1}^{N} \bm{F}_{iE}
\tag{2.41}
$$

The total mass $M$ is 
$$
M = \sum_{i=1}^{N} m_i
\tag{2.42}
$$

The center of mass position vector $\bm{R}_c$ is expressed in terms of the individual inertial mass position vectors $\bm{R}_i$ as
$$
\bm{R}_c = \frac{1}{M} \sum_{i=1}^{N} m_i \bm{R}_i
\tag{2.46}
$$

> [!info] Definition of the center of mass
> The system center of mass position vector $\bm{R}_c$ is defined such that
> $$
> \sum_{i=1}^{N} m_i \, \bm{r}_i = \sum_{i=1}^{N} m_i \, (\bm{R}_i - \bm{R}_c) = \bm{0}
> \tag{2.43}
> $$
> 
> $$
> M \bm{R}_c = \sum_{i=1}^{N} m_i \bm{R}_i
> \tag{2.45}
> $$

> [!question]- Why the center of mass is defined in this way, as a mass-weighted ($m$-weighted) position? Why not a mass-squared-weighted ($m^2$-weighted) position (just an arbitrary statement)?
> 
> - The net external force acting on the object produces a translational motion of the center of mass. 
> - The net external torque about the center of mass produces a rotational motion around the center of mass.
> 
> This allows us to describe the system's translational motion without worrying about the complexities of rotational motion.
> 
> By choosing the center of mass as the point where all the mass is concentrated, we can analyze the translational motion (linear acceleration) of the object separately from its rotational motion.
> 

**Superparticle theorem**: The dynamics of the mass center of the system of $N$ particles under the influence of the total external force vector $F$ is the same as the dynamics of the superparticle $M$.
$$
M \ddot{\bm{R}}_c = \sum_{i=1}^{N} m_i \ddot{\bm{R}}_i = \sum_{i=1}^{N} \bm{F}_i = \bm{F}
\tag{2.45}
$$
Think of the Earth-Moon system in the solar system as an example.


### Kinetic Energy

The total kinetic energy of a system of N constant mass particles mi can therefore be written as
$$
\begin{align}
T &= \frac{1}{2} \sum_{i=1}^{N} \left( m_i \dot{\bm{R}}_i \cdot \dot{\bm{R}}_i \right)
\tag{2.49} \\
%
&= \frac{1}{2} \sum_{i=1}^{N} \left( m_i (\dot{\bm{R}}_c+\dot{\bm{r}_i}) \cdot (\dot{\bm{R}}_c+\dot{\bm{r}_i})   \tag{Use $\dot{\bm{R}_i}=\dot{\bm{R}}_c+\dot{\bm{r}_i}$} \right) \\
%
&= \frac{1}{2} \sum_{i=1}^{N} \left( m_i (\dot{\bm{R}}_c \cdot \dot{\bm{R}}_c + 2 \dot{\bm{R}}_c \cdot \dot{\bm{r}_i} + \dot{\bm{r}_i} \cdot \dot{\bm{r}_i})   \tag{Factor out $\dot{\bm{R}_c}$}  \right) \\
%
&= \frac{1}{2} \sum_{i=1}^{N} \left( m_i \dot{\bm{R}}_c \cdot \dot{\bm{R}}_c \right) + \sum_{i=1}^{N} \left( m_i \cdot \dot{\bm{R}}_c \cdot \dot\bmr_i \right) + \frac{1}{2} \sum_{i=1}^{N} \left( m_i \dot{\bm{r}}_i \cdot \dot{\bm{r}}_i \right)  \\
&= \frac{1}{2} \left( \sum_{i=1}^{N} m_i \right) \dot{\bm{R}}_c \cdot \dot{\bm{R}}_c + \dot{\bm{R}}_c \cdot \left( \sum_{i=1}^{N} m_i \dot\bmr_i \right) + \frac{1}{2} \sum_{i=1}^{N} \left( m_i \dot{\bm{r}}_i \cdot \dot{\bm{r}}_i \right)  \\
&= \frac{1}{2} \left( \sum_{i=1}^{N} m_i \right) \dot{\bm{R}}_c \cdot \dot{\bm{R}}_c + \dot{\bm{R}}_c \cdot \left( \sum_{i=1}^{N} \ddt (m_i \bmr_i) \right) + \frac{1}{2} \sum_{i=1}^{N} \left( m_i \dot{\bm{r}}_i \cdot \dot{\bm{r}}_i \right) \\
&= \frac{1}{2} \left( \sum_{i=1}^{N} m_i \right) \dot{\bm{R}}_c \cdot \dot{\bm{R}}_c + \dot{\bm{R}}_c \cdot \ddt \left( \sum_{i=1}^{N} (m_i \bmr_i) \right) + \frac{1}{2} \sum_{i=1}^{N} \left( m_i \dot{\bm{r}}_i \cdot \dot{\bm{r}}_i \right) \\
&= \frac{1}{2} \left( \sum_{i=1}^{N} m_i \right) \dot{\bm{R}}_c \cdot \dot{\bm{R}}_c + \dot{\bm{R}}_c \cdot \ddt \ccancelto[green]{\bm{0}}{\left( \sum_{i=1}^{N} (m_i \bmr_i) \right)} + \frac{1}{2} \sum_{i=1}^{N} \left( m_i \dot{\bm{r}}_i \cdot \dot{\bm{r}}_i \right) \\
\tag{2.50} \\
\end{align}
$$

Finally, we have the simplest definition of kinetic energy, which clearly consists of two parts:
$$
T = \textcolor{blue}{ \frac{1}{2} M \dot{\bm{R}}_c \cdot \dot{\bm{R}}_c } + \textcolor{red}{ \frac{1}{2} \sum_{i=1}^{N} m_i \dot{\bm{r}}_i \cdot \dot{\bm{r}}_i }
\tag{2.51}
$$
- <mark style="color:#0000ffff">The first term contains the system translational kinetic energy.</mark>
- <mark style="color:#ff0000ff">The second contains the system rotation and deformation kinetic energy.</mark>

The **kinetic energy rate** $\dot{T}$ is:
$$
\begin{align}
\frac{dT}{dt} &= \textcolor{blue}{ M \ddot{\bm{R}}_c } \cdot \dot{\bm{R}}_c + \sum_{i=1}^{N} m_i \textcolor{red}{ \ddot{\bm{r}}_i } \cdot \dot{\bm{r}}_i  \tag{2.52} \\
%
\frac{dT}{dt} &= \textcolor{blue}{ \bm{F} } \cdot \dot{\bm{R}}_c + \sum_{i=1}^{N} m_i \textcolor{red}{ \ddot{\bm{R}}_i } \cdot \dot{\bm{r}}_i \textcolor{red}{ - } \sum_{i=1}^{N} m_i \textcolor{red}{ \ddot{\bm{R}}_c } \cdot \dot{\bm{r}}_i   \tag{2.53} \\
%
&= \bm{F} \cdot \dot{\bm{R}}_c + \sum_{i=1}^{N} \textcolor{green}{ m_i \ddot{\bm{R}}_i } \cdot \dot{\bm{r}}_i - \ddot{\bm{R}}_c \cdot \cancelto{\bm{0}}{ \left( \sum_{i=1}^{N} m_i \dot{\bm{r}}_i \right) }  \\
%
&= \bm{F} \cdot \dot{\bm{R}}_c + \sum_{i=1}^{N} \textcolor{green}{ \bm{F}_i } \cdot \dot{\bm{r}}_i  \tag{2.54} 
\end{align}
$$

Now we try to *simplify the second term under certain assumptions*.
If there are only **conservative forces $\bm{F}_i$** are acting on $m_i$ , which can be written as the gradient of a potential function $V_i(\bmr_i)$:
$$
\bmF_i = - \nabla V_i(\bmr_i) = - \frac{\partial V_i}{\partial \bmr_i}
\tag{2.55}
$$

Defining the **total conservative potential function $V$** as
$$
V (\bmr_1, \bmr_2, \cdots, \bmr_N) = \sum_{i=1}^N V_i (\bmr_i) \,,
$$
and using the relationship
$$
{\rm d} V_i(\bmr_i(t), t)  = \frac{\partial V_i}{\partial \bmr_i} \cdot {\rm d}{\bmr}_i + \cancelto{0}{\frac{\partial V_i}{\partial t}} {\rm d}t\,,  \tag{Total derivative, move ${\rm d}t$ then}
$$
$$
\ddt V_i(\bmr_i(t), t) = \frac{\partial V_i}{\partial \bmr_i} \cdot \dot{\bmr}_i + \cancelto{0}{\frac{\partial V_i}{\partial t}} ,   \tag{*Explicitly* independent of $t$ }
$$
then we have:
$$
\ddt V = \sum_{i=1}^N \ddt {V}_i = \sum_{i=1}^N \frac{\partial V_i}{\partial \bmr_i} \cdot \dot{\bmr}_i = - \sum_{i=1}^N \bmF_i \cdot \dot{\bmr}_i
\tag{2.56}
$$

>[!question]- Is this derivative correct? <br> The order of summation and derivative operators is switched.
> The derivative and summation are interchangeable if the summation involves terms that are differentiable with respect to $t$.
> - The summation is finite (or absolutely convergent if infinite).
> - Each term $V_i(\bmr_i, t)$​ is differentiable with respect to $t$.


Now Eq. (2.54) can be written as
$$
\ddt T + \ddt V = \bmF \cdot \dot{\bmR}_c
$$

- If the total force $\bmF = \bm{0}$, the total energy $E=T+V$ is conserved.

- If the total force $\bmF = -\nabla V_c(\bmR_c)$ is also a conservative force due to a potential function $V_c(\bmR)_c$, the total system energy $E=T+V+V_c$ is conserved. 

In other cases of general forces exerted, we need to integrate the kinetic energy rate $\dot{{T}}$ to find the work, which is:
$$
\begin{align}
T(t_2) - T(t_1) &= \int_{\bm{R}_c(t_1)}^{\bm{R}_c(t_2)} \bm{F} \cdot \textcolor{blue}{ d\bm{R}_c } + \sum_{i=1}^N \int_{\bm{r}(t_1)}^{\bm{r}(t_2)} \bm{F}_i \cdot \textcolor{green}{ d\bm{r}_i }    \tag{2.60} \\
&= \int_{t_1}^{t_2} \bm{F} \cdot \textcolor{blue}{ \dot{\bm{R}}_c \cdot \dt } + \sum_{i=1}^N \int_{t_1}^{t_2} \bm{F}_i \cdot \textcolor{green}{ \dot{\bm{r}}_i \cdot \dt } \tag{2.59}
\end{align}
$$
where the first integral is translational work done by the total force $\bmF$, and the second integral is the rotation and deformation work on each particle.


### Linear Momentum

The total linear momentum $\bmp$ of the system is defined as the sum
$$
\bm{p} = \sum_{i=1}^N \bm{p}_i = \sum_{i=1}^N \left( m_i \dot{\bm{R}}_i \right)
\tag{2.61}
$$

We can write the total linear momentum expression in terms of the total system mass $M$ and the center of mass inertial velocity vector $\bmR_c$
$$
\bm{p} = \sum_{i=1}^N \left( m_i \dot{\bm{R}}_i \right) = \sum_{i=1}^N m_i (\dot{\bm{R}}_c + \dot{\bmr}_i) = \sum_{i=1}^N m_i \dot{\bm{R}}_c + \cancelto{\bm{0}}{\sum_{i=1}^N m_i \dot{\bmr}_i} = M \dot{\bmR}_c
\tag{2.62}
$$

>[!note] 
>Notice that the center of mass is **defined** in a way such that this simplification is feasible.

The the time rate of change of the linear momentum of a particle system is equal to the total external force acting on the system:
$$
\dot{\bmp} = \sum_{i=1}^N (m_i \ddot{\bmR}_i) = \sum_{i=1}^N \bmF_i = \bmF
$$

**Law of conservation of linear momentum**: If no external force $\bmF$ is present, then the total system linear momentum vector $\bmp$ will be constant.



### Angular Momentum

The total system angular momentum vector $\bmH$ about the point $P$ (an arbitrary point) is given as the sum of all the single particle angular momentum vectors about this point:
$$
\bm{H}_P = \sum_{i=1}^N \bm{\sigma}_i \times m_i \dot{\bm{\sigma}}_i
\tag{2.66}
$$
where $\bm{\sigma}_i = \bm{R}_i - \bm{R}_P$ is the relative position vector, with $\bmR_i$ and $\bmR_p$ standing for position vectors.

The rate of $\bmH_P$ is
$$
\begin{align}
\dot{\bm{H}}_P 
&= \sum_{i=1}^N \dot{\bm{\sigma}}_i \times m_i \dot{\bm{\sigma}}_i + \sum_{i=1}^N \bm{\sigma}_i \times m_i \ddot{\bm{\sigma}}_i    \tag{2.67} \\
&= \cancelto{\bm{0}}{\sum_{i=1}^N \dot{\bm{\sigma}}_i \times m_i \dot{\bm{\sigma}}_i} + \sum_{i=1}^N \bm{\sigma}_i \times m_i (\ddot{\bm{R}}_i - \ddot{\bm{R}}_P)    \tag{cross-product} \\
&= \sum_{i=1}^N \bm{\sigma}_i \times m_i \ddot{\bm{R}}_i - \left( \sum_{i=1}^N \bm{\sigma}_i m_i \right) \times \ddot{\bm{R}}_P    \tag{2.68} \\
&= \sum_{i=1}^N \bm{\sigma}_i \times \bmF_i - \left( \sum_{i=1}^N \bm{R}_i m_i - \sum_{i=1}^N m_i \bm{R}_P \right) \times \ddot{\bm{R}}_P   \\
&= \sum_{i=1}^N \bm{\sigma}_i \times \bmF_i - M(\bmR_c - \bmR_P) \times \ddot{\bm{R}}_P   \tag{center of mass} \\
&= \textcolor{blue}{ \bmL_P } + \textcolor{red}{ M \ddot{\bmR}_P \times (\bmR_c - \bmR_P) }  \tag{2.71}
\end{align}
$$
- <mark style="color:#0000ffff">The first term is defined as total external torque $\bmL_P$ applied to the system.</mark>
- <mark style="color:#ff0000ff">The second term is the change due to the acceleration of the reference point $\bmR_P$ and the relative position.</mark>

If no external torque $\bmL_P$ is acting on the system of particles, then the total angular momentum vector $\bmH_P$ is constant. 

>[!note]
>Notice that $P$ is an arbitrary point in the derivation. But if we choose the center of mass as $P$, Eq. (2.71) can be simplified further.
>
>So, again, the center of mass is **defined** in a way such that this simplification is feasible.



## Reduce to a Single Particle System

Just set $N=1$ for the above discussions.

## Extend to a Continuous System

For most case, summations can be safely and carefully converted to integrals.

$$
{\rm d}\bm{F} = \ddot{\bm{R}} \, {\rm d}m
$$

$$
\bm{F} = \int_B {\rm d}\bm{F}
$$

$$
M \, \bm{R}_C = \int_B \bm{R} \, {\rm d}m
$$

$$
T = \frac{1}{2} M \dot{\bm{R}}_c \cdot \dot{\bm{R}}_c + \frac{1}{2} \int_B \dot{\bm{r}} \cdot \dot{\bm{r}} \, dm
$$

$$
\frac{dT}{dt} = M \ddot{\bm{R}}_c \cdot \dot{\bm{R}}_c + \int_B \dot{\bm{r}} \cdot \ddot{\bm{r}} \, dm
$$

$$
\bm{H}_P = \int_B \bm{\sigma} \times \dot{\bm{\sigma}} \, dm
$$

$$
\dot{\bm{H}}_P = \bm{L}_P + M \ddot{\bm{R}}_P \times \left( \bm{R}_c - \bm{R}_P \right)
$$


## Textbook problem 2.10
![[fig-p2-10_rolling_cylinder_with_offset_mass.png|600]]

## Textbook problem 2.11
![[fig-p2-11_rolling_vall_inside_sphere.png|600]]

## Rocket Problem


## Homework 01

Due on Feb 02. 
Check Canvas for detailed guidance on submissions.

Use office hours if you need.

Emails will be replied as timely as I could.