---
title: "40. The Classical Electromagnetic Field Hamiltonian"
---
(ch-classemf)=

# 40. The Classical Electromagnetic Field Hamiltonian

(sec-classemf-1)=

## Introduction

In these notes we motivate the necessity for quantizing the electromagnetic field, we outline a procedure for doing that, and then we carry out the classical part of that procedure, which is to find a classical Hamiltonian for the combined system of matter plus electromagnetic field. In a subsequent set of notes we shall quantize this classical Hamiltonian and study the results. Standard references for the material in these notes include Heitler, *The Quantum Theory of Radiation* and Cohen-Tannoudji, Dupont-Roc and Grynberg, *Photons and Atoms*.

(sec-classemf-2)=

## The Electrostatic (Coulomb) Model, its Limitations and Generalizations

So far in this course we have mostly used an electrostatic or Coulomb model to describe the interactions of charged particles with one another. In this model, a charged particle responds to the electric field $\Evec = -\del \Phi$ evaluated at the position of the particle, where the electrostatic potential $\Phi$ is determined by the instantaneous (non-retarded) positions of all the other charged particles. The potential $V=q\Phi$, where $q$ is the charge of the particle, enters into the particle Hamiltonian. This model omits a number of important physical effects, including the magnetic fields produced by the moving charges, the effects of retardation (finite velocity of propagation of signals between the charged particles), and radiation.

If the velocities are low and the distances between particles not too great, then the dominant (quasi-static) part of the magnetic interactions between charged particles can be taken into account by adding certain velocity-dependent terms to the classical Lagrangian, resulting in the so-called *Darwin Lagrangian*. In the Darwin Lagrangian, magnetic fields are treated in a similar manner to electrostatic fields: the magnetic field at some (field) point in space is determined by the instantaneous (nonretarded) positions and velocities of the charged particles. We will not use the Darwin Lagrangian explicitly in this course, but its spirit was very much with us when we computed the spin-orbit corrections to the atomic Hamiltonian in {ref}`ch-finestruc`. In multi-electron atoms, there are other effects of a similar nature, for example, the orbital motion of one electron is influenced by the $\vvec \cross \Bvec$ force due to the magnetic field produced by the motion of the other electrons. These effects are small (they are part of the fine-structure terms), a sign that the electrostatic model is a good first approximation.

In both the electrostatic and Darwin models, the fields are definite functions of the instantaneous (non-retarded) particle positions and velocities, so the dynamics of the particles can be described by a Hamiltonian containing only the particle degrees of freedom. Only Hamiltonians of this sort have been considered up to this point in this course. These models, however, are incapable of representing effects such as retardation and radiation.

As for retardation, its effects are small for nonrelativistic systems of small spatial extent, so the electrostatic model is often quite a good one, but the question remains as to how we would treat those effects if we wished to. In fact, in multielectron atoms retardation effects are of the same order as the fine structure, and must be taken into account for a fully satisfactory theoretical treatment of the fine structure.

Radiation is also a small effect in ordinary atoms, in the sense that the probability of emitting a photon is small during a single rotational period of an electron in an excited state. Nevertheless, over a large number of rotational periods radiation becomes a near certainty, and an atom in an excited state will make a transition to a lower energy state. But there is no hint of this in the electrostatic or Darwin models, either in classical mechanics or in quantum mechanics. For example, in quantum mechanics, these models predict that excited states of atoms are stationary states, that is, energy eigenstates, with an infinite lifetime. Similarly, in classical mechanics in the electrostatic model two charged particles orbit each other in Kepler ellipses forever without emitting any radiation. The inclusion of magnetic effects through a Darwin model modifies the orbits but does not lead to radiation.

In books on classical electromagnetic theory, there are typically two kinds of problems encountered. In one, the electromagnetic field is given and it is desired to compute the trajectories of the particles that respond to this field. In the other, the currents and/or charges are given, and it is desired to compute the fields produced. For example, this is how the radiation field produced by accelerated charged particles is usually computed: One assumes that the trajectory of a charged particle is given, with given velocity and acceleration at any instant of time. This implies a certain charge and current density in space, which are then used as sources in Maxwell's equations, from which the total fields can be computed. These fields are dominated by radiation at large distances, while for low velocity particles at short distances they are dominated by non-retarded Coulomb or Coulomb-plus-Darwin fields.

In reality, however, fields and the particles act on each other, and the dynamics of the combined field-particle system must be solved for a fully realistic account. This is not an easy problem in classical electrodynamics, which explains why books on the subject usually avoid it or simplify it in various ways. There are no nontrivial exact solutions of the equations of motion for the coupled field-particle system, and approximate solutions require some small parameter. We shall find a similar situation in quantum mechanics as well, where fortunately for our applications there is a small parameter (the fine structure constant $\alpha \approx 1/137$) that serves as a perturbation parameter.

Moreover, at the classical level there is a fundamental difficulty with the formulation of the interactions of charged particles with electromagnetic fields, namely the infinite self-energy of a point particle. This difficulty cannot be cured at the classical level, and all classical models that incorporate the point nature of charged particles are ultimately inconsistent. These infinities played a central role in the history of quantum electrodynamics, as we shall explain below.

These considerations indicate that in order to incorporate effects such as retardation and radiation into quantum mechanics, it will be necessary to describe the coupled dynamics of the matter plus the field. This cannot be done with a Hamiltonian that contains only the matter degrees of freedom; instead, it will be necessary to include the field degrees of freedom as well. Doing this, however, requires some additional formalism, so in introductory courses in quantum mechanics the emission and absorption of radiation is usually discussed within a simplified model that we now describe.

(sec-classemf-3)=

## The Semiclassical Theory of Radiation

In classical mechanics a charged particle responds to the forces produced on it by an electromagnetic field, absorbing energy from the field and returning some energy back to it in the form of radiation. Thus the field is modified by the presence of the particle. But if the field is strong it may be possible to ignore the effect of the particle back on the field, and to treat the particle as if it were moving in some given field.

Similarly, in quantum mechanics we can study the effect of a strong electromagnetic field on a system of charged particles by assuming that the fields are given functions of space and time, with given “external” potentials $\Phi(\xvec,t)$ and $\Avec(\xvec,t)$. We do not worry too much about the sources of the external fields in such applications, because we ignore the reaction of our system back on those sources, which are not included as a part of the system under consideration. For example, we may consider an atom interacting with a light wave produced by a laser, or a magnetic field produced by currents in a coil. In such cases, the effects of the external field on a quantum mechanical system of charged particles is described by incorporating the external potentials $\Phi$ and $\Avec$ into the particle Hamiltonian. This is what we did in studying the Stark and Zeeman effect in {ref}`ch-stark`\ and \zeeman, and spin precession in {ref}`ch-spinmagf`.

If the external field is a radiation field, then the model is called the *semiclassical theory of radiation*, since the matter is treated by quantum mechanics but the field is treated classically. We studied an example of the semiclassical theory of radiation in our treatment of the photoelectric effect in {ref}`ch-photelec`. That will be the only example considered in this course.

The semiclassical theory of radiation can describe rather easily the absorption of radiation by systems of charged particles, since the particles just respond to the forces of the external field, which changes their dynamical state. This is how we used this theory in our study of the photoelectric effect. It is not so easy to describe the emission of radiation within the semiclassical theory of radiation, but that can also be done in an *ad hoc* manner. The procedure involves combining the results for absorption with some kinetic theory (in the form of the Einstein $A$- and $B$-coefficients), statistical mechanics, and random phase assumptions. In this manner one can calculate the rate of emission of radiation (the power emitted) by a system of charged particles, both in the presence of an external field (stimulated emission), and in its absence (spontaneous emission). The argument is tricky and convoluted, and ultimately inconsistent, since the currents produced by the quantum system are ignored in Maxwell's equations. Nevertheless, the semiclassical theory of radiation is definitely useful, and you will doubtlessly see it again if you study quantum optics or related subjects.

At a more fundamental level, however, the semiclassical theory of radiation is definitely unsatisfactory. Even if it were possible to restore self-consistency in the emission and absorption of radiation (to include the quantized particle currents and charges as sources of the field), the problem remains that the field is treated by classical mechanics, that is, the classical Maxwell equations, while the matter is treated by quantum mechanics. Thus we have a system in which some degrees of freedom are treated classically, while other are treated quantum mechanically. Any such hybrid classical-quantum model leads immediately to interpretational difficulties, for example, by making measurements on the classical degrees of freedom it becomes possible to violate the uncertainty principle in the quantum degrees of freedom. In the present case, if we can measure a classical electromagnetic field at a given point of space and time with arbitrary precision (the usual assumption in classical electromagnetic theory), then we can identify the position and velocity of the charged particle that produced that field to arbitrary precision. In actuality, measurements of field strengths are made by observing the forces on charged particles, which themselves obey the laws of quantum mechanics. The implications of quantum mechanics for the measurement of electromagnetic field quantities were examined in a famous 1933 paper by Bohr and Rosenfeld (English translation available in *Quantum Theory and Measurement*, by J. A. Wheeler and W. H. Zurek), which is a primary reference for these kinds of questions.

(sec-classemf-4)=

## The Necessity of Quantizing the Electromagnetic Field

Thus we cannot expect that any hybrid classical-quantum model will bring us enlightenment into the fundamental physics of the interactions of charged particles and electromagnetic fields. Instead, we expect that a proper understanding will require that both field and matter be treated by quantum mechanics. We know how to do this for the matter, at least in the nonrelativistic approximation, but the usual (classical) description of the electromagnetic field as a field of $c$-numbers (the values of $\Evec$ and $\Bvec$ that can be measured with arbitrary precision) must be replaced by a quantum description.

We can already see some outlines of the resulting theory without doing much work. For example, one of the postulates of quantum mechanics is that every measurement process corresponds to a Hermitian operator acting on some ket space, and that the possible outcomes of the measurement are the eigenvalues of that operator. These outcomes are assigned probabilities by the rules of quantum mechanics, which describe the statistical results of measurements on an ensemble of identically prepared systems. In addition, in general different observables are not compatible, that is, they cannot be measured simultaneously with infinite precision. See {ref}`ch-postulat`\ and \density. Thus we must expect that in the quantum theory of the electromagnetic field, measurements of $\Evec$ and $\Bvec$ are associated with some operators that act on some ket space, and that these measurements will exhibit statistical fluctuations and obey some uncertainty relations. In the quantum theory of the electromagnetic field, the $c$-number (real-valued) fields $\Evec$ and $\Bvec$ that form the basis of classical electromagnetic theory are replaced by *operator-valued* fields (actually, vectors of operators). These will be our first examples of *quantum fields*.

Now a few remarks about the history of quantum electrodynamics. Quantum mechanics was born in 1900 with Planck's derivation of the correct formula for the black body spectrum. Although no one at the time fully understood Planck's result, nevertheless it was clear that the electromagnetic field must obey some kind of quantum laws that are distinct from those of classical electromagnetic theory. Indeed, the classical theory predicts an “ultraviolet catastrophe,” that is, an infinite energy density, for radiation in thermal equilibrium with a heat bath. It was not until 1925 that the first reasonably complete formulation of quantum mechanics came about, and almost immediately, in two papers in 1926, Jordan made the first attempts at quantizing the electromagnetic field. By 1927 Dirac had laid out the basis of quantum electrodynamics, much as we shall study it in this course. This early version of quantum electrodynamics gave physically meaningful results for the interactions of charged particles with the electromagnetic field at lowest order of perturbation theory. These results were able to explain a wide array of phenomena involving the interactions of matter with radiation.

