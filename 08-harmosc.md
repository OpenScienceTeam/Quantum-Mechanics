---
title: "08. Harmonic Oscillators and Coherent States"
---
(ch-harmosc)=

# 08. Harmonic Oscillators and Coherent States

(sec-harmosc-1)=

## Introduction

Harmonic oscillators are ubiquitous in physics. For example, the small vibrations of most mechanical systems near the bottom of a potential well can be approximated by harmonic oscillators. This includes the case of small vibrations of a molecule about its equilibrium position or small amplitude lattice vibrations in a solid. For another example, the motion of a charged particle in a uniform magnetic field, a problem of considerable interest in solid state physics, can be transformed into a harmonic oscillator (see {ref}`ch-magfield`). Finally, the excitations of a free field, such as the electromagnetic field, are described by harmonic oscillators (see {ref}`ch-classemf`{} and \quantemf). These excitations are usually identified with particles, so that we speak of photons, phonons, etc, depending on the type of field. In many of these cases the harmonic oscillator description is only approximate, and perturbation methods may be used to take into account higher order corrections. For example, in field theory, perturbation methods based on harmonic oscillators are used to take into account the interactions of (non-free) fields, allowing us to describe phenomena such as the emission and absorption of radiation (see {ref}`ch-radnmatt`{} and \photscatt). In these notes we concentrate mainly on mechanical oscillators, but will make a few remarks about applications in quantum optics.

(sec-harmosc-2)=

## Harmonic Oscillators in Mechanical Systems

Consider a mechanical system of $n$ degrees of freedom, in which the particles interact by means of some potential $V(x_1, \ldots, x_n)$. Here $n$ could be very large (for example, in the lattice vibrations of a solid, we would have $n=3N$, where $N$ is the number of atoms). We write the Hamiltonian as

:::{math}
:label: eq-harmosc-1
H=\sum_{i=1}^n {p_i^2 \over 2m_i} + V(x_1, \ldots, x_n).
:::

The masses $m_i$ associated with the various degrees of freedom might be equal for different $i$, for example, if three of the $x_i$ are the $(x,y,z)$ coordinates of a single particle, or if there are identical particles in the system. To be general, however, we allow the $m_i$ to be distinct. We will transform and approximate this Hamiltonian by a series of simple transformations, which will convert it into a sum of one-dimensional harmonic oscillators. In each of these transformations we will denote the new coordinates and momenta with a prime, which we drop after the transformation is carried out.

We begin by making all the mass parameters identical. Let $M$ be a reference mass for the whole system, for example, the average mass of all the particles, or the mass of a hydrogen atom (the reference for the system of atomic weights). Then define dimensionless numbers $\mu_i$ by

:::{math}
:label: eq-harmosc-2
\mu_i = {m_i \over M},
:::

and perform the transformation,

:::{math}
:label: eq-harmosc-3
x'_i = {x_i  \over \sqrt{\mu_i}}, \qquad p'_i = \sqrt{\mu_i}\,p_i.
:::

This is a transformation on the $x$ and $p$ operators of the system, producing new operators which preserve the Heisenberg-Born commutation relations {eq}`eq-spatialdof-69a`. We define a transformed potential energy by

:::{math}
:label: eq-harmosc-4
W(x'_1, \ldots, x'_n) = V(x_1, \ldots, x_n).
:::

Then the transformed Hamiltonian can be written (after dropping the primes),

:::{math}
:label: eq-harmosc-5
H = {1\over 2M} \sum_{i=1}^n  p_i^2 + W(x_1, \ldots, x_n).
:::

A point of configuration space $(x_{10}, \ldots, x_{n0})$ where the force vanishes is one where the first derivatives of $W$ vanish,

:::{math}
:label: eq-harmosc-6
\frac{\partial W}{\partial x_i}(x_{10}, \ldots, x_{n0}) =0.
:::

Such a point is called a *critical point* of the potential. Near $(x_{10}, \ldots, x_{n0})$, the potential may be approximated by its Taylor series expansion through quadratic order,

:::{math}
:label: eq-harmosc-7
W(x_1, \ldots, x_n) \approx W_0 + {1\over 2} \sum_{ij} W''_{ij} \,(x_i-x_{i0})(x_j-x_{j0}),
:::

where $W_0$ is the value of $W$ at the critical point and where

:::{math}
:label: eq-harmosc-8
W''_{ij}= {\partial^2 W \over \partial x_i \partial x_j} (x_{10}, \ldots, x_{n0}).
:::

The critical point $(x_{10}, \ldots, x_{n0})$ is a minimum of the potential if the matrix $W''_{ij}$ is positive definite, since this means that the potential energy increases as we move away from $(x_{10}, \ldots, x_{n0})$ in any direction. This is the only case we will consider. Thus, the eigenvalues of $W''_{ij}$ are all positive.

We substitute the approximation {eq}`eq-harmosc-7` into the Hamiltonian {eq}`eq-harmosc-5`, redefining the origin of energy to absorb the term $W_0$. We can always get rid of a constant term in any Hamiltonian in this way, since only energy differences are physically meaningful. Next we shift the origin of the coordinates by writing $x'_i = x_i - x_{0i}$, placing the minimum of $W$ at the origin, and then drop the primes. Finally, we transform the coordinates and momenta by

:::{math}
:label: eq-harmosc-9
x'_i = \sum_j R_{ij}\, x_j, \qquad p'_i = \sum_j R_{ij}\, p_j,
:::

where $R$ is the orthogonal matrix that diagonalizes $W''$. This is again a transformation of the operators $x$ and $p$ of the system that preserves the canonical commutation relations {eq}`eq-spatialdof-69a`. After dropping the primes, the Hamiltonian becomes

:::{math}
:label: eq-harmosc-10
H=\sum_{i=1}^n \Bigl( {p_i^2 \over 2M} + {M\omega_i^2 x_i^2 \over 2}\Bigr),
:::

where the positive eigenvalues of $W''$ are written as $M\omega_i^2$. The Hamiltonian has been transformed into a sum of $n$ one-dimensional harmonic oscillators.

The frequencies $\omega_i$ defined by these transformations are the frequencies of small vibrations of the normal modes of the system, which are represented by the final coordinates $x_i$. Some of these frequencies may be equal, that is, the matrix $W''$ may have degeneracies. Of course, these degeneracies of the $n \times n$ matrix $W''$ are not to be confused with any possible degeneracies of the quantum Hamiltonian. Degeneracies among the frequencies $\omega_i$ are common in the vibrations of simple molecules, due to identical particles and the symmetry of the equilibrium configurations.

The Hamiltonian {eq}`eq-harmosc-10` is easily solved, both in classical mechanics and in quantum mechanics, because the separate degrees of freedom are decoupled from one another. In quantum mechanics, this means that the Schr\"odinger equation for the Hamiltonian {eq}`eq-harmosc-10` is separable into $n$ Schr\"odinger equations for one-dimensional harmonic oscillators, and that the energy eigenfunctions of the entire system can be written as products of eigenfunctions of one-dimensional harmonic oscillators.

The cubic and higher order terms in the Taylor series of $W$ that were neglected in the derivation of {eq}`eq-harmosc-10` can be transformed to the normal mode coordinates and restored to the Hamiltonian, whereupon they provide a coupling between the various harmonic oscillators. These terms can then be handled by perturbation theory, in which the harmonic oscillators form the unperturbed system. This is only useful, however, when the amplitude of vibrations is not too large, since it may require too many terms of the Taylor series to represent the potential accurately for large amplitude vibrations, or the series may not converge far enough away from the minimum.

(sec-harmosc-3)=

## The One-Dimensional Harmonic Oscillator

Let us write the Hamiltonian for one of the terms in {eq}`eq-harmosc-10` in the form,

:::{math}
:label: eq-harmosc-11
H={p^2 \over 2m} + {m\omega^2 x^2\over 2},
:::

dropping the $i$ subscripts and writing $m$ instead of $M$. The parameters of the Hamiltonian define a characteristic length, time, velocity, momentum, energy, etc., so that it is possible to introduce scaled, dimensionless variables, as follows:

