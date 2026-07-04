---
title: "46. Introduction to the Dirac Equation"
---
(ch-dirac)=

# 46. Introduction to the Dirac Equation

(sec-dirac-1)=

## Introduction

In 1927 Pauli published a version of the Schr\"odinger equation for spin-$\frac{1}{2}$ particles that incorporates the interaction of the spin with a magnetic field. This equation is

:::{math}
:label: eq-dirac-1
i\hbar\frac{\partial \psi}{\partial t} = \Bigl[{1\over 2m}\Bigl( \pvec-{q\over c}\Avec\Bigr)^2 -\muvec\cdot\Bvec + q\Phi \Bigr]\psi,
:::

where the magnetic moment $\muvec$ is related to the spin $\Svec$ as described in {ref}`ch-spinmagf`. See Prob. {ref}`prob-jjcouple-1`(b) and {eq}`eq-jjcouple-27`. Pauli understood that spin was in a sense a relativistic effect, and that his equation amounted to a grafting of some relativistic corrections onto the nonrelativistic framework of the Schr\"odinger theory. As such, he felt that his equation was neither deep nor elegant, and he hesitated to publish it, hoping to find a proper and complete relativistic theory of the electron. In that effort, however, he was anticipated by Dirac, who in 1928 published his work on his wave equation, which we take up in these notes.

The Dirac equation is rightly regarded as one of the great monuments of modern physics. There is considerable formalism involved in mastering it, but it is an essential part of relativistic quantum mechanics, and we will take it one step at a time.

(sec-dirac-2)=

## The Dirac Equation

{ref}`ch-kleing`\ describes the state of affairs when Dirac undertook his investigations of relativistic wave equations. Recognizing that the negative probabilities of the Klein-Gordon equation were related to the fact that the Klein-Gordon equation is second order in time, Dirac decided to find a relativistic wave equation that was first order in time. Following Dirac, we write this wave equation as

:::{math}
:label: eq-dirac-2
i\hbar \frac{\partial \psi}{\partial t} = H\psi,
:::

that is, as a Schr\"odinger equation, but with some Hamiltonian $H$ that is to be determined. We search for the correct relativistic $H$, taking at first the case of the free particle.

Dirac reasoned that since his equation was first order in the time derivative, and since relativity is supposed to treat space and time on an equal footing, it should also be first order in the spatial derivatives. That is, it should be linear in the derivatives $\partial/\partial x_i$, or, equivalently, in the momentum operators $-i\hbar\,\partial/\partial x_i$. Therefore he guessed that $H$ would have the form

:::{math}
:label: eq-dirac-3
H = c\alphavec\cdot\pvec + mc^2 \beta,
:::

where $\alphavec$ is a vector containing the coefficients multiplying the spatial derivatives and where $\pvec=-i\hbar\del$ is the usual momentum operator. A factor of $c$ has been split off $\alphavec$ so that these coefficients will be dimensionless. Dirac also added a constant term involving a coefficient $\beta$, with $mc^2$ split off so that $\beta$ would also be dimensionless. The coefficients $\alphavec$ and $\beta$ are to be determined. Thus, the Dirac equation for a free particle can be written,

:::{math}
:label: eq-dirac-4
i\hbar\frac{\partial \psi}{\partial t} = -i\hbar c \sum_{k=1}^3 \alpha_k \frac{\partial \psi}{\partial x_k} + mc^2\beta\psi.
:::

The coefficients $\alpha_k$ or $\alphavec= (\alpha_1 ,\alpha_2 ,\alpha_3)$ cannot be ordinary numbers, because if they were $\alphavec$ would specify some privileged direction in space, which we don't expect for a free particle. Therefore Dirac assumed that the wave function $\psi$ was some kind of multicomponent object or spinor,

:::{math}
:label: eq-dirac-5
\psi = \begin{pmatrix}\psi_1 \\ \vdots \\ \psi_N \\\end{pmatrix},
:::

where the number of components $N$ is to be determined. Then $\alpha_k$, $k=1,2,3$, and $\beta$ are $N\times N$ matrices. The matrices $\alpha_k$ form a “vector” of matrices $\alphavec$, much as the Pauli matrices $\sigmavec$ do. You must henceforth understand, when looking at the Dirac equation, that $\psi$ is a spinor and $\alphavec$ and $\beta$ are matrices, although usually we do not indicate this explicitly. Since the free-particle Hamiltonian should be invariant under space and time displacements, the matrices $\alpha_k$ and $\beta$ must be constant, that is, independent of $\xvec$ and $t$. Thus, they act on the spin degrees of freedom of the particle, much as do the Pauli matrices in the nonrelativistic theory of a spin-$\frac{1}{2}$ particle, and commute with purely spatial operators such as $\xvec$ and $\pvec$. Also, since the Dirac Hamiltonian should be Hermitian, the matrices $\alpha_k$ and $\beta$ must also be Hermitian.

To determine the matrices $\alpha_k$ and $\beta$, Dirac required that every solution of the Dirac equation should also satisfy the Klein-Gordon equation. This is so that the classical energy-momentum relation, $E^2=m^2c^4 + c^2\pvec^2$, would be satisfied. Applying $i\hbar\,\partial/\partial t$ to {eq}`eq-dirac-4` we obtain,

