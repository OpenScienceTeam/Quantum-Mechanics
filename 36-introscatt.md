---
title: "36. Introduction to Time-Independent Scattering Theory and Scattering from Central Force Potentials"
---
(ch-introscatt)=

# 36. Introduction to Time-Independent Scattering Theory and Scattering from Central Force Potentials

(sec-introscatt-1)=

## Introduction

In {ref}`ch-tdpt`{} we considered some scattering problems as an application of time-dependent perturbation theory, taking a time-dependent approach. In these notes we take a time-independent approach to potential scattering in three dimensions, that is, we will be interested in energy eigenfunctions of the Schr\"odinger equation,

:::{math}
:label: eq-introscatt-1
H\psi(\xvec)=-{\hbar^2 \over 2m}\del^2\psi(\xvec) + V(\xvec)\psi(\xvec) = E\psi(\xvec),
:::

for positive energies $E>0$. These solutions must satisfy certain boundary conditions to be useful in scattering theory. These energy eigenfunctions are part of the continuous spectrum so they extend to infinity and are not normalizable. Thus, they do not represent the state of physical particles, although they can be thought of as a limit of such states.

For the sake of generality we do not at first assume that the potential $V(\xvec)$ is rotationally invariant, but as usual in scattering theory we assume that it approaches zero with distance,

:::{math}
:label: eq-introscatt-2
\lim_{r\to\infty} V(\xvec) = 0,
:::

where $r=|\xvec|$. In fact, the simplest case is the one in which $V\to0$ faster than $1/r$ as $r\to\infty$ (see \secrintroscatt-10). This excludes the case of the Coulomb potential or potentials with a Coulomb tail, which are important in practice but which require special techniques.

We will speak of the scattering of a particle by the potential $V(\xvec)$, as if it were a fixed potential in space, but in reality the beam particle interacts with a target, which often is another particle. Then a proper treatment requires us to take into account the dynamics of both particles. The changes necessary to do this were discussed in some detail in {ref}`ch-tdpt`. For now we simply note that if the target is very massive, then it can be thought of as producing a potential for the beam particle that is fixed in space (that is, in an inertial frame), as we shall assume in these notes.

We begin by examining the boundary conditions that the desired solutions of the Schr\"odinger equation should satisfy in a scattering problem, in order to develop an intuitive picture of what they look like. This leads to a definition of the *scattering amplitude* and its relation to the differential cross . We then specialize to the case of central force potentials, for which the Schr\"odinger equation is separable in spherical coordinates and for which many special results are available. We devote some attention to hard sphere scattering, which is probably the most tractable central force scattering problem, and which illustrates many features of scattering from more general potentials. Finally we discuss the optical theorem in the context of potential scattering in three dimensions, an exact result that has many generalizations.

(sec-introscatt-2)=

## Classical Scattering:  The Steady State

We begin by considering a classical model of a scattering experiment. A beam of particles is directed at a target, as illustrated in {ref}`fig-introscatt-1`. We imagine that all the particles have the same momentum $\pvec$, and that the density of particles is uniform across the beam. In reality the beam has to be turned on at some time, so we can imagine a time-dependent problem in which the beam particles first approach the scatterer, then begin to interact with it, and then produce an outward traveling front of scattered particles. If we stand at any given point and wait, then initially there are no scattered particles, then the front arrives and we start to see them, and after the front has passed we reach a steady state, in which the flux of scattered particles is constant in time. The farther we are from the scatterer, the longer we have to wait for a steady state to be achieved, but eventually it will happen.

:::{figure} images/introscatt-fig01.png
:label: fig-introscatt-1
:width: 80%

Classical scattering. A beam of particles, all with the same momentum $\pvec$, is directed against a target.
:::

To obtain an idealized steady state we can imagine that the time at which the beam is switched on recedes to $-\infty$, while the source of the beam also recedes to infinity, so that we have a steady beam coming in from infinite distance in the upstream direction. We can further idealize the situation by letting the final time advance to $+\infty$, so that a steady flux of scattered particles exists at all spatial locations.

In this steady state, at any spatial point we have a definite flux of scattered particles, and, if we are inside the beam, also a flux of incident particles. If we are at a distance from the scatterer large enough that the potential can be neglected, then the kinetic energy of the scattered particles is the same as that of the incident particles, because the scattering is elastic. That is, when a particle gains kinetic energy by falling into the potential well, it loses the same amount when climbing back out again (or if the potential is positive it will lose kinetic energy on entering the potential, and then gain it back when exiting).

There is also the question of how wide the beam is. Real beams have a finite width, which we normally make much larger than the range of the potential (however that is defined). It is worth noting that in classical scattering the total cross is nominally infinite, unless the potential rigorously vanishes outside some radius. That is because if $V(\xvec)$ goes to zero only gradually as $r=|\xvec|\to\infty$, then there is some small angle of scattering, even at large impact parameters. Most of the infinite cross that results in such a case is due to small angle scattering, so $d\sigma/d\Omega$ diverges as $\theta\to0$. Most of this small angle scattering might well be of no practical interest, but to see it one would need a beam that is infinitely wide (another idealization). In quantum mechanics, as we will see, total cross s are finite if the potential dies off rapidly enough with distance (it need not rigorously vanish beyond a certain radius).

Notice that if we extend the width of the beam to infinity, then (with the other idealizations we have made) the classical stationary state is uniquely determined by the momentum $\pvec$ of the incident beam, that is, the momentum it has far upstream at a large distance from the scatterer.

(sec-introscatt-3)=

## The Stationary State in Quantum Scattering

In quantum mechanics a *stationary state* is usually defined as an energy eigenstate, which with the time-dependence has a wave function of the form $\psi(\xvec)\,e^{-iEt/\hbar}$. The wave function is not stationary, but the probability density $\rho$ and current $\Jvec$ are. Thus it is plausible that the stationary state we have just described in classical scattering should correspond to an energy eigenstate in quantum scattering.

It is not hard to visualize such an eigenfunction but there are several idealizations that must be understood. For example, as in the classical case, the steady state can be realized as the limit of a time-dependent situation. We proceed intuitively. Probably the simplest way to realize this limit is to let the initial state be a wave packet, for example, a Gaussian wave packet, whose expectation value of momentum is $\pvec$ and whose spread in momentum is some $\Delta p \ll |\pvec|$. We will be interested in the limit $\Delta p\to0$ so that the initial state has a well defined momentum $\pvec$ in the limit. But the width of the wave packet in real space is $\Delta x \ge \hbar/(2\Delta p)$, which goes to $\infty$ as $\Delta p\to 0$. As it does so, the value of the normalized wave function $\psi(\xvec)$ goes to zero, since the wave function is spread over larger and larger regions of space. Therefore it is convenient to deal with unnormalized wave functions, and to require that the magnitude of $\psi(\xvec)$ at the center of the wave packet remain finite as $\Delta p\to0$. This means that in the limit the wave function has an infinite norm. As this limit is approached, the middle of the wave packet looks more and more like a plane wave with momentum $\pvec$.

We wish the wave packet at the initial time to lie far enough upstream that is has essentially no interaction with the potential. The wave packet is aimed at the target, but it evolves according to the free particle Hamiltonian until the leading edge reaches the region where the potential is effective. This guarantees that the initial wave packet does not have any components along the bound states of the potential $V(\xvec)$, since any such bound state wave functions are localized in the neighborhood of the potential. We do not want such components in the initial wave packet, since the bound states are not scattering states; bound states evolve in time simply by oscillating in place, without scattering. However, since the size of the wave packet $\Delta x$ goes to $\infty$ in the limit $\Delta p\to 0$, we must pull the center of the initial wave packet farther and farther away from the scatterer to guarantee that it has no overlap with the potential at the initial time. Then we must wait for a longer and longer time for the wave packet to reach the scatterer.

:::{figure} images/introscatt-fig02.png
:label: fig-introscatt-2
:width: 80%

Quantum scattering by a potential $V(\xvec)$. Incident and scattered waves are shown.
:::

Thus there are several interlocking limits that must be taken at once, but when $\Delta p$ is small and we wait until the center of the wave packet has reached the scatterer, then for some time around this time and for some distance away from the scatterer we have a nearly steady state, in which a wave that locally looks like a plane wave is incident on the scatterer, and a scattered wave is radiating outward from the scatterer. In the limit we achieve a quantum steady state that is illustrated in {ref}`fig-introscatt-2` and that resembles the classical steady state described in \secrintroscatt-2. The quantum steady state that results in the limit depends only on the initial momentum $\pvec$.

(sec-introscatt-4)=

## Boundary Conditions

If we are far from the scatterer then in the resulting steady state we see two waves, an incident wave which is a plane wave of momentum $\pvec$ and a scattered wave, radiating away from the scatterer. To rigorously define the decomposition of the total wave into an incident wave and scattered wave which is valid everywhere (even where the potential is active), we write the exact solution to the Schr\"odinger equation as

:::{math}
:label: eq-introscatt-3
\psi(\xvec)=\psi_inc(\xvec)+\psi_scatt(\xvec),
:::

where the indicent wave is a plane wave of momentum $\pvec=\hbar\kvec$,

:::{math}
:label: eq-introscatt-4
\psi_inc(\xvec) = e^{i\kvec\cdot\xvec}
:::

and where $\psi_scatt(\xvec)$ is defined as the difference between the exact and incident wave, so that {eq}`eq-introscatt-3` is true. Also, in the asymptotic region, at large $r$ where the potential is negligible, we require that the scattered wave consist of purely outgoing waves, moving in the radial direction away from the scatterer.

If we conceive of the potential has having some well defined range then the angle subtended by the scatterer is nonzero at any finite radius $r$, so the “outward” direction is not precisely defined. This is especially clear in the case that the potential is not rotationally invariant, so that it has no well defined center. But as $r\to\infty$ the angle subtended goes to zero, and the radial direction does become well defined. In this limit, we require that the scattered wave have the form

