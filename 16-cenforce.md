---
title: "16. Central Force Motion"
---
(ch-cenforce)=

# 16. Central Force Motion

(sec-cenforce-1)=

## Introduction

In these notes we provide an introduction to central force motion, including the examples of the free particle, the rigid rotor and diatomic molecules. We will take up the hydrogen atom in {ref}`ch-hydrogen`.

(sec-cenforce-2)=

## The Radial Schr\"odinger Equation

Initially we imagine a force center at the origin of a system of coordinates creating a force field described by a potential $V(r)$. The potential is a function only of the radius $r$ and is invariant under rotations. A particle moves in this force field.

:::{figure} images/cenforce-fig01.png
:label: fig-cenforce-1
:width: 80%

If the object creating a central force field is very massive, we may treat the motion of a particle in the field as a one-body problem.
:::

The force is presumably created by some particle or physical object. We assume that its mass is infinite (or much larger than that of the particle in orbit) so that the frame attached to it is an inertial frame. Sometimes this is not a bad approximation, for example, in atoms where the nucleus is much heavier than the electrons. If this is the case, then we obtain a one-body problem for the motion of the particle, which is described by the Hamiltonian

:::{math}
:label: eq-cenforce-1
H={p^2\over 2m} + V(r).
:::

We assume the particle is spinless, or that spin effects can be neglected. Thus the Hilbert space for the particle is the space of wave functions $\psi(\xvec)$. In {ref}`ch-orbamsph`\ we developed the theory of the rotation operators $U(\Rmat)$ and angular momentum operators $\Lvec$ that act on this space. We also found the standard angular momentum basis, which consists of radial wave functions times $Y_{\ell m}$'s.

The Hamiltonian {eq}`eq-cenforce-1` possesses rotational symmetry, that is, it commutes with all rotation operators $U(\Rmat)$, whose action on wave functions is given by {eq}`eq-orbamsph-13`. Without going into details, this is obvious from the fact that the kinetic energy is proportional to $p^2 = \pvec\cdot\pvec$, the dot product of two vectors, while the potential energy is a function of $r=\sqrt{r^2}$, where $r^2 = \xvec\cdot\xvec$, another dot product of two vectors. Since the dot product of classical ($c$-number) vectors is invariant under classical rotations, we expect the same for vectors of quantum operators. We will explore this question in more detail in {ref}`ch-wigeck`, but for now the basic line of reasoning should be clear. If there is any doubt, one can explicitly verify the commutators

:::{math}
:label: eq-cenforce-2
[\Lvec,H]=0,
:::

which show that

:::{math}
:label: eq-cenforce-3
[U(\Rmat),H]=0
:::

since $U(\Rmat)$ is a function of $\Lvec$. Conversely, if an operator commutes with all rotations $U(\Rmat)$, then it commutes in particular with infinitesimal rotations, and therefore with the three components of $\Lvec$.

As a result, $H$ commutes with the commuting operators $L^2$ and $L_z$, so the three operators $(H,L^2,L_z)$ possess a simultaneous eigenbasis. From {ref}`ch-orbamsph`\ we already know the general form of a simultaneous eigenfunction of $L^2$ and $L_z$; it is

:::{math}
:label: eq-cenforce-4
\psi(r,\theta,\phi) = R(r) Y_{\ell m}(\theta,\phi),
:::

where $R(r)$ is an arbitrary radial wave function. See {eq}`eq-orbamsph-42`. By demanding that this wave function also be an eigenfunction of $H$, we can determine the radial wave function $R(r)$.

To do this we substitute {eq}`eq-cenforce-4` into the Schr\"odinger equation for the Hamiltonian {eq}`eq-cenforce-1`,

:::{math}
:label: eq-cenforce-5
\Bigl[ {p^2\over 2m} + V(r)\Bigr]\psi = E\psi.
:::

Working on the kinetic energy first and using {eq}`eq-orbamsph-30`, we have

:::{math}
:label: eq-cenforce-6
{p^2\over 2m} \psi = -{\hbar^2 \over 2m} \del^2 \psi =-{\hbar^2 \over 2m} {1\over r^2} \pop{}{r} \Bigl( r^2 \frac{\partial \psi}{\partial r}\Bigr) + {L^2 \over 2mr^2} \psi.
:::

But if $\psi$ has the form {eq}`eq-cenforce-4`, then $L^2$ acting on the $Y_{\ell m}$ part brings out $\ell(\ell+1)\hbar^2$, and all terms have a common factor of $Y_{\ell m}$. This also applies to the potential energy and total energy terms in the Schr\"odinger equation, so the common factor of $Y_{\ell m}$ can be cancelled. We obtain an equation for the radial function $R(r)$ alone,

:::{math}
:label: eq-cenforce-7
\boxed{-{\hbar^2\over 2m} {1\over r^2} \dod{}{r} \Bigl( r^2 \dod{R}{r}\Bigr) + U(r)R(r) = E R(r),}
:::

where $U(r)$ is the *effective potential*,

:::{math}
:label: eq-cenforce-8
U(r) = {\ell(\ell+1)\hbar^2 \over 2mr^2} + V(r).
:::

The effective potential is the sum of the *centrifugal potential* (the first term) and the true potential, $V(r)$. The centrifugal potential is physically the angular part of the kinetic energy, what could be written classically as

:::{math}
:label: eq-cenforce-9
{m\over 2}(r^2{\dot\theta}^2 + r^2\sin^2\theta {\dot\phi}^2) = {L^2 \over 2mr^2}.
:::

Mathematically, however, it looks like a potential and it is usually treated that way. The first term of Eq.~(7) is the radial part of the kinetic energy, what could be written classically as $(m/2){\dot r}^2$. {eq}`eq-cenforce-7` is called the *radial Schr\"odinger equation*, or, as we shall call it, version one of the radial Schr\"odinger equation.

Version two of the radial Schr\"odinger equation is created by making the substitution

:::{math}
:label: eq-cenforce-10
f(r) = rR(r),
:::

which after a little algebra results in

:::{math}
:label: eq-cenforce-11
\boxed{-{\hbar^2\over 2m} {d^2 f(r) \over dr^2} +U(r)f(r) = Ef(r).}
:::

This version is easy to remember because it is almost the same as the one-dimensional Schr\"odinger equation (usually written in terms of some variable $x$ with $-\infty < x < +\infty$). The only differences are the presence of the centrifugal potential in the radial Schr\"odinger equation and the fact that $r$ lies in the range $0\le r < \infty$.

It is reasonable to define the normalization of the radial wave function $R(r)$ by the integral,

:::{math}
:label: eq-cenforce-12
\int_0^\infty r^2\,dr\, |R(r)|^2,
:::

because that is the radial part of the three-dimensional normalization integral

:::{math}
:label: eq-cenforce-13
\int d^3\xvec \, |\psi(\xvec)|^2 = \int_0^\infty r^2\,dr\int d\Omega \, |\psi(r,\theta,\phi)|^2
:::

when $\psi$ has the form {eq}`eq-cenforce-4`. Notice that this implies the normalization of the version two radial function $f(r)$,

:::{math}
:label: eq-cenforce-14
\int_0^\infty dr\, |f(r)|^2,
:::

which is the usual one for the one-dimensional Schr\"odinger equation apart from the range of integration.

(sec-cenforce-3)=

## Separation of Variables

