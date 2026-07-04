---
title: "42. Emission and Absorption of Radiation"
---
(ch-radnmatt)=

# 42. Emission and Absorption of Radiation

(sec-radnmatt-1)=

## Introduction

In these notes we will examine some simple examples of the interaction of the quantized radiation field with matter. We will mostly be concerned with the emission and absorption of radiation by atoms. With minor changes, our results also apply to molcules, nuclei, and other material systems. The scattering of radiation by matter is treated in {ref}`ch-photscatt`. These notes continue with the notation for description of the electromagnetic field and its modes that was developed in {ref}`ch-classemf` and {ref}`ch-quantemf`. These notes also make use of the notation developed in {ref}`ch-tdpt` (on time-dependent perturbation theory), in which $\ket{i}$ is an initial state and $\ket{n}$ is a variable final state that we must sum over to get physical transition rates. In these notes these initial and final states are identified with specific states of the matter-field system, depending on the problem under consideration.

(sec-radnmatt-2)=

## Hamiltonian for Matter Plus Radiation

We begin with the Hamiltonian for the combined matter-field system,

:::{math}
:label: eq-radnmatt-1
H=H_matter + H_em,
:::

which is a quantized version of the classical Hamiltonian presented in \classemf.16. The quantized field Hamiltonian was presented in {eq}`eq-quantemf-16`, which we reproduce here,

:::{math}
:label: eq-radnmatt-2
H_em = \sum_\lambda \hbar\omega_k \, a^\hc_\lambda a_\lambda,
:::

where we use box normalization. The classical matter Hamiltonian was presented in {eq}`eq-classemf-97`, which we reinterpret as a quantum operator and augment with terms for spins interacting with the magnetic field,

:::{math}
:label: eq-radnmatt-3
H_matter = \sum_\alpha {1\over 2m_\alpha} \Bigl[ \pvec_\alpha - {q_\alpha\over c} \Avec(\rvec_\alpha) \Bigr]^2 + \sum_{\alpha<\beta} {q_\alpha q_\beta \over |\rvec_\alpha - \rvec_\beta|} - \sum_\alpha \muvec_\alpha\cdot\Bvec(\rvec_\alpha).
:::

In this Hamiltonian, indices $\alpha$, $\beta$, etc label the particles, whose positions and momenta are $\rvec_\alpha$ and $\pvec_\alpha$. These are taken as operators with the usual commutation relations. The vector $\muvec_\alpha$ is the magnetic moment of particle $\alpha$, related to the spin in the usual way. The spin-dependent terms are exactly the ones we have always used, except that now the magnetic field $\Bvec$ itself is quantized.

When it is necessary to refer to an arbitrary field point at which a field is evaluated, we will write it as $\xvec$. This is not an observable, rather the observable is the field itself, for example, $\Bvec(\xvec)$ is a different (vector) observable for each value of $\xvec$. However, in many cases a field is evaluated at a particle position $\rvec_\alpha$, which is an observable.

The total Hamiltonian {eq}`eq-radnmatt-1` involves both the matter and field degrees of freedom, and acts on the total ket space

:::{math}
:label: eq-radnmatt-4
\ES = \ES_matter \otimes \ES_em,
:::

where $\ES_em$ is the ket space for the field (a Fock space) described in {ref}`ch-quantemf`, and where $\ES_matter$ is the usual ket space for nonrelativistic particles, possibly with spin.

Most of the following discussion works for any nonrelativistic system (atom, molecule, nucleus, nanotube, solid), but when it is necessary to be specific, we will for simplicity take the matter Hamiltonian to be that of a single-electron atom with an effective central force potential,

:::{math}
:label: eq-radnmatt-5
H_matter = {1\over 2m}\Bigl[\pvec+{e\over c}\Avec(\rvec) \Bigr]^2 + U(r) + {e\over mc} \Svec\cdot\Bvec(\rvec),
:::

where we write the potential as $U$ to avoid confusion with the volume of the box $V$. In this Hamiltonian we assume for simplicity that the nucleus is infinitely massive, and we set $q=-e$ and $g=2$ for the electron charge and $g$-factor. This Hamiltonian is not a special case of the Hamiltonian {eq}`eq-radnmatt-3`, but can be derived from it in a certain approximation (see Prob.~\prbrradnmatt-4).

The total Hamiltonian, including the matter and field terms, is complicated, and cannot be solved exactly even in simple models. Therefore we must resort to perturbation theory. We begin by expanding the total Hamiltonian into three terms, $H=H_0+H_1+H_2$, where

:::{math}
\begin{aligned}
H_0 &= {\pvec^2\over 2m} + U(r) + \sum_\lambda \hbar\omega_k \, a^\hc_\lambda a_\lambda,
\end{aligned}
:::

:::{math}
\begin{aligned}
H_1 &= {e\over mc}\bigl[ \pvec\cdot\Avec(\rvec) + \Svec\cdot\Bvec(\rvec) \bigr],
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-6
\begin{aligned}
H_2 &= {e^2\over 2mc^2} \Avec(\rvec)^2,
\end{aligned}
:::

which is basically an expansion in the coupling between the matter and the field. This Hamiltonian represents the interaction of a single-electron atom with an electromagnetic field. It turns out that as an order of magnitude, $H_1\ll H_0$ and $H_2\ll H_1$ if the electric fields associated with the light waves are small in comparison to the electric fields felt by the electron due to the nucleus, that is, if $E_wave \ll E_nucleus$. This is easiest to see if the fields $\Avec$, $\Bvec$ are treated as classical ($c$-number) fields, representing a light wave, but the same estimates follow from the quantized fields. In most practical situations, this condition is met; however, in certain modern experiments involving high intensity laser light, this condition is not met, and different approximation methods must be used. In our initial applications, we will be doing first order perturbation theory, and we will be able to neglect $H_2$; but in second order calculations it is necessary to treat terms involving both $H_1^2$ and $H_2$.

We note that the unperturbed Hamiltonian $H_0$ in {eq}`eq-radnmatt-6` is the sum of a Hamiltonian for the matter and one for the field, with no interaction. This Hamiltonian is therefore solvable, and the unperturbed eigenkets are simply tensor products of atomic eigenkets with field eigenkets. Denoting the states of the atom by capital letters such as $\ket{X}$, we can write a typical eigenstate of $H_0$ in the form $\ket{X} \ket{\ldots n_\lambda \dots}$.

(sec-radnmatt-3)=

## Spontaneous Emission

Our first application will be the spontaneous emission of a photon by an atom in an excited state. We will use box normalization for this calculation. Let $\ket{A}$ and $\ket{B}$ be two discrete (bound) states of the atom, with $E_A < E_B$, and suppose at $t=0$ the atom is in the upper state $\ket{B}$. Suppose furthermore that at $t=0$ the electromagnetic field is in the vacuum state $\ket{0}$ (with no photons). We will be interested in time-dependent transitions to the state in which the atom is in the lower state $\ket{A}$, and a photon has been emitted, so that the field contains one photon. Since the wave vector $\kvec$ of the outgoing photon in the final state is continuously variable (after $V\to\infty$), we have an example of a time-dependent perturbation problem with a continuum of final states.

The initial state is a tensor product of the atomic state $\ket{B}$ with the vacuum state $\ket{0}$ for the field,

:::{math}
:label: eq-radnmatt-7
\ket{i} = \ket{B}\ket{0}=\ket{B0},
:::

with an energy $E_i=E_B$ (the energy of the atomic state $B$). The final state, denoted $\ket{n}$ in the general notation of {ref}`ch-tdpt`, is the tensor product of the atomic state $\ket{A}$ with a state of the field in which there is one photon in mode $\lambda$. We will write this state in various ways,

:::{math}
:label: eq-radnmatt-8
\ket{n} = \ket{A} a^\hc_\lambda \ket{0}=\ket{A}\ket{\lambda} =\ket{A\lambda}.
:::

The energy of the final state is $E_n= E_A + \hbar\omega_k$, where the $k$-subscript on $\omega_k$ is understood to refer to the $k$ contained in $\lambda=(\kvec,\mu)$. The Einstein frequency is

:::{math}
:label: eq-radnmatt-9
\omega_{ni} = {\hbar\omega_k -(E_B - E_A) \over \hbar} = \omega_k - \omega_{BA} = c(k-k_{BA}),
:::

where $\omega_{BA}$ and $k_{BA}$ are respectively the frequency and wavenumber associated with the energy difference $E_B-E_A$.

According to time-dependent perturbation theory [see {eq}`eq-tdpt-36`], the transition amplitude from initial state $\ket{i}$ to final state $\ket{n}$ in first order perturbation theory is

:::{math}
:label: eq-radnmatt-10
c_n(t) = {2\over i\hbar}\, e^{i\omega_{ni}t/2} \, {\sin(\omega_{ni}t/2)\over \omega_{ni}} \, \matrixelement{n}{H_1}{i},
:::

where for our problem $\omega_{ni}$ is given by {eq}`eq-radnmatt-9`. The term $\delta_{ni}$ present in the general formula {eq}`eq-tdpt-30` vanishes since for our problem $n\ne i$ (the initial and final states have different numbers of photons). The square of the transition amplitude is the transition probability,

