---
title: "12. Rotations in Quantum Mechanics, and Rotations of Spin-1/2 Systems"
---
(ch-spinrot)=

# 12. Rotations in Quantum Mechanics, and Rotations of Spin-1/2 Systems

(sec-spinrot-1)=

## Introduction

In these notes we develop a general strategy for finding unitary operators to represent rotations in quantum mechanics, and we work through the specific case of rotations in spin-$\frac{1}{2}$ systems. We find that the relation between spin-$\frac{1}{2}$ rotations and classical rotations is two-to-one, due to the appearance of non-classical phase factors. In a certain sense spin-$\frac{1}{2}$ rotations constitute a basic building block in the theory of rotations in quantum mechanics, out of which rotations for an arbitrary system can be constructed. The general theory of rotations in quantum mechanics will be developed in later sets of notes.

(sec-spinrot-2)=

## Physical Meaning of Rotations in Quantum Mechanics

In classical mechanics, we can rotate the state of a dynamical system, that is, we can rotate all the position and velocity vectors $(\rvec,\vvec)$ for each particle, to create a new or rotated state. Similarly, in quantum mechanics, given a state $\ket{\psi}$ (taken for simplicity to be pure), it is possible to define a rotated state such that the expectation values of all vector operators in the rotated state are rotated relative to the expectation values in the original state, exactly as classical vectors would transform under rotations in a classical system. The transformation between the original quantum state $\ket{\psi}$ and the rotated quantum state is brought about by means of a certain rotation operator, which is unitary because probabilities must be preserved under rotations.

What does it mean physically to rotate a quantum state? Certainly we cannot go in with a wrench, and rotate the wave function of the electrons in an atom, or rotate the spins of those electrons. In any case, as we have emphasized, the wave function represents the properties of an ensemble of systems, not an individual system, so rotating a quantum state must be equivalent to rotating the properties of the ensemble. One point of view is to identify a quantum state with the apparatus that prepares the ensemble of systems about which the quantum state makes statistical predictions. We can certainly rotate a preparation apparatus, and it is logical to regard the state prepared by the rotated apparatus as the rotated state. This point of view gives us a definition of a rotated state, without however specifying the phase of that state.

Alternatively, quantum systems may experience rotations as a result of their time evolution. For example, many small molecules are approximately rigid bodies, and their time evolution is approximately given by a time-dependent rotation operator, just as the time evolution of a classical rigid body is specified by a time-dependent rotation $\Rmat(t)$ (see {ref}`sec-classrot-12`). For another example, spins in magnetic fields evolve by means of a time-dependent rotation operator. The magnetic field can either be external or internal; for example, the electrons in an atom precess in the magnetic field of the nucleus (which is a moving charge in the electron rest frame, and which may have an intrinsic magnetic field of its own). Or the magnetic field may be external, permitting experimental control over the orientation of spins. Another example of rotations in quantum mechanics is produced by Thomas precession, a relativistic but purely inertial effect that rotates all the dynamical variables of an accelerated system, for example, the spin of an electron in an orbit in an atom. Different subsystems of a given system may be rotated by different amounts, for example, it is possible to change the orientation of a molecule without rotating its spins (hit it with another molecule), or vice versa (apply a magnetic field). Thus we speak of spatial rotation operators, spin rotation operators, etc.

The phases associated with rotations are observable. For example, in a neutron interferometer, it is possible to split a beam of neutrons into two, and to subject one of the two resulting beams to a magnetic field, which will rotate the neutron spins. By recombining the beams and observing the interference pattern, phase shifts such as the $-1$ multiplicative factor that occurs on rotating a spin-$\frac{1}{2}$ system by $2\pi$ can be observed. This is a rather direct observation of a phase shift, but phases also enter into quantization conditions (recall the Bohr-Sommerfeld rules), and theoretical predictions of energy levels would not agree with experiment if all phases were not accounted for correctly.

(sec-spinrot-3)=

## Postulates for Rotation Operators

Suppose we have some quantum mechanical system, and an associated Hilbert space of states. We will be interested in finding operators that act on these states that represent the action of rotations at the classical level. If a classical rotation is specified by a rotation matrix $\Rmat$ (relative to some inertial frame), then we will denote the associated operator by $U(\Rmat)$. For the time being we will work only with proper rotations, so that $\Rmat\in SO(3)$. We will denote the association itself by

:::{math}
:label: eq-spinrot-1
\Rmat \mapsto U(\Rmat),
:::

which simply means that $U$ is a function of the classical rotation $\Rmat$.

As you might imagine, the specific form of the operators $U(\Rmat)$ depends on the system, but it turns out that there is a great deal that can be said about these operators without going into the specific nature of the system. These are the properties of rotation operators that follow from the properties of classical rotations, that is, ultimately from the Euclidean geometry of three-dimensional space. We will concentrate on these properties first, and then deal with specific physical systems (spin systems, central force problems, atoms, etc) which are treated in later sets of notes.

We make a series of reasonable assumptions or postulates that the rotation operators $U(\Rmat)$ should satisfy. First, these operators should be unitary, because a symmetry operation should preserve probabilities:

:::{math}
:label: eq-spinrot-2
U(\Rmat)^{-1} = U(\Rmat)^\dagger.
:::

Next, we assume that when the classical rotation is the identity, so is the unitary operator,

:::{math}
:label: eq-spinrot-3
U(\Imat) =1.
:::

Finally, we assume that the unitary operator corresponding to the product of two rotations is the product of the unitary operators, so that

:::{math}
:label: eq-spinrot-4
U(\Rmat_1)U(\Rmat_2) = U(\Rmat_1\Rmat_2).
:::

This means that the unitary operators $U(\Rmat)$ reproduce the multiplication law of classical rotations. These requirements imply that inverse rotations are mapped into inverse unitary operators,

:::{math}
:label: eq-spinrot-5
U(\Rmat^{-1}) = U(\Rmat)^{-1} = U(\Rmat)^\hc.
:::

If the requirements {eq}`eq-spinrot-2` to {eq}`eq-spinrot-5` are satisfied, then we say that $U(\Rmat)$ (more precisely, the mapping {eq}`eq-spinrot-1`) forms a *representation* of $SO(3)$ by means of unitary operators. As we will see, these requirements are actually too strong, and in the case of systems of half-integral spin, they cannot be met; for such systems we can almost find a representation, but we ultimately fail because of phase factors. However, the search for a unitary representation of the classical rotations is educational, and the phase factors are not so much a difficulty as an opportunity for obtaining a deeper understanding of rotations, and for finding new physics at the quantum level.

In addition to the mathematical requirements given by {eq}`eq-spinrot-3` to {eq}`eq-spinrot-5`, the operators $U(\Rmat)$ must also satisfy physical properties we expect of rotations. For example, the expectation values of vector operators should transform as classical vectors.

(sec-spinrot-4)=

## Representations of Near-Identity Rotations

The key to finding a unitary representation of the rotations is to begin with near-identity rotations. First, some notation. We notice that a rotation in axis-angle form actually depends only on the product $\theta{\hat{\mathbf{n}}}$ of the axis and the angle,

:::{math}
:label: eq-spinrot-6
\Rmat({\hat{\mathbf{n}}},\theta) = e^{\theta {\hat{\mathbf{n}}}\cdot\Jmatvec},
:::

so we introduce a vector of angles $\thetavec$ defined by

:::{math}
:label: eq-spinrot-7
\thetavec=\theta {\hat{\mathbf{n}}},
:::

and write $\Rmat(\thetavec)$ for the rotation. Now if the rotation is near-identity, we can approximate it by the leading terms of the exponential series,

:::{math}
:label: eq-spinrot-8
\Rmat(\thetavec) = \Imat + \thetavec\cdot\Jmatvec + \ldots,
:::

which is {eq}`eq-classrot-32`. This implies that

