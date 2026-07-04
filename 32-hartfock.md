---
title: "32. The Hartree-Fock Method in Atoms"
---
(ch-hartfock)=

# 32. The Hartree-Fock Method in Atoms

(sec-hartfock-1)=

## Introduction

The Hartree-Fock method is a basic method for approximating the solution of many-body electron problems in atoms, molecules, and solids. With modifications, it is also extensively used for protons and neutrons in nuclear physics, and in other applications. In the Hartree-Fock method, one attempts to find the best multi-particle state that can be represented as a Slater determinant of single particle states, where the criterion for “best” is the usual one in the variational method in quantum mechanics. For the Hartree-Fock method, this means that the expectation value of the energy should be stationary with respect to variations in the single particle orbitals. Hartree-Fock solutions are often used as a starting point for a perturbation analysis, which is capable of giving more accurate approximations. In these notes, we discuss the Hartree-Fock method in atomic physics. Later we will use it as the basis of a perturbation analysis that reveals the basic facts about atomic structure in multielectron atoms.

This is our first excursion into the physics of systems with more than two identical particles, and we will use it as an opportunity to elaborate on the symmetrization postulate in the context of a practical example.

(sec-hartfock-2)=

## The Basic $N$-electron Hamiltonian

The Hamiltonian we wish to solve initially is the nonrelativistic, electrostatic approximation for an atom with $N$ electrons and nuclear charge $Z$. We do not necessarily assume $N=Z$, so we leave open the possibility of dealing with ions. The case $N<Z$ is a positive ion, and $N>Z$ is a negative ion. We know that negative ions exist as bound states, for example, $\\textH^-$ or the common ion $Cl^-$. In atomic units, our Hamiltonian is

:::{math}
:label: eq-hartfock-1
H = \sum_{i=1}^N \Bigl({p_i^2\over 2} -{Z\over r_i}\Bigr) + \sum_{i<j} {1\over r_{ij}}.
:::

This Hamiltonian neglects a number of physical effects, including mass polarization (coming from the finite nuclear mass), fine structure, retardation, hyperfine interactions, radiative corrections, etc. These are all small for atoms near the beginning of the periodic table, but the fine structure terms are of relative order $(Z\alpha)^2$ and so become important near the end of the periodic table. For heavy atoms, the Hamiltonian~{eq}`eq-hartfock-1`, which is fundamentally nonrelativistic, is not a good starting point for atomic structure; instead, it is more useful to begin with a relativistic treatment, based on the Dirac equation. In these notes, we will stick with the Hamiltonian~{eq}`eq-hartfock-1`. Of the various corrections not included in {eq}`eq-hartfock-1`, the spin-orbit terms are particularly notable, because they couple the spatial and spin degrees of freedom. We will have something to say about spin-orbit corrections later. With the neglect of all these corrections, the Hamiltonian {eq}`eq-hartfock-1` is a purely orbital operator. We will call $H$ in {eq}`eq-hartfock-1` the “basic $N$-electron Hamiltonian.”

We break the basic $N$-electron Hamiltonian into two terms, $H=H_1+H_2$, where

:::{math}
:label: eq-hartfock-2
H_1=\sum_i^{N} \left({p_i^2\over 2} - {Z\over r_i}\right),
:::

and

:::{math}
:label: eq-hartfock-3
H_2=\sum_{i<j} {1\over r_{ij}}.
:::

The 1 and 2 subscripts indicate that the two terms involve respectively one- and two-electron operators, that is, operators that involve the coordinates of one or two electrons at a time. There is no implication that $H_2$ is smaller than $H_1$, and we do not intend to treat $H_2$ by perturbation theory. It is true that in helium we treated $H_1$ as an unperturbed Hamiltonian and $H_2$ as a perturbation (there we called them $H_0$ and $H_1$, see {eq}`eq-helium-24a`, and we got results that explained at least the qualitative features of the excited states of helium. But in heavier atoms such an approach is not useful. Instead, in these notes we will treat $H=H_1+H_2$ by the variational method.

(sec-hartfock-3)=

## Good Quantum Numbers

The Hamiltonian {eq}`eq-hartfock-1` has a number of exactly conserved quantities, in addition to the obvious example of $H$ itself. First, the total orbital angular momentum,

:::{math}
:label: eq-hartfock-4
\Lvec = \sum_{i=1}^N \Lvec_i,
:::

is conserved, and therefore also any function of $\Lvec$, of which $L^2$ and $L_z$ are notable because they not only commute with $H$ but also with each other. On the other hand, the orbital angular momenta of the individual electrons $\Lvec_i$ are not conserved, because the inter-electron Coulomb interactions are not invariant under spatial rotations of the individual electron coordinates. Next, the Hamiltonian {eq}`eq-hartfock-1` is a purely spatial operator, and so commutes with any of the individual spin operators, $\Svec_i$, and therefore with any function of these, notably the total spin,

:::{math}
:label: eq-hartfock-5
\Svec = \sum_{i=1}^N \Svec_i,
:::

and the total spin operators $S^2$ and $S_z$. Next, $H$ commutes with parity $\pi$. Finally, $H$ commutes with the operators $E_{ij}$ that exchange the labels of electrons $i$ and $j$. Note that there is one exchange operator for every pair of electrons. More generally, $H$ commutes with permutation operators, which are generalizations of the exchanges. As in helium, we can also define orbital and spin permutation operators, and $H$ commutes with these separately. We will have more to say about exchanges and permutations below. This list of good quantum numbers is basically the same one that we had in the case of helium.

Note that we are talking about the operators that commute with the basic $N$-electron Hamiltonian {eq}`eq-hartfock-1`; when the various corrections are added, some operators are no longer conserved. For example, when the spin-orbit terms are added, we find that neither $\Lvec$ nor $\Svec$ commutes with $H$, but $\Jvec=\Lvec+\Svec$ does. Similarly, with the inclusion of spin-orbit terms, the Hamiltonian no longer commutes with orbital and spin permutations separately, but it still commutes with overall permutations. Going in the other direction, there are cruder approximations than {eq}`eq-hartfock-1` that have higher symmetry; for example, the central field Hamiltonian {eq}`eq-atomstruc-8a` commutes with the individual orbital angular momenta $\Lvec_i$. We will say more about central field Hamiltonians in {ref}`ch-atomstruc`.

These facts follow a general rule, namely, the more idealized an approximation of a physical system, the higher the degree of symmetry, the larger number of conserved quantities and the higher degree of degeneracy in the energy eigenstates. Conversely, more realistic treatments mean lower symmetry, fewer exactly conserved quantities, and splitting of degeneracies.

(sec-hartfock-4)=

## The Idea of Hartree

Hartree developed a variational treatment of multi-electron atoms which we now describe. Hartree's trial wave function is a product of single particle orbitals, one for each electron. The word *orbital* refers to a single-particle wave function, either including or not including spin, depending on the context. Hartree's multiparticle trial wave function is

:::{math}
:label: eq-hartfock-6
\ket{\Phi_H}=\ket{1}^{(1)} \ket{2}^{(2)} \ldots \ket{N}^{(N)},
:::

where the $H$ subscript means “Hartree.” In this notation, the parenthesized numbers attached to the kets are electron labels, while the numbers inside the kets are orbital labels. Thus, we have in mind $N$ electrons that are assigned to $N$ orbitals in some way.

In the following we will attempt to use Latin indices $i,j, \ldots = 1, \ldots N$ to label electrons, and Greek indices $\lambda, \mu, \ldots = 1, \ldots, N$ to label orbitals. This is convenient to keep track of the two different kinds of objects that are being labeled.

The orbitals $\ket{\lambda}$ in Hartree's trial wave function are assumed to be the product of a spatial part $\ket{u_\lambda}$ times a spin part $\ket{m_{s\lambda}}$,

:::{math}
:label: eq-hartfock-7
\ket{\lambda}=\ket{u_\lambda}\ket{m_{s\lambda}}.
:::

The spin part is assumed to be an eigenstate of $S_z$ for the individual electron, with eigenvalue

:::{math}
:label: eq-hartfock-8
m_{s\lambda}=\pm\frac{1}{2},
:::

where a definite value of $m_{s\lambda}$ is assigned to each orbital. This amounts to making Hartree's trial wave function $\ket{\Phi_H}$ an eigenstate of each of the operators $S_{iz}$ for each of the electrons. There is no loss of generality in this, since the Hamiltonian~{eq}`eq-hartfock-1` commutes with each of the operators $S_{iz}$, which also commute with each other. As for the spatial part of each orbital, it is associated with a wave function on three-dimensional space by

:::{math}
:label: eq-hartfock-9
u_\lambda(\rvec) = \braket{\rvec}{u_\lambda}.
:::

In Hartree's theory the variational parameters are the spatial parts of the single particle orbitals, $u_\lambda(\rvec)$, that is, the entire functions. Thus, Hartree's variational calculation gives the best multiparticle wave function for the atom that can be written as the product of single particle wave functions of definite spin, where “best” means lowest energy. Recall that in helium we did a variational calculation in which the effective nuclear charge, a single number, was the variational parameter. In Hartree's method, the variational parameters are a set of $N$ functions on three-dimensional space. This is considerably more sophisticated than what we did in the case of helium, since there are effectively an infinite number of variational parameters.

In the variational method one can use any trial wave function one wishes, but the answers will usually not be very good unless some physical or other kind of reasoning indicates that the trial wave function is close to the true ground state. In the case of the Hartree method, the basic physical idea is that in a multielectron atom, each electron sees an effective potential produced by the nucleus and the average effects of the other electrons. This is the idea behind “screening.” If we imagine that this effective potential is the same potential $V(\rvec)$ for all the electrons, then the multiparticle Hamiltonian~{eq}`eq-hartfock-1` is approximated by

:::{math}
:label: eq-hartfock-10
H=\sum_{i=1}^N \biggl( {p_i^2 \over 2} + V(\rvec_i)\biggr),
:::

that is, it is the sum of $N$ identical single particle Hamiltonians, one for each particle. The eigenfunctions of such a multiparticle Hamiltonian are products of single particle eigenfunctions of the single particle Hamiltonian in {eq}`eq-hartfock-10`, that is, they have the form of Hartree's trial wave function.

There are, however, two complications in this basic picture. One is that each electron sees an effective potential produced by the nucleus and the *other* electrons, not *itself*. Thus, there is really a different effective potential for each electron. If we replace the common potential $V(\rvec_i)$ in {eq}`eq-hartfock-10` by $V_i(\rvec_i)$, a potential that depends on the electron in question, then the eigenfunctions of $H$ in {eq}`eq-hartfock-10` are still products of single particle wave functions, but each will be the eigenfunction of a different single-particle Hamiltonian.

The second complication is the symmetrization postulate, which requires the multielectron state to be antisymmetric under exchange. Notice that Hartree's trial wave function does not satisfy the symmetrization postulate. We will see how these issues play out as we develop the theory in more detail.

(sec-hartfock-5)=

## Hartree's Energy Functional

We now apply the variational method to the basic $N$-electron Hamiltonian {eq}`eq-hartfock-1`, using Hartree's trial wave function {eq}`eq-hartfock-6`. The results are not entirely satisfactory, since Hartree's trial wave function does not satisfy the requirements of the symmetrization postulate, but we do the calculation anyway because it is somewhat simpler than the Hartree-Fock calculation that follows and because it illustrates some of the technical aspects that will be useful later. Hartree's variational calculation is also interesting physically.

We require the expectation value of the Hamiltonian~{eq}`eq-hartfock-1` with respect to Hartree's trial wave function~{eq}`eq-hartfock-6`. In the following we will assume that the single particle orbitals making up Hartree's trial wave function are normalized,

:::{math}
:label: eq-hartfock-11
\braket{\lambda}{\lambda} =1.
:::

As we explain later, this condition is enforced by means of Lagrange multipliers.

We begin with the one-electron operator $H_1$ in {eq}`eq-hartfock-2`, which we write as

:::{math}
:label: eq-hartfock-12
H_1 = \sum_{i=1}^N h_i,
:::

where

:::{math}
:label: eq-hartfock-13
h_i = {p_i^2 \over 2} - {Z \over r_i}.
:::

The operator $h_i$ involves only the position and momentum of particle $i$. Then we can write the required expectation value as

:::{math}
:label: eq-hartfock-14
\matrixelement{\Phi_H}{H_1}{\Phi_H} = \sum_{i=1}^N \bra{1}^{(1)} \bra{2}^{(2)} \ldots \bra{N}^{(N)} \; h_i \; \ket{1}^{(1)} \ket{2}^{(2)} \ldots \ket{N}^{(N)}.
:::

To understand the matrix elements in the sum, let us take the special case $i=2$. Since the operator $h_2$ only involves the position and momentum of particle 2, it is “transparent” to all the bras on the left and kets on the right that involve particles other than particle 2. Because of the normalization condition~{eq}`eq-hartfock-11`, these bras and kets combine together to give unity, and only the matrix element

:::{math}
:label: eq-hartfock-15
\bra{2}^{(2)} \; h_2 \; \ket{2}^{(2)}
:::

remains. By this example we see that the sum~{eq}`eq-hartfock-14` becomes

:::{math}
:label: eq-hartfock-16
\matrixelement{\Phi_H}{H_1}{\Phi_H} = \sum_{i=1}^N \bra{i}^{(i)} \; h_i \; \ket{i}^{(i)},
:::

which is nice because we have reduced the multiparticle matrix element to a sum of single particle matrix elements. However, matrix elements in the sum violate our rule of using Latin indices $i,j$ to label particles and Greek indices $\lambda,\mu$ to label orbitals. We can fix this by rewriting {eq}`eq-hartfock-16` in the form

:::{math}
:label: eq-hartfock-17
\matrixelement{\Phi_H}{H_1}{\Phi_H} = \sum_{\lambda=1}^N \bra{\lambda}^{(i)} \; h_i \; \ket{\lambda}^{(i)},
:::

where we add the condition that $i=\lambda$.

Now we can write out the single particle matrix elements explicitly in terms of the unknown orbitals $u_\lambda(\rvec)$. Since $h_i$ is a purely spatial operator, the spin parts of $\bra{\lambda}$ and $\ket{\lambda}$ in {eq}`eq-hartfock-17` combine to give unity, and the matrix element is just a spatial integral,

:::{math}
:label: eq-hartfock-18
\bra{\lambda}^{(i)} \; h_i \; \ket{\lambda}^{(i)} = \int d^3\rvec_i \; u^\cc_\lambda(\rvec_i) \left( {p_i^2\over 2} - {Z\over r_i} \right) u_\lambda(\rvec_i),
:::

where we integrate over $\rvec_i$, the coordinates of particle $i$. But this variable $\rvec_i$ is obviously just a dummy variable of integration, which we can replace simply by $\rvec$. Altogether, we can write {eq}`eq-hartfock-17` in the form

:::{math}
:label: eq-hartfock-19
\matrixelement{\Phi_H}{H_1}{\Phi_H} = \sum_{\lambda=1}^N I_\lambda,
:::

where

:::{math}
:label: eq-hartfock-20
I_\lambda=\int d^3\rvec \; u^\cc_\lambda(\rvec) \left( {p^2\over 2} - {Z\over r} \right) u_\lambda(\rvec).
:::

The energy of the Hartree state involves the sum of the average kinetic energy of the single particle orbitals plus their potential energy of interaction with the nucleus. It is reasonable that such terms should appear.

Next we consider the expectation value of the two-electron operator $H_2$ of {eq}`eq-hartfock-3` with respect to the Hartree trial wave function~{eq}`eq-hartfock-6`. As above, we can write this as a sum of multiparticle matrix elements,

:::{math}
:label: eq-hartfock-21
\matrixelement{\Phi_H}{H_2}{\Phi_H} = \sum_{i<j} \bra{1}^{(1)} \bra{2}^{(2)} \ldots \bra{N}^{(N)} \; {1\over r_{ij}} \; \ket{1}^{(1)} \ket{2}^{(2)} \ldots \ket{N}^{(N)}.
:::

Again, to take an example, consider the term $i=2$, $j=3$. Then all the bras and kets for electrons other than electrons 2 and 3 combine together to give unity, due to the normalization~{eq}`eq-hartfock-11`, leaving a two-particle matrix element,

:::{math}
:label: eq-hartfock-22
\bra{2}^{(2)} \bra{3}^{(3)} \; {1\over r_{23}} \; \ket{2}^{(2)} \ket{3}^{(3)}.
:::

By this example we see that the expectation value can be written,

:::{math}
:label: eq-hartfock-23
\matrixelement{\Phi_H}{H_2}{\Phi_H} = \sum_{i<j} \bra{i}^{(i)} \bra{j}^{(j)} \; {1\over r_{ij}} \; \ket{i}^{(i)} \ket{j}^{(j)}= \sum_{\lambda<\mu} \bra{\lambda}^{(i)} \bra{\mu}^{(j)} \; {1\over r_{ij}} \; \ket{\lambda}^{(i)} \ket{\mu}^{(j)},
:::

where in the final sum we switch to Greek indices for orbitals and add the conditions $i=\lambda$ and $j=\mu$.

In the final matrix elements in {eq}`eq-hartfock-23` the bra $\bra{\lambda}^{(i)}$ and ket $\ket{\lambda}^{(i)}$ for particle $i$ have the same spinor attached to them, and the operator in the middle is a purely spatial operator. Thus, the spin scalar product just gives unity, and the matrix element reduces to a spatial integration insofar as the coordinates of particle $i$ are concerned. The same is true for particle $j$. We denote the matrix element in question by $J_{\lambda\mu}$, which we write out as an integral over the coordinates of particles $i$ and $j$,

:::{math}
:label: eq-hartfock-24
J_{\lambda\mu} = \int d^3\rvec_i \, d^3\rvec_j \; u^\cc_\lambda(\rvec_i) u^\cc_\mu(\rvec_j) \, {1\over r_{ij}} \, u_\lambda(\rvec_i) u_\mu(\rvec_j).
:::

But the variables of integration, $\rvec_i$ and $\rvec_j$, are just dummies, and we can rewrite this in the form,

:::{math}
:label: eq-hartfock-25
J_{\lambda\mu}=\int d^3\rvec \, d^3\rvec' \; {|u_\lambda(\rvec)|^2 |u_\mu(\rvec')|^2 \over |\rvec-\rvec'|}.
:::

