---
title: "Appendix A. Gaussian, SI and Other Systems of Units in Electromagnetic Theory"
---
(ch-a-emunits)=

# Appendix A. Gaussian, SI and Other Systems of Units in Electromagnetic Theory

(sec-emunits-1)=

## Introduction

Most students are taught SI units in their undergraduate courses in electromagnetism, but in this course we will use Gaussian units or other systems of units derived from them (atomic units, natural units, etc). This Appendix is intended to help you become familiar with Gaussian units, assuming you have a background in SI units. We will also mention briefly other systems of units, which you may encounter in other courses. We will make only limited use of SI units in this course, mainly for expressing the answers to homework problems.

This Appendix is intended to be as practical as possible for the purposes of this course. We will address the most common problems you will encounter first, and then discuss some general considerations that lie behind the choices of units. We will concentrate on the problems you will likely encounter in this course on quantum mechanics, and neglect other issues. For reference you may also wish to look at Jackson's discussion of units (an appendix in *Classical Electrodynamics*).

In this appendix vectors $\Evec$, $\Bvec$, $\Dvec$ and $\Hvec$ have their usual meanings, while $\Pvec$ and $\Mvec$ are the electric and magnetic dipole moments per unit volume, respectively, and $\pvec$ and $\mvec$ are the electric and magnetic dipole moments of individual dipoles, respectively. The scalar and vector potentials are $\Phi$ and $\Avec$, respectively.

(sec-emunits-2)=

## A Comparison of SI and Gaussian Units

The main advantage of SI units is popularity. The entire engineering world runs on volts, ohms, farads, etc (all SI units), so almost any discussion of electrical equipment or experimental apparatus will be in terms of SI units. The main advantage of Gaussian units is that they make fundamental physical issues and theoretical relations involving electromagnetic phenomena more clear. For example, special relativity and quantum electrodynamics are simpler, more transparent and more elegant in Gaussian units than in SI units, and generally the various formulas of electromagnetism are simpler and easier to remember in Gaussian units than in SI units. Gaussian units are really the simpler system of units, and they would be better for pedagogical purposes were it not for the fact that students must deal with SI units some day anyway.

SI units have gradually been winning the popularity contest against Gaussian and other systems of units. Almost all engineers, most chemists and many physicists now use SI units almost exclusively, and undergraduate courses in electricity and magnetism are now normally taught in SI units. Book publishers have contributed to this trend; they want books written in SI units so engineers will buy them. Nevertheless, it is unlikely that Gaussian units will ever be completely abandoned, because they are so superior for fundamental physical questions.

We will now list several aspects in which SI and Gaussian (and other systems of units) differ.

A fairly trivial difference is the system of units used for mass, distance and time (leaving aside charge for the moment). In SI units, the MKS (meter-kilogram-second) system is used, while the Gaussian units use the cgs (centimeter-gram-second) system. Thus, converting mechanical quantities (energy, force, etc) from SI to Gaussian units only involves various powers of 10. See {ref}`tbl-emunits-1`.

:::{table} Converting mass, distance, and mechanical units only involves powers of 10.
:label: tbl-emunits-1

| | MKS unit | cgs unit | Conversion |
|:---:|:---:|:---:|:---:|
| mass | kilogram | gram | $1\text{kg} = 10^3\text{gm}$ |
| distance | meter | centimeter | $1\text{m} = 10^2\text{cm}$ |
| energy | Joule | erg | $1\text{J} = 10^7\text{erg}$ |
| force | Newton | dyne | $1\text{N} = 10^5\text{dyne}$ |

:::
Another fairly trivial aspect in which SI and Gaussian units differ is the placement of the $4\pi$'s in the formulas. In any system of units for electromagnetism factors of $4\pi$ will appear somewhere; the usual choices are in Maxwell's equations, or else in the force laws (Coulomb and Biot-Savart). The difference is brought about by either absorbing factors of $\sqrt{4\pi}$ into the definition of the unit of charge or splitting them off. Units in which the $4\pi$'s have been eliminated from Maxwell's equations are called *rationalized*; SI units are an example of rationalized units, in which the $4\pi$'s appear in Coulomb's law and the Biot-Savart law (in the factors $1/4\pi\epsilon_0$ and $\mu_0/4\pi$), but not in Maxwell's equations. Gaussian units are not rationalized, so the $4\pi$'s appear in Maxwell's equations. See {eq}`eq-emunits-14`--{eq}`eq-emunits-17`.

Another difference between SI and Gaussian units, this one not so trivial, is the definition of the unit of charge. In Gaussian units, the unit of charge is defined to make Coulomb's law look simple, that is, with a force constant equal to 1 (instead of the $1/4\pi\epsilon_0$ that appears everywhere in SI units). This leads to a simple rule for translating formulas of electrostatics (without $\Dvec$) from SI to Gaussian units: just replace $1/4\pi\epsilon_0$ by $1$. Thus, there are no $\epsilon_0$'s in Gaussian units (see \secremunits-4). There are no $\mu_0$'s either, since these can be expressed in terms of the speed of light by the relation

