---
title: "17. Hydrogen and Hydrogen-Like Atoms"
---
(ch-hydrogen)=

# 17. Hydrogen and Hydrogen-Like Atoms

(sec-hydrogen-1)=

## Introduction

There is an amazing amount of physics in the hydrogen atom. The simplest model, the electrostatic model that we consider in these notes, is an exactly solvable problem that reveals the gross structure of the hydrogen atom and explains the formulas of Balmer and Rydberg for its spectral lines. Later, in {ref}`ch-finestruc`, we will consider corrections due to relativity and spin, which produce the fine structure in the spectrum of hydrogen as well as giving us an introductory view of relativistic quantum mechanics. Then, in {ref}`ch-hyperfine`, we will consider the magnetic interactions between the atomic electron and the magnetic dipole moment of the nucleus, which are otherwise known as hyperfine effects. These are important for many applications ranging from atomic clocks to astrophysics. Later we study the Lamb shift, a shift in the atomic energy levels due to the interaction of the atomic electron with the quantized electromagnetic field, which is most notable in the case of hydrogen where it splits the degeneracy of the $2s$ and $2p$ states. Finally, in {ref}`ch-spdirac`{} we consider the exact solution of the hydrogen atom for the Dirac equation, the relativistic wave equation for the electron, as well as (in {ref}`ch-foldyw`) the expansion of solutions of the Dirac equation in powers of $v/c$, recovering thereby all the fine structure effects examined earlier in {ref}`ch-finestruc`. Hydrogen is also a basic model for the physics of atoms, providing a context and a reference for all of atomic physics and as well as for the physics of collections of atoms, including molecules and most systems of interest in condensed matter physics.

In addition to hydrogen itself in these notes we will also consider *hydrogen-like* atoms, that is, atoms with a nucleus of some charge and a single electron. This includes the ion $\\textHe^+$, singly ionized helium, also called hydrogen-like helium; the ion $\\textLi^{++}$, doubly ionized lithium, also called hydrogen-like lithium, etc. As usual in atomic physics, we denote the nuclear charge by $Z$, which ranges from 1 for hydrogen to 92 for uranium and beyond.

(sec-hydrogen-2)=

## Hydrogen in the History of Quantum Mechanics

Hydrogen played a central role in the history of quantum mechanics. By the 1880's Balmer and Rydberg had found an empirical formula fitting the observed spectral lines in hydrogen,

:::{math}
:label: eq-hydrogen-1
{1\over\lambda} = R\Bigl({1\over n^2} - {1\over m^2}\Bigr),
:::

where $\lambda$ is the wavelength of the radiation emitted, $R$ is a constant that can be determined from the spectroscopic data, and $n$ and $m$ are positive integers such that $n<m$. In 1913 Bohr showed that the Rydberg formula {eq}`eq-hydrogen-1` could be explained by demanding that the orbits of the electron in hydrogen are quantized, that is, restricted to those for which the classical action is an integer multiple of $h=2\pi\hbar$, and that when atoms jump from one quantized orbit to another, the frequency of the photon emitted is given by Einstein's formula $\Delta E = \hbar\omega$. This was not obvious, because this frequency is not the same as the orbital frequency of either the old or new orbit. Bohr's theory showed that the Rydberg constant $R$ in {eq}`eq-hydrogen-1` was given by

:::{math}
:label: eq-hydrogen-2
R={me^4 \over 4\pi\hbar^3 c},
:::

a result that agreed well with the spectroscopic data. The value of $\hbar$ was known by that time due to the work of Planck and others on black body radiation. Bohr's theory explained other things as well, such as the dependence of the Rydberg constant on the nuclear charge $Z$ in single-electron atoms [the formula {eq}`eq-hydrogen-2` applies only to hydrogen].

In 1916 Sommerfeld used a relativistic generalization of Bohr's method of quantizing orbits to explain (apparently) the fine structure of hydrogen, although we now know that this calculation gave the correct answer somewhat by accident. Sommerfeld did not know about spin and the version of the old quantum theory he was using had some inadequacies, but by a kind of a miracle the answers turned out to agree with experiment. In spite of these misconceptions, however, Sommerfeld was correct in realizing that the fine structure was a relativistic correction to the dynamics of hydrogen.

When the first version of genuine quantum mechanics appeared 1925, in the form of Heisenberg's matrix mechanics, one of the first problems solved was the hydrogen atom. It is entirely nontrivial to do this within the framework of matrix mechanics, but the solution was given in 1926 in a brilliant paper by Pauli. Pauli had been primed for the task by his earlier work on the hydrogen molecule-ion ($H_2^{+}$) in the old quantum theory. Soon afterward the Schr\"odinger equation and wave mechanics appeared, and Schr\"odinger himself solved his equation for the hydrogen atom, much along the same lines as presented in these notes.