:::{math}
:label: eq-dirac-6
-\hbar^2 {\partial^2\psi\over\partial t^2} = H^2 \psi =-\hbar^2c^2 \sum_{k\ell} \alpha_k\alpha_\ell {\partial^2 \psi \over \partial x_k \partial x_\ell}  -i\hbar mc^3 \sum_{k=1}^3 (\alpha_k \beta + \beta\alpha_k) \frac{\partial \psi}{\partial x_k} + m^2c^4 \beta^2\psi.
:::

In order that this agree with the Klein-Gordon equation {eq}`eq-kleing-7`, we must have

:::{math}
:label: eq-dirac-7
{1\over 2}(\alpha_k\alpha_\ell + \alpha_\ell\alpha_k) = \delta_{k\ell}, \qquad \alpha_k\beta + \beta\alpha_k =0, \qquad \beta^2 = 1,
:::

where we symmetrize the first equation in $k$ and $\ell$ since the derivatives $\partial^2\psi/\partial x_k \partial x_\ell$ are symmetric. The right-hand sides of {eq}`eq-dirac-7` are understood to be multiplied by the $N\times N$ identity matrix, which we write simply as $1$. Notice that if we set $k=\ell$ in the first of these equations we get $\alpha_k^2=1$, $k=1,2,3$, so all four Dirac matrices $\alpha_k$, $\beta$ square to unity.

The conditions {eq}`eq-dirac-7` are conveniently expressed in terms of anticommutators. That is, we rewrite them as

:::{math}
:label: eq-dirac-8
\{\alpha_k,\alpha_\ell\} = 2\delta_{k\ell}, \qquad \{\alpha_k,\beta\}=0, \qquad \{\beta,\beta\} = 2.
:::

Equations {eq}`eq-dirac-7` or {eq}`eq-dirac-8` constitute the *Dirac algebra*, that is, the set of algebraic relations which the Dirac matrices $\alpha_k$ and $\beta$ must satisfy. They amount to an encoding of the relativistic energy-momentum relations in terms of matrices. The Dirac algebra is a special case of a kind of anticommuting algebra, encoding the components of a metric tensor, that in mathematics is known as a *Clifford algebra*.

(sec-dirac-3)=

## Finding the Dirac Matrices

To find Hermitian matrices $\alpha_k$, $\beta$ that satisfy the Dirac algebra we note first of all that $\alpha_k^2=1$ and $\beta^2=1$, so the eigenvalues of all four matrices can only be $\pm1$. Next, multiplying the middle equation in {eq}`eq-dirac-7` from the left by $\beta$ and taking traces we find

:::{math}
:label: eq-dirac-9
\tr(\beta \alpha_k\beta) + \tr(\alpha_k) =0.
:::

But by cycling the order of matrices, the first term can be written

:::{math}
:label: eq-dirac-10
\tr(\beta \alpha_k \beta) = \tr(\beta^2\alpha_k) = \tr(\alpha_k),
:::

which, when used in {eq}`eq-dirac-9`, gives $\tr\alpha_k=0$. In a similar manner we show that $\tr\beta=0$. The Dirac matrices are Hermitian and traceless. Since the trace is the sum of the eigenvalues, which must be $\pm1$, the number of positive and negative eigenvalues must be equal. This means that the dimension $N$ of the Dirac matrices must be even.

The simplest possibility is $N=2$. All $2\times2$ Hermitian matrices can be expanded as a linear combination of the Pauli matrices $\sigmavec$ and the identity with real coefficients, which can be used to search for the expansion coefficients which will cause the Dirac relations {eq}`eq-dirac-8` to be satisfied. It turns out after an analysis that there is no solution to the Dirac algebra in terms of $2\times2$ matrices.

The next simplest case is $N=4$. Here Dirac was able to find a explicit solution for matrices $\alpha_k$ and $\beta$ that satisfies his algebra. The solution can be written,

:::{math}
:label: eq-dirac-11
\begin{aligned}
\alphavec = \begin{pmatrix}0 & \sigmavec \\ \sigmavec & 0 \\\end{pmatrix}, \qquad \beta= \begin{pmatrix}1 & 0 \\ 0 & -1 \\\end{pmatrix}, \qquad \\text{\rm(Dirac-Pauli)}
\end{aligned}

:::

where the $4\times4$ matrices are partitioned into four $2\times2$ matrices, which are represented in terms of Pauli matrices and the $2\times2$ identity matrix (indicated simply by $1$). As indicated, {eq}`eq-dirac-11` constitutes the *Dirac-Pauli representation* of the Dirac algebra.

(sec-dirac-4)=

## Equivalent and Inequivalent Representations

Whenever we have an abstract set of algebraic relations that a set of matrices or linear operators must satisfy, such as the Dirac algebra {eq}`eq-dirac-8`, and we find an explicit set of matrices or operators that satisfy those relations, then we say that we have found a *representation* of those relations. Thus, Dirac found a representation of his algebra by means of $4\times4$ matrices. However, a representation, once found, is not unique, because we can conjugate all the matrices by a fixed, nonsingular matrix $S$. That is, if we make the replacements,

