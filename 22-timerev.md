---
title: "22. Time Reversal"
---
(ch-timerev)=

# 22. Time Reversal

(sec-timerev-1)=

## Introduction

We have now considered the space-time symmetries of translations, proper rotations, and spatial inversions (that is, improper rotations) and the operators that implement these symmetries on a quantum mechanical system. We now turn to the last of the space-time symmetries, namely, time reversal. As we shall see, time reversal is different from all the others, in that it is implemented by means of antiunitary transformations.

(sec-timerev-2)=

## Time Reversal in Classical Mechanics

Consider the classical motion of a single particle in three-dimensional space. Its trajectory $\xvec(t)$ is a solution of the equations of motion, $\Fvec = m\avec$. We define the time-reversed classical motion as $\xvec(-t)$. It is the motion we would see if we took a movie of the original motion and ran it backwards. Is the time-reversed motion also physically allowed (that is, does it also satisfy the classical equations of motion)?

The answer depends on the nature of the forces. Consider, for example, the motion of a charged particle of charge $q$ in a static electric field $\Evec=-\del\Phi$, for which the equations of motion are

:::{math}
:label: eq-timerev-1
m{d^2\xvec\over dt^2} = q\Evec(\xvec).
:::

If $\xvec(t)$ is a solution of these equations, then so is $\xvec(-t)$, as follows from the fact that the equations are second order in time, so that the two changes of sign coming from $t\to-t$ cancel. However, this property does not hold for magnetic forces, for which the equations of motion include first order time derivatives:

:::{math}
:label: eq-timerev-2
m{d^2\xvec\over dt^2} = {q\over c} \dod{\xvec}{t} \cross \Bvec(\xvec).
:::

In this equation, the left-hand side is invariant under $t\to-t$, while the right-hand side changes sign. For example, in a constant magnetic field, the sense of the circular motion of a charged particle (clockwise or counterclockwise) is determined by the charge of the particle, not the initial conditions, and the time-reversed motion $\xvec(-t)$ has the wrong sense. We see that motion in a given electric field is time-reversal invariant, while in a magnetic field it is not.

We must add, however, that whether a system is time-reversal invariant depends on the definition of “the system.” In the examples above, we were thinking of the system as consisting of a single charged particle, moving in given fields. But if we enlarge “the system” to include the charges that produce the fields (electric and magnetic), then we find that time-reversal invariance is restored, even in the presence of magnetic fields. This is because when we set $t \to -t$, the velocities of all the particles change sign, so the current does also. But this change does nothing to the charges of the particles, so the charge density is left invariant. Thus, the rules for transforming charges and currents under time reversal are

:::{math}
:label: eq-timerev-3
\rho \to \rho, \qquad \Jvec \to -\Jvec.
:::

But according to Maxwell's equations, this implies the transformation laws

:::{math}
:label: eq-timerev-4
\Evec \to \Evec, \qquad \Bvec \to -\Bvec,
:::

for the electromagnetic field under time reversal. With these rules, we see that time-reversal invariance is restored to {eq}`eq-timerev-2`, since there are now two changes of sign on the right hand side.

Thus we have worked out the basic transformation properties of the electromagnetic field under time reversal, and we find that electromagnetic effects are overall time-reversal invariant. We have shown this only in classical mechanics, but it is also true in quantum mechanics.

Similarly, in quantum physics we are often interested in the time-reversal invariance of a given system, such as an atom interacting with external fields. The usual point of view is to take the external fields as just given, and not to count them as part of the system. Under these circumstances the atomic system is time-reversal invariant if there are no external magnetic fields, but time-reversal invariance is broken in their presence. On the other hand, the atom generates its own, internal, magnetic fields, such as the dipole fields associated with the magnetic moments of electrons or nuclei, or the magnetic field produced by the moving charges. Since these fields are produced by charges that are a part of “the system,” however, they do not break time-reversal invariance. We summarize these facts by saying that electromagnetic effects are time-reversal invariant in isolated systems.

It turns out the same is true for the strong forces, a fact that is established experimentally. The weak forces do, however, violate time-reversal invariance (or at least CP-invariance) at a small level. We shall say more about such violations later in these notes.

(sec-timerev-3)=

## Time Reversal and the Schr\"odinger Equation

Let us consider the quantum analog of {eq}`eq-timerev-1`, that is, the motion of a charged particle in a given electric field. The Schr\"odinger equation in this case is

:::{math}
:label: eq-timerev-5
i\hbar \frac{\partial \psi(\xvec,t)}{\partial t} = \Bigl[ -{\hbar^2\over 2m} \del^2 + q\Phi(\xvec) \Bigr] \psi(\xvec,t).
:::

Suppose $\psi(\xvec,t)$ is a solution of this equation. Following what we did in the classical case, we ask if $\psi(\xvec,-t)$ is also a solution. The answer is no, for unlike the classical equations of motion {eq}`eq-timerev-1`, the Schr\"odinger equation is first order in time, so the left hand side changes sign under $t \to -t$, while the right hand side does not. If, however, we take the complex conjugate of {eq}`eq-timerev-5`, then we see that $\psi^\cc(\xvec,-t)$ is a solution of the Schr\"odinger equation, since the complex conjugation changes the sign of $i$ on the left hand side, which compensates for the change in sign from $t \to -t$.

Altogether, we see that if we define the time-reversed motion in quantum mechanics by the rule

:::{math}
:label: eq-timerev-6
\psi_r(\xvec,t) = \psi^\cc(\xvec,-t),
:::

where the $r$-subscript means “reversed,” then charged particle motion in a static electric field is time-reversal invariant. We can see already from this example that time reversal in quantum mechanics is represented by an antilinear operator, since a linear operator is unable to map a wave function into its complex conjugate.

Similarly, the quantum analog of {eq}`eq-timerev-2` is the Schr\"odinger equation for a particle in a magnetic field,

:::{math}
:label: eq-timerev-7
i\hbar\frac{\partial \psi(\xvec,t)}{\partial t} = {1\over 2m} \Bigr[ -i\hbar \del - {q\over c}\Avec(\xvec) \Bigr]^2 \psi(\xvec,t).
:::

In this case if $\psi(\xvec,t)$ is a solution, it does not follow that $\psi^\cc(\xvec,-t)$ is a solution, because of the terms that are linear in $\Avec$. These terms are purely imaginary, and change sign when we complex conjugate the Schr\"odinger equation. But $\psi^\cc(\xvec,-t)$ is a solution in the reversed magnetic field, that is, after the replacement $\Avec\to-\Avec$. This is just as in the classical case.

(sec-timerev-4)=

## The Time-Reversal Operator $\Theta$

The definition {eq}`eq-timerev-6` of the time-reversed wave function applies to a spinless particle moving in three-dimensions. We shall be interested in generalizing it to other systems, such as multiparticle systems with spin, as well as preparing the ground for generalizations to relativistic systems and quantum fields. If $\ket{\psi(t)}$ is a time-dependent state vector of a system that satisfies the Schr\"odinger equation

:::{math}
:label: eq-timerev-8
i\hbar \pop{}{t} \ket{\psi(t)} = H \ket{\psi(t)},
:::

then on analogy with {eq}`eq-timerev-6` we shall write the time-reversed state as

:::{math}
:label: eq-timerev-9
\ket{\psi_r(t)} = \Theta \ket{\psi(-t)},
:::

where $\Theta$, the *time-reversal operator*, is to be defined for different systems based on certain postulates that we shall require of it. The operator $\Theta$ by itself does not involve time, as we see from {eq}`eq-timerev-6`, where it has the effect of complex conjugating the wave function; rather, it is a mapping that takes kets into other kets. In particular, setting $t=0$ in {eq}`eq-timerev-9`,

:::{math}
:label: eq-timerev-10
\ket{\psi_r(0)} = \Theta\ket{\psi(0)},
:::

we see that $\Theta$ maps the initial conditions of the original motion into the initial conditions of the time-reversed motion.

We obtain a set of postulates for $\Theta$ as follows. First, since probabilities should be conserved under time reversal, we require

:::{math}
:label: eq-timerev-11
\Theta^\dagger \Theta = 1.
:::

Next, in classical mechanics, the initial conditions of a motion $\xvec(t)$ transform under time reversal according to $(\xvec_0,\pvec_0) \to (\xvec_0, -\pvec_0)$, so we postulate that the time-reversal operator in quantum mechanics should satisfy the conjugation relations,

:::{math}
:label: eq-timerev-12
\Theta \xvec \Theta^\hc = \xvec, \qquad \Theta \pvec \Theta^\hc = -\pvec.
:::

