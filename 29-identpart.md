---
title: "29. Identical Particles"
---
(ch-identpart)=

# 29. Identical Particles

(sec-identpart-1)=

## Introduction

Understanding the quantum mechanics of systems of identical particles requires a new postulate, the *symmetrization postulate*, in addition to the measurement postulates of quantum mechanics considered earlier in the course. The symmetrization postulate has far reaching consequences for the physics of multiparticle systems, and is basic to the understanding of the physical properties of almost all kinds of aggregates of matter. This applies especially to the statistical and thermodynamic properties of matter. In these notes we introduce the basic concepts, using diatomic molecules as an example.

(sec-identpart-2)=

## The Model

Let us consider a system of two identical particles, interacting by means of a central force potential. The Hamiltonian is

:::{math}
:label: eq-identpart-1
H = {\pvec_1^2 \over 2m} + {\pvec_2^2 \over 2m} + V(|\xvec_2 -\xvec_1|).
:::

The masses are equal in the two kinetic energy terms because the particles are identical. This Hamiltonian describes quite a few physical situations, for example, the scattering of two protons at low velocities $(v\ll c)$ where the forces are predominantly electrostatic. Low velocity proton-proton scattering is important in applications, for example, in the study of thermonuclear reaction rates in the interior of stars.

A system consisting of two protons or two electrons cannot have bound states because the forces are repulsive. To deal with systems of identical particles that do possess bound states we will consider diatomic molecules.

Diatomic molecules such as $H_2$, $N_2$ or $Cl_2$ in which the two nuclear species are identical are called *homonuclear* diatomics. Diatomics such as HCl and CO are called *heteronuclear* diatomics. If the two atoms are chemically identical but the nuclei are different isotopes, for example, in the hydrogen molecule in which one atom is ordinary hydrogen and the other is deuterium (the molecule HD), then the molecule is considered heteronuclear.

We will use the Hamiltonian {eq}`eq-identpart-1` for homonuclear diatomic molecules. Then the “particles” whose positions and momenta appear in that Hamiltonian are actually atoms, which are composite particles. Composite particles are those composed of other particles; in this case, an atom is composed of electrons and a nucleus. Nuclei are also composite particles, being composed of protons and neutrons, and protons and neutrons are themselves composite, being composed of quarks. As far as anyone knows, electrons and quarks and some other particles are really fundamental, and not composed of smaller constituents.

There is the question of what justifies the treatment of a composite particle like an atom as a single particle, as in the Hamiltonian {eq}`eq-identpart-1`. In reality, the hydrogen molecule $H_2$ consists of two protons and two electrons, that is, four particles, while the molecule $N_2$ consists of two nuclei and 14 electrons, and yet the Hamiltonian {eq}`eq-identpart-1` only involves the coordinates and momenta of two particles, the atoms. The short answer is the Born-Oppenheimer approximation, which justifies such a treatment under certain circumstances. One condition on the validity of the Born-Oppenheimer approximation is that the velocities of the nuclei should be small compared to the velocities of the electrons. We touched on the Born-Oppenheimer approximation in {ref}`ch-cenforce`, and will take it up in somewhat greater depth later, in {ref}`ch-adiab`. Problem {ref}`prob-adiab-2` shows how a composite particle acquires a wave function, in a simple but physically realistic example.

In the Born-Oppenheimer approximation, the atoms are seen as particles whose positions and masses are the same as those of the nuclei, but which interact with one another by means of an effective potential $V$. The dynamics of the electrons does not appear explicitly in this description, rather it is absorbed into the potential energy function $V$. This function contains the electrostatic energy of interaction of the two nuclei (which of course is repulsive), plus the electrostatic energy of the electrons, both among themselves and with the nuclei, plus the kinetic energy of the electrons. The electron clouds adjust as the nuclei move about (the charge clouds polarize one another), and the energy required to bring about this polarization is contained in the potential $V$. As described in {ref}`ch-cenforce`, the potential $V(r)$ for diatomic molecules is strongly repulsive at short distances, it has an attractive well at intermediate distances with a minimum at some radius $r_0$, and it goes to zero for large $r$. The detailed form of this function depends on the nature of the two atoms in the diatomic, but these qualitative features are the same for essentially all diatomics. See Fig.~\figr\cenforce.8.

There is also the question of the spin of the atoms. If the electronic state is ${}^1\Sigma$, in the standard notation for diatomic molecules (the notation specifies orbital and spin quantum numbers for the electrons), then it turns out that the spin and orbital angular momentum of the electrons can be ignored, and the atoms behave as if they were particles with the same spin as the nuclei. In fact, the ground electronic state of most diatomic molecules (both hetero- and homonuclear) is ${}^1\Sigma$. The main exception is the molecule $O_2$, which has the unusual electronic ground state ${}^3\Sigma$. For simplicity in the following discussion of diatomic molecules we will exclude the case of oxygen.

In summary, for the diatomics we shall consider, the two atoms can be treated as particles with the same mass and spin as the nucleus, but interacting through the effective Born-Oppenheimer potential $V$ in {eq}`eq-identpart-1`.

(sec-identpart-3)=

## Exchange Symmetry

The Hamiltonian {eq}`eq-identpart-1` possesses a new type of symmetry that we have not seen before in this course, namely, *exchange*. For our two-particle system there is an operator $E_{12}$ that exchanges particles 1 and 2. It will be defined precisely in a moment, but it is easy to see that the Hamiltonian {eq}`eq-identpart-1` is invariant if the labels of particles 1 and 2 are swapped. This means that the operator $E_{12}$ satisfies

:::{math}
:label: eq-identpart-2
E_{12}^\dagger H E_{12} = H.
:::

