---
title: "Appendix B. Classical Mechanics"
---
(ch-b-classmech)=

# Appendix B. Classical Mechanics

(sec-classmech-1)=

## Introduction

In this Appendix we summarize some aspects of classical mechanics that will be relevant for our course in quantum mechanics. We concentrate on the Lagrangian and Hamiltonian formulation of classical mechanics.

(sec-classmech-2)=

## Lagrangians, Dissipation, and Entropy

In this Appendix we consider exclusively classical systems that can be described by a Lagrangian. This means that we neglect friction and other dissipative processes that cause an increase in entropy. Dissipation is always present in macroscopic systems, so its neglect is an approximation that is more or less good depending on circumstances.

The concept of entropy applies when making a statistical description of a system, which is often necessary when the number of degrees of freedom is large. Entropy provides a measure of our ignorance of the state of the system, that is, of the values of the dynamical variables that describe the system.

In some macroscopic systems it is a good approximation to concentrate on just a few degrees of freedom that we are interested in, and to neglect interactions with a large number of other degrees of freedom that we do not care about. For example, in the motion of a planet around the sun we may wish to describe the position of the center of mass of the planet in detail while ignoring its rotations as well as the internal stresses inside the solid body of the planet, the bulk motions of fluids in its oceans and atmospheres, etc. The latter are macroscopic degrees of freedom that are in turn coupled to microscopic ones, the motions of the individual atoms and molecules that make up the planet. There is a chain of couplings leading from macroscopic degrees of freedom down to microscopic ones, and a corresponding transport of energy from large motions down to small ones, ultimately resulting in the production of heat.

If the couplings at any stage are small it may be possible to neglect them, to obtain a closed system with few degrees of freedom. This would certainly simplify the problem and may be valid over short periods of time. But over longer periods dissipation will be important and cannot be ignored. For example, ancient dissipative processes inside the body of the moon have caused it to settle into a state in which its rotation is synchronized with its revolution, so that we see only one face of it from the earth. And the tides in the earth's oceans lead to dissipation of energy in the earth-moon system, causing the day to become longer while the moon recedes from the earth. (The energy required to move the moon away from the earth comes from the kinetic energy of the earth's rotation. Conservation of angular momentum requires that the moon recede in this process.) The earth-moon system is heading toward a state in which the length of the day and the length of the month are equal.

Similar concepts apply to a block sliding across a table. Friction causes the kinetic energy of the block to be converted into heat in the block and the table, that is, into the energy of motion of the individual atoms and molecules of the block and table. If friction is small, we may neglect it and treat the block as if its center of mass or center of mass and orientation were isolated degrees of freedom, not interacting with any other.

If we do wish to take friction into account in the motion of a block sliding across a table, we may do so while limiting ourselves to a small number of degrees of freedom by using a phenomenological force law, for example, one that says that the frictional force is $-k|\vvec|^\alpha \vvec$, where $k>0$ and $\alpha$ are constants and where $\vvec$ is the velocity of the block. Such force laws may have some theoretical justification or may be just fits to experimental data. They amount to taking into account the large number of internal degrees of freedom of the block and table in an average way. It is straightforward to write down Newton's laws $\Fvec=m\avec$, including such frictional forces, to obtain differential equations for the motion of the few degrees of freedom we are interested in. Such frictional force laws, however, preclude a Lagrangian formulation of the system.

In this course we will be especially interested in microscopic systems with a small number of degrees of freedom, whose dynamics we will follow in detail, that is, without using statistics. Such systems are sometimes isolated from their environment, so it is not hard to write down equations of motion for their internal dynamics. An example is an atom or molecule in a low-density gas between collisions. Since such systems only have a small number of degrees of freedom, there is no question of any coupling to a large number of “internal” degrees of freedom, as in the case of the block. If the system is not isolated, however, then it does interact with “external” degrees of freedom, that is with external fields (gravitational, electromagnetic, etc).

In such cases we will assume that the external fields are simply given as a function of space and time. In reality, external fields are never known precisely, for example, a magnetic field produced by a current in some coils has fluctuations due to the finite temperature of the source of the current and of the coils themselves. In this course, we shall ignore such effects.

In summary, we shall ignore dissipative effects in this course, so that a Lagrangian description is possible. Systems that can be described by a Lagrangian include classical systems of point particles, fluids, elastic media and fields, both in nonrelativistic and relativistic mechanics. We begin with the nonrelativistic mechanics of systems of point particles.

(sec-classmech-3)=

## Constrained Systems, Configuration Space, and Generalized Coordinates

In a system with $N$ particles, the positions of all the particles relative to an inertial frame are specified by $3N$ coordinates, $(x_1,y_1,z_1, \ldots, x_N,y_N,z_N)$, or $(\xvec_1,\ldots,\xvec_N)$ for short. Sometimes the positions of the particles are subject to *constraints*, for example, if a particle is sliding on the surface of a sphere of radius $a$, its position coordinates are subject to the constraint $x^2+y^2+z^2=a^2$. Or if the particles make up a rigid body, then the distances between any two particles is constant,

:::{math}
:label: eq-classmech-1
|\xvec_i - \xvec_j| = const,
:::

for all $i,j=1,\ldots,N$. Constraints appear both in classical mechanics and in quantum mechanics, for example, many small molecules are approximately rigid bodies.

Constrained systems are idealizations of systems with a larger number of degrees of freedom, in which strong confining forces cause the particles to move on or near the constraint surface. For example, a particle sliding on the surface of a sphere of radius $a$ can be thought of as a particle that feels a strong restoring force if it moves away from the surface $r=a$ in three-dimensional space.

Interesting issues arise when exploring such models in detail to see how the simple picture of constrained dynamics emerges from a more realistic model with strong constraining forces. For example, one finds that if the initial position is on the constraint surface and the initial velocity is tangent to it, then the position remains on the constraint surface at later times, to a good approximation when the constraining forces are strong. When the initial position is not on the constraint surface or the initial velocity is not tangent to it, then there are high-frequency oscillations about the constraint surface and the dynamics along the constraint surface are modified. This is an interesting chapter in adiabatic theory that we shall not pursue here, although we will touch on adiabatic problems in the course (see {ref}`ch-adiab`).

In the case of constraints, the positions of the $N$ particles are described by some number $n<3N$ of coordinates, call them $q_1, \ldots, q_n$. For example, in the case of the particle sliding on the sphere we have $n=2$ and we can take $(q_1,q_2)=(\theta,\phi)$, the usual spherical coordinates on the sphere. In the case of the rigid body with one point fixed we have $n=3$ and we can take $(q_1,q_2,q_3)=(\alpha,\beta,\gamma)$, the Euler angles of a rotation that maps a standard orientation of the rigid body into the actual orientation. See {ref}`sec-classrot-13` for the definition of Euler angles. In the case of a rigid body whose center of mass is free to move (for example, in a model of a planet), we have $n=6$ and coordinates $(q_1,\ldots,q_6)=(\alpha,\beta,\gamma,X,Y,Z)$, where $(X,Y,Z)$ are the coordinates of the center of mass. In general, the positions $(\xvec_1,\ldots,\xvec_N)$ of the particles are functions of the $q$'s,

:::{math}
:label: eq-classmech-2
\xvec_i = \xvec_i(q_1,\ldots,q_n,t), \qquad i=1,\ldots,N.
:::

If the constraints are time-dependent, then these functions depend on time as indicated. For example, in the case of a particle sliding on a sphere of radius $a$ we have

:::{math}
:label: eq-classmech-3
\begin{aligned}
x &=a\sin\theta\cos\phi, \\
y &=a\sin\theta\sin\phi, \\
z &=a\cos\theta. \\

\end{aligned}
:::

If there are no constraints, then we have $n=3N$ and we can take $(q_1, \ldots, q_{3N}) = (x_1,y_1,z_1,\ldots, x_N,y_N,z_N)$, that is, we can let the $q$'s be the rectangular coordinates of the particles. We may choose not to do this, however, for example, in the case of a single particle moving in three-dimensional space we may wish to use spherical coordinates and choose $(q_1,q_2,q_3) = (r,\theta,\phi)$.

In general (with or without constraints), the $q$'s are coordinates on *configuration space*, an abstract space in which a single point represents the positions of all the particles of the system. The number of the $q$'s, which is the dimension of configuration space, is called the *number of degrees of freedom*. In the case of a single particle moving in three-dimensional space, configuration space is the same as physical space, but in general configuration space is best regarded as an abstract space. Here are two examples of configuration spaces. The configuration space of a system of $N$ unconstrained particles is $\Reals^{3N}$, while the configuration space of a rigid body with one point fixed is the rotation group manifold $SO(3)$ (see {ref}`ch-classrot`).

The coordinates $q_i$, $i=1,\ldots,n$, are called *generalized coordinates*. The word “generalized” simply means that the coordinates need not be rectangular coordinates. For constrained systems such as the particle sliding on a sphere, rectangular coordinates are not an option and all coordinates are “generalized.”

(sec-classmech-4)=

## Variational Principles in Optics

It has been known for a long time that certain problems in optics can be expressed in terms of a variational principle. Consider, for example, the laws of reflection from a mirror, which state that the angle of incidence is equal to the angle of reflection. See {ref}`fig-classmech-1`, in which a light ray leaves point $A$, reflects off the mirror at point $R$, and then reaches point $B$. The actual path taken by the light ray on going from $A$ to $B$, path $ARB$ in the figure, is the one that minimizes the total distance of travel. For example, the dotted path $AR'B$ is longer. But the shortest path is also the one for which the angle of incidence is equal to the angle of reflection ($\angle ARC = \angle\, CRB$ in the figure).

:::{figure} images/classmech-fig01.png
:label: fig-classmech-1
:width: 80%

The actual path taken by a light ray when reflecting from a mirror, $ARB$, is the one that minimizes the total distance traveled.
:::

:::{figure} images/classmech-fig02.png
:label: fig-classmech-2
:width: 80%

The path taken by the light ray on passing from one medium with index of refraction $n_1$ to another with index of refraction $n_2$ minimizes the quantity $\ell_1 n_1 + \ell_2 n_2$.
:::