:::{math}
:label: eq-dirac-12
\alphavec \to S\alphavec S^{-1}, \qquad \beta \to S\beta S^{-1},
:::

then the Dirac algebra {eq}`eq-dirac-8` is still satisfied. This amounts to a change of basis in “spin space.” However, since we want the matrices $\alphavec$ and $\beta$ to be Hermitian, we should restrict the matrix $S$ to be unitary.

Any two representations (speaking of matrix representations) of the same dimensionality that differ merely by a change of basis are called *equivalent*. The implication is that equivalent representations are trivially related. But if two matrix representations of the same dimensionality are not related by a change of basis, then they are said to be *inequivalent*.

In the case of the Dirac algebra, it can be shown that all $4\times4$ representations are equivalent to the representation {eq}`eq-dirac-11` found by Dirac. Thus, we can say that to within a change of basis in spin space, Dirac's representation {eq}`eq-dirac-11`, the Dirac-Pauli representation, is unique. It is the representation of the Dirac algebra of smallest dimensionality, and thus provides the simplest solution to the problem of finding matrices that satisfy the Dirac algebra.

We remark that Dirac's representation of his algebra is also *irreducible*. This means that there is no change of basis that causes all the matrices to take on a block-diagonal structure (the same block-diagonal structure for all matrices). If there were such a change of basis, then the blocks would constitute a representation of the Dirac algebra by means of matrices smaller than $4\times4$, and we have seen that there is no such representation.

In doing physical calculations in the Dirac theory it is never actually necessary to use explicit representations of the Dirac matrices, such as the Dirac-Pauli representation {eq}`eq-dirac-11`. The same is actually true of the Pauli matrices $\sigmavec$; it is never actually necessary to use the explicit forms of the three Pauli matrices that all students of quantum mechanics memorize. Nevertheless, some calculations are simpler in one representation or another. The Dirac-Pauli representation {eq}`eq-dirac-11` of the Dirac algebra is most useful in studying the nonrelativistic limit of the Dirac equation, and it is the one that we will use the most. But we mention another representation, the *Weyl representation*, that is useful for studying ultrarelativistic particles such as neutrinos. The Weyl representation is

:::{math}
:label: eq-dirac-13
\begin{aligned}
\alphavec=\begin{pmatrix}\sigmavec & 0 \\ 0 & -\sigmavec \\\end{pmatrix}, \qquad \beta=\begin{pmatrix}0 & -1 \\ -1 & 0 \\\end{pmatrix}, \qquad \\text{\rm(Weyl)}.
\end{aligned}

:::

The explicit change of basis taking us from the Dirac-Pauli to the Weyl representation is

:::{math}
:label: eq-dirac-14
(\alpha_k)_Weyl = W^\dagger \,(\alpha_k)_D-P \,W, \qquad \beta_Weyl = W^\dagger\, \beta_D-P \,W,
:::

where

:::{math}
:label: eq-dirac-15
\begin{aligned}
W = {1\over\sqrt{2}} \begin{pmatrix}1 & -1 \\ 1 & 1 \\\end{pmatrix}.
\end{aligned}

:::

There is another representation of the Dirac algebra in common use, the *Maiorana representation*, that makes the effects of time-reversal simple. We will not use the Maioriana representation and so will not quote it.

We remark that the fact that the Dirac matrices are 4-dimensional has nothing to do with the fact that space-time is 4-dimensional. The Dirac matrices act on spin space, not on space-time. Conversely, while there are 4-dimensional matrices with space-time indices, such as a Lorentz transformation $\Lambda^\mu{}_\nu$ or the electromagnetic field tensor $F_{\mu\nu}$, these do not act on spin space.

(sec-dirac-5)=

## Minimal Coupling

{eq}`eq-dirac-3` gives the Dirac Hamiltonian for a free particle, where now we take $\psi$ to be a 4-component spinor and we have explicit representations for the matrices $\alphavec$ and $\beta$. To incorporate the interaction of the particle with an electromagnetic field we may use the minimal coupling prescription, which is described at a classical level in {ref}`sec-classmech-17`. In the present context it means that we make the replacements,

:::{math}
:label: eq-dirac-16
H \to H-q\Phi, \qquad \pvec\to \pvec -{q\over c}\Avec,
:::

in {eq}`eq-dirac-3`, where $q$ is the charge of the particle and $\Phi$ and $\Avec$ are the scalar and vector potentials. This gives the new Hamiltonian,

:::{math}
:label: eq-dirac-17
H = c\alphavec\cdot\Bigl[\pvec-{q\over c}\Avec(\xvec,t) \Bigr] + q\Phi(\xvec,t) + mc^2\beta.
:::

It is a guess that this is the correct Hamiltonian for a Dirac particle interacting with the electromagnetic field, but it is the simplest guess consistent with Lorentz covariance.

Notice that in coming this far we have made the simplest choice possible at each stage where there was more than one possibility, including the representation of the Dirac algebra and the minimal coupling prescription.