:::{math}
:label: eq-radnmatt-11
P_n(t)={2\pi t\over \hbar^2}\, \Delta_t(\omega_{ni}) |\matrixelement{n}{H_1}{i}|^2,
:::

where we have used {eq}`eq-tdpt-46`.

We work first on the matrix element. According to {eq}`eq-radnmatt-7`, {eq}`eq-radnmatt-8`, and {eq}`eq-radnmatt-6`, we have

:::{math}
:label: eq-radnmatt-12
\matrixelement{n}{H_1}{i} = {e\over mc} \bra{A} \bra{0} a_\lambda \bigl[ \pvec\cdot\Avec(\rvec) + \Svec\cdot\Bvec(\rvec) \bigr]  \ket{B} \ket{0},
:::

where $\Avec(\rvec)$ and $\Bvec(\rvec)$ are the quantized fields, given in box-normalization form by {eq}`eq-quantemf-22` and {eq}`eq-quantemf-24`, but here evaluated at the particle position $\rvec$. The general structure of these equations is that both $\Avec$ and $\Bvec$ consist of a Fourier series involving both annihilation and creation operators. That is, both fields have the form

:::{math}
:label: eq-radnmatt-13
\Avec, \Bvec \sim \sum_{\lambda'} \bigl( \ldots a_{\lambda'} \ldots a^\hc_{\lambda'} \ldots \bigr),
:::

where all inessential factors are suppressed and where we use $\lambda'$ as the dummy index of summation to avoid confusion with the $\lambda$ which represents the mode of the outgoing photon. Now we can see that all annihilation operators $a_{\lambda'}$ give zero, since they act on the vacuum $\ket{0}$ to the right in {eq}`eq-radnmatt-12`. As for the creation operators $a^\hc_{\lambda'}$, these all give zero, too, except for the one term $\lambda'=\lambda$ in the $\lambda'$ sum, because the operator $a^\hc_{\lambda'}$ must create a photon that is then destroyed by the operator $a_\lambda$ to the left in {eq}`eq-radnmatt-12`. In other words, the field matrix element has the form,

:::{math}
:label: eq-radnmatt-14
\matrixelement{0}{a_\lambda a^\hc_{\lambda'}}{0} = \delta_{\lambda\lambda'},
:::

as follows from the commutation relations {eq}`eq-quantemf-6`. Therefore the field scalar product kills the sum in {eq}`eq-radnmatt-13`, leaving behind the factors $\epsilon^\cc_\lambda \, e^{-i\kvec\cdot\rvec}$.

After the field scalar product has been taken, the matrix element is reduced to

:::{math}
:label: eq-radnmatt-15
\matrixelement{n}{H_1}{i} = {e\over mc} \sqrt{2\pi\hbar c^2\over V} {1\over \sqrt{\omega_k}} \matrixelement{A}{\bigl[\pvec\cdot\epsilonvec^\cc_\lambda -i\Svec\cdot(\kvec\cross\epsilonvec^\cc_\lambda)\bigr] e^{-i\kvec\cdot\rvec}}{B}.
:::

Only an atomic matrix element remains, which we abbreviate by the definition,

:::{math}
:label: eq-radnmatt-16
M_{BA} =  {i\over\hbar} \matrixelement{B}{\bigl[\pvec\cdot\epsilonvec_\lambda +i\Svec\cdot(\kvec\cross\epsilonvec_\lambda)] e^{i\kvec\cdot\rvec}}{A},
:::

so that

:::{math}
:label: eq-radnmatt-17
\matrixelement{n}{H_1}{i} = {e\over mc} \sqrt{2\pi\hbar c^2\over V} {1\over \sqrt{\omega_k}} \, i\hbar M^\cc_{BA}.
:::

In manipulating $M_{BA}$, it is useful to note that $\epsilonvec\cdot\pvec$ commutes with $e^{i\kvec\cdot\rvec}$, because of the transversality condition $\epsilonvec\cdot\kvec=0$. The matrix element $M_{BA}$ depends on the quantum numbers of the atomic states $A$ and $B$, and on the mode $\lambda=(\kvec,\mu)$ of the outgoing photon.

We will denote a transtion rate with the symbol $w$, indicating probability per unit time. When the atom emits a photon and drops into a lower state, the photon can go out into any of a number of final states, each with its own probability. Physically interesting results are obtained by summing these probabilities over collections of final states. In our case, let us choose a direction ${\hat{\mathbf{n}}}_f$ for the outgoing photon, and construct a small cone of solid angle $\Delta\Omega$ surrounding ${\hat{\mathbf{n}}}_f$, as in Fig.~\figr\tdpt.5. (In that figure, the cone referred to the direction of a scattered particle, whereas here it refers to the direction of the emitted photon.)

The quantity we are interested in is the probability per unit time per unit solid angle, for given initial atomic state $\ket{A}$ and final atomic state $\ket{B}$, and for given polarization $\mu$ of the final photon. We denote this quantity by $(dw/d\Omega)_\mu$, where $A$ and $B$ are understood. To obtain this we must take the time long enough that the probability is proportional to time, which means that it is long enough that $\Delta_t(\omega_{ni})$ can be replaced by $\delta(\omega_{ni})$. We also take $V\to\infty$ to get physical results. Thus, the differential transition rate is

:::{math}
:label: eq-radnmatt-18
\Bigl({dw\over d\Omega}\Bigr)_\mu = \lim_{t\to\infty} \lim_{V\to\infty} {1\over t} \, {1\over \Delta\Omega} \, \sum_{\kvec \in cone} {2\pi t\over\hbar^2} \, \Delta_t(\omega_{ni}) \, \Bigl({e\over mc}\Bigr)^2 {2\pi\hbar c^2\over V}\, {1\over \omega}\, \hbar^2 |M_{BA}|^2.
:::

In the large volume limit the sum can be replaced by an integral, just as in {eq}`eq-tdpt-76`. That is, we can make the replacement,

:::{math}
:label: eq-radnmatt-19
\sum_{\kvec\in cone} \to {V\over (2\pi)^3} \, \Delta\Omega \int_0^\infty k^2\,dk = {V\over (2\pi)^3} \, {\Delta\Omega\over c^3} \int_0^\infty \omega^2\,d\omega,
:::

where we have transformed the variable of integration from $k$ to $\omega=ck$. Putting the pieces together, we have

:::{math}
:label: eq-radnmatt-20
\Bigl({dw\over d\Omega}\Bigr)_\mu = {1\over 2\pi} \, {e^2\hbar\over m^2c^3} \int_0^\infty \omega \, d\omega\, \delta(\omega-\omega_{BA}) |M_{BA}|^2.
:::

The matrix element $M_{BA}$ depends on the wave vector $\kvec$ of the outgoing photon, but when we sum only over $\kvec$ in the small cone the direction of $\kvec$ is fixed by the direction ${\hat{\mathbf{n}}}_f$ of the cone.

On doing the integral we obtain the result,

:::{math}
:label: eq-radnmatt-21
\Bigl( \dod{w}{\Omega} \Bigr)_\mu = {1\over 2\pi} {e^2\over m^2 c^3} \hbar\omega |M_{BA}|^2,
:::

where now $\omega=\omega_{BA}$. Also, in this result the magnitude of $\kvec$ that appears in $M_{BA}$ is determined by conservation of energy, that is, it is given by $k=k_{BA}=\omega_{BA}/c$, so now $M_{BA}$ depends only on the two atomic states $A$ and $B$, and on the polarization $\mu$ and direction ${\hat{\mathbf{k}}}$ of the outgoing photon. {eq}`eq-radnmatt-21` gives us the intensity of the emitted radiation as a function of both photon polarization and direction. This result can be obtained from the semiclassical theory of radiation only in an ad hoc and convoluted manner, but it is perhaps the easiest calculation of quantum electrodynamics.

If we are only interested in the total rate of emission, regardless of direction or polarization, then we should sum the answer {eq}`eq-radnmatt-21` over $\mu$ and integrate over solid angle of the outgoing photon. For this purpose it is convenient to introduce an abbreviation,

:::{math}
:label: eq-radnmatt-22
\overline{|M_{BA}|^2} = {1\over 2} \sum_\mu {1\over 4\pi} \int d\Omega \, |M_{BA}|^2,
:::

which is the average of the square of the matrix element over polarizations and angles, and which depends only on the atomic states $A$ and $B$. In terms of this quantity, the total transition rate can be written,

:::{math}
:label: eq-radnmatt-23
w={4e^2 \over m^2 c^3} \hbar \omega \overline{|M_{BA}|^2} = A_E,
:::

where $A_E$ is the Einstein $A$ coefficient (defined to be the rate of spontaneous emission).

(sec-radnmatt-4)=

## Time Scales

This is a good point to examine the various time scales that appear in this derivation of the transition rate. First, the limit $t\to\infty$ that was used in passing from {eq}`eq-radnmatt-18` to {eq}`eq-radnmatt-20` was used to replace $\Delta_t(\omega-\omega_{BA})$ by $\delta(\omega-\omega_{BA})$. Without this replacement, the probability does not grow in proportion to time, and we do not have a transition rate. In fact, we do not literally take $t$ to infinity, we only need $t$ to be large enough that the function $\Delta_t(\omega-\omega_{BA})$ is narrow enough in $\omega$ that it behaves like a $\delta$-function under the integral in {eq}`eq-radnmatt-20`. As explained in {ref}`ch-tdpt`, at finite $t$ the function $\Delta_t$ has a width $\Delta\omega \sim 1/t$. Therefore the replacement will be valid if $\Delta\omega$ is much less than the frequency scale of the rest of the integrand in {eq}`eq-radnmatt-20`. The rest of the integrand is the factor $\omega |M_{BA}|^2$, which depends on $\omega$ mainly through the factor $\omega$. Thus we must have $\Delta \omega\ll\omega_{BA}$ as the condition for the replacement of $\Delta_t$ by a $\delta$-function. If the quantum numbers of atomic states $A$ and $B$ are not too large, then $\omega_{BA}$ is of the order of the orbital frequency of the electron, that is, it is of order 1 in atomic units. Thus the condition for the replacement becomes $t\gg 1$ in atomic units, that is, the time must be much larger than a single orbital period of the electron.

There are also limits on the validity of our result {eq}`eq-radnmatt-23` at long times. Let us denote the probability that the system remains in the initial state $\ket{i}=\ket{B0}$ by $P_i(t)$. In our analysis of time-dependent perturbation theory in {ref}`ch-tdpt`{} we did not examine the case $n=i$, but the probability to remain in the initial state must be 1 minus the probability to make a transition, by conservation of probability. That is, we must have

:::{math}
:label: eq-radnmatt-24
P_i(t) = 1-A_Et,
:::

according to our result {eq}`eq-radnmatt-23`.

:::{figure} images/radnmatt-fig01.png
:label: fig-radnmatt-1
:width: 80%

The prediction of first-order, time-dependent perturbation theory is that after time $t=1/A_E$, the probability of remaining in the initial state goes negative. A better approximation gives an exponential decay, but this requires a different theory, valid for longer times than we have considered.
:::

But this implies that the probability goes negative for times $t>1/A_E$, as illustrated by the dotted line in {ref}`fig-radnmatt-1`, so there must be something wrong with our theory at such long times. Therefore our theory can be valid only for times such that

:::{math}
:label: eq-radnmatt-25
1 \ll t \ll {1\over A_E},
:::

measured in atomic units. Physically, $t$ must be large compared to an orbital period and small compared to the lifetime of the excited state. As we will see in \secrradnmatt-9, $A_E$ is of order $\alpha^3\sim 10^{-6}$ in atomic units for electric dipole transitions in hydrogen, and even smaller for other types. Thus there is plenty of room for the condition {eq}`eq-radnmatt-25` on $t$ to be met. (In other systems or circumstances the conditions may not be so favorable.)

Our theory breaks down for times comparable to $1/A_E$ because our calculation of the transition probability in {ref}`ch-tdpt`{} did not take into account the depletion of probability from the initial state. To deal with the behavior atomic systems on a time scale comparable to or larger than $1/A_E$, more powerful techniques must be used than time-dependent perturbation theory. We will see the need for this later when we take up resonance fluorescence.

(sec-radnmatt-5)=

## Absorption of Radiation by Matter

Next we consider the process of absorption, in which the atom is initially in the lower state $\ket{A}$, from which it absorbs a photon from the field and gets lifted into the higher state $\ket{B}$ (both assumed to be discrete). Since the field must contain some photons if one is to be absorbed, we assume the initial state of the field is given by $\ket{\ldots n_\lambda \ldots}$, for some given list of occupation numbers $\{n_\lambda\}$. The atom can absorb a photon from any mode that initially has photons in it (but for long times, only those that nearly conserve energy will be important), so the state of the system after some time will be a linear combination of final states in which one of the modes has one fewer photon than in the initial state. In the following calculation, we let $\lambda$ stand for the mode from which a photon has been absorbed, so that effectively $\lambda$ also becomes a label of final states. That is, we take our initial and final states to be

:::{math}
:label: eq-radnmatt-26
\begin{aligned}
\ket{i} &= \ket{A} \ket{\ldots n_\lambda \ldots}, \\
\ket{n} &= \ket{B} \ket{\ldots,n_\lambda-1, \ldots}, \\

\end{aligned}
:::

where it is understood that all occupations numbers are identical in the initial and final states except in mode $\lambda$. The resonance frequency we will use is

:::{math}
:label: eq-radnmatt-27
\omega_{ni} = {E_B-E_A - \hbar\omega_k \over \hbar} =\omega_{BA}-\omega_k = c(k_{BA}-k),
:::

which is the same as the one we had for spontaneous emission except for the sign.

Now the matrix element has the form

:::{math}
:label: eq-radnmatt-28
\matrixelement{n}{H_1}{i} = {e\over mc} \bra{B} \bra{\ldots,n_\lambda-1,\ldots } \bigl[ \pvec\cdot\Avec(\rvec) + \Svec\cdot\Bvec(\rvec) \bigr]  \ket{A} \ket{\ldots n_\lambda \ldots},
:::

where again the general structure of $\Avec$ and $\Bvec$ is indicated by {eq}`eq-radnmatt-13`. We see now that the only term from the $\lambda'$ sum in {eq}`eq-radnmatt-13` that survives the field scalar product is the annihilation operator $a_{\lambda'}$ for $\lambda'=\lambda$, because this is the only operator that will lower the number of photons in mode $\lambda$ by one. Furthermore, we have