The exchange operator is unitary and satisfies

:::{math}
:label: eq-identpart-3
E_{12}^2=1,
:::

as is obvious since exchanging labels twice brings us back to the original state. From this it follows that

:::{math}
:label: eq-identpart-4
E_{12}^{-1} = E_{12}^\dagger = E_{12},
:::

so $E_{12}$ is also Hermitian. Its eigenvalues are $e_{12} = \pm 1$ (using a lower case $e$ for the eigenvalues).

{eq}`eq-identpart-2` implies

:::{math}
:label: eq-identpart-5
[E_{12}, H] =0,
:::

so $E_{12}$ is a symmetry operator that commutes with the Hamiltonian. From this all the usual consequences of symmetries follow. For example, $E_{12}$ and $H$ possess a simultaneous eigenbasis, that is, it is possible to organize the eigenstates of $H$ (by forming linear combinations of degenerate states, if necessary) to make them into eigenstates of $E_{12}$. This means that the energy eigenstates can be classified by their behavior (even or odd) under exchange.

To create the simultaneous eigenstates of $E_{12}$ and $H$ it is convenient to diagonalize $E_{12}$ first, since this is easier than diagonalizing $H$. Operator $E_{12}$ has only two eigenvalues, so the Hilbert space breaks up into two orthogonal subspaces,

:::{math}
:label: eq-identpart-6
\ES_tot = \ES_even \oplus \ES_odd,
:::

where $\ES_tot$ is the entire Hilbert space of wave functions upon which the Hamiltonian {eq}`eq-identpart-1` acts, and where $\ES_even$ and $\ES_odd$ are the eigenspaces of $E_{12}$ corresponding to eigenvalues $e_{12}=+1$ and $e_{12}=-1$, respectively. Then in view of {eq}`eq-identpart-5`, the Hamiltonian $H$ has vanishing matrix elements between these two subspaces (it does not “connect” the two subspaces), so $H$ can be diagonalized within each subspace separately. This yields the usual practical advantage of symmetry operators, that is, it is much easier to diagonalize Hamiltonians on smaller spaces.

These are the usual consequences of having a symmetry operator that commutes with a Hamiltonian, and, with the change of a few words, everything we have said would also apply to symmetry operators such as parity $\pi$, which also satisfies $\pi^2=1$. See {ref}`sec-parity-10`. The exchange operator, however, has characteristics that are quite different from other symmetry operators. In particular, it turns out that only one of the two subspaces $\ES_even$ or $\ES_odd$ is physical. Which one it is depends on the spin of the identical particles. The other subspace consists of wave functions that simply do not correspond to anything in the real world.

(sec-identpart-4)=

## Definition of $E_{12}$

We now make a precise definition of the exchange operator $E_{12}$ for a system consisting of two identical particles. In the following we let $\ES$ stand for the Hilbert space of a single particle. We choose an arbitrary orthonormal basis $\{ \ket{\alpha} \}$ in this space, where $\alpha$ is an index taking on discrete or continuous values. Then

:::{math}
:label: eq-identpart-7
\ES = \mathspan \{ \ket{\alpha} \}.
:::

We let $\ES_tot$ be the Hilbert space for the two particle system (same notation as above). If the particles are identical, as we assume, this Hilbert space can be thought of as the product of two identical copies of the single particle Hilbert space,

:::{math}
:label: eq-identpart-8
\ES_tot = \ES \otimes \ES.
:::

We will put labels on the spaces $\ES$ if we wish to indicate to which particle (1 or 2) they refer, for example,

:::{math}
:label: eq-identpart-9
\ES_tot = \ES^{(1)} \otimes \ES^{(2)}.
:::

A basis for the two-particle Hilbert space is the set

:::{math}
:label: eq-identpart-10
\{ \ket{\alpha}^{(1)} \otimes \ket{\beta}^{(2)} \},
:::

where $\alpha$ and $\beta$ are independent indices that label the vectors of two copies of the same basis in $\ES$. Thus, they run over the same values. In {eq}`eq-identpart-10` we have indicated the particle number (1 or 2) to which the basis vectors belong. For brevity we write the basis vectors in $\ES_tot$ as

:::{math}
:label: eq-identpart-11
\ket{\alpha}^{(1)} \otimes \ket{\beta}^{(2)} = \ket{\alpha\beta}.
:::

Now the exchange operator is defined by

:::{math}
:label: eq-identpart-12
E_{12} \ket{\alpha\beta} = \ket{\beta\alpha}.
:::

This defines the action of $E_{12}$ on a set of basis vectors; by linearity, the definition is extended to any linear combination of them, that is, any state in $\ES_tot$. Properties {eq}`eq-identpart-3`--{eq}`eq-identpart-4` follow immediately from this definition. It turns out this definition is independent of the basis $\ket{\alpha}$ chosen in the single-particle Hilbert space.

There is no clean way to define an exchange operator for particles that are not identical, nor is there any use for such an operator. We will only use exchange operators for identical particles.

(sec-identpart-5)=

## Exchange Operator in Wave Function Language

Let us now see what $E_{12}$ does to the wave function of the system. We start with the case of a spinless particle, in which the single particle Hilbert space has the basis of position eigenkets, $\{ \ket{\xvec} \}$, where $\xvec$ runs over all of three-dimensional space. Then the basis in $\ES_tot$ is

:::{math}
:label: eq-identpart-13
\{ \ket{\xvec_1}^{(1)} \otimes \ket{\xvec_2}^{(2)} = \ket{\xvec_1 \xvec_2} \},
:::

