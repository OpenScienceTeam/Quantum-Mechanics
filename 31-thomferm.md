---
title: "31. The Thomas-Fermi Model"
---
(ch-thomferm)=

# 31. The Thomas-Fermi Model

(sec-thomferm-1)=

## Introduction

The Thomas-Fermi model is a relatively crude model of multi-electron atoms that is useful for many purposes in a first approximation. The basic idea is to represent the electron cloud surrounding the nucleus as a zero-temperature, negatively charged, degenerate Fermi-Dirac fluid, which is held in a condition of hydrostatic equilibrium by a balance between pressure gradients and electrostatic forces.

(sec-thomferm-2)=

## Zero Temperature, Degenerate Electron Gas

The equation of state of a degenerate, zero-temperature electron gas is a standard topic in statistical mechanics, which we now summarize. We begin with a box of volume $V$, into which $N$ electrons are placed. We assume that any external potential is sufficiently slowly varying that the electron wave functions in the box can be approximated by plane waves. Then the density of states with respect to electron wave number $k$ is

:::{math}
:label: eq-thomferm-1
\dod{N}{k}={k^2V\over\pi^2},
:::

which includes a factor of $2$ for the electron spin. We integrate this from $k=0$ to $k=k_F$, where $k_F$ is the Fermi wave number, to obtain the number density $n$:

:::{math}
:label: eq-thomferm-2
n={N\over V} = {k_F^3 \over 3\pi^2}.
:::

We solve this for $k_F$ to find,

:::{math}
:label: eq-thomferm-3
k_F = (3\pi^2 n)^{1/3}.
:::

Similarly, we multiply {eq}`eq-thomferm-1` by the kinetic energy $\hbar^2 k^2/2m$ for a single electron and integrate from $k=0$ to $k=k_F$ to get the total kinetic energy of the electrons in the box,

:::{math}
:label: eq-thomferm-4
E={\hbar^2 V k_F^5 \over 10 m\pi^2}.
:::

Eliminating $k_F$ between {eq}`eq-thomferm-2` and {eq}`eq-thomferm-4`, we express $E$ as a function of the “macroscopic” parameters $V$ and $N$,

:::{math}
:label: eq-thomferm-5
E={\hbar^2(3\pi^2 N)^{5/3} \over 10 m \pi^2} \, V^{-2/3}.
:::

Finally, using $P=-dE/dV$, we obtain the pressure $P$ as a function of the number density $n$,

:::{math}
:label: eq-thomferm-6
P={\hbar^2 \over 15 m\pi^2}(3\pi^2 n)^{5/3},
:::

which is the equation of state at zero temperature.

(sec-thomferm-3)=

## Fluid Model of Atom

The electron fluid surrounding the nucleus is like the atmosphere of a planet or a star, except that electrostatic forces hold the fluid in rather than gravitational forces. Since the fluid itself carries charge, the force on a fluid element comes from both the nucleus and the other electrons. Since the fluid organizes itself in a rotationally symmetric cloud around the nucleus, the force on a given electron fluid element arises strictly from the nucleus and the electron fluid at smaller radii than the given fluid element. (In actual atoms, the electron cloud is not exactly rotationally symmetric, but it is so in the Thomas-Fermi model.) Obviously, the density and pressure of the electron fluid will increase from small or zero values at large distances from the nucleus to a maximum at the nucleus itself. One of our goals will be to find expressions for the density and pressure as a function of distance from the nucleus.

The net force per unit volume on an element of the electron fluid is the sum of $-\del P$ due to the pressure gradient and $\rho \Evec$ due to the electric field, where $\rho$ is the electron charge density. These forces must balance each other in equilibrium. Since $\rho = -en$ and $\Evec=-\del\Phi$, where $\Phi$ is the electrostatic potential, we have the condition for hydrostatic equilibrium,

:::{math}
:label: eq-thomferm-7
\del P = en\del\Phi.
:::

We note that the force per unit volume $-\del P$ will be directed outward, since the pressure must increase as we move inward, so the electrostatic force per unit volume $\rho\Evec=en\del\Phi$ must be directed inward. {eq}`eq-thomferm-7` is augmented by the Poisson equation,

:::{math}
:label: eq-thomferm-8
\del^2\Phi = -4\pi\rho = 4\pi ne - 4\pi Ze \delta(\xvec),
:::

