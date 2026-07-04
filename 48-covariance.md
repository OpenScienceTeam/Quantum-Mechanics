---
title: "48. Covariance of the Dirac Equation"
---
(ch-covariance)=

# 48. Covariance of the Dirac Equation

(sec-covariance-1)=

## Introduction

In accordance with the principle of relativity, physics must “look the same” in all Lorentz frames. This means that physical theories that are consistent with the principle of relativity must have the same form in all Lorentz frames, that is, they must be covariant. In this set of notes we examine the covariance of the Dirac equation.

In these notes we mainly deal with the Dirac wave function $\psi$, which is understood to be a four-component spinor. But occasional reference is made to the scalar Klein-Gordon wave function, which will be denoted by $\psi_{KG}$.

(sec-covariance-2)=

## Covariant Form of the Dirac Equation

We begin with the free particle. The Dirac equation, as developed in {ref}`ch-dirac`, is

:::{math}
:label: eq-covariance-1
i\hbar\frac{\partial \psi}{\partial t} = -i\hbar c\, \alphavec\cdot\del\psi + mc^2\beta\,\psi.
:::

The operator $\partial/\partial t$ on the left-hand side is not a Lorentz scalar, because the time $t$ represents just one component of the 4-vector $x^\mu=(ct,\xvec)$. The Dirac equation, as written, is not manifestly Lorentz covariant. Let us bring all the derivatives over to one side, and write the Dirac equation as

:::{math}
:label: eq-covariance-2
i\hbar c\Bigl(\frac{\partial \psi}{\partial (ct)} + \alphavec\cdot\del\psi\Bigr) =mc^2\beta\,\psi.
:::

To put this into covariant form, we multiply through by $\beta$, using $\beta^2=1$, to obtain

:::{math}
:label: eq-covariance-3
i\hbar c\Bigl(\beta\frac{\partial \psi}{\partial (ct)} + \beta\alphavec\cdot\del\psi\Bigr) = mc^2\psi.
:::

The constant operator on the right-hand side, $mc^2$, is a Lorentz scalar, while the operators

:::{math}
:label: eq-covariance-4
\partial_\mu = \pop{}{x^\mu} = \Bigl(\pop{}{(ct)}, \del\Bigr)
:::

that appear on the left-hand side transform as a covariant vector (see Appendix~\tensor). Therefore we guess that the coefficients that multiply $\partial_\mu$ on the left-hand side must transform as a contravariant 4-vector, so that the entire operator on the left-hand side will be a Lorentz scalar.

To bring this out notationally, we define

:::{math}
:label: eq-covariance-5
\gamma^0=\beta, \qquad \gamma^i = \beta\alpha_i,
:::

for $i=1,2,3$, so that the free particle Dirac equation can be written,

:::{math}
:label: eq-covariance-6
i\hbar \gamma^\mu \frac{\partial \psi}{\partial x^\mu} = mc\,\psi,
:::

after cancelling a factor of $c$. We have written the four matrices defined in {eq}`eq-covariance-5` as $\gamma^\mu$, $\mu=0,1,2,3$, which we can think of as a 4-vector of Dirac matrices, much as the Pauli matrices $\sigmavec$ constitute a 3-vector of matrices. If we introduce the covariant momentum operators,

:::{math}
:label: eq-covariance-7
p_\mu = i\hbar\pop{}{x^\mu} =i\hbar\Bigl( \pop{}{(ct)}, \del\Bigr)
:::

[see {eq}`eq-kleing-20`], then the free particle Dirac equation takes on the suggestive form,

:::{math}
:label: eq-covariance-8
(\gamma^\mu p_\mu -mc)\psi=0.
:::

The notation suggests that $\gamma^\mu p_\mu$ is a Lorentz scalar, but we will not have proven that until we see how and in what sense $\gamma^\mu$ constitutes a 4-vector. To do that, we will have to show that it transforms as a 4-vector under Lorentz transformations. Moreover, since $\gamma^\mu$ is a 4-vector of $4\times4$ matrices, not ordinary numbers, its transformation law will not be the same as that of the 4-vectors encountered in classical relativity theory, as discussed in Appendix~\tensor. Instead, as we shall see, it transforms by a four-dimensional generalization of the definition of a vector operator in quantum mechanics, which is discussed in {ref}`sec-transfop-4`.

To introduce the coupling with the electromagnetic field, we use the covariant version of the minimal coupling prescription {eq}`eq-dirac-16`,

:::{math}
:label: eq-covariance-9
p_\mu \to p_\mu -{q\over c} A_\mu,
:::

where $A^\mu$ is the 4-vector potential,

:::{math}
:label: eq-covariance-10
A^\mu=\begin{pmatrix}\Phi\\\Avec\\\end{pmatrix}, \qquad A_\mu=\begin{pmatrix}\Phi\\ -\Avec\\\end{pmatrix}.
:::

See also {ref}`sec-classmech-17`. This puts the Dirac equation for a particle interacting with the electromagnetic field into the form,

:::{math}
:label: eq-covariance-11
\Bigl(\gamma^\mu p_\mu -{q\over c} \gamma^\mu A_\mu -mc\Bigr)\psi=0.
:::

Contractions between $\gamma^\mu$ and ordinary 4-vectors such as $A_\mu$, or 4-vectors of operators such as $p_\mu$, are very common in the Dirac theory. Here is some notation for such contractions. Let $X^\mu$ be any 4-vector. Then we define

:::{math}
:label: eq-covariance-12
\Xslash=\gamma^\mu X_\mu,
:::

which is called the *Feynman slash*. When you see the Feynman slash, you must recognize that it is a $4\times4$ Dirac matrix, with components that are numbers, possibly with a space-time dependence, as in $\Aslash$, or operators, as in $\pslash$. In terms of this notation, the Dirac equation becomes

:::{math}
:label: eq-covariance-13
\Bigl(\pslash -{q\over c}\Aslash - mc\Bigr)\psi=0.
:::

This is regarded as the covariant version of the Dirac equation. It is equivalent to the Hamiltonian version, $i\hbar\partial\psi/\partial t=H\psi$, with $H$ given by {eq}`eq-dirac-17`.

The covariant version of the Dirac equation {eq}`eq-covariance-13` produces the Pauli equation {eq}`eq-dirac-1` in the nonrelativistic limit with $g=2$, as we showed in {ref}`sec-dirac-9`. And yet it is simpler in form than the Pauli equation, in spite of the extra notation. In fact, as we will see in a later set of notes, {eq}`eq-covariance-13` contains even more physics than the Pauli equation, for if it is expanded to fourth order in $v/c$ it produces all the fine structure corrections we saw in {ref}`ch-finestruc`.

(sec-covariance-3)=

## The Matrices $\gamma^\mu$

The matrices $\gamma^\mu$, defined by {eq}`eq-covariance-5`, constitute an alternative version of the Dirac matrices $\alphavec$ and $\beta$, useful when we wish to reveal the covariant aspects of the Dirac equation. All the properties of the $\alphavec$ and $\beta$ matrices can be converted into properties of the matrices $\gamma^\mu$. Here we list some of them.

First, there are the values of the matrices. In the usual Dirac-Pauli representation, they are

:::{math}
:label: eq-covariance-14
\begin{aligned}
\gamma^0 = \beta = \begin{pmatrix}1 & 0 \\ 0 & -1 \\\end{pmatrix}, \qquad \gamma^i = \beta\alpha_i = \begin{pmatrix}0 & \sigma_i \\ -\sigma_i & 0 \\\end{pmatrix}, \qquad \\text{Dirac-Pauli}
\end{aligned}

:::

while in the Weyl representation they are

:::{math}
:label: eq-covariance-15
\begin{aligned}
\gamma^0=\beta=\begin{pmatrix}0 & -1\\ -1 & 0\\\end{pmatrix}, \qquad \gamma^i = \beta\alpha_i = \begin{pmatrix}0 & \sigma_i \\ -\sigma_i & 0\\\end{pmatrix}. \qquad \\text{Weyl}
\end{aligned}

:::

Next there are the Hermiticity properties. Recall that $\alphavec$ and $\beta$ are Hermitian. This implies that $\gamma^0$ is Hermitian, while $\gamma^i$, $i=1,2,3$, are anti-Hermitian. This is easily proved using the properties of the $\alphavec$ and $\beta$ matrices, for example,

:::{math}
:label: eq-covariance-16
\begin{aligned}
(\gamma^0)^\dagger &= \beta^\dagger = \beta = \gamma^0, \\
(\gamma^i)^\dagger &= (\beta\alpha_i)^\dagger = \alpha_i\beta = -\beta\alpha_i = -\gamma^i, \\

\end{aligned}
:::

where we have used the anticommutation relation, $\{\alpha_i,\beta\}=0$ and $\beta^2=1$.

Finally, there are the anticommutation properties of the $\gamma^\mu$, which are easily derived from those of $\alphavec$ and $\beta$. Explicitly, we have

:::{math}
:label: eq-covariance-17
\begin{aligned}
\{\gamma^0,\gamma^0\} &= \{\beta,\beta\}=2, \\
\{\gamma^0,\gamma^i\} &= \{\beta,\beta\alpha_i\} =\beta^2\alpha_i + \beta\alpha_i\beta=\alpha_i-\alpha_i=0, \\
\{\gamma^i,\gamma^j\} &= \{\beta\alpha_i,\beta\alpha_j\} =\beta\alpha_i\beta\alpha_j + \beta\alpha_j\beta\alpha_i =-\alpha_i\alpha_j-\alpha_j\alpha_i=-2\delta_{ij}, \\

\end{aligned}
:::

where again we use the anticommutation relations {eq}`eq-dirac-8`.

We can summarize the anticommutation relations of the matrices $\gamma^\mu$ by writing,

:::{math}
:label: eq-covariance-18
\boxed{\{\gamma^\mu,\gamma^\nu\} = 2g^{\mu\nu}.}
:::

Here it is understood that the right hand side multiplies the identity matrix, usually denoted by 1 in the Dirac theory. This equation looks covariant, and indeed we will see that it is, once we have worked out the transformation properties of the matrices $\gamma^\mu$. {eq}`eq-covariance-18` is a compact, covariant form of the Dirac algebra first presented in {eq}`eq-dirac-8`, which as we recall arose from the demand that the relativisitc energy-momentum relations should be satisfied by free particle solutions of the Dirac equation. It is used frequently in the Dirac theory.

We make a remark on the positions of the spatial index $i$ in $\gamma^i$ and $\alpha_i$. We use an upper (superscript) position on $\gamma^i$ because this is seen as the spatial components of a contravariant vector $\gamma^\mu$ (it is $\gamma^{\mu\to i}$, in the notation discussed in {ref}`sec-tensor-20`). On the other hand, $\alphavec$ is not the spatial components of any 4-vector (there is no $\alpha^0$), rather $\alphavec$ is seen as an object that is intrinsically a 3-vector, so we just use lower indices for its components. The case of the velocity vector is similar; we write simply $v_i$ for the usual components of the velocity vector $\vvec$, since this is never the spatial part of a 4-vector [see the comment after {eq}`eq-tensor-9`, and note that in the Dirac theory, $\vvec = c\alphavec$].