where we indicate the abbreviated form for the product basis. The vectors $\xvec_1$ and $\xvec_2$ run independently over all of three-dimensional space to create the basis. The subscripts on $\xvec_1$, $\xvec_2$ are not particle labels, they just distinguish two points in three-dimensional space (we could have called them $\xvec_a$ and $\xvec_b$, for example). In terms of this basis, the two-particle wave function is

:::{math}
:label: eq-identpart-14
\Psi(\xvec_1,\xvec_2) = \braket{\xvec_1 \xvec_2}{\Psi},
:::

that is, it is the scalar product of the system ket $\ket{\Psi}$ with the basis vector $\ket{\xvec_1 \xvec_2}$. Here and below we use a capital letter $\Psi$ to refer to the state of a two-particle system. According to {eq}`eq-identpart-12` the action of $E_{12}$ on these basis states is

:::{math}
:label: eq-identpart-15
E_{12} \ket{\xvec_1 \xvec_2} = \ket{\xvec_2 \xvec_1}.
:::

Now we ask, what is the wave function of the state $E_{12} \ket{\Psi}$, call it $\Psi'(\xvec_1,\xvec_2)$? By the definition of the wave function {eq}`eq-identpart-14` it is

:::{math}
:label: eq-identpart-16
\Psi'(\xvec_1,\xvec_2)= \matrixelement{\xvec_1 \xvec_2}{E_{12}}{\Psi} = \braket{\xvec_2 \xvec_1}{\Psi} = \Psi(\xvec_2, \xvec_1),
:::

where we allow $E_{12}$ to act to the left and use {eq}`eq-identpart-15`. This is a simple rule:

:::{math}
:label: eq-identpart-17
\Psi(\xvec_1, \xvec_2) \mathop{\longrightarrow}\limits^{E_{12}} \Psi(\xvec_2, \xvec_1).
:::

Next we consider the case of two identical particles with spin $s$. Here the single particle Hilbert space $\ES$ has the basis

:::{math}
:label: eq-identpart-18
\{ \ket{\xvec} \otimes \ket{m} = \ket{\xvec m}\},
:::

the product of position eigenkets times the eigenkets of $S_z$, where $m=-s, \ldots,+s$. Thus we may take the basis of the two-particle Hilbert space $\ES_tot$ to be

:::{math}
:label: eq-identpart-19
\{ \ket{\xvec_1 m_1}^{(1)} \otimes \ket{\xvec_2 m_2}^{(2)} = \ket{\xvec_1 \xvec_2 m_1 m_2} \},
:::

where we indicate the abbreviated form for the basis vectors in $\ES_tot$. In this case the definition {eq}`eq-identpart-12` of the exchange operator implies

:::{math}
:label: eq-identpart-20
E_{12} \ket{\xvec_1 \xvec_2 m_1 m_2} = \ket{\xvec_2 \xvec_1 m_2 m_1}.
:::

In terms of the wave function,

:::{math}
:label: eq-identpart-21
\Psi_{m_1m_2}(\xvec_1,\xvec_2) = \braket{\xvec_1 \xvec_2 m_1 m_2}{\Psi},
:::

the action of the exchange operator may be written as

:::{math}
:label: eq-identpart-22
\Psi_{m_1m_2}(\xvec_1, \xvec_2) \mathop{\longrightarrow}\limits^{E_{12}} \Psi_{m_2m_1}(\xvec_2, \xvec_1),
:::

that is, exchange swaps both the spin and spatial labels.

(sec-identpart-6)=

## The ${}^{12}C_2$ Molecule

Let us now consider the ${}^{12}C_2$ molecule, a homonuclear diatomic molecule in which both nuclei have spin 0. This is a perfectly good diatomic molecule whose rotational spectrum can be analyzed experimentally, but it does not form a gas like $H_2$ or $N_2$ because it is chemically reactive (the carbon atoms like to form chains, rings, buckyballs, nanotubes, etc). Unfortunately there is no ordinary gas of homonuclear diatomic molecules with nuclear spin 0 that serves our purposes (${}^4He$ is a noble gas and does not form molecules in the ordinary sense, ${}^{16}O$ has been excluded because of its unusual electronic structure, other spin-0 isotopes are radioactive, etc). So we will work with ${}^{12}C_2$.

The Hamiltonian describing the vibrations and rotations of this molecule is {eq}`eq-identpart-1`, where the potential $V$ has a minimum at some radius $r_0$ (the bond length), creating a potential well that supports bound states. The excitations in this potential well are approximately harmonic for low quantum numbers, and correspond physically to the quantized vibrations of the molecule. The molecule can also rotate, and the total quantized energy is approximately the sum of a vibrational and a rotational contribution. See {eq}`eq-cenforce-82`.

As usual with central force Hamiltonians, we may transform {eq}`eq-identpart-1` from lab coordinates $(\xvec_1,\xvec_2)$ to center-of-mass and relative coordinates $(\Rvec,\rvec)$, defined in the case of equal masses by

:::{math}
:label: eq-identpart-23
\begin{aligned}
\Rvec &={\xvec_1 + \xvec_2 \over 2}, \\
\rvec &= \xvec_2 - \xvec_1. \\

\end{aligned}
:::

This is a special case of the transformation presented in {ref}`sec-cenforce-9`, in which the two masses are equal. Under this transformation the Hamiltonian {eq}`eq-identpart-1` becomes

:::{math}
:label: eq-identpart-24
H= {\Pvec^2 \over 2M} + {\pvec^2 \over 2\mu} + V(r),
:::

where $\Pvec$ is the momentum conjugate to the center-of-mass position $\Rvec$, and $\pvec$ is the momentum conjugate to the relative position $\rvec$, and where $r = |\rvec|$ is the distance between the two particles. The mass $M=2m$ is the total mass of the system, while $\mu=m/2$ is the reduced mass. The momentum $\Pvec$ is physically the total linear momentum of the system (it is $\pvec_1 + \pvec_2$). We can write this Hamiltonian as the sum of a center-of-mass and a relative term,

