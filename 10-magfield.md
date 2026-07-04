---
title: "10. Charged Particles in Magnetic Fields"
---
(ch-magfield)=

# 10. Charged Particles in Magnetic Fields

(sec-magfield-1)=

## Introduction

An introduction to the quantum mechanics of charged particles in magnetic fields was given in {ref}`ch-tevolut`. In these notes we examine several problems involving charged particles in magnetic fields.

One of the issues that will be of most interest to us is the role of the magnetic vector potential $\Avec$ in quantum mechanics. In classical mechanics and classical electromagnetic theory, one could say that $\Avec$ is unnecessary, since both the equations of particle motion {eq}`eq-emunits-18` and Maxwell's equations are expressed purely in terms of $\Evec$ and $\Bvec$. Moreover, $\Evec$ and $\Bvec$ are physical in the sense that they can be measured, while $\Avec$ is not. One can construct devices that measure both $\Evec$ and $\Bvec$, but there is no such thing as an $\Avec$-meter. One can say that $\Avec$ contains a physical element (because $\Bvec$ can be computed from it), but it also contains a nonphysical element (the part of $\Avec$ that changes under a gauge transformation). In other words, $\Avec$ is partly conventional (what we call the gauge convention).

Similar considerations apply to $\Phi$, the scalar potential, although not so dramatically as with the vector potential. There is no such thing as a $\Phi$-meter. It is true that there are volt meters, but they have two wires, and measure the *relative* potential between two points. Moreover, the potential difference is only meaningful in the electrostatic approximation.

When we turn to quantum mechanics, however, we are struck by the fact that the Schr\"odinger equation, as a differential equation in $(x,y,z)$, necessarily involves the vector potential. Moreover, the wave function is gauge-dependent (see {ref}`sec-tevolut-19`). Does this mean that the vector potential has a direct physical significance in quantum mechanics? That is, are there physical effects in quantum mechanics that depend on the vector potential, that cannot be expressed in terms of $\Bvec$ alone?

The answer is no, a gauge convention remains just a convention in quantum mechanics, just as it is in classical mechanics. But quantum mechanics reveals that magnetic fields can have nonlocal effects, that is, a magnetic field in one region of space can have an effect on charged particles in another region of space where there is no magnetic field. These effects are expressed through the vector potential, while at the same time remaining gauge-invariant. This nonlocality is seen perhaps most clearly in the Aharanov-Bohm effect. Similar nonlocal effects occur in time-dependent electric fields.

We begin with some generalities on velocity operators, and then turn to the problem of a charged particle in a uniform magnetic field, a problem of great importance in condensed matter physics, astrophysics and elsewhere. Next we treat the Aharonov-Bohm effect, which reveals a kind of nonlocality in quantum mechanics that challenges our understanding of the meaning of the wave function. It does not, however, contradict any of the principles of quantum mechanics. Finally, we present Dirac's analysis of the magnetic monopole, which leads to an explanation of the quantization of electric charge.

(sec-magfield-2)=

## Velocity Operators

The Hamiltonian for a particle of mass $m$ and charge $q$ in an electromagnetic field is given in {eq}`eq-tevolut-69`, which we reproduce here:

:::{math}
:label: eq-magfield-1
H = {1\over 2m}\Bigl[\pvec -{q\over c}\Avec(\xvec,t)\Bigr]^2 + q\Phi(\xvec,t),
:::

where the potentials $\Phi$ and $\Avec$ are related to $\Evec$ and $\Bvec$ by {eq}`eq-tevolut-67a`. The momentum $\pvec$ appearing in this Hamiltonian is the canonical momentum. In classical mechanics, the velocity of the particle is given in terms of the canonical momentum by

:::{math}
:label: eq-magfield-2
\vvec={1\over m} \Bigl[\pvec - {q\over c}\Avec(\xvec,t) \Bigr].
:::

We adopt this formula also in quantum mechanics, and interpret $\vvec$ as a vector of operators. The same definition of velocity arises when applying the Heisenberg equations of motion to the Hamiltonian {eq}`eq-magfield-1`, that is, $\dot\xvec=\vvec$ (see Prob. {ref}`prob-tevolut-1`). In terms of the velocity operators, the Hamiltonian takes on the simple form,

:::{math}
:label: eq-magfield-3
H = {m\over 2}v^2 + q\Phi.
:::

This reveals the physical meaning of $H$ more clearly than {eq}`eq-magfield-1`, that is, the first major term of {eq}`eq-magfield-1` is just the kinetic energy of the particle.

But the Hamiltonian in the form {eq}`eq-magfield-3` raises a new question. If this is supposed to be the Hamiltonian for a particle in a magnetic field, why does the magnetic field $\Bvec$ (or even $\Avec$, from which $\Bvec$ can be computed) not appear in it? The same Hamiltonian would apply even if $\Bvec$ were zero, but obviously the physics would not be the same.

The answer is that the magnetic field is hiding in the commutators of the velocity operators, which do appear in the Hamiltonian. The components of velocity do not commute with one another, in general. Using the definition {eq}`eq-magfield-2` and the commutators

:::{math}
:label: eq-magfield-4
\begin{aligned}
[x_i,f(\pvec)] = i\hbar \frac{\partial f}{\partial p_i}, \\
[p_i,g(\xvec)] = -i\hbar \frac{\partial g}{\partial x_i}, \\

\end{aligned}
:::

(see Prob. {ref}`prob-spatialdof-4`), we find

:::{math}
:label: eq-magfield-5
[v_i,v_j] = {1\over m^2}\Bigl\{ [p_i,p_j] -{q\over c}\bigl([p_i,A_j] + [A_i,p_j]\bigr) +{q^2\over c^2}[A_i,A_j]\Bigr\} = {i\hbar q\over m^2 c} B_{ij},
:::

where

:::{math}
:label: eq-magfield-6
B_{ij} = \frac{\partial A_j}{\partial x_i}-\frac{\partial A_i}{\partial x_j} = \epsilon_{ijk} \, B_k.
:::

The antisymmetric tensor $B_{ij}$ contains the components of the magnetic field,

:::{math}
:label: eq-magfield-7
\begin{aligned}
B_{ij} = \begin{pmatrix}0 & B_z & -B_y \\ -B_z & 0 & B_x  \\ B_y & -B_x & 0 \\\end{pmatrix}.
\end{aligned}

:::

Putting this together, we have

:::{math}
:label: eq-magfield-8
[v_i,v_j] = {i\hbar q\over m^2 c}\, \epsilon_{ijk}\, B_k.
:::

We also note the commutators,

:::{math}
:label: eq-magfield-9
[x_i,v_j] = {i\hbar \over m} \, \delta_{ij}.
:::

The velocity commutators {eq}`eq-magfield-8` are proportional to the components of the magnetic field. Notice that this result holds regardless of the nature of the magnetic field (nonuniform, time-dependent, etc), with or without an electric field. If the magnetic field vanishes, then the components of velocity commute with one another, as is obvious since in that case $\pvec=m\vvec$, and since $[p_i,p_j]=0$.

(sec-magfield-3)=

## The Uniform Magnetic Field.  Classical Motion

We now consider the case $\Evec=0$, $\Bvec = B{\hat{\mathbf{z}}}$ where $B$ is a constant (independent of space and time). We also assume the particle is an electron, with charge $q=-e$. In the case of a positive particle the direction of motion changes as do the signs in various formulas.

The classical equations of motion are

:::{math}
:label: eq-magfield-10
\avec = -{e \over mc} \vvec \cross \Bvec,
:::

where $\vvec$ is the velocity and $\avec$ the acceleration. These can also be written,

:::{math}
:label: eq-magfield-11
\avec = \omega \,{\hat{\mathbf{z}}} \cross \vvec,
:::

where

:::{math}
:label: eq-magfield-12
\omega = {e B\over mc}
:::

is the frequency of the orbital gyration of the electron (the *gyrofrequency*). We write out {eq}`eq-magfield-11` in components,

:::{math}
:label: eq-magfield-13a
\begin{aligned}
a_x &= -\omega v_y,
\end{aligned}
:::

:::{math}
:label: eq-magfield-13b
\begin{aligned}
a_y &= \omega v_x,
\end{aligned}
:::

:::{math}
:label: eq-magfield-13c
\begin{aligned}
a_z &= 0.
\end{aligned}
:::

{eq}`eq-magfield-13c` shows that $v_z$ is a constant, in fact, the motion in the $z$-direction is that of a free particle in one dimension,

:::{math}
:label: eq-magfield-14
z = v_zt + z_0.
:::

Next we integrate {eq}`eq-magfield-13a` and {eq}`eq-magfield-13b` once in time and write the result as

:::{math}
:label: eq-magfield-15
\begin{aligned}
v_x &= -\omega(y-Y), \\
v_y &= \omega(x-X), \\

\end{aligned}
:::

where $X$ and $Y$ are constants of integration. Solving these for $X$ and $Y$, we have

:::{math}
:label: eq-magfield-16
\begin{aligned}
X &= x-{v_y \over \omega}, \\
Y &= y+{v_x \over \omega}.
\end{aligned}
:::

We will interpret $X$ and $Y$ momentarily.

Now define $\xi = x-X$ and $\eta = y-Y$, so that $\dot\xi = v_x$ and $\dot\eta = v_y$. Then the equations of motion {eq}`eq-magfield-15` become

:::{math}
:label: eq-magfield-17
\begin{aligned}
\begin{pmatrix}\dot\xi \\ \dot \eta \\\end{pmatrix} = \omega \begin{pmatrix}0 & -1 \\ 1 & 0 \\\end{pmatrix} \begin{pmatrix}\xi \\ \eta \\\end{pmatrix}.
\end{aligned}

:::

The solution is