(sec-dirac-6)=

## The Probabilty Density and Current

Let us now search for a conserved probability density and current. Following the steps we used in the nonrelativistic theory, we begin by writing down the Dirac equation and its Hermitian conjugate. We use the Hamiltonian {eq}`eq-dirac-17`, which includes the interaction with an electromagnetic field via the minimal coupling prescription. The Dirac equation itself is

:::{math}
:label: eq-dirac-18
i\hbar\frac{\partial \psi}{\partial t} = c\alphavec\cdot\Bigl(-i\hbar\del\psi -{q\over c} \Avec\psi\Bigr) + q\Phi\psi + mc^2\beta\psi.
:::

When we take the Hermitian conjugate, the column spinor $\psi$ is mapped into a row spinor,

:::{math}
:label: eq-dirac-19
\begin{aligned}
\psi=\left[\begin{matrix}\psi_1 \\ \psi_2\\ \psi_3\\ \psi_4\\\end{matrix}\right]\to \psi^\dagger = \left[\begin{matrix}\psi_1^\cc & \psi_2^\cc & \psi_3^\cc & \psi_4^\cc \\\end{matrix}\right].
\end{aligned}

:::

In the following you must remember that $\psi^\dagger$ is a row spinor, so that when it is multiplied onto a Dirac matrix from the left it produces another row spinor. The Dirac matrices $\alphavec$ and $\beta$ are mapped into themselves under Hermitian conjugation, since they are Hermitian, and the order of matrix and spinor multiplication is reversed. Altogether, the Hermitian conjugate of the Dirac equation is

:::{math}
:label: eq-dirac-20
-i\hbar\frac{\partial \psi^\dagger}{\partial t} = c\Bigl[i\hbar(\del\psi^\dagger)\cdot\alphavec -{q\over c}\psi^\dagger(\alphavec\cdot\Avec)\Bigr] + q\Phi\psi^\dagger +mc^2 \psi^\dagger \beta.
:::

Now we multiply {eq}`eq-dirac-18` on the left by $\psi^\dagger$ and {eq}`eq-dirac-20` on the right by $\psi$, where complete contractions in spinor indices is understood, so the results are scalars insofar as the spin indices are concerned. The terms involving $\Avec$, $\Phi$ and $\beta$ are the same, so when we subtract these cancel. What is left is

:::{math}
:label: eq-dirac-21
i\hbar\Bigl( \psi^\dagger \frac{\partial \psi}{\partial t} + \frac{\partial \psi^\dagger}{\partial t}\psi\Bigr) = -i\hbar c[\psi^\dagger \alphavec\cdot\del\psi + (\del\psi^\dagger)\cdot\alphavec\psi],
:::

or,

:::{math}
:label: eq-dirac-22
\frac{\partial \rho}{\partial t} + \del\cdot\Jvec =0,
:::

where

:::{math}
:label: eq-dirac-23
\rho=\psi^\dagger \psi, \qquad \Jvec=c\psi^\dagger \alphavec \psi.
:::

In this derivation multiplication of spin matrices times spinors is implied, as is the multiplication of row spinors times column spinors. If this is not clear we can always write out the spin operations explicitly, for example, {eq}`eq-dirac-23` can be written,

:::{math}
:label: eq-dirac-24
\rho = \sum_{r=1}^4 |\psi_r|^2, \qquad J_i = c\sum_{r,s=1}^4 \psi_r^\cc \,(\alpha_i)_{rs} \,\psi_s.
:::

We have not only found a conserved probability density and current, but the density is nonnegative definite, $\rho\ge0$. Recall that the conserved density in the theory of the Klein-Gordon equation could take on any sign, and so could not be interpreted as a probability density. In deriving {eq}`eq-dirac-23` Dirac felt that he had overcome one of the main difficulties of the Klein-Gordon equation.

Notice that in the nonrelativistic Pauli theory of a spin-$\frac{1}{2}$ particle the wave function is a 2-component spinor,

:::{math}
:label: eq-dirac-25
\psi=\left[\begin{matrix}\psi_+ \\ \psi_-\\\end{matrix}\right],
:::

and the probability density is

:::{math}
:label: eq-dirac-26
\rho=\psi^\dagger \psi = |\psi_+|^2 + |\psi_-|^2.
:::

It is the probability density of finding the particle, if we don't care about the spin state. That is, it is the probability density of finding a spin up particle, plus the probability density of finding a spin down particle. We do not yet have a physical interpretation of the four components of the Dirac spinor, but the similarity between Dirac's $\rho$ and the $\rho$ in the Pauli theory is notable.

If we set

:::{math}
:label: eq-dirac-27
J^\mu=\begin{pmatrix}c\rho \\ \Jvec \\\end{pmatrix}
:::

then the continuity equation {eq}`eq-dirac-22` looks covariant,

:::{math}
:label: eq-dirac-28
\partial_\mu J^\mu = \frac{\partial J^\mu}{\partial x^\mu} =0.
:::