:::{math}
:label: eq-emunits-1
\epsilon_0\mu_0 = {1\over c^2}.
:::

Instead of $\epsilon_0$'s and $\mu_0$'s, one sees only factors of $c$ in Gaussian units. In SI units one could use {eq}`eq-emunits-1` to eliminate one of the three constants $\epsilon_0$, $\mu_0$ and $c$, but not in a symmetrical manner, so in practice all three constants are retained. The result is that formulas in SI units can be written in a nonunique manner.

In SI units one sees expressions such as the permittivity, permeability or impedance of “free space.” These are not fundamental physical properties of free space, but rather artifacts of the SI system of units, which disappear (along with the $\epsilon_0$'s and $\mu_0$'s) in Gaussian units.

In Gaussian units the unit of charge (the statcoulomb) is defined as the charge such that two charges of one statcoulomb each at one centimeter distance will feel an electrostatic force of one dyne. Thus, in Gaussian units, the electrostatic force constant in Coulomb's law is 1 (see {eq}`eq-emunits-4`, and it is possible to solve Coulomb's law for the charge, dimensionally speaking, to express the unit of charge in terms of other units. This gives

:::{math}
:label: eq-emunits-2
Q = \left( {ML^3\over T^2}\right)^{1/2},
:::

where $M$, $L$, $T$ and $Q$ stand for mass, distance, time and charge, respectively. That is, one statcoulomb is the same as one $gm^{1/2}cm^{3/2}/sec$. It is not practical to do this with SI units (since the force constant is not 1), so the SI unit of charge (the Coulomb) is usually regarded as an independent unit in the SI system. You may not like the fractional powers that appear in {eq}`eq-emunits-2`, but you are always free to treat the statcoulomb as an independent unit also in Gaussian units. Many formulas appear with the square of charge, so there are no fractional powers. In any case, dimensional relations are much simpler in Gaussian units than in SI units.

Another difference between SI and Gaussian units is the fact that the magnetic field $\Bvec$ is defined with an extra factor of $c$ in Gaussian units compared to SI units. This same factor of $c$ percolates down to all derived magnetic quantities, including $\Avec$, $\Mvec$, $\Hvec$ and $\mvec$, and it means that all these quantities have different dimensions in SI units than in Gaussian units, even after the relation {eq}`eq-emunits-2` is taken into account. This is the main difference that makes it difficult to remember how to convert magnetic formulas from SI units to Gaussian units.

It has the benefit, however, that in Gaussian units all the fields $\Evec$, $\Pvec$, $\Dvec$, $\Bvec$, $\Mvec$ and $\Hvec$ have the same dimensions, while in SI units the dimensions are all different. In addition, the scalar and vector potentials $\Phi$ and $\Avec$ have the same dimensions in Gaussian units, but not in SI units. The uniform dimensions for fields in Gaussian units make it easy to remember formulas in that system, and it makes fundamental physical relations more transparent. For example, dielectrics convert $\Evec$ into $\Dvec$, and relativity converts $\Evec$ into $\Bvec$, with coefficients that are dimensionless in Gaussian units. In SI units, it is necessary to insert factors of $\epsilon_0$, $\mu_0$, etc.\ into the conversion formulas, which makes them harder to remember.

A final difference between Gaussian and SI units are the different definitions of the fields $\Dvec$ and $\Hvec$ (in terms of $\Evec$ and $\Pvec$, and $\Bvec$ and $\Mvec$), and likewise different definitions of electric and magnetic susceptibilities. We will not make much use of $\Dvec$ and $\Hvec$ in this course (they are important for the properties of bulk matter), but for reference the differences are described in \secremunits-6.

Other systems of units involve difference choices. For example, the Heaviside-Lorentz system is similar to the Gaussian system, but it is rationalized. There are no $\epsilon_0$'s or $\mu_0$'s in the Heaviside-Lorentz system. Heaviside-Lorentz units are favored by field theorists, who prefer not to see factors of $4\pi$ in the field Lagrangian.

There are many other choices. For example, it would be easy to construct a Gaussian system of units for electromagnetism that uses MKS units for mass, distance and time (and a correspondingly modified definition of the statcoulomb, so the electrostatic force constant would still be unity). Such a system would be nonstandard, but it would have all the advantages of the Gaussian cgs system and none of the disadvantages of the SI system.

:::{table} Numerical values of physical constants in SI and Gaussian units, to four significant figures. Source: Phys.\ Rev.\ D {50}, 1233(1994).
:label: tbl-emunits-2

