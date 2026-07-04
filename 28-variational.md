---
title: "28. The Variational Method"
---
(ch-variational)=

# 28. The Variational Method

(sec-variational-1)=

## Introduction

Very few realistic problems in quantum mechanics are exactly solvable, so approximation methods are a virtual necessity for understanding the physics of real systems. In {ref}`ch-pertth`\ we considered bound state perturbation theory, which allows us to find the discrete energy eigenvalues and eigenstates of a system that is close to a solvable system. But what do we do when there is no exactly solvable system close to a given system, as often happens in practice? One answer is the variational method, which we discuss in these notes.

The variational method is particularly useful for finding approximations to the ground state energy and eigenfunction of a system. It is harder to use for excited states, with some exceptions that we will mention in this set of notes. Nevertheless, the variational method is a vital one in the repertoire of techniques useful in quantum mechanics.

(sec-variational-2)=

## A Theorem on Variational Estimates to the Ground State Energy

The variational method is based on a certain theorem regarding variational estimates to the ground state energy. As we state and prove the theorem, we will make some remarks indicating how it is used in practice.

Let $H$ be a Hamiltonian which is assumed to have some bound states. Let the discrete (bound state) energy eigenvalues be ordered $E_0<E_1<E_2\ldots$. The eigenvalues are allowed to be degenerate. There may also be a continuous spectrum above some energy, as often happens in practice.

Let $\ket{\psi}$ be any normalizable state. We do not assume it is normalized because unnormalized states are convenient in practice. Then the theorem states that

:::{math}
:label: eq-variational-1
{\matrixelement{\psi}{H}{\psi} \over \braket{\psi}{\psi}} \ge E_0.
:::

That is, the expectation value of energy with respect to the state $\ket{\psi}$ is an upper bound to the ground state energy.

The theorem does not tell us how far above the ground state energy the left hand side of the inequality {eq}`eq-variational-1` is, so it would not seem to be of much help in estimating the ground state energy. It would be better if we also had a lower bound, so $E_0$ would be bracketed between two numbers. There are methods for finding lower bounds to energy levels, but they require some extra information and extra work. See Ballentine, *Quantum Mechanics*, for more details. In practice the state $\ket{\psi}$ is chosen to be an approximation to the ground state, based on physical intuition or other criteria, and the upper bound on $E_0$ that is obtained is often quite useful.

To prove the theorem let $\ket{\phi}$ be a normalized version of the state $\ket{\psi}$,

:::{math}
:label: eq-variational-2
\ket{\phi} = {\ket{\psi} \over \sqrt{\braket{\psi}{\psi}}},
:::

so that

:::{math}
:label: eq-variational-3
\braket{\phi}{\phi} =1
:::

and

:::{math}
:label: eq-variational-4
{\matrixelement{\psi}{H}{\psi} \over \braket{\psi}{\psi}} = \matrixelement{\phi}{H}{\phi}.
:::

Now let us decompose $\ket{\phi}$ into a component lying in the ground state eigenspace and a component orthogonal to this eigenspace. We write the decomposition as

:::{math}
:label: eq-variational-5
\ket{\phi} = a\ket{0} + \ket{\epsilon},
:::

where $\ket{0}$ is a normalized state lying in the ground eigenspace,

:::{math}
:label: eq-variational-6
\braket{0}{0}=1, \qquad H\ket{0} = E_0\ket{0},
:::

where $a$ is a complex number, and where $\ket{\epsilon}$ is the component orthogonal to the ground state eigenspace, so that

:::{math}
:label: eq-variational-7
\braket{0}{\epsilon}=0.
:::

If the ground state is nondegenerate, then $\ket{0}$ can be taken to be the normalized ground state itself. Then by squaring {eq}`eq-variational-5` and using {eq}`eq-variational-7`, we have

:::{math}
:label: eq-variational-8
\braket{\phi}{\phi} = 1 = |a|^2 + \braket{\epsilon}{\epsilon},
:::

since the cross terms vanish.

Now {eq}`eq-variational-4` becomes

:::{math}
:label: eq-variational-9
\matrixelement{\phi}{H}{\phi} = |a|^2 E_0 + \matrixelement{\epsilon}{H}{\epsilon},
:::

