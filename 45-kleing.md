---
title: "45. Introduction to Relativistic Quantum Mechanics and the Klein-Gordon Equation"
---
(ch-kleing)=

# 45. Introduction to Relativistic Quantum Mechanics and the Klein-Gordon Equation

(sec-kleing-1)=

## Introduction

We turn now to relativistic quantum mechanics. We follow a roughly historical order in presenting this material, even though it involved some misconceptions at various stages. It would be possible to leapfrog directly to the modern point of view, but some important ideas would have to be badly unmotivated. Along the way we will learn many things that are indispensable for the modern point of view.

(sec-kleing-2)=

## Early Attempts by Schr\"odinger

See {ref}`sec-spatialdof-12` for a simplified version of the history leading up to the development of the Schr\"odinger equation. We take up the story here with the ideas of de~Broglie, in which a free particle of mass $m$, momentum $\pvec$, and energy

:::{math}
:label: eq-kleing-1
E=\sqrt{m^2c^4 + c^2\pvec^2}
:::

was somehow to be associated with a plane wave,

:::{math}
:label: eq-kleing-2
e^{i(\kvec\cdot\xvec-\omega t)},
:::

where the frequency $\omega$ and wave vector $\kvec$ were related to the energy and momentum by the Einstein relations $E=\hbar\omega$ and $\pvec=\hbar\kvec$. Thus, the wave can also be written,

:::{math}
:label: eq-kleing-3
e^{i(\pvec\cdot\xvec-Et)/\hbar}.
:::

Einstein had first proposed these relations for particles of light, only later named photons, and de~Broglie had suggested that they should apply to material particles as well.

In addition to free particles, de~Broglie also thought about particles moving in a potential. He realized that the Einstein relations, combined with Bohr's quantization condition in the old quantum theory,

:::{math}
:label: eq-kleing-4
\oint \pvec\cdot d\xvec = nh,
:::

where the integral is taken around a closed classical orbit, would imply that there was an integral number of wavelengths along the quantized orbits. We now know that this is a version of the WKB quantization condition, an introduction to which is provided in {ref}`ch-wkb`.

In 1925 Schr\"odinger set about to follow up on a remark made by Debye, that if there was a wave there should be a wave equation. Thus the problem was to find the wave equation of which {eq}`eq-kleing-3` was the solution. Noticing that $i\hbar\partial/\partial t$ acting on {eq}`eq-kleing-3` brings down $E$, while $-i\hbar\del$ brings down $\pvec$, Schr\"odinger guessed that the wave equation should be

:::{math}
:label: eq-kleing-5
i\hbar \frac{\partial \psi}{\partial t} = \sqrt{m^2 c^4 -\hbar^2 c^2 \del^2} \,\psi,
:::

that is, an equation which encodes the energy-momentum relation {eq}`eq-kleing-1` by means of operators.

Unfortunately, the square root in this equation is hard to interpret. It makes sense in momentum space, but it is nonlocal in real space and not very attractive. Moreover, it does not treat space and time on an equal footing, as we would expect for a relativistic theory, so it's hard to see how it can be covariant. To fix this, Schr\"odinger squared the energy momentum relation {eq}`eq-kleing-1`,

:::{math}
:label: eq-kleing-6
E^2 = m^2c^4 + c^2 p^2,
:::

and transcribed this into a wave equation, again making the replacements $E\to i\hbar\partial/\partial t$, $\pvec\to-i\hbar\del$. This gave

:::{math}
:label: eq-kleing-7
-\hbar^2 {\partial^2 \psi \over \partial t^2} = m^2c^4 \psi -\hbar^2 c^2 \del^2 \psi.
:::

This equation is now known as the *Klein-Gordon equation* for a free particle. An equivalent form is

:::{math}
:label: eq-kleing-8
\dAlembertian\psi = {1\over c^2} {\partial^2 \psi \over \partial t^2} - \del^2 \psi = -\Bigl( {mc\over\hbar}\Bigr)^2 \psi,
:::

where $\dAlembertian$ is the d'Alembertian or wave operator.

(sec-kleing-3)=

## The Compton Wave Length

On the right of {eq}`eq-kleing-8` appears the inverse of the *Compton wave length* of the particle, defined by