However, as remarked earlier in connection with the Schr\"odinger theory (see {ref}`sec-kleing-6`), to show that {eq}`eq-dirac-28` is covariant we must show that $J^\mu$ transforms as a 4-vector under Lorentz transformations. That is a fairly large project that we defer until we have a better physical understanding of the Dirac equation (it is covered in {ref}`ch-covariance`).

(sec-dirac-7)=

## Free Particle Solutions at Rest

To gain physical insight into the Dirac equation, we examine the simplest possible free particle solutions, namely those for a particle at rest. We use the Dirac-Pauli representation for the Dirac matrices. The free particle Dirac equation can be written,

:::{math}
:label: eq-dirac-29
i\hbar\frac{\partial \psi}{\partial t} = -i\hbar c\alphavec\cdot\del\psi + mc^2 \beta \psi.
:::

But if the particle is at rest then the momentum vanishes, and $\del\psi=0$. Then the Dirac equation becomes

:::{math}
:label: eq-dirac-30
\begin{aligned}
i\hbar \frac{\partial \psi}{\partial t} = mc^2 \begin{pmatrix}1 & 0 \\ 0 & -1\\\end{pmatrix}\psi,
\end{aligned}

:::

where the matrix shown is $\beta$ [see {eq}`eq-dirac-11`]. The four components of the Dirac spinor decouple in this case, and the solutions are easy to write down. They are

:::{math}
:label: eq-dirac-31
\begin{pmatrix}1\\ 0 \\ 0 \\ 0 \\\end{pmatrix} e^{-imc^2t/\hbar}, \quad \begin{pmatrix}0\\ 1\\ 0\\ 0\\\end{pmatrix} e^{-imc^2t/\hbar}, \quad \begin{pmatrix}0\\ 0\\ 1\\ 0\\\end{pmatrix} e^{+imc^2t/\hbar}, \quad \begin{pmatrix}0\\ 0\\ 0\\ 1\\\end{pmatrix} e^{+imc^2t/\hbar}.
:::

The first pair of these solutions have energy $mc^2$, just what we would expect for a particle at rest, with the usual custom in relativity theory of including the rest mass-energy in the reckoning the energy of the particle. The second pair of solutions have energy $-mc^2$. We see that the Dirac equation, like the Klein-Gordon equation, possesses solutions of negative energy. There is no ready interpretation of these solutions, and we will have to do some work to find their proper physical meaning. As for the positive energy solutions, we note that if we ask for the free particle solutions at rest of the Pauli equation, they are

:::{math}
:label: eq-dirac-32
\begin{pmatrix}1 \\ 0 \\\end{pmatrix}, \qquad \begin{pmatrix}0 \\ 1 \\\end{pmatrix},
:::

with no dependence on space or time. These look very similar to the first two solutions {eq}`eq-dirac-31` of the Dirac equation, in fact they are the same if we ignore the third and fourth components of the spinor and shift the origin of energy by $mc^2$ to conform with the usual custom of reckoning energy in nonrelativistic problems.

Do not let this example lead you to think that the first two components of the Dirac spinor are identical to the two components of the Pauli spinor. This is true for the free particle at rest, but not for other problems, including the free particle in some state of motion. Nevertheless, it is true that the solutions of the Pauli equation that are the nonrelativistic limit of the Dirac equation do coincide approximately with the upper two components of the Dirac spinor. We will examine this point in a little more detail in a moment, and in considerably more detail in {ref}`ch-foldyw`.

(sec-dirac-8)=

## Heisenberg Equations of Motion

To gain further insight into the physical interpretation of the Dirac equation, we examine the Heisenberg equations of motion. See {ref}`sec-tevolut-5` for the basic theory of the Heisenberg picture. We will write the Heisenberg equations of motion as

:::{math}
:label: eq-dirac-33
\dot X = \frac{\partial X}{\partial t} - {i\over\hbar} [X,H],
:::

where $H$ is the Hamiltonian and $X$ is any operator. This is the same as {eq}`eq-tevolut-22`, but without the $H$ subscripts. We will use the Hamiltonian {eq}`eq-dirac-17`, that is, the Hamiltonian of a Dirac particle interacting with an electromagnetic field. We will write the kinetic momentum as

:::{math}
:label: eq-dirac-34
\pivec = \pvec - {q\over c}\Avec(\xvec,t),
:::

to distinguish it from the canonical momentum $\pvec$. Then the Hamiltonian is

:::{math}
:label: eq-dirac-35
H=c\alphavec\cdot\pivec + q\Phi + mc^2\beta.
:::

Basic commutators are

:::{math}
:label: eq-dirac-36
[x_i,x_j] =0, \qquad [x_i,\pi_j] = i\hbar\,\delta_{ij}, \qquad [\pi_i,\pi_j] = {i\hbar q\over c} \epsilon_{ijk}\, B_k,
:::

where $B_i$ is the component of the magnetic field. See also Prob. {ref}`prob-tevolut-1` and {eq}`eq-magfield-5` and {eq}`eq-magfield-6`.

First we let $X=x_i$ (a component of the position operator). The operator $x_i$ has no explicit time dependence, and everything in $H$ except $\pivec$ commutes with $x_i$. Thus,

