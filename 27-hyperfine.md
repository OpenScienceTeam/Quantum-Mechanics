---
title: "27. Hyperfine Structure in Atoms"
---
(ch-hyperfine)=

# 27. Hyperfine Structure in Atoms

(sec-hyperfine-1)=

## Introduction

The nucleus of an atom contains localized charge and current distributions, which produce electric and magnetic fields that can be decomposed into multipole fields much as in classical electrostatics or magnetostatics. The first of the multipole moments, the electric monopole, is the Coulomb electrostatic field that holds the electrons in their orbits and produces the gross structure of the atom. The higher order multipole moments produce small corrections to the atomic structure that are known generally as hyperfine effects.

The terminology “hyperfine” refers to the energy scale of these effects, which is smaller than that of the fine structure. The physics, however, of hyperfine effects is completely different from that of fine structure. In practice, the most important hyperfine effects are those due to the magnetic dipole and electric quadrupole fields of the nucleus. Higher multipole moments of the nucleus are important in nuclear physics, but not usually in atomic physics.

In these notes we will study hyperfine effects in atoms, concentrating mainly on the magnetic dipole field in the case of ordinary hydrogen. As we shall see, hyperfine effects couple the dynamics of the atomic electron to that of the nucleus, thereby enlarging the Hilbert space, introducing new quantum numbers, and shifting and splitting the energy levels.

In spite of the small energy scales involved, hyperfine effects are quite important in applications ranging from atomic physics to astrophysics. For example, the radiative transition between the two hyperfine levels of the ground state of the hydrogen atom produces the 21 centimeter line that plays an important role in radio astronomy.

For another example, atomic clocks often use as their basic oscillator a hyperfine transition in the ground state of the heavy alkali atoms, rubidium or cesium. The reproducibility of the frequency of these transitions is so great that the second is now defined as 9,192,631,770 periods of the photon emitted in the hyperfine transition of the ${}^{133}Cs$ atom, exactly. Atomic clocks based on cesium hyperfine transitions currently have a precision of the order of one part in $10^{15}$. More recently “optical clocks” have been invented that use transitions in the optical range of frequencies. Some of these have precisions approaching one part in $10^{18}$.

The GPS (global positioning system) relies on radio timing signals emitted by satellites in high earth orbit containing atomic clocks. In order to achieve the desired precision of position measurements on the earth it is necessary to take into account the effects of both special and general relativity in analyzing the timing signals. Special relativity enters because of the time dilation of the clocks moving in their orbits, and general relativity because of the difference in the gravitational potential between the clock in orbit and the receiver on the surface of the earth (this is the gravitational red shift).

(sec-hyperfine-2)=

## Multipoles in Electrostatics and Magnetostatics

In classical electrostatics, a localized charge distribution $\rho$ produces a potential $\Phi$ that at field points outside the charge distribution can be expanded into multipoles,

:::{math}
:label: eq-hyperfine-1
\Phi(\rvec) = {q\over r} + {\dvec\cdot\rvec\over r^3} + {1\over 6} \sum_{ij} {Q_{ij}\,T_{ij}\over r^5} + \ldots,
:::

where $q$ is the total charge of the distribution, $\dvec$ is its dipole moment vector and $Q_{ij}$ is its quadrupole moment tensor, and where the tensor $T_{ij}$ is defined by

:::{math}
:label: eq-hyperfine-2
T_{ij}=3x_ix_j-r^2\,\delta_{ij}.
:::

See {ref}`fig-hyperfine-1`. The terms of the series {eq}`eq-hyperfine-1` are the monopole, dipole and quadrupole terms, in that order. See {ref}`sec-orbamsph-11` for more details on the electrostatic multipole expansion.

Similarly, a localized, steady current distribution $\Jvec$ produces a vector potential that can be expanded into multipoles,

:::{math}
:label: eq-hyperfine-3
\Avec(\rvec) = {\muvec\cross\rvec\over r^3} + \ldots,
:::

where it is assumed that magnetic monopoles do not exist so there is no monopole term, where the dipole term with magnetic dipole moment $\muvec$ is shown, and where higher order terms not shown include the magnetic quadrupole term etc. Each term of the multipole expansion falls off as one higher power of $r$ than the previous term. The multipole expansion of the electric and magnetic fields is obtained by computing $\Evec=-\del\Phi$ and $\Bvec=\del\cross\Avec$.

:::{figure} images/hyperfine-fig01.png
:label: fig-hyperfine-1
:width: 80%

The origin of coordinates is placed inside a region to which a charge distribution $\rho$ and current distribution $\Jvec$ are confined. The field point $\rvec$ is outside the charge and current distributions.
:::

The quantities $q$, $\dvec$, $Q_{ij}$ and $\muvec$ that appear in the multipole expansions are moments of the charge and current distributions,

:::{math}
:label: eq-hyperfine-4
\begin{aligned}
q&=\int d^3\rvec \, \rho(\rvec), \qquad \dvec = \int d^3\rvec \, \rho(\rvec) \, \rvec, \\
Q_{ij} &= \int d^3\rvec \, \rho(\rvec) \,(3x_ix_j -r^2\,\delta_{ij}), \qquad \muvec = {1\over 2c} \int d^3\rvec \, \rvec \cross\Jvec(\rvec), \\

\end{aligned}
:::

The dipole moment vector $\dvec$ is the charge-weighted position vector, and the quadrupole moment tensor $Q_{ij}$ is the charge-weighted tensor $T_{ij}$. The tensors $T_{ij}$ and $Q_{ij}$ are symmetric and traceless, and thus contain five independent components. These moments characterize the source distribution but are independent of position.

The nomenclature of the multipoles is explained in {ref}`tbl-hyperfine-1`. Each pole is associated with an integer $k=0,1,2,\ldots$, and the name contains a Latin or Greek prefix indicating the number $2^k$. We shall refer to them in general as $2^k$-poles.

:::{list-table} The names of the multipoles are obtained by using Latin or Greek prefixes indicating a power of 2.
:label: tbl-hyperfine-1
:header-rows: 2

* - Pole
  - Numbers
  - 
* - Monopole
  - $1=2^0$
  - 
* - Dipole
  - $2=2^1$
  - 
* - Quadrupole
  - $4=2^2$
  - 
* - Octupole
  - $8=2^3$
  - 

:::
(sec-hyperfine-3)=

## About Nuclei and Nuclear Multipole Moments