where we include the charge density for the nucleus in the final term. In most of the following analysis we will drop this $\delta$-function term for the nucleus, since it will be understood that we are working at nonzero $r$, where this term vanishes. We will incorporate the effects of the nuclear charge by imposing proper boundary conditions on various quantities as $r\to0$.

(sec-thomferm-4)=

## Solving the Self-Consistent Equations

Equations~{eq}`eq-thomferm-6`, {eq}`eq-thomferm-7` and {eq}`eq-thomferm-8` are three equations in three unknowns $P$, $n$, and $\Phi$. To solve these, we begin by taking the gradient of {eq}`eq-thomferm-6`, to obtain

:::{math}
:label: eq-thomferm-9
\del P = {\hbar^2 \over 3m} (3\pi^2)^{2/3} n^{2/3} \del n,
:::

which we combine with {eq}`eq-thomferm-7` to eliminate the pressure. We then find

:::{math}
:label: eq-thomferm-10
{\hbar^2\over 3m} (3\pi^2)^{2/3} n^{-1/3} \del n = e\del\Phi,
:::

which we integrate to obtain

:::{math}
:label: eq-thomferm-11
{\hbar^2\over 2m} (3\pi^2 n)^{2/3} = e(\Phi-\Phi_0)=e\Psi,
:::

where $\Phi_0$ is a constant of integration and where

:::{math}
:label: eq-thomferm-12
\Psi=\Phi-\Phi_0.
:::

Before proceeding, we require an interpretation of the constant $\Phi_0$. Only a partial interpretation can be given at this point, but we can say some things. First, we note that by {eq}`eq-thomferm-3` the left hand side of {eq}`eq-thomferm-11` can be reexpressed,

:::{math}
:label: eq-thomferm-13
{\hbar^2\over 2m} (3\pi^2 n)^{2/3} = {\hbar^2 k_F^2 \over 2m} = {p_F^2 \over 2m},
:::

where $p_F=\hbar k_F$ is the Fermi momentum. Thus, {eq}`eq-thomferm-13` gives the kinetic energy of an electron at the top of the Fermi sea, and {eq}`eq-thomferm-11` can be written,

:::{math}
:label: eq-thomferm-14
{p_F^2 \over 2m} - e\Phi = -e\Phi_0.
:::

The left hand side of this equation is the total energy (kinetic plus potential) for an electron at the top of the Fermi sea, which is the constant $-e\Phi_0$. The potential $\Phi$ certainly depends on $r$, as does $p_F$ (since it depends on $n$), but the sum of the two terms on the left is independent of $r$.

(sec-thomferm-5)=

## Interpretation of Constant $\Phi_0$

This constant $-e\Phi_0$ is the chemical potential of the electron gas, since the chemical potential is defined as the change in the energy of a system when a particle is added, under conditions of constant entropy. In the present case, the entropy is constant because the temperature is zero, and the energy of the additional particle is the energy at the top of the Fermi sea (kinetic plus potential), which is where the additional particle must go because of the Pauli principle. If the chemical potential were not independent of $r$, then electrons would move from one radius to another to equalize it.

Another interpretation of the constant $\Phi_0$ is obtained from a plot of the potential energy $\Phi(r)$. We do not yet have an analytic solution for $\Phi(r)$, but certainly this function goes as $Ze/r$ for small $r$, where the field of the nucleus dominates, and it must approach zero for large $r$. There are two cases to consider. Letting $N$ be the number of electrons in the atom (a change of notation from above, where $N$ was the number of electrons in the box), then if $N<Z$ we have a positive ion, and if $N=Z$ we have a neutral atom. We know that negative ions exist in nature (for example, $H^-$), but negative ions cannot be accommodated in the Thomas-Fermi model, for if we ever reach a radius at which the total electron charge is equal to the nuclear charge $Z$, then the vector $\rho\Evec$ vanishes at that radius, and there can be no hydrostatic equilibrium. Any additional electron fluid beyond that radius will experience both pressure and electrostatic forces directed outward, and will not be bound. Therefore the cases of interest are $N<Z$ and $N=Z$. In the case $N<Z$, the potential $\Phi$ must fall off at large $r$ as $(Z-N)e/r$, and in the case $N=Z$ it must fall off even faster than $1/r$, since a neutral atom is being left behind. Furthermore, the potential must decrease monotonically as $r$ increases, so that the electrostatic force vector be always directed inward. Therefore the potential $\Phi(r)$ must look as in {ref}`fig-thomferm-1`, at least schematically.

:::{figure} images/thomferm-fig01.png
:label: fig-thomferm-1
:width: 80%