:::{math}
:label: eq-dirac-37
[x_i,H] = c[x_i,\alpha_j \pi_j] = c\alpha_j [x_i,\pi_j] = i\hbar c\, \alpha_i.
:::

We use the Heisenberg equations of motion to define the velocity operator $\vvec$, and we find

:::{math}
:label: eq-dirac-38
\vvec = \dot\xvec = c\alphavec.
:::

The velocity operator in the Dirac theory turns out to be a purely spin operator, which is a surprise. In the Schr\"odinger or Pauli theory the velocity operator is $\vvec=\pivec/m$, or, for a free particle, simply $\vvec=\pvec/m$. It is a purely spatial operator in the nonrelativistic theory. In the relativistic theory of the free particle we might have expected something like

:::{math}
:label: eq-dirac-39
\vvec = {c^2\pvec \over E} = {c^2 \pvec \over \sqrt{m^2c^4 + c^2\pvec^2}}
:::

which is the expression in classical relativity giving the velocity as a function of the momentum. In any case, we might have expected the velocity to be a function of the momentum, and, hence, a purely spatial operator.

It will take us some time to understand the physical meaning of this result, which is discussed further later in connection with the Gordon decomposition of the current (see {ref}`sec-spdirac-10`.) For now we simply remark that the same interpretation of $c\alphavec$ (as a velocity operator) also appears in the probability current, $\Jvec = c\psi^\dagger\alphavec \psi$ [see {eq}`eq-dirac-23`]. Recall that the probability current in the nonrelativistic theory is $\Re(\psi^\cc \vvec \psi)$, and, in any case, the probability current has to have dimensions of probability density ($\psi^\dagger \psi$) times a velocity.

Further strange features of the velocity operator in the Dirac theory emerge when we consider making a measurement of the velocity. If we measure one component of the velocity, say, $v_x = v_1$, the answers can only be the eigenvalues of the operator $c\alpha_1$. But we have seen that the eigenvalues of all the Dirac matrices are $\pm1$. Therefore, a measurement of $v_x$ yields only two results, $\pm c$. Furthermore, we cannot measure more than one component of the velocity simultaneously, since the commutator $[\alpha_i,\alpha_j]$ is nonzero. In the Dirac theory the components of the velocity do not commute, so it is impossible to measure the direction of motion of the particle.

Another strange feature of the velocity operator is that it does not commute with the free particle Hamiltonian, so the velocity (or its expectation value) is not constant, even for a free particle. This behavior is related to the *Zitterbewegung*, which we will consider in {ref}`sec-spdirac-11`.

A proper appreciation of these results requires developments that have not been explained yet. For now suffice it to say that it turns out that the position operator does not have the same meaning in relativistic quantum mechanics as in the nonrelativistic theory, because if we try to localize the particle in a region smaller than the Compton wavelength there will arise significant amplitudes for the production of particle-antiparticle pairs. Thus, we are no longer dealing with a single particle. Recall that the photon does not have a position operator.

Now we compute the time derivative of the kinetic momentum $\pivec$, for which

:::{math}
:label: eq-dirac-40
\frac{\partial \pivec}{\partial t} = -{q\over c} \frac{\partial \Avec}{\partial t}.
:::

Working out the commutators and expressing the derivatives of $\Avec$ and $\Phi$ in terms of the electric and magnetic fields, we find

:::{math}
:label: eq-dirac-41
\dot\pivec = q\Bigl[\Evec(\xvec,t) + {1\over c} \vvec \cross \Bvec(\xvec,t)\Bigr],
:::

where $\vvec=c\alphavec$. This is precisely the equation of motion for the kinetic momentum of a charged particle in classical relativity theory, which of course here is reinterpreted as an operator equation. In the classical theory $\pivec = m\gamma\vvec$, but as we have seen, in the quantum theory the velocity and momentum are not functions of one another.

The Heisenberg equations of motion are useful for finding the time-dependence of expectation values of wave packets, a subject we will return to when we reconsider the strange features of the velocity operator.

(sec-dirac-9)=

## The Nonrelativistic Limit of the Dirac Equation

An obvious requirement for any successful relativistic theory such as the Dirac equation is that it must reduce to the known, nonrelativistic theory when the velocity is small compared to the speed of light. We will now examine solutions of the Dirac equation in the low velocity limit, using a simple procedure that gives us the answers to order $(v/c)^2$. In {ref}`ch-foldyw`{} we will carry out a more systematic expansion of the Dirac equation in powers of $v/c$.

Instead of the condition $v\ll c$, we will write the energy as $mc^2$ plus a correction that is small compared to $mc^2$. This gives us the nonrelativistic limit of the positive energy solutions of the Dirac equation. Since the time dependence of the wave function $\psi$ is governed by the energy (energy eigenstates have the time dependence $e^{-iEt/\hbar}$), let us split off a factor of $e^{-imc^2t/\hbar}$ from the Dirac wave function $\psi$. This will remove the dominant part of the time-dependence of $\psi$ when the energy is $mc^2$ plus a small correction. Let us also break the 4-component spinor into two 2-component spinors $\phi$ and $\chi$, using the Dirac-Pauli representation. That is, let us substitute