By this time the concept of spin had been introduced and comprehended much in its modern form, by Kronig, Pauli and others, and it was understood that spin was a part of some as yet incomplete understanding of relativistic quantum mechanics. A major breakthrough was made by Dirac in 1927, with his relativistic wave equation for the electron. Dirac did not solve his equation for the hydrogen atom, instead that was done by Darwin in 1928. This exact solution of the Dirac equation reproduced all of the fine structure effects in hydrogen to within the experimental accuracy available at that time. (When asked once why he did not solve his own equation for hydrogen, Dirac replied that he was afraid to, for fear that the answers would come out wrong and ruin his theory.)

The Dirac equation predicts an exact degeneracy between the $2s_{1/2}$ and $2p_{1/2}$ levels of hydrogen, but spectroscopists in the 1930's began to suspect that there might be a splitting between them, one that was just beyond the resolution available with optical techniques. At the same time several theorists began to suspect that this splitting was due to the interaction of the atomic electron with the quantized electromagnetic field, one in which the atomic electron first emits and then reabsorbs a photon. The problem was that quantum electrodynamics of that day inevitably led to infinities in all higher order perturbation calculations, including this one, so that it was impossible to get a theoretical number without overcoming the difficulty of the infinities. But after World War II experimentalists pushed the story forward with dramatic new results. In 1947, using newly developed microwave techniques, Lamb and Retherford not only verified that there is indeed a splitting between these levels, but they also measured it to high accuracy. On hearing about this, Hans Bethe carried out a calculation of the Lamb shift, finding good agreement with experiment. Bethe's calculation was nonrelativistic and somewhat heuristic, but his calculation did show that it was possible to make sense of the difference between infinite quantities to obtain finite answers that agree with experiment. Then the challenge was on to do the same calculation correctly, with fully relativistic quantum mechanics and the new ideas of renormalization. This was carried out by French and Weisskopf, Feynman, and others, providing one of the earliest and most dramatic successes of renormalization theory.

(sec-hydrogen-3)=

## Atomic Units

Atomic units are units in which $e=m=\hbar=1$, where $m$ is the electron mass and $e$ is the charge of the proton, as usual in this course. They are particularly convenient in atomic problems as a way of getting rid of the clutter of constants that would appear in other units, and for helping us visualize the order of magnitude of various expressions. For example, the atomic unit of distance is the Bohr radius, the size of the hydrogen atom. Similarly, the atomic unit of velocity is the velocity of the electron in the ground state of hydrogen, the unit of energy is twice the ionization potential of hydrogen, the unit of frequency is the frequency of the electron's orbit in the ground state of hydrogen, etc. There is a unique unit of distance, energy, time, momentum, etc., that can be constructed out of $e$, $m$ and $\hbar$, so that all of these become just 1 in atomic units. These quantities were given in {ref}`tbl-cenforce-1`, an expanded version of which we present here in {ref}`tbl-hydrogen-1`.

:::{list-table} Atomic units of distance, energy, time, etc.
:label: tbl-hydrogen-1
:header-rows: 1

* - Dimension
  - Unit
  - Value
* - distance
  - $a_0=\hbar^2/me^2$
  - $0.5\,{\AA}$
* - energy
  - $K_0=e^2/a_0=me^4/\hbar^2$
  - $27\,\mathrm{eV}$
* - velocity
  - $v_0=e^2/\hbar$
  - $\alpha c \approx c/137$
* - momentum
  - $p_0=me^2/\hbar$
  - $mv_0$
* - angular momentum
  - $L_0=\hbar$
  - $\hbar$
* - frequency
  - $\omega_0=me^4/\hbar^3 =K_0/\hbar$
  - $1/T_0$
* - time
  - $T_0=\hbar^3/me^4=1/\omega_0$
  - $2.4\times 10^{-17}\,\mathrm{sec}$

:::
Notice that the energy of the ground state of hydrogen is $-1/2$ in atomic units while the period of the electron orbit in the ground state is $2\pi$ (that is, $2\pi T_0 \approx 1.5\times 10^{-16}\, \mathrm{sec}$ in ordinary units). Notice also that the speed of light in atomic units is

:::{math}
:label: eq-hydrogen-3
c= {1\over\alpha} \approx 137 \qquad  \text{(atomic units)}.
:::

(sec-hydrogen-4)=

## The Electrostatic Model

In these notes we shall use the electrostatic model for hydrogen-like atoms, in which the electron and nucleus interact by an electrostatic force, which is determined by the instantaneous positions of the particles. The electrostatic model is an approximation to electrodynamics in which one neglects the retardation in the communication between the particles, magnetic effects, and the effects of radiation. As a part of the electrostatic model we shall also assume the electron motion is nonrelativistic, something that is justified in the case of hydrogen, for which the velocity of the electron in the ground state is $\alpha c < 1\%\,c$, as shown by {ref}`tbl-hydrogen-1`. We have no choice in this matter, since we have only studied the nonrelativistic Schr\"odinger equation so far, and we do not know how to treat fully relativistic quantum problems. Under these assumptions, we have a two-body problem as described in {ref}`sec-cenforce-9`, in which the potential is

