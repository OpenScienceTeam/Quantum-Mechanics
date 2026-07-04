---
title: "06. Topics in One-Dimensional Wave Mechanics"
---
(ch-topicsoned)=

# 06. Topics in One-Dimensional Wave Mechanics

(sec-topicsoned-1)=

## Introduction

In these notes we consider some topics that arise when solving the time-independent Schr\"odinger equation for potential motion in one dimension. I have borrowed most of this material from the lecture notes of Professor Eugene Commins. The Schr\"odinger equation is

:::{math}
:label: eq-topicsoned-1
-{\hbar^2\over 2m} {d^2\psi \over dx^2} +V(x)\psi(x) = E\psi(x).
:::

(sec-topicsoned-2)=

## Degeneracies in One Dimension

Let $\psi(x)$ and $\phi(x)$ be two solutions of {eq}`eq-topicsoned-1` corresponding to the same energy $E$, so that

:::{math}
:label: eq-topicsoned-2
\begin{aligned}
-{\hbar^2\over 2m} \psi'' + V(x)\psi &= E\psi, \\
-{\hbar^2\over 2m} \phi'' + V(x)\phi &= E\phi. \\

\end{aligned}
:::

We multiply the first equation by $\phi$ and the second by $\psi$ and subtract, to get

:::{math}
:label: eq-topicsoned-3
\phi\psi'' - \psi\phi'' = 0 = \dod{W}{x},
:::

where $W$ is the *Wronskian* of the two solutions,

:::{math}
:label: eq-topicsoned-4
\begin{aligned}
W = \phi\psi' - \psi\phi' =\left|\begin{matrix}\phi & \psi \\ \phi' & \psi' \\\end{matrix} \right|.
\end{aligned}

:::

Thus, $W$ is a constant (independent of $x$).

Now suppose (usually due to boundary conditions) that both $\psi$ and $\phi$ vanish at some point $x$. We include the possibilities $x\to+\infty$, $x\to-\infty$, or both. Then $W=0$ everywhere, so

:::{math}
:label: eq-topicsoned-5
{\psi'\over\psi} = {\phi'\over\phi},
:::

which implies

:::{math}
:label: eq-topicsoned-6
\psi(x) = c\phi(x),
:::

where $c$ is a constant.

We see that if both $\psi$ and $\phi$ vanish anywhere on the $x$-axis, including $\pm\infty$, then they are proportional to one another. There is no degeneracy.

Bound state eigenfunctions die off exponentially outside the classically allowed region, so these go to zero at both infinities and must be nondegenerate. In a potential such as that sketched in Fig.~\figr\hilbert.4, the positive energy eigenstates are not bound, but they do die off exponentially at one of the infinities, and so are nondegenerate. In the case of a potential $V(x)$ that approaches zero at both infinities, positive energy eigenfunctions do not approach zero at either infinity, so the theorem just proved does not forbid degeneracies. In fact, such eigenfunctions are two-fold degenerate, as can be seen from the case of the free particle, where $e^{\pm ikx}$ are both eigenfunctions of energy $E=\hbar^2k^2/2m$.

(sec-topicsoned-3)=

## The Reality of Energy Eigenfunctions

Since the Schr\"odinger equation {eq}`eq-topicsoned-1` is real, if $\psi$ is a solution of energy $E$, then so is $\psi^\cc$. But if the energy $E$ is nondegenerate, then $\psi$ and $\psi^\cc$ must be proportional,

:::{math}
:label: eq-topicsoned-7
\psi = c\psi^\cc,
:::

for some constant $c$. By squaring both sides we have

:::{math}
:label: eq-topicsoned-8
|\psi|^2 = |c|^2 |\psi|^2,
:::

which shows that $c$ must be a phase factor, $c=e^{i\alpha}$. Therefore

:::{math}
:label: eq-topicsoned-9
\psi=e^{i\alpha}\psi^\cc.
:::

Now defining

:::{math}
:label: eq-topicsoned-10
\phi(x) = e^{-i\alpha/2}\psi(x) = e^{i\alpha/2}\psi(x)^\cc = \phi(x)^\cc,
:::

we see that $\phi(x)$ is real. We conclude that any nondegenerate energy eigenfunction in one dimension is proportional to a real eigenfunction. In other words, by a phase convention, the nondegenerate eigenfunctions can be chosen to be real.

In the case of degenerate eigenfunctions, it can be shown that one can always choose linear combinations that are real. For example, in the case of the free particle we have degenerate, complex eigenfunctions $e^{\pm ikx}$. But by forming linear combinations, we can create the real eigenfunctions $\sin kx$ and $\cos kx$.

