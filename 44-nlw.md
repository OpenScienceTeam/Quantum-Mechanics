---
title: "44. Natural Line Width, Long-Time Behavior and the Lamb Shift"
---
(ch-nlw)=

# 44. Natural Line Width, Long-Time Behavior and the Lamb Shift

(sec-nlw-1)=

## Introduction

Let us return to the Kramers-Heisenberg formula. For simplicity we consider the case of elastic scattering, $A+\gamma \to A+\gamma'$, in which the state $A$ is the ground state. The cross is

:::{math}
:label: eq-nlw-1
\dod{\sigma}{\Omega'} = r_e^2 |M|^2,
:::

where

:::{math}
:label: eq-nlw-2
M={\hat{\boldsymbol{\epsilon}}}\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc} + {1\over m\hbar}\sum_{I\ne A} \left[ {\matrixelement{A}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A} \over \omega-\omega_{IA}} - {\matrixelement{A}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{A} \over \omega+\omega_{IA}}\right],
:::

which are {eq}`eq-photscatt-43` and {eq}`eq-photscatt-44`. The first term under the sum, which corresponds to the Feynman diagram in {ref}`fig-nlw-1`, is resonant when $\omega=\omega_{IA}$ for some intermediate state $I$, that is, the denominator goes to zero at this frequency and the cross nominally becomes infinite. Note that there is a sum over intermediate states $I\ne A$, so states $I$ must be excited states, and when $\omega=\omega_{IA}$ it means that the incident photon has the right energy to lift the system into the excited state $I$. Only one state $I$ (or a collection of degenerate states) can be resonant for a given incident photon frequency $\omega$; when $\omega$ is near $\omega_{IA}$ for some intermediate state $I$, then that one term in the sum in the Kramers-Heisenberg formula dominates and we can approximate the amplitude by neglecting the others.

:::{figure} images/nlw-fig01.png
:label: fig-nlw-1
:width: 80%

Feynman diagram for the first term under the sum in Eq. {eq}`eq-nlw-2`, which is resonant when $\omega=\omega_{IA}$ for some intermediate state $I$. At resonance, energy is conserved at the lower vertex (circled).
:::

The resonant divergence of the scattering cross is nonphysical, so a number of questions are raised. First, what is wrong with our derivation of the Kramers-Heisenberg formula, that we obtain non-physical divergences, and how do we correct them? Next, how close to $\omega=\omega_{IA}$ can we come before the Kramers-Heisenberg formula {eq}`eq-photscatt-44` breaks down? And finally, since we know the cross cannot really be infinite at resonance $\omega=\omega_{IA}$, how high does it go? Recall that for non-resonant frequencies, that is, $\omega$ that are not close to $\omega_{IA}$ for any intermediate state $I$, the Kramers-Heisenberg cross is of order $r_e^2 = \alpha^4 a_0^2$. That is, it is of order $\alpha^4\sim 10^{-9}$ in atomic units, which is very small by atomic standards. It is of interest to see by what factor this small cross is enhanced at resonance.

To see some of the qualitative features of the divergences in the Kramers-Heisenberg formula, consider the Feynman diagram of {ref}`fig-nlw-1`. A question that arises is whether energy is conserved at the vertices of the diagram, for example, at the lower vertex (circled), where the energy of the initial state is $E_A+\hbar\omega$ and that of the intermediate state is $E_I$. The answer depends on the photon energy $\hbar\omega$ but for most values of this parameter energy is not conserved. There is no reason why it should be, since the intermediate states originate in a resolution of the identity, which is a sum over all states, regardless of their energy. Nevertheless, the Feynman diagram suggests that somehow the initial state is transformed into the intermediate state at a certain time, which later transforms into the final state. In quantum mechanics energy is only precisely defined in processes that take an infinite amount of time, while for a process that takes time $\Delta t$ the energy is uncertain by an amount $\Delta E \sim \hbar/\Delta t$. In fact, intermediate states in Feynman diagrams only survive for a limited amount of time, or at least this is an interpretation that can be given to the machinery of the Dyson series developed in {ref}`ch-tdpt`. Such a state is called *virtual*. For the lower vertex of the Feynman diagram in question, note that $\Delta E= E_I-E_A-\hbar\omega$, so that $\Delta E$ is proportional to the resonant denominator we see in the Kramers-Heisenberg formula. The whole amplitude is proportional to $1/\Delta E$, that is, it is proportional to the amount of time that the intermediate state is allowed to survive.

If $\omega$ is not near any resonant frequency $\omega_{IA}$ for any intermediate state $I$, then $\Delta E$ is of order unity in atomic units, so any given intermediate state $I$ survives only for a time of order unity before disappearing again. This means that the contribution of the state $I$ to the transition amplitude, which is computed in the Dyson series as an integral over time, can only accumulate to a small value before the virtual state disappears. The time integral in question is the one over $t''$ in {eq}`eq-tdpt-34`; the integrand has the phase factor $e^{i\omega_{ki}t''}$, which in the context of the Kramers-Heisenberg formula is

:::{math}
:label: eq-nlw-3
e^{i(E_I-E_A-\hbar\omega)t''/\hbar} =e^{i\Delta E t''/\hbar}.
:::

If $\omega$ is not resonant, then the contribution to the transition amplitude just oscillates with a frequency $\Delta E/\hbar$ and remains small.

If however we let $\omega$ approach a resonant frequency $\omega_{IA}$ for some intermediate state $I$, then $\Delta E$ gets smaller, the virtual state lives for a longer time, and the transition amplitude accumulates. This is reflected by the fact that the denominator gets smaller. As $\Delta E\to 0$, it would appear that the virtual state could live for an arbitrarily long time, which would mean that it is becoming a real state.

But the intermediate state $I$ in question must be an excited state, since we are assuming that $A$ is the ground state, so it cannot live forever, rather it will eventually undergo the spontaneous emission of a photon and drop into a lower state. This will become a significant process when $\Delta E$ is comparable to $\Gamma=\hbar/\tau$, where $\tau$ is the lifetime of the excited state $I$. $\Gamma$ is the usual symbol used for the decay rate of an excited state, measured in energy units. Thus we can expect that the predictions of the Dyson series and the Kramers-Heisenberg formula, as derived in {ref}`ch-photscatt`, will break down when

:::{math}
:label: eq-nlw-4
|\Delta E| = |E_I-E_A-\hbar\omega| <\approx \Gamma.
:::

As explained in {ref}`ch-radnmatt`, for E1 transitions $\Gamma$ is of order $\alpha^3 \sim 10^{-6}$ in atomic units, so the fraction of the $\omega$ axis over which the breakdown occurs is very small. For M1 and higher order transitions $\Gamma$ is even smaller. In other applications (nuclear physics, particle physics) $\Gamma$ may be relatively much larger (that is, broad resonances exist).

Time-dependent perturbation theory, as we have presented it in {ref}`ch-tdpt`, is based on the method of successive approximations, in which a lower order approximation is substituted back into the Schr\"odinger equation in the interaction picture and integrated to get the next approximation. It does not take into account the depletion of probability from the initial state due to the perturbation, so its validity is limited to short times, that is, $t\ll \hbar/\Gamma$. To cure the divergences in the Kramers-Heisenberg formula we need a theory capable of handling the long-time behavior of the system, that is, one that is valid for times $t>\approx \hbar/\Gamma$.

