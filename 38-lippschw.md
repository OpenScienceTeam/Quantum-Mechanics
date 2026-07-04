---
title: "38. The Lippmann-Schwinger Equation and Formal Scattering Theory"
---
(ch-lippschw)=

# 38. The Lippmann-Schwinger Equation and Formal Scattering Theory

(sec-lippschw-1)=

## Introduction

In earlier lectures we studied the scattering of spinless particles by central force potentials. Such problems are tractable because the Schr\"odinger equation is separable in spherical coordinates, and we were able to reduce everything we wanted to know to the properties of radial wave functions. But those are a rather restricted class of problems.

In these notes we apply Green's functions and Green's operators to scattering problems. Although we mainly treat potential scattering in three dimensions, in fact the techniques we develop have a much broader applicability. We shall see that Green's functions lead to powerful operator methods for treating scattering problems that allow us to derive both exact results and approximation methods in scattering theory. These can be generalized in a variety of ways, for example, to relativistic and field theoretic problems.

We begin by deriving the Lippmann-Schwinger equation, a formulation of the scattering problem in terms of an integral equation that is central to all further developments. An asymptotic analysis of this equation leads to an exact relation between the scattering amplitude and the properties of the wave field at small radii (where the potential is active). This is ultimately the basis of several exact results involving the scattering amplitude. The Lippmann-Schwinger equation also easily leads to a simple approximation scheme, the Born series, as well as to an intuitive and quantitative criterion for the conditions of validity of the Born approximation. Then we develop some of the properties of the exact Green's operator for the system, and show how all results of interest in scattering theory can be expressed in terms of it. Then we discuss the transition operator, in terms of which the exact scattering amplitude can be expressed, which allows a neat determination of the effects of various symmetries (parity, time reversal, etc) on the scattering amplitude. Finally we discuss the orthonormality relations satisfied by the scattering states.

This material is background on the $S$-matrix, which we will not discuss in these notes, but which is a central object of investigation in advanced treatments of scattering theory, especially in relativistic quantum mechanics.

(sec-lippschw-2)=

## The Lippmann-Schwinger Equation

We consider potential scattering of a spinless particle in three dimensions. We write the Schr\"odinger equation in the form {eq}`eq-greensfuns-12`,

:::{math}
:label: eq-lippschw-1
(E-H_0)\psi(\xvec) = V(\xvec)\psi(\xvec),
:::

where $E>0$ since we are interested in scattering solutions. The potential $V(\xvec)$ is not necessarily rotationally invariant, but we do assume it falls off sufficiently rapidly as $r\to\infty$. We will be more quantitative about this condition below. We treat the right-hand side of {eq}`eq-lippschw-1` as a driving or source term, so the general solution can be written

:::{math}
:label: eq-lippschw-2
\psi(\xvec) = \phi(\xvec) + \int d^3\xvec' \, G_0(\xvec,\xvec',E)V(\xvec')\psi(\xvec'),
:::

where $\phi(\xvec)$ is a solution of the homogeneous equation, that is, $(E-H_0)\phi(\xvec)=0$, and $G_0$ is an energy-dependent Green's function for the free-particle Hamiltonian $H_0$. (As in {ref}`ch-greensfuns`, the 0-subscript means “free particle.”) The homogeneous solution $\phi(\xvec)$ is a free-particle wave function of energy $E$. With different choices for $\phi$ and $G_0$, we get different solutions $\psi$ of {eq}`eq-lippschw-1`.

Because we are interested physically in scattered waves that are radiated outward from the scatterer, we take $G_0$ to be the outgoing free-particle Green's function, $G_{0+}$, given by {eq}`eq-greensfuns-98`. We will examine the boundary conditions on the scattered wave more carefully in a moment. As for the homogeneous solution $\phi(\xvec)$, we take it to be a plane wave with wave vector $\kvec$,

:::{math}
:label: eq-lippschw-3
\phi_\kvec(\xvec) = \braket{\xvec}{\kvec} = {e^{i\kvec\cdot\xvec} \over (2\pi)^{3/2}},
:::

and we interpret it as the incident wave. We just write $\ket{\kvec}$ for the plane wave of wave vector $\kvec$ in ket language. As discussed earlier, the scattered wave is the difference between the exact solution and the incident wave, a free particle solution. Our plane waves are normalized so that

:::{math}
:label: eq-lippschw-4
\braket{\kvec}{\kvec'} = \delta^3(\kvec-\kvec').
:::

With this choice of Green's function and incident wave, {eq}`eq-lippschw-2` becomes

:::{math}
:label: eq-lippschw-5
\psi(\xvec) = \phi_\kvec(\xvec) + \int d^3\xvec' \, G_{0+}(\xvec,\xvec',E)V(\xvec')\psi(\xvec').
:::

This is the *Lippmann-Schwinger* equation. It is not so much a solution of the original Schr\"odinger equation {eq}`eq-lippschw-1` as a reformulation of it in terms of an integral equation, since the unknown wave field $\psi(\xvec)$ occurs both on the left-hand side and under the integral on the right-hand side.

The Lippmann-Schwinger equation {eq}`eq-lippschw-5` contains both an energy eigenvalue $E$ and a wave vector $\kvec$. These are related by the

:::{math}
:label: eq-lippschw-6
free-particle expression, E={\hbar^2k^2\over 2m},
:::

in spite of the fact that $\phi_\kvec(\xvec)$ is not a solution of the exact Schr\"odinger equation (at least not where $V(\xvec)\ne 0$). This is because $\phi_\kvec(\xvec)$ is a solution of the homogeneous equation $(E-H_0)\phi_\kvec=0$, whose energy parameter is the same as the energy eigenvalue of the exact Schr\"odinger equation {eq}`eq-lippschw-1`. More physically, the experimenter is free to launch particles at the target with any value of momentum, but the energy and momentum are related by the free particle relation since the particles are free where they are launched, in the asymptotic region. Moreover, the energy of the particles in the beam is the same as the energy eigenvalue of the corresponding solution of the Schr\"odinger equation. This is plausible physically because a uniform beam of particles directed against a target produces after a while a steady state, statistically speaking, in which a definite number of particles per unit time are scattered into any given element of solid angle. It is plausible that this steady state should correspond to a solution $\psi(\xvec)$ of the Schr\"odinger equation with energy $E$, since measuring the energy of the particles in the asymptotic region produces the value $E$.

