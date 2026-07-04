---
title: "01. The Mathematical Formalism of Quantum Mechanics"
---
(ch-hilbert)=

# 01. The Mathematical Formalism of Quantum Mechanics

(sec-hilbert-1)=

## Introduction

The prerequisites for Physics 221A include a full year of undergraduate quantum mechanics. In this semester we will survey that material, organize it in a more logical and coherent way than the first time you saw it, and pay special attention to fundamental principles. We will also present some new material. Physics 221B will largely consist of new material.

We begin by presenting some of the mathematical formalism of quantum mechanics. We will introduce more mathematics later in the course as needed, but for now we will concentrate on the linear algebra of spaces of wave functions, which are called *Hilbert spaces*. These notes gather together and summarize most of what you will need to know of this subject, so we can proceed with other matters. In the next set of notes we will turn to the physical postulates of quantum mechanics, which allow us to connect experimental results with the mathematics presented here.

Introductory courses on linear algebra are usually limited to finite-dimensional, real vector spaces. Making the vector spaces complex is a small change, but making them infinite-dimensional is a big step if one wishes to be rigorous. We will make no attempt to be rigorous in the following---to do so would require more than one course in mathematics and leave no time for the physics. Instead, we will follow the usual procedure in physics courses when encountering new mathematics, which is to proceed by example and analogy, attempting to gain an intuitive understanding for some of the main ideas without going into technical proofs. Specifically, in dealing with Hilbert spaces we will try to apply what we know about finite-dimensional vector spaces to the infinite-dimensional case, often using finite-dimensional intuition in infinite dimensions, and we will try to learn where things are different in infinite dimensions and where one must be careful. Fortunately, it is one of the consequences of the mathematical definition of a Hilbert space that many of its properties are the obvious generalizations of those that hold in finite dimensions, so much of finite-dimensional intuition does carry over. We will use what we know about spaces of wave functions (an example of a Hilbert space) to gain some intuition about where this is not so.

(sec-hilbert-2)=

## Hilbert Spaces

Let us consider a wave function $\psi(x)$ for a one-dimensional quantum mechanical problem. In practice it is common to require $\psi(x)$ to be normalized, but for the purpose of the following discussion we will require only that it be normalizable, that is, that

:::{math}
:label: eq-hilbert-1
\int |\psi(x)|^2 \, dx < \infty
:::

(which means that the integral is finite; usually when we write an integral without limits like the one above, we mean that the limits are $-\infty$ to $+\infty$, or over all of space if the integral is multidimensional). Wave functions that are not normalizable cannot represent physically realizable states, because the probability of finding a real particle somewhere in space must be unity. Nevertheless, wave functions that are not normalizable, such as the free particle energy eigenfunctions $e^{ikx}$, are definitely useful for some purposes, and we will have to say something about them later. For now, however, we will stick to normalizable wave functions.

Mathematically speaking, the space of complex functions that are normalizable (or *square integrable*) in the sense of {eq}`eq-hilbert-1` constitutes a complex vector space. This is because if $\psi(x)$ is square-integrable, then so is $c\psi(x)$, where $c$ is any complex number, and if $\psi_1(x)$ and $\psi_2(x)$ are square-integrable, then so is $\psi_1(x) + \psi_2(x)$. Moreover, the space is infinite-dimensional (see \secrhilbert-29). This vector space is an example of a *Hilbert space*; in general, a Hilbert space is a complex, inner product vector space (a vector space upon which an inner or scalar product is defined) with certain additional properties that will not concern us in this course (see \secrhilbert-29). Often the term “Hilbert space” is defined to be an infinite-dimensional space, but in this course we will refer to any of the vector spaces of wave functions that occur in quantum mechanics as Hilbert spaces, even when finite-dimensional.

As you know, given a normalized wave function $\psi(x)$ in configuration space, $|\psi(x)|^2$ is the probability density for making measurements of position on an ensemble of systems. The wave function $\psi(x)$ is connected physically with position measurements. (See {ref}`sec-classmech-3` for the definition of “configuration space.”)

Given $\psi(x)$ in configuration space, one can compute the corresponding wave function $\phi(p)$ in momentum space, by a version of the Fourier transform:

:::{math}
:label: eq-hilbert-2
\phi(p) = {1\over \sqrt{2\pi\hbar}} \int dx\, e^{-ipx/\hbar} \, \psi(x).
:::

The Fourier transform is linear and invertible (via the inverse Fourier transform), so it provides a one-to-one, linear map between the space of wave functions $\psi(x)$ and that of $\phi(p)$. Moreover, according to the Parseval identity, the norm of $\psi$ in configuration space and the norm of $\phi$ in momentum space are equal,

:::{math}
:label: eq-hilbert-3
\int dx \, |\psi(x)|^2 = \int dp\, |\phi(p)|^2,
:::

so if we consider the Hilbert space of normalizable wave functions $\{\psi(x)\}$ in configuration space, then the set $\{\phi(p)\}$ of corresponding momentum space wave functions also forms a Hilbert space. (The “norm” of a wave function is the square root of the quantity shown in {eq}`eq-hilbert-3`; it is like the length of a vector.)

The momentum space wave function $\phi(p)$ is connected with the measurement of momentum, in particular, if $\phi(p)$ is normalized then $|\phi(p)|^2$ is the probability density for momentum measurements on an ensemble of systems. The Parseval identity expresses the equality of the total probability for measurements of either position or momentum.

Likewise, let $\{u_n(x), n=1,2,\ldots\}$ be an orthonormal set of energy eigenfunctions, $Hu_n(x) = E_nu_n(x)$ for some Hamiltonian $H$. An arbitrary wave function $\psi(x)$ can be expanded as a linear combination of the functions $u_n(x)$, that is, we can write

:::{math}
:label: eq-hilbert-4
\psi(x) = \sum_n c_n u_n(x),
:::

where the expansion coefficients $c_n$ are given by

:::{math}
:label: eq-hilbert-5
c_n = \int dx \, u_n(x)^\cc \psi(x).
:::

{eq}`eq-hilbert-4` can be regarded as a linear transformation taking us from the sequence of coefficients $(c_1,c_2,\ldots)$ to the wave function $\psi(x)$, while {eq}`eq-hilbert-5` goes the other way.

The sequence of coefficients $(c_1,c_2,\ldots)$ uniquely characterizes the state of the system, and we can think of it as the “wave function in energy space.” Notice that if the sequence is normalized, $\sum_n|c_n|^2=1$, then the probability of making a measurement $E=E_n$ of energy is $|c_n|^2$. Also, the norm of the original wave function $\psi(x)$ can be expressed in terms of the expansion coefficients by

:::{math}
:label: eq-hilbert-6
\int dx \, |\psi(x)|^2 = \sum_n |c_n|^2,
:::

which is finite if $\psi(x)$ belongs to Hilbert space. This is another expression of conservation of probability. Mathematically speaking, the set of sequences $\{(c_1,c_2,\ldots)\}$ of complex numbers of finite norm is yet another example of a Hilbert space.

Thus, we have three Hilbert spaces, the two spaces of wave functions, $\{\psi(x)\}$ and $\{\phi(p)\}$, and the space of sequences $\{(c_1,c_2,\ldots)\}$, all assumed to be normalizable. These Hilbert spaces are isomorphic, in the sense that the vectors of each space are related to one another by invertible, norm-preserving linear transformations, so they all contain the same information. (See \secrhilbert-29 for some mathematical points regarding Hilbert spaces of wave functions.) Therefore none of these spaces can be taken as more fundamental than the other; any calculation that can be carried out in one space (or in one *representation*, as we will say), can be carried out in another.

Psychologically, there is a tendency to think of wave functions $\psi(x)$ on configuration space as fundamental, probably because we are used to thinking of fields such as electric fields defined over physical space. This is also the bias imposed on us by our first courses in quantum mechanics, as well as the historical development of the subject. Also, we live in physical space, not momentum space. But the Schr\"odinger wave function is not really defined over physical space, rather it is defined over *configuration space*, which is the same only in the case of a single particle (see {ref}`sec-classmech-3`). Furthermore, completely apart from the mathematical equivalence of the different Hilbert spaces discussed above, the physical postulates of quantum mechanics show that the different wave functions discussed above correspond to the measurement of different sets of physical observables. They also show that there is a kind of democracy among the different physical observables one can choose to measure, as long as the set of observables is compatible and complete in a sense we will discuss later.

Finally, even if we do have a single particle moving in three dimensions so the wave function $\psi(\rvec)$ can be thought of as a field over physical space, the physical measurement of $\psi(\rvec)$ is very different from the measurement of a classical field such as the electric field or the pressure of a fluid. We have thermometers that can measure the temperature at a point, we have pressure gauges, and it is possible to measure electric and magnetic fields at points of space. But there is no such thing as a “$\psi$-meter” for measuring the wave function $\psi(\rvec)$. Later we will consider how one can obtain $\psi(\rvec)$ from measurements, but the process involves several subtleties. (In particular, it requires one to understand the difference between a pure and a mixed state; only pure states have wave functions.) It is a very different business than the measurement of a classical field. See Prob. {ref}`prob-postulat-3`.

In summary, it is probably best to think of the different wave functions as equivalent descriptions of the same physical reality, none of which is more fundamental than the other. This leads to the concept of the state space of a quantum mechanical system as an abstract vector space in which the state vector lies, while the various wave functions are the expansion coefficients of this state vector with respect to some basis. Different bases give different wave functions, but the state vector is the same.

This was not the point of view in the early days of quantum mechanics, when $\psi(\rvec)$ was seen as a complex-valued field on physical space, and before it was completely clear what the wave function of multiparticle systems should be. We will return to this earlier point of view when we take up the Dirac equation and field theory, but that reconsideration will not change the basic concept of the state space for the quantum mechanical system, a complex vector space in which the state vector lies.

Thus, the mathematical formalism of quantum mechanics exhibits a kind of form invariance or *covariance* with respect to the set of observables one chooses to represent the states of a system. This view of quantum mechanics, and the transformation theory connected with changes of representation, was worked out in the early days of the quantum theory, notably by Dirac, Born, Jordan, von Neumann and others.

(sec-hilbert-3)=

## Dirac Ket Notation

Since none of the three Hilbert spaces has any claim over the other, it is preferable to use a notation that does not prejudice the choice among them. This is what the Dirac notation does. In the Dirac notation, a state of a system is represented by a so-called *ket vector*, denoted by $\ket{\;}$, which stands for any of the three wave functions discussed above, $\psi(x)$, $\phi(p)$, or $\{c_n\}$, assuming that they are related by the transformations {eq}`eq-hilbert-2` and {eq}`eq-hilbert-5`. It is customary to put a symbol into the ket to identify the state, to write, for example, $\ket{\psi}$ [although the choice of the letter $\psi$ seems to point to something special about the configuration space wave function $\psi(x)$, which there is not]. Some people think of a ket $\ket{\psi}$ as simply another notation for a wave function on configuration space, and I have even seen some authors write equations like

:::{math}
:label: eq-hilbert-7
\psi(x) = \ket{\psi}.  
:::

But our point of view will be that the space of kets is yet another Hilbert space, an abstract space that is isomorphic to but distinct from any of the concrete Hilbert spaces of wave functions discussed above. Thus, we will never use equations like {eq}`eq-hilbert-7`. I think this approach is appropriate in view of the physical postulates of quantum mechanics, which show how one can construct a Hilbert space out of the results of physical measurements. There is no need to start with wave functions. Therefore we will now put wave functions aside, and discuss the mathematical properties of ket spaces. Later, in {ref}`ch-spatialdof`, we will return to wave functions, in effect deriving them from the ket formalism. In this set of notes, we use wave functions only for the purpose of illustrating some general features of Hilbert spaces, calling on your experience with them in a previous course in quantum mechanics.

(sec-hilbert-4)=

## Kets, Ket Spaces and Rays

Kets and ket spaces arise out of the physical postulates of quantum mechanics, which we will discuss in {ref}`ch-postulat`. For now we will just say enough to get started.

A basic postulate of quantum mechanics is that a given physical system is associated with a certain complex vector space, which we will denote by $\ES$. The physical principles by which this vector space is constructed will be discussed later, but for now we simply note that the properties of this space such as its dimensionality are determined by the physics of the system under consideration. For some systems, $\ES$ is finite-dimensional (notably spin systems), while for others it is infinite-dimensional. The vectors of the space $\ES$ are called *kets*, and they are denoted in the Dirac notation by $\ket{\;}$, as discussed above. Since $\ES$ is a complex vector space, the multiplication of kets by complex numbers and the addition of kets is defined. The product of a complex number $c$ and a ket $\ket{\psi}$ can be written in either order,

