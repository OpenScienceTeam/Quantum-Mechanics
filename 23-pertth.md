---
title: "23. Bound-State Perturbation Theory"
---
(ch-pertth)=

# 23. Bound-State Perturbation Theory

(sec-pertth-1)=

## Introduction

Bound state perturbation theory applies to the bound states of perturbed systems, for which the energy levels are discrete and separated from one another. The system may also have a continuous spectrum, but the interest is attached to the discrete states. The effects of perturbations on states of the continuous spectrum, or on discrete states imbedded in the continuum, require different techniques, such as time-dependent perturbation theory.

The version of bound-state perturbation theory that you are probably familiar with is called Rayleigh-Schr\"odinger perturbation theory. In these notes, we will begin with a variation on Rayleigh-Schr\"odinger perturbation theory, called Brillouin-Wigner perturbation theory. The Brillouin-Wigner theory is simpler and less messy to derive than the Rayleigh-Schr\"odinger theory, and it also gives more accurate answers in many circumstances. Its disadvantage is that the unknown energy levels are given only implicitly, in terms of the solutions of nonlinear equations. But if explicit formulas for the energy levels are desired, it is easy to expand the solutions in powers of the perturbation parameter, whereupon the results of the Rayleigh-Schr\"odinger theory are recovered. In my opinion, this is the easiest and most elegant way to derive Rayleigh-Schr\"odinger perturbation theory.

(sec-pertth-2)=

## The Unperturbed and Perturbed States

We consider an unperturbed Hamiltonian $H_0$ with eigenvalues $\epsilon_k$ and eigenstates $\ket{k\alpha}$, where $\alpha$ is an index introduced to resolve degeneracies, so that

:::{math}
:label: eq-pertth-1
H_0\ket{k\alpha} = \epsilon_k\ket{k\alpha}.
:::

See {ref}`fig-pertth-1`, in which the unperturbed levels $\epsilon_k$ are illustrated on a vertical axis. Although we use a notation appropriate for a discrete spectrum of $H_0$, we actually allow it to have a mixed spectrum, typically a continuous spectrum above some energy and a discrete one below that, as often happens in practice. Sums over states, such as {eq}`eq-pertth-4`, must be interpreted as including the continuous part of the spectrum, as necessary, as shown for example in {eq}`eq-hilbert-109` and {eq}`eq-hilbert-110`.

We pick one of the discrete levels $\epsilon_n$ for study, so the index $n$ will be fixed for the following discussion. We denote the eigenspace of the unperturbed system corresponding to eigenvalue $\epsilon_n$ by $\HS_n$, so that the unperturbed eigenkets $\{ \ket{n\alpha}, \alpha=1,2,\ldots \}$ form a basis in this space.

:::{figure} images/pertth-fig01.png
:label: fig-pertth-1
:width: 80%

The energy levels $\epsilon_k$ of the unperturbed system $H_0$ are shown on a vertical axis. These levels are degenerate in general. One of these, $\epsilon_n$, is selected out for study. When the perturbation $H_1$ is turned on, level $\epsilon_n$ may split and shift. The energy level $E$ of the perturbed system $H_0+\lambda H_1$ is one that grows out of $\epsilon_n$ as the perturbation is turned on.
:::

:::{figure} images/pertth-fig02.png
:label: fig-pertth-2
:width: 80%

Subspace $\HS_n$ is the unperturbed eigenspace for level $\epsilon_n$, and $\HS_n^\perp$ is the orthogonal subspace. Projectors $P$ and $Q$ project onto $\HS_n$ and $\HS_n^\perp$, respectively. The exact eigenstate lies approximately in $\HS_n$, with a small correction $Q\ket{\psi}$ orthogonal to this subspace.
:::


We take the perturbed Hamiltonian to be $H=H_0+\lambda H_1$, where $\lambda$ is a formal expansion parameter that we allow to vary between 0 and 1 to interpolate between the unperturbed and perturbed system. When the perturbation is turned on, the unperturbed energy level $\epsilon_n$ may split and shift. We denote one of the exact energy levels that grows out of $\epsilon_n$ by $E$, as shown in {ref}`fig-pertth-1`. We let $\ket{\psi}$ be an exact energy eigenket corresponding to energy $E$, so that