:::{math}
:label: eq-spinrot-9
\Jmat_k = \left. \frac{\partial \Rmat(\thetavec)}{\partial \theta_k} \right|_{\thetavec=0},
:::

for $k=1,2,3$.

The unitary operator that corresponds to the rotation $\Rmat(\thetavec)$ can also be parameterized by $\thetavec$, so we will write $U(\thetavec)=U\bigl(\Rmat(\thetavec)\bigr)$. In the case of small angles, we can approximate $U(\thetavec)$ by the leading terms of its Taylor series,

:::{math}
:label: eq-spinrot-10
U(\thetavec) = 1 + \sum_k \left.\frac{\partial U(\thetavec)}{\partial \theta_k} \right|_{\thetavec=0} \theta_k + \ldots,
:::

where the first term is 1 (the identity operator) because of {eq}`eq-spinrot-3`. At this point you may wish to review the manner in which we defined linear momentum $\pvec$ as the generator of translations in {ref}`ch-spatialdof`, or the manner in which we defined the Hamiltonian in {ref}`ch-tevolut`. See especially {eq}`eq-spatialdof-30`, {eq}`eq-spatialdof-65`, {eq}`eq-tevolut-6` and {eq}`eq-tevolut-8`. Following the pattern of those definitions, we now define the *angular momentum* of the quantum system as the vector operator $\Jvec$ with components $J_k$ given by

:::{math}
:label: eq-spinrot-11
J_k = i\hbar \left.\frac{\partial U(\thetavec)}{\partial \theta_k} \right|_{\thetavec=0}.
:::

This defines $\Jvec$ relative to some definition for the unitary rotation operators $U(\Rmat)$, so different systems, with different definitions of rotation operators, will have different definitions of the angular momentum (for some it will be orbital angular momentum, for others,spin, etc). This definition of angular momentum allows us to write a near-identity rotation as

:::{math}
:label: eq-spinrot-12
U(\thetavec) = 1 -{i\over\hbar} \thetavec\cdot\Jvec + \ldots.
:::

We split off a factor of $i$ in the definition of $J_k$ in {eq}`eq-spinrot-11` so that the operators $J_k$ will be Hermitian, because in quantum mechanics we think of Hermitian operators as the generators of unitary operators. The Hermiticity of $J_k$ follows by substituting {eq}`eq-spinrot-12` into $U(\thetavec)U(\thetavec)^\dagger =1$ (exactly as we proved the Hermiticity of the operator $\khat$ in {ref}`sec-spatialdof-5`). As for the factor of $\hbar$, it makes $J_k$ have dimensions of angular momentum.

Reverting now to our original axis-angle notation, we can write the near-identity rotation operator as

:::{math}
:label: eq-spinrot-13
U({\hat{\mathbf{n}}},\theta) = 1 -{i\over\hbar} \theta{\hat{\mathbf{n}}}\cdot\Jvec + \ldots.
:::

Since the operators $\Jvec$ were defined in terms of $U(\Rmat)$, this is not an explicit solution for the rotation operators $U$, even for infinitesimal rotations. But at least is shows how those rotation operators depend on the axis and angle, which is progress. Note that $\Jvec$ is a fixed set of three Hermitian operators that are independent of the axis or angle. In a moment we will extend this relation to arbitrary angles.

When defining the angular momentum in quantum mechanics, we have some of the same issues we faced earlier when trying to define linear momentum in quantum mechanics by taking over some definition from classical mechanics. In the case of linear momentum, we decided that the role that linear momentum plays in classical mechanics as the generator of translations was the most fundamental role; this supersedes definitions such as $\pvec=m\vvec$, which are not as general. Similarly, in quantum mechanics, we will define the angular momentum as the generator of rotations, rather than as $\rvec\cross\pvec$, which is not as general. For not only is $\rvec\cross\pvec$ meaningless for systems such as spin systems, but even for the spatial degrees of freedom of a spinless particle, it is not always true that the generator of rotations is $\rvec\cross\pvec$ (for example, in the presence of magnetic fields). We take the generator of rotations to be the most fundamental role of angular momentum, because, among other reasons, these generators (the components of $\Jvec$) are conserved in systems with rotational symmetry. Moreover, the generality of our definition allows us to treat the angular momentum of orbital motion, spin systems, systems in magnetic fields, multiparticle systems, relativisitic systems and quantum fields under the same formalism.

(sec-spinrot-5)=

## Rotation Operators for Any Angle

The relation {eq}`eq-spinrot-13`, which gives $U({\hat{\mathbf{n}}},\theta)$ when $\theta$ is small, can be extended to a closed formula valid for any $\theta$. The pattern follows what we did earlier with translation operators in {ref}`sec-spatialdof-5` and with classical rotations in {ref}`sec-classrot-9`. We begin by seeking a differential equation for $U({\hat{\mathbf{n}}},\theta)$. By the definition of the derivative,

:::{math}
:label: eq-spinrot-14
\dod{U({\hat{\mathbf{n}}},\theta)}{\theta} = \lim_{\epsilon\to 0} {U({\hat{\mathbf{n}}},\theta+\epsilon) -U({\hat{\mathbf{n}}},\theta) \over \epsilon}.
:::

But since the operators $U({\hat{\mathbf{n}}},\theta)$ form a representation of the classical rotations $\Rmat({\hat{\mathbf{n}}},\theta)$ [see {eq}`eq-spinrot-4`] and since rotations about a fixed axis commute [see {eq}`eq-classrot-17`], we have

:::{math}
:label: eq-spinrot-15
U({\hat{\mathbf{n}}},\theta+\epsilon) = U({\hat{\mathbf{n}}},\epsilon) U({\hat{\mathbf{n}}},\theta),
:::

and the numerator in {eq}`eq-spinrot-14` has a common factor of $U({\hat{\mathbf{n}}},\theta)$ that can be taken out to the right. Thus we have

:::{math}
:label: eq-spinrot-16
\dod{U({\hat{\mathbf{n}}},\theta)}{\theta} = \lim_{\epsilon\to 0} \left( {U({\hat{\mathbf{n}}},\epsilon) -1 \over \epsilon} \right) U({\hat{\mathbf{n}}},\theta).
:::

The remaining limit can be evaluated in terms of the angular momentum $\Jvec$ with the aid of {eq}`eq-spinrot-13`, where the small angle $\theta$ of that formula is identified with $\epsilon$ here. This gives the differential equation,

:::{math}
:label: eq-spinrot-17
\dod{U({\hat{\mathbf{n}}},\theta)}{\theta} = -{i\over\hbar} ({\hat{\mathbf{n}}}\cdot\Jvec) U({\hat{\mathbf{n}}},\theta).
:::

Subject to the initial condition $U({\hat{\mathbf{n}}},0)=1$, this has the unique solution,

:::{math}
:label: eq-spinrot-18
U({\hat{\mathbf{n}}},\theta) = \exp\Bigl( -{i\over\hbar} \theta {\hat{\mathbf{n}}}\cdot\Jvec \Bigr).
:::

This solution can also be obtained as the limit of the product of a large number of small angle rotations, as in {ref}`sec-classrot-9` [see {eq}`eq-classrot-42`--{eq}`eq-classrot-43`].

{eq}`eq-spinrot-18` shows that we can find the rotation operators $U({\hat{\mathbf{n}}},\theta)$ corresponding to the classical rotations $R({\hat{\mathbf{n}}},\theta)$ once we know the angular momentum operators $\Jvec$. This greatly simplifies the problem, because there are only three angular momentum operators, but an infinite family of rotation operators. The angular momentum operators are not arbitrary, however; in addition to being Hermitian, they must satisfy certain commutation relations.

(sec-spinrot-6)=

## Commutation Relations for Angular Momentum

Let us consider the rotation $\Cmat$ defined in {eq}`eq-classrot-63`, and its unitary representative $U(\Cmat)$. We have