:::{math}
:label: eq-hilbert-8
c\ket{\psi} = \ket{\psi}c.
:::

In addition, there exist physical principles that allow us to associate a definite (pure) state of a physical system with a ray in $\ES$. We will say more about this association later, when we will define what we mean by a pure state of a physical system, but for now we simply note that a ray in $\ES$ is a 1-dimensional vector subspace of $\ES$, that is, it consists of kets $\ket{\psi}$ related to some nonzero ket $\ket{\psi_0}$ by a complex multiplicative factor, that is,

:::{math}
:label: eq-hilbert-9
\ket{\psi} = c\ket{\psi_0},
:::

for some complex number $c$. The kets $\ket{\psi}$ in the ray differ from one another only by normalization and overall phase, which have no physical significance; thus, we say that a (pure) physical state corresponds to the ray (not to any particular ket in the ray).

(sec-hilbert-5)=

## The Dual Space and Bras

You are probably familiar with the fact that kets correspond to wave functions $\psi(x)$, while bras correspond to complex conjugated wave functions $\psi(x)^\cc$. But if we are doing without wave functions until we can properly derive them, how do we describe bras and the complex conjugation of kets? The answer is the dual correspondence.

Also, it would appear that $\psi(x)^\cc$ is just another wave function, so it should belong to the same space of wave functions as $\psi(x)$. But it turns out that there is great advantage in regarding kets and bras as belonging to two different spaces. Kets belong to the space $\ES$, while bras belong to the so-called *dual space*, denoted $\ES^\cc$.

If $\ES$ is any (complex) vector space, then the *dual space*, denoted $\ES^\cc$, is the space of complex-valued, linear operators that act on $\ES$. In the Dirac notation, such operators are called *bras*, and are denoted $\bra{\;}$. (In mathematics, they are called *forms, covectors* or *dual vectors*.) As with kets, it is customary to insert some symbol to identify a bra and distinguish it from other bras, such as $\bra{\alpha}$. In mathematical language, we write

:::{math}
:label: eq-hilbert-10
\bra{\alpha}:\ES \to \Complexes,
:::

which means that $\bra{\alpha}$ maps a ket into a complex number. To be a bra, the map must be linear. If $\ket{\psi}$ is a ket, then the complex number that results by letting $\bra{\alpha}$ act on it can be written $\bra{\alpha}(\ket{\psi})$. Usually we drop the parentheses write the complex number simply as $\braket{\alpha}{\psi}$, but if we wish to emphasize the interpretation of the bra as an operator acting on kets we will keep the parentheses.

Since the map is required to be linear, we have

:::{math}
:label: eq-hilbert-11
\bra{\alpha}(c_1\ket{\psi_1} + c_2\ket{\psi_2}) = c_1 \bra{\alpha}(\ket{\psi_1}) + c_2 \bra{\alpha} (\ket{\psi_2}).
:::

A bra, as a linear operator acting on kets, is not to be confused with the familiar linear operators used in quantum mechanics, such as the Hamiltonian operator, which also act on kets. The distinction is that a bra is a complex-valued operator, whereas the Hamiltonian and other such operators are ket-valued operators.

It is easy to see how to define the product of a bra with a complex scalar, and the sum of two bras; we simply set

:::{math}
:label: eq-hilbert-12
(c\bra{\alpha})(\ket{\psi}) = c\bra{\alpha}(\ket{\psi}),
:::

and

:::{math}
:label: eq-hilbert-13
(\bra{\alpha_1} + \bra{\alpha_2})(\ket{\psi}) = \bra{\alpha_1}(\ket{\psi}) + \bra{\alpha_2}(\ket{\psi}).
:::

Therefore the set of all bras acting on a given ket space forms a vector space in its own right, which by definition is the dual space $\ES^\cc$. It is easy to show that if $\ES$ is finite-dimensional, then $\ES^\cc$ is also, and has the same dimension. If $\ES$ is infinite-dimensional, then the dual space $\ES^\cc$ is also infinite-dimensional.

What we have said so far allows us to talk about bras, but not to convert a ket into a bra (the analog of the complex conjugation of wave functions). To do that we need to introduce the metric or scalar product on our ket space. In real, Euclidean vector spaces the metric is what allows us to measure distances, and from that, angles. This is an analogy to keep in mind while thinking about the metric in (complex) Hilbert spaces, because it provides useful geometrical interpretations.

(sec-hilbert-6)=

## The Scalar Product and Dual Correspondence

We postulate the existence of a metric or scalar product $g$ on $\ES$, which is a function

:::{math}
:label: eq-hilbert-14
g:\ES\times\ES \to \Complexes
:::

with certain properties. This notation means that $g$ is a function that takes two kets and produces a complex number; for example, we will write $g(\ket{\psi},\ket{\phi})$ for the complex number that results upon letting $g$ act on kets $\ket{\psi}$ and $\ket{\phi}$. The postulated properties of $g$ are the following. First, $g$ is linear in its second operand and antilinear in its first operand. Explicitly, this means

:::{math}
:label: eq-hilbert-15a
\begin{aligned}
g(\ket{\psi}, c_1\ket{\phi_1}+c_2\ket{\phi_2}) &= c_1 g(\ket{\psi},\ket{\phi_1}) + c_2 g(\ket{\psi},\ket{\phi_2}),
\end{aligned}
:::

:::{math}
:label: eq-hilbert-15b
\begin{aligned}
g(c_1\ket{\psi_1}+c_2\ket{\psi_2},\ket{\phi}) &= c_1^\cc g(\ket{\psi_1},\ket{\phi}) + c_2^\cc g(\ket{\psi_2},\ket{\phi}).
\end{aligned}
:::

(An antilinear function requires us to take the complex conjugate of the coefficients when evaluating it on linear combinations of vectors.) Next, $g$ is symmetric or Hermitian, which means

:::{math}
:label: eq-hilbert-16
g(\ket{\psi},\ket{\phi}) = g(\ket{\phi},\ket{\psi})^\cc.
:::

Third, $g$ is positive definite, which means

:::{math}
:label: eq-hilbert-17
g(\ket{\psi},\ket{\psi}) \ge 0,
:::

for all $\ket{\psi}$, with equality holding if and only if $\ket{\psi}=0$. Note that by property {eq}`eq-hilbert-16`, the left hand side of {eq}`eq-hilbert-17` is necessarily real.

Next, given the metric $g$, we can define the *dual correspondence*, which is a mapping that converts kets into bras. It is the map which in wave function language amounts to taking the complex conjuate of a wave function. We will denote the dual correspondence by $DC$; it is the map

:::{math}
:label: eq-hilbert-18
DC: \ES \to \ES^\cc.
:::

If $\ket{\psi}$ is a ket, then we will denote the bra corresponding to it under the dual correspondence by $\bra{\psi}$, with the same identifying symbol. We define the bra $\bra{\psi}$ in terms of its action on an arbitrary ket $\ket{\phi}$; the definition is

:::{math}
:label: eq-hilbert-19
\bra{\psi}(\ket{\phi}) = g(\ket{\psi},\ket{\phi}).
:::

The idea is that in the scalar product, we regard the first argument as fixed and the second as variable, which gives us a complex valued function of kets, which according to {eq}`eq-hilbert-15a` is linear. Thus, the function is a bra. By way of notation, we will denote the bra resulting from a given ket under the dual correspondence by a dagger, so that if

:::{math}
:label: eq-hilbert-20
DC:\ket{\psi} \mapsto \bra{\psi},
:::

then we will write

:::{math}
:label: eq-hilbert-21
\bra{\psi} = (\ket{\psi})^\hc.
:::

We will say that $\bra{\psi}$ is the *Hermitian conjugate* of $\ket{\psi}$. We note that since the scalar product is antilinear in its first operand, the dual correspondence is antilinear, that is,

:::{math}
:label: eq-hilbert-22
(c_1\ket{\psi_1}+c_2\ket{\psi_2})^\hc = c_1^\cc \bra{\psi_1} + c_2^\cc \bra{\psi_2}.
:::

If $\ES$ is finite-dimensional, then it is easy to prove that the dual correspondence is one-to-one and onto, so that every bra is in fact the Hermitian conjugate of some ket. This follows from the postulated properties of the metric. In infinite-dimensional spaces, this is true only if certain restrictions are placed on the bra space. We will ignore such technicalities, and proceed as if the dual correspondence is always one-to-one and onto (which, with the right understandings, it is for a Hilbert space). This means that every bra is the dagger of some unique ket, so the dual correspondence has an inverse. We will denote the inverse with the same dagger notation, so that

:::{math}
:label: eq-hilbert-23
\ket{\psi} = (\bra{\psi})^\hc,
:::

and so that

:::{math}
:label: eq-hilbert-24
(\ket{\psi})^{\hc\hc} = \ket{\psi}.
:::

We now simplify the notation for the scalar product by dropping the parentheses on the left hand side of {eq}`eq-hilbert-19`. That is, we write

:::{math}
:label: eq-hilbert-25
\bra{\psi}(\ket{\phi}) = g(\ket{\psi},\ket{\phi})= \braket{\psi}{\phi}.
:::

With this notational change, we can rewrite properties {eq}`eq-hilbert-16` and {eq}`eq-hilbert-17` of the metric as

:::{math}
:label: eq-hilbert-26
\braket{\psi}{\phi} = \braket{\phi}{\psi}^\cc,
:::

and

:::{math}
:label: eq-hilbert-27
\braket{\psi}{\psi} \ge 0,
:::

for all $\ket{\psi}$, with equality if and only if $\ket{\psi}=0$. The complex number $\braket{\psi}{\phi}$ is sometimes called the *inner product* or *scalar product* of $\ket{\psi}$ and $\ket{\phi}$. Using the notation shown in {eq}`eq-hilbert-25`, we can henceforth dispense with the $g$-notation when talking about scalar products.

(sec-hilbert-7)=

## The Schwarz Inequality

We can now prove an important theorem, namely the *Schwarz inequality*. We are interested in this inequality for complex vector spaces, but it is also true in real vector spaces with a positive definite inner product, that is, in Euclidean spaces. There it is equivalent to the geometrical fact that the shortest distance between two points is a straight line. The Schwarz inequality is important in quantum mechanics because it is used to prove the Heisenberg uncertainty relations.

The Schwarz inequality says that

:::{math}
:label: eq-hilbert-28
|\braket{\psi}{\phi}|^2 \le \braket{\psi}{\psi} \braket{\phi}{\phi},
:::

for all $\ket{\psi}$ and $\ket{\phi}$, with equality if and only if $\ket{\psi}$ and $\ket{\phi}$ are linearly dependent, that is, if they lie in the same ray. To prove the theorem, we set

:::{math}
:label: eq-hilbert-29
\ket{\alpha} = \ket{\psi} + \lambda \ket{\phi},
:::

where $\lambda$ is a complex number, and we use {eq}`eq-hilbert-27` to write,

:::{math}
:label: eq-hilbert-30
\braket{\alpha}{\alpha} = \braket{\psi}{\psi} + \lambda \braket{\psi}{\phi} + \lambda^\cc \braket{\phi}{\psi} + |\lambda|^2 \braket{\phi}{\phi} \ge 0.
:::

This is true for all kets $\ket{\psi}$ and $\ket{\phi}$, and all complex numbers $\lambda$. Since the Schwarz inequality is obviously true if $\ket{\phi}=0$, we consider the case $\ket{\phi}\ne 0$, and we set

:::{math}
:label: eq-hilbert-31
\lambda = -{\braket{\phi}{\psi} \over \braket{\phi}{\phi}},
:::

so that {eq}`eq-hilbert-30` becomes

:::{math}
:label: eq-hilbert-32
\braket{\psi}{\psi} - {|\braket{\psi}{\phi}|^2 \over \braket{\phi}{\phi}} \ge 0,
:::

which is equivalent to {eq}`eq-hilbert-28`. Finally, it is easy to show that {eq}`eq-hilbert-32` becomes an equality if $\ket{\psi} = c\ket{\phi}$ for any complex number $c$, and conversely, if {eq}`eq-hilbert-32` is an equality, then $\braket{\alpha}{\alpha}=0$, which implies $\ket{\alpha}=0$, or $\ket{\psi} = -\lambda\ket{\phi}$. Therefore the equality holds in {eq}`eq-hilbert-28` if and only if $\ket{\psi}$ and $\ket{\phi}$ are linearly dependent.

(sec-hilbert-8)=

## Operators

Next we discuss *operators*. Usually in quantum mechanics we use only linear or antilinear operators. A linear operator $L$ and an antilinear operator $A$ are both mappings from the ket space into itself,

:::{math}
:label: eq-hilbert-33
L:\ES \to \ES, \qquad A:\ES \to \ES,
:::

