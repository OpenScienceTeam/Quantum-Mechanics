---
title: "43. Scattering of Radiation by Matter"
---
(ch-photscatt)=

# 43. Scattering of Radiation by Matter

(sec-photscatt-1)=

## Introduction

In the previous set of notes we treated the emission and absorption of radiation by matter. In these notes we turn to the scattering of radiation by matter. As before, the material system in question can be almost anything (atom, molecule, nucleus, etc), but when it is necessary to be specific we shall for simplicity assume that it is a single-electron atom. The formalism is easily extended to other types of material systems.

We shall see that in a certain sense the emission and absorption of radiation are special cases of the scattering of radiation, in which the frequency of the initial photon is close to a resonance frequency of the material system (the Einstein frequency connecting two energy eigenstates). In such cases it is partly a matter of preference how one should view the process, but in some respects the scattering point of view is more fundamental and elegant.

(sec-photscatt-2)=

## Applications

The applications of the theory developed in these notes are very broad. Almost any situation in which radiation passes through a gas affords an example of the physics we shall describe here. For example, in infrared and Raman scattering experiments radiation is passed through a molecular gas and the absorption spectrum or scattering cross is measured, providing a primary source of information about the structure of molecules.

Another example involves radiation passing through the Earth's atmosphere. The atmosphere is mostly transparent to sunlight, but there is some scattering, especially at the higher (blue) frequencies. This is Rayleigh scattering, which is discussed in 12. The higher frequencies are more strongly scattered because they are closer to certain resonances in the ultraviolet. As we shall see, the cross for scattering rises rapidly as a function of frequency as we approach a resonance. This is the reason the sky is blue: When we look at a part of the sky away from the sun, the blue light we see is sunlight scattered by the air along our line of sight.

The Earth in turn radiates thermal radiation in the infrared that must pass through the atmosphere to reach outer space where it escapes. This radiation has a frequency range that covers the vibrational transitions of most simple molecules, so it is strongly scattered by several types of molecules such as the greenhouse gases $CO_2$, $H_2O$ and $CH_4$. Thus an infrared photon leaving the Earth's surface must diffuse through the atmosphere in a random walk, a process that is much slower than passing straight through. The greenhouse gases act like a blanket, keeping the Earth warm. Notice that the atmosphere makes it easy for radiation to get in at optical frequencies, and difficult to get back out at infrared frequencies.

There are many examples in astrophysics where the scattering or absorption of radiation by matter is important. For example, sunlight passing through the cooler outer layers of the sun's atmosphere produces an absorption spectrum (the dark Fraunhoffer lines) that give information about the chemical species occurring in the sun and the physical conditions in its atmosphere. Similar information is available for other stars. For another example, transport of energy by radiation is important in the interior of stars, in which photons undergo repeated scattering by free electrons in the plasma and by bound electrons in atoms (if the atoms are not completely stripped, it depends on circumstances) and slowly diffuse upward toward the surface. In many stars such as the sun this radiative transport dominates the energy transport at certain radii, while at other radii convective transport is dominant.

The interaction of photons with matter is also important in nuclear physics. In the M\"ossbauer effect, for example, gamma ray photons emitted in the decay of a nucleus are used to excite other nuclei, lifting them from their ground state into an excited state. See {ref}`sec-transfop-12`. The resonance is very narrow, however, and the photon can be shifted out of resonance by a Doppler shift involving only small velocities. The M\"ossbauer effect provided the first clear experimental demonstration of the red shift that photons suffer on climbing out of a gravitational field. This effect implies that clocks run at different rates in different regions of a gravitational field. It is one of the conceptual corner stones of general relativity.

(sec-photscatt-3)=

## The Scattering Problem

We shall consider the reaction

:::{math}
:label: eq-photscatt-1
A + \gamma \to B + \gamma',
:::

in which an atom in state $A$ interacts with an incident photon $\gamma$, which leaves the atom in state $B$ and produces the scattered photon $\gamma'$. We will write $\lambda=(\kvec\mu)$, $\lambda'=(\kvec'\mu')$ for the modes of the incident and scattered photons, where $\mu$ is a polarization index, as described in {ref}`sec-classemf-12`. We will assume that $\lambda \ne \lambda'$, since otherwise there is no scattering. If $A=B$, the scattering is elastic (the initial and final atomic states are the same), and by conservation of energy we have $\omega = \omega'$, where $\omega$ and $\omega'$ are the frequencies of the photons with modes $\lambda$ and $\lambda'$. If $A \ne B$, the scattering is inelastic, and we have $\omega \ne \omega'$. In this case the final atomic state $B$ may either be higher or lower in energy than the initial state $A$, depending on circumstances. We will use box normalization in our analysis, so the indices $\lambda$, $\lambda'$, etc are discrete. With a few changes, the states $\ket{A}$ and $\ket{B}$ can be interpreted as belonging to a molecule, nucleus, or other material system, rather than an atom.

We shall treat the scattering reaction {eq}`eq-photscatt-1` by means of time-dependent perturbation theory, developed in {ref}`ch-tdpt`. As we shall see, we will have to make some extensions of that theory for the application at hand. Our earlier presentation of time-dependent perturbation theory was stated in a general notation, in which $\ket{i}$ is an initial state, $\ket{n}$ is a variable final state that we must sum over to get useful transition probabilities, and $\ket{k}$ is an intermediate state. These initial, final and intermediate states will be identified with particular states in our atom-field system, so we will switch back and forth between the general notation and the one specific to our problem.

Specifically, we have one photon in both our initial and final states. We will write these states in a variety of ways,

