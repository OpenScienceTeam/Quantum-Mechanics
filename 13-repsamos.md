---
title: "13. Representations of the Angular Momentum Operators and Rotations"
---
(ch-repsamos)=

# 13. Representations of the Angular Momentum Operators and Rotations

(sec-repsamos-1)=

## Introduction

In {ref}`ch-spinrot`\ we introduced the concept of rotation operators acting on the Hilbert space of some quantum mechanical system, and set down postulates [{eq}`eq-spinrot-2`--{eq}`eq-spinrot-4`] that those operators should satisfy. From these we defined the angular momentum operators $\Jvec$ [in {eq}`eq-spinrot-11`] and showed that the multiplication law for rotations implies that the components of $\Jvec$ satisfy the commutation relations {eq}`eq-spinrot-24`. Finally, we examined the case of spin-$\frac{1}{2}$ systems, for which $\Jvec=(\hbar/2)\sigmavec$, finding a double-valued representation $U=U(\Rmat)$ of the classical rotations by unitary operators, or, better, a single-valued representation of spin rotations by the classical rotations, $\Rmat=\Rmat(U)$.

In these notes we generalize the treatment of rotations of spin-$\frac{1}{2}$ systems, which was presented in {ref}`ch-spinrot`, to an arbitrary quantum mechanical system. We assume that rotation operators are defined on the Hilbert space $\ES$ of our system. In practice this includes almost any system one can think of. The generators of the rotations are the components of the angular momentum $\Jvec$, a vector of Hermitian operators that satisfy the commutation relations

:::{math}
:label: eq-repsamos-1
[J_i, J_j] = i\hbar \, \epsilon_{ijk} \, J_k.
:::

In terms of these, the rotation operators in axis-angle form are given by

:::{math}
:label: eq-repsamos-2
U({\hat{\mathbf{n}}},\theta) = \exp\Bigl[ -{i\over\hbar} \theta ({\hat{\mathbf{n}}} \cdot\Jvec) \Bigr].
:::

Conversely, the angular momentum operators are given in terms of the rotation operators by

:::{math}
:label: eq-repsamos-3
J_i = i\hbar \Bigl.\frac{\partial U(\thetavec)}{\partial \theta_i} \Bigr|_{\thetavec=0},
:::

where in comparison to {eq}`eq-repsamos-2` we have set $\thetavec=\theta{\hat{\mathbf{n}}}$. Knowledge of the rotation operators implies knowledge of the angular momentum, and vice versa.

In general, symmetries impose a geometrical structure on the Hilbert space of a quantum system. That is, they cause the Hilbert space to be broken up into a family of orthogonal subspaces, each of which contains states that transform in a certain way under the symmetry operations. For example, parity in one-dimensional wave mechanics causes the Hilbert space of wave functions to decompose into two orthogonal subspaces, containing the wave functions that are even or odd under parity. By defining a set of orthonormal basis vectors in each of the subspaces of a certain symmetry class we obtain a so-called *symmetry adapted basis* that is especially convenient for studying the symmetry properties of the system and for numerical work. If the Hamiltonian commutes with the symmetry in question, then it is possible to choose a symmetry adapted basis that is also an energy eigenbasis, and these are especially convenient for studying the system.

We will see that rotations and the associated the angular momentum operators can be used to construct a symmetry-adapted basis on the Hilbert space, what we will call a *standard angular momentum basis*. This basis will lead to a decomposition of our Hilbert space into an orthogonal set of *invariant, irreducible subspaces*, the vectors of which transform in an especially simple manner under rotations.

Although we will speak in these notes of a Hilbert space which is the ket space or state space of a quantum mechanical system, and we will use the Dirac notation for the (ket) vectors of this space, there are a wide variety of other vector spaces to which the same analysis applies. These include other types of ket spaces, such as subspaces of a given ket space, or tensor products of ket spaces. They also include spaces that are not ket spaces at all, such as vector spaces of operators (which we will take up in {ref}`ch-wigeck`), or ordinary, three-dimensional, physical space (certainly a space upon which rotations act), or spaces of classical fields (for example, electric and magnetic), in which the standard angular momentum basis is related to the multipole expansion of those fields. Thus, the treatment of this set of notes is actually quite general.

(sec-repsamos-2)=

## The spectrum of $J^2$ and $J_3$

We will now explore the consequences of the angular momentum commutation relations {eq}`eq-repsamos-1` for the spectrum of various angular momentum operators. It is rather amazing how much follows from the commutation relations alone. We use a variation of Dirac's algebraic method that was applied in {ref}`sec-harmosc-4` to the harmonic oscillator.

We begin by constructing the nonnegative definite operator $J^2$,

:::{math}
:label: eq-repsamos-4
J^2 = J_1^2 + J_2^2 + J_3^2,
:::

which, as an easy calculation shows, commutes with all three components of $\Jvec$,

:::{math}
:label: eq-repsamos-5
[J^2,\Jvec] = 0.
:::

Since $J^2$ commutes with $\Jvec$, it commutes also with any function of $\Jvec$. Let $X(\Jvec)$ be such a function, for example, $X$ could be $J_1$, $J_2$, $J_3$, $J_\pm$, $J^2$, or the rotation operators $\exp(-i\theta{\hat{\mathbf{n}}}\cdot\Jvec/\hbar)$. Then

:::{math}
:label: eq-repsamos-6
[J^2,X(\Jvec)]=0.
:::

An operator such as $J^2$ that commutes with all the generators of a group is called a *Casimir operator*.

Since $J^2$ and $\Jvec$ commute, we can construct simultaneous eigenkets of $J^2$ and any one of the components of $\Jvec$. However, since these components do not commute with each other, we cannot find simultaneous eigenbasis of more than one component of $\Jvec$. By convention we choose the 3-component, and look for simultaneous eigenkets of $J^2$ and $J_3$.

We denote the eigenvalues of $J^2$ and $J_3$ by $a\hbar^2$ and $m\hbar $, respectively, so that $a$ and $m$ are dimensionless. We note that $a$ and $m$ must be real, since $J^2$ and $J_3$ are Hermitian, and that $a\ge0$, since $J^2$ is nonnegative definite.

We will begin by assuming for simplicity that the operators $(J^2,J_3)$ form a complete set of commuting operators by themselves, so that their simultaneous eigenstates $\ket{am}$ are nondegenerate and form a basis in the Hilbert space. Later we will return to what happens when this is not so.

The eigenvalue equations determine the kets $\ket{am}$ to within a normalization and a phase. We assume the kets are normalized, so that the set $\{\ket{am}\}$ forms an orthonormal basis in the Hilbert space,

:::{math}
:label: eq-repsamos-7
\braket{am}{a'm'}=\delta_{aa'}\,\delta_{mm'}.
:::

We assume that some arbitrary (at this point) phase conventions have been chosen for the kets $\ket{am}$. The eigenvalue-eigenket equations are

:::{math}
:label: eq-repsamos-8
\begin{aligned}
J^2 \ket{a m} & = a\hbar^2  \ket{a m}, \\
J_3 \ket{a m} & = m\hbar  \ket{a m}. \\

\end{aligned}
:::

We will be interested in the simultaneous eigenvalues $(m,a)$, which can be represented as “eigenpoints” in the $m$-$a$ plane. At this point all we know is that $a\ge0$, so the eigenpoints must lie in the upper half plane.

To find these eigenvalues we introduce the ladder or raising and lowering operators,

:::{math}
:label: eq-repsamos-9
J_\pm = J_1 \pm iJ_2.
:::

These are Hermitian conjugates of each other,

:::{math}
:label: eq-repsamos-10
(J_{\pm})^\dagger = J_{\mp},
:::

and they satisfy the commutation relations,

:::{math}
:label: eq-repsamos-11
\begin{aligned}
[J_3, J_\pm] &= \pm \hbar J_\pm,
\end{aligned}
:::

:::{math}
:label: eq-repsamos-12
\begin{aligned}
[J^2, J_\pm] &= 0,
\end{aligned}
:::

as well as the relations,

:::{math}
:label: eq-repsamos-13
\begin{aligned}
J_-J_+ &= J^2 - J_3(J_3+\hbar),
\end{aligned}
:::

:::{math}
:label: eq-repsamos-14
\begin{aligned}
J_+J_- &= J^2 - J_3(J_3-\hbar).
\end{aligned}
:::

The operators $J_+J_-$ and $J_-J_+$ are nonnegative definite.

