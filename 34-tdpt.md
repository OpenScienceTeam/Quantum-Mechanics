---
title: "34. Time-Dependent Perturbation Theory"
---
(ch-tdpt)=

# 34. Time-Dependent Perturbation Theory

(sec-tdpt-1)=

## Introduction

Time-dependent perturbation theory applies to Hamiltonians of the form

:::{math}
:label: eq-tdpt-1
H=H_0 + H_1(t),
:::

where $H_0$ is solvable and $H_1$ is treated as a perturbation. In bound state perturbation theory (see {ref}`ch-pertth`) we were interested in the the shifts in the energy levels and eigenfunctions of the unperturbed system induced by the perturbation $H_1$, which was assumed to be time-independent. In time-dependent perturbation theory, on the other hand, we are usually interested in time-dependent transitions between eigenstates of the unperturbed system induced by the perturbation $H_1$. In time-dependent perturbation theory the perturbation $H_1$ is allowed to depend on time, as indicated by {eq}`eq-tdpt-1`, but it does not have to be time-dependent, and in fact in practice often it is not. Time-dependent perturbation theory is especially useful in scattering theory, problems involving the emission and absorption of radiation, and in field theoretic problems of various kinds. Such problems will occupy us for the rest of the course.

Time-dependent transitions are usually described by the *transition amplitude*, defined as the quantity

:::{math}
:label: eq-tdpt-2
\matrixelement{f}{U(t)}{i},
:::

where $U(t)$ is the exact time evolution operator for the Hamiltonian {eq}`eq-tdpt-1`, and where $\ket{i}$ and $\ket{f}$ are two eigenstates of the unperturbed Hamiltonian $H_0$ (the “initial” and “final” states). The transition amplitude can be regarded as simply a matrix element of the exact time evolution operator in the eigenbasis of the unperturbed Hamiltonian, but it is also the amplitude to find the system in state $\ket{f}$ when it was known to be in the state $\ket{i}$ at $t=0$. Thus, the absolute square of the transition amplitude is the *transition probability*, the probability to make the transition $i\to f$ in time $t$. Often we are interested in transitions to some collection of final states, in which case we must sum the transition probabilities over all these states.

In these notes we shall develop the basic formalism of time-dependent perturbation theory and study some simple examples. For the most part we shall simply follow the formulas to see where they lead, without examining the conditions of validity or the limitations of the results. We will address those questions in the context of some examples, both in these and in successive notes.

(sec-tdpt-2)=

## Time-Evolution Operators

Let us denote the unperturbed time-evolution operator by $U_0(t)$ and the exact one by $U(t)$. Since the full Hamiltonian may depend on time, the exact time-evolution operator actually depends on two times, $t$ and $t_0$, but we shall set $t_0=0$ and just write $U(t)$. See {ref}`sec-tevolut-2`. These operators satisfy the evolution equations,

:::{math}
:label: eq-tdpt-3a
\begin{aligned}
i\hbar\frac{\partial U_0(t)}{\partial t} &= H_0 U_0(t),
\end{aligned}
:::

:::{math}
:label: eq-tdpt-3b
\begin{aligned}
i\hbar\frac{\partial U(t)}{\partial t} &= H(t) U(t),
\end{aligned}
:::

which are versions of {eq}`eq-tevolut-13`. Since $H_0$ is independent of time, {eq}`eq-tdpt-3a` can be solved,

:::{math}
:label: eq-tdpt-4
U_0(t) = e^{-iH_0t/\hbar},
:::

but if $H_1$ depends on time then there is no similarly simple expression for $U(t)$.

(sec-tdpt-3)=

## The Interaction Picture

The *interaction picture* is a picture that is particularly convenient for developing time-dependent perturbation theory. It is intermediate between the Schr\"odinger and Heisenberg pictures that were discussed in {ref}`sec-tevolut-5`. Recall that in the Schr\"odinger picture, the kets evolve in time but the operators do not (at least if they have no explicit time dependence), while in the Heisenberg picture the kets do not evolve but the operators do. In the interaction picture, the time evolution of the kets in the Schr\"odinger picture that is due to the unperturbed system $H_0$ is stripped off, leaving only the evolution due to the perturbation $H_1$. This is presumably slower than the evolution due to the whole Hamiltonian $H$, since $H_1$ is assumed small compared to $H_0$. We will not attempt to state precisely what “small” means in this context, rather we will develop the perturbation expansion as a power series in $H_1$ and then examine its limitations in various examples.

In the following we shall use an $S$ subscript on kets and operators in the Schr\"odinger picture, and an $I$ on those in the interaction picture. We will not use the Heisenberg picture in these notes. If the subscript is omitted, the Schr\"odinger picture will be assumed. The the relation between the kets in the Schr\"odinger and interaction pictures is

:::{math}
:label: eq-tdpt-5
\ket{\psi_I(t)} = U_0^\hc(t) \ket{\psi_S(t)}.
:::

Compare this to {eq}`eq-tevolut-17`, which shows the relation between kets in the Schr\"odinger and Heisenberg pictures. The difference is that in {eq}`eq-tdpt-5` we are only stripping off the evolution due to $H_0$, not the whole time evolution. Notice that at $t=0$ the Schr\"odinger and interaction picture kets agree,

:::{math}
:label: eq-tdpt-6
\ket{\psi_I(0)} = \ket{\psi_S(0)}.
:::

As for operators in the interaction picture, they are defined by

:::{math}
:label: eq-tdpt-7
A_I(t) = U_0^\hc(t) A_S(t) U_0(t).
:::

In practice $A_S$ is often time-independent, but $A_I$ is always time-dependent. Compare this to {eq}`eq-tevolut-19`, which shows the relation between operators in the Schr\"odinger and Heisenberg pictures.

(sec-tdpt-4)=

## Evolution in the Interaction Picture

Let us define $W(t)$ as the operator that evolves kets in the interaction picture forward from time 0 to final time $t$:

:::{math}
:label: eq-tdpt-8
\ket{\psi_I(t)} = W(t) \ket{\psi_I(0)}.
:::

The operator $W(t)$ is a time-evolution operator, but we use the symbol $W$ to avoid confusion with the two other time-evolution operators introduced so far, $U_0(t)$ and $U(t)$.

It is easy to find a relation among these three operators. Substituting {eq}`eq-tdpt-5` and {eq}`eq-tdpt-6` into {eq}`eq-tdpt-8`, we have

:::{math}
:label: eq-tdpt-9
\ket{\psi_I(t)} = U_0(t)^\hc \ket{\psi_S(t)} = U_0(t)^\hc U(t) \ket{\psi_S(0)}= U_0(t)^\hc U(t)\ket{\psi_I(0)},
:::

or, since $\ket{\psi_I(0)}$ is arbitrary,

:::{math}
:label: eq-tdpt-10
W(t) = U_0(t)^\hc U(t).
:::

The operator $W(t)$ is equivalent to first evolving forward for time $t$ under the exact Hamiltonian, then evolving backwards for the same time under the unperturbed Hamiltonian.

(sec-tdpt-5)=

## The $S$-Matrix

For an application in which the interaction picture leads to a interesting perspective, consider a scattering experiment in which a wave packet is directed against a target, described by a potential $U(\xvec)$. We assume that the potential dies off rapidly with distance, and that at the initial time the wave packet is far enough away from the scatterer that it is essentially free. For simplicity we assume that the potential (or other perturbing Hamiltonian) is time-independent.

Initially the wave packet evolves according to the free particle Hamiltonian, since it does not overlap with the potential. That is, the wave packet moves with an average velocity and simultaneously spreads, as studied in Prob. {ref}`prob-tevolut-3`. After some time, however, the wave packet begins to interact with the potential, producing a scattered wave that radiates outward from the potential in various directions. Depending on the size of the wave packet and that of the scatterer, some of the wave packet may effectively miss the scatterer and proceed in the forward direction, largely unaffected by the scattering process. In any case, after some time the scattered wave and the remaining part of the incident wave packet move away from the scatterer, and once again evolve according to the free particle Hamiltonian. Thus, the exact time evolution is that of a free particle both at large negative times and large positive times.

Let us now view the evolution of the quantum state in the interaction picture. Initially and for large negative times the wave function in the Schr\"odinger picture evolves according the free particle Hamiltonian, so in the interaction picture the wave function does not evolve at all. The wave function in the interaction picture does not begin to change until the wave packet in the Schr\"odinger picture starts to interact with the potential. Then the wave packet in the interaction picture does evolve, and continues to do so as long as the Schr\"odinger wave function has any overlap with the scatterer. As the Schr\"odinger wave function leaves the region of the scatterer, however, the wave function in the interaction picture ceases to evolve, and at large positive times it approaches another, constant wave function.

Thus, the interaction picture kets $\ket{\psi_I(-T)}$ and $\ket{\psi_I(T)}$ approach constant kets as $T\to\infty$. The scattering process associates a given initial state $\lim_{T\to\infty}\ket{\psi_I(-T)}$ with a definite final state $\lim_{T\to\infty}\ket{\psi_I(T)}$. This association is linear, and defines the $S$-*matrix*. It is usually called a “matrix” but really it is an operator, whose matrix elements in some basis form a matrix. The usual basis is that of free particle states, that is, plane waves. In this form, the $S$-matrix bears a close relationship to the cross .

We can easily express the $S$-matrix (or operator) in terms of time-evolution operators. Since

:::{math}
:label: eq-tdpt-11
\ket{\psi_I(-T)} = W(-T)\ket{\psi_I(0)} \quad and \quad \ket{\psi_I(T)}=W(T)\ket{\psi_I(0)},
:::

we have

:::{math}
:label: eq-tdpt-12
\ket{\psi_I(T)} = W(T)W(-T)^\dagger\ket{\psi_I(-T)}.
:::

But

:::{math}
:label: eq-tdpt-13
W(T)W(-T)^\dagger = U_0^\dagger(T) U(T) [U_0^\dagger(-T) U(-T)]^\dagger = U_0^\dagger(T) U(2T) U_0^\dagger(T),
:::

where we have used $U_0^\dagger(T)=U_0(-T)$ and $U^\dagger(T)=U(-T)$. But by the definition of the $S$ operator, this implies

:::{math}
:label: eq-tdpt-14
S = \lim_{T\to\infty} U_0^\dagger(T) U(2T) U_0^\dagger(T).
:::

The $S$-matrix is a central object in advanced treatments of scattering theory, but its mathematics involves noncommuting limits and is tricky. In these notes we take a simpler approach to scattering theory, one that involves a straightforward perturbation expansion of the operator $W(t)$ in powers of the perturbing Hamiltonian $H_1$.

(sec-tdpt-6)=

## The Dyson Series

We obtain a differential equation for $W(t)$ by differentiating {eq}`eq-tdpt-10` and using {eq}`eq-tdpt-3a`,

:::{math}
\begin{aligned}
i\hbar \frac{\partial W(t)}{\partial t} &= i\hbar \frac{\partial U_0(t)^\hc}{\partial t} U(t) + U_0(t)^\hc\, i\hbar \frac{\partial U(t)}{\partial t} = -U_0(t)^\hc H_0 U(t) + U_0(t)^\hc HU(t)
\end{aligned}
:::

:::{math}
:label: eq-tdpt-15
\begin{aligned}
&= U_0(t)^\hc H_1U(t) = [U_0(t)^\hc H_1 U_0(t)] [ U_0(t)^\hc U(t)],
\end{aligned}
:::

where we have used $H=H_0+H_1$ in the third equality, whereupon the terms in $H_0$ cancel. The result can be written,

:::{math}
:label: eq-tdpt-16
i\hbar \frac{\partial W(t)}{\partial t} = H_{1I}(t) W(t),
:::

