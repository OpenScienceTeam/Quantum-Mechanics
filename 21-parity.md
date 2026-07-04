---
title: "21. Parity"
---
(ch-parity)=

# 21. Parity

(sec-parity-1)=

## Introduction

We have now completed our study of proper rotations in quantum mechanics, one of the important space-time symmetries. In these notes we shall examine parity, another space-time symmetry. In a latter set of notes we shall take up the third, which is time reversal. All these symmetries are special cases of Lorentz transformations, which are united in a relativistic treatment.

(sec-parity-2)=

## Spatial Inversion

Parity begins life as an operation on three-dimensional, physical space, represented in an inertial frame by the matrix

:::{math}
:label: eq-parity-1
\begin{aligned}
\Pmat=\begin{pmatrix}-1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & -1 \\\end{pmatrix} = -\Imat.
\end{aligned}

:::

See also {eq}`eq-classrot-16` and the discussion in {ref}`sec-classrot-5`. This operation, which we call *spatial inversion*, inverts vectors through the origin, mapping $\xvec$ into $-\xvec$. The most important properties of $\Pmat$ for our purposes are

:::{math}
:label: eq-parity-2
\Pmat^2 = \Imat,
:::

and

:::{math}
:label: eq-parity-3
\Pmat \Rmat \Pmat^{-1} = \Rmat,
:::

for all proper rotations $\Rmat \in SO(3)$. These properties are trivial in view of {eq}`eq-parity-1`; in particular, $\Pmat$, being a multiple of the identity, commutes with all matrices, so $\Pmat \Rmat \Pmat^{-1} = \Rmat \Pmat \Pmat^{-1} = \Rmat$.

The spatial inversion $\Pmat$ is an example of an improper rotation, that is, it belongs to $O(3)$ but not $SO(3)$. In fact, every proper rotation is mapped into an improper one by multiplying by $\Pmat$, and vice versa. See Fig.~\figr\classrot.5 to visualize the spaces of proper and improper rotations.

(sec-parity-3)=

## Parity in Quantum Mechanics

In this we introduce the operator $\pi$, called the *parity* operator, which corresponds to the spatial inversion operation $\Pmat$.

Recall that in the case of proper rotations, we sought and found operators $U(\Rmat)$, acting on the Hilbert space of various quantum mechanical systems, that implement the effect of classical, proper rotations $\Rmat$. The operators $U(\Rmat)$ were required to satisfy certain postulates, including one that they be unitary, and another that they reproduce the multiplication law of the classical, proper rotations. See {ref}`sec-spinrot-3`. We represent this mapping between classical rotations and rotation operators by

:::{math}
:label: eq-parity-4
\Rmat \mapsto U(\Rmat),
:::

and we say that it specifies a unitary representation of the classical rotation group $SO(3)$.

Similarly, in the case of spatial inversion, we seek an operator $\pi$ acting on the Hilbert space of various quantum mechanical systems that is associated with the spatial inversion operation $\Pmat$,

:::{math}
:label: eq-parity-5
\Pmat \mapsto \pi,
:::

which is required to satisfy certain postulates. These are that $\pi$ be unitary,

:::{math}
:label: eq-parity-6
\pi^\hc \pi =1,
:::

and that it should satisfy

:::{math}
:label: eq-parity-7
\pi^2 = 1,
:::

and

:::{math}
:label: eq-parity-8
\pi U(\Rmat) \pi^\hc = U(\Rmat)
:::

for all $\Rmat \in SO(3)$. The latter two postulates are representations of the multiplication laws {eq}`eq-parity-2` and {eq}`eq-parity-3` at the level of spatial transformations. The first two postulates imply that $\pi$ is both unitary and Hermitian, so that

:::{math}
:label: eq-parity-9
\pi=\pi^\hc=\pi^{-1},
:::

while the third postulate {eq}`eq-parity-8` is equivalent to

:::{math}
:label: eq-parity-10
[\pi,\Jvec] = 0,
:::

where $\Jvec$ is the angular momentum (the generator of the rotation operators $U(\Rmat)$). In short, $\pi$ is a scalar operator [see {eq}`eq-transfop-8` and {eq}`eq-transfop-10`]. These postulates do not uniquely determine the parity operator for all quantum mechanical systems, but they narrow the possibilities considerably so that it is easy to find a suitable definition of $\pi$ in specific cases.

Taken together with the properties of $U(\Rmat)$, the postulates for $\pi$ amount to requiring that the set of operators $U(\Rmat)$ and $\pi U(\Rmat)$ for $\Rmat \in SO(3)$ form a unitary representation of the full rotation group $O(3)$. That is, generalizing the map {eq}`eq-parity-4` to include improper rotations, we can say

:::{math}
:label: eq-parity-11
\pi = U(\Pmat).
:::

(sec-parity-4)=

## Parity for a Spinless Particle in Three Dimensions

Let us begin with the case of a spinless particle moving in three dimensions, for which the basis states can be taken to be the position eigenkets $\ket{\xvec}$ and the Hilbert space is isomorphic to the space of configuration space wave functions $\psi(\xvec)$. In this case we defined the rotation operators by

:::{math}
:label: eq-parity-12
U(\Rmat) \ket{\xvec} = \ket{\Rmat \xvec},
:::

which we found satisfactory. See {eq}`eq-orbamsph-3` and the discussion in {ref}`sec-orbamsph-2`. In a similar spirit, we now guess that the definition of parity for such systems should be

:::{math}
:label: eq-parity-13
\pi\ket{\xvec} = \ket{\Pmat\xvec} = \ket{-\xvec}.
:::

This transformation law on basis kets implies that wave functions transform according to

:::{math}
:label: eq-parity-14
\psi(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{\pi}} \psi(-\xvec).
:::

We must check that this definition satisfies the postulates {eq}`eq-parity-6`--{eq}`eq-parity-8`.

First, by applying $\pi$ twice, we have two changes of sign,