:::{math}
:label: eq-dirac-42
\psi = e^{-imc^2t/\hbar}\begin{pmatrix}\phi\\\chi\\\end{pmatrix}
:::

into the Dirac equation, which we write in the Schr\"odinger form {eq}`eq-dirac-2` with the Hamiltonian {eq}`eq-dirac-35`, including the interaction with the electromagnetic field.

The left-hand side becomes

:::{math}
:label: eq-dirac-43
i\hbar\frac{\partial \psi}{\partial t} = e^{-imc^2t/\hbar}\Bigl[ mc^2 + i\hbar\pop{}{t}\Bigr]\begin{pmatrix}\phi\\\chi\\\end{pmatrix},
:::

while the right-hand side is

:::{math}
:label: eq-dirac-44
\begin{aligned}
(c\alphavec\cdot\pivec + q\Phi + mc^2\beta)\psi = e^{-imc^2t/\hbar}\Bigl[ c\begin{pmatrix}0 & \sigmavec\cdot\pivec \\ \sigmavec\cdot\pivec & 0 \\\end{pmatrix} + q\Phi + mc^2 \begin{pmatrix}1 & 0 \\ 0 & -1 \\\end{pmatrix} \Bigr] \begin{pmatrix}\phi\\\chi\\\end{pmatrix},
\end{aligned}

:::

where we have written out the matrices $\alphavec$ and $\beta$ explicitly. Cancelling the common phase and rearranging the terms slightly, the Dirac equation becomes a system of two coupled equations involving the 2-component spinors $\phi$ and $\chi$:

:::{math}
:label: eq-dirac-45a
\begin{aligned}
i\hbar\frac{\partial \phi}{\partial t} &= c(\sigmavec\cdot\pivec) \chi + q\Phi\phi,
\end{aligned}
:::

:::{math}
:label: eq-dirac-45b
\begin{aligned}
i\hbar\frac{\partial \chi}{\partial t} &= c(\sigmavec\cdot\pivec)\phi +q\Phi\chi -2mc^2\chi.
\end{aligned}
:::

This coupled system is exactly equivalent to the original Dirac equation.

In {eq}`eq-dirac-45b` there are three terms involving $\chi$. The term $q\Phi\chi$ is of the order of the nonrelativistic kinetic energy (times $\chi$), assuming that the kinetic and potential energies trade back and forth as is typical, for example, in the orbital motion of an electron in an atom. That is, $q\Phi\ll mc^2$, according to our assumptions. The term $i\hbar\partial\chi/\partial t$ must also be of the order of the nonrelativistic kinetic energy (times $\chi$), because we have already stripped off $mc^2$ from the time dependence that represents the total (relativistic) energy. Therefore both these terms are small compared to $-2mc^2\chi$, and can be neglected. Doing this, we can solve {eq}`eq-dirac-45b` for $\chi$ in terms of $\phi$,

:::{math}
:label: eq-dirac-46
\chi \approx {1\over 2mc} (\sigmavec\cdot\pivec)\phi.
:::

Now substituting this into {eq}`eq-dirac-45a`, we obtain

:::{math}
:label: eq-dirac-47
i\hbar\frac{\partial \phi}{\partial t} = {1\over 2m} (\sigmavec\cdot\pivec)^2\phi + q\Phi\phi.
:::

This equation is actually the Pauli equation. To see this, note that $\pivec$ commutes with $\sigmavec$, so

:::{math}
:label: eq-dirac-48
(\sigmavec\cdot\pivec)^2 = \sigma_i\pi_i\sigma_j\pi_j =\sigma_i\sigma_j\pi_i\pi_j =(\delta_{ij}+ i\epsilon_{ijk}\,\sigma_k)\pi_i\pi_j, = \pivec^2 + i\epsilon_{ijk}\,\sigma_k\pi_i\pi_j,
:::

where we use the properties of the Pauli matrices [see {eq}`eq-hilbert-145`]. Since the Levi-Civita symbol $\epsilon_{ijk}$ is antisymmetric in $i$ and $j$, the second term in this equation can be written,

:::{math}
:label: eq-dirac-49
{i\over 2} \epsilon_{ijk}\,\sigma_k (\pi_i\pi_j - \pi_j\pi_i) = {i\over 2} \epsilon_{ijk}\, \sigma_k[\pi_i,\pi_j] = -{\hbar q\over 2c}\,\epsilon_{ijk}\,\sigma_k\, \epsilon_{ij\ell}\,B_\ell = -{\hbar q\over c} \,\sigmavec\cdot\Bvec,
:::

where we use the commutator in {eq}`eq-dirac-36` and {eq}`eq-tensor-52`. Altogether, we have

:::{math}
:label: eq-dirac-50
(\sigmavec\cdot\pivec)^2 = \pivec^2 - {\hbar q\over c}\,\sigmavec\cdot\Bvec,
:::

so {eq}`eq-dirac-47` becomes

:::{math}
:label: eq-dirac-51
i\hbar\frac{\partial \phi}{\partial t} = \Bigl( {\pivec^2\over 2m} -\muvec\cdot\Bvec + q\Phi\Bigr)\phi,
:::