This should hold in systems where the operators $\xvec$ and $\pvec$ are meaningful. In such systems, these requirements imply

:::{math}
:label: eq-timerev-13
\Theta \Lvec \Theta^\hc = -\Lvec,
:::

where $\Lvec=\xvec\cross\pvec$ is the orbital angular momentum. As for spin angular momentum, we shall postulate that it transform in the same way as orbital angular momentum,

:::{math}
:label: eq-timerev-14
\Theta \Svec \Theta^\hc = -\Svec.
:::

This is plausible in view of a simple classical model of a spin, in which a particle like an electron is seen as a small charged sphere spinning on its axis. The rotation produces both an angular momentum and a magnetic moment. This model has flaws and cannot be taken very seriously, but at least it does indicate that if we reverse the motion of the charges on the sphere, both the angular momentum and the magnetic moment should reverse. Accepting both {eq}`eq-timerev-13` and {eq}`eq-timerev-14`, we see that we should have

:::{math}
:label: eq-timerev-15
\Theta \Jvec \Theta^\hc = -\Jvec,
:::

for all types of angular momentum.

(sec-timerev-5)=

## $\Theta$ Cannot Be Unitary

It turns out that the conjugation relations {eq}`eq-timerev-12` cannot be satisfied by any unitary operator. For if we take the canonical commutation relations,

:::{math}
:label: eq-timerev-16
[x_i, p_j] = i\hbar \, \delta_{ij},
:::

and conjugate with $\Theta$, we find

:::{math}
:label: eq-timerev-17
\Theta [x_i,p_j] \Theta^\hc = -[x_i,p_j] = -i\hbar\,\delta_{ij} = \Theta (i\hbar \, \delta_{ij}) \Theta^\hc.
:::

The quantity $i\hbar\,\delta_{ij}$ is just a number, so if $\Theta$ is unitary it can be brought through to cancel $\Theta^\hc$, and we obtain a contradiction. Thus, we are forced to conclude that the time-reversal operator $\Theta$ must be antilinear, so that the imaginary unit $i$ on the right-hand side of {eq}`eq-timerev-17` will change into $-i$ when $\Theta$ is pulled through it.

(sec-timerev-6)=

## Wigner's Theorem

A famous theorem proved by Wigner says that if we have a mapping of a ket space onto itself, taking, say, kets $\ket{\psi}$ and $\ket{\phi}$ into kets $\ket{\psi'}$ and $\ket{\phi'}$, such that the absolute values of all scalar products are preserved, that is, such that

:::{math}
:label: eq-timerev-18
|\braket{\psi}{\phi}| = |\braket{\psi'}{\phi'}|
:::

for all $\ket{\psi}$ and $\ket{\phi}$, then, to within inessential phase factors, the mapping must be either a linear unitary operator or an antilinear unitary operator. The reason Wigner does not demand that the scalar products themselves be preserved (only their absolute values) is that the only quantities that are physically measurable are absolute squares of scalar products. These are the probabilities that are experimentally measurable. This theorem is discussed in more detail by Messiah, *Quantum Mechanics*, in which a proof is given. (See also Steven Weinberg, *The Quantum Theory of Fields I.*) Its relevance for the discussion of symmetries in quantum mechanics is that a symmetry operation must preserve the probabilities of all experimental outcomes, and thus all symmetries must be implemented either by unitary or antiunitary operators. In fact, all symmetries except time reversal (translations, proper rotations, parity, and others as well) are implemented by unitary operators. Time reversal, however, requires antiunitary operators.

(sec-timerev-7)=

## Properties of Antilinear Operators

Since we have not encountered antilinear operators before, we now make a digression to discuss their mathematical properties. We let ${\cal E}$ be the ket space of some quantum mechanical system. In the following general discussion we denote linear operators by $L$, $L_1$, etc., and antilinear operators by $A$, $A_1$, etc. Both linear and antilinear operators are mappings of the ket space onto itself,

:::{math}
\begin{aligned}
&L:{\cal E} \to {\cal E},
\end{aligned}
:::

:::{math}
:label: eq-timerev-19
\begin{aligned}
&A:{\cal E} \to {\cal E},
\end{aligned}
:::

but they have different distributive properties when acting on linear combinations of kets:

:::{math}
:label: eq-timerev-20a
\begin{aligned}
L\bigl( c_1 \ket{\psi_1} + c_2 \ket{\psi_2} \bigr) &= c_1 \, L\ket{\psi_1} + c_2 \, L\ket{\psi_2}
\end{aligned}
:::

:::{math}
:label: eq-timerev-20b
\begin{aligned}
A\bigl( c_1 \ket{\psi_1} + c_2 \ket{\psi_2} \bigr) &= c_1^\cc \, A\ket{\psi_1} + c_2^\cc \, A\ket{\psi_2}
\end{aligned}
:::