:::{math}
:label: eq-spinrot-19
U(\Cmat) = U(\Rmat_1)U(\Rmat_2)U(\Rmat_1^{-1}) U(\Rmat_2^{-1}).
:::

Let us expand both sides of this equation in a Taylor series in the angles $\theta_1$ and $\theta_2$, defined by $\Rmat_1=\Rmat({\hat{\mathbf{n}}}_1, \theta_1)$ and $\Rmat_2 = \Rmat({\hat{\mathbf{n}}}_2,\theta_2)$. The answer can be obtained in two ways. In one approach, we expand the exponentials for $U(\Rmat_1)$, $U(\Rmat_2)$, etc., according to {eq}`eq-spinrot-18`, and multiply the series. This gives

:::{math}
:label: eq-spinrot-20
\begin{aligned}
U(\Cmat) &= \Bigl[1-{i\theta_1\over\hbar}({\hat{\mathbf{n}}}_1\cdot\Jvec) -{\theta_1^2\over 2\hbar^2}({\hat{\mathbf{n}}}_1\cdot\Jvec)^2 + \ldots\Bigr] \Bigl[1-{i\theta_2\over\hbar}({\hat{\mathbf{n}}}_2\cdot\Jvec) -{\theta_2^2\over 2\hbar^2}({\hat{\mathbf{n}}}_2\cdot\Jvec)^2 + \ldots\Bigr] \\
&\times \Bigl[1+{i\theta_1\over\hbar}({\hat{\mathbf{n}}}_1\cdot\Jvec) -{\theta_1^2\over 2\hbar^2}({\hat{\mathbf{n}}}_1\cdot\Jvec)^2 + \ldots\Bigr] \Bigl[1+{i\theta_2\over\hbar}({\hat{\mathbf{n}}}_2\cdot\Jvec) -{\theta_2^2\over 2\hbar^2}({\hat{\mathbf{n}}}_2\cdot\Jvec)^2 + \ldots\Bigr]. \\

\end{aligned}
:::

The calculation is similar to that in {eq}`eq-classrot-64` leading to {eq}`eq-classrot-65`. When the series are multiplied, first order terms vanish, but at second order the product becomes

:::{math}
:label: eq-spinrot-21
U(\Cmat) = 1-{1\over\hbar^2} \theta_1\theta_2 [{\hat{\mathbf{n}}}_1\cdot\Jvec, {\hat{\mathbf{n}}}_2\cdot\Jvec] + \ldots.
:::

On the other hand, according to {eq}`eq-classrot-66`, $\Cmat$ is a near-identity rotation with axis ${\hat{\mathbf{m}}}$ and angle $\phi$, $\Cmat=\Imat +\phi{\hat{\mathbf{m}}}\cdot\Jmatvec$, where ${\hat{\mathbf{m}}}$ and $\phi$ are given by {eq}`eq-classrot-67`. Therefore

:::{math}
:label: eq-spinrot-22
U(\Cmat) = 1-{i\phi\over\hbar} {\hat{\mathbf{m}}}\cdot\Jvec + \ldots =1-{i\over\hbar}\theta_1\theta_2 ({\hat{\mathbf{n}}}_1\cross{\hat{\mathbf{n}}}_2) \cdot\Jvec + \ldots,
:::

where we use {eq}`eq-classrot-67`. This is consistent with {eq}`eq-spinrot-21` only if

:::{math}
:label: eq-spinrot-23
[{\hat{\mathbf{n}}}_1\cdot\Jvec, {\hat{\mathbf{n}}}_2\cdot\Jvec] = i\hbar ({\hat{\mathbf{n}}}_1\cross{\hat{\mathbf{n}}}_2)\cdot \Jvec.
:::

By setting ${\hat{\mathbf{n}}}_1$ and ${\hat{\mathbf{n}}}_2$ to ${\hat{\mathbf{x}}}$, ${\hat{\mathbf{y}}}$, ${\hat{\mathbf{z}}}$, we obtain

:::{math}
:label: eq-spinrot-24
\boxed{[J_i,J_j] = i\hbar\, \epsilon_{ijk} \, J_k.}
:::

These are the standard commutation relations for angular momentum in quantum mechanics, here extracted from the properties of rotation operators. These commutation relations are the quantum analogs of the classical commutation relations {eq}`eq-classrot-34` for the $\Jmat$ matrices; the two commutation relations are the same, apart from conventional factors of $i$ and $\hbar$.

The usual approach to deriving the angular momentum commutation relations {eq}`eq-spinrot-24` in elementary courses in quantum mechanics is to work with the specific example of orbital angular momentum, whose definition $\Lvec = \rvec \cross \pvec$ is taken over from classical mechanics. One then just works out the commutators of the components of $\Lvec$, and argues that other forms of angular momentum such as spin ought to have the same commutation relations. Here we have derived the angular momentum commutation relations in all generality, following from the properties of rotations. The specific case of orbital angular momentum $\Lvec$ will be dealt with in {ref}`ch-orbamsph`.

We have shown that the only way the unitary operators $U$ can reproduce the multiplication law for the classical rotations $\Rmat$ is if the infinitesimal generators in each case satisfy the same commutation relations, apart from conventional factors of $i$ and $\hbar$. Therefore we adopt the following strategy in developing the general theory of the representations of classical rotations. We begin by seeking the most general form that a vector of Hermitian operators $\Jvec$ can take, given that it satisfies the commutation relations {eq}`eq-spinrot-24`. For example, we will be interested in the matrices that represent these operators in some appropriately chosen basis. When we have found specific operators $\Jvec$ that satisfy the commutation relations {eq}`eq-spinrot-24`, we will say that we have found a *representation* of those commutation relations. Next, given some such operators $\Jvec$, we exponentiate linear combinations of them as in {eq}`eq-spinrot-18`, to obtain the unitary rotation operators $U({\hat{\mathbf{n}}},\theta)$. These can also be represented as matrices in some basis. Finally, we explore the physical implications of these operators, to guarantee that they have the physical properties we expect of rotations.

(sec-spinrot-7)=

## Angular Momentum and Rotation Operators for Spin-$\frac{1}{2}$ Systems

Thus, we must begin by finding a representation of the angular momentum commutation relations {eq}`eq-spinrot-24`. We will take up the general problem of doing this in {ref}`ch-repsamos`; for the remainder of these notes, however, we will restrict consideration to a spin-$\frac{1}{2}$ system, which possesses a 2-dimensional ket space. To find operators $\Jvec$ acting on this space that satisfy the commutation relations {eq}`eq-spinrot-24`, we simply notice that

:::{math}
:label: eq-spinrot-25
\Jvec = {\hbar\over2} \sigmavec
:::

will do the trick. This is because of the commutation relations for the Pauli matrices,

:::{math}
:label: eq-spinrot-26
[\sigma_i,\sigma_j] = 2i\,\epsilon_{ijk}\,\sigma_k.
:::

Therefore we provisionally take the rotation operators to be

:::{math}
:label: eq-spinrot-27
U({\hat{\mathbf{n}}},\theta) = e^{-i \theta{\hat{\mathbf{n}}}\cdot\sigmavec/2} =\cos{\theta\over2} - i({\hat{\mathbf{n}}}\cdot\sigmavec) \sin{\theta\over2},
:::

where we use the standard properties of the Pauli matrices to reexpress the Taylor series for the exponential in terms of trigonometric functions (see Prob. {ref}`prob-hilbert-1`).