The potential $\Phi(r)$ must go to $\infty$ for small $r$ and to zero for large $r$, and must decrease monotonically as $r$ increases. A positive constant $\Phi_0$ is illustrated, which indicates an atom with a definite radius $r_0$.
:::

Suppose now that the constant $\Phi_0$ is positive. Then as indicated in the figure, there is some radius $r_0$ where $\Phi=\Phi_0$. But at this radius, we have $n=0$ according to {eq}`eq-thomferm-11`, which implies $P=0$ according to {eq}`eq-thomferm-6`. Therefore the radius $r_0$ must be the surface of the atom, at which the charge density and pressure have fallen to zero, and beyond which there is only vacuum. For $r>r_0$, there is no more electron fluid, so the equations above are replaced simply by $n=0$, $P=0$, and the Poisson equation $\del^2\Phi=0$ for $\Phi$. Later we will see that the case $\Phi_0>0$ corresponds to a positive ion, $N<Z$. On the other hand, if we let $\Phi_0$ approach zero, then from the figure $r_0$ moves out to infinity, and we have an atom whose electron cloud extends out to infinite radius (the electron density approaches zero, but never exactly equals zero). Later we will see that this case corresponds to a neutral atom, $N=Z$. Finally, we will see later that the case $\Phi_0<0$ corresponds to a neutral atom under applied pressure.

(sec-thomferm-6)=

## The Thomas-Fermi Equation

We now rewrite the Laplace equation {eq}`eq-thomferm-8` in terms of the variable $\Psi$,

:::{math}
:label: eq-thomferm-15
\del^2\Psi=4\pi ne,
:::

which, taken with {eq}`eq-thomferm-11` gives us two equations in the two unknowns $n$ and $\Psi$. Neither of these variables is convenient as a dependent variable, because they both diverge at $r=0$. For example, since $\Phi$ is dominated by the field of the nucleus near $r=0$ and since $\Phi_0$ is a constant, we have $\Psi \sim Ze/r$ for small $r$, which by {eq}`eq-thomferm-11` implies that $n$ goes as $r^{-3/2}$ for small $r$.

Therefore instead we introduce a new dependent variable,

:::{math}
:label: eq-thomferm-16
f={r\Psi\over Ze},
:::

which is dimensionless and takes on the value $f(0)=1$. To express other variables in terms of $f$, we find first

:::{math}
:label: eq-thomferm-17
e\Psi = {Ze^2\over r}\, f,
:::

:::{math}
:label: eq-thomferm-18
n={1\over 3\pi^2} \left( {2me\Psi\over\hbar^2}\right)^{3/2},
:::

and then

:::{math}
:label: eq-thomferm-19
n={1\over 3\pi^2} \left({2mZe^2 \over \hbar^2} \right)^{3/2} {f^{3/2}\over r^{3/2}}.
:::

From these it is easy to get a radial equation for $f$. This involves some messy constants, which we clean up by writing

:::{math}
:label: eq-thomferm-20
r=bx,
:::

where $x$ is a dimensionless radial variable, and where $b$ has dimensions of distance and is given by

:::{math}
:label: eq-thomferm-21
b={(3\pi)^{2/3} \over 2^{7/3}} {a_0\over Z^{1/3}} =0.88 {a_0\over Z^{1/3}},
:::

where $a_0$ is the usual Bohr radius. Finally, this gives the Thomas-Fermi equation for $f$,

:::{math}
:label: eq-thomferm-22
{d^2 f\over dx^2} = {f^{3/2} \over x^{1/2}}.
:::

This equation is universal in the sense that all physical constants have been removed by scaling transformations.

(sec-thomferm-7)=

## Interpreting the Solutions of the Thomas-Fermi Equation

The Thomas-Fermi equation {eq}`eq-thomferm-22` is second order and therefore possesses two constants of integration; but one is taken already by the boundary condition $f(0)=1$, so there is only a one-parameter family of solutions with physical meaning. This family can be parameterized by $f'(0)$, the initial slope of $f(x)$. The Thomas-Fermi equation is nonlinear and cannot be solved analytically, and we must resort to numerical work to find the solutions. Some numerical solutions are plotted in {ref}`fig-thomferm-2` for several values of the initial slope. The character of the solutions can be understood graphically, without doing any numerical work. Note that by {eq}`eq-thomferm-22`, as long as $f$ and $x$ are both positive (the only case of interest), the function $f(x)$ must be concave upward.