:::{math}
:label: eq-photscatt-2
\begin{aligned}
\ket{i} &= \ket{A} a^\hc_\lambda \ket{0} = \ket{A}\ket{\lambda} = \ket{A\lambda}, \\
\ket{n} &= \ket{B} a^\hc_{\lambda'} \ket{0} = \ket{B}\ket{\lambda'} = \ket{B\lambda'}.
\end{aligned}
:::

The energies of these states are

:::{math}
:label: eq-photscatt-3
\begin{aligned}
E_i &= E_A + \hbar\omega, \\
E_n &= E_B + \hbar\omega', \\

\end{aligned}
:::

where $E_A$ and $E_B$ are the energies of the two atomic states. The Einstein frequency connecting the initial and final states is

:::{math}
:label: eq-photscatt-4
\omega_{ni} = {E_n - E_i \over \hbar} = \omega_{BA} + \omega' - \omega,
:::

where $\omega_{BA} =(E_B-E_A)/\hbar$.

The problem will be to compute the differential cross $d\sigma/d\Omega'$, where $\Omega'$ refers to the direction of the outgoing photon (in mode $\lambda'$). The differential cross is a function of the mode of the initial photon $\lambda$, the two atomic states $A$ and $B$, and of the polarization and direction of the final photon, whose mode is $\lambda'$. The energy of the final photon is determined by conservation of energy.

(sec-photscatt-4)=

## The Transition Amplitude Vanishes at First Order in $\Avec$

We will take the Hamiltonian for the interaction of the matter with the radiation to be $K=K_0 + K_1 + K_2$, where

:::{math}
:label: eq-photscatt-5a
\begin{aligned}
K_0 &= {\pvec^2 \over 2m} + U(r) + \sum_\lambda \hbar\omega_\lambda \, a^\hc_\lambda a_\lambda,
\end{aligned}
:::

:::{math}
:label: eq-photscatt-5b
\begin{aligned}
K_1 &= {e\over mc}[ \pvec \cdot \Avec(\xvec) + \Svec\cdot\Bvec(\xvec)],
\end{aligned}
:::

:::{math}
:label: eq-photscatt-5c
\begin{aligned}
K_2 &= {e^2 \over 2m c^2} \Avec(\xvec)^2.
\end{aligned}
:::

We write our Hamiltonian as $K$ so as not to confuse it with the Hamiltonian $H=H_0+H_1$ that is used in the general theory of time-dependent perturbation theory. We will have to identify $H_0$ with $K_0$ for our particular problem, and $H_1$ with $K_1+K_2$. Although we have written $K_0$ as a single-electron system, very little of the following analysis depends on this and our results, as mentioned, will be valid also for molecules, nuclei, and other systems.

The Hamiltonian $K$ is ordered in powers of the vector potential $\Avec$, which represents physically the amplitude of the light wave. That is, $K_0$ is $O(1)$, $K_1$ is $O(\Avec)$, including the term $\Svec\cdot\Bvec$ since $\Bvec=\del\cross\Avec$, and $K_2$ is $O(\Avec^2)$.

The transition amplitude in first order time-dependent perturbation theory is given by {eq}`eq-tdpt-36`, which we reproduce here:

:::{math}
:label: eq-photscatt-6
c_n^{(1)}(t) = {2\over i\hbar} e^{i\omega_{ni} t/2} \Bigl( {\sin \omega_{ni}t/2 \over \omega_{ni}}\Bigr) \matrixelement{n}{H_1}{i}.
:::

For our application we must replace $H_1$ by $K_1+K_2$, but if we only wish to work to first order in $\Avec$ we can ignore $K_2$ compared to $K_1$. Thus we make the replacement,

:::{math}
:label: eq-photscatt-7
\matrixelement{n}{H_1}{i} \to \matrixelement{n}{K_1}{i}= {e\over mc} \matrixelement{B\lambda'} {[\pvec\cdot\Avec(\xvec) + \Svec\cdot\Bvec(\xvec)]} {A\lambda},
:::

in {eq}`eq-photscatt-6`. The fields $\Avec$ and $\Bvec$ have Fourier series {eq}`eq-quantemf-22` and {eq}`eq-quantemf-24` in terms of the modes of the field. If we write out these series, suppressing all factors except the creation and annihilation operators, then they have the structure,

:::{math}
:label: eq-photscatt-8
\Avec,\Bvec = \sum_{\lambda_1} \bigl( a_{\lambda_1} \ldots a^\hc_{\lambda_1}\bigr),
:::

where we are careful to use the index $\lambda_1$ as a dummy variable of summation, so as not to confuse it with the indices $\lambda$ and $\lambda'$ of the incident and scattered photons.

Now focusing on the field part of the matrix element {eq}`eq-photscatt-7`, we see that the annihilation operator $a_{\lambda_1}$ does not contribute to the transition amplitude, because it acts on a state with a single photon, $\ket{A\lambda}$, and either produces a state with zero photons (if $\lambda_1 = \lambda$) or annihilates it (if $\lambda_1 \ne \lambda)$. In either case, the resulting state is orthogonal to the state $\ket{B\lambda'}$, and gives zero when the scalar product is taken. Similarly, the creation operator $a^\hc_{\lambda_1}$ in the Fourier series {eq}`eq-photscatt-8` acts on the single photon state $\ket{A\lambda}$ and produces a two-photon state, which is necessarily orthogonal to any one-photon state such as $\ket{B\lambda'}$. Again, the field part of the scalar product vanishes. Thus we find

:::{math}
:label: eq-photscatt-9
\matrixelement{n}{K_1}{i}=0,
:::

and there is no contribution to the scattering amplitude at first order in $\Avec$.

More generally, in any vacuum expectation value of a product of creation and annihilation operators, something like

:::{math}
:label: eq-photscatt-10
\matrixelement{0}{\\text{product of a's and a^\dagger s}}{0},
:::

the answer vanishes unless the number of $a$'s and the number of $a^\dagger$'s are equal. In particular, the answer vanishes if the total number of $a$'s and $a^\dagger$'s is odd.

We see that for our problem, we must go to second order in $\Avec$ to find a nonvanishing contribution; this will involve second order perturbation theory.

(sec-photscatt-5)=

## Second-Order Time-Dependent Perturbation Theory

This is the first time we have had an application of second-order time-dependent perturbation theory, so we shall return to the formalism of {ref}`ch-tdpt`\ and develop the theory at second order, using the notation of those notes. In particular, the Hamiltonian is $H=H_0 + H_1$. The second-order contribution to the transition amplitude $c_n(t)$ in the interaction picture is given by {eq}`eq-tdpt-34` in the general case in which $H_1$ in the Schr\"odinger picture is allowed to depend on time. For our scattering application, $H_1$ is time-independent, so we can do the time integrations appearing in {eq}`eq-tdpt-31a`. The integral in the first order term in {eq}`eq-tdpt-31a` was done already in {ref}`sec-tdpt-9`, with the result shown in {eq}`eq-tdpt-36` and reproduced above in {eq}`eq-photscatt-6`. As for the integrals in the second order term in {eq}`eq-tdpt-31b`, we first do the $t''$ integration, finding,

:::{math}
:label: eq-photscatt-11
c^{(2)}_n(t) = {1\over (i\hbar)^2} \int_0^t dt' \, \sum_k e^{i\omega_{nk}t'} \Bigl( {e^{i\omega_{ki}t'} -1 \over i\omega_{ki}}\Bigr) \matrixelement{n}{H_1}{k} \matrixelement{k}{H_1}{i}.
:::

Recall that the sum on $k$ is a sum over “intermediate states” that came from the insertion of a resolution of the identity between the two Hamiltonian factors in {eq}`eq-tdpt-31b`. We combine the phase factors in {eq}`eq-photscatt-11`, using the identity,

:::{math}
:label: eq-photscatt-12
\omega_{nk} + \omega_{ki} = \omega_{ni},
:::

and then we do the $t'$ integration,

:::{math}
\begin{aligned}
c^{(2)}_n(t) &= {1\over (i\hbar)^2} \int_0^t dt' \, \sum_k {1\over i\omega_{ki}} (e^{i\omega_{ni}t'} - e^{i\omega_{nk}t'}) \matrixelement{n}{H_1}{k} \matrixelement{k}{H_1}{i}
\end{aligned}
:::

:::{math}
:label: eq-photscatt-13
\begin{aligned}
&= {1\over (i\hbar)^2} \sum_k {1\over i\omega_{ki}} \Bigl[ \Bigl( {e^{i\omega_{ni}t} -1 \over i\omega_{ni}}\Bigr) -\Bigl({e^{i\omega_{nk}t}-1\over i\omega_{nk}}\Bigr) \Bigr]\matrixelement{n}{H_1}{k} \matrixelement{k}{H_1}{i}.
\end{aligned}
:::

Of the two major time-dependent factors in the square brackets in {eq}`eq-photscatt-13`, the first one,

:::{math}
:label: eq-photscatt-14
{e^{i\omega_{ni}t} -1 \over i\omega_{ni}} = 2 e^{i\omega_{ni}t/2} \, {\sin \omega_{ni}t/2 \over \omega_{ni}},
:::

is the same time-dependent factor that appears in the first order term $c^{(1)}_n(t)$ shown in {eq}`eq-photscatt-6`. Notice that this factor is independent of $k$ and can be taken out of the sum in {eq}`eq-photscatt-13`. When squared to produce a probability, this factor produces a quantity proportional to time multiplied times a function of frequency that gets narrower as time gets longer,

:::{math}
:label: eq-photscatt-15
{\sin^2 \omega t/2 \over \omega^2} = {\pi\over 2} \, t\, \Delta_t(\omega),
:::

where

:::{math}
:label: eq-photscatt-16
\lim_{t\to\infty} \Delta_t(\omega) = \delta(\omega).
:::

See {eq}`eq-tdpt-46` and {eq}`eq-tdpt-47`. The fact that the result is proportional to time is essential for getting a transition rate (a probability per unit time), and the emerging $\delta$-function in the limit $t\to\infty$ is necessary for energy conservation, as explained in {ref}`ch-tdpt`. In fact, as explained in {ref}`sec-tdpt-15`, we do not really have to take $t$ to $\infty$, it need only be long enough for certain initial transients to die away. These transients are related to the artificiality of the initial conditions, and are nonphysical.

The initial conditions for the scattering problem considered in these notes contain an artificial element, as did the initial conditions in the potential scattering problem considered in {ref}`sec-tdpt-14`. That is, we are assuming that at $t=0$ the atom is known to be in the state $A$ and the field consists of a single photon in mode $\lambda$. This mode is a plane wave that fills up all of space, including the region occupied by the atom. It would be impossible to set up such initial conditions experimentally, since there is no way for a light wave to get into the region occupied by the atom without interacting with it. A more realistic set of initial conditions would be a wave packet made up out of single photon states that initially is remote from the atom and not interacting with it. To treat such wave packets, however, would require a more sophisticated formalism than we are using here, so we will stick with the initial conditions we have chosen. The price we pay, however, is the appearance of initial transients without physical significance.

The second major time-dependent term inside the square brackets in {eq}`eq-photscatt-13` is just such a transient. This term, when squared, does not produce something proportional to time, but rather just gives bounded oscillations that go to zero in the limit $t\to\infty$ after we divide by time. Thus, they do not contribute to the transition rate. This is because the frequency $\omega_{nk}$ occurring in that term is not independent of $k$. The same is true for the cross terms that arise when the sum of the two major time-dependent terms in {eq}`eq-photscatt-13` is squared. Thus, if all we are interested in is the transition rate and not the initial transients, we can drop the second major time-dependent term in {eq}`eq-photscatt-13`.

The result is an effective transition amplitude at second order that is proportional to the time-dependent factor {eq}`eq-photscatt-14`, the same factor that occurs at first order. Combining the first and second order terms, we obtain an effective transition amplitude,

:::{math}
:label: eq-photscatt-17
c^eff_n(t) =  {2\over i\hbar} e^{i\omega_{ni} t/2} \Bigl( {\sin \omega_{ni}t/2 \over \omega_{ni}}\Bigr) \biggl[\matrixelement{n}{H_1}{i} + \sum_k {\matrixelement{n}{H_1}{k} \matrixelement{k}{H_1}{i} \over E_i - E_k} \biggr],
:::

where we have taken the denominator $\omega_{ki}$ appearing in {eq}`eq-photscatt-13` and written it as $-(E_i-E_k)/\hbar$. The result is the “energy denominator” seen in the second order contribution in {eq}`eq-photscatt-17`. Recall that we had such energy denominators also in second-order bound state perturbation theory (see {ref}`ch-pertth`). We drop the zeroth order contribution $\delta_{ni}$ to the transition amplitude since for our scattering problem $n \ne i$ (since $\lambda \ne \lambda'$).

(sec-photscatt-6)=

## The Photon Scattering Amplitude at Order $\Avec^2$

For our application $H_1$ in {eq}`eq-photscatt-17` must be replaced by $K_1+K_2$. At first order of perturbation theory, this gives the matrix element

:::{math}
:label: eq-photscatt-18
\matrixelement{n}{K_1+K_2}{i}.
:::

As we have just seen, however, the contribution to this matrix element from $K_1$ vanishes. But at second order in $\Avec$ we must keep the term $\matrixelement{n}{K_2}{i}$. This is the second-order Hamiltonian $K_2$ taken in first-order perturbation theory. Likewise, in the second order term of the general expression {eq}`eq-photscatt-17`, we can simply replace $H_1$ by $K_1$, ignoring $K_2$, if we wish to work to second order in $\Avec$. That is, we take the first-order Hamiltonian $K_1$ at second order perturbation theory. Altogether, the effective transition amplitude for our scattering problem, valid through order $\Avec^2$, is

:::{math}
:label: eq-photscatt-19
c^eff_n(t) =  {2\over i\hbar} e^{i\omega_{ni} t/2} \Bigl( {\sin \omega_{ni}t/2 \over \omega_{ni}}\Bigr) \Bigl[\matrixelement{n}{K_2}{i} + \sum_k {\matrixelement{n}{K_1}{k} \matrixelement{k}{K_1}{i} \over E_i - E_k} \Bigr],
:::

where $K_1$ and $K_2$ are given by {eq}`eq-photscatt-5a` and states $\ket{i}$ and $\ket{n}$ are given by {eq}`eq-photscatt-2`.

(sec-photscatt-7)=

## $K_2$ in First-Order Perturbation Theory

We begin with the term

:::{math}
:label: eq-photscatt-20
\matrixelement{n}{K_2}{i} ={e^2\over 2mc^2} \matrixelement{B\lambda'}{\Avec(\xvec)^2}{A\lambda}.
:::

Squaring the Fourier series {eq}`eq-quantemf-22` for $\Avec$, we obtain a product series with the structure,

:::{math}
:label: eq-photscatt-21
\Avec(\xvec)^2 \sim \sum_{\lambda_1 \lambda_2} (a_{\lambda_1} \ldots a^\hc_{\lambda_1}) \cdot (a_{\lambda_2} \ldots a^\hc_{\lambda_2}),
:::

where we suppress all factors except the creation and annihilation operators. This allows us to concentrate on the photon part of the matrix element {eq}`eq-photscatt-20`. We see that there are four types of products of creation and annihilation operators that occur in $\Avec^2$. The product of the two annihilation operators $a_{\lambda_1} a_{\lambda_2}$ does not contribute to the transition amplitude, since it acts on the single photon state $\ket{A\lambda}$ producing zero. Likewise, the product of the two creation operators $a^\hc_{\lambda_1} a^\hc_{\lambda_2}$ does not contribute, since it acts on $\ket{A\lambda}$ creating a three-photon state that is orthogonal to the one-photon state $\ket{B\lambda'}$. The product of the annihilation operator times the creation operator, $a_{\lambda_1} a^\hc_{\lambda_2}$, does contribute, however, as long as $\lambda_1 = \lambda$ and $\lambda_2 = \lambda'$. That is, the photon destroyed by $a_{\lambda_1}$ must be the incident photon, and the one created by $a^\hc_{\lambda_2}$ must be the scattered photon. Taking into account the other factors in the Fourier series, this product of operators corresponds to the product of polarization vectors ${\hat{\boldsymbol{\epsilon}}}_{\lambda} \cdot {\hat{\boldsymbol{\epsilon}}}^\cc_{\lambda'}$ and the product of phase factors $e^{i\kvec\cdot\xvec-i\kvec'\cdot\xvec}$. Similarly, the product of the creation operator times the annihilation operator $a^\hc_{\lambda_1} a_{\lambda_2}$ contributes as long at $\lambda_1=\lambda'$ and $\lambda_2 = \lambda$, and in this case the product of polarization vectors is ${\hat{\boldsymbol{\epsilon}}}^\cc_{\lambda'} \cdot {\hat{\boldsymbol{\epsilon}}}_\lambda$ and the product of phase factors is $e^{-i\kvec'\cdot\xvec + i\kvec\cdot\xvec}$. The terms that contribute are those that have a total of two annihilation and two creation operators between the vacuum bra and vacuum ket.

Thus out of the double infinite series {eq}`eq-photscatt-21` for $\Avec^2$, only two terms contribute to the transition amplitude, and both have the same product of polarization vectors and the same phase factors. The contributions of these two terms are equal. It is now easy to do the photon part of the matrix element, leaving only an atomic matrix element. The result is

:::{math}
:label: eq-photscatt-22
\matrixelement{n}{K_2}{i} = 2 \times {e^2 \over 2mc^2} {2\pi\hbar c^2 \over V} {1\over \sqrt{\omega \omega'}} ({\hat{\boldsymbol{\epsilon}}} \cdot {\hat{\boldsymbol{\epsilon}}}^{\prime\cc}) \, \matrixelement{B}{e^{i(\kvec-\kvec')\cdot\xvec}}{A},
:::

where the leading factor of 2 comes from the fact that we have two identical terms, and where we have made the abbreviations, ${\hat{\boldsymbol{\epsilon}}} = {\hat{\boldsymbol{\epsilon}}}_{\lambda}$, ${\hat{\boldsymbol{\epsilon}}}' = {\hat{\boldsymbol{\epsilon}}}_{\lambda'}$.

In the following we shall use the dipole approximation, in which $e^{i(\kvec-\kvec')\cdot\xvec} = 1$. As explained in {ref}`ch-radnmatt`, this approximation is equivalent to $a/\lambda \ll 1$, where $a$ is the size of the atom and $\lambda$ is the wave length of the radiation. This is an excellent approximation for atoms at optical frequencies, where the ratio $a/\lambda$ is less than $10^{-3}$. This causes the atomic matrix element in {eq}`eq-photscatt-22` to become simply $\braket{B}{A} = \delta_{BA}$. We see that the $K_2$-term only contributes to elastic scattering. Altogether, the matrix element becomes

:::{math}
:label: eq-photscatt-23
\matrixelement{n}{K_2}{i} = \Bigl({e^2\over mc^2}\Bigr) \Bigl({2\pi\hbar c^2\over V}\Bigr) {1\over \sqrt{\omega\omega'}} ({\hat{\boldsymbol{\epsilon}}}\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}) \, \delta_{BA}.
:::

(sec-photscatt-8)=

## Feynman Diagrams

Before proceeding to the $K_1^2$ term, we show how the terms of the perturbation series are associated with Feynman diagrams. A Feynman diagram is basically a space-time diagram showing the interactions of the particles. The diagrams correspond to terms in the transition amplitude; thus, each diagram is a complex number.

The time sequence of particle interaction in a Feynman diagram comes from the Dyson series in time-dependent perturbation theory. The Dyson series is given by {eq}`eq-tdpt-25`, reproduced here:

:::{math}
:label: eq-photscatt-24
\ket{\psi_I(t)} = \ket{i}+ {1\over i\hbar} \int_0^t dt' \, H_{1I}(t')\ket{i} +{1\over (i\hbar)^2} \int_0^t dt' \, \int_0^{t'} dt'' \, H_{1I}(t') H_{1I}(t'')\ket{i} + \ldots.
:::

This is a power series in $H_1$, a solution of the time-dependent Schr\"odinger equation in the interaction picture with initial condition $\ket{\psi_I(0)}=\ket{i}$. The Hamiltonian $H_{1I}$ is in the interaction picture; it is time-dependent even when $H_1$ (in the Schr\"odinger picture) is not, hence $H_{1I}$ at different times do not commute.

We will use the second order term of the Dyson series to illustrate the time ordering. In this term the various times satisfy

:::{math}
:label: eq-photscatt-25
t\ge t' \ge t'' \ge 0,
:::

where the initial time is 0, $t'$ and $t''$ are a pair of sequenced intermediate times, and $t$ is the final time. This leads to a language for describing the second order term of the Dyson series: we say that the initial state $\ket{i}$ is unchanged until time $t''$ when it is acted upon by $H_{1I}(t'')$, after which it is unchanged until time $t'$ when it is acted upon by $H_{1I}(t')$, after which it is unchanged until the final time $t$. The second order contribution to the transition amplitude is the sum (that is, the integral) of all such contributions, for all possible (ordered) values of $t'$ and $t''$.

Similarly, the first order term involves interacting with $H_{1I}$ at one intermediate time $t'$, and the zeroth order term involves no interaction. The pattern is clear for terms of any order.

:::{figure} images/photscatt-fig01.png
:label: fig-photscatt-1
:width: 80%

The seagull diagram. The four-point vertex describes the action of $K_{2I}$ at intermediate time $t'$, which annihilates the incident photon in mode $\lambda$, creates the scattered photon in mode $\lambda$, and connects initial atomic state $A$ with final state $B$. Time runs from bottom to top in the diagram, with the time sequence $0\le t' \le t$.
:::

To return to our problem, the term $\matrixelement{n}{K_2}{i}$ involves the second order Hamiltonian, but comes from the first order term in the Dyson series. Thus there is one interaction with $K_2$ at one intermediate time. This interaction destroys the incident photon $\lambda$ and creates the final photon $\lambda'$, and connects the initial atomic state $A$ with the final atomic state $B$. The Feynman diagram is shown in {ref}`fig-photscatt-1`; it is called a “seagull” diagram. In the diagram time increases from bottom to top. The atom lines are straight lines, and the photon lines are curvy. The single interaction with $K_2$ is an example of a 4-point vertex, that is, an interof four lines. Four-point vertices are created by the term $\Avec^2$ in the Hamiltonian, because of the structure of the product of the two Fourier series discussed above.

(sec-photscatt-9)=

## The term $K_1^2$ in Second Order Perturbation Theory

Now we turn to the second order term in the transition amplitude, extracted from {eq}`eq-photscatt-19`:

:::{math}
:label: eq-photscatt-26
\sum_k {\matrixelement{n}{K_1}{k} \matrixelement{k}{K_1}{i} \over E_i-E_k},
:::

where we use the general notation for the initial state $\ket{i}$, the final state $\ket{n}$, and the intermediate state $\ket{k}$. In our problem $k$ runs over a complete set of state of the matter plus field system, and in particular, it must include states of any number of photons. But $\ket{i}=\ket{A\lambda}$ and $\ket{n}=\ket{B\lambda'}$ contain only one photon, and $K_1$ can create or destroy only one photon, so the only intermediate states that give nonvanishing matrix elements are those with either zero or two photons. Thus there are two cases.

:::{figure} images/photscatt-fig02.png
:label: fig-photscatt-2
:width: 80%

In case I, the incident photon is destroyed before the final photon is created. There are zero photons in the intermediate state.
:::

:::{figure} images/photscatt-fig03.png
:label: fig-photscatt-3
:width: 80%

In case II, the final photon is created before the incident photon is destroyed. There are two photons in the intermediate state.
:::


In case I, the intermediate state contains zero photons. The first application of $K_1$ (at the first intermediate time, $t''$ in our notation) annihilates the incident photon $\lambda$, and the second application of $K_1$ (at the second intermediate time, $t'$ in our notation) creates the final photon $\lambda$. In case II, the intermediate state contains two photons, which must be in modes $\lambda$ and $\lambda'$. The first application of $K_1$ creates the final photon $\lambda'$ and the second (later) application of $K_1$ destroys the incident photon $\lambda$. Thus we have

:::{math}
:label: eq-photscatt-27
\begin{aligned}
\ket{k} = \begin{cases}\ket{I}\ket{0} \equiv \ket{I}, & Case I\\  \ket{I}a_\lambda^\dagger a_{\lambda'}^\dagger\ket{0} \equiv \ket{I\lambda\lambda'}, & Case II\\\end{cases}
\end{aligned}

:::

where $I$ refers to an intermediate atomic state. The Feynman diagrams for cases I and II are given in Figs.~{ref}`fig-photscatt-2` and {ref}`fig-photscatt-3`.

We may now evaluate the contributions of cases~I and II to the sum {eq}`eq-photscatt-26`. The initial and final energies $E_i$ and $E_n$, in the general notation, are translated into the notation of this problem by {eq}`eq-photscatt-3`. In case~I, the energy of the intermediate state, $E_k$ in the general notation, becomes $E_I$, the energy of the intermediate atomic state, in the notation of this problem. Thus, in case~I, the energy denominator in the sum {eq}`eq-photscatt-26` becomes

:::{math}
:label: eq-photscatt-28
E_i-E_k \to E_A+\hbar\omega - E_I = \hbar(\omega-\omega_{IA}),
:::

where $\omega_{IA} = (E_I-E_A)/\hbar$. Also, the second matrix element in {eq}`eq-photscatt-26` is interpreted as

:::{math}
:label: eq-photscatt-29
\matrixelement{k}{K_1}{i} = \matrixelement{I}{K_1}{A\lambda} = {e\over mc}\sqrt{2\pi\hbar c^2\over\ds V} {1\over\sqrt{\omega}} \matrixelement{I} {\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A},
:::

after using {eq}`eq-photscatt-5b` for $K_1$ and evaluating the field part of the matrix elements. We have dropped the term involving $\Svec\cdot\Bvec$, since it is of order $\alpha$ compared to the term $\pvec\cdot\Avec$ (this is equivalent to the dipole approximation, in which we set $e^{i\kvec\cdot\xvec}=1$). What is left is a purely atomic matrix element. Similarly, the first matrix element in {eq}`eq-photscatt-26` is interpreted as

:::{math}
:label: eq-photscatt-30
\matrixelement{n}{K_1}{k} = \matrixelement{B\lambda'}{K_1}{I} = {e\over mc}\sqrt{2\pi\hbar c^2\over \ds V} {1\over\sqrt{\omega'}} \matrixelement{B}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}} {I}.
:::

Altogether, the contribution of case~I, that is, the Feynman diagram in {ref}`fig-photscatt-2`, to the sum {eq}`eq-photscatt-26` is

:::{math}
:label: eq-photscatt-31
\Bigl({e^2\over m c^2}\Bigr) \Bigl({2\pi\hbar c^2\over V}\Bigr) {1\over\sqrt{\omega\omega'}} {1\over m\hbar}\sum_I {\matrixelement{B}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A} \over \omega-\omega_{IA}}.
:::

Similarly, we find the contribution of case~II, that is, the Feynman diagram in {ref}`fig-photscatt-3`. It works out to be

:::{math}
:label: eq-photscatt-32
\Bigl({e^2\over m c^2}\Bigr) \Bigl({2\pi\hbar c^2\over V}\Bigr) {1\over\sqrt{\omega\omega'}} {1\over m\hbar}\sum_I {\matrixelement{B}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{A} \over -\omega'-\omega_{IA}}.
:::

Putting the pieces together, the total transition amplitude {eq}`eq-photscatt-19` becomes

:::{math}
:label: eq-photscatt-33
c^eff_n(t) =  {2\over i\hbar} e^{i\omega_{ni} t/2} \Bigl( {\sin \omega_{ni}t/2 \over \omega_{ni}}\Bigr) \Bigl({e^2\over mc^2}\Bigr)\Bigl({2\pi\hbar c^2\over V}\Bigr) {1\over\sqrt{\omega\omega'}} M,
:::

where $M$ is an abbreviation,

:::{math}
:label: eq-photscatt-34
M={\hat{\boldsymbol{\epsilon}}}\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc} \, \delta_{BA} + {1\over m\hbar}\sum_I \left[ {\matrixelement{B}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A} \over \omega-\omega_{IA}} - {\matrixelement{B}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{A} \over \omega'+\omega_{IA}}\right].
:::

Note that $M$ is dimensionless. Note also that the sum over intermediate atomic states $I$ must include states of the continuum; for these, the notation $\sum_I$ is an abbreviation for an integral over the continuous quantum numbers, as well as a sum over the discrete ones.

(sec-photscatt-10)=

## The Kramers-Heisenberg Formula

Let us fix the mode $\lambda$ of the incident photon, the initial and final atomic states $A$ and $B$, and the polarization $\mu'$ of the outgoing photon. Then the final state is $\ket{n}=\ket{B\lambda'}$, in which only the final wave vector $\kvec'$ of the outgoing photon is variable. We must sum the transition probabilities over a collection of final states to obtain the differential cross , exactly as we did in the simpler scattering problems considered in {ref}`ch-tdpt`.

Let ${\hat{\mathbf{n}}}_f$ be a chosen direction for the outgoing photon, and let us construct a small cone of solid angle $\Delta\Omega'$ about this direction, as in Fig.~\figr\tdpt.5. The prime on $\Omega'$ means that it is a solid angle referring to the outgoing photon. Let us also define $k'_f$ as the magnitude of $\kvec'$ as determined by conservation of energy, that is,

:::{math}
:label: eq-photscatt-35
k'_f = {\omega'\over c} = {\omega-\omega_{BA}\over c},
:::

which follows from $\omega_{ni}=0$ [see {eq}`eq-photscatt-4`].

The differential cross $d\sigma/d\Omega'$, for fixed values of $\lambda=(\kvec,\mu)$, $A$, $B$ and $\mu'$, is the transition probability per unit time per unit solid angle $\Omega'$ of the outgoing photon per unit incident flux of the incoming photon for transitions in which $\kvec'$ lies in the small cone just described, in the limit that time is long enough for the initial transients to die away. We also take $V\to\infty$ to get rid of the box and to obtain physical results. That is, we can write

:::{math}
:label: eq-photscatt-36
{d\sigma\over d\Omega'} = \lim_{t\to\infty} \lim_{V\to\infty} {1\over J_inc} {1\over \Delta\Omega'} {1\over t} \sum_{\kvec'\in cone} |c^eff_{B\lambda'}(t)|^2.
:::

As we have done in {ref}`ch-tdpt`, we sum over all wave vectors $\kvec'$ in the small cone, and do not try to enforce energy conservation by hand. Taking the factors in {eq}`eq-photscatt-36` one at a time, the incident flux of photons is $J_inc=c/V$, since there is one incident photon in the box travelling at the speed of light. The sum over final photon states $\kvec'$ becomes an integral in the limit $V\to\infty$,

:::{math}
:label: eq-photscatt-37
\sum_{\kvec'\text{in cone}} \to {V\over (2\pi)^3} \int_cone d^3\kvec' = {V\over (2\pi)^3} \Delta\Omega' \int_0^\infty k^{\prime 2}\,dk' = {V\over (2\pi)^3} {\Delta\Omega'\over c^3} \int_0^\infty \omega^{\prime 2}\,d\omega'.
:::

Finally, the square of the transition amplitude {eq}`eq-photscatt-33` becomes

:::{math}
:label: eq-photscatt-38
|c^eff_{B\lambda'}(t)|^2 = {2\pi t\over\hbar^2} \,\Delta_t (\omega_{BA}+\omega'-\omega) \Bigl({e^2\over m}\Bigr)^2 \Bigl({2\pi\hbar\over V}\Bigr)^2 {1\over\omega\omega'} |M|^2.
:::

where we have used {eq}`eq-tdpt-46`. The matrix element $M$ depends on $\kvec'$ because it contains the polarization vectors $\epsilon' =\epsilon_{\lambda'} =\epsilon_{\kvec'\mu'}$. The direction of $\kvec'$ is determined by the cone, that is, the choice of ${\hat{\mathbf{n}}}_f$.

Putting the pieces together, we find

:::{math}
:label: eq-photscatt-39
{d\sigma\over d\Omega'} = {1\over c^4} \int_0^\infty \omega^{\prime 2}\,d\omega'\, {1\over\hbar^2} \,\delta(\omega_{BA}+\omega'-\omega)\, {1\over \omega\omega'}{e^4\hbar^2\over m^2} |M|^2,
:::

or, upon doing the integral,

:::{math}
:label: eq-photscatt-40
{d\sigma\over d\Omega'}=r_e^2 \,{\omega'\over\omega} |M|^2,
:::

where

:::{math}
:label: eq-photscatt-41
r_e={e^2\over mc^2} = 2.82\times 10^{-13}cm
:::

and where in the final expression it is understood that $\kvec'=k'_f {\hat{\mathbf{n}}}_f$, since the direction of $\kvec'$ is fixed by the small cone and the magnitude by the energy-conserving $\delta$-function. Also, $\omega'=\omega-\omega_{BA}$ is determined by energy conservation. {eq}`eq-photscatt-40`, with $M$ given by {eq}`eq-photscatt-34`, is the *Kramers-Heisenberg* formula. It was first derived by methods of the old quantum theory, and is important historically because the calculation led Heisenberg to realize that a fundamental difference between classical mechanics and quantum mechanics is that in quantum mechanics classical observables are replaced by noncommuting operators. (Heisenberg thought of these operators as matrices, hence the name “matrix mechanics” for the first version of quantum mechanics).

The quantity $r_e$ is called the *classical radius of the electron*. It is called “classical” because the expression does not involve $\hbar$ and because it has a classical interpretation: it is the radius outside of which the integrated energy in the electric field of the electron, $\int E^2/8\pi$, is equal to the rest-mass-energy $E=mc^2$ of the electron (apart from constants of order unity). At one point physicists were playing with the idea that the observed mass of the electron might be purely energy in the field. This idea was not very successful, however, and later developments in quantum electrodynamics showed that it was rather naive. However, the general idea points to a paradox of classical electromagnetism, namely, the total integrated energy of the electric field of a point particle, if it is carried all the way to $r=0$ and if Coulomb's law is valid all the way to $r=0$, is infinite. As we shall see when we study the Lamb shift, the quantum theory also leads (nominally) to an infinite mass of the electron. In addition to the infinite zero-point energy, it is one of the infinities that appear in quantum field theory.

In any case, the cross-{eq}`eq-photscatt-40` is proportional to

:::{math}
:label: eq-photscatt-42
r_e^2= \alpha^4 a_0^2,
:::

where $a_0$ is the Bohr-radius. Since $\alpha^4\approx 3\times 10^{-9}$ this is a very small area by atomic standards. The geometrical cross of the atom is roughly $\pi a_0^2$, and this is roughly the cross for the scattering of electrons of several eV of energy by an atom. But quantity $r_e^2$, which sets the scale for photon scattering, is much smaller.

Can the dimensionless quantity $|M|^2$ enhance the cross for photon scattering? One can see from the definition {eq}`eq-photscatt-34` that all quantities appearing there are of order unity in atomic units, if the states $\ket{A}$ and $\ket{B}$ have reasonably small quantum numbers. If, however, one of the denominators should be small, then $M$ can be large and lead to an enhancement. In fact, the denominator in the first term in {eq}`eq-photscatt-34` is small if $\omega\approx\omega_{IA}$, that is, if the incident photon has the right energy to raise the atom from its initial state $\ket{A}$ to an intermediate state $\ket{I}$. This intermediate state must be higher in energy, since $\omega>0$. If this is the case, the incident photon is in resonance with one of the excitation frequencies of the atom. Similar interpretations can be given to the second term, although in that term the outgoing photon is emitted before the incident photon is absorbed, as indicated by the Feynman diagram in {ref}`fig-photscatt-3`.

If $\omega$ is chosen so that there are no resonances (none of the denominators in {eq}`eq-photscatt-34` is small) then the cross-for atom-photon scattering is comparable to $r_e^2$, and is very small by atomic standards. This is why ordinary gases are transparent to radiation at optical frequencies, unless very thick.

We will now examine the Kramers-Heisenberg formula in various special and limiting cases.

(sec-photscatt-11)=

## Elastic Scattering

First we examine elastic scattering, in which the final atomic state is the same as the initial, that is, $B=A$. This means that $\omega'=\omega$ (the final photon energy is the same as the initial photon energy), so the Kramers-Heisenberg formula simplifies a little,

:::{math}
:label: eq-photscatt-43
\dod{\sigma}{\Omega'} = r_e^2 |M|^2,
:::

where now

:::{math}
:label: eq-photscatt-44
M={\hat{\boldsymbol{\epsilon}}}\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc} + {1\over m\hbar}\sum_{I\ne A} \left[ {\matrixelement{A}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A} \over \omega-\omega_{IA}} - {\matrixelement{A}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}})}{I} \matrixelement{I}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{A} \over \omega+\omega_{IA}}\right] \quad (elastic).
:::

We have excluded the term $I=A$ from the sum because it vanishes anyway.

In this case it is possible to combine the first (seagull) term with the other two terms. This involves some reverse engineering or unsimplifying to make the first term look like the others. In the first step we use the identity, $\delta_{ij} = (1/i\hbar)(x_ip_j-p_jx_i)$ to write the first term of {eq}`eq-photscatt-44` as

:::{math}
:label: eq-photscatt-45
\begin{aligned}
{\hat{\boldsymbol{\epsilon}}}\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc} &= \sum_{ij} \matrixelement{A}{\epsilon_i \epsilon^{\prime\cc}_j \, \delta_{ij}}{A}= {1\over i\hbar}\sum_{ij} \matrixelement{A}{\epsilon_i\epsilon^{\prime\cc}_j( x_ip_j - p_jx_i)}{A} \\
&={1\over i\hbar}\bigl[\matrixelement{A}{(\xvec\cdot{\hat{\boldsymbol{\epsilon}}}) (\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{A} -\matrixelement{A}{(\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}) (\xvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A}\bigr] \\
&={1\over i\hbar}\sum_{I\ne A}\bigl[ \matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} \matrixelement{I}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A} -\matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A}\bigr], \\

\end{aligned}
:::

where in the last step we have introduced a resolution of the identity and excluded the term $I=A$ since it vanishes anyway. Next we use the identity,

:::{math}
:label: eq-photscatt-46
\pvec={m\over i\hbar}[\xvec,K_0],
:::

where $K_0$ is given by {eq}`eq-photscatt-5a` and only the atomic part is relevant. This is essentially the Heisenberg equation of motion for $\xvec$, using $K_0$ as the Hamiltonian, and it allows us to convert matrix elements in $\pvec$ to those in $\xvec$ or vice versa, as we did in {ref}`sec-radnmatt-8`. In the present problem it allows us to write

:::{math}
:label: eq-photscatt-47
\matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} = {\matrixelement{A}{(\xvec K_0-K_0\xvec)\cdot{\hat{\boldsymbol{\epsilon}}}}{I} \over E_I-E_A}= {i\over m} {\matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I}\over \omega_{IA}},
:::

where we have used the fact that $\ket{A}$ and $\ket{I}$ are eigenstates of $K_0$. Similarly we have

:::{math}
:label: eq-photscatt-48
\matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A} = -{i\over m} {\matrixelement{I}{\pvec\cdot\epsilonvec}{A} \over \omega_{IA}},
:::

obtained by swapping the labels $A$ and $I$.

Combining {eq}`eq-photscatt-47` and {eq}`eq-photscatt-48` with {eq}`eq-photscatt-45`, we obtain

:::{math}
:label: eq-photscatt-49
{\hat{\boldsymbol{\epsilon}}}\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}= {1\over m\hbar}\sum_{I\ne A} \left[ {\matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I} \matrixelement{I}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A} \over \omega_{IA}} +{\matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} \matrixelement{I}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A} \over \omega_{IA}} \right].
:::

This allows us to combine the terms in {eq}`eq-photscatt-44` to obtain

:::{math}
:label: eq-photscatt-50
M = {\omega\over m\hbar}\sum_{I\ne A}{1\over\omega_{IA}} \left[{\matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I} \matrixelement{I}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A} \over \omega-\omega_{IA}} + {\matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} \matrixelement{I}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A} \over \omega+\omega_{IA}}\right]\quad (elastic).
:::

