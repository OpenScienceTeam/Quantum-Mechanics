---
title: "20. The Wigner-Eckart Theorem"
---
(ch-wigeck)=

# 20. The Wigner-Eckart Theorem

(sec-wigeck-1)=

## Introduction

The Wigner-Eckart theorem concerns matrix elements of a type that is of frequent occurrence in all areas of quantum physics, especially in perturbation theory and in the theory of the emission and absorption of radiation. This theorem allows one to determine quickly the selection rules for the matrix element that follow from rotational invariance. In addition, if matrix elements must be calculated, the Wigner-Eckart theorem frequently offers a way of significantly reducing the computational effort. We will make quite a few applications of the Wigner-Eckart theorem in this course.

The Wigner-Eckart theorem is based on an analysis of how operators transform under rotations, a study of which was initiated in {ref}`ch-transfop`. It turns out that operators of a certain type, the irreducible tensor operators, are associated with angular momentum quantum numbers and have transformation properties similar to those of kets with the same quantum numbers. An exploitation of these properties leads to the Wigner-Eckart theorem.

(sec-wigeck-2)=

## The Spherical Basis

We return to our development of the properties of operators under rotations. We take up the subject of the *spherical basis*, which is a basis of unit vectors in ordinary three-dimensional space that is alternative to the usual Cartesian basis. Initially we just present the definition of the spherical basis without motivation, and then we show how it can lead to some dramatic simplifications in certain problems. Then we explain its deeper significance.

We denote the usual Cartesian basis by ${\hat{\mathbf{c}}}_i$, $i=1,2,3$, so that

:::{math}
:label: eq-wigeck-1
{\hat{\mathbf{c}}}_1={\hat{\mathbf{x}}}, \qquad {\hat{\mathbf{c}}}_2={\hat{\mathbf{y}}}, \qquad {\hat{\mathbf{c}}}_3={\hat{\mathbf{z}}}.
:::

We have previously denoted this basis by ${\hat{\mathbf{e}}}_i$, but in these notes we reserve the symbol ${\hat{\mathbf{e}}}$ for the spherical basis.

The spherical basis is defined by

:::{math}
\begin{aligned}
{\hat{\mathbf{e}}}_1 &= -{{\hat{\mathbf{x}}} + i{\hat{\mathbf{y}}} \over \sqrt{2}},
\end{aligned}
:::

:::{math}
\begin{aligned}
{\hat{\mathbf{e}}}_0 &= {\hat{\mathbf{z}}},
\end{aligned}
:::

:::{math}
:label: eq-wigeck-2
\begin{aligned}
{\hat{\mathbf{e}}}_{-1} &= {{\hat{\mathbf{x}}} - i{\hat{\mathbf{y}}} \over \sqrt{2}}.
\end{aligned}
:::

This is a complex basis, so vectors with real components with respect to the Cartesian basis have complex components with respect to the spherical basis. We denote the spherical basis vectors collectively by ${\hat{\mathbf{e}}}_q$, $q=1,0,-1$.

The spherical basis vectors have the following properties. First, they are orthonormal, in the sense that

:::{math}
:label: eq-wigeck-3
{\hat{\mathbf{e}}}_q^\cc \cdot {\hat{\mathbf{e}}}_{q'} = \delta_{qq'}.
:::

Next, an arbitrary vector $\Xvec$ can be expanded as a linear combination of the vectors ${\hat{\mathbf{e}}}^\cc_q$,

:::{math}
:label: eq-wigeck-4
\Xvec = \sum_q {\hat{\mathbf{e}}}^\cc_q  X_q,
:::

where the expansion coefficients are

:::{math}
:label: eq-wigeck-5
X_q = {\hat{\mathbf{e}}}_q \cdot \Xvec.
:::

These equations are equivalent to a resolution of the identity in 3-dimensional space,

:::{math}
:label: eq-wigeck-6
\Imat = \sum_q {\hat{\mathbf{e}}}^\cc_q {\hat{\mathbf{e}}}_q,
:::

in which the juxtaposition of the two vectors is dyad notation for representing the tensor product.

You may wonder why we expand $\Xvec$ as a linear combination of ${\hat{\mathbf{e}}}_q^\cc$, instead of ${\hat{\mathbf{e}}}_q$. The latter type of expansion is possible too, that is, any vector $\Yvec$ can be written

:::{math}
:label: eq-wigeck-7
\Yvec=\sum_q {\hat{\mathbf{e}}}_q Y_q,
:::

where

:::{math}
:label: eq-wigeck-8
Y_q = {\hat{\mathbf{e}}}^\cc_q\cdot\Yvec.
:::

These relations correspond to a different resolution of the identity,

:::{math}
:label: eq-wigeck-9
\Imat = \sum_q {\hat{\mathbf{e}}}_q {\hat{\mathbf{e}}}^\cc_q.
:::

The two types of expansion give the contravariant and covariant components of a vector with respect to the spherical basis; in this course, however, we will only need the expansion indicated by {eq}`eq-wigeck-4`.

(sec-wigeck-3)=

## An Application of the Spherical Basis

To show some of the utility of the spherical basis, we consider the problem of dipole radiative transitions in a single-electron atom such as hydrogen or an alkali. It is shown in {ref}`ch-radnmatt`{} that the transition amplitude for the emission of a photon is proportional to matrix elements of the dipole operator between the initial and final states. We use an electrostatic, spinless model for the atom, as in {ref}`ch-cenforce`, and we consider the transition from initial energy level $E_{n\ell}$ to final level $E_{n'\ell'}$. These levels are degenerate, since the energy does not depend on the magnetic quantum number $m$ or $m'$. The wave functions have the form,

:::{math}
:label: eq-wigeck-10
\psi_{n\ell m}(r,\theta,\phi) = R_{n\ell}(r) Y_{\ell m}(\Omega),
:::

as in {eq}`eq-cenforce-15`.

The dipole operator is proportional to the position operator of the electron, so we must evaluate matrix elements of the form,

:::{math}
:label: eq-wigeck-11
\matrixelement{n\ell m}{\xvec}{n'\ell' m'},
:::

where the initial state is on the left and the final one on the right. The position operator $\xvec$ has three components, and the initial and final levels consist of $2\ell+1$ and $2\ell'+1$ degenerate states, respectively. Therefore if we wish to evaluate the intensity of a spectral line as it would be observed, we really have to evaluate $3(2\ell'+1)(2\ell+1)$ matrix elements, for example, $3\times 3 \times 5=45$ in a $3d \to 2p$ transition. This is because the energy of the photon is $E_\gamma=E_{n\ell}-E_{n'\ell'}$, which is independent of the initial and final $m$ and $m'$ quantum numbers. This count is actually an exaggeration, as we shall see, because many of the matrix elements vanish, but there are still many nonvanishing matrix elements to be calculated.

A great simplification can be achieved by expressing the components of $\xvec$, not with respect to the Cartesian basis, but with respect to the spherical basis. First we define

:::{math}
:label: eq-wigeck-12
x_q = {\hat{\mathbf{e}}}_q\cdot\xvec,
:::

exactly as in Eq.{eq}`eq-wigeck-5`. Next, by inspecting a table of the $Y_{\ell m}$'s (see {ref}`sec-orbamsph-7`), we find that for $\ell=1$ we have

:::{math}
\begin{aligned}
r Y_{11}(\theta,\phi) &= -r \sqrt{ \displaystyle 3 \over \displaystyle 8\pi}\, \sin\theta e^{i\phi} = \sqrt{ \displaystyle 3 \over \displaystyle 4\pi} \Bigl( - {x+iy \over \sqrt{2}} \Bigr),
\end{aligned}
:::

:::{math}
\begin{aligned}
r Y_{10}(\theta,\phi) &= r \sqrt{ \displaystyle 3 \over \displaystyle 4\pi}\, \cos\theta = \sqrt{ \displaystyle 3 \over \displaystyle 4\pi} (z),
\end{aligned}
:::

:::{math}
:label: eq-wigeck-13
\begin{aligned}
r Y_{1,-1}(\theta,\phi) &= r \sqrt{ \displaystyle 3 \over \displaystyle 8\pi}\, \sin\theta e^{-i\phi} = \sqrt{ \displaystyle 3 \over \displaystyle 4\pi} \Bigl( {x-iy \over \sqrt{2}} \Bigr),
\end{aligned}
:::

where we have multiplied each $Y_{1m}$ by the radius $r$. On the right hand side we see the spherical components $x_q$ of the position vector $\xvec$, as follows from the definitions {eq}`eq-wigeck-2`. The results can be summarized by

:::{math}
:label: eq-wigeck-14
r Y_{1q}(\theta,\phi) = \sqrt{ \displaystyle 3 \over \displaystyle 4\pi}\, x_q,
:::

for $q=1,0,-1$, where $q$ appears explicitly as a magnetic quantum number. This equation reveals a relationship between vector operators and the angular momentum value $\ell=1$, something we will have more to say about presently.