:::{math}
:label: eq-pertth-2
H\ket{\psi}=(H_0+\lambda H_1)\ket{\psi} = E \ket{\psi}.
:::

Both $E$ and $\psi$ are understood to be functions of $\lambda$; as $\lambda\to 0$, $E$ approaches $\epsilon_n$ and $\ket{\psi}$ approaches some state lying in $\HS_n$. {eq}`eq-pertth-2` only determines $\ket{\psi}$ to within a normalization and phase, which can be functions of $\lambda$; we are free to choose as we wish these to simplify our work.

It helps to have a picture of the perturbation problem in terms of the geometry of Hilbert space. We break the Hilbert space into the subspace $\HS_n$ and its orthogonal complement which we denote by $\HS_n^\perp$. The latter space is spanned by the unperturbed eigenkets $\{ \ket{k\alpha}\}$ for all $k \ne n$. Since the perturbation is small, the exact eigenket $\ket{\psi}$ presumably lies nearly in $\HS_n$, with only a small component orthogonal to $\HS_n$, as illustrated in {ref}`fig-pertth-2`. The components of $\ket{\psi}$ parallel and perpendicular to $\HS_n$ are conveniently expressed in terms of the projector $P$ onto the subspace $\HS_n$ and the orthogonal projector $Q$, defined by

:::{math}
:label: eq-pertth-3
P=\sum_\alpha \ketbra{n\alpha}{n\alpha},
:::

and

:::{math}
:label: eq-pertth-4
Q=\sum_{\substack{k\ne n \\ \alpha}} \ketbra{k\alpha}{k\alpha}.
:::

These projectors satisfy $P^2=P$, $Q^2=Q$, $PQ=QP=0$ and $P+Q=1$. They also commute with $H_0$,

:::{math}
:label: eq-pertth-5
[P,H_0] = [Q,H_0]=0,
:::

since they project onto eigenspaces of $H_0$. In terms of these projectors, the components of $\ket{\psi}$ parallel and perpendicular to $\HS_n$ are $P\ket{\psi}$ and $Q\ket{\psi}$, respectively, as illustrated in {ref}`fig-pertth-2`.

The component $P\ket{\psi}$ of the exact eigenstate $\ket{\psi}$ lies in the unperturbed eigenspace, and thus is itself an unperturbed eigenstate. It is therefore a linear combination of the known unperturbed eigenstates $\{\ket{n\alpha}, \alpha =1,2, \ldots \}$. The orthogonal component $Q\ket{\psi}$, on the other hand, is harder to find. In the following we will think of $P\ket{\psi}$ as the easy part of $\ket{\psi}$ and $Q\ket{\psi}$ as the hard part, and attempt to solve for the hard part $Q\ket{\psi}$ (or else the total solution $\ket{\psi} = P\ket{\psi}+Q\ket{\psi}$) in terms of the easy part $P\ket{\psi}$. It turns out it is possible to write a neat power series expansion for this solution, {eq}`eq-pertth-16` below.

As a first step in the derivation of this series, we rearrange {eq}`eq-pertth-2` in the form,

:::{math}
:label: eq-pertth-6
(E-H_0)\ket{\psi} = \lambda H_1\ket{\psi}.
:::

We would like to divide this equation by $E-H_0$ to solve for $\ket{\psi}$, but before proceeding we must examine $(E-H_0)^{-1}$ to see if it is well behaved. The idea of dividing by $E-H_0$ is closely related to the use of Green's functions. See {ref}`ch-greensfuns`, where the basic idea is presented and developed.

(sec-pertth-3)=

## The Inverse of $E-H_0$ on $\HS_n^\perp$

The operator $(E-H_0)^{-1}$ is a function of the operator $H_0$, which according to {eq}`eq-hilbert-129` can be written in terms of the eigenvalues and projectors of $H_0$,

:::{math}
:label: eq-pertth-7
{1\over E-H_0} = \sum_{k\alpha} {\ketbra{k\alpha}{k\alpha} \over E-\epsilon_k}.
:::

The resulting expression, however, is meaningless if the exact eigenvalue $E$ should equal any of the unperturbed eigenvalues $\epsilon_k$. In that case, one or more denominators vanish, indicating that $E-H_0$ does not possess an inverse. Even if none of the denominators vanishes, nevertheless the exact eigenvalue $E$ is presumably close to the unperturbed eigenvalue $\epsilon_n$, and therefore the terms $k=n$ in {eq}`eq-pertth-7` are large (and these terms diverge at $\lambda=0$, where $E=\epsilon_n$).