an equation of the same form as {eq}`eq-tdpt-3a`, but one in which only the perturbing Hamiltonian $H_1$ appears, and that in the interaction picture. By applying both sides of {eq}`eq-tdpt-16` to the initial state $\ket{\psi_I(0)}$, we obtain a version of the Schr\"odinger equation in the interaction picture,

:::{math}
:label: eq-tdpt-17
i\hbar \pop{\ket{\psi_I(t)}}{t} = H_{1I}(t) \ket{\psi_I(t)}.
:::

It is now easy to obtain a solution for $W(t)$ as a power series in the perturbing Hamiltonian $H_1$. First we integrate {eq}`eq-tdpt-16` between time 0 and time $t$, obtaining

:::{math}
:label: eq-tdpt-18
W(t) = 1 + {1\over i\hbar} \int_0^t dt' \, H_{1I}(t')W(t'),
:::

where we have used $W(0)=1$. This is an exact result, but it is not a solution for $W(t)$, since $W(t)$ appears on the right-hand side. But by substituting the left-hand side of {eq}`eq-tdpt-18` into the right-hand side, that is, iterating the equation, we obtain

:::{math}
:label: eq-tdpt-19
W(t) = 1 + {1\over i\hbar} \int_0^t dt' \, H_{1I}(t') + {1\over (i\hbar)^2} \int_0^t dt' \int_0^{t'} dt'' \, H_{1I}(t') H_{1I}(t'')W(t''),
:::

another exact equation in which the term containing $W(t)$ on the right hand side has been pushed to second order. Substituting {eq}`eq-tdpt-18` into the right-hand side of {eq}`eq-tdpt-19` pushes the term in $W(t)$ to third order, etc. Continuing in this way, we obtain a formal power series for $W(t)$,

:::{math}
:label: eq-tdpt-20
W(t) = 1 +{1\over i\hbar} \int_0^t dt' \, H_{1I}(t') +{1\over (i\hbar)^2} \int_0^t dt' \, \int_0^{t'} dt'' \, H_{1I}(t') H_{1I}(t'') +\ldots.
:::

This series is called the *Dyson series*. It is obviously a kind of a series expansion of $W(t)$ in powers of $H_1$.

(sec-tdpt-7)=

## The Usual Problem

Let us assume for simplicity that $H_0$ has a discrete spectrum, and let us write

:::{math}
:label: eq-tdpt-21
H_0\ket{n} = E_n \ket{n},
:::

where $n$ is a discrete index. The usual problem in time-dependent perturbation theory is to assume that the system is initially in an eigenstate of the unperturbed system, what we will call the “initial” state $\ket{i}$ with energy $E_i$,

:::{math}
:label: eq-tdpt-22
H_0 \ket{i} = E_i \ket{i}.
:::

This is just a special case of {eq}`eq-tdpt-21` (with $n=i$). That is, we assume the initial conditions are

:::{math}
:label: eq-tdpt-23
\ket{\psi_I(0)} = \ket{\psi_S(0)} = \ket{i}.
:::

We will be interested in finding the state of the system at a later time,

:::{math}
:label: eq-tdpt-24
\ket{\psi_I(t)} = W(t)\ket{i}.
:::

By applying the Dyson series {eq}`eq-tdpt-20` to this equation, we obtain a perturbation expansion for $\ket{\psi_I(t)}$,

:::{math}
:label: eq-tdpt-25
\ket{\psi_I(t)} = \ket{i}+ {1\over i\hbar} \int_0^t dt' \, H_{1I}(t')\ket{i} +{1\over (i\hbar)^2} \int_0^t dt' \, \int_0^{t'} dt'' \, H_{1I}(t') H_{1I}(t'')\ket{i} + \ldots.
:::

(sec-tdpt-8)=

## Transition Amplitudes

Let us expand the exact solution of the Schr\"odinger equation in the interaction picture in the unperturbed eigenstates,

:::{math}
:label: eq-tdpt-26
\ket{\psi_I(t)} = \sum_n c_n(t) \ket{n},
:::

with coefficients $c_n(t)$ that are functions of time. We can solve for these coefficients by multiplying {eq}`eq-tdpt-26` on the left by the bra $\bra{n}$, which gives

:::{math}
:label: eq-tdpt-27
c_n(t) = \matrixelement{n}{W(t)}{i},
:::

showing that $c_n(t)$ is a transition amplitude in the interaction picture, that is, a matrix element of the time-evolution operator $W(t)$ in the interaction picture with respect to the unperturbed eigenbasis. These are not the same as the transition amplitudes {eq}`eq-tdpt-2`, which are the matrix elements of $U(t)$ (the time-evolution operator for kets in the Schr\"odinger picture) with respect to the unperturbed eigenbasis. There is, however, a simple relation between the two. That is, substituting {eq}`eq-tdpt-10` into {eq}`eq-tdpt-27`, we have

:::{math}
:label: eq-tdpt-28
c_n(t) = \matrixelement{n}{U_0(t)^\hc U(t)}{i} = e^{iE_nt/\hbar} \, \matrixelement{n}{U(t)}{i},
:::

where we have allowed $U_0(t)^\hc$ to act to the left on bra $\bra{n}$. We see that the transition amplitudes in the interaction picture and those in the Schr\"odinger picture are related by a simple phase factor. The phase factor removes the rapid time evolution of the transition amplitudes in the Schr\"odinger picture due to the unperturbed system, leaving behind the slower evolution due to $H_1$. The transition probabilities are the squares of the amplitudes and are the same in either case,

:::{math}
:label: eq-tdpt-29
P_n(t) = |c_n(t)|^2 = |\matrixelement{n}{W(t)}{i}|^2 = |\matrixelement{n}{U(t)}{i}|^2.
:::

The perturbation expansion of the transition amplitude $c_n(t)$ is easily obtained by multiplying {eq}`eq-tdpt-25` by the bra $\bra{n}$. We write the result in the form,

:::{math}
:label: eq-tdpt-30
c_n(t) = \delta_{ni} + c_n^{(1)}(t) + c_n^{(2)}(t) + \ldots,
:::

where the parenthesized numbers indicate the order of perturbation theory, and where

:::{math}
:label: eq-tdpt-31a
\begin{aligned}
c_n^{(1)}(t) &= {1\over i\hbar} \int_0^t dt' \, \matrixelement{n}{H_{1I}(t')}{i},
\end{aligned}
:::

:::{math}
:label: eq-tdpt-31b
\begin{aligned}
c_n^{(2)}(t) &= {1\over (i\hbar)^2} \int_0^t dt' \, \int_0^{t'} dt'' \, \matrixelement{n}{H_{1I}(t') H_{1I}(t'')}{i},
\end{aligned}
:::

etc.

We now switch back to the Schr\"odinger picture in the expressions for the $c_n^{(r)}$. The interaction picture is useful for deriving the perturbation expansion, but the Schr\"odinger picture is more convenient for subsequent calculations. For $c_n^{(1)}$, we have

:::{math}
\begin{aligned}
c_n^{(1)}(t) &= {1\over i\hbar} \int_0^t dt'\, \matrixelement{n}{U_0^\hc(t') H_1(t') U_0(t')}{i}
\end{aligned}
:::

:::{math}
:label: eq-tdpt-32
\begin{aligned}
& \qquad= {1\over i\hbar} \int_0^t dt'\, e^{i\omega_{ni} t'} \, \matrixelement{n}{H_1(t')}{i},
\end{aligned}
:::

where we have allowed $U_0(t')^\hc$ and $U_0(t')$ to act to the left and right, respectively, on bra $\bra{n}$ and ket $\ket{i}$, bringing out the phase factor $e^{i\omega_{ni}t'}$ where $\omega_{ni}$ is the Einstein frequency connecting unperturbed states $n$ and $i$,

:::{math}
:label: eq-tdpt-33
\omega_{ni} = {E_n - E_i \over \hbar}.
:::

As for $c_n^{(2)}$, it is convenient to introduce a resolution of the identity $\sum \ketbra{k}{k}$ between the two factors of $H_{1I}$ in {eq}`eq-tdpt-31b` before switching to the Schr\"odinger picture. This gives

:::{math}
:label: eq-tdpt-34
c_n^{(2)}(t) = {1\over(i\hbar)^2} \int_0^{t} dt' \, \int_0^{t'} dt'' \, \sum_k e^{i\omega_{nk} t' + i\omega_{ki} t''} \, \matrixelement{n}{H_1(t')}{k} \matrixelement{k}{H_1(t'')}{i}.
:::

From this the pattern at any order of perturbation theory should be clear. In {eq}`eq-tdpt-34`, the states $\ket{k}$ are known as *intermediate states*, the idea being that there is a time sequence as we move from the right to the left in the product of matrix elements, starting with the initial state $\ket{i}$, moving through the intermediate state $\ket{k}$ and ending with the final state $\ket{n}$. Notice that the variables of integration satisfy $t\ge t' \ge t'' \ge 0$.

(sec-tdpt-9)=

## The Case that $H_1$ is Time-independent

This is about as far as we can go without making further assumptions about $H_1$, so that we can do the time integrals. Let us now assume that $H_1$ is time-independent, an important case in practice. Then the matrix elements are independent of time and can be taken out of the integrals, and the integrals that remain are elementary. For example, in {eq}`eq-tdpt-32` we have the integral

:::{math}
:label: eq-tdpt-35
\int_0^t dt' \, e^{i\omega t'} =  2 e^{i\omega t/2} \, {\sin \omega t/2 \over \omega},
:::

so that

:::{math}
:label: eq-tdpt-36
c_n^{(1)}(t) = {2\over i\hbar} e^{i\omega_{ni} t/2} \Bigl( {\sin \omega_{ni}t/2 \over \omega_{ni}}\Bigr) \matrixelement{n}{H_1}{i}.
:::

The case of $c_n^{(2)}$ is similar but more complicated. We will return to it in {ref}`ch-photscatt`{} when we apply second order time-dependent perturbation theory to the problem of the scattering of photons.

The transition probability $P_n(t)$ can also be expanded in the perturbation series,

:::{math}
:label: eq-tdpt-37
P_n(t) = |c_n(t)|^2 = |\delta_{ni} + c_n^{(1)}(t) + c_n^{(2)}(t) + \ldots|^2.
:::

Notice that on taking the square there are cross terms, that is, interference terms between the amplitudes at different orders.

For now we assume that the final state we are interested in is not the the initial state, that is, we take the case $n \ne i$ so the first term in {eq}`eq-tdpt-37` vanishes, and we work only to first order of perturbation theory. Then we have

:::{math}
:label: eq-tdpt-38
P_n(t) = | c_n^{(1)}(t)|^2 = {4\over\hbar^2} \Bigl( {\sin^2 \omega_{ni}t/2 \over \omega_{ni}^2} \Bigr) |\matrixelement{n}{H_1}{i}|^2.
:::

The transition probability depends on time and on the final state $n$. As for the time dependence, it is contained in the first factor in the parentheses, while both this factor and the matrix element depend on the final state $\ket{n}$. However, the factor in the parentheses depends on the state $n$ only through its energy $E_n$, which is contained in the Einstein frequency $\omega_{ni}$, while the matrix element depends on all the properties of the state $\ket{n}$, for example, its momentum, spin, etc.

The case $n=i$ is interesting, too, as it gives the amplitude and probability for the system to remain in the initial state. This case will be analyzed in some detail in {ref}`ch-nlw`.

(sec-tdpt-10)=

## The Case of Time-Periodic Perturbations

Another case that is important in practice is when $H_1$ has a periodic time dependence of the form

:::{math}
:label: eq-tdpt-39
H_1(t) = K e^{-i\omega_0t} + K^\hc e^{i\omega_0t},
:::

where $\omega_0$ is the frequency of the perturbation and $K$ is an operator (generally not Hermitian). We call the first and second terms in this expression the positive and negative frequency components of the perturbation, respectively. This case applies, for example, to the interaction of spins or atoms with a given, classical electromagnetic wave, a problem that is studied in {ref}`ch-photelec`.

