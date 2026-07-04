---
title: "49. The Foldy-Wouthuysen Transformation"
---
(ch-foldyw)=

# 49. The Foldy-Wouthuysen Transformation

(sec-foldyw-1)=

## Introduction

In {ref}`sec-dirac-9` we carried out a nonrelativistic approximation to the Dirac equation through order $(v/c)^2$, relative to the rest-mass energy $mc^2$, obtaining the Pauli equation including the $\muvec\cdot\Bvec$ term with $g=2$. In these notes we will carry out the expansion through order $(v/c)^4$. To do this we will use a systematic procedure known as the Foldy-Wouthuysen transformation. This transformation block-diagonalizes the matrices that appear in the Dirac equation, thereby decoupling the upper and lower 2-component spinors of the 4-component Dirac spinor and producing two decoupled 2-component spinor equations. Our presentation of this subject is based on that of Bjorken and Drell, *Relativistic Quantum Mechanics*.

(sec-foldyw-2)=

## Units and Ordering

In these notes we use natural units, in which $\hbar=c=1$. In these units the fine structure constant becomes

:::{math}
:label: eq-foldyw-1
 \alpha = {e^2\over\hbar c} = e^2,
:::

so that e\approx 1/\sqrt{137} (recall that in atomic units, $e=1$).

We take the basic parameter of smallness to be $v/c=v$, but the order of other quantities (for example, the magnetic field) in terms of this small quantity depends on the physical sitation. That is, we must choose a reference system to establish the order magnitude of of various physical quantities in terms of $v/c$. For our reference system we will take the ground state of hydrogen. Thus our results will be valid for any other system whose basic orders of magnitude are comparable to those of hydrogen, such as other atoms of low $Z$ near the ground state as well as many problems in molecular or condensed matter physics. For other problems such as those with strong external fields it would be advisable to rethink the ordering scheme.

Although we are mainly interested in the electron, the Dirac equation describes any particle of spin $\frac{1}{2}$ and $g\approx 2$, such as the positron or various muons. Therefore we will leave the mass $m$ and charge $q$ of the particle as free parameters. This will not affect the ordering of terms in powers of $v/c$. Other particles with anomalous $g$-factors require a modified treatment. See Prob. {ref}`prob-covariance-4`.

In the ground state of hydrogen $v/c$ is of the order of the fine structure constant $\alpha$, so the expansion in powers of $v/c$ can be thought of as an expansion in powers of $\alpha$. We shall, however, use a formal expansion parameter $\eta$ instead of $\alpha$, partly to avoid confusion between the fine struction constant and the Dirac matrices $\alphavec$. For example, we shall say that the velocity $v$ is of order $\eta$. The only purpose of $\eta$ is to keep track of the order of various terms.

:::{table} Ordering of various quantities in powers of $\eta \sim v/c$. It is assumed that electric and magnetic fields are internally generated.
:label: tbl-foldyw-1

| Quantity | Symbol | Order |
|:---:|:---:|:---:|
| $\text{Electron mass}$ | $m$ | $\eta^0 = 1$ |
| $\text{Velocity}$ | $v$ or $u$ | $\eta^1 = 1$ |
| $\text{Kinetic energy}$ | $(1/2)mv^2$ | $\eta^2$ |
| $\text{Potential energy}$ | $q\Phi$ | $\eta^2$ |
| $\text{Kinetic momentum}$ | $\pivec = m \vvec$ | $\eta$ |
| $\text{Fine structure constant}$ | $\alpha$ | $\eta$ |
| $\text{Compton } \lambda$ | $\lambda_C = 1/m$ | $\eta^0 = 1$ |
| $\text{Bohr radius}$ | $a_0 = \lambda_C / \alpha = 1/ma^2$ | $\eta^{-1}$ |
| $\text{Orbital period}$ | $T_0 \sim a_0/v_0 \sim 1/m\alpha^2$ | $\eta^{-2}$ |
| $\nabla$ | $\sim 1/a_0$ | $\eta$ |
| $\partial/\partial t$ | $\sim 1/T_0$ | $\eta^2$ |
| $q\Evec_\parallel$ | $-q\nabla\Phi$ | $\eta^3$ |
| $q\Avec$ | $\sim v (q\Phi)$ | $\eta^3$ |
| $q\Bvec$ | $ q\nabla \times \Avec$ | $\eta^4$ |
| $q\Evec_\perp$ | $-q(\partial \Avec/\partial t)$ | $\eta^5$ |