Let us take some normalized eigenket $\ket{am}$ of $J^2$ and $J_3$, for some as yet unknown values of $a$ and $m$, and sandwich it around {eq}`eq-repsamos-13` and {eq}`eq-repsamos-14`. We find

:::{math}
:label: eq-repsamos-15
\begin{aligned}
\matrixelement{am}{J_-J_+}{am} &= \hbar^2 [a-m(m+1)] \ge 0,
\end{aligned}
:::

:::{math}
:label: eq-repsamos-16
\begin{aligned}
\matrixelement{am}{J_+J_-}{am} &= \hbar^2 [a-m(m-1)] \ge 0,
\end{aligned}
:::

where the inequalities follow from the fact that the left hand sides are the squares of ket vectors [see {eq}`eq-hilbert-27`]. Taken together, these imply

:::{math}
:label: eq-repsamos-17
a \ge \max[m(m+1), m(m-1)].
:::

:::{figure} images/repsamos-fig01.png
:label: fig-repsamos-1
:width: 80%

Functions $m(m+1)$ and $m(m-1)$.
:::

:::{figure} images/repsamos-fig02.png
:label: fig-repsamos-2
:width: 80%

Function $\max[m(m+1),m(m-1)]$, with maximum and minimum values of $m$ for a given value of $a$. We define $j=m_max$, which makes $j$ a function of $a$ and vice versa, that is, $a=j(j+1)$.
:::


The functions $m(m\pm1)$ are plotted in {ref}`fig-repsamos-1`, and the maximum of these two functions is plotted in {ref}`fig-repsamos-2`. The maximum function is symmetric about $m=0$, and $\ge0$ everywhere. According to {eq}`eq-repsamos-17`, the eigenpoints $(m,a)$ must lie in the shaded region in {ref}`fig-repsamos-2` or on its boundary.

Let $a$ be an eigenvalue of $J^2$. A value of $a$ is indicated by a horizontal line in {ref}`fig-repsamos-2`, which intersects the boundary of the shaded region in two points. There must be one or more eigenpoints on this line, whose $m$ values lie between certain maximum and minimum values, which are functions of $a$. Let us define

:::{math}
:label: eq-repsamos-18
j=m_max(a),
:::

so that

:::{math}
:label: eq-repsamos-19
m_min(a)=-j,
:::

as shown in {ref}`fig-repsamos-2`. The $(m,a)$ coordinates of the two interpoints are $\bigl(-j,j(j+1)\bigr)$ on the left and $\bigl(j,j(j+1)\bigr)$ on the right, so $j$ is a function of $a$ given by

:::{math}
:label: eq-repsamos-20
a=j(j+1),
:::

with $j\ge0$. Then we have

:::{math}
:label: eq-repsamos-21
-j \le m \le +j.
:::

It turns out to be more convenient to parameterize the eigenvalues and eigenkets of $J^2$ by $j$ instead of $a$, so henceforth let us write $j(j+1)\hbar^2$ for the eigenvalue of $J^2$ instead of $a\hbar^2$, and let us write $\ket{jm}$ instead of $\ket{am}$ for the eigenkets of $J^2$ and $J_3$. Then {eq}`eq-repsamos-8` become

:::{math}
:label: eq-repsamos-22
\begin{aligned}
J^2\ket{jm} &= j(j+1)\hbar^2 \,\ket{jm}, \\
J_3\ket{jm} &= m\hbar \,\ket{jm}, \\

\end{aligned}
:::

and the orthonormality conditions {eq}`eq-repsamos-7` become

:::{math}
:label: eq-repsamos-23
\braket{jm}{j'm'}=\delta_{jj'}\,\delta_{mm'}.
:::

We also rewrite {eq}`eq-repsamos-15` and {eq}`eq-repsamos-16` with this change of notation, noting that the right hand sides can be factored,

:::{math}
:label: eq-repsamos-24
\begin{aligned}
\matrixelement{jm}{J_-J_+}{jm} &= \hbar^2 [j(j+1)-m(m+1)] =\hbar^2 (j-m)(j+m+1) \ge 0,
\end{aligned}
:::

:::{math}
:label: eq-repsamos-25
\begin{aligned}
\matrixelement{jm}{J_+J_-}{jm} &= \hbar^2 [j(j+1)-m(m-1)] =\hbar^2(j+m)(j-m+1) \ge 0.
\end{aligned}
:::

Also let us replace the $m$-$a$ plane with the $m$-$j$ plane, so that {ref}`fig-repsamos-2` becomes {ref}`fig-repsamos-3`.

:::{figure} images/repsamos-fig03.png
:label: fig-repsamos-3
:width: 80%

ure {ref}`fig-repsamos-2` redrawn with $j$ as the vertical coordinate instead of $a$, where $a=j(j+1)$. The bounding lines are now $j=\pm m$, and for a given value of $j$ (the horizontal line) $m$ is bounded by $-j\le m \le +j$.
:::

:::{figure} images/repsamos-fig04.png
:label: fig-repsamos-4
:width: 80%

Spots are shown in $m$-$j$ plane for allowed eigenvalues. Whether a given $j$ value (a horizontal line in the figure) actually occurs depends on the application; but if it does occur, then all $m$-values (the spots along the horizontal line, between $-j$ and $+j$, in integer steps) occur.
:::


The behavior of $J_+$ as a raising operator is indicated by the following theorem.

:::{admonition} Theorem
:class: theorem
:label: thm-repsamos-1

If the state $J_+\ket{jm}$ does not vanish, then it is an eigenstate of $J^2$ and $J_3$ with eigenvalues $j(j+1)\hbar^2$ and $(m+1)\hbar$, respectively.
:::


In this theorem, we assume that $\ket{jm}$ is an eigenket of $J^2$ and $J_z$ with the indicated quantum numbers, and that it is normalized as indicated by {eq}`eq-repsamos-23`, and, in particular, that $\ket{jm}\ne0$. We have to worry about the possibility that $J_+\ket{jm}$ is zero, because zero vectors are not usually considered eigenvectors of anything. The theorem says that $J_+$ does not change the $j$ quantum number but it raises $m$ by one unit. The theorem is easily proved with the help of the commutation relations {eq}`eq-repsamos-11` and {eq}`eq-repsamos-12`,

:::{math}
\begin{aligned}
J^2 \bigl( J_+\ket{jm} \bigr) & = J_+ J^2 \ket{jm} = j(j+1)\hbar^2 \bigl( J_+\ket{jm} \bigr),
\end{aligned}
:::

:::{math}
:label: eq-repsamos-26
\begin{aligned}
J_3 \bigl( J_+\ket{jm} \bigr) &= (J_+J_3 + \hbar J_+)\ket{jm} =(m+1)\hbar \bigl( J_+\ket{jm} \bigr).
\end{aligned}
:::

Similarly, we can show that if the state $J_-\ket{jm}$ does not vanish, then it is an eigenket of $J^2$ and $J_3$ with eigenvalues $j(j+1)\hbar^2$ and $(m-1)\hbar$, respectively. That is, $J_-$ does not change the $j$ quantum number but it lowers $m$ by one unit.

We must worry about the case $J_+\ket{jm}=0$. Since a vector vanishes if and only if its square vanishes, we have $J_+\ket{jm}=0$ if and only if

:::{math}
:label: eq-repsamos-27
\matrixelement{jm}{J_-J_+}{jm}= \hbar^2(j-m)(j+m+1)=0,
:::

where we use {eq}`eq-repsamos-24`. But this holds if and only if either $m=j$ or $m=-j-1$. But $m=-j-1$ is impossible in view of {eq}`eq-repsamos-21`, so we see that

:::{math}
:label: eq-repsamos-28
J_+\ket{jm}=0\quad iff \quad m=j.
:::

Similarly, we find that

:::{math}
:label: eq-repsamos-29
J_-\ket{jm}=0\quad iff\quad m=-j.
:::

From this it immediately follows that

:::{math}
:label: eq-repsamos-30
m=j-n_1,
:::

where $n_1\ge0$ is an integer, for if this were not so, we could successively apply $J_+$ to $\ket{jm}$ (which is nonzero), and generate nonzero kets with successively higher values of $m$ until the rule {eq}`eq-repsamos-21` was violated. Similarly, we show that

:::{math}
:label: eq-repsamos-31
m=-j+n_2,
:::