Finally, we can write the expectation value of $H_2$ as

:::{math}
:label: eq-hartfock-26
\matrixelement{\Phi_H}{H_2}{\Phi_H} = \sum_{\lambda<\mu} J_{\lambda\mu}.
:::

The integrals $J_{\lambda\mu}$ are examples of “direct” integrals of the type we saw earlier in our perturbation treatment of the excited states of helium. Only the case $\lambda\ne\mu$ occurs in the calculation above. The physical interpretation of $J_{\lambda\mu}$ for $\lambda\ne\mu$ is that it is the mutual electrostatic energy of interaction of the two electron clouds associated with orbitals $u_\lambda(\rvec)$ and $u_\mu(\rvec)$, that is, it is the energy required to move these two clouds rigidly from infinite separation to their final position in the atom. Since the clouds are negatively charged they repel one another, and the required energy is positive. This is also obvious from {eq}`eq-hartfock-25`, since the integrand is strictly positive.

Also, the physical interpretation of $J_{\lambda\mu}$ makes it clear that it must be symmetric in the two indices,

:::{math}
:label: eq-hartfock-27
J_{\lambda\mu}=J_{\mu\lambda},
:::

which also follows from the integral~{eq}`eq-hartfock-23` by swapping the variables $\rvec$, $\rvec'$ of integration. Because of this symmetry, the expectation value of $H_2$ can be written,

:::{math}
:label: eq-hartfock-28
\matrixelement{\Phi_H}{H_2}{\Phi_H} = {1\over 2} \sum_{\lambda \ne \mu} J_{\lambda\mu},
:::

which is more convenient for later work. The omission of the diagonal terms $\lambda=\mu$ means that the self-energies of the electron clouds are not counted in the Hartree energy functional. The self-energy for orbital $\lambda$ would be $(1/2)J_{\lambda\lambda}$, which according to standard electrostatics is the energy required to bring together infinitesimal charges from infinity to form the charge cloud $|u_\lambda(\rvec)|^2$. Of course, this notion takes no account of the indivisible quantum of electric charge $e$. It is physically plausible that the mutual energies of the electron clouds should occur in the energy functional, but not the self-energies.

Altogether, we can write the expectation value for the energy in Hartree's theory as

:::{math}
:label: eq-hartfock-29
E[\Phi_H] = \matrixelement{\Phi_H}{H}{\Phi_H} = \sum_{\lambda=1}^N I_\lambda + {1\over 2} \sum_{\lambda \ne \mu} J_{\lambda\mu}.
:::

This expectation value is regarded as a functional of Hartree's multiparticle state, as indicated, or, equivalently, of the set of single particle orbitals $\{u_\lambda(\rvec)\}$.

(sec-hartfock-6)=

## The Hartree Equations

The Hartree state $\ket{\Phi_H}$ is not normalized unless we impose some constraints to make this so. See {ref}`sec-variational-5`, where we used a Lagrange multiplier to enforce normalization in a family of trial wave functions. The easiest way to do this is to require the single particle orbitals to be normalized as indicated by {eq}`eq-hartfock-11`. The spin parts of the orbitals $\ket{\lambda}$ are already normalized, so the normalization condition reduces to a spatial integral,

:::{math}
:label: eq-hartfock-30
\int d^3\rvec \, u_\lambda^\cc(\rvec) u_\lambda(\rvec) = 1.
:::

Thus there are really $N$ constraints, one for each orbital. Denoting the corresponding Lagrange multipliers by $\epsilon_\lambda$, we subtract the Lagrange multiplier term from the functional $E[\Phi_H]$ in {eq}`eq-hartfock-29` to obtain a modified functional,

:::{math}
:label: eq-hartfock-31
F[\Phi_H] = \sum_{\lambda=1}^N I_\lambda + {1\over 2} \sum_{\lambda \ne \mu} J_{\lambda\mu} - \sum_{\lambda=1}^N \epsilon_\lambda ( \braket{\lambda}{\lambda}-1).
:::

