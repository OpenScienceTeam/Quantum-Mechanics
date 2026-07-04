---
title: "26. The Zeeman Effect in Hydrogen and Alkali Atoms"
---
(ch-zeeman)=

# 26. The Zeeman Effect in Hydrogen and Alkali Atoms

(sec-zeeman-1)=

## Introduction

The Zeeman effect concerns the interaction of atomic systems with external magnetic fields. A basic understanding of the Zeeman effect is needed for many aspects of modern research in atomic physics. In addition, the Zeeman effect played an important historical role in the development of quantum mechanics, leading to the discovery of spin, the $g$-factor of the electron, and the Thomas precession. In these notes we treat the Zeeman effect in one-electron atoms.

(sec-zeeman-2)=

## Units and Orders of Magnitude

We will use atomic units, so that $m=\hbar=e=1$. This means that $c=1/\alpha \approx 137$, where $\alpha$ is the fine structure constant. It also means that the Bohr magneton becomes

:::{math}
:label: eq-zeeman-1
\mu_B = {e \hbar \over 2mc} = {1 \over 2c} = {\alpha\over 2},
:::

while the magnetic moment of the electron becomes

:::{math}
:label: eq-zeeman-2
\muvec = -g {e \over 2mc} \Svec = -{1\over c} \Svec =-\alpha \Svec,
:::

where we approximate $g\approx2$ for the electron $g$ factor. Thus, the energy of interaction of the electron spin in a magnetic field is

:::{math}
:label: eq-zeeman-3
-\muvec\cdot\Bvec = \alpha \Bvec \cdot \Svec.
:::

We must also deal with magnetic fields in atomic units. A magnetic field of strength $B=1$ in atomic units is equivalent to $B=B_0$ in ordinary Gaussian units, where $B_0$ is the unique magnetic field strength that can be constructed out of $e$, $\hbar$ and $m$. That field is

:::{math}
:label: eq-zeeman-4
B_0 = {e \over a_0^2} = {m^2 e^5 \over \hbar^4} = 1.72 \times 10^7 \;Gauss,
:::

where $a_0$ is the Bohr radius (the unit of distance in atomic units). $B_0$ is the strength of a magnetic field that is equal to the electrostatic field of the proton at the Bohr radius in the hydrogen atom (thus, it is also the atomic unit of electric field). Electric and magnetic fields have the same dimensions in Gaussian units, although one is usually called statvolts/cm and the other Gauss; see Appendix~\emunits. If an external field of strength $B_0$ is applied to a hydrogen atom in the ground state, the electron will feel a magnetic force that is of the order of $\alpha$ times the electric force, since the velocity of the electron is $v/c = \alpha$. If you want to apply a magnetic field so strong that the magnetic force is equal to the Coulomb electric force from the nucleus, the field must have the strength $B_0/\alpha = 2.35 \times 10^9 \;Gauss$. Such fields are so strong that atoms in the ordinary sense do not exist; the dynamics is dominated by magnetic forces at all distances larger than a Bohr radius. At higher magnetic field strengths, new physics appears. For example, at the strength $B=B_0/\alpha^3 = 4.41 \times 10^{13} \;Gauss$, the energy of the lowest Landau level is becoming relativistic.

For reference, the strongest steady magnetic fields that can be created in a laboratory are of the order of 10~T or $10^5$~Gauss. By using explosives or other means to compress magnetic flux, fields of the order of $10^3$~T or $10^7$~Gauss can be created for a short period of time. In astrophysics, much stronger magnetic fields arise. It is believed that at the surface of a neutron star there exist magnetic fields of up to $10^{12}$ Gauss, and there is speculation about fields of up to $10^{15}$ Gauss in “magnetars”. Because of these astrophysical applications, there has been some interest in recent years in the exotic physics that arises at high field strengths. In these notes we will assume that the external fields are steady state fields created in the laboratory, and hence have a maximum value of about $10^5$~Gauss or $10^{-2}$ atomic units.

(sec-zeeman-3)=

## The Hamiltonian and Neglected Terms

In atomic units, the Hamiltonian for the electron in a single-electron atom (hydrogen-like or alkali) is

:::{math}
:label: eq-zeeman-5
H={1\over 2}\Bigl( \pvec +\alpha \Avec\Bigr)^2 +V(r) + H_FS + \alpha\Bvec \cdot \Svec,
:::

where the charge of the electron is $q=-1$, where $V(r)$ is the central force potential (either Coulomb for hydrogen or screened Coulomb for alkalis), and where $H_{FS}$ is the sum of the fine-structure corrections presented in {eq}`eq-finestruc-25a`. We assume a uniform magnetic field,

:::{math}
:label: eq-zeeman-6
\Bvec = B {\hat{\mathbf{z}}},
:::

and we take the gauge

:::{math}
:label: eq-zeeman-7
\Avec = {1 \over 2} \Bvec \cross \rvec,
:::

which is Coulomb gauge so that $\del \cdot \Avec=0$. This implies

:::{math}
:label: eq-zeeman-8
\pvec \cdot \Avec = \Avec \cdot \pvec,
:::

so the cross terms in the expansion of the kinetic energy can be written in either order.

We expand the kinetic energy $T$ in the Hamiltonian {eq}`eq-zeeman-5` into three terms,

:::{math}
:label: eq-zeeman-9
T= {1\over 2}\Bigl( \pvec +\alpha \Avec\Bigr)^2 ={p^2\over 2} + \alpha \pvec \cdot \Avec + {\alpha^2 \over 2} A^2= T_0 + T_1 + T_2.
:::

The cross term can also be written,

:::{math}
:label: eq-zeeman-10
T_1 = {\alpha \over 2} \pvec \cdot (\Bvec \cross \rvec) = {\alpha \over 2} \Bvec \cdot \Lvec,
:::

where $\Lvec = \rvec \cross \pvec$. The third term can also be written,

:::{math}
:label: eq-zeeman-11
T_2 = {\alpha^2\over 8}B^2(x^2 + y^2).
:::

It looks like a potential (it is a function only of the particle coordinates).