We denote the spin of the nucleus by $\Ivec$, reserving the symbol $\Svec$ for the electron spin. We let the quantum number of the operator $I^2$ be $i$, so that $I^2$ has eigenvalues $i(i+1)\hbar^2$. We denote the nuclear Hilbert space by $\ES_nucl$, a $(2i+1)$-dimensional space in which the standard basis is $\{ \ket{im_i}, m_i=-i, \ldots, +i\}$. The nuclear Hilbert space consists of a single irreducible subspace under rotations. In actual stable nuclei, the spin ranges from $i=0$ to $i=15/2$. For example, the proton, the nucleus of ordinary hydrogen, has $i=1/2$, while the deuteron, the heavier isotope of hydrogen, has $i=1$. The isotope ${}^{133}Cs$ used in atomic clocks has $i=7/2$.

Not all the multipole fields that occur classically are allowed in the case of a nuclei. There are two rules governing the allowed multipole moments of the nucleus. The first is that electric multipoles of odd $k$ and magnetic multipoles of even $k$ are forbidden. To see why, consider what would happen if the nucleus had an electric dipole moment. Then the dipole term in {eq}`eq-hyperfine-1` would be a (presumably small) correction to the potential seen by the atomic electron. Since the potential seen by the electron is $V=-e\Phi$, the perturbing Hamiltonian would be

:::{math}
:label: eq-hyperfine-5
H_1= -e{\dvec\cdot\rvec\over r^3}.
:::

The dipole moment vector $\dvec$ is not a $c$-number as in classical electrostatics, rather it is a (vector) operator acting on the nuclear Hilbert space, just like the magnetic moment $\muvec$. And just like $\muvec$, $\dvec$ must be proportional to the spin, say, $\dvec=k\Ivec$, because all vector operators on a single irreducible subspace are proportional. See Prob. {ref}`prob-wigeck-2`(a). Thus,

:::{math}
:label: eq-hyperfine-6
H_1=-ke {\Ivec\cdot\rvec\over r^3}.
:::

Now under parity $\pi$ the angular momentum $\Ivec$ is invariant, but the electron position vector $\rvec$ changes sign. And under time reversal $\Theta$ the angular momentum vector $\Ivec$ changes sign and $\rvec$ does not. Thus we find that $H_1$ violates both parity and time reversal,

:::{math}
:label: eq-hyperfine-7
\begin{aligned}
\pi H_1 \pi^\dagger &= -H_1, \\
\Theta H_1 \Theta^\dagger &= -H_1. \\

\end{aligned}
:::

A similar argument applies to the other forbidden terms.

The presence of such terms would indicate a violation of both parity and time reversal. The weak interactions do violate parity, and we do know that time reversal (more precisely, CP) is violated at a very small level in certain decay processes (see {ref}`ch-parity`{} and \timerev), so it is possible that the terms forbidden by this rule actually exist at a small level. For example, the neutron or the electron may have an electric dipole moment, but if such moments exist, they are certainly very small. There is currently considerable experimental interest in lowering the known upper bounds on these “forbidden” moments, or possibly even discovering a nonzero value for some of them, because a numerical value for one of these moments would shed light on physics beyond the standard model.

The experimentally known limits on the electric dipole moment of the neutron give rise to what is known as the “strong CP-problem” in particle physics. Theories of the strong interactions suggest that they should violate CP symmetry at a level that would show up as an electric dipole moment of the neutron that is larger than the experimentally known upper bound. Recall that the CPT theorem says that the product CPT is an exact symmetry of all quantum fields, so CP violation implies violation of time reversal. This suggests that there is some mechanism to suppress CP violation. One possibility that has been explored involves postulating the existence of a particle of very small mass, the “axion.” Nowadays the axion, in addition to solving the strong CP-problem, is looked upon as a candidate for dark matter, and extensive searches are underway to find it. Its discovery would be a major advance in both particle physics and astrophysics.

The second rule states that a $2^k$-pole can occur only if $k\le 2i$. For example, the proton with $i=\frac{1}{2}$ can (and does) possess an electric monopole moment and a magnetic dipole moment, but not an electric quadrupole moment. The deuteron with $i=1$ can (and does) possess an electric quadrupole moment, but the alpha particle with $i=0$ can possess only the electric monopole moment. There are no hyperfine effects in ${}^4He$, or with any other isotope with spin~0 (such as ${}^{12}C$ or ${}^{16}O$).

Lying behind this rule is the fact that the operator representing the $2^k$-pole on the nuclear Hilbert space is, in fact, an order $k$ irreducible tensor operator. We have already studied the examples of the magnetic dipole moment and the electric quadrupole moment, which are respectively $k=1$ and $k=2$ irreducible tensor operators. In fact, the expansion of classical electric and magnetic fields into multipoles is an example of the decomposition of a space of fields on three-dimensional space into irreducible subspaces under rotations, each of which has an angular momentum value ($\ell=0$ for monopole, $\ell=1$ for dipole, etc). The fields in question are classical fields, not quantum wave functions, but the transformation properties under rotations is exactly as presented in {ref}`ch-repsamos`\ and \orbamsph.

