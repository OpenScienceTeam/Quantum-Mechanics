---
title: "15. Orbital Angular Momentum and Spherical Harmonics"
---
(ch-orbamsph)=

# 15. Orbital Angular Momentum and Spherical Harmonics

(sec-orbamsph-1)=

## Introduction

In {ref}`ch-repsamos`, we worked out the general theory of the representations of the angular momentum operators $\Jvec$ and the corresponding rotation operators. That theory made no assumptions about the kind of system upon which the angular momentum and rotation operators act, for example, whether it is a spin system or has spatial degrees of freedom, whether single particle or multiparticle, whether nonrelativistic or relativistic, etc., because most of the theory of rotations is independent of those details. We did work through the specific case of spin-$\frac{1}{2}$ systems in detail in {ref}`ch-spinrot`. In this set of notes we consider another important example of the theory of rotations, namely, a system consisting of a single particle moving in three-dimensional space. We assume either that the particle is spinless, or that the spin degrees of freedom can be ignored.

For most of these notes we make no assumptions about the Hamiltonian governing the single particle, but the theory of rotations is most useful in the case that the particle is moving in a central force field, that is, one for which the potential $V=V(r)$ is a function of the radius $r$ only. We will discuss central force problems in {ref}`ch-cenforce`.

In these notes we follow the usual custom in the physics literature of denoting the orbital angular momentum by $\Lvec$ instead of the general notation $\Jvec$ used earlier. Similarly, we use the quantum number $\ell$ instead of $j$.

(sec-orbamsph-2)=

## Rotation Operators for Spatial Degrees of Freedom

The wave function for a spinless particle in three dimensions can be written

:::{math}
:label: eq-orbamsph-1
\psi(\xvec) = \braket{\xvec}{\psi},
:::

where $\ket{\psi}$ is the state vector and $\ket{\xvec}$ are the position eigenkets. The general relation of such wave functions to the measurement postulates was laid out in {ref}`ch-spatialdof`; in particular, we are assuming that the three components of the position vector $\xvec$ by themselves form a complete set of commuting observables, so that the position eigenkets $\ket{\xvec}$ form a continuous basis for the Hilbert space of physical states.

Introductory courses on quantum mechanics usually define the orbital angular momentum of a single particle as $\Lvec=\xvec \cross \pvec$. This formula is borrowed from classical mechanics, where $\xvec\cross\pvec$ is (usually, not always) the angular momentum of a single particle moving in three-dimensional space. In this course, however, angular momentum is defined as the generator of rotations, as explained in {ref}`ch-spinrot`\ and \repsamos. Therefore we begin with a definition of rotation operators on our single particle system, and then derive their generators.

Let us recall that we defined translation operators by

:::{math}
:label: eq-orbamsph-2
T(\avec)\ket{\xvec} = \ket{\xvec+\avec},
:::

where $\avec$ is a displacement vector. This is {eq}`eq-spatialdof-21`. This definition makes sense, because if the particle is known to lie in a small region around position $\xvec$, then the translated quantum state must mean the particle is known to lie in a small region around $\xvec+\avec$. This is just what we mean by the active point of view in applying translations.

Similarly, let $\Rmat \in SO(3)$ be a proper rotation, and define an operator $U(\Rmat)$ by

:::{math}
:label: eq-orbamsph-3
U(\Rmat) \ket{\xvec} = \ket{\Rmat\xvec}.
:::

This definition is physically reasonable, because the position eigenket $\ket{\xvec}$ is the state of the system after a measurement of the position operator has yielded the value $\xvec$, while $\ket{\Rmat\xvec}$ is the state after such a measurement has given the value $\Rmat\xvec$. For example, position can be measured by passing particle through a small hole in a screen, and if we rotate the screen so that the hole moves from $\xvec$ to $\Rmat\xvec$, then it is logical to call the state produced by the rotated measuring apparatus the rotated state.

This argument does not specify the phase of the rotated state, however, and if we were to worry about this we would insert a phase factor on the right hand side of {eq}`eq-orbamsph-3` that would depend on both $\xvec$ and $\Rmat$. Similar concerns could also be raised when defining the translation operators. We will ignore this possible complication as it turns out to be unnecessary in kinetic-plus-potential problems, and we will just work with the definition {eq}`eq-orbamsph-3`. Problems with magnetic fields, however, force us to think about those phase factors more carefully. This could be foreseen by the fact that a gauge transformation, insofar as its effect on wave functions is concerned, is equivalent to a change in the phase conventions for the position eigenkets.

The definition {eq}`eq-orbamsph-3` of the rotation operators is provisional until we have demonstrated several things. First, we note that {eq}`eq-orbamsph-3` actually does specify the operator $U(\Rmat)$, because it gives the action of that operator on a set of basis vectors. By linearity, the action of $U(\Rmat)$ on an arbitrary vector is thereby specified. Next, we note that the definition implies that $U(\Rmat)$ forms a representation of the rotation group $SO(3)$, that is,

:::{math}
:label: eq-orbamsph-4
U(\Rmat_1)U(\Rmat_2)=U(\Rmat_1\Rmat_2).
:::

This follows directly from the definition, since

:::{math}
:label: eq-orbamsph-5
U(\Rmat_1)U(\Rmat_2)\ket{\xvec} = U(\Rmat_1)\ket{\Rmat_2\xvec} =\ket{\Rmat_1\Rmat_2\xvec} = U(\Rmat_1\Rmat_2)\ket{\xvec}.
:::

{eq}`eq-orbamsph-4` also implies

:::{math}
:label: eq-orbamsph-6
U(\Imat) = 1
:::

and

:::{math}
:label: eq-orbamsph-7
U(\Rmat^{-1}) = U(\Rmat)^{-1}.
:::

Next we work out the effect of $U(\Rmat)$ on a wave function. We start with

:::{math}
:label: eq-orbamsph-8
\ket{\psi} = \int d^3\xvec \, \ket{\xvec} \braket{\xvec}{\psi} = \int d^3\xvec \,\ket{\xvec} \psi(\xvec),
:::

expanding an arbitrary state $\ket{\psi}$ in terms of the position eigenbasis. Next we apply $U(\Rmat)$ to both sides, writing