We estimate the relative order of magnitude of the three terms in the kinetic energy by first looking at the ratio,

:::{math}
:label: eq-zeeman-12
{T_1 \over T_0} \sim { \alpha BL \over p^2} \sim \alpha B,
:::

where we use for a reference a state of hydrogen with quantum numbers that are of order unity, so that $p$ (the momentum of the electron in atomic units) and $L$ (its angular momentum) are both of order unity. Since we have decided that $B$ (in atomic units) is no more than $10^{-2}$, this ratio is about $10^{-4}$ maximum, and $T_1 \ll T_0$. Similarly, we find that the ratio $T_2/T_1$ is of the same order of magnitude, so $T_2$ is much smaller in turn than $T_1$.

The term $T_1$ is of the same order of magnitude as the energy of interaction of the spin with the magnetic field (the last term in {eq}`eq-zeeman-5`, and taken together these terms form what we shall call the Zeeman Hamiltonian,

:::{math}
:label: eq-zeeman-13
H_Z = {\alpha\over 2} \Bvec \cdot (\Lvec + 2\Svec) ={\alpha \over 2}B (L_z + 2 S_z).
:::

The 2 multiplying the spin is really the $g$-factor of the electron, indicating that different kinds of angular momentum produce magnetic moments in different proportions.

The Zeeman Hamiltonian $H_Z$ is of the same order of magnitude as $T_1$, which by our assumptions is at most about $10^{-4}$ in atomic units. This coincidentally is the same order of magnitude as the fine structure terms $H_FS$, at least in hydrogen, where they are of order $\alpha^2$. Of course by decreasing the strength of the magnetic field we can make $H_Z \ll H_FS$. Similarly, by going to excited states, where fine structure effects are smaller than in the ground state, we can make $H_Z \gg H_FS$. In the following we will analyze both limits in the comparison between $H_Z$ and $H_FS$. As for the term $T_2$, it is much smaller than any of the other terms, and we drop it. The result is the Hamiltonian that we will use for our analysis of the Zeeman effect,

:::{math}
:label: eq-zeeman-14
H={p^2 \over 2} + V(r) + H_FS + H_Z,
:::

where $H_Z$ is given by {eq}`eq-zeeman-13`.

(sec-zeeman-4)=

## Case I.  $H_Z$ Dominant, $H_FS$ Negligible

The first case we shall consider is one in which $H_Z$ is so much larger than $H_FS$ that $H_FS$ can be neglected altogether. This might require unrealistically large magnetic fields by laboratory standards (it depends on the quantum numbers), but it provides a useful reference for later work.

To analyze this case we take the unperturbed Hamiltonian and the perturbation to be

:::{math}
:label: eq-zeeman-15
\begin{aligned}
H_0 &= {p^2 \over 2} + V(r),
\end{aligned}
:::

:::{math}
:label: eq-zeeman-16
\begin{aligned}
H_1 &= H_Z.
\end{aligned}
:::

The unperturbed Hamiltonian is the nonrelativistic, electrostatic model of the atom, but we include the spin degrees of freedom in the wave functions. Thus, for hydrogen the energies are $E_n = -1/2n^2$ with degeneracies $2n^2$, and for the alkalis the energies are $E_{n\ell}$ with degeneracies $2(2\ell +1)$.

Thus we must think about degenerate perturbation theory. As usual, a good choice of basis of unperturbed eigenstates inside the degenerate, unperturbed eigenspaces may simplify the calculation (see \finestruc.5). The obvious choices of unperturbed eigenbases are the uncoupled basis, $\{ \ket{n \ell m_\ell m_s} \}$, and the coupled basis, $\{ \ket{n \ell j m_j} \}$. To see which is better, we make a table indicating which operators $H_1=H_Z$ commutes with. We only list the $z$-component of various angular momentum operators in the table, because the perturbation breaks the full rotational symmetry of the unperturbed system, and can only be invariant with respect to rotations about the $z$-axis.

:::{list-table} The table indicates whether $H_Z$ commutes with the given angular momentum operator (${Y}={yes}$, ${N} = {no}$).
:label: tbl-zeeman-1
:header-rows: 2

* - $L^2$
  - $S_z$
  - $S^2$
  - $J_z$
  - $J^2$
  - 
* - Y
  - Y
  - Y
  - Y
  - N
  - 

:::
We find that all the operators in the list commute with $H_Z$, except $J^2 = L^2 + 2\Lvec \cdot \Svec + S^2$, which fails because $\Lvec \cdot \Svec$ contains the $x$- and $y$-components of $\Lvec$ and $\Svec$, which do not commute with $L_z$ or $S_z$. The table makes it clear that the uncoupled basis is better for the perturbation calculation, since the operators $(L^2, L_z, S_z)$ of the complete set that define the uncoupled basis all commute with $H_Z$. Thus, in this basis, the matrix of $H_Z$ (either the $2n^2 \times 2n^2$ matrix for hydrogen or the $2(2\ell +1) \times 2(2\ell+1)$ matrix for the alkalis) in the unperturbed eigenspace is completely diagonal. As in the fine structure calculation of {ref}`ch-finestruc`, we escape having to diagonalize any matrices when doing degenerate perturbation theory.

:::{figure} images/zeeman-fig01.png
:label: fig-zeeman-1
:width: 80%

a. Strong field Zeeman splitting in $2s$ level of hydrogen. The number in parentheses is the degeneracy of the unperturbed state. The energy shifts $\Delta E$ are measured in units of $\mu_B B$. The quantum numbers in the kets are $\ket{m_\ell m_s}$, the other quantum numbers $n=2$ and $\ell=0$ being understood.
:::

:::{figure} images/zeeman-fig02.png
:label: fig-zeeman-2
:width: 80%

b. Same as {ref}`fig-zeeman-1`a, except for the $2p$ level of hydrogen, which is 6-fold degenerate. The perturbed level $\Delta E=0$ is 2-fold degenerate. Quantum numbers $n=2$ and $\ell=1$ are understood.
:::


Therefore the energy shifts are given by

:::{math}
:label: eq-zeeman-17
\Delta E = {\alpha\over 2}B \matrixelement{n\ell m_\ell m_s}{(L_z + 2S_z)} {n\ell m_\ell m_s} = {\alpha\over 2}B(m_\ell + 2m_s) = (\mu_B B)(m_\ell + 2m_s).
:::

In the final expression we have used {eq}`eq-zeeman-1`, which makes the answer valid in both atomic and ordinary units, since $\mu_B B$ has dimensions of energy. The results are displayed in {ref}`fig-zeeman-1`a for the $2s$ set of states and in {ref}`fig-zeeman-1`b for the $2p$ set of states of hydrogen. We see that the 2-fold degeneracy of the $2s$ states is completely lifted by the perturbation, while the 6-fold degeneracy of the $2p$ set of states is only partially lifted, with five equally spaced energy levels in the presence of the magnetic field, one of which is 2-fold degenerate.

Actually, Figs.~{ref}`fig-zeeman-1` are valid for any $s$ or $p$ set of states, either in hydrogen or in an alkali. In hydrogen, however, notice that there is a further degeneracy, because the states $\Delta E/\mu_B B = \pm 1$ in the $2s$ set of states are degenerate with the $\Delta E/ \mu_B B =\pm 1$ states of the $2p$ set. Altogether, of the 8 degenerate states of the the $n=2$ level of hydrogen in the unperturbed system, there are two nondegenerate levels ($\Delta E/ \mu_B B = \pm 2$) after the perturbation is turned on, and three 2-fold degenerate levels ($\Delta E/\mu_B B = 0,\pm 1$).

(sec-zeeman-5)=

## Case II.  $H_Z \gg H_SO$, $H_SO$ not Negligible

Now we consider the case that $H_Z$ is much larger than the fine structure terms $H_FS$, as in \secrzeeman-4, but not so large that those corrections can be neglected. Thus we will take the new unperturbed Hamiltonian to be

:::{math}
:label: eq-zeeman-18
H_0= {p^2 \over 2m} + V(r) +H_Z,
:::

with $H_FS$ as a perturbation. Notice that this $H_0$ is the entire Hamiltonian of \secrzeeman-4.

More precisely, we will take $H_1$ to be the spin-orbit term only, and ignore the relativistic kinetic energy and Darwin corrections. This is not realistic, because all three fine structure terms are of the same order of magnitude, but we do it for simplicity. As for the spin-orbit term, we write

:::{math}
:label: eq-zeeman-19
f(r) = {\alpha^2\over 2} {1\over r} \dod{V}{r},
:::

so that

:::{math}
:label: eq-zeeman-20
H_1=H_SO= f(r) \Lvec\cdot\Svec.
:::

In the following we concentrate mainly on hydrogen, with a few comments about the alkalis. Some of the eigenstates of $H_0$ are degenerate, as we have seen in \secrzeeman-4, so we must think about degenerate perturbation theory. We can only use the uncoupled basis, since the coupled basis is not an eigenbasis of $H_0$. Thus we must look at the matrix elements

:::{math}
:label: eq-zeeman-21
\matrixelement{n\ell m_\ell m_s}{H_SO} {n\ell'm'_\ell m'_s},
:::

where we put primes to cover the degenerate eigenspaces of $H_0$. For example, in the $n=2$ levels of hydrogen, we found in \secrzeeman-4 that there were three 2-fold degenerate levels of $H_0$ (see Figs.~{ref}`fig-zeeman-1`a and {ref}`fig-zeeman-1`b). However, we see right away that $[H_SO,L^2]=0$, so the prime on $\ell$ is not necessary, and in fact we can carry out the perturbation analysis in subspaces of given $\ell$ separately. This is what we must do anyway in the case of the alkalis, where there is no degeneracy in $\ell$ in the unperturbed system. In the case of the $n=2$ levels of hydrogen, we see that we have only one 2-fold degeneracy, that between the $\ket{n\ell m_\ell m_s} = \ket{2,1,-1,\frac{1}{2}}$ and $\ket{2,1,1,-\frac{1}{2}}$ states. This makes one $2\times 2$ matrix. Let us look at the off-diagonal element,

:::{math}
:label: eq-zeeman-22
\matrixelement{2,1,-1,\frac{1}{2}}{f(r)\Lvec\cdot\Svec} {2,1,1,-\frac{1}{2}},
:::

in which we use the identity,

:::{math}
:label: eq-zeeman-23
\Lvec\cdot\Svec = {1\over 2}(L_+ S_- + L_-S_+) + L_zS_z.
:::

To be nonvanishing, the operator in the middle of the matrix element {eq}`eq-zeeman-22` must connect states with $\Delta m_\ell = 2$, but in fact that operator permits only $\Delta m_\ell =0$ or $\pm1$. Therefore the off-diagonal matrix element {eq}`eq-zeeman-22` vanishes, and, for the $n=2$ levels of hydrogen, we can use nondegenerate perturbation theory. Once again, there are no matrices to diagonalize.

Therefore to get the energy shifts we need only look at the diagonal matrix elements,

:::{math}
:label: eq-zeeman-24
\Delta E = \matrixelement{n\ell m_\ell m_s} {f(r)\Lvec\cdot\Svec}{n\ell m_\ell m_s} = m_\ell m_s \matrixelement{n\ell m_\ell m_s} {f(r)}{n \ell m_\ell m_s},
:::

where we have used {eq}`eq-zeeman-23`. The spin kets cancel each other in the final matrix element, which turns into a purely orbital matrix element of the type we saw previously in the treatment of the fine structure. See \finestruc.9. We have

:::{math}
:label: eq-zeeman-25
\matrixelement{n\ell m_\ell m_s} {f(r)}{n \ell m_\ell m_s} = \matrixelement{n \ell m_\ell}{f(r)}{n\ell m_\ell} ={\alpha^2 \over 2} \matrixelement{n\ell 0}{{1\over r^3}}{n\ell 0},
:::

where in the last step we have specialized to hydrogen. We use the expectation value {eq}`eq-finestruc-47`, which is only valid for $\ell \ne 0$, to find

:::{math}
:label: eq-zeeman-26
\Delta E = {\alpha^2 \over 2n^3} {m_\ell m_s \over \ell(\ell+\frac{1}{2})(\ell+1)} = {\alpha^2\over 48} m_\ell m_s,
:::

in the $2p$ levels of hydrogen. As for the $2s$ levels, for them $\Lvec=0$ (that is, the operator $\Lvec$ vanishes on the $2s$-subspace), so $\Delta E=0$.

(sec-zeeman-6)=

## Case III:  $H_Z \ll H_FS$

The final case we shall examine is the weak field limit, in which $H_Z \ll H_FS$. Thus we take the unperturbed Hamiltonian and perturbation to be

:::{math}
:label: eq-zeeman-27
\begin{aligned}
H_0 &= {p^2 \over 2m} + V(r) + H_FS,
\end{aligned}
:::

:::{math}
:label: eq-zeeman-28
\begin{aligned}
H_1 &= H_Z = \mu_B B(L_z + 2S_z).
\end{aligned}
:::

In the case of hydrogen, one should also consider the Lamb shift for a realistic treatment. For example, in the $n=2$ levels of hydrogen, the Lamb shift is about 10 times smaller than the fine structure energy shifts, indicating that we really should question how the Lamb shift compares to the Zeeman term which is also (by our assumptions) much smaller than the fine structure term. For simplicity, however, we will ignore the Lamb shift in the following and work with {eq}`eq-zeeman-27` and {eq}`eq-zeeman-28`.

The unperturbed energies are $E_{nj}$ for hydrogen or $E_{n\ell j}$ for the alkalis, and the unperturbed eigenstates are members of the coupled basis $\ket{n\ell j m_j}$. There is no option of using the uncoupled basis, which is not an eigenbasis of $H_0$. The degeneracies are $2j+1$ in the case of the alkalis, and more than this in hydrogen because of the degeneracy between different $\ell$ values. For example, the eight $n=2$ states of hydrogen consist of two levels, each 4-fold degenerate (see Fig.~\figr\finestruc.2). Thus we must think about degenerate perturbation theory.

In hydrogen the matrix elements we need have the form

:::{math}
:label: eq-zeeman-29
\matrixelement{n\ell' j m'_j}{H_Z} {n\ell j m_j},
:::

where on the left we omit the primes on $n$ and $j$ since they define the unperturbed energy level $E_{nj}$, but put primes on the other two indices. In the case of the alkalis we do not need the prime on $\ell$, since the unperturbed energies are $E_{n\ell j}$. Actually, we do not need the prime on $\ell$ in the case of hydrogen, either, since $[L^2, H_Z]=0$. Nor for that matter do we need the prime on $m_j$, since $[J_z, H_Z]=0$, and once again we escape from having to diagonalize any matrices. The energy shifts are

:::{math}
:label: eq-zeeman-30
\Delta E = \matrixelement{n\ell jm_j}{\mu_B B(L_z + 2S_z)} {n\ell j m_j}.
:::

We write $L_z+2S_z = J_z + S_z$, so that this becomes

:::{math}
:label: eq-zeeman-31
\Delta E = \mu_B B\Bigl[m_j + \matrixelement{n\ell jm_j}{S_z}{n\ell jm_j}\Bigr].
:::

The final matrix element of $S_z$ is not entirely trivial to evaluate in a reasonably elegant manner. A technique that has been found to do this involves some results in angular momentum theory. We now make a digression to discuss these results, before returning to apply them to the weak field Zeeman effect.

(sec-zeeman-7)=

## The Projection Theorem

In this we adopt the general notation for a standard angular momentum basis, $\ket{\gamma jm}$, which was used in {ref}`ch-repsamos`. Compared to the notation used in \secrzeeman-6, the correspondences are

:::{math}
:label: eq-zeeman-32
\begin{aligned}
\gamma &\to n\ell, \\
j      &\to j, \\
m      &\to m_j. \\

\end{aligned}
:::

We begin with an identity due to Dirac. We let $\Vvec$ be any vector operator. Then we have the identity,

:::{math}
:label: eq-zeeman-33
[J^2,[J^2,\Vvec]] = \hbar^2[ 2(J^2\Vvec + \Vvec J^2) - 4(\Vvec\cdot\Jvec)\Jvec].
:::

This identity can be proved by working with the definition {eq}`eq-transfop-21`. The proof will be left as an exercise. See Prob.~\prbrzeeman-1.

We sandwich both sides of Dirac's identity {eq}`eq-zeeman-33` between the states $\bra{\gamma' j m'}$ and $\ket{\gamma jm}$, in which the $j$ values are the same on both sides but the other indices are allowed to be different. We let $\Xvec = [J^2,\Vvec]$, so that the left hand side of {eq}`eq-zeeman-33` is $[J^2,\Xvec]$ and its matrix element is

:::{math}
:label: eq-zeeman-34
\matrixelement{\gamma' jm'}{J^2\Xvec - \Xvec J^2} {\gamma jm} = j(j+1)\hbar^2 \matrixelement{\gamma'jm'}{\Xvec-\Xvec}{\gamma jm} =0.
:::

Therefore the matrix element of the right hand side of {eq}`eq-zeeman-33` between the same states vanishes, or,

:::{math}
:label: eq-zeeman-35
2\matrixelement{\gamma'jm'}{J^2\Vvec + \Vvec J^2} {\gamma jm} = 4j(j+1)\hbar^2 \matrixelement{\gamma'jm'}{\Vvec} {\gamma jm} = 4\matrixelement{\gamma'jm'}{(\Vvec\cdot\Jvec)\Jvec} {\gamma jm}.
:::

Rearranging, we have

:::{math}
:label: eq-zeeman-36
\matrixelement{\gamma'jm'}{\Vvec}{\gamma jm} ={1\over j(j+1)\hbar^2} \matrixelement{\gamma'jm'}{(\Vvec\cdot\Jvec)\Jvec} {\gamma jm},
:::

which is the *projection theorem*. It is useful in several applications in atomic physics. It has generalizations in which the $j$ values on the two sides of the matrix element are allowed to be distinct, but this simpler version is all we shall need for the application we shall consider.

:::{figure} images/zeeman-fig03.png
:label: fig-zeeman-3
:width: 80%

Geometrical meaning of the projection theorem.
:::

The geometrical meaning of the projection theorem can be seen in {ref}`fig-zeeman-2`. If we think of $\Jvec$ and $\Vvec$ as classical vectors, then the projection of $\Vvec$ onto the direction $\Jvec$ is given by

:::{math}
:label: eq-zeeman-37
{(\Vvec\cdot\Jvec)\Jvec \over J^2}.
:::

On the other hand, the quantum projection theorem {eq}`eq-zeeman-36` states that the matrix elements of a vector operator $\Vvec$ on a subspace of a given $j$ are the same as the matrix elements of the projection {eq}`eq-zeeman-37`, with the denominator $J^2$ reinterpreted as $j(j+1)\hbar^2$. The projection theorem can also be seen as an example of the Wigner-Eckart theorem, in which the reduced matrix element is explicitly evaluated.

(sec-zeeman-8)=

## The Weak Field Zeeman Effect

We now return to the matrix element of $S_z$ in {eq}`eq-zeeman-31`, which we need for the energy shifts in the weak field Zeeman effect. We use the projection theorem with the identifications {eq}`eq-zeeman-32`, and we also identify $\Vvec$ with $\Svec$. In this application of the projection theorem the states are the same on both sides of the matrix element, so we do not need the primes seen in {eq}`eq-zeeman-36`. Thus we have

:::{math}
:label: eq-zeeman-38
\matrixelement{n\ell jm_j}{S_z}{n\ell jm_j} = {1\over j(j+1)} \matrixelement{n\ell jm_j} {(\Svec\cdot\Jvec)J_z}{n\ell jm_j},
:::

where we have taken the $z$-component and reverted to atomic units. The operator $J_z$ brings out the quantum number $m_j$ when acting on the ket, while the operator $\Svec\cdot\Jvec$ can be put into a more useful form by expanding $L^2=(\Jvec-\Svec)^2$. This gives

:::{math}
:label: eq-zeeman-39
\Svec\cdot\Jvec = {1\over2}[J^2 + S^2 - L^2].
:::

Altogether, the matrix element becomes

:::{math}
:label: eq-zeeman-40
\matrixelement{n\ell jm_j}{S_z}{n\ell jm_j} = m_j{j(j+1)+s(s+1)-\ell(\ell+1) \over 2j(j+1)},
:::

and the energy shift {eq}`eq-zeeman-31` becomes

:::{math}
:label: eq-zeeman-41
\Delta E = g_L (\mu_B B) m_j,
:::

where

:::{math}
:label: eq-zeeman-42
g_L = 1+ {j(j+1)+s(s+1)-\ell(\ell+1) \over 2j(j+1)}.
:::

The dimensionless number $g_L$ is called the *Land\'e $g$-factor*.

It might seem surprising that the energy shifts should be proportional to $m_j$, for while it is true that $J_z=L_z+S_z$, the orbital and spin angular momentum do not contribute equally to the magnetic moment, due to the different $g$-factors ($g=1$ for orbital angular momentum, $g=2$ for electron spin, hence the expression $L_z+2S_z$ in the Zeeman Hamiltonian). That is, the angular momentum operator is $\Jvec=\Lvec+\Svec$, while the magnetic moment operator $\muvec$ is proportional to $\Lvec+2\Svec$. Thus, $\muvec$ is not proportional to $\Jvec$. In {ref}`ch-spinmagf`\ it was pointed out that in classical electrodynamics, the angular momentum and magnetic moment of a system are in general not proportional, and the question was left open why they should be so for a particle such as the nucleus of an atom. We see here that in atomic systems, too, the magnetic moment and angular momentum are not proportional. But the energy shifts {eq}`eq-zeeman-41` are the same as if the magnetic moment of the atom (orbital plus spin) were given by

:::{math}
:label: eq-zeeman-43
\muvec = -g_L \mu_B {\Jvec \over\hbar},
:::

a generalization of Eq. {eq}`eq-spinmagf-12` (with $q=-e$).

The reason for this is that all vector operators are proportional to any given vector operator on a single irreducible subspace under rotations. See Prob. {ref}`prob-wigeck-2`(a). The angular momentum $\Jvec$ is a convenient reference vector operator, so all vector operators, including $\Lvec+2\Svec$, are proportional to $\Jvec$ on a single irreducible subspace. In the limit of weak magnetic field, the Zeeman Hamiltonian does not mix irreducible subspaces, that is, it only involves a single set of states $\ket{n\ell jm_j}$ with the same $n$, $\ell$ and $j$ but with different $m_j$, so the energy shifts are proportional to $m_j$. For stronger fields, for example, one strong enough to overwhelm the fine structure splitting as in \secrzeeman-5, the dependence of the energy levels on the magnetic quantum numbers is more complicated. The same would happen in a nucleus if the magnetic field were strong enough to mix more than one eigenspace of the nuclear Hamiltonian, although that would require extraordinarily large magnetic fields by ordinary standards.

\problems

(prob-zeeman-1)=

**Problem \prbdzeeman-1..** 

Show that if $\Avec$ is a vector operator, then

:::{math}
:label: eq-zeeman-44
[J^2,[J^2,\Avec]] = 2\hbar^2 (\Avec J^2 + J^2 \Avec) -4\hbar^2 (\Avec\cdot\Jvec) \Jvec.
:::

Then use this to show that

:::{math}
:label: eq-zeeman-45
j(j+1)\hbar^2 \matrixelement{\gamma'j m'}{\Avec}{\gamma jm} = \matrixelement{\gamma'jm'}{(\Avec\cdot\Jvec)\Jvec} {\gamma jm},
:::

where the notation of {ref}`ch-repsamos`\ is used.

(prob-zeeman-2)=

**Problem \prbdzeeman-2..** 

In these notes we have studied various limiting cases. In \secrzeeman-8 we studied the case that $B$ is so weak that the spin-orbit term dominates the Zeeman term. There we found (see {eq}`eq-zeeman-41` that the energy shifts were

:::{math}
:label: eq-zeeman-46
\Delta E= g\mu_B Bm_j,
:::

where $g$ is the Land\'e $g$-factor,

:::{math}
:label: eq-zeeman-47
g=1+{j(j+1) + s(s+1) - \ell(\ell+1) \over 2j(j+1)}.
:::

Next, when $B$ is so strong that the spin-orbit term can be neglected (\secrzeeman-4), we found {eq}`eq-zeeman-17` for the energy shifts. Some books (e.g., Sakurai) do similar calculations, but they ignore the Darwin and relativistic kinetic energy corrections, which is not realistic because they are of the same order of magnitude as the spin-orbit term.

Consider therefore the Hamiltonian,

:::{math}
:label: eq-zeeman-48
H=H_0 + H_1,
:::

where

:::{math}
:label: eq-zeeman-49
H_1 = H_{RKE} + H_{SO} + H_D + H_Z.
:::

See {eq}`eq-finestruc-25a`, {eq}`eq-finestruc-26a` and {eq}`eq-zeeman-13` for the definitions of these various terms. Take the magnetic field to point along the $z$-axis, $\Bvec=B{\hat{\mathbf{z}}}$. The term $H_Z$ is proportional to the applied field $B$, which is a parameter of the perturbing Hamiltonian. You are to evaluate the corrections to the energy levels due to this perturbation, as a function of $B$, using first-order perturbation theory. To simplify the notation, I suggest that you use atomic units throughout. Also, I recommend that you introduce the dimensionless variable $x$ to represent the strength of the magnetic field,

:::{math}
:label: eq-zeeman-50
x={B\over B_1},
:::

where

:::{math}
:label: eq-zeeman-51
B_1={e^7 m^2\over \hbar^5 c} = \alpha B_0,
:::

where $B_0$ is defined by {eq}`eq-zeeman-4`. This definition is useful for the present problem, because it makes $x=1$ approximately the value for which the Zeeman term is comparable to the fine structure term.

:::{figure} images/zeeman-fig04.png
:label: fig-zeeman-4
:width: 80%

Graph of solutions to Prob. \prbrzeeman-2. The Zeeman energy shift $\Delta E$ is measured relative to the $n=2$ level of hydrogen in the electrostatic model, which is $-1/2\cdot2^2$ in atomic units. The fine structure energy shifts at zero field strength are $-(5/128)\alpha^2$ for the $2s_{1/2}$ and $2p_{1/2}$ levels, where $\alpha$ is the fine structure constant, and $-(1/128)\alpha^2$ for the $2p_{3/2}$ levels. The model ignores the Lamb shift, which is why the $2s_{1/2}$ and $2p_{1/2}$ levels are degenerate in the figure at zero field strength. Including the Lamb shift would modify the picture slightly.
:::

\problempart{(a)} Out of the list of operators, $L^2$, $L_x$, $L_y$, $L_z$, $S^2$, $S_x$, $S_y$, $S_z$, $J^2$, $J_x$, $J_y$, $J_z$, $\pi$, indicate which commute with $H_0$ and which commute with the entire Hamiltonian $H$. Use this information to choose a convenient basis in the 8-dimensional subspace of the $n=2$ degenerate energy levels of $H_0$, for which the perturbing Hamiltonian will be as diagonal as possible.

\problempart{(b)} Let $\Delta E$ be the difference between the true energy levels of $H$ (including the perturbation) and the 8-fold degenerate level $E_2=-1/8=-1/(2\cdot2^2)$ of $H_0$. Find all eight levels as a function of $x$ in atomic units.

\problempart{(c)} Expand these results out for small $x$, and show that they agree with {eq}`eq-zeeman-46`. Also expand the results for large $x$, and show that the results agree with {eq}`eq-zeeman-17`.

See {ref}`fig-zeeman-3`, a plot of the answers. The figure reveals a typical behavior of energy levels in various versions of the Zeeman effect. Notice that energy levels cross as the parameter (in this case, the magnetic field strength) is varied. Notice also that the fine structure splitting is overwhelmed by the Zeeman energy shifts at relatively small values of the parameter $x$. We might have expected this to occur around $x\approx 1$, based on the scalings we have introduced, but the quantum numbers introduce additional dimensionless factors that reduce the value to something closer to $x\approx 0.03$, which corresponds to a magnetic field of about $4 \,KG = 0.4 \,T$.

(prob-zeeman-3)=

**Problem \prbdzeeman-3..** 

\problempart{(a)} Since $\Avec$ is a vector operator, the Wigner-Eckart theorem says

:::{math}
:label: eq-zeeman-52
\matrixelement{\gamma'j'm'}{A_q}{\gamma jm} = \reducedme{\gamma'j'}{A}{\gamma j} \braket{j'm'}{j1mq},
:::

where $A_q={\hat{\mathbf{e}}}_q\cdot\Avec$. See {ref}`sec-wigeck-2` for the spherical basis ${\hat{\mathbf{e}}}_q$. Now let $f$ be a scalar operator. Then since $f\Avec$ is another vector operator, we must have

:::{math}
:label: eq-zeeman-53
\matrixelement{\gamma'j'm'}{fA_q}{\gamma jm} = \reducedme{\gamma'j'}{(fA)}{\gamma j} \braket{j'm'}{j1mq},
:::

where $\reducedme{\gamma'j'}{(fA)}{\gamma j}$ just means the reduced matrix element for the vector operator $f\Avec$. Also, since $f$ is a scalar, we have

:::{math}
:label: eq-zeeman-54
\matrixelement{\gamma'j'm'}{f}{\gamma jm} = \delta_{m'm}\, \delta_{j'j}\,\reducedme{\gamma' j}{f}{\gamma j},
:::

where the Clebsch-Gordan coefficient is trivial since $k=q=0$.

Show that

:::{math}
:label: eq-zeeman-55
\reducedme{\gamma'j'}{(fA)}{\gamma j}= \sum_\Gamma \reducedme{\gamma'j'}{f}{\Gamma j'} \reducedme{\Gamma j'}{A}{\gamma j}.
:::

\problempart{(b)} For the special case $\Avec=\Jvec$, work out an explicit formula for the reduced matrix element, $\reducedme{\gamma' j'}{J}{\gamma j}$. **Hint:** Take the $q=0$ component, $J_0=J_z$, and use {eq}`eq-jjcouple-72a` to evaluate the Clebsch-Gordan coefficient explicitly. Then solve for the reduced matrix element.

\problempart{(c)} Since $\Avec$ and $\Bvec$ are vector operators, $\Avec\cdot\Bvec$ is a scalar operator. Express the reduced matrix element of the scalar $\Avec\cdot\Bvec$ in terms of the reduced matrix elements of $\Avec$ and $\Bvec$. **Hint:** Note that

:::{math}
:label: eq-zeeman-56
\Avec\cdot\Bvec = \sum_q (\Avec\cdot\evec_q) (\evec_q^\cc\cdot\Bvec)=\sum_q A_q B_q^\hc,
:::

where we use {eq}`eq-wigeck-9`.

\problempart{(d)} Now show that

:::{math}
:label: eq-zeeman-57
\matrixelement{\gamma'j'm'}{(\Avec\cdot\Jvec)\Jvec}{\gamma jm}
:::

vanishes unless $j=j'$. In the case $j=j'$, work out the reduced matrix element in terms of the reduced matrix element of $\Avec$. Use this to show that

:::{math}
:label: eq-zeeman-58
\matrixelement{\gamma' jm'}{(\Avec\cdot\Jvec)\Jvec} {\gamma jm} = j(j+1)\hbar^2 \matrixelement{\gamma'jm'}{\Avec} {\gamma jm},
:::

which is the projection theorem.

(prob-zeeman-4)=

**Problem \prbdzeeman-4..** 

:::{math}
:label: eq-zeeman-59
\psi=\begin{pmatrix}\psi_+ \\ \psi_- \\\end{pmatrix},
:::

as in {eq}`eq-jjcouple-14`. Then the Hermitian conjugate wave function can be seen as a 2-component row spinor,

:::{math}
:label: eq-zeeman-60
\psi^\dagger = (\psi_+^*, \psi_-^*).
:::

In this notation, the normalization integral can be written

:::{math}
:label: eq-zeeman-61
\int d^3\xvec \, \psi^\dagger(\xvec) \psi(\xvec) = 1.
:::

\problempart{(a)} The magnetic moment operator of an electron is given by {eq}`eq-spinmagf-16`, and that of a neutron by {eq}`eq-spinmagf-24`. Find the expectation value of the magnetic moment operator for an electron and for a neutron, when the wave function satisfies $\psi_-(\xvec)=0$, that is, the particle is polarized as “spin up.” Express your answer in terms of $g$-factors and other physical constants.

In this case the expectation value of the magnetic moment vector has only a $z$-component. We consider this $z$-component to be “the magnetic moment” (that is, a scalar value) of the electron or neutron.

\problempart{(b)} Iron has a density of 7.87 $gm/cm^3$, and an atomic weight of 55.8. Assuming each iron atom has an average of one electron aligned in the $z$-direction, find the magnetization $\Mvec$. (The magnetization is defined as the dipole moment per unit volume in both SI and Gaussian units. See Appendix~\emunits. The Gaussian unit of magnetization is $Gauss$, and the SI unit is $J/\\textTesla-m^3$, which is also an $Ampere/m$. One $Ampere/m$ is the same magnetization as as $10^{-3}\,Gauss$.)

A uniformly magnetized sphere has a magnetic field given by

:::{math}
:label: eq-zeeman-62
\Bvec = {8\pi\over 3} \Mvec,
:::

in Gaussian units. Compute the magnetic field strength inside a uniformly magnetized sphere of iron, under the assumptions of the previous paragraph.

Iron actually has four $3d$ electrons whose spins can be aligned. If you multiply your answer by 4, you will get a value close to but somewhat larger than the practical saturation field strength in an iron core magnet. This number is important to experimentalists, for example, particle physicists who must bend particle beams with magnetic fields. To achieve much higher field strengths requires superconductors, which produce them by means of massive currents, without the aid of any substance of high permeability as a core.

\problempart{(c)} A neutron star has a density of $4\times 10^{14} \, gm/cm^3$. Find the magnetic field inside a uniformly magnetized sphere of such material, assuming each neutron is aligned with the magnetic field.

(prob-zeeman-5)=

**Problem \prbdzeeman-5..** 

(prob-zeeman-6)=

**Problem \prbdzeeman-6..** 

The deuteron has only one bound state, the ground state, with energy $E_0=-2.2\,MeV$. It has spin~1 and $g$-factor,

:::{math}
:label: eq-zeeman-63
g_d=0.857.
:::

The deuteron has an observed electric quadrupole moment.

We will model deuterium as a 2-body system consisting of a proton and a neutron. We make the approximation that the masses of the proton and neutron are equal. The proton and neutron both have spin $\frac{1}{2}$ and their $g$-factors are

:::{math}
:label: eq-zeeman-64
g_p=5.586, \qquad g_n=-3.826.
:::

What we call the “spin” of the deuteron is really the total angular momentum of this 2-body system,

:::{math}
:label: eq-zeeman-65
\Ivec=\Lvec+\Svec_p + \Svec_n,
:::

where $\Lvec=\rvec\times\pvec$ is the orbital angular momentum of the relative motion of the 2-body system, and $\Svec_p$ and $\Svec_n$ are the spins of the proton and neutron. The ground state is an eigenstate of $I^2$ with quantum number $i=1$, and is 3-fold degenerate with $m_i=+1,0,-1$.

As explained in {ref}`ch-spinmagf`, when a proton or neutron is placed in a magnetic field, there is an interaction energy given by $-\muvec_p\cdot\Bvec$ or $-\muvec_n\cdot\Bvec$, respectively, where

:::{math}
:label: eq-zeeman-66
\muvec_p = g_p\mu_N\Svec_p, \qquad \muvec_n = g_n\mu_N\Svec_n.
:::

The nuclear magneton $\mu_N$ is a convenient reference for measuring nuclear magnetic moments; it is defined by

:::{math}
:label: eq-zeeman-67
\mu_N={e\hbar\over 2m_p c},
:::

which by convention uses the proton mass, even for the neutron and other particles. When the deuteron is placed in a weak magnetic field, its energy shift is proportional to $m_i$,

:::{math}
:label: eq-zeeman-68
\Delta E=-g_d(\mu_N B)m_i,
:::

which serves to define $g_d$, the deuteron $g$-factor. It is like the Land\'e $g$-factor, which applies to atoms, but one difference is that even very powerful magnetic fields are “weak” by nuclear standards. Our problem will be to explain the observed value of $g_d$ in terms of a 2-body model of the deuteron.

\problempart{(a)} It is shown in Prob. {ref}`prob-variational-2` that the ground state of a central force problem is always an $s$-wave (with $\ell=0$). If deuterium is a central force problem, then its one and only ground state must have $\ell=0$. Then we can ignore $\Lvec$ in {eq}`eq-zeeman-65` and just concentrate on the spin degrees of freedom. (Take the Hilbert space to be just the product of the two spin Hilbert spaces, with $\Ivec=\Svec_p+\Svec_n$.) The perturbing (Zeeman) Hamiltonian is just the interaction of the two spins with the magnetic field,

:::{math}
:label: eq-zeeman-69
H_Z = -(\muvec_p+\muvec_n)\cdot\Bvec = -\mu_N(g_p\Svec_p+g_n\Svec_n)\cdot\Bvec.
:::

The spins must be in the triplet state, since we know that $i=1$.

Use the projection theorem to find an expression for the $g$-factor of the deuteron in this model. Evaluate the expression numerically.

\problempart{(b)} You should get an answer that is pretty good but not perfect. Call this answer $g_{d0}$, the first stab at a theoretical prediction of the $g$-factor of the deuteron.

We conclude that the deuteron is not exactly a central force problem. But the calculation of part (a) shows that the ground state wave function of the deuteron is probably mostly an $s$-wave (because the agreement is pretty good), but that there must be contributions from orbital angular momentum values $\ell\ne0$. Mixing of different $\ell$ values in an energy eigenstate means that $L^2$ is not a good quantum number; if the system is not central force, then this is no surprise.

Hydrogen is not a central force problem, either, if we include the fine structure. We know that fine structure corrections are essentially relativistic, and are of order $(v/c)^2$ compared to nonrelativistic energies. Take the observed binding energy of the deuteron and assume it gives an estimate of the kinetic energy of the proton or neutron as they orbit one another. Use this to obtain an estimate of $v/c$, and compare it to the $v/c$ of the electron in the ground state of hydrogen. Use this to estimate the momentum of the proton or neutron in its orbit around the other particle, and then use the uncertainty princple to estimate the radius of the orbit. You should find a value somewhat larger than the radius of the proton, which is about $1.3\times10^{-13}\,cm$. This is because the deuteron is only weakly bound, and the wave function tunnels significantly into the classically forbidden region.

\problempart{(c)} Henceforth we must include the spatial degrees of freedom in our model, and we cannot ignore $\Lvec$ in {eq}`eq-zeeman-65`. The orbital motion of the proton, a charged particle, must contribute to the magnetic moment of the deuteron.

Let $\ket{\psi}$ be the normalized ground state of deuterium. This is an eigenstate of $I^2$ and $I_z$ with quantum numbers $i=1$ and $m_i$, respectively. Project this onto the eigenspaces of $L^2$, and call the projected vectors $c_\ell\ket{\psi_\ell}$, where $\ket{\psi_\ell}$ is normalized. That is, write

:::{math}
:label: eq-zeeman-70
\ket{\psi}=\sum_\ell c_\ell \ket{\psi_\ell},
:::

where

:::{math}
:label: eq-zeeman-71
\sum_\ell |c_\ell|^2 = 1.
:::

Use the experimental facts and the rules of angular momentum to determine which $\ell$ values may occur in this sum.

We have decided that $c_0\ne0$. Given this and the fact that the strong interactions conserve parity, revise your list of allowed $\ell$ values. See {ref}`sec-parity-8`.

Show that the ground state $\psi$ is an eigenstate of $S^2$, where

:::{math}
:label: eq-zeeman-72
\Svec=\Svec_p+\Svec_n
:::

is the total spin of the proton-neutron system. Note that $\Ivec=\Lvec+\Svec$.

\problempart{(d)} In atoms, the Zeeman Hamiltonian is given by

:::{math}
:label: eq-zeeman-73
H_Z=\mu_B(\Lvec+2\Svec)\cdot\Bvec,
:::

a version of {eq}`eq-zeeman-13`, which shows the $g$-factors ($g=1$ for orbital and $g=2$ for spin) of an electron.

In deuterium, we must take

:::{math}
:label: eq-zeeman-74
H_Z=-\mu_N\Bigl({1\over2}\Lvec + g_p\Svec_p + g_n\Svec_n\Bigr)\cdot\Bvec,
:::

that is, with an orbital $g$ factor of $1/2$. This is because the orbital operator in deuterium $\Lvec=\rvec\cross\pvec$ includes the angular momentum of both the proton and the neutron about their common center of mass, while only the proton contributes to the orbital magnetic moment (because the neutron is neutral). This is where we use the approximation that the proton and neutron masses are equal; it hardly makes a difference for this problem.

Compute the energy shift in terms of the unknown coefficients $c_\ell$. Assume $\Bvec=B{\hat{\mathbf{z}}}$, and notice that the $\Lvec$ term vanishes on an $s$-wave. Explain why the cross terms vanish. For the other terms use the projection theorem, and choose your angular momentum carefully. Find an expression for $g_d$ in terms of the coefficients $c_\ell$.

\problempart{(e)} Plug in the experimental value of $g_d$ and find the probability that the deuteron is not in an $s$-wave. By the way, the nonvanishing electric quadrupole moment also shows that the deuteron is not purely an $s$-wave.
