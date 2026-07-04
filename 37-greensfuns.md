---
title: "37. Green's Functions in Quantum Mechanics"
---
(ch-greensfuns)=

# 37. Green's Functions in Quantum Mechanics

(sec-greensfuns-1)=

## Introduction

Green's functions and the closely associated Green's operators are central to any reasonably sophisticated and comprehensive treatment of scattering and decay processes in quantum mechanics. In these notes we shall develop the theory of Green's functions and operators, which will be applied to simple scattering problems in the next set of notes. Later, in {ref}`ch-nlw`, we will see that Green's operators provide the key to understanding the long-time behavior of quantum systems, such as an atom undergoing radiative decay. Green's operators are also necessary for the construction of the $S$-matrix, a central object in the most satisfactory treatments of scattering theory, especially in relativistic quantum mechanics.

The Green's functions and operators that we will deal with come in two varieties, the time-dependent and the energy-dependent (or time-independent). Time-dependent Green's functions are closely related to the propagator that we studied in {ref}`ch-pathint`. They are useful for solving time-dependent problems, such as the types we treated earlier by time-dependent perturbation theory.

We begin these notes by presenting a sketch of the problem of scattering of electromagnetic waves, which provides a motivation for the use of Green's functions in scattering theory in general. Next we discuss time-dependent Green's functions in quantum mechanics, which are a stepping stone into the theory of energy-dependent Green's functions. We present water wave analogies for both time-dependent and energy-dependent Green's functions in quantum mechanics, which not only provide useful physical pictures but also make some of the mathematics comprehensible. Finally, we work out the special case of the Green's function for a free particle. Green's functions are actually applied to scattering theory in the next set of notes.

(sec-greensfuns-2)=

## Scattering of Electromagnetic Waves

In the following presentation of scattering of electromagnetic waves we shall use only the most schematic notation, suppressing indices $\mu$, $\nu$, etc as well as $4\pi$'s, $\epsilon_0$'s, etc. The point is to convey the general structure of the equations and the physical picture associated with them without going into details.

We write Maxwell's equations for the vector potential $A$ (really the 4-vector $A^\mu$) in the form

:::{math}
:label: eq-greensfuns-1
\dAlembertian A = J,
:::

where $J$ is the 4-current (really $J^\mu$) and where $\dAlembertian$ is the d'Alembertian operator,

:::{math}
:label: eq-greensfuns-2
\dAlembertian = {1\over c^2}{\partial^2 \over \partial t^2} - \del^2.
:::

{eq}`eq-greensfuns-1` holds in Lorenz gauge ($\partial_\mu A^\mu=0$). Mathematically, {eq}`eq-greensfuns-1` is an *inhomogeneous equation*, that is, it has source or driving terms (the current) on the right-hand side.

The corresponding *homogeneous equation* is

:::{math}
:label: eq-greensfuns-3
\dAlembertian A_h=0,
:::

with no source term. We put an $h$-subscript on the solution of the homogeneous equation; physically, $A_h$ represents a source-free electromagnetic field, for example, a vacuum, plane light wave. Notice that if we have two solutions of the inhomogeneous {eq}`eq-greensfuns-1`,

:::{math}
:label: eq-greensfuns-4
\dAlembertian A_1=J, \qquad \dAlembertian A_2=J,
:::

then their difference is a solution of the homogeneous equation,

:::{math}
:label: eq-greensfuns-5
\dAlembertian (A_1-A_2)=0.
:::

A common problem in electromagnetic theory is to compute the field $A$ produced by a given source current $J$. The standard method for solving such problems uses Green's functions. The general solution of the inhomogeneous equation {eq}`eq-greensfuns-1` is