:::
We take the reference energy to be the electron rest mass-energy $mc^2=m$, which we regard as of order $\eta^0=1$, as indicated in {ref}`tbl-foldyw-1`. The velocity $v$ is of order $\eta$; in the hydrogen ground state we have denoted the velocity by $v_0$ (see, for example, {ref}`tbl-cenforce-1`), which in natural units is $\alpha$ (the fine structure constant). Thus the kinetic energy of the electron $mv^2/2$ is of order $\eta^2$, as shown in the table. Assuming that kinetic and potential energy trade off between themselves as is typical in a bound state problem, the potential energy $q\Phi$ must also be of order $\eta^2$. Also, the kinetic momentum,

:::{math}
:label: eq-foldyw-2
\pivec=\pvec-q\Avec = m\vvec
:::

is of order $\eta$, as shown in the table.

The unit of length in natural units is the Compton wavelength, $\lambda_C =\hbar/mc = 1/m$, which is regarded as of order $\eta^0=1$. The Bohr radius $a_0$ is a factor of $1/\alpha$ times larger than this, $a_0=\lambda_C/\alpha = 1/m\alpha$, which is therefore of order $\eta^{-1}$. The scale of the atom is large in the units we are using. Likewise, the orbital period $T_0$ in the atom is of order $a_0/v_0=1/m\alpha^2$, which is of order $\eta^{-2}$. This is also large in the units we are using. (The natural unit of time is $\hbar/mc^2 = 1/m$; the orbital period in hydrogen is a factor of $1/\alpha^2$ times larger than this.)

We will order all electric and magnetic fields as if they were internally generated. This does not mean that they have to be internally generated, it just means that they will be ordered as if they were. (For example, in {ref}`ch-zeeman`{} it was noted that strong laboratory magnetic fields are roughly of the same order of magnitude as those generated by electron orbital and spin currents in an atom.) For example, we will treat the electrostatic potential as of order $\Phi\sim e/a_0$, so that $q\Phi \sim e^2/a_0 = \alpha/a_0 = \alpha^2/m$. This is another way of seeing that $q\Phi$ is of order $\eta^2$.

We assume we are working in Coulomb gauge, so the longitudinal electric field is given by $\Evec_\parallel=-\del\Phi$. But since the atomic scale length $a_0$ is of order $\eta^{-1}$, the operator $\del$ must be treated as of order $1/a_0\sim\eta$. Thus we find that $q\Evec_\parallel$ is of order $\eta^3$, as indicatated in the table.

The scalar and vector potentials $\Phi$ and $\Avec$ produced by a point charge $q$ with position $\rvec$ and velocity $\vvec$ are obtained from {eq}`eq-emunits-5` and {eq}`eq-emunits-9`, with $\rho(\xvec)=q\,\delta(\xvec-\rvec)$ and $\Jvec(\xvec)=q\vvec\,\delta(\xvec-\rvec)$. These show that $\Avec\sim (v/c)\Phi$, so that $q\Avec$ is of order $\eta^3$. This means that $q\Bvec=q\del\cross\Avec$ is of order $\eta^4$. Also, the time derivative $\partial/\partial t$ must be of order $1/T_0$, that is, order $\eta^2$. Therefore the quantity $q\Evec_\perp=-q(\partial\Avec/\partial t)$, where $\Evec_\perp$ is the transverse electric field, is of order $\eta^5$. These orderings are summarized in {ref}`tbl-foldyw-1`.

(sec-foldyw-3)=

## Transforming the Hamiltonian

The Hamiltonian for a Dirac particle interacting with an electromagnetic field is