Finally, let us use the commutator {eq}`eq-photscatt-46` convert matrix elements in $\pvec$ into matrix elements in $\xvec$. The conversions

:::{math}
:label: eq-photscatt-51
\begin{aligned}
 \matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} &= -im\,\omega_{IA} \matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I}, \qquad \matrixelement{A}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I} = -im\,\omega_{IA} \matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I},\\  \matrixelement{I}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A} &= im\,\omega_{IA} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A}, \qquad \matrixelement{I}{\pvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A} = im\,\omega_{IA} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A}.\\ 
\end{aligned}
:::

With these, {eq}`eq-photscatt-50` becomes

:::{math}
:label: eq-photscatt-52
M={m\omega\over\hbar}\sum_{I\ne A}\omega_{IA}\left[ {\matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A} \over \omega-\omega_{IA}} + {\matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A} \over \omega+\omega_{IA}}\right] \quad (elastic).
:::

(sec-photscatt-12)=

## Low Frequency Elastic Scattering

So far we have transformed the quantity $M$ for elastic scattering without approximation. Now, however, let us consider the case in which the frequency of the incident photon is small compared to any resonance frequency $\omega_{IA}$. For example, if $\ket{A}$ is the ground state of the atom, this means that $\hbar\omega$ is small compared to the energy needed to raise the atom into the first excited state. Then we can expand the the quantity $M$ in {eq}`eq-photscatt-52` in powers of $\omega/\omega_{IA}$. The $\omega$-dependent terms in {eq}`eq-photscatt-52` are

