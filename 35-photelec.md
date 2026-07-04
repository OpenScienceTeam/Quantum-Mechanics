---
title: "35. The Photoelectric Effect"
---
(ch-photelec)=

# 35. The Photoelectric Effect

(sec-photelec-1)=

## Introduction

In these notes we consider the ejection of an atomic electron by an incident photon, which is an example of the photoelectric effect. The photon should have an energy in the ultraviolet to x-ray range, for reasons to be explained below; thus, our results will provide a semi-quantitative model for the absorption of x-rays by matter. In these notes, we use a version of the semiclassical theory of radiation, in which the radiation field is treated classically, but the atomic system quantum mechanically. Certain quantum mechanical concepts, notably photons, are used in the description of the classical radiation field. The photoelectric effect is not only interesting and important physically, but the following calculation also provides excellent exercise in time-dependent perturbation theory, the treatment of cross s, and assorted physical facts.

(sec-photelec-2)=

## The Incident Photon

We suppose the incident photon has energy $E_0=\hbar\omega_0$ and momentum $\pvec_0=\hbar\kvec_0$. (We use the 0 subscript to refer to the incident photon; quantities without this subscript, such as $E$ or $\kvec$, will refer to the ejected electron.) For simplicity, we assume the atom has a single electron (or a single electron of interest), and that it is initially in its ground state. We let $E_g$ be the energy of this ground state; naturally, $E_g<0$. Then by conservation of energy, we must have

:::{math}
:label: eq-photelec-1
\hbar\omega_0 > |E_g|,
:::

so that the photon will have enough energy to eject the electron.

Actually, we will make a stronger assumption, namely,

:::{math}
:label: eq-photelec-2
\hbar\omega_0 \gg |E_g|,
:::

for the following reason. Assuming the atom is initially neutral, the ejected electron leaves a positive ion behind and travels out in the long-range Coulomb field of the ion. Therefore the final electron state is not that of a free particle, but rather one of the unbound or positive energy solutions of the Coulomb potential. The unbound Coulomb wave functions are important in many applications, and they can be determined by the usual methods for solving differential equations (power series, etc). These wave functions turn out to be hypergeometric functions, and for serious work involving Coulomb scattering and other applications one must know about them. Nevertheless, it would be simpler if we could deal with free particle wave functions for the final electron states. We can do this in a certain approximation if we assume that the energy of the ejected electron is much greater than the binding energy $|E_g|$, so that the ejected electron does not feel the Coulomb field very much. This is why we make the assumption {eq}`eq-photelec-2`, so that we can approximate the final electron wave functions by free particle solutions.

By energy conservation we have

:::{math}
:label: eq-photelec-3
\hbar\omega_0 + E_g = E,
:::

where $E$ is the final electron energy. Under the condition {eq}`eq-photelec-2`, both $\hbar\omega_0$ and $E$ will be large compared to $|E_g|$, and nearly equal to one another. Therefore we can rewrite the condition {eq}`eq-photelec-2` in another form, and combine it with the condition that our electron be nonrelativistic, by writing

:::{math}
:label: eq-photelec-4
|E_g| \ll E \ll mc^2.
:::

This can be put into dimensionless form by dividing by $mc^2$,

:::{math}
:label: eq-photelec-5
(Z\alpha)^2 \ll {E\over mc^2} \ll 1,
:::

where we use the estimate $|E_g| \sim (Z\alpha)^2 mc^2$, valid for hydrogen-like atoms. For example, in the case of hydrogen, we might restrict the energy of the incident photon to lie in the range,

:::{math}
:label: eq-photelec-6
100~ev <\approx \hbar\omega_0 <\approx 100~Kev.
:::

Such photons lie in the far ultraviolet to x-ray region. If we were willing to deal with hypergeometric functions we could extend the lower limit downward; if we were willing to use relativistic quantum mechanics, we could extend the upper limit upwards. But we will live with the stated limits.

We will describe the incident photon by means of a classical light wave, with vector potential