:::{math}
:label: eq-harmosc-12
\bar x = {x \over \sqrt{{\displaystyle \hbar \over \displaystyle m\omega}}}, \quad \bar t = \omega t, \quad \bar v = {v \over \sqrt{{\displaystyle \hbar\omega \over \displaystyle m}}}, \quad \bar p = {p \over \sqrt{m\hbar\omega}}, \quad \bar E = {E\over \hbar \omega}, \quad \bar H = {H \over \hbar \omega},
:::

etc. This procedure is equivalent to choosing units such that $m=\omega=\hbar=1$.

This transformation cleans up the clutter of constants that would otherwise follow us through the following derivations, and makes the essential ideas more clear. To transform back to physical variables, we take any quantity appearing in dimensionless form and multiply it by the characteristic unit of distance, time, energy, etc. In particular, the wave function $\psi(x)$ must have dimensions of $\\textlength^{-1/2}$, so that $|\psi(x)|^2$ will be a probability density. Therefore the relation between the original wave function $\psi(x)$ and the transformed one $\bar\psi(\bar x)$ is

:::{math}
:label: eq-harmosc-13
\psi(x) =\Bigl({m\omega\over \hbar}\Bigr)^{1/4} \bar\psi(\bar x).
:::

After transforming to the dimensionless variables {eq}`eq-harmosc-12`, we drop the overbars. Then the Hamiltonian becomes

:::{math}
:label: eq-harmosc-14
H = {1\over 2}(\hat p^2 + \hat x^2),
:::

and the commutation relations are

:::{math}
:label: eq-harmosc-15
[\hat x,\hat p] = i.
:::

Here and below we put hats on the operators $\hat x$, $\hat p$, to distinguish them from the $c$-numbers $x$, $p$ (eigenvalues or classical quantities). For other operators this distinction will usually not be necessary.

Because the potential goes to infinity as $x\to\pm\infty$, the energy eigenfunctions die off exponentially as $x \to \pm \infty$ and must be normalizable. Thus, the spectrum of $H$ is discrete. Moreover, according to the discussion in {ref}`sec-topicsoned-2`, the eigenfunctions must be nondegenerate.

(sec-harmosc-4)=

## Dirac's Algebraic Method for the Eigenvalues

We now derive the spectrum of $H$ using Dirac's algebraic method. This method is based on the observation that the Hamiltonian of the classical harmonic oscillator is a quadratic function of $x$ and $p$ that can be factored into linear factors,

:::{math}
:label: eq-harmosc-16
{1\over 2}(x^2 + p^2) = \Bigl( {x+ip \over \sqrt{2}} \Bigr) \Bigl( {x-ip \over \sqrt{2}} \Bigr).
:::

The factors define complex coordinates in terms of which the classical motion is especially simple. Since the quantum Hamiltonian consists of noncommuting operators, the factorization in the quantum case is slightly more complicated, but the basic definitions follow from {eq}`eq-harmosc-16`.

For the quantum problem we begin by defining non-Hermitian operators $a$ and $a^\dagger$, which are Hermitian conjugates of each other,

:::{math}
:label: eq-harmosc-17
a = {1\over\sqrt{2}} (\hat x+i\hat p), \qquad a^\hc = {1\over\sqrt{2}} (\hat x-i\hat p).
:::

These have the inverses,

:::{math}
:label: eq-harmosc-18
\hat x = {1\over\sqrt{2}}(a + a^\hc), \qquad \hat p = {-i\over\sqrt{2}} (a - a^\hc).
:::

Operators $a$, $a^\hc$ have the commutation relation,

:::{math}
:label: eq-harmosc-19
[a,a^\hc] =1,
:::

which follows from {eq}`eq-harmosc-15`. Operator $a$ is called an “annihilation” or “lowering” operator, and $a^\dagger$ is called a “creation” or “raising” operator. We express the Hamiltonian in terms of these operators, obtaining

:::{math}
:label: eq-harmosc-20
H= a^\dagger a +{1\over 2} = N+{1\over 2},
:::

which is the quantum analog of the classical factorization {eq}`eq-harmosc-16`. The extra $1/2$ in {eq}`eq-harmosc-20` comes from the quantum commutation relation {eq}`eq-harmosc-19`. The operator $N$ is the “number” operator, defined by

:::{math}
:label: eq-harmosc-21
N=a^\hc a.
:::

This operator is nonnegative definite, that is,

:::{math}
:label: eq-harmosc-22
\matrixelement{\phi}{N}{\phi} \ge 0,
:::

for all states $\ket{\phi}$, since the given expectation value is the square of the state $a\ket{\phi}$. See {eq}`eq-hilbert-27`.

We will now derive the spectrum of $N$, from which that of $H$ follows by {eq}`eq-harmosc-20`. Both $H$ and $N$ have the same eigenstates. Let $\ket{\nu}$ be a normalized eigenstate of $N$ with eigenvalue $\nu$,

:::{math}
:label: eq-harmosc-23
N\ket{\nu} = \nu \ket{\nu}.
:::

The notation $\nu$ is used to indicate that as far as we know at this point, the eigenvalue could be any number, positive, negative, integer or fraction (it must be real since $N$ is Hermitian). However, multiplying {eq}`eq-harmosc-23` by the bra $\bra{\nu}$ and using the fact that $N$ is nonnegative definite, we find

:::{math}
:label: eq-harmosc-24
\matrixelement{\nu}{N}{\nu} = \matrixelement{\nu}{a^\dagger a}{\nu} = \nu \ge 0.
:::

The eigenvalues $\nu$ of $N$ cannot be negative.

Next we derive the following commutation relations between $N$ and $a$ and $a^\dagger$:

:::{math}
:label: eq-harmosc-25a
\begin{aligned}
Na &= a^\dagger a a = a a^\dagger a - a = a(N-1),
\end{aligned}
:::

:::{math}
:label: eq-harmosc-25b
\begin{aligned}
Na^\dagger &= a^\dagger a a^\dagger = a^\dagger a^\dagger a + a^\dagger = a^\dagger (N + 1).
\end{aligned}
:::

These imply

:::{math}
:label: eq-harmosc-26a
\begin{aligned}
Na \ket{\nu} &= (\nu-1) a\ket{\nu},
\end{aligned}
:::

:::{math}
:label: eq-harmosc-26b
\begin{aligned}
N a^\dagger \ket{\nu} &= (\nu+1) a^\dagger \ket{\nu}.
\end{aligned}
:::

{eq}`eq-harmosc-26a` states that if the ket $a\ket{\nu}$ does not vanish, then it is an eigenket of $N$ with eigenvalue $\nu-1$; and {eq}`eq-harmosc-26b` states that if the ket $a^\dagger \ket{\nu}$ does not vanish, then it is an eigenket of $N$ with eigenvalue $\nu+1$. We have to worry about the possibility that these kets might vanish, since, for example, if $a \ket{\nu}=0$, then {eq}`eq-harmosc-26a` simply says $0=0$, and, in any case, we usually require an eigenket of an operator to be nonzero.

Does the ket $a\ket{\nu}$ vanish? (Recall that we are assuming that $\ket{\nu}$ is normalized, hence nonzero.) To find out, we compute its square,

:::{math}
:label: eq-harmosc-27
\matrixelement{\nu}{a^\dagger a}{\nu} = \matrixelement{\nu}{N}{\nu} = \nu,
:::

and use the fact that a vector in Hilbert space vanishes if and only if its square vanishes. We see that $a \ket{\nu}$ vanishes if and only if $\nu=0$. Similarly, computing the square of $a^\dagger \ket{\nu}$ and using the commutation relation {eq}`eq-harmosc-19`, we find,

:::{math}
:label: eq-harmosc-28
\matrixelement{\nu}{a a^\dagger}{\nu} = \matrixelement{\nu}{N+1}{\nu} = \nu+1,
:::

which never vanishes since $\nu \ge 0$. Thus, the ket $a^\dagger \ket{\nu}$ never vanishes.