To find the transition amplitude in this case we substitute {eq}`eq-tdpt-39` into {eq}`eq-tdpt-32` and perform the integration, whereupon we obtain two terms,

:::{math}
\begin{aligned}
c_n^{(1)}(t) = {2\over i\hbar} \Bigl[ &e^{i(\omega_{ni}-\omega_0)t/2} \, {\sin(\omega_{ni}-\omega_0)t/2 \over \omega_{ni}-\omega_0} \, \matrixelement{n}{K}{i}
\end{aligned}
:::

:::{math}
:label: eq-tdpt-40
\begin{aligned}
+&e^{i(\omega_{ni}+\omega_0)t/2} \, {\sin(\omega_{ni}+\omega_0)t/2 \over \omega_{ni}+\omega_0} \, \matrixelement{n}{K^\hc}{i}\Bigr].
\end{aligned}
:::

For any given final state $n$, both these terms are present and contribute to the transition amplitude, and when we square the amplitude to get the transition probability, there are cross terms (interference terms) between these two contributions to the amplitude.

Often, however, we are most interested in those final states to which most of the probability goes, which are the states for which one or the other of the two denominators in {eq}`eq-tdpt-40` is small. For these states we have $\omega_{ni}\mp\omega_0\approx0$, or

:::{math}
:label: eq-tdpt-41
E_n \approx E_i \pm \hbar\omega_0.
:::

We see that the first (positive frequency) term is resonant when the system has absorbed a quantum of energy $\hbar\omega_0$ from the perturbation, whereas the second (negative frequency) term is resonant when the system has given up a quantum of energy $\hbar\omega_0$ to the perturbation. We call these two cases *absorption* and *stimulated emission*, respectively.

Taking the case of absorption, and looking only at final states $\ket{n}$ that are near resonance ($E_n \approx E_i + \hbar\omega_0$), we can write the transition probability to first order of perturbation theory as

:::{math}
:label: eq-tdpt-42
P_n = {4\over \hbar^2} \Bigl[ {\sin^2(\omega_{ni}-\omega_0)t/2 \over (\omega_{ni}-\omega_0)^2}\Bigr] |\matrixelement{n}{K}{i}|^2.
:::

Similarly, for nearly resonant final states in stimulated emission, we have

:::{math}
:label: eq-tdpt-43
P_n = {4\over \hbar^2} \Bigl[ {\sin^2(\omega_{ni}+\omega_0)t/2 \over (\omega_{ni}+\omega_0)^2}\Bigr] |\matrixelement{n}{K^\hc}{i}|^2.
:::

These formulas may be compared to {eq}`eq-tdpt-38`. In all cases, $P_n$ has a dependence on time that is described by functions of a similar form.

(sec-tdpt-11)=

## How $P_n$ Depends on Time

Let us fix the final state $\ket{n}$ and examine how the probability $P_n(t)$ develops as a function of time in first order time-dependent perturbation theory. To be specific we will take the case of a time-independent perturbation and work with {eq}`eq-tdpt-38`, but with $\omega_{ni}$ replaced by $\omega_{ni}\pm\omega_0$ and $H_1$ replaced by $K$ or $K^\hc$, everything we say also applies to absorption or stimulated emission.

Obviously $P_n(0) = 0$ (because $n\ne i$ and all the probability lies in state $\ket{i}$ at $t=0$). At later times we see that $P_n(t)$ oscillates at frequency $\omega_{ni}$ between 0 and a maximum proportional to $1/\omega_{ni}^2$. The frequency $\omega_{ni}$ measures how far the final state is “off resonance,” that is, how much the final energy differs from the initial energy. In some applications this difference can be regarded as a failure to conserve energy, which is allowed over finite time intervals by the energy-time uncertainty relation $\Delta E \Delta t >\approx \hbar$. If $\omega_{ni}$ is large, the probability $P_n(t)$ oscillates rapidly between zero and a small maximum. But as we move the state $\ket{n}$ closer to the initial state $\ket{i}$ in energy, $\omega_{ni}$ gets smaller, the period of oscillations becomes longer, and the amplitude grows.

If there is a final state $\ket{n}$ degenerate in energy with the initial state $\ket{i}$ (not the same state since we are assuming $n\ne i$), then $\omega_{ni}=0$ and the time-dependent factor in {eq}`eq-tdpt-38` takes on its limiting value, which is $t^2/4$. In this case, first order perturbation theory predicts that the probability $P_n(t)$ grows without bound, obviously an absurdity after a while since we must have $P_n \le 1$. This is an indication of the fact that at sufficiently long times first order perturbation theory breaks down and we must take into account higher order terms in the perturbation expansion. In fact, to get sensible results at such long times, it is necessary to take into account an infinite number of terms (that is, to do some kind of summation of the series). But at short times it is correct that $P_n$ for a state on resonance grows as $t^2$.

These considerations are important when the system has a discrete spectrum, for example, when a spin is interacting with a time-periodic magnetic field or when we are looking at a few discrete states of an atom in the presence of laser light. These are important problems in practice. Recall that in {ref}`ch-spinmagf`\ we solved the Schr\"odinger equation exactly for a spin in a certain kind of time-periodic magnetic field, but in more general cases an exact solution is impossible and we may have to use time-dependent perturbation theory. It is interesting to compare the exact solution presented in {ref}`ch-spinmagf`\ with the perturbative solutions presented here, to see the limitations of the perturbative solutions.

In such problems with a discrete spectrum, the resonance condition $\omega_{ni}=0$ may not be satisfied exactly for any final state $n\ne i$. In fact, in problems of emission and absorption, if the frequency $\omega_0$ of the perturbation is chosen randomly, then it is unlikely that the resonant energy $E_i \pm \hbar\omega_0$ will exactly coincide with any unperturbed energy eigenvalue. In that case, first-order theory predicts that the transition probability to all final states just oscillates in time.

On the other hand, if the final states are members of a continuum, then there are an infinite number of final states arbitrarily close to the initial state in energy. For those cases, we must examine how the transition probability depends on energy.

(sec-tdpt-12)=

## How $P_n$ Depends on Energy

Now let us fix the time $t$ and examine how the expression for $P_n(t)$ in first order perturbation theory, {eq}`eq-tdpt-38`, depends on the energy $E_n$ of the final state $\ket{n}$ (working for simplicity with the case of a time-independent perturbation). We shall concentrate on the energy dependence of the time-dependent factor in the parentheses, remembering that the matrix element also depends on the energy (and other parameters) of the final state. To do this we plot the function $\sin^2(\omega t/2)/\omega^2$ as a function of $\omega$, as shown in Figs.~{ref}`fig-tdpt-1` and {ref}`fig-tdpt-2` for two different times. In the plot, $\omega$ is to be identified with $\omega_{ni}=(E_n-E_i)/\hbar$, so that $\omega$ specifies the energy of the final state and $\omega=0$ is the resonance (energy conserving) condition.

:::{figure} images/tdpt-fig01.png
:label: fig-tdpt-1
:width: 80%

The function $\sin^2(\omega t/2)/\omega^2$ as a function of $\omega$ for fixed $t$. The dotted curve is the envelope $1/\omega^2$.
:::

:::{figure} images/tdpt-fig02.png
:label: fig-tdpt-2
:width: 80%

Same but for a larger value of $t$. The area of the curve is dominated by the central lobe, and grows in proportion to $t$.
:::


The curve consists of oscillations under the envelope $1/\omega^2$, with zeroes at $\omega=(2n\pi/t)$. The central lobe has height $t^2/4$ and width that is proportional to $1/t$, so the area of the central lobe is proportional to $t$. As $t$ increases, the central lobe grows in height and gets narrower, a behavior that reminds us of functions that approach a $\delta$-function, but in this case the limit is not a $\delta$-function because the area is not constant. In fact, the total area is given exactly by an integral that can be evaluated by contour integration,

:::{math}
:label: eq-tdpt-44
\int_{-\infty}^{+\infty} d\omega \, {\sin^2\omega t/2 \over \omega^2} = {\pi t\over 2},
:::

showing that the area is indeed proportional to $t$. Thus if we divide by $t$ we do get a $\delta$-function as $t\to \infty$,

:::{math}
:label: eq-tdpt-45
\lim_{t\to\infty} {1\over t} {\sin^2\omega t/2 \over \omega^2} = {\pi\over 2} \delta(\omega).
:::

For fixed $\omega\ne0$ the function under the limit in this expression approaches 0 as $t\to\infty$, while exactly at $\omega=0$ it grows in proportion to $t$, with a constant total area. This is exactly the behavior that produces a $\delta$-function in the limit.

In physical applications we never really go to infinite time, rather we work with times long enough that there is negligible error in replacing the function on the left-hand side of {eq}`eq-tdpt-45` by its limit. To deal with the case of finite time, we introduce the notation,

:::{math}
:label: eq-tdpt-46
{\sin^2 \omega t/2 \over \omega^2} = {\pi \over 2} t \Delta_t(\omega),
:::

which defines the function $\Delta_t(\omega)$. Then the limit {eq}`eq-tdpt-45` can be written,

:::{math}
:label: eq-tdpt-47
\lim_{t\to\infty} \Delta_t(\omega) = \delta(\omega).
:::

As we shall see when we take up some applications, the $\delta$-function in {eq}`eq-tdpt-45` enforces energy conservation in the limit $t\to\infty$, that is, only transitions to final states of the same energy as the initial state are allowed in that limit. At finite times, transitions take place to states in a range of energies about the initial energy, given in frequency units by the width of the function $\Delta_t(\omega)$. But as we have seen this width is of order $1/t$, or, in energy units, $\hbar/t$. This is an example of the energy-time uncertainty relation, $\Delta E \Delta t >\approx \hbar$, indicating that a system that is isolated over a time interval $\Delta t$ has an energy that is uncertain by an amount $\Delta E >\approx \hbar/\Delta t$.

Now we can write the transition probability {eq}`eq-tdpt-38` as

:::{math}
:label: eq-tdpt-48
P_n(t) = {2\pi t \over \hbar^2} \Delta_t(\omega_{ni}) \, |\matrixelement{n}{H_1}{i}|^2.
:::

This applies in first order perturbation theory, in the case $n \ne i$.

(sec-tdpt-13)=

## Cross and Differential Cross In preparation for applications to scattering, we make a digression to define and discuss cross s and differential cross s. These concepts are best understood in a classical context, but most of the ideas carry over without trouble into quantum mechanics.

:::{figure} images/tdpt-fig03.png
:label: fig-tdpt-3
:width: 80%

Classical scattering of particles. The outgoing asymptotic direction ${\hat{\mathbf{n}}}=(\theta,\phi)$ is a function of the impact parameter $\bvec$.
:::

We first discuss classical scattering from a fixed target, which is illustrated in {ref}`fig-tdpt-3`. An incident beam of particles of momentum $\pvec$ and uniform density is directed against a target, illustrated by the shaded region in the figure. The target is described by a potential $U(\xvec)$. The origin of a coordinate system is located in or near the target, and in the figure the beam is directed in the $z$-direction. A transverse plane $T$ is erected perpendicular to the beam at a large, negative value of $z$, where the potential $U(\xvec)$ is negligible. The plane $T$ is parallel to the $x$-$y$ plane, and when the particles cross it their momentum is purely in the $z$-direction, since no interaction with the potential has occurred yet. The negative $z$-axis is extended back to the plane $T$ along a center line $C$, intersecting it at point $O$, which serves as an origin in the plane.

