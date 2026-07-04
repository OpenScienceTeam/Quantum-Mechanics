---
title: "30. Helium and Helium-like Atoms"
---
(ch-helium)=

# 30. Helium and Helium-like Atoms

(sec-helium-1)=

## Introduction

In these notes we treat helium and helium-like atoms, which are systems consisting of one nucleus and two electrons. If the nuclear charge is $Z=2$, then we are dealing with ordinary helium, while $Z=3$ is the $Li^+$ ion, $Z=4$ is the $Be^{++}$ ion, etc. In recent years there has been some interest in helium-like uranium, the ion $U^{90+}$, with $Z=92$, for tests of quantum electrodynamics. A case not to be overlooked is $Z=1$, a system consisting of a hydrogen nucleus plus two electrons. This system certainly has unbound states, for example, the states in electron-hydrogen scattering. It is not obvious that it possesses bound states, however, since it is not clear that one proton is capable of binding two electrons. In fact, a bound state of this system does exist, the $H^-$ ion, which can be thought of as an electron bound to an otherwise neutral hydrogen atom. The second electron is rather weakly bound, as we shall see. The ion $H^-$ plays an important role in applications, for example, in energy transport in stellar atmospheres. It is also used in proton accelerators to defeat Liouville's theorem in the process of filling up accelerating rings. In the following discussion of helium-like atoms we focus mostly on the bound states, but some attention is also given to the unbound states.

(sec-helium-2)=

## The Basic Hamiltonian

In these notes we work in atomic units, $e=m=\hbar=1$. We place the nucleus of charge $Z$ at the origin of our system of coordinates and we let $\xvec_1$ and $\xvec_2$ be the positions of the two electrons. Then the basic Hamiltonian describing the helium-like system is

:::{math}
:label: eq-helium-1
H = {\pvec_1^2 \over 2} + {\pvec_2^2 \over 2} - {Z \over r_1} - {Z \over r_2} +{1 \over r_{12}},
:::

where $r_1 = |\xvec_1|$, $r_2=|\xvec_2|$, and $r_{12} = |\xvec_2 - \xvec_1|$.

This Hamiltonian incorporates all the nonrelativistic, electrostatic effects in helium, but it omits a number of small effects and makes some approximations. The approximation in the use of the Hamiltonian {eq}`eq-helium-1` is numerically quite good, but there is some interesting physics in the neglected terms and consideration of them leads to an improved understanding of some of the steps we take in solving the approximate system.

First, the frame attached to the nucleus is not really an inertial frame, since the nucleus is pulled by the electric forces from the electrons and accelerates somewhat in response. The accelerated nucleus then has an effect back on the electrons, so that the overall effect is to couple the dynamics of the electrons. However, since the mass of the nucleus is large in comparison to the mass of the electron, the corrections, which are known as “mass polarization” terms, are small. See Prob.~\cenforce.4, where it is shown that the coupling is proportional to $\pvec_1\cdot\pvec_2$. Similar corrections result from ignoring the small difference between the true electron mass and the reduced mass of the electron and the nucleus. Both these corrections are of order of the electron to nucleus mass ratio, which is approximately $10^{-4}$ in helium.

Second, there are a variety of fine structure terms which, as in hydrogen, can be thought of as relativistic corrections. These are all of order $\alpha^2$ or $(Z\alpha)^2$, and are roughly of order $10^{-3}$ to $10^{-4}$ in helium. (But as in hydrogen, fine structure effects grow with $Z$, and are more important in heavier atoms.) In addition to the relativistic kinetic energy correction, the Darwin term and the spin-orbit term, all of which are present in hydrogen, there are also terms representing the interaction of one electron with the magnetic field produced by the orbital motion of the other electron (spin-other-orbit terms), or produced by the magnetic moment of the other electron (spin-spin terms). There are also terms taking into account retardation in the communication between the two electrons.

Third, there are interactions with the quantized electromagnetic field, generalizations of the Lamb shift in hydrogen.

Finally, there may be hyperfine interactions between the electron and the multipole moments of the nucleus (but not in ordinary helium, since the $\alpha$-particle has spin 0).

With the neglect of all these small terms, the basic helium-like Hamiltonian {eq}`eq-helium-1` is a purely spatial operator, and does not involve the spin. Thus, it is similar in its level of approximation to the electrostatic model of hydrogen. Due to the requirements of the symmetrization postulate, however, spin plays a significant role in the structure of helium, much more so than in hydrogen at a similar level of approximation.

(sec-helium-3)=

## Wave Functions and Hilbert Spaces

As explained in \jjcouple.3, the Hilbert space of a single electron can be written $\ES=\ES_orb\otimes\ES_spin$, where a basis in $\ES_orb$ is the set of position eigenkets $\{\ket{\xvec}\}$ and a basis is $\ES_spin$ is the set of eigenkets $\{\ket{sm}\}$ of the operators $S^2$ and $S_z$, where $s=\frac{1}{2}$ and $m=\pm\frac{1}{2}$. The quantum number $s$ is constant and can be suppressed if it is understood, so sometimes we write simply $\ket{m}$ for the spin eigenkets. A basis in the total Hilbert space is the product basis $\{\ket{\xvec m}\}$ where $\ket{\xvec m}=\ket{\xvec}\ket{m}$. A wave function in the orbital Hilbert space $\ES_orb$ is $\psi(\xvec)=\braket{\xvec}{\psi}$, while one in the total Hilbert space $\ES$ is $\psi_m(\xvec)=\braket{\xvec m}{\psi}$.

In a system with two electrons the total Hilbert space is the product of two copies of the orbital and spin Hilbert spaces for the two electrons,

:::{math}
:label: eq-helium-2
\ES_tot=\ES^{(1)}_orb \otimes \ES^{(1)}_spin \otimes \ES^{(2)}_orb \otimes \ES^{(2)}_spin,
:::

where the numbers in parentheses are the labels of the two electrons. This is the “nominal” Hilbert space discussed in {ref}`ch-identpart`, that is, it consists of the wave functions that we would have if there were no symmetrization postulate. A basis in $\ES_tot$ is the product of the bases in the constituent spaces,

:::{math}
:label: eq-helium-3
\ket{\xvec_1 m_1}^{(1)} \ket{\xvec_2 m_2}^{(2)} =\ket{\xvec_1 \xvec_2 m_1 m_2}.
:::

If we rearrange the factors in {eq}`eq-helium-2` we can write the total two-electron Hilbert space as

:::{math}
:label: eq-helium-4
\ES_tot=\ES_orb\otimes \ES_spin,
:::

where

:::{math}
:label: eq-helium-5a
\begin{aligned}
\ES_orb &= \ES_orb^{(1)} \otimes \ES_orb^{(2)},
\end{aligned}
:::

:::{math}
:label: eq-helium-5b
\begin{aligned}
\ES_spin &= \ES_spin^{(1)} \otimes \ES_spin^{(2)}
\end{aligned}
:::

The factorization {eq}`eq-helium-4` is useful for the study of helium and many other systems with two identical particles. A basis in $\ES_orb$ is the set $\{\ket{\xvec_1\xvec_2}\}$, while there are two obvious bases in $\ES_spin$, the uncoupled and coupled,

:::{math}
:label: eq-helium-6
\{\ket{m_1m_2}\} \qquad or \qquad \{\ket{SM_S}\},
:::

as explained in \identpart.8. Here $S=0$ is the singlet state and $S=1$ indicates the set of triplet states.

{eq}`eq-helium-4` means that an arbitrary wave function in $\ES_tot$ is a linear combination of products of wave functions in $\ES_orb$ and those in $\ES_spin$. In the special case that a wave function in $\ES_tot$ consists of a single product of this type, we can speak of the “spatial part” and “spin part” of the wave function. Such language is very common in discussions of helium and other two- or multi-particle systems, but it is important to realize that it only applies to wave functions of a special type. The reason such wave functions are relevant in the case of helium has to do with the exchange operators that commute with the Hamiltonian {eq}`eq-helium-1`.

(sec-helium-4)=

## Exchange Operators

The Hamiltonian {eq}`eq-helium-1` commutes with three exchange operators that we now define, in terms of their action on the basis kets $\ket{\xvec_1 \xvec_2 m_1 m_2}$ in $\ES_tot$. These are

:::{math}
:label: eq-helium-7
\begin{aligned}
E_{12}^orb \ket{\xvec_1 \xvec_2 m_1 m_2} &= \ket{\xvec_2 \xvec_1 m_1 m_2},
\end{aligned}
:::

:::{math}
:label: eq-helium-8
\begin{aligned}
E_{12}^spin \ket{\xvec_1 \xvec_2 m_1 m_2} &= \ket{\xvec_1 \xvec_2 m_2 m_1},
\end{aligned}
:::

:::{math}
:label: eq-helium-9
\begin{aligned}
E_{12} \ket{\xvec_1 \xvec_2 m_1 m_2} &= \ket{\xvec_2 \xvec_1 m_2 m_1}.
\end{aligned}
:::

We will denote the eigenvalues of these three operators by $e_{12}^orb$, $e_{12}^spin$, and $e_{12}$, respectively.

The Hamiltonian {eq}`eq-helium-1` commutes with $E_{12}^orb$ because it is a purely orbital operator that is symmetrical in the exchange of the two electrons. It commutes with $E_{12}^spin$ because it is a purely orbital operator that commutes with any spin operator. And in view of {eq}`eq-helium-10`, the Hamiltonian {eq}`eq-helium-1` also commutes with $E_{12}$.

But the Hamiltonian {eq}`eq-helium-1` is only an approximation to the true Hamiltonian for helium. If we include the fine structure terms, which as in hydrogen couple the spin and orbital degrees of freedom, then the resulting Hamiltonian no longer commutes with $E_{12}^orb$ or $E_{12}^spin$ separately.

