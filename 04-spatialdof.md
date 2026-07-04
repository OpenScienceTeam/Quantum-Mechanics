---
title: "04. Spatial Degrees of Freedom"
---
(ch-spatialdof)=

# 04. Spatial Degrees of Freedom

(sec-spatialdof-1)=

## Introduction

In these notes we develop the theory of wave functions in configuration space, building it up from the ket formalism and the postulates of quantum mechanics. We consider a system with one particle moving in space. In this set of notes we will not deal with the dynamics of the particle, so we will not need to say what the Hamiltonian is (that is taken care of in {ref}`ch-tevolut`). We assume the particle has no spin or other internal degrees of freedom, or that if such degrees of freedom exist they can be ignored. This allows us to establish an isomorphism between the Hilbert space of kets and the Hilbert space of wave functions on configuration space. We then introduce translation operators and use them and the classical correspondence to motivate the definition of momentum in quantum mechanics. We then explore the two representations, position and momentum, and the relationship between them. Finally, we discuss minimum uncertainty wave packets.

(sec-spatialdof-2)=

## The Position Representation; Wave Functions

For simplicity we begin with the one-dimensional case, in which the physical system is a particle moving in one dimension. According to the postulates of quantum mechanics, this system is associated with a Hilbert space $\ES$. We assume the position $x$ of a particle in one dimension can be measured, and that the results of the measurement are continuous. Thus, we are dealing with the case of the continuous spectrum. We denote the operator corresponding to measuring $x$ by $\xhat$, so the eigenvalue-eigenket problem is

:::{math}
:label: eq-spatialdof-1
\xhat \ket{x} = x \ket{x}.
:::

Here $\xhat$ is the operator, $x$ is the eigenvalue, and $\ket{x}$ is the eigenket with eigenvalue $x$. Since $x$ belongs to the continuous spectrum, the eigenkets $\ket{x}$ are not normalizable and lie outside Hilbert space.

We also assume that $\xhat$ by itself forms a complete set of commuting observables, which, as we shall see, means that the wave function is a scalar (it has only one component). In practice, this means that we are dealing with a spinless particle (a particle of spin 0, for example, the $\pi$-meson, the nucleus of ordinary helium, or the hydrogen atom in its ground state). It may also mean that we have a particle with spin, such as the electron, but the spin degrees of freedom are not important for the physics we are interested in. This point was discussed in {ref}`sec-postulat-5`.

Since $\xhat$ is a complete set of commuting observables, the eigenkets $\ket{x}$ are nondegenerate and form a basis in the Hilbert space in the continuum sense. These eigenkets are only defined by {eq}`eq-spatialdof-1` to within a normalization and a phase. We fix the normalization by requiring

:::{math}
:label: eq-spatialdof-2
\braket{x_1}{x_2} = \delta(x_1-x_2),
:::

the usual orthonormality condition in the continuum. The phase conventions for the eigenkets $\ket{x}$ are a question we shall return to later. Under these assumptions, the resolution of the identity takes the form

:::{math}
:label: eq-spatialdof-3
1 = \int_{-\infty}^{+\infty} dx\, \ketbra{x}{x}.
:::

Now let $\ket{\psi}$ represent a normalized (pure) state of the system, let $I=[x_0,x_1]$ be an interval on the $x$-axis, and let $P_I$ be the corresponding projection operator,

:::{math}
:label: eq-spatialdof-4
P_I= \int_{x_0}^{x_1} dx \, \ketbra{x}{x}.
:::

Then, according to the postulates of quantum mechanics ({ref}`sec-postulat-2`), we have

:::{math}
:label: eq-spatialdof-5
\\textProb(x_0 \le x \le x_1) = \matrixelement{\psi}{P_I}{\psi} = \int_{x_0}^{x_1} dx \, \braket{\psi}{x} \braket{x}{\psi}.
:::

We now introduce the definition,

:::{math}
:label: eq-spatialdof-6
\boxed{\psi(x) = \braket{x}{\psi},}
:::

of the *wave function* $\psi(x)$, whereupon the probability {eq}`eq-spatialdof-5` can be written,

:::{math}
:label: eq-spatialdof-7
\\textProb(x_0 \le x \le x_1) = \int_{x_0}^{x_1} dx \, |\psi(x)|^2.
:::

Since the interval $[x_0,x_1]$ is arbitrary, we see that $|\psi(x)|^2$ must be interpreted as the *probability density* of finding the particle on the $x$-axis. We have derived wave functions from the ket formalism plus the postulates of quantum mechanics, as promised in {ref}`ch-hilbert`.

{eq}`eq-spatialdof-6` is important because it shows how to go from kets to wave functions. It takes the place of sloppy notation such as {eq}`eq-hilbert-7`. That is, in addition to the Hilbert space $\ES$ of kets, we have another Hilbert space, this one consisting of normalizable wave functions on configuration space, $\psi(x)$. {eq}`eq-spatialdof-6` expresses the mapping between these spaces, which identifies kets with wave functions. To go the other direction, we multiply $\ket{\psi}$ on the left by the resolution of the identity {eq}`eq-spatialdof-3`,

:::{math}
:label: eq-spatialdof-8
\ket{\psi} = \int dx \, \ket{x} \braket{x}{\psi},
:::

which, by using {eq}`eq-spatialdof-6`, becomes

:::{math}
:label: eq-spatialdof-9
\boxed{\ket{\psi} = \int dx \, \ket{x} \psi(x).}
:::

This is the inverse of {eq}`eq-spatialdof-6`, allowing one to go from a wave function $\psi(x)$ to the corresponding ket $\ket{\psi}$. We see that $\psi(x)$ is the set of expansion coefficients of the ket $\ket{\psi}$ in the position eigenbasis.

Another consequence of this formalism follows easily. Suppose we have two kets $\ket{\psi}$ and $\ket{\phi}$, and we wish to compute the scalar product $\braket{\psi}{\phi}$ in wave function language. We simply insert the resolution of the identity {eq}`eq-spatialdof-3` between the bra and the ket to obtain,

:::{math}
:label: eq-spatialdof-10
\braket{\psi}{\phi} = \int dx \, \braket{\psi}{x}\braket{x}{\phi} = \int dx \, \psi^\cc(x)\phi(x),
:::

a familiar formula that translates the scalar product on the Hilbert space of kets into the language of wave functions.

This formalism is easily generalized to three dimensions. Let $\xvec$ be a position vector in three-dimensional space, with components $(x,y,z)$ or $(x_1,x_2,x_3)$. The measurement of the three components of position corresponds to a vector of operators, which we denote by ${\hat{\mathbf{x}}}$ (with a hat), to distinguish the operators from their eigenvalues (the results of the position measurement). In quantum mechanics, when we speak of a “vector operator” we usually mean a *vector of operators*, in this case three operators ${\hat{\mathbf{x}}}= (\xhat,\yhat,\zhat) = (\xhat_1, \xhat_2, \xhat_3)$. We assume that the components of ${\hat{\mathbf{x}}}$ commute with one another,

:::{math}
:label: eq-spatialdof-11
[\xhat_i,\xhat_j]=0,
:::

which as explained in {ref}`ch-postulat`\ can be tested experimentally. For example, if we filter a beam in $x$ and then $y$ by means of small slits, or do it in the reverse order, we find that the statistical results of arbitrary measurements on the filtered beam are the same in both cases.

As above we assume that we can ignore any internal degrees of freedom of the particle, so that the three operators ${\hat{\mathbf{x}}}$ by themselves form a complete set of commuting observables. Then the simultaneous eigenkets of ${\hat{\mathbf{x}}}$ are nondegenerate and form a basis by themselves. The eigenket-eigenvalue problem is

:::{math}
:label: eq-spatialdof-12
\xhat_i\ket{\xvec} = x_i\ket{\xvec},
:::

for $i=1,2,3$, a set of three simultaneous equations satisfied by an single eigenket $\ket{\xvec}=\ket{x,y,z}$, labeled by the three eigenvalues of the three commuting operators. In obvious generalizations of the one-dimensional case, we normalize these kets according to

:::{math}
:label: eq-spatialdof-13
\braket{\xvec_1}{\xvec_2} = \delta^3(\xvec_1-\xvec_2) = \delta(x_1-x_2) \delta(y_1-y_2) \delta(z_1-z_2),
:::

we have a resolution of the identity,

:::{math}
:label: eq-spatialdof-14
1 = \int d^3\xvec \, \ketbra{\xvec}{\xvec},
:::

and the transformation between wave functions and kets is given by

:::{math}
:label: eq-spatialdof-15
\psi(\xvec) = \braket{\xvec}{\psi},
:::

and

:::{math}
:label: eq-spatialdof-16
\ket{\psi} = \int d^3\xvec \, \ket{\xvec} \psi(\xvec).
:::