(see {eq}`eq-hilbert-34a`. In particular, an antilinear operator does not commute with a constant, when the latter is regarded as a multiplicative operator in its own right. Rather, we have

:::{math}
:label: eq-timerev-21
\boxed{ Ac = c^\cc A.}
:::

It follows from these definitions that the product of two antilinear operators is linear, and the product of a linear with an antilinear operator is antilinear. More generally, a product of operators is either linear or antilinear, depending on whether the number of antilinear factors is even or odd, respectively.

We now have to rethink the entire Dirac bra-ket formalism, to incorporate antilinear operators. To begin, we define the action of antilinear operators on bras. We recall that a bra, by definition, is a complex-valued, linear operator on kets, that is, a mapping,

:::{math}
:label: eq-timerev-22
bra:{\cal E} \to \Complexes,
:::

and that the value of a bra acting on a ket is just the usual scalar product. Thus, if $\bra{\phi}$ is a bra, then we have

:::{math}
:label: eq-timerev-23
\bigl( \bra{\phi} \bigr) \bigl( \ket{\psi} \bigr) = \braket{\phi}{\psi}.
:::

We now suppose that an antilinear operator $A$ is given, that is, its action on kets is known, and we wish to define its action on bras. For example, if $\bra{\phi}$ is a bra, we wish to define $\bra{\phi}A$. In the case of linear operators, the definition was

:::{math}
:label: eq-timerev-24
\bigl( \bra{\phi}L \bigr) \bigl( \ket{\psi} \bigr) = \bigl( \bra{\phi} \bigr) \bigl( L\ket{\psi} \bigr).
:::

Since the positioning of the parentheses is irrelevant, it is customary to drop them, and to write simply $\matrixelement{\phi}{L}{\psi}$. In other words, we can think of $L$ as acting either to the right or to the left. However, the analogous definition for antilinear operators does not work, for if we try to write

:::{math}
:label: eq-timerev-25
\bigl( \bra{\phi}A \bigr) \bigl( \ket{\psi} \bigr) = \bigl( \bra{\phi} \bigr) \bigl( A\ket{\psi} \bigr),
:::

then $\bra{\phi}A$ is indeed a complex-valued operator acting on kets, but it is an antilinear operator, not a linear one. Bras are supposed to be linear operators. Therefore we introduce a complex conjugation to make $\bra{\phi}A$ a linear operator on kets, that is, we set

:::{math}
:label: eq-timerev-26
\boxed{ \bigl( \bra{\phi}A \bigr) \ket{\psi} = \bigl[ \bra{\phi} \bigl( A\ket{\psi} \bigr) \bigr]^\cc. }
:::

This rule is easiest to remember in words: we say that in the case of an antilinear operator, it *does* matter whether the operator acts to the right or to the left in a matrix element, and if we change the direction in which the operator acts, we must complex conjugate the matrix element. In the case of antilinear operators, parentheses are necessary to indicate which direction the operator acts. The parentheses are awkward, and the fact is that Dirac's bra-ket notation is not as convenient for antilinear operators as it is for linear ones.

Next we consider the definition of the Hermitian conjugate. We recall that in the case of linear operators, the Hermitian conjugate is defined by

:::{math}
:label: eq-timerev-27
L^\hc \ket{\psi} = \bigl( \bra{\psi} L \bigr)^\hc,
:::

for all kets $\ket{\psi}$, or equivalently by

:::{math}
:label: eq-timerev-28
\matrixelement{\phi}{L^\hc}{\psi} = \matrixelement{\psi}{L}{\phi}^\cc,
:::

for all kets $\ket{\psi}$ and $\ket{\phi}$. Here the linear operator $L$ is assumed given, and we are defining the new linear operator $L^\dagger$. The definition {eq}`eq-timerev-27` also works for antilinear operators, that is, we set

:::{math}
:label: eq-timerev-29
A^\hc \ket{\psi} = \bigl( \bra{\psi} A \bigr)^\hc.
:::

We note that by this definition, $A^\hc$ is an antilinear operator if $A$ is antilinear. Now, however, when we try to write the analog of {eq}`eq-timerev-28`, we must be careful about the parentheses. Thus, we have

:::{math}
:label: eq-timerev-30
\bra{\phi} \bigl( A^\hc \ket{\psi} \bigr) = \bigl[ \bigl( \bra{\psi} A \bigr) \ket{\phi} \bigr]^\cc.
:::

This rule is also easiest to remember in words. It is really a reconsideration of the rule stated in {ref}`sec-hilbert-13`, that the Hermitian conjugate of any product of complex numbers, kets, bras and operators is obtained by reversing the order and taking the Hermitian conjugate of all factors. This rule remains true when antilinear operators are in the mix, but the parentheses indicating the direction in which the antilinear operator acts must also be reversed at the same time that $A$ is changed into $A^\hc$ or vice versa. That is, the direction in which the antilinear operator acts is reversed.

The boxed equations~{eq}`eq-timerev-21` and {eq}`eq-timerev-26` summarize the principal rules for antilinear operators that differ from those of linear operators.

(sec-timerev-8)=

## Antiunitary Operators

We wrote down {eq}`eq-timerev-11` thinking that it would require probabilities to be preserved under $\Theta$. This would certainly be true if $\Theta$ were unitary, but since we now know $\Theta$ must be antilinear, we should think about probability conservation under antilinear transformations.

We define an *antiunitary* operator $A$ as an antilinear operator that satisfies

:::{math}
:label: eq-timerev-31
AA^\hc = A^\hc A =1.
:::

We note that the product $AA^\hc$ or $A^\hc A$ is a linear operator, so this definition is meaningful. Just like unitary operators, antiunitary operators preserve the absolute values of scalar products, as indicated by Wigner's theorem. To see this, we let $\ket{\psi}$ and $\ket{\phi}$ be arbitrary kets, and we set $\ket{\psi'}=A\ket{\psi}$, $\ket{\phi'}=A\ket{\phi}$, where $A$ is antiunitary. Then we have

:::{math}
:label: eq-timerev-32
\braket{\phi'}{\psi'} = \bigl( \bra{\phi}A^\hc \bigr) \bigl( A\ket{\psi} \bigr) = \bigl[ \bra{\phi} \bigl( A^\hc A \ket{\psi}\bigr) \bigr]^\cc = \braket{\phi}{\psi}^\cc,
:::

where we reverse the direction of $A^\hc$ in the second equality and use $A^\hc A=1$ in the third. Antiunitary operators take scalar products into their complex conjugates, and {eq}`eq-timerev-18` is satisfied. Thus, we were correct in writing down {eq}`eq-timerev-11` for probability conservation under time reversal.

(sec-timerev-9)=

## The $LK$ Decomposition

Given an antilinear operator $A$ of interest, it is often convenient to factor it into the form

:::{math}
:label: eq-timerev-33
A=LK,
:::

where $L$ is a linear operator and $K$ is a particular antilinear operator chosen for its simplicity. The idea is that $K$ takes care of the antilinearity of $A$, while $L$ takes care of the rest. The choices made for $K$ are usually of the following type.

Let $Q$ stand for a complete set of commuting observables (a single symbol $Q$ for all operators in the set). Let $n$ be the collective set of quantum numbers corresponding to $Q$, so that the basis kets in this representation are $\ket{n}$. The index $n$ can include continuous quantum numbers as well as discrete ones. Then we define a particular antilinear operator $K_Q$ by requiring, first, that $K_Q$ be antilinear, and second, that

:::{math}
:label: eq-timerev-34
K_Q \ket{n} = \ket{n}.
:::

Notice that the definition of $K_Q$ depends not only on the operators $Q$ that make up the representation, but also the phase conventions for the eigenkets $\ket{n}$. If $K_Q$ were a linear operator, {eq}`eq-timerev-34` would imply $K_Q=1$; but since $K_Q$ is antilinear, the equation $K_Q=1$ is not only not true, it is meaningless, since it equates an antilinear operator to a linear one. But {eq}`eq-timerev-34` does completely specify $K_Q$, for if $\ket{\psi}$ is an arbitrary ket, expanded according to

:::{math}
:label: eq-timerev-35
\ket{\psi} = \sum_n c_n \ket{n},
:::

then

:::{math}
:label: eq-timerev-36
K_Q\ket{\psi} = \sum_n c_n^\cc \ket{n},
:::

where we use {eq}`eq-timerev-20b` and {eq}`eq-timerev-34`. Thus, the action of $K_Q$ on an arbitrary ket is known. The effect of $K_Q$ is to bring about a complex conjugation of the expansion coefficients in the $Q$ representation. These expansion coefficients are the same as the wave function in the $Q$ representation; thus, in wave function language in the $Q$ representation, $K_Q$ just maps the wave function into its complex conjugate.

Consider, for example, the ket space for a spinless particle in three dimensions. Here we can work in the position representation, in which $Q=\xvec$ and in which the basis kets are $\ket{\xvec}$. Then we define the antilinear operator $K_{\xvec}$ by

:::{math}
:label: eq-timerev-37
K_{\xvec}\ket{\xvec} = \ket{\xvec},
:::

so that if $\ket{\psi}$ is an arbitrary ket and $\psi(\xvec)$ its wave function, then

:::{math}
:label: eq-timerev-38
K_{\xvec}\ket{\psi} = K_{\xvec} \int d^3\xvec \, \ket{\xvec}\braket{\xvec}{\psi} = K_{\xvec} \int d^3\xvec \,  \ket{\xvec}\psi(\xvec) = \int d^3\xvec \,  \ket{\xvec}\psi^\cc(\xvec).
:::

Thus, $\psi(\xvec)$ is mapped into $\psi(\xvec)^\cc$.

The operator $K_Q$ looks simple in the $Q$-representation. It may of course be expressed in other representations, but then it no longer looks so simple. For example, $K_\xvec$ is not as simple in the momentum representation as in the configuration representation (an explicit expression for $K_\xvec$ in the momentum representation will be left as an exercise).

It follows from the definition~{eq}`eq-timerev-34` that $K_Q$ satisfies

:::{math}
:label: eq-timerev-39
K_Q^2=1.
:::

(Just multiply {eq}`eq-timerev-34` by $K_Q$ and note that $K_Q^2$ is a linear operator, so that {eq}`eq-timerev-39` is meaningful.) The operator $K_Q$ also satisfies

:::{math}
:label: eq-timerev-40
K_Q=K_Q^\hc,
:::

and is therefore antiunitary. To prove this, we let $K_Q^\hc$ act on a basis ket and then insert a resolution of the identity,

:::{math}
:label: eq-timerev-41
K_Q^\hc \ket{n} = \sum_m \ket{m} \bra{m} \bigl( K_Q^\hc \ket{n} \bigr).
:::

But

:::{math}
:label: eq-timerev-42
\bra{m} \bigl( K_Q^\hc \ket{n} \bigr) = \bigl[\bigl(\bra{m}K_Q^\hc\bigr) \ket{n}\bigr]^\cc = \bra{n} \bigl(K_Q \ket{m}\bigr) = \braket{n}{m} = \delta_{nm},
:::

where in the first step we reverse the direction in which $K_Q^\hc$ acts, in the second reverse the order and conjugate all the factors to get the complex conjugate, and in the last step we use $K_Q\ket{m} = \ket{m}$. Altogether, this gives

:::{math}
:label: eq-timerev-43
K_Q^\hc \ket{n} = \ket{n}.
:::

But since $K_Q^\hc$ has the same effect on the basis kets as $K$, and since both are antilinear, they must be equal antilinear operators, $K_Q = K_Q^\hc$.

(sec-timerev-10)=

## Time Reversal in Spinless Systems

In the case of a spinless particle, we decided in \secrtimerev-3 that the time-reversal operator has the effect of complex conjugating the wave function $\psi(\xvec)$. Let us reconsider the case of spinless systems from the standpoint of the axioms that $\Theta$ is supposed to satisfy, and see if we can rederive this result. Once we have done that, we will turn to particles with spin.

In the case of a spinless particle moving in three dimensions, the ket space is $\ES = \mathspan\{\ket{\xvec}\}$ and the wave functions are $\psi(\xvec)$. The time-reversal operator $\Theta$, whatever it is, can be factored into $LK$, where $K=K_\xvec$ is the complex conjugation operator in the position representation, and where $L$ is unitary. Let us begin by finding what $K$ does to the operators $\xvec$ and $\pvec$ under conjugation. We recall from \secrtimerev-9 that $K=K^\hc=K^{-1}$. Tracking the effect of $K\xvec K^\hc$ on a wave function, we have

:::{math}
:label: eq-timerev-44
\psi(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{K^\hc}} \psi^\cc(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{\xvec}} \xvec\psi^\cc(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{K}} \xvec\psi(\xvec),
:::

or,

:::{math}
:label: eq-timerev-45
K\xvec K^\hc = \xvec.
:::

Similarly, for the momentum operator we have

:::{math}
:label: eq-timerev-46
\psi(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{K^\hc}} \psi^\cc(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{\pvec}} -i\hbar\del\psi^\cc(\xvec) \mathrel{\mathop{\\text{\rightarrowfill}}^{K}} +i\hbar\del\psi(\xvec),
:::

or,

:::{math}
:label: eq-timerev-47
K \pvec K^\hc = -\pvec.
:::

These agree with the postulates {eq}`eq-timerev-12`, and produce the right transformation law {eq}`eq-timerev-13` for orbital angular momentum. Therefore in the $LK$-decomposition of $\Theta$ we take $L=1$ and define

:::{math}
:label: eq-timerev-48
\Theta = K_\xvec,
:::

restoring the $\xvec$-subscript to $K$ for clarity. Time reversal is simply complex conjugation of the wave function in the $\xvec$-representation for a spinless particle.

This result can be easily generalized to the case of any number of spinless particles in any number of dimensions. The time-reversal operator $\Theta$ is defined as the complex conjugation operation in the configuration representation, so that its action on wave functions is given by

:::{math}
:label: eq-timerev-49
\psi(\xvec_1, \ldots, \xvec_n) \mathop{\longrightarrow}\limits^\Theta \psi^\cc(\xvec_1, \ldots, \xvec_n).
:::

This is a simple rule that covers many cases occurring in practice.

(sec-timerev-11)=

## Time Reversal and Spin

Next we consider the spin degrees of freedom of a particle of spin $s$. For simplicity we will at first ignore the spatial degrees of freedom, so the $(2s+1)$-dimensional ket space is $\ES = \mathspan\{\ket{sm}, m=-s,\ldots,s\}$. As usual, the basis kets are eigenstates of $S_z$. The postulated time-reversal operator must satisfy the conjugation relations,

:::{math}
:label: eq-timerev-50
\Theta \Svec \Theta^\hc = -\Svec.
:::

As we will show, this condition determines $\Theta$ to within a phase factor.

First we consider the operator $S_z$, which satisfies

:::{math}
:label: eq-timerev-51
\Theta S_z \Theta^\hc = -S_z.
:::

From this it easily follows that the ket $\Theta\ket{sm}$ is an eigenket of $S_z$ with eigenvalue $-m\hbar$,

:::{math}
:label: eq-timerev-52
S_z\Theta\ket{sm} = -\Theta S_z\ket{sm} =-m\hbar \Theta\ket{sm}.
:::

But since the eigenkets of $S_z$ are nondegenerate, we must have

:::{math}
:label: eq-timerev-53
\Theta\ket{sm} = c_m \ket{s,-m},
:::

where $c_m$ is a constant that presumably depends on $m$. In fact, if we square both sides of {eq}`eq-timerev-53` and use the fact that $\Theta$ is antiunitary, we will that $c_m$ is a phase factor. To find the $m$-dependence of $c_m$, we study the commutation relations of $\Theta$ with the raising and lowering operators. For example, for $S_+$, we have

:::{math}
:label: eq-timerev-54
\Theta S_+ \Theta^\hc = \Theta (S_x + iS_y) \Theta^\hc = -S_x + i S_y = -S_-,
:::

where we use {eq}`eq-timerev-15` and where a second sign reversal takes place in the $S_y$-term due to the imaginary unit $i$. There is a similar equation for $S_-$; we summarize them both by writing

:::{math}
:label: eq-timerev-55
\Theta S_\pm \Theta^\hc = -S_\mp.
:::

Now let us apply $S_+$ to the ket $\Theta\ket{sm}$, and use the commutation relations {eq}`eq-timerev-54`. We find

:::{math}
\begin{aligned}
S_+\Theta\ket{sm} &= -\Theta S_-\ket{sm} =-\hbar \sqrt{(s+m)(s-m+1)} \, \Theta \ket{s,m-1}
\end{aligned}
:::

:::{math}
\begin{aligned}
&=-\hbar \sqrt{(s+m)(s-m+1)} \, c_{m-1} \, \ket{s,-m+1} = c_m S_+\ket{s,-m}
\end{aligned}
:::

:::{math}
:label: eq-timerev-56
\begin{aligned}
&= \hbar \sqrt{(s+m)(s-m+1)} \, c_m \ket{s,-m+1},
\end{aligned}
:::

or, on cancelling the square roots,

:::{math}
:label: eq-timerev-57
\Theta\ket{s,m-1} = -c_m \ket{s,-m+1}.
:::

But by {eq}`eq-timerev-53`, this must also equal $c_{m-1}\ket{s,-m+1}$. Thus we find

:::{math}
:label: eq-timerev-58
c_{m-1} = - c_m,
:::

so $c_m$ changes by a sign every time $m$ increments or decrements by $1$.

We can summarize this result by writing

:::{math}
:label: eq-timerev-59
\Theta\ket{sm} = \eta (-1)^{s-m} \ket{s,-m},
:::

where $\eta$ is a phase that is independent of $m$. We have written the exponent of $-1$ in {eq}`eq-timerev-59` as $s-m$ because if $s$ is half-integer then so is $m$, but $s-m$ is always an integer. The main point is that the coefficient alternates in sign as $m$ increases or decreases by unit steps. We have proven our earlier assertion, that $\Theta$ is determined to within a phase by the conjugation relation {eq}`eq-timerev-50`.

Since the phase $\eta$ is independent of $m$, it can be absorbed into the definition of $\Theta$, by writing, say, $\Theta=\eta\Theta_1$, where $\Theta_1$ is a new time-reversal operator. Such an overall phase has no effect on the desired commutation relations {eq}`eq-timerev-15`, as one can easily verify, and in fact is devoid of physical significance. A common choice in practice is to choose $\eta=i^{2s}$ so that

:::{math}
:label: eq-timerev-60
\Theta \ket{sm} = i^{2m} \ket{s,-m}.
:::

This phase convention is nice because it is the obvious generalization of {eq}`eq-timerev-96`, which applies to orbital angular momentum.

(sec-timerev-12)=

## Another Approach to Time Reversal and Spin

Another approach to finding a time-reversal operator that satisfies {eq}`eq-timerev-50` is to attempt an $LK$-decomposition of $\Theta$. Since the usual basis is the $S_z$ basis, we examine the antiunitary operator $K_{S_z}$, for which we simply write $K$ in the following. We begin by conjugating $\Svec$ by $K$, finding,

:::{math}
:label: eq-timerev-61
K \begin{pmatrix}S_x \\ S_y\\ S_z \\\end{pmatrix} K^\dagger = \begin{pmatrix}S_x \\ -S_y \\ S_z \\\end{pmatrix}.
:::

The operators $S_x$ and $S_z$ did not change sign because their matrices in the standard angular momentum basis are real (see {ref}`sec-repsamos-5`), while $S_y$ does change sign since its matrix for $S_y$ is purely imaginary. We see that $\Theta$ is not equal to $K$, because the latter only changes the sign of one of the components of spin.

Nevertheless, the result can be fixed up with a unitary operator. Let $U_0$ be the spin rotation by angle $\pi$ about the $y$-axis,

:::{math}
:label: eq-timerev-62
U_0 = U({\hat{\mathbf{y}}},\pi) = e^{-i\pi S_y/\hbar}.
:::

Such a rotation leaves the $y$-component of a vector invariant, while flipping the signs of the $x$- and $z$-components. This is really an application of the adjoint formula {eq}`eq-repsamos-91`. Thus we have

:::{math}
:label: eq-timerev-63
U_0 \begin{pmatrix} S_x \\ -S_y \\ S_z \\\end{pmatrix} U_0^\dagger = \begin{pmatrix} -S_x \\ -S_y \\ -S_z \\\end{pmatrix}.
:::

Altogether, we can satisfy the requirement {eq}`eq-timerev-50` by defining

:::{math}
:label: eq-timerev-64
\Theta = e^{-i\pi S_y/\hbar}K = K e^{-i\pi S_y/\hbar},
:::

where $e^{-i\pi S_y/\hbar}$ and $K$ commute because the matrix for $e^{-i\pi S_y/\hbar}$ in the standard basis is real.

Comparing the approach of this to that in \secrtimerev-11, we see that the operator $\Theta$ defined by {eq}`eq-timerev-64` must be the same as that defined in {eq}`eq-timerev-59`, for some choice of $\eta$. In fact, with some additional trouble one can show that $\eta=1$ works (although this is not a very important fact, since $\eta$ is nonphysical anyway).

(sec-timerev-13)=

## Spatial and Spin Degrees of Freedom

Let us now include the spatial degrees of freedom, and consider the case of a spinning particle in three-dimensional space. The ket space is $\ES=\mathspan\{\ket{\xvec,m}\}$, following the notation of {eq}`eq-jjcouple-10`, and the wave functions are $\psi_m(\xvec)$, as in {eq}`eq-jjcouple-12`. In this case, the obvious definition of the time-reversal operator is the product of the two operators introduced above ($\Theta=K_{\xvec}$ for the spatial degrees of freedom, and $\Theta=K_{S_z}U_0$ for the spin degrees of freedom). That is, we take

:::{math}
:label: eq-timerev-65
\Theta=K e^{-i\pi S_y/\hbar},
:::

where now $K=K_{\xvec S_z}$ is the complex conjugation operator in the $\ket{\xvec m}$ basis, and where the rotation operator only rotates the spin (not the spatial degrees of freedom). This is the same as {eq}`eq-timerev-64`, except for a reinterpretation of the operator $K$.

For example, in the case of a spin-$\frac{1}{2}$ particle, we have $S_y = (\hbar/2) \sigma_y$, so

:::{math}
:label: eq-timerev-66
\begin{aligned}
e^{-i\pi S_y/\hbar} = e^{-i(\pi/2)\sigma_y} = \cos(\pi/2) - i\sigma_y \sin(\pi/2)= -i\sigma_y = \begin{pmatrix}0 & -1 \\ 1 & 0 \\\end{pmatrix},
\end{aligned}

:::

so a two component spinor as in {eq}`eq-jjcouple-14` transforms under time reversal according to

:::{math}
:label: eq-timerev-67
\begin{pmatrix}\psi_+(\xvec) \\ \psi_-(\xvec) \\\end{pmatrix} \mathop{\longrightarrow}\limits^\Theta \begin{pmatrix}-\psi_-^\cc(\xvec) \\ \psi_+^\cc(\xvec) \\\end{pmatrix}.
:::

More generally, for any $s$ the wave function $\psi_m(\xvec)$ transforms under time-reversal according to

:::{math}
:label: eq-timerev-68
\psi_m(\xvec) \mathop{\longrightarrow}\limits^\Theta \sum_{m'} d^s_{mm'}(\pi) \, \psi_{m'}^\cc(\xvec),
:::

where we use the reduced rotation matrices defined by {eq}`eq-repsamos-66`. Compare this to {eq}`eq-timerev-49` for a spinless particle.

Finally, to implement time reversal on a system of many spinning particles, for which the ket space is the tensor product of the ket spaces for the individual particles (both orbital and spin), we simply take $\Theta$ to be a product of operators of the form {eq}`eq-timerev-65`, one for each particle. The result is the formula {eq}`eq-timerev-65` all over again, with $K$ now interpreted as the complex conjugation in the tensor product basis,

:::{math}
:label: eq-timerev-69
\ket{\xvec_{1}m_{s1}} \otimes \ldots \otimes \ket{\xvec_{n}m_{sn}},
:::

where $n$ is the number of particles, and where the spin rotation is the product of the individual spin rotations,

:::{math}
:label: eq-timerev-70
e^{-i\pi S_y/\hbar} = e^{-i\pi S_{1y}/\hbar} \ldots e^{-i\pi S_{ny}/\hbar}.
:::

Here $S_y$ is the $y$-component of the total spin of the system,

:::{math}
:label: eq-timerev-71
S_y = S_{1y} + \ldots + S_{ny}.
:::

It may seem strange that a rotation about the $y$-axis should appear in {eq}`eq-timerev-64` or {eq}`eq-timerev-65`, since the time-reversal operator should not favor any particular direction in space. Actually, the time-reversal operator does not favor any particular direction, it is just the decomposition into the indicated unitary operator $e^{-i\pi S_y/\hbar}$ and the antiunitary complex conjugation operator $K$ which has treated the three directions in an asymmetrical manner. That is, the complex conjugation antiunitary operator $K$ is tied to the $S_z$ representation and the standard phase conventions used in angular momentum theory; since $K$ does not treat the three directions symmetrically, the remaining unitary operator $e^{-i\pi S_y/\hbar}$ cannot either. However, their product does.

Often in multiparticle systems we are interested to combine spin states of individual particles together to form eigenstates of total $S^2$ and $S_z$. This gives us a complete set of commuting observables that include the total $S^2$ and $S_z$, rather than the $S_z$'s of individual particles as in {eq}`eq-timerev-69`. But since the Clebsch-Gordan coefficients are real, the complex conjugation operator $K$ in the new basis is the same as in the old, and {eq}`eq-timerev-65` still holds.

(sec-timerev-14)=

## Examples of Hamiltonians

Let us now consider some examples of Hamiltonians that either do or do not commute with time reversal.

First, any kinetic-plus-potential Hamiltonian in three dimensions,

:::{math}
:label: eq-timerev-72
H={\pvec^2\over 2m} + V(\xvec),
:::

commutes with time reversal, because the kinetic energy is even in the momentum and the position vector is invariant. We emphasize that the potential need not be a central force potential. The motion of a charged particle in a given electrostatic field, discussed in \secrtimerev-3, is an example of such a system. More generally, kinetic-plus-potential Hamiltonians for any number of particles in any number of dimensions commute with time reversal.

The easiest way to break time-reversal invariance is to introduce a external magnetic field. Then the kinetic energy becomes

:::{math}
:label: eq-timerev-73
{1\over 2m}\Bigl[ \pvec - {q\over c} \Avec(\xvec)\Bigr]^2,
:::

which does not commute with time reversal because $\pvec$ changes sign under conjugation by $\Theta$, while $\Avec(\xvec)$ does not.

As mentioned previously, however, if the magnetic field is internally generated, then time-reversal invariance is not broken. For example, in an atom the spin-orbit interaction is the magnetic interaction between the spin of the electron and the magnetic field produced by the motion of the nucleus around the electron, as seen in the electron rest frame. It is described by a term in the Hamiltonian of the form

:::{math}
:label: eq-timerev-74
f(r) \Lvec \cdot \Svec,
:::

which according to {eq}`eq-timerev-15` is invariant under time reversal (both $\Lvec$ and $\Svec$ change sign). Similarly, spin-spin interactions such as hyperfine effects in an atom, which are proportional to $\Ivec \cdot \Svec$ ($\Ivec$ is the nuclear spin, $\Svec$ the electron spin) are invariant under time reversal. These are all examples of the invariance of electromagnetic effects under time reversal.

Are there any examples of interactions that break time-reversal invariance but that only involve internally generated fields? Yes, suppose for example that the nucleus has an electric dipole moment, call it $\muvec_e$. By the Wigner-Eckart theorem, this vector is proportional to the spin $\Svec$, so we get a term in the Hamiltonian,

:::{math}
:label: eq-timerev-75
H_int = -\muvec_e \cdot \Evec =k \Svec \cdot \Evec,
:::

where $k$ is a constant. This term is odd under time reversal, and so breaks time-reversal invariance. Time-reversal invariance is known to be respected to a very high degree of approximation, so terms of the form {eq}`eq-timerev-75`, if they are present in ordinary atoms, are very small.

There is currently considerable experimental interest in the detection of electric dipole moments of nuclei and particles such as the proton, neutron and electron, because the existence of such moments would imply a violation of time-reversal invariance and would give information about physics beyond the standard model.

(sec-timerev-15)=

## The Time-Reversed Motion

We began our discussion of time reversal by working at the classical level and asking under what conditions the time-reversed motion is also a solution of the equations of motion. Let us now address the same question in quantum mechanics, assuming for simplicity that the Hamiltonian is time-independent. We assume $\ket{\psi(t)}$ satisfies the Schr\"odinger equation, and we define the time-reversed state $\ket{\psi_r(t)}$ by {eq}`eq-timerev-9`. Does it also satisfy the Schr\"odinger equation?

To begin we just compute the time derivative of the time-reversed state,

:::{math}
:label: eq-timerev-76
i\hbar\pop{}{t} \ket{\psi_r(t)} = i\hbar\pop{}{t} \Theta \ket{\psi(-t)} = \Theta \Bigl[ -i\hbar \pop{}{t} \ket{\psi(-t)}\Bigr],
:::

where $\Theta$ changes $i$ to $-i$ when we pull it to the left. $\Theta$ commutes with $\partial/\partial t$ because $\Theta$ is a Hilbert space operator and $\partial/\partial t$ is just a derivative with respect to a parameter (time) that the state depends on. (If this is not clear, write out the time derivative as a limit in which $\Delta t\to0$.) Now let us write $\tau=-t$, so that

:::{math}
:label: eq-timerev-77
\ket{\psi_r(t)} = \Theta \ket{\psi(\tau)},
:::

and so that {eq}`eq-timerev-76` becomes

:::{math}
\begin{aligned}
i\hbar\pop{}{t} \ket{\psi_r(t)} &= \Theta \Bigl[ i\hbar \pop{}{\tau} \ket{\psi(\tau)}\Bigr] = \Theta H \ket{\psi(\tau)}
\end{aligned}
:::

:::{math}
:label: eq-timerev-78
\begin{aligned}
&= (\Theta H \Theta^\hc) \Theta\ket{\psi(\tau)} = (\Theta H \Theta^\hc) \ket{\psi_r(t)}.
\end{aligned}
:::

We see that the time-reversed state satisfies the Schr\"odinger equation with the time-reversed Hamiltonian, by which we mean $\Theta H \Theta^\hc$. We also see that the time-reversed motion satisfies the original Schr\"odinger equation if the Hamiltonian is invariant under time-reversal, that is, if

:::{math}
:label: eq-timerev-79
\Theta H \Theta^\hc = H \qquad \\textor \qquad [\Theta,H]=0.
:::

Another approach to the same result is to write a solution of the Schr\"odinger equation as

:::{math}
:label: eq-timerev-80
\ket{\psi(t)} = \exp(-itH/\hbar) \ket{\psi(0)},
:::

to which we apply $\Theta$,

:::{math}
:label: eq-timerev-81
\Theta \ket{\psi(t)} = \Theta \exp(-itH/\hbar) \Theta^\dagger \Theta \ket{\psi(0)}.
:::

The conjugated time-evolution operator can be written,

:::{math}
:label: eq-timerev-82
\Theta \exp(-itH/\hbar) \Theta^\dagger = \exp\Bigl[ \Theta (-itH/\hbar) \Theta^\dagger \Bigr] = \exp(+itH/\hbar),
:::

where we have used the antilinearity of $\Theta$ and {eq}`eq-timerev-79`. Then replacing $t$ by $-t$ and using the definition {eq}`eq-timerev-9` of $\ket{\psi_r(t)}$, we have

:::{math}
:label: eq-timerev-83
\ket{\psi_r(t)} = \exp(-itH/\hbar) \ket{\psi_r(0)}.
:::

We see that $\ket{\psi_r(t)}$ is also a solution of the time-dependent Schr\"odinger equation.

(sec-timerev-16)=

## Time Reversal and Energy Eigenstates

We have seen the effect of time reversal on the solutions of the time-dependent Schr\"odinger equation. Let us now examine the effect on the energy eigenstates.

Let $\ket{\psi}$ be an energy eigenstate for any system,

:::{math}
:label: eq-timerev-84
H\ket{\psi} = E\ket{\psi},
:::

and suppose that $[\Theta,H]=0$. Then

:::{math}
:label: eq-timerev-85
H(\Theta\ket{\psi}) = \Theta H\ket{\psi} = E(\Theta\ket{\psi}),
:::

that is, $\Theta$ maps eigenstates of $H$ into eigenstates of $H$ with the same energy. If the original eigenstate is nondegenerate, then $\Theta \ket{\psi}$ must be proportional to $\ket{\psi}$,

:::{math}
:label: eq-timerev-86
\Theta \ket{\psi} = c \ket{\psi},
:::

where $c$ is a constant. In fact, the constant is a phase factor, as we see by squaring both sides,

:::{math}
:label: eq-timerev-87
(\bra{\psi}\Theta^\dagger)(\Theta\ket{\psi}) = [\bra{\psi} (\Theta^\dagger\Theta\ket{\psi})]^\cc = \braket{\psi}{\psi}^\cc = 1 = |c|^2,
:::

where we reverse the direction of $\Theta^\hc$ in the first step and use $\Theta^\hc\Theta=1$ in the second. Thus we can write

:::{math}
:label: eq-timerev-88
\Theta\ket{\psi} = e^{i\alpha} \ket{\psi}.
:::

Now multiplying this by $e^{-i\alpha/2}$, we find

:::{math}
:label: eq-timerev-89
e^{-i\alpha/2}\Theta\ket{\psi} = \Theta e^{i\alpha/2} \ket{\psi} = e^{i\alpha/2} \ket{\psi},
:::

or, with $\ket{\phi} = e^{i\alpha/2}\ket{\psi}$,

:::{math}
:label: eq-timerev-90
\Theta\ket{\phi} = \ket{\phi}.
:::

We see that nondegenerate energy eigenstates of a Hamiltonian that is time-reversal invariant can always be chosen (by changing the overall phase, if necessary), so that the eigenstate is invariant under time reversal.

(sec-timerev-17)=

## Reality of Energy Eigenfunctions in Spinless Systems

In particular, for a spinless system in three dimensions with a kinetic-plus-potential Hamiltonian, {eq}`eq-timerev-88` implies that nondegenerate energy eigenfunctions $\psi(\xvec)$ satisfy

:::{math}
:label: eq-timerev-91
\psi^\cc(\xvec) = e^{i\alpha}\, \psi(\xvec).
:::

Now define a new wave function,

:::{math}
:label: eq-timerev-92
\phi(\xvec) = e^{i\alpha/2} \, \psi(\xvec),
:::

so that

:::{math}
:label: eq-timerev-93
\phi(\xvec) = \phi^\cc(\xvec).
:::

We see that a nondegenerate energy eigenfunction in a spinless kinetic-plus-potential system is always proportional to a real eigenfunction; the eigenfunction may be chosen to be real. We invoked the identical argument in {ref}`ch-topicsoned`, when we showed that nondegenerate energy eigenfunctions in simple one-dimensional problems can always be chosen to be real.

In the case of degeneracies, the eigenfunctions are not necessarily proportional to real eigenfunctions, but real eigenfunctions can always be constructed out of linear combinations of the degenerate eigenfunctions. We state this fact without proof, but we offer some examples. First, a free particle in one dimension has the degenerate energy eigenfunctions, $e^{ipx/\hbar}$ and $e^{-ipx/\hbar}$, both of which are intrinsically complex; but real linear combinations are $\cos(px/\hbar)$ and $\sin(px/\hbar)$.

Similarly, a spinless particle moving in a central force field in three dimensions possesses the energy eigenfunctions,

:::{math}
:label: eq-timerev-94
\psi_{n\ell m}(\xvec) = R_{n\ell}(r) Y_{\ell m}(\theta,\phi),
:::

which are degenerate since by the Wigner-Eckart theorem the energy $E_{n\ell}$ is independent of the magnetic quantum number $m$. The radial wave functions $R_{n\ell}$ can be chosen to be real, as we suppose, but the $Y_{\ell m}$'s are complex. However, in view of {eq}`eq-orbamsph-57`, we have

:::{math}
:label: eq-timerev-95
\psi_{n\ell m}^\cc(\xvec) = (-1)^m \psi_{n\ell,-m}(\xvec),
:::

or, in ket language,

:::{math}
:label: eq-timerev-96
\Theta \ket{n\ell m} = (-1)^m \ket{n\ell,-m}.
:::

In this case, real wave functions can be constructed out of linear combinations of the states $\ket{n\ell m}$ and $\ket{n\ell,-m}$. Sometimes it is convenient to ignore the radial variables and think of the Hilbert space of functions on the unit sphere, as we did in {ref}`ch-orbamsph`; then we treat $\Theta$ as the complex conjugation operator acting on such functions, and we have

:::{math}
:label: eq-timerev-97
\Theta \ket{\ell m} = (-1)^m \ket{\ell,-m},
:::

instead of {eq}`eq-timerev-96`. This is a ket version of {eq}`eq-orbamsph-57`.

(sec-timerev-18)=

## Kramers Degeneracy

{eq}`eq-timerev-65` allows us to compute the square of $\Theta$, which is used in an important theorem to be discussed momentarily. We find

:::{math}
:label: eq-timerev-98
\Theta^2 = K e^{-i\pi S_y/\hbar}K e^{-i\pi S_y/\hbar} = e^{-2\pi iS_y/\hbar},
:::

where we commute $K$ past the rotation and use $K^2=1$. The result is a total spin rotation of angle $2\pi$ about the $y$-axis. This rotation can be factored into a product of spin rotations, one for each particle, as in {eq}`eq-timerev-70`. For every boson, that is, for every particle with integer spin, the rotation by $2\pi$ is $+1$, while for every fermion, that is, for every particle of half-integer spin, the rotation by $2\pi$ is $-1$, because of the double-valued representation of the classical rotations for the case of half-integer angular momentum. Thus, the product {eq}`eq-timerev-98` is $+1$ if the system contains an even number of fermions, and $-1$ if it contains an odd number.

This result has an application. Consider an arbitrarily complex system of possibly many spinning particles, in which the Hamiltonian is invariant under time reversal. One may think, for example, of the electronic motion in a solid or a molecule. There is no assumption that the system be invariant under rotations; this would not usually be the case, for example, in the electronic motion in the molecule. Suppose such a system has a nondegenerate energy eigenstate $\ket{\psi}$ with eigenvalue $E$, as in \secrtimerev-16, so that $\ket{\psi}$ satisfies {eq}`eq-timerev-88`. Now multiplying that equation by $\Theta$, we obtain

:::{math}
:label: eq-timerev-99
\Theta^2\ket{\psi} = \Theta e^{i\alpha} \ket{\psi} = e^{-i\alpha} \Theta\ket{\psi} = \ket{\psi}.
:::

But if the system contains an odd number of fermions, then according to {eq}`eq-timerev-98` we must have $\Theta^2=-1$, which contradicts {eq}`eq-timerev-99`. Therefore the assumption of a nondegenerate energy level must be incorrect. We conclude that in time-reversal invariant systems with an odd number of fermions, the energy levels are always degenerate. This is called *Kramers degeneracy*. More generally, one can show that in such systems, the energy levels have a degeneracy that is even [see Prob.~\prbrtimerev-5(c)]. Kramers degeneracy is lifted by any effect that breaks the time-reversal invariance, notably external magnetic fields.

One example of Kramers degeneracy has appeared already, in Prob. {ref}`prob-wigeck-3`, in which it is asked to compute the energy levels of a nucleus of spin $\frac{3}{2}$ in an inhomogeneous electric field. The system consists of the nucleus, and it is not isolated, since it is interacting with the external electric field. But such interactions do not break time-reversal invariance, so the nuclear Hamiltonian (which we do not need to know explicitly) commutes with $\Theta$. But since the system has half-integer spin, all eigenstates must be degenerate. In fact, the solution of the problem shows that the four energy eigenstates fall into two degenerate pairs.

Other examples of Kramers degeneracy will be pointed out as they occur in applications studied later in the course.

(sec-timerev-19)=

## CPT Invariance and CP Violation

In relativistic quantum mechanics, it is believed that all physical fields must be Lorentz covariant and that interactions must be local. These hypotheses lead to the CPT theorem, which states that the product of charge conjugation ($C$), parity ($P$) and time reversal ($T$) is an exact symmetry of nature. We have discussed parity and time reversal but not charge conjugation, which can only be understood properly in a relativistic context. Nevertheless, the basic idea is that charge conjugation maps particles into their antiparticles, thereby changing their charge.

For a period of time after the discovery of parity violation in 1954, it was believed that although $P$ was not a good symmetry of nature, at least the product $CP$ would be a good symmetry. In 1964, however, an example of $CP$-violation was discovered in the decay of the neutral $K$-mesons. This research was carried out by Cronin and Fitch, who later received the Nobel prize for their work. If we accept the validity of the CPT~theorem, $CP$-violation implies violation of time reversal. More recently there has been extensive experimental work on the decays of the $B$-mesons, which also exhibit $CP$-violation. This work has been carried out in the BaBar experiments at SLAC, and has resulted in a better understanding of $CP$-violation in the standard model.

There is much current speculation that the observed asymmetry between matter and antimatter in the universe is due to time-reversal violating effects shortly after the big bang. The idea is that matter and antimatter were created in almost equal measure, the small difference being due to $T$ violation. Later the matter and antimatter mostly annihilated, leaving behind only a small residue of matter, which however makes up the matter we see in the universe today, including ourselves. These are just speculations, but they show the importance of time reversal and other fundamental symmetries in current physical thinking.

\problems

(prob-timerev-1)=

**Problem \prbdtimerev-1.}  This is a variation on Sakurai *Modern Quantum Mechanics.** 

\problempart{(a)* Let $U(\Rmat)$ be a rotation operator on the state space of any system (however complex). Show that $[\Theta,U(\Rmat)]=0$ for all $\Rmat$.

\problempart{(b)} Denote the basis states in a single irreducible subspace under rotations of any system by $\ket{jm}$. By considering $\Theta U(\Rmat)\ket{jm}$, show that

:::{math}
:label: eq-timerev-100
[D^j_{m'm}(\Rmat)]^\cc = (-1)^{m-m'} D^j_{-m',-m}(\Rmat).
:::

\problempart{(c)} Show that if $T^k_q$ is an irreducible tensor operator, then so is

:::{math}
:label: eq-timerev-101
S^k_q = (-1)^q \bigl( T^k_{-q} \bigr)^\hc.
:::

Operator $S^k$ is regarded as the Hermitian conjugate of $T^k$.

(prob-timerev-2)=

**Problem \prbdtimerev-2.}  This is Sakurai, *Modern Quantum Mechanics.** 

Suppose a spinless particle is bound to a fixed center by a potential $V(\xvec)$ so asymmetric that no energy level is degenerate. Using time-reversal invariance, prove

:::{math*
:label: eq-timerev-102
\xpecval{\Lvec}=0
:::

for any energy eigenstate. (This is known as *quenching* of orbital angular momentum.) If the wave function of such a nondegenerate energy eigenstate is expanded as

:::{math}
:label: eq-timerev-103
\sum_{\ell m} F_{\ell m}(r) Y_{\ell m}(\theta,\phi),
:::

what kind of phase restrictions do we obtain on $F_{\ell m}(r)$?

(prob-timerev-3)=

**Problem \prbdtimerev-3..** 

:::{math}
:label: eq-timerev-104
\Theta^2=s,
:::

where $s=+1$ for a system with an even number of fermions, and $s=-1$ for an odd number.

It was noted in {eq}`eq-timerev-32` that antiunitary operators map scalar products into their complex conjugates, so, in particular this applies to time reversal.

From this it follows that if we have an orthonormal set of vectors, $\{\ket{n}, n=1,2,\ldots\}$ with $\braket{n}{m}=\delta_{nm}$, and if we define

:::{math}
:label: eq-timerev-105
\ket{n'}=\Theta\ket{n},
:::

then

:::{math}
:label: eq-timerev-106
\braket{n'}{m'} = \delta_{nm}^\cc = \delta_{nm}.
:::

The set $\{\ket{n}\}$ need not span the whole space (it need not be a basis). Notice that this does not say whether the new basis vectors $\ket{n'}$ are linearly independent of the old ones $\ket{n}$. In summary, we can say that time reversal maps orthonormal sets into orthonormal sets.

Let $\Espace$ be the Hilbert space for a system, and let $\Sspace\subset\Espace$ be a subspace. We say that $\Sspace$ is *invariant* under $\Theta$ if for every $\ket{\psi}\in\Sspace$, $\Theta\ket{\psi}\in\Sspace$ (that is, $\Theta$ maps $\Sspace$ into itself).

\problempart{(a)} Let $H$ be a Hamiltonian that is invariant under time reversal, that is, $\Theta^\dagger H\Theta = H$. Show that the bound state energy eigenspaces of $H$ are invariant under $\Theta$.

In the following it is worthwhile keeping in mind two examples of subspaces invariant under $\Theta$, namely, the whole space ($\Sspace=\Espace$) and the energy eigenspaces of a $\Theta$-invariant Hamiltonian.

\problempart{(b)} If $\Sspace$ is invariant under $\Theta$, show that it is also invariant under $\Theta^\dagger$. (Hint: Use $\Theta^2=s$.)

\problempart{(c)} Let $\Sspace$ be invariant under $\Theta$, and let $\Aspace\subset\Sspace$ be a subspace of $\Sspace$ that is also invariant under $\Theta$. Let $\Bspace$ be the subspace of $\Sspace$ that is orthogonal to $\Aspace$, so that

:::{math}
:label: eq-timerev-107
\Sspace=\Aspace\oplus\Bspace.
:::

Show that $\Bspace$ is also invariant under $\Theta$. Hint: a vector $\ket{\psi}\in\Sspace$ lies in $\Bspace$ if it is orthogonal to all vectors $\ket{a}\in\Aspace$.

(prob-timerev-4)=

**Problem \prbdtimerev-4.} This problem continues Prob.~\prbrtimerev-3.  In this problem we consider the case of an even number of fermions, so that $s=+1$.  As in Prob.~\prbrtimerev-3, we let $\Sspace\subset\Espace$ be a $\Theta$-invariant subspace.  We assume that $\Sspace$ is not the trivial subspace $\{0\.** 

\problempart{(a)} Show that }$\Sspace$ contains a one-dimensional, invariant subspace. Hint: Let $\ket\psi\in\Sspace$ be any nonzero vector in $\Sspace$, and consider $\Theta\ket{\psi}$. Either $\ket{\psi}$ and $\Theta\ket{\psi}$ are linearly independent, or they are not. Consider the two cases.

\problempart{(b)} Assuming that $\Sspace$ is $n$-dimensional where $n\ge1$ is finite, show that

:::{math}
:label: eq-timerev-108
\Sspace=\Sspace_1\oplus \ldots \oplus \Sspace_n,
:::

where each $\Sspace_i$ is one-dimensional and the various $\Sspace_i$ are orthogonal to one another.

If $\Sspace$ is infinite-dimensional, we will assume that the decomposition {eq}`eq-timerev-108` is still valid, with $n\to\infty$. (It is obvious that we can keep on splitting off invariant, one-dimensional subspaces for as long as we want.)

\problempart{(c)} Show that a one-dimensional, $\Theta$-invariant subspace possesses a basis that is invariant under $\Theta$, that is, a vector $\ket{e}$ such that $\braket{e}{e}=1$ and $\Theta\ket{e}=\ket{e}$.

Thus, if we take $\Sspace=\Espace$, in the case $s=+1$ we have shown that the Hilbert space possesses an orthonormal basis of $\Theta$-invariant vectors; these might be used for diagonalizing a Hamiltonian. If we take $\Sspace$ to be an energy eigenspace of a $\Theta$-invariant Hamiltonian, then we have shown that a basis of orthonormal energy eigenvectors inside the eigenspace can be chosen to be invariant under $\Theta$.

\problempart{(d)} If $H$ is $\Theta$-invariant, show that its matrix elements with respect to a $\Theta$-invariant basis are real. In the usual applications this is obvious in the case of spinless particles, because the Schr\"odinger equation is real and $\Theta$-invariant basis functions are real; but it is not so trivial when the particles have spin. Diagonalizing real matrices is easier than diagonalizing complex ones.

\problempart{(e)} If we have any two orthonormal bases $\{\ket{e_n}\}$ and $\{\ket{f_n}\}$ on a subspace $\Sspace$, then these are related by an unitary transformation,

:::{math}
:label: eq-timerev-109
\ket{f_n} = \sum_m \ket{e_m}\, U_{mn},
:::

where

:::{math}
:label: eq-timerev-110
U_{mn}=\braket{e_m}{f_n}.
:::

The matrix $U_{mn}$ is unitary because

:::{math}
:label: eq-timerev-111
(UU^\dagger)_{mn} = \sum_k U_{mk} U_{nk}^\cc = \sum_k \braket{e_m}{f_k}\braket{f_k}{e_n} = \braket{e_m}{e_n}=\delta_{mn}.
:::

Similarly we show that $(U^\dagger U)_{mn}=\delta_{mn}$.

Suppose $\Sspace$ is $\Theta$-invariant as are the bases $\{\ket{e_n}\}$ and $\{\ket{f_n}\}$. Show that the matrix $U_{mn}$ defined by {eq}`eq-timerev-110` is orthogonal (that is, the matrix elements are real). Conversely, show that if $\{\ket{e_n}\}$ is $\Theta$-invariant and $U$ is real orthogonal, then $\{\ket{f_n}\}$ is $\Theta$-invariant. This is trivial, but taken together the statements show that the set of $\Theta$-invariant bases on an $N$-dimensional, $\Theta$-invariant space $\Sspace$ can be placed in one-to-one correspondence with elements of the group $O(N)$.

We see that in the case $s=+1$, a basis can always be chosen such that the matrix elements of a $\Theta$-invariant Hamiltonian are real; and such a matrix can be diagonalized by means of a real, orthogonal transformation, giving us energy eigenstates that are $\Theta$-invariant. This fact reveals the computational advantages of time-reversal invariance.

(prob-timerev-5)=

**Problem \prbdtimerev-5..** 

\problempart{(a)} Let $\Sspace$ be an invariant subspace, that is, invariant under $\Theta$, with $\dim\Sspace\ge1$. Show tht $\Sspace$ does not contain any one-dimensional, invariant subspace.

Thus, $\dim\Sspace\ge2$. If $\Sspace$ is identified with an energy eigenspace, the conclusion is the same as that regarding Kramers degeneracy in \secrtimerev-18.

\problempart{(b)} Let $\Sspace$ be a $\Theta$-invariant subspace as in part~(a), and let $\ket{\psi}$ be a nonzero vector in $\Sspace$. Also let $\ket{\phi}=\Theta\ket{\psi}$. Show that $\ket{\phi}\ne0$ and that $\braket{\phi}{\psi}=0$. Use these facts to show that $\Sspace$ possesses a two-dimensional, invariant subspace.

\problempart{(c)} Assuming that $\Sspace$ is $n$-dimensional where $n\ge1$ is finite, show that

:::{math}
:label: eq-timerev-112
\Sspace=\Sspace_1\oplus \ldots \oplus \Sspace_n,
:::

where each $\Sspace_i$ is two-dimensional and the various $\Sspace_i$ are orthogonal to one another. Thus, $n=2N$ is even.

If $\Sspace$ is infinite-dimensional, we will assume that the decomposition {eq}`eq-timerev-112` is still valid, with $n\to\infty$. (It is obvious that we can keep on splitting off invariant, two-dimensional subspaces for as long as we want.)

(prob-timerev-6)=

**Problem \prbdtimerev-6..** 

\problempart{(a)} Work out $\Theta^\dagger H \Theta$ and $\Theta^\dagger K \Theta$, where

:::{math}
:label: eq-timerev-113
H=H_0+H_{SO}.
:::

Note that $\Theta$ commutes with $\Pi$.

\problempart{(b)} Let $\{\ket{\alpha,+}, \alpha=1,2,\ldots\}$ be an orthonormal basis in the subspace ${\cal E}_+$,

:::{math}
:label: eq-timerev-114
\braket{\alpha,+}{\beta,+} = \delta_{\alpha\beta}.
:::

We do not assume it is an energy eigenbasis; it may be a basis we will use for diagonalizing the Hamiltonian. Define

:::{math}
:label: eq-timerev-115
\ket{\alpha,-}=\Theta\ket{\alpha,+}.
:::

According to {eq}`eq-timerev-106`, the set $\{\ket{\alpha,-}, \alpha=1,2,\ldots\}$ is orthonormal. Show that this set lies in the subspace ${\cal E}_-$. It is easy to show that it is actually a basis in ${\cal E}_-$; you may assume this.

\problempart{(c)} To obtain the energy eigenstates we must diagonalize the Hamiltonian. Let us look at the matrix elements of $H$ in a four-dimensional space spanned by $\ket{\alpha,\pm}$ and $\ket{\beta,\pm}$ for fixed values of $\alpha$ and $\beta$. Put the basis vector in this order: $\ket{\alpha,+}$, $\ket{\beta,+}$, $\ket{\alpha,-}$ and $\ket{\beta,-}$.

The Hamiltonian matrix is $4\times4$. Find all restrictions on the 16 matrix elements that come from the properties and relations you have worked out among the operators $H$, $K$ and $\Theta$.

Write out the matrix of the 16 matrix elements in terms of a set of real parameters $a$, $b$, $c$, etc. For example, you can write a complex number as $a+ib$, a real number as just $c$, etc.

\problempart{(d)} Find the energy eigenvalues. Does Kramers degeneracy apply? By varying the positions of the nuclei (just the $x$ and $y$ components, since they must lie in the $x$-$y$ plane) we can vary the parameters $a$, $b$, etc. How many parameters must we vary for the energy eigenvalues to be completely (four-fold) degenerate?