:::{math}
:label: eq-identpart-25
H=H_CM + H_rel,
:::

where

:::{math}
:label: eq-identpart-26
H_CM= {\Pvec^2 \over 2M}
:::

is a free particle Hamiltonian, and where

:::{math}
:label: eq-identpart-27
H_rel = {\pvec^2 \over 2\mu} + V(r).
:::

As for the wave function, we may transform it also to the new coordinates $(\Rvec,\rvec)$. We will write

:::{math}
:label: eq-identpart-28
\Psi(\xvec_1, \xvec_2) = \Psi(\Rvec,\rvec).
:::

The Schr\"odinger equation for {eq}`eq-identpart-24` separates according to the decomposition {eq}`eq-identpart-25`, so that energy eigenfunctions have the form

:::{math}
:label: eq-identpart-29
\Psi(\Rvec,\rvec) = \Phi(\Rvec) \psi(\rvec),
:::

where $\Phi(\Rvec)$ is an eigenfunction of $H_CM$ and $\psi(\rvec)$ is an eigenfunction of $H_rel$. The 2-particle Hilbert space $\ES_tot$ is spanned by products of basis wave functions of this form, that is, it has the decomposition

:::{math}
:label: eq-identpart-30
\ES_tot = \ES_CM \otimes \ES_rel,
:::

in addition to the decomposition {eq}`eq-identpart-9`. We will write {eq}`eq-identpart-29` in ket language as

:::{math}
:label: eq-identpart-31
\ket{\Psi} = \ket{\Phi} \ket{\psi},
:::

omitting the $\otimes$ for simplicity. The eigenfunction $\Phi(\Rvec)$ is a free-particle energy eigenfunction, which we may take to be

:::{math}
:label: eq-identpart-32
\Phi(\Rvec) = \exp(i\Pvec\cdot\Rvec/\hbar),
:::

where $\Pvec$ is the momentum eigenvalue. This plane wave is not the only choice for a free particle energy eigenfunction, but it is a simple one. As for the relative energy eigenfunction $\psi(\rvec)$, it is a solution of a central force problem and must have the form

:::{math}
:label: eq-identpart-33
\psi_{n\ell m}(\rvec) = f_{n\ell}(r) Y_{\ell m}(\Omega),
:::

where $f$ is the radial wave function and $(n,\ell,m)$ are the usual central force quantum numbers. With center-of-mass and relative eigenfunctions {eq}`eq-identpart-32` and {eq}`eq-identpart-33`, we will write the total energy eigenfunction {eq}`eq-identpart-29` in ket language as

:::{math}
:label: eq-identpart-34
\ket{\Psi} = \ket{\Pvec} \ket{n\ell m}.
:::

The total energy of the product wave function {eq}`eq-identpart-29` or {eq}`eq-identpart-34` is

:::{math}
:label: eq-identpart-35
E_tot = {\Pvec^2 \over 2M} + E_{n\ell},
:::

where $E_{n\ell}$ is the central force energy eigenvalue, which is independent of $m$ because of the rotational invariance of $H_rel$ (and the Wigner-Eckart theorem). In the case of a molecular potential $V$, this energy has the approximate form,

:::{math}
:label: eq-identpart-36
E_{n\ell} = {\ell (\ell+1)\hbar^2 \over 2I} + (n+\frac{1}{2})\hbar\omega,
:::

where $I=\mu r_0^2$ is the moment of inertia of the diatomic at its equilibrium bond length and $n$ is the quantum number of the approximately harmonic vibrations whose frequency is $\omega$. This approximation is rough and is valid only for small vibrational quantum numbers $n$ (near the bottom of the well, where the harmonic approximation is best), but it conveys the right idea about the rotational-vibrational spectrum of the molecule. Notice that the first term in {eq}`eq-identpart-36`, the energy of a rigid rotor of moment of inertia $I$ and angular momentum $\sqrt{\ell(\ell+1)} \hbar$, is also the centrifugal potential for a central force Hamiltonian in which the radius $r$ is fixed at the equilibrium bond length $r_0$. The energy {eq}`eq-identpart-36` is the sum of a rotational and a vibrational contribution.

Now let us consider the effect of the exchange operator $E_{12}$ on these energy eigenfunctions. By swapping labels 1 and 2, it is easy to see from {eq}`eq-identpart-23` that $\Rvec$ and $\rvec$ transform under $E_{12}$ according to

:::{math}
:label: eq-identpart-37
\begin{aligned}
\Rvec & \longrightarrow\Rvec, \\
\rvec & \longrightarrow -\rvec, \\

\end{aligned}
:::

so the effect on the wave function is

:::{math}
:label: eq-identpart-38
\Psi(\Rvec,\rvec) \mathop{\longrightarrow}\limits^{E_{12}} \Psi(\Rvec,-\rvec).
:::

The center-of-mass position is not affected, but the relative position vector is flipped through the origin. This behavior reminds us of the parity operator $\pi$, which flips all position vectors through the origin, and, in fact, $E_{12}$ behaves the same as parity insofar as the relative coordinate is concerned. As a result it is easy to confuse exchange and parity, a bad idea since physically they are quite distinct. Nevertheless, since we know what parity does to central force eigenfunctions, it is easy to see the effect of exchange on two-particle eigenfunctions such as {eq}`eq-identpart-29`. In particular, parity does not affect the radial wave function $f_{n\ell}(r)$, but it multiplies the $Y_{\ell m}$ by $(-1)^\ell$ (a phase that is independent of $m$). See {eq}`eq-parity-52`. As for the center-of-mass part of the wave function, by {eq}`eq-identpart-38` exchange does nothing to it. Altogether, we have