The identification of the operators $U({\hat{\mathbf{n}}},\theta)$ with rotations is provisional because we must show that these operators make physical sense as rotations. For example, let us consider the Stern-Gerlach experiment, in which we measure the components of the magnetic moment vector $\muvec$. We showed earlier that the operators corresponding to the components of $\muvec$, when represented in an eigenbasis of $\mu_z$ with appropriate phase conventions, produce matrices proportional to the Pauli matrices $\sigmavec$. Therefore, since we expect $\muvec$ transform as a vector under rotations, so should $\sigmavec$. This means that if we have an (old) state $\ket{\psi}$, and a new or rotated state $\ket{\psi'}=U({\hat{\mathbf{n}}},\theta)\ket{\psi}$, then we expect that the expectation values of $\sigmavec$ in the old and new states should be related by the classical rotation $\Rmat({\hat{\mathbf{n}}},\theta)$. In other words, we should have

:::{math}
:label: eq-spinrot-28
\matrixelement{\psi'}{\sigmavec}{\psi'} = \matrixelement{\psi}{U^\hc \sigmavec U}{\psi} = \Rmat \matrixelement{\psi}{\sigmavec}{\psi},
:::

or, since this must hold for all $\ket{\psi}$,

:::{math}
:label: eq-spinrot-29
U^\hc \sigmavec U = \Rmat \sigmavec,
:::

where it is understood that $U=U({\hat{\mathbf{n}}},\theta)$ and $\Rmat=\Rmat({\hat{\mathbf{n}}},\theta)$. In case {eq}`eq-spinrot-29` it not clear, we write it out in components,

:::{math}
:label: eq-spinrot-30
U^\hc \sigma_i U = \sum_j R_{ij}\sigma_j.
:::

To see if {eq}`eq-spinrot-29` is true, we simply substitute {eq}`eq-spinrot-27` to obtain

:::{math}
\begin{aligned}
U^\hc \sigmavec U &= \Bigl[ \cos{\theta\over2} + i({\hat{\mathbf{n}}}\cdot\sigmavec)\sin{\theta\over 2}\Bigr] \sigmavec \Bigl[\cos{\theta\over2} - i({\hat{\mathbf{n}}}\cdot\sigmavec) \sin{\theta\over2} \Bigr]
\end{aligned}
:::

:::{math}
:label: eq-spinrot-31
\begin{aligned}
&= \cos^2{\theta\over 2} \sigmavec + i\cos{\theta\over2} \sin{\theta\over2} \bigl[{\hat{\mathbf{n}}}\cdot\sigmavec,\sigmavec \bigr] + ({\hat{\mathbf{n}}}\cdot\sigmavec) \sigmavec ({\hat{\mathbf{n}}}\cdot\sigmavec) \sin^2{\theta\over2}.
\end{aligned}
:::

Next we use the properties of the Pauli matrices to derive the identities,

:::{math}
:label: eq-spinrot-32
\bigl[ {\hat{\mathbf{n}}}\cdot\sigmavec,\sigmavec\bigr] = -2i \, {\hat{\mathbf{n}}}\cross\sigmavec, \qquad ({\hat{\mathbf{n}}}\cdot\sigmavec)\sigmavec({\hat{\mathbf{n}}}\cdot\sigmavec) = 2{\hat{\mathbf{n}}}({\hat{\mathbf{n}}}\cdot\sigmavec) -\sigmavec,
:::

which we use to rewrite {eq}`eq-spinrot-31` in the form,

:::{math}
:label: eq-spinrot-33
U^\hc \sigmavec U = \cos\theta \, \sigmavec + (1-\cos\theta){\hat{\mathbf{n}}}({\hat{\mathbf{n}}}\cdot\sigmavec) + \sin\theta \, {\hat{\mathbf{n}}}\cross\sigmavec.
:::

Finally, by comparing this with {eq}`eq-classrot-44`, we see that {eq}`eq-spinrot-29` is verified. Encouraged by this result, we henceforth consider the operators $U({\hat{\mathbf{n}}},\theta)$ defined by {eq}`eq-spinrot-27` to be rotation operators for spin-$\frac{1}{2}$ systems.

(sec-spinrot-8)=

## The Spin-$\frac{1}{2}$ Adjoint Formula

Before leaving the result {eq}`eq-spinrot-29`, however, we will comment on it further, since it is useful in its own right. In fact, this result is a spinor version of the adjoint formula {eq}`eq-classrot-48`, which we derived earlier for classical rotations. To see the analogy more clearly, we first replace $U$ by $U^{-1}=U^\hc$ and $\Rmat$ by $\Rmat^{-1}=\Rmat^t$ in {eq}`eq-spinrot-29`, so that

:::{math}
:label: eq-spinrot-34
\boxed{ U\sigmavec U^\hc = \Rmat^{-1}\sigmavec.}
:::

Next we dot both sides by some vector $\avec$, and use {eq}`eq-classrot-72` to obtain

:::{math}
:label: eq-spinrot-35
U(\avec\cdot\sigmavec)U^\hc = (\Rmat\avec)\cdot\sigmavec.
:::

This may be compared to the adjoint formula {eq}`eq-classrot-48` for classical rotations, which we reproduce here with a slight change of notation:

:::{math}
:label: eq-spinrot-36
\Rmat(\avec\cdot\Jmatvec)\Rmat^t=(\Rmat\avec)\cdot\Jmatvec.
:::

We will refer to {eq}`eq-spinrot-34` or its variants as the adjoint formula for spinor rotations.

(sec-spinrot-9)=

## The Double-Valued Representation

We seem to be in good shape for the interpretation of the operators $U({\hat{\mathbf{n}}},\theta)$ as spinor rotations. There is, however, one wrinkle, which we find upon looking at specific examples of rotations. In particular, if we rotate a spinor about some axis ${\hat{\mathbf{n}}}$ by the angles of $\theta=0$ and $\theta=2\pi$, we find

:::{math}
:label: eq-spinrot-37
U({\hat{\mathbf{n}}},0)=1, \qquad U({\hat{\mathbf{n}}},2\pi) = -1,
:::

according to {eq}`eq-spinrot-27`. We see that the spinor of an electron or other spin-$\frac{1}{2}$ particle rotated by $2\pi$ does not return to its original value, but rather undergoes a phase change of $-1$.

The fact that a $2\pi$ rotation is not the identity operation is a nonclassical effect, and we must first ask what the physical significance is (in particular, whether it has any physical consequences). Certainly an overall phase factor of a quantum state has no physical significance, but it is possible to split a beam of spin-$\frac{1}{2}$ particles into two, and to subject one of the resulting beams to a rotation by $2\pi$, whereupon the phase shift becomes observable in the interference pattern that results when the beams are recombined. This experiment has actually been performed with neutron beams, which are split and recombined by means of a neutron interferometer (essentially a large silicon crystal used as a kind of neutron diffraction grating). These experiments are discussed in more detail by Sakurai, *Modern Quantum Mechanics*, and they show that we must take the $-1$ phase shift for $2\pi$ rotations to be real.

The fact that a $2\pi$ rotation is not the identity operation on spinors of spin-$\frac{1}{2}$ systems means that we must reconsider our original quest for a representation of the classical rotations by means of unitary operators acting on a ket space, as laid out by {eq}`eq-spinrot-1`--{eq}`eq-spinrot-5`. In fact, the $U$ operators defined by {eq}`eq-spinrot-27` do not form a representation of the classical rotations in the strict sense of the word, simply because they are not parameterized by the classical rotations. That is, the $U$ operators are not a function of the $\Rmat$ matrices, at least not in the sense of a single-valued function; this is clear from the special case of

:::{math}
:label: eq-spinrot-38
\Rmat({\hat{\mathbf{n}}},0) = \Rmat({\hat{\mathbf{n}}},2\pi)=\Imat,
:::

a single classical rotation for which there are two unitary operators, shown by {eq}`eq-spinrot-37`. More generally, it can be shown that corresponding to every classical rotation $\Rmat$ there are two unitary spinor rotations,

:::{math}
:label: eq-spinrot-39
\Rmat({\hat{\mathbf{n}}},\theta) \mapsto \begin{cases} U({\hat{\mathbf{n}}},\theta), \\  U({\hat{\mathbf{n}}},\theta+2\pi) = -U({\hat{\mathbf{n}}},\theta), \\\end{cases}
:::

which replaces {eq}`eq-spinrot-1`. The two unitary operators $U$ corresponding to a given $\Rmat$ differ by a sign. We see that the association between classical and spinor rotations is not one-to-one, but rather one-to-two.

In view of this, notation such as $U(\Rmat)$ is not really proper for spin-$\frac{1}{2}$ rotations, without some understanding as to which of the two unitary operators is meant. [On the other hand, the notation $U({\hat{\mathbf{n}}},\theta)$ is unambiguous, as indicated by {eq}`eq-spinrot-27`.] For example, the representation law {eq}`eq-spinrot-4` could be rewritten in the form,

:::{math}
:label: eq-spinrot-40
U(\Rmat_1)U(\Rmat_2) = \pm U(\Rmat_1\Rmat_2),
:::

which would mean that if we take one of the two unitary operators corresponding to $\Rmat_1$ and $\Rmat_2$ and multiply them, we will obtain one of the two unitary operators corresponding to $\Rmat_1\Rmat_2$. With this interpretation, {eq}`eq-spinrot-40` is correct for spinor rotations (but it is awkward and can lead to confusion).

(sec-spinrot-10)=

## The Group Manifolds $SU(2)$ and $SO(3)$

We explained in {ref}`ch-classrot`\ that the Baker-Campbell-Hausdorff theorem guaranteed that the group composition or multiplication law for finite operations was effectively contained in the commutation relations. This was why we focused first on finding a representation of the commutation relations {eq}`eq-spinrot-24`, a task that will occupy us at greater length in the next set of notes, and why we were confident that when we exponentiated linear combinations of the angular momentum operators we would obtain operators that would reproduce the composition law of the classical rotations. What, then, has gone wrong, that we should end up with a double-valued representation, so that {eq}`eq-spinrot-4` must be replaced by {eq}`eq-spinrot-40`? The answer is that the spinor representation of the rotations is locally one-to-one, but globally one-to-two.

To explain this statement more precisely, we need to discuss the group $SU(2)$. The notation $SU(2)$ is standard in mathematical physics for the group of $2\times2$ complex unitary matrices with determinant $+1$. As in the notation $SO(3)$, the $S$ stands for “special,” which means the determinant is $+1$.

The significance of $SU(2)$ in the present discussion is that every spinor rotation $U({\hat{\mathbf{n}}},\theta)$ defined by {eq}`eq-spinrot-27` for some axis ${\hat{\mathbf{n}}}$ and some angle $\theta$ is a member of the group $SU(2)$; and, conversely, every member of the group $SU(2)$ can be written in the form $U({\hat{\mathbf{n}}},\theta)$ for some axis ${\hat{\mathbf{n}}}$ and some angle $\theta$. We will not prove these facts; the proofs are easy, and are left as exercises. But we note the following consequence. Namely, since any group is closed under multiplication, if we form the product of two spinor rotations of the form $U({\hat{\mathbf{n}}},\theta)$, we obtain another spinor rotation of the same form. Thus, every spinor rotation can be written in axis-angle form, and (like the classical rotations) there is no loss of generality in assuming this form for a spinor rotation. We see that $SU(2)$ *is* the group of spinor rotations.

To understand the one-to-two association between $SO(3)$ and $SU(2)$ more thoroughly, it helps to view things geometrically in terms of the respective group manifolds. As explained in {ref}`ch-classrot`, the group manifold for $SO(3)$ can be seen as a 3-dimensional surface living in the 9-dimensional space of all $3\times3$ real matrices. Similarly, the group manifold for $SU(2)$ can be seen as a surface living in the space of all $2\times2$ complex matrices. Since a $2\times2$ complex matrix has 4 complex components, each with a real and imaginary part, it takes 8 real numbers to specify an arbitrary $2\times2$ complex matrix, and we can say that $2\times2$ complex matrix space is 8-dimensional. But the condition $U^\hc U=1$ constitutes 4 real constraints, and the condition $\det U=+1$ is one more real constraint, for a total of 5 constraints on 8 variables. Therefore the group manifold $SU(2)$ can be seen as a 3-dimensional surface living in the 8-dimensional space of all $2\times2$ complex matrices. We see that both group manifolds $SO(3)$ and $SU(2)$ are 3-dimensional; this is also evident from the axis-angle parameterization of $SU(2)$ matrices, which involves 3 real parameters.

:::{figure} images/spinrot-fig01.png
:label: fig-spinrot-1
:width: 80%

There exist finite neighborhoods of the identity elements in the two groups, $SO(3)$ and $SU(2)$, which can be placed into one-to-one correspondence in such as way that the composition law is reproduced, according to Eq. {eq}`eq-spinrot-4`. But the neighborhoods cannot be expanded to cover the whole group manifold without losing the one-to-one correspondence.
:::

The identity matrix $\Rmat=\Imat$ is one point of interest on the group manifold $SO(3)$, and the identity $U=1$ is one point of interest on the group manifold $SU(2)$. These two points are associated with one another by the requirement {eq}`eq-spinrot-3`. Next, once we have found a representation of the angular momentum commutation relations by {eq}`eq-spinrot-25`, we have a one-to-one correspondence between infinitesimal neighborhoods of the respective identity elements, as indicated by {eq}`eq-spinrot-13`. Next, the Baker-Campbell-Hausdorff theorem guarantees that by exponentiation we obtain a one-to-one correspondence between finite neighborhoods of the identity elements, which moreover satisfies the representation law {eq}`eq-spinrot-4`. This is illustrated in {ref}`fig-spinrot-1`, and it is in this sense that we say that the representation of $SO(3)$ by $SU(2)$ is locally one-to-one. But if we try to expand the two neighborhoods on the two group manifolds, we will find that when the neighborhood in $SO(3)$ has covered the whole group manifold, the corresponding neighborhood in $SU(2)$ has only covered half of that group manifold. In effect, $SU(2)$ is twice as big as $SO(3)$, corresponding to the fact that the periodicity of spinor rotations about a fixed axis is $4\pi$, not $2\pi$. Thus, we say that globally the representation is one-to-two.

(sec-spinrot-11)=

## Explicit Relationship Between $SU(2)$ and $SO(3)$

The one-to-two character of the spinor represenation of rotations can be seen in another way. Let us return to the spinor adjoint formula {eq}`eq-spinrot-29`, which we write in the form

:::{math}
:label: eq-spinrot-41
U^\hc \sigma_i U = \sum_j R_{ij} \, \sigma_j.
:::

We multiply this equation on the right by $\sigma_k$ and take traces, using the identity

:::{math}
:label: eq-spinrot-42
\tr(\sigma_j\sigma_k) = 2\delta_{jk},
:::

to obtain

:::{math}
:label: eq-spinrot-43
R_{ij} = {1\over2} \tr \bigl( U^\hc \sigma_i U \sigma_j \bigr).
:::

The significance of this result is that it is an explicit formula giving, not $U$ as a function of $\Rmat$, but rather $\Rmat$ as a function of $U$. We see that since the right hand side is quadratic in $U$, both $U$ and $-U$ correspond to the same $\Rmat$. Furthermore, it is straightforward to show explicitly from this formula that

:::{math}
:label: eq-spinrot-44
\Rmat(U_1)\Rmat(U_2) = \Rmat(U_1U_2).
:::

See Prob.~\prbrspinrot-2.

Thus, although we started out looking for representations $U=U(\Rmat)$ of the classical rotations by unitary operators, in the case of spin-$\frac{1}{2}$ systems what we have found instead is a representation of unitary spin rotation operators by classical rotations, $\Rmat=\Rmat(U)$. This suggests that the spin rotation group $SU(2)$ is really the more fundamental group, and that the general theory of rotations is best formulated with $SU(2)$ as the starting point. This indeed is the most useful point of view in quantum mechanics, and it has its advantages even in purely classical problems.

(sec-spinrot-12)=

## The Cayley-Klein Parameters

The Cayley-Klein parameters are a set of parameters for representing rotations, either classical or spinor. They were discovered in the nineteenth century before the advent of quantum mechanics, and were originally intended for use in classical problems of rigid body motion. (They are still used for that purpose.) Pauli himself was familiar with the theory of the Cayley-Klein parameters, which apparently helped him to discover the matrices that now bear his name, and to get credit for the theory of electron spin.

To see how the Cayley-Klein parameters come about, we first write an arbitrary $2\times2$ complex matrix in terms of its four complex components,

:::{math}
:label: eq-spinrot-45
\begin{aligned}
U=\begin{pmatrix} a & b \\ c & d \\\end{pmatrix}.
\end{aligned}

:::

Next, the constraint that $U$ be unitary is equivalent to the demand that the rows of $U$ form a pair of orthonormal unit vectors, or,

:::{math}
:label: eq-spinrot-46a
\begin{aligned}
|a|^2 + |b|^2 &=1,
\end{aligned}
:::

:::{math}
:label: eq-spinrot-46b
\begin{aligned}
|c|^2 + |d|^2 &=1,
\end{aligned}
:::

:::{math}
:label: eq-spinrot-46c
\begin{aligned}
a^\cc c + b^\cc d &= 0.
\end{aligned}
:::

Also, the requirement $\det U=1$ is equivalent to

:::{math}
:label: eq-spinrot-47
\det U = ad-bc =1.
:::

Now if we take {eq}`eq-spinrot-46c` and {eq}`eq-spinrot-47` and solve for $c$ and $d$, assuming $a$ and $b$ are given, we find $c=-b^\cc$, $d=a^\cc$, so that an arbitrary element of $SU(2)$ can be written in the form,

:::{math}
:label: eq-spinrot-48
\begin{aligned}
U=\begin{pmatrix} a & b \\  -b^\cc & a^\cc \\\end{pmatrix},
\end{aligned}

:::

where $a$ and $b$ are complex numbers satisfying the constraint {eq}`eq-spinrot-46a`. Finally, if we break $a$ and $b$ into their real and imaginary parts according to

:::{math}
:label: eq-spinrot-49
a=x_0 + i x_3, \qquad b=x_2 + ix_1,
:::

then an arbitrary element of $SU(2)$ has the form

:::{math}
:label: eq-spinrot-50
\begin{aligned}
U= \begin{pmatrix} x_0 + i x_3 & x_2 + i x_1 \\  -x_2 + ix_1 & x_0 -ix_3 \\\end{pmatrix} = x_0 + i(x_1\sigma_1 + x_2\sigma_2 + x_3\sigma_3)= x_0 + i \xvec \cdot \sigmavec,
\end{aligned}

:::

where the four real numbers $(x_0,x_1,x_2,x_3)$ satisfy the constraint

:::{math}
:label: eq-spinrot-51
x_0^2 + x_1^2 + x_2^2 + x_3^2 = 1.
:::

The parameters $(x_0,x_1,x_2,x_3)$ are the Cayley-Klein parameters, in terms of which an arbitrary spinor rotation is represented by {eq}`eq-spinrot-50`. An arbitrary classical rotation can also be written in terms of Cayley-Klein parameters, by using {eq}`eq-spinrot-43` to write $\Rmat$ in terms of $U$. One might ask why we should parameterize rotations by four parameters, subject to one constraint, when we could use three parameters subject to no constraints. The answer is that the various options for three parameters, such as the Euler angles, are unsymmetrical and do not cover the group manifold without introducing coordinate singularities (similar to the singularity in spherical coordinates at the north pole). The lack of symmetry of the Euler angles quickly leads to ugly calculations, and coordinate singularities are inconvenient for many purposes (computer programs, for example).

The constraint {eq}`eq-spinrot-51` is interesting, for it shows that the group manifold $SU(2)$ can be seen as a 3-dimensional surface living, not in 8-dimensional matrix space, as earlier, but in a 4-dimensional space with coordinates $(x_1,x_2,x_3,x_4)$. Furthermore, the surface in question is simply the set of all points in this 4-dimensional space at a unit distance from the origin; the surface is the 3-dimensional surface of a sphere in 4-dimensional space, or the manifold $S^3$ in standard mathematical terminology.

(sec-spinrot-13)=

## Spinor Rotations about the Coordinate Axes

Let us now tabulate the spinor rotations about the three coordinate axes, much as we did in {eq}`eq-classrot-18` for classical rotations. We have

:::{math}
\begin{aligned}
U({\hat{\mathbf{x}}},\theta) &= \cos{\theta\over2} - i\sigma_x \sin{\theta\over2} = \begin{pmatrix} \cos{\theta\over2} & -i\sin{\theta\over2} \\  -i\sin{\theta\over2} & \cos{\theta\over2} \\\\\end{pmatrix},
\end{aligned}

:::

:::{math}
\begin{aligned}
U({\hat{\mathbf{y}}},\theta) &= \cos{\theta\over2} -i\sigma_y \sin{\theta\over2} = \begin{pmatrix} \cos{\theta\over2} & -\sin{\theta\over2} \\  \sin{\theta\over2} & \cos{\theta\over2} \\\\\end{pmatrix},
\end{aligned}

:::

:::{math}
:label: eq-spinrot-52
\begin{aligned}
U({\hat{\mathbf{z}}},\theta) &= \cos{\theta\over2} -i\sigma_z \sin{\theta\over2} = \begin{pmatrix} e^{-i\theta/2} & 0 \\ 0 & e^{i\theta/2} \\.       \\\end{pmatrix}
\end{aligned}

:::

The matrix for $U({\hat{\mathbf{z}}},\theta)$ is diagonal, because these matrices represent the corresponding operators in the basis of eigenkets of $S_z=(\hbar/2)\sigma_z$. Obviously, the exponential of a diagonal matrix is diagonal.

The elementary rotations in {eq}`eq-spinrot-52` can be combined to obtain an Euler angle parameterization for spinor rotations. This is a direct transcription of {eq}`eq-classrot-57`,

:::{math}
:label: eq-spinrot-53
U(\alpha,\beta,\gamma) = U({\hat{\mathbf{z}}},\alpha) U({\hat{\mathbf{y}}},\beta) U({\hat{\mathbf{z}}},\gamma),
:::

and is just the spinor representative of the latter. However, the ranges on the Euler angles are different from the classical case; here we have

:::{math}
\begin{aligned}
& 0\le \alpha \le 2\pi,
\end{aligned}
:::

:::{math}
\begin{aligned}
& 0\le \beta \le \pi,
\end{aligned}
:::

:::{math}
:label: eq-spinrot-54
\begin{aligned}
& 0\le \gamma \le 4\pi,
\end{aligned}
:::

where the final angle $\gamma$ is allowed to range to $4\pi$ to cover the extra spinor rotations.

(sec-spinrot-14)=

## A Spin “Pointing In” a Given Direction

You have no doubt heard the expression, “a spinor pointing in the such-and-such direction.” What does this language mean, considering that a spinor for spin-$\frac{1}{2}$ particle is a complex 2-vector, not a real 3-vector? To explain this terminology, we introduce the eigenbasis of the operator $S_z$, which we denote by $\ket{\pm}$. These kets are of course represented by unit vectors in the $S_z$ basis itself,

:::{math}
:label: eq-spinrot-55
\ket{+} = \begin{pmatrix} 1 \\ 0 \\\end{pmatrix}, \qquad \ket{-} = \begin{pmatrix} 0 \\ 1 \\\end{pmatrix},
:::

where to be precise the kets are not equal to the column vectors indicated, rather the components of the kets in the $S_z$-basis are given. The 2-vectors corresponding to $\ket{+}$ and $\ket{-}$ are often denoted in the literature by $\alpha$ and $\beta$ (the “spin up” and “spin down” spinors, respectively).

To begin, we simply declare that the ket $\ket{+}$ is the spinor “pointing in the ${\hat{\mathbf{z}}}$ direction.” Next, to obtain a spinor pointing in an arbitrary direction ${\hat{\mathbf{n}}}$, we first consider a classical rotation, say, $\Rmat_0$, which maps the ${\hat{\mathbf{z}}}$ direction into the ${\hat{\mathbf{n}}}$ direction,

:::{math}
:label: eq-spinrot-56
{\hat{\mathbf{n}}} = \Rmat_0 {\hat{\mathbf{z}}}.
:::

A rotation $\Rmat_0$ with this property is easy to write down in Euler angle form; we simply let $\alpha$ be the azimuthal angle of ${\hat{\mathbf{n}}}$ and $\beta$ the polar angle, so that $\Rmat_0$ has the form

:::{math}
:label: eq-spinrot-57
\Rmat_0 = \Rmat(\alpha,\beta,0) = \Rmat({\hat{\mathbf{z}}},\alpha)\Rmat({\hat{\mathbf{y}}},\beta).
:::

The rotation $\Rmat_0$ that satisfies {eq}`eq-spinrot-56` is not unique; we could allow any value of the Euler angle $\gamma$ (not just $\gamma=0$). But $\Rmat_0$ in {eq}`eq-spinrot-57` will work. Then to obtain the spinor “pointing in” the ${\hat{\mathbf{n}}}$ direction (call it $\ket{{\hat{\mathbf{n}}};+}$), we simply define

:::{math}
:label: eq-spinrot-58
\ket{{\hat{\mathbf{n}}};+} = U_0 \ket{+},
:::

where $U_0=U(\Rmat_0)$. We don't care about the overall phase of this spinor, which is why we can ignore the Euler angle $\gamma$, and why we don't care which of the two $U_0$'s is chosen in {eq}`eq-spinrot-58`.

It is easy to work out the 2-vector representing $\ket{{\hat{\mathbf{n}}};+}$ in the $S_z$ basis. We simply write out the Euler angle representation of $U_0$,

:::{math}
:label: eq-spinrot-59
U_0 = U({\hat{\mathbf{z}}},\alpha)U({\hat{\mathbf{y}}},\beta),
:::

and appeal to the matrices {eq}`eq-spinrot-52`. We find

:::{math}
:label: eq-spinrot-60
\ket{{\hat{\mathbf{n}}};+} = \begin{pmatrix} e^{-i\alpha/2} \cos{\beta\over2} \\  e^{i\alpha/2} \sin{\beta\over2} \\\end{pmatrix}.
:::

Since the overall phase is immaterial, we can multiply this by $e^{\pm i\alpha/2}$, if we like, to clear one or the other of the two phase factors in the 2-vector.

The spinor $\ket{{\hat{\mathbf{n}}};+}$ has several notable properties. First, it is an eigenspinor of ${\hat{\mathbf{n}}}\cdot\sigmavec$, that is, of the component of the spin in the ${\hat{\mathbf{n}}}$ direction, with eigenvalue $+1$. This is easily proved with the help of the spinor adjoint formula {eq}`eq-spinrot-29`:

:::{math}
\begin{aligned}
{\hat{\mathbf{n}}}\cdot\sigmavec \ket{{\hat{\mathbf{n}}};+} &= U_0 U_0^\hc ({\hat{\mathbf{n}}}\cdot\sigmavec) U_0 \ket{+} = U_0 {\hat{\mathbf{n}}}\cdot(\Rmat_0\sigmavec) \ket{+}
\end{aligned}
:::

:::{math}
\begin{aligned}
&= U_0 \bigl(\Rmat_0^{-1}{\hat{\mathbf{n}}}\bigr)\cdot\sigmavec \ket{+} = U_0 ({\hat{\mathbf{z}}}\cdot\sigmavec) \ket{+}
\end{aligned}
:::

:::{math}
\begin{aligned}
&= U_0 \sigma_z \ket{+} = U_0 \ket{+} = \ket{{\hat{\mathbf{n}}};+}, & {eq}`eq-spinrot-61`
\end{aligned}
:::

where we use {eq}`eq-spinrot-56`. Next, the expectation value of the spin in any direction orthogonal to ${\hat{\mathbf{n}}}$, taken with respect to $\ket{{\hat{\mathbf{n}}};+}$, vanishes, as indicated by

:::{math}
:label: eq-spinrot-62
\matrixelement{{\hat{\mathbf{n}}};+}{\sigmavec}{{\hat{\mathbf{n}}};+} ={\hat{\mathbf{n}}}.
:::

To prove this we again use the adjoint formula to reexpress the left hand side,

:::{math}
:label: eq-spinrot-63
\matrixelement{{\hat{\mathbf{n}}};+}{\sigmavec}{{\hat{\mathbf{n}}};+}= \matrixelement{+}{U_0^\hc \sigmavec U_0}{+} = \Rmat_0 \matrixelement{+}{\sigmavec}{+}.
:::

But the final expectation value in this expression is a vector whose $x$, $y$ and $z$ components are $0$, $0$, and $1$, as a direct appeal to the Pauli matrices will show. That is, this vector is the unit vector ${\hat{\mathbf{z}}}$, so the right hand side of {eq}`eq-spinrot-63` becomes ${\hat{\mathbf{n}}}$ in accordance with {eq}`eq-spinrot-56`. This proves {eq}`eq-spinrot-62`.

It is a fact that for a spin-$\frac{1}{2}$ system, every spinor “points in” some direction, that is, every spinor is an eigenspinor of ${\hat{\mathbf{n}}}\cdot\sigmavec$ for some ${\hat{\mathbf{n}}}$. This is not true for values of the spin greater than $\frac{1}{2}$.

This concludes what we have to say about rotations on spin-$\frac{1}{2}$ systems. In the next notes we consider the general problem of constructing representations of the angular momentum commutation relations and the corresponding representations of rotations.

\problems

(prob-spinrot-1)=

**Problem \prbdspinrot-1.} This is problem~3.8 of Sakurai, *Modern Quantum Mechanics.** 