(sec-covariance-4)=

## Transformation of the Dirac Wave Function

We turn to the transformation properties of the Dirac wave function $\psi$ under Lorentz transformations. We begin by guessing the form of the transformation law, by analogy with the transformation laws for different types of fields under ordinary rotations, as well as certain types of fields under Lorentz transformations.

The transformation laws for scalar and vector fields in 3-dimensional space under ordinary rotations was reviewed in {ref}`sec-lorentz-11`. If $S(\xvec)$ is a scalar field and $\Rmat$ specifies a rotation, then the rotated field $S'$ is given in terms of the original field $S$ by

:::{math}
:label: eq-covariance-19
S'(\xvec) = S\bigl(\Rmat^{-1}\xvec\bigr).
:::

See {eq}`eq-lorentz-85`. This transformation law applies in particular to the wave function of a spin-0 particle, as explained in {ref}`sec-orbamsph-2`. See {eq}`eq-orbamsph-13`. Next, if $\Evec(\xvec)$ is a vector field, then the rotated field is given by

:::{math}
:label: eq-covariance-20
\Evec'(\xvec)=\Rmat\Evec\bigl(\Rmat^{-1}\xvec\bigr).
:::

See {eq}`eq-lorentz-87`. Next, the case of the wave function of a particle of spin~$s$ was treated in Prob. {ref}`prob-jjcouple-1`(a). If $\psi(\xvec)$ is the $2s+1$-component spinor of a particle of spin~$s$ and $\Rmat$ is a rotation, then the rotated wave function is

:::{math}
:label: eq-covariance-21
\psi'(\xvec) = D^s(\Rmat)\psi\bigl(\Rmat^{-1}\xvec\bigr)
:::

(this is the solution to the problem). Here $D^s$ is the $(2s+1)\times(2s+1)$ rotation matrix, as explained in {ref}`ch-repsamos`, and it is understood that this matrix multiplies the spinor $\psi$. The rotation matrices satisfy the representation property,

:::{math}
:label: eq-covariance-22
D^s(\Rmat_1) D^s(\Rmat_2) = \pm D^s(\Rmat_1\Rmat_2),
:::

where the $\pm$ sign only applies in the case of half-integer $s$. See {eq}`eq-repsamos-72`--{eq}`eq-repsamos-74` and the discussion of double-valued representations in {ref}`sec-spinrot-9`.

We see that in all cases (scalar, vector, spinor), the rotated field at point $\xvec$ is expressed in terms of the original field at the inverse rotated point $\Rmat^{-1}\xvec$, while the value of the field is transformed by the appropriate rotation matrix (no rotation at all for a scalar, the classical rotation matrix $\Rmat$ for a vector field, and the $D^s$-matrix for a spinor field of spin $s$).

In special relativity we consider fields on space-time, and subject them to Lorentz transformations. Letting $x$ stand for the four space-time coordinates $x^\mu$ or $(\xvec,t)$, the transformation rule for a scalar field under a Lorentz transformation $\Lambda^\mu{}_\nu$ is

:::{math}
:label: eq-covariance-23
S'(x) = S\bigl(\Lambda^{-1}x\bigr).
:::

See {eq}`eq-lorentz-88`. The Klein-Gordon wave function $\psi_{KG}$ is a scalar field that represents a spin-0 particle, and it transforms according to this rule,

:::{math}
:label: eq-covariance-24
\psi'_KG(x) = \psi_KG\bigl(\Lambda^{-1}x\bigr).
:::

In the case of a contravariant vector field $X^\mu$, the transformation law is

:::{math}
:label: eq-covariance-25
X^{\prime\,\mu}(x) = \Lambda^\mu{}_\nu \, X^\nu\bigl(\Lambda^{-1}x\bigr).
:::

In these cases the Lorentz transformed field at space-time point $x$ is expressed in terms of the original field at space-time point $\Lambda^{-1}x$, while the value of the field transforms by the appropriate matrix (none at all for a scalar, and $\Lambda^\mu{}_\nu$ for a contravariant vector field).

These examples suggest that the Dirac wave function $\psi$ should transform under Lorentz transformations according to

:::{math}
:label: eq-covariance-26
\psi'(x) = D(\Lambdamat)\psi\bigl(\Lambda^{-1}x\bigr),
:::

where $D(\Lambdamat)$ is some kind of $4\times4$ matrix that acts on the spin part of $\psi$. We know that the Dirac equation is giving us the relativistic quantum mechanics of a spin-$\frac{1}{2}$ particle, and we know that when the nonrelativistic wave function of a spin-$\frac{1}{2}$ particle is rotated the matrix $D^{1/2}$ appears as in {eq}`eq-covariance-21`. Since rotations are special cases of Lorentz transformations, we must expect some kind of spin matrix as in {eq}`eq-covariance-26` when the Dirac wave function is subjected to a Lorentz transformation. Moreover, we expect that the matrices $D(\Lambdamat)$ should satisfy the representation property,

:::{math}
:label: eq-covariance-27
D(\Lambdamat_1)D(\Lambdamat_2) = \pm D(\Lambdamat_1\Lambdamat_2),
:::

since this means that if we apply a Lorentz transformation $\Lambdamat_2$ to a Dirac wave function, then a second one $\Lambdamat_1$, the effect is the same as applying the single Lorentz transformation $\Lambdamat_1\Lambdamat_2$. That is, the matrices $D(\Lambdamat)$ should form a representation of the Lorentz group. We include a $\pm$ sign in {eq}`eq-covariance-27` because we know this sign is necessary in the case of ordinary rotations of a spin-$\frac{1}{2}$ particle, and because rotations are special cases of Lorentz transformations.

(sec-covariance-5)=

## The Space-Time Part of the Transformation

Let us concentrate first on the space-time part of the transformation {eq}`eq-covariance-26`, to see if it makes sense. Consider an eigenfunction of energy and momentum, that is, an eigenfunction of the free-particle Dirac equation. We write this as

:::{math}
:label: eq-covariance-28
\psi(x) \sim e^{i(\pvec\cdot\xvec-Et)/\hbar},
:::

where $\sim$ means that we are concentrating on the space-time dependence of the wave function and ignoring the spin. (If we were talking about the Klein-Gordon wave function then we could replace $\sim$ by $=$.) We can put this into covariant form by using

:::{math}
:label: eq-covariance-29
x^\mu=\begin{pmatrix}ct\\\xvec\\\end{pmatrix}, \qquad p^\mu=\begin{pmatrix}E/c\\\pvec\\\end{pmatrix},
:::

so that

:::{math}
:label: eq-covariance-30
p_\mu x^\mu = Et-\pvec\cdot\xvec,
:::

and

:::{math}
:label: eq-covariance-31
\psi(x) \sim \exp\Bigl(-{i\over\hbar}p_\mu x^\mu\Bigr) =\exp\Bigl[-{i\over\hbar}(p\cdot x)\Bigr],
:::

where we use the notation of {eq}`eq-lorentz-104` for the scalar product of two 4-vectors. Now subjecting this to a Lorentz transformation specified by $\Lambdamat$ and using the transformation law {eq}`eq-covariance-26`, this becomes

:::{math}
:label: eq-covariance-32
\psi'(x) \sim \exp\Bigl[-{i\over\hbar}p\cdot(\Lambda^{-1}x)\Bigr].
:::

But by {eq}`eq-lorentz-105` the scalar product in the exponent can also be written $p'\cdot x$ where $p'=\Lambda p$, or

:::{math}
:label: eq-covariance-33
p^{\prime\,\mu} = \Lambda^\mu{}_\nu\, p^\nu.
:::

The momentum $p^{\prime\,\mu}$ is the Lorentz transformed version of the original momentum $p^\mu$, in the active sense. That is, when we boost and/or rotate a free-particle Dirac eigenfunction according to {eq}`eq-covariance-26`, the energy-momentum 4-vector of the new wave function is the boosted and/or rotated version of the original energy-momentum 4-vector. This is just what we want.

(sec-covariance-6)=

## The Spin Part of the Lorentz Transformation

The spin part of the Lorentz transformation is specified by the as-yet-unknown matrices $D(\Lambdamat)$. We obtain a condition on these by requiring that the Dirac equation be covariant. For this it suffices to work with the free particle. Suppose $\psi(x)$ is a free-particle solution, that is, it satisfies

:::{math}
:label: eq-covariance-34
i\hbar\gamma^\mu \,\frac{\partial \psi(x)}{\partial x^\mu} = mc\,\psi(x).
:::

Let us demand that the Lorentz-transformed wave function $\psi'(x) = D(\Lambdamat) \psi(\Lambdamat^{-1}x)$ also satisfy the free-particle Dirac equation, that is, let us demand that Lorentz transformations map free particle solutions into other free particle solutions. Then we have

:::{math}
:label: eq-covariance-35
i\hbar\gamma^\mu D(\Lambdamat) \pop{\psi(\Lambdamat^{-1}x)}{x^\mu} = mc\, D(\Lambdamat) \psi(\Lambdamat^{-1}x).
:::

In this formula, space-time indices are indicated explicitly, for example, $\gamma^\mu \partial/\partial x^\mu$, but spinor indices are not. For example, $\psi$ is a 4-component column spinor and $D(\Lambdamat)$ is a $4\times4$ matrix, and matrix multiplication is implied. We have pulled the $\partial/\partial x^\mu$ past $D(\Lambdamat)$ since the latter depends on $\Lambdamat$ but not on $x$.

Let us write

:::{math}
:label: eq-covariance-36
y^\mu = (\Lambda^{-1})^\mu{}_\nu \, x^\nu
:::

and multiply {eq}`eq-covariance-35` by $D(\Lambdamat)^{-1}$ to clear the $D(\Lambdamat)$ on the right hand side. Then we get

:::{math}
:label: eq-covariance-37
i\hbar \, D(\Lambdamat)^{-1} \gamma^\mu D(\Lambdamat) \frac{\partial \psi(y)}{\partial x^\mu} = mc\,\psi(y).
:::

But since $\psi$ satisfies the Dirac equation, we have

:::{math}
:label: eq-covariance-38
i\hbar\gamma^\nu\, \frac{\partial \psi(y)}{\partial y^\nu} = mc\,\psi(y)
:::

which is just {eq}`eq-covariance-34` with $x\to y$ and $\mu\to\nu$. We also have

:::{math}
:label: eq-covariance-39
\frac{\partial \psi(y)}{\partial x^\mu} = \frac{\partial \psi(y)}{\partial y^\nu} \frac{\partial y^\nu}{\partial x^\mu} = \frac{\partial \psi(y)}{\partial y^\nu} (\Lambda^{-1})^\nu{}_\mu.
:::