:::{math}
:label: eq-foldyw-3
\begin{array}{ccccccc}
&& \eta^0 && \eta^1 && \eta^2 \\
H &=& m\boldsymbol{\beta} &+& \boldsymbol{\alpha}\cdot\vec{\pi} &+& q\Phi,
\end{array}
:::

where the terms have been arranged in increasing order in $\eta$, as shown (that is, in decreasing order of magnitude). We work with the Dirac-Pauli representation of the Dirac matrices.

We organize the Dirac matrices into those that are “even”, that is, block-diagonal,

:::{math}
:label: eq-foldyw-4
\begin{aligned}
1=\begin{pmatrix}1 & 0 \\ 0 & 1 \\\end{pmatrix}, \qquad \beta=\begin{pmatrix}1 & 0 \\ 0 & -1 \\\end{pmatrix}, \qquad \Sigmavec=\begin{pmatrix}\sigmavec & 0 \\ 0 & \sigmavec\\\end{pmatrix},
\end{aligned}

:::

and those that are “odd”, that is, off-diagonal,

:::{math}
:label: eq-foldyw-5
\begin{aligned}
\alphavec=\begin{pmatrix}0 & \sigmavec \\ \sigmavec & 0\\\end{pmatrix},
\end{aligned}

:::

where all $4\times4$ Dirac matrices are partitioned into four $2\times2$ matrices. The only odd matrices we will need are the three components of $\alphavec$, but $\gamma_5$ is also odd and would be needed in other problems. We see that the terms of the Hamiltonian {eq}`eq-foldyw-3` that are even (odd) as Dirac matrices are also of even (odd) order in $\eta$. We will also write the Hamiltonian {eq}`eq-foldyw-3` as

:::{math}
:label: eq-foldyw-6
\begin{array}{ccccccc}
&& \eta^0 && \eta^1 && \eta^2 \\[2pt]
H &=& m\boldsymbol{\beta} &\!+\!& \odd &\!+\!& \even,
\end{array}
:::

where $\odd$ and $\even$ are the odd and even terms at order $\eta$ and $\eta^2$, respectively,

:::{math}
:label: eq-foldyw-7
\odd=\pivec\cdot\alphavec, \qquad \even=q\Phi.
:::

We shall subject the Hamiltonian {eq}`eq-foldyw-3` to a unitary transformation that eliminates the odd Dirac matrices, thereby transforming it into a new Hamiltonian which is block-diagonal. The new Dirac equation will consists of two 2-component equations that are decoupled from one another, one of which will turn out to be the Pauli equation with relativistic corrections. The transformation will be carried out as a power series expansion in powers of $\eta$, that is, $v/c$.

We write the original Dirac equation as

:::{math}
:label: eq-foldyw-8
i\frac{\partial \psi}{\partial t} = H\psi,
:::

and the new one as