but they have different properties when acting on linear combinations of kets. In particular, we have

:::{math}
:label: eq-hilbert-34a
\begin{aligned}
L(c_1\ket{\psi_1} + c_2\ket{\psi_2}) &= c_1 L\ket{\psi_1} + c_2 L\ket{\psi_2},
\end{aligned}
:::

:::{math}
:label: eq-hilbert-34b
\begin{aligned}
A(c_1\ket{\psi_1} + c_2\ket{\psi_2}) &= c_1^\cc A\ket{\psi_1} + c_2^\cc A\ket{\psi_2}.
\end{aligned}
:::

The only antilinear operator of interest in nonrelativistic quantum mechanics is the time-reversal operator, which we will discuss in {ref}`ch-timerev`. For now we ignore antilinear operators, and concentrate exclusively on linear operators.

Linear operators themselves can be multiplied by complex numbers and added, so they form a complex vector space in their own right. Linear operators can also be multiplied with one another; the product $AB$ means, apply $B$ first, then $A$ (to some ket). The multiplication is associative,

:::{math}
:label: eq-hilbert-35
A(BC) = (AB)C,
:::

for any linear operators $A$, $B$, $C$, but it is not commutative, that is

:::{math}
:label: eq-hilbert-36
AB \ne BA
:::

in general. The lack of commutativity of two linear operators $A$ and $B$ is measured by their *commutator*, defined by

:::{math}
:label: eq-hilbert-37
[A,B] = AB - BA.
:::

For reference, we also define the *anticommutator*,

:::{math}
:label: eq-hilbert-38
\{ A,B \} = AB+BA.
:::

We use the same curly bracket notation for the anticommutator as for the Poisson bracket in classical mechanics (see {ref}`sec-classmech-21`). It will usually be clear from context which is intended.

A linear operator $A$ may possess an inverse, $A^{-1}$; if it exists, it satisfies

:::{math}
:label: eq-hilbert-39
AA^{-1} = A^{-1}A = 1,
:::

where the identity operator is simply denoted by $1$. In finite-dimensional spaces, if $A^{-1}$ exists, then it is both a right- and a left-inverse; but in infinite dimensional spaces, some operators may possess a right-inverse but not a left-inverse, or vice versa. When all indicated inverses exist, we have

:::{math}
:label: eq-hilbert-40
(AB)^{-1} = B^{-1} A^{-1}.
:::

A more careful treatment of the subject of operator inverses in infinite-dimensional spaces must deal with domains of definition, boundedness and other matters. We may wish to gloss over these in a first course in practical quantum mechanics.

(sec-hilbert-9)=

## Rules for Commutators

The commutator $[\;,\;]$ obeys the following properties, which are trivial consequences of the definition {eq}`eq-hilbert-37`. In the following, capital letters are linear operators and lower case letters are complex numbers. First, the commutator is linear in both operands,

:::{math}
:label: eq-hilbert-41
\begin{aligned}
[c_1A_1+c_2A_2,B] &= c_1[A_1,B] + c_2[A_2,B], \\
[A,c_1B_1+c_2B_2] &= c_1[A,B_1] + c_2[A,B_2], \\

\end{aligned}
:::

it is antisymmetric,

:::{math}
:label: eq-hilbert-42
[A,B] = -[B,A],
:::

and it obeys the *Jacobi identity*,

:::{math}
:label: eq-hilbert-43
[A,[B,C]] +[B,[C,A]] + [C,[A,B]]=0.
:::

Any bracket operation $[\;,\;]$ defined on any vector space (not just spaces of linear operators) that satisfies properties {eq}`eq-hilbert-41`--{eq}`eq-hilbert-43` qualifies that vector space as a *Lie algebra*.

In addition, the commutator satisfies the following properties, sometimes referred to as the derivation property or Leibnitz rule:

:::{math}
:label: eq-hilbert-44
\begin{aligned}
[AB,C] &= A[B,C] + [A,C]B, \\
[A,BC] &= B[A,C] + [A,B]C. \\

\end{aligned}
:::

Calculations in quantum mechanics often require one to reduce complicated commutators into simpler ones that are known. Rules {eq}`eq-hilbert-44` are especially useful for this purpose. It is interesting that properties {eq}`eq-hilbert-41`--{eq}`eq-hilbert-44` are also valid for the Poisson bracket in classical mechanics [except that the ordering of the factors in {eq}`eq-hilbert-44`, which must be respected in quantum mechanics, is immaterial in classical mechanics]. See {ref}`sec-classmech-21`.

(sec-hilbert-10)=

## The Action of Operators on Bras

The operators we have introduced begin life as operators that act on kets, mapping them into other kets; but the definition of these operators is easily extended to allow them to act on bras, whereupon they produce other bras. If $\bra{\psi}$ is a bra and $A$ an operator, we denote the action of $A$ on $\bra{\psi}$ by $\bra{\psi}A$, with the bra to the left. That is, we think of $A$ as acting on kets to the right, but on bras to the left. The definition of $\bra{\psi}A$ is as follows. Since $\bra{\psi}A$ is supposed to be a new bra, it is specified by its action on an arbitrary ket, say, $\ket{\phi}$; the definition is given by writing

:::{math}
:label: eq-hilbert-45
(\bra{\psi}A) (\ket{\phi}) = \bra{\psi}(A\ket{\phi}).
:::

Since by this definition the ordering of the parentheses is immaterial, it is customary to drop them, and to write simply

:::{math}
:label: eq-hilbert-46
(\bra{\psi}A) (\ket{\phi}) = \matrixelement{\psi}{A}{\phi}.
:::

Thus, we can think of $A$ as acting either to the left or the right in the “matrix element” $\matrixelement{\psi}{A}{\phi}$.

(sec-hilbert-11)=

## The Outer Product

If $\ket{\alpha}$ and $\ket{\beta}$ are kets, then we can define a linear operator denoted by $\ketbra{\alpha}{\beta}$, whose action on an arbitrary ket $\ket{\psi}$ is given by

:::{math}
:label: eq-hilbert-47
(\ketbra{\alpha}{\beta}) \ket{\psi} = \ket{\alpha} \braket{\beta}{\psi},
:::

where the right-hand side is the product of the complex number $\braket{\beta}{\psi}$ times the ket $\ket{\alpha}$. The action of $\ketbra{\alpha}{\beta}$ on bras is given by

:::{math}
:label: eq-hilbert-48
\bra{\psi} (\ketbra{\alpha}{\beta}) = \braket{\psi}{\alpha} \bra{\beta}.
:::

This is not the definition of $\ketbra{\alpha}{\beta}$, which is given by {eq}`eq-hilbert-47`, rather it is a simple consequence of that definition. Its proof will be left as an exercise. The operator $\ketbra{\alpha}{\beta}$ can be viewed as the tensor product of the ket $\ket{\alpha}$ with the bra $\bra{\beta}$; this kind of product is similar to the dyadic product used in ordinary vector or tensor analysis. The operator $\ketbra{\alpha}{\beta}$ is called the *outer product* of $\ket{\alpha}$ and $\ket{\beta}$.

(sec-hilbert-12)=

## Bases and Orthonormal Bases; Resolutions of the Identity

As in any vector space, a *basis* is a set of linearly independent vectors that span the entire space, and the number of such vectors is the dimension of the space. This is a familiar concept in finite dimensions. In an infinite-dimensional space, we obviously need an infinite number of basis vectors, but is the basis countably or uncountably infinite? That is, can we label the basis vectors with a discrete index, or do we need continuous indices as well? As it turns out, it is one the mathematical properties of Hilbert spaces that they always possess a countable basis, that is, a set of linearly independent, normalizable vectors that span the space and can be indexed $n=1,2,3,\ldots$, or by some other such discrete indexing scheme. This does not mean that every basis we encounter will be labeled by a discrete index, only that such bases always exist. In fact, in practice in quantum mechanics we frequently encounter “bases” with continuous indices as well, but the basis vectors of the continuum are not normalizable and do not belong to Hilbert space. We will say more about these kinds of bases later, and for now proceed with the case of discrete bases, consisting of normalizable vectors. As an example, you may think of the harmonic oscillator wave functions $u_n(x)$ in one-dimensional quantum mechanics, which are normalizable, belong to Hilbert space, and form a discrete, complete set.

Let us denote a discrete basis in a ket space by $\{\ket{n}, n=1,\ldots\}$. We say the basis is *orthonormal* if

:::{math}
:label: eq-hilbert-49
\braket{n}{m} = \delta_{mn}.
:::

We usually use orthonormal bases in quantum mechanics, but non-orthonormal bases are useful sometimes as well (if more difficult to work with). In any basis, an arbitrary ket $\ket{\psi}$ can be represented as a linear combination of the basis vectors,

:::{math}
:label: eq-hilbert-50
\ket{\psi} = \sum_n c_n \ket{n} =\sum_n \ket{n} c_n,
:::

and if the basis is orthonormal, the expansion coefficients are given by

:::{math}
:label: eq-hilbert-51
c_n = \braket{n}{\psi}.
:::

Substituting this into {eq}`eq-hilbert-50`, we have

:::{math}
:label: eq-hilbert-52
\ket{\psi} = \sum_n \ket{n}\braket{n}{\psi} =\Bigl(\sum_n \ketbra{n}{n}\Bigr) \ket{\psi},
:::

or, since $\ket{\psi}$ is arbitrary,

:::{math}
:label: eq-hilbert-53
1 = \sum_n \ketbra{n}{n},
:::

where $1$ is the identity operator. This is the *resolution of the identity* associated with the orthonormal basis $\{ \ket{n} \}$.

Resolutions of the identity associated with bases with continuous indices will be discussed below.

(sec-hilbert-13)=

## Hermitian Conjugation

We have already defined Hermitian conjugation (denoted by the dagger $\dagger$) of bras and kets. We now define Hermitian conjugation of operators. If $A:\ES\to\ES$ is a linear operator, then $A^\hc:\ES\to\ES$ is another linear operator, defined by its action on an arbitrary ket $\ket{\psi}$ by

:::{math}
:label: eq-hilbert-54
A^\hc \ket{\psi} = (\bra{\psi}A)^\hc.
:::

We should note that $\bra{\psi}$ is an antilinear function of $\ket{\psi}$ (because of the dual correspondence), but when we do the (second) Hermitian conjugation indicated on the right hand side of {eq}`eq-hilbert-54`, the result is a linear function of $\ket{\psi}$. Thus, $A^\hc$ is a linear operator.

There are a number of immediate consequences of this definition, which we list here. The proofs are left as simple exercises.

:::{math}
:label: eq-hilbert-55
\matrixelement{\phi}{A^\hc}{\psi} = \matrixelement{\psi}{A}{\phi}^\cc,
:::

:::{math}
:label: eq-hilbert-56
(A^\hc)^\hc = A,
:::

:::{math}
:label: eq-hilbert-57
(c_1 A_1 + c_2 A_2)^\hc = c_1^\cc A_1^\hc + c_2^\cc A_2^\hc,
:::

:::{math}
:label: eq-hilbert-58
(AB)^\hc = B^\hc A^\hc,
:::

:::{math}
:label: eq-hilbert-59
(\ketbra{\alpha}{\beta})^\hc = \ketbra{\beta}{\alpha}.
:::

We have now defined the action of the Hermitian conjugate operation ${}^\hc$ on kets, bras, and operators. It is convenient also to define the action of the Hermitian conjugate on complex numbers as being identical with ordinary complex conjugation. With this understanding, we can state a general rule, which is illustrated in several various ways in the results above, which says that the Hermitian conjugate of a product of objects (kets, bras, operators, complex numbers) is given by reversing the order of the objects and replacing each by its Hermitian conjugate. The products involved can be either ordinary multiplication by scalars, operator products, or inner or outer (tensor) products. We only require that the original product be meaningful.

(sec-hilbert-14)=

## Hermitian, Anti-Hermitian and Unitary Operators

We say that an operator $A$ is *Hermitian* if it is equal to its own Hermitian conjugate,

:::{math}
:label: eq-hilbert-60
A^\hc = A.
:::

An equivalent definition is

:::{math}
:label: eq-hilbert-61
\matrixelement{\psi}{A}{\phi} = \matrixelement{\phi}{A}{\psi}^\cc,
:::

for all kets $\ket{\psi}$ and $\ket{\phi}$. Similarly, an operator is said to be *anti-Hermitian* if it satisfies

:::{math}
:label: eq-hilbert-62
A^\hc = -A.
:::

An arbitrary operator is in general neither Hermitian nor anti-Hermitian, but can always be uniquely decomposed into a sum of a Hermitian and an anti-Hermitian operator:

:::{math}
:label: eq-hilbert-63
A = {A+A^\hc \over 2} + {A-A^\hc \over 2}.
:::

If $A$ is Hermitian, then the matrix element $\matrixelement{\psi}{A}{\psi}$ is necessarily real, for all choices of $\ket{\psi}$, in accordance with {eq}`eq-hilbert-55`. We say that a Hermitian operator is *positive definite* if it satisfies

:::{math}
:label: eq-hilbert-64
\matrixelement{\psi}{A}{\psi} > 0,
:::

for all nonzero kets $\ket{\psi}$. Similarly, we say that $A$ is *nonnegative definite* if

:::{math}
:label: eq-hilbert-65
\matrixelement{\psi}{A}{\psi} \ge 0,
:::

for all kets $\ket{\psi}$.

We have not discussed eigenvalues yet, but a positive definite, Hermitian operator is one whose eigenvalues are all positive, while a nonnegative definite, Hermitian operator is one whose eigenvalues are all nonnegative.

A simple but important theorem is the following:

:::{admonition} Theorem
:class: theorem
:label: thm-hilbert-1

The product of two Hermitian operators is Hermitian if and only if they commute.
:::


 The (trivial) proof is left as an exercise.

An operator $U$ is *unitary* if

:::{math}
:label: eq-hilbert-66
UU^\hc = U^\hc U = 1,
:::

so that

:::{math}
:label: eq-hilbert-67
U^{-1} = U^\hc.
:::

The product of two unitary operators is always unitary.

(sec-hilbert-15)=

## Eigenvalues and Eigenkets; the Spectrum of an Operator

If $A$ is an operator acting on $\ES$ and there exists a nonzero ket $\ket{u}$ and complex number $a$ such that

:::{math}
:label: eq-hilbert-68
A\ket{u} = a\ket{u},
:::

then we say that $\ket{u}$ is an *eigenket* of $A$ and $a$ is a (right) *eigenvalue*. Similarly, if there exists a nonzero bra $\bra{v}$ and a complex number $b$ such that

:::{math}
:label: eq-hilbert-69
\bra{v}A = b\bra{v},
:::

then we say that $\bra{v}$ is an *eigenbra* of $A$ and $b$ is a (left) eigenvalue. In finite dimensions, every right eigenvalue is also a left eigenvalue, but in infinite dimensions this need not be true.

We define the *spectrum* of an operator as the set of its eigenvalues, seen as a subset of the complex plane. (If necessary, we can distinguish between a left and right spectrum.) In finite dimensions, this is a set of discrete points in the complex plane.

:::{figure} images/hilbert-fig01.png
:label: fig-hilbert-1
:width: 80%

Examples of spectra of operators. Part (a), the harmonic oscillator; part (b), the free particle; part (c), the hydrogen atom; part (d), a finite-dimensional unitary operator.
:::

Some examples of the spectra of familiar operators in quantum mechanics are illustrated in {ref}`fig-hilbert-1`. In part (a) of the figure we have the spectrum of the harmonic oscillator, whose eigenvalues $E_n = (n+\frac{1}{2})\hbar\omega$ are shown as spots on the real energy axis. This is an example of a *discrete spectrum*. Only real energies are physically meaningful, but we show the whole complex energy plane because in general eigenvalues of operators are complex. (We will see complex energies play a role in scattering and resonance theory later in the course.) In part (b) we have the spectrum of the free particle Hamiltonian $H=p^2/2m$. It consists of all real energies $E\ge0$, indicated by the thick line on the positive real axis. This is an example of the *continuous spectrum*. In part (c) we have the spectrum of the hydrogen atom. It consists of a discrete set of spots at negative energy, representing the bound states, an infinite number of which accumulate as we approach $E=0$. As with the free particle, there is a continuous spectrum above $E=0$. Altogether, the hydrogen atom has a *mixed spectrum* (discrete and continuous). Finally, in part (d) we have the spectrum of a unitary operator on a finite-dimensional space. Its eigenvalues are phase factors that lie on the unit circle in the complex plane.

:::{figure} images/hilbert-fig02.png
:label: fig-hilbert-2
:width: 80%

An operator $A$ acting on ket space $\ES$ has eigenspaces $\ES_n$, associated with its discrete eigenvalues $a_n$.
:::

:::{figure} images/hilbert-fig03.png
:label: fig-hilbert-3
:width: 80%

In the case of a Hermitian operator, the eigenspaces are orthogonal.
:::


In the case of the discrete spectrum, the set of kets $\ket{u}$ that satisfy {eq}`eq-hilbert-68` for a given eigenvalue $a$ forms a vector subspace of the ket space. This subspace is at least 1-dimensional, but the dimensionality may be higher (even infinite, on infinite-dimensional vector spaces). We will call this subspace the *eigenspace* of the operator corresponding to the given eigenvalue. If the eigenspace is 1-dimensional, then we say the eigenvalue is *nondegenerate*, otherwise, that it is *degenerate*. We refer to the dimensionality of the eigenspace as the *order* of the degeneracy. This is the same as the number of linearly independent eigenvectors of a given eigenvalue. We can imagine the eigenspaces of the discrete spectrum as illustrated in {ref}`fig-hilbert-2`, which shows the eigenspaces for a two-fold degenerate eigenvalue $a_1$ and a nondegenerate eigenvalue $a_2$ ($\dim\ES_1=2$, $\dim\ES_2=1$).

(sec-hilbert-16)=

## The Case of Hermitian Operators

In general, there is no simple relation between the eigenkets and eigenbras of an operator, even in finite dimensions. But if an operator $A$ is Hermitian, then there are a number of simplifications. We speak for the time being of the discrete spectrum.

First, the eigenvalue $a$ is real, so the spectrum in the complex eigenvalue plane is a subset of the real axis. To prove this we take $A\ket{u} = a\ket{u}$ and multiply on the left by $\bra{u}$, obtaining

:::{math}
:label: eq-hilbert-70
\matrixelement{u}{A}{u} = a\braket{u}{u}.
:::

Now taking the complex conjugate of this, the left-hand side goes into itself, while the right becomes $a^\cc \braket{u}{u}$. Thus we have

:::{math}
:label: eq-hilbert-71
(a-a^\cc)\braket{u}{u} =0.
:::

Since $\ket{u}\ne 0$, this implies $a=a^\cc$.

Second, if $A\ket{u}=a\ket{u}$, then $\bra{u}A = a\bra{u}$, so that the eigenbras are the Hermitian conjugates of the eigenkets, and the left and right eigenvalues are equal.

Third, any two eigenkets corresponding to distinct eigenvalues are orthogonal. We state this final property as a theorem:

:::{admonition} Theorem
:class: theorem
:label: thm-hilbert-2

The eigenspaces of a Hermitian operator corresponding to distinct eigenvalues are orthogonal. This means that any pair of vectors chosen from the two eigenspaces are orthogonal.
:::


To prove this, we let $A\ket{u} =a\ket{u}$ and $A\ket{u'} = a'\ket{u'}$ for two eigenkets $\ket{u}$ and $\ket{u'}$ and two eigenvalues $a$ and $a'$. Multiplying the first equation by $\bra{u'}$ and the second by $\bra{u}$, we obtain

