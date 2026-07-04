---
title: "14. Spins in Magnetic Fields"
---
(ch-spinmagf)=

# 14. Spins in Magnetic Fields

(sec-spinmagf-1)=

## Introduction

A nice illustration of rotation operator methods that is also important physically is the problem of spins in magnetic fields. The earliest experiments along these lines were those of Stern and Gerlach, which in 1922 first revealed the quantization of electron spin. Similar but later experiments by Stern and other collaborators were used to make crude measurements of the proton magnetic moment and other nuclear magnetic moments. In the 1930's Rabi developed the techniques of spin flipping with time-dependent magnetic fields, which he used to make much more accurate measurements of nuclear magnetic moments as well as important discoveries such as the existence of an electric quadrupole moment in the deuteron. After World War II, Bloch and Purcell developed methods for studying magnetic resonance in bulk samples (solid or liquid), by measuring microwave power absorbed at resonance or by looking at the time development and relaxation of induced magnetization. In the same period, Rabi's beam techniques were improved upon by Ramsey and Hahn developed the method of spin echo, in which the dephasing of a bulk magnetization is time-reversed following a spin flip and the original magnetization is restored. The spin echo technique now forms the basis of medical imaging by magnetic resonance. Modern applications of magnetic resonance include measurements of nuclear magnetic moments and $g$-factors, measurements of diamagnetic shielding of external fields in molecules or solids (important in chemistry and solid state physics), the construction of sensitive magnetometers and atomic clocks, and tomography or imaging in medicine and biology.

Earlier in the course we examined experimental and gedanken-experimental data from the Stern-Gerlach experiment, which concerned the measurement of the magnetic moment $\muvec$ of silver atoms. In these notes we will focus on the magnetic moments of a variety of particles, including elementary particles such as the electron and muon and well as composite particles such as nucleons (protons and neutrons), nuclei themselves, atoms and molecules. The existence of a magnetic moment, a vector of observables, implies that there is a kind of internal, orientational degree of freedom to such particles. This degree of freedom is associated with what we call the “spin” of the particle, which is the generator of rotations on the Hilbert space describing these internal degrees of freedom.

(sec-spinmagf-2)=

## Magnetic Moments and Angular Momentum

We begin by reviewing magnetic moments in classical electromagnetism. Consider a localized current distribution $\Jvec(\xvec)$. (This is the electric current, not to be confused with an angular momentum.) You may think of the currents that are present in an atom or nucleus. Associated with this current distribution is the *magnetic moment*, defined by