:::{math}
:label: eq-orbamsph-9
\ket{\psi'} = U(\Rmat) \ket{\psi}
:::

for the rotated state. This gives

:::{math}
:label: eq-orbamsph-10
\ket{\psi'} = \int d^3\xvec \, \ket{\Rmat \xvec} \psi(\xvec).
:::

We now change variables in the integral, writing $\xvec' = \Rmat \xvec$, so that

:::{math}
:label: eq-orbamsph-11
d^3\xvec' = (\det\Rmat)d^3\xvec = d^3\xvec,
:::

since $\det\Rmat=1$. Thus we find

:::{math}
:label: eq-orbamsph-12
\ket{\psi'} = \int d^3\xvec \, \ket{\xvec} \psi(\Rmat^{-1}\xvec),
:::

where we have dropped the prime on the dummy variable of integration.

We see that the wave function of the rotated state $\ket{\psi'}$ is given by

:::{math}
:label: eq-orbamsph-13
\psi'(\xvec) = \bigl(U(\Rmat)\psi\bigr)(\xvec) = \psi(\Rmat^{-1} \xvec),
:::

where we use the notation $U(\Rmat)\psi$ to mean the wave function $\psi'$ of the rotated state $\ket{\psi'}$. This may be compared to the corresponding formula in the case of translations,

:::{math}
:label: eq-orbamsph-14
\bigl(T(\avec)\psi\bigr)(\xvec) = \psi(\xvec-\avec),
:::

which is a 3-dimensional version of {eq}`eq-spatialdof-23`. In both Eqs~{eq}`eq-orbamsph-13` and {eq}`eq-orbamsph-14`, the transformed wave function, evaluated at some point, is the original wave function evaluated at the inverse transformed point. As explained in {ref}`sec-spatialdof-3`, a mnemonic for remembering this is to write $\xvec' = \Rmat\xvec$ for the “old” and “new” points $\xvec$ and $\xvec'$, respectively, and then to say, the value of the old wave function at the old point is equal to the value of the new wave function at the new point, that is,

:::{math}
:label: eq-orbamsph-15
\psi'(\xvec') = \psi(\xvec).
:::

This rule is necessary in the active point of view. For example, if the old wave function $\psi(\xvec)$ has a large concentration of probability around a point $\xvec_0$, then the new, rotated wave function must have a large concentration around the actively rotated point $\Rmat\xvec_0$. See Fig.~\figr\spatialdof.1 for an illustration in the case of translations.

It is now easy to show that the operators $U(\Rmat)$ are unitary. We simply compute the square norm of the new wave function,

:::{math}
:label: eq-orbamsph-16
\int d^3\xvec \, |\psi'(\xvec)|^2 = \int d^3\xvec \, |\psi(\Rmat^{-1}\xvec)|^2 = \int d^3\xvec \, |\psi(\xvec)|^2,
:::

where in the last step we have performed a change of variables of integration, $\xvec'=\Rmat^{-1}\xvec$, and then dropped the prime. We see that the norm of an arbitrary state is preserved by $U(\Rmat)$, which is therefore unitary. See Prob. {ref}`prob-hilbert-6`(c) and (d).

In summary, we have found a representation of the classical rotations acting on the Hilbert space of our quantum mechanical system by means of unitary operators. This is precisely the starting point for the theory laid out in {ref}`ch-repsamos`. Notice by the way that the representation is single-valued, that is, there is only one unitary operator $U(\Rmat)$ for each $\Rmat$. This means that of the possible values for the angular momentum quantum number shown in {eq}`eq-repsamos-32`, the half-integer values cannot occur, since they lead to double-valued representations. That is, $\ell$ can only take on the values $\{0,1,2,\ldots\}$.

(sec-orbamsph-3)=

## The Orbital Angular Momentum $\Lvec$

We define the orbital angular momentum $\Lvec$ as the generators of our rotation operators $U(\Rmat)$. We can find $\Lvec$ explicitly by working with infinitesimal rotations. Let us write such a rotation in axis-angle form,

:::{math}
:label: eq-orbamsph-17
\Rmat({\hat{\mathbf{n}}},\theta) = \Imat + \theta {\hat{\mathbf{n}}}\cdot\Jmatvec,
:::

where $\theta \ll 1$. The corresponding unitary operator is

:::{math}
:label: eq-orbamsph-18
U({\hat{\mathbf{n}}},\theta) = 1 - {i\over\hbar} \theta {\hat{\mathbf{n}}}\cdot\Lvec,
:::

which is the definition of $\Lvec$. See {eq}`eq-repsamos-2` and {eq}`eq-repsamos-3`.

We substitute these infinitesimal rotations into {eq}`eq-orbamsph-13`. On the right we will need $\Rmat^{-1}$, which is given by

:::{math}
:label: eq-orbamsph-19
\Rmat({\hat{\mathbf{n}}},\theta)^{-1} = \Imat - \theta {\hat{\mathbf{n}}}\cdot\Jmatvec,
:::

that is, {eq}`eq-orbamsph-17` with $\theta \to -\theta$. Then {eq}`eq-orbamsph-13` becomes

:::{math}
:label: eq-orbamsph-20
\Bigl(1-{i\over\hbar} \theta {\hat{\mathbf{n}}}\cdot\Lvec\Bigr) \psi(\xvec) = \psi\bigl((\Imat - \theta {\hat{\mathbf{n}}}\cdot\Jmatvec)\xvec\bigr) = \psi(\xvec - \theta {\hat{\mathbf{n}}}\cross\xvec) = \psi(\xvec) - \theta ({\hat{\mathbf{n}}} \cross \xvec) \cdot \del \psi,
:::

where we have expanded the right hand side out to first order in $\theta$. The leading order terms cancel, and $\theta$ cancels from the first order terms, which can be written as

:::{math}
:label: eq-orbamsph-21
({\hat{\mathbf{n}}}\cdot\Lvec)\psi = -i\hbar ({\hat{\mathbf{n}}} \cross \xvec)\cdot \del \psi = ({\hat{\mathbf{n}}} \cross \xvec) \cdot \pvec \,\psi = {\hat{\mathbf{n}}}\cdot(\xvec \cross \pvec) \psi,
:::

where we have introduced the momentum operator $\pvec$ which is $-i\hbar\del$ when acting on wave functions $\psi(\xvec)$. Since ${\hat{\mathbf{n}}}$ and $\psi$ are arbitrary, {eq}`eq-orbamsph-21` implies

:::{math}
:label: eq-orbamsph-22
\Lvec=\xvec\cross\pvec.
:::

Our definition {eq}`eq-orbamsph-3` of the rotation operators gives a definition of angular momentum that coincides with the usual definition of orbital angular momentum in quantum mechanics.

According to the theory presented in {ref}`ch-spinrot`\ and \repsamos, the components of $\Lvec$ must satisfy the commutation relations,

:::{math}
:label: eq-orbamsph-23
[L_i,L_j] = i\hbar \, \epsilon_{ijk} \, L_k.
:::

That they do so is easily verified from the definition {eq}`eq-orbamsph-22` (if it were not true, there would be something seriously wrong with the whole theory.) Next, following the theory laid out in {ref}`ch-repsamos`, we work on constructing the standard angular momentum basis.

(sec-orbamsph-4)=

## Orbital Angular Momentum Operators in Spherical Coordinates

The standard angular momentum basis is an eigenbasis of the operators $(L^2,L_z)$, with certain phase and other conventions. Thus in the present case the basis vectors are wave functions indexed by $\ell$ and $m$ such that

:::{math}
:label: eq-orbamsph-24
\begin{aligned}
L^2 \psi_{\ell m}(\xvec) &= \ell(\ell+1) \hbar^2 \psi_{\ell m}(\xvec), \\
L_z \psi_{\ell m}(\xvec) &= m \hbar \psi_{\ell m}(\xvec). \\

\end{aligned}
:::

The key to finding these wave functions is to first find the “stretched” states, that is, the states with $m=\ell$ (the maximum value of $m$ for a given $\ell$). States for other values of $m$ can then be generated by applying lowering operators. The stretched wave functions $\psi_{\ell\ell}$ satisfy {eq}`eq-orbamsph-24` with $m=\ell$. The operator $L^2$ is, however, somewhat difficult to work with. It turns out to be easier to specify the stretched state as the eigenstate of $L_z$ with eigenvalue $\ell\hbar$ which is annihilated by the raising operator. See {eq}`eq-repsamos-28`. Thus the stretched state satisfies

:::{math}
:label: eq-orbamsph-25
\begin{aligned}
L_z \psi_{\ell\ell}(\xvec) &= \ell \hbar \,\psi_{\ell\ell}(\xvec),
\end{aligned}
:::

:::{math}
:label: eq-orbamsph-26
\begin{aligned}
L_+ \psi_{\ell\ell}(\xvec) &= 0.
\end{aligned}
:::

These equations are most conveniently solved in spherical coordinates.

Writing out the three components of $\Lvec$ as differential operators in rectangular coordinates, we can apply the chain rule to transform them to spherical coordinates. The transformation is straightforward but requires some algebra. See the Jacobian matrices {eq}`eq-vecident-24` and {eq}`eq-vecident-25`. The results are

:::{math}
:label: eq-orbamsph-27
\begin{aligned}
L_x &= -i\hbar\Bigl( y\pop{}{z}-z\pop{}{y}\Bigr) = -i\hbar\Bigl( -\sin\phi\pop{}{\theta} -\cot\theta \cos\phi\pop{}{\phi}\Bigr), \\
L_y &= -i\hbar\Bigl( z\pop{}{x}-x\pop{}{z}\Bigr) = -i\hbar\Bigl(\cos\phi\pop{}{\theta} -\cot\theta \sin\phi\pop{}{\phi}\Bigr), \\
L_z &= -i\hbar\Bigl( x\pop{}{y}-y\pop{}{x} \Bigr) = -i\hbar \pop{}{\phi}. \\

\end{aligned}
:::

The component $L_z$ is particularly simple in spherical coordinates, and it is not hard to see why: $L_z$ is the generator of rotations about the $z$-axis, and $\phi$ is the azimuthal angle. The usual spherical coordinate system singles out the $z$-axis for special treatment, which is why the operators $L_x$ and $L_y$ are more complicated.

Next we compute the raising and lowering operators,

:::{math}
:label: eq-orbamsph-28
L_\pm = L_x \pm iL_y = -i\hbar \, e^{\pm i\phi} \Bigl( \pm i\pop{}{\theta} -\cot\theta\pop{}{\phi} \Bigr),
:::

and the Casimir operator $L^2$,

:::{math}
:label: eq-orbamsph-29
L^2 = {1\over2} \bigl( L_+L_- + L_-L_+ \bigr) + L_z^2 = -\hbar^2 \Bigl[ {1\over\sin\theta} \pop{}{\theta} \Bigl( \sin\theta\pop{}{\theta}\Bigr) +{1\over\sin^2\theta} {\partial^2\over\partial \phi^2} \Bigr].
:::

At this point we notice the relation of $L^2$ to the Laplacian operator,

:::{math}
:label: eq-orbamsph-30
\pvec^2 \psi = -\hbar^2 \del^2 \psi = -\hbar^2 {1\over r^2} \pop{}{r} \Bigl( r^2 \frac{\partial \psi}{\partial r}\Bigr) +{L^2\over r^2} \psi.
:::

See {eq}`eq-vecident-23`. We will come back to this formula later, but for now we are more interested in angular momentum than kinetic energy.

A striking feature about the operators $\Lvec$ in spherical components is that the radial differential operator $\partial/\partial r$ does not occur in them (hence it does not occur in any function of $\Lvec$, either, such as $L^2$, $L_\pm$, or the rotation operators $\exp(-i\theta {\hat{\mathbf{n}}} \cdot \Lvec/\hbar)$). The geometrical reason is that rotations in physical space change the direction of vectors, but not their magnitude; therefore the motion of the tip of a given vector takes place on the surface of a sphere. This is also true of infinitesimal rotations, which connect nearby points of the same $r$ value but different $\theta$ and $\phi$ values. Therefore the components of $\Lvec$, in terms of which infinitesimal rotations are expressed, do not involve any differentiation with respect to $r$.

(sec-orbamsph-5)=

## The Hilbert Space of Wave Functions on a Sphere

Because of this fact, we can think of the angular momentum operators as acting on functions $f(\theta,\phi)$ defined on the sphere, rather than on functions $\psi(\xvec)=\psi(r,\theta,\phi)$ defined in the full 3-dimensional space. The radius of the sphere is unimportant (since when using it we are only interested the angular dependence), so we can take it to be a sphere of unit radius. This is often a useful point of view, and we will now make a small digression for notation for functions defined on the unit sphere.

We denote a point on the unit sphere either by $(\theta,\phi)$ or by ${\hat{\mathbf{r}}}$, indicating a unit vector based at the origin whose tip lies on the unit sphere. For example, we will write $f(\theta,\phi)=f({\hat{\mathbf{r}}})$. We will adopt a Dirac bra-ket notation for functions on the unit sphere, for example, making the association,

:::{math}
:label: eq-orbamsph-31
f(\theta,\phi) = f({\hat{\mathbf{r}}}) \longleftrightarrow \ket{f}.
:::

We define the scalar product of two such functions by

:::{math}
:label: eq-orbamsph-32
\braket{f}{g} = \int d\Omega \, f(\theta,\phi)^\cc g(\theta,\phi),
:::

where $d\Omega=\sin\theta \, d\theta\,d\phi$. This makes the space of normalizable wave functions on the unit sphere into a Hilbert space. We define a $\delta$-function on the unit sphere by

:::{math}
:label: eq-orbamsph-33
\delta_{\theta_0\phi_0}(\theta,\phi) = {\delta(\theta-\theta_0)\delta(\phi-\phi_0) \over \sin\theta},
:::

which is a function concentrated at the point $(\theta_0,\phi_0)$. Then

:::{math}
:label: eq-orbamsph-34
\int d\Omega \, \delta_{\theta_0\phi_0}(\theta,\phi) f(\theta,\phi) = f(\theta_0,\phi_0),
:::

for any function $f$. We associate this $\delta$-function with a ket by

:::{math}
:label: eq-orbamsph-35
\delta_{\theta_0\phi_0}(\theta,\phi) \longleftrightarrow \ket{{\hat{\mathbf{r}}}_0},
:::

where $(\theta_0,\phi_0)={\hat{\mathbf{r}}}_0$. Then we have

:::{math}
:label: eq-orbamsph-36
f(\theta,\phi)=f({\hat{\mathbf{r}}}) = \braket{{\hat{\mathbf{r}}}}{f}.
:::

(sec-orbamsph-6)=

## The Standard Angular Momentum Basis for Orbital Angular Momentum

We return to {eq}`eq-orbamsph-25` and {eq}`eq-orbamsph-26` for the stretched wave function $\psi_{\ell\ell}(r,\theta,\phi)$, which we express in spherical coordinates. First, the $L_z$ equation {eq}`eq-orbamsph-25` can be written,

:::{math}
:label: eq-orbamsph-37
-i\hbar \frac{\partial \psi(r,\theta,\phi)}{\partial \phi} = \ell\hbar \,\psi(r,\theta,\phi),
:::

which has the general solution

:::{math}
:label: eq-orbamsph-38
\psi_{\ell\ell}(r,\theta,\phi) = F_{\ell\ell}(r,\theta) e^{i\ell\phi},
:::

where $F_{\ell\ell}(r,\theta)$ is an arbitrary function. By the theory of {ref}`ch-repsamos`\ we know that $\ell$ must be a nonnegative integer or half-integer, but in fact {eq}`eq-orbamsph-38` shows that $\ell$ must be an integer since otherwise the wave function $\psi_{\ell\ell}$ would not be single-valued. Wave functions in quantum mechanics are single-valued functions of position because $\psi(\xvec)$ is just the expansion of the state $\ket{\psi}$ with respect to the position eigenbasis, and the basis kets $\ket{\xvec}$ are single-valued. This is the same conclusion we reached earlier at the end of \secrorbamsph-2. Thus we have determined the $\phi$-dependence of the function $\psi_{\ell\ell}(r,\theta,\phi)$.

To get the $\theta$-dependence, we call on the $L_+$-equation {eq}`eq-orbamsph-26`, using {eq}`eq-orbamsph-28` for $L_+$ in spherical coordinates. Applying this to the form {eq}`eq-orbamsph-38` for $\psi_{\ell\ell}$, the $\phi$-derivatives can be carried out, whereupon we find

:::{math}
:label: eq-orbamsph-39
-i\hbar e^{i\phi}\Bigl(i\pop{}{\theta} -i\ell\cot\theta\Bigr)F_{\ell\ell}(r,\theta)e^{i\ell\phi} =0,
:::

or, canceling various factors,

:::{math}
:label: eq-orbamsph-40
\pop{F_{\ell\ell}(r,\theta)}{\theta} = \ell\cot\theta F_{\ell\ell}(r,\theta).
:::

This has the solution,

:::{math}
:label: eq-orbamsph-41
F_{\ell\ell}(r,\theta)=u(r) \sin^\ell\theta,
:::

where $u(r)$ is an arbitrary function of $r$, or

:::{math}
:label: eq-orbamsph-42
\psi_{\ell\ell}(r,\theta,\phi) = u(r) \sin^\ell\theta \, e^{i\ell\phi}.
:::

These are the stretched wave functions.

We see that the simultaneous eigenfunctions of $L^2$ and $L_z$ are indeed degenerate, since any radial function $u(r)$ may appear in {eq}`eq-orbamsph-42`. In order to resolve these degeneracies, we may introduce an arbitrarily chosen basis $\{ u_n(r)\}$ of radial wave functions, and write

:::{math}
:label: eq-orbamsph-43
\psi_{n\ell\ell}(r,\theta,\phi) = u_n(r) \sin^\ell\theta e^{i\ell\phi}.
:::

The index $n$ we use here serves the same purpose as the index $\gamma$ used in {ref}`ch-repsamos`; it labels an arbitrarily chosen orthonormal basis in the stretched eigenspace. We see that the multiplicity of the integral values of $\ell$ on the Hilbert space of wave function $\psi(\xvec)$ is infinity.

Another approach is simply to throw away the radial variables, and work on the unit sphere. On the Hilbert space of wave functions $f(\theta,\phi)$ on the unit sphere, the simultaneous stretched eigenfunction of $L^2$ and $L_z$ is

:::{math}
:label: eq-orbamsph-44
f_{\ell\ell}(\theta,\phi) = \sin^\ell\theta \, e^{i\ell\phi},
:::

and it is nondegenerate. Therefore, on this Hilbert space, the multiplicity $N_\ell$ is zero for half-integral $\ell$, and unity for integral $\ell$. When we normalize $f_{\ell\ell}$ using the rule

:::{math}
:label: eq-orbamsph-45
\braket{f}{f}=\int d\Omega \, |f|^2 =1,
:::

we find

:::{math}
:label: eq-orbamsph-46
Y_{\ell\ell}(\theta,\phi) = {(-1)^\ell \over 2^\ell \ell!} \sqrt{\displaystyle {\displaystyle (2\ell+1)! \over \displaystyle 4\pi}} \, \sin^\ell \theta \, e^{i\ell\phi},
:::

where we have identified the normalized $f_{\ell\ell}$ with the stretched spherical harmonic $Y_{\ell\ell}$, and where we have introduced the conventional phase factor $(-1)^\ell$. Recall that in the general theory developed in {ref}`ch-repsamos`, the phase of the stretched state $\ket{jj}$ was left arbitrary.

To obtain the states corresponding to other values of $m$, we can apply lowering operators. We use {eq}`eq-repsamos-43`, making the replacements, $j\to\ell$, $J_-\to L_-$. By induction one can show that

:::{math}
:label: eq-orbamsph-47
\Bigl({L_-\over\hbar}\Bigr)^{\ell-m} \sin^\ell\theta e^{i\ell\phi} = {e^{im\phi} \over \sin^m \theta} \Bigl[ {d\over d(\cos\theta)} \Bigr]^{\ell-m} \sin^{2\ell}\theta,
:::

and altogether we find

:::{math}
:label: eq-orbamsph-48
Y_{\ell m}(\theta,\phi) = {(-1)^\ell \over 2^\ell \ell!} \sqrt{\displaystyle{\displaystyle 2\ell+1 \over \displaystyle 4\pi} {\displaystyle (\ell+m)! \over \displaystyle (\ell-m)!}} \, {e^{im\phi} \over \sin^m \theta} \Bigl[ {d\over d(\cos\theta)} \Bigr]^{\ell-m} \sin^{2\ell}\theta.
:::

This formula is valid for all $m$ in the range, $-\ell\le m \le +\ell$.

{eq}`eq-orbamsph-48` can be expressed in terms of Legendre polynomials and associated Legendre functions. First we consider the case $m=0$, and call on the Rodriguez formula for the Legendre polynomial $P_\ell(x)$ [see Abramowitz and Stegun, Eq.~(8.6.18)],

:::{math}
:label: eq-orbamsph-49
P_\ell(x) = {(-1)^\ell \over 2^\ell \ell!}  {d^\ell \over dx^\ell} (1-x^2)^\ell,
:::

where we set

:::{math}
:label: eq-orbamsph-50
x=\cos\theta.
:::

Then {eq}`eq-orbamsph-48` becomes

:::{math}
:label: eq-orbamsph-51
Y_{\ell 0}(\theta,\phi) = \sqrt{\displaystyle { \displaystyle 2\ell+1 \over \displaystyle 4\pi}} \, P_\ell(\cos\theta).
:::

The choice of the phase factor $(-1)^\ell$ in {eq}`eq-orbamsph-46` was designed to make $Y_{\ell 0}$ real and positive at the north pole ($\cos\theta=1$); this follows from {eq}`eq-orbamsph-75`.

Now let us consider the case $m\ge0$. We can construct the $Y_{\ell m}$ for this case by applying raising operators to the state $Y_{\ell 0}$. Using induction on {eq}`eq-repsamos-48a`, we obtain

:::{math}
:label: eq-orbamsph-52
\ket{\ell m} = \sqrt{\displaystyle {\displaystyle (\ell-m)! \over \displaystyle (\ell+m)!}} \Bigl( {L_+\over\hbar} \Bigr)^m \ket{\ell 0}.
:::

(This formula only works for integer angular momentum, since the value $m=0$ is possible only in this case.) Next we use induction to obtain

:::{math}
\begin{aligned}
\Bigl({L_+\over\hbar}\Bigr)^m P_\ell(\cos\theta) &= (-1)^m \sin^m \theta\, e^{im\phi} \Bigl[{d\over d(\cos\theta)}\Bigr]^m P_\ell(\cos\theta)
\end{aligned}
:::

:::{math}
:label: eq-orbamsph-53
\begin{aligned}
&= (-1)^m e^{im\phi} \, P_{\ell m}(\cos\theta),
\end{aligned}
:::

where we have introduced the associated Legendre function, defined by

:::{math}
:label: eq-orbamsph-54
P_{\ell m}(x) = (1-x^2)^{m/2} {d^m P_\ell(x)\over dx^m}.
:::

[See Abramowitz and Stegun, Eq.~(8.6.6), and beware of the difference between their function $P^m_n$ and $P_{nm}$, see the on notation on p.~332.] Altogether, for $m\ge0$ we have

:::{math}
:label: eq-orbamsph-55
Y_{\ell m}(\theta,\phi) = (-1)^m \sqrt{\displaystyle {\displaystyle 2\ell+1\over \displaystyle 4\pi} {\displaystyle (\ell-m)! \over \displaystyle (\ell+m)!}} \, e^{im\phi} \, P_{\ell m}(\cos\theta).
:::

For the case $m<0$, we go back to {eq}`eq-orbamsph-48`, we set $m=-|m|$, and we use {eq}`eq-orbamsph-49` and {eq}`eq-orbamsph-54`. The result is

:::{math}
:label: eq-orbamsph-56
Y_{\ell,-|m|}(\theta,\phi) = \sqrt{\displaystyle {\displaystyle 2\ell+1 \over \displaystyle 4\pi} {\displaystyle (\ell -|m|)! \over \displaystyle (\ell+|m|)!}} \, e^{-i|m|\phi} \, P_{\ell,|m|}(\cos\theta),
:::

which is equivalent to

:::{math}
:label: eq-orbamsph-57
Y_{\ell,-m}(\theta,\phi) = (-1)^m Y_{\ell m}(\theta,\phi)^\cc,
:::

valid for any value of $m$.

In summary, the standard angular momentum basis for the space of wave functions $f(\theta,\phi)$ defined on the unit sphere consists of the $Y_{\ell m}$'s. The irreducible subspaces are the $(2\ell+1)$-dimensional spaces of wave functions spanned by the $Y_{\ell m}$'s for fixed $\ell$ with $m=-\ell,\ldots, +\ell$. There is precisely one such subspace for each integer value of $\ell$ in the Hilbert space of wave functions on the sphere. For the Hilbert space of wave functions on three-dimensional space, there is an infinite set of irreducible subspaces for each integer value of $\ell$, that is, the spaces of wave functions spanned by $u_n(r) Y_{\ell m}(\theta,\phi)$ for fixed $n$ and $\ell$.

Notice that the theory of the $Y_{\ell m}$'s is completely founded on the general theory of raising and lowering operators as laid out in {ref}`ch-repsamos`, and that even the phase conventions are the standard ones presented in those notes. Only the phase $(-1)^\ell$ of the stretched state in {eq}`eq-orbamsph-46` goes beyond the conventions established in those notes.

(sec-orbamsph-7)=

## Table of $Y_{\ell m}$'s

We present a short table of $Y_{\ell m}$'s:

:::{math}
:label: eq-orbamsph-58
\begin{aligned}
Y_{00}&={1\over\sqrt{4\pi}}, \quad Y_{11}=-\sqrt{\ds3\over\ds 8\pi}\,\sin\theta\,e^{i\phi},\quad Y_{10}=\sqrt{\ds3\over\ds 4\pi}\,\cos\theta,\quad Y_{1,-1}=\sqrt{\ds3\over\ds 8\pi}\,\sin\theta\,e^{-i\phi}, \\
Y_{22}&=\sqrt{\ds15\over 32\pi}\,\sin^2\theta\,e^{2i\phi}, \quad Y_{21}=-\sqrt{\ds15\over 8\pi}\,\sin\theta\cos\theta\, e^{i\phi},\quad Y_{20}=\sqrt{\ds5\over 16\pi}\, (3\cos^2\theta-1), \\
Y_{2,-1}&= \sqrt{\ds15\over 8\pi}\, \sin\theta\cos\theta \,e^{-i\phi}, \quad Y_{2,-2}= \sqrt{\ds15\over 32\pi}\, \sin^2\theta\, e^{-2i\phi}. \\

\end{aligned}
:::

(sec-orbamsph-8)=

## $Y_{\ell m}$'s in Cartesian Coordinates

Sometimes versions of the spherical harmonics in Cartesian coordinates are useful. If we multiply {eq}`eq-orbamsph-46` by $r^\ell$, we obtain

:::{math}
:label: eq-orbamsph-59
r^\ell\, Y_{\ell\ell}(\theta,\phi) = {(-1)^\ell \over 2^\ell \, \ell!} \sqrt{\ds (2\ell+1)! \over \ds 4\pi}\, (x+iy)^\ell.
:::

This is a homogeneous polynomial in $x$, $y$ and $z$ of degree $\ell$. We can create the $Y_{\ell m}$'s for other values of $m$ by applying the lowering operator $L_-$, which in Cartesian coordinates is

:::{math}
:label: eq-orbamsph-60
L_- = L_x -iL_y = -i\hbar\Bigl[\Bigl(y\pop{}{z}-z\pop{}{y} \Bigr) - i\Bigl(z\pop{}{x}-x\pop{}{z}\Bigr)\Bigr].
:::

While carrying out the derivatives might be complicated, notice that each derivative $\partial/\partial x$, $\partial/\partial y$, $\partial/\partial z$, lowers the degree of the polynomial, while the multiplication by $x$, $y$ or $z$ raises it back. Thus we see that $r^\ell Y_{\ell m}(\theta,\phi)$, when expressed in Cartesian coordinates, is a homogeneous polynomial in $x$, $y$, and $z$ of degree $\ell$, for all $m$.

An important application of this fact is that under parity, which causes $(x,y,z)$ to go into $(-x,-y,-z)$, the function $Y_{\ell m}$ changes by $(-1)^\ell$. This is the parity of $Y_{\ell m}$, and hence of the wavefunctions $R_{n\ell}(r) Y_{\ell m}(\theta,\phi)$ that occur in central force problems. Notice that the parity depends only on $\ell$, and is independent of $m$. Parity is covered in detail in {ref}`ch-parity`.

(sec-orbamsph-9)=

## Rotating $Y_{\ell m}$'s

There are several interesting and useful results that follow from applying rotation operators to the $Y_{\ell m}$'s. It is often important to rotate the $Y_{\ell m}$'s, because by the very definition of the spherical coordinates $(\theta,\phi)$, a privileged role has been assigned to the $z$-axis. In addition, the $z$-axis has been selected out again for a privileged role by the standard convention of working with eigenfunctions of $L^2$ and $L_z$. In many problems it is necessary to refer calculations to another axis, something that can be done with rotation operators.

First let us write the ket $\ket{\ell m}$ to stand for the function $Y_{\ell m}(\theta,\phi)$, regarded as a function defined on the unit sphere, so that

:::{math}
:label: eq-orbamsph-61
Y_{\ell m}({\hat{\mathbf{r}}}) = \braket{{\hat{\mathbf{r}}}}{\ell m}.
:::

Since we have determined that $Y_{\ell m}$ is the nondegenerate eigenfunction of $L^2$ and $L_z$ on the unit sphere, we do not need any extra quantum numbers in $\ket{\ell m}$. We now apply a rotation operator specified by $\Rmat$ to a $Y_{\ell m}$ and use {eq}`eq-orbamsph-13`. We have

:::{math}
:label: eq-orbamsph-62
\bigl( U(\Rmat)Y_{\ell m}\bigr)({\hat{\mathbf{r}}}) = Y_{\ell m} \bigl(\Rmat^{-1} {\hat{\mathbf{r}}} \bigr) =\matrixelement{{\hat{\mathbf{r}}}}{U(\Rmat)}{\ell m} =\sum_{m'} \braket{{\hat{\mathbf{r}}}}{\ell m'} \matrixelement{\ell m'}{U(\Rmat)}{\ell m},
:::

where in effect we rotate the $Y_{\ell m}$ in two ways, once by rotating the argument in three-dimensional space, and the other time by rotating it as a basis function in its irreducible subspace of Hilbert space. The matrix element in the final expression is a $D$ matrix, so we obtain

:::{math}
:label: eq-orbamsph-63
\bigl(U(\Rmat) Y_{\ell m} \bigr)({\hat{\mathbf{r}}}) = Y_{\ell m}(\Rmat^{-1}{\hat{\mathbf{r}}}) = \sum_{m'} Y_{\ell m'}({\hat{\mathbf{r}}}) \, D^\ell_{m'm}(\Rmat).
:::

This may be recognized as a special case of {eq}`eq-repsamos-87`.

{eq}`eq-orbamsph-63` gives $Y_{\ell m}$ at one point on the sphere as a linear combination of other $Y_{\ell m}$'s, for the same value of $\ell$ but all values of $m$, at another point on the sphere. The fact that the linear combination does not involve other values of $\ell$ is due to the invariance of the irreducible subspace spanned by the $Y_{\ell m}$'s for fixed $\ell$ but variable $m$, under the action of rotations.

{eq}`eq-orbamsph-63` can be used to express the values of the $Y_{\ell m}$'s at a point of interest in terms of the their values at the north pole (a convenient reference point). To put this in convenient form, we change notation in {eq}`eq-orbamsph-63`, and replace ${\hat{\mathbf{r}}}$ by ${\hat{\mathbf{z}}}$, and replace $\Rmat$ by $\Rmat^{-1}$. Then we write ${\hat{\mathbf{r}}}=\Rmat{\hat{\mathbf{z}}}$, so that $\Rmat$ is interpreted as a rotation that maps the ${\hat{\mathbf{z}}}$-axis into some direction ${\hat{\mathbf{r}}}$ of interest. Then we obtain

:::{math}
:label: eq-orbamsph-64
Y_{\ell m}({\hat{\mathbf{r}}}) = \sum_{m'} Y_{\ell m'}({\hat{\mathbf{z}}}) \, D^\ell_{m'm}(\Rmat^{-1}).
:::

If we write ${\hat{\mathbf{r}}}=(\theta,\phi)$ for the direction of interest, then a rotation that maps the ${\hat{\mathbf{z}}}$-axis into this direction is easily given in Euler angle form,

:::{math}
:label: eq-orbamsph-65
\Rmat(\phi,\theta,0){\hat{\mathbf{z}}} = {\hat{\mathbf{r}}},
:::

that is, with $\alpha=\phi$ and $\beta=\theta$, because the first two Euler angles were designed to specify the direction of the rotated ${\hat{\mathbf{z}}}$-axis. Also, the value of $Y_{\ell m}$ at the north pole is especially simple, because all the associated Legendre functions $P_{\ell m}(\cos\theta)$ vanish at $\theta=0$ unless $m=0$, and in that case we have $P_\ell(1)=1$. Therefore

:::{math}
:label: eq-orbamsph-66
Y_{\ell m}({\hat{\mathbf{z}}}) = \sqrt{2\ell+1\over 4\pi} \, \delta_{m0}.
:::

Finally, we can use {eq}`eq-repsamos-71` to rewrite the matrix $D(\Rmat^{-1})$, and {eq}`eq-orbamsph-64` becomes,

:::{math}
:label: eq-orbamsph-67
\boxed{ Y_{\ell m}(\theta,\phi) = \sqrt{2\ell+1\over 4\pi}\, D^{\ell\cc}_{m0}(\phi,\theta,0).}
:::

In this way we have found a useful connection between the $Y_{\ell m}$'s and the $D$-matrices.

(sec-orbamsph-10)=

## The Addition Theorem for Spherical Harmonics

We can use this to derive another nice result. Consider the following function defined on the unit sphere:

:::{math}
:label: eq-orbamsph-68
f(\theta,\phi)=f({\hat{\mathbf{r}}})=P_\ell(\cos\theta) =P_\ell({\hat{\mathbf{r}}}\cdot{\hat{\mathbf{z}}}) = \sqrt{4\pi\over 2\ell+1}\, Y_{\ell 0}({\hat{\mathbf{r}}}),
:::

where $P_\ell$ is the usual Legendre polynomial and ${\hat{\mathbf{r}}}=(\theta,\phi)$ is some direction of interest. Now let us rotate this function by some rotation specified by $\Rmat$. We have

:::{math}
:label: eq-orbamsph-69
\bigl(U(\Rmat)f\bigr)({\hat{\mathbf{r}}}) = f(\Rmat^{-1}{\hat{\mathbf{r}}}) =P_\ell(\Rmat^{-1}{\hat{\mathbf{r}}}\cdot{\hat{\mathbf{z}}}) =P_\ell({\hat{\mathbf{r}}}\cdot\Rmat{\hat{\mathbf{z}}}),
:::

where in the final step we use the fact that $\Rmat^{-1}=\Rmat^t$ to transfer the rotation matrix from ${\hat{\mathbf{r}}}$ to ${\hat{\mathbf{z}}}$ in the scalar product. See Prob. {ref}`prob-classrot-2`(a). Now we choose the matrix $\Rmat$ to have the Euler angle form $\Rmat(\phi',\theta',0)$, so that ${\hat{\mathbf{r}}}' =(\theta',\phi')= \Rmat{\hat{\mathbf{z}}}$, where ${\hat{\mathbf{r}}}'$ is another direction of interest (in addition to ${\hat{\mathbf{r}}}$). Then {eq}`eq-orbamsph-68` and {eq}`eq-orbamsph-69` become

:::{math}
:label: eq-orbamsph-70
P_\ell({\hat{\mathbf{r}}}\cdot{\hat{\mathbf{r}}}')=\sqrt{4\pi\over 2\ell+1}\, Y_{\ell 0}(\Rmat^{-1}{\hat{\mathbf{r}}}) = \sqrt{4\pi\over 2\ell+1} \sum_m Y_{\ell m}({\hat{\mathbf{r}}}) \, D^\ell_{m0}(\theta',\phi',0),
:::

where we use {eq}`eq-orbamsph-63` to expand the rotated $Y_{\ell m}$. Finally, we use {eq}`eq-orbamsph-67` to write the result purely in terms of $Y_{\ell m}$'s, and we have

:::{math}
:label: eq-orbamsph-71
\boxed{P_\ell({\hat{\mathbf{r}}}\cdot{\hat{\mathbf{r}}}') = {4\pi\over 2\ell+1} \sum_m Y_{\ell m}(\theta,\phi) \, Y_{\ell m}^\cc(\theta',\phi'),}
:::

which is the (very useful) *addition theorem* for the spherical harmonics.

(sec-orbamsph-11)=

## The Multipole Expansion in Electrostatics

We will now review the multipole expansion in electrostatics, which fits in well at this point in the presentation and which will be of use several times in the course.

We begin with the Legendre polynomials, which are defined by

:::{math}
:label: eq-orbamsph-72
{1\over\sqrt{1-2ux + u^2}} = \sum_{\ell=0}^\infty u^\ell\,P_\ell(x),
:::

where the series converges for $|u|<1$. That is, they are the coefficients of the expansion of the left-hand side in powers of the parameter $u$. The left-hand side is considered the *generating function* of the Legendre polynomials. Carrying out the expansion, we find the first few Legendre polynomials,

:::{math}
:label: eq-orbamsph-73
P_0(x)=1, \qquad P_1(x)=x, \qquad P_2(x)={1\over2}(3x^2-1).
:::

Note that if we set $x=1$ in {eq}`eq-orbamsph-72` we obtain

:::{math}
:label: eq-orbamsph-74
{1\over 1-u} = \sum_{\ell=0}^\infty u^\ell P_\ell(1).
:::

Comparing the Taylor series expansion of the left-hand side with the series on the right, we find

:::{math}
:label: eq-orbamsph-75
P_\ell(1)=1.
:::

This is essentially the standard normalization for the Legendre polynomials.

:::{figure} images/orbamsph-fig01.png
:label: fig-orbamsph-1
:width: 80%

The origin of a system of coordinates is located inside a localized charge distribution with density $\rho$. The variable $\xvec'$ runs over the charge distribution, while $\xvec$ is a field point at which the potential $\Phi$ is desired.
:::

Now consider a localized charge distribution $\rho$, as in {ref}`fig-orbamsph-1`, with a field point $\xvec$ that is well outside the distribution. The electrostatic potential at $\xvec$ is given by

:::{math}
:label: eq-orbamsph-76
\Phi(\xvec) = \int d^3\xvec'\, {\rho(\xvec')\over |\xvec-\xvec'|}
:::

[see {eq}`eq-emunits-5`], where the variable of integration $\xvec'$ runs over the charge distribution. Writing $r=|\xvec|$ and $r'=|\xvec'|$, we have

:::{math}
:label: eq-orbamsph-77
|\xvec-\xvec'| = \sqrt{r^2-2\xvec\cdot\xvec'+r'^2} =r\sqrt{1-2u\cos\gamma+u^2},
:::

where $u=r'/r<1$ and $\gamma$ is the angle between the vectors $\xvec$ and $\xvec'$, as shown in the figure. Then using the expansion {eq}`eq-orbamsph-72` we have

:::{math}
:label: eq-orbamsph-78
{1\over |\xvec-\xvec'|} = \sum_{\ell=0}^\infty {r^{\prime\ell}\over r^{\ell+1}} P_\ell(\cos\gamma) =\sum_{\ell m} {r^{\prime\ell}\over r^{\ell+1}} {4\pi\over 2\ell+1} \, Y_{\ell m}(\theta,\phi) Y_{\ell m}^\cc(\theta'\phi'),
:::

where in the last step we use the addition theorem {eq}`eq-orbamsph-71`, and where $(r\theta\phi)$ are the spherical coordinates of $\xvec$ and $(r'\theta'\phi')$ are those of $\xvec'$. This allows us to write the potential as

:::{math}
:label: eq-orbamsph-79
\Phi(r,\theta,\phi) = \sum_{\ell=0}^\infty \sqrt{\ds 4\pi\over\ds 2\ell+1} \, {1\over r^{\ell+1}}\sum_m Y_{\ell m}(\theta,\phi) \, C_{\ell m},
:::

where the coefficients $C_{\ell m}$ characterize the charge distribution and are given by

:::{math}
:label: eq-orbamsph-80
C_{\ell m}= \sqrt{\ds 4\pi\over\ds 2\ell+1} \int d^3\xvec'\, \rho(\xvec')\,r^{\prime\ell} \, Y_{\ell m}^\cc (\theta',\phi').
:::

Since $r^{\prime\ell} Y_{\ell m}^\cc(\theta',\phi')$ is a homogeneous polynomial in $(x',y',z')$ of degree $\ell$ (see \secrorbamsph-8), the coefficients $C_{\ell m}$ are moments of degree $\ell$ of the charge distribution. {eq}`eq-orbamsph-79` is the multipole expansion of the potential in spherical coordinates. The terms fall off with distance as $1/r^{\ell+1}$, so that at large distances the first nonvanishing term dominates.

The multipole expansion in rectangular coordinates is also useful. Expanding $1/|\xvec-\xvec'|$ directly in powers of $\xvec'$, assuming $r'<r$, we obtain

:::{math}
:label: eq-orbamsph-81
{1\over |\xvec-\xvec'|} = {1\over r} + {\xvec'\cdot\xvec\over r^3} + {1\over 2}\sum_{ij} x'_ix'_j \Bigl({3x_ix_j - r^2\delta_{ij} \over r^5}\Bigr) + \ldots.
:::

We substitute this into {eq}`eq-orbamsph-76` and write the potential in terms of the contributions at various orders by $\Phi=\sum_\ell \Phi_\ell$. At order $\ell=0$ we have

:::{math}
:label: eq-orbamsph-82
\Phi_0(\xvec) = {q\over r},
:::

where $q$ is the zeroth moment of the charge distribution, that is, it is the total charge,

:::{math}
:label: eq-orbamsph-83
q=\int d^3\xvec' \, \rho(\xvec').
:::

At order $\ell=1$ we obtain

:::{math}
:label: eq-orbamsph-84
\Phi_1(\xvec) = {\dvec\cdot\xvec\over r^3},
:::

where $\dvec$ is the first moment of the charge distribution, that is, it is the dipole moment vector,

:::{math}
:label: eq-orbamsph-85
\dvec=\int d^3\xvec' \, \xvec' \rho(\xvec').
:::

As for the term $\ell=2$, we note first that the tensor $3x_ix_j-r^2\delta_{ij}$ which appears in {eq}`eq-orbamsph-81` is symmetric and traceless, and that it is contracted against $x'_ix'_j$ which is symmetric but not traceless. However, we can subtract the trace from $x'_ix'_j$ without changing the result, since $\delta_{ij}$ contracted against $3x_ix_j-r^2\delta_{ij}$ vanishes. This allows us to write the second order term in {eq}`eq-orbamsph-81` more symmetrically as

:::{math}
:label: eq-orbamsph-86
{1\over 6}\sum_{ij}(3x'_ix'_j-r'^2\delta_{ij}) \Bigl({3x_ix_j - r^2\delta_{ij}\over r^5}\Bigr).
:::

Then the $\ell=2$ contribution to the potential can be written as

:::{math}
:label: eq-orbamsph-87
\Phi_2(\xvec) = {1\over 6} \sum_{ij} Q_{ij} \Bigl({3x_ix_j-r^2\delta_{ij}\over r^5}\Bigr),
:::

where $Q_{ij}$ is the quadrupole moment tensor,

:::{math}
:label: eq-orbamsph-88
Q_{ij}=\int d^3\xvec' \, \rho(\xvec') (3x'_ix'_j-r^{\prime2}\delta_{ij}).
:::

Notice that $Q_{ij}$ is also symmetric and traceless. Equations~{eq}`eq-orbamsph-82`, {eq}`eq-orbamsph-84` and {eq}`eq-orbamsph-87` give the monopole, dipole and quadrupole contributions to the potential, respectively, in rectangular coordinates.

By comparing the monopole term in rectangular coordinates to that in spherical coordinates, we see that $C_{00}=q$, since $Y_{00}=1/\sqrt{4\pi}$. The dipole and quadrupole terms will be compared in {ref}`ch-wigeck`.

Finally, we note that sometimes the field point $\xvec$ is inside the charge distribution. In that case it is convenient break the region of integration into the region $r'<r$, where we expand in the ratio $r'/r$, and the region $r'>r$, where we expand in the ratio $r/r'$. The expansion is conveniently written as

:::{math}
:label: eq-orbamsph-89
{1\over |\xvec-\xvec'|} = \sum_{\ell=0}^\infty {r_<^\ell \over r_>^{\ell+1}} P_\ell(\cos\gamma) = \sum_{\ell m} {4\pi\over 2\ell+1} {r_<^\ell \over r_>^{\ell+1}} Y_{\ell m}^\cc(\theta',\phi')Y_{\ell m}(\theta,\phi),
:::

where $r_<=\min(r,r')$ and $r_>=\max(r,r')$.

(sec-orbamsph-12)=

## Orbital Angular Momentum in Multiparticle Systems

Consider now a system of $n$ spinless particles moving in three-dimensional space. The basis kets are $\ket{\xvec_1, \ldots, \xvec_n}$, and the wave functions are $\psi(\xvec_1, \ldots, \xvec_n) = \braket{\xvec_1, \ldots, \xvec_n}{\psi}$. The obvious generalization of the definition {eq}`eq-orbamsph-3` of the rotation operators $U(\Rmat)$ is

:::{math}
:label: eq-orbamsph-90
U(\Rmat)\ket{\xvec_1, \ldots, \xvec_n} = \ket{\Rmat \xvec_1, \ldots, \Rmat \xvec_n},
:::

or, in wave function language,

:::{math}
:label: eq-orbamsph-91
(\Rop \psi)(\xvec_1, \ldots, \xvec_n) = \psi(\Rmat^{-1} \xvec_1, \ldots, \Rmat^{-1} \xvec_n),
:::

as in {eq}`eq-orbamsph-13`. By considering infinitesimal rotations it is easy to work out the generator of rotations; it is

:::{math}
:label: eq-orbamsph-92
\Lvec = \sum_{i=1}^n \Lvec_i = \sum_{i=1}^n \xvec_i \cross \pvec_i.
:::

The orbital angular momentum for the entire system is the sum of the orbital angular momenta for the individual particles.

It may be of interest to rotate some of the particles and not others. For example, the operator that rotates only particle $i$ while leaving the others alone is

:::{math}
:label: eq-orbamsph-93
U_i({\hat{\mathbf{n}}},\theta) = \exp\Bigl( -{i\over \hbar} \theta {\hat{\mathbf{n}}} \cdot \Lvec_i\Bigr).
:::

Such operators are useful when the system is invariant under rotations of the individual particles (for example, in the central field approximation in atomic physics).

The standard angular momentum basis for a multiparticle system is best constructed by means of coupling of angular momenta, a topic covered in {ref}`ch-jjcouple`.

\problems

(prob-orbamsph-1)=

**Problem \prbdorbamsph-1.}  Consider wave functions $f(\theta,\phi)$ on the unit sphere, as in \secrorbamsph-5.  Using the differential operators in \secrorbamsph-4, find the simultaneous eigenfunction of $L^2$ and $L_z$ with eigenvalues $2\hbar^2$ and $\hbar$, respectively (that is, the case $\ell=1$).  Normalize this wave function but leave leave a phase factor that will be determined later.  Now apply $L_-$ twice to this state fill out the standard basis vectors in an irreducible subspace.  The wave functions are proportional to $Y_{1m}$ for $m=1,0,-1$.  By requiring $Y_{10}$ to be real and positive at the north pole, determine the phase.  Compare your answers to a table of $Y_{\ell m.** 

(prob-orbamsph-2)=

**Problem \prbdorbamsph-2..** 

\problempart{(a)} Consider a spinless particle moving in three-dimensional space. It was shown \secrorbamsph-6 that the standard angular momentum basis consists of wavefunctions of the form }$u_n(r) Y_{\ell m}(\theta,\phi)$, where $u_n(r)$ is an arbitrary basis of radial wave functions. The wave functions being referred to here are configuration space wave functions, $\psi(\xvec)$ or $\psi (r,\theta ,\phi)$. Consider the wave functions $\phi(\pvec)$ in the momentum representation. Let $(p,\beta,\alpha)$ be spherical coordinates in momentum space, that is,

:::{math}
:label: eq-orbamsph-94
\begin{aligned}
p_x &= p \sin\beta \cos\alpha, \\
p_y &= p \sin\beta \sin\alpha, \\
p_z &= p \cos\beta. \\

\end{aligned}
:::

Find the form of the wavefunctions that make up the standard angular momentum basis in momentum space.

\problempart{(b)} Let $\psi(\xvec)$ be a wave function in three dimensions, and let $\psi'(\xvec)$ be the rotated wave function corresponding to rotation matrix $\Rmat \in SO(3)$. Use {eq}`eq-orbamsph-13` and the usual expression for the momentum space wave function,

:::{math}
:label: eq-orbamsph-95
\phi(\pvec) = \int {d^3\xvec \over (2\pi\hbar)^{3/2}} \, e^{-i\pvec\cdot\xvec/\hbar} \, \psi(\xvec),
:::

to find a relation between $\phi'(\pvec)$ and $\phi(\pvec)$.

\problempart{(c)} A useful formula in scattering theory is the expansion of a plane wave in terms of free particle solutions of definite angular momentum. It is

:::{math}
:label: eq-orbamsph-96
e^{i\kvec\cdot\xvec} = \sum_{\ell=0}^\infty e^{i\ell\pi/2} \, (2\ell+1) j_\ell(kr) P_\ell(\cos\gamma),
:::

where $\gamma$ is the angle between $\xvec$ and $\kvec$, where $j_\ell$ is a spherical Bessel function, and where $P_\ell$ is a Legendre polynomial.

Suppose $\psi(\xvec) = u(r) Y_{\ell m}(\theta,\phi)$. Show that $\phi(\pvec) = v(p) Y_{\ell m}(\beta,\alpha)$, and find a one-dimensional integral transform connecting the radial functions $u(r)$ and $v(p)$.

(prob-orbamsph-3)=

**Problem \prbdorbamsph-3..** 

\problempart{(a)} Suppose unitary operators $U(\Rmat)$ on some Hilbert space satisfy the representation property, {eq}`eq-spinrot-4`. By taking matrix elements with respect to a standard angular momentum basis $\ket{jm}$, translate that condition into an equivalent condition in terms of $D$-matrices.

\problempart{(b)} Show that the addition theorem for spherical harmonics, {eq}`eq-orbamsph-71`, is a special case of the preceding result.