The usual way of deriving the radial Schr\"odinger equation in introductory courses is to separate the three-dimensional Schr\"odinger equation in spherical coordinates. The results are the same as in \secrcenforce-2. The method of separation of variables, when it works, is a powerful one for solving multidimensional partial differential equations that sometimes leads to exact solutions that would be difficult to find otherwise. Most wave equations are not separable in any coordinate system, however. Fortunately, many common model problems are separable in at least one coordinate system, while many others are close to a separable system and can be treated by perturbation theory. If this is not so, then usually numerical techniques will be required to find solutions. Some systems are separable in more than one coordinate system, for example, the Schr\"odinger equation for all central force problems in three dimensions is separable in spherical coordinates, while the free particle is also separable in rectangular coordinates and the hydrogen atom is also separable in confocal parabolic coordinates.

In all cases, separability is related to the existence of constants of the motion, that is, operators that commute with the Hamiltonian that are related to some symmetry of the system. If the Schr\"odinger equation for some multidimensional system is not separable in any coordinate system, it probably means that the system does not possess any continuous symmetries at all. It may possess discrete symmetries, such as parity and time reversal, but these do not lead to separability of the wave equation in any coordinates. If the Schr\"odinger equation is separable in more than one coordinate system, it means that the system respects a larger symmetry group than that needed to ensure the solvability of the problem at all. For example, all central force problems in quantum mechanics are separable in spherical coordinates, which corresponds to the $SO(3)$ symmetry of the system under rotations. But the free particle is also invariant under translations, so the free particle Schr\"odinger equation is also separable in rectangular coordinates, while the hydrogen atom, which possesses an $SO(4)$ symmetry group, is separable also in confocal parabolic coordinates.

Thus, the success of the method of separation of variables is due to some symmetry of the system, although this is usually not obvious when we apply the method. In this course we are emphasizing the symmetries and their impact on our understanding of the quantum mechanics, so we have approached the solution of several problems by studying the symmetry operators first and then studying the Hamiltonian. For example, in solving the problem of the charged particle in a uniform magnetic field, we diagonalized the operators that commute with the Hamiltonian first, whereupon the Hamiltonian was easy to diagonalize. Also, in central force motion, we diagonalized the operators $L^2$ and $L_z$ first, which led to the standard angular momentum basis, and then we turned our attention to the Hamiltonian (as in this set of notes). This approach leads to the solution of some problems or at least useful results even when the system is not separable. For example, as we shall see in {ref}`sec-transfop-9`, it is possible to understand some important general features of systems with rotational invariance, including very complicated ones, with no need to talk about separating the wave equation (indeed, in some cases we do not even know what the wave equation is, only the symmetries it possesses). We will accumulate several examples of this type before the course is over. In all cases, it turns out to be a good strategy to diagonalize the symmetry operators first, and then to turn our attention to the Hamiltonian.

(sec-cenforce-4)=

## Quantum Numbers and Degeneracies

The radial Schr\"odinger equation is parameterized by $\ell$, with $\ell=0,1,2,\ldots$, because the centrifugal potential depends on $\ell$. Thus we might say that there is a different radial Schr\"odinger equation for each value of $\ell$. The energy eigenvalues for a given value of $\ell$ may be either discrete or continuous. In fact, for potentials $V(r)$ that go to 0 as $r\to\infty$, there will be a continuous spectrum above the continuum threshold at $E=0$. For such potentials and for a given value of $\ell$, there will always be a continuous spectrum, but there may or may not be any bound states. For example, in the case of the deuteron, which is approximately a central force problem involving a proton and a neutron, there is one bound state for $\ell=0$, and none at all for any higher values of $\ell$. (However, spin-dependent forces are important in the case of the deuteron, and the system is not purely a central force problem.)

Assuming there are bound states, let us denote their discrete eigenvalues by $E_{n\ell}$, where $n$ just sequences the levels for a given value of $\ell$, using some scheme. Thus, the energy depends on two quantum numbers, $n$ and $\ell$, but not on $m$. Similarly, the radial wave functions $R(r)$ or $f(r)$ depend on the same two quantum numbers, so we shall write $R_{n\ell}(r)$ or $f_{n\ell}(r)$ to emphasize this. The total wave function is

:::{math}
:label: eq-cenforce-15
\psi_{n\ell m}(r,\theta,\phi) = R_{n\ell}(r) Y_{\ell m} (\theta,\phi).
:::

The radial Schr\"odinger equation shares some features with the usual one-dimensional Schr\"odinger equation, for example, if $f(r)$ vanishes anywhere on the interval $0\le r < \infty$ then the eigenfunctions are nondegenerate. See {ref}`sec-topicsoned-2`. But for realistic potentials $f(r)$ goes as $r^{\ell+1}$ as $r\to0$ (see \secrcenforce-5), so $f(0)=0$ and the radial eigenfunctions are nondegenerate, in both the bound and unbound cases. Of course the bound eigenfunctions also go to zero as $r\to\infty$. We see that the discrete eigenvalues $E_{n\ell}$ are distinct, that is, nondegenerate, for a given value of $\ell$. The nondegeneracy we are referring to here concerns the eigenvalues and eigenfunctions of the radial Schr\"odinger equation for a given value of $\ell$, regarded as a one-dimensional wave equation.

When we consider the three-dimensional Schr\"odinger equation, however, and include the angular quantum numbers, then degeneracies appear. That is, the energies $E_{n\ell}$ are at least $(2\ell+1)$-fold degenerate because they do not depend on $m$. Physically this is due to the fact that the energy of the system does not depend on the orientation. The quantum number $m$ indicates the projection of the angular momentum $\Lvec$ onto the $z$-axis. But if we rotate our system (or the axes), this projection changes. Therefore the energy eigenvalues cannot depend on $m$.

There could be further degeneracies, however. It is possible that some $E_{n\ell}$ could be equal for different values of $\ell$, in which case the degeneracy would be higher than $(2\ell+1)$. For a randomly chosen potential $V(r)$, this is not very likely, since the different radial wave equations for different values of $\ell$ have spectra that are effectively independent of each other. Generically, the degeneracies are just $2\ell+1$ for each $E_{n\ell}$, no more than what is predicted by rotational invariance alone.

For some potentials, however, there are systematic degeneracies among different $E_{n\ell}$ for different values of $n$ and $\ell$. This applies to the Coulomb potential $V(r) = -k/r$ and the harmonic oscillator potential $V(r) = kr^2$. The harmonic oscillator we are referring to is the three-dimensional, isotropic harmonic oscillator. There are no other examples in three-dimensional central force motion. In both cases, the extra degeneracy is due to some extra symmetry that goes beyond ordinary $SO(3)$ (rotational) invariance. For the Coulomb potential, the symmetry group is $SO(4)$, while for the three-dimensional, isotropic harmonic oscillator, it is $SU(3)$. In the case of hydrogen, the extra degeneracy applies only in the electrostatic, spinless, nonrelativistic model, in which the energy levels $E_n$ are proportional to $-1/2n^2$, where $n$ is the principal quantum numbers. The extra degeneracy appears in the fact that these levels are independent of $\ell$. As we add extra physical effects, coming closer to a realistic description of hydrogen, we will see the extra degeneracy gradually disappear. When all physical effects are included, hydrogen, too, has only the $(2j+1)$-fold degeneracy expected on the basis of rotational invariance.

(sec-cenforce-5)=

## Behavior of the Radial Eigenfunctions Near $r=0$