:::{math}
:label: eq-introscatt-5
\psi_scatt(r,\theta,\phi) \sim {e^{ikr}\over r}f(\theta,\phi),
:::

where the symbol $\sim$ means that we are giving the asymptotic form of the scattered wave, valid when $r\to\infty$. More precisely, this symbol means that the left hand side equals the right hand side, plus corrections that go to zero more rapidly as $r\to\infty$ than does the right hand side. For example, there may be corrections of order $1/r^2$ that are not shown. The asymptotic form in {eq}`eq-introscatt-5` indicates a wave that is traveling outward in the radial direction (as we see if we attach the time-dependent factor $e^{-iEt/\hbar}$), and which has an angular dependence given by the function $f(\theta,\phi)$.

In the asymptotic region both the incident wave and the scattered wave must satisfy the free particle Schr\"odinger equation, assuming the potential in {eq}`eq-introscatt-1` is negligible as $r\to\infty$. As for the incident plane wave, this is obvious, and we see that the energy eigenvalue $E$ of the Schr\"odinger equation and the wave vector $\kvec$ of the incident wave are related by the free-particle relation,

:::{math}
:label: eq-introscatt-6
E = {\hbar^2 k^2 \over 2m}.
:::

Physically this means that where the particles are launched, in the asymptotic region far upstream, their energy is purely kinetic.

As for the scattered wave, we only have an asymptotic form for it, so it must satisfy the free-particle Schr\"odinger equation to leading asymptotic order. To show that it does we apply the kinetic energy operator in spherical coordinates [see {eq}`eq-vecident-23`],

:::{math}
:label: eq-introscatt-7
-{\hbar^2\over 2m}\del^2 \psi_scatt(r,\theta,\phi) = -{\hbar^2\over 2m} \Bigl[{1\over r^2}\pop{}{r} r^2 \pop{}{r} + \ldots \Bigr] \Bigl[ {e^{ikr}\over r}f(\theta,\phi) + \ldots\Bigr] ={\hbar^2 k^2\over 2m} {e^{ikr}\over r}f(\theta,\phi) + \ldots,
:::

where the ellipses indicate terms that die off faster as $r\to\infty$ than the terms shown. Notice that the angular derivatives in the Laplacian operator are of higher order in $1/r$ than the radial derivatives. Thus we find that the asymptotic form of the scattered wave does satisfy the free-particle Schr\"odinger equation to leading asymptotic order, with an energy given by the free-particle relation {eq}`eq-introscatt-6`. That is, the $k$ parameter of the asymptotic form of the scattered wave equals $|\kvec|$, where $\kvec$ is the wave vector of the incident wave. This is the expression of conservation of energy in the scattering process in in quantum mechanics.

Many books write down the asymptotic form {eq}`eq-introscatt-5` of the scattered wave as if it were obvious. In fact, it is not always true (see \secrintroscatt-10), and it takes some effort to understand why it is reasonable and what its conditions of its validity are.

The intuitive arguments presented suggest that the Schr\"odinger equation {eq}`eq-introscatt-1` has a unique solution satisfying the boundary conditions indicated by {eq}`eq-introscatt-3`--{eq}`eq-introscatt-5`. If the potential $V$ falls off more rapidly than $1/r$ then this is true, as can be proven with the theory of integral equations. An introduction to the latter is given in {ref}`ch-lippschw`. Thus, the unique solution is parameterized by the momentum $\pvec=\hbar\kvec$ of the incident wave. We will henceforth write the solution as $\psi_\kvec(\xvec)$ when we wish to emphasize this dependence.

We see that there are many linearly independent solutions of the Schr\"odinger equation {eq}`eq-introscatt-1` of energy $E>0$, since we are free to direct the incident beam at the target from any direction we like. For a given $E$, this family is parameterized by the direction of $\kvec$. Thus in three-dimensional scattering, the family is continuous and is parameterized by points on a sphere. In one-dimensional scattering, there are only two linearly independent solutions for a given $E$, corresponding to waves incident from the right or left.

(sec-introscatt-5)=

## Densities and Currents

Energy eigenfunctions of {eq}`eq-introscatt-1` of energy $E\ge0$ are unbounded and not normalizable, so the usual density $\rho=|\psi|^2$ cannot be interpreted as a probability density. In scattering theory it is easiest to interpret $\rho$ as the density of particles in the beam, as we shall do here. Similarly, we interpret the current,

:::{math}
:label: eq-introscatt-8
\Jvec = \Re\Bigl[\psi^\cc \Bigl(-{i\hbar\del\over m}\Bigr) \psi\Bigr],
:::

as a particle current, not a probability current. The overall normalization of the unbounded wave function is arbitrary, and represents simply the intensity of the beam. Quantities of interest, such as the differential cross , are independent of this normalization.

(sec-introscatt-6)=

## The Scattering Amplitude and Cross Section

The function $f(\theta,\phi)$ in the asymptotic form of the scattered wave {eq}`eq-introscatt-5` is called the *scattering amplitude*. It is in general a complex function of the angles. A good deal of scattering theory is devoted to its determination, since it bears a simple relation to the differential cross .

:::{figure} images/introscatt-fig03.png
:label: fig-introscatt-3
:width: 80%

A particle detector intercepts a small solid angle $\Delta\Omega$ which defines a cone as seen from the scatterer. Particles scattered into this cone will enter the detector.
:::

Cross s and differential cross s were defined in {ref}`ch-tdpt`, where the relation between cross s and transition rates was discussed. In the present case let us imagine an experimental situation such as illustrated in {ref}`fig-introscatt-3`. A detector, located at some distance from the scatterer, intercepts all scattered particles coming out in a small cone of solid angle $\Delta\Omega$, centered on some direction ${\hat{\mathbf{n}}}=(\theta,\phi)$. The counting rate is the scattered current $\Jvec_scatt$ integrated across the aperture to the detector.

The particle density in the incident beam is

:::{math}
:label: eq-introscatt-9
n_inc = |\psi_inc(\xvec)|^2 =1.
:::

Similarly, the incident current is

:::{math}
:label: eq-introscatt-10
\Jvec_inc = \Re\Bigl[e^{-i\kvec\cdot\xvec}\Bigl(-{i\hbar\over m}\del\Bigr) e^{i\kvec\cdot\xvec}\Bigr]= {\hbar \kvec \over m} = \vvec,
:::

where $\vvec$ is the velocity of the incident beam. In magnitude, $J_inc = v$.

By our calculation $n_inc$ is dimensionless, and if you are fastidious you might want it to have dimensions of inverse volume (or particles per unit volume). If so you can multiply the wave function by a constant of dimensions $volume^{-3/2}$, but since the physical quantities we are interested in are independent of the normalization of the wave function, this is not necessary.

As for the scattered current, in the asymptotic region it is

:::{math}
:label: eq-introscatt-11
\Jvec_scatt \sim \Re\Bigl\{\Bigl[{e^{-ikr}\over r} f(\theta,\phi)^\cc\Bigr]\Bigl(-{i\hbar\over m}\Bigr) \Bigl[\del{e^{ikr}\over r}f(\theta,\phi)\Bigr]\Bigr\},
:::

