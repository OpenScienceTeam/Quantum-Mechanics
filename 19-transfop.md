---
title: "19. Transformation of Operators Under Rotations"
---
(ch-transfop)=

# 19. Transformation of Operators Under Rotations

(sec-transfop-1)=

## Introduction

In both classical and quantum mechanics we classify observables according to how they transform under symmetries, including proper rotations, improper rotations, Lorentz transformations, etc. For example, we speak of scalars, vectors, tensors, pseudoscalars, pseudovectors, etc. In these notes we examine how operators transform under proper rotations, developing a classification scheme that will be important for understanding rotational symmetry in quantum mechanics. We will take up the case of improper rotations in {ref}`ch-parity`, time reversal in {ref}`ch-timerev`, and Lorentz transformations in {ref}`ch-covariance`. The material of these notes is background on the Wigner-Eckart theorem, which we take up in {ref}`ch-wigeck`.

(sec-transfop-2)=

## Definition of a Rotated Operator

We consider a quantum mechanical system with a ket space upon which rotation operators $U(\Rmat)$, forming a representation of the classical rotation group $SO(3)$, are defined. The representation will be double-valued if the angular momentum of the system is a half-integer. In these notes we consider only proper rotations $\Rmat$; improper rotations will be taken up later. The operators $U(\Rmat)$ map kets into new or rotated kets,