:::{math}
:label: eq-photelec-7
\Avec(\xvec,t) = A_0 \epsilonvec e^{i(\kvec_0\cdot\xvec-\omega_0t)} + \\textc.c.,
:::

where $A_0$ is the amplitude (assumed to be real), and where $\epsilonvec$ is the polarization unit vector (also assumed to be real, indicating linear polarization). This vector potential is in the Coulomb gauge (the scalar potential is taken to be zero), so that

:::{math}
:label: eq-photelec-8
\del\cdot\Avec=0,
:::

as follows by taking the divergence of {eq}`eq-photelec-7` and using the transversality condition,

:::{math}
:label: eq-photelec-9
\epsilonvec\cdot\kvec_0=0.
:::

(sec-photelec-3)=

## The Atomic System

The atomic system for the one-electron atom described by the unperturbed Hamiltonian,

:::{math}
:label: eq-photelec-10
H_0={p^2\over 2m} + V(\xvec).
:::

For part of the following calculation we can leave $V(\xvec)$ unspecified, but at a certain point we will specialize to a hydrogen-like atom with

:::{math}
:label: eq-photelec-11
V(\xvec) = -{Ze^2\over r}.
:::

As mentioned, we assume that the atom is initially in its ground state $\ket{g}$ with energy $E_g$, so that

:::{math}
:label: eq-photelec-12
H_0\ket{g} = E_g \ket{g}.
:::

We will assume that the unbound electron in the final state is described by a plane wave with wave vector $\kvec$,

:::{math}
:label: eq-photelec-13
\psi_\kvec(\xvec) = \braket{\xvec}{\kvec} = {e^{i\kvec\cdot\xvec} \over \sqrt{V}},
:::

where we adopt box normalization as in {eq}`eq-tdpt-63`--{eq}`eq-tdpt-65`. The final energy is denoted $E$.

The perturbing Hamiltonian is

:::{math}
:label: eq-photelec-14
H_1 = {e\over mc}\pvec\cdot\Avec,
:::

which comes from expanding $(1/2m)(\pvec+e\Avec/c)^2$ and dropping the term in $\Avec^2$. We note that $\pvec\cdot\Avec=\Avec\cdot\pvec$ because of the Coulomb gauge condition {eq}`eq-photelec-8`. We will also write the perturbing Hamiltonian in the form,

:::{math}
:label: eq-photelec-15
H_1(t) = K e^{-i\omega_0t} + K^\hc e^{+i\omega_0t}
:::

[see {eq}`eq-tdpt-39`], so that

:::{math}
:label: eq-photelec-16
K = {eA_0\over mc} (\epsilonvec\cdot\pvec) e^{i\kvec_0\cdot\xvec}.
:::

We drop the term in $\Avec^2$ because we will be working only to first order in perturbation theory; if we were to go to second order, this term would have to be included.

(sec-photelec-4)=

## The Transition Rate

We can now proceed to the transition rate, which follows from {eq}`eq-tdpt-42` and which we write in the form,

:::{math}
:label: eq-photelec-17
w = {2\pi\over \hbar^2} \sum_\kvec |\matrixelement{\kvec}{K}{g}|^2 \Delta_t(\omega),
:::

where

:::{math}
:label: eq-photelec-18
\omega={E-\hbar\omega_0-E_g \over \hbar} = {1\over\hbar} \Bigl( {\hbar^2 k^2 \over 2m} - \hbar\omega_0 - E_g \Bigr).
:::

The sum in {eq}`eq-photelec-17` is to be taken over final states which lie in a small cone of solid angle $\Delta\Omega$ about some final wave vector $\kvec_f$, as in Fig.~\figr\tdpt.5. We choose the direction of $\kvec_f$ to be some direction of interest, and we choose the magnitude of $\kvec_f$ by conservation of energy, so that

:::{math}
:label: eq-photelec-19
{\hbar^2 k_f^2 \over 2m} = \hbar\omega_0 + E_g.
:::

The notational difference between $\kvec$ and $\kvec_f$ is that $\kvec$ is a variable final electron state over which we are summing, which does not necessarily conserve energy, while $\kvec_f$ does conserve energy and is in some fixed direction of interest.