It still commutes with $E_{12}$, however, regardless of how many physical effects we include or how many correction terms we add, because the two electrons are identical. All physical Hamiltonians that describe two electrons commute with $E_{12}$; if this were not true, it would be possible to distinguish the electrons.

The properties of these exchange operators follow immediately from their definitions. The operators are all Hermitian and unitary, their square is 1 (the identity operator), and their eigenvalues are $\pm 1$, as in {eq}`eq-identpart-3` and {eq}`eq-identpart-4`. They also satisfy

:::{math}
:label: eq-helium-10
E_{12} = E_{12}^orb E_{12}^spin,
:::

and

:::{math}
:label: eq-helium-11
[E_{12}^orb, E_{12}^spin] = 0.
:::

Thus $E_{12}^orb$ and $E_{12}^spin$ possess a simultaneous eigenbasis. Since $E_{12}$ is a function of $E_{12}^orb$ and $E_{12}^spin$, any simultaneous eigenspaces of $E_{12}^orb$ and $E_{12}^spin$ is automatically an eigenspace of $E_{12}$, with eigenvalue

:::{math}
:label: eq-helium-12
e_{12} = e_{12}^orb e_{12}^spin.
:::

Since the set of operators $(H,E_{12}^orb,E_{12}^spin)$ are mutually commuting, they possess a simultaneous eigenbasis. Here $H$ is the Hamiltonian {eq}`eq-helium-1`. Equivalently, we can organize the eigenstates of $H$ so that they are also eigenstates of $E_{12}^orb$ and $E_{12}^spin$.

To construct such eigenstates we start with $E_{12}^spin$. Let us use a capital $\Psi$ to refer to states in $\ES_tot$ and a lower case $\psi$ for states in $\ES_orb$. Then an eigenstate of $E_{12}^spin$ is the product

:::{math}
:label: eq-helium-13
\ket{\Psi}=\ket{\psi}\ket{SM_S},
:::

for any $\ket{\psi}\in\ES_orb$, since

:::{math}
:label: eq-helium-14
E_{12}^spin \ket{\Psi} = \sigma_S \ket{\Psi},
:::

where the eigenvalue $e_{12}^spin =\sigma_S$ is defined by {eq}`eq-identpart-45`. The most general eigenstate of $E_{12}^spin$ is a linear combination of such states {eq}`eq-helium-13` with the same value of $S$.

Next, we make $\ket{\Psi}$ an eigenstate of $H$ by requiring that the spatial part $\ket{\psi}$ of $\ket{\Psi}$ be an eigenstate of $H$, regarded as a purely orbital operator. That is, we must solve

:::{math}
:label: eq-helium-15
H\ket{\psi} = E\ket{\psi},
:::

or, in wave function language,

:::{math}
:label: eq-helium-16
H\psi(\xvec_1,\xvec_2) = E \psi(\xvec_1,\xvec_2),
:::

a purely orbital eigenvalue-eigenfunction problem. This is the hard part, something we shall devote some attention to in these notes.

Then, to obtain an eigenfuction also of $E_{12}^orb$, we note that if $\psi(\xvec_1,\xvec_2)$ is a solution of {eq}`eq-helium-16`, then so is $\psi(\xvec_2,\xvec_1)$, with the same energy. Thus we can form the wave functions

:::{math}
:label: eq-helium-17
\psi(\xvec_1,\xvec_2) \pm \psi(\xvec_2,\xvec_1),
:::