:::{math}
:label: eq-greensfuns-6
A(x) = A_h(x) + \int dx' \, G(x,x') J(x'),
:::

again in a very schematic notation in which $x$ means $(\xvec,t)$, and where $G(x,x')$ is a Green's function for the operator $\dAlembertian$. An arbitrary solution $A_h$ is added to the right-hand side, to give the general solution for $A$. The solution of an inhomogeneous equation is never unique, because one can always add an arbitrary homogeneous solution to it. Physically, a unique solution is selected out by boundary conditions (which allow one to choose the correct $A_h(x)$).

The Green's function satisfies

:::{math}
:label: eq-greensfuns-7
\dAlembertian G(x,x') = \delta^4(x-x'),
:::

where $\dAlembertian$ acts only on the $x$ dependence of $G$. This is itself an inhomogeneous equation, so $G(x,x')$ is not unique, either. Usually different Green's functions are characterized by the boundary conditions they satisfy.

All of this is for a given $J$, but in practice we may not know ahead of time what $J$ is. Consider, for example, the scattering of electromagnetic waves by a metal object. When the incident wave strikes the metal, its electric field causes currents $J$ to flow in the metal, and these radiate the scattered wave. More precisely, the electrons in the metal respond *both* to the incident field and the scattered field, that is, the current elements act on one another as well as responding to the incident field. Thus we have

:::{math}
:label: eq-greensfuns-8
J = \sigma A,
:::

where $\sigma$ is the conductivity operator and $A$ is the *total* field, the incident plus the scattered. (You are probably familiar with the above equation in the form $\Jvec=\sigma \Evec$, where $\sigma$ is often taken as a constant. But $\Evec$ is related to the derivatives of $A$, and in {eq}`eq-greensfuns-8` we have absorbed those derivatives into the definition of $\sigma$. Also, $\sigma$ is in general not constant, but an operator. {eq}`eq-greensfuns-8` is a general statement of the relation between the current and the fields that drive it in a linear medium.) Although $J$ responds to the total field, incident plus scattered, it is the *source* of the scattered wave only.

With the substitution {eq}`eq-greensfuns-8`, the original equation {eq}`eq-greensfuns-1` becomes

:::{math}
:label: eq-greensfuns-9
\dAlembertian A = \sigma A,
:::

or,

:::{math}
:label: eq-greensfuns-10
(\dAlembertian - \sigma)A=0.
:::

The original, inhomogeneous wave equation has become homogeneous. We see that whether an equation is homogeneous or inhomogeneous depends partly on our point of view. We also see that finding the scattered wave is a self-consistent problem of finding sources produced by the incident plus scattered wave that themselves produce the scattered wave.

:::{figure} images/greensfuns-fig01.png
:label: fig-greensfuns-1
:width: 80%

Reflection of light from a mirror. In one point of view we have an incident and a reflected wave, satisfying certain boundary conditions at the surface of the mirror. In another point of view, we have the incident wave plus the scattered wave radiated by currents in the metal.
:::

As a simple example, consider the reflection of light from a mirror. The usual point of view in textbooks is to regard this as a boundary value problem, in which one forms linear combinations of vacuum light waves to the left of the mirror (the incident plus reflected wave, see {ref}`fig-greensfuns-1`), whose sum satisfies certain boundary conditions at the surface of the mirror. There is no field to the right of the mirror because the wave cannot penetrate it. In another point of view, however, the total field is the incident field which is a vacuum plane wave everywhere in space, including to the right of the mirror, plus the scattered field which is the field produced by the currents in the mirror. These currents radiate in both directions, and they do so in such a manner that the scattered wave to the right exactly cancels the incident wave in that region. It is this latter point of view that will dominate our treatment of scattering theory from here on out.

(sec-greensfuns-3)=

## Sources and Scattered Waves in Quantum Mechanics

The physical picture of currents and sources afforded by electromagnetic scattering can be carried over to quantum mechanics. To be specific, consider potential scattering of a spinless particle in three dimensions, where the Schr\"odinger equation we wish to solve is

:::{math}
:label: eq-greensfuns-11
(H_0+V)\psi(\xvec) = E\psi(\xvec).
:::

Here $H_0=p^2/2m$ and $E>0$ is the positive energy of some scattering solution. We rearrange this equation in the form,

:::{math}
:label: eq-greensfuns-12
(E-H_0)\psi(\xvec) = V\psi(\xvec).
:::

This should be compared to the electromagnetic equation,

:::{math}
:label: eq-greensfuns-13
\Box A = J = \sigma A.
:::

In both cases we have a free particle or free wave operator on the left-hand side, $\dAlembertian$ in the electromagnetic case and $E-H_0$ in the quantum case. On the right-hand side we have a term proportional to the field, $\sigma A$ in the electromagnetic case and $V\psi$ in the quantum case. We see that the potential $V$ plays the same role as the conductivity in the electromagnetic case. The wave function $\psi(\xvec)$ can be seen as the sum of an incident plus a scattered wave, in which the scattered wave is produced by “sources” whose “strength” at any point $\xvec$ is $V(\xvec)\psi(\xvec)$.

To solve {eq}`eq-greensfuns-12` we require a Green's function for the operator $E-H_0$, which is an example of an energy-dependent Green's function. Before discussing energy-dependent Green's functions, however, we must first discuss time-dependent Green's functions.

(sec-greensfuns-4)=

## Time-Dependent Green's Functions in Quantum Mechanics

Let us consider the inhomogeneous time-dependent Schr\"odinger equation,

:::{math}
:label: eq-greensfuns-14
\Bigl[ i\hbar\pop{}{t} - H(t)\Bigr] \psi(\xvec,t) = S(\xvec,t),
:::

where $H(t)$ is some Hamiltonian and $S(\xvec,t)$ is a “source” term. We allow the Hamiltonian to depend on time because sometimes it does and in any case it leads to the most symmetrical treatment of the problem. Later we will specialize to the case of time-independent Hamiltonians. To solve this equation we require a time-dependent Green's function $F$, that is, a function that satisfies the equation

:::{math}
:label: eq-greensfuns-15
\Bigl[ i\hbar\pop{}{t} - H(t)\Bigr] F(\xvec,t;\xvec',t') = i\hbar \,\delta(t-t') \, \delta^3(\xvec-\xvec').
:::

Any function $F(\xvec,t;\xvec',t')$ that satisfies this differential equation will be considered a Green's function for the operator $i\hbar \partial/\partial t - H(t)$. The Green's function $F$ depends on a pair of space-time points. We will think of the first of these, $(\xvec,t)$, as the “field” point, and the second, $(\xvec',t')$, as the “source” point. But be careful, because some books (for example, Jackson's) reverse these interpretations, sometimes randomly. The Hamiltonian operator $H$ only acts on the field variables, for example, if it is a kinetic-plus-potential operator,

:::{math}
:label: eq-greensfuns-16
H(t) = -{\hbar^2\over 2m}\del^2 + V(\xvec,t),
:::

then $\del$ acts on the $\xvec$-dependence of $F$. The $i\hbar$ on the right-hand side of {eq}`eq-greensfuns-15` is conventional. The rest of the right-hand side is obviously a four-dimensional space-time $\delta$-function of the type we saw in {eq}`eq-greensfuns-7`.

If we can find such a Green's function $F$, then the general solution of the inhomogeneous equation {eq}`eq-greensfuns-14` can be written,

:::{math}
:label: eq-greensfuns-17
\psi(\xvec,t) = \psi_h(\xvec,t) + {1\over i\hbar} \int_{-\infty}^{\infty} dt' \int d^3\xvec' \, F(\xvec,t;\xvec',t') \, S(\xvec',t'),
:::

where $\psi_h$ is an arbitrary solution of the homogeneous equation,

:::{math}
:label: eq-greensfuns-18
\Bigl[ i\hbar\pop{}{t} - H(t)\Bigr]\psi_h(\xvec,t) =0.
:::

That is, $\psi_h(\xvec,t)$ is a solution of the ordinary (homogeneous) Schr\"odinger equation with Hamiltonian $H(t)$ (without driving terms). Since there are many such solutions, the solution {eq}`eq-greensfuns-17` of the inhomogeneous equation is not unique.

We see that if we can solve the inhomogeneous equation with a $\delta$-function driving term, that is, {eq}`eq-greensfuns-15` for the Green's function $F$, then we can solve the inhomogeneous equation {eq}`eq-greensfuns-14` with an arbitrary driving term. In effect, we break up the driving term into a sum of $\delta$-function contributions, and then add the wave fields (the Green's function $F$) corresponding to each of these. The result is the integral in the second term in {eq}`eq-greensfuns-17`.

(sec-greensfuns-5)=

## The Outgoing Time-Dependent Green's Function

There are many time-dependent Green's functions, but the most important one for our purposes is the *outgoing* (or *retarded*) Green's function, defined by

:::{math}
:label: eq-greensfuns-19
K_+(\xvec,t;\xvec',t') = \Theta(t-t')\, \matrixelement{\xvec}{U(t,t')}{\xvec'}.
:::

Here $\Theta$ is the Heaviside step function,

:::{math}
:label: eq-greensfuns-20
\begin{aligned}
\Theta(\tau) = \begin{cases}0, &\tau <0, \\ 1,  &\tau >0, \\\end{cases}
\end{aligned}

:::

which has the property,

:::{math}
:label: eq-greensfuns-21
\dod{\Theta(\tau)}{\tau} = \delta(\tau).
:::

Also, $U(t,t')$ in {eq}`eq-greensfuns-19` is the time-evolution operator (see {ref}`sec-tevolut-2`), which depends on both the final time $t$ and the initial time $t'$ since the Hamiltonian $H(t)$ is time-dependent. The properties of $U(t,t')$ that we need are the Schr\"odinger equation,

:::{math}
:label: eq-greensfuns-22
i\hbar \frac{\partial U(t,t')}{\partial t} = \Hhat(t) U(t,t'),
:::

and the initial conditions,

:::{math}
:label: eq-greensfuns-23
U(t',t') = 1
:::

(see Secs. {ref}`sec-tevolut-2` and {ref}`sec-tevolut-4`). The hat on $\Hhat$ in {eq}`eq-greensfuns-22` will be explained momentarily.

To show that $K_+(\xvec,t;\xvec',t')$ actually is a Green's function, we differentiate both sides of {eq}`eq-greensfuns-19`, obtaining,

:::{math}
:label: eq-greensfuns-24
i\hbar\frac{\partial K_+(\xvec,t;\xvec',t')}{\partial t} = i\hbar \,\delta(t-t')\, \matrixelement{\xvec}{U(t,t')}{\xvec'} + \Theta(t-t') \, \matrixelement{\xvec}{\Hhat(t)U(t,t')}{\xvec'},
:::

where we have used {eq}`eq-greensfuns-22` in the second term. As for the first term on the right-hand side, the $\delta$-function vanishes if $t \ne t'$, so we might as well set $t=t'$ inside $U(t,t')$, since the answer vanishes otherwise. But then we can use the initial conditions {eq}`eq-greensfuns-23`, so the first term becomes

:::{math}
:label: eq-greensfuns-25
i\hbar \,\delta(t-t')\, \braket{\xvec}{\xvec'} = i\hbar \,\delta(t-t')\, \delta^3(\xvec-\xvec').
:::

As for the second term, we must first explain that we are using the notation $H(t)$ to stand for the Hamiltonian operator acting on wave functions $\psi(\xvec,t)$, while writing $\Hhat(t)$ to stand for the corresponding operator acting on kets. The relation between them is

:::{math}
:label: eq-greensfuns-26
H(t)\psi(\xvec,t) = H(t) \,\braket{\xvec}{\psi(t)} = \matrixelement{\xvec}{\Hhat(t)}{\psi(t)}.
:::

Thus the second term on the right-hand side of {eq}`eq-greensfuns-24` can be written,

:::{math}
:label: eq-greensfuns-27
\Theta(t-t') \,H(t) \, \matrixelement{\xvec}{U(t,t')}{\xvec'} = H(t) \, K_+(\xvec,t;\xvec',t').
:::

Rearranging the result, we have

:::{math}
:label: eq-greensfuns-28
\Bigl[i\hbar \pop{}{t} -H(t)\Bigr] K_+(\xvec,t;\xvec',t') = i\hbar\, \delta(t-t') \, \delta^3(\xvec-\xvec').
:::

This proves that $K_+(\xvec,t;\xvec',t')$ is indeed a Green's function for {eq}`eq-greensfuns-14`.

In {ref}`ch-pathint`\ we used the notation

:::{math}
:label: eq-greensfuns-29
K(\xvec,t;\xvec',t') = \matrixelement{\xvec}{U(t,t')}{\xvec'},
:::

(without the $+$ subscript) and we called the function $K$ the “propagator.” The outgoing Green's function $K_+$, related to $K$ by

:::{math}
:label: eq-greensfuns-30
K_+(\xvec,t;\xvec',t') = \Theta(t-t')\, K(\xvec,t;\xvec',t'),
:::

is also called the “propagator,” or, to be more precise, the “outgoing” or “retarded” propagator. The two functions are closely related, but $K$ (without the $\Theta$-function) is not a Green's function.

The properties of $K_+$ that will be important to us are the following. First, $K_+(\xvec,t;\xvec',t')$ vanishes for $t<t'$, on account of the step function. Second, $K_+(\xvec,t;\xvec',t')$ is a solution of the time-dependent Schr\"odinger equation in the field variables $(\xvec,t)$ for $t>t'$, since the function $\delta(t-t')$ on the right-hand side of {eq}`eq-greensfuns-28` vanishes for $t>t'$. It also (trivially) satisfies the Schr\"odinger equation for $t<t'$, since $K_+=0$ in that case. Third, if we let $t$ approach $t'$ from the positive side, then $K_+$ approaches $\delta^3(\xvec-\xvec')$. This follows from the definition {eq}`eq-greensfuns-19`, since $\Theta(t-t') = 1$ on the positive side, and $U(t,t') \to 1$ (the identity operator) in the limit. That is,

:::{math}
:label: eq-greensfuns-31
\lim_{t \to t'_+} K_+(\xvec,t;\xvec',t') = \delta^3(\xvec-\xvec').
:::

Thus, $K_+(\xvec,t;\xvec',t')$ for $t>t'$ can be thought of as the solution $\psi(\xvec,t)$ of the time-dependent Schr\"odinger equation with the singular initial conditions $\psi(\xvec,t')=\delta^3(\xvec-\xvec')$ at $t=t'$.

These properties allow us to visualize the outgoing Green's function $K_+$ in a water wave analogy. We imagine a lake that has been quiet from $t=-\infty$ until $t=t'$, whereupon we go to position $\xvec'$ in the lake and disturb it in a spatially and temporally localized manner (for example, we poke our finger into the lake just once, or throw a stone into the lake). Then the wave field that radiates outward from the disturbance is the outgoing time-dependent Green's function, that is, $K_+(\xvec,t;\xvec',t')$ is the value of the field at position $\xvec$ at time $t$, that was produced by the disturbance at point $\xvec'$ at time $t'$. The waves for $t>t'$ are freely propagating (they are not driven).

For another example, an earthquake or an underground explosion is a disturbance that is localized in space and time, and the waves that radiate outward are the outgoing Green's function for sound waves in the earth.

If we use the outgoing time-dependent Green's function $K_+(\xvec,t;\xvec',t')$ to solve the driven Schr\"odinger equation {eq}`eq-greensfuns-14`, then the solution is

:::{math}
:label: eq-greensfuns-32
\psi(\xvec,t) = \psi_h(\xvec,t) + {1\over i\hbar}\int_{-\infty}^\infty dt' \int d^3\xvec' \, K_+(\xvec,t;\xvec',t')\, S(\xvec',t').
:::

However, the $\Theta(t-t')$ factor that appears in the definition of $K_+$ means that the integrand vanishes for times $t'>t$, so the upper limit of the $t'$ integration in the integral {eq}`eq-greensfuns-32` can be replaced by $t$. Also, let us impose the requirement of *causality*, that is, the field $\psi(\xvec,t)$ is caused by the source $S(\xvec,t)$. This means that if $S(\xvec,t)=0$ for times $t<t_0$, then we must have $\psi(\xvec,t)=0$ for $t<t_0$. So setting $t$ in {eq}`eq-greensfuns-32` to some time $t<t_0$, the left hand side vanishes, as does the integral, because the variable of integration $t'$ must satisfy $t'<t<t_0$, so $S(\xvec,t')=0$. Therefore the homogeneous solution $\psi_h(\xvec,t)$ must also vanish for $t<t_0$. But this means that $\psi_h(\xvec,t)=0$ for all $t$, since the solution of the homogeneous equation is determined by its initial conditions, which in this case are zero. Altogether, the causal solution we obtain using the outgoing Green's function is

:::{math}
:label: eq-greensfuns-33
\psi(\xvec,t) = {1\over i\hbar} \int_{-\infty}^t dt' \int d^3\xvec' \, K(\xvec,t,\xvec',t')\, S(\xvec',t'),
:::

where we have dropped the $+$ subscript on $K$ (see {eq}`eq-greensfuns-29`, since it is not necessary any more.

This is the causal solution of the inhomogeneous wave equation. It is also possible to construct solutions that do not obey the principle of causality (the wave is nonzero before the source acts). These solutions are nonphysical, but useful in scattering theory nonetheless.

(sec-greensfuns-6)=

## The Incoming Time-Dependent Green's Function

There is another time-dependent Green's function of importance, the *incoming* or *advanced* Green's function, defined by

:::{math}
:label: eq-greensfuns-34
K_-(\xvec,t;\xvec',t') = -\Theta(t'-t)\, \matrixelement{\xvec}{U(t,t')}{\xvec'}.
:::

In comparison to the definition {eq}`eq-greensfuns-19` of $K_+$, the argument in the step function is reversed, so $K_-(\xvec,t;\xvec',t')$ vanishes for times $t>t'$. It will be left as an exercise to show that $K_-$ actually is a Green's function, that is, that it satisfies {eq}`eq-greensfuns-15`.

The incoming Green's function $K_-$ satisfies the Schr\"odinger equation in the variables $(\xvec,t)$ both for $t<t'$ and $t>t'$, trivially in the latter case since $K_-=0$ for those times. It also has the limiting form as $t$ approaches $t'$ from below,

:::{math}
:label: eq-greensfuns-35
\lim_{t \to t'_-} K_-(\xvec,t;\xvec',t') = -\delta^3(\xvec-\xvec').
:::

Thus, in the water wave analogy, $K_-$ consists of waves that have existed on the lake from time $t=-\infty$ up to $t=t'$. As $t$ approaches $t'$ from below, these waves converge on location $\xvec'$, assembling to produce a $\delta$-function precisely at $\xvec'$ as $t=t'$. At that instant, our finger comes up and absorbs all the energy in the wave, leaving a quiet lake for all times afterward ($t>t'$).

Obviously the incoming Green's function would be impossible to set up experimentally, while the outgoing Green's function is easy. This is why the outgoing Green's function is the primary one used in scattering theory, where the waves travel outward from the scatterer. Nevertheless, the incoming Green's function is also important in scattering theory, as we will see.

(sec-greensfuns-7)=

## Green's Operators

We associate the Green's functions $K_\pm(\xvec,t;\xvec',t')$ with Green's *operators* $\Khat_\pm(t,t')$ by

:::{math}
:label: eq-greensfuns-36
K_\pm(\xvec,t;\xvec',t') = \matrixelement{\xvec}{\Khat_\pm(t,t')}{\xvec'}
:::

The Green's functions are just the position space matrix elements of the Green's operators, that is, the functions are the kernels of the integral transforms in position space that are needed to carry out the effect of the operators on wave functions. We will write Green's operators with a hat and Green's functions without one. The definitions {eq}`eq-greensfuns-19` and {eq}`eq-greensfuns-34` of the Green's functions $K_\pm$ are equivalent to the operator definitions,

:::{math}
:label: eq-greensfuns-37
\Khat_\pm(t,t') = \pm\Theta\bigl(\pm(t-t')\bigr) U(t,t').
:::

These satisfy an operator version of {eq}`eq-greensfuns-15`,

:::{math}
:label: eq-greensfuns-38
\Bigl[i\hbar\pop{}{t} - \Hhat(t)\Bigr] \Khat_\pm(t,t') = i\hbar \, \delta(t-t'),
:::

where the right-hand side is understood to be a multiple of the identity operator. When we sandwich both sides of this between $\bra{\xvec}$ and $\ket{\xvec'}$, the spatial $\delta$-function appears on the right-hand side, as seen in {eq}`eq-greensfuns-15`.

The operator notation is not only more compact than the wave function notation, it is also more general, since we do not have to be specific about the form of the Hamiltonian or the nature of the Hilbert space upon which it acts. For example, it applies to particles with spin, multiparticle systems, composite particles with internal structure, relativistic problems, and field theoretic problems of various types.

(sec-greensfuns-8)=

## Time-Independent Hamiltonians

In the special case that $\Hhat$ is independent of time, the time-evolution operator $U(t,t')$ depends only on the elapsed time $t-t'$ (see {ref}`sec-tevolut-4`). In this case we will write $U(t)$ for the time evolution operator, where $t$ is now the elapsed time, and of course we have $U(t) = \exp(-i\Hhat t/\hbar)$. Then with a slight change of notation we define the operators

:::{math}
:label: eq-greensfuns-39
\Khat_\pm(t) = \pm \Theta(\pm t) U(t),
:::

which satisfy

:::{math}
:label: eq-greensfuns-40
\Bigl( i\hbar\pop{}{t} - \Hhat\Bigr) \Khat_\pm(t) = i\hbar \, \delta(t).
:::

We will write

:::{math}
:label: eq-greensfuns-41
K_\pm(\xvec,\xvec',t) = \matrixelement{\xvec}{\Khat_\pm(t)}{\xvec'}
:::

for the Green's functions in the case of time-independent Hamiltonians.

As a special case, for the free particle in three dimensions, $H=H_0 = p^2/2m$, the Green's functions are

:::{math}
:label: eq-greensfuns-42
K_{0\pm}(\xvec,\xvec',t) = \pm \Theta(\pm t) \Bigl( {m \over 2\pi i\hbar t}\Bigr)^{3/2} \exp\Bigl[ {i\over \hbar} {m (\xvec-\xvec')^2 \over 2t} \Bigr],
:::

where the $0$-subscript refers to “free particle.” See {eq}`eq-pathint-11`.

(sec-greensfuns-9)=

## Energy-Dependent Green's Functions in Quantum Mechanics

Let us now consider the inhomogeneous time-independent Schr\"odinger equation,

:::{math}
:label: eq-greensfuns-43
(E-H)\psi(\xvec)= S(\xvec),
:::

where $H$ is a time-independent Hamiltonian and $S(\xvec)$ is a source term. As above, $H$ stands for the differential operator acting on wave functions $\psi(\xvec)$, for example,

:::{math}
:label: eq-greensfuns-44
H = -{\hbar^2\over 2m}\del^2 + V(\xvec),
:::

and $\Hhat$ stands for the Hamiltonian operator acting on kets. To solve {eq}`eq-greensfuns-43` we require a Green's function for the operator $E-H$, that is, a function $G(\xvec,\xvec',E)$ that satisfies

:::{math}
:label: eq-greensfuns-45
(E-H)G(\xvec,\xvec',E) = \delta^3(\xvec-\xvec'),
:::

where $H$ acts only on the $\xvec$-dependence of $G$ (the “field” point), while $\xvec'$ (the “source” point) and $E$ are considered parameters. The Green's function depends on $E$ because the operator $E-H$ depends on $E$; we shall call it an *energy-dependent* Green's function. We will use the symbol $G$ for energy-dependent Green's functions, and $K$ for time-dependent Green's functions. The energy $E$ is not necessarily an eigenvalue of the Hamiltonian $H$, rather it should be thought of as a parameter that we adjust depending on the application. In fact, as we shall see shortly, it sometimes even takes on complex values.

Green's functions are not unique, but if we find one, we can write the general solution of {eq}`eq-greensfuns-43` as

:::{math}
:label: eq-greensfuns-46
\psi(\xvec) = \psi_h(\xvec) + \int d^3\xvec \, G(\xvec,\xvec',E)\, S(\xvec'),
:::

where $\psi_h(\xvec)$ is a solution of the homogeneous equation, $(E-H)\psi_h(\xvec)=0$. That is, $\psi_h(\xvec)$ is an eigenfunction of $H$ of energy $E$ (and if $E$ is not an eigenvalue of $H$, then $\psi_h=0$).

We can express an energy-dependent Green's function in terms of an associated operator by writing

:::{math}
:label: eq-greensfuns-47
G(\xvec,\xvec',E) = \matrixelement{\xvec}{\Ghat(E)}{\xvec'}.
:::

Then the defining equation {eq}`eq-greensfuns-45` of an energy-dependent Green's function can be written in operator form as

:::{math}
:label: eq-greensfuns-48
(E-\Hhat)\Ghat(E) = 1.
:::

This would seem to have the solution,

:::{math}
:label: eq-greensfuns-49
\Ghat(E) = (E-\Hhat)^{-1},
:::

but, as we shall see, the operator $E-\Hhat$ either has no inverse, or has a unique inverse, or has many inverses, depending on the value of $E$. In a finite-dimensional vector space, an operator (that is a matrix) has an inverse if and only if its determinant is nonzero, and if it has one, it is unique. In infinite dimensional spaces this is no longer true. As we shall see, the multiple inverses that exist for $E-\Hhat$ are related to boundary conditions.

The mathematics of energy-dependent Green's functions is tricky because of various noncommuting limits, which are related to the fact that the Schr\"odinger equation has no damping. In the following we make no pretense of mathematical rigor, but we will attempt to provide physical models and images that help visualize the functions being considered and that make their mathematical properties plausible. To start this process, we now make digression into the subject of frequency-dependent Green's functions for water waves, the analog of energy-dependent Green's functions in quantum mechanics. This will provide us with concrete physical images and analogies to help us understand the mathematics we will encounter later with quantum mechanical Green's functions.

(sec-greensfuns-10)=

## A Water Wave Analogy

The analogy between water waves and Schr\"odinger waves is imperfect because water waves obey nonlinear differential equations that are second order in time, while the Schr\"odinger equation is linear and first order in time. (Small amplitude water waves are governed by a linear equation, however.) We shall gloss over such differences, concentrating instead on the physical picture afforded by the analogy.

Imagine a lake of finite area that has been quiet from $t=-\infty$ until $t=0$, whereupon we go to position $\xvec'$ (the source point) in the lake, and create a spatially localized disturbance that is periodic with frequency $\omega$ (for example, we poke our finger up and down in the water). We do this for all positive time from $t=0$ to $t=\infty$. As you can imagine, waves are radiated from the initial disturbance, they travel to the shores and reflect and come back, creating a complicated wave pattern that nevertheless simplifies after a while because of the decay of the initial transients. The decay depends on the damping present in the water waves; we assume the damping is small, and represented by a parameter $\epsilon$. After the decay of the initial transients, a steady wave pattern is established, that is, a fixed wave field oscillating everywhere with the same frequency $\omega$ as the driver. Obviously we can set the driving frequency to any value we wish; this frequency is analogous to the energy parameter $E$ of the energy-dependent, inhomogeneous Schr\"odinger equation {eq}`eq-greensfuns-45`, which as we have mentioned can also be regarded as an adjustable parameter (the quantum frequency is $\omega=E/\hbar$).

The wave pattern established on the lake after the decay of the transients is the Green's function $G(\xvec,\xvec',\omega)$, after the oscillatory time-dependence at frequency $\omega$ has been stripped off, where $\xvec$ is the observation point (the field point), and $\xvec'$ and $\omega$ the parameters (the source point and frequency). We consider this wave field in three different cases.

In case~(a), the frequency $\omega$ is not near any of the eigenfrequencies $\omega_n$ of the lake, that is, the driving is off-resonance. In that case, the wave field is approximately in phase with the driving term, and while some energy is delivered to the waves in each cycle by the driver, an almost equal amount is removed (assuming the damping is small). The small difference is a net amount of energy delivered to the waves and lost by dissipation. If we take the limit $\epsilon\to0$ (not possible in real water waves but useful to imagine when comparing to the Schr\"odinger equation) the wave pattern does not change much, but the energies gained and lost on each cycle approach one another since there is no longer any energy lost to dissipation.

Notice that as $\epsilon \to 0$, we must wait longer and longer for the initial transients to die out; effectively, we are first taking the limit $t\to\infty$ (so the transients die out), then $\epsilon\to 0$. If we carried out the limits in the other order, first setting $\epsilon=0$, then driving the lake and waiting a long time, the transients would never die out and would be with us all the way to $t=\infty$. Thus, the two limits do not commute.

In case~(b), the frequency is near to one of the eigenfrequencies of the lake, $\omega \approx \omega_n$, that is, the driving is on-resonance. In this case the wave and the driver are nearly $90^\circ$ out of phase, the amplitude of the waves is large, and the wave field (the Green's function $G(\xvec,\xvec',\omega))$ is nearly equal to the eigenfunction of the lake at the frequency $\omega_n$. The driver mostly delivers energy to the waves on each cycle, removing comparatively little. The net energy delivered is lost in dissipation, in fact it is only the dissipation that limits the amplitude of the waves, which goes to infinity as $\epsilon\to0$. The Green's function does not exist (it diverges) as $\epsilon\to0$ when $\omega=\omega_n$.

This is what happens when $\omega$ is equal to one of the discrete eigenfrequencies of the wave system. What about the continuous eigenfrequencies? Let us call this case (c). A finite lake only has discrete frequencies of oscillation, so let us imagine opening up the lake to make an ocean that extends to infinity. Again we drive the wave field at source point $\xvec'$ at frequency $\omega$ (which necessarily belongs to the continuous spectrum, since the infinite ocean supports oscillations at all frequencies) and wait for transients to die out. The steady-state wave field radiates out from the source and decays exponentially with distance as it extends out into the ocean, due to the damping. If we now take the limit that the damping goes to zero, the spatial extent of the wave pattern grows longer and longer, in the limit producing a wave field carrying energy all the way out to infinity. In the limit $\epsilon\to0$ the wave field decays with distance only as a power law (for example, it is proportional to $1/\sqrt{r}$ in two dimensions), which reflects the ever larger regions into which the energy radiated by the source propagates. Now the energy delivered to the water by the source just radiates out to infinity. The wave pattern is not an eigenfunction of the infinite ocean.

(sec-greensfuns-11)=

## Motivation For Energy-Dependent Green's Function

Based on the water wave analogy, we consider driving the Schr\"odinger {eq}`eq-greensfuns-14` with a source that is localized in space, that is turned on at $t=0$, and that is periodic in time with frequency $\omega=E/\hbar$. Notice that $E$ indicates the driving frequency, which is arbitrary. That is, we take the source to be

:::{math}
:label: eq-greensfuns-50
S(\xvec,t)=\Theta(t)\,\delta(\xvec-\xvec_0)\,e^{-iEt/\hbar},
:::

so that $\xvec_0$ is the location of the source. We also assume that the Hamiltonian is time-independent, so that

:::{math}
:label: eq-greensfuns-51
K(\xvec,t;\xvec',t')=K(\xvec,\xvec',t-t')= \matrixelement{\xvec}{U(t-t')}{\xvec'},
:::

where $t-t'$ is the elapsed time. Then the causal solution {eq}`eq-greensfuns-33` is

:::{math}
:label: eq-greensfuns-52
\psi(\xvec,t)={1\over i\hbar} \int_{-\infty}^t dt' \int d^3\xvec' \, K(\xvec,\xvec',t-t')\Theta(t')\delta(\xvec'-\xvec_0) \,e^{-iEt'/\hbar}.
:::

This vanishes if $t<0$, while for $t>0$ it becomes

:::{math}
:label: eq-greensfuns-53
\psi(\xvec,t)={1\over i\hbar} \int_0^t dt'\, K(\xvec,\xvec_0,t-t')\, e^{-iEt'/\hbar} ={e^{-iEt/\hbar}\over i\hbar} \int_0^t d\tau\, e^{iE\tau/\hbar}\,K(\xvec,\xvec_0,\tau),
:::

where we have substituted $\tau=t-t'$ in the final step.

If we strip off the time dependence $e^{-iEt/\hbar}$, then, based on what we have said about the water wave analogy, what is left should approach the Green's function $G(\xvec,\xvec_0,E)$ as $t\to\infty$, that is, we should have

:::{math}
:label: eq-greensfuns-54
G(\xvec,\xvec',E)={1\over i\hbar} \int_0^\infty dt\, e^{iEt/\hbar}\,K(\xvec,\xvec',t),
:::

with a slight change of notation. Since $G(\xvec,\xvec',E) =\matrixelement{\xvec}{\Ghat(E)}{\xvec'}$ and $K(\xvec,\xvec',t) =\matrixelement{\xvec}{U(t)}{\xvec'}$, this implies

:::{math}
:label: eq-greensfuns-55
\Ghat(E)={1\over i\hbar}\int_0^\infty dt\, e^{iEt/\hbar}\,U(t),
:::

or

:::{math}
:label: eq-greensfuns-56
\Ghat(E)={1\over i\hbar}\int_{-\infty}^{\infty} dt\, e^{iEt/\hbar}\,\Khat_+(t),
:::

since $\Khat_+(t)=\Theta(t)U(t)$.

This would mean that $\Ghat(E)$ is the one-sided Fourier transform of $U(t)$ in time, with $E$ being the energy-like conjugate variable, or the full (two-sided) Fourier transform of the outgoing time-dependent Green's operator, $\Khat_+(t)$. This is the right idea, but we must modify it slightly, as we now explain.

(sec-greensfuns-12)=

## The Outgoing Energy-Dependent Green's Operator

Since the energy-dependent Green's operator {eq}`eq-greensfuns-55` or {eq}`eq-greensfuns-56` is basically the Fourier transform of the outgoing time-dependent Green's operator, we shall call it the outgoing energy-dependent Green's operator and henceforth denote it by $\Ghat_+(E)$. We will write $G_+(\xvec,\xvec',E)$ for the corresponding, outgoing energy-dependent Green's function. We obtain an expression for the operator by setting $U(t)=e^{-i\Hhat t/\hbar}$ in {eq}`eq-greensfuns-55` and doing the integral,

:::{math}
:label: eq-greensfuns-57
\Ghat_+(E) = {1\over i\hbar} \int_0^\infty dt\, e^{iEt/\hbar} \, U(t) = {1\over i\hbar} \int_0^\infty dt \, e^{i(E-\Hhat)t/\hbar} = \left. -{e^{i(E-\Hhat)t/\hbar} \over E-\Hhat} \right|_0^\infty.
:::

In carrying out this integration we are treating $\Hhat$ as if it were an ordinary number; the justification is contained in the definition of a function of an operator, which is discussed in {ref}`sec-hilbert-25`. In the present case, we are dealing with functions of the Hamiltonian $\Hhat$. The antiderivative in the final expression, evaluated at the lower limit $t=0$, just gives the operator $1/(E-\Hhat)$, but at the upper limit it is not meaningful since $e^{i(E-\Hhat)t/\hbar}$ does not approach a definite limit as $t\to\infty$. We are talking about the limit of an operator, but if we let this operator act on an energy eigenstate $\ket{n}$ it brings out a phase factor $e^{i(E-E_n)t/\hbar}$ that oscillates indefinitely as $t\to\infty$ without approaching any limit. It is in this sense that we say that the operator $e^{i(E-\Hhat)t/\hbar}$ does not approach a definite limit as $t\to\infty$. Thus the original Fourier transform in {eq}`eq-greensfuns-56` is not defined.

The problematic oscillatory terms are effectively transients that never die out at $t\to\infty$ because the Schr\"odinger equation has no damping. We can fix this by putting a small, artificial damping term in the Schr\"odinger equation. To do this we replace the Hamiltonian $\Hhat$ by $\Hhat - i\epsilon$, where $\epsilon>0$ is the damping parameter, which causes all solutions die out as $e^{-\epsilon t/\hbar}$ as $t\to\infty$. With this substitution, the upper limit in {eq}`eq-greensfuns-57` goes to zero as $t\to\infty$, so the Fourier transform {eq}`eq-greensfuns-56` gives the definite result $1/(E+i\epsilon - \Hhat)$.

An equivalent point of view is to keep the Hamiltonian $\Hhat$ without modification, but to replace the energy parameter $E$ of the Fourier transform by $E+i\epsilon$, that is, to promote it into a complex variable that we push into the upper half of the complex plane by giving it a positive imaginary part. Let us write $z$ for a complexified energy, in this case $z=E+i\epsilon$, and define an outgoing Green's operator for such complex energies by

:::{math}
:label: eq-greensfuns-58
\Ghat_+(z) = {1\over i\hbar} \int_0^\infty e^{izt/\hbar} \, U(t) = {1 \over z-\Hhat} \qquad \\text{\Im z >0}.
:::

Later we will have to take the limit $\epsilon\to0$ to get the Green's operator for physical (that is, real) values of the energy.

(sec-greensfuns-13)=

## Properties of $\Ghat_+(z)$ for $\Im z>0$

Thus the Green's operator $\Ghat_+(z)$ is just the inverse of the operator $z-\Hhat = E+i\epsilon-\Hhat$ for $\Im z >0$. This operator is not Hermitian, but it does have a complete set of orthonormal eigenfunctions, namely, those of $\Hhat$. And since the eigenvalues of $\Hhat$ are all real, the eigenvalues of $z-\Hhat$ always have a nonzero imaginary part (since $\Im z = \epsilon \ne 0$), and never vanish. Thus, for $\epsilon >0$, the inverse of $z-\Hhat$ exists and is unique.

Let us write the inverse of $z-\Hhat$ in terms of the eigenvalues and eigenprojectors of $\Hhat$, as in {eq}`eq-hilbert-130`. Suppose that $\Hhat$ has some discrete, negative eigenvalues $E_n <0$ and corresponding eigenstates $\ket{n \alpha}$,

:::{math}
:label: eq-greensfuns-59
\Hhat \ket{n \alpha} = E_n \ket{n \alpha},
:::

where $\alpha$ is an index introduced to resolve any degeneracies, and a continuous spectrum of positive energies $E\ge 0$ and corresponding eigenstates $\ket{E \alpha}$,

:::{math}
:label: eq-greensfuns-60
\Hhat\ket{E \alpha} = E \ket{E \alpha}.
:::

This would be the normal case for kinetic-plus-potential Hamiltonians for a single particle in one, two or three dimensions. For simplicity let us assume that $\alpha$ is a discrete index (although in practice this may be continuous, too). Then the eigenstates can be normalized so as to satisfy the orthonormality conditions,

:::{math}
:label: eq-greensfuns-61
\begin{aligned}
\braket{n \alpha}{n' \alpha'} &= \delta_{\alpha\alpha'} \, \delta_{nn'}, \\
\braket{n \alpha}{E \alpha'} &= 0, \\
\braket{E \alpha}{E' \alpha'} &= \delta_{\alpha\alpha'}\, \delta(E-E'), \\

\end{aligned}
:::

and the resolution of the identity is

:::{math}
:label: eq-greensfuns-62
1 = \sum_{n\alpha} \ketbra{n \alpha}{n\alpha} + \int_0^\infty dE\, \sum_\alpha \ketbra{E \alpha}{E\alpha}.
:::

Corresponding to this is a resolution of the Green's operator,

:::{math}
:label: eq-greensfuns-63
\Ghat_+(E+i\epsilon) = {1\over E+i\epsilon-\Hhat} = \sum_{n\alpha} {\ketbra{n\alpha}{n\alpha} \over E+i\epsilon-E_n} + \int_0^\infty dE' \, \sum_\alpha {\ketbra{E'\alpha}{E'\alpha} \over E+i\epsilon-E'},
:::

where we have changed the variable of integration over positive energy eigenstates to $E'$ to avoid confusion with the energy parameter $E$ of the Green's operator. We see that as long as $\epsilon>0$, none of the denominators in {eq}`eq-greensfuns-63` vanish. Thus, regarded as a function of the complex variable $z$, $\Ghat_+(z) = 1/(z-\Hhat)$ is a well defined operator in the entire upper half energy plane, $\Im z>0$.

(sec-greensfuns-14)=

## $\Ghat_+$ for Real Energies

We must take $\epsilon\to0$ to obtain results for physical (that is, real) values of the energy. Let us define

:::{math}
:label: eq-greensfuns-64
\Ghat_+(E) = \lim_{\epsilon\to 0} \Ghat_+(E+i\epsilon),
:::

to the extent that this limit is meaningful. We are following the same procedure used with water waves, first taking $t\to\infty$ with finite damping, then letting the damping go to zero. To see if this is meaningful, we examine the three cases shown in {ref}`fig-greensfuns-2`. These cases correspond precisely to the three cases examined earlier for water waves.

:::{figure} images/greensfuns-fig02.png
:label: fig-greensfuns-2
:width: 80%

Different cases for the limit $\epsilon\to 0$ in the definition of $\Ghat(E)$. The spectrum of $\Hhat$ consists of a discrete set of negative eigenvalues $E_n$, plus a continuum of positive eigenvalues $E\ge 0$ (heavy line).
:::

In case (a), $\Re z = E$ is not equal to any of the eigenvalues of $\Hhat$, either discrete or continuous. This means that $E$ is a negative energy lying in one of the gaps between the discrete, negative eigenvalues $E_n$. In this case, as $\epsilon\to0$ none of the denominators in {eq}`eq-greensfuns-63` vanish, either in the discrete sum, where $E \ne$ any $E_n$, or in the continuous integral, where the variable of integration $E'$ is positive while $E<0$. Thus, the limit is defined, and $\Ghat(E) = 1/(E-\Hhat)$. The inverse of $E-\Hhat$ is meaningful and unique for such real energies.

In case (b), $\Re z$ is equal to $E_n$, one of the discrete, negative eigenvalues of a bound state of the system. In this case, one of the terms in the sum {eq}`eq-greensfuns-63` diverges as $\epsilon\to 0$, in fact, for small $\epsilon$ the sum is dominated by one term that is proportional to the projection operator onto the eigenspace corresponding to $E_n$,

:::{math}
:label: eq-greensfuns-65
P_n =\sum_\alpha \ketbra{n\alpha}{n\alpha}
:::

(see {ref}`sec-hilbert-24`). For such energies the Green's operator $\Ghat_+(E)$ does not exist (it diverges).

In case (c), $\Re z>0$, so as $\epsilon\to0$ we approach one of the positive eigenvalues of the continuous spectrum of $\Hhat$. In this case, none of the denominators in the discrete sum in {eq}`eq-greensfuns-63` vanish, but the denominator under the integral does approach zero at $E'=E$, which is part of the range of integration. As it turns out, the limit of the integral as $\epsilon\to0$ is defined nevertheless. We will not prove this fact, but we will work out an example later (in \secrgreensfuns-18) in which we will see that the $E'$-integral is well behaved as $\epsilon\to0$, in spite of the singularity in the integrand. Thus, for $E>0$, $G_+(E)$ is defined. It would be tempting to write simply $1/(E-\Hhat)$ for this operator, but at positive energies taking the limit $\epsilon\to0$ is not the same as just setting $\epsilon=0$. In particular, if we just set $\epsilon=0$ in {eq}`eq-greensfuns-63`, then the integral is not defined as it stands due to the singularity in the integrand at $E'=E$. When integrals like this arise some books simply offer a “prescription” of replacing $E$ by $E+i\epsilon$ (whereupon the integral is defined) and then taking the limit. This prescription, as we see, amounts to using the outgoing Green's function. At positive energies (energies belonging to the continuous spectrum) it is better not to use the notation $1/(E-\Hhat)$. Instead, it is better to be more explicit and write $\lim_{\epsilon \to 0} 1/(E+i\epsilon-\Hhat)$.

Now we must prove that $\Ghat_+(E)$, when it is defined (that is, when $E$ is not equal to any of the discrete, bound state eigenvalues $E_n$), is actually a Green's operator for the inhomogeneous Schr\"odinger equation {eq}`eq-greensfuns-43`. That is, we must show that it satisfies {eq}`eq-greensfuns-48`. We do this by using the definition {eq}`eq-greensfuns-64`,

:::{math}
\begin{aligned}
(E-\Hhat) \Ghat_+(E) &= \lim_{\epsilon\to0} (E-\Hhat)G_+(E+i\epsilon) =\lim_{\epsilon\to0} (E+i\epsilon -\Hhat -i\epsilon) {1 \over E+i\epsilon-\Hhat}
\end{aligned}
:::

:::{math}
\begin{aligned}
&= \lim_{\epsilon\to0} [1 -i\epsilon \Ghat(E+i\epsilon)] =1, & {eq}`eq-greensfuns-66`
\end{aligned}
:::

where in the second equality we add and subtract $i\epsilon$ inside the first factor and in the third equality we use the fact that the inverse of $E+i\epsilon-\Hhat$ is well defined when $\epsilon>0$. In the final step we use the assumption that $E$ is such that $G_+(E)$ is defined, so the limit of $\epsilon G_+(E+i\epsilon)$ is zero.

Since $\Ghat_+(E)$, defined whenever $E$ is not equal to one of the discrete eigenvalues of $\Hhat$, is a Green's operator for the operator $E-\Hhat$, the corresponding Green's function $G_+(\xvec,\xvec',E)$ can be used to solve the inhomogeneous Schr\"odinger equation {eq}`eq-greensfuns-43` for such energies. In the next set of notes we shall show how this is used in scattering theory, but first we must examine another energy-dependent Green's operator.

(sec-greensfuns-15)=

## The Incoming Energy-Dependent Green's Operator

The *incoming* energy-dependent Green's operator, denoted $\Ghat_-(E)$, is defined basically as the Fourier transform of the incoming time-dependent Green's operator $\Khat_-(t)$,

:::{math}
:label: eq-greensfuns-67
\Ghat_-(E) = {1\over i\hbar} \int_{-\infty}^{+\infty} dt\, e^{iEt/\hbar} \, \Khat_-(t),
:::

apart from convergence issues. Compare this to definition {eq}`eq-greensfuns-56` for the outgoing Green's operator. Recall that $\Khat_-(t) = -\Theta(-t) U(t)$, so this integral is cut off for positive times, and can be written

:::{math}
:label: eq-greensfuns-68
\Ghat_-(E) = -{1\over i\hbar} \int_{-\infty}^0 dt\, e^{i(E-\Hhat)t/\hbar}.
:::

The integral can be done, but the antiderivative does not converge at the lower limit $t\to-\infty$, much as was the case with the integral for $G_+(E)$ at the upper limit $t\to\infty$. In this case we cure the problem by replacing $\Hhat$ by $\Hhat+i\epsilon$ in the Schr\"odinger equation, which causes all solutions to *grow* as $e^{\epsilon t/\hbar}$, thereby guaranteeing that any solution that is finite at $t=0$ is zero at $t=-\infty$ (the solutions damp if you go backwards in time). This substitution is equivalent to replacing $E$ by $E-i\epsilon$ in {eq}`eq-greensfuns-67`, thereby pushing the energy into the *lower* half of the complex plane and leading to the definition

:::{math}
:label: eq-greensfuns-69
\Ghat_-(z) = -{1\over i\hbar} \int_{-\infty}^0 e^{izt/\hbar} \, U(t) = {1 \over z-\Hhat} \qquad \\text{\Im z <0},
:::

where now $z=E-i\epsilon$. Compare this to {eq}`eq-greensfuns-58`; the final answer is the same formula, but it is defined in different parts of the complex energy plane.

Analyzing $\Ghat_-(z)$ as we did above with $\Ghat_+(z)$, we find that it is well defined in the entire lower half plane ($\Im z < 0$). To get a Green's operator defined at physical (real) values of $E$, we define

:::{math}
:label: eq-greensfuns-70
\Ghat_-(E) = \lim_{\epsilon\to0} \Ghat_-(E-i\epsilon),
:::

a limit that exists as long as $E$ is not equal to any of the discrete, bound state eigenvalues $E_n$ of $\Hhat$. Where the limit does exist, $\Ghat_-(E)$ is a legitimate Green's operator, that is, it satisfies

:::{math}
:label: eq-greensfuns-71
(E-\Hhat)G_-(E) = 1,
:::

and so can be used to solve inhomogeneous Schr\"odinger equations.

We did not present any situation analogous to the incoming Green's function in our discussion of water waves in \secrgreensfuns-10. It turns out that in cases (a) and (b), the water wave field corresponding to the incoming Green's function is the same as that for the outgoing Green's function (for the same value of $\omega$). In particular, the incoming Green's function also diverges when $\omega$ is equal to one of the eigenfrequencies $\omega_n$ of a finite lake and $\epsilon\to0$. But in case (c), the wave field on the infinite ocean is different in the two cases (incoming and outgoing). Whereas the outgoing wave field consists of waves carrying a steady flux of energy away from the driver out to infinity, the incoming wave field carries energy in the opposite direction. That is, in the limit of zero damping, the water wave field on the infinite ocean corresponding to the incoming Green's function consists of waves carrying a steady flux of energy inward from infinity, concentrating it in ever smaller regions of space near the driver, which finally absorbs this energy.

It is obvious that it would be very difficult to set up even an approximation to the incoming wave field experimentally, while setting up the outgoing wave field would be easy. Correspondingly, the incoming Green's function is not used in solving actual scattering problems, but it is useful in studying theoretical aspects of scattering.

(sec-greensfuns-16)=

## The Discontinuity Across the Real Energy Axis

We should not be surprised to find more than one Green's function or operator, since these are not unique. This is because Green's functions are themselves solutions of an inhomogeneous wave equation, for example, {eq}`eq-greensfuns-45`, and are only determined by that equation to within the addition of a solution of the homogeneous equation. Thus the difference between any two Green's functions is a solution of the homogeneous equation (in our case, it is an eigenfunction of $H$ with energy $E$).

Nevertheless, since we have two specific Green's operators $\Ghat_\pm(E)$ defined for real energies $E\ne E_n$, it is of interest to compute the difference between them. Let us denote the difference by ${\hat \Delta}$,

:::{math}
:label: eq-greensfuns-72
{\hat\Delta}(E) = \lim_{\epsilon\to0} [\Ghat_+(E+i\epsilon) - \Ghat_-(E-i\epsilon)] =\lim_{\epsilon\to0}\Bigl( {1\over E+i\epsilon-\Hhat} - {1\over E-i\epsilon-\Hhat}\Bigr).
:::

This limit is easier to understand if we replace $E$ by $x$ and $\Hhat$ by $x_0$, and consider the analogous limit for ordinary numbers (not operators):

:::{math}
:label: eq-greensfuns-73
\lim_{\epsilon\to0} \Bigl( {1\over x-x_0+i\epsilon} - {1\over x-x_0-i\epsilon}\Bigr) = \lim_{\epsilon\to0} {-2i\epsilon \over (x-x_0)^2 + \epsilon^2}.
:::

The final fraction is a quantity that approaches zero as $\epsilon\to 0$ for all $x\ne x_0$, but it approaches infinity as $\epsilon\to 0$ when $x=x_0$. Moreover, regarded as a function of $x$ it is a Lorentzian function with area that is independent of $\epsilon$,

:::{math}
:label: eq-greensfuns-74
\int_{-\infty}^{+\infty} dx \, {\epsilon \over (x-x_0)^2 + \epsilon^2} = \pi,
:::

and it becomes ever more sharply localized about $x=x_0$ as $\epsilon\to0$. It is, therefore, a representation of the $\delta$-function,

:::{math}
:label: eq-greensfuns-75
\lim_{\epsilon\to 0} {\epsilon \over (x-x_0)^2 + \epsilon^2} = \pi \,\delta(x-x_0).
:::

Thus we can write {eq}`eq-greensfuns-72` as

:::{math}
:label: eq-greensfuns-76
{\hat\Delta}(E) = -2\pi i \,\delta(E-\Hhat).
:::

The operator $\delta(E-\Hhat)$ is strange-looking, but it is defined by the methods of {ref}`sec-hilbert-25`. In particular, expanding this operator in the eigenbasis of $\Hhat$, we have

:::{math}
:label: eq-greensfuns-77
\delta(E-\Hhat) = \sum_{n\alpha} \ketbra{n\alpha}{n\alpha} \, \delta(E-E_n) + \int_0^\infty dE' \sum_\alpha \ketbra{E'\alpha}{E'\alpha} \, \delta(E-E').
:::

Let us examine ${\hat \Delta}(E)$ in the three cases considered above. When $E$ lies in the gaps between the negative eigenvalues $E_n$ of $\Hhat$ (case (a)), then the $\delta$-functions in the sum over discrete states are all zero, since $E\ne$ any $E_n$. Also, the $\delta$-function under the integral over positive energies vanishes, since $E'>0$ and $E<0$. Thus, ${\hat\Delta}(E)=0$ for such energies, and $G_+(E+i\epsilon)$ and $G_-(E-i\epsilon)$ approach the same limit (the operator $1/(E-\Hhat)$, which is well defined and unique for such energies). In case (b), when $E=E_n$ for some $n$, one of the $\delta$-functions in the sum over discrete states is infinity, and ${\hat\Delta}(E)$ is not defined for such energies (it diverges). In case (c), when $E>0$, the $\delta$-functions in the discrete sum all vanish, but the $\delta$-function under the integral gives a nonzero answer, and we find

:::{math}
:label: eq-greensfuns-78
{\hat\Delta}(E) = -2\pi i\sum_\alpha \ketbra{E\alpha}{E\alpha} \qquad \\text{E>0}.
:::

Later we will evaluate this final expression explicitly for the case of a free particle.

We see that for positive energies, the two Green's operators $\Ghat_\pm(E)$ are well defined, but they are not the same operator. This is why notation like $1/(E-\Hhat)$ is ambiguous for such energies; instead, it is better to be more explicit and to write $\lim_{\epsilon\to0} 1/(E\pm i\epsilon -\Hhat)$.

(sec-greensfuns-17)=

## The Green's Operator as an Analytic Function of Complex Energy

These results show that $\Ghat_-(z)$ is the analytic continuation of $\Ghat_+(z)$ through the gaps between the discrete, negative eigenvalues $E_n$ of $\Hhat$, and that, in a sense, these are the same operator, call it $\Ghat(z)$, uniquely defined everywhere in the complex energy plane where $\Im z\ne0$, with certain limits as the real axis is approached from above or below. This operator is called the *resolvent*. It may be expanded in the energy eigenbasis,

:::{math}
:label: eq-greensfuns-79
\Ghat(z) = {1\over z-\Hhat} = \sum_{n\alpha} {\ketbra{n\alpha}{n\alpha} \over z-E_n} + \int_0^\infty dE' \sum_\alpha {\ketbra{E'\alpha}{E'\alpha} \over z-E'}.
:::

It is natural to borrow language from complex variable theory to describe the dependence of $\Ghat(z)$ on $z$, even though the usual notion of an analytic function applies to a complex-valued function of a complex variable, and we have here an operator-valued function. Without defining what the latter means precisely we just remark that one can always speak of the matrix elements of the resolvent, that is, the Green's function

:::{math}
:label: eq-greensfuns-80
G(\xvec,\xvec',z)=\matrixelement{\xvec}{\Ghat(z)}{\xvec'},
:::

which is a complex-valued function of $z$.

From this point of view we see from the expansion {eq}`eq-greensfuns-79` that the resolvent $\Ghat(z)$ is an analytic function of $z$ whenever none of the denominators vanish, that is, everywhere in the complex plane where $\Im z\ne0$ and on the negative real axis between the discrete eigenvalues. The resolvent evidently has poles at the discrete, negative, bound state eigenvalues $E_n$, whose residues are the projectors onto the corresponding energy eigenspaces. The residues can be picked up from a Cauchy-type contour integral that only samples $\Ghat(z)$ at $z$ values for which it is defined,

:::{math}
:label: eq-greensfuns-81
P_n = \sum_{\alpha} \ketbra{n\alpha}{n\alpha} = {1\over 2\pi i} \int_C {dz \over z-\Hhat},
:::

where the contour $C$, illustrated in {ref}`fig-greensfuns-3`, encloses the pole at $z=E_n$ (and no other).

:::{figure} images/greensfuns-fig03.png
:label: fig-greensfuns-3
:width: 80%

Contour $C$ for the integral {eq}`eq-greensfuns-81`, giving the projector onto the energy eigenspace with eigenvalue $E_n$.
:::

:::{figure} images/greensfuns-fig04.png
:label: fig-greensfuns-4
:width: 80%

The branch cut at positive energies can be deformed, revealing further singularities of $\Ghat(z)$ on a second Riemann sheet.
:::


As for the continuous spectrum of $\Hhat$ on the positive real energy axis, $\Ghat(z)$ approaches different values as $z$ approaches $E>0$ from above or below. This is interpreted by saying that $\Ghat(z)$ has a branch cut extending from $E=0$ to $E=\infty$ along the real axis, whose discontinuity is the operator ${\hat\Delta}(E)$ given by {eq}`eq-greensfuns-76`. $\Ghat(z)$ on one side of this branch cut can be analytically continued across the branch cut to the other side, but the result is not $\Ghat(z)$ on the other side, rather it is $\Ghat(z)$ on a second Riemann sheet that is revealed when we push the branch cut aside. See {ref}`fig-greensfuns-4`, where $\Ghat(z)$ is analytically continued from the upper half plane into the lower. When this is done, sometimes further singularities are revealed, which like those on the first (original) Riemann sheet have physical significance. In particular, a pole on the second Riemann sheet in the lower half complex plane represents a *resonance* of the Hamiltonian $\Hhat$, that is, a long-lived state that is actually part of the continuum but which behaves for short times (short compared to the decay time) as if it were a discrete energy eigenstate. We have seen resonances previously in one-dimensional problems (which we analyzed by WKB theory, see Prob. {ref}`prob-wkb-3`), and in the doubly excited states of helium (see {ref}`sec-helium-9`). We will encounter them again when we study the decay of excited atomic states by the emission of a photon, in {ref}`ch-nlw`.

We see that the singularities of $\Ghat(z)$ contain coded within themselves all of the physical information we might require about the Hamiltonian $\Hhat$: its discrete eigenvalues, the projectors onto the corresponding eigenspaces (from which the bound state eigenfunctions may be extracted), the continuous spectrum, and even the resonances. As we shall see, the resolvent $\Ghat(z)$ also allows us to compute the scattering amplitude and the (related) $S$-matrix for positive energies. As such, the operator $\Ghat(z)$ is an object of central importance in quantum mechanics.

This very richness, however, means that finding $\Ghat(z)$ explicitly is equivalent to (and just as difficult as) solving the original Hamiltonian $\Hhat$, and that for most practical problems we will have to resort to perturbation theory or numerical methods to find $\Ghat(z)$. We will shortly see some perturbative approaches to finding $\Ghat(z)$, and Prob. {ref}`prob-lippschw-1` is an example in which the exact Green's operator can be found analytically.

(sec-greensfuns-18)=

## The Free-Particle Green's Functions $G_{0\pm}(\xvec,\xvec',E)$

As an example, let us compute the outgoing and incoming Green's functions for a free particle. This case is simple enough that we can do all the calculations explicitly, and it is important also for applications to scattering theory. We denote the free particle Green's functions (outgoing and incoming) by $G_{0\pm}(\xvec,\xvec',E)$, with a 0-subscript that means “free particle.” We shall compute these Green's functions both for $E>0$ and $E<0$, and use them to illustrate some of the general theory presented above.

To find $G_{0+}$ we use {eq}`eq-greensfuns-58` with $z=E+i\epsilon$, deferring the limit $\epsilon\to0$ until later. We introduce the momentum representation, in which $\Ghat_{0+}$ is diagonal, so that

:::{math}
\begin{aligned}
G_{0+}(\xvec,\xvec';z) &= \matrixelement{\xvec} {{1\over z -\Hhat_0}}{\xvec'} =\int d^3\pvec \, d^3\pvec'\, \braket{\xvec}{\pvec} \matrixelement{\pvec}{{1\over z-\Hhat_0}}{\pvec'} \braket{\pvec'}{\xvec'}
\end{aligned}
:::

:::{math}
:label: eq-greensfuns-82
\begin{aligned}
&\qquad= \int {d^3\pvec \over (2\pi\hbar)^3} \, { e^{i\pvec\cdot(\xvec-\xvec')/\hbar} \over z- p^2/2m},
\end{aligned}
:::

where we use

:::{math}
:label: eq-greensfuns-83
\matrixelement{\pvec}{{1\over z-\Hhat_0}}{\pvec'} = { \delta(\pvec-\pvec') \over z- p^2/2m}.
:::

{eq}`eq-greensfuns-82` makes it clear that the Green's function depends only on the vector difference,

:::{math}
:label: eq-greensfuns-84
\xivec = \xvec-\xvec'
:::

(this is a consequence of the translational invariance of the free-particle Hamiltonian $H_0$).

We change variables of integration in {eq}`eq-greensfuns-82` by $\pvec=\hbar\qvec$ and we write

:::{math}
:label: eq-greensfuns-85
z = E+i\epsilon = {\hbar^2 w^2 \over 2m},
:::

so that $w$ is a complex version of $k$. The parameter $w$ is specified in terms of the complex energy by

:::{math}
:label: eq-greensfuns-86
w = {\sqrt{2mz} \over \hbar} = {\sqrt{2m(E+i\epsilon)} \over \hbar},
:::

but we must say which of the two square roots is intended. We treat $\epsilon$ as small and illustrate the two cases $E>0$ and $E<0$ in {ref}`fig-greensfuns-5`. When $E=E_1>0$, we take $w$ to lie just above the real axis, like $w_1$ in the figure. When $E=E_2<0$, we take $w$ to lie just to the right of the imaginary axis, like $w_2$ in the figure. Then as $\epsilon\to0$, we define

:::{math}
:label: eq-greensfuns-87
\begin{aligned}
\lim_{\epsilon\to0} w = \begin{cases} k, & E\ge0, \\ i\kappa, & E\le 0. \\\end{cases}
\end{aligned}

:::

where

:::{math}
:label: eq-greensfuns-88
k={\sqrt{2mE} \over \hbar}, \qquad E\ge0,
:::

and

:::{math}
:label: eq-greensfuns-89
\kappa = {\sqrt{2m|E|} \over \hbar}, \qquad E\le0.
:::

Thus, $k$ is the usual wave number for positive energies, while $\kappa$ is the exponential decay factor for free-particle solutions of negative energy.

:::{figure} images/greensfuns-fig05.png
:label: fig-greensfuns-5
:width: 80%

Defining the branch of $w$, the complex version of the wave number $k$, in the case $z=E+i\epsilon$ (outgoing Green's function).
:::

:::{figure} images/greensfuns-fig06.png
:label: fig-greensfuns-6
:width: 80%

Doing the same for the case $z=E-i\epsilon$ (incoming Green's function).
:::


With these changes of notation we have

:::{math}
:label: eq-greensfuns-90
G_{0+}(\xvec,\xvec',z) = -{1\over (2\pi)^3} {2m \over \hbar^2} \int d^3\qvec \, {e^{i\qvec\cdot\xivec} \over q^2 - w^2}.
:::

This equation makes it clear that the Green's function actually depends only on the magnitude of $\xivec$, since the integral is invariant if we replace $\xivec$ by $\Rmat\xivec$, where $\Rmat$ is any rotation matrix. This is due to the rotational invariance of the Hamiltonian $\Hhat_0$. Therefore without loss of generality we can place $\xivec$ on the $z$-axis, so that $\qvec\cdot\xivec = qR\cos\theta$, where $\theta$ is the usual spherical angle in $\qvec$-space and where

:::{math}
:label: eq-greensfuns-91
R=|\xivec|=|\xvec-\xvec'|.
:::

Then carrying out the angular integrations we have

:::{math}
:label: eq-greensfuns-92
G_{0+}(\xvec,\xvec';z) = -{1\over (2\pi)^2} {2m\over \hbar^2} {1\over iR} \int_0^\infty q\, dq\, {e^{iqR} - e^{-iqR} \over q^2-w^2}.
:::

As for the term with $-e^{-iqR}$, we substitute $q'=-q$ and drop the prime, which makes the integrand the same as the first term, but with range of integration $-\infty$ to $0$. Thus the two terms together are

:::{math}
:label: eq-greensfuns-93
G_{0+}(\xvec,\xvec';z) = -{1\over (2\pi)^2} {2m\over \hbar^2} {1\over iR} \int_{-\infty}^\infty q\, dq\, {e^{iqR} \over (q-w)(q+w)}.
:::

This final integral can be evaluated by Cauchy's residue theorem. The integrand decays exponentially in the upper half $q$-plane, so we can close the contour of integration with a semicircle at infinity, which then picks up the pole at $q=w$. Notice that it is essential that $w$ be off the real axis (that is, $\epsilon>0$) for this to work. The result is

:::{math}
:label: eq-greensfuns-94
G_{0+}(\xvec,\xvec';z) = -{1 \over 4\pi} {2m \over \hbar^2} {e^{iwR} \over R},
:::

where it is understood that $z=E+i\epsilon$ and that $w$ lies in the first quadrant.

We may treat the incoming Green's function $G_-(\xvec,\xvec',z)$ similarly, where now $z=E-i\epsilon$. Now $z$ lies in the lower half plane and $w$, defined by

:::{math}
:label: eq-greensfuns-95
w = {\sqrt{2mz} \over \hbar} = {\sqrt{2m(E-i\epsilon)} \over \hbar},
:::

can be taken to lie in the fourth quadrant, as illustrated in {ref}`fig-greensfuns-6`. Now in the limit $\epsilon\to0$ we have

:::{math}
:label: eq-greensfuns-96
\begin{aligned}
\lim_{\epsilon\to0} w = \begin{cases} k, & E\ge0, \\ -i\kappa, & E\le 0. \\\end{cases}
\end{aligned}

:::

Evaluating the integral in this case we find

:::{math}
:label: eq-greensfuns-97
G_{0-}(\xvec,\xvec',z) = -{1 \over 4\pi} {2m \over \hbar^2} {e^{-iwR} \over R}.
:::

Finally we take the limit $\epsilon\to0$, using either {eq}`eq-greensfuns-87` or {eq}`eq-greensfuns-96` for the outgoing and incoming cases, respectively. The results can be summarized by

:::{math}
:label: eq-greensfuns-98
\begin{aligned}
G_{0\pm}(\xvec,\xvec',E) = -{1 \over 4\pi} {2m \over \hbar^2} \begin{cases} \ds { \ds e^{\pm ik|\xvec-\xvec'|} \over \ds |\xvec-\xvec'|}, & E\ge0, \\  \ds { \ds e^{-\kappa |\xvec-\xvec'|} \over \ds |\xvec-\xvec'| }, & E\le 0.  \\\end{cases}
\end{aligned}

:::

One point to notice is that this limit *exists*. This is an example of the integral in {eq}`eq-greensfuns-63` when $E>0$, showing that the limit exists when $\epsilon\to0$, in spite of the fact that the integrand diverges at one point.

{eq}`eq-greensfuns-98` gives the Green's functions $G_{0\pm}$ explicitly for a free particle. Each satisfies the inhomogeneous Schr\"odinger equation {eq}`eq-greensfuns-45`, which in the case of a free particle is

:::{math}
:label: eq-greensfuns-99
\Bigl(E+{\hbar^2\over 2m}\del^2\Bigr) G(\xvec,\xvec',E) = \delta^3(\xvec-\xvec'),
:::

so $G_{0\pm}(\xvec,\xvec',E)$ is a free particle solution of energy $E$ at all spatial points $\xvec$ except $\xvec=\xvec'$, where $R=0$ and $G_{0\pm}$ is singular. For $E>0$, the free particle solution in the region $R>0$ consists of spherical waves either radiating outward (for $G_{0+}$) or inward (for $G_{0-}$). (The waves are seen to radiate one direction or another when we attach the time dependence $e^{-iEt/\hbar}$.)

(sec-greensfuns-19)=

## Discontinuity ${\hat\Delta}(E)$ for the Free Particle

As predicted in \secrgreensfuns-16, the Green's functions $G_{0\pm}$ are analytic continuations of one another across the negative real energy axis, where of course there are no poles for discrete states because this is the case of a free particle. That is, $\Ghat_{0+}(E)=\Ghat_{0-}(E)$ for $E<0$. As for the positive energy axis, there is a discontinuity given by

:::{math}
:label: eq-greensfuns-100
\Delta(\xvec,\xvec',E) = G_{0+}(\xvec,\xvec',E) - G_{0-}(\xvec,\xvec',E) = -{i \over 2\pi} {2m \over \hbar^2} {\sin kR \over R}, \qquad \\text{E\ge0}.
:::

According to {eq}`eq-greensfuns-76`, this final result should be the matrix element,

:::{math}
:label: eq-greensfuns-101
\matrixelement{\xvec}{{\hat \Delta}(E)}{\xvec'} = -2\pi i \matrixelement{\xvec}{\delta(E-H_0)}{\xvec'}.
:::

We leave it as an exercise to show that this is true. (One can compute the matrix element by switching to a momentum representation, as we did in {eq}`eq-greensfuns-82` for the Green's function.)

% Ideas about problems. % 1) Derive reflection of light wave from mirror both ways. % 2) There are many “exercises for the reader” in these notes. % 3) Calculate G_{0\pm} in 1d. % 4) Show explicitly using del^2(1/R) that G_0 satisfies wave eqn.