where $n_2\ge0$ is another integer. But taken together, {eq}`eq-repsamos-30` and {eq}`eq-repsamos-31` imply $2j=n_1+n_2$, that is, $2j$ is a nonnegative integer. Thus, the only values of $j$ allowed by the commutation relations {eq}`eq-repsamos-1` are nonnegative integers or half-integers,

:::{math}
:label: eq-repsamos-32
j\in \{0, \frac{1}{2}, 1, \frac{3}{2}, \ldots\}.
:::

When we say that $j$ belongs to the indicated set of values (integers and half-integers), we mean that the commutation relations alone tell us that $j$ can take on only these values. They do not tell us which of these values actually occur in a specific application.

For example, speaking of the spin of a spin-$\frac{1}{2}$ particle, $j$ (that is, the spin) takes on only the value $j=\frac{1}{2}$. But in a central force problem, in which the energy eigenfunctions are $\psi_{n\ell m}(r,\theta,\phi)$ and $j$ is identified with the orbital angular momentum $\ell$, $j$ (that is, $\ell$) takes on all possible integer values $(0,1,2,\ldots)$ but none of the half-integer values.

But in any application, if some $j$ value does occur, then all $m$ values in the range,

:::{math}
:label: eq-repsamos-33
m=-j, -j+1, \ldots, +j,
:::

also occur, for if any one $m$ value in this list occurs, that is, if a nonzero eigenket $\ket{jm}$ exists, then all other nonzero eigenkets with the same $j$ value but other $m$ values in the range {eq}`eq-repsamos-33` can be generated from the given one by raising and lowering operators. Thus, the eigenvalue $j(j+1)\hbar^2$ of $J^2$ is $(2j+1)$-fold degenerate. The allowed eigenvalues of $J^2$ and $J_3$ are illustrated as spots in the $m$-$j$ plane in {ref}`fig-repsamos-4`.

(sec-repsamos-3)=

## Superselection Rules

The commutation relations {eq}`eq-repsamos-1` alone only tell us that the $j$ values that occur in any application belong to the set {eq}`eq-repsamos-32`, consisting of nonnegative integers and half-integers. It turns out, however, that in physical applications the values of $j$ that occur are either all integers or all half-integers. In nonrelativistic quantum mechanics, this is is because the spins of particles are either integers or half-integers, and orbital angular momenta are always integers. That is, if $\Espace$ is the Hilbert space of a physical system and if rotation operators (and therefore angular momentum operators) are defined on it, then the eigenvalues of $J^2$ that occur in $\Espace$ are given either by integer $j$ or half-integer $j$, never a mixture of the two. This is sometimes stated by saying that there is no physical meaning to linear combinations of states with integer $j$ and half-integer $j$. This type of restriction is called a “superselection rule.”

This superselection rule only applies when the rotations in question represent physical rotations in 3-dimensional space, as discussed in {ref}`ch-classrot`. Sometimes there arise operators of the same mathematical form as physical rotations but without this physical meaning, for example, in the two-dimensional, isotropic harmonic oscillator that forms the basis of Schwinger's treatment of angular momentum theory (see Prob. {ref}`prob-harmosc-2`). In such cases linear combinations of integer and half-integer $j$ can and do occur.

(sec-repsamos-4)=

## Phase Conventions and Matrix Elements of $J_\pm$

Since by assumption the simultaneous eigenkets of $J^2$ and $J_3$ are nondegenerate, the state $J_-\ket{jm}$ must be proportional to $\ket{j,m-1}$,

:::{math}
:label: eq-repsamos-34
J_-\ket{jm}=c_m \ket{j,m-1},
:::

where $c_m$ is a complex number. Squaring both sides and using {eq}`eq-repsamos-25` we obtain

:::{math}
:label: eq-repsamos-35
\matrixelement{jm}{J_+J_-}{jm} = \hbar^2(j+m)(j-m+1) = |c_m|^2,
:::

or,

:::{math}
:label: eq-repsamos-36
J_-\ket{jm}=\hbar e^{i\alpha_m}\, \sqrt{(j+m)(j-m+1)}\,\ket{j,m-1},
:::

where $e^{i\alpha_m}$ is a phase. Let us write out these equations starting with the “stretched state” $m=j$ and lowering $m$ in unit steps,

:::{math}
:label: eq-repsamos-37
\begin{aligned}
J_-\ket{jj} &= \hbar e^{i\alpha_j}\,\sqrt{(2j)(1)}\, \ket{j,j-1}, \\
J_-\ket{j,j-1} &=\hbar e^{i\alpha_{j-1}}\, \sqrt{(2j-1)(2)} \, \ket{j,j-2}, \\
&\vdots \\

\end{aligned}
:::

etc. These show that if we choose the phase of the stretched state $\ket{jj}$ arbitrarily, then we can absorb the phases $e^{i\alpha_m}$ into the phase conventions for the states $\ket{jm}$ for $m<j$, thereby linking the phase conventions of all the states $\ket{jm}$ for fixed $j$ to that of the stretched state $\ket{jj}$. This gets rid of the phase factors, and gives

:::{math}
:label: eq-repsamos-38
J_-\ket{jm} = \hbar \sqrt{(j+m)(j-m+1)}\, \ket{j,m-1}.
:::

Similarly, $J_+\ket{jm}$ must be proportional to $\ket{j,m+1}$,

:::{math}
:label: eq-repsamos-39
J_+\ket{jm} = d_m\,\ket{j,m+1},
:::

where $d_m$ is a complex number. Applying $J_-$ to both sides, on the left we obtain

:::{math}
:label: eq-repsamos-40
J_-J_+\ket{jm} = \hbar^2[j(j+1)-m(m+1)]\ket{jm} = \hbar^2(j-m)(j+m+1)\ket{jm},
:::

where we use {eq}`eq-repsamos-13`, whereas on the right we obtain

:::{math}
:label: eq-repsamos-41
d_m\,J_-\ket{j,m+1} = d_m\hbar\sqrt{(j-m)(j+m+1)}\,\ket{jm},
:::

where we use {eq}`eq-repsamos-38`. This allows us to solve for $d_m$, and altogether we obtain

:::{math}
:label: eq-repsamos-42
J_+\ket{jm}=\hbar \sqrt{(j-m)(j+m+1)}\,\ket{j,m+1}.
:::

These phase conventions cause the matrix elements of $J_\pm$ in the basis $\ket{jm}$ to be real and positive. These phase conventions are standard and convenient in the theory of angular momentum and rotations, but there is no physics in them.

With these phase conventions we can use a little induction to express an arbitrary basis vector $\ket{jm}$ as a lowered version of the stretched state $\ket{jj}$,

:::{math}
:label: eq-repsamos-43
\ket{jm} = \sqrt{\ds{\ds (j+m)! \over \ds (2j)! (j-m)!}} \, \Bigl({J_- \over \hbar}\Bigr)^{j-m} \ket{jj}.
:::

This may be compared to {eq}`eq-harmosc-38` for the harmonic oscillator. The basis $\{\ket{jm}\}$ that we have constructed is what we shall call the *standard angular momentum basis* for the Hilbert space in the case we are considering (where eigenkets $\ket{jm}$ of $J^2$ and $J_3$ are nondegenerate).

(sec-repsamos-5)=

## Matrices in the Standard Angular Momentum Basis

For practical calculations we often require the matrix elements of functions $X(\Jvec)$ of the angular momentum $\Jvec$ in the standard angular momentum basis. Because of the commutator {eq}`eq-repsamos-6`, all these matrices are diagonal in the quantum number $j$. That is, we have

:::{math}
:label: eq-repsamos-44
\begin{aligned}
0&=\matrixelement{jm}{[J^2,X(\Jvec)]}{j'm'} = \matrixelement{jm}{J^2X(\Jvec)-X(\Jvec)J^2}{j'm'} \\
& =[j(j+1)-j'(j'+1)]\matrixelement{jm}{X(\Jvec)}{j'm'}, \\

\end{aligned}
:::

so either $j=j'$ or $\matrixelement{jm}{X(\Jvec)}{j'm'}=0$. Thus we can write

:::{math}
:label: eq-repsamos-45
\matrixelement{jm}{X(\Jvec)}{j'm'} = \delta_{jj'} \, \matrixelement{jm}{X(\Jvec)}{jm'},
:::

in which the $j$ values on the two sides of the last matrix element are the same. As we say, functions of the angular momentum $X(\Jvec)$ do not mix together subspaces with different values of $j$. As a result, the matrices of any operator $X(\Jvec)$ in the standard angular momentum basis are specified by a set of submatrices, one for each $j$ value, whose rows and columns are indexed by $m$ and $m'$ and whose size is $2j+1$.