Also, the probability that the particle will be found in a region $R$ of three-dimensional space is

:::{math}
:label: eq-spatialdof-17
\int_R d^3\xvec \, |\psi(\xvec)|^2,
:::

so $|\psi(\xvec)|^2$ must be interpreted as the probability density.

Equations {eq}`eq-spatialdof-6` or {eq}`eq-spatialdof-15` define the *wave function* $\psi(x)$ or $\psi(\xvec)$, respectively, in quantum mechanics. A question that arises sometimes when solving the Schr\"odinger equation is whether $\psi$ is single-valued. But by our definitions, $\psi(x)$ or $\psi(\xvec)$ is automatically single-valued, since it is just the expansion coefficient of the state $\ket{\psi}$ with respect to the basis $\ket{x}$ or $\ket{\xvec}$.

Equations~{eq}`eq-spatialdof-6` and {eq}`eq-spatialdof-9` (in one dimension) or {eq}`eq-spatialdof-15` and {eq}`eq-spatialdof-16` (in three dimensions) make explicit the transformations back and forth between the Hilbert space of ket vectors $\ket{\psi}$ and the Hilbert space of wave functions $\psi(x)$ or $\psi(\xvec)$. As discussed in {ref}`sec-hilbert-3`, we regard these two Hilbert spaces as isomorphic but distinct, and we say that the space of wave functions $\psi(x)$ or $\psi(\xvec)$ forms the *configuration representation* of the space of kets $\ket{\psi}$. There are other representations, and while the configuration representation is often used in practice one should note that in the postulates of quantum mechanics there is no privileged role assigned to it. Any calculation that can be carried out in the configuration representation can be carried out in any other representation with the same results from a physical standpoint.

In effect, a representation is merely a choice of basis, allowing one to work with the expansion coefficients of a state vector $\ket{\psi}$ with respect to the chosen basis instead of the abstract ket vectors themselves. As noted below {eq}`eq-spatialdof-9`, the configuration space wave function $\psi(x)$ or $\psi(\xvec)$ is the expansion coefficients of the state ket $\ket{\psi}$ with respect to the basis of position eigenkets $\{ \ket{x} \}$ or $\{ \ket{\xvec} \}$. In quantum mechanics we frequently choose as a basis the simultaneous eigenkets of a complete set of commuting observables; thus, the basis is labeled by the observables in question, and we speak, for example, of the position representation, momentum representation, etc. Nothing prevents us from using other bases, however (which have no correspondence with any simple set of commuting observables).

Just as the wave function $\psi(x)$ represents the ket vector $\ket{\psi}$ in the configuration representation, so also is there a representation of various operators that act on ket vectors. Consider, for example, the operator $\xhat$ (working in one dimension for simplicity). We know that the ket $\ket{\psi}$ corresponds to the wave function $\psi(x)=\braket{x}{\psi}$. What wave function does the ket $\xhat\ket{\psi}$ correspond to? Let $\ket{\phi} = \xhat\ket{\psi}$, so that

:::{math}
:label: eq-spatialdof-18
\phi(x) = \braket{x}{\phi} = \matrixelement{x}{\xhat}{\psi} = x \braket{x}{\psi} = x\psi(x),
:::

where we have used $\bra{x}\xhat = x \bra{x}$, the Hermitian conjugate of {eq}`eq-spatialdof-1`. We see that the effect of multiplying a ket vector $\ket{\psi}$ by the operator $\xhat$ is to multiply the corresponding configuration wave function $\psi(x)$ by $x$. That is, we can write

:::{math}
:label: eq-spatialdof-19
(\xhat \psi)(x)=x\psi(x).
:::

As we say, the operator $\xhat$ is *represented* by multiplication by $x$ in the configuration representation. It is represented by other operations in other representations. Similarly, in three dimensions we have

:::{math}
:label: eq-spatialdof-20
(\xhat_i \psi)(\xvec) = x_i\psi(\xvec).
:::

You may worry about the physical meaning of the unnormalizable eigenkets $\ket{x}$ or $\ket{\xvec}$. In reality we never measure the position of a particle exactly, instead the best we can do is to localize it in some small region of space. The eigenkets $\ket{x}$ or $\ket{\xvec}$ are an idealization of this process, in which the size of the region is allowed to approach zero. This limit also leads to singular mathematics, since the eigenkets $\ket{x}$ or $\ket{\xvec}$ have infinite norm and do not belong to Hilbert space.

Measuring the position of a particle is really a nonrelativistic concept, because as we localize a particle to smaller and smaller regions, by the uncertainty principle the momentum increases, ultimately taking on relativistic values. Then processes such as the creation of particle-antiparticle pairs come into play, and we are really dealing with a multi-particle situation, which is properly handled by the methods of quantum field theory. We will find later in the course that the position operator for a particle in relativistic quantum mechanics is one that is fraught with difficulties. The position operator is really a nonrelativistic concept.

(sec-spatialdof-3)=

## Translation Operators

The subject of position measurements leads naturally into the question of translational invariance. The energy and other physical properties of an isolated system do not change if it is moved somewhere else, a fact that is more precisely stated by saying that the Lagrangian or Hamiltonian of such systems is invariant under spatial translations. This symmetry in turn leads to the conservation of momentum, which first appeared in physics as Newton's third law.

If a system is not isolated then its energy does depend on its position, for example, the potential energy of an electron in an electric field changes if the electron is moved. But the electric field is created by other charges somewhere else, and if those charges are included in the “system,” then the energy does not change when the entire system is moved.

In summary, spatial translations are a fundamental symmetry of nature which is closely related to the law of conservation of momentum. We now develop translation operators in quantum mechanics, working initially in one dimension for simplicity.

Let $a$ be a displacement. We imagine a displacement operation as one that acts on a physical system, moving all particles from their initial positions (say, $x$) to their new positions ($x+a$), both measured relative to an inertial frame. This is sometimes called the *active* point of view, because our operations take a given physical system and transform it into a new system, in this case in a different location.

In quantum mechanics, we can define a *translation operator* which carries out this operation on a physical system. The translation operator $T(a)$ is a linear operator acting on the Hilbert space of a physical system, parameterized by the displacement $a$. We define the translation operator in one dimension by

:::{math}
:label: eq-spatialdof-21
T(a)\ket{x} = \ket{x+a}.
:::

This definition makes sense, because physically $\ket{x}$ is the state of the system after a measurement has placed the particle in a small region around position $x$, and similarly for $\ket{x+a}$. {eq}`eq-spatialdof-21` is actually a definition of the operators $T(a)$ because the kets $\ket{x}$ form a basis. If we specify the action of a linear operator on a set of basis vectors, then by linear superposition its action on an arbitrary vector becomes known.

{eq}`eq-spatialdof-21` gives the action of the translation operator on the position eigenkets. Let us also work out its action on wave functions. Let $\ket{\psi}$ be a state with wave function $\psi(x) =\braket{\psi}{x}$, and let $\ket{\phi}=T(a)\ket{\psi}$ be the translated state with wave function $\phi(x) =\braket{x}{\phi}$. What is the relationship between the old wave function $\psi(x)$ and the new one $\phi(x)$? We answer this by writing