:::{figure} images/thomferm-fig02.png
:label: fig-thomferm-2
:width: 80%

Numerical solutions of the Thomas-Fermi equation for different values of the initial slope. The critical initial slope of about -1.588 corresponds to a neutral atom; initial slopes that are more negative correspond to a positive ion, with a definite radius; and initial slopes that are less negative correspond to a neutral atom under pressure.
:::

There are three cases to consider. In the first case, $f'(0)$ is sufficiently negative that the curve $f(x)$ meets the $x$-axis at some point $x_0$, so that $f(x_0)=0$. The curve in {ref}`fig-thomferm-2` with $f'(0)=-1.64$ illustrates this case. Note that the slope $f'(x_0)$ is negative. It is clear from the figure that $x_0$ is a function of the initial slope $f'(0)$, and that as $f'(0)$ increases, so does $x_0$. The meaning of $x_0$ is that it is the surface of the atom, outside of which the electron density vanishes. That is, $x_0$ is the equivalent of the point $r_0$ in {ref}`fig-thomferm-1`, according to $r_0=bx_0$, for if $f(x_0)=0$, then by {eq}`eq-thomferm-17` we also have $\Psi=0$, and therefore $\Phi=\Phi_0$, $n=0$, and $P=0$.

In this case it is of interest to compute the total number of electrons in the atom, which is

:::{math}
:label: eq-thomferm-23
N = \int_0^{r_0} 4\pi r^2\,dr \, n(r) = Z \int_0^{x_0} dx \, x^{1/2} f^{3/2},
:::

where we have used {eq}`eq-thomferm-19` and {eq}`eq-thomferm-20`. But the integrand of the final integral can be rewritten with the help of the Thomas-Fermi equation {eq}`eq-thomferm-22`, whereupon it becomes an exact derivative,

:::{math}
:label: eq-thomferm-24
x^{1/2} f^{3/2} = x f''(x) = \dod{}{x}[xf'(x) - f(x)].
:::

Therefore we have

:::{math}
:label: eq-thomferm-25
{N\over Z} = [xf'(x) - f(x)]\Bigr|_0^{x_0} = x_0f'(x_0) + 1,
:::

or,

:::{math}
:label: eq-thomferm-26
-x_0f'(x_0) = {Z-N \over Z}.
:::

Since the left hand side is positive, we see that this case corresponds to a positive ion with $N<Z$. If we wish to model a specific positive ion with given values of $Z$ and $N$, it will be necessary to search numerically for the initial slope $f'(0)$ that will cause {eq}`eq-thomferm-25` to be satisfied.

As commented earlier, as we increase the initial slope $f'(0)$, the value $x_0$ at which $f=0$ increases. It is not obvious but it is true that $x_0$ can be made to increase without bound in this manner, so that as $f'(0)$ approaches a critical initial slope from below, the curve $f(x)$ becomes one that asymptotes to the $x$-axis for large $x$. The critical initial slope is found numerically to be $f'(0) \approx -1.588$, and the solution $f(x)$ in this case is illustrated in {ref}`fig-thomferm-2`. As this slope is approached, we have

:::{math}
:label: eq-thomferm-27
\lim_{x_0\to\infty} -x_0 f'(x_0) =0,
:::

that is, $f'(x_0)$ goes to zero faster than $x_0$ goes to infinity. (In fact, one can show that $f'(x_0)$ goes as $1/x_0^4$ for large $x_0$.) By combining {eq}`eq-thomferm-26` and {eq}`eq-thomferm-27`, we see that this case corresponds to a neutral atom ($N=Z$), and that such an atom in the Thomas-Fermi model has an infinite radius. For neutral atoms, there is one particular solution of the Thomas-Fermi equation, with $f(0)=1$ and $f'(0)\approx -1.588$, which applies to all atoms. This solution is a universal function, independent of $Z$. This function has been tabulated and can be found in references. We notice that by {eq}`eq-thomferm-20` and {eq}`eq-thomferm-21`, we can say that the scale length of the neutral Thomas-Fermi atom goes as $Z^{-1/3}$.

Finally, the third case is the one in which the initial slope $f'(0)$ is greater than the critical value of approximately $-1.588$, so the electron density neither vanishes nor approaches zero at any radius. The curves in {ref}`fig-thomferm-2` with initial slopes $f'(0)=-1.49$ and $-1.54$ illustrate this case. This case can be used to model a neutral atom under pressure; we simply choose the radius $x_0$ at which

:::{math}
:label: eq-thomferm-28
{N\over Z}=1 = \int_0^{x_0} dx \, x^{1/2} f^{3/2},
:::

and declare that radius to correspond to the volume allotted to an atom in a bulk sample under pressure. Since $f$ does not vanish at $x_0$, there will be a nonzero value of the pressure at $x_0$, which is interpreted as the applied pressure. In this way it is possible to obtain a crude equation of state for matter under pressure. We do not attempt to model charged ions under pressure, because the large electric fields make it impossible to collect bulk samples of charged ions.

(sec-thomferm-8)=

## Crudeness of the Thomas-Fermi Model

The Thomas-Fermi model is crude on several accounts. When we derived the equation of state of the degenerate electron gas, we assumed that it was possible to carve out a box that was small enough that the potential was nearly constant over its size, but large enough that it contained a large number of electrons, so that we could take the thermodynamic limit. These requirements are in conflict, and are never satisfied in an atom, except in a crude sense. Furthermore, the electron fluid, as we have treated it, is infinitely divisible, and does not accommodate the discrete charge $-e$ of individual electrons.

These limitations are obvious in the results, for the Thomas-Fermi model gives no hint of the shell structure that we know exists in atoms. In fact, the Thomas-Fermi model generally does a poor job of describing the properties of the outermost electrons (which are involved in the ionization potential, the chemical properties of the atom, its shell structure, etc.), and of the properties of the electron cloud near the nucleus. (In reality the electron density approaches a finite value as $r\to0$, but in the Thomas-Fermi model it diverges as $r^{-3/2}$.) But the Thomas-Fermi model does a fair job of describing the electron density at intermediate radii, and gives moderately good results for the average properties of atoms, such as the average binding energy or rms charge radius. Therefore it is useful for such applications as calculations of the slowing down of particles passing through matter (an important subject in experimental physics). The Thomas-Fermi model is also useful as a starting approximation for more sophisticated atomic models, such as the Hartree-Fock approximation.

\problems

(prob-thomferm-1)=

**Problem \prbdthomferm-1.}  Let $f(x)$ be the solution of the Thomas-Fermi equation {eq}`eq-thomferm-22` with initial condition $f(0)=1$ that asymptotes to the $x$-axis as $x\to\infty$.  Assuming that $f$ has an expansion in inverse powers of $x$, show that the leading power is $x^{-3.** 

:::{math}
:label: eq-thomferm-29
f(x) \approx {144\over x^3}
:::

for large }$x$.