:::{math}
:label: eq-magfield-18
\begin{aligned}
\begin{pmatrix}\xi(t) \\ \eta(t)\\\end{pmatrix} = \exp\left[\omega t\begin{pmatrix}0 & -1 \\ 1 & 0 \\\end{pmatrix}\right] \begin{pmatrix}\xi_0 \\ \eta_0 \\\end{pmatrix} = \begin{pmatrix}\cos\omega t & -\sin\omega t \\ \sin\omega t & \cos\omega t \\\end{pmatrix} \begin{pmatrix}\xi_0 \\ \eta_0 \\\end{pmatrix},
\end{aligned}

:::

where we sum the exponential power series of matrices as in Prob. {ref}`prob-hilbert-1`(b). The final matrix is a rotation in the counterclockwise direction in the $x$-$y$ plane by angle $\omega t$.

Now using $x=X+\xi$, $y=Y+\eta$, we see that the orbit in the $x$-$y$ plane is a circle centered on $(X,Y)$, as illustrated in {ref}`fig-magfield-1`. Taking into account the motion {eq}`eq-magfield-14` in the $z$-direction, we see that overall the orbit in three-dimensional space is a helix. The particle moves on a circle parallel to the $x$-$y$ plane, which itself is moving uniformly in the $z$-direction with velocity $v_z$. The center of the circle is called the *guiding center*. The guiding center coordinates are $(X,Y,z)$.

:::{figure} images/magfield-fig01.png
:label: fig-magfield-1
:width: 80%

The classical motion of an electron in the $x$-$y$ plane in a uniform magnetic field $\Bvec=B{\hat{\mathbf{z}}}$. $X$ and $Y$ are the coordinates of the guiding center.
:::

(sec-magfield-4)=

## The Energy Spectrum

Now we turn to the quantum problem. First we shall determine the energy spectrum (that is, the energy eigenvalues). For simplicity, we ignore the spin of the electron. This is not a good approximation, because when the spin is included, the energy levels are rather different from what we find here. See Prob. {ref}`prob-jjcouple-2`. We do it anyway, because it is easy to include the spin once we have solved the spinless problem, and we wish to address one issue at a time. The energy of the particle is something that can be measured, and so must be gauge-invariant. Therefore there must be a way of finding the energy eigenvalues in a gauge-invariant manner, that is, without committing ourselves to a gauge convention for $\Avec$. We will see that this is true.

The quantum Hamiltonian, expressed in terms of velocity variables, is given by {eq}`eq-magfield-3` with $\Phi=0$,

:::{math}
:label: eq-magfield-19
H={m\over 2}(v_x^2 + v_y^2) + {m\over 2}v_z^2 =H_\perp + H_\parallel.
:::

The energy is purely kinetic, and we have broken it into its parallel and perpendicular parts (that is, parallel to $\Bvec$ and in the $x$-$y$ plane). Since $q=-e$ and $\Bvec=B{\hat{\mathbf{z}}}$, the commutators {eq}`eq-magfield-8` become

:::{math}
:label: eq-magfield-20
\begin{aligned}
[v_x,v_y]& =-{i\hbar eB \over m^2 c} = -{i\hbar\omega\over m}, \\
[v_x,v_z] &= [v_y,v_z] = 0, \\

\end{aligned}
:::

where $\omega$ is the frequency {eq}`eq-magfield-12` of the classical motion. We see immediately that $[H_\perp,H_\parallel]=0$, so $H_\perp$ and $H_\parallel$ possess a simultaneous eigenbasis, which is an eigenbasis of $H$.

Our strategy for analyzing $H$ is to borrow definitions of interesting operators from the classical solution and to explore their properties. The most interesting operators for the perpendicular motion are $(x,y)$, $(X,Y)$, and $(v_x,v_y)$. The most interesting operators for the parallel motion are $(z,v_z)$. We borrow the classical definitions of $(X,Y)$, {eq}`eq-magfield-16`, and reinterpret them as operator equations that define $(X,Y)$ in terms of the position and velocity operators for the electron.

The commutator of the guiding center coordinates is

:::{math}
:label: eq-magfield-21
[X,Y] = \Bigl[x-{v_y\over\omega}, y+{v_x\over\omega}\Bigr] ={1\over\omega}\bigl( [x,v_x] -[v_y,y]\bigr) -{1\over \omega^2}[v_y,v_x] = {i\hbar\over m\omega},
:::

where we use {eq}`eq-magfield-9` and {eq}`eq-magfield-20`. Similarly we calculate the other commutators among the operators $(X,Y,v_x,v_y,z,v_z)$. The results are summarized in {ref}`tbl-magfield-1`.

:::{list-table} Commutators among various operators. The commutator in the table is $[R,C]$, where $R$ is the operator labeling the row and $C$ is the operator labeling the column. The table is antisymmetric.
:label: tbl-magfield-1
:header-rows: 1

* - 
  - $X$
  - $Y$
  - $v_x$
  - $v_y$
  - $z$
  - $v_z$
* - $X$
  - $0$
  - ${i\hbar\over m\omega}$
  - $0$
  - $0$
  - $0$
  - $0$
* - $Y$
  - $-{i\hbar\over m\omega}$
  - $0$
  - $0$
  - $0$
  - $0$
  - $0$
* - $v_x$
  - $0$
  - $0$
  - $0$
  - $-{i\hbar\omega\over m}$
  - $0$
  - $0$
* - $v_y$
  - $0$
  - $0$
  - ${i\hbar\omega\over m}$
  - $0$
  - $0$
  - $0$
* - $z$
  - $0$
  - $0$
  - $0$
  - $0$
  - $0$
  - ${i\hbar\over m}$
* - $v_z$
  - $0$
  - $0$
  - $0$
  - $0$
  - $-{i\hbar\over m}$
  - $0$

:::
The table shows that to within constant factors, the set of operators $(X,Y,v_x,v_y,z,v_z)$ forms a set of three canonically conjugate pairs of operators, that is, operators that satisfy the Heisenberg-Born commutation relations {eq}`eq-spatialdof-69a`. To bring this out more clearly we define new operators $(Q_i,P_i)$, $i=1,2,3$, by

:::{math}
:label: eq-magfield-22
\begin{aligned}
X &= {1\over\sqrt{m\omega}} Q_1, \qquad \qquad v_y = \sqrt{\ds{\ds\omega\over\ds m}} Q_2, \qquad\qquad z=Q_3, \\
Y &= {1\over\sqrt{m\omega}} P_1, \qquad \qquad v_x = \sqrt{\ds{\ds\omega\over\ds m}} P_2, \qquad \qquad mv_z =P_3, \\

\end{aligned}
:::

so that

:::{math}
:label: eq-magfield-23
[Q_i,Q_j]=[P_i,P_j]=0, \qquad \qquad [Q_i,P_j] = {i\hbar}\,\delta_{ij}.
:::

By working with variables of obvious physical importance, we have found a “canonical transformation,” that is, a transformation that preserves the canonical commutation relations. (See {ref}`sec-classmech-27` for canonical transformations in classical mechanics.)

Now we express $H$ in terms of these new variables, substituting {eq}`eq-magfield-22` into {eq}`eq-magfield-19`. We find

:::{math}
:label: eq-magfield-24
H=H_\perp+H_\parallel = {\omega\over 2}(Q_2^2 + P_2^2) +{P_3^2\over 2m}.
:::

The perpendicular kinetic energy appears as a harmonic oscillator, while the parallel kinetic energy appears as a one-dimensional free particle. The eigenvalues of $H_\perp$ are immediate; they are

:::{math}
:label: eq-magfield-25
E_{\perp n} = (n+\frac{1}{2})\hbar\omega.
:::

We know this because Dirac's derivation of the energy levels of the harmonic oscillator in {ref}`sec-harmosc-4` depends only on the commutation relations of the operators $x$ and $p$, which are reproduced here by operators $Q_2$ and $P_2$. The quantized energy levels of the perpendicular kinetic energy are called *Landau levels*.