:::{math}
:label: eq-photscatt-53
{\omega_{IA}\over\omega\pm\omega_{IA}} \approx \pm 1- {\omega\over\omega_{IA}}.
:::

The contribution of the constant term in this expansion to the sum {eq}`eq-photscatt-52` is

:::{math}
:label: eq-photscatt-54
\sum_{I\ne A} \bigl[-\matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A} +\matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A}\bigr].
:::

We can restore the term $I=A$ into this sum since it vanishes anyway and obtain a resolution of the identity $\sum\ketbra{I}{I}$ over atomic states. Thus the sum {eq}`eq-photscatt-54` becomes

:::{math}
:label: eq-photscatt-55
-\matrixelement{A}{(\xvec\cdot{\hat{\boldsymbol{\epsilon}}}) (\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc})}{A} +\matrixelement{A}{(\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}) (\xvec\cdot{\hat{\boldsymbol{\epsilon}}})}{A}=0.
:::

The constant term in the expansion {eq}`eq-photscatt-53` vanishes when used in the sum. Going to next order in $\omega/\omega_{IA}$ we have

:::{math}
:label: eq-photscatt-56
M={m\omega^2\over\hbar}\sum_{I\ne A}{1\over\omega_{IA}} \bigl[ \matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{I} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{A}+ \matrixelement{A}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}}{I} \matrixelement{I}{\xvec\cdot{\hat{\boldsymbol{\epsilon}}}}{A} \bigr] \quad \\text{elastic, \omega\ll\omega_{IA}}.
:::