:::{math}
:label: eq-radnmatt-29
a_\lambda \ket{\ldots n_\lambda \ldots} = \sqrt{n_\lambda} \, \ket{\ldots,n_\lambda-1,\ldots},
:::

so after the field scalar product is taken, we are left with

:::{math}
\begin{aligned}
\matrixelement{n}{H_1}{i} &= {e\over mc} \sqrt{2\pi\hbar c^2\over V} {\sqrt{n_\lambda}\over \sqrt{\omega_k}} \matrixelement{B}{\bigl[\pvec\cdot\epsilonvec_\lambda +i\Svec\cdot(\kvec\cross\epsilonvec_\lambda)\bigr] e^{i\kvec\cdot\rvec}}{A}
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-30
\begin{aligned}
&={e\over mc} \sqrt{2\pi\hbar c^2\over V} {\sqrt{n_\lambda}\over \sqrt{\omega_k}} (-i\hbar) M_{BA}.
\end{aligned}
:::

The atomic matrix element is the same as in the process of emission, except it is complex conjugated. Finally, when we use this matrix element to compute the transition rate, we have

:::{math}
:label: eq-radnmatt-31
w= {2\pi\over\hbar^2} \sum_\lambda {e^2\over m^2c^2} {2\pi\hbar c^2\over V} {n_\lambda \over\omega_k} \hbar^2 |M_{BA}|^2 \, \delta(\omega-\omega_{BA}).
:::

This would be fine if we had exact knowledge of the initial state of the electromagnetic field (if we knew it was in the pure state $\ket{\ldots n_\lambda \ldots}$, and if we knew exactly what all the $n_\lambda$ were), but in practice we often do not have such information. Often we have only statistical information about the initial state of the field; this is certainly true for black body radiation, but it is also usually true for other types of radiation fields, including laser light. Let us suppose, therefore, that we only know some probability distribution for the occupation numbers, say, $P(\{n_\lambda\})$, which is the probability for a specific list $\{n_\lambda\}$ of occupation numbers. For example, in thermal equilibrium (black body radiation), we would have

:::{math}
:label: eq-radnmatt-32
P(\{n_\lambda\}) = {1\over Z} \exp\Bigl( -\beta\sum_\lambda n_\lambda \, \hbar\omega_k \Bigr).
:::

Working with such a probability distribution is equivalent to working with a density operator for the electromagnetic field that is diagonal in the occupation number representation,

:::{math}
:label: eq-radnmatt-33
\rho = \sum_{\{n_\lambda\}} \ket{\{n_\lambda\}} P(\{n_\lambda\}) \bra{\{n_\lambda\}}.
:::

As explained in {ref}`ch-density`, the absence of off-diagonal terms means that the relative phases between different occupation number states are random.

Under such a statistical assumption, we should replace $w$ by its average over the probability distribution. This involves placing a sum over $\{n_\lambda\}$ times $P(\{n_\lambda\})$ before the right hand side of {eq}`eq-radnmatt-31`. But the only term in the right hand side that depends on $\{n_\lambda\}$ is the single factor of $n_\lambda$ itself, which then gets replaced by its average,

:::{math}
:label: eq-radnmatt-34
\xpecval{n_\lambda} = \sum_{\{n_\lambda\}} P(\{n_\lambda\}) \, n_\lambda.
:::

Finally, we can replace the sum on $\lambda$ by the usual limit as $V\to\infty$,

:::{math}
:label: eq-radnmatt-35
\sum_\lambda \to \sum_\mu {V\over (2\pi)^3} \, {1\over c^3} \int_0^\infty \omega^2\,d\omega \int d\Omega_k,
:::

where we sum over all states (the modes from which the photon could be absorbed) because we are only interested here in the total rate of absorption. As usual, the $\omega$-integral is trivial because of the $\delta$-function. We obtain

:::{math}
:label: eq-radnmatt-36
w= {1\over 2\pi} {e^2\over m^2c^3} \hbar\omega \sum_\mu \int d\Omega_k \, \xpecval{n_\lambda} |M_{BA}|^2.
:::