In order to avoid small or vanishing denominators, and to work with operators that are guaranteed to be well defined, we define a new operator $R$ which is {eq}`eq-pertth-7` with the terms $k=n$ suppressed:

:::{math}
:label: eq-pertth-8
R=\sum_{\substack{k\ne n \\ \alpha}} {\ketbra{k\alpha}{k\alpha} \over E-\epsilon_k}.
:::

The operator $R$ is closely related to the Green's operators that we shall consider later in the course, when we take up scattering theory.

It is possible that $E-\epsilon_n$ is not the only small or vanishing denominator in {eq}`eq-pertth-7`. For example, if there are other unperturbed energy levels $\epsilon_k$ lying close to $\epsilon_n$, then the perturbation could push the exact energy $E$ near to or past some of these other levels, and then other small denominators would result in {eq}`eq-pertth-7`. This will certainly happen if the perturbation is large enough. For the time being we will assume this does not happen, so that {eq}`eq-pertth-8` is free of small denominators. This is the situation illustrated in {ref}`fig-pertth-1`. When this is not the case we shall refer to “nearly degenerate perturbation theory,” which is discussed in \secrpertth-7.

The operator $R$ satisfies

:::{math}
:label: eq-pertth-9
\begin{aligned}
PR &= RP = 0, \\
QR &= RQ = R, \\

\end{aligned}
:::

and

:::{math}
:label: eq-pertth-10
R(E-H_0)=(E-H_0)R=Q.
:::

These equations show that $R$ vanishes on the subspace $\HS_n$, while it is the inverse of $E-H_0$ on the subspace $\HS_n^\perp$. Note that $Q$ is just the identity operator on $\HS_n^\perp$.

(sec-pertth-4)=

## A series for $\ket{\psi}$ in terms of $P\ket{\psi}$

We return now to {eq}`eq-pertth-6` and multiply through by $R$, using {eq}`eq-pertth-10`. This gives

:::{math}
:label: eq-pertth-11
Q\ket{\psi} = \lambda RH_1\ket{\psi},
:::

which expresses the “hard” part of the exact eigenstate $Q\ket{\psi}$ in terms of the total exact eigenstate $\ket{\psi}$. To turn this into something more useful, we first add $P\ket{\psi}$ to both sides, obtaining

:::{math}
:label: eq-pertth-12
\ket{\psi} = P\ket{\psi} + \lambda RH_1\ket{\psi}.
:::

This expresses the exact eigenket $\ket{\psi}$ in terms of its projections onto $\HS_n$ and $\HS_n^\perp$, of which the second term is a small correction. It is not an explicit solution for $\ket{\psi}$ since $\ket{\psi}$ occurs on the right hand side, but it can be converted into a power series solution by a method of successive approximation.

In particular, note that if we neglect the second term in {eq}`eq-pertth-12`, which is of order $\lambda$, we obtain $\ket{\psi} = P\ket{\psi}$, which is correct to lowest order. To improve on the approximation, we substitute the left hand side of {eq}`eq-pertth-12` into the second term on the right hand side, obtaining,

:::{math}
:label: eq-pertth-13
\ket{\psi} = P\ket{\psi} + \lambda RH_1 P \ket{\psi} + \lambda^2 RH_1 RH_1 \ket{\psi},
:::

which is still an exact equation. Now all terms on the right hand side except the last one involve the “easy” part $P\ket{\psi}$ of the exact eigenstate, and only the final term, which is second order in the perturbation, involves $\ket{\psi}$. If we neglect that term, we obtain an expression for $\ket{\psi}$ in terms of $P\ket{\psi}$ that is valid to first order in $\lambda$. Continuing this way, we can substitute the left hand side of {eq}`eq-pertth-12` into the last term in {eq}`eq-pertth-13`, to push the hard term to fourth order in $\lambda$, etc. The result is a formal power series for the solution $\ket{\psi}$ in terms of the easy part $P\ket{\psi}$.

Another way to get the same thing is to rearrange {eq}`eq-pertth-12`,

:::{math}
:label: eq-pertth-14
(1-\lambda RH_1) \ket{\psi} = P \ket{\psi},
:::

