---
title: "33. Elements of Atomic Structure in Multi-Electron Atoms"
---
(ch-atomstruc)=

# 33. Elements of Atomic Structure in Multi-Electron Atoms

(sec-atomstruc-1)=

## Introduction

In these notes we combine perturbation theory with the results of the Hartree-Fock calculation outlined in {ref}`ch-hartfock`{} to obtain a basic qualitative and semi-quantitative understanding of the low-lying energy levels and energy eigenfunctions in multi-electron atoms. We concentrate on the ground state configuration of low-$Z$ atoms where $LS$-coupling is applicable. The presentation in these notes is based on the book *Intermediate Quantum Mechanics* by Bethe and Jackiw.

In these notes we continue with the custom of using the capital letters $L$, $S$ and $J$ for the quantum numbers of the whole atom, while reserving lower case letters $\ell$, $s$, $j$ for those of a single electron.

(sec-atomstruc-2)=

## Summary of the Results of Hartree-Fock Theory

In {ref}`ch-hartfock`{} we found a variational estimate to the ground state of the basic $N$-electron atom Hamiltonian {eq}`eq-hartfock-1`, reproduced here:

:::{math}
:label: eq-atomstruc-1
H = \sum_{i=1}^N \Bigl({p_i^2\over 2} -{Z\over r_i}\Bigr) + \sum_{i<j} {1\over r_{ij}}.
:::