:::{math}
:label: eq-hilbert-72
\begin{aligned}
\matrixelement{u'}{A}{u} &= a \braket{u'}{u}, \\
\matrixelement{u}{A}{u'} &= a' \braket{u}{u'}. \\

\end{aligned}
:::

Now taking the Hermitian conjugate of the second equation and subtracting from the first, we find

:::{math}
:label: eq-hilbert-73
(a-a')\braket{u}{u'} =0,
:::

showing that either $a=a'$ or else $\braket{u}{u'}=0$.

In view of this theorem, {ref}`fig-hilbert-3` gives a more accurate picture of the eigenspaces of a Hermitian operator than does {ref}`fig-hilbert-2`.

(sec-hilbert-17)=

## Completeness

In looking at Figs.~{ref}`fig-hilbert-2` and {ref}`fig-hilbert-3` we may imagine that the space in which the eigenspaces lie is three dimensional, so the two eigenspaces (of dimension 2 and 1) “fill up” the whole space. Do the eigenspaces of an operator always “fill up” the space upon which the operator acts? An operator that does this is said to be *complete*. The answer is no, not even in finite dimensions. For example, the matrix

:::{math}
:label: eq-hilbert-74
\begin{pmatrix}0 & 1 \\ 0 & 0\\\end{pmatrix}
:::

possesses only one eigenvector, namely,

:::{math}
:label: eq-hilbert-75
\begin{pmatrix}1 \\ 0 \\\end{pmatrix},
:::

so it has only a single one-dimensional eigenspace. The matrix {eq}`eq-hilbert-74` is not Hermitian.

On the other hand, in finite dimensions every Hermitian operator is complete. Thus, the sum of the dimensionalities of the eigenspaces is the dimension of the whole space. Since the eigenspaces are orthogonal, by choosing an orthonormal basis in each eigenspace we obtain an orthonormal eigenbasis for the whole space, that is, a set of orthonormal basis vectors that are also eigenvectors of the operator. This is a consequence of the standard methods taught in linear algebra courses for diagonalizing Hermitian matrices, which explicitly produce the orthonormal eigenbasis.

Notice that the orthonormal eigenbasis is not unique. First, if there is any degeneracy (any eigenspace with dimensionality $\ge2$), then obviously there are an infinite number of ways of choosing an orthonormal basis in that eigenspace. But even in a nondegenerate (one-dimensional) eigenspace, a normalized eigenvector is only determined to within a phase factor.

These nice properties of Hermitian operators are shared by a larger class of *normal* operators, which will be studied in a homework exercise. Occasionally in quantum mechanics we must deal with the eigenvectors of non-Hermitian operators and worry about their completeness properties. This happens, for example, in the theory of the Dirac equation.

(sec-hilbert-18)=

## The Direct Sum; Orthonormal Eigenbases

Suppose we have some vector space $\ES$, and suppose $\ES_1$ and $\ES_2$ are vector subspaces of $\ES$ that have no element in common except 0, such as the spaces we see in Figs.~{ref}`fig-hilbert-2` and {ref}`fig-hilbert-3`. Then we say that the *direct sum* of $\ES_1$ and $\ES_2$, denoted $\ES_1\oplus \ES_2$, is the set of vectors that can be formed by taking linear combinations of vectors in the two subspaces. That is,

:::{math}
:label: eq-hilbert-76
\ES_1 \oplus \ES_2 = \{ \ket{\psi_1} + \ket{\psi_2} \\text{\rm\ such that } \ket{\psi_1} \in \ES_1, \ket{\psi_2} \in \ES_2 \}.
:::

The direct sum is itself a vector subspace of $\ES$. One can also think of the direct sum as the span of the set of vectors formed when we throw together a basis in $\ES_1$ with a basis in $\ES_2$. Thus, we have

:::{math}
:label: eq-hilbert-77
\dim(\ES_1 \oplus \ES_2) = \dim \ES_1 + \dim\ES_2.
:::

This is not the most abstract definition of the direct sum, but it is the one we will use.

We can now express the completeness property in finite dimensions in terms of the direct sum. Let $A$ be an operator acting on a finite-dimensional space $\ES$. Let the eigenvalues of $A$ be $a_1,\ldots, a_N$, and let $\ES_n$ be the $n$-th eigenspace, that is,

:::{math}
:label: eq-hilbert-78
\ES_n = \{ \ket{u} \\text{\rm\ such that } A\ket{u} = a_n\ket{u} \}.
:::

Then $A$ is complete if

:::{math}
:label: eq-hilbert-79
\ES_1 \oplus \ES_2 \oplus \ldots \oplus \ES_N = \ES.
:::

In finite dimensions, any Hermitian $A$ is complete, and moreover it decomposes the original Hilbert space $\ES$ into a collection of orthogonal subspaces, the eigenspaces of the operator.

Let us choose an orthonormal basis, say $\ket{nr}$, in each of the subspaces $\ES_n$, where $r$ is an index labeling the orthonormal vectors in the subspace, so that $r=1,\ldots,\dim\ES_n$. This can always be done, in many ways. Then, since the various subspaces are themselves orthogonal, the collection of vectors $\ket{nr}$ for all $n$ and $r$ forms an orthonormal basis on the entire space $\ES$, so that

:::{math}
:label: eq-hilbert-80
\braket{nr}{n'r'} = \delta_{nn'} \, \delta_{rr'}.
:::

These kets are eigenkets of $A$,

:::{math}
:label: eq-hilbert-81
A\ket{nr} = a_n \ket{nr},
:::

that is, they constitute an orthonormal eigenbasis. Furthermore, we have the resolution of the identity,

:::{math}
:label: eq-hilbert-82
1 = \sum_{nr} \ketbra{nr}{nr},
:::

corresponding to the chosen orthonormal eigenbasis of the complete Hermitian operator $A$. Also, the operator itself can be written in terms of this eigenbasis,

:::{math}
:label: eq-hilbert-83
A=\sum_{nr} a_n \ketbra{nr}{nr}.
:::

This follows if we let both sides of this equation act on a basis vector $\ket{n'r'}$, whereupon the answers are the same. By linear superposition, the same applies to any vector. Thus, both sides are the same operator.

(sec-hilbert-19)=

## Spectral Properties in Infinite Dimensions

Here we make some remarks about infinite-dimensional ket spaces and illustrate the kinds of new phenomena that can arise.

In infinite dimensions, there exist Hermitian operators that are not complete. To cover this case, we define a complete Hermitian operator as an *observable*. This terminology is related to the physical interpretation of observables in quantum mechanics, as explained in {ref}`ch-postulat`. In practice we seldom deal with incomplete Hermitian operators in quantum mechanics.

We now use examples from one-dimensional wave mechanics to illustrate some phenomena that can occur in infinite dimensions. The Hilbert space of wave functions in one dimension consists of normalizable functions $\psi(x)$ with the scalar product,

:::{math}
:label: eq-hilbert-84
\braket{\psi}{\phi} = \int_{-\infty}^{+\infty} dx \, \psi^\cc(x) \phi(x).
:::

We will present four examples of operators and their spectral properties.

The first is the one-dimensional harmonic oscillator with Hamiltonian,

:::{math}
:label: eq-hilbert-85
H={p^2 \over 2m} + {m\omega^2 x^2\over2},
:::

which is a Hermitian operator. The energy eigenvalues are

:::{math}
:label: eq-hilbert-86
E_n = (n+\frac{1}{2})\hbar\omega,
:::

so that the spectrum consists of a discrete set of isolated points on the positive energy axis, as illustrated in {ref}`fig-hilbert-1`(a). The eigenfunctions $u_n(x)$ are normalizable (they belong to Hilbert space) and orthogonal for different values of the energy. Thus they can be normalized so that

:::{math}
:label: eq-hilbert-87
\braket{n}{m} = \int dx \, u_n^\cc(x) u_m(x) = \delta_{mn}.
:::

These eigenfunctions are nondegenerate and complete, so we have a resolution of the identity,

:::{math}
:label: eq-hilbert-88
1 = \sum_{n=0}^\infty \ketbra{n}{n}.
:::

Not all Hermitian operators on an infinite dimensional space have a discrete spectrum. As a second example, consider the momentum operator in one dimension, which is $\phat=-i\hbar\, d/dx$. (We put a hat on the operator, to distinguish it from the eigenvalue $p$.) The momentum is a Hermitian operator (see below). The eigenvalue-eigenfunction equation for this operator is

:::{math}
:label: eq-hilbert-89
\phat u_p(x)= pu_p(x) =-i\hbar\dod{u_p}{x},
:::

where $u_p(x)$ is the eigenfunction with eigenvalue $p$. This equation has a solution for all values, real and complex, of the parameter $p$,

:::{math}
:label: eq-hilbert-90
u_p(x) = c\, e^{ipx/\hbar},
:::

where $c$ is a constant. If $p$ has a nonzero imaginary part, then $u_p(x)$ diverges exponentially as $x\to\infty$ or $x\to -\infty$, so the “eigenfunction” is rather badly behaved. It is certainly not normalizable in this case. But even if $p$ is purely real, the function $u_p(x)$ is still not normalizable, so it does not represent a physically allowable state (a vector of Hilbert space). The momentum operator $\phat$ does not have any eigenvectors that belong to Hilbert space, much less a basis.

One way to handle this case, which provides a kind of generalization of the nice situation we find in finite dimensions, is to regard every real number $p$ as an eigenvalue of $\phat$, which means that the spectrum of $p$ is the entire real axis (in the complex $p$-plane). See {ref}`fig-hilbert-1`(b) for an illustration of the spectrum of the free particle Hamiltonian, which is the portion $E\ge0$ of the real axis. Recall that in finite dimensions a Hermitian operator has only real eigenvalues. This is an example of the *continuous spectrum*. Also, the eigenfunctions that result in this case are orthonormal and complete in a certain sense, but as noted they do not belong to Hilbert space. We obtain an orthonormal basis, but it consists of vectors that lie outside Hilbert space.

We adopt a normalization of the eigenfunctions (that is, we choose the constant $c$ in {eq}`eq-hilbert-90` so that

:::{math}
:label: eq-hilbert-91
u_p(x) = {e^{ipx/\hbar} \over \sqrt{2\pi\hbar}},
:::

because this implies a convenient normalization relation,

:::{math}
:label: eq-hilbert-92
\braket{p_0}{p_1} = \int dx\, u_{p_0}^\cc(x)\, u_{p_1}(x) = \int {dx \over 2\pi\hbar} \, e^{i(p_1-p_0)x/\hbar} = \delta(p_0-p_1),
:::

where we write the function $u_p(x)$ in ket language as $\ket{p}$ (giving only the eigenvalue). The eigenfunctions $u_p(x)$ of the continuous spectrum are orthonormal only in the $\delta$-function sense. They are also complete, in the sense that an arbitrary wave function $\psi(x)$ can be expanded as a linear combination of them, but since they are indexed by a continuous variable, the linear combination is an integral, not a sum. That is, given $\psi(x)$, we can find expansion coefficients $\phi(p)$ such that

:::{math}
:label: eq-hilbert-93
\psi(x) = \int_{-\infty}^\infty dp\, \phi(p)\, u_p(x) = \int_{-\infty}^\infty {dp \over \sqrt {2\pi\hbar}} e^{ipx/\hbar} \, \phi(p).
:::

We know this because {eq}`eq-hilbert-93` is essentially a Fourier transform, whose inverse is given by

:::{math}
:label: eq-hilbert-94
\phi(p) =  \int {dx \over\sqrt{2\pi\hbar}} \, e^{-ipx/\hbar} \, \psi(x) = \int dx \, u_p^\cc(x) \, \psi(x) = \braket{p}{\psi}.
:::

We see that the “momentum space wave function” $\phi(p)$ is otherwise the scalar product $\braket{p}{\psi}$.

Another example of an operator with a continuous spectrum is the position operator $\hat x$ (again using hats to denote an operator). This operator acting on wave functions means, multiply by $x$. If we denote the eigenfunction of this operator with eigenvalue $x_0$ by $f_{x_0}(x)$, then the eigenvalue equation is

:::{math}
:label: eq-hilbert-95
\hat x f_{x_0}(x) = xf_{x_0}(x) = x_0f_{x_0}(x),
:::

or,

:::{math}
:label: eq-hilbert-96
(x-x_0)f_{x_0}(x)=0.
:::

This implies either $x=x_0$ or $f_{x_0}(x)=0$, so $f_{x_0}(x)$ is a “function” that is zero everywhere except possibly at $x_0$. We interpret this situation in terms of the Dirac delta function, by writing the solution as

:::{math}
:label: eq-hilbert-97
f_{x_0}(x) = \delta(x-x_0).
:::

Again, the spectrum is continuous and occupies the entire real axis; again, the “eigenfunctions” are of infinite norm and obey the continuum orthonormality condition,

:::{math}
:label: eq-hilbert-98
\braket{x_0}{x_1} = \int dx \, \delta(x-x_0) \delta(x-x_1) = \delta(x_0-x_1),
:::

where we write the function $f_{x_0}(x)$ in ket language as $\ket{x_0}$ (giving only the eigenvalue). In addition, we have the identity,

:::{math}
:label: eq-hilbert-99
\psi(x_0) = \int dx\, \delta(x-x_0) \, \psi(x) = \int dx\,f_{x_0}^\cc(x)\, \psi(x) = \braket{x_0}{\psi}.
:::

We see that the wave function $\psi(x_0)$ is otherwise the scalar product $\braket{x_0}{\psi}$. Substituting this back into {eq}`eq-hilbert-99` and using {eq}`eq-hilbert-98`, we have

:::{math}
:label: eq-hilbert-100
\braket{x_0}{\psi} = \int dx\, \braket{x_0}{x} \braket{x}{\psi},
:::

or, since $x_0$ is arbitrary,

:::{math}
:label: eq-hilbert-101
\ket{\psi} = \int dx \, \ket{x} \braket{x}{\psi}.
:::

Finally, since $\ket{\psi}$ is arbitrary, we can strip it off, leaving

:::{math}
:label: eq-hilbert-102
1 = \int dx \, \ketbra{x}{x},
:::

the resolution of the identity in the case of the continuous eigenbasis of the position operator.

We can also get the resolution of the identity in the momentum basis. Since $\psi(x) = \braket{x}{\psi}$ for any $\psi$, we have $u_p(x) =\braket{x}{p}$. Substituting these and {eq}`eq-hilbert-94` into {eq}`eq-hilbert-93`, we have

:::{math}
:label: eq-hilbert-103
\braket{x}{\psi} = \int dp\, \braket{x}{p}\braket{p}{\psi},
:::

or, stripping off both $\bra{x}$ on the left and $\ket{\psi}$ on the right,

:::{math}
:label: eq-hilbert-104
1 =\int dp\, \ketbra{p}{p}.
:::

Equations {eq}`eq-hilbert-102` and {eq}`eq-hilbert-104` illustrate resolutions of the identity in the case of the continuous spectrum.

:::{figure} images/hilbert-fig04.png
:label: fig-hilbert-4
:width: 80%

A potential in 1-dimension with both bound and unbound eigenstates.
:::

For a final example, let us consider the 1-dimensional potential illustrated in {ref}`fig-hilbert-4`, which has a well followed on the right by an infinitely high barrier. The purpose of the barrier is simply to make the unbound energy eigenfunctions nondegenerate, which simplifies the following discussion. In a potential such as this, we expect there to be some number of bound eigenfunctions $u_n(x)$ in the potential well, which have negative energies $E_n<0$. These eigenfunctions are normalizable, because the wave functions die off exponentially outside the well, and we can normalize them according to $\braket{n}{m}=\delta_{nm}$, as with the discrete spectra discussed above. But there will also be unbound eigenfunctions $u_E(x)$ corresponding to any energy $E\ge0$; these eigenfunctions become free particle wave functions at large negative $x$, and therefore have infinite norm. We normalize them according to $\braket{E}{E'} = \delta(E-E')$. Finally, all bound states are orthogonal to all continuum states, $\braket{n}{E}=0$. Thus, the completeness relation in this case has the form,

:::{math}
:label: eq-hilbert-105
1 = \sum_n \ketbra{n}{n} + \int_0^\infty dE \, \ketbra{E}{E}.
:::

In this case we have an example of a *mixed spectrum*, with some discrete and some continuous eigenvalues. The spectrum consists of a discrete set of points $E_n$ on the negative energy axis, plus the entire positive energy axis $E\ge0$.

More complicated kinds of spectra also occur. It is possible to have discrete states imbedded in the continuum, not in real physical problems but in approximations to them, in which certain interactions are switched off. When all the physics is taken into account, such discrete states typically move off the real axis, and become resonances with a finite lifetime. Examples of this occurs in the autoionizing states of helium, or in the radiative decay of excited atomic states. See {ref}`ch-nlw`. It is also possible to have a discrete spectrum in which the eigenvalues are not isolated, as in the random potentials that occur in the theory of Anderson localization, an important topic in solid state physics.

(sec-hilbert-20)=

## Generalizations about Spectra, Eigenspaces and Eigenbases

On a finite-dimensional Hilbert space, all Hermitian operators have a discrete spectrum (and they are moreover complete). The continuous and more complicated types of spectra arise only in the infinite dimensional case.

In the infinite dimensional case, each eigenvalue of the discrete spectrum corresponds to a definite eigenspace, a subspace of the Hilbert space consisting of normalizable eigenvectors of the Hermitian operator in question. If such an eigenspace is finite dimensional, then it possesses a finite, discrete basis of normalizable eigenvectors, as does any finite-dimensional Hilbert space. If an eigenspace of the discrete spectrum is infinite dimensional, then it is an infinite dimensional subspace of a Hilbert space and is therefore an infinite dimensional Hilbert space in its own right. This means that it is possible to choose a discrete basis of normalizable vectors that span this space, but that it may be convenient in practice to choose other types of bases, such as a continuous basis, consisting of unnormalizable vectors outside Hilbert space, or a mixed basis, or other possibilities.

An example of an infinite dimensional eigenspace of an operator with a discrete spectrum is given by the parity operator acting on wave functions $\psi(x)$ in one dimension. The two eigenspaces consist of wave functions that are even and odd under $x\to-x$, corresponding to the eigenvalues $+1$ and $-1$ of the parity operator, and both are infinite dimensional.

In the continuous spectrum, there is no subspace of the Hilbert space corresponding to a given eigenvalue. For example, in the case of the free particle in one dimension with Hamiltonian $H=p^2/2m$, for a given $E>0$ there are two linearly independent eigenfunctions, $e^{ikx}$ and $e^{-ikx}$, where $E=\hbar^2k^2/2m$. But these eigenfunctions are not normalizable, and do not belong to Hilbert space. Since there is no linear combination of these eigenfunctions that is normalizable, they do not specify a subspace of Hilbert space. On the other hand, any interval in the continuous spectrum does correspond to a subspace of the Hilbert space. This subspace consists of normalizable vectors that can be represented as linear combinations of the unnormalizable eigenvectors whose eigenvalues lie in the given interval.

For example, let $I=[p_0,p_1]$ be an interval of the momentum axis. Then normalizable wave functions $\psi(x)$ whose Fourier transform $\phi(p)$ vanishes outside the interval $I$ form a subspace of the Hilbert space of normalizable wave functions $\psi(x)$.

Concepts like this are familiar in electronics. A circuit that passes a signal in a certain frequency range $[\omega_0,\omega_1]$ while rejecting frequency components outside that range is analogous to a projection operator in quantum mechanics that projects onto a certain interval of the momentum axis $[p_0,p_1]$. The main difference is that one works in the time domain and the other in the spatial domain [when acting on wave functions $\psi(x)$].

The concept of a subspace corresponding to an interval of the continuous spectrum plays a role in the measurement postulates of quantum mechanics, as we will see in {ref}`ch-postulat`.

(sec-hilbert-21)=

## Proving of Hermiticity of the Momentum

To show that the momentum operator $\hat p$ is Hermitian on the Hilbert space of wave functions $\psi(x)$ with scalar product {eq}`eq-hilbert-84`, we appeal to the definition of Hermiticity in the form {eq}`eq-hilbert-61`. Letting $\psi(x)$ and $\phi(x)$ be two wave functions, we have

:::{math}
:label: eq-hilbert-106
\matrixelement{\psi}{\hat p}{\phi} = \int dx \, \psi^\cc \left(-i\hbar \frac{\partial \phi}{\partial x} \right) = \int dx \, \left(-i\hbar \pop{}{x}\right) (\psi^\cc \phi) + \int dx \, \left(i\hbar \frac{\partial \psi^\cc}{\partial x} \right) \phi,
:::

by integration by parts. The first integral vanishes if $\psi$ and $\phi$ go to zero as $x \to \pm\infty$, something we normally expect for normalizable wave functions (but see \secrhilbert-29). The final integral is

:::{math}
:label: eq-hilbert-107
\left[ \int dx \, \phi^\cc \left( -i\hbar \frac{\partial \psi}{\partial x}\right)\right]^\cc = \matrixelement{\phi}{\phat}{\psi}^\cc,
:::

which completes the proof. A similar proof can be given for Hamiltonians of the form $H=p^2/2m + V(x)$. More simply, once we know that $\xhat$ and $\phat$ are Hermitian, we can use the general rules presented in these notes (for example, {eq}`eq-hilbert-58` and \secrhilbert-25)) to conclude that the sum of any real function of $\xhat$ and any real function of $\phat$ is Hermitian.

(sec-hilbert-22)=

## Orthonormality and Completeness in the General (Degenerate) Case

We return now to the general case of a complete Hermitian operator $A$ (an observable) acting on an infinite-dimensional Hilbert space. In general, the spectrum consists of a discrete part, with eigenvalues $a_n$, and a continuous part, with eigenvalues $a(\nu)$ that are functions of some continuous variable $\nu$. (We could choose $\nu=a$, but sometimes it is convenient to use another continuous parameter upon which the eigenvalue depends. For example, we may wish to use the momentum $p$ instead of the energy $E$ to parameterize continuum energy eigenvalues and eigenfunctions.) In addition, we must in general introduce another index $r$ to resolve degeneracies in degenerate subspaces; for simplicity we will assume that $r$ is a discrete index, although in some problems this would be continuous, too. Then the orthonormality conditions have the form,

:::{math}
\begin{aligned}
\braket{nr}{n'r'} &= \delta_{nn'} \, \delta_{rr'},
\end{aligned}
:::

:::{math}
\begin{aligned}
\braket{nr}{\nu r'} &= 0,
\end{aligned}
:::

:::{math}
:label: eq-hilbert-108
\begin{aligned}
\braket{\nu r}{\nu' r'} &= \delta(\nu-\nu') \, \delta_{rr'},
\end{aligned}
:::

and the completeness relation has the form,

:::{math}
:label: eq-hilbert-109
1 = \sum_{nr} \ketbra{nr}{nr} + \int d\nu \, \sum_r \ketbra{\nu r}{\nu r}.
:::

As a specific example of these relations, consider the hydrogen atom in the electrostatic model, in which we neglect the electron spin. The bound state wave functions are $\psi_{n\ell m}(\rvec)$ in the usual notation, which we write in ket language as $\ket{n\ell m}$. We normalize these so that $\braket{n\ell m}{n'\ell'm'} =\delta_{nn' }\,\delta_{\ell\ell' }\,\delta_{mm'}$. In addition, there are unbound (and unnormalizable) eigenfunctions of energy $E\ge0$, which we write in ket language as $\ket{E\ell m}$. We normalize these so that $\braket{ E\ell m}{ E'\ell' m'} =\delta(E-E' )\delta_{\ell\ell' }\,\delta_{mm'}$. Also, the bound states are orthogonal to the unbound states, $\braket{n\ell m}{ E\ell' m'}=0$. Then the completeness relation has the form,

:::{math}
:label: eq-hilbert-110
1 = \sum_{n\ell m} \ketbra{n\ell m}{n \ell m} + \int_0^\infty dE \sum_{\ell m} \ketbra{E \ell m}{E\ell m}.
:::

The generalized orthonormality and completeness relations we have just presented are examples of an important theorem, which we now quote:

:::{admonition} Theorem
:class: theorem
:label: thm-hilbert-3

An observable always possesses an orthonormal eigenbasis.
:::


 This eigenbasis must include states of infinite norm, if the observable possesses a continuous spectrum.

(sec-hilbert-23)=

## Simultaneous Eigenbases of Commuting Observables

Next we turn to an important theorem, applications of which will occur many times in this course:

:::{admonition} Theorem
:class: theorem
:label: thm-hilbert-4

Two observables possess a simultaneous eigenbasis if and only if they commute. This eigenbasis may be chosen to be orthonormal. By extension, a collection of observables possesses a simultaneous eigenbasis if and only if they commute.
:::


For simplicity we will work on a finite-dimensional Hilbert space $\ES$. We begin with the case of two observables. In the first part of the proof, we assume we have two Hermitian operators $A$, $B$ that commute. We wish to prove that they possess a simultaneous eigenbasis.

Consider the $n$-th eigenspace $\ES_n$ of the operator $A$, and let $\ket{u}$ be a eigenket in this eigenspace, so that

:::{math}
:label: eq-hilbert-111
A\ket{u} = a_n\ket{u}.
:::

Then by multiplying by $B$ and using the fact that $AB=BA$, we easily conclude that

:::{math}
:label: eq-hilbert-112
A(B\ket{u}) = a_n (B\ket{u}),
:::

in which we use parentheses to emphasize the fact that the ket $B\ket{u}$ is also an eigenket of $A$ with the same eigenvalue, $a_n$. Note the possibility that $B\ket{u}$ could vanish, which does not, however, change any of the following argument. We see that if any ket $\ket{u}$ belongs to the subspace $\ES_n$, then so does the ket $B\ket{u}$.

To complete the proof we need the concept of the *restriction* of an operator to a subspace. In general, it is only meaningful to talk about the restriction of an operator to some subspace of a larger space upon which the operator acts if it should happen that the operator maps any vector of the given subspace into another vector of the same subspace. In this case, we say that the subspace is *invariant* under the action of the operator.

In the present example, both operators $A$ and $B$ leave the subspace $\ES_n$ invariant. As for $A$, this follows from {eq}`eq-hilbert-111`, which is in effect the definition of $\ES_n$. As for $B$, this follows from {eq}`eq-hilbert-112`. Let us denote the restriction of $A$ and $B$ to the subspace $\ES_n$ by $\bar A$ and $\bar B$, respectively. Then, according to {eq}`eq-hilbert-111`, $\bar A$ is a multiple of the identity, $\bar A=a_n \bar I$, where $\bar I$ stands for the identity operator acting on the subspace. The operator $\bar B$ cannot be expressed so simply, but it is a Hermitian operator, since $B$ was Hermitian on the larger space $\ES$. Since we are assuming that $\ES$ is finite-dimensional, so is $\ES_n$, and therefore $\bar B$ is complete on $\ES_n$. Therefore $\bar B$ possesses an orthonormal eigenbasis in $\ES_n$, say,

:::{math}
:label: eq-hilbert-113
\bar B \ket{nr} = b_{nr} \ket{nr},
:::

where $r=1,\ldots,\dim\ES_n$. Here $n$ is considered fixed, and if there are any degeneracies of $\bar B$, they are indicated by repetitions of the eigenvalues $b_{nr}$ for different values of $r$.

If we now construct the bases $\ket{nr}$ in a similar manner for each value of $n$, then we obtain a simultaneous, orthonormal eigenbasis for both $A$ and $B$ on the whole space $\ES$. Notice that there may be degeneracies of $B$ that cross the eigenspaces of $A$, that is, there may be repetitions in the values $b_{nr}$ for different values of $n$.

To prove the converse of Theorem~{ref}`thm-hilbert-4`, we assume that $A$ and $B$ possess a simultaneous eigenbasis. We sequence the kets of this eigenbasis according to some index $s$, and write

:::{math}
:label: eq-hilbert-114
A\ket{s} = a_s \ket{s}, \qquad B\ket{s} = b_s \ket{s}.
:::

In these formulas, we do not assume that the eigenvalues $a_s$ or $b_s$ are distinct for different values of $s$; degeneracies are indicated by repetitions of the values $a_s$ or $b_s$ for different values of $s$. Now from {eq}`eq-hilbert-114` it follows immediately that

:::{math}
:label: eq-hilbert-115
AB\ket{s} = a_s b_s \ket{s} = BA\ket{s},
:::

or,

:::{math}
:label: eq-hilbert-116
[A,B]\ket{s} =0.
:::

But since the kets $\ket{s}$ form a basis, {eq}`eq-hilbert-116` implies $[A,B]=0$. QED. (The extension of Theorem~{ref}`thm-hilbert-4` will be left as an exercise.)

An important corollary of Theorem~{ref}`thm-hilbert-4` occurs when some eigenvalue $a_n$ of $A$ is nondegenerate, so that $\ES_n$ is 1-dimensional. In that case, all kets in $\ES_n$ are proportional to any nonzero ket in $\ES_n$. Thus, if we let $\ket{n}$ be some standard, normalized eigenket of $A$ with eigenvalue $a_n$, then {eq}`eq-hilbert-112` tells us that $B\ket{n}$ must be proportional to $\ket{n}$, say,

:::{math}
:label: eq-hilbert-117
B\ket{n} = b\ket{n},
:::

for some number $b$. We see that $b$ is an eigenvalue of $B$, and $\ket{n}$ is an eigenket, although the theorem does not tell us the value of $b$. The number $b$ must be real, since $B$ is Hermitian. We summarize these facts by another theorem.

:::{admonition} Theorem
:class: theorem
:label: thm-hilbert-5

If two observables $A$ and $B$ commute, $[A,B]=0$, then any nondegenerate eigenket of $A$ is also an eigenket of $B$. (It may be a degenerate eigenket of $B$.) By extension, if $A_1, \ldots, A_n$ are observables that commute with each other and with another observable $B$, then any nondegenerate, simultaneous eigenket of $A_1,\ldots,A_n$ is also an eigenket of $B$.
:::


 The proof of the extension will be left as an exercise.

As an example of this theorem, consider a Hamiltonian that commutes with parity, $[H,\pi]=0$. According to the theorem, every nondegenerate eigenstate of the Hamiltonian is necessarily a state of definite parity (even or odd), that is, it is an eigenstate of parity. Recall that in the one-dimensional harmonic oscillator, the energy eigenstate for $n=even$ are even under parity, while those for $n=odd$ are odd.

(sec-hilbert-24)=

## Projection Operators

We turn now to the subject of projection operators. We say that an operator $P$ is a *projection operator* or a *projector* if it is an observable that satisfies

:::{math}
:label: eq-hilbert-118
P^2 = P.
:::

(On account of this equation, we say that $P$ is *idempotent*, from Latin *idem* = `same,' and *potens* = `powerful.') It follows immediately from this definition that the eigenvalues of $P$ are either 0 or 1, for if we write

:::{math}
:label: eq-hilbert-119
P\ket{p} = p\ket{p},
:::

then by {eq}`eq-hilbert-118` we have

:::{math}
:label: eq-hilbert-120
P^2 \ket{p} = P\ket{p} = p^2 \ket{p} = p\ket{p},
:::

or,

:::{math}
:label: eq-hilbert-121
(p^2-p)\ket{p}=0.
:::

Thus, either $p^2=p$ or $\ket{p}=0$; we exclude the latter possibility, since eigenkets are supposed to be nonzero, and therefore conclude that either $p=0$ or $p=1$. Therefore $P$ breaks the Hilbert space $\ES$ into two orthogonal subspaces,

:::{math}
:label: eq-hilbert-122
\ES = \ES_0 \oplus \ES_1,
:::

such that $P$ annihilates any vector in $\ES_0$, and leaves any vector in $\ES_1$ invariant. We say that $\ES_1$ is the space upon which $P$ *projects*.

Projection operators arise naturally in the eigenvalue problem for an observable $A$. For simplicity, assume that $A$ has a discrete spectrum, so that we can write

:::{math}
:label: eq-hilbert-123
A\ket{nr} = a_n \ket{nr},
:::

where $\ket{nr}$ is an orthonormal eigenbasis of $A$, with an arbitrarily chosen orthonormal basis $r=1,\ldots,\dim \ES_n$ in each eigenspace $\ES_n$. We then define

:::{math}
:label: eq-hilbert-124
P_n = \sum_r \ketbra{nr}{nr}.
:::

It is left as an exercise to show that the operator $P_n$ actually is a projector, and that it projects onto eigenspace $\ES_n$ of $A$. The set of projectors $P_n$ for different $n$ also satisfy

:::{math}
:label: eq-hilbert-125
P_n P_m = P_m P_n = \delta_{nm} \, P_n.
:::

As we say, the projectors $P_n$ form an orthogonal set.

It follows immediately from the definition {eq}`eq-hilbert-124` and the resolution of the identity {eq}`eq-hilbert-82` that

:::{math}
:label: eq-hilbert-126
\sum_n P_n =1,
:::

which is yet another way of writing the completeness relation for $A$.

One can also express the operator $A$ itself in terms of its projectors. We simply let $A$ act on both sides of the resolution of the identity, {eq}`eq-hilbert-82`, and use {eq}`eq-hilbert-123` and {eq}`eq-hilbert-124`. The result is

:::{math}
:label: eq-hilbert-127
A = \sum_n a_n P_n.
:::

In the case of the continuous spectrum, a projector can be associated with an interval $I=[\nu_1,\nu_2]$ of the parameter describing the continuous spectrum. For if we normalize the eigenkets of some operator $A$ as in {eq}`eq-hilbert-108`, then it is easy to show that the operator

:::{math}
:label: eq-hilbert-128
P_I = \int_{\nu_1}^{\nu_2} d\nu \, \sum_r \ketbra{\nu r}{\nu r}
:::

is a projector, and that the projectors for two intervals $I$ and $I'$ are orthogonal if and only if $I$ and $I'$ do not intersect.

The use of projection operators is generally preferable to the use of eigenvectors, because the latter are not unique. Even when nondegenerate and normalized, an eigenvector is subject to multiplication by an arbitrary phase factor, and in the case of degeneracies, an orthonormal basis can be chosen in the degenerate eigenspace in many ways. However, it is easy to show that the projector defined in {eq}`eq-hilbert-124` is invariant under all such redefinitions, as should be obvious from the geometrical fact that $P_n$ projects onto $\ES_n$. Also, in the continuous spectrum there are no eigenvectors that belong to Hilbert space (which means that they are normalizable and hence physical), but the projection operators {eq}`eq-hilbert-128` are always defined and well behaved.

(sec-hilbert-25)=

## A Function of an Observable

The concept of a *function* of an observable arises in many places. We begin with the case of the discrete spectrum. If $A$ is an observable with discrete eigenvalues $a_1,a_2,\ldots$ and corresponding projectors $P_1,P_2,\ldots$, we define $f(A)$ by

:::{math}
:label: eq-hilbert-129
f(A) = \sum_n f(a_n) P_n.
:::

It is easy to show that when $f$ is a polynomial or power series, $f(A)$ is the same as the obvious polynomial or power series in the operator $A$; but {eq}`eq-hilbert-129` defines a function of an observable in more general cases, such as the important cases $f(x) = 1/(x-x_0)$, or even $f(x)=\delta(x-x_0)$. When $A$ has a continuous spectrum, we can no longer express $f(A)$ in terms of projectors, but we can write it in terms of the complete basis of eigenkets, in the notation of {eq}`eq-hilbert-109`. In this case we have

:::{math}
:label: eq-hilbert-130
f(A) = \sum_{nr} f(a_n) \ketbra{nr}{nr} + \int d\nu \sum_r f\bigl(a(\nu)\bigr) \ketbra{\nu r}{\nu r}.
:::

(sec-hilbert-26)=

## Number Terminology

In quantum mechanics we often have to draw the distinction between an operator and its eigenvalues, or an operator (a quantum observable) and its classical counterpart, which is number. Some terminology due to Dirac is useful for such purposes. Dirac refers to an ordinary (real or complex) number as a “$c$-number,” while he calls an operator a “$q$-number.” We will often use this terminology.

(sec-hilbert-27)=

## Operators and Kets versus Matrices and Vectors

We now consider the relation between abstract kets, bras, and operators and the vectors and matrices of numbers that are used to represent those abstract objects. Consider, for example, the eigenvalue problem $A\ket{u}=a_n\ket{u}$ for a Hermitian operator $A$. To convert this into numerical form, we simply choose an arbitrary orthonormal basis $\{ \ket{k} \}$, $\braket{k}{\ell} = \delta_{k\ell}$, and insert a resolution of the identity $\sum \ketbra{\ell}{\ell}$ before the ket $\ket{u}$ on both sides. We then multiply from the left with bra $\bra{k}$, to obtain

:::{math}
:label: eq-hilbert-131
\sum_\ell \matrixelement{k}{A}{\ell} \braket{\ell}{u} = c_n \braket{k}{u}.
:::

Thus, with

:::{math}
:label: eq-hilbert-132
A_{k\ell} = \matrixelement{k}{A}{\ell},  \qquad u_k = \braket{k}{u},
:::

we have

:::{math}
:label: eq-hilbert-133
\sum_\ell A_{k\ell} \, u_\ell = a_n u_k.
:::

The matrix elements $A_{k\ell}$ form a Hermitian matrix,

:::{math}
:label: eq-hilbert-134
A_{k\ell} = A^\cc_{\ell k},
:::

and the eigenvalue problem becomes that of determining the eigenvalues and eigenvectors of a Hermitian matrix. Now the eigenvector $u_k$, as a column vector of numbers, contains the components of the eigenket $\ket{u}$ with respect to the chosen basis. Of course, if the Hilbert space is infinite-dimensional, then the matrix $A_{k\ell}$ is also infinite-dimensional. In practice, one usually truncates the infinite-dimensional matrix at some finite size, in order to carry out numerical calculations. One can hope that if the answers seem to converge as the size of the truncation is increased, then one will obtain good approximations to the true answers (this is the usual procedure).

The above is for a discrete basis. Sometimes we are also interested in a continuous basis, for example, the eigenbasis $\ket{x}$ of the operator $\hat x$. Again working with the eigenvalue problem $A\ket{u}=a_n\ket{u}$, we can insert a resolution of the identity $\int dx' \, \ketbra{x'}{x'}$ before $\ket{u}$ on both sides, and multiply from the left by $\bra{x}$. Then using the orthogonality relation {eq}`eq-hilbert-98`, we obtain

:::{math}
:label: eq-hilbert-135
\int dx' \, \matrixelement{x}{A}{x'} \braket{x'}{u} = a_n \braket{x}{u},
:::

or,

:::{math}
:label: eq-hilbert-136
\int dx' \, A(x,x') u(x') = a_n u(x),
:::

where

:::{math}
:label: eq-hilbert-137
A(x,x') = \matrixelement{x}{A}{x'}, \qquad u(x) = \braket{x}{u}.
:::

We see that the “matrix element” of an operator with respect to a continuous basis is nothing but the kernel of the integral transform that represents the action of that operator in the given basis. (The kernel of an integral transform such as {eq}`eq-hilbert-136` is the function $A(x,x')$ that appears under the integral.)

(sec-hilbert-28)=

## Traces

The trace of a matrix is defined as the sum of the diagonal elements of the matrix. Likewise, we define the trace of an operator $A$ acting on a Hilbert space as the sum of the diagonal matrix elements of $A$ with respect to any orthonormal basis. Thus, in a discrete basis $\{\ket{k}\}$ we have

:::{math}
:label: eq-hilbert-138
\tr A = \sum_k \matrixelement{k}{A}{k}.
:::

One can easily show that it does not matter which basis is chosen; the trace is a property of the operator alone. One can also use a continuous basis to compute the trace (replacing sums by integrals). The operator in {eq}`eq-hilbert-138` need not be Hermitian, but if it is, then the trace is equal to the sum of the eigenvalues, each weighted by the order of the degeneracy,

:::{math}
:label: eq-hilbert-139
\tr A = \sum_n g_n a_n,
:::

where $g_n$ is the order of the degeneracy of $a_n$. This is easily proven by choosing the basis in {eq}`eq-hilbert-138` to be the orthonormal eigenbasis of $A$. But if $A$ has a continuous range of eigenvalues, then the result diverges (or is not defined). Even if the spectrum of $A$ is discrete, the sum {eq}`eq-hilbert-139` need not converge.

The trace of a product of operators is invariant under a cyclic permutation of the product. For example, in the case of three operators, we have

:::{math}
:label: eq-hilbert-140
\tr (ABC) = \tr (BCA) = \tr (CAB).
:::

This property is easily proven. Another simple identity is

:::{math}
:label: eq-hilbert-141
\tr \ketbra{\alpha}{\beta} = \braket{\beta}{\alpha}.
:::

If $A$ and $B$ are operators, we are often interested in a kind of “scalar product” of $A$ with $B$, especially when we are expressing some operators as linear combinations of other operators (the Pauli matrices, for example). The most useful definition of a scalar product of two operators is

:::{math}
:label: eq-hilbert-142
(A,B) = \tr (A^\hc B) = \sum_{mn}  A^\cc_{mn} B_{mn},
:::

where the final expression involves the matrix elements of $A$ and $B$ with respect to an arbitrary orthonormal basis. Thus, the scalar product of an operator with itself is the sum of the absolute squares of the matrix elements,

:::{math}
:label: eq-hilbert-143
(A,A) = \sum_{mn} |A_{mn}|^2,
:::

which vanishes if and only if $A=0$.

(sec-hilbert-29)=

## Mathematical Notes

We collect here some remarks of a mathematical nature on the preceding discussion. For a precise treatment of the mathematics involved, see the references.

The set of normalizable wave functions $\{\psi(x)\}$ is infinite-dimensional because given any finite sequence of normalizable wave functions, $(\psi_1, \ldots, \psi_n)$, one can always find a new normalizable wave function that is linearly independent of those given.

A Hilbert space is a complex, normed vector space that is *complete*. The latter property means that all Cauchy sequences converge to a point of the space. This property is automatic in finite dimensions. In addition, many authors require a Hilbert space to be *separable*, which means that it possesses a countable basis. Sakurai (in *Modern Quantum Mechanics*) is mistaken when he says that a Hilbert space has an uncountable basis; he is thinking of the “bases” of the continuous spectrum, such as the set $\{ \delta(x-x_0) | x_0 \in \Reals\}$, but these basis wave functions are not normalizable and do not belong to Hilbert space. In field theory, one must deal with spaces that are not separable (since they possess uncountable bases of normalizable vectors, but not countable ones). Such spaces are called *Fock spaces*.

Properly speaking, functions $\psi(x)$ do not stand in one-to-one correspondence with elements of Hilbert space. The functions must be measurable, and two functions that differ by a subset of measure zero are considered equivalent. Thus, it is really an equivalence class of wave functions $\psi(x)$ that corresponds to a state vector $\ket{\psi}$. All these wave functions, however, give the same results in their physical predictions (such as the probability of finding a particle on some interval). This is related to the fact that one cannot measure a wave function at a point, so there is no physical way to detect the difference between two wave functions that differ on a subset of measure zero.

Sometimes Hermitian operators are also called *self-adjoint*; to be precise about this terminology, on a finite-dimensional Hilbert space “Hermitian” and “self-adjoint” are equivalent, but on an infinite-dimensional space this is true only if certain assumptions are made about the properties of the operators and their domains of definition.

The usual Hermitian operators encountered in quantum mechanics (for example, Hamiltonians) are complete, although the mathematical proof is often technical. In fact, the completeness property is intimately tied up with the physical interpretation of the measurement process, since (according to the usual interpretation of measurement) if a measurement were to correspond to an incomplete operator, it would mean that measuring all possible outcomes would result in a total probability less than unity. In this course (and in most of the literature on quantum mechanics) we assume the completeness of all Hermitian operators we encounter without further comment.

Regarding the first integral on the right in {eq}`eq-hilbert-106`, which must vanish in order to show that $\matrixelement{\psi}{\phat}{\phi} = \matrixelement{\phi}{\phat}{\psi}^\cc$, we note that normalizability does not imply that a wave function $\psi(x)$ approaches zero as $x \to \pm \infty$. At issue here is the fact that the momentum operator $\phat$ is *unbounded*, that is, it maps some normalizable wave functions into unnormalizable ones (taking them out of Hilbert space). If, however, both $\phat\psi$ and $\phat\phi$ are normalizable, then the integral in question does vanish.

(sec-hilbert-30)=

## References

The standard early reference for physicists on the formalism of quantum mechanics is P. A. M. Dirac, *The Principles of Quantum Mechanics*, 4th ed (Oxford University Press, Oxford, 1974), while for mathematicians it is John von Neumann, *Mathematical Foundations of Quantum Mechanics* (Princeton University Press, Princeton, 1955) (this is the English translation of the German original). Modern textbooks that devote more than the usual attention to mathematical questions include Albert Messiah, *Quantum Mechanics* vols. I and II (John Wiley, New York, 1966) (translation of French original), and Leslie E. Ballentine, *Quantum Mechanics: A Modern Development* (World Scientific, Singapore, 1998). The standard modern reference on the mathematics of quantum mechanics is Michael Reed and Barry Simon, *Functional Analysis* revised ed (Academic Press, New York, 1980), and, by the same authors, *Fourier Analysis, Self-Adjointness* (Academic Press, New York, 1975). See also *Quantum Mechanics in Hilbert Space* by Eduard Prugove\v cki (Dover, Mineola, New York, 1981).

\problems

(prob-hilbert-1)=

**Problem \prbdhilbert-1..** 

:::{math}
:label: eq-hilbert-144
I = \begin{pmatrix}1 & 0 \\ 0 & 1\\\end{pmatrix}, \quad \sigma_x = \begin{pmatrix}0 & 1\\ 1 & 0 \\\end{pmatrix}, \quad \sigma_y = \begin{pmatrix}0 & -i\\ i & 0 \\\end{pmatrix}, \quad \sigma_z = \begin{pmatrix}1 & 0 \\ 0 & -1 \\\end{pmatrix}.
:::

Matrices $\sigma_x$, $\sigma_y$ and $\sigma_z$ are called the *Pauli matrices*. We will also denote them $\sigma_1$, $\sigma_2$, $\sigma_3$.

\problempart{(a)} Show that

:::{math}
:label: eq-hilbert-145
\sigma_i \sigma_j = \delta_{ij} + i\epsilon_{ijk} \, \sigma_k,
:::

where $\delta_{ij}$ is understood to be multiplied by $I$, where we use the summation convention (see {ref}`sec-tensor-3`), and where $\epsilon_{ijk}$ is the completely antisymmetric Levi-Civita symbol (see {ref}`sec-tensor-15`, and ask if you don't understand, since this notation will be used frequently in the course). Notice that {eq}`eq-hilbert-145` implies

:::{math}
:label: eq-hilbert-146
[\sigma_i,\sigma_j]=2i\, \epsilon_{ijk}\,\sigma_k,
:::

and

:::{math}
:label: eq-hilbert-147
\{\sigma_i,\sigma_j\} = 2\delta_{ij},
:::

where the curly brackets are the anticommutator.

What we mean by a *vector operator* is a vector *of* operators, for example, $\Avec=(A_x,A_y,A_z)$, where $A_x$, $A_y$ and $A_z$ are operators. Now given any two vector operators $\Avec$, $\Bvec$ that commute with $\sigmavec$ but not necessarily with each other, use {eq}`eq-hilbert-145` to show that

:::{math}
:label: eq-hilbert-148
(\sigmavec\cdot\Avec) (\sigmavec\cdot\Bvec) = \Avec\cdot\Bvec + i \sigmavec\cdot(\Avec\times\Bvec),
:::

where

:::{math}
:label: eq-hilbert-149
\sigmavec = \sigma_x {\hat{\mathbf{x}}} + \sigma_y {\hat{\mathbf{y}}} + \sigma_z {\hat{\mathbf{z}}}.
:::

We think of $\sigmavec$ as a “vector” of $2\times 2$ matrices.

Two vector operators are considered to commute if all of their components commute. Note that in general, $\Avec \cdot \Bvec \ne \Bvec \cdot \Avec$, and $\Avec \times \Bvec \ne -\Bvec \times \Avec$.

\problempart{(b)} Let ${\hat{\mathbf{n}}}$ be an arbitrary unit vector and $\theta$ an arbitrary angle. Show that

:::{math}
:label: eq-hilbert-150
\exp(-i\theta \sigmavec \cdot {\hat{\mathbf{n}}}) = I \cos\theta - i (\sigmavec\cdot{\hat{\mathbf{n}}}) \sin \theta.
:::

In this course we will often drop the $I$, it being understood that a scalar like $\cos\theta$ is multiplied by the identity matrix.

(prob-hilbert-2)=

**Problem \prbdhilbert-2..** 

\problempart{(a)} Consider two operators $A$, $B$ that do not necessarily commute. Show that

:::{math}
:label: eq-hilbert-151
e^A B e^{-A} = B + [A,B] + {1\over 2!} [A,[A,B]] + {1\over 3!} [A,[A,[A,B]]] + \ldots.
:::

Hint: Replace $A$ by $\lambda A$, where $\lambda$ is a parameter, and let the left-hand side be $F(\lambda)$. Find a differential equation satisfied by $F(\lambda)$, and solve it. Alternatively, expand $F(\lambda)$ in a Taylor series in $\lambda$.

\problempart{(b)} Let $A(t)$ be an operator that depends on time. Derive the following operator identity:

:::{math}
:label: eq-hilbert-152
\dod{(e^A)}{t}\,e^{-A} = \sum_{n=0}^\infty {1 \over (n+1)!} L_A^n \left(\dod{A}{t}\right),
:::

where

:::{math}
:label: eq-hilbert-153
L_A (X) = [A,X], \quad L_A^2 (X) = [A,[A,X]], \quad \ldots,
:::

where $X$ is an arbitrary operator. Also, $L_A^0(X) = X$. Do not assume that $A$ commutes with $dA/dt$. We will use this identity when we study the nonrelativistic limit of the Dirac equation.

(prob-hilbert-3)=

**Problem \prbdhilbert-3..** 

\problempart{(a)} If $A$ and $B$ are square matrices, show that

:::{math}
:label: eq-hilbert-154
\tr(AB) = \tr(BA).
:::

Also prove {eq}`eq-hilbert-140`.

\problempart{(b)} Show that $\tr\sigma_i=0$. It may be easiest just to use the definitions {eq}`eq-hilbert-144`. Then use {eq}`eq-hilbert-145` to find a simple expression for $\tr(\sigma_i\sigma_j)$.

\problempart{(c)} The set of four $2\times2$ matrices, $(I,\sigmavec)$ form a basis in the space of $2\times2$ matrices, that is, an arbitrary $2\times2$ matrix can be expressed as a linear combination of these four matrices. Thus, if $M$ is an arbitrary $2\times2$ matrix, it can be expressed as

:::{math}
:label: eq-hilbert-155
M = aI + \bvec\cdot\sigmavec,
:::

This follows from the fact that $I$ and the three $\sigma_i$ are linearly independent, as can be seen just by looking at the four matrices. Find neat expressions for the expansion coefficients, $a$ and $\bvec=(b_1,b_2,b_3)$. Do this by taking traces, or by multiplying by a Pauli matrix and then taking traces. Also show that $M$ is Hermitian if and only if $a$, $\bvec$ are real.

\problempart{(d)} Now suppose that $M$ is nonzero in only the $(r,s)$ slot, where it has a 1. That is, let

:::{math}
:label: eq-hilbert-156
M_{ij} = \delta_{ir}\,\delta_{js}.
:::

Use this in {eq}`eq-hilbert-155` to find a nice expression for $(\sigma_m)_{ij}(\sigma_m)_{k\ell}$ (summation convention everywhere, so sum on $m$ in this expression) in terms of Kronecker deltas.

(prob-hilbert-4)=

**Problem \prbdhilbert-4..** 

\problempart{(a)} Show that {eq}`eq-hilbert-48` follows from {eq}`eq-hilbert-47`.

\problempart{(b)} Prove {eq}`eq-hilbert-55`, {eq}`eq-hilbert-58`, and {eq}`eq-hilbert-59`.

\problempart{(c)} Prove that the product of two Hermitian operators is Hermitian if and only if they commute.

\problempart{(d)} Show that

:::{math}
:label: eq-hilbert-157
\tr\bigl(\ketbra{\alpha}{\beta}\bigr) = \braket{\beta}{\alpha}.
:::

(prob-hilbert-5)=

**Problem \prbdhilbert-5..** 

We define an operator to be *normal* if it commutes with its Hermitian conjugate, $[A,A^\hc]=0$. Notice that Hermitian, anti-Hermitian, and unitary operators are normal. In the following you may assume that you are working on a finite-dimensional Hilbert space.

\problempart{(a)} Show that if $A$ is normal, and $A\ket{u}=a\ket{u}$ for some nonzero $\ket{u}$, then $A^\hc\ket{u}=a^\cc\ket{u}$. Thus, the eigenbras of $A$ are the Hermitian conjugates of the eigenkets, and the left spectrum is identical to the right spectrum. Hint: it is not necessary to introduce orthonormal bases or anything of the kind.

\problempart{(b)} Show that the eigenspaces corresponding to distinct eigenvalues of a normal operator are orthogonal. This is a generalization of the easy and familiar proof for Hermitian operators.

(prob-hilbert-6)=

**Problem \prbdhilbert-6..** 

\problempart{(a)} If $A$ is an observable, show that

:::{math}
:label: eq-hilbert-158
P_n = \prod_{k\ne n} {A-a_k \over a_n - a_k},
:::

where $P_n$ is the projector onto the $n$-th eigenspace of $A$. This shows that the projector $P_n$ is a function of the operator $A$ (see \secrhilbert-25).

\problempart{(b)} Show that if

:::{math}
:label: eq-hilbert-159
\matrixelement{\psi}{A}{\psi}=0
:::

for all $\ket{\psi}$, then $A=0$. ($A$ is not necessarily Hermitian.) Would this be true on a real vector space? (A real vector space is one in which the coefficients allowed in forming linear combinations of basis vectors are real. In a complex vector space, such as Hilbert space, these coefficients are allowed to be complex.)

(prob-hilbert-7)=

**Problem (c)} Let $U$ be a linear operator, and let $\ket{\psi'} = U\ket{\psi}$.  Show that $\braket{\psi'}{\psi'} = \braket{\psi}{\psi}$ for all kets $\ket{\psi.** 

(prob-hilbert-8)=

**Problem (d)} Consider now the Hilbert space for a particle moving in one dimension, which is infinite-dimensional.  Let $\ket{n.** 

:::{math}
:label: eq-hilbert-160
U\ket{n}=\ket{n+1}.
:::

Show that if $\ket{\psi'}=U\ket{\psi}$, then $\braket{\psi'}{\psi'}=\braket{\psi}{\psi}$. Then show that

:::{math}
:label: eq-hilbert-161
U^\dagger U=1.
:::

Thus $U$ has a left inverse, and it is $U^\dagger$. Does $U$ have a right inverse? Is $U$ unitary?

This problem shows that in an infinite dimensional Hilbert space, if an operator preserves the norm of all vectors, and if it possesses an inverse (both left and right), then it is unitary.

(prob-hilbert-9)=

**Problem \prbdhilbert-7.}  Let $V$ be a real vector space with a positive definite scalar product.  If $x$ and $y$ are vectors in $V$, we denote their scalar product by $(x,y)$.  This is like the scalar product $\braket{x}{y.**