In this form we can see the induced dipole moment tensor of the atom in the presence of the light wave. See {eq}`eq-stark-31` for the polarizability of hydrogen in the presence of a static (DC) electric field (that is, in the Stark effect). The physics is that the incident light wave produces an induced electric dipole moment in the atom, oscillating at the same frequency as the wave, which radiates the scattered wave. In fact, much of the process can be understood classically.

For now the important fact is that the amplitude $M$ is proportional to $\omega^2$, so the cross is proportional to $\omega^4$. This dependence of the cross on frequency was first derived by Raleigh in his study of light scattering by small particles, so the process is called *Rayleigh scattering*. When sunlight passes through the atmosphere the higher frequency blue light is more strongly scattered than the longer wavelengths, which explains why the sky is blue. It also explains why sunsets are red, since the sunlight passing through thick layers of atmosphere has its higher frequencies depleted by Raleigh scattering and mainly the red light gets through.

(sec-photscatt-13)=

## Thomson Scattering

Let us now consider the opposite limit, in which $\omega$ is much larger than any atomic transition frequency. This may look absurd since we sum over all intermediate states $I$ going out to arbitrarily high energies. However, the matrix elements in {eq}`eq-photscatt-34` are small when the intermediate state $I$ has large quantum numbers compared to those of the states $A$ and $B$ (which we assume are small). In this limit both terms in the sum in {eq}`eq-photscatt-34` have large denominators and become negligible compared to the first (seagull) term. Specializing to elastic scattering, in this limit the Kramers-Heisenberg formula becomes simply