These results are a special case of time-reversal invariance, which is studied in a more general and systematic way later in the course. See {ref}`ch-timerev`.

(sec-topicsoned-4)=

## Interleaving of the Nodes

The zeros of an energy eigenfunction $\psi(x)$ are called its *nodes*. Suppose the potential $V(x)$ supports some bound states, with energies $E_0 < E_1 < E_2 \ldots$. We know these energies must be nondegenerate. Then it can be shown that the $n$-th excited bound state with energy $E_n$ has precisely $n$ nodes. Moreover, the nodes interleave one another, that is, the nodes of $\psi_n(x)$ lie between the nodes of $\psi_{n+1}(x)$. This can be seen in some examples such as the harmonic oscillator. See Figs.~{ref}`fig-topicsoned-1` and {ref}`fig-topicsoned-2`. The proof of these facts may be found in Morse and Feshbach.

:::{figure} images/topicsoned-fig01.png
:label: fig-topicsoned-1
:width: 80%

Eigenfunction $\psi_n(x)$ has $n$ nodes. Harmonic oscillator eigenfunctions are illustrated for $n=0,1,2$.
:::

:::{figure} images/topicsoned-fig02.png
:label: fig-topicsoned-2
:width: 80%

The nodes of successive eigenfunctions interleave, here illustrated for $n=5,6$. The small dots are the nodes for $n=5$, the large ones for $n=6$.
:::


Here is an application. Consider the double well oscillator, whose potential is sketched in {ref}`fig-topicsoned-3`. If the barrier in the middle is high, then tunnelling is small and the ground state wave functions in the left and right wells do not communicate with each other very much. Thus, both $\psi_\ell(x)$ and $\psi_r(x)$ are nearly ground states for the whole potential, and there is a near degeneracy.

:::{figure} images/topicsoned-fig03.png
:label: fig-topicsoned-3
:width: 80%

A double well potential (heavy line). Also shown are the approximate ground state wave functions in the left and right wells.
:::

As shown in \secrtopicsoned-2, however, there cannot be an exact degeneracy. Now since the Hamiltonian commutes with parity, by Theorem {ref}`thm-hilbert-5` the eigenstates of $H$, which are nondegenerate, must also be eigenstates of parity. Since $\psi_\ell$ and $\psi_r$ are not eigenstates of parity, to get the energy eigenstates we must form symmetric and antisymmetric linear combinations,

:::{math}
:label: eq-topicsoned-11
\psi_{\pm} = {1\over\sqrt{2}}(\psi_r \pm \psi_\ell),
:::

which are illustrated in Figs.~{ref}`fig-topicsoned-4` and {ref}`fig-topicsoned-5`. These are eigenstates of parity.

:::{figure} images/topicsoned-fig04.png
:label: fig-topicsoned-4
:width: 80%

Even eigenfunction in double well potential.
:::

:::{figure} images/topicsoned-fig05.png
:label: fig-topicsoned-5
:width: 80%

Odd eigenfunction in double well potential.
:::


But which one of them is the ground state, and which the excited state? According to the rules we have presented, the symmetric state in {ref}`fig-topicsoned-4` has no node, and must be the ground state, while the antisymmetric state in {ref}`fig-topicsoned-5` has one node and must be the first excited state.

\problems

(prob-topicsoned-1)=

**Problem \prbdtopicsoned-1..** 

:::{math}
:label: eq-topicsoned-12
V(x) = -a\delta(x)
:::

can be seen as the limit of a square well potential,

:::{math}
:label: eq-topicsoned-13
\begin{aligned}
V(x) = -a \times \begin{cases} 1/L, & |x|\le L/2, \\  0,  & |x|>L/2, \\\end{cases}
\end{aligned}

:::

as $L\to0$. The parameter $a$ has dimensions of energy times distance. The potential shown is a $\delta$-function well potential (for $a>0$), but by changing the sign of $a$ we get a $\delta$-function barrier.

Show that the $\delta$-function well supports precisely one bound state. Find the energy and the wave function.

**Hint:** This can be done by taking the limit of a square well solution, but the following is an easier method.

Normally we require the wave function and its first derivative to be continuous in $x$ in a one-dimensional solution of the Schr\"odinger equation. If the first derivative had a discontinuity, it would mean that the second derivative, which appears in the kinetic energy term, would have a $\delta$-function at the location of the discontinuity of the first derivative. That $\delta$-function can only be balanced out in the Schr\"odinger equation if the potential has a $\delta$-function. However, in the present situation, that is precisely what we have.

So solve the Schr\"odinger equation in the region $x<0$ and $x>0$, where $V=0$, and then find the discontinuity in $\psi'$ across $x=0$ by integrating over a small interval $[-\epsilon,\epsilon]$.