This physical picture suggests (correctly, as it turns out) that the Lippmann-Schwinger equation has a unique solution $\psi(\xvec)$ for a given wave vector $\kvec$ (which determines $E$). That is, for a given $E$, there is a unique solution satisfying the given boundary conditions (which consist of the given incident wave of wave vector $\kvec$, plus the fact that the scattered waves are purely outgoing). This is in contrast to the original Schr\"odinger equation, the differential equation {eq}`eq-lippschw-1`, which has many solutions for a given energy $E$. This is clear physically, since the experimenter is free to direct the beam against the target from any incident direction, thereby generating different states of the same energy. We will write $\psi_\kvec(\xvec)$ to emphasize the $\kvec$-dependence of the solution. With this slight change of notation, the Lippmann-Schwinger equation becomes

:::{math}
:label: eq-lippschw-7
\psi_\kvec(\xvec) = \phi_\kvec(\xvec) + \int d^3\xvec' \, G_{0+}(\xvec,\xvec',E) V(\xvec') \psi_\kvec(\xvec'),
:::

or, in ket form,

:::{math}
:label: eq-lippschw-8
\ket{\psi_\kvec} = \ket{\kvec} +{\Ghat}_{0+}(E) V\ket{\psi_\kvec},
:::

where it is understood that $E$ and $\kvec$ are related by the free-particle relation {eq}`eq-lippschw-6`. As usual, the ket form has the advantages of compactness and generality. Finally, substituting the form of the free particle outgoing Green's function {eq}`eq-greensfuns-98` into {eq}`eq-lippschw-7`, we have the explicit integral equation,

:::{math}
:label: eq-lippschw-9
\psi_\kvec(\xvec) = \phi_\kvec(\xvec) -{1\over 4\pi} {2m\over \hbar^2} \int d^3\xvec' \, {e^{ik|\xvec-\xvec'|} \over |\xvec-\xvec'|} \, V(\xvec')\psi_\kvec(\xvec').
:::

The Lippmann-Schwinger equation is a fundamental result, as important for scattering theory as the Schr\"odinger equation is for the rest of quantum mechanics. As we shall see, it opens the door to many exact results in scattering theory as well as various approximation methods.

There are obviously many variations on this derivation. For example, the incident wave need not be a plane wave. For another example, the unperturbed Hamiltonian might include part of the potential, presumably a part such that $H_0$ can be solved, while $V$ contains the rest of the potential. For example, in proton-proton scattering we might take $H_0$ to include the (long-ranged) Coulomb potential of the two protons, while $V$ would contain the short-ranged nuclear potential. In this case, $\phi$ would be a Coulomb solution of positive energy.

(sec-lippschw-3)=

## The Scattering Amplitude

The Lippmann-Schwinger equation in the form {eq}`eq-lippschw-9` represents the scattered wave as a superposition of outgoing spherical waves, radiating from each point of space $\xvec'$ where $V(\xvec')\ne 0$. The integration over $\xvec'$ in {eq}`eq-lippschw-9` represents this superposition. In general, the different spherical waves are not in phase with one another, and their interference gives rise to the angular dependence of the scattered wave.

:::{figure} images/lippschw-fig01.png
:label: fig-lippschw-1
:width: 80%

An incident plane wave with wave vector $\kvec$ is launched against a localized potential. Observation point $\xvec$ is in the asymptotic region, while $\xvec'$ is a variable of integration that runs over the region where $V(\xvec')\ne0$. Wave vector $\kvec'$ has the same magnitude as the incident wave vector $\kvec$, but points in the direction of the observation point.
:::

Let us assume for the moment that the potential rigorously vanishes outside some radius $R$, and let us consider the case in which $\xvec$ in {eq}`eq-lippschw-9` is well outside this radius, $r\gg R$. We interpret $\xvec$ as an “observation point” (see {ref}`fig-lippschw-1`). Then the variable of integration $\xvec'$ in {eq}`eq-lippschw-9` is limited by $r'<R$, and we have $r' \ll r$ over the entire range of integration. Therefore we may expand the integrand in powers of $r'/r$. We are only interested in the dominant term as $r\to\infty$, but different parts of the integrand must be expanded to different orders in $r'/r$. For example, in the exponent $e^{ik|\xvec-\xvec'|}$ we have

:::{math}
:label: eq-lippschw-10
|\xvec-\xvec'| \approx r - {\xvec\cdot\xvec'\over r} = r - {\hat{\mathbf{r}}}\cdot\xvec',
:::

where ${\hat{\mathbf{r}}}$ is a unit vector from the scatterer to the distant observation point. Now we define a scattered wave vector,

:::{math}
:label: eq-lippschw-11
\kvec' = k{\hat{\mathbf{r}}},
:::

which has the same magnitude as the incident wave vector $\kvec$ (because the scattering is elastic), and which also points from the scatterer to the observer. Then

:::{math}
:label: eq-lippschw-12
k|\xvec-\xvec'| = kr - \kvec'\cdot\xvec'.
:::

The first term $kr$ is large as $r\to\infty$, while the next term is independent of $r$. We stop at this order of the expansion, because the following term is down by a factor of $r'/r$, so it goes to zero as $r\to\infty$. As for the denominator in {eq}`eq-lippschw-9`, we expand it to lowest order,