From this it follows that $\nu$ must be an integer. Suppose it is not, for example, suppose $\nu=1/2$. Then $a\ket{\frac{1}{2}}$ is a nonzero ket that is an eigenket of $N$ with eigenvalue $-1/2$. But by {eq}`eq-harmosc-24` this is impossible. On the other hand, if $\nu$ is an integer, then we obtain no contradiction, since the eigenvalue can be lowered in integer steps by applying $a$ until we reach $\ket{0}$, and then the next application of $a$ gives $a\ket{0}=0$ (not some ket $\ket{-1}$). It follows that the spectrum of $N$ consists of nonnegative integers, in fact, it must consist of all nonnegative integers, since if one is present the others can be generated by applying raising and lowering operators. We will henceforth write $n$ instead of $\nu$ to emphasize that the eigenvalues of $N$ are integers.

Let the normalized eigenstates of $N$ be $\{ \ket{n}, n=0,1,\ldots \}$, with some phase conventions yet to be specified. The Hamiltonian $H$ has the same eigenstates as $N$, so

:::{math}
:label: eq-harmosc-29
H\ket{n} = E_n \ket{n},
:::

where

:::{math}
:label: eq-harmosc-30
E_n = n+{1\over 2}.
:::

Thus we have found the energy eigenvalues.

(sec-harmosc-5)=

## Phase Conventions for the Eigenstates

Now we examine the matrix elements of $a$ and $a^\dagger$ in the basis $\{ \ket{n} \}$, and choose phase conventions to make them look nice. From {eq}`eq-harmosc-26a` we have in the case $n>0$,

:::{math}
:label: eq-harmosc-31
a \ket{n} = c_n \ket{n-1},
:::

where $c_n$ is a complex constant depending on $n$. Its magnitude can be computed by squaring both sides,

:::{math}
:label: eq-harmosc-32
\matrixelement{n}{a^\dagger a}{n} = n = |c_n|^2,
:::

or

:::{math}
:label: eq-harmosc-33
a \ket{n} = e^{i\alpha_n} \sqrt{n} \, \ket{n-1},
:::

where $\alpha_n$ is the phase of $c_n$. For example, writing out the first few equations, we have

:::{math}
:label: eq-harmosc-34
\begin{aligned}
a \ket{1} &= e^{i\alpha_1} \sqrt{1} \ket{0}, \\
a \ket{2} &= e^{i\alpha_2} \sqrt{2} \ket{1}, \\

\end{aligned}
:::

etc. These equations show that by redefining the phases of $\ket{1}$, $\ket{2}$, etc., we can absorb the phase factors $e^{i\alpha_1}$, $e^{i\alpha_2}$, etc. The phase of $\ket{0}$ is not changed and can be chosen arbitrarily, but then the phases of all the other eigenstates are fixed. Then we have simply $a \ket{n} = \sqrt{n}\, \ket{n-1}$.

By a similar argument, {eq}`eq-harmosc-26b` implies

:::{math}
:label: eq-harmosc-35
a^\dagger \ket{n} = d_n \ket{n+1},
:::

where $d_n$ is a new constant, dependent on $n$. But applying $a$ to both sides, we have

:::{math}
:label: eq-harmosc-36
aa^\dagger \ket{n} = (a^\dagger a +1) \ket{n} = (n+1) \ket{n} = d_n a\ket{n+1} = d_n \sqrt{n+1} \, \ket{n},
:::

or $d_n = \sqrt{n+1}$.

In summary, we have

:::{math}
:label: eq-harmosc-37
\begin{aligned}
\boxed{\begin{aligned} a \ket{n} &= \sqrt{n} \, \ket{n-1}, \\  a^\hc \ket{n} &= \sqrt{n+1} \, \ket{n+1},
\end{aligned}}
\end{aligned}
:::

which we emphasize because of their utility in calculations involving harmonic oscillators.

(sec-harmosc-6)=

## Harmonic Oscillator Eigenfunctions

The excited state $\ket{n}$ can be built up from the ground state $\ket{0}$ by applying raising operators. Some simple induction shows that

:::{math}
:label: eq-harmosc-38
\ket{n} = { (a^\hc)^n \over \sqrt{n!}} \ket{0}.
:::

To convert the relations above into wave function language, we first find the ground state wave function by writing out the wave function equivalent of $a\ket{0}=0$, that is

:::{math}
:label: eq-harmosc-39
{1\over\sqrt{2}}\Bigl(x+\dod{}{x}\Bigr) \psi_0(x)=0,
:::

where $\psi_0(x) =\braket{x}{0}$. This is easily solved and normalized to give

:::{math}
:label: eq-harmosc-40
\psi_0(x) = {1\over\pi^{1/4}} \, e^{-x^2/2}.
:::

Next, to find the excited state wave functions, we write out the wave function equivalent of {eq}`eq-harmosc-38`, which is

:::{math}
:label: eq-harmosc-41
\psi_n(x) = {1\over\pi^{1/4}} {1\over \sqrt{n! \, 2^n}} \Bigl(x-\dod{}{x}\Bigr)^n e^{-x^2/2}.
:::

We simplify this by using the identity,

:::{math}
:label: eq-harmosc-42
\Bigl(x-\dod{}{x}\Bigr) e^{x^2/2}\, f(x)=-e^{x^2/2} \, \dod{f(x)}{x},
:::

for any function $f$. This gives

:::{math}
:label: eq-harmosc-43
\psi_n(x) = {1\over\pi^{1/4}} {(-1)^n\over \sqrt{n!\,2^n}}\, e^{x^2/2} \Bigl( \dod{}{x} \Bigr)^n e^{-x^2}.
:::

Finally, we use the Rodriguez formula for the Hermite polynomials $H_n(x)$ [see Abramowitz and Stegun, Eq.~(22.11.7)],

:::{math}
:label: eq-harmosc-44
H_n(x) = (-1)^n e^{x^2} \Bigl( \dod{}{x}\Bigr)^n e^{-x^2},
:::

to obtain

:::{math}
:label: eq-harmosc-45
\psi_n(x) = {1\over\pi^{1/4}} {1\over\sqrt{n!\,2^n}} H_n(x) \, e^{-x^2/2}.
:::

The $x$ here is really the $\bar x$ of {eq}`eq-harmosc-12`. If we restore the original units, we have

:::{math}
:label: eq-harmosc-46
\psi_n(x) = \Bigl({m\omega\over\pi\hbar}\Bigr)^{1/4} {1\over\sqrt{n!\,2^n}} H_n\Bigl( \sqrt{\ds{\ds m\omega \over \ds\hbar}}x\Bigr)\, e^{-m\omega x^2/2\hbar}.
:::

It is nice to be able to write the eigenfunctions explicitly in terms of Hermite polynomials, but for most practical purposes abstract operations involving kets and creation and annihilation operators are more useful than explicit representations in terms of wave functions.

(sec-harmosc-7)=

## The Heisenberg Picture and Classical Equations of Motion

The harmonic oscillator is a problem that is easily and profitably treated in the Heisenberg picture. In this operators will be understood to be in the Heisenberg picture unless otherwise stated, but without any $H$ subscripts as in {ref}`sec-tevolut-5`. We will also make considerable use of the classical equations of motion.

The Hamiltonian, being time-independent, is the same in the Heisenberg and Schr\"odinger pictures,

:::{math}
:label: eq-harmosc-47
H={1\over 2} (\xhat^2 + \phat^2).
:::

See {eq}`eq-tevolut-29`. The Heisenberg equations of motion are

:::{math}
:label: eq-harmosc-48
\dod{\xhat}{t}= {1\over i\hbar} [\xhat,H] = \phat, \qquad \dod{\phat}{t} = {1\over i\hbar} [\phat,H] = -\xhat.
:::

These are identical in form to the classical equations of motion,

:::{math}
:label: eq-harmosc-49
\dod{x}{t} = \frac{\partial H}{\partial p} = p, \qquad \dod{p}{t} = - \frac{\partial H}{\partial x} = -x,
:::