The behavior of the radial wave function for small $r$ is often important in applications. Let us assume the potential is either well behaved at the origin or that if it diverges it does so no faster than $1/r$. This covers the important case of the Coulomb potential. Let us also assume that the wave function $R(r)$ goes as $r^k$ for some power $k$ near $r=0$, something we will write as $R(r) \sim r^k$. This means that $R(r) = ar^k$ for some constant $a\ne0$ plus other terms that go to zero more rapidly than $r^k$ as $r\to0$, or, equivalently,

:::{math}
:label: eq-cenforce-16
\lim_{r\to0} { R(r) \over a r^k} = 1.
:::

Then for small $r$ we have

:::{math}
:label: eq-cenforce-17
-{\hbar^2\over 2m}{1\over r^2} \dod{}{r} \Bigl( r^2 \dod{R(r)}{r}\Bigr) = -a{\hbar^2\over 2m}k(k+1) r^{k-2},
:::

and

:::{math}
:label: eq-cenforce-18
{\hbar^2 \ell(\ell+1) \over 2mr^2}R(r) = a{\hbar^2\over 2m} \ell(\ell+1)r^{k-2}.
:::

As for the term $V(r)R(r)$, it behaves at worst as $r^{k-1}$ as $r\to0$, so it is negligible compared to the terms {eq}`eq-cenforce-17` and {eq}`eq-cenforce-18` as $r\to0$. The same is true for the term $ER(r)$, which behaves as $r^k$ as $r\to0$. The dominant terms in the radial Schr\"odinger equation at small $r$ come from the kinetic energy alone (including the centrifugal potential). Since these terms have to cancel, we have

:::{math}
:label: eq-cenforce-19
k(k+1) = \ell(\ell+1).
:::

This has two solutions,

:::{math}
:label: eq-cenforce-20
k=\ell \qquad and \qquad k=-\ell-1.
:::

The solution $k=-\ell-1$ is not acceptable when $\ell\ge1$, because then $|R(r)|^2$ would have a nonintegrable singularity at $r=0$, that is, the wave function would not be normalizable and there would be an infinite amount of probability in a small neighborhood of $r=0$. As for the case $\ell=0$, this would result in $\psi(r) = a/r$ near $r=0$, which would not satisfy the Schr\"odinger equation at $r=0$ because

:::{math}
:label: eq-cenforce-21
\del^2 \Bigl({1\over r}\Bigr) = -4\pi\delta(\xvec).
:::

That is, the kinetic energy in the 3-dimensional Schr\"odinger equation would contain a $\delta$-function, and for the Schr\"odinger equation to be satisfied, that $\delta$-function would have to be cancelled by another $\delta$-function in the potential energy.

:::{figure} images/cenforce-fig02.png
:label: fig-cenforce-2
:width: 80%

The radial wave function $R(r)$ behaves as $r^\ell$ near $r=0$. It lies down ever more flat against the $r$-axis as $\ell$ increases. This is only the leading behavior of $R(r)$ for small $r$; as $r$ increases, correction terms become important.
:::

Thus, the only possible solution of {eq}`eq-cenforce-19` is $k=\ell$, and we see that the radial wave function has the behavior

:::{math}
:label: eq-cenforce-22
R(r) \sim r^\ell
:::

near $r=0$. The leading behavior depends only on the angular momentum quantum number $\ell$. This is a simple rule that is often important in practice. It means that the radial wave function $R(r)$ lies down more and more flat near $r=0$ as $\ell$ increases (see {ref}`fig-cenforce-2`), and that the probability of finding the particle in some small neighborhood of $r=0$ goes to zero exponentially as $\ell$ increases. This applies, for example, to the probability of finding an atomic electron inside the nucleus.

(sec-cenforce-6)=

## Free Particle

Let us now take the case of the free particle, $V(r)=0$. In this case there is no question of the mass of the object that creates the force field, since there is no force. The free particle Hamiltonian is symmetric under both translations and rotations, so a complete set of commuting observables can be chosen in more than one way. If we choose $(p_x,p_y,p_z)$ as the complete set, then the simultaneous eigenstate is

:::{math}
:label: eq-cenforce-23
\psi(\xvec) = e^{i\kvec\cdot\xvec},
:::

a plane wave with $\pvec=\hbar\kvec$. The energy is given in terms of the momentum eigenvalues by

:::{math}
:label: eq-cenforce-24
E={\pvec^2 \over 2m}.
:::

The spectrum is continuous with $E\ge 0$.

If we choose $(H,L^2,L_z)$ as the complete set, then we must solve the radial Schr\"odinger equation with $V=0$. This is easier in version one, {eq}`eq-cenforce-7`. Expressing the energy in terms of a wave number $k$ by

:::{math}
:label: eq-cenforce-25
E = {\hbar^2 k^2 \over 2m},
:::

and writing $\rho = kr$ for a dimensionless radial variable, the radial Schr\"odinger equation becomes

:::{math}
:label: eq-cenforce-26
{1\over \rho^2} \dod{}{\rho} \Bigl( \rho^2 \dod{R}{\rho}\Bigr) +\Bigl[ 1 -{\ell(\ell+1) \over \rho^2} \Bigr] R=0.
:::

This is the standard differential equation for the spherical Bessel functions. These come in two types, denoted $j_\ell(\rho)$ and $y_\ell(\rho)$ (see Abramowitz and Stegun, Chapter~10).

:::{figure} images/cenforce-fig03.png
:label: fig-cenforce-3
:width: 80%

Spherical Bessel functions $j_\ell(\rho)$ for different values of $\ell$.
:::

:::{figure} images/cenforce-fig04.png
:label: fig-cenforce-4
:width: 80%

Spherical Bessel functions $y_\ell(\rho)$ for different values of $\ell$.
:::


The functions $j_\ell(r)$ are regular at the origin and so are physically acceptable solutions for the free particle. Some examples are plotted in {ref}`fig-cenforce-3`, which clearly shows the behavior $R(r) \sim r^\ell$ near $r=0$. The functions $y_\ell(\rho)$ diverge at the origin and so are not acceptable free particle solutions if the particle is able to reach the origin. They are plotted in {ref}`fig-cenforce-4`. On the other hand, the $y$-type spherical Bessel functions are useful in scattering theory where at large distances from the origin the particle becomes free, and it is desired to represent an arbitrary solution of the Schr\"odinger equation in that region. Since there is no attempt to extend those solutions all the way down to $r=0$, the $y$-type solutions are acceptable (and necessary) in that case.

(sec-cenforce-7)=

## Limiting Forms of the Spherical Bessel Functions

Many problems involving special functions can be solved knowing only the limiting forms for large and small values of the arguments. In the case of the spherical Bessel functions, the limiting forms at small $\rho$ are

:::{math}
:label: eq-cenforce-27
\begin{aligned}
j_\ell(\rho) &\approx {\rho^\ell \over 1\cdot 3 \cdot 5 \ldots (2\ell+1)},
\end{aligned}
:::

:::{math}
:label: eq-cenforce-28
\begin{aligned}
y_\ell(\rho) &\approx -{1 \cdot 3 \cdot 5 \ldots (2\ell-1) \over \rho^{\ell+1}}.
\end{aligned}
:::