But the maximum order of an irreducible tensor operator on the nuclear Hilbert space with spin $i$ is $k=2i$. To see this notice that any operator $A$ that acts on the nuclear Hilbert space can be expanded as a linear combination of the operators $\ketbra{m_i}{m'_i}$, where $\ket{m_i} = \ket{im_i}$ (we suppress the index $i$, which is constant):

:::{math}
:label: eq-hyperfine-8
A = \sum_{m_i,m'_i} \ket{m_i} \matrixelement{m_i}{A}{m'_i} \bra{m'_i} = \sum_{m_i,m'_i} A_{m_im'_i} \, \ketbra{m_i}{m'_i},
:::

where

:::{math}
:label: eq-hyperfine-9
A_{m_im'_i} = \matrixelement{m_i}{A}{m'_i}.
:::

Thus, the $(2i+1)^2$ operators $\ketbra{m_i}{m'_i}$ form a basis in the space of operators acting on the nuclear Hilbert space. But since the kets $\ket{m_i}$ transform under rotations according to the irreducible representation $j=i$, and since the bras $\bra{m'_i}$ also transform according to the same irreducible representation, the operator $\ketbra{m_i}{m'_i}$ transforms according to

:::{math}
:label: eq-hyperfine-10
i \otimes i = 0 \oplus \ldots \oplus 2i.
:::

Each $k$ in the range $0\le k\le 2i$ occurs precisely once in this list, so on the nuclear Hilbert space there is precisely one scalar operator (to within a multiplicative constant), one vector, etc, all the way up to one order $k=2i$ irreducible tensor operator. Equivalently, any operator that acts on the nuclear Hilbert space can be represented as a sum of irreducible tensor operators of order not exceeding $k=2i$. Operators with $k>2i$ do not occur. See Prob. {ref}`prob-wigeck-2`(a).

To understand how the moments that are forbidden in the case of a nucleus or an elementary particle can occur classically, see the discussion in Secs. {ref}`sec-transfop-9` and {ref}`sec-transfop-12` (it has to do with the fact that in the case of the nucleus, we are dealing with a single irreducible subspace under rotations).

(sec-hyperfine-4)=

## Magnetic Dipole Hyperfine Effects.   The Physical Picture

The only hyperfine effect we shall examine in these notes is the one due to the magnetic dipole moment of the nucleus. It turns out that if the electric quadrupole moment exists, then its effects are of the same order of magnitude as those of the magnetic dipole, so any realistic treatment requires that the two be treated together (unless selection rules make the quadrupole term vanish). In the following we will treat magnetic dipole effects in a single electron atom with nuclear spin $i$, but to be realistic $i$ should not exceed $\frac{1}{2}$. This condition holds in ordinary hydrogen with the proton as its nucleus, and at a certain point in the calculation we will specialize to that case.

A classical model of the effect will be useful in understanding what we do. To be specific we think of hydrogen. The proton at the center of the atom produces a magnetic dipole field in addition to the electrostatic, Coulomb field. The Coulomb field is rotationally invariant, but the magnetic dipole field depends on the orientation of the proton. As the electron moves in its orbit, which is largely determined by the electrostatic force, it also feels a $\vvec\cross\Bvec$ force due to the proton's magnetic field, which modifies the orbit somewhat. At the same time the electron's spin has an energy of orientation in the proton's magnetic field, and precesses in response. Also, the proton itself feels a magnetic field produced by the electron, both by its orbital motion and by its own magnetic moment, and precesses in response. Thus the orientation of the proton is not constant, but evolves in time as the electron executes its orbit. This picture makes it clear that the dynamics of the proton spin are coupled to the dynamics of the atomic electron, and that they must be handled together.

In the following we shall make a quantum mechanical analysis of these effects. Perhaps surprisingly, it turns out to be possible to obtain a closed formula for the shifts in the atomic energy levels, in terms of the expectation value of $1/r^3$. In the case of hydrogen, the latter can be evaluated explicitly.

(sec-hyperfine-5)=

## About Magnetic Dipoles

We begin by considering magnetic dipole fields in classical magnetostatics. A point magnetic dipole of moment $\muvec$ situated at the origin of the coordinates produces a magnetic field $\Bvec = \del\cross \Avec$, where

:::{math}
:label: eq-hyperfine-11
\Avec(\rvec) = {\muvec\cross\rvec \over r^3} = -\muvec \cross \del\Bigl( {1\over r} \Bigr).
:::

The vector potential $\Avec$ falls off as $1/r^2$ and the magnetic field $\Bvec$ as $1/r^3$ at large $r$, both with a nontrivial angular dependence. Both fields have a singularity at the origin that must be treated with some care in the quantum mechanical analysis of hyperfine effects.

We will do this by smearing out the point dipole moment over a sphere of small radius $a$, producing a model in which the dipole is replaced by a uniformly magnetized sphere at the origin. Recall that in magnetostatics the magnetization $\Mvec$ is the dipole moment per unit volume, so we require

:::{math}
:label: eq-hyperfine-12
\muvec = V \Mvec,
:::

where $\Mvec$ is the constant magnetization inside the sphere and where $V$ is the volume of the sphere,

:::{math}
:label: eq-hyperfine-13
V = {4\over 3} \pi a^3.
:::

This model produces fields that are well behaved everywhere in space. When we are done with the quantum mechanical calculation, we will take $a \to 0$ in such a way that $\muvec$ is constant, and we will find physical results that are finite and well behaved. Notice that in this limit, $\Mvec \to \infty$.

The problem of the uniformly magnetized sphere is a standard one in courses on electromagnetism. The vector potential $\Avec$ at a field point $\rvec$ can be computed as an integral over the source distribution inside the volume of the sphere,

:::{math}
:label: eq-hyperfine-14
\Avec(\rvec) = \int_vol d^3\rvec' \, {\Mvec\cross(\rvec-\rvec') \over |\rvec-\rvec'|^3} = \Mvec \cross \biggl[ -\del \int_vol d^3\rvec' \, \Bigl( {1\over |\rvec-\rvec'|} \Bigr)\biggr].
:::

The field point $\rvec$ can be either inside or outside the sphere. The quantity in the square brackets is easily evaluated with some reasoning from electrostatics. The integral is the electrostatic potential produced at field point $\rvec$ due to a uniformly charged sphere of radius $a$ and charge density $\rho=1$. Thus, the negative gradient of that integral is the electric field produced by the same charge density. But by Gauss's law, that electric field is $\rvec/r^3$ times the amount of charge inside radius $r$. Thus we have

:::{math}
:label: eq-hyperfine-15
\begin{aligned}
-\del \int_vol d^3\rvec' \Bigl( {1\over |\rvec-\rvec'|} \Bigr) = {\rvec \over r^3} \times \begin{cases} \ds{\ds 4\pi \over \ds 3} r^3, & r<a, \\  \ds {\ds 4\pi \over \ds 3} a^3, & r>a. \\\end{cases}
\end{aligned}

:::

Combining this with {eq}`eq-hyperfine-12`--{eq}`eq-hyperfine-14`, we obtain

:::{math}
:label: eq-hyperfine-16
\begin{aligned}
\Avec(\rvec) = \muvec\cross\rvec \begin{cases} \ds {\ds 1 \over \ds a^3}, & r<a, \\  \ds {\ds  1 \over \ds r^3}, & r>a. \\\end{cases}
\end{aligned}

:::

The exterior solution is identical to that of a point dipole, {eq}`eq-hyperfine-11`; in the region $r>a$, one cannot tell from the field alone whether it is produced by a point dipole or a uniformly magnetized sphere of the same strength.

By taking the curl we compute the magnetic field,

:::{math}
:label: eq-hyperfine-17
\begin{aligned}
\Bvec(\rvec) = \begin{cases} \ds {\ds 2\muvec \over \ds a^3}, & r<a, \\  \ds {\ds\muvec \cdot \Tmat\over\ds r^5}, & r>a. \\\end{cases}
\end{aligned}

:::

where $\Tmat$ is defined in {eq}`eq-hyperfine-2`. The notation $\muvec \cdot \Tmat$ means the vector whose $j$-th component is $\sum_i \mu_i T_{ij}$. Notice that $T_{ij}$ is a symmetric and traceless tensor, something that becomes a $k=2$ irreducible tensor operator when reinterpreted as a quantum operator. The vector potential {eq}`eq-hyperfine-16` is continuous at the radius $r=a$; the magnetic field {eq}`eq-hyperfine-17`, however, has a discontinuity there, due to a surface current.

To express both $\Avec$ and $\Bvec$ in single formulas, we introduce the following functions:

:::{math}
:label: eq-hyperfine-18
\begin{aligned}
\Delta(r) = \begin{cases} \ds{\ds 1 \over \ds a^3}, & r<a, \\  0, & r>a,\\\end{cases}
\end{aligned}

:::

and

:::{math}
:label: eq-hyperfine-19
\begin{aligned}
f(r) = \begin{cases} 0, & r<a, \\  1, & r>a. \\\end{cases}
\end{aligned}

:::

Then we can write

:::{math}
:label: eq-hyperfine-20
\Avec(\rvec) = (\muvec\cross\rvec) \biggl[ \Delta(r) + {f(r) \over r^3} \biggr],
:::

and

:::{math}
:label: eq-hyperfine-21
\Bvec(\rvec) = \muvec \cdot \biggl[ 2\Delta(r) \Imat + f(r){\Tmat\over r^5}\biggr],
:::

where $\Imat$ is the identity tensor.

When we take the limit $a \to 0$, $\Delta(r)$ becomes a function that is concentrated inside a small volume $(4\pi/3) a^3$ with a value that goes to $\infty$ in such a way that the integral of $\Delta(r)$ over all space is the constant $4\pi/3$. This is the behavior of a function whose limit is a delta function, so we can write

:::{math}
:label: eq-hyperfine-22
\lim_{a \to 0} \Delta(r) = {4 \pi \over 3} \delta(\rvec).
:::

As for $f(r)$, it has the limit,

:::{math}
:label: eq-hyperfine-23
\lim_{a \to 0} f(r) = 1.
:::

(sec-hyperfine-6)=

## The Hamiltonian and the Hilbert Space

We turn now to the atom in which the nucleus resides. In these notes we will be mainly interested in hyperfine effects in hydrogen and alkali atoms, the latter treated as atoms with a single electron (the valence electron) moving in a screened Coulomb potential.

In the following we use atomic units and take $g=2$ for the $g$-factor of the electron, so $\mu_B = 1/2c$. The Hamiltonian for the atomic electron is

:::{math}
:label: eq-hyperfine-24
H={1\over2} \biggl( \pvec + {1\over c} \Avec\biggr)^2 +V(r) + H_FS + H_Lamb + {1\over c}\Svec \cdot \Bvec,
:::

where $V(r)$ is the central force potential. This could be the Hamiltonian for the Zeeman effect, except that in this case the fields $\Avec$ and $\Bvec$ are not external fields, rather they are the magnetic dipole fields of the nucleus. Thus, they are given by {eq}`eq-hyperfine-20` and {eq}`eq-hyperfine-21`. We include in the Hamiltonian the fine structure terms $H_FS$, the sum of the three terms shown in {eq}`eq-finestruc-25a`, and terms responsible for the Lamb shift, since we wish to make a realistic treatment of hyperfine effects which are smaller than those just listed. We will not need to know much about the Lamb shift in the following analysis, except that it splits the energy levels in hydrogen to give them a dependence on $\ell$.

The expressions {eq}`eq-hyperfine-20` and {eq}`eq-hyperfine-21` for $\Avec$ and $\Bvec$ are the fields of a classical magnetic dipole at the origin, but now for use in the Hamiltonian {eq}`eq-hyperfine-24` we must reinterpret $\muvec$ as an operator acting on the nuclear Hilbert space, given in terms of the nuclear spin by

:::{math}
:label: eq-hyperfine-25
\muvec = g_N \mu_N \Ivec,
:::

where $g_N$ is the $g$-factor of the nucleus and $\mu_N$ is the nuclear magnetic moment (see \spinmagf.8). Thus, the Hamiltonian {eq}`eq-hyperfine-24` must be interpreted as an operator acting the total Hilbert space

:::{math}
:label: eq-hyperfine-26
\ES = \ES_elec \otimes \ES_nucl,
:::

where $\ES_elec$, the electronic Hilbert space, is the product of its orbital and spin parts,

:::{math}
:label: eq-hyperfine-27
\ES_elec = \ES_orb \otimes \ES_spin.
:::

Basis states in $\ES$ can be defined as products of basis states in $\ES_elec$ and in $\ES_nucl$. For $\ES_elec$ the obvious basis is the eigenbasis of $H_0$, $\{ \ket{n\ell j m_j} \}$ in the notation of {ref}`ch-finestruc`, which have energies $E_{n\ell j}$. In alkalis the energies depend strongly on $\ell$, and in hydrogen they depend on $\ell$ because of the Lamb shift. The obvious basis in $\ES_nucl$ is $\{ \ket{im_i} \}$. Thus we define the basis states in $\ES$,

:::{math}
:label: eq-hyperfine-28
\ket{n\ell j m_j} \otimes \ket{im_i} = \ket{n \ell j m_j m_i},
:::

where we suppress the index $i$ in the shorthand notation on the right hand side, since it is a constant. We will call this the “uncoupled basis,” because the electronic angular momentum $\Jvec$ and nuclear angular momentum $\Ivec$ are not coupled. Of course, orbital and spin angular momentum have already been coupled to produce $\Jvec$, so the basis {eq}`eq-hyperfine-28` is really only partially uncoupled. These uncoupled basis states are eigenstates of $H_0$ on the whole Hilbert space $\ES$. The energy does not depend on the quantum numbers $m_j$ or $m_i$, so the energy eigenstates are $(2j+1)(2i+1)$-fold degenerate.

Now we expand the kinetic energy in the Hamiltonian {eq}`eq-hyperfine-24` as in {ref}`ch-zeeman`\ and neglect the term in $A^2$, writing the result as $H = H_0 + H_1$, where

:::{math}
:label: eq-hyperfine-29
H_0 = {p^2 \over 2} +V(r) + H_FS + H_Lamb,
:::

and

:::{math}
:label: eq-hyperfine-30
H_1 = {1\over c} (\pvec \cdot \Avec + \Svec \cdot \Bvec).
:::

Here we have used the fact that our $\Avec$ is in Coulomb gauge, $\del \cdot \Avec=0$, so $\pvec\cdot\Avec = \Avec\cdot\pvec$. We write the two terms in $H_1$ as $H_{1,orb}$ and $H_{1,spin}$. For $H_{1,orb}$ we use $1/c=2\mu_B$ and {eq}`eq-hyperfine-25` and {eq}`eq-hyperfine-20`, rearranging the triple product,

:::{math}
:label: eq-hyperfine-31
\pvec \cdot(\Ivec \cross \rvec) = \Ivec \cdot (\rvec \cross \pvec) = \Ivec \cdot \Lvec.
:::

This gives

:::{math}
:label: eq-hyperfine-32
H_{1,orb} = {1\over c} \pvec\cdot\Avec =k(\Ivec \cdot \Lvec) \biggl[ \Delta(r) + {f(r) \over r^3} \biggr],
:::

where we have set

:::{math}
:label: eq-hyperfine-33
k=2g_N\mu_B\mu_N = g_eg_N\mu_B\mu_N
:::

for the product of the effective magnetic moments of the electron and the nucleus (including $g$-factors). As for $H_{1,spin}$, we rearrange it similarly, obtaining

:::{math}
:label: eq-hyperfine-34
H_{1,spin} = {1\over c} \Svec \cdot \Bvec = k\biggl[ 2\Delta(r) (\Ivec \cdot\Svec) + f(r) {(\Ivec \cdot\Tmat\cdot \Svec)\over r^5}\biggr].
:::

Notice that $H_{1,orb}$ is a kind of spin-orbit interaction (but it is the spin of the nucleus, not the spin of the electron), and $H_{1,spin}$ is a kind of spin-spin interaction.

Properly we should only take the limit $a \to 0$ after we have formed matrix elements, but in many books this limit is taken before, resulting in the formulas,

:::{math}
:label: eq-hyperfine-35
H_{1,orb} = k(\Ivec \cdot \Lvec) \biggl[ {4\pi\over 3} \delta(\rvec) + { 1 \over r^3} \biggr],
:::

and

:::{math}
:label: eq-hyperfine-36
H_{1,spin} = k \biggl[ {8\pi \over 3} \delta(\rvec) (\Ivec \cdot\Svec) + {(\Ivec \cdot\Tmat\cdot \Svec)\over r^5}\biggr].
:::

The terms involving $\delta(\rvec)$ are called “Fermi contact terms,” because they vanish except when the electron and nucleus are in contact with one another ($r=0)$, and in honor of Fermi, who first carried out the calculation presented in this set of notes.

(sec-hyperfine-7)=

## The Perturbation Calculation

Both terms {eq}`eq-hyperfine-32` and {eq}`eq-hyperfine-34` in the perturbing Hamiltonian have the form of $\Ivec$ dotted into a vector that is constructed out of electronic operators, that is, operators that act only on the electronic Hilbert space. Since the angular momentum $\Jvec$ generates rotations that rotate electronic vectors, while $\Ivec$ generates rotations that rotate $\Ivec$ itself, the dot products in $H_1$ are not invariant under either electronic rotations alone or under nuclear rotations alone. For this reason, $H_1$ does not commute with either $J_z$ or $I_z$, and the uncoupled basis {eq}`eq-hyperfine-28` is not the best one for carrying out the perturbation calculation (see \finestruc.5).

The dot products in question, however, are invariant under total rotations of the system, electronic plus nuclear, which are generated by the total angular momentum of the system defined by

:::{math}
:label: eq-hyperfine-37
\Fvec = \Jvec + \Ivec = \Lvec + \Svec + \Ivec.
:::

This suggests that we couple together $\Jvec$ and $\Ivec$ to create eigenstates of $F^2$ and $F_z$. We will call the result the “coupled basis”; it is given by

:::{math}
:label: eq-hyperfine-38
\ket{n\ell j f m_f} = \sum_{m_j,m_i} \ket{n\ell jm_jm_i} \braket{jim_jm_i}{fm_f},
:::

where the final scalar products are the Clebsch-Gordan coefficients.

In the coupled basis the matrix elements we need to consider for degenerate perturbation theory are

:::{math}
:label: eq-hyperfine-39
\matrixelement{n\ell jfm_f}{H_1}{n\ell j f'm'_f},
:::

where the unprimed indices on the two sides specify the degenerate unperturbed energy level $E_{n\ell j}$, while the remaining indices specify the basis inside the degenerate eigenspace of the unperturbed system. But since $[\Fvec,H_1]=0$, and since if $H_1$ commutes with $\Fvec$ it commutes with any function of $\Fvec$ such as $F^2$, the matrix {eq}`eq-hyperfine-39` is diagonal in both $f$ and $m_f$, and the primes can be dropped. We need only compute the diagonal matrix elements to find the energy shifts, and once again we have succeeded in doing a degenerate perturbation calculation without diagonalizing any matrices. Thus we have

:::{math}
:label: eq-hyperfine-40
\Delta E = \matrixelement{n\ell jfm_f}{H_1} {n\ell jfm_f}.
:::

We now evaluate these matrix elements for the case $\ell \ne 0$. In this case the contact terms do not contribute in the limit $a \to 0$, because the wave functions go as $r^\ell$ near $r=0$, and thus vanish at $r=0$ when $\ell \ne 0$. As for the other terms, we take the limit $a \to 0$ so $f(r)=1$, and write the result in the form

:::{math}
:label: eq-hyperfine-41
\Delta E = k \matrixelement{n\ell jfm_f}{\Ivec \cdot \Gvec} {n\ell jfm_f},
:::

where

:::{math}
:label: eq-hyperfine-42
\Gvec = {\Lvec\over r^3} + {\Tmat \cdot \Svec \over r^5} = {\Lvec\over r^3}+ { 3\rvec(\rvec \cdot \Svec) - r^2 \Svec \over r^5},
:::

where we use {eq}`eq-hyperfine-2`. Note that $\Gvec$ is a purely electronic vector operator.

We simplify {eq}`eq-hyperfine-41` by using the projection theorem (see {ref}`sec-zeeman-7` and Prob. {ref}`prob-zeeman-1`), which tells us that an operator such as $\Gvec$, which is a vector under rotations generated by $\Jvec$, sandwiched between eigenstates of $J^2$ with the same $j$ value on both sides, can be replaced by an operator proportional to $\Jvec$:

:::{math}
:label: eq-hyperfine-43
\Gvec \to {(\Gvec\cdot\Jvec)\Jvec \over j(j+1)}.
:::

Thus

:::{math}
:label: eq-hyperfine-44
\Delta E = {k\over j(j+1)} \matrixelement{n\ell jfm_f} {(\Ivec \cdot \Jvec)(\Jvec \cdot \Gvec)} {n\ell jfm_f}.
:::

Now the two dot products can be simplified. First, by {eq}`eq-hyperfine-37`, we have

:::{math}
:label: eq-hyperfine-45
\Ivec\cdot\Jvec = {1\over 2} \bigl( F^2 - J^2 - I^2).
:::

Next, we use $\rvec \cdot \Jvec = \rvec \cdot \Svec$ (since $\rvec \cdot \Lvec=0$) to write

:::{math}
:label: eq-hyperfine-46
\Gvec \cdot \Jvec = {L^2\over r^3} +{3(\rvec\cdot\Svec)^2 -r^2S^2\over r^5},
:::

where a term $\Lvec\cdot\Svec/r^3$ has cancelled. Then, since $\Svec = (1/2)\sigmavec$ and since $\sigma_i \sigma_j = \delta_{ij} + i\epsilon_{ijk}\, \sigma_k$, the final term in {eq}`eq-hyperfine-46` simplifies,

:::{math}
:label: eq-hyperfine-47
3(\rvec\cdot\Svec)^2  = {3r^2\over 4},
:::

which cancels $r^2S^2 = 3r^2/4$. The result is simply

:::{math}
:label: eq-hyperfine-48
\Gvec \cdot \Jvec = {L^2\over r^3}.
:::

Then, with {eq}`eq-hyperfine-45` and {eq}`eq-hyperfine-48`, the energy shift {eq}`eq-hyperfine-44` becomes

:::{math}
:label: eq-hyperfine-49
\Delta E = k { f(f+1)-j(j+1)-i(i+1) \over 2j(j+1)} \, \ell(\ell+1)\Bigl< {1\over r^3} \Bigr>,
:::

where the final expectation value of $1/r^3$ can be reduced to a purely spatial matrix element with respect to the state $\ket{n\ell 0}$ exactly as in \finestruc.7. Specializing to hydrogen and using {eq}`eq-hyperfine-33` and {eq}`eq-finestruc-47`, we find

:::{math}
:label: eq-hyperfine-50
\Delta E = {g_eg_N\mu_B\mu_N\over a_0^3} {1\over n^3} { f(f+1)-j(j+1)-i(i+1) \over j(j+1)(2\ell+1)},
:::

where we have introduced a factor of $1/a_0^3$ ($a_0$ is the Bohr radius) to make the answer have dimensions of energy (thus it is now valid in ordinary units).

{eq}`eq-hyperfine-50` is the final expression for the hyperfine structure energy shift in hydrogen in the case $\ell \ne 0$. However, one can show that the same answer holds also in the case $\ell=0$, so {eq}`eq-hyperfine-50` applies in all cases.

(sec-hyperfine-8)=

## The New Energy Levels

The energy levels were $E_{n\ell j}$ before the hyperfine interactions were turned on, but since $\Delta E$ in {eq}`eq-hyperfine-50` depends on $f$, they now have the form $E_{n\ell jf}$. The energy eigenstates are $\ket{n\ell jfm_f}$, and are $(2f+1)$-fold degenerate, since the energy does not depend on $m_f$. This is precisely the situation expected of a generic system invariant under rotations; the energy eigenspaces consist of a single irreducible subspace under rotations (see Secs. {ref}`sec-transfop-9`--{ref}`sec-transfop-12`); and the degeneracy present is explained by rotational invariance alone.

The energy shift {eq}`eq-hyperfine-50` causes the fine structure levels in the Dirac picture of hydrogen to split, giving rise to hyperfine multiplets. For example, the ground state $1s_{1/2}$ splits into two levels $f=0$ and $f=1$, of which $f=0$ is lower since by {eq}`eq-hyperfine-50` the energies are an increasing function of $f$. This $f=0$ level is the true ground state of hydrogen. It is nondegenerate. The $f=1$ level is 3-fold degenerate, and lies above the ground state by an energy of approximately $1.42$~GHz in frequency units, or $21$~cm in wave length units, or $0.068$~K in temperature units. Since $\ell=0$ for these states, the total angular momentum $\Fvec$ is really just the total spin $\Svec+\Ivec$, and the $f=0$ and $f=1$ states are the spin singlet and triplet states, respectively. The electron and proton spins are antiparallel in the ground (singlet) state; when one of the spins is flipped to make them parallel (the triplet state), the energy is raised.

Similarly, other $j=1/2$ states including the $2s_{1/2}$ and $2p_{1/2}$ states split into an $f=0$ and $f=1$ pair. The $2p_{3/2}$ state in the Dirac picture splits into an $f=1$ and $f=2$ pair.

Electric dipole transitions between the various hyperfine levels are governed by the matrix element,

:::{math}
:label: eq-hyperfine-51
\matrixelement{n\ell jfm_f}{x_q}{n'\ell'j'f'm'_f}.
:::

The selection rules for this matrix element follow from the Wigner-Eckart theorem and parity. The Wigner-Eckart theorem can be used three times, once for each of the three angular momenta $\Lvec$, $\Jvec$ and $\Fvec$, since $x_q$ is a $k=1$ irreducible tensor operator with respect to rotations generated by any of these angular momenta. Thus, the matrix element {eq}`eq-hyperfine-51` vanishes unless the following selection rules are satisfied:

:::{math}
\begin{aligned}
m_f &= m'_f + q,
\end{aligned}
:::

:::{math}
\begin{aligned}
\Delta f &= 0, \pm 1\quad \\textbut f=0 \to f=0 not allowed,
\end{aligned}
:::

:::{math}
\begin{aligned}
\Delta j &=0, \pm 1,
\end{aligned}
:::

:::{math}
:label: eq-hyperfine-52
\begin{aligned}
\Delta \ell &= \pm1.
\end{aligned}
:::

The exclusion of $f=0 \to f=0$ comes from the fact that $0\otimes1=1$, so if $f=f'=0$, then the matrix element vanishes. The only reason we do not also exclude $j=0 \to j=0$ is that $j$ is half-integral, and cannot take on the value 0. And the only reason we do not make a special case of excluding $\ell=0 \to \ell=0$ is that that case is already excluded by parity.

The hyperfine splitting of the $1s_{1/2}$ level in hydrogen is particularly interesting. The separation between the $f=0$ and $f=1$ hyperfine levels is 1.42~GHz, or 21~cm in wavelength units. Electric dipole transitions between these two levels are forbidden by parity, but magnetic dipole transitions are allowed. (One can see this from another standpoint: since spins do not interact with electric fields, an electric dipole transition cannot flip the spins to convert the triplet to the singlet state. But magnetic dipole transitions can.)

The 21~cm line is quite important in radio astronomy. Spiral galaxies typically possess large clouds of atomic hydrogen, which radiate at the 21~cm wavelength. A population of the excited state $f=1$ is maintained by collisions; the temperatures prevalent in the clouds are high enough that the populations of the ground state $f=0$ and the first excited state $f=1$ are determined mostly by the degeneracies (1 for $f=0$ and 3 for $f=1$, although there is some effect due to the Boltzmann factor). By measuring Doppler shifts, the state of motion of the clouds can be measured. In this way, it was first proven that the Milky Way is a spiral galaxy. The 21~cm line is also important in absorption spectra, which can be used to determine the temperature of the clouds of atomic hydrogen.

Molecular hydrogen has a completely different hyperfine structure from atomic hydrogen, arising from the spin-spin interaction of the two protons in the molecule. The transitions between the hyperfine levels of molecular hydrogen are in the megahertz range of frequencies.

\problems

(prob-hyperfine-1)=

**Problem \prbdhyperfine-1..** 

\problempart{(a)} {eq}`eq-hyperfine-50` was derived in the case $\ell\ne0$. Show that it also applies in the case $\ell=0$. Hint: Use the fact that the components of the tensor $T_{ij}$, defined in {eq}`eq-hyperfine-2`, are $r^2$ times linear combinations of the $Y_{2m}(\theta,\phi)$, for $m=-2, \ldots, +2$. This is related to the fact that $T_{ij}$ is the Cartesian version of an order 2 irreducible tensor.

\problempart{(b)} Our analysis of the hyperfine interaction in hydrogen has included the energy of interaction of the electron with the magnetic dipole field produced by the proton, but it seems that we have not included the energy of interaction of the proton spin with the magnetic field produced by the electron. As seen by the proton, the electron produces a magnetic field for two reasons: first, it is a charge in motion, therefore a current, which makes a magnetic field. This is the magnetic field due to the orbital motion of the electron. Next, the electron has a magnetic moment of its own, which makes a dipole magnetic field. This is the magnetic field produced by the spin of the electron.

Work out an expression for the energy of interaction of the proton spin with the magnetic field produced by the orbital motion of the electron. Follow the analysis of the spin-orbit interaction in {ref}`sec-finestruc-2`, but run it backwards. That is, putting primes on the fields in the electron rest frame and no primes on fields in the proton rest frame, use Coulomb's law to write down the field $\Evec'$ of the electron in its own rest frame, then Lorentz transform to the lab frame to get $\Bvec$ (call this $\Bvec_orb$, the magnetic field due to the orbital motion of the electron). Then the energy of interaction of the proton with this magnetic field is $-\muvec_p \cdot \Bvec_orb$, where $\muvec_p$ is the proton magnetic moment. Notice that unlike the analysis of {ref}`sec-finestruc-2`, there is no factor of $\frac{1}{2}$ from Thomas precession, because the proton frame is not accelerated.

Now use {eq}`eq-hyperfine-21` in the limit $a \to 0$ to obtain the magnetic field produced by the dipole moment of the electron at the position of the proton. Call this $\Bvec_spin$, and write down an expression for the energy of interaction $-\muvec_p \cdot \Bvec_spin$.

If you add these terms to the Hamiltonian ({eq}`eq-hyperfine-29` plus {eq}`eq-hyperfine-30`), does it change the energy shifts {eq}`eq-hyperfine-50`? These energy shifts are confirmed experimentally (for example, by the 21~cm line). What is wrong?

\problempart{(c)} Compute the hyperfine splitting of the ground state of positronium in wavelength units. Notice that in positronium, the fine structure and hyperfine structure are of the same order of magnitude.

Now some remarks about part (c). The interesting thing about this calculation is that the answer based on what you now know is actually wrong, because it omits a virtual process (a Feynman diagram) in which the positron and electron annihilate into a photon, which then materialize back into a positron and electron.

The analysis of this process requires quantum field theory. The Hamiltonians we usually use in atomic, molecular and solid state physics, expressed in terms of a finite number of particles and a finite number of degrees of freedom, are only valid up to a certain degree of accuracy, beyond which interactions with the infinite degrees of freedom in various fields (electromagnetic, electron-positron, strong interactions, $\ldots$) cannot be ignored. The first place where this occurs in hydrogen is with the Lamb shift. In positronium, it happens at the level of the fine structure (in positronium, the hyperfine structure is considered part of the fine structure).

(prob-hyperfine-2)=

**Problem \prbdhyperfine-2.} In our derivation of the energy shifts {eq}`eq-hyperfine-50`, we assumed that hyperfine effects were much smaller than the Lamb shift.  This is what allowed us to assume that the $\ell$ values on the two sides of the matrix element {eq}`eq-hyperfine-39` were the same.  Compute the hyperfine energy shifts for the $2s_{1/2}$ and $2p_{1/2}$ levels in hydrogen, and compare to the Lamb shift.  Make a sketch of the energy levels like that in Fig.~\figr\finestruc.3, including the hyperfine structure (but you can omit the $2p_{3/2.** 

(prob-hyperfine-3)=

**Problem \prbdhyperfine-3..** 

In the usual atomic clock an atomic beam is passed through a region of space with an oscillating magnetic field produced by an RF oscillator, much as in the magnetic resonance experiments discussed in {ref}`ch-spinmagf`. When the frequency of the oscillator is close enough to the hyperfine transition frequency, it causes the hyperfine state to change, thereby modifying the trajectory of the atom in a subsequent Stern-Gerlach apparatus. A feedback mechanism locks the frequency of the oscillator onto the hyperfine transition frequency, so that only atoms following a certain trajectory, corresponding to a certain }$f$ value, are passed. See R.~E.~Beehler, R.~C.~Mockler and J.~M.~Richardson, *Metrologia* **1**, 114(1965).

Hyperfine transition frequencies in the alkali atoms and hydrogen are among the most accurately known physical quantities. In fact, as mentioned, the second is currently defined in terms of the hyperfine transition frequency in cesium. As for hydrogen, measurements of the transition frequency give $\nu_0=1,420,405,751.7667\pm0.001\,Hz$ [see L.~Essen, R.~W.~Donaldson, M.~J.~Bangham and E.~G.~Hope, *Nature (London)* **229**, 110(1971)].

Unfortunately, to flip the hyperfine state we need a background field $\Bvec_0$, in addition to the oscillating magnetic field, as explained in {ref}`ch-spinmagf`, and this modifies the hyperfine transition frequency. Thus, it is necessary to know how the hyperfine transition frequency depends on the background field $B_0$ in order to make the correction. Also, the accuracy of the clock now depends on the accuracy with which we can measure $B_0$.

In this problem for simplicity we will work with hydrogen, but the theory is not much more complicated for atoms such as cesium.

\problempart{(a)} Let $W$ be the energy difference between the two hyperfine states in hydrogen (the $f=0$ and $f=1$ states). This can be calculated from {eq}`eq-hyperfine-50`, or from the experimental value of $\nu_0$. (They should agree, and since you shouldn't believe everything you read you might want to check that they do.) To estimate the magnetic field strengths we will be talking about, let us note that the energy of interaction of an electon spin with a magnetic field $B$ is of the order of $\mu_B B$, and let us define a field strength $B_1$ by

:::{math}
:label: eq-hyperfine-53
B_1={W\over \mu_B},
:::

where $\mu_B$ is the Bohr magneton. Evaluate $B_1$ in Gauss or Tesla (see {ref}`sec-emunits-7`). This is roughly the field strength at which the effect of an external field is comparable to the hyperfine interaction. When $B_0\approx B_1$ the hyperfine structure seen at $B_0=0$ is strongly modified by the external field. We will want to operate the atomic clock at field strengths $B_0\ll B_1$, so that the corrections due to $B_0$ are small.

\problempart{(b)} Write the Hamiltonian for the hydrogen atom as $H=H_0+H_1$ where

:::{math}
:label: eq-hyperfine-54
\begin{aligned}
H_0&=H_{ES}+H_{FS}+H_{Lamb}, \\
H_1&=H_{HFS}+H_Z. \\

\end{aligned}
:::

Here $H_{ES}$ is the Hamiltonian in the electrostatic model, $H_{FS}$ are the fine structure corrections studied in {ref}`ch-finestruc`, $H_{Lamb}$ are terms responsible for the Lamb shift, $H_{HFS}$ are the hyperfine corrections, what was called $H_1$ in {eq}`eq-hyperfine-30` (which is presented in atomic units), and $H_Z$ contains terms representing the interaction of the atom with the external field $\Bvec_0$. By treating both $H_{HFS}$ and $H_Z$ as of the same order of magnitude, we will be able to see what happens to the hyperfine structure as the external field $B_0$ is varied from zero up to the value $B_1$ and beyond.

The answers to this problem do not depend on $H_{Lamb}$ and it can be ignored for the purpose of doing the problem. We include it anyway in {eq}`eq-hyperfine-54` because it is really there. It is worthwhile thinking about why it does not affect the answers.

Write out an expression for $H_Z$, including the interaction of the proton spin with the magnetic field $\Bvec_0$. The latter interaction is small but it has a qualitative effect on the energy level diagram so we will keep it. Neglect other terms that are very small. Express $H_Z$ as a multiple of $\mu_B B_0$, and use the abbreviation,

:::{math}
:label: eq-hyperfine-55
\gamma={g_p m_e\over 2 m_p}.
:::

I suggest you use the gauge $\Avec_0=(1/2)\Bvec_0\cross\rvec$, so that $\Bvec_0=\del\cross\Avec_0$ and $\del\cdot\Avec_0=0$.

\problempart{(c)} Find the energy shifts of the ground state ($1s$) of the hydrogen atom in the model represented by $H_0$ due to $H_1$.

I suggest you write $\Delta E_0$ and $\Delta E_1$ for the energies of the hyperfine states $f=0$ and $f=1$, respectively, relative to the energy of the $1s$ level in the model represented by $H_0$. These are the energies computed from {eq}`eq-hyperfine-50` with $f=0$ and $f=1$. Note that

:::{math}
:label: eq-hyperfine-56
W=\Delta E_1-\Delta E_0.
:::

Sketch the behavior of the $1s$ energy levels as a function of $B_0$, as $B_0$ is varied from zero up to $B_1$ and beyond.

\problempart{(d)} You will see that when $B_0\ll B_1$ the effect of $H_Z$ is to split the energy levels indicated by {eq}`eq-hyperfine-50` in proportion to their $m_f$ values, with an effective $g$-factor, as in the weak field Zeeman effect studied in {ref}`ch-zeeman`. Therefore when we operate the atomic clock, we have to decide which pair of magnetic substates we will use for the transition. Actual atomic clocks use the two $m_f=0$ substates (for example, in cesium it is the transition between $\ket{fm_f}=\ket{30}$ and $\ket{40}$). Explain why this is the best choice.

\problempart{(e)} Let $\nu_0=1,420,405,751.7667\pm0.001\,Hz$ be the hyperfine transition frequency in hydrogen in the absence of a background field $B_0$, as quoted above, let $\nu$ be the frequency of the transition when there is a background field $B_0$, and let $\nu=\nu_0+\Delta\nu$. When $B_0\ll B_1$, express $\Delta\nu/\nu_0$ as a function of the dimensionless ratio $B_0/B_1$.

Suppose $B_0=0.05G$, which is known to within an accuracy of $\delta B_0/B_0=1\%$. Find the corresponding accuracy $\delta(\Delta\nu/\nu_0)$. This is the limitation on the precision with which the clock can measure time, due to the accuracy in the measurement of $B_0$.