:::{math}
:label: eq-kleing-9
\lambda_C = {\hbar \over mc}.
:::

This is a characteristic distance associated with the particle, which has the following physical interpretation. Suppose a particle of mass $m$ is confined to a box of size $L$. By the uncertainty principle, the momentum must take on values of the order of $\hbar/L$. The momentum increases as the box is made smaller. How small must we make the box such that the momentum takes on relativistic values, say, $p\sim mc$? The answer is clearly $\hbar/mc$, the Compton wavelength. Thus, the Compton wavelength is the scale at and below which the effects of relativistic quantum mechanics become important. The distance $\lambda_C$ is attributed to Compton because it appears in his analysis of the elastic scattering of x-rays by electrons, published in 1923.

Lighter particles have longer Compton wavelengths. The electron's Compton wavelength is $\alpha$ (the fine structure constant) times the Bohr radius:

:::{math}
:label: eq-kleing-10
{\hbar\over mc} = \alpha a_0 = {e^2\over \hbar c} {\hbar^2\over me^2} = 3.9\times 10^{-11}\\textcm \;\\text{electrons}.
:::

Thus, the effects of relativistic quantum mechanics are important for an electron on a length scale that is roughly the size of an atom divided by 137. For the $\pi$-meson the Compton wave length is approximately $1.4\times 10^{-13}\\textcm$, roughly the range of the nuclear forces. See \tdpt.15, where it is explained that the Yukawa potential is the time-independent Green's function for Klein-Gordon equation {eq}`eq-kleing-8`. For the photon, for which $m=0$, the Compton wavelength is infinite, so photons are relativistic at all distance scales. Notice that for photons the Klein-Gordon equation becomes the wave equation,

:::{math}
:label: eq-kleing-11
\dAlembertian \psi = {1\over c^2} {\partial^2 \psi \over \partial t^2} - \del^2 \psi = 0,
:::

which of course comes out of Maxwell's equations and describes the propagation of light waves.

(sec-kleing-4)=

## Negative Energy Solutions

Given the plane wave {eq}`eq-kleing-3`, we found the Klein-Gordon equation as the equation that it satisfies. Let's turn this around and ask, given the Klein-Gordon equation, what is the most general plane wave solution? Parameterizing the plane wave by $E$ and $\pvec$ as in {eq}`eq-kleing-3` and substituting into the Klein-Gordon equation {eq}`eq-kleing-8`, we obtain {eq}`eq-kleing-6` again, or,

:::{math}
:label: eq-kleing-12
E=\pm\sqrt{m^2c^4 +c^2\pvec^2}.
:::

If $E$ and $\pvec$ are connected by this relation, for either choice of sign, then the wave {eq}`eq-kleing-3` satisfies the Klein-Gordon equation. {eq}`eq-kleing-12` is of course the relativistic energy-momentum relation all over again, except with the possibility of solutions in which $E<0$ (with the choice of the minus sign on the square root). We would not have obtained these solutions if we had used {eq}`eq-kleing-5`, but Schr\"odinger's act of squaring the classical energy-momentum relation has introduced them. The Klein-Gordon equation possesses solutions of negative energy.

To avoid confusion, we remark that in a relativistic context we usually include the rest mass in an accounting of the energy of a particle, while in a nonrelativistic context we usually do not. For example, if $v/c\ll 1$, or, equivalently, $p\ll mc$, then {eq}`eq-kleing-1` can be expanded, giving

:::{math}
:label: eq-kleing-13
E=mc^2 + {p^2\over 2m} + \ldots.
:::

This shows that at low velocities $E$ is the energy of the rest mass, $mc^2$, plus the usual nonrelativistic kinetic energy. Of course we frequently see solutions of the nonrelativistic Schr\"odinger equation with negative energy (for example, the bound states of hydrogen), but those energies are measured relative to $mc^2$. If $mc^2$ is added to those negative energies, the result is always positive, since $mc^2$ is large compared to the usual energies of a nonrelativistic problem. What we are talking about in the case of the negative energies of the Klein-Gordon equation are energies that are negative even when $mc^2$ is included in the accounting of the energy. For example, with the choice of the minus sign in {eq}`eq-kleing-12`, we have $E \le -mc^2$.

