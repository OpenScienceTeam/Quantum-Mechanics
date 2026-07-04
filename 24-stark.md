---
title: "24. The Stark Effect in Hydrogen and Alkali Atoms"
---
(ch-stark)=

# 24. The Stark Effect in Hydrogen and Alkali Atoms

(sec-stark-1)=

## Introduction

In these notes we consider the Stark effect in hydrogen and alkali atoms as a physically interesting example of bound state perturbation theory. The Stark effect concerns the behavior of atoms in external electric fields. We choose hydrogen and alkali atoms because they are single-electron atoms (in the case of alkalis, this is a model). We particularly emphasize the role that symmetry principles play in the analysis of the Stark effect, and the physical ramifications.

The first observations of the splitting of spectral lines by electric fields were made by Stark in 1913, for which he was awarded the Nobel prize in 1919. Stark was an early supporter of Einstein's relativity theory, as well as Einstein's ideas about photons, about which most physicists of the time were very skeptical. After the Nazis came to power, however, he obtained a high position in the scientific establishment and, along with fellow Nobel laureate Philipp Lenard, promoted the notion that “Jewish physics,” which meant especially the theory of relativity, was degenerate and false. He also attacked Heisenberg, who defended both Einstein and relativity. After World War II, he was sentenced to four years in prison by a denazification court. Today Stark is remembered probably more for his racist and nationalistic political views than for his science.

(sec-stark-2)=

## Atomic Models

The one-electron atom will be modeled with the central force Hamiltonian,

:::{math}
:label: eq-stark-1
H_0 = {p^2\over 2m} + V_0(r).
:::

For hydrogen the potential is

:::{math}
:label: eq-stark-2
V_0(r) = -{e^2\over r},
:::

while for the alkalis the potential is described in {ref}`sec-hydrogen-9`.

In this Hamiltonian we ignore spin and other small effects such as relativistic corrections, hyperfine effects and the Lamb shift. These effects cause a splitting and shifting of the energy levels of our simplified model, as well as the introduction of new quantum numbers and new degrees of freedom. But these effects are all small, and if the applied electric field is strong enough, it will overwhelm them and the physical consequences will be much as we shall describe them with our simplified model. For weak applied electric fields, however, a realistic treatment would require that all the small effects (the external electric field included) be treated together. See Prob.~\prbrstark-2, in which the transition from weak to strong electric fields is explored.

(sec-stark-3)=

## The Unperturbed System

Before embarking on perturbation theory, we must understand the unperturbed system, its energies, eigenstates and their degeneracies. In the electrostatic model, the unperturbed energy levels in hydrogen are

:::{math}
:label: eq-stark-3
given by the usual Bohr formula, E_n = -{1\over 2n^2} {e^2\over a_0},  where a_0 is the Bohr radius (see
:::

{ref}`tbl-hydrogen-1`). Here we ignore the small difference between the electron mass $m$ and the reduced mass $\mu$. According to {eq}`eq-hydrogen-24`, these levels are $n^2$-fold degenerate. In the case of the alkalis, the energy levels have the form $E_{n\ell}$, and are $(2\ell+1)$-fold degenerate. There is no simple formula for the alkali levels $E_{n\ell}$, but for given $n$, the energies are an increasing function of $\ell$, as shown in case of sodium in Fig.~\figr\hydrogen.3. As we shall see, the differences in the degeneracies has an important impact on the Stark effect in hydrogen as compared to that in the alkalis. As explained in {ref}`ch-hydrogen`, the extra degeneracy in hydrogen is due to the extra symmetry [$SO(4)$ instead of $SO(3)$] that it possesses, in comparison with a generic central force problem, such as an alkali in the model described in {ref}`sec-hydrogen-9`. As for the eigenstates, in both hydrogen and the alkalis they have the form $\ket{n\ell m}$; these are central force eigenfunctions of the form

:::{math}
:label: eq-stark-4
\psi_{n\ell m}(\xvec) = R_{n\ell}(r) \, Y_{\ell m}(\theta,\phi).
:::

(sec-stark-4)=

## Potentials and Nonperturbative Considerations

As for the perturbation, let us write $\Fvec$ for the external electric field (instead of $\Evec$, to avoid confusion with the energy $E$), and let us take it to lie in the $z$-direction,

:::{math}
:label: eq-stark-5
\Fvec = F{\hat{\mathbf{z}}}.
:::

Thus, the perturbing potential has the form

:::{math}
:label: eq-stark-6
V_1 = q\Phi=-q\Fvec\cdot\xvec = eFz,
:::

where we set $q=-e$ for the electron. The unperturbed potential $V_0$ depends on $r$, but the perturbing potential $V_1$ depends on $z$, so the perturbation breaks the full $SO(3)$ rotational symmetry of the unperturbed problem. However, the perturbed Hamiltonian is still invariant under $SO(2)$ rotations about the $z$-axis.