so that

:::{math}
:label: eq-pertth-15
\ket{\psi} = \Bigl({1 \over 1-\lambda RH_1}\Bigr) P\ket{\psi}.
:::

The inverse operator is then easily expanded in a series,

:::{math}
\begin{aligned}
\ket{\psi} &= \sum_{s=0}^\infty \lambda^s (RH_1)^s P\ket{\psi}
\end{aligned}
:::

:::{math}
:label: eq-pertth-16
\begin{aligned}
&= P\ket{\psi} + \lambda RH_1 P\ket{\psi} + \lambda^2 RH_1RH_1 P\ket{\psi} + \ldots.
\end{aligned}
:::

This is the basic series out of which all the results of perturbation theory are constructed. The series might not converge, but in perturbation theory we do not necessarily need convergent series.

(sec-pertth-5)=

## Nondegenerate Perturbation Theory

In nondegenerate perturbation theory the level $\epsilon_n$ of $H_0$ is nondegenerate. Then the index $\alpha$ is not needed for the level $\epsilon_n$, and we can write simply $\ket{n}$ for the corresponding eigenstate. We retain $\alpha$ for the other levels $k\ne n$, since these may still be degenerate. Then since the space $\HS_n$ is 1-dimensional and is spanned by $\ket{n}$, we must have $P\ket{\psi} = c\ket{n}$, where $c$ is some constant. It is obvious from {ref}`fig-pertth-2` that $\ket{\psi}$ and $P\ket{\psi}$ cannot both be normalized, since one is the base and the other the hypotenuse of a right triangle. In the following it is convenient to choose the normalization and phase of $\ket{\psi}$ so that $c=1$. Thus we have

:::{math}
:label: eq-pertth-17
P\ket{\psi} =	\ket{n},
:::

where we assume that $\ket{n}$ and the other unperturbed eigenstates are normalized. This is the most convenient normalization convention for nondegenerate perturbation theory, but it means that $\ket{\psi}$ is not normalized, in fact from {ref}`fig-pertth-2` it is clear that $\braket{\psi}{\psi} > 1$, since the hypoteneuse is longer than the base. After we are done with the perturbation expansion, we are free to normalize $\ket{\psi}$ in the usual way. With this normalization convention, we have

:::{math}
:label: eq-pertth-18
\braket{n}{\psi} = 1.
:::

Now the series {eq}`eq-pertth-16` becomes

:::{math}
\begin{aligned}
\ket{\psi} &= \sum_{s=0}^\infty \lambda^s (RH_1)^s \ket{n}
\end{aligned}
:::

:::{math}
\begin{aligned}
&= \ket{n} + \lambda RH_1 \ket{n} +\lambda^2 RH_1RH_1 \ket{n} + \ldots
\end{aligned}
:::

