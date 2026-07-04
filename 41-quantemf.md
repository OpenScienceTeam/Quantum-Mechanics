---
title: "41. The Quantized Electromagnetic Field"
---
(ch-quantemf)=

# 41. The Quantized Electromagnetic Field

(sec-quantemf-1)=

## Introduction

In these notes we will quantize the electromagnetic field, starting with the classical Hamiltonian description worked out in {ref}`ch-classemf`. We will work primarily with the free field, and leave the interaction with matter for later sets ({ref}`ch-radnmatt`{} and \photscatt). These notes continue with the notation established in {ref}`ch-classemf`.

(sec-quantemf-2)=

## Dirac or Canonical Quantization

To *quantize* a classical system means that we pass from a classical description of the system to the quantum description. The classical description involves a classical Lagrangian or Hamiltonian, and a set of classical coordinates describing the dynamical state, that is, a set of $q$'s and $\dot q$'s or $q$'s and $p$'s. Classical observables are functions of these coordinates. In the quantum description, the $q$'s and $p$'s become reinterpreted as operators that act on a state space or Hilbert space of some kind. Since quantum mechanics has more physics in it than classical mechanics, the process of quantization can never be completely deductive. Instead, the classical mechanics offers at best a guide to guessing the structure of the quantum system. Ultimately the correctness of the quantum system we have obtained must be checked experimentally.

Nevertheless, the procedure that is known to work for mechanical systems is to replace the $q$'s and $p$'s of the classical system by operators that satisfy the canonical commutation relations,

:::{math}
:label: eq-quantemf-1
[q_i,q_j]=0, \qquad [p_i,p_j]=0, \qquad [q_i,p_j]=i\hbar\,\delta_{ij}.
:::

See {eq}`eq-spatialdof-69a`. These are the obvious analogs of the classical canonical Poisson bracket relations, see {eq}`eq-classmech-108`. Then the state space of the quantum system is taken to be the Hilbert space of wave functions $\psi(q_1,\ldots, q_N)$, and the quantum $q$'s and $p$'s have an action on this space given by

:::{math}
:label: eq-quantemf-2
q_i = \text{multiplication by }q_i, \qquad p_i = -i\hbar\pop{}{q_i},
:::

which cause the commutation relations {eq}`eq-quantemf-1` to be satisfied. As we say, we have found a *representation* of the commutation relations {eq}`eq-quantemf-1` by means of specific operators acting on a specific Hilbert space.

This procedure is called *canonical* or *Dirac quantization*. In mechanical systems it only works if the $q$'s and $p$'s are the Cartesian coordinates of the particles of the system. Even then if there are classical observables that contain $q$-$p$ products, then it is ambiguous what the corresponding quantum operator should be, since classically $qp=pq$, but in quantum mechanics $qp=pq+i\hbar$. That is, there is an ordering ambiguity when observables contain products of noncommuting operators.

The reason that Dirac quantization only works in Cartesian coordinates is related to the ordering ambiguity. In classical mechanics, a coordinate transformation of the form $Q_i=Q_i(q,p)$, $P_i=P_i(q,p)$ is said to be a *canonical transformation* if the new (capitalized) $Q$'s and $P$'s satisfy the same Poisson bracket relations as the old (lower case) $q$'s and $p$'s. This also preserves the form of Hamilton's equations of motion. See {ref}`sec-classmech-27`. For example, the transformation that takes us from the Cartesian position $\xvec$ and momentum $\pvec$ of a particle to the spherical coordinates $(r,\theta,\phi)$ and corresponding momenta $(p_r,p_\theta,p_\phi)$ is a canonical transformation. But if we apply the Dirac quantization prescription in spherical coordinates, then we do not get the right answer for operators such as the Hamiltonian. The correct way to get the quantum Hamiltonian in spherical coordinates is first to quantize in Cartesian coordinates, and then to transform to spherical coordinates using the chain rule for the momentum operators. In other words, Dirac quantization does not commute with classical canonical transformations. An exception is the case of linear canonical transformations, where, with the right understandings, quantization does commute with the classical transformation.

In quantum field theory other methods of quantization have been developed that are easier to apply or better in some respects than canonical quantization. One of the problems with canonical quantization is that it is not manifestly covariant. In modern field theory one prefers to work with Lagrangians rather than Hamiltonians, which maintain manifest Lorentz covariance. Quantization takes place by using the Lagrangian in the path integral, which is an expression for the quantum propagator. Another issue is that field theories usually involve gauge fields, which transform in certain ways under gauge transformations. Canonical quantization, however, in its simplest versions, requires one to fix the gauge. That is, the quantization is not manifestly gauge-invariant. In fact, the electromagnetic field is a gauge field, and we have already chosen to work in Coulomb gauge. This destroys not only the manifest Lorentz covariance of the theory, but the manifest gauge invariance. Nevertheless, canonical quantization is not only the simplest procedure for quantizing the electromagnetic field, but also the one that historically was pursued first, and we will use it here.

(sec-quantemf-3)=

## Quantizing the Free Electromagnetic Field

In these notes we will work with the free electromagnetic field only. Thus, the Hamiltonian is just the Hamiltonian for the free field,

:::{math}
:label: eq-quantemf-3
H = {1\over2}\sum_\lambda \omega_k \bigl( P_\lambda^2 + Q_\lambda^2\bigr)
:::

[see {eq}`eq-classemf-75`], where we adopt box normalization as in {ref}`ch-classemf`. To quantize, we reinterpret the variables $Q_\lambda$, $P_\lambda$ as operators satisfying the commutation relations,