:::{math}
:label: eq-spinmagf-1
\muvec = {1\over 2c} \int d^3\xvec'\, \xvec'\cross\Jvec(\xvec').
:::

Here we write the variable of integration as $\xvec'$, which runs over the current distribution, to distinguish it from field points $\xvec$ to be introduced momentarily. Since $\xvec'$ is integrated over, the magnetic moment does not depend on position $\xvec$, but it may depend on time.

If the current distribution is placed in an external magnetic field $\Bvec(\xvec)$ then it experiences a force and a torque given by

:::{math}
:label: eq-spinmagf-2
\begin{aligned}
\Fvec &= \del[\muvec\cdot\Bvec(\xvec)],
\end{aligned}
:::

:::{math}
:label: eq-spinmagf-3
\begin{aligned}
\Tvec &= \muvec\cross\Bvec(\xvec).
\end{aligned}
:::

These expressions are derived in books on electromagnetism, such as Jackson, *Classical Electrodynamics*. They are based on the approximation that the magnetic field is slowly varying over the extent of the current distribution, something that for laboratory scale magnetic fields and dipoles of atomic or nuclear size would be an excellent approximation. Note that in {eq}`eq-spinmagf-2` the gradient operator only acts on $\Bvec(\xvec)$, since $\muvec$ is independent of $\xvec$. The current distribution is presumably produced by charged particles. If the force {eq}`eq-spinmagf-2` is the only force acting on the system and if $\xvec$ above is chosen to be the center of mass then by Newton's laws we obtain an equation of motion for the center of mass of the system,

:::{math}
:label: eq-spinmagf-4
m{d^2\xvec\over dt^2} = \del[\muvec\cdot\Bvec(\xvec)],
:::

and another for the angular momentum of the system about the center of mass,

:::{math}
:label: eq-spinmagf-5
\dod{\Lvec}{t} = \muvec\cross\Bvec(\xvec).
:::

Equation {eq}`eq-spinmagf-4` normally applies to a system that is electrically neutral, such as a neutron or a silver atom; if the system has a net charge then there will also be the Lorentz force $(q/c)\vvec\cross\Bvec$ and possibly an electric force $q\Evec$.

We cannot solve {eq}`eq-spinmagf-4` for the trajectory of the center of mass $\xvec$ without knowing how $\muvec$ depends on time. Thus, we also need an equation for the time dependence of $\muvec$. {eq}`eq-spinmagf-5` is not that, unless we have a relation between $\muvec$ and $\Lvec$.

In some circumstances $\muvec$ is proportional to $\Lvec$, in fact, such a proportionality is implied by the Stern-Gerlach results analyzed in {ref}`ch-postulat`. Those results, combined with a further analysis of signs and phase conventions [see {eq}`eq-postulat-24` and \spatialdof.16], show that for a silver atom

:::{math}
:label: eq-spinmagf-6
\muvec=-\mu_0\,\sigmavec,
:::

where $\sigmavec$ are the Pauli matrices and $\mu_0$ is a constant of dimensions of magnetic moment that can be determined experimentally. In fact, Stern and Gerlach measured $\mu_0$, obtaining a value close to the *Bohr magneton*, a unit of magnetic moment given by

:::{math}
:label: eq-spinmagf-7
\mu_B={e\hbar\over 2 m_e c}.
:::

On the other hand, our analysis in {ref}`ch-spinrot`{} of rotations and angular momentum for spin-$\frac{1}{2}$ systems showed that $\Svec=(\hbar/2)\sigmavec$, where now we write $\Svec$ for the angular momentum instead of the general notation $\Jvec$ used in {eq}`eq-spinrot-25`. Combined with {eq}`eq-spinmagf-6` this shows that for a silver atom,

:::{math}
:label: eq-spinmagf-8
\muvec=-{e\over m_e c}\Svec.
:::

This relation actually describes the electron, since a silver atom acquires both its magnetic moment and angular momentum from its single, unpaired valence electron.

At this point it is instructive to consider a simple classical model of magnetic moment and angular momentum. Consider, for example, a particle of mass $m$, charge $q$, position $\xvec$ and velocity $\vvec$ in a circular orbit of radius $a$. Placing the orbit in the $x$-$y$ plane, the angular momentum is

:::{math}
:label: eq-spinmagf-9
\Lvec=m \xvec\cross\vvec = mva\,{\hat{\mathbf{z}}},
:::

while according to {eq}`eq-spinmagf-1` the magnetic moment is

:::{math}
:label: eq-spinmagf-10
\muvec={qva\over 2c}{\hat{\mathbf{z}}}.
:::

These imply

:::{math}
:label: eq-spinmagf-11
\muvec={q\over 2mc}\Lvec,
:::

so that in this simple classical model, the magnetic moment and angular momentum are proportional.

They are not proportional in all classical models of mass and charge motion, however. This is easy to see, since the angular momentum depends on the mass distribution and its state of motion, while the magnetic moment depends on the charge distribution and its state of motion. These two do not have to be the same, for example, in a wire the electrons move and the ions are stationary. Thus, in classical mechanics $\Lvec$ and $\muvec$ generally point in different directions. This question is explored in more detail in Prob.~\prbrspinmagf-4.

If we try to apply the classical equation {eq}`eq-spinmagf-11` to the case of an electron, setting $q=-e$ and $m=m_e$ and replacing $\Lvec$ by $\Svec$, we obtain {eq}`eq-spinmagf-8`, except for a factor of 2. Therefore in circumstances in which the angular momentum of a particle (which we call “spin”) is proportional to the magnetic moment, we can write the proportionality between them as

:::{math}
:label: eq-spinmagf-12
\muvec = g {q\over 2mc} \Svec,
:::

where $q$ is the charge of the particle, $m$ its mass and $g$ is the dimensionless, so-called *$g$-factor* of the particle. The $g$-factor is a fudge factor that hides our ignorance of how the magnetic moment is actually generated inside the particle.

For particles such as the electron, proton, neutron and atomic nuclei the magnetic moment is proportional to the spin and nontrivial $g$-factors are required to express the proportionality quantitatively. Thus the question arises as to why these two vectors are proportional in these important cases, whereas classically they are not required to be so. This question cannot be answered at this point in the course but is addressed in Prob. {ref}`prob-wigeck-2`.

{\newsec{{ref}`sec-spinmagf-3`. The Hilbert Space for Spin and Magnetic Moments}

In the case of the silver atom we decided in {ref}`ch-postulat`{} that the Hilbert space upon which the magnetic moment operator acts is 2-dimensional, and that it is spanned by eigenkets of $\mu_z$ that we denoted by $\ket{+}$ and $\ket{-}$:

:::{math}
:label: eq-spinmagf-13
\ES=\mathspan\{\ket{+},\ket{-}\}.
:::

Since $\mu_z$ is proportional to $S_z$ this is actually a standard angular momentum basis, one that we can also write as

:::{math}
:label: eq-spinmagf-14
\{\ket{sm}, m=\pm\frac{1}{2}\},
:::

where $s=\frac{1}{2}$ is the quantum number of the operator $S^2$ which has the eigenvalue $s(s+1)\hbar^2$ (so that $s$ replaces $j$ in the general notation of {ref}`ch-repsamos`). As required by the angular momentum commutation relations, the quantum number $s$ belongs to the set shown in {eq}`eq-repsamos-32`; only the one value $s=\frac{1}{2}$ is needed for this application, and it occurs with multiplicty 1, so the extra index $\gamma$ seen in the general notation $\ket{\gamma jm}$ is not needed (see {ref}`sec-repsamos-10`). The Hilbert space consists of a single irreducible subspace under rotations, with $s=\frac{1}{2}$.

It turns out that for other particles in the same class mentioned previously, including the electron, proton, neutron and atomic nuclei, the Hilbert space upon which the magnetic moment acts is also a single irreducible subspace under rotations whose $s$ value is what we call the *spin* of the particle. The Hilbert space and its standard angular momentum basis are described by

:::{math}
:label: eq-spinmagf-15
\ES=\mathspan\{\ket{sm}, m=-s,\ldots,+s\},
:::

where $s$ is a fixed number belonging to the set {eq}`eq-repsamos-32`, which like the $g$-factor is a characteristic of the particle. Note that $\dim\ES=2s+1$.

Thus another question arises, namely, why does the Hilbert space associated with the magnetic moment of these important particles consist of a single irreducible subspace under rotations? This question also cannot be answered at this point in the course, but the topic is addressed in Secs. {ref}`sec-transfop-9`--{ref}`sec-transfop-12`. It turns out that the answer is related to that of the previous question, why the magnetic moment and angular momentum are proportional.

For the rest of these notes, we will accept that $\muvec$ and $\Svec$ are proportional and related by an equation such as {eq}`eq-spinmagf-12`, and that the Hilbert space is given by {eq}`eq-spinmagf-15`. This is all we need to talk about the spins and $g$-factors of various particles.

(sec-spinmagf-4)=

## Examples of Magnetic Moments and $g$-factors

Let us look at some important examples of spins and magnetic moments. The data is summarized in {ref}`tbl-spinmagf-1`.

:::{list-table} Spins and $g$-factors for various particles and nuclei.
:label: tbl-spinmagf-1
:header-rows: 1

* - Particle
  - charge
  - spin
  - $g$-factor
* - electron
  - $-e$
  - $\frac{1}{2}$
  - $2\times 1.0011\ldots$
* - positron
  - $+e$
  - $\frac{1}{2}$
  - $2\times 1.0011\ldots$
* - proton
  - $+e$
  - $\frac{1}{2}$
  - $5.586\ldots$
* - neutron
  - $0$
  - $\frac{1}{2}$
  - $-3.826\ldots$
* - deuteron
  - $+e$
  - $1$
  - $0.857\ldots$
* - $\alpha$-particle
  - $+2e$
  - $0$
  - 

:::
For the electron, a spin-$\frac{1}{2}$ particle with $q=-e$, the relation {eq}`eq-spinmagf-12` can be written

:::{math}
:label: eq-spinmagf-16
\muvec = -g_e \Bigl( {e\hbar\over 2m_ec}\Bigr) {\Svec\over\hbar},
:::

where $m_e$ and $g_e$ are the electron mass and $g$-factor, and where we have multiplied and divided by $\hbar$ to make the factor $\Svec/\hbar=\sigmavec/2$ dimensionless. The factor $g_e$ is also dimensionless, so the quantity in the parentheses has dimensions of magnetic moment. This is the Bohr magneton, introduced in {eq}`eq-spinmagf-7`. The Bohr magneton is a convenient unit of magnetic moment for electrons or atoms with unpaired electrons.

The electron $g$-factor can be written,

:::{math}
:label: eq-spinmagf-17
g_e = 2\Bigl( 1 + {\alpha\over 2\pi} + \ldots \Bigr) = 2.00232,
:::

where the series indicated is a power series in the fine structure constant,

:::{math}
:label: eq-spinmagf-18
\alpha = {e^2\over \hbar c} \approx {1\over 137}.
:::

This series is the result of a perturbation calculation in quantum electrodynamics, in which the $O(\alpha)$ correction terms and higher are known as *radiative corrections* since physically they come from the interaction of the electron with the quantized electromagnetic and electron-positron fields. The first correction term in this series, shown in {eq}`eq-spinmagf-17`, was calculated by Schwinger in the late 1940's, and was notable as one of the first successful applications of renormalization theory. These correction terms are small, so to a good approximation $g_e \approx 2$. The value $g_e=2$ comes out of the Dirac equation (the equation of the electron in relativistic quantum mechanics, see {ref}`ch-dirac`), so it is known as the Dirac value. For a time in the early days of atomic physics the existence of the small corrections was not known, either experimentally or theoretically, and it was believed that the $g$-factor was exactly 2, as predicted by the Dirac equation. The discovery of the small deviations from the Dirac value led to a theoretical push to understand radiative corrections.

The discovery of radiative corrections has led to a competition between theory and experiment, to see if a discrepancy develops as the $g$-factor is measured and calculated to ever higher precision. The purpose originally was to test QED, and now it has shifted to to a search for new physics, especially physics beyond the standard model. The $g$-factor of the electron and other particles such as the muon are now among the most accurately known physical quantities.

Approximating the $g$-factor by 2, the electron magnetic moment can be written,

:::{math}
:label: eq-spinmagf-19
\muvec = -g_e \mu_B {\sigmavec\over 2} \approx -\mu_B \sigmavec.
:::

The minus sign in this equation means that the electron magnetic moment and angular momentum point in opposite directions.

The positron is the antiparticle of the electron, with the same mass and $g$-factor but opposite charge. Its magnetic moment is therefore given by

:::{math}
:label: eq-spinmagf-20
\muvec = g_e \mu_B {\sigmavec\over 2} \approx \mu_B \sigmavec.
:::

For the proton we have $q=+e$ and $s=\frac{1}{2}$, so

:::{math}
:label: eq-spinmagf-21
\muvec = g_p \Bigl({e\hbar\over 2m_p c}\Bigr) {\Svec\over\hbar},
:::

where the quantity in parentheses is the *nuclear magneton*,

:::{math}
:label: eq-spinmagf-22
\mu_N = {e\hbar\over 2m_p c},
:::

so we can write

:::{math}
:label: eq-spinmagf-23
\muvec = g_p\mu_N {\sigmavec\over2}.
:::

The nuclear magneton is a convenient unit for the magnetic moments of the proton, neutron and other hadrons and various nuclei. It differs from the Bohr magneton by the presence of the proton mass in the denominator instead of the electron mass, and so is about 2000 times smaller than the Bohr magneton. Nuclear magnetic moments, which are of the order of a nuclear magneton, are therefore much smaller than electron magnetic moments, so they make only small corrections to the total magnetic moment of an atom with unpaired electrons. If all the electrons in an atom are paired so that their magnetic moments cancel, then the nuclear magnetic moment is all that remains. The proton $g$-factor $g_p \approx 5.586$ is determined experimentally [see S.~G.~Karshenboim and V.~Ivanov, *Phys. Lett.* B **566**, 27(2003)].

The neutron is electrically neutral, $q=0$, but nevertheless has a nonzero magnetic moment given by

:::{math}
:label: eq-spinmagf-24
\muvec = g_n \mu_N {\Svec\over\hbar} = g_n \mu_N {\sigmavec\over 2},
:::

where $g_n \approx -3.823$. The neutron is considered to have a negative $g$-factor, because $\muvec$ and $\Svec$ are in opposite directions. The usual electronic charge $e$ is used in $\mu_N$, even though the neutron is neutral; and by convention, the proton mass is used in $\mu_N$, even in the neutron equation {eq}`eq-spinmagf-24`. Crude models of mixtures of up and down quarks are able to explain the proton and neutron magnetic moments to within several percent, but it is very difficult to improve on these calculations. The difficulty is the usual one in hadron physics, where the strong interactions usually preclude a perturbative treatment.

The proton and neutron $g$-factors are sometimes said to be *anomalous*, because they differ from the Dirac value of 2. Of course, so does the electron $g$-factor, if we include the radiative corrections.

Nuclei have a variety of spins and magnetic moments. For the deuteron, a spin-one particle, we have

:::{math}
:label: eq-spinmagf-25
\muvec = g_d \mu_N {\Svec\over\hbar},
:::

where $g_d \approx 0.857$. Notice that $\Svec/\hbar$ is the vector of $3\times3$ matrices for spin 1, not the Pauli matrices (see {eq}`eq-repsamos-52` and {eq}`eq-repsamos-53`).

The magnetic moment of the deuteron can be considered as due to the magnetic moments of the constituent proton and neutron, plus some contribution due to the orbital motion of the proton. See Prob. {ref}`prob-zeeman-6`. Plugging in the actual numbers gives information about the deuteron wave function, that is, the wave function of the two particle system consisting of proton and neutron. More information about this wave function comes from scattering experiments, the measured electric quadrupole moment of the deuteron, and other sources. It turns out that the interaction between the proton and neutron is not governed by a purely central force potential, but rather there are strong spin-dependent forces as well. As a result, the spatial part of the wave function is not a pure eigenstate of orbital angular momentum, but rather consists of a linear combination of an $s$-wave and a $d$-wave (with $\ell=0$ and $\ell=2$). The deuteron has spin 1 because the energy of the proton-neutron system is minimized when the spins are aligned. When the spins are opposite, the proton-neutron system has no bound state. In fact, deuteron has no bound excited states (there is only one bound state, the ground state).

For the $\alpha$-particle, a spin-0 particle, we have $\muvec=0$ exactly. Spin-0 particles cannot have a magnetic moment, because the spin operator vanishes [see {eq}`eq-repsamos-55`].

(sec-spinmagf-5)=

## Hamiltonian for a Spin in a Magnetic Field

The force on a magnetic dipole {eq}`eq-spinmagf-2` can be written as $\Fvec=-\del V$, where

:::{math}
:label: eq-spinmagf-26
V(\xvec)=-\muvec\cdot\Bvec(\xvec),
:::

that is, the quantity $-\muvec\cdot\Bvec$ behaves as a potential energy, insofar as the total force on the dipole is concerned. Moreover, this quantity is also the energy of orientation of the magnetic dipole in an external magnetic field, as is shown in books on electromagnetism. Therefore it is a good guess that the Hamiltonian describing the motion of a neutral magnetic dipole in a magnetic field should be

:::{math}
:label: eq-spinmagf-27
H={\pvec^2\over 2m}-\muvec\cdot\Bvec(\xvec).
:::

If this is interpreted as a classical Hamiltonian, then by Hamilton's equations it gives {eq}`eq-spinmagf-4` for the acceleration of the dipole.

If the Hamiltonian {eq}`eq-spinmagf-27` is interpreted as a quantum Hamiltonian, then it can be shown that it explains the splitting of the beam in a Stern-Gerlach apparatus. This requires techniques from adiabatic theory (see {ref}`ch-adiab`), which we will not go into here.

For the rest of these notes we will restrict consideration to problems in which the magnetic field is uniform in space, so there is no coupling to the spatial degrees of freedom. This is often a good approximation in practice, since laboratory magnetic fields are usually quite uniform on the atomic scale. We will, however, allow the magnetic field to be a function of time, $\Bvec = \Bvec(t)$, because this in fact is the principal means by which spins are controlled experimentally.

As a result, we can ignore the spatial degrees of freedom and take the Hamiltonian to be

:::{math}
:label: eq-spinmagf-28
H= -\muvec\cdot\Bvec = \gamma \Bvec \cdot \Svec,
:::

where

:::{math}
:label: eq-spinmagf-29
\gamma = -g {q\over 2mc}.
:::

To be specific, in the rest of these notes we will assume $\gamma>0$ (as it would be for an electron), but if $\gamma<0$ then directions of precession and various other conclusions must be reversed.

(sec-spinmagf-6)=

## The Time Evolution is a Rotation

Consider first the general problem in which the magnetic field has an arbitrary time dependence, $\Bvec=\Bvec(t)$. We denote the unitary time evolution operator by $W(t,t_0)$, reserving the symbol $U$ for rotation operators, as in {ref}`ch-repsamos`. The Schr\"odinger equation for $W$ is {eq}`eq-tevolut-13`, which in the present case is

:::{math}
:label: eq-spinmagf-30
i\hbar\frac{\partial W(t,t_0)}{\partial t} = \gamma[\Bvec(t)\cdot\Svec] W(t,t_0).
:::

If nothing further is said about the time dependence of $\Bvec$, we cannot write down the solution in explicit form, but we can at least note that the time-evolution operator $W$ is always a rotation operator. To see this, we consider the infinitesimal time advance implied by the Schr\"odinger equation,

:::{math}
:label: eq-spinmagf-31
W(t+\Delta t,t_0) = \Bigl[ 1 -{i\gamma\Delta t\over\hbar} \Bvec(t)\cdot\Svec\Bigr] W(t,t_0).
:::

The factor in the square brackets is an infinitesimal rotation operator, as we can see if we compare it to

:::{math}
:label: eq-spinmagf-32
U({\hat{\mathbf{n}}},\Delta\theta) =1 - {i\Delta\theta\over\hbar} {\hat{\mathbf{n}}}\cdot\Svec,
:::

valid when $\Delta\theta\ll 1$. We see that the axis of the infinitesimal rotation is given by

:::{math}
:label: eq-spinmagf-33
{\hat{\mathbf{n}}} = {\hat{\mathbf{b}}}(t),
:::

where we write

:::{math}
:label: eq-spinmagf-34
\Bvec(t) = B(t) {\hat{\mathbf{b}}}(t)
:::

for the magnitude and direction of the magnetic field. The angle of the infinitesimal rotation is given by

:::{math}
:label: eq-spinmagf-35
\Delta \theta = \gamma B(t) \Delta t,
:::

or,

:::{math}
:label: eq-spinmagf-36
\omega =  {\Delta\theta\over\Delta t} = \gamma B(t).
:::

The angular velocity can also be written as a vector,

:::{math}
:label: eq-spinmagf-37
\omegavec = \omega{\hat{\mathbf{n}}}= \gamma \Bvec(t),
:::

which is parallel to $\Bvec$ (antiparallel, if $\gamma<0$).

We see that as time proceeds, $W$ develops by the composition of a large number of infinitesimal rotation operators; since the product of rotation operators is always a rotation operator, $W$ itself is a rotation operator. However, the axis and rate of rotation are in general functions of time. This is very much as in classical rigid body motion, in which $\omegavec$ is some function of time, which in general is not constant either in magnitude or direction. In classical rigid body motion, $\omegavec$ is determined as a function of time by solving the Euler equations; in the quantum mechanical motion of a charged particle in a magnetic field, $\omegavec$ is simply given as a function of time by {eq}`eq-spinmagf-37`. In either case, once $\omegavec(t)$ is known, the subsequent problem of determining the time-dependent rotation is very similar.

(sec-spinmagf-7)=

## Constant Magnetic Field

We turn now to some cases in which {eq}`eq-spinmagf-30` can be solved explicitly. The simplest one is that of a spin in a constant magnetic field,

:::{math}
:label: eq-spinmagf-38
\Bvec = B {\hat{\mathbf{b}}} = const.
:::

The Hamiltonian is now time-independent, so $W$ only depends on the elapsed time $t$. We borrow notation from \secrspinmagf-6, writing,

:::{math}
:label: eq-spinmagf-39
\omegavec=\gamma\Bvec = \omega {\hat{\mathbf{b}}},
:::

and

:::{math}
:label: eq-spinmagf-40
\omega = \gamma B,
:::

where now $\omegavec$ and its magnitude $\omega$ are time-independent. Thus the Schr\"odinger equation for $W$ is

:::{math}
:label: eq-spinmagf-41
i\hbar \frac{\partial W(t)}{\partial t} = (\omegavec\cdot\Svec) W(t).
:::

This can be immediately integrated, giving

:::{math}
:label: eq-spinmagf-42
W(t) = \exp\Bigl[ -{i\over\hbar} (\omegavec \cdot \Svec) t \Bigr] = U({\hat{\mathbf{b}}}, \omega t).
:::

The time evolution consists of a rotation about the axis ${\hat{\mathbf{b}}}$ with frequency $\omega$.

In the case of the electron, the frequency of spin precession is

:::{math}
:label: eq-spinmagf-43
\omega = {g_e \over 2} {eB \over mc},
:::

which, in the approximation $g_e \approx 2$, is equal to the nonrelativistic frequency of orbital motion of the electron in the uniform magnetic field (the gyrofrequency, see {ref}`ch-magfield`). Certain so-called $g-2$ experiments exploit this near equality to measure the small difference between the two frequencies, which provides a direct measurement of the radiative corrections in {eq}`eq-spinmagf-17`.

:::{figure} images/spinmagf-fig01.png
:label: fig-spinmagf-1
:width: 80%

In a constant magnetic field, $\xpecval{\Svec}$ precesses about the field direction at frequency $\omega = \gamma B$.
:::

:::{figure} images/spinmagf-fig02.png
:label: fig-spinmagf-2
:width: 80%

The field in magnetic resonance experiments consists of a constant field $\Bvec_0$ plus a time-dependent field $\Bvec_1(t)$ that is perpendicular to $\Bvec_0$ and that rotates about $\Bvec_0$ at frequency $\omega_1$.
:::


Given $W(t)$, it is straightforward to find the time evolution of the expectation value of the spin. We have

:::{math}
\begin{aligned}
\xpecval{\Svec}(t) &= \matrixelement{\psi(t)}{\Svec}{\psi(t)} =\matrixelement{\psi_0}{U({\hat{\mathbf{b}}},\omega t)^\hc \Svec U({\hat{\mathbf{b}}},\omega t)}{\psi_0}
\end{aligned}
:::

:::{math}
:label: eq-spinmagf-44
\begin{aligned}
&=\Rmat({\hat{\mathbf{b}}},\omega t) \matrixelement{\psi_0}{\Svec}{\psi_0} = \Rmat({\hat{\mathbf{b}}},\omega t) \xpecval{\Svec}(0),
\end{aligned}
:::

where we have used the adjoint formula {eq}`eq-repsamos-91`. We see that the expectation value of $\Svec$ rotates counterclockwise (for $\gamma>0$) about the direction of the magnetic field, sweeping out a cone. This is illustrated in {ref}`fig-spinmagf-1`.

(sec-spinmagf-8)=

## Magnetic Resonance Experiments

A more interesting case occurs in magnetic resonance experiments. Here the magnetic field consists of a constant, background field $\Bvec_0 = B_0 {\hat{\mathbf{b}}}_0$, plus a time-dependent $\Bvec_1(t)$ that is perpendicular to $\Bvec_0$ and oscillating with some frequency $\omega_1$. In the absence of $\Bvec_1$, the spin would evolve according to a time-dependent rotation with angular velocity,

:::{math}
:label: eq-spinmagf-45
\omegavec_0 = \omega_0 {\hat{\mathbf{b}}}_0,
:::

whose magnitude is

:::{math}
:label: eq-spinmagf-46
\omega_0 = \gamma B_0.
:::

The time-dependent field $\Bvec_1(t)$ is used to induce spin flips. To do this its magnitude need not be large, but its frequency $\omega_1$ should be at or near resonance with the precession frequency $\omega_0$ in the background field. Thus, the interesting case is $|\Bvec_1| \ll B_0$ and $\omega_1 \approx \omega_0$. Notice that $\omega_0$ is determined by the magnitude of the background field $\Bvec_0$, but $\omega_1$ is the frequency of the time-dependence of $\Bvec_1(t)$, and is independent of its magnitude.

We will consider the case that $\Bvec_1(t)$ rotates in a counterclockwise direction (clockwise, if $\gamma<0$) at frequency $\omega_1$ in the plane perpendicular to $\Bvec_0$, as illustrated in {ref}`fig-spinmagf-2`. This case has the advantage that the Schr\"odinger equation can be solved exactly in terms of rotation operators. We assume the magnitude of $\Bvec_1$ is constant, so the vector $\Bvec_1(t)$ traces out a circle in the perpendicular plane. The time-dependence of $\Bvec_1$ can be expressed in terms of a classical rotation about the axis ${\hat{\mathbf{b}}}_0$,

:::{math}
:label: eq-spinmagf-47
\Bvec_1(t) = \Rmat_1(t) \Bvec_{10},
:::

where $\Bvec_{10}$ is a constant vector (the initial value of $\Bvec_1(t)$) perpendicular to $\Bvec_0$, and where

:::{math}
:label: eq-spinmagf-48
\Rmat_1(t) = \Rmat({\hat{\mathbf{b}}}_0,\omega_1 t).
:::

Another possibility for the time-dependence of $\Bvec_1$ will be mentioned below.

The Schr\"odinger equation can now be written,

:::{math}
:label: eq-spinmagf-49
i\hbar \pop{\ket{\psi(t)}}{t} = \gamma \{[\Bvec_0 + \Rmat_1(t)\Bvec_{10}]\cdot\Svec\} \ket{\psi(t)}.
:::

We solve this by effectively going over to a frame rotating with frequency $\omega_1$ about the axis $\bvec_0$. This cancels out the rotation of the field $\Bvec_1(t)$, giving a constant magnetic field $\Bvec_0+\Bvec_{10}$ in the rotating frame. However, as is well known, Coriolis effects in a rotating frame reproduce the effects of a magnetic field, and can be used to enhance or cancel out the effects of a true magnetic field. In the present case, in the rotating frame the effects of $\Bvec_0$ are partially or totally cancelled, resulting in an effective magnetic field $\Bvec_eff$ that is the sum of a reduced magnetic field in the direction ${\hat{\mathbf{b}}}_0$ plus the constant field $\Bvec_{10}$ in the perpendicular direction.

We obtain the effect of going to a rotating frame by stripping off the time dependence

:::{math}
:label: eq-spinmagf-50
U_1(t) = U({\hat{\mathbf{b}}}_0,\omega_1t)
:::

from the state vector $\ket{\psi(t)}$, that is, by setting

:::{math}
:label: eq-spinmagf-51
\ket{\psi(t)} = U_1(t) \ket{\phi(t)},
:::

where $\ket{\phi(t)}$ is a new state vector. Notice that $U_1(t)$ has the same axis and angle as $R_1(t)$, defined in {eq}`eq-spinmagf-48`. Differentiating {eq}`eq-spinmagf-51`, we obtain

:::{math}
:label: eq-spinmagf-52
i\hbar\pop{\ket{\psi(t)}}{t} = U_1 \Bigl[ \omega_1 ({\hat{\mathbf{b}}}_0\cdot\Svec) + i\hbar\pop{}{t}\Bigr] \ket{\phi(t)}.
:::

On the other hand, with the substitution {eq}`eq-spinmagf-51` the Schr\"odinger equation {eq}`eq-spinmagf-49` becomes

:::{math}
:label: eq-spinmagf-53
i\hbar \pop{\ket{\psi(t)}}{t} = \gamma [(\Bvec_0 + \Rmat_1\Bvec_{10})\cdot\Svec] U_1 \ket{\phi(t)}.
:::

Now we equate the right hand sides of {eq}`eq-spinmagf-52` and {eq}`eq-spinmagf-53` and multiply through by $U_1^\dagger$, to obtain

:::{math}
:label: eq-spinmagf-54
\omega_1({\hat{\mathbf{b}}}_0\cdot\Svec)\ket{\phi(t)} + i\hbar\pop{}{t}\ket{\phi(t)} = \gamma(\Bvec_0 + \Rmat_1\Bvec_{10})\cdot (U_1^\dagger \Svec U_1) \ket{\phi(t)}.
:::

Here we have pulled the $U_1^\dagger$ through the constant $\gamma$, the vectors $\Bvec_0$ and $\Bvec_{10}$ and the matrix $\Rmat_1$, because these are just numbers or matrices and vectors composed of numbers, while $U_1^\dagger$, $\Svec$ and $U_1$ are operators that act on kets. Now we use the adjoint formula {eq}`eq-repsamos-91`, with $\Jvec$ replaced by $\Svec$, $U$ replaced by $U_1^\dagger$, and $\Rmat$ replaced by $\Rmat_1^{-1}$. This gives

:::{math}
:label: eq-spinmagf-55
U_1^\dagger \Svec U_1 = \Rmat_1\Svec,
:::

so the dot product on the right hand side of {eq}`eq-spinmagf-54` becomes

:::{math}
:label: eq-spinmagf-56
(\Bvec_0 + \Rmat_1\Bvec_{10})\cdot(\Rmat_1\Svec)= [\Rmat_1^{-1}(\Bvec_0 + \Rmat_1\Bvec_{10})]\cdot\Svec = (\Bvec_0+\Bvec_{10})\cdot\Svec,
:::

where we use {eq}`eq-classrot-72`, which expresses the invariance of the dot product under rotations. Also note that $\Rmat_1^{-1}\Bvec_0=\Bvec_0$, since $\Bvec_0$ is the axis of $\Rmat_1$. Thus {eq}`eq-spinmagf-54` becomes

:::{math}
:label: eq-spinmagf-57
\omega_1({\hat{\mathbf{b}}}_0\cdot\Svec)\ket{\phi(t)} + i\hbar\pop{}{t}\ket{\phi(t)} = \gamma(\Bvec_0+\Bvec_{10})\cdot\Svec \ket{\phi(t)}, =(\omega_0{\hat{\mathbf{b}}}_0 + \gamma\Bvec_{10})\cdot \Svec \ket{\phi(t)}.
:::

Rearranging this, we can write the effective Schr\"odinger equation for $\ket{\phi(t)}$ in the form

:::{math}
:label: eq-spinmagf-58
i\hbar \pop{\ket{\phi(t)}}{t} = \{[(\omega_0-\omega_1){\hat{\mathbf{b}}}_0 + \gamma\Bvec_{10}] \cdot\Svec\} \ket{\phi(t)} = \gamma (\Bvec_eff \cdot \Svec) \ket{\phi(t)},
:::

where

:::{math}
:label: eq-spinmagf-59
\gamma \Bvec_eff = (\omega_0-\omega_1){\hat{\mathbf{b}}}_0 + \gamma \Bvec_{10},
:::

or,

:::{math}
:label: eq-spinmagf-60
\Bvec_eff = \Bigl(B_0 - {\omega_1 \over \gamma}\Bigr) {\hat{\mathbf{b}}}_0 + \Bvec_{10}.
:::

This is the effective magnetic field in the rotating frame. We break it up into its magnitude and direction,

:::{math}
:label: eq-spinmagf-61
\Bvec_eff = B_eff {\hat{\mathbf{b}}}_eff,
:::

so that

:::{math}
:label: eq-spinmagf-62
B_eff = \sqrt{\displaystyle \Bigl( B_0 -{\displaystyle \omega_1 \over \displaystyle \gamma} \Bigr)^2 + B_{10}^2 }.
:::

We also define

:::{math}
:label: eq-spinmagf-63
\Omega=\gamma B_eff = \sqrt{(\omega_0-\omega_1)^2 + \gamma^2 B_{10}^2},
:::

called the *Rabi flopping frequency*. Notice that if $B_{10} \ll B_0$ and $\omega_1 \approx \omega_0$, then $\Omega \ll \omega_0$ (the flopping frequency is much less than the precession frequency). We will also denote the angle between ${\hat{\mathbf{b}}}_0$ and ${\hat{\mathbf{b}}}_eff$ by $\theta$, so that

:::{math}
:label: eq-spinmagf-64
\sin\theta = {B_{10} \over B_eff},
:::

as illustrated in {ref}`fig-spinmagf-3`.

:::{figure} images/spinmagf-fig03.png
:label: fig-spinmagf-3
:width: 80%

In the rotating frame, the field $\Bvec_1=\Bvec_{10}$ is stationary, and $\Bvec_0$ is reduced in magnitude by $\omega_1/\gamma$. The resulting field is $\Bvec_eff$, which is constant in the rotating frame.
:::

:::{figure} images/spinmagf-fig04.png
:label: fig-spinmagf-4
:width: 80%

The expectation value of the spin $\Svec$ precesses about the axis ${\hat{\mathbf{a}}}(t)$ with frequency $\Omega$, while that axis itself precesses about $\Bvec_0$ with frequency $\omega_1$.
:::


The Schr\"odinger equation for $\ket{\phi(t)}$, {eq}`eq-spinmagf-58`, is the case of a spin in a constant magnetic field, so the solution is

:::{math}
:label: eq-spinmagf-65
\ket{\phi(t)} = U({\hat{\mathbf{b}}}_eff,\Omega t) \ket{\phi(0)}.
:::

Combining this with {eq}`eq-spinmagf-51`, we obtain the time evolution operator for the original Schr\"odinger equation {eq}`eq-spinmagf-49`,

:::{math}
:label: eq-spinmagf-66
W(t) = U({\hat{\mathbf{b}}}_0,\omega_1 t) U({\hat{\mathbf{b}}}_eff, \Omega t).
:::

As before, we can use the solution {eq}`eq-spinmagf-66` to find the evolution of the expectation value of the spin. We find,

:::{math}
:label: eq-spinmagf-67
\xpecval{\Svec}(t) = \Rmat({\hat{\mathbf{b}}}_0, \omega_1t) \Rmat({\hat{\mathbf{b}}}_eff, \Omega t) \xpecval{\Svec}(0).
:::

Thus, $\xpecval{\Svec}$ sweeps out a cone at frequency $\Omega$ about an axis ${\hat{\mathbf{a}}}$ that makes an angle $\theta$ with the direction ${\hat{\mathbf{b}}}_0$, while this axis itself sweeps out a cone about ${\hat{\mathbf{b}}}_0$ at frequency $\omega_1$. This is illustrated in {ref}`fig-spinmagf-4`. The direction ${\hat{\mathbf{b}}}_eff$ is the initial direction of the axis at $t=0$, so that

:::{math}
:label: eq-spinmagf-68
{\hat{\mathbf{a}}}(t) = \Rmat({\hat{\mathbf{b}}}_0, \omega_1 t) {\hat{\mathbf{b}}}_eff.
:::

{eq}`eq-spinmagf-67` can be expressed explicitly in terms of the time-dependent axis ${\hat{\mathbf{a}}}(t)$ by use of the exponentiated adjoint formula, {eq}`eq-classrot-51`:

:::{math}
:label: eq-spinmagf-69
\xpecval{\Svec}(t) = \Rmat\bigl( {\hat{\mathbf{a}}}(t), \Omega t \bigr) \Rmat({\hat{\mathbf{b}}}_0, \omega_1 t) \xpecval{\Svec}(0),
:::

which provides another way of visualizing the time evolution of $\xpecval{\Svec}$.

We remark that in practice it is easier to use a different time-dependent field $\Bvec_1$, given by

:::{math}
:label: eq-spinmagf-70
\Bvec_1(t) = 2B_{10}{\hat{\mathbf{x}}} \cos\omega_1t,
:::

where we put $\Bvec_0$ along the $z$-axis. This field is the sum of two counter-rotating fields,

:::{math}
\begin{aligned}
\Bvec_1(t) &= B_{10}({\hat{\mathbf{x}}} \cos\omega_1t + {\hat{\mathbf{y}}} \sin\omega_1t)
\end{aligned}
:::

:::{math}
:label: eq-spinmagf-71
\begin{aligned}
&+ B_{10}({\hat{\mathbf{x}}} \cos\omega_1t - {\hat{\mathbf{y}}} \sin\omega_1t),
\end{aligned}
:::

so that if we go into the rotating frame as above then one of these fields becomes constant while the other is rotating in the opposite direction at a frequency $2\omega_1$. This is much higher than $\Omega$ under the conditions we have posited, so the oppositely rotating field causes only small changes in the solution we have given. High frequency perturbations generally have only a small effect on a system because before the effect has a chance to build up, the perturbation changes sign and starts working in the opposite direction.

(sec-spinmagf-9)=

## A Sample Calculation

Suppose we have a spin-$\frac{1}{2}$ particle, initially in an up state, $\ket{\psi_0}= \ket{+}$, and suppose we ask for the probability at a later time of finding the spin in the down state $\ket{-}$. We take the direction $\Bvec_0$ to lie along the $z$-axis, and we place the vectors $\Bvec_{10}$ and ${\hat{\mathbf{b}}}_eff$ in the $x$-$z$ plane. To compute the probability amplitude for the $\frac{1}{2} \to -\frac{1}{2}$ transition, we use {eq}`eq-spinmagf-66` to obtain

:::{math}
:label: eq-spinmagf-72
\matrixelement{-}{W(t)}{+} =\matrixelement{-}{U({\hat{\mathbf{z}}},\omega_1t)U({\hat{\mathbf{b}}}_eff, \Omega t)}{+} =e^{i\omega_1t/2} \, \matrixelement{-}{U({\hat{\mathbf{b}}}_eff, \Omega t)}{+}.
:::

But since

:::{math}
:label: eq-spinmagf-73
{\hat{\mathbf{b}}}_eff = {\hat{\mathbf{z}}} \cos\theta + {\hat{\mathbf{x}}} \sin \theta,
:::

we have

:::{math}
:label: eq-spinmagf-74
\matrixelement{-}{W(t)}{+} = -i e^{i\omega_1 t/2} \, \sin\theta \sin{\Omega t\over 2}.
:::

Thus, the transition probability is

:::{math}
:label: eq-spinmagf-75
P_{\ffract1/2 \to -\ffract1/2} = \sin^2 \theta \sin^2 {\Omega t\over 2}.
:::

In the resonant case, $\omega_1=\omega_0$, we have $B_eff = B_{10}$ and $\theta=\pi/2$, so that the axis of the rotating cone lies in the $x$-$y$ plane. In this case, the transition probability {eq}`eq-spinmagf-75` reaches a maximum value of unity when $t = \pi/\Omega$.

\problems

(prob-spinmagf-1)=

**Problem \prbdspinmagf-1..** 

:::{math}
:label: eq-spinmagf-76
\Bvec= B_0 {\hat{\mathbf{z}}} + B_{10}({\hat{\mathbf{x}}} \cos\omega_1 t + {\hat{\mathbf{y}}} \sin\omega_1 t),
:::

employed in magnetic resonance experiments (assume $\gamma>0$). If at $t=0$, the particle is in state $m=0$, find the transition probabilities $P(0\to\pm1)$ as a function of time.

(prob-spinmagf-2)=

**Problem \prbdspinmagf-2..** 

:::{math}
:label: eq-spinmagf-77
\ket{\psi(t)} = U(\alpha,\beta,\gamma)\ket{\psi(0)},
:::

where $U$ is a rotation operator that depends on Euler angles $(\alpha,\beta,\gamma)$, and where the Euler angles are functions of time. Therefore the Schr\"odinger equation for $\ket{\psi(t)}$ must imply equations of evolution for the Euler angles.

Let $\omegavec(t)$ be defined by

:::{math}
:label: eq-spinmagf-78
\omegavec(t)\cdot\Svec = -\muvec\cdot\Bvec(t).
:::

Find equations of motion for the Euler angles, assuming $\omegavec(t)$ is given. Your answer will be identical to the equations of motion of the Euler angles in classical rigid body theory (for given $\omegavec(t)$).

(prob-spinmagf-3)=

**Problem \prbdspinmagf-3..** 

\problempart{(a)} A spin in a bulk sample is only partially aligned with a background magnetic field, because thermal agitation is always disrupting the alignment. The partial alignment of a spin in a magnetic field is a standard problem in statistical mechanics. The alignment can be increased by going to lower temperatures, but this is obviously not feasible in medical imaging.

Consider a biological sample at 300K in a magnetic field of 6T (for example, you in an MRI device). After a certain relaxation time, the nuclear spins will reach thermal equilibrium with their environment (a heat bath). Calculate the fractional magnetization of protons under such circumstances (the magnetization compared to the maximum we would have at 0K). Finally, for a sample of water under the conditions indicated, compute the magnetization due to protons in Gauss. The magnetization is the magnetic dipole moment per unit volume.

\problempart{(b)} Compute the spin precession frequency of protons in a field of 6T. Express your answer in Hz.

\problempart{(c)} An RF electromagnetic wave is used to create the rotating magnetic field $\Bvec_1$ [see {eq}`eq-spinmagf-47`.] If the power flux of the wave is $1KW/m^2$, what is the Rabi flopping frequency $\Omega$ when the wave is in resonance with the precession? Express your answer in Hertz. Remember that we do not want to cook the patient.

(prob-spinmagf-4)=

**Problem \prbdspinmagf-4..** 

Consider a system of classical charged particles of masses $m_i$ and charges $q_i$, $i=1,\ldots,N$. Let the positions and velocities of the particles be $\rvec_i$ and $\vvec_i$. We assume the classical Hamiltonian is invariant under rotations, so the total classical angular momentum,

:::{math}
:label: eq-spinmagf-79
\Lvec=\sum_i \Lvec_i = \sum_i m_i \,\rvec_i \cross \vvec_i,
:::

is conserved. The current produced by particle $i$ at position $\xvec$ is

:::{math}
:label: eq-spinmagf-80
\Jvec_i(\xvec,t) = q_i \vvec_i \,\delta^3\bigl(\xvec-\rvec_i(t) \bigr).
:::

Compute the magnetic moment $\muvec$ according to {eq}`eq-spinmagf-1` and show that if all the particles are identical, then $\muvec$ and $\Lvec$ are proportional. What is the constant of proportionality?

This calculation applies to a classical model of an atom with an infinitely heavy nucleus because all the electrons have the same mass and charge. The nucleus does not have the same mass and charge as the electrons, but in the limit that its mass is infinite its velocity is zero so it does not contribute to either the angular momentum or the magnetic moment and the result still holds.

A similar calculation in quantum mechanics shows that the orbital contribution to the magnetic moment of atoms, including multielectron atoms, is proportional to the orbital angular momentum with the same proportionality factor as in the classical calculation, that is, with a $g$-factor of 1.

This calculation does not apply to a classical model of a compound nucleus, because the protons and neutrons do not have the same charge (and, to a lesser extent, because their masses are not exactly equal). In any case, in both atoms and nuclei, we must take into account the spins of the particles, as well as the orbital angular momentum, in a realistic, quantum mechanical accounting of the magnetic moment.

In general, the classical magnetic momennt is not proportional to the angular momentum; and the quantum mechanical magnetic moment operator is not proportional to the quantum mechanical angular momentum operator. This applies to the orbital contribution, the spin contribution, and to the total. Nevertheless, it turns out that in weak magnetic fields, the effective quantum mechanical magnetic moment and the total angular momentum are proportional, with some effective $g$-factor, on the energy eigenspaces of typical quantum systems. This fact will be explained in {ref}`sec-zeeman-8`.