(sec-radnmatt-6)=

## Absorption of Isotropic and Unpolarized Radiation

The average number of photons per mode $\xpecval{n_\lambda}$ is a function of $\lambda$, that is, in general it depends on $k$, ${\hat{\mathbf{k}}}$, and $\mu$. But if the radiation is isotropic and unpolarized, then by definition $\xpecval{n_\lambda}$ depends only on the magnitude of the wave vector $k$ (or equivalently, on the frequency $\omega$). For simplicity, let us consider this case. Then $\xpecval{n_\lambda}$ can be taken out of the sum and integral in {eq}`eq-radnmatt-36`, and what remains is the average of the squared matrix element, as in {eq}`eq-radnmatt-22`. The result is

:::{math}
:label: eq-radnmatt-37
w_abs={4e^2 \over m^2 c^3} \hbar \omega \overline{|M_{BA}|^2} \, \xpecval{n_\lambda} = A_E \, \xpecval{n_\lambda},
:::

which is the rate of absorption for isotropic, unpolarized radiation. It is just $\xpecval{n_\lambda}$ times the Einstein $A$-coefficient, a simple result.

It is, however, more convenient to express $\xpecval{n_\lambda}$ in terms of macroscopic quantities. The average number of photons in mode $\lambda$ can be expressed macroscopically in terms of the energy density per unit frequency interval. This follows from writing out the energy density $u$ (energy per unit volume) of the field in a box,

:::{math}
:label: eq-radnmatt-38
u ={1\over V} \sum_\lambda \xpecval{n_\lambda} \, \hbar\omega_k \to {1\over(2\pi)^3} \,{1\over c^3} \int_0^\infty \omega^2 \, d\omega \int d\Omega_k \sum_\mu \xpecval{n_\lambda} \, \hbar\omega_k,
:::

where the limit $V\to\infty$ is indicated. But if the radiation is unpolarized and isotropic, then the entire summand/integrand becomes independent of ${\hat{\mathbf{k}}}$ and $\mu$, and $\int d\Omega_k \, \sum_\mu$ can be replaced by $8\pi$. This gives

:::{math}
:label: eq-radnmatt-39
u ={\hbar\over \pi^2 c^3} \int_0^\infty d\omega \, \omega^3 \xpecval{n_\lambda},
:::

where it is understood that $\xpecval{n_\lambda}$ is a function only of $\omega$. But this is equivalent to

:::{math}
:label: eq-radnmatt-40
\dod{u}{\omega} = {\hbar \omega^3 \over \pi^2 c^3} \xpecval{n_\lambda}.
:::

This is really an elementary result, which just amounts to counting states. Of course, if we use {eq}`eq-quantemf-39` for $\xpecval{n_\lambda}$, we obtain the usual Planck formula for $du/d\omega$.

Equations~{eq}`eq-radnmatt-37` and {eq}`eq-radnmatt-40` show that the rate of absorption is proportional to $du/d\omega$. Following Einstein, we write this relationship in the form

:::{math}
:label: eq-radnmatt-41
w_abs = B_E \, \dod{u}{\omega},
:::

which serves to define $B_E$, the Einstein $B$-coefficient. Now {eq}`eq-radnmatt-37`, {eq}`eq-radnmatt-40` and {eq}`eq-radnmatt-41` can be used to obtain a relation between the Einstein $A$- and $B$-coefficients,

:::{math}
:label: eq-radnmatt-42
A_E = {\hbar\omega^3 \over \pi^2 c^3} B_E.
:::

The relation between the Einstein $A$ and $B$ coefficients depends only on the counting of states in the electromagnetic field; it does not depend on the nature of the matter interacting with the radiation. Thus, {eq}`eq-radnmatt-42` is valid for radiation interacting with any kind of matter (atoms in a gas, nuclei inside a star, etc). {eq}`eq-radnmatt-42` is of use in the semiclassical theory of radiation, in which $B_E$ can be computed after a tricky and convoluted calculation, but $A_E$ is impossible.

(sec-radnmatt-7)=

## Stimulated Emission

Finally, let us examine the process of emission in the presence of radiation. This is just like the spontaneous emission considered above, except the photon field is not assumed to be empty in the initial state. We let the initial and final states be

:::{math}
:label: eq-radnmatt-43
\begin{aligned}
\ket{i} &= \ket{B} \ket{\ldots n_\lambda \ldots}, \\
\ket{n} &= \ket{A} \ket{\ldots,n_\lambda+1, \ldots}, \\

\end{aligned}
:::

where it is understood that all occupation numbers are the same in the initial and final states, except in mode $\lambda$, which gains a photon. Now the matrix element for time-dependent perturbation theory has the form

:::{math}
:label: eq-radnmatt-44
\matrixelement{n}{H_1}{i} = {e\over mc} \bra{A}\bra{\ldots,n_\lambda+1,\ldots} (\pvec\cdot\Avec + \Svec\cdot\Bvec) \ket{B}\ket{\ldots n_\lambda \ldots},
:::