Subsequent developments were not all smooth sailing, however. By the early 1930's it had become apparent that quantum electrodynamics, as it was then understood, led inevitably to infinities in higher order perturbation theory. Some of these infinities were quantum versions of the infinite self-mass of the point particle that had already been a problem in classical electrodynamics, but in addition it turned out in the quantum theory that particles have an infinite charge. These difficulties were a major preoccupation of theoretical physics during the first twenty years of quantum electrodynamics (roughly 1927 to 1948). Some physicists thought that the classical theory should first be cured of its infinities before applying quantum mechanics, while others thought that quantum mechanics itself should be replaced by a more fundamental theory. In the end, it turned out that quantum mechanics, combined with an insistence on relativistic covariance and gauge invariance, led to a set of rules for consistently removing the infinities from quantum electrodynamics to all orders of perturbation theory. This was the renormalization program due to Feynman, Schwinger, Tomonaga and Dyson. We shall cover some of the basic ideas of renormalization later in the course, when we study Bethe's derivation of the Lamb shift. The result is the modern theory of quantum electrodynamics, which has served as a model for the quantum theory of other fundamental interactions (for example, quantum chromodynamics or QCD, the modern theory of the strong interactions, or the electroweak theory, which unifies the electromagnetic and weak interactions, both of which reached maturity in the 1970's). See the book *QED and the Men Who Made It*, by Silvan Schweber, for more details about the fascinating history of quantum electrodynamics.

Granted that we must quantize the electromagnetic field, the question is how to do it. More generally, given a classical description of any dynamical system, how do we go over to the proper quantum mechanical treatment? No deductive procedure can be given, since quantum mechanics has more physics in it than does classical mechanics, and in fact this is often a nontrivial question. For example, although the classical theory of the gravitational field (Einstein's general relativity) has been known for over a hundred years, it is still not certain what the correct quantum version of this theory should be.

Nevertheless, if we follow the procedure that is known to work for nonrelativistic material systems, it would run something like this. First we find the classical equations of motion, which we write in the form ${\ddot q}_i = \ldots$, where the $q_i$'s are the generalized coordinates of the classical system. This is basically a version of Newton's laws ($\Fvec = m\avec$). Next we find a classical Lagrangian $L(q,{\dot q})$ that gives the classical equations of motion as the Euler-Lagrange equations. Next we convert the Lagrangian into a classical Hamiltonian $H(q,p)$, by means of the Legendre transformation. Finally, we use the prescription of Dirac, which replaces the $q$'s and $p$'s of the classical system by operators satisfying the canonical commutation relations, $[q_i, p_j] = i\hbar\,\delta_{ij}$. This last step is not unique, because multiplication of classical observables is commutative, while that of quantum observables is not, and in any case there may be physical effects of a quantum nature that are not suspected at the classical level (for example, spin). The validity of the resulting quantum mechanical description must be checked by comparison with experiment.

In these notes we shall follow an abbreviated route through this process, skipping the classical Lagrangian stage, and going directly from the equations of motion to the classical Hamiltonian by a series of guesses. We shall do this both for the free electromagnetic field (one for which there are no sources), and for the field interacting with matter. In a subsequent set of notes we shall quantize the resulting classical Hamiltonian to obtain a quantum mechanical description of the combined matter-field system.

(sec-classemf-5)=

## The Equation of Motion

The equations of motion are Maxwell's equations. We break these into the homogeneous equations,

:::{math}
\begin{aligned}
\del\cross\Evec &= -{1\over c}\frac{\partial \Bvec}{\partial t},
\end{aligned}
:::

:::{math}
:label: eq-classemf-1
\begin{aligned}
\del\cdot\Bvec&=0,
\end{aligned}
:::

and the inhomogeneous equations (the ones driven by the charges and currents),

:::{math}
\begin{aligned}
\del\cdot\Evec &=4\pi\rho,
\end{aligned}
:::

:::{math}
:label: eq-classemf-2
\begin{aligned}
\del\cross\Bvec &= {4\pi\over c} \Jvec + {1\over c} \frac{\partial \Evec}{\partial t}.
\end{aligned}
:::

See Appendix~\emunits. These equations are first order in time. The charge density $\rho$ and the current density $\Jvec$ satisfy the continuity equation,

:::{math}
:label: eq-classemf-3
\frac{\partial \rho}{\partial t} + \del\cdot\Jvec =0.
:::

The homogeneous Maxwell equations imply the existence of scalar and vector potentials, $\Phi$ and $\Avec$, respectively, such that

:::{math}
:label: eq-classemf-4a
\begin{aligned}
\Evec &= -\del\Phi-{1\over c}\frac{\partial \Avec}{\partial t},
\end{aligned}
:::

:::{math}
:label: eq-classemf-4b
\begin{aligned}
\Bvec &= \del\cross\Avec.
\end{aligned}
:::

The potentials are not unique, but may be subjected to a *gauge transformation*, that is, $\Phi$ and $\Avec$ may be replaced by $\Phi'$ and $\Avec'$, where

:::{math}
:label: eq-classemf-5a
\begin{aligned}
\Phi' &= \Phi -{1\over c} \frac{\partial \chi}{\partial t},
\end{aligned}
:::

:::{math}
:label: eq-classemf-5b
\begin{aligned}
\Avec' &= \Avec + \del\chi,
\end{aligned}
:::

for any scalar field $\chi$, and {eq}`eq-classemf-4a` are still satisfied. We will call $\chi$ the “gauge scalar.” Since the physical fields $\Evec$ and $\Bvec$ are not modified by a gauge transformation, we may say that the potentials $\Phi$ and $\Avec$ contain both a physical part (because the physical fields can be computed from them) and a nonphysical part (which changes when we do a gauge transformation). Expressions~{eq}`eq-classemf-4a` cause the homogeneous Maxwell equations to be satisfied identically, while the inhomogeneous Maxwell equations become

:::{math}
:label: eq-classemf-6a
\begin{aligned}
\del^2\Phi &= -4\pi\rho -{1\over c}\pop{}{t}(\del\cdot\Avec),
\end{aligned}
:::

:::{math}
:label: eq-classemf-6b
\begin{aligned}
\del^2 \Avec - {1\over c^2} {\partial^2 \Avec \over \partial t^2} &= -{4\pi\over c}\Jvec +\del\Bigl( {1\over c}\frac{\partial \Phi}{\partial t} + \del\cdot\Avec\Bigr).
\end{aligned}
:::

These are the classical equations of motion of the electromagnetic field in terms of the potentials.

We now ask, what are the $q$'s (the generalized coordinates) for the electromagnetic field? A hint comes from mechanical systems, where the $q$'s satisfy differential equations that are second order in time. This suggests that the $q$'s of the electromagnetic field are not the components of $\Evec$ or $\Bvec$, which by Maxwell's equations {eq}`eq-classemf-1` and {eq}`eq-classemf-2` obey equations that are first order in time. Instead, the suggestion is that the $q$'s are related to the vector potential $\Avec$, which by {eq}`eq-classemf-6b` obeys an equation that is second order in time. The potentials, however, are not unique, so before we quantize we will decide on a gauge convention, that is, a convention that fixes the nonphysical part of the potentials.

(sec-classemf-6)=

## Coulomb Gauge

It turns out that the most satisfactory gauge for our purposes is Coulomb gauge, defined by the condition

:::{math}
:label: eq-classemf-7
\del\cdot\Avec = 0.
:::

It is shown in courses on electromagnetic theory that Coulomb gauge always exists, that is, given an arbitrary set of potentials $\Phi$, $\Avec$, there always exists a gauge scalar $\chi$ such that the new potentials defined by {eq}`eq-classemf-5a` satisfy the Coulomb gauge condition {eq}`eq-classemf-7`.

A gauge convention such as the Coulomb gauge condition {eq}`eq-classemf-7` is ultimately nonphysical, that is, no physical results can depend on the choice of gauge. But the structure of the theory and the nature of the calculations we do are strongly influenced by the choice of gauge. We will now discuss the advantages and disadvantages that Coulomb gauge offers for the purposes of quantizing the electromagnetic field.

One disadvantage of Coulomb gauge is that it is not Lorentz covariant. If the Coulomb gauge condition {eq}`eq-classemf-7` holds in one Lorentz frame, it does not hold in another. Maxwell's equations themselves are Lorentz covariant, and if the matter is also treated relativistically, then all physical results will be Lorentz covariant regardless of the gauge we use. But the use of a noncovariant gauge means that covariance will not be evident at intermediate stages of the calculation. As we say, we do not have *manifest* Lorentz covariance when using Coulomb gauge. This will not bother us too much in our initial applications, which will involve the interactions of the electromagnetic field with nonrelativistic matter, described by the usual Schr\"odinger equation, but it would be a greater concern in any attempt to formulate a covariant approach to the quantization of the electromagnetic field.

Another disadvantage of Coulomb gauge is that it disguises somewhat the effects of retardation. We will discuss this later in more detail.

A third disadvantage of Coulomb gauge is that the quantum field theory that results upon quantization leads to infinities in higher order perturbation theory. The difficulty of these infinities and the history of their resolution were discussed briefly above. Here it is worth mentioning that the approach that finally led to success was one that was explicitly Lorentz covariant and gauge invariant at each step (so, in particular, Coulomb gauge is not a suitable starting point for understanding renormalization in quantum electrodynamics).

An advantage of Coulomb gauge is that in the case of low velocity systems of limited spatial extent, it captures the dominant, electrostatic effects in simple terms. This is the case for most systems of interest in atomic, molecular and nuclear physics. That is, Coulomb gauge builds naturally on the electrostatic model discussed above, which we know works well up to a point. For many systems of interest to us, Coulomb gauge gives us good unperturbed Hamiltonians.

A second advantage of Coulomb gauge is that it provides the simplest route to the quantization of the electromagnetic field, that is, the route with the least amount of additional formalism that must be mastered. It is therefore preferred in introductory treatments. This advantage is decisive for our purposes.

To understand electrodynamics in Coulomb gauge, it is necessary to understand the concepts of transverse and longitudinal vector fields. We now make a digression into this subject.

(sec-classemf-7)=

## Transverse and Longitudinal Vector Fields

Let $\Fvec(\xvec)$, $\Gvec(\xvec)$, etc., be vector fields in $\xvec$-space, where we suppress any time-dependence. We will normally take these vector fields to be real. We define the Fourier transforms of such vector fields by

:::{math}
\begin{aligned}
\tilde\Fvec(\kvec) &= \int {d^3\xvec\over (2\pi)^{3/2}} \, e^{-i\kvec\cdot\xvec} \, \Fvec(\xvec),
\end{aligned}
:::

:::{math}
:label: eq-classemf-8
\begin{aligned}
\Fvec(\xvec) &= \int {d^3\kvec \over (2\pi)^{3/2}} \, e^{i\kvec\cdot\xvec} \, \tilde\Fvec(\kvec),
\end{aligned}
:::

where we use tildes to denote quantities in $\kvec$-space. Our conventions for Fourier transforms balance the $2\pi$'s in the forward and inverse transformation (these are the same conventions we used in {ref}`ch-tdpt`, see {eq}`eq-tdpt-78`. The Fourier transformed field $\tilde\Fvec$ is complex, but it satisfies the identity,

:::{math}
:label: eq-classemf-9
\tilde\Fvec(\kvec) = \tilde\Fvec(-\kvec)^\cc,
:::

on account of the reality of $\Fvec$ in $\xvec$-space. With these conventions for the Fourier transform, the Parseval identity has the form,

:::{math}
:label: eq-classemf-10
\int d^3\xvec \, \Fvec(\xvec)\cdot\Gvec(\xvec) = \int d^3\kvec \, \tilde\Fvec(\kvec)^\cc \cdot \tilde\Gvec(\kvec).
:::

An arbitrary vector field in $\kvec$-space can be decomposed into its longitudinal and transverse parts, which are respectively parallel and perpendicular to $\kvec$. That is, we write

:::{math}
:label: eq-classemf-11
\tilde\Fvec(\kvec) = \tilde\Fvec_\perp(\kvec) +\tilde\Fvec_\parallel(\kvec),
:::

where

:::{math}
:label: eq-classemf-12
\tilde\Fvec_\parallel(\kvec) = {1\over k^2} \kvec [\kvec\cdot\tilde\Fvec(\kvec)],
:::

so that

:::{math}
:label: eq-classemf-13
\kvec\cdot\tilde\Fvec_\perp(\kvec)=0, \qquad \kvec\cross\tilde\Fvec_\parallel(\kvec)=0.
:::

On transforming {eq}`eq-classemf-11` back to $\xvec$-space, we obtain the longitudinal and transverse components of $\Fvec$ in that space,

:::{math}
:label: eq-classemf-14
\Fvec(\xvec) = \Fvec_\perp(\xvec) + \Fvec_\parallel(\xvec),
:::

where $\Fvec_\perp$ and $\Fvec_\parallel$ are respectively the inverse Fourier transforms of $\tilde\Fvec_\perp$ and $\tilde\Fvec_\parallel$. But since the operator $\del$ in $\xvec$-space maps into multiplication by $i\kvec$ in $\kvec$-space, the relations {eq}`eq-classemf-13` are equivalent to

:::{math}
:label: eq-classemf-15
\del\cdot\Fvec_\perp(\xvec)=0, \qquad \del\cross\Fvec_\parallel(\xvec)=0.
:::

Thus, an arbitrary vector field $\Fvec(\xvec)$ can be decomposed in a part that is divergence-free ($\Fvec_\perp(\xvec)$) and a part that is curl-free ($\Fvec_\parallel(\xvec)$).

Notice that the gradient of a scalar is purely longitudinal, since $\del\cross \del f=0$, while the curl of a vector field is automatically transverse, since $\del \cdot \del \cross \Fvec=0$.

The process of projecting out the transverse and longitudinal parts of a vector field is a local operation in $\kvec$-space, but it is nonlocal in $\xvec$-space. That is, the value of $\Fvec_\perp$ at some point $\xvec$ depends on the values of $\Fvec$ at all other points of $\xvec$-space. The projection operator in $\xvec$-space is actually an integral transform,

:::{math}
:label: eq-classemf-16
F_{\perp i}(\xvec) = \sum_j \int d^3\xvec' \, \Delta^\perp_{ij}(\xvec-\xvec') F_j(\xvec'),
:::

where the kernel, $\Delta^\perp_{ij}$, is called the *transverse delta function*. Notice that it is really a tensor in the indices $i,j$. We will now derive two useful expressions for the transverse delta function.

One way to project out the transverse part of $\Fvec$ is first to transform $\Fvec$ over to $\kvec$-space, then to project out the transverse part in $\kvec$-space, then to transform back to $\xvec$-space. If we do this, we find

:::{math}
:label: eq-classemf-17
\Fvec_\perp(\xvec) = \int {d^3\kvec \over (2\pi)^{3/2}} \, e^{i\kvec\cdot\xvec} \Bigl(\Imat - {\kvec\kvec \over k^2}\Bigr) \int {d^3\xvec' \over (2\pi)^{3/2}} e^{-i\kvec\cdot\xvec'} \Fvec(\xvec'),
:::

where $\Imat$ is the identity tensor and where we use dyadic notation in the term $\kvec\kvec/k^2={\hat{\mathbf{k}}}{\hat{\mathbf{k}}}$. Comparing this to {eq}`eq-classemf-16`, we can easily read off the transverse delta function, which is

:::{math}
:label: eq-classemf-18
\Delta^\perp_{ij}(\xvec-\xvec') = \int {d^3\kvec \over (2\pi)^3} e^{i\kvec\cdot(\xvec-\xvec')} \Bigl( \delta_{ij} - {k_ik_j\over k^2} \Bigr).
:::

The transverse delta function is just the Fourier transform of the transverse projection operator in $\kvec$-space, evaluated at the vector difference $\xvec-\xvec'$.

A second expression for the transverse delta function is obtained by working directly in $\xvec$-space. In the decomposition {eq}`eq-classemf-14`, we note that since $\Fvec_\parallel$ is curl-free, it can be represented as the gradient of a scalar, say,

:::{math}
:label: eq-classemf-19
\Fvec_\parallel = \del f.
:::

We can solve for $f$ by taking the divergence of {eq}`eq-classemf-14`, and noting $\del\cdot\Fvec_\perp=0$. Thus, we have

:::{math}
:label: eq-classemf-20
\del^2 f = \del\cdot\Fvec.
:::

We solve this by inverting the Laplacian, to find

:::{math}
:label: eq-classemf-21
f(\xvec) = -{1\over 4\pi} \int d^3\xvec'\, {\del'\cdot\Fvec(\xvec') \over |\xvec-\xvec'|} = {1\over 4\pi} \int d^3\xvec' \, \del'\Bigl( {1\over |\xvec-\xvec'|} \Bigr) \cdot \Fvec(\xvec'),
:::

where we are careful to write $\del'$ for derivatives with respect to $\xvec'$, and where we have integrated by parts and thrown away boundary terms to get the second integral. We note that in the second integral, we could replace $\del'$ by $-\del$, since it acts only on a function of $\xvec-\xvec'$. Finally, by using {eq}`eq-classemf-19` to obtain the longitudinal part of $\Fvec$ and subtracting this from $\Fvec$ itself, we obtain the transverse part. We find

:::{math}
:label: eq-classemf-22
\Fvec_\perp(\xvec) = \Fvec(\xvec) +{1\over 4\pi} \del \int d^3\xvec' \, \del\Bigl( {1\over |\xvec-\xvec'|} \Bigr) \cdot \Fvec(\xvec'),
:::

which by comparison with {eq}`eq-classemf-16` gives

:::{math}
:label: eq-classemf-23
\Delta^\perp_{ij}(\xvec-\xvec') = \delta(\xvec-\xvec') \delta_{ij} +{1\over 4\pi} \del_i \del_j \Bigl( {1\over |\xvec-\xvec'|} \Bigr).
:::

This can be cast into somewhat more symmetrical form by reexpressing the first term:

:::{math}
:label: eq-classemf-24
\Delta^\perp_{ij}(\xvec-\xvec') = -{1\over 4\pi} \Bigl( \delta_{ij} \del^2 - {\partial^2 \over \partial x_i \partial x_j} \Bigr) \Bigl( {1\over |\xvec-\xvec'|}\Bigr).
:::

We note one final identity involving transverse and longitudinal vector fields. It is not in general true that the transverse and longitudinal parts of a vector field in ordinary space are perpendicular at a given point, that is, $\Fvec_\perp(\xvec) \cdot \Gvec_\parallel(\xvec)$ does not in general vanish. This is because the projection process is nonlocal in $\xvec$-space. On the other hand, we obviously have $\tilde\Fvec_\perp \cdot \tilde \Gvec_\parallel =0$ at each point of $\kvec$-space. Therefore by the Parseval identity {eq}`eq-classemf-10`, we do find an orthogonality of sorts in $\xvec$-space, namely

:::{math}
:label: eq-classemf-25
\int d^3\xvec \, \Fvec_\perp(\xvec)\cdot \Gvec_\parallel(\xvec)=0.
:::

In all these operations involving transverse and longitudinal vector fields, we have assumed that the fields in question are sufficiently well behaved to legitimize the various steps. In particular, we assume that all fields fall off rapidly enough at infinity to allow the neglect of boundary terms in the integrations by parts.

(sec-classemf-8)=

## Field Equations in Coulomb Gauge

In Coulomb gauge, the vector potential is purely transverse, $\Avec=\Avec_\perp$. We shall generally omit the $\perp$ on $\Avec$. Notice that the gauge transformation {eq}`eq-classemf-5b` changes only the longitudinal part of $\Avec$, since $\del\chi$ is purely longitudinal. Thus we can say that the nonphysical part of $\Avec$ is the longitudinal part, while the physical part is the transverse part. Coulomb gauge consists of setting the nonphysical part to zero, in a certain sense.

The Coulomb gauge condition simplifies the equations of motion {eq}`eq-classemf-6a`, which become

:::{math}
:label: eq-classemf-26a
\begin{aligned}
\del^2\Phi &= -4\pi\rho,
\end{aligned}
:::

:::{math}
:label: eq-classemf-26b
\begin{aligned}
\del^2 \Avec - {1\over c^2} {\partial^2 \Avec \over \partial t^2} &= -{4\pi\over c}\Jvec +\del\Bigl( {1\over c}\frac{\partial \Phi}{\partial t}\Bigr).
\end{aligned}
:::

Now the equation for the scalar potential is just the Poisson equation, which we can solve by standard methods from electrostatics (using the Green's function for the Laplacian operator). This gives

:::{math}
:label: eq-classemf-27
\Phi(\xvec,t) = \int d^3\xvec' \, {\rho(\xvec',t) \over |\xvec-\xvec'|}.
:::

This is almost a familiar formula from electrostatics, but not quite. The point is that we are not doing electrostatics, rather we are interested in fully time-dependent electromagnetic phenomena, as indicated by the time dependence in $\Phi(\xvec,t)$ and $\rho(\xvec,t)$. Notice that according to {eq}`eq-classemf-27`, $\Phi$ at one spatial point at a given time is computed in terms of the charge density at all other spatial points *at the same time*. There is no retardation in this formula. This would be fine in electrostatics, where the charges are not moving, but in our applications the charges are moving, in general. Thus it appears that relativistic causality (the principle that signals cannot travel faster than the speed of light) is violated in the Coulomb gauge, at least insofar as the scalar potential $\Phi$ is concerned.

Actually there is no problem from a physical standpoint, since one cannot measure $\Phi$. What one measures is $\Evec$, which is given in terms of $\Phi$ and $\Avec$ by {eq}`eq-classemf-4a`. Notice that if we use Coulomb gauge in that equation, then the two terms given are precisely the longitudinal and transverse parts of the electric field, that is,

:::{math}
:label: eq-classemf-28
\Evec_\parallel = -\del\Phi, \qquad \Evec_\perp = -{1\over c}\frac{\partial \Avec}{\partial t}.
:::

Although $\Evec_\parallel$ is non-retarded, it turns out that $\Evec_\perp$ contains both a retarded and non-retarded part, and that the non-retarded parts cancel each other when the total electric field $\Evec$ is computed. There is no violation of relativistic causality in Coulomb gauge.

On the other hand, if the system has limited spatial extent and consists of low velocity particles, then the charge density $\rho$ at the field time $t$ is approximately equal to the charge density at the retarded time, and the effects of retardation are small. In fact, the usual electrostatic model, which we have used almost exclusively in this course up to this time, is equivalent to determining $\Phi$ by {eq}`eq-classemf-27` and neglecting $\Evec_\perp$.

(sec-classemf-9)=

## Periodic Boundary Conditions

A field system such as the electromagnetic field has an infinite number of degrees of freedom, in fact, a continuous infinity if the field can take on independent values everywhere in space. To reduce the degrees of freedom to a discrete (but still infinite) set, it is convenient to introduce periodic boundary conditions. This is exactly what we did earlier with scattering theory in {ref}`ch-tdpt`. We imagine that the universe is divided up into cubical boxes of volume $V=L^3$ with sides of length $L$, and that all the physics, both fields and matter, are periodic in the boxes. This simplifies many calculations, and physical results may be obtained in the end by taking $V\to\infty$. With periodic boundary conditions, all fields can be represented in terms of Fourier series instead of Fourier integrals.

Our conventions for these Fourier series are the following. Let $S(\xvec)$ be a generic scalar field satisfying periodic boundary conditions. Then we can expand $S$ as

:::{math}
:label: eq-classemf-29
S(\xvec) = {1\over\sqrt{V}} \sum_\kvec S_\kvec \, e^{i\kvec\cdot\xvec},
:::

where the factor of $1/\sqrt{V}$ is conventional. We omit the tilde on the Fourier coefficients $S_\kvec$, since the subscript indicates which space is referred to. The sum is taken over a discrete set of values of $\kvec$,

:::{math}
:label: eq-classemf-30
\kvec={2\pi \over L} \nvec,
:::

where $\nvec=(n_x,n_y,n_z)$ is a vector of integers, each of which ranges from $-\infty$ to $+\infty$. We visualize this as a lattice of points in $\kvec$-space. The density of points in $\kvec$-space with respect to the measure $d^3\kvec$ is $V/(2\pi)^3$, which goes to infinity as $V\to\infty$, with the result that $\kvec$ takes on continuous values in this limit. The Fourier coefficients $S_\kvec$ in {eq}`eq-classemf-29` are given in terms of the original function $S(\xvec)$ by

:::{math}
:label: eq-classemf-31
S_\kvec = {1\over\sqrt{V}} \int_V d^3\xvec\, e^{-i\kvec\cdot\xvec} S(\xvec),
:::

where the integral is taken over the volume of the box. The coefficients $S_\kvec$ are in general complex, but if $S(\xvec)$ is real, then they satisfy

:::{math}
:label: eq-classemf-32
S_\kvec = S^\cc_{-\kvec}.
:::

Similarly, for a vector field $\Fvec(\xvec)$ the Fourier coefficients are defined by

:::{math}
:label: eq-classemf-33
\Fvec_\kvec={1\over\sqrt{V}} \int_V d^3\xvec\, e^{-i\kvec\cdot\xvec}\, \Fvec(\xvec).
:::

As for the Parseval identity, we will mostly use it with vector fields. Let $\Fvec(\xvec)$ and $\Gvec(\xvec)$ be two real vector fields with Fourier coefficients $\Fvec_\kvec$ and $\Gvec_\kvec$. Then we have

:::{math}
:label: eq-classemf-34
\int_V d^3\xvec\, \Fvec(\xvec)\cdot\Gvec(\xvec)= \sum_\kvec \Fvec^\cc_{\kvec} \cdot \Gvec_\kvec.
:::

Finally, when we let $V\to\infty$ and go over to the continuous case, we make the transcriptions,

:::{math}
:label: eq-classemf-35
\sum_\kvec \to {V\over (2\pi)^3} \int d^3\kvec,
:::

:::{math}
:label: eq-classemf-36
\Fvec_\kvec \to {(2\pi)^{3/2} \over \sqrt{V}} \tilde\Fvec(\kvec),
:::

and

:::{math}
:label: eq-classemf-37
\delta_{\kvec,\kvec'} \to {(2\pi)^3\over V} \delta(\kvec-\kvec').
:::

This makes the results conform with the conventions for Fourier transforms presented in \secrclassemf-7.

(sec-classemf-10)=

## Free Field Case.  Plane Wave Solutions

We will find the Hamiltonian for the classical electromagnetic field first in the case of the free field, and generalize later to the case of the field interacting with matter. The free field means $\rho=0$ and $\Jvec=0$, that is, we imagine a universe with only electromagnetic fields and no matter.

In this case {eq}`eq-classemf-26a` implies $\Phi=0$, and {eq}`eq-classemf-26b` simplifies to

:::{math}
:label: eq-classemf-38
\del^2 \Avec - {1\over c^2} {\partial^2 \Avec \over \partial t^2}=0,
:::

that is, $\Avec$ satisfies the wave equation. The free field consists purely of light waves, propagating through space. The electric and magnetic fields are now given by

:::{math}
:label: eq-classemf-39
\Evec=-{1\over c} \frac{\partial \Avec}{\partial t}, \qquad \Bvec = \del\cross\Avec.
:::

Both $\Evec$ and $\Bvec$ are purely transverse.

One solution of the wave equation {eq}`eq-classemf-38` is a plane light wave of wave vector $\kvec$ and frequency $\omega$, whose vector potential is

:::{math}
:label: eq-classemf-40
\Avec(\xvec,t) = {1\over\sqrt{V}} \Cvec_0 \,e^{i(\kvec\cdot\xvec - \omega t)} +\\textc.c.
:::

Here $\Cvec_0$ is a constant amplitude vector and we have split off a factor of $1/\sqrt{V}$ for later convenience. Because of the periodic boundary conditions, $\kvec$ lies on one of the lattice points in $\kvec$-space. In order to satisfy the wave equation {eq}`eq-classemf-38`, $\kvec$ and $\omega$ must satisfy

:::{math}
:label: eq-classemf-41
\omega = \omega_\kvec =c|\kvec| = ck,
:::

the usual dispersion relation for light waves. We will usually omit the $\kvec$ subscript on $\omega$ when referring to light waves, it being understood that $\omega$ and $\kvec$ are related by {eq}`eq-classemf-41`. The complex conjugate is added on the right-hand side of {eq}`eq-classemf-40` because the vector potential $\Avec$ is real. The amplitude vector $\Cvec_0$ in {eq}`eq-classemf-40` must be allowed to be complex, however, in order to accommodate all possible solutions of the wave equation with a given wave vector $\kvec$. For example, if we want the $y$-component of $\Avec$ to be $90^\circ$ out of phase with the $x$-component, we can take $C_{0x}=1$ and $C_{0y}=i$ (in some units). Both the real and imaginary parts of the components of $\Cvec_0$ are physically meaningful. Also, because of the Coulomb gauge condition {eq}`eq-classemf-7`, the amplitude vector must be transverse,

:::{math}
:label: eq-classemf-42
\kvec\cdot\Cvec_0 = 0,
:::

that is, $\Cvec_0$ must lie in the plane perpendicular to $\kvec$.

The plane wave {eq}`eq-classemf-40` is just a particular solution of the wave equation, but the general solution is an arbitrary linear combination of waves of this form,

:::{math}
:label: eq-classemf-43
\Avec(\xvec,t)= {1\over\sqrt{V}} \sum_\kvec \Cvec_{0\kvec} \, e^{i(\kvec\cdot\xvec - \omega t)} + c.c.,
:::

where now we attach a $\kvec$-subscript to $\Cvec_{0\kvec}$ to indicate an arbitrary, transverse, complex amplitude vector assigned to each lattice point in $\kvec$-space.

Next, we change the notation slightly by absorbing the time-dependence into the amplitude vector, defining

:::{math}
:label: eq-classemf-44
\Cvec_\kvec(t) = \Cvec_{0\kvec}\, e^{-i\omega t},
:::

so that

:::{math}
:label: eq-classemf-45
{\dot\Cvec}_\kvec +i\omega \Cvec_\kvec = 0.
:::

Then the vector potential and its time derivative can be written as Fourier series,

:::{math}
:label: eq-classemf-46a
\begin{aligned}
\Avec(\xvec) & = {1\over\sqrt{V}} \sum_\kvec \bigl( \Cvec_\kvec \, e^{i\kvec\cdot\xvec} + \Cvec_\kvec^\cc \, e^{-i\kvec\cdot\xvec} \bigr),
\end{aligned}
:::

:::{math}
:label: eq-classemf-46b
\begin{aligned}
\frac{\partial \Avec(\xvec)}{\partial t} &= {1\over\sqrt{V}} \sum_\kvec \bigl( -i\omega \Cvec_\kvec \, e^{i\kvec\cdot\xvec} +i\omega \Cvec_\kvec^\cc \, e^{-i\kvec\cdot\xvec} \bigr),
\end{aligned}
:::

where it is understood that $\Avec$, $\partial \Avec/\partial t$, and $\Cvec_\kvec$ all depend on time.

Equations~{eq}`eq-classemf-46a` show that if the amplitude vectors $\Cvec_\kvec$ are given at some time, then the fields $\Avec$ and $\partial\Avec/\partial t$ can be computed at the same time. The converse is also true: Given $\Avec$ and $\partial\Avec /\partial t$ at some time, we can compute the amplitude vectors $\Cvec_\kvec$ at the same time.

To see this we note first that because of the terms going as $e^{-i\kvec\cdot\xvec}$, the series {eq}`eq-classemf-46a` are not Fourier series of the type modeled in {eq}`eq-classemf-33`. We can bring them into that form, however, by changing the dummy index of summation $\kvec$ in the second term to $-\kvec$. Notice that when we do this, $\omega$ does not change, since $\omega_\kvec = \omega_{-\kvec}$. Thus we obtain,

:::{math}
:label: eq-classemf-47a
\begin{aligned}
\Avec(\xvec) &= {1\over\sqrt{V}} \sum_\kvec \Avec_\kvec \, e^{i\kvec\cdot\xvec} = {1\over\sqrt{V}} \sum_\kvec (\Cvec_\kvec + \Cvec_{-\kvec}^\cc) e^{i\kvec\cdot\xvec},
\end{aligned}
:::

:::{math}
:label: eq-classemf-47b
\begin{aligned}
\frac{\partial \Avec(\xvec)}{\partial t} &= {1\over\sqrt{V}} \sum_\kvec {\dot\Avec}_\kvec \, e^{i\kvec\cdot\xvec} = {1\over\sqrt{V}} \sum_\kvec (-i\omega \Cvec_{\kvec} + i\omega \Cvec_{-\kvec}^\cc) e^{i\kvec\cdot\xvec},
\end{aligned}
:::

which defines $\Avec_\kvec$ and ${\dot\Avec}_\kvec$ as the Fourier coefficients of fields $\Avec$ and $\partial\Avec/\partial t$, as in {eq}`eq-classemf-33`, and allows us to solve for them in terms of the amplitude vectors $\Cvec_\kvec$,

:::{math}
:label: eq-classemf-48
\begin{aligned}
\Avec_\kvec & = \Cvec_\kvec + \Cvec^\cc_{-\kvec}, \\
\dot\Avec_\kvec & = -i\omega(\Cvec_\kvec - \Cvec^\cc_{-\kvec}).
\end{aligned}
:::

Solving these, we find

:::{math}
:label: eq-classemf-49a
\begin{aligned}
\Cvec_\kvec &= {1\over2} \Bigl( \Avec_\kvec + {i\over\omega} \dot\Avec_\kvec\Bigr),
\end{aligned}
:::

:::{math}
:label: eq-classemf-49b
\begin{aligned}
\Cvec^\cc_{-\kvec} &= {1\over 2} \Bigl( \Avec_\kvec - {i\over\omega} \dot\Avec_\kvec\Bigr).
\end{aligned}
:::

{eq}`eq-classemf-49b` is equivalent to {eq}`eq-classemf-49a`, as we see by taking the complex conjugate of both sides, replacing $\kvec$ by $-\kvec$, and using the reality condition {eq}`eq-classemf-32`. Thus, given $\Avec$ and $\partial \Avec/\partial t$ at some instant in time, we can compute the Fourier coefficients $\Avec_\kvec$ and ${\dot\Avec}_\kvec$ by {eq}`eq-classemf-33`, then find the complex amplitude vectors $\Cvec_\kvec$ by {eq}`eq-classemf-49a`.

We see that {eq}`eq-classemf-49a` (or just {eq}`eq-classemf-49a` can be regarded as the inverse of {eq}`eq-classemf-47a`. In effect, we have a coordinate transformation,

:::{math}
:label: eq-classemf-50
\Bigl(\Avec,\frac{\partial \Avec}{\partial t}\Bigr) \longleftrightarrow \{ \Cvec_\kvec\},
:::

taking us from the pair of fields $\Avec$, $\partial\Avec/\partial t$ to the set of amplitude vectors $\Cvec_\kvec$ or back again.

(sec-classemf-11)=

## Polarization Vectors

We now make a digression into the subject of polarization vectors. These are a pair of orthonormal unit vectors in the plane perpendicular to $\kvec$, in terms of which a transverse vector can be expanded. See {ref}`fig-classemf-1`.

:::{figure} images/classemf-fig01.png
:label: fig-classemf-1
:width: 80%

Polarization vectors and the transverse plane in $\kvec$-space.
:::

We denote the polarization vectors by $\epsilonvec_{\kvec\mu}$, where $\mu=1,2$ is the *polarization index* that labels the vectors. Polarization vectors must be allowed to be complex, in order to accommodate electromagnetic waves in which the phases of the different components differ. We choose them to be orthonormal in the sense of complex vectors, so they satisfy

:::{math}
:label: eq-classemf-51
\epsilonvec_{\kvec\mu} \cdot \epsilonvec_{\kvec\mu'}^\cc = \delta_{\mu\mu'}.
:::

They also satisfy

:::{math}
:label: eq-classemf-52
\kvec\cdot\epsilonvec_{\kvec\mu} =0,
:::

since they are transverse. Beyond these conditions, the polarization vectors are arbitrary, and, in particular, there is no necessary relation between polarization vectors for one $\kvec$ value and another (in any case, the transverse planes are different for different values of $\kvec$).

Taken with ${\hat{\mathbf{k}}}$, the two polarization vectors form an orthonormal triad with a completeness relation (resolution of the identity) given by

:::{math}
:label: eq-classemf-53
\sum_{\mu=1}^2 \epsilonvec_{\kvec\mu} \epsilonvec_{\kvec\mu}^\cc + {\hat{\mathbf{k}}} {\hat{\mathbf{k}}} =\Imat,
:::

so that an arbitrary vector $\Xvec$ can be expanded as

:::{math}
:label: eq-classemf-54
\Xvec = \sum_{\mu=1}^2 X_\mu \epsilonvec_{\kvec\mu} + X_k {\hat{\mathbf{k}}},
:::

where

:::{math}
:label: eq-classemf-55
X_\mu = \epsilonvec_{\kvec\mu}^\cc \cdot \Xvec, \qquad X_k = {\hat{\mathbf{k}}}\cdot\Xvec.
:::

It is always possible to choose real polarization vectors, since $\kvec$ is real. For example, if ${\hat{\mathbf{k}}}={\hat{\mathbf{z}}}$, then a pair of real polarization vectors is simply ${\hat{\mathbf{x}}}$ and ${\hat{\mathbf{y}}}$. Real polarization vectors correspond to linearly polarized light, that is, a light wave for which the electric field vector at a fixed point of space traces out a line segment (going back and forth over it in each cycle). Complex polarization vectors can always be expanded as linear combinations of real polarization vectors. The relative phase (in the sense of complex numbers) of the two components of a complex polarization vector with respect to a real basis indicates the relative phase shift between the two components of the electric field. If this phase shift is $\pm 90^\circ$, we have circularly polarized light, in which the electric field vector at a fixed point of space traces out a circle. Other phase shifts correspond to elliptically polarized light. The overall phase of a polarization vector is immaterial for determining the type of polarization; in this sense polarization vectors are like two-component spinors in quantum mechanics, for which the overall phase is nonphysical.

(sec-classemf-12)=

## The Mode Expansion

Since the amplitude vectors $\Cvec_\kvec$ are transverse, they can be expanded as a linear combination of the polarization vectors,

:::{math}
:label: eq-classemf-56
\Cvec_\kvec = \sum_{\mu=1}^2 C_{\kvec\mu} \, {\hat{\boldsymbol{\epsilon}}}_{\kvec\mu},
:::

so that {eq}`eq-classemf-46a` becomes

:::{math}
:label: eq-classemf-57
\Avec(\xvec) = {1\over\sqrt{V}} \sum_{\kvec\mu} \Bigl( C_{\kvec\mu} \, {\hat{\boldsymbol{\epsilon}}}_{\kvec\mu} \, e^{i\kvec\cdot\xvec} + C_{\kvec\mu}^\cc \, {\hat{\boldsymbol{\epsilon}}}_{\kvec\mu}^\cc \, e^{-i\kvec\cdot\xvec}\Bigr).
:::

We will regard this as a sum over the *modes* of the electromagnetic field, where each mode is specified by a value of $\kvec$ and a polarization index $\mu$. There are two modes for each lattice point in $\kvec$-space. We will often use the following abbreviation for the *mode index*,

:::{math}
:label: eq-classemf-58
\lambda=(\kvec,\mu),
:::

for example,

:::{math}
:label: eq-classemf-59
C_\lambda = {\hat{\boldsymbol{\epsilon}}}_\lambda^\cc \cdot \Cvec_\kvec.
:::

We call the $C_\lambda$ the *mode amplitudes*; they are complex numbers, one for each mode of the field. They satisfy the equations of motion

:::{math}
:label: eq-classemf-60
{\dot C}_\lambda + i\omega C_\lambda = 0,
:::

with the solution

:::{math}
:label: eq-classemf-61
C_\lambda(t) = C_{0\lambda} \, e^{-i\omega t}.
:::

Finally, the mode expansions of $\Avec$ and $\partial\Avec/\partial t$ are

:::{math}
:label: eq-classemf-62a
\begin{aligned}
\Avec(\xvec) &= {1\over\sqrt{V}} \sum_\lambda \Bigl( C_\lambda \, {\hat{\boldsymbol{\epsilon}}}_\lambda\, e^{i\kvec\cdot\xvec} + C_\lambda^\cc \, {\hat{\boldsymbol{\epsilon}}}_\lambda^\cc \, e^{-i\kvec\cdot\xvec}\Bigr),
\end{aligned}
:::

:::{math}
:label: eq-classemf-62b
\begin{aligned}
\frac{\partial \Avec(\xvec)}{\partial t} &= {1\over\sqrt{V}} \sum_\lambda \Bigl( -i\omega C_\lambda \, {\hat{\boldsymbol{\epsilon}}}_\lambda e^{i\kvec\cdot\xvec} +i\omega C_\lambda^\cc \, {\hat{\boldsymbol{\epsilon}}}_\lambda^\cc \, e^{-i\kvec\cdot\xvec}\Bigr).
\end{aligned}
:::

The transformation {eq}`eq-classemf-56` or its inverse {eq}`eq-classemf-59` can be seen as another coordinate transformation, on top of {eq}`eq-classemf-50`,

:::{math}
:label: eq-classemf-63
\{ \Cvec_\kvec \} \longleftrightarrow \{ C_\lambda \},
:::

a fairly trivial one, in fact, but it shows that knowledge of the mode amplitudes $C_\lambda$ allows one to compute $\Avec$ and $\partial\Avec/\partial t$ and vice versa.

(sec-classemf-13)=

## The Dynamical State of the Electromagnetic Field

In classical mechanics, the *dynamical state* of a system is the specification of enough information to determine the subsequent time evolution of that system. For example, in a mechanical system we can specify the positions and velocities (or momenta) of all the particles. In the case of the Schr\"odinger equation, the dynamical state is specified by the wave function at a given time, $\psi(\xvec,t_0)$, which constitutes a complete set of initial conditions since the Schr\"odinger equation is first order in time. The wave equation {eq}`eq-classemf-38`, on the other hand, is second order in time, so a specification of the dynamical state of the system (the free field in Coulomb gauge) requires both $\Avec$ and $\partial \Avec/\partial t$ at a given time.

However, the coordinate transformation {eq}`eq-classemf-50`, given explicitly by {eq}`eq-classemf-47a` and {eq}`eq-classemf-49a`, shows that the dynamical state of the electromagnetic field is equally well specified by the set of amplitude vectors $\{ \Cvec_\kvec\}$. Or, with the subsequent coordinate transformation {eq}`eq-classemf-63`, it is specified by the set of mode amplitudes $\{ C_\lambda \}$, one complex number for each mode of the field. These transformations can be regarded as coordinate transformations on the state space or *phase space* of the electromagnetic field. See {ref}`sec-classmech-18` for this terminology in classical mechanics.

Although the transformation {eq}`eq-classemf-50` was motivated by the plane wave solutions for the free field, you may notice that the transformation itself does not involve any equations of motion. It simply gives two alternative descriptions of the state of the field. It is true that for the free field in the description $(\Avec,\partial\Avec/\partial t)$ the equations of motion are the wave equation {eq}`eq-classemf-38`, while in the description $\Cvec_\kvec$ or $C_\lambda$ the equations of motion are {eq}`eq-classemf-45` or {eq}`eq-classemf-60`. But these coordinate transformations can be used regardless of the equations of motion. Indeed, below we shall use these transformations in the case of the interacting field, for which the equations of motion are different from {eq}`eq-classemf-38` or {eq}`eq-classemf-45` or {eq}`eq-classemf-60`.

(sec-classemf-14)=

## A Guess for the Canonical Coordinates

We return to our goal of finding a classical Hamiltonian description of the electromagnetic field, working for the moment with the case of the free field. To do this we require both a Hamiltonian and a proper definition of canonical coordinates, that is, a set of $q$ and $p$ coordinates in terms of which Hamilton's classical equations of motion are equivalent to Maxwell's equations. In this we guess the canonical coordinates.

:::{figure} images/classemf-fig02.png
:label: fig-classemf-2
:width: 80%

Evolution of mode amplitude $C_\lambda$ in the complex plane.
:::

For the free field, the mode amplitudes have the evolution given by {eq}`eq-classemf-61`. When viewed in the complex plane, the motion is circular in the clockwise direction, with frequency $\omega$ (the frequency of the light wave of the given mode). See {ref}`fig-classemf-2`. This reminds us of the motion of a classical harmonic oscillator in the $q$-$p$ phase plane (see Fig.~\figr\harmosc.1). This suggests that each mode of the free electromagnetic field can be described as a harmonic oscillator, and that the $q$ and the $p$ of the oscillator are proportional to the real and imaginary parts of $C_\lambda$, respectively.

To be more precise, the Hamiltonian for a mechanical harmonic oscillator is

:::{math}
:label: eq-classemf-64
H={p^2 \over 2m} + {m\omega^2 q^2 \over 2},
:::

whose orbit in phase space is an ellipse. But if we introduce the change of coordinates,

:::{math}
:label: eq-classemf-65
p=\sqrt{m\omega}\,p', \qquad q={q' \over \sqrt{m\omega}},
:::

and then drop the primes, then in the new coordinates the Hamiltonian is more symmetrical between $p$ and $q$,

:::{math}
:label: eq-classemf-66
H = {\omega\over 2}(p^2 + q^2),
:::

and the orbit in phase space is indeed now a circle. The motion is clockwise with frequency $\omega$, just like the mode amplitude $C_\lambda$. The transformation {eq}`eq-classemf-65` is an example of a canonical transformation in classical mechanics, in which phase space area is preserved (since the transformation squeezes in one direction and stretches in the other).

Now we introduce canonical coordinates $(Q_\lambda,P_\lambda)$ for mode $\lambda$ by writing,

:::{math}
:label: eq-classemf-67
C_\lambda = \\textconst.\times (Q_\lambda + iP_\lambda),
:::

where the constant is to be determined.

(sec-classemf-15)=

## A Guess for the Free-Field Hamiltonian

In mechanical systems the Hamiltonian is the energy of the system, so we guess that the field Hamiltonian will be the energy of the field. That energy is

:::{math}
:label: eq-classemf-68
H= {1\over 8\pi} \int_V d^3\xvec \, (E^2 + B^2),
:::

which we denote by $H$ in anticipation that this will prove to be the Hamiltonian. Since we are using periodic boundary conditions, we integrate only over the volume $V$ of the box.

To express $H$ in terms of the mode amplitudes, we write out Fourier series for $\Evec=-(1/c)\partial \Avec/\partial t$ and $\Bvec=\del\cross \Avec$, using {eq}`eq-classemf-62b` for $\Evec$ and differentiating {eq}`eq-classemf-62a` for $\Bvec$. This gives

:::{math}
:label: eq-classemf-69
\begin{aligned}
\Evec(\xvec,t) &= {1\over\sqrt{V}} \sum_\lambda \Bigl[ {i\omega\over c} C_\lambda \epsilonvec_\lambda \, e^{i\kvec\cdot\xvec} + c.c.\Bigr],
\end{aligned}
:::

:::{math}
:label: eq-classemf-70
\begin{aligned}
\Bvec(\xvec,t) &= {1\over\sqrt{V}} \sum_\lambda \Bigl[ i C_\lambda (\kvec\cross\epsilonvec_\lambda) \, e^{i\kvec\cdot\xvec} + c.c. \Bigr].
\end{aligned}
:::

Let us look first at the integral of $E^2$ in the Hamiltonian {eq}`eq-classemf-68`. This is

:::{math}
\begin{aligned}
\\text{E^2}-term= {1\over 8\pi} \int_V d^3\xvec \, {1\over V} \sum_{\lambda\lambda'} & \Bigl[ {i\omega\over c} C_\lambda \epsilonvec_\lambda \, e^{i\kvec\cdot\xvec} -{i\omega\over c} C^\cc_\lambda \epsilonvec^\cc_\lambda \, e^{-i\kvec\cdot\xvec}\Bigr]
\end{aligned}
:::

:::{math}
:label: eq-classemf-71
\begin{aligned}
& \quad \cdot \Bigl[ {i\omega'\over c} C_{\lambda'} \epsilonvec_{\lambda'} \, e^{i\kvec'\cdot\xvec} -{i\omega'\over c} C^\cc_{\lambda'} \epsilonvec^\cc_{\lambda'} \, e^{-i\kvec'\cdot\xvec} \Bigr].
\end{aligned}
:::

There are four major terms in this integral; let us look at one of the cross terms, namely,

:::{math}
\begin{aligned}
\\text{C_\lambda C^\cc_{\lambda'}-term} & = {1\over 8\pi} \int_V d^3\xvec \, {1\over V} \sum_{\lambda\lambda'} {\omega\omega'\over c^2} C_\lambda C^\cc_{\lambda'} (\epsilonvec_\lambda \cdot \epsilonvec^\cc_{\lambda'}) \, e^{i(\kvec-\kvec')\cdot\xvec}
\end{aligned}
:::

:::{math}
\begin{aligned}
& ={1\over 8\pi} \sum_{\lambda\lambda'} {\omega\omega'\over c^2} C_\lambda C^\cc_{\lambda'} (\epsilonvec_\lambda \cdot \epsilonvec^\cc_{\lambda'}) \, \delta_{\kvec,\kvec'} ={1\over 8\pi} \sum_{\kvec\mu\mu'} {\omega^2\over c^2} C_{\kvec\mu} C^\cc_{\kvec\mu'} (\epsilonvec_{\kvec\mu} \cdot \epsilonvec^\cc_{\kvec\mu'})
\end{aligned}
:::

:::{math}
:label: eq-classemf-72
\begin{aligned}
&= {1\over 8\pi} \sum_{\kvec\mu} {\omega^2 \over c^2} |C_{\kvec\mu}|^2 = {1\over 8\pi} \sum_\lambda {\omega^2\over c^2} |C_\lambda|^2,
\end{aligned}
:::

where we have carried out the spatial integration in the second equality, written $\lambda=(\kvec,\mu)$ and $\lambda'=(\kvec',\mu')$ and done the $\kvec'$-sum in the third equality, and then used {eq}`eq-classemf-51` in the fourth equality. Thus we have evaluated one of the cross terms. By a similar calculation, we find that the other cross term in $E^2$ integral, as well as the two cross terms in the $B^2$ integral, all give the same answer as {eq}`eq-classemf-72`. As for the other terms (the $C_\lambda C_{\lambda'}$-terms and the $C^\cc_\lambda C^\cc_{\lambda'}$-terms), we find that these cancel when the electric and magnetic contributions are combined. Altogether, the Hamiltonian becomes

:::{math}
:label: eq-classemf-73
H= {1\over 2\pi} \sum_\lambda {\omega^2\over c^2} |C_\lambda|^2.
:::

This tells us how to choose the constant in {eq}`eq-classemf-67` to make the Hamiltonian come out as a sum of harmonic oscillators in the symmetrical form {eq}`eq-classemf-66`, one for each mode of the field. That is, we write

:::{math}
:label: eq-classemf-74
C_\lambda = \sqrt{{\pi c^2 \over \omega}} (Q_\lambda + iP_\lambda),
:::

which defines $Q_\lambda$ and $P_\lambda$ in terms of $C_\lambda$. Then The Hamiltonian becomes

:::{math}
:label: eq-classemf-75
H= \sum_\lambda {\omega_\lambda\over 2} (Q_\lambda^2 +P^2_\lambda).
:::

Here we have written $\omega_\lambda$ instead of $\omega$ to emphasize that $\omega$ depends on $\kvec$ (so $\omega$ cannot be taken out of the sum). The field Hamiltonian is a sum of harmonic oscillators, one for each mode of the field.

Since there have been several guesses in the derivation of this Hamiltonian, we should now check to see that it really does give the correct equations of motion. But this is relatively easy. We have

:::{math}
:label: eq-classemf-76
\dot Q_\lambda = \frac{\partial H}{\partial P_\lambda} = \omega P_\lambda, \qquad \dot P_\lambda = -\frac{\partial H}{\partial Q_\lambda} = -\omega Q_\lambda,
:::

which imply ${\dot C}_\lambda = -i\omega_\lambda C_\lambda$, which when used in the coordinate transformation {eq}`eq-classemf-63` implies ${\dot\Cvec}_\kvec + i\omega\Cvec_\kvec=0$, which when used in the coordinate transformation {eq}`eq-classemf-50`, or, explicitly, {eq}`eq-classemf-47a`, implies that $\Avec$ satisfies the wave equation {eq}`eq-classemf-38`, which for the free field in Coulomb gauge implies Maxwell's equations.

In classical mechanics, the number of independent $q$'s, or the number of $(q,p)$ pairs in the Hamiltonian, is called the number of *degrees of freedom*. We see that the electromagnetic field has one degree of freedom for each mode of the field (two per $\kvec$ value). The total number of degrees of freedom is infinite.

(sec-classemf-16)=

## The Field Interacting with Matter

We turn now to the case of the electromagnetic field interacting with matter. For this we must adopt some model of the matter. We will assume we have $n$ particles, with mass $m_\alpha$, charge $q_\alpha$, position $\rvec_\alpha$ and velocity $\vvec_\alpha$, $\alpha=1, \ldots, n$. We will use indices $\alpha$, $\beta$, etc., to label the particles. The particles produce charge and current densities given by

:::{math}
:label: eq-classemf-77
\begin{aligned}
\rho(\xvec,t) &= \sum_\alpha q_\alpha \, \delta\bigl(\xvec-\rvec_\alpha(t)\bigr),
\end{aligned}
:::

:::{math}
:label: eq-classemf-78
\begin{aligned}
\Jvec(\xvec,t) &= \sum_\alpha q_\alpha \dot \rvec_\alpha \, \delta\bigl(\xvec-\rvec_\alpha(t)\bigr).
\end{aligned}
:::

Notice that $\xvec$ is the field point, that is, the point of space where the charge or current density is measured, while $\rvec_\alpha$ is the position of the particle. We will henceforth maintain this notational distinction between field points ($\xvec$) and particle positions ($\rvec_\alpha$). Notice that $\rho(\xvec,t)$ acquires its time dependence because the particle positions $\rvec_\alpha$ depend on time; $\Jvec$ depends on time additionally through the particle velocity $\vvec_\alpha$. These charge and current densities satisfy the continuity equation {eq}`eq-classemf-3`.

For the interacting field the equations of motion for the potentials in Coulomb gauge are {eq}`eq-classemf-26a`. As noted in \secrclassemf-8, the scalar potential $\Phi$ satisfies a non-retarded Poisson equation, with solution in terms of $\rho$ given by {eq}`eq-classemf-27`. With {eq}`eq-classemf-77` for the charge density, the integral can be done, giving

:::{math}
:label: eq-classemf-79
\Phi(\xvec,t) = \sum_\alpha {q_\alpha \over |\xvec - \rvec_\alpha(t)|}.
:::

This is a familiar formula from electrostatics, applied here, however, to electrodynamics, without retardation.

{eq}`eq-classemf-27` or {eq}`eq-classemf-79` shows that the scalar potential $\Phi$ in Coulomb gauge is a function of the particle coordinates, that is, it is not an independent dynamical variable. If it were, it would satisfy some equations of evolution, and it would be necessary to specify initial conditions for $\Phi$ to determine the values of $\Phi$ at a later time. Instead, $\Phi$ becomes completely known once the particle positions are known. This is in contrast to the transverse components of the vector potential, which are true dynamical degrees of freedom of the field, and which, as we have seen in the case of the free field, are associated with a set of independent $p$'s and $q$'s.

Another way to express $\Phi$ in terms of the matter degrees of freedom is to Fourier transform the Poisson equation, {eq}`eq-classemf-26a`, which gives $-k^2 \Phi_\kvec = -4\pi\rho_\kvec$, or

:::{math}
:label: eq-classemf-80
\Phi_\kvec = {4\pi \over k^2} \rho_\kvec.
:::

We will assume the total charge in the box is zero, so $\rho_\kvec=0$ at $\kvec=0$ and there is no problem with $\kvec=0$ in {eq}`eq-classemf-80`.

Of the four components of the 4-vector potential $A^\mu=(\Phi,\Avec)$, one ($\Phi$) is a function of the matter degrees of freedom, one (the longitudinal component of $\Avec$) vanishes, and two (the transverse components of $\Avec$) are true dynamical variables of the field. This is how it works in Coulomb gauge. In other gauges the results are similar; the electromagnetic field has only two true degrees of freedom for each value of $\kvec$.

The equation of motion for $\Avec$ interacting with matter is {eq}`eq-classemf-26b`. Since the left-hand side of this equation is purely transverse, the right-hand side must be purely transverse also. But the term $\del(\partial \Phi/\partial t)$ is purely longitudinal, so we suspect this must cancel out the longitudinal part of the current $\Jvec$. To check that this is true, we transform {eq}`eq-classemf-26b` to $\kvec$-space, obtaining

:::{math}
:label: eq-classemf-81
-k^2 \Avec_\kvec - {1\over c^2} {\ddot\Avec}_\kvec = -{4\pi\over c} \Jvec_\kvec + {i\kvec \over c} {\dot\Phi}_\kvec,
:::

and dot with ${\hat{\mathbf{k}}}$ to obtain

:::{math}
:label: eq-classemf-82
0 = -{4\pi\over c} J_{\parallel\kvec} + {ik\over c} {\dot\Phi}_\kvec.
:::

The longitudinal component of the current $J_{\parallel\kvec}$ can be expressed in terms of the charge density $\rho$ by Fourier transforming the continuity equation {eq}`eq-classemf-3`,

:::{math}
:label: eq-classemf-83
{\dot\rho}_\kvec +i\kvec\cdot\Jvec_\kvec=0,
:::

or ${\dot\rho}_\kvec = -ik J_{\parallel\kvec}$. The continuity equation constrains the longitudinal component of the current, but imposes no constraints on the transverse part. Also, from {eq}`eq-classemf-80` we have ${\dot\Phi_\kvec} = (4\pi/k^2){\dot\rho}_\kvec$. When these are used in {eq}`eq-classemf-82`, the two terms on the right-hand side cancel, verifying our suspicions.

Thus, the continuity equation and the Poisson equation imply that the right-hand side of {eq}`eq-classemf-26b` is purely transverse, and we can write

:::{math}
:label: eq-classemf-84
\del^2 \Avec - {1\over c^2} {\partial^2 \Avec \over \partial t^2} = -{4\pi\over c}\Jvec_\perp.
:::

In Coulomb gauge, the vector potential, which is purely transverse, is driven by the transverse components of the current. Since $\Avec$ was described by harmonic oscillators in the case of the free field, we suspect that it will be described by driven harmonic oscillators in the case of the interacting field, where the driving terms depend on the matter degrees of freedom. This will result in a transfer of energy between the matter and field, that is, it will result in the emission and absorption of radiation.

(sec-classemf-17)=

## Mode Amplitude Equations of Motion for the Interacting Field

To see these driven harmonic oscillators explicitly, we will define the amplitude vectors $\Cvec_\kvec$ in terms of $(\Avec,\partial\Avec/\partial t)$ by {eq}`eq-classemf-46a` or their inverse {eq}`eq-classemf-49a`, effectively borrowing the coordinate transformation {eq}`eq-classemf-50` from the free-field case for use in the case of the interacting field. The equation of motion for $\Avec$, however, is now the driven wave equation {eq}`eq-classemf-84`, not the free wave equation. Thus we must find the new equations of motion for the amplitude vectors $\Cvec_\kvec$, something to replace {eq}`eq-classemf-45`.

To do this we first project out the transverse components of {eq}`eq-classemf-81`, obtaining

:::{math}
:label: eq-classemf-85
{\ddot\Avec}_\kvec + \omega^2 \Avec_\kvec = 4\pi c \Jvec_{\perp\kvec},
:::

after multiplying through by $c^2$. Next we compute the quantity ${\dot\Cvec}_\kvec + i\omega\Cvec_\kvec$, which vanishes for the free field. Using {eq}`eq-classemf-49a`, we have

:::{math}
\begin{aligned}
{\dot\Cvec}_\kvec + i\omega\Cvec_\kvec &= {1\over 2}\Bigl({\dot\Avec}_\kvec + {i\over\omega} {\ddot\Avec}_\kvec\Bigr) +{i\omega\over 2} \Bigl(\Avec_\kvec + {i\over \omega}{\dot\Avec}_\kvec \Bigr)
\end{aligned}
:::

:::{math}
:label: eq-classemf-86
\begin{aligned}
&={i\over 2\omega} ({\ddot\Avec}_\kvec + \omega^2 \Avec_\kvec).
\end{aligned}
:::

But by {eq}`eq-classemf-85`, this becomes

:::{math}
:label: eq-classemf-87
{\dot\Cvec}_\kvec + i\omega\Cvec_\kvec = {2\pi i c\over \omega} \Jvec_{\perp\kvec}.
:::

This is the equation of motion for the amplitude vectors $\Cvec_\kvec$ for the interacting field that replaces {eq}`eq-classemf-45` for the free field.

Next we project out the components $C_\lambda$ of $\Cvec_\kvec$ along the polarization vectors as in {eq}`eq-classemf-59`, so that

:::{math}
:label: eq-classemf-88
C_\lambda = {\hat{\boldsymbol{\epsilon}}}_\lambda^\cc \cdot \Cvec_\kvec, \qquad \Cvec_\kvec = \sum_\mu C_\lambda {\hat{\boldsymbol{\epsilon}}}_\lambda,
:::

and similarly for the components $J_{\perp\lambda}$ of $\Jvec_{\perp\kvec}$. Thus we obtain the equations for the mode amplitudes for the interacting field,

:::{math}
:label: eq-classemf-89
{\dot C}_\lambda + i\omega C_\lambda = {2\pi i c \over \omega} J_{\perp\lambda},
:::

which replaces {eq}`eq-classemf-60` for the free field.

The method we are following here, of borrowing definitions made in the case of the free field and using them (with modified equations of motion) for the interacting field, is known in the theory of differential equations as *Lagrange's method of variation of parameters*. It is often useful for driven linear systems, precisely the type of system we are dealing with here.

(sec-classemf-18)=

## The Hamiltonian for the Matter-Field System

As in the case of the free field, we guess that the Hamiltonian for the combined matter-field system will be the total energy of that system. This energy consists of two parts, a matter (kinetic) energy and a field energy, so we write

:::{math}
:label: eq-classemf-90
H=\sum_\alpha {1\over 2}m_\alpha v_\alpha^2 + {1\over 8\pi} \int_V d^3\xvec\, (E^2 + B^2).
:::

At this point we are using the nonrelativistic expression for the kinetic energy of the particles, and, in fact, this is the first point where we have assumed that the particles are nonrelativistic. We could create a relativistically covariant classical model by using the relativistic expression for the kinetic energy of the particles, but that would lead to difficulties upon quantization since so far we only know how to handle nonrelativistic matter in quantum mechanics. We will deal with relativistic quantum mechanics later in the course, but for now we must restrain our ambitions.

You may wonder where the potential energy of the matter is in {eq}`eq-classemf-90`. As we shall see, the potential energy is hiding in the field energy. Without knowing this, however, we can check to see that the total energy, as defined by {eq}`eq-classemf-90`, is actually a constant of motion. To do that we must call on Maxwell's equations {eq}`eq-classemf-1` and {eq}`eq-classemf-2` for the field, and the nonrelativistic Newton-Lorentz equations of motion for the matter,

:::{math}
:label: eq-classemf-91
m_\alpha \ddot \rvec_\alpha = q_\alpha \Bigl[ \Evec(\rvec_\alpha) + {1\over c} \dot \rvec_\alpha \cross \Bvec(\rvec_\alpha)\Bigr].
:::

When $dH/dt$ is expanded out by the chain rule, applied to {eq}`eq-classemf-90`, and the equations of motion are used, one finds $dH/dt=0$. The quantity $H$ defined by {eq}`eq-classemf-90` is an exact constant of motion (the total energy) of the combined system of matter plus field.

The expression for the field energy in {eq}`eq-classemf-90` is the same as the one we used in the case of the free field, but now now $\Evec$ contains both a longitudinal and transverse part, see {eq}`eq-classemf-28`. Thus the electric field energy is

:::{math}
:label: eq-classemf-92
{1\over 8\pi} \int_V d^3\xvec\, (\Evec_\parallel + \Evec_\perp)^2.
:::

But the cross terms in the dot product cancel when integrated over the box, due to the Parseval identity (see {eq}`eq-classemf-25` or {eq}`eq-classemf-34`). Thus, the electric field energy decomposes into a longitudinal part and a transverse part.

As for the longitudinal part, it is

:::{math}
\begin{aligned}
{1\over 8\pi} \int_V d^3\xvec \, E^2_\parallel &= {1\over 8\pi} \int_V d^3\xvec \, \del\Phi\cdot\del\Phi = -{1\over 8\pi} \int_V d^3\xvec\, \Phi\del^2\Phi = {1\over 2} \int_V d^3\xvec\, \Phi\rho
\end{aligned}
:::

:::{math}
:label: eq-classemf-93
\begin{aligned}
&={1\over2} \sum_\beta q_\beta \Phi(\rvec_\beta) = {1\over2} \sum_{\alpha\beta} {q_\alpha q_\beta \over |\rvec_\alpha - \rvec_\beta|},
\end{aligned}
:::

where we integrate by parts in the second equality, use the Poisson equation {eq}`eq-classemf-26a` in the third, the expression {eq}`eq-classemf-77` for $\rho$ in the fourth, which allows the integral to be done, and the expression {eq}`eq-classemf-79` for $\Phi$ in the fifth. We see that the longitudinal field energy is otherwise the nonretarded Coulomb potential energy of the collection of point particles. The factor of $1/2$ compensates for the double counting of particle pairs.

Unfortunately, this sum contains the diagonal terms $\alpha=\beta$, which are infinite. These terms represent the infinite self-energy of the point particles, which as mentioned previously is a fundamental difficulty in classical electrodynamics. We will simply discard these infinite diagonal terms, and hope that the resulting theory makes sense. (In fact, it does, but only to lowest order in perturbation theory.)

As for the transverse electric contribution to the field energy, $\Evec_\perp=-(1/c)\partial\Avec/\partial t$ can be represented as a Fourier series over modes by calling on {eq}`eq-classemf-62b`, which leads to the same series in {eq}`eq-classemf-69` that was used in the case of the free field (in that case, the transverse electric field was the total electric field). Similarly, the Fourier series for the magnetic field is given by {eq}`eq-classemf-70`, which was used in the case of the free field. Thus the transverse electric and magnetic contributions to the energy, when expressed in terms of mode amplitudes, lead to the same sum over modes, {eq}`eq-classemf-73`, as in the case of the free field.

Next we guess that the correct definition of $Q_\lambda$ and $P_\lambda$ for the interacting field is the same one used for the free field, {eq}`eq-classemf-74`, since if we drive a harmonic oscillator we do not change its $q$ or $p$, we just change the equations of motion. Thus the transverse field energy is given by the same sum over harmonic oscillators, {eq}`eq-classemf-75`, that we found in the case of the free field. Thus we have

:::{math}
:label: eq-classemf-94
{1\over 8\pi} \int_V d^3\xvec \, (E_\perp^2 + B^2) = \sum_\lambda {\omega_\lambda \over 2} (Q_\lambda^2 + P_\lambda^2).
:::

As for the kinetic energy of the matter in {eq}`eq-classemf-90`, it is expressed in terms of the velocities of the particles. But Hamiltonians are normally expressed in terms of momenta, not velocities. We guess that the correct definition of the momenta of the particles is the one that is usually used in the classical dynamics of particles interacting with electromagnetic fields,

:::{math}
:label: eq-classemf-95
\pvec_\alpha = m_\alpha \dot\rvec_\alpha + {q_\alpha\over c} \Avec(\rvec_\alpha),
:::

that is, in situations where one is studying the motion of particles in given (external) fields and not attempting to include the dynamics of the field, as we are here. With this substitution, we can write the total Hamiltonian for the matter-field system as

:::{math}
:label: eq-classemf-96
H=H_matt + H_em,
:::

where

:::{math}
:label: eq-classemf-97
H_matt = \sum_\alpha {1\over 2m_\alpha} \Bigl[\pvec_\alpha -{q_\alpha\over c} \Avec(\rvec_\alpha) \Bigr]^2 + \sum_{\alpha<\beta} {q_\alpha q_\beta \over |\rvec_\alpha - \rvec_\beta|},
:::

and

:::{math}
:label: eq-classemf-98
H_em = {1\over 8\pi} \int_V d^3\xvec\, (E_\perp^2 + B^2) = \sum_\lambda {\omega_\lambda \over 2} (Q_\lambda^2 + P_\lambda^2).
:::

Again, we have made several guesses and must check that this Hamiltonian gives the correct equations of motion, according to Hamilton's equations. The equations of motion are the Newton-Lorentz equations {eq}`eq-classemf-91` for the matter, and {eq}`eq-classemf-89` for the mode amplitudes, which, as shown in \secrclassemf-17, are equivalent to the driven wave equation {eq}`eq-classemf-84` for $\Avec$, which is equivalent to the full Maxwell equations. This check will be left as an exercise.

(sec-classemf-19)=

## Exactly Conserved Quantities

The combined matter field system has several exactly conserved quantities, in addition to the energy or Hamiltonian, given by {eq}`eq-classemf-90`. These can be obtained in a systematic manner by writing down the Lagrangian for the matter-field system and then applying *Noether's theorem*, which is a general relation between symmetries and invariants in Lagrangian mechanics. The matter-field Lagrangian is invariant under several space-time symmetries, including time translations, spatial translations, and rotations. The conserved quantity associated with time translations is the energy or Hamiltonian, which we have already discussed. The conserved quantity associated with spatial translations is the momentum, given by

:::{math}
:label: eq-classemf-99
\Pvec = \sum_\alpha m_\alpha \vvec_\alpha + {1\over 4\pi c} \int d^3\xvec \, \Evec \cross \Bvec.
:::

This is the expression for the total momentum of the matter-field system, using our nonrelativistic model for the matter. One can show explicitly that $d\Pvec/dt=0$, by appealing to the equations of motion. The field contribution is proportional to the integral of the Poynting vector $(c/4\pi)\Evec\cross\Bvec$, which is the energy flux of the electromagnetic field. This however is proportional to the momentum density, $1/(4\pi c)\Evec\cross\Bvec$.

Notice that the matter contribution to the momentum is just the kinetic momentum. You may wonder where the extra term $(q_\alpha/c)\Avec(\rvec_\alpha)$ is, which is added to the kinetic momentum to get the canonical momentum $\pvec_\alpha$, as in {eq}`eq-classemf-95`. The answer is that in Coulomb gauge, this term comes from the longitudinal contribution to the field momentum, that is, it is the integral of $(1/4\pi c)\Evec_\parallel \times \Bvec$. This correction term, taking us from the kinetic to the canonical momentum, is necessary for a Hamiltonian description of charged particles interacting with fields, but it is somewhat mysterious when the fields are just considered given. But by including the field as a part of the dynamical system, we see that this contribution is just part of the field momentum. The total momentum of the matter-plus-field system is a rather simple expression.

The energy and momentum constants of motion can also be obtained by working with the stress-energy tensor for the combined matter-plus-field system. This approach is most elegant in a relativistic treatment, in which the four-divergence of the stress energy tensor vanishes. This leads to four continuity equations, one for energy and three for the components of momentum. When these are integrated over all space, the energy and momentum constants of motion emerge. The constants we have quoted above for $H$ and $\Pvec$ are the limits of the relativistic constants when the velocities of the material particles are low.

The invariance of the classical Lagrangian under rotations leads to a conservation law for angular momentum. The total angular momentum of the matter-plus-field system is

:::{math}
:label: eq-classemf-100
\Jvec = \sum_\alpha m_\alpha \rvec_\alpha \cross \vvec_\alpha +{1\over 4\pi c} \int d^3\xvec \, \xvec\cross(\Evec\cross\Bvec),
:::

where $\Jvec$ (the total angular momentum) is not to be confused with the current.

These exactly conserved quantities for the combined matter-plus-field system are the only ones that exist for that system. We have given a somewhat abbreviated discussion of them because most of the details belong in a course on classical electromagnetism. These classical conserved quantities will be of use to us later when we quantize the electromagnetic field.

(sec-classemf-20)=

## Normal Variables

Finally, we make one further cosmetic change in preparation for quantization. We define new variables $a_\lambda$,

:::{math}
\begin{aligned}
a_\lambda &= {Q_\lambda + iP_\lambda \over \sqrt{2\hbar}},
\end{aligned}
:::

:::{math}
:label: eq-classemf-101
\begin{aligned}
a_\lambda^\cc &= {Q_\lambda - iP_\lambda \over \sqrt{2\hbar}},
\end{aligned}
:::

which are obviously just classical analogs of annihilation and creation operators in quantum mechanics. We call these variables *normal variables*. The normal variables are related to the $C_\lambda$ by

:::{math}
:label: eq-classemf-102
C_\lambda = \sqrt{{2\pi\hbar c^2 \over \omega_\lambda}} \, a_\lambda.
:::

Expressing the vector potential and field Hamiltonian in terms of the normal variables, we have

:::{math}
:label: eq-classemf-103
\Avec(\xvec) = \sqrt{{2\pi\hbar c^2\over V}} \sum_\lambda {1\over\sqrt{\omega_\lambda}} \Bigl[ a_\lambda \epsilonvec_\lambda \, e^{i\kvec\cdot\xvec} + \\textc.c. \Bigr],
:::

and

:::{math}
:label: eq-classemf-104
H_em = \sum_\lambda \hbar\omega_\lambda |a_\lambda|^2.
:::

The fields $\Evec_\perp$ and $\Bvec$ can also be expressed in terms of normal variables,

:::{math}
:label: eq-classemf-105
\Evec_\perp(\xvec) = -{1\over c}\frac{\partial \Avec}{\partial t} = {1\over c}\sqrt{{2\pi\hbar c^2\over V}} \sum_\lambda \sqrt{\omega_\lambda} \Bigl[ia_\lambda \epsilonvec_\lambda\, e^{i\kvec\cdot\xvec} +\\textc.c.\Bigr],
:::

and

:::{math}
:label: eq-classemf-106
\Bvec(\xvec) = \del\cross\Avec = \sqrt{{2\pi\hbar c^2\over V}} \sum_\lambda {1\over\sqrt{\omega_\lambda}} \Bigl[ ia_\lambda (\kvec\cross\epsilonvec_\lambda) e^{i\kvec\cdot\xvec} + \\textc.c.\Bigr].
:::

\problems

(prob-classemf-1)=

**Problem \prbdclassemf-1..** 

\problempart{(a)} Calculate, as a function of $\rvec(t)$, the electric field $\Evec_\parallel(\xvec,t)$ at point $\xvec$ and time $t$ from charge $q$. Show that $\Evec_\parallel(\xvec,t)$ can be written,

:::{math}
:label: eq-classemf-107
\Evec_\parallel(\xvec,t) = \Evec_\parallel(\xvec,0) + \delta\Evec_\parallel(\xvec,t),
:::

where $\delta\Evec_\parallel$ is given by a power series in $|\rvec(t)|/R$. Show that the lowest order term of this expansion can be expressed as a function of $q\rvec(t)$ and of the transverse $\delta$-function, $\Delta^\perp_{ij}(\xvec)$.

\problempart{(b)} Find the current $\Jvec(\xvec,t)$ associated with the motion of the particle. Express the transverse current $\Jvec_\perp(\xvec,t)$ at the point of observation $\xvec$ as a function of $q\dot\rvec(t)$ and the transverse $\delta$-function $\Delta^\perp_{ij}(\xvec-\rvec(t))$. Explain why to the lowest order in $|\rvec(t)|/R$, one can replace $\Delta^\perp_{ij}(\xvec-\rvec(t))$ by $\Delta^\perp_{ij}(\xvec)$. Write the Maxwell equation giving $\partial \Evec_\perp(\xvec,t)/\partial t$ in terms of $\Jvec_\perp(\xvec,t)$ and $\Bvec(\xvec,t)$. Begin by ignoring the contribution of $\Bvec$ to $\partial \Evec_\perp/\partial t$. Integrate the equation between $0$ and $t$. Show that the transverse electric field $\Evec_\perp(\xvec,t)$ produced by $\Jvec_\perp(\xvec,t)$ compensates exactly (to lowest order in $|\rvec(t)|/R$) the field $\delta\Evec_\parallel(\xvec,t)$ found in part (a). The small parameter here is $r/R$, not $v/c$; the particle motion could be fast (relativistic).

\problempart{(c)} By eliminating the electric field from Maxwell's equations, find the equation of motion for the magnetic field $\Bvec$. Justify the approximation made above of neglecting the contribution of $\Bvec$ to $\partial\Evec_\perp/\partial t$ over short periods ($T\ll R/c$).

(prob-classemf-2)=

**Problem \prbdclassemf-2..** 

Please note the difference between $\xvec$, an arbitrary point of space at which a field may be evaluated, and $\rvec_\alpha$, the position of particle $\alpha$. The field point $\xvec$ is not a dynamical variable; it does not have an equation of evolution. The point $\rvec_\alpha$ is a dynamical variable; it does have an equation of motion.

The quantity $a_\lambda$ is classical, in spite of the $\hbar$. We could have written $\Avec$ in terms of the mode amplitude $C_\lambda$, defined by {eq}`eq-classemf-88`, but $a_\lambda$, which is proportional to $C_\lambda$, is more convenient since it carries over to the annihilation operator in quantum mechanics.

\problempart{(a)} Use the chain rule to show that Hamilton's classical equations for $Q_\lambda$ and $P_\lambda$ are equivalent to

:::{math}
:label: eq-classemf-108
\begin{aligned}
{\dot a}_\lambda &= -{i\over\hbar} \frac{\partial H}{\partial a_\lambda^\cc}, \\
{\dot a}^\cc_\lambda &= {i\over\hbar} \frac{\partial H}{\partial a_\lambda}, \\

\end{aligned}
:::

which are more convenient for the following work. Notice that these equations are complex conjugates of each other.

\problempart{(b)} Now use Hamilton's equations for $\rvec_\alpha$ to obtain

:::{math}
:label: eq-classemf-109
m_\alpha\vvec_\alpha = m_\alpha{\dot\rvec}_\alpha = \pvec_\alpha - {q_\alpha\over c}\Avec(\rvec_\alpha).
:::

\problempart{(c)} What we mean by $\partial \Avec(\xvec)/\partial t$ is the time derivative of the field $\Avec$, evaluated at some field point $\xvec$, holding $\xvec$ fixed. We also call this $\dot \Avec(\xvec)$. The time evolution is due to the time dependence of the $a_\lambda$ and $a^\cc_\lambda$, upon which $\Avec$ depends. With this understanding, we have

:::{math}
:label: eq-classemf-110
{\dot\Avec}(\xvec;a_\lambda,a^\cc_\lambda) = \frac{\partial \Avec(\xvec)}{\partial t} = \sum_\lambda \Bigl[\pop{\Avec(\xvec; a_\lambda, a^\cc_\lambda)} {a_\lambda}\,{\dot a}_\lambda + c.c.\Bigr],
:::

where we have shown explicitly that $\Avec$ depends on the $a_\lambda$ and $a^\cc_\lambda$. Show that Hamilton's equations imply

:::{math}
:label: eq-classemf-111
\dot \Avec(\xvec) = \sqrt{2\pi\hbar c^2\over V} \sum_\lambda \sqrt{\omega_\lambda} \bigl( -ia_\lambda \epsilonvec_\lambda e^{i\kvec\cdot\xvec} + c.c.\bigr).
:::

This is equivalent to {eq}`eq-classemf-62b`, with the coefficients $C_\lambda$ replaced by $a_\lambda$ according to {eq}`eq-classemf-102`. Hint: Notice the resolution of identity, {eq}`eq-classemf-53`, which allows you to do the polarization ($\mu$) sum.

\problempart{(d)} Now show that

:::{math}
:label: eq-classemf-112
m_\alpha \ddot \rvec_\alpha = q_\alpha \Bigl[ \Evec(\rvec_\alpha) + {1\over c} \vvec_\alpha \cross \Bvec(\rvec_\alpha) \Bigr],
:::

where $\Evec$ is the total electric field, longitudinal plus transverse. Notice that the time derivative of $\Avec(\rvec_\alpha; a_\lambda, a^\cc_\lambda)$ must be interpreted as

:::{math}
:label: eq-classemf-113
\dod{\Avec(\rvec_\alpha;a_\lambda,a^\cc_\lambda)}{t} = \frac{\partial \Avec(\rvec_\alpha;a_\lambda,a^\cc_\lambda)}{\partial \rvec_\alpha} \cdot \vvec_\alpha + {\dot\Avec}(\rvec_\alpha; a_\lambda,a^\cc_\lambda),
:::

since the field is evaluated at the particle position, and the particle position is moving.

\problempart{(e)} Finally show that

:::{math}
:label: eq-classemf-114
{\ddot\Avec} = c^2\del^2\Avec + 4\pi c \Jvec_\perp.
:::

This equation is equivalent to Maxwell's equations.

(prob-classemf-3)=

**Problem \prbdclassemf-3..**