that is, the two sets of equations just differ by the interpretation of the symbols. The classical equations of motion {eq}`eq-harmosc-49` are easily solved in terms of some initial conditions,

:::{math}
:label: eq-harmosc-50
\begin{aligned}
\begin{pmatrix}x(t) \\ p(t) \\\end{pmatrix} = \begin{pmatrix}\cos t & \sin t \\  -\sin t & \cos t\\\end{pmatrix} \begin{pmatrix}x_0 \\ p_0 \\\end{pmatrix}.
\end{aligned}

:::

But just by putting hats on the symbols, this is also the solution of the Heisenberg equations of motion {eq}`eq-harmosc-48`,

:::{math}
:label: eq-harmosc-51
\begin{aligned}
\begin{pmatrix}\xhat(t) \\ \phat(t) \\\end{pmatrix} = \begin{pmatrix}\cos t & \sin t \\  -\sin t & \cos t\\\end{pmatrix} \begin{pmatrix}\xhat_0 \\ \phat_0 \\\end{pmatrix}.
\end{aligned}

:::

:::{figure} images/harmosc-fig01.png
:label: fig-harmosc-1
:width: 80%

The classical motion in phase space is circular, in the clockwise direction.
:::

The classical solution {eq}`eq-harmosc-50` is easily interpreted geometrically in phase space. The matrix shown is a rotation matrix in the $x$-$p$ plane, in the clockwise direction for positive $t$. Thus the phase point $\bigl(x(t),p(t)\bigr)$ traces out a circle at unit frequency (or frequency $\omega$ if we restore ordinary units), as shown in {ref}`fig-harmosc-1`.

A certain set of complex variables is particularly nice for describing the classical motion. These are

:::{math}
:label: eq-harmosc-52
\begin{aligned}
z &= {1\over\sqrt{2}} (x+ip), \qquad\qquad x = {1\over\sqrt{2}}(z + {\bar z}), \\
{\bar z} &= {1\over\sqrt{2}} (x-ip), \qquad\qquad p = {-i\over\sqrt{2}} (z - {\bar z}), \\

\end{aligned}
:::

where the overbar indicates complex conjugation. These are obviously classical versions of the annihilation and creation operators, defined in {eq}`eq-harmosc-17`. These variables make the $x$-$p$ phase plane into a complex plane, where $x$ and $p$ are proportional to the real and imaginary parts of $z$. The classical Hamiltonian expressed in terms of these variables is $H={\bar z}z = |z|^2$, as shown in {eq}`eq-harmosc-16`. The classical equations of motion in the variables $(z,{\bar z})$ are simply

:::{math}
:label: eq-harmosc-53
\dot z = -i z, \qquad \dot {\bar z} = i{\bar z},
:::

with solution,

:::{math}
:label: eq-harmosc-54
z(t) = e^{-it} \, z_0, \qquad {\bar z}(t) = e^{it} \, {\bar z}_0.
:::

These are equivalent to {eq}`eq-harmosc-50`. The phase factor $e^{-it}$ causes the point $z(t)$ in the complex plane to rotate in a clockwise direction as in {ref}`fig-harmosc-1`.

Similarly, the Heisenberg equations of motion for $a$ and $a^\dagger$ can be written out,

:::{math}
:label: eq-harmosc-55
\dot a = -ia, \qquad \dot a^\dagger = ia^\dagger,
:::

and solved,

:::{math}
:label: eq-harmosc-56
a(t) = e^{-it} \, a(0), \qquad a^\dagger(t) = e^{it} \, a^\dagger(0),
:::

exactly as in the classical equations {eq}`eq-harmosc-53` and {eq}`eq-harmosc-54`.

If $\ket{\psi}$ is some state in the Heisenberg picture, we can take expectation values of both sides of {eq}`eq-harmosc-51` with respect to $\ket{\psi}$ to obtain

:::{math}
:label: eq-harmosc-57
\begin{aligned}
\begin{pmatrix}\xpecval{\xhat}(t) \\ \xpecval{\phat}(t) \\\end{pmatrix} = \begin{pmatrix}\cos t & \sin t \\  -\sin t & \cos t\\\end{pmatrix} \begin{pmatrix}\xpecval{\xhat}(0) \\ \xpecval{\phat}(0) \\\end{pmatrix}.
\end{aligned}

:::

Recall that expectation values are the same in the Heisenberg and Schr\"odinger pictures, so this equation can be interpreted in the Schr\"odinger picture if we like. We see that the expectation values follow the classical motion, as in {eq}`eq-harmosc-51` or {ref}`fig-harmosc-1`. See the discussion of the Ehrenfest relations in {ref}`sec-tevolut-16`.

(sec-harmosc-8)=

## Introduction to Coherent States

We shall discuss coherent states in the context of a one-dimensional harmonic oscillator, continuing with dimensionless units where $m=\omega=\hbar=1$. Coherent states in quantum optics are very similar from a mathematical standpoint, although the physical interpretation is quite different.

We define a coherent state as a wave function $\psi(x) =\braket{x} {\psi}$ such that

:::{math}
:label: eq-harmosc-58
\Delta x = \Delta p = {1\over\sqrt{2}}.
:::

Thus, the coherent state is a minimum uncertainty wave packet, since $\Delta x \Delta p$ takes on its minimum value of $1/2$. The expectation values of $\xhat$ and $\phat$ can be anything, and serve as parameters of the coherent state. As shown in {ref}`sec-spatialdof-18`, a minimum uncertainty wave packet is always a Gaussian, and so also are the coherent state wave functions.

A common use of coherent states in the current literature is to explore the relationship between quantum and classical mechanics, and to obtain insight into the classical limit of a quantum system. In classical mechanics both $x$ and $p$ can be measured with infinite precision in principle, so the state of a classical system is defined by a point $(x,p)$ in phase space. In quantum mechanics, measurements of $x$ and $p$ display fluctuations about the average values $\xpecval{x}$ and $\xpecval{p}$. The statistics of the fluctuations when measured across the ensemble are restricted by the uncertainty relations {eq}`eq-postulat-50`. But since a minimum uncertainty wave packet reduces these fluctuations to their minimum value, it is natural to regard a minimum uncertainty wave packet as the quantum object that comes as close as possible to a definite classical state.

The ground state of the harmonic oscillator {eq}`eq-harmosc-40` is an example of a coherent state, one for which $\xpecval{x}=\xpecval{p}=0$. In a moment we will construct other coherent states with other values of $\xpecval{x}$ and $\xpecval{p}$.

Minimum uncertainty wave packets satisfying {eq}`eq-harmosc-58` are not the only kind possible, for example, we could have

:::{math}
:label: eq-harmosc-59
\psi(x)={\sqrt{2}\over \pi^{1/4}} \, e^{-x^2},
:::

for which

:::{math}
:label: eq-harmosc-60
\Delta x = {1\over 2}, \qquad \Delta p=1.
:::