The choice of the minus sign in {eq}`eq-kleing-12` gives negative energies that have no analog either in classical relativity theory or in the nonrelativistic quantum theory, so we have no interpretation for them. It took several years to understand them properly, and in the end it turns out that they are related to the existence of antiparticles, in a somewhat nontrivial way. This will be one of the most important conclusions in our story of the development of relativistic quantum mechanics, but in 1925 neither Schr\"odinger nor anyone else had any idea of the existence of antimatter, so the negative energy solutions were a puzzle. We will ignore these interpretational difficulties for now and push on to explore the properties of the Klein-Gordon equation.

(sec-kleing-5)=

## Covariant Notation for the Klein-Gordon Equation

If an equation is consistent with the principles of special relativity, it should be possible to write it in covariant form, that is, in a form that is the same in all Lorentz frames. This usually involves writing the equation in terms of 4-vectors and tensors. See Appendix~\tensor\ for a review of tensor analysis, including a discussion of tensors in special relativity. Covariant notation implies among other things a notation in which the space and time coordinates are placed on an equal footing. Sometimes we prefer a notation in which space and time are treated separately. We will call this “$3+1$-notation”. {eq}`eq-kleing-8` is the Klein-Gordon equation in $3+1$-notation.

To put it into covariant notation, we introduce the space-time “position” contravariant 4-vector $x^\mu$ and its covariant version $x_\mu$,

:::{math}
:label: eq-kleing-14
x^\mu=\begin{pmatrix}ct \\ \xvec\\\end{pmatrix}, \qquad x_\mu = \begin{pmatrix}ct \\ -\xvec\\\end{pmatrix},
:::

where we use the metric

:::{math}
:label: eq-kleing-15
\begin{aligned}
g_{\mu\nu} = g^{\mu\nu} = \begin{pmatrix}1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & -1 & 0 \\ 0 & 0 & 0 & -1\\\end{pmatrix}
\end{aligned}

:::

to raise and lower indices. See {ref}`sec-tensor-12` for raising and lowering indices in tensor analysis, and {ref}`sec-tensor-19` for the Minkowski metric in special relativity. Notice that in {eq}`eq-kleing-14` we have $x^0 = x_0 = ct$, so that all four components of $x^\mu$ or $x_\mu$ have dimensions of distance. The derivative operators (a “space-time gradient”) associated with $x^\mu$ and $x_\mu$ are

:::{math}
:label: eq-kleing-16
\partial_\mu = \pop{}{x^\mu} =\begin{pmatrix} {\ds\pop{}{\ds(ct)}} \\  \del \\\end{pmatrix}, \qquad \partial^\mu = \pop{}{x_\mu}= \begin{pmatrix} {\ds\pop{}{\ds(ct)}} \\  -\del \\\end{pmatrix}.
:::

Notice that the positions of the indices on the operators $\partial_\mu$ and $\partial^\mu$ are opposite ($x^\mu$ and $x_\mu$, respectively) of the spatial coordinates in the denominator of the derivative. This is because if $x^\mu$ transforms as a contravariant vector, then $\partial_\mu = \partial/\partial x^\mu$ transforms as a covariant vector.

In this notation the d'Alembertian operator can be written,

:::{math}
:label: eq-kleing-17
\dAlembertian = \partial_\mu \partial^\mu = {1\over c^2} {\partial^2 \over \partial t^2} - \del^2,
:::

so that the Klein-Gordon equation {eq}`eq-kleing-8` becomes

:::{math}
:label: eq-kleing-18
\partial^\mu \partial_\mu \,\psi = -\Bigl({mc \over \hbar}\Bigr)^2\psi.
:::

This is one covariant version of the Klein-Gordon equation.

The energy-momentum 4-vector in special relativity is

:::{math}
:label: eq-kleing-19
p^\mu = \begin{pmatrix}E/c \\ \pvec \\\end{pmatrix}, \qquad p_\mu = \begin{pmatrix}E/c \\ -\pvec \\\end{pmatrix},
:::

