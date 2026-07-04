---
title: "50. Solutions of the Dirac Equation and Their Properties"
---
(ch-spdirac)=

# 50. Solutions of the Dirac Equation and Their Properties

(sec-spdirac-1)=

## Introduction

In {ref}`ch-dirac`{} we introduced the Dirac equation in much the same manner as Dirac himself did, with the motivation of curing the problems of the Klein-Gordon equation. We saw that the Dirac equation, unlike the Klein-Gordon equation, admits a conserved 4-current with a nonnegative definite time component, so that it can be interpreted as a probability 4-current. On the other hand, the Klein-Gordon equation has one problem that is shared with the Dirac equation, the existence of negative energy solutions, for which we have no interpretation as yet. We might suppose that the negative energy solutions could simply be declared to be nonphysical, but this turns out to be impossible, as we will see. In addition, the velocity operator in the Dirac theory is strange, being a purely spin operator when we might have expected something purely spatial on the nonrelativistic analogy. The same velocity operator appears in the spatial part of the probability current. It is however encouraging that the Dirac equation automatically produces the correct interaction of the spin with a magnetic field, with the (almost exactly) correct $g$-factor for an electron. To summarize, as a candidate relativistic wave equation for the electron, the Dirac equation presents some remarkable successes, some strange features, and some others with no obvious physical interpretation.

The purpose of these notes is to explore some solutions of the Dirac equation and their properties, in order to accumulate some results that will be useful for later work, to reveal some further successes of the Dirac equation, and to explore some of the puzzling aspects of the theory in order to understand them better and to lay the foundation for their ultimate resolution.

We begin by exploring the properties of free particle solutions of the Dirac equation, including the negative energy solutions. The free particle solutions form a basis of orthonormal eigenfunctions that will be useful for later work, especially when we turn to the second quantization of the Dirac field. We do not manage at this time to obtain a physical interpretation of the negative energy free particle solutions, but we learn some things about them, such as their energy spectrum and the fact that, in a certain sense, they have negative momentum and spin as well as negative energy. We then turn to the Gordon decomposition of the current, which gives some understanding as to why the velocity appears as a spin operator in the Dirac theory. Then we present a discussion of the Zitterbewegung, a kind of jittering motion that the Dirac electron undergoes on a rapid time scale, even in the case of a free particle. The Zitterbewegung is related to the Darwin term in atomic physics (see {ref}`ch-finestruc`). Finally, we discuss central force problems in general and then the exact solution of the hydrogen atom for the Dirac equation. This gives us not only all the fine structure corrections we saw in {ref}`ch-finestruc`{} but also negative energy solutions. For these, however, as in the case of the free particle, we have no interpretation as yet.

The net effect of this set of notes will be to give us experience with some exact solutions of the Dirac equation (the free particle and the hydrogen atom), some understanding of some of the strange features (the velocity operator), some new strange features (the Zitterbewegung), and yet still no physical interpretation of the negative energy solutions (that will come later).

In the following treatment of free particle solutions it will be important to distinguish the momentum operator (3-vector or 4-vector) from the corresponding vectors of $c$-numbers. Therefore we will put an “op” subscript on the momentum when an operator is intended, such as $\pvec_op=-i\hbar\del$ or $p^\mu_op =i\hbar\,\partial^\mu$, and omit the “op” subscript when a $c$-number is intended. For other operators the distinction will not be necessary so we will omit the “op” subscripts. We will use hats on unit vectors, as usual.

(sec-spdirac-2)=

## Free Particle Solutions of the Pauli Equation

The Pauli Hamiltonian for a free particle of spin $\frac{1}{2}$ is $H=\pvec_op^2/2m$ and the wave function is a 2-component spinor. A complete set of commuting observables that also commute with the Hamiltonian is $(\pvec_op,S_z)$. The eigenfunctions of $H$ that are also eigenfunctions of these observables are

:::{math}
:label: eq-spdirac-1
\begin{pmatrix}1\cr0\\\end{pmatrix}e^{i(\pvec\cdot\xvec-Et)/\hbar}, \qquad \begin{pmatrix}0\cr1\\\end{pmatrix}e^{i(\pvec\cdot\xvec-Et)/\hbar},
:::

where $\pvec$ is the momentum eigenvalue, where the first solution is an eigenfunction of $S_z$ with eigenvalue $+\hbar/2$ and the second with eigenvalue $-\hbar/2$. We have included the time dependence in these solutions, where $E=\pvec^2/2m$.

(sec-spdirac-3)=

## Dirac Free Particle Solutions and Spin

The Dirac Hamiltonian for a free particle is

:::{math}
:label: eq-spdirac-2
H=c\pvec_op\cdot\alphavec + \beta mc^2.
:::

In comparison to the Pauli theory, we might expect to find eigenfunctions of $H$ that are also eigenfunctions of $\pvec_op$ and $(\hbar/2)\Sigma_3$, the latter being the Dirac generalization of the Pauli operator $S_z=(\hbar/2)\sigma_3$. This does not work, however, for although $\pvec_op$ and $\Sigmavec$ commute with each other (one is purely spatial and the other purely spin), and although $\pvec_op$ commutes with $H$, $\Sigmavec$ does not commute with $H$. This is because $\Sigmavec$ generates spin rotations, which rotate the vector $\alphavec$ but not the spatial vector $\pvec_op$, so the dot product $\pvec_op\cdot\alphavec$ is not invariant. On the other hand, orbital angular momentum $\Lvec$ generates spatial rotations that rotate $\pvec_op$ but not $\alphavec$, so again $\pvec_op\cdot\alphavec$ is not invariant. Obviously if we want to find an angular momentum operator that does commute with $H$, it is $\Jvec=\Lvec+(\hbar/2)\Sigmavec$, the total angular momentum (orbital plus spin) of the Dirac particle. See {ref}`sec-covariance-17`.

Although orbital and spin angular momentum are defined for the Dirac particle, they are not separately conserved, even for a free particle. This is a reflection of the more intimate coupling of orbital and spin degrees of freedom in the relativistic theory, as compared to nonrelativistic quantum mechanics. Recall that for the photon, orbital and spin angular momentum are separately not even defined, although $\Jvec$ is.

On account of these considerations, we can expect spin to play a more complicated role in the theory of free particle solutions of the Dirac equation than it does in the Pauli theory.

(sec-spdirac-4)=

## Free Particle Solutions of the Dirac Equation at Rest

There are four linearly independent solutions of the time-dependent Dirac equation for a free particle at rest. These are given in {eq}`eq-dirac-31`, reproduced here:

:::{math}
:label: eq-spdirac-3
\begin{pmatrix}1\\ 0 \\ 0 \\ 0 \\\end{pmatrix} e^{-imc^2t/\hbar}, \quad \begin{pmatrix}0\\ 1\\ 0\\ 0\\\end{pmatrix} e^{-imc^2t/\hbar}, \quad \begin{pmatrix}0\\ 0\\ 1\\ 0\\\end{pmatrix} e^{+imc^2t/\hbar}, \quad \begin{pmatrix}0\\ 0\\ 0\\ 1\\\end{pmatrix} e^{+imc^2t/\hbar}.
:::

The first two of these have energy $+mc^2$, and the last two have energy $-mc^2$, as we find by applying either $H$ or $i\hbar\,\partial/\partial t$. We have as yet no physical interpretation for the solutions of negative energy, but they will turn out to be important so we must keep them and investigate their properties.

The solutions at rest, {eq}`eq-spdirac-3`, are eigenstates of $\Sigma_3$, that is, the spin is polarized in the $\pm{\hat{\mathbf{z}}}$ direction in the rest frame. In following work we will want to be more general, and to allow the spin to be polarized in an arbitrary direction in the rest frame. Let ${\hat{\mathbf{s}}}$ be a unit vector in the rest frame of the particle. If $(\theta,\phi)$ are the angles of ${\hat{\mathbf{s}}}$ in spherical coordinates, then we define the 2-component (Pauli) spinor $\chi({\hat{\mathbf{s}}})$ as the spinor “pointing in” the direction ${\hat{\mathbf{s}}}$, as explained in {ref}`sec-spinrot-14`. According to {eq}`eq-spinrot-60`, this spinor is

:::{math}
:label: eq-spdirac-4
\chi({\hat{\mathbf{s}}})=\begin{pmatrix} e^{-i\phi/2}\cos(\theta/2)\\ e^{i\phi/2}\sin(\theta/2)\\\end{pmatrix},
:::

to within an overall phase which will not be important to us. In this notation the eigenspinors of ${\hat{\mathbf{s}}}\cdot\sigmavec$ are $\chi(\pm{\hat{\mathbf{s}}})$,

:::{math}
:label: eq-spdirac-5
({\hat{\mathbf{s}}}\cdot\sigmavec)\chi({\hat{\mathbf{s}}}) = \chi({\hat{\mathbf{s}}}), \qquad ({\hat{\mathbf{s}}}\cdot\sigmavec)\chi(-{\hat{\mathbf{s}}}) = -\chi(-{\hat{\mathbf{s}}}),
:::

the second of which follows by making the replacement ${\hat{\mathbf{s}}}\to-{\hat{\mathbf{s}}}$ in the first. For a fixed value of ${\hat{\mathbf{s}}}$, the spinors $\chi(\pm{\hat{\mathbf{s}}})$ form an orthonormal basis in the space of 2-component spinors.

Now we define two types of 4-component spinors, here broken into their upper and lower 2-component spinors,

:::{math}
:label: eq-spdirac-6
u_0({\hat{\mathbf{s}}}) = \begin{pmatrix}\chi({\hat{\mathbf{s}}})\\ 0\\\end{pmatrix}, \qquad v_0({\hat{\mathbf{s}}}) = \begin{pmatrix}0\\ \chi(-{\hat{\mathbf{s}}})\\\end{pmatrix},
:::

where the 0 subscript on $u_0$ and $v_0$ means, “at rest.” The odd thing about these definitions is that we have used $\chi(-{\hat{\mathbf{s}}})$ in the definition of $v_0$, that is, with a minus sign on the direction of spin. The reason for this choice will be explained momentarily. These spinors are eigenspinors of the Dirac matrix ${\hat{\mathbf{s}}}\cdot\Sigmavec$, where

:::{math}
:label: eq-spdirac-7
\begin{aligned}
\Sigmavec=\begin{pmatrix}\sigmavec & 0 \\ 0 & \sigmavec\\\end{pmatrix}
\end{aligned}

:::