:::{math}
:label: eq-hydrogen-4
V(r)=-{Ze^2\over r}.
:::

Thus, version~2 [see {eq}`eq-cenforce-11`] of the radial Schr\"odinger equation is

:::{math}
:label: eq-hydrogen-5
-{\hbar^2\over 2\mu} {d^2f\over dr^2} +\Bigl[ {\ell(\ell+1)\hbar^2 \over 2\mu r^2} -{Ze^2\over r}\Bigr]f(r) = Ef(r),
:::

where $\mu$ is the reduced mass of the electron-nucleus system. In the case of ordinary hydrogen with a proton as the nucleus, the reduced mass $\mu$ differs from the true electron mass $m$ by less than one part in $10^3$, and for heavier atoms the fraction is even smaller. We shall retain the distinction between $m$ and $\mu$, but numerically they are very close.

(sec-hydrogen-5)=

## Solving the Radial Schr\"odinger Equation

To put this equation into dimensionless form we shall adopt what we call *modified atomic units*, which are obtained from atomic units by making the replacements $m\to\mu$ and $e^2 \to Ze^2$. Modified atomic units are units in which $\mu=\hbar=\sqrt{Ze^2}=1$. The change $m\to\mu$ has only a small effect, but $e^2 \to Ze^2$ gives all the units a dependence on $Z$, which is worth noting. Modified atomic units are summarized in {ref}`tbl-hydrogen-2`.

:::{list-table} Modified tomic units of distance, energy, time, etc., useful for treating hydrogen-like atoms.
:label: tbl-hydrogen-2
:header-rows: 1

* - Dimension
  - Unit
  - Value
* - distance
  - $a=\hbar^2/\mu Ze^2$
  - $\approx a_0/Z$
* - energy
  - $K=\mu Z^2e^4/\hbar^2$
  - $\approx Z^2K_0$
* - velocity
  - $v=Z e^2/\hbar$
  - $Zv_0=Z\alpha c \approx (Z/137)c$
* - frequency
  - $\omega=\mu Z^2e^4/\hbar^3 =K/\hbar$
  - $\approx Z^2\omega_0$
* - time
  - $T=\hbar^3/\mu Z^2e^4$
  - $\approx T_0/Z^2$

:::
From {ref}`tbl-hydrogen-2` we see that the size of a hydrogen-like atom scales as $1/Z$, while the energies scale as $Z^2$. Notice in particular the velocity, which scales as $Z$. For hydrogen or other small-$Z$ elements near the beginning of the periodic table this velocity is small compared to the speed of light. But near the end of the periodic table the electron in hydrogen-like ions is becoming relativistic. For example, for hydrogen-like uranium ($Z=92$) we have $v\approx (92/137)c \approx 0.67\,c$. We can expect the same thing for $K$-shell (inner shell) electrons in heavy atoms, even when all the other electrons are present (that is, for the neutral atoms). We see that the nonrelativistic Schr\"odinger equation is not a good starting approximation for heavy atoms.

:::{figure} images/hydrogen-fig01.png
:label: fig-hydrogen-1
:width: 80%

The true, centrifugal and effective potentials for hydrogen, for the case $\ell=1$. Energy (vertical axis) and radius (horizontal axis) are measured in modified atomic units.
:::

Returning to the radial Schr\"odinger equation {eq}`eq-hydrogen-5`, we sketch the effective potential, as shown in {ref}`fig-hydrogen-1`. The positive centrifugal potential dominates for small $r$, while the negative true potential dominates for large $r$. The competition between the two produces a well in the effective potential, as shown in the figure, and we can expect bound states. In fact, the well supports an infinite number of bound states, for all values of $\ell$. This is because of the long tail, which dies off only as $1/r$. One can see from the figure that there are also unbound states with energies in the range $0\le E<\infty$. We will be mainly interested in the bound states in this set of notes, but one must remember that there are also unbound states. In particular, a resolution of the identity requires both the bound states and unbounded states (the bound state wavefunctions by themselves do not form a complete set). See {eq}`eq-hilbert-110`.

In modified atomic units, the radial Schr\"odinger equation {eq}`eq-hydrogen-5` becomes

:::{math}
:label: eq-hydrogen-6
{d^2 f \over dr^2} + \Bigl[ -{\ell(\ell+1) \over r^2} + {2\over r}+2E\Bigr]f = 0.
:::

To find the bound states (for which $E<0$) it is convenient to introduce a parameter

:::{math}
:label: eq-hydrogen-7
\nu={1\over\sqrt{-2E}}.
:::

Next, to transform the radial wave equation to a standard form, we first define a modified radial variable,

:::{math}
:label: eq-hydrogen-8
\rho={2r\over\nu},
:::

whereupon {eq}`eq-hydrogen-6` becomes