See Abramowitz and Stegun, Eqs.~(10.1.2) and (10.1.3). As for $j_\ell(\rho)$, we see the small $r$ rule {eq}`eq-cenforce-22`, to within a constant (which we couldn't have guessed anyway because it is conventional). As for $y_\ell(\rho)$, we see the solution $k=-\ell-1$ of {eq}`eq-cenforce-19` that we rejected earlier as nonphysical.

The limiting forms at large $\rho$ (actually, $\rho\gg\ell$) are

:::{math}
:label: eq-cenforce-29
\begin{aligned}
j_\ell(\rho) &\approx {1\over\rho} \cos\Bigl[\rho-(\ell+1){\pi\over 2}\Bigr] = {1\over\rho}\sin\Bigl(\rho-{\ell\pi\over2}\Bigr),
\end{aligned}
:::

:::{math}
:label: eq-cenforce-30
\begin{aligned}
y_\ell(\rho) &\approx {1\over\rho} \sin\Bigl[\rho-(\ell+1){\pi\over 2}\Bigr] = -{1\over\rho}\cos\Bigl(\rho-{\ell\pi\over2}\Bigr).
\end{aligned}
:::

See Abramowitz and Stegun, Eqs.~(10.1.1), (9.2.1) and (9.2.2). These are useful in scattering theory.

(sec-cenforce-8)=

## WKB Theory and Spherical Bessel Functions

The limiting forms at large $\rho$ can be obtained by treating the radial Schr\"odinger equation (in version two) by one-dimensional WKB theory, apart from normalization. We discuss this briefly without going into details because WKB theory provides an easy way to understand all the qualitative features of the functions $j_\ell(\rho)$ and $y_\ell(\rho)$, as seen in Figs.~{ref}`fig-cenforce-3` and {ref}`fig-cenforce-4`.

It turns out that the accuracy of the WKB approximation for radial wave equations is improved if the quantity $\ell(\ell+1)$ is replaced by $(\ell+\frac{1}{2})^2$. This is called the *Langer modification*, and it has to do with the singularity in the centrifugal potential at $r=0$. That is, for the purposes of WKB theory, we work with the effective radial potential,

:::{math}
:label: eq-cenforce-31
U(r) = {\hbar^2 (\ell+\frac{1}{2})^2 \over 2mr^2} + V(r).
:::

The centrifugal potential cannot be turned off and is present even for a free particle (except when $\ell=0$). Thus the effective potential depends on $\ell$, and we have different turning points etc depending on $\ell$. In the case of the free particle ($V=0$) the turning point $r_0$ is the solution of

:::{math}
:label: eq-cenforce-32
E = {\hbar^2 k^2 \over 2m} = U(r_0) = {\hbar^2 (\ell+\frac{1}{2})^2 \over 2m r_0^2},
:::

or,

:::{math}
:label: eq-cenforce-33
kr_0 = \rho_0 = \ell+\frac{1}{2}.
:::

The turning point moves out as $\ell$ increases, something that can also be seen from {ref}`fig-cenforce-5`.

It might seem strange that a free particle should have a turning point at all. The only reason it does is the centrifugal potential, which, as mentioned, is really a part of the kinetic energy. {ref}`fig-cenforce-6`, which shows a classical orbit of a free particle of some energy $E=p^2/2m$ and angular momentum $L$, helps explain the situation. The orbit is a straight line which must pass at some minimum distance from the origin. In the figure, the orbit lies in the $x$-$y$ plane. The minimum distance is $r_min=L/p$. The family of all possible classical orbits of the given $E$ and $L$ is a set of straight lines tangent to the sphere $r=r_min$. In quantum mechanics, the minimum radius becomes the radial turning point $r_0 = (\ell+\frac{1}{2})\hbar/p = (\ell+\frac{1}{2})/k$.

:::{figure} images/cenforce-fig05.png
:label: fig-cenforce-5
:width: 80%

The radial turning point for a free particle moves out as $\ell$ increases.
:::

:::{figure} images/cenforce-fig06.png
:label: fig-cenforce-6
:width: 80%

The minimum distance of approach to the origin of a classical free particle of momentum $p$ and angular momentum $L$ is $r_min = L/p$.
:::


For $\ell>0$ the exact spherical Bessel functions $j_\ell(\rho)$, which are 0 at $\rho=0$, rise up to a first maximum somewhat after the point $\rho=\ell+\frac{1}{2}$, and then oscillate beyond that. From the standpoint of WKB theory, we have a classically forbidden region to the left of the turning point $\rho=\ell+\frac{1}{2}$, an Airy-function type of behavior in the neighborhood of the turning point (see Fig.~\figr\wkb.8), and a classically allowed region to the right, exactly as we would expect on the basis of {ref}`fig-cenforce-5`. The case $\ell=0$ is an exception, since in that case the centrifugal potential vanishes and there is no turning point.

The functions $y_\ell(\rho)$ can also be understood from the standpoint of WKB theory; these are the functions that diverge exponentially as we move into the classically forbidden region (that is, as we move to the left of the turning point at $\rho=\ell+\frac{1}{2}$), and have the behavior of the $\Bi$ function in the neighborhood of the turning point (see Fig.~\figr\wkb.9).

It will be left as an exercise to work out the details of the WKB approximations to the spherical Bessel functions. The WKB solutions turn out to be more accurate than {eq}`eq-cenforce-29` and {eq}`eq-cenforce-30` when $\rho$ is not too much larger than $\ell+\frac{1}{2}$, but go over to them in the limit $\rho \gg \ell+\frac{1}{2}$.

% You can derive the expansion of the plane wave in terms of spherical % Bessel functions, apart from the normalization, by going to k-space % and using a k-space delta function in spherical coordinates. But % that requires the expansion of the spherical delta function in terms % of Ylm's.

(sec-cenforce-9)=

## Two-Body Central Force Motion

We return to the discussion of \secrcenforce-2. If the source of the force field is not infinitely massive, then a coordinate system attached to it is not an inertial frame and we must take into account the dynamics of the force center itself. That is, we must deal with a two-body problem, which we describe in an arbitrary (“lab”) inertial frame. We let $\xvec_1$ and $\xvec_2$ be the coordinates of the two particles with respect to this frame, with masses $m_1$ and $m_2$, respectively. We assume the force is described by a potential

:::{math}
:label: eq-cenforce-34
V=V(|\xvec_1-\xvec_2|),
:::

which depends only on the distance between the particles. The Hamiltonian is the sum of the kinetic and potential energies,

:::{math}
:label: eq-cenforce-35
H = {p_1^2\over 2m_1} + {p_2^2\over 2m_2} + V(|\xvec_1-\xvec_2|),
:::

where $\pvec_1$ and $\pvec_2$ are the momenta of the two particles.

We assume the particles are spinless or else we ignore spin. We write $\Psi(\xvec_1,\xvec_2)$ for the configuration space wave function, upon which the operators $\pvec_k$ act as differential operators,

:::{math}
:label: eq-cenforce-36
\pvec_k = -i\hbar\pop{}{\xvec_k} = -i\hbar\del_k, \qquad k=1,2.
:::

Translation operators $T(\avec)$ act on the wave function according to

:::{math}
:label: eq-cenforce-37
\bigl(T(\avec)\Psi\bigr)(\xvec_1,\xvec_2) = \Psi(\xvec_1-\avec, \xvec_2-\avec),
:::

a two-particle, three dimensional generalization of {eq}`eq-spatialdof-23`. The generator of translations is the total momentum,

:::{math}
:label: eq-cenforce-38
\Pvec = \pvec_1 + \pvec_2.
:::

The Hamiltonian commutes with all translations because the distance between the particles is not changed when both particles are displaced by the same amount. Therefore $H$ also commutes with the total momentum,

:::{math}
:label: eq-cenforce-39
[H,\Pvec]=0.
:::

The Hamiltonian is also invariant under rotations. Rotation operators act upon $\Psi$ according to

:::{math}
:label: eq-cenforce-40
\bigl(U(\Rmat)\Psi\bigr)(\xvec_1,\xvec_2) = \Psi( \Rmat^{-1}\xvec_1, \Rmat^{-1}\xvec_2),
:::

as explained in \orbamsph.9. The angular momentum of the system (the generator of rotations) is

:::{math}
:label: eq-cenforce-41
\Lvec = \Lvec_1 + \Lvec_2,
:::

where

:::{math}
:label: eq-cenforce-42
\Lvec_k = \xvec_k \cross \pvec_k, \qquad k=1,2,
:::

that is, it is the sum of the angular momenta of the two particles. The Hamiltonian {eq}`eq-cenforce-35` commutes with all rotations and hence with the total angular momentum $\Lvec$,

:::{math}
:label: eq-cenforce-43
[H,\Lvec]=0.
:::

To solve the Schr\"odinger equation $H\Psi = E\Psi$ for Hamiltonian {eq}`eq-cenforce-35` we introduce a change of coordinates,

:::{math}
:label: eq-cenforce-44
\begin{aligned}
\Rvec &= {m_1 \xvec_1 + m_2 \xvec_2 \over M},
\end{aligned}
:::

:::{math}
:label: eq-cenforce-45
\begin{aligned}
\rvec &= \xvec_2 - \xvec_1,
\end{aligned}
:::

where

:::{math}
:label: eq-cenforce-46
M=m_1 + m_2
:::

is the total mass of the system, so that $\Rvec$ is the position of the center of mass and $\rvec$ is the relative position vector between the particles. We write $\Psi(\Rvec,\rvec) =\Psi(\xvec_1, \xvec_2)$ for the wave function transformed to the new coordinates. We also define momenta “conjugate” to $\Rvec$ and $\rvec$ as the differential operators,

:::{math}
:label: eq-cenforce-47
\Pvec = -i\hbar\pop{}{\Rvec}, \qquad \pvec = -i\hbar\pop{}{\rvec},
:::

when acting on wave functions $\Psi(\Rvec,\rvec)$. By the chain rule, we can express the momenta $\pvec_1$ and $\pvec_2$ of the particles in the lab frame in terms of $\Pvec$ and $\pvec$,

:::{math}
:label: eq-cenforce-48
\begin{aligned}
\pvec_1 &= -i\hbar\pop{}{\xvec_1} = -i\hbar\Bigl( \frac{\partial \Rvec}{\partial \xvec_1}\cdot\pop{}{\Rvec} + \frac{\partial \rvec}{\partial \xvec_1}\cdot\pop{}{\rvec}\Bigr) = -i\hbar\Bigl( {m_1\over M} \pop{}{\Rvec} - \pop{}{\rvec}\Bigr),
\end{aligned}
:::

:::{math}
:label: eq-cenforce-49
\begin{aligned}
\pvec_2 &= -i\hbar\pop{}{\xvec_2} = -i\hbar\Bigl( \frac{\partial \Rvec}{\partial \xvec_2}\cdot\pop{}{\Rvec} + \frac{\partial \rvec}{\partial \xvec_2}\cdot\pop{}{\rvec}\Bigr) = -i\hbar\Bigl( {m_2\over M} \pop{}{\Rvec} + \pop{}{\rvec}\Bigr),
\end{aligned}
:::

or,

:::{math}
:label: eq-cenforce-50
\begin{aligned}
\pvec_1 &= {m_1\over M}\Pvec - \pvec,
\end{aligned}
:::

:::{math}
:label: eq-cenforce-51
\begin{aligned}
\pvec_2 &= {m_2\over M}\Pvec + \pvec.
\end{aligned}
:::

Solving these for $\Pvec$ and $\pvec$, we find

:::{math}
:label: eq-cenforce-52
\begin{aligned}
\Pvec &= \pvec_1 + \pvec_2,
\end{aligned}
:::

:::{math}
:label: eq-cenforce-53
\begin{aligned}
\pvec &= {m_1\pvec_2 - m_2 \pvec_1 \over M},
\end{aligned}
:::

and we see that $\Pvec$ defined by {eq}`eq-cenforce-47` is the total linear momentum of the system (the generator of translations), as in {eq}`eq-cenforce-38`. The transformation $(\xvec_1,\pvec_1; \xvec_2,\pvec_2) \to (\Rvec,\Pvec; \rvec,\pvec)$ specified by {eq}`eq-cenforce-44`, {eq}`eq-cenforce-45`, {eq}`eq-cenforce-52` and {eq}`eq-cenforce-53` is an example of a “canonical transformation,” that is, one which preserves the canonical commutation relations. That is, we have

:::{math}
:label: eq-cenforce-54
[R_i, P_j] = [r_i, p_j] = i\hbar \, \delta_{ij}, \qquad [R_i,r_j] = [R_i,p_j] = [P_i,r_j] = [P_i,p_j]=0,
:::

where $r_i$ and $R_i$ refer to the components of $\rvec$ and $\Rvec$, respectively. We see that any function of $(\Rvec,\Pvec)$ commutes with any function of $(\rvec,\pvec)$.

Transforming the Hamiltonian {eq}`eq-cenforce-35` to the new coordinates is straightforward. As for the potential, it becomes $V(|\xvec_1-\xvec_2|) = V(|\rvec|) = V(r)$, where $r=|\rvec|$ is the distance between the two particles. Also transforming the kinetic energy, we find the Hamiltonian as a sum of a center-of-mass term and a relative term,

:::{math}
:label: eq-cenforce-55
H = H_CM + H_rel,
:::

where

:::{math}
:label: eq-cenforce-56
H_CM = {P^2 \over 2M},
:::

and

:::{math}
:label: eq-cenforce-57
H_rel = {p^2 \over 2\mu} + V(r).
:::

Here $\mu$ is the *reduced mass*, defined by

:::{math}
:label: eq-cenforce-58
{1\over \mu} = {1\over m_1} + {1\over m_2}.
:::

The reduced mass $\mu$ is the harmonic mean of the masses $m_1$ and $m_2$. If one of the two particles is much more massive than the other (for example, in hydrogen where the proton is roughly 2000 times more massive than the electron), then the reduced mass is closer to the mass of the *lighter* of the two particles (for example, the electron, in the case of hydrogen). At the other extreme, if the two masses are equal, $m_1=m_2=m$, then $\mu=m/2$.

The Hamiltonian $H_CM$ is a free particle Hamiltonian, containing physically the kinetic energy *of* the center of mass, while $H_rel$ is physically the kinetic energy *about* the center of mass plus the potential energy. The two Hamiltonians $H_CM$ and $H_rel$ commute with each other,

:::{math}
:label: eq-cenforce-59
[H_CM,H_rel]=0,
:::

because they are functions of different degrees of freedom, and they also commute with the total Hamiltonian $H$. Thus, $H_CM$ and $H_rel$ possess a simultaneous eigenbasis, which is also an eigenbasis of the total Hamiltonian $H$.

This simultaneous eigenbasis consists of functions of the form,

:::{math}
:label: eq-cenforce-60
\Psi(\Rvec,\rvec) = \Phi(\Rvec) \psi(\rvec),
:::

a product of a center-of-mass wave function $\Phi$ times a relative wave function $\psi$. Each of these are eigenfunctions of their respective Hamiltonians,

:::{math}
:label: eq-cenforce-61
\begin{aligned}
H_CM \Phi &= E_CM\Phi,
\end{aligned}
:::

:::{math}
:label: eq-cenforce-62
\begin{aligned}
H_rel \psi &= E_rel\psi,
\end{aligned}
:::

where the eigenvalue $E$ of the total Hamiltonian $H$ is given by

:::{math}
:label: eq-cenforce-63
E = E_CM + E_rel.
:::

The center-of-mass equation {eq}`eq-cenforce-61` is easy to solve since $H_CM$ is just a free particle Hamiltonian. For example, if we choose the three components of $\Pvec$ as a complete set of commuting observables for the center-of-mass motion, we have eigenfunctions

:::{math}
:label: eq-cenforce-64
\Phi(\Rvec) = e^{i\Pvec\cdot\Rvec/\hbar},
:::

that is, plane wave with momentum $\Pvec$ (being somewhat sloppy about the distinction between the operator $\Pvec$ and its eigenvalues). Of course we may also solve this free particle equation in spherical coordinates.

The relative wave equation {eq}`eq-cenforce-62` has the form of a pseudo-one-body problem of the kind considered earlier in these notes, but with a reinterpretation of the variables. Now $\rvec$ is the relative position vector between the two particles, and $\pvec$ is defined by {eq}`eq-cenforce-53`. Also, the mass $m$ used earlier in these notes must be identified with the reduced mass $\mu$. In the limit $m_1 \to \infty$ while holding $m_2$ fixed, we recover the earlier results in which we had an infinitely massive force center. It is worthwhile keeping in mind, however, that in real problems the position and momentum operators for relative motion in a two-body problem such as hydrogen are really functions of the positions and momenta of *both* particles.

As a final remark, we transform the total angular momentum of the system $\Lvec$, expressed in terms of the coordinates of the two particles in {eq}`eq-cenforce-41` and {eq}`eq-cenforce-42`, over to the new coordinates. We find

:::{math}
:label: eq-cenforce-65
\Lvec = \Lvec_CM + \Lvec_rel,
:::

where

:::{math}
:label: eq-cenforce-66
\Lvec_CM = \Rvec \cross \Pvec, \qquad \Lvec_rel = \rvec \cross \pvec.
:::

The Hamiltonian $H_CM$ commutes with $\Lvec_CM$, and $H_rel$ commutes with $L_rel$. In other language, the total Hamiltonian $H$ commutes not only with overall rotations of the system, but with rotations of the center of mass and with rotations about the center of mass separately.

(sec-cenforce-10)=

## The Rigid Rotor

As an example of central force motion we consider the rigid rotor. We have already considered the rigid rotor in a plane (see {ref}`sec-wkb-12`), but now we consider it in three dimensions. The rotor consists of two masses $m_1$ and $m_2$ connected by a massless, rigid rod of length $r_0$, as in {ref}`fig-cenforce-7`. This is an example of central force motion because the constraint $r=r_0$ can be thought of as due to a sharply confining potential $V(r)$ centered on $r=r_0$.

:::{figure} images/cenforce-fig07.png
:label: fig-cenforce-7
:width: 80%

A rigid rotor in which the two masses $m_1$ and $m_2$ are separated by a fixed distance $r_0$. The center of mass is closer to the more massive end.
:::

First we look at the classical mechanics. The moment of inertia about the center of mass is

:::{math}
:label: eq-cenforce-67
I=\mu r_0^2.
:::

The energy is

:::{math}
:label: eq-cenforce-68
E= {L^2 \over 2I} = {L^2 \over 2\mu r_0^2}.
:::

It is the same as the centrifugal potential, which is logical since the centrifugal potential is really the angular part of the kinetic energy, which is all there is for a rigid rotor.

The classical configuration, apart from the center-of-mass degrees of freedom, is just the orientation of the rotor, specified by angles $(\theta,\phi)$. This suggests that the wave function in quantum mechanics should be $\psi(\theta,\phi)$ (with no $r$-dependence). As for the quantum Hamiltonian, we guess that it should be

:::{math}
:label: eq-cenforce-69
H={L^2 \over 2I},
:::

the obvious operator corresponding to the classical energy {eq}`eq-cenforce-68`.

This makes it easy to solve the Schr\"odinger equation, $H\psi = E\psi$. The energy eigenvalues are

:::{math}
:label: eq-cenforce-70
E_\ell = {\ell(\ell+1)\hbar^2 \over 2I} ={\ell(\ell+1)\hbar^2 \over 2\mu r_0^2},
:::

and the eigenfunctions are

:::{math}
:label: eq-cenforce-71
\psi_{\ell m}(\theta,\phi) = Y_{\ell m}(\theta,\phi).
:::

The energies do not depend on the magnetic quantum number $m$, and are $(2\ell+1)$-fold degenerate.

(sec-cenforce-11)=

## Diatomic Molecules

Rigid rotors are an idealization that does not exist in nature, but diatomic molecules exist and have many similar features. Consider, for example, carbon monoxide (CO). The atomic masses are $m_C \approx 12 \,m_H$, $m_O \approx 16 \,m_H$, where $m_H$ is the mass of the hydrogen atom, with $m_H \approx 1800 \,m$, where $m$ is the mass of the electron. We denote the reduced mass of the carbon-oxygen system by $M$ (rather than $\mu$ as above, since we wish to contrast the large mass $M$ with the small electron mass $m$). Numerically,

:::{math}
:label: eq-cenforce-72
M = \\textreduced mass \approx 7\,m_H \approx 10^4 \,m,
:::

very roughly. This leads to some small parameters that we will see in the analysis of the molecule,

:::{math}
:label: eq-cenforce-73
{m\over M} \approx 10^{-4}, \qquad \sqrt{\ds{\ds m\over \ds M}} \approx 10^{-2}, \qquad \Bigl({\ds{\ds m\over \ds M}}\Bigr)^{1/4} \approx 10^{-1},
:::

where very rough values are given. These values apply very roughly to most common diatomic molecules.

A diatomic molecule can be regarded as a central force problem involving two bodies (the atoms), each treated as a particle. Of course the particles in question are composite, made up of nuclei and electrons, but in a certain approximation they may be treated as independent units, that is, particles in their own right. The more elaborate theory that justifies this is called the *Born-Oppenheimer approximation*.

:::{figure} images/cenforce-fig08.png
:label: fig-cenforce-8
:width: 80%

Typical potential in a diatomic molecule. The equilibrium radius is $r_0$, the well depth is $V_0$.
:::

The potential of interaction of two atoms in a diatomic molecule is sketched in {ref}`fig-cenforce-8`. The potential is strongly repulsive at short distances, because as the two atoms are brought together their electron clouds overlap and by the Pauli principle the electrons are forced into higher energy states. It is the same principle at work as when a degenerate electron gas is compressed; the short range repulsion of two atoms can be thought of as due to the pressure of a degenerate electron gas. At large distances the force is mostly electrostatic, and is attractive. Each atom causes the other atom to polarize, creating an attractive dipole-dipole interaction. In between these two effects compete with one another, creating a potential well. The potential is characterized by two parameters, the well depth $V_0$ and the equilibrium radius $r_0$ (that is, $r_0$ is the distance to the minimum of the potential, which classically would be an equilibrium radius). For CO the actual values are $V_0 = 11\, eV$, $r_0 = 1.1 \,\AA$.

There is no simple analytical form for $V(r)$, so we will rely on order-of-magnitude estimates that follow from dimensional analysis. The basic fact we rely on is that the force between the atoms is determined by the dynamics of the electron clouds. There are only three fundamental constants that enter into the electron dynamics: $m$, $e$ and $\hbar$. The speed of light $c$ is not on the list because the interaction is electrostatic and the electron motion is nonrelativistic. It is important to note that the nuclear masses do not enter into the potential. One might wonder whether some dimensionless parameters are important, such as the number of electrons in the atom, or, equivalently, the nuclear charges (6 for C and 8 for O). The answer is that these numbers are not as important as one might expect, because the atomic interactions, at the distances we are interested in, are mediated mostly by the valence electrons. Inside the typical radius of the valence electrons is the atomic core, consisting of electrons that shield and nearly neutralize the positive charge from the nucleus.

From $e$, $m$ and $\hbar$ it is possible to construct a unique distance, energy, time, etc. These are displayed in {ref}`tbl-cenforce-1`. These are the same values of distance, energy, etc, that appear in the hydrogen atom, and for the same reason: the only physical constants we have to work with are $e$, $m$ and $\hbar$. For example, $a_0$ is the Bohr radius and $K_0$ is twice the ionization potential of hydrogen ($2\times 13.6\,eV$). Notice in particular $v_0$: it is the velocity of the electron in the ground state of hydrogen. Although fast, it is still nonrelativisitic ($v_0 < 1\%\,c$). As claimed, the electrons are nonrelativistic.

:::{list-table} Characteristic distance, time, etc for electron dynamics in an atom.
:label: tbl-cenforce-1
:header-rows: 1

* - Dimension
  - Definition
  - Value
* - distance
  - $a_0=\hbar^2/me^2$
  - $0.5\,{\AA}$
* - energy
  - $K_0=e^2/a_0=me^4/\hbar^2$
  - $27\,\mathrm{eV}$
* - velocity
  - $v_0=e^2/\hbar$
  - $\alpha c \approx c/137$
* - frequency
  - $\omega_0=me^4/\hbar^3 =K_0/\hbar$
  - $1/T_0$
* - time
  - $T_0=\hbar^3/me^4=1/\omega_0$
  - $2.4\times 10^{-17}\,\mathrm{sec}$

:::
Returning to the CO potential $V(r)$ in {ref}`fig-cenforce-8`, the well depth $V_0$ should be of the same order of magnitude as $K_0$; in fact, it is about 40\%. Also, $r_0$ should be of the same order of magnitude as $a_0$; in fact, it is a little more than twice as big. For an order-of-magnitude estimate, the agreement is not bad.

The radial Schr\"odinger equation in our potential is

:::{math}
:label: eq-cenforce-74
-{\hbar^2\over 2M} {d^2 f\over dr^2} +\Bigl[ {\ell(\ell+1)\hbar^2 \over 2Mr^2} + V(r)\Bigr] f(r) = Ef(r).
:::

At first we take $\ell=0$, so we have a one-dimensional Schr\"odinger equation with potential $V(r)$. Since there is a well we expect bound states, which physically are the quantized vibrations of the molecule. We can approximate the potential near the bottom of the well by a harmonic oscillator potential, that is, we can write

:::{math}
:label: eq-cenforce-75
V(r) \approx -V_0 + {M\over 2} \omega_v^2 (r-r_0)^2,
:::

where $\omega_v$ is the frequency of small vibrations. {ref}`fig-cenforce-8` shows that as the energy is raised much above the bottom of the well the parabolic approximation ceases to be a good one, but if there are many bound states then we can expect the low-lying ones to be described at least roughly by the harmonic approximation. In a moment we will estimate the number of bound states.

We can estimate the parameter $\omega_v$ in {eq}`eq-cenforce-75` by supposing that when $r-r_0 \sim r_0 \sim a_0$, then the potential is near dissociation, that is, $V(r)$ is near zero. Dropping factors of $1/2$ etc, this gives

:::{math}
:label: eq-cenforce-76
M\omega_v^2 (r-r_0)^2 \sim M\omega_v^2 a_0^2 \sim V_0 \sim K_0,
:::

or,

:::{math}
:label: eq-cenforce-77
\omega_v = \sqrt{\ds{\ds K_0 \over \ds Ma_0^2}} = \sqrt{\ds{\ds m\over \ds M}} \, \omega_0,
:::

where $\omega_0$ is given by {ref}`tbl-cenforce-1`. As long as the harmonic approximation is valid, the vibrational energy levels are $(n+\frac{1}{2})\hbar\omega_v$, where $n=0,1,\ldots$ is the vibrational quantum number.

The vibrational frequency of the molecule is down by a factor of the square root of the mass ratio, roughly $10^{-2}$ according to {eq}`eq-cenforce-73`, in comparison to the typical frequency of the electronic motion $\omega_0$. Frequency $\omega_0$ is also (as an order of magnitude) the frequency of a photon emitted or absorbed in a transition between electronic states, while the energy difference between two neighboring levels of the vibrational harmonic oscillator is $\hbar\omega_v$, that is, the emitted or absorbed photon has frequency $\omega_v$. Thus, vibrational transitions involve photons of energy roughly $100$ times smaller than electronic transitions. Electronic transitions are typically in the visible to ultraviolet range of frequencies, while vibrational transitions are in the near to mid infrared.

We can estimate the number of bound vibrational states by taking the ratio,

:::{math}
:label: eq-cenforce-78
N_vib = {V_0\over \hbar\omega_v} \sim {K_0\over \hbar\omega_v} = \sqrt{\ds{\ds M\over \ds m}} \sim 100.
:::

This is roughly the value for many diatomic molecules.

In the vibrational ground state the wave function is a Gaussian of width $a_ho$ (where “ho” means “harmonic oscillator”), which according to {eq}`eq-harmosc-12` is given by

:::{math}
:label: eq-cenforce-79
a_ho = \sqrt{\ds{\ds \hbar\over\ds M\omega_v}} = \left({m\over M}\right)^{1/4} \, a_0 \approx 0.1\,a_0.
:::

In the ground state the wave function occupies roughly 10\% of the bond length. The molecule does behave like a rigid rotor at least approximately, because the interatomic separation lies in a narrow range near $r_0$.

To account for the case $\ell\ne0$, we must include the centrifugal potential. But since the wave function occupies only a small part of the $r$-axis near $r=r_0$, the centrifugal potential is nearly constant over the extent of the wave function and we can just replace $r$ by $r_0$ in the centrifugal potential:

:::{math}
:label: eq-cenforce-80
{\ell(\ell+1)\hbar^2 \over 2Mr^2} \to {\ell(\ell+1)\hbar^2 \over 2Mr_0^2} = {\ell(\ell+1)\hbar^2 \over 2I},
:::

where $I$ is the moment of inertia in the equilibrium position. We see the appearance of the energies of the rigid rotor, derived in an intuitive way in \secrcenforce-10. The replacement {eq}`eq-cenforce-80` will become less accurate as $n$ increases (because the vibrational wave function is more spread out), or as $\ell$ increases (because the centrifugal potential becomes more rapidly varying in $r$).

With the replacements {eq}`eq-cenforce-75` and {eq}`eq-cenforce-80`, the radial Schr\"odinger equation becomes

:::{math}
:label: eq-cenforce-81
-{\hbar^2\over 2M} {d^2f\over dr^2} + \Bigl[ {\ell(\ell+1)\hbar^2 \over 2I} -V_0 + {M\over 2}\omega_v^2 (r-r_0)^2\Bigr] f(r) = Ef(r).
:::

This is a harmonic oscillator with shifted origin and a constant term ($-V_0$ plus the centrifugal potential) added. The energy eigenvalues are immediate:

:::{math}
:label: eq-cenforce-82
E_{n\ell} = -V_0 + \Bigl(n+{1\over2}\Bigr)\hbar\omega_v + {\ell(\ell+1)\hbar^2 \over 2I}.
:::

This is only valid for small $n$ and $\ell$, but it does give an easy and roughly accurate picture of the rotational and vibrational spectrum of the molecule. Notice that the energies have the general form predicted for central force potential in \secrcenforce-4, that is, they depend on both $n$ and $\ell$.

Let's examine the spacing between rotational energy levels in order to estimate the energy of the photon emitted or absorbed in a rotational transition. We define $\Delta E_rot$ as the spacing between the $\ell=0$ and $\ell=1$ levels, or,

:::{math}
:label: eq-cenforce-83
\Delta E_rot = {\hbar^2\over 2I} \sim {\hbar^2 \over M a_0^2} = {m\over M}\, K_0 \sim 10^{-4} \, K_0.
:::

This is roughly $100$ times smaller than $\Delta E_vib = \hbar\omega_v$, and roughly 10,000 times smaller than the energy of an electronic transition. The photons emitted or absorbed in rotational transitions typically lie in the far infrared to microwave range.

The molecule has three different energy scales: that of $K_0$, involved in electronic transitions, or equivalently, the energy of dissociation of the molecule (breaking the bond); the vibrational energy $\hbar\omega_v$, roughly the square root of the mass ratio times smaller; and the energy of rotational transitions, roughly the square root of the mass ratio times smaller still.

Greenhouse gases absorb infrared radiation from the earth by making vibrational transitions in molecules. These are not usually diatomic molecules, because the stretching vibrations of molecular bonds typically have too high a frequency. In addition, the main molecular species in the atmosphere, $N_2$ and $O_2$, are homonuclear diatomics without a permanent electric dipole moment. Instead, the greenhouse culprits are mainly $CO_2$ and $H_2O$, triatomics that have bending and twisting modes of lower frequency.

\problems

(prob-cenforce-1)=

**Problem \prbdcenforce-1..** 

:::{math}
:label: eq-cenforce-84
x=\rho\cos\phi, \qquad y=\rho\sin\phi.
:::

\problempart{(a)} Find the most general function $\psi(\rho,\phi)$ that is an eigenfunction of $L_z$. Express it in terms of a radial wave function $R(\rho)$, along the lines of what is done in the notes for the three-dimensional case. What is the spectrum of $L_z$?

\problempart{(b)} Consider a central force Hamiltonian in two dimensions,

:::{math}
:label: eq-cenforce-85
H={\pvec^2\over 2m_0} + V(\rho),
:::

where $\pvec=(p_x,p_y)$. In this problem $m_0$ is the mass of the particle, while $m$ is the quantum number of $L_z$. Show that this Hamiltonian commutes with $L_z$. Therefore simultaneous eigenfunctions of $H$ and $L_z$ exist.

By expressing the Laplacian in polar coordinates and using the result of part~(a), find a radial wave equation for $R(\rho)$ that will determine energy eigenfunctions and eigenvalues.

\problempart{(c)} Define a modified radial wave function by

:::{math}
:label: eq-cenforce-86
f(\rho) = \rho^a R(\rho),
:::

where $a$ is a power to be determined. Determine $a$ by requiring that the modified radial wave equation should look like the one-dimensional Schr\"odinger equation, apart from the range of the variable $\rho$ and the presence of the centrifugal potential.

\problempart{(d)} Consider the case of the free particle. Express the radial eigenfunctions $R(\rho)$ in terms of ordinary Bessel functions, $J_\nu(x)$, and in terms of the energy and the quantum number of $L_z$. You will have to look up the differential equation for ordinary Bessel functions.

\problempart{(e)} For any potential that is not too badly behaved near the origin, find the dependence of the radial eigenfunction $R(\rho)$ near $\rho=0$. Verify that the free particle solutions of part~(d) satisfy this condition.

(prob-cenforce-2)=

**Problem \prbdcenforce-2..** 

\problempart{(a)} The potential well is illustrated in {ref}`fig-cenforce-8`, with $V_0 = 11\,eV$, $r_0 = 1.1\, {\rm\AA}$. Approximate the potential near the bottom of the well by {eq}`eq-cenforce-75`, with some vibrational frequency $\omega_v$. By assuming that $V(r)=0$ (dissociation) when $r-r_0=r_0$, solve {eq}`eq-cenforce-75` numerically for $\omega_v$. Compare to the experimental value, which is $\nu=6.5\times 10^{13}\\textHz$. Note that $\omega=2\pi\nu$. How well does the order-of-magnitude estimate {eq}`eq-cenforce-77` work? See {ref}`tbl-cenforce-1` for $\omega_0$.

\problempart{(b)} What is the probability that the CO molecule is in the $n=1$ vibrational state at $300$ Kelvins? A typical infrared photon trying to escape the earth's atmosphere has an energy of 300K. There is not much CO in the atmosphere (good thing, since it's poisonous), but if there were, would it be efficient at absorbing or scattering photons by making vibrational transitions? Such absorption or scattering would impede the escape of heat from the earth, creating a greenhouse effect.