Now consider a neutral atom of charge $Z$. The Thomas-Fermi solution for a neutral atom predicts a charge cloud which extends to infinity, so if we define the radius of the atom as the radius beyond which there is no more charge, then that radius is always infinite for neutral atoms. But suppose we define the radius of the neutral atom as that radius which contains all the electrons except one. Use the approximation {eq}`eq-thomferm-29` to compute this radius, and note its $Z$ dependence.

(prob-thomferm-2)=

**Problem \prbdthomferm-2..** 

\problempart{(a)} Show that

:::{math}
:label: eq-thomferm-30
E_1 = {3Z^2e^2J\over 2b} \quad and \quad E_2 = -{7\over3} E_1,
:::

where

:::{math}
:label: eq-thomferm-31
J=\int_0^\infty \Bigl(\dod{f}{x}\Bigr)^2 \,dx = 0.454,
:::

and where $b$ is defined by {eq}`eq-thomferm-21`.

\problempart{(b)} The structure equations of the Thomas-Fermi atom can be derived from a variational principle, instead of by balancing forces. To do this, we regard the total energy of the Thomas-Fermi atom as a functional of the electron number density, $n(r)$. The electron fluid is assumed to obey the zero-temperature equation of state of a Fermi-Dirac ideal gas. The particular function $n(r)$ that minimizes the total energy, subject to the constraint that the total number of electrons be constant,

:::{math}
:label: eq-thomferm-32
N=Z = \int_0^\infty 4\pi r^2 n(r) \,dr,
:::

is the actual $n(r)$ in the Thomas-Fermi model.

Notice that if $n(r)$ is replaced by $\alpha^3 n(\alpha r)$, where $\alpha$ is a scale parameter, then the total number of electrons is constant. Use this to show that in the Thomas-Fermi model,

:::{math}
:label: eq-thomferm-33
E_total = E_1+E_2+E_3 = -E_1.
:::