:::{math*
:label: eq-spinrot-64
U(\alpha,\beta,\gamma)= U({\hat{\mathbf{z}}},\alpha)U({\hat{\mathbf{y}}},\beta)U({\hat{\mathbf{z}}},\gamma)
:::

be the Euler angle representation of a rotation on a spin-$\frac{1}{2}$ system. Find the axis ${\hat{\mathbf{n}}}$ and angle $\theta$ of this rotation in terms of the Euler angles.

(prob-spinrot-2)=

**Problem \prbdspinrot-2..** 

:::{math}
:label: eq-spinrot-65
A = a_0 I + \avec\cdot\sigmavec,
:::

where $(a_0,\avec)$ are the (generally complex) expansion coefficients. See Prob. {ref}`prob-hilbert-3`(c). Notice that if $A$ is Hermitian, then $(a_0,\avec)$ are real. Notice also that

:::{math}
:label: eq-spinrot-66
\det A = a_0^2 - \avec\cdot\avec.
:::

It is convenient to write $\sigma_0=I$, and to regard $\sigma_0$ as a fourth Pauli matrix. Then {eq}`eq-spinrot-65` becomes,

:::{math}
:label: eq-spinrot-67
A=\sum_{\mu=0}^3 a_\mu \, \sigma_\mu.
:::

Notice that we have the orthogonality relation,

:::{math}
:label: eq-spinrot-68
\tr(\sigma_\mu \sigma_\nu) = 2 \delta_{\mu\nu},
:::

which can be used to solve {eq}`eq-spinrot-67` for the expansion coefficients,

:::{math}
:label: eq-spinrot-69
a_\mu ={1\over2} \tr(\sigma_\mu A).
:::

Use these results to show that

:::{math}
:label: eq-spinrot-70
\tr(AB) = {1\over2}\sum_\mu \tr(\sigma_\mu A) \tr(\sigma_\mu B),
:::

where $A$ and $B$ are $2\times 2$ matrices.

Use these results to prove {eq}`eq-spinrot-44`.

(prob-spinrot-3)=

**Problem \prbdspinrot-3..** 

\problempart{(a)} The spinor “pointing in” the ${\hat{\mathbf{n}}}$ direction was defined by {eq}`eq-spinrot-58`. Show that every spinor “points” in some direction. For this, it is sufficient to show that for every normalized spinor $\ket{\chi}$, $\matrixelement{\chi}{\sigmavec}{\chi}$ is a unit vector. You can prove this directly, or use the formalism based on {eq}`eq-spinrot-70` above. This property only holds for spin-$\frac{1}{2}$ particles.

\problempart{(b)} Consider now the phenomenon of polarization in classical electromagnetic theory. The most general physical electric field of a plane light wave of frequency $\omega$ travelling in the $z$-direction can be written in the form

:::{math}
:label: eq-spinrot-71
\Evec_phys(\rvec,t) = \Re \sum_{\mu=1}^2 {\hat{\boldsymbol{\epsilon}}}_\mu E_\mu e^{i(kz-\omega t)},
:::

where $\mu=1,2$ corresponds to $x,y$, where ${\hat{\boldsymbol{\epsilon}}}_1 ={\hat{\mathbf{x}}}$, ${\hat{\boldsymbol{\epsilon}}}_2={\hat{\mathbf{y}}}$, and where $E_1=E_x$ and $E_2=E_y$ are two complex amplitudes, and where $\omega=ck$. Thus, the wave is parameterized by the two complex numbers, $E_x$, $E_y$. Often we are not interested in absolute amplitudes, only relative ones, so we normalize the wave by setting

:::{math}
:label: eq-spinrot-72
|E_x|^2 + |E_y|^2 = E_0^2,
:::

for some suitably chosen reference amplitude $E_0$. This allows us to associate the wave with a normalized, 2-component complex “spinor,” according to

:::{math}
:label: eq-spinrot-73
\chi={1\over E_0}\begin{pmatrix} E_x \\ E_y \\\end{pmatrix}.
:::

Furthermore, we are often not interested in any overall phase of this spinor, since such an overall phase corresponds merely to a shift in the origin of time in {eq}`eq-spinrot-71`. This cannot be detected anyway in experiments that average over the rapid oscillations of the wave (a practical necessity at optical frequencies).

If we normalize according to {eq}`eq-spinrot-72` and {eq}`eq-spinrot-73` and ignore the overall phase, then the four real parameters originally inherent in $(E_x,E_y)$ are reduced to two, which describe the state of *polarization* of the wave. For example, the spinors

:::{math}
:label: eq-spinrot-74
\chi_x = \begin{pmatrix}1\cr0\\\end{pmatrix}, \quad \chi_y = \begin{pmatrix}0\cr1\\\end{pmatrix},
:::

correspond to linear polarization in the $x$- and $y$-directions, respectively. Notice that polarization in the $+x$-direction is the same as that in the $-x$-direction; they differ only by an overall phase. Similarly, the spinors

:::{math}
:label: eq-spinrot-75
\chi_r = {1\over\sqrt{2}} \begin{pmatrix}1\\ -i\\\end{pmatrix}, \quad \chi_\ell = {1\over\sqrt{2}} \begin{pmatrix}1 \\ i\\\end{pmatrix},
:::

correspond to right and left circular polarizations, respectively. Right circular polarization means the electric vector rotates in a clockwise direction in the $x$-$y$ plane, tracing out a circle, whereas in left circular polarization, the electric vector rotates counterclockwise. Here I am using the conventions of Jackson, *Classical Electrodynamics* and Born and Wolf, *Principles of Optics*, but other authors, such as Sakurai, *Modern Quantum Mechanics*, use the opposite conventions. Right circular polarization corresponds to photons with negative helicity, and vice versa. In more general polarization states, the electric vector traces out an ellipse in the $x$-$y$ plane; these are called elliptical polarizations. A limiting case of the ellipse is where the electric vector traces a line, back and forth; these are linear polarization states.

In optics it is conventional to introduce the so-called *Stokes' parameters* to describe the state of polarization. These are defined by

:::{math}
\begin{aligned}
s_0 &= (|E_x|^2 + |E_y|^2)/E_0^2=1,
\end{aligned}
:::

:::{math}
\begin{aligned}
s_1 &= (|E_x|^2 - |E_y|^2)/E_0^2,
\end{aligned}
:::

:::{math}
\begin{aligned}
s_2 &= 2\Re( E_x E_y^\cc)/E_0^2,
\end{aligned}
:::

:::{math}
:label: eq-spinrot-76
\begin{aligned}
s_3 &= 2\Im( E_x E_y^\cc)/E_0^2.
\end{aligned}
:::

(See Born and Wolf, *Principles of Optics*, p.~31.) Show that these parameters satisfy

:::{math}
:label: eq-spinrot-77
s_1^2 + s_2^2 + s_3^2=1,
:::

so that ${\hat{\mathbf{s}}}=(s_1,s_2,s_3)$ is a unit vector. The sphere upon which this unit vector lies is called the *Poincar\'e sphere*; points on this sphere correspond to polarization states. Notice that the Stokes' parameters are independent of the overall phase of the wave, being bilinear in the field amplitudes $(E_x,E_y)$. Indicate which points on the Poincar\'e sphere correspond to linear $x$- and $y$-polarization, and which to right and left circular polarization. What kind of polarization does the positive $2$-axis in $\svec$-space correspond to? What about the negative $2$-axis? (We will refer to directions in $\svec$-space by the indices 1,2,3, to avoid confusion with $x$, $y$, $z$ in real space).

\problempart{(c)} Compute the expectation value $\matrixelement {\chi}{\sigmavec}{\chi}={\hat{\mathbf{n}}}$ for the spinor {eq}`eq-spinrot-73`, and relate the components of ${\hat{\mathbf{n}}}$ to the Stokes' parameters. You will see that Stokes and Poincar\'e didn't exactly follow quantum mechanical conventions (since quantum mechanics had not yet been invented in their day), but the basic idea is that the point on the Poincar\'e sphere indicates the direction in which the spinor {eq}`eq-spinrot-73` is “pointing.”

\problempart{(d)} Now suppose we have a quarter-wave plate with its fast and slow axes in the $x$- and $y$-direction, respectively. This causes a relative phase shift in the $x$- and $y$-components of the spinor {eq}`eq-spinrot-73` by $\pi/2$, that is,

:::{math}
:label: eq-spinrot-78
\begin{aligned}
\begin{pmatrix}E_x' \\  E_y'\\\end{pmatrix} = \begin{pmatrix} e^{-i\pi/4} & 0 \\ 0 & e^{i\pi/4} \\\end{pmatrix} \begin{pmatrix} E_x \\ E_y \\\end{pmatrix},
\end{aligned}

:::

where the unprimed fields are those entering the quarter wave plate, and the primed ones are those exiting it. Show that the effect of the quarter wave plate on an incoming polarization state, as represented by a point on the Poincar\'e sphere, can be represented by a rotation in $\svec$-space. Find the $3\times3$ rotation matrix such that ${\hat{\mathbf{s}}}'=\Rmat{\hat{\mathbf{s}}}$. Use this picture to determine the effect of the quarter wave plate on linear $x$- and $y$- polarizations, and on right and left circular polarizations. What polarization must we feed into the quarter wave plate to get right circular polarization coming out?