in both contravariant and covariant versions. This is the classical energy-momentum 4-vector, but we can convert it into operators by the associations, $E \to i\hbar \partial/\partial t$, $\pvec \to -i\hbar\del$,

:::{math}
:label: eq-kleing-20
\begin{aligned}
p^\mu = \begin{pmatrix} E/c \\ \pvec \\\to \phat^\mu = i\hbar\partial^\mu = i\hbar\pop{}{x_\mu} = \begin{pmatrix}{\ds i\hbar \pop{}{\ds (ct)}} \\  -i\hbar\del \\, \\  p_\mu = \begin{pmatrix} E/c \\ -\pvec \\ \to \phat_\mu = i\hbar\partial_\mu = i\hbar\pop{}{x^\mu} =\begin{pmatrix}{\ds i\hbar\pop{}{\ds (ct)}} \\  i\hbar\del\\, \\ 

\end{pmatrix}
\end{pmatrix}
\end{pmatrix}
\end{pmatrix}
\end{aligned}
:::

where the arrow shows the transition from the classical object to the operator acting on wave functions and where the hat is used to distinguish the operator from the $c$-number or classical quantity. These are covariant versions of the Einstein-de~Broglie-Schr\"odinger relations connecting energy and momentum with operators.

We can rewrite the Klein-Gordon equation {eq}`eq-kleing-18` in terms of the covariant, 4-momentum operators $\phat^\mu$. We find

:::{math}
:label: eq-kleing-21
(\phat^\mu \phat_\mu - m^2c^2)\psi = 0,
:::

which is seen as an encoding of the classical, relativistic relation,

:::{math}
:label: eq-kleing-22
p^\mu p_\mu = {E^2\over c^2} - \pvec^2 = m^2c^2,
:::

in terms of operators. {eq}`eq-kleing-21` is another covariant version of the Klein-Gordon equation.

(sec-kleing-6)=

## Probability Density and Current

An essential part of the physical interpretation of the nonrelativistic Schr\"odinger equation is the conserved probability density and current. See {ref}`sec-tevolut-14`. For Hamiltonians of the kinetic-plus-potential form, these are

:::{math}
:label: eq-kleing-23
\rho = \psi^\cc\psi, \qquad \Jvec = \Re (\psi^\cc \vvec \psi) = -{i\hbar\over 2m} [\psi^\cc \del\psi - (\del\psi^\cc) \psi],
:::

where $\vvec=\pvec/m=-i\hbar\del/m$ is the velocity operator. To say that $\rho$ and $\Jvec$ are “conserved” means that they satisfy the continuity equation,

:::{math}
:label: eq-kleing-24
\frac{\partial \rho}{\partial t} + \del\cdot\Jvec=0.
:::

Sometimes the continuity equation can be put into covariant form. If we write

:::{math}
:label: eq-kleing-25
J^\mu = \begin{pmatrix}c\rho \\ \Jvec \\\end{pmatrix},
:::

then the continuity equation can be written

:::{math}
:label: eq-kleing-26
\partial_\mu J^\mu = \frac{\partial J^\mu}{\partial x^\mu} = \frac{\partial \rho}{\partial t} + \del\cdot\Jvec =0.
:::

It says that the 4-divergence of the 4-current vanishes.

We should not, however, use such notation for the Schr\"odinger $\rho$ and $\Jvec$, given by {eq}`eq-kleing-23`. To obtain a 4-vector it is not sufficient to write down four quantities and attach a Greek index; instead it is necessary to show that the four quantities transform as a 4-vector under Lorentz transformations. The Schr\"odinger $\rho$ and $\Jvec$ in {eq}`eq-kleing-23` certainly do not do this, since the Schr\"odinger equation is nonrelativistic equation that is not covariant under Lorentz transformations. It is possible to specify how the Schr\"odinger wave function transforms from one frame to another, but it is an implementation of a Galilean transformation, not a Lorentz transformation.

The Klein-Gordon equation also possesses a conserved density and current, one that is covariant. It is given by

:::{math}
:label: eq-kleing-27
J^\mu = {i\hbar\over 2m}[\psi^\cc (\partial^\mu \psi) - (\partial^\mu \psi^\cc)\psi]= {1\over m} \Re[\psi^\cc (i\hbar\,\partial^\mu)\psi],
:::