:::{math}
:label: eq-parity-15
\pi^2 \ket{\xvec} =\ket{\xvec},
:::

so the postulate {eq}`eq-parity-7` is satisfied. Next, since

:::{math}
:label: eq-parity-16
\int d^3\xvec \, |\psi(\xvec)|^2 = \int d^3\xvec \, |\psi(-\xvec)|^2
:::

for all wave functions $\psi$, the operator $\pi$ is unitary (it preserves the normalization of states), and the postulate {eq}`eq-parity-6` is satisfied. See Problem {ref}`prob-hilbert-6`(c). Finally, since

:::{math}
:label: eq-parity-17
\pi U(\Rmat) \ket{\xvec} = \pi \ket{\Rmat \xvec} = \ket{-\Rmat\xvec} = U(\Rmat)\pi\ket{\xvec}
:::

we have $\pi U(\Rmat) = U(\Rmat)\pi$, which is equivalent to the postulate {eq}`eq-parity-8`. All postulates are satisfied, so we shall take {eq}`eq-parity-13` as the definition of $\pi$ for a spinless particle in three-dimensional space.

As for the last postulate {eq}`eq-parity-8` and its equivalent form {eq}`eq-parity-10`, since the angular momentum for a spinless particle in three-dimensional space is the orbital angular momentum $\Lvec=\xvec \cross \pvec$, we have

:::{math}
:label: eq-parity-18
\pi \Lvec \pi^\hc = \Lvec.
:::

This follows from the postulates, but can also be verified directly.

It is also of interest to compute the conjugation relations of other vector operators with respect to $\pi$. We start with the position operator $\xvec$. For the sake of the following demonstration, we will write ${\hat{\mathbf{x}}}$ for the operator, and $\xvec$ for associated vectors of $c$-numbers. In the configuration representation, the operator ${\hat{\mathbf{x}}}$ means multiplication of the wave function by the position of the particle, that is,

:::{math}
:label: eq-parity-19
({\hat{\mathbf{x}}} \psi)(\xvec) = \xvec \psi(\xvec).
:::

Now computing the effect of $\pi{\hat{\mathbf{x}}}\pi^\hc$ on an arbitrary wave function, we have

:::{math}
:label: eq-parity-20
\psi(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{\pi^\hc}} \psi(-\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{{\hat{\mathbf{x}}}}} \xvec\psi(-\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{\pi}} -\xvec\psi(\xvec)=-({\hat{\mathbf{x}}}\psi)(\xvec),
:::

where we use $\pi^\hc = \pi$.

Thus we have

:::{math}
:label: eq-parity-21
\pi \xvec \pi^\hc = -\xvec,
:::

where we have dropped the hats so that now $\xvec$ represents the operator again. We see that conjugating the position operator $\xvec$ by $\pi$ converts it into $-\xvec$. This is reasonable, in view of the action of $\Pmat$ on points of space. Similarly, we find

:::{math}
:label: eq-parity-22
\pi\pvec\pi^\hc = -\pvec.
:::

This is fairly obvious, since $\pvec=-i\hbar\del$ in the position representation, and $\del=\partial/\partial \xvec$ should change sign when $\xvec$ does. Taking the cross product of {eq}`eq-parity-21` and {eq}`eq-parity-22`, we obtain {eq}`eq-parity-18`.

(sec-parity-5)=

## Parity for Spin Systems

Next let us consider just the spin degrees of freedom for a particle with spin, ignoring the spatial degrees of freedom for the time being. The Hilbert space is

:::{math}
:label: eq-parity-23
\ES_spin = \mathspan\{\ket{sm}, m=-s,\ldots,+s\},
:::

with the standard angular momentum basis shown. We would like to find a reasonable definition of $\pi$ that satisfies the postulates {eq}`eq-parity-6`--{eq}`eq-parity-8`. This means finding the action of $\pi$ on the basis states $\ket{sm}$. Since the angular momentum in this case is the spin vector $\Svec$, the form {eq}`eq-parity-10` of the third postulate is

:::{math}
:label: eq-parity-24
[\pi,\Svec]=0.
:::

The states $\ket{sm}$ are nondegenerate eigenstates of $S_z$ on the Hilbert space {eq}`eq-parity-23`, and {eq}`eq-parity-24` implies $[\pi,S_z]=0$. Therefore by Theorem {ref}`thm-hilbert-5`, $\ket{sm}$ must also be an eigenstate of parity,

:::{math}
:label: eq-parity-25
\pi\ket{sm} = \eta_m \ket{sm},
:::

where as indicated the eigenvalue $\eta_m$ might depend on $m$, as far as we know at this point. Theorem {ref}`thm-hilbert-5` does not tell us the value of this eigenvalue, but it must be real since $\pi$ is Hermitian. Now by applying raising and lowering operators and using {eq}`eq-parity-24` again, we have

:::{math}
\begin{aligned}
S_\pm (\pi\ket{sm}) &= \pi S_\pm\ket{sm} =\sqrt{(s\mp m)(s\pm m+1)} \hbar \, \pi\ket{s,m\pm1}
\end{aligned}
:::

:::{math}
:label: eq-parity-26
\begin{aligned}
&=\eta_m \sqrt{(s\mp m)(s\pm m+1)} \hbar \, \ket{s,m\pm1},
\end{aligned}
:::

or, on canceling the square roots,

:::{math}
:label: eq-parity-27
\pi \ket{s,m\pm1} = \eta_m \ket{s,m\pm1}.
:::

By comparing this to {eq}`eq-parity-25`, we see that $\eta_m = \eta_{m\pm1}$, or, by induction, that $\eta$ is independent of $m$ for all $2s+1$ values it can take on. This fact could have been seen from another standpoint, for since $\pi$ is a scalar operator, by the Wigner-Eckart theorem for scalars its eigenvalues must be independent of $m$. See Secs. {ref}`sec-transfop-9`-{ref}`sec-transfop-12`. Thus we shall write simply

:::{math}
:label: eq-parity-28
\pi\ket{sm} = \eta \ket{sm}.
:::