:::{math}
:label: eq-identpart-39
E_{12} \ket{\Psi} = E_{12} \ket{\Pvec}\ket{n\ell m} =(-1)^\ell \ket{\Psi}.
:::

The energy eigenfunctions are automatically eigenfunctions of $E_{12}$; this is the simultaneous eigenbasis whose existence is promised by the commutation relation $[E_{12},H]=0$. We see that the exchange quantum number of the energy eigenfunction is $(-1)^\ell$.

(sec-identpart-7)=

## The Symmetrization Postulate

So far we have just explored the mathematical consequences of the commutation relation $[E_{12},H]=0$. Now, however, we must take into account the important experimental fact that the states of odd $\ell$ in the rotational spectrum of ${}^{12}C_2$ do not exist. This can be determined by direct spectroscopic means, and there is similar evidence of missing rotational states, both spectroscopic and thermodynamic, for other homonuclear diatomic molecules. If one of the carbon atoms is replaced by a different isotope, say ${}^{14}C$, then all angular momentum states $\ell$ are observed. In this case the masses are no longer equal and some of the transformations we have written down require modification, and the operator $E_{12}$ is not very meaningful. Nevertheless, it is meaningful to talk about the angular momentum states $\ell$ of the rotor, and all of them are present if the nuclei are not identical. We can say that in the case of the ${}^{12}C_2$ molecule, only the subspace $\ES_even$ in {eq}`eq-identpart-6` is physical. It is perfectly possible to write down wave functions that are odd under exchange, including perfectly valid eigenfunctions of the Hamiltonian {eq}`eq-identpart-1`, but these do not correspond to anything physical. They are just mathematical objects without any correspondence with physical reality.

These facts about the ${}^{12}C_2$ molecule are a special case of a collection of experimental evidence that can be summarized in what we will call the *symmetrization postulate*:

- {} **Symmetrization Postulate.\ **{\sl In any system consisting of two or more identical particles, the wave function is symmetric under the exchange of any two identical bosons, and antisymmetric under the exchange of any two identical fermions.}

Recall that bosons are particles of integer spin, while fermions are particles of half-integer spin. Notice that a system may contain more than one different species of identical particles, for example, helium has two identical protons and two identical neutrons in the nucleus, and two identical electrons orbiting the nucleus. The symmetrization postulate applies to exchange of any pair of identical particles of any species. We have only defined the exchange operator in these notes for the case of two identical particles, but the definition is easily extended to multiparticle systems, something we shall do when we study such systems.

This postulate cannot be derived from the earlier (measurement) postulates of quantum mechanics discussed in {ref}`ch-postulat`\ or \density. Within the context of nonrelativistic quantum mechanics it must simply be taken as an experimental fact. Indeed it *is* an experimental fact, and historically this was how it was discovered. Nevertheless, within the framework of relativistic quantum field theory, it is possible to justify the symmetrization postulate on the basis of certain reasonable assumptions. These include the requirement that energy be bounded from below and that relativistic causality hold (signals cannot travel faster than the speed of light). This theoretical derivation of the symmetrization postulate was given by Pauli in 1940, in the form of the famous *spin and statistics theorem*. It is regarded as one of the triumphs of relativistic quantum field theory.

Although as we say the symmetrization postulate cannot be derived from the measurement postulates of quantum mechanics, at least within the nonrelativistic theory, nevertheless it is possible to see that there are some problems with the measurement postulates as stated earlier when particles are identical. This is related to the existence of nonphysical operators, which we will mention momentarily. The measurement situation is discussed more fully in Messiah, *Quantum Mechanics*.

It has to be regarded as a defect of the wave function language for quantum mechanics that it is possible to write down wave functions or “states” that do not correspond to any physical reality. This defect is remedied by methods of quantum field theory, which we will take up later in the course, in which all states that one can write down are physical. Quantum field theory also incorporates the exchange symmetry of the states in a natural way (there is no need to discuss exchange operators). Nevertheless, it is probably more satisfactory from a pedagogical standpoint to continue with wave function language for the time being, although this does mean that we must keep track of what is the physical subspace of the nominal Hilbert space we are working with.

The present formalism not only allows us to write down nonphysical wave functions, it also allows us to write down nonphysical operators. A nonphysical operator is one that takes a state in the physical subspace of the nominal Hilbert space (one that satisfies the right symmetry under exchange), and maps it into a nonphysical state (one that does not have the right symmetry). An example is the operator $\xvec_1^op$, where the “op” reminds us that this is an operator and not an eigenvalue ($c$-number). We might call this the “operator corresponding to the measurement of the position of particle 1.” The problem with this operator from a physical standpoint is that you cannot measure the position of “particle 1.” You can select a region of space (in a two-particle system), and ask whether there is a particle in that region. But if you find one, you cannot say whether it is particle 1 or particle 2, since they are identical. On the other hand, the operator $\Rvec =(\xvec_1+\xvec_2)/2$ is a physical operator (we omit the “op” superscripts), because it commutes with $E_{12}$ and hence leaves the physical subspace invariant.

The same reasoning applies to the spin operators $\Svec_1$ and $\Svec_2$, neither of which is physical. Thus the magnetic quantum numbers $m_1$ and $m_2$ that appear in the wave function {eq}`eq-identpart-22`, for example, are really nonphysical. The total spin operator $\Svec=\Svec_1 + \Svec_2$, however, and functions of it, are physical, since they commute with $E_{12}$. Physical operators correspond to measurements that can actually be made. Nonphysical operators may be useful for mathematical purposes in manipulating wave functions, not all of which need be physical, but they do not correspond to anything that can be measured.