The trajectory of one particle is illustrated in the figure. It crosses the plane $T$ at a position described by the *impact parameter*, a vector $\bvec$, which goes from the origin $O$ in the plane to the interpoint. The impact parameter only has $x$- and $y$-components. The particle continues forward and interacts with the potential, going out in some direction ${\hat{\mathbf{n}}}=(\theta,\phi)$. This direction is defined asymptotically, that is, it is the direction of the particle's momentum when it is once again at a large distance from the target. The outgoing direction is a function of the impact parameter,

:::{math}
:label: eq-tdpt-49
{\hat{\mathbf{n}}}={\hat{\mathbf{n}}}(\bvec),
:::

which can be determined by integrating the equations of motion from given initial conditions on the plane $T$.

{eq}`eq-tdpt-49` defines a mapping from the transverse plane $T$ to the unit sphere of outgoing directions, and the differential cross is closely related to the Jacobian of this map. That is, $d\sigma/d\Omega$ is the ratio of an infinitesimal area element in $T$ to a corresponding infinitesimal solid angle on the sphere.

To visualize this in more detail, we construct a small cone of solid angle $\Delta\Omega$, centered on the outgoing direction ${\hat{\mathbf{n}}}=(\theta,\phi)$, as illustrated in {ref}`fig-tdpt-4`. The particles whose asymptotic, outgoing directions lie inside this cone cross the plane $T$ inside an area indicated by the shaded area in plane $T$ in the figure. This area represents the portion of the incident flux of particles that is directed into the small cone by the scattering process. It defines the *differential cross * $d\sigma/d\Omega$ by the formula,

:::{math}
:label: eq-tdpt-50
Area = \dod{\sigma}{\Omega} \, \Delta\Omega.
:::

The differential cross $d\sigma/d\Omega$ is a function of $(\theta,\phi)$.

It is possible that more than one impact parameter $\bvec$ will lead to the same final outgoing direction ${\hat{\mathbf{n}}}$, for example, depending on $\bvec$ a particle may orbit the target one or more times before emerging in a definite final direction. In that case the area in {eq}`eq-tdpt-50` should be replaced by a sum of areas, each corresponding to the same small solid angle $\Delta\Omega$ in the outgoing direction.

:::{figure} images/tdpt-fig04.png
:label: fig-tdpt-4
:width: 80%

A subset of particles goes out into a small cone of solid angle $\Delta\Omega$ centered on the direction ${\hat{\mathbf{n}}}=(\theta,\phi)$. They cross the plane $T$ inside an area which is $(d\sigma/d\Omega)\Delta\Omega$.
:::

Another point of view deals with counting rates. We use the symbol $w$ to stand for a rate, with dimensions of $time^{-1}$, for example, number of particles per unit time or probability per unit time. A detector situated in {ref}`fig-tdpt-4` so as to intercept all particles coming out in the cone will have a counting rate given by the rate at which particles cross the shaded area in plane $T$. We denote this counting rate by $(dw/d\Omega)\Delta\Omega$. But this is just the flux of incident particles times the shaded area, that is,

:::{math}
:label: eq-tdpt-51
\dod{w}{\Omega} = J_inc \,\dod{\sigma}{\Omega}.
:::

As for the incident flux, it is given by

:::{math}
:label: eq-tdpt-52
\Jvec_inc = n\vvec,
:::

where $n$ is the number of particles per unit volume in the incident beam and $\vvec=\pvec/m$ is the incident velocity. The magnitude $J_inc = |\Jvec_inc|$ appears in {eq}`eq-tdpt-51`, since the transverse plane is orthogonal to the velocity $\vvec$. It is obvious that the counting rate is proportional to the incident flux, so {eq}`eq-tdpt-51` gives another way of thinking about the differential cross : It is the counting rate, normalized by the incident flux.

The total scattering rate $w$ is the rate at which particles are scattered at any nonzero angle. It is the integral of the differential scattering rate,

:::{math}
:label: eq-tdpt-53
w = \int d\Omega \, \dod{w}{\Omega}.
:::

It is related to the total cross $\sigma$ by

:::{math}
:label: eq-tdpt-54
w = J_inc\,\sigma,
:::

where

:::{math}
:label: eq-tdpt-55
\sigma = \int d\Omega \, \dod{\sigma}{\Omega}.
:::

In classical scattering, the total cross is often infinite, due to a large number of particles that are scattered by only a small angle.

The relation {eq}`eq-tdpt-51` applies in the case of a single scatterer located inside the incident beam. In many practical circumstances there are multiple, identical scatterers. An example is Rutherford's scattering experiment, in which a beam of $\alpha$-particles is directed against a gold foil. The individual gold nuclei are the scatterers, of which there are a large number in the region of the foil crossed by the beam.

In this case we can speak of the scattering rate (differential or total) per unit volume of the scattering material, which is $n_inc n_targ v$ times the cross (differential or total), where $n_inc$ and $n_targ$ are the number of incident particles and scatterers per unit volume, respectively. Then integrating over the interaction region, we find that {eq}`eq-tdpt-51` is replaced by

:::{math}
:label: eq-tdpt-56
\dod{w}{\Omega} = \dod{\sigma}{\Omega} v \int d^3\xvec \, n_inc n_targ,
:::

where $v$ is again the velocity of the beam. In this formula, both $n_inc$ and $n_targ$ can be functions of position, as they often are in practice. We are assuming that $v$ is constant, so that it can be taken out of the integral (the beam consists of particles of a given momentum).

Another case that is common in practice is when there are two beams intersecting one another. In this case it is easiest to work in the center-of-mass frame, in which the momenta of the particles in the two beams are equal and opposite. As we have seen in {ref}`ch-cenforce`, when two particles interact by means of a central force potential, their relative motion is described by a pseudo-one-body problem. Thus, the results for scattering from a fixed target with central force potential $U$ can be transcribed into those for scattering of two particles in the center of mass frame, in which the position vector $\xvec$ of the beam particle relative to the scatterer is replaced by $\rvec=\xvec_2 -\xvec_1$, the relative position vector between two particles in the two beams, and where the mass $m$ of the beam particle is replaced by the reduced mass $\mu$ of the two particle system. Then the transition rate is given by a modified version of {eq}`eq-tdpt-56`,

:::{math}
:label: eq-tdpt-57
\dod{w}{\Omega} = \dod{\sigma}{\Omega} v \int d^3\xvec \, n_1 n_2,
:::

where $n_1$ and $n_2$ are the densities of the two beams, which may be functions of position, and where $v$ is now the *relative* velocity of the two beams. The integral is taken over the region where the two beams overlap.

The transformation between the lab positions and momenta of the two particles, $(\xvec_1,\pvec_1)$ and $(\xvec_2,\pvec_2)$, and the center of mass position and momentum $(\Rvec,\Pvec)$ and the relative position and momentum $(\rvec,\pvec)$, is given by Eqs.~({eq}`eq-cenforce-44`{}--{eq}`eq-cenforce-45`) and ({eq}`eq-cenforce-50`{}--{eq}`eq-cenforce-53`). The definitions of $\Rvec$, the center of mass position, and $\Pvec=\pvec_1+\pvec_2$, the total momentum of the two particle system as seen in the lab frame, are clear physically. So also is the definition of $\rvec =\xvec_2 -\xvec_1$, the relative separation between the two particles. But the definition of $\pvec$, the momentum conjugate to $\rvec$,

:::{math}
:label: eq-tdpt-58
\pvec={m_1 \pvec_2 - m_2\pvec_1 \over m_1+m_2},
:::