| Constant | Symbol | SI | Gaussian |
|:---:|:---:|:---:|:---:|
| Speed of light | $c$ | $2.998 \times 10^8 \text{m/sec}$ | $2.998 \times 10^{10} \text{cm/sec}$ |
| Planck's constant | $\hbar$ | $1.055 \times 10^{-34} \text{J-sec}$ | $1.055 \times 10^{-27} \text{erg-sec}$ |
| Boltzmann constant | $k$ | $1.381 \times 10^{-23} \text{J/K}$ | $1.381 \times 10^{-16} \text{erg/K}$ |
| Avogadro number | $N_A$ | $6.022 \times 10^{23}$ | $6.022 \times 10^{23}$ |
| Fine structure constant | $\alpha$ | $1/137.0$ | $1/137.0$ |
| Proton charge | $e$ | $1.602 \times 10^{-19} \text{C}$ | $4.803 \times 10^{-10} \text{statcoul}$ |
| Electron mass | $m_e$ | $9.109 \times 10^{-31} \text{kg}$ | $9.109 \times 10^{-28} \text{gm}$ |
| Proton mass | $m_p$ | $1.673 \times 10^{-27} \text{kg}$ | $1.673 \times 10^{-24} \text{gm}$ |
| Neutron mass | $m_n$ | $1.675 \times 10^{-27} \text{kg}$ | $1.675 \times 10^{-24} \text{gm}$ |
| Permittivity of free space | $\epsilon_0$ | $8.854 \times 10^{-12} \text{F/m}$ | — |
| Permeability of free space | $\mu_0$ | $1.257 \times 10^{-6} \text{N/A}^2$ | — |

:::
(sec-emunits-3)=

## Converting Numerical Values

The values of various fundamental physical constants in the two systems of units are summarized in {ref}`tbl-emunits-2`. Naturally if you carry out a calculation consistently in one system of units, the answer emerges in that system of units. For example, an electric field calculated in Gaussian units comes out in statvolts/centimeter. Usually calculations in the Gaussian system are easier, because there are fewer constants (no $\epsilon_0$'s or $\mu_0$'s).

Once a numerical answer is calculated in one system of units, you may need to convert it to another. {ref}`tbl-emunits-1` can be used to convert mechanical quantities, and {ref}`tbl-emunits-3` will help in converting electromagnetic quantities.

:::{table} Conversion of electromagnetic quantities between SI and Gaussian units. The notation (3) represents $2.9979\ldots$, the same number (apart from a power of 10) that occurs in the speed of light. Note that one $\text{statvolt/cm}$ is the same as one Gauss.
:label: tbl-emunits-3

| Quantity | SI unit | Gaussian unit | Conversion |
|:---:|:---:|:---:|:---:|
| Charge $q$ | Coulomb | statcoulomb | $1 \text{ C} = (3) \times 10^9 \text{ statcoulombs}$ |
| Potential $\Phi$ | Volt | statvolt | $1 \text{ statvolt} = (3)00 \text{ Volts}$ |
| Electric field $\mathbf{E}$ | Volt/m | statvolt/cm | $1 \text{ statvolt/cm} = (3) \times 10^4 \text{ V/m}$ |
| Magnetic field $\mathbf{B}$ | Tesla | Gauss | $1 \text{ Tesla} = 10^4 \text{ Gauss}$ |

:::
(sec-emunits-4)=

## Useful Things to Remember

The following is a list of useful things to remember when converting numbers, equations, or concepts between SI and Gaussian units.

- It is useful to remember that 1 statvolt is (approximately) 300 Volts, and that 1 Tesla is exactly $10^4$ Gauss.

- It is worthwhile memorizing Maxwell's equations in both systems of units, both the vacuum equations {eq}`eq-emunits-14`--{eq}`eq-emunits-17`, and the macroscopic equations {eq}`eq-emunits-40`--{eq}`eq-emunits-41`.

- Equations of electrostatics without $\Dvec$ can be converted from SI to Gaussian units by replacing $1/4\pi\epsilon_0$ by 1. Gaussian electrostatic equations (without $\Dvec$) containing $e^2$ can be converted to SI units by replacing $e^2$ by $e^2/4\pi\epsilon_0$. Probably the easiest way to convert other equations in electrostatics and all magnetic equations is to look them up in a table (see \secremunits-5.)

- In Gaussian units, all the fields $\Evec$, $\Bvec$, $\Pvec$, $\Mvec$, $\Dvec$ and $\Hvec$ have the same dimensions. In particular, this means that in Gaussian units one statvolt/cm (the unit of $\Evec$) is identical to 1 Gauss (the unit of $\Bvec$). Also, in Gaussian units the scalar and vector potentials $\Phi$ and $\Avec$ have the same dimensions. This makes it easy to remember where to put the factors of $c$ in Maxwell's equations and other places.

- The electric polarization vector $\Pvec$ is defined as the electric dipole moment per unit volume, and the magnetization vector $\Mvec$ is defined as the magnetic dipole moment per unit volume, in *both* Gaussian and SI units.