In fact, any operator that attempts to label the particles is nonphysical. It is impossible to write down a wave function for a system of identical particles without labeling the particles, but no physics can depend on this labeling. (And with methods of quantum field theory, the necessity for this labeling disappears.)

(sec-identpart-8)=

## The Hydrogen Molecule

We now consider the hydrogen molecule $H_2$, in which the nuclei are protons (ordinary hydrogen). The proton is a fermion with spin $\frac{1}{2}$, so by the symmetrization postulate only the subspace $\ES_odd$ of the nominal Hilbert space is physical. Let us see what difference this makes in comparison with the case of ${}^{12}C$, whose nucleus is a boson.

The Hamiltonian is still {eq}`eq-identpart-1`, with the proton mass $m$ and Born-Oppenheimer potential $V$ for hydrogen. In particular, there are no spin-dependent terms in the Hamiltonian, which is a purely spatial operator. More precisely, the energy of the system does depend to a small extent on the orientation of the proton spins (for example, through the dipole-dipole interaction of the two protons), but this energy is extremely small compared to the terms present in {eq}`eq-identpart-1`. The neglect of these spin-dependent terms in no way affects any of the major conclusions of the following argument, in which we find a dramatic dependence of the behavior of the hydrogen molecule, depending on the spin state. This is the normal situation in nonrelativistic quantum mechanics: the direct magnetic interactions of spins involve only very small energies, but due to the requirements of the symmetrization postulate, spin ends up having a much bigger effect than the magnetic energy alone would indicate.

Since the Hamiltonian has the same form as in the case of the ${}^{12}C_2$ molecule, most of the analysis of its eigenfunctions and eigenvalues goes through exactly as in \secridentpart-6. The only difference is that the wave function must be multiplied by a spin part, that is, the total Hilbert space is

:::{math}
:label: eq-identpart-40
\ES_tot = \ES_orb \otimes \ES_spin,
:::

where $\ES_orb$ describes the spatial or orbital degrees of freedom, exactly like $\ES_tot$ in {eq}`eq-identpart-30`, while

:::{math}
:label: eq-identpart-41
\ES_spin = \mathspan \{ \ket{m_1}^{(1)} \otimes \ket{m_2}^{(2)} = \ket{m_1 m_2} \}.
:::

The spatial part of the energy eigenfunctions for the $H_2$ molecule have the form shown in {eq}`eq-identpart-29`--{eq}`eq-identpart-34`; these can be multiplied by any spin wave function (any linear combination of the spin basis states $\ket{m_1m_2}$) and we will have an energy eigenfunction, since $H$ does not operate on the spin variables. As for the energies, they are given by {eq}`eq-identpart-35` and {eq}`eq-identpart-36`, exactly as with ${}^{12}C$ (of course, the constants $m$, $\omega$, etc., are different).

Some eigenfunctions created in this way, however, are nonphysical, because they are not odd under exchange. To create eigenfunctions that do have the right properties under exchange, it helps to choose a basis for the spin part of the wave function other than $\{ \ket{m_1m_2} \}$. This basis is what we called the “uncoupled basis” in Notes.~\jjcouple. The coupled basis is $\{ \ket{SM}\}$, the eigenbasis of $S^2$ and $S_z$, where $\Svec=\Svec_1+\Svec_2$. We use capital letters $S$ and $M$ for the quantum numbers of the operators $S^2$ and $S_z$, respectively, to indicate that they refer to properties of the multiparticle system. We use lower case letters $s$, $m$, etc., to refer to the properties of a single particle. As noted above, the operators $S^2$ and $S_z$ commute with $E_{12}$ and are physical, so their eigenfunctions (which are nondegenerate) must be eigenfunctions also of $E_{12}$. See Theorem {ref}`thm-hilbert-5`.

Indeed, this is the case. If we just write out the Clebsch-Gordan expansion for $\frac{1}{2} \otimes \frac{1}{2}$ we get

:::{math}
:label: eq-identpart-42
\begin{aligned}
\ket{00} & = {1\over\sqrt{2}} \Bigl( \ket{\frac{1}{2}}\ket{-\frac{1}{2}} - \ket{-\frac{1}{2}}\ket{\frac{1}{2}}\Bigr),
\end{aligned}
:::

:::{math}
:label: eq-identpart-43a
\begin{aligned}
\ket{11} &= \ket{\frac{1}{2}} \ket{\frac{1}{2}},
\end{aligned}
:::

:::{math}
:label: eq-identpart-43b
\begin{aligned}
\ket{10} &= {1\over\sqrt{2}} \Bigl( \ket{\frac{1}{2}}\ket{-\frac{1}{2}} + \ket{-\frac{1}{2}}\ket{\frac{1}{2}}\Bigr),
\end{aligned}
:::

:::{math}
\begin{aligned}
\ket{1,-1} &= \ket{-\frac{1}{2}} \ket{-\frac{1}{2}}, & {eq}`eq-identpart-43a`
\end{aligned}
:::

which expresses the states $\ket{SM}$ on the left hand side as linear combinations of the states $\ket{m_1 m_2}$ on the right. The state {eq}`eq-identpart-42`, with $S=0$, is called the *singlet* state (because there is only one state), while the three states {eq}`eq-identpart-43a`, with $S=1$, are called the *triplet* state (because there are three of them). It follows from direct inspection of this table that all these states $\ket{SM}$ are eigenstates of $E_{12}$: the singlet state is odd under exchange, while the triplet states (all three of them) are even under exchange. The exchange symmetry does not depend on the magnetic quantum number $M$. We can summarize these facts by writing