We denote the estimate for the ground state by $\ket{\Phi}$; it is a Slater determinant composed of $N$ single particle orbitals, $\ket{\lambda}$, $\lambda=1,\ldots,N$, as in {eq}`eq-hartfock-39`. The individual orbitals are a product of a spatial part times a spin part, $\ket{\lambda} =\ket{u_\lambda}\ket{m_{s\lambda}}$, where $u_\lambda(\rvec) =\braket{\rvec}{u_\lambda}$ is the spatial wave function and $\ket{m_{s\lambda}}$ is an assignment of spins (up or down) to each orbital. Once the Hartree-Fock equations have been solved, the orbitals specify the self-consistent direct and exchange potentials, $V_d(\rvec)$ and $V_{ex}(\rvec,\rvec')$, according to {eq}`eq-hartfock-91` and {eq}`eq-hartfock-92`, where the exchange “potential” is really the $\rvec$-space kernel of the operator that we call a potential.

We assume that these potentials have been averaged over spatial and spin rotations, as described in {ref}`sec-hartfock-16`, which causes $V_d$ and $V_{ex}$ to be replaced by ${\bar V}_{d}$ and ${\bar V}_{ex}$, as in {eq}`eq-hartfock-100` and {eq}`eq-hartfock-101`. The spatial parts of the orbitals are then solutions of the pseudo-Schr\"odinger equation

:::{math}
:label: eq-atomstruc-2
h u_\lambda(\rvec) = \epsilon_\lambda u_\lambda(\rvec),
:::

where the effective single-particle Hamiltonian is

:::{math}
:label: eq-atomstruc-3
h(\rvec,\pvec) = {p^2\over 2} - {Z\over r} +{\bar V}_d(r) - {\bar V}_{ex},
:::

Here we denote the exchange potential, as an operator, by simply ${\bar V}_{ex}$, recognizing that it is actually an integral transform.

Since the single-particle Hamiltonian $h$ is rotationally invariant, the single-particle orbitals $\ket{\lambda}$ are characterized by the standard set of central field quantum numbers for an electron, that is, $(n\ell m_\ell m_s)$. Also, the spatial part of the orbitals is given by

:::{math}
:label: eq-atomstruc-4
u_\lambda(\rvec) = R_{n\ell}(r) Y_{\ell m_\ell}(\theta,\phi),
:::

for some radial wave functions $R_{n\ell}(r)$ that are determined by solving the pseudo-Schr\"odinger equation {eq}`eq-atomstruc-2`. Each orbital $\ket{\lambda}$ is associated with an energy $\epsilon_\lambda=\epsilon_{n\ell}$, an eigenenergy of the Hamiltonian $h(\rvec,\pvec)$ that only depends on the quantum numbers $n$ and $\ell$, as usual for a central force problem.

The orbitals $\ket{\lambda}$ that go into the Slater determinant $\Phi$ must be linearly independent, so the quantum numbers $\lambda=(n\ell m_\ell m_s)$ of the orbitals must be distinct. Since the orbitals are eigenstates of the single-particle Hamiltonian $h$, they are, in fact, orthonormal. The Hamiltonian $h$ has an infinite number of eigenstates, so we must choose $N$ of them to form the Slater determinant and to compute the self-consistent potentials $V_d$ and $V_{ex}$ while carrying out the iteration to solve the Hartree-Fock equations. When we obtain the Hartree-Fock estimate for the energy, the result will depend only on the quantum numbers $(n\ell)$, and not on the magnetic quantum numbers $(m_\ell,m_s)$. Equivalently, the estimate for the energy will depend only on the number of occupied orbitals in each subshell. As explained in {ref}`sec-hartfock-16`, the list of occupation numbers is called the *electron configuration*.

::::{table} Electron configurations for some atoms. $\Ar$ refers to the argon core, $1s^2\,2s^2\,2p^6\,3s^2\,3p^6$, while $\Rn$ refers to the radon core, $\Ar 3d^{10}\,4s^2\,4p^6\,4d^{10}\,4f^{14}\,5s^2\,5p^6\,5d^{10}\,6s^2\,6p^6$.
:label: tbl-atomstruc-1

:::{table}
| Atom | Z | Config        |
| :---: | :-: | :------------ |
| H    | 1  | $1s$          |
| He   | 2  | $1s^2$        |
| Li   | 3  | $1s^2 2s$     |
| Be   | 4  | $1s^2 2s^2$   |
| B    | 5  | $1s^2 2s^2 2p$|
| C    | 6  | $1s^2 2s^2 2p^2$|
| N    | 7  | $1s^2 2s^2 2p^3$|
| O    | 8  | $1s^2 2s^2 2p^4$|
| F    | 9  | $1s^2 2s^2 2p^5$|
| Ne   | 10 | $1s^2 2s^2 2p^6$|
| Na   | 11 | $1s^2 2s^2 2p^6 3s$|
| Mg   | 12 | $1s^2 2s^2 2p^6 3s^2$|
:::
:::{table}
| Atom | Z  | Config               |
| :---: | :-: | :------------------- |
| K    | 19 | $[\mathrm{Ar}] 4s$     |
| Ca   | 20 | $[\mathrm{Ar}] 4s^2$   |
| Sc   | 21 | $[\mathrm{Ar}] 3d^1 4s^2$ |
| Ti   | 22 | $[\mathrm{Ar}] 3d^2 4s^2$ |
| V    | 23 | $[\mathrm{Ar}] 3d^3 4s^2$ |
| Cr   | 24 | $[\mathrm{Ar}] 3d^5 4s^1$ |
| Mn   | 25 | $[\mathrm{Ar}] 3d^5 4s^2$ |
| Fe   | 26 | $[\mathrm{Ar}] 3d^6 4s^2$ |
| Co   | 27 | $[\mathrm{Ar}] 3d^7 4s^2$ |
| Ni   | 28 | $[\mathrm{Ar}] 3d^8 4s^2$ |
| Cu   | 29 | $[\mathrm{Ar}] 3d^{10} 4s^1$ |
| Zn   | 30 | $[\mathrm{Ar}] 3d^{10} 4s^2$ |
:::
:::{table}
| Atom | Z  | Config                    |
| :---: | :-: | :------------------------ |
| Fr   | 87 | $[\mathrm{Rn}] 7s^1$        |
| Ra   | 88 | $[\mathrm{Rn}] 7s^2$        |
| Ac   | 89 | $[\mathrm{Rn}] 6d^1 7s^2$   |
| Th   | 90 | $[\mathrm{Rn}] 6d^2 7s^2$   |
| Pa   | 91 | $[\mathrm{Rn}] 5f^2 6d^1 7s^2$ |
| U    | 92 | $[\mathrm{Rn}] 5f^3 6d^1 7s^2$ |
| Np   | 93 | $[\mathrm{Rn}] 5f^4 6d^1 7s^2$ |
| Pu   | 94 | $[\mathrm{Rn}] 5f^6 7s^2$   |
| Am   | 95 | $[\mathrm{Rn}] 5f^7 7s^2$   |
| Cm   | 96 | $[\mathrm{Rn}] 5f^7 6d^1 7s^2$ |
| Bk   | 97 | $[\mathrm{Rn}] 5f^9 7s^2$   |
| Cf   | 98 | $[\mathrm{Rn}] 5f^{10} 7s^2$ |
:::
::::

Different choices of electron configuration lead to different estimates of the ground state energy; we must choose the one that gives the smallest estimate. This gives the electron configuration for the ground state of the atom, as tabulated in references (for example, periodic tables of the elements). As we move from one atom to the next, the sequence of electron configurations reveals a filling sequence, that is, a sequence of subshells that are filled. See {ref}`tbl-atomstruc-1`. For atoms of small $Z$, the sequence proceeds like this: $1s$, $2s$, $2p$, $3s$, etc. However, for heavier atoms there may be some competition between subshells, for example, in the transition elements the $4s$ and $3d$ subshells have nearly the same energy, so as we move from one element to the next, the next electron may go into the $3d$ or $4s$ subshell, whichever is energetically favorable, or it may go into the $3d$ subshell while borrowing another electron from the $4s$ subshell. This phenomenon was explained in terms of the exchange energy in {ref}`sec-hartfock-13`. Thus in the case of atoms of small $Z$ the electron configuration for the ground state consists of a series of complete subshells plus a final subshell that may be incomplete, for example, carbon has the configuration $1s^22s^22p^2$, in which the $2p$ subshell is incomplete (it has six orbitals but only two are filled). But heavier atoms such as the transition elements may have more than one incomplete subshell, for example, chromium has the configuration $1s^22s^22p^63s^23p^63d^54s$, in which the $3d$ subshell with ten orbitals has only five filled, and the $4s$ subshell with two orbitals has only one filled. We might mention that while in hydrogen the $4s$ subshell has a higher energy than the $3d$, in heavier atoms the self-consistent potentials do not follow the rules of hydrogen.

{ref}`tbl-atomstruc-1` contains a partial table of electron configurations which shows these features of the subshell filling sequence. The table includes a list of low-$Z$ atoms, a list of transition elements showing the competition between the $3d$ and $4s$ subshells, and a list of actinides, showing the competition between the $5f$, $6d$ and $7s$ subshells.

To summarize, for a given atom, Hartree-Fock theory, combined with averaging of the potentials, gives us an electron configuration; a set of self-consistent, rotationally invariant potentials ${\bar V}_d$ and ${\bar V}_{ex}$; a set of eigenenergies $\epsilon_{n\ell}$; and a set of single particle orbitals $\ket{\lambda}$ where $\lambda=(n\ell m_\ell m_s)$. Actually, since the self-consistent potentials can be determined from the orbitals, it suffices just to give the orbitals; and since the orbitals are central force eigenfunctions as in {eq}`eq-atomstruc-4`, it suffices to just give the radial wave functions. For example, for carbon with configuration $1s^22s^22p^2$ it suffices to give (in addition to the configuration) the radial wave functions $R_{1s}$, $R_{2s}$ and $R_{2p}$ and the eigenenergies $\epsilon_{1s}$, $\epsilon_{2s}$ and $\epsilon_{2p}$. These radial functions and energies can only be found numerically.

(sec-atomstruc-3)=

## The Central Field Approximation

The Slater determinant $\ket{\Phi}$ that emerges from Hartree-Fock theory is not only a variational estimate to the ground state wave function, it is also an exact eigenstate of the multi-particle Hamiltonian,

:::{math}
:label: eq-atomstruc-5
H_0 = \sum_{i=1}^N h(\rvec_i,\pvec_i),
:::

that is,

:::{math}
:label: eq-atomstruc-6
H_0 \ket{\Phi} = E_0 \ket{\Phi}.
:::

This is because each of the $N!$ terms of the Slater determinant consists of the same orbitals, just permuted among the electrons, but $H_0$ brings out the total energy given by

:::{math}
:label: eq-atomstruc-7
E_0 = \sum_\lambda \epsilon_\lambda = \sum_{n\ell} \nu_{n\ell}\, \epsilon_{n\ell},
:::

which is invariant under permutations and is the same for all $N!$ terms. Here in the last sum $\nu_{n\ell}$ is the occupation number of subshell $(n\ell)$, that is, the number of electrons in that subshell. Note that although the ground eigenstate $\ket{\Phi}$ of $H_0$ is the Hartree-Fock estimate to the ground state eigenfunction of the atom, $E_0$ is not the Hartree-Fock estimate to the energy, since it double counts the direct and exchange potential energies among the electrons. See {eq}`eq-hartfock-97`, which shows that $E_0$ is too high. We will show how to correct this energy in a moment.

The Hamiltonian $H_0$ represents what is called the *central field approximation* to the atom. It is a cruder model than the basic $N$-electron atom Hamiltonian {eq}`eq-atomstruc-1`. It has more symmetry than that Hamiltonian, which is invariant under spatial rotations of the entire $N$-electron system, generated by $\Lvec=\sum_i \Lvec_i$, but not under spatial rotations of the individual electrons, generated by the individual angular momenta $\Lvec_i$. The central field Hamiltonian $H_0$, however, is invariant under the rotations of individual electrons, that is, it commutes with each $\Lvec_i$ individually. It is a general rule in applications of quantum mechanics that the more idealized the model, the more symmetry there is and thus a higher degree of degeneracy. We will examine the degeneracy of $H_0$ in more detail below.

(sec-atomstruc-4)=

## Coupling Schemes

We can make the central field Hamiltonian $H_0$ the basis of a perturbation expansion by writing $H=H_0+H_1$, where

:::{math}
:label: eq-atomstruc-8a
\begin{aligned}
H_0 &= \sum_{i=1}^N h(\rvec_i,\pvec_i) = \sum_{i=1}^N \Bigl[ {p_i^2 \over 2} - {Z\over r_i} + {\bar V}_d(r_i) - {\bar V}_{ex,i}\Bigr],
\end{aligned}
:::

:::{math}
:label: eq-atomstruc-8b
\begin{aligned}
H_1 &= \sum_{i<j} {1\over r_{ij}} - \sum_{i=1}^N \Bigl[{\bar V}_d(r_i) - {\bar V}_{ex,i}\Bigr].
\end{aligned}
:::

Here $H_0$ is the central field Hamiltonian {eq}`eq-atomstruc-5` and $H_1$ is written so that $H=H_0+H_1$ is the basic $N$-electron atom Hamiltonian {eq}`eq-atomstruc-1`. That is, we have added and subtracted the direct and exchange potentials inside $H$ to make $H_0+H_1$.

The term $H_1$ in {eq}`eq-atomstruc-8b` consists of the exact interelectron Coulomb interactions, that is, the term $\sum_{i<j} 1/r_{ij}$, minus the rotational average of the direct minus exchange potentials, summed over electrons. This is sometimes called the “residual Coulomb potential.” If the rotational averaging provides a good approximation to the exact interelectron Coulomb interactions, then the term $H_1$ should be much smaller than the exact interelectron interactions. The exact interelectron Coulomb interactions are too big to treat by perturbation theory (apart from the case of helium, where the results are not very satisfactory from a numerical standpoint), but with the rotational average subtracted off, the result, the term $H_1$ above, is small enough for a successful perturbation treatment. That is, we have $H_1 \ll H_0$. We shall outline this perturbation treatment below.

But if $H_1$ is now a small term, the question arises, how does it compare to other small terms we have neglected so far, such as the fine structure terms? To take these into account as well, we shall contemplate another term in the Hamiltonian,

:::{math}
:label: eq-atomstruc-9
H_2 = \sum_{i=1}^N \xi(r_i) \Lvec_i \cdot \Svec_i,
:::

which is the sum of the spin-orbit interactions for each electron. The quantity $\xi(r)$ is a function of the radius of the electron (see {eq}`eq-finestruc-13` whose details will not concern us. The spin-orbit term is only one of several fine structure terms, most of which we are omitting for simplicity, and even the spin-orbit term is treated somewhat schematically. Our goal will be to give a qualitative understanding of the effects of the fine structure terms without going into detail.

But to return to the question posed, what is the quantitative relation between $H_1$ and $H_2$? It turns out that the answer depends on $Z$. In low $Z$ atoms near the beginning of the periodic table, we have $H_2 \ll H_1 \ll H_0$. For such atoms, it makes sense to first treat $H_1$ as a perturbation on $H_0$, find the eigenstates of $H_0+H_1$, then to treat $H_2$ as a second perturbation on top of $H_0+H_1$. This scheme involves classifying the eigenstates of $H_0+H_1$ by their good quantum numbers, including $L$ and $S$, as discussed in \secratomstruc-7 below. This scheme is called $LS$- or *Russell-Saunders coupling*. For high $Z$ atoms, however, near the end of the periodic table, it turns out that $H_1 <\approx H_2 \ll H_0$. In this case it makes sense to first treat $H_2$ as a perturbation on top of $H_0$, then to treat $H_1$ as a perturbation on top of $H_0+H_2$. This scheme is called *$jj$-coupling*, on account of the quantum numbers that arise in it. In these notes we consider only $LS$-coupling.

(sec-atomstruc-5)=

## The Unperturbed System in $LS$-Coupling

Let us therefore consider $H_1$ as a perturbation on top of $H_0$. As usual in perturbation theory, we must first understand the unperturbed system, its eigenstates and eigenvalues, and in particular its degeneracies, since those affect how the perturbation calculation is carried out. The ground state energy of $H_0$ is $E_0$, shown in {eq}`eq-atomstruc-7`, and the Slater determinant $\ket{\Phi}$ composed of central field orbitals is a ground state eigenfunction of $H_0$. Each subshell contains $2(2\ell+1)$ orbitals, each of which has the same energy $\epsilon_{n\ell}$, but not all the orbitals are necessarily occupied by electrons. In complete subshells, in which all the orbitals are occupied, there is only one way to assign orbitals to the electrons. But if there are any incomplete subshells, then there is more than one way to assign central field orbitals without changing the energy $E_0$, since the energy $E_0$ does not depend on the assignment of magnetic quantum numbers $(m_\ell,m_s)$ to the orbitals. Thus, if there are any incomplete subshells, the ground state of $H_0$ is degenerate, and the degenerate eigenfunctions are the Slater determinants specified by the choices of magnetic quantum numbers for the orbitals in incomplete subshells.

To distinguish the various Slater determinants with different magnetic quantum numbers, we will replace the notation $\ket{\Phi}$ with $\mset$, where “$m$-set” refers to the magnetic quantum numbers in incomplete subshells only. We do not need to specify the magnetic quantum numbers in complete subshells, since there is only one possible assignment for those. Here the electron configuration is understood, which specifies which subshells are incomplete and how many electrons they contain. In the equation,

:::{math}
:label: eq-atomstruc-10
H_0 \mset = E_0 \mset,
:::

a version of {eq}`eq-atomstruc-6`, the energy $E_0$ depends on the configuration but not on the $m$-set, and the order of the degeneracy is the number of possible $m$-sets.

Notice that in assigning orbitals to electrons the order of the assignment does not matter, since all electrons are permuted among all orbitals by the Slater determinant. All that matters is which orbitals are assigned, that is, the list of assigned orbitals. More precisely, if we change the order in which the orbitals are assigned to the electrons, the Slater determinant will change sign if the rearrangement of the orbitals amounts to an odd permutation. Apart from this sign, the order does not matter, and even the sign is pinned down if we put the orbitals in a standard order when assigning them. Therefore the number of distinct assignments of $n$ electrons to orbitals in a subshell containing $s=2(2\ell+1)$ slots is the binomial coefficient $\begin{pmatrix}s \cr n \cr\end{pmatrix}$, which is the number of distinct unordered subsets of $n$ elements taken from a set of $s$ elements. This is the number of distinct $m$-sets possible for the given subshell. As explained above, for low $Z$ atoms the electron configuration has only one incomplete subshell, so the degeneracy of the ground state is a single binomial coefficient for that subshell. For heavier atoms there may be more than one incomplete subshell, in which case the degeneracy is the product of the binomial coefficients, one for each incomplete subshell.

(sec-atomstruc-6)=

## Enumerating $m$-sets

Consider, for example, B (boron), with electron configuration $1s^22s^22p$. There is one electron in the one incomplete ($2p$) subshell. Since this subshell contains $2(2\ell+1)=6$ slots (for $\ell=1$), there are six possible $m$-sets, and the ground state energy $E_0$ is six-fold degenerate. The degeneracy is given by the binomial coefficient,

:::{math}
:label: eq-atomstruc-11
\begin{pmatrix}6\\ 1\\\end{pmatrix} = 6.
:::

See {ref}`tbl-atomstruc-2`.

:::{table} Allowed $m$-sets for boron, with configuration $1s^22s^22p$.
:label: tbl-atomstruc-2

|   | $m_\ell$ | $m_s$   |
|---|----------|---------|
| 1 | 1        | $1/2$   |
| 2 | 1        | $-1/2$  |
| 3 | 0        | $1/2$   |
| 4 | 0        | $-1/2$  |
| 5 | -1       | $1/2$   |
| 6 | -1       | $-1/2$  |

:::
Now consider carbon, with configuration $1s^22s^22p^2$, whose $m$-sets are listed in {ref}`tbl-atomstruc-3`. There are now two electrons in the incomplete $2p$ subshell, so the degeneracy is

:::{math}
:label: eq-atomstruc-12
\begin{pmatrix}6\\ 2\\\end{pmatrix}=15.
:::

Since there are two electrons, there are now two $m_\ell$ and two $m_s$ values in an $m$-set. The table lists all combinations of $m_\ell$ pairs in descending order, that is, such that $m_{\ell1}\ge m_{\ell2}$. For example, the table contains $(m_{\ell1},m_{\ell2})=(1,0)$ but not $(m_{\ell1},m_{\ell2})=(0,1)$, which is just an exchange of quantum numbers that does not represent a distinct state. When the two $m_\ell$ values are equal, for example, in row~1 of the table where $(m_{\ell1},m_{\ell2})=(1,1)$, then only one set of $m_s$ values is given, namely, $(m_{s1},m_{s2})=(\frac{1}{2}, -\frac{1}{2})$, because if $m_{s1}=m_{s2}$ then the state vanishes, and because $(m_{s1},m_{s2})=(-\frac{1}{2},\frac{1}{2})$ is the same state as $(m_{s1},m_{s2})=(\frac{1}{2},-\frac{1}{2})$. But if the $m_\ell$ values are distinct, as for example in rows~2--5 of table where $(m_{\ell1},m_{\ell2})=(1,0)$, then all $2^2=4$ combinations of $(m_{s1},m_{s2})$ values are given, because they all represent distinct states. Proceeding in this way the table lists all possible $m$-sets, confirming that there are 15 total.

::::{table} Allowed $m$-sets for carbon, with configuration $1s^22s^22p^2$.
:label: tbl-atomstruc-3

:::{table}

| $m_{\ell 1}$ | $m_{\ell 2}$ | $m_{s 1}$ | $m_{s 2}$   |
| :-----------: | :-----------: | :--------: | :---------: |
| 1            | 1            | $1/2$      | $-1/2$      |
| 2            | 1            | $1/2$      | $-1/2$      |
| 3            | 1            | $1/2$      | $-1/2$      |
| 4            | 1            | $-1/2$     | $-1/2$      |
| 5            | 1            | $1/2$      | $-1/2$      |
| 6            | 1            | $1/2$      | $-1/2$      |
| 7            | 1            | $1/2$      | $-1/2$      |
| 8            | 1            | $-1/2$     | $1/2$       |

:::
:::{table}

| $m_{\ell 1}$ | $m_{\ell 2}$ | $m_{s 1}$ | $m_{s 2}$   |
| :-----------: | :-----------: | :--------: | :---------: |
| 9            | 0            | $-1/2$     | $-1/2$      |
| 10           | 0            | $1/2$      | $-1/2$      |
| 11           | 0            | $-1/2$     | $-1/2$      |
| 12           | 0            | $1/2$      | $-1/2$      |
| 13           | 0            | $-1/2$     | $-1/2$      |
| 14           | 0            | $-1/2$     | $-1/2$      |
| 15           | 0            | $1/2$      | $-1/2$      |
| 16           | -1           | $1/2$      | $-1/2$      |

:::
::::

::::{table} Allowed $m$-sets for nitrogen, with configuration $1s^22s^22p^3$.
:label: tbl-atomstruc-4
:::{table}

| $m_{\ell 1}$ | $m_{\ell 2}$ | $m_{\ell 3}$ | $m_{s 1}$ | $m_{s 2}$ | $m_{s 3}$ |
| :-----------: | :-----------: | :-----------: | :--------: | :--------: | :--------: |
| 1            | 1            | 1            | $1/2$      | $-1/2$     | $1/2$      |
| 2            | 1            | 1            | $1/2$      | $-1/2$     | $-1/2$     |
| 3            | 1            | 1            | $1/2$      | $1/2$      | $-1/2$     |
| 4            | 1            | 1            | $-1/2$     | $-1/2$     | $-1/2$     |
| 5            | 1            | 0            | $1/2$      | $1/2$      | $1/2$      |
| 6            | 1            | 0            | $-1/2$     | $1/2$      | $-1/2$     |
| 7            | 1            | 0            | $-1/2$     | $1/2$      | $1/2$      |
| 8            | 1            | 0            | $1/2$      | $1/2$      | $-1/2$     |
| 9            | 1            | -1           | $1/2$      | $1/2$      | $-1/2$     |
| 10           | 1            | -1           | $1/2$      | $-1/2$     | $-1/2$     |

:::
:::{table}

| $m_{\ell 1}$ | $m_{\ell 2}$ | $m_{\ell 3}$ | $m_{s 1}$ | $m_{s 2}$ | $m_{s 3}$ |
| :-----------: | :-----------: | :-----------: | :--------: | :--------: | :--------: |
| 11           | 1            | 0            | $-1/2$     | $1/2$      | $1/2$      |
| 12           | 1            | 0            | $-1/2$     | $1/2$      | $-1/2$     |
| 13           | 1            | 0            | $-1/2$     | $-1/2$     | $-1/2$     |
| 14           | 1            | 0            | $1/2$      | $-1/2$     | $-1/2$     |
| 15           | 1            | -1           | $1/2$      | $1/2$      | $-1/2$     |
| 16           | 1            | -1           | $-1/2$     | $1/2$      | $-1/2$     |
| 17           | 0            | 0            | $1/2$      | $1/2$      | $1/2$      |
| 18           | 0            | 0            | $-1/2$     | $1/2$      | $-1/2$     |
| 19           | 0            | -1           | $1/2$      | $1/2$      | $-1/2$     |
| 20           | 0            | -1           | $-1/2$     | $1/2$      | $-1/2$     |

:::
::::
As a final example, consider nitrogen, with configuration $1s^22s^22p^3$. The number of $m$-sets is

:::{math}
:label: eq-atomstruc-13
\begin{pmatrix}6\\ 3\\\end{pmatrix} = 20.
:::

These are listed in {ref}`tbl-atomstruc-4`. The $m_{\ell}$ triplets are listed in descending order, that is, $m_{\ell1}\ge m_{\ell2}\ge m_{\ell3}$, but triplets with the same values, that is, $m_{\ell1} =m_{\ell2}=m_{\ell3}$, are omitted, since for those it is impossible to assign electron spin quantum numbers $m_s=\pm\frac{1}{2}$ without creating a duplicate and hence a zero state. In cases where two $m_\ell$'s are equal and one different, for example, rows~1--2 with $(m_{\ell1}, m_{\ell2}, m_{\ell3})=(1,1,0)$, the identical $m_\ell$ values are matched with $m_s=\frac{1}{2}$ and $m_s=-\frac{1}{2}$, and the odd $m_\ell$ is matched with $m_s=\pm\frac{1}{2}$, giving a total of two states. In cases where all three $m_\ell$'s are distinct, for example, rows~7--14 of the table for which $(m_{\ell1}, m_{\ell2}, m_{\ell3}) =(1,0,-1)$, all possible $m_s$ values are assigned, giving $2^3=8$ distinct states. The number of distinct $m$-sets in the table is 20, agreeing with the binomial coefficient {eq}`eq-atomstruc-13`.

(sec-atomstruc-7)=

## Good Quantum Numbers of the Basic $N$-electron Atom Hamiltonian

We see that if the electron configuration contains any incomplete subshells then the ground state of $H_0$ is degenerate. This means that we can expect the ground state of $H_0$ to split when the perturbation $H_1$ is turned on, and that in principle we will have to diagonalize a matrix to find the energy shifts. As usual in perturbation theory, it helps to employ a basis in the perturbation calculation that is an eigenbasis of a set of commuting operators, in which as many as possible of the operators commute with the perturbation. See {ref}`sec-finestruc-8`. In the present case, the operators that commute with $H_1$ are the same that commute with $H=H_0+H_1$, that is, the operators in question commute with the basic $N$-electron Hamiltonian {eq}`eq-atomstruc-1`.

These operators were discussed in {ref}`sec-hartfock-2`, and include $\Lvec$, $\Svec$ and $\pi$. If we ask for a list of operators that commute with $H$ and with each other, then a suitable choice is $L^2$, $L_z$, $S^2$, $S_z$ and $\pi$. Thus the eigenstates of $H=H_0+H_1$ can rigorously be characterized by their quantum numbers $(LM_LSM_S\pi)$ (using $\pi$ both for the parity operator and its eigenvalue). The Slater determinant $\mset$, however, is an eigenstate only of $L_z$, $S_z$ and $\pi$, and not, in general, of $L^2$ and $S^2$.

To see this consider first

:::{math}
:label: eq-atomstruc-14
L_z = \sum_{i=1}^N L_{iz},
:::

the $z$-component of orbital angular momentum, summed over all the electrons. When this is applied to a single term in a Slater determinant $\mset$, each operator $L_{iz}$ brings out the value $m_{\ell i}$, the $m_\ell$~value of the orbital assigned to electron $i$ in the given term. Thus $L_z$ brings out the sum of these values, $\sum_i m_{\ell i}$. There are $N!$ terms in the Slater determinant, but these consist of permuting orbitals among electrons, and this sum is invariant under such permutations. Thus the sum is the same for all the $N!$ terms of the Slater determinant, and we have

:::{math}
:label: eq-atomstruc-15
L_z \mset = \Bigl(\sum_{i=1}^N m_{\ell i}\Bigr) \mset.
:::

Similarly, we have

:::{math}
:label: eq-atomstruc-16
S_z \mset = \Bigl(\sum_{i=1}^N m_{s i}\Bigr) \mset.
:::

As for parity, the operator $\pi$ maps all position vectors $\rvec_i$ into $-\rvec_i$, and so brings out a factor $(-1)^{\ell_i}$ from the orbital with angular momentum quantum number $\ell_i$. The product of these factors is invariant under permutations and therefore the same for all the terms of the Slater determinant, and we have

:::{math}
:label: eq-atomstruc-17
\pi\mset = \Bigl[\prod_{i=1}^N (-1)^{\ell_i}\Bigr] \mset.
:::

The parity eigenvalue depends only on the electron configuration, which specifies the $\ell$ quantum numbers for all the electrons. In the following discussion we will be concentrating on the fixed ground state configuration of an atom, so the parity quantum number will be fixed and will not play a large role in the subsequent considerations.

In summary, the Slater determinant $\mset$ composed of central field orbitals is an eigenstate of $L_z$, $S_z$ and $\pi$ with quantum numbers

:::{math}
:label: eq-atomstruc-18
M_L = \sum_{i=1}^N m_{\ell i}, \qquad M_S =  \sum_{i=1}^N m_{s i}, \qquad \pi = \prod_{i=1}^N (-1)^{\ell_i}.
:::

Actually, the sums and products in these eigenvalues can be taken over incomplete subshells only, since the sums $\sum_i m_{\ell i}$ and $\sum_i m_{si}$ are 0 when taken over complete subshells, and the product $\prod_i (-1)^{\ell_i}$ is 1 when taken over complete subshells. Thus, the eigenvalues of $M_L$ and $M_S$ depend only on the $m$-set. As for the parity $\pi$, it is independent of the $m$-set and depends only on the configuration.

A similar argument does not work, however, for the operators $L^2$ and $S^2$. The individual terms of a given Slater determinant $\mset$ are not in general eigenstates of these operators, and neither is the sum. The Slater determinants $\mset$, for the $m$-sets allowed by the configuration, span the ground eigenspace of $H_0$, but they diagonalize only the symmetry operators $L_z$, $S_z$ and $\pi$, not $L^2$ and $S^2$.

(sec-atomstruc-8)=

## A Symmetry Adapted Basis

Let us denote the ground eigenspace of $H_0$ by $\ES_0$. This space is spanned by the Slater determinants $\mset$, where the $m$-sets run over all allowed by the incomplete subshells (for example, 15 in the case of carbon). Thus in first order perturbation theory we need in principle to diagonalize the matrix $\matrixelement{\\text{m}-set}{H_1}{\\text{m-set}^{\prime}}$ to find the energy shifts, which give us the energy eigenvalues of $H=H_0+H_1$ that grow out of $E_0$ as $H_1$ is switched on.

This matrix may be large (for example, it is $15\times15$ in the case of carbon), so it will help to choose a good basis to simplify the diagonalization. The best basis is an eigenbasis of a set of commuting, good quantum numbers, such as $(L^2,S^2,L_z,S_z)$, as discussed in \secratomstruc-7. We omit $\pi$ from the list since it is constant on $\ES_0$ (all basis states $\mset$ have the same parity). The set of Slater determinants $\mset$ is not such a basis, since it is not an eigenbasis of $L^2$ or $S^2$, in general.

The operators $(L^2,S^2,L_z,S_z)$ commute with $H_0$ and so can be restricted to $\ES_0$ (see {ref}`sec-hilbert-23`). Also, since they commute with each other, they possess simultaneous eigenspaces inside $\ES_0$. These simultaneous eigenspaces are characterized by the quantum numbers $(L,S,M_L,M_S)$ of the operators $(L^2,S^2,L_z,S_z)$. If any of these eigenspaces are multidimensional, that is, if there is any degeneracy inside $\ES_0$ remaining after the quantum numbers $(L,S,M_L,M_S)$ are specified, then we can introduce an index $\gamma$ to label an arbitrarily chosen orthonormal basis inside the eigenspaces. In this way we conclude that there is an orthonormal basis inside $\ES_0$ that we can label by $\ket{\gamma LSM_LM_S}$. Furthermore, we can show that if $\gamma$, $L$ and $S$ are held fixed, then the basis vectors with different values of $M_L$ and $M_S$ are related by the raising and lowering operators, $L_\pm$ and $S_\pm$. This is a way of saying that $\ES_0$ breaks up into irreducible subspaces under both purely orbital and purely spin rotations, which in turn is a consequence of the fact that $\ES_0$ is invariant under both orbital and spin rotations.

Actually, as it turns out, for small $Z$ the simultaneous eigenspaces of $(L^2,S^2,L_z,S_z)$ inside $\ES_0$ are nondegenerate, so the index $\gamma$ is not needed. The first element for which such a degeneracy appears is vanadium, with $Z=23$. For simplicity in the following we will suppress the index $\gamma$, since the examples we will deal with have $Z<23$ (but see Prob.~\prbratomstruc-1).

So to find a good basis for perturbation theory, we must find the basis vectors $\ket{LSM_LM_S}$ inside $\ES_0$ as linear combinations of the Slater determinants $\mset$. We write these linear combinations schematically as

:::{math}
:label: eq-atomstruc-19
\ket{LSM_LM_S} = \sum_{\\text{m}-sets} (coefs) \mset.
:::

Once we have found the coefficients, then we can compute the matrix elements of $H_1$ inside $\ES_0$ with respect to the new basis,

:::{math}
:label: eq-atomstruc-20
\matrixelement{LSM_LM_S}{H_1}{LSM_LM_S}.
:::

Since $H_1$ commutes with all of the operators $(L^2,S^2,L_z,S_z)$, it is diagonal in the basis $\ket{LSM_LM_S}$ and the energy shifts are the diagonal elements {eq}`eq-atomstruc-20`. (The off-diagonal elements vanish, and there is no need for primes on one side or the other in {eq}`eq-atomstruc-20`.) Moreover, since $H_1$ is invariant under both spatial and spin rotations, the energy shifts do not depend on the quantum numbers $M_L$ or $M_S$. Thus, after the perturbation is turned on, the energies depend on $L$ and $S$, and are $(2L+1)(2S+1)$-fold degenerate. In general, the unperturbed energy level $E_0$ will split into more than one energy level, each characterized by a value of $L$ and $S$.

The values of $L$ and $S$ that occur for a given atom are called *multiplets*. These are the energy levels of low-$Z$ atoms that are seen experimentally, at a resolution at which fine structure can be ignored. Understanding the multiplets, such as which ones occur and in what order, constitutes a basic understanding of the structure of multielectron atoms.

Determining the coefficients in the expansion {eq}`eq-atomstruc-19` is somewhat like the problem of finding Clebsch-Gordan coefficients, but it is more complicated because there are two distinct kinds of angular momenta, orbital and spin, because the number of individual angular moments (the $\Lvec_i$ and $\Svec_i$ for the electrons in the incomplete subshells) that must be added is in general more than two, and because of the requirements of antisymmetry. Still, it is not that hard (see Prob.~\prbratomstruc-2). For the time being, however, we shall concentrate on a simpler problem, which is to determine which multiplets (which values of $L$ and $S$) occur in $\ES_0$. This is necessary in any case before we can compute the coefficients in {eq}`eq-atomstruc-19`.

(sec-atomstruc-9)=

## Determining the Multiplets

The spectroscopic notation for a multiplet with given $L$ and $S$ is ${}^{2S+1}L$, where $L$ is replaced by one of the code letters, $S$, $P$, $D$, $F$, etc., for $L=0,1,2,3, \ldots$. We will now determined the multiplets inside the ground state eigenspace of $H_0$ for several different atoms.

For any atom with complete subshells, for example, beryllium with configuration $1s^22s^2$ or neon with configuration $1s^22s^22p^6$, there is only one multiplet, ${}^1S$ (that is, $L=0$ and $S=0$), which is pronounced, “singlet-$S$.” For such atoms, there is only one way to assign orbitals to electrons, and therefore only a single Slater determinant, which spans the one-dimensional eigenspace $\ES_0$. Now since $\ES_0$ is invariant under both spatial and spin rotations, it must break up into irreducible subspaces under both kinds of rotations. But a one-dimensional space can only hold the value 0 of angular momentum, since all higher values have multi-dimensional irreducible subspaces. Therefore only the values $L=0$ and $S=0$ are allowed.

In atoms with incomplete subshells, the allowed multiplets are determined by the incomplete subshells only. This is because the other (complete) subshells have $L=0$ and $S=0$, which do not contribute to the total $L$ and $S$ of the atom.

In the case of boron there is one electron in the incomplete shell $2p$, and the $m$-sets are given in {ref}`tbl-atomstruc-2`. The total orbital and spin angular momentum of the atom are the same as the orbital and spin of this one electron, that is, $L=\ell=1$ and $S=s=1/2$. Thus there is one multiplet, ${}^2P$ (pronounced “doublet-$P$”). It has a degeneracy $2\times3=6$, the same as the binomial coefficient {eq}`eq-atomstruc-11`.

:::{table} Multiplets in the ground configuration $1s^22s^22p^2$ of carbon.
:label: tbl-atomstruc-5

| $L$ | $S$ | multiplet | degen        |
| :-: | :-: | :-------- | :----------- |
| 0 | 0     | $^1S$     | $1 \times 1 = 1$ |
| 1 | 1     | $^3P$     | $3 \times 3 = 9$ |
| 2 | 0     | $^1D$     | $1 \times 5 = 5$ |
| total |    |           | 15           |

:::
In the case of carbon there are two $2p$ electrons. We can determine the allowed multiplets by a special method that only works for two equivalent electrons. Here the word “equivalent” means, belonging to the same subshell. Both electrons have $\ell=1$. When we combine two angular momenta $\ell=1$, we obtain $1\otimes1 = 0\oplus 1 \oplus 2$, that is, $L=0$, $1$ or $2$. Of these, $L=2$ is symmetric under exchange of the electrons, $L=1$ is antisymmetric, and $L=0$ is symmetric. In general, when we combine two angular momenta, the maximum value of total angular momentum is symmetric under exchange, and the exchange symmetry alternates as we decrease that value down to 0. See Prob. {ref}`prob-identpart-2`. Similarly, when we combine the spins of the two electrons, we get $\frac{1}{2} \otimes \frac{1}{2} = 0 \oplus 1$, that is $S=0$ or $S=1$, of which $S=1$ is symmetric under exchange of electrons and $S=0$ is antisymmetric. Now since the overall wave function must be antisymmetric, we can have a state that is symmetric under orbital exchange and antisymmetric under spin exchange, or vice versa. Thus the possibilities are $L=0$, $S=0$, or ${}^1S$; $L=1$ and $S=1$, or ${}^3P$; and $L=2$ and $S=0$, or ${}^1D$. These multiplets are pronounced, “singlet-$S$,” “triplet-$P$,” and “singlet-$D$.” These possibilities are enumerated in {ref}`tbl-atomstruc-5` along with the degeneracies, that is, the dimensionalities of the subspaces of a given multiplet. These dimensionalities add up to 15, as they must.

We now present a tabular way of getting the multiplets for carbon which can be generalized to more than two equivalent electrons. {ref}`tbl-atomstruc-6`, which is an expanded version of {ref}`tbl-atomstruc-3`, shows the work. The logic is similar to that employed in the determining the allowed values of $j$ and $m$ when coupling angular momenta (see {ref}`sec-jjcouple-10`).


:::{table} A tabular way of getting the multiplets in carbon.
:label: tbl-atomstruc-6

|   | $m_{\ell 1}$ | $m_{\ell 2}$ | $m_{s 1}$ | $m_{s 2}$ | $M_L$ | $M_S$ | $L$ | $S$ | multiplet | degen |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | 1 | 1 | 1/2 | -1/2 | 2 | 0 | 2 | 0 | $^1D (\uparrow)$ | $1 \times 5 = 5$ |
| 2 | 1 | 0 | 1/2 | 1/2 | 1 | 1 | 1 | 1 | $^3P (\uparrow)$ | $3 \times 3 = 9$ |
| 3 | 1 | 0 | 1/2 | -1/2 | 1 | 0 | $\S$ | | | |
| 4 | 1 | 0 | -1/2 | 1/2 | 1 | 0 | $\dag$ | | | |
| 5 | 1 | 0 | -1/2 | -1/2 | 1 | -1 | $\dag$ |  |  |  |
| 6 | 1 | -1 | 1/2 | 1/2 | 0 | 1 | $\dag$ | | | |
| 7 | 1 | -1 | 1/2 | -1/2 | 0 | 0 | $\S$ | | | |
| 8 | 1 | -1 | -1/2 | 1/2 | 0 | 0 | $\dag$ | | | |
| 9 | 1 | -1 | -1/2 | -1/2 | 0 | -1 | $\dag$ | | | |
| 10 | 1 | 0 | 1/2 | -1/2 | 0 | 0 | 0 | 0 | $^1S (\ddagger)$ | $1 \times 1 = 1$ |
| 11 | 0 | -1 | 1/2 | 1/2 | -1 | 1 | $\dag$ | | | |
| 12 | 0 | -1 | 1/2 | -1/2 | -1 | 0 | $\S$ | | | |
| 13 | 0 | -1 | -1/2 | 1/2 | -1 | 0 | $\dag$ | | | |
| 14 | 0 | -1 | -1/2 | -1/2 | -1 | -1 | $\dag$ | | | |
| 15 | -1 | -1 | 1/2 | -1/2 | -2 | 0 | $\S$ | | | |
| total | | | | | | | | | | 15 |

:::
The 15 $m$-sets for carbon are listed and numbered in the first five columns of the table, after which follow two columns with the $M_L$ and $M_S$ values. The method begins with row 1, an $m$-set with $M_L=2$ and $M_S=0$. This is the highest $M_L$ value in the table, and $M_S=0$ is the highest (actually, the only) value that occurs with $M_L=2$. Therefore this $m$-set is a nondegenerate simultaneous eigenstate of $L_z$ and $S_z$ with eigenvalues $2$ and $0$, respectively. Now since $L^2$ and $S^2$ both commute with $L_z$ and $S_z$, this state must be an eigenstate of both $L^2$ and $S^2$, according to Theorem {ref}`thm-hilbert-5`. But what are the quantum numbers of $L^2$ and $S^2$, that is, what are $L$ and $S$? First, $L$ cannot be less than 2 because that would violate the rule $M_L\le L$. Nor can $L$ be greater than 2, because if it were, we could apply a raising operator $L_+$ to this state and obtain a state with $M_L=3$. But there is no state with $M_L=3$. Therefore we must have $L=2$. A similar logic shows that $S$ must be 0 for this state. This means that $m$-set number 1 is the doubly stretched state of a multiplet with $L=2$ and $S=0$, that is, the multiplet ${}^1D$, as shown in the table. The multiplet is marked with the symbol \S.

This multiplet has $(2L+1)(2S+1)=5\times1=5$ states in it, which can be obtained by applying the lowering operators $L_-$ and $S_-$ to the doubly stretched state. Actually, in this case, we need only apply $L_-$, since $S=0$. Applying $L_-$ once gives a state with $M_L=1$ and $M_S=0$. Now there are two $m$-sets with these values of $M_L$ and $M_S$, numbers 3 and 4, and number 3 is marked with the symbol \S, meaning ${}^1D$. This does not mean that if we apply $L_-$ to the $m$-set number 1 we get $m$-set number 3. It means that $m$-sets 3 and 4 span a 2-dimensional space, and if we apply $L_-$ to $m$-set number 1 we get a vector in this space, that is, a linear combination of $m$-sets numbers 3 and 4. Applying $L_-$ again we get a state with $M_L=0$, $M_S=0$, which must lie in the 2-dimensional space spanned by $m$-sets numbers 7 and 8. The first of these is marked with \S. Similarly we mark $m$-set 12 with \S, indicating one vector in the 2-dimensional space spanned by $m$-sets 12 and 13, with $M_L=-1$ and $M_S=0$, and finally we mark $m$-set 15 with \S, which spans the 1-dimensional space with $M_L=-2$ and $M_S=0$.

Next we look for the $m$-set in the table that is not marked with \S{} that has the highest $M_L$ and $M_S$ values. We find it in $m$-set number 2, which has $M_L=1$ and $M_S=1$. This must be the doubly stretched state of a multiplet with $L=1$ and $S=1$, that is, a ${}^3P$ multiplet. We mark this $m$-set and all 8 others that can be obtained from it by applying $L_-$ and $S_-$ with the symbol \dag. Finally, we look for $m$-sets that are not marked either with \S{} or \dag{} and we find $m$-set number 10, the doubly stretched state of a multiplet with $L=0$ and $S=0$, that is, the ${}^1S$ multiplet. It has only one state, which is marked with \ddag. In this way, we find the same multiplets for carbon as were given in {ref}`tbl-atomstruc-5`.

:::{table} for obtaining the multiplets in nitrogen.
:label: tbl-atomstruc-7

| | $m_{l1}$ | $m_{l2}$ | $m_{l3}$ | $m_{s1}$ | $m_{s2}$ | $m_{s3}$ | $M_L$ | $M_S$ | $L$ | $S$ | Multiplet | degen |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 1 | 1 | 1 | 0 | 1/2 | -1/2 | 1/2 | 2 | 1/2 | 2 | 1/2 | $^2D$ (§) | $2 \times 5 = 10$ |
| 2 | 1 | 1 | -1 | 1/2 | -1/2 | 1/2 | 1 | 1/2 | $\S$ | |  |  |
| 3 | 1 | 0 | 0 | 1/2 | 1/2 | -1/2 | 1 | 1/2 | 1 | 1/2 | $^2P$ (†) | $2 \times 3 = 6$ |
| 4 | 1 | 0 | -1 | 1/2 | 1/2 | 1/2 | 0 | 3/2 | 0 | 3/2 | $^4S$ (‡) | $4 \times 1 = 4$ |
| 5 | 1 | 0 | -1 | 1/2 | 1/2 | -1/2 | 0 | 1/2 | $\S$ |  |  | |
| 6 | 1 | 0 | -1 | 1/2 | -1/2 | 1/2 | 0 | 1/2 | $\dag$ |  |  | |
| 7 | 1 | 0 | -1 | -1/2 | 1/2 | 1/2 | 0 | 1/2 | $\dag$ | |  | |
| total | | | | | | | | | | |  | $20$ |

:::
The tabular method can be applied to nitrogen, with 3 equivalent electrons. A simplification is to notice that if all we want are the multiplets, it suffices to list only the $m$-sets with $M_L\ge0$ and $M_S\ge0$, since the multiplets are identified by their doubly stretched states. In the case of nitrogen, this only requires us to list 7 $m$-sets out of 20. These are shown in {ref}`tbl-atomstruc-7`. The multiplets are ${}^2D$, ${}^2P$ and ${}^4S$ (pronounced, “quartet-$S$”), and the degeneracies add up to 20, as they must.

After nitrogen we come to oxygen with configuration $1s^22s^22p^4$, which has four occupied orbitals in the $2p$ subshell and two unoccupied ones, or, as we say, two “holes.” Some experience with constructing tables as above shows that holes lead to the same multiplets as electrons. Therefore the multiplets for oxygen are the same as for carbon, that is, ${}^1S$, ${}^3P$ and ${}^1D$. Similarly, fluorine, one hole in the $2p$ subshell, has the same multiplet as boron, namely, ${}^2P$, and neon, with all subshells filled, has the one multiplet ${}^1S$.

(sec-atomstruc-10)=

## Hund's Rules and Fine Structure

{ref}`fig-atomstruc-1` shows the low-lying energy levels of carbon. The levels shown are experimental, but at the resolution of the diagram they are identical to the multiplets of the basic $N$-electron Hamiltonian {eq}`eq-atomstruc-1`. That Hamiltonian omits a number of small effects such as fine structure, but those are too small to be seen at the scale of the diagram. At higher resolution, however, many of the levels of the diagram will be seen to be split. The levels are labeled by the configuration they belong to, with even parity configurations on the left and odd ones on the right. The three multiplets we found in Tables~{ref}`tbl-atomstruc-5` and {ref}`tbl-atomstruc-6` are the three lowest levels, all of even parity, labeled as belonging to the ground state configuration $a=1s^22s^22p^2$. One can see that this configuration is reasonably well separated from other (excited state) configurations.

The theory we have presented so far tells us the multiplets in the ground state configuration, but not their energies or even the ordering of the energies. These of course can be obtained by explicitly evaluating the matrix elements {eq}`eq-atomstruc-20`. It turns out that when there is only one multiplet, for example, in the case of complete subshells, then the energy estimate coming from first order perturbation theory agrees with the Hartree-Fock estimate (see Prob. {ref}`prob-variational-3`), while if there is more than one multiplet, then the one with minimum energy is less than the Hartree-Fock estimate but still an upper bound to the true ground state of the Hamiltonian {eq}`eq-atomstruc-1`. In {ref}`fig-atomstruc-1` we see that the ground state multiplet for carbon is ${}^3P$.

:::{figure} images/atomstruc-fig01.png
:label: fig-atomstruc-1
:width: 80%

Atomic energy levels of carbon. Energies are measured in eV from the ground state, and all levels less than $10eV$ are shown. Levels of even parity ($\pi=+1$) are on the left, those of odd parity ($\pi=-1$) on the right. The superscripts $a$, $b$, etc, refer to the electron configuration, with $a=2s^22p^2$, $b=2s^22p3p$, $c=2s^22p3d$, $d=2s^22p4p$, $e=2s2p^3$, $f=2s^22p3s$, $g=2s^22p4s$. All configurations are understood to be attached to a helium core, $1s^2$. Source: NIST database.
:::

A set of semi-empirical rules, called *Hund's rules*, tell which multiplet in the ground state configuration has the least energy (this is the ground state multiplet). Hund's rule number~1 says that the ground state multiplet has the highest value of $S$ among all the multiplets in the ground state configuration. For example, in the case of carbon, the multiplet ${}^3P$ has the highest $S$, and we see that it is the ground state. Higher $S$ leads to lower energy because it implies that the individual spins are aligned, which in turn means that the spin part of wave function is symmetric, which implies that the spatial part of the wave function is antisymmetric. This keeps the electrons further apart, lowering their Coulomb energy. This is the same reason that the triplet states are lower in energy than the singlet states in helium, as explained in {ref}`sec-helium-11`. In case there is more than one multiplet with the highest value of $S$, Hund's rule number~2 says that of these, the one with the highest $L$ has the lowest energy.

When we apply the fine-structure perturbation $H_2$ (see {eq}`eq-atomstruc-9` on top of $H_0+H_1$, we see that in general we will have degenerate perturbation theory, in which we must contemplate diagonalizing the matrix

:::{math}
:label: eq-atomstruc-21
\matrixelement{LSM'_LM'_S}{H_2}{LSM_LM_S}.
:::

Here it is understood that we are working in the ground state configuration, and that $L$ and $S$ specify a unique multiplet (so that the index $\gamma$ is not needed). The indices $L$ and $S$ are the same on both sides of the matrix element, because they specify the multiplet, that is, the eigenspace of the Hamiltonian $H_0+H_1$, while the $M_L$ and $M_S$ indices are allowed to be different because they specify the basis inside that unperturbed eigenspace. The matrix is not diagonal in $M_L$ or $M_S$ because $\Lvec$ and $\Svec$, which generate respectively rotations of all orbital and all spin degrees of freedom, do not commute with $H_2$.

This is potentially a large matrix, for example, it is $9\times9$ in the case of the ground state multiplet ${}^3P$ of carbon. But the strategy for diagonalizing it is (by this time) obvious: we must switch from the uncoupled basis $\ket{LSM_LM_S}$ to the coupled basis $\ket{LSJM_J}$, in which $\Jvec=\Lvec+\Svec$. The total angular momentum $\Jvec$ generates rotations of all degrees of freedom of the system, so it commutes with $H_2$. Therefore we define

:::{math}
:label: eq-atomstruc-22
\ket{LSJM_J} = \sum_{M_LM_S} \ket{LSM_LM_S} \braket{LSM_LM_S}{JM_J},
:::

where the last matrix element is a Clebsch-Gordan coefficient, and now the energy shifts are just the diagonal matrix elements with respect to the coupled basis,

:::{math}
:label: eq-atomstruc-23
\Delta E_{LSJ}= \matrixelement{LSJM_J}{H_2}{LSJM_J},
:::

and they are independent of $M_J$ as indicated. The new energy levels are $(2J+1)$-fold degenerate.

For example, in the case of the ground state multiplet ${}^3P$ of carbon, in which $L=1$ and $S=1$, we have $J=0$, $1$ or $2$. We see that the 9-dimensional multiplet breaks up into three subspaces when fine structure is turned on, of dimensionality 1, 3 and 5. These are the energy levels of $H_0+H_1+H_2$, called *terms*. Terms are denoted ${}^{2S+1}L_J$ in spectroscopic notation. For example, in the case of the ground state multiplet of carbon, the terms are ${}^3P_0$, ${}^3P_1$ and ${}^3P_2$.

The theory presented does not allow us to say which term in the ground state multiplet has the lowest energy, but Hund's rule number ~3 comes to the rescue. This rule says that in configurations in which the incomplete subshell is less than half filled, the term with the lowest energy is the one with the lowest $J$. These are called *regular* multiplets. But if the incomplete subshell is more than half filled, then the term with the least energy is the one with the highest $J$. These are called *inverted* multiplets. For example, in the case of carbon, for which the $2p$ subshell is less than half filled, the ground state term is ${}^3P_0$. But in oxygen, which as the same multiplets as carbon (because holes behave the same as electrons, insofar as determining multiplets is concerned), the ground state term is ${}^3P_2$. These ground state terms give the exact quantum numbers of the true ground state of $H_0+H_1+H_2$.

In the case of multiplets in which the incomplete subshell is exactly half filled, such as nitrogen, first order perturbation theory for the terms gives a vanishing result, and one must go on to second order theory. We omit the details.

\problems

(prob-atomstruc-1)=

**Problem \prbdatomstruc-1.} Work out the multiplets ${}^{2S+1}L$ which result from 3 equivalent $d$ electrons.  (“Equivalent” means that they all belong to the same subshell.)  Check to make sure your answer adds up to the correct number of levels, based on the degeneracy expected in the central field approximation.  You will see the necessity of the index $\gamma$ in $\ket{\gamma LSM_LM_S}$, since some multiplets appear more than once.  In the case of vanadium, use Hund's rules to determine the ground state multiplet.  When spin-orbit coupling is turned on, the multiplets split, and the resulting levels are denoted ${}^{2S+1.** 

(prob-atomstruc-2)=

**Problem \prbdatomstruc-2.} Write out the ${}^2P$ wave functions explicitly for an $(np)^3$ configuration (e.g., nitrogen), that is, as linear combinations of Slater determinants that you may identify by their $m$-sets (the set of magnetic quantum numbers for electrons in incomplete subshells).  To help the grader, use the same ordering of magnetic quantum numbers as shown in {ref}`tbl-atomstruc-4`, for example, denote Slater determinant number~5 in that table by $\ket{100;\frac{1}{2},\frac{1}{2},-\frac{1}{2}.** 

{ref}`tbl-atomstruc-4` effectively gives a standard ordering for the orbitals in the Slater determinant, one in which $m_{\ell1}\ge m_{\ell2} \ge m_{\ell3}$ and in which the $m_s$ values corresponding to a run of equal $m_\ell$ values are in descending order. Since there can be a maximum of two $m_\ell$ values in a row that are equal, that means $(\frac{1}{2},-\frac{1}{2})$ for the corresponding $m_s$ values in that case. This rule is followed in the table.

(prob-atomstruc-3)=

**Problem \prbdatomstruc-3..** 

The energy eigenvalues $E_0$ of $H_0$ are determined by the electron configuration. We will be interested in lead (Pb, $Z=82$), with two $6p$ electrons outside closed subshells, and bismuth (Bi, $Z=83$), with three $6p$ electrons outside closed subshells. For such heavy atoms, $H_2$ is larger than $H_1$, so we first solve the Hamiltonian $H_0$, then successively add the terms $H_2$ and $H_1$, and see what happens to the energy levels and eigenstates.

We can assume that $H_0$ is solved for the ground state configuration, and that it gives a known energy $E_0$. This would involve Hartree-Fock theory, and would give us the central potential $\bar V_i$. Next we add $H_2$ and write

:::{math}
:label: eq-atomstruc-24
H_0+H_2 = \sum_{i=1}^Z h(\rvec_i,\pvec_i,\Svec_i),
:::

where

:::{math}
:label: eq-atomstruc-25
h(\rvec,\pvec,\Svec) = {p^2\over 2} - {Z\over r} + {\bar V}_d(r)-{\bar V}_{ex,i}+ \xi(r) \Lvec\cdot\Svec.
:::

We write the single particle eigenstates and eigenvalues as

:::{math}
:label: eq-atomstruc-26
h\ket{\lambda} = \epsilon_\lambda \ket{\lambda},
:::

where $\lambda$ stands for the single particle quantum numbers $(n\ell j m_j)$, and where $\epsilon_\lambda$ is independent of $m_j$, $\epsilon_\lambda = \epsilon_{nlj}$. The states $\ket{\lambda}$ form an orthonormal basis in the Hilbert space for a single electron. The eigenstates of $H_0+H_2$ are Slater determinants formed out of $Z$ orbitals $\ket{\lambda}$, and the corresponding energies are

:::{math}
:label: eq-atomstruc-27
E_{0+2} = \sum_\lambda \epsilon_\lambda.
:::

The terms $\epsilon_\lambda = \epsilon_{n\ell j}$ in the last, incomplete subshell, the $6p$ with $\ell=1$, have two possible $j$ values, $1/2$ and $3/2$. So the contribution from the last subshell depends on the number of electrons with $j=1/2$ and the number with $j=3/2$.

For example, in Pb with the $6s^2$ configuration, the two electrons can give three possible pairs of $j$ values, $(j_1,j_2)= (\frac{3}{2},\frac{3}{2})$, $(\frac{3}{2},\frac{1}{2})$, or $(\frac{1}{2},\frac{1}{2})$. Therefore the single level $E_0$ of $H_0$ breaks up into three levels $E_{0+2}$, labeled by $(j_1,j_2)$, when we turn on $H_2$. As we know from spin-orbit theory ({ref}`ch-finestruc`), the energy $\epsilon_{n\ell j}$ is an increasing function of $j$, so the $(j_1,j_2)$ are sequenced as indicated in {ref}`fig-atomstruc-2`.

:::{figure} images/atomstruc-fig02.png
:label: fig-atomstruc-2
:width: 80%

Term diagram in $jj$-coupling for lead (Pb). Drawing is not to scale.
:::

Finally, when we turn on $H_1$, the individual $\Jvec_i$ operators no longer commute with the Hamiltonian, but $\Jvec = \sum_i \Jvec_i$ does. Therefore we must now organize the energy eigenstates according to the $(J,M_J)$ quantum numbers. In Pb, for example, the $(\frac{3}{2},\frac{3}{2})$ state splits into $J=0$ and $J=2$ states. The state $J=1$, which occurs in $\frac{3}{2}\otimes\frac{3}{2}$, is not allowed by the Pauli principle. Likewise, the $(\frac{3}{2},\frac{1}{2})$ level splits into $J=1$ and $J=2$ levels, because $\frac{3}{2}\otimes\frac{1}{2}=1\oplus2$. Here the Pauli principle causes no extra restriction, because $j_1\ne j_2$. Finally, the $(\frac{1}{2},\frac{1}{2})$ gives only a $J=0$ level. All these levels and their degeneracies (in parentheses) are indicated in the figure.

\problempart{(a)} For the case of bismuth ($6p^3$ configuration), indicate the allowed $(j_1,j_2,j_3)$ terms and their degeneracies when $H_2$ is added to $H_0$. Make sure the degeneracies add up to the degeneracy of the $6p^3$ configuration. Indicate also the allowed $J$ values contained in each $(j_1,j_2,j_3)$ term.

(prob-atomstruc-4)=

**Problem (b)} The $(\frac{3}{2},\frac{3}{2},\frac{1}{2})$ term contains a $J=3/2$ component.  Find the normalized states $\ket{JM_J}$ in this component for $M_J=\frac{3}{2}$ and $M_J=\frac{1}{2}$.  Write your answers as linear combinations of Slater determinants composed of orbitals $\ket{\lambda}$; the Slater determinant will be identified by the $(j,m_j)$ quantum numbers of the last three orbitals, since the orbitals for the 80 core electrons are fixed.  To help the grader(s), identify these Slater determinants as $\ket{j_1j_2j_3;m_{j1}m_{j2}m_{j3}.**