(sec-nlw-2)=

## Decay of an Excited State; the Decay Rate $\Gamma$

To analyze the long-time behavior of quantum systems, we will take a model problem, that of the decay of an atom in an excited state $B$. We outline the problem in this , which contains a slight rephrasing of some of the material given in {ref}`sec-radnmatt-3`. For the rest of this analysis we set $\hbar=1$ except that we restore $\hbar$'s selectively when it makes final formulas look more familiar.

:::{figure} images/nlw-fig02.png
:label: fig-nlw-2
:width: 80%

An atom in excited state $B$ emits a photon and drops into a lower state, of which there may be more than one ($A$, $A'$, etc).
:::

We assume the atom is initially in an excited state $B$ with no photons in the field, and that it subsequently makes a transition to a lower state $A$ with the emission of a photon. There may be more than one lower energy state to which a transition can be made, $A'$, $A''$, etc., as illustrated in {ref}`fig-nlw-2`. As in {ref}`ch-radnmatt`{} we let the initial state be $\ket{B0}=\ket{B}\ket{0}$, where $\ket{0}$ is the vacuum state of the field, and we let the final state be $\ket{A\lambda}=\ket{A}a_\lambda^\dagger\ket{0}$, that is, the state in which the atom is in state $\ket{A}$ and there is one photon in the field of mode $\lambda=(\kvec,\mu)$. We take the Hamiltonian to be

:::{math}
:label: eq-nlw-5
K=K_0 + K_1 + K_2 = K_0+K',
:::

where $K_0$, $K_1$ and $K_2$ are given by {eq}`eq-photscatt-5a` and where we set $K'=K_1+K_2$ as it is convenient to have a symbol for the entire perturbation.

According to first-order time-dependent perturbation theory, the transition amplitude in the interaction picture to find the system in state $\ket{A\lambda}$ at time $t$ is

:::{math}
:label: eq-nlw-6
c_{A\lambda}(t) = -2i\, e^{i\omega_{ni}t/2}\, {\sin(\omega_{ni}t/2)\over \omega_{ni}}\, \matrixelement{A\lambda}{K'}{B0},
:::

where $\omega_{ni}$ is interpreted as

:::{math}
:label: eq-nlw-7
\omega_{ni} = {E_B - E_A -\hbar\omega \over \hbar} = \omega_{BA}-\omega.
:::

See {eq}`eq-tdpt-36` and {eq}`eq-radnmatt-10`. We note that $K_1$ can only change the number of photons by $\pm1$ while $K_2$ can change them only by 0 or $\pm2$, so $K'$ in {eq}`eq-nlw-6` can be replaced by $K_1$.

Squaring the transition amplitude to get a probability we have

:::{math}
:label: eq-nlw-8
P_{A\lambda}(t) = 2\pi t \,\Delta_t(\omega_{BA}-\omega) \,|\matrixelement{A\lambda}{K_1}{B0}|^2,
:::

where $\Delta_t$ is the usual symbol we have used for an approximate $\delta$-function, as defined by {eq}`eq-tdpt-46`. Dividing this by $t$ and summing over final states gives us the transition rate, according to first-order time-dependent perturbation theory. If we want the total rate of decay, we must sum not only over all photon states $\lambda$ but all atomic states $A$. This gives

:::{math}
:label: eq-nlw-9
\Gamma = 2\pi \sum_{A\lambda} |\matrixelement{A\lambda}{K_1}{B0}|^2 \, \delta(\omega_{BA}-\omega),
:::

where we have taken $t$ long enough to replace the function $\Delta_t$ by a genuine $\delta$-function. There is no harm in summing over all states $A$, including those higher in energy than $B$, since for those the $\delta$-function will give zero.

A $\delta$-function is only meaningful under an integral, so when interpreting formulas such as {eq}`eq-nlw-9` it must be understood that the sum on photon modes $\lambda$ includes a sum on wavevectors $\kvec$ of the photon, which in the infinite volume limit can be written as an integral over the frequency $\omega$ of the photon,

:::{math}
:label: eq-nlw-10
\sum_{\kvec} \to {V\over (2\pi)^3} \int d\Omega_k {1\over c^3} \int_0^\infty \omega^2 \, d\omega.
:::

The volume factor $V$ will cancel when we compute the matrix element.

As noted in {ref}`ch-radnmatt`, this calculation of the decay rate really gives the slope of the decay curve at $t=0$. See Fig.~\figr\radnmatt.1, in which the decay rate is denoted $A_E$ (the Einstein $A$-coefficient) rather than $\Gamma$. (The notation $A_E$ is appropriate for the decay rate to a specific final state, while $\Gamma$ is the decay rate to all possible final states.) First-order time-dependent perturbation theory is giving the probability of remaining in the initial state $\ket{B0}$ as

:::{math}
:label: eq-nlw-11
P_{B0}(t) = 1-\Gamma t,
:::

which is correct for $t\ll 1/\Gamma$ but absurd for longer times. For longer times we might expect an exponential decay law $P_{B0}(t) = e^{-\Gamma t}$ but that is not proven by first-order time-dependent perturbation theory. We *do* have the first term in the Taylor expansion of the exponential,

:::{math}
:label: eq-nlw-12
e^{-\Gamma t} = 1-\Gamma t + \ldots,
:::

but we haven't proven that the higher order terms are the right ones.

To access the long-time behavior of the system it won't help to go to higher order in time-dependent perturbation theory. These higher order terms will generate powers of $t$, that is, a Taylor series expansion of the probability in time about $t=0$. This is a poor way to understand the long-time behavior.

(sec-nlw-3)=

## An Approach Based on Laplace Transforms and Green's Functions

Let us return to the formalism of time-dependent perturbation theory in the general notation used in {ref}`ch-tdpt`. We write the Hamiltonian as $H=H_0+H_1$, and we let the initial state be

:::{math}
:label: eq-nlw-13
\ket{\psi(0)}=\ket{i},
:::

where $\ket{i}$ is an eigenstate of $H_0$,

:::{math}
:label: eq-nlw-14
H_0 \ket{i} = E_i \ket{i}.
:::

The state of the system at a later time is

:::{math}
:label: eq-nlw-15
\ket{\psi(t)} = U(t)\ket{i} = \sum_n a_n(t) \ket{n},
:::

where we have expanded $\ket{\psi(t)}$ as a linear combination of eigenstates of $H_0$, $H_0\ket{n} = E_n\ket{n}$, for simplicity assumed to be discrete. The expansion coefficients $a_n(t)$ are the transition amplitudes in the Schr\"odinger picture,

:::{math}
:label: eq-nlw-16
a_n(t) = \matrixelement{n}{U(t)}{i}.
:::

In this analysis we will work in the Schr\"odinger picture, but for reference the transition amplitudes in the interaction picture, which we denote by $c_n(t)$ as in {ref}`ch-tdpt`, are related to those of the Schr\"odinger picture by

:::{math}
:label: eq-nlw-17
c_n(t) = e^{iE_n t}\,a_n(t).
:::

See {eq}`eq-tdpt-28`. The two amplitudes differ by a phase factor, so the transition probability, which is the square of the amplitudes, is the same in both pictures. Differentiating {eq}`eq-nlw-16` with respect to time we obtain an evolution equation for the transition amplitudes in the Schr\"odinger picture,

:::{math}
:label: eq-nlw-18
i{\dot a}_n = \matrixelement{n}{i\frac{\partial U}{\partial t}}{i} = \matrixelement{n}{(H_0+H_1)U(t)}{i},
:::

or,

:::{math}
:label: eq-nlw-19
i{\dot a}_n = E_n a_n + \sum_k \matrixelement{n}{H_1}{k} a_k.
:::

This is really just a version of the Schr\"odinger equation and it is exact.

We will solve {eq}`eq-nlw-19` by means of Laplace transforms. A Laplace transform is essentially a one-sided Fourier transform, that is, the range of integration only goes from 0 to $\infty$ instead of $-\infty$ to $+\infty$. (In comparison to the usual definition of the Laplace transform there is also the question of a deformation of the contour of integration in the complex plane, which we gloss over, the main point being that we will be using a one-sided Fourier transform.) The one-sided transform is necessary in our applications since we are interested in decay processes that go to zero as $t\to\infty$ but which diverge as $t\to-\infty$ (and in any case we are only interested in $t\ge 0$). The variable conjugate to $t$ is an energy-like variable, so we want to consider transforms like

:::{math}
:label: eq-nlw-20
\int_0^\infty dt \, e^{iEt} \, a_n(t) = \int_0^\infty dt \, e^{iEt} \, \matrixelement{n}{U(t)}{i}.
:::

The essence of this integral is

:::{math}
:label: eq-nlw-21
\int_0^\infty dt \, e^{iEt}\, U(t).
:::

However, as discussed in {ref}`sec-greensfuns-12`, this integral does not converge at the upper limit. To fix this we push $E$ into the upper half complex energy plane, making the replacement $E\to z=E+i\epsilon$, where $z$ is a complex energy. Then the integral {eq}`eq-nlw-21` gives the Green's operator, to within constant factors. To get these right, we define the “Laplace transform” for our purposes as the integral operator

:::{math}
:label: eq-nlw-22
-i \int_0^\infty dt \, e^{izt},
:::

for $\Im z>0$. Then we have

:::{math}
:label: eq-nlw-23
-i\int_0^\infty dt \, e^{izt}\, a_n(t) = -i\int_0^\infty dt \, e^{izt} \, \matrixelement{n}{U(t)}{i} = \matrixelement{n}{G(z)}{i} = {\tilde a}_n(z),
:::

where $G(z)$ is the Green's operator as defined by {eq}`eq-greensfuns-58` (with $\hbar=1$), and where we denote the Laplace transform of $a_n(t)$ by ${\tilde a}_n(z)$.

The advantage of Laplace transforms is that they convert differential equations into algebraic equations, which are easier to solve, and they also deal nicely with initial conditions and transients. This is like the method of complex impedances when analyzing an electrical circuit, which is much easier than solving coupled differential equations for the currents and charges in the circuit elements.

Applying the Laplace transform to the left-hand side of the Schr\"odinger equation {eq}`eq-nlw-19` and integrating by parts we obtain

:::{math}
:label: eq-nlw-24
-i\int_0^\infty dt\,e^{izt} \, i{\dot a}_n(t) = \left. e^{izt}\,a_n(t)\right|_0^\infty -iz\int_0^\infty dt \, e^{izt}\, a_n(t) = -a_n(0)+ z{\tilde a}_n(z).
:::

Note that $a_n(0)=\delta_{ni}$. Applying the Laplace transform also to the right-hand side of {eq}`eq-nlw-19` we obtain

:::{math}
:label: eq-nlw-25
(z-E_n) {\tilde a}_n(z) = \delta_{ni} + \sum_k \matrixelement{n}{H_1}{k} {\tilde a}_k(z).
:::

This is an algebraic equation for the Laplace transforms of the transition amplitudes that is equivalent to the Schr\"odinger equation and is still exact.

We can obtain the same result by noting that

:::{math}
:label: eq-nlw-26
G(z) = {1\over z-H} = {1\over z-H_0-H_1},
:::

so that

:::{math}
:label: eq-nlw-27
(z-H_0-H_1)G(z) = 1.
:::

Now sandwiching this by $\bra{n}$ on the left and $\ket{i}$ on the right, we obtain

:::{math}
:label: eq-nlw-28
\matrixelement{n}{(z-H_0-H_1)G(z)}{i} = (z-E_n){\tilde a}_n(z) - \sum_k \matrixelement{n}{H_1}{k} {\tilde a}_k(z) = \delta_{ni},
:::

which is the same as {eq}`eq-nlw-25`.

(sec-nlw-4)=

## Solving for the Transition Amplitudes

We now apply these results to the decay problem described in \secrnlw-2, making the identifications $\ket{i}\to\ket{B0}$, $E_i = E_B$, $H_0=K_0$, and $H_1=K'=K_1+K_2$. Also, we make the approximation of working on the subspace of the ket space spanned by $\ket{B0}$ and $\ket{A\lambda}$, ignoring all states with two or more photons. This means that we interpret the resolution of the identity as

:::{math}
:label: eq-nlw-29
\sum_k \ketbra{k}{k} \to \ketbra{B0}{B0} + \sum_{A\lambda} \ketbra{A\lambda}{A\lambda}.
:::

We can enlarge this space to get a better approximation, at the expense of solving a more complicated system of equations.

We specialize {eq}`eq-nlw-25` to the case $n=i$, which for our decay problem means that the final state is the same as the initial state $\ket{B0}$. The corresponding amplitude is $a_{B0}(t)$, the amplitude to remain in the initial state. Making the replacement {eq}`eq-nlw-29` for this case we obtain

:::{math}
:label: eq-nlw-30
(z-E_B){\tilde a}_{B0}(z) = 1 + \matrixelement{B0}{K'}{B0}\,{\tilde a}_{B0}(z) + \sum_{A\lambda} \matrixelement{B0}{K'}{A\lambda}\, {\tilde a}_{A\lambda}(z).
:::

Taking into account the numbers of photons that $K_1$ and $K_2$ can create or destroy, we can write this as

:::{math}
:label: eq-nlw-31
(z-E_B){\tilde a}_{B0}(z) = 1 + \matrixelement{B0}{K_2}{B0}\,{\tilde a}_{B0}(z) + \sum_{A\lambda} \matrixelement{B0}{K_1}{A\lambda}\, {\tilde a}_{A\lambda}(z).
:::

Similarly, taking the case $n\ne i$ and identifying $\ket{n}$ with $\ket{A\lambda}$, so that $E_n=E_A+\omega$, we can write {eq}`eq-nlw-25` as

:::{math}
:label: eq-nlw-32
(z-E_A-\omega){\tilde a}_{A\lambda}(z) = \matrixelement{A\lambda}{K_1}{B0} \,{\tilde a}_{B0}(z) + \sum_{A'\lambda'} \matrixelement{A\lambda}{K_2}{A'\lambda'}\, {\tilde a}_{A'\lambda'}(z),
:::

where we have restricted the resolution of the identity as in {eq}`eq-nlw-29`.

Equations~{eq}`eq-nlw-31` and {eq}`eq-nlw-32` are algebraic equations for the Laplace transforms of the transition amplitudes, ${\tilde a}_{B0}(z)$ and ${\tilde a}_{A\lambda}(z)$. The various terms can be assigned an order in the perturbation $K_1+K_2$, where we count $K_2$ as of order $K_1^2$. The amplitude ${\tilde a}_{B0}(z)$ is of order unity in the perturbation, since it is non-zero even when $K_1=K_2=0$, as shown by {eq}`eq-nlw-31`. Then since the matrix element $\matrixelement{A\lambda}{K_1}{B0}$ is of order $K_1$, we see from {eq}`eq-nlw-32` that the amplitude ${\tilde a}_{A\lambda}(z)$ is also of order $K_1$. This also follows from the fact that transitions to the states $A\lambda$ are induced by $K_1$. From this it follows that the final term in {eq}`eq-nlw-32` is of order $K_1^3$. As for {eq}`eq-nlw-31`, its terms are of at most second order in $K_1$.

We will work to second order in the perturbation, neglecting the final, third order term in {eq}`eq-nlw-32` (the final sum). This allows us to solve for the amplitude ${\tilde a}_{A\lambda}(z)$ in terms of ${\tilde a}_{B0}(z)$,

:::{math}
:label: eq-nlw-33
{\tilde a}_{A\lambda}(z) = {\matrixelement{A\lambda}{K_1}{B0} \over z-E_A-\omega} \, {\tilde a}_{B0}(z).
:::

We substitute this back into {eq}`eq-nlw-31`, which allows us to solve for the amplitude ${\tilde a}_{B0}(z)$,

:::{math}
:label: eq-nlw-34
{\tilde a}_{B0}(z) = {1\over D(z)},
:::

where we define

:::{math}
:label: eq-nlw-35
D(z) = z-E_B - \matrixelement{B0}{K_2}{B0} - \sum_{A\lambda} {|\matrixelement{A\lambda}{K_1}{B0}|^2 \over z-E_A-\omega}.
:::

The symbol $D$ stands for “denominator.” Finally, we can substitute this back into {eq}`eq-nlw-33` to obtain

:::{math}
:label: eq-nlw-36
{\tilde a}_{A\lambda}(z) = {\matrixelement{A\lambda}{K_1}{B0}\over (z-E_A-\omega)D(z)}.
:::

Equations~{eq}`eq-nlw-34` and {eq}`eq-nlw-36` are explicit solutions for the Laplace transforms of the transition amplitudes $a_{B0}(t)$ and $a_{A\lambda}(t)$. We must now carry out the inverse Laplace transform to get the amplitudes themselves.

(sec-nlw-5)=

## Inverting the Laplace Transform

Let us revert to a general notation, denoting transition amplitudes by $a_n(t)$ and their Laplace transforms by ${\tilde a}_n(z)$. To carry out the inverse Laplace transform we consider the integral

:::{math}
:label: eq-nlw-37
{-1 \over 2\pi i} \int_{C_+} dz \, e^{-izt}\, {\tilde a}_n(z)= {-1 \over 2\pi i} \int_{C_+} dz \, e^{-izt}\, \matrixelement{n}{G(z)}{i},
:::

where $C_+$ is a contour that runs just above the real axis in the complex energy plane, as illustrated in {ref}`fig-nlw-3`. The essence of this integral is

:::{math}
:label: eq-nlw-38
{-1 \over 2\pi i} \int_{C_+} dz \, e^{-izt}\, G(z).
:::

If $t<0$ then the integrand is exponentially damped in the upper half plane, and the contour can be closed by a semicircle at infinity which does not contribute to the integral, as illustrated in {ref}`fig-nlw-4`. This contour encloses no singularities since $G(z)$ is analytic in the upper half plane, so the value of the integral is zero.

:::{figure} images/nlw-fig03.png
:label: fig-nlw-3
:width: 80%

The contour $C_+$, used in the inverse Laplace transfrom, runs just above the real energy axis.
:::

:::{figure} images/nlw-fig04.png
:label: fig-nlw-4
:width: 80%

For negative times $t<0$ the contour $C_+$ can be closed in the upper half-plane.
:::


For positive times $t>0$ the integrand diverges exponentially in the upper half-plane so we cannot close the contour there. Nor can we close it in the lower half-plane, since that would involve crossing the real energy axis where $G(z)$ has singularities (poles and branch cuts). To evaluate the integral {eq}`eq-nlw-38` for positive times we consider a different integral,

:::{math}
:label: eq-nlw-39
{-1 \over 2\pi i} \int_{C_-} dz \, e^{-izt}\, G(z),
:::

where $C_-$ runs just below the real energy axis, as illustrated in {ref}`fig-nlw-5`. For positive times $t>0$ the integrand damps exponentially in the lower half-plane, so the contour can be closed as in {ref}`fig-nlw-6`. But since $G(z)$ is also analytic in the lower half-plane, the integral {eq}`eq-nlw-39` vanishes for $t>0$.

:::{figure} images/nlw-fig05.png
:label: fig-nlw-5
:width: 80%

The contour $C_-$ runs just below the real energy axis.
:::

:::{figure} images/nlw-fig06.png
:label: fig-nlw-6
:width: 80%

For positive times $t>0$ the contour $C_-$ can be closed in the lower half-plane.
:::


To return to the integral {eq}`eq-nlw-38` for positive times, we can subtract the integral {eq}`eq-nlw-39` without changing the value since the latter is zero. That is, for $t>0$ we have

:::{math}
:label: eq-nlw-40
\begin{aligned}
{-1 \over 2\pi i} \int_{C_+} dz \, e^{-izt}\, G(z)&= {-1 \over 2\pi i} \int_{C_+-C_-} dz \, e^{-izt}\, G(z) \\
&={-1 \over 2\pi i} \int_{-\infty}^{+\infty} dE \, e^{-iEt}\, \lim_{\epsilon\to0} [G(E+i\epsilon)-G(E-i\epsilon)], \\

\end{aligned}
:::

where as the contours $C_+$ and $C_-$ are pushed toward the real axis we get an integral running over the real axis itself, in which the integrand contains the difference in $G(z)$ just above and just below the real axis. But this is the discontinuity in the Green's operator across the real axis, which is $-2\pi i\,\delta(E-H)$. See {eq}`eq-greensfuns-72` and {eq}`eq-greensfuns-76`. Thus the integral {eq}`eq-nlw-40` becomes

:::{math}
:label: eq-nlw-41
\int_{-\infty}^{+\infty} dE \, e^{-iEt} \, \delta(E-H) = e^{-iHt} = U(t).
:::

Altogether, we have

:::{math}
:label: eq-nlw-42
\begin{aligned}
{-1 \over 2\pi i} \int_{C_+} dz \, e^{-izt}\, G(z) = \begin{cases} 0 & t<0, \\  U(t) & t>0,\\\end{cases}
\end{aligned}

:::

and the inverse Laplace transform of the transition amplitude is

:::{math}
:label: eq-nlw-43
a_n(t) = {-1\over 2\pi i} \int_{C_+} dz \, e^{-izt} \, {\tilde a}_n(z), \qquad \\text{t>0}.
:::

(sec-nlw-6)=

## Transition Amplitude $a_{B0}(t)$ in the Unperturbed System

Now we apply the inverse Laplace transform to the amplitudes ${\tilde a}_{B0}(z)$ and ${\tilde a}_{A\lambda}(z)$, given by {eq}`eq-nlw-34` and {eq}`eq-nlw-36`. We start with the amplitude to remain in the initial state $\ket{B0}$,

:::{math}
:label: eq-nlw-44
a_{B0}(t) = {-1\over 2\pi i} \int_{C_+} dz \, {e^{-izt} \over D(z)}.
:::

Before doing this in full detail, let us neglect the terms of $D(z)$ seen in {eq}`eq-nlw-35` that involve the perturbing Hamiltonians $K_1$ and $K_2$, in order to see the evolution due to the unperturbed system. We do this to gain some experience and confidence with the formalism.

:::{figure} images/nlw-fig07.png
:label: fig-nlw-7
:width: 80%

Complex plane for the inverse Laplace transform for the unperturbed approximation to $a_{B0}(t)$. The integrand has a simple pole on the real axis at $z=E_B$.
:::

:::{figure} images/nlw-fig08.png
:label: fig-nlw-8
:width: 80%

The contour of {ref}`fig-nlw-7` can be closed in the lower half-plane and contracted around the pole.
:::


In that case $D(z)$ becomes simply $z-E_B$, and we have

:::{math}
:label: eq-nlw-45
a_{B0}(t) = {-1\over 2\pi i} \int_{C_+} dz \, {e^{-izt} \over z-E_B}.
:::

The integrand has a pole on the real axis at $z=E_B$ and no other singularities. For $t>0$ the contour $C_+$ can be closed with a semicircle in the lower half-plane and can then be contracted into a small circle running in the clockwise (negative) direction around the pole. See Figs.~{ref}`fig-nlw-7` and {ref}`fig-nlw-8`. Then by the residue theorem we have

:::{math}
:label: eq-nlw-46
a_{B0}(t) = e^{-iE_B t},
:::

which is exactly the time evolution we expect for the amplitude to remain in the initial state when there is no perturbation. We see that the time dependence of the amplitude depends on the location of the poles of the integrand of the inverse Laplace transform.

(sec-nlw-7)=

## Denominator $D(z)$ on the Real Axis

To handle the full expression {eq}`eq-nlw-35` for $D(z)$ let us first set $z=E+i\epsilon$ for a point on the contour $C_+$,

:::{math}
:label: eq-nlw-47
D(E+i\epsilon) = E+i\epsilon -\matrixelement{B0}{K_2}{B0} + \sum_{A\lambda} {|\matrixelement{A\lambda}{K_1}{B0}|^2 \over E_A+\omega - E - i\epsilon},
:::

where we have changed the sign of the denominator of the last term and compensated with the overall sign of that term. We remember that $\sum_\lambda$ actually implies the integral {eq}`eq-nlw-10` over $\omega$.

We want to let $\epsilon\to0$ in this expression to get $D(z)$ on the real axis, but the final term is tricky. It looks like we could just set $\epsilon=0$ in this term and we would obtain a quantity that was purely real, but this is incorrect. In fact, if we just set $\epsilon=0$ we get an integral that has the mathematical form

:::{math}
:label: eq-nlw-48
\int_a^b dx \, {f(x) \over x-x_0},
:::

where $f(x)$ is a smooth function and where the interval $[a,b]$ straddles the singularity at $x_0$. (The variable $x$ in the integral {eq}`eq-nlw-48` is like $\omega$ in the integral {eq}`eq-nlw-47`.) The problem is that the integral {eq}`eq-nlw-48` is not defined. The part of the integral from $x=a$ to $x=x_0$ diverges with one sign and the part from $x=x_0$ to $x=b$ diverges with the opposite sign. Thus the integral has the form $\infty-\infty$, and is not defined.

We cannot just set $\epsilon=0$ in an expression like {eq}`eq-nlw-47`, instead we must take the limit $\epsilon\to0$. That is, we have something of the form

:::{math}
:label: eq-nlw-49
\lim_{\epsilon\to0} \int_a^b dx\, {f(x) \over x-x_0 -i\epsilon}.
:::

Assuming $f$ is real, the real and imaginary parts of this integrand are obtained from

:::{math}
:label: eq-nlw-50
{1\over x-x_0-i\epsilon} = {x-x_0 \over (x-x_0)^2 + \epsilon^2} + {i\epsilon \over (x-x_0)^2 + \epsilon^2}.
:::

As for the imaginary part, as $\epsilon\to0$ we get a representation of the $\delta$-function,

:::{math}
:label: eq-nlw-51
\lim_{\epsilon\to0} {\epsilon \over (x-x_0)^2 + \epsilon^2} = \pi\,\delta(x-x_0),
:::

so the imaginary part of the final sum in {eq}`eq-nlw-47` is nonzero as $\epsilon\to0$ and is given by

:::{math}
:label: eq-nlw-52
\pi\sum_{A\lambda}|\matrixelement{A\lambda}{K_1}{B0}|^2 \, \delta(E_A + \omega -E).
:::

A bare formula like {eq}`eq-nlw-51` is not meaningful if interpreted as the limit of a function, since the so-called “$\delta$-function” is not a real function. It does not make sense to say that the $\delta$-function is zero everywhere except at one point where it is infinite, and that its integral is unity. Instead a formula like {eq}`eq-nlw-49` must be understood as being used under an integral sign, in which the left-hand side is integrated against a smooth function $f(x)$ and the limit is taken. The “$\delta$-function” is an example of what is called a *distribution*, something that can be regarded as the limit of a family of functions used under an integral.

There are other distributions besides the $\delta$-function, in fact, the real part of {eq}`eq-nlw-50` is another example which is denoted

:::{math}
:label: eq-nlw-53
P\Bigl({1\over x-x_0}\Bigr)=\lim_{\epsilon\to0} {x-x_0 \over (x-x_0)^2 + \epsilon^2}.
:::

This is called the “principal value” of $1/(x-x_0)$. This equation is a “bare” formula like {eq}`eq-nlw-51`. Its real meaning is

:::{math}
:label: eq-nlw-54
P\int dx\, {f(x)\over x-x_0} = \lim_{\epsilon\to0} \int dx\, {x-x_0 \over (x-x_0)^2 + \epsilon^2}\, f(x).
:::

Without the $P$ the left-hand side of this equation would not be defined, as explained above.

Now we can take the limit $\epsilon\to0$ to push $D(z)$ down onto the real axis. We write

:::{math}
:label: eq-nlw-55
D(E) = \lim_{\epsilon\to0} D(E+i\epsilon) = E - E_B - \matrixelement{B0}{K_2}{B0} +f_1(E) + if_2(E),
:::

where

:::{math}
:label: eq-nlw-56
f_1(E)=P\sum_{A\lambda} {|\matrixelement{A\lambda}{K_1}{B0}|^2 \over E_A+\omega-E}, \qquad f_2(E)= \pi \sum_{A\lambda} |\matrixelement{A\lambda}{K_1}{B0}|^2 \, \delta(E_A+\omega-E).
:::

(sec-nlw-8)=

## The Zero of $D(z)$ and the Complex Energy of State $B$

The zero of $D(z)$ is the pole of the integrand of the inverse Laplace transform {eq}`eq-nlw-44` and is important for evaluating that integral. It also turns out to be a kind of complex energy of the state $B$, once the perturbation is turned on. In the unperturbed system $D(z)$ has a zero on the real axis at $z=E_B$ but when the perturbation is turned on $D(E)$ is nonzero everywhere on the real axis because the imaginary part is positive there. Thus the zero must have moved to some complex location nearby. We denote the zero by $z_B$, so that $D(z_B)=0$. We write $z_B=E_B+\delta z$ so that $\delta z$ is the shift in the zero of $D(z)$ due to the perturbation. To find $\delta z$ we write

:::{math}
:label: eq-nlw-57
D(z_B) = D(E_B +\delta z) = \delta z -\matrixelement{B0}{K_2}{B0} +f_1(E_B+\delta z) + if_2(E_B+\delta z)=0.
:::

Assuming $\delta z$ is small we neglect it in the last two terms which are already small, finding

:::{math}
:label: eq-nlw-58
\delta z = \matrixelement{B0}{K_2}{B0} -f_1(E_B) - if_2(E_B)=0,
:::

or,

:::{math}
:label: eq-nlw-59
z_B = E_B + \matrixelement{B0}{K_2}{B0} + P\sum_{A\lambda} {|\matrixelement{A\lambda}{K_1}{B0}|^2 \over E_B-E_A-\omega} -i\pi \sum_{A\lambda} |\matrixelement{A\lambda}{K_1}{B0}|^2 \, \delta(E_A+\omega-E_B),
:::

where we have rearranged signs in the third term. We see that the zero of $D(z)$ has moved off the real axis into the lower half plane. As for its imaginary part, a comparison with {eq}`eq-nlw-9` shows that it is $-\Gamma_B/2$, where $\Gamma_B/\hbar$ is the decay rate of state $B$.

The real part of $\delta z$ bears a close relationship to the energy shifts of bound state perturbation theory, as explained in {ref}`ch-pertth`. The state $\ket{B0}$ is a bound (normalizable) eigenstate of $K_0$ with energy $E_B$. It is an eigenstate of the unperturbed system, that is, the atom with the interactions with the electromagnetic field switched off. Of course, in reality we cannot switch off those interactions; do they lead to shifts in atomic energy levels?

To answer this question we consider using bound state perturbation theory to compute the shift in level $E_B$ due to the perturbation $K'=K_1+K_2$. According to {eq}`eq-pertth-22`, there is a first order shift

:::{math}
:label: eq-nlw-60
\Delta E^{(1)}_B = \matrixelement{B0}{K'}{B0} =\matrixelement{B0}{K_2}{B0},
:::

where $K_1$ does not contribute. Also, according to {eq}`eq-pertth-23` the nominal second order shift is

:::{math}
:label: eq-nlw-61
\Delta E^{(2)}_B = \sum_{k\ne B0} {|\matrixelement{k}{K'}{B0}|^2 \over E_B-E_k}.
:::

If we replace $K'$ by $K_1$ to get the lowest order contribution, then the only states $k$ that we need sum over are the single photon states $\ket{A\lambda}$, and we obtain

:::{math}
:label: eq-nlw-62
\Delta E^{(2)}_B = \sum_{A\lambda} {|\matrixelement{A\lambda}{K_1}{B0}|^2 \over E_B-E_A-\omega}.
:::

This is almost the third term on the right in {eq}`eq-nlw-59`, missing only the principal value sign.

Actually, without the principal value $\Delta E^{(2)}_B$ in {eq}`eq-nlw-62` is not defined, nor is it justified to use bound state perturbation theory to find the energy shift in the state $\ket{B0}$ due to the interaction with the electromagnetic field. Bound state perturbation theory applies when we have discrete energy levels that are separated from one another, and in this system the state $\ket{B0}$ is a discrete state imbedded in the continuum. Nevertheless, our search for the zero of $D(z)$ has led to expressions that are obviously related to the energy shifts of bound state perturbation theory, except that the answers are well defined and the energy shift includes an imaginary part. Let us therefore simply *define* $\Delta E^{(2)}_B$ to be the third term on the right in {eq}`eq-nlw-59` (that is, by {eq}`eq-nlw-62` but with a principal value sign), so that

:::{math}
:label: eq-nlw-63
z_B = E_B + \Delta E^{(1)}_B + \Delta E^{(2)}_B - i\Gamma_B/2 = {\tilde E}_B - i\Gamma_B/2,
:::

where

:::{math}
:label: eq-nlw-64
{\tilde E}_B = E_B + \Delta E^{(1)}_B + \Delta E^{(2)}_B.
:::

Then ${\tilde E}_B$ is the real part of the energy of atomic state $B$, corrected for interactions with the field, while the imaginary part is $-\Gamma_B/2$.

(sec-nlw-9)=

## The Transition Amplitude $a_{B0}(t)$ and the Exponential Decay Law

We return to the integral {eq}`eq-nlw-44` for the transition amplitude $a_{B0}(t)$. The integrand has a pole at $z=z_B$, located near and below the energy $E_B$ of the unperturbed state $\ket{B0}$, as illustrated in {ref}`fig-nlw-9`. The contour can be closed with a semicircle in the lower half plane and can then be contracted into a small circle around the pole at $z_B$ in the lower half plane.

:::{figure} images/nlw-fig09.png
:label: fig-nlw-9
:width: 80%

Complex plane for the inverse Laplace transform for $a_{B0}(t)$, Eq. {eq}`eq-nlw-44`. The integrand has a simple pole at $z=z_B$, near and below the unperturbed energy $E_B$.
:::

:::{figure} images/nlw-fig10.png
:label: fig-nlw-10
:width: 80%

The contour of {ref}`fig-nlw-9` can be closed in the lower half-plane and contracted around the pole at $z=z_B$.
:::


Near $z=z_B$ we can expand $D(z)$,

:::{math}
:label: eq-nlw-65
D(z)= D(z_B)+(z-z_B)D'(z_B)+\ldots.
:::

But the first term vanishes and by {eq}`eq-nlw-35` we have $D'(z) = 1 + O(K_1^2)$. Therefore to lowest order,

:::{math}
:label: eq-nlw-66
D(z) = z-z_B
:::

when $z$ is near $z_B$. The contour in {ref}`fig-nlw-10` can be contracted arbitrarily close to the pole at $z_B$ so the integral {eq}`eq-nlw-44` can be written

:::{math}
:label: eq-nlw-67
a_{B0}(t) = {-1\over 2\pi i}\oint dz\, {e^{-izt} \over z-z_B} = e^{-iz_B t},
:::

where the circle is traversed in a clockwise (negative) direction. We can also write this as

:::{math}
:label: eq-nlw-68
a_{B0}(t) = e^{-i({\tilde E}_B -i\Gamma_B/2)t} =e^{-i{\tilde E}_B t}\, e^{-\Gamma_B t/2}.
:::

This shows that the amplitude to remain in the initial state evolves with a real phase factor indicating an energy ${\tilde E}_B$, that is, one corrected for the interactions with the field, but with an exponential decay factor. The probability to remain in the initial state is the square of the amplitude,

:::{math}
:label: eq-nlw-69
P_{B0}(t) = e^{-\Gamma_B t},
:::

which shows the exponential decay law.

We see that the exponential decay law is not a rigorous consequence of the Schr\"odinger equation, but rather it follows from a series of nontrivial approximations. In fact, it is known that there are deviations from the exponential decay law for long times.

The unperturbed system has a genuine bound state at $E=E_B$ but when the perturbation is turned on there is only a continuous spectrum in the neighborhood of $E=E_B$. The discrete state has “dissolved into the continuum,” and become a *resonance*. A similar mechanism explains the resonances associated with the doubly excited states in helium, as discussed in {ref}`sec-helium-9`.

This derivation has been based on a model of an atom, but it applies in its essence to the decay of any excited state of a system, including radioactive decays of nuclei and decays of unstable particles. The derivation looks complicted, but that is because the exponential law is not exact. The usual “simple” derivations of the exponential decay law rely on a type of statistical assumption of the Markov type, which means that the transition probability for a system depends only on the present state and not the previous history. This is what we usually assume about radioactive decay. For example, if a nucleus has not decayed after ten times its average lifetime, the probability that it will decay in the next second is the same as it always was. The nucleus does not try to “hurry up and decay” because it has failed to do so for so long. At least this is what we usually assume. But studying the decay by solving the Schr\"odinger equation, we find that the exponential decay law is only approximate. Various aspects of this situation are discussed in an appendix to the first edition of Sakurai's book, *Modern Quantum Mechanics*.

(sec-nlw-10)=

## The Transition Amplitude $a_{A\lambda}(t)$

We can also get the amplitude to make a transition from the initial state $\ket{B0}$ to some specific final state $\ket{A\lambda}$. According to {eq}`eq-nlw-36` this is

:::{math}
:label: eq-nlw-70
a_{A\lambda}(t) = {-1\over 2\pi i} \int_{C_+} dz\, {e^{-izt} \over (z-E_A-\omega)D(z)} \matrixelement{A\lambda}{K_1}{B0}.
:::

The matrix element is independent of $z$ and can be taken out of the integral. As for the rest of the integrand, it has poles at $z=E_A+\omega$ and at $z=z_B$, as illustrated in {ref}`fig-nlw-11`. The figure is drawn for the case $E_A < E_B$, as required if there is to be a transition $\ket{B0} \to \ket{A\lambda}$.

:::{figure} images/nlw-fig11.png
:label: fig-nlw-11
:width: 80%

Complex plane for the inverse Laplace transform for $a_{A\lambda}(t)$, Eq. {eq}`eq-nlw-70`. The integrand has poles at $z=E_A+\omega$ and at $z=z_B$.
:::

:::{figure} images/nlw-fig12.png
:label: fig-nlw-12
:width: 80%

The contour of {ref}`fig-nlw-11` can be closed in the lower half-plane and contracted to two small circles around the poles at $z=E_A+\omega$ and $z=z_B$.
:::


Evaluation of the integral by the residue theorem gives two terms, one for each pole,

:::{math}
:label: eq-nlw-71
a_{A\lambda}(t) = \matrixelement{A\lambda}{K_1}{B0} \Bigl[{e^{-i(E_A+\omega)t}\over D(E_A+\omega)} + {e^{-iz_B t} \over z_B-E_A-\omega}\Bigr].
:::

This is valid for any final state $\ket{A\lambda}$ but the amplitude will be small unless energy is approximately conserved, which means that $E_A+\omega$ is near to $E_B$, and therefore near to $z_B$. If this is the case then {eq}`eq-nlw-66` gives

:::{math}
:label: eq-nlw-72
D(E_A+\omega) = E_A+\omega-z_B= E_A+\omega - {\tilde E}_B + i\Gamma_B/2 = \omega-{\tilde\omega}_{BA} + i\Gamma_B/2,
:::

where we define

:::{math}
:label: eq-nlw-73
{\tilde\omega}_{BA} = {\tilde E}_B - E_A.
:::

Then the two denominators in {eq}`eq-nlw-71` are the same to within a sign and the result can be written

:::{math}
:label: eq-nlw-74
a_{A\lambda}(t) = \matrixelement{A\lambda}{K_1}{B0}\, e^{-i(E_A+\omega)t} \Bigl[{1-e^{i(\omega-{\tilde\omega}_{BA})t} \, e^{-\Gamma_Bt/2} \over \omega-{\tilde\omega}_{BA} + i\Gamma_B/2}\Bigr].
:::

(sec-nlw-11)=

## Amplitude and Probability as $t\to\infty$

The long-time behavior of the system is of interest but as $t\to\infty$ the amplitude $a_{A\lambda}(t)$ oscillates and does not approach a limit due to the phase factor $e^{-i(E_A+\omega)t}$. This factor is due to the evolution under the unperturbed Hamiltonian $H_0$, which is all that matters at long times because the photon will have left the atom behind and is no longer interacting with it. A similar situation holds in scattering theory, in which a wave packet directed at a target evolves according to the free particle Hamiltonian at large negative and large positive times. See the discussion in {ref}`sec-tdpt-5`.

If we switch to the interaction picture this time evolution is stripped off, and the amplitude is

:::{math}
:label: eq-nlw-75
c_{A\lambda}(t) = \matrixelement{A\lambda}{K_1}{B0} \Bigl[{1-e^{i(\omega-{\tilde\omega}_{BA})t} \, e^{-\Gamma_Bt/2} \over \omega-{\tilde\omega}_{BA} + i\Gamma_B/2}\Bigr].
:::

This is the same result we got with time-dependent perturbation theory, see {eq}`eq-nlw-6` and {eq}`eq-nlw-7`, except that $\omega-\omega_{BA}$ is replaced by $\omega-{\tilde\omega}_{BA} + i\Gamma_B/2$. The transition amplitude in the interaction picture does have a long-time limit,

:::{math}
:label: eq-nlw-76
\lim_{t\to\infty} c_{A\lambda}(t) = {\matrixelement{A\lambda}{K_1}{B0} \over \omega-{\tilde\omega}_{BA} + i\Gamma_B/2},
:::

whose square gives the long-time probability,

:::{math}
:label: eq-nlw-77
\lim_{t\to\infty} P_{A\lambda}(t)= {|\matrixelement{A\lambda}{K_1}{B0}|^2 \over (\omega-{\tilde\omega}_{BA})^2 + \Gamma_B^2/4}.
:::

:::{figure} images/nlw-fig13.png
:label: fig-nlw-13
:width: 80%

The transition probability has a Lorentzian dependence on the frequency. The peak is centered at the resonance frequency $\omega={\tilde\omega}_{BA}$ and its full width at half maximum is $\Gamma_B/\hbar$. ure is not to scale.
:::

The correction term $\Gamma_B^2/4$ in the denominator does not matter much if $|\omega-{\tilde\omega}_{BA}|\gg \Gamma_B$, but when $|\omega-{\tilde\omega}_{BA}|\sim \Gamma_B$ the transition probability varies rapidly in $\omega$. The matrix element may also depend on $\omega$ but is nearly constant over the small range of order $\Gamma_B$ about resonance. Overall the dependence of the transition probability has the Lorentzian shape, with a full width at half maximum (FWHM) of $\Gamma_B$. See {ref}`fig-nlw-13`.

The Lorentzian replaces the energy-conserving $\delta$-function that we had with time-dependent perturbation theory. The photons emitted in the transition $B\to A$ do not all have the same energy, but rather there is a spread of order $\Gamma_B$. Note the scales in the figure. In a typical atomic problem ${\tilde\omega}_{BA}$ is of order unity in atomic units, while for E1 transitions $\Gamma_B$ is of order $\alpha^3\sim 10^{-6}$.

The width $\Gamma_B/\hbar$ is what is called the *natural line width* of the spectral line $B\to A$. Other effects also contribute to the broadening of the spectral line, for example, Doppler shifts if the source is a gas. Doppler shifts broaden the spectral line with a Gaussian profile, because of the Maxwellian distribution of particle velocities. If the density of the gas is above a certain amount there will also be *pressure broadening*, caused by the fact that before the atom has a chance to decay it has a collision with another atom. This effectively resets the clock in the evolution of the state of the atom. With pressure broadening the width of the spectral line can still be written $\Delta\omega\sim 1/\tau$, except that now $\tau$ is the collision time instead of the lifetime for spontaneous emission. The natural line width is the minimum line width obtained when all other sources of broadening are eliminated.

You may wonder why in the formula {eq}`eq-nlw-73` for ${\tilde\omega}_{BA}$ we correct the energy $E_B$ for interactions with the field but not $E_A$. Actually we should correct both energies but our formalism has not done this since we have restricted the ket space to states with at most one photon. Notice that if $A$ is the ground state its lifetime is infinite so $\Gamma_A=0$, but $A$ could be an excited state lying between $B$ and the ground state, as illustrated in {ref}`fig-nlw-2`. We would need a more sophisticated model to take into account the decay of both states $B$ and such a excited state $A$. This is required, for example, in problems of optical pumping or photon cascades. If $A$ is also an excited state then the line shape of the transition $B\to A$ is a Lorentzian with FWHM given by $\Gamma_A+\Gamma_B$.

As $t\to\infty$ the atom drops into the state $A$ with $100\%$ probability, so the sum of all the probabilities {eq}`eq-nlw-77` should add to 1. We can see that it does if we make the replacement,

:::{math}
:label: eq-nlw-78
{1\over (\omega-{\tilde\omega}_{BA})^2 + \Gamma_B^2/4} \to {2\pi\over \Gamma_B} \delta(\omega-{\tilde\omega}_{BA}),
:::

which follows from the representation {eq}`eq-nlw-51` of the $\delta$-function and the fact that the matrix element is slowly varying over the energy range $\Gamma_B$. This gives

:::{math}
:label: eq-nlw-79
\sum_{A\lambda} P_{A\lambda}(\infty) = {2\pi\over \Gamma_B} \sum_{A\lambda} |\matrixelement{A\lambda}{K_1}{B0}|^2 \, \delta(\omega-{\tilde\omega}_{BA}) =1,
:::

as follows from {eq}`eq-nlw-9`.

(sec-nlw-12)=

## Fixing the Kramers-Heisenberg Formula

Now we can see how to fix the singularities in the Kramers-Heisenberg formula. As noted in \secrnlw-1, the vanishing denominators arise from the time integrals in the Dyson series. For the resonant terms in question, the phase factor that is integrated is given by {eq}`eq-nlw-3`, which we write here as

:::{math}
:label: eq-nlw-80
(e^{-iE_It})^* \, e^{-i(E_A+\omega)t},
:::

dropping the primes on $t$ and setting $\hbar=1$. The two time-dependent exponential factors shown came from a matrix element which in the case of the Kramers-Heisenberg formula can be written

:::{math}
:label: eq-nlw-81
\matrixelement{I}{U_0(t)^\dagger K_1 U_0(t)}{A\lambda},
:::

where the factors of $U_0$ represent the switch from the interaction picture to the Schr\"odiner picture. From another point of view they also represent the time evolution of the states of the system at a lower order approximation that is being substituted back into the Schr\"odinger equation and integrated over time to get the next order approximation.

Based on what we have done with the long-time behavior of quantum systems, however, it would be more accurate to use the time evolution of states $I$ and $A$ corrected for the interactions with the field, that is, to replace the factor {eq}`eq-nlw-80` by

:::{math}
:label: eq-nlw-82
[e^{-i({\tilde E}_I -i\Gamma_I/2)t}]^* \, e^{-i(\tilde E_A+\omega)t},
:::

where

:::{math}
:label: eq-nlw-83
\begin{aligned}
{\tilde E}_I & = E_I + \Delta E^{(1)}_I + \Delta E^{(2)}_I, \\
{\tilde E}_A & = E_A + \Delta E^{(1)}_A + \Delta E^{(2)}_A, \\

\end{aligned}
:::

as in {eq}`eq-nlw-64`. We do not include a term $\Gamma_A$ because in our outline of the problem in \secrnlw-1 we assumed that $A$ was the ground state of the atom.

If we do this, then the denominator $\omega_{IA}-\omega$ of the Kramers-Heisenberg formula {eq}`eq-nlw-1` is replaced by

:::{math}
:label: eq-nlw-84
{\tilde\omega}_{IA} - \omega - i\Gamma_I/2.
:::

where

:::{math}
:label: eq-nlw-85
{\tilde\omega}_{IA} = {\tilde E}_I - {\tilde E}_A
:::

(like {eq}`eq-nlw-73` but with both energies corrected). It is logical that the resonance frequency $\omega_{IA}$ should be corrected in this manner, because the real resonance occurs at ${\tilde\omega}_{IA}$, not $\omega_{IA}$. Also, the denominator now has an imaginary part and does not vanish at $\omega={\tilde\omega}_{IA}$. We see, as suspected in \secrnlw-1, that the nominal Kramers-Heisenberg formula breaks down when $|\omega-{\tilde\omega}_{IA}| <\approx \Gamma_I/\hbar$. Near such frequencies the amplitude sum {eq}`eq-nlw-2` is dominated by a single term, and

:::{math}
:label: eq-nlw-86
M \approx {1\over m\hbar} {\matrixelement{A}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\,*})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A} \over {\tilde\omega}_{IA} - i\Gamma_I/2}.
:::

The cross is given by

:::{math}
:label: eq-nlw-87
\dod{\sigma}{\Omega'} = r_e^2 {1\over m^2\hbar^2} {|\matrixelement{A}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\,*})}{I}|^2 |\matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A}|^2 \over (\omega-{\tilde\omega}_{IA})^2 + \Gamma_I^2/4}.
:::

If the transition $I\to A$ is allowed as an E1 transition, then $\Gamma_I$ is of order $\alpha^3$ in atomic units, so that at resonance the cross saturates at a value that is of order $\alpha^{-6} \sim 10^{13}$ times larger than it is out in the “desert” where $\omega$ is not close to any ${\tilde\omega}_{IA}$. In terms of powers of the fine structure constant, the cross is of order $\alpha^{-2} a_0^2 \sim 10^4 \,a_0^2$ at resonance, which is quite large by atomic standards. This is of the order of the square of the wavelength, which is characteristic of resonant cross s in general.

Thus the cross as a function of frequency has the Lorentzian shape in the neighborhood of a resonance, much like the sketch in {ref}`fig-nlw-13`. The width of the resonance is of order $\Gamma_I/\hbar$ and the height is of order $1/\Gamma_I^2$, so if a gas is subjected to broad band radiation then by far the majority of the scattering is resonant, at least until the beam is depleted of resonant photons. This is the reason for the dark Fraunhoffer lines in the solar spectrum; as light from the sun passes through the cooler, outer layers of the atmosphere of the sun, the resonant photons are scattered into random directions and removed from the direct sunlight. In this process, the Doppler shift from the motion of the atoms causes the dark lines to be broadened considerably in comparison to the natural line width.

It was realized by the mid-nineteenth century that the dark Fraunhoffer lines in the spectrum of the sun or other stars occur at the same frequencies as the emission spectra of various elements, and so can be used to determine the chemical composition of stellar atmospheres. The element helium was first discovered in this way in the sun's atmosphere, before it was known on earth (hence the name, from Greek “helios” meaning “sun”).