Similarly, the laws of refraction (Snell's law) can be cast into a variational form. See {ref}`fig-classmech-2`, in which there are two media with indices of refraction $n_1$ and $n_2$. In this case it is not the total distance that is minimized, but the distance multiplied by the index of refraction. That is, the actual path, $ARB$ in the figure, is the one that minimizes $\ell_1n_1 + \ell_2n_2$, where $\ell_1$ is the distance from $A$ to a point on the interface, and $\ell_2$ is the distance from that point to $B$. It can be shown that this path is one that satisfies Snell's law,

:::{math}
:label: eq-classmech-4
n_1\sin\theta_1 = n_2 \sin\theta_2.
:::

In both these cases there is a space of paths over which the minimization takes place. In the case of the mirror, the space of paths consists of all paths that connect $A$ to a point on the mirror by a straight line, and then connect that point to $B$ by another straight line. This is a 2-parameter space of paths, because the mirror is a 2-dimensional surface (the parameters are the coordinates on the surface of the mirror). But the space of paths can be enlarged to include arbitrary, curved paths that join $A$ to $B$, staying on one side of the mirror and touching it once, as in {ref}`fig-classmech-3`. The actual path still has the minimum length, because all curved paths between any two points are longer than the straight path between those points. The enlarged path space is infinite-dimensional. Similarly, in the refraction problem illustrated in {ref}`fig-classmech-2`, the space of paths can be enlarged to include curved paths that cross the interface only once.

:::{figure} images/classmech-fig03.png
:label: fig-classmech-3
:width: 80%

The space of paths reflecting from the mirror can be enlarged to include curved paths, and the actual path still minimizes the distance.
:::

A more general situation is one in which the index of refraction is a function of position, $n=n(\xvec)$, for example, when a light ray passes through the earth's atmosphere. In this case it can be shown that the actual path taken by the light ray is one that minimizes the integral,

:::{math}
:label: eq-classmech-5
A[\xvec(s)] = \int n(\xvec)\, ds,
:::

where the path is parameterized by the arc length $s$. This integral is the generalization of the sum $\ell_1n_1 + \ell_2n_2$ used in the refraction example above. In this case the space of paths consists of all paths that join given points $\xvec_0$ and $\xvec_1$. The actual path satisfies the differential equation,

:::{math}
:label: eq-classmech-6
\dod{}{s}\Bigl( n(\xvec) \dod{\xvec}{s}\Bigr) = \del n,
:::

which is the Euler-Lagrange equation (see \secrclassmech-7) for the variational problem defined by {eq}`eq-classmech-5`.

The quantity $A[\xvec(s)]$ in {eq}`eq-classmech-5` is a functional of the path, and it is not obvious why it should be minimized along the actual path. A justification can be given by applying the short wavelength or WKB approximation to Maxwell's equations in a slowly varying medium, but that does not make the form of the functional $A[\xvec(s)]$ intuitive, nor does it explain why nonphysical paths should enter into a physical formulation of the problem. That is, the question arises, if the actual path followed by the light ray minimizes a certain quantity, does nature somehow know about the nonphysical paths in order to reject them? There is no answer purely within classical theory. As discussed in {ref}`ch-pathint`, however, a more satisfactory justification comes from quantum mechanics. Suffice it to say here that in books the functional $A[\xvec(s)]$ is often multiplied by $1/c$, whereupon it becomes the time required for a particle to move along the light ray at the phase velocity $v=c/n$. That is, it becomes a time functional,

:::{math}
:label: eq-classmech-7
T[\xvec(s)] = {1\over c} A[\xvec(s)] = \int {n\over c} \, ds = \int {ds\over v} = \int dt.
:::

Thus, one can say that the actual path minimizes the time, defined in this way. Why the phase velocity should appear here rather than the group velocity (which is the actual velocity at which signals propagate) is however a mystery.

Actually, the physical path does not always minimize the time. More generally it is a critical or stationary point of the time functional, that is, the physical path satisfies

:::{math}
:label: eq-classmech-8
{\delta T \over \delta \xvec(s)} =0.
:::

The first functional derivative of the time functional with respect to the path vanishes on the physical path.

(sec-classmech-5)=

## Critical Points

In elementary calculus, if we wish to find the extrema of a function $f(x_1,\ldots, x_n)$ of several variables, we first find the roots of

:::{math}
:label: eq-classmech-9
\frac{\partial f}{\partial x_i}(x_{01},\ldots,x_{0n}) = 0, \qquad i=1,\ldots,n,
:::

that is, we look for the places where the gradient of $f$ vanishes. These roots $(x_{01},\ldots,x_{0n})$ are called the *critical points* of the function $f$. We can describe a critical point in words by saying small variations about the critical point give rise to only second order variations in the value of the function (the first order variations vanish).

Critical points are candidates for extrema. To find out if one is an extremum and of what type, we may examine the second derivative matrix evaluated at the critical point,

:::{math}
:label: eq-classmech-10
{\partial^2 f \over \partial x_i \partial x_j} (x_{01},\ldots,x_{0n}).
:::

This matrix is real and symmetric, so its eigenvalues are real. If the eigenvalues are all positive, then the critical point is a minimum, that is, small variations about the critical point can only increase the value of the function. In general the minimum is only local, that is, there may be other minima with smaller values of $f$ at some distance away. If all the eigenvalues of the matrix {eq}`eq-classmech-10` are negative, then the critical point is a (generally local) maximum. If some are negative and some are positive, then the critical point is a saddle. And if some eigenvalues are zero, then any test based on second derivatives alone is inconclusive.

Similarly, the condition {eq}`eq-classmech-8` in optics can be stated by saying that the physical path is a critical point (in path space) of the time functional, that is, the functional is stationary on the physical paths.

(sec-classmech-6)=

## Hamilton's Principle

There is also a variational formulation of nondissipative systems in classical mechanics. It says that the functional

:::{math}
:label: eq-classmech-11
A[q(t)] = \int_{t_0}^{t_1} L(q,\dot q,t) \,dt
:::

is stationary on the physical paths, where $L$ is the Lagrangian function. Here $q$ is short for $(q_1,\ldots,q_n)$, the generalized coordinates, and $n$ is the number of degrees of freedom. Equivalently,

:::{math}
:label: eq-classmech-12
{\delta A \over  \delta q_i(t)} =0
:::

on the physical paths, for $i=1,\ldots,n$. This is called *Hamilton's principle*. The quantity $A[q(t)]$ is called the *action* associated with the path $q(t)$. In some cases, the action is actually minimum along the physical path, but in general the physical path is just a critical point of the action functional.

The space of paths that enters into Hamilton's principle is the space of all smooth paths $q(t)$ satisfying

:::{math}
:label: eq-classmech-13
q(t_0) = q_0, \qquad q(t_1) = q_1,
:::

for fixed values of $t_0$, $t_1$, $q_0$ and $q_1$. Here as above $q$ stands for all the generalized coordinates $(q_1, \ldots, q_n)$. The endtimes $t_0$ and $t_1$ are the limits of the integral {eq}`eq-classmech-11`. If $q$ is one-dimensional, paths in this path space may be visualized in the $q$-$t$ plane as in {ref}`fig-classmech-4`.

:::{figure} images/classmech-fig04.png
:label: fig-classmech-4
:width: 80%

A path $q(t)$ satisfying fixed boundary conditions $q(t_0)=q_0$ and $q(t_1)=q_1$. Also shown is a modified path $q(t) + \delta q(t)$, satisfying the same endpoint and endtime conditions.
:::

(sec-classmech-7)=

## The Euler-Lagrange Equations

The functional derivative {eq}`eq-classmech-12` can be computed as follows. Let $q(t)$ be any path in the path space, that is, any path satisfying the boundary conditions. It need not be a physical path, that is, one that satisfies Newton's laws. Let $\delta q(t)$ be a small variation that takes the path $q(t)$ into a nearby path $q(t) + \delta q(t)$, as in {ref}`fig-classmech-4`. The new path is also required to be in the path space, so $\delta q(t_0) = \delta q(t_1) = 0$. The velocity along the original path is $\qdot(t)$ and that along the modified path is $\qdot(t) + \delta \qdot(t)$, where

:::{math}
:label: eq-classmech-14
\delta \qdot(t) = \dod{\delta q(t)}{t}.
:::

Then the variation in the action is

:::{math}
:label: eq-classmech-15
\delta A = A[q(t)+\delta q(t)] - A[q(t)] = \int_{t_0}^{t_1} dt \sum_{i=0}^n \Bigl[ \frac{\partial L}{\partial q_i} \, \delta q_i(t) + \frac{\partial L}{\partial \qdot_i} \, \delta \qdot_i(t)\Bigr],
:::

dropping terms that are second order or higher in $\delta q$. But the second term on the right can be integrated by parts,

:::{math}
:label: eq-classmech-16
\int_{t_0}^{t_1} dt \sum_{i=0}^n \frac{\partial L}{\partial \qdot_i} \, \delta \qdot_i = \sum_{i=0}^n \left.\frac{\partial L}{\partial \qdot_i} \, \delta q_i\right|_{t_0}^{t_1} -\int_{t_0}^{t_1} dt \sum_{i=0}^n \dod{}{t} \Bigl(\frac{\partial L}{\partial \qdot_i}\Bigr) \,\delta q_i(t),
:::

where the first major term on the right vanishes because of the boundary conditions $\delta q(t_0) = \delta q(t_1) = 0$. Altogether, we have

:::{math}
:label: eq-classmech-17
\delta A = \int_{t_0}^{t_1} dt \sum_{i=0}^n \Bigl[ \frac{\partial L}{\partial q_i} - \dod{}{t}\Bigl(\frac{\partial L}{\partial \qdot_i}\Bigr)\Bigr] \delta q_i(t).
:::

Thus by the definition of the functional derivative,

:::{math}
:label: eq-classmech-18
{\delta A \over \delta q_i(t)} = \frac{\partial L}{\partial q_i} - \dod{}{t}\Bigl(\frac{\partial L}{\partial \qdot_i}\Bigr).
:::

This is the quantity which vanishes along the physical paths, so the equations of motion satisfied by the physical paths are

:::{math}
:label: eq-classmech-19
\dod{}{t} \Bigl(\frac{\partial L}{\partial \qdot_i}\Bigr) = \frac{\partial L}{\partial q_i},
:::

for $i=1,\ldots,n$. These are the *Euler-Lagrange equations*.

An ordinary function over some domain may have any number of critical points, from zero to infinity. Similarly, for a given path space, that is, for given values of $t_0$, $t_1$, $q_0$ and $q_1$, the action functional {eq}`eq-classmech-11` may have any number of critical points. That is, for the given endpoints and endtimes, there may be any number of physical paths, from zero to infinity. Many books erroneously state that the physical path is unique for given endpoints and endtimes.

(sec-classmech-8)=

## The Lagrangian, and the Case $L=T-V$

To say that a classical system admits a Lagrangian formulation means that there exists a function $L(q,\qdot,t)$ such that the Euler-Lagrange equations {eq}`eq-classmech-19` are equivalent to Newton's laws. As mentioned, such a formulation exists whenever the system is nondissipative. This is shown by actually finding the Lagrangian function in different cases. We will not go through the proof of equivalence to Newton's laws here, instead we will just quote the Lagrangian function for the cases of greatest interest to us. The actual proof is straightforward for unconstrained systems, but more elaborate in the case of constraints, especially time-dependent ones.

The most important case for this course is that of nonrelativistic systems in which the forces can be obtained from a scalar potential. Let $V(\xvec_1, \ldots, \xvec_N,t)$ be the potential energy of the system, expressed as a function of the positions of the $N$ particles and possibly the time. It is assumed that there is a force on particle $i$ given by

:::{math}
:label: eq-classmech-20
\Fvec_i = -\frac{\partial V(\xvec_1,\ldots,\xvec_N,t)}{\partial \xvec_i}, \qquad i=1,\ldots,N.
:::

In addition, if there are constraints, then there are also forces of constraint acting on the particles. We do not need to take explicit account of the forces of constraint in a Lagrangian formulation, but they must be dealt with when using Newton's laws. We assume that the forces {eq}`eq-classmech-20` and the forces of constraint are the only forces acting on the particles. By using the relations {eq}`eq-classmech-2`, the potential energy can be expressed in terms of the generalized coordinates and possibly the time,

:::{math}
:label: eq-classmech-21
V=V(q_1,\ldots,q_n,t).
:::

Similarly, by differentiating {eq}`eq-classmech-2` with respect to time and using the chain rule, the kinetic energy $T$ can be expressed as a function of the $q$'s, the $\qdot$'s and possibly the time,

:::{math}
:label: eq-classmech-22
T = {1\over2} \sum_{i=1}^N m_i |\dot\xvec_i|^2 = {1\over 2} \sum_{i=1}^N m_i \left| \frac{\partial \xvec_i}{\partial t}+ \sum_{k=1}^n \frac{\partial \xvec_i}{\partial q_k} \qdot_k\right|^2 =T(q,\qdot,t),
:::

where $m_i$ is the mass of particle $i$ and where $n$ is the number of degrees of freedom.

In this case the Lagrangian is the difference between the kinetic and potential energies,

:::{math}
:label: eq-classmech-23
L(q,\qdot,t) = T(q,\qdot,t) - V(q,t).
:::

An important case in practice is that of unconstrained particles interacting by means of electrostatic forces, including “external” electrostatic fields. In this case the potential energy of the $N$ particles is

:::{math}
:label: eq-classmech-24
V(\xvec_1, \ldots, \xvec_N,t) = {1\over 2} \sum_{i \ne j} {Q_iQ_j \over |\xvec_i-\xvec_j|} + \sum_{i=1}^N Q_i \,\Phi_ext(\xvec_i,t),
:::

where $Q_i$ is the charge of particle $i$ and where $\Phi_ext(\xvec,t)$ is the electrostatic potential energy per unit charge due to external fields. The first sum on the right is the electrostatic energy of interaction of the particles among themselves. The sum is taken over all pairs $(i,j)$, omitting the diagonal terms $i=j$ which represent the infinite self-energy of the charged particles. The second term is the external potential, corresponding to an external electric field,

:::{math}
:label: eq-classmech-25
\Evec_ext(\rvec,t) = - \del \Phi_ext(\rvec,t).
:::

Here we use $\rvec$ for an arbitrary field point at which the field may be evaluated.

The external potential may depend on time if the charges producing the external fields are moving. Think, for example, of an atom between the plates of a capacitor to which an AC voltage is applied. In this case the external electric field may be written,

:::{math}
:label: eq-classmech-26
\Evec_ext = E_0 {\hat{\mathbf{z}}} \cos \omega t,
:::

where $E_0$ is the amplitude of the electric field, assumed to be pointing in the $z$-direction, and $\omega$ is the frequency. Then the external potential is

:::{math}
:label: eq-classmech-27
\Phi_ext = -E_0 z \cos\omega t.
:::

The potential {eq}`eq-classmech-24` only takes into account the interactions of the charged particles in the electrostatic approximation, which is valid for nonrelativistic systems of small spatial extent. That is, the equations of motion are equivalent to

:::{math}
:label: eq-classmech-28
m_i {\ddot\xvec_i} = Q_i [\Evec_int(\xvec_1, \ldots, \xvec_N)+\Evec_ext(\xvec_i,t)].
:::

This approximation neglects magnetic effects as well as the effects of retardation and radiation. See {ref}`ch-classemf`{} for further discussion.

(sec-classmech-9)=

## Magnetic Fields

The Lagrangian formulation may also be applied to problems with magnetic fields. The simplest case is one in which the magnetic fields are external, that is, we ignore any magnetic fields arising from the motion of the charged particles of the system itself. We write the external magnetic field in the form

:::{math}
:label: eq-classmech-29
\Bvec_ext(\rvec,t) = \del\cross\Avec_ext(\rvec,t),
:::

where $\Avec_ext$ is the vector potential. As indicated, the external magnetic field is allowed to depend on time. Then the Lagrangian is

:::{math}
:label: eq-classmech-30
L = T-V + \sum_{i=1}^N {Q_i\over c} {\dot\xvec_i} \cdot \Avec_ext(\xvec_i,t).
:::

If $V$ is given by {eq}`eq-classmech-24`, then the Euler-Lagrange equations are equivalent to

:::{math}
:label: eq-classmech-31
m_i {\ddot \xvec}_i = Q_i\Bigl[ \Evec_int(\xvec_1,\ldots,\xvec_N) + \Evec_ext(\xvec_i,t) + {1\over c} {\dot\xvec}\cross \Bvec_ext(\xvec_i,t)\Bigr].
:::

If it is desired to take into account the internal magnetic fields produced by the moving charges of the system itself, this may be done in an approximate way by adding extra terms to obtain the *Darwin Lagrangian*. See the discussion in Landau and Lifshitz or Jackson. The Darwin Lagrangian has more physics in it than the Lagrangian {eq}`eq-classmech-30`, but it still omits the effects of retardation and radiation. If these are important, one must include the infinite degrees of freedom of the electromagnetic field. See the discussion in {ref}`ch-classemf`.

(sec-classmech-10)=

## Advantages of Lagrangian Mechanics

The Lagrangian formulation of mechanics affords several advantages compared to Newton's laws. First, the Lagrangian is a single (scalar) function, which implicitly contains within it all the equations of motion. Thus, if we wish to transform to a new coordinate system, it is much easier to transform the (single, scalar) Lagrangian than the (vector, multicomponent) equations of motion. The Lagrangian formulation is the easiest way to write down the classical equations of motion in curvilinear coordinates.

In addition, if there are constraints, the Lagrangian formulation automatically gives us the correct equations of motion without having to take the forces of constraint into account. This is considerably simpler than working with Newton's laws, where the forces of constraint must be eliminated.

Third, there is a general relationship in Lagrangian mechanics between symmetries and invariants. That is, every symmetry of the system corresponds to a conservation law. This is called *Noether's theorem*.

Finally, the Lagrangian formulation of a classical system leads to the Hamiltonian formulation, which is the point at which we may pass to quantum mechanics.

The main disadvantage of the Lagrangian formulation is that it is unable to account for dissipative effects.

(sec-classmech-11)=

## The Momentum

Let us return to the Lagrangian $L(q,\qdot,t)$, expressed in terms of generalized coordinates. We define the quantity

:::{math}
:label: eq-classmech-32
p_i = \frac{\partial L}{\partial \qdot_i},
:::

which we call the *generalized momentum conjugate to* $q_i$. In terms of $p_i$, the Euler-Lagrange equations {eq}`eq-classmech-19` can be written,

:::{math}
:label: eq-classmech-33
\dod{p_i}{t} = \frac{\partial L}{\partial q_i}.
:::

The physical meaning of the generalized momentum depends on the coordinates used and the nature of the forces.

Consider first Cartesian coordinates, for which we write the momentum conjugate to $\xvec_i$ as $\pvec_i$ (a 3-vector),

:::{math}
:label: eq-classmech-34
\pvec_i = \frac{\partial L}{\partial {\dot\xvec}_i}.
:::

Restricting the Lagrangian {eq}`eq-classmech-30` to a single charged particle interacting with a given (external) electromagnetic field, we find

:::{math}
:label: eq-classmech-35
\pvec= m\dot\xvec + {q\over c} \Avec(\xvec,t).
:::

The first term, $m \dot\xvec$, is the usual definition of the momentum in elementary mechanics. We call this term alone the *kinetic momentum*. In the presence of a nonzero vector potential, however, there is a second term. We call the total momentum of {eq}`eq-classmech-35` the *canonical momentum*. The canonical momentum depends on the choice of gauge for the vector potential, so it is not as physical as the kinetic momentum (its value depends on the gauge convention). For this reason one may prefer formulations based on the kinetic momentum. The canonical momentum, however, is necessary for a Hamiltonian formulation of mechanics in the presence of magnetic fields, and it is the canonical momentum that corresponds to the momentum operator $-i\hbar\del$ in quantum mechanics.

The extra term in the canonical momentum {eq}`eq-classmech-35` is somewhat mysterious in this formulation of particle mechanics, but it acquires an explanation in terms of the momentum of the electromagnetic field when the field degrees of freedom are included in the system. This is especially simple in the case of Coulomb gauge. This point is discussed further in {ref}`ch-classemf`.

In curvilinear coordinates the momentum has other interpretations. For example, consider the case of a particle moving in a potential $V$ in 3-dimensional space, for which the Lagrangian in spherical coordinates is

:::{math}
:label: eq-classmech-36
L={m\over 2}({\dot r}^2 + r^2 {\dot\theta}^2 + r^2\sin^2\theta\, {\dot\phi}^2) - V(r,\theta,\phi).
:::

Then the momentum conjugate to the azimuthal angle $\phi$ is

:::{math}
:label: eq-classmech-37
p_\phi = \frac{\partial L}{\partial {\dot\phi}} = m r^2 \sin^2\theta\, {\dot\phi}={\hat{\mathbf{z}}}\cdot(\xvec\cross\pvec),
:::

which physically is the $z$-component of the angular momentum $\Lvec$, as indicated.

To see how the generalized momentum changes under a change of coordinates, let us temporarily write $q^i$ (with a superscript, that is, a contravariant index) for the coordinates, and let us consider a change of coordinates $q^{\prime\,i} = q^{\prime\,i}(q)$. See Appendix~\tensor\ for a discussion of contravariant and covariant indices in tensor analysis, and how they transform under coordinate transformations. For simplicity we assume the coordinate transformation is time-independent. Then the generalized velocity transforms according to the chain rule,

:::{math}
:label: eq-classmech-38
\qdot^{\prime\,i} = \sum_j \pop{q^{\prime\,i}}{q^j} \, \qdot^j,
:::

which is the transformation law for a contravariant vector. Similarly, the generalized momentum transforms as

:::{math}
:label: eq-classmech-39
p'_i = \sum_j \frac{\partial q^j}{\partial q^{\prime\,i}} \, p_j,
:::

that is, as a covariant vector. For example, in spherical coordinates, the generalized momenta $(p_r,p_\theta,p_\phi)$ are the covariant components of the momentum vector $\pvec$ in spherical coordinates.

Taken together, {eq}`eq-classmech-38` and {eq}`eq-classmech-39` imply that the quantity $\sum_i p_i \, dq^i/dt$, and hence the differential form $\sum_i p_i \, dq^i$, are invariants under general coordinate transformations on configuration space.

(sec-classmech-12)=

## Regular and Irregular Lagrangians

Expanding out the time derivative in the Euler-Lagrange equations {eq}`eq-classmech-19`, we have

:::{math}
:label: eq-classmech-40
\sum_j {\partial^2 L \over \partial \qdot_i \partial \qdot_j} \, {\ddot q}_j = -\sum_j {\partial^2 L \over \partial \qdot_i \partial q_j} \, \qdot_j - {\partial^2 L \over \partial \qdot_i \partial t} + \frac{\partial L}{\partial q_i},
:::

which can be solved for the generalized accelerations ${\ddot q_i}$ if

:::{math}
:label: eq-classmech-41
\det {\partial^2 L \over \partial \qdot_i \partial \qdot_j} \ne 0.
:::

Lagrangians for which {eq}`eq-classmech-41` holds are said to be *regular*. All Lagrangians normally encountered in nonrelativistic particle mechanics are regular, and, in particular, all the nonrelativisitc Lagrangians cited in this Appendix are regular. Irregular Lagrangians do occur, however, in relativistic particle mechanics, and they are common in relativistic field theory, such as in the Lagrangian formulation of the electromagnetic field.

For a regular Lagrangian, we can solve the Euler-Lagrange for the generalized accelerations,

:::{math}
:label: eq-classmech-42
{\ddot q}_i = F_i(q,\qdot,t),
:::

where $F_i$ are some functions. That is, the equations of motion are a system of coupled, second-order differential equations on configuration space. These can be converted into a system of coupled, first-order differential equations by introducing the generalized velocities $v_i$, and writing,

:::{math}
:label: eq-classmech-43
\begin{aligned}
\qdot_i &= v_i, \\
{\dot v}_i &= F_i(q,v,t). \\

\end{aligned}
:::

(sec-classmech-13)=

## Lagrangians for Relativistic Problems

Relativistic mechanics can also be put into Lagrangian form. See Appendix~\tensor\ for our notation for relativistic problems (we follow the notation of Jackson, *Classical Electrodynamics*, 3rd ed).

In a covariant formulation of relativistic mechanics we must not parameterize the particle orbits by time, which is specific to one Lorentz frame. Instead it is desirable to treat the time on the same footing as the three spatial coordinates, and to write $x^\mu(\lambda)$ for the world line of the particle, where $\lambda$ is an arbitrary parameter of the world line. See {ref}`fig-classmech-5`. You might think that proper time $\tau$ would be the natural parameter of the world line, but proper time is linked to the space-time coordinates by the differential relation

:::{math}
:label: eq-classmech-44
g_{\mu\nu}\,dx^\mu dx^\nu = c^2 dt^2 - d\xvec^2 = c^2 d\tau^2,
:::

and it is desirable to use a parameter that is independent of the coordinates.

:::{figure} images/classmech-fig05.png
:label: fig-classmech-5
:width: 80%

The world line $x^\mu(\lambda)$ of a particle, where $\lambda$ is an arbitrary parameter. One spatial dimension is suppressed in the figure.
:::

:::{math}
:label: eq-classmech-45
The action is a functional of the world line, A[x^\mu(\lambda)] = \int L\, d\lambda,  where L is the Lagrangian,
:::

which we take to be a function of $x^\mu$ and $dx^\mu/d\lambda$. We require the equations of motion to be covariant. This is automatic if the action is a Lorentz scalar, which causes the Euler-Lagrange equations to have the same form in all Lorentz frames. This in turn implies that the Lagrangian $L(x^\mu, dx^\mu/d\lambda)$ must be a Lorentz scalar. This is a powerful constraint on the form of the Lagrangian for relativistic problems that determines it almost uniquely in various situations.

We begin with the case of the free particle. The dynamics of the free particle is invariant under space-time displacements, so the Lagrangian cannot depend on $x^\mu$ (it cannot depend on our choice of origin of our Lorentz frame). Thus the Lagrangian can depend only on $dx^\mu/d\lambda$, the world velocity with respect to $\lambda$. The only scalar that can be constructed out of this is

:::{math}
:label: eq-classmech-46
g_{\mu\nu} \dod{x^\mu}{\lambda} \dod{x^\nu}{\lambda} = \dod{x^\mu}{\lambda} \dod{x_\mu}{\lambda} = c^2 \Bigl(\dod{\tau}{\lambda}\Bigr)^2,
:::

so the Lagrangian must be a function of this quantity. We take it to be

:::{math}
:label: eq-classmech-47
L=mc \left(\dod{x^\mu}{\lambda} \dod{x_\mu}{\lambda} \right)^{1/2} = mc^2 \, \dod{\tau}{\lambda},
:::

because this makes the momentum conjugate to $x^\mu$ come out to be the usual 4-momentum $p_\mu$ of a particle [see {eq}`eq-classmech-48`]. Notice that with this Lagrangian, $L\,d\lambda = mc^2 \,d\tau$, so the action $A[x^\mu(\lambda)]$ is $mc^2$ times the elapsed time as measured by a clock attached to the particle.

The momentum conjugate to $x^\mu$ is given by a version of {eq}`eq-classmech-32`,

:::{math}
:label: eq-classmech-48
p_\mu = {\partial L \over \ds \partial \Bigl(\ds {dx^\mu \over \ds d\lambda}\Bigr)} = {mc \over \ds \Bigl( {\ds dx^\nu\over \ds d\lambda} {\ds dx_\nu\over \ds d\lambda}\Bigr)^{1/2}} \, \dod{x_\mu}{\lambda} = m \dod{x_\mu}{\tau},
:::

where the time derivatives of our earlier discussion are reinterpreted as $\lambda$-derivatives, and where we use {eq}`eq-classmech-46`. Our use of the lower index on $p_\mu$ is in accordance with the usual rules for placing indices when we differentiate with respect to something with indices (see {ref}`sec-tensor-6`), and also with the fact that the momentum transforms as a covariant vector [see {eq}`eq-classmech-39`]. We can raise this index with the metric, obtaining,

:::{math}
:label: eq-classmech-49
p^\mu = m \dod{x^\mu}{\tau},
:::

and examine the components. The time component is

:::{math}
:label: eq-classmech-50
p^0 = mc \dod{t}{\tau} = mc\gamma = E/c,
:::

where $\gamma$ is the usual relativistic factor of time dilation,

:::{math}
:label: eq-classmech-51
\gamma = \dod{t}{\tau} = {1 \over \sqrt{1-v^2/c^2}}.
:::

The spatial components give

:::{math}
:label: eq-classmech-52
p^{\mu\to i} = m\dod{x_i}{\tau} = m \dod{t}{\tau} \dod{x_i}{t} = m\gamma v_i=p_i,
:::

where we use the notation explained in {ref}`sec-tensor-20` for the spatial components of a 4-vector. Equations~{eq}`eq-classmech-50` and {eq}`eq-classmech-52` are equivalent to the usual definition of the momentum 4-vector,

:::{math}
:label: eq-classmech-53
p^\mu = \begin{pmatrix} E/c \\ \pvec\\\end{pmatrix},
:::

where $E=mc^2\gamma$ and $\pvec=m\gamma\vvec$.

Since the Lagrangian {eq}`eq-classmech-47` is independent of $x^\mu$, the Euler-Lagrange equations are

:::{math}
:label: eq-classmech-54
\dod{p_\mu}{\lambda} = \frac{\partial L}{\partial x^\mu}=0,
:::

where again we reinterpret time derivatives [see {eq}`eq-classmech-19`] as $\lambda$ derivatives. After raising the index and multiplying by $d\lambda/d\tau$ this becomes

:::{math}
:label: eq-classmech-55
\dod{p^\mu}{\tau} = m{d^2 x^\mu\over d\tau^2} =0.
:::

These are the correct equations of motion for the free particle. The parameter $\lambda$ has disappeared, as it must, since it was arbitrary.

Now suppose our particle has charge $Q$. We wish to incorporate its interaction with an external electromagnetic field, described by the 4-vector potential,

:::{math}
:label: eq-classmech-56
A^\mu = \begin{pmatrix}\Phi \\ \Avec \\\end{pmatrix},
:::

and the field tensor,

:::{math}
:label: eq-classmech-57
\begin{aligned}
F_{\mu\nu} = \partial_\mu A_\nu - \partial_\nu A_\mu = \begin{pmatrix}0 & E_x & E_y & E_z \\ -E_x & 0 & -B_z & B_y \\ -E_y & B_z & 0 & -B_x \\ -E_z & -B_y & B_x & 0 \\\end{pmatrix}.
\end{aligned}

:::

The simplest Lorentz scalar we can construct out of $dx^\mu/d\lambda$ and the tensors describing the electromagnetic field is $A_\mu(x) dx^\mu/d\lambda$. Other choices such as

:::{math}
:label: eq-classmech-58
F_{\mu\nu}\,\dod{x^\mu}{\lambda} \dod{x^\nu}{\lambda}
:::

will not do, since they vanish. Adding a multiple of $A_\mu(x)\,dx^\mu/d\lambda$ to the free particle Lagrangian {eq}`eq-classmech-47` and adjusting the coefficient to get the correct equations of motion, we find the Lagrangian,

:::{math}
:label: eq-classmech-59
L= mc \left(\dod{x^\mu}{\lambda} \dod{x_\mu}{\lambda} \right)^{1/2} + {Q\over c} A_\mu(x) \dod{x^\mu}{\lambda}.
:::

Now the action contains a term,

:::{math}
:label: eq-classmech-60
{Q\over c} \int A_\mu(x) \, dx^\mu,
:::

a relativistic version of an integral related to magnetic flux and gauge transformations (see {ref}`sec-tevolut-7`).

The new Lagrangian {eq}`eq-classmech-59` gives the canonical momentum,

:::{math}
:label: eq-classmech-61
p_\mu = {\partial L \over \ds \partial \Bigl(\ds {dx^\mu \over \ds d\lambda}\Bigr)} = m \dod{x_\mu}{\tau} + {Q\over c} A_\mu(x).
:::

We see again the distinction between the canonical momentum $p_\mu$ (the sum of both terms on the right hand side) and the kinetic momentum (the first term alone). When necessary to distinguish the two momenta, we will write $p_\mu^kin$ for the kinetic momentum. It is the momentum (without distinction) in the case of a free particle. If we write its components as

:::{math}
:label: eq-classmech-62
p^\mu_kin = \begin{pmatrix}E_kin/c \\ \pvec_kin \\\end{pmatrix},
:::

where we have raised the index, then the usual relativistic energy-momentum relation is

:::{math}
:label: eq-classmech-63
E_kin = \sqrt{m^2c^4 + \pvec_kin^2}.
:::

Notice that this $E_kin$ includes the rest mass, so its low velocity limit is $E_kin = mc^2 + \pvec^2/2m$.

Now the Euler-Lagrange equations are

:::{math}
:label: eq-classmech-64
\dod{p_\mu}{\lambda} = m \dod{}{\lambda} \dod{x_\mu}{\tau} + {Q\over c} (\partial_\nu A_\mu) \dod{x^\nu}{\lambda} = \frac{\partial L}{\partial x^\mu} = {Q\over c} (\partial_\mu A_\nu) \dod{x^\nu}{\lambda},
:::

or, after raising $\mu$, using {eq}`eq-classmech-57`, and multiplying by $d\lambda/d\tau$,

:::{math}
:label: eq-classmech-65
m{d^2 x^\mu \over d\tau^2} = {Q\over c} F^\mu{}_\nu \, \dod{x^\nu}{\tau}.
:::

These are the correct covariant equations of motion for a relativistic charged particle in an electromagnetic field. They contain the usual Lorentz force law in their spatial components, and an energy equation in the time component.

(sec-classmech-14)=

## Relativistic Lagrangians in $3+1$-Notation

Sometimes we wish to describe the relativistic dynamics of a particle $3+1$-notation, that is, with respect to the space and time coordinates $\xvec$ and $t$ of a specific Lorentz frame. This does not change the fundamental Lorentz covariance of the theory, but it does destroy manifest Lorentz covariance.

It is easy to refer the particle dynamics to the coordinate time $t$ of a specific Lorentz frame. Since the parameter $\lambda$ of \secrclassmech-13 was arbitrary, we can simply set $\lambda=t$. Then we have

:::{math}
:label: eq-classmech-66
\dod{x^\mu}{\lambda} \dod{x_\mu}{\lambda} = c^2 - \vvec^2 = {c^2 \over \gamma^2},
:::

where $\vvec = d\xvec/dt$. Then the free particle Lagrangian {eq}`eq-classmech-47` can be written,

:::{math}
:label: eq-classmech-67
L = {mc^2 \over \gamma}  = mc^2 \sqrt{1 -{\vvec^2 \over c^2}}.
:::

Using this to compute the momentum conjugate to $\xvec$, we find

:::{math}
:label: eq-classmech-68
\frac{\partial L}{\partial \vvec}= -{m\vvec \over \sqrt{\ds 1- {\ds \vvec^2 \over \ds c^2}}} = - m\gamma\vvec,
:::

with a minus sign compared to the usual definition of the 3-momentum in relativity theory. This is the same minus sign that we get by replacing $\mu$ by $i$ in {eq}`eq-classmech-48`, which leads to $p_{\mu\to i} = -p_i$. It is another manifestation of the notational difficulties caused by our choice of sign of the metric (see {ref}`sec-tensor-20`). To make the momentum agree with the usual definition in a $3+1$-formulation of mechanics we may multiply the Lagrangian by $-1$. This does not affect the equations of motion.

To include the interaction with an electromagnetic field we set $\lambda=t$ in the interaction term,

:::{math}
:label: eq-classmech-69
{Q\over c}A_\mu(x) \dod{x^\mu}{\lambda} = Q\Phi - {Q\over c}\vvec\cdot\Avec,
:::

so that the entire Lagrangian, including the change of sign, is

:::{math}
:label: eq-classmech-70
L = -mc^2 \sqrt{\ds 1 -{\ds \vvec^2 \over \ds c^2}} -Q\Phi + {Q\over c} \vvec\cdot\Avec.
:::

Now the canonical momentum is

:::{math}
:label: eq-classmech-71
\pvec = m\gamma\vvec + {Q\over c}\Avec(\xvec,t),
:::

the relativistic generalization of {eq}`eq-classmech-35`. The canonical momentum is the relativistic version of the kinetic momentum plus the same correction term, $(Q/c)\Avec$, seen in the nonrelativistic formula {eq}`eq-classmech-35`.

It is straightforward to work out the equations of motion that follow from the Lagrangian {eq}`eq-classmech-70`. They are

:::{math}
:label: eq-classmech-72
\dod{}{t}(m\gamma\vvec) = Q\Bigl[\Evec(\xvec,t) + {\vvec\over c}\cross\Bvec(\xvec,t) \Bigr],
:::

which are equivalent to the covariant equations {eq}`eq-classmech-65`. The left-hand side is the relativistic definition of the force (the time rate of change of momentum), and the right-hand side is the Lorentz force.

In the low velocity limit we may expand the square root in the first term of the Lagrangian {eq}`eq-classmech-70`. This gives

:::{math}
:label: eq-classmech-73
L = -mc^2 + {m\vvec^2\over 2} -Q\Phi + {Q\over c}\cdot\Avec.
:::

This agrees with the Lagrangian {eq}`eq-classmech-30`, if we specialize the latter to the case of a single particle and set $V=Q\Phi$. There is also the addition of the constant term $-mc^2$, which does not affect the equations of motion. Although in the nonrelativistic theory we are accustomed to write the Lagrangian as $T-V$ plus a magnetic term, notice that in the relativistic theory the first term $-mc^2/\gamma$ of the Lagrangian {eq}`eq-classmech-70` is not the kinetic energy, which would be $mc^2\gamma$.

(sec-classmech-15)=

## Hamilton's Equations

Let us return to our general discussion of Lagrangian mechanics given in Secs.~\secrclassmech-7--\secrclassmech-12. The condition {eq}`eq-classmech-41` is also the condition that the definition {eq}`eq-classmech-32` of the generalized momentum can be solved for the velocities, that is, that we can express the velocities as functions of the $q$'s, the $p$'s and the time:

:::{math}
:label: eq-classmech-74
\qdot_j = \qdot_j(q,p,t),
:::

where $p$ stands for all the generalized momenta, $(p_1, \ldots, p_n)$. Thus for regular Lagrangians we can introduce the $p$'s as new coordinates, eliminate the $v$'s from {eq}`eq-classmech-43`, and express the equations of motion as a system of first-order differential equations involving the $q$'s and the $p$'s.

The equations of motion can be put into an especially symmetrical form in terms of the *Hamiltonian* function, defined by

:::{math}
:label: eq-classmech-75
H(q,p,t)=\sum_j p_j \qdot_j -L.
:::

The right-hand side of this expression is a function of $(q,\qdot,t)$, in particular, $p_i$ emerges as a function of $(q,\qdot,t)$ due to its definition {eq}`eq-classmech-32`, but we use {eq}`eq-classmech-74` to eliminate the $\qdot$'s in favor of the $p$'s, and express $H$ as a function of $(q,p,t)$ as shown.

Now we compute $\partial H/\partial q_i$, noting carefully that this derivative means holding $p$ fixed. We have

:::{math}
:label: eq-classmech-76
\frac{\partial H}{\partial q_i} = \sum_j p_j \frac{\partial \qdot_j}{\partial q_i} -\frac{\partial L}{\partial q_i} - \sum_j \frac{\partial L}{\partial \qdot_j} \frac{\partial \qdot_j}{\partial q_i},
:::

where $\partial \qdot_j/\partial q_i$ means the derivative of functions {eq}`eq-classmech-74`, taken at fixed $p$. But by {eq}`eq-classmech-32` the first and third terms on the right of {eq}`eq-classmech-76` cancel, while the second term on the right can be simplified with the help of {eq}`eq-classmech-33`. The result is $\partial H/\partial q_i = -\pdot_i$. Similarly, we compute $\partial H/\partial p_i$, which means holding $q$ fixed. We have

:::{math}
:label: eq-classmech-77
\frac{\partial H}{\partial p_i} = \qdot_i + \sum_j p_j \frac{\partial \qdot_j}{\partial p_i} - \sum_j \frac{\partial L}{\partial \qdot_j} \frac{\partial \qdot_j}{\partial p_i},
:::

where $\partial \qdot_j/\partial p_i$ means the derivative of functions {eq}`eq-classmech-74`, taken at fixed $q$. But by {eq}`eq-classmech-32` the two sums on the right hand side cancel, and we have $\partial H/\partial p_i = \qdot_i$.

In summary, we find

:::{math}
:label: eq-classmech-78
\boxed{\dod{q_i}{t} = \frac{\partial H}{\partial p_i}, \qquad \dod{p_i}{t} = -\frac{\partial H}{\partial q_i}.}
:::

These are *Hamilton's equations*. They are equivalent to the Euler-Lagrange equations in the case of a regular Lagrangian. Hamilton's equations display a notable symmetry between $q$ and $p$.

(sec-classmech-16)=

## Examples of Hamiltonians

Let us take a nonrelativistic, unconstrained system of $N$ particles interacting by means of a potential $V(\xvec_1,\ldots, \xvec_N,t)$, such as the electrostatic potential {eq}`eq-classmech-24`. The kinetic energy is

:::{math}
:label: eq-classmech-79
T={1\over2}\sum_{i=1}^N m_i |{\dot\xvec}_i|^2,
:::

and the Lagrangian is $L=T-V$. The momentum conjugate to $\xvec_i$ is

:::{math}
:label: eq-classmech-80
\pvec_i = m_i{\dot\xvec}_i,
:::

which can be inverted to solve for ${\dot\xvec}_i$ as a function of $\pvec_i$,

:::{math}
:label: eq-classmech-81
{\dot\xvec}_i = {1\over m_i} \pvec_i,
:::

a special case of {eq}`eq-classmech-74`. Then according to {eq}`eq-classmech-75` the Hamiltonian is

:::{math}
:label: eq-classmech-82
H= \sum_{i=1}^N \pvec_i\cdot{\dot\xvec_i} -L.
:::

But the first term is twice the kinetic energy, $2T$, so altogether,

:::{math}
:label: eq-classmech-83
H=T+V = \sum_{i=1}^N {|\pvec_i|^2 \over 2m_i} + V(\xvec_1, \ldots, \xvec_N,t),
:::

where we have used {eq}`eq-classmech-81` to eliminate ${\dot\xvec}_i$ in favor of $\pvec_i$. In this example, the Hamiltonian is the sum of the kinetic plus the potential energy, that is, it is the total energy.

Let us take the previous example and add an external magnetic field, producing the Lagrangian {eq}`eq-classmech-30`. Now the canonical momentum is

:::{math}
:label: eq-classmech-84
\pvec_i = m_i {\dot\xvec}_i + {Q_i\over c} \Avec(\xvec_i,t),
:::

where we drop the “ext” subscript on $\Avec$. This can be solved for ${\dot\xvec}_i$,

:::{math}
:label: eq-classmech-85
{\dot\xvec}_i = {1\over m_i}\Bigl[\pvec_i - {Q_i\over c}\Avec(\xvec_i,t) \Bigr],
:::

giving another version of {eq}`eq-classmech-74`. Now computing $H$ according to {eq}`eq-classmech-75` and using {eq}`eq-classmech-85` to eliminate ${\dot\xvec}_i$ in favor of $\pvec_i$, we find

:::{math}
:label: eq-classmech-86
H=\sum_{i=1}^N {1\over 2m_i} \Bigl[ \pvec_i - {Q_i\over c}\Avec(\xvec_i,t)\Bigr]^2 + V(\xvec_1,\ldots,\xvec_N,t).
:::

We will use this Hamiltonian frequently in this course. It is important to note that the first term is still the kinetic energy, just expressed in a somewhat complicated form because of the use of the canonical momentum {eq}`eq-classmech-84`.

Even in the presence of a magnetic field, the total energy of the system is still the sum of the kinetic and the potential energies. This corresponds to the physical fact that magnetic forces do not change the energy of a particle, because they are always orthogonal to the velocity vector.

The Hamiltonian is the total energy of the system in other examples, too, such as in relativistic problems. More generally, we may *define* the total energy of the system to be the Hamiltonian. For example, starting with the relativistic Lagrangian {eq}`eq-classmech-70` and applying the definition of the Hamiltonian {eq}`eq-classmech-75`, we obtain

:::{math}
:label: eq-classmech-87
H = \sqrt{m^2c^4 + c^2\Bigl(\pvec -{Q\over c}\Avec\Bigr)^2} + q\Phi,
:::

after taking some effort to eliminate $\vvec$ in favor of $\pvec$. The first term is just the kinetic energy of the particle, including the rest mass term $mc^2$, that is, it is $mc^2\gamma$, since

:::{math}
:label: eq-classmech-88
\gamma = {1\over\sqrt{\ds 1-{\ds\vvec^2\over\ds c^2}}} = \sqrt{1+ {\ds\pvec_kin^2 \over\ds m^2c^2}}.
:::

Expanding the square root in {eq}`eq-classmech-87` in the low velocity limit, we obtain

:::{math}
:label: eq-classmech-89
H = mc^2 + {1\over 2m}\Bigl(\pvec - {Q\over c}\Avec \Bigr)^2 + q\Phi,
:::

a version of {eq}`eq-classmech-86` in which the energy includes the rest mass term $mc^2$.

If we attempt to compute the Hamiltonian corresponding to the covariant Lagrangian {eq}`eq-classmech-47` or {eq}`eq-classmech-59`, we find that it vanishes, $H=0$. The reason is that these Lagrangians are not regular, and it is not possible to solve for the “velocities” $dx^\mu/d\lambda$ in terms of the momenta $p_\mu$. Hamiltonians in the usual sense are generators of translations in time, that is, time measured relative to a specific Lorentz frame. Thus Hamiltonians (in the usual formulation) cannot be covariant. This is one reason why in relativistic quantum field theory there is an effort to get away from Hamiltonians and to shift attention to objects that can support a covariant formulation of the dynamics, such as the Lagrangian, the path integral, and the $S$-matrix.

(sec-classmech-17)=

## The Minimal Coupling Prescription

The *minimal coupling prescription* is a simple rule for passing from a description of a free particle to that of the particle interacting with an electromagnetic field. It can be described as the replacement,

:::{math}
:label: eq-classmech-90
p^\mu \to p^\mu - {Q\over c}A^\mu.
:::

Here the $p^\mu$ on the left is the momentum (both kinetic and canonical) in the description of the free particle, while $p^\mu$ on the right is the canonical momentum in the description of the particle interacting with the field. Thus, the entire right hand side is still the kinetic momentum. The replacement takes one expression for the kinetic momentum and replaces it by another. The replacement can be broken into its space and time components, which are equivalent to

:::{math}
:label: eq-classmech-91
E \to E-Q\Phi, \qquad \pvec \to \pvec-{Q\over c}\Avec.
:::

Although we have given the minimal coupling prescription in relativistic form, it can be applied to nonrelativistic problems. For example, the energy and momentum of a nonrelativistic free particle are related by

:::{math}
:label: eq-classmech-92
E = {\pvec^2\over 2m}.
:::

Making the minimal coupling replacement {eq}`eq-classmech-91`, this becomes

:::{math}
:label: eq-classmech-93
E-q\Phi = {1\over 2m}\Bigl(\pvec-{Q\over c}\Avec\Bigr)^2,
:::

which, if we solve for $E$ and reinterpret $E$ as the Hamiltonian, becomes

:::{math}
:label: eq-classmech-94
H = {1\over 2m}\Bigl(\pvec-{Q\over c}\Avec\Bigr)^2 + Q\Phi,
:::

a single-particle version of the Hamiltonian {eq}`eq-classmech-86`.

As for a relativistic particle, the energy-momentum relation is

:::{math}
:label: eq-classmech-95
E = \sqrt{m^2c^4 + c^2\pvec^2}.
:::

Carrying out the minimal coupling prescription {eq}`eq-classmech-91` on this and solving for $E$, we obtain the Hamiltonian {eq}`eq-classmech-87`.

The prescription {eq}`eq-classmech-90` or {eq}`eq-classmech-91` is called “minimal” because it amounts to using the simplest Lorentz invariant coupling possible between the particle and the electromagnetic field, as explained in \secrclassmech-13. It is just a quick way of getting the Hamiltonian without having to go through the details of the Lagrangian and the Legendre transformation. The Hamiltonian so obtained is classical, but can be taken over into quantum mechanics as a first guess for a quantum description of the system. Minimal coupling does not always give the correct answers from a physical standpoint, that is, sometimes particles interact with the field by means of more complicated couplings than the simplest one. For example, the Hamiltonian {eq}`eq-classmech-86`, interpreted as a quantum Hamiltonian, does not include the interaction of the spin of the particles with a magnetic field (terms that appear in the Pauli equation). But even when the answer is not correct it is still interesting, because any corrections must involve additional Lorentz-invariant couplings that are more complicated than the minimal one.

Although we have only described minimal coupling in terms of particle mechanics, it can also be applied to fields, where it amounts to adding the term

:::{math}
:label: eq-classmech-96
{1\over c} \int d^3\xvec \, J^\mu A_\mu
:::

to the field Lagrangian, where $J^\mu$ is the 4-current associated with the matter field.

(sec-classmech-18)=

## Phase Space

The space upon which $(q,p)$ are coordinates is called *phase space*. Phase space can be thought of as the state space of the classical system, that is, the space in which a single point represents the *dynamical state* of the system. The dynamical state of a classical system is the specification of enough information to determine the future evolution of the system. Specifying a point of configuration space (the $q$'s) is not enough, instead we must also include the velocities (the $\qdot$'s), or, alternatively, the momenta (the $p$'s).

A point $(q,p)$ of phase space represents a complete set of initial conditions because Hamilton's equations on phase space are first order in time. We can visualize the flow in phase space through the vector field with components $(\qdot,\pdot)$, which is called a *Hamiltonian vector field*. {ref}`fig-classmech-6` illustrates the Hamiltonian vector field in the 2-dimensional phase space for the harmonic oscillator,

:::{math}
:label: eq-classmech-97
H={p^2\over 2m} + {m\omega^2 q^2 \over 2}.
:::

:::{figure} images/classmech-fig06.png
:label: fig-classmech-6
:width: 80%

The Hamiltonian vector field in phase space for the harmonic oscillator. One orbit (an ellipse) is shown.
:::

The orbit passing through a point of phase space is obtained by following the arrows of the Hamiltonian vector field. The orbit is tangent to the vector field at each point. One orbit of the harmonic oscillator (an ellipse) is illustrated in {ref}`fig-classmech-6`. Theorems about differential equations guarantee a unique solution $q(t)$, $p(t)$ passing through a given initial point $(q_0,p_0)$ at $t=t_0$ when the vector field is smooth. Thus, there is a unique orbit passing through each point of phase space. Orbits cannot cross one another in phase space, because the interpoint would have two orbits passing through it. Orbits in configuration space, however, are free to cross one another, since the equations of motion on configuration space are second order in time. For example, planets can and do collide.

(sec-classmech-19)=

## Time Evolution of Observables

A *classical observable* is simply any function of $q$, $p$, and possibly $t$. If the observable depends on $t$ it is said to have an *explicit* time-dependence. An example of an explicitly time-dependent observable is the electrostatic potential {eq}`eq-classmech-27`. In addition, any observable has a time-dependence when seen by a particle (or phase point) moving along its orbit, due to the time-dependence of $q$ and $p$. This is called an *implicit* time-dependence. For an observable $A(q,p,t)$, the total time derivative as seen by the phase point moving along its orbit is

:::{math}
:label: eq-classmech-98
\dod{A}{t} = \frac{\partial A}{\partial t} + \sum_i \Bigl(\frac{\partial A}{\partial q_i} \, \qdot_i + \frac{\partial A}{\partial p_i} \, \pdot_i\Bigr) =\frac{\partial A}{\partial t} + \sum_i \Bigl(\frac{\partial A}{\partial q_i}\frac{\partial H}{\partial p_i} -\frac{\partial A}{\partial p_i}\frac{\partial H}{\partial q_i}\Bigr),
:::

where we have used Hamilton's equations {eq}`eq-classmech-78` in the final form. The first term $\partial A/\partial t$ in {eq}`eq-classmech-98` represents the explicit time-dependence, while the sum represents the implicit time-dependence.

(sec-classmech-20)=

## Conservation of Energy

Setting $A=H$ in {eq}`eq-classmech-98`, we find the rate of change of the Hamiltonian itself along an orbit,

:::{math}
:label: eq-classmech-99
\dod{H}{t} = \frac{\partial H}{\partial t},
:::

since in that case the sum in {eq}`eq-classmech-98` vanishes. In particular, if the Hamiltonian has no explicit time-dependence, then $\partial H/\partial t=0$, and the Hamiltonian is conserved, $dH/dt=0$. This is the general law of *conservation of energy*.

The energy (the Hamiltonian) is not conserved if the Hamiltonian has an explicit time-dependence. In practice, such a time-dependence usually arises when a system is interacting with time-dependent, “external” forces, for example, the atom between the capacitor plates that feels the time-dependent electric field {eq}`eq-classmech-26`. Notice in this case that we assume that the external electric field is just a given function of space and time, and we ignore any reaction of the atom back on the charges in the capacitor. In reality, the atom consists of charged particles that produce their own electric field, which has an effect on the external system producing the external electric field. If we include the external charges in our definition of “the system” as well as the back reaction of the atom on these charges, then we have an enlarged system in which energy is conserved.

Similarly, consider a space craft that is obtaining a “gravity boost” by passing close to the planet Jupiter. Because Jupiter is so massive, it is a good approximation to assume that the position of Jupiter is just a given function of time, independent of the position of the spacecraft. Then the spacecraft feels a time-dependent gravitational field due to Jupiter, from which it can extract energy and get expelled from the solar system. In reality, Jupiter does react to the spacecraft, and moves slightly closer to the sun as the spacecraft leaves the solar system. Overall, energy is conserved.

(sec-classmech-21)=

## The Poisson Bracket

The final sum in {eq}`eq-classmech-98` is an example of a Poisson bracket, which is defined in general as follows. Let $A$ and $B$ be any two classical observables, possibly time-dependent. Then the *Poisson bracket* of $A$ and $B$ is another classical observable, given by

:::{math}
:label: eq-classmech-100
\{A,B\} = \sum_{i=1}^n \Bigl( \frac{\partial A}{\partial q_i}\frac{\partial B}{\partial p_i} - \frac{\partial A}{\partial p_i}\frac{\partial B}{\partial q_i} \Bigr).
:::

In terms of the Poisson bracket, {eq}`eq-classmech-98` can be written,

:::{math}
:label: eq-classmech-101
\dod{A}{t} = \frac{\partial A}{\partial t} + \{A,H\}.
:::

The Poisson bracket has the following properties. In the following we use capital letters for classical observables, and lower case letters for numbers (real or complex). First, it is linear in both operands,

:::{math}
:label: eq-classmech-102
\begin{aligned}
\{a_1 A_1 + a_2 A_2, B\} &= a_1 \{A_1,B\} +a_2 \{A_2,B\}, \\
\{A,b_1B_1 + b_2B_2\} &= b_1\{A,B_1\} + b_2\{A,B_2\}. \\

\end{aligned}
:::

Second, it is antisymmetric in the two operands,

:::{math}
:label: eq-classmech-103
\{A,B\} = -\{B,A\}.
:::

Third, it obeys the Leibnitz rule,

:::{math}
:label: eq-classmech-104
\{A,BC\} = B\{A,C\} + \{A,B\}C.
:::

Closely related to the Leibnitz rule is the chain rule for Poisson brackets, which is the following. If observable $B$ depends on a collection of other observables, say,

:::{math}
:label: eq-classmech-105
B=B(C_1,\ldots,C_K),
:::

then

:::{math}
:label: eq-classmech-106
\{A,B\} = \sum_{k=1}^K \{A,C_k\} \frac{\partial B}{\partial C_k}.
:::

A similar expression holds when $A$ depends on further observables.

Fourth, it satisfies the Jacobi identity,

:::{math}
:label: eq-classmech-107
\{A,\{B,C\}\} + \{B,\{C,A\}\} + \{C,\{A,B\}\} = 0.
:::

All these properties are straightforward to prove from the definition.

The Poisson brackets of the phase space coordinates, the $q$'s and $p$'s, among themselves are notable. These are

:::{math}
:label: eq-classmech-108
\{q_i,q_j\}=0, \qquad \{q_i,p_j\}=\delta_{ij}, \qquad \{p_i,p_j\}=0.
:::

(sec-classmech-22)=

## Conserved Quantities

In general, a *conserved quantity* or *constant of the motion* is a classical observable that is constant as we follow the Hamiltonian flow along an orbit. That is, $C$ is a constant of motion if

:::{math}
:label: eq-classmech-109
\dod{C}{t} = \frac{\partial C}{\partial t} + \{C,H\} = 0.
:::

A *time-independent* constant of the motion is one with no explicit time-dependence, so that $\partial C/\partial t=0$. It follows that time-independent constants of the motion are classical observables whose Poisson bracket with the Hamiltonian vanishes, $\{C,H\}=0$. As we say, such observables *Poisson commute* with the Hamiltonian.

In particular, the Hamiltonian Poisson commutes with itself, $\{H,H\}=0$, due to the antisymmetry of the Poisson bracket, property {eq}`eq-classmech-103`. Thus we recover {eq}`eq-classmech-99`.

(sec-classmech-23)=

## Liouville's Theorem

Liouville's theorem states that the volume of a region of phase space is constant in time, when the boundary of that volume and all the points inside it are allowed to move down their respective orbits by the same amount of elapsed time. In systems of one degree of freedom, in which phase space is the 2-dimensional $q$-$p$ plane, Liouville's theorem implies conservation of area, as illustrated in {ref}`fig-classmech-7`.

:::{figure} images/classmech-fig07.png
:label: fig-classmech-7
:width: 80%

Liouville's theorem in the phase plane. All points on the boundary of curve $C_0$ are allow to follow the Hamiltonian flow for the same amount of elapsed time, thereby mapping $C_0$ into $C_1$. The area enclosed is constant.
:::

Liouville's theorem is proved by a $2n$-dimensional version of Gauss's law. The essence of the proof is the vanishing of the total divergence of the flow vector in phase space,

:::{math}
:label: eq-classmech-110
\sum_{i=1}^n \Bigl(\frac{\partial \qdot_i}{\partial q_i} + \frac{\partial \pdot_i}{\partial p_i}\Bigr) = \sum_{i=1}^n \Bigl[\pop{}{q_i} \Bigl(\frac{\partial H}{\partial p_i}\Bigr) - \pop{}{p_i}\Bigl(\frac{\partial H}{\partial q_i}\Bigr)\Bigr]=0.
:::

(sec-classmech-24)=

## Classical Statistical Mechanics

A classical system whose state is only known statistically may be described at a certain time by means of a probability distribution $\rho$ on phase space. In general $\rho$ changes in time, so $\rho$ is a function of $q$, $p$ and $t$. The normalization condition is

:::{math}
:label: eq-classmech-111
\int d^nq\,d^np \, \rho(q,p,t) = 1,
:::

for all $t$. Alternatively, we may interpret $\rho$ as giving the density (per unit volume in phase space) of an ensemble of systems, each of which is governed by the same Hamiltonian $H$. The systems do not interact with one another. In this interpretation, the integral of $\rho$ over all phase space is the number of systems in the ensemble. It differs from the previous interpretation only in the normalization of $\rho$.

The evolution equation for $\rho$ may be obtained as follows. Consider an infinitesimal volume of phase space, with a certain number of systems of the ensemble in it. Let the volume move with the Hamiltonian flow, as in {ref}`fig-classmech-7`. The volume of the volume element does not change in this process, according to Liouville's theorem. Nor does the number of systems in the volume element, since the individual systems just evolve according to the (common) Hamiltonian. Therefore the number of systems per unit volume, which is $\rho$, is constant as we move along orbits. That is,

:::{math}
:label: eq-classmech-112
\frac{\partial \rho}{\partial t} + \{\rho,H\}=0.
:::

This is the *Liouville equation*.

Let $H$ be time-independent. It follows from the Liouville equation that the probability density can be constant in time (that is, $\partial \rho/\partial t=0$) only if $\{\rho,H\}=0$. The only way this can happen is if $\rho$ is a function of the time-independent constants of the motion. That is, let $\rho=\rho(C_1, \ldots, C_K)$, where the $C$'s are time-independent constants of the motion. Then by the chain rule property {eq}`eq-classmech-106` of the Poisson bracket we have

:::{math}
:label: eq-classmech-113
\{\rho,H\} = \sum_k \frac{\partial \rho}{\partial C_k} \{C_k,H\} = 0.
:::

To analyze these statements carefully requires ergodic theory, which we will not go into.

In some cases the only time-independent constant of the motion is the Hamiltonian itself. Then $\rho$ is constant in time only if $\rho$ is a function of the Hamiltonian. Two cases are of interest. One is

:::{math}
:label: eq-classmech-114
\rho=A \, \delta(H-E),
:::

where $A$ is a normalization constant and $E$ is an energy. The ensemble consists of systems of a known energy $E$. This is called the *microcanonical* ensemble. It is appropriate for isolated systems, in which the energy is constant.

Another important case is

:::{math}
:label: eq-classmech-115
\rho = {1\over Z} e^{-\beta H},
:::

where $\beta=1/kT$ is the usual thermodynamic parameter ($k$ is the Boltzmann constant, and $T$ the temperature). This is the *canonical* ensemble, appropriate for a system in contact with a heat bath at temperature $T$. Here $1/Z$ is the normalization of $\rho$, so that

:::{math}
:label: eq-classmech-116
Z(\beta) = \int d^nq\,d^np \, e^{-\beta H}.
:::

The quantity $Z(\beta)$ is the (classical) *partition function*.

(sec-classmech-25)=

## Hamilton's Principal Function

Let us return to the action functional {eq}`eq-classmech-11`, which is defined on paths belonging to the path space defined by {eq}`eq-classmech-13`. This path space is parameterized by the endpoints $q_0$ and $q_1$ and the endtimes $t_0$ and $t_1$. As noted, there may be more than one physical path in this path space, that is, more than one path on which the action is stationary. Let us denote these physical paths by $q_b(t)$, where $b$ is a “branch” index labeling the paths. Generally the branch index is discrete, so we can take $b=1,2,\ldots$.

The physical paths cause the action to be stationary. Does the action play any other role in mechanics? In particular, is there any significance to the *value* of the action functional, evaluated on a physical path? This value depends only on the branch index, and on the parameters of the path space itself. We will write $S_b(q_0,t_0;q_1,t_1)$ for this function, so that

:::{math}
:label: eq-classmech-117
S_b(q_0,t_0;q_1,t_1) = A[q_b(t)] = \int_{t_0}^{t_1} dt\, L\bigl( q_b(t), \qdot_b(t),t\bigr).
:::

This function is called *Hamilton's principal function*. It is also called “the action,” but you must not confuse it with the action functional $A[q(t)]$ or the other quantities called “the action” in classical mechanics. (They all have dimensions of action, but otherwise are different.)

Hamilton found that his principal function satisfies some interesting differential equations, which imply that knowledge of this function is equivalent to knowing the general solution of the classical equations of motion. This is remarkable, because Hamilton's principal function is a single function, while the general solution of the equations of motion involves $2n$ functions, giving the final $q$, $p$ coordinates as functions of the initial $q$, $p$ coordinates and the time.

:::{figure} images/classmech-fig08.png
:label: fig-classmech-8
:width: 80%

A path $q(t)$ satisfying fixed boundary conditions $q(t_0)=q_0$ and $q(t_1)=q_1$. Also shown is a modified path $q(t) + \delta q(t)$, satisfying the same endpoint and endtime conditions.
:::

{ref}`fig-classmech-8` illustrates a physical orbit $q(t)$ in the $q$-$t$ plane and a nearby physical orbit $q(t)+\delta q(t)$, whose final position $q_1$ and $t_1$ have been shifted slightly by amounts $dq_1$ and $dt_1$. That is, the modified orbit $q(t)+\delta q(t)$ satisfies

:::{math}
:label: eq-classmech-118
q(t_1+dt_1) + \delta q(t_1+dt_1) = q_1 + dq_1.
:::

This is at the upper limit. As shown in {ref}`fig-classmech-8`, the modified orbit coincides with the original orbit at the lower limit, that is,

:::{math}
:label: eq-classmech-119
q(t_0) + \delta q(t_0) = q_0,
:::

so $\delta q(t_0) = 0$.

{ref}`fig-classmech-8` differs from {ref}`fig-classmech-4` in several respects. First, the path $q(t)$ in {ref}`fig-classmech-4` is any path satisfying the endpoint and endtime conditions {eq}`eq-classmech-13`, generally a nonphysical path, while $q(t)$ in {ref}`fig-classmech-8` is a physical path. That is, $q(t)$ in {ref}`fig-classmech-8` is one of the paths $q_b(t)$ mentioned above, but we have suppressed the $b$ index. Next, $\delta q(t)$ in {ref}`fig-classmech-4` is a variation about the generally nonphysical path $q(t)$, producing another, generally nonphysical path, $q(t)+\delta q(t)$ in the same path space specified by {eq}`eq-classmech-13`. In {ref}`fig-classmech-8`, however, $\delta q(t)$ is the difference between two physical paths, $q(t)$ and $q(t)+\delta q(t)$. Also, the modified path $q(t)+\delta q(t)$ belongs to a different path space than $q(t)$, that is, it satisfies the modified endpoint and endtime conditions {eq}`eq-classmech-118` at the upper limit.

With these understandings, we can compute the difference in Hamilton's principal function between the two paths of {ref}`fig-classmech-8`. We suppress the branch index on $S$ as well as on $q(t)$. We have

:::{math}
\begin{aligned}
dS &= S(q_0,t_0;q_1+dq_1,t_1+dt_1) - S(q_0,t_0;q_1,t_1)
\end{aligned}
:::

:::{math}
\begin{aligned}
&= \int_{t_0}^{t_1+dt_1} L\bigl(q(t)+\delta q(t), \qdot(t) + \delta \qdot(t), t\bigr)\,dt - \int_{t_0}^{t_1} L\bigl(q(t),\qdot(t),t\bigr)\,dt
\end{aligned}
:::

:::{math}
:label: eq-classmech-120
\begin{aligned}
&= L(q_1,\qdot_1,t_1)\,dt_1 + \int_{t_0}^{t_1} dt \sum_{i=1}^n \Bigl[ \frac{\partial L}{\partial q_i} \delta q_i(t) + \frac{\partial L}{\partial \qdot_i} \delta \qdot_i(t)\Bigr],
\end{aligned}
:::

where $\qdot_1 = \qdot(t_1)$ and where we have expanded the right hand side out to first order in small quantities. We integrate the last term by parts as we did in {eq}`eq-classmech-16`, to obtain

:::{math}
:label: eq-classmech-121
\int_{t_0}^{t_1} dt \sum_{i=1}^n \Bigl[ \frac{\partial L}{\partial q_i} \delta q_i(t) + \frac{\partial L}{\partial \qdot_i} \delta \qdot_i(t)\Bigr] = \sum_{i=1}^n \left.\frac{\partial L}{\partial \qdot_i}\delta q_i(t) \right|_{t_0}^{t_1} - \int_{t_0}^{t_1} dt\, \sum_{i=1}^n \Bigl[ \frac{\partial L}{\partial q_i} - \dod{}{t}\Bigl(\frac{\partial L}{\partial \qdot_i}\Bigr)\Bigr] \delta q(t).
:::

This time, however, $\delta q$ does not vanish at $t_1$, while the integral on the right does vanish because the physical path $q(t)$ satisfies the Euler-Lagrange equations. The result is simply

:::{math}
:label: eq-classmech-122
\sum_{i=1}^n \frac{\partial L}{\partial \qdot_i}\delta q_i(t_1) = \sum_{i=1}^n p_{1i}\,\delta q_i(t_1),
:::

where $p_1$ means the momentum of the path $q(t)$, evaluated at $t_1$. Putting this back into {eq}`eq-classmech-118`, we have

:::{math}
:label: eq-classmech-123
dS = L_1\, dt_1 + \sum_{i=1}^n p_{1i}\,\delta q_i(t_1).
:::

Now expanding {eq}`eq-classmech-118` out to first order in small quantities, we have

:::{math}
:label: eq-classmech-124
\qdot(t_1)\, dt_1 + \delta q(t_1) = dq_1,
:::

which can be solved for $\delta q(t_1)$. Substituting this into {eq}`eq-classmech-123` gives

:::{math}
:label: eq-classmech-125
dS = \sum_{i=1}^n p_{1i} \, dq_{1i} - H_1\, dt_1,
:::

where

:::{math}
:label: eq-classmech-126
H_1 = \sum_{i=1}^n p_{1i}\,\qdot_{1i} - L_1
:::

is the Hamiltonian, evaluated at the $t_1$ endpoint of the path $q(t)$.

{eq}`eq-classmech-125` implies

:::{math}
:label: eq-classmech-127
\frac{\partial S}{\partial q_{1i}} = p_{1i}, \qquad \frac{\partial S}{\partial t_1} = -H_1.
:::

In {ref}`fig-classmech-8` we have varied the upper endpoint and endtime of the physical path $q(t)$, while keeping the lower endpoint and endtime fixed. If we also vary the lower endpoint and endtime, we find

:::{math}
:label: eq-classmech-128
\frac{\partial S}{\partial q_{0i}} = -p_{0i}, \qquad \frac{\partial S}{\partial t_0} = H_0.
:::

(sec-classmech-26)=

## The Hamilton-Jacobi Equation

Hamilton realized that {eq}`eq-classmech-127` and {eq}`eq-classmech-128` allow the general solution of the equations of motion to be obtained once his principal function $S$ is known. Since $S$ is a function of the parameters of the path space, $(q_0,t_0;q_1,t_1)$, the $q$-derivative in {eq}`eq-classmech-128` gives the initial momentum as a function of these parameters,

:::{math}
:label: eq-classmech-129
p_0 = p_0(q_0,t_0;q_1,t_1),
:::

where we just write $p_0$ for the vector of initial momenta $p_{0i}$, $i=1,\ldots, n$. This equation can be solved for $q_1$, giving us functions,

:::{math}
:label: eq-classmech-130
q_1 = Q(q_0,p_0,t_0,t_1),
:::

where $q_1$ is the value of the function $Q$. The function $Q$ gives the final position $q_1$ as a function of the initial position and momentum $(q_0,p_0)$ and the initial and final times $t_0$ and $t_1$.

Similarly, the $q$-derivative of {eq}`eq-classmech-127` gives the final momentum $p_1$ as a functions of the parameters of the path space,

:::{math}
:label: eq-classmech-131
p_1 = p_1(q_0,t_0;q_1,t_1).
:::

But by substituting {eq}`eq-classmech-130` into this, we can eliminate $q_1$ and express $p_1$ as a function of $(q_0,p_0,t_0,t_1)$:

:::{math}
:label: eq-classmech-132
p_1 = P(q_0,p_0,t_0,t_1),
:::

in which $p_1$ is the value of the function $P$. The function $P$ gives the final momentum $p_1$ as a function of the initial position and momentum $(q_0,p_0)$ and the initial and final times $t_0$ and $t_1$.

Taken together, the functions $Q$ and $P$ constitute the general solution of the equations of motion, that is, these functions specify the final dynamical state $(q_1,p_1)$ given the initial dynamical state $(q_0,p_0)$ and the two times. Given Hamilton's principal function $S$, the derivation only involves differentiations and algebraic operations (inverting systems of equations). There are no differential equations to be solved.

Thus we would like to find a way of determining Hamilton's principal function $S$. This function is defined in {eq}`eq-classmech-117` as the integral of the Lagrangian along the orbit, but if the orbits are not known we cannot do the integral. Therefore we seek an equation satisfied by $S$.

The desired equation comes from the time derivative in {eq}`eq-classmech-127`. In that equation, $H_1$ means the Hamiltonian evaluated at the final point on the orbit, that is, it is $H(q_1,p_1,t_1)$. At that point, however, $p_1$ is given by the $q$-derivative in {eq}`eq-classmech-127`. Putting the pieces together, we have

:::{math}
:label: eq-classmech-133
H\Bigl(q_1,\frac{\partial S}{\partial q_1},t_1\Bigr) + \frac{\partial S}{\partial t_1} = 0. .
:::

This is the *Hamilton-Jacobi equation* for the function $S$. It determines the $q_1$ and $t_1$ dependence of $S$. To determine the $q_0$ and $t_0$ dependence, we treat {eq}`eq-classmech-128` in a similar manner. This gives

:::{math}
:label: eq-classmech-134
H\Bigl(q_0,-\frac{\partial S}{\partial q_0},t_0\Bigr) - \frac{\partial S}{\partial t_0}=0,
:::

in effect a second Hamilton-Jacobi equation also satisfied by $S$. The solution of the classical equations of motion (Hamilton's equations), a system of coupled, ordinary differential equations, is equivalent to the solution of the pair of partial differential equations, {eq}`eq-classmech-133` and {eq}`eq-classmech-134`.

Solving {eq}`eq-classmech-133` and {eq}`eq-classmech-134` for Hamilton's principal function is not usually a practical way of solving the equations of motion of classical mechanics. There is a modification of this procedure, however, due to Jacobi, that is quite useful in certain applications. For the case of time-independent Hamiltonians, Jacobi's theory leads to another version of the Hamilton-Jacobi equation,

:::{math}
:label: eq-classmech-135
H\Bigl(q,\frac{\partial W}{\partial q}\Bigr) = E,
:::

where $E$ is an energy. This can be regarded as a time-independent version of the Hamilton-Jacobi equation. Here $W$ is a function of $q$ and a collection of parameters which turn out to be constants of motion. We will not pursue this topic here, which is covered in advanced books on classical mechanics. But Hamilton's principal function $S$ is important in semiclassical treatments of quantum mechanics (see {ref}`ch-wkb`\ and \pathint), where it appears as the phase of the propagator. If one must evaluate it, the easiest way is usually to use the definition {eq}`eq-classmech-117`. The function $W$ also appears in semiclassical treatments of quantum mechanics, where it is essentially the phase of an energy eigenfunction.

(sec-classmech-27)=

## Canonical Transformations

Coordinate transformations on phase space are used for many purposes. Classical perturbation theory, for example, is based on the idea of applying successive coordinate transformations that simplify the equations of motion to progressively higher powers of the perturbation parameter. When a coordinate transformation is carried out, a question is whether the new equations of motion can be written in the standard Hamiltonian form {eq}`eq-classmech-78`.

Let $(q,p)$ be the old coordinates on phase space and let $Q$ and $P$ stand for $2n$ invertible functions of $(q,p,t)$ that represent a new coordinate system on phase space. That is, let

:::{math}
:label: eq-classmech-136
\begin{aligned}
Q &= Q(q,p,t), \\
P &= P(q,p,t), \\

\end{aligned}
:::

where, as indicated, the coordinate transformation is allowed to depend on time. Suppose now that for all old Hamiltonians $H(q,p,t)$ there exists a “new Hamiltonian,” call it $K(Q,P,t)$, such that the new equations of motion are given by

:::{math}
:label: eq-classmech-137
{\dot Q}_i = \frac{\partial K}{\partial P_i}, \qquad {\dot P}_i = -\frac{\partial K}{\partial Q_i}.
:::

Then it can be shown that the new coordinates $Q$ and $P$ satisfy the Poisson bracket relations,

:::{math}
:label: eq-classmech-138
\begin{aligned}
\{Q_i,Q_j\} & = \sum_k\Bigl(\frac{\partial Q_i}{\partial q_k}\frac{\partial Q_j}{\partial p_k} - \frac{\partial Q_i}{\partial p_k}\frac{\partial Q_j}{\partial q_k}\Bigr) = 0, \\
\{Q_i,P_j\} & = \sum_k\Bigl(\frac{\partial Q_i}{\partial q_k}\frac{\partial P_j}{\partial p_k} - \frac{\partial Q_i}{\partial p_k}\frac{\partial P_j}{\partial q_k}\Bigr) = \delta_{ij}, \\
\{P_i,P_j\} & = \sum_k\Bigl(\frac{\partial P_i}{\partial q_k}\frac{\partial P_j}{\partial p_k} - \frac{\partial P_i}{\partial p_k}\frac{\partial P_j}{\partial q_k}\Bigr) = 0. \\
\end{aligned}
:::

In other words, the new coordinates satisfy the same Poisson bracket relations among themselves as the old coordinates. See {eq}`eq-classmech-108`.

Conversely, suppose the coordinate transformation satisfies {eq}`eq-classmech-138`. Then it can be shown that a new Hamiltonian $K(Q,P,t)$ exists such that the new equations of motion are {eq}`eq-classmech-137`.

A coordinate transformation that satisfies {eq}`eq-classmech-138` is called a *canonical transformation*. Canonical transformations are conveniently specified in terms of scalar “generating functions,” of which Hamilton's principal function $S$ and the function $W$ of {eq}`eq-classmech-135` are examples. There is also the problem of determining the new Hamiltonian $K$, given a canonical transformation and an old Hamiltonian $H$. If the transformation is time-independent, then the new Hamiltonian is the same as the old one, just transformed to the new coordinates. That is, $K(Q,P) = H(q,p)$ in this case. In the general, time-dependent, case, $K$ is not the same as $H$, rather there is an extra term involving the generating function. These topics are covered in advanced courses on classical mechanics.