In fact, since the states $\ket{sm}$ form a basis for $\ES_spin$, all kets in this space are eigenstates of $\pi$ with eigenvalue $\eta$, that is, $\pi$ is $\eta$ times the identity operator.

Now using the fact that $\pi^2=1$, we find that $\eta^2=1$, or $\eta=\pm1$, and we have

:::{math}
:label: eq-parity-29
\pi\ket{sm} = \pm \ket{sm}.
:::

The postulates required of $\pi$ reduce its definition to a choice of a sign. This sign is the same for all vectors in the Hilbert space $\ES_spin$ of {eq}`eq-parity-23`, so it is really a characteristic of the particle, that is, a constant like the spin quantum number $s$.

Can this sign be determined by any further arguments or by appeal to experimental results? Within nonrelativistic quantum mechanics, the answer is no, the final choice of sign is without physical consequences and can be made arbitrarily. The simplest choice is $\eta=1$, and for as long as we remain with the nonrelativistic theory, we shall assume that the parity operator satisfies

:::{math}
:label: eq-parity-30
\pi\ket{sm} = \ket{sm}.
:::

That is, the parity operator has no effect on the spin state of the particle.

In relativistic quantum mechanics, however, it becomes possible to create and destroy particles. In some cases, an initial state of a definite parity decays or otherwise evolves into a state in which a particle has been created or destroyed, and in order to account for conservation of parity it is necessary to attribute a certain parity to a particle because of the kind of particle it is. This is called *intrinsic parity*, and it is equivalent to making one of the two choice $\eta=\pm1$ for each type of particle in the process. Some details of this assignment depend on the type of particle, fermion or boson. (It turns out that for fermions, the intrinsic parity of a particle-antiparticle pair is odd; it is arbitrary whether the particle is interpreted as having even intrinsic parity and the antiparticle odd, or vice versa. See {ref}`ch-covariance`.) Not all interactions conserve parity, but for those that do, it is necessary in relativistic interactions to take into account the intrinsic parities of particles. Then the total parity of a state is the product of the intrinsic parities of the particles times the parities of the spatial parts of the wave functions. For example, the photon turns out to have negative intrinsic parity. This is related to Laporte's rule, which we discuss presently, which states that the parity of an atom changes when a photon is emitted in an electric dipole transition. The parity of the atom changes, but the parity of the entire system, including the electromagnetic field, is conserved, as we see when we include the intrinsic parity of the photon. The intrinsic parity of particles cannot be understood very well outside of the relativistic theory, but we will have more to say about it {ref}`ch-covariance`.

Returning to nonrelativistic quantum mechanics, if we include the spatial degrees of freedom of a particle, so that the Hilbert space is spanned by the basis kets

:::{math}
:label: eq-parity-31
\ket{\xvec}\otimes \ket{sm} = \ket{\xvec, m},
:::

then the parity operator is defined by

:::{math}
:label: eq-parity-32
\pi\ket{\xvec,m} = \ket{-\xvec,m}.
:::

This is equivalent to the action on the wave function,

:::{math}
:label: eq-parity-33
\psi_m(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{\pi}} \psi_m(-\xvec).
:::

As we say, parity is a purely spatial operator, and does not affect the spin (in the nonrelativistic theory).

(sec-parity-6)=

## Transformation Properties Under Parity

Returning to the conjugation relations {eq}`eq-parity-18`, {eq}`eq-parity-21` and {eq}`eq-parity-22`, we see that some vectors (for example, $\xvec$ and $\pvec$) change sign when conjugated by parity, while some (for example, $\Lvec$ and $\Svec$) do not. All these vectors are vector operators according to the definitions {eq}`eq-transfop-15` or {eq}`eq-transfop-21`, that is, they all transform in the same way under conjugation by proper rotations, but their transformation laws under improper rotations differ. Thus we can take the set of vector operators and break it down according to how the vectors transform under parity. If $\Vvec$ is a vector operator and

:::{math}
:label: eq-parity-34
\pi \Vvec \pi^\hc = \pm \Vvec,
:::

then we will say that $\Vvec$ is a *true vector* or *polar vector* if the sign is $-1$, or a *pseudovector* or *axial vector* if the sign is $+1$. Thus, $\xvec$ and $\pvec$ are true vectors, while $\Lvec$ and $\Svec$ (more generally, any angular momentum $\Jvec$) are pseudovectors. Other vectors in physics can be classified similarly, for example, the electric field $\Evec$ is a true vector, while the magnetic field $\Bvec$ is a pseudovector.

Similarly, we can classify scalars. If $K$ is a scalar operator according to the definitions {eq}`eq-transfop-8` or {eq}`eq-transfop-10`, and if

:::{math}
:label: eq-parity-35
\pi K \pi^\hc = \pm K,
:::

then we will say that $K$ is a *true scalar* if the sign is $+1$ or a *pseudoscalar* if the sign is $-1$ (notice the signs are reversed compared to the terminology for a vector). An example of a true scalar is $\xvec\cdot\pvec$, while an example of a pseudoscalar is $\pvec\cdot\Svec$.

(sec-parity-7)=

## Hamiltonians Invariant Under Parity

We argued previously that the Hamiltonian for an isolated system must be a scalar, that is, invariant under proper rotations, because the energy could not depend on the orientation. See {ref}`sec-transfop-9`. But are these Hamiltonians scalars or pseudoscalars or a combination of the two? That is, are they also invariant under parity?

As an example, consider a central force Hamiltonian,

:::{math}
:label: eq-parity-36
H={p^2\over 2m} + V(r).
:::

This certainly commutes with parity, for although $\pvec$ is mapped into $-\pvec$, the kinetic energy contains $\pvec\cdot\pvec$, which is invariant. Also, the potential energy is a function of the radius $r$, the magnitude of the vector $\xvec$, which does not change when $\xvec$ changes its sign. Parity is a good quantum number for all central force Hamiltonians.