and only the creation operator $a^\hc_{\lambda'}$ for $\lambda'=\lambda$ survives in the sum {eq}`eq-radnmatt-13`. Also, we have

:::{math}
:label: eq-radnmatt-45
a^\hc_\lambda\ket{\ldots n_\lambda \ldots} = \sqrt{n_\lambda +1} \, \ket{\ldots, n_\lambda+1, \ldots},
:::

so that when we compute the transition rate, we obtain

:::{math}
:label: eq-radnmatt-46
w_emiss= {2\pi\over\hbar^2} \sum_\lambda {e^2\over m^2c^2} {2\pi\hbar c^2\over V} {n_\lambda+1 \over\omega_k} \hbar^2 |M_{BA}|^2 \, \delta(\omega-\omega_{BA}),
:::

which is exactly the same as the absorption rate {eq}`eq-radnmatt-31` except for the replacement of $n_\lambda$ by $n_\lambda+1$. It is also the same as the rate of spontaneous emission {eq}`eq-radnmatt-18`, except for the replacement of 1 by $n_\lambda+1$. Thus, the $n_\lambda$ part is regarded as the rate of stimulated emission, and the 1 part is the rate of spontaneous emission.

If the sum on $\lambda$ is taken over all photon states, then the result is the total rate of emission of the photon into any final state. Of course energy conservation restricts which final states the photon may go into, and the matrix element has a dependence on the direction of the outgoing photon, but there are still many possible final states. But because of the numerator in $n_\lambda+1$, those states that are already populated by photons are more likely to receive the emitted photon. In this way, photon states that are already populated tend to become more populated; one can say that bosons not only can occupy the same state, they like to occupy the same state. The classical or semiclassical interpretation of this process is simple, for if we imagine an initial photon state that is already populated as a classical electromagnetic wave, assumed to be in resonance with the atomic transition, then the wave shakes the atom at its resonant frequency and stimulates the emission of a new photon with the same frequency, wave vector and polarization as the wave itself.

This is the basic principle of amplification in lasers and masers, which typically work by passing radiation through a cavity containing a population of atoms in an excited state. These atoms are stimulated to emit photons into one or a few states, which tends to increase the amplitude of the wave. However, stimulated emission is in competition with absorption, which according to {eq}`eq-radnmatt-31` has a transition rate that is also proportional to $n_\lambda$. Of course, absorption removes photons from the wave. Therefore lasing normally requires a population inversion, to give the advantage to the process of emission.

The $+1$ in {eq}`eq-radnmatt-45`, representing the rate of spontaneous emission, is generally parasitic to laser operation, since the emitted photon is just as happy to go out in any direction or polarization. For proper laser operation, the population inversion must be sufficiently favorable to overcome these and other losses.

Let us now assume that the initial radiation field is represented by an isotropic and unpolarized ensemble $P(\{n_\lambda\})$, just as we did for absorption. Then we can average over the ensemble and sum over modes $\lambda$ in {eq}`eq-radnmatt-46`, to obtain

:::{math}
:label: eq-radnmatt-47
w_emiss = A_E (\xpecval{n_\lambda}+1) = B_E \dod{u}{\omega} + A_E.
:::

We see that the rate of stimulated emission is equal to the rate of absorption; this is called *detailed balance*, which means that transition rates between two microscopic states are equal. Detailed balance is not necessary to establish thermal equilibrium, but it generally holds in first order perturbation theory, due to the Hermiticity of the perturbing Hamiltonian $H_1$.

(sec-radnmatt-8)=

## Decomposition of $M_{BA}$ into Multipoles

We will now analyze the atomic matrix element $M_{BA}$, given by {eq}`eq-radnmatt-16`, which applies to both emission and absorption. First we note that the phase $\kvec\cdot\rvec$ in the exponent in {eq}`eq-radnmatt-16` is small over the size of the atom. This follows easily in atomic units, in which the size of the atom is $a \sim 1/Z$, and the frequency of the emitted or absorbed radiation is $\omega \sim Z^2$. But since $k=\omega/c =\alpha\omega$ in atomic units, and since $x \sim a$, we have

:::{math}
:label: eq-radnmatt-48
\kvec\cdot\rvec \sim Z\alpha.
:::

If $Z$ is not too large, this is a small quantity. Similarly, we find that the term $i\Svec\cdot(\kvec\cross\epsilonvec_\lambda)$ in {eq}`eq-radnmatt-16` is of order $Z\alpha$ relative to $\pvec\cdot\epsilonvec_\lambda$. Therefore expanding in powers of $k$ is equivalent to expanding in powers of $Z\alpha$. We write

:::{math}
:label: eq-radnmatt-49
M_{BA} = M^{(0)}_{BA} + M^{(1)}_{BA} + \ldots
:::

for this expansion, where

:::{math}
:label: eq-radnmatt-50
\begin{aligned}
M^{(0)}_{BA} &= {i\over \hbar} \matrixelement{B} {\epsilonvec_\lambda\cdot\pvec}{A},
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-51
\begin{aligned}
M^{(1)}_{BA} &= -{1\over\hbar} \matrixelement{B} {\Svec\cdot(\kvec\cross\epsilonvec_\lambda) + (\epsilonvec_\lambda\cdot\pvec)(\kvec\cdot\rvec)}{A}.
\end{aligned}
:::

As we shall show, the term $M^{(0)}_{BA}$ is the electric dipole ($E1$) term, while the term $M^{(1)}_{BA}$ contains both the magnetic dipole ($M1$) term and the electric quadrupole ($E2$) term.

First we work on $M^{(0)}_{BA}$. We invoke the following commutator, which is equivalent to the Heisenberg equations of motion for the operator $\rvec$,

:::{math}
:label: eq-radnmatt-52
[\rvec,H_0] = {i\hbar\pvec\over m} = i\hbar \dot\rvec.
:::

Here $H_0$ can be taken to be the unperturbed atomic Hamiltonian seen in {eq}`eq-radnmatt-6` since the field Hamiltonian will not contribute. Using {eq}`eq-radnmatt-52` in {eq}`eq-radnmatt-50`, we find

:::{math}
\begin{aligned}
M^{(0)}_{BA} &= {m \over \hbar^2} \epsilonvec_\lambda \cdot \matrixelement{B}{\rvec H_0 - H_0\rvec}{A}
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-53
\begin{aligned}
&={m\over\hbar^2}(E_A-E_B) \epsilonvec_\lambda\cdot \matrixelement{B}{\rvec}{A} =-{m\omega\over\hbar}\epsilonvec_\lambda\cdot \matrixelement{B}{\rvec}{A},
\end{aligned}
:::

where $\omega=\omega_{BA}=(E_B-E_A)/\hbar$. The matrix element of $\rvec$ is proportional to the matrix element of the electric dipole operator, defined by

:::{math}
:label: eq-radnmatt-54
\Dvec=-e\rvec,
:::

so we will henceforth refer to $M_{BA}^{(0)}$ as the electric dipole contribution to the matrix element. We will write this contribution as

:::{math}
:label: eq-radnmatt-55
M_{BA}^{E1} = -{m\omega\over\hbar} \epsilonvec_\lambda\cdot \matrixelement{B}{\rvec}{A}.
:::

Because the electric dipole term is the leading term in the expansion in $kx$, the assumption $kx \ll 1$ is sometimes called the electric dipole approximation.

As for $M^{(1)}_{BA}$, we work on the orbital part first [the second term in {eq}`eq-radnmatt-51`]. We note that the two factors in this term can be written in any order, since

:::{math}
:label: eq-radnmatt-56
[\epsilonvec_\lambda\cdot\pvec, \kvec\cdot\rvec] = -i\hbar \, \epsilonvec_\lambda \cdot \kvec =0,
:::

because the light waves are transverse. We use the summation convention and break this term up into its symmetric and antisymmetric parts, finding,

:::{math}
\begin{aligned}
M^{(1)}_orb &= -{1\over\hbar} k_i \epsilon_j \matrixelement{B}{x_i p_j}{A}
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-57
\begin{aligned}
&= -{1\over 2\hbar} k_i \epsilon_j \matrixelement{B}{x_ip_j - x_jp_i}{A} -{1\over 2\hbar} k_i \epsilon_j \matrixelement{B}{x_ip_j+x_jp_i}{A}.
\end{aligned}
:::

The antisymmetric part can be written in terms of the orbital angular momentum,

:::{math}
:label: eq-radnmatt-58
-{1\over 2\hbar} k_i \epsilon_j \matrixelement{B}{x_ip_j - x_jp_i}{A} = -{1\over 2\hbar} (\kvec\cross\epsilonvec) \cdot \matrixelement{B}{\rvec\cross\pvec}{A},
:::

which, when combined with the spin part of $M^{(1)}_{BA}$ [the first term in {eq}`eq-radnmatt-51`], gives the magnetic dipole contribution to the matrix element,

:::{math}
:label: eq-radnmatt-59
M^{M1}_{BA} = -{1\over 2\hbar} (\kvec\cross\epsilonvec_\lambda)\cdot \matrixelement{B}{\Lvec + 2 \Svec}{A}.
:::

With the help of the commutation relations {eq}`eq-radnmatt-52` and {eq}`eq-radnmatt-56`, the symmetric part of $M^{(1)}_{BA}$ can be transformed as follows:

:::{math}
\begin{aligned}
-{1\over2\hbar} k_i \epsilon_j \matrixelement{B} {x_ip_j + p_ix_j}{A} &= {im\over 2\hbar^2} \, k_i\epsilon_j \matrixelement{B}{x_ix_jH_0 - H_0x_ix_j}{A}
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-60
\begin{aligned}
&= -{im \omega \over 2\hbar} k_i \epsilon_j \matrixelement{B}{x_ix_j}{A},
\end{aligned}
:::

where we have swapped $x_j$ and $p_i$ in the second term of the first expression. In the final expression it is customary to replace the operator $x_ix_j$ by $Q_{ij}/3$, where $Q_{ij}$ is the electric quadrupole operator,

:::{math}
:label: eq-radnmatt-61
Q_{ij} = 3x_ix_j - r^2 \delta_{ij}.
:::

Quadrupole moments were discussed in {ref}`sec-orbamsph-11`; see {eq}`eq-orbamsph-88`. The extra term proportional to $\delta_{ij}$ in {eq}`eq-radnmatt-61` makes no contribution to the matrix element {eq}`eq-radnmatt-60` because $\epsilonvec\cdot\kvec=0$. We include it anyway because it makes the tensor $Q_{ij}$ a $k=2$ irreducible tensor operator. The extra term in {eq}`eq-radnmatt-61` has the effect of subtracting off the $k=0$ component of the tensor product $x_ix_j$. Altogether, we find the electric quadrupole contribution to the matrix element,

:::{math}
:label: eq-radnmatt-62
M^{E2}_{BA} = -{im\omega \over 6\hbar} \, k_i\epsilon_j \, \matrixelement{B}{Q_{ij}}{A}.
:::

In these operations on the atomic matrix element $M_{BA}$, we have been doing two things: one is to expand the matrix element in the small quantity $kx\ll1$, and the other is to organize the results into irreducible tensor operators. We have done this in an ad hoc manner for the first three terms ($E1$, $M1$ and $E2$) of the multipole expansion; these are the terms that are usually of most importance in atomic physics. However, in nuclear and molecular physics, one often has need to go to higher order in the multipole expansion, and one must be more systematic.

It is not necessary to expand in powers of $kx$ in order to carry out the multipole expansion, and in some applications $kx$ is not small. This is notably true in nuclear physics, where $kx$ is not as favorable as in atomic applications. To carry out the multipole expansion without expanding in powers of $kx$, it is convenient to organize the photon states as eigenfunctions of $(k,\pi,J^2,J_z$), rather than as eigenfunctions of $(\kvec,\Omega)$ as we have done. The eigenfunctions of $(\pi,J^2,J_z)$ are known as *vector spherical harmonics*; they are a generalization of the ordinary spherical harmonics to vector fields. The theory of the vector spherical harmonics is essentially a straightforward application of rotation operators to the wave functions of a spin-1 particle, but it is sufficiently lengthy that we will not go into it in detail.

However, we remark that if $kx$ is small, it means that the phase of the light wave is nearly constant over the spatial extent of the radiator, namely, the atom. We recall that in scattering theory we have $s$-wave scattering in the long wavelength limit, because the radiators stimulated by the incident wave are all in phase. In $s$-wave scattering, the scattered wave is isotropic and the cross is independent of angle. In the case of a scalar wave, it is possible to radiate $s$-waves, but for transverse vector waves such as electromagnetic waves there are no $s$-waves. Instead, the lowest angular momentum state for the radiated waves is the $j=1$ state, which comes in two varieties, odd and even parity, representing electric and magnetic dipole radiation. These give the simplest radiation patterns possible with electromagnetic waves. If $kx$ is not small, it means that it is necessary to take into account the phase differences in the radiated wave across the radiator, which can be regarded as the effects of retardation.

(sec-radnmatt-9)=

## Order of Magnitude of Different Multipoles

The total matrix element $M_{BA}$ is a sum of terms in the multipole expansion, but if $kx$ is small, there will be one term of leading order that dominates the others. Thus, in atomic transitions, the radiation is dominantly of one type ($E1$, $M1$, etc.), although higher order corrections are present, in general. The transition rate for the different multipole types is conveniently estimated by working in atomic units and expressing the dependence of $w$ on $Z$ and the fine structure constant $\alpha=1/c$. For simplicity, we will ignore the dependence on the atomic quantum numbers, but if any of these are large, they should be taken into account, too. Then we find that the matrix element $M^{E1}_{BA}$ of {eq}`eq-radnmatt-55` is of order $Z$ in atomic units, while the matrix elements $M^{M1}_{BA}$ and $M^{E2}_{BA}$, given by {eq}`eq-radnmatt-59` and {eq}`eq-radnmatt-62`, are both of order $\alpha Z^2$. Therefore the spontaneous transition rate, given by {eq}`eq-radnmatt-23`, goes as $\alpha^3 Z^4$ for $E1$ transitions, and as $\alpha^5 Z^6$ for $M1$ and $E2$ transitions. We see that if $Z$ is not too large, the condition {eq}`eq-radnmatt-25` on time scales is easily met. In fact, for $Z\approx 1$ and for quantum numbers of order unity, the lifetimes for electric dipole transitions are of the order of $\alpha^3 \sim 10^{-6}$ times smaller than the orbital period of the electron. For example, in the $2p \to 1s$ transition in hydrogen (the fastest one), we can think of the electron as orbiting on the order of a million times before dropping into the ground state. The factor becomes $\alpha^5 \sim 10^{-10}$ for $M1$ and $E2$ transitions that are even slower.

(sec-radnmatt-10)=

## Selection Rules

The operators that occur in the various multipole matrix elements {eq}`eq-radnmatt-55`, {eq}`eq-radnmatt-59`, and {eq}`eq-radnmatt-62`, can be expressed in terms of irreducible tensor operators $T^k_q$. These operators also have well defined transformation properties under conjugation by parity $\pi$. Table~radnmatt-1 summarizes the different operators we have considered and lists their $k$ values and parities. The general rules are that an $Ek$ or an $Mk$ operator is an irreducible tensor operator (perhaps in Cartesian form) of order $k$, and that an $Ek$-operator has parity $(-1)^k$ and an $Mk$-operator has parity $(-1)^{k+1}$.

:::{table} Multipole terms in the expansion of the transition matrix element. The order $k$ and parity $\pi$ of the irreducible tensor operator $T^k_q$ are tabulated. \par
:label: tbl-radnmatt-1

| | $T_q^k$ | $k$ | $\pi$ | Selection Rules |
|:---:|:---:|:---:|:---:|:---|
| $E1$ | r | 1 | $-$ | $\Delta j = 0, \pm 1, \Delta \ell = \pm 1$ |
| $M1$ | $\mathbf{L} + 2\mathbf{S}$ | 1 | $+$ | $\Delta j = 0, \pm 1, \Delta \ell = 0$ |
| $E2$ | $Q_{ij}$ | 2 | $+$ | $\Delta j = 0, \pm 1, \pm 2, \Delta \ell = 0, \pm 2$ |

:::
These operators are sandwiched between atomic states $A$ and $B$, which are eigenstates of various angular momentum operators and also of parity (ignoring the weak interactions). The Wigner-Eckart theorem and rules of parity can be applied to the resulting matrix elements to obtain selection rules. For example, consider a model of hydrogen in which we include the fine structure corrections but ignore the hyperfine structure. Let us denote the upper state $B$ by $\ket{n\ell jm_j}$ and the lower state $A$ by $\ket{n' \ell' j'm'_j}$, so the different multipole contributions have the form $\matrixelement{n\ell jm_j}{T^k_q}{n'\ell' j' m'_j}$. The selection rules for $E1$ transitions are familiar; the operator $\rvec$ is a $k=1$ irreducible tensor operator both under total rotations, generated by $\Jvec$, and under purely orbital rotations, generated by $\Lvec$. Therefore the Wigner-Eckart theorem gives the selection rules $\Delta j=0,\pm1$ and $\Delta \ell=0,\pm1$; but the case $\Delta \ell=0$ is excluded by parity (otherwise known as Laporte's rule). For $M1$ transitions, the operator $\Lvec+2\Svec$ is a $k=1$ irreducible tensor operator under total rotations, generated by $\Jvec$, but is the sum of a $k=1$ and a $k=0$ operator under purely spatial rotations. Again, the Wigner-Eckart theorem gives $\Delta j=0,\pm1$ and $\Delta \ell=0,\pm1$, but this time parity excludes the case $\Delta\ell=\pm1$. Similarly, for $E2$ transitions, the case $\Delta \ell=\pm1$, which would be allowed by the Wigner-Eckart theorem, is excluded by parity. These rules are summarized in Table~radnmatt-1.

There are further restrictions imposed by the Wigner-Eckart theorem. For example, an $E2$ transition $j=\frac{1}{2} \to j=\frac{1}{2}$ is not allowed, because it is impossible to reach $j=\frac{1}{2}$ from $2\otimes\frac{1}{2}$. Similarly, $\ell=0 \to \ell=0$ is impossible in $E2$ transitions. In hydrogen, only half-integral $j$ are allowed, but in atoms with an even number of electrons, $J$ is integral, and there are further rules of a similar sort. For example, $J=0 \to J=0$ is impossible in either $E1$ or $M1$ transitions.

An interesting case in hydrogen is the $2s_{1/2} \to 1s_{1/2}$ transition. Of course, the $2p$ states can make an $E1$ transition to the ground state, and do so with a lifetime on the order of $10^{-9}$~sec. However, the $2s_{1/2} \to 1s_{1/2}$ is forbidden as an $E1$ transition, because of parity. It would appear from Table~radnmatt-1 that this transition is allowed as an $M1$ transition, but it turns out that the matrix element {eq}`eq-radnmatt-59` vanishes because of the orthogonality of the radial wave functions. In detail, the story of the $M1$ transition in this case is somewhat complicated. It turns out that if the hydrogen atom is modeled with the Dirac equation, then the $M1$ matrix element does not exactly vanish, but it is higher order in powers of $v/c\sim\alpha$ than one would normally expect, and is very small. A similar result is obtained with the Schr\"odinger-Pauli theory, if we expand to higher order in $kx$ and extract the $M1$ contribution from some higher order terms (although the Schr\"odinger-Pauli theory is not reliable for terms that are higher order in $v/c$). Suffice it to say that the $M1$ matrix element is very small. What about higher multipole moments in the $2s_{1/2} \to 1s_{1/2}$ transition? The $E2$ transition is forbidden in this case because it would be both a $j=\frac{1}{2} \to j=\frac{1}{2}$ and an $\ell=0 \to \ell=0$ transition. Similarly, we can see that all higher order multipole transitions are forbidden, because we cannot reach $j=\frac{1}{2}$ from $k\otimes\frac{1}{2}$, when $k\ge2$. In fact, it turns out that the principal decay mode of the metastable $2s_{1/2}$ state is a two-photon decay to the $1s_{1/2}$ state, with a lifetime of about $10^{-1}$~sec. See Prob. {ref}`prob-photscatt-1`.

Speaking of small effects, we may also notice that the $2s_{1/2}$ can decay to the $2p_{1/2}$ state by an $E1$ transition, since the latter is lower in energy by the (small) Lamb shift. But this rate is much smaller than the two-photon decay mentioned above, and does not contribute much to the overall decay rate. This transition is, however, important when driven by microwaves at or near the resonant frequency of 1.06 GHz. Indeed, Lamb and Retherford first used such microwave techniques in 1949 to make an unequivocal and high precision measurement of the Lamb shift.

(sec-radnmatt-11)=

## Angle and Polarization Dependence of Radiation

Let us return now to the process of spontaneous emission, and consider the intensity of the emitted radiation as a function of angle and polarization. We will work this out only for electric dipole radiation, the most common case. We can imagine an experimental situation such as that illustrated in {ref}`fig-radnmatt-2`, which effectively measures the polarization $\mu$ and direction ${\hat{\mathbf{k}}}$ of the outgoing photon. In the following we will assume for simplicity that some state ($\mu=\pm1$) of circular polarization is measured, but other states of polarization are only slightly more complicated to analyze.

:::{figure} images/radnmatt-fig02.png
:label: fig-radnmatt-2
:width: 80%

Photons are emitted from a source of excited atoms at the origin of the coordinates. Photons emitted in a small solid angle around the direction $\kvec$ are filtered by the polarizer $P$, which passes only one state of polarization, and are detected by the detector $D$.
:::

We start with {eq}`eq-radnmatt-21`, into which we substitute {eq}`eq-radnmatt-53` for the electric dipole approximation to the matrix element. This gives

:::{math}
:label: eq-radnmatt-63
\Bigl(\dod{w}{\Omega}\Bigr)_\mu = {1\over 2\pi} {e^2\omega^3\over\hbar c^3} |\epsilonvec_\mu \cdot \rvec_{BA}|^2,
:::

where $\epsilonvec_\mu=\epsilonvec_\mu({\hat{\mathbf{k}}})=\epsilonvec_\lambda$, and where

:::{math}
:label: eq-radnmatt-64
\rvec_{BA} = \matrixelement{B}{\rvec}{A}.
:::

For simplicity we assume the atom is a hydrogen-like atom in the fine-structure model (we ignore hyperfine effects, etc.), and we take the upper and lower states to be $\ket{B}=\ket{n\ell jm_j}$ and $\ket{A}=\ket{n'\ell'j'm'_j}$, as above, so that

:::{math}
:label: eq-radnmatt-65
\rvec_{BA} = \matrixelement{n\ell jm_j}{\rvec} {n'\ell'j'm'_j}.
:::

(However, hardly anything changes if we use the eigenstates $\ket{\alpha\pi LJM_J}$ of a multi-electron atom.)

It is convenient to expand $\rvec$ in terms of the spherical basis as in {eq}`eq-wigeck-4`,

:::{math}
:label: eq-radnmatt-66
\rvec=\sum_q {\hat{\mathbf{e}}}^\cc_q x_q,
:::

because then the components $x_q$ are components of a rank~1 irreducible tensor operator. We also use {eq}`eq-quantemf-80` to express $\epsilonvec_\mu$ in terms of the spherical basis. Then we have

:::{math}
:label: eq-radnmatt-67
\epsilonvec_\mu\cdot\rvec=\sum_q x_q \, {\hat{\mathbf{e}}}^\cc_q \cdot \bigl[\Rmat({\hat{\mathbf{k}}}){\hat{\mathbf{e}}}_\mu\bigr] = \sum_q x_q \, D^1_{q\mu}({\hat{\mathbf{k}}}),
:::

where $\Rmat({\hat{\mathbf{k}}})$ is defined by {eq}`eq-quantemf-78` and $D^1({\hat{\mathbf{k}}})$ is the corresponding $D$-matrix, and where we use {eq}`eq-wigeck-28`.

Now when we compute $\epsilonvec_\mu\cdot\rvec_{BA}$, we obtain a sum over the matrix elements of $x_q$, which can be transformed by the Wigner-Eckart theorem [see {eq}`eq-wigeck-44`]:

:::{math}
\begin{aligned}
\epsilonvec_\mu\cdot\rvec_{BA} &= \sum_q \matrixelement{n\ell jm_j}{x_q}{n'\ell'j'm'_j} \, D^1_{q\mu}({\hat{\mathbf{k}}})
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-68
\begin{aligned}
&= \reducedme{n\ell j}{x}{n'\ell'j'} \sum_q \braket{jm_j}{j'1m'_jq} \, D^1_{q\mu}({\hat{\mathbf{k}}}).
\end{aligned}
:::

But by the selection rule {eq}`eq-jjcouple-51` for the Clebsch-Gordan coefficients, only the term $q=m_j-m'_j$ survives in the sum. Therefore when we combine all the pieces together, we obtain the following expression for the differential transition rate for electric dipole transitions:

:::{math}
:label: eq-radnmatt-69
\Bigl(\dod{w}{\Omega}\Bigr)_\mu = {1\over 2\pi} {e^2\omega^3\over\hbar c^3} |\reducedme{n\ell j}{x}{n'\ell'j'}|^2\, |\braket{jm_j}{j'1m'_jq}|^2 \, |D^1_{q\mu}({\hat{\mathbf{k}}})|^2,
:::

where now it is understood that $q=m_j-m'_j$ ($q$ is not summed over). This is a convenient expression, because the reduced matrix element shows the dependence of the transition rate on the manifolds $(n\ell j)$ and $(n'\ell'j')$ of the initial and final states, the Clebsch-Gordan coefficient shows the dependence on the magnetic quantum numbers, and the $D$-matrix shows the dependence on the polarization and direction of the outgoing photon. Furthermore, writing the $D$-matrix in Euler angle form and using {eq}`eq-repsamos-67`, we have

:::{math}
:label: eq-radnmatt-70
\Bigl(\dod{w}{\Omega}\Bigr)_\mu \sim |{\hat{\mathbf{e}}}^\cc_q\cdot\epsilonvec_\mu({\hat{\mathbf{k}}})|^2= |D^1_{q\mu}(\phi,\theta,0)|^2 = [d^1_{q\mu}(\theta)]^2,
:::

where as illustrated in {ref}`fig-radnmatt-2` $(\theta,\phi)$ are the spherical angles of ${\hat{\mathbf{k}}}$ and where we suppress all leading factors and concentrate on the dependence on ${\hat{\mathbf{k}}}$ and $\mu$. We see that the intensity of the emitted radiation is independent of the azimuthal angle $\phi$, as we would expect since the initial and final states are eigenstates of $J_z$. Finally, we can invoke {eq}`eq-repsamos-70` for the reduced rotation matrix to determine the angular distribution as a function of $\theta$ for different choices of $q$ and $\mu$. The angular distribution is plotted in {ref}`fig-radnmatt-3` for different cases. By the way, the quantity $q$ has a simple interpretation, for if we write its definition in the form $m_j=m'_j+q$, we see that $q$ is just the $J_z$ quantum number of the emitted photon, since the total $J_z$ of the combined matter-field system is conserved in the emission process.

:::{figure} images/radnmatt-fig03.png
:label: fig-radnmatt-3
:width: 80%

Polar plots of intensity of electric dipole radiation for different cases. Case $(a)$, $q=\mu=\pm1$; case $(b)$, $q=0$, $\mu=\pm1$; case $(c)$, $q=-\mu=\pm1$. Intensity is azimuthally symmetric.
:::

The radiation patterns in {ref}`fig-radnmatt-2` can be seen experimentally by placing the source (for example, a gas discharge tube) in a strong magnetic field, which will split the various magnetic substates of the otherwise degenerate initial and final states, so that a transition with a definite value of $\Delta m_j = -q$ can be observed. On the other hand, in many practical circumstances there is no magnetic field to split these substates, nor is the initial ensemble of atoms polarized. In such cases, the atom has an equal probability of being in any of the magnetic substates of the initial, degenerate atomic level; and all transitions to the various magnetic substates of the final, degenerate atomic level lie on top of one another (they have the same frequency), so the spectroscope simply sees a single line whose intensity is the superposition of the intensities of possibly several transitions. Furthermore, if the initial state of the atom is unpolarized, then it has no preferred direction, and the emitted radiation is isotropic. In this case we might as well ask for the total transition rate (integrated over all solid angles and summed over polarizations). We will now analyze this case for electric dipole radiation.

(sec-radnmatt-12)=

## The Total Transition Rate

We begin by computing the total transition rate. We could do this by integrating {eq}`eq-radnmatt-69` over solid angles and summing it over polarizations, but it is just as easy to go back to {eq}`eq-radnmatt-23`, and to use the electric dipole expression {eq}`eq-radnmatt-53` for the matrix element. Also, for simplicity, we will use the simple electrostatic, spinless model for the states $\ket{n\ell m}$ of the one-electron atom, that is, we will ignore the fine structure corrections. Then combining {eq}`eq-radnmatt-22` and {eq}`eq-radnmatt-53`, we have

:::{math}
:label: eq-radnmatt-71
\overline{|M_{BA}|^2} = {m^2\omega^2\over \hbar^2} {1\over 8\pi} \sum_\mu \int d\Omega_k \, |\epsilonvec_\mu({\hat{\mathbf{k}}})\cdot\rvec_{BA}|^2,
:::

where now

:::{math}
:label: eq-radnmatt-72
\rvec_{BA}= \matrixelement{n\ell m}{\rvec}{n'\ell'm'}.
:::

Here the initial and final states are $\ket{B}=\ket{n\ell m}$ and $\ket{A}=\ket{n'\ell'm'}$, respectively. The polarization sum in {eq}`eq-radnmatt-71` is easy if we use the completeness relation {eq}`eq-classemf-53` for the polarization vectors. This gives

:::{math}
:label: eq-radnmatt-73
\sum_{\mu=\pm1} |\epsilonvec_\mu({\hat{\mathbf{k}}}) \cdot \rvec_{BA}|^2 = |\rvec_{BA}|^2 - |{\hat{\mathbf{k}}}\cdot\rvec_{BA}|^2.
:::

Next, the angular integration of this over $\Omega_k$ is easy, since the first term is independent of angle and the second term is just the angle average of one component of a vector. Thus we have

:::{math}
:label: eq-radnmatt-74
\int d\Omega_k \, \bigl( |\rvec_{BA}|^2 - |{\hat{\mathbf{k}}}\cdot\rvec_{BA}|^2 \bigr) = {8\pi\over 3} |\rvec_{BA}|^2.
:::

Altogether, {eq}`eq-radnmatt-71` becomes

:::{math}
:label: eq-radnmatt-75
\overline{|M_{BA}|^2} = {1\over 3} {m^2\omega^2\over \hbar^2} |\rvec_{BA}|^2.
:::

As for the $\rvec_{BA}$, it is convenient to use it in complex conjugated form,

:::{math}
:label: eq-radnmatt-76
|\rvec_{BA}|^2 = |\matrixelement{B}{\rvec}{A}|^2 = |\matrixelement{A}{\rvec}{B}|^2 = |\rvec_{AB}|^2,
:::

where

:::{math}
:label: eq-radnmatt-77
\rvec_{AB} = \matrixelement{n'\ell'm'}{\rvec}{n\ell m}.
:::

We expand $\rvec$ in this expression in the spherical basis as in {eq}`eq-radnmatt-66`, so that

:::{math}
:label: eq-radnmatt-78
\rvec_{AB} = \sum_q {\hat{\mathbf{e}}}^\cc_q \matrixelement{A}{x_q}{B},
:::

and so that

:::{math}
:label: eq-radnmatt-79
|\rvec_{AB}|^2 = \sum_q |\matrixelement{n'\ell'm'}{x_q}{n\ell m}|^2.
:::

But by {eq}`eq-wigeck-14`, the quantity $x_q$ can be expressed in terms of $Y_{1q}(\theta,\phi)$, where $(\theta,\phi)$ are the spherical angles in $\rvec$-space. This causes the matrix element in {eq}`eq-radnmatt-79` to factor into a radial part times an angular part,

:::{math}
:label: eq-radnmatt-80
\matrixelement{n'\ell'm'}{x_q}{n\ell m} =  I_r I_\Omega,
:::

where

:::{math}
:label: eq-radnmatt-81
I_r = \int_0^\infty r^2\, dr\, R_{n'\ell'}(r) r R_{n\ell}(r),
:::

and

:::{math}
:label: eq-radnmatt-82
I_\Omega = \sqrt{{4\pi\over 3}} \int d\Omega\, Y^\cc_{\ell'm'}(\Omega) Y_{1q}(\Omega) Y_{\ell m}(\Omega).
:::

We apply the 3-$Y_{\ell m}$ formula {eq}`eq-jjcouple-67` to the latter, to obtain

:::{math}
:label: eq-radnmatt-83
I_\Omega = \sqrt{{2\ell+1\over 2\ell'+1}} \, \braket{\ell 1mq}{\ell'm'} \braket{\ell'0}{\ell 100}.
:::

Then {eq}`eq-radnmatt-79` becomes

:::{math}
:label: eq-radnmatt-84
|\rvec_{AB}|^2 = {2\ell+1 \over 2\ell'+1} I_r^2 |\braket{\ell'0}{\ell100}|^2 \sum_q \braket{\ell'm'}{\ell1mq} \braket{\ell1mq}{\ell'm'},
:::

which shows how the total transition rate depends on the magnetic quantum numbers of the transition.

Now, however, we assume that the initial state is unpolarized and that we don't care which final state the atom falls into. Then we obtain an effective value of $|\rvec_{AB}|^2$ by averaging over initial magnetic substates, and summing over final magnetic substates. This causes the replacement,

:::{math}
:label: eq-radnmatt-85
|\rvec_{AB}|^2 \to {1\over 2\ell+1} \sum_{mm'} |\rvec_{AB}|^2.
:::

But when we use {eq}`eq-radnmatt-84` in this, the $q$ and $mm'$ sums can be done,

:::{math}
:label: eq-radnmatt-86
\sum_{mm'} \sum_q \braket{\ell'm'}{\ell1mq} \braket{\ell1mq}{\ell'm'} = \sum_{m'} 1 = 2\ell'+1,
:::

where we use the orthonormality relation {eq}`eq-jjcouple-50a` of the Clebsch-Gordan coefficients. Finally, putting all the pieces together and using {eq}`eq-radnmatt-23`, we find the effective Einstein $A$-coefficient for electric dipole radiation,

:::{math}
:label: eq-radnmatt-87
A^{E1} = {4\over 3} {e^2\omega^3 \over \hbar c^3} I_r^2 |\braket{\ell'0}{\ell100}|^2.
:::

A standard reference for the material in these notes is Bethe and Salpeter, *Quantum Mechanics of One- and Two-Electron Atoms*, which includes tables of dipole transition rates.

\problems

(prob-radnmatt-1)=

**Problem \prbdradnmatt-1.}  The perturbation expansion {eq}`eq-radnmatt-6` is valid if $E_wave \ll E_nucleus.** 

(prob-radnmatt-2)=

**Problem \prbdradnmatt-2. Compute the lifetime of the 21~cm transition in Hydrogen, $1s_{1/2} \; (f=1) \to 1s_{1/2.** 

(prob-radnmatt-3)=

**Problem \prbdradnmatt-3.} A hydrogen atom is at distance $D$ from a hot blue star with radius $R$ and surface temperature $T$, which radiates significantly in the ultraviolet.  Assume $D\gg R$, so that the light coming from the star is concentrated in a narrow range of solid angles.  Assume the surface of the star radiates as a blackbody. Assume the atom is unpolarized.  When the atom absorbs a photon, taking it from the $1s$ state to the $2p$ state, it absorbs the photon momentum and suffers a recoil; then in short order ($\sim 10^{-9.** 

(prob-radnmatt-4)=

**Problem \prbdradnmatt-4.}  The matter Hamiltonian {eq}`eq-radnmatt-5` is not a special case of the Hamiltonian {eq}`eq-radnmatt-3`, because the potential $U(r)$ in {eq}`eq-radnmatt-5` is an external, $c$-number potential introduced in an *ad hoc.** 

\problempart{(a)* Consider a two-particle system with masses }$m_1$ and $m_2$ and charges $q_1=e$ and $q_2=-e$. This covers the case of hydrogen, for which $m_1\gg m_2$, and positronium (a bound state of an electron and a positron), for which $m_1=m_2$. Write the matter Hamiltonian as

:::{math}
:label: eq-radnmatt-88
H_matt={1\over 2m_1}\Bigl[\pvec_1 -{e\over c}\Avec(\rvec_1)\Bigr]^2 +{1\over 2m_2} \Bigl[\pvec_2 + {e\over c}\Avec(\rvec_2)\Bigr]^2 -{e^2\over |\rvec_1-\rvec_2|},
:::

where we ignore the $\muvec\cdot\Bvec$ terms because we will be working only to the accuracy of the $E1$ or electric dipole approximation. In this approximation, $\kvec\cdot\rvec$ is of order $\alpha\approx 1/137$ and is negligible, where $\rvec$ is the separation between the two particles. This means that $\Avec(\rvec_1)$ or $\Avec(\rvec_2)$ can be approximated by $\Avec(\Rvec)$, where $\Rvec$ is the center of mass position.

Perform a transformation from the particle positions ($\rvec_1$,$\rvec_2$) and momenta ($\pvec_1$,$\pvec_2$) to center-of-mass positions and momenta ($\Rvec$,$\Pvec$) and relative positions and momenta ($\rvec$,$\pvec$), as in {ref}`sec-cenforce-9`. Let $M$ be the total mass of the system and $\mu$ the reduced mass, as in {ref}`sec-cenforce-9`. Show that in the dipole approximation, the Hamiltonian {eq}`eq-radnmatt-88` can be transformed into

:::{math}
:label: eq-radnmatt-89
H_matt = {P^2\over 2M} + {1\over 2\mu}\Bigl[\pvec + {e\over c}\Avec(\Rvec)\Bigr]^2 -{e^2\over r}.
:::

\problempart{(b)} This is similar to the Hamiltonian {eq}`eq-radnmatt-5`. Differences include the center-of-mass kinetic energy term $P^2/2M$, present here but absent in {eq}`eq-radnmatt-5`; the replacement of $m$ in {eq}`eq-radnmatt-5` by $\mu$ here; and the fact that the Hilbert space contains the center-of-mass degrees of freedom as well as those of the electron and the electromagntic field. Write the total Hamiltonian (matter plus field) in the form

:::{math}
:label: eq-radnmatt-90
H = H_matt + H_em = H_0 + H_1 + H_2,
:::

where

:::{math}
:label: eq-radnmatt-91a
\begin{aligned}
H_0 &= {P^2\over 2M} + {p^2\over 2\mu} -{e^2\over r} + \sum_\lambda \hbar\omega_\lambda \, a^\dagger_\lambda a_\lambda,
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-91b
\begin{aligned}
H_1 &= {e\over \mu c} \,\pvec\cdot\Avec(\Rvec),
\end{aligned}
:::

:::{math}
:label: eq-radnmatt-91c
\begin{aligned}
H_2 &= {e^2\over 2\mu c^2}\,\Avec(\Rvec)^2, .
\end{aligned}
:::

Write the eigenstates of $H_0$ as a product of a matter times a field part, where the matter eigenstate has the form $\ket{X\Kvec}$, where $X$ refers to an atomic state and $\Kvec$ is an eigenstate of the center-of-mass Hamiltonian (with $\Pvec=\hbar\Kvec$). Notice that there three classes of degrees of freedom now, the relative coordinates in the atom, the center of mass coordinates, and the field.

Assume the system is initially in the excited atomic state $B$ with no photons in the field, as in \secrradnmatt-3, and with the initial center of mass momentum $\hbar\Kvec_i=0$. Use first-order time-dependent perturbation theory to compute the differential transition rate as in {eq}`eq-radnmatt-21`, with $M_{BA}$ replaced by the electric dipole approximation as in {eq}`eq-radnmatt-50`. You want the rate at which photons make transitions into a small cone, but you do not care about the center of mass momentum, so you should sum over all values of $\Kvec$ in the final state.

Show that in addition to the physics discussed in Secs.~\secrradnmatt-3 and \secrradnmatt-8, we find the fact that the atom as a whole recoils upon the emission of the photon. The photon frequency is no longer $\omega=\omega_{BA}$, but rather there is a correction, which is small since $\hbar\omega\ll Mc^2$. Compute this correction as a function of $\omega_{BA}$ to first order in small quantities. This correction is the Doppler shift due to the recoil of the atom. It is certainly small, but important in some applications, for example, in laser cooling of atomic gases and in the M\"ossbauer effect (see {ref}`sec-transfop-12`).