This functional is required to be stationary with respect to arbitrary variations in the unknown single particle wave functions, $u_\lambda(\rvec)$. These wave functions are generally complex, so arbitrary variations consist of independent arbitrary variations in the real and imaginary parts. But varying the real and imaginary parts independently is equivalent to varying the wave function and its complex conjugate independently; therefore we require the vanishing of two functional derivatives,

:::{math}
:label: eq-hartfock-32
{\delta F[\Phi_H] \over \delta u_\lambda(\rvec)} =0, \qquad {\delta F[\Phi_H] \over \delta u^\cc_\lambda(\rvec)} = 0.
:::

The second of these equations leads to the Hartree equations in their usual form, and the first to the complex conjugate of those equations; therefore it suffices to work with the second equation only.

Carrying out the required functional derivative, we obtain the Hartree equations,

:::{math}
:label: eq-hartfock-33
\left( {p^2\over2} -{Z\over r} \right) u_\lambda(\rvec) +V_\lambda(\rvec) u_\lambda(\rvec) = \epsilon_\lambda u_\lambda(\rvec),
:::

where

:::{math}
:label: eq-hartfock-34
V_\lambda(\rvec) = \sum_{\mu \ne \lambda} \int d^3\rvec' \, {|u_\mu(\rvec')|^2 \over |\rvec-\rvec'|}.
:::

The Hartree equations~{eq}`eq-hartfock-33` have the form of a set of pseudo-Schr\"odinger equations for the orbitals $u_\lambda(\rvec)$, in which the Lagrange multiplier $\epsilon_\lambda$ plays the role of an eigenvalue. The potential energy includes the potential of the nucleus, $-Z/r$, as well as the potential $V_\lambda(\rvec)$. The latter is physically the electrostatic potential produced at field point $\rvec$ by the charge clouds of all the other orbitals $\mu \ne \lambda$, as may be seen from {eq}`eq-hartfock-34`. The exclusion of the orbital $\lambda$ from this sum is what makes the sum depend on $\lambda$; the electron with orbital $\lambda$ is not acted upon by its own charge cloud. This corresponds to the exclusion of the self-energies from the energy functional. Thus, there is a different potential $V_\lambda$ for each orbital $\lambda$. The potential $V_\lambda$ can only be known when all the other orbitals $u_\mu(\rvec)$ for $\mu \ne \lambda$ are known. But each of these orbitals also satisfies a Hartree equation, so in fact what we have in {eq}`eq-hartfock-33` is a system of $N$ coupled, nonlinear, integro-differential equations.

In spite of their mathematical complexity, however, the Hartree equations {eq}`eq-hartfock-34` are quite clear physically: Each electron moves in the average field produced by all the other electrons. Sometimes one speaks of the *self-consistent field*, that is, the Hartree orbitals $u_\lambda(\rvec)$ are eigenfunctions of potential energies that depend on those orbitals themselves. The Hartree equations are an example of a *mean field theory*, in which one particle is assumed to move in the average field produced by the other particles. Mean field theories are common in many-body physics and in statistical mechanics.

Since the potentials in the Hartree theory are not known until the orbitals are known, the Hartree equations cannot be solved by the usual methods of solving the Schr\"odinger equation (in a given potential). Instead, the usual procedure is to use a method of iteration. First one makes a guess for the orbitals $u_\lambda(\rvec)$, for example, they might be taken as the eigenfunctions of the Thomas-Fermi potential for an atom of given $Z$ and $N$. From these, the potentials $V_\lambda(\rvec)$ are computed by {eq}`eq-hartfock-34`, and then the $N$ Schr\"odinger equations with potentials $V_\lambda(\rvec)$ are solved for the eigenfunctions $u_\lambda(\rvec)$. These are then used to compute new potentials $V_\lambda(\rvec)$, etc., until the procedure converges.

As described, this procedure requires one to solve fully three-dimensional Schr\"odinger equations, since the potentials $V_\lambda(\rvec)$ are generally not rotationally invariant. It is not easy to solve wave equations in three dimensions, and even with modern computers one would prefer not to do it if possible. To avoid this, Hartree suggested that once the potentials $V_\lambda(\rvec)$ were computed from the orbitals, they be averaged over angles to produce a central field potential,

:::{math}
:label: eq-hartfock-35
{\bar V}_\lambda(r) = {1\over 4\pi} \int d\Omega \, V_\lambda(\rvec),
:::

where as indicated the averaged potential ${\bar V}_\lambda$ only depends on the radius $r$. This is of course an additional approximation, which degrades the accuracy of the method. With this modification, Hartree's method requires only the solution of a radial equation, a much easier task than solving a three-dimensional equation.

Since each of the Hartree orbitals $u_\lambda(\rvec)$ is an eigenfunction of a Schr\"odinger operator with its own potential $V_\lambda(\rvec)$, the different orbitals are not orthogonal to one another,

:::{math}
:label: eq-hartfock-36
\braket{\lambda}{\mu} \ne \delta_{\lambda\mu}, \qquad \lambda \ne \mu.
:::

That is, they are eigenfunctions of different single-particle Hamiltonians. The orbitals are normalized, $\braket{\lambda}{\lambda}=1$, but not orthogonal to one another.

The energy associated with the solutions of the Hartree equations, that is, the energy we minimized in deriving those equations, is just the energy functional~{eq}`eq-hartfock-29` evaluated at the Hartree wave function. You might suppose that the eigenvalues $\epsilon_\lambda$ are somehow the energies of the individual electrons, and that if we add them up we would get the energy of the multielectron state. But this is not so, for if we multiply the Hartree equation {eq}`eq-hartfock-33` by $u_\lambda^\cc(\rvec)$ and integrate, we obtain

:::{math}
:label: eq-hartfock-37
I_\lambda + \sum_{\mu \ne \lambda} J_{\lambda\mu} = \epsilon_\lambda.
:::

Now summing this over $\lambda$ and using {eq}`eq-hartfock-29`, we find

:::{math}
:label: eq-hartfock-38
E[\Phi_H] = \sum_{\lambda=1}^N \epsilon_\lambda - {1\over 2} \sum_{\lambda \ne \mu} J_{\lambda\mu}.
:::

It is the energy $E[\Phi_H]$ that is the estimate (an upper bound, actually) to the ground state energy of the atom.

The Hartree orbitals and the estimated energy of the ground state of the atom do not depend on the assignment of the spins $m_{s\lambda}$ to the orbitals. We expect energies to depend on spin in multielectron systems for the reasons we saw in the case of helium: The spin state affects the spatial state because of the requirements of the symmetrization postulate, and the spatial state affects the energy because of Coulomb interactions. Naturally we do not see any of this in the Hartree theory, because Hartree's trial wave function does not satisfy the symmetrization postulate. This is the main defect of this trial wave function. To remedy it, Fock modified Hartree's trial wave function shortly after Hartree's results were announced, producing what is now called Hartree-Fock theory.

(sec-hartfock-7)=

## The Hartree-Fock Trial Wave Function

Fock's trial wave function is an antisymmetrized version of Hartree's; we will denote it by $\ket{\Phi}$, without the $H$ subscript. Like Hartree's trial wave function, that of Fock is specified by a set of single particle orbitals with definite value of spin as in {eq}`eq-hartfock-7` and {eq}`eq-hartfock-9`, but the electrons are permuted among the orbitals in all $N!$ possible ways and a linear combination of the $N!$ terms is made with plus or minus signs, depending on whether the permutation is even or odd. The result is conveniently expressed as a so-called *Slater determinant*,

:::{math}
:label: eq-hartfock-39
\begin{aligned}
\ket{\Phi}={1\over \sqrt{N!}} \left| \begin{matrix} \ket{1}^{(1)} & \ket{2}^{(1)} & \ldots & \ket{N}^{(1)}\\  \ket{1}^{(2)} & \ket{2}^{(2)} & \ldots & \\  \vdots & \vdots & \ddots & \vdots \\  \ket{1}^{(N)} & & \ldots & \ket{N}^{(N)} \\\end{matrix} \right|.
\end{aligned}

:::

The prefactor $1/\sqrt{N!}$ is a normalization constant. The determinant may be expanded by the definition of a determinant, producing the $N!$ terms with plus and minus signs mentioned above. The signs and the sum over permutations guarantee that the Hartree-Fock state satisfies the symmetrization postulate, something we will discuss in more detail below.

Apart from the antisymmetrization, the basic idea of the Hartree-Fock method is the same as that of the Hartree method. Both methods are variational; the Hartree-Fock method determines the best estimate to the ground state wave function of the atom within the class of multiparticle wave functions that are properly antisymmetrized products of single particle wave functions.