{ref}`fig-stark-1` is a plot of the total potential $V_0+V_1$ along the $z$-axis, which reveals several qualitative features of the exact solution. For small $z$, the attractive Coulomb field dominates the total potential, and we have the usual Coulomb well that supports atomic bound states. We assume the applied electric field $\Fvec$ is small compared to the electric field due to the nucleus in this region, which justifies the use of perturbation theory. This is reasonable for most realistic, laboratory strength fields $\Fvec$, since the electric field due to the nucleus at a typical atomic distance is of the order of $10^9$ Volts/cm. In practice, large electric fields can be created in capacitors in which the dielectric layer is very thin, for example, a layer of metal oxide, which may be only a few atoms thick. Elsewhere laboratory electric fields tend to be much weaker than those inside atoms.

:::{figure} images/stark-fig01.png
:label: fig-stark-1
:width: 80%

The total potential energy $V_0+V_1$ along the $z$-axis for an atomic electron in the Stark effect. The atomic states that are bound in the absence of the external field become resonances (dotted lines) when the perturbation is turned on.
:::

However, for large negative $z$, the unperturbed potential goes to zero, while the perturbing potential becomes large and negative. At intermediate values of negative $z$, the competition between the two potentials gives a maximum in the total potential. The electric force on the electron, which is the negative of the slope of the potential energy curve, is zero at the maximum of the potential, so this is the point where the applied and the nuclear electric fields cancel each other. Given the relative weakness of the applied field, the maximum must occur at a distance from the nucleus that is large in comparison to the Bohr radius $a_0$. Atomic states with small principal quantum numbers $n$ lie well inside this radius (hence in the region where the external electric field is much smaller than the electric field of the nucleus). The perturbation analysis we shall perform applies to these states.

The bound states of the unperturbed system are able to tunnel through the potential barrier, as indicated by the dotted lines in the figure. We see that when an external electric field is turned on, the bound states of the atom cease to be bound in the strict sense, and become resonances. This happens regardless of how weak the external field is. This is because an electron can gain an arbitrarily large amount of energy in an uniform field if we are willing to move it far enough, and this energy can be larger than the binding energy of the atom. Electrons that tunnel through the barrier and emerge into the classically allowed region at large negative $z$ will accelerate in the external field, leaving behind an ion. This is the phenomenon of *field ionization*.

However, the time scale for this tunneling may be very long. As we know from WKB theory, the tunneling probability is exponentially small in the tunneling action, so we expect the deeper bound states to have longer lifetimes in the external field, perhaps extremely long lifetimes. Furthermore, as the strength of the electric field is decreased, the distance the electron must tunnel increases, and the tunneling probability decreases exponentially. On the other hand, the atom has an infinite number of very weakly bound states that pile up at $E=0$, and many of these will lie above the top of the barrier when the external field is turned on. In the presence of the perturbation, these states are ionized immediately.

In the following perturbation analysis, we will see no evidence of the tunneling. A resonance can be thought of as an energy level that has both a real and an imaginary part, where the imaginary part is related to the lifetime by $\tau=\hbar/\Im E$; as we will see, bound state perturbation theory will only give us the shift in the real parts of the energy levels under the perturbation. The imaginary parts can be computed by various means, such as WKB theory, time-dependent perturbation theory, or (in the case of hydrogen) an exact separation of the wave equation in confocal parabolic coordinates.

(sec-stark-5)=

## No Linear Stark Effect in the Ground State

For simplicity, let us begin the perturbation analysis with the ground state of the atom, so we can use nondegenerate perturbation theory. In the case of hydrogen, the ground state is the $1s$ or $\ket{n\ell m}=\ket{100}$ level, and for an alkali, the ground state has the form $\ket{n00}$ (for example, $n=3$ for $\rm Na$). According to {eq}`eq-pertth-22` (with a change of notation), the first order shift in the ground state energy level is given by

:::{math}
:label: eq-stark-7
\Delta E^{(1)}_gnd = \matrixelement{n00}{eFz}{n00} =0,
:::