As we know, central force Hamiltonians usually represent a two-particle system interacting by means of forces derivable from a potential that is a function only of the distance between the two particles. See {ref}`sec-cenforce-9`. All these Hamiltonians commute with parity. This generalizes to any number of particles interacting by means of forces derivable from potentials depending only on the distances between the particles, such as the electrostatic Coulomb approximation to the interactions of charged particles. This covers a wide variety of approximate Hamiltonians for atoms, molecules, and other systems. What happens when we include electromagnetic and relativistic effects? As it turns out, such Hamiltonians still commute with parity, as long as the electromagnetic fields are internally generated (that is, the system is still isolated). For example, one of the magnetic and relativistic corrections in a single electron atom is the spin-orbit term, which is proportional to $\Lvec\cdot\Svec$. But by the rules above, this is a true scalar (the dot product of two pseudovectors). What about when we include the emission and absorption of radiation, that is, of photons? In this case, too, parity is conserved, as long as we include the parity of the electromagnetic field (that is, of the photons) in our account. We summarize these facts by saying that the electromagnetic forces conserve parity.

The strong forces, responsible for the interactions of nucleons inside a nucleus as well as interactions of other hadronic particles such as the $\pi$-meson, also conserve parity. This fact was originally established by experiments involving nuclei and particles, which showed that in strong interactions the parity of the initial state is always equal to the parity of the final state. In reckoning the parity of states, however, it is necessary to take into account the intrinsic parities of various particles, for example, the $\pi$-meson (all three charge states of it) has negative intrinsic parity (just like the photon).

For these reasons, it used to be believed that parity conservation was a fundamental law of nature, much like the rotational invariance of isolated systems. This belief ended abruptly in 1956, however, when Lee and Yang suggested that parity might be violated in weak interactions. They also suggested experiments to test the idea that were quickly carried out. These showed that, indeed, parity is violated in $\beta$-decay, a prime example of a weak interaction.

The weak forces are present in ordinary atomic and nuclear interactions, but, as the name implies, they are very small compared to the electromagnetic and strong interactions, at least at low energy. The weak forces become relatively stronger as the energy is increased, and it is currently believed that at energies much higher than now available in accelerators the strong, electromagnetic and weak forces all become comparable in strength. Considering only low energy interactions, however, we can say that the weak interactions are extremely small compared to the electromagnetic and nuclear interactions, in fact, they are so small that they are quite difficult to detect even if one is looking for them. There has been some effort in the Berkeley Physics department to detect the effects of weak interactions in atomic physics, and these experiments are difficult. For most ordinary purposes at ordinary energies, the weak interactions can be ignored and all Hamiltonians for isolated systems conserve parity to an extremely high degree of accuracy.

It is, however, easy to create a system that does not conserve parity, simply by placing it in an external field. Such a system is no longer isolated, and parity need not be conserved. For example, suppose a particle of charge $q$ moving in a central force field is placed in an external, uniform electric field $\Evec_0$. Then the Hamiltonian is

:::{math}
:label: eq-parity-37
H={p^2 \over 2m} + V(r) - q\xvec\cdot\Evec_0.
:::

This does not commute with parity because the last term changes sign upon conjugation by parity.

In such cases, however, parity conservation is restored if we enlarge our definition of “the system” to include the charges creating the electric field. For example, if $\Evec_0$ is created by positive and negative charges arrayed along the parallel plates of a capacitor, and if these charges are included in “the system,” then $\pi$ will swap the positive and negative charges and reverse the direction of $\Evec_0$. Since $\xvec$ also changes sign, the whole Hamiltonian will once again be invariant under parity.

(sec-parity-8)=

## Parity and Energy Eigenstates in Isolated Systems

Suppose we have an isolated system with Hamiltonian $H$. As we have explained, in most applications $H$ commutes with parity to an extremely high degree of accuracy, so let us assume that $\pi H\pi^\dagger =H$, that is, $[\pi,H]=0$.

Since the system is isolated, $H$ commutes with all proper rotations, and is a scalar operator according to the definition {eq}`eq-transfop-8`. Then Theorem {ref}`thm-transfop-1` states that the energy eigenspaces consist of one or more irreducible subspaces under rotations, and the addendum says that, with few exceptions, they consist of precisely one irreducible subspace. So let us consider this generic case, for which each energy eigenvalue is associated with a definite $j$ value and has an energy eigenspace that is $2j+1$-fold degenerate.

As in {ref}`ch-repsamos`{} and \transfop{} let $\SS_{jm}$ be the eigenspace of operators $J^2$ and $J_3$ with quantum numbers $j$ and $m$, and let $\ket{\psi}$ be a bound energy eigenstate in the stretched subspace $\SS_{jj}$ with eigenvalue $E$, so that

:::{math}
:label: eq-parity-38
J^2\ket{\psi}=j(j+1)\hbar^2\,\ket{\psi}, \quad J_3\ket{\psi}=j\hbar\,\ket{\psi}, \quad H\ket{\psi}=E\ket{\psi},
:::

Under our assumptions of genericity, $H$ restricted to $\SS$ is nondegenerate, that is, $\ket{\psi}$ is the only state in $\SS_{jj}$ with the energy $E$.

Now $\pi$ commutes with $\Jvec$ and hence with $J^2$ and $J_z$, and so it can be restricted to $\SS_{jj}$. And since $\ket{\psi}$ is a nondegenerate eigenstate of $H$ and since $\pi$ commutes with $H$, according to Theorem {ref}`thm-hilbert-5`, $\ket{\psi}$ must also be an eigenstate of parity,

:::{math}
:label: eq-parity-39
\pi\ket{\psi}=e\ket{\psi},
:::

where $e=\pm1$. Theorem {ref}`thm-hilbert-5` does not tell us what the value of $e$ is.

Now it is easy to show that all the states obtained by applying lowering operators to $\ket{\psi}$ are also eigenstates of parity with the same eigenvalue $e$ as the stretched state. That is,