Now combining {eq}`eq-covariance-37` and {eq}`eq-covariance-38` and cancelling $i\hbar$, we get

:::{math}
:label: eq-covariance-40
D(\Lambdamat)^{-1} \gamma^\mu D(\Lambdamat) \frac{\partial \psi(y)}{\partial y^\nu} (\Lambda^{-1})^\nu{}_\mu = \gamma^\nu \frac{\partial \psi(y)}{\partial y^\nu}.
:::

But $\partial\psi(y)/\partial y^\nu$ is arbitrary (by choosing different free particle solutions we can make it anything we want), so

:::{math}
:label: eq-covariance-41
D(\Lambdamat)^{-1} \gamma^\mu D(\Lambdamat)\, (\Lambda^{-1})^\nu{}_\mu = \gamma^\nu,
:::

or, by multiplying by $\Lambdamat$ to clear the $\Lambdamat^{-1}$ on the left hand side,

:::{math}
:label: eq-covariance-42
\boxed{D(\Lambdamat)^{-1} \gamma^\mu D(\Lambdamat) = \Lambda^\mu{}_\nu \, \gamma^\nu.}
:::

This result is important because it is the fundamental relation that the matrices $D(\Lambdamat)$ must satisfy. In fact, it allows those matrices to be determined, as we shall see. It is also a statement that the 4-vector of matrices $\gamma^\mu$ actually transforms as a 4-vector. For comparison recall the adjoint formula for rotations of a spin-$\frac{1}{2}$ particle,

:::{math}
:label: eq-covariance-43
U(\Rmat)^\dagger \sigmavec U(\Rmat) = \Rmat \sigmavec
:::