Now the matrix elements {eq}`eq-wigeck-11` become a product of a radial integral times an angular integral,

:::{math}
:label: eq-wigeck-15
\begin{aligned}
\matrixelement{n\ell m}{x_q}{n'\ell' m'} &= \int_0^\infty r^2 \, dr \, R^\cc_{n\ell}(r) r R_{n'\ell'}(r) \\
&\quad \times \sqrt{\ds 4\pi \over \ds 3} \int d\Omega \, Y^\cc_{\ell m}(\theta,\phi) Y_{1q}(\theta,\phi) Y_{\ell' m'}(\theta,\phi). \\

\end{aligned}
:::

We see that all the dependence on the three magnetic quantum numbers $(m,q,m')$ is contained in the angular part of the integral. Moreover, the angular integral can be evaluated by the three-$Y_{\ell m}$ formula, {eq}`eq-jjcouple-67`, whereupon it becomes proportional to the Clebsch-Gordan coefficient,

:::{math}
:label: eq-wigeck-16
\braket{\ell m}{\ell' 1 m' q}.
:::

The radial integral is independent of the three magnetic quantum numbers $(m,q,m')$, and the trick we have just used does not help us to evaluate it. But it is only one integral, and after it has been done, all the other integrals can be evaluated just by computing or looking up Clebsch-Gordan coefficients.

The selection rule $m=q+m'$ in the Clebsch-Gordan coefficient {eq}`eq-wigeck-16` means that many of the integrals vanish, so we have exaggerated the total number of integrals that need to be done. But had we worked with the Cartesian components $x_i$ of $\xvec$, this selection rule might not have been obvious. In any case, even with the selection rule, there may still be many nonzero integrals to be done (nine, in the case $3d \to 2p$).

The example we have just given of simplifying the calculation of matrix elements for a dipole transition is really an application of the Wigner-Eckart theorem, which is the main topic of these notes.

The process we have just described is not just a computational trick, rather it has a physical interpretation. The initial and final states of the atom are eigenstates of $L^2$ and $L_z$, and the photon is a particle of spin 1 (see {ref}`ch-quantemf`). Conservation of angular momentum requires that the angular momentum of the initial state (the atom, with quantum numbers $\ell$ and $m$) should be the same as the angular momentum of the final state (the atom, with quantum numbers $\ell'$ and $m'$, plus the photon with spin 1). Thus, the selection rule $m=m'+q$ means that $q$ is the $z$-component of the spin of the emitted photon, so that the $z$-component of angular momentum is conserved in the emission process. As for the selection rule $\ell\in\{\ell'-1,\ell',\ell'+1\}$, it means that the amplitude is zero unless the possible total angular momentum quantum number of the final state, obtained by combining $\ell'\otimes 1$, is the total angular momentum quantum number of the initial state. This example shows the effect of symmetries and conservation laws on the selection rules for matrix elements.

This is only an incomplete accounting of the symmetry principles at work in the matrix element {eq}`eq-wigeck-11` or {eq}`eq-wigeck-15`; as we will see in {ref}`ch-parity`, parity also plays an important role.

(sec-wigeck-4)=

## Significance of the Spherical Basis

To understand the deeper significance of the spherical basis we examine {ref}`tbl-wigeck-1`. The first row of this table summarizes the principal results obtained in {ref}`ch-repsamos`, in which we worked out the matrix representations of angular momentum and rotation operators. To review those results, we start with a ket space (first column) upon which proper rotations act by means of unitary operators $U(\Rmat)$ (second column). We refer only to proper rotations $\Rmat \in SO(3)$, and we note that the representation may be double-valued.

The rotation operators have generators, defined by {eq}`eq-spinrot-13`, that is, that equation can be taken as the definition of $\Jvec$ when the rotation operators $U(\Rmat)$ are given. [{eq}`eq-spinrot-11` is equivalent.] The generators appear in the third column of the table. The components of $\Jvec$ satisfy the usual commutation relations {eq}`eq-spinrot-24` since the operators $U(\Rmat)$ form a representation of the rotation group.

:::{list-table} The rows of the table indicate different vector spaces upon which rotations act by means of unitary operators. The first row refers to a ket space (a Hilbert space of a quantum mechanical system), the second to ordinary three-dimensional space (physical space), and the third to the space of operators. The operators in the third row are the usual linear operators of quantum mechanics that act on the ket space, for example, the Hamiltonian. The first column identifies the vector space. The second column shows how rotations $\Rmat \in SO(3)$ act on the given space. The third column shows the generators of the rotations, that is, the 3-vector of Hermitian operators that specify infinitesimal rotations. The fourth column shows the standard angular momentum basis (SAMB), and the last column, the transformation law of vectors of the standard angular momentum basis under rotations.
:label: tbl-wigeck-1
:header-rows: 1

* - Space
  - Action
  - Ang Mom
  - SAMB
  - Action on SAMB
* - Kets
  - $\ket{\psi} \mapsto U\ket{\psi}$
  - $\Jvec$
  - $\ket{\gamma jm}$
  - $U\ket{\gamma jm} = \sum_{m'} \ket{\gamma jm'} D^j_{m'm}$
* - 3D Space
  - $\xvec \mapsto \Rmat\xvec$
  - $i\Jmatvec$
  - $\evechat_q$
  - $\Rmat \evechat_q = \sum_{q'} \evechat_{q'} D^1_{q'q}$
* - Operators
  - $A \mapsto UAU^\hc$
  - $\ldots$
  - $T^k_q$
  - $UT^k_q U^\hc = \sum_{q'} T^k_{q'} D^k_{q'q}$

:::
Next, since $J^2$ and $J_z$ commute, we construct their simultaneous eigenbasis, with an extra index $\gamma$ to resolve degeneracies. Also, we require states with different $m$ but the same $\gamma$ and $j$ to be related by raising and lowering operators. This creates the standard angular momentum basis (SAMB), indicated in the fourth column.

In the last column, we show how the vectors of the standard angular momentum basis transform under rotations. This table entry is essentially {eq}`eq-repsamos-58`. A basis vector $\ket{\gamma jm}$, when rotated, produces a linear combination of other basis vectors for the same values of $\gamma$ and $j$ but different values of $m$. This implies that the space spanned by $\ket{\gamma jm}$ for fixed $\gamma$ and $j$, but for $m=-j,\ldots,+j$ is invariant under rotations. This space has dimensionality $2j+1$. It is, in fact, an irreducible invariant space.

Note that the $D$-matrices that appear in the transformation law in the last column are universal matrices, dependent only on the angular momentum commutation relations and phase conventions, but independent of the nature of the system. See the discussion in Seec. {ref}`sec-jjcouple-13`.

Now we turn to the other rows of the table. At the beginning of {ref}`ch-repsamos`\ we remarked that the analysis of those notes applies to other spaces besides ket spaces. All that is required is that we have a vector space upon which rotations act by means of unitary operators. For other vectors spaces the notation may change (we will not call the vectors kets, for example), but otherwise everything else goes through.

The second row of {ref}`tbl-wigeck-1` summarizes the case in which the vector space is ordinary three-dimensional (physical) space. Rotations act on this space by means of the matrices $\Rmat$, which, being orthogonal, are also unitary (an orthogonal matrix is a special case of a unitary matrix). The action consists of just rotating vectors in the usual sense, as indicated in the second column.

The generators of rotations in this case must be a vector $\Jvec$ of Hermitian operators, that is, Hermitian matrices, that satisfy

:::{math}
:label: eq-wigeck-17
U({\hat{\mathbf{n}}},\theta) = 1 -{i\over\hbar} \theta {\hat{\mathbf{n}}}\cdot\Jvec,
:::

when $\theta$ is small. Here $U$ really means the same thing as $\Rmat$, since we are speaking of the action on three-dimensional space, and 1 means the same as the identity matrix $\Imat$. We will modify this definition of $\Jvec$ slightly by writing $\Jvec' = \Jvec/\hbar$, thereby absorbing the $\hbar$ into the definition of $\Jvec$ and making $\Jvec'$ dimensionless. This is appropriate when dealing with ordinary physical space, since it has no necessary relation to quantum mechanics. (The spherical basis is also useful in classical mechanics, for example.) Then we will drop the prime, and just remember that in the case of this space, we will use dimensionless generators. Then we have

:::{math}
:label: eq-wigeck-18
U({\hat{\mathbf{n}}},\theta) = 1 -i\theta {\hat{\mathbf{n}}}\cdot\Jvec.
:::

But by a change of notation this is the same as

:::{math}
:label: eq-wigeck-19
R({\hat{\mathbf{n}}},\theta) = \Imat + \theta {\hat{\mathbf{n}}}\cdot\Jmatvec,
:::

as in {eq}`eq-classrot-32`, where the vector of matrices $\Jmatvec$ is defined by {eq}`eq-classrot-22`. These imply

:::{math}
:label: eq-wigeck-20
\Jvec = i\Jmatvec,
:::

as indicated in the third column of {ref}`tbl-wigeck-1`. Writing out the matrices $J_i$ explicitly, we have

:::{math}
:label: eq-wigeck-21
\begin{aligned}
J_1=\begin{pmatrix}0&0&0\\ 0&0&-i\\ 0&i&0\\\end{pmatrix},\quad J_2=\begin{pmatrix}0&0&i\\ 0&0&0\\ -i&0&0\\\end{pmatrix},\quad J_3=\begin{pmatrix}0&-i&0\\ i&0&0\\ 0&0&0\\\end{pmatrix}.
\end{aligned}

:::

These matrices are indeed Hermitian, and they satisfy the dimensionless commutation relations,

:::{math}
:label: eq-wigeck-22
[J_i, J_j] = i \epsilon_{ijk}\, J_k,
:::

as follows from {eq}`eq-wigeck-20` and {eq}`eq-classrot-34`.

We can now construct the standard angular momentum basis on three-dimensional space. In addition to {eq}`eq-wigeck-21`, we need the matrices for $J^2$ and $J_\pm$. These are

:::{math}
:label: eq-wigeck-23
\begin{aligned}
J^2 = \begin{pmatrix}2&0&0\\ 0&2&0\\ 0&0&2\\\end{pmatrix}
\end{aligned}

:::

and

:::{math}
:label: eq-wigeck-24
\begin{aligned}
J_\pm = \begin{pmatrix}0&0&\mp1 \\ 0&0&-i\\ \pm1&i&0\\\end{pmatrix}.
\end{aligned}

:::

We see that $J^2=2\Imat$, which means that every vector in ordinary space is an eigenvector of $J^2$ with eigenvalue $j(j+1)=2$, that is, with $j=1$. An irreducible subspace with $j=1$ in any vector space must be 3-dimensional, but in this case the entire space is 3-dimensional, so the entire space consists of a single irreducible subspace under rotations with $j=1$.

The fact that physical space carries the angular momentum value $j=1$ is closely related to the fact that vector operators are irreducible tensor operators of order 1, as explained below. It is also connected with the fact that the photon, which is represented classically by the vector field $\Avec(\xvec)$ (the vector potential), is a spin-1 particle.

Since every vector in three-dimensional space is an eigenvector of $J^2$, the standard basis consists of the eigenvectors of $J_3$, related by raising and lowering operators (this determines the phase conventions of the vectors, relative to that of the stretched vector). But we can easily check that the spherical unit vectors {eq}`eq-wigeck-2` are the eigenvectors of $J_3$, that is,

:::{math}
:label: eq-wigeck-25
J_3 {\hat{\mathbf{e}}}_q = q\,{\hat{\mathbf{e}}}_q, \qquad q=0,\pm1.
:::

Furthermore, it is easy to check that these vectors are related by raising and lowering operators, that is,

:::{math}
:label: eq-wigeck-26
J_\pm {\hat{\mathbf{e}}}_q = \sqrt{(1\mp q)(1\pm q+1)} \, {\hat{\mathbf{e}}}_{q\pm 1},
:::

where $J_\pm$ is given by {eq}`eq-wigeck-24`. Only the overall phase of the spherical basis vectors is not determined by these relations. The overall phase chosen in the definitions {eq}`eq-wigeck-2` has the nice feature that ${\hat{\mathbf{e}}}_0={\hat{\mathbf{z}}}$.

Since the spherical basis is a standard angular momentum basis, its vectors must transform under rotations according to {eq}`eq-repsamos-87`, apart from notation. Written in the notation appropriate for three-dimensional space, that transformation law becomes

:::{math}
:label: eq-wigeck-27
\Rmat {\hat{\mathbf{e}}}_q = \sum_{q'} {\hat{\mathbf{e}}}_{q'} D^1_{q'q}(\Rmat).
:::

We need not prove this as an independent result; it is just a special case of {eq}`eq-repsamos-87`, in a different notation. This transformation law is also shown in the final column of {ref}`tbl-wigeck-1`, in order to emphasize its similarity to related transformation laws on other spaces.

{eq}`eq-wigeck-27` has an interesting consequence, obtained by dotting both sides with ${\hat{\mathbf{e}}}^\cc_{q'}$. We use a round bracket notation for the dot product on the left hand side, and we use the orthogonality relation {eq}`eq-wigeck-3` on the right hand side, which picks out one term from the sum. We find

:::{math}
:label: eq-wigeck-28
\bigl({\hat{\mathbf{e}}}^\cc_{q'},\Rmat{\hat{\mathbf{e}}}_{q}\bigr) = D^1_{q'q}(\Rmat),
:::

which shows that $D^1_{q'q}$ is just the matrix representing the rotation operator on three-dimensional space with respect to the spherical basis. The usual rotation matrix contains the matrix elements with respect to the Cartesian basis, that is,

:::{math}
:label: eq-wigeck-29
\bigl( {\hat{\mathbf{c}}}_i, \Rmat {\hat{\mathbf{c}}}_j \bigr) = R_{ij}.
:::

See {eq}`eq-classrot-7`. For a given rotation, matrices $\Rmat$ and $D^1(\Rmat)$ are similar (they differ only by a change of basis).

In the third row of the table the vector space upon which rotations act is the space of operators, that is, the usual linear operators in quantum mechanics that map the ket space into itself. The action of rotations on operators is indicated in the second column, which is the same as the definition of the rotated operator presented by {eq}`eq-transfop-7`. The third column, for the generators of rotations, is left blank. It is explored in Prob.~\prbrwigeck-1. For the remaining two columns of the third row of {ref}`tbl-wigeck-1`, we turn the definition of a new class of operators.

(sec-wigeck-5)=

## Irreducible Tensor Operators

We define an *irreducible tensor operator* of order $k$ as a set of $2k+1$ operators $T^k_q$, for $q=-k,\ldots,+k$, that satisfy

:::{math}
:label: eq-wigeck-30
\boxed{U\, T^k_q \, U^\hc = \sum_{q'} T^k_{q'} \, D^k_{q'q}(U),}
:::

for all rotation operators $U$. We denote the irreducible tensor operator itself by $T^k$, and its $2k+1$ components by $T^k_q$. This definition is really a version of {eq}`eq-repsamos-87`, applied to the space of operators. It means that the components of an irreducible tensor operator are basis operators in a standard angular momentum basis that spans an irreducible subspace of operators. Thus we place $T^k_q$ in the SAMB column of the third row of {ref}`tbl-wigeck-1`, and the transformation law {eq}`eq-wigeck-30` in the last column. The three transformation laws in the last column (for three different kinds of spaces) should be compared. We see that the order $k$ of an irreducible tensor operator behaves like an angular momentum quantum number $j$, and $q$ behaves like $m$.

The index $k$ of an irreducible tensor operator of a physical observable is restricted to integer values, $k=0,1,\ldots$. This is unlike the case of the standard angular momentum basis states in a ket space, in which the index $j$ can take on either integer or half-integer values. The physical reason for this is that operators that represent physically observable quantities must be invariant under a rotation of $2\pi$. The mathematical reason is that our definition of a rotated operator, given by {eq}`eq-transfop-6`, is quadratic $U(\Rmat)$, so that the representation of rotations on the vector space of operators is always a single-valued representation of $SO(3)$.

Let us look at some examples of irreducible tensor operators. A scalar operator $K$ is an irreducible tensor operator of order $0$, that is, it is an example of an irreducible tensor operator $T^0_0$. This follows easily from the fact that $K$ commutes with any rotation operator $U$, and from the fact that the $j=0$ rotation matrices are simply given by the $1\times1$ matrix $(1)$ [see {eq}`eq-repsamos-68`].

Irreducible tensor operators of order $1$ are constructed from vector operators by transforming from the Cartesian basis to the spherical basis. If we let $\Vvec$ be a vector operator as defined by {eq}`eq-transfop-14`, and define its spherical components by

:::{math}
:label: eq-wigeck-31
V_q = T^1_q = {\hat{\mathbf{e}}}_q \cdot \Vvec,
:::

then we have

:::{math}
\begin{aligned}
U(\Rmat) V_q U(\Rmat)^\hc &= {\hat{\mathbf{e}}}_q\cdot (\Rmat^{-1}\Vvec) = (\Rmat{\hat{\mathbf{e}}}_q)\cdot\Vvec
\end{aligned}
:::

:::{math}
:label: eq-wigeck-32
\begin{aligned}
&=\sum_{q'} V_{q'} D^1_{q'q}(\Rmat),
\end{aligned}
:::

where we use {eq}`eq-wigeck-27` and {eq}`eq-classrot-72`.

The electric quadrupole operator is given as a Cartesian tensor in {eq}`eq-transfop-29`. This Cartesian tensor is symmetric and traceless, so it contains only 5 independent components, which span an irreducible subspace of operators. In fact, this subspace is associated with angular momentum value $k=2$. It is possible to introduce a set of operators $T^2_q$, $q=-2,\ldots,+2$ that form a standard angular momentum basis in this space, that is, that form an order 2 irreducible tensor operator. These can be regarded as the spherical components of the quadrupole moment tensor. This subject is explored in more detail in Prob.~\prbrwigeck-2.

(sec-wigeck-6)=

## Commutation Relations of an Irreducible Tensor Operator with $\Jvec$

Above we presented two equivalent definitions of scalar and vector operators, one involving transformation properties under rotations, and the other involving commutation relations with $\Jvec$. We will now do the same with irreducible tensor operators. To this end, we substitute the infinitesimal form {eq}`eq-transfop-16` of the rotation operator $U$ into both sides of the definition {eq}`eq-wigeck-30`.

On the right we will need the $D$-matrix for an infinitesimal rotation. Since the $D$-matrix contains just the matrix elements of $U$ with respect to a standard angular momentum basis [this is the definition of the $D$-matrices, see {eq}`eq-repsamos-56`], we require these matrix elements in the case of an infinitesimal rotation. For $\theta\ll 1$, {eq}`eq-repsamos-56` becomes

:::{math}
:label: eq-wigeck-33
D^j_{m'm}({\hat{\mathbf{n}}},\theta) = \matrixelement{jm'} {\Bigl(1-{i\over\hbar} \theta{\hat{\mathbf{n}}}\cdot\Jvec\Bigr)} {jm} = \delta_{m'm} -{i\over\hbar} \theta \matrixelement{jm'}{{\hat{\mathbf{n}}}\cdot\Jvec}{jm}.
:::

Changing notation $(jm'm) \to (kq'q)$ and substituting this and {eq}`eq-transfop-16` into the definition {eq}`eq-wigeck-30` of an irreducible tensor operator, we obtain

:::{math}
:label: eq-wigeck-34
\Bigl(1-{i\over\hbar}\theta{\hat{\mathbf{n}}}\cdot\Jvec\Bigr) T^k_q \Bigl(1+{i\over\hbar}\theta{\hat{\mathbf{n}}}\cdot\Jvec\Bigr)= \sum_{q'} T^k_{q'} \Bigl( \delta_{q'q} -{i\over\hbar} \theta \matrixelement{kq'}{{\hat{\mathbf{n}}}\cdot\Jvec}{kq} \Bigr),
:::

or, since ${\hat{\mathbf{n}}}$ arbitrary unit vector,

:::{math}
:label: eq-wigeck-35
[\Jvec, T^k_q] = \sum_{q'} T^k_{q'} \matrixelement{kq'}{\Jvec}{kq}.
:::

The operators $\Jvec$ on the left- and right-hand sides of {eq}`eq-wigeck-34` and {eq}`eq-wigeck-35` are not the same operators. On the left $\Jvec$ is the angular momentum on the same space upon which the operators $T^k_q$ act; in practice this is usually the state space of a quantum system. The $\Jvec$ on the right is the angular momentum operator on a model space in which the matrices $D^k_{q'q}$ are defined. See the discussion in {ref}`sec-jjcouple-13`.

{eq}`eq-wigeck-35` specifies a complete set of commutation relations of the components of $\Jvec$ with the components of an irreducible tensor operator, but it is usually transformed into a different form. First we take the $z$-component of both sides and use $J_z \ket{kq} = \hbar q \ket{kq}$, so that

:::{math}
:label: eq-wigeck-36
\matrixelement{kq'}{J_z}{kq} = q\hbar \,\delta_{q'q}.
:::

This is {eq}`eq-repsamos-47` with a change of notation. Then {eq}`eq-wigeck-35` becomes {eq}`eq-wigeck-43a` below. Next dot both sides of {eq}`eq-wigeck-35` with ${\hat{\mathbf{x}}}\pm i{\hat{\mathbf{y}}}$, and use

:::{math}
:label: eq-wigeck-37
J_\pm \ket{kq} = \sqrt{(k\mp q)(k\pm q+1)} \hbar \, \ket{k,q\pm1},
:::

or

:::{math}
:label: eq-wigeck-38
\matrixelement{kq'}{J_\pm}{kq} = \sqrt{(k\mp q)(k\pm q+1)} \hbar \, \delta_{q',q\pm1}.
:::

This is {eq}`eq-repsamos-48b` with a change of notation. Then we obtain {eq}`eq-wigeck-43b` below. Finally, take the $i$-th component of {eq}`eq-wigeck-35`,

:::{math}
:label: eq-wigeck-39
[J_i,T^k_q] = \sum_{q'} T^k_{q'} \matrixelement{kq'}{J_i}{kq},
:::

and form the commutator of both sides with $J_i$,

:::{math}
:label: eq-wigeck-40
\begin{aligned}
[J_i,[J_i,T^k_q]] &= \sum_{q'} [J_i,T^k_{q'}] \matrixelement{kq'}{J_i}{kq} =\sum_{q'q''} T^k_{q''} \matrixelement{kq''}{J_i}{kq'} \matrixelement{kq'}{J_i}{kq} \\
&=\sum_{q''} T^k_{q''} \matrixelement{kq''}{J_i^2}{kq}, \\

\end{aligned}
:::

where we have used {eq}`eq-wigeck-35` again to create a double sum. Finally summing both sides over $i$, we obtain,

:::{math}
:label: eq-wigeck-41
\sum_i [J_i,[J_i,T^k_q]] = \sum_{q''} T^k_{q''} \matrixelement{kq''}{J^2}{kq}.
:::

But

:::{math}
:label: eq-wigeck-42
\matrixelement{kq''}{J^2}{kq} = k(k+1)\hbar^2 \, \delta_{q''q},
:::

a version of {eq}`eq-repsamos-46`, so we obtain {eq}`eq-wigeck-43c` below.

In summary, an irreducible tensor operator satisfies the following commutation relations with the components of angular momentum:

:::{math}
:label: eq-wigeck-43a
\begin{aligned}
[J_z, T^k_q] &= \hbar q \, T^k_q,
\end{aligned}
:::

:::{math}
:label: eq-wigeck-43b
\begin{aligned}
[J_\pm, T^k_q] &= \hbar\sqrt{(k\mp q)(k\pm q+1)} \, T^k_{q\pm1},
\end{aligned}
:::

:::{math}
:label: eq-wigeck-43c
\begin{aligned}
\sum_i [J_i,[J_i, T^k_q]] &= \hbar^2 k(k+1) \, T^k_q.
\end{aligned}
:::

We see that forming the commutator with $J_\pm$ plays the role of a raising or lowering operator for the components of an irreducible tensor operator. As we did with scalar and vector operators, we can show that these angular momentum commutation relations are equivalent to the definition {eq}`eq-wigeck-30` of an irreducible tensor operator. This is done by showing that {eq}`eq-wigeck-43a` are equivalent to {eq}`eq-wigeck-30` in the case of infinitesimal rotations, and that if {eq}`eq-wigeck-30` is true for any two rotations, it is also true for their product. Thus by building up finite rotations as products of infinitesimal ones we show the equivalence of {eq}`eq-wigeck-30` and {eq}`eq-wigeck-43a`. Many books take {eq}`eq-wigeck-43a` as the definition of an irreducible tensor operator.

(sec-wigeck-7)=

## Statement and Applications of the Wigner-Eckart Theorem

The Wigner-Eckart theorem is not difficult to remember and it is quite easy to use. In this we discuss the statement of the theorem and ways of thinking about it and its applications, before turning to its proof.

The Wigner-Eckart theorem concerns matrix elements of an irreducible tensor operator with respect to a standard angular momentum basis of kets, something we will write in a general notation as $\matrixelement {\gamma'j'm'} {T^k_q} {\gamma jm}$. As an example of such a matrix element, you may think of the dipole matrix elements $\matrixelement {n'\ell'm'} {x_q} {n\ell m}$ that we examined in \secrwigeck-3. In that case the operator (the position or dipole operator) is an irreducible tensor operator with $k=1$.

The matrix element $\matrixelement {\gamma'j'm'} {T^k_q} {\gamma jm}$ depends on 8 indices, $(\gamma'j'm';\gamma jm; kq)$, and in addition it depends on the specific operator $T$ in question. The Wigner-Eckart theorem concerns the dependence of this matrix element on the three magnetic quantum numbers $(m'mq)$, and states that that dependence is captured by a Clebsch-Gordan coefficient. More specifically, the Wigner-Eckart theorem states that $\matrixelement {\gamma'j'm'} {T^k_q} {\gamma jm}$ is proportional to the Clebsch-Gordan coefficient $\braket{j'm'}{jkmq}$, with a proportionality factor that is independent of the magnetic quantum numbers. That proportionality factor depends in general on everything else besides the magnetic quantum numbers, that is, $(\gamma'j';\gamma j;k)$ and the operator in question. The standard notation for the proportionality factor is $\reducedme{\gamma'j'}{T^k}{\gamma j}$, something that looks like the original matrix element except the magnetic quantum numbers are omitted and a double bar is used. The quantity $\reducedme{\gamma'j'}{T^k}{\gamma j}$ is called the *reduced matrix element*. With this notation, the Wigner-Eckart theorem states

:::{math}
:label: eq-wigeck-44
\boxed{ \matrixelement{\gamma' j'm'}{T^k_q}{\gamma jm} = \reducedme{\gamma' j'}{T^k}{\gamma j} \, \braket{j'm'}{jkmq}.}
:::

The reduced matrix element can be thought of as depending on the irreducible tensor operator $T^k$ and the two irreducible subspaces $(\gamma'j')$ and $(\gamma j)$ that it links. Some authors (for example, Sakurai) include a factor of $1/\sqrt{2j+1}$ on the right hand side of {eq}`eq-wigeck-44`, but here that factor has been absorbed into the definition of the reduced matrix element. The version {eq}`eq-wigeck-44` is easier to remember and closer to the basic idea of the theorem.

To remember the Clebsch-Gordan coefficient it helps to suppress the bra $\bra{\gamma'j'm'}$ from the matrix element and think of the ket $T^k_q \ket{\gamma jm}$, or, more precisely, the $(2j+1)(2k+1)$ kets that are produced by letting $m$ and $q$ vary over their respective ranges. This gives an example of an operator with certain angular momentum indices multiplying a ket with certain angular momentum indices. It turns out that such a product of an operator times a ket has much in common with the product (i.e., the tensor product) of two kets, insofar as the transformation properties of the product under rotations are concerned. That is, suppose we were multiplying a ket $\ket{kq}$ with the given angular momentum quantum numbers times another ket $\ket{jm}$ with different angular momentum quantum numbers. Then we could find the eigenstates of total angular momentum by combining the constituent angular momenta according to $k\otimes j$. Actually, in thinking of kets $T^k_q \ket{jm}$, it is customary to think of the product of the angular momenta in the reverse order, that is, $j\otimes k$. This is an irritating convention because it makes the Wigner-Eckart theorem harder to remember, but I suspect it is done this way because in practice $k$ tends to be small and $j$ large.

In any case, thinking of the product of kets, the product

:::{math}
:label: eq-wigeck-45
\ket{jm} \otimes \ket{kq} = \ket{jkmq}
:::

contains various components of total $J^2$ and $J_z$, that is, it can be expanded as a linear combination of eigenstates of total $J^2$ and $J^z$, with expansion coefficients that are the Clebsch-Gordan coefficients. The coefficient with total angular momentum $j'$ and $z$-component $m'$ is the Clebsch-Gordan coefficient $\braket{j'm'}{jkmq}$, precisely what appears in the Wigner-Eckart theorem {eq}`eq-wigeck-44`.

Probably the most useful application of the Wigner-Eckart theorem is that it allows us to easily write down selection rules for the given matrix element, based on the selection rules of the Clebsch-Gordan coefficient occurring in {eq}`eq-wigeck-44`. In general, a *selection rule* is a rule that tells us when a matrix element must vanish on account of some symmetry consideration. The Wigner-Eckart theorem provides us with all the selection rules that follow from rotational symmetry; a given matrix element may have other selection rules based on other symmetries (for example, parity). The selection rules that follow from the Wigner-Eckart theorem are that the matrix element $\matrixelement{\gamma j'm'}{T^k_q}{\gamma jm}$ vanishes unless $m'=m+q$ and $j'$ takes on one of the values, $|j-k|, |j-k|+1, \ldots, j+k$.

Furthermore, suppose we actually have to evaluate the matrix \ \fi\fi $\matrixelement{\gamma' j'm'}{T^k_q}{\gamma jm}$ for all $(2k+1)(2j+1)$ possibilities we get by varying $q$ and $m$. We must do this, for example, in computing atomic transition rates. (We need not vary $m'$ independently, since the selection rules enforce $m'=m+q$.) Then the Wigner-Eckart theorem tells us that we actually only have to do one of these matrix elements (presumably, whichever is the easiest), because if we know the left hand side of {eq}`eq-wigeck-44` for one set of magnetic quantum numbers, and if we know the Clebsch-Gordan coefficient on the right-hand side, then we can determine the proportionality factor, that is, the reduced matrix element. Then all the other matrix elements for other values of the magnetic quantum numbers follow by computing (or looking up) Clebsch-Gordan coefficients. This procedure requires that the first matrix element we calculate be nonzero.

In some other cases, we have analytic formulas for the reduced matrix element. That was the case of the application in \secrwigeck-3, where the three-$Y_{\ell m}$ formula allowed us to compute the proportionality factor explicitly.

(sec-wigeck-8)=

## The Wigner-Eckart Theorem for Scalar Operators

Let us consider a scalar operator for which $k=q=0$, such as the Hamiltonian $H$ for an isolated system, that is, with $T^0_0=H$. In this case the Clebsch-Gordan coefficient is

:::{math}
:label: eq-wigeck-46
\braket{j'm'}{j0m0} = \delta_{j'j}\, \delta_{m'm},
:::

so the Wigner-Eckart theorem can be written

:::{math}
:label: eq-wigeck-47
\matrixelement{\gamma'j'm'}{H}{\gamma j m} = C^j_{\gamma'\gamma}\, \delta_{j'j} \, \delta_{m'm},
:::

where

:::{math}
:label: eq-wigeck-48
C^j_{\gamma'\gamma}=\reducedme{\gamma'j}{H}{\gamma j}.
:::

The matrix elements of the Hamiltonian of an isolated system in a standard angular momentum basis are diagonal in both $j$ and $m$, and moreover are independent of $m$.

If we wish to find the eigenvalues of the Hamiltonian we can diagonalize the matrices $C^j_{\gamma'\gamma}$, where $j$ labels the matrix and $\gamma,\gamma'=1,\ldots,N_j$, where $N_j$ is the multiplicity of the given $j$ value.

(sec-wigeck-9)=

## Recursion Relations for Matrix Elements

Many books rationalize the Wigner-Eckart theorem by showing that matrix elements of the form $\matrixelement{\gamma'j'm'}{T^k_q}{\gamma jm}$ satisfy the same recursion relations as the Clebsch-Gordan coefficients $\braket{j'm'}{jkmq}$, and by arguing that that fact implies that the two are proportional. The conclusion is correct, but the ususal presentations fall far short of actually proving it. Nevertheless, it is worthwhile outlining the usual argument.

We obtain a selection rule for the matrix element $\matrixelement{\gamma'j'm'}{T^k_q}{\gamma jm}$ by sandwiching $\bra{\gamma'j'm'}$ and $\ket{\gamma jm}$ around the commutation relation {eq}`eq-wigeck-43a`. This gives

:::{math}
:label: eq-wigeck-49
(m'-m-q)\matrixelement{\gamma'j'm'}{T^k_q}{\gamma jm}=0,
:::

so either $m'=m+q$ or $\matrixelement{\gamma'j'm'}{T^k_q}{\gamma jm}=0$.

Similarly, we obtain recursion relations by sandwiching $\bra{\gamma'j'm'}$ and $\ket{\gamma jm}$ around the commutation relations {eq}`eq-wigeck-43b`. Noting that

:::{math}
:label: eq-wigeck-50
\bra{\gamma'j'm'}J_+ = [J_-\ket{\gamma'j'm'}]^\dagger =\sqrt{(j'+m')(j'-m'+1)}\bra{\gamma'j'm'-1},
:::

we obtain

:::{math}
:label: eq-wigeck-51
\begin{aligned}
&\sqrt{(j'+m')(j'-m'+1)}\, \matrixelement{\gamma'j',m'-1}{T^k_q}{\gamma jm} \\
&\qquad=\sqrt{(j-m)(j+m+1)} \, \matrixelement{\gamma'j'm'}{T^k_q}{\gamma j,m+1} \\
&\qquad+\sqrt{(k-q)(k+q+1)}\, \matrixelement{\gamma'j'm'}{T^k_{q+1}}{\gamma jm}, \\

\end{aligned}
:::

which may be compared to the recursion relation {eq}`eq-jjcouple-53` for the Clebsch-Gordan coefficients. Similarly, we find

:::{math}
:label: eq-wigeck-52
\begin{aligned}
&\sqrt{(j'-m')(j'+m'+1)}\, \matrixelement{\gamma'j',m'+1}{T^k_q}{\gamma jm} \\
&\qquad=\sqrt{(j+m)(j-m+1)} \, \matrixelement{\gamma'j'm'}{T^k_q}{\gamma j,m-1} \\
&\qquad+\sqrt{(k+q)(k-q+1)}\, \matrixelement{\gamma'j'm'}{T^k_{q-1}}{\gamma jm}, \\

\end{aligned}
:::

which may be compared to {eq}`eq-jjcouple-54`.

The rest of the proof is based on an argument from linear algebra that proceeds as follows. Let $\Mmat$ be an $n\times n$ matrix and $x$ an $n$-dimensional vector. The equation $\Mmat x=0$ has a set of solutions $\{x\}$ that constitute a vector space, called the *kernel* of $\Mmat$. If $\det\Mmat\ne0$, the kernel is the trivial space $\{0\}$, but if $\det\Mmat=0$ then the dimension of the kernel is $\ge1$.

If the kernel is 1-dimensional, then any solution $x$ is proportional to any nonzero solution $x_0$, that is, $x=c x_0$. In the application to the proof of the Wigner-Eckart theorem, the matrix $\Mmat$ is the set of coefficients of the recursion relations, the unknown $x$ is the collection of matrix elements $\matrixelement{\gamma'j'm'}{T^k_q}{\gamma jm}$, $x_0$ is the set of Clebsch-Gordan coefficients $\braket{j'm'}{jkmq}$, and $c$ is the reduced matrix element.

Since filling in the details of this approach is somewhat tedious, we present an alternative proof of the Wigner-Eckart theorem, one based on the observation that if a set of vectors indexed by $jm$ values transforms under rotations as a standard angular momentum basis, then it is a standard angular momentum basis.

(sec-wigeck-10)=

## Proof of the Wigner-Eckart Theorem

Consider the product of kets $\ket{jm}\otimes \ket{kq} = \ket{jkmq}$ with the given angular momentum quantum numbers, and consider the $(2j+1)(2k+1)$-dimensional product space spanned by such kets when we allow the magnetic quantum numbers $m$ and $q$ to vary over their respective ranges. The eigenstates $\ket{JM}$ of total $J^2$ and $J_z$ in this space are given by the Clebsch-Gordan expansion,

:::{math}
:label: eq-wigeck-53
\ket{JM} = \sum_{mq} \ket{jkmq} \braket{jkmq}{JM}.
:::

Moreover, the states $\ket{JM}$ for fixed $J$ and $M=-J,\ldots,+J$ form a standard angular momentum basis in an invariant, irreducible subspace of dimension $2J+1$ in the product space. This means that the basis states $\ket{JM}$ are not only eigenstates of total $J^2$ and $J_z$, but they are also linked by raising and lowering operators. Equivalently, the states $\ket{JM}$ transform as a standard angular momentum basis under rotations,

:::{math}
:label: eq-wigeck-54
U\ket{JM} = \sum_{M'} \ket{JM'} D^J_{M'M}(U).
:::

Now consider the $(2j+1)(2k+1)$ kets $T^k_q \ket{\gamma jm}$ obtained by varying $m$ and $q$. We construct linear combinations of these with the same Clebsch-Gordan coefficients as in {eq}`eq-wigeck-53`,

:::{math}
:label: eq-wigeck-55
\ket{X;JM} = \sum_{mq} T^k_q \ket{\gamma jm} \braket{jkmq}{JM},
:::

and define the result to be the ket $\ket{X;JM}$, as indicated. The indices $JM$ in the ket $\ket{X;JM}$ indicate that the left-hand side depends on these indices, because the right hand side does; initially we assume nothing else about this notation. Similarly, $X$ simply stands for everything else the left-hand side depends on, that is, $X$ is an abbreviation for the indices $(\gamma kj)$.

However, in view of the similarity between {eq}`eq-wigeck-53` and {eq}`eq-wigeck-55`, we can guess that $\ket{X;JM}$ is actually an eigenstate of $J^2$ and $J_z$ with quantum numbers $J$ and $M$, and that the states $\ket{X;JM}$ are related by raising and lowering operators. That is, we guess

:::{math}
:label: eq-wigeck-56a
\begin{aligned}
J_z \ket{X;JM} &= M\hbar \,\ket{X;JM},
\end{aligned}
:::

:::{math}
:label: eq-wigeck-56b
\begin{aligned}
J_\pm \ket{X;JM} &= \sqrt{(J\mp M)(J\pm M+1)} \hbar \, \ket{X;J,M\pm1},
\end{aligned}
:::

:::{math}
:label: eq-wigeck-56c
\begin{aligned}
J^2 \ket{X;JM} &= J(J+1)\hbar^2 \, \ket{X;JM}.
\end{aligned}
:::

If true, this is equivalent to the transformation law,

:::{math}
:label: eq-wigeck-57
U\ket{X;JM} = \sum_{M'} \ket{X;JM'} \, D^J_{M'M}(U),
:::

exactly as in {eq}`eq-wigeck-54`. Equations~{eq}`eq-wigeck-56a` and {eq}`eq-wigeck-57` are equivalent because {eq}`eq-wigeck-56a` can be obtained from {eq}`eq-wigeck-57` by specializing to infinitesimal rotations, while {eq}`eq-wigeck-57` can be obtained from {eq}`eq-wigeck-56a` by building up finite rotations out of infinitesimal ones.

In \secrwigeck-11 below we will prove that these guesses are correct. For now we merely explore the consequences. To begin, since $\ket{X;JM}$ is an eigenstate of $J^2$ and $J_z$ with quantum numbers $J$ and $M$, it can be expanded as a linear combination of the standard basis kets $\ket{\gamma j m}$ with the same values $j=J$ and $m=M$, but in general all possible values of $\gamma$. That is, we have an expansion of the form,

:::{math}
:label: eq-wigeck-58
\ket{X;JM} = \sum_{\gamma'} \ket{\gamma' JM}\,C^{kJMj}_{\gamma'\gamma},
:::

where the indices on the expansion coefficients $C^{kJMj}_{\gamma'\gamma}$ simply list all the parameters they can depend on. These coefficients, do not, however, depend on $M$, as we show by applying raising or lowering operators to both sides, and using {eq}`eq-wigeck-56b`. This gives

:::{math}
\begin{aligned}
&\sqrt{(J\mp M)(J\pm M+1)}\hbar \, \ket{X;J,M\pm1}
\end{aligned}
:::

:::{math}
:label: eq-wigeck-59
\begin{aligned}
&\qquad\qquad = \sum_{\gamma'} \sqrt{(J\mp M)(J\pm M+1)}\hbar \, \ket{\gamma'J,M\pm1} \, C^{kJMj}_{\gamma'\gamma},
\end{aligned}
:::

or, after canceling the square roots,

:::{math}
:label: eq-wigeck-60
\ket{X;J,M\pm1} = \sum_{\gamma'} \ket{\gamma' J,M\pm1}\,C^{kJMj}_{\gamma'\gamma}.
:::

Comparing this to {eq}`eq-wigeck-58`, we see that the expansion coefficients are the same for all $M$ values, and thus independent of $M$. We will henceforth write simply $C^{kJj}_{\gamma'\gamma}$ for them.

Now we return to the definition {eq}`eq-wigeck-55` of the kets $\ket{X;JM}$ and use the orthogonality of the Clebsch-Gordan coefficients {eq}`eq-jjcouple-50a` to solve for the kets $T^k_q\ket{\gamma jm}$. This gives

:::{math}
:label: eq-wigeck-61
T^k_q \ket{\gamma jm} = \sum_{JM} \ket{X;JM} \braket{JM}{jkmq} = \sum_{\gamma''JM} \ket{\gamma''JM}\, C^{kJj}_{\gamma''\gamma} \, \braket{JM}{jkmq},
:::

where we use {eq}`eq-wigeck-58`, replacing $\gamma'$ with $\gamma''$. Now multiplying this by $\bra{\gamma'j'm'}$ and using the orthonormality of the basis $\ket{\gamma jm}$, we obtain

:::{math}
:label: eq-wigeck-62
\matrixelement{\gamma'j'm'}{T^k_q}{\gamma jm} = C^{kj'j}_{\gamma'\gamma} \, \braket{j'm'}{jkmq},
:::

which is the Wigner-Eckart theorem {eq}`eq-wigeck-44` if we identify

:::{math}
:label: eq-wigeck-63
C^{kj'j}_{\gamma'\gamma} = \reducedme{\gamma'j'}{T^k}{\gamma j}.
:::

(sec-wigeck-11)=

## Proof of {eq}`eq-wigeck-57`

To complete the proof of the Wigner-Eckart theorem we must prove {eq}`eq-wigeck-57`, that is, we must show that the kets $\ket{X;JM}$ transform under rotations like the vectors of a standard angular momentum basis. To do this we call on the definition of $\ket{X;JM}$, {eq}`eq-wigeck-55`, and apply $U$ to both sides,

:::{math}
:label: eq-wigeck-64
U\ket{X;JM} = \sum_{mq} U T^k_q U^\hc \, U\ket{\gamma jm} \braket{jkmq}{JM}.
:::

Next we use the definition of an irreducible tensor operator {eq}`eq-wigeck-30` and the transformation law for standard basis vectors under rotations, {eq}`eq-repsamos-87`, to obtain

:::{math}
:label: eq-wigeck-65
U\ket{X;JM} = \sum_{\begin{matrix}\scriptstyle mq \\
\scriptstyle m'q'\\\end{matrix}} T^k_{q'} \ket{\gamma j m'} \,D^j_{m'm}(U) \,D^k_{q'q}(U)\, \braket{jkmq}{JM}.
:::

We now call on {eq}`eq-jjcouple-64` with a change of indices,

:::{math}
:label: eq-wigeck-66
D^j_{m'm}(U) D^k_{q'q}(U) = \sum_{J'M'M''} \braket{jkm'q'}{J'M'} \,D^{J'}_{M'M''}(U)\, \braket{J'M''}{jkmq},
:::

which expresses the product of $D$-matrices in {eq}`eq-wigeck-65` in terms of single $D$-matrices. When we substitute {eq}`eq-wigeck-66` into {eq}`eq-wigeck-65`, the $m'q'$-sum is doable by the definition {eq}`eq-wigeck-55`,

:::{math}
:label: eq-wigeck-67
\sum_{m'q'} T^k_{q'} \ket{\gamma jm'} \braket{jkm'q'}{J'M'} = \ket{X;J'M'},
:::

and the $mq$-sum is doable by the orthogonality of the Clebsch-Gordan coefficients,

:::{math}
:label: eq-wigeck-68
\sum_{mq} \braket{J'M''}{jkmq} \braket{jkmq}{JM} = \delta_{J'J} \, \delta_{M''M}.
:::

Altogether, {eq}`eq-wigeck-65` becomes

:::{math}
:label: eq-wigeck-69
U\ket{X;JM} = \sum_{J'M'M''} \ket{X;J'M'} D^{J'}_{M'M''}(U)\, \delta_{J'J} \, \delta_{M''M} = \sum_{M'} \ket{X;JM'} D^J_{M'M}(U).
:::

This proves {eq}`eq-wigeck-57`.

(sec-wigeck-12)=

## Products of Irreducible Tensor Operators

As we have seen, the idea behind the Wigner-Eckart theorem is that a product of an irreducible tensor operator $T^k_q$ times a ket of the standard basis $\ket{\gamma jm}$ transforms under rotations exactly as the tensor product of two kets of standard bases with the same quantum numbers, $\ket{jm}\otimes \ket{kq}$. Similarly, it turns out that the product of two irreducible tensor operators, say, $X^{k_1}_{q_1} Y^{k_2}_{q_2}$, transforms under rotations exactly like the tensor product of kets with the same quantum numbers, $\ket{k_1q_1} \otimes \ket{k_2q_2}$. In particular, such a product of operators can be represented as a linear combination of irreducible tensor operators with order $k$ lying in the range $|k_1-k_2|,\ldots, k_1+k_2$, with coefficients that are Clebsch-Gordan coefficients. That is, we can write

:::{math}
:label: eq-wigeck-70
X^{k_1}_{q_1} Y^{k_2}_{q_2} = \sum_{kq} T^k_q \, \braket{kq}{k_1k_2q_1q_2},
:::

where the $T^k_q$ are new irreducible tensor operators.

To prove this, we first solve for $T^k_q$,

:::{math}
:label: eq-wigeck-71
T^k_q = \sum_{q_1q_2} X^{k_1}_{q_1} Y^{k_2}_{q_2} \, \braket{k_1k_2q_1q_2}{kq},
:::

which we must show is an irreducible tensor operator. To do this, we conjugate both sides of this with a rotation operator $U$ and use the fact that $X$ and $Y$ are irreducible tensor operators,

:::{math}
\begin{aligned}
UT^k_q U^\hc &= \sum_{q_1q_2} UX^{k_1}_{q_1} U^\hc \, UY^{k_2}_{q_2} U^\hc \, \braket{k_1k_2q_1q_2}{kq}
\end{aligned}
:::

:::{math}
:label: eq-wigeck-72
\begin{aligned}
&= \sum_{\begin{matrix}\scriptstyle q_1q_2\\ {-2} \scriptstyle q'_1q'_2\\\end{matrix} X^{k_1}_{q'_1} Y^{k_2}_{q'_2} \, D^{k_1}_{q'_1q_1}(U) D^{k_2}_{q'_2q_2}(U)\, \braket{k_1k_2q_1q_2}{kq}. \\}
\end{aligned}

:::

Next we use {eq}`eq-jjcouple-64` with a change of symbols,

:::{math}
:label: eq-wigeck-73
D^{k_1}_{q'_1q_1}(U) D^{k_2}_{q'_2q_2}(U) = \sum_{KQQ'} \braket{k_1k_2q'_1q'_2}{KQ'} D^K_{Q'Q}(U) \braket{KQ}{k_1k_2q_1q_2},
:::

which we substitute into {eq}`eq-wigeck-72`. Then the $q'_1q'_2$-sum is doable in terms of the expression {eq}`eq-wigeck-71` for $T^k_q$,

:::{math}
:label: eq-wigeck-74
\sum_{q'_1q'_2} X^{k_1}_{q'_1} Y^{k_2}_{q'_2} \braket{k_1k_2q'_1q'_2}{KQ'} = T^K_{Q'},
:::

and the $q_1q_2$-sum is doable by the orthogonality of the Clebsch-Gordan coefficients,

:::{math}
:label: eq-wigeck-75
\sum_{q_1q_2} \braket{KQ}{k_1k_2q_1q_2} \braket{k_1k_2q_1q_2}{kq} = \delta_{Kk} \, \delta_{Qq}.
:::

Then {eq}`eq-wigeck-72` becomes

:::{math}
:label: eq-wigeck-76
UT^k_qU^\hc = \sum_{KQQ'} T^K_{Q'} D^K_{Q'Q} \, \delta_{Kk} \, \delta_{Qq} = \sum_{q'} T^k_{q'} D^k_{q'q}(U).
:::

This shows that $T^k_q$ is an irreducible tensor operator, as claimed.

As an application, two vector operators $\Vvec$ and $\Wvec$, may be converted into $k=1$ irreducible tensor operators $V_q$ and $W_q$ by going over to the spherical basis. From these we can construct $k=0,1,2$ irreducible tensor operators according to

:::{math}
:label: eq-wigeck-77
T^k_q = \sum_{q_1q_2} V_{q_1}W_{q_2} \braket{11q_1q_2}{kq}.
:::

This will yield the same decomposition of a second rank tensor discussed in {ref}`sec-transfop-8`, where we found a scalar ($k=0$), a vector ($k=1$), and a symmetric, traceless tensor ($k=2$).

\problems

(prob-wigeck-1)=

**Problem \prbdwigeck-1..** 

Now let $\SS$ be the space of linear operators that act on $\AS$. We call an element of $\SS$ a “super” operator because it acts on ordinary operators; ordinary operators in $\AS$ act on kets in $\ES$. We will denote super-operators with a hat, to distinguish them from ordinary operators. (This terminology has nothing to do with supersymmetry.)

Given an ordinary operator $A \in \AS$, it is possible to associate it in several different ways with a super-operator. For example, we can define a super operator $\hat A_L$, which acts by left multiplication:

:::{math}
:label: eq-wigeck-78
\hat A_L X = AX,
:::

where $X$ is an arbitrary ordinary operator. This equation obviously defines a linear super-operator, that is, $\hat A_L(X+Y) = \hat A_LX + \hat A_LY$, etc. Similarly, we can define a super-operator associated with $A$ by means of right multiplication, or by means of the forming of the commutator, as follows:

:::{math}
:label: eq-wigeck-79
\begin{aligned}
\hat A_R X &= XA, \\
\hat A_C X &= [A,X].
\end{aligned}
:::

There are still other ways of associating an ordinary operator with a super-operator. Let $\Rmat$ be a classical rotation, and let $U(\Rmat)$ be a representation of the rotations acting on the ket space $\ES$. Thus, the operators $U(\Rmat)$ belong to the space $\AS$. Now associate such a rotation operator $U(\Rmat)$ in $\AS$ with a super-operator $\hat U(\Rmat)$ in $\SS$, defined by

:::{math}
:label: eq-wigeck-80
\hat U(\Rmat) X = U(\Rmat) \, X \, U(\Rmat)^\hc.
:::

Again, $\hat U(\Rmat)$ is obviously a linear super-operator.

\problempart{(a)} Show that $\hat U(\Rmat)$ forms a representation of the rotations, that is, that

:::{math}
:label: eq-wigeck-81
\hat U(\Rmat_1) \hat U(\Rmat_2) = \hat U(\Rmat_1\Rmat_2).
:::

This is easy.

Now let $U(\Rmat)$ be infinitesimal as in {eq}`eq-transfop-16`, and let

:::{math}
:label: eq-wigeck-82
\hat U(\Rmat) = 1 -{i\over\hbar} \theta {\hat{\mathbf{n}}}\cdot\hat\Jvec.
:::

(Here the hat on ${\hat{\mathbf{n}}}$ denotes a unit vector, while that on $\hat\Jvec$ denotes a super-operator.) Express the super-operator $\hat\Jvec$ in terms of ordinary operators. Write {eq}`eq-wigeck-43a` in super-operator notation. Work out the commutation relations of the super-operators $\hat \Jvec$.

\problempart{(b)} Now write out nine equations, specifying the action of the three super-operators $\hat J_i$ on the the basis operators $V_j$. Write the answers as linear combinations of the $V_j$'s. Then write out six more equations, specifying the action of the super raising and lowering operators, $\hat J_\pm$, on the three $V_j$.

Now find the operator $A$ that is annihilated by $\hat J_+$. Do this by writing out the unknown operator as a linear combination of the $V_j$'s, in the form

:::{math}
:label: eq-wigeck-83
A = a_x V_x + a_y V_y + a_z V_z,
:::

and then solving for the coefficients $a_i$. Show that this operator is an eigenoperator of $\hat J_z$ with eigenvalue $+\hbar$. In view of these facts, the operator $A$ must be a “stretched” operator for $k=1$; henceforth write $T^1_1$ for it. This operator will have an arbitrary, complex multiplicative constant, call it $c$. Now apply $\hat J_-$, and generate $T^1_0$ and $T^1_{-1}$. Choose the constant $c$ to make $T^1_0$ look as simple as possible. Then write

:::{math}
:label: eq-wigeck-84
T^1_q = {\hat{\mathbf{e}}}_q\cdot\Vvec,
:::

and thereby “discover” the spherical basis.

(prob-wigeck-2)=

**Problem \prbdwigeck-2..** 

\problempart{(a)} In the case of a nucleus, the spin Hilbert space $\ES_spin = \mathspan\{\ket{sm}, m=-s, \ldots, +s\}$ is actually the ground state of the nucleus. It is customary to denote the angular momentum $j$ of the ground state by $s$. This state is $(2s+1)$-fold degenerate. The nuclear spin operator $\Svec$ is really the restriction of the total angular momentum of the nucleus $\Jvec$ to this subspace of the (much larger) nuclear Hilbert space.

Let $A^k_q$ and $B^k_q$ be two irreducible tensor operators on $\ES_spin$. As explained in these notes, when we say “irreducible tensor operator” we are really talking about the collection of $2k+1$ operators obtained by setting $q=-k, \ldots, +k$. Use the Wigner-Eckart theorem to explain why any two such operators of the same order $k$ are proportional to one another. This need not be a long answer.

Thus, all scalars are proportional to a standard scalar ($1$ is convenient), and all vector operators (for example, the magnetic moment $\muvec$) are proportional to a standard vector ($\Svec$ is convenient), etc.

For a given $s$, what is the maximum value of $k$? What is the maximum order of an irreducible tensor operator that can exist on space $\ES_spin$ for a proton (nucleus of ordinary hydrogen)? A deuteron (heavy hydrogen)? An alpha particle (nucleus of helium)? These rules limit the electric and magnetic multipole moments that a nucleus is allowed to have, as is discussed more fully in {ref}`ch-hyperfine`.

\problempart{(b)} Let $\Avec$ and $\Bvec$ be two vector operators (on any Hilbert space, not necessarily $\ES_spin$), with spherical components $A_q$, $B_q$, as in {eq}`eq-wigeck-31`. As explained in the notes, $A_q$ and $B_q$ are $k=1$ irreducible tensor operators. As explained in \secrwigeck-12, it is possible to construct irreducible tensor operators $T^k_q$ for $k=0,1,2$ out of the nine operators, $\{A_q B_{q'}, q,q'=-1,0,1\}$. Write out the three operators $T^0_0$, $T^1_1$ and $T^2_2$ in terms of the Cartesian products $A_i B_j$. Just look up the Clebsch-Gordan coefficients. There are nine operators in $T^0_0$, $T^1_q$ and $T^2_q$, but I'm only asking you to compute these three to save you some work.

Show that $T^0_0$ is proportional to $\Avec\cdot\Bvec$, that $T^1_1$ is proportional to a spherical component of $\Avec \cross \Bvec$, and that $T^2_2$ can be written in terms of the components of the symmetric and traceless part of the Cartesian tensor $A_iB_j$, which is

:::{math}
:label: eq-wigeck-85
{1\over2}(A_iB_j + A_jB_i) - {1\over 3}(\Avec\cdot\Bvec) \delta_{ij}.
:::

\problempart{(c}) In classical electrostatics, the quadrupole moment tensor $Q_{ij}$ of a charge distribution $\rho(\xvec)$ is defined by

:::{math}
:label: eq-wigeck-86
Q_{ij} = \int d^3\xvec \, \rho(\xvec) [3x_i x_j - r^2\, \delta_{ij}],
:::

where $\xvec$ is measured relative to some origin inside the charge distribution. The quadrupole moment tensor is a symmetric, traceless tensor. The quadrupole energy of interaction of the charge distribution with an external electric field $\Evec = -\del\phi$ is

:::{math}
:label: eq-wigeck-87
E_quad = {1\over 6} \sum_{ij} Q_{ij} {\partial^2 \phi(0) \over \partial x_i \partial x_j}.
:::

This energy must be added to the monopole and dipole energies, plus the higher multipole energies.

In the case of a nucleus, we choose the origin to be the center of mass, whereupon the dipole moment and dipole energy vanish. The monopole energy is just the usual Coulomb energy $q\phi(0)$, where $q$ is the total charge of the nucleus. Thus, the quadrupole term is the first nonvanishing correction. However, the energy must be understood in the quantum mechanical sense.

Let $\{ \xvec_\alpha, \alpha=1, \ldots, Z \}$ be the position operators for the protons in a nucleus. The neutrons are neutral, and do not contribute to the electrostatic energy. The electric quadrupole moment operator for the nucleus is defined by

:::{math}
:label: eq-wigeck-88
Q_{ij} = e \sum_\alpha (3x_{\alpha i} x_{\alpha j} - r^2_\alpha \, \delta_{ij}),
:::

where $e$ is the charge of a single proton. In an external electric field, the nuclear Hamiltonian contains a term $H_quad$, exactly in the form of {eq}`eq-wigeck-87`, but now interpreted as an operator.

The operator $Q_{ij}$, being symmetric and traceless, constitutes the Cartesian specification of a $k=2$ irreducible tensor operator, that you could turn into standard form $T^2_q, q=-2, \ldots, +2$ using the method of part (b) if you wanted to. We'll stay with the Cartesian form here, however. When the operator $Q_{ij}$ is restricted to the ground state (really a manifold of $2s+1$ degenerate states), it remains a $k=2$ irreducible tensor operator. According to part (a), it must be proportional to some standard irreducible tensor operator, for which $3S_i S_j - S^2 \delta_{ij}$ is convenient. That is, we must be able to write

:::{math}
:label: eq-wigeck-89
Q_{ij} = a(3S_i S_j - S^2 \delta_{ij}),
:::

for some constant $a$.

It is customary in nuclear physics to denote the “quadrupole moment” of the nucleus by the real number $Q$, defined by

:::{math}
:label: eq-wigeck-90
Q = \matrixelement{ss}{Q_{33}}{ss},
:::

where $\ket{ss}$ is the stretched state. Don't confuse $Q_{ij}$, a tensor of operators, with $Q$, a single number.

The book, *Modern Quantum Mechanics* by J. J. Sakurai gives the interaction energy of a nucleus in an external electric field as

:::{math}
:label: eq-wigeck-91
H_int = {eQ \over 2s(s-1)\hbar^2} \Bigl[ \Bigl({\partial^2 \phi \over \partial x^2}\Bigr)S_x^2 + \Bigl({\partial^2 \phi \over \partial y^2}\Bigr)S_y^2 + \Bigl({\partial^2 \phi \over \partial z^2}\Bigr)S_z^2\Bigr],
:::

where $\phi$ is the electrostatic potential for the external field satisfying the Laplace equation $\del^2\phi=0$ and where the coordinate axes are chosen so that the off-diagonal elements of $\partial^2\phi/\partial x_i \partial x_j$ vanish. Here $\phi$ and its derivatives are evaluated at the center of mass of the nucleus and $\phi$ satisfies the Laplace equation rather than the Poisson equation because the sources of the external electric field are outside the nucleus.

Express the quantity $a$ in {eq}`eq-wigeck-89` in terms of $Q$, and derive a version of {eq}`eq-wigeck-91`. This equation, copied out of the book, has an error in it; correct it.

(prob-wigeck-3)=

**Problem \prbdwigeck-3..** 

A spin-$\frac{3}{2}$ nucleus situated at the origin is subjected to an external inhomogeneous electric field. The basic electric quadrupole interaction is given by {eq}`eq-wigeck-91` (but corrected), where as above $\phi$ satisfies the Laplace equation and the off-diagonal components $\partial^2\phi/\partial x_i\partial x_j$ vanish. Show that the interaction energy can be written

:::{math}
:label: eq-wigeck-92
A(3S_z^2-S^2) + B(S_+^2+S_-^2),
:::

and express $A$ and $B$ in terms of the nonvanishing second derivatives of $\phi$, evaluated at the origin. Determine the energy eigenkets (in terms of $\ket{m}$, where $m=\pm\frac{3}{2}, \pm\frac{1}{2}$) and the corresponding energy eigenvalues. Is there any degeneracy?