:::{math}
:label: eq-hydrogen-9
{d^2 f\over d\rho^2} + \Big[ -{\ell(\ell+1)\over \rho^2} + {\nu\over\rho} -{1\over4} \Bigr]f=0.
:::

To obtain the asymptotic (large $\rho$) behavior of the solution $f$, we neglect the terms in $1/\rho^2$ and $1/\rho$, whereupon we find $f\sim e^{\pm\rho/2}$. The solution that goes as $e^{\rho/2}$ is not normalizable, so we want the one that goes as $e^{-\rho/2}$ at large $\rho$.

This leads us to define a new radial wave function $g$ by

:::{math}
:label: eq-hydrogen-10
f(\rho)=\rho^{\ell+1}\, e^{-\rho/2} \, g(\rho),
:::

where we have also removed a factor of $\rho^{\ell+1}$ to account for the behavior of $R(r)$ at the origin (see {ref}`sec-cenforce-5`) as well as the extra factor of $r$ connecting $f$ and $R$ [see {eq}`eq-cenforce-10`]. Substituting this into {eq}`eq-hydrogen-6` gives an equation for $g$,

:::{math}
:label: eq-hydrogen-11
\rho {d^2 g \over d\rho^2} + (2\ell+2-\rho) \dod{g}{\rho} +(\nu-\ell-1)g=0.
:::

If we seek a power series solution for this equation, we find that if the power series does not terminate, then $g(\rho)$ diverges as $e^\rho$ as $\rho\to\infty$, thereby overwhelming the factor $e^{-\rho/2}$ in {eq}`eq-hydrogen-10` and causing the solution $f$ to diverge. Such solutions are not normalizable and not acceptable as bound states. But we find that if $\nu$ is an integer $\ge\ell+1$, then the power series solution of {eq}`eq-hydrogen-11` terminates, that is, it is a polynomial. In this case the wave function is normalizable, and we have a bound state solution. To represent these bound states, we will henceforth write $n$ instead of $\nu$, where for given $\ell$, $n$ takes on the values

:::{math}
:label: eq-hydrogen-12
n=\ell+1, \ell+2, \ldots.
:::

The degree of the polynomial solution $g(\rho)$ to {eq}`eq-hydrogen-11` is $n-\ell-1$. The integer $n$ is called the *principal quantum number*. Now {eq}`eq-hydrogen-7` gives the energy as a function of $n$,

:::{math}
:label: eq-hydrogen-13
E_n = -{1\over 2n^2}.
:::

This is in modified atomic units; we must multiply by $K$ (see {ref}`tbl-hydrogen-2`) to convert to ordinary units. We see that there are an infinite number of bound states for each value of $\ell$.

{eq}`eq-hydrogen-11` is a second order differential equation that must have two linearly independent solutions, of which the power series solution we have discussed in the preceding paragraph is only one. We should investigate the other solutions. To obtain them we use the method of Frobenius, in which one seeks a solution of the form,

:::{math}
:label: eq-hydrogen-14
g(\rho) = \rho^s \sum_{k=0}^\infty a_k\,\rho^k,
:::

that is, a power series multiplied by a fixed power, which, if negative or fractional, indicates a singularity at $\rho=0$. In fact, plugging {eq}`eq-hydrogen-14` into {eq}`eq-hydrogen-11` shows that one solution has $s=0$, which is the power series mentioned above; in that case the power series terminates if $\nu=n$ satisfies {eq}`eq-hydrogen-12`. The other solution has $s=-2\ell-1$, which has a singularity at the origin. This solution leads the the small $r$ dependence of the radial wave function $R(r) \sim 1/r^{\ell+1}$, which was discussed in general terms in {ref}`sec-cenforce-5`. That solution is nonphysical and is rejected. There remain only the polynomial solutions with $\nu=n$.

The transformations leading up to {eq}`eq-hydrogen-11` have put it into the standard form for the differential equation satisfied by the associated Laguerre polynomials. See Abramowitz and Stegun, Chapter~22, and table entry (22.6.15). Abramowitz and Stegun denote the associated Laguerre polynomials by $L_n^{(\alpha)}$; they are polynomials of degree $n$ in $x$, parameterized by $\alpha$ (with reference to their notation, note that their $n$ is not the same as ours).

Writing out the standard differential equation for the Laguerre polynomials and comparing it to {eq}`eq-hydrogen-11`, we find the solution,

:::{math}
:label: eq-hydrogen-15
g(\rho) = L_{n-\ell-1}^{2\ell+1}(\rho),
:::

so that

:::{math}
:label: eq-hydrogen-16
f_{n\ell}(r) = \rho^{\ell+1}\,e^{-\rho/2}\, L_{n-\ell-1}^{2\ell+1}(\rho),
:::

where we have appended the quantum numbers $n\ell$ to the radial wave function.

(sec-hydrogen-6)=

## The Normalization