(see {eq}`eq-spinrot-29`. This is a special case of the transformation law for a vector operator, that is, the transformation law for a 3-vector under spatial rotations. See also {eq}`eq-transfop-14` for the general case of a vector operator.

We remark that had we been using the passive point of view, then our requirement that Lorentz transformations map free particle solutions of the Dirac equation into other free particle solutions would become the requirement that the free-particle Dirac equation have the same form in all Lorentz frames.

(sec-covariance-7)=

## The Matrices $D(\Lambdamat)$ for Infinitesimal Lorentz Transformations

The case of infinitesimal Lorentz transformations is especially important. To see why, note that if {eq}`eq-covariance-42` is valid for two Lorentz transformations,

:::{math}
:label: eq-covariance-44
\begin{aligned}
D(\Lambdamat_1)^{-1} \gamma^\mu D(\Lambdamat_1) &= (\Lambda_1)^\mu{}_\nu \, \gamma^\nu \\
D(\Lambdamat_2)^{-1} \gamma^\mu D(\Lambdamat_2) &= (\Lambda_2)^\mu{}_\nu \, \gamma^\nu, \\

\end{aligned}
:::

then it is true for their product $\Lambdamat_1\Lambdamat_2$. We see this by combining {eq}`eq-covariance-44` to get

:::{math}
:label: eq-covariance-45
\begin{aligned}
D(\Lambdamat_2^{-1})D(\Lambdamat_1^{-1})\gamma^\mu D(\Lambdamat_1)D(\Lambdamat_2) &= D(\Lambdamat_2^{-1}) (\Lambda_1)^\mu{}_\nu \, \gamma^\nu D(\Lambdamat_2) = (\Lambda_1)^\mu{}_\nu \, D(\Lambdamat_2^{-1}) \gamma^\nu D(\Lambdamat_2) \\
&= (\Lambda_1)^\mu{}_\nu \, (\Lambda_2)^\nu{}_\sigma \gamma^\sigma = (\Lambda_1 \Lambda_2)^\mu{}_\sigma \, \gamma^\sigma.
\end{aligned}
:::

But according to the representation law {eq}`eq-covariance-27`, the left-hand side of {eq}`eq-covariance-45` can be written

:::{math}
:label: eq-covariance-46
D\bigl((\Lambdamat_1\Lambdamat_2)^{-1}\bigr)\gamma^\mu D(\Lambdamat_1 \Lambdamat_2),
:::

where the $\pm$ sign cancels out. This proves the assertion.

Thus, if we can find $D(\Lambdamat)$ satisfying {eq}`eq-covariance-42` for infinitesimal Lorentz transformations, and if we use the representation property {eq}`eq-covariance-27` to build up $D(\Lambdamat)$ for finite, proper Lorentz transformations as products of infinitesimal ones, then the finite ones will automatically satisfy {eq}`eq-covariance-42`. We recall that any proper Lorentz transformation can be built up a product of infinitesimal ones (see the end of {ref}`sec-lorentz-3`). This simplifies the problem of finding the matrices $D(\Lambdamat)$ considerably.

The general form of an infinitesimal Lorentz transformation was presented in {eq}`eq-lorentz-63`. It is

:::{math}
:label: eq-covariance-47
\Lambdamat = \Imat + {1\over2} \theta_{\mu\nu} \Jmat^{\mu\nu},
:::

where $\theta_{\mu\nu}$ is an antisymmetric tensor or matrix of small numbers, specifying the infinitesimal Lorentz transformation, and where $\Jmat^{\mu\nu}$ is an antisymmetric “tensor” of $4\times4$ matrices. We recall that for fixed value of $\mu$ and $\nu$, $\Jmat^{\mu\nu}$ is a $4\times4$ matrix, that is, the $\mu$ and $\nu$ are labels of the matrix, not its component indices. The components are $(\Jmat^{\mu\nu})^\alpha{}_\beta$, and are given by {eq}`eq-lorentz-64`. Because $\theta_{\mu\nu}=-\theta_{\nu\mu}$, there are only 6 independent components of $\theta_{\mu\nu}$, which are obtained if we restrict the indices to $\mu<\nu$. Thus we can think of the infinitesimal $\Lambdamat$ in {eq}`eq-covariance-47` as functions of these six independent $\theta_{\mu\nu}$.

The $D$-matrix representing this infinitesimal Lorentz transformation, $D(\Lambdamat)$, must also therefore be a function of the six independent $\theta_{\mu\nu}$. Let us expand this $D(\Lambdamat)$ out to first order in the independent $\theta_{\mu\nu}$,

:::{math}
:label: eq-covariance-48
D(\Lambdamat) = D(\theta_{\mu\nu}) = 1 + \sum_{\mu<\nu} \theta_{\mu\nu} \frac{\partial D}{\partial \theta_{\mu\nu}}(0).
:::

Now we define matrices $\sigma^{\mu\nu}$ for $\mu<\nu$ by

:::{math}
:label: eq-covariance-49
\frac{\partial D}{\partial \theta_{\mu\nu}}(0) = -{i\over2} \, \sigma^{\mu\nu},
:::

and then define $\sigma^{\mu\nu} = - \sigma^{\nu\mu}$ for $\mu\ge\nu$. Since the derivatives are evaluated at $\theta_{\mu\nu}=0$, the matrices $\sigma^{\mu\nu}$ are independent of $\theta_{\mu\nu}$, that is, they are constants. The factor $-i/2$ is conventional, but it is intended to make the answers come out in familiar form for rotations of nonrelativistic spinors, which we know about already. The matrices $\sigma^{\mu\nu}$ form an antisymmetric “tensor” of $4\times4$ Dirac matrices (that is, matrices that act on spin space). This is a generalization of the 4-vector of Dirac matrices $\gamma^\mu$. Later we will see that $\sigma^{\mu\nu}$ actually transforms as a tensor under Lorentz transformations, in a generalization of {eq}`eq-covariance-42`. We must find the explicit form of the matrices $\sigma^{\mu\nu}$ to determine $D(\Lambdamat)$ for infinitesimal Lorentz transformations.

We extend the sum in {eq}`eq-covariance-48` to all $\mu,\nu$, so that

:::{math}
:label: eq-covariance-50
D(\Lambdamat) = 1-{i\over 4} \, \theta_{\mu\nu}\, \sigma^{\mu\nu}.
:::

To determine the matrices $\sigma^{\mu\nu}$, we substitute the infinitesimal Lorentz transformation {eq}`eq-covariance-47` or its spinor representative {eq}`eq-covariance-50` into the fundamental transformation law for $\gamma^\mu$, {eq}`eq-covariance-42`, switching indices $\mu\nu \to \alpha\beta$ on $\sigma$ to avoid collision of indices. This gives

:::{math}
:label: eq-covariance-51
\Bigl(1+{i\over4}\theta_{\alpha\beta}\sigma^{\alpha\beta} \Bigr) \gamma^\mu \Bigl(1-{i\over4}\theta_{\alpha\beta} \sigma^{\alpha\beta}\Bigr) = \Bigl[\Imat + {1\over2}\theta_{\alpha\beta}\, \Jmat^{\alpha\beta}\Bigr]^\mu{}_\nu \, \gamma^\nu,
:::

or, on multiplying this out and keeping terms that are first order in $\theta_{\alpha\beta}$,

:::{math}
:label: eq-covariance-52
{i\over4}\theta_{\alpha\beta} [\sigma^{\alpha\beta}, \gamma^\mu] = {1\over2} \theta_{\alpha\beta} (g^{\mu\alpha} \gamma^\beta - g^{\mu\beta}\gamma^\alpha),
:::

where we have used {eq}`eq-lorentz-64` for the components of $\Jmat^{\alpha\beta}$. The antisymmetric but otherwise arbitrary coefficients $\theta_{\alpha\beta}$ on both sides are contracted with objects antisymmetric in $(\alpha\beta)$, so we can cancel $\theta_{\alpha\beta}$ to obtain

:::{math}
:label: eq-covariance-53
{i\over4}[\sigma^{\alpha\beta},\gamma^\mu] = {1\over2} (g^{\mu\alpha} \gamma^\beta - g^{\mu\beta} \gamma^\alpha).
:::

This equation must be solved for $\sigma^{\alpha\beta}$.

The notation suggests that $\sigma^{\alpha\beta}$ transforms as a tensor under Lorentz transformations. We guess that that is true. We already know that $\gamma^\mu$ transforms as a 4-vector under Lorentz transformations, in the sense of {eq}`eq-covariance-42`. This implies that $\gamma^\alpha\gamma^\beta$ (the product of two $\gamma$-matrices, another $4\times4$ spin matrix) transforms as a second rank tensor under Lorentz transformations, that is, that

:::{math}
:label: eq-covariance-54
D(\Lambdamat^{-1})\gamma^\alpha\gamma^\beta D(\Lambdamat) = \Lambda^\alpha{}_\sigma \, \Lambda^\beta{}_\tau \gamma^\sigma \gamma^\tau.
:::

This fact will be left as a easy exercise. But $\gamma^\alpha \gamma^\beta$ is not antisymmetric, in fact, it has a nonvanishing symmetric part given by the fundamental anticommutation relations {eq}`eq-covariance-18`. However its antisymmetric part is an antisymmetric, second rank tensor of Dirac matrices, so it is a good guess that it must be the same as $\sigma^{\alpha\beta}$ to within a multiplicative constant.

That is, let us guess that $\sigma^{\alpha\beta} = k(\gamma^\alpha\gamma^\beta - \gamma^\beta\gamma^\alpha)= k[\gamma^\alpha,\gamma^\beta]$ for some constant $k$. Substituting this into {eq}`eq-covariance-53` and using the anticommutation relations {eq}`eq-covariance-18`, we find after some algebra that it works with $k=i/2$. Altogether, we find

:::{math}
:label: eq-covariance-55
\boxed{\sigma^{\mu\nu} = {i\over2} [\gamma^\mu,\gamma^\nu],}
:::

switching back to indices $\mu,\nu$. This is the explicit solution for the matrices that appear in $D(\Lambda)$ for an infinitesimal Lorentz transformation, as shown in {eq}`eq-covariance-50`.

The matrices $\sigma^{\mu\nu}$ are considered the *generators* of the Dirac representation $D(\Lambdamat)$ of Lorentz transformations. They are analogous to the Pauli matrices $\sigmavec$ of the nonrelativistic theory, which play as similar role as the generators of spin rotations for a spin-$\frac{1}{2}$ particle. That is, an infinitesimal rotation matrix for a spin-$\frac{1}{2}$ particle is given by

:::{math}
:label: eq-covariance-56
U({\hat{\mathbf{n}}},\theta) = 1-{i\over2}\theta{\hat{\mathbf{n}}}\cdot\sigmavec = 1-{i\over2} \thetavec\cdot\sigmavec,
:::

where $\thetavec=\theta {\hat{\mathbf{n}}}$ is a vector of small angles specifying the infinitesimal rotation. This is discussed in {ref}`ch-spinrot`, and {eq}`eq-covariance-56` is a small-angle version of {eq}`eq-spinrot-27`. {eq}`eq-covariance-56` in the nonrelativistic Pauli theory may be compared to {eq}`eq-covariance-50` in the relativistic Dirac theory.

The matrices $\sigma^{\mu\nu}$ are a new set of $4\times4$ Dirac matrices, in addition to $\gamma^\mu$. As the notation indicates, $\sigma^{\mu\nu}$ transforms as a second rank tensor, in the sense of

:::{math}
:label: eq-covariance-57
D(\Lambdamat^{-1}) \sigma^{\mu\nu} D(\Lambdamat) = \Lambda^\mu{}_\alpha \, \Lambda^\nu{}_\beta \, \sigma^{\alpha\beta},
:::

as follows from {eq}`eq-covariance-54` and {eq}`eq-covariance-55`.

(sec-covariance-8)=

## $D(\Lambdamat)$ for Pure Rotations

Let us specialize to the case of pure rotations, which is summarized by {eq}`eq-lorentz-68`, {eq}`eq-lorentz-70`, {eq}`eq-lorentz-72`, {eq}`eq-lorentz-74` and {eq}`eq-lorentz-75`. In this case, of the six $\theta_{\mu\nu}$ we have $\theta_{0i}=0$. As for the remaining three components $\theta_{ij}$, we express these in terms of a 3-vector of angles $\theta_i$ by $\theta_i=(1/2) \epsilon_{ijk}\, \theta_{jk}$, or its inverse, $\theta_{ij} = \epsilon_{ijk}\, \theta_k$. The vector of small angles $\theta_i$ is related to the axis and angle of the infinitesimal rotation by $\thetavec=\theta {\hat{\mathbf{n}}}$, that is, $\theta = |\thetavec|$ and ${\hat{\mathbf{n}}}=\thetavec/\theta$. Then the Dirac $D$-matrix for an infinitesimal rotation can be written,

:::{math}
:label: eq-covariance-58
D({\hat{\mathbf{n}}},\theta) = 1 -{i\over4} \theta_{ij} \, \sigma^{ij} = 1- {i\over4} \epsilon_{ijk} \, \sigma^{ij} \, \theta_k = 1-{i\over2} \Sigma_k\,\theta_k,
:::

where we define

:::{math}
:label: eq-covariance-59
\Sigma_i = {1\over2} \epsilon_{ijk}\, \sigma^{jk}.
:::

In this notation we can also write the infinitesimal rotation as

:::{math}
:label: eq-covariance-60
D({\hat{\mathbf{n}}},\theta) = 1 -{i\over2} \theta {\hat{\mathbf{n}}}\cdot\Sigmavec =1-{i\over2}\thetavec\cdot\Sigmavec,
:::

which should be compared to {eq}`eq-covariance-56` in the nonrelativistic theory. The formulas look the same except for $\sigmavec\to\Sigmavec$; of course, $\sigmavec$ is a vector of $2\times2$ matrices, while $\Sigmavec$ is a vector of $4\times4$ matrices.

The vector of Dirac matrices $\Sigmavec$ is a new set to be added to the collection we have so far. The menagerie of Dirac matrices can be divided into those that are useful in a $3+1$-description of the theory, and those that are useful in a covariant description. The former set includes $\alphavec$, $\beta$, and $\Sigmavec$. We put a lower index on the components $\Sigma_i$ of $\Sigmavec$ for the same reasons we did on $\alpha_i$. The set of Dirac matrices useful in a covariant description includes $\gamma^\mu$, $\sigma^{\mu\nu}$ and one more to be added later.

As for the matrices $\Sigmavec$, they can be worked out by evaluating the commutators in the definition {eq}`eq-covariance-55` and using {eq}`eq-covariance-14`. Since the matrices $\gamma^i$ are the same in both the Dirac-Pauli and Weyl representations, the answers are the same in both representations. We find

:::{math}
:label: eq-covariance-61
\begin{aligned}
\Sigmavec=\begin{pmatrix}\sigmavec & 0 \\  0 & \sigmavec\end{pmatrix} \qquad \\text{Dirac-Pauli and Weyl}.
\end{aligned}

:::

We can now find the Dirac $D$-matrices for rotations of any finite angle, by composing rotations by an infinitesimal angle. When $\theta$ is not small we write

:::{math}
:label: eq-covariance-62
D({\hat{\mathbf{n}}},\theta) = \bigl[D\bigl({\hat{\mathbf{n}}},{\theta\over N}\bigr)\bigr]^N = \lim_{N\to\infty} \Bigl[1-{i\over2} {\theta\over N} {\hat{\mathbf{n}}}\cdot\Sigmavec \Bigr]^N = \exp\Bigl(-{i\over2}\theta{\hat{\mathbf{n}}}\cdot\Sigmavec \Bigr),
:::

where we use a matrix version of the limit {eq}`eq-spatialdof-42`. Another method of building up finite rotations out of infinitesimal ones is to use a differential equation, as in Secs. {ref}`sec-classrot-9` and {ref}`sec-spinrot-5`.

If we use the explicit form {eq}`eq-covariance-61` for $\Sigmavec$, we obtain the Dirac rotation matrices in the form

:::{math}
:label: eq-covariance-63
\begin{aligned}
D({\hat{\mathbf{n}}},\theta) = \begin{pmatrix} U({\hat{\mathbf{n}}},\theta) & 0 \\  0 & U({\hat{\mathbf{n}}},\theta) \\\end{pmatrix} \qquad \\text{Dirac-Pauli and Weyl},
\end{aligned}

:::

where $U({\hat{\mathbf{n}}},\theta)$ is the $2\times2$ rotation matrix for spin-$\frac{1}{2}$ particles, that is,

:::{math}
:label: eq-covariance-64
U({\hat{\mathbf{n}}},\theta) = \exp\Bigl(-i{\theta\over2}{\hat{\mathbf{n}}}\cdot\sigmavec\Bigr) =\cos{\theta\over2} - i({\hat{\mathbf{n}}}\cdot\sigmavec)\sin{\theta\over2}
:::

(this is {eq}`eq-spinrot-27`. We see that to subject a Dirac 4-component spinor to a purely spatial rotation, we rotate both the upper and lower 2-component spinors by the nonrelativistic rotation matrix for a spin-$\frac{1}{2}$ particle. This is true in both the Dirac-Pauli and Weyl representations.

(sec-covariance-9)=

## $D(\Lambda)$ for Pure Boosts

The case of pure boosts is summarized by {eq}`eq-lorentz-69`, {eq}`eq-lorentz-71`, {eq}`eq-lorentz-73`, {eq}`eq-lorentz-76` and {eq}`eq-lorentz-77`. In this case, of the six independent $\theta_{\mu\nu}$, the three parameters contained in $\theta_{ij}$ vanish leaving the three $\theta_{0i}$ to parameterize the boost. We write $\lambda_i = \theta_{0i}$ for these parameters, the components of a boost vector $\lambdavec$ with rapidity $\lambda=|\lambdavec|$ and boost axis ${\hat{\mathbf{b}}}=\lambdavec/\lambda$. The correction term in the infinitesimal $D$-matrix in {eq}`eq-covariance-50` is

:::{math}
:label: eq-covariance-65
-{i\over4}\theta_{\mu\nu} \sigma^{\mu\nu} = -{i\over4} (\theta_{0i}\sigma^{0i} + \theta_{i0} \sigma^{i0}) = -{i\over2} \theta_{0i}\sigma^{0i} = -{i\over2} \lambda_i \sigma^{0i}.
:::

But

:::{math}
:label: eq-covariance-66
\sigma^{0i} = {i\over2} [\gamma^0,\gamma^i] = {i\over2}[\beta,\beta\alpha_i] = {i\over2}(\beta^2\alpha_i - \beta\alpha_i\beta)= i\alpha_i,
:::

so for infinitesimal boosts we have

:::{math}
:label: eq-covariance-67
D({\hat{\mathbf{b}}},\lambda) = 1+{1\over2}\lambdavec\cdot\alphavec = 1+{\lambda\over2} {\hat{\mathbf{b}}}\cdot\alphavec.
:::

We see that the velocity matrices $\alphavec$ are the generators of boosts, perhaps not a surprise.

To obtain finite boosts we follow the same procedure shown in {eq}`eq-covariance-62` for rotations, which gives

:::{math}
:label: eq-covariance-68
D({\hat{\mathbf{b}}},\lambda) = \exp\Bigl({\lambda\over2}{\hat{\mathbf{b}}} \cdot\alphavec\Bigr).
:::

The exponential is easiest to carry out in the Weyl representation {eq}`eq-dirac-13`, in which the matrices $\alphavec$ are block-diagonal,

:::{math}
:label: eq-covariance-69
\begin{aligned}
\alphavec=\begin{pmatrix}\sigmavec & 0 \\  0 & -\sigmavec\\\end{pmatrix} \qquad (Weyl).
\end{aligned}

:::

The result can be expressed as

:::{math}
:label: eq-covariance-70
\begin{aligned}
D({\hat{\mathbf{b}}},\lambda) = \begin{pmatrix} V({\hat{\mathbf{b}}},\lambda) & 0 \\  0 & V({\hat{\mathbf{b}}},\lambda)^{-1} \\\end{pmatrix} \qquad (Weyl),
\end{aligned}

:::

where

:::{math}
:label: eq-covariance-71
V({\hat{\mathbf{b}}},\lambda) = \exp\Bigl( {\lambda\over2} {\hat{\mathbf{b}}}\cdot\sigmavec\Bigr) = \cosh{\lambda\over2} + ({\hat{\mathbf{b}}}\cdot\sigmavec) \sinh{\lambda\over2}
:::

and

:::{math}
:label: eq-covariance-72
V({\hat{\mathbf{b}}},\lambda)^{-1} = V({\hat{\mathbf{b}}},-\lambda) =\cosh{\lambda\over2} - ({\hat{\mathbf{b}}}\cdot\sigmavec) \sinh{\lambda\over2}.
:::

Although the rotation matrices $U({\hat{\mathbf{n}}},\theta)$ (see {eq}`eq-covariance-64` are unitary, the matrices $V({\hat{\mathbf{b}}},\lambda)$ which appear in the boosts are not (in fact, they are Hermitian). One can see that the $V$-matrices are like the $U$-matrices but with an imaginary angle.

To obtain the boosts in the Dirac-Pauli representation, we can either exponentiate the 4-dimensional $\alphavec$ matrices in that representation, or else change the basis according to

:::{math}
:label: eq-covariance-73
X_DP = W X_W W^\dagger,
:::

where $X$ is any Dirac matrix and the subscripts DP and W refer to the Dirac-Pauli and Weyl representations, respectively, and where

:::{math}
:label: eq-covariance-74
\begin{aligned}
W={1\over\sqrt{2}} \begin{pmatrix}1 & -1 \\ 1 & 1 \\\end{pmatrix}.
\end{aligned}

:::

See {eq}`eq-dirac-14`--{eq}`eq-dirac-15`. This gives

:::{math}
:label: eq-covariance-75
\begin{aligned}
D({\hat{\mathbf{b}}},\lambda) = \begin{pmatrix} \cosh(\lambda/2) & ({\hat{\mathbf{b}}}\cdot\sigmavec) \sinh(\lambda/2)\\  ({\hat{\mathbf{b}}}\cdot\sigmavec)\sinh(\lambda/2) & \cosh(\lambda/2) \\\end{pmatrix} \qquad \\text{Dirac-Pauli}.
\end{aligned}

:::

(sec-covariance-10)=

## Properties of the matrices $D(\Lambdamat)$

We recall the theorem quoted in {ref}`sec-lorentz-6`, that every proper Lorentz transformation can be represented uniquely as a product of a rotation times a boost, $\Lambdamat=\Rmat\Bmat$. Since we now have the $D$-matrices for both pure rotations and pure boosts, we can use this theorem to find the $D$-matrix for an arbitrary Lorentz transformation. It is the product of a rotation matrix of the form {eq}`eq-covariance-63`, times a boost matrix of the form {eq}`eq-covariance-70` or {eq}`eq-covariance-75`. As mentioned, the $D$-matrices for pure rotations are unitary, while those for pure boosts are Hermitian, and not generally unitary. The product of a rotation times a boost is a matrix with no particular symmetry, in general.

We usually say that unitary transformations are needed to implement symmetry operations, in order to preserve probabilities. Why then are the Dirac $D$-matrices not unitary? The answer is that the $D(\Lambdamat)$ only implement the spin part of a Lorentz transformation, but there is a spatial part, too. Since the probability density is $\psi^\dagger \psi$ in the Dirac theory, a normalized wave function satisfies

:::{math}
:label: eq-covariance-76
\int d^3\xvec \, \psi^\dagger(\xvec,t) \psi(\xvec,t) =1,
:::

for all $t$. Under a Lorentz transformation the volume element $d^3\xvec$ is not invariant, but rather scales by the relativistic factor $\gamma=1/\sqrt{1-(v/c)^2}$ of length contraction and time dilation (obviously not to be confused with a Dirac matrix). Similarly, the spin part of a Lorentz transformation guarantees that $\psi^\dagger \psi$ is not an invariant, either (it is the time component of a 4-vector), rather it also acquires a factor of $\gamma$ upon being subjected to a Lorentz transformation, which cancels the factor of $\gamma$ coming from the volume element. Thus, the normalization integral is invariant, but $\psi^\dagger \psi$ is not. That is, the overall transformation is unitary, even if the spin part is not. The exception is a pure rotation, under which both $\psi^\dagger \psi$ and $d^3\xvec$ are invariant, and $D$ is unitary. This discussion has been rather imprecise and lacking in details because a proper understanding of probability conservation in a relativistic theory must take into account the relativity of simultaneity, and is best expressed in terms of currents and 3-forms in space-time. Nevertheless, we will see the factor of $\gamma$ appear when we consider the transformation of spinors for free particles.

Notice that the Dirac $D$-matrices for pure rotations in {eq}`eq-covariance-63` have the same double-valuedness seen in nonrelativistic rotations. That is, rotations about an axis ${\hat{\mathbf{n}}}$ by angles $\theta$ and $\theta+2\pi$ give the same classical rotation, but the Dirac rotations differ by a sign, $D({\hat{\mathbf{n}}},\theta+2\pi) = -D({\hat{\mathbf{n}}},\theta)$. On the other hand, there is no double-valuedness in the boosts, as seen in {eq}`eq-covariance-70` or {eq}`eq-covariance-75`; a classical boost with a given axis ${\hat{\mathbf{b}}}$ and rapidity $\lambda$ corresponds to a unique Dirac $D$ matrix, which boosts a spinor. Overall, the Dirac $D$-matrices have the same double-valuedness seen in spinor rotations, with nothing added on account of boosts. Thus, a sign ambiguity appears if we attempt to parameterize a Dirac $D$-matrix by a classical Lorentz transformation, as in the notation $D(\Lambdamat)$, but not if we parameterize rotations and boosts by $({\hat{\mathbf{n}}},\theta)$ and $({\hat{\mathbf{b}}},\lambda)$.

(sec-covariance-11)=

## Conjugation of Dirac Matrices by $\gamma^0$

The generators of unitary transformations are Hermitian, but since the Dirac $D$-matrices are in general not unitary, the generators $\sigma^{\mu\nu}$ cannot be in general Hermitian. In fact, the spatial parts, $\sigma^{ij}$, or, equivalently, $\Sigmavec$, are Hermitian, as can be seen in {eq}`eq-covariance-59` and {eq}`eq-covariance-61`. But the components $\sigma^{0i}=i\alpha_i$, which generate boosts, are anti-Hermitian. See {eq}`eq-covariance-66`.

But there is a simple relation between $\sigma^{\mu\nu}$ and $(\sigma^{\mu\nu})^\dagger$, given by

:::{math}
:label: eq-covariance-77
\boxed{\gamma^0 \sigma^{\mu\nu} \gamma^0 = \bigl(\sigma^{\mu\nu}\bigr)^\dagger.}
:::

This in turn implies

:::{math}
:label: eq-covariance-78
\boxed{\gamma^0 D(\Lambdamat)^{-1} \gamma^0 = D(\Lambdamat)^\dagger.}
:::

This replaces the usual property for unitary matrices, $U^{-1} = U^\dagger$, when working with Dirac $D$-matrices.

To prove {eq}`eq-covariance-77`, we begin with

:::{math}
:label: eq-covariance-79
\boxed{\gamma^0 \gamma^\mu \gamma^0 = \bigl(\gamma^\mu\bigr)^\dagger.}
:::

We recall that $\gamma^0=\beta$ is Hermitian, and $\gamma^i=\beta\alpha_i$ is anti-Hermitian (see {eq}`eq-covariance-16`. So

:::{math}
:label: eq-covariance-80
\gamma^0 \gamma^0 \gamma^0 = \beta^3 = \beta = \gamma^0 = \bigl(\gamma^0\bigr)^\dagger,
:::

and

:::{math}
:label: eq-covariance-81
\gamma^0\gamma^i\gamma^0 = \beta^2 \alpha_i \beta = \alpha_i\beta = -\beta\alpha_i=-\gamma^i =\bigl(\gamma^i\bigr)^\dagger.
:::

This proves {eq}`eq-covariance-79`.

To prove {eq}`eq-covariance-77` we use the definition {eq}`eq-covariance-55`, and write

:::{math}
:label: eq-covariance-82
\begin{aligned}
\gamma^0 \sigma^{\mu\nu} \gamma^0 &= {i\over 2}\gamma^0 \bigl(\gamma^\mu\gamma^\nu - \gamma^\nu\gamma^\mu\bigr)\gamma^0 = {i\over2} \bigl[\bigl(\gamma^0\gamma^\mu\gamma^0\bigr) \bigl(\gamma^0\gamma^\nu \gamma^0\bigr) - (\mu\leftrightarrow\nu)\bigr] \\
&= {i\over2}\bigl[\bigl(\gamma^\mu\bigr)^\dagger \bigl(\gamma^\nu\bigr)^\dagger - (\mu\leftrightarrow\nu)\bigr] = {i\over 2} \bigl(\gamma^\nu\gamma^\mu-\gamma^\mu\gamma^\nu \bigr)^\dagger = \bigl(\sigma^{\mu\nu}\bigr)^\dagger. \\

\end{aligned}
:::

Now from {eq}`eq-covariance-50`, we have, in the case of an infinitesimal Lorentz transformation,

:::{math}
:label: eq-covariance-83
D(\Lambdamat)^{-1} = 1+{i\over4}\theta_{\mu\nu} \, \sigma^{\mu\nu},
:::

and

:::{math}
:label: eq-covariance-84
D(\Lambdamat)^\dagger = 1+{i\over4}\theta_{\mu\nu} \bigl(\sigma^{\mu\nu}\bigr)^\dagger.
:::

{eq}`eq-covariance-78` easily follows from this in the case of an infinitesimal Lorentz transformation. But it is easy to show that if {eq}`eq-covariance-78` is true for two proper Lorentz transformations, then it is true for their product. Since an arbitrary proper Lorentz transformation can be built up as a product of infinitesimal Lorentz transformations, the result must be true for an arbitrary proper Lorentz transformation.

The case of parity, an improper Lorentz transformation, is taken up below.

(sec-covariance-12)=

## The Adjoint Spinor and Probability Current

We are now prepared to show that the Dirac probability current, defined by {eq}`eq-dirac-23`, transforms as a 4-vector under Lorentz transformations. To begin we write the components of the current in the following way:

:::{math}
:label: eq-covariance-85
\begin{aligned}
J^0 &= c\rho = c\psi^\dagger \psi = c\psi^\dagger \gamma^0 \gamma^0 \psi, \\
J^i &= c\psi^\dagger \alpha_i \psi = c\psi^\dagger \gamma^0 \gamma^0\alpha_i\psi = c\psi^\dagger \gamma^0 \gamma^i \psi. \\

\end{aligned}
:::

The combination $\psi^\dagger\gamma^0$ is of frequent occurrence in the Dirac theory, so we give it a special notation,

:::{math}
:label: eq-covariance-86
\boxed{\psibar = \psi^\dagger\gamma^0,}
:::

and we call it the *adjoint spinor*. Notice that the adjoint spinor contains a complex conjugated version of $\psi$, and is a row spinor. In terms of the adjoint spinor, we can write

:::{math}
:label: eq-covariance-87
\boxed{J^\mu = c\,\psibar \gamma^\mu \psi.}
:::

This is regarded as the covariant form of the probability current.

Let us see how $J^\mu(x)$ transforms under a Lorentz transformation. The Dirac spinor $\psi$ itself transforms according to {eq}`eq-covariance-26`, which we write in the form

:::{math}
:label: eq-covariance-88
\psi(x) \mathrel{\mathop{\text{t}o 20pt {\rightarrowfill}}^{\Lambdamat}} D(\Lambdamat)\psi\bigl(\Lambdamat^{-1}x\bigr).
:::

Thus the adjoint spinor transforms according to

:::{math}
:label: eq-covariance-89
\psibar(x) = \psi^\dagger(x)\gamma^0 \mathrel{\mathop{\text{t}o 20pt {\rightarrowfill}}^{\Lambdamat}} \psi^\dagger\bigl(\Lambdamat^{-1}x\bigr)D(\Lambdamat)^\dagger \gamma^0 = \psi^\dagger\bigl(\Lambdamat^{-1}x\bigr)\gamma^0\gamma^0 D(\Lambdamat)^\dagger\gamma^0 = \psibar\bigl(\Lambdamat^{-1}x\bigr)D(\Lambdamat)^{-1},
:::

where we have used {eq}`eq-covariance-78`. Therefore $J^\mu$ itself transforms according to

:::{math}
:label: eq-covariance-90
\begin{aligned}
J^\mu(x) &= c\psibar(x)\gamma^\mu\psi(x) \transformsby{\Lambdamat} c \psibar\bigl(\Lambdamat^{-1}x\bigr) D(\Lambdamat)^{-1} \gamma^\mu D(\Lambdamat) \psi\bigl(\Lambdamat^{-1}x\bigr) \\
&= \Lambda^\mu{}_\nu\, c\psibar\bigl(\Lambdamat^{-1}x\bigr) \gamma^\nu \psi\bigl(\Lambdamat^{-1}x\bigr) = \Lambda^\mu{}_\nu\, J^\nu\bigl(\Lambdamat^{-1}x\bigr), \\

\end{aligned}
:::

where we have used {eq}`eq-covariance-42`. The result is that $J^\mu(x)$ transforms as a vector field on space-time should under an active Lorentz transformation, as shown in {eq}`eq-covariance-25`. Thus, the continuity equation {eq}`eq-dirac-28` is covariant, as we require.

(sec-covariance-13)=

## How Fields Transform

We are collecting several examples of different kinds of fields and how they transform under Lorentz transformations. {ref}`tbl-covariance-1` summarizes the ones we have encountered so far, and several new ones as well. The transformation properties of Dirac spinors and adjoint spinors has been discussed in these notes. The case of scalars (that is, scalars under Lorentz transformations) has been discussed in {ref}`ch-lorentz`, in which it was pointed out that $E^2-B^2$ is a Lorentz scalar that can be constructed out of the electromagnetic field [see {eq}`eq-lorentz-88`--({eq}`eq-lorentz-89`]. It has also been mentioned that the Klein-Gordon wave function $\psi_KG$ is a Lorentz scalar. Can we construct a Lorentz scalar out of the Dirac wave function? Yes, it turns out that the quantity $\psibar(x)\psi(x)$ is a Lorentz scalar. The proof of this fact will be left as an exercise. Notice that $\psi^\dagger(x)\psi(x)$ is not a Lorentz scalar, in fact it is the time-component of a 4-vector (essentially the current $J^\mu$).

:::{table} Transformation properties of various types of fields under an active Lorentz transformation.
:label: tbl-covariance-1

| Field | Transformation Law |
|:---:|:---|
| $\mathrm{Spinor}$ | $\psi(x) \xrightarrow{\Lambda} D(\Lambda)\psi(\Lambda^{-1}x)$ |
| $\mathrm{Adjoint Spinor}$ | $\bar{\psi}(x) \xrightarrow{\Lambda} \bar{\psi}(\Lambda^{-1}x)D(\Lambda^{-1})$ |
| $\mathrm{Scalar}$ | $S(x) \xrightarrow{\Lambda} S(\Lambda^{-1}x)$ |
| $\mathrm{Vector}$ | $V^{\mu}(x) \xrightarrow{\Lambda} \Lambda^{\mu}_{\ \nu} V^{\nu}(\Lambda^{-1}x)$ |
| $\mathrm{Tensor}$ | $T^{\mu\nu}(x) \xrightarrow{\Lambda} \Lambda^{\mu}_{\ \alpha} \Lambda^{\nu}_{\ \beta} T^{\alpha\beta}(\Lambda^{-1}x)$ |
| $\mathrm{Pseudoscalar}$ | $K(x) \xrightarrow{\Lambda} (\det \Lambda) K(\Lambda^{-1}x)$ |
| $\mathrm{Pseudovector}$ | $W^{\mu}(x) \xrightarrow{\Lambda} (\det \Lambda) \Lambda^{\mu}_{\ \nu} W^{\nu}(\Lambda^{-1}x)$ |

:::
The table shows the transformation law for a generic 4-vector field $V^\mu(x)$; examples include the 4-vector potential $A^\mu$ in electromagnetism (see {eq}`eq-covariance-10`, the Klein-Gordon probability current (see {eq}`eq-kleing-27` and the Dirac probability current (which we have gone to some trouble in these notes to show is a genuine 4-vector, see \secrcovariance-12).

The table also refers to a generic second-rank, relativistic tensor $T^{\mu\nu}$ and its transformation law. Such tensors occur in electromagnetic theory, for example, the field tensor $F^{\mu\nu}$ and the stress-energy tensor. A second-rank, antisymmetric tensor occurs in the Dirac theory; it is $\psibar(x) \sigma^{\mu\nu}\psi(x)$. This is proportional to a relativistic generalization of the magnetization $\Mvec$ (the dipole moment per unit volume), which in the nonrelativistic Pauli theory of the electron can be written as $\psi^\dagger \muvec \psi$, where $\muvec$ is the magnetic moment operator for the electron. See {ref}`sec-jjcouple-6`. We will see this tensor appear in the Gordon decomposition of the current, which is discussed in {ref}`sec-spdirac-10`.

(sec-covariance-14)=

## Improper Lorentz Transformations and Parity

Recall that an improper Lorentz transformation is one that cannot be built up from near-identity transformations, rather it is the product of a proper Lorentz transformation times time-reversal or parity or both. See \lorentz.3.

Recall also that in the nonrelativistic theory we classified vectors as either true vectors or pseudo-vectors, depending on how they transform under parity (odd and even, respectively). See \parity.6. We also spoke of scalars and pseudoscalars.

In the relativistic theory a pseudoscalar (for example, $K$ in the table, or $\Evec\cdot\Bvec$ in electromagnetism) transforms as a scalar under proper Lorentz transformations but under improper ones it acquires a sign given by $\det\Lambdamat$. Similarly, a pseudovector (for example, $W^\mu$ in the table) transforms as a vector under proper Lorentz transformation but under improper ones it acquires the same sign. In the following the only improper Lorentz transformation we will consider is parity, or products of parity times proper Lorentz transformations. For simplicity we will leave time-reversal out of the picture. With this understanding, $\det\Lambdamat=+1$ for proper Lorentz transformations and $\det\Lambdamat=-1$ for improper ones.

The classical Lorentz transformation corresponding to parity is

:::{math}
:label: eq-covariance-91
\begin{aligned}
\Pmat = \begin{pmatrix}1 & 0 & 0 & 0 \\ 0 & -1 & 0 & 0 \\ 0 & 0 & -1 & 0 \\ 0 & 0 & 0 & -1\\\end{pmatrix},
\end{aligned}

:::

in other words, it is the spatial inversion operation, which leaves time alone. Notice that $\det\Pmat=-1$.

Let us look for the operator $\pi$ that acts on Dirac wave functions, corresponding to the spatial inversion operation $\Pmat$. In the nonrelativistic theory, parity is a purely spatial operation with no effect on the spin [see {eq}`eq-parity-33`]. Therefore we might guess that the same is true in the Dirac theory, that is, that the transformation law for the Dirac wave function should be $\psi(\xvec,t) {\displaystyle\transformsby{\pi}} \psi(-\xvec,t)$. It turns out, however, that this does not work. Instead we must write

:::{math}
:label: eq-covariance-92
\psi(\xvec,t) \transformsby{\pi} D(\Pmat)\psi(-\xvec,t),
:::

where $D(\Pmat)$ is a spin matrix to be determined. Notice that the transformation of the space-time dependence in {eq}`eq-covariance-92` can also be written,

:::{math}
:label: eq-covariance-93
\psi(x) \transformsby{\pi} D(\Pmat)\psi\bigl(\Pmat^{-1}x\bigr),
:::

which makes the transformation law under parity a generalization of {eq}`eq-covariance-26`, which was originally intended to apply to proper Lorentz transformations only.

We determine $D(\Pmat)$ by requiring that parity map free particle solutions of the Dirac equation into other free particle solutions. The analysis of this question proceeds exactly as in \secrcovariance-6, and it leads to a conclusion of the same form as {eq}`eq-covariance-42`, that is, $D(\Pmat)$ must satisfy

:::{math}
:label: eq-covariance-94
D(\Pmat)^{-1} \gamma^\mu D(\Pmat) = P^\mu{}_\nu \, \gamma^\nu,
:::

where $P^\mu{}_\nu$ are the components of $\Pmat$. This implies

:::{math}
:label: eq-covariance-95
\begin{aligned}
&\mu=0: \qquad D(\Pmat)^{-1} \gamma^0 D(\Pmat) = \gamma^0 = \bigl(\gamma^0\bigr)^\dagger, \\
&\mu=i: \qquad D(\Pmat)^{-1} \gamma^i D(\Pmat) = -\gamma^i = \bigl(\gamma^i\bigr)^\dagger. \\

\end{aligned}
:::

But in view of {eq}`eq-covariance-79`, we see that {eq}`eq-covariance-95` are satisfied if we take

:::{math}
:label: eq-covariance-96
D(\Pmat) = e^{i\alpha}\, \gamma^0,
:::

where $\alpha$ is any phase. And we see that $D(\Pmat)=1$ will not work; in the relativistic theory, parity *must* involve the spin. This is another indication of the more intimate coupling between spatial and spin degrees of freedom in the relativistic theory.

The classical Lorentz transformation $\Pmat$ obeys certain properties, including

:::{math}
:label: eq-covariance-97a
\begin{aligned}
\Pmat \Rmat({\hat{\mathbf{n}}},\theta) &= \Rmat({\hat{\mathbf{n}}},\theta)\Pmat,
\end{aligned}
:::

:::{math}
:label: eq-covariance-97b
\begin{aligned}
\Pmat \Bmat({\hat{\mathbf{b}}},\lambda) &= \Bmat({\hat{\mathbf{b}}},-\lambda)\Pmat,
\end{aligned}
:::

:::{math}
:label: eq-covariance-97c
\begin{aligned}
\Pmat^2 &= \Imat,
\end{aligned}
:::

where $\Rmat$ and $\Bmat$ refer to pure rotations and pure boosts, respectively. (Spatial inversion commutes with rotations but inverts the direction of a boost.) If we demand that $D(\Pmat)$, taken along with the $D(\Lambdamat)$ that we have worked out, form a representation of the extended Lorentz group including parity (but still excluding time-reversal), then we should have

:::{math}
:label: eq-covariance-98a
\begin{aligned}
D(\Pmat) D({\hat{\mathbf{n}}},\theta) &= D({\hat{\mathbf{n}}},\theta)D(\Pmat),
\end{aligned}
:::

:::{math}
:label: eq-covariance-98b
\begin{aligned}
D(\Pmat) D({\hat{\mathbf{b}}},\lambda)&= D({\hat{\mathbf{b}}},-\lambda)D(\Pmat),
\end{aligned}
:::

:::{math}
:label: eq-covariance-98c
\begin{aligned}
D(\Pmat)^2 &=1,
\end{aligned}
:::

where $D({\hat{\mathbf{n}}},\theta)$ and $D({\hat{\mathbf{b}}},\lambda)$ are pure rotations and pure boosts as in {eq}`eq-covariance-63` and {eq}`eq-covariance-70` or {eq}`eq-covariance-75`, respectively.

{eq}`eq-covariance-98c` implies that $e^{i\alpha}$ in {eq}`eq-covariance-96` must be $\pm1$, so that

:::{math}
:label: eq-covariance-99
D(\Pmat)=\pm\gamma^0.
:::

The final choice of sign is purely a convention; if we take it to be $+1$, then it means that the *intrinsic parity* of the electron (see \parity.5) is $+1$. This in turn means that the intrinsic parity of the positron is $-1$, although we are jumping the gun to be talking about positrons at this point. But no physics would change if we made the opposite convention. For any fermion, the intrinsic parities of the particle and antiparticle are opposite, but it is a matter of convention which is which. In the following we will settle the matter by taking

:::{math}
:label: eq-covariance-100
D(\Pmat)=+\gamma^0.
:::

Does this choice of $D(\Pmat)$ satisfy {eq}`eq-covariance-98a` and {eq}`eq-covariance-98b`? In the case of {eq}`eq-covariance-98a` for an infinitesimal rotation, the question boils down to

:::{math}
:label: eq-covariance-101
\gamma^0 \sigma^{ij} \gamma^0 = \sigma^{ij},
:::

which is true in view of {eq}`eq-covariance-77` and the fact that $\sigma^{ij}$ consists of Hermitian matrices. In the case of {eq}`eq-covariance-98b` for an infinitesimal boost, we must check

:::{math}
:label: eq-covariance-102
\gamma^0 \alpha_i \gamma^0 = -\alpha_i,
:::

which is also true. But if these relations are true for infinitesimal Lorentz transformations then they are true for any proper Lorentz transformation, by building up finite transformations as the products of infinitesimal ones (by now you must appreciate the power of this argument). We conclude that our definition of $D(\Pmat)$ {eq}`eq-covariance-100` is satisfactory.

With this definition of $D(\Pmat)$ it is easy to check that the Dirac current, proportional to $\psibar\gamma^\mu\psi$, transforms as a true vector (not a pseudovector), and that $\psibar\psi$ transforms as a true scalar (not a pseudoscalar).

(sec-covariance-15)=

## Pseudoscalars and Pseudovectors

Pseudoscalars and pseudovectors are important in the weak interactions, notably in the theory of the neutrino, which do not conserve parity. To construct these types of fields we must introduce a new (and final) Dirac matrix,

:::{math}
:label: eq-covariance-103
\gamma_5 = \gamma^5 = i\gamma^0\gamma^1\gamma^2\gamma^3.
:::

The 5 index is not a space-time index (obviously), rather it is a way of defining a new Dirac matrix without using up another letter of the Greek alphabet. We do not use a 4 because $\gamma_4$ is a Dirac matrix used in (mostly older) versions of the theory which use $x_4=ict$ as an imaginary coordinate on space-time. See {ref}`sec-tensor-21`. The upper or lower position of the index 5 is of no significance. The complete set of Dirac matrices useful in a covariant description includes $\gamma^\mu$, $\sigma^{\mu\nu}$ and $\gamma_5$ (one can also include the identity matrix $1$).

The explicit form of the matrix $\gamma_5$ is

:::{math}
:label: eq-covariance-104
\begin{aligned}
\gamma_5=\begin{pmatrix}0&1\cr1&0\\\end{pmatrix} \quad \text{(Dirac-Pauli)}, \qquad \begin{pmatrix}1&0\cr0&-1\\\end{pmatrix} \quad \text{(Weyl)}.
\end{aligned}

:::

Other properties of $\gamma_5$ include the following:

:::{math}
:label: eq-covariance-105a
\begin{aligned}
\bigl(\gamma_5\bigr)^\dagger &= \gamma_5,
\end{aligned}
:::

:::{math}
:label: eq-covariance-105b
\begin{aligned}
\bigl(\gamma_5\bigr)^2 &=1,
\end{aligned}
:::

:::{math}
:label: eq-covariance-105c
\begin{aligned}
\{\gamma_5,\gamma^\mu\} &= 0,
\end{aligned}
:::

:::{math}
:label: eq-covariance-105d
\begin{aligned}
[\gamma_5,\sigma^{\mu\nu}] &= 0,
\end{aligned}
:::

Notice that {eq}`eq-covariance-105c` implies

:::{math}
:label: eq-covariance-106
\{\gamma_5,D(\Pmat)\} =0,
:::

and {eq}`eq-covariance-105d` implies

:::{math}
:label: eq-covariance-107
[\gamma_5,D(\Lambdamat)]=0,
:::

for all proper Lorentz transformations $\Lambdamat$. We will just prove property {eq}`eq-covariance-105c`. Take the case $\mu=2$. We have

:::{math}
:label: eq-covariance-108
\gamma_5\gamma^2 = i\gamma^0\gamma^1\gamma^2\gamma^3\gamma^2 = -i\gamma^0\gamma^1\gamma^2\gamma^2\gamma^3 = -i\gamma^2\gamma^0\gamma^1\gamma^2\gamma^3 = -\gamma^2\gamma_5,
:::

where in the first step we move the $\gamma^2$ on the right past $\gamma^3$, incurring one minus sign, and in the second step we move the $\gamma^2$ on the left past $\gamma^1$ and $\gamma^0$, incurring two minus signs. We can summarize {eq}`eq-covariance-106` and {eq}`eq-covariance-107` by writing

:::{math}
:label: eq-covariance-109
\gamma_5 D(\Lambdamat) = (\det\Lambdamat) D(\Lambdamat) \gamma_5,
:::

valid for both proper and improper Lorentz transformations $\Lambdamat$ (still excluding time-reversal).

It is now easy to construct the pseudoscalar and pseudovector in the Dirac theory. The pseudoscalar is $\psibar(x)\gamma_5\psi(x)$, and the pseudovector is $\psibar(x)\gamma_5\gamma^\mu\psi(x)$.

(sec-covariance-16)=

## The Dirac Algebra and Bilinear Covariants

The various fields with the various transformation properties under Lorentz transformations that are summarized in {ref}`tbl-covariance-1` are needed to construct Lorentz invariant Lagrangians that model experimental data. That data shows that nature either does or does not respect various symmetries, which in turn dictates the kinds of fields that may appear in the Lagrangian. It is believed that all interactions are invariant under proper Lorentz transformations, at least at scales at which gravitational effects are unimportant, but it is known that some interactions do not respect parity or time-reversal (more precisely, $CP$-invariance). For example, at low energies the Lagrangian for the weak interactions involves the difference between a vector and a pseudovector (the “$V-A$” theory), which is responsible for parity violation.

The types of fields listed in {ref}`tbl-covariance-1` are *bilinear covariants*, which we now describe. These are associated with the *algebra* of the Dirac matrices $\gamma^\mu$. The algebra is defined as the set of all linear combinations, with complex coefficients, of all matrices that can be formed by multiplying the $\gamma^\mu$. It is the space of all complex polynomials that can be constructed out of the $\gamma^\mu$.

The algebra generated by the $2\times2$ Pauli matrices is simpler, so let us look at it first. There are three Pauli matrices $\sigma_i$, $i=1,2,3$, but $(\sigma_i)^2=1$ so the algebra includes the identity matrix. A general quadratic monomial in the Pauli matrices can be reduced to a polynomial of first degree by the formula,

:::{math}
:label: eq-covariance-110
\sigma_i\sigma_j = \delta_{ij} + i\epsilon_{ijk} \, \sigma_k,
:::

so the algebra generated by the Pauli matrices consists of all first degree polynomials, that is, all matrices of the form $a+\bvec\cdot\sigmavec$, where $a$ and $\bvec$ are complex coefficients. But the set of matrices, $\{1,\sigmavec\}$ spans the space of all $2\times2$ matrices, so the algebra generated by the Pauli matrices consists of all $2\times2$ matrices.

The Dirac algebra is generated by the four $4\times4$ Dirac matrices $\gamma^\mu$. Since $\bigl(\gamma^\mu\bigr)^2 = \pm1$, the Dirac algebra contains the identity matrix. The quadratic monomial $\gamma^\mu\gamma^\nu$ looks like 16 matrices, but only six of these are independent, because of the anticommutator $\{\gamma^\mu, \gamma^\nu\} = \gamma^\mu\gamma^\nu + \gamma^\nu\gamma^\mu = 2g^{\mu\nu}$ (times the identity matrix). The antisymmetric part is captured by $\sigma^{\mu\nu} = (i/2)[\gamma^\mu,\gamma^\nu]$, which has 6 independent components.

As for cubic monomials, say, $\gamma^\mu\gamma^\nu\gamma^\sigma$, these can be reduced to a first degree polynomial if any of the indices $\mu$, $\nu$, and $\sigma$ are equal. For example, $\gamma^2\gamma^3\gamma^2=-\gamma^2\gamma^2\gamma^3= \gamma^3$. But if all three indices are distinct, then one index must be omitted, so there are 4 independent cubic monomials that cannot be reduced to lower degree. In fact, these are given by $\gamma_5\gamma^\mu$, where $\mu$ indicates the index that is omitted. For example, if $\mu=2$ we have

:::{math}
:label: eq-covariance-111
\gamma_5\gamma^2=i\gamma^0\gamma^1\gamma^2\gamma^3\gamma^2 = -i\gamma^0\gamma^1\bigl(\gamma^2\bigr)^2\gamma^3 = +i\gamma^0\gamma^1\gamma^3,
:::

where the final result is a cubic monomial with $\mu=2$ omitted.

Finally, a quartic monomial $\gamma^\mu\gamma^\nu\gamma^\sigma\gamma^\tau$ can be reduced to a lower degree unless all four indices are distinct, in which case the matrix is proportional to $\gamma_5$. Thus, there is one independent quartic monomial. All higher degree monomials must contain repetitions of indices, and so can be reduced to lower degree.

:::{table} Bilinear covariants and the Dirac algebra.
:label: tbl-covariance-2

| Matrices | Name | Count |
|:---:|:---:|:---:|
| $1$ | $\mathrm{Scalar}$ | 1 |
| $\gamma^\mu$ | $\mathrm{Vector}$ | 4 |
| $\sigma^{\mu\nu}$ | $\mathrm{Tensor}$ | 6 |
| $\gamma_5 \gamma^\mu$ | $\mathrm{Pseudovector}$ | 4 |
| $\gamma_5$ | $\mathrm{Pseudoscalar}$ | 1 |
| $\mathrm{Total}$ | | $16$ |

:::
The list of Dirac matrices that span the Dirac algebra is summarized in {ref}`tbl-covariance-2`. By sandwiching these matrices between $\psibar$ and $\psi$ we obtain one of the bilinear covariants given in {ref}`tbl-covariance-1`. The matrices listed are linearly independent, so they span the space of all $4\times4$ Dirac matrices. Thus the Dirac algebra consists of all $4\times4$ matrices, and an arbitrary $4\times4$ matrix can be expressed uniquely as a linear combination of the the 16 basis matrices listed in {ref}`tbl-covariance-2`.

(sec-covariance-17)=

## Angular Momentum of the Dirac Particle

In {ref}`ch-spinrot`{} we defined the angular momentum of a system as the generator of rotations. See {eq}`eq-spinrot-13`. Since we now know how to apply rotations to the Dirac particle, we can work out the angular momentum operator by considering infinitesimal rotations and examininng the correction term.

The Dirac wave function $\psi(x)$ transforms under a general Lorentz transformation according to {eq}`eq-covariance-26`. The transformation has two parts, a space-time Lorentz transformaiton specified by $\Lambdamat$, which in the case of pure rotations only affects the spatial coordinates $\xvec$ and leaves the time alone; and a spin part, specified by a Dirac matrix $D(\Lambdamat)$, which in the case of pure rotations is given by {eq}`eq-covariance-63`. Making the Lorentz transformation a pure rotation with an infinitesimal angle $\theta$, we can write {eq}`eq-covariance-26` as

:::{math}
:label: eq-covariance-112
\psi'(\xvec,t) = \Bigl(1-{i\over2}\theta{\hat{\mathbf{n}}}\cdot\Sigmavec \Bigr) \psi\bigl(\xvec -\theta({\hat{\mathbf{n}}}\cdot\Jmatvec) \xvec,t) = \psi(\xvec,t) -{i\over2}\theta({\hat{\mathbf{n}}}\cdot\Sigmavec)\psi -\theta[({\hat{\mathbf{n}}}\cdot\Jmatvec)\xvec]\cdot\del\psi,
:::

where we use {eq}`eq-lorentz-74` and {eq}`eq-lorentz-70` for the infinitesimal rotation $\Lambdamat$ and {eq}`eq-covariance-62` for the corresponding infinitesimal $D$-matrix. But by {eq}`eq-classrot-26` the second correction term in {eq}`eq-covariance-112` can be written,

:::{math}
:label: eq-covariance-113
-\theta ({\hat{\mathbf{n}}}\cross\xvec)\cdot\del\psi = -{i\over\hbar} ({\hat{\mathbf{n}}}\cross\xvec)\cdot\pvec \psi =-{i\over\hbar} {\hat{\mathbf{n}}}\cdot(\xvec\cross\pvec)\psi =-{i\over\hbar}{\hat{\mathbf{n}}}\cdot\Lvec\psi,
:::

where $\pvec=-i\hbar\del$ and $\Lvec=\xvec\cross\pvec$. This is essentially the same derivation of the orbital angular momentum as given in {ref}`sec-orbamsph-3`, but here we also have a spin part, the first correction term in {eq}`eq-covariance-112`. Writing $-(i/\hbar){\hat{\mathbf{n}}}\cdot\Jvec$ for the entire correction term, we obtain

:::{math}
:label: eq-covariance-114
\Jvec=\Lvec + {\hbar\over2}\Sigmavec
:::

for the entire angular momentum of the Dirac particle. This is an obvious generalization of the angular momentum $\Jvec =\Lvec+ (\hbar/2)\sigmavec$ of a spin-$\frac{1}{2}$ particle in the Pauli theory.

\problems

(prob-covariance-1)=

**Problem \prbdcovariance-1.} The generators $\sigma^{\mu\nu}$ of the Dirac representation of Lorentz transformations must satisfy {eq}`eq-covariance-53`, which is a version of {eq}`eq-covariance-42` when the Lorentz transformation is infinitesimal.   We guess that $\sigma^{\mu\nu.** 

(prob-covariance-2)=

**Problem \prbdcovariance-2..** 

\problempart{(a)} Show that }$\psibar(x)\psi(x)$ transforms as a scalar under proper Lorentz transformations.

\problempart{(b)} Show that $\psibar(x)\sigma^{\mu\nu}\psi(x)$ transforms as a second rank tensor under proper Lorentz transformations.

\problempart{(c)} Show that $\psibar(x)\psi(x)$ transforms as a scalar (not a pseudoscalar) under parity. Show that the Dirac current transforms transforms as a vector (not a pseudovector) under parity.

\problempart{(d)} Show that $\psibar(x)\gamma_5\psi(x)$ transforms as a pseudoscalar, and that $\psibar(x)\gamma_5\gamma^\mu\psi(x)$ transforms as a pseudovector.

(prob-covariance-3)=

**Problem \prbdcovariance-3.}  A continuation of Problem {ref}`prob-dirac-1`.  A fact not mentioned in that earlier problem is that the representation of the Dirac algebra in $2+1$ dimensions has two *inequivalent.** 

\problempart{(a)* Assume that the 2-component Dirac wave function transforms under proper Lorentz transformations }$\Lambda$ in $2+1$ dimensions according to

:::{math}
:label: eq-covariance-115
\psi'(x) = D(\Lambda) \psi(\Lambda^{-1} x),
:::

where $D(\Lambda)$ is some (as yet unknown) $2\times2$ representation of the proper Lorentz transformations in $2+1$ dimensions and $x=(ct,x_1,x_2)$ (1,2 mean $x$, $y$). Assuming that $\psi(x)$ satisfies the free particle Dirac equation, and that $\psi'(x)$ is given by {eq}`eq-covariance-115`, demand that $\psi'(x)$ also satisfy the free particle Dirac equation and thereby derive a condition that the representation $D(\Lambda)$ must satisfy.

\problempart{(b)} Write out explicitly the matrices $D({\hat{\mathbf{z}}},\theta)$ for the case of pure rotations and $D({\hat{\mathbf{b}}},\lambda)$ for the case of pure boosts, where ${\hat{\mathbf{b}}}$ lies in the $x$-$y$ plane. Do this in the Dirac-Pauli representation. Show that if you work in the Maiorana representation, the $D$-matrices are purely real.

\problempart{(c)} Show that in $2+1$ dimensions, the spatial inversion operation is a proper Lorentz transformation, that is, it can be continuously connected with the identity. Thus there is no problem of determining $D(\Pmat)$ as in $3+1$ dimensions; it is already taken care of by the proper Lorentz transformations worked out in part~(b).

(prob-covariance-4)=

**Problem \prbdcovariance-4.}  This problem is borrowed from Bjorken and Drell, *Relativistic Quantum Mechanics.** 

We have seen that the Dirac equation with minimal coupling to the electromagnetic field gives a $g$-factor of $2$, very close to the experimental value for the electron. What do we do with spin-$\frac{1}{2}$ particles such as the proton and neutron, which have “anomalous” $g$-factors?

In this problem we use natural units, $\hbar=c=1$. Next, we modify the Dirac equation to include another coupling to the electromagnetic field, in addition to the minimal coupling,

:::{math}
:label: eq-covariance-116
\Bigl(\pslash-q\Aslash -{\kappa e\over 4m} \sigma_{\mu\nu} F^{\mu\nu} -m \Bigr)\psi=0,
:::

where $m$ is the mass, $q$ the charge, and $\kappa$ the strength of the anomalous magnetic moment term. For the electron, $q=-e$ and $\kappa=0$; for the proton, $q=e$ and $\kappa=1.79$; and for the neutron, $q=0$ and $\kappa=-1.91$. Here $F_{\mu\nu}$ is defined in terms of the vector potential $A_\mu$ by

:::{math}
:label: eq-covariance-117
F_{\mu\nu} = \frac{\partial A_\nu}{\partial x^\mu}-\frac{\partial A_\mu}{\partial x^\nu},
:::

which agrees with Jackson. See also {ref}`sec-classmech-13`, and {eq}`eq-classmech-56` and {eq}`eq-classmech-57`.

\problempart{(a)} Write out the modified Dirac Hamiltonian, and show that it is Hermitian.

\problempart{(b)} Show that probability is conserved, i.e.,

:::{math}
:label: eq-covariance-118
\frac{\partial J^\mu}{\partial x^\mu}=0,
:::

where $J^\mu$ is defined exactly as for the unmodified Dirac equation, $J^\mu = \bar\psi\gamma^\mu\psi$.

\problempart{(c)} Covariance. Suppose $\psi(x)$ satisfies the modified Dirac equation {eq}`eq-covariance-116`, and let

:::{math}
:label: eq-covariance-119
\begin{aligned}
\psi'(x) &= D(\Lambdamat)\psi(\Lambdamat^{-1}x), \\
A^{\prime\mu}(x) &= \Lambda^\mu{}_\nu \, A^\nu(\Lambdamat^{-1}x), \\
F^{\prime\mu\nu}(x) &= \Lambda^\mu{}_\alpha \, \Lambda^\nu{}_\beta \, F^{\alpha\beta} (\Lambdamat^{-1}x). \\

\end{aligned}
:::

Then show that $\psi'(x)$ satisfies the modified Dirac equation {eq}`eq-covariance-116`, but with Lorentz transformed fields $A^{\prime\mu}(x)$ and $F^{\prime\mu\nu}(x)$ instead of the original fields.

\problempart{(d)} Assume $\Evec=0$, $\Bvec\ne0$ (in order to see what the effective magnetic moment of the particle is). Perform a simple nonrelativistic approximation as in {ref}`sec-dirac-9`, and show that you get the right $g$-factors for the proton and neutron.