:::{math}
:label: eq-quantemf-4
[Q_\lambda,P_{\lambda'}]=i\hbar\,\delta_{\lambda\lambda'}, \qquad [Q_\lambda,Q_{\lambda'}]=[P_\lambda,P_{\lambda'}]=0,
:::

whereupon the Hamiltonian $H$ also becomes an operator.

We see that the free field Hamiltonian is a sum of independent harmonic oscillators, one for each mode of the field, so we introduce the usual Dirac algebraic formalism for harmonic oscillators. See {ref}`ch-harmosc`, and note that Dirac's formalism is based on the $q$-$p$ commutation relations, which are satisfied by the $Q_\lambda$ and $P_\lambda$ in the present application. First we define the annihilation and creation operators,

:::{math}
:label: eq-quantemf-5
\begin{aligned}
a_\lambda &= {Q_\lambda +iP_\lambda \over \sqrt{2\hbar}}, \\
a^\hc_\lambda &= {Q_\lambda -iP_\lambda \over \sqrt{2\hbar}}, \\

\end{aligned}
:::

which are just like the classical formulas {eq}`eq-classemf-101` except for the replacement of $\cc$ by $\hc$. These operators satisfy the commutation relations,

:::{math}
:label: eq-quantemf-6
[a_\lambda, a^\hc_{\lambda'}] = \delta_{\lambda\lambda'}, \qquad [a_\lambda,a_{\lambda'}] = [a^\hc_\lambda, a^\hc_{\lambda'}] =0,
:::

as follows from {eq}`eq-quantemf-4`. Next we write the free field Hamiltonian {eq}`eq-quantemf-3` in terms of the creation and annihilation operators,

:::{math}
:label: eq-quantemf-7
H = \sum_\lambda \hbar\omega_k \Bigl( a^\hc_\lambda a_\lambda + {1\over 2}\Bigr),
:::

where the $1/2$ represents the usual zero point energy of a harmonic oscillator. Here we are following exactly the same procedure we used with mechanical oscillators (see {ref}`ch-harmosc`), but in a moment we will have to reconsider this step. We also define the usual number operator,

:::{math}
:label: eq-quantemf-8
N_\lambda = a^\hc_\lambda a_\lambda.
:::

What are the ket spaces upon which these operators act? It is possible to introduce a Hilbert space of wave functions $\psi(Q_\lambda)$ for each mode of the field, but in practice this is never done because the algebraic relations among the operators and energy eigenkets are all that is ever needed and they are much more convenient to work with than wave functions. We will denote the energy eigenkets of a single oscillator $\lambda$ by $\ket{n_\lambda}$, where $n_\lambda=0,1,\ldots$ is the usual quantum number of a harmonic oscillator. These kets span a space $\ES_\lambda$ associated with the single mode, which is the space upon which the operators $Q_\lambda$, $P_\lambda$ (for the given value of $\lambda$) act. The ket space for the entire electromagnetic field is the tensor product over the modes,

:::{math}
:label: eq-quantemf-9
\ES_em = \prod_\lambda \otimes \ES_\lambda.
:::

An arbitrary (pure) quantum state of the electromagnetic field is a ket in the space $\ES_em$.

The energy eigenstates of $H$ are specified by a list of quantum numbers $(\ldots n_\lambda\ldots)$, one for each mode of the field; the eigenstates themselves can be written in various ways,

:::{math}
:label: eq-quantemf-10
\ket{\ldots n_\lambda \ldots} =\prod_\lambda \otimes \ket{n_\lambda}.
:::

The creation/annihilation operators act on these eigenstates in the usual way,

:::{math}
:label: eq-quantemf-11
\begin{aligned}
a_\lambda \ket{\ldots n_\lambda \ldots} &= \sqrt{n_\lambda} \, \ket{\ldots n_\lambda-1 \ldots}, \\
a^\hc_\lambda \ket{\ldots n_\lambda \ldots} &= \sqrt{n_\lambda+1} \, \ket{\ldots n_\lambda+1 \ldots}, \\

\end{aligned}
:::

where it is understood that $a^\dagger_\lambda$ only raises the quantum number for mode $\lambda$, and leaves all the others alone; and similarly $a_\lambda$ only lowers the quantum number for mode $\lambda$. See {eq}`eq-harmosc-37`. We will call the basis $\ket{\ldots n_\lambda \ldots}$ the *occupation number* basis.

The ground state of the free field is the state with all $n_\lambda=0$, which we denote simply by $\ket{0}$,

:::{math}
:label: eq-quantemf-12
\ket{0} = \ket{\ldots 0 \ldots}.
:::

We call $\ket{0}$ the *vacuum state*. It is not to be confused with the zero ket; the vacuum is a state of unit norm, $\braket{0}{0}=1$. The vacuum ket is annihilated by any annihilation operator and the vacuum bra is annihilated by any creation operator,

:::{math}
:label: eq-quantemf-13
a_\lambda\ket{0}=0, \qquad \bra{0}a^\hc_\lambda =0.
:::

On the other hand, by applying creation operators to the vacuum, we can build up any of the energy eigenstates. That is, we have

:::{math}
:label: eq-quantemf-14
\ket{\ldots n_\lambda \ldots} = \prod_\lambda {(a^\hc_\lambda)^{n_\lambda} \over \ds \sqrt{n_\lambda!}} \ket{0},
:::

which is a generalization of {eq}`eq-harmosc-38` for a one-dimensional, mechanical oscillator.

(sec-quantemf-4)=

## The Energy of the Vacuum

The vacuum is the state of minimum energy of the electromagnetic field. Unfortunately, according to {eq}`eq-quantemf-7`, this energy is infinite:

:::{math}
:label: eq-quantemf-15
\matrixelement{0}{H}{0} = \sum_\lambda {\hbar\omega_k\over 2}=\infty.
:::

The vacuum energy is the infinite sum of the zero point energies of all the oscillators that make up the field. In the case of mechanical harmonic oscillators with a finite number of degrees of freedom, the zero point energy is real and physically meaningful, but here in the case of the electromagnetic field it is an embarrassment that causes difficulties of physical interpretation.

The zero point energy is just one of several classes of infinities that arise in quantum field theory, and it is one of the easier ones to rationalize away. In one approach, we simply argue that for most physical processes the definition of the origin of energy is a matter of convention, since it is only differences in energy that matter. Adding a constant to the Hamiltonian does not affect the equations of motion (either the classical Hamilton equations or the Heisenberg equations in quantum mechanics), so we ought to be able to throw the zero point energy away since it is just a constant, albeit an infinite one.

In another approach, we can argue that the zero point energy is connected with the ambiguities inherent in the quantization of classical Hamiltonians containing nontrivial orderings of $q$'s and $p$'s. It is true that the Hamiltonian {eq}`eq-quantemf-3` does not have any $q$-$p$ products, but that is true only in the $(Q_\lambda,P_\lambda)$ system of canonical coordinates. In another coordinate system there would be nontrivial products. For example, classically there is no difference between $a_\lambda^\cc a_\lambda$ and $a_\lambda a_\lambda^\cc$, but in quantum mechanics $a_\lambda^\hc a_\lambda = a_\lambda a_\lambda^\hc - 1$. Therefore if we decided to quantize by replacing $a$'s and $a^\cc$'s by $a$'s and $a^\hc$'s, the quantum Hamiltonian would depend on the ordering of the classical $a$'s and $a^\cc$'s. By using different orderings, we could get the Hamiltonian {eq}`eq-quantemf-7`, or one having twice the zero point energy, or one with no zero point energy at all. Without further rationalization, we will choose the latter possibility, so that the Hamiltonian becomes

:::{math}
:label: eq-quantemf-16
H = \sum_\lambda \hbar\omega_k \, a^\hc_\lambda a_\lambda,
:::

and so that the energy of the state $\ket{\ldots n_\lambda \ldots}$ is given by

:::{math}
:label: eq-quantemf-17
H \ket{\ldots n_\lambda \ldots} = \Bigl( \sum_\lambda n_\lambda \, \hbar\omega_k \Bigr) \ket{\ldots n_\lambda \ldots},
:::

or,

:::{math}
:label: eq-quantemf-18
\matrixelement{\ldots n_\lambda \ldots}{H} {\ldots n_\lambda \ldots} = \sum_\lambda n_\lambda\hbar \omega_k.
:::

In particular, the energy of the vacuum is zero.

(sec-quantemf-5)=

## Is the Zero-Point Energy Real?

As mentioned, the correctness of a quantum theory can only be verified by comparison with experiment. Are there any observable consequences of the zero point energy that we have just thrown away? In a mechanical oscillator, one can in principle change the spring constant, that is, the frequency of the oscillator. If we take a harmonic oscillator, initially in its ground state, and slowly change the frequency from its initial value to zero, then work is done as the ground state wave packet slowly expands. It is like the work done by a gas as the volume of its container is increased. In this way the ground state energy $\hbar\omega/2$ can be accessed. There are many other ways of showing that the zero point energy of a mechanical oscillator is real.

In the case of the electromagnetic field we cannot change the frequencies of the modes, but we can change the structure of the modes with conductors that change the boundary conditions satisfied by the electromagnetic field. For example, let us consider a parallel-plate capacitor. For simplicity we idealize the conductors as having infinite conductivity at all frequencies. Then the modes of the field are modified from what they would be in empty space, because of the presence of the conductors. In particular, the light waves between the plates have a mode structure similar to the energy eigenfunctions of a particle in a box.

If one quantizes the electromagnetic field in the presence of the plates, one gets one harmonic oscillator for each mode, just as in the absence of the plates, and the total zero-point energy is still infinite. But it turns out that it is possible to make sense of the *difference* between the infinite zero-point energy in the presence of the plates, and that in the absence of the plates, and that the result is finite (or rather, the energy per unit area of the capacitor plates is finite). That is, one can make sense of the difference between two infinities. This difference can be interpreted as the change in ground state energy of the field when the plates are introduced. If $L$ is the distance between the plates, then it turns out that this energy per unit area of the plates is given by

:::{math}
:label: eq-quantemf-19
{E\over A} = -{\pi^2\,\hbar c \over 720 L^3},
:::

which depends on $L$.

Thus we obtain the prediction that as the distance between the plates is varied, work must be done to make up for the change in the zero point energy. That is, there must be a force between the plates, or rather a pressure, which is a force per unit area:

:::{math}
:label: eq-quantemf-20
{F\over A} = -\dod{}{L}\Bigl({E\over A}\Bigr) =-{\pi^2 \,\hbar c \over 240 L^4}.
:::

This is called the *Casimir effect* (see *Proceedings of the Koninklijke Nederlandse Akademie van Wetenschappen* **51**, 793(1948)). Of course there will be an electrostatic force between the plates if they carry a charge, but this is a prediction of a force between the plates when they are both electrically neutral, with a particular dependence on the distance. Because of the minus sign in {eq}`eq-quantemf-20`, the force is attractive.

The Casimir effect has been tested experimentally, and the results agree with the theory. Experimentally it is difficult to keep a pair of plates exactly parallel, so some of the work has involved conductors of different shapes. See Steve K. Lamoreaux, *Phys.{* Rev.{} Lett.} **78**, 5(1997). Nevertheless, the basic idea is as described here. There has been renewed interest in the Casimir effect in recent years, because of applications in nanophysics.

The zero point energy is not just an infinite energy, it is an infinite energy *density*. That is because we are using box normalization, so when we divide the (infinite) zero point energy by the volume $V$ of the box, we still have an infinite result. We stated above that for most physical processes it is only energy differences that are important, but there is one place where the absolute amount of energy matters, and that is in gravity. Since energy and mass are related by $E=mc^2$, energy corresponds to mass which produces gravitational fields. An infinite mass density obviously makes no sense in gravitational theory, but we can argue that the sum over modes in sum {eq}`eq-quantemf-15` for the zero point energy should be cut off when the wave length becomes comparable to the Planck length (see {eq}`eq-spatialdof-67`. This gives a finite but very large energy density in space. The energy density is one component of the stress energy tensor, which is the source of the gravitational field in general relativity. The other components of the stress energy tensor associated with the zero point of the field can also be computed, and they give rise to a source term in the Einstein equations for the gravitational field that is of the form $\Lambda\,g_{\mu\nu}$, that is, they have the same form as the cosmological term, where $\Lambda$ is the cosmological constant. Recent observations give a small, positive numerical value for the cosmological constant. This contribution to the stress-energy tensor, the source of the gravitational field, is sometimes called “dark energy” (not to be confused with “dark matter”). Unfortunately, the value of $\Lambda$ obtained from the zero point dynamics of quantum fields is enormously much larger than the observed value (by a factor of something like $10^{120}$). No one knows the reason for this large discrepancy, but the suspicion remains that the zero point dynamics of quantum fields have something to do with the cosmological term in general relativity, and hence with the expansion of the universe.

(sec-quantemf-6)=

## Photons

We saw classically that the normal variable $a_\lambda$ is proportional to the amplitude of a plane electromagnetic wave of mode $\lambda=(\kvec,\mu)$. Thus, the classical quantity $|a_\lambda|^2 = a^\cc_\lambda a_\lambda$ is proportional to the energy in the mode. But in quantum mechanics, we are finding that the energy in mode $\lambda$, which is proportional to the expectation value of $a^\hc_\lambda a_\lambda$, is quantized in units of $\hbar\omega_k$. This of course is exactly as in the original quantum hypothesis developed by Planck and Einstein, and we are led to interpret a state with quantum number $n_\lambda$ as one containing $n_\lambda$ photons, each with energy $\hbar\omega_k$.

Actually, Planck only suggested that energy transfers between matter and radiation should take place in units of $\hbar\omega$. It was Einstein who insisted that the energy in the field itself should be restricted to multiples of $\hbar\omega$ (that is, the energy in a mode with frequency $\omega$). He also suggested that these energy quanta should be associated with particles, that is, particles of light. At the time everyone thought Einstein was crazy, but in the end he proved to be right.

Thus we have the beginning of the particle interpretation of the quantum states that belong to the ket space $\ES_em$. In the following discussion we will gradually flesh out this interpretation by examining successively the momentum, spin and statistics, and angular momentum of these particles. In the process, we will see that the formalism we have developed for the quantization of the field incorporates a quantum mechanical description of a system in which particles can be created or destroyed, so that the number of particles is variable. The particles in question are photons, which can be created in arbitrary numbers at arbitrarily low energies, because they are massless. But the formalism we will develop serves as a paradigm for higher energy (relativistic) processes in which massive particles can be created or destroyed.

(sec-quantemf-7)=

## The Momentum of the Field, and of Photons

Einstein also suggested that a photon of energy $\hbar\omega$ should have a momentum of $\hbar\kvec$, where $\omega$ and $\kvec$ are related by the classical dispersion relation for light waves, $\omega=c|\kvec|$. We turn now to the momentum of the electromagnetic field, and to the momentum of photons.

To investigate the momentum in the quantum theory, we must transcribe the classical momentum given by {eq}`eq-classemf-99` into a quantum operator. For the present we are working with the free field only, for which the matter terms can be dropped and for which $\Evec=\Evec_\perp$. Therefore the momentum is purely that of the field, given by the second term in {eq}`eq-classemf-99`,

:::{math}
:label: eq-quantemf-21
\Pvec = {1\over 4\pi c} \int d^3\xvec \, \Evec\cross \Bvec
:::

Classically, the fields are functions of the $a$'s and $a^\cc$'s; our strategy will be to transcribe these to $a$'s and $a^\hc$'s to get a quantum operator.

We begin with the fields $\Avec$, $\Evec=\Evec_\perp$ and $\Bvec$, which are expressed classically in terms of $a$'s and $a^\cc$'s by {eq}`eq-classemf-103`, {eq}`eq-classemf-105` and {eq}`eq-classemf-106`. When we transcribe these over to quantum mechanics, replacing $a$'s and $a^\cc$'s by $a$'s and $a^\dagger$'s, we obtain the operators,

:::{math}
:label: eq-quantemf-22
\begin{aligned}
\Avec(\xvec) &= \sqrt{2\pi\hbar c^2 \over V} \sum_\lambda {1\over\sqrt{\omega_k}} \bigl( \epsilonvec_\lambda a_\lambda e^{i\kvec\cdot\xvec} + \epsilonvec^\cc_\lambda a_\lambda^\hc e^{-i\kvec\cdot\xvec} \bigr),
\end{aligned}
:::

:::{math}
:label: eq-quantemf-23
\begin{aligned}
\Evec_\perp(\xvec) &= {1\over c} \sqrt{2\pi\hbar c^2\over V} \sum_\lambda \sqrt{\omega_k} \bigl( i\epsilonvec_\lambda a_\lambda e^{i\kvec\cdot\xvec} -i\epsilonvec_\lambda^\cc a_\lambda^\hc e^{-i\kvec\cdot\xvec} \bigr),
\end{aligned}
:::

:::{math}
:label: eq-quantemf-24
\begin{aligned}
\Bvec(\xvec) &= \sqrt{2\pi\hbar c^2\over V} \sum_\lambda {1\over \sqrt{\omega_k}} \bigl[ i(\kvec\cross\epsilonvec_\lambda) a_\lambda e^{i\kvec\cdot\xvec} -i(\kvec\cross\epsilonvec^\cc_\lambda) a_\lambda^\hc e^{-i\kvec\cdot\xvec} \bigr].
\end{aligned}
:::

Just as in classical field theory, the field point $\xvec$ is regarded merely as a parameter of the fields, but now the fields themselves are operators, since the right hand sides are linear combinations of the operators $a_\lambda$ and $a^\hc_\lambda$. Thus, $\Avec(\xvec)$, $\Evec_\perp(\xvec)$, and $\Bvec(\xvec)$ are now seen as fields of operators that act on the ket space of the quantized system; they are our first examples of *quantum fields*. We note that just as the classical fields are real, these quantum fields are Hermitian. As usual in quantum mechanics, Hermitian operators correspond to measurements that can be made on a physical system, and such measurements are subject to statistical fluctuations and the constraints of the uncertainty principle. We will see that such features are present in the measurement of the quantized electromagnetic fields.

To return to the momentum, the expression {eq}`eq-quantemf-21` for $\Pvec$ is classical. The classical fields $\Evec$ and $\Bvec$ that appear in the integrand can be expanded as linear combinations of $a$'s and $a^\cc$'s, according to {eq}`eq-classemf-105` and {eq}`eq-classemf-106`. But when we replace the $a$'s and $a^\cc$'s by $a$'s and $a^\hc$'s in order to obtain the quantum expression for $\Pvec$, there arises the question of the proper ordering of the classical $a$'s and $a^\cc$'s. We could simply follow the ordering given by $\Evec_\perp\cross\Bvec$, but this as it turns out leads to an infinite zero point momentum, much like the zero point energy in {eq}`eq-quantemf-7`. We would like to have $\matrixelement{0}{\Pvec}{0}=0$, so the momentum of the vacuum would vanish. We can accomplish this if we order the $a$'s and $a^\cc$'s in the classical formula by placing all $a^\cc$'s to the left of all $a$'s, and then replacing the $a$'s and $a^\cc$'s by $a$'s and $a^\hc$'s. Then when we compute the vacuum expectation value of $\Pvec$, there will always be an annihilation operator next to the vacuum ket $\ket{0}$, or a creation operator next to the vacuum bra $\bra{0}$, and the result will vanish.

The following notation is convenient for this purpose. If we have any polynomial in $a$'s and $a^\hc$'s, we will define the *normal ordered* polynomial as the rearrangement obtained by moving all $a^\hc$'s to the left and all $a$'s to the right. In this process, we discard any commutators of $a$'s and $a^\hc$'s (effectively, we work with the classical expression, then replace $a$'s and $a^\cc$'s by $a$'s and $a^\hc$'s.) If $Q$ is such a polynomial, we denote its normal ordered rearrangement by $\lcolon Q \rcolon$. For example, we can write the quantum Hamiltonian of the free electromagnetic field as

:::{math}
:label: eq-quantemf-25
H = {1\over 8\pi} \int d^3\xvec \; \lcolon E_\perp^2 + B^2 \rcolon,
:::

and the momentum of the free field is

:::{math}
:label: eq-quantemf-26
\Pvec = {1\over 4\pi c} \int d^3\xvec \; \lcolon \Evec_\perp \cross \Bvec \rcolon.
:::

Let us now express the free field momentum $\Pvec$ in terms of $a$'s and $a^\hc$'s. We substitute {eq}`eq-quantemf-23` and {eq}`eq-quantemf-24` into {eq}`eq-quantemf-26`, and obtain

:::{math}
:label: eq-quantemf-27
\begin{aligned}
\Pvec &= {1\over 4\pi c} \int d^3\xvec \, {1\over c} {2\pi\hbar c^2 \over V} \sum_{\lambda\lambda'} \sqrt{\ds {\omega \over \omega'}} \, \lcolon\bigl[ i\epsilonvec_\lambda a_\lambda e^{i\kvec\cdot\xvec} - i \epsilonvec^\cc_\lambda a^\hc_\lambda e^{-i\kvec\cdot\xvec} \bigr] \\
&\qquad \times \bigl[ i(\kvec' \cross\epsilonvec_{\lambda'}) a_{\lambda'} e^{i\kvec'\cdot\xvec} -i(\kvec' \cross\epsilonvec^\cc_{\lambda'}) a^\hc_{\lambda'} e^{-i\kvec'\cdot\xvec} \bigr]\rcolon,
\end{aligned}
:::