To normalize the radial wave functions we use the generating function of the associated Laguerre polynomials. This is a somewhat technical exercise, which we now outline. For the generating function, see Abramowitz and Stegun, table entry (22.9.15), which we write in the form

:::{math}
:label: eq-hydrogen-17
G(\rho,z) = {1\over (1-z)^{\alpha+1}} \exp\Bigl[-\rho{z\over 1-z}\Bigr] =\sum_{p=0}^\infty z^p \, L^\alpha_p(\rho),
:::

where we have changed the notation slightly to avoid conflict between our notation and that of Abramowitz and Stegun. Function $G$ is the generating function of the associated Laguerre polynomials, and {eq}`eq-hydrogen-17` can be regarded as the definition of those polynomials. We write out {eq}`eq-hydrogen-17` again, with $p\to q$ and $z\to z'$, and multiply both sides together. Then we multiply both sides by $\rho^{\alpha+1}\,e^{-\rho}$ and integrate from $\rho=0$ to $\rho=\infty$. On the left we obtain

:::{math}
:label: eq-hydrogen-18
{1\over [(1-z)(1-z')]^{\alpha+1}} \int_0^\infty d\rho \, \rho^{\alpha+1}\, \exp\Bigl[-\rho\Bigl(1+{z\over 1-z} + {z'\over 1-z'} \Bigr)\Bigr] = (\alpha+1)! {(1-z)(1-z') \over (1-zz')^{\alpha+2}},
:::

while on the right we obtain

:::{math}
:label: eq-hydrogen-19
\sum_{p,q=0}^\infty z^p z^{\prime q}\, \int_0^\infty d\rho\, \rho^{\alpha+1}\, e^{-\rho}\, L^\alpha_p(\rho)\, L^\alpha_q(\rho).
:::

Expanding the left hand side {eq}`eq-hydrogen-18` in a double power series in $z$ and $z'$ and picking out the term in $z^p z^{\prime p}$ and equating it to the same term on the right, we find the integral,

:::{math}
:label: eq-hydrogen-20
\int_0^\infty d\rho \, \rho^{\alpha+1}\, e^{-\rho} \, [L^\alpha_p(\rho)]^2 = (2p+\alpha+1) {(p+\alpha)! \over p!}.
:::

This allows us to normalize the radial wave functions {eq}`eq-hydrogen-16`, where we set $\alpha=2\ell+1$ and $p=n-\ell-1$. We write the result in terms of the version~1 radial wave function,

:::{math}
:label: eq-hydrogen-21
R_{n\ell}(r)={2\over n^2} \, \sqrt{(n-\ell-1)! \over (n+\ell)!} \,\rho^\ell\, e^{-\rho/2} \, L^{2\ell+1}_{n-\ell-1}(\rho),
:::

where we recall that $\rho=2r/n$ and that the result is expressed in modified atomic units.

Now the orthonormality conditions for the radial wave functions are

:::{math}
:label: eq-hydrogen-22
\int_0^\infty r^2 \, dr \, R_{n\ell}(r) R_{n'\ell}(r) = \delta_{nn'}.
:::

Notice that the radial wavefunctions are orthonormal only for fixed $\ell$; there is no simple orthonormality condition connecting radial wave functions of different $\ell$. The three-dimensional wave functions $R_{n\ell}(r)Y_{\ell m}(\theta,\phi)$ are orthogonal for different $\ell$ because of the orthogonality of the $Y_{\ell m}$'s.

Beware in comparing these results to other authors (e.g., Schiff), who use different conventions for the associated Laguerre polynomials. Here we have followed Abramowitz and Stegun.

The generating function can also be used to compute expectation values of powers of $r$, that is,

:::{math}
:label: eq-hydrogen-23
\xpecval{r^k} = \int_0^\infty r^2\,dr\, r^k\, |R_{n\ell}(r)|^2,
:::

The process is somewhat lengthy and not very illuminating, however, and the calculation is somewhat different for every different value of $k$. But if we do this for the special case $k=-2$, for which the answer is given by {eq}`eq-hydrogen-33`, then we can use the Kramers relation (see Prob.~\prbrhydrogen-1) to obtain $\xpecval{r^k}$ for all other integer values of $k$.

(sec-hydrogen-7)=

## The Energy Levels

In central force problems the radial wave equation is parameterized by $\ell$, so we get a different set of energy levels for each $\ell$. It is often convenient to plot these on a diagram in which the levels for each value of $\ell$ are arranged in a column labeled by $\ell$. Effectively this is a plot with energy on the vertical axis and angular momentum on the horizontal axis. Doing this for hydrogen, we obtain {ref}`fig-hydrogen-2`.

:::{figure} images/hydrogen-fig02.png
:label: fig-hydrogen-2
:width: 80%

The energy levels of a hydrogen-like atom in the electrostatic model, with energy measured in modified atomic units.
:::

As seen at the top of {ref}`fig-hydrogen-2`, the angular momentum quantum numbers $\ell=0,1,2,3,\ldots$ are associated with a series of code letters, $s$, $p$, $d$, $f$, etc. After $f$ the code letters follow the letters of the alphabet, $g$, $h$, $i$, etc. These have only a historical significance, but they are used universally in spectroscopic notation so one must know them and how to translate them into angular momentum values. The energy along the vertical axis is given in in modified atomic units (see {ref}`tbl-hydrogen-2`). The energy levels within a given column are sequenced by principal quantum number $n$, which according to {eq}`eq-hydrogen-12` begins with $\ell+1$ at the bottom of the column and increases by one at each successive higher level in the column. An infinite number of these levels accumulates below $E=0$, which is the continuum threshold. The spectroscopic notation for a given level in a given column is $n\ell$, where $\ell$ is replaced by the one of the code letters, $s$, $p$, $d$, $f$, etc. For example, the ground state is denoted $1s$.

We can make a plot like this for any central force problem. Since the radial Schr\"odinger equation is parameterized by $\ell$, we get in effect a different spectrum for each value of $\ell$. For a randomly chosen central force potential, these different spectra are effectively unrelated to one another, and there is very little chance that a level in one column will coincide with a level in another. At least, not exactly; of course they can come very close, and they will do so in regions where the energy levels are closely spaced. But an exact coincidence is unlikely.

A unique feature of hydrogen, however, is that there is an exact degeneracy among the levels of a given $n$ across the different columns. That is because the energies, given by {eq}`eq-hydrogen-13`, depend only on $n$ and are independent of $\ell$. This degeneracy is not due to rotational invariance, which only explains why the energies are independent of the magnetic quantum number $m$. Instead, it is due to the fact that hydrogen, in the electrostatic model, possesses a larger symmetry group than $SO(3)$, the group of rotations, which is the symmetry of any central force problem. Hydrogen, as it turns out, has the symmetry group $SO(4)$ for the bound states, the group of proper rotations in a Euclidean space of four dimensions. These four dimensional rotations do not act solely on the configuration space coordinates of the hydrogen atom, that is, the $x$, $y$ and $z$ coordinates of the electron; instead, they involve nontrivial transformations that affect both the position and the momentum of the electron. The generators of this $SO(4)$ symmetry include $\Lvec$ (which of course generates ordinary rotations) and the Runge-Lenz vector. We will not go into the details of this extra symmetry of the hydrogen atom, but a readable introduction to it is given by Schiff.

The total degeneracy of the energy level $E_n$ can be obtained by summing degeneracies horizontally across the levels of {ref}`fig-hydrogen-2`. Each level shown in the figure is actually $2\ell+1$ degenerate levels, because of the magnetic quantum number which runs over $m=-\ell,\ldots,+\ell$. Therefore the total degeneracy is

:::{math}
:label: eq-hydrogen-24
degen(E_n) = \sum_{\ell=0}^{n-1} 2\ell+1= n^2.
:::

(sec-hydrogen-8)=

## Breaking the Extra Degeneracy

As we have explained, the degeneracy between states of the same $n$ but different $\ell$ is not a general feature of central force potentials but rather is unique to hydrogen. Therefore any central force perturbation to the Coulomb potential will break the degeneracy in $\ell$ while maintaining that in $m$. We now present two physically interesting ways of doing this.

One concerns is the *volume effect*, which is explored in detail in Prob. {ref}`prob-pertth-1`. The volume effect is due to the fact that the nucleus is not a point charge, but rather has its charge spread out over a finite volume. This modifies the energy levels of the atom somewhat.

The radius of a proton or a neutron is roughly $10^{-13}\,cm$, and when nucleons are bound to one another in a compound nucleus they behave roughly like hard spheres in contact. Thus, a simple model of the nucleus is a sphere of radius $A^{1/3} \times 10^{-13}\,cm$, where $A$ is the total number of nucleons, over which the total charge $Ze$ is spread out in some manner. The charge density dies off rapidly outside the nuclear radius, so that well outside the nucleus the electrostatic potential is the Coulomb potential, $Ze/r$. Inside the nucleus, however the true potential deviates significantly from the Coulomb potential, and, in particular, it does not diverge as $r\to0$.

Taking into account the spread in the nuclear charge, the potential is not exactly a Coulomb potential, so we should not expect to see an exact degeneracy in $\ell$. But the nucleus is very small compared to an atom, for example, it is nearly $10^5$ times smaller in the case of hydrogen. So the region over which the potential deviates from the Coulomb potential is relatively very small. Given the behavior of wave functions near the origin, as discussed in {ref}`sec-cenforce-5`, we can expect $s$-waves (with $\ell=0$) to be most strongly affected by the volume effect. This is indeed the case; the states with higher values of $\ell$ are hardly affected. But overall, there is a dependence on $\ell$ introduced into energy levels, thereby breaking the $\ell$-degeneracy of the pure Coulomb field.

:::{figure} images/hydrogen-fig03.png
:label: fig-hydrogen-3
:width: 80%

Energy level diagram for sodium (source: NIST database). Energy $E=0$ is the ionization limit for a single electron (one electron at infinity plus a $\\textNa^+$ ion in its ground state). Only the few lowest lying levels are shown. These illustrate the strong dependence of the energy $E_{n\ell}$ on the quantum number $\ell$.
:::

(sec-hydrogen-9)=

## Central Force Model of Alkali Atoms

The second example is a simple model of the alkali atoms. Neutral alkali atoms such as $\rm Na$ have one electron in the outer, valence shell, which surrounds a core of completely filled subshells containing $Z-1$ electrons. A model of such atoms treats the inner core as a spherically symmetric distribution of negative charge that screens the nuclear charge. The amount of screening depends on the radius; as $r\to 0$, the full, unscreened charge of the nucleus is seen, whereas when the valence electron is pulled far away from the core, it leaves behind an ion of $+1$ unit of charge. We can use Gauss' law to find the electric field (which under our assumptions has only a radial component) seen by the valence electron,

:::{math}
:label: eq-hydrogen-25
E(r) = {eZ_eff(r) \over r^2},
:::

where $Z_eff(r)$ is the total charge inside radius $r$. It has the limiting forms,

:::{math}
:label: eq-hydrogen-26
\begin{aligned}
Z_eff(r) \to \begin{cases} Z, & r\to 0, \\ 1, & r\to\infty. \\\end{cases}
\end{aligned}

:::

This gives the potential for the valence electron,

:::{math}
:label: eq-hydrogen-27
V(r) = -e^2 \int_r^\infty {Z_eff(r) \over r^2} \, dr.
:::

There is no simple formula for $Z_eff(r)$ or for $V(r)$.

Like the Coulomb potential, the screened potential {eq}`eq-hydrogen-27` goes to $-\infty$ as $r\to0$, and to 0 as $r\to\infty$. But the manner in which it does so is not like any given Coulomb potential with a fixed $Z$, and if it is regarded as a perturbation of a Coulomb potential with a fixed $Z$, then the perturbation is not small. Thus, we should expect some strong breaking of the degeneracy in $\ell$ that is present in hydrogen-like atoms.

The energy level diagram for sodium, shown in {ref}`fig-hydrogen-3`, shows that this is the case. In sodium the principal quantum number begins with $n=3$ because the two inner shells are filled. Notice that the $3p$ level is not at all close to the $3s$ level, in fact, the transition $3p\to 3s$ is the sodium $D$-line, the strong yellow line that makes most fires yellow. It is an optical transition, with an energy comparable to transitions between states of different $n$ in hydrogen. Note, however, that the $4d$ and $4f$ levels of sodium are nearly degenerate. This is because when $\ell$ is large the classical orbit is nearly circular, so that if $n$ is large, too, then the electron's orbit remains well outside the atomic core. Out in that region, the potential $V(r)$ is approximately that of hydrogen. States of small $\ell$, even when $n$ is large, involve orbits that dive into the core where the non-Coulomb nature of the potential is felt.

(sec-hydrogen-10)=

## The Wave Functions

Returning to hydrogen, we can obtain an explicit formula for the Laguerre polynomials either by expanding the generating function {eq}`eq-hydrogen-17` in powers of $z$ or by reference to Abramowitz and Stegun, table entry (22.3.9). This gives

:::{math}
:label: eq-hydrogen-28
L^{2\ell+1}_{n-\ell-1}(\rho) = \sum_{k=0}^{n-\ell-1} (-1)^k {(n+\ell)! \over k! (2\ell+1+k)! (n-\ell-1-k)!} \, \rho^k.
:::

From this we can work out the first few radial wave functions $R_{n\ell}$, which we tabulate here:

:::{math}
:label: eq-hydrogen-29a
\begin{aligned}
R_{10}(r) &= {2\over \sqrt{a^3}} \, e^{-r/a},
\end{aligned}
:::

:::{math}
:label: eq-hydrogen-29b
\begin{aligned}
R_{20}(r) &= {1\over 2\sqrt{2a^3}} \, e^{-r/2a}(2-r/a),
\end{aligned}
:::

:::{math}
:label: eq-hydrogen-29c
\begin{aligned}
R_{21}(r) &= {1\over 2\sqrt{6a^3}} \, (r/a) e^{-r/2a},
\end{aligned}
:::

:::{math}
:label: eq-hydrogen-29d
\begin{aligned}
R_{30}(r) &= {2\over 9\sqrt{3a^3}} \, e^{-r/3a}\Bigl[3-2\Bigl({r\over a}\Bigr) +{2\over9} \Bigl({r\over a}\Bigr)^2\Bigr],
\end{aligned}
:::

:::{math}
:label: eq-hydrogen-29e
\begin{aligned}
R_{31}(r) &= {2\over 27\sqrt{6a^3}} \, e^{-r/3a}\, {r\over a}\Bigl[4-{2\over 3} \Bigl({r\over a}\Bigr)\Bigr],
\end{aligned}
:::

:::{math}
:label: eq-hydrogen-29f
\begin{aligned}
R_{32}(r) &= {4\over 81\sqrt{30a^3}}\, e^{-r/3a} \, \Bigl({r\over a}\Bigr)^2,
\end{aligned}
:::

where we have restored ordinary units and $a$, the effective Bohr radius, is given in {ref}`tbl-hydrogen-2`. It is worthwhile mentioning that while the energies $E_n$ do not depend on the angular momentum quantum number $\ell$, the wave functions $R_{n\ell}(r)$ depend on both $n$ and $\ell$.

The method that has been used in these notes to derive the energy eigenvalues and eigenfunctions for hydrogen, that is, the method based on a power series expansion of the solution, can be used successfully in several problems in quantum mechanics. In addition to the hydrogen atom, problems solvable by this method include the harmonic oscillator, which leads to Hermite polynomials; the $\theta$-equation in the theory of the spherical harmonics, which leads to the associated Legendre polynomials; the $D$-matrices, which are the wave functions for the rotational motion of symmetric-top molecules, which lead to Jacobi polynomials; and several others. You will be aware, of course, that in the case of the harmonic oscillator ({ref}`ch-harmosc`) and the $Y_{\ell m}$'s ({ref}`ch-orbamsph`) we did not rely mainly on differential equations or power series, rather we used algebraic techniques, that is, raising and lowering operators. It is natural to ask, therefore, whether algebraic techniques exist also for hydrogen. The answer is yes, and the method is tied up with the $SO(4)$ symmetry of the hydrogen atom mentioned earlier. In these notes we have chosen to use more traditional methods to solve the hydrogen atom, because it would take us too far afield to develop the algebraic techniques.

We will mention, however, that the algebraic techniques in question involve a mapping from the bound states of hydrogen onto the spherical harmonics in four dimensions, that is, the harmonics that live on the 3-dimensional surface of a sphere in 4-dimensional, Euclidean space. The $SO(4)$ symmetry group acts on this sphere by 4-dimensional, orthogonal transformations. As for the unbound states of hydrogen with $E>0$, these correspond to harmonics on the unit mass hyperboloid in 4-dimensional Minkowski space. For these the symmetry group is $SO(3,1)$, that is, the Lorentz group. The appearance of the Lorentz group here has nothing to do with relativity in a physical sense, it is just that the mathematics of the positive energy solutions of hydrogen gives rise to it.

\problems

(prob-hydrogen-1)=

**Problem \prbdhydrogen-1..** 

\problempart{(a)} Write out the radial Schr\"odinger equation for a hydrogen-like atom. (“Hydrogen-like” means $V(r)=-Ze^2/r$.) Show that if $a=\hbar^2/\mu Ze^2$, then

:::{math}
:label: eq-hydrogen-30
{d^2 u\over dr^2} + \Bigl[ -{\ell(\ell+1) \over r^2} + {2\over ar} - {1 \over n^2 a^2} \Bigr] u =0,
:::

where $u$ is the normalized radial wave function corresponding to quantum numbers $n$ and $\ell$. Now multiply this by $r^{k+1}(du/dr)$ and integrate from $0$ to $\infty$. Use integration by parts to show that

:::{math}
:label: eq-hydrogen-31
(k+1) \int_0^\infty r^k \Bigl( \dod{u}{r} \Bigr)^2 dr = {k+1\over n^2 a^2} \xpecval{r^k} -{2k \over a} \xpecval{r^{k-1}} +\ell(\ell+1)(k-1)\xpecval{r^{k-2}}.
:::

In the integrations, you may assume that $k>-2\ell-1$, which will cause the boundary terms to vanish.

\problempart{(b)} Now multiply {eq}`eq-hydrogen-30` by $r^k u$ and do more integration by parts, and combine the result with {eq}`eq-hydrogen-31` to show that

:::{math}
:label: eq-hydrogen-32
{k+1\over n^2} \xpecval{r^k} - (2k+1) a \xpecval{r^{k-1}} + {a^2 k\over 4} \bigl[ (2\ell+1)^2-k^2 \bigr] \xpecval{r^{k-2}}=0.
:::

This is called the *Kramer's relation*.

\problempart{(c)} Use {eq}`eq-hydrogen-32` to find $\xpecval{r^k}$ for $k=-1$, $k=1$, and $k=2$. Notice that you cannot evaluate $\xpecval{1/r^2}$ by this method. For that you need to face up to generating functions, or some other method. However, given that

:::{math}
:label: eq-hydrogen-33
\Bigl<{1\over r^2}\Bigr> = {1\over a^2n^3(\ell+\frac{1}{2})},
:::

find $\xpecval{1/r^3}$. The latter is needed for the fine structure perturbations and the Zeeman effect.

(prob-hydrogen-2)=

**Problem \prbdhydrogen-2..**