We can easily give explicit formulas for some of these matrices. The matrices of $J^2$ are especially simple, since the standard angular momentum basis is an eigenbasis of $J^2$,

:::{math}
:label: eq-repsamos-46
\matrixelement{jm}{J^2}{jm'} = j(j+1)\hbar^2 \, \delta_{mm'}.
:::

The matrix of $J^2$ for a given value of $j$ is a multiple of the identity. Similarly, the standard angular momentum basis is also an eigenbasis of $J_3$, so

:::{math}
:label: eq-repsamos-47
\matrixelement{jm}{J_3}{jm'} = m\hbar \, \delta_{mm'}.
:::

The matrix of $J_3$ for a given value of $j$ is diagonal, but it is not a multiple of the identity.

The matrices of $J_+$ and $J_-$ can be obtained from {eq}`eq-repsamos-38` and {eq}`eq-repsamos-42` by multiplying on the left by $\bra{jm'}$ and using the orthonormality of the basis. This gives

:::{math}
:label: eq-repsamos-48a
\begin{aligned}
\matrixelement{jm}{J_+}{jm'} &= \hbar\sqrt{(j+m)(j-m+1)}\, \delta_{m,m'+1},
\end{aligned}
:::

:::{math}
:label: eq-repsamos-48b
\begin{aligned}
\matrixelement{jm}{J_-}{jm'} &=\hbar\sqrt{(j-m)(j+m+1)}\, \delta_{m,m'-1},
\end{aligned}
:::

where we have swapped $m$ and $m'$ in the results. Notice that the matrix for $J_-$ is the transpose of that for $J_+$, since $J_- = (J_+)^\dagger$ and for real matrices the Hermitian conjugate is the same as the transpose. Also, since $J_1$ and $J_2$ can be expressed in terms of $J_\pm$,

:::{math}
:label: eq-repsamos-49
J_1 = {1\over2}(J_+ + J_-), \qquad J_2 = {1\over2i}(J_+ - J_-),
:::

it is easy to write down the matrices for $J_1=J_x$ and $J_2=J_y$. Note that since the matrices of $J_\pm$ are real, by {eq}`eq-repsamos-49` those of $J_1=J_x$ are real and those of $J_2=J_y$ are purely imaginary.

Thus we know the matrix elements of all three components of $\Jvec$ in the standard angular momentum basis. From these one can find the matrix elements of any function of $\Jvec$, such as the rotation operators $U({\hat{\mathbf{n}}},\theta)$. Notice that all these matrices are diagonal in $j$ (the matrix elements are proportional to $\delta_{j'j}$), so the matrix elements themselves depend only on $j$, $m'$ and $m$.

Let us look at some specific examples. For a given operator $X=X(\Jvec)$ we present the matrix with components $X_{mm'}=\matrixelement{jm}{X}{jm'}$, with $m$ labeling the rows and $m'$ labeling the columns, and with magnetic quantum numbers starting with the stretched value $m=j$ and proceeding down to $m=-j$ in integer steps as we move across rows or down columns.

In the case $j=\frac{1}{2}$ the matrices for $J_3$ and $J_+$ are

:::{math}
:label: eq-repsamos-50
\begin{aligned}
J_3= J_z =\hbar\begin{pmatrix}\frac{1}{2} &0\\  0 & -\frac{1}{2}\\\end{pmatrix}= {\hbar\over 2}\sigma_z, \qquad J_+= \hbar \begin{pmatrix}0 &1 \\ 0 & 0 \\\end{pmatrix}.
\end{aligned}

:::

We do not display the matrix for $J_-$ since it is just the transpose of the matrix for $J_+$. But from $J_+$ and $J_-$ we compute the matrices for $J_1$ and $J_2$,

:::{math}
:label: eq-repsamos-51
\begin{aligned}
J_1 =J_x = \hbar\begin{pmatrix}0 & \frac{1}{2}\\  \frac{1}{2} & 0\\\end{pmatrix}={\hbar\over2}\sigma_x, \qquad J_2 = J_y = \hbar\begin{pmatrix}0 & -i/2 \\  i/2 & 0\\\end{pmatrix} = {\hbar\over 2}\sigma_y.
\end{aligned}

:::

We see that when $j=1/2$, $\Jvec=(\hbar/2)\sigmavec$, the same conclusion we reached in {ref}`ch-spinrot`{} (and note that we are confusing an operator with the matrix representing that operator in the standard angular momentum basis).

In the case $j=1$ the matrices for $J_3=J_z$ and $J_+$ are

:::{math}
:label: eq-repsamos-52
\begin{aligned}
J_3=J_z = \hbar \begin{pmatrix}1 &0 &0\\ 0 &0 &0\\ 0 &0 &-1\\\end{pmatrix}, \qquad J_+ = \hbar \begin{pmatrix} 0 &\sqrt{2} &0 \\ 0 &0 &\sqrt{2}\\ 0 &0 &0\\\end{pmatrix},
\end{aligned}

:::

from which we obtain the matrices for $J_1$ and $J_2$,

:::{math}
:label: eq-repsamos-53
\begin{aligned}
J_1=J_x={\hbar\over\sqrt{2}}\begin{pmatrix}0 & 1 & 0\\ 1 & 0 & 1\\ 0 & 1 & 0\\\end{pmatrix}, \qquad J_2=J_y={\hbar\over\sqrt{2}} \begin{pmatrix}0 & -i & 0\\ i & 0 & -i\\ 0 & i & 0\\\end{pmatrix}.
\end{aligned}

:::

In these equations we see the generalization of the Pauli matrices to the case $j=1$.

In the case $j=\frac{3}{2}$, the matrices for $J_3=J_z$ and $J_+$ are

:::{math}
:label: eq-repsamos-54
\begin{aligned}
J_3=J_z= \hbar \begin{pmatrix}\frac{3}{2} &0 &0 &0\\  0 &\frac{1}{2} &0 &0\\  0 &0 &-\frac{1}{2} &0\\  0 &0 &0 &-\frac{3}{2}\\\end{pmatrix}, \qquad J_+ = \hbar \begin{pmatrix}0 &\sqrt{3} &0 &0\\ 0 &0 &2 &0\\ 0 &0 &0 &\sqrt{3}\\ 0 &0 &0 &0\\\end{pmatrix}.
\end{aligned}

:::

We omit the matrices for $J_1=J_x$ and $J_2=J_y$ in this case, but they are easily computed.

A case not to be neglected is $j=0$, for which $m$ can take on only one value, $m=0$, so that all matrices are $1\times1$. The matrices are

:::{math}
:label: eq-repsamos-55
J_+=J_-=J_1=J_2=J_3=(0).
:::

The angular momentum operator $\Jvec$ is zero on a subspace in which $j=0$.

(sec-repsamos-6)=

## Rotation Matrices

The matrices of the rotation operators are especially important, and we give them a special notation. If $U$ is a rotation operator, we define

:::{math}
:label: eq-repsamos-56
D^j_{m'm}(U) = \matrixelement{jm'}{U}{jm}.
:::

The symbol $D$ is for German *Drehung*, which means, “rotation.” These matrices are also sometimes referred to as “Wigner $D$-matrices.”

The rotation operator $U$ can be parameterized in a variety of ways, for example, in axis-angle form $U(\theta,{\hat{\mathbf{n}}})$, in Euler angle form $U(\alpha,\beta,\gamma)$ or as a function of a spatial rotation, $U(\Rmat)$. In these cases we can write $D^j_{mm'}(\theta,{\hat{\mathbf{n}}})$, $D^j_{mm'}(\alpha,\beta,\gamma)$ or $D^j_{mm'}(\Rmat)$ for the corresponding rotation matrix. We can also write $D^j_{mm'}(U)$, to indicate the dependence of the rotation matrix on the unitary operator. Note that if $U$ is a double-valued function of $\Rmat$, then so is the matrix $D^j_{mm'}(\Rmat)$.

The $D$-matrices appear when we rotate a basis vector of the standard angular momentum basis. By inserting a resolution of the identity we have

:::{math}
:label: eq-repsamos-57
U\ket{jm} = \sum_{j'm'} \ket{j'm'} \matrixelement{j'm'}{U}{jm}.
:::

But since the final matrix element is proportional to $\delta_{jj'}$ [see {eq}`eq-repsamos-45`], the sum reduces to just one over $m'$,

:::{math}
:label: eq-repsamos-58
U\ket{jm} = \sum_{m'} \ket{jm'} D^j_{m'm}(U).
:::

When we apply a rotation to a basis vector $\ket{jm}$, we obtain a linear combination of basis vectors with the same value of $j$, and the $D$-matrices give the expansion coefficients. There is no mixing of different $j$ values.

In the case $j=0$ the matrices for all three components of $\Jvec$ are just $(0)$, so the matrix for the rotation operator is

:::{math}
:label: eq-repsamos-59
D^0_{mm'}(U) = (1).
:::

This means that a state with $j=0$ is invariant under rotations, since multiplying by 1 does nothing. An example is the ground state of hydrogen, in which wave function $\psi_{100}(\xvec)$ is rotationally invariant (the angular dependence is given by $Y_{00}(\theta,\phi)$, which is a constant, independent of angle). If we include the spins of the electron and proton in our description of the hydrogen atom, the ground state is still a state of $j=0$ (the spin singlet state, although the quantum number is usually called $f$ instead of $j$. See {ref}`ch-hyperfine`).

In the case $j=1/2$, we have already worked out the matrices for the rotation operators in axis-angle form,

:::{math}
:label: eq-repsamos-60
D^{1/2}_{mm'}(\theta,{\hat{\mathbf{n}}}) = [\cos(\theta/2) -i({\hat{\mathbf{n}}}\cdot\sigmavec)\sin(\theta/2)]_{mm'}
:::

[see {eq}`eq-spinrot-27` and Prob. {ref}`prob-hilbert-1`(b)]. Rotation matrices in axis-angle form for higher values of $j$ can also be worked out.

The rotation matrix $D^j_{mm'}({\hat{\mathbf{n}}},\theta)$ is especially simple in the case that ${\hat{\mathbf{n}}}={\hat{\mathbf{z}}}$, since in that case the rotation matrix, being the exponential of the diagonal matrix {eq}`eq-repsamos-47`, is itself diagonal. Thus we have

:::{math}
:label: eq-repsamos-61
D^j_{mm'}({\hat{\mathbf{z}}},\theta) = e^{-im\theta} \, \delta_{mm'}.
:::

This particular rotation leads to an important conclusion. When $j$ is half-integral, then so is $m$, and we find

:::{math}
:label: eq-repsamos-62
D^j_{mm'}({\hat{\mathbf{z}}},2\pi) = -\delta_{mm'}.
:::

Thus, rotating any system of half-integer angular momentum by an angle of $2\pi$ does not return it to its original value, but rather multiplies the state by $-1$. This actually applies to any axis, not just the $z$-axis. This generalizes what we saw earlier for the special case $j=\frac{1}{2}$. For all half-integer values of $j$ the representation of spatial rotations $\Rmat$ by quantum rotations is double-valued, exactly as for spin-$\frac{1}{2}$ systems. In this case the ranges on the Euler angles are modified, as seen in {eq}`eq-spinrot-54`. However, in the case of integer $j$, we have

:::{math}
:label: eq-repsamos-63
D^j_{mm'}({\hat{\mathbf{z}}},2\pi)= + \delta_{mm'},
:::

which actually applies to any axis (not just ${\hat{\mathbf{z}}}$). For integer $j$ the quantum rotations form a single-valued representation of the spatial rotations $\Rmat$.

Although the $D$-matrices form a single- or double-valued representation of $SO(3)$, depending on the value of $j$, it can be said that they always form a single-valued representation of $SU(2)$, the group of spin-$\frac{1}{2}$ rotations, while $SU(2)$ itself forms a double-valued representation of $SO(3)$. Actually, it is better to say that $SO(3)$ is a single-valued representation of $SU(2)$, which points to $SU(2)$ as the fundamental group of rotations in quantum mechanics.

(sec-repsamos-7)=

## Euler Angles and Reduced Rotation Matrices

In many applications the Euler angle parameterization of the rotation matrices is convenient. We write

:::{math}
:label: eq-repsamos-64
U(\alpha,\beta,\gamma) = U({\hat{\mathbf{z}}},\alpha)U({\hat{\mathbf{y}}},\beta) U({\hat{\mathbf{z}}},\gamma),
:::

which is the same as {eq}`eq-spinrot-53` except here generalized to arbitrary values of $j$. By taking matrix elements and introducing resolutions of the identity we obtain

:::{math}
:label: eq-repsamos-65
\matrixelement{jm}{U(\alpha,\beta,\gamma)}{jm'}= \sum_{m_1m_2} \matrixelement{jm}{U({\hat{\mathbf{z}}},\alpha)}{jm_1} \matrixelement{jm_1}{U({\hat{\mathbf{y}}},\beta)}{jm_2} \matrixelement{jm_2}{U({\hat{\mathbf{z}}},\gamma)}{jm'},
:::

where the resolutions of the identity involve only a sum over $m$, not over $j$, for the same reason as in {eq}`eq-repsamos-58`. But the first and third matrix elements are for rotations about the ${\hat{\mathbf{z}}}$ axis, which by {eq}`eq-repsamos-61` are diagonal. As for the middle rotation about the ${\hat{\mathbf{y}}}$-axis, we give a special notation for it,

:::{math}
:label: eq-repsamos-66
d^j_{mm'}(\beta) = \matrixelement{jm}{U({\hat{\mathbf{y}}},\beta)}{jm'},
:::

which we call a “reduced rotation matrix.” Altogether, we have

:::{math}
:label: eq-repsamos-67
D^j_{mm'}(\alpha,\beta,\gamma) = e^{-im\alpha -im'\gamma} \,d^j_{mm'}(\beta).
:::

The reduced rotation matrix $d^j_{mm'}(\beta)$ is the nontrivial part of the matrix $D^j_{mm'}(\alpha,\beta,\gamma)$, so only it is presented in tables of rotation matrices. Notice that since the matrices for $J_2=J_y$ are purely imaginary by our phase conventions, the matrices for $U({\hat{\mathbf{y}}},\beta)=\exp(-i\beta J_y/\hbar)$, that is, the reduced rotation matrices, are purely real. This is a convenient aspect of the various conventions we have established, and it explains why Wigner chose the $zyz$-convention for Euler angles, instead of the $zxz$-convention which is common in books on classical mechanics.

We now present some examples of the reduced rotation matrices. For the case $j=0$, the result is trivial:

:::{math}
:label: eq-repsamos-68
d^0_{mm'}(\beta) = \begin{pmatrix}1\\\end{pmatrix},
:::

which is a special case of {eq}`eq-repsamos-59`.

For the case $j=1/2$, we use the properties of the Pauli matrices to obtain

:::{math}
:label: eq-repsamos-69
\begin{aligned}
d^{1/2}_{mm'}(\beta)= \cos(\beta/2) - i\sigma_y \sin(\beta/2) =\begin{pmatrix}\cos(\beta/2) &-\sin(\beta/2)\\  \sin(\beta/2) &\cos(\beta/2)\\\end{pmatrix},
\end{aligned}

:::

which is a special case of {eq}`eq-spinrot-27` (see also Prob. {ref}`prob-hilbert-1`).

For the case $j=1$, we can find recursions among the powers of the matrix for $J_y$, and sum the exponential series to obtain

:::{math}
:label: eq-repsamos-70
\begin{aligned}
d^1_{mm'}(\beta) = \begin{pmatrix} \frac{1}{2}(1+\cos\beta) & -\sin\beta/\sqrt{2} & \frac{1}{2}(1-\cos\beta)\\  \sin\beta/\sqrt{2} &\cos\beta &-\sin\beta/\sqrt{2}\\  \frac{1}{2}(1-\cos\beta) &\sin\beta/\sqrt{2} &\frac{1}{2}(1+\cos\beta)\\\end{pmatrix}.
\end{aligned}

:::

For higher values of $j$ it is most convenient to use recursion relations or other methods for calculating the matrices $d^j$. These matrices are tabulated in standard references on rotations in quantum mechanics. The matrix elements $d^j_{mm'}(\beta)$ are closely related to the Jacobi polynomials of $\cos\beta/2$, and they satisfy various differential equations and recursion relations. A more elegant way of getting these matrices is to use Schwinger's algebraic method, which converts angular momentum algebra into a version of harmonic oscillator algebra. An introduction to this subject was given in Prob. {ref}`prob-harmosc-2`.

(sec-repsamos-8)=

## Properties of the Rotation Matrices

The $D$-matrices have many properties, of which we mention three. First, if $U$ is a rotation operator and $D^j_{mm'}(U)$ the corresponding matrix, then the operator $U^{-1}$ corresponds to the matrix $D^{-1}$. But since $U$ is unitary, so is the matrix $D$, and we have

:::{math}
:label: eq-repsamos-71
D^j_{mm'}(U^{-1}) = [D^j(U)^{-1}]_{mm'} = [D^j(U)^\hc]_{mm'}= D^{j\cc}_{m'm}(U).
:::

Next there is the representation property. If we think of the $D$-matrices as parameterized by the unitary rotation operators $U$, then

:::{math}
:label: eq-repsamos-72
D^j(U_1)D^j(U_2) = D^j(U_1U_2).
:::

If we think of $D$-matrices as parameterized by the classical rotations $\Rmat$, then in the case of integer $j$ they form a representation of $SO(3)$,

:::{math}
:label: eq-repsamos-73
D^j(\Rmat_1)D^j(\Rmat_2) = D^j(\Rmat_1\Rmat_2), \qquad \\text{j integer}.
:::

In the case of half-integral $j$ they form a double valued representation of $SO(3)$, in which each classical $\Rmat$ corresponds to two $D$-matrices, differing by a sign. In that case we can write

:::{math}
:label: eq-repsamos-74
D^j(\Rmat_1)D^j(\Rmat_2) = \pm D^j(\Rmat_1\Rmat_2), \qquad \\text{j half-integer},
:::

with the same understandings as in {eq}`eq-spinrot-40`.

Next, the transformation properties of angular momentum under time reversal, a topic that we take up in {ref}`ch-timerev`, show that

:::{math}
:label: eq-repsamos-75
D^j_{mm'}(U) = (-1)^{m'-m} \, D^{j\cc}_{-m,-m'}(U).
:::

See Prob. {ref}`prob-timerev-1`.

(sec-repsamos-9)=

## The Grand Orthogonality Theorem

We mention one final, important property. The components of the $D$-matrices satisfy certain orthonormality properties, when integrated over the group manifold. If we express the $D$-matrices as functions of the Euler angles $(\alpha,\beta,\gamma)$ (see Secs. {ref}`sec-classrot-13` and {ref}`sec-spinrot-13`), then we have

:::{math}
:label: eq-repsamos-76
{1\over 16\pi^2}\int_0^{2\pi}d\alpha \int_0^\pi \sin\beta\,d\beta \int_0^{4\pi}d\gamma \, D^j_{mk}(\alpha,\beta,\gamma)^\cc \,D^{j'}_{m'k'}(\alpha,\beta,\gamma) = {\delta_{jj'}\,\delta_{mm'}\,\delta_{kk'} \over 2j+1}.
:::

This is valid for all $j$, both integral and half-integral. The ranges on the Euler angles given are those needed to cover $SU(2)$, as explained in {ref}`sec-spinrot-13` and by {eq}`eq-spinrot-54`. These ranges are needed if $j$ is a half-integer. But if $j=\ell$ is an integer, then the second half of the range $0\le\gamma\le 4\pi$ just duplicates the first half, $0\le \gamma\le 2\pi$, and {eq}`eq-repsamos-76` can be replaced by

:::{math}
:label: eq-repsamos-77
{1\over 8\pi^2}\int_0^{2\pi}d\alpha \int_0^\pi \sin\beta\,d\beta \int_0^{2\pi}d\gamma \, D^\ell_{mk}(\alpha,\beta,\gamma)^\cc \,D^{\ell'}_{m'k'}(\alpha,\beta,\gamma) = {\delta_{\ell\ell'}\,\delta_{mm'}\,\delta_{kk'} \over 2\ell+1}.
:::

Here the ranges on the Euler angles are those needed to cover $SO(3)$.

A physical application of these relations occurs in the quantum theory of the rigid body. Many small molecules are approximately rigid bodies, and the theory applies to them. In the quantum rigid body the wave function can be thought of as a function on the group manifold, $\psi(\alpha,\beta,\gamma)$, whose square gives the probability density for the orientation of the molecule. In the case of the symmetric top a suitable complete set of commuting observables for the energy eigenfunctions are $(L^2,L_z,{\bar L}_z)$, where $L_z$ is the $z$-component of the angular momentum with respect to the space frame and ${\bar L}_z$ is the $z$-component of the angular momentum with respect to the body frame. The Hamiltonian is a function of $L^2$ and ${\bar L}_z$, and the energy eigenfunctions are the components $D^\ell_{mk}(\alpha,\beta,\gamma)$ of the $D$-matrices. The integral {eq}`eq-repsamos-77` expresses the orthonormality of these eigenfunctions.

We will not prove these orthonormality relations. Their significance is much deeper than the application to the rigid body would suggest; in fact, these are special cases of what is called the *grand orthogonality theorem*, which applies to the unitary repressntations of any group. Here [in {eq}`eq-repsamos-76` and {eq}`eq-repsamos-77`] the groups are $SU(2)$ and $SO(3)$.

(sec-repsamos-10)=

## Degeneracies and Multiplicities

Let us now consider the general case in which the simultaneous eigenstates of $J^2$ and $J_3$ are degenerate, that is, the operators $(J^2,J_3)$ by themselves do not form a complete set of commuting operators, and their simultaneous eigenspaces are multidimensional. Let us denote the eigenspace of $J^2$ and $J_3$ with eigenvalues $j(j+1)\hbar^2$ and $m\hbar$ by $\SS_{jm}$, and let us write

:::{math}
:label: eq-repsamos-78
N_{jm} = \dim\SS_{jm}.
:::

We wish to consider the case that $N_{jm}>1$.

Let us take the stretched eigenspace $\SS_{jj}$ which has dimension $N_{jj}$, and let us choose a set of $N_{jj}$ linearly independent vectors in this space. Applying $J_-$ to these vectors, we obtain a set of $N_{jj}$ vectors that are eigenvectors of $J^2$ and $J_3$ with eigenvalues $j(j+1)\hbar^2$ and $(m-1)\hbar$ (that is, with a lowered value of $m$). These vectors must lie in the eigenspace $\SS_{j,j-1}$, and, as one can show, they are also linearly independent. Thus, $\dim \SS_{j,j-1} = N_{j,j-1} \ge N_{jj}$.

Now choose a set of $N_{j,j-1}$ linearly independent vectors in $\SS_{j,j-1}$ and apply the raising operator $J_+$ to them. This creates a set of $N_{j,j-1}$ vectors that lie in the stretched eigenspace $\SS_{jj}$, which, as one can show, are also linearly independent. Thus, $N_{jj} \ge N_{j,j-1}$. But this is consistent with $N_{j,j-1} \ge N_{jj}$ only if $N_{j,j-1} = N_{jj}$.

Continuing in this way, we see that all the eigenspaces $\SS_{jm}$ for $m=-j ,\ldots, +j$ have the same dimensionality. We denote this dimensionality by $N_j$, which we call the *multiplicity* of the given $j$ value. The multiplicity can take on any value from 0 (in which case the $j$ value does not occur) to $\infty$.

:::{figure} images/repsamos-fig05.png
:label: fig-repsamos-5
:width: 80%

The standard angular momentum basis $\ket{\gamma jm}$ is obtained by choosing an arbitrary orthonormal basis in the stretched space $\SS_{jj}$, indexed by $\gamma$, and applying lowering operators.
:::

Now let us choose an arbitrary, orthonormal basis in the stretched space $\SS_{jj}$, indexed by an index $\gamma$, where $\gamma=1 ,\ldots, N_j$. See {ref}`fig-repsamos-5`. In practice $\gamma$ may be the quantum number (or numbers) of one or more additional observables, that commute with both $J^2$ and $J_z$ and that form a complete set when taken with $J^2$ and $J_z$. For example, in the hydrogen atom, a commonly used complete set of commuting observables is $(H,L^2,L_z)$ with quantum numbers $(n,\ell,m)$, where $n$ takes the place of $\gamma$ and $j$ is replaced by $\ell$ to indicate orbital angular momentum.

Let us call these vectors $\ket{\gamma jj}$. If we apply $J_-$ to these, we obtain vectors in the next space down, $\SS_{j,j-1}$. One can easily show that the orthogonality of these vectors is preserved under the action of $J_-$. As for the normalization, it is changed by $J_-$, as indicated by the square root factor in {eq}`eq-repsamos-38`, but if we compensate for this we obtain an orthonormal basis in $\SS_{j,j-1}$. Let us call the new vectors $\ket{\gamma j,j-1}$, that is, let us *define* $\ket{\gamma j,j-1}$ by

:::{math}
:label: eq-repsamos-79
J_-\ket{\gamma jj} = \hbar \, \sqrt{(j+j)(j-j+1)} \, \ket{\gamma j,j-1}.
:::

Continuing in this way, we propagate an orthonormal basis from $\SS_{jj}$ all the way down to $\SS_{j,-j}$, as in {ref}`fig-repsamos-5`. We call the basis vectors $\ket{\gamma jm}$, and by their construction they satisfy

:::{math}
:label: eq-repsamos-80
\begin{aligned}
J_+\ket{\gamma jm} &= \hbar \sqrt{(j-m)(j+m+1)} \, \ket{\gamma j,m+1}, \\
J_-\ket{\gamma jm} &= \hbar \sqrt{(j+m)(j-m+1)} \, \ket{\gamma j,m-1}. \\

\end{aligned}
:::

Equivalently, using recursion as in {eq}`eq-repsamos-43`, we can write

:::{math}
:label: eq-repsamos-81
\ket{\gamma jm} = \sqrt{\ds{\ds (j+m)! \over \ds (2j)! (j-m)!}} \, \Bigl({J_- \over \hbar}\Bigr)^{j-m} \ket{\gamma jj}.
:::

By this construction, the raising and lowering operators change only the $m$ values, not the $j$ or $\gamma$ values. The resulting set of vectors forms an orthonormal basis on the entire Hilbert space $\ES$,

:::{math}
:label: eq-repsamos-82
\braket{\gamma' j'm'}{\gamma jm} = \delta_{\gamma\gamma'} \, \delta_{jj'} \, \delta_{mm'}.
:::

We call the basis $\{\ket{\gamma jm}\}$ a *standard angular momentum basis* on $\ES$ in the general case in which $(J^2,J_3)$ by themselves do not form a complete set. It is still an eigenbasis of $J^2$ and $J_3$,

:::{math}
:label: eq-repsamos-83
\begin{aligned}
J^2 \ket{\gamma jm} &= \hbar^2 \, j(j+1) \ket{\gamma jm}, \\
J_3 \ket{\gamma jm} &= \hbar \, m\ket{\gamma jm}, \\

\end{aligned}
:::

in which the index $\gamma$ resolves the degeneracies.

We can now write down the matrix elements of the raising and lowering operators, as well as those of $J^2$ and $J_3$, in the standard angular momentum basis $\ket{\gamma jm}$. Multiplying {eq}`eq-repsamos-80` or {eq}`eq-repsamos-83` on the left by $\bra{\gamma'j'm'}$ and using the orthonormality, we obtain

:::{math}
:label: eq-repsamos-84a
\begin{aligned}
\matrixelement{\gamma'j'm'}{J_3}{\gamma jm} &= \delta_{\gamma'\gamma}\,\delta_{j'j}\times m\hbar\,\delta_{m'm},
\end{aligned}
:::

:::{math}
:label: eq-repsamos-84b
\begin{aligned}
\matrixelement{\gamma'j'm'}{J_\pm}{\gamma jm} &= \delta_{\gamma'\gamma}\,\delta_{j'j}\times \sqrt{(j\mp m)(j\pm m+1)}\,\hbar\, \delta_{m',m\pm1},
\end{aligned}
:::

:::{math}
:label: eq-repsamos-84c
\begin{aligned}
\matrixelement{\gamma'j'm'}{J^2}{\gamma jm} &= \delta_{\gamma'\gamma}\,\delta_{j'j}\times j(j+1) \hbar^2 \, \delta_{m'm}.
\end{aligned}
:::

The matrix elements are diagonal in both $\gamma$ and $j$, and depend only on $j$, $m'$ and $m$. Note especially that the matrix elements are independent of $\gamma$.

Since these properties apply to $J_\pm$ and $J_3$, they apply to $J_1$ and $J_2$ as well, that is, to all three components of $\Jvec$, and therefore to any function $X(\Jvec)$. For example, the matrix elements of a rotation operator $U=U({\hat{\mathbf{n}}},\theta)$ in the standard angular momentum basis satisfy

:::{math}
:label: eq-repsamos-85
\matrixelement{\gamma jm}{U}{\gamma'j'm'} = \delta_{\gamma\gamma'}\,\delta_{jj'}\, \matrixelement{\gamma jm}{U}{\gamma jm'},
:::

where the final matrix element is just the $D$-matrix,

:::{math}
:label: eq-repsamos-86
\matrixelement{\gamma jm}{U}{\gamma jm'} =D^j_{mm'}(U).
:::

Not only is this independent of $\gamma$, it is the same $D$-matrix we defined in \secrrepsamos-6.

A practical way of thinking about these conclusions is to say that in standard angular momentum basis $\ket{\gamma jm}$, the extra index $\gamma$ just goes along for the ride insofar as angular momentum or rotation operators are concerned.

(sec-repsamos-11)=

## Invariant, Irreducible Subspaces

In {eq}`eq-repsamos-57` and {eq}`eq-repsamos-58` above we considered the action of a rotation operator on a vector of the standard angular momentum basis. Let us reconsider that action now that we have the extra index $\gamma$ in the basis. By inserting a resolution of the identity, we have

:::{math}
:label: eq-repsamos-87
\begin{aligned}
U\ket{\gamma jm} &= \sum_{\gamma'j'm'} \ket{\gamma'j'm'} \matrixelement{\gamma'j'm'}{U}{\gamma jm}= \sum_{m'}\ket{\gamma jm'}\matrixelement{\gamma jm'}{U}{\gamma jm} \\
&= \sum_{m'} \ket{\gamma jm'} D^j_{m'm}(U), \\

\end{aligned}
:::

where $U=U({\hat{\mathbf{n}}},\theta)$ is a rotation operator, where the $\gamma'$ and $j'$ sums can be done because of the Kronecker deltas in {eq}`eq-repsamos-85` and where we have used {eq}`eq-repsamos-86`. The rotation operator mixes neither spaces of different $j$ nor spaces of different $\gamma$. The same conclusion applies to any function $X(\Jvec)$ of the angular momentum.

We see that if we rotate a basis vector $\ket{\gamma jm}$ we get a linear combination of vectors with the same $\gamma$ and $j$ but different $m$. This calls attention to the subspaces,

:::{math}
:label: eq-repsamos-88
\ES_{\gamma j} = \mathspan\{\ket{\gamma jm}, m=-j,\ldots,+j\},
:::

which are invariant under the action of any function of the angular momentum $\Jvec$, notably the rotation operators. That is, if we take any vector in one of these subspaces and apply any angular momentum or rotation operator to it, we obtain another vector in the same subspace. Note that

:::{math}
:label: eq-repsamos-89
\dim\ES_{\gamma j}=2j+1.
:::

The concept of a subspace that is invariant under the action of an operator was touched upon previously in {ref}`sec-hilbert-23`. Note that the subspaces $\ES_{\gamma j}$ are orthogonal to one another, that is, every vector in one such space is orthogonal to every vector in any other such space.

The subspaces $\ES_{\gamma j}$ are not only invariant under the action of the rotations, they are also *irreducible*. This means that they contain no smaller subspaces that are invariant under the rotations. These invariant, irreducible subspaces play an important role in any system upon which rotations act, and we shall refer to them frequently. We will call them *irreducible subspaces* for short. You may think of them as spaces spanned by vectors connected by raising and lowering operators. The entire Hilbert space $\ES$ upon which rotations act is decomposed by the action of the rotations into a direct sum of mutually orthogonal, invariant, irreducible subspaces,

:::{math}
:label: eq-repsamos-90
\ES = \sum_{\gamma j} \oplus \ES_{\gamma j}.
:::

This is a basic geometrical structure imposed on the Hilbert space by the action of rotations.

An important application of these concepts occurs in any system that is isolated from its environment, so that its energy does not depend on its orientation. Such systems are very common in applications. In this case the Hamiltonian commutes with all rotation operators, which, it turns out, implies that each energy eigenspaces consists of one or more irreducible subspaces, usually just one. In the usual case that an energy eigenspace consists of a single irreducible subspace, the energy level is characterized by an angular momentum quantum number $j$ and is $2j+1$-fold degenerate. We will explore these facts in greater detail in {ref}`ch-wigeck`.

The concept of an invariant, irreducible subspace plays an important role in the representation theory of any group. We have developed the idea here in an *ad hoc* manner, suitable for the rotation group and the applications we will consider.

(sec-repsamos-12)=

## Generalized Adjoint Formula

We recall that we derived a version of the adjoint formula for classical rotations in {eq}`eq-classrot-48`, and later we found an analogous formula, {eq}`eq-spinrot-34`, for spin-$\frac{1}{2}$ rotations. We now generalize this to arbitrary representations of the rotation operators. The generalization is obvious; it is

:::{math}
:label: eq-repsamos-91
\boxed{ U \Jvec U^\hc = \Rmat^{-1} \Jvec,}
:::

where $U=U({\hat{\mathbf{n}}},\theta)$ and $\Rmat=\Rmat({\hat{\mathbf{n}}},\theta)$. Notice that the left hand side is quadratic in $U$, so in the case of double-valued representations of $SO(3)$, it does not matter which $U$ operator we choose to represent the rotation $\Rmat$.

To prove {eq}`eq-repsamos-91`, we define the operator vector,

:::{math}
:label: eq-repsamos-92
\Kvec(\theta) = U({\hat{\mathbf{n}}},\theta) \, \Jvec \, U({\hat{\mathbf{n}}},\theta)^\hc,
:::

and we note the initial condition,

:::{math}
:label: eq-repsamos-93
\Kvec(0) = \Jvec.
:::

Next we obtain a differential equation for $\Kvec(\theta)$:

:::{math}
\begin{aligned}
\dod{\Kvec(\theta)}{\theta} &= \dod{U}{\theta} \Jvec U^\hc + U \Jvec \dod{U^\hc}{\theta} = -{i\over\hbar} U [{\hat{\mathbf{n}}}\cdot\Jvec, \Jvec] U^\hc
\end{aligned}
:::

:::{math}
:label: eq-repsamos-94
\begin{aligned}
&= -{\hat{\mathbf{n}}}\cross (U\Jvec U^\hc) = -({\hat{\mathbf{n}}} \cdot\Jmatvec) \Kvec.
\end{aligned}
:::

The solution is

:::{math}
:label: eq-repsamos-95
\Kvec(\theta) = \exp\bigl( -\theta{\hat{\mathbf{n}}}\cdot\Jmatvec\bigr) \Kvec(0) = \Rmat({\hat{\mathbf{n}}},\theta)^{-1} \Jvec,
:::

which is equivalent to the adjoint formula {eq}`eq-repsamos-91`.

Finally, we can dot both sides of {eq}`eq-repsamos-91` by $-i \theta {\hat{\mathbf{n}}} /\hbar$ and exponentiate, to obtain a formula analogous to {eq}`eq-classrot-51`. After placing $0$ subscripts on $U$ and $\Rmat$ for clarity, the result is

:::{math}
:label: eq-repsamos-96
U_0 U({\hat{\mathbf{n}}},\theta) U_0^\hc = U(\Rmat_0{\hat{\mathbf{n}}},\theta),
:::

where $U_0$ and $\Rmat_0$ are corresponding quantum and classical rotations. This is an exponentiated version of the adjoint formula, similar to Eq.~({eq}`eq-classrot-51`. Notice again that the left hand side is quadratic in $U_0$, so that in the case of double-valued representations it does not matter which $U_0$ operator we choose to represent the rotation $\Rmat_0$. {eq}`eq-repsamos-96` is an exponentiated version of the adjoint formula {eq}`eq-repsamos-91`.

\problems

(prob-repsamos-1)=

**Problem \prbdrepsamos-1.}  A molecule is approximately a rigid body. Consider a molecule such as $H_2O$, $NH_3$, or $CH.** 

:::{math}
:label: eq-repsamos-97
H= {L_x^2\over 2I_x} + {L_y^2\over 2I_y} + {L_z^2\over 2I_z},
:::

where $\Lvec=(L_x,L_y,L_z)$ is the angular momentum vector with respect to the body frame, and $(I_x,I_y,I_z)$ are the principal moments of inertia. The body frame is assumed to be the principal axis frame in {eq}`eq-repsamos-97`. The angular velocity $\omegavec$ of the rigid body is related to the angular momentum $\Lvec$ by

:::{math}
:label: eq-repsamos-98
\Lvec = \Imat \omegavec,
:::

where $\Imat$ is the moment of inertia tensor. When {eq}`eq-repsamos-98` is written in the principal axis frame, it becomes

:::{math}
:label: eq-repsamos-99
\omega_i = {L_i \over I_i},     \qquad i=x,y,z.
:::

Finally, the equations of motion for the angular velocity or angular momentum in the body frame are the *Euler equations*,

:::{math}
:label: eq-repsamos-100
\dot\Lvec + \omegavec\cross\Lvec=0.
:::

By using {eq}`eq-repsamos-99` to eliminate either $\omegavec$ or $\Lvec$, {eq}`eq-repsamos-100` can be regarded as an equation for either $\Lvec$ or $\omegavec$. The Euler equations are trivial for a spherical top ($I_x=I_y=I_z$), they are easily solvable in terms of trigonometric functions for a symmetric top ($I_x=I_y=I_\perp \ne I_z$), and they are solvable in terms of elliptic functions for an asymmetric top ($I_x$, $I_y$, $I_z$ all unequal). The symmetric top is studied in all undergraduate courses in classical mechanics.

\problempart{(a)} In quantum mechanics, it turns out that the Hamiltonian operator for a rigid body has exactly the form {eq}`eq-repsamos-97`. The angular momentum $\Lvec$ satisfies the commutation relations,

:::{math}
:label: eq-repsamos-101
[ L_i, L_j ] = -i\hbar\, \epsilon_{ijk} \, L_k,
:::

with a minus sign relative to the familiar commutation relations because the components of $\Lvec$ are (in this problem) measured relative to the body frame. (We will not justify this. If the components of $\Lvec$ were measured with respect to the space or inertial frame, then there would be the usual plus sign in {eq}`eq-repsamos-101`.) Compute the Heisenberg equations of motion for $\Lvec$, and compare them with the classical Euler equations. You may take {eq}`eq-repsamos-98` or {eq}`eq-repsamos-99` over into quantum mechanics, in order to define an operator $\omegavec$ to make the Heisenberg equations look more like the classical Euler equations. (Just get the equation for $L_x$, then cycle indices to get the others.) Make your answer look like {eq}`eq-repsamos-100` as much as possible.

\problempart{(b)} It is traditional in the theory of molecules to let the quantum number of $L_z$ (referred to the body frame) be $k$. Write the rotational energy levels of a symmetric top ($I_x=I_y=I_\perp \ne I_z$) in terms of a suitable set of quantum numbers. Indicate any degeneracies. How is the oblate case ($I_z > I_\perp$) qualitatively different from the prolate case ($I_\perp > I_z$)? Hint: In order to deal with standard commutation relations, you may wish to write $\tilde\Lvec=-\Lvec$, so that $[\tilde L_i, \tilde L_j] = i\hbar\,\epsilon_{ ijk}\,\tilde L_k$.

(prob-repsamos-2)=

**Problem 2..** 

:::{math}
:label: eq-repsamos-102
{\hat{\mathbf{n}}}={1 \over \sqrt{3}} (1,1,1),
:::

measured, and the result is $\hbar$. Subsequently $S_z$ is measured, with various probabilities of the three possible outcomes.

Let $\Rmat$ be a rotation that maps the ${\hat{\mathbf{z}}}$ axis into ${\hat{\mathbf{n}}}$, that is, let

:::{math}
:label: eq-repsamos-103
\Rmat{\hat{\mathbf{z}}} = {\hat{\mathbf{n}}}.
:::

Express the aforementioned probabilities in terms of the matrix, $D^1_{mm'}(\Rmat)$. Work out this matrix to find the probabilities explicitly. You may use tables of $d$-matrices.

(prob-repsamos-3)=

**Problem 3..** 

First show that if {eq}`eq-repsamos-91` is true for two rotation operators $U_1$ and $U_2$, and the corresponding classical rotations $\Rmat_1$ and $\Rmat_2$, then it is true for the products $U=U_1U_2$ and $\Rmat=\Rmat_1\Rmat_2$. Then show that {eq}`eq-repsamos-91` is true for infinitesimal rotations. This is sufficient to prove the formula.