:::{math}
:label: eq-lippschw-13
{1\over |\xvec-\xvec'|} \approx {1\over r},
:::

since the next term goes to zero faster than $1/r$ as $r\to\infty$.

Altogether, when $\xvec$ is in the asymptotic region the Lippmann-Schwinger becomes

:::{math}
:label: eq-lippschw-14
\psi_\kvec(\xvec) = \phi_\kvec(\xvec) -{1\over 4\pi} {2m\over\hbar^2} {e^{ikr}\over r} \int d^3\xvec' \, e^{-i\kvec'\cdot\xvec'} \, V(\xvec') \psi_\kvec(\xvec'),
:::

dropping correction terms that go to zero faster than $1/r$ as $r\to\infty$. The integral is now independent of the magnitude of $\xvec$, but depends on its direction through $\kvec'$. The scattered wave has the form of $e^{ikr}/r$ times a function of the scattering angle, that is, the asymptotic wave field can be written as

:::{math}
:label: eq-lippschw-15
\psi_\kvec(\xvec) = {1\over (2\pi)^{3/2}} \Bigl[ e^{i\kvec\cdot\xvec} + {e^{ikr} \over r} \, f(\kvec,\kvec') \Bigr],
:::

where $f(\kvec,\kvec')$ is the scattering amplitude. We previously argued on somewhat intuitive grounds that the asymptotic form of the wave field must have this form, and we proved that it does so in the case of central force scattering. Now we have proved it for scattering from a potential of any shape.

We assumed above that the potential rigorously vanishes outside some radius. If this is not true, it can still be shown that the asymptotic form {eq}`eq-lippschw-14` is correct, as long as the potential $V(\xvec)$ goes to zero faster than $1/r$ as $r\to\infty$. As a practical matter, this covers all potentials of interest except the Coulomb potential.

We have previously written the scattering amplitude as $f(\theta,\phi)$, referring to the spherical coordinates of some coordinate system, but now we are writing it in the coordinate-independent form $f(\kvec,\kvec')$, specifying both the incident and scattered vectors. The notation is slightly misleading, since $f$ is not an independent function of both vectors, whose magnitudes are required to be equal. By comparing {eq}`eq-lippschw-14` and {eq}`eq-lippschw-15`, we can read off an expression for the scattering amplitude,

:::{math}
:label: eq-lippschw-16
f(\kvec,\kvec') = -{(2\pi)^{3/2}\over 4\pi} {2m\over \hbar^2} \int d^3\xvec' \, e^{-i\kvec'\cdot\xvec'} V(\xvec') \psi_\kvec(\xvec')= -{4\pi^2 m\over\hbar^2} \matrixelement{\kvec'}{V}{\psi_\kvec},
:::

where we use {eq}`eq-lippschw-4`. This is an exact expression for the scattering amplitude, a property of the wave field in the asymptotic region, in terms of an integral involving the wave field in the region where the potential is nonzero. Thus it provides a connection between the region at large radii and the region at small radii. {eq}`eq-lippschw-16` cannot be used immediately to calculate the scattering amplitude unless we know the values of the exact solution $\psi_\kvec(\xvec)$ at small radii, but it is important for deriving general relations concerning the scattering amplitude as well as for developing approximation methods.

(sec-lippschw-4)=

## The Incoming Solutions

What would have happened if we had used the incoming Green's function $G_{0-}$ in the integral equation {eq}`eq-lippschw-2`? The solution $\psi$ would still be unique for given wave vector $\kvec$ of the wave $\phi_\kvec$, but it would not be the same solution we have been discussing. Instead, it would consist of waves streaming inward from infinity toward the scatterer, which would combine with plane wave $\phi_\kvec$ to form an exact solution of the Schr\"odinger equation with energy $E$. These solutions would obviously be impossible to set up experimentally, but they are perfectly good solutions of the Schr\"odinger equation from a mathematical standpoint, and, as it turns out, they are also useful in scattering theory. When it is necessary to distinguish the two types of solutions, we will write them $\psi_\kvec^{(\pm)}(\xvec)$, where the sign indicates the type of Green's function used ($+ = \\textoutgoing$, $-=\\textincoming$). If we omit the sign, the outgoing solution will be assumed. These two types of solutions satisfy the Lippmann-Schwinger equations,

:::{math}
:label: eq-lippschw-17
\psi_\kvec^{(\pm)}(\xvec) = \phi_\kvec(\xvec) + \int d^3\xvec' \, G_{0\pm}(\xvec,\xvec',E) V(\xvec') \psi_\kvec^{(\pm)}(\xvec'),
:::

or, in ket language,

:::{math}
:label: eq-lippschw-18
\ket{\psi_\kvec^{(\pm)}} = \ket{\kvec} + \Ghat_{0\pm}(E)V\ket{\psi_\kvec^{(\pm)}}.
:::

(sec-lippschw-5)=

## An Integral Equation for Bound States

It is also possible to formulate an integral equation for the bound states. When $E<0$, there can be no homogeneous solution as in {eq}`eq-lippschw-2`, because no free particle solution $\phi$ for $E<0$ has the right behavior at infinity. Therefore there is only the inhomogeneous term. Furthermore, both Green's functions $G_{0\pm}$ are equal for $E<0$, as shown in {eq}`eq-greensfuns-98`, and indeed, there is only one Green's function with the right behavior at infinity. Thus we obtain the following integral equation for the bound states:

:::{math}
:label: eq-lippschw-19
\psi(\xvec) = -{1\over 4\pi}{2m\over\hbar^2} \int d^3\xvec' \, {e^{-\kappa|\xvec-\xvec'|} \over |\xvec-\xvec'|} \, V(\xvec') \psi(\xvec'),
:::

which can be satisfied only for discrete values of $E=-\hbar^2\kappa^2/2m$.

(sec-lippschw-6)=

## The Born Series

Let us write the Lippmann-Schwinger equation {eq}`eq-lippschw-8` in the form

:::{math}
:label: eq-lippschw-20
\ket{\kvec} = [1-G_{0+}(E)V] \ket{\psi_\kvec},
:::

which makes it clear that if we could invert the operator on the right-hand side, we could solve explicitly for the solution $\ket{\psi_\kvec}$. (We henceforth drop the hat on the Green's operator, it being fairly clear when an operator is being referred to and when a function.) We denote the required inverse by

:::{math}
:label: eq-lippschw-21
\Omega_+(E) = [1-G_{0+}(E)V]^{-1},
:::

where $\Omega_+(E)$ is called the *M\o ller scattering operator*. It is an operator that (for the given energy $E$) maps the incident plane wave $\ket{\kvec}$ into the associated, exact scattering solution $\ket{\psi_\kvec}$,

:::{math}
:label: eq-lippschw-22
\ket{\psi_\kvec} = \Omega_+(E) \ket{\kvec}.
:::

Similarly, we define an incoming version of this operator,

:::{math}
:label: eq-lippschw-23
\Omega_-(E) = [1-G_{0-}(E)V]^{-1},
:::

which is useful for finding incoming solutions,

:::{math}
:label: eq-lippschw-24
\ket{\psi^{(-)}_\kvec} = \Omega_-(E) \ket{\kvec}.
:::

More generally, we can define an operator $\Omega(z)$, depending on a complexified energy,

:::{math}
:label: eq-lippschw-25
\Omega(z) = [1-G_{0}(z)V]^{-1},
:::

so that

:::{math}
:label: eq-lippschw-26
\Omega_\pm(E) = \lim_{\epsilon\to0} \Omega(E\pm i\epsilon).
:::

(This is not quite standard notation. Most references on scattering theory define a M\o ller wave operator, call it ${\tilde \Omega}_\pm$, that is independent of energy. The two operators have the same effect when acting on plane waves, however: ${\tilde \Omega_\pm} \ket{\kvec} = \Omega_\pm(E)\ket{\kvec}$, where $E$ is related to $\kvec$ by the free particle relation.)

A simple approach to obtaining a useful expression for $\Omega(z)$ is to treat $V$ as small and expand the inverse operator in a power series. This gives

:::{math}
:label: eq-lippschw-27
\Omega(z) = {1\over 1-G_0(z)V} = 1 + G_0(z)V + G_0(z)VG_0(z)V + \ldots,
:::

or, by {eq}`eq-lippschw-26`,

:::{math}
:label: eq-lippschw-28
\Omega_\pm(E) = 1 + G_{0\pm}(E)V + G_{0\pm}(E)VG_{0\pm}(E)V + \ldots.
:::

When this series is applied to the Lippmann-Schwinger equation in the form {eq}`eq-lippschw-20`, it gives

:::{math}
:label: eq-lippschw-29
\ket{\psi_\kvec} = \ket{\kvec} + G_{0+}(E)V\ket{\kvec} + G_{0+}(E)VG_{0+}(E)V \ket{\kvec} + \ldots.
:::

This is called the *Born series* for the scattering solution $\ket{\psi_\kvec}$. When it is truncated at $n$-th order in the potential $V$, we speak of the $n$-th *Born approximation*. Similarly, the expansion {eq}`eq-lippschw-28` can be substituted into the expression {eq}`eq-lippschw-16` for the scattering amplitude, yielding

:::{math}
:label: eq-lippschw-30
f(\kvec,\kvec') = -{4\pi^2 m \over \hbar^2} \Bigl[ \matrixelement{\kvec'}{V}{\kvec} + \matrixelement{\kvec'}{V G_{0+}(E)V}{\kvec} + \matrixelement{\kvec'}{V G_{0+}(E)V G_{0+}(E)V}{\kvec} + \ldots\Bigr],
:::

which is the Born series for the scattering amplitude. Again, if we truncate at $n$-th order, we obtain the $n$-th Born approximation to the scattering amplitude.

The Born series can also be obtained by a method of successive approximations. If we take the Lippmann-Schwinger equation in the form {eq}`eq-lippschw-8` and substitute the left-hand side into the right-hand side, we obtain

:::{math}
:label: eq-lippschw-31
\ket{\psi_\kvec} = \ket{\kvec} + G_{0+}(E)V \ket{\kvec} + G_{0+}(E)V G_{0+}(E)V \ket{\psi_\kvec},
:::

an exact equation in which the unknown wave function $\ket{\psi_\kvec}$ has been pushed into a second order term in $V$. By substituting {eq}`eq-lippschw-8` into {eq}`eq-lippschw-31` again, the term containing $\ket{\psi_\kvec}$ can be pushed to third order, etc. This procedure also generates the terms of the Born series, but with an explicit remainder term.

We shall examine the conditions of validity of the Born approximation in a moment, but for now we just remark that the series does not necessarily converge, and the Born expansion is only useful in some problems. Obviously it will work best when $V$ is small in some sense.

The first Born approximation to the scattering amplitude is

:::{math}
:label: eq-lippschw-32
f(\kvec,\kvec') = -{4\pi^2 m \over \hbar^2} \matrixelement{\kvec'}{V}{\kvec} = -{\sqrt{2\pi} \, m\over\hbar^2}\, {\tilde V}(\kvec'-\kvec),
:::

where $\tilde V$ is the Fourier transform of the potential $V$ using the convention {eq}`eq-tdpt-78`, and where $\kvec'-\kvec$ (times $\hbar$) is the momentum transfer in the scattering. On taking the square of the scattering amplitude, we obtain the cross in the first Born approximation,

:::{math}
:label: eq-lippschw-33
\dod{\sigma}{\Omega} = {2\pi m^2 \over \hbar^4} |{\tilde V}(\kvec'-\kvec)|^2,
:::

which agrees with our earlier result {eq}`eq-tdpt-80` from time-dependent perturbation theory. Although the scattering amplitude in the first Born approximation only depends on the difference between the incident and scattered momenta, this is not true in higher Born approximations, as one may easily see.

The first Born approximation gives the same result as first-order, time-dependent perturbation theory because there is a close relationship between the Dyson series (in the time domain) and the Born series (in the energy domain). Both are straightforward power series expansions in powers of the potential $V$. The Born series, however, makes it easier to analyze the conditions of validity of the approximation, a subject to which we now turn.

(sec-lippschw-7)=

## Conditions of Validity of the Born Approximation

Let us write the Lippmann-Schwinger equation and the first Born approximation for the scattering solution $\ket{\psi_\kvec}$ side-by-side to compare them:

:::{math}
:label: eq-lippschw-34
\begin{aligned}
\ket{\psi_\kvec} &= \ket{\kvec} + G_{0+}(E)V\ket{\psi_\kvec}, \\
\ket{\psi_\kvec} &\approx \ket{\kvec} + G_{0+}(E)V\ket{\kvec}. \\

\end{aligned}
:::

This shows that the scattered wave as computed by the first Born approximation is a good approximation to the exact scattered wave, everywhere in space, if the exact solution is approximately given by the incident wave at small radii where the potential is substantially nonzero. This leads to the intuitive conditions of validity of the first Born approximation: the approximation is good if the potential does not distort the incident plane wave too much in the neighborhood of the potential itself. This in turn shows that the Born approximation is good if the potential is weak or if the incident energy is high (since in that case the incident particles blast through the potential without being deflected very much).

To be more quantitative, we follow Gottfried, *Quantum Mechanics* and introduce the dimensionless quantity,

:::{math}
:label: eq-lippschw-35
C = {\phi_\kvec(\xvec) - \psi_\kvec(\xvec) \over \phi_\kvec(\xvec)},
:::

which we want to be small in the region where $V(\xvec)$ is largest. The quantity $C$ depends on $\xvec$, but we evaluate it at $\xvec=0$, for a (hopefully) typical point inside the scatterer. Then $C$ depends only on $\kvec$. Using the Lippmann-Schwinger equation and evaluating the integral transform at $\xvec=0$, we get

:::{math}
:label: eq-lippschw-36
C={m\over 2\pi\hbar^2} \int d^3\xvec'\, {e^{ikr'} \over r'} V(\xvec') \psi_\kvec(\xvec') \times (2\pi)^{3/2}.
:::

Since this is only an estimate, we replace $\psi_\kvec(\xvec)$ with $\phi_\kvec(\xvec)$,

:::{math}
:label: eq-lippschw-37
C = {m\over 2\pi\hbar^2} \int d^3\xvec \, {e^{ikr} \over r} V(\xvec) e^{i\kvec\cdot\xvec},
:::

dropping the primes on the dummy variable of integration. If $V(\xvec) = V(r)$ is central force, then we can do the angular integration, obtaining

:::{math}
:label: eq-lippschw-38
C={2m\over \hbar^2 k} \int_0^\infty dr\, e^{ikr} \, \sin kr V(r).
:::

The quantity $C$ should satisfy $|C| \ll 1$ if the Born approximation is a good one. Our argument leading to this criterion is not air-tight, but the criterion is useful nonetheless.

Consider, for example, the Yukawa potential,

:::{math}
:label: eq-lippschw-39
V(r) = A {e^{-r/a} \over r},
:::

where in comparison to {eq}`eq-tdpt-116` we have set $\kappa=1/a$ so that $a$ is the effective range of the potential. Then the integral {eq}`eq-lippschw-38` can be done, yielding

:::{math}
:label: eq-lippschw-40
C = {imAa \over \hbar^2} {\ln(1-2ika) \over ka}.
:::

This has the limits,

:::{math}
:label: eq-lippschw-41
\begin{aligned}
C = {mAa\over\hbar^2} \times \begin{cases} 2, & ka \ll 1, \\  i\ds{\ds\ln ka \over \ds ka}, & ka \gg 1.\end{cases}
\end{aligned}

:::

Small $ka$ means that the incident wave length is much larger than the range of the potential; recall that in this case we have predominantly $s$-wave scattering. In this case, the validity of the Born approximation is equivalent to the requirement that the Yukawa potential (if attractive) should be so weak that it does not support any bound states. Large $ka$ means that the wavelength is small compared to the range of the potential. Notice that $|C| \to \infty$ in the limit $a\to\infty$, which takes the Yukawa potential to the Coulomb potential. The conditions of validity of the Born approximation are not met for any $k$ for Coulomb scattering, as remarked earlier (see {ref}`sec-tdpt-20`).

(sec-lippschw-8)=

## The Exact Green's Function

So far in our applications of Green's functions to scattering theory we have only used the unperturbed Green's function, $G_{0\pm}$. But it turns out that many of the interesting quantities in scattering theory can be expressed in terms of the exact Green's function or operator for the system. Let us recall the definitions of the resolvent operators,

:::{math}
:label: eq-lippschw-42
G_0(z) = {1\over z-H_0}, \qquad G(z) = {1 \over z-H},
:::

which are well defined as long as $z$ is not equal to any eigenvalue of the corresponding Hamiltonian (either discrete or continuous). The Green's operators for real energy $E$ are defined by setting $z=E\pm i\epsilon$ and taking $\epsilon\to0$, when that limit exists (which it does as long as $E$ is not equal to any discrete, bound state eigenvalue). It was remarked in {ref}`ch-greensfuns`\ that the exact resolvent $G(z)$ contains all the physical information we might be interested in about the given system, including the scattering solutions and amplitudes. We will now show how this comes about.

There are a number of useful relations connecting the exact resolvent and the unperturbed one that follow by just playing around with the definitions {eq}`eq-lippschw-42`. For example, for any $z$ not on the real axis, where the inverses of $z-H_0$ and $z-H$ are defined and unique, we have

:::{math}
:label: eq-lippschw-43
z-H_0 = z-H+V = \begin{cases} \ds \Bigl(1+V{\ds 1 \over \ds z-H}\Bigr)(z-H) =[1+VG(z)](z-H), \\  \ds (z-H)\Bigl(1+{\ds 1 \over \ds z-H}V\Bigr) =(z-H)[1+G(z)V], \\\end{cases}
:::

where the two versions differ by factoring $z-H$ out to the right or to the left. Now multiplying the first identity from the right and the second from the left by $G(z)$, we obtain

:::{math}
:label: eq-lippschw-44a
\begin{aligned}
(z-H_0)G(z) &= 1+VG(z),
\end{aligned}
:::

:::{math}
:label: eq-lippschw-44b
\begin{aligned}
G(z)(z-H_0) &= 1+G(z)V.
\end{aligned}
:::

Finally, we multiply the first equation from the left and the second from the right by $G_0(z)$, to obtain

:::{math}
:label: eq-lippschw-45a
\begin{aligned}
G(z) &= G_0(z) + G_0(z)VG(z),
\end{aligned}
:::

:::{math}
\begin{aligned}
G(z) &= G_0(z) + G(z)VG_0(z). & {eq}`eq-lippschw-45a`
\end{aligned}
:::

These are two identities connecting the exact and unperturbed resolvents in which only the order of the factors in the last term is different.

Equations~{eq}`eq-lippschw-45a` can be regarded as Lippmann-Schwinger equations for the exact Green's function. To see this, we first set $z=E+i\epsilon$ and take $\epsilon \to 0$ to get the outgoing Green's operators. Next we sandwich both equations between $\bra{\xvec}$ and $\ket{\xvec'}$ to convert them into the language of Green's functions instead of operators. Finally, we consider the unknown, exact Green's function $G_+$ as being analogous to the unknown, exact wave function $\psi_\kvec(\xvec)$ in the Lippmann-Schwinger equation, while the (known) unperturbed Green's function $G_{0+}$ is taken to be analogous to the incident plane wave $\phi_\kvec$. For example, this procedure applied to {eq}`eq-lippschw-45a` gives

:::{math}
:label: eq-lippschw-46
G_+(\xvec,\xvec',E) = G_{0+}(\xvec,\xvec',E) + \int d^3\xvec'' \, G_{0+}(\xvec,\xvec'',E) V(\xvec'') G_+(\xvec'',\xvec',E),
:::

which should be compared to {eq}`eq-lippschw-7`. In this case the effective Lippmann-Schwinger equation defines the dependence of $G_+(\xvec,\xvec',E)$ on the field point $\xvec$. The analogous procedure applied to {eq}`eq-lippschw-45a` gives a Lippmann-Schwinger equation that defines the dependence of $G_+(\xvec,\xvec',E)$ on the source point $\xvec'$.

Now we rearrange {eq}`eq-lippschw-45a` as we did with {eq}`eq-lippschw-30`,

:::{math}
:label: eq-lippschw-47
[1-G_0(z)V] G(z) = G_0(z),
:::

which shows that

:::{math}
:label: eq-lippschw-48
G(z) = \Omega(z) G_0(z),
:::

where $\Omega(z)$ is the M\o ller wave operator defined by {eq}`eq-lippschw-27`. We see that knowledge of $\Omega(z)$ not only allows us to convert the incident plane wave $\phi_k$ into the exact scattering solution $\psi_\kvec$ (see {eq}`eq-lippschw-22`, but it also allows us to convert the unperturbed resolvent into the exact resolvent. {eq}`eq-lippschw-48` also makes it easy to expand the exact resolvent in a Born series, expressed in terms of the unperturbed resolvent,

:::{math}
:label: eq-lippschw-49
G(z) = G_0(z) + G_0(z)VG_0(z) + G_0(z)VG_0(z)VG_0(z) +\ldots.
:::

Another interesting relation follows by solving {eq}`eq-lippschw-48` for $\Omega(z)$ and then using {eq}`eq-lippschw-44b`,

:::{math}
:label: eq-lippschw-50
\Omega(z) = G(z)(z-H_0) = 1+G(z)V.
:::

In other words, from the definition {eq}`eq-lippschw-25` of $\Omega(z)$, we have

:::{math}
:label: eq-lippschw-51
[1-G_0(z)V][1+G(z)V] = 1.
:::

We see that the inverse of $1-G_0(z)V$, needed to solve the Lippmann-Schwinger equation, can be expressed in terms of the exact resolvent. Thus the exact scattering solution can be written,

:::{math}
:label: eq-lippschw-52
\ket{\psi_\kvec} = [1+G_+(E)V]\ket{\kvec},
:::

again showing how knowledge of the exact Green's function allows us to determine exact scattering solutions.

(sec-lippschw-9)=

## The Transition Operator

Let us return to {eq}`eq-lippschw-16` for the scattering amplitude $f(\kvec,\kvec')$ and substitute {eq}`eq-lippschw-52` into it. We write the result as

:::{math}
:label: eq-lippschw-53
f(\kvec,\kvec') = -{4\pi^2 m\over \hbar^2} \matrixelement{\kvec'}{T(E)}{\kvec},
:::

where $T(E)$, the *transition operator*, is defined by

:::{math}
:label: eq-lippschw-54
T(E) = V + VG_+(E)V.
:::

{eq}`eq-lippschw-53` is a somewhat more symmetrical representation of the scattering amplitude than {eq}`eq-lippschw-16`, because we have plane wave states on both sides of the matrix element. The transition operator incorporates all the complexities of the scattering process, and {eq}`eq-lippschw-53` is exact. Notice that if $T(E)$ is replaced by the potential $V$, we obtain the first Born approximation to the scattering amplitude. The transition operator is not Hermitian, but rather satisfies

:::{math}
:label: eq-lippschw-55
T(E)^\hc = V + V G_-(E)V,
:::

where we use the fact that

:::{math}
:label: eq-lippschw-56
[G_+(E)]^\hc = \Bigl[\lim_{\epsilon\to0} {1\over E+i\epsilon-H}\Bigr]^\hc = \Bigl[\lim_{\epsilon\to0} {1\over E-i\epsilon-H}\Bigr] =G_-(E).
:::

The transition operator, or $T$-operator for short, is useful for exploring the effects of symmetry on the scattering amplitude. This is an important question experimentally, when the fundamental symmetries that are obeyed or broken by some interaction are under investigation.

:::{figure} images/lippschw-fig02.png
:label: fig-lippschw-2
:width: 80%

Effects of various symmetries on the scattering amplitude: (a), parity; (b), time-reversal; (c), parity and time-reversal.
:::

We begin with parity $\pi$ (see {ref}`ch-parity`). The action of parity on plane wave states is given by $\pi\ket{\kvec}=\ket{-\kvec}$. Suppose that the Hamiltonian commutes with parity, so that $[\pi,H]=0$ and $[\pi,V]=0$. Then $\pi$ commutes with any function of $H$, so that

:::{math}
:label: eq-lippschw-57
[\pi,G(z)] = \Bigl[ \pi,{1\over z-H} \Bigr] =0.
:::

From this and {eq}`eq-lippschw-54` it follows that $[\pi,T(E)]=0$. Then we have

:::{math}
:label: eq-lippschw-58
\matrixelement{\kvec'}{T(E)}{\kvec} = \matrixelement{\kvec'}{\pi^\hc\pi T(E) \pi^\hc\pi}{\kvec}= \matrixelement{-\kvec'}{T(E)}{-\kvec},
:::

or,

:::{math}
:label: eq-lippschw-59
f(\kvec',\kvec) = f(-\kvec',-\kvec).
:::

This is illustrated as case (a) in {ref}`fig-lippschw-2`.

Next let us consider time-reversal (see {ref}`ch-timerev`). The action of time-reversal on the (spinless) plane wave states is given by $\Theta\ket{\kvec} = \ket{-\kvec}$, since the wave function $e^{i\kvec\cdot\xvec}$ is transformed into its complex conjugate $e^{-i\kvec\cdot\xvec}$ [see {eq}`eq-timerev-49`]. Suppose that $\Theta$ commutes with the Hamiltonian $H$, and therefore with $V$, $[\Theta,H]=[\Theta,V]=0$. This does not mean that $\Theta$ commutes with $G_+(E)$, for we have

:::{math}
:label: eq-lippschw-60
\Theta G_{0+}(E) \Theta^\hc = \Theta \Bigl( \lim_{\epsilon\to0} {1\over E+i\epsilon-H}\Bigr) \Theta^\hc= \lim_{\epsilon\to0} {1\over E-i\epsilon-H} = G_{0-}(E),
:::

since the antiunitary $\Theta$ turns $E+i\epsilon$ into $E-i\epsilon$. (More pictorially, we can say that reversing the direction of time turns the outgoing Green's operator into the incoming Green's operator.) Now {eq}`eq-lippschw-54`, {eq}`eq-lippschw-55`, and {eq}`eq-lippschw-60` imply

:::{math}
:label: eq-lippschw-61
\Theta T(E) \Theta^\hc = T(E)^\hc.
:::

Now let us examine the effect of time-reversal invariance on the matrix elements of the $T$-operator. We have

:::{math}
\begin{aligned}
\matrixelement{\kvec'}{T(E)}{\kvec} &= \bra{\kvec'}\bigl( \Theta^\hc \Theta T(E) \Theta^\hc \Theta \ket{\kvec} \bigr) = \bra{\kvec'} \bigl( \Theta^\hc T(E)^\hc \ket{-\kvec} \bigr)
\end{aligned}
:::

:::{math}
:label: eq-lippschw-62
\begin{aligned}
&= [\matrixelement{-\kvec'}{T(E)^\hc}{-\kvec}]^\cc = \matrixelement{-\kvec}{T(E)}{-\kvec'},
\end{aligned}
:::

where the parentheses are used to indicate that the time-reversal operators act to the right, and where in the third equality we have reversed the direction in which $\Theta^\hc$ is acting, and used {eq}`eq-timerev-26`. Thus, time reversal invariance implies that the scattering amplitude satisfies

:::{math}
:label: eq-lippschw-63
f(\kvec,\kvec') = f(-\kvec',-\kvec).
:::

This property is called *microreversibility*, and it is illustrated in case (b) in Fig.~lippschw-1.

Finally, if both parity and time-reversal are symmetries of the Hamiltonian, then we have

:::{math}
:label: eq-lippschw-64
f(\kvec,\kvec') = f(\kvec',\kvec).
:::

This property is called *detailed balance*, and it is illustrated in case (c) in Fig.~lippschw-1.

(sec-lippschw-10)=

## Orthonormality of the Scattering Solutions

We shall now derive the orthonormality relations for the exact scattering states $\ket{\psi_\kvec}$. These relations are not easy to derive directly from the Schr\"odinger equation or from the integral equation {eq}`eq-lippschw-7`, but they can be easily obtained with the help of our various identities involving Green's operators. We begin by using {eq}`eq-lippschw-52` to transform the scalar product of two exact scattering states,

:::{math}
:label: eq-lippschw-65
\braket{\psi_{\kvec'}}{\psi_\kvec} = \braket{\psi_{\kvec'}}{\kvec} + \matrixelement{\psi_{\kvec'}}{G_+(E)V}{\kvec},
:::

where $E=\hbar^2k^2/2m$. The second term of this equation can be written,

:::{math}
:label: eq-lippschw-66
\matrixelement{\psi_{\kvec'}}{G_+(E)V}{\kvec} = \lim_{\epsilon\to0} \bra{\psi_{\kvec'}} {1\over E+i\epsilon-H} V \ket{\kvec} = \lim_{\epsilon\to0} {1\over E+i\epsilon-E'} \matrixelement{\psi_{\kvec'}}{V}{\kvec},
:::

where we have allowed $H$ to act to the left on $\bra{\psi_\kvec'}$, which brings out the eigenvalue $E' = \hbar^2k'^2/2m$. As for the first term on the right in {eq}`eq-lippschw-65`, we first write down the Hermitian conjugate of the Lippmann-Schwinger equation {eq}`eq-lippschw-8`, with $E$ and $\kvec$ replaced by $E'$ and $\kvec'$,

:::{math}
:label: eq-lippschw-67
\bra{\psi_{\kvec'}} = \bra{\kvec'} + \bra{\psi_{\kvec'}}VG_{0-}(E'),
:::

where we have used {eq}`eq-lippschw-56`. Then we have

:::{math}
\begin{aligned}
\braket{\psi_{\kvec'}}{\kvec} &= \braket{\kvec'}{\kvec} + \matrixelement{\psi_{\kvec'}}{VG_{0-}(E')}{\kvec} = \delta^3(\kvec-\kvec') + \lim_{\epsilon\to0} \bra{\psi_{\kvec'}} V{1\over E'-i\epsilon-H_0} \ket{\kvec}
\end{aligned}
:::

:::{math}
:label: eq-lippschw-68
\begin{aligned}
&= \delta^3(\kvec-\kvec')+ \lim_{\epsilon\to0} {1\over E'-i\epsilon-E} \matrixelement{\psi_{\kvec'}}{V}{\kvec},
\end{aligned}
:::

where we have allowed $H_0$ to act to the right on $\ket{\kvec}$, which brings out the eigenvalue $E=\hbar^2k^2/2m$. Now combining {eq}`eq-lippschw-66` and {eq}`eq-lippschw-68`, we obtain

:::{math}
:label: eq-lippschw-69
\braket{\psi_{\kvec'}}{\psi_\kvec} = \delta^3(\kvec-\kvec'),
:::

a simple result.

Although the exact scattering states $\ket{\psi_\kvec}$ are orthonormal, they are not complete in general, because of bound states. All bound states of the Hamiltonian $H$ are orthogonal to all scattering states,

:::{math}
:label: eq-lippschw-70
\braket{n\alpha}{\psi_\kvec} =0,
:::

because they are eigenfunctions of the Hamiltonian $H$ with different (positive and negative) energies.

The completeness relation relation is

:::{math}
:label: eq-lippschw-71
\sum_{n\alpha} \ketbra{n\alpha}{n\alpha} + \int d^3\kvec \, \ketbra{\psi_\kvec}{\psi_\kvec} = 1.
:::

This can be proved by a contour integration that inverts the definition of the Green's operators. We will not go into details here.

\problems

(prob-lippschw-1)=

**Problem \prbdlippschw-1.} This problem is a variation on Sakurai, *Modern Quantum Mechanics.** 

\problempart{(a)* Find the free-particle Green's function in one dimension,

:::{math}
:label: eq-lippschw-72
G_{0+}(x,x';E) = \lim_{\epsilon\to0} \matrixelement{x}{{1\over E+i\epsilon-H_0}}{x'},
:::

where

:::{math}
:label: eq-lippschw-73
H_0 = {p^2\over 2m}.
:::

Do this for both $E>0$ and $E<0$, as in the 3-dimensional case discussed in {ref}`ch-greensfuns`. Also find $G_{0-}(x,x';E)$. Show explicitly that they satisfy

:::{math}
:label: eq-lippschw-74
\Bigl(E+{\hbar^2\over 2m} {d^2\over dx^2} \Bigr) G_{0\pm}(x,x';E) = \delta(x-x').
:::

You may find it useful to note that

:::{math}
:label: eq-lippschw-75
\dod{|x|}{x} = 2\Theta(x)-1,
:::

and

:::{math}
:label: eq-lippschw-76
\dod{\Theta(x)}{x} = \delta(x).
:::

The Heaviside step function $\Theta(x)$ is defined by {eq}`eq-greensfuns-20`.

\problempart{(b)} Write down a 1-dimensional version of the Lippmann-Schwinger equation for an exact scattering solution $\psi(x)$ associated with an incoming (from the left) free particle state $\phi(x)=e^{ikx}/\sqrt{2\pi}$. The exact solution $\psi(x)$ satisfies the Schr\"odinger equation in a potential $V(x)$, which you can consider to be localized. Consider asymptotic forms (large $|x|$) and find expressions for the transmission and reflection amplitudes $t$ and $r$ which are analogous to {eq}`eq-lippschw-32` in three dimensions. These amplitudes are defined by

:::{math}
\begin{aligned}
\psi(x) &= {1\over \sqrt{2\pi}} [e^{ikx} + re^{-ikx}], \qquad \\text{x\to-\infty},
\end{aligned}
:::

:::{math}
:label: eq-lippschw-77
\begin{aligned}
\psi(x) &= {1\over \sqrt{2\pi}} t e^{ikx}, \qquad \\text{x\to+\infty}.
\end{aligned}
:::

\problempart{(c)} Consider the potential,

:::{math}
:label: eq-lippschw-78
V(x) = \lambda \delta(x).
:::

This potential can be seen as the limit of a rectangular barrier (for $\lambda>0$) with width $a$ and height $V_0 = \lambda/a$ as $a\to 0$. The attractive case $\lambda<0$ is similar.

Solve the Lippmann-Schwinger equation directly, and write out explicit forms for the wave function $\psi(x)$ for $x<0$ and $x>0$. To help the reader, please use the abbreviation,

:::{math}
:label: eq-lippschw-79
D={m\lambda\over \hbar^2 k},
:::

as much as possible. Note that $D$ is dimensionless. Compute $t$ and $r$ in terms of $D$ and show explicitly that $|t|^2 + |r|^2 =1$.

\problempart{(d)} The operator equation,

:::{math}
:label: eq-lippschw-80
G_+(E)= G_{0+}(E)+ G_{0+}(E)VG_+(E),
:::

was proved in lecture. It is a kind of Lippmann-Schwinger equation for the exact Green's function. Write this out as an integral equation for the exact Green's function, assume the potential is given by {eq}`eq-lippschw-78`, and solve for $G_+(x,x';E)$. Consider the case $\lambda<0$. Show that this Green's function has one pole on the negative energy axis, located at the energy of the one (and only) bound state. Show that the residue of this pole is the projection operator onto the eigenspace of this bound state.

(prob-lippschw-2)=

**Problem \prbdlippschw-2.} This is Sakurai, *Modern Quantum Mechanics.** 

:::{math*
:label: eq-lippschw-81
\sigma \approx {m^2\over \pi\hbar^4} \int d^3\xvec \, d^3\xvec' \, V(r) V(r') {\sin^2 k|\xvec-\xvec'| \over k^2 (\xvec-\xvec')^2},
:::

in each of the following ways:

\problempart{(a)} By integrating the differential cross computed using the first Born approximation.

\problempart{(b)} By applying the optical theorem to the forward scattering amplitude in the *second* Born approximation. Note that $f(0)$ is real if the first Born approximation is used.

(prob-lippschw-3)=

**Problem \prbdlippschw-3..** 

:::{math}
:label: eq-lippschw-82
\dod{\sigma}{\Omega} = |F(\alpha)|^2 \dod{\sigma_0}{\Omega},
:::

where $d\sigma_0/d\Omega$ is the differential cross for scattering by a single scatterer, where $\alpha$ is the angle between $\avec$ and $\kvec'$. Find the form factor $F(\alpha)$.