where again the cross terms cancel. We add and subtract $E_0$ from $H$ in the second term, using {eq}`eq-variational-8`, to obtain

:::{math}
:label: eq-variational-10
\matrixelement{\phi}{H}{\phi} = E_0 + \matrixelement {\epsilon}{H-E_0}{\epsilon}.
:::

The operator $H-E_0$ is a nonnegative definite operator (see {eq}`eq-hilbert-65`, so the second term is $\ge 0$. This is because the eigenvalues of $H-E_0$ are just those of $H$, shifted downward by $E_0$, that is, they are $(0,E_1-E_0, E_2-E_0, \ldots)$, which are all nonnegative. This proves {eq}`eq-variational-1`.

Notice that if the wave function $\ket{\psi}$ is a good approximation to the ground state wave function, so that $\ket{\epsilon}$ is small, then the error in the energy (the second term in {eq}`eq-variational-10` is of second order in $\ket{\epsilon}$. Thus, rather crude approximations to the ground state wave function often give rather good estimates of the ground state energy.

(sec-variational-3)=

## Families of Trial Wave Functions

If we compute the expectation value of the energy with respect to a family of wave functions then all the answers are upper bounds to the true ground state energy, and the lowest one must be the closest. This leads to a criterion for the best estimate for the ground state wave function: it is the one that minimizes the energy. We call the members of the family “trial wave functions.”

In practice we often choose a continuous family of trial wave functions. Let $\lambda$ be a continuous parameter, and let us write the family as $\ket{\psi(\lambda)}$. Then we define a function of $\lambda$, really an energy function,

:::{math}
:label: eq-variational-11
F(\lambda) = {\matrixelement{\psi(\lambda)}{H} {\psi(\lambda)} \over \braket{\psi(\lambda)}{\psi(\lambda)}}.
:::

We minimize this by finding the root $\lambda_0$ of

:::{math}
:label: eq-variational-12
\frac{\partial F}{\partial \lambda}=0,
:::

so that the best estimate to the ground state wave function out of the family is $\ket{\psi(\lambda_0)}$ and the best estimate for the ground state energy is $F(\lambda_0)$. Of course we must check that the root of {eq}`eq-variational-12` is actually a minimum. This procedure is easily generalized to the case of multiple parameters, $\lambda=(\lambda_1,\ldots,\lambda_n)$, for which we find the roots of $\partial F/\partial\lambda_i=0$ (the critical points of the function $F$).

We note that a critical point of the function $F$ is not necessarily a minimum. It could be a maximum, a saddle point, or something more complicated. The choices are partially classified by the second derivative matrix, $\partial^2 F/\partial \lambda_i\partial\lambda_j$, evaluated at the critical point. If this matrix has all positive eigenvalues, then the critical point is a minimum; if it has all negative eigenvalues, then the critical point is a maximum; if some eigenvalues are positive and some negative, then the critical point is a saddle; and if some eigenvalues vanish, then the second derivative matrix alone is not sufficient to classify the critical point.

(sec-variational-4)=

## A One-Dimensional Example

As an example suppose we wish to find the ground state energy and wave function of a particle in one dimension moving in the well $V(x)=|x|$. We take $m=1$, so the Hamiltonian is

:::{math}
:label: eq-variational-13
H={p^2\over 2} + |x|.
:::

This problem can be solved exactly in terms of Airy functions, which shows that the ground state energy is $E_0 = -y_1/2^{1/3}$, where $y_1$ is the first negative root (moving away from zero) of $\Ai'(y)=0$. This gives $E_0=0.808$, approximately.

As a crude trial wave function let us use the Gaussian,

:::{math}
:label: eq-variational-14
\psi(a,x)= e^{-ax^2},
:::

where $a$ is the variational parameter. Actually we know that Gaussians are the exact ground state wave functions of harmonic oscillators, not the potential in {eq}`eq-variational-13`. But at least the trial wave function and the exact ground state wave function have no nodes (see {ref}`sec-topicsoned-4`), so they have that in common.

The calculation is straightforward. The normalization integral is

:::{math}
:label: eq-variational-15
\braket{\psi}{\psi} = \int_{-\infty}^{+\infty} dx\, e^{-2ax^2} = \sqrt{\ds {\ds \pi\over \ds 2a}},
:::

the integral for the kinetic energy is

:::{math}
:label: eq-variational-16
\matrixelement{\psi}{{p^2\over 2}}{\psi} = {1\over 2}\sqrt{\ds{\ds\pi a\over \ds 2}},
:::

and that for the potential energy is

:::{math}
:label: eq-variational-17
\matrixelement{\psi}{V}{\psi} = 2\int_0^\infty x\,dx\, e^{-2ax^2} = {1\over 2a}.
:::

Altogether, the function we wish to minimize is

:::{math}
:label: eq-variational-18
F(a) = {a\over 2} + {1\over\sqrt{2\pi a}}.
:::

We differentiate, finding

:::{math}
:label: eq-variational-19
F'(a) = {1\over 2} - {1 \over 2\sqrt{2\pi a^3}},
:::

which has the root

:::{math}
:label: eq-variational-20
a_0 = {1\over (2\pi)^{1/3}}.
:::

This gives the estimate for the ground state energy,

:::{math}
:label: eq-variational-21
F(a_0) = {3\over 2}{ 1\over (2\pi)^{1/3}} = 0.813.
:::

This compares favorably with (and is an upper bound to) the exact ground state energy of $E_0=0.808$. Notice how good the estimate of the energy is, in spite of the crudeness of the trial wave function.

(sec-variational-5)=

## Lagrange Multipliers for Normalization

In practice the normalization denominators in {eq}`eq-variational-11` are often inconvenient. One possibility is simply to normalize each member of the set of trial wave functions so those denominators are not present. But often it is easier to enforce normalization by using Lagrange multipliers. This means that out of some family of trial wave functions $\ket{\psi(\lambda)}$, of which only a subset is normalized, we minimize the expectation value of the Hamiltonian with respect to the normalized subset.

To use the Lagrange multiplier method, we introduce the function,

:::{math}
:label: eq-variational-22
F(\lambda,\beta) = \matrixelement{\psi(\lambda)}{H} {\psi(\lambda)} - \beta \bigl( \braket{\psi(\lambda)}{\psi(\lambda)} -1\bigr),
:::

and then require

:::{math}
:label: eq-variational-23
\frac{\partial F}{\partial \lambda}=0 \qquad and \qquad \frac{\partial F}{\partial \beta}=0.
:::

The Lagrange multiplier $\beta$ is in effect another variational parameter. The second equation implies normalization.

As an example of the Lagrange multiplier method, let $\{\ket{n}, n=0,1,\ldots\}$ be any orthonormal basis (not usually the eigenbasis of $H$, since we don't know what that is). For example, $H$ might be a one-dimensional oscillator in a potential we cannot handle easily, and $\{\ket{n}\}$ might be the eigenbasis of the harmonic oscillator. Then the unknown ground state $\ket{\psi}$ can be expanded in the orthonormal basis,

:::{math}
:label: eq-variational-24
\ket{\psi} = \sum_{n=0}^\infty c_n \ket{n}.
:::

There is no approximation in this, but we do not know what the coefficients $c_n$ are.

But in practice, for example, on computers, we can only handle a finite basis, so we write

:::{math}
:label: eq-variational-25
\ket{\psi} = \sum_{n=0}^{N-1} c_n \ket{n},
:::

where $N$ is finite, and we regard the coefficients $c_n$, not as the exact expansion coefficients in the given basis, but rather as parameters of a trial wave function. Then the function $F$ of {eq}`eq-variational-22` becomes

:::{math}
:label: eq-variational-26
F(\{c_n\},\beta) = \sum_{m,n=0}^{N-1} c_n^\cc \matrixelement{n}{H}{m} c_m -\beta\Bigl( \sum_{n=0}^{N-1} |c_n|^2 -1\Bigr).
:::

The coefficients $c_n$ are complex, so we want to vary with respect to their real and imaginary parts. An equivalent procedure is to vary with respect to $c_n$ and $c_n^\cc$, treated as independent complex variables. This gives

:::{math}
:label: eq-variational-27a
\begin{aligned}
\frac{\partial F}{\partial c_n^\cc} &= \sum_{m=0}^{N-1} \matrixelement{n}{H}{m} c_m - \beta c_n = 0,
\end{aligned}
:::

:::{math}
:label: eq-variational-27b
\begin{aligned}
\frac{\partial F}{\partial c_n} &= \sum_{m=0}^{N-1} c_m^\cc \matrixelement{m}{H}{n} - \beta c_n^\cc =0,
\end{aligned}
:::

:::{math}
:label: eq-variational-27c
\begin{aligned}
\frac{\partial F}{\partial \beta} &=  \sum_{n=0}^{N-1} |c_n|^2 -1 = 0.
\end{aligned}
:::

The second equation is the complex conjugate of the first equation and gives no additional information. The first equation shows that the Lagrange multiplier $\beta$ is the eigenvalue of the truncated, $N\times N$ matrix of matrix elements of $H$ with respect to the given basis, while the coefficients $c_n$ are the eigenvectors of this matrix. The third equation shows that the eigenvectors are normalized. Let us denote the eigenvalues of this matrix by $\beta_n$, ordered so that $\beta_0\le\beta_1\le\ldots\le\beta_{N-1}$. We see that the eigenvalues of truncated matrix and the corresponding, normalized eigenvectors are critical points of the energy function {eq}`eq-variational-26`. The minimum eigenvalue $\beta_0$ and corresponding eigenvector are a true minimum of the functional.

When finding the energy eigenvalues of a Hamiltonian on a computer it is natural to truncate an infinite basis set to some finite size and to diagonalize that matrix, because there is little choice. It is also natural to hope that the eigenvalues of the truncated matrix will be good approximations to the exact eigenvalues of the Hamiltonian, and to hope that they will converge to those exact eigenvalues as $N\to\infty$. What the theorem proved in \secrvariational-2 adds to this is the fact that the minimum eigenvalue of the truncated matrix, $\beta_0$, is actually an upper bound to the true ground state energy, $\beta_0 \ge E_0$. Moreover, if we increase the size of the truncation, this minimum eigenvalue can only decrease, thereby coming closer to the true eigenvalue. This is because when we increase $N$ we are considering a larger family of trial wave functions that includes all the trial wave functions at a lower level of truncation. The minimum energy of the larger set must be less than or equal to the minimum energy of the smaller set contained in it.

The variational parameters $c_n$ in the example {eq}`eq-variational-25` can be regarded as *linear* parameters, that is, coefficients in a linear combination of wave functions, while the parameter $a$ in the example {eq}`eq-variational-14` can be regarded as a *nonlinear* parameter, because the trial wave function depends nonlinearly on it. The parameters of trial wave functions can be of either kind, and in general the set of trial wave functions is not a vector subspace of the Hilbert space but rather some other type of subset.

(sec-variational-6)=

## The Hylleraas-Undheim Theorem

In the case of purely linear parameters, as in the trial wavefunction {eq}`eq-variational-25`, a theorem proved by Hylleraas and Undheim goes considerably beyond the simple theorem proved in \secrvariational-2. In the following it is convenient to reinterpret the notation $E_n$, by indicating degeneracies by repetitions of the values $E_n$ for successive $n$. For example, if the ground state were 2-fold degenerate and the first excited state nondegenerate, then we would have $E_0=E_1<E_2<E_3$, etc. Then it turns out that not only is $\beta_0$ an upper bound to $E_0$, but in fact $\beta_n \ge E_n$ for all $n=0,\ldots,N-1$. That is, all the eigenvalues of the truncated matrix are upper bounds to the corresponding exact eigenvalues.

Moreover, if we consider two different truncations of the exact expansion {eq}`eq-variational-24`, one with the first $M$ basis states and the second with the first $N$ basis states, with $M<N$, then it can be shown that

:::{math}
:label: eq-variational-28
\beta^{(N)}_m \le \beta^{(M)}_m \le \beta^{(N)}_{N-M+m},
:::

for $m=1,\ldots,M$, where the dimension of the matrix is indicated in parentheses. In particular, if $N=M+1$, then

:::{math}
:label: eq-variational-29
\beta^{(M+1)}_m \le \beta^{(M)}_m \le \beta^{(M+1)}_{m+1},
:::

for $m=1,\ldots,M$. In other words, the eigenvalues of the truncated matrix of size $M$ and that of size $M+1$ interleave each other.

In {eq}`eq-variational-24` we imagined that the Hilbert space was infinite-dimensional, as it often is in practice. But if it has dimension $N$ where $N$ is finite, then the first $N$ basis states $\ket{n}$ span the whole space, and the eigenvalues of the $N\times N$ matrix of the Hamiltonian are the exact eigenvalues. In that case, {eq}`eq-variational-28` becomes (for a truncation $M<N$),

:::{math}
:label: eq-variational-30
E_m \le \beta^{(M)}_m \le E_{N-M+m},
:::

for $m=1,\ldots,M$, and we get not only upper bounds but also lower bounds on some of the exact energies (but still only an upper bound for the ground state energy).

(sec-variational-7)=

## Variational Estimates for the Excited States

If the family of trial wave function contains any nonlinear parameters, then in general we obtain only an upper bound to the ground state energy, and no bounds at all, either upper or lower, on the excited state energies. Nevertheless, there are circumstances when we can obtain rigorous upper bounds on some excited state energies, even with nonlinear variational parameters. Suppose for example that the ground state $\ket{0}$ (assumed nondegenerate, for simplicity) were exactly known. Then by choosing trial wave functions $\ket{\psi}$ that are orthogonal to the exact ground state, $\braket{0}{\psi}=0$, we would obtain an upper bound to the first excited state energy $E_1$. This is easily proved by same methods used to prove {eq}`eq-variational-1`. Unfortunately, if we are using the variational method, we probably do not know what the ground state wave function is. Of course we can find an estimate to it by using the variational method, but making our trial wave functions orthogonal to an estimate of the ground state is not good enough to give us a bound on the excited states. So this idea is not very useful in practice.

Sometimes however it is possible to find trial wave functions that are orthogonal to the exact ground state, without knowing what that ground state is. Suppose for example we have a one-dimensional potential that is invariant under parity, $V(x)=V(-x)$. Then we know that the ground state is even under parity and the first excited state is odd. By choosing a family of trial wave functions that are odd under parity, they are guaranteed to be orthogonal to the ground state, and the variational method with this set will give an upper bound to the first excited state energy $E_1$.

More generally in any system with an exact symmetry the variational method can be used to obtain an upper bound to the minimum energy level in each symmetry class, for example, in each set of wave functions with a given value $j$, in a system with rotational invariance (where $j$ is the quantum number of the total angular momentum of the system).

\problems

(prob-variational-1)=

**Problem \prbdvariational-1..** 

Consider a 1-dimensional problem, with Hamiltonian

:::{math}
:label: eq-variational-31
H={p^2\over 2m} + V(x),
:::

where $-\infty < x < +\infty$. Assume that $V(x)$ vanishes for $|x|>R$. For $|x| < R$, the potential is allowed to do almost anything (it may be positive in some places, and negative in others). Write down an expression for the expectation value of the energy for the Gaussian wave function,

:::{math}
:label: eq-variational-32
\psi(x)={1\over \sqrt{a\sqrt{\pi}}} \exp\Bigl(-{x^2\over 2a^2}\Bigr),
:::

and evaluate the integrals you can evaluate. Use the result to show that a bound state exists if the potential satisfies

:::{math}
:label: eq-variational-33
\int V(x)\,dx < 0.
:::

We may call such a potential “overall attractive.”

Now try the same trick in 3 dimensions and show that it does not work. Assume $V(\xvec)=0$ for $r>R$, and use the wave function

:::{math}
:label: eq-variational-34
\psi(\xvec)={1\over\bigl( a\sqrt{\pi} \bigr)^{3/2} } \exp \Bigl( - {r^2\over 2a^2} \Bigr).
:::

(prob-variational-2)=

**Problem \prbdvariational-2..** 

(prob-variational-3)=

**Problem \prbdvariational-3.} Consider a system with a nondegenerate ground state.  According to nondegenerate perturbation theory (see {eq}`eq-pertth-23`, the second order correction to the ground state energy is always $\le0$.  Does this imply that the first order estimate to the energy, $\epsilon_0+\matrixelement{0}{H_1}{0.** 

\problempart{(a)} Find a proof that the first order estimate to the ground state energy is actually an upper bound to the true ground state energy.

\problempart{(b)} Now allow the ground state to be degenerate. When we turn on the perturbation }$H_1$, the ground state will in general split. Show that the estimate in first order perturbation theory for the lowest of these levels is a rigorous upper bound to the ground state energy.