(A note for the mathematically inclined. Technically, Dirac's derivation also involves an assumption of the irreducibility of the representation of the commutation relations, which amounts to making certain assumptions of nondegeneracy. The consequences of this assumption, both in the case of the harmonic oscillator and in the problem of the particle in a magnetic field, are obvious physically and on a first pass need not be belabored.)

As for the eigenvalues of $H_\parallel$, they are those of a free particle in one dimension, that is, the spectrum is continuous with $E_\parallel \ge 0$. Overall, the energy is

:::{math}
:label: eq-magfield-26
E_{nP_3} = (n+\frac{1}{2})\hbar\omega + {P_3^2 \over 2m},
:::

where now $P_3$ is an eigenvalue (a $c$-number) of the operator $P_3$, which has the spectrum $-\infty < P_3 < +\infty$.

The Hamiltonian {eq}`eq-magfield-24` is unusual because it does not depend on $(Q_1,P_1)$, which are essentially the guiding center coordinates $(X,Y)$. It would not be unusual to find a Hamiltonian that was independent of one of the coordinates, in which case the conjugate momentum would be a conserved quantity. But in this case neither the coordinate $Q_1$ nor the conjugate momentum $P_1$ appears, so they are both conserved. This makes sense physically, because classically the energy does not depend on where the circle is located in the $x$-$y$ plane, and moreover both $X$ and $Y$ are constants of motion.

The Hamiltonian $H_\perp$ in {eq}`eq-magfield-24` does not look exactly like the standard Hamiltonian for a mechanical harmonic oscillator,

:::{math}
:label: eq-magfield-27
H={p^2\over 2m} + {m\omega^2 x^2\over 2}.
:::

To bring out the relation between the two, we set

:::{math}
:label: eq-magfield-28
x = {x' \over \sqrt{m\omega}}, \qquad p = p' \sqrt{m\omega},
:::

which is a canonical transformation preserving the fundamental commutation relations. It causes the Hamiltonian {eq}`eq-magfield-27` to become

:::{math}
:label: eq-magfield-29
H = {\omega\over2} (x^2 + p^2),
:::

after dropping the primes. This has the same form as $H_\perp$ in {eq}`eq-magfield-24`.

We have succeeded in obtaining the energy levels of the electron moving in a uniform magnetic field by gauge-invariant means. That is, we never had to work with gauge-dependent quantities, such as $\Avec$ or $\psi$. It makes sense that we can do this, because the energy levels are experimentally measurable, and must be gauge-invariant.

(sec-magfield-5)=

## The Energy Eigenfunctions

Wave functions $\psi(x,y,z)$ in the presence of a magnetic field are gauge-dependent, as we have seen in {ref}`sec-tevolut-19`, so we will have to choose a gauge convention for $\Avec$ before we can find the energy eigenfunctions. One way to do this is to choose a gauge and then attempt to separate the Schr\"odinger equation in some coordinate system. It turns out that if the gauge chosen has the right symmetry, then the time-independent Schr\"odinger equation is separable in some coordinate system. In general, separability works when the system has some symmetry, although this is not completely obvious in the actual procedure.

The following method is more clear. Instead of focusing on the separation of the Schr\"odinger equation, we look for a complete set of commuting observables for the Hamiltonian {eq}`eq-magfield-19`. In the following we put hats on the operators $(\phat_i,\vhat_i,\Qhat_i,\Phat_i,\Xhat, \Yhat)$ to distinguish from the corresponding $c$-numbers $(p_i,v_i,Q_i,P_i,X,Y)$, where $i=1,2,3$. For other operators this distinction will not be necessary so we will omit the hats.

As we have already noted, $H_\perp$ and $H_\parallel$ commute with each other and with $H=H_\perp+H_\parallel$, so we can take $(H_\perp,H_\parallel)$, or, better, $(H_\perp,\Phat_3)$ as a pair of commuting operators. Recall that $H_\parallel=\Phat_3^2/2m$. But these operators do not form a complete set because the first degree of freedom $(\Qhat_1,\Phat_1)$, or, equivalently, the guiding center coordinates $(\Xhat,\Yhat)$, are not represented. But since any function of $(\Qhat_1,\Phat_1)$ commutes with any function of $(\Qhat_2,\Phat_2)$ and $(\Qhat_3,\Phat_3)$, we can take any function of $(\Qhat_1,\Phat_1)$, or, equivalently, $(\Xhat,\Yhat)$, as the third operator.

The fact that there is more than one way to choose the complete set of commuting observables means that the energy eigenfunctions are degenerate, and there is more than one way of choosing an orthonormal basis in the degenerate eigenspaces. Such freedom arises because the motion of a charged particle in a uniform magnetic field is a highly symmetrical problem. In particular, it is clear that the magnetic field is invariant under translations in the $x$-, $y$-, and $z$-directions, as well as under rotations about the $z$-axis. If we add further physical effects (for example, an electric field), then some of this symmetry is broken and the set of choices for a complete set of commuting observables narrows. For now we will take the third operator to be $\Qhat_1$, or, equivalently, $\Xhat$, which is probably the simplest choice. Thus we will be interested in finding the simultaneous eigenfunctions of $(\Xhat,H_\perp,\Phat_3)$.

Since $\Xhat$ and $\Phat_3$ are simpler than $H_\perp$, we find their eigenfunctions first. We start with $\Phat_3$, for which we wish to solve

:::{math}
\begin{aligned}
\Phat_3 \psi(x,y,z) &= m\vhat_z \psi(x,y,z)= \Bigl[\phat_z +{e\over c}A_z(x,y,z) \Bigr]\psi(x,y,z)
\end{aligned}
:::

:::{math}
:label: eq-magfield-30
\begin{aligned}
&=\Bigl[-i\hbar\pop{}{z} +{e\over c}A_z(x,y,z)\Bigr] \psi(x,y,z) = P_3 \psi(x,y,z),
\end{aligned}
:::

where we use $\Phat_3 = m\vhat_z$ and {eq}`eq-magfield-2`. This equation is hard to solve because of the presence of $A_z(x,y,z)$. Can we choose a gauge so that $A_z=0$? We write out $\Bvec = B{\hat{\mathbf{z}}} = \del\cross\Avec$ in components,

:::{math}
:label: eq-magfield-31
\begin{aligned}
B_x &= \frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z} = 0, \\
B_y &= \frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x} = 0, \\
B_z &= \frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y} = B, \\

\end{aligned}
:::

and we notice that if $A_z=0$ then $A_x$ and $A_y$ are independent of $z$,

:::{math}
:label: eq-magfield-32
\begin{aligned}
A_x &= A_x(x,y), \\
A_y &= A_y(x,y). \\

\end{aligned}
:::

This means that the entire vector potential $\Avec$ is independent of $z$, that is, it is invariant under displacements in the $z$-direction. This is obviously one of the symmetries of the magnetic field $\Bvec$, which with the choice $A_z=0$ is reproduced by the vector potential.

Since $A_z=0$, we have

:::{math}
:label: eq-magfield-33
\Phat_3 = m\vhat_z = \phat_z,
:::

so henceforth we will write simply $\phat_z$ for $\Phat_3$, and similarly for the eigenvalue $p_z=P_3$. Then {eq}`eq-magfield-30` becomes

:::{math}
:label: eq-magfield-34
\phat_z \psi(x,y,z) = -i\hbar\frac{\partial \psi(x,y,z)}{\partial z} = p_z \psi(x,y,z),
:::

or,

:::{math}
:label: eq-magfield-35
\psi(x,y,z) = \phi(x,y) e^{ip_z z/\hbar},
:::

where $\phi(x,y)$ is an arbitrary function of $(x,y)$. The wave function is a free particle solution in the $z$-direction.

We determine $\phi(x,y)$ by requiring that $\psi(x,y,z)$ be an eigenfunction also of $\Xhat$ and $H_\perp$. We start with $\Xhat$, for which the eigenvalue-eigenfunction problem is

:::{math}
:label: eq-magfield-36
\Xhat \psi(x,y,z) = X\psi(x,y,z),
:::

where $\psi$ is given by {eq}`eq-magfield-35`. But since the operator $\Xhat$ does not involve the coordinate $z$, we can cancel the factor of $e^{ip_zz/\hbar}$, and we have

:::{math}
\begin{aligned}
\Xhat \phi(x,y) &= \Bigl(x-{1\over\omega}\vhat_y\Bigr) \phi(x,y) =\Bigl[x - {1\over m\omega}\Bigl(\phat_y + {e\over c} A_y(x,y)\Bigr)\Bigr]\phi(x,y)
\end{aligned}
:::

:::{math}
:label: eq-magfield-37
\begin{aligned}
&=\Bigl[x - {1\over m\omega}\Bigl(-i\hbar\pop{}{y}+ {e\over c} A_y(x,y)\Bigr)\Bigr]\phi(x,y) = X\phi(x,y).
\end{aligned}
:::

We simplify this equation by choosing $A_y$ to cancel the $x$, that is,

:::{math}
:label: eq-magfield-38
x-{e\over m\omega c}A_y = x -{1\over B}A_y = 0,
:::

or,

:::{math}
:label: eq-magfield-39
A_y=Bx.
:::

This is consistent with {eq}`eq-magfield-31` if $A_x=0$, so in effect we have now chosen the gauge,

:::{math}
:label: eq-magfield-40
\Avec = Bx\,{\hat{\mathbf{y}}}.
:::

This vector potential is invariant under translations in the $y$- and $z$- directions, but not the $x$-direction. Of course the magnetic field is invariant under translations in all three directions. We see that overall, the vector potential $\Avec$ has less symmetry than the magnetic field $\Bvec$.

{eq}`eq-magfield-37` now simplifies to

:::{math}
:label: eq-magfield-41
{i\hbar\over m\omega} \frac{\partial \phi(x,y)}{\partial y} = X\phi(x,y),
:::

or,

:::{math}
:label: eq-magfield-42
\phi(x,y) = e^{-im\omega Xy/\hbar} f(x),
:::

where $f$ is an arbitrary function of $x$. We now have a simultaneous eigenfunction of $\phat_z$ and $\Xhat$.

We determine $f(x)$ by requiring that $\psi$ also be an eigenfunction of $H_\perp$, that is, we solve $H_\perp\psi = E_\perp \psi$. But since $H_\perp$ does not involve the $z$-coordinate, we can cancel the factor $e^{ip_zz/\hbar}$ and work with

:::{math}
:label: eq-magfield-43
H_\perp \phi(x,y) = E_\perp \phi(x,y),
:::

or,

:::{math}
\begin{aligned}
{m\over 2}(\vhat_x^2 + \vhat_y^2) \phi(x,y) &=  {1\over 2m}\Bigl[\Bigl(\phat_x + {e\over c}A_x\Bigr)^2 +\Bigl(\phat_y + {e\over c}A_y\Bigr)^2\Bigr] f(x) e^{-im\omega Xy/\hbar}
\end{aligned}
:::

:::{math}
\begin{aligned}
&={1\over 2m}\Bigl[ -\hbar^2 {\partial^2 \over \partial x^2} +\Bigl(-i\hbar\pop{}{y} +{eBx\over c}\Bigr)^2\Bigr] f(x) e^{-im\omega Xy/\hbar}
\end{aligned}
:::

:::{math}
:label: eq-magfield-44
\begin{aligned}
&=E_\perp f(x) e^{-im\omega Xy/\hbar}.
\end{aligned}
:::

But now $-i\hbar\partial/\partial y$ brings down a factor $-m\omega X$, so we can cancel the phase factor and we have an equation purely in the coordinate $x$,

:::{math}
:label: eq-magfield-45
-{\hbar^2\over 2m} {d^2 f(x)\over dx^2} + {m\omega^2\over 2}(x-X)^2f(x) = E_\perp f(x).
:::

This is the equation of a harmonic oscillator, with origin shifted to $x=X$. The energies are $E_\perp = (n+\frac{1}{2})\hbar\omega$, which we knew already, and the eigenfunctions are

:::{math}
:label: eq-magfield-46
f(x) = u_n(x-X),
:::