:::{math}
:label: eq-photscatt-57
\dod{\sigma}{\Omega'} = r_e^2\, |{\hat{\boldsymbol{\epsilon}}}\cdot{\hat{\boldsymbol{\epsilon}}}^{\prime\cc}|^2.
:::

The physics here is that if the energy of the incident photon is much higher than the binding energy of the electron, then the electron behaves as if it were free and not attached to the atom at all. In fact, the cross-{eq}`eq-photscatt-57` applies to the scattering of photons by free electrons, which is called *Thomson scattering*. The area $r_e^2$ is the characteristic size of the Thomson cross-.

However, our derivation is limited by the fact that we are using nonrelativistic quantum mechanics, so the validity of the Thomson cross-is limited by $\hbar\omega \ll mc^2$, where $m$ is the electron mass. If the photon is relativistic in the sense $\hbar\omega$ is comparable to or greater than $mc^2$, then the process is called *Compton scattering* and the cross-, which is more complicated than the Thomson formula {eq}`eq-photscatt-57`, is called the *Klein-Nishina* cross-.

Notice that the Thomson cross does not depend on the spin of the electron. That is because we used the electrostatic model in its derivation, as well as the dipole approximation (ignoring spin-dependent terms etc). In the Klein-Nishina formula there is a dependence on the electron spin.

An interesting feature of Thomson scattering is that even if the incident photon is unpolarized, the scattered photon has a net polarization. In fact, for certain scattering angles, it is in a pure polarization state.

(sec-photscatt-14)=

## Raman Scattering

Raman scattering is an example of inelastic scattering, which we describe in broad terms.

A typical example consists of passing optical radiation, for example, a laser beam, through a molecular gas. A detector collects photons scattered by the beam at various angles. If the frequency of the optical radiation is $\omega$, then most of the scattered photons also have frequency $\omega$, that is, the scattering is elastic. But typically one also detects a smaller number of photons that have been downshifted or upshifted in frequency by some amount $\Delta\omega$. If the scattered photon has a lower frequency than the incident photons, it means the photon has given up some energy to the molecule, typically raising it into a higher vibrational state; conversely, if scattered photon is upshifted in frequency then it has gained energy from the molecule, which has made a transition to a lower vibrational state. If the vibrational mode in question is approximated by a harmonic oscillator, then $\Delta\omega$ is the vibrational frequency and $\hbar\Delta\omega$ is the change in vibrational energy when the quantum number $n$ of the harmonic oscillator changes by 1. If the molecule is a diatomic then it has only one vibrational mode, as explained in {ref}`sec-cenforce-11`, but polyatomic molecules have more than one vibrational mode. Section {ref}`sec-cenforce-11` also explaines that vibrational frequencies are typically down by a factor of roughly 100 in comparison to optical frequencies, so this is a measure of $\Delta\omega/\omega$ in such experiments. In this way the frequency shifts of the scattered photons give direct experimental information on the vibrational energy levels of the molecule.

The spectral lines that are shifted down from the incident frequency $\omega$ are called *Stokes lines*, and those that are shifted up are called *anti-Stokes lines*. In practice Stokes lines tend to be stronger than anti-Stokes lines because the Boltzmann factor suppresses the populations of higher vibrational states. For example, if the gas is at a low enough temperature that almost all the vibrational modes are in the ground state, then one will see only Stokes lines.

\problems

(prob-photscatt-1)=

**Problem \prbdphotscatt-1.} This is a variation on Sakurai, *Advanced Quantum Mechanics.** 