which vanishes because of parity. The operator $z$ is odd under parity, while the state $\ket{n00}$ is one of a definite parity (even), so the matrix element vanishes. The matrix elements are the same as in the theory of electric dipole radiative transitions, and follow the same selection rules (here Laporte's rule). See {ref}`sec-parity-11`. As we say, there is no linear Stark effect (no first order energy shift) in the ground state of hydrogen or the alkalis.

(sec-stark-6)=

## Linear Stark Effect and Permanent Electric Dipole Moments

The linear Stark effect is closely related to the permanent electric dipole moment of the corresponding quantum state. In classical electrostatics, the dipole moment vector $\dvec$ of a charge distribution is defined by

:::{math}
:label: eq-stark-8
\dvec = \int d^3\xvec \, \rho(\xvec) \xvec,
:::

that is, it is the charge-weighted position vector. [This is {eq}`eq-orbamsph-85`.] In the presence of an external electric field $\Fvec$, the classical dipole has the energy,

:::{math}
:label: eq-stark-9
E = - \dvec \cdot \Fvec,
:::

which is the potential energy of orientation of the dipole.

To describe the quantum mechanics of a single charged particle, we may replace $\rho(\xvec)$ in {eq}`eq-stark-8` by $q|\psi(\xvec)|^2$ (see {ref}`sec-tevolut-15`), and interpret the result as the expectation value of the *dipole moment operator*,

:::{math}
:label: eq-stark-10
\xpecval\dvec = \int d^3\xvec \, \psi(\xvec)^\cc (q\xvec) \psi(\xvec),
:::

where the operator itself is given by

:::{math}
:label: eq-stark-11
\dvec=q\xvec.
:::

If there is more than one charged particle we define the dipole moment operator by the sum,

:::{math}
:label: eq-stark-12
\dvec = \sum_i q_i \xvec_i.
:::

A quantum state $\ket{\psi}$ is considered to have a permanent electric dipole moment if the expectation value $\matrixelement{\psi}{\dvec}{\psi}$ is nonzero. In the case of a single electron system with $q=-e$, the expectation value is

:::{math}
:label: eq-stark-13
\xpecval{\dvec} = \matrixelement{\psi}{(-e\xvec)}{\psi},
:::

so that if $\ket{\psi}$ is an energy eigenstate, then the first order energy shift due to the external field $\Fvec$ is

:::{math}
:label: eq-stark-14
\Delta E^{(1)} = -\xpecval{\dvec} \cdot \Fvec.
:::

Compare this to {eq}`eq-stark-9`. We see that there is a nonzero linear Stark effect in the quantum state $\ket{\psi}$ if and only if the state possesses a nonzero permanent electric dipole moment. The linear relationship shown in {eq}`eq-stark-14` between the energy shift and the applied electric field explains the terminology, “linear Stark effect.”

(sec-stark-7)=

## No Linear Stark Effect in Any Nondegenerate State of Any System

Since we failed to find a linear Stark effect in the ground state of hydrogen or alkalis, let us look for one in other systems. For the time being we consider only nondegenerate energy eigenstates.

Suppose we have a Hamiltonian $H_0$ for any isolated system (atom, molecule, nucleus, etc., of arbitrary complexity). $H_0$ could be the Hamiltonian for hydrogen or the alkali atom, but with all the small corrections and (in the case of the alkali) multiparticle effects included, or it could be a multiparticle system. The $0$ subscript means the unperturbed system; the system is no longer isolated after the external field is turned on. We suppose this Hamiltonian commutes with parity, $[\pi,H_0]=0$. This is an extremely good approximation for most systems, since parity violations come from the weak interactions which are extremely small in most circumstances. In the following we will neglect small parity violating effects, and treat all Hamiltonians $H_0$ for isolated systems as if they commute with parity.

Now let $\ket{\psi}$ be a nondegenerate energy eigenstate of such a system. It was shown in {ref}`sec-parity-8` that such eigenstates are also eigenstates of parity, that is

:::{math}
:label: eq-stark-15
\pi\ket{\psi} = e \ket{\psi},
:::

where $e=\pm 1$. This is really a simple application of Theorem {ref}`thm-hilbert-5`. Thus,

:::{math}
:label: eq-stark-16
\matrixelement{\psi}{\dvec}{\psi}=0,
:::

because $\dvec$ only connects states of opposite parity.

The vanishing of the linear Stark effect in the ground state of hydrogen and the alkalis was not special to those systems or the models we used for them, but follows from conservation of parity and the fact that we are considering nondegenerate states.

(sec-stark-8)=

## No Linear Stark Effect in the Excited States of Alkalis

We see that if we wish to find a nonvanishing linear Stark effect, we must examine degenerate states. We begin with the excited states of the alkalis, which are simpler than the excited states of hydrogen because the degeneracy is smaller. These states have energies $E_{n\ell}$ and are $(2\ell+1)$-fold degenerate, that is, they are degenerate for $\ell \ge 1$, so to find the first order energy shifts we must use degenerate perturbation theory. According to \pertth.6, the first order energy shifts for the Stark effect in the excited states of the alkalis are the eigenvalues of the $(2\ell+1)\times(2\ell+1)$ matrix indexed by $m$ and $m'$,

:::{math}
:label: eq-stark-17
\matrixelement{n\ell m}{eFz}{n\ell m'}.
:::

Notice that $n$ and $\ell$ are the same on both sides of these matrix elements, because these indices label the unperturbed, degenerate level. Only the index $m$ is allowed to be different on the two sides, because this index labels the basis kets lying in the unperturbed eigenspace.

But we need not do any work to find the eigenvalues of this matrix, because all the matrix elements {eq}`eq-stark-17` vanish, again by parity. This is because the parity of a central force eigenstate $\ket{n\ell m}$ is $(-1)^\ell$ (see {ref}`sec-parity-11`), which is the same on both sides of the matrix elements {eq}`eq-stark-17`. So once again we fail to find a linear Stark effect.

(sec-stark-9)=

## Degeneracies and Parity in Generic, Isolated Systems

To review some facts about isolated systems, the presentation of Secs. {ref}`sec-transfop-9`--{ref}`sec-transfop-12` led to Theorem {ref}`thm-transfop-1`, which states that the energy eigenspaces of isolated systems consist of one or more irreducible subspaces under rotations. We also explained that with a few exceptions, including the electrostatic model of hydrogen, these eigenspaces consist of just a single irreducible subspace, characterized by a value of $j$. Then, in {ref}`sec-parity-8`, we explained that in isolated systems that are invariant under parity, the energy eigenspaces consisting of a single irreducible subspace are also eigenspaces of parity, that is, they are states of a definite parity. If we call these energy levels $\ket{njm}$, where $n$ is a sequencing number of the energy for a given value of $j$, then the matrix needed to compute the first order Stark effect on energy level $E_{nj}$ is

:::{math}
:label: eq-stark-18
\matrixelement{njm}{\dvec}{njm'},
:::

where $\dvec$ is given by {eq}`eq-stark-12`. But since $\dvec$ is odd under parity (it is a true vector), and since the parities of the two states on the two sides of the matrix element {eq}`eq-stark-18` are the same, this matrix element vanishes. This implies the vanishing of the linear Stark effect in energy eigenstates of generic, isolated systems.

We see that to find a nonvanishing linear Stark effect in an isolated system we must find a system in which there is a degeneracy between different energy multiplets $E_{nj}$ for different values of $(nj)$, and, moreover, we must have different multiplets of the same energy but opposite parity. The most important example where such multiplets of the same energy but opposite parity occur is the excited states of hydrogen, to which we now turn.

(sec-stark-10)=

## Linear Stark Effect in the Excited States of Hydrogen

The excited states of hydrogen ($n \ge 2$) have a degeneracy between states of opposite parity, since $\ell=0, \ldots, n-1$ and since the parity is even for even $\ell$ and odd for odd $\ell$. According to first order, degenerate perturbation theory, the shifts in the energy levels $E_n$ are given by the eigenvalues of the $n^2 \times n^2$ matrix, indexed by $(\ell m)$ and $(\ell' m')$,

:::{math}
:label: eq-stark-19
\matrixelement{n\ell m}{eFz}{n\ell'm'}.
:::

Notice the indices that are primed and those that are not. This is potentially a large matrix, but many of the matrix elements vanish because of various symmetry considerations. The $\ell$-selection rule, which follows from the Wigner-Eckart theorem and parity, is the same as in the theory of dipole transitions, namely, $\Delta\ell=\pm1$ (the Wigner-Eckart theorem would allow $\Delta\ell=0$, but this is excluded by parity). There is also a selection rule on the magnetic quantum number: since the operator $z$ is the $q=0$ component of a $k=1$ irreducible tensor operator [see {eq}`eq-wigeck-13`], the matrix element vanishes unless $m=m'$.

Consider, for example, the case $n=2$. The four degenerate states include the $2s$ level, with eigenstate $\ket{n\ell m}=\ket{200}$, and the $2p$ level, with eigenstates $\ket{21m}$ for $m=0,\pm1$. According to the selection rules, only the states $\ket{200}$ and $\ket{210}$ are connected by the perturbation. Therefore of the 16 matrix elements in the $4\times4$ matrix, the only nonvanishing ones are

:::{math}
:label: eq-stark-20
\matrixelement{200}{eFz}{210}=-W
:::

and its complex conjugate. This matrix element is easily evaluated by resorting to the hydrogen radial wave functions, given in {ref}`sec-hydrogen-10`. The result is real and negative, so that $W$ defined above is positive. We find

:::{math}
:label: eq-stark-21
W=3eFa_0.
:::

The energy $W$ is of the order of the energy needed to shift the electron from one side of the atom to the other in the external field.

:::{figure} images/stark-fig02.png
:label: fig-stark-2
:width: 80%

The Stark effect splits the $n=2$ level of hydrogen into three levels, of which one is two-fold degenerate.
:::

The $2\times2$ matrix connecting the two states $\ket{200}$ and $\ket{210}$ is

:::{math}
:label: eq-stark-22
\begin{aligned}
\begin{pmatrix}0 & -W \\ -W & 0 \\\end{pmatrix},
\end{aligned}

:::

and its eigenvalues are the first order energy shifts in the $n=2$ level,

:::{math}
:label: eq-stark-23
\Delta E^{(1)}_2 = \pm W.
:::

In addition, the two states $\ket{211}$ and $\ket{21,-1}$ do not shift their energies at first order, so the other two eigenvalues of the matrix {eq}`eq-stark-19` are $\Delta E^{(1)}_2 = 0,0$. The energy shifts are illustrated in {ref}`fig-stark-2`, in which the states $\ket{ \pm W}$ are those with energy shifts $\pm W$. We see that the four-fold degeneracy of the $n=2$ state of hydrogen is only partially lifted at first order in the perturbation, since $\ket{211}$ and $\ket{21,-1}$ remain degenerate at this order.

(sec-stark-11)=

## Explanation of Remaining Degeneracy

We may ask whether this remaining degeneracy is lifted at some higher order of perturbation theory, or whether it persists to all orders. To answer this it is best to look at the exact symmetries of the full, perturbed Hamiltonian $H_0+H_1$, without doing perturbation theory at all.

The unperturbed Hamiltonian, being rotationally invariant, commutes with $\Lvec$ (all three components of angular momentum), but the perturbation is only invariant under rotations about the $z$-axis, so it only commutes with $L_z$. Likewise, the unperturbed Hamiltonian commutes with parity $\pi$, but the perturbation does not, so $\pi$ is not a symmetry of the fully perturbed system. Finally, the unperturbed Hamiltonian is invariant under time reversal $\Theta$; this symmetry is preserved by the perturbation. This takes care of the obvious symmetries of the unperturbed and perturbed systems, but not the extra $SO(4)$ symmetry of hydrogen. We will not go into this in detail, except to mention that some of the extra symmetry present in the unperturbed system persists under the perturbation, a fact that is reflected in the separability of the Schr\"odinger equation for the fully perturbed system in confocal parabolic coordinates. The obvious symmetries, however, are sufficient for understanding the degeneracies of the perturbed system.

Since $H$ and $L_z$ commute, they possess simultaneous eigenspaces that we may denote by $\ES_{Em}$. We consider only the bound states, so the allowed values of $E$ are discrete, and the spectrum of $L_z$ contains only integers $m$ (positive, negative or zero). If $\ket{\psi} \in \ES_{Em}$, then

:::{math}
:label: eq-stark-24
H\ket{\psi}=E\ket{\psi}, \qquad L_z\ket{\psi}=m\hbar\ket{\psi}.
:::

Now consider the state $\Theta\ket{\psi}$. Since $\Theta H=H\Theta$ and $\Theta L_z = -L_z\Theta$, we have

:::{math}
:label: eq-stark-25
\begin{aligned}
H\bigl(\Theta\ket{\psi}\bigr) &= E \bigl(\Theta\ket{\psi}\bigr), \\
L_z\bigl(\Theta\ket{\psi}\bigr) &= -m \hbar\bigl( \Theta\ket{\psi}\bigr), \\

\end{aligned}
:::

that is, $\Theta$ maps $\ket{\psi}$ into another state with the same energy (see {ref}`sec-timerev-16`) but opposite value of $L_z$ (see {eq}`eq-timerev-13`. If $m=0$ this means that both $\ket{\psi}$ and $\Theta\ket{\psi}$ belong to $\ES_{E,m=0}$; they could even be proportional. But if $m\ne0$ then $\Theta\ket{\psi}$ is an eigenket of $H$ and $L_z$ with eigenvalues $E$ and $-m\hbar$ where $-m\ne m$; thus, there must exist an eigenspace of $H$ and $L_z$ with eigenvalues $E$ and $-m\hbar$, that is $\ES_{E,-m}$ exists and $\Theta$ maps $\ES_{Em}$ into $\ES_{E,-m}$.

For $m\ne0$ the spaces $\ES_{Em}$ and $\ES_{E,-m}$ are orthogonal (since the eigenvalues of Hermitian $L_z$ are different), so $\ket{\psi}$ and $\Theta\ket{\psi}$ are linearly independent, and there is a degeneracy in the energy that crosses $m$ values. We see that in systems in which $H$ commutes with both $L_z$ and $\Theta$, the energy eigenstates for which $m\ne0$ are at least two-fold degenerate.

In a little more detail, the map induced by $\Theta$ between $\ES_{Em}$ and $\ES_{E,-m}$ is one-to-one and onto, that is, it is invertible. We see this because $\Theta$, being anti-unitary, maps a set of linearly independent vectors to a set of linearly independent vectors. Since the image of $\ES_{Em}$ under $\Theta$ inside $\ES_{E,-m}$ must fit inside $\ES_{E,-m}$, we must have $\dim\ES_{E,-m} \le \dim\ES_{Em}$. But $\Theta$ also maps $\ES_{E,-m}$ into $\ES_{Em}$, so we must have $\dim\ES_{Em}\le \dim\ES_{E,-m}$. Altogether, this shows that $\ES_{Em}$ and $\ES_{E,-m}$ have the same dimensionality, and thus the energy eigenstates in $\ES_{Em}$ are paired with those of the same energy in $\ES_{E,-m}$. This is just what we see to first order in perturbation theory in {ref}`fig-stark-2`, but now we can conclude that the degeneracy between the states with $m=\pm1$ is exact and persists to all orders.

The same argument applies to any system in which the Hamiltonian commutes with both $L_z$ and $\Theta$. For example, in the theory of the $H_2^+$ molecule, we are interested in the motion of an electron in the field of two protons. If we imagine the protons pinned down at locations $z=\pm a/2$ on the $z$-axis, then the Hamiltonian commutes with both $L_z$ and $\Theta$. Then by the previous argument, all states with $m\ne0$ are at least doublets. In reality, of course, the protons are not pinned down, but rather the molecule is free to vibrate and rotate like a dumbbell. When these effects are included, it is found that the $\pm m$ doublets become split. This is called “$\Lambda$-doubling,” where $\Lambda$ (not $m$) is the standard notation for the magnetic quantum number of the electrons about the axis of a diatomic molecule.

This argument, which we have used to prove the necessity of a degeneracy for $m\ne0$, should not be confused with Kramer's degeneracy, which applies whenever we have a system with an odd number of fermions. In the present calculation, we are ignoring the spin of the electrons, treating them as if they were spinless particles, so Kramer's degeneracy does not apply.

(sec-stark-12)=

## The Perturbed Eigenfunctions

To return to the Stark effect in the $n=2$ levels of hydrogen, we can also work out the perturbed eigenstates. These are linear combinations of the unperturbed eigenstates, with coefficients given by the eigenvectors of the matrix {eq}`eq-stark-22`. Explicitly, we have

:::{math}
\begin{aligned}
\ket{+W} &= {1\over\sqrt{2}} (\ket{200} - \ket{210}),
\end{aligned}
:::

:::{math}
:label: eq-stark-26
\begin{aligned}
\ket{-W} &= {1\over\sqrt{2}} (\ket{200} + \ket{210}).
\end{aligned}
:::

The coefficients in these linear combinations are the same as the coefficients $c_\alpha$ in {eq}`eq-pertth-25`. In the language of {ref}`ch-pertth`, we are determining the projection $P\ket{\psi}$ of the exact eigenstates $\ket{\psi}$ onto the unperturbed eigenspace. This is zeroth order part of the exact eigenstates, since the part orthogonal to the unperturbed eigenspace $Q\ket{\psi}$ is small. Notice that even though the perturbation is small, it has caused large (order unity) changes in the eigenstates.

The perturbed eigenstates are mixtures with equal probabilities of states of opposite parity. The phases are different for the two states $\ket{\pm W}$, causing the charge distribution to be shifted either above or below the origin on the $z$-axis. The energy of the state is either raised or lowered compared to the unperturbed energy, depending on whether the charge distribution has been moved with or against the external field.

(sec-stark-13)=

## The Stark Effect and Radiative Transitions

There is some interesting physics involving radiative transitions and the Stark effect on the $n=2$ levels of hydrogen. In the absence of an external field, the $2p$ level of hydrogen has a lifetime on the order of $10^{-9}$ seconds, before the atom emits a photon and drops into the $1s$ state. But the $2s$ level is metastable, decaying much more slowly, mainly via two photon emission, in about $10^{-1}$ seconds. This makes it easy to create a population of mainly $2s$ and $1s$ states of hydrogen. For example, if we knock a population of hydrogen atoms into mixture of excited states by collisions with an electron beam, then after a short time ($10^{-9}sec\ll t \ll 10^{-1}sec$) everything will have decayed into either the $1s$ state or the metastable $2s$ state.

Now the $2s$ state is a linear combination of the states $\ket{\pm W}$,

:::{math}
:label: eq-stark-27
\ket{200} = {1\over\sqrt{2}} (\ket{+W} + \ket{-W}),
:::

as we easily see from {eq}`eq-stark-26`. This applies even in the absence of an applied electric field, in which case $\ket{200}$ is an energy eigenstate (a stationary state). But in the presence of an applied field, states $\ket{\pm W}$ differ in energy by $2W$, and evolve with different time-dependent phases. Let us imagine that at $t=0$ the system is in the state $\ket{200}$ given by {eq}`eq-stark-27`. Then the probability of finding the system in the state $\ket{210}$ at a later time is

:::{math}
:label: eq-stark-28
\sin^2 (Wt/\hbar),
:::

that is, the system oscillates back and forth between the $2s$ and $2p$ states with frequency $2W/\hbar$. At least, this would be the conclusion if we could turn off the radiative transitions; as it is, however, once the system enters the $2p$ state, it rapidly makes a radiative transition to the $1s$ ground state. The effect of turning on the electric field is to rapidly depopulate the $2s$ state, causing the emission of a burst of photons.

(sec-stark-14)=

## Induced Dipole Moment in the Ground State of Hydrogen

Let us return to the ground state of hydrogen. Although the first order Stark energy shift in this state vanishes, the first order shift in the wave function is nonzero. We see this from {eq}`eq-pertth-24`, which for the present problem is

:::{math}
:label: eq-stark-29
\ket{\psi} = \ket{100} + \sum_{(n\ell m) \ne (100)} \ket{n\ell m} {\matrixelement{n\ell m}{eFz}{100} \over E_1 - E_n}.
:::

Here $\ket{\psi}$ is the perturbed ground state. This state has a nonzero electric dipole moment, unlike the unperturbed ground state. As we say, the ground state of hydrogen does not have any permanent electric dipole moment, but it does have an *induced* dipole moment in the presence of an electric field. For if we compute the expectation value of the dipole operator $\dvec=-e\xvec$ and carry the answer to first order in the perturbation, we find

:::{math}
:label: eq-stark-30
\xpecval{\dvec} = \matrixelement{\psi}{\dvec}{\psi} = \alpha \Fvec,
:::

where the *polarizability* $\alpha$ is given by

:::{math}
:label: eq-stark-31
\alpha = -2e^2\sum_{(n\ell m) \ne (100)} {\matrixelement{100}{z}{n\ell m} \matrixelement{n\ell m}{z}{100} \over E_1-E_n}.
:::

The $x$- and $y$-components vanish in {eq}`eq-stark-30`, and $\alpha$ is positive in {eq}`eq-stark-31` because the energy denominator is negative. We see that in first order perturbation theory there is a linear relationship between the dipole moment of the atom and the applied electric field. The polarizability $\alpha$ is a scalar for the ground state of hydrogen, but more generally (for example, for molecules) it is a tensor that specifies the linear relationship between $\dvec$ and $\Fvec$,

:::{math}
:label: eq-stark-32
d_i = \sum_j \alpha_{ij} \, F_j.
:::

Given the polarizability of a single atom, one can compute the dielectric constant of a gas of the atoms, although for hydrogen under normal circumstances it is unrealistic to speak of a gas of atoms (as opposed to molecules). The calculation is easiest for a dilute gas; at higher densities, one must distinguish between the electric field seen by an individual atom or molecule and the macroscopic, average electric field. A good approximation at intermediate densities is afforded by the Clausius-Mossotti equation. This is an example of how electric susceptibilities can be computed from first principles.

(sec-stark-15)=

## Quadratic Stark Effect in Hydrogen

Since the first order energy shift in the ground state vanishes, it is of interest to compute the second order shift. We invoke {eq}`eq-pertth-23` with necessary changes of notation, to write

:::{math}
:label: eq-stark-33
\Delta E^{(2)}_gnd = \sum_{(n\ell m)\ne(100)} {\matrixelement{100}{eFz}{n\ell m} \matrixelement{n\ell m}{eFz}{100} \over E_1 - E_n} = -{1\over2}\alpha F^2.
:::

We see that the second order energy shift can be expressed in terms of the polarizability. Because the energy shift is proportional to the square of the applied electric field, we speak of the *quadratic Stark effect*. This energy can also be written,

:::{math}
:label: eq-stark-34
\Delta E^{(2)}_gnd = - {1\over 2}\xpecval{\dvec}\cdot\Fvec.
:::

The presence of the $\frac{1}{2}$ in this formula may be puzzling, since we are accustomed to thinking of the energy of a dipole in a field as $-\dvec\cdot\Fvec$. The reason for this factor is that the dipole moment is induced by the external field, and is itself proportional to $\Fvec$; the energy {eq}`eq-stark-34` is the work done on the atom by the external field as it builds up from zero to its maximum value. The usual expression $-\dvec\cdot\Fvec$ is the potential energy of orientation of a dipole of *fixed* strength in a *fixed* electric field.

It is of interest to evaluate the sum {eq}`eq-stark-31`, to obtain a closed form expression for the polarizability $\alpha$. This sum contains an infinite number of terms, and, in fact, it is more complicated than it appears, because the continuum states must also be included (there is an integral over the continuum states as well as a sum over the discrete, bound states). There are various exact methods of evaluating this sum, but we will content ourselves with an estimate. We begin with the fact that the energy levels $E_n$ increase with $n$, so that

:::{math}
:label: eq-stark-35
E_n-E_1 > E_2-E_1 = {3\over8} {e^2\over a_0}.
:::

But this implies that

:::{math}
:label: eq-stark-36
\alpha < {2e^2\over E_2-E_1} \sum_{n\ell m} \matrixelement{100}{z}{n\ell m} \matrixelement{n\ell m}{z}{100}.
:::

We excluded the term $(n\ell m)=(100)$ in {eq}`eq-stark-31`, but we can restore it in {eq}`eq-stark-36` after taking out the constant denominator, since this term vanishes anyway. The result contains a resolution of the identity, so that the sum in {eq}`eq-stark-36` becomes the matrix element,

:::{math}
:label: eq-stark-37
\matrixelement{100}{z^2}{100} = a_0^2.
:::

This gives the estimate

:::{math}
:label: eq-stark-38
\alpha < {16\over3} a_0^3.
:::

An exact treatment of the sum {eq}`eq-stark-31` gives the result,

:::{math}
:label: eq-stark-39
\alpha = {9\over2} a_0^3,
:::

so the exact expression for the second order energy shift is

:::{math}
:label: eq-stark-40
\Delta E^{(2)}_gnd = -{9\over4} F^2 a_0^3.
:::

This energy shift is of the order of the energy of the external field contained in the volume of the atom.

(sec-stark-16)=

## The Case of Nearly Degenerate States

Let us return to the case of a generic, isolated system. As discussed previously the energy multiplets $E_{nj}$ for different values of $(nj)$ do not coincide, so there is no degeneracy between states of opposite parity, and hence, rigorously speaking, no linear Stark effect. But energy multiplets with different $(nj)$ can come very close to one another, a seen for example in the $s$ and $p$ classes of states of sodium in Fig.~\figr\hydrogen.3, which each have an infinite number of states piling up at the continuum limit $E=0$. If the energy difference between multiplets of opposite parity is very small, it is logical on physical grounds that it would not make any difference, and the system should behave as if there were a degeneracy between states of opposite parity. That is, a linear Stark effect should exist.

As for the special case of hydrogen, the exact degeneracy between the $2s$ and $2p$ states is only a feature of the approximation of the spinless, nonrelativistic, electrostatic model {eq}`eq-stark-1`. In real hydrogen, the $2p$ states are split into the $2p_{1/2}$ and $2p_{3/2}$ states, neither of which coincides exactly in energy with the $2s$ state (properly, the $2s_{1/2}$ state). The splitting between the $2s_{1/2}$ and the $2p_{1/2}$ states is particularly interesting; it is due to the interaction of the atomic electron with the quantized electromagnetic field, and is called the *Lamb shift*. Because of the Lamb shift, the $2s_{1/2}$ state actually lies approximately $1.058$ GHz above the $2p_{1/2}$ state.

Thus, in a realistic treatment of hydrogen, there is no degeneracy between states of opposite parity, although the $2s_{1/2}$ and $2p_{1/2}$ levels come very close. Therefore there is, rigorously speaking, no linear Stark effect in the $n=2$ levels of hydrogen either, and the dependence of the energy shift on applied electric fields is always quadratic, at least for weak fields. In stronger fields, however, the Stark energy can overwhelm the small splitting between energy eigenstates of opposite parity, causing mixing between them and resulting in a linear dependence of the energy shift on the applied electric field. That is, at intermediate field strengths, there is a transition from a quadratic dependence to a linear dependence of the energy on the applied field. The field strength at which the transition occurs depends on the energy difference and the matrix elements in question.

These considerations are relevant to the case of *polar* molecules, that is, those that carry a “permanent electric dipole moment.” Examples are heteronuclear diatomic molecules such as CO or HCl. It was explained in {ref}`ch-cenforce`\ that such molecules are examples of central force motion, and how the vibrational and rotational spectrum can be understood in terms of a model of a rigid or nearly rigid rotating dumbbell. Polar molecules are molecules in which there is a charge separation between the two ends of the dumbbell, so that, classically speaking, there is a permanent electric dipole moment. In quantum mechanics, however, we must look at the energy eigenfunctions,

:::{math}
:label: eq-stark-41
\psi_{n\ell m}(\xvec) = R_{n\ell}(r) Y_{\ell m}(\theta,\phi),
:::

where, as explained in {ref}`ch-cenforce`, the radial wave function $R_{n\ell}(r)$ is highly concentrated near the equilibrium radius $r_0$ (at least for small vibrational quantum numbers $n$). Since the parity of these states is $(-1)^\ell$, the actual energy eigenstates of the molecule do not have a permanent electric dipole moment. In effect, the $Y_{\ell m}$ smears the probability distribution over angles in such a way that the permanent dipole moment is averaged to zero.

However, rotational states (for different values of $\ell$) are separated by energies that are typically in the far infrared or microwave range of frequencies, and as $\ell$ increases, the states alternate in parity. So for sufficiently strong applied electric field, there is a strong mixing of rotational states of opposite parity (even and odd $\ell$), and the molecule begins to behave as if it has a permanent electric dipole moment.

\problems

(prob-stark-1)=

**Problem \prbdstark-1..** 

:::{math}
:label: eq-stark-42
\Delta E= 0, \quad \pm\sqrt{A^2 +B^2}, \quad \pm {\sqrt{3}\over2} B,
:::

where $A$ and $B$ are quantities which you must define but which you need not evaluate. Hint: the matrix can be reduced to smaller matrices, of which one is $3\times3$. Do this one first.

Indicate the degeneracies of these levels. Can you guarantee that these degeneracies will persist to all orders of perturbation theory?

(prob-stark-2)=

**Problem \prbdstark-2.} As explained in \secrstark-13, if a hydrogen atom in the $2s_{1/2}$ state is placed in an external electric field, the energy eigenstates become mixtures of the $2s_{1/2}$ and $2p_{1/2}$ states, so as time progresses the amplitude moves out of the metastable $2s_{1/2}$ state and into the $2p_{1/2}$ state, which decays rapidly.  However, due to the Lamb shift, the $2s_{1/2}$ and $2p_{1/2.** 

Use “nearly degenerate perturbation theory” (see \pertth.16) to analyze the effect of an external electric field on the }$2s_{1/2}$ and $2p_{1/2}$ levels of hydrogen. This is not a model calculation like that done in class, where we looked at the Stark effect on the $n=2$ levels of hydrogen in the electrostatic model; rather, we want to know what would happen in real hydrogen. Thus, you should use the fine structure model of hydrogen, including the spin, and take into account the Lamb shift, which suppresses the $2p_{1/2}$ level about 1.06~GHz below the $2s_{1/2}$ level. The $2p_{3/2}$ level is 10.9~GHz above the $2p_{1/2}$ level, and can be ignored for the purpose of this problem. We ignore the hyperfine structure in this problem. See {ref}`sec-finestruc-17` and Fig.~\figr\finestruc.3.

Show that the energy shifts are quadratic in the field strength for small amplitude electric fields, but that they become linear at larger strengths. Thus there is a threshold field strength, call it $F_0$, where the behavior changes from quadratic to linear. Estimate $F_0$ in Volts/cm. Sketch the energy levels as a function of the electric field strength $F$. In the limit $F\gg F_0$, you will obtain a linear relationship between $\Delta E$ and $F$, but it will not be the linear relationship {eq}`eq-stark-21` found above. Explain why. Explain how this problem provides an example of Kramer's degeneracy (and use this fact to cut your work in half).

In this problem you may use {eq}`eq-stark-20`.