which can be seen as a space-time generalization of the spatial vector $\Jvec$ of the Schr\"odinger theory, shown in {eq}`eq-kleing-23`. To show that this is conserved we take the 4-divergence,

:::{math}
:label: eq-kleing-28
\partial_\mu J^\mu = {i\hbar\over 2m}[(\partial_\mu \psi^\cc)(\partial^\mu\psi) + \psi^\cc (\dAlembertian\psi) - (\dAlembertian\psi^\cc)\psi -(\partial^\mu\psi^\cc)(\partial_\mu\psi)].
:::

The first and fourth terms cancel, as do the second and third if we use the Klein-Gordon equation {eq}`eq-kleing-18` and its complex conjugate. Thus we obtain $\partial_\mu J^\mu=0$ for the Klein-Gordon current.

Moreover, the current $J^\mu$ transforms as a 4-vector under Lorentz transformations. This follows if we assume that the Klein-Gordon wave function $\psi(\xvec,t)$ transforms as a scalar under Lorentz transformations (the simplest transformation law possible). We have been implicitly assuming that the Klein-Gordon wave function $\psi$ is a scalar, in the sense of having only one component, what we would expect for the wave function of a spin-0 particle. In the nonrelativistic (Schr\"odinger) theory the wave function of a spin-0 particle is a scalar also in the sense that it has the same value when subjected to a spatial rotation. See Prob. {ref}`prob-jjcouple-1`(a), where the transformation properties of wave functions under rotations is explored. If we assume that the (scalar) Klein-Gordon wave function $\psi$ is a scalar under all Lorentz transformations (not just spatial rotations), then its space-time gradient $\partial^\mu\psi$ transforms as a 4-vector. Thus, $J^\mu$, defined by {eq}`eq-kleing-28`, also transforms as a 4-vector.

(sec-kleing-7)=

## Difficulties with the Klein-Gordon Equation

Unfortunately, the density associated with the time component of the current,

:::{math}
:label: eq-kleing-29
\rho = {1\over c} J^0 = {i\hbar\over 2mc^2} \Bigl[\psi^\cc \frac{\partial \psi}{\partial t} - \frac{\partial \psi^\cc}{\partial t} \, \psi \Bigr],
:::

is not positive definite, as we require of a probability density. That is, the Klein-Gordon equation seems to lead to “negative probabilities.” We will not analyze this difficulty further, except to remark that it can be seen to be related to the fact that the Klein-Gordon equation is second order in time, which in turn is due to Schr\"odinger's squaring of the energy momentum relation. One can also see that the negative probabilities are related to the existence of negative-energy solutions.

We have identified two difficulties with the Klein-Gordon equation: the existence of negative energy solutions, for which we have no physical interpretation, and the lack of positive definite probability density. For these and other reasons, the Klein-Gordon equation was regarded as unsatisfactory in the years immediately after its introduction. It has since been rehabilitated, and is now considered a respectable wave equation describing relativistic particles of spin-0, such as $\pi$-mesons. But this involves some considerable reinterpretation of its meaning, which will take us some time to appreciate.

Schr\"odinger, who first wrote down the Klein-Gordon equation, could not make sense of it, and never published it. After setting it aside for a period of time, as an afterthought he returned to it, deciding just to try his ideas on the nonrelativistic version, that is, starting with the nonrelativistic energy-momentum relation,

:::{math}
:label: eq-kleing-30
E = {\pvec^2\over 2m}.
:::

This led to what we now usually call the Schr\"odinger equation for a free particle,

:::{math}
:label: eq-kleing-31
i\hbar\frac{\partial \psi}{\partial t} = -{\hbar^2 \over 2m} \del^2 \psi.
:::

Incorporating also a potential energy into this description, Schr\"odinger quickly solved a series of problems ranging from the hydrogen atom to the harmonic oscillator and several others. He also showed the equivalence of his new “wave mechanics” with the matrix mechanics of Heisenberg, that had been introduced the previous year. He published these results in a series of papers in 1926. Somewhat later, Klein and Gordon decided to try Schr\"odinger's ideas on a relativistic particle, and rediscovered the equation that now bears their names.