(this is {eq}`eq-covariance-61`. That is,

:::{math}
:label: eq-spdirac-8
({\hat{\mathbf{s}}}\cdot\Sigmavec)u_0({\hat{\mathbf{s}}}) = u_0({\hat{\mathbf{s}}}), \qquad ({\hat{\mathbf{s}}}\cdot\Sigmavec)v_0({\hat{\mathbf{s}}}) = -v_0({\hat{\mathbf{s}}}).
:::

Then the most general free-particle solutions of the Dirac equation when the particle is at rest can be written

:::{math}
:label: eq-spdirac-9
u_0({\hat{\mathbf{s}}})\, e^{-imc^2t/\hbar}, \qquad v_0({\hat{\mathbf{s}}})\, e^{+imc^2t/\hbar},
:::

of which the first has energy $+mc^2$ and the second $-mc^2$. These are the positive- and negative-energy solutions, respectively. If ${\hat{\mathbf{s}}}$ is chosen to run over two oppositely oriented unit vectors in the rest frame, then the solutions {eq}`eq-spdirac-9` constitute a complete set of free particle solutions at rest, with definite spins in the rest frame.

(sec-spdirac-5)=

## Boosting the Solutions at Rest

To create free particle solutions in some state of motion we apply a boost to the free particle at rest. We first consider this problem from a classical standpoint. Let $\pvec$ be the desired 3-momentum of our particle, and $\Lambdamat(\pvec)$ the boost that will take the particle at rest into one with momentum $\pvec$. The 4-momentum of the particle at rest is

:::{math}
:label: eq-spdirac-10
p_0^\mu = \begin{pmatrix}mc\\ \zerovec\\\end{pmatrix},
:::

where again the $0$-subscript means “at rest” and the 4-vector is given in $(1+3)$-notation. The 4-momentum of the particle after the boost is

:::{math}
:label: eq-spdirac-11
p^\mu=\begin{pmatrix}E/c\\ \pvec\\\end{pmatrix},
:::

where

:::{math}
:label: eq-spdirac-12
E=E(\pvec) = \sqrt{m^2c^4 + c^2\pvec^2}.
:::

This is of course the standard definition of the energy of a free particle in relativity theory, but in the following it will be important to remember that the symbol $E$ stands for the positive square root in {eq}`eq-spdirac-12`, even when we are talking about negative energy solutions. Also, in the following both the energy $E$ and the 4-momentum $p^\mu$ will be understood to be functions of the 3-momentum $\pvec$, which by itself characterizes the state of motion of the particle after the boost.

We can put the boost $\Lambdamat(\pvec)$ into axis-rapidity form, as in {ref}`sec-lorentz-5`. The boost must be in the direction of the momentum $\pvec$ so the boost axis is

:::{math}
:label: eq-spdirac-13
{\hat{\mathbf{b}}} = {\pvec\over |\pvec|},
:::

where ${\hat{\mathbf{b}}}$ is a unit vector, and its rapidity $\lambda$ is given implicitly as a function of $\pvec$ by

:::{math}
:label: eq-spdirac-14
\cosh\lambda = {E\over mc^2}, \qquad \sinh\lambda = {|\pvec|\over mc}, \qquad \tanh\lambda={c|\pvec|\over E}= {|\vvec|\over c},
:::

where $\vvec$ is the velocity of the particle after the boost. With this axis and rapidity, we have $\Lambdamat(\pvec) = \Lambdamat ({\hat{\mathbf{b}}},\lambda)$. The action of a boost in axis-rapidity notation on an arbitrary 4-vector is given explicitly by {eq}`eq-lorentz-34`. Applying that equation, we can check that

:::{math}
:label: eq-spdirac-15
p^\mu = \Lambda(\pvec)^\mu{}_\nu \, p_0^\nu.
:::

We shall sometimes write this as $p=\Lambda p_0$, using simply $p$ and $p_0$ for the 4-momenta with components $p^\mu$ and $p_0^\mu$.

We turn now to the quantum side of the boost, that is, boosting the free particle solutions at rest, {eq}`eq-spdirac-9`, of the Dirac equation. In this process it will be convenient to use covariant notation insofar as possible. As for the exponents in {eq}`eq-spdirac-9`, notice that

:::{math}
:label: eq-spdirac-16
mc^2t = (mc)(ct) = p_{0\mu}\, x^\mu = p_0\cdot x,
:::

in the notation of {eq}`eq-lorentz-104` for the Minkowski scalar product of two 4-vectors. Therefore we can write the positive and negative energy solutions for a free particle at rest as

:::{math}
:label: eq-spdirac-17
u_0({\hat{\mathbf{s}}})\,e^{-i(p_0\cdot x)/\hbar}, \qquad v_0({\hat{\mathbf{s}}})\,e^{+i(p_0\cdot x)/\hbar}.
:::

Under the Lorentz transformation $\Lambdamat(\pvec)$, a Dirac 4-component wave function $\psi(x)$ is mapped into $D(\pvec)\psi\bigl (\Lambda(\pvec)^{-1}\,x\bigr)$, as explained in {ref}`sec-covariance-4`, where we define

:::{math}
:label: eq-spdirac-18
D(\pvec)=D\bigl(\Lambdamat(\pvec)\bigr).
:::

Under this mapping, the exponents in {eq}`eq-spdirac-17` transform according to

:::{math}
:label: eq-spdirac-19
p_0\cdot x \mapsto p_0\cdot (\Lambda^{-1}\,x) = (\Lambda\,p_0)\cdot x = p \cdot x = p_\mu x^\mu,
:::

where we use the identity {eq}`eq-lorentz-105`. This calculation is essentially the same as that presented in {ref}`sec-covariance-5`. As for the matrix $D(\pvec)$, the $D$-matrix in axis-rapidity notation is given by {eq}`eq-covariance-75`. Here we express the hyperbolic functions of half-angles in terms of the energy and momentum of the particle after the boost, as follows:

:::{math}
:label: eq-spdirac-20
\begin{aligned}
\cosh{\lambda\over2} &= \sqrt{{\cosh\lambda+1\over2}} = \sqrt{{E+mc^2\over 2mc^2}}, \\
\sinh{\lambda\over2} &= \sqrt{{\cosh\lambda-1\over2}} = \sqrt{{E-mc^2\over 2mc^2}}, \\
\tanh{\lambda\over2} &= \sqrt{{E-mc^2 \over E+mc^2}} = \sqrt{{E^2 -m^2c^4 \over (E+mc^2)^2}} = {c|\pvec| \over E+mc^2}. \\

\end{aligned}
:::

Substituting these into {eq}`eq-covariance-75`, we obtain the explicit form of the $D$-matrix,

:::{math}
:label: eq-spdirac-21
\begin{aligned}
D(\pvec) = \sqrt{{E+mc^2\over 2mc^2}} \begin{pmatrix} 1 & \ds{\ds c \pvec\cdot\sigmavec \over \ds E+mc^2} \\ \ds {\ds c\pvec\cdot\sigmavec \over \ds E+mc^2}  & 1 \\\end{pmatrix}.
\end{aligned}

:::

Under the Lorentz transformation $D(\pvec)$ acts on the spinors $u_0({\hat{\mathbf{s}}})$, $v_0({\hat{\mathbf{s}}})$, giving us boosted spinors that we will write as

:::{math}
:label: eq-spdirac-22
u(\pvec,{\hat{\mathbf{s}}}) = D(\pvec)u_0({\hat{\mathbf{s}}}), \qquad v(\pvec,{\hat{\mathbf{s}}})=D(\pvec)v_0({\hat{\mathbf{s}}}),
:::

without the 0-subscript. The boosted positive and negative energy solutions are now

:::{math}
:label: eq-spdirac-23
u(\pvec,{\hat{\mathbf{s}}})\,e^{-i(p\cdot x)/\hbar}, \qquad v(\pvec,{\hat{\mathbf{s}}})\,e^{+i(p\cdot x)/\hbar}.
:::

If we apply $H$ or $i\hbar\partial/\partial t$ to these to obtain their energies, we find that the positive energy solutions have energy $E$, given in terms of the momentum $\pvec$ which parameterizes the boost by {eq}`eq-spdirac-12`, while the negative energy solutions have energy $-E$. We see that when we boost a negative energy solution at rest, we obtain a solution whose energy is even more negative. Thus, the energy spectrum of the free particle Dirac Hamiltonian consists of a positive energy part ranging from $+mc^2$ to $\infty$, and a negative energy part ranging from $-mc^2$ to $-\infty$, as illustrated in {ref}`fig-spdirac-1`. There is an energy gap between $-mc^2$ and $+mc^2$.

:::{figure} images/spdirac-fig01.png
:label: fig-spdirac-1
:width: 20%

The energy spectrum of the free particle Dirac Hamiltonian consists of all positive energies $\ge +mc^2$ and all negative energies $\le -mc^2$. There is an energy gap between $-mc^2$ and $+mc^2$.
:::

The free particle solutions {eq}`eq-spdirac-23` are not only eigenfunctions of energy, they are also eigenfunctions of momentum. If we apply the operator $\pvec_op=-i\hbar\del$ to these solutions, we find that positive energy solutions are eigenfunctions of momentum with eigenvalue $\pvec$, while the negative energy solutions are eigenfunctions of momentum with eigenvalue $-\pvec$. We see that when we boost a negative energy solution at rest by a Lorentz transformation parameterized by $\pvec$, we obtain a solution with momentum $-\pvec$ (in the opposite direction of the boost). In a certain sense, the negative energy solutions have not only negative energy but also negative momentum.

We see that the negative energy solutions $v(\pvec,{\hat{\mathbf{s}}})e^{i(p\cdot x)/\hbar}$ have a momentum eigenvalue that is the opposite of the momentum label $\pvec$. The same is true for the spin label, on account of the minus sign introduced into our definition of $v_0({\hat{\mathbf{s}}})$ in {eq}`eq-spdirac-6`. The purpose of that minus sign was consistency in the labeling of the negative energy solutions; the way we have done it, both the spin and momentum eigenvalues of those solutions are the opposite of the spin and momentum labels. This convention will be convenient when we come to hole theory, in {ref}`ch-holedirac`.

(sec-spdirac-6)=

## Covariant Notation for Free Particle Solutions

Instead of labeling the $u$- and $v$-spinors by the 3-vectors $\pvec$ and ${\hat{\mathbf{s}}}$, it is convenient to use 4-vectors, as a part of a notation that is as covariant as possible. As for the momentum, we will simply label the spinors by $p$, which stands for the 4-momentum $p^\mu$ in {eq}`eq-spdirac-15`. Since the 4-momentum $p$ is a function of the 3-momentum $\pvec$, and since the 3-momentum $\pvec$ is the spatial part of the 4-momentum $p$, the new momentum label carries the same information as the old.

As for the spin, let us go back to the spinors before the boost, and promote the spin 3-vector ${\hat{\mathbf{s}}}$ into a 4-vector $s_0$ by defining

:::{math}
:label: eq-spdirac-24
s_0^\mu = \begin{pmatrix}0\\{\hat{\mathbf{s}}}\\\end{pmatrix},
:::

that is, $s_0^\mu$ is a purely spatial unit vector in the rest frame of the particle. Again, the 0-subscript means “at rest.” Notice that in the rest frame, the spin $s_0$ is purely space-like, while the momentum $p_0$ is purely time-like, so we have the dot products,

:::{math}
:label: eq-spdirac-25
p_0\cdot p_0 =m^2c^2, \qquad p_0\cdot s_0 =0, \qquad s_0\cdot s_0 = -1,
:::

the last being equivalent to ${\hat{\mathbf{s}}}\cdot{\hat{\mathbf{s}}}=1$.

Now when we boost the particle we boost the 4-vector $s_0$ along with it, writing

:::{math}
:label: eq-spdirac-26
s=\Lambda(\pvec) s_0, \qquad or \qquad s^\mu = \Lambda(\pvec)^\mu{}_\nu \, s_0^\nu.
:::

After the boost the 4-vector $s$ is a unit space-like vector in the rest frame of the particle, that is, it lies in the 3-dimensional hyperplane that is Minkowski orthogonal to the 4-momentum $p$. Because the Minkowski scalar product is preserved under Lorentz transformations, the boosted 4-vectors $p$ and $s$ satisfy the same dot product relations as the 4-vectors $p_0$ and $s_0$ at rest, that is,

:::{math}
:label: eq-spdirac-27
p\cdot p=m^2c^2, \qquad p\cdot s=0, \qquad s\cdot s = -1.
:::

We will henceforth label the boosted spinors {eq}`eq-spdirac-22` by the 4-vectors $p$ and $s$ instead of the 3-vectors $\pvec$ and ${\hat{\mathbf{s}}}$, that is, as $u(p,s)$ and $v(p,s)$. The notation is slightly illogical, since $u$ and $v$ are not functions of two independent 4-vectors $p$ and $s$, rather $p$ is a function of the 3-momentum $\pvec$ and $p$ and $s$ must satisfy {eq}`eq-spdirac-27`. Nevertheless, the notation is useful and convenient. Likewise, when we need to refer to the spinors at rest, we will henceforth write them as $u(p_0,s_0)$, $v(p_0,s_0)$ rather than $u_0({\hat{\mathbf{s}}})$, $v_0({\hat{\mathbf{s}}})$, as above.

Altogether, in this covariant notation, a complete set of solutions of the free particle Dirac equation is obtained from

:::{math}
:label: eq-spdirac-28
u(p,s)e^{-i(p\cdot x)/\hbar}, \qquad v(p,s)e^{+i(p\cdot x)/\hbar},
:::

by letting $\pvec$ run over all of 3-momentum space and allowing $s$ to run over two oppositely oriented unit vectors orthogonal to $p$, that is, in the rest frame of the particle.

Notice that if we apply the energy-momentum 4-vector of operators $p^\mu_op = i\hbar\,\partial^\mu$ to these solutions we obtain

:::{math}
:label: eq-spdirac-29
\begin{aligned}
p^\mu_op \,u(p,s)e^{-i(p\cdot x)/\hbar} &= +p^\mu\, u(p,s)e^{-i(p\cdot x)/\hbar}, \\
p^\mu_op \,v(p,s)e^{i(p\cdot x)/\hbar} &= -p^\mu\, v(p,s)e^{i(p\cdot x)/\hbar}. \\

\end{aligned}
:::

For the negative energy solutions, the energy-momentum eigenvalues are opposite the energy-momentum label $p$ of the solutions.

(sec-spdirac-7)=

## Geometrical Interpretation of the Spinors $u(p,s)$ and $v(p,s)$

A geometrical interpretation may be given of the manner in which the spinors $u(p,s)$ and $v(p,s)$ are parameterized. This takes place in 4-dimensional momentum space with coordinates $p^\mu$, that is, $E$ and $\pvec$. This space is sketched in {ref}`fig-spdirac-2`, in which the $z$-component is suppressed to make a drawing possible.

:::{figure} images/spdirac-fig02.png
:label: fig-spdirac-2
:width: 80%

The forward and backward mass shells, the surfaces upon which $E^2=m^2c^4 + c^2\pvec^2$, are illustrated, in 4-momentum space. Given a 3-momentum $\pvec$ (illustrated in only two dimensions in the figure), we can erect the vertical in the $E$ direction, which intersects the forward mass shell at the 4-momentum $p^\mu$. Directly opposite in 4-momentum space is the 4-momentum $-p^\mu$, on the backward mass shell. The $u$-spinors are associated with the point $p^\mu$ and the $v$-spinors with the point $-p^\mu$, so we call the forward mass shell the “$u$-shell” and the backward one the “$v$-shell.”
:::

:::{figure} images/spdirac-fig03.png
:label: fig-spdirac-3
:width: 80%

An enlarged view of the point with coordinates $p^\mu$ on the forward ($u$) mass shell. The “plane” (really a 3-dimensional space) tangent to the mass shell at this point contains vectors that are Minkowski orthogonal to $p^\mu$, that is, they are purely spatial in the rest frame of the particle. Two opposite unit vectors $s^\mu$ and $-s^\mu$ are chosen in this plane which specify the polarization of the spin.
:::


{ref}`fig-spdirac-3` contains a magnified picture of the point on the forward or $u$- mass shell with coordinates $p^\mu$. The plane tangent to the mass shell at the point is illustrated. In the diagram it is a plane, but really it is a 3-dimensional space. Vectors in this plane are Minkowski orthogonal to $p^\mu$, so they represent 4-vectors that are purely spatial in the rest frame of the particle. Two unit vectors in this plane are illustrated, $s^\mu$ and $-s^\mu$, which represent two polarizations for the spin, and correspond to the spinors $u(p,\pm s)$. A similar diagram applies on the backward or $v$-shell. By convention, the spinor $v(p,s)$ has 4-momentum $-p$ and is polarized in the direction $-s$.

(sec-spdirac-8)=

## The Spinors $u(p,s)$ and $v(p,s)$ as Covariant Eigenspinors

The spinors $u(p,s)$ and $v(p,s)$ can be characterized in covariant notation as eigenspinors of certain Dirac matrices. First, the spinors $u(p_0,s_0)$ and $v(p_0,s_0)$ at rest are eigenspinors of $\gamma^0$, as we see from {eq}`eq-covariance-14` and {eq}`eq-spdirac-6`,

:::{math}
:label: eq-spdirac-30
\gamma^0 u(p_0,s_0) = u(p_0,s_0), \qquad \gamma^0 v(p_0,s_0) = -v(p_0,s_0).
:::

The eigenspaces of $\gamma^0$ are 2-dimensional. But

:::{math}
:label: eq-spdirac-31
\gamma^0 = {p_0 \cdot \gamma \over mc} = {\pslash_0 \over mc},
:::

so we have

:::{math}
:label: eq-spdirac-32a
\begin{aligned}
\pslash_0 u(p_0,s_0) &= mc\,u(p_0,s_0),
\end{aligned}
:::

:::{math}
:label: eq-spdirac-32b
\begin{aligned}
\pslash_0 v(p_0,s_0) &= -mc\,v(p_0,s_0).
\end{aligned}
:::

Let us now boost these equations. Applying $D(\pvec)$ to {eq}`eq-spdirac-32a`, we find

:::{math}
:label: eq-spdirac-33
\begin{aligned}
D(\pvec) \pslash_0 u(p_0,s_0) &= D(\pvec) (p_0 \cdot \gamma) D(\pvec)^{-1} D(\pvec) u(p_0,s_0) = \bigl(p_0 \cdot (\Lambda^{-1} \gamma)\bigr) u(p,s) \\
&= \bigl((\Lambda \,p_0)\cdot \gamma\bigr) u(p,s) = (p\cdot\gamma) u(p,s) = \pslash\,u(p,s) = mc \,D(\pvec)u_0 = mc \, u(p,s), \\

\end{aligned}
:::

where we use {eq}`eq-covariance-42` in the second equality. Applying $D(\pvec)$ in a similar manner to {eq}`eq-spdirac-32b` gives us altogether

:::{math}
:label: eq-spdirac-34
(\pslash-mc)u(p,s)=0, \qquad (\pslash+mc)v(p,s)=0.
:::

The spinors $u(p,s)$ and $v(p,s)$ are eigenspinors of $\pslash$ with eigenvalues $+mc$ and $-mc$, respectively. Equations~{eq}`eq-spdirac-32a` are special cases of {eq}`eq-spdirac-34` (for the particle at rest). Equations~{eq}`eq-spdirac-34` gives us covariant way of characterizing the $p$-dependence of the spinors $u(p,s)$ and $v(p,s)$.

Please note that {eq}`eq-spdirac-34` are purely spinor equations with no space-time dependence, and that $\pslash$ involves the $c$-number 4-vector $p^\mu$, not the operator vector $p^\mu_op$. The free particle Dirac equation in covariant form involves the operator 4-vector (see {eq}`eq-covariance-8` or {eq}`eq-covariance-13`),

:::{math}
:label: eq-spdirac-35
(\pslash_op-mc)\psi(x)=0.
:::

When we apply this to a positive energy solution, we get

:::{math}
:label: eq-spdirac-36
(\pslash_op-mc)u(p,s)e^{-i(p\cdot x)/\hbar} = (\pslash-mc)u(p,s)e^{-i(p\cdot x)/\hbar}=0,
:::

since $p^\mu_op$ just brings out $p^\mu$ from the exponent. When we apply it to a negative energy solution, we get

:::{math}
:label: eq-spdirac-37
(\pslash_op-mc)v(p,s)e^{+i(p\cdot x)/\hbar}= (-\pslash-mc)v(p,s)e^{+i(p\cdot x)/\hbar} =0,
:::

since $p^\mu_op$ brings out $-p^\mu$ from the exponent. We have used {eq}`eq-spdirac-34` in the final step in both these results.

Equations~{eq}`eq-spdirac-34` can be used to construct projection operators $\Pi_\pm$, which when applied to an arbitrary spinor project out the positive and negative energy components. These are

:::{math}
:label: eq-spdirac-38
\Pi_\pm = {mc \pm \pslash\over 2mc},
:::

and they satisfy

:::{math}
:label: eq-spdirac-39
(\Pi_+)^2 = \Pi_+, \quad (\Pi_-)^2 = \Pi_-, \quad \Pi_+\Pi_-=\Pi_-\Pi_+=0, \quad \Pi_+ + \Pi_- = 1,
:::

which says that they are complementary projectors. They also satisfy

:::{math}
:label: eq-spdirac-40
\Pi_+u(p,s)=u(p,s), \quad \Pi_+v(p,s)=0, \quad \Pi_-u(p,s)=0, \quad \Pi_-v(p,s)=v(p,s),
:::

which shows how they project out the positive and negative energy components of an arbitrary linear combination of positive and negative energy spinors.

One can also give a covariant way of characterizing the $s$-dependence of $u(p,s)$ and $v(p,s)$. It turns out that these spinors are eigenspinors of $\sslash\gamma_5$, and that projection operators can be constructed that project out the positive or negative components of spin along the spin vector $s$. See Prob.~\prbrspdirac-1.

(sec-spdirac-9)=

## Orthonormality Relations for the Spinors $u(p,s)$ and $v(p,s)$

The spinors $u(p,s)$ and $v(p,s)$ satisfy two types of orthonormality relations, one the adjoint and the other the Hermitian. The adjoint relations are a bit easier to derive, so we present these first. The relations are

:::{math}
:label: eq-spdirac-41a
\begin{aligned}
\ubar(p,s) u(p,s') &= \delta_{ss'},
\end{aligned}
:::

:::{math}
:label: eq-spdirac-41b
\begin{aligned}
\ubar(p,s) v(p,s') &= \vbar(p,s) u(p,s')=0,
\end{aligned}
:::

:::{math}
:label: eq-spdirac-41c
\begin{aligned}
\vbar(p,s) v(p,s') &= -\delta_{ss'},
\end{aligned}
:::

where $s'$ takes on only two values, $\pm s$, so that $s'$ is a polarization the same as $s$ or in the opposite direction in the rest frame. There is also the completeness relation,

:::{math}
:label: eq-spdirac-42
1 = \sum_{\pm s} \bigl[u(p,s)\ubar(p,s) - v(p,s)\vbar(p,s)\bigr],
:::

where 1 represents the $4\times4$ identity matrix, where the sum is taken over a polarization vector and its opposite, and the outer product of a column spinor times a row spinor is implied.

{eq}`eq-spdirac-41a` may be proved as follows:

:::{math}
:label: eq-spdirac-43
\begin{aligned}
\ubar(p,s) u(p,s') &= u^\dagger(p,s)\gamma^0 u(p,s') = u^\dagger(p_0,s_0)D(\pvec)^\dagger \gamma^0 D(\pvec) u(p_0,s'_0) \\
&=u^\dagger(p_0,s_0)\gamma^0 \gamma^0 D(\pvec)^\dagger \gamma^0 D(\pvec)u(p_0,s'_0) \\
&=u^\dagger(p_0,s_0)\gamma^0 D(\pvec)^{-1}D(\pvec) u(p_0,s'_0) = \ubar(p_0,s_0)u(p_0,s'_0),
\end{aligned}
:::

where we use {eq}`eq-covariance-78`. Thus $\ubar(p,s)u(p,s)$ is unchanged when referred to the rest frame. But

:::{math}
:label: eq-spdirac-44
\ubar(p_0,s_0)u(p_0,s'_0) = u^\dagger(p_0,s_0)\gamma^0 u(p_0,s'_0) = u^\dagger(p_0,s_0)u(p_0,s'_0) = \bigl(\chi^\dagger({\hat{\mathbf{s}}}), 0\bigr) \begin{pmatrix}\chi({\hat{\mathbf{s}}}')\\ 0\\\end{pmatrix} = \delta_{ss'},
:::

where we use {eq}`eq-spdirac-30`. Equations.~{eq}`eq-spdirac-41b` and {eq}`eq-spdirac-41c` may be proved similarly, as may the completeness relation {eq}`eq-spdirac-42`.

The Hermitian orthonormality relations involve a modified 4-vector $\tilde p$, defined by $\tilde p = \Lambda(-\pvec)p_0$, that is,

:::{math}
:label: eq-spdirac-45
{\tilde p}^\mu = \Lambda(-\pvec)^\mu{}_\nu \, p_0^\nu = \begin{pmatrix}E/c \\ -\pvec\\\end{pmatrix}.
:::

These are

:::{math}
:label: eq-spdirac-46a
\begin{aligned}
u^\dagger(p,s) u(p,s') &= {E\over mc^2}\, \delta_{ss'},
\end{aligned}
:::

:::{math}
:label: eq-spdirac-46b
\begin{aligned}
u^\dagger(p,s) v({\tilde p},s') &= v^\dagger(p,s) u({\tilde p},s') = 0,
\end{aligned}
:::

:::{math}
:label: eq-spdirac-46c
\begin{aligned}
v^\dagger(p,s) v(p,s') &= {E\over mc^2}\, \delta_{ss'},
\end{aligned}
:::

where again, for given $s$, the vector $s'$ takes on only the two values, $\pm s$. The proofs of these relations will be left as an exercise.

(sec-spdirac-10)=

## The Gordon Decomposition of the Current

The next topic gives us some insight into why the velocity operator $\vvec=c\alphavec$ is a purely spin operator in the Dirac theory, in contrast to the nonrelativistic theory. The velocity operator appears in the Heisenberg equations of motion, in the probability current, and other places. See the discussion in {ref}`sec-dirac-8`.

We will work with the covariant version of the Dirac equation for a particle interacting with an external electromagnetic field, {eq}`eq-covariance-11`. We write this equation in the form,

:::{math}
:label: eq-spdirac-47
i\hbar\,\gamma^\nu\frac{\partial \psi}{\partial x^\nu} -{q\over c} A_\nu \gamma^\nu \psi = mc\,\psi.
:::

We multiply this on the left by by $\psibar\gamma^\mu$, which causes the current to appear on the right hand side,

:::{math}
:label: eq-spdirac-48
i\hbar\Bigl(\psibar \gamma^\mu \gamma^\nu \frac{\partial \psi}{\partial x^\nu} \Bigr)-{q\over c} A_\nu (\psibar \gamma^\mu \gamma^\nu \psi) = mc\,(\psibar \gamma^\mu \psi) = m J^\mu.
:::

The right hand side of this equation is real but the left hand side is not obviously so. To bring out the reality, we take the complex conjugate of {eq}`eq-spdirac-48`, which, after the use of {eq}`eq-covariance-79`, can be written

:::{math}
:label: eq-spdirac-49
-i\hbar\Bigl(\frac{\partial \psibar}{\partial x^\nu}\gamma^\nu\gamma^\mu\psi \Bigr)-{q\over c} A_\nu (\psibar \gamma^\nu\gamma^\mu\psi) = mJ^\mu.
:::

We add these two together. The terms involving $A_\nu$ give

:::{math}
:label: eq-spdirac-50
-{q\over c} A_\nu [\psibar(\gamma^\mu\gamma^\nu + \gamma^\nu\gamma^\mu)\psi] = -{q\over c} A_\nu[\psibar( 2g^{\mu\nu})\psi]= -2\psibar\Bigl({q\over c}A^\mu\Bigr)\psi.
:::

As for the terms involving the derivatives of $\psi$, we use

:::{math}
:label: eq-spdirac-51
\gamma^\mu\gamma^\nu = {1\over2} \{\gamma^\mu,\gamma^\nu\} + {1\over 2} [\gamma^\mu,\gamma^\nu] = g^{\mu\nu} -i\sigma^{\mu\nu}
:::

(see {eq}`eq-covariance-18` and {eq}`eq-covariance-55`), to obtain

:::{math}
:label: eq-spdirac-52
i\hbar\Bigl[\psibar(g^{\mu\nu}-i\sigma^{\mu\nu}) \frac{\partial \psi}{\partial x^\nu}\Bigr]- i\hbar\Bigl[\frac{\partial \psibar}{\partial x^\nu} (g^{\mu\nu}+i\sigma^{\mu\nu}) \psi\Bigr] = 2\Re(\psibar i\hbar\partial^\mu \psi) + \hbar\pop{}{x^\nu} (\psibar \sigma^{\mu\nu}\psi).
:::

Altogether, we obtain

:::{math}
:label: eq-spdirac-53
J^\mu ={1\over m}\Re\Big[\psibar\Bigl(i\hbar\,\partial^\mu - {q\over c}A^\mu \Bigr)\psi\Bigr] + {\hbar\over 2m} \pop{}{x^\nu} (\psibar\sigma^{\mu\nu}\psi),
:::

after dividing by $2m$.

{eq}`eq-spdirac-53` is the Gordon decomposition of the Dirac current. The first term is obviously a generalization of the Klein-Gordon current (see {eq}`eq-kleing-27`, with the addition of the interaction with an electromagnetic field. The Klein-Gordon current, in turn, is a relativistic generalization of the probability current for a spinless, nonrelativistic particle, given in {eq}`eq-tevolut-57`. This term alone is called the *convection* current, since it involves only the purely spatial operator $p^\mu_op = i\hbar\,\partial^\mu$, which describes the state of motion of the particle. The second term in {eq}`eq-spdirac-53` is called the *magnetization* current, since it is the relativistic generalization of the magnetization current that was introduced in {ref}`sec-jjcouple-6`.

In summary, the Gordon decomposition of the current shows us that the velocity operator $\dot{\xvec}=c\alphavec$ in the Dirac theory, a purely spin operator, corresponds to the entire current of the nonrelativistic theory, including the magnetization current. We may point out that the Dirac version of the classical $\vvec\cross\Bvec$ force that a charged particle experiences in a magnetic field is $c\alphavec\cross\Bvec$, as shown by {eq}`eq-dirac-41`. That is, the magnetization current contributes to the $\vvec\cross\Bvec$ force, which is what we would expect physically.

(sec-spdirac-11)=

## The Zitterbewegung

Other strange features of the Dirac velocity operator $\vvec=\dot{\xvec}=c\alphavec$ that were discussed in {ref}`sec-dirac-8` included the fact that the velocity is not constant, even for a free particle, and the fact that the different components of the velocity do not commute with one other. We return now to the Heisenberg equations of motion, the subject of {ref}`sec-dirac-8`, working for simplicity with the case of a free particle.

Specializing the results of {ref}`sec-dirac-8` to the case of a free particle, we obtain the Heisenberg equations of motion for $\xvec$ and $\pvec=\pivec$, that is, $\dot{\xvec}=c\alphavec$, $\dot{\pvec}=0$ (we henceforth omit the hats on the momentum operator). As for $\alphavec$, we work out the Heisenberg equations of motion as follows:

:::{math}
:label: eq-spdirac-54
i\hbar\, {\dot\alpha}_i = [\alpha_i,H] = \alpha_i H - H\alpha_i = 2\alpha_iH - \alpha_iH - H\alpha_i = 2\alpha_iH -\{\alpha_i,H\}.
:::

We write it this way because the anticommutator of $\alphavec$ with $H$ is easier to work out than the commutator. Using {eq}`eq-dirac-8` we get the anticommutator,

:::{math}
:label: eq-spdirac-55
\{\alpha_i,H\} = c\{\alpha_i,\alphavec\cdot\pvec\} = c\{\alpha_i,\alpha_j\}p_j = 2c\,\delta_{ij}\,p_j = 2cp_i.
:::

Thus we have

:::{math}
:label: eq-spdirac-56
\dot{\alphavec} = -{2i\over\hbar}(\alphavec H-c\pvec).
:::

What makes this equation easy to solve is the fact that both $H$ and $\pvec$ are constants of motion. One way to solve an operator equation like {eq}`eq-spdirac-56` is to interpret all the quantities as $c$-numbers, then to solve the $c$-number equation as an ordinary differential equation, then to use that solution to guess the solution to the operator equation, which can be checked by back-substitution. In this case, the quantities $H$ and $\pvec$ in the $c$-number equation are taken as constants. Of course operators do not commute in general while $c$-numbers do, so we can expect that the $c$-number equation can be wrong by an ordering of operators, which we must take into account when making the guess. In this case the procedure is straightforward; {eq}`eq-spdirac-56` interpreted as a $c$-number equation can be easily solved by Lagrange's method of variation of parameters, and the solution makes it easy to guess the solution to the operator equation. In this way we find the solution to the Heisenberg equation of motion {eq}`eq-spdirac-56`,

:::{math}
:label: eq-spdirac-57
\alphavec(t)={c\pvec\over H} + \Bigl[ \alphavec(0) - {c\pvec\over H}\Bigr]e^{-2iHt/\hbar}.
:::

This can be checked by back substitution.

In this solution $c\pvec/H$ means the operator $c\pvec$ multiplied by the operator $1/H$. It does not matter which order we do the multiplication, because $\pvec$ and $H$ commute (otherwise the notation $c\pvec/H$ would be ambiguous). Also, we note that $1/H$ is defined because the spectrum of $H$ (see {ref}`fig-spdirac-1`) has an energy gap from $-mc^2$ to $+mc^2$ and does not include $E=0$.

To interpret this equation we multiply through by $c$ to get the velocity operator,

:::{math}
:label: eq-spdirac-58
\vvec(t) = {c^2\pvec\over H} + \Bigl[\vvec(0) -{c^2\pvec\over H}\Bigr] e^{-2iHt/\hbar}.
:::

We integrate this with respect to time, obtaining

:::{math}
:label: eq-spdirac-59
\xvec(t) = \xvec(0) + {c^2\pvec t\over H} + \Bigl[\vvec(0) -{c^2\pvec\over H}\Bigr] \Bigl[{e^{-2iHt/\hbar} -1 \over (-2iH/\hbar)}\Bigr],
:::

the solution for the position operator $\xvec(t)$ in the Heisenberg picture.

The first term of {eq}`eq-spdirac-58`, interpreted classically, is exactly the classical expression for the velocity as a function of the momentum in special relativity. See {eq}`eq-dirac-39`. It is, moreover, constant in time, as we expect for the velocity of a free particle in relativistic mechanics. We know, however, that the velocity does not commute with the Hamiltonian in the Dirac theory, so the velocity is not really a constant. The time dependence is contained in the second term in {eq}`eq-spdirac-58`, which contains the factor $e^{-2iHt/\hbar}$.

To understand this time dependence better, we take the expectation value of {eq}`eq-spdirac-58` with respect to a state $\psi$ that contains mainly positive energy solutions of energy close to $+mc^2$, that is, an essentially nonrelativistic state. This is all in the Heisenberg picture, so $\psi$ is the initial wave function. Then the Hamiltonian applied to this state brings out a quantity of order $mc^2$, and the operator $e^{-2iHt/\hbar}$ behaves like the phase factor $e^{-2imc^2t/\hbar}$. This factor oscillates on a time scale of order $\tau=\hbar/mc^2\approx 1.3\times 10^{-21}sec$, which is of order $\alpha^2\approx 1/(137)^2$ times smaller than the (already short) time scale in atomic units. See {ref}`tbl-hydrogen-1`.

For $t\ll\tau$ we can replace the exponential $e^{-2iHt/\hbar}$ by simply 1, and {eq}`eq-spdirac-58` and {eq}`eq-spdirac-59` become

:::{math}
:label: eq-spdirac-60
\begin{aligned}
\vvec(t) &= \vvec(0), \qquad t\ll\tau,
\end{aligned}
:::

:::{math}
:label: eq-spdirac-61
\begin{aligned}
\xvec(t) &= \xvec(0) + \vvec(0)t, \qquad t\ll\tau.
\end{aligned}
:::

On this time scale the expectation value of $\xvec$ moves in a straight line. Also, since the eigenvalues of each component of $\alpha$ are $\pm1$, the electron moves at a velocity comparable to the speed of light, so the distance covered in time $\tau$, before the phase factor $e^{-2imc^2t/\hbar}$ has a chance to change sign, is of order

:::{math}
:label: eq-spdirac-62
c\tau = {\hbar\over mc},
:::

that is, the Compton wavelength.

If the particle is essentially nonrelativistic then the the expectation value of first term in {eq}`eq-spdirac-58` is $\ll c$, so it is small in comparison to the second term. But on time scales $\gg\tau$, the second term averages to zero, while the integral of the first term continues to accumulate. Thus on longer time scales, we have

:::{math}
:label: eq-spdirac-63
\begin{aligned}
\vvec(t) &= {c^2\pvec\over E},\qquad t\gg\tau,
\end{aligned}
:::

:::{math}
:label: eq-spdirac-64
\begin{aligned}
\xvec(t) &= \xvec(0) + {c^2\pvec t\over E},\qquad t\gg\tau,
\end{aligned}
:::

and the expectation value of the particle position follows a straight line at constant velocity, as we would expect from classical relativistic mechanics.

The rapid motion of the particle on a time scale of $\tau$ and a length scale of the Compton wavelength was first pointed out by Schr\"odinger in 1930, who called it the *Zitterbewegung*, German for “jittering motion.” An interesting feature of the Zitterbewegung is that it is not present in a wave packet consisting solely of positive energy solutions. See Prob.~\prbrspdirac-5. The Zitterbewegung, when present, arises from the interference between the positive and negative energy solutions.

For this reason we may question if the negative energy solutions are real. Perhaps we should just declare them to be nonphysical, then we would not have to interpret them and the Zitterbewegung would go away.

Unfortunately, this does not work, for quite a few reasons. First of all, we can solve the Dirac equation for other problems besides the free particle. For example, the Dirac equation for the hydrogen atom is exactly solvable, and it gives positive energy solutions in good agreement with experiment, including the fine structure. These positive energy solutions can be expanded as linear combinations of free particle solutions, but the positive energy free particle solutions by themselves do not form a complete set. Thus, the expansion of (say) the ground state wave function of the Dirac hydrogen atom as a linear combination of free particle solutions will necessarily contain some negative energy components. In addition, the solution of the Dirac hydrogen atom also possesses negative energy solutions, and we have (at this point) no more physical interpretation for them than we do for the negative energy solutions for the free particle. But if we are going to declare them nonphysical, we now have a problem: Are we going to declare the negative energy free particle solutions nonphysical, or the negative energy hydrogen atom solutions? These two classes of negative energy solutions do not span the same subspace of the Dirac Hilbert space.

On the other hand, if we accept the negative energy free particle solutions, then we must have Zitterbewegung in any state that is a linear combination of both positive and negative free particle solutions. But we have just seen that the Dirac hydrogen atom wave functions are precisely such linear combinations. So does the Zitterbewegung exist in hydrogen? The answer is yes, it lies behind the Darwin term, as explained in {ref}`sec-finestruc-2`. We will make a more careful analysis of the relation between the Darwin and other fine structure terms and the Dirac equation in a later set of notes, but for now we can see that there is no option to naively discard the negative energy solutions.

Ultimately we will see that the negative energy solutions of the free particle Dirac equation are related to positrons, the antiparticle of the electron, and that the Zitterbewegung is related to the fact that when an electron interacts with a potential, such as the potential of the nucleus in the hydrogen atom, there arises some finite amplitude for the formation of an electron-positron pair. That is, for brief periods of time, at least, there exist three particles instead of just one: two electrons and one positron. But in the early history of the Dirac equation, no one suspected the existence of antimatter, so these interpretations lay in the future.

(sec-spdirac-12)=

## Central Force Motion and Complete Sets of Commuting Observables

In the case of a central force potential the time-independent Dirac equation can be reduced to a pair of one-dimensional, first-order, coupled radial wave equations, a generalization of the single second-order radial wave equation that arises in the nonrelativistic theory (see {eq}`eq-cenforce-7` and {eq}`eq-cenforce-11` for the latter). In some cases the Dirac radial wave equations can be solved in terms of standard special functions of mathematical physics. The main example that we are interested in is the Coulomb potential, but part of the analysis applies to any central force problem so we treat that first. The Coulomb potential (for hydrogen-like atoms) is covered in Secs.~\secrspdirac-16--18. For the rest of these notes we use natural units ($\hbar=c=1$), except at the end where we restore ordinary units when presenting results.

We seek the energy eigenvalues and eigenfunctions of the Dirac Hamiltonian in a central force potential, that is, we wish to solve

:::{math}
:label: eq-spdirac-65
H\psi=E\psi,
:::

where

:::{math}
:label: eq-spdirac-66
H=\alphavec\cdot\pvec + V(r) + m\beta.
:::

We identify the potential $V(r)$ with $q\Phi(r)$ in problems with electrostatic fields.

We appeal to the fine structure model of atoms (see {ref}`ch-finestruc`) for hints as to how to proceed, since this model incorporates relativistic effects to order $(v/c)^2$, relative to nonrelativistic energies. We recall that a complete set of commuting observables in the fine structure model is $(H,L^2,J^2,J_z)$. Of these, $H$, $J^2$ and $J_z$ are commuting observables also in the relativistic (Dirac) problem, since $\Jvec=\Lvec+(1/2)\Sigmavec$ commutes with the Hamiltonian {eq}`eq-spdirac-66`. However, $[L^2,H]\ne0$, as we find by a direct calculation of the commutator, so $L^2$ cannot be used as a member of the complete set in the relativistic theory and must be replaced by some other operator. In a moment we will see what the choices for this (fourth) operator are.

Accepting that $J^2$ and $J_z$ will be members of our complete set, we begin by looking for the most general eigenfunction of these with quantum numbers $(jm_j)$. We work in the Dirac-Pauli representation of the Dirac matrices, in which the matrices $\Sigmavec$ are block-diagonal,

:::{math}
:label: eq-spdirac-67
\begin{aligned}
\Sigmavec=\begin{pmatrix}\sigmavec & 0 \\ 0 & \sigmavec \\\end{pmatrix}.
\end{aligned}

:::

We break the 4-component Dirac spinor $\psi$ into two 2-component Pauli spinors,

:::{math}
:label: eq-spdirac-68
\psi=\begin{pmatrix}\phi \\ \chi \\\end{pmatrix},
:::

so that the action of the Dirac angular momentum $\Jvec=\Lvec+(1/2)\Sigmavec$ on $\psi$ is equivalent to the action of two Pauli angular momenta $\Jvec=\Lvec+(1/2)\sigmavec$ acting separately on $\phi$ and $\chi$. Thus the eigenfunctions of $J^2$ and $J_z$ in the Dirac theory are 4-component spinors $\psi$ in which both $\phi$ and $\chi$ are eigenfunctions of the Pauli operators $J^2$ and $J_z$, with the same quantum numbers $(jm_j)$.

Eigenfunctions of $(J^2,J_z)$ in the Pauli theory are conveniently expressed in terms of *spinor spherical harmonics*, which are 2-component spinors defined over the unit sphere. We define them by

:::{math}
:label: eq-spdirac-69
{\cal Y}^\ell_{jm_j}(\theta,\phi) = \sum_{m_\ell m_s}Y_{\ell m_\ell}(\theta,\phi)\, \chi_{m_s} \,\braket{\ell s m_\ell m_s}{jm_j},
:::

where $\chi_{m_s}$ for $m_s=\pm\frac{1}{2}$ are the spin-up and spin-down spinors (the unit vectors in spin space), and where in the Clebsch-Gordan coefficient $s$ has the value $\frac{1}{2}$. The spinor spherical harmonics are eigenfunctions of $L^2$ as well as $J^2$ and $J_z$, with quantum number $\ell$, which, for a given value of $j$ can take on only the values $\ell=j\pm 1/2$. Of course, $j$ is a half-integer, $j=\frac{1}{2}, \frac{3}{2}, \ldots$. We are seeing eigenfunctions of $L^2$ here because they arise when we construct eigenfunctions of $J^2$ and $J_z$ by the usual method of coupling $\ell\otimes\frac{1}{2}$, but since $[L^2,H]\ne0$ we do not expect to find energy eigenfunctions of the Dirac Hamiltonian that are also eigenfunctions of $L^2$. In any case, the spin spherical harmonics are eigenfunctions of $L^2$ only as Pauli spinors, not as Dirac spinors.

The Clebsch-Gordan coefficients in {eq}`eq-spdirac-69` can be worked out by the method of Prob. {ref}`prob-jjcouple-3`. These allow us to write out the explicit forms of the spin spherical harmonics,

:::{math}
:label: eq-spdirac-70
\begin{aligned}
{\cal Y}^{j-1/2}_{jm_j} &= {1\over\sqrt{2j}}\begin{pmatrix}\sqrt{j+m_j}\, Y_{j-1/2,m_j-1/2} \\  \sqrt{j-m_j}\,Y_{j-1/2,m_j+1/2}\\, \\  {\cal Y}^{j+1/2}_{jm_j}&={1\over\sqrt{2j+2}} \begin{pmatrix}-\sqrt{j-m_j+1}\, Y_{j+1/2,m_j-1/2} \\  \sqrt{j+m_j+1}\,Y_{j+1/2,m_j+1/2}\\,\\ 

\end{pmatrix}
\end{pmatrix}
\end{aligned}
:::

where each ${\cal Y}$ and each $Y$ is understood as a function of $(\theta,\phi)$. We note that the spinor spherical harmonics are orthonormal,

:::{math}
:label: eq-spdirac-71
\int d\Omega\, \bigl({\cal Y}^\ell_{jm_j}\bigr)^\dagger {\cal Y}^{\ell'}_{j'm'_j} = \delta_{\ell\ell'}\, \delta_{jj'}\,\delta_{m_jm'_j}.
:::

We can now write down the most general 2-component eigenfunction of $(J^2,J_z)$ with quantum numbers $(jm_j)$. It must be a linear combination of ${\cal Y}^\ell_{jm_j}$ for the two values $\ell=j\pm\frac{1}{2}$, where each of the coefficients is allowed to be an arbitrary function of $r$,

:::{math}
:label: eq-spdirac-72
A(r){\cal Y}^{j-1/2}_{jm_j}(\theta,\phi) + B(r) {\cal Y}^{j+1/2}_{jm_j}(\theta,\phi).
:::

From this it follows that the most general 4-component spinor that is an eigenfunction of the Dirac operators $(J^2,J_z)$ with eigenvalues $(jm_j)$ is of the form,

:::{math}
:label: eq-spdirac-73
\psi_{jm_j}(\xvec) = \begin{pmatrix} A(r){\cal Y}^{j-1/2}_{jm_j} + B(r) {\cal Y}^{j+1/2}_{jm_j} \\  C(r){\cal Y}^{j-1/2}_{jm_j} + D(r) {\cal Y}^{j+1/2}_{jm_j}\\\end{pmatrix},
:::

where $A(r)$, $B(r)$, $C(r)$ and $D(r)$ are four arbitrary radial wave functions and where the upper and lower 2-component spinors have the same $(jm_j)$ values. The radial wave functions will be determined by demanding that $\psi$ be an eigenfunction of the remaining members of our complete set of commuting observables.

(sec-spdirac-13)=

## The Fourth Observable and the Operator $K$

Now we can see some choices for the fourth observable in the complete set of the Dirac theory, the one that will replace $L^2$ in the fine structure model. The simplest choice is parity, which in the Dirac theory is discussed in {ref}`sec-covariance-14`. We write the Dirac parity operator as

:::{math}
:label: eq-spdirac-74
\pi=\pi_s\gamma^0,
:::

where $\pi_s$ takes care of the spatial part of parity,

:::{math}
:label: eq-spdirac-75
(\pi_s\psi)(\xvec)=\psi(-\xvec),
:::

and where $\gamma^0$ takes care of the spin part. The parity operator has an arbitrary $\pm$ sign (see {ref}`sec-covariance-14`), which we have chosen in {eq}`eq-spdirac-75` so as to make the intrinsic parity of the electron $+1$. In the case of 2-component (Pauli) spinors, the parity operator consists of $\pi_s$ alone, which takes $\phi(\xvec)$ into $\phi(-\xvec)$. See {ref}`ch-parity`.

When we apply $\pi_s$ to the Dirac spinor {eq}`eq-spdirac-73` it brings out $(-1)^\ell$ in each term, that is, $(-1)^{j\pm1/2}$. Thus the $A$ and $B$ terms acquire opposite signs, as do the $C$ and $D$ terms. But when we multiply the spinor by $\gamma^0$, the lower 2-component spinor acquires an additional phase of $-1$. Therefore if we require that the Dirac spinor {eq}`eq-spdirac-73` be an eigenstate of parity, then either $B=C=0$, in which case the parity is $(-1)^{j-1/2}$, or else $A=D=0$, in which case the parity is $(-1)^{j+1/2}$. We will write the simultaneous eigenfunctions of $(\pi,J^2,J_z)$ as

:::{math}
:label: eq-spdirac-76
\psi_{\kappa jm_j}(\xvec)=\begin{pmatrix} F(r){\cal Y}^{j-1/2}_{jm_j} \\  iG(r) {\cal Y}^{j+1/2}\\\end{pmatrix}, \qquad \psi_{\kappa jm_j}(\xvec)=\begin{pmatrix} F(r){\cal Y}^{j+1/2}_{jm_j} \\  iG(r){\cal Y}^{j-1/2}_{jm_j}\\\end{pmatrix},
:::

where the first and second spinors have parity $(-1)^{j-1/2}$ and $(-1)^{j+1/2}$, respectively, where the arbitrary radial wave functions are now written as $F$ and $G$ and where for later convenience we have split off a factor of $i$ in the lower component. We see that indeed these spinors are not eigenfunctions of $L^2$, which has a different value in the upper and lower components.

We have introduced a new quantum number $\kappa$ in {eq}`eq-spdirac-76`, which is related to the eigenvalue of a new operator $K$. This operator serves as well as parity for creating a complete set, but it is not as obvious a choice. It is defined by

:::{math}
:label: eq-spdirac-77
K=\beta(\Lvec\cdot\Sigmavec+1).
:::

This is a scalar under spatial rotations so it commutes with $\Jvec$. It also commutes with parity $\pi$, that is, it is a true scalar, not a pseudoscalar.

The fact that it also commutes with $H$ follows from a straightforward but not very illuminating calculation. First note the commutator $[\beta,\Sigmavec]=0$ and the identity,

:::{math}
:label: eq-spdirac-78
\alpha_i\Sigma_j= \Sigma_i\alpha_j = \delta_{ij}\,\gamma_5 + i\epsilon_{ijk} \,\alpha_k,
:::

which follows from the definitions {eq}`eq-dirac-11` and {eq}`eq-covariance-104` and which implies

:::{math}
:label: eq-spdirac-79
\{\alpha_i,\Sigma_j\} = 2\delta_{ij}\,\gamma_5, \qquad [\alpha_i,\Sigma_j] = 2i\epsilon_{ijk}\,\alpha_k.
:::

To compute $[K,H]$ we need the commutator,

:::{math}
:label: eq-spdirac-80
\begin{aligned}
[\beta(\Lvec\cdot\Sigmavec),\alphavec\cdot\pvec]&= \beta(\Lvec\cdot\Sigmavec)(\alphavec\cdot\pvec)- (\alphavec\cdot\pvec)\beta(\Lvec\cdot\Sigmavec) =\beta[(\Lvec\cdot\Sigmavec)(\alphavec\cdot\pvec)+ (\alphavec\cdot\pvec)(\Lvec\cdot\Sigmavec)] \\
&=\beta\{\Lvec\cdot\Sigmavec,\alphavec\cdot\pvec\},
\end{aligned}
:::

which is expressed in terms of an anticommutator as shown. As for the latter, we migrate factors in the second term,

:::{math}
:label: eq-spdirac-81
(\alphavec\cdot\pvec)(\Lvec\cdot\Sigmavec)= \alpha_i p_i L_j \Sigma_j = \alpha_i L_j p_i \Sigma_j + i\epsilon_{ijk} \,\alpha_i p_k \Sigma_j,
:::

using {eq}`eq-transfop-21`. We continue to migrate factors in the first term in this expression,

:::{math}
:label: eq-spdirac-82
\alpha_i L_j p_i \Sigma_j = \alpha_i L_j \Sigma_j p_i = L_j \alpha_i \Sigma_j p_i = - L_j \Sigma_j \alpha_i p_i + 2\delta_{ij}\,\gamma_5 L_j p_i = -(\Lvec\cdot\Sigmavec)(\alphavec\cdot\pvec),
:::

since $\Lvec\cdot\pvec=0$. This cancels the first term of the anticommutator in {eq}`eq-spdirac-80`. As for the second term in {eq}`eq-spdirac-81`, it is

:::{math}
:label: eq-spdirac-83
i\epsilon_{ijk} \,\alpha_i p_k \Sigma_j = i\epsilon_{ijk}\,\alpha_i \Sigma_j p_k = i\epsilon_{ijk}\,(\delta_{ij}\, \gamma_5 +i\epsilon_{ij\ell}\,\alpha_\ell)p_k =-2\delta_{k\ell}\,\alpha_\ell p_k,
:::

which gives finally for the commutator {eq}`eq-spdirac-80`,

:::{math}
:label: eq-spdirac-84
[\beta(\Lvec\cdot\Sigmavec),\alphavec\cdot\pvec] = -2\beta(\alphavec\cdot\pvec).
:::

The other commutators we need are $[K,\beta]=0$ and

:::{math}
:label: eq-spdirac-85
[\beta,\alphavec\cdot\pvec] = 2\beta(\alphavec\cdot\pvec),
:::

so that on adding {eq}`eq-spdirac-84` and {eq}`eq-spdirac-85` and assembling the pieces we obtain $[K,H]=0$.

In view of these commutators we will henceforth take $(H,K,J^2,J_z)$ as our complete set of commuting operators, although parity $\pi$ could be used in place of $K$.

To obtain the spectrum of $K$ we first note that for the Dirac angular momentum $\Jvec=\Lvec+(1/2)\Sigmavec$ we have

:::{math}
:label: eq-spdirac-86
J^2=L^2+\Lvec\cdot\Sigmavec+{3\over4}.
:::

Next we look at the square of $K$,

:::{math}
:label: eq-spdirac-87
K^2 = \beta(\Lvec\cdot\Sigmavec+1)\beta (\Lvec\cdot\Sigmavec+1) = (\Lvec\cdot\Sigmavec+1)^2 =(\Lvec\cdot\Sigmavec)^2 + 2\Lvec\cdot\Sigmavec +1.
:::

We evaluate the first term of this result with the help of {eq}`eq-hilbert-148`,

:::{math}
:label: eq-spdirac-88
(\Lvec\cdot\Sigmavec)^2 = L^2 + i\Sigmavec\cdot(\Lvec\times \Lvec),
:::

which is a little tricky, since $\Lvec\cross\Lvec=i\Lvec$ is not zero, rather it is equivalent to the commutation relations $[L_i,L_j]=i\epsilon_{ijk}\,L_k$. Thus we obtain

:::{math}
:label: eq-spdirac-89
K^2 = L^2 + \Lvec\cdot\Sigmavec+1 = J^2+{1\over4},
:::

and when we apply $K^2$ to an eigenstate of $J^2$ with eigenvalue $j$, it brings out $j(j+1)+1/4=(j+1/2)^2$. Therefore the eigenvalues of $K$ are $\pm(j+1/2)$.

To apply $K$ to the wave functions {eq}`eq-spdirac-76` we need the action of the Pauli operator $\Lvec\cdot\sigmavec$ on the spinor spherical harmonics. Since the Pauli angular momentum is given by $\Jvec=\Lvec+(1/2)\sigmavec$, we have

:::{math}
:label: eq-spdirac-90
J^2 = L^2 + \Lvec\cdot\sigmavec + {3\over 4},
:::

which looks like {eq}`eq-spdirac-86` but is a Pauli, not a Dirac, operator. This implies

:::{math}
:label: eq-spdirac-91
(\Lvec\cdot\sigmavec) {\cal Y}^\ell_{jm_j} = \Bigl[j(j+1)-\ell(\ell+1)-{3\over 4}\Bigr] {\cal Y}^\ell_{jm_j},
:::

which in turn implies, for the two values $\ell=j\pm 1/2$,

:::{math}
:label: eq-spdirac-92
\begin{aligned}
(\Lvec\cdot\sigmavec+1){\cal Y}^\ell_{jm_j} =\begin{cases}+(j+\frac{1}{2}){\cal Y}^\ell_{jm_j}, & \ell=j-\frac{1}{2},\\  -(j+\frac{1}{2}){\cal Y}^\ell_{jm_j}, & \ell=j+\frac{1}{2},\\\end{cases}
\end{aligned}

:::

These show that if we apply the Pauli operator $\Lvec\cdot\sigmavec+1$ to the upper and lower components of the Dirac spinors {eq}`eq-spdirac-76`, we bring out a factor of $+(j+\frac{1}{2})$ in one component and $-(j+\frac{1}{2})$ in the other. But then when we multiply by $\beta$, the entire Dirac spinor acquires an overall factor, which is the eigenvalue $(j+\frac{1}{2})$ of $K$ for the first spinor in {eq}`eq-spdirac-76` and $-(j+\frac{1}{2})$ for the second. Thus the eigenvalue of $K$ distinguishes the two spinors in {eq}`eq-spdirac-76`. It is customary in the literature to denote the negative of the eigenvalue of $K$ by $\kappa$, which has the value $\kappa=-(j+\frac{1}{2})$ for the first spinor in {eq}`eq-spdirac-76` and $\kappa=+(j+\frac{1}{2})$ in the second. The extra minus sign is confusing, but we fear greater confusion if we change the convention. {ref}`tbl-spdirac-1` summarizes the relations among $\kappa$, the parity, and the angular momentum quantum number $\ell$ attached to the upper and lower components of the Dirac spinors {eq}`eq-spdirac-76`.

:::{table} Values of $\ell$ quantum number for upper and lower spinors and overall parity, as a function of $k$, the eigenvalue of $K$.
:label: tbl-spdirac-1

| $\kappa$ | $\ell(\text{upper})$ | $\ell(\text{lower})$ | $\pi$ |
|:---:|:---:|:---:|:---:|
| $-(j + \frac{1}{2})$ | $j - \frac{1}{2}$ | $j + \frac{1}{2}$ | $(-1)^{j-1/2}$ |
| $+(j + \frac{1}{2})$ | $j + \frac{1}{2}$ | $j - \frac{1}{2}$ | $(-1)^{j+1/2}$ |

:::
Recall that in the nonrelativistic limit, the upper 2-component spinor of the Dirac theory becomes the Pauli spinor of the nonrelativistic theory. See {ref}`sec-dirac-9`. In the case of the Dirac spinors {eq}`eq-spdirac-76`, we see that the $\ell$ quantum number of the nonrelativistic limit is the one labeled $\ell{\rm(upper)}$ in {ref}`tbl-spdirac-1`, and that the radial wave function $F(r)$ of the relativistic theory becomes $R(r)$ of the nonrelativistic theory. The radial wave function $R(r)$ is discussed in {ref}`sec-cenforce-2`.

It is common in the literature to label the eigenfunctions of $(K,J^2,J_z)$ by $\psi_{\ell jm_j}$ rather than $\psi_{\kappa jm_j}$ as we have done here, where $\ell$ refers to $\ell{\rm(upper)}$ in {ref}`tbl-spdirac-1`. This has the advantage of labeling the solutions of the Dirac equation by the same quantum numbers that apply in the nonrelativistic limit, but of course it does not imply that the Dirac wave functions are eigenfunctions of $L^2$.

(sec-spdirac-14)=

## The Action of $\sigmavec\cdot\pvec$

{eq}`eq-spdirac-76` now gives us the simultaneous eigenfunctions of $(K,J^2,J_z)$. When we demand that these also be eigenfunctions of $H$ we obtain equations that will determine the radial wave functions $F(r)$ and $G(r)$. We substitute the spinors {eq}`eq-spdirac-76` into the Dirac equation, obtaining

:::{math}
:label: eq-spdirac-93
\begin{aligned}
\left[\begin{pmatrix}0 & \sigmavec\cdot\pvec \\  \sigmavec\cdot\pvec & 0\\\end{pmatrix} +m\begin{pmatrix}1 & 0 \\  0 & -1 \\\end{pmatrix} +V(r)-E\right] \begin{pmatrix}F(r){\cal Y}^{j\mp1/2}_{jm_j}\\  iG(r){\cal Y}^{j\pm1/2}_{jm_j}\\\end{pmatrix}=0,
\end{aligned}

:::

where the upper sign refers to the first spinor {eq}`eq-spdirac-76` and the lower sign to the second. The corresponding values of $\kappa$ are shown in {ref}`tbl-spdirac-1`.

This makes it evident that we will need to evaluate expressions of the form $(\sigmavec\cdot\pvec)A(r){\cal Y}^{j\pm1/2}_{jm_j}$, where $A(r)$ is some radial function. It is easier to evaluate $(\sigmavec\cdot\xvec)A(r){\cal Y}^{j\pm1/2}_{jm_j}$ (with $\xvec$ instead of $\pvec$), because it is only a multiplicative operator on the $\xvec$-space wave functions and not a differential operator. Moreover, once we have the latter we can obtain the former by using the identity,

:::{math}
:label: eq-spdirac-94
(\sigmavec\cdot\pvec)(\sigmavec\cdot\xvec) = \pvec\cdot\xvec -i(\sigmavec\cdot\Lvec) = -i\Bigl[ r\pop{}{r} +3 + \sigmavec\cdot\Lvec\Bigr],
:::

where we use {eq}`eq-hilbert-148` and the fact that $x_i (\partial /\partial x_i) = r(\partial/\partial r)$.

Therefore we turn our attention to evaluating

:::{math}
:label: eq-spdirac-95
\begin{aligned}
(\sigmavec\cdot\xvec)A(r){\cal Y}^{j\pm1/2}_{jm_j}(\theta,\phi)= rA(r)\begin{pmatrix}\cos\theta & \sin\theta\,e^{-i\phi}\\  \sin\theta\,e^{i\phi} & -\cos\theta \\\end{pmatrix} {\cal Y}^{j\pm1/2}_{jm_j}(\theta,\phi).
\end{aligned}

:::

We see that under the action of $(\sigmavec\cdot\xvec)$ the radial part of the wave function $A(r)$ just gets multiplied by $r$. As for the angular part, it will be desirable to expand it as a linear combination of spin spherical harmonics. To do this we freeze the radial coordinate $r$ and work with the Hilbert space of spinors over a sphere, in which the spin spherical harmonics ${\cal Y}^\ell_{jm_j}$ form a complete orthonormal basis. We denote these in ket language by $\ket{\ell jm_j}$, where $j=\frac{1}{2},\frac{3}{2},\frac{5}{2},\ldots$, $m_j=-j,\ldots,+j$, and $\ell=j\pm\frac{1}{2}$. The radial coordinate $r$ can be regarded as just a constant for this part of the calculation.

In this notation we wish to evaluate

:::{math}
:label: eq-spdirac-96
(\sigmavec\cdot\xvec) \ket{\ell jm_j} = \sum_{\ell'j'm'_j}\ket{\ell'j'm_j'} \matrixelement{\ell'j'm_j'}{\sigmavec\cdot\xvec} {\ell jm_j}.
:::

This sum simplifies. Since $\sigmavec\cdot\xvec$ is a scalar under rotations generated by $\Jvec$, it commutes with $\Jvec$ and hence with both $J^2$ and $J_z$, so its matrix elements in the basis $\ket{\ell jm_j}$ are diagonal in both $j$ and $m_j$. Moreover it anticommutes with parity $\pi_s$ (it is a pseudoscalar, not a scalar), so it must map a state with quantum number $\ell=j\pm\frac{1}{2}$ into one with quantum number $\ell=j\mp\frac{1}{2}$. This means that $\ell'$ in the sum {eq}`eq-spdirac-96` can only take on the value $\ell'={\tilde\ell}$, where if $\ell=j\pm\frac{1}{2}$ then ${\tilde\ell}=j\mp\frac{1}{2}$. Thus the sum {eq}`eq-spdirac-96` reduces to a single term, which in the two cases $\ell=j\pm\frac{1}{2}$ can be written

:::{math}
:label: eq-spdirac-97
\begin{aligned}
(\sigmavec\cdot\xvec)\ket{j-\frac{1}{2},jm_j} &=\alpha r\ket{j+\frac{1}{2},jm_j}, \\
(\sigmavec\cdot\xvec)\ket{j+\frac{1}{2},jm_j} &=\beta r\ket{j-\frac{1}{2},jm_j}, \\

\end{aligned}
:::

where $\alpha$ and $\beta$ are given by

:::{math}
:label: eq-spdirac-98
\alpha r=\matrixelement{j+\frac{1}{2},jm_j} {(\sigmavec\cdot\xvec)}{j-\frac{1}{2},jm_j}, \qquad \beta r=\matrixelement{j-\frac{1}{2},jm_j} {(\sigmavec\cdot\xvec)}{j+\frac{1}{2},jm_j}.
:::

But since $\sigmavec\cdot\xvec$ is Hermitian, these imply $\beta=\alpha^\cc$. Finally, since $(\sigmavec\cdot\xvec)^2=r^2$, we see that $\alpha$ is a phase factor, $|\alpha|^2=1$.

There is some effort in evaluating the final phase $\alpha$. A straightforward method is simply to apply the matrix in {eq}`eq-spdirac-95` to the spinors {eq}`eq-spdirac-70`, noting that the components of the matrix can be written in terms of the $Y_{\ell m}$'s for $\ell=1$, as in {eq}`eq-wigeck-13`. The product of $Y_{\ell m}$'s can then be expressed in terms of single $Y_{\ell m}$'s by means of the 3-$Y_{\ell m}$ formula, {eq}`eq-jjcouple-59`, and finally the result can be expanded in terms of spinor spherical harmonics. After some algebra along these lines, we find $\alpha=-1$. We summarize the results by writing

:::{math}
:label: eq-spdirac-99
(\sigmavec\cdot\xvec)A(r)\,{\cal Y}^{\ell}_{jm_j} = -rA(r)\,{\cal Y}^{\tilde\ell}_{jm_j},
:::

where again if $\ell=j\pm\frac{1}{2}$, then ${\tilde\ell} =j\mp\frac{1}{2}$.

Now we divide both sides of {eq}`eq-spdirac-99` by $r$ and apply $(\sigmavec\cdot\pvec)$, using {eq}`eq-spdirac-94` and {eq}`eq-spdirac-91`. We find

:::{math}
:label: eq-spdirac-100
-i\Bigl[r\pop{}{r} + 3 + j(j+1)-\ell(\ell+1)-{3\over4} \Bigr] \Bigl[{A(r)\over r}\Bigr]{\cal Y}^\ell_{jm_j} = -(\sigmavec\cdot\pvec)A(r)\,{\cal Y}^{\tilde\ell}_{jm_j}.
:::

Writing this out for the two cases $\ell=j\pm\frac{1}{2}$, we obtain

:::{math}
:label: eq-spdirac-101
\begin{aligned}
(\sigmavec\cdot\pvec)A(r)\,{\cal Y}^{j-1/2}_{jm_j} &= i\Bigl[\dod{A}{r}-{j-1/2\over r}A(r)\Bigr] {\cal Y}^{j+1/2}_{jm_j}, \\
(\sigmavec\cdot\pvec)A(r)\,{\cal Y}^{j+1/2}_{jm_j} &= i\Bigl[\dod{A}{r}+{j+3/2\over r}A(r)\Bigr] {\cal Y}^{j-1/2}_{jm_j}, \\

\end{aligned}
:::

which is the desired action of $\sigmavec\cdot\pvec$ on 2-component eigenfunctions of $(L^2,J^2,J_z)$.

(sec-spdirac-15)=

## The Radial Wave Equations

Now we may substitute {eq}`eq-spdirac-101` into the Dirac equation {eq}`eq-spdirac-93`. While we are at it we will express the radial wave functions $F(r)$, $G(r)$ in terms of alternative radial wave functions $f(r)$ and $g(r)$, defined by

:::{math}
:label: eq-spdirac-102
F(r)={f(r)\over r}, \qquad G(r)={g(r)\over r},
:::

which are just like the transformation {eq}`eq-cenforce-10` used in the nonrelativistic theory to create what we called version two of the radial wave equation.

The result is two coupled, 2-component equations equations for the upper and lower components of the Dirac spinor, from which the common spinor spherical harmonic can be canceled, leaving two coupled radial wave equations for $f(r)$ and $g(r)$. These are

:::{math}
:label: eq-spdirac-103
\begin{aligned}
\dod{f}{r}\mp {j+1/2\over r}f(r)&=[m+E-V(r)]g(r), \\
\dod{g}{r}\pm {j+1/2\over r}g(r)&=[m-E+V(r)]f(r), \\

\end{aligned}
:::

where as in {eq}`eq-spdirac-93` the upper sign corresponds to the first spinor {eq}`eq-spdirac-76` and the lower sign to the second. These equations can also be written in terms of the quantum number $\kappa$,

:::{math}
:label: eq-spdirac-104a
\begin{aligned}
\dod{f}{r}+{\kappa\over r}f(r)&=[m+E-V(r)]g(r),
\end{aligned}
:::

:::{math}
:label: eq-spdirac-104b
\begin{aligned}
\dod{g}{r}-{\kappa\over r}g(r)&=[m-E+V(r)]f(r),
\end{aligned}
:::

where $\kappa=\mp(j+1/2)$, as indicated in {ref}`tbl-spdirac-1`. These are the radial wave equations in the Dirac theory that replace version two of the radial wave equation, {eq}`eq-cenforce-11`, in the Schr\"odinger theory.

The nonrelativistic limit of these equations is obtained by the method of {ref}`sec-dirac-9`. That is, we approximate $E\approx m\gg V$ so that the right hand side of {eq}`eq-spdirac-104a` becomes $2mg(r)$, which allows that equation to be solved for $g$ in terms of $f$. This is then substituted into {eq}`eq-spdirac-104b` to eliminate $g$ and obtain an equation purely for $f$. This turns out to be version two of the radial Schr\"odinger equation, {eq}`eq-cenforce-11`.

(sec-spdirac-16)=

## The Hydrogen Atom

We now specialize to the case $V(r)=-Ze^2/r$ for a hydrogen-like atom. We will solve the Dirac equation {eq}`eq-spdirac-65` for the bound states in this potential. Note that in natural units $e^2=\alpha\approx 1/137$, so that $Ze^2=Z\alpha$ is a dimensionless parameter of the problem. This parameter ranges from about $1/137$ for hydrogen to about $2/3$ for uranium and beyond, remaining, however, always less than unity for all known nuclei. As we will see, the ground state of the Dirac equation is a bound state only for $Z\alpha<1$, that is, $Z<\approx 137$, and becomes unbound for higher $Z$. This lends some interest to the question of whether nuclei with $Z>137$ exist or could be made, even briefly. Note, however, that the potential $Z\alpha/r$ is an idealization and that in the real world it must be modified at small radii because nuclei are not point charges. The corrections required for this become more important as $Z$ increases. See {ref}`sec-hydrogen-8` and Prob. {ref}`prob-pertth-1`.

Since the probability density in the Dirac theory is $\psi^\dagger\psi$, the normalization integral for normalized bound states is

:::{math}
:label: eq-spdirac-105
\int d^3\xvec\,\psi^\dagger(\xvec)\psi(\xvec)=1.
:::

If we specialize this to Dirac wave functions of the form {eq}`eq-spdirac-76` and carry out the integral in spherical coordinates, we have

:::{math}
:label: eq-spdirac-106
\int d^3\xvec\,\psi^\dagger\psi = \int_0^\infty r^2\,dr (|F(r)|^2 + |G(r)|^2) = \int_0^\infty dr\, \bigl(|f(r)|^2+|g(r)|^2)=1,
:::

where we use {eq}`eq-spdirac-71`. We see that a Dirac central force eigenfunction is normalizable if and only if both $f(r)$ and $g(r)$ are normalizable as one-dimensional wave functions on the interval $[0,\infty)$.

We first look at the Dirac equation when $r$ is large, so that the potential energy and the terms that involve $\kappa/r$ can be neglected. Then {eq}`eq-spdirac-104a` become

:::{math}
:label: eq-spdirac-107
\dod{f}{r}=(m+E)g, \qquad \dod{g}{r}=(m-E)f,
:::

or,

:::{math}
:label: eq-spdirac-108
{d^2f\over dr^2} = (m^2-E^2)f, \qquad {d^2g\over dr^2} = (m^2-E^2)g.
:::

If $|E|>m$ these have oscillatory solutions that are not normalizable and cannot represent bound states. Likewise if $|E|=m$ the solutions are of the form $c_1+c_2r$, which are not normalizable. We see that the Dirac hydrogen-like atom has a continuous spectrum for $E\ge m$, which corresponds to the positive energy, continuous spectrum of the nonrelativistic hydrogen atom. But the Dirac equation also possesses a continuous spectrum for $E\le -m$, that is, it possesses negative energy solutions, just like the free particle.

Finally, if $|E|<m$ then the solutions go as

:::{math}
:label: eq-spdirac-109
f(r), g(r) \sim \exp(\pm\sqrt{m^2-E^2}\,r), \qquad r\to\infty,
:::

which are normalizable if we choose the minus sign. We see that bound states are possible only in the range $|E|<m$, that is, $-m<E<m$, and that the eigenfunctions must behave asymptotically as $\exp(-\sqrt{m^2-E^2}\,r)$.

We define a new radial variable,

:::{math}
:label: eq-spdirac-110
\rho=2\sqrt{m^2-E^2}\,r,
:::

so that the asymptotic behavior of the bound state wave functions will be $e^{-\rho/2}$. Then {eq}`eq-spdirac-104a` become

:::{math}
:label: eq-spdirac-111
\begin{aligned}
\dod{f}{\rho}+{\kappa\over\rho}f &= \Bigl({1\over 2\gamma}+ {Z\alpha\over\rho}\Bigr)f, \\
\dod{g}{\rho} -{\kappa\over\rho}g &= \Bigl( {\gamma\over2} -{Z\alpha\over\rho}\Bigr), \\

\end{aligned}
:::

where

:::{math}
:label: eq-spdirac-112
\gamma=\sqrt{\ds{m-E\over m+E}}.
:::

Next we define new radial wave functions $a(\rho)$ and $b(\rho)$, in which the asymptotic behavior has been stripped off,

:::{math}
:label: eq-spdirac-113
f(r)=e^{-\rho/2}\,a(r), \qquad g(r)=e^{-\rho/2}\,b(r),
:::

which cause {eq}`eq-spdirac-111` to become

:::{math}
:label: eq-spdirac-114a
\begin{aligned}
\dod{a}{\rho} -{a\over2} +{\kappa\over\rho}a &=\Bigl({1\over 2\gamma}+{Z\alpha\over\rho}\Bigr)b,
\end{aligned}
:::

:::{math}
:label: eq-spdirac-114b
\begin{aligned}
\dod{b}{\rho}- {b\over2} -{\kappa\over\rho} b &= \Bigl({\gamma\over2}-{Z\alpha\over\rho}\Bigr) a.
\end{aligned}
:::

We examine the behavior of the solutions near $\rho=0$. We assume that the dominant behavior of $a(\rho)$ and $b(\rho)$ when $\rho$ is small is $a_0 \rho^s$ and $b_0\rho^t$, respectively, for some powers $s$ and $t$, where $a_0\ne0$ and $b_0\ne0$. Then the left hand side of {eq}`eq-spdirac-114a` is dominated by $(s+\kappa)a_0\rho^{s-1}$ and the right hand side by $b_0Z\alpha\rho^{t-1}$. Therefore if $t<s$ the right hand side dominates, and we must have $b_0Z\alpha=0$ or $b_0=0$. But this contradicts our assumption about the leading behavior, so we cannot have $t<s$ and we must have $s\ge t$. A similar argument applied to {eq}`eq-spdirac-114b` shows that we must have $t\ge s$. Taken together, these imply $t=s$. We see that both $a(\rho)$ and $b(\rho)$ begin with the same power $s$.

It then follows that to leading order both sides of both {eq}`eq-spdirac-114a` go as $\rho^{s-1}$, and that the coefficients must satisfy

:::{math}
:label: eq-spdirac-115
\begin{aligned}
(s+\kappa)a_0 &= Z\alpha\,b_0, \\
(s-\kappa)b_0 &= -Z\alpha\,a_0 \\

\end{aligned}
:::

or

:::{math}
:label: eq-spdirac-116
\begin{aligned}
\begin{pmatrix}s+\kappa & -Z\alpha \\  Z\alpha & s-\kappa\\\end{pmatrix} \begin{pmatrix}a_0\\  b_0\\\end{pmatrix} =0.
\end{aligned}

:::

Thus, the determinant $s^2-\kappa^2+(Z\alpha)^2$ of the matrix must vanish, or,

:::{math}
:label: eq-spdirac-117
s=\pm \sqrt{\kappa^2-(Z\alpha)^2} = \pm\sqrt{(j+1/2)^2-(Z\alpha)^2}.
:::

Because the smallest value of $j+1/2$ is $1$, we see that the exponent $s$ will be real for all $j$ as long as $Z\alpha<1$.

The case $Z\alpha>1$ does not occur in real atoms, and even if it did, the potential would not be pure Coulomb because nuclei are not point charges. Nevertheless there is some interest in solving the problem anyway. We see that $Z\alpha>1$ leads to purely imaginary exponents $s$ for small values of $j$, which, as it turns out, produce wave functions that are oscillatory and not normalizable. Thus, the usual ground state of hydrogen would disappear as a bound state for such high values of $Z$, and be replaced by unbound states. This strange behavior for high $Z$ is related to what is called the “supercritical vacuum,” and is properly understood by methods of quantum field theory. In a sense what happens is that for high $Z$ the electric field becomes strong enough to pull electron-positron pairs out of the vacuum, and thus a multiparticle situation is created.

Similar effects occur in a square well potential, if it is deep enough. You would think that the deeper the well gets, the more tightly bound the electron would be, but in the Dirac equation that is not so, since for deep enough wells we start to get unbound solutions. This effect is related to what is called the “Klein paradox,” another one of the puzzling aspects of the Dirac equation, when treated as the wave equation for a single, relativistic particle. In these notes we assume $Z\alpha<1$, which means that $s$ is real for all $j$.

Now it turns out that we can reject the minus sign in {eq}`eq-spdirac-117` on grounds of the regularity of the wave function. If we require that the amount of probability in a region near $\rho=0$ be finite, then the integral

:::{math}
:label: eq-spdirac-118
\int_0^\epsilon \rho^{2s}\,d\rho
:::

must be finite for some $\epsilon>0$. But this implies $2s>-1$, or $s>-1/2$. If we demand in addition that the expectation value of the potential energy term $Z\alpha/\rho$ be finite, then we obtain $2s-1>-1$, or $s>0$. These regularity conditions are discussed in greater detail by W. Greiner, *Relativistic Quantum Mechanics*. We henceforth take only the positive root for $s$ in {eq}`eq-spdirac-117`.

If $Z\alpha$ is small then $s$ is approximately $j+1/2$, an integer, but with a small negative correction. With the correction $s$ is not an integer, so the wave function behaves as a fractional power of $r$ near the origin. In the case $j=1/2$, $s$ is a fraction less than 1, which means that the wave functions $F$ and $G$ (see {eq}`eq-spdirac-102` go like a small negative power of $r$ near the origin. That is, they diverge at $r=0$, unlike the nonrelativistic solution, which is regular there. In spite of the divergence, the net probability in a neighborhood of the origin is finite, as is the expectation value of the potential, as noted above.

(sec-spdirac-17)=

## Recursion Relations and Energy Levels

We now write $a(\rho)$ and $b(\rho)$ as power series,

:::{math}
:label: eq-spdirac-119
a(\rho)=\rho^s\sum_{k=0}^\infty a_k\rho^k, \qquad b(\rho)=\rho^s\sum_{k=0}^\infty b_k\rho^k,
:::

and substitute these into {eq}`eq-spdirac-114a`. By equating coefficients of the different powers of $\rho$ we obtain recursion relations for the coefficients $a_n$ and $b_n$. These are conveniently written in matrix--vector form,

:::{math}
:label: eq-spdirac-120
A_k x_k = B x_{k-1},
:::

where

:::{math}
:label: eq-spdirac-121
\begin{aligned}
A_k=\begin{pmatrix}k+s+\kappa & -Z\alpha \\  Z\alpha & k+s-\kappa\\\end{pmatrix}, \qquad B={1\over2}\begin{pmatrix}1 & 1/\gamma \\  \gamma & 1\\\end{pmatrix},
\end{aligned}

:::

and

:::{math}
:label: eq-spdirac-122
x_k = \begin{pmatrix}a_k\\ b_k\\\end{pmatrix}.
:::

It is understood that $x_k=0$ for $k<0$. In the following we will use letters $w$, $x$, etc., at the end of the alphabet for 2-component vectors, and those near the beginning, $a$, $b$, etc., for scalars, for example, $a_k$ and $b_k$ are the components of $x_k$.

Setting $k=0$ in {eq}`eq-spdirac-120` we obtain $A_0x_0=0$, which is {eq}`eq-spdirac-116`. Since $x_0\ne0$ this implies $\det A_0=0$, which as shown above determines $s$. As for $x_0$, it is any nonzero vector in the one-dimensional kernel of $A_0$. For $k>0$ the matrices $A_k$ are nonsingular, since

:::{math}
:label: eq-spdirac-123
\det A_k = k(2s+k),
:::

so we can write the recursion relation as

:::{math}
:label: eq-spdirac-124
x_k = A_k^{-1}Bx_{k-1}, \qquad k>0.
:::

The matrix $B$ is also singular. We pay special attention to its image, a one-dimensional space spanned by

:::{math}
:label: eq-spdirac-125
w=\begin{pmatrix}1\\  \gamma\\\end{pmatrix}.
:::

Vector $w$ is an eigenvector of $B$ with eigenvalue 1,

:::{math}
:label: eq-spdirac-126
Bw=w.
:::

The kernel of $A_0$ is conveniently handled with the adjoint (or adjugate) of $A_0$. If $M$ is any $2\times2$ matrix, then the adjoint $\tilde M$ is defined by

:::{math}
:label: eq-spdirac-127
\begin{aligned}
M=\begin{pmatrix}a & b \\  c & d\\\end{pmatrix}, \qquad {\tilde M}=\begin{pmatrix}d & -b \\ -c & a\\\end{pmatrix},
\end{aligned}

:::

so that $M{\tilde M} = (\det M)I$. Thus $A_0 {\tilde A}_0=0$ and ${\tilde A}_0$ maps any vector into a vector in the kernel of $A_0$. It is convenient to choose

:::{math}
:label: eq-spdirac-128
\begin{aligned}
x_0 = {\tilde A}_0 w = \begin{pmatrix}s-\kappa & Z\alpha \\  -Z\alpha & s+\kappa\\\end{pmatrix} \begin{pmatrix}1\\  \gamma\\\end{pmatrix} = \begin{pmatrix}s-\kappa+\gamma Z\alpha \\  -Z\alpha + \gamma(s+\kappa)\\\end{pmatrix}.
\end{aligned}

:::

In the following we will need $Bx_0$, which must be a multiple of $w$. Using {eq}`eq-spdirac-121` and {eq}`eq-spdirac-128`, we find

:::{math}
:label: eq-spdirac-129
Bx_0= -\nu w,
:::

where

:::{math}
:label: eq-spdirac-130
\nu={Z\alpha\over2}\Bigl({1\over\gamma}-\gamma\Bigr) -s.
:::

Also, for $k>0$ we write

:::{math}
:label: eq-spdirac-131
\begin{aligned}
A_k^{-1} = {{\tilde A}_k \over \det A_k} ={1\over k(2s+k)} \begin{pmatrix}k+s-\kappa & Z\alpha \\  -Z\alpha & k+s+\kappa\\\end{pmatrix} ={1\over k(2s+k)}({\tilde A}_0 + kI).
\end{aligned}

:::

Now to apply the recursion relation {eq}`eq-spdirac-124` for $k=1$ we must evaluate

:::{math}
:label: eq-spdirac-132
({\tilde A}_0+I)Bx_0 = -\nu ({\tilde A}_0+I) w = -\nu(x_0+w),
:::

so that

:::{math}
:label: eq-spdirac-133
x_1 = A_1^{-1}Bx_0 = {-\nu \over 1\cdot(2s+1)} (x_0+w).
:::

Iterating the recursion relation in a similar manner, we obtain

:::{math}
:label: eq-spdirac-134
x_k = {(-1)^k \nu(\nu-1)\ldots(\nu-k+1) \over k!(2s+1)(2s+2)\ldots (2s+k)} (x_0+kw).
:::

If $\nu$ is not an integer $\ge 0$ then as $k$ gets large the coefficient in front of $x_0$ approaches $1/k!$, so that the series for both $a(\rho)$ and $b(\rho)$ behave like $e^\rho$. This overwhelms the factor of $e^{-\rho/2}$ that we have stripped off, making both $f(\rho)$ and $g(\rho)$ diverges as $e^{\rho/2}$ as $\rho\to\infty$. These solutions are not normalizable and must be rejected. We conclude that $\nu$ must be a nonnegative integer, $\nu=N$, with $N\ge0$. Then $x_k=0$ for $k>N$, and both $a(\rho)$ and $b(\rho)$ are polynomials in $\rho$ of degree $N$. These are dominated at large $\rho$ by $e^{-\rho/2}$, so that the wave functions are normalizable and acceptable as bound states.

Now since

:::{math}
:label: eq-spdirac-135
{1\over\gamma}-\gamma =\sqrt{\ds{m+E\over m-E}} - \sqrt{\ds{m-E\over m+E}} = {2E\over \sqrt{m^2-E^2}},
:::

{eq}`eq-spdirac-131` becomes

:::{math}
:label: eq-spdirac-136
N+s =  {Z\alpha E \over \sqrt{m^2-E^2}},
:::

which we solve for $E$ to obtain,

:::{math}
:label: eq-spdirac-137
E={mc^2 \over \sqrt{\ds{1+{(Z\alpha)^2\over (N+s)^2}}}},
:::

where we have restored ordinary units. These are the energy eigenvalues of the bound states of the Dirac hydrogen atom; they are functions of the two quantum numbers, $j$ and $N$. The bound state energies are all positive and lie in the interval $0<E<mc^2$.

:::{figure} images/spdirac-fig04.png
:label: fig-spdirac-4
:width: 80%

The energy spectrum of the Dirac hydrogen atom, here illustrated for $Z=1$. The usual hydrogen ground state $n=1$ lies 13.6 eV below the rest mass-energy, $mc^2$, and the usual unbound states of the Schr\"odinger theory lie in a continuum above $E=mc^2$. However, there also exists another continuum of unbound (negative energy) states with $E\le -mc^2$.
:::

To connect these quantum numbers with those of the nonrelativistic hydrogen atom, we expand in powers of $Z\alpha$. For this we only need $s$ to lowest order,

:::{math}
:label: eq-spdirac-138
s=\sqrt{\kappa^2-(Z\alpha)^2} \approx |\kappa| = j+1/2,
:::

so that

:::{math}
:label: eq-spdirac-139
E=mc^2\biggl[ 1- {(Z\alpha)^2 \over 2(N+j+\frac{1}{2})^2}\biggr] = mc^2 - {Ze^2\over 2an^2},
:::

where $a=\hbar^2/mZe^2$ (see {ref}`tbl-hydrogen-2`) is the effective Bohr radius and where we set

:::{math}
:label: eq-spdirac-140
n=N+j+\frac{1}{2}
:::

which is identified with the usual principal quantum number of the nonrelativistic problem. To second order in $Z\alpha$, the Dirac energy levels are the rest-mass-energy $mc^2$ of the electron, shifted downward by the binding energies of the Schr\"odinger theory in the electrostatic model.

Expressed in terms of $n$ instead of $N$, {eq}`eq-spdirac-137` becomes the Dirac hydrogen energy levels as cited in {eq}`eq-finestruc-51`. As discussed in {ref}`ch-finestruc`, the energy levels {eq}`eq-spdirac-137`, when expanded to fourth order in $Z\alpha$, yield all the fine structure corrections obtained by perturbation theory in those notes. This means that the Dirac equation automatically incorporates the spin-orbit corrections, including the factor of $1/2$ due to Thomas precession, as well as the not-so-obvious Darwin term. All this complexity in the Schr\"odinger-Pauli theory is contained in the simple equation {eq}`eq-covariance-13`. The entire spectrum of the Dirac hydrogen atom is illustrated in {ref}`fig-spdirac-4`, including the two continua of unbound states with $E\ge mc^2$ and $E\le -mc^2$.

(sec-spdirac-18)=

## Energy Eigenfunctions

It is now straightforward to work out the energy eigenfunctions. We combine {eq}`eq-spdirac-113`, {eq}`eq-spdirac-119`, {eq}`eq-spdirac-122` and {eq}`eq-spdirac-134` with $\nu=N$ to obtain

:::{math}
:label: eq-spdirac-141
\begin{aligned}
\begin{pmatrix}f(\rho)\\  g(r)\\ &= e^{-\rho/2}\begin{pmatrix}a(\rho)\\  b(\rho)\\ = \rho^s e^{-\rho/2} \sum_{k=0}^N \rho^k x_k\\  &={\Gamma(2s+1)\,N!\over\Gamma(N+2s+1)} \rho^s e^{-\rho/2}\biggl(x_0 + w \rho\dod{}{\rho}\biggr) L^{2s}_N(\rho),\\ 
\end{pmatrix}
\end{pmatrix}
\end{aligned}
:::

where we use Abramowitz and Stegun, *Handbook of Mathematical Functions*, Eq.~(22.3.9), for the definition of the associated Laguerre polynomials. In the present context that definition can be written,

:::{math}
:label: eq-spdirac-142
L^{2s}_N(\rho) = \sum_{k=0}^N {(-1)^k \,\Gamma(N+2s+1) \over (N-k)! \,\Gamma(k+2s+1)} {\rho^k\over k!}.
:::

Also, the 2-vectors $x_0$ and $w$ are given by {eq}`eq-spdirac-125` and {eq}`eq-spdirac-128`. In these formulas it is necessary to use gamma functions instead of factorials, because the upper index of the Laguerre polynomials ($2s$) is not an integer.

To explore the nonrelativistic limit it is convenient to use the identities,

:::{math}
:label: eq-spdirac-143
\rho\dod{}{\rho}L^{2s}_N(\rho) = (N+2s)L^{2s-1}_N(\rho) -2s L^{2s}_N(\rho) = -\rho L^{2s+1}_{N-1}(\rho),
:::

of which the first is easily derived from the definition {eq}`eq-spdirac-142` and the second is Abramowitz and Stegun, Eq.~(22.8.6) (and which is also easily derived from the definition). Then we have two expressions for the radial wave functions,

:::{math}
:label: eq-spdirac-144
\begin{aligned}
\begin{pmatrix}f(\rho)\\  g(\rho)\\&= \rho^s e^{-\rho/2} \bigl[(x_0-2sw)L^{2s}_N(\rho) +w(N+2s)L^{2s-1}_N(\rho)\bigr] \\  &=\rho^s e^{-\rho/2}\bigl[x_0 L^{2s}_N(\rho) -\rho wL^{2s+1}_{N-1}(\rho)\bigr], \\\end{pmatrix}
\end{aligned}

:::

where we drop the constant prefactors seen on the right in {eq}`eq-spdirac-141` since at this point we are not interested in the normalization. The two forms of the solution {eq}`eq-spdirac-144` are useful for taking the nonrelativistic limit, in which we expand everything to lowest order in $Z\alpha$. The form {eq}`eq-spdirac-144` is useful when $\ell=j-\frac{1}{2}$, in which case the second term dominates and produces $\rho^{\ell+1} e^{-\rho/2}L^{2\ell+1}_{n-\ell-1}(\rho)$ to leading order in $Z\alpha$, which is the nonrelativistic wave function (see {eq}`eq-hydrogen-16`; and the form {eq}`eq-spdirac-144` is useful when $\ell=j+\frac{1}{2}$ in which case the second term again dominates and produces the same nonrelativistic wave function.

The normalization of the Dirac wave functions may also be obtained in closed form; it may be found in the references.

\problems

(prob-spdirac-1)=

**Problem \prbdspdirac-1..** 

:::{math}
:label: eq-spdirac-145
\Sigma_{\pm} = {1\pm \sslash\gamma_5 \over 2},
:::

which project out the positive and negative spin components of an arbitrary 4-spinor of a free particle. As far as the negative energy spinors $v(p,s)$ are concerned, notice that these project out the components whose labels are $+s$ and $-s$, while the labels are the negatives of the spin eigenvalues.

(prob-spdirac-2)=

**Problem \prbdspdirac-2..** 

\problempart{(a)} Prove {eq}`eq-spdirac-41b`, {eq}`eq-spdirac-41c` and {eq}`eq-spdirac-42`.

\problempart{(b)} Prove {eq}`eq-spdirac-46a`. It may help to note that the $D$ matrix for a pure boost is Hermitian, and that $D(\pvec)^{-1} = D(-\pvec)$.

(prob-spdirac-3)=

**Problem \prbdspdirac-3..** 

:::{math}
:label: eq-spdirac-146
\begin{aligned}
\Pi_+ &= \sum_{\pm s} u(p,s)\ubar(p,s), \\
\Pi_- &= -\sum_{\pm s} v(p,s)\vbar(p,s), \\

\end{aligned}
:::

that is, the positive and negative energy projectors are the first and second terms in {eq}`eq-spdirac-42`, respectively. As in that equation, the summation is taken over two spin vectors that point in opposite directions in the rest frame.

(prob-spdirac-4)=

**Problem \prbdspdirac-4..** 

Apply this approximation to the Dirac current $J^\mu=c\psibar\gamma^\mu\psi$ to get the probability density and probability current in the Pauli theory, to order $(v/c)^2$. See if the answer includes a magnetization current. See {ref}`sec-jjcouple-6`.

(prob-spdirac-5)=

**Problem \prbdspdirac-5..** 

:::{math}
:label: eq-spdirac-147
\psi(\xvec,t) = \int d^3\pvec \sum_{\pm s} \Bigl[A(p,s) u(p,s) e^{-i(p\cdot x)/\hbar} + B(p,s) v(p,s) e^{+i(p\cdot x)/\hbar}\Bigr],
:::

where $A(p,s)$ and $B(p,s)$ are expansion coefficients. We write these as if they depend on two 4-vectors $p$ and $s$, but the notation is like the dependence of $u(p,s)$ and $v(p,s)$, that is, the 4-vector $p$ is really a function of the 3-momentum $\pvec$ (the variable of integration) and $s$ is taken over only two opposite unit vectors in the rest frame. This wave function is in the Schr\"odinger picture, since the explicit time-dependence is given.

Compute the expectation value of the velocity operator $\vvec=c\alphavec$ to get $\xpecval{\vvec}(t)$, and show that it is independent of $t$ and contains no Zitterbewegung if the wave packet consists purely of positive energy solutions (that is, if $B(p,s)=0$).

(prob-spdirac-6)=

**Problem \prbdspdirac-6..** 

:::{math}
:label: eq-spdirac-148
\Avec = B_0 x{\hat{\mathbf{y}}},
:::

which is translationally invariant in the $y$-direction. This means that $p_y$ will be a constant of the motion (although you must distinguish between the kinetic and canonical momentum).

Here is some background on the nonrelativistic problem, which will save you some time. Ignore the spin and the motion in the $z$-direction, for simplicity. Then the Schr\"odinger equation is

:::{math}
:label: eq-spdirac-149
{1\over 2m} \Bigl[ {\hat p}_x^2 + \Bigl( {\hat p}_y + m\omega x \Bigr)^2 \Bigr]\psi(x,y) = E\psi(x,y).
:::

Here we put hats on the momentum operators to distinguish them from the corresponding eigenvalues (where relevant), which are $c$-numbers. For example, $\hat p_y = -i\hbar \partial/\partial y$. Also, we define

:::{math}
:label: eq-spdirac-150
\omega= {eB_0\over mc}.
:::

Then the wave equation {eq}`eq-spdirac-149` is separable, and has the solution,

:::{math}
:label: eq-spdirac-151
\psi(x,y) = e^{ip_yy/\hbar}\, u_n(\xi),
:::

where $p_y$ is the eigenvalue of $\hat p_y$, where

:::{math}
:label: eq-spdirac-152
\xi = x+{p_y\over m\omega},
:::

and where $u_n$ is the usual, normalized Hermite function for the one-dimensional harmonic oscillator with frequency $\omega$,

:::{math}
:label: eq-spdirac-153
u_n(\xi) = \Bigl( {m\omega \over \pi\hbar} \Bigr)^{1/4} {1\over\sqrt{n! 2^n}} H_n\Bigl( \sqrt{m\omega\over\hbar} \, \xi\Bigr) \exp\Bigl( -{m\omega x^2\over 2\hbar}\Bigr).
:::

Here $H_n$ is the usual Hermite polynomial, defined by {eq}`eq-harmosc-44`. The energy eigenvalue for the eigenfunction {eq}`eq-spdirac-151` is

:::{math}
:label: eq-spdirac-154
E=(n+\frac{1}{2})\hbar\omega,
:::

where $n=0,1,2,\ldots$ is the Landau level. The energy is independent of the quantum number $p_y$. The wave function is like a ridge in the $x$-$y$ plane, centered on $x=-p_y/m\omega$ (i.e., on $\xi=0$), and running in the $y$-direction.

\problempart{(a)} Solve the Dirac equation for the relativistic electron in the same magnetic field. This time you must include the $z$-motion and the spin. Express the energy in terms of the quantum numbers $(n,p_y,p_z,m_s)$. Write out explicitly a complete set of positive energy solutions as 4-component spinors. You need not normalize these solutions, and you may ignore the negative energy solutions.

\problempart{(b)} Consider the motion of a Dirac electron in the field,

:::{math}
:label: eq-spdirac-155
\Bvec = B_1{\hat{\mathbf{z}}}, \qquad \Evec=E_1{\hat{\mathbf{x}}},
:::

where $0 < E_1 < B_1$. The solution of the Dirac equation for this problem can be obtained from the solution to part (a) by using the transformation law {eq}`eq-covariance-26`. Find matrices $\Lambdamat$ and $D(\Lambdamat)$ which will cause $\psi'(x)$ to be the solution in the field {eq}`eq-spdirac-155` if $\psi(x)$ is the solution in the purely magnetic field of part (a). You will also need to find a relation between $(E_1,B_1)$ and $B_0$. You need not write out the solution $\psi'(x)$ explicitly, but do find the energy eigenvalues in terms of the same quantum numbers $(n,p_y,p_z,m_s)$ as in part (a).