which, if they do not vanish, are eigenstates of $E_{12}^orb$ with eigenvalue $e_{12}^orb=\pm 1$ (the same $\pm$ that appears in {eq}`eq-helium-17`.

Finally, in view of {eq}`eq-helium-12`, only those states that are symmetric under spatial exchange and antisymmetric under spin exchange, or vice versa, are antisymmetric under total exchange $E_{12}$, as required by the symmetrization postulate. The physical subspace of the nominal Hilbert space is the direct sum of the subspace with $e_{12}^orb = +1$ and $e_{12}^spin = -1$, and the one with $e_{12}^orb = -1$ and $e_{12}^spin = +1$.

The situation regarding spatial and spin exchange symmetries is summarized in {ref}`tbl-helium-1`, which also indicates some standard nomenclature. As in {ref}`tbl-identpart-1`, “para” refers to a wave function that is spatially symmetric, and “ortho” to one that is spatially antisymmetric under exchange. At one time helium was thought to consist of two different species, parahelium and orthohelium, since the spectrum of helium indicates two classes of energy levels with no (or only very weak) transitions between them. {ref}`tbl-helium-1` is almost exactly the same as {ref}`tbl-identpart-1`, the main difference being that in the case of the hydrogen molecule, it was possible to write down an explicit form for the spatial part of the energy eigenfunctions, {eq}`eq-identpart-33`, since we had a central force Hamiltonian, whereas in helium it is much more difficult to solve the spatial eigenfunction equation {eq}`eq-helium-15`. (And in the hydrogen molecule we had two identical protons, whereas in helium we have two identical electrons.)

:::{list-table} Linkage of spatial and spin exchange symmetry in helium and terminology.
:label: tbl-helium-1
:header-rows: 1

* - $e_{12}^{orb}$
  - name
  - $e_{12}^{spin}$
  - $e_{12}$
  - $S$
  - degen
  - name
* - $+1$
  - para
  - $-1$
  - $-1$
  - $0$
  - $1$
  - singlet
* - $-1$
  - ortho
  - $+1$
  - $-1$
  - $1$
  - $3$
  - triplet

:::
In summary, we have derived the rule about helium eigenfunctions that most students learn in first courses on quantum mechanics, namely, that these eigenfunctions are products of spatial wave functions times spin wave functions with opposite symmetry under exchange. We saw the same rule previously in connection with the hydrogen molecule.

However, the true nature of this rule should be understood. First, the operators $E_{12}^orb$ and $E_{12}^spin$ do not have the same fundamental significance as the overall exchange operator $E_{12}$. In particular, there is no symmetrization postulate for $E_{12}^orb$ or $E_{12}^spin$. Next, the factorization of the energy eigenfunctions into symmetric spatial parts and antisymmetric spin parts, or vice versa, arises because $H$ commutes with $E_{12}^orb$ and $E_{12}^spin$ and because commuting operators possess simultaneous eigenstates. If we had included the small fine structure corrections in the Hamiltonian {eq}`eq-helium-1`, however, then we would find that $H$ no longer commutes with $E_{12}^orb$ or $E_{12}^spin$ separately, although of course it would still commute with $E_{12}$. Thus, the usual rule about the factorization of the wave functions only applies to the nonrelativistic, electrostatic approximation to the helium atom. This is in contrast to the symmetrization postulate itself, which is rigorously correct.

(sec-helium-5)=

## Good Quantum Numbers

Sometimes an operator that commutes with the Hamiltonian is called a “good quantum number.” The terminology is old and it confuses an operator with its quantum number, but it is in common use.

The helium Hamiltonian {eq}`eq-helium-1` is not exactly solvable nor even close to any exactly solvable system (at least for small $Z$), so it is rather difficult to obtain good approximations to its eigenstates and eigenvalues. In cases like this it is especially important to pay attention to the exact symmetries of the Hamiltonian, that is, the operators that commute with it (the “good quantum numbers”). Commuting operators possess simultaneous eigenbases, and, since symmetry operators are usually easier to diagonalize than Hamiltonians, it is usually a good idea to diagonalize them first. This means that we need only search in the eigenspaces of the symmetry operators for the eigenstates of the Hamiltonian, a significantly easier task than searching in the whole Hilbert space. For example, if we must diagonalize a matrix to find the energy eigenstates and eigenvalues, it is best to use a symmetry-adapted basis (one that is already an eigenbasis of the symmetry operators). Even if we do not attempt to find the eigenstates of the Hamiltonian explicitly, we can at least say that those eigenstates are labelled by symmetry labels, namely, the quantum numbers of the symmetry operators. This is a common situation for example in particle physics or nuclear physics, where no one knows how to calculate the masses of the baryons or the energies of nuclear states very accurately, but these states are rigorously characterized by their quantum numbers (spin, parity, etc.)

For the helium Hamiltonian {eq}`eq-helium-1` we have already begun this process, by noting that $H$ commutes with $E_{12}^orb$ and $E_{12}^spin$, and by finding the simultaneous eigenbases of these two operators. This served the dual purpose of narrowing the spaces in which we need to search for energy eigenstates, and of satisfying the symmetrization postulate (by requiring $e_{12}=-1$).

But there are other symmetries of the Hamiltonian {eq}`eq-helium-1`. Most notably, since $H$ is a scalar operator, it commutes with rotations. In fact, since it is a purely spatial operator, it commutes with both spatial and spin rotations independently, and thus with $\Lvec = \Lvec_1 + \Lvec_2 $ and $\Svec=\Svec_1 + \Svec_2$. It does not, however, commute with spatial rotations of particle 1 or of particle 2 separately, because the term $1/r_{12}$ in the Hamiltonian is only invariant when we rotate the positions of both particles simultaneously. That is, $H$ does not commute with $\Lvec_1$ or $\Lvec_2$ separately. The Hamiltonian does commute with $\Svec_1$ and $\Svec_2$ separately, however, in fact, it commutes with any function of spin. But as we have seen, the total spin $\Svec = \Svec_1 + \Svec_2$ is more convenient to work with than the individual spins because it is physical and commutes with $E_{12}^spin$, and because the coupled basis is an eigenbasis of $E_{12}^spin$.

The Hamiltonian {eq}`eq-helium-1` also commutes with parity $\pi$, a purely spatial operator that acts on the basis kets of the entire Hilbert space $\ES$ by

:::{math}
:label: eq-helium-18
\pi \ket{\xvec_1 \xvec_2 m_1 m_2} = \ket{-\xvec_1, -\xvec_2, m_1,m_2}.
:::

Parity flips the spatial coordinates of the particles but has no effect on spin (at least in nonrelativistic quantum mechanics). We will not make much use of parity in the case of helium, but it is more important in multielectron atoms.

:::{list-table} Operators that commute with the approximate helium Hamiltonian (\eqr\cn.1) and their corresponding quantum numbers. The symmetrization postulate forces $e_{12}=-1$.
:label: tbl-helium-2
:header-rows: 1

* - Operator
  - $E_{12}^{orb} $
  - $E_{12}^{spin}$
  - $E_{12}$
  - $L^2$
  - $L_z$
  - $S^2$
  - $S_z$
* - Qu. Num.
  - $e_{12}^{orb}$
  - $e_{12}^{spin}$
  - $e_{12}=-1$
  - $L$
  - $M_L$
  - $S$
  - $M_S$

:::
A list of operators that $H$ commutes with along with their quantum numbers is shown in {ref}`tbl-helium-2`. Moreover these operators commute with each other. Thus, without knowing anything else about the eigenstates of $H$, we can say that they are characterized by the quantum numbers of the operators in the table. However, several of the quantum numbers are superfluous. For example, $e_{12}$ is forced to be $-1$ by the symmetrization postulate, so $e_{12}^orb$ and $e_{12}^spin$ are opposite one another and not independent. In fact, by {eq}`eq-identpart-44` knowledge of $S$ implies knowledge of $e_{12}^spin$ and therefore knowledge of $e_{12}^orb$. Thus an independent set of quantum numbers is $(LM_L SM_S)$. Within a simultaneous eigenspace of the symmetry operators with the given quantum numbers, we can in principle diagonalize the Hamiltonian, and label the energy eigenstates within that subspace by a sequencing number $N$. Thus, the energy eigenstates can be denoted $\ket{NLM_LSM_S}$. As for the energy eigenvalues, they are independent of $M_L$ and $M_S$ because of the rotational invariance of the Hamiltonian, so we can write

:::{math}
:label: eq-helium-19
H \ket{NLM_LSM_S} = E_{NLS} \ket{NLM_LSM_S}.
:::

The energies $E_{NLS}$ are $(2L+1)(2S+1)$-fold degenerate, because of the freedom in the magnetic quantum numbers.

You might suspect that the energies $E_{NLS}$ should also be independent of the total spin $S$, since the Hamiltonian {eq}`eq-helium-1` is a purely spatial operator. That would be true if there were no symmetrization postulate, but in that case the quantum number $e_{12}^orb$ would not be superfluous, and, since $e_{12}^orb$ is a spatial operator itself, the energies would depend on its eigenvalue. In fact, this is precisely what happens in real helium where the symmetrization postulate is operative, it is just that the quantum number $e_{12}^orb$ is not explicitly stated since it is determined by the value of $S$. In other words, in real helium, the spin state specified by $S$ determines the exchange symmetry of the spin part of the wave function which determines the exchange symmetry of the spatial part of the wave function which does affect the energy. Thus, the energy does depend on $S$, in spite of the fact that $H$ is a purely spatial operator.

In fact, the dependence of the energy on $S$ is typically large, that is, of the order of a Coulomb (electrostatic) energy, much larger than the (magnetic) energies associated with the explicitly spin-dependent terms that we have neglected in Hamiltonian {eq}`eq-helium-1`. This is because wave functions that are symmetric or antisymmetric under spatial exchange have very different distributions of probability in three-dimensional space, and therefore correspond to quite different Coulomb energies. We will see this explicitly below when we analyze helium by perturbation theory. A similar phenomenon occurs in ferromagnetism, where the energies involved in flipping spins (the magnetization of the material) are much larger than can be accounted for by the magnetic interaction of arrays of magnetic dipoles. This discrepancy in energy scales was known before quantum mechanics had matured, and was regarded as a mystery. The true explanation was given by Heisenberg: when you flip spins, you change the symmetry of the spin part of the wave function, which by the symmetrization postulate forces changes in the spatial part of the wave function, which changes the Coulomb energy of the charge configuration. Ferromagnets are more complicated because there is a large number of particles, but the basic idea is the same as in helium.

In {ref}`tbl-helium-2` we have listed all the obvious symmetries (except parity) of the basic helium Hamiltonian {eq}`eq-helium-1`. Are there any more (not so obvious) symmetries? Sometimes a system does have additional symmetries in addition to the obvious ones. Notably this happens in the case of hydrogen, which has an $SO(4)$ symmetry (only the $SO(3)$ symmetry under spatial rotations is obvious). This extra symmetry is responsible for the extra degeneracy of hydrogen, in comparison to other central force problems. As we say, hydrogen has “hidden” symmetry. Another example with hidden symmetry is the multidimensional, isotropic harmonic oscillator. Apart from these two examples, however, there are very few systems in the real world with extra or hidden symmetry (it depends partly on your definition of “hidden,” but you should not expect such symmetry in most problems). In particular, helium has no extra symmetry beyond what we have listed.

The standard spectroscopic notation for the level $E_{NLS}$ is $N^{2S+1}L$, where $L$ is replaced by one of the code letters, $S$, $P$, $D$, $F$, etc., for $L=0,1,2,3$, etc. As we did in our discussion of the hydrogen molecule in {ref}`sec-identpart-8`, we use capital letters are used to represent the quantum numbers of the collective system (in this case, the whole atom), and reserve lower case letters for the quantum numbers of a single particle (in this case, an electron). For example, the state $2^3P$ is the state with $N=2$, $S=1$ and $L=1$. This is really a manifold of $(2L+1)(2S+1)=3\times 3 =9$ degenerate states.

(sec-helium-6)=

## Ionization Potentials

So far we have succeeding in labeling the energy levels of helium-like atoms by their good quantum numbers and determining their degeneracies, in the approximation given by {eq}`eq-helium-1`, without knowing much about the system apart from its symmetries. We now look at some experimental and other facts about such atoms.

First we present some ionization potentials. The ionization potential of an atom is the energy needed to remove one electron from the atom, assumed to be in its ground state, to infinity. If an atom has several electrons, there are successive ionization potentials, as more and more electrons are removed. The final state consists of a nucleus plus the electrons, all of which are at rest and at an infinite distance from one other.

It is a matter of convention in most areas of physics to decide where on the energy axis $E=0$ lies, since only energy differences are physically meaningful. (This is true as long as gravitational effects are neglected. But in general relativity, the mass corresponding to energy by $m=E/c^2$ has a gravitational effect, so the absolute measure of energy is physically significant.) But it is common in electrostatics to define the state of zero potential energy to be the one in which all charges are at an infinite separation from one another. This is what we have done with the potential energy in the Hamiltonian {eq}`eq-helium-1`. If the kinetic energies also vanish, then we have a state of zero total energy. With this convention for the state $E=0$, the sum of all the ionization potentials of the atom (with a minus sign) is the ground state energy of the atom. (Notice that we have not separated the protons in the nucleus or transported them to infinity. We are using a convention that is convenient in atomic physics, but perhaps not nuclear physics.)

:::{figure} images/helium-fig01.png
:label: fig-helium-1
:width: 80%

Important energies of helium obtained from ionization potentials. Energies are measured in atomic units.
:::

:::{figure} images/helium-fig02.png
:label: fig-helium-2
:width: 80%

Same as {ref}`fig-helium-1`, but for $H^-$. The energy scale is down by a factor of $1/4$ compared to helium.
:::


In the case of helium, the ionization potentials are

:::{math}
:label: eq-helium-20
\begin{aligned}
He &\to He^+ + e^- - 0.904~a.u., \\
He^+ &\to He^{++} + e^- - 2.0~a.u. \\

\end{aligned}
:::

The first ionization potential may be compared to that of hydrogen, which is $0.5~a.u.$ In fact, helium has the highest ionization potential of any neutral atom. See Fig.~\figr\hartfock.1. The second ionization potential is easy to understand, since the $He^+$ ion is a hydrogen-like atom, whose ground state energy is $-Z^2/2=-2~a.u.$ To calculate the first ionization potential, however, is a nontrivial problem. In the case of $H^-$, the ionization potentials are

:::{math}
:label: eq-helium-21
\begin{aligned}
H^- &\to H + e^- - 0.028~a.u., \\
H &\to H^+ + e^- - 0.5~a.u. \\

\end{aligned}
:::

In $H^-$ the extra electron is only weakly bound to the neutral H atom.

Figures~{ref}`fig-helium-1` and {ref}`fig-helium-2` illustrate the information obtained from the ionization potentials. The energy $E=0$ is the state of complete dissociation. The ground state energy of helium is $E=-2.904~a.u.$, while the state in which one electron has been removed to infinity has energy $E=-2~a.u.$ Once this electron has been removed, it may be given any positive kinetic energy, so there is a continuous spectrum above $E=-2~a.u.$ In $H^-$, the ground state energy is $E=-0.528~a.u.$ and the continuum begins at $E=-0.5~a.u.$, the ground state energy of a neutral hydrogen atom.

:::{figure} images/helium-fig03.png
:label: fig-helium-3
:width: 80%

Bound states of helium with quantum numbers. Energies are measured in atomic units. Notice the gap in the energy scale between the ground state and the excited states.
:::

(sec-helium-7)=

## The Bound States

From {ref}`fig-helium-1` it is clear that the bound states of helium must lie between $E_0=-2.904~a.u.$ and $E=-2~a.u.$ These bound states and their quantum numbers are displayed in {ref}`fig-helium-3` with an expanded energy scale. The energy levels in the figure are the eigenvalues of the Hamiltonian {eq}`eq-helium-1`, which are not exactly the same as the experimental values due to the neglect of small terms in that Hamiltonian. The difference, however, is too small to see on the scale of the diagram (in fact, at higher resolution, many of these levels will be seen to have a fine structure splitting).

The levels in {ref}`fig-helium-3` cannot be regarded as purely experimental data, even at a scale where fine structure is ignored and the Hamiltonian {eq}`eq-helium-1` is a good approximation, because spectroscopic data only gives differences between energy levels, not their absolute values. It takes some disentangling of the experimental data to produce energy levels. In addition, the levels in {ref}`fig-helium-3` have been assigned quantum numbers, which requires some theoretical input. In effect, we have skipped ahead to the answer (the spectrum of helium) in presenting {ref}`fig-helium-3`. This may be the best way to understand helium on a first pass.

In {ref}`fig-helium-3`, the para states (spatially symmetric, spin singlet) are on the left, and the ortho states (spatially antisymmetric, spin triplet) are on the right. Each vertical column contains the energy levels for a given value of $L$ and $S$, the good quantum numbers of the Hamiltonian {eq}`eq-helium-1`. Only columns out to $L=2$ ($D$-states) are shown in the figure, but in actual helium $L$ ranges from 0 to $\infty$. The levels in a given column are sequenced in ascending order by $N$, with certain conventions for the starting value of $N$. In each column there is an infinite number of levels that accumulate just below the continuum limit, much as in hydrogen. The energy levels in a given column are the eigenvalues of the Hamiltonian {eq}`eq-helium-1`, restricted to a simultaneous eigenspace of the operators $L^2$, $S^2$, $L_z$ and $S_z$ (it being understood that we are within the antisymmetric eigenspace of the exchange operator $E_{12}$).

Notice the following qualitative features of the energy level diagram for helium. First, the ground state is a singlet state ($1^1S$), which is considerably below the excited states (notice the gap in the energy scale). The excited states look roughly the same on the para and ortho sides, but there is no $1^3S$ state (no state on the ortho side that seems to correspond to the $1^1S$ state). Second, for a fixed value of $N$ and $S$, the energies are an increasing function of $L$ (the “staircase effect”) (at least this is true for $N=2$ and most other values of $N$). This is the same effect we saw in alkali atoms. Third, for fixed $N$ and $L$, the ortho states are lower in energy than the para states (thus, if a $1^3S$ state existed, we would expect it to be below the actual ground state $1^1S$). Later we will provide a theoretical explanation for some of these features.

In the case of $H^-$, the ground state is the only bound state, and it has the quantum numbers $1^1S$ (same as the ground state of helium).

(sec-helium-8)=

## Perturbation Analysis.  The Unperturbed System

We now turn to the problem of finding the spatial eigenfunctions of the Hamiltonian {eq}`eq-helium-1`, which is a purely orbital operator. Denoting such an eigenfunction by $\psi(\xvec_1,\xvec_2)$, we wish to solve

:::{math}
:label: eq-helium-22
H\psi(\xvec_1,\xvec_2) = E \psi(\xvec_1,\xvec_2).
:::

In addition, we wish these eigenfunctions to be even or odd under orbital exchange,

:::{math}
:label: eq-helium-23
E_{12}^orb \psi(\xvec_1,\xvec_2) = \pm \psi(\xvec_1,\xvec_2),
:::

where the $\pm 1$ is $e_{12}^orb$, the eigenvalue of $E_{12}^orb$. As explained above, $e_{12}^orb=+1$ are called para states, and $e_{12}^orb=-1$ are called ortho states. We know it is possible to construct simultaneous eigenfunctions of $H_0$ and $E_{12}^orb$ because they commute. Once we have found these eigenfunctions, it will be easy to multiply them by spin states (singlet or triplet) of the opposite exchange symmetry to obtain an overall eigenfunction of the Hamiltonian, including spin, that satisfies the symmetrization postulate. This part is relatively easy; the hard part will be solving {eq}`eq-helium-22` as a purely orbital problem.

An obvious strategy for finding the eigenfunctions of the Hamiltonian {eq}`eq-helium-1` is to use perturbation theory, in which the inter-electron Coulomb potential $1/r_{12}$ is taken as a perturbation. That is, we write $H=H_0+H_1$, where

:::{math}
:label: eq-helium-24a
\begin{aligned}
H_0 &= \Bigl({p_1^2\over 2} - {Z\over r_1}\Bigr) + \Bigl({p_2^2\over 2} - {Z\over r_2}\Bigr),
\end{aligned}
:::

:::{math}
:label: eq-helium-24b
\begin{aligned}
H_1 &= {1\over r_{12}}.
\end{aligned}
:::

We have grouped the terms in $H_0$ to emphasize that $H_0$ is the sum of two hydrogen-like Hamiltonians, one for each electron, moving in the field of a nuclear charge $Z$. This decomposition of $H$ into $H_0$ and $H_1$ is not very favorable for perturbation theory in the case of small $Z$, since the inter-electron potential is comparable to the electron-nucleus potentials. The comparison is especially unfavorable for $H^{-}$ (the case $Z=1$). It gets better for larger $Z$. We do the perturbation analysis anyway, since it is relatively straightforward and there are not many choices.

:::{figure} images/helium-fig04.png
:label: fig-helium-4
:width: 80%

Coordinates for the nucleus and two electrons in space.
:::

It is obvious from {ref}`fig-helium-4` what the effect of the perturbation $1/r_{12}$ is. When it is switched off, the two electrons no longer repel one another and settle in somewhat closer to the nucleus than they would otherwise. The wave functions for the two electrons can be thought of as two clouds that overlap in the neighborhood of the nucleus. Conversely, when we turn the perturbation on, the electron clouds expand somewhat so the electrons can get away from one another. They also tend to stay on opposite sides of the nucleus, for the same reason.

As usual in perturbation theory, we must understand the unperturbed system first, its eigenfunctions, degeneracies, and symmetries. Since $H_0$ is a sum of two hydrogen-like Hamiltonians, the (two-particle) eigenfunctions of $H_0$ are products of single particle eigenfunctions of the hydrogen-like Hamiltonians in the field of nuclear charge $Z$. We call these single-particle eigenfunctions *orbitals*. They are central force eigenfunctions, and since we are only concerned with the spatial part here, they are characterized by the usual central force quantum numbers $(n\ell m)$. Notice that we are using lower case letters for the quantum numbers of a single electron. The single particle hydrogen-like energy is $-Z^2/2n^2$. We denote these orbitals in ket language by $\ket{n\ell m}$. Then the two-particle eigenfunctions of $H_0$ are products of these, which we denote by

:::{math}
:label: eq-helium-25
\ket{n_1\ell_1m_1}^{(1)} \ket{n_2 \ell_2 m_2}^{(2)} = \ket{n_1 \ell_1 m_1 \, n_2 \ell_2 m_2},
:::

where the numbers in parentheses indicate which of the two electrons (1 or 2) is referred to, and where the right hand side is a shorthand notation for these states. These states depend on six quantum numbers. They are eigenfunctions of $H_0$,

:::{math}
:label: eq-helium-26
H_0 \ket{n_1 \ell_1 m_1 \, n_2 \ell_2 m_2} =E^{(0)}_{n_1n_2} \ket{n_1 \ell_1 m_1 \, n_2 \ell_2 m_2},
:::

where the $(0)$ on the energy indicates that it is the energy in zeroth order of perturbation theory. This zeroth order energy is a sum of the two hydrogen-like energies,

:::{math}
:label: eq-helium-27
E^{(0)}_{n_1n_2} = -{Z^2\over 2}\Bigl({1\over n_1^2} + {1\over n_2^2}\Bigr),
:::

and it depends only on the two principal quantum numbers $n_1$ and $n_2$.

The states {eq}`eq-helium-25` are eigenstates of $H_0$, but not in general of $E_{12}^orb$. However it is easy to construct eigenfunctions of $E_{12}^orb$ simply by symmetrizing or antisymmetrizing under exchange. There are two cases. In Case I, the two sets of single particle quantum numbers are equal (all of them), $(n_1 \ell_1 m_1) = (n_2 \ell_2 m_2) \equiv (n \ell m)$, and we write simply

:::{math}
:label: eq-helium-28
\ket{n \ell m \, n \ell m}
:::

for these states. In this case the states are already even under orbital exchange, so they are para states ($e_{12}^orb=+1$). There are no ortho states in Case I.

In Case II, one or more of the two sets of quantum numbers are different, $(n_1 \ell_1 m_1) \ne (n_2 \ell_2 m_2)$. In this case we can easily write down normalized eigenstates of $E_{12}^orb$,

:::{math}
:label: eq-helium-29
{1\over\sqrt{2}} \bigl( \ket{n_1 \ell_1 m_1 \, n_2 \ell_2 m_2} \pm \ket{n_2 \ell_2 m_2 \, n_1 \ell_1 m_1}\bigr),
:::

where the eigenvalue is $e_{12}^orb=\pm 1$. In this case we have both para and ortho states. The energy does not change when we carry out this symmetrization or antisymmetrization because both terms have the same energy. It is still given by {eq}`eq-helium-27`, and it does not depend on the choice of the $\pm$ sign. We now have a set of unperturbed energy eigenstates that are also eigenstates of $E_{12}^orb$.

:::{figure} images/helium-fig05.png
:label: fig-helium-5
:width: 80%

Unperturbed energy levels of helium, that is, levels of the Hamiltonian {eq}`eq-helium-24a`. The energy axis is vertical with energies measured in atomic units, and levels are labeled by principal quantum numbers $(n_1,n_2)$. The shaded area is the continuum.
:::

{ref}`fig-helium-5` shows the energy levels of $H_0$, with the para states on the left and ortho states on the right. The levels are labeled by their principal quantum numbers $(n_1,n_2)$.

Let us focus first on the levels below the shaded area in {ref}`fig-helium-5`, that is, the levels lying below the continuum threshold at $E=-2$ (all energies are in atomic units). These levels are called *singly excited* states because one of the hydrogen-like orbitals is in the ground state ($n_1=1$), while the other ($n_2$) takes on any value. The absolute ground state of $H_0$ is the $(1,1)$ state with $n_1=n_2=1$, at an energy of $-4$. The ground state is on the para side; there is no analogous state on the ortho side because this is Case~I, described in the paragraph surrounding {eq}`eq-helium-28`.

It is instructive to compare these levels with the exact bound states of helium, shown in {ref}`fig-helium-3`. One difference is that the levels in {ref}`fig-helium-3` are separated by the $L$ quantum number, while those in {ref}`fig-helium-5` are not. There is no point in separating the levels of {ref}`fig-helium-5` by the orbital angular momentum quantum numbers because the hydrogen-like energies do not depend on them. Apart from that, however, the two energy level diagrams are qualitatively similar. In particular, in both cases we have an infinite number of levels that accumulate at the continuum threshold $E=-2$.

Our analysis of the unperturbed system shows already why there is no $1^3S$ state in real helium: it is because it would have to be a perturbed version of an antisymmetrized ground state wave function, and the ground state wave function is spatially symmetric. On the other hand, the unperturbed spectrum shows no evidence of the staircase effect (hydrogen energies do not depend on $\ell$), and there is exact degeneracy between the ortho and para sides (when a level exists on both sides). That is, the unperturbed energies do not depend on the $\pm$ sign in {eq}`eq-helium-29`, which represents the spatial symmetry of the wave function. In addition, the unperturbed ground state is rather badly off in energy, $-4$ instead of the exact value of $-2.904$. In fact, all the unperturbed energies are too low; this is because the perturbation $H_1$ in {eq}`eq-helium-24b` is a positive operator, and can only raise energies. These differences between the unperturbed and exact spectra are clarified by perturbation theory.

(sec-helium-9)=

## The Doubly Excited States

{ref}`fig-helium-5` shows something else, the so-called *doubly excited* states in which both orbitals have principal quantum numbers $>1$. The doubly excited series with $n_1=2$ and $n_2\ge2$ is shown in the figure (twice, once on the para side and once on the ortho side). There are other series (not shown), with $n_1=3,4,\ldots$.

Insofar as the unperturbed Hamiltonian $H_0$ is concerned, these are *discrete states imbedded in the continuum*. That is, a state such as the $(2,2)$ state is a bound state of $H_0$ with a normalizable wave function, but it exists at an energy that lies in the continuous spectrum of another set of states, those with $n_1=1$ and the second electron with a positive energy. The wave functions of the continuum are products of the ground state wave function for the first electron times an unbound hydrogen-like solution for the second electron (subsequently symmetrized or antisymmetrized to obtain a definite exchange symmetry). These wave functions are not normalizable, as we expect in the continuous spectrum.

:::{figure} images/helium-fig06.png
:label: fig-helium-6
:width: 80%

Experimental cross for the reaction $\gamma+He\to He^+ +e^-$, as a function of photon energy. The peaks are resonances corresponding to the doubly excited states of helium. See R. P. Madden and K. Codling, *Astrophys. J.* **141**, 364(1965); and Robert D. Hudson and Lee J. Kieffer, *Atomic Data* **2**, 205(1971).
:::

What happens to these discrete, doubly excited states when the perturbation $1/r_{12}$ is turned on? It turns out that they do not remain discrete states, instead they become coupled to the continuum states of nearby energy, so the actual spectrum of helium above the continuum threshold $E=-2$ is strictly continuous. There are no exact bound states of helium above this threshold.

Nevertheless, the exact system does in effect know about the doubly excited states of the unperturbed system. Consider, for example, what happens when we direct a beam of photons of some energy at helium atoms in the ground state. When the photon energy exceeds the ionization potential of helium, 0.904~a.u., it may be absorbed by the atom and an electron ejected. The electron emerges with an energy that is the difference between the photon energy and the ionization potential. The experimental cross for this reaction is shown in {ref}`fig-helium-6`. One can see sharp peaks or enhancements in the cross , which correspond to the doubly excited states of helium. One can view this reaction as a two-step process, $\gamma + He \to He^* \to He^+ + e^-$, in which $He^*$ refers to a doubly excited state.

This effect can be understood classically. The solar system has eight major planets that move in approximately circular orbits that are stable on human time scales. Nevertheless, it is energetically possible for Jupiter to move somewhat closer to the sun, moving into a lower energy state, and eject all the other seven planets from the solar system. Will this ever happen? Modern chaos theory indicates that it probably will, if we wait long enough, assuming that the motion of the planets is governed by Newton's laws and no other effects (such as the death of the sun or an encounter with another star) intervene. Nevertheless, the solar system must be mostly stable for very long times, since the earth has apparently been in approximately the same orbit for about $4\times 10^9$ years.

Whether or not the ejection of the major planets is possible, it certainly happens that Jupiter and other planets have encounters with other (usually smaller) objects and cause them to be ejected. This effect is deliberately exploited by spacecraft that are to leave the solar system (such as the Mariner spacecraft).

In the case of the doubly excited states of helium, we can imagine the two electrons having a close encounter, which causes one to drop into the ground state and the other to be ejected. Unlike the case of the solar system, where Jupiter can move into any state of (continuous) lower energy, the first electron must drop into one of the discrete energy levels allowed to it. This is why the actual ground state of helium is stable: the two electrons are interacting strongly all the time, but there are no lower states for one of them to drop into. Apart from the effects of quantization, the classical picture gives an idea of the mechanism in helium. In particular, depending on the two sets of quantum numbers of the doubly excited state, it may take a long time for one electron to have a close encounter with the other. This is like the long-time stability of the solar system. In this case we have a state of the system that is nearly a stationary state, that is, an energy eigenstate. It is not exactly a stationary state, however, instead it is a *resonance*, a state with a finite life time. Resonances were examined in homework problem {ref}`prob-wkb-3` in a simple one-dimensional example.

Helium can be raised into a doubly excited state by many methods, not only absorption of photons but also collisions with electrons or other means. In all cases the doubly excited state $He^*$ exists for a period of time and then decays into the helium ion $He^+$ and a free electron. This is called the *Auger process*.

(sec-helium-10)=

## Perturbation Analysis of the Ground State

The ground state wave function of $H_0$ is of the form {eq}`eq-helium-28`, with $(n\ell m)=(100)$, that is, it is the state $\ket{100\,100}$. It is nondegenerate, so to compute the energy shift due to $H_1$ in first order perturbation theory we must compute\

:::{math}
:label: eq-helium-30
\Delta E_gnd = \matrixelement {100\,100}{H_1}{100\,100} =\int d^3\xvec_1\,d^3\xvec_2 \, {|\psi_{100}(\xvec_1)|^2 |\psi_{100}(\xvec_2)|^2 \over r_{12}},
:::

where we have written out the matrix element explicitly as an integral over the six-dimensional configuration space and where the wave functions are hydrogen-like orbitals in the field of nuclear charge $Z$.

The integral {eq}`eq-helium-30` has an interpretation in electrostatics. The squares of the wave functions seen in that integral are probability densities for the two electrons in physical space, which may be multiplied by the charges $-e$ ($=-1$ in atomic units) to obtain charge densities. Then the integral is the mutual energy of interaction of the two charge clouds. That is, if we imagine the two charge clouds translated rigidly, starting at an infinite separation, then the integral is the energy required to bring them into their final position where they overlap completely. Because the charge clouds repel one another, this energy is positive. It is precisely the energy shift $\Delta E$ in first order perturbation theory.

The hydrogen-like orbital for the ground state is

:::{math}
:label: eq-helium-31
\psi_{100}(\xvec)=\Bigl({Z^3\over\pi}\Bigr)^{1/2} \, e^{-Zr}.
:::

To do the integral {eq}`eq-helium-30` we expand the Coulomb denominator,

:::{math}
:label: eq-helium-32
{1\over r_{12}} = {1\over |\xvec_1 - \xvec_2|} = \sum_{\ell=0}^\infty {r_<^\ell \over r_>^{\ell+1}} P_\ell(\cos\gamma),
:::

where

:::{math}
:label: eq-helium-33
r_< = \min(r_1,r_2), \qquad r_>=\max(r_1,r_2),
:::

and

:::{math}
:label: eq-helium-34
\gamma = \angle(\xvec_1,\xvec_2).
:::

See \orbamsph.11. The angle $\gamma$ is illustrated in {ref}`fig-helium-4`. In addition we expand the Legendre polynomial in {eq}`eq-helium-32` in terms of spherical harmonics, using the addition theorem {eq}`eq-orbamsph-71`. For our present purposes we write this theorem as

:::{math}
:label: eq-helium-35
P_\ell(\cos\gamma) = {4\pi \over 2\ell+1} \sum_m Y_{\ell m}(\Omega_1) Y_{\ell m}^\cc(\Omega_2).
:::

Transforming the integral to spherical coordinates in both $\xvec_1$ and $\xvec_2$ and collecting all the pieces, we have

:::{math}
:label: eq-helium-36
\begin{aligned}
\Delta E_gnd & = {Z^6 \over \pi^2} \int_0^\infty r_1^2\,dr_1\int d\Omega_1 \int_0^\infty r_2^2\,dr_2\int d\Omega_2 \, e^{-2Z(r_1+r_2)} \\
&\qquad \times \sum_{\ell=0}^\infty {r_<^\ell \over r_>^{\ell+1}} {4\pi \over 2\ell+1} \sum_m Y_{\ell m}(\Omega_1) Y_{\ell m}^\cc(\Omega_2) \\

\end{aligned}
:::

We do the $\Omega_2$ integral first, using the orthonormality of the $Y_{\ell m}$'s and the fact that $Y_{00}=1/\sqrt{4\pi}$ is a constant,

:::{math}
:label: eq-helium-37
\int d\Omega_2\, Y_{\ell m}^\cc(\Omega_2) = \sqrt{4\pi} \int d\Omega_2 \, Y_{\ell m}^\cc(\Omega_2) Y_{00}(\Omega_2) = \sqrt{4\pi} \, \delta_{\ell 0} \, \delta_{m0}.
:::

The Kronecker deltas cause both sums to be replaced by the single term $\ell=m=0$. Then the $\Omega_1$ integration is easy,

:::{math}
:label: eq-helium-38
\int d\Omega_1\, Y_{00}(\Omega_1) = \sqrt{4\pi}.
:::

This leaves us with

:::{math}
:label: eq-helium-39
\Delta E_gnd = 16 Z^6  \int_0^\infty r_1^2\,dr_1 S(r_1),
:::

where $S(r_1)$ is the second integral,

:::{math}
:label: eq-helium-40
S(r_1) = \int_0^\infty r_2^2\,dr_2\, {e^{-2Z(r_1+r_2)} \over r_>} = \int_0^{r_1} r_2^2\,dr_2\, {e^{-2Z(r_1+r_2)} \over r_1} + \int_{r_1}^\infty r_2^2\,dr_2\, {e^{-2Z(r_1+r_2)} \over r_2}.
:::

These integrals are elementary and after some algebra we find

:::{math}
:label: eq-helium-41
\Delta E_gnd = {5\over 8}Z,
:::

or

:::{math}
:label: eq-helium-42
E^{(1)}_gnd = -Z^2 + {5\over 8}Z,
:::

where the $(1)$ means the energy correct to first order of perturbation theory. Evidently perturbation theory is developing a series in inverse powers of $Z$.

:::{list-table} Comparison of ground state energies at zeroth and first order of perturbation theory with the exact ground state energies, for ${H}^-$ and ${He}$.
:label: tbl-helium-3
:header-rows: 2

* - Atom
  - $Z$
  - $E_{gnd}^{(0)}$
  - $E_{gnd}^{(1)}$
  - $E_{gnd}^{exact}$
* - ${H}^-$
  - $1$
  - $-1$
  - $-0.375$
  - $-0.528$
* - ${He}$
  - $2$
  - $-4$
  - $-2.75$
  - $-2.904$

:::
{ref}`tbl-helium-3` shows a numerical comparison of the ground state energies of helium and $H^-$, as estimated from the unperturbed system and from first order perturbation theory. It will be seen that the first order correction does close the gap between the calculated energy and the true energy, but it overshoots the mark and ends up being too high.

If we did not know the exact ground state energy, what would we make of this estimate from first order perturbation theory? For example, do we have any idea how far away it might be from the true ground state energy, or whether it is even too high or too low?

We know that the variational principle always gives us an upper bound to the ground state energy. It turns out that the estimate from first order perturbation theory can be interpreted as a variational estimate, and that it is, therefore, an upper bound. The trial wave function that makes this identification is the unperturbed eigenfunction, which in this case is nondegenerate. See Prob. {ref}`prob-variational-3`. But perturbation theory alone does not give a lower bound, so we are somewhat in the dark as to how far away our estimate is from the true ground state. In practice we can get information about this by applying variational estimates with more and more sophisticated trial wave functions, and observing the numerical convergence. This is not rigorous, but often it works well enough.

In this example we do have a lower bound, namely, the ground state of $H_0$, which is $-4$. This is not very close to the true ground state, nor can we improve the estimate as we can with the variational method, by choosing better trial wave functions. There are methods of getting lower bounds that can be improved, which we do not consider here.

Even without knowing how far away we are from the true ground state, however, an upper bound can be useful for some purposes. Consider, for example, the $H^-$ ion. It is not obvious on physical grounds that this exists as a bound state. If it were not known experimentally that it does exist, how could we prove it theoretically? One way is to find a trial wave function that gives an upper bound to the ground state energy that lies below the continuum threshold, which is $-0.5\,a.u.$ Unfortunately, our estimate from first order perturbation theory, $-0.375\,a.u.$, lies above this threshold, so we do not have a theoretical proof of the existence of $H^-$. But we should keep this example in mind later when we apply the variational method to helium-like atoms.

(sec-helium-11)=

## Perturbation Analysis of the Excited States

We now apply perturbation theory to the excited states of helium, concentrating on the bound states. We need consider only the singly excited states, since, as noted, the doubly excited states are already above the continuum threshold, and the perturbation can only raise the energies. We will set $(n_1,n_2)=(1,n)$ for the singly excited states, so the unperturbed energy is

:::{math}
:label: eq-helium-43
E^{(0)}_{1n} = -{Z^2\over 2} \Bigl(1+{1\over n^2}\Bigr).
:::

We will be interested in the case $n\ge2$. We write the unperturbed energy eigenstates as

:::{math}
:label: eq-helium-44
\ket{NLM\pm} = {1\over\sqrt{2}} (\ket{100\,n\ell m} \pm \ket{n\ell m\,100}),
:::

where we use the notation {eq}`eq-helium-25` for the products of hydrogen-like orbitals. This is case~II, shown in {eq}`eq-helium-29`. The $\pm$ sign on either side is the eigenvalue of $E_{12}^orb$, the orbital exchange operator. As for the notation $NLM$, we are using capital letters for the quantum numbers of all the electrons in the atom, and lower case letters $n\ell m$ for the quantum numbers of a single electron. For example, $L$ is the quantum number of the operator $L^2= (\Lvec_1 +\Lvec_2)^2$. But for singly excited states the entire angular momentum comes from the second electron, since the first electron is in the ground state for which $\ell=0$. Thus in {eq}`eq-helium-44` it is understood that $L=\ell$, $M=m$ and $N=n$. For example, the state with $N=2$, $L=1$ and $e_{12}^orb=-1$ is the unperturbed version of the $2^3P$ state in helium. Whether we write $n\ell m$ or $NLM$ depends on which aspect of the problem we wish to emphasize. In any case, notice that the notation $\ket{NLM\pm}$ contains quantum numbers of the orbital observables in {ref}`tbl-helium-2` that commute with the entire Hamiltonian $H_0+H_1$. That is, we are using a symmetry adapted basis for studying the perturbation.

The unperturbed eigenstates {eq}`eq-helium-44` are degenerate, since the unperturbed energy depends only on the quantum number $N=n$, and we should think about degenerate perturbation theory. But in the basis $\ket{NLM\pm}$ we need not diagonalize any matrices, since $H_1$ commutes with all the operators of the complete set of commuting observables that specify the unperturbed basis vectors inside a degenerate eigenspace of the unperturbed Hamiltonian, that is, the operators $L^2$, $L_z$ and $E_{12}^orb$. Therefore the energy shifts are given by the diagonal matrix elements,

:::{math}
:label: eq-helium-45
\Delta E_{NL\pm} = \matrixelement{NLM\pm}{H_1}{NLM\pm}.
:::

The energy shifts do not depend on $M$ because of the Wigner-Eckart theorem and the fact that $H_1$ is a scalar operator, but they do depend on all the other quantum numbers $NL\pm$, as we shall see. Substituting {eq}`eq-helium-44` into {eq}`eq-helium-45` we have

:::{math}
:label: eq-helium-46
\begin{aligned}
\Delta E_{NL\pm} = {1\over 2}[ &(\matrixelement{100\,n\ell m}{H_1}{100\,n\ell m} + \matrixelement{n\ell m\,100}{H_1}{n\ell m\,100}) \\
\pm& (\matrixelement{100\,n\ell m}{H_1}{n\ell m\,100}+ \matrixelement{n\ell m\,100}{H_1}{100\,n\ell m})]. \\

\end{aligned}
:::

But the pairs of matrix elements inside the round parentheses are equal, as we see by writing them out as spatial integrals and swapping $\xvec_1$ and $\xvec_2$, so we have

:::{math}
:label: eq-helium-47
\Delta E_{NL\pm} = J_{n\ell} \pm K_{n\ell},
:::

where

:::{math}
:label: eq-helium-48
\begin{aligned}
J_{n\ell} &= \matrixelement{100\,n\ell m}{{1\over r_{12}}} {100\,n\ell m},
\end{aligned}
:::

:::{math}
:label: eq-helium-49
\begin{aligned}
K_{n\ell} &= \matrixelement{100\,n\ell m}{{1\over r_{12}}} {n\ell m\,100}.
\end{aligned}
:::

The integrals $J_{n\ell}$ and $K_{n\ell}$ are called the *direct* and *exchange* integrals, respectively. As for the direct integrals, if we write them out explicitly as a integrals over the configuration space of the two electrons, using the hydrogen-like orbitals $\psi_{n\ell m}(\xvec)$, we have

:::{math}
:label: eq-helium-50
J_{n\ell} = \int d^3\xvec_1 \, d^3\xvec_2 \, {|\psi_{100}(\xvec_1)|^2 |\psi_{n\ell m}(\xvec_2)|^2 \over |\xvec_1-\xvec_2|}.
:::

This has the interpretation as the mutual electrostatic energy of the two electron clouds associated with orbitals $(100)$ and $(n\ell m)$, exactly as in the integral {eq}`eq-helium-30`, which applies to the ground state of helium. In fact, that integral is a direct integral itself, with $(n\ell m)=(100)$. The direct integrals $J_{nl}$ are obviously real and positive.

As for the exchange integrals, they are

:::{math}
:label: eq-helium-51
K_{n\ell} = \int d^3\xvec_1 \, d^3\xvec_2 \, {\psi_{100}^\cc(\xvec_1)\psi_{n\ell m}^\cc(\xvec_2) \psi_{n\ell m}(\xvec_1)\psi_{100}(\xvec_2) \over |\xvec_1-\xvec_2|}.
:::

These are also real, as is easily shown by swapping the variables of integration $\xvec_1$ and $\xvec_2$. It can also be shown that the exchange integrals are positive. We will omit the proof of this fact since it is not particularly illuminating, but we note that it is plausible that $K_{n\ell}$ should be positive, since the denominator makes the integrand large in regions of the six-dimensional configuration space where $\xvec_1\approx\xvec_2$. But in such regions, the numerator is approximately

:::{math}
:label: eq-helium-52
|\psi_{100}(\xvec)|^2 |\psi_{n\ell m}(\xvec)|^2,
:::

where $\xvec\approx\xvec_1\approx\xvec_2$. That is, the numerator is positive in such regions. (The rigorous proof that $K_{nl}>0$ is given in an appendix to Slater's books on atomic physics.)

The fact that $K_{n\ell}$ is positive has a simple physical interpretation, however. Since the energy shifts {eq}`eq-helium-47` are $J_{n\ell} \pm K_{n\ell}$, it means that the ortho states (with the $-$ sign) are lower in energy than the para states (with the $+$ sign). This is one of the qualitative features of the exact spectrum of helium noted in \secrhelium-7. One can understand why this is so as follows. Let $\Psi(\xvec_1,\xvec_2)$ be the wave function of the two electrons. For ortho states, $\Psi(\xvec_1,\xvec_2) = -\Psi(\xvec_2 ,\xvec_1)$. But when $\xvec_1=\xvec_2$, this means $\Psi=0$. For ortho states, the two-electron wave function vanishes when the two electrons are on top of each other, that is, the wave function has a node at $\xvec_1=\xvec_2$. For para states, on the other hand, the wave function has an anti-node, that is, it is a maximum at $\xvec_1=\xvec_2$. (In using the words “node” and “anti-node” we are applying one-dimensional terminology to the six-dimensional problem at hand, but the terminology does convey the right idea.) But since the electrons repel one another and do not like to be on top of one another, the electrostatic energy of interaction is larger in para states than in ortho states.

:::{figure} images/helium-fig07.png
:label: fig-helium-7
:width: 80%

Effect of the perturbation $1/r_{12}$ on the $N=2$ levels of helium. Diagram is schematic and not to scale, but it does show the correct ordering of the $N=2$ levels in real helium, that is (from lowest to highest), $2^3S$, $2^1S$, $2^3P$, $2^1P$.
:::

A schematic illustration of the effects of the perturbation on the $N=2$ levels of helium is given in {ref}`fig-helium-7`. The unperturbed levels are labeled with the quantum numbers of the hydrogen-like orbitals that enter into the unperturbed wave functions, that is, $1s2s$ and $1s2p$. Such a list of central force quantum numbers for individual electrons is called an *electron configuration* of the atomic state. In the same notation, the ground state is given the configuration $1s^2$ (both electrons are in the $1s$ orbital). Notice, however, that the electron configuration applies rigorously only to the unperturbed wave function. For example, although we say that the electron configuration in the ground state of helium is $1s^2$, or that that of the $N=2$ levels is $1s2s$ or $1s2p$, nevertheless the exact wave functions are not products of single electron orbitals (in the case of the ground state) or symmetrized or antisymmetrized products (in the case of the excited states). This is because the perturbation changes the wave functions.

A qualitative feature shown in {ref}`fig-helium-7` is the fact that the direct integrals $J_{n\ell}$ are an increasing function of $\ell$. This is responsible for the “staircase effect,” that is, the fact that the $P$ levels are higher than the $S$ levels. A similar effect can be seen in the alkalis (see Fig.~\figr\hydrogen.3 for the case of sodium), and the explanation is the same: as the angular momentum of one electron is increased, it moves further away from the nucleus, and the nuclear charge is more effectively screened by the other electron(s) (one, in the case of helium; the core electrons, in the case of the alkalis).

We see that all the qualitative features of the excited states of real helium, discussed in \secrhelium-7, are explained by perturbation theory. These are the absence of any $1^3S$ state; the fact that the ortho states are lower in energy than the singlet states; and the fact that the energy is an increasing function of $L$ (the staircase effect). From a quantitative standpoint, however, perturbation theory, as we have outlined it, is less satisfactory, which is why we do not attempt to evaluate the direct and exchange integrals explicitly. The variational method does better from a quantitative standpoint.

(sec-helium-12)=

## Variational Treatment of Ground State

The unperturbed ground state was represented in ket language in \secrhelium-10 as $\ket{100\,100}$. In wave function language it is the product of two hydrogen-like ground state orbitals (see {eq}`eq-helium-31`,

:::{math}
:label: eq-helium-53
\Psi_{1s^2}(\xvec_1,\xvec_2) = {Z^3\over\pi}\, e^{-Z(r_1+r_2)}.
:::

where the subscript $1s^2$ refers to the electron configuration of the ground state. The unperturbed energy ($-4$) is rather badly off. The reason was explained in \secrhelium-8: the two electrons repel one another, and the true charge cloud stays somewhat further away from the nucleus than indicated by {eq}`eq-helium-53`.

Equivalently, we can say that each electron partially screens the nucleus from the other, so that each electron sees an effective nuclear charge $Z_e$ that is somewhat less than the true nuclear charge $Z$. Since only one electron is doing the screening and the screening is only partial, we would expect any reasonable measure of $Z_e$ to lie between $Z-1$ and $Z$. This suggests that we use as a trial wave function the product of two hydrogen-like ground-state orbitals in a Coulomb field with effective charge $Z_e$, that is,

:::{math}
:label: eq-helium-54
\Psi_trial(\xvec_1,\xvec_2) = {Z_e^3 \over \pi} e^{-Z_e(r_1+r_2)},
:::

where we treat $Z_e$ as a variational parameter. In accordance with the variational method we will minimize the expectation value of the energy with respect to $Z_e$, and thereby determine $Z_e$. This is an example of how we can use physical reasoning to choose a trial wave function. We will write the wave function {eq}`eq-helium-54` in ket language as $\ket{100\,100(Z_e)}$.

The trial wave function {eq}`eq-helium-54` is already normalized, so we do not need any Lagrange multipliers (see {ref}`sec-variational-5`). We merely need to calculate the expectation value of $H$. To do this we write $H$ in the form,

:::{math}
:label: eq-helium-55
H=\Bigl({p_1^2\over 2} -{Z_e\over r_1}\Bigr) +\Bigl({p_2^2\over 2} -{Z_e\over r_2}\Bigr) +(Z_e-Z)\Bigl({1\over r_1} + {1\over r_2}\Bigr) + {1\over r_{12}},
:::

where we have added and subtracted terms to cause the appearance of two single-particle, hydrogen-like Hamiltonians with nuclear charge $Z_e$.

The expectation value of the first major term in {eq}`eq-helium-55` with respect to the trial wave function is

:::{math}
\begin{aligned}
&\matrixelement{100\,100(Z_e)} {\Bigl({p_1^2\over 2}-{Z_e\over r_1}\Bigr)} {100\,100(Z_e)}
\end{aligned}
:::

:::{math}
:label: eq-helium-56
\begin{aligned}
&\; =\bra{100(Z_e)}^{(1)}\bra{100(Z_e)}^{(2)} \Bigl({p_1^2\over 2}-{Z_e\over r_1}\Bigr) \ket{100(Z_e)}^{(1)}\ket{100(Z_e)}^{(2)},
\end{aligned}
:::

where we have factored the two-particle wave function into a product of two single-particle orbitals, and where the numbers in parentheses indicate which particle is referred to. But the operator in the middle depends only on the coordinates of particle 1, so the bra and the ket referring to particle 2 just combine to give their normalization, which is 1. Thus the two-particle matrix element {eq}`eq-helium-56` reduces to a single-particle matrix element,

:::{math}
:label: eq-helium-57
\matrixelement{100(Z_e)} {\Bigl({p^2\over2}-{Z_e\over r}\Bigr)} {100(Z_e)} =-{Z_e^2\over 2},
:::

where we drop the $(1)$ superscripts and $1$ subscripts, since the coordinates $\xvec_1$ of the remaining particle are just dummy variables of integration. This is the expectation value of a hydrogen-like Hamiltonian with effective charge $Z_e$ with respect to its own ground state, which is just the ground state energy with the same effective charge, as shown. The expectation value of the second major term in {eq}`eq-helium-55` proceeds similarly, and gives the same answer, doubling the contribution {eq}`eq-helium-57`.

As for the third major term in {eq}`eq-helium-55`, we will need the expectation value of $1/r_1$ with respect to the trial wave function. This is

:::{math}
\begin{aligned}
&\matrixelement{100\,100(Z_e)}{{1\over r_1}}{100\,100(Z_e)} =\bra{100(Z_e)}^{(1)}\bra{100(Z_e)}^{(2)} {1\over r_1} \ket{100(Z_e)}^{(1)}\ket{100(Z_e)}^{(2)}
\end{aligned}
:::

:::{math}
:label: eq-helium-58
\begin{aligned}
&\;=\matrixelement{100(Z_e)}{1\over r}{100(Z_e)} =Z_e,
\end{aligned}
:::

where we proceed as in the previous paragraph to reduce the two-particle matrix element to a one-particle matrix element, and where we use {eq}`eq-finestruc-39` for the final expectation value (with $Z$ replaced by $Z_e$ and $n=1$). The expectation value of $1/r_2$ proceeds similarly, and doubles the answer. Overall, the expectation value of the third major term in {eq}`eq-helium-55` is

:::{math}
:label: eq-helium-59
2(Z_e-Z)Z_e = 2Z_e^2 - 2ZZ_e.
:::

As for the final term in {eq}`eq-helium-55`, the inter-electron potential $1/r_{12}$, this depends on the coordinates of both particles and so its expectation value cannot be reduced to a single-particle matrix element as in the case of the other terms. However, the expectation value in question is the same one we calculated earlier in our perturbation analysis of the ground state (in \secrhelium-10) except for the replacement of $Z$ by $Z_e$. Therefore the answer follows immediately from {eq}`eq-helium-41`,

:::{math}
:label: eq-helium-60
\matrixelement{100\,100(Z_e)}{{1\over r_{12}}} {100\;100(Z_e)} = {5\over 8} Z_e.
:::

Adding up the pieces, we have

:::{math}
:label: eq-helium-61
\matrixelement{100\;100(Z_e)}{H} {100\;100(Z_e)} = Z_e^2 -2ZZ_e + {5\over 8}Z_e \equiv F(Z_e).
:::

We wish to minimize $F(Z_e)$ with respect to $Z_e$. We have

:::{math}
:label: eq-helium-62
\dod{F}{Z_e} = 2(Z_e-Z) + {5\over 8},
:::

which has the root

:::{math}
:label: eq-helium-63
Z_e = Z-{5\over 16}.
:::

We see that by the variational criterion of the best trial wave function, each electron screens $5/16$ of a nuclear charge from the other electron. The variational estimate for the ground state energy is $F(Z_e)$ where $Z_e$ is given by {eq}`eq-helium-63`. This is

:::{math}
:label: eq-helium-64
E_gnd^var = -Z^2 + {5\over 8}Z - {25\over 256}.
:::

The first two terms agree with the results of first order perturbation theory, {eq}`eq-helium-42`, but with correction which is negative. Since the variational result is an upper limit to the ground state energy, we see that

:::{math}
:label: eq-helium-65
E_gnd^exact < E_gnd^var < E_gnd^{(1)},
:::

where the $(1)$ superscript refers to the results of first order perturbation theory, as in {eq}`eq-helium-42`.

:::{list-table} Comparision of ground state energies of ${He}$ and ${H}^{-}$, calculated by both perturbation theory and the variational method, with the exact ground state energies.
:label: tbl-helium-4
:header-rows: 2

* - Atom
  - $Z$
  - $Z_e$
  - $E_{gnd}^{(0)}$
  - $E_{gnd}^{(1)}$
  - $E_{gnd}^{var}$
  - $E_{gnd}^{exact}$
* - ${H}^-$
  - $1$
  - $\frac{11}{16}$
  - $-1$
  - $-0.375$
  - $-0.473$
  - $-0.528$
* - ${He}$
  - $2$
  - $1\frac{11}{16}$
  - $-4$
  - $-2.75$
  - $-2.848$
  - $-2.904$

:::
{ref}`tbl-helium-4` summarizes the results of both perturbation theory and the variational method for the ground states of $He$ and $H^-$. In the case of helium we see that the variational method has closed about two thirds of the distance between the results of first order perturbation theory and the exact ground state energy. In the case of $H^-$ the variational result is disappointing, in that the estimate of the ground state energy ($-0.473$) is still above the continuum threshold of $-0.5$. If we did not know that $H^-$ exists as a bound state, we would not yet have a theoretical proof that it does. To give that, it would be necessary to find a more complicated trial wave function (with more or different parameters), such that the expectation value of the energy would be less than $-0.5$. From a physical standpoint, it is clear what is wrong with our trial wave function {eq}`eq-helium-54`: it does not incorporate the tendency of the electrons to stay on opposite sides of the nucleus, that is, it does not incorporate any correlation in the positions of the two electrons. With a trial wave function that does take this effect into account, it is possible to obtain a variational estimate that is less than $-0.5$, thereby providing a theoretical proof of the existence of $H^-$ as a bound state.

The variational method has been applied to the ground state of helium and helium-like atoms with much more sophisticated and complicated trial wave functions than we have considered here. The original calculations along these lines were carried out by Hylleraas, and with modern computers it is possible to go much further. By such means the ground state energy of the Hamiltonian {eq}`eq-helium-1` for $Z=2$ and other values of $Z$ has been obtained to many significant figures. The accuracy obtained is far beyond that needed to show the difference between the ground state energy of the Hamiltonian {eq}`eq-helium-1` and the experimental ground state energy of helium, which are not equal because the Hamiltonian {eq}`eq-helium-1` omits a number of small effects, as discussed in \secrhelium-2.

\problems

(prob-helium-1)=

**Problem \prbdhelium-1..** 

\problempart{(a)}How would this diagram be different if the electron were a spin~0 particle? If it were a spin~$\frac{3}{2}$ particle? You do not need to be quantitative, but if some levels go up or down, say which ones and which way. If some levels appear or disappear, say which ones. What are the degeneracies of the levels in actual helium? What would they be if the electron were a spin-0 particle?

\problempart{(b)} The electric dipole operator for a multielectron atom is defined by {eq}`eq-stark-12`, where the charges are the electrons (with $q=-e)$. Electric dipole transitions between two states are governed by the matrix element of the electric dipole operator between the states in question. Explain why there are no electric dipole transitions between ortho and para eigenstates of the Hamiltonian {eq}`eq-helium-1`.

**Remark:** The eigenstates of the Hamiltonian {eq}`eq-helium-1` are not exactly the eigenstates of real helium because of the neglect of small terms, notably, the fine structure terms. When these are included, it turns out that electric dipole transitions are allowed between ortho and para states, but the amplitude is small and the lines are very weak. For this reason, it was thought at one time on spectroscopic grounds that parahelium and orthohelium were two different species of helium. The weak spectral lines connecting the ortho and para states are called “intercombination lines.”

(prob-helium-2)=

**Problem \prbdhelium-2..** 

:::{math}
:label: eq-helium-66
-{1\over 2} {\partial^2 \psi \over \partial x^2} -Z \delta(x) \psi = E\psi.
:::

[Units such that $m=\hbar=1$, and the Coulomb potential is replaced by $-Z\delta(x)$].

\problempart{(a)} Find the ground state energy and wave function $\psi_0(x)$, and verify that

:::{math}
:label: eq-helium-67
\xpecval{T} = -E = - {1\over2} \xpecval{V}.
:::

\problempart{(b)} Now consider the one-dimensional “helium” atom which obeys

:::{math}
:label: eq-helium-68
H\psi(x_1,x_2) = -{1\over 2} {\partial^2 \psi \over \partial x_1^2} - {1\over 2} {\partial^2 \psi \over \partial x_2^2} - Z\delta(x_1) \psi - Z\delta(x_2)\psi +\delta(x_1-x_2)\psi = E\psi,
:::

where $x_1$, $x_2$ are the coordinates of the two “electrons” on the $x$-axis. First treat $\delta(x_1-x_2)$ as a perturbation and find the ground state energy to first order. Compare to 3-dimensional helium.

\problempart{(c)} Now employ the variational method with a trial wave function analogous to that used in class for the ground state of 3-dimensional helium. Find the best value of $\xpecval{H}$ and compare to 3-dimensional helium.

\problempart{(d)} For one-dimensional “helium,” take a trial wave function of the form

:::{math}
:label: eq-helium-69
\psi(x_1,x_2) = u(x_1)u(x_2),
:::

where $u(x)$ is the variational parameter (that is, the whole function, as in Hartree theory). Assume $u(x)$ is real; there is no loss of generality in this. Find an equation for $u(x)$. It will be a kind of Hartree equation, and it will contain a pseudo-energy eigenvalue, call it $\epsilon$. Define $\epsilon$ so that the equation looks like

:::{math}
:label: eq-helium-70
-{1\over 2} u''(x) + \ldots = \epsilon u(x),
:::

where the ellipsis indicates omitted terms.

\problempart{(e)} The desired solution must be normalizable (in fact, we demand that it be normalized), so we must have

:::{math}
:label: eq-helium-71
\lim_{x\to\pm\infty} u(x) = 0.
:::

Show that this can only be satisfied if $\epsilon<0$. Hint: To solve the equation, make the change of notation, $u\to x$, $x\to t$, and interpret it as a one-dimensional problem in classical mechanics.

\problempart{(f)} Find the normalized solution $u(x)$ and the pseudo-eigenvalue $\epsilon$.

\problempart{(g)} Find the variational estimate of the ground state energy of one-dimensional “helium”. Hint: Note that

:::{math}
:label: eq-helium-72
\xpecval{H}= 2\epsilon - \xpecval{\delta(x_1-x_2)}.
:::

Does your new estimate improve on the results of part (a)? Would you expect it to do so?

(prob-helium-3)=

**Problem \prbdhelium-3..** 

\problempart{(a)} The exchange integral $K_{n\ell}$ defined in {eq}`eq-helium-51` depends on two hydrogen-like orbitals. It is easily generalized to any two single-particle orbitals (recall that “orbital” means a single-particle wave function). Show that if the two orbitals have no spatial overlap, then the exchange integral vanishes. Then use your knowledge of hydrogen-like orbitals to explain the dependence of the exchange integral on $n$ for fixed $\ell$, and on $\ell$ for fixed $n$.

\problempart{(b)} Go to {\tt http://physics.nist.gov/PhysRefData/ASD/levels\_form.html} and check your predictions using the experimental data on the first several excited states of helium. Enter “He I” for the atom (this is neutral helium). You will see that some of the levels have a fine structure, which we did not discuss in detail in class. This should not prevent you from checking your predictions.