:::{math}
:label: eq-transfop-1
\ket{\psi'} = U(\Rmat) \ket{\psi},
:::

where $\ket{\psi'}$ is the rotated ket. We will also write this as

:::{math}
:label: eq-transfop-2
\ket{\psi} \mathrel{\mathop{\\text{\rightarrowfill}}^{\Rmat}} U(\Rmat)\ket{\psi}.
:::

In the case of half-integer angular momenta, the mapping above is only determined to within a sign by the classical rotation $\Rmat$.

Now if $A$ is an operator, we define the *rotated operator* $A'$ by requiring that the expectation value of the original operator with respect to the initial state be equal to the expectation value of the rotated operator with respect to the rotated state, that is,

:::{math}
:label: eq-transfop-3
\matrixelement{\psi'}{A'}{\psi'} = \matrixelement{\psi}{A}{\psi},
:::

which is to hold for all initial states $\ket{\psi}$. But this implies

:::{math}
:label: eq-transfop-4
\matrixelement{\psi}{U(\Rmat)^\hc \,A'\, U(\Rmat)}{\psi} =\matrixelement{\psi}{A}{\psi},
:::

or, since $\ket{\psi}$ is arbitrary [see Prob. {ref}`prob-hilbert-6`(b)],

:::{math}
:label: eq-transfop-5
U(\Rmat)^\hc \, A' \, U(\Rmat) = A.
:::

Solving for $A'$, this becomes

:::{math}
:label: eq-transfop-6
A' = U(\Rmat) \, A \, U(\Rmat)^\hc,
:::

which is our definition of the rotated operator. We will also write this in the form,

:::{math}
:label: eq-transfop-7
A \mathrel{\mathop{\\text{\rightarrowfill}}^{\Rmat}} U(\Rmat) \, A \, U(\Rmat)^\hc.
:::

Notice that in the case of half-integer angular momenta the rotated operator is specified by the $SO(3)$ rotation matrix $\Rmat$ alone, since the sign of $U(\Rmat)$ cancels and the answer does not depend on which of the two rotation operators is used on the right hand side. This is unlike the case of rotating kets, where the sign does matter. {eq}`eq-transfop-7` defines the action of rotations on operators.

(sec-transfop-3)=

## Scalar Operators

Now we classify operators by how they transform under rotations. First we define a *scalar operator* $K$ to be an operator that is invariant under rotations, that is, that satisfies

:::{math}
:label: eq-transfop-8
\boxed{U(\Rmat) \, K \, U(\Rmat)^\hc = K,}
:::

for all operators $U(\Rmat)$. This terminology is obvious. Notice that it is equivalent to the statement that a scalar operator commutes with all rotations,

:::{math}
:label: eq-transfop-9
[U(\Rmat), K] =0.
:::

If an operator commutes with all rotations, then it commutes in particular with infinitesimal rotations, and hence with the generators $\Jvec$. See {eq}`eq-spinrot-13`. Conversely, if an operator commutes with $\Jvec$ (all three components), then it commutes with any function of $\Jvec$, such as the rotation operators. Thus another equivalent definition of a scalar operator is one that satisfies

:::{math}
:label: eq-transfop-10
\boxed{[\Jvec,K]=0.}
:::

The most important example of a scalar operator is the Hamiltonian for an isolated system, not interacting with any external fields. The consequences of this for the eigenvalues and eigenstates of the Hamiltonian are discussed in Secs.~\secrtransfop-9 and \secrtransfop-12 below.

(sec-transfop-4)=

## Vector Operators

In ordinary vector analysis in three-dimensional Euclidean space, a vector is defined as a collection of three numbers that have certain transformation properties under rotations. It is not sufficient just to have a collection of three numbers; they must in addition transform properly. Similarly, in quantum mechanics, we define a *vector operator* as a vector *of* operators (that is, a set of three operators) with certain transformation properties under rotations.

Our requirement shall be that the expectation value of a vector operator, which is a vector of ordinary or $c$-numbers, should transform as a vector in ordinary vector analysis. This means that if $\ket{\psi}$ is a state and $\ket{\psi'}=U(\Rmat)\ket{\psi}$ is the rotated state as in {eq}`eq-transfop-1`, then

:::{math}
:label: eq-transfop-11
\matrixelement{\psi'}{\Vvec}{\psi'} = \Rmat \matrixelement{\psi}{\Vvec}{\psi},
:::

which must hold if $\Vvec$ is to be considered a genuine vector operator. In case the notation in {eq}`eq-transfop-11` is not clear, we write the same equation out in components,

:::{math}
:label: eq-transfop-12
\matrixelement{\psi'}{V_i}{\psi'} = \sum_j R_{ij} \matrixelement{\psi}{V_j}{\psi}.
:::

{eq}`eq-transfop-11` or {eq}`eq-transfop-12` is to hold for all $\ket{\psi}$, so by {eq}`eq-transfop-1` they imply

:::{math}
:label: eq-transfop-13
U(\Rmat)^\dagger \, \Vvec \,U(\Rmat) = \Rmat\Vvec,
:::

or, (after swapping $\Rmat$ and $\Rmat^{-1}$)

:::{math}
:label: eq-transfop-14
U(\Rmat) \, \Vvec \, U(\Rmat)^\hc = \Rmat^{-1} \Vvec.
:::

Inn components this is

:::{math}
:label: eq-transfop-15
\boxed{U(\Rmat) \, V_i \, U(\Rmat)^\hc = \sum_j V_j \, R_{ji}.}
:::

We will take {eq}`eq-transfop-13`, {eq}`eq-transfop-14` or {eq}`eq-transfop-15` as the definition of a vector operator.

In the case of a scalar operator, we had one definition {eq}`eq-transfop-8` involving its properties under conjugation by rotations, and another {eq}`eq-transfop-10` involving its commutation relations with the angular momentum $\Jvec$. The latter is in effect a version of the former, when the rotation is infinitesimal. Similarly, for vector operators there is a definition equivalent to {eq}`eq-transfop-14` or {eq}`eq-transfop-15` that involves commutation relations with $\Jvec$. To derive it we let $U$ and $\Rmat$ in {eq}`eq-transfop-14` have axis-angle form with an angle $\theta\ll 1$, so that

:::{math}
:label: eq-transfop-16
U(\Rmat) = 1 - {i\over\hbar} \theta {\hat{\mathbf{n}}}\cdot\Jvec,
:::

and

:::{math}
:label: eq-transfop-17
\Rmat = \Imat + \theta {\hat{\mathbf{n}}}\cdot\Jmatvec.
:::

See {eq}`eq-classrot-22` and {eq}`eq-classrot-32` for the latter. Then the definition {eq}`eq-transfop-14` becomes

:::{math}
:label: eq-transfop-18
\Bigl( 1 -{i\over\hbar} \theta{\hat{\mathbf{n}}}\cdot\Jvec \Bigr) \Vvec \Bigr( 1 +{i\over\hbar} \theta{\hat{\mathbf{n}}}\cdot\Jvec \Bigr) = (\Imat - \theta {\hat{\mathbf{n}}}\cdot\Jmatvec) \Vvec,
:::

or

:::{math}
:label: eq-transfop-19
[ {\hat{\mathbf{n}}}\cdot\Jvec, \Vvec] = -i\hbar \, {\hat{\mathbf{n}}}\cross\Vvec.
:::

Taking the $j$-th component of this, we have

:::{math}
:label: eq-transfop-20
n_i[J_i,V_j] = -i\hbar \, \epsilon_{jik}\, n_i V_k,
:::

or, since ${\hat{\mathbf{n}}}$ is an arbitrary unit vector,

:::{math}
:label: eq-transfop-21
\boxed{[ J_i, V_j ] = i\hbar \, \epsilon_{ijk} \, V_k.}
:::

Any vector operator satisfies this commutation relation with the angular momentum of the system.

The converse is also true; if {eq}`eq-transfop-21` is satisfied, then $\Vvec$ is a vector operator. This follows since {eq}`eq-transfop-21` implies {eq}`eq-transfop-19` which implies {eq}`eq-transfop-18`, that is, it implies that the definition {eq}`eq-transfop-14` is satisfied for infinitesimal rotations. But it is easy to show that if {eq}`eq-transfop-14` is true for two rotations $\Rmat_1$ and $\Rmat_2$, then it is true for the product $\Rmat_1\Rmat_2$. Therefore, since finite rotations can be built up as the product of a large number of infinitesimal rotations (that is, as a limit), {eq}`eq-transfop-21` implies {eq}`eq-transfop-14` for all rotations. Equations {eq}`eq-transfop-14` and {eq}`eq-transfop-21` are equivalent ways of defining a vector operator.

We have now defined scalar and vector operators. Combining them, we can prove various theorems. For example, if $\Vvec$ and $\Wvec$ are vector operators, then $\Vvec\cdot\Wvec$ is a scalar operator, and $\Vvec\cross\Wvec$ is a vector operator. This is of course just as in vector algebra, except that we must remember that operators do not commute, in general. For example, it is not generally true that $\Vvec\cdot\Wvec=\Wvec\cdot\Vvec$, or that $\Vvec\cross\Wvec = -\Wvec\cross\Vvec$.

If we wish to show that an operator is a scalar, we can compute its commutation relations with the angular momentum, as in {eq}`eq-transfop-10`. However, it may be easier to consider what happens when the operator is conjugated by rotations. For example, the central force Hamiltonian {eq}`eq-cenforce-1` is a scalar because it is a function of the dot products $\pvec\cdot\pvec = p^2$ and $\xvec\cdot\xvec = r^2$. See {ref}`sec-cenforce-2`.

(sec-transfop-5)=

## Examples of Vector Operators

Consider a system consisting of a single spinless particle moving in three-dimensional space, for which the wave functions are $\psi(\xvec)$ and the angular momentum is $\Lvec = \xvec\cross \pvec$. To see whether $\xvec$ is a vector operator (we expect it is), we compute the commutation relations with $\Lvec$, finding,

:::{math}
:label: eq-transfop-22
[L_i, x_j] = i\hbar \, \epsilon_{ijk} \, x_k.
:::

According to {eq}`eq-transfop-21`, this confirms our expectation. Similarly, we find

:::{math}
:label: eq-transfop-23
[L_i,p_j] = i\hbar \, \epsilon_{ijk} \, p_k,
:::

so that $\pvec$ is also a vector operator. Then $\xvec \cross \pvec$ (see transfop-4) must also be a vector operator, that is, we must have

:::{math}
:label: eq-transfop-24
[L_i, L_j] = i\hbar \, \epsilon_{ijk} \, L_k.
:::

This last equation is of course just the angular momentum commutation relations, but here with a new interpretation. More generally, by comparing the adjoint formula {eq}`eq-repsamos-91` with the commutation relations {eq}`eq-transfop-21`, we see that the angular momentum $\Jvec$ is always a vector operator.

(sec-transfop-6)=

## If it Looks Like a Vector $\ldots$

Not everything that looks like a vector is a vector operator, according to our definition {eq}`eq-transfop-15`. Consider, for example, the Stark effect, in which an atom interacts with an external electric field $\Evec_0$. If the atom has a single electron, then the interaction term in the Hamiltonian is the potential

:::{math}
:label: eq-transfop-25
V_1(\xvec) = e\Evec_0\cdot\xvec.
:::

The vector $\xvec$ is a vector operator, as we have seen, but what about $\Evec_0$? It is in fact just a vector of $c$-numbers, which, regarded as multiplicative operators on wave functions, commute with everything. Therefore we have

:::{math}
:label: eq-transfop-26
U(\Rmat)\Evec_0 U(\Rmat)^\dagger = \Evec_0,
:::

which does not satisfy the definition {eq}`eq-transfop-15` of a vector operator. Since $\Evec_0$ is not a vector operator, $V_1(\xvec)$ is not a scalar operator.

To understand this situation, we note that the rotation operators $U(\Rmat)$ rotate the physical observables of our system, such as the position $\xvec$ and momentum $\pvec$ of the electron. They do not rotate external parameters, such as $\Evec_0$. On the other hand, the external electric field $\Evec_0$ is created by some charges somewhere. Imagine, for example, that the atom is between the plates of a capacitor, with charges arrayed along the plates to create $\Evec_0$. If these charges are included in “the system,” then when we rotate the system the field $\Evec_0$ is rotated as well. Then $\Evec_0$ becomes a vector operator and $V_1$ becomes a scalar operator.

We will see similar issues regarding the definition of “the system” when we come to conservation of parity and time reversal.

(sec-transfop-7)=

## Tensor Operators

Finally we define a *tensor operator* as a tensor *of* operators with certain transformation properties that we will illustrate in the case of a rank-2 tensor. In this case we have a set of 9 operators $T_{ij}$, where $i,j=1,2,3$, which can be thought of as a $3\times 3$ matrix of operators. These are required to transform under rotations according to

:::{math}
:label: eq-transfop-27
U(\Rmat) \, T_{ij} \, U(\Rmat)^\hc = \sum_{k\ell} T_{k\ell}\, R_{ki} R_{\ell j},
:::

which is a generalization of {eq}`eq-transfop-15` for vector operators. As with scalar and vector operators, a definition equivalent to {eq}`eq-transfop-27` may be given that involves the commutation relations of $T_{ij}$ with the components of angular momentum.

As an example of a tensor operator, let $\Vvec$ and $\Wvec$ be vector operators, and write

:::{math}
:label: eq-transfop-28
T_{ij} = V_i W_j.
:::

Then $T_{ij}$ is a tensor operator (it is the tensor product of $\Vvec$ with $\Wvec$). This is just an example; in general, a tensor operator cannot be written as the product of two vector operators as in {eq}`eq-transfop-28`. In practice, however, many tensor operators appear as linear combinations of such products.

Consider, for example, the quadrupole moment operator. In a system with a collection of particles with positions $\xvec_\alpha$ and charges $q_\alpha$, where $\alpha$ indexes the particles, the quadrupole moment operator is

:::{math}
:label: eq-transfop-29
Q_{ij} = \sum_\alpha q_\alpha(3x_{\alpha i}\,x_{\alpha j} - r_\alpha^2 \, \delta_{ij}).
:::

This is obtained from {eq}`eq-orbamsph-88` by setting

:::{math}
:label: eq-transfop-30
\rho(\xvec) = \sum_\alpha q_\alpha\, \delta(\xvec-\xvec_\alpha).
:::

The quadrupole moment operator is especially important in nuclear physics, in which the particles are the protons in a nucleus with charge $q=e$. Notice that the first term under the sum {eq}`eq-transfop-29` is an operator of the form {eq}`eq-transfop-28`, with $\Vvec = \Wvec = \xvec_\alpha$.

Tensor operators of other ranks (besides 2) are possible; a scalar is considered a tensor operator of rank 0, and a vector is considered a tensor of rank 1. In the case of tensors of arbitrary rank, the transformation law involves one copy of the matrix $\Rmat^{-1}=\Rmat^t$ for each index of the tensor.

(sec-transfop-8)=

## Invariant and Irreducible Subspaces of Operators

Let us return to {eq}`eq-transfop-15`, the transformation law defining a vector operator. This says that if we rotate any one of the components of a vector operator, we get a linear combination of the three components of that vector operator. The same is true if we rotate any linear combination of the three components.

In this respect it is useful to think of the space of operators as a vector space, and the components of a vector operator as “basis operators” that span a 3-dimensional subspace of the space of operators. (We assume the vector operator is not identically zero.) Operators form a vector space because they can be added to one another and multiplied by scalars, that is, linear combinations of operators are operators.

Then the 3-dimensional subspace of operators spanned by the components of a vector operator is invariant under the action of rotations, which is defined by {eq}`eq-transfop-7`. This means that if we rotate any operator belonging to this subspace, we obtain another operator belonging to the same subspace, a fact that is a simple consequence of {eq}`eq-transfop-15`.

Similarly, the nine components $T_{ij}$ of a tensor operator, if linearly independent, span a 9-dimensional space of operators that according to the definition {eq}`eq-transfop-27` is invariant under the action of rotations.

Another example of an invariant subspace of operators is the 1-dimensional subspace spanned by any nonzero scalar operator $K$, as follows from the definition {eq}`eq-transfop-8` of a scalar operator.

Thus, we have three examples of subspaces of operators that are invariant under rotations, those spanned by the components of a scalar operator, a vector operator, or a second-rank tensor operator, which are of dimensionality 1, 3 and 9 respectively.

Now in general when we have a subspace (of any vector space) that is invariant under rotations, we can ask if it possesses a smaller subspace that is also invariant. If it does, we say it is *reducible*; it not, it is *irreducible*. Invariant, reducible subspaces can always be broken up into smaller invariant, irreducible subspaces, so that the irreducible subspaces are the building blocks of reducible subspaces. It turns out that the invariant, irreducible subspaces are orthogonal to one another.

By our definition, every invariant, 1-dimensional subspace is automatically irreducible, because it contains no smaller subspace. Therefore the 1-dimensional subspace of operators spanned by a scalar operator is automatically irreducible.

What about the 3-dimensional subspace spanned by the components of any nonzero vector operator? It turns out that this, too, is irreducible. See Prob.~\prbrtransfop-2.

What about the 9-dimensional space spanned by the components $T_{ij}$ of a tensor operator (we assume the nine components are linearly independent)? It turns out this subspace is reducible. To see how, let us work with the example {eq}`eq-transfop-28` of a tensor operator, $T_{ij}=V_iW_j$. We draw attention to the trace of this tensor,

:::{math}
:label: eq-transfop-31
\tr T = \sum_i T_{ii} = \sum_i V_i W_i = \Vvec\cdot\Wvec,
:::

which as shown is the dot product of the two vector operators $\Vvec$ and $\Wvec$. This is a scalar, which is invariant under rotations, so the 9-dimensional space of operators spanned by the $T_{ij}$ has a 1-dimensional, invariant subspace, spanned by $T_{11}+T_{22}+T_{33}$. This subspace, being 1-dimensional, is irreducible.

This leaves a complementary, 8-dimensional subspace of operators. Is this reducible? Yes, it possesses a 3-dimensional invariant subspace spanned by the operators

:::{math}
:label: eq-transfop-32
\begin{aligned}
X_3 &= T_{12} - T_{21} = V_1 W_2 - V_2 W_1, \\
X_1 &= T_{23} - T_{32} = V_2 W_3 - V_3 W_2, \\
X_2 &= T_{31} - T_{13} = V_3 W_1 - V_1 W_3, \\

\end{aligned}
:::

or, in other words,

:::{math}
:label: eq-transfop-33
\Xvec = \Vvec \cross \Wvec.
:::

The components of $\Xvec$ form a vector operator, so by themselves they span an irreducible invariant subspace under rotations. As we see, the components of $\Xvec$ contain the antisymmetric part of the original tensor $T_{ij}$.

The remaining 5-dimensional subspace is irreducible. It is spanned by operators containing the symmetric part of the tensor $T_{ij}$, with the trace removed (or, as we say, the symmetric, traceless part of $T_{ij}$). The following five operators form a basis in this subspace:

:::{math}
:label: eq-transfop-34
\begin{aligned}
S_1 &= T_{12} + T_{21}, \\
S_2 &= T_{23} + T_{32}, \\
S_3 &= T_{31} + T_{13}, \\
S_4 &= T_{11} - T_{22}, \\
S_5 &= T_{11} + T_{22} - 2T_{33}. \\

\end{aligned}
:::

The original tensor $T_{ij}$ breaks up in three irreducible subspaces, a 1-dimensional scalar (the trace), a 3-dimensional vector (the antisymmetric part), and the 5-dimensional symmetric, traceless part. Notice that these dimensionalities are in accordance with the Clebsch-Gordan decomposition,

:::{math}
:label: eq-transfop-35
1 \otimes 1 = 0 \oplus 1 \oplus 2,
:::

which corresponds to the count of dimensionalities,

:::{math}
:label: eq-transfop-36
3 \times 3 = 1 + 3 + 5 = 9.
:::

This Clebsch-Gordan series arises because the vector operators $\Vvec$ and $\Wvec$ form two $\ell=1$ irreducible subspaces of operators, and when we form $T$ according to $T_{ij} = V_i W_j$, we are effectively combining angular momenta as indicated by {eq}`eq-transfop-35`. The only difference from our usual practice is that we are forming products of vector spaces of operators, instead of tensor products of ket spaces.

We have examined this decomposition in the special case $T_{ij} = V_i W_j$, but the decomposition itself applies to any second rank tensor $T_{ij}$. More generally, Cartesian tensors of any rank $\ge 2$ are reducible.

It is possible that a given tensor $T_{ij}$ may have one or more of the three irreducible components that vanish. The quadrupole moment tensor {eq}`eq-transfop-29`, for example, is already symmetric and traceless, so its nine components are actually linear combinations of just five linearly independent operators. For another example, an antisymmetric tensor satisfying $T_{ij} = -T_{ji}$ contains only the three-dimensional (vector) subspace.

The decomposition of a tensor operator $T_{ij}$ into its irreducible components gives us a preview of how angular momentum quantum numbers are attached to operators. This topic will be developed in more detail in {ref}`ch-wigeck`.

(sec-transfop-9)=

## Energy Eigenstates in Isolated Systems

In this we explore the consequences of rotational invariance for the eigenstates, eigenvalues and degeneracies of a scalar operator. The most important scalar operator in practice is the Hamiltonian for an isolated system, so for concreteness we will speak of such a Hamiltonian, but the following analysis applies to any scalar operator.

Let $H$ be the Hamiltonian for an isolated system, and let $\ES$ be the Hilbert space upon which it acts. Since $H$ is a scalar it commutes with $\Jvec$, and therefore with the commuting operators $J^2$ and $J_3$. Let us denote the simultaneous eigenspaces of $J^2$ and $J_3$ with quantum numbers $j$ and $m$ by $\SS_{jm}$, as illustrated in Fig.~\figr\repsamos.5. It was shown in {ref}`ch-repsamos`{} that for a given system, $j$ takes on certain values that must be either integers or half-integers. For example, in central force motion we have only integer values of $j$ (which is called $\ell$ in that context), while for the $\ironfiftyseven$ nucleus, which is discussed in more detail in the next , we have only half-integer values. For each value of $j$ that occurs there is a collection of $2j+1$ eigenspaces $\SS_{jm}$ of $J^2$ and $J_3$, for $m=-j,\ldots,+j$. These spaces are mapped invertibly into one another by $J_+$ and $J_-$, as illustrated in Fig.~\figr\repsamos.5, and if they are finite-dimensional, then they all have the same dimension. As in {ref}`ch-repsamos`, we write $N_j=\dim\SS_{jj}$, which we call the multiplicity of the given $j$ value.

In {ref}`ch-repsamos`{} we constructed a standard angular momentum basis by picking an arbitrary orthonormal basis in each stretched space $\SS_{jj}$, with the basis vectors labeled by $\gamma$ as in Fig.~\figr\repsamos.5, where $\gamma=1,\ldots,N_j$. We denote these basis vectors in $\SS_{jj}$ by $\ket{\gamma jj}$. Then by applying lowering operators, we construct an orthonormal basis in each of the other $\SS_{jm}$, for $m$ running down to $-j$. In this way we construct a standard angular momentum basis $\ket{\gamma jm}$ on the whole Hilbert space $\ES$. In this construction, it does not matter how the basis $\ket{\gamma jj}$ is chosen in $\SS_{jj}$, as long as it is orthonormal.

Now, however, we have a Hamiltonian, and we would like a simultaneous eigenbasis of $H$, $J^2$ and $J_3$. To construct this we restrict $H$ to $\SS_{jj}$ for some $j$ (see {ref}`sec-hilbert-23` for the concept of the restriction of an operator to a subspace, and how it is used in proving that commuting operators possess a simultaneous eigenbasis). This restricted $H$ is a Hermitian operator on $\SS_{jj}$ so it possesses an eigenbasis on that space.

The spectrum of $H$ on $\SS_{jj}$ can be either discrete, continuous, or mixed (in most problems we will consider in this course it has a continuous spectrum above a threshold energy, and may have discrete bound states below that). Let us focus on the bound states and assume that $H$ possesses at least one bound eigenstate $\ket{\psi}$ on $\SS_{jj}$ with corresponding eigenvalue $E$. Then $\ket{\psi}$ satisfies

:::{math}
:label: eq-transfop-37
J^2\ket{\psi}=j(j+1)\hbar^2\,\ket{\psi}, \qquad J_3\ket{\psi}= j\hbar\,\ket{\psi},\qquad H\ket{\psi} = E\ket{\psi}.
:::

Now by applying a lowering operator $J_-$ we find

:::{math}
:label: eq-transfop-38
J_-H\ket{\psi}=HJ_-\ket{\psi} = EJ_-\ket{\psi},
:::

so that $J_-\ket{\psi}$ is an eigenstate of $H$, lying in the space $\SS_{j,j-1}$, with the same eigenvalue $E$ as $\ket{\psi}\in \SS_{jj}$. Continuing to apply lowering operators, we generate a set of $2j+1$ linearly independent eigenstates of $H$ with the same eigenvalue $E$, that is, $E$ is independent of the quantum number $m$. These states span an irreducible, invariant subspace of $\ES$.

There may be other irreducible subspaces with the same energy. This can occur in two ways. It could happen that there is another energy eigenstate in $\SS_{jj}$, linearly independent of $\ket{\psi}$, with the same energy $E$. That is, it is possible that $E$ is a degenerate eigenvalue of $H$ restricted to $\SS_{jj}$. In general, every discrete eigenvalue $E$ of $H$ restricted to $\SS_{jj}$ corresponds to an eigenspace, a subspace of $\SS_{jj}$ that may be multidimensional. Choosing an orthonormal basis in this subspace and applying lowering operators, we obtain a set of orthogonal, irreducible subspaces of the same value of $j$, each with $2j+1$ dimensions and all having the same energy.

It could also happen that there is another bound energy eigenstate, in a different space $\SS_{j'j'}$ for $j'\ne j$, with the same energy $E$ as $\ket{\psi}\in\SS_{jj}$. This would be a degeneracy of $H$ that crosses $j$ values. If such a degeneracy exists, then we have at least two irreducible subspaces of the same energy, one of dimension $2j+1$ and the other of dimension $2j'+1$. In other words, degeneracies can occur either within a given $j$ value or across $j$ values.

These facts that we have accumulated can be summarized by a theorem:

:::{admonition} Theorem
:class: theorem
:label: thm-transfop-1

The discrete energy eigenspaces of an isolated system consist of one or more invariant, irreducible subspaces under rotations, each associated with a definite $j$ value. The different irreducible subspaces can be chosen to be orthogonal.
:::


Let us look at two examples of how this theorem works out in practice, the first a simple one with a small number of degrees of freedom that is exactly solvable, and the other a complicated one with a large number of degrees of freedom, in which all we know about the Hamiltonian is that it is invariant under rotations.

(sec-transfop-10)=

## Example: Central Force Motion

For the simple example we take the case of central force motion, for which we use the notation $\Lvec$, $\ell$ etc.{} instead of $\Jvec$, $j$ etc.

In central force motion the stretched subspace $\SS_{\ell\ell}$ consists of wave functions $R(r)Y_{\ell\ell}(\theta,\phi)$, where $R(r)$ is any radial wave function. To find the energy eigenstates in this stretched subspace we solve the radial Schr\"odinger equation for the given $\ell$ value, which produces in general a continuous and a discrete spectrum. We assume there is a discrete spectrum for the given $\ell$ value and denote the energy eigenvalues and corresponding radial wave functions by $E_{n\ell}$ and $R_{n\ell}(r)$, as in {ref}`ch-cenforce`. By applying lowering operators to the wave function $R_{n\ell}(r)\,Y_{\ell\ell}(\theta,\phi)$, we obtain an irreducible subspace of degenerate energy eigenfunctions, spanned by $\{R_{n\ell}(r)\, Y_{\ell m}(\theta,\phi), m=+\ell, \ldots, -\ell\}$.

Now we consider degeneracies. Is it possible, for a given value of $\ell$ in a central force problem, that a bound energy eigenvalue can be degenerate? That is, can there be more than one linearly independent bound energy eigenstate of a given energy in $\SS_{\ell\ell}$? As discussed in {ref}`sec-cenforce-4`, the answer is no, the boundary conditions on the radial wave functions guarantee that there can be no degeneracy of this type. In central force problems, we do not have degeneracies within a given $\ell$ value.

Then is it possible that there is a degeneracy between different values of $\ell$? Again, as discussed in {ref}`ch-cenforce`, the answer is that in general it is not very likely, since the different radial equations for different values of $\ell$ are effectively different Schr\"odinger equations whose centrifugal potentials are different.

The fact is that systematic degeneracies require a symmetry. We are already taking into account the $SO(3)$ symmetry of proper rotations, which explains the degeneracy in the magnetic quantum number $m$, so any additional degeneracy will require a larger symmetry group than $SO(3)$. In the absence of such extra symmetry, degeneracies between different $\ell$ values can occur only by “accident,” that is, by fine tuning parameters in a Hamiltonian to force a degeneracy to happen. This is not likely in most practical situations. Therefore in central force problems we do not normally expect degeneracies that cross subspaces of different values of $\ell$.

As explained in {ref}`ch-hydrogen`, however, the electrostatic model of hydrogen is a notable exception, due to the symmetry group $SO(4)$ possessed by this model, which is larger than the rotation group $SO(3)$. The extra symmetry in this model of hydrogen explains why the energy levels $E_n=-1/2n^2$ (in the right units) are the same across the angular momentum values $\ell=0,\ldots,n-1$. The isotropic harmonic oscillator in two or more dimensions is another example of a system with extra degeneracy; such oscillators are approximate models for certain types of molecular vibrations.

For a more complicated example of how Theorem~{ref}`thm-transfop-1` works out in practice we examine some energy levels of the nucleus $\ironfiftyseven$, which is important in the M\"ossbauer effect. We use the opportunity to digress into some of the interesting physics connected with this effect. We begin with a general discussion of aspects of the emission and absorption of photons by quantum systems.

(sec-transfop-11)=

## Emission and Absorption of Photons

When an atom, nucleus or other quantum system is in an excited state $B$ and emits a photon while dropping into the ground state $A$,

:::{math}
:label: eq-transfop-39
B\to A+\gamma,
:::

then a simple description of the process says that the energy of the photon is given by

:::{math}
:label: eq-transfop-40
E_\gamma=E_B-E_A,
:::

where $E_B$ and $E_A$ are the energies of the states $B$ and $A$. If now there is another atom, nucleus or other system of the same type nearby in its ground state $A$, then it would appear that that photon has exactly the right energy to induce the inverse reaction,

:::{math}
:label: eq-transfop-41
A+\gamma \to B,
:::

thereby lifting the second system into the excited state $B$.

Does this mean, for example, that when an atom in a gas emits a photon that the photon only travels as far as the nearest neighboring atom before being absorbed again? No, because there are several effects that complicate the basic picture just presented, modifying the energy $E_\gamma$ of the photon so that is it not exactly given by {eq}`eq-transfop-40`. These include the natural line width of the transition $B\to A$; Doppler shifts; recoil; and, in the case of nuclei, what are called chemical shifts.

In quantum mechanics the energy of a system is only precisely defined in a process that takes place over an infinite amount of time. The excited state $B$ of our system is unstable with some lifetime $\tau$, so its energy $E_B$ is only defined to within an uncertainty of order $\Delta E_B = \hbar/\tau$. Assuming $A$ is the ground state, it is stable and can exist over an infinite amount of time, so there is no uncertainty in its energy. Overall, the uncertainty in the energy $E_B$ creates uncertainty of order $\hbar/\tau$ to the energy of the photon $E_\gamma$ emitted in the process {eq}`eq-transfop-39`. This can be seen experimentally; if all other sources of broadening of the spectral line are eliminated, then the energy of photons emitted in an atomic or nuclear transition does not have a definite value, but rather there is a spread of order $\Delta E=\hbar/\tau$ about the nominal value $E_B-E_A$. This spread is called the *natural line width* of the spectral line. The natural line width of spectral lines is examined in some detail in {ref}`ch-nlw`.

Similarly, if a photon of energy $E_\gamma$ encounters a quantum system of the same type at rest in its ground state $A$, then if $E_\gamma$ is roughly within the range $\Delta E=\hbar/\tau$ about the nominal energy $E_B-E_A$ it will be able to lift the second system into the excited state $B$, that is, the inverse reaction {eq}`eq-transfop-41` will take place.

On the other hand, if the emitting atom, nucleus or other quantum system is in a state of motion, then the frequency $\omega_\gamma=E_\gamma/\hbar$ of the emitted photon will be Doppler shifted and may no longer be within the resonance needed to raise another such system into its excited state. Writing simply $E$ for the nominal energy $E_B-E_A$ of the photon, the velocity $v$ needed to shift the photon out of resonance is given by

:::{math}
:label: eq-transfop-42
{v\over c} = {\Delta E\over E} = {\hbar\over E\tau}.
:::

Whether or not the photon is shifted out of resonance depends on the velocity and other parameters, but in many practical circumstances one will find that thermal velocities do exceed the value given by {eq}`eq-transfop-42`. A similar logic applies in case the receiving system is in a state of motion (or both, as would be the case of a gas).

Even if the emitting atom or nucleus or other system is at rest, the energy $E_\gamma$ is not given exactly by {eq}`eq-transfop-40` because of the recoil of the emitting system when the photon is emitted. The photon has energy $E=\hbar\omega$ and momentum $\pvec=\hbar\kvec$ where $\omega =c|\kvec|$, so by conservation of momentum the emitting system suffers a recoil and has momentum $m\vvec=-\hbar\kvec$ after the photon of frequency $\omega$ is emitted, where $m$ is the mass of the emitting system. Thus {eq}`eq-transfop-40` should be replaced by

:::{math}
:label: eq-transfop-43
E_\gamma + {1\over2}mv^2 = E_B-E_A,
:::

where $\vvec$ is the recoil velocity. Some of the available energy goes into kinetic energy of the recoiling system, and the energy $E_\gamma$ of the emitted photon is actually less than the nominal value {eq}`eq-transfop-40`. Again, whether this recoil shift is greater or less than the natural line width depends on the parameters of the problem.

(sec-transfop-12)=

## The $\ironfiftyseven$ Nucleus and the M\"ossbauer Effect

The M\"ossbauer effect involves a transition $\ironfiftyseven^\cc \to \ironfiftyseven+\gamma$ between two energy levels of the $\ironfiftyseven$ nucleus, where the simple notation $\ironfiftyseven$ (or $A$) refers to the ground state and $\ironfiftyseven^\cc$ (or $B$) refers to an excited state. These states are illustrated in the energy level diagram for the nucleus given in {ref}`fig-transfop-1`. The photon emitted has energy 14.4~KeV, and the lifetime of the excited state $\ironfiftyseven^\cc$ is $\tau=9.8\times10^{-8}$~sec. From these figures we find $\Delta\omega/\omega = \Delta E/E=4.7\times10^{-13}$, where $E$ and $\omega$ are the energy and frequency of the emitted photon. The spread in the energy is very small compared to the energy. For example, according to {eq}`eq-transfop-42`, to Doppler shift the photon out of resonance it would require a velocity of $v/c=4.7\times10^{-13}$, or $v=0.014 \,cm/sec$.

:::{figure} images/transfop-fig01.png
:label: fig-transfop-1
:width: 80%

Energy level diagram relevant for the M\"ossbauer effect in $\ironfiftyseven$. $\ironfiftyseven$ is the ground state, $\ironfiftyseven^\cc$ is an excited state, and $\ironfiftyseven^{\cc\cc}$ is a more highly excited state. Principal transitions via photon emission are shown.
:::

The M\"ossbauer effect makes use of a source containing iron nuclei in the excited state $\ironfiftyseven^*$, which emits photons, and a receiver containing iron nuclei in the ground state which may absorb them by being lifted into the excited state $\ironfiftyseven^\cc$ via the reverse reaction. The receiver can be a block of natural iron, which contains the isotope $\ironfiftyseven$ at the 2\% level, behind which a gamma-ray detector is placed. If the incident photons are within the narrow resonant range of energies, then they will be absorbed by the block of iron, and the detector will detect nothing. But if they are shifted out of resonance, the gamma rays will pass through the block of iron and the detector will detect them. If there is some effect that shifts the frequency of the gamma rays from their nominal energy (for example, the gravitational red shift in the Pound-Rebka experiment), then a compensating Doppler shift can be introduced by giving the source some velocity. By measuring the velocity of the source needed to shift the gamma rays back into resonance, one can measure the shift caused by the effect in question.

However, plugging in the numbers shows that the recoil shift described by {eq}`eq-transfop-43`, where $m$ is the mass of an iron nucleus, is much greater than the natural line width, so the recoil would seem to spoil the whole idea. But the iron nucleus is not free, rather it is part of a crystal lattice, whose vibrations are described by a large number of harmonic oscillators, the normal modes of the lattice. (See the discussion in {ref}`sec-harmosc-2`.) Thus the recoil kinetic energy $E=(1/2)mv^2$ in {eq}`eq-transfop-43` is not free to take on any value, rather it must be some multiple of $\hbar\omega_\ell$, where $\omega_\ell$ is the frequency of a normal mode of the lattice. That is, when the photon is emitted by the nucleus, some number of phonons are also emitted into the lattice, representing the recoil energy. Note that $\omega_\ell$ is the frequency of a sound wave in the lattice, which is much less than the frequency of the emitted gamma ray.

:::{figure} images/transfop-fig02.png
:label: fig-transfop-2
:width: 80%

A one dimensional model of an iron atom coupled to a normal mode of the lattice. The mass of the iron atom is $m$, the mass of the crystal is $M$. The iron atom emits a photon of energy $\hbar\omega$ and suffers a recoil (an impulse) as a result.
:::

To model this situation in the simplest possible way, let us imagine an iron atom connected to a spring, forming a one-dimensional harmonic oscillator, as illustrated in {ref}`fig-transfop-2`. In the figure $m$ is the mass of the iron atom while $M$ is the mass of the crystal lattice to which it is coupled. When the atom emits a photon it suffers an an impulse, that is, a change $\Delta p$ in its momentum. The emission takes place over a short time compared to the frequency of the harmonic oscillator (a normal mode of the lattice), so the position of the iron atom does not change much during the emission process. Classically we can model the impulse by the map,

:::{math}
:label: eq-transfop-44
x\mapsto x, \qquad p\mapsto p+\Delta p.
:::

To model the effect of the recoil in quantum mechanics, we use the momentum displacement operator $S(b)$ introduced in {ref}`ch-harmosc`{} [see {eq}`eq-harmosc-64`--{eq}`eq-harmosc-66`]. That is, if $\ket{\psi}$ is the state of the oscillator before the photon is emitted, then the state after the emission is

:::{math}
:label: eq-transfop-45
\ket{\psi'}=e^{i\Delta p x/\hbar}\ket{\psi}.
:::

The final state can be expanded in energy eigenstates,

:::{math}
:label: eq-transfop-46
\ket{\psi'}=\sum_n c_n\ket{n},
:::

so that the probability of finding the oscillator in state $n$ after the photon has been emitted is $|c_n|^2$. In particular, if the initial state of the oscillator $\ket{\psi}=\ket{n_i}$ is an energy eigenstate, then the probability $|c_n|^2$ is the probability to make a transition $n_i \to n$ as a result of the recoil. As we say, $n-n_i$ phonons are emitted. See Prob. {ref}`prob-harmosc-4`.

In fact, there is a certain probability that no phonons are emitted at all, that is $n=n_i$ and the oscillator remains in the initial state. Because of quantum mechanics, the recoil energy cannot take on any value, but rather is quantized, and the value zero is allowed. What makes the $\ironfiftyseven$ nucleus attractive for the M\"ossbauer effect is that it has a reasonable probability for this *recoilless emission*.

Of course there is not only a recoil energy but also a recoil momentum. In the M\"ossbauer effect, recoilless emission does not violate conservation of momentum because the entire crystal lattice, with an effectively infinite mass $M$ (as in the figure) takes up the recoil momentum.

The excited state $\ironfiftyseven^\cc$ has only a short lifetime but in practice a population of these excited states is maintained in the source as a part of the decay chain of $\cobaltfiftyseven$, as shown in {ref}`fig-transfop-1`. $\cobaltfiftyseven$ has a lifetime of 271 days, which is long enough to make it practical to use it as a source of $\ironfiftyseven^\cc$ in a real experiment. As shown in the figure, $\cobaltfiftyseven$ transforms into an excited state $\ironfiftyseven^{\cc\cc}$ by electron capture, after which $\ironfiftyseven^{\cc\cc}$ decays by the emission of a photon into $\ironfiftyseven^\cc$, which is the source of the photons of interest in the M\"ossbauer effect.

M\"ossbauer was awarded the Nobel Prize in 1961 for his discovery of recoilless emission of gamma ray photons and some of its applications. A notable early application was the Pound-Rebka experiment, carried out in 1959, in which the M\"ossbauer effect was used to make the first measurement of the gravitational red shift. This is the red shift photons experience when climbing in a gravitational field, in accordance with the 1911 prediction of Einstein. The gravitational red shift is one of the physical cornerstones of general relativity.

(sec-transfop-13)=

## Energy levels in $\ironfiftyseven$

To return to the subject of Hamiltonians and their energy levels in isolated systems, let us draw attention to the three levels $\ironfiftyseven$, $\ironfiftyseven^\cc$ and $\ironfiftyseven^{\cc\cc}$, in {ref}`fig-transfop-1`. These are energy levels of the Hamiltonian for the $\ironfiftyseven$ nucleus, and, according to Theorem~{ref}`thm-transfop-1`, each must consist of one or more irreducible subspaces under rotations. In fact, each of them consists of precisely one such irreducible subspace, with a definite $j$ value, which is indicated in the figure ($\frac{1}{2}$ for the ground state $\ironfiftyseven$, and $\frac{3}{2}$ and $\frac{5}{2}$ for the two excited states $\ironfiftyseven^\cc$ and $\ironfiftyseven^{\cc\cc}$, respectively). Also indicated are the parities of these states (all three have odd parity). The parity of energy eigenstates of isolated systems is discussed in {ref}`sec-parity-8`.

A model for the Hamiltonian of the $\ironfiftyseven$ nucleus views it as a 57-particle system, that is, with 26 protons and 31 neutrons. The Hamiltonian is some function of the positions, momenta and spins of the particles,

:::{math}
:label: eq-transfop-47
H=H(\xvec_\alpha,\pvec_\alpha,\Svec_\alpha),
:::

where $\alpha=1,\ldots,57$. In this model the total angular momentum of the system is the sum of the orbital and spin angular momenta of the nucleons,

:::{math}
:label: eq-transfop-48
\Jvec=\sum_{\alpha=1}^{57} \xvec_\alpha \cross \pvec_\alpha + \Svec_\alpha,
:::

and the “spins” of the various nuclear states shown in {ref}`fig-transfop-1` are actually the quantum numbers of $J^2$ (that is, we call $\Jvec$ the “spin” and use the notation $\Svec$ etc.\null{} for it). For example, we say that the ground state $\ironfiftyseven$ has spin $s=\frac{1}{2}$.

This model is more or less crude, due to the fact that protons and neutrons are composite particles, each made up of three quarks, which interact with the quark and gluon fields via the strong interactions. For our purposes the only thing that matters is that rotations act upon the state space of the system by means of unitary operators, and that these commute with the Hamiltonian. The model {eq}`eq-transfop-47` at least gives us something concrete to think about.

Each nuclear energy eigenstate consists of a single irreducible subspace under rotations for the same reasons discussed in connection with central force motion in \secrtransfop-9. That is, extra degeneracy requires extra symmetry or else an unlikely accident, and neither of these is to be expected in nuclei. Therefore each energy level is characterized by a unique angular momentum value, as indicated in the figure.

We can summarize these accumulated facts by stating an addendum to Theorem~{ref}`thm-transfop-1`.

**Addendum to Theorem 1.**{\sl{} With a few exceptions, notably the electrostatic model of hydrogen, the bound state energy eigenspaces of isolated systems consist of a single invariant, irreducible subspace under rotations. Thus, the energy eigenvalues are characterized by an angular momentum quantum number, which is variously denoted $\ell$, $s$, $j$, etc, depending on the system.}

We can now understand why the Hilbert space for spins in magnetic fields consists of a single irreducible subspace under rotations for a large class of particles, a question that was raised in {ref}`ch-spinmagf`. For example, if we place the $\ironfiftyseven$ nucleus in a magnetic field that is strong by laboratory standards, say, 10T, then the energy splitting between the two magnetic substates $m=\pm\frac{1}{2}$ will be of the order of 100~MHz in frequency units, or about $4\times10^{-7}eV$, or roughly $3\times10^{-11}$ times smaller than the energy separation from the first excited state $\ironfiftyseven^\cc$. Therefore it is an excellent approximation to ignore the state $\ironfiftyseven^\cc$ and all other excited states of the $\ironfiftyseven$ nucleus, and to treat the Hilbert space of the nucleus as if it were a single irreducible subspace with $s=\frac{1}{2}$, that is, the ground eigenspace. In other words, in the case of nuclei, the $2s+1$-dimensional Hilbert space used in our study of spins in magnetic fields in {ref}`ch-spinmagf`{} is actually a subspace of a larger Hilbert space. It is, in fact, an energy eigenspace of an isolated system. This in turn explains why the magnetic moment is proportional to the spin [see Prob. {ref}`prob-wigeck-2`(a)].

\problems

(prob-transfop-1)=

**Problem \prbdtransfop-1..** 

The gravitational red shift is a prediction of general relativity, but the basic physics behind it can be understood in elementary terms. In the Pound-Rebka experiment, photons were launched upward from the ground, just outside a building at Harvard University. These photons were then received by a detector just outside the window of an upper floor of the building, approximately 20~meters above the ground.

Suppose at the very moment a photon is released at the ground, a physicist with a detector in hand jumps out of the upper storey window. As the photon is climbing upward in the earth's gravitational field, suffering a red shift in the process, the physicist is falling, accelerating downward. At a certain point the detector captures the photon and the physicist measures its frequency. This frequency is blue shifted compared to what it would be if the physicist had just held the detector out the window, instead of jumping, because of the Doppler shift due to the downward motion of the detector.

It turns out that the gravitational red shift and the blue shift due to the falling detector (cum physicist) exactly cancel. Thus, the physicist finds a measured frequency of the photon exactly equal to the frequency it had when emitted at ground level. You can use this fact to calculate the gravitational red shift as seen by a detector that is just held out the window, not falling.

This situation is similar to that illustrated in the “shoot the monkey” demonstration used in elementary physics classes, except that instead of an arrow shot at the monkey particles of light are used. The basic physical reasoning used here is close to that employed by Einstein in his 1911 paper which first predicted the gravitational red shift.

\problempart{(a)} If an atom is free (not a part of a crystal lattice or otherwise bound to anything else), then it suffers some recoil on emitting a photon, which produces a shift $\Delta\omega$ in the frequency of the emitted photon. In the case of the 14.4~KeV photon emitted by the ${}^{57}Fe$ nucleus, calculate the fractional shift $\Delta\omega/\omega$ due to this recoil and compare to the natural line width.

\problempart{(b)} If the ${}^{57}Fe$ atom is free-floating in a gas at 300~K, calculate the average $\Delta\omega/\omega$ due to the Doppler shift due to the thermal motion of the atom.

\problempart{(c)} Calculate the $\Delta\omega/\omega$ for the gravitational red shift of the same photon climbing (as in the Pound-Rebka experiment) about 20 meters in the earth's gravitational field, and compare to the $\Delta\omega/\omega$ due to the natural line width. You will see that the experiment was a delicate one that required careful measurement and attention to systematic errors.

(prob-transfop-2)=

**Problem \prbdtransfop-2.} Consider a vector operator $\Vvec$ and a tensor operator $T_{ij.** 

\problempart{(a)} Show that if one component of }$\Vvec$ vanishes, then they all do.

\problempart{(b)} Is this true for a tensor operator $T_{ij}$?