:::{math}
:label: eq-identpart-44
E_{12} \ket{SM} = \sigma_S \ket{SM},
:::

where

:::{math}
:label: eq-identpart-45
\begin{aligned}
\sigma_S = \begin{cases} -1, & S=0, \\ +1, & S=1  \\\end{cases}.
\end{aligned}

:::

If we choose the spin states $\ket{SM}$ for the spin part of the energy eigenfunction, then the total energy eigenfunction for the hydrogen molecule is

:::{math}
:label: eq-identpart-46
\ket{\Psi} = \ket{\Pvec} \ket{n\ell m} \ket{SM}.
:::

Applying the exchange operator, we now find

:::{math}
:label: eq-identpart-47
E_{12} \ket{\Psi} = (-1)^\ell \sigma_S \ket{\Psi}.
:::

Again we have constructed the simultaneous eigenbasis of $E_{12}$ and $H$, whose existence is guaranteed by $[E_{12},H]=0$; to do this we had to form some linear combinations, namely precisely those in {eq}`eq-identpart-42` and {eq}`eq-identpart-43a`.

Now in view of the symmetrization postulate, we see that only those states with

:::{math}
:label: eq-identpart-48
(-1)^\ell \sigma_S = -1
:::

are physical. This means that if $S=0$ (singlet spin state), then $\ell$ must be even, while if $S=1$ (triplet state), then $\ell$ must be odd. Unlike the case of ${}^{12}C_2$, the $H_2$ molecule possesses all rotational states, both even and odd $\ell$; however, the degeneracies are not the same, due to the differing spin degeneracies. The situation is summarized in {ref}`tbl-identpart-1`.

:::{list-table} Linkage of spatial and spin exchange symmetry in the ${H}_2$ molecule and terminology.
:label: tbl-identpart-1
:header-rows: 1

* - $S$
  - degen
  - $e_{12}^{spin}$
  - $\ell$
  - $e_{12}^{orb}$
  - $e_{12}$
  - name
  - 
* - $0$
  - $1$
  - $-1$
  - even
  - $+1$
  - $-1$
  - para
  - 
* - $1$
  - $3$
  - $+1$
  - odd
  - $-1$
  - $-1$
  - ortho
  - 

:::
At the left of the table is the terminology for the spin state, singlet or triplet, followed by the spin value $S$ and the spin degeneracy. The quantum number $e_{12}^spin$ is the symmetry of the spin part of the wave function under exchange, that is, it is $\sigma_S$. By the symmetrization postulate, this implies the opposite exchange symmetry of the spatial part of the wave function, $e_{12}^orb$, so that the total exchange symmetry $e_{12}$ can be $-1$, as required. In the final column are more names; “para” refers to a wave function that is spatially symmetric, while “ortho” refers to a spatially antisymmetric wave function. In the case of the $H_2$ molecule, these names are linked to the spin states as shown in the table (in other systems there may be a different relation between spatial and spin symmetry). Corresponding to these names, one sometimes speaks of “parahydrogen” and “orthohydrogen” as if they were two species of $H_2$.

The degeneracies in particular have an impact on the thermodynamic properties of $H_2$ gas. At high temperatures (for $H_2$ this means room temperature) the angular momentum quantum number $\ell$ is large and there is little relative difference between the energies of the neighboring even and odd rotational states $\ell$ and $\ell+1$. Thus the Boltzmann factor $\exp(-E/kT)$ is nearly the same for both states, and the relative populations are determined mostly by the degeneracies. Thus, at high temperatures, $H_2$ gas consists of $25\%$ parahydrogen and $75\%$ orthohydrogen (a 1-to-3 ratio). At low temperatures, however, the hydrogen molecule mostly drops into the ground rotational state $\ell=0$, which is a singlet (para) state, so the percentage of parahydrogen approaches $100\%$ at low temperatures. This is in thermal equilibrium; as you lower the temperature of hydrogen gas, orthohydrogen molecules in the triplet state must undergo spin flips to convert to parahydrogen in order to maintain equilibrium. The spin degeneracies play an important role in the specific heat of hydrogen gas at low temperatures, and, in particular, the specific heat is quite different from what would be predicted if we did not know about the symmetrization postulate.

Experimental measurements of the rotational spectrum of $*H*_2$ at low temperatures played an important role historically in the realization that there is a general relationship between spin and statistics, although the interpretation of the experimental results was hindered by the fact that the equilibration time between the spin singlet and triplet states is rather long (it is measured in days, in the absence of catalysts). This is because the proton spins can only be flipped by magnetic forces, which are quite weak during the collision of two $H_2$ molecules. Therefore if you cool hydrogen gas at room temperature down to low temperatures, the ratio of spin singlet and triplet states stays at its high temperature value (1-to-3) for quite some time (it takes a long time for the system to approach thermal equilibrium).