where $\lambda=(\kvec\mu)$, $\lambda'=(\kvec'\mu')$, and $\omega=\omega_k$, $\omega'=\omega_{k'}$. There are four major terms in this expression. Let us first consider the term involving the product $a_\lambda a_{\lambda'}$:

:::{math}
:label: eq-quantemf-28
\begin{aligned}
a_\lambda a_{\lambda'}-\text{term} &= - {\hbar \over 2V} \int d^3\xvec \, \sum_{\kvec\kvec'} \sum_{\mu\mu'} \sqrt{\ds {\omega \over \omega'}} \, \bigl[ \epsilonvec_{\kvec\mu} \cross (\kvec' \cross \epsilonvec_{\kvec'\mu'}) \bigr] \, a_{\kvec\mu} a_{\kvec'\mu'} \, e^{i(\kvec+\kvec')\cdot\xvec} \\
&=+{\hbar \over 2} \sum_{\kvec\mu\mu'} [\epsilonvec_{\kvec\mu} \cross (\kvec \cross\epsilonvec_{-\kvec,\mu'})] \, a_{\kvec\mu} a_{-\kvec,\mu'},
\end{aligned}
:::

where we have used

:::{math}
:label: eq-quantemf-29
{1\over V} \int d^3\xvec \, e^{i(\kvec+\kvec')\cdot\xvec} = \delta_{\kvec,-\kvec'}.
:::

Note that after setting $\kvec'=-\kvec$, we have $\omega'=\omega$. Next we expand out the double cross product and use {eq}`eq-classemf-52`, so that {eq}`eq-quantemf-28` becomes

:::{math}
:label: eq-quantemf-30
\\text{a_\lambda a_{\lambda'}-term} = {\hbar\over 2} \sum_{\kvec\mu\mu'} \kvec (\epsilonvec_{\kvec\mu} \cdot \epsilonvec_{-\kvec,\mu'})\, a_{\kvec\mu} a_{-\kvec,\mu'}= -{\hbar\over 2} \sum_{\kvec\mu\mu'} \kvec (\epsilonvec_{-\kvec,\mu'} \cdot \epsilonvec_{\kvec\mu}) \, a_{-\kvec,\mu'} a_{\kvec\mu},
:::

where in the second equality we have replaced the dummy index of summation $\kvec$ by $-\kvec$, and swapped the indices $\mu$, $\mu'$. However, since $[a_{\kvec\mu}, a_{-\kvec,\mu}]=0$, the whole expression is equal to the negative of itself, and therefore vanishes. In a similar manner we find that the term in {eq}`eq-quantemf-27` involving $a^\hc_\lambda a^\hc_{\lambda'}$ also vanishes.

This leaves the terms involving $a_\lambda a^\hc_{\lambda'}$ and $a^\hc_\lambda a_{\lambda'}$, of which the first becomes $a^\hc_{\lambda'} a_\lambda$ upon normal ordering. By an analysis similar to that above, this term is

:::{math}
\begin{aligned}
:label: eq-quantemf-31
\\text{a^\hc_{\lambda' a_\lambda}-term} &= {\hbar\over 2V} \int d^3\xvec \, \sum_{\kvec\kvec'} \sum_{\mu\mu'} \sqrt{\ds {\omega \over \omega'}} \, \bigl[ \epsilonvec_{\kvec\mu} \cross (\kvec' \cross \epsilonvec^\cc_{\kvec'\mu'})\bigr] \, a^\hc_{\kvec'\mu'} a_{\kvec\mu} \, e^{i(\kvec-\kvec')\cdot\xvec} \\
&= {\hbar\over2} \sum_{\kvec\mu\mu'} \epsilonvec_{\kvec\mu} \cross (\kvec \cross \epsilonvec^\cc_{\kvec\mu'}) \, a^\hc_{\kvec\mu'} a_{\kvec\mu} \\
&= {\hbar\over2} \sum_{\kvec\mu} \kvec \, a^\hc_{\kvec\mu} a_{\kvec\mu} = {1\over 2} \sum_\lambda \hbar \kvec \, a^\hc_\lambda a_\lambda,
\end{aligned}
:::

where we have used {eq}`eq-classemf-51` in expanding the double cross product. Similarly, the $a^\hc_\lambda a_{\lambda'}$ term gives the same answer, and doubles it. Altogether, we find

:::{math}
:label: eq-quantemf-32
\Pvec = \sum_\lambda \hbar\kvec \, a^\hc_\lambda a_\lambda = \sum_\lambda \hbar\kvec \, N_\lambda,
:::

where $N_\lambda$ is the number operator.

The momentum operator $\Pvec$ commutes with the Hamiltonian $H$, and is diagonal in the occupation number basis $\ket{\ldots n_\lambda\ldots}$ of energy eigenkets. The occupation number basis states are not only eigenstates of energy, but also of momentum. Explicitly, we have

:::{math}
:label: eq-quantemf-33
\Pvec \ket{\ldots n_\lambda \ldots} = \Bigl( \sum_\lambda n_\lambda \, \hbar\kvec \Bigr) \ket{\ldots n_\lambda \ldots}.
:::

We see that, just as the energy of a mode of the field is quantized in integer multiples of $\hbar\omega_k$, the momentum in the mode is quantized in integer multiples of $\hbar\kvec$. We interpret this by saying that the photon is a particle of energy $\hbar\omega_k$ and momentum $\hbar\kvec$, which is completely in accordance with the dispersion relation $\omega=ck$ for a light wave, as well as the relativistic energy-momentum relation $E=cp$ for a massless particle. This is exactly as predicted by Einstein.

(sec-quantemf-8)=

## History of the Planck Radiation Law, and the Birth of Quantum Mechanics

Quantum mechanics was born in 1900 with Planck's announcement of his expression for the energy density per unit frequency in black body radiation. Planck and others had been working on the black body spectrum for a number of years, and by the 1890's the high frequency part of the spectrum was known, due to some work by Wien. This part of the spectrum already contained Planck's constant, whose significance as a fundamental constant of nature was appreciated by Planck. In the fall of 1900 Planck was able to make a sophisticated guess as to the correct distribution at all frequencies after seeing some experimental data by Rubens and others on the energy density at intermediate and lower frequencies. He then spent three months of intense work trying to justify the result, finding that he could do so if he hypothesized that energy could be transferred between matter and radiation only in integer multiples of $\hbar\omega$. Neither Planck nor anyone else at the time understood the need for this hypothesis.

This is a fascinating period in the history of physics. In retrospect it is possible to see that Planck was hindered in his researches by a lack of understanding of the fundamental principles of equilibrium statistical mechanics, in which the entropy is the logarithm of the number of accessible states and the statistical distribution of states in thermal equilibrium is determined by the Boltzmann factor. Planck might have been assisted by the papers of J. Willard Gibbs, but apparently he had not read them, perhaps because they were written in English. Instead, Planck followed the usual procedure in those days for finding thermal equilibrium, which was to solve a kinetic equation and to find equilibrium as the long-time limit. This was through the medium of what Boltzmann called an “$H$-theorem.” For this reason Planck spent some considerable effort on detailed models of matter interacting with radiation, looking for an $H$-theorem that would give him the ultimate equilibrium. We now know that finding the equilbrium distribution is much easier than finding out how equilibrium is approached from a non-equilibrium situation.

Planck was further hindered in this effort by a reluctance to introduce statistical arguments into his kinetic theories. Boltzmann had already emphasized the need for statistics, but Planck did not accept his arguments, being overly fixated on the fact that the microscopic equations of motion are time-reversible. Planck and Boltzmann even had some rather sharp and public exchanges over the matter. Nevertheless, reading between the lines, one can see that as Planck's work progressed, he gradually became aware that Boltzmann was right about the need for statistics. After Boltzmann committed suicide in 1906, Planck wrote a memorial essay in which, again reading between the lines, one can see an expression of guilt over his intellectual debt to Boltzmann and his awareness of how much Boltzmann's ideas actually contributed to Planck's greatest accomplishment, his radiation law.

Planck's result attracted almost no attention for several years after its publication, but someone who noticed was Einstein, unknown at this stage of his career. Neither Einstein nor Planck had read Gibb's papers, but Einstein, in his earliest significant publications, rederived much of Gibbs's work on equilibrium statistical mechanics in his own way. Gibbs summarized much of his work in his book, *Elementary Principles in Statistical Mechanics*, which was published in 1902, about the same time as Einstein's papers on the same subject. Naturally, since Einstein had derived much of the same material for himself, he had a slightly different perspective than Gibbs, and, in particular, Einstein was fascinated by the subject of fluctuations about equilibrium. Einstein later used his expertise in statistical mechanics as a principal tool in developing his photon hypothesis.

(sec-quantemf-9)=

## Statistical Mechanics of the Electromagnetic Field

Introductory courses on statistical mechanics usually derive the Planck spectrum by making arguments about the statistics of putting identical particles into boxes. This leaves the impression that special arguments are needed to derive this important result, in addition to the basic principles of statistical mechanics, which are founded on the Boltzmann hypothesis that the probability of finding a state of energy $E$ in a system in thermal equilibrium with a heat bath at temperature $T$ is proportional to $e^{-E/kT}$.

Statistical mechanics normally requires one to work with a system of finite size, so that the energy spectrum is discrete and the total energy finite. This is one place where the box normalization we have been using is not just a mathematical crutch, but is essential for the work at hand.

We consider a box of volume $V$ containing electromagnetic radiation, which is in thermal equilibrium with a heat bath at temperature $T$. We use the usual parameter $\beta=1/kT$, so that the density operator can be written

:::{math}
:label: eq-quantemf-34
\rho = {1\over Z}\, e^{-\beta H},
:::

where $H$, the Hamiltonian for the free field, is given by {eq}`eq-quantemf-16`. As usual, the normalization $Z$ is the partition function,

:::{math}
:label: eq-quantemf-35
Z(\beta) = \tr e^{-\beta H}.
:::

The trace is easily evaluated in the occupation number basis,

:::{math}
:label: eq-quantemf-36
\begin{aligned}
Z(\beta) &= \sum_{(\ldots n_\lambda\ldots)} \matrixelement{\ldots n_\lambda \dots} {\exp\Bigl(-\beta\sum_\lambda \hbar\omega_k \, a^\hc_\lambda a_\lambda\Bigr)} {\ldots n_\lambda \ldots} \\
& \qquad = \sum_{(\ldots n_\lambda\ldots)} \exp\Bigl(-\beta\sum_\lambda n_\lambda \, \hbar\omega_k \Bigr) =\sum_{(\ldots n_\lambda\ldots)} \prod_\lambda e^{-n_\lambda \beta \,\hbar\omega_k},
\end{aligned}
:::

where the sum is taken over all possible integer sequences $(\ldots n_\lambda\ldots)$. But the sum of products is the product of sums, so

:::{math}
:label: eq-quantemf-37
Z(\beta) =\prod_\lambda \sum_{n_\lambda=0}^\infty e^{-\beta n_\lambda \hbar\omega_k} = \prod_\lambda {1\over 1-e^{-\beta \hbar\omega_k}},
:::

where in the final expression we have summed the geometrical series. [If these steps are not clear, try to imagine that the field only has two modes, $\lambda_1$ and $\lambda_2$, and carry out the algbra leading to {eq}`eq-quantemf-37`.]

From the partition function various statistical averages can be computed. For example, the average energy is given by

:::{math}
:label: eq-quantemf-38
E=-\frac{\partial \log Z(\beta)}{\partial \beta}=\sum_\lambda {\hbar\omega_k \over e^{\beta\hbar\omega_k}-1}.
:::

Here the symbol $E$ stands for the statistical average of the energy of the blackbody radiation, taken over the ensemble. {eq}`eq-quantemf-38` shows that the average number of photons in mode $\lambda$ is

:::{math}
:label: eq-quantemf-39
\langle n_\lambda\rangle = { 1 \over e^{\beta\hbar\omega_k}-1},
:::

which is one of the ways of expressing Planck's result. This result can also be obtained directly by averaging $n_\lambda$ over the ensemble.

If the box is big enough that the average wavelength of the photons is much smaller than the dimensions of the box, then we can replace the $\kvec$-sum by an integral, as in {eq}`eq-classemf-35`. That is, we can make the replacements,

:::{math}
:label: eq-quantemf-40
\sum_\lambda = \sum_\kvec \sum_\mu = {2V\over (2\pi)^3} \int d^3\kvec = {8\pi V \over(2\pi)^3} \int_0^\infty k^2 \, dk = {V\over \pi^2 c^3} \int_0^\infty \omega^2 \, d\omega,
:::

where we replace $\sum_\mu$ by 2 since the summand does not depend on polarization, and where we can do the angular integration in $\kvec$-space to get $4\pi$ since the integrand does not depend on the direction of $\kvec$. In the final step we switch from $k$ to $\omega=ck$ as the variable of integration. Altogether, this gives

:::{math}
:label: eq-quantemf-41
{E\over V} = u = {\hbar\over\pi^2 c^3} \int_0^\infty \omega^2 \, d\omega {\omega \over e^{\beta\hbar\omega}-1} = {1\over \pi^2 c^3 \hbar^3 \beta^4} \int_0^\infty {x^3\over e^x-1}\,dx,
:::

where $u$ is the energy per unit volume in the black body radiation and we have set $x=\beta\hbar\omega$ in the integral. If we write

:::{math}
:label: eq-quantemf-42
u=\int_0^\infty d\omega\,\dod{u}{\omega},
:::

then, by the first integral in {eq}`eq-quantemf-41`, we have

:::{math}
:label: eq-quantemf-43
\dod{u}{\omega} = {\hbar\over\pi^2 c^3} {\omega^3 \over e^{\beta\hbar\omega}-1},
:::

which is the usual way of writing the Planck distribution law.

The final integral in {eq}`eq-quantemf-41` can be done by expanding the denominator in a geometric series, so that

:::{math}
:label: eq-quantemf-44
{1\over e^x-1} = {e^{-x} \over 1-e^{-x}} = e^{-x} \sum_{n=0}^\infty e^{-nx} = \sum_{n=1}^\infty e^{-nx}.
:::

This gives

:::{math}
:label: eq-quantemf-45
\int_{0}^\infty {x^3\over e^x-1}\,dx = \sum_{n=1}^\infty \int_0^\infty x^3 e^{-nx}\,dx =3! \sum_{n=1}^\infty {1\over n^4} = 6\, \zeta(4) = {\pi^4\over 15}.
:::

See Abramowitz and Stegun, *Handbook of Mathematical Functions*, Eqs.~(6.1.1) and (6.1.6) for the properties of the $\Gamma$-function, and Eqs.~(23.2.18) and (23.2.25) for the properties of the Riemann $\zeta$-function. Altogether, we obtain

:::{math}
:label: eq-quantemf-46
u = {\pi^2 \over 15} {(kT)^4 \over (\hbar c)^3}.
:::

This expression for the energy density of the black body radiation is closely related to the Stefan-Boltzmann law, which gives the power radiated per unit area by a black body. Boltzmann first gave a theoretical derivation of this result in the 1870's, using classical thermodynamics in a gedankenexperiment in which black body radiation was used as the working fluid in a Carnot cycle. This result for $u$ contains effectively the energy summed over all modes; it does not by itself tell how that energy is distributed among the modes. Planck's formula {eq}`eq-quantemf-43` does that; it was much more difficult to derive.

(sec-quantemf-10)=

## The Schr\"odinger and Heisenberg Pictures

So far we have identified the state space for the free electromagnetic field and some observables acting on this space that correspond to definite physical measurements, including the energy $H$, momentum $\Pvec$ and the various fields $\Avec$, $\Evec$ and $\Bvec$. Measurements of the fields involve some issues that we will explore in \secrquantemf-12.

In this discussion up to this point it has been assumed that we are working in the Schr\"odinger picture. Thus, operators such as $H$ and $\Evec(\xvec)$ are fixed, time-independent operators that act on the state space, while state vectors in that space evolve in time, leading to a time-dependence of the expectation values of these opertors, as well as of other statistics of measurements (dispersions, correlation functions, etc).

The Heisenberg picture, however, reveals a closer correspondence with classical mechanics, both in field theory and in mechanics. See the discussion in {ref}`sec-tevolut-5`. In the Heisenberg picture the state vectors do not evolve in time, whereas the operators do. In particular, the creation and annihilation operators have a time evolution. For the free field the Heisenberg equations of motion for these operators are

:::{math}
:label: eq-quantemf-47
i\hbar\, {\dot a}_\lambda = [a_\lambda,H], \qquad i\hbar \,{\dot a}^\dagger_\lambda = [a^\dagger_\lambda,H],
:::

where $H$ is the sum {eq}`eq-quantemf-16`. Working out the commutators using {eq}`eq-quantemf-6` we find

:::{math}
:label: eq-quantemf-48
{\dot a}_\lambda = -i\omega_k \, a_\lambda, \qquad {\dot a}^\dagger_\lambda = i\omega_k \, a^\dagger_\lambda,
:::

which have the solution,

:::{math}
:label: eq-quantemf-49
a_\lambda(t) = a_\lambda(0)\,e^{-i\omega_kt}, \qquad a^\dagger_\lambda(t) = a^\dagger_\lambda(0) e^{i\omega_kt}.
:::

These are Hermitian conjugates of each other, as they should be.

The time-dependence of $a_\lambda$ and $a^\dagger_\lambda$ engenders a time dependence of the fields $\Avec$, $\Evec$ and $\Bvec$. Thus {eq}`eq-quantemf-22`--{eq}`eq-quantemf-24`, which apply in the Schr\"odinger picture, are replaced in the Heisenberg picture by

:::{math}
:label: eq-quantemf-50
\begin{aligned}
\Avec(\xvec,t) &= \sqrt{2\pi\hbar c^2 \over V} \sum_\lambda {1\over\sqrt{\omega}} \bigl[ \epsilonvec_\lambda a_\lambda(0) \,e^{i(\kvec\cdot\xvec-\omega t)} + \epsilonvec^\cc_\lambda a_\lambda^\hc(0) \,e^{-i(\kvec\cdot\xvec-\omega t)} \bigr],
\end{aligned}
:::

:::{math}
:label: eq-quantemf-51
\begin{aligned}
\Evec_\perp(\xvec,t) &= {1\over c} \sqrt{2\pi\hbar c^2\over V} \sum_\lambda \sqrt{\omega} \bigl[ i\epsilonvec_\lambda a_\lambda(0) \,e^{i(\kvec\cdot\xvec-\omega t)} -i\epsilonvec_\lambda^\cc a_\lambda^\hc(0) \,e^{-i(\kvec\cdot\xvec-\omega t)} \bigr],
\end{aligned}
:::

:::{math}
:label: eq-quantemf-52
\begin{aligned}
\Bvec(\xvec,t) &= \sqrt{2\pi\hbar c^2\over V} \sum_\lambda {1\over \sqrt{\omega}} \bigl[ i(\kvec\cross\epsilonvec_\lambda) a_\lambda(0) \,e^{i(\kvec\cdot\xvec-\omega t)} -i(\kvec\cross\epsilonvec^\cc_\lambda) a_\lambda^\hc(0) \,e^{-i(\kvec\cdot\xvec-\omega t)} \bigr],
\end{aligned}
:::

where $\omega=\omega_k$. These in turn imply the operator equations,

:::{math}
:label: eq-quantemf-53
\Evec = -{1\over c}\dot{\Avec}, \qquad \del\cross\Evec = -{1\over c} \dot{\Bvec}, \qquad \del\cross\Bvec = {1\over c} \dot{\Evec},
:::

which are equivalent to Maxwell's equations for the free field. The non-dynamical equations $\del\cdot\Evec=0$ and $\del\cdot\Bvec=0$ are also implied by {eq}`eq-quantemf-50`--{eq}`eq-quantemf-52`.

We see that Maxwell's equations are valid as they stand in quantum electrodynamics, as long as the fields are interpreted as quantum fields in the Heisenberg picture. We mention that the Heisenberg picture is especially suitable for a covariant description of quantum fields.

(sec-quantemf-11)=

## The Limit $V\to\infty$

The box normalization we have been using up to this point is mostly a matter of mathematical convenience, which allows us to describe the modes of the field by a discrete index $\lambda=(\kvec\mu)$, where $\kvec$ is discrete. But apart from applications like those in \secrquantemf-9 it is nonphysical, and moreover it makes certain topics, such as the angular momentum of the field, impossible to discuss. This is because the angular momentum is the generator of rotations, and the boxes are not invariant under rotations. Therefore, in preparation for subsequent developments, we consider now the changes that take place in our formalism when we take the limit $V\to\infty$.

The rules for taking the limit $V\to\infty$, thereby converting Fourier series into Fourier integrals, were given by {eq}`eq-classemf-35`--{eq}`eq-classemf-37`. We now apply these rules to the Fourier expansions {eq}`eq-quantemf-22`--{eq}`eq-quantemf-24` for the fields $\Avec$, $\Evec_\perp$, and $\Bvec$. First we change notation for the polarization vectors,

:::{math}
:label: eq-quantemf-54
\epsilonvec_{\kvec\mu} \to \epsilonvec_\mu(\kvec),
:::

which is merely a way of reminding ourselves that $\kvec$ is now a continuous variable. Next we note that the annihilation operator $a_{\kvec\mu}$ is like a Fourier coefficient in $\kvec$-space of the field $\Avec(\xvec)$, so we use the rule {eq}`eq-classemf-36` for it, and make the replacement

:::{math}
:label: eq-quantemf-55
a_{\kvec\mu} \to {(2\pi)^{3/2} \over \sqrt{V}} a_\mu(\kvec).
:::

With these changes, the quantum fields become

:::{math}
:label: eq-quantemf-56
\begin{aligned}
\Avec(\xvec) &= \sqrt{2\pi\hbar c^2} \int {d^3\kvec\over (2\pi)^{3/2}} \, {1\over\sqrt{\omega_k}} \\
&\qquad \times \sum_\mu \bigl[ \epsilonvec_\mu(\kvec) a_\mu(\kvec) e^{i\kvec\cdot\xvec} + \epsilonvec^\cc_\mu(\kvec) a_\mu^\hc(\kvec) e^{-i\kvec\cdot\xvec} \bigr],
\end{aligned}
:::

:::{math}
:label: eq-quantemf-57
\begin{aligned}
\Evec_\perp(\xvec) &= {1\over c} \sqrt{2\pi\hbar c^2} \int {d^3\kvec\over (2\pi)^{3/2}} \, \sqrt{\omega_k} \\
&\qquad \times \sum_\mu \bigl[ i\epsilonvec_\mu(\kvec) a_\mu(\kvec) e^{i\kvec\cdot\xvec} -i\epsilonvec_\mu^\cc(\kvec) a_\mu^\hc(\kvec) e^{-i\kvec\cdot\xvec} \bigr],
\end{aligned}
:::

:::{math}
:label: eq-quantemf-58
\begin{aligned}
\Bvec(\xvec) &= \sqrt{2\pi\hbar c^2} \int {d^3\kvec\over (2\pi)^{3/2}} \, {1\over \sqrt{\omega_k}} \\
&\qquad \times \sum_\mu \bigl\{ i[\kvec]\cross\epsilonvec_\mu(\kvec)] a_\mu(\kvec) e^{i\kvec\cdot\xvec} -i[\kvec\cross\epsilonvec^\cc_\mu(\kvec)] a_\mu^\hc(\kvec) e^{-i\kvec\cdot\xvec} \bigr\}.
\end{aligned}
:::

The commutation relations {eq}`eq-quantemf-6` also change; now we have

:::{math}
:label: eq-quantemf-59
[a_\mu(\kvec), a^\hc_{\mu'}(\kvec')] = \delta_{\mu\mu'} \, \delta(\kvec-\kvec'), \qquad [a_\mu(\kvec), a_{\mu'}(\kvec')] = [a^\hc_\mu(\kvec), a^\hc_{\mu'}(\kvec')]=0.
:::

When we go over to the continuum limit ($V\to\infty$), the operators $a_\mu(\kvec)$ and $a_\mu^\hc(\kvec)$ become singular, and have physical meaning only when used in expressions that are integrated over $\kvec$-space. It is easy to see why. When we were working in a box, a single mode was represented by a given plane light wave that was periodic in the box. When we quantize this mode and place, say, one photon in it, we have energy $\hbar\omega$ in volume $V$, so the amplitude of the wave (speaking in classical terms) is finite, and the energy density is nonzero. When we go over to the continuum limit, however, the volume becomes infinite so the energy density corresponding to any finite number of photons in a single mode is zero. The energy of a single photon is still $\hbar\omega$, but if it is placed into a single mode, the energy is spread over all of space. Therefore if we want to obtain a localized distribution of energy, we must form linear combinations of different photon states with different $\kvec$ values, that is, we must construct a wave packet. This will in practice always turn into some kind of integral over $\kvec$-space. It is in this sense that the Dirac delta function occurring in the commutator {eq}`eq-quantemf-59` should be interpreted; we recall that delta functions only have meaning when used under integral signs.

(sec-quantemf-12)=

## Statistics of Measurements of $\Evec$ and $\Bvec$

In general, measurements in quantum mechanics are subject to fluctuations, as we make them across an ensemble of identically prepared systems. The same must be true for the quantum fields $\Avec(\xvec)$, $\Evec(\xvec)$, $\Bvec(\xvec)$, etc. This is in contrast to classical electromagnetism, in which one imagines that field strengths can be measured with arbitrary precision and produce a definite answer. We now examine the question of the measurement of electromagnetic fields, working with the free field for simplicity.

Let us start with the electric fields, given as a Fourier integral over modes by {eq}`eq-quantemf-57`. Notice that $\xvec$ is the location at which the field is measured, and is not an operator. The operator is $\Evec(\xvec)$, corresponding to what is measured. If we measure $\Evec$ at the specific point $\xvec$ when the quantum state of the field is the vacuum $\ket{0}$, then the average value obtained is

:::{math}
:label: eq-quantemf-60
\matrixelement{0}{\Evec(\xvec)}{0} =0 .
:::

This follows because $\Evec(\xvec)$ is a linear combination of creation and annihilation operators, and

:::{math}
:label: eq-quantemf-61
a_\mu(\kvec)\ket{0}=0, \qquad and \qquad \bra{0}a_\mu^\hc(\kvec)=0.
:::

This makes sense: the average value of $\Evec(\xvec)$ in the vacuum should be zero.

But this doesn't mean that the individual measurements will give zero, only the average. To see what happens to individual measurements, let us compute the dispersion, which is

:::{math}
:label: eq-quantemf-62
\begin{aligned}
\matrixelement{0}{\Evec(\xvec)^2}{0} &= 2\pi\hbar \int{d^3\kvec \, d^3\kvec'\over (2\pi)^3} \sum_{\mu\mu'} \sqrt{\omega\omega'} \\
\bra{0} & \Bigl[ia_\mu(\kvec) \epsilonvec_\mu(\kvec) \,e^{i\kvec\cdot\xvec}- ia^\hc_\mu(\kvec)\epsilonvec^\cc_\mu (\kvec)\,e^{-i\kvec\cdot\xvec}\Bigr] \\
\cdot & \Bigl[ia_{\mu'}(\kvec') \epsilonvec_{\mu'}(\kvec') \,e^{i\kvec'\cdot\xvec} - i a^\hc_{\mu'}(\kvec') \epsilonvec^\cc_{\mu'}(\kvec') \,e^{-i\kvec'\cdot\xvec}\Bigr] \ket{0}. \\

\end{aligned}
:::

Of the four major terms, only the one involving $a_\mu(\kvec) a^\hc_{\mu'}(\kvec')$ is nonzero, because all the others have an annihilation operator adjacent to the vacuum ket $\ket{0}$ or a creation operator adjacent to the vacuum bra $\bra{0}$. As for the one term that is nonzero, we have

:::{math}
:label: eq-quantemf-63
\matrixelement{0}{a_\mu(\kvec)a^\hc_{\mu'}(\kvec')}{0} =\matrixelement{0}{a^\hc_{\mu'}(\kvec')a_\mu(\kvec) + \delta_{\mu\mu'}\,\delta(\kvec-\kvec')}{0} = \delta_{\mu\mu'}\,\delta(\kvec-\kvec'),
:::

where we have used the commutator {eq}`eq-quantemf-59`. The Kronecker and Dirac deltas allow us to do the $\mu'$-sum and $\kvec'$-integral. The dot product simplifies,

:::{math}
:label: eq-quantemf-64
\epsilonvec_\mu(\kvec)\cdot\epsilonvec^\cc_{\mu'}(\kvec') \to\epsilonvec_\mu(\kvec)\cdot\epsilonvec^\cc_\mu(\kvec)=1,
:::

and the phase factor disappears,

:::{math}
:label: eq-quantemf-65
e^{i\kvec\cdot\xvec-i\kvec'\cdot\xvec} \to 1,
:::

so we get

:::{math}
:label: eq-quantemf-66
\matrixelement{0}{\Evec(\xvec)^2}{0} = 2\pi\hbar \int {d^3\kvec\over (2\pi)^3} \sum_\mu \omega = {4\pi\hbar c\over (2\pi)^3} \int d^3\kvec \, k = {2\hbar c\over \pi} \int_0^\infty k^3 \,dk,
:::

where we have replaced the $\mu$-sum by 2 and the angular integration by $4\pi$. The final integral diverges, but if we replace the upper limit by some cutoff $k=K$, then we get

:::{math}
:label: eq-quantemf-67
\matrixelement{0}{\Evec(\xvec)^2}{0} = {\hbar c \over 2\pi} \, K^4 \to \infty \quad as \quad K\to\infty.
:::

We should not be surprised by this infinite result, since $E^2/8\pi$ is one term in the energy density of the field, and the vacuum zero-point energy density is infinite, as noted in \secrquantemf-5. Although we threw away the zero-point energy in the Hamiltonian, it reappears in the computation of the dispersion in the measured value of the electric field strength.

How do we reconcile this result with the fact that real measurements of $\Evec$ always give a finite value? One way to understand this is to note that real measuring devices occupy a finite volume, and hence measure the average of $\Evec$ over some region.

Let ${\cal R}$ be a region of space with volume ${\cal V}$ (not to be confused with the volume $V$ of the box---we are not using box normalization here anyway), and let us define the average electric field,

:::{math}
:label: eq-quantemf-68
\bar{\Evec} = {1\over {\cal V}} \int_{\cal R} d^3\xvec \, \Evec(\xvec).
:::

Then we can easily see that $\matrixelement{0}{\bar{\Evec}}{0}=0$. As for the dispersion, it is

:::{math}
:label: eq-quantemf-69
\begin{aligned}
\matrixelement{0}{{\bar{\Evec}}^2}{0} &= {1\over {\cal V}^2} \int_{\cal R}d^3\xvec \, \int_{\cal R}d^3\xvec' \, (2\pi\hbar) \int{d^3\kvec \, d^3\kvec'\over (2\pi)^3} \sum_{\mu\mu'} \sqrt{\omega\omega'} \\
\bra{0} & \Bigl[ia_\mu(\kvec) \epsilonvec_\mu(\kvec) \,e^{i\kvec\cdot\xvec}- ia^\hc_\mu(\kvec)\epsilonvec^\cc_\mu (\kvec)\,e^{-i\kvec\cdot\xvec}\Bigr] \\
\cdot & \Bigl[ia_{\mu'}(\kvec') \epsilonvec_{\mu'}(\kvec') \,e^{i\kvec'\cdot\xvec'} - i a^\hc_{\mu'}(\kvec') \epsilonvec^\cc_{\mu'}(\kvec') \,e^{-i\kvec'\cdot\xvec'}\Bigr] \ket{0}. \\

\end{aligned}
:::

As for the large matrix element in the integrand, it is the same as in {eq}`eq-quantemf-62` except that $\xvec$ in the second factor has been replaced by $\xvec'$. Thus once again only one term of four survives, and it simplifies according to {eq}`eq-quantemf-63`. Once again the $\mu'$-sum and $\kvec'$ integrals can be done, and once again we can use {eq}`eq-quantemf-64`. Now, however, the phase factor becomes

:::{math}
:label: eq-quantemf-70
e^{i\kvec\cdot\xvec - i\kvec'\cdot\xvec'} \to e^{i\kvec\cdot(\xvec-\xvec')},
:::

so altogether we have
:::{math}
:label: eq-quantemf-71
\matrixelement{0}{{\bar{\Evec}}^2}{0} &= {1\over {\cal V}^2} \int_{\cal R}d^3\xvec \, \int_{\cal R}d^3\xvec' \, (2\pi\hbar) \int {d^3\kvec\over(2\pi)^3} \, 2\omega \, e^{i\kvec\cdot(\xvec-\xvec')},
:::

where the polarization sum has been replaced by 2.

We will estimate this integral as an order of magnitude. Since both $\xvec, \xvec' \in {\cal R}$, the distance $|\xvec-\xvec'|$ is less than the linear dimension of ${\cal R}$, call it $L$, so that ${\cal V} \sim L^3$. Now if $k\ll 1/L$, then $\kvec\cdot(\xvec-\xvec') \ll 1$, and

:::{math}
:label: eq-quantemf-72
e^{i\kvec\cdot(\xvec-\xvec')} \approx 1.
:::

But if $k\gg 1/L$, then $e^{i\kvec\cdot(\xvec-\xvec')}$ is rapidly oscillating in $k$, and it chops up the rest of the integrand to give effectively zero. This means that we can estimate the value of the integral by setting the upper limit on $k$ to $K=1/L$, and dropping the phase factor. Then the $\kvec$-integral can be done, and it gives the same result obtained in {eq}`eq-quantemf-67`, with the cutoff $K$. The result is independent of $\xvec$ and $\xvec'$, so

:::{math}
:label: eq-quantemf-73
{1\over{\cal V}} \int d^3\xvec \to 1 \qquad and \qquad {1\over{\cal V}} \int d^3\xvec' \to 1.
:::

Thus we get, as an order of magnitude and dropping dimensionless constants of order unity,

:::{math}
:label: eq-quantemf-74
\matrixelement{0}{{\bar{\Evec}}^2}{0} = \hbar cK^4 = {\hbar cK\over {\cal V}} = {\hbar\omega\over {\cal V}},
:::

where $\omega=cK$ is the cutoff frequency.

We see that quantum electrodynamics predicts that the measurement of electric field strength, with an instrument occupying a volume ${\cal V}=L^3$, will produce fluctuations whose dispersion is given by $\hbar\omega/{\cal V}$, where $\omega=cK=c/L$ (all as an order of magnitude). This is in the vacuum, that is, in the absence of any applied field.

Are these fluctuations real? Yes, charged particles respond to them, and they modify the dynamics of the particle. For example, the Lamb shift is due to the interaction of the atomic electron with the fluctuating electromagnetic field. The theoretical treatment of this effect must, however, take account of infinities that arise in the calculation, and the final answer must be obtained as the difference between two infinities, in a certain sense. Making sense out of the differences between infinities is the business of renormalization theory, without which quantum electrodynamics is rather limited in what it can do. In this course we will mainly study effects that can be understood without renormalization theory, but there is an approximate derivation of the Lamb shift, based on nonrelativistic quantum mechanics and due to Bethe, that is not too difficult to understand and which gives quite good results from a numerical standpoint.

Suppose we are interested in detecting an electromagnetic signal, for example, a radio transmission. Using classical electromagnetic theory, we calculate an electric field $E_signal$ at the location of our detector. But the detector will also pick up quantum fluctuations, call them $E_quant$. The classical signal will only be detected cleanly if $E_signal \gg E_quant$.

Let the size of the antenna be $\lambda$, the wavelength of the signal. Measure the strength of the signal not by the electric field amplitude $E_signal$ but by the number of photons per unit volume, $n$. (Don't confuse this $n$, which has dimensions of number/volume, with the mode numbers $n_\lambda$ used elsewhere in these notes, which are pure numbers.) Then

:::{math}
:label: eq-quantemf-75
E_signal^2 \sim n\hbar\omega \gg E_quant^2 \sim {\hbar\omega\over \lambda^3}.
:::

This gives

:::{math}
:label: eq-quantemf-76
n\lambda^3 \gg 1,
:::

the number of photons in a cubic wavelength must be much greater than 1. This is the usual criterion for the validity of classical electromagnetism in the detection of signals.

(sec-quantemf-13)=

## Helicity Polarization Vectors

For the analysis of the angular momentum of the field, a particular choice of polarization vectors is convenient. These are essentially circular polarization vectors, with a particular phase convention. In general, polarization vectors are two orthonormal, possibly complex unit vectors that span the plane perpendicular to $\kvec$. These vectors are, of course, functions of $\kvec$, or, more precisely, of the direction ${\hat{\mathbf{k}}}$. A convenient way to construct such vectors is to start with two constant, orthonormal unit vectors that span the $x$-$y$ plane, so that taken with ${\hat{\mathbf{z}}}$ they form an orthonormal triad. Then the vectors of this triad are rotated by a rotation matrix $\Rmat$ that is required to map the ${\hat{\mathbf{z}}}$ direction into the ${\hat{\mathbf{k}}}$ direction. We write $\Rmat({\hat{\mathbf{k}}})$ for this matrix; it is a function of ${\hat{\mathbf{k}}}$, and by its definition we have

:::{math}
:label: eq-quantemf-77
\Rmat({\hat{\mathbf{k}}}){\hat{\mathbf{z}}} = {\hat{\mathbf{k}}}.
:::

Such a matrix is easy to construct; if the spherical angles of ${\hat{\mathbf{k}}}$ are $(\theta,\phi)$, then we will take

:::{math}
:label: eq-quantemf-78
\Rmat({\hat{\mathbf{k}}}) = \Rmat_z(\phi)\Rmat_y(\theta) = \Rmat(\phi,\theta,0),
:::

where the final expression is in terms of Euler angles. When the two vectors of the triad that span the $x$-$y$ plane are rotated by $\Rmat({\hat{\mathbf{k}}})$, they become two vectors that span the plane perpendicular to ${\hat{\mathbf{k}}}$, since the orthonormality conditions are preserved by the rotation.

In particular, suppose we take the original triad to be the spherical basis of unit vectors, introduced in {eq}`eq-transfop-40`, which we reproduce here:

:::{math}
:label: eq-quantemf-79
\begin{aligned}
{\hat{\mathbf{e}}}_1 &= -{{\hat{\mathbf{x}}} + i{\hat{\mathbf{y}}} \over \sqrt{2}}, \\
{\hat{\mathbf{e}}}_0 &= {\hat{\mathbf{z}}}, \\
{\hat{\mathbf{e}}}_{-1} &= {{\hat{\mathbf{x}}} - i{\hat{\mathbf{y}}} \over \sqrt{2}}.
\end{aligned}
:::

For light propagating in the $z$-direction, the vector ${\hat{\mathbf{e}}}_1$ corresponds to left circular polarization (the electric field vector rotates counterclockwise in the $x$-$y$ plane), and the vector ${\hat{\mathbf{e}}}_{-1}$ corresponds to right circular polarization light (the electric vector rotates clockwise). These are the conventions used by Jackson, *Classical Electrodynamics* and by Born and Wolf, *Principles of Optics* and by most people in optics, but they are the opposite to what particle physicists would have preferred if they could have established the convention. Apparently for this reason, Sakurai, *Modern Quantum Mechanics*, has reversed the conventions. I think it is less confusing to stay with the standard terminology of optics.

Given the spherical basis {eq}`eq-quantemf-79`, we can define a rotated triad by

:::{math}
:label: eq-quantemf-80
\epsilonvec_{\kvec\mu} = \Rmat({\hat{\mathbf{k}}}) {\hat{\mathbf{e}}}_\mu,
:::

so that $\epsilonvec_{\kvec0}={\hat{\mathbf{k}}}$, and $\epsilonvec_{\kvec\mu}$ for $\mu=\pm1$ span the plane perpendicular to ${\hat{\mathbf{k}}}$ and represent states of circular polarization for waves propagating in the ${\hat{\mathbf{k}}}$ direction. We will henceforth take the index $\mu$ to run over $\pm1$ for these polarization vectors (not 1 and 2, as in {ref}`ch-classemf`). In addition to the orthonormality and completeness relations {eq}`eq-classemf-51`--{eq}`eq-classemf-53`, one can show that these vectors also satisfy the relation $\epsilonvec_{\kvec\mu}=\epsilonvec_{-\kvec,\mu}^\cc$ and the relations

:::{math}
:label: eq-quantemf-81
\epsilonvec_{\kvec\mu} = (-1)^\mu \epsilonvec_{\kvec,-\mu}^\cc,
:::

and

:::{math}
:label: eq-quantemf-82
\epsilonvec_{\kvec\mu}^\cc \cross \epsilonvec_{\kvec\mu} = i\mu {\hat{\mathbf{k}}},
:::

which are valid for $\mu=0,\pm1$. These relations are easily proved because they are just rotated versions of the analogous relations for the constant vectors ${\hat{\mathbf{e}}}_\mu$. We will call the basis of polarization vectors {eq}`eq-quantemf-80` the *helicity* basis.

(sec-quantemf-14)=

## The Longitudinal Polarization

The longitudinal polarization vector $\mu=0$, that is, $\epsilonvec_{\kvec 0}={\hat{\mathbf{k}}}$, is the direction of propagation. Light waves only have the two transverse polarizations $\mu=\pm1$, but if the photon had a mass then it turns out that the the longitudinal polarization would exist as well. The longitudinal polarization is also present when electromagnetic waves propagate through matter; for example, plasma oscillations, which are electrostatic in nature, have a longitudinal polarization.

(sec-quantemf-15)=

## The Angular Momentum of the Photon

We turn now to the angular momentum of the photon. This is a somewhat complicated subject, and we can give only a partial analysis here. The classical angular momentum of the matter-field system is given by {eq}`eq-classemf-100`. We specialize to the case of the free field, for which the angular momentum consists of only the second term in {eq}`eq-classemf-100`,

:::{math}
:label: eq-quantemf-83
\Jvec= {1\over 4\pi c} \int d^3\xvec \; \xvec\cross(\Evec\cross\Bvec),
:::

where $\Evec=\Evec_\perp$. The classical angular momentum of the field $\Jvec$ can be broken into “orbital” and “spin” contributions (borrowing quantum terminology for the classical field). The angular momentum is the generator of rotations, and when we apply an infinitesimal rotation to the classical fields, there arises one term due to the rotation of the value of the field (the “spin”), and another due to the rotation of the point at which the field is evaluated (the “orbital angular momentum”). We write $\Jvec=\Lvec+\Svec$ for these two terms, where

:::{math}
:label: eq-quantemf-84
\Lvec = {1\over 4\pi c} \int d^3\xvec \; \xvec\cross(\del\Avec\cdot \Evec),
:::

and

:::{math}
:label: eq-quantemf-85
\Svec = {1\over 4\pi c} \int d^3\xvec \; \Evec\cross\Avec.
:::

We will transcribe these expressions over into quantum operators, starting with $\Svec$, which is the simpler of the two. We write the spin as a normal ordered operator,

:::{math}
:label: eq-quantemf-86
\begin{aligned}
\Svec &= -{1\over 4\pi c} \int d^3\xvec \; \lcolon \Avec\cross\Evec_\perp \rcolon \\
&=-{\hbar\over 2V} \int d^3\xvec \, \sum_{\lambda\lambda'} \sqrt{\ds \omega' \over \ds \omega} \lcolon \bigl[ \epsilonvec_\lambda a_\lambda e^{i\kvec\cdot\xvec} + \epsilonvec^\cc_\lambda a^\hc_\lambda e^{-i\kvec\cdot\xvec}\bigr] \\
&\qquad\cross \bigl[ i \epsilonvec_{\lambda'} a_{\lambda'} e^{i\kvec'\cdot\xvec} - i\epsilonvec^\cc_{\lambda'} a^\hc_{\lambda'} e^{-i\kvec'\cdot\xvec}\bigr] \rcolon,
\end{aligned}
:::

and then we evaluate terms as we did previously for the momentum $\Pvec$. As before, we find that the terms involving $a_\lambda a_{\lambda'}$ and $a^\hc_{\lambda} a^\hc_{\lambda'}$ vanish, while the remaining two cross terms give equal contributions. The answer can be written in the form,

:::{math}
:label: eq-quantemf-87
\Svec = i\hbar \sum_{\kvec\mu\mu'} \epsilonvec_{\kvec\mu} \cross \epsilonvec^\cc_{\kvec\mu'} \, a^\hc_{\kvec\mu'} a_{\kvec\mu},
:::

which is valid for any choice of polarization vectors. The $\mu$ sum only runs over the transverse polarizations. If, however, we choose the helicity basis {eq}`eq-quantemf-80`, then the cross product vanishes unless $\mu=\mu'$, and we can use the identity {eq}`eq-quantemf-82` to write

:::{math}
:label: eq-quantemf-88
\Svec = \sum_{\kvec\mu} \hbar {\hat{\mathbf{k}}} \mu \, a^\hc_{\kvec\mu} a_{\kvec\mu} =\sum_\kvec \hbar{\hat{\mathbf{k}}} (a^\hc_{\kvec+}a_{\kvec+} - a^\hc_{\kvec-}a_{\kvec-}) = \sum_\kvec \hbar{\hat{\mathbf{k}}} (N_{\kvec+} - N_{\kvec-}),
:::

where $N_{\kvec\pm}$ are the number operators for $\mu=\pm1$.

Just like the energy $H$ and momentum $\Pvec$, the spin $\Svec$ can be expressed purely in terms of number operators, so it commutes with the free-field Hamiltonian and is diagonal in the occupation number basis $\ket{\ldots n_\lambda \ldots}$. We see that photons of $\mu=\pm1$ contribute to the angular momentum of the system an amount that is $\hbar$ times $\pm1$ in the direction of the propagation. As we say, such photons have *helicity* of $\pm1$.

(sec-quantemf-16)=

## The Orbital Angular Momentum of the Field

To discuss the orbital angular momentum of the field {eq}`eq-quantemf-84` it is convenient to introduce a change of notation. We define vector fields of annihilation/creation operators,

:::{math}
:label: eq-quantemf-89
\begin{aligned}
\avec(\kvec) &= \sum_\mu \epsilonvec_\mu(\kvec) a_\mu(\kvec), \\
\avec^\hc(\kvec) &= \sum_\mu \epsilonvec^\cc_\mu(\kvec) a^\hc_\mu(\kvec),
\end{aligned}
:::

which satisfy the commutation relations,

:::{math}
:label: eq-quantemf-90
\begin{aligned}
&[a_i(\kvec), a_j^\hc(\kvec')] = T_{ij}(\kvec) \, \delta(\kvec-\kvec'), \\
&[a_i(\kvec), a_j(\kvec')] = [a^\hc_i(\kvec), a^\hc_j(\kvec')]=0,
\end{aligned}
:::

where $i,j$ refer to the Cartesian components and where $T_{ij}(\kvec)$ is the transverse projection tensor in $\kvec$-space,

:::{math}
:label: eq-quantemf-91
T_{ij}(\kvec) = \delta_{ij} - {k_i k_j \over k^2}.
:::

Fields $\avec(\kvec)$ and $\avec^\hc(\kvec)$ are transverse quantum fields in $\kvec$-space.

Now we can transcribe the classical orbital angular momentum of the field {eq}`eq-quantemf-85` into a normal ordered, quantum operator. We begin with

:::{math}
:label: eq-quantemf-92
\Lvec = {1\over 4\pi c} \int d^3\xvec \; \xvec\cross(\lcolon \del\Avec\cdot \Evec_\perp \rcolon),
:::

and then we express the integrand in terms of creation and annihilation operators. After simplification, we find an expression for the $i$-th component of the orbital angular momentum operator of the free field,

:::{math}
:label: eq-quantemf-93
L_i = {i\hbar\over2}\, \epsilon_{ij\ell} \int d^3\kvec \, k_\ell \Bigl[ \avec^\hc(\kvec) \cdot \frac{\partial \avec(\kvec)}{\partial k_j} - \frac{\partial \avec^\hc(\kvec)}{\partial k_j} \cdot \avec(\kvec) \Bigr].
:::

We see that the orbital angular momentum of the field is not expressed in terms of number operators, nor is it diagonal in the occupation number $\ket{\ldots n_\lambda \ldots}$ basis. This should not be surprising; the modes we have been dealing with are plane waves at the classical level, and we know that planes waves in the quantum mechanics of a single particle are not angular momentum eigenstates. Instead, the nonrelativistic free particle eigenfunctions that are also eigenfunctions of $L^2$ and $L_z$ are spherical Bessel functions times $Y_{\ell m}$'s, times a spinor if the particle has spin. Something like this (but more complicated) is going on here with photon states; it is possible to organize photon states as eigenstates of the angular momentum operators, but our plane wave formalism developed so far has not done this. The subject of the angular momentum of the photon is somewhat lengthy, so we will not go into it further at this point, but some additional remarks will be made below.

For reference, we now write out the energy, momentum and spin of the field in the new (continuum) language:

:::{math}
:label: eq-quantemf-94
\begin{aligned}
H &= \int d^3\kvec \, \hbar\omega_k \, \sum_\mu a^\hc_\mu(\kvec) a_\mu(\kvec) = \int d^3\kvec \, \hbar\omega_k \, \avec^\hc(\kvec)\cdot\avec(\kvec),
\end{aligned}
:::

:::{math}
:label: eq-quantemf-95
\begin{aligned}
\Pvec &= \int d^3\kvec \, \hbar\kvec \, \sum_\mu a^\hc_\mu(\kvec) a_\mu(\kvec) = \int d^3\kvec \, \hbar\kvec \, \avec^\hc(\kvec)\cdot\avec(\kvec),
\end{aligned}
:::

:::{math}
:label: eq-quantemf-96
\begin{aligned}
\Svec &= \int d^3\kvec \, \hbar{\hat{\mathbf{k}}} \sum_\mu \mu \, a^\hc_\mu(\kvec) a_\mu(\kvec) =-i\hbar \int d^3\kvec \, \avec^\hc(\kvec)\cross \avec(\kvec).
\end{aligned}
:::

In the first expression for $\Svec$, we must use the circular or helicity basis of polarization vectors {eq}`eq-quantemf-80`, but any polarization vectors can be used in the other expressions.

(sec-quantemf-17)=

## Particles in Quantum Field Theory

A striking aspect of the formalism of the quantized electromagnetic field that we are developing is that it gives us a new way of describing the quantum mechanics of particles, in this case, photons. We are accustomed to describing the state of a single particle of spin $s$ by means of a wave function $\psi(\xvec,m)$; this is in the $(\xvec,S_z)$-representation, so $m=-s,\ldots,+s$. Similarly, we are accustomed to describing the state of a two-particle system by a wave function $\psi(\xvec_1,m_1;\xvec_2,m_2)$, which if the particles are identical must obey the symmetry requirement,

:::{math}
:label: eq-quantemf-97
\psi(\xvec_1,m_1;\xvec_2,m_2) = \pm \psi(\xvec_2,m_2;\xvec_1,m_1)
:::

($+$ for bosons, $-$ for fermions). In the wave function formalism we have been using, the number of particles is fixed, and is determined by the type of wave function we are using.

But in the quantized electromagnetic field, we describe photon states by the kets $\ket{\ldots n_\lambda \ldots}$, in which the number of photons in each mode is indicated by the integers $n_\lambda$. These occupation numbers can take on any value $n_\lambda =0,1,2,\ldots$, so the ket space $\ES_em$, which is spanned by the occupation number basis kets $\ket{\ldots n_\lambda \ldots}$, includes states for any number of photons. It also includes states that are linear combinations of states of different numbers of photons, but there is no way to form such linear combinations with the wave functions for material particles that we have considered so far in this course.

(sec-quantemf-18)=

## The Wave Function of the Photon

This raises the question, what is the relation between the occupation number basis states $\ket{\ldots n_\lambda \ldots}$ and the usual wave functions we are familiar with? Let us first consider the kets in $\ES_em$ that contain no photons. The only state with no photons is the vacuum $\ket{0}$, which spans a 1-dimensional subspace of $\ES_em$.

Next we consider states of a single photon. A particular single photon state can be created by applying a creation operator to the vacuum, which gives $a^\hc_\mu(\kvec)\ket{0}$ for some $\mu$ and $\kvec$. But this is not the most general single photon state, which would be a linear combination of states of the form $a^\hc_\mu(\kvec)\ket{0}$, with different values of $\mu$ and $\kvec$. We write such a state in the form,

:::{math}
:label: eq-quantemf-98
\ket{\Psi_1} = \int d^3\kvec \, \sum_\mu f(\kvec,\mu) \, a^\hc_\mu(\kvec)\ket{0},
:::

where the $1$-subscript on $\Psi$ simply means that we have a single-photon state, and where the function $f(\kvec,\mu)$ specifies the linear combination. The function $f(\kvec,\mu)$ is an arbitrary complex function, apart from the condition

:::{math}
:label: eq-quantemf-99
\int d^3\kvec \sum_{\mu=\pm1} | f(\kvec,\mu)|^2 = 1,
:::

which is required to make $\braket{\Psi_1}{\Psi_1}=1$. Conversely, given a single photon state $\ket{\Psi_1}$, we can solve for $f$ by using

:::{math}
:label: eq-quantemf-100
f(\kvec,\mu)= \matrixelement{0}{a_\mu(\kvec)}{\Psi_1},
:::

as follows from the commutation relations {eq}`eq-quantemf-59`. We see that (normalized) single particle photon states in $\ES_em$ can be placed into one-to-one correspondence with (normalized) wave functions $f(\kvec,\mu)$, where $\mu=\pm1$. We will call $f(\kvec,\mu)$ the “wave function of the photon.”

Similarly, we can create two-photon states by applying two creation operators to the vacuum, say, $a^\hc_\mu(\kvec) a^\hc_{\mu'}(\kvec') \ket{0}$. An arbitrary two-photon state is a linear combination of such states,

:::{math}
:label: eq-quantemf-101
\ket{\Psi_2} = \int d^3\kvec \, d^3\kvec' \, \sum_{\mu\mu'} f(\kvec,\mu;\kvec',\mu') \, a^\hc_\mu(\kvec) a^\hc_{\mu'}(\kvec') \ket{0}.
:::

We will interpret $f(\kvec,\mu;\kvec',\mu')$ as the wave function of the two-photon state. However, since the two creation operators in {eq}`eq-quantemf-101` commute with one another, they could be applied in the opposite order, with no change to the state $\ket{\Psi_2}$. Therefore the function $f$ might as well be symmetric in the arguments $(\kvec,\mu)$ and $(\kvec',\mu')$,

:::{math}
:label: eq-quantemf-102
f(\kvec,\mu;\kvec',\mu') = f(\kvec',\mu';\kvec,\mu),
:::

because any antisymmetric part would not contribute to $\ket{\Psi_2}$. As a result, we reach the important conclusion that *photons are bosons*.

When we work with wave functions for identical particles, it is possible to write down a wave function that is not properly symmetrized (or antisymmetrized), even though such functions have no physical meaning. But when we specify two-photon states by means of creation operators applied to the vacuum, the states are always properly symmetrized, since the symmetrization is automatically built into the commutation relations of the creation operators. The same holds for states of any number of photons ($n>2$).

There is a similar formalism that works for fermions, and which automatically gives properly antisymmetrized states. This formalism also uses creation and annihilation operators, but the operators are required to satisfy anticommutation relations, instead of commutation relations. See \holedirac.12.

Let us denote the subspace of $\ES_em$ spanned by the vacuum state by $\ES_0$, the subspace spanned by all one-photon states by $\ES_1$, the subspace spanned by all two-photon states by $\ES_2$, etc. Then we have

:::{math}
:label: eq-quantemf-103
\ES_em = \ES_0 \oplus \ES_1 \oplus \ES_2 \oplus \ldots.
:::

Operators that act on $\ES_em$ that have matrix elements connecting the different subspaces $\ES_n$ are capable of changing the number of photons; such operators include the creation and annihilation operators $a_\mu(\kvec)$ and $a_\mu^\hc(\kvec)$, as well as the field operators $\Avec(\xvec)$, etc. The free field Hamiltonian $H$ does not change the number of photons, but the when the matter Hamiltonian is included, the number of photons can change. Thus, in interactions with matter, the number of photons can increase or decrease; this is otherwise just the process of emission and absorption of radiation by matter, which we will consider in detail in subsequent notes.

Actually, the decomposition {eq}`eq-quantemf-103` is naive, because it does not include states with an infinite number of photons. But many of the applications we will consider have only a finite number of photons, and it is true that we can talk about the subspaces of the state space of the electromagnetic field with a fixed number of photons.

The ket space $\ES_em$ is an example of a *Fock space*. There is a mathematical distinction between a Fock space and a Hilbert space that need not concern us; we will simply use these terms for linguistic relief, with a Fock space designating a ket space incorporating a variable number of particles, such as $\ES_em$, and with a Hilbert space designating the ket space with a fixed number of particles. For example, the wave functions $f(\kvec,\mu)$ introduced in {eq}`eq-quantemf-98` belong to a Hilbert space of wave functions, while the ket $\ket{\Psi_1}$ in that equation belongs to the Fock space $\ES_em$.

(sec-quantemf-19)=

## Representations for the Wave Function of the Photon

As we have emphasized, a wave function is just the expansion coefficients of the state vector in some basis. See {ref}`ch-spatialdof`. Moreover, the bases that are normally used for this purpose are the eigenbases of some complete set of commuting observables. For example, in the case of a massive, nonrelativistic particle of spin $s$, the most popular form of the wave function is probably $\psi(\xvec,m) =\braket{\xvec,m}{\psi}$. This is in the $(\xvec,S_z)$-representation, that is, the complete set of commuting observables used for the basis is $(\xvec,S_z)$. Of course, we are free to use other representations if we want to. Now we are calling $f(\kvec,\mu)$ the wave function of the photon, but what is the representation? It turns out that it is the $(\kvec,\Omega)$-representation, where

:::{math}
:label: eq-quantemf-104
\Omega = {\hat{\mathbf{k}}}\cdot\Svec
:::

is the *helicity* operator, and $\mu$ is the eigenvalue of helicity. Also, it turns out that the wave function $f(\kvec,\mu)$ represents the state of a spin-1 particle.

In the following discussion it will be important to distinguish between the Fock space $\ES_em$, the ket space for the electromagnetic field, and the Hilbert space of wave functions of a single particle. Let us begin with the Hilbert space of a massive particle of spin $s$, which can be identified with the space of wave functions $\psi(\xvec,m)$. The vector $\xvec$ is the usual position operator that acts on this space, and the vector $\kvec=\pvec/\hbar$ is proportional to the usual momentum operator. For example, in the $(\xvec,S_z)$-representation, $\xvec$ is represented by multiplication by $\xvec$, and $\kvec$ is represented by $-i\del$. The operators $\xvec$ and $\kvec$, which act on the Hilbert space of a single particle, are not to be confused with the $\xvec$ and $\kvec$ which occur in the theory of the quantized field, which are merely labels of the degrees of freedom of the field, and are not operators. In fact, there is no position operator for the field, and although the field does have a momentum operator [see {eq}`eq-quantemf-95`], it is quite different from the operator $\kvec$ that acts on the single-particle Hilbert space. Similarly, we have the usual orbital angular momentum $\Lvec=\xvec\cross\pvec$ and the usual spin $\Svec$ that act on the Hilbert space of a single particle, but these are not to be confused with the orbital and spin angular momentum operators for the field [see {eq}`eq-quantemf-96` and {eq}`eq-quantemf-93`], which act on $\ES_em$. Finally, the helicity operator $\Omega={\hat{\mathbf{k}}}\cdot\Svec$ acts on the Hilbert space of a single particle; it is not a Fock space operator.

The helicity operator is just the component of the spin in a certain direction (the direction of propagation), so its eigenvalue $\mu$ is like a magnetic quantum number, and takes on the values $\mu=-s,\ldots,+s$. At least, this is the case for a particle of nonzero mass, the only case we have considered so far in this course. But it was shown by Wigner in 1939 that massless particles only have the stretched helicity states, $\mu=\pm s$. For example, the photon, with $s=1$, only possesses the $\mu=\pm1$ states, and the graviton, another massless particle with $s=2$, only possesses the $\mu=\pm2$ states. As we have seen, the exclusion of the $\mu=0$ states for the photon is equivalent to the transversality condition for the fields. But if photons had a nonzero mass, then they would also possess longitudinal polarizations, and all three helicity states would be allowed. Wigner's result can be understood more fully in terms of Lorentz transformations; if a particle has a nonzero mass, then it is always possible to go to the rest frame of the particle, whereupon ordinary spatial rotations can rotate the spin into any direction. But a massless particle has no rest frame.

(sec-quantemf-20)=

## Physical and Nonphysical Operators for a Photon

In the case of a photon, the helicity states $\mu=0$ which would be allowed for a massive particle are simply not present. This means that the physical Hilbert space of wave functions for a photon is only a subspace of the space that would be allowed for a massive particle, and that any (Hilbert space) operator that has nonvanishing matrix elements between the $\mu=\pm1$ subspaces and the $\mu=0$ subspace must be regarded as nonphysical for a photon, since it would map a physically meaningful photon state into a physically meaningless state. As a result, we can classify the operators that act on the state of a massive particle into those that are or are not meaningful when the mass is set to zero. Certainly any operator that commutes with helicity will not mix the eigenspaces of helicity, and so is meaningful when acting on photon states. This includes helicity $\Omega$ itself, as well as the momentum $\kvec$. However, the position operator $\xvec$ does not commute with helicity (because it does not commute with $\kvec$), and is not meaningful for a photon. Thus, the photon does not have a position operator. An eigenfunction of position is a $\delta$-function, but such a function is not transverse. If we project out the transverse part, we get the transverse delta-function {eq}`eq-classemf-24`, which is not localized.

Nor does the photon have an orbital angular momentum operator, because the (Hilbert space) angular momentum $\Lvec=\xvec\cross\pvec$, which is defined for a massive particle, does not commute with helicity ${\hat{\mathbf{k}}}\cdot\Svec$ ($\Lvec$ generates spatial rotations, which rotate the ${\hat{\mathbf{k}}}$ part of the dot product, but leave the $\Svec$ part alone), and it mixes the $\mu=\pm1$ and $\mu=0$ eigenspaces of helicity. Similarly, the photon does not have a spin operator, because $[\Svec,\Omega]\ne0$ and because $\Svec$ mixes the $\mu=\pm1$ and $\mu=0$ subspaces. On the other hand, the total angular momentum $\Jvec=\Lvec+\Svec$ is meaningful as an operator acting on single photon states, since $[\Jvec,\Omega]=0$. Thus, it is possible to talk about the angular momentum states of a photon, it is just not possible to break this up into orbital and spin contribution as we can with a massive particle. (Indeed, as we will see when we study the Dirac equation, there is a more intimate coupling between spin and spatial degrees of freedom in relativistic quantum mechanics than in the nonrelativistic theory, even for massive particles such as the electron.)

Finally, there is one (Hilbert space) operator that does not commute with helicity but which nevertheless is defined for the photon, because it does not mix the $\mu=\pm1$ and $\mu=0$ subspaces. This is the parity $\pi$, defined in the usual way in nonrelativistic quantum mechanics, which satisfies

:::{math}
:label: eq-quantemf-105
\pi \Omega \pi^\hc = -\Omega
:::

($\pi$ flips the sign of ${\hat{\mathbf{k}}}$, but leaves $\Svec$ alone). Parity maps the $\mu=1$ helicity subspace into the $\mu=-1$ subspace (there is no mixing with $\mu=0$ states), and so is allowed for a photon.

Altogether, the single-particle operators that are or are not meaningful for a photon are summarized in Table~quantemf-1. It may seem odd that helicity $\Omega$ is a meaningful operator when it is defined in terms of $\Svec$, which is not meaningful; however, we can just was well write the helicity as $\Omega={\hat{\mathbf{k}}}\cdot\Jvec$, since $\kvec\cdot\Lvec=0$.


{\tiny\singlespacing\bf Table~quantemf-1. \rm Single particle operators that are defined for a massive particle are classified into those that are or are not meaningful for a massless particle, such as the photon. }

Of course, once we have a photon wave function $f(\kvec,\mu)$ in the $(\kvec,\Omega)$-representation, there is no harm in transforming it to another representation such as $(\xvec,S_z)$, as if it were the wave function of a massive particle, so long as we realize that only a restricted class of wave functions of $(\xvec,m)$ will be allowed for a photon (namely, those lying in the $\mu=\pm1$ eigenspaces). To be explicit about this, let us first specify the transformation between the $(\kvec,\Omega)$- and $(\kvec,S_z)$-representations; we will denote the respective wave functions by $f(\kvec,\mu)$ and $f(\kvec,m)$. Then it is easy to show that

:::{math}
:label: eq-quantemf-106
f(\kvec,m) = \sum_\mu D^1_{m\mu}({\hat{\mathbf{k}}}) f(\kvec,\mu),
:::

where $D^1({\hat{\mathbf{k}}})$ is the rotation matrix corresponding to the rotation $\Rmat({\hat{\mathbf{k}}})$ introduced in {eq}`eq-quantemf-77`. Next, to transform from the $(\kvec,S_z)$-representation to the $(\xvec,S_z)$-representation, where we denote the wave function by $f(\xvec,m)$, we simply use the usual Fourier transform,

:::{math}
:label: eq-quantemf-107
f(\xvec,m) = \int {d^3\kvec \over (2\pi)^{3/2}} \, e^{i\kvec\cdot\xvec} \, f(\kvec,m).
:::

There is an alternative form for the wave functions $f(\kvec,\mu)$, $f(\kvec,m)$ or $f(\xvec,m)$ of a spin-1 particle (massive or massless), in which the spin indices are replaced by Cartesian components of an ordinary 3-vector. This (Cartesian) form of the wave function can be specified in two equivalent forms,

:::{math}
:label: eq-quantemf-108
\fvec(\kvec) = \sum_\mu \epsilonvec_\mu(\kvec) f(\kvec,\mu) =\sum_m {\hat{\mathbf{e}}}_m f(\kvec,m),
:::

which is an ordinary (Cartesian) vector field over $\kvec$-space. The wave function $f(\kvec,\mu)$ or $f(\kvec,m)$ lies in the subspace spanned by the helicity states $\mu=\pm1$ if and only if $\fvec(\kvec)$ is transverse, that is, $\kvec\cdot\fvec(\kvec)=0$. If we take the Fourier transform,

:::{math}
:label: eq-quantemf-109
\fvec(\xvec) = \int {d^3\kvec\over (2\pi)^{3/2}} \, e^{i\kvec\cdot\xvec} \, \fvec(\kvec),
:::

we get a (Cartesian) vector field $\fvec(\xvec)$ in ordinary space that is missing the $\mu=0$ helicity state if and only if it is transverse, that is, if $\del\cdot\fvec(\xvec)=0$. Such transverse, Cartesian vector fields $\fvec(\kvec)$ or $\fvec(\xvec)$ are often a convenient way of specifying the wave function of a photon.

(sec-quantemf-21)=

## Vector Multipole Fields

We can now explain the absence of the (Hilbert space) operators $\xvec$, $\Lvec$ and $\Svec$ for a photon from another point of view. First, the orbital angular momentum $\Lvec$ is the generator of spatial rotations, which rotate the point of application of the wave function $\fvec(\xvec)$ or $\fvec(\kvec)$. But if we rotate only the point of application $\kvec$ and not the direction $\fvec$ of the vector field itself, then the transversality condition $\kvec\cdot\fvec(\kvec)=0$ is not preserved. Similarly, the spin $\Svec$ is the generator of rotations of the direction of the vector field $\fvec$, but not its point of application. This also does not preserve the transversality condition. Finally, $\xvec$ is the generator of displacements in $\kvec$-space, and such displacements also do not preserve the transversality condition.

We will now make some comments about the various complete sets of commuting observables that are useful for free particle states, both for massive particles and for photons. In the case of a massive, spinless particle, the most obvious free particle wave functions are the momentum eigenfunctions $\psi(\xvec) = e^{i\kvec\cdot\xvec}$, for which the CSCO is just $\kvec$ (that is, the three commuting components of $\kvec$). Such plane waves are not eigenstates of angular momentum, of course; if we desire these, then we can use the wave functions $\psi(\xvec) = j_\ell(kr) Y_{\ell m}(\theta,\phi)$, for which the CSCO is $(k,L^2,L_z)$. If the particle has spin, then we can multiply by an eigenspinor of $S_z$, and obtain the wave functions $\psi(\xvec,m) = e^{i\kvec\cdot\xvec} \chi^{m_s}_m$ or $j_\ell(kr) Y_{\ell m}(\theta,\phi) \chi^{m_s}_m$, for which the CSCO's are $(\kvec,S_z)$ and $(k,L^2,L_z,S_z)$, respectively. (The spinor $\chi^{m_s}_m$ has components $\delta_{m,m_s}$ in the $S_z$ basis, that is, it is an eigenspinor of $S_z$ with quantum number $m_s$.) Finally, if we desire eigenstates of the total angular momentum, we can combine $\Lvec$ and $\Svec$ with the Clebsch-Gordan coefficients for $\ell \otimes s$, to obtain the CSCO $(k,L^2,J^2,J_z)$.

None of these three obvious choices for the CSCO for the states of a massive free particle, $(\kvec,S_z)$, $(k,L^2,L_z,S_z)$, or $(k,L^2,J^2,J_z)$, will work for a photon, because they all include one or more operators that are meaningless when the mass is zero. If we wish plane wave states, then we must replace $S_z$ with something else. The helicity $\Omega$ is convenient, and this leads to the plane wave, helicity eigenstates, for which the CSCO is $(\kvec,\Omega)$. These are the photon states created by our creation operators $a^\hc_\mu(\kvec)$ [with the choice {eq}`eq-quantemf-80` for polarization vectors]. If we wish eigenstates of angular momentum, then we can include $J^2$ and $J_z$ in the CSCO, but we must replace $L^2$ which may be used for a massive particle. It turns out there are two convenient substitutes for $L^2$, one being the helicity $\Omega$, and the other being parity $\pi$. Thus, we obtain two possible CSCO's for describing photons of definite angular momentum, $(k,J^2,J_z,\Omega)$ and $(k,J^2,J_z,\pi)$. The latter choice is the more popular, because we are often interested in the conservation (or violation) of parity, as well as angular momentum. The single photon wave functions $\fvec(\xvec)$ which are simultaneous eigenfunctions of $(k,J^2,J_z,\pi)$ are called the *vector multipole fields*, and are discussed in Jackson's book. They are messier to work with than plane waves, but necessary when a proper understanding of the conservation of angular momentum is desired.

\problems

(prob-quantemf-1)=

**Problem \prbdquantemf-1.} Sakurai in his book *Advanced Quantum Mechanics.** 

(prob-quantemf-2)=

**Problem \prbdquantemf-2..** 

\problempart{(a)* Given any density operator $\rho$, the entropy is defined by {eq}`eq-density-36` and {eq}`eq-density-37`. Show that if the system is in thermal equilibrium with a heat bath, so that the density operator is given by {eq}`eq-density-38`, then

:::{math}
:label: eq-quantemf-110
F=E-TS = -kT \log Z,
:::

where $F$ is the Helmholtz free energy.

\problempart{(b)} Compute $\log Z$ and hence $F$ for black body radiation in a box of volume $V$. Assume the linear dimensions of the box are large compared to the average wavelength, so the $\kvec$-sum can be replaced by an integral. Then use

:::{math}
:label: eq-quantemf-111
S=-\Bigl(\frac{\partial F}{\partial T}\Bigr)_V, \qquad P=-\Bigl(\frac{\partial F}{\partial V}\Bigr)_T,
:::

to compute the entropy and equation of state.

If an ordinary gas is subjected to an isothermal expansion (we increase $V$ while holding $T$ fixed), then the pressure decreases. Explain in physical terms why this does not happen for a gas of photons. (In both cases the temperature can be held constant by placing the container of gas in contact with a heat bath.)

(prob-quantemf-3)=

**Problem \prbdquantemf-3.}  Assuming the zero-point energy of the electromagnetic field is real, we obtain a finite value of the energy density (or mass density, using $E=mc^2$) if we cut off the $\kvec$-sum in {eq}`eq-quantemf-15` at the Planck length (see {eq}`eq-spatialdof-67`.  That is, take $k_max = 1/L_Planck$.  Calculate this mass density in $gm/cm.** 

The observed value of the cosmological constant $\Lambda$ is $1.1\times 10^{-52\, m^{-2}}\$. According to general relativity, this corresponds to a mass density of

:::{math}
:label: eq-quantemf-112
\rho={c^2\Lambda\over 8\pi G},
:::

where $G$ is Newton's constant of gravitation. Compare this mass density to the one predicted by the zero point motion of the electromagnetic field, using the cutoff suggested in the previous paragraph.

(prob-quantemf-4)=

**Problem \prbdquantemf-4..** 

**Hints:** Use the resolution of the identity, {eq}`eq-classemf-53`. The following identity is also useful:

:::{math}
:label: eq-quantemf-113
\begin{aligned}
[(\Avec\cross\Bvec)\cdot\Cvec] \, [(\Dvec\cross\Evec)\cdot\Fvec] =\det\begin{pmatrix} \Avec\cdot\Dvec & \Avec\cdot\Evec & \Avec\cdot\Fvec\\ \Bvec\cdot\Dvec & \Bvec\cdot\Evec & \Bvec\cdot\Fvec\\ \Cvec\cdot\Dvec & \Cvec\cdot\Evec & \Cvec\cdot\Fvec\\\end{pmatrix}
\end{aligned}

:::

Note that $(\Avec\cross\Bvec)_i$ can be written $(\Avec\cross\Bvec)\cdot {\hat{\mathbf{e}}}_i$, where ${\hat{\mathbf{e}}}_i$ is one of the unit vectors, ${\hat{\mathbf{x}}}$, ${\hat{\mathbf{y}}}$, ${\hat{\mathbf{z}}}$. Also note that

:::{math}
:label: eq-quantemf-114
\delta(\xvec-\xvec') = {1\over V} \sum_{\kvec} e^{i\kvec\cdot(\xvec-\xvec')}.
:::

This is the Fourier series for the $\delta$-function.

(prob-quantemf-5)=

**Problem \prbdquantemf-5.}  Compute the distance $L$ between the plates of a capacitor at which the Casimir pressure {eq}`eq-quantemf-20` is one atmosphere.   One atmosphere is $1.01\times 10^5\, N/m^2 = 1.01\times 10^6\, dyne/{\rm cm.**