A Slater determinant is not so much specified by the single particle orbitals $\ket{\lambda}$ that make it up, as by the $N$-dimensional subspace of the single-particle Hilbert space that is spanned by these orbitals. First note that if the orbitals are linearly dependent, then the Slater determinant vanishes (since its columns are linearly dependent). Thus, if we want an nonzero Slater determinant, the single particle orbitals must be linearly independent. This means that they span an $N$-dimensional subspace of the single particle Hilbert space (they form a basis in this subspace). Next we define new orbitals $\ket{\lambda'}$ that are nonsingular linear combinations of the old orbitals,

:::{math}
:label: eq-hartfock-40
\ket{\lambda'} = \sum_\lambda \ket{\lambda} C_{\lambda\lambda'}
:::

where $C$ is an $N\times N$ matrix with $\det C \ne 0$. Then forming a Slater determinant $\ket{\Phi'}$ from the new orbitals, we have

:::{math}
:label: eq-hartfock-41
\ket{\Phi'} = (\det C) \ket{\Phi}.
:::

The new multiparticle state $\ket{\Phi'}$ is proportional to the old one, and hence specifies the same state physically.

The variational method will optimize the multiparticle state $\ket{\Phi}$ (it will minimize the energy), but in view of {eq}`eq-hartfock-41` it cannot be expected to produce unique answers for the single particle orbitals $\ket{\lambda}$ unless some extra conditions are imposed. In the following we will narrow the possibilities for the single particle orbitals by requiring them to be orthonormal,

:::{math}
:label: eq-hartfock-42
\braket{\lambda}{\mu} = \delta_{\lambda\mu} = \delta(m_{s\lambda},m_{s\mu}) \int d^3\rvec\, u_\lambda^\cc(\rvec) u_\mu(\rvec).
:::

There is no loss of generality in this, because it is always possible to choose an orthonormal basis in the $N$-dimensional space spanned by the single particle orbitals. This still does not uniquely specify the single particle orbitals, because they can always be rotated by a unitary transformation (for which $\det C$ is a phase factor), but it is a convenient assumption. Recall that in the Hartree theory, the single particle orbitals could not be orthonormal.

With this normalization condition, it follows that the state $\ket{\Phi}$ defined by {eq}`eq-hartfock-39` is normalized,

:::{math}
:label: eq-hartfock-43
\braket{\Phi}{\Phi}=1,
:::

that is, with the normalization factor $1/\sqrt{N!}$. See Prob.~\prbrhartfock-1.

(sec-hartfock-8)=

## Mathematical Properties of Permutations

We now make a digression into the subjects of permutations and the symmetrization postulate, which are raised by our use of Slater determinants as a trial wave function. In the process we will give some attention to bosons as well as fermions. We begin with the mathematical properties of permutations.

A *permutation* is defined as an invertible mapping of the set of the first $N$ integers onto itself,

:::{math}
:label: eq-hartfock-44
P:\{1,\ldots, N\} \to \{1,\ldots,N\}.
:::

Since the mapping is invertible, it maps each integer in the set into a unique integer in the same set; thus, it amounts to a rearrangement of the integers in the set. The number of distinct permutations acting on the set $\{1,\ldots,N\}$ is just the number of ways of rearranging the $N$ integers, namely, $N!$.

One way to specify a permutation is just to tabulate the values of the function $P$, which we denote by $P_n$ or $P(n)$. For example, in the case $N=3$, we might have


Equivalently, we may tabulate the function horizontally,

:::{math}
:label: eq-hartfock-46
\begin{aligned}
P=\begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \\\end{pmatrix},
\end{aligned}

:::

where the first row contains $n$ and the second $P(n)$.

The set of permutations satisfies the definition of a group. First, the identity permutation exists; it is just the identity function, $P(n)=n$. Second, by their definition, permutations are invertible. Third, permutations can be multiplied. If $P$ and $Q$ are two permutations, then the product $PQ$ is the composition of the two functions, that is,

:::{math}
:label: eq-hartfock-47
(PQ)(n) = P(Q(n)).
:::

This product is another permutation. The multiplication of permutations is associative, but not in general commutative. The group of permutations of the first $N$ integers has $N!$ elements.

A special kind of permutation is an *exchange*, which swaps two integers and leaves the rest alone. The idea and notation are clear enough from an example (in the case $N=5$),

:::{math}
:label: eq-hartfock-48
\begin{aligned}
E_{24} = \begin{pmatrix}1 & 2 & 3 & 4 & 5 \\ 1 & 4 & 3 & 2 & 5 \\\end{pmatrix}.
\end{aligned}

:::

Not every permutation is an exchange, but every permutation can be written as a product of exchanges. For example, the permutation

:::{math}
:label: eq-hartfock-49
\begin{aligned}
P=\begin{pmatrix}1 & 2 & 3 & 4 \\ 3 & 4 & 2 & 1 \\\end{pmatrix}
\end{aligned}

:::

can be factored as follows, where we show the mappings of successive permutations horizontally:

:::{math}
:label: eq-hartfock-50
\begin{aligned}
\begin{matrix}   & E_{13} &&  E_{24} && E_{12}\\ 1 & \longrightarrow & 3 & \longrightarrow & 3 & \longrightarrow & 3\\ 2 & \longrightarrow & 2 & \longrightarrow & 4 & \longrightarrow & 4\\ 3 & \longrightarrow & 1 & \longrightarrow & 1 & \longrightarrow & 2\\ 4 & \longrightarrow & 4 & \longrightarrow & 2 & \longrightarrow & 1\\\end{matrix}
\end{aligned}

:::

The first permutation puts the 3 in the right final position, the second the 4, and the last one, the 1 and 2. Thus, the $P$ in {eq}`eq-hartfock-49` can be written,

:::{math}
:label: eq-hartfock-51
P=E_{12} E_{24} E_{13}.
:::

The decomposition of a permutation into a product of exchanges is not unique, but the number of exchanges required is always either even or odd. Therefore we can define the *parity* of a permutation as the quantity $+1$ for an even permutation, and $-1$ for an odd one. We will denote this quantity by $(-1)^P$. For example, the permutation in {eq}`eq-hartfock-49` is odd, since there are 3 exchanges in {eq}`eq-hartfock-51`. A basic fact about permutations is that the parity of a product of permutations is the product of the parities, or,

:::{math}
:label: eq-hartfock-52
(-1)^{P} (-1)^{Q} = (-1)^{PQ}.
:::

This follows easily by factoring $P$ and $Q$ into exchanges; the number of exchanges in $PQ$ is the sum of the numbers of exchanges in $P$ and $Q$.

(sec-hartfock-9)=

## Permutation Operators in Quantum Mechanics

In general, a quantum system may consist of one or more species of identical particles, for example, the protons and neutrons in a nucleus. In nonrelativistic quantum mechanics, the numbers of particles of each species are fixed. The case of photons is somewhat special; photons of course travel at the speed of light, and in that sense are always relativistic. But since they are massless they are easily created and destroyed in interactions with nonrelativistic matter, so it is often desirable to treat with them within a formalism that is otherwise nonrelativistic. In the following we will ignore the case of photons, and think of a nonrelativistic quantum system with fixed numbers of massive particles of different species. We treat this system with the wave function or ket formalism we have developed so far in this course (not field theory). It then is possible to define operators that permute the particles within the different classes of identical particles. These are associated with the mathematical permutations defined above, but are operators that act on the Hilbert space of the quantum system. For simplicity we take the case of a system with just one species of $N$ identical particles (the case relevant to our treatment of the electrons in an atom); the generalization to more than one species is trivial.

Let $\{\ket{X}\}$ be a basis in the single particle Hilbert space. Such a basis always exists. The index $X$ may stand for a collection of quantum numbers, for example, $(n,\ell,m_\ell,m_s)$. Then the $N$-particle Hilbert space possesses the basis,

:::{math}
:label: eq-hartfock-53
\ket{X_1}^{(1)} \ket{X_2}^{(2)} \ldots \ket{X_N}^{(N)},
:::

where the list $(X_1,X_2, \ldots, X_N)$ runs over all combinations of $N$ indices of the single particle basis, and the numbers in parentheses label the particles. See also {ref}`sec-jjcouple-2`. Now let $P$ be a permutation, and define the action of an operator $U(P)$ on the multiparticle basis states by

:::{math}
:label: eq-hartfock-54
U(P)\ket{X_1}^{(1)} \ket{X_2}^{(2)} \ldots \ket{X_N}^{(N)} = \ket{X_{P_1}}^{(1)} \ket{X_{P_2}}^{(2)} \ldots \ket{X_{P_N}}^{(N)}.
:::

By linearity, this definition can be extended to arbitrary vectors of the multiparticle Hilbert space. One can show that the resulting operator is actually independent of the basis in the single particle Hilbert space that was used in its definition. One can also show that this operator $U(P)$ preserves the norm of all states, and hence is unitary. {eq}`eq-hartfock-54` is obviously a generalization of {eq}`eq-identpart-12`, which applied to the case of two identical particles.

The definition {eq}`eq-hartfock-54` has the consequence that the unitary operators $U(P)$ reproduce the multiplication law of the permutations themselves, in the following sense:

:::{math}
:label: eq-hartfock-55
U(P) U(Q) = U(QP).
:::

[If it is desired that the right-hand side of this equation should be $U(PQ)$, so that the unitary operators form a representation of the permutations, then $P$ on the left-hand side of {eq}`eq-hartfock-54` can be replaced by $P^{-1}$. This would not change any of the main conclusions presented in these notes, but it would complicate the presentation slightly.]

We will henceforth for simplicity write $P$ for the unitary operators $U(P)$, since there will be little danger of confusion.

(sec-hartfock-10)=

## Permutation Operators and the Symmetrization Postulate

We stated the symmetrization postulate in {ref}`ch-identpart`\ in terms of the properties of wave functions when identical particles are exchanged. Exchange operators are special cases of permutation operators, which we have just defined. Since a permutation can be factored into a product of exchanges, we can now state the symmetrization postulate in a different and somewhat more general manner. Namely, let $\ket{\Psi}$ be a multiparticle state of a system consisting of $N$ identical particles. Then the multiparticle states that are physically allowed are those that satisfy

:::{math}
:label: eq-hartfock-56
\begin{aligned}
P\ket{\Psi} = \begin{cases} + \ket{\Psi}, & bosons, \\ (-1)^P \ket{\Psi}, & fermions. \\\end{cases}
\end{aligned}

:::

In the wave function or ket formalism we have been using up to this time in this course, it is impossible to write down a multiparticle state for identical particles without labeling the particles. You will see that the definition of the permutation operators above required us to label the particles. One of the consequences of the symmetrization postulate, however, is that no physics depends on this labeling. For example, in the Hartree-Fock trial wave function {eq}`eq-hartfock-39`, the individual orbitals are assigned definite values of spin (up or down). But we cannot say that electron 1, for example, has a definite spin, since the Slater determinant permutes all electrons among all the orbitals. It is meaningful to say how many electrons are spin up and how many spin down, but not which ones are which.

Another aspect of the present formalism is that it is possible to write down multiparticle states that are not physical at all, since they do not satisfy the symmetrization postulate. In fact, we should not even call them “states,” since they are just mathematical wave functions without physical meaning. They may be useful for mathematical purposes, however, as we saw with Hartree's trial wave function {eq}`eq-hartfock-6`. Thus, we may speak of the “nominal Hilbert space” consisting of all multiparticle wave functions we can write down, whether physical or not. The physically allowed states, those that satisfy the symmetrization postulate {eq}`eq-hartfock-56`, occupy a subspace of the nominal Hilbert space, what we may call the “physical subspace.”

Just as some states are nonphysical, some operators that act on the nominal Hilbert space are nonphysical, too, in the sense that they do not correspond to any measurement process that can actually be carried out. A physical operator is necessarily one that maps any physical state into another physical state, that is, it must leave the physical subspace of the nominal Hilbert space invariant. Operators that commute with all permutations satisfy this condition and are physical. An example is the atomic Hamiltonian {eq}`eq-hartfock-1`, in fact, the two terms $H_1$ and $H_2$ in {eq}`eq-hartfock-2` and {eq}`eq-hartfock-3` individually commute with all permutations,

:::{math}
:label: eq-hartfock-57
[P,H_1] = [P,H_2] = 0,
:::

since the permutation operators just permute the labels in a sum such as {eq}`eq-hartfock-2` without changing the sum itself. Similarly, the total orbital angular momentum $\Lvec$ and spin $\Svec$, defined in {eq}`eq-hartfock-4` and {eq}`eq-hartfock-5`, are physical operators. The individual orbital angular momenta $\Lvec_i$ and spins $\Svec_i$ are, however, not physical.

In fact we can say that all physical observables (Hamiltonians and others) involving identical particles must commute with all permutations of those particles, since otherwise the particles would not be identical.

(sec-hartfock-11)=

## The Symmetrization Postulate and the Pauli Exclusion Principle

The usual statement of the Pauli exclusion principle is that no two electrons can occupy the same state. This refers of course to the case of identical fermions. It is important to understand that the “states” in question are *single-particle* states, and that when we talk about electrons being “in” such states we are implicitly thinking of a multiparticle state that is a properly antisymmetrized tensor product of such single particle states, that is, it is a Slater determinant as in {eq}`eq-hartfock-39`. The Slater determinant vanishes if any two single particle states $\ket{\lambda}$ are identical, since in that case two columns of the determinant are equal. As remarked in \secrhartfock-7, the more general condition is that the Slater determinant vanishes if the set of single particle orbitals is linearly dependent.

It is important to realize that such multiparticle fermion states (Slater determinants of single particle orbitals) are not the most general multiparticle states. While an arbitrary physical, multiparticle fermion state (one lying in the physical subspace) can always be written as a linear combination of Slater determinants, it is unlikely that the actual multiparticle states occurring in the real world have the form of a single Slater determinant. Slater determinants, that is, multiparticle fermion states in which it is meaningful to talk about the (single particle) “states” that the electrons are “in,” are much more common in theory or in vague or elementary descriptions of physical phenomena than they are in the real world. For example, these notes are devoted to Hartree-Fock theory, but the Slater determinant used in Hartree-Fock theory is only a trial wave function, and the actual wave functions of real atoms (ground states or otherwise) never have the form of a single Slater determinant.

Thus, the usual statement of the Pauli exclusion principle is rather limited in scope, and is not as general as the symmetrization postulate as given above.

(sec-hartfock-12)=

## The Antisymmetrizing Projector

In this we consider the case of $N$ identical fermions. The physical multiparticle states form a subspace of the nominal multiparticle Hilbert space, and it should be possible to write down a projection operator $A$ that projects onto this subspace. It turns out that this projector can be expressed in terms of the permutation operators,

:::{math}
:label: eq-hartfock-58
A={1\over N!} \sum_P (-1)^P P.
:::

To say that $A$ is a projection operator means that it is Hermitian, $A^\hc=A$, and that it is idempotent, $A^2=A$ (see {ref}`sec-hilbert-24`). The operator $A$ is Hermitian because the permutation operators $P$ are all unitary, and for every $P$ in the sum in {eq}`eq-hartfock-58` the term containing $P^{-1}=P^\hc$ also occurs (they could be the same term). Therefore when we form the Hermitian conjugate of the sum, the terms involving $P$ and $P^{-1}$ just exchange places, the sum goes into itself, and we find $A^\hc=A$.

To show that $A$ is idempotent, we begin by letting $Q$ be a fixed permutation, and we consider the product

:::{math}
:label: eq-hartfock-59
(-1)^{Q} Q A = {1\over N!} \sum_P (-1)^{Q} (-1)^P Q P.
:::

By {eq}`eq-hartfock-52`, this can also be written

:::{math}
:label: eq-hartfock-60
{1\over N!}\sum_P (-1)^{QP} QP = {1\over N!} \sum_P (-1)^{P'} P',
:::

where $P'=QP$. The variable of summation $P$ in this final sum is just a dummy variable, which runs over all the permutations. But if we take the list of permutations and multiply each on the left by a fixed permutation $Q$, the result is the same list all over again, but just in a different order. Therefore when $P$ runs over all permutations, so does $P'=QP$, and we can replace the dummy index of summation $P$ in {eq}`eq-hartfock-60` by $P'$. The result is

:::{math}
:label: eq-hartfock-61
(-1)^{Q} QA = {1\over N!} \sum_{P'} (-1)^{P'} P' = A.
:::

Now let us take the product $A^2$, and expand the first factor only. We have

:::{math}
:label: eq-hartfock-62
A^2 = \left( {1\over N!} \sum_P (-1)^P P \right) A = {1\over N!} \sum_P (-1)^P PA = {1\over N!} \sum_P A,
:::

where we use {eq}`eq-hartfock-61` in the last step. But this final sum is a sum of $N!$ terms, all of which are identical (namely, $A$), so the sum itself is just $N! A$. Thus the $N!$'s cancel, and we have $A^2=A$. Therefore $A$ is indeed a projection operator.

We must now show that $A$ projects onto the physical subspace, that is, if $\ket{\Psi}$ is an arbitrary multiparticle state, then $\ket{\Psi'}= A\ket{\Psi}$ is a state that satisfies the symmetrization postulate. To do this we apply the symmetrization postulate in the form {eq}`eq-hartfock-56`:

:::{math}
:label: eq-hartfock-63
P\ket{\Psi'} = PA\ket{\Psi} = (-1)^P A\ket{\Psi} =(-1)^P \ket{\Psi'},
:::

where we use {eq}`eq-hartfock-61`. Thus, the state $\ket{\Psi'}$ is properly antisymmetrized.

(sec-hartfock-13)=

## The Hartree-Fock Energy Functional

We return now to Hartree-Fock theory, and compute the expectation value of the Hamiltonian~{eq}`eq-hartfock-1` with respect to the Hartree-Fock trial wave function $\ket{\Phi}$ in {eq}`eq-hartfock-39`. First we note that the expansion of the Slater determinant by the definition of a determinant is equivalent to applying all $N!$ permutation operators $P$ to the Hartree state $\ket{\Phi_H}$ in {eq}`eq-hartfock-6` and summing the terms with $+$ and $-$ signs, corresponding to the parity of the permutation. Thus, by {eq}`eq-hartfock-58`, the Slater determinant is proportional to the antisymmetrizing projector $A$ applied to the (unsymmetrized) Hartree state. Including the prefactors, we have

:::{math}
:label: eq-hartfock-64
\ket{\Phi} = \sqrt{N!}\, A\ket{\Phi_H}.
:::

This is a convenient way of writing the Hartree-Fock state in terms of the Hartree state.

Next we note that since the terms in the Hamiltonian $H_1$ and $H_2$ commute with all permutations $P$ (see {eq}`eq-hartfock-57`, by the definition {eq}`eq-hartfock-58` they also commute with $A$,

:::{math}
:label: eq-hartfock-65
[H_1,A] = [H_2,A] = 0.
:::

In fact, this is true of any operator that is physically meaningful.

Now we compute the expectation value of $H_1$ in {eq}`eq-hartfock-2` with respect to the Hartree-Fock state. First we use {eq}`eq-hartfock-64` to write the expectation value in terms of the Hartree state,

:::{math}
:label: eq-hartfock-66
\matrixelement{\Phi}{H_1}{\Phi} = N! \matrixelement{\Phi_H}{A^\hc H_1 \,A} {\Phi_H}.
:::

But the operator in this latter matrix element can be simplified,

:::{math}
:label: eq-hartfock-67
A^\hc H_1 \, A = AH_1A=H_1A^2=H_1 A,
:::

where we use {eq}`eq-hartfock-65` and the relations $A^\hc=A$ and $A^2=A$. Thus {eq}`eq-hartfock-66` can be written

:::{math}
:label: eq-hartfock-68
\matrixelement{\Phi}{H_1}{\Phi} = N! \matrixelement{\Phi_H}{H_1 A}{\Phi_H}= \sum_{i=1}^N \sum_P (-1)^P \matrixelement{\Phi_H}{h_i P}{\Phi_H},
:::

where we have used {eq}`eq-hartfock-2` and {eq}`eq-hartfock-58` to expand $H_1$ and $A$, and where the individual particle Hamiltonian $h_i$ is defined in {eq}`eq-hartfock-13`.

Let us take the case $i=2$ for the matrix element in {eq}`eq-hartfock-68`, and write out the Hartree states in terms of single particle orbitals as in {eq}`eq-hartfock-6`. We find

:::{math}
\begin{aligned}
&\matrixelement{\Phi_H}{h_2 P}{\Phi_H}=
\end{aligned}
:::

:::{math}
:label: eq-hartfock-69
\begin{aligned}
&\qquad \bra{1}^{(1)} \bra{2}^{(2)} \bra{3}^{(3)} \ldots \bra{N}^{(N)} \; h_2 \; \ket{P_1}^{(1)} \ket{P_2}^{(2)} \ket{P_3}^{(3)} \ldots \ket{P_N}^{(N)},
\end{aligned}
:::

where we express action of the permutation $P$ on the Hartree state $\ket{\Phi_H}$ as in \secrhartfock-9. The operator in the center of this matrix element, namely $h_2$, only acts on the variables for particle 2, and therefore only involves the bra $\bra{2}^{(2)}$ on the left and the ket $\ket{P_2}^{(2)}$ on the right. All other single particle bras and kets pass right through $h_2$, and combine with each other in accordance with the orthonormality condition $\braket{\lambda}{\mu}=\delta_{\lambda\mu}$. Thus, the matrix element becomes,

:::{math}
:label: eq-hartfock-70
\matrixelement{\Phi_H}{h_2 P}{\Phi_H}= \delta_{1P_1} \, \delta_{3P_3} \, \delta_{4P_4} \ldots \, \delta_{NP_N} \bra{2}^{(2)} \; h_2 \; \ket{P_2}^{(2)},
:::

where only the $i=2$ term is omitted from the product of Kronecker deltas. But this matrix element was taken out of the expression in {eq}`eq-hartfock-68`, where it is summed over all permutations $P$, and we see that the Kronecker deltas will severely limit the permutations of this sum that yield nonvanishing terms. In fact, the Kronecker deltas in {eq}`eq-hartfock-70` will force the permutation to have the form,

:::{math}
:label: eq-hartfock-71
\begin{aligned}
P=\begin{pmatrix}1 & 2 & 3 & 4 & \ldots & N\\ 1 & x & 3 & 4 & \ldots & N\\\end{pmatrix},
\end{aligned}

:::

where only $x=P_2$ is not determined by the Kronecker deltas. But since a permutation must be a rearrangement of the $N$ numbers on the top row, the only possibility for $x=P_2$ on the bottom row is the value 2. Therefore the only permutation that survives in the sum {eq}`eq-hartfock-68` is the identity permutation, which is an even permutation.

Thus we have

:::{math}
:label: eq-hartfock-72
\sum_P (-1)^P \matrixelement{\Phi_H}{h_2 P}{\Phi_H}= \bra{2}^{(2)} \; h_2 \; \ket{2}^{(2)},
:::

and {eq}`eq-hartfock-68` becomes

:::{math}
:label: eq-hartfock-73
\matrixelement{\Phi}{H_1}{\Phi} = \sum_{i=1}^N \bra{i}^{(i)} \; h_i\; \ket{i}^{(i)}= \sum_{\lambda=1}^N \bra{\lambda}^{(i)} \; h_i \ket{\lambda}^{(i)},
:::

where in the last step we have switched to Greek indices for orbitals and added the condition $i=\lambda$. The result is the same as the expectation value of $H_1$ in Hartree's simpler theory, {eq}`eq-hartfock-17`, so

:::{math}
:label: eq-hartfock-74
\matrixelement{\Phi}{H_1}{\Phi} = \sum_{\lambda=1}^N I_\lambda,
:::

where $I_\lambda$ is defined in {eq}`eq-hartfock-20`.

The term $H_2$ in {eq}`eq-hartfock-3` is treated similarly. We have

:::{math}
\begin{aligned}
\matrixelement{\Phi}{H_2}{\Phi}&= N! \matrixelement{\Phi_H}{A^\hc H_2 \,A}{\Phi_H}
\end{aligned}
:::

:::{math}
:label: eq-hartfock-75
\begin{aligned}
&=N! \matrixelement{\Phi_H}{H_2 A}{\Phi_H}= \sum_{i<j} \sum_P (-1)^P \matrixelement{\Phi_H}{{1\over r_{ij}}P}{\Phi_H},
\end{aligned}
:::

just as in {eq}`eq-hartfock-66`--{eq}`eq-hartfock-68`. To understand the matrix elements appearing here, we take the example $i=2$, $j=3$, for which we have

:::{math}
\begin{aligned}
&\matrixelement{\Phi_H}{{1\over r_{23}}P}{\Phi_H}
\end{aligned}
:::

:::{math}
:label: eq-hartfock-76
\begin{aligned}
&\quad =\bra{1}^{(1)} \bra{2}^{(2)} \bra{3}^{(3)} \ldots \bra{N}^{(N)} \, {1\over r_{23}} \, \ket{P_1}^{(1)} \ket{P_2}^{(2)} \ket{P_3}^{(3)} \ldots \ket{P_N}^{(N)},
\end{aligned}
:::

just as in {eq}`eq-hartfock-69`. Proceeding as before, we note that the operator $1/r_{23}$ only acts on the coordinates for particles 2 and 3, so all the other single particle bras and kets combine by orthonormality. We obtain a product of $N-2$ Kronecker deltas,

:::{math}
:label: eq-hartfock-77
\matrixelement{\Phi_H}{{1\over r_{23}}P}{\Phi_H}= \delta_{1P_1} \; \delta_{4P_4} \; \delta_{5P_5} \ldots \delta_{NP_N}\; \bra{2}^{(2)} \bra{3}^{(3)} \, {1\over r_{23}} \, \ket{P_2}^{(2)} \ket{P_3}^{(3)},
:::

where only the $i=2,3$ terms are omitted from the product of Kronecker deltas. As before, when this matrix element is summed over permutations as in {eq}`eq-hartfock-75`, most permutations will not contribute. In fact, the Kronecker deltas will force the permutations to have the form,

:::{math}
:label: eq-hartfock-78
\begin{aligned}
P=\begin{pmatrix} 1 & 2 & 3 & 4 & 5 & \ldots & N\\ 1 & x & y & 4 & 5 & \ldots & N\\\end{pmatrix},
\end{aligned}

:::

where only $x=P_2$ and $y=P_3$ are not determined. But there are only two permutations of this form. One is the identity permutation $P=I$, an even permutation, for which $x=P_2=2$ and $y=P_3=3$; and the other is the permutation that exchanges particles 2 and 3, $P=E_{23}$, an odd permutation, for which $x=P_2=3$ and $y=P_3=2$.

Therefore the sum in {eq}`eq-hartfock-75` can be written

:::{math}
\begin{aligned}
\matrixelement{\Phi}{H_2}{\Phi} & = \sum_{i<j} \Bigl[ \bra{i}^{(i)} \bra{j}^{(j)} \, {1\over r_{ij}} \ket{i}^{(i)} \ket{j}^{(j)} - \bra{i}^{(i)} \bra{j}^{(j)} \, {1\over r_{ij}} \ket{j}^{(i)} \ket{i}^{(j)} \Bigr]
\end{aligned}
:::

:::{math}
:label: eq-hartfock-79
\begin{aligned}
&= \sum_{\lambda<\mu} \Bigl[ \bra{\lambda}^{(i)} \bra{\mu}^{(j)} \, {1\over r_{ij}} \ket{\lambda}^{(i)} \ket{\mu}^{(j)} - \bra{\lambda}^{(i)} \bra{\mu}^{(j)} \, {1\over r_{ij}} \ket{\mu}^{(i)} \ket{\lambda}^{(j)} \Bigr],
\end{aligned}
:::

where in the final expression we add the conditions $i=\lambda$, $j=\mu$. The first term in the final sum is the same expression we had in the case of the Hartree theory (see {eq}`eq-hartfock-23`, and can be expressed as a sum over the direct integrals $J_{\lambda\mu}$ defined in {eq}`eq-hartfock-25`.

As for the matrix elements in the second term in the final sum in {eq}`eq-hartfock-79`,

:::{math}
:label: eq-hartfock-80
\bra{\lambda}^{(i)} \bra{\mu}^{(j)} \, {1\over r_{ij}} \ket{\mu}^{(i)} \ket{\lambda}^{(j)},
:::

they can also be written out in terms of the spatial and spin parts of the orbitals for particles $i$ and $j$. As for particle $i$, the orbitals in the bra and ket on the two sides are not the same, so the spin parts are not necessarily identical. The operator in the middle is a purely spatial operator, so the spin parts of the orbitals combine to give the Kronecker delta $\delta(m_{s\lambda},m_{s\mu})$. The same Kronecker delta occurs when we combine the spin parts of the bra and ket for particle $j$, but since a Kronecker delta is equal to its own square, we need only represent it once. As for the spatial parts of the matrix element, they can be written in terms of integrals over the coordinates $\rvec_i$ and $\rvec_j$ of particles $i$ and $j$, which, however, are dummy variables of integration that we replace by $\rvec$ and $\rvec'$. We write the result as

:::{math}
:label: eq-hartfock-81
K_{\lambda\mu} = \delta(m_{s\lambda},m_{s\mu}) \int d^3\rvec \, d^3\rvec' \; {u^\cc_\lambda(\rvec) u^\cc_\mu(\rvec') u_\lambda(\rvec') u_\mu(\rvec) \over |\rvec-\rvec'|}.
:::

This is an *exchange integral* of the type we saw previously in our perturbation treatment of the excited states of helium. We recall that the exchange integrals were responsible for the splitting between ortho and para states in helium, that is, they account for the energy shift when the spatial symmetry of the wave function is forced to change because of a change in spin symmetry.

Altogether, we can express the expectation value of $H_2$ in the Hartree-Fock theory as

:::{math}
:label: eq-hartfock-82
\matrixelement{\Phi}{H_2}{\Phi} = \sum_{\lambda<\mu}(J_{\lambda\mu} - K_{\lambda\mu}).
:::

The first term is the same as in the Hartree theory (see {eq}`eq-hartfock-26`, but the second term is new.

The exchange integrals $K_{\lambda\mu}$ do not have such a simple electrostatic interpretation as the direct integrals $J_{\lambda\mu}$. By use of Green's theorem one can prove that they are positive (see Appendix~19 of *Quantum Theory of Atomic Structure*, by John C. Slater). This is plausible in any case, since the denominator $|\rvec-\rvec'|$ causes the regions where $\rvec\approx\rvec'$ to dominate the integral, and in such regions the numerator of the integrand is positive. Thus, since they enter with a minus sign in the energy functional {eq}`eq-hartfock-82`, the Hartree-Fock energy is lower than the Hartree energy, and provides a better estimate to the ground state energy. This is what we would expect, given that the Hartree-Fock wave function is more sophisticated (and closer to the physics since it is a physically allowed state).

However, note that because of the Kronecker delta in {eq}`eq-hartfock-81`, the exchange integrals are nonzero only between orbitals of the same spin (both up or both down). Thus, when spins are aligned (either all up or all down), the effect of the exchange integrals is maximized. In this case, the exchange integrals reduce the overall energy of the collection of electrons. This is a reflection of the fact that when spins are aligned, the symmetry of the spin states forces an antisymmetry of the spatial parts of the multiparticle wave function, so that the electrons are kept apart. This in turn reduces the electrostatic energy of interaction of the electrons. On the other hand, when half the spins are up and half down, the effect of the exchange terms is minimized, and the energy is raised. The same phenomenon occurred in the case of helium, where the ortho states are lower in energy than the para states for the same configuration.

Because states with all spins aligned are lower in energy, the ground states of atoms do have their spins aligned in this way to the extent it is allowed by the symmetrization postulate. In the case of a full subshell, there is only one way to assign the spins, and that is half up and half down. But when a new subshell is being filled, the electrons that go in first will align themselves (all up, say), until the subshell is half-filled; after that, by the Pauli principle, spins must start to go in pointing down. The first spin to go in down, after the subshell is half-full, causes an abrupt raising of the energy of the atom and a lowering of the ionization energy; this is the explanation for the glitch between nitrogen and oxygen in the graph of the ionization potential as a function of $Z$. See {ref}`fig-hartfock-1`. The special stability of half-filled subshells also explains why chromium, in the first transition series of elements, which might have been expected to have a configuration of $3d^4 4s^2$, actually borrows an electron from $4s$ subshell and ends up with configuration $3d^5 4s$.

:::{figure} images/hartfock-fig01.png
:label: fig-hartfock-1
:width: 80%

Ionization potentials (I.P.) for low-$Z$ atoms. Energies measured in atomic units.
:::

The exchange integrals are real and symmetric in their indices, $K_{\lambda\mu} = K_{\mu\lambda}$, like the direct integrals, and are positive. In addition, the direct and exchange integrals are equal on

:::{math}
:label: eq-hartfock-83
the diagonal, J_{\lambda\lambda} = K_{\lambda\lambda},  as follows by inspection of the integrals.  The
:::

diagonal elements are the self-energies of the electron clouds which we do not expect to appear in the physics of the electron interactions, but since only the difference $J_{\lambda\mu}-K_{\lambda\mu}$ occurs in the sum {eq}`eq-hartfock-82`, we can extend that sum to include the diagonal terms without changing anything. Then extending the sum to all $\lambda$ and $\mu$, we can

:::{math}
:label: eq-hartfock-84
write the expectation value as \matrixelement{\Phi}{H_2}{\Phi}= {1\over2}\sum_{\lambda\mu} (J_{\lambda\mu}-K_{\lambda\mu}),  where we divide by 2 to compensate for the double
:::

counting. This is the most convenient form for the expectation value.

Altogether, the energy functional in the Hartree-Fock theory is

:::{math}
:label: eq-hartfock-85
E[\Phi] = \matrixelement{\Phi}{H}{\Phi}= \sum_{\lambda=1}^N I_\lambda +{1\over2} \sum_{\lambda\mu} (J_{\lambda\mu}-K_{\lambda\mu}).
:::

(sec-hartfock-14)=

## The Hartree-Fock Equations

We wish the energy to be stationary with respect to variations in the single particle orbitals $u_\lambda(\rvec)$, but we cannot allow arbitrary variations because we wish to preserve the orthonormality conditions {eq}`eq-hartfock-42`. These constitute $N^2$ constraints, so we should introduce $N^2$ Lagrange multipliers, which we can arrange in a matrix denoted by $\epsilon_{\lambda\mu}$. Then we can add the Lagrange multiplier term

:::{math}
:label: eq-hartfock-86
\sum_{\lambda\mu} \epsilon_{\lambda\mu} \bigl(\braket{\lambda}{\mu}-\delta_{\lambda\mu}\bigr)
:::

to the energy functional $E[\Phi]$. This would be the honest way of enforcing these constraints, and if we do it, we will get the correct answers.

It turns out, however, that a simpler approach gives the same results. In the simpler approach, instead of demanding that the single particle orbitals be orthonormal, we simply demand that they be normalized. This amounts to only $N$ constraints, $\braket{\lambda}{\lambda}=1$, which can be enforced by adding the term

:::{math}
:label: eq-hartfock-87
\sum_\lambda \epsilon_\lambda \bigl(\braket{\lambda}{\lambda}-1\bigr)
:::

to the energy functional. Here $\epsilon_\lambda$ are the $N$ Lagrange multipliers, and the constraint condition is given explicitly in terms of the unknown spatial orbitals $u_\lambda$ by

:::{math}
:label: eq-hartfock-88
\braket{\lambda}{\lambda} = \int d^3\rvec \; u^\cc_\lambda(\rvec) u_\lambda(\rvec),
:::

since the spin parts of the orbital $\ket{\lambda}$ simply combine to give unity. The reason this simpler method works is that once the variational equations have been derived, it turns out that the solutions to those equations are automatically orthogonal. Thus, the orthogonality conditions are not really necessary. But to believe this we must prove the orthogonality of the solutions of the variational equations, since we are not enforcing orthogonality with Lagrange multipliers. We will return to this task later.

Altogether, our functional is

:::{math}
:label: eq-hartfock-89
F[\Phi] = \sum_{\lambda=1}^N I_\lambda +{1\over2} \sum_{\lambda\mu} (J_{\lambda\mu}-K_{\lambda\mu}) -\sum_{\lambda=1}^N \epsilon_\lambda \bigl(\braket{\lambda}{\lambda}-1\bigr),
:::

where we use the symbol $F$ to indicated a modified energy functional.

Carrying out the functional derivative, we find the Hartree-Fock equations in the form,

:::{math}
:label: eq-hartfock-90
\left( {p^2\over2} -{Z\over r} \right) u_\lambda(\rvec) +V_d(\rvec) u_\lambda(\rvec) -\int d^3\rvec' \, V_{ex}(\rvec,\rvec') u_\lambda(\rvec') = \epsilon_\lambda u_\lambda(\rvec),
:::

where we define

:::{math}
:label: eq-hartfock-91
V_d(\rvec)= \sum_{\mu=1}^N \int d^3\rvec' \, { |u_\mu(\rvec')|^2 \over |\rvec-\rvec'|},
:::

and

:::{math}
:label: eq-hartfock-92
V_{ex}(\rvec,\rvec') = \sum_{\mu=1}^N \delta(m_{s\lambda},m_{s\mu}) {u_\mu(\rvec) u^\cc_\mu(\rvec') \over |\rvec-\rvec'|}.
:::

As in the Hartree theory, the Hartree-Fock equations have the form of a pseudo-Schr\"odinger equation, in which the Lagrange multiplier $\epsilon_\lambda$ plays the role of an eigenvalue, and the Schr\"odinger operator is determined self-consistently by the orbitals $u_\lambda(\rvec)$ themselves. The functions $V_d(\rvec)$ and $V_{ex}(\rvec,\rvec')$ are called the *direct* and *exchange* potentials; both of these are self-consistent, that is, determined only once the orbitals $u_\lambda(\rvec)$ are known.

The direct potential $V_d(\rvec)$ is almost the same as the potential $V_\lambda(\rvec)$ in the Hartree theory, the difference being that it includes the potential of all the electrons, including the one with orbital $u_\lambda$ itself. In other words, it contains the self-interactions, and a given orbital seems to be acted upon by the electric field produced by itself. We do not expect the self-interactions to appear physically, and actually they do not, since the diagonal $\lambda=\mu$ contributions to the direct and exchange terms in the Hartree-Fock equations {eq}`eq-hartfock-90` cancel. But it is convenient to leave them in the direct potential $V_d(\rvec)$, because this makes this potential the same for all orbitals (independent of $\lambda$). Recall that in the Hartree theory, the fact that the potentials depended on $\lambda$ meant that the different orbitals were driven by different Schr\"odinger operators, and hence not orthogonal to one another.

The exchange potential $V_{ex}(\rvec,\rvec')$ is the new element in the Hartree-Fock equations. The exchange term in these equations has the form of an integral transform applied to the orbital $u_\lambda(\rvec)$, in which $V_{ex}(\rvec,\rvec')$ is the kernel. This is a linear operator, but it is not a multiplicative operator in the position representation, like $V_d(\rvec)$ (that is, like an ordinary potential). As a result, the exchange potential is referred to as a “nonlocal potential.” If we denote the exchange potential, regarded as an operator, by simply $V_{ex}$, then its relation to the function $V_{ex}(\rvec,\rvec')$ is simply

:::{math}
:label: eq-hartfock-93
V_{ex}(\rvec,\rvec') = \matrixelement{\rvec}{V_{ex}}{\rvec'}.
:::

The operator is nonlocal because its matrix elements in the position representation are not diagonal. The exchange potential is harder to interpret physically than the direct potential, but it is responsible for the effective repulsion that electrons in the same spin states feel due to the symmetrization postulate, which forces the spatial parts of their wave functions to repel one another.

As noted, the direct potential is the same for all orbitals $\lambda$, but the exchange potential does depend on the orbital in question, through the Kronecker delta $\delta(m_{s\lambda},m_{s\mu})$. But since $m_{s\lambda}$ can only take on the values $\pm\frac{1}{2}$, there are in fact only two exchange potentials, which with a slight change of notation we might write as

:::{math}
:label: eq-hartfock-94
V^\pm_{ex}(\rvec,\rvec') = \sum_{\mu=1}^N \delta(m_{s\mu},\pm\frac{1}{2}) {u_\mu(\rvec) u^\cc_\mu(\rvec') \over |\rvec-\rvec'|}.
:::

Then all spin-up orbitals $u_\lambda$ are driven by the exchange potential $V^+_{ex}$, and all spin down orbitals by $V^-_{ex}$. Thus, the Hartree-Fock equations {eq}`eq-hartfock-90` can be thought of as two coupled equations, one for spin-up orbitals and one for spin-down orbitals,

:::{math}
:label: eq-hartfock-95
\left( {p^2 \over 2} - {Z\over r} + V_d - V_{ex}^\pm \right) u_\lambda(\rvec) = \epsilon_\lambda u_\lambda(\rvec),
:::

where the $\pm$ sign is the same one in $m_{s\lambda} = \pm\frac{1}{2}$, and where we just write $V^{\pm}_{ex} u_\lambda$ for the wave function produced by the integral transform in {eq}`eq-hartfock-90`. Equations~{eq}`eq-hartfock-95` are coupled because the self-consistent potentials $V_d(\rvec)$ and $V_{ex}^{\pm}(\rvec,\rvec')$ involve all the orbitals. However, once these potentials have been determined self-consistently, then the spin up and spin down orbitals $u_\lambda$ are eigenfunctions of two distinct single-particle Hamiltonian operators.

Now we can see that the actual solutions to the Hartree-Fock equations are orthonormal, and verify the claims made earlier when we introduced the simplified Lagrange multiplier term {eq}`eq-hartfock-87`. For if we take two orbitals $\lambda \ne \lambda'$, both with the same value of spin, then since both orbitals satisfy the same Schr\"odinger equation (that is, both either with $V^+_{ex}$ or with $V^-_{ex}$), the spatial wave functions $u_\lambda(\rvec)$ and $u_{\lambda'}(\rvec)$ are automatically orthogonal. But if the spins are opposite, then the orbitals are orthogonal due to the spins. Altogether, the orthonormality constraints $\braket{\lambda}{\mu}=\delta_{\lambda\mu}$ are satisfied in Hartree-Fock theory.

This is in contrast to Hartree's theory, where the orbitals are not orthogonal (an unattractive feature of that theory). In fact, the Hartree-Fock theory is in many respects more symmetrical and elegant than the Hartree theory (and more physical, too, since it employs properly antisymmetrized wave functions). Nevertheless, the nonlocal exchange potential is definitely more difficult to work with than the direct potential, and people who do numerical calculations are always searching for approximations or other ways to avoid dealing with it.

(sec-hartfock-15)=

## Koopmans' Theorem

We will now attempt to give an interpretation for the pseudo-eigenvalues $\epsilon_\lambda$ that occur in the Hartree-Fock equations {eq}`eq-hartfock-90`. If we multiply this equation by $u_\lambda(\rvec)^\cc$ and integrate, we obtain

:::{math}
:label: eq-hartfock-96
I_\lambda + \sum_{\mu=1}^N (J_{\lambda\mu}-K_{\lambda\mu}) =\epsilon_\lambda.
:::

We might think that this $\epsilon_\lambda$ is somehow the energy of electron $\lambda$, and that the total energy of the atom would be the sum of the $\epsilon_\lambda$'s. But this is incorrect, for if we sum {eq}`eq-hartfock-96` over $\lambda$, we obtain

:::{math}
:label: eq-hartfock-97
\sum_\lambda \epsilon_\lambda = \sum_\lambda I_\lambda +\sum_{\lambda\mu} (J_{\lambda\mu}-K_{\lambda\mu}) = E + {1\over2} \sum_{\lambda\mu} (J_{\lambda\mu}-K_{\lambda\mu}),
:::

where $E$ is the total energy of the atom according to {eq}`eq-hartfock-85`. On the other hand, there is an approximate relation between the largest of the eigenvalues $\epsilon_\lambda$ and the ionization potential of the atom. Assuming that we order the eigenvalues $\epsilon_\lambda$ in ascending order, then $\epsilon_N$ is the largest one. The ionization potential of the atom is the difference between the ground state energy of the atom with $N$ electrons, and the ground state energy of the (different) atom with $N-1$ electrons. According to {eq}`eq-hartfock-85`, these two energies are

:::{math}
:label: eq-hartfock-98a
E(N)=\sum_{\lambda=1}^N I_\lambda + {1\over2} \sum_{\lambda,\mu=1}^N (J_{\lambda\mu}-K_{\lambda\mu}),
:::

and

:::{math}
:label: eq-hartfock-98b
E(N-1)=\sum_{\lambda=1}^{N-1} I_\lambda +{1\over2} \sum_{\lambda,\mu=1}^{N-1} (J_{\lambda\mu}-K_{\lambda\mu}),
:::

The quantities $I_\lambda$, $J_{\lambda\mu}$, and $K_{\lambda\mu}$ in the two equations are not the same, since the fields are determined self-consistently, and when we remove one electron, we will obtain different self-consistent solutions for the orbitals. But if we assume this difference is small and ignore it, then we can subtract {eq}`eq-hartfock-98b` from {eq}`eq-hartfock-98a` to obtain the ionization potential (IP):

:::{math}
:label: eq-hartfock-99
IP = I_N + \sum_{\mu=1}^N (J_{N\mu}-K_{N\mu}) =\epsilon_N.
:::

In deriving this equation, it helps to remember that $J_{\lambda\lambda}=K_{\lambda\lambda}$ (on the diagonal). The result {eq}`eq-hartfock-99` is known as *Koopmans' theorem*.

(sec-hartfock-16)=

## Averaging and the Electron Configuration

The Hartree-Fock equations are nonlinear, and can be solved by an iterative procedure much as in Hartree's theory. As in Hartree's theory, in order to avoid solving fully three-dimensional wave equations at each iteration, we can add an additional, simplifying step in the iteration: After we have used a set of orbitals $u_\lambda(\rvec)$ to compute the direct and exchange potentials $V_d(\rvec)$ and $V_{ex}(\rvec,\rvec')$, we average these over angles to obtain rotationally invariant potentials, call them ${\bar V}_d(r)$ and ${\bar V}_{ex}(\rvec,\rvec')$. The physical reasoning behind this step is that we expect the atom, at least in the ground state, to be approximately spherically symmetric, so we hope there will not be a great loss in accuracy in forcing the self-consistent potentials to have the same symmetry.

For the direct potential, the angle average is given by

:::{math}
:label: eq-hartfock-100
{\bar V}_d(r) = {1\over 4\pi} \int d\Omega \, V_d(\rvec),
:::

as in {eq}`eq-hartfock-35`. The formula for averaging the exchange potential is slightly more complicated, so we will not write it down, but we remark that the effect is to create an averaged exchange operator ${\bar V}^\pm_{ex}$ with integral kernel ${\bar V}^\pm_{ex}(\rvec,\rvec')$ that is invariant under all rotations,

:::{math}
:label: eq-hartfock-101
U(\Rmat) {\bar V}^\pm_{ex} U(\Rmat)^\dagger = {\bar V}^\pm_{ex},
:::

for all $\Rmat \in SO(3)$. (The unitary operator $U(\Rmat)$, acting on three-dimensional wave functions, is defined in {eq}`eq-orbamsph-13`.) The result is a pair of Schr\"odinger operators (one for spin up, one for spin down) for the orbitals $u_\lambda(\rvec)$ that are rotationally invariant, so that the wave equations separate in spherical coordinates and the orbitals $u_\lambda(\rvec)$ have the central force form $R_{n\ell}(r) Y_{\ell m_\ell}(\Omega)$. Then only radial equations need be solved at each step of the iteration, that is, essentially one-dimensional Schr\"odinger equations, a much easier task than solving three-dimensional equations. After this step, the energies do not depend on the orbital magnetic quantum number $m_\ell$.

A further approximation of the same sort is to average the Hartree-Fock equations over spin rotations as well as spatial ones. This replaces the two exchange potentials ${\bar V}^\pm_{ex}$ by their average,

:::{math}
:label: eq-hartfock-102
{\bar V}^\pm_{ex} \to {1\over 2} ({\bar V}^+_{ex}+{\bar V}^-_{ex}),
:::

which we will call simply ${\bar V}_{ex}$ (without the $\pm$). After this is done, there is effectively only one Hartree-Fock operator (the same for spin up and spin down orbitals), and the energies do not depend on the spin magnetic quantum number $m_s$. The Hartree-Fock equations that must now be solved are

:::{math}
:label: eq-hartfock-103
\left( {p^2 \over 2} - {Z \over r} + {\bar V}_d - {\bar V}_{ex} \right) u_\lambda(\rvec) = \epsilon_\lambda u_\lambda(\rvec).
:::

With these averaging steps included, the labels $\lambda$ of the Hartree-Fock orbitals $\ket{\lambda}$ can be identified with a list of central force quantum numbers, $\lambda=(n\ell m_\ell m_s)$, and the eigenvalues $\epsilon_{\lambda}$ become $\epsilon_{n\ell}$ (independent of $m_\ell$ and $m_s$). Thus, it becomes possible to describe the electrons as being “in” various central force orbitals, not which electrons are in which orbitals (because that would imply a nonphysical labeling of the electrons), but simply a list of the orbitals that are occupied. This list is called the *electron configuration* of the atom. Since the energies do not depend on the magnetic quantum numbers $m_\ell$ and $m_s$, the electron configuration is limited to a count of the number of electrons possessing the various $(n\ell)$ values. For a given $(n\ell)$ value, the number of possible magnetic quantum numbers is $2(2\ell+1)$; the corresponding states are said to form a *subshell* of the atom. Some examples will illustrate the standard spectroscopic notation for electron configurations. For helium, it is $1s^2$; for beryllium, $1s^22s^2$; for carbon, $1s^22s^22p^2$; for sodium, $1s^22s^22p^63s$. As shown, the number of electrons in a subshell is indicated by an superscript. Standard periodic tables of the elements usually list the configuration of all the atoms, that is, the ground states of the neutral atoms. It must be understood that the central field potentials in question are self-consistent, and that they depend on the atom in question (the value of Z).

It should also be understood that the electron configuration does not refer to the actual ground state of the atom, but rather to the best approximation to it according to the variational principle and other approximations we have made. The true ground (or any other state) of an atom never has exactly the form of a single Slater determinant, comprised of a list of single particle orbitals. It may certainly be expanded as a linear combination of such Slater determinants, but there is no guarantee on the basis of anything that we have said that the expansion is even dominated by a single term. This is once again a warning to be careful of language in which one speaks of which state various electrons are “in.” Such language is only meaningful for product wave functions, which are common in theory but rare in the real world.

An interesting fact about the Hartree-Fock equations is that the averaging procedure described above is actually unnecessary in the case of completely filled subshells, for example, beryllium with $1s^22s^2$ or neon with $1s^22s^22p^6$. In this case, self-consistent solutions exist in the form of central field eigenfunctions. That is, with orbitals of this form, the direct and exchange potentials are automatically invariant under both spatial and spin rotations. See Prob.~\prbrhartfock-2.

\problems

(prob-hartfock-1)=

**Problem \prbdhartfock-1.}  Show that the Slater determinant $\ket{\Phi}$ in {eq}`eq-hartfock-39` is normalized if the orbitals $\ket{\lambda.** 

(prob-hartfock-2)=

**Problem \prbdhartfock-2..** 

It is a familiar fact that a three-dimensional central force Hamiltonian }$H=p^2/2m+V(r)$ has eigenfunctions in the form $R_{n\ell}(r) Y_{\ell m}(\Omega)$, and that the energies only depend on $n$ and $\ell$. It turns out that these facts are true for any rotationally invariant Hamiltonian in three dimensions (that is, $H$ need not have the simple kinetic-plus-potential form). This is important in Hartree-Fock theory, because the exchange potential is not an ordinary potential.

\problempart{(a)} In Hartree-Fock theory, the direct potential is given in terms of the orbitals $u_\lambda(\rvec)$ by {eq}`eq-hartfock-91`. Suppose that the orbitals are central force orbitals so $\lambda=(n\ell m_\ell m_s)$, and suppose that all subshells are filled. Show that the direct potential is then rotationally invariant, that is, it only depends on $r=|\rvec|$.

Hint: It is easiest to solve this as a problem in electrostatics. The potential will be rotationally invariant if the charge density is rotationally invariant. To prove the latter fact, use the addition theorem for spherical harmonics, {eq}`eq-orbamsph-71`. Once the charge density is known the potential can be determined by Gauss's law.

\problempart{(b)} An operator $\Khat$ is rotationally invariant if it commutes with all rotation operators,

:::{math}
:label: eq-hartfock-104
U(\Rmat)^\dagger \Khat U(\Rmat) = \Khat,
:::

for all $\Rmat \in SO(3)$. See {eq}`eq-orbamsph-3` or {eq}`eq-orbamsph-13` for the definition of $U(\Rmat)$. $K$ is also called a scalar operator (see {ref}`sec-transfop-3`). Let $K(\rvec,\rvec')$ be the kernel of the operator $\Khat$, so that the action or $\Khat$ on a wave function $\psi$ is

:::{math}
:label: eq-hartfock-105
(\Khat\psi)(\rvec) = \int d^3\rvec' \, K(\rvec,\rvec')\psi(\rvec').
:::

Then the kernel is the $\rvec$-space matrix elements of the operator $\Khat$,

:::{math}
:label: eq-hartfock-106
K(\rvec,\rvec') = \matrixelement{\rvec}{\Khat}{\rvec'}.
:::

This is precisely the situation we have with the exchange potentials in Hartree-Fock theory, see {eq}`eq-hartfock-92`. (If the kernel of the exchange potential is $V^\pm_{ex}(\rvec,\rvec')$, then we may write the operator as ${\hat V}^\pm_{ex}$. See {eq}`eq-hartfock-93` for the definition of the kernel.)

If $\Khat$ is rotationally invariant, then we must have

:::{math}
:label: eq-hartfock-107
\matrixelement{\rvec}{U(\Rmat)^\dagger \Khat U(\Rmat)}{\rvec'} =\matrixelement{\Rmat\rvec}{\Khat}{\Rmat\rvec'} = \matrixelement{\rvec}{\Khat}{\rvec'},
:::

or,

:::{math}
:label: eq-hartfock-108
K(\rvec,\rvec') = K(\Rmat\rvec, \Rmat\rvec'),
:::

for all $\Rmat \in SO(3)$. Think of the kernel $K(\rvec,\rvec')$ as a function of two vectors in 3D~space. According to {eq}`eq-hartfock-108`, if $\Khat$ is rotationally invariant, then the value of $K(\rvec,\rvec')$ is unchanged if both vectors are rotated by the same rotation. This means that $K(\rvec,\rvec')$ is actually only a function of the rotational invariants of the triangle formed by the two vectors $\rvec$ and $\rvec'$. The triangle invariants include the lengths of the three sides of the triangle, $r=|\rvec|$, $r'=|\rvec'|$, and $|\rvec-\rvec'|$, or the three angles of the triangle.

Show that in the case of complete subshells, two exchange potentials $V^\pm_{ex}(\rvec,\rvec')$ are functions only of the triangle invariants, so that the operators ${\hat V}^\pm_{ex}$ are rotationally invariant. Show also that the two exchange potentials (for spin up and spin down orbitals) are equal, so there is only one Hartree-Fock equation (and we can drop the $\pm$).

Parts (a) and (b) of this problem show that in the case of complete subshells, it is not necessary to average the potentials (direct and exchange), since they automatically turn out to be invariant under rotations and independent of spin.

(prob-hartfock-3)=

**Problem \prbdhartfock-3..** 

In Bose-Einstein condensates (cold gases of bosonic atoms), the temperature and density are such that for atom-atom scattering $\lambda\gg R$, where $R$ is the radius of the atom and where $\lambda$, the de~Broglie wavelength, is comparable to the interparticle separation (this is required for the condensation). Thus replacing the atom-atom potential by a $\delta$-function is a good approximation.

Typically Bose-Einstein condensates are gases in which the atoms are moving in some external, confining potential, call it $V(\rvec)$. Based on what we have said, the Hamiltonian for a system of $N$ identical bosonic atoms of spin~0 in the potential $V$ is

:::{math}
:label: eq-hartfock-109
H=\sum_{i=1}^N \left( {p_i^2\over 2m} + V(\rvec_i)\right) + g \sum_{i<j} \delta^3(\rvec_i-\rvec_j).
:::

This differs from the Hamiltonian we used in studying the electrons in atoms in three respects: (1) the external potential is $V$ instead of $Z/r$; (2) the interaction potentials are $\delta$-functions instead of Coulomb interactions; (3) the particles are spin-0 bosons.

Write down a trial wave function for the ground state of this system of bosons that is as close in spirit as possible to the Hartree-Fock trial wave function in atoms, given that these are bosons instead of fermions. Derive a self-consistent, three-dimensional Schr\"odinger-like equation that must be satisfied to minimize the energy of the system. This equation is the starting point of much current research into Bose-Einstein condensates.