which is only an asymptotic form since we are using the asymptotic form {eq}`eq-introscatt-5` of the scattered wave. To evaluate this we take the gradient of the scattered wave spherical coordinates (see {eq}`eq-vecident-20`,

:::{math}
:label: eq-introscatt-12
\del{e^{ikr}\over r}f(\theta,\phi)= {\hat{\mathbf{r}}}\Bigl[ {ik\,e^{ikr} \over r}\, f(\theta,\phi)\Bigr] + O\Bigl({1\over r^2}\Bigr),
:::

where we only carry the result to leading order in $1/r$. Substituting this into {eq}`eq-introscatt-8`, we find

:::{math}
:label: eq-introscatt-13
\Jvec_scatt \sim v\, {|f(\theta,\phi)|^2 \over r^2}\, {\hat{\mathbf{r}}}.
:::

To leading order, the asymptotic form of the scattered current is purely in the outward radial direction, as we expect. Terms in $\Jvec_scatt$ that go to zero faster than $1/r^2$ as $r\to\infty$ will not contribute to the counting rate, since the area of the aperture of the detector, for fixed $\Delta\Omega$, is proportional to $r^2$.

Now we integrate the scattered current over the aperture to the detector, which we assume is at large distance $r$ from the scatterer, and which has area $r^2\Delta\Omega$. The counting rate is

:::{math}
:label: eq-introscatt-14
\dod{w}{\Omega}\, \Delta\Omega = \int_aperture \Jvec_scatt \cdot d\avec = v |f(\theta,\phi)|^2 \,\Delta\Omega,
:::

where $d\avec$ is the area element of the aperture and $dw/d\Omega$ is the counting rate per unit solid angle. Now dividing this by $J_inc = v$, we obtain

:::{math}
:label: eq-introscatt-15
\dod{\sigma}{\Omega} = |f(\theta,\phi)|^2,
:::

a simple result. This equation explains the interest in finding $f(\theta,\phi)$, since it leads immediately to the differential cross , which is measurable. Notice that the counting rate, which is physically observable in a scattering experiment, depends only on the leading asymptotic form of the scattered wave function. One does not need to know the exact form of the scattered wave (at smaller values of $r$ where correction terms to the asymptotic expansion of the scattered wave are important, or in the scattering region where the potential is nonzero).

Now for some comments about this calculation. Notice that we computed the flux of the scattered particles intercepted by the detector, but we ignored the incident particles. In realistic scattering experiments the detector is usually located outside the beam, so incident particles do not enter it. Our incident wave {eq}`eq-introscatt-4` fills all of space, but that is an artifact of our model. In reality the beam will be cut off at some finite transverse size, and if the scattering angle is not too small, the detector can be located outside the beam.

If the scattering angle is very small, however, then the detector will have to be inside the beam and it will detect incident particles as well as scattered ones. The counting rate is still the particle flux intercepted by the aperture of the detector, but the flux is neither the incident flux nor the scattered flux nor the sum of the two, but rather the flux computed from the total wave function $\psi=\psi_inc + \psi_scatt$. Since the current is quadratic in the wave function, there are cross terms or interference terms between the incident wave and the scattered wave. Taking all these effects into account leads to the *optical theorem*, which we take up in \secrintroscatt-17.

(sec-introscatt-7)=

## Central Force Scattering

We now specialize to the important case of a central force potential, $V=V(r)$. The main simplification in this case is that the Schr\"odinger equation {eq}`eq-introscatt-1` is separable in spherical coordinates (see {ref}`ch-cenforce`), so the solutions can be written in the form

:::{math}
:label: eq-introscatt-16
\psi_{k\ell m}(\xvec) = \psi_{k\ell m}(r,\theta,\phi) = R_{k\ell}(r) Y_{\ell m}(\theta,\phi),
:::

where $R_{k\ell}(r)$ is a solution of version one of the radial Schr\"odinger equation, {eq}`eq-cenforce-7`, with potential $V(r)$. The radial eigenfunction $R_{k\ell}(r)$ is parameterized by $\ell$ because the radial Schr\"odinger equation contains $\ell$ in the centrifugal potential. It is also parameterized by the energy $E$, which we will normally indicate by an equivalent wave number $k$, given by $E=\hbar^2k^2/2m$. The three-dimensional solution $\psi$ depends on $k$, $\ell$ and $m$, as indicated in {eq}`eq-introscatt-16`. Of these, $k\ge0$ is a continuous index and $\ell$ and $m$ are discrete.

The solutions {eq}`eq-introscatt-16` of the Schr\"odinger equation do not satisfy the boundary conditions {eq}`eq-introscatt-3`--{eq}`eq-introscatt-5` that we require for a scattering solution, but they do form a complete set so the desired scattering solution can be expressed as a linear combination of them. Since the scattering solution is an energy eigenfunction of energy $E=\hbar^2 k^2/2m$ it can only be a linear combination of central force eigenfunctions {eq}`eq-introscatt-16` with the same energy, that is, there must be coefficients $A_{\ell m}$ such that

:::{math}
:label: eq-introscatt-17
\psi_\kvec(\xvec) = \sum_{\ell m} A_{\ell m}\, R_{k\ell}(r)\, Y_{\ell m}(\theta,\phi),
:::

where the $\kvec$ on the left and the $k$ on the right are related by $k=|\kvec|$. In a moment we will find the expansion coefficients $A_{\ell m}$ in terms of some simple parameters that characterize the potential (namely, the phase shifts $\delta_\ell$).

(sec-introscatt-8)=

## Free Particle Solutions

Free particle solutions were discussed in Secs. {ref}`sec-cenforce-6`{} --{ref}`sec-cenforce-8`. Here we recall some of that material and present some further facts that will be useful in scattering theory.

In the case of the free particle the radial Schr\"odinger equation {eq}`eq-cenforce-7` with energy $E=\hbar^2k^2/2m$ has two linearly independent solutions, $j_\ell(kr)$ and $y_\ell(kr)$, where $j_\ell$ and $y_\ell$ are the spherical Bessel functions. The small and large argument limiting forms of these Bessel functions are given by {eq}`eq-cenforce-27`--{eq}`eq-cenforce-30`. If the potential $V(r)$ is zero all the way down to $r=0$, that is, if the particle is free everywhere, then the $y$-type Bessel functions are not allowed because they diverge at $r=0$. Then a complete set of free particle energy eigenfunctions is

:::{math}
:label: eq-introscatt-18
\psi^free_{k\ell m}(r,\theta,\phi) = j_\ell(kr)\, Y_{\ell m}(\theta,\phi).
:::

But if we are seeking free particle solutions in some region away from $r=0$, such as in the asymptotic region of a scattering problem where the potential can be ignored, then the $y$-type solutions are also allowed.

The incident plane wave $e^{i\kvec\cdot\xvec}$ is a free particle solution of the Schr\"odinger equation that is obtained by separating the wave equation in rectangular coordinates, while the solutions {eq}`eq-introscatt-18` are obtained by separating in spherical coordinates. Thus the incident plane wave can be expressed as a linear combination of the solutions {eq}`eq-introscatt-18`. The expansion gives $e^{i\kvec\cdot\xvec}$ as a linear combination of the solutions {eq}`eq-introscatt-18` with the same energy. The expansion coefficients can be worked out with some use of recursion relations satisfied by the spherical Bessel functions and the Legendre polynomials. We omit details here, which may be found in textbooks such as Messiah, Sakurai or Commins. The result, however, is useful. It is

:::{math}
:label: eq-introscatt-19
e^{i\kvec\cdot\xvec} = \sum_{\ell m} 4\pi\, i^\ell j_\ell(kr) Y_{\ell m}^\cc({\hat{\mathbf{k}}}) Y_{\ell m}({\hat{\mathbf{r}}}),
:::

where ${\hat{\mathbf{r}}}$ and ${\hat{\mathbf{k}}}$ refer to the directions of the vectors $\xvec$ and $\kvec$ on the left hand side, where $Y_{\ell m}({\hat{\mathbf{r}}})$ means the same as $Y_{\ell m}(\theta,\phi)$ and where as usual $k=|\kvec|$.

This expansion can be rewritten with the use of the addition theorem for spherical harmonics, {eq}`eq-orbamsph-71`, which for present purposes we write in the form

:::{math}
:label: eq-introscatt-20
P_\ell({\hat{\mathbf{r}}}\cdot{\hat{\mathbf{k}}}) = P_\ell(\cos\gamma) = {4\pi \over 2\ell +1} \sum_m Y_{\ell m}^\cc({\hat{\mathbf{k}}}) Y_{\ell m}({\hat{\mathbf{r}}}),
:::

where $\gamma$ is the angle between $\xvec$ and $\kvec$. Then the expansion {eq}`eq-introscatt-19` becomes

:::{math}
:label: eq-introscatt-21
e^{i\kvec\cdot\xvec} = \sum_{\ell=0}^\infty i^\ell (2\ell+1) j_\ell(kr) P_\ell(\cos\gamma).
:::

Notice that if we take $\kvec$ to lie in the $z$-direction, $\kvec = k{\hat{\mathbf{z}}}$, then $\gamma$ is the same as $\theta$, the usual spherical coordinate. In that case, the incident plane wave becomes

:::{math}
:label: eq-introscatt-22
e^{i\kvec\cdot\xvec} = e^{ikr\cos\theta}=e^{ikz},
:::

that is, it is independent of the azimuthal angle $\phi$, and the sum {eq}`eq-introscatt-21` is the expansion of the plane wave in Legendre polynomials of $\cos\theta$.

The spherical Bessel functions $j_\ell$ and $y_\ell$ are real, but complex linear combinations of them are often useful. These are the *spherical Hankel functions*, defined by

:::{math}
:label: eq-introscatt-23
\begin{aligned}
h^{(1)}_\ell(\rho) &= j_\ell(\rho) + i y_\ell(\rho), \\
h^{(2)}_\ell(\rho) &= j_\ell(\rho) - i y_\ell(\rho). \\

\end{aligned}
:::

The two types of spherical Hankel functions are complex conjugates of each other,

:::{math}
:label: eq-introscatt-24
h^{(1)}_\ell(\rho) = h^{(2)}_\ell(\rho)^\cc.
:::

These functions have particularly simple asymptotic forms when $\rho\gg\ell$, namely,

:::{math}
:label: eq-introscatt-25
\begin{aligned}
h^{(1)}_\ell(\rho) &=i^{-(\ell+1)}\,{e^{i\rho} \over \rho}, \\
h^{(2)}_\ell(\rho) &=i^{\ell+1}\,{e^{-i\rho} \over \rho}, 
\end{aligned}
:::

which are equivalent to {eq}`eq-cenforce-29`--{eq}`eq-cenforce-30`. The phases $i^{\pm(\ell+1)}$ that makes these expressions look complicated are just conventions. Otherwise the asymptotic forms of the spherical Hankel functions are just $e^{\pm i\rho}/\rho$, corresponding in scattering problems to incoming and outgoing spherical waves.

(sec-introscatt-9)=

## Partial Waves

The exact solution of the Schr\"odinger equation $\psi_\kvec(\xvec)$ is decomposed into incident and scattered waves according to

:::{math}
:label: eq-introscatt-26
\psi_\kvec(\xvec) = e^{i\kvec\cdot\xvec} +\psi_scatt(\xvec),
:::

as in {eq}`eq-introscatt-3`. The angular dependence of the total wave $\psi_\kvec(\xvec)$ and that of the incident wave $e^{i\kvec\cdot\xvec}$ are represented as linear combinations of $Y_{\ell m}$'s by {eq}`eq-introscatt-17` and {eq}`eq-introscatt-19`, respectively. Let us similarly decompose the angular dependence of the scattered wave by writing

:::{math}
:label: eq-introscatt-27
\psi_scatt(\xvec) = \psi_scatt(r,\theta,\phi) =\sum_{\ell m} S_{\ell m}(r) \, Y_{\ell m}(\theta,\phi),
:::

where the functions $S_{\ell m}(r)$ are effectively the radial wave functions of the scattered wave,

:::{math}
:label: eq-introscatt-28
S_{\ell m}(r) =\int d\Omega \, Y_{\ell m}^\cc(\theta,\phi) \, \psi_scatt(r,\theta,\phi).
:::

Then {eq}`eq-introscatt-26` can be written

:::{math}
:label: eq-introscatt-29
\sum_{\ell m} A_{\ell m}\, R_{k\ell}(r)\, Y_{\ell m}({\hat{\mathbf{r}}})= \sum_{\ell m} 4\pi \, i^\ell \, j_\ell(kr) Y_{\ell m}({\hat{\mathbf{r}}}) Y_{\ell m}^\cc({\hat{\mathbf{k}}}) +\sum_{\ell m} S_{\ell m}(r) \, Y_{\ell m}({\hat{\mathbf{r}}}).
:::

This equation is exact. But the $Y_{\ell m}$'s are linearly independent so {eq}`eq-introscatt-29` is equivalent to

:::{math}
:label: eq-introscatt-30
A_{\ell m}\, R_{k\ell}(r) = 4\pi \, i^\ell \, j_\ell(kr) \, Y_{\ell m}^\cc({\hat{\mathbf{k}}}) +S_{\ell m}(r).
:::

Now we extract the leading asymptotic forms of the three terms in {eq}`eq-introscatt-30` as $r\to\infty$. As for the total wave function, we need the asymptotic form of $R_{k\ell}(r)$. We argue that if $V(r)$ falls off rapidly enough then at large $r$ it can be ignored and $R_{k\ell}(r)$ must be a linear combination of the free particle solutions $j_\ell(kr)$ and $y_\ell(kr)$. Precisely how fast $V(r)$ must fall off for this to be true is examined in \secrintroscatt-10. Actually, it is more convenient to use the spherical Hankel functions and to write

:::{math}
:label: eq-introscatt-31
R_{kl}(r) \sim B_\ell \,h^{(1)}_\ell(kr) + B_\ell^\cc \, h^{(2)}_\ell(kr),
:::

where $B_\ell$ and $B_\ell^\cc$ are the coefficients of the linear combination. Here we are assuming that the exact radial wave function $R_{kl}(r)$ has been chosen to be real, as we can do since the radial wave equation is a real equation. This means that the coefficients of the linear combination of the spherical Hankel functions must be complex conjugates of each other, as shown, because of {eq}`eq-introscatt-24`. Thus the phase of $R_{k\ell}(r)$ is specified to within a $\pm$ sign, but its normalization has not been specified. The right-hand side of {eq}`eq-introscatt-31` is a good approximation to the left-hand side when $r$ is large enough that the potential can be neglected.

We now break $B_\ell$ into its magnitude and phase,

:::{math}
:label: eq-introscatt-32
B_\ell = |B_\ell|\, e^{i\delta_\ell},
:::

and absorb the magnitude $|B_\ell|$ into the normalization of $R_{k\ell}(r)$. This fixes the normalization of the radial wave functions; they are now determined to within a $\pm$ sign. Then we have

:::{math}
:label: eq-introscatt-33
R_{k\ell}(r) \sim e^{i\delta_\ell}\, h^{(1)}_\ell(kr) + e^{-i\delta_\ell}\, h^{(2)}_\ell(kr),
:::

or, if we replace the Hankel functions by their asymptotic forms {eq}`eq-introscatt-25`, valid when $kr\gg\ell$,

:::{math}
:label: eq-introscatt-34
R_{k\ell}(r) \sim {1\over kr} \bigl[ i^{-(\ell+1)}\,e^{i(kr+\delta_\ell)} + i^{\ell+1}\, e^{-i(kr+\delta_\ell)} \bigr].
:::

This is the asymptotic form of the radial wave functions; it is parameterized by the *phase shifts* $\delta_\ell$, which play a fundamental role in central force scattering.

As for the incident wave in {eq}`eq-introscatt-30`, it is a plane wave whose radial wave functions are the Bessel functions $j_\ell(kr)$. These have the asymptotic form

:::{math}
:label: eq-introscatt-35
j_\ell(kr) = {1\over 2}\bigl[ h^{(1)}_\ell(kr) + h^{(2)}_\ell(kr)\bigr] \sim {1\over 2kr}\bigl[i^{-(\ell+1)}\, e^{ikr} + i^{\ell+1}\, e^{-ikr}\bigr],
:::

which follows from {eq}`eq-introscatt-23` and {eq}`eq-introscatt-25`.

Finally, for the scattered wave in {eq}`eq-introscatt-30` we use {eq}`eq-introscatt-5` in {eq}`eq-introscatt-28` to obtain

:::{math}
:label: eq-introscatt-36
S_{\ell m}(r) \sim {e^{ikr}\over r}\, f_{\ell m},
:::

where the $f_{\ell m}$ are the expansion coefficients of the scattering amplitude when expanded as a linear combination of $Y_{\ell m}$'s,

:::{math}
:label: eq-introscatt-37
f(\theta,\phi)=\sum_{\ell m} f_{\ell m} \, Y_{\ell m}(\theta,\phi).
:::

Altogether, when we take the leading asymptotic form of all three terms in {eq}`eq-introscatt-30` we obtain

:::{math}
:label: eq-introscatt-38
\begin{aligned}
A_{\ell m} & {1\over kr} \bigl[i^{-(\ell+1)}\, e^{i(kr+\delta_\ell)}+ i^{\ell+1}\, e^{-i(kr+\delta_\ell)}\bigr] \\
&= 4\pi\,i^\ell {1\over 2kr}\bigl[i^{-(\ell+1)}\, e^{ikr} + i^{\ell+1}\,e^{-ikr} \bigr]\, Y_{\ell m}^\cc({\hat{\mathbf{k}}}) +{e^{ikr}\over r}\, f_{\ell m}. \\

\end{aligned}
:::

All three terms go as $1/r$ at large $r$, so we have obtained the leading asymptotic term of the entire equation {eq}`eq-introscatt-30`, and this is exact. The result is a linear combination of incoming and outgoing spherical waves, which are linearly independent; notice that that the scattered wave only has an outgoing part (this is the boundary condition imposed by the physics).

Working first with the coefficients of the incoming wave $e^{-ikr}/r$ we see that we can solve for the coefficients $A_{\ell m}$ in terms of the phase shifts. We find

:::{math}
:label: eq-introscatt-39
A_{\ell m} = 4\pi\,i^\ell {1\over 2} Y_{\ell m}^\cc({\hat{\mathbf{k}}})\, e^{i\delta_\ell}.
:::

Then using this in the outgoing part, we can solve for the expansion coefficients $f_{\ell m}$ of the scattering amplitude. In the algebra it helps to notice that

:::{math}
:label: eq-introscatt-40
{e^{2i\delta_\ell} -1 \over 2i} = e^{i\delta_\ell} \, \sin\delta_\ell.
:::

Thus we find

:::{math}
:label: eq-introscatt-41
f_{\ell m} = {4\pi \over k} e^{i\delta_\ell}\, \sin\delta_\ell \, Y_{\ell m}^\cc({\hat{\mathbf{k}}}),
:::

or,

:::{math}
:label: eq-introscatt-42
f(\theta,\phi) = {4\pi \over k} \sum_{\ell m} e^{i\delta_\ell} \, \sin\delta_\ell \, Y_{\ell m}({\hat{\mathbf{r}}}) Y_{\ell m}^\cc({\hat{\mathbf{k}}}).
:::

This is the desired result, which expresses the scattering amplitude in terms of the phase shifts $\delta_\ell$. Another version is obtained with the help of the addition theorem {eq}`eq-introscatt-20`,

:::{math}
:label: eq-introscatt-43
f(\theta) = {1\over k} \sum_{\ell=0}^\infty (2\ell+1) e^{i\delta_\ell} \, \sin\delta_\ell \, P_\ell(\cos\theta),
:::

where we have set $\kvec=k{\hat{\mathbf{z}}}$ so that ${\hat{\mathbf{r}}}\cdot{\hat{\mathbf{k}}}=\cos\theta$, where $\theta$ is the usual spherical angle. When $\kvec=k{\hat{\mathbf{z}}}$ it is obvious that the whole central force scattering problem is symmetric under rotations about the $z$-axis so $f$ must be a function of $\theta$ alone. Expressions {eq}`eq-introscatt-42` or {eq}`eq-introscatt-43` are the *partial wave* expansion of the scattering amplitude. We shall discuss this result momentarily, but first we examine an important point that we have glossed over so far.

(sec-introscatt-10)=

## Asymptotic Form of the Radial Wave Functions

In the derivation of the partial wave expansion we assumed [see {eq}`eq-introscatt-31`] that if the potential dies off rapidly enough with distance, then at large distances the radial eigenfunctions approach linear combinations of free particle solutions. Let us now examine how rapidly $V(r)$ must die off for this to be true.

As explained in {ref}`ch-cenforce`, the radial eigenfunction $R_{k\ell}(r)$ is related to an alternative version of the radial eigenfunction $u_{k\ell}(r) = rR_{k\ell}(r)$, which satisfies version two of the radial Schr\"odinger equation, {eq}`eq-cenforce-11`. (Function $u$ was called $f$ in {ref}`ch-cenforce`.) For our present purposes we rearrange these two versions of the radial Schr\"odinger equation as

:::{math}
:label: eq-introscatt-44
{1\over r^2} \dod{}{r}\Bigl( r^2 \dod{R_{k\ell}}{r}\Bigr) + k^2 R_{k\ell}(r) = W(r) R_{k\ell}(r)
:::

and

:::{math}
:label: eq-introscatt-45
u''_{k\ell}(r) + k^2 u_{k\ell}(r) = W(r) u_{k\ell}(r),
:::

where

:::{math}
:label: eq-introscatt-46
W(r) = {\ell(\ell+1)\over r^2} + {2m\over\hbar^2} V(r).
:::

Since both the true potential and the centrifugal potential go to zero as $r\to\infty$, the function $W(r)$ also goes to zero as $r\to\infty$. So as a first stab at analyzing the asymptotic form of $u_{k\ell}(r)$, let us neglect $W(r)$ altogether on the right hand side of the radial Schr\"odinger equation {eq}`eq-introscatt-45`. Then the solution for $u_{k\ell}(r)$ is simply a linear combination of the exponentials $e^{\pm ikr}$, and $R(r)$ is a linear combination of $e^{\pm ikr}/r$, as we assumed in {eq}`eq-introscatt-34`.

To take into account the effects of $W(r)$, let us write the solution of {eq}`eq-introscatt-45` as

:::{math}
:label: eq-introscatt-47
u_{k\ell}(r) = e^{g(r)\pm ikr},
:::

where $g(r)$ is a correction that will account for the effects of the function $W(r)$. If we can show that $g(r)\to 0$ as $r\to\infty$, then the correct asymptotic forms of $u_{k\ell}(r)$ will be a linear combination of the solutions $e^{\pm ikr}$. That is, the function $W(r)$ on the right hand side will make no difference in the asymptotic form of the solution. Substituting {eq}`eq-introscatt-47` into the radial Schr\"odinger equation {eq}`eq-introscatt-45`, we obtain an equation for $g$,

:::{math}
:label: eq-introscatt-48
g'' + g^{\prime\,2} \pm 2ikg' = W(r).
:::

This is rigorously equivalent to {eq}`eq-introscatt-45`.

Now we consider the behavior of $W(r)$ as $r\to\infty$. If the true potential $V(r)$ goes to zero faster than $1/r^2$, then $W(r)$ is dominated by the centrifugal potential and also goes to zero as $1/r^2$. We assume $\ell\ne0$, so the centrifugal potential does not vanish. If the true potential goes to zero more slowly than $1/r^2$, let us assume that it does so as a power law, $1/r^p$, where $1<p\le 2$. This excludes the case of the Coulomb potential, for which $p=1$, but it approaches the Coulomb potential as $p\to1$. Then $W(r)$ has the asymptotic form,

:::{math}
:label: eq-introscatt-49
W(r) \sim {a\over r^p},
:::

where $1<p\le 2$ and $a$ is a constant. The case $\ell=0$ can be handled as a special case, but it does not change any of the conclusions that we shall draw.

We are interested in solving {eq}`eq-introscatt-48` in the asymptotic region when $W$ has the asymptotic behavior {eq}`eq-introscatt-49`. Let us assume that $g$ is asymptotically given by a power law,

:::{math}
:label: eq-introscatt-50
g(r) \sim {b\over r^s},
:::

where $b$ is another constant and $s>0$. Then the three terms on the left hand side of {eq}`eq-introscatt-48` go as $1/r^{s+2}$, $1/r^{2s+2}$ and $1/r^{s+1}$, in that order. The third term dominates, so to leading order we have $s=p-1$, so that $0<s\le 1$, and the power law ansatz for $g$ has a solution. That is, $g(r)\sim b/r^{p-1}$, $g(r)$ does go to zero as $r\to\infty$, and thus the asymptotic form of $u_{k\ell}(r)$ is a linear combination of $e^{\pm ikr}$.

But in the case of the Coulomb potential, $W(r) \sim a/r$, that is, with $p=1$. Then taking the dominant term in {eq}`eq-introscatt-48`, we have

:::{math}
:label: eq-introscatt-51
\pm 2ik g'(r) = {a\over r},
:::

or,

:::{math}
:label: eq-introscatt-52
g(r) = \mp {ia\over 2k}\ln(kr).
:::

The logarithm does not go to zero as $r\to\infty$, in fact, it increases without bound (although very slowly). Thus, in the case of the Coulomb potential, the asymptotic form of the radial wave function is

:::{math}
:label: eq-introscatt-53
u_{k\ell}(r) \sim \exp\Bigl\{\pm i\Bigl[kr - {a\over 2k} \ln(kr) \Bigr]\Bigr\}.
:::

The Coulomb potential gives rise to long range, logarithmic phase shifts that do not approach the free particle phases as $r\to\infty$.

In summary, if the potential $V(r)$ goes to zero faster than $1/r$, then the asymptotic form of the radial wave function is given by the linear combinations $e^{\pm ikr}$ (for $u_{k\ell}$) or by $e^{\pm ikr}/r$ (for $R_{k\ell}$), the latter of which is what we assumed in the derivation of the partial wave expansion {eq}`eq-introscatt-42` or {eq}`eq-introscatt-43`. For the rest of these notes we will assume that $V(r)$ does satisfy this condition, thereby excluding the Coulomb potential.

By the way, the derivation of {eq}`eq-introscatt-30` did not make any assumption about the asymptotic behavior of $S_{kl}(r)$, but now we have shown that if $V(r)\to0$ faster than $1/r$ then $R_{kl}(r) \sim e^{\pm ikr}/r$, so in that case $S_{kl}(r)$ has the same behavior. Then if we choose outgoing boundary conditions we obtain the form {eq}`eq-introscatt-5` for the scattered wave. In the case of the Coulomb potential, however, the form {eq}`eq-introscatt-5` of the scattered wave is not correct.

(sec-introscatt-11)=

## Partial Wave Expansion of the Cross Section

We return to the partial wave expansion of the scattering amplitude, {eq}`eq-introscatt-42` or {eq}`eq-introscatt-43`, which give the scattering amplitude as a linear combination of spherical harmonics or Legendre polynomials. Squaring the scattering amplitude we obtain the differential cross ,

:::{math}
:label: eq-introscatt-54
\dod{\sigma}{\Omega}(\theta,\phi) = \Bigl({4\pi \over k}\Bigr)^2 \sum_{\ell m \ell' m'} e^{i(\delta_\ell-\delta_{\ell'})} \, \sin\delta_\ell \, \sin\delta_{\ell'} \, Y_{\ell m}^\cc({\hat{\mathbf{k}}}) \, Y_{\ell'm'}({\hat{\mathbf{k}}}) \, Y_{\ell m}({\hat{\mathbf{r}}}) \, Y_{\ell'm'}^\cc({\hat{\mathbf{r}}}),
:::

or, with $\kvec=k{\hat{\mathbf{z}}}$,

:::{math}
:label: eq-introscatt-55
\dod{\sigma}{\Omega}(\theta) = {1\over k^2} \sum_{\ell\ell'} (2\ell+1)(2\ell'+1)e^{i(\delta_\ell-\delta_{\ell'})} \, \sin\delta_\ell \, \sin\delta_{\ell'} \, P_\ell(\cos\theta) \, P_{\ell'}(\cos\theta).
:::

These expressions have cross terms that do not simplify, but which show up experimentally as oscillations in the angular dependence of the differential cross . Some of these may be seen in Figs.~{ref}`fig-introscatt-8` or {ref}`fig-introscatt-9`.

On the other hand, when we integrate over all angles to obtain the total cross , the cross terms integrate to zero. This is easiest to see in the form {eq}`eq-introscatt-54`, due to the orthonormality of the $Y_{\ell m}$'s. The result is

:::{math}
:label: eq-introscatt-56
\sigma = \int d\Omega \, \dod{\sigma}{\Omega} = \Bigl({4\pi\over k}\Bigr)^2 \sum_{\ell m} \sin^2\delta_\ell \, Y_{\ell m}^\cc({\hat{\mathbf{k}}}) \, Y_{\ell m}({\hat{\mathbf{k}}}),
:::

or, with another application of the addition theorem (and noting that ${\hat{\mathbf{k}}}\cdot{\hat{\mathbf{k}}}=1$ and $P_\ell(1)=1$),

:::{math}
:label: eq-introscatt-57
\sigma = {4\pi\over k^2} \sum_{\ell=0}^\infty (2\ell+1) \sin^2\delta_\ell.
:::

This is the partial wave expansion of the total cross .

(sec-introscatt-12)=

## The Phase Shifts $\delta_\ell$

These results show the importance of the phase shifts $\delta_\ell$, which determine the coefficients of the angular expansion of the scattering amplitude and cross . We now make some comments on the properties and intuitive meaning of these phase shifts.

The phase shifts are defined by the asymptotic form of the radial wave functions {eq}`eq-introscatt-34` and are determined by the potential $V(r)$. That is, $\delta_\ell$ is the phase of the incoming or outgoing part of the exact radial wave function, relative to that of a free particle. Thus, the phase shifts vanish for a free particle. The phase shifts depend on $\ell$ because the radial wave function does so. They depend on the energy, too, and if we wish to emphasize this we can write $\delta_\ell(E)$. Since by our analysis the phase of the radial wave is determined to within a $\pm$ sign, the phase shift $\delta_\ell$ is determined to within an integer multiple of $\pi$.

For an intuitive view of the phase shifts we can imagine launching spherical waves inward at the scatterer from a large distance, allowing them to converge on the origin and then bounce back. The wave can be given an angular modulation proportional to a $Y_{\ell m}$ to give it a dependence on $\ell$. Then we will find a certain phase shift in the reflected wave compared to the incident wave. We can do this both for the free particle and the one with a potential; the difference in the phase shifts in the two cases is $\delta_\ell$.

As a more practical matter, the phase shifts can be determined by solving the radial wave equation somehow and then comparing the asymptotic form of the solution with the form {eq}`eq-introscatt-34` to get the phase shifts. In some cases this can be done analytically, and it can also be done numerically. For the latter one simply chooses regular boundary conditions for $R(r)$ at $r=0$, and then integrates the radial Schr\"odinger equation outward numerically. When a radius is reached where the potential is negligible a comparison of the numerical solution to {eq}`eq-introscatt-33` gives the phase shifts. Another approach is to use WKB theory; since the radial wave equation is one-dimensional, WKB theory can be very effective in obtaining information about the radial wave function. Some aspects of this approach were explored in Prob. {ref}`prob-wkb-4`.

WKB theory leads easily to some general conclusions about the phase shifts. Suppose we have a well localized potential, for example, one that dies off exponentially with $r$ such as the Yukawa potential {eq}`eq-tdpt-116`. Let $a$ be a measure of the range of the potential. Then the centrifugal potential, which only falls off as $1/r^2$, will dominate for large $r$ if $\ell>0$. Thus for a given $E$, if $\ell$ is big enough the radial turning point in the centrifugal potential will lie outside the range $a$ of the true potential, and the radial wave function will be able to reach the true potential only by tunneling through the centrifugal potential. The wave function decays exponentially in the classically forbidden region, so for such large $\ell$ values the true potential will have only an exponentially small influence on the wave function, which will be nearly the same as a free particle radial wave function of the same value of $\ell$ and $E$. Thus for such large $\ell$ values we expect the phase shifts to be small, and to decay exponentially with $\ell$ as $\ell$ increases beyond a certain cutoff.

To estimate the $\ell$ value beyond which such behavior holds, we set the nominal turning point in the centrifugal potential to the range of the true potential, that is,

:::{math}
:label: eq-introscatt-58
E = {\hbar^2 k^2\over 2m} = {\ell(\ell+1)\hbar^2 \over 2m a^2}.
:::

If we ignore the difference between $\ell$ and $\ell+1$, this gives the estimate,

:::{math}
:label: eq-introscatt-59
\ell_cutoff = ka,
:::

beyond which the phase shifts decay exponentially toward $\delta_\ell=0$. In summary, for a well localized potential of range $a$, an estimate of the number of terms that contribute significantly to the partial wave expansion is $ka$.

This means that for well localized potentials such as the Yukawa potential, the partial wave sum {eq}`eq-introscatt-57` converges, and the total cross is finite. A more careful WKB analysis is capable of giving more precise conditions on the potential for the total cross to be finite.

(sec-introscatt-13)=

## Hard Sphere Scattering

As an example of the partial wave expansion, let us consider scattering from a hard sphere. The potential is

:::{math}
:label: eq-introscatt-60
\begin{aligned}
V(r)=\begin{cases}\infty, &r<a, \\ 0, &r>a,\end{cases}
\end{aligned}

:::

where $a$ is the radius of the sphere. In the region $r>a$ the solution is a linear combination of free particle solutions, which we write as

:::{math}
:label: eq-introscatt-61
R_{kl}(r) = B_\ell \,h^{(1)}_\ell(kr) + B_\ell^\cc \, h^{(2)}_\ell(kr),
:::

which is the same as {eq}`eq-introscatt-31` except for the hard sphere it is exact and {eq}`eq-introscatt-31` was only an asymptotic form. As in the analysis of {eq}`eq-introscatt-31` we write $B_\ell =|B_\ell| e^{i\delta_\ell}$ and absorb $|B_\ell|$ into the normalization of the $R_{k\ell}(r)$, so that $\delta_\ell$ are the phase shifts.

These are determined by imposing the boundary condition that $R_{kl}(r)$ vanish at the surface of the sphere,

:::{math}
:label: eq-introscatt-62
R_{kl}(a) = e^{i\delta_\ell}\,h^{(1)}_\ell(ka) + e^{-i\delta_\ell}\, h^{(2)}_\ell(ka) = 0,
:::

or,

:::{math}
:label: eq-introscatt-63
e^{2i\delta_\ell} = -{h^{(2)}_\ell(ka) \over h^{(1)}_\ell(ka)}.
:::

This can be solved for the $\delta_\ell$, which give us the scattering amplitude and differential cross . We will consider two limiting cases, in which the limiting forms of the spherical Bessel functions can be used.

(sec-introscatt-14)=

## The limit $ka\ll 1$

In the first case we assume $ka\ll 1$. This is equivalent to $\lambda\gg a$, where $\lambda=2\pi/k$ is the wavelength of the incident waves, that is, the scatterer is much smaller than a wavelength. The small argument forms of $j_\ell$ and $y_\ell$, {eq}`eq-cenforce-27` and {eq}`eq-cenforce-28`, show that in this case $y_\ell(ka)$ is large and negative and $j_\ell(ka)$ is small and positive. We write {eq}`eq-introscatt-63` as

:::{math}
:label: eq-introscatt-64
e^{2i\delta_\ell} = -{j_\ell(ka) -iy_\ell(ka) \over j_\ell(ka)+iy_\ell(ka)} = {1+i (j_\ell/y_\ell) \over 1 -i(j_\ell/y_\ell)} = 1+2i(j_\ell/y_\ell) =e^{2i(j_\ell/y_\ell)},
:::

valid when $j_\ell(ka)/y_\ell(ka)$ is small, as here. Thus we find, to a good approximation,

:::{math}
:label: eq-introscatt-65
\delta_\ell={j_\ell(ka)/y_\ell(ka)} = -{(ka)^{2\ell+1} \over (2\ell-1)!!(2\ell+1)!!}.
:::

Since $ka\ll1$, this shows that not only is the lowest phase shift $\delta_0$ small, the higher phase shifts $\delta_\ell$ for $\ell\ge1$ are even smaller. In this limit

:::{math}
:label: eq-introscatt-66
\delta_0 = -ka,
:::

and the series {eq}`eq-introscatt-43` for the scattering amplitude is dominated by the single term $\ell=0$. Thus we have

:::{math}
:label: eq-introscatt-67
f(\theta) = {1\over k}(-ka) = -a, \qquad ka\ll 1,
:::

since $e^{i\delta_\ell}\approx 1$ and $P_0(\cos\theta)=1$. We see that the differential cross is independent of angle,

:::{math}
:label: eq-introscatt-68
{d\sigma\over d\Omega} = a^2,
:::

and the total cross is

:::{math}
:label: eq-introscatt-69
\sigma = \int d\Omega \, {d\sigma\over d\Omega} = 4\pi a^2.
:::

The total cross is four times as large as the geometrical cross-al area of the small sphere. The classical cross is just this cross-al area, $\pi a^2$, but the regime $\lambda \gg a$ is the one in which we expect classical mechanics to be a poor approximation to quantum mechanics, so we should not be surprised by the difference.

(sec-introscatt-15)=

## $s$-wave Scattering

When the partial wave $\ell=0$ dominates the expansion of the scattering amplitude, we speak of *$s$-wave scattering*. The scattered wave is isotropic and has an equal intensity in all directions, including the forward direction. Since $a\ll\lambda$ the sphere is too small to create a shadow; instead, the incident wave effectively wraps all the way around the scatterer. As we will see later, $s$-wave scattering applies to any localized potential whose characteristic size $a$ satisfies $a\ll\lambda$, that is, $ka\gg 1$ (not just hard spheres). The fundamental reason was given in \secrintroscatt-12: for $\ell>0$ the radial wave functions must tunnel through the centrifugal potential to reach the scatterer, and the tunneling is deeper the higher the $\ell$ value. We see from {eq}`eq-introscatt-65` that when $ka\ll 1$ the phase shifts are indeed an exponentially decreasing function of $\ell$ (in fact, including the factorials, even faster than exponential).

There are many physical examples in which $s$-wave scattering is important. For example, a Bose-Einstein condensate is a dilute gas of atoms at a temperature at which the de~Broglie wavelength $\lambda$ of the atoms due to their thermal motion is larger than the interparticle separation. Since the gas is dilute, the interparticle separation in turn is much larger than the atomic size, call it $a$, so we have $\lambda\gg a$, or $ka\ll 1$. Thus the interactions of the atoms with one another is described by $s$-wave scattering, and scattering of atoms by atoms, in all its complexity, is described by a single parameter, which is the phase shift $\delta_0$.

In $s$-wave scattering any two potentials that give the same phase shift $\delta_0$ will have the same effect. Therefore in theoretical models the exact potential can be replaced by a simpler one, as long as the phase shift is the same. Delta function potentials are popular for this purpose, which explains their appearance in the models of Bose-Einstein condensates such as the Gross-Pitaevski equation (for which see Prob. {ref}`prob-hartfock-3`).

When light scatters from particles that are much smaller than the wavelength, for example, when optical radiation is scattered by atoms in a gas, is this $s$-wave scattering, and is the scattered wave isotropic? (This is a tricky question.) The answer is no, because electromagnetic waves are vector waves, not scalar waves as we have been discussing in these notes. In the case of electromagnetic waves, the scattering when $ka\ll 1$ is dominated by dipole radiation, which has a nontrivial angular dependence. Electromagnetic waves have no monopole radiation (that is, $s$-wave radiation), and the next higher term in the multipole series is the first one to appear. It is the one that dominates at small $ka$.

Similarly, gravitational radiation, which has received much attention since its actual detection a few years ago, has neither a monopole nor a dipole term, rather the first multipole to appear is the quadrupole.

(sec-introscatt-16)=

## The Limit $ka\gg 1$

The second case we consider is the opposite extreme, $ka\gg 1$, that is, $\lambda\ll a$. In this case the sphere is much larger than a wavelength. Now there are many $\ell$ values that contribute to the partial wave sum. For small $\ell$, for which $\ell\ll ka$, we can use the asymptotic forms {eq}`eq-introscatt-25` in {eq}`eq-introscatt-63`. We find

:::{math}
:label: eq-introscatt-70
e^{2i\delta_\ell} = - e^{-2i[ka-(\ell+1)\pi/2]},
:::

or, with $-1=e^{-i\pi}$,

:::{math}
:label: eq-introscatt-71
\delta_\ell = {\ell\pi\over 2}-ka.
:::

This says that $\delta_\ell$ advances by $\pi/2$ when $\ell$ increases by 1, but this is an approximation that is only valid when $\ell\ll ka$. According to {eq}`eq-introscatt-59` we need to sum the partial wave expansion out to $\ell \approx ka$, after which we expect the terms of the series to rapidly approach zero. Actually the increment in $\delta_\ell$, which is indeed $\pi/2$ when $\ell\ll ka$, gradually decreases as $\ell$ climbs toward $ka$, after which it rapidly goes to zero. This behavior is illustrated in some numerical examples in Figs.~{ref}`fig-introscatt-4` and {ref}`fig-introscatt-5`.

:::{figure} images/introscatt-fig04.png
:label: fig-introscatt-4
:width: 80%

Phase shifts in hard sphere scattering. The phase shifts $\delta_\ell$ are represented as points on a circle with plane polar angle $\delta_\ell$. The radius of the circle grows as $\ell$ increases, to keep the points from getting mixed up with each other as they orbit the circle. Some points are labeled with their $\ell$ values. The phase shifts increase with decreasing increment as $\ell$ increases, until $\ell\approx ka$, whereupon $\delta_\ell\to0$. Plot is for $ka=10$.
:::

:::{figure} images/introscatt-fig05.png
:label: fig-introscatt-5
:width: 80%

Same as {ref}`fig-introscatt-4` except $ka=20$.
:::


The cutoff at $\ell\approx ka$ was explained earlier in terms of WKB theory; a more intuitive explanation is illustrated in {ref}`fig-introscatt-6`. We imagine particles of fixed energy $E=\hbar^2k^2/2m$ emitted in various directions from a point on the surface of a sphere of radius $a$. These represent the waves scattered by the sphere. The angular momentum of the particles depends on the direction of emission; its minimum value is $L=0$ when the particles are launched in the radial direction, and its maximum value $L=pa=\hbar ka$ is when the particles are launched tangentially to the sphere. The maximum value of $L$ corresponds to a maximum angular momentum quantum number, $\ell=L/\hbar = ka$. The same reasoning works for any short-range potential with an effective range of $a$; the partial wave expansion cuts off near $\ell\approx ka$.

:::{figure} images/introscatt-fig06.png
:label: fig-introscatt-6
:width: 80%

Particles of fixed energy are launched in various directions from a point on the surface of a sphere. The maximum angular momentum is achieved when the direction is tangent to the sphere at the point of launch.
:::

We can use the behavior of the phase shifts to estimate the total cross in the limit $ka\gg 1$. While the points representing the $\delta_\ell$ are orbiting their circle as in Figs.~{ref}`fig-introscatt-4` and {ref}`fig-introscatt-5`, the average value of $\sin^2\delta_\ell$ is $1/2$. Since the series cuts off near $\ell\approx ka$, the total cross {eq}`eq-introscatt-57` can be estimated by

:::{math}
:label: eq-introscatt-72
\sigma \approx {4\pi\over k^2} \sum_{\ell=0}^{ka} (2\ell+1){1\over 2}.
:::

Using the sum

:::{math}
:label: eq-introscatt-73
\sum_{\ell=0}^L (2\ell+1) = (L+1)^2,
:::

we obtain the estimate

:::{math}
:label: eq-introscatt-74
\sigma \approx {4\pi\over k^2} {(ka)^2\over 2} = 2\pi a^2,
:::

where we ignore the difference between $ka$ and $ka+1$. We see that the cross is twice the classical value in the case $ka\gg 1$.

These conclusions are confirmed by detailed calculations, which show that $\sigma\to 4\pi a^2$ as $ka\to0$ and $\sigma\to 2\pi a^2$ as $ka\to\infty$. See {ref}`fig-introscatt-7`.

:::{figure} images/introscatt-fig07.png
:label: fig-introscatt-7
:width: 80%

Total cross $\sigma$ as a multiple of $\pi a^2$ for hard sphere scattering as a function of $ka$. The total cross has the limits $\sigma\to 4\pi a^2$ as $ka\to0$ and $\sigma\to 2\pi a^2$ as $ka\to\infty$.
:::

If we think of the classical limit as one in which the de~Broglie wavelength $\lambda$ is much smaller than the scale of the potential, then it is surprising that the limit $\sigma\to 2\pi a^2$ as $ka\to\infty$ since this is twice the classical cross , $\pi a^2$. To see how this “extra” cross-is distributed in angle we refer to {ref}`fig-introscatt-8`, a plot of the differential cross for various values of $ka$.

:::{figure} images/introscatt-fig08.png
:label: fig-introscatt-8
:width: 80%

Differential cross in hard sphere scattering, as a multiple of $a^2$. Curves are labeled by the value of $ka$, which increases from 0.1 to 8. Scattering angle $\theta$ is measured in degrees.
:::

:::{figure} images/introscatt-fig09.png
:label: fig-introscatt-9
:width: 80%

Same as {ref}`fig-introscatt-8` except multiplied by $\sin\theta$. Area under curves in a given angle range is proportional to the total cross in that range.
:::


{ref}`fig-introscatt-8` shows that for small values of $ka$, the differential cross is nearly independent of angle, confirming that we have $s$-wave scattering. The cross $d\sigma/d\Omega$ is nearly $a^2$ in this range, confirming {eq}`eq-introscatt-68`. As $ka$ increases, $d\sigma/d\Omega$ decreases at large angles toward the classical value, but at small angles a forward peak rises up, growing narrower and higher. At the edge of forward peak there also arise oscillations. {ref}`fig-introscatt-9` is a similar plot except that $d\sigma/d\Omega$ has been multiplied by $\sin\theta$, which makes the integrated cross proportional to area under the curve. This makes it easier to see that the total cross in the forward peak is about the same as the classical cross . In fact, detailed calculations (see Prob.~\prbrintroscatt-1) show that both the forward peak and the classical cross contribute $\pi a^2$ to the total. The “extra” cross comes entirely from the forward peak.

This peak is due to diffraction. As the waves pass by the edge of the sphere they are bent in an inward direction, that is, the direction necessary to close in the shadow behind the sphere. Diffraction theory shows that if we move far enough downstream, the shadow is completely filled by diffracted waves. Of course the differential cross is defined in the limit $r\to\infty$, so there is no shadow in the differential cross . Diffraction causes the direction of the waves to change from the incident direction, and so must be counted as part of the scattering.

(sec-introscatt-17)=

## The Optical Theorem

The optical theorem is an exact relationship between the total cross $\sigma$ and the scattering amplitude $f$. In the context of potential scattering that we have considered in these notes, the optical theorem is

:::{math}
:label: eq-introscatt-75
\sigma ={4\pi\over k} \Im f(0),
:::

where $f(0)$ refers to the scattering amplitude in the forward direction.

The optical theorem is trivial to prove in the case of scattering by central force potentials. We place the $z$-axis along the direction of the beam so that the usual polar angle $\theta$ is the scattering angle. Then {eq}`eq-introscatt-43` implies

:::{math}
:label: eq-introscatt-76
{4\pi\over k}\Im f(0) = {4\pi\over k^2}\Im \sum_{\ell=0}^\infty (2\ell+1)e^{i\delta_\ell}\,\sin\delta_\ell \,P_\ell(1) = {4\pi\over k^2} \sum_{\ell=0}^\infty (2\ell+1)\sin^2\delta_\ell = \sigma,
:::

where we have used {eq}`eq-introscatt-57` and {eq}`eq-orbamsph-75`. This proof is straightforward but it gives no insight into what the theorem means.

The theorem {eq}`eq-introscatt-75` actually applies to scattering by any potential $V(\xvec)$ that dies off faster than $1/r$ as $r\to\infty$, so that the asymptotic wave function is

:::{math}
:label: eq-introscatt-77
\psi(\xvec) \sim e^{i\kvec\cdot\xvec} + {e^{ikr}\over r}\, f(\theta,\phi),
:::

as indicated by {eq}`eq-introscatt-3` and {eq}`eq-introscatt-5`. That is, we need not assume that the potential is rotationally invariant. The two terms in {eq}`eq-introscatt-77` are the incident and scattered waves, respectively.

Since the wave function $\psi(\xvec)$ is a solution of the time-independent Schr\"odinger equation, the current

:::{math}
:label: eq-introscatt-78
\Jvec=\Re\psi^\cc(\xvec)\Bigl(-{i\hbar\del\over m}\Bigr) \psi(\xvec)
:::

satisfies $\del\cdot\Jvec=0$, so by Stokes' theorem the integral of $\Jvec$ over any closed surface vanishes. See {eq}`eq-tevolut-55`--{eq}`eq-tevolut-57`. We will integrate $\Jvec$ over a large sphere of radius $r$ centered at the origin of the coordinates, which we assume is inside the region occupied by the potential as in {ref}`fig-introscatt-2`. We will take the limit $r\to\infty$, so that the asymptotic form {eq}`eq-introscatt-77` of the wave function can be used.

Thus the asymptotic form of the current is

:::{math}
:label: eq-introscatt-79
\begin{aligned}
\Jvec &\sim \Re\Bigl[e^{-i\kvec\cdot\xvec} + {e^{-ikr}\over r} \, f^\cc(\theta,\phi)\Bigr] \Bigl(-{i\hbar\del\over m}\Bigr) \Bigl[e^{i\kvec\cdot\xvec} + {e^{ikr}\over r}\, f(\theta,\phi)\Bigr] \\
&=v\Re\Bigl[e^{-ikr\cos\theta} + {e^{-ikr}\over r} \, f^\cc(\theta,\phi)\Bigr] \Bigl[{\hat{\mathbf{z}}}\, e^{ikr\cos\theta} + {\hat{\mathbf{r}}} {e^{ikr}\over r} \,f(\theta,\phi)\Bigr], \\

\end{aligned}
:::

where we have set $\kvec=k{\hat{\mathbf{z}}}$ and $v=\hbar k/m$ and retained only the leading term in the gradient of the scattered wave, as in {eq}`eq-introscatt-12`. The neglected terms will not contribute to the integral over the sphere when we take the limit $r\to\infty$.

The current is quadratic in the wave function $\psi(\xvec)$, so in addition to the incident current and scattered current there is a contribution coming from the cross terms, which represent the interference between the incident wave and the scattered wave. We write

:::{math}
:label: eq-introscatt-80
\Jvec=\Jvec_inc + \Jvec_scatt + \Jvec_x,
:::

where $\Jvec_x$ is the interference current. By Stokes' theorem we have

:::{math}
:label: eq-introscatt-81
\int_sphere \Jvec\cdot d\avec =0,
:::

where $d\avec = r^2 {\hat{\mathbf{r}}}\, d\Omega$ is the area element of the sphere.

:::{figure} images/introscatt-fig10.png
:label: fig-introscatt-10
:width: 80%

The incident current passes straight through the sphere and produces no net flux across its surface.
:::

:::{figure} images/introscatt-fig11.png
:label: fig-introscatt-11
:width: 80%

The scattered current produces a net flux of particles leaving the sphere, proportional to the total cross .
:::


The incident current is

:::{math}
:label: eq-introscatt-82
\Jvec_inc = v\Re \bigl[e^{-ikr\cos\theta}\bigr] \bigl[{\hat{\mathbf{z}}}\,e^{ikr\cos\theta}\bigr] = v\,{\hat{\mathbf{z}}},
:::

It is a constant vector whose integral over sphere vanishes,

:::{math}
:label: eq-introscatt-83
\int_sphere \Jvec_inc\cdot d\avec=0,
:::

as is obvious from {ref}`fig-introscatt-10`.

The scattered current was already computed in \secrintroscatt-6. It is

:::{math}
:label: eq-introscatt-84
\Jvec_scatt = v\Re\Bigl[{e^{-ikr}\over r}\, f^\cc(\theta,\phi)\Bigr] \Bigl[{\hat{\mathbf{r}}} \, {e^{ikr}\over r}\, f(\theta,\phi)\Bigr] = v\, {{\hat{\mathbf{r}}}\over r^2} \,|f(\theta,\phi)|^2,
:::

whose integral over the sphere is

:::{math}
:label: eq-introscatt-85
\int_sphere\Jvec\cdot d\avec = v\int_sphere |f(\theta,\phi)|^2 \,d\Omega = \sigma v,
:::

where $\sigma$ is the total cross and where we have used {eq}`eq-introscatt-15`. The scattered wave gives a net outgoing flux, proportional to the cross , which is no surprise. See {ref}`fig-introscatt-11`.

Therefore the interference current must provide a net inward flux that cancels the scattered flux. From {eq}`eq-introscatt-79` we have

:::{math}
:label: eq-introscatt-86
\Jvec_x = {v\over r} \Re \Bigl[{\hat{\mathbf{z}}} \, e^{-ikr(1-\cos\theta)}\,f^\cc(\theta,\phi) + {\hat{\mathbf{r}}}\,e^{ikr(1-\cos\theta)}\,f(\theta,\phi)\Bigr].
:::

But the real part of a complex number is the same as the real part of its complex conjugate, so we can replace the first term in {eq}`eq-introscatt-86` by its complex conjugate to obtain

:::{math}
:label: eq-introscatt-87
\Jvec_x = {v\over r} \Re\bigl[ ({\hat{\mathbf{z}}}+{\hat{\mathbf{r}}})\, e^{ikr(1-\cos\theta)} \, f(\theta,\phi)\bigl].
:::

Now the interference flux is

:::{math}
:label: eq-introscatt-88
\int_sphere \Jvec_x\cdot d\avec = vr \Re \int_0^{2\pi}d\phi \int_0^\pi \sin\theta\,d\theta\, (1+\cos\theta)\, e^{ikr(1-\cos\theta)}\,f(\theta,\phi).
:::

We wish to evaluate this integral in the limit $r\to\infty$, which is slightly delicate. The prefactor of $r$ would tend to make the integral diverge, but the factor $e^{ikr(1-\cos\theta)}$ in the integrand oscillates ever more rapidly in $\theta$ as $r$ gets larger, thereby chopping up the integrand and tending to make the integral vanish. To clarify the competition between these tendencies, we integrate by parts in $\theta$, obtaining

:::{math}
:label: eq-introscatt-89
\begin{aligned}
\int_sphere \Jvec_x\cdot d\avec &= vr \Re\int_0^{2\pi}d\phi \int_0^\pi d\theta\, {1\over ikr} \Bigl[\dod{}{\theta} e^{ikr(1-\cos\theta)}\Bigr] (1+\cos\theta)f(\theta,\phi) \\
&= {v\over k}\Re\int_0^{2\pi}d\phi\, \Bigl\{-i\Bigl. e^{ikr(1-\cos\theta)}\,(1+\cos\theta) f(\theta,\phi)\Bigr|^{\theta=\pi}_{\theta=0} \\
&\qquad +i\int_0^\pi d\theta\, e^{ikr(1-\cos\theta)} \dod{}{\theta}\bigl[(1+\cos\theta)f(\theta,\phi)\bigr] \Bigr\}. \\

\end{aligned}
:::

The integration by parts has eliminated the prefactor of $r$, so now the final integral oscillates itself to death as $r\to\infty$ and can be dropped. Evaluating the remaining term under the $\phi$-integral at the limits $\theta=0,\pi$, we see that it vanishes at $\theta=\pi$ and that at $\theta=0$ it is proportional to $f(0,\phi)$ which is what we are writing simply as $f(0)$ and which is independent of $\phi$. Thus we find

:::{math}
:label: eq-introscatt-90
\int_sphere \Jvec_x\cdot d\avec = {v\over k}\Re\int_0^{2\pi}d\phi\, 2i f(0) = -{4\pi v\over k}\Im f(0).
:::

The sum of this plus the scattered flux $\sigma v$ vanishes, which produces the optical theorem {eq}`eq-introscatt-75`.

We see that the interference flux comes in from the forward direction, where it partially cancels the incident flux going in the other direction.

The optical theorem has many generalizations. One version of it applies for the scattering of classical electromagnetic waves (vector waves, in contrast to the scalar waves considered here). Another applies to inelastic scattering in quantum mechanics, in which $\sigma$ is the total cross , including both elastic and inelastic scattering, while $f(0)$ refers only to the forward amplitude for elastic scattering. This is because only the wave for elastic scattering can interfere with the incident wave. There are many other applications in fields ranging from quantum mechanics to black hole physics.

\problems

(prob-introscatt-1)=

**Problem \prbdintroscatt-1..** 

\problempart{(a)} Work out the classical differential cross $d\sigma/d\Omega$ for a hard sphere of radius $a$, and integrate it to get the total cross $\sigma$.

\problempart{(b)} In problem {ref}`prob-pathint-1`, you worked out the far field wave function $\psi(x,y,z)$, for $z\gg ka^2$, when a plane wave $e^{ikz}$ traveling in the positive $z$-direction strikes a screen in the $x$-$y$ plane with a circular hole of radius $a$ cut out. In that problem the hole was centered on the origin. The solution was worked out for $\theta=\rho/z \ll 1$ (the paraxial approximation), where $\rho = \sqrt{x^2+y^2}$.

By subtracting this solution from the incident wave $e^{ikz}$, you get the far field wave function when a plane wave $e^{ikz}$ strikes the *complementary* screen, that is, just a disk of radius $a$ at the origin.

It turns out this wave field is the same as the wave field in hard sphere (of radius $a$) scattering in the limit $ka \gg 1$, if measured in the forward direction. That is because for forward scattering from a hard scatterer, the physics is dominated by diffraction, so it is only the projection of the scatterer onto the $x$-$y$ plane that matters.

Write the scattered wave as $(e^{ikr}/r)f(\theta)$, express $r$ as a function of $z$ and $\theta$ for small $\theta$, expand out to lowest order in $\theta$, and compare to the asymptotic wave field to get an expression for the scattering amplitude for small angles $\theta$. Use the optical theorem, {eq}`eq-introscatt-75`, to compute $\sigma$.

\problempart{(c)} Show that $d\sigma/d\Omega$ in the forward direction has a narrow peak of width $\Delta\theta \sim 1/ka \ll 1$. Write down an integral giving the contribution of this forward peak to the total cross in terms of the first root $b$ of the Bessel function $J_1$. You can approximate $\sin\theta = \theta$ in this integral, since $\theta$ is small. It turns out that the value of this integral does not change much if the upper limit is extended to infinity. Use the integral

:::{math}
:label: eq-introscatt-91
\int_0^\infty {dx \over x} \, J_1(x)^2 = {1\over 2},
:::

to find the contribution of the forward peak to the total cross . (See Gradshteyn and Ryzhik, integral number 6.538.2.)

(prob-introscatt-2)=

**Problem \prbdintroscatt-2..** 

:::{math}
:label: eq-introscatt-92
\begin{aligned}
V(r)=\begin{cases} V_0=const, & r<a, \\  0, & r>a, \\\end{cases}
\end{aligned}

:::

where $V_0$ may be positive or negative. Using the method of partial waves, show that for $|V_0|\ll E=\hbar^2k^2/2m$ and $ka\ll 1$ the differential cross is isotropic and that the total cross is given by

:::{math}
:label: eq-introscatt-93
\sigma_tot = {16\pi\over 9} {m^2 V_0^2 a^6 \over \hbar^4}.
:::

Suppose the energy is raised slightly. Show that the angular distribution can then be written as

:::{math}
:label: eq-introscatt-94
\dod{\sigma}{\Omega} = A + B\cos\theta.
:::

Obtain an approximate expression for $B/A$.

(prob-introscatt-3)=

**Problem \prbdintroscatt-3..** 

Consider the scattering of a polarized, spin~$\frac{1}{2}$ particle by a target, such as a neutron by the nucleus of an atom (we may assume that the nucleus is polarized, too). There is some amplitude for scattering that does not flip the spin, and some for scattering that does.

Suppose the incident particle is polarized spin up, so that the incident wave function can be taken to be

:::{math}
:label: eq-introscatt-95
\psi_inc = e^{i\kvec\cdot\rvec} \begin{pmatrix}1\\ 0\\\end{pmatrix}.
:::

The asymptotic form for the scattered wave is

:::{math}
:label: eq-introscatt-96
\psi_scatt \sim {e^{ikr}\over r} \begin{pmatrix}f_+(\theta,\phi) \\ f_-(\theta,\phi)\end{pmatrix},
:::

where $f_\pm$ are the scattering amplitudes with ($-$) and without ($+$) spin flip.

Find a generalization of the optical theorem in this case. Recall {eq}`eq-jjcouple-30` for the probability current for particles with spin. Is it possible that some target could cause the spin to flip with 100\% probability? How do your answers change if a magnetization term such as seen in {eq}`eq-jjcouple-33` is included in the probability current?