:::{math}
:label: eq-parity-40
\pi (J_-)^r \ket{\psi} = (J_-)^r \pi\ket{\psi} = e(J_-)^r\ket{\psi},
:::

for $r=1,2,\ldots,2j$. That is, all $2j+1$ degenerate energy eigenstates in the irreducible subspace have the same parity.

Thus the parity value can be associated with the energy level itself, just like the $j$ value. This is why the three nuclear states shown in Fig.~\figr\transfop.1 are assigned definite values of parity (all three, $\ironfiftyseven$, $\ironfiftyseven^\cc$ and $\ironfiftyseven^{\cc\cc}$, have negative parity).

In the case of nuclei, the energies, angular momenta (or spins) and parities of energy levels are determined experimentally, since theoretical calculations of these quantities are difficult. In atoms and molecules, theory is in better shape, and these quantities can be calculated with greater or lesser difficulty.

In the nongeneric case of the electrostatic model of hydrogen, it is not true that all energy eigenstates are eigenstates of parity. It is true that in central force motion each angular momentum value $\ell$ is associated with the definite parity $(-1)^\ell$ [see {eq}`eq-parity-52`], but since there are degeneracies of energy that cross angular momentum values, it is possible to form linear combinations of energy eigenstates of the same energy but opposite parity. For example, the $2s$ and $2p$ levels in hydrogen have the same energy but opposite parities. These facts play an important role in understanding the Stark effect, which is discussed in {ref}`ch-stark`.

(sec-parity-9)=

## Parity in One-Dimensional Systems

Consider a one-dimensional Hamiltonian,

:::{math}
:label: eq-parity-41
H={p^2\over 2m} + V(x).
:::

This commutes with parity if and only if $V(x)=V(-x)$, that is, if the potential is symmetric about $x=0$. Now in one-dimensional systems with a localized potential, the bound energy eigenstates are nondegenerate because the wave functions must vanish at $x=\pm\infty$. See {ref}`sec-topicsoned-2`. Therefore by Theorem {ref}`thm-hilbert-5`, the energy eigenstates must also be eigenstates of parity. That is, the bound energy eigenfunctions satisfy $\psi(x) = \pm \psi(-x)$, for some choice of sign that depends on the eigenfunction. For example, in the harmonic oscillator, which has the symmetric potential $V(x) = m\omega^2 x^2/2$, the $n$-th energy eigenfunction has parity $(-1)^n$. See \harmosc.6.

(sec-parity-10)=

## Considerations of Symmetry Raised by Parity

Parity illustrates some issues that arise whenever a Hamiltonian possesses a symmetry. Some of these have already been discussed in connection with rotations, but parity is a simpler symmetry so some of the ideas are easier to appreciate.

Whenever a Hamiltonian possesses a symmetry and we wish to diagonalize it or otherwise study its properties, it is a good idea to diagonalize the symmetry operators first. This is because symmetry operators are usually easier to diagonalize than Hamiltonians, and their eigenbases, sometimes called *symmetry-adapted* bases, are especially convenient for further study of the Hamiltonian. For example, in the case of rotational invariance, the symmetry adapted basis is the standard angular momentum basis $\ket{\gamma jm}$, an eigenbasis of $J^2$ and $J_z$.

Similarly, if a Hamiltonian commutes with parity, it may be convenient to study it in a basis which is an eigenbasis of parity. Since $\pi^2=1$, the eigenvalues $e$ satisfy $e^2=1$, or $e=\pm1$. Thus the Hilbert space is decomposed into two subspaces, the eigenspaces of parity with $e=\pm1$. We can call these the even and odd subspaces,

:::{math}
:label: eq-parity-42
\ES = \ES_even \oplus \ES_odd.
:::

Then a symmetry adapted basis consists of an orthonormal basis inside $\ES_even$ plus an orthonormal basis inside $\ES_odd$. We can write the basis vectors as $\ket{\gamma e}$, where

:::{math}
:label: eq-parity-43
\pi \ket{\gamma e} = e \ket{\gamma e},
:::

so that $e$ indicates which subspace the vectors lie in, and where $\gamma$ is a label of the orthonormal basis vectors inside $\ES_even$ (for $e=+1$) or inside $\ES_odd$ (for $e=-1$). This notation is similar to the notation $\ket{\gamma jm}$ which we used for a standard angular momentum basis, where the index $\gamma$ plays a similar role.

It is possible to write down projection operators that project onto the even and odd subspaces in terms of the parity operator itself. These are

:::{math}
:label: eq-parity-44
P_\pm = {1 \pm \pi \over 2}.
:::

It is easy to show that the operators $P_\pm$ satisfy the requirements of a projection operator (see {ref}`sec-hilbert-24`), and that when applied to an arbitrary state $\ket{\psi}$ (not necessarily an eigenstate of parity), they project it onto one or the other of the two subspaces, producing an eigenstate of parity of the eigenvalue indicated. For example, in a one-dimensional problem, if $\psi(x)$ is an arbitrary wave function (not necessarily even or odd), then

:::{math}
:label: eq-parity-45
(P_+\psi)(x) = {1\over 2}[\psi(x)+\psi(-x)]
:::

and

:::{math}
:label: eq-parity-46
(P_-\psi)(x) = {1\over 2}[\psi(x)-\psi(-x)]
:::

are the even and odd parts of $\psi(x)$, respectively.

The matrix elements of the Hamiltonian in the symmetry adapted basis are noteworthy. Assuming the Hamiltonian commutes with parity, we have

:::{math}
:label: eq-parity-47
\matrixelement{\gamma'e'}{H}{\gamma e} =\matrixelement{\gamma'e'}{\pi^\hc H \pi}{\gamma e} = e'e \,\matrixelement{\gamma'e'}{H}{\gamma e},
:::

which implies that the matrix element vanishes unless $e'e=1$. But this is equivalent to $e'=e$, so the Hamiltonian is diagonal in the parity quantum number $e$, and we have