:::{math}
\begin{aligned}
\phi(x) &= \braket{x}{\phi} =\matrixelement{x}{T(a)}{\psi} = \int dx' \, \matrixelement{x}{T(a)}{x'} \braket{x'}{\psi} =\int dx' \, \braket{x}{x'+a} \braket{x'}{\psi}
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-22
\begin{aligned}
&= \int dx' \, \delta(x-x'-a) \psi(x') = \psi(x-a),
\end{aligned}
:::

where we have inserted a resolution of the identity, used {eq}`eq-spatialdof-21` and {eq}`eq-spatialdof-2`, and carried out the integral. We write the result as

:::{math}
:label: eq-spatialdof-23
\bigl(T(a)\psi\bigr)(x) = \psi(x-a),
:::

where we have replaced $\phi$ by $T(a)\psi$. This is a companion to {eq}`eq-spatialdof-21`, which gives the action of translation operators on the basis kets; this gives their action on wave functions.

There are several remarks concerning {eq}`eq-spatialdof-23`. First, notice the minus sign in this equation, compared to the plus sign in {eq}`eq-spatialdof-21`. The minus sign is necessary to get a wave function that has been moved forward under the displacement operation, as illustrated in {ref}`fig-spatialdof-1`. To remember the signs it helps to write {eq}`eq-spatialdof-22` in the form, $\bigl(T(a)\psi\bigr) (x+a) =\psi(x)$ and to say, “the value of the new wave function at the new point equals the value of the old wave function at the old point.”

:::{figure} images/spatialdof-fig01.png
:label: fig-spatialdof-1
:width: 80%

The action of the translation operator $T(a)$ on a wave function $\psi(x)$.
:::

Another remark is that that {eq}`eq-spatialdof-23` uses the translation operator $T(a)$ in a different sense from its original definition, because it is acting on a configuration space wave function $\psi$ instead of a ket $\ket{\psi}$. As we say, {eq}`eq-spatialdof-23` gives the *representation* of the operator $T(a)$ on configuration space wave functions.

Finally, we remark that many books would write {eq}`eq-spatialdof-23` without the parentheses, that is, as

:::{math}
:label: eq-spatialdof-24
T(a)\psi(x) = \psi(x-a).
:::

The problem with this notation is that it is not clear what $T(a)$ acts on. $\psi$ is a function, and $\psi(x)$ is the value of that function at a point $x$, that is, it is a number. Does $T(a)$ act on the function or the value of the function? Obviously, it acts on the function, which is what the extra parentheses in {eq}`eq-spatialdof-23` make explicit.

The translation operator is easily generalized to three dimensions, where the displacement $\avec$ is a vector, and the translation operator is defined by

:::{math}
:label: eq-spatialdof-25
T(\avec)\ket{\xvec} = \ket{\xvec+\avec}.
:::

The other formulas and results of this are easily generalized to the three-dimensional case.

(sec-spatialdof-4)=

## Properties of the Translation Operators

The translation operators in one dimension satisfy the following properties:

:::{math}
:label: eq-spatialdof-26a
\begin{aligned}
T(0) &= 1,
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-26b
\begin{aligned}
T(a)T(b) &= T(a+b) = T(b)T(a),
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-26c
\begin{aligned}
T(a)^{-1} &= T(-a),
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-26d
\begin{aligned}
T(a)^{-1} &= T(a)^\dagger.
\end{aligned}
:::

Property {eq}`eq-spatialdof-26a` follows immediately from the definition {eq}`eq-spatialdof-21`. Property {eq}`eq-spatialdof-26b` is the composition law that is also obvious from the definition {eq}`eq-spatialdof-21`; it can be proved explicitly by writing

:::{math}
:label: eq-spatialdof-27
T(a)T(b)\ket{x} = T(a)\ket{x+b} = \ket{x+b+a} = T(a+b)\ket{x}.
:::

Note that the parameter $x+b+a$ of the ket $\ket{x+b+a}$ is just a label of the ket, so these labels obey the usual (commutative) rules for addition. This implies that the translation operators are commutative, as indicated in {eq}`eq-spatialdof-26b`. The third property {eq}`eq-spatialdof-26c` is proved by setting $b=-a$ in {eq}`eq-spatialdof-26b`. The translation operators are invertible. The last property {eq}`eq-spatialdof-26d` states that the translation operators are unitary. We prove this by letting $\psi(x)$ be an arbitrary wave function, and $\ket{\phi} = T(a)\ket{\psi}$, so that $\phi(x)=\psi(x-a)$. Then

:::{math}
:label: eq-spatialdof-28
\int dx \, |\phi(x)|^2 = \int dx\, |\psi(x-a)|^2= \int dx \, |\psi(x)|^2,
:::

as we prove by substituting $x'=x-a$ in the middle integral. Thus, $T(a)$ preserves the norm of arbitrary states. But a linear operator that does this is necessarily unitary (see Prob. {ref}`prob-hilbert-6`(c)).

Altogether, properties {eq}`eq-spatialdof-26a`--{eq}`eq-spatialdof-26d` qualify the set of translation operators as a group of unitary operators. Unitary operators appear frequently in symmetry operations because these are the only linear operators that preserve probabilities (hence, the results of physical measurements). In this case, the group is *Abelian*, which means that the translation operators commute with one another (property {eq}`eq-spatialdof-26b`).

(sec-spatialdof-5)=

## The Generator of Translations

A simple idea that arises in the case of continuous symmetries is that a given, finite symmetry operation can be built up as a composition of smaller symmetry operations. For example, a displacement of one meter is the composition of a thousand displacements of one millimeter. In the limit we can imagine a finite symmetry operation as being built up out of an infinite number of infinitesimal symmetry operations. For this reason, special attention is attached to infinitesimal symmetry operations. It turns out that infinitesimal versions of unitary symmetry operators in quantum mechanics are always expressible in terms of certain Hermitian operators, which are called the *generators* of the symmetry. We will now see how this works out in the case of translations.

Thinking of a small displacement $a$, we expand the translation operator $T(a)$ in a Taylor series in powers of $a$. This series begins with

:::{math}
:label: eq-spatialdof-29
T(a) = T(0) + a \dod{T}{a}(0) + \ldots.
:::

The first (zeroth order) term is $T(0)=1$, and as for the second (first order) term, we notice that $dT/da|_{a=0}$ does not depend on $a$ so it is some operator with no parameters. We put this into a more convenient form by defining

:::{math}
:label: eq-spatialdof-30
\khat = i\dod{T}{a}(0),
:::

where the hat emphasizes that $\khat$ is an operator (in contrast to $a$, which is a number).

In these notes we frequently use a hat to distinguish an operator from an ordinary number, or from the classical counterpart of the operator. We normally omit the hat when there is no danger of confusion (for example, $T$ above is an operator, but we put no hat on it). But we also use the hat for unit vectors, and certain other purposes. We will explain these as they arise, so the meaning will be clear in any particular context.

Through first order, we can write the expansion of the translation operator as

:::{math}
:label: eq-spatialdof-31
T(a) = 1 -ia\khat+ \ldots.
:::

We have split off a factor of $i$ in the definition {eq}`eq-spatialdof-30` so that $\khat$ will be Hermitian. This follows when we use {eq}`eq-spatialdof-31` to write out the series for $T(a)^\hc$ and $T(-a)=T(a)^{-1}$:

:::{math}
:label: eq-spatialdof-32
\begin{aligned}
T(a)^\hc &= 1 + ia\khat^\dagger + \ldots, \\
T(-a) &= 1 + ia \khat + \ldots, \\

\end{aligned}
:::

which by {eq}`eq-spatialdof-26c` and {eq}`eq-spatialdof-26d` must be equal. But this implies

:::{math}
:label: eq-spatialdof-33
\khat = \khat^\dagger.
:::

The Hermitian operator $\khat$ appears in the first correction term in {eq}`eq-spatialdof-31`, which, when $a$ is small, is an infinitesimal translation. For this reason $\khat$ is regarded as the *generator* of translations in one dimension. That is, if we knew how to act on states with the operator $\khat$, we could bring about an infinitesimal translation; and finite translations are compositions of a large number of small translations. As yet we have no physical interpretation for $\khat$, but since it is Hermitian it must correspond to the measurement of some physical quantity. We will see in a moment what that is.

(sec-spatialdof-6)=

## Exponential Form for Translation Operators

We have only written out the first two terms in the Taylor series {eq}`eq-spatialdof-31` for $T(a)$, but the entire series can be summed and put into a neat form. To do this we will obtain a differential equation for $T(a)$ and then solve it. See Prob. {ref}`prob-hilbert-2`(a), which uses similar techniques. We first write out the definition of the derivative of $T(a)$ as a limit,

:::{math}
:label: eq-spatialdof-34
\dod{T(a)}{a} = \lim_{\epsilon\to0} {T(a+\epsilon) - T(a) \over \epsilon}.
:::

By {eq}`eq-spatialdof-26b`, the first term in the numerator can be written as $T(\epsilon)T(a)$, which allows the operator $T(a)$ to be factored out of the entire numerator to the right:

:::{math}
:label: eq-spatialdof-35
\dod{T(a)}{a} = \Bigl( \lim_{\epsilon\to0} {T(\epsilon)-1 \over \epsilon} \Bigr) T(a).
:::

But the remaining limit is just the derivative $dT(a)/da$ evaluated at $a=0$, which by {eq}`eq-spatialdof-30` is $-i\khat$. Altogether, we obtain

:::{math}
:label: eq-spatialdof-36
\dod{T(a)}{a} = -i\khat \,T(a).
:::

This is a differential equation that we must solve subject to the initial conditions $T(0)=1$. The solution is immediate,

:::{math}
:label: eq-spatialdof-37
T(a)= \exp(-ia\khat).
:::

Now we can easily extend the power series {eq}`eq-spatialdof-31` to higher order,

:::{math}
:label: eq-spatialdof-38
T(a)=1 -ia\khat -{1\over2} a^2\khat^2+ \ldots.
:::

We see that the generator of translations $\khat$, which first appeared in infinitesimal translation operators, also appears in the exponential form for finite translation operators.

There is another way to obtain {eq}`eq-spatialdof-37` that is closer to the idea of building up finite transformations from infinitesimal ones. Suppose $a$ is a displacement that is not small. We break it up into a large number $N$ of small displacements, writing $\epsilon=a/N$. Then property {eq}`eq-spatialdof-26b` implies

:::{math}
:label: eq-spatialdof-39
T(a) = T(\epsilon)^N.
:::

But if $\epsilon$ is small, we can approximate $T(\epsilon)$ by the first two terms of the Taylor series, as in {eq}`eq-spatialdof-31`, without assuming at this point that we know what the higher order terms are. Thus we have

:::{math}
:label: eq-spatialdof-40
T(a) \approx (1-i\epsilon\khat)^N.
:::

This approximation should get better as $\epsilon$ gets smaller, that is, as $N$ increases. This makes it plausible that we should have the limit,

:::{math}
:label: eq-spatialdof-41
T(a) = \lim_{N\to\infty} \Bigl(1-{ia\khat\over N}\Bigr)^N.
:::

This is similar to the limit of elementary calculus,

:::{math}
:label: eq-spatialdof-42
\lim_{N\to\infty}\Bigl(1+{x\over N}\Bigr)^N = e^x.
:::

Applying this to {eq}`eq-spatialdof-41` we obtain the exponential expression {eq}`eq-spatialdof-37`.

(sec-spatialdof-7)=

## Action of $\khat$ on Kets and Wave Functions

It is easy to work out the action of $\khat$ on the basis kets $\ket{x}$. We simply write

:::{math}
:label: eq-spatialdof-43
\khat \ket{x} = i\Bigl.\dod{T(a)}{a} \ket{x}\Bigr|_{a=0} = i\Bigl.\dod{}{a}\ket{x+a}\Bigr|_{a=0} = i\dod{}{x} \ket{x}.
:::

The derivative of the ket $\ket{x}$ may look strange. In wave function language it is the derivative of a $\delta$-function. One can use expressions with derivatives of kets as in {eq}`eq-spatialdof-43`, formally integrating by parts as if they were ordinary functions, and obtain correct answers.

We obtain an equivalent result that looks more familiar by working out the action of $\khat$ on a wave function. The procedure is the same:

:::{math}
:label: eq-spatialdof-44
(\khat\psi)(x) = i\Bigl. \Bigl(\dod{T(a)}{a}\psi\Bigr)(x) \Bigr|_{a=0} = i \Bigl. \dod{}{a} \psi(x-a)\Bigr|_{a=0} = -i\dod{\psi(x)}{x}.
:::

We start to see the appearance of the usual momentum operator on wave functions.

(sec-spatialdof-8)=

## Translations in Three Dimensions, and Commutation Relations

In a similar manner, for translation operators in three dimensions we define

:::{math}
:label: eq-spatialdof-45
\khat_i = i \Bigl.\frac{\partial T(\avec)}{\partial a_i}\Bigr|_{\avec=0},
:::

where $i=1,2,3$. This gives us a Hermitian vector operator (that is, a vector of Hermitian operators) ${\hat{\mathbf{k}}}$, with components $\khat_i$, $i=1,2,3$. Now the exponential form of the translation operator is

:::{math}
:label: eq-spatialdof-46
T(\avec) = \exp(-i\avec\cdot{\hat{\mathbf{k}}}) = 1 -i\avec\cdot{\hat{\mathbf{k}}} -{1\over 2}(\avec\cdot{\hat{\mathbf{k}}})^2 +\ldots.
:::

This series can be used to obtain the commutation relations of the operators ${\hat{\mathbf{k}}}=(\khat_1,\khat_2,\khat_3)$. We expand the product $T(\avec)T(\bvec)$ in power series, carrying everything to second order,

:::{math}
\begin{aligned}
T(\avec)T(\bvec) & = \Bigl[1-i(\avec\cdot{\hat{\mathbf{k}}}) -{1\over2}(\avec\cdot{\hat{\mathbf{k}}})^2 + \ldots \Bigr] \Bigl[1-i(\bvec\cdot{\hat{\mathbf{k}}}) -{1\over2}(\bvec\cdot{\hat{\mathbf{k}}})^2 + \ldots \Bigr]
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-47
\begin{aligned}
&= 1-i(\avec+\bvec)\cdot{\hat{\mathbf{k}}} -{1\over2}(\avec\cdot{\hat{\mathbf{k}}})^2 -(\avec\cdot{\hat{\mathbf{k}}})(\bvec\cdot{\hat{\mathbf{k}}}) -{1\over2}(\bvec\cdot{\hat{\mathbf{k}}})^2 + \ldots.
\end{aligned}
:::

But since $T(\avec)T(\bvec) =T(\bvec) T(\avec)$, the answer must be the same if we swap $\avec$ and $\bvec$. Most of the series is obviously symmetric in $\avec$ and $\bvec$, but the one term $(\avec\cdot{\hat{\mathbf{k}}}) (\bvec\cdot{\hat{\mathbf{k}}})$ is not. When we subtract the swapped series from the original series, we obtain a vanishing commutator,

:::{math}
:label: eq-spatialdof-48
[\avec\cdot{\hat{\mathbf{k}}}, \bvec\cdot{\hat{\mathbf{k}}}]=0.
:::

Since this is true for all choices of $\avec$ and $\bvec$, we can choose each of these vectors to be one of the unit vectors along the coordinate axes (nine choices in all), and we find

:::{math}
:label: eq-spatialdof-49
[\khat_i, \khat_j]=0.
:::

We see that ${\hat{\mathbf{k}}}$ is a vector of commuting, Hermitian operators.

The relations {eq}`eq-spatialdof-43` and {eq}`eq-spatialdof-44` are also easily generalized to three dimensions. These give

:::{math}
:label: eq-spatialdof-50
\khat_i \ket{\xvec} = i\pop{}{x_i} \ket{\xvec},
:::

and

:::{math}
:label: eq-spatialdof-51
\bigl(\khat_i\psi\bigr)(\xvec) = -i \frac{\partial \psi(\xvec)}{\partial x_i},
:::

or, in vector notation,

:::{math}
:label: eq-spatialdof-52
\bigl({\hat{\mathbf{k}}}\psi\bigr)(\xvec) = -i\del\psi(\xvec).
:::

{eq}`eq-spatialdof-51` provides another way to derive the commutation relations {eq}`eq-spatialdof-49`, that is, the derivatives $\partial/\partial x_i$ and $\partial/\partial x_j$ commute with one another.

It is also easy to work out the commutation relations among the operators $\xhat_i$ and $\khat_j$. We just apply them to a wave function in opposite orders, obtaining

:::{math}
:label: eq-spatialdof-53
\begin{aligned}
\xhat_i\khat_j\psi &= x_i \Bigl(-i\pop{}{x_j}\Bigr)\psi = -ix_i\frac{\partial \psi}{\partial x_j}, \\
\khat_j\xhat_i\psi &= \Bigl(-i\pop{}{x_j}\Bigr)x_i\psi = -i\,\delta_{ij}\,\psi -i x_i\frac{\partial \psi}{\partial x_j}.
\end{aligned}
:::

Subtracting these, we find

:::{math}
:label: eq-spatialdof-54
[\xhat_i, \khat_j] = i\, \delta_{ij}.
:::

Combined with {eq}`eq-spatialdof-11` and {eq}`eq-spatialdof-49`, this gives a complete set of commutation relations among the components of the operators ${\hat{\mathbf{x}}}$ and ${\hat{\mathbf{k}}}$.

(sec-spatialdof-9)=

## The Momentum in Classical Mechanics

We shall make a few remarks about the momentum in classical mechanics, in preparation for our discussion of the momentum in quantum mechanics.

As explained in {ref}`sec-classmech-11`, there is more than one definition of the momentum of particle in classical mechanics. One is the *kinetic momentum*,

:::{math}
:label: eq-spatialdof-55
\pvec = m \dot\xvec,
:::

and the other is the *canonical momentum*,

:::{math}
:label: eq-spatialdof-56
\pvec= \frac{\partial L}{\partial \dot\xvec},
:::

where $L$ is the Lagrangian. In the case of a particle of charge $q$ moving in static electric and magnetic fields $\Evec=-\del \Phi$ and $\Bvec = \del \cross \Avec$, the Lagrangian is

:::{math}
:label: eq-spatialdof-57
L(\xvec,\dot\xvec) = {m \over 2} | \dot \xvec|^2 -q\Phi(\xvec) + {q \over c} \dot\xvec \cdot \Avec(\xvec),
:::

so the canonical momentum is given by {eq}`eq-classmech-35`, reproduced here,

:::{math}
:label: eq-spatialdof-58
\pvec= m \dot\xvec + {q\over c} \Avec(\xvec).
:::

In the presence of a magnetic field (more precisely, in the presence of a vector potential) the definitions of the classical momentum {eq}`eq-spatialdof-55` and {eq}`eq-spatialdof-56` are not the same. We have not defined the momentum operator in quantum mechanics yet, but before we do, we must ask which of these two classical momenta will it correspond to, the kinetic or the canonical?

We have been developing the properties of the operator $\khat$ in quantum mechanics, which is the generator of displacements. It turns out that there is a similar role played by the momentum in classical mechanics, but it is the canonical momentum, not the kinetic, that does this. Let us write $f(x,p)$ be a function of the position and momentum for a particle moving in one dimension. We can think of $f$ as a *classical observable*. Then we can define a classical translation operator that acts on classical observables according to

:::{math}
:label: eq-spatialdof-59
\bigl( T_cl(a) f\bigr)(x,p) =f(x-a,p).
:::

This operator moves the function $f(x,p)$ forward in $x$ while leaving $p$ alone. If now $a$ is a small displacement, then the result can be expanded to first order,

:::{math}
:label: eq-spatialdof-60
\bigl( T_cl(a) f\bigr)(x,p) = f(x,p) - a\frac{\partial f}{\partial x}.
:::

But the correction term can be written in terms of a Poisson bracket of $f$ with the momentum,

:::{math}
:label: eq-spatialdof-61
-a \frac{\partial f}{\partial x}= a\{ p, f \}.
:::

Finite displacements can be built up by composing infinitesimal displacements, and the result can be expressed in terms of an exponential series of iterated Poisson brackets. We introduce the following notation for the Poisson bracket,

:::{math}
:label: eq-spatialdof-62
L_X A = \{X,A\},
:::

where $X$ and $A$ are arbitrary classical observables. Then a finite displacement can be expressed as

:::{math}
:label: eq-spatialdof-63
T_cl(a) = \exp(a L_p),
:::

that is,

:::{math}
:label: eq-spatialdof-64
\begin{aligned}
f(x-a,p) &= \bigl(T_cl(a)f\bigr)(x,p) = \bigl(\exp(aL_p) f\bigr)(x,p) \\
&=f(x,p) + a \{ p,f\} + {a^2\over 2!} \{p,\{p,f\}\} + \ldots \\
&= f(x,p) - a\frac{\partial f}{\partial x}(x,p) + {a^2\over 2!} {\partial^2 f \over \partial x^2}(x,p) +\ldots \\

\end{aligned}
:::

which may be compared to {eq}`eq-spatialdof-37` and {eq}`eq-spatialdof-38`. The result is the Taylor series expansion of $f(x,p)$ in the variable $x$. It may also be compared to the exponential series developed in Prob. {ref}`prob-hilbert-2`(a).

These results are easily generalized to three dimensions. In three dimensions, the distinction between the kinetic and canonical momentum becomes important. It is the canonical momentum, not the kinetic, that generates translations in classical mechanics (in cases where it makes a difference). That is, the Poisson brackets are computed with respect to the canonical momentum, not the kinetic. See {eq}`eq-classmech-100`.

The role that momentum plays in classical mechanics as the generator of displacements is closely connected with the conservation of momentum in systems with translational symmetry. This conservation law is a special case of *Noether's theorem*, which presents a general relationship between continuous symmetries and conserved quantities.

(sec-spatialdof-10)=

## The Momentum in Quantum Mechanics

Let us work in three dimensions. According to the postulates of quantum mechanics, measurements of the momentum $\pvec$ of a particle must correspond to some operator (actually, a vector of three operators), call it ${\hat{\mathbf{p}}}$, where the hat distinguishes the classical or $c$-number momentum $\pvec$ from the operator. At this point we know what the Hilbert space is for particles moving in three dimensions; it is a ket space $\ES$ that isomorphic to the space of wave functions $\psi(\xvec)$. But what does the momentum operator ${\hat{\mathbf{p}}}$ do to states in this space? That is, what is the momentum operator explicitly?

The operator ${\hat{\mathbf{k}}}$ is the generator of displacements in quantum mechanics, since by {eq}`eq-spatialdof-31` it provides the small correction necessary when an infinitesimal displacement is carried out. Also, as noted, ${\hat{\mathbf{k}}}$ corresponds to the measurement of some physical quantity, and both ${\hat{\mathbf{k}}}$ and $\pvec$ (the latter being the generator of translations in classical mechanics) are vectors. So the suspicion arises that ${\hat{\mathbf{k}}}$ is related to the momentum operator ${\hat{\mathbf{p}}}$ in quantum mechanics. The vector operators ${\hat{\mathbf{k}}}$ and ${\hat{\mathbf{p}}}$ cannot be equal, however, because they have different units: ${\hat{\mathbf{k}}}$ has units of inverse length, and ${\hat{\mathbf{p}}}$ has units of momentum. To make the units come out right we guess that there is a proportionality factor between ${\hat{\mathbf{p}}}$ and ${\hat{\mathbf{k}}}$ with units of action, a constant that we call $\hbar$:

:::{math}
:label: eq-spatialdof-65
{\hat{\mathbf{p}}} = \hbar {\hat{\mathbf{k}}}.
:::

We take this as the definition of momentum in quantum mechanics.

The postulates of quantum mechanics do not tell us what quantum operator corresponds to a given classical quantity, so we must not think that the definition of momentum ${\hat{\mathbf{p}}}$ is engraved in stone. The best we can do is to find a vector of operators in quantum mechanics that has properties similar to the classical momentum and that goes over to the classical momentum in the classical limit. In fact, the similarity with the classical momentum (as the generator of translations) has motivated the definition {eq}`eq-spatialdof-65`, and, as for the classical limit and the other expected properties of momentum, they will be laid bare as we proceed.

(sec-spatialdof-11)=

## The Constant $\hbar$

Notice that $\hbar$ did not appear in the postulates of quantum mechanics; it appears for the first time in our development of the formalism in {eq}`eq-spatialdof-65`. The value of $\hbar$ in ordinary units must be determined experimentally. The discussion so far has been based on the analysis of a single particle moving in three-dimensional space, so one might question whether different particles have different values of $\hbar$. We would not get the usual classical limit if this were so, so it seems theoretically doubtful that there are different values of $\hbar$, but it is a question that can be tested experimentally (all the $\hbar$'s turn out to be the same to within experimental accuracy). Given that there is only one $\hbar$, there is the option of choosing “natural units” in which $\hbar=1$.

The relation {eq}`eq-spatialdof-65` implies the usual de~Broglie relation connecting momentum and wavelength,

:::{math}
:label: eq-spatialdof-66
\lambda={2\pi\hbar \over p},
:::

as we shall show momentarily, so the value of $\hbar$ can be determined by measuring the de~Broglie wavelength of a particle of a known momentum. The most elegant experiments along these lines have involved Bragg diffraction of a neutron beam from a single, large (about 10cm) silicon crystal with no dislocations or grain boundaries. The manufacture of such crystals has become feasible with modern semiconductor technology. The predictions of the relation {eq}`eq-spatialdof-65` are fully confirmed. Actually, if {eq}`eq-spatialdof-65` were not correct, there are very few of the theoretical predictions of quantum mechanics that would agree with experiment.

The silicon neutron interferometer just mentioned was used in the 1970's to measure the phase shift of neutron wave functions as the neutrons fall in the earth's gravitational field. This was the first demonstration that gravitational potentials enter the Schr\"odinger equation in the same manner as other potentials. The experiment and results are discussed in Sakurai, *Modern Quantum Mechanics* and in Commins, *Quantum Mechanics: An Experimentalist's Approach*. Commins has a particulary nice explanation of the neutron interferometer.

The fact that $\hbar$ is a universal constant was known to Planck and others in the 1890's, even before quantum mechanics existed. Planck knew that a constant with dimensions of action must occur in the expression for the spectrum of black body radiation, even before the correct expression was known. He also realized that $h=2\pi\hbar$, $c$ and $G$ (Newton's constant of gravitation) could be combined to create a natural system of units for distance, time and mass. The Planck unit of distance is

:::{math}
:label: eq-spatialdof-67
L_Planck = \sqrt{{\hbar G \over c^3}} = 1.6 \times 10^{-33}cm.
:::

It is the length scale at which the effects of both quantum mechanics and gravity are expected to be important. Physics at such scales is currently a matter of much speculation, and is likely to remain so for some time, in view of the near impossibility of direct experimental tests. Nevertheless the importance of the length scale itself has been known for a long time.

(sec-spatialdof-12)=

## The Momentum in Quantum Mechanics:  The History

The pseudo-axiomatic approach we are taking here to the development of the momentum operator in quantum mechanics is quite different from the historical one. In a series of papers between 1905 and 1916, Einstein developed the idea that light of frequency $\omega$ and wave vector $\kvec$ is associated with particles of energy $E=\hbar\omega$ and momentum $\pvec=\hbar\kvec$. We now call these particles “photons,” although that name was not coined until later. According to Maxwell's equations the frequency and wave number of a light wave are related by $\omega=ck$, so Einstein's formulas give the energy-momentum relation for the photon as $E=cp$, exactly what the special theory of relativity predicts for a massless particle traveling at the speed of light. Einstein's arguments relied heavily on statistical mechanics. Most physicists of the time regarded the idea of particles of light as completely crazy, since it had been established a hundred years earlier that light was a wave. But in 1922 Compton showed experimentally that collisions between x-rays and electrons obey the relativistic rules of conservation of energy and momentum, assuming Einstein's expressions for the energy and momentum of the photon. With this physicists began to take the wave-particle duality more seriously. In 1924, de~Broglie argued that if light could have both wave and particle aspects, then so might ordinary particles also have wave aspects. This was in part an appeal to the unity of physics, and a suggestion offered by the equivalence of energy and mass, as shown by special relativity. De~Broglie suggested that the formulas $E=\hbar\omega$ and $\pvec=\hbar\kvec$ should apply also to massive particles, giving the frequency and wave vector of a wave associated with the particles. Somewhat later Debye remarked that if there was a wave, there should be a wave equation, and Schr\"odinger, on hearing of this, set out to find it. He first tried a relativistic wave equation without success, only later trying the nonrelativistic version which gave an explanation of the hydrogen spectra and other physical facts. The latter equation is the one usually associated with his name.

A good recent book that covers this history and much else is *Einstein and the Quantum* by A. Douglas Stone.

(sec-spatialdof-13)=

## Properties of the Momentum

We will provisionally accept the definition {eq}`eq-spatialdof-65` of the momentum operator in quantum mechanics, and proceed to examine the consequences. First, the translation operators can now be written in the form,

:::{math}
:label: eq-spatialdof-68
T(\avec) = \exp\Bigl[-{i\over\hbar}(\avec\cdot{\hat{\mathbf{p}}}) \Bigr] = 1 - {i\over\hbar}(\avec\cdot{\hat{\mathbf{p}}}) + \ldots.
:::

The various commutation relations we have evaluated may now be expressed in terms of ${\hat{\mathbf{p}}}$ instead of ${\hat{\mathbf{k}}}$ and gathered together in one place,

:::{math}
:label: eq-spatialdof-69a
\begin{aligned}
[\xhat_i, \xhat_j] &=0,
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-69b
\begin{aligned}
[\xhat_i, \phat_j] &= i\hbar \, \delta_{ij},
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-69c
\begin{aligned}
[\phat_i,\phat_j] &=0.
\end{aligned}
:::

These are the Heisenberg-Born commutation relations. They may be compared to the classical canonical Poisson bracket relations, {eq}`eq-classmech-108`.

Also, the properties {eq}`eq-spatialdof-50` and {eq}`eq-spatialdof-52` of the operators ${\hat{\mathbf{k}}}$ are easily translated into the properties of the momentum. We have

:::{math}
:label: eq-spatialdof-70
{\hat{\mathbf{p}}} \ket{\xvec} = i\hbar \del \ket{\xvec},
:::

and

:::{math}
:label: eq-spatialdof-71
({\hat{\mathbf{p}}}\psi)(\xvec) = -i\hbar \del\psi(\xvec).
:::

{eq}`eq-spatialdof-70` gives the action of the momentum operator in ket language, whereas {eq}`eq-spatialdof-71` gives it in the position representation. It has other forms in other representations. Another form of these equations is

:::{math}
:label: eq-spatialdof-72
\matrixelement{\xvec}{{\hat{\mathbf{p}}}}{\psi} =-i\hbar\del \braket{\xvec}{\psi}.
:::

This is really a rephrasing of {eq}`eq-spatialdof-71`, and can be obtained by taking the Hermitian conjugate of {eq}`eq-spatialdof-70` and then multiplying by the ket $\ket{\psi}$.

(sec-spatialdof-14)=

## The Momentum Representation

Because ${\hat{\mathbf{p}}}$ is a vector of commuting, Hermitian operators, these operators possess a simultaneous eigenbasis. We write the eigenvalue-eigenket problem for momentum in the form,

:::{math}
:label: eq-spatialdof-73
{\hat{\mathbf{p}}} \ket{\pvec} = \pvec \ket{\pvec}.
:::

We solve this in the configuration representation, that is, we multiply {eq}`eq-spatialdof-73` on the left by the bra $\bra{\xvec}$, define the wave function of the momentum eigenket $\ket{\pvec}$ by

:::{math}
:label: eq-spatialdof-74
\psi_\pvec(\xvec) = \braket{\xvec}{\pvec},
:::

and use {eq}`eq-spatialdof-71` to obtain

:::{math}
:label: eq-spatialdof-75
-i\hbar \del \psi_\pvec(\xvec) = \pvec \psi_\pvec(\xvec).
:::

Thus, $\psi_\pvec(\xvec)$ is the eigenfunction of the differential operator $-i\hbar\del$ (really three commuting differential operators) with eigenvalue $\pvec$. The solution exists for all values of $\pvec$ and is unique to within a constant,

:::{math}
:label: eq-spatialdof-76
\psi_\pvec(\xvec) = A e^{i\pvec\cdot\xvec/\hbar},
:::

where $A$ is a normalization and a phase. Thus, momentum has a continuous spectrum, so we normalize the eigenstates according to

:::{math}
:label: eq-spatialdof-77
\braket{\pvec_1}{\pvec_2} = \delta^3(\pvec_1-\pvec_2).
:::

Using the integral

:::{math}
:label: eq-spatialdof-78
\int d^3\xvec \, e^{i(\pvec_2-\pvec_1)\cdot \xvec/\hbar} = (2\pi\hbar)^3 \delta(\pvec_1 - \pvec_2),
:::

the normalization constant $A$ in {eq}`eq-spatialdof-76` is determined to within a phase, which we fix by demanding that $A$ be real and positive. The result is

:::{math}
:label: eq-spatialdof-79
\boxed{\braket{\xvec}{\pvec} = {1 \over (2\pi\hbar)^{3/2}} \, e^{i\pvec\cdot\xvec/\hbar}.}
:::

The eigenfunctions of momentum are plane waves, whose wave length is given by the de~Broglie relation {eq}`eq-spatialdof-66`.

Since the momentum eigenstates are nondegenerate, the momentum operators ${\hat{\mathbf{p}}}$ form a complete set of commuting observables, and we may speak of the *momentum representation*. The resolution of the identity in this representation is

:::{math}
:label: eq-spatialdof-80
1 = \int d^3\pvec \, \ketbra{\pvec}{\pvec}.
:::

We will denote the wave function of the state $\ket{\psi}$ in the momentum representation by

:::{math}
:label: eq-spatialdof-81
\phi(\pvec) = \braket{\pvec}{\psi}
:::

(compare {eq}`eq-spatialdof-15` for the configuration representation), so that by multiplying {eq}`eq-spatialdof-80` onto the ket $\ket{\psi}$ we obtain

:::{math}
:label: eq-spatialdof-82
\ket{\psi} = \int d^3\pvec \, \ket{\pvec} \phi(\pvec),
:::

similar to {eq}`eq-spatialdof-16` in the configuration representation. The wave function $\phi(\pvec)$ is the expansion coefficients of the state $\ket{\psi}$ with respect to the momentum eigenbasis $\{ \ket{\pvec} \}$.

By using {eq}`eq-spatialdof-79` and resolutions of the identity it is easy to switch back and forth between wave functions $\psi(\xvec)$ and $\phi(\pvec)$, representing the same quantum state in two different representations. For example, we have

:::{math}
:label: eq-spatialdof-83
\psi(\xvec) = \braket{\xvec}{\psi} = \int d^3\pvec \, \braket{\xvec}{\pvec} \braket{\pvec}{\psi} = \int {d^3\pvec \over (2\pi\hbar)^{3/2}} \, e^{i\pvec\cdot\xvec/\hbar} \, \phi(\pvec),
:::

and its inverse,

:::{math}
:label: eq-spatialdof-84
\phi(\pvec) = \int {d^3\xvec \over (2\pi\hbar)^{3/2}} \, e^{-i\pvec\cdot\xvec/\hbar} \, \psi(\xvec).
:::

The wave functions $\psi(\xvec)$ and $\phi(\pvec)$ are Fourier transforms of one another, modulo the insertion of factors of $\hbar$ to account for the physical units.

In the momentum representation, the operator ${\hat{\mathbf{p}}}$ is represented simply by multiplication by $\pvec$, the vector of $c$-numbers. That is, if $\phi(\pvec)$ is given in terms of the state $\ket{\psi}$ by {eq}`eq-spatialdof-81`, then the momentum space wave function of the state ${\hat{\mathbf{p}}}\ket{\psi}$ is

:::{math}
:label: eq-spatialdof-85
\matrixelement{\pvec}{{\hat{\mathbf{p}}}}{\psi} = \pvec \braket{\pvec}{\psi} = \pvec \,\phi(\pvec),
:::

where we have allowed ${\hat{\mathbf{p}}}$ to act to the left on the bra $\bra{\pvec}$, bringing out the eigenvalue $\pvec$. We can write this as

:::{math}
:label: eq-spatialdof-86
({\hat{\mathbf{p}}}\phi)(\pvec) = \pvec\phi(\pvec).
:::

Similarly, the operator ${\hat{\mathbf{x}}}$ in the momentum representation is given by

:::{math}
:label: eq-spatialdof-87
({\hat{\mathbf{x}}} \phi)(\pvec) = i\hbar \frac{\partial \phi(\pvec)}{\partial \pvec}.
:::

Compare this to {eq}`eq-spatialdof-71`, and notice the difference in sign. This follows since if $\phi(\pvec)$ is related to $\ket{\psi}$ by {eq}`eq-spatialdof-81`, then what we mean by the left-hand side of {eq}`eq-spatialdof-87` is

:::{math}
\begin{aligned}
\matrixelement{\pvec}{{\hat{\mathbf{x}}}}{\psi} &= \int d^3\xvec \, \braket{\pvec}{\xvec} \matrixelement{\xvec}{{\hat{\mathbf{x}}}}{\psi} = \int {d^3\xvec \over (2\pi\hbar)^{3/2}} \, e^{-i\pvec\cdot\xvec/\hbar} \, \xvec \psi(\xvec)
\end{aligned}
:::

:::{math}
:label: eq-spatialdof-88
\begin{aligned}
&= i\hbar \pop{}{\pvec} \int {d^3\xvec \over (2\pi\hbar)^{3/2}} \, e^{-i\pvec\cdot\xvec/\hbar} \, \psi(\xvec) = i\hbar \frac{\partial \phi(\pvec)}{\partial \pvec}.
\end{aligned}
:::

Finally, we summarize the representations of the operators $\xhat_i$ and $\phat_i$ in the configuration and momentum representations in {ref}`tbl-spatialdof-1`.

:::{list-table} Representations of the operators $\xhat_i$ and $\phat_i$ when acting on configuration and momentum space wave functions. \par
:label: tbl-spatialdof-1
:header-rows: 2

* - 
  - $\xhat_i$
  - $\phat_i$
* - 
  - 
  - 
* - Configuration
  - $\text{mult by } x_i$
  - -$i\hbar\pop{}{x_i}$
* - Momentum
  - $i\hbar\pop{}{p_i}$
  - $\text{mult by } p_i$

:::
(sec-spatialdof-15)=

## Multiparticle Wave Functions

In a system of $N$ particles, the positions of the individual particles are independent observables that commute with one another, so a complete set (ignoring spin for now) consists of the operators $({\hat{\mathbf{x}}}_1, \ldots, {\hat{\mathbf{x}}}_N)$, with eigenvalues $(\xvec_1, \ldots, \xvec_N)$. In this case the wave function is defined by

:::{math}
:label: eq-spatialdof-89
\psi(\xvec_1, \ldots, \xvec_N) = \braket{\xvec_1, \ldots, \xvec_N}{\psi}.
:::

The wave function is defined over configuration space, that is, the space in which a single point specifies the positions of all the particles. This is the same configuration space as in classical mechanics, which is discussed in {ref}`sec-classmech-3`. Configuration space coincides with physical space only in the case of a single particle. Similarly, one can define a multiparticle, momentum space wave function $\phi(\pvec_1, \ldots,\pvec_N)$.

If one is careful about the application of the postulates of quantum mechanics, one will see certain subtleties in the derivation of {eq}`eq-spatialdof-89` in the case of identical particles. We will examine this question more carefully in {ref}`ch-identpart`.

(sec-spatialdof-16)=

## The Sign of $i$

The following is a remark concerning the the definition of ${\hat{\mathbf{k}}}$ in {eq}`eq-spatialdof-30`, which led to the definition of momentum in {eq}`eq-spatialdof-65`. We split off a factor of $i$ in {eq}`eq-spatialdof-30` to make ${\hat{\mathbf{k}}}$ Hermitian, but the same would have been achieved if we had split off $-i$ (thereby changing the definition of ${\hat{\mathbf{k}}}$ by a sign). This would lead to the opposite sign in the definition of ${\hat{\mathbf{p}}}$, and changes in signs in many of the subsequent formulas. Would this change lead to any physical consequences or contradictions with experiment?

The answer is no, but it would change most of the familiar formulas in quantum mechanics, by replacing $i$ by $-i$. For example, a plane wave with wave vector $\kvec$ would become $e^{-i\kvec\cdot\xvec}$ instead of the usual $e^{i\kvec\cdot\xvec}$. It is a matter of convention to choose the sign of $i$ in quantum mechanics, and our choice has been made in {eq}`eq-spatialdof-30` and {eq}`eq-spatialdof-65`. Once this choice has been made, however, then the sign of the Pauli matrix $\sigma_y$ is determined, so that spin angular momentum has the same commutation relations as orbital angular momentum. This was a question addressed in Prob. {ref}`prob-density-2`(d).

(sec-spatialdof-17)=

## The Position-Momentum Uncertainty Relation

The generalized uncertainty relations {eq}`eq-postulat-49`, applied to the case of position $x$ and momentum $p$ of a particle in one-dimension, for which $[x,p]=i\hbar$, give

:::{math}
:label: eq-spatialdof-90
\Delta x\,\Delta p \ge {\hbar\over 2}.
:::

This can be used in a number of applications to obtain quick estimates of orders of magnitude of physical quantities, including three-dimensional problems where for simplicity we ignore the vector nature of $\xvec$ and $\pvec$. We give several examples.

Consider a beam of particles of well defined momentum $\pvec=p_0\, {\hat{\mathbf{z}}}$ directed at a screen in the plane $z=0$. The screen has a hole of dimension $L$ (the hole need not be circular, $L$ is just an order of magnitude estimate of the size of the hole). The hole confines the particles in the $x$- and $y$-directions to a distance of order $L$, so by {eq}`eq-spatialdof-90` the particles acquire a transverse momentum (in the $x$- or $y$-directions) roughly of magnitude

:::{math}
:label: eq-spatialdof-91
p_\perp = {\hbar\over L},
:::

where we drop constants of order unity since this is only an estimate. Thus downstream from the hole the beam should spread at an angle given roughly by

:::{math}
:label: eq-spatialdof-92
\theta = {p_\perp \over p_0} = {\hbar \over Lp_0} = {\lambda\over 2\pi L},
:::

where $\lambda$ is the wave length of the incident waves. This calculation assumes the angle $\theta$ is small, which is equivalent to $\lambda \ll L$, that is, the hole should be at least a few wavelengths in diameter. This very simple estimate of the spreading angle of the beam is confirmed by more complicated calculations of diffraction theory in the far-field (Fraunhofer) region.

If we eliminate all momenta $p$ in favor of wave numbers $k$, by $p=\hbar k$, then all the $\hbar$'s disappear and we have results that can be applied also to classical waves (light waves, sound waves, etc).

For another example, let $a$ be an estimate of the size of a hydrogen atom. The electron is confined to a distance of order $a$ and so must have a momentum of order $p=\hbar/a$. In a circular orbit this implies a centrifugal force of

:::{math}
:label: eq-spatialdof-93
{mv^2\over a} = {p^2\over ma} = {\hbar^2\over ma^3}.
:::

Equating this to the electrostatic force on the electron from the proton, $e^2/a^2$, and solving for $a$, we obtain

:::{math}
:label: eq-spatialdof-94
a = {\hbar^2\over me^2}.
:::

This is the usual expression for the Bohr radius. Given an estimate for the size of an atom and the known density of ordinary matter, one also obtains an estimate for the Avogadro number and many other physical quantities.

(sec-spatialdof-18)=

## Minimum Uncertainty Wave Packets

Let us loosely define a *wave packet* in one dimension as a wave function $\psi(x)$ whose dispersions $\Delta x$ and $\Delta p$, defined as in {ref}`sec-postulat-8` by

:::{math}
:label: eq-spatialdof-95
\begin{aligned}
(\Delta x)^2 &= \xpecval{\xhat^2} - \xpecval{\xhat}^2, \\
(\Delta p)^2 &= \xpecval{\phat^2} - \xpecval{\phat}^2, \\

\end{aligned}
:::

are small, that is, close to the minimum values allowed by the inequality,

:::{math}
:label: eq-spatialdof-96
\Delta x \Delta p \ge {\hbar\over 2}.
:::

See {eq}`eq-postulat-50`. Similarly, let us define a *minimum uncertainty wave packet* as one for which the product $\Delta x \Delta p$ takes on its minimum value of $\hbar/2$.

Let $\psi(x)$ be a normalized, minimum uncertainty wave packet with

:::{math}
:label: eq-spatialdof-97
\begin{aligned}
\matrixelement{\psi}{\xhat}{\psi} &= \xpecval{\xhat} =0, \\
\matrixelement{\psi}{\phat}{\psi} &= \xpecval{\phat} =0, \\

\end{aligned}
:::

and let $\Delta x = L$, so that $\Delta p = \hbar/2L$. Now let

:::{math}
:label: eq-spatialdof-98
\ket{\zeta} = \Bigl(\xhat + {2iL^2\over\hbar}\phat\Bigr) \ket{\psi}.
:::

The operator appearing on the right seems to have been pulled out of the air, but it is a version of an annihilation operator of the general form $\xhat+i\phat$, with coefficients adjusted to make the following argument come out right. We will see such annihilation operators again when we discuss the harmonic oscillator. Now squaring {eq}`eq-spatialdof-98`, we obtain

:::{math}
:label: eq-spatialdof-99
\braket{\zeta}{\zeta} = \xpecval{\xhat^2} +{2iL^2 \over \hbar} \xpecval{\xhat\phat-\phat\xhat} + {4L^4\over\hbar^2} \xpecval{\phat^2} = L^2 - 2L^2 + L^2 = 0.
:::

This implies $\ket{\zeta}=0$ (see {eq}`eq-hilbert-27`, so {eq}`eq-spatialdof-98` in wave function language becomes

:::{math}
:label: eq-spatialdof-100
2L^2 \dod{\psi}{x} + x\psi=0,
:::

which has the normalized solution,

:::{math}
:label: eq-spatialdof-101
\psi(x) = {1\over{\sqrt{L\sqrt{2\pi}}}}\, e^{-x^2/4L^2}.
:::

The minimum uncertainty wave packet is a Gaussian. If we allow $\xpecval{\xhat}=a$ and $\xpecval{\phat}=b$ to take on arbitrary values $a$, $b$ as shown, then we find

:::{math}
:label: eq-spatialdof-102
\psi(x) = {1\over{\sqrt{L\sqrt{2\pi}}}} \exp\Bigl[ -{(x-a)^2 \over 4L^2} + i{b(x-a) \over \hbar} + i\gamma\Bigr],
:::

where $\gamma$ is a phase. The wave packet is still a Gaussian, but it has been shifted in position and momentum.

\problems

(prob-spatialdof-1)=

**Problem \prbdspatialdof-1.} Let $\ket{\psi}$ be the state of a spinless particle in three dimensions, and let $\phi(\pvec) = \braket{\pvec}{\psi}$ be its momentum space wave function.  Find the momentum space wave function of the state $T(\avec)\ket{\psi.** 

(prob-spatialdof-2)=

**Problem \prbdspatialdof-2..** 

A question that has exercised various people is the relation between classical observables (that is, functions of }$x$ and $p$) and quantum observables (that is, functions of $\xhat$ and $\phat$). One problem is to *quantize* a classical observable, that is, given a classical function $A(x,p)$, what is the corresponding quantum observable? Dirac suggested that $x$ and $p$ should be associated with $\xhat$ and $\phat$, but this gives rise to an ambiguity in cases like the classical function $xp$. Should it correspond to $\xhat\phat$ or to $\phat\xhat$, or maybe to their average (which at least would be Hermitian)?

Another answer to this question was given by Weyl. We introduce the Weyl transform in this problem because it is good exercise in the position and momentum representations.

We denote operators with a hat, as in $\hat x$ or $\hat A$, and we denote eigenvalues or classical quantities without a hat, as in $x$ or $A(x,p)$. We work in one dimension, and think of a wave function $\psi(x)$ or $\psi(x,t)$.

If $\hat A$ is an operator, we define the {\sl Weyl transform} of $\hat A$, denoted $A(x,p)$, by

:::{math}
:label: eq-spatialdof-103
A(x,p) = \int_{-\infty}^{+\infty} ds \, e^{-ips/\hbar} \, \matrixelement{x+s/2}{\hat A}{x-s/2}.
:::

Here the notation $\ket{x-s/2}$, for example, means the eigenket of $\hat x$ with eigenvalue $x-s/2$. It is useful to think of $A(x,p)$ as a function defined on the classical $(x,p)$ phase space which is in some sense the classical observable corresponding to the quantum operator $\hat A$.

\problempart{(a)} Show that if $A(x,p)$ is the Weyl transform of operator $\hat A$, then $A(x,p)^\cc$ is the Weyl transform of $\hat A^\hc$. In particular, this shows that the Weyl transform of a Hermitian operator is a real function on phase space.

\problempart{(b)} Show that if operators $\hat A$ and $\hat B$ have Weyl transforms $A(x,p)$ and $B(x,p)$, respectively, then

:::{math}
:label: eq-spatialdof-104
\tr(\hat A^\hc \hat B) = \int {dx\,dp \over 2\pi\hbar} \, A(x,p)^\cc B(x,p).
:::

Notice how the right hand side looks like the “scalar product” of two classical observables on phase space.

\problempart{(c)} Find the Weyl transforms of the following operators: $1$ (the identity operator); $\hat x$; $\hat p$; $\hat x \hat p$; $\hat p \hat x$; $\hat p^2/2m + V(\hat x)$.

\problempart{(d)} The classical probability density $\rho(x,p)$ in phase space (see {ref}`sec-classmech-24`) describes a system whose dynamical state can only be described statistically. Since $\rho(x,p)$ is a probability density, it is nonnegative, $\rho(x,p)\ge0$, and it is normalized,

:::{math}
:label: eq-spatialdof-105
\int \rho(x,p)\,dx\,dp=1.
:::

The probability density in $x$ alone (call it $F(x)$) or in $p$ alone (call it $G(p)$) is obtained by integrating $\rho$ over the other variable ($p$ or $x$),

:::{math}
:label: eq-spatialdof-106
\int \rho(x,p)\,dp = F(x), \qquad \int \rho(x,p)\,dx = G(p),
:::

and each of these is normalized,

:::{math}
:label: eq-spatialdof-107
\int F(x)\,dx=1, \qquad \int G(p)\,dp=1.
:::

The functions $F(x)$ or $G(p)$ are called *marginal distributions* in statistics.

It turns out that the Weyl transform $W(x,p)$ of the density operator $\hat\rho$ in quantum mechanics is very similar in its properties to the classical probability density $\rho(x,p)$. The function $W(x,p)$ is called the *Wigner function*. Because $\hat\rho$ is Hermitian, the Wigner function is real.

For simplicity let us work with a pure state, so $\hat\rho=\ketbra{\psi}{\psi}$. Express the marginal distribution

:::{math}
:label: eq-spatialdof-108
\int W(x,p)\,dp
:::

in terms of the wave function $\psi(x)$. Now let $\phi(p)$ be the momentum space wave function, and express the marginal distribution

:::{math}
:label: eq-spatialdof-109
\int W(x,p)\,dx
:::

in terms of $\phi(p)$. What is the normalization integral,

:::{math}
:label: eq-spatialdof-110
\int W(x,p)\,dx\,dp?
:::

These results suggest that $W(x,p)$ is a distribution function of particles in phase space whose statistics reproduces the statistics inherent in quantum measurement, apart from the normalization. Unlike a classical distribution function $\rho(x,p)$, however, $W(x,p)$ can take on negative values. These “negative probabilities” have no meaning in any statistical sense, but they only arise, in a certain sense, when we attempt to measure $x$ and $p$ simultaneously to a precision greater than that allowed by the uncertainty principle. The Wigner function can be used to express quantum statistical mechanics in a manner that is surprisingly similar to classical statistical mechanics, but one which is still fully quantum mechanical.

(prob-spatialdof-3)=

**Problem \prbdspatialdof-3.} Given that the range of the nuclear forces is approximately $10^{-13}$~cm, estimate the velocity of the proton or neutron in a deuteron (a bound state of a proton and a neutron). Compare this $v/c$ to the $v/c$ of the electron in the ground state of hydrogen.  It is believed that nuclear forces are independent of the charge state of the nucleon; thus, two protons should feel the same nuclear force as two neutrons.  Calculate the nuclear force between two protons at a distance of $10^{-13.** 

(prob-spatialdof-4)=

**Problem \prbdspatialdof-4..** 

(prob-spatialdof-5)=

**Problem \prbdspatialdof-5.} The Large Hadron Collider is designed to reach an energy of 7~TeV ($7\times 10^{12.**