where $u_n(x)$ are the energy eigenfunctions of the usual harmonic oscillator [see {eq}`eq-harmosc-46`]. Overall, the simultaneous eigenfunction of $(\Xhat,H_\perp,\phat_z)$ with quantum numbers $(X,n,p_z)$ is

:::{math}
:label: eq-magfield-47
\psi_{Xnp_z}(x,y,z) = e^{-im\omega Xy/\hbar + ip_zz/\hbar} \, u_n(x-X).
:::

:::{figure} images/magfield-fig02.png
:label: fig-magfield-2
:width: 80%

Plot of $|\psi|^2$ in the $x$-$y$ plane for $n=0$. Vertical direction is $|\psi|^2$.
:::

The probability density $|\psi|^2$ for the Landau ground state ($n=0$) in the $x$-$y$ plane is plotted in {ref}`fig-magfield-2`. Squaring the wave function gets rid of the phase factors in {eq}`eq-magfield-47`, and allows us to plot a real function. The result is a “Gaussian mountain range” that is centered on the line $x=X$. Notice that the wave function does not look at all like the classical solution; that is because we have constructed an eigenfunction of ${\hat X}$, the $x$-component of the guiding center position. But since ${\hat X}$ and ${\hat Y}$ do not commute, the value of $Y$ is completely undetermined. That is the reason the mountain range extends to infinity in the $y$-direction.

We could have chosen ${\hat Y}$ instead of ${\hat X}$ as the third observable (in addition to $H_\perp$ and ${\hat P}_3$) to form a complete set, but the simultaneous eigenfunctions of that set would have mountain ranges extending out to infinity in the $x$-direction. These features are a consequence of the nonvanishing commutator $[{\hat X},{\hat Y}]$. The energy eigenfunction would still not look much like the classical orbits, in this case in effect because the classical orbit is smeared in the $x$-direction.

Another possibility is to choose the $z$-component of angular momentum as the third observable. This is explored in Prob.~\prbrmagfield-1. Does this produce wave functions that look more like the classical orbit? Unfortunately, no, because an eigenstate of $L_z$ must be completely indeterminate in the conjugate angle $\phi$. It is as if the classical solution is smeared out by rotating it about the $z$-axis. Remember that the classical orbit is a circle, but it is centered on $(X,Y)$, not the origin in general. So when the classical circular orbit is smeared around in $\phi$, it creates an annular ring around the origin, which is where the eigenfunctions of $(L_z,H_\perp,P_3)$ are concentrated.

Can we find energy eigenfunctions that do look like the classical orbits? Yes, it turns out that we want to use a coherent state in the $X$ and $Y$ operators. These are eigenfunctions of not only $H_\perp$ and $P_3$ but also of the annihilation operator proportional to ${\hat X}+i{\hat Y}$. These are not eigenstates of complete sets of commuting observables, because the annihilation operator is not Hermitian and so is not an observable. But the energy eigenfunctions in this representation do resemble rather closely the classical orbits, that is, circles centered on the guiding center position $(X,Y)$ (actually the expectation values of the operators ${\hat X}$, $\hat Y$, as usual with coherent states). The use of coherent states in the motion of a charged particle in a uniform magnetic field is explored in Prob.~\prbrmagfield-4.

One final comment. In most of the literature the energy eigenfunctions {eq}`eq-magfield-47` would be described as the “solution in the gauge $\Avec=Bx\,{\hat{\mathbf{y}}}$” [the gauge {eq}`eq-magfield-40`]. This is because if we use the gauge {eq}`eq-magfield-40` in the three-dimensional Schr\"odinger equation, then it is separable in rectangular coordinates and the solution is {eq}`eq-magfield-47`. But it would be better to call {eq}`eq-magfield-47` “the energy eigenfunctions that are also eigenfunctions of $\Xhat$ and $\Phat_3$,” which is essentially what we have done here, since once the solution is obtained (by any means) we can perform a gauge transformation on it, as described in {ref}`sec-tevolut-19`, and put it into any gauge we want. The gauge transformation will change the phase of the wave function but not $|\psi|^2$, so {ref}`fig-magfield-2` does not change, nor does the physics that explains the mountain range in the $y$-direction. The usual terminology confuses the gauge which causes the Schr\"odinger equation to be separable with the gauge in terms of which the wave function is expressed. If we consider a class of wave functions that are related by gauge transformations as being physically equivalent, then the physics of the solution is determined by the complete set of commuting observables, not the gauge.

(sec-magfield-6)=

## The Flux Quantum

Although the $x$ and $y$ coordinates of the particle are commuting operators, as we have seen the $X$ and $Y$ coordinates of the guiding center are not. Thus, the guiding center $X$-$Y$ plane is more like a phase space than a configuration space. The same can be said for the $v_x$-$v_y$ plane.

Let us consider a region of the guiding center plane with an area of one Planck cell. See {ref}`sec-wkb-13` for a discussion of Planck cells. Measured in terms of the variables $Q_1$ and $P_1$ the area is $\Delta Q_1 \Delta P_1 = 2\pi\hbar$. But this can be expressed in terms of the guiding center coordinates through {eq}`eq-magfield-22`,

:::{math}
:label: eq-magfield-48
\Delta Q_1 \Delta P_1 = m\omega \Delta X \Delta Y = {eB \over c} \Delta X \Delta Y = 2\pi\hbar,
:::

or,

:::{math}
:label: eq-magfield-49
B \Delta X \Delta Y = {2\pi\hbar c \over e} = {hc \over e},
:::

where $h=2\pi\hbar$ is Planck's original constant. This is the amount of flux passing through a single Planck cell of the guiding center plane. It indicates how much area of the guiding center plane is occupied by a single quantum state.

The quantity $hc/e$ on the right hand side is a natural unit of magnetic flux, called a “flux quantum.” The name is somewhat inappropriate, because magnetic flux is not quantized---there is no rule that magnetic flux must come in integer multiples of a flux quantum. Nevertheless, the flux quantum is a unit that appears in many problems involving magnetic fields.

For example, two-dimensional electron systems are common in condensed matter physics, when electrons are trapped in the $z$-direction by some potential, for example, at the interface between two media. Then if a magnetic field is applied perpendicular to the interface, the electrons occupy various Landau levels.

Naturally a realistic two-dimensional system like this does not extend to infinity but rather is confined to a finite area in the $x$-$y$ plane by the size of the sample. If we fill up electron states starting from the ground state and increasing in energy, as we must if we want the ground state of a multielectron system, then how many electrons in the two-dimensional system can occupy the Landau ground state? The answer is the area of the sample divided by the area $\Delta X \Delta Y$ shown in {eq}`eq-magfield-49`, times two to account for the electron spin. That is, it is twice the number of flux quanta in the flux intercepted by the whole sample. After this, successive electrons enter the first Landau level until it is filled, etc.

If now we change the magnetic field, the number of electrons contained in each Landau level changes. If we increase the magnetic field then the ground Landau level can hold more electrons, so electrons from the first Landau level move down into the ground Landau level, etc. Conversely if we lower the magnetic field. (This is assuming the system remains in the collective ground state as the magnetic field is changed.) The physics described here lies behind the de Haas-van Alphen effect, which refers to the fact that the magnetization of a bulk sample is a periodic function of the magnetic field, under the right circumstances.

(sec-magfield-7)=

## The Aharanov-Bohm Effect

We now take up the Aharanov-Bohm effect, which concerns the quantum mechanics of a charged particle in the field of a long solenoid. The analysis leads to further insight into the role of the vector potential $\Avec$ in quantum mechanics, as well as the surprising conclusion that magnetic fields in one region of space can have an effect on charged particles in another region where the magnetic field is zero.

:::{figure} images/magfield-fig03.png
:label: fig-magfield-3
:width: 80%

A long solenoid is centered on the $z$-axis.
:::

:::{figure} images/magfield-fig04.png
:label: fig-magfield-4
:width: 80%

Cross of the solenoid. The radius in the $x$-$y$ plane is $a$.
:::


The long solenoid is a simple problem in magnetostatics. We center the solenoid on the $z$-axis, as shown in {ref}`fig-magfield-3`. It has a circular cross in the $x$-$y$ plane, as shown in {ref}`fig-magfield-4`, with radius $\rho=a$, where

:::{math}
:label: eq-magfield-50
\rho=\sqrt{x^2+y^2}.
:::

The magnetic field is uniform in the $z$-direction inside the solenoid and zero outside,

:::{math}
:label: eq-magfield-51
\begin{aligned}
\Bvec=\begin{cases}B{\hat{\mathbf{z}}}, & \rho<a, \\  0, & \rho>a,\\\end{cases}
\end{aligned}

:::

as illustrated in {ref}`fig-magfield-5`.

To obtain the vector potential we assume it is in the $\phi$-direction, $\Avec=A_\phi\,{\hat{\boldsymbol{\phi}}}$, and then we integrate $\Avec$ in the counterclockwise direction around a circle $C$ of radius $\rho$ in the $x$-$y$ plane, centered on the $z$-axis. We allow the circle $C$ to be either inside or outside the solenoid. The integral is the magnetic flux captured by the circle, that is,

:::{math}
:label: eq-magfield-52
\begin{aligned}
\oint_C \Avec\cdot d\ellvec = 2\pi\rho \, A_\phi = \begin{cases}\pi\rho^2 B, & \rho<a, \\  \pi a^2 B, & \rho>a,\\\end{cases}
\end{aligned}

:::

or,

:::{math}
:label: eq-magfield-53
\begin{aligned}
A_\phi=\begin{cases}B\,\ds {\rho\over 2}, & \rho<a, \\  B\,\ds {a^2\over 2\rho}, & \rho>a.\\\end{cases}
\end{aligned}

:::

The magnetic field and vector potential are plotted in Figs.~{ref}`fig-magfield-5` and {ref}`fig-magfield-6`. The magnetic field has a discontinuity at $\rho=a$ because of the surface current in the solenoid, but the vector potetial is continuous there. Note especially that the vector potential is nonzero in the exterior region where $\Bvec=0$.