:::{math}
:label: eq-parity-48
\matrixelement{\gamma'e'}{H}{\gamma e} = \delta_{e'e} \, C^e_{\gamma'\gamma},
:::

where $C^e_{\gamma'\gamma}$ just indicates the indices the nonvanishing matrix elements can depend on. This may be compared to {eq}`eq-wigeck-48`, which applies to Hamiltonians that are invariant under proper rotations. The fact that the matrix element vanishes if $e' \ne e$ is sometimes stated in words by saying that the Hamiltonian does not “connect” states of different parity.

In many cases it is necessary to diagonalize a Hamiltonian numerically, by setting up a matrix for it in some basis. There is the question, however, of what basis to use. If the Hamiltonian respects a symmetry then there is great advantage in using a symmetry adapted basis, since it reduces the size of the matrices that must be diagonalized. For example, in the parity-adapted basis $\ket{\gamma e}$, to diagonalize a Hamiltonian that commutes with parity we must diagonalize the two matrices $C^e_{\gamma'\gamma}$ with rows and columns indexed by $\gamma'$ and $\gamma$, for $e=\pm1$. Effectively we are diagonalizing the Hamiltonian separately in each of the subspaces $\ES_even$ and $\ES_odd$. If we arrange the basis vectors so that all the even vectors $\ket{\gamma,+1}$ come first, and all the odd vectors $\ket{\gamma,-1}$ come second, then the Hamiltonian matrix has the form,


where the upper (or even-even) block is the matrix $C^{+1}_{\gamma'\gamma}$, and the lower (or odd-odd) block is the matrix $C^{-1}_{\gamma'\gamma}$, and where $X$ indicates a non-zero block.

There are many numerical algorithms for diagonalizing a matrix, but a common one (the Householder algorithm) involves a computational effort that scales as $N^3$, where $N$ is the size of the matrix. Thus the effort to diagonalize two matrices of size $N/2$ is $2(N/2)^3 = N^3/4$, or about $1/4$ the effort of diagonalizing a single $N\times N$ matrix. This is the improvement in computational efficiency when using a symmetry adapted basis for a Hamiltonian that commutes with parity, as compared to diagonalizing the Hamiltonian in an arbitrary (nonsymmetric) basis.

(sec-parity-11)=

## Parity and Selection Rules

Parity gives rise to important selection rules which we will illustrate for the case of dipole transitions in an electrostatic model of a single-electron atom. The energy eigenfunctions are the usual ones in central force motion,

:::{math}
:label: eq-parity-50
\psi_{n\ell m}(r,\theta,\phi) = R_{n\ell}(r) Y_{\ell m}(\theta,\phi),
:::

which we shall write in ket language as $\ket{n\ell m}$. The matrix elements relevant to electric dipole transitions are

:::{math}
:label: eq-parity-51
\matrixelement{n'\ell'm'}{\xvec}{n\ell m}.
:::

We need to find the action of parity on the eigenstates $\ket{n\ell m}$. Since the radius $r$ is invariant under the replacement $\xvec \to -\xvec$, only the $Y_{\ell m}$ part of the wave function is affected by parity. The $Y_{\ell m}$'s have the property that if they are multiplied by $r^\ell$, where $r$ is the radius, then the result is a homogeneous polynomial in the Cartesian coordinates $x$, $y$ and $z$ of degree $\ell$. See {ref}`sec-orbamsph-8`. But since $x$, $y$ and $z$ all change sign under parity, and since the factor $r^\ell$ is invariant, the $Y_{\ell m}$ changes by $(-1)^\ell$ under parity. We summarize this by writing

:::{math}
:label: eq-parity-52
\pi\ket{n\ell m} = (-1)^\ell \ket{n\ell m}.
:::

The energy eigenfunctions {eq}`eq-parity-50` are also eigenfunctions of parity, with eigenvalue $(-1)^\ell$. This is often a useful fact. Notice that the eigenvalues do not depend on $m$. This was to be expected, since $\pi$ is a scalar operator, and according to the Wigner-Eckart theorem, the eigenvalues of a scalar operator do not depend on $m$. See {ref}`sec-transfop-9`.

Now using the fact that $\xvec$ is odd under parity, we can make some statements about the matrix element {eq}`eq-parity-51`. That is,

:::{math}
:label: eq-parity-53
\matrixelement{n'\ell'm'}{\xvec}{n\ell m} = -\matrixelement{n'\ell'm'}{\pi^\hc\xvec\pi}{n\ell m} = -(-1)^{\ell+\ell'} \matrixelement{n'\ell'm'}{\xvec}{n\ell m}.
:::

Thus, the matrix element {eq}`eq-parity-51` vanishes unless $-(-1)^{\ell+\ell'} = 1$, or

:::{math}
:label: eq-parity-54
\Delta \ell = \\textodd,
:::

where $\Delta \ell = \ell-\ell'$.

We see that the parity of the atomic state must change under an electric dipole transition. This selection rule is known as *Laporte's rule*. Initially it was observed experimentally, and later it was explained by Wigner on the basis of parity. As noted above, Laporte's rule is equivalent to the statement that the intrinsic parity of the photon is negative.

In the case of the matrix element {eq}`eq-parity-51`, the Wigner-Eckart theorem gives the selection rule $\Delta\ell = 0,\pm1$, that is, these are the values of $\Delta \ell$ allowed by rotational invariance alone. But parity excludes the value $\Delta\ell =0$, so the final selection rule is $\Delta\ell=\pm1$.

\problems

(prob-parity-1)=

**Problem \prbdparity-1..** 

We did not discuss the spin angular functions in class, but these are spinor functions on the unit sphere that arise when we combine orbital and spin angular momentum for a central force problem for a spinning particle. Here we will take the case $s=\frac{1}{2}$ (for example, in hydrogen). Let $\ket{n\ell m_\ell}$ be ket language for the wave function $R_{n\ell}(r) Y_{\ell m_\ell}(\theta,\phi)$, the solution of the Schr\"odinger equation for a spinless particle in a central force field, and let $\ket{s m_s}$ be the usual spin states (here $s=\frac{1}{2}$ and $m_s = \pm \frac{1}{2}$). We distinguish between $m_\ell$ and $m_s$, the two types of magnetic quantum numbers. We multiply the wave functions times the spin functions and form linear combinations with the Clebsch-Gordan coefficients to get eigenstates of $J^2$ and $J_z$, where $\Jvec=\Lvec+\Svec$. These are

:::{math}
:label: eq-parity-55
\ket{n\ell j m_j} = \sum_{m_\ell,m_s} \ket{n\ell m_\ell} \ket{s m_s} \braket{\ell s m_\ell m_s}{j m_j}.
:::

The spatial wave functions $\psi_{n\ell m_\ell}(\xvec) =R_{n\ell}(r) Y_{\ell m_\ell}(\theta,\phi)$ factor into a radial part times an angular part. Let us write this in ket language as $\ket{n\ell m_\ell} = \ket{n \ell} \ket{\ell m_\ell}$. The factor $R_{n\ell}(r)$ or $\ket{n\ell}$ is the same for all terms in the sum above, so it can be taken out and what is left is a two-component spinor that depends only on the angles. This is what in wave function language Sakurai calls ${\cal Y}^{j m_j}_\ell$; in ket language we will write

:::{math}
:label: eq-parity-56
\ket{\ell j m_j} = \sum_{m_\ell m_s} \ket{\ell m_\ell} \ket{s m_s} \braket{\ell s m_\ell m_s}{j m_j}.
:::

\problempart{(a)} For the case $\ell=0$, $j=\frac{1}{2}$, $m_j=\frac{1}{2}$, write out the two-component spinor ${\cal Y}^{j m_j}_\ell$ as functions of $(\theta,\phi)$.

\problempart{(b)} Multiply this by $\sigmavec\cdot\xvec$, and express the result as a linear combination of other spin angular functions ${\cal Y}^{j m_j}_\ell$.

\problempart{(c)} Certain values of $j$, $m_j$ and $\ell$ occur in the sum, and certain others do not. Use symmetry principles to explain why the values that occur are allowed and the others are not.

**Hint:** It may help to think of three kinds of rotations: spin rotations, orbital rotations, and total (spin plus orbital) rotations.

(prob-parity-2)=

**Problem \prbdparity-2..** 

Because of weak (neutral-current) interactions, there is a parity-violating potential between the atomic electron and the nucleus as follows:

:::{math}
:label: eq-parity-57
V=\lambda[\delta(\xvec)\,\Svec\cdot\pvec + \Svec\cdot\pvec\, \delta(\xvec)],
:::

where $\Svec$ and $\pvec$ are the spin and momentum operators of the electron, and the nucleus is assumed to be situated at the origin. As a result, the ground state of an alkali atom, usually characterized by $\ket{n\ell jm}$, actually contains very tiny contributions from other eigenstates as follows:

:::{math}
:label: eq-parity-58
\ket{n\ell jm} \to \ket{n\ell jm} + \sum_{n'\ell'j'm'} C_{n'\ell'j'm'}\, \ket{n'\ell'j'm'},
:::

On the basis of symmetry considerations alone, what can you say about the values of $(n'\ell'j'm')$ that give rise to nonvanishing contributions? Suppose the radial wave functions and energy levels are all known. Indicate how you can calculate $C_{n'\ell'j'm'}$. Are there any further restrictions on $(n'\ell'j'm')$ that go beyond those due to symmetry considerations?

(prob-parity-3)=

**Problem \prbdparity-3..** 

A collection of $N\ge3$ nuclei is distributed in the $x$-$y$ plane. They do not lie on a line. Nucleus $i$ has position $\Rvec_i=(R_{ix},R_{iy},0)$. The positions of the nuclei are fixed. An electron moves in the field of these nuclei.

Let $A$ be the reflection in the $x$-$y$ plane. It is represented by the matrix

:::{math}
:label: eq-parity-59
\begin{aligned}
\Amat=\begin{pmatrix}1 & 0 & 0\\ 0 & 1 & 0\\ 0 & 0 & -1\\\end{pmatrix},
\end{aligned}

:::

which maps $(x,y,z)$ into $(x,y,-z)$. The electrostatic potential $\Phi(\xvec)$ of the nuclei is invariant under reflection in the $x$-$y$ plane, that is,

:::{math}
:label: eq-parity-60
\Phi(x,y,z) = \Phi(x,y,-z),
:::

or

:::{math}
:label: eq-parity-61
\Phi(\Amat\xvec) = \Phi(\xvec)
:::

for short.

:::{figure} images/parity-fig01.png
:label: fig-parity-1
:width: 80%

The $x$-$y$ plane, viewed from the side. The spots in the $x$-$y$ plane are the nuclei. $\xvec$ is a typical point, and $\Amat\xvec$ is the reflection of this point through the $x$-$y$ plane. The figure illustrates Eqs. {eq}`eq-parity-62` and {eq}`eq-parity-63`.
:::

From $\Evec=-\del\Phi$ and {eq}`eq-parity-60` or {eq}`eq-parity-61` it follows that

:::{math}
:label: eq-parity-62
\begin{pmatrix}E_x(x,y,-z)\\  E_y(x,y,-z)\\  E_z(x,y,-z)\\\end{pmatrix} = \begin{pmatrix}E_x(x,y,z)\\  E_y(x,y,z)\\  -E_z(x,y,z)\\\end{pmatrix},
:::

or

:::{math}
:label: eq-parity-63
\Evec(\Amat\xvec)=\Amat\Evec(\xvec)
:::

for short. This also follows by inspection of {ref}`fig-parity-1`.

\problempart{(a)} Every improper rotation can be written as $\Pmat \Rmat({\hat{\mathbf{n}}},\theta)$, where $\Pmat$ is given by {eq}`eq-parity-1` and $\Rmat({\hat{\mathbf{n}}},\theta)$ is a proper rotation in axis-angle form. Write

:::{math}
:label: eq-parity-64
\Amat=\Pmat\Rmat({\hat{\mathbf{n}}},\theta)
:::

and identify ${\hat{\mathbf{n}}}$ and $\theta$.

\problempart{(b)} Is $\Phi(\xvec)$ a scalar operator? Is $\Evec(\xvec)$ a vector operator?

\problempart{(c)} In the electrostatic approximation the Hamiltonian for the electron is

:::{math}
:label: eq-parity-65
H_0={\pvec^2\over 2m} + V(\xvec),
:::

where

:::{math}
:label: eq-parity-66
V(\xvec) = -e\Phi(\xvec).
:::

Define a unitary operator $W$ that acts on the Hilbert space of the electron and that corresponds to $\Amat$ above in some reasonable way. I suggest you denote the usual parity operator by $\Pi$, to avoid confusion with the angle $\pi$. You may find it convenient to refer to different types of rotation operators,

:::{math}
:label: eq-parity-67
\begin{aligned}
U_o({\hat{\mathbf{n}}},\theta) &= e^{-i\theta{\hat{\mathbf{n}}}\cdot\Lvec/\hbar} \qquad {\rm(orbital)}, \\
U_s({\hat{\mathbf{n}}},\theta) &= e^{-i\theta{\hat{\mathbf{n}}}\cdot\Svec/\hbar} \qquad {\rm(spin)}, \\
U_t({\hat{\mathbf{n}}},\theta) &= e^{-i\theta{\hat{\mathbf{n}}}\cdot\Jvec/\hbar} \qquad {\rm(total)}, \\

\end{aligned}
:::

as needed, where $\Jvec=\Lvec+\Svec$.

Work out the conjugation relations,

:::{math}
:label: eq-parity-68
W^\dagger \begin{pmatrix}x\\ y\\ z\\\end{pmatrix} W, \qquad and \qquad W^\dagger \begin{pmatrix}p_x \\ p_y\\ p_z\\\end{pmatrix} W,
:::

or simply $W^\dagger \xvec W$ and $W^\dagger \pvec W$ for short. Note that for any function $f(\xvec)$,

:::{math}
:label: eq-parity-69
W^\dagger f(\xvec)W =f\bigl(W^\dagger \xvec W\bigr).
:::

The $W$ you define should satisfy

:::{math}
:label: eq-parity-70
W^\dagger H_0 W=H_0.
:::

If it does not, go back and change the definition so that it does. Notice that since you defined $W$ to be unitary, this is equivalent to $[W,H_0]=0$.

\problempart{(d)} So the system is invariant under reflection in the plane, and we have found an operator corresponding to that reflection that commutes with the electrostatic Hamiltonian $H_0$. Now we will see if the symmetry persists when we include relativistic corrections.

The spin-orbit Hamiltonian worked out in {ref}`ch-finestruc`{} [see {eq}`eq-finestruc-13`] applies only in the case of a radial electric field. The more general expression [see {eq}`eq-foldyw-49`] is

:::{math}
:label: eq-parity-71
H_{SO} = {e\over 4m^2c^2} \bigl[\Evec(\xvec)\cross\pvec - \pvec\cross\Evec(\xvec)\bigr] \cdot\Svec,
:::

where the quantity in the square brackets is the sum of an operator and its Hermitian conjugate, to make $H_{SO}$ Hermitian.

Does the operator $W$ you defined in part~(c) commute with $H_{SO}$? If not, modify it so that it does, and call the new operator $X$. Make sure it is still unitary. Depending on your choice of $W$ it is possible that no modification is necessary, then $X=W$. If $X\ne W$, reconsider the commutation relations {eq}`eq-parity-68`. Also work out the commutation relations

:::{math}
:label: eq-parity-72
X^\dagger\begin{pmatrix}E_x(\xvec)\\ E_y(\xvec)\\ E_z(\xvec)\\\end{pmatrix}X \qquad and \qquad X^\dagger\begin{pmatrix}S_x \\ S_y\\ S_z\\\end{pmatrix}X,
:::

or $X^\dagger \Evec(\xvec)X$ and $X^\dagger\Svec X$ for short. Hint: notice that $[(\Rmat\Avec)\cross(\Rmat\Bvec)]\cdot(\Rmat\Cvec) = (\Avec\cross\Bvec)\cdot\Cvec$, for all proper rotations $\Rmat$ and all vectors $\Avec$, $\Bvec$, $\Cvec$. See Prob. {ref}`prob-classrot-2`.

\problempart{(e)} In quantum mechanics we like Hermitian operators that commute with the Hamiltonian, because they possess simultaneous eigenbases, and for other reasons. The operator $X$ you found in part~(d) should be unitary. Find a simple expression for $X^2$.

Is the $X$ you found in part~(d) Hermitian? If not, make a simple modification to it to create a new operator, call it $K$, that is both unitary and Hermitian and that commutes with $H$. If no modification is necessary, then $K$ will be the same as $X$ obtained in part~(d). If $K$ is both unitary and Hermitian, then its its eigenvalues must be $\pm1$. Show that this is so.

Let the electron wave function be

:::{math}
:label: eq-parity-73
\psi = \begin{pmatrix}\psi_+(x,y,z)\\ \psi_-(x,y,z)\\\end{pmatrix}.
:::

Find the $\pm$ components of the wave function $K\psi$, and find the conditions that $\psi_+$ and $\psi_-$ must satisfy in order that $\psi$ be an eigenfunction of $K$ with eigenvalues $\pm1$.

Thus the Hilbert space breaks up into two orthogonal eigenspaces of $K$, which we denote by ${\cal E}_\pm$, where $k=\pm1$ is the eigenvalue of $K$. Write this as

:::{math}
:label: eq-parity-74
{\cal E} = {\cal E}_+ \oplus {\cal E}_-.
:::

This system and its symmetry become more interesting when time reversal is added to the mix of symmetries. See the continuation of this problem in Prob. {ref}`prob-timerev-6`.