Consider the $2s \to 1s$ transition in hydrogen. The matrix elements for single photon emission are very small, so ignore them, and consider the emission of two photons. This in fact is the dominant mechanism for the $2s \to 1s$ decay. It is sufficient to use the electrostatic model (ignore the spin of the electron, the fine structure, etc), so the atomic states are $\ket{n\ell m*}$. Use the Hamiltonian $K=K_0+K_1+K_2$, given by {eq}`eq-photscatt-5a`, with $U(r)=-e^2/r$ so that it applies to hydrogen, and drop the spin-dependent term in $K_1$. Also use the dipole approximation, so $e^{i\kvec\cdot\xvec}=1$. See {eq}`eq-photscatt-17` for the effective transition amplitude in second order time-dependent perturbation theory. Remember that $H_1$ in must be identified with $K_1 + K_2$ in our application. Let $B$ stand for the $2s$ state, $A$ for the $1s$ state, and $I$ for an intermediate state. Obtain an expression for the differential transition rate,

:::{math}
:label: eq-photscatt-58
{ dw \over d\omega \,d\Omega \, d\Omega'},
:::

defined by saying that

:::{math}
:label: eq-photscatt-59
{ dw \over d\omega \,d\Omega \, d\Omega'} \Delta \omega \, \Delta \Omega \, \Delta \Omega'
:::

is the probability per unit time for two photons to be emitted with frequencies $\omega$, $\omega'$, with $\omega+\omega'=\omega_{BA} = (E_B-E_A)/\hbar$, with $0 \le \omega \le \omega_{BA}/2$, with $\omega$ lying in a small interval $\Delta \omega$, and with wave vectors $\kvec$, $\kvec'$ lying in two small cones of solid angles $\Delta \Omega$ and $\Delta \Omega'$. You can write your answer in the style we used for the Kramers-Heisenberg formula, {eq}`eq-photscatt-40`, with the cross proportional to the square of a certain amplitude, which you should define. The answer is a function of $\omega$ and the directions and polarizations of the two outgoing photons. Good advice is to use atomic units (it is much easier).

Indicate which intermediate states contribute to the sum. Simplify the expression as far as you can. This is a challenge to see how far you can go with the simplification. Hint: if you simplify enough, then it is easy to sum over polarizations and integrate over the solid angles of both photons, leaving behind only an integral over $\omega$ to get the total transition rate. This problem is relatively simple for a two-photon process, since the initial and final atomic states are rotationally invariant.

(prob-photscatt-2)=

**Problem \prbdphotscatt-2..** 

(prob-photscatt-3)=

**Problem \prbdphotscatt-3.}  When we direct photons at an atom, we can choose the frequency of the incident photon $\omega$ to be anything we want.   Depending on the atomic states $\ket{A}$ and $\ket{B.** 

\problempart{(a)} Show that if the first term is resonant, then the intermediate state }$I$ must be higher in energy than both states $\ket{A}$ and $\ket{B}$. Show that if $\omega$ is resonant with an atomic transition, then so is $\omega'$. Is there any necessary relation between $E_A$ and $E_B$ (must one be higher than the other, or vice versa)? What states $A$ and $B$ would you choose and what frequency $\omega$ if you wanted to guarantee that the first term could not be resonant for any $I$?

\problempart{(b)} Show that if the second term is resonant, then the intermediate state $I$ must be lower in energy than both states $\ket{A}$ and $\ket{B}$. Show that if the second term is resonant for some $\omega$, $A$ and $B$, then both $\omega$ and $\omega'$ are resonant with some atomic transition. Is there any necessary relation between $E_A$ and $E_B$ (must one be higher than the other, or vice versa)? What states $A$ and $B$ would you choose and what frequency $\omega$ if you wanted to guarantee that the second term in {eq}`eq-photscatt-34` could not be resonant for any $I$?