:::{figure} images/magfield-fig05.png
:label: fig-magfield-5
:width: 80%

The magnetic field is uniform inside the solenoid and zero outside.
:::

:::{figure} images/magfield-fig06.png
:label: fig-magfield-6
:width: 80%

The vector potential is continuous at the boundary $\rho=a$ and nonzero in the exterior region.
:::


Evidently we have derived the identity,

:::{math}
:label: eq-magfield-54
\del\cross\Bigl({Ba^2\over 2\rho}{\hat{\boldsymbol{\phi}}}\Bigr)=0,
:::

which applies in the exterior region and which is easily checked with {eq}`eq-vecident-11`. In view of where we are going, you may wonder why we do not just set $\Avec=0$ in the exterior region, since that is simpler and would also give $\Bvec=0$. The reason is that such a choice would introduce a discontinuity in $\Avec$ at $\rho=a$, which, upon taking the curl, would give a $\delta$-function singularity in $\Bvec$. Although the current $\Jvec$ does have a $\delta$-function singularity at $\rho=a$, the magnetic field does not. Thus we cannot avoid the conclusion that $\Avec\ne0$ in the exterior region.

Let us consider the motion of a spinless particle of mass $m$ and charge $q$ in the exterior region. We imagine the surface of the solenoid $\rho=a$ is a hard wall that the particle bounces off, so that it never enters the region where $\Bvec\ne0$. The nonvanishing vector potential in the exterior region would have no effect on the classical motion of the particle, since the Lorentz force $(q/c)\vvec\cross\Bvec=0$. However, the Schr\"odinger equation is expressed in terms of $\Avec$, not $\Bvec$. Does the nonvanishing vector potential in the exterior region give rise to physical effects on the quantum mechanics of charged particles moving in that region? That is, does the behavior of the charged particle in the exterior region depend on the strength of the magnetic field inside the solenoid?

The answer is yes, as we find simply by solving the Schr\"odinger equation in the exterior region, with the vector potential {eq}`eq-magfield-53` and the boundary condition $\psi=0$ at $\rho=a$. The energy eigenfunctions are easily obtained and involve Bessel functions $J_\nu(k\rho)$ and $Y_\nu(k\rho)$, where $E=\hbar^2k^2/2m$. The order $\nu$ of the Bessel functions, as it turns out, depends on $B$, thereby confirming that the solution of the Schr\"odinger equation in the exterior region depends on the strength of the magnetic field in the interior region, where the particle never ventures.

:::{figure} images/magfield-fig07.png
:label: fig-magfield-7
:width: 80%

A path $P=[\xvec(\tau)]$ that contributes to the path integral between initial point $\xvec_0$ at $t=0$ and final point $\xvec$ at time $t$. Shaded region is the solenoid; the path integral is taken over paths are lie outside the solenoid.
:::

:::{figure} images/magfield-fig08.png
:label: fig-magfield-8
:width: 80%

Any two paths that are homotopic, such as $P$ and $P'$, give rise to the same magnetic action.
:::


But we prefer not to deal with Bessel functions so we shall examine the problem from the standpoint of the path integral rather than the energy eigenfunctions. This approach is not only more vivid in the physical picture it offers but is interesting in its own right.

The fields are time-independent so we write the propagator as

:::{math}
:label: eq-magfield-55
K(\xvec,\xvec_0,t)=\matrixelement{\xvec}{U(t)}{\xvec_0} = \int dP \,e^{(i/\hbar)S[P]},
:::

where we have used a version of {eq}`eq-pathint-29` for the path integral. Here the path $\xvec(\tau)$ is denoted by $P$ for simplicity, and the notation $dP$ stands for $C\,d[\xvec(\tau)]$, including the constant factor $C$ seen in {eq}`eq-pathint-29`. It is understood that all paths satisfy the boundary conditions $\xvec(0)=\xvec_0$ and $\xvec(t)=\xvec$, where $\xvec$, $\xvec_0$ and $t$ are the parameters upon which $K$ depends, as illustrated in {ref}`fig-magfield-7`. Also, we write the action functional as $S$ to avoid confusion with the vector potential $\Avec$. Since the Lagrangian of a particle in a magnetic field is

:::{math}
:label: eq-magfield-56
L={1\over 2}mv^2 +{q\over c}\vvec\cdot\Avec(\xvec)
:::

(see {ref}`sec-classmech-9`), the action functional is given explicitly by

:::{math}
:label: eq-magfield-57
S[P]=S[\xvec(\tau)]= \int_0^t d\tau \, \Bigl[ {m\over 2}\Bigl(\dod{\xvec}{\tau}\Bigr)^2 +{q\over c}\dod{\xvec}{\tau}\cdot \Avec\bigl(\xvec(\tau)\bigr) \Bigr] =S_free[P]+S_mag[P],
:::

which shows the decomposition of the action into a free part and a magnetic part. It is understood that the space of paths that we integrate over consists of all paths joining the initial and final space-time points $(\xvec_0,0)$ and $(\xvec,t)$ that do not enter the region $\rho<a$, although they are allowed to loop or bounce off the walls of the solenoid as many times as they want. With this understanding, the free action alone would give us the propagator for the scattering of otherwise free particles from the hard walls of a cylinder at $\rho=a$.

The magnetic action, however, modifies the propagator. Notice first that the $d\tau$ factors cancel in the magnetic action, so that it does not depend on the $\tau$ parameterizatio of the path,

:::{math}
:label: eq-magfield-58
S_mag[P] = {q\over c} \int_{\xvec_0}^\xvec \Avec(\xvec)\cdot d\xvec,
:::

that is, it is just a line integral in 3-dimensional space. In fact, the magnetic action almost does not depend on the path at all, except for the endpoints. More precisely, consider two paths $P$ and $P'$ that can be continuously deformed into one another without crossing the solenoid, as illustrated in {ref}`fig-magfield-8`. Such paths are said to be *homotopic*. Then the magnetic actions along the two paths are identical,