- The energy of a electric dipole $\pvec$ or a magnetic dipole $\mvec$ in an external electric or magnetic field is given by $-\pvec\cdot\Evec$ or $-\mvec\cdot\Bvec$ in *both* SI and Gaussian units. However, the dimensions of $\mvec$ and $\Bvec$ are different in the two systems (because of the $1/c$ factor discussed above).

(sec-emunits-5)=

## Dictionary of Electromagnetic Equations in SI and Gaussian Units

It is possible to give general rules for converting an equation from Gaussian to SI units or vice versa, but in practice it is easier to look things up in a dictionary. In this we list the principal equations of electromagnetism in both SI and Gaussian units, apart from equations involving $\Dvec$ and $\Hvec$, which are given in \secremunits-6. The SI equations are on the left and the Gaussian equations on the right. If an equation is the same in both systems, it is listed only once.

The continuity equation:

:::{math}
:label: eq-emunits-3
\del\cdot\Jvec + \frac{\partial \rho}{\partial t} =0\quad\text{(SI,G)}.
:::

Coulomb's law:

:::{math}
:label: eq-emunits-4
F={1\over 4\pi\epsilon_0} {q_1q_2 \over r^2}\quad\text{(SI)},  F={q_1q_2 \over r^2}\quad\text{(G)},
:::

where $F$ is the force between the two particles, directed along the line joining the particles and considered positive if repulsive, negative if attractive. Potential produced by charge distribution $\rho(\rvec)$ in electrostatics:

:::{math}
:label: eq-emunits-5
\Phi(\rvec) = {1\over 4\pi\epsilon_0} \int d^3\rvec' \, {\rho(\rvec') \over |\rvec-\rvec'|}\quad\text{(SI)},  \Phi(\rvec) = \int d^3\rvec' \, {\rho(\rvec') \over |\rvec-\rvec'|}\quad\text{(G)}.
:::

Electric field in terms of potential in electrostatics:

:::{math}
:label: eq-emunits-6
\Evec = -\del\Phi\quad\text{(SI,G)}.
:::

Potential in terms of electric field in electrostatics:

:::{math}
:label: eq-emunits-7
\Phi(\rvec) = -\int_{\rvec_0}^\rvec \Evec(\rvec')\cdot d\rvec'\quad\text{(SI,G)},
:::

where the path connecting $\rvec_0$ and $\rvec$ is arbitrary. Poisson equation in electrostatics:

:::{math}
:label: eq-emunits-8
\del^2\Phi = -{\rho \over \epsilon_0}\quad\text{(SI)},  \del^2\Phi=-4\pi\rho\quad\text{(G)}.
:::

In magnetostatics the current is steady and satisfies $\del\cdot\Jvec=0$. Vector potential in terms of current in magnetostatics:

:::{math}
:label: eq-emunits-9
\Avec(\rvec)={\mu_0\over 4\pi} \int d^3\rvec' \,{\Jvec(\rvec') \over |\rvec-\rvec'|}\quad\text{(SI)},  \Avec(\rvec)={1\over c} \int d^3\rvec' \,{\Jvec(\rvec') \over |\rvec-\rvec'|}\quad\text{(G)},
:::

where $\Avec$ is in Coulomb gauge ($\del\cdot\Avec=0$).

Electric and magnetic fields in terms of potentials in the general (time-dependent) case:

:::{math}
:label: eq-emunits-10
\Evec = -\del\Phi -\frac{\partial \Avec}{\partial t}\quad\text{(SI)},  \Evec = -\del\Phi -{1\over c}\frac{\partial \Avec}{\partial t}\quad\text{(G)},
:::

:::{math}
  \Bvec = \del\cross\Avec\quad\text{(SI,G)}.
:::

These are valid in any gauge.

Gauge transformation:

:::{math}
:label: eq-emunits-12
\Avec' = \Avec+\del g\quad\text{(SI,G)},
:::

:::{math}
:label: eq-emunits-13
  \Phi' = \Phi-\frac{\partial g}{\partial t}\quad\text{(SI)},  \Phi'=\Phi-{1\over c}\frac{\partial g}{\partial t}\quad\text{(G)},
:::

where $g$ is the *gauge scalar* converting one choice of potentials $(\Phi,\Avec)$ into another choice $(\Phi',\Avec')$.

Vacuum Maxwell equations:

:::{math}
:label: eq-emunits-14
\del\cdot\Evec ={\rho\over\epsilon_0}\quad\text{(SI)},  \del\cdot\Evec= 4\pi\rho\quad\text{(G)},
:::

:::{math}
:label: eq-emunits-15
  \del\cross\Bvec = \mu_0\Jvec + \epsilon_0\mu_0\frac{\partial \Evec}{\partial t}\quad\text{(SI)},  \del\cross\Bvec = {4\pi\over c} \Jvec + {1\over c}\frac{\partial \Evec}{\partial t}\quad\text{(G)},
:::

:::{math}
:label: eq-emunits-16
  \del\cross\Evec = -\frac{\partial \Bvec}{\partial t}\quad\text{(SI)},  \del\cross\Evec = -{1\over c}\frac{\partial \Bvec}{\partial t}\quad\text{(G)},
:::

:::{math}
:label: eq-emunits-17
  \del\cdot\Bvec=0\quad\text{(SI,G)}.
:::

Force on a charged particle of charge $q$ in an electric and magnetic field,

:::{math}
:label: eq-emunits-18
\Fvec=q(\Evec+\vvec\cross\Bvec)\quad\text{(SI)},  \Fvec=q\Bigl(\Evec+{1\over c}\vvec\cross\Bvec\Bigr)\quad\text{(G)},
:::

where $\vvec$ is the velocity of the particle.

Electric dipole moment of a static charge distribution $\rho(\rvec)$:

:::{math}
:label: eq-emunits-19
\pvec = \int d^3\rvec \, \rvec \rho(\rvec)\quad\text{(SI,G)}.
:::

The electric polarization vector $\Pvec$ is the electric dipole moment per unit volume in both systems of units. It gives rise to a bound charge density,

:::{math}
:label: eq-emunits-20
\rho_b = -\del\cdot\Pvec.\quad\text{(SI,G)}
:::

Energy of an electric dipole $\pvec$ in an external electric field:

:::{math}
:label: eq-emunits-21
W=-\pvec\cdot\Evec\quad\text{(SI,G)}.
:::

See \secremunits-6 for the electric susceptibility, the permittivity and dielectric constant, and the displacement vector $\Dvec$.

Magnetic dipole moment of static current distribution $\Jvec(\rvec)$:

:::{math}
:label: eq-emunits-22
\mvec={1\over 2} \int d^3\rvec \, \rvec\cross\Jvec(\rvec)\quad\text{(SI)},  \mvec={1\over 2c} \int d^3\rvec \, \rvec\cross\Jvec(\rvec)\quad\text{(G)}.
:::

The magnetization vector $\Mvec$ is the magnetic dipole moment per unit volume in both systems of units. The bound current density $\Jvec_b$ depends on both $\Mvec$ and $\Pvec$ in time-dependent systems,

:::{math}
:label: eq-emunits-23
\Jvec_b = \del\cross\Mvec+\frac{\partial \Pvec}{\partial t}\quad\text{(SI)},  \Jvec_b = c\del\cross\Mvec+\frac{\partial \Pvec}{\partial t}\quad\text{(G)}.
:::

Energy of a magnetic dipole $\mvec$ in an external magnetic field:

:::{math}
:label: eq-emunits-24
W=-\mvec\cdot\Bvec\quad\text{(SI,G)}.
:::

See \secremunits-6 for the magnetic susceptibility, the permeability, and the magnetic field vector $\Hvec$.

The vacuum energy density of the electromagnetic field:

:::{math}
:label: eq-emunits-25
u={\epsilon_0 E^2 \over 2} + {B^2 \over 2\mu_0}\quad\text{(SI)},  u={1\over 8\pi}(E^2+B^2)\quad\text{(G)}.
:::

The vacuum energy flux (Poynting vector):

:::{math}
:label: eq-emunits-26
\Svec={1\over\mu_0} \Evec\cross\Bvec\quad\text{(SI)},  \Svec={c\over 4\pi} \Evec\cross\Bvec\quad\text{(G)}.
:::

The vacuum momentum density $\gvec$ is $(1/c^2)$ times the Poynting vector in both systems of units,

:::{math}
:label: eq-emunits-27
\gvec=\epsilon_0 \Evec\cross\Bvec\quad\text{(SI)},  \gvec={1\over 4\pi c}\Evec\cross\Bvec\quad\text{(G)}.
:::

Elementary treatments of $u$, $\Svec$ and $\gvec$ in the presence of matter are often flawed by the neglect of thermodynamic considerations. Many of the equations found in textbooks involving these quantities are only correct at zero temperature, or under conditions of local thermal equilibrium and adiabaticity.

(sec-emunits-6)=

## The Macroscopic Fields $\Dvec$ and $\Hvec$

The vectors $\Pvec$, $\Dvec$, $\Mvec$ and $\Hvec$ apply in the presence of bulk matter and are defined by some kind of macroscopic and/or statistical averaging process. The fields $\Evec$ and $\Bvec$ can be either microscopic or macroscopic, depending on context.

The definitions of $\Dvec$ in terms of $\Evec$ and $\Pvec$ and of $\Hvec$ in terms of $\Bvec$ and $\Mvec$ in Gaussian and SI units cannot be reconciled by taking the relation {eq}`eq-emunits-2` into account, or (in the case of $\Hvec$, $\Bvec$ and $\Mvec$) the extra factor of $c$ in the definitions of magnetic quantities. Instead, one must take into account an extra factor of $4\pi$ that has been inserted into the definitions in one of the two systems of units. This is an extra layer of confusion in the comparison between the two systems of units. In practice it is probably easiest to look formulas up.

The displacement vector $\Dvec$ in terms of the electric field $\Evec$ and the polarization $\Pvec$:

:::{math}
:label: eq-emunits-28
\Dvec=\epsilon_0\Evec+\Pvec\quad\text{(SI)},  \Dvec=\Evec+4\pi\Pvec\quad\text{(G)}.
:::

In a linear medium, the polarization $\Pvec$ is a linear function of the electric field $\Evec$,

:::{math}
:label: eq-emunits-29
P_i = \epsilon_0 \sum_j (\chi_e)_{ij} \, E_j\quad\text{(SI)},  P_i = \sum_j (\chi_e)_{ij} \, E_j\quad\text{(G)},
:::

where the dimensionless electric susceptibility tensor $(\chi_e)_{ij}$ is characteristic of the medium. In an isotropic medium, $\chi_e$ becomes a scalar, and we have

:::{math}
:label: eq-emunits-30
\Pvec=\epsilon_0 \chi_e \Evec\quad\text{(SI)},  \Pvec=\chi_e \Evec\quad\text{(G)}.
:::

Although $\chi_e$ is dimensionless, it does not have the same value in the two systems of units:

:::{math}
:label: eq-emunits-31
\chi_e^SI = 4\pi \chi_e^G.
:::

In a linear medium (for simplicity taken to be isotropic), $\Dvec$ is proportional to $\Evec$,

:::{math}
:label: eq-emunits-32
\Dvec = \epsilon\Evec\quad\text{(SI,G)},
:::

where $\epsilon$, the permittivity or dielectric constant of the medium, is given in terms of the susceptibility by

:::{math}
:label: eq-emunits-33
\epsilon=\epsilon_0(1+\chi_e)\quad\text{(SI)},  \epsilon=1+4\pi\chi_e\quad\text{(G)}.
:::

The permittivity $\epsilon$ is dimensionless in Gaussian units. The same quantity is sometimes called the *relative* permittivity in SI units, and denoted $\epsilon_r=\epsilon/\epsilon_0$.

The magnetic field vector $\Hvec$ in terms of $\Bvec$ and magnetization $\Mvec$:

:::{math}
:label: eq-emunits-34
\Hvec={1\over\mu_0}\Bvec - \Mvec\quad\text{(SI)},  \Hvec=\Bvec-4\pi\Mvec\quad\text{(G)}.
:::

In a linear medium, the magnetization $\Mvec$ is a linear function of the magnetic field $\Hvec$,

:::{math}
:label: eq-emunits-35
M_i = \sum_j (\chi_m)_{ij} \,H_j\quad\text{(SI,G)},
:::

where the dimensionless magnetic susceptibility tensor $(\chi_m)_{ij}$ is characteristic of the medium. In an isotropic linear medium, $\chi_m$ becomes a scalar, and we have

:::{math}
:label: eq-emunits-36
\Mvec=\chi_m\Hvec\quad\text{(SI,G)}.
:::

Although $\chi_m$ is dimensionless, it does not have the same value in the two systems of units:

:::{math}
:label: eq-emunits-37
\chi_m^SI = 4\pi \chi_m^G.
:::

In a linear medium (for simplicity taken to be isotropic), $\Bvec$ is proportional to $\Hvec$,

:::{math}
:label: eq-emunits-38
\Bvec = \mu\Hvec\quad\text{(SI,G)},
:::

where $\mu$, the permeability of the medium, is given in terms of the magnetic susceptibility by

:::{math}
:label: eq-emunits-39
\mu=\mu_0(1+\chi_m)\quad\text{(SI)},  \mu=1+4\pi\chi_m\quad\text{(G)}.
:::

The permeability $\mu$ is dimensionless in Gaussian units. The same quantity is sometimes called the *relative* permeability in SI units, and denoted $\mu_r=\mu/\mu_0$.

The inhomogeneous, macroscopic Maxwell equations (in the presence of matter) are

:::{math}
:label: eq-emunits-40
\del\cdot\Dvec=\rho_f\quad\text{(SI)},  \del\cdot\Dvec=4\pi\rho_f\quad\text{(G)},
:::

:::{math}
:label: eq-emunits-41
  \del\cross\Hvec=\Jvec_f + \frac{\partial \Dvec}{\partial t}\quad\text{(SI)},  \del\cross\Hvec={4\pi\over c}\Jvec_f+{1\over c} \frac{\partial \Dvec}{\partial t}\quad\text{(G)},
:::

where $\rho_f$ and $\Jvec_f$ are the free charge and current densities, respectively. The homogeneous Maxwell equations are the same as in vacuum, {eq}`eq-emunits-16`--{eq}`eq-emunits-17`.

(sec-emunits-7)=

## Magnetic Moments

As explained in {ref}`ch-spinmagf`, magnetic moments of particles are measured in units of *magnetons*, which generally have the form

:::{math}
:label: eq-emunits-42
\mu = {e\hbar\over 2m}\quad\text{(SI)}, \mu = {e\hbar\over 2mc}\quad\text{(G)},
:::

where $m$ is the mass of the particle. See {eq}`eq-spinmagf-7` and {eq}`eq-spinmagf-22`. Although the formulas for the magnetic moment differ in the two systems of units, the quantity $\mu B$ is an energy in both systems of units, so $\mu$ has dimensions of $Joules/Tesla$ in SI units, and $ergs/Gauss$ in Gaussian units.

(sec-emunits-8)=

## The Physics Behind the Choices

Fundamental physical concepts are independent of any choice of units, but can be lost in the mass of conventions that are employed. Therefore it is worthwhile looking at some of the basic physics of electromagnetism and the rationales that led to choices listed above.

Coulomb's law states that two charges exert a force on one another that is proportional to the product of the charges and inversely proportional to the distance between the charges,

:::{math}
:label: eq-emunits-43
F = k_e {Q_1 Q_2 \over d^2},
:::

where $Q_1$ and $Q_2$ are the charges and $d$ is the distance. The force $F$ is a scalar in this equation but the force vector is directed along a line between the particles and is repulsive (attractive) if $F>0$ ($F<0$).

The constant $k_e$ obviously depends on the units chosen for charge. One possibility is to use an arbitrary definition, for example, the amount of charge deposited on a standard glass rod by three rubs with a standard cat fur, or the amount of charge needed to deposit so many grams of silver in an electrochemical cell. Arbitrary systems of units like this were once common, for example, the original definition of the second was 1/86,400 of a day (the rotational period of the earth), and the meter was originally defined (following the recommendation of the French Academy of Sciences in 1791) as 1/10,000,000 of the distance from the equator to the north pole of the earth. Later these definitions were changed several times to enhance the reproducibility of the standards. Now the second is defined in terms of the period of the radiation produced in a hyperfine transition of the cesium 133 atom, and the meter is defined so that the speed of light in vacuum is 299,792,458 m/sec exactly.

If an arbitrary unit of charge is chosen, then the constant $k_e$ must be measured experimentally. Another possibility is to define the unit of charge so that the constant $k_e$ takes on a simple value. The value $k_e=1$ is especially simple, and this is the choice made in the Gaussian system of units (with the cgs system used for units of distance and force). That is, the statcoulomb is the charge such that two charges of one statcoulomb each at a distance of one centimeter exert a force of one dyne on one another. In SI units, the unit of charge (the Coulomb) causes the electrostatic force constant $k_e$ not to have a particularly simple value, so that insofar as electrostatics is concerned, the definition of the Coulomb appears to be arbitrary. Actually, the Coulomb is defined so that the magnetic force law looks (somewhat) simple, a point we will return to below. In SI units, the constant $k_e$ is written as $1/4\pi\epsilon_0$. Given that the value of $k_e$ is not particularly simple, there is the question as to why this constant is written in such a complicated way. The purpose of the $4\pi$ is to rationalize Maxwell's equations, but the manner of writing $\epsilon_0$ in the constant and the 0-subscript are unfortunate, since they make the simple physics of Coulomb's law look complicated.

Next we consider the definition of the electric field. We begin with an imaginary experiment, in which a set of charges are present in some region of space. We treat these charges as if they were the only charges in the universe (any others are assumed to be far enough away that they have no effect on our experiment). The charges may be in an arbitrary state of motion. We pick out one charge $Q$, call it the “test” charge, and measure the force on it under different circumstances. When $Q$ is stationary, we call the force $\Fvec_e$ on $Q$ the “electric” force, and we find experimentally that it is proportional to $Q$. It also depends on the position $\xvec$ of $Q$ and the time $t$ at which the measurement is made. Then we define the electric field $\Evec(\xvec,t)$ as the force per unit charge on $Q$, so that

:::{math}
:label: eq-emunits-44
\Fvec_e = Q \Evec(\xvec,t).
:::

This definition of electric field (electric force per unit charge) is the same in both SI and Gaussian units.

Suppose now that the test charge $Q$ in our imaginary experiment is in motion with velocity $\vvec$. Then we define the “magnetic force” on $Q$ as the total force $\Fvec$ minus the electric force $\Fvec_e$ (the force that $Q$ would experience if it were stationary),

:::{math}
:label: eq-emunits-45
\Fvec_m = \Fvec-\Fvec_e.
:::

Then we can take the following as experimental facts. First, $\Fvec_m$ (like $\Fvec_e$) is proportional to $Q$. Second, it is linear in the velocity $\vvec$, that is, if we do several measurements with the same $Q$ but with different velocities, we find that if velocity $\vvec_1$ gives magnetic force $\Fvec_{m1}$ and velocity $\vvec_2$ gives magnetic force $\Fvec_{m2}$, then velocity $a_1\vvec_1 + a_2\vvec_2$ gives magnetic force $a_1 \Fvec_{m1} + a_2 \Fvec_{m2}$. Third, the magnetic force is orthogonal to the velocity, $\vvec \cdot \Fvec_m = 0$. The first and second properties mean that there is a matrix $\Mmat$, a function of the position $\xvec$ of $Q$ and the time $t$ of the measurement, such that

:::{math}
:label: eq-emunits-46
\Fvec_m = Q \Mmat \vvec,
:::

while the third property means that $\Mmat$ is antisymmetric, $M_{ij} = -M_{ji}$. An antisymmetric matrix has 3 independent components, which are conveniently expressed in terms of a vector $\Xvec=(X_x, X_y, X_z)$ by

:::{math}
:label: eq-emunits-47
\begin{aligned}
\Mmat = \begin{pmatrix} 0 & X_z & -X_y \\ -X_z & 0 & X_x \\ X_y & -X_x & 0 \\\end{pmatrix},
\end{aligned}

:::

so that {eq}`eq-emunits-46` has the form

:::{math}
:label: eq-emunits-48
\Fvec_m = Q \vvec \cross \Xvec.
:::

Now we define the magnetic field. Unlike the definition of the electric field, the magnetic field is defined differently in the SI and Gaussian systems. In the SI system, the magnetic field is defined by $\Bvec = \Xvec$, whereas in the Gaussian system, it is defined by $\Bvec = c\Xvec$. This explains the extra factor of $c$ in the Gaussian force law {eq}`eq-emunits-18`. The Gaussian definition causes $\Evec$ and $\Bvec$ to have the same dimensions (the statvolt/cm and the Gauss are actually identical units).

In these imaginary experiments we have not said how the force on the test charge $Q$ is specified by the rest of the charges (the “source” charges). Two cases are simple. If the source charges are stationary (and have been so for a long time), then the electric force on the test charge is given by

:::{math}
:label: eq-emunits-49
\Fvec_e = k_e Q \int d^3\xvec' \, \rho(\xvec') {\xvec-\xvec' \over | \xvec-\xvec'|^3},
:::

where $\rho$ is the source charge density, $k_e$ is the electric constant introduced in {eq}`eq-emunits-43` and $\xvec$ is the position of the test charge. If the sources charges are in motion but the source current is steady (and has been so for a long time), then the magnetic force on the test charge is given by

:::{math}
:label: eq-emunits-50
\Fvec_m = k_m Q \vvec \cross \int d\xvec'\, \Jvec(\xvec') \cross {\xvec-\xvec' \over | \xvec-\xvec'|^3},
:::