A minimum uncertainty wave packet satisfying this condition is sometimes called a “squeezed state.” Actually, the wave function {eq}`eq-harmosc-59` is the ground state of a different harmonic oscillator than the one we have been discussing, one with different mass or frequency parameters. We cannot choose units so that $m=\omega=\hbar=1$ for both oscillators, so the distinction between a coherent state (with equal position and momentum dispersions as in {eq}`eq-harmosc-58` and a squeezed state (with unequal dispersions) is only meaningful relative to a reference oscillator. In applications to quantum optics there is a natural reference oscillator, namely, the one describing a single mode of the electromagnetic field, whose excitations are identified with photons. In the case of mechanical problems, we must simply pick some reference oscillator. In the following we assume that the oscillator we started with, {eq}`eq-harmosc-11`, with definite mass and frequency parameters, is the reference, and our definitions of coherent and squeezed states will be made relative to that reference.

:::{figure} images/harmosc-fig02.png
:label: fig-harmosc-2
:width: 80%

The ground state of the harmonic oscillator is seen as a circular blob in the classical phase space, centered on the origin.
:::

:::{figure} images/harmosc-fig03.png
:label: fig-harmosc-3
:width: 80%

Operators $T(a)$ and $S(b)$ can be used to move the state to a new location $(a,b)$ in phase space.
:::


It is useful to visualize the ground state of our harmonic oscillator as a circular blob in the classical phase space, as illustrated in {ref}`fig-harmosc-2`. This is not intended as a rigorous representation of the harmonic oscillator state, but merely as a picture that is useful for visualizing the fluctuations in the measurement process. We could make the picture more rigorous by introducing the Wigner function $W(x,p)$, discussed in Prob. {ref}`prob-spatialdof-2`(d), but for simplicity we will not do that. We note, however, that the blob could be regarded as having an area of $2\pi\hbar$, the single Planck cell occupied by the quantum state.

To represent classical states with generally nonzero values of $x$ and $p$, we would like to have minimum uncertainty wave packets with given values of $\xpecval{\xhat}$ and $\xpecval{\phat}$. These can be constructed from the ground state of the harmonic oscillator $\ket{0}$ by means of translation operators in position and momentum. Translation operators in position were discussed in {ref}`sec-spatialdof-3`. In the present (dimensionless, one-dimensional) notation, they are defined by

:::{math}
:label: eq-harmosc-61
T(a) = e^{-ia\phat},
:::

where $a$ is the displacement. Their action on position and momentum space wave functions is given by

:::{math}
:label: eq-harmosc-62
\begin{aligned}
\bigl(T(a)\psi\bigr)(x) &= \psi(x-a), \\
\bigl(T(a)\phi\bigr)(p) &= e^{-iap} \,\phi(p). \\

\end{aligned}
:::

The operators $T(a)$ have the following effect on expectation values. Let $\matrixelement{\psi}{\xhat}{\psi} = \xpecval{x}$, $\matrixelement{\psi}{\phat}{\psi} = \xpecval{p}$, and let $\ket{\psi'} = T(a) \ket{\psi}$. Then $\matrixelement{\psi'}{\xhat}{\psi'} = \xpecval{x} +a$ and $\matrixelement{\psi'}{\phat}{\psi'} = \xpecval{p}$. We summarize these by writing,

:::{math}
:label: eq-harmosc-63
\begin{pmatrix}\xpecval{x} \\ \xpecval{p} \\\end{pmatrix} \mathrel{\mathop{\\text{\rightarrowfill}}^{T(a)}} \begin{pmatrix}\xpecval{x} + a \\ \xpecval{p} \\\end{pmatrix}.
:::

The operator $T(a)$ has no effect on the dispersions $\Delta x$ or $\Delta p$. This fact is easily checked, but is plausible in any case since an ordinary probability distribution when displaced rigidly changes its mean but not its standard deviation.

Now we introduce the momentum displacement operators $S(b)$, defined by

:::{math}
:label: eq-harmosc-64
S(b) = e^{ib\xhat},
:::

which have the following effect on position and momentum space wave functions,

:::{math}
:label: eq-harmosc-65
\begin{aligned}
\bigl( S(b) \psi\bigr)(x) &= e^{ibx} \, \psi(x), \\
\bigl( S(b) \phi\bigr)(p) &= \phi(p-b), \\

\end{aligned}
:::

which may be compared to {eq}`eq-harmosc-62`. The operators $S(b)$ have the following effect on expectation values,

:::{math}
:label: eq-harmosc-66
\begin{pmatrix}\xpecval{x} \\ \xpecval{p} \\\end{pmatrix} \mathrel{\mathop{\\text{\rightarrowfill}}^{S(b)}} \begin{pmatrix}\xpecval{x} \\ \xpecval{p} +b \\\end{pmatrix},
:::

with no effect on the dispersions $\Delta x$ or $\Delta p$. The cited properties of $T(a)$ and $S(b)$ are easily verified.

Since both $T(a)$ and $S(b)$ leave the dispersions $\Delta x$ and $\Delta p$ invariant, a minimum uncertainty wave packet is mapped into another minimum uncertainty wave packet by these operators, with new values of $\xpecval{\xhat}$ and $\xpecval{\phat}$. For example, the state $T(a)S(b)\ket{0}$ can be thought of as a blob in phase space centered on $(x,p)=(a,b)$, as illustrated in {ref}`fig-harmosc-3`.

(sec-harmosc-9)=

## Heisenberg Operators and Glauber's Theorem

A minor problem, however, is that the operators $T(a)$ and $S(b)$ do not commute, something that is not surprising in view of the fact that they are exponentials of noncommuting operators. In detail, if we apply these operators in different orders to a wave function $\psi(x)$ we get

:::{math}
:label: eq-harmosc-67
\begin{aligned}
\psi(x) &\mathrel{\mathop{\\text{\rightarrowfill}}^{T(a)}} \psi(x-a) \mathrel{\mathop{\\text{\rightarrowfill}}^{S(b)}} e^{ibx} \,\psi(x-a), \\
\psi(x) &\mathrel{\mathop{\\text{\rightarrowfill}}^{S(b)}} e^{ibx} \,\psi(x) \mathrel{\mathop{\\text{\rightarrowfill}}^{T(a)}} e^{ib(x-a)} \,\psi(x-a), \\

\end{aligned}
:::

or,

:::{math}
:label: eq-harmosc-68
S(b)T(a) = e^{iab}\, T(a)S(b).
:::

This means that the phase of the final state illustrated in {ref}`fig-harmosc-3` depends on the order in which we apply $T(a)$ and $S(b)$. In order to treat $\xhat$ and $\phat$ on a more equal footing, we now introduce the *Heisenberg operators*, which carry out displacements in position and momentum simultaneously.

The Heisenberg operators are defined by

:::{math}
:label: eq-harmosc-69
W(a,b) = e^{i(b\xhat-a\phat)},
:::

which may be compared to {eq}`eq-harmosc-61` and {eq}`eq-harmosc-64`. The relation between the Heisenberg operators $W(a,b)$ and the operators $T(a)$ and $S(b)$ is clarified by Glauber's theorem, to which we now turn.

:::{admonition} Theorem
:class: theorem
:label: thm-harmosc-1

(Glauber's Theorem.) If $A$ and $B$ are operators such that $[A,B]$ commutes with both $A$ and $B$, then
:::{math}
:label: eq-harmosc-70
e^A e^B = \exp\Bigl( A + B +{1\over 2}[A,B]\Bigr).
:::
:::


To prove this theorem, we introduce the $\lambda$-dependent operator $F(\lambda)$,

:::{math}
:label: eq-harmosc-71
F(\lambda) = e^{\lambda A} e^{\lambda B},
:::

so that

:::{math}
:label: eq-harmosc-72
\dod{F(\lambda)}{\lambda} =  A e^{\lambda A} e^{\lambda B} + e^{\lambda A} B e^{\lambda B} = \bigl( A + e^{\lambda A} B e^{-\lambda A} \bigr) F(\lambda).
:::

But we know that

:::{math}
:label: eq-harmosc-73
e^{\lambda A} B e^{-\lambda A} = B + \lambda [A,B] + {\lambda^2\over 2!} [A,[A,B]] + \ldots,
:::

according to Prob. {ref}`prob-hilbert-2`(a). But since $[A,B]$ commutes with $A$ and $B$, all terms in this series after the first two vanish. Therefore we have

:::{math}
:label: eq-harmosc-74
\dod{F(\lambda)}{\lambda} = \Bigl(A+B+\lambda [A,B]\Bigr)F(\lambda).
:::

If all symbols were numbers instead of operators, the solution, subject to initial conditions $F(0)=1$, would be

:::{math}
:label: eq-harmosc-75
F(\lambda) = \exp\Bigl( \lambda(A+B) + {\lambda^2\over 2} [A,B] \Bigr),
:::

and we may take this as a guess for the solution of the operator problem. To verify that the guess is correct, we must check that the exponent in {eq}`eq-harmosc-75` commutes with its $\lambda$-derivative. This is straightforward to do. Finally, setting $\lambda=1$, we obtain the proof of the theorem. Glauber's theorem has a fairly narrow scope, but it is useful in a number of applications.

We apply Glauber's theorem to the product,

:::{math}
:label: eq-harmosc-76
T(a)S(b) = e^{-ia\phat} \, e^{ib\xhat},
:::

setting $A=-ia\phat$ and $B=ib\xhat$, so that

:::{math}
:label: eq-harmosc-77
[A,B] = -iab.
:::

The commutator is a $c$-number, which commutes with everything, so the conditions of Glauber's theorem are satisfied, and we have

:::{math}
:label: eq-harmosc-78
T(a)S(b) = e^{i(-a\phat+b\xhat -ab/2)},
:::

or,

:::{math}
:label: eq-harmosc-79
W(a,b) = e^{iab/2}\, T(a)S(b) = e^{-iab/2} S(b)T(a).
:::

The Heisenberg operator just splits the phase between the two choices, $T(a)S(b)$ and $S(b)T(a)$. It has the following effect on expectation values,

:::{math}
:label: eq-harmosc-80
\begin{pmatrix}\xpecval{x} \\ \xpecval{p} \\\end{pmatrix} \mathrel{\mathop{\\text{\rightarrowfill}}^{W(a,b)}} \begin{pmatrix}\xpecval{x} +a \\ \xpecval{p} +b \\\end{pmatrix},
:::

and leaves the dispersions $\Delta x$ and $\Delta p$ invariant.

We now define the *coherent states* by

:::{math}
:label: eq-harmosc-81
\ket{a,b} = W(a,b) \ket{0}.
:::

The coherent state $\ket{a,b}$ is parameterized by its expectation values $\xpecval{\xhat} =a$ and $\xpecval{\phat} = b$, and can be thought of as a blob centered on point $(a,b)$ in phase space as in {ref}`fig-harmosc-3`. The wave function of the coherent state $\ket{a,b}$ is easily worked out; it is

:::{math}
:label: eq-harmosc-82
\psi_{a,b}(x) = \braket{x}{a,b} = {1\over \pi^{1/4}} \exp\Bigl[ - {(x-a)^2\over 2} + ibx -{iab\over 2} \Bigr].
:::

The coherent states form a 2-parameter family of minimum uncertainty wave packets, that can be thought of as populating the entire phase plane. They have many interesting properties, for example, they form a complete set (but not orthonormal), so that an arbitrary wave function can be expressed as a linear combination of minimum uncertainty wave packets.

(sec-harmosc-10)=

## Time Evolution of Coherent States

Since a coherent state is the quantum state that is as close as we can come to a classical state, it is of interest to compare the time evolution of a coherent state in quantum mechanics to the corresponding classical time evolution. We know part of the answer already, for as shown in \secrharmosc-7, the expectation values of the time-evolved quantum state follow the classical motion. But does the initial coherent state remain a minimum uncertainty wave packet? And what about the other details of the quantum evolution?

To answer these questions, we will consider an initial state that is a coherent state, $\ket{\psi(0)} = \ket{x_0p_0}=W(x_0,p_0)\ket{0}$, where we make the replacements, $a\to x_0$, $b\to p_0$ to represent an initial point in phase space. The coherent state itself can be thought of as a blob in phase space centered on $(x_0,p_0)$, as in {ref}`fig-harmosc-4`.

We will determine the time evolution of this state under the harmonic oscillator Hamiltonian by expanding the initial state as a linear combination of harmonic oscillator eigenstates. The expansion can be achieved by using complicated identities involving Hermite polynomials and Gaussians, but an operator approach is much easier. We begin by casting the Heisenberg operator used to define the initial state into an alternative and useful form. This operator is

:::{math}
:label: eq-harmosc-83
W(x_0,p_0) = \exp\bigl[i(p_0 \xhat - x_0 \phat)\bigr].
:::

First, we adopt a complex notation for the points in phase space, exactly as in {eq}`eq-harmosc-52` but here referring to the initial point $(x_0,p_0)$,

:::{math}
:label: eq-harmosc-84
z_0 = {x_0 + ip_0 \over \sqrt{2}}, \qquad {\bar z}_0 = {x_0 -ip_0 \over \sqrt{2}},
:::

and we use $z_0$ instead of $(x_0,p_0)$ to parameterize the coherent state as well as the Heisenberg operator:

:::{math}
:label: eq-harmosc-85
\ket{x_0p_0} = W(x_0,p_0)\ket{0} = \ket{z_0} = W(z_0)\ket{0}.
:::

Similarly, we use the creation and annihilation operators (see {eq}`eq-harmosc-17` instead of $\xhat$ and $\phat$. Then the exponent in the Heisenberg operator, a linear combination of $\xhat$ and $\phat$, becomes a linear combination of $a$ and $a^\dagger$:

:::{math}
:label: eq-harmosc-86
W(x_0,p_0) = W(z_0) = \exp\bigl[i(p_0\xhat - x_0\phat)\bigr] = \exp(z_0 a^\dagger - {\bar z}_0 a).
:::

We now apply Glauber's theorem again, this time with $A=z_0 a^\dagger$ and $B=-{\bar z}_0 a$, so that $[A,B] = |z_0|^2$. The commutator is a $c$-number that commutes with everything, so the conditions of Glauber's theorem are met and we have

:::{math}
:label: eq-harmosc-87
\exp(z_0 a^\dagger) \exp(-{\bar z}_0 a) = \exp\bigl(z_0 a^\dagger - {\bar z}_0 a + \frac{1}{2} |z_0|^2\bigr),
:::

or,

:::{math}
:label: eq-harmosc-88
W(z_0) = e^{-|z_0|^2/2} \, \exp(z_0 a^\dagger) \exp(-{\bar z}_0 a).
:::

This is a form of the Heisenberg operator alternative to the form {eq}`eq-harmosc-83`.

We now apply {eq}`eq-harmosc-88` to the ground state $\ket{0}$. Since all positive powers of $a$ annihilate $\ket{0}$, we have

:::{math}
:label: eq-harmosc-89
\exp( - {\bar z}_0 a) \ket{0} =\Bigl[1 - {\bar z}_0 a + {1\over 2} {\bar z}_0^2 a^2 - \ldots\Bigr] \ket{0}= \ket{0}.
:::

As for the operator $\exp\bigl( z_0a^\hc \bigr)$, we expand the exponential and use {eq}`eq-harmosc-38` to find

:::{math}
:label: eq-harmosc-90
\ket{z_0} = W(z_0)\ket{0} = \exp\Bigl( -{|z_0|^2 \over 2} \Bigr) \sum_{n=0}^\infty {z_0^n \over \sqrt{n!}} \, \ket{n}.
:::

This is the desired expansion of the coherent state in terms of energy eigenstates. We see that the probability of finding the system in energy eigenstate $n$ is

:::{math}
:label: eq-harmosc-91
P_n = e^{-|z_0|^2} \, {|z_0|^{2n} \over n!} = e^{-(p_0^2 + x_0^2)/2} \, {(p_0^2 + x_0^2)^n \over 2^n n!}.
:::

This can be expressed in terms of the average energy of the coherent state $\ket{z_0}$, which we write as $E_0+1/2$:

:::{math}
:label: eq-harmosc-92
E_0 +{1\over2}= \matrixelement{z_0}{\Hhat}{z_0} = |z_0|^2 +{1\over 2}= {1\over2}(p_0^2 + x_0^2)+{1\over2},
:::

where the $1/2$ is the zero point energy and $E_0$ is the extra energy the coherent state acquires on being transported in phase space from $(0,0)$ to $(x_0,p_0)$. Then the probability $P_n$ can be written

:::{math}
:label: eq-harmosc-93
P_n = e^{-E_0} {E_0^n \over n!}.
:::

This makes it obvious that the probability is normalized,

:::{math}
:label: eq-harmosc-94
\sum_{n=0}^\infty P_n =1.
:::

In statistics, the distribution {eq}`eq-harmosc-93` is called a *Poisson* distribution. In quantum optics, it is the distribution of the number of photons in a coherent state. (It is customary to exclude the $1/2$ from the accounting of the energy of photons, as discussed in {ref}`ch-quantemf`.)

:::{figure} images/harmosc-fig04.png
:label: fig-harmosc-4
:width: 80%

A coherent state can be used like the hands of a clock, to tell (approximately) the phase angle $\varphi$ of the oscillator.
:::

Obviously, the coherent state is not an energy eigenstate, except in the special case $(x_0,p_0)=(0,0)$ (the ground state of the harmonic oscillator). The expansion {eq}`eq-harmosc-90` illustrates an interesting version of the time-energy uncertainty principle, $\Delta E \Delta t >\approx \hbar$, since an energy eigenstate implies exact knowledge of $E$, so that $\Delta E=0$ and $\Delta t = \infty$. This means that in an energy eigenstate, we have no knowledge of the phase angle $\varphi$ of the classical oscillator, illustrated in {ref}`fig-harmosc-4`, which could be used as a clock to tell the time. A correct semiclassical picture of an energy eigenstate is not a particle on an orbit or even a wave packet on an orbit as in {ref}`fig-harmosc-4`, but rather an object smeared out all along the classical orbit so as to give a uniform distribution in time. Recall the classical probability density in WKB theory, {eq}`eq-wkb-51`, which is uniform in time around the classical orbit. Since a coherent state such as illustrated in {ref}`fig-harmosc-4` is localized in the phase angle $\varphi$ it cannot be an energy eigenstate. Indeed, an alternative version of the time-energy uncertainty relation for harmonic oscillators is

:::{math}
:label: eq-harmosc-95
\Delta n \Delta \varphi >\approx 1,
:::

where $n$ is the quantum number.

We can make a semiquantitative check of the relation {eq}`eq-harmosc-95` in the following way. From {ref}`fig-harmosc-4`, we can estimate $\Delta\varphi$ by noting that since the radius in phase space is $(x_0^2+p_0^2)^{1/2} \sim \sqrt{E}$, and since $\Delta x = \Delta p \sim 1$, then $\Delta \varphi \sim 1/\sqrt{E}\sim 1/\sqrt{n}$. But from the Poisson distribution {eq}`eq-harmosc-91`, we have $\Delta n \sim \sqrt{n}$, so {eq}`eq-harmosc-95` is verified. In the case of the quantized electromagnetic field, the number $n$ is identified with the number of photons, and the phase angle $\varphi$ is identified with the phase of the electromagnetic wave $\Evec(\rvec,t) = E_0\epsilonvec \cos(\kvec\cdot\rvec-\omega t + \varphi)$ in the usual sense in classical electromagnetic theory. Thus we see that in the quantized theory of the electromagnetic field, a state of well defined phase angle $\varphi$ must be uncertain as to the number of photons it contains.

We can now easily find the time evolution of the coherent state. First we apply the time evolution operator to {eq}`eq-harmosc-90`, using

:::{math}
:label: eq-harmosc-96
U(t) \ket{n} = e^{-iHt} \, \ket{n} = e^{-iE_nt} \, \ket{n} = e^{-i(n+1/2)t} \, \ket{n},
:::

to obtain

:::{math}
:label: eq-harmosc-97
U(t) \ket{z_0} = e^{-it/2} e^{-|z_0|^2/2} \sum_{n=0}^\infty {z_0^n e^{-int} \over \sqrt{n!}} \, \ket{n}.
:::

In this we see the appearance of $z(t)=e^{-it}\, z_0$, the solution of the classical equations of motion (see {eq}`eq-harmosc-54`. and we note that $|z_0| = |z(t)|$. Thus we can write {eq}`eq-harmosc-97` as

:::{math}
:label: eq-harmosc-98
U(t)\ket{z_0} = e^{-it/2} e^{-|z(t)|^2/2} \sum_{n=0}^\infty {z(t)^n \over \sqrt{n!}} \ket{n} =e^{-it/2} \ket{z(t)},
:::

where in the last step we have used {eq}`eq-harmosc-90` with $z_0$ replaced by $z(t)$. Therefore, to within the time-dependent phase $e^{-it/2}$, an initial coherent state remains a coherent state in the course of time in the harmonic oscillator, with the phase space parameters $(x,p)$ following a classical trajectory. The dispersions $\Delta x$ and $\Delta p$ are constant in time, retaining their values given by {eq}`eq-harmosc-58`, and the wave packet remains a minimum uncertainty wave packet for all times.

A free particle Gaussian wave packet that is minimum uncertainty at $t=0$ spreads in time, with $\Delta x$ becoming arbitrarily large as $t\to\infty$, as shown in Prob. {ref}`prob-tevolut-3`. For these initial conditions, the wave packet also spreads as $t\to-\infty$, that is, for negative times its width shrinks until it reaches the minimum uncertainty value at $t=0$, after which it grows.

We have just shown, however, that in the case of the harmonic oscillator, an initial coherent state, a minimum uncertainty wave packet, remains minimum uncertainty with a constant value of $\Delta x$ as time advances. Another interesting case is when the initial state is a squeezed state. In this case it can be shown that under the time evolution generated by the harmonic oscillator, the width of the wave packet oscillates with twice the frequency of the oscillator itself, that is, the wave packet “breathes” periodically. This wave packet is minimum uncertainty, that is, it satisfies $\Delta x\Delta p=\hbar/2$, at each integer multiple of a quarter period, while in between it satisfies $\Delta x\Delta p > \hbar/2$. These facts can be shown either by operator methods or more direct methods based on solving the Schr\"odinger equation.

In the case of Hamiltonians that are quadratic polynomials in $\xhat_i$ and $\phat_i$, such as the harmonic oscillator, not only are the Ehrenfest relations exact, but all the properties of the quantum time evolution bear an especially close relationship to the classical motion. For example, the spreading or breathing of wave packets can be understood in terms of ensembles of particles in the classical phase space.

\problems

(prob-harmosc-1)=

**Problem \prbdharmosc-1..** 

:::{math}
:label: eq-harmosc-99
\phi_n(p) = \int {dx\over\sqrt{2\pi}} \, e^{-ipx} \psi_n(x).
:::

Get the phases right.

(prob-harmosc-2)=

**Problem \prbdharmosc-2..** 

:::{math}
:label: eq-harmosc-100
H={p_1^2 + p_2^2\over 2m} + {m\over 2} (\omega_1^2 x_1^2 + \omega_2^2 x_2^2).
:::

An arbitrary potential that is quadratic in $x_1$ and $x_2$ and that has a minimum can be brought into this form by shifting the origin and rotating the axes, if necessary. The frequencies in the 1- and 2-directions are allowed to be different. You may know that the classical orbits in this case are Lissajous figures. The orbit is closed if the frequencies are commensurable.

The case in which $\omega_1=\omega_2=\omega$ is especially interesting. Two or higher dimensional oscillators with equal frequencies occur in many examples of molecular vibrations. In two dimensions this gives an example of two-dimensional central force motion,

:::{math}
:label: eq-harmosc-101
H={1\over 2m}(p_1^2 + p_2^2) + {m\omega^2 \over 2}(x_1^2+x_2^2),
:::

since the potential is a function of the radius $\rho=(x_1^2+x_2^2)^{1/2}$.

All central force problems in two dimensions have a symmetry, which is rotations in the plane. The generator of this symmetry is

:::{math}
:label: eq-harmosc-102
L=x_1p_2 - x_2 p_1.
:::

It is the $z$-component of angular momentum, and it is a constant of motion (see {ref}`sec-tevolut-10`) for any central force problem in two dimensions. But the two-dimensional, isotropic harmonic oscillator has further constants of motion, indicating a larger symmetry group than just rotations in the plane.

Let us choose units so that $m=\hbar=\omega=1$ in {eq}`eq-harmosc-101`. Then

:::{math}
:label: eq-harmosc-103
H={1\over2}(p_1^2+x_1^2) + {1\over2}(p_2^2+x_2^2).
:::

Define creation and annihilation operators as in {eq}`eq-harmosc-17`,

:::{math}
:label: eq-harmosc-104
a_\mu={x_\mu + ip_\mu\over\sqrt{2}}, \qquad a_\mu^\dagger={x_\mu - ip_\mu\over\sqrt{2}},
:::

where we let Greek indices run over 1,2. These obey a generalization of the commutation relations {eq}`eq-harmosc-19`,

:::{math}
:label: eq-harmosc-105
[a_\mu,a_\nu]=0, \qquad [a_\mu,a^\dagger_\nu]=\delta_{\mu\nu}, \qquad [a^\dagger_\mu,a^\dagger_\nu]=0,
:::

which is just a statement that each oscillator has commutation relations like {eq}`eq-harmosc-19`, and the variables of one oscillator commute with the variables of the other.

\problempart{(a)} Define number operators as in {eq}`eq-harmosc-21`,

:::{math}
:label: eq-harmosc-106
N_\mu = a^\dagger_\mu a_\mu, \qquad \mu=1,2,
:::

Then define further operators,

:::{math}
:label: eq-harmosc-107
I = {1\over2} (N_1 + N_2) = {1\over 2} \sum_\mu a^\dagger_\mu a_\mu,
:::

and

:::{math}
:label: eq-harmosc-108
J_i = {1\over2} \sum_{\mu\nu} a^\dagger_\mu (\sigma_i)_{\mu\nu}\, a_\nu,
:::

where $\sigma_i$ are the Pauli matrices and $i=1,2,3$.

Find the energy eigenvalues and degeneracies of the Hamiltonian {eq}`eq-harmosc-103`, that is, find the spectrum of $H$ and the dimensions of the energy eigenspaces. Now let $j$ be an eigenvalue of $I$. What are the allowed values of $j$ (that is, what is the spectrum of $I$)?

\problempart{(b)} Show that if $F_{\mu\nu}$ and $G_{\mu\nu}$ are $2\times2$ matrices of numbers, and if we define operators $f$ and $g$ by

:::{math}
:label: eq-harmosc-109
\begin{aligned}
f&=\sum_{\mu\nu} a^\dagger_\mu F_{\mu\nu}\, a_\nu, \\
g&=\sum_{\mu\nu} a^\dagger_\mu G_{\mu\nu}\, a_\nu, \\

\end{aligned}
:::

then

:::{math}
:label: eq-harmosc-110
[f,g] = \sum_{\mu\nu} a^\dagger_\mu [F,G]_{\mu\nu} \, a_\nu.
:::

Use this result to evaluate the commutators $[I,J_i]$ and $[J_i,J_j]$. Explain why all three $J_i$ are constants of motion. Find a relationship between one of the $J_i$ and $L$ in {eq}`eq-harmosc-102`.

\problempart{(c)} Show that

:::{math}
:label: eq-harmosc-111
J^2 = \sum_i J_i^2 = I(I+1).
:::

You may find it useful to use the identity,

:::{math}
:label: eq-harmosc-112
\sum_i (\sigma_i)_{\mu\nu} \, (\sigma_i)_{\alpha\beta} = 2\delta_{\mu\beta}\,\delta_{\nu\alpha} - \delta_{\mu\nu}\,\delta_{\alpha\beta},
:::

which is the solution to Prob. {ref}`prob-hilbert-3`(d).

\problempart{(d)} Let $n_1$ and $n_2$ be the usual harmonic oscillator quantum numbers for oscillators 1 and 2 in {eq}`eq-harmosc-103`, and let the energy eigenstates be $\ket{n_1n_2}$. Show that $\ket{n_1n_2}$ is an eigenket of $J^2$ and $J_3$. Express the eigenvalue of $J^2$ in terms of $j$, and let the eigenvalue of $J_3$ be $m$ (not to be confused with the mass, which at this point we have set to unity). For a given value of $j$, what values of $m$ are allowed?

You will see that this problem reproduces the beginnings of angular momentum theory. It can be extended to produce formulas for the Clebsch-Gordan coefficients, the rotation $d$-matrices (see {ref}`ch-repsamos`), and many other things, with everything based ultimately on harmonic oscillator creation and annihilation operators.

(prob-harmosc-3)=

**Problem \prbdharmosc-3..** 

\problempart{(a)} Find convenient expressions for $W(z_0)^\dagger aW(z_0)$ and $W(z_0)^\dagger a^\dagger W(z_0)$, where $W(z_0)$ is the Heisenberg operator {eq}`eq-harmosc-86` and $a$ and $a^\dagger$ are the annihilation and creation operators. **Hint:** See Prob. {ref}`prob-hilbert-2`(a). Then show that the coherent state $\ket{z_0} = W(z_0)\ket{0}$ is an eigenstate of the annihilation operator $a$ with eigenvalue $z_0$.

\problempart{(b)} The annihilation operator is not Hermitian, so its eigenvalues are not real in general, nor are its eigenstates orthonormal, that is, $\braket{z_0}{z_1} \ne 0$ when $z_0 \ne z_1$. Nevertheless, they are complete in a certain sense. Prove that

:::{math}
:label: eq-harmosc-113
\int {dx_0 dp_0 \over 2\pi}  \,\ketbra{z_0}{z_0} = 1.
:::

This resolution of the identity shows that an arbitrary wave function can be expanded as a linear combination of coherent states, that is, Gaussian wave packets. However, the expansion is not unique, because the coherent states are actually overcomplete (they are not linearly independent). In fact, there are many vanishing linear combinations of coherent states (with nonzero coefficients). Nevertheless, the formula {eq}`eq-harmosc-113` looks neat. It can be used as the basis of a path integral.

\problempart{(c)} Use the Heisenberg picture to obtain expressions for $U(t) a U(t)^\dagger$ and $U(t) a^\dagger U(t)^\dagger$, where $a$ and $a^\dagger$ are the usual annihilation and creation operators in the Schr\"odinger picture, and $U(t)$ is the time-evolution operator for the harmonic oscillator. Then use these to obtain a simple expression for

:::{math}
:label: eq-harmosc-114
U(t) W(z_0) U(t)^\dagger.
:::

Finally, use that to obtain a simple expression for $U(t) \ket{z_0}$. This approach to finding the time evolution of a coherent state is easier than the one taken in the notes, which involved normal ordered Taylor series.

(prob-harmosc-4)=

**Problem \prbdharmosc-4..** 

:::{figure} images/harmosc-fig05.png
:label: fig-harmosc-5
:width: 80%

A simple one-dimensional model of an iron atom coupled to the modes of the crystal lattice. The emitted photon has energy $\hbar\omega_0$, while the frequency of the spring is $\omega$. The mass $M$ of the lattice is taken to $\infty$. $m$ is the mass of the iron atom.
:::

An iron atom of mass $m$ is attached by a spring to a large mass $M\to\infty$. The frequency of the harmonic oscillator is $\omega$, while the frequency of the photon is $\omega_0$. When the iron atom emits the photon, it suffers a recoil momentum whose magnitude is

:::{math}
:label: eq-harmosc-115
\hbar k_0 = \hbar\omega_0/c.
:::

Classically, we can say that the effect of the emission of the photon is to map the position and momentum of the iron atom according to

:::{math}
:label: eq-harmosc-116
x \mapsto x, \qquad p \mapsto p+\Delta p,
:::

where $|\Delta p| = \hbar k_0$.

If $\psi(x)$ is the wave function of the iron atom before the photon is emitted, what is the wave function after the photon is emitted, that is, after the impulse indicated by {eq}`eq-harmosc-116` is delivered? Express your answer in terms of $\Delta p$.

If the iron atom is initially in the ground state of the harmonic oscillator ($n=0$), what is the probability that it will be found in state $n$ after the photon has been emitted? That is, what is the probability of the transition $0\to n$? Express your answer as a function of $\Delta p$ and other parameters of the problem. Verify that the sum of probabilities is 1.

In particular, you will see that there is a non-zero probability for recoilless emission, $0\to 0$.

You may find it convenient to carry out the calculation in units in which $m=\hbar=\omega=1$, where $\omega$ is the frequency of the harmonic oscillator (not to be confused with the frequency of the photon). If so, you should restore ordinary units in your final answer.