\problempart{(c)} A CO molecules makes a transition from the $\ell=1$ to the $\ell=0$ rotational state. What is the frequency (in Hertz) of the photon emitted? Compare to the vibrational frequency in part (a), and note the rough estimates made in \secrcenforce-11. What is the most probable value of $\ell$ in CO gas at 300K? Absorption or scattering of photons by rotational transitions is most probable when $\Delta\ell=1$, and falls off rapidly for higher values of $\Delta\ell$. Is CO at 300K effective at scattering typical infrared photons at 300K, by making rotational transitions?

(prob-cenforce-3)=

**Problem \prbdcenforce-3.}  Consider the helium atom in a lab frame.  The positions of the nucleus, electron 1 and electron 2 are $\xvec_n$, $\xvec_{e1}$ and $\xvec_{e2.** 

:::{math}
:label: eq-cenforce-87
H = {\pvec_n^2 \over 2M} + {\pvec_{e1}^2 \over 2m} + {\pvec_{e2}^2 \over 2m} + V(\xvec_n,\xvec_{e1}, \xvec_{e2}).
:::

We will only be interested in the kinetic energy in this problem.

Let }$\Rvec$ be the center of mass position and let

:::{math}
:label: eq-cenforce-88
\begin{aligned}
\rvec_1 & = \xvec_{e1} - \xvec_n, \\
\rvec_2 & = \xvec_{e2} - \xvec_n, \\

\end{aligned}
:::

so that $\rvec_1$ and $\rvec_2$ are the positions of the two electrons relative to the nucleus. Also define new momentum operators,

:::{math}
:label: eq-cenforce-89
\Pvec = -i\hbar \pop{}{\Rvec}, \quad \pvec_1 = -i\hbar \pop{}{\rvec_1}, \quad \pvec_2 = -i\hbar \pop{}{\rvec_2}.
:::

Express the kinetic energy as a function of these new momentum operators. You will obtain a term proportional to $\pvec_1 \cdot \pvec_2$. This is called a “mass polarization” term.

The usual simple-minded treatment of helium treats the nucleus as infinitely heavy. In this approach there are no mass polarization terms. Explain why its a good approximation to neglect those terms (thus, the usual approach is ok).