requires some comment. (This is essentially {eq}`eq-cenforce-53`.

We offer two interpretations of this equation. First, we compute $\pvec/\mu$, where $\mu$ is the reduced mass, given by {eq}`eq-cenforce-58`, or, equivalently,

:::{math}
:label: eq-tdpt-59
\mu = {m_1 m_2 \over m_1 + m_2}.
:::

Dividing this into {eq}`eq-tdpt-58` gives

:::{math}
:label: eq-tdpt-60
{\pvec \over \mu} = {\pvec_2 \over m_2} - {\pvec_1 \over m_1},
:::

or,

:::{math}
:label: eq-tdpt-61
\pvec = \mu \vvec,
:::

where

:::{math}
:label: eq-tdpt-62
\vvec = \vvec_2 -\vvec_1
:::

is the relative velocity. In other words, we have a version of the usual formula $\pvec=m\vvec$, where $\pvec$ is the momentum conjugate to the relative position vector, $\vvec$ is the relative velocity, and $m$ is replaced by the reduced mass.

Another interpretation is to imagine the two particle system as seen in the center-of-mass frame, in which $\Pvec=0$. If we let $\pvec_2=\qvec$, then $\pvec_1 = -\qvec$, which when substituted into {eq}`eq-tdpt-58` gives $\pvec=\qvec$. Thus, the momentum $\pvec$, defined as the conjugate to the relative position $\rvec$, or, equivalently, by {eq}`eq-tdpt-58`, is in fact the momentum of one or the other of the particles (to within a sign) as seen in the center-of-mass frame.

(sec-tdpt-14)=

## Application:  Potential Scattering

We return now to time-dependent perturbation theory, and examine an application, namely, potential scattering of a spinless particle from a fixed target, described by a potential $U(\xvec)$. We let the unperturbed Hamiltonian be $H_0=\pvec^2/2m$ and we take the perturbation to be $H_1=U(\xvec)$, where $U$ is some potential. We do not assume the potential is rotationally invariant, but it should approach zero sufficiently fast as $r=|\xvec|\to\infty$. We will examine this condition more carefully in {ref}`sec-introscatt-10`.

The unperturbed eigenstates are free particle solutions, which we take to be plane waves. In order to deal with discrete final states, we place our system in a large box of side $L$ and volume $V=L^3$, and we adopt periodic boundary conditions. This is equivalent to dividing the universe up into boxes and demanding that all the physics be periodic, that is, the same in all the boxes. We shall assume that the size of the box is much larger than the range of the potential $U(\xvec)$. When we are done we take $V\to\infty$ to get physical results. We denote the unperturbed eigenstates by $\ket{\kvec}$, with wave functions

:::{math}
:label: eq-tdpt-63
\psi_\kvec(\xvec) = \braket{\xvec}{\kvec} = {e^{i\kvec\cdot\xvec}\over\sqrt{V}},
:::

so that

:::{math}
:label: eq-tdpt-64
\braket{\kvec}{\kvec'} = \delta_{\kvec,\kvec'}.
:::

Here we are normalizing the eigenfunctions to the volume of the box, and integrating over the volume of the box when forming scalar products as in {eq}`eq-tdpt-64`. The quantized values of $\kvec$ are given by

:::{math}
:label: eq-tdpt-65
\kvec = {2\pi\over L}\nvec,
:::

where $\nvec=(n_x,n_y,n_z)$ is a vector of integers, each of which ranges from $-\infty$ to $+\infty$. The unperturbed eigenstates can be represented as a lattice of points in $\kvec$-space, in which the lattice spacing is $2\pi/L$ and the density is $(L/2\pi)^3 = V/(2\pi)^3$. We let $\ket{\kvec_i}$ be an incident plane wave (the initial state), and $\ket{\kvec}$ be some final state.

Notice that the initial state is somewhat unrealistic from a physical standpoint. The initial state is a plane wave $\exp(i\kvec_i\cdot\xvec)$ that fills up all of space, including the region where $U(\xvec)$ is appreciably nonzero. Let us suppose it is a potential well. Thinking in classical terms, it is as if all of space is filled with particles with exactly the same momentum and energy, even the particles in the middle of the well. Of course a particle coming in from infinity and entering a potential well will gain kinetic energy, and the direction of its momentum will change (this is the scattering process in action). But the particles of our initial state in the middle of the potential have the same kinetic energy and momentum as the particles that are coming in from infinity. Obviously this initial condition would be difficult to establish in practice. Nevertheless, it turns out that these particles with the wrong energy and momentum in the initial state do not affect the transition probabilities after sufficiently long times, and so they do not affect the cross that we shall compute. All they do is give rise to short-time transients that can be regarded as nonphysical since they arise from the artificialities of the initial conditions. We shall say more about these transients below, but for now we shall just continue to follow the formulas of time-dependent perturbation theory.

In this application the perturbing Hamiltonian is time-independent, so the transition amplitude in first order perturbation theory is given by {eq}`eq-tdpt-36`, with the change of notation $\ket{i} \to \ket{\kvec_i}$, $\ket{n} \to \ket{\kvec}$, etc. The transition amplitude is

:::{math}
:label: eq-tdpt-66
c_{\kvec}^{(1)}(t) = {2\over i\hbar} \, e^{i\omega t/2} \,\Bigl( {\sin\omega t/2 \over \omega}\Bigr) \matrixelement{\kvec}{U(\xvec)}{\kvec_i},
:::

where

:::{math}
:label: eq-tdpt-67
\omega={E_\kvec - E_{\kvec_i} \over \hbar} = {\hbar \over 2m} (k^2 - k_i^2),
:::

and the transition probability is

:::{math}
:label: eq-tdpt-68
\sum_\kvec {2\pi\over\hbar^2} \, t\Delta_t(\omega) \, |\matrixelement{\kvec}{U(\xvec)}{\kvec_i}|^2,
:::

where we sum over some set of final states for which $\kvec\ne\kvec_i$. Note that {eq}`eq-tdpt-67` implies

:::{math}
:label: eq-tdpt-69
\dod{\omega}{k}={\hbar k\over m} = {p\over m} = v,
:::

where $v$ is the classical velocity of the beam particles. It is also the group velocity of free particle wave packets.

:::{figure} images/tdpt-fig05.png
:label: fig-tdpt-5
:width: 80%

To compute the differential transition rate $dw/d\Omega$, we sum over all lattice points in $\kvec$-space lying in a small cone of solid angle $\Delta\Omega$ centered on some final vector $\kvec_f$ of interest. The direction ${\hat{\mathbf{n}}}_f$ of $\kvec_f$ determines the $(\theta,\phi)$ dependence of the differential cross .
:::

Which final states $\kvec$ do we sum over? This depends on what question we wish to ask. If we are interested in the transition rate to any final state, then we sum over all of them (every lattice point in $\kvec$-space except $\kvec_i$). Often, however, we are interested in more refined information. In the present case, let us sum over all final states (lattice points) that lie in a cone of small solid angle $\Delta\Omega\ll 1$ in $\kvec$-space, as illustrated in {ref}`fig-tdpt-5`. Let the cone be centered on a direction ${\hat{\mathbf{n}}}_f$, a given unit vector pointing toward some counting device in a scattering experiment. Then we define a “final wave vector” $\kvec_f$ by requiring that $\kvec_f$ have the same direction as ${\hat{\mathbf{n}}}_f$, and that it satisfy conservation of energy,

:::{math}
:label: eq-tdpt-70
{\hbar^2 k_f^2 \over 2m} = {\hbar^2 k_i^2 \over 2m},
:::

that is, $k_f = k_i$. Then

:::{math}
:label: eq-tdpt-71
\kvec_f = k_i {\hat{\mathbf{n}}}_f.
:::

This is only a definition, and although $\kvec_f$ satisfies energy conservation, notice that the states in the cone that we sum over include states of all energies, from 0 to $\infty$.

With this understanding of the states we sum over in the expression {eq}`eq-tdpt-68`, we see that we are computing the probability as a function of time that the system will occupy a momentum state lying in the cone. Under some circumstances transition probabilities are proportional to time, and then we can refer to a *transition rate* as the probability per unit time for the process in question. We will generally use the symbol $w$ for transition rates. In the present case, we divide the probability {eq}`eq-tdpt-68` by $t$ and write

:::{math}
:label: eq-tdpt-72
\dod{w}{\Omega} \Delta\Omega = \sum_{\kvec \in cone} {2\pi\over\hbar^2} \, \Delta_t(\omega)\, |\matrixelement{\kvec}{U(\xvec)}{\kvec_i}|^2,
:::

where $dw/d\Omega$ is the transition rate per unit solid angle, a quantity that is generally a function of direction, in this case, the direction ${\hat{\mathbf{n}}}_f$.

Notice that the factors of $t$ have canceled in {eq}`eq-tdpt-72`, but the right-hand side still depends on $t$ through $\Delta_t(\omega)$. If, however, $t$ is large enough that $\Delta_t(\omega)$ can be replaced by $\delta(\omega)$, then the right hand side does become independent of $t$, and the transition rate is meaningful. We see that at short times we do not have a transition rate, but that at longer times we do.

For now let us assume that $t$ is large enough that $\Delta_t(\omega)$ can be replaced by $\delta(\omega)$, since this gives the simplest answer. This condition will be examined quantitatively in \secrtdpt-15. Then using {eq}`eq-tdpt-67`, we can transform $\delta(\omega)$ by the rules for $\delta$-functions,

:::{math}
:label: eq-tdpt-73
\delta(\omega) = {\delta(k-k_i)\over |d\omega/dk|}= {m\over \hbar k} \, \delta(k-k_i),
:::

where we use {eq}`eq-tdpt-69`.

We must also take the limit $V\to\infty$ to obtain physical results. In this limit, the initial wave function $\psi_\kvec(\xvec)$ loses meaning (it goes to zero everywhere, since it is normalized to unity over the volume of the box), as does the differential transition rate $dw/d\Omega$. However, the differential cross $d\sigma/d\Omega$, which is the differential transition rate normalized by the incident flux, is well defined in the limit. The incident flux is

:::{math}
:label: eq-tdpt-74
J_inc = n_iv_i = {1\over V} {\hbar k_i\over m},
:::

where $n_i=1/V$ is the number of particles per unit volume in the incident state, and $v_i=\hbar k_i/m$ is the incident velocity. Thus

:::{math}
:label: eq-tdpt-75
\dod{\sigma}{\Omega} = {Vm \over \hbar k_i} \dod{w}{\Omega}.
:::

Also, in the limit $V\to\infty$, the sum over lattice points $\kvec$ in {eq}`eq-tdpt-72` can be replaced by an integral,

:::{math}
:label: eq-tdpt-76
\sum_{\kvec \in cone} \to {V \over (2\pi)^3} \int_cone d^3\kvec ={V \over (2\pi)^3} \Delta\Omega \int_0^\infty k^2 \, dk,
:::

where $V/(2\pi)^3$ is the density of states per unit volume in $\kvec$-space and where we have switched to spherical coordinates in $\kvec$-space and done the angular integral over the narrow cone.

Finally we evaluate the matrix element in {eq}`eq-tdpt-72`. It is

:::{math}
:label: eq-tdpt-77
\matrixelement{\kvec}{U(\xvec)}{\kvec_i} = \int d^3\xvec \, \psi_\kvec^\cc(\xvec) U(\xvec) \psi_{\kvec_i}(\xvec) = {1\over V} \int d^3\xvec \, e^{-i(\kvec-\kvec_i)\cdot\xvec} \, U(\xvec) = {(2\pi)^{3/2} \over V} {\tilde U}(\kvec-\kvec_i),
:::

where we use {eq}`eq-tdpt-63` and define the Fourier transform ${\tilde U}(\qvec)$ of the potential $U(\xvec)$ by

:::{math}
:label: eq-tdpt-78
\tilde U(\qvec) = \int {d^3\xvec \over (2\pi)^{3/2}} \, e^{-i\qvec\cdot\xvec} \, U(\xvec).
:::

Putting all the pieces together, we have

:::{math}
\begin{aligned}
\dod{\sigma}{\Omega} &= {Vm \over \hbar k_i} {1\over \Delta \Omega}{V \over (2\pi)^3} \Delta\Omega \int_0^\infty k^2 \, dk \, {2\pi\over \hbar^2} {m \over \hbar k_i} \delta(k-k_i) {(2\pi)^3 \over V^2} |{\tilde U}(\kvec-\kvec_i)|^2
\end{aligned}
:::

:::{math}
:label: eq-tdpt-79
\begin{aligned}
&= {2\pi\over \hbar^2} \Bigl({m \over \hbar k_i}\Bigr)^2 \int_0^\infty k^2 \, dk \, \delta(k-k_i) |{\tilde U}(\kvec-\kvec_i)|^2,
\end{aligned}
:::

where the factors of $V$ and $\Delta\Omega$ have canceled, as they must. Notice that $\kvec$ under the integral is a vector, but only its magnitude $k$ is a variable of integration. The direction of $\kvec$ is that of the small cone, that is, $\kvec= k {\hat{\mathbf{n}}}_f$. Now the $\delta$-function makes the integral easy to do. In particular, $\kvec=k {\hat{\mathbf{n}}}_f$ becomes $k_i {\hat{\mathbf{n}}}_f = k_f {\hat{\mathbf{n}}}_f = \kvec_f$. Notice that if $t$ is large enough to make the replacement $\Delta_t(\omega) \to \delta(\omega)$ but not infinite, the function $\delta(k-k_i)$ should be understood as a function of small but nonzero width. Thus after finite time $t$ the transitions are actually taking place to states that lie in a small energy range about the initial energy. This is an important point: in time-dependent perturbation theory, we do not attempt to enforce energy conservation artificially, rather our job is to solve the Schr\"odinger equation, and when we do we find that energy conservation emerges in the limit $t\to\infty$.

The final answer is now easy. It is

:::{math}
:label: eq-tdpt-80
\dod{\sigma}{\Omega} = 2\pi {m^2\over\hbar^4} | \tilde U(\kvec_f - \kvec_i)|^2.
:::

Notice that the momentum transfer in the scattering process is

:::{math}
:label: eq-tdpt-81
\pvec_f - \pvec_i = \hbar(\kvec_f - \kvec_i),
:::

and the differential cross is a function of this momentum transfer. This result from first-order time-dependent perturbation theory is the same as that obtained in the first Born approximation, which we take up in {ref}`ch-lippschw`.

The result {eq}`eq-tdpt-80` is valid in the high-energy limit, in which the exact wave function in the midst of the potential does not differ much from the unperturbed wave function. This condition will be examined quantitatively in {ref}`sec-lippschw-7`. This makes crude sense: since the Hamiltonian is $H_0+H_1=p^2/2m+U(\xvec)$, if the kinetic energy of the incident particles is large then in a sense we have $H_0\gg H_1$, and an expansion of the transition amplitude in powers of $H_1$ should be valid. But high energy particles blast through the potential without being deflected very much. At low energies a naive power series expansion in powers of $H_1$ will not work, and other techniques are needed. Some of these are explored in {ref}`ch-introscatt`{} and \lippschw.

(sec-tdpt-15)=

## Short-Time Behavior

Let us now estimate the time after which the replacement $\Delta_t(\omega) \to \delta(\omega)$ becomes valid. Let us call this time $t_1$, which we shall estimate as an order of magnitude.

The function $\Delta_t(\omega)$ has a width in $\omega$ given by $\Delta \omega = 1/t$, as an order of magnitude, or, in energy units, $\Delta E = \hbar/t$. We can convert this to wavenumber units by using

:::{math}
:label: eq-tdpt-82
\Delta k = {\Delta\omega\over (d\omega/dk)}={1\over vt},
:::

where we use {eq}`eq-tdpt-69`. This is the width in the variable $k$ of the function we are writing as $\delta(k-k_i)$ under the integral in {eq}`eq-tdpt-79`. The replacement of this function by an exact delta function is valid if this $\Delta k$ is much less than the scale of variation of the function ${\tilde U}(k{\hat{\mathbf{n}}}_f - \kvec_i)$ with respect to $k$, that is, the increment in $k$ over which $\tilde U$ undergoes a significant change.

To estimate this, let us suppose that the potential $U(\xvec)$ has a range (in real space) of $a$, that is, it falls to zero rapidly outside this radius. Thus in the Fourier transform

:::{math}
:label: eq-tdpt-83
{\tilde U}(\kvec)=\int{d^3\xvec\over(2\pi)^{3/2}} \, e^{-i\kvec\cdot\xvec}\,U(\xvec)
:::

the integral cuts off for values of $\xvec$ outside the radius $|\xvec|=a$. The integral gives the function ${\tilde U}(\kvec)$ as a linear combination of plane waves $e^{-i\kvec\cdot\xvec}$, regarded as waves in $\kvec$-space, and the contributions of the shortest wavelength $\Delta k_min$ in $\kvec$-space come from the maximum value of $|\xvec|$ that contribute to the integral. Thus

:::{math}
:label: eq-tdpt-84
\Delta k_min = {1\over a},
:::

and the condition under which $\Delta_t(\omega)$ can be replaced by $\delta(\omega)$ is $\Delta k \ll \Delta k_min$. This is

:::{math}
:label: eq-tdpt-85
{1\over vt} \ll {1\over a},
:::

or,

:::{math}
:label: eq-tdpt-86
t \gg t_1 = {a \over v}.
:::

We see that $t_1$ is of the order of the time it takes a beam particle to traverse the range of the potential, that is, it is approximately the time over which the scattering takes place.

It is also the time required for the “unphysical” particles in the initial state, the ones that find themselves in the midst of the potential at $t=0$ with the wrong energy and momentum, to get scattered out of the potential and to be replaced by new particles that come in from the incident beam. As these particles are scattered also, there develops a “front” of scattered particles, moving away from the scatterer, while a steady state develops behind the front. As time goes on, the unphysical particles become proportionally unimportant in the accounting of the transition rate. Thus the transients at times $t < t_1$ in the solution of the Schr\"odinger equation are related to the artificiality of the initial conditions.

This line of physical reasoning is essentially classical, but it suggests that at a fixed distance from the scatterer, the exact time-dependent solution of the Schr\"odinger equation, the wave function $\psi_S(\xvec,t) = \matrixelement{\xvec}{U(t)}{\kvec_i}$ in the Schr\"odinger picture, actually approaches a quantum stationary state, that is, an energy eigenfunction of the full Hamiltonian $H_0+H_1$, in the limit $t\to\infty$. This eigenfunction has the time dependence $e^{-iE_it/\hbar}$, that is, it has the same energy as the free particle state $\ket{\kvec_i}$. One must simply wait for the front and any dispersive tail trailing behind it to pass, and then one has a steady stream of outgoing particles. To be careful about this argument, one must worry about bound states of the potential, which correspond to the unphysical particles in the classical picture whose energy is too low to escape from the potential well.

(sec-tdpt-16)=

## Two-Body Central Force Scattering

A variation on the analysis of \secrtdpt-14 is two-body scattering from a central force potential. The two-body Hamiltonian is

:::{math}
:label: eq-tdpt-87
H={\pvec_1^2\over 2m_1} + {\pvec_2^2\over 2m_2} + U(|\xvec_2-\xvec_1|) = {\Pvec^2 \over 2M} + {\pvec^2\over 2\mu} + U(r) = H_CM + H_rel,
:::

where we have transformed the lab coordinates and momenta to center-of-mass and relative coordinates and momenta, as in {ref}`ch-cenforce`. Here $M=m_1+m_2$ is the total mass and $\mu$, given by {eq}`eq-tdpt-59` or {eq}`eq-cenforce-58`, is the reduced mass. Also, the center-of-mass and relative Hamiltonians are

:::{math}
:label: eq-tdpt-88
H_CM = {\Pvec^2 \over 2M}, \qquad H_rel = {\pvec^2 \over 2\mu} + U(r).
:::

To compute the cross it is easiest to work with $H_rel$ and to ignore $H_CM$. Then we have an effective one-body problem that can be analyzed by the same method as in \secrtdpt-14, with $\xvec$ replaced by $\rvec$ and $m$ replaced by $\mu$. Also, $\pvec$ is now interpreted as the momentum conjugate to $\rvec$, which was discussed in \secrtdpt-13.

We take $H_0=\pvec^2/2\mu$ and $H_1=U(r)$. The unperturbed eigenstates are plane waves $\ket{\kvec}$ of momentum $\pvec=\hbar\kvec$, as in \secrtdpt-14, normalized to a box of volume $V$,

:::{math}
:label: eq-tdpt-89
\psi_\kvec(\rvec) = \braket{\rvec}{\kvec} = {e^{i\kvec\cdot\rvec} \over \sqrt{V}},
:::

exactly as in {eq}`eq-tdpt-63`. Physically, $\kvec$ can be interpreted as $\kvec_2 = -\kvec_1$ when the lab frame is identified with the center-of-mass frame, as discussed in \secrtdpt-13.

We compute the probability of making a transition $\ket{\kvec_i} \to \ket{\kvec}$, and then sum over all $\kvec$ lying in a small cone centered on some $\kvec_f$, as in \secrtdpt-14. The physical situation can be visualized as in {ref}`fig-tdpt-6`, which shows the initial and final wave vectors of both particles as seen in the center-of-mass frame.

:::{figure} images/tdpt-fig06.png
:label: fig-tdpt-6
:width: 80%

Two-body scattering as seen in the center-of-mass frame. Particle 2 comes in from the left, particle 1 from the right. The initial and final wave vectors of the two particles as seen in the center of mass frame are shown and expressed in terms of the initial and final wave vectors $\kvec_i$ and $\kvec_f$ of the center-of-mass motion.
:::

Finally, to compute the differential cross we divide the differential transition rate by the incident flux, defined as $J=nv$ as in \secrtdpt-13, where $n=1/V$ (one incident particle in the box of volume $V$, where particle 2 can be thought of as the incident particle), and where $v=p/\mu$ is the relative velocity. Alternatively, we can think of two particles in a box of volume $V$, so that $n_1=n_2=1/V$, whereupon the integral in {eq}`eq-tdpt-57`, taken over the box, gives $(1/V^2)V = 1/V$. The conversion from transition rate to cross is the same in either case. The final differential cross is given by {eq}`eq-tdpt-80`, with $m$ replaced by $\mu$. As {ref}`fig-tdpt-6` makes clear, the cross is measured in the center-of-mass frame.

All of this assumes that the two particles are distinguishable. If they are identical, then it is necessary to use properly symmetrized or antisymmetrized wave functions (including the spin), as discussed in {ref}`ch-identpart`. See Prob.~\prbrtdpt-1. In this case one finds interference terms in the cross between the direct and exchanged matrix elements.

Another point of view is to include the center-of-mass dynamics in the description of the scattering process, that is, to use the entire Hamiltonian {eq}`eq-tdpt-87`, including $H_CM$. In this case we take

:::{math}
:label: eq-tdpt-90
H_0 = {\Pvec^2\over 2M} + {\pvec^2\over 2\mu}, \qquad H_1 = U(r).
:::

The unperturbed eigenstates can be taken to be $\ket{\Kvec\kvec}$, with wave function

:::{math}
:label: eq-tdpt-91
\Psi_{\Kvec\kvec}(\Rvec,\rvec) = \braket{\Rvec\rvec}{\Kvec\kvec} = {e^{i(\Kvec\cdot\Rvec + \kvec\cdot\rvec)} \over V},
:::

which are assumed to have periodic boundary conditions in a box of volume $V$ in both the coordinates $\Rvec$ and $\rvec$. The normalization is such that

:::{math}
:label: eq-tdpt-92
\int d^3\Rvec \, d^3\rvec |\Psi_{\Kvec\kvec}(\Rvec,\rvec)|^2 =1,
:::

where both the $\Rvec$ and $\rvec$ integrations are taken over the volume $V$, and the orthonormality relations are

:::{math}
:label: eq-tdpt-93
\braket{\Kvec\kvec}{\Kvec'\kvec'} = \delta_{\Kvec\Kvec'} \, \delta_{\kvec\kvec'}.
:::

The unperturbed energies are

:::{math}
:label: eq-tdpt-94
E_{\Kvec\kvec} = {\hbar^2\Kvec^2\over 2M} + {\hbar^2\kvec^2\over 2\mu}.
:::

The box is a mathematical crutch that allows us to deal with a discrete spectrum, and exactly how we set it up and the boundary conditions we impose are not important as long as $V\to\infty$ gives physical results. In the present case, both $\Kvec$ and $\kvec$ are quantized to lie on a lattice, as in {eq}`eq-tdpt-65`. As $V\to\infty$, both $\Kvec$ and $\kvec$ take on continuous values.

Now let $\ket{\Kvec_i,\kvec_i}$ be an initial state, and $\ket{\Kvec\kvec}$ some final state. Given that $\Pvec$ commutes with the entire Hamiltonian $H=H_0+H_1$, there cannot be any transitions that change the value of $\Kvec$, so we must have $c_{\Kvec\kvec}(t)=0$ if $\Kvec\ne\Kvec_i$. This is true under the exact time evolution engendered by $H$, and is not a conclusion of perturbation theory. However, we see the same thing in first order perturbation theory if we compute the matrix element of the perturbing Hamiltonian between the initial and final states,

:::{math}
:label: eq-tdpt-95
\matrixelement{\Kvec\kvec}{U(r)}{\Kvec_i\kvec_i} = {1\over V^2} \int d^3\Rvec \, d^3\rvec \, e^{-i(\Kvec-\Kvec_i)\cdot\Rvec} \, e^{-i(\kvec-\kvec_i)\cdot\rvec} \, U(r) = \delta_{\Kvec,\Kvec_i} \, {(2\pi)^{3/2} \over V}\, \tilde U(\kvec-\kvec_i),
:::

where the $\rvec$-integration is the same as in {eq}`eq-tdpt-77`. Except for the Kronecker delta in the total momentum, it is the same result obtained previously.

The Einstein frequency appearing in the expression for $c_{\Kvec\kvec}^{(1)}(t)$ is

:::{math}
:label: eq-tdpt-96
\omega = \hbar\Bigl({\Kvec^2\over 2M} + {\kvec^2\over 2\mu} - {\Kvec_i^2\over 2M} -{\kvec_i^2\over 2\mu}\Bigr),
:::

but, in view of the Kronecker delta in {eq}`eq-tdpt-95`, the result is simply

:::{math}
:label: eq-tdpt-97
\omega={\hbar\over 2\mu}(\kvec^2 - \kvec_i^2),
:::

for states for which $c_{\Kvec\kvec}^{(1)}$ does not vanish. This is just {eq}`eq-tdpt-67` all over again, with $m$ replaced by $\mu$. The energy of the center-of-mass motion does not change in the scattering process.

Now squaring $c^{(1)}_{\Kvec\kvec}(t)$ we get a probability of the transition $\ket{\Kvec_i\kvec_i} \to \ket{\Kvec\kvec}$ in first-order, time-dependent perturbation theory, which we must sum over some collection of final states to get a physically meaningful result. Notice that the square of the Kronecker delta $\delta_{\Kvec,\Kvec_i}$ is just the same as the original Kronecker delta.

It is best to carry out the sum as follows. Let ${\cal R}$ be a region of $\Kvec$-space, which may or may not contain the initial momentum $\Kvec_i$. Then we sum over all final $\kvec$ in a cone as in Figs.~{ref}`fig-tdpt-5` or {ref}`fig-tdpt-6`, and over all $\Kvec$ values in ${\cal R}$. Dividing the probability by the time $t$, we interpret the result as the transition rate,

:::{math}
:label: eq-tdpt-98
\int_{\cal R} d^3\Kvec \, \Delta\Omega \, {d^5 w \over d\Kvec^3\,d\Omega}.
:::

Here the 5 on $d^5w$ indicates that $d^3\Kvec$ is 3-dimensional and $d\Omega$ is 2-dimensional. (By the same logic we should write $d^2 w/d\Omega$ for the usual differential transition rate instead of $dw/d\Omega$, as we have been doing.) This integral can also be interpreted as

:::{math}
:label: eq-tdpt-99
\int_{\cal R} d^3\Kvec \int_cone d\Omega \, {d^5 w \over d\Kvec^3\,d\Omega},
:::

since the cone is small.

When we carry out the same sum on the probabilities, the Kronecker delta $\delta_{\Kvec,\Kvec_i}$ guarantees that the sum vanishes unless $\Kvec_i$ lies in the region ${\cal R}$. Finally, dividing by the incident flux $v/V$, we can take the limit $V\to\infty$ and the result is

:::{math}
:label: eq-tdpt-100
\begin{aligned}
\int_{\cal R} d^3\Kvec \, {d^5 \sigma \over d\Kvec^3\,d\Omega} = \begin{cases}\ds 2\pi {\ds \mu^2\over\ds \hbar^4} |{\tilde U}(\kvec-\kvec_i)|^2, & if \Kvec_i \in {\cal R} \\  0, & otherwise.\\\end{cases}
\end{aligned}

:::

This may be reinterpreted by writing

:::{math}
:label: eq-tdpt-101
{d^5 \sigma \over d\Kvec^3\,d\Omega} = 2\pi {\mu^2\over\hbar^4} |{\tilde U}(\kvec-\kvec_i)|^2 \, \delta^3(\Kvec-\Kvec_i),
:::

where the Dirac delta-function shows conservation of the center-of-mass momentum. Integrating this over all $\Kvec$, we obtain

:::{math}
:label: eq-tdpt-102
\int d^3\Kvec \, {d^5 \sigma \over d\Kvec^3\,d\Omega} = {d^2 \sigma\over d\Omega} = 2\pi {\mu^2\over\hbar^4} |{\tilde U}(\kvec-\kvec_i)|^2,
:::

which reproduces our earlier results.

(sec-tdpt-17)=

## Application: Electrostatic Scattering and Form Factors

Let us consider the scattering of a charged particle by an electrostatic potential created by a charge distribution $\rho(\xvec)$. The charge distribution need not be a point charge; for example, it could be the extended charge distribution inside a proton or a neutron (even though the neutron is neutral, it does contain a nontrivial charge distribution), or it could be the distribution created by the nucleus and the electron cloud of an atom. We denote the charge of the beam particle by $Q_b$.

The charge density and electrostatic potential $\Phi(\xvec)$ are related by the Poisson equation,

:::{math}
:label: eq-tdpt-103
\del^2\Phi(\xvec) = -4\pi\rho(\xvec),
:::

and the potential appearing in the Schr\"odinger equation is $U(\xvec)=Q_b\Phi(\xvec)$. The differential cross {eq}`eq-tdpt-80` requires the Fourier transform $\tilde U(\qvec)$ of $U(\xvec)$, a useful expression for which can be obtained by Fourier transforming the Poisson equation. Denoting the variable upon which the Fourier transform depends by $\qvec$, as in {eq}`eq-tdpt-78`, and noting that the operator $-\del^2$ in $\xvec$-space becomes multiplication by $q^2=|\qvec|^2$ in $\qvec$-space, we find

:::{math}
:label: eq-tdpt-104
\tilde\Phi(\qvec) = {4\pi\over q^2} \,\tilde\rho(\qvec),
:::

where we use a tilde for the Fourier transforms of various quantities.

For use in the cross {eq}`eq-tdpt-80` we identify $\qvec$ with the quantity

:::{math}
:label: eq-tdpt-105
\qvec=\kvec-\kvec_i,
:::

where now we write simply $\kvec$ instead of $\kvec_f$ for the final wave vector. Thus, the momentum transfer is

:::{math}
:label: eq-tdpt-106
\hbar\qvec = \pvec-\pvec_i.
:::

Then the cross {eq}`eq-tdpt-80` can be written

:::{math}
:label: eq-tdpt-107
{d\sigma\over d\Omega} = {4m^2Q_b^2\over \hbar^4q^4}\, |f(\qvec)|^2,
:::

where

:::{math}
:label: eq-tdpt-108
f(\qvec)= (2\pi)^{3/2} \tilde\rho(\qvec) =\int d^3\xvec \, e^{-i\qvec\cdot\xvec}\, \rho(\xvec).
:::

The quantity $f(\qvec)$ is called the *form factor* of the charge distribution; it is just the Fourier transform of $\rho(\xvec)$, with a certain normalization.

We can transform the denominator in {eq}`eq-tdpt-107`. Squaring {eq}`eq-tdpt-106`, we have

:::{math}
:label: eq-tdpt-109
\hbar^2 q^2 = \pvec^2 -2\pvec\cdot\pvec_i+\pvec_i^2 = 2p^2(1-\cos\theta) = 4p^2\sin^2(\theta/2)= 8mE \sin^2(\theta/2),
:::

where $\theta$ is the angle between the initial momentum $\pvec_i$ and the final one $\pvec$, that is, it is the scattering angle; where we use $\pvec^2=\pvec_i^2$, which is energy conservation; and where we use $p^2=2mE$, where $E$ is the kinetic energy of the beam particle. Then the cross {eq}`eq-tdpt-107` becomes

:::{math}
:label: eq-tdpt-110
\dod{\sigma}{\Omega} = {Q_b^2\over 16E^2\sin^4(\theta/2)} \,|f(\qvec)|^2.
:::

(sec-tdpt-18)=

## Coulomb Scattering in the Born Approximation

Let us suppose the target is a point particle of charge $Q_t$, so that

:::{math}
:label: eq-tdpt-111
\rho(\xvec)=Q_t \,\delta(\xvec).
:::

Then

:::{math}
:label: eq-tdpt-112
f(\qvec) = Q_t,
:::

and {eq}`eq-tdpt-107` becomes

:::{math}
:label: eq-tdpt-113
\dod{\sigma}{\Omega} = {Q_b^2Q_t^2 \over 16E^2 \sin^4(\theta/2)},
:::

which we recognize as the Rutherford cross .

It is nice to derive the Rutherford cross by means of time-dependent perturbation theory, but the result is actually a fluke, for when we examine the conditions of validity of the approximations leading to {eq}`eq-tdpt-80` we find that in the case of the Coulomb potential $U(\xvec)=Q_t/r$ they are not met for any value of the initial momentum. See \lippschw.7. This is a somewhat strange situation.

The Rutherford cross is exact for the classical scattering of two nonrelativistic, point charged particles in the electrostatic approximation (this is a standard calculation in classical mechanics). It turns out that it is also the exact cross for the Coulomb scattering of two distinguishable, nonrelativistic particles in the electrostatic approximation in quantum mechanics. This is shown by obtaining the exact solution of the Schr\"odinger equation in the potential $U(\xvec)=Q_t/r$ for positive energies and with the right boundary conditions. That is, the exact cross is obtained from exact solutions of the hydrogen-like Hamiltonian for positive energies. Recall that in {ref}`ch-hydrogen`{} on hydrogen-like atoms we only considered bound state solutions. The exact positive energy solutions are somewhat more technical to deal with than the bound state solutions, but scattering solutions can be obtained by separating the Schr\"odinger equation in confocal parabolic coordinates. The details are given in many books, for example, Schiff.

The details of this calculation are useful in many applications, for example, the calculation of thermonuclear reaction rates inside stars. Although the temperatures inside stars are quite high by ordinary standards the nuclei are still essentially nonrelativistic and ordinary Rutherford scattering applies to their interactions. A nuclear reaction requires that nuclei, which have positive charges and which therefore repel one another, come within the range of the nuclear forces. If the nuclei were governed strictly by classical mechanics they would never do this, since at the temperatures prevalent they do not have enough kinetic energy to overcome the repulsive Coulomb barrier. But a quantum treatment shows that there is some amplitude to tunnel through the barrier and bring the nuclei into contact, where the nuclear reactions can take place. Tunneling amplitudes have a strong dependence on energy (see Prob.~\wkb.3 for a one-dimensional example), which implies that thermonuclear reaction rates in stars are a strong function of temperature. The details are obtained from the exact scattering solution in the Coulomb potential.

When we use the Coulomb charge density {eq}`eq-tdpt-111` in the cross {eq}`eq-tdpt-110` we are effectively applying time-dependent perturbation theory to scattering in a hydrogen-like system, but we are only carrying the perturbation expansion out to lowest order in powers of the potential. Why then do we get the exact answer? Does it mean that all the higher order terms vanish?

The answer is more complicated than it seems, and must be understood in terms of the *scattering amplitude*, which is introduced in {ref}`ch-introscatt`. The cross is the square of the scattering amplitude, which is a complex quantity. It turns out that in the first Born approximation, equivalent to first-order time-dependent perturbation theory, the phase of the scattering amplitude for Coulomb scattering is completely wrong but by a kind of accident its absolute value is exactly right. Thus when we square the amplitude to get the cross , the phase cancels and we get the exact answer.

In the Coulomb scattering of identical particles, however, there are cross-terms between the direct and exchange amplitudes, needed to satisfy the symmetrization postulate, and these do depend on the phase of the scattering amplitude. Thus, the first Born approximation for the Coulomb scattering of identical particles does not give the right answer, since the cross terms are all wrong. See Prob.~\prbrtdpt-1.

(sec-tdpt-19)=

## Other Types of Electrostatic Scattering

All this does not mean that our result {eq}`eq-tdpt-107` or {eq}`eq-tdpt-110` is useless, however. The problem with the Coulomb potential, from the standpoint of time-dependent perturbation theory or the Born approximation, is that it has effectively an infinite range. The long-range nature of this potential shows up in the Rutherford cross by the fact that the cross diverges rather badly at $\theta=0$, that is, it goes as $\theta^{-4}$. In the Coulomb potential there is a large probability of small-angle scattering, which obviously comes (speaking classically) from particles with a large impact parameter. Since the potential is long-range, these particles feel the Coulomb force and undergo some scattering.

On the other hand, we see from {eq}`eq-tdpt-107` that the form factor squared is a kind of fudge factor that converts the Rutherford cross into the actual cross for a distributed charge distribution $\rho(\xvec)$. If the form factor should vanish at $\qvec=0$, that is, if its Taylor series should start with a term proportional to $\qvec$, then $|f(\qvec)|^2$ will cancel two of the powers of $q$ seen in the denominator in {eq}`eq-tdpt-107`, so the cross will only diverge as $\theta^{-2}$ at small angles, instead of $\theta^{-4}$. It turns out that the condition $f(0)=0$ is equivalent to the vanishing of the total charge in $\rho(\xvec)$ (see Prob.~\prbrtdpt-3), which means that the charge distribution does not have a monopole moment. Then the potential does not have a Coulomb tail at large distances, rather it falls off as $1/r^2$ or faster, and much of the small-angle scattering present in the Rutherford cross is eliminated.

If in addition the target charge distribution has no electric dipole moment, then it turns out that $f(\qvec)$ is quadratic in $\qvec$ for small values of $\qvec$, so that the $q^4$ denominator in the Rutherford cross is completely eliminated and the cross {eq}`eq-tdpt-107` is nonsingular at $\theta=0$. In cases like this the conditions of validity of cross {eq}`eq-tdpt-107` are met for some initial momenta (basically, for high enough initial energy).

Consider, for example, the elastic scattering of electrons by a hydrogen atom. We model the atom as charge distribution described by a point nucleus and an electron cloud with charge density

:::{math}
:label: eq-tdpt-114
\rho(\xvec)= -|\psi_{100}(r)|^2 = -{e^{-2r}\over \pi},
:::

where we use {eq}`eq-hydrogen-29a` and where we work in atomic units ($m=e=\hbar=1$). Adding the charge density $\delta(\xvec)$ of the nucleus to this and computing the Fourier transform, we obtain the form factor as

:::{math}
:label: eq-tdpt-115
f(\qvec) = 1-{16\over (q^2+4)^2}.
:::

When this is used in {eq}`eq-tdpt-107` we obtain a cross for electron-hydrogen scattering that is useful at moderately high electron energies (by atomic standards, that is, $E>1$ or $E\gg1$ in atomic units).

The scattering of charged particles by atoms is important in calculating $dE/dx$, the rate at which a charged particle loses energy per unit distance when passing through matter. This is an important problem in many areas such as experimental high energy physics. In practice the calculations often must be relativistic and must take into account both elastic and inelastic scattering. At sufficiently high energies, the energy loss for electrons and muons is dominated by bremsstrahlung, the emission of photons as the electron or muon is accelerated in the field of the atomic nucleus.

Experimental probes of the internal structure of the proton and neutron by electron scattering played an important role in showing that these particles are made up of three constituent point particles, now known as quarks. These experiments were carried out during the 1960's at the Stanford Linear Accelerator, and many similar experiments, using a variety of incident particles and a variety of targets, have been performed since, accumulating a body of experimental evidence that has guided and confirmed the theory of quantum chromodynamics, the theory of the strong interactions. In these experiments the beam particles are relativistic, so that magnetic effects are important in addition to electric effects. As a result the relativistic treatment of the scattering requires more than one form factor, but the basic ideas are the same as in the nonrelativistic electrostatic model considered here.

(sec-tdpt-20)=

## Example:  The Yukawa Potential

Simple models of nuclear interactions between nucleons such as the proton and neutron often make use of the *Yukawa potential*,

:::{math}
:label: eq-tdpt-116
U(r) = A {e^{-\kappa r} \over r},
:::

where $A$ and $\kappa$ are constants. The Yukawa potential is obviously a kind of modified Coulomb potential, with the extra factor $e^{-\kappa r}$ that cuts off the potential at a distance of the order of $1/\kappa$ and gives it a finite range. In Yukawa's day it was known that the nuclear forces have a finite range on the order of $10^{-13}\,cm$, and he was thinking of a generalization of electromagnetic forces that would incorporate this fact.

To use the Yukawa potential in {eq}`eq-tdpt-80` it is necessary to know its Fourier transform. The Fourier integral can be carried out directly by means of contour integration, but the following approach is easier. First we note that

:::{math}
:label: eq-tdpt-117
(\del^2-\kappa^2)\Bigl({e^{-\kappa r}\over r}\Bigr)= -4\pi\,\delta(\xvec),
:::

an obvious generalization of the Poisson equation for a point charge in electrostatics, which can be derived by directly applying {eq}`eq-vecident-23` and using $\del^2(1/r)=-4\pi\,\delta(\xvec)$. {eq}`eq-tdpt-117` shows that the Yukawa potential is the Green's function of static solutions of the Klein-Gordon equation,

:::{math}
:label: eq-tdpt-118
{1\over c^2}{\partial^2 \psi\over\partial t^2} - \del^2\psi =-\kappa^2\psi,
:::

which is the simplest relativistic wave equation for a particle of mass $M$, where

:::{math}
:label: eq-tdpt-119
\kappa=M/\hbar c.
:::

See {ref}`ch-kleing`{} for more details. Note that $\kappa=1/\lambda_C$ where $\lambda_C =\hbar c/M$ is the Compton wave length of the particle of mass $M$ appearing in the Klein-Gordon equation. See \finestruc.5 for an explanation of the physical meaning of the Compton wavelength.

In Yukawa's application the numbers come out about right if the particle is identified with the $\pi$-meson, whose mass is $140\,MeV$. This corresponds to a Compton wave length of

:::{math}
:label: eq-tdpt-120
\lambda_C=1.4\times 10^{-13}\,cm,
:::

close to the known range of the nuclear forces. (In Yukawa's day, however, there was some confusion between the $\pi$-meson and what is now called the muon, as the muon was detected first and has a similar mass.) Yukawa's idea was that the meson whose mass $M$ appears in his potential through $\kappa=m/\hbar c$ was the boson that carries the strong interactions, in the same way as the photon carries the electromagnetic interactions. Note that the Klein-Gordon equation goes over to the usual wave equation as $M\to0$; the latter of course comes out of Maxwell's equations. In the same limit, the Yukawa potential becomes the Coulomb potential.

Now multiplying {eq}`eq-tdpt-117` by $A$ and Fourier transforming, we obtain

:::{math}
:label: eq-tdpt-121
{\tilde U}(\qvec) = {4\pi A \over (2\pi)^{3/2}} {1 \over \kappa^2 + q^2},
:::

using our normalization conventions for the Fourier transform and $\qvec$ as the variable conjugate to $\xvec$. From this and {eq}`eq-tdpt-122` we obtain the cross for scattering from a Yukawa potential,

:::{math}
:label: eq-tdpt-122
\dod{\sigma}{\Omega} = {4A^2 m^2\over \hbar^4(q^2+\kappa^2)^2}= {4A^2 m^2 \over \hbar^4} {1 \over (4k^2 \sin^2 \theta/2 + \kappa^2)^2}.
:::

This result depends on several parameters ($A$, $m$, $\kappa$ and $k$), and it is valid only for certain ranges of them. The details can be worked out by the method of \lippschw.7.

If we set $A=Q_bQ_t$ and take the limit $M\to0$, the Yukawa cross {eq}`eq-tdpt-122` goes over to the Rutherford cross . As discussed in \secrtdpt-18, however, this cannot be regarded as a valid derivation of the Rutherford cross .

(sec-tdpt-21)=

## Other Applications

Here are some other applications of time-dependent perturbation theory that we will consider later in the course. As an example of an atom interacting with a classical light wave, we shall study the photoelectric effect in {ref}`ch-photelec`. In the photoelectric effect, a high energy photon, described by a classical light wave, ejects an electron from an atom, leaving behind a positive ion. Later we will consider the emission and absorption of radiation by an atom using the quantized theory of the electromagnetic field, that is, we will study the emission and absorption of photons. A similar example, one that requires second-order time-dependent perturbation theory, is the scattering of photons by matter. Later still we will consider a variety of relativistic processes that are applications of time-dependent perturbation theory, including relativistic scattering of charged particles and the creation and annihilation of electron-positron pairs.

\problems

(prob-tdpt-1)=

**Problem \prbdtdpt-1..** 

\problempart{(a)} In classical mechanics we can always distinguish particles by placing little spots of paint on them. Suppose we have two particles in classical mechanics that are identical apart from insignificant spots of blue and green paint. (The spots have no effect on the scattering.) Suppose the differential cross in the center-of-mass system for the detection of blue particles is $(d\sigma/d\Omega)(\theta,\phi)$. What is the differential cross $(d\sigma/d\Omega)_dc(\theta,\phi)$ for the detection of particles when we don't care about the color?

\problempart{(b)} Consider the scattering of two identical particles of spin $s$ in quantum mechanics. Work in the center-of-mass system, and let $\mu=m/2$ be the reduced mass. Consider in particular three cases: $s=0$, $s=\frac{1}{2}$, and $s=1$. Organize the eigenstates of $H_0=p^2/2\mu$ as tensor products of spatial states times spin states; make the spin states eigenstates of $S^2$ and $S_z$, where $\Svec=\Svec_1+\Svec_2$, and make the spatial states properly symmetrized or antisymmetrized plane waves. Let the initial spin state be $\ket{S_i M_{Si}}$ and the final one be $\ket{S_f M_{Sf}}$. Since potential scattering cannot flip the spin, the cross will be proportional to $\delta(S_i,S_f) \delta(M_{Si},M_{Sf})$. Find the differential cross in terms of

:::{math}
:label: eq-tdpt-123
\tilde U_+ = \tilde U(\kvec_f+\kvec_i), \qquad \tilde U_- = \tilde U(\kvec_f-\kvec_i),
:::

where $\tilde U$ is defined as in {eq}`eq-tdpt-78`. Use the fact that $U(\xvec)=U(-\xvec)$ to simplify the result as much as possible. Use notation like that in {eq}`eq-tdpt-80`.

\problempart{(c)} For the three cases $s=0$, $s=\frac{1}{2}$, $s=1$, assume that the initial state is unpolarized and that we do not care about the final spin state. Find the differential cross in terms of the quantities $a=|\tilde U_+|^2$, $b=|\tilde U_-|^2$, and $c=\Re (\tilde U^\cc_+ \tilde U_-)$.

\problempart{(d)} Work out the answer for the case of Coulomb scattering of two electrons, and compare to the classical Rutherford formula, {eq}`eq-tdpt-113`. Express your answer in a notation similar to that of {eq}`eq-tdpt-113`. The cross term you get in applying the results of part (c) to Coulomb scattering is actually incorrect; the trouble is that plane waves do not adequately represent the unbound Coulomb wave functions, which have long range, logarithmic phase shifts. The correct answer is called the Mott cross , which we will discuss later in class.

Although the result obtained in this problem for Coulomb scattering is not correct, the calculation does show that in the case of identical particles the cross involves interference terms between direct and exchange amplitudes. Also, there are other problems, for example, the scattering of two neutrons or two identical atoms, for which the technique gives answers that are correct in the appropriate range of parameters.

(prob-tdpt-2)=

**Problem \prbdtdpt-2..** 

If we take into account relativistic corrections, however, then there is a small probability for flipping the spin.

Consider the scattering of an electron by a central force potential $U(r)$. Suppose the electron spin of the incident beam is polarized in the $+{\hat{\mathbf{z}}}$ direction. Including the spin-orbit interaction {eq}`eq-finestruc-13`, find the differential cross for electrons polarized in the $-{\hat{\mathbf{z}}}$ direction after the scattering. Express it as a certain factor times the cross {eq}`eq-tdpt-80`. Notice that $V$ in {eq}`eq-finestruc-13` is called $U$ in these notes.

**Note:** It is common in scattering problems to assume that the incident particles are directed in the $z$-direction. We do not want to do that in this problem, since the $z$-direction is the direction of polarization of the spin of the incident electrons. Call the incident wave vector $\kvec_i$ and the final one $\kvec_f$ or just $\kvec$, as in these notes. These can be in any direction. Also note the identity {eq}`eq-zeeman-23`.

This problem gives an example of *inelastic scattering*, in which the internal state of the particles can change as a result of the scattering, or perhaps new particles created. In this case it is the spin state of the incident particle that can change. Other examples include the scattering of an electron from an atom, in which the state of the atom may change, or scattering in which a photon is emitted, etc. In general, the different processes (elastic and inelastic) are called *channels*. High energy processes tend to have many inelastic channels.

(prob-tdpt-3)=

**Problem \prbdtdpt-3..** 

Let the electrostatic potential of the scatterer be $\Phi(\xvec)$, as in \secrtdpt-17. If we wish the form factor to suppress the small angle scattering, then we should require that $f(\qvec)=0$ at $\qvec=0$. Show that this implies that the total charge in the distribution $\rho(\xvec)$ vanishes. This makes sense: if the total charge vanishes, then at large distances there is no Coulomb tail to $\Phi(\xvec)$.

The form factor can be expanded in powers of $\qvec$ for small $\qvec$,

:::{math}
:label: eq-tdpt-124
f(\qvec)=f(0) + \qvec\cdot\frac{\partial f(\qvec)}{\partial \qvec} + \ldots
:::

Show that if the source distribution has no electric dipole moment, then the first order term (proportional to $\qvec$) vanishes. If the total charge is also zero, then the differential cross {eq}`eq-tdpt-80` does not diverge at $\qvec=0$. In particular, this is true for any rotationally symmetric charge distribution of zero total charge, like that of the hydrogen atom with the form factor {eq}`eq-tdpt-115`.