where

:::{math}
:label: eq-dirac-52
\muvec = {\hbar q \over 2mc} \sigmavec = g\Bigl({q \over 2mc}\Bigr)\Svec,
:::

where we have set $\Svec=(\hbar/2)\sigmavec$ for a spin-$\frac{1}{2}$ particle, and where $g=2$. See {eq}`eq-spinmagf-12`.

{eq}`eq-dirac-51` is the Pauli equation for a particle of spin $\frac{1}{2}$ (because $\phi$ has two components), with the interaction of the spin with the magnetic field included and with a $g$-factor of 2. As we have seen in {ref}`ch-spinmagf`, the $g$-factor of the electron is very close to 2. In Dirac's day the small corrections to the value 2 had not been seen experimentally and were not suspected theoretically, so as far as anyone knew the Dirac equation gave the exact $g$-factor of the electron. It is evident that Dirac's program for developing his wave equation, as described in these notes, is giving us a theory of the electron. Other particles of spin~$\frac{1}{2}$, such as the proton and neutron, with their “anomalous” magnetic moments, will require a modified development.

This is the first of a series of miraculous successes of the Dirac equation that we will see as we proceed. In the first place notice that in the nonrelativistic theory, if we want to include the interaction of the magnetic moment of the electron with a magnetic field, we must put the term $-\muvec\cdot\Bvec$ into the Hamiltonian by hand, based on our knowledge that this is the energy of interaction of a classical magnetic moment with a magnetic field. (And this classical interaction involves some subtleties that are completely skipped in most books. In general, the subject of magnetic energy is treated poorly in many books, with some common mistakes.) In the Dirac equation, however, we did not have to put this interaction in by hand, rather it followed automatically from the minimal assumptions we have made (the simplest representation of the Dirac algebra, and the minimal coupling prescription for the interaction with the electromagnetic field). Not only that, but we get the correct $g$-factor for the electron to a high degree of accuracy, while in the nonrelativistic theory the $g$-factor has to be taken as a measured parameter without theoretical support. For this reason the value $g=2$ is sometimes called the “Dirac” value, while other values are considered “anomalous”.

Although there remain some interpretational difficulties with the Dirac equation, including the negative energy solutions and some others we will discuss later, these successes are so striking that we continue with the theory to see where it will lead. The next step is to see how the Dirac equation transforms under Lorentz transformations.

\problems

(prob-dirac-1)=

**Problem \prbddirac-1.} The Dirac equation in two space dimensions. Suppose we lived in a world with two space dimensions ($x$ and $y$) and one time dimension.  Let $x^\mu = (ct,x,y)$, and otherwise use the obvious restrictions of ordinary relativity theory to two spatial dimensions (for example, $g_{\mu\nu.** 

:::{math}
:label: eq-dirac-53
B=\frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y}.
:::

More generally, true vectors in three dimensions become 2-vectors when restricted to two dimensions, but pseudo-vectors in three dimensions become (pseudo) scalars in two dimensions. You will find that in some respects the Dirac equation in two spatial dimensions is very similar to what was done in lecture in three spatial dimensions, and in other respects it is different.

\problempart{(a)} Carry out Dirac's program of finding a relativistic wave equation that is first order in both space and time. Show that the Dirac algebra of }$\alphavec=(\alpha_1,\alpha_2)$ and $\beta$ matrices can be satisfied by $2\times2$ Hermitian matrices. This is the simplest solution for the Dirac algebra in $2+1$ dimensional space-time. Thus, the Dirac spinor has two components. The solution is not unique, because you can change the basis (conjugate any solution with some unitary matrix to create another representation of the algebra), so let your primary solution be one in which $\beta$ is diagonal. Call this the “Dirac-Pauli” representation. Also compute the matrices $\gamma^\mu$ in the Dirac-Pauli representation. The Dirac-Pauli representation is most convenient for studying the nonrelativistic limit.

Now find a representation in which the matrices $\gamma^\mu$ are purely imaginary. See {eq}`eq-covariance-5` for the definition of the matrices $\gamma^\mu$. Call this the “Maiorana representation.” The Maiorana representation makes Lorentz transformations on the spinors look most simple.

\problempart{(b)} Write out the Dirac equation including minimal coupling to the electromagnetic field, and show that it possesses a positive definite probability density with an associated probability current that taken together satisfy the continuity equation.

\problempart{(c)} Work out the Heisenberg equations of motion for $\xvec$ and $\pivec=\pvec -(q/c)\Avec$.

(prob-dirac-2)=

**Problem (d).** 

:::{math}
:label: eq-dirac-54
\psi=e^{-imc^2t/\hbar} \begin{pmatrix} \phi \\ \chi \\\end{pmatrix},
:::

and assume that the energy is $E=mc^2 + \\textsmall$. Find an approximation giving $\chi$ in terms of $\phi$, and use it to obtain an effective Schr\"odinger equation for the upper component $\phi$. Is the resulting Schr\"odinger equation realistic for any problems in our real (3-dimensional) world?