:::{math}
:label: eq-magfield-59
S_mag[P']-S_mag[P] = {q\over c}\oint \Avec(\xvec)\cdot d\xvec = 0,
:::

since the difference as shown is the integral of $\Avec$ around the closed loop obtained by first following $P'$ and then following $P$ backwards to the initial point. This integral is the magnetic flux through the loop, which is zero since the magnetic field vanishes in the exterior region.

:::{figure} images/magfield-fig09.png
:label: fig-magfield-9
:width: 80%

Two paths $P$ and $P'$ that are not homotopic.
:::

If the paths are not homotopic it is because they loop the solenoid a different number of times, as illustrated in {ref}`fig-magfield-9`. In the figure, path $P'$ loops the solenoid twice in the counterclockwise direction, relative to path $P$. Thus, the difference in the magnetic actions is proportional to twice the flux $\Phi$ through the solenoid,

:::{math}
:label: eq-magfield-60
S_mag[P']-S_mag[P] = 2{q\Phi\over c},
:::

where

:::{math}
:label: eq-magfield-61
\Phi=\pi a^2 B.
:::

To be more general let us choose a reference path $P_0$ and define $S_0=S_mag[P_0]$. Then we define the *winding number* of any path $P$ as the number of times the closed loop $P-P_0$ goes around the solenoid in the counterclockwise direction, where $P-P_0$ means, first follow $P$, then follow $P_0$ backwards. Then it is intuitively clear that any two paths are homotopic if and only if they have the same winding number. Also,

:::{math}
:label: eq-magfield-62
S_mag[P]=S_0+n{q\Phi\over c},
:::

where $n$ is the winding number of path $P$. Remember that in this discussion it is understood that all paths have the same endpoints $\xvec_0$ and $\xvec$. This means that the space of paths can be broken up into *homotopy classes*, that is, a homotopy class indexed by $n$ is the set of all paths that have the same winding number. The integer $n$ takes on all values, positive, negative and zero. We denote the $n$-th homotopy class by ${\cal C}_n$.

Then the path integration can be written,

:::{math}
:label: eq-magfield-63
\int_{\\text{\sevenrm all \scriptstyle P}} dP = \sum_{n=-\infty}^{+\infty} \int_{P\in {\cal C}_n} dP.
:::

As for the integrand, it can be written

:::{math}
:label: eq-magfield-64
e^{(i/\hbar)S[P]} = e^{(i/\hbar)S_free[P]}\, e^{(i/\hbar)S_0} \, e^{inq\Phi/\hbar c}.
:::

Of the three factors shown, the middle one does not depend on $P$ at all, while the last depends only on the homotopy class. Thus, overall the path integral can be written

:::{math}
:label: eq-magfield-65
K(\xvec,\xvec_0,t) = e^{iS_0/\hbar} \sum_{n=-\infty}^{+\infty} e^{inq\Phi/\hbar c} \int_{P\in{\cal C}_n} dP \, e^{(i/\hbar)S_free[P]}.
:::

We see that the different homotopy classes contribute to the path integral with different overall phases, which are proportional to the winding number $n$ of the homotopy class. On the other hand, if there is no magnetic field in the solenoid, then the propagator is

:::{math}
:label: eq-magfield-66
K(\xvec,\xvec_0,t)= \int_{\\text{\sevenrm all \scriptstyle P}} dP\, e^{(i/\hbar)S_free[P]} = \sum_{n=-\infty}^{+\infty} \int_{P\in {\cal C}_n} dP\, e^{(i/\hbar)S_free[P]},
:::

a similar expression but without the extra phases attached to the homotopy classes. Thus, the homotopy classes interfere with each other in a different manner when there is a magnetic field in the solenoid.

Now notice that if the particle is an electron with $q=-e$ then the extra phases can be written

:::{math}
:label: eq-magfield-67
e^{inq\Phi/\hbar c} = e^{-ine\Phi/\hbar c} =e^{-2n\pi i \Phi/\Phi_0},
:::

where $\Phi_0=2\pi\hbar e/c=he/c$ is the flux quantum (see \secrmagfield-6). Thus if the magnetic flux in the solenoid is an integer multiple of a flux quantum then all these phase factors become unity, and the propagator becomes

:::{math}
:label: eq-magfield-68
K(\xvec,\xvec_0,t) = e^{iS_0/\hbar} \sum_{n=-\infty}^{+\infty} \int_{P\in{\cal C}_n} dP \, e^{(i/\hbar)S_free[P]}= e^{iS_0/\hbar} \int_{\\text{\sevenrm all \scriptstyle P}} dP\, e^{(i/\hbar)S_free[P]},
:::

which is the same as the propagator {eq}`eq-magfield-66` in the absence of a magnetic field except for the overall factor $e^{iS_0/\hbar}$. As for the latter, it can be eliminated by a gauge transformation. See Prob. {ref}`prob-pathint-4`.

Altogether, we conclude that the magnetic field in the solenoid, where the particle never goes, influences both the energy eigenfunctions and the propagator of a charged particle in the exterior region.

Now we may return to the question, does the vector potential $\Avec$ have effects in quantum mechanics that are not gauge-invariant, that is, effects that cannot be expressed purely in terms of $\Bvec$? The answer is no, since the extra phases that occur in the Aharonov-Bohm effect are expressed purely in terms of the flux $\Phi$ in the solenoid, which is gauge invariant.

:::{figure} images/magfield-fig10.png
:label: fig-magfield-10
:width: 80%

A solenoid carrying magnetic flux $\Phi$ lies just behind the slitted screen of a double slit experiment. A plane wave of electrons is incident upon the slitted screen. The solenoid causes a phase relative shift of $2\pi\Phi/\Phi_0$ between the two paths joining the two slits to a point on the detection screen, where $\Phi_0$ is a flux quantum.
:::

So far we have merely shown that the energy eigenfunctions and the propagator in the exterior region depend on the flux in the solenoid. What difference does this make physically? One answer is given by an idealized double slit experiment, as illustrated in {ref}`fig-magfield-10`. A plane wave is incident upon a screen with two slits, behind which an lies a solenoid carrying magnetic flux $\Phi$. The solenoid introduces a relative phase shift of $2\pi\Phi/\Phi_0$ between the two paths from the two slits to the detection screen. Thus, as the flux in the solenoid is changed, the interference pattern moves to the right or left under the envelope (the dotted line), returning to its original shape after $\Phi$ has increased by an integer multiple of a flux quantum $\Phi_0=hc/e$. Experiments along these lines have been carried out (see R. G. Chambers, *Phys.\ Rev.\ Lett.*\ **5**, 3(1960)) with results that agree with the predictions of quantum mechanics.

(sec-magfield-8)=

## Magnetic Monopoles

A magnetic monopole is a hypothetical particle that produces a magnetic field just like the Coulomb electric field of an ordinary charged particle. In spite of intensive searches, magnetic monopoles have never been observed. Nevertheless, they are much beloved by theorists, who find them interesting for many reasons. One is the argument first given by Dirac, which explains the quantization of electric charge, under the assumption that at least one magnetic monopole exists in the universe.

The quantization of electric charge refers to the fact that the charges of all known charged particles are integer multiples of the charge on the proton, what we denote by $e$ in this course (with $e>0$). In saying this we understand that we are talking about particles that can exist freely; otherwise, the quantum of charge is $e/3$, carried by quarks. The accuracy to which this is known is very high. For example, if the positive charge on a proton and the negative charge on an electron did not exactly cancel one another, then a hydrogen atom would carry a net charge, a small one if the difference were small. This would mean that a hydrogen atom would accelerate in a uniform electric field. No such response is detected experimentally.

The quantization of charge is closely related to the conservation of charge. For example, a neutron decays into a proton, an electron, and an antineutrino. If the neutron and neutrino are genuinely neutral, and if the charge on the proton is not equal and opposite to the charge on the electron, then charge is not conserved in the reaction. It is known experimentally that the charge on the neutron is very close to zero.

Modern theoretical ideas about the quantization of charge relate it to the compactness of gauge groups, which in turn is related to ideas about extra (“compactified”) dimensions. While such ideas are very appealing, it cannot be said that they are well supported experimentally. In this we present the argument of Dirac for quantization of charge, based on magnetic monopoles.

We assume our monopole is infinitely massive and placed at the origin of the coordinates. The magnetic field has the form of a Coulomb field,

:::{math}
:label: eq-magfield-69
\Bvec(\xvec) = k {\xvec \over r^3},
:::

where $k$ is the strength of the monopole. This magnetic field satisfies

:::{math}
:label: eq-magfield-70
\del\cdot\Bvec = 4\pi k \,\delta(\xvec),
:::

so the usual Maxwell equation $\del\cdot\Bvec=0$ is only valid for $r>0$. Exactly at $r=0$ we have a $\delta$-function singularity.

We will be interested in studying the quantum mechanics of a particle of charge $q$ in the field of the monopole {eq}`eq-magfield-69`. The Hamiltonian involves the vector potential $\Avec$, so we must find an $\Avec$ such that $\Bvec$ of {eq}`eq-magfield-69` can be written as $\Bvec=\del\cross\Avec$. By writing out the curl in spherical coordinates (see {ref}`sec-vecident-4`), it is possible to uncurl $\Bvec$ and obtain $\Avec$. The answer is not unique, but one that readily suggests itself is

:::{math}
:label: eq-magfield-71
\Avec_N = {k(1-\cos\theta)\over r\sin\theta}\, {\hat{\boldsymbol{\phi}}}.
:::

The vector potential is purely in the $\phi$~direction. Notice that while the magnetic field $\Bvec$ has full rotational symmetry, this vector potential has only rotational symmetry about the $z$-axis.

:::{figure} images/magfield-fig11.png
:label: fig-magfield-11
:width: 80%

The vector potential $\Avec_N$ is well behaved in the northern hemisphere, and has a singularity at the south pole (a string on the negative $z$-axis).
:::

:::{figure} images/magfield-fig12.png
:label: fig-magfield-12
:width: 80%

The vector potential $\Avec_S$ is well behaved in the southern hemisphere, and has a singularity at the north pole (a string on the positive $z$-axis).
:::


The $\sin\theta$ in the denominator of {eq}`eq-magfield-71` suggests a singularity when $\theta=0$ or $\theta=\pi$. Actually, there is no singularity at $\theta=0$, because the factor $1-\cos\theta$ goes to zero faster than $\sin\theta$ as $\theta\to0$. But there is indeed a divergence as $\theta\to\pi$; the magnitude of the vector potential diverges, and its direction becomes undefined (because ${\hat{\boldsymbol{\phi}}}$ is undefined when $\theta=\pi$). Thus there is a singularity of the vector potential $\Avec_N$ on the negative $z$-axis, which is called the *string* of the monopole. See {ref}`fig-magfield-11`, where the string is indicated by the heavy wavy line. It is really a misnomer to call this the “string of the monopole”; the magnetic field $\Bvec$ itself is perfectly well behaved on the negative $z$-axis. It would be better to call it the “string of the vector potential.”

Vector potentials are not unique, but can be changed by a gauge transformation. It is interesting to use a gauge scalar [see {eq}`eq-tevolut-81a`] that is proportional to $\phi$, the azimuthal angle. Note that

:::{math}
:label: eq-magfield-72
\del\phi = {{\hat{\boldsymbol{\phi}}} \over r\sin\theta},
:::

in spherical coordinates. For example, subtracting the gradient of $2k\phi$ from $\Avec_N$ we obtain another vector potential (a different choice of gauge),

:::{math}
:label: eq-magfield-73
\Avec_S = \Avec_N - \del(2k\phi) =-{k(1+\cos\theta)\over r \sin\theta} \,{\hat{\boldsymbol{\phi}}}.
:::

This vector potential is well behaved on the negative $z$-axis but has a string on the positive $z$-axis. See {ref}`fig-magfield-12`.

We see that it is possible to move the string by performing a gauge transformation. Is it possible to get rid of the string altogether by a gauge transformation? That is, does there exist a vector potential for the magnetic field {eq}`eq-magfield-69` that is regular everywhere (except of course at $r=0$, where $\Bvec$ itself is singular)?

The answer is no, as can be proved by contradiction. Suppose there exists a vector potential $\Avec$ that is regular everywhere except at $r=0$, such that the monopole field {eq}`eq-magfield-69` is given by $\del\cross\Avec$. We imagine a small disk, really the end cap of a sphere, through which we wish to compute the magnetic flux, as in the first part of {ref}`fig-magfield-13`. The flux $\Phi$ is computed by

:::{math}
:label: eq-magfield-74
\Phi = \oint \Avec\cdot d\ellvec,
:::

where the direction of integration around the boundary of the disk is shown by the arrow in the figure. Now we allow the disk to grow into the surface of a sphere, which gradually swallows the monopole. In the end the flux intercepted by the surface approaches $4\pi k$, which can be computed by using {eq}`eq-magfield-70` and Gauss's law, while the circle around the boundary of the surface shrinks. As it does so, the integral {eq}`eq-magfield-74` must approach zero, if $\Avec$ is smooth as assumed, since the distance over which the integration takes place is going to zero. Thus we reach a contradiction, $4\pi k=0$, and the assumption about the existence of a vector potential that is smooth everywhere in the region $r>0$ must be wrong. The vector potentials of magnetic monopoles inevitably have strings.

:::{figure} images/magfield-fig13.png
:label: fig-magfield-13
:width: 80%

A surface swallowing a monopole. As it does so, the magnetic flux captured by the surface approaches $4\pi k$, while the contour of integration around the boundary of the surface approaches zero (at the right of the figure).
:::

If we examine the vector potentials $\Avec_N$ and $\Avec_S$ over a sphere centered on the monopole, we see that $\Avec_N$ is regular (well behaved) over the northern hemisphere, and can be continued across the equator into the southern hemisphere, but not as far as the south pole. We call $\Avec_N$ “north regular gauge.” As for $\Avec_S$, it is regular over the southern hemisphere and can be continued across the equator into the northern hemisphere, but not as far as the north pole. We call $\Avec_S$ “south regular gauge.” Thus we can create two regions that overlap in a strip around the equator, with each vector potential regular in its own region. See {ref}`fig-magfield-14`.

:::{figure} images/magfield-fig14.png
:label: fig-magfield-14
:width: 80%

The regions $N$, $S$, of definition of $\Avec_N$ and $\Avec_S$ overlap at the equator $E$.
:::

To avoid singularities we must solve the Schr\"odinger equation in patches. Suppose we do this, and find solutions $\psi_N$ and $\psi_S$ in the regions in which $\Avec_N$ and $\Avec_S$ are regular. In the overlap region, the solutions must be related by the gauge transformation. See {eq}`eq-tevolut-82`, which in the present context becomes

:::{math}
:label: eq-magfield-75
\psi_N(\xvec) = e^{2iqk\phi/\hbar c} \psi_S(\xvec),
:::

where we have used $f=2k\phi$ for the gauge scalar. This equation applies around the equatorial strip.

The solution of the Schr\"odinger equation must be continuous, otherwise the first derivative of $\psi$ would have a $\delta$-function and the second derivative in the kinetic energy term would have a $\delta'$-function that could not be cancelled by any other term in the equation. But both $\psi_N$ and $\psi_S$ can be continuous in the overlap region only if the coefficient of the azimuthal angle $\phi$ in {eq}`eq-magfield-75` is an integer, that is, if

:::{math}
:label: eq-magfield-76
{2qk \over \hbar c} = n.
:::

But this implies

:::{math}
:label: eq-magfield-77
q = \Bigl({\hbar c \over 2k}\Bigr)n,
:::

or the charge on the particle must be an integer multiple of a fundamental unit, proportional to the inverse of the charge on the monopole. Thus, if there exists even one monopole in the universe, the consistency of quantum mechanics requires the quantization of charge.

Dirac's argument is fundamentally topological, and in modern theoretical treatments is expressed in terms of cohomology, fiber bundles and characteristic classes. Such topological concepts have assumed a prominent role in modern theoretical physics.

\problems

(prob-magfield-1)=

**Problem \prbdmagfield-1.} Consider a spinless electron moving in the uniform magnetic field $\Bvec=B{\hat{\mathbf{z}}}$.  Let $n$ be the quantum number of $H_\perp$ (the Landau level), and let $P_3$ be the eigenvalue of operator ${\hat P.** 

To find wave functions we need a third operator, in addition to }$H_\perp$ and ${\hat P}_3$ and commuting with them, to form a complete set of commuting operators. The choice $\hat X$ for the third operator was discussed above. That choice is useful for making the translational invariance in the $y$-direction manifest. Here we make a different choice for the third operator, namely,

:::{math}
:label: eq-magfield-78
L = L_z = xp_y -yp_x,
:::

the angular momentum (or, rather, its $z$-component), which makes the rotational invariance about the $z$-axis manifest.

{eq}`eq-magfield-78` is the usual definition of angular momentum, but it is only conserved if the vector potential is chosen to be rotationally invariant. Let us choose the gauge

:::{math}
:label: eq-magfield-79
\Avec = {B \over 2} (-y{\hat{\mathbf{x}}} + x{\hat{\mathbf{y}}}).
:::

If you plot the vector field $\Avec$ in the $x$-$y$ plane, or transform it to polar coordinates, you will see that it is invariant under rotations about the $z$-axis.

Since $A_z=0$, the kinetic momentum in the $z$-direction $P_3=mv_z$ is the same as the canonical momentum $p_z$. Thus we will henceforth write $p_z$ instead of $P_3$.

\problempart{(a)} Express $L$ in terms of variables $(X,Y,v_x,v_y)$ and then in terms of $(Q_1,P_1,Q_2,P_2)$. Show that it commutes with both $H_\perp$ and ${\hat P}_3$, so that all three operators, $(L,H_\perp,{\hat P}_3)$ commute with one another. Let the eigenvalues of $L$ be written $m\hbar$. Show that $m$ is an integer. For given $n$, what are the allowed values of $m$?

Actually, a somewhat more convenient operator for the third member of the complete set is

:::{math}
:label: eq-magfield-80
K= {1\over 2} (Q_1^2 + P_1^2),
:::

another harmonic oscillator. Let $k$ be the usual harmonic oscillator quantum number for this oscillator. Express $m$ as a function of $n$ and $k$. Henceforth let us take $(K,H_\perp,{\hat P}_3)$ as the complete set of commuting observables.

\problempart{(b)} Now we work on finding the wave functions $\psi(x,y,z)$ that are simultaneous eigenfunctions of $(K,H_\perp,{\hat P}_3)$. For the rest of this problem, let us choose units so that $m=\omega=\hbar=1$, which simplifies the algebra and which entails no loss of physics since physical units can always be restored in the final formulas.

First show that an eigenfunction $\psi(x,y,z)$ of ${\hat p}_z$ with eigenvalue $p_z$ has the form

:::{math}
:label: eq-magfield-81
\psi(x,y,z) = \phi(x,y) e^{ip_z z}.
:::

This is the easy operator.

Choosing $\phi(x,y)$ so that the function is also an eigenfunction of both $K$ and $H_\perp$ takes more work. We first work on the double ground state $k=0$, $n=0$. Introduce annihilation and creation operators $a$, $a^\dagger$ for oscillator $K$ and another pair $b$, $b^\dagger$ for oscillator $H_\perp$. The double ground state wave function must be annihilated by both $a$ and $b$. That is, we want

:::{math}
:label: eq-magfield-82
(a\phi_{00})(x,y) = (b\phi_{00})(x,y) = 0.
:::

Write out $a$ and $b$ as differential operators in $x$ and $y$.

The subsequent analysis is simplified if we use complex coordinates $w$, $\bar w$ in the $x$-$y$ plane, defined by

:::{math}
:label: eq-magfield-83
\begin{aligned}
w &={1\over\sqrt{2}}(x+iy), \\
\bar w &= {1\over\sqrt{2}}(x-iy), \\

\end{aligned}
:::

so that

:::{math}
:label: eq-magfield-84
\begin{aligned}
\pop{}{w} &= {1\over\sqrt{2}} \Bigl( \pop{}{x} -i\pop{}{y} \Bigr), \\
\pop{}{\bar w} &= {1\over\sqrt{2}} \Bigl( \pop{}{x} +i\pop{}{y} \Bigr). \\

\end{aligned}
:::

Transform the differential operators for $a$ and $b$ to the $w$, $\bar w$ coordinates, and solve {eq}`eq-magfield-82` for $\phi_{00}(x,y)$. Normalize it.

\problempart{(c)} Now write out differential operators in the $w$, $\bar w$ coordinates for the creation operators $a^\dagger$ and $b^\dagger$. Use them to obtain the normalized wave function $\phi_{kn}$ for $k=0$, $n>0$.

\problempart{(d)} Use the Rodriguez formula for the associated Laguerre polynomials,

:::{math}
:label: eq-magfield-85
L^m_n(x) = {1\over n!} e^x x^{-m} {d^n\over dx^n} (x^{n+m} e^{-x})
:::

[see Abramowitz and Stegun, Eq.~(22.11.6)], to express the normalized wavefunction $\phi_{kn}(x,y)$ for any values of $k$ and $n$ in terms of associated Laguerre polynomials. Hint: Use the identity,

:::{math}
:label: eq-magfield-86
\Bigl( \pop{}{w} - {\bar w\over 2} \Bigr) e^{w\bar w/2} f(w,\bar w) = e^{w\bar w/2} \pop{}{w} f(w,\bar w),
:::

where $f$ is any function.

(prob-magfield-2)=

**Problem \prbdmagfield-2..** 

:::{math}
:label: eq-magfield-87
\Bvec(\xvec)=g{\xvec\over |\xvec|^3},
:::

where $g$ is a constant. Although monopoles have never been observed, nevertheless people have carried out experiments to search for them. In such experiments, it is important to know the behavior of ordinary matter in a monopole field, in order to recognize the signatures a monopole would make in experimental apparatus.

\problempart{(a)} Write down Newton's laws for the electron motion. You may use the abbreviation,

:::{math}
:label: eq-magfield-88
\mu = {eg\over mc}.
:::

To solve these equations of motion, we begin by a search for constants of motion. If it were an electric monopole instead of a magnetic monopole, then we would obviously have four constants of motion: the energy $E$ and angular momentum $\Lvec=m\xvec\cross\vvec$. Show that the usual (orbital) angular momentum vector $\Lvec=m\xvec\cross\vvec$ is not conserved. Show that $L^2$ is conserved, however. This gives you two time-independent constants of motion, $(E,L^2)$, which are not enough to obtain the complete solution. Therefore we must find more constants of motion.

\problempart{(b)} Consider the vector potential,

:::{math}
:label: eq-magfield-89
\Avec={-g\cos\theta \over r\sin\theta} {\hat{\boldsymbol{\phi}}}.
:::

This vector potential is well behaved everywhere except on the $z$-axis (both positive and negative). Verify that this vector potential gives the magnetic field of {eq}`eq-magfield-87`. This vector potential is invariant under rotations about the $z$-axis, that is, the angle $\phi$ is ignorable. Use this vector potential in a classical Lagrangian in spherical coordinates, and use Noether's theorem to obtain another conserved quantity (in addition to $E$, $L^2$). (Noether's theorem says that if a Lagrangian is independent of $q_i$, the $p_i$ is conserved.) Show that this quantity is $L_z$ plus another quantity which you may call $S_z$. Write $J_z=L_z+S_z$, so that $J_z$ is the new conserved quantity. As the notation suggests, interpret $J_z$ as the $z$-component of a vector $\Jvec$, i.e., guess the formula for $\Jvec=\Lvec+\Svec$ (all 3 components). Hint: to help you with the guess, transform $J_z$ to rectangular coordinates. By resorting to Newton's laws, show explicitly that $\Jvec$ is conserved. You now have four time-independent constants of motion, $(E,\Jvec)$. There are only four, because $L^2$ is a function of $\Jvec$; show this.