:::{math}
:label: eq-pertth-19
\begin{aligned}
&= \ket{n} + \lambda\sum_{\substack{k\ne n \\ \alpha}} \ket{k\alpha}{\matrixelement{k\alpha}{H_1}{n} \over   E-\epsilon_k} \\  &\qquad+\lambda^2\sum_{\substack{k\ne n \\ \alpha}} \sum_{\substack{k' \ne n \\ \alpha'}} \ket{k\alpha}{\matrixelement{k\alpha}{H_1}{k'\alpha'} \matrixelement{k'\alpha'}{H_1}{n} \over (E-\epsilon_k)(E-\epsilon_{k'})} +\ldots \\
\end{aligned}

:::

which expresses the exact eigenket $\ket{\psi}$ as an infinite series in terms of the unperturbed eigenket $\ket{n}$. However, the operator $R$ still involves the unknown energy level $E$, which appears in the denominators, so {eq}`eq-pertth-19` is still not an explicit solution for the exact eigenket $\ket{\psi}$.

To find an equation for $E$, we multiply {eq}`eq-pertth-6` on the left by $\bra{n}$ and use {eq}`eq-pertth-18` to get

:::{math}
:label: eq-pertth-20
\matrixelement{n}{(E-H_0)}{\psi} = E-\epsilon_n = \lambda \matrixelement{n}{H_1}{\psi},
:::

and then we substitute {eq}`eq-pertth-19` into this. Thus we find

:::{math}
\begin{aligned}
E &= \epsilon_n + \lambda\matrixelement{n}{H_1}{n} + \lambda^2 \matrixelement{n}{H_1RH_1}{n} + \lambda^3 \matrixelement{n}{H_1RH_1RH_1}{n} + \ldots
\end{aligned}
:::

:::{math}
:label: eq-pertth-21
\begin{aligned}
&=\epsilon_n + \lambda\matrixelement{n}{H_1}{n}+ \lambda^2\sum_{\substack{k\ne n \\ \alpha}} {\matrixelement{n}{H_1}{k\alpha} \matrixelement{k\alpha}{H_1}{n} \over E-\epsilon_k} \\  & \qquad +\lambda^3 \sum_{\substack{k\ne n \\ \alpha}} \sum_{\substack{k' \ne n \\ \alpha'}} { \matrixelement{n}{H_1}{k\alpha} \matrixelement{k\alpha}{H_1}{k'\alpha'} \matrixelement{k'\alpha'}{H_1}{n} \over (E-\epsilon_k)(E-\epsilon_{k'})} +\ldots.
\end{aligned}

:::

Since the unknown exact energy $E$ still appears in the denominators on the right hand side of this equation, this is not an explicit solution for $E$. But {eq}`eq-pertth-21` does give $E$ explicitly through $O(\lambda)$,

:::{math}
:label: eq-pertth-22
E = \epsilon_n + \lambda \matrixelement{n}{H_1}{n} +O(\lambda^2),
:::

which agrees with the usual result of Rayleigh-Schr\"odinger perturbation theory. If we want the energy correct through $O(\lambda^2)$, we can substitute the zeroth order approximation for $E$, namely, $E=\epsilon_n$, into the denominator of the $O(\lambda^2)$ term in {eq}`eq-pertth-21`, whereupon we find

:::{math}
:label: eq-pertth-23
E=\epsilon_n + \lambda\matrixelement{n}{H_1}{n}+ \lambda^2\sum_{\substack{k\ne n \\ \alpha}} {\matrixelement{n}{H_1}{k\alpha} \matrixelement{k\alpha}{H_1}{n} \over \epsilon_n-\epsilon_k} +O(\lambda^3),
:::

which agrees with Rayleigh-Schr\"odinger theory through $O(\lambda^2)$. Similarly, if we wish the energy correct to $O(\lambda^3)$, we can substitute the first order expression {eq}`eq-pertth-22` for $E$ into the denominator of the $O(\lambda^2)$ term in {eq}`eq-pertth-21`, and the zeroth order expression $E=\epsilon_n$ into the $O(\lambda^3)$ term, etc. When the denominators are expanded out in powers of $\lambda$, the results of Rayleigh-Schr\"odinger perturbation theory are recovered. At third order and beyond, the expressions of the Raleigh-Schr\"odinger theory are more complicated than those of the Brillouin-Wigner theory, because of the extra terms that come from expanding the denominators.

Once the energy $E$ has been determined in this manner, we can go back to {eq}`eq-pertth-19` and obtain the eigenkets. For example, through first order we have

:::{math}
:label: eq-pertth-24
\ket{\psi}= \ket{n} + \lambda\sum_{\substack{k\ne n \\ \alpha}} \ket{k\alpha}{\matrixelement{k\alpha}{H_1}{n} \over   \epsilon_n-\epsilon_k}+ O(\lambda^2),
:::

which again is the usual result from Rayleigh-Schr\"odinger perturbation theory.

(sec-pertth-6)=

## Degenerate Perturbation Theory

In the case that the unperturbed energy level $\epsilon_n$ is degenerate, the projection of the exact eigenket $\ket{\psi}$ onto $\HS_n$ must be a linear combination of the unperturbed eigenkets $\ket{n\alpha}$,

:::{math}
:label: eq-pertth-25
P\ket{\psi} = \sum_\alpha \ket{n\alpha} c_\alpha,
:::

where $c_\alpha$ are the expansion coefficients. Since $Q\ket{\psi}$ is orthogonal to all the kets $\ket{n\alpha}$, we have

:::{math}
:label: eq-pertth-26
\matrixelement{n\alpha}{P}{\psi}= \braket{n\alpha}{\psi} = c_\alpha.
:::

To obtain an equation for the $c_\alpha$'s, we multiply {eq}`eq-pertth-6` on the left by $\bra{n\alpha}$ and use {eq}`eq-pertth-26` to obtain,

:::{math}
:label: eq-pertth-27
\matrixelement{n\alpha}{(E-H_0)}{\psi} =(E-\epsilon_n)c_\alpha = \lambda \matrixelement{n\alpha}{H_1}{\psi}.
:::

We substitute {eq}`eq-pertth-16` into this, using {eq}`eq-pertth-25` for $P\ket{\psi}$, and we find

:::{math}
\begin{aligned}
(E-\epsilon_n)c_\alpha &= \sum_\beta\Bigl[\lambda \matrixelement{n\alpha}{H_1}{n\beta} + \lambda^2 \matrixelement{n\alpha}{H_1RH_1}{n\beta} +\ldots\Bigr]c_\beta
\end{aligned}
:::

:::{math}
:label: eq-pertth-28
\begin{aligned}
&= \sum_\beta\Biggl[\lambda \matrixelement{n\alpha}{H_1}{n\beta} + \lambda^2 \sum_{\substack{k\ne n \\ \gamma}} {\matrixelement{n\alpha}{H_1}{k\gamma} \matrixelement{k\gamma}{H_1}{n\beta} \over E-\epsilon_k} +\ldots\Biggr]c_\beta. \\
\end{aligned}

:::

This equation must be solved simultaneously for the eigenvalues $E$ and the unknown expansion coefficients $c_\alpha$.

We see that the expansion coefficients $c_\alpha$, which determine $P\ket{\psi}$ by {eq}`eq-pertth-25`, are the eigenvectors of a $g\times g$ matrix, where $g$ is the degeneracy of the unperturbed eigenvalue $\epsilon_n$, and that the energy shifts $E-\epsilon_n$ are the eigenvalues. But this is not the standard problem of determining the eigenvalues and eigenvectors of a matrix, because the unknown energies $E$ appear not only on the left-hand side but also in the denominators in the second and higher order terms of the matrix.

In practice, however, the most common type of problem is one in which we desire the energy shifts to first order in $\lambda$. We can find these by truncating the series in {eq}`eq-pertth-28` at first order, whereupon the energy shifts $E-\epsilon_n$ are the eigenvalues of the matrix $\matrixelement{n\alpha}{H_1}{n\beta}$, that is, they are the eigenvalues of the matrix of the perturbing Hamiltonian inside the degenerate eigenspace of unperturbed system. At this order there are no energy denominators to worry about and we can just diagonalize the matrix. Also, the eigenvectors $c_\alpha$ corresponding to the energy shifts determine $P\ket{\psi}$ via {eq}`eq-pertth-25`, so that the perturbed eigenkets are known to zeroth order. In many applications this is sufficient (see, for example, the treatmant of the Stark effect on the $n=2$ levels of hydrogen in {ref}`sec-stark-12`).

The first order matrix $\matrixelement{n\alpha}{H_1}{n\beta}$ may or may not have degeneracies itself. If it does not, then all degeneracies are lifted at first order; if it does, the remaining degeneracies may be lifted at a higher order, or may persist to all orders. Degeneracies that persist to all orders are almost always due to some symmetry of the system, which can usually be recognized at the outset.

To proceed to second order, we may substitute the zeroth order solution $E=\epsilon_n$ into the denominators of the second order term in {eq}`eq-pertth-28` and truncate the series at this order. We then obtain a new eigenvalue-eigenvector problem for the unknown energy corrections $E-\epsilon_n$ and coefficients $c_\alpha$, which differs from the one we had at first order by the addition of a second order matrix as a correction to the matrix $\matrixelement{n\alpha} {H_1} {n\beta}$ that we had at first order. We can evaluate the eigenvalues and eigenvectors of the sum of these two matrices by standard matrix techniques, or we can regard the new eigenvalue-eigenvector problem as a new problem in bound state perturbation theory, in which the first order matrix $\matrixelement{n\alpha} {H_1} {n\beta}$ plays the role of a new unperturbed Hamiltonian, say, $\tilde H_0$, and the second order matrix plays the role of a new perturbation, say, $\tilde H_1$. We will have to use either the nondegenerate or degenerate versions of this theory, depending on whether or not all degeneracies of the original Hamiltonian $H_0$ were lifted at first order. In any case, once the energies $E$ and coefficients $c_\alpha$ have been determined to some order, they can be substituted into {eq}`eq-pertth-25` to determine $P\ket{\psi}$.

Finally, once $E$ and $P\ket{\psi}$ are known to some order, these can be substituted into {eq}`eq-pertth-16` to determine $Q\ket{\psi}$.

(sec-pertth-7)=

## Nearly Degenerate Perturbation Theory

Now let us consider the case in which the unperturbed levels of $H_0$, while not technically degenerate, are close to one another. This often happens in practice, because levels are often grouped into multiplets of closely spaced levels, which are more widely separated from other multiplets. Suppose to be specific that two levels, say, $\epsilon_n$ and $\epsilon_m$, are close enough to one another that first order perturbations will push the exact level $E$ close to or onto the unperturbed level $\epsilon_m$. Then the denominators in the $k=m$ terms in {eq}`eq-pertth-8` are small, and that equation cannot be used.

In this case we may proceed as follows. Let us choose choose some energy, call it $\bar\epsilon$, which is close to $\epsilon_n$ and $\epsilon_m$. It could, for example, be one of the energies $\epsilon_n$ or $\epsilon_m$ themselves, or it could be their average, etc. Then let us take the original unperturbed Hamiltonian and perturbation and rearrange them in the form,

:::{math}
:label: eq-pertth-29
H=H_0+ H_1 = H'_0 + H'_1,
:::

where

:::{math}
:label: eq-pertth-30
\begin{aligned}
H_0 &= \sum_{k\alpha} \epsilon_k \, \ketbra{k\alpha}{k\alpha},
\end{aligned}
:::

:::{math}
:label: eq-pertth-31
\begin{aligned}
H'_0 &= \sum_{\substack{k\ne n,m \\ \alpha}} \epsilon_k \, \ketbra{k\alpha}{k\alpha} + \sum_{\substack{k = n,m \\ \alpha}} \bar\epsilon \, \ketbra{k\alpha}{k\alpha},  \\  H'_1 &= H_1 + \sum_{\substack{k=n,m \\ \alpha}} (\epsilon_k - \bar\epsilon) \ketbra{k\alpha}{k\alpha}.
\end{aligned}

:::

In effect, we have merged the nearly degenerate levels $\epsilon_n$, $\epsilon_m$ into a single degenerate level $\bar\epsilon$, and thrown the correction terms into $H'_1$. Then standard degenerate perturbation theory may be applied. We will call this procedure “nearly degenerate perturbation theory.”

An equivalent approach to nearly degenerate perturbation theory is to exclude both sets of terms $k=n$ and $k=m$ from the definition of $R$, and to proceed from there. Then $R$ becomes the inverse of $E-H_0$ on the space orthogonal to $\HS_n \oplus \HS_m$.

\problems

(prob-pertth-1)=

**Problem \prbdpertth-1..** 

\problempart{(a)} Compute the shifts in the energy levels of a single-electron (hydrogen-like) atom of nuclear charge $Z$ due to the finite size of the nucleus. Treat the nucleus as a uniform sphere of charge of radius $r_0A^{1/3}$, where $r_0 = 1.3\times 10^{-13}$ cm and $A$ is the number of nucleons. Express your answer as some number of eV times some function of $Z$, $A$, and the quantum numbers of the atomic state. Only treat those atomic states for which the effect is the largest. This is called the *volume effect*. You may use

:::{math}
:label: eq-pertth-33
R_{n0}(0) = 2\Bigl( {Z\over na_0}\Bigr)^{3/2},
:::

valid in hydrogen-like atoms, where $a_0=\hbar^2/me^2$ is the Bohr radius.

The volume effect induces a splitting between the $2s$ and $2p$ levels of hydrogen. Compare this to the Lamb shift (another splitting of the same two levels). The Lamb shift raises the $2s$ level relative to the $2p$ level by approximately 1.05 GHz in frequency units.

\problempart{(b)} A muonic atom is one in which the electron has been replaced by a negative muon $\mu^-$, a particle with a charge $q=-e$ and a mass of 105~$MeV/c^2$. Compute $\Delta E/E$ for the volume effect via first order perturbation theory for the $1s$ level of muonic uranium (${}^{238}U$). Is this calculation reliable?

(prob-pertth-2)=

**Problem \prbdpertth-2..** 

:::{math}
:label: eq-pertth-34
H= {1\over 2} \Bigl( {L_1^2\over I_1} + {L_2^2\over I_2} + {L_3^2\over I_3} \Bigr),
:::

where $(I_1,I_2,I_3)$ are the principal moments of inertia and where $(L_1,L_2,L_3) = (L_x,L_y,L_z)$ are angular momentum operators satisfying the commutation relations,

:::{math}
:label: eq-pertth-35
[L_i,L_j] = i\, \epsilon_{ijk} \, L_k.
:::

You may assume that the angular momentum takes on only integer values. The Hamiltonian {eq}`eq-pertth-34` describes the rotational spectrum of molecules. Physically, the quantities $L_i$ are the negatives of the components of the angular momentum with respect to the body frame.

In the case of a *spherical top*, such as methane ($CH_4$), we have $I_1=I_2=I_3=I$. The Hamiltonian is

:::{math}
:label: eq-pertth-36
H={L^2 \over 2I},
:::

and the energy levels are

:::{math}
:label: eq-pertth-37
E_\ell= {\ell(\ell+1)\over 2I},
:::

which is $(2\ell+1)$-fold degenerate since $E_\ell$ is independent of $m$.

In the case of a *symmetric top* such as ammonia($NH_3$), we have $I_1=I_2=I_\perp \ne I_3$. The Hamiltonian is

:::{math}
:label: eq-pertth-38
H={L^2 - L_3^2 \over 2I_\perp} +{L_3^2 \over 2I_3},
:::

and the energy levels are

:::{math}
:label: eq-pertth-39
E_{\ell m} = A + Bm^2,
:::

where

:::{math}
:label: eq-pertth-40
A = {\ell(\ell+1)\over 2 I_\perp}, \qquad B={1\over 2}\Bigl({1\over I_3} - {1\over I_\perp}\Bigr),
:::

and where $m$ is the usual quantum number of $L_z$.

Now consider the case of a slightly *asymmetric top*. (Water is an example of an asymmetric top molecule.) Let

:::{math}
:label: eq-pertth-41
{1\over I_1} = {1+ \epsilon \over I_\perp}, \qquad {1\over I_2} = {1-\epsilon \over I_\perp},
:::

where $\epsilon$ is small. These equations are equivalent to defining

:::{math}
:label: eq-pertth-42
I_\perp = {2I_1 I_2 \over I_1 + I_2}, \qquad \epsilon = {I_2 - I_1 \over I_1+I_2}.
:::

Write the Hamiltonian as $H=H_0+\epsilon H_1$, where $H_0$ is the symmetric top Hamiltonian in {eq}`eq-pertth-38`.

You may find the following relations useful:

:::{math}
:label: eq-pertth-43a
\begin{aligned}
\matrixelement{m}{L_+^2}{m'} &= \matrixelement{m'}{L_-^2}{m}^\cc,
\end{aligned}
:::

:::{math}
:label: eq-pertth-43b
\begin{aligned}
\matrixelement{m}{L_+^2}{m'} &= (-1)^{m+m'} \matrixelement{-m'}{L_+^2}{-m},
\end{aligned}
:::

but if you use {eq}`eq-pertth-43b` you must prove it.

\problempart{(a)} Consider the state $m=0$. Find the first order of perturbation theory at which the energy shift does not vanish, and compute the energy shift at that order. In addition to the abbreviations {eq}`eq-pertth-40`, use

:::{math}
:label: eq-pertth-44
C={1\over 4I_\perp},
:::

and express your answer in terms of the constants $A$, $B$ and $C$.

\problempart{(b)} Find the first order of perturbation theory at which the energy shifts for the $m=\pm1$ levels do not vanish, and compute them at that order.

\problempart{(c)} Find the first order of perturbation theory at which the energy shifts for the $m=\pm2$ levels do not vanish, and compute them at that order. Express your answer in terms of

:::{math}
:label: eq-pertth-45
X={\ell(\ell-1)(\ell+1)(\ell+2) \over 4B}, \qquad Y = {(\ell-3)(\ell-2)(\ell+3)(\ell+4) \over 12B}.
:::

Notice the appearance of a sum over “intermediate states.”

\problempart{(d)} What order of perturbation theory do you have to go to in order to find the first nonvanishing correction to the energy in the case of $m=\pm3$? $m=\pm4$?