Next we make the replacement

:::{math}
:label: eq-photelec-20
w \to \dod{w}{\Omega} \Delta\Omega
:::

and the replacement {eq}`eq-tdpt-76` in {eq}`eq-photelec-17`, in order to go over to the transition rate per unit solid angle. This gives

:::{math}
:label: eq-photelec-21
\dod{w}{\Omega} = {2\pi\over\hbar^2} {V\over(2\pi)^3} \int_0^\infty k^2 \, dk\, |\matrixelement{\kvec}{K}{g}|^2 \Delta_t(\omega),
:::

which we will transform in various ways. First we must relate $dw/d\Omega$ to the differential cross ,

:::{math}
:label: eq-photelec-22
\dod{w}{\Omega} = n_i v_i \dod{\sigma}{\Omega},
:::

where $n_i$ is the number density of the incident particles and $v_i$ is their velocity. But since the incident particles are photons, their velocity is $v_i=c$.

To compute $n_i$ we must mix classical and quantum concepts. An incident beam consisting of $n_i$ photons per unit volume has an energy density $u=n_i\hbar\omega_0$; on the other hand, by classical electromagnetic theory we have $u=(E^2+B^2)/8\pi$. In the light wave {eq}`eq-photelec-7` the electric and magnetic contributions to the energy density are equal, and cross terms vanish when we average over the volume of the box. Thus we find,

:::{math}
:label: eq-photelec-23
u={E^2+B^2\over 8\pi} = {\omega_0^2 A_0^2 \over 2\pi c^2} = n_i\hbar\omega_0,
:::

or

:::{math}
:label: eq-photelec-24
n_i = {\omega_0 A_0^2 \over 2\pi\hbar c^2} = {k_0 A_0^2 \over 2\pi\hbar c},
:::

where we have used $\omega_0=ck_0$. We now solve {eq}`eq-photelec-22` for the cross , finding,

:::{math}
:label: eq-photelec-25
\dod{\sigma}{\Omega} = {2\pi\hbar \over k_0 A_0^2} \dod{w}{\Omega}.
:::

(sec-photelec-5)=

## The Matrix Element and Cross Section

Next we work on the right hand side of {eq}`eq-photelec-21`. First, we write out the matrix element, using {eq}`eq-photelec-16`,

:::{math}
:label: eq-photelec-26
\matrixelement{\kvec}{K}{g} = {eA_0\over mc} \matrixelement{\kvec} {(\epsilonvec\cdot\pvec) e^{i\kvec_0\cdot\xvec}}{g} = {eA_0\hbar\over mc} (\epsilonvec\cdot\kvec) \matrixelement{\kvec}{e^{i\kvec_0\cdot\xvec}}{g},
:::

where in the final step we have allowed the momentum operator $\pvec$ to act to the left on the plane wave state $\bra{\kvec}$, bringing out a factor of $\hbar\kvec$. The remaining matrix element can be expressed in terms of the Fourier transform of the ground state wave function $\psi_g(\xvec)=\braket{\xvec}{g}$,

:::{math}
:label: eq-photelec-27
\matrixelement{\kvec}{e^{i\kvec_0\cdot\xvec}}{g} = {1\over\sqrt{V}} \int d^3\xvec \, e^{-i(\kvec-\kvec_0)\cdot\xvec} \, \psi_g(\xvec) = {(2\pi)^{3/2}\over \sqrt{V}} \tilde \psi_g(\qvec),
:::

where

:::{math}
:label: eq-photelec-28
\qvec=\kvec-\kvec_0
:::

and where

:::{math}
:label: eq-photelec-29
\tilde \psi_g(\qvec) = \int {d^3\xvec \over (2\pi)^{3/2}} \, e^{-i\qvec\cdot\xvec} \, \psi_g(\xvec).
:::

Finally, we transform the function $\Delta_t(\omega)$ in {eq}`eq-photelec-21`, using {eq}`eq-photelec-18` and {eq}`eq-photelec-19`:

:::{math}
:label: eq-photelec-30
\Delta_t(\omega) \to \delta(\omega) = {m\over \hbar k} \delta(k-k_f).
:::

At this point we remark that had we been doing a problem in the emission or absorption of optical radiation from an atom, we would have been able to expand the exponential $e^{i\kvec_0\cdot\xvec}$ in {eq}`eq-photelec-26`, since radiation in this frequency range satisfies $k_0r \ll 1$ (the wavelength is much larger than the atomic size). This would lead to the multipole expansion (the dipole approximation at lowest order). We cannot make this expansion in the present calculation, however, because we are dealing with radiation of short wavelength, such as x-rays.

We now gather all the pieces together [{eq}`eq-photelec-25`, {eq}`eq-photelec-21`, {eq}`eq-photelec-26`, {eq}`eq-photelec-27` and {eq}`eq-photelec-30`] to obtain

:::{math}
:label: eq-photelec-31
\dod{\sigma}{\Omega} = {2\pi\hbar\over k_0 A_0^2} {2\pi\over\hbar^2} {V\over (2\pi)^3} \int_0^\infty k^2 \, dk \, {e^2 A_0^2 \hbar^2 \over m^2 c^2} (\epsilonvec\cdot\kvec)^2 {(2\pi)^3\over V} |\tilde\psi_g(\qvec)|^2 {m\over \hbar k} \delta(k-k_f),
:::

or,

:::{math}
:label: eq-photelec-32
\dod{\sigma}{\Omega} = (2\pi)^2 {e^2\over mc^2} {k_f\over k_0} (\epsilonvec\cdot\kvec_f)^2 |\tilde\psi_g(\qvec)|^2,
:::

where now $\qvec=\kvec_f-\kvec_0$. We see that all the volume factors cancel out of {eq}`eq-photelec-31`, as they should, as do the factors of $A_0$, which we expect because a cross by definition is independent of the incident flux. The vector $\qvec=\kvec_f-\kvec_0$ reminds us of the momentum transfer vector $\kvec_f-\kvec_i$ which occurred in our analysis of elastic scattering in {ref}`ch-tdpt`, but here the quantity $\hbar\qvec$ is the momentum difference between the final electron and the initial photon. Unlike the case of elastic scattering, where we had $k_f=k_i$, here the vectors $\kvec_f$ and $\kvec_0$ are of different magnitudes.

(sec-photelec-6)=

## Momentum Transfer

The fact that the vector $\qvec$ is nonzero means that a proper understanding of momentum conservation must take into account the nucleus as well as the photon and the electron. The reason the nuclear momentum has not appeared explicitly in our calculations is that we implicitly assumed in writing down {eq}`eq-photelec-10` that the nuclear mass was infinitely large in comparison to the electron mass. This of course is a good approximation, and it means that the nucleus can carry off a large amount of momentum without moving very fast. In the limit of infinite nuclear mass, the nucleus acts like a momentum source or sink which is able to provide whatever momentum is needed for the reaction at hand. This is important, because in the absence of such a momentum source, a reaction such as

:::{math}
:label: eq-photelec-33
\gamma +e \to e,
:::

that is, the absorption of a photon by a free electron, is impossible (one cannot satisfy both energy and momentum conservation in this reaction). Similarly, in the absence of a momentum source, the reaction

:::{math}
:label: eq-photelec-34
e \to e +\gamma
:::

is impossible. But if there is a nucleus nearby to take up some momentum, then the reaction {eq}`eq-photelec-34` does occur; this is called *Bremsstrahlung* (German for “braking radiation”), and it is one of the principal mechanisms for the slowing down of fast charged particles in matter (especially important for light particles like electrons and muons). Our assumption of infinite nuclear mass in the present calculation has caused the conservation of momentum to appear only implicitly, in contrast to the conservation of energy, which is explicitly expressed by the $\delta$-function in {eq}`eq-photelec-31`.

We have written the cross {eq}`eq-photelec-32` so that the classical radius of the electron $r_e$ makes its appearance,