\problempart{(c)} By playing around with dot products of various vectors and looking for exact time derivatives, find more constants of motion. Use these to find $r^2$ as a function of $t$. Show that the electron can reach the singularity at $r=0$ only if $L^2=0$.

\problempart{(d)} Show that the orbit lies on a cone whose apex is at the origin. Find the opening angle of the cone as a function of $(E,\Jvec)$. Find a vector which specifies the axis of the cone. Assume $L^2\ne0$, and let $t=0$ occur at the point of closest approach. Find the distance of closest approach as a function of $(E,L)$.

\problempart{(e)} Choose the axes so that $\Jvec$ is parallel to the $z$-axis. Find $(r,\theta,\phi)$ as functions of $t$.

\problempart{(f)} The solution of this problem was first carried out by H.~Poincar\'e, *Compt.\ Rend.*\ **123**, 530(1896). Poincar\'e pointed out that the orbit is a geodesic on the cone, since the force is always orthogonal to the cone. This follows since the tangent plane to the cone is spanned by the velocity vector and the radius vector ${\hat{\mathbf{r}}}$, and for the monopole field the magnetic force is orthogonal to both. But a cone is a flat surface, as shown by the fact that it can be unrolled into a plane.

Take a piece of plain white paper, and draw a straight line on it. This line is a geodesic. Now roll the paper into a cone. Try cones of different opening angles and different relations to the straight line. The straight line now appears as the orbit of an electron in the field of a monopole. You can see how it spirals in on the cone, reaching a point of closest approach, and then sprirals out.