These experiments were carried out by Hori in Copenhagen in 1927, and gave results that did not agree with the theory previously worked out by Hund (because Hori's hydrogen gas was not in thermal equilibrium). The discrepancy was resolved by Dennison shortly afterward, who called attention to the long equilibration time. Dennison at first did not realize the importance of his result; only as an afterthought, he published another paper in which he pointed out that the data and its correct interpretation showed that the proton has spin $\frac{1}{2}$ and that it obeys Fermi statistics (antisymmetric wave functions). This was a big breakthrough in the appreciation of the general relation between spin and statistics. The episode is recounted in *The Story of Spin*, by Sin-itiro Tomonaga.

\problems

(prob-identpart-1)=

**Problem \prbdidentpart-1..** 

\problempart{(a)} In classical statistical mechanics, each degree of freedom contributes an amount $\frac{1}{2}Nk$ to the specific heat $C_v$, where $N$ is the number of particles and $k$ is the Boltzmann constant. In this context, a “degree of freedom” means a quadratic term in the Hamiltonian, for example, $p^2/2$ or $x^2/2$. For example, the three translational degrees of freedom of a molecule contribute $\frac{3}{2}Nk$, and the two rotational degrees of freedom of a diatomic contribute $Nk$ more (the third rotational degree of freedom about the axis of the molecule is frozen out because of the small moment of inertia).

Use quantum statistical mechanics to compute the rotational contribution to the specific heat $C_v$ of $H_2$ gas in both the low and high temperature limits. In each case, just give the dominant term at low or high temperatures. Give a quantitative condition as to what “low” and “high” temperatures mean in this case, and work out a characteristic temperature in Kelvins that separates the two temperature regimes. Hint: in the high temperature limit, evaluate the sum by regarding it as a Riemann sum approximation to an integral. Then do the integral. The bond length of the hydrogen molecule is 0.74 Angstrom.

\problempart{(b)} Do the same for $D_2$ gas (deuterium).

(prob-identpart-2)=

**Problem \prbdidentpart-2.} In working the previous problem, you may have noticed that when you combine equal spins, say, $j_1=j_2=j$, according to $\Svec=\Jvec_1+\Jvec_2$, then the states $s=2j$, that is, the states $\ket{s m_s}$ for $s=2j$, are symmetric under exchange $E_{12}$, the states $s=2j-1$ are antisymmetric, etc.  In the following problem you must not use any properties of the Clebsch-Gordan coefficients, only general properties of operators such as $S^2$, $S_z$, $E_{12.** 

\problempart{(a)} Prove that the states }$s=2j$ are symmetric under exchange (all of them, that is, all $2s+1$ of them).

\problempart{(b)} Prove that as the total value of $s$ is decreased from its maximum of $2j$ to its minimum of 0, the states $\ket{s m_s}$ alternate between symmetric and antisymmetric under exchange. Hint: Review the general proof for the addition of angular momenta, that says when you combine angular momenta according to $\Svec = \Jvec_1 + \Jvec_2$, you get $j=|j_1-j_2|, \ldots, j_1+j_2$. In the present case we are interested in $j_1=j_2=j$. Think of the square of $(2j+1)^2$ lattice points in the $m_1$-$m_2$ plane, representing the uncoupled basis $\ket{m_1}\ket{ m_2}$.

(prob-identpart-3)=

**Problem \prbdidentpart-3..** 

\problempart{(a)} Consider hydrogen gas at STP (one atmosphere pressure, $T=273K$). Let us estimate the time required for the proton spin in an individual hydrogen molecule to flip, thereby converting a molecule of orthohydrogen into parahydrogen, or vice versa. The proton spin in a given hydrogen molecule responds to magnetic fields which are produced by the protons in another hydrogen molecule during collisions. Estimate the cross for collision of two hydrogen molecules as $\sigma=2\pi a_0^2$, where $a_0$ is the Bohr radius. This will be a rough calculation so one or two significant figures will be enough. Calculate the number of collisions per second that a given hydrogen molecule will experience.

During the collision, the protons in one molecule and those in the other never come much closer together than $a_0$, because they are cushioned by the electron clouds. Ignoring all angle dependence, estimate the magnetic field one proton will experience at a distance of $a_0$ from the other proton (in Gauss). Estimate the time of collision $\tau$ as $a_0/v$, where $v$ is the average velocity of the molecules at the temperature given. Then use this to estimate $\Delta \theta$, the angle by which the spin on one proton changes during the collision time $\tau$, due to the magnetic field of the proton in the other molecule.

Finally, given that the angles accumulate between collisions by a random walk, estimate the time required for a total angle of $\pi$ to accumulate. Take this as an estimate of the equilibration time for ortho and parahydrogen. You can see the time would be somewhat longer at lower temperatures, and shorter at higher pressures.

:::{list-table} Rotational energy of ${H}_2$ molecule in thermal equilibrium as a function of temperature. Energy per molecule is given, in Kelvins; temperature is in Kelvins.
:label: tbl-identpart-2
:header-rows: 1

* - $T$
  - $E$
  - $T$
  - $E$
  - $T$
  - $E$
* - $0$
  - $0.0$
  - $50$
  - $37.1$
  - $100$
  - $111.3$
* - $5$
  - $0.0$
  - $55$
  - $47.4$
  - $105$
  - $115.8$
* - $10$
  - $0.0$
  - $60$
  - $57.2$
  - $110$
  - $120.0$
* - $15$
  - $0.0$
  - $65$
  - $66.4$
  - $115$
  - $123.9$
* - $20$
  - $0.2$
  - $70$
  - $74.9$
  - $120$
  - $127.7$
* - $25$
  - $1.4$
  - $75$
  - $82.5$
  - $125$
  - $131.4$
* - $30$
  - $4.4$
  - $80$
  - $89.4$
  - $130$
  - $135.0$
* - $35$
  - $9.8$
  - $85$
  - $95.6$
  - $135$
  - $138.5$
* - $40$
  - $17.5$
  - $90$
  - $101.3$
  - $140$
  - $141.9$
* - $45$
  - $26.9$
  - $95$
  - $106.5$
  - $145$
  - $145.3$

:::
(prob-identpart-4)=

**Problem (b)} Hydrogen gas at room temperature is lowered to $20{\rm K.** 

We keep the hydrogen thermally insulated and wait for it to come to thermal equilibrium. What temperature does the thermometer register when equilibrium is achieved? Use {ref}`tbl-identpart-2` to make a reasonable estimate. Take the bond length of the hydrogen molecule to be 0.74 Angstrom.