:::{math}
:label: eq-photelec-35
r_e = {e^2\over mc^2} = \alpha^2 a_0 =2.82 \times 10^{-13} cm.
:::

This radius is called classical because there is no $\hbar$ in it; its physical meaning is that it is the radius (to within an order of magnitude) outside of which the electrostatic energy of the nominal monopole field (divided by $c^2$) equals the mass of the electron. The total electrostatic energy in the field of a monopole is, of course, infinite.

To proceed with the analysis, we will now assume that $V(r)=-Ze^2/r$, for a hydrogen-like atom. Then the ground state wave function is

:::{math}
:label: eq-photelec-36
\psi_g(\xvec) = {1\over \sqrt{\pi a^3}} \, e^{-r/a},
:::

where $a=a_0/Z$ and $a_0$ is the usual Bohr radius. It is then straightforward to compute the Fourier transform, according to {eq}`eq-photelec-29`. We find

:::{math}
:label: eq-photelec-37
\tilde \psi_g(\qvec) = {1\over \pi} {(2a)^{3/2} \over (1+a^2q^2)^2}.
:::

This is obviously proportional to the momentum-space wave function of the ground state of the hydrogen atom; notice that it is a rational function of the momentum. In any case, the cross now becomes

:::{math}
:label: eq-photelec-38
\dod{\sigma}{\Omega} = 32 {e^2 \over mc^2} {k_f \over k_0} |\epsilonvec\cdot\kvec_f|^2 {a^3 \over (1+a^2q^2)^4}.
:::

(sec-photelec-7)=

## Approximating the Cross Section

This cross can be boiled down further by incorporating the approximation {eq}`eq-photelec-4`. This occurs in two steps. First, it turns out that the initial photon wave number $k_0$ is much smaller than the final electron wave number $k_f$. To show this, we write out the conservation of energy equation {eq}`eq-photelec-3` in the form

:::{math}
:label: eq-photelec-39
\hbar\omega_0 = \hbar ck_0 \approx {\hbar^2 k_f^2 \over 2m},
:::

where we neglect $E_g$ in comparison to $\hbar\omega_0$. But this can be put in the form,

:::{math}
:label: eq-photelec-40
{k_0\over k_f} \approx {\hbar k_f \over 2mc} = {p_f\over 2mc} = {v_f\over 2c} \ll 1,
:::

where $p_f$ and $v_f$ are the final electron momentum and velocity, respectively, and where we make use of the nonrelativistic assumption $E\ll mc^2$. We see that $k_0/k_f$ is indeed small, of the order of $v_f/c$, and for consistency in a nonrelativistic treatment, we should neglect terms of relative order

:::{math}
:label: eq-photelec-41
\Bigl( {k_0\over k_f} \Bigr)^2 \sim \Bigl( {v_f \over c} \Bigr)^2.
:::

For example, the quantity $q^2$, which occurs in the cross {eq}`eq-photelec-38`, can be approximated,

:::{math}
\begin{aligned}
q^2 &= (\kvec_f - \kvec_0)^2 \approx k_f^2 -2\kvec_f\cdot\kvec_0 = k_f^2 - 2k_f k_0 \cos\theta
\end{aligned}
:::

:::{math}
:label: eq-photelec-42
\begin{aligned}
&= k_f^2 \Bigl( 1 - {v_f\over c} \cos\theta \Bigr),
\end{aligned}
:::

where we neglect terms of relative order $(k_0/k_f)^2$. This is the first approximation.

On the other hand, we also have

:::{math}
:label: eq-photelec-43
a^2k_f^2 = {2ma^2\over \hbar^2} {\hbar^2 k_f^2 \over 2m} \sim {\hbar^2\over Z^2 m e^4} E \sim {E \over |E_g|} \gg 1,
:::

so that

:::{math}
:label: eq-photelec-44
1+a^2q^2 \approx a^2 k_f^2 \Bigl( 1 - {v_f\over c}\cos\theta \Bigr).
:::

This is the second approximation.