(prob-magfield-3)=

**Problem \prbdmagfield-3..** 

To simplify the algebra, choose units so that $m=c=\hbar=1$, and let $eB = \omega$ and $eE = \epsilon$ (here $\epsilon$ is not necessarily small). Notice that $\omega$ is the frequency of the circular motion in the absence of an electric field.

The classical motion is along a circle that “drifts” in the $y$-direction with velocity,

:::{math}
:label: eq-magfield-90
v_d= c{E\over B}={\epsilon\over\omega}.
:::

At a certain point in the calculation you may find this a convenient substitution.

\problempart{(a)} Express the Hamiltonian as a function of the operators $({\hat X},{\hat Y},{\hat v}_x,{\hat v}_y)$. In the case of the uniform magnetic field (without $\Evec$) we found that $H$ commuted with any function of $\hat X$ or $\hat Y$. What functions of $\hat X$ and $\hat Y$ does $H$ commute with now that we have an electric field? What is the energy of a state that is an eigenstate of both $\hat X$ and $H$? Express the energy in terms of some reasonable quantum number(s).

\problempart{(b)} Choose a gauge $\Avec = Bx{\hat{\mathbf{y}}}$, where ${\hat{\mathbf{y}}}$ is the unit vector in the $y$-direction. Let ${\hat X}\psi(x,y) = X\psi(x,y)$. Find the most general wave function $\psi(x,y)$ that satisfies this equation.

\problempart{(c)} Now let $H\psi(x,y)=K\psi(x,y)$, where $K$ is the energy, and where $\psi$ has the form determined in part (b). Express the solution $\psi(x,y)$ in terms of $u_n(x)$, defined to be the normalized harmonic oscillator eigenfunction for quantum number $n$.

\problempart{(d)} Compute the $y$-component $J_y$ of the probability flux, properly interpreted as a particle flux since the wave function is not normalizable. Integrate this flux over the line $y=const$ to get the number of particles/unit time crossing this line. Notice the relation to the drift velocity.

(prob-magfield-4)=

**Problem \prbdmagfield-4..** 

\problempart{(a)} Consider an electron moving in the magnetic field $\Bvec = B{\hat{\mathbf{z}}}$. We ignore the spin of the electron (we treat it as if it were a spinless particle), and we ignore the motion in the $z$-direction. Thus, we have a 2-dimensional problem, in the $x$-$y$ plane.

In this problem I recommend that you use units such that $m=\hbar=\omega=1$, where $\omega$ is the gyrofrequency [see {eq}`eq-magfield-12`]. Also, use the vector potential,

:::{math}
:label: eq-magfield-91
\Avec={B\over2}\begin{pmatrix}-y \\ x \\ 0 \\\end{pmatrix} ={1\over2} \Bvec\cross\rvec.
:::

As in the notes above I recommend that you put hats on the symbols $x$, $y$, $v_x$, $v_y$, $p_x$, $p_y$, $X$ and $Y$ when operators are intended, and omit the hats when $c$-numbers or classical values are intended. For other operators this distinction will not be necessary and you can omit the hats.

The classical guiding center is defined by

:::{math}
:label: eq-magfield-92
X=x-v_y, \qquad Y=y+v_x,
:::

which are dimensionless versions of {eq}`eq-magfield-16`. Also define the operators $a$, $a^\dagger$, $b$ and $b^\dagger$ by

:::{math}
:label: eq-magfield-93
\begin{aligned}
a &= {\Xhat+i\Yhat\over\sqrt{2}}, \qquad a^\dagger = {\Xhat-i\Yhat\over\sqrt{2}}, \\
\Xhat&={a+a^\dagger\over\sqrt{2}}, \qquad \Yhat={a-a^\dagger\over i\sqrt{2}}, \\

\end{aligned}
:::

and

:::{math}
:label: eq-magfield-94
\begin{aligned}
b &= {\vhat_y + i\vhat_x\over\sqrt{2}}, \qquad b^\dagger = {\vhat_y-i\vhat_x\over\sqrt{2}}, \\
\vhat_x&={b-b^\dagger \over i\sqrt{2}}, \qquad \vhat_y={b+b^\dagger\over\sqrt{2}}. \\

\end{aligned}
:::

It helps to notice that $X$ and $v_y$ are like $q$'s, while $Y$ and $v_x$ are like $p$'s [see {eq}`eq-magfield-22`].

Let $\psi_{00}(x,y)$ be the wave function such that

:::{math}
:label: eq-magfield-95
a\psi_{00}=b\psi_{00}=0.
:::

Find the normalized wave function $\psi_{00}(x,y)$. Hint: I suggest you work with $(a+b)\psi_{00}=0$ and $(a-b)\psi_{00}=0$. We will denote the ket corresponding to the wave function $\psi_{00}(x,y)$ by $\ket{00}$.

We will take the complete set of commuting observables for this problem to be $(K,H)$, where $H$ is the Hamiltonian and

:::{math}
:label: eq-magfield-96
K={1\over2}(\Xhat^2+\Yhat^2).
:::

With this understanding, explain the meaning of the 00-subscript on $\psi_{00}(x,y)$.

\problempart{(b)} Define operators,

:::{math}
:label: eq-magfield-97
T_1(X,Y) = \exp[i(Y\Xhat-X\Yhat)], \qquad T_2(v_x,v_y) = \exp[i(v_x\vhat_y-v_y\vhat_x)].
:::

Explain why $T_1(X,Y)$ and $T_2(v_x,v_y)$ commute with one another.

Letting $\psi(x,y)$ be an arbitrary wave function, work out

:::{math}
:label: eq-magfield-98
[T_1(X,Y)\psi](x,y) \qquad and \qquad [T_2(v_x,v_y)\psi](x,y).
:::

It helps to notice that both $T_1$ and $T_2$ can be factored into commuting operators, each of which is either a pure configuration space displacement, or one in momentum space. If you use this fact, explain why the factors commute.

:::{figure} images/magfield-fig15.png
:label: fig-magfield-15
:width: 80%

When the electron emits a photon the recoil causes both the velocity and guiding center position to change. The actual position does not.
:::

\problempart{(c)} If the initial conditions for the classical motion are $v_x(0)=0$, $v_y(0)=v_0$, find the classical solutions $v_x(t)$, $v_y(t)$.

\problempart{(d)} Let $\psi(x,y,t)$ be a solution of the time-dependent Schr\"odinger equation. We are interested in the solution for which the initial condition $\psi(x,y,0)$ is the wave function corresponding to the state

:::{math}
:label: eq-magfield-99
T_2(0,v_0)\ket{00},
:::

with $v_x=0$ and $v_y=v_0$. That is,

:::{math}
:label: eq-magfield-100
\psi(x,y,0) = \matrixelement{x,y}{T_2(0,v_0)}{00}.
:::

Find $\psi(x,y,t)$.

Hint: you may find the following definitions convenient:

:::{math}
:label: eq-magfield-101
w={v_y+iv_x\over \sqrt{2}}, \qquad {\bar w} = {v_y-iv_x\over\sqrt{2}},
:::

and

:::{math}
:label: eq-magfield-102
Z={X+iY\over\sqrt{2}}, \qquad {\bar Z} = {X-iY\over\sqrt{2}}.
:::

Finally, at some point you may wish to write

:::{math}
:label: eq-magfield-103
w(t)={v_y(t)+iv_x(t)\over\sqrt{2}},
:::

where $v_x(t)$ and $v_y(t)$ were determined in part~(c).

\problempart{(e)} Suppose the electron is in the state $\ket{00}$ at times $t<0$. It emits a photon at $t=0$ whose momentum is in the negative $y$-direction, causing the expectation value of the velocity of the electron, just after the photon is emitted, to be $\xpecval{(\vhat_x,\vhat_y)}=(0,v_0)$. Find the probability $P_n$ that for $t>0$ the electron is in Landau level $n$. Express your answer in ordinary (not dimensionless) units. If you have done Prob. {ref}`prob-harmosc-4`, compare your answer to the answer of that problem.

Hints: Note that the impulse delivered by the photon changes both the velocity and the guiding center position, as is necessary for consistency with {eq}`eq-magfield-92` since the particle position does not change. This is also obvious from a picture (see {ref}`fig-magfield-15`). Thus, the state of the system just after the photon is emitted is *not* the same as the initial condition in part~(d).