where $\Jvec$ is the source current density and $k_m$ is a new constant (the magnetic force constant). Equations~{eq}`eq-emunits-49` and {eq}`eq-emunits-50` have been written purely in terms of forces, without reference to the electric or magnetic fields (the latter of which is defined differently in the two systems of units), because we wanted to have expressions for the electric and magnetic forces that were as independent of conventions as possible. No assumptions have been made about the unit of charge or the definitions of the electric and magnetic fields in these equations.

Taking the ratio, dimensionally speaking, of {eq}`eq-emunits-49` and {eq}`eq-emunits-50` shows that the ratio $k_e/k_m$ has dimensions of $velocity^2$. Therefore the value of this ratio is independent of the choice made for the unit of charge. In fact, both $k_e$ and $k_m$ can be measured in laboratory experiments (using some arbitrary unit of charge, if necessary), and their ratio computed. This was done in the early history of electromagnetism, and it was found that

:::{math}
:label: eq-emunits-51
{k_e \over k_m} = c^2,
:::

to experimental accuracy. Now we believe that the relation {eq}`eq-emunits-51` is exactly true (at least, it is a fundamental tenet of electromagnetic theory). Thus, the electric and magnetic force constants are not independent. In Gaussian units, {eq}`eq-emunits-51` implies $k_m = 1/c^2$, and in SI units, where $k_m$ is usually written $\mu_0/4\pi$, it implies $\epsilon_0 \mu_0 = 1/c^2$. The situation is summarized in {ref}`tbl-emunits-4`.

:::{table} Electric and magnetic force constants in the different systems of units. \par
:label: tbl-emunits-4

| Units | $k_e$ | $k_m$ |
|:---:|:---:|:---:|
| Gaussian | $1$ | $\frac{1}{c^2}$ |
| SI | $\frac{1}{4\pi\epsilon_0}$ | $\frac{\mu_0}{4\pi}$ |

:::
In SI units, the unit of charge (the Coulomb) is chosen so as to make the magnetic force constant $k_m=\mu_0/4\pi$ take on the value $10^{-7}$ (exactly). One could say this is a way of making the magnetic force law look simple (instead of the electric force law, the choice made in Gaussian units). Of course, $10^{-7}$ is not as simple as 1, but the result is that the Ampere (one Coulomb/sec) is a reasonable unit in simple laboratory experiments and common electrical devices.