:::{figure} images/photelec-fig01.png
:label: fig-photelec-1
:width: 80%

Coordinates for the photoelectric effect.
:::

(sec-photelec-8)=

## Angular Dependence and Total Cross Section

We now introduce coordinates, as illustrated in {ref}`fig-photelec-1`. We assume the atom is at the origin, and that the photon comes in along the negative $z$-axis, so that $\kvec_0 = k_0{\hat{\mathbf{z}}}$. The photon is assumed to be linearly polarized in the $x$-direction, so that $\epsilonvec={\hat{\mathbf{x}}}$. The ejected electron goes out in the direction $(\theta,\phi)$.

With the geometry indicated in {ref}`fig-photelec-1` and the approximations {eq}`eq-photelec-42` and {eq}`eq-photelec-44`, we can simplify the cross {eq}`eq-photelec-38`. We find

:::{math}
:label: eq-photelec-45
\dod{\sigma}{\Omega} = {32\over k_0} \Bigl( {e^2\over mc^2} \Bigr) {1 \over (k_fa)^5} {\sin^2\theta \cos^2\phi \over [1 - (v_f/c)\cos \theta]^4}.
:::

This is the cross for linear polarization in the $x$-direction. If we had had linear polarization in the $y$-direction, we would have obtained $\sin^2 \phi$ in {eq}`eq-photelec-45` instead of $\cos^2\phi$. To deal with the case of unpolarized light, we must average over initial polarizations; this can be carried out formally by using a density matrix for the photons, but in the present case it amounts to adding $\sin^2\phi$ and $\cos^2\phi$ and dividing by 2. If we also expand the denominator to first order in $v_f/c$, we obtain

:::{math}
:label: eq-photelec-46
\Bigl(\dod{\sigma}{\Omega}\Bigr)_unpol = {16\over k_0} \Bigl( {e^2\over mc^2} \Bigr) {1\over(k_fa)^5} \sin^2\theta \Bigl( 1 + 4{v_f\over c}\cos\theta \Bigr).
:::

Finally, we can integrate this over all solid angles of the final ejected electron, whereupon the term in $\cos\theta$ disappears, to obtain the total cross for unpolarized radiation,

:::{math}
:label: eq-photelec-47
\sigma_tot = {128 \pi \over 3} {1\over k_0} \Bigl( {e^2\over mc^2} \Bigr) {1\over (ak_f)^5}.
:::

The total cross can be written in various ways; for example, we can express it in terms of the incident photon energy $E_0 =\hbar\omega_0$ and the Bohr radius $a_0$ of hydrogen:

:::{math}
:label: eq-photelec-48
\sigma_tot = {16\pi\sqrt{2}\over 3} \alpha^8 Z^5 a_0^2 \Bigl( {mc^2 \over E_0} \Bigr)^{7/2},
:::

where $\alpha$ is the fine structure constant. In this form the cross is manifestly an area, since $a_0^2$ is essentially the cross-al area of a hydrogen atom. This area is reduced by the very small factor $\alpha^8$, but magnified by the presumably large factor $(mc^2/E_0)^{7/2}$ (because of the nonrelativistic assumption $E\ll mc^2$), and by the possibly large factor $Z^5$. Although this formula was derived only for a hydrogen-like atom, it is valid in a semiquantitative way for the ejection of $K$-shell electrons by x-rays in any atom. The strong $Z$-dependence indicates that heavier atoms are more effective in stopping x-rays, and the strong inverse energy dependence indicates that hard x-rays are more penetrating than soft ones.

\problems

(prob-photelec-1)=

**Problem \prbdphotelec-1..** 

:::{math}
:label: eq-photelec-49
{e^2\over a_0} \ll E_0 \ll mc^2,
:::

where $a_0$ is the usual (hydrogen) Bohr radius, and make approximations this set of notes. In particular, expand your answer through first order in $v_f/c$. Find the total cross and express it as a function of $E_0$, and as a multiple of $a_0^2$.

Note that the light wave interacts with both the electron and the positron; therefore you must set up a two-particle Hamiltonian.