:::{math}
:label: eq-foldyw-9
i\frac{\partial \psi'}{\partial t} =H'\psi',
:::

that is, with primes, where the old and new wave functions are related by

:::{math}
:label: eq-foldyw-10
\psi' = e^S \psi.
:::

We refer to $S$ as the “generator” of the transformation; we choose it to be anti-Hermitian, so that $e^S$ will be unitary. From {eq}`eq-foldyw-10` we obtain

:::{math}
:label: eq-foldyw-11
i\frac{\partial \psi'}{\partial t} = i\frac{\partial e^S}{\partial t}\,\psi + e^S i\frac{\partial \psi}{\partial t} =\Bigl(i\frac{\partial e^S}{\partial t}\,e^{-S} + e^S H e^{-S}\Bigr) \psi',
:::

so that

:::{math}
:label: eq-foldyw-12
H'=e^S H e^{-S} + i\frac{\partial e^S}{\partial t}\,e^{-S}.
:::

As we shall see, $S$ is small, that is, of positive order in $\eta$, so that we can expand the exponentials and carry out the transformation in terms of power series.

(sec-foldyw-4)=

## Expanding the New Hamiltonian

The expansion of the two terms in {eq}`eq-foldyw-12` in power series was explored in Prob. {ref}`prob-hilbert-2`. The solution involves iterated commutators of $S$ with other operators, which are conveniently expressed by the notation,

:::{math}
:label: eq-foldyw-13
L_SX = [S,X], \quad L_S^2X=[S,[S,X]], \quad L_S^3X=[S,[S,[S,X]]],
:::

etc., where $X$ is any operator and where $L_S^0X=X$. In this notation the two terms of {eq}`eq-foldyw-12` can be written

:::{math}
:label: eq-foldyw-14
e^S H e^{-S} = e^{L_S} H = \sum_{n=0}^\infty {1\over n!} L_S^n H = H + L_S H + {1\over 2!}L_S^2 H + \ldots,
:::

and

:::{math}
:label: eq-foldyw-15
i\frac{\partial e^S}{\partial t}e^{-S} = i\sum_{n=0}^\infty {1\over (n+1)!} L_S^n {\dot S}=i\Bigl( {\dot S} + {1\over 2!}L_S{\dot S} +{1\over 3!}L_S^2{\dot S} +\ldots\Bigr),
:::

where

:::{math}
:label: eq-foldyw-16
{\dot S}=\frac{\partial S}{\partial t}.
:::

We now apply the series {eq}`eq-foldyw-14` to the three terms {eq}`eq-foldyw-6`, arranging the terms so that {eq}`eq-foldyw-12` can be written

:::{math}
:label: eq-foldyw-17
\begin{array}{ccccccccccccc}
&& \eta^0 && \eta^1 && \eta^2 && \eta^3 && \eta^4 && \\[4pt]
H' &=& m\boldsymbol{\beta}
   &\!+\!& L_S(m\boldsymbol{\beta})
   &\!+\!& \frac{1}{2}L_S^2(m\boldsymbol{\beta})
   &\!+\!& \frac{1}{6}L_S^3(m\boldsymbol{\beta})
   &\!+\!& \frac{1}{24}L_S^4(m\boldsymbol{\beta})
   &\!+\!& \ldots \\[4pt]
&&&\!+\!& \odd
   &\!+\!& L_S\odd
   &\!+\!& \frac{1}{2}L_S^2\odd
   &\!+\!& \frac{1}{6}L_S^3\odd
   &\!+\!& \ldots \\[4pt]
&&&&&\!+\!& \even
   &\!+\!& L_S\even
   &\!+\!& \frac{1}{2}L_S^2\even
   &\!+\!& \ldots \\[4pt]
&&&&&&&\!+\!& \mathrlap{\text{terms in $\dot{S}$}},
&&&&
\end{array}
:::

The terms in ${\dot S}$ that are referred to come from the second term of {eq}`eq-foldyw-12`, expanded according to {eq}`eq-foldyw-15`.

(sec-foldyw-5)=

## The Generator $S$

Our strategy will be to choose the generator $S$ so that

:::{math}
:label: eq-foldyw-18
L_S(m\beta)=m[S,\beta]=-\odd,
:::

thereby killing the two terms in the $\eta^1$ column of {eq}`eq-foldyw-17`. Notice that this makes $S$ of order $\eta$, confirming that powers of $L_S$ correspond to increasing powers of $\eta$, as indicated by the columns of terms in {eq}`eq-foldyw-17`. By writing out $S$ as a $4\times4$ matrix with four unknown $2\times2$ submatrices and computing $L_S(m\beta)$ it is easy to solve for $S$. We find

:::{math}
:label: eq-foldyw-19
S={1\over 2m}\beta\odd,
:::

which is anti-Hermitian, as required. In manipulating these expressions it is worth noting that $\pivec$ is purely a spatial operator that commutes with the Dirac matrices $\alphavec$, $\beta$ and $\Sigmavec$, which are purely spin operators. The anticommutator

:::{math}
:label: eq-foldyw-20
\{\beta,\odd\}=0
:::

is also useful.

Next, from

:::{math}
:label: eq-foldyw-21
S={1\over2m}\beta(\alphavec\cdot\pivec)= {1\over 2m}\beta\alphavec\cdot(\pvec-q\Avec)
:::

we obtain

:::{math}
:label: eq-foldyw-22
{\dot S} = -{q\over 2m}\beta\alphavec\cdot\frac{\partial \Avec}{\partial t},
:::

which, by {ref}`tbl-foldyw-1`, is of order $\eta^5$ and thus off the charts in {eq}`eq-foldyw-17`. We see that through fourth order, we can ignore all terms in ${\dot S}$.

Now {eq}`eq-foldyw-18` allows us to combine the first two rows of {eq}`eq-foldyw-17`, for example,

:::{math}
:label: eq-foldyw-23
{1\over2}L_S^2(m\beta) + L_S\odd = {1\over2}L_S\odd.
:::

Then {eq}`eq-foldyw-17` becomes

:::{math}
:label: eq-foldyw-24
\begin{array}{ccccccccccc}
&& \eta^0 && \eta^2 && \eta^3 && \eta^4 && \\[2pt]
H' &=& m\boldsymbol{\beta}
   &\!+\!& \frac{1}{2}L_S\odd
   &\!+\!& \frac{1}{3}L_S^2\odd
   &\!+\!& \frac{1}{8}L_S^3\odd
   &\!+\!& \ldots \\[4pt]
&&&\!+\!& \even
   &\!+\!& L_S\even
   &\!+\!& \frac{1}{2}L_S^2\even
   &\!+\!& \ldots,
\end{array}
:::

in which the odd column at order $\eta$ has disappeared.

This shows that we will need powers of $L_S$ applied to $\odd$. The first of these is

:::{math}
:label: eq-foldyw-25
L_S\odd ={1\over2m}[\beta\odd,\odd]={1\over2m} (\beta\odd^2-\odd\beta\odd)={1\over m}\beta\odd^2,
:::

where we have used the anticommutator {eq}`eq-foldyw-20`. In a similar manner we find

:::{math}
:label: eq-foldyw-26
L_S^2\odd = -{1\over m^2}\odd^3, \qquad L_S^3\odd = -{1\over m^3}\beta\odd^4.
:::

(sec-foldyw-6)=

## The New Hamiltonian Through Second Order

Equations~{eq}`eq-foldyw-24` and {eq}`eq-foldyw-25` show that the second order Hamiltonian involves the operator $\odd^2$, which we put into a useful form as follows. First, noting that all components of $\pivec$ commute with all components of $\alphavec$, we have

:::{math}
:label: eq-foldyw-27
\odd^2 = (\alphavec\cdot\pivec)^2 = \alpha_i\pi_i \alpha_j\pi_j = \alpha_i\alpha_j\pi_i\pi_j.
:::

Next, by using the definitions {eq}`eq-foldyw-4` and {eq}`eq-foldyw-5` we verify the useful identity,

:::{math}
:label: eq-foldyw-28
\alpha_i\alpha_j = \delta_{ij} + i\epsilon_{ijk}\, \Sigma_k,
:::

which shows that

:::{math}
:label: eq-foldyw-29
\odd^2 = \pivec^2 + i\epsilon_{ijk}\,\Sigma_k \pi_i\pi_j.
:::

In the final term in this equation we note that $\epsilon_{ijk}$ is antisymmetric in $(ij)$, so this term can be written

:::{math}
:label: eq-foldyw-30
{i\over2}\epsilon_{ijk}\,\Sigma_k(\pi_i\pi_j-\pi_j\pi_i) ={i\over2}\epsilon_{ijk}\,\Sigma_k\,[\pi_i,\pi_j].
:::

But it follows from the definition {eq}`eq-foldyw-2` that

:::{math}
:label: eq-foldyw-31
[\pi_i,\pi_j]=iq\,\epsilon_{ij\ell}\, B_\ell,
:::

which are essentially the velocity commutators previously derived as {eq}`eq-magfield-5`. These commutators also appeared in Prob. {ref}`prob-tevolut-1`. Thus the expression {eq}`eq-foldyw-30` can be written

:::{math}
:label: eq-foldyw-32
-{q\over 2} \epsilon_{ijk}\, \Sigma_k \, \epsilon_{ij\ell}\, B_\ell = -q\,\delta_{k\ell} \Sigma_k B_\ell = -q\Sigmavec\cdot\Bvec,
:::

where we use {eq}`eq-tensor-52`. Altogether, we obtain

:::{math}
:label: eq-foldyw-33
\odd^2 = \pivec^2 -q\Sigmavec\cdot\Bvec.
:::

This work allows us to write the new Hamiltonian through second order as

:::{math}
:label: eq-foldyw-34
H' = m\beta + {1\over2m}\beta(\pivec^2-q\Sigmavec\cdot\Bvec) +q\Phi + O(\eta^3).
:::

To second order in $\eta$ the Hamiltonian has been block-diagonalized. The upper 2-components of the transformed Dirac equation through second order have now become the usual Pauli equation {eq}`eq-dirac-1`, with $g=2$ and the constant term $mc^2$ added to the Hamiltonian. The calculation thus far is equivalent to what we did in an *ad hoc* manner in {ref}`sec-dirac-9`, but we have all the higher order terms and can continue with the expansion.

(sec-foldyw-7)=

## A Second Foldy-Wouthuysen Transformation

The transformation so far has eliminated the odd contribution to the Hamiltonian at order $\eta$, but the odd term at order $\eta^3$ remains. It is

:::{math}
:label: eq-foldyw-35
H'_3 = {1\over3}L_S^2\odd + L_S\even.
:::

To eliminate this term we must carry out a second Foldy-Wouthousen transformation, this time with a generator $S'$ that takes $H'$ into a new Hamiltonian $H''$. That is, we write

:::{math}
:label: eq-foldyw-36
H''=e^{S'}H'e^{-S'} + i\pop{e^{S'}}{t}e^{-S'},
:::

a version of {eq}`eq-foldyw-12`, taken to the next step. Expanding the exponentials in power series as before, we find that to eliminate $H'_3$ we must find $S'$ such that

:::{math}
:label: eq-foldyw-37
L_{S'}(m\beta)=m[S',\beta]=-H'_3.
:::

But we do not need to solve this equation explicitly, we only need to note that a solution exists, and that it gives $S'$ which is of order $\eta^3$.

(sec-foldyw-8)=

## The New Hamiltonian at Fourth Order

With this knowledge we can see that all other commutators and correction terms in {eq}`eq-foldyw-36` are of order $\eta^5$ and higher. Thus we find

:::{math}
:label: eq-foldyw-38
H''_4 = H'_4 = {1\over8}L_S^3\odd + {1\over2}L_S^2\even = -{1\over 8m^3}\beta\odd^4 + {1\over2}L_S^2\even,
:::

where we use {eq}`eq-foldyw-26`. As for $\odd^4$, if we only want this to fourth order in $\eta$ we can ignore the correction term in {eq}`eq-foldyw-33`, which by {ref}`tbl-foldyw-1` is of order $\eta^4$. For the same reason we can ignore the correction term in Eq.{eq}`eq-foldyw-2`, which according to the table is of order $\eta^3$. Thus

:::{math}
:label: eq-foldyw-39
\odd^4 = (\pivec^2-q\Sigmavec\cdot\Bvec)^2 \to \pivec^4 = (\pvec-q\Avec)^4 \to p^4,
:::

where $\to$ means dropping terms of order $\eta^5$ or higher. Altogether, the first term in $H''_4$ in {eq}`eq-foldyw-38` becomes

:::{math}
:label: eq-foldyw-40
{1\over8}L_S^3\odd \to -\beta{p^4\over 8m^3}.
:::

To compute the second term in {eq}`eq-foldyw-38` we start with

:::{math}
:label: eq-foldyw-41
L_S\even = {1\over 2m}[\beta\odd,\even] ={q\over2m}[\beta\alpha_i\pi_i,\Phi] ={q\over2m}\beta\alpha_i[\pi_i,\Phi],
:::

since $\beta$ and $\alpha_i$ are spin operators and $\pi_i$ and $\Phi$ are spatial. But

:::{math}
:label: eq-foldyw-42
[\pi_i,\Phi] = [p_i,\Phi] = -i\frac{\partial \Phi}{\partial x_i} \to i E_i,
:::

where in the last step we drop the transverse electric field which is of higher order, as noted in {ref}`tbl-foldyw-1`. Thus we find

:::{math}
:label: eq-foldyw-43
L_S\even = {iq\over 2m}\beta(\alphavec\cdot\Evec),
:::

to the order required.

We must now apply $L_S$ to this. We obtain

:::{math}
:label: eq-foldyw-44
\begin{aligned}
L_S^2\even &= {iq\over 4m^2}[\beta\odd, \beta(\alphavec\cdot\Evec)] = {iq\over 4m^2} [\beta\odd\beta(\alpha\cdot\Evec)- \beta(\alphavec\cdot\Evec)\beta\odd] =-{iq\over 4m^2}[\odd,\alphavec\cdot\Evec] \\
&\to -{iq\over 4m^2}[\alphavec\cdot\pvec,\alphavec\cdot\Evec], \\

\end{aligned}
:::

where we use the anticommutator $\{\beta,\alpha_i\}=0$ and drop the correction term in {eq}`eq-foldyw-2`. The remaining commutator is

:::{math}
:label: eq-foldyw-45
\begin{aligned}
[\alphavec\cdot\pvec,\alphavec\cdot\Evec] &= \alpha_ip_i\alpha_jE_j-\alpha_iE_i\alpha_jp_j =\alpha_i\alpha_j(p_iE_j-E_ip_j) \\
&=(\delta_{ij}+i\epsilon_{ijk}\,\Sigma_k)(p_iE_j-E_ip_j) = \pvec\cdot\Evec-\Evec\cdot\pvec +i\Sigmavec\cdot(\pvec\cross\Evec-\Evec\cross\pvec), \\

\end{aligned}
:::

where we have used the identity {eq}`eq-foldyw-28`. This can be simplified with

:::{math}
:label: eq-foldyw-46
\pvec\cdot\Evec-\Evec\cdot\pvec = [p_i,E_i] = -i\del\cdot\Evec.
:::

Now putting the pieces together we obtain the total fourth order Hamiltonian as

:::{math}
:label: eq-foldyw-47
H''_4 = {1\over8}L_S^3\odd+{1\over2}L_S^2\even = -\beta{p^4\over 8m^3} -{q\over8m^2}\del\cdot\Evec + {q\over8m^2} \Sigmavec\cdot(\pvec\cross\Evec-\Evec\cross\pvec),
:::

to the order required. The Hamiltonian is now block-diagonalized through fourth order in $v/c$. The total Hamiltonian through fourth order is obtained by adding this term to {eq}`eq-foldyw-34`.

(sec-foldyw-9)=

## The Upper Two Components

To obtain the effective 2-component Hamiltonian for the upper two components of the transformed Dirac spinor $\psi''$ we just replace the Dirac matrices $\beta$ and $\Sigmavec$ by their upper $2\times2$ blocks, which are 1 and $\sigmavec$, respectively. Writing simply $H$ for this Hamiltonian, it is

:::{math}
:label: eq-foldyw-48
H=m + {\pivec^2\over 2m} -{q\over2m}\sigmavec\cdot\Bvec +q\Phi -{p^4\over 8m^3} -{q\over8m^2}\del\cdot\Evec +{q\over8m^2}\sigmavec\cdot(\pvec\cross\Evec-\Evec\cross\pvec).
:::

We restore ordinary units to this, obtaining

:::{math}
:label: eq-foldyw-49
\begin{aligned}
H & = mc^2 + {1\over2m}\Bigl(\pvec-{q\over c}\Avec\Bigr)^2 -g{q\hbar\over2mc}\Svec\cdot\Bvec + q\Phi -{p^4\over 8m^3c^2} -{q\hbar^2\over8m^2c^2}\del\cdot\Evec \\
 & \qquad-{q\over4m^2c^2}\Svec\cdot(\pvec \cross\Evec-\Evec \cross\pvec),
\end{aligned}
:::

where we write $\pivec=\pvec-(q/c)\Avec$, $\Svec=(\hbar/2)\sigmavec$ and $g=2$.

The last three terms of this Hamiltonian are the correction terms at order $(v/c)^4$. The first of these is the relativistic kinetic energy correction, denoted $H_RKE$ in {eq}`eq-finestruc-5`. In the second of these we write $\Evec=-\del\Phi$ and $V=q\Phi$, so that it becomes

:::{math}
:label: eq-foldyw-50
{\hbar^2\over 8m^2c^2}\del^2V,
:::

which is precisely the Darwin term given previously in {eq}`eq-finestruc-23`. The final term in {eq}`eq-foldyw-49` is the spin-orbit term, which which we have previously considered only in the case of a central force potential. To specialize to that case, we assume $\Phi=\Phi(r)$ so that

:::{math}
:label: eq-foldyw-51
q\Evec=-q\del\Phi(r) = -q{\xvec\over r}\dod{\Phi}{r} = -{\xvec\over r} \dod{V}{r}.
:::

Then

:::{math}
:label: eq-foldyw-52
q\pvec\cross\Evec=-(\pvec\cross\xvec){1\over r}\dod{V}{r} = {1\over r}\dod{V}{r}\Lvec = -q\Evec\cross\pvec,
:::

so that for central force potentials the final term of {eq}`eq-foldyw-49` can be written

:::{math}
:label: eq-foldyw-53
{1\over 2m^2c^2}{1\over r}\dod{V}{r} \Lvec\cdot\Svec,
:::

which is the spin-orbit term seen previously in {eq}`eq-finestruc-13`.

(sec-foldyw-10)=

## Discussion

In the pseudo-derivation of the spin-orbit term given in {ref}`ch-finestruc`{} we glossed over the derivation of the extra factor of $1/2$ due to Thomas precession, because it would have been a substantial excursion to go into it in detail. Nevertheless, it is interesting to see how rotations can be generated by the composition of boosts, and the physical consequences of these. The Dirac equation, however, implicitly knows about Thomas precession, and about how the extra rotation effectively cancels out one half of the precession of the spin in the electron's rest frame. The Dirac equation also implicitly knows that the $g$ factor of the electron is 2 (very nearly).

In the case of hydrogen the Dirac equation gives results that are in agreement with spectroscopic data to high precision, the main discrepancies being the hyperfine structure and the Lamb shift, both of which involve extra physics not incorporated into the Dirac equation. The same can be said for the corrections to the $g$-factor, which along with the Lamb shift are due to interactions with the electromagnetic field (they are so-called “radiative corrections”). Of course there are also corrections due to the finite mass of the nucleus, which are mostly accounted for by replacing the electron mass $m$ by the reduced mass $\mu$. To account for these in a manner that is fully satisfactory from a fundamental standpoint, however, is more challenging.

Perhaps the most important point of these results concerns our narrative on the development of our understanding of the Dirac equation. The ingredients in the Dirac equation are the simplest that can be conceived for a relativistic wave equation for a particle with spin. The implementation of the Dirac algebra is the simplest, and the coupling to the electromagnetic field is minimal. The fact that such a large amount of physically correct detail, in excellent agreement with experiment, emerges from these assumptions is impressive evidence that the Dirac equation is an important and largely correct step in the merging of quantum mechanics with special relativity. Nothing we have said so far, however, sheds any light on the meaning of the negative energy solutions of the Dirac equation, which are the main conceptual difficulty that must be solved before we have a fully satisfactory framework for understanding relativistic quantum mechanics. The next few sets of notes outline the resolution of this problem.

\problems

(prob-foldyw-1)=

**Problem \prbdfoldyw-1..** 

(prob-foldyw-2)=

**Problem \prbdfoldyw-2..**
