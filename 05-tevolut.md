---
title: "05. Time Evolution in Quantum Mechanics"
---
(ch-tevolut)=

# 05. Time Evolution in Quantum Mechanics

(sec-tevolut-1)=

## Introduction

In these notes we develop the formalism of time evolution in quantum mechanics, continuing the quasi-axiomatic approach that we have been following in earlier notes. First we introduce the time evolution operator and define the Hamiltonian in terms of it. Then we discuss the evolution of state vectors and the Schr\"odinger equation, the evolution of observables in the Heisenberg picture and the Heisenberg equations of motion, the evolution of the density operator, and the initial value problem. Next we introduce the Hamiltonian for potential motion and discuss aspects of it, including wave function representations of the Schr\"odinger equation, the probability density and current, and the Ehrenfest relations. Finally we discuss the Schr\"odinger equation for a charged particle in a magnetic field, and discuss its transformation properties under gauge transformations.

(sec-tevolut-2)=

## The Time-Evolution Operator

Let the pure state of a system at some initial time $t_0$ be described by the state vector $\ket{\psi(t_0)}$, and let the state at some final time $t$ be described by $\ket{\psi(t)}$. We postulate that these two state vectors are related by a linear operator $U(t,t_0)$, parameterized by the two times, that is,

:::{math}
:label: eq-tevolut-1
\ket{\psi(t)} = U(t,t_0) \ket{\psi(t_0)}.
:::

We write the final time first and the initial time second in $U(t,t_0)$. This is another (the seventh) postulate of quantum mechanics, which we can add to the list in {ref}`sec-density-19`.

The operator $U(t,t_0)$ must satisfy the following three properties. First, it reduces to the identity at $t=t_0$,

:::{math}
:label: eq-tevolut-2
U(t_0,t_0) = 1.
:::

Second, it must be unitary in order to preserve probabilities,

:::{math}
:label: eq-tevolut-3
U(t,t_0)^{-1} = U(t,t_0)^\dagger.
:::

For example, the probability of finding a particle somewhere in space must be 1, and, assuming particles are neither created or destroyed, this probability must be independent of time. In relativistic interactions particles are created and destroyed, but even here we require the unitarity of $U(t,t_0)$. The logic is that if we measure some observable, the probability of getting some answer must be 1, independent of $t$. As for measuring the position of a particle in relativity theory, we will see later in the course that the position operator is not well defined in relativistic quantum mechanics, precisely because of the possibility of particle creation or destruction.

The third property says that if we evolve a system from some initial time $t_0$ to some intermediate time $t_1$, and then from $t_1$ to some final time $t_2$, we must get the same answer as evolving directly from $t_0$ to $t_2$. In other words, we can regard the state at any intermediate time as the initial conditions for the second half of the time evolution. According to this *composition* property,

:::{math}
:label: eq-tevolut-4
we have U(t_2,t_1) U(t_1,t_0) = U(t_2,t_0).
:::

(sec-tevolut-3)=

## The Hamiltonian

Now consider an infinitesimal time evolution from time $t$ to $t+\epsilon$, where $\epsilon$ is small. We expand $U(t+\epsilon,t)$ out to first order in $\epsilon$ and write the correction term as follows:

:::{math}
:label: eq-tevolut-5
U(t+\epsilon,t) = 1 -i\epsilon \Omega(t) + \ldots,
:::

where the ellipsis indicates higher order terms in $\epsilon$. Effectively, we have defined the operator $\Omega(t)$ as

:::{math}
:label: eq-tevolut-6
\Omega(t) = i\left. \pop{}{t'} U(t',t)\right|_{t'=t}.
:::

We introduce the factor of $i$ in {eq}`eq-tevolut-6` in order to make $\Omega$ Hermitian. This follows from the unitarity of $U(t,t_0)$, precisely as in the demonstration of the Hermiticity of $\khat$ in {ref}`sec-spatialdof-5`. The operator $\Omega$ depends on $t$ in general because the right-hand side of {eq}`eq-tevolut-6` does so.

The operator $\Omega(t)$ can be regarded as the *generator* of time translations in quantum mechanics, because it gives the small correction needed to advance a state from time $t$ to $t+\epsilon$. Evolution over a finite time interval can be regarded as the result of a large number of small displacements in time, so knowing $\Omega(t)$ in principle allows us to evolve the system over any time interval. Since it is Hermitian, $\Omega(t)$ presumably corresponds to something we can observe.

The classical Hamiltonian $H$ is considered the generator of time translations in classical mechanics. This means that for small time increments we can calculate the correction in $q$ or $p$ or any other classical observable by forming the Poisson bracket with $H$. To see this explicitly, let $f(x,p)$ be a classical observable (for a particle moving in one dimension, for simplicity), which acquires a time dependence because $x$ and $p$ evolve in time as a particle moves along its orbit. Then, working to first order in a small time increment $\epsilon$, we have

:::{math}
:label: eq-tevolut-7
\begin{aligned}
f(t+\epsilon) &= f(t) + \epsilon\dod{f}{t} = f(t) +\epsilon\Bigl(\xdot \frac{\partial f}{\partial x} + \pdot \frac{\partial f}{\partial p}\Bigr) \\
&= f(t)+\epsilon\Bigl(\frac{\partial H}{\partial p}\frac{\partial f}{\partial x} -\frac{\partial H}{\partial x}\frac{\partial f}{\partial p}\Bigr) =f(t) -\epsilon\{H,f\}, \\

\end{aligned}
:::

where we use Hamilton's equations, {eq}`eq-classmech-78`, and the definition of the Poisson bracket, {eq}`eq-classmech-100`. This should be compared to {eq}`eq-spatialdof-64`, which shows the analogous role of the momentum in classical mechanics as the generator of translations.

Because of the role of the classical Hamiltonian as the generator of time translations, we guess that $\Omega(t)$ is closely related to the operator that we should define as the *quantum Hamiltonian*, denoted by $\Hhat$ (with a hat to distinguish it from the classical Hamiltonian $H$). We cannot have $\Omega=\Hhat$ because $\Omega$ has units of inverse time, while $\Hhat$ has units of energy. We fix this by defining

:::{math}
:label: eq-tevolut-8
\Hhat(t) = \hbar \Omega(t).
:::

With this definition, the infinitesimal time evolution {eq}`eq-tevolut-5` becomes

:::{math}
:label: eq-tevolut-9
U(t+\epsilon,t) = 1-{i\epsilon\over\hbar} \Hhat(t) + \ldots.
:::

We remark that Hamiltonians in classical mechanics depend on time when there are time-dependent forces or fields present. See the discussion in {ref}`sec-classmech-20`. For example, the motion of a charged particle in an electromagnetic wave is described by a time-dependent Hamiltonian. We expect the same to be true in quantum mechanics, so $\Hhat$ depends on $t$, in general. As in classical mechanics, however, time-independent Hamiltonians are an important special case, and offer some simplifications.

Our presentation leads to the question of whether the $\hbar$ in {eq}`eq-tevolut-8` is the same as in {eq}`eq-spatialdof-65`, ${\hat{\mathbf{p}}}=\hbar{\hat{\mathbf{k}}}$. See {ref}`sec-spatialdof-12` for an overview of the history of the relations $E=\hbar\omega$ and $\pvec=\hbar\kvec$. Here we simply note that these relations are obviously the space- and time-components of a single 4-vector, in which energy and momentum are generators of displacements in time and space, respectively. Relativistic covariance requires that the $\hbar$'s in these relations be the same. We are only concerning ourselves with the nonrelativistic theory at this point, but it is obvious that relativistic covariance will be impossible to establish if these $\hbar$'s are different.

(sec-tevolut-4)=

## Differential Equations for Time Evolution

To obtain a differential equation for $U(t,t_0)$ we take the derivative with respect to the final time $t$, using the definition of the derivative:

:::{math}
:label: eq-tevolut-10
\frac{\partial U(t,t_0)}{\partial t} = \lim_{\epsilon\to0} {U(t+\epsilon,t_0) - U(t,t_0) \over \epsilon}.
:::

But by the composition property {eq}`eq-tevolut-4`, we can write

:::{math}
:label: eq-tevolut-11
U(t+\epsilon,t_0) = U(t+\epsilon,t) U(t,t_0),
:::

so the operator $U(t,t_0)$ can be factored out to the right in {eq}`eq-tevolut-10`, giving

:::{math}
:label: eq-tevolut-12
\frac{\partial U(t,t_0)}{\partial t} = \left[\lim_{\epsilon\to0} {U(t+\epsilon,t)-1 \over \epsilon}\right] U(t,t_0).
:::

The remaining limit is $\partial U(t',t)/\partial t'|_{t'=t}$, which by {eq}`eq-tevolut-6` and {eq}`eq-tevolut-8` is $-i\Omega(t) = -i\Hhat(t)/\hbar$. Altogether, {eq}`eq-tevolut-12` becomes

:::{math}
:label: eq-tevolut-13
\boxed{ i\hbar \frac{\partial U(t,t_0)}{\partial t} = \Hhat(t)U(t,t_0).}
:::

This differential equation is subject to the initial conditions {eq}`eq-tevolut-2`. In practice $\Hhat(t)$ is usually a given operator as a function of time and we wish to solve for $U(t,t_0)$. With the given initial conditions, the solution is unique.

Now differentiating {eq}`eq-tevolut-1` with respect to $t$ and using {eq}`eq-tevolut-13`, we obtain a differential equation for the state vector $\ket{\psi(t)}$,

:::{math}
:label: eq-tevolut-14
\boxed{ i\hbar \pop{}{t} \ket{\psi(t)} = \Hhat(t) \ket{\psi(t)},}
:::

which is subject to the given initial condition $\ket{\psi(t_0)}$ for the state vector. This is the *Schr\"odinger equation*. This is a ket equation that differs only trivially from the operator equation {eq}`eq-tevolut-13`.

The case that the Hamiltonian is independent of time, $\partial \Hhat(t)/\partial t=0$, is important in practice. In this case, {eq}`eq-tevolut-13` has the solution,

:::{math}
:label: eq-tevolut-15
U(t,t_0) = \exp[-i\Hhat(t-t_0)/\hbar],
:::

showing that $U(t,t_0)$ only depends on the elapsed time $t-t_0$ when $\Hhat$ is independent of $t$. Writing simply $t$ for the elapsed time (or choosing $t_0=0$), we have

:::{math}
:label: eq-tevolut-16
U(t) = e^{-i\Hhat t/\hbar}.
:::

In this case, $\Hhat$ commutes with $U(t)$.

In the general case in which $\Hhat$ depends on time, there is no simple solution for $U(t,t_0)$. In this case $\Hhat(t)$ does not commute with $U(t,t_0)$, nor for that matter does it usually commute with itself at different times.

(sec-tevolut-5)=

## The Heisenberg Picture

The time evolution of a classical observable along an orbit is given by {eq}`eq-classmech-98` or {eq}`eq-classmech-101`. In quantum mechanics we see a closer analogy with classical mechanics if we allow observables to evolve in time. Up to this point in our discussion of time evolution in quantum mechanics we have used the *Schr\"odinger picture*, in which kets evolve according to the Schr\"odinger equation {eq}`eq-tevolut-14`, and operators do not evolve (unless they have an explicit time dependence, in which case their only evolution is due to this time dependence). We shall continue to use the Schr\"odinger picture for most of this course, but there are certain problems and topics that are best handled in the *Heisenberg picture*, in which kets do not evolve in time but operators do. We shall now explain these two pictures and the relation between them.

In the following we drop the hats on $H$, it being understood that we are speaking of the quantum Hamiltonian.

The Schr\"odinger and Heisenberg pictures differ by a time-dependent, unitary transformation. In the following we shall put an $S$ subscript on kets and operators in the Schr\"odinger picture and an $H$ subscript on them in the Heisenberg picture. If a ket or an operator appears without a subscript, the Schr\"odinger picture is assumed. If $\ket{\psi_S(t)} = \ket{\psi(t)}$ is the time-dependent state vector in the Schr\"odinger picture, then the state vector in the Heisenberg picture is defined by

:::{math}
:label: eq-tevolut-17
\ket{\psi_H} = U(t,t_0)^\dagger \ket{\psi_S(t)}.
:::

By {eq}`eq-tevolut-1` and {eq}`eq-tevolut-3`, this is equivalent to

:::{math}
:label: eq-tevolut-18
\ket{\psi_H} = \ket{\psi_S(t_0)},
:::

where $t_0$ is the initial time. The state vector in the Heisenberg picture does not evolve because it is equal to the ket in the Schr\"odinger picture at the initial time $t_0$. As for operators, if $A_S(t) = A(t)$ is an operator in the Schr\"odinger picture, which for generality we allow to have an explicit time dependence, then the corresponding operator in the Heisenberg picture is

:::{math}
:label: eq-tevolut-19
A_H(t) = U(t,t_0)^\dagger A_S(t) U(t,t_0).
:::

The Heisenberg operator $A_H(t)$ has a time dependence for two reasons, first because the Schr\"odinger operator $A_S(t)$ may have an (explicit) time dependence, and second because the operators $U(t,t_0)$ and $U(t,t_0)^\dagger$ depend on time, what we regard as the implicit time dependence. Notice that the Heisenberg operator depends on time even if the Schr\"odinger operator does not (because of the implicit time dependence). See {ref}`sec-classmech-20` for a discussion of explicit and implicit time dependence in classical observables.

There is no evolution equation for $\ket{\psi_H}$ in the Heisenberg picture, but the operators obey an evolution equation obtained by taking the derivative of the definition {eq}`eq-tevolut-19` and using {eq}`eq-tevolut-13`. This gives

:::{math}
:label: eq-tevolut-20
i\hbar \dod{A_H}{t} = -U^\dagger H A_S U + U^\dagger A_S H U + i\hbar U^\dagger \frac{\partial A_S}{\partial t} U,
:::

where $H=H_S$ is the Hamiltonian in the Schr\"odinger picture, which may be time dependent. But by inserting the product $UU^\dagger$ between $A_S$ and $H$ in the first two terms above, the result can be written purely in terms of operators in the Heisenberg picture,

:::{math}
:label: eq-tevolut-21
i\hbar \dod{A_H}{t} = [A_H,H_H] + i\hbar \left( \frac{\partial A}{\partial t} \right)_H,
:::

where the last term means, differentiate $A$ with respect to its explicit time dependence in the Schr\"odinger picture, then convert to the Heisenberg picture. This may also be written

:::{math}
:label: eq-tevolut-22
\dod{A_H}{t} = -{i\over\hbar} [A_H,H_H] +\left( \frac{\partial A}{\partial t} \right)_H,
:::

whereupon the analogy with the classical equation {eq}`eq-classmech-101` is more striking. Equations~{eq}`eq-tevolut-21` or {eq}`eq-tevolut-22` are the Heisenberg equations of motion for operators.

(sec-tevolut-6)=

## Algebraic Relations Same in Both Pictures

Suppose we have an operator $A_S$ in the Schr\"odinger picture, so that in the Heisenberg picture it is $A_H=U^\dagger A_S U$, where $U=U(t,t_0)$. Then if $B_S=f(A_S)$ for some function $f$, it turns out that

:::{math}
:label: eq-tevolut-23
B_H = U^\dagger f(A_S)U = f(U^\dagger A_S U)=f(A_H).
:::

This is easy to see in the case that $f$ is a polynomial or power series, for example, if $B_S=A_S^2$ we have

:::{math}
:label: eq-tevolut-24
B_H = U^\dagger A_S A_S U = U^\dagger A_S U U^\dagger A_S U = A_H^2,
:::

but the result can be proved more generally by using the definition of a function of an operator given in {ref}`sec-hilbert-25`. Likewise, suppose we have an algebraic relation in the Schr\"odinger picture such as $C_S=A_S B_S$, where $A_S$ and $B_S$ need not commute. Then it is easy to show that $C_H=A_HB_H$. In other words, algebraic relations among operators in the Schr\"odinger picture are converted into the corresponding algebraic relations in the Heisenberg picture simply by replacing the $S$ subscripts with $H$'s.

In particular, commutation relations have the same form in both pictures. If $C_S = [A_S,B_S]$, then $C_H = [A_H, B_H]$. Also, if $V(\xvec_S)$ is a potential energy in the Schr\"odinger picture, then

:::{math}
:label: eq-tevolut-25
U^\dagger V(\xvec_S) U = V(\xvec_H)
:::

is the potential energy in the Heisenberg picture. This means that the Hamiltonian has the same form in both pictures, for example, if

:::{math}
:label: eq-tevolut-26
H_S = {\pvec_S^2 \over 2m} + V(\xvec_S),
:::

then

:::{math}
:label: eq-tevolut-27
H_H = {\pvec_H^2\over 2m} + V(\xvec_H).
:::

(sec-tevolut-7)=

## The Heisenberg and Schr\"odinger Pictures are Physically Equivalent

All measurable quantities in quantum mechanics can be expressed in terms of matrix elements of the form $\matrixelement{\phi}{A}{\psi}$. These, however, are the same in both the Heisenberg and Schr\"odinger pictures,

:::{math}
:label: eq-tevolut-28
\matrixelement{\phi_S(t)}{A_S}{\psi_S(t)} = \matrixelement{\phi_H}{A_H(t)}{\psi_H},
:::

since the unitary operators cancel when {eq}`eq-tevolut-17` and {eq}`eq-tevolut-19` are substituted. Thus, if we can find the time evolution of operators in the Heisenberg picture, we can predict the outcome of all experiments equally well as by finding the time evolution of the state vector in the Schr\"odinger picture. For some problems, the Heisenberg picture is easier to use (the harmonic oscillator, for example). In addition, the Heisenberg picture is needed in relativistic quantum field theory to establish manifest Lorentz covariance. Although most of nonrelativistic quantum mechanics is usually carried out in the Schr\"odinger picture (and also in this course), it can be argued that the Heisenberg picture is more fundamental.

In the special case that the Schr\"odinger Hamiltonian is independent of time, the operator $U(t,t_0)=U(t-t_0)$ is a function of $H$ and so commutes with it, according to {eq}`eq-tevolut-16`. Thus, in this case, the Schr\"odinger and Heisenberg Hamiltonians are the same,

:::{math}
:label: eq-tevolut-29
H_H = U(t)^\dagger H_S U(t) = H_S,
:::

where we have set $t_0=0$ as in {eq}`eq-tevolut-16`.

There are other pictures besides the Schr\"odinger and Heisenberg pictures. In the interaction picture, which we will take up in {ref}`ch-tdpt`, the time dependence due to some unperturbed Hamiltonian $H_0$ is stripped off from the kets and transferred to the operators. But the time dependence remaining from some perturbation $H_1$ is left on the kets. Thus, the interaction picture is intermediate between the Schr\"odinger and Heisenberg pictures. It is especially useful in time-dependent perturbation theory and scattering theory.

(sec-tevolut-8)=

## Time Evolution of the Density Operator

{eq}`eq-tevolut-14`, the Schr\"odinger equation, gives the time evolution of the state vector in quantum mechanics. As we have seen in {ref}`ch-density`, however, the state of a quantum system is described in general by a density operator, not a state vector. Therefore we require an equation of evolution for the density operator. We work here in the Schr\"odinger picture, and consider the density operator for a discrete ensemble of pure states $\ket{\psi_i}$ with statistical weights $f_i$, as in {eq}`eq-density-16`. The density operator $\hat\rho$ is a function of time because the states $\ket{\psi_i}$ are functions of time. We put a hat on $\hat\rho$ to distinguish it from the classical density $\rho$ discussed in {ref}`sec-classmech-24`.

At the initial time $t_0$ the density operator is given by

:::{math}
:label: eq-tevolut-30
{\hat\rho}(t_0) = \sum_i f_i \ketbra{\psi_i(t_0)}{\psi_i(t_0)},
:::

while at the final time it is

:::{math}
:label: eq-tevolut-31
\begin{aligned}
{\hat\rho}(t) &= \sum_i f_i \ketbra{\psi_i(t)}{\psi_i(t)} = U(t,t_0) \left( \sum_i f_i \ketbra{\psi_i(t_0)}{\psi_i(t_0)} \right) U(t,t_0)^\dagger \\
&= U(t,t_0) {\hat\rho}(t_0) U(t,t_0)^\dagger. \\

\end{aligned}
:::

Differentiating this last expression with respect to time and using {eq}`eq-tevolut-13`, we find

:::{math}
:label: eq-tevolut-32
i\hbar \pop{{\hat\rho}}{t} = [\Hhat,{\hat\rho}].
:::

This equation replaces the Schr\"odinger equation when we have mixed states. By a slight change {eq}`eq-tevolut-32` can be written

:::{math}
:label: eq-tevolut-33
\pop{{\hat\rho}}{t} -{i\over\hbar}[{\hat\rho},\Hhat] =0,
:::

whereupon the analogy with the classical Liouville equation {eq}`eq-classmech-112` is more clear. {eq}`eq-tevolut-32` looks similar to the Heisenberg equation of motion for some observable, {eq}`eq-tevolut-22`, but they are not the same since we are working here in the Schr\"odinger picture.

(sec-tevolut-9)=

## Commutators and Poisson Brackets

Comparing the quantum equations {eq}`eq-tevolut-22` and {eq}`eq-tevolut-33` with their classical counterparts {eq}`eq-classmech-101` and {eq}`eq-classmech-112`, respectively, we see that one goes into the other if we map commutators into Poisson brackets according to the rule,

:::{math}
:label: eq-tevolut-34
[A,B] \to i\hbar \{A,B\}.
:::

This association was first noticed by Dirac, and it helped him to establish the formal structure of quantum mechanics on the classical model. In important cases it is an exact correspondence, that is, quantum commutators are the same as classical Poisson brackets, apart from the factor $i\hbar$ and a reinterpretation of the symbols as operators (quantum observables) instead of classical observables. Compare, for example, the classical canonical Poisson bracket relations {eq}`eq-classmech-108` with the Heisenberg-Born commutation relations {eq}`eq-spatialdof-69a`. Another example is the classical Poisson bracket relations for the components of orbital angular momentum, $\Lvec=\xvec\cross\pvec$,

:::{math}
:label: eq-tevolut-35
\{L_i, L_j\} = \epsilon_{ijk}\,L_k,
:::

which may be compared to the quantum commutation relations for the components of the angular momentum operator,

:::{math}
:label: eq-tevolut-36
[L_i, L_j] = i\hbar \, \epsilon_{ijk}\, L_k.
:::

In other cases, Dirac's correspondence {eq}`eq-tevolut-34` is only approximate.

(sec-tevolut-10)=

## Constants of Motion

In classical mechanics, an observable $A=A(q,p)$ is a *constant of motion* if its value is constant as $q$ and $p$ evolve along an orbit. For simplicity in this we only speak of observables without an explicit time dependence, and we assume that the Hamiltonian, too, has no explicit time dependence. But according to {eq}`eq-classmech-101`, this means that $A$ has vanishing Poisson bracket with the Hamiltonian, $\{A,H\}=0$.

Similarly, in quantum mechanics, we say that an observable $A$ without an explicit time dependence is a *constant of motion* if it commutes with the Hamiltonian, $[A,H]=0$. Then the Heisenberg equations of motion {eq}`eq-tevolut-21` imply

:::{math}
:label: eq-tevolut-37
\dod{A_H}{t}=0.
:::

This in turn implies that the expectation value of $A$ with respect to any state is constant in time,

:::{math}
:label: eq-tevolut-38
\dod{}{t}\xpecval{A} =0,
:::

where, as we have seen, the expectation value can be computed in either picture (Schr\"odinger or Heisenberg).

Energy eigenstates in many practical problems are expressed as simultaneous eigenstates of a complete set of commuting observables, of which the Hamiltonian is one. For example, in central force motion we often use $(H,L^2,L_z)$. But since the other observables in the list, besides the Hamiltonian, all commute with the Hamiltonian, they are all constants of motion, and their expectation values with respect to arbitrary states are independent of time. And since the Hamiltonian commutes with itself, it is also a constant of motion.

(sec-tevolut-11)=

## The Initial Value Problem for Time-Independent Hamiltonians

The initial value problem refers to the problem of finding the final state $\ket{\psi(t)}$ at some time $t$, given the initial state $\ket{\psi(t_0)}$ at some initial time $t_0$. When the Hamiltonian is time-independent, it is possible to give an explicit solution to the initial value problem in terms of the eigenstates and eigenvalues of the Hamiltonian.

Suppose $H$ in {eq}`eq-tevolut-14` is time-independent. Let us denote its eigenstates by $\ket{n}$ and corresponding eigenvalues by $E_n$, so that

:::{math}
:label: eq-tevolut-39
H\ket{n} = E_n \ket{n},
:::

where $n$ can stand for one or more quantum numbers needed to specify an energy eigenstate. For simplicity we assume the index $n$ is discrete, but the formulas are easily extended to handle a continuous or mixed spectrum. Let us expand the time-dependent state $\ket{\psi(t)}$ in terms of the energy eigenstates,

:::{math}
:label: eq-tevolut-40
\ket{\psi(t)} = \sum_n c_n(t) \ket{n},
:::

where the expansion coefficients $c_n$ depend on time. Then by substituting {eq}`eq-tevolut-40` into {eq}`eq-tevolut-14`, we find

:::{math}
:label: eq-tevolut-41
i\hbar {\dot c}_n = E_n c_n,
:::

or,

:::{math}
:label: eq-tevolut-42
c_n(t) = e^{-iE_n t/\hbar} \, c_n(0).
:::

Thus we have

:::{math}
:label: eq-tevolut-43
\ket{\psi(t)} = \sum_n e^{-iE_n t/\hbar} c_n(0) \ket{n},
:::

where

:::{math}
:label: eq-tevolut-44
c_n(0) = \braket{n}{\psi(0)}.
:::

These results are equivalent to expanding the time-evolution operator in energy eigenstates,

:::{math}
:label: eq-tevolut-45
U(t) = e^{-iHt/\hbar} = \sum_n e^{-iE_nt/\hbar} \, \ketbra{n}{n}.
:::

This is a special case of a function of an observable expressed in terms of the projectors of that observable, as described in {ref}`sec-hilbert-25`.

Often the easiest way to solve the initial value problem in quantum mechanics is first to find the eigenfunctions of the Hamiltonian, then to compute the expansion coefficients of $\ket{\psi}$ at $t=0$ by {eq}`eq-tevolut-44`, and finally to sum the series {eq}`eq-tevolut-43`. This only works for time-independent Hamiltonians, however.

In particular, if the system is known to be in an energy eigenstate at $t=0$, then it stays in this state forever. The only thing that changes in time is the overall phase of the state, $e^{-iE_nt/\hbar}$. For this reason an energy eigenstate is also called a *stationary state*.

(sec-tevolut-12)=

## Hamiltonian for Potential Motion

So far we have defined the Hamiltonian operator as the generator of time evolution, but we have not said what the Hamiltonian actually is in any specific case. The simplest case is that of a particle of mass $m$ moving in a potential $V(\xvec,t)$, which for generality we allow to depend on time. See {ref}`sec-classmech-8` for the physical meaning of time-dependent potentials, including an example. See also See. {ref}`sec-classmech-20` for a discussion of time-dependent Hamiltonians. In practice, the potential is often time-independent. The classical equations of motion are

:::{math}
:label: eq-tevolut-46
m \avec = -\del V(\xvec,t),
:::

where $\avec=\ddot\xvec$. The classical Hamiltonian is a single-particle version of {eq}`eq-classmech-83`,

:::{math}
:label: eq-tevolut-47
H= {\pvec^2\over 2m} + V(\xvec,t).
:::

To obtain the quantum Hamiltonian, we take this formula and reinterpret the classical observables $\xvec$ and $\pvec$ as operators acting on the ket space spanned by the position eigenkets $\ket{\xvec}$, as in {ref}`ch-spatialdof`. This space is isomorphic to the space of wave functions $\psi(\xvec)$. The operators $\xvec$ and $\pvec$ satisfy the Heisenberg-Born commutation relations {eq}`eq-spatialdof-69a`. As in classical mechanics, the Hamiltonian {eq}`eq-tevolut-47` is the sum of the kinetic and the potential energies.

Quantum mechanics must go over to classical mechanics in the limit in which $\hbar$ is small, that is, when all actions of a problem are large in comparison to $\hbar$. So it is an educated guess that we can adopt a classical Hamiltonian in this manner, reinterpret it, and get the correct quantum Hamiltonian. Ultimately, the success of our guess must be verified by comparison with experiment, or comparison with a more fundamental theory that we trust. And of course we trust fundamental theories when they have been verified by experiment. There is no process of logical deduction to obtain quantum mechanics from classical mechanics, since new physics is involved.

The potentials $V$ that are used in practice are often phenomenological models that represent guesses or hopes that some complicated physics can be represented by a potential. For example, we may try to represent the interaction of two atoms, or of a proton and a neutron, by a potential. Actually, atoms and nucleons are composite particles with internal structure, and their interactions can only be represented by a potential in an approximate manner.

A large part of atomic, molecular and condensed matter physics can be understood in terms of the electrostatic interactions of charged particles. These are described by the potential {eq}`eq-classmech-24`, which can be regarded as “fundamental.” But effects involving spin, magnetic fields, relativistic corrections, the emission and absorption of radiation and other phenomena require other types of Hamiltonians. We will consider magnetic fields below in \secrtevolut-17, and the other generalizations will be taken up later in the course.

The multiparticle generalization of {eq}`eq-tevolut-47` is straightforward. Let there be $N$ particles with masses $m_i$, positions $\xvec_i$ and momenta $\pvec_i$, and assume that they interact by means of a potential. Then the classical Hamiltonian is

:::{math}
:label: eq-tevolut-48
H=\sum_{i=1}^N {\pvec_i^2 \over 2m_i} + V(\xvec_1, \ldots, \xvec_N).
:::

In a multiparticle system, the wave function is $\psi(\xvec_1, \ldots, \xvec_N,t)$. It is a function defined over the multidimensional configuration space (see \classmech.3).

(sec-tevolut-13)=

## Representations of the Schr\"odinger Equation

The Hamiltonian {eq}`eq-tevolut-47` is presented in terms of operators $\xvec$ and $\pvec$. We will not put hats on these operators as we did in {ref}`ch-spatialdof`, since it will usually be clear from context whether a quantum operator is intended and or a $c$-number. These operators are represented in different ways in different representations, as discussed in Secs. {ref}`sec-spatialdof-13` and {ref}`sec-spatialdof-14` (see {ref}`tbl-spatialdof-1`). We now translate the ket version of the Schr\"odinger equation, {eq}`eq-tevolut-14`, into its configuration space representation, using the Hamiltonian {eq}`eq-tevolut-47`. We write $\psi(\xvec,t) =\braket {\xvec} {\psi(t)}$. Then using {eq}`eq-spatialdof-20` and {eq}`eq-spatialdof-71` or {ref}`tbl-spatialdof-1` for the actions of $\xvec$ and $\pvec$ on configuration space wave functions, we obtain

:::{math}
:label: eq-tevolut-49
-{\hbar^2\over 2m} \del^2 \psi(\xvec,t) +V(\xvec,t) \psi(\xvec,t) = i\hbar\frac{\partial \psi(\xvec,t)}{\partial t}.
:::

If the potential is independent of time, then we often wish to find the energy eigenfunctions of the Hamiltonian, call them $\psi_n(\xvec) = \braket{\xvec}{n}$ where $\ket{n}$ are the energy eigenkets as in {eq}`eq-tevolut-39`. These satisfy

:::{math}
:label: eq-tevolut-50
\Bigl[-{\hbar^2 \over 2m}\del^2 + V(\xvec)\Bigr] \psi_n(\xvec) = E_n \psi_n(\xvec),
:::

which is the configuration space representation of {eq}`eq-tevolut-39`. Equations {eq}`eq-tevolut-49` and {eq}`eq-tevolut-50` are the time-dependent and time-independent versions, respectively, of the Schr\"odinger equation in configuration space, for a single particle moving in a given potential.

We can also write down the Schr\"odinger equation in momentum space. In the time-independent version, it is

:::{math}
:label: eq-tevolut-51
{p^2\over 2m} \phi_n(\pvec) + \int d^3\pvec' \, {\tilde V}(\pvec-\pvec')\phi_n(\pvec') = E_n\phi_n(\pvec),
:::

where $\phi_n(\pvec) = \braket{\pvec}{n}$ and where

:::{math}
:label: eq-tevolut-52
{\tilde V}(\pvec) = \int {d^3\xvec \over (2\pi\hbar)^3} \, e^{-i\pvec\cdot\xvec/\hbar} \, V(\xvec).
:::

The first term on the left of {eq}`eq-tevolut-51` (the kinetic energy) is a multiplicative operator in momentum space, which is simpler than the differential operator (the Laplacian) that occurs in configuration space. The potential, on the other hand, has become an integral operator. The momentum space version of the Schr\"odinger equation is useful for some problems, notably the hydrogen atom.

(sec-tevolut-14)=

## The Probability Density and Current

Let us consider a single particle moving in three-dimensional space under the influence of a potential $V$, as described by the Hamiltonian {eq}`eq-tevolut-40`. The potential may be time-dependent. Let us write

:::{math}
:label: eq-tevolut-53
\rho(\xvec,t) = |\psi(\xvec,t)|^2
:::

for the probability density on configuration space (not to be confused with the density operator). The probability density changes in time, in general, but the integral over all space,

:::{math}
:label: eq-tevolut-54
\int d^3\xvec\, \rho(\xvec,t) = \int d^3\xvec\, |\psi(\xvec,t)|^2 = \int d^3\xvec\, \braket{\psi(t)}{\xvec} \braket{\xvec}{\psi(t)} = \braket{\psi(t)}{\psi(t)} = 1,
:::

does not, since it is just the square norm of the wave function which is constant in time due to the unitarity of $U(t,t_0)$.

Associated with the probability density $\rho(\xvec,t)$ is a probability current $\Jvec(\xvec,t)$ satisfying

:::{math}
:label: eq-tevolut-55
\del\cdot\Jvec + \frac{\partial \rho}{\partial t} =0.
:::

The current is conveniently expressed in terms of the velocity operator, which in the configuration representation is given by

:::{math}
:label: eq-tevolut-56
\vvec = {1\over m}\pvec = -{i\hbar\over m} \del.
:::

The current itself is

:::{math}
:label: eq-tevolut-57
\Jvec(\xvec,t) = {1\over 2} [ \psi^\cc(\xvec,t) \vvec \psi(\xvec,t) + \psi(\xvec,t) \vvec \psi^\cc(\xvec,t)]= \Re[\psi^\cc(\xvec,t) \vvec \psi(\xvec,t)]
:::

The current looks like the real part of the expectation value of $\vvec$, but it is not since we do not integrate over all space. It is however the real part of the integrand of that expectation value. It is straightforward to prove the continuity equation {eq}`eq-tevolut-55` with the aid of the Schr\"odinger equation {eq}`eq-tevolut-49`.

Notice that if $\psi(\xvec,t)$ is an energy eigenfunction $\psi_n(\xvec) e^{-iE_nt/\hbar}$, then $\rho$ is independent of time and the continuity equation reduces to $\del\cdot\Jvec=0$. Also, if the Hamiltonian is of the kinetic-plus-potential form, then time-reversal invariance (see {ref}`ch-topicsoned`{} and \timerev) implies that the energy eigenfunctions can be chosen to be real. In that case, $\Jvec=0$.

The definition of the probability current depends on the system. For the case considered here, a single particle moving in 3-dimensional space, the probability current $\Jvec$ is a 3-vector. In an $N$-particle system the probability current is a $3N$-vector on the $3N$-dimensional configuration space. Also, even for a single particle, the definition is modified in the presence of magnetic fields, as we shall explain in \secrtevolut-17 below, or when there is spin.

(sec-tevolut-15)=

## Physical Significance of the Probability Density and Current

The existence of a probability density $\rho$ and current $\Jvec$ that satisfy the continuity equation {eq}`eq-tevolut-55` is usually regarded as an essential part of the probabilistic interpretation of the wave function $\psi$. There is, however, the question of the physical interpretation of $\rho$ and $\Jvec$.

The physical interpretation of the density $\rho$ is clear on the basis of the postulates of quantum mechanics: It gives the distribution of measured positions of the particle when measurements are made across an ensemble of identically prepared systems. We should not think that the particle in an individual system has been somehow smeared around in space. If we make a measurement of the position of the particle, we find some definite value, not some fraction of a particle in one region and another fraction in another. In particular, if the particle has charge, we never measure a fraction of the charge. Thus, fundamentally, the density $\rho$ describes the statistics of the ensemble, not some kind of smearing of an individual system. Nevertheless, there are circumstances in which the latter interpretation also appears, as we shall explain. Similar considerations apply to the current $\Jvec$.

In the case of a charged particle, it is suggestive to multiply both the probability density $\rho$ and current $\Jvec$ by the charge of the particle $q$, and to write

:::{math}
:label: eq-tevolut-58
\rho_c = q\rho, \qquad \Jvec_c = q\Jvec,
:::

since then the continuity equation for $\rho_c$ and $\Jvec_c$ looks like the law of conservation of charge,

:::{math}
:label: eq-tevolut-59
\del\cdot\Jvec_c + \frac{\partial \rho_c}{\partial t} =0.
:::

But now the question arises, do this $\rho_c$ and $\Jvec_c$ serve as sources for electromagnetic fields? If so, are these fields measurable? That is, are electric and magnetic fields produced by the average positions and motions of the charged particle across the ensemble, or by their “actual” positions and velocities in an individual system? (We put “actual” in quotes because position and velocity do not commute, and so cannot simultaneously have a precise value.)

Consider, for example, a hydrogen atom in the ground state. The wave function for the electron is rotationally symmetric and dies off exponentially with a scale length which is the Bohr radius, so the probability density $\rho=|\psi|^2$ and effective charge density $\rho_c = -e\rho$ do the same. At a distance large compared to the Bohr radius, the electron wave function and hence probability density are essentially zero. Since the probability density is rotationally symmetric, that is, it is a function only of the radius $r$, the electric field produced by $\rho_c$ is easy to calculate by Gauss's law. The electric field is purely in the radial direction, and, far from the proton, it is the same as that of an electron at the origin (the position of the proton). If we add the electric field of the proton, the total electric field far from the hydrogen atom is zero.

On the other hand, in a classical model of the hydrogen atom, in which the electron has a definite position, the electric field produced by the electron and proton is a dipole field, which falls off as $1/r^3$. Moreover, the dipole is time-dependent, as the electron moves around in its orbit. This is quite different from the electric field produced by the average charge density $\rho_c$.

If we take an actual hydrogen atom in the ground state and measure the electric field, which do we get? A dipole field, or a field that falls off exponentially to zero within a short distance?

This is a somewhat subtle question. In the first place, the electron is in orbit around the proton, so if we wish to see a dipole field we would need to make the measurement on a time scale shorter than the orbital period of the electron, which is something like $10^{-16}$ seconds. It would be hard to make such a measurement in practice. On longer time scales we will see an average field. In fact, taking an expectation value of an observable with respect to an energy eigenfunction is similar to making a time average in classical mechanics. (The one goes over into the other in the classical limit.) This can be seen crudely by the time-energy uncertainty principle, $\Delta t \Delta E >\approx \hbar$. In an energy eigenstate, $\Delta E=0$ since the energy is exactly known. Thus the time is completely unknown.

But if it were practical to make a measurement of the electric field on a very short time scale, what would we find? To answer this question, we must first remember that according to the measurement postulates of quantum mechanics, all observables are represented by operators that act on some ket space. This must also apply to the measurement of the electric field that we are contemplating. According to classical electromagnetic theory, the electric field at field point $\rvec$ due to an electron of charge $-e$ at position $\xvec$ is

:::{math}
:label: eq-tevolut-60
\Evec(\rvec) = -{e(\rvec-\xvec)\over|\rvec-\xvec|^3},
:::

in the electrostatic approximation. There are two measurable quantities that appear in this formula, the position $\xvec$ of the electron and the value $\Evec$ of the electric field at observation point $\rvec$. But the observation point $\rvec$ is not an observable, since we are not measuring it; it is just the place where we make the measurement of $\Evec$. With this understanding, we see that $\Evec$ is a function of $\xvec$, that is, $\Evec(\rvec)$ is an operator (really, a vector of operators) that act on the ket space for the electron. Since the components of $\xvec$ commute with one another, so also do the components of $\Evec$, and $\Evec$ at one point $\rvec_1$ commutes with $\Evec$ at another point $\rvec_2$. In fact, by measuring $\Evec$ at any point $\rvec$ and knowing the charge of the electron, we can solve {eq}`eq-tevolut-60` for $\xvec$, the position of the electron. Measuring the electric field at a point is thus equivalent to measuring the position of the electron. The value measured in any individual system is thus a dipole field, as in the classical case.

We emphasize that this discussion is based on the electrostatic approximation, in which we ignore the retardation in the communication between the source of the field (the electron, at position $\xvec$) and the observer (at position $\rvec$). We also ignore magnetic fields and other effects that lie outside the electrostatic approximation.

It is possible to make a variation on this situation that is not hampered by short time scales. Consider a double slit (really, a double hole) experiment, in which a plane wave (a pure state of a given energy) of electrons is directed against a screen $S$. See {ref}`fig-tevolut-1`. There are two holes in the screen that are large compared to the wavelength, so that two parallel beams emerge on the other side. We assume the beams are wide enough to ignore diffraction effects (the spreading of the beam) over the extent of the experiment. Then probability density $\rho$ is nonzero inside two cylinders (the two beams) downstream from the holes. This is a variation in the double slit experiment, in which one of the questions is whether a single electron passes somehow through both holes, or how we can know which hole it passed through.

:::{figure} images/tevolut-fig01.png
:label: fig-tevolut-1
:width: 80%

A variation of the double slit experiment, in which we attempt to measure which hole in the screen $S$ the electron passed through by measuring the electric field produced on test charge $T$ as the electron passes by.
:::

Let us place a test charge $T$ half way between the two beams, as in the figure. By symmetry, the electric field produced by $\rho_c$ is zero on the axis between the two beams, so if $T$ is affected by the electric field of the particle smeared out according to $\rho_c$, then it should not move. But if we think of an individual system in a classical sense, each electron will pass by the test charge on one side or the other. If we imagine that $T$ is massive enough that it does not move much while the electron is passing by, then the main effect of the electron is to deliver an impulse in the transverse direction (up or down in the figure). If we see which direction the test charge moves, we can detect which of the two beams the electron was in. So now the question is, what does the test particle really do in a double hole experiment of this type? Does it respond to the average electric field, or to the field of an individual electron, as in a classical model?

To answer this question we must realize that the test particle is a quantum mechanical system in its own right, so we must represent it by a wave function, say a wave packet centered initially on the symmetry axis between the two beams. In fact, because the test particle interacts with the electron in the beam, we are really dealing with a two-particle system. Suppose for simplicity that initially the wave function has the product form, $\Psi(\xvec_e,\xvec_T) =\psi_e (\xvec_e) \psi_T(\xvec_T)$, where $e$ refers to the electron and $T$ to the test particle, and where $\psi_T(\xvec_T)$ is a wave packet centered on position $T$ in the figure. There is of course the extra assumption that the entire system is in a pure state.

Then we are inclined to ask, does the wave packet of the test particle move up or down, as if the electron were in one beam or the other, or does it stay put, in response to the electric field produced by $\rho_c$? As it turns out, this is not exactly the right question, because although the test particle has a wave function (a wave packet) at the initial time, once the interaction begins the two-particle wave function can no longer be represented as a product of two single-particle wave functions. As we say, the two particles become “entangled.” That is, the concept of the wave function of the test particle, by itself, loses meaning. See Prob. {ref}`prob-density-3` for more on this point. It does make sense, however, to talk about the probability density of the test particle in space, and we can ask whether that moves in one direction or the other, or whether it stays put. The answer is that it does neither; it splits into two parts, with one going up and the other down. The probability distribution of the test particle responds to the probability distribution of the electron, but that tells us nothing about what an actual test particle will do. That is, if we measure the velocity of the test particle after some time, we will find that it has some probability of pointing upward, and some of pointing downward (50\% each, in the symmetrical arrangement of {ref}`fig-tevolut-1`).

What we are seeing here is the first step in the measurement process, in this case, measuring which of the two beams the electron is in. In general, in a measurement process, the system interacts with the measuring apparatus, causing the combined quantum mechanical system of system plus measuring apparatus to become entangled. This entanglement is roughly similar to correlations of random variables in ordinary statistics, but more subtle because it is quantum statistics, not classical. The combined system remains entangled even if the interaction ceases after some time (for example, when the measuring apparatus is removed).

To pursue line of thinking further would take us deeper into the quantum theory of measurement. Let us instead return to the probability density $\rho$ and current $\Jvec$, and just mention that similar considerations apply to $\Jvec$ as to $\rho$. That is, a moving charge produces a magnetic field, which is in principle measurable. If the time scale for the measurement is long compared to the time scale of the system being measured, then the magnetic field is the one produced by the ensemble average of the system, that is, by $\Jvec_c$. On shorter time scales, it will be the field produced by an individual member of the ensemble, with probabilities determined by the rules of quantum mechanics.

An example we will see later in the course in which one electron is influenced by the average field of other electrons is the Hartree approximation in many-electron atoms. See {ref}`ch-hartfock`.

To summarize with a simple rule, it sometimes leads to physical insight to view $\rho_c$ and $\Jvec_c$ as the sources of electric and magnetic fields in individual systems. A detailed understanding of this fact must take into account adiabatic considerations (that is, time scales) and the measurement postulates of quantum mechanics.

(sec-tevolut-16)=

## The Ehrenfest Relations

Let us continue with a single particle moving in 3-dimensional space under the influence of the potential $V(\xvec,t)$. The Hamiltonian is {eq}`eq-tevolut-47`. Let us work out the Heisenberg equations of motion {eq}`eq-tevolut-22` for the position $\xvec$ and momentum $\pvec$. Neither of these operators has any explicit time dependence, so the equations of motion are

:::{math}
:label: eq-tevolut-61
\begin{aligned}
\dot\xvec &= -{i\over\hbar} [\xvec,H], \\
\dot\pvec &= -{i\over\hbar} [\pvec,H]. \\

\end{aligned}
:::

We omit the $H$-subscripts, but these operators are in the Heisenberg picture. The commutators can be evaluated with the help of the results of Prob. {ref}`prob-spatialdof-4`.

The result is

:::{math}
:label: eq-tevolut-62a
\begin{aligned}
\dot\xvec &= {\pvec\over m},
\end{aligned}
:::

:::{math}
:label: eq-tevolut-62b
\begin{aligned}
\dot\pvec &= -\del V(\xvec,t).
\end{aligned}
:::

These are operator versions of Newton's laws {eq}`eq-tevolut-46`. Now we take the expectation value of {eq}`eq-tevolut-62a` with respect to some state $\ket{\psi}$, remembering that expectation values are the same in the Heisenberg and Schr\"odinger pictures. Here we attach subscripts $H$ and $S$ to indicate the picture. We have

:::{math}
\begin{aligned}
\matrixelement{\psi_H}{\dod{\xvec_H}{t}}{\psi_H} &= \dod{}{t} \matrixelement{\psi_H}{\xvec_H(t)}{\psi_H} = \dod{}{t} \matrixelement{\psi_S(t)}{\xvec_S}{\psi_S(t)}
\end{aligned}
:::

:::{math}
:label: eq-tevolut-63
\begin{aligned}
&={1\over m} \matrixelement{\psi_H}{\pvec_H(t)}{\psi_H} ={1\over m} \matrixelement{\psi_S(t)}{\pvec_S}{\psi_S(t)},
\end{aligned}
:::

where we use the fact that the ket $\ket{\psi_H}$ and the operators $\xvec_S$ and $\pvec_S$ are independent of time. A similar calculation applies to {eq}`eq-tevolut-62b`. Then the expectation values of {eq}`eq-tevolut-62a` become

:::{math}
:label: eq-tevolut-64
\begin{aligned}
\dod{\xpecval{\xvec}}{t} &= {1\over m} \xpecval{\pvec}, \\
\dod{\xpecval{\pvec}}{t} &= -\xpecval{\del V(\xvec,t)}, \\

\end{aligned}
:::

where we are now in the Schr\"odinger picture and have dropped the $S$ subscripts. These are versions of the classical Hamilton's equations, applied to expectation values. Eliminating $\xpecval{\pvec}$ from them, we have

:::{math}
:label: eq-tevolut-65
m{d^2\xpecval{\xvec} \over dt^2} = -\xpecval{\del V(\xvec,t)},
:::

an expectation value version of the classical Newton's equations {eq}`eq-tevolut-46`. Equations {eq}`eq-tevolut-64` or {eq}`eq-tevolut-65` are the *Ehrenfest relations* for a particle moving in a potential in 3-dimensional space.

The Ehrenfest relations are exact, and they make no assumption about the state $\ket{\psi}$ that is used for the expectation values. In particular, it need not be a wave packet. But these equations do not say that the expectation value of $\xvec$ follows the classical motion. That would be true if the right hand side of {eq}`eq-tevolut-65` were $-\del V(\xpecval{\xvec},t)$ instead of $-\xpecval{\del V(\xvec,t)}$.

On the other hand, suppose the wave function $\psi(\xvec)$ is localized about its expectation value $\xvec_0 = \xpecval{\xvec}$, that is, suppose it is a wave packet, and suppose $f(\xvec)$ is a function that is slowly varying on the scale length of the width of $\psi$. Both $\psi$ and $f$ may depend on time, but we suppress the time dependence. Then

:::{math}
\begin{aligned}
\xpecval{f(\xvec)} &= \int d^3\xvec \, |\psi(\xvec)|^2 f(\xvec)
\end{aligned}
:::

:::{math}
:label: eq-tevolut-66
\begin{aligned}
&\approx \int d^3\xvec \, |\psi(\xvec)|^2 \Bigl[ f(\xvec_0) + (\xvec-\xvec_0)\cdot \del f(\xvec_0) + \ldots\Bigr] = f(\xvec_0)=f(\xpecval{\xvec}),
\end{aligned}
:::

since the first order term in the Taylor series vanishes upon integration. Identifying $f$ with one of the components of $\del V$, we see that $-\xpecval{\del V(\xvec,t)}$ is approximately equal to $-\del V(\xpecval{\xvec},t)$, under the conditions stated. In other words, the expectation value $\xpecval{\xvec}$ of a wave packet moving in a slowly varying potential does indeed approximately follow the classical motion. The corrections to {eq}`eq-tevolut-66` that have been omitted involve the second derivatives of $f$.

It should be noted that the width of the wave packet is not constant in time, and that in general, wave packets spread, so that a wave function that is initially localized in configuration space will not stay that way. When the width of the wave function becomes comparable to the scale length of the potential, the expectation values no longer follow the classical motion even approximately.

In the special case that $f$ in {eq}`eq-tevolut-66` is a linear function of $\xvec$, the correction terms all vanish, and {eq}`eq-tevolut-66` is exact. Note that the force $-\del V$ is linear in $\xvec$ when the potential $V$ itself is quadratic in $\xvec$. We see that the expectation value of the position of the particle $\xpecval{\xvec}$ follows the classical motion in potentials that are quadratic functions of the coordinates. Such potentials include the free particle, the particle in a uniform electric or gravitational field, the harmonic oscillator, and other examples. For such potentials, the result holds regardless of the nature of the wave function (it need not be a wave packet).

One can show that the expectation values follow the classical motion more generally when the Hamiltonian is any quadratic function of $\xvec$ and $\pvec$. In addition to the systems mentioned, this includes a charged particle moving in a uniform magnetic field.

The Ehrenfest relations provide one way of understanding how the classical limit emerges from quantum mechanics. Another way involves WKB theory, which we will take up in {ref}`ch-wkb`.

(sec-tevolut-17)=

## Particles in Electromagnetic Fields

Let us now consider a single particle of charge $q$ moving in an electromagnetic field, which for generality we allow to be time-dependent. The fields are given in terms of the scalar potential $\Phi$ and the vector potential $\Avec$ by

:::{math}
:label: eq-tevolut-67a
\begin{aligned}
\Evec &=-\del\Phi -{1\over c}\frac{\partial \Avec}{\partial t},
\end{aligned}
:::

:::{math}
:label: eq-tevolut-67b
\begin{aligned}
\Bvec &=\del\cross\Avec.
\end{aligned}
:::

The classical equations of motion are expressed in terms of $\Evec$ and $\Bvec$,

:::{math}
:label: eq-tevolut-68
m \avec = q\Bigl[\Evec(\xvec,t) + {1\over c} \vvec\cross\Bvec(\xvec,t)\Bigr],
:::

where $\vvec=\dot\xvec$ and $\avec=\ddot\xvec$. But the classical Hamiltonian requires the use of the potentials $\Phi$ and $\Avec$,

:::{math}
:label: eq-tevolut-69
H = {1\over 2m}\Bigl[\pvec -{q\over c}\Avec(\xvec,t)\Bigr]^2 + q\Phi(\xvec,t),
:::

which is a single-particle version of {eq}`eq-classmech-86`. The momentum $\pvec$ appearing here is the *canonical momentum*, related to the velocity by

:::{math}
:label: eq-tevolut-70
\pvec = m\vvec + {q\over c}\Avec(\xvec,t),
:::

which is not to be confused with the *kinetic momentum* $\pvec_kin=m\vvec$. In the presence of a magnetic field, these two momenta are not the same. See the discussion in {ref}`sec-classmech-11`. Because of the relationship {eq}`eq-tevolut-70`, the first major term of the Hamiltonian {eq}`eq-tevolut-69` is just the kinetic energy, $(1/2)mv^2$, albeit written in a complicated way.

It is strange that the classical Hamiltonian requires the use of potentials and the canonical momentum, none of which is gauge-invariant. This is, however, a fact. The curious status of potentials in quantum theory is explored further in {ref}`ch-magfield`.

To obtain the Hamiltonian for a charged particle moving in an electromagnetic field in quantum mechanics we take over the classical Hamiltonian {eq}`eq-tevolut-68` and reinterpret $\xvec$ and $\pvec$ as operators. We call this the *quantization* of the classical Hamiltonian. This makes $\pvec$ the quantum analog of the canonical momentum in classical mechanics, but, as discussed in {ref}`ch-spatialdof`, that is the momentum that should be interpreted as the generator of translations and the one that corresponds to the operator $-i\hbar\del$ in the configuration representation (not the kinetic momentum).

There is one issue that arises in this process, namely the fact that the product $\pvec\cdot\Avec$ occurs in the expansion of the kinetic energy. Classically, $\pvec\cdot\Avec=\Avec\cdot\pvec$, but in quantum mechanics these are not the same because of the commutation relations $[x_i,p_j]=i\hbar\,\delta_{ij}$. Thus there is an ambiguity in the quantization of the classical Hamiltonian, because the results depend on the order in which the classical expression is written (before the classical $\xvec$'s and $\pvec$'s are replaced by quantum operators). We resolve this ambiguity by interpreting the kinetic energy operator as

:::{math}
\begin{aligned}
{1\over 2m}\Bigl[\pvec -{q\over c}\Avec(\xvec,t)\Bigr]^2 &={1\over 2m}\Bigl[\pvec -{q\over c}\Avec(\xvec,t)\Bigr] \cdot\Bigl[\pvec -{q\over c}\Avec(\xvec,t)\Bigr]
\end{aligned}
:::

:::{math}
:label: eq-tevolut-71
\begin{aligned}
&={p^2\over 2m} -{q\over 2mc}(\pvec\cdot\Avec+\Avec\cdot\pvec) +{q^2\over 2mc^2}A^2.
\end{aligned}
:::

By this interpretation, $H$ is Hermitian, as it must be. Notice that in the presence of a magnetic field, $p^2/2m$ is not the kinetic energy, rather the kinetic energy is the entire expression {eq}`eq-tevolut-71`.

As in our previous exercise in quantization, it is a guess that the Hamiltonian {eq}`eq-tevolut-69`, reinterpreted as a quantum operator, is correct physically. In fact, this Hamiltonian neglects several effects that we shall incorporate later.

Now translating the time-dependent Schr\"odinger equation into the configuration representation, we obtain the differential equation,

:::{math}
:label: eq-tevolut-72
{1\over 2m}\Bigl[-i\hbar\del -{q\over c}\Avec(\xvec,t) \Bigr]^2 \psi(\xvec,t) + q\Phi(\xvec,t)\psi(\xvec,t) = i\hbar\frac{\partial \psi(\xvec,t)}{\partial t},
:::

which generalizes {eq}`eq-tevolut-49`. Explicitly, the differential operator on the left of {eq}`eq-tevolut-72` is given by

:::{math}
:label: eq-tevolut-73
\Bigl[-i\hbar\del -{q\over c}\Avec(\xvec,t) \Bigr]^2 \psi = -\hbar^2\del^2\psi +{i\hbar q\over c}\del\cdot(\Avec \psi) +{i\hbar q\over c}\Avec\cdot\del\psi +{q^2\over c^2}A^2\psi.
:::

Similarly, when $\Phi$ and $\Avec$ are time-independent, we can write down the time-independent Schr\"odinger equation,

:::{math}
:label: eq-tevolut-74
{1\over 2m}\Bigl[-i\hbar\del -{q\over c}\Avec(\xvec) \Bigr]^2 \psi(\xvec) + q\Phi(\xvec)\psi(\xvec) =E\psi(\xvec),
:::

an equation for the energy eigenfunction $\psi(\xvec)$ and eigenvalue $E$.

The Schr\"odinger equation {eq}`eq-tevolut-72` possesses a conserved probability current $\Jvec$. The definition is {eq}`eq-tevolut-57`, the same as in the absence of a magnetic field, but now the velocity operator must be interpreted as

:::{math}
:label: eq-tevolut-75
\vvec = {1\over m}\Bigl[\pvec -{q\over c}\Avec(\xvec,t)\Bigr] ={1\over m}\Bigl(-i\hbar\del -{q\over c}\Avec(\xvec,t) \Bigr).
:::

It will be left as an exercise to show that $\rho=|\psi|^2$ and $\Jvec$ with this definition satisfy the continuity equation {eq}`eq-tevolut-55`.

(sec-tevolut-18)=

## Unitary Transformations

Unitary transformations provide invertible maps of the Hilbert space onto itself that preserve all scalar products and hence probabilities. They are widely used in the study of symmetries, perturbation theory, and elsewhere.

Let the Schr\"odinger equation be written

:::{math}
:label: eq-tevolut-76
H\ket{\psi(t)} = i\hbar\pop{}{t}\ket{\psi(t)},
:::

and let $U(t)$ be a unitary operator, which for generality we allow to depend on time. Then, multiplying {eq}`eq-tevolut-76` through by $U(t)$, we can write

:::{math}
:label: eq-tevolut-77
U(t)HU(t)^\dagger U(t)\ket{\psi(t)} = U(t)i\hbar\pop{}{t}\ket{\psi(t)} = i\hbar\pop{}{t}\bigl[U(t)\ket{\psi(t)}\bigr] -i\hbar \frac{\partial U(t)}{\partial t}U(t)^\dagger U(t)\ket{\psi(t)},
:::

or,

:::{math}
:label: eq-tevolut-78
H'\ket{\psi'(t)} = i\hbar\pop{}{t}\ket{\psi'(t)},
:::

where

:::{math}
:label: eq-tevolut-79
\ket{\psi'(t)}=U(t)\ket{\psi(t)}
:::

and

:::{math}
:label: eq-tevolut-80
H' = U(t)HU(t)^\dagger +i\hbar\frac{\partial U(t)}{\partial t}U^\dagger(t).
:::

Thus, the form of the Schr\"odinger equation remains the same after the unitary transformation, with a new Hamiltonian.

(sec-tevolut-19)=

## Gauge Transformations in Quantum Mechanics

An example of a unitary transformation is a gauge transformation, or, at least, this is one interpretation. We now show how this comes about.

The potentials $\Phi$ and $\Avec$ that give $\Evec$ and $\Bvec$ through {eq}`eq-tevolut-67a` are not unique, rather they can be subjected to a *gauge transformation*, specified by a scalar field $f$ that we call the *gauge scalar*. The new (primed, or gauge-transformed) potentials are given in terms of the old ones by

:::{math}
:label: eq-tevolut-81a
\begin{aligned}
\Phi' &= \Phi - {1\over c}\frac{\partial f}{\partial t},
\end{aligned}
:::

:::{math}
:label: eq-tevolut-81b
\begin{aligned}
\Avec' &= \Avec + \del f.
\end{aligned}
:::

The electric and magnetic fields, however, do not change under the gauge transformation, that is, $\Evec'=\Evec$ and $\Bvec'=\Bvec$. Thus we might say that the potentials $\Phi$ and $\Avec$ contain a physical part (because the physical fields $\Evec$ and $\Bvec$ can be computed from them), and a nonphysical part (the part that changes under a gauge transformation). Since the Hamiltonian {eq}`eq-tevolut-69` is expressed in terms of $\Phi$ and $\Avec$, we must understand how it and the Schr\"odinger equation change under a gauge transformation.

It turns out that when we change the gauge of $\Phi$ and $\Avec$, we must also change the wave function $\psi(\xvec,t)$. In fact, $\psi$ changes by a space- and time-dependent phase factor,

:::{math}
:label: eq-tevolut-82
\psi'(\xvec,t) = e^{i\alpha(\xvec,t)}\,\psi(\xvec,t),
:::

where $\alpha$ is related to the gauge scalar by

:::{math}
:label: eq-tevolut-83
\alpha(\xvec,t)={q\over\hbar c}\,f(\xvec,t).
:::

Writing

:::{math}
:label: eq-tevolut-84
\begin{aligned}
\psi(\xvec,t)&=\braket{\xvec}{\psi(t)}, \\
\psi'(\xvec,t)&=\braket{\xvec}{\psi'(t)}, \\

\end{aligned}
:::

for two time-dependent state vectors $\ket{\psi(t)}$ and $\ket{\psi'(t)}$, we can interpret the gauge transformation {eq}`eq-tevolut-82` as the effect of a time-dependent unitary transformation on state vectors,

:::{math}
:label: eq-tevolut-85
\ket{\psi'(t)} = e^{i\alpha(\xvec,t)}\,\ket{\psi(t)}.
:::

Then, in view of the commutator,

:::{math}
:label: eq-tevolut-86
[e^{i\alpha(\xvec,t)},\pvec]=-\hbar\del\alpha(\xvec,t)\, e^{i\alpha(\xvec,t)}
:::

(see Prob. {ref}`prob-spatialdof-4`), we have

:::{math}
:label: eq-tevolut-87
e^{i\alpha(\xvec,t)} \Bigl[\pvec-{q\over c}\Avec(\xvec,t)\Bigr] = \Bigl[\pvec-{q\over c}\Avec(\xvec,t)-\hbar\del\alpha(\xvec,t) \Bigr]\, e^{i\alpha(\xvec,t)} = \Bigl[\pvec-{q\over c}\Avec'(\xvec,t)\Bigr]\,e^{i\alpha(\xvec,t)},
:::

where we have used {eq}`eq-tevolut-81b` and {eq}`eq-tevolut-83`. In other words, pushing the phase factor $e^{i\alpha(\xvec,t)}$ through the expression for the kinetic momentum changes $\Avec$ into $\Avec'$.

Let us now write the Schr\"odinger equation as in {eq}`eq-tevolut-76`, where

:::{math}
:label: eq-tevolut-88
H={1\over 2m}\Bigl[\pvec-{q\over c}\Avec(\xvec,t)\Bigr]^2 +q\Phi(\xvec,t),
:::

and let us transform the state vector according to {eq}`eq-tevolut-85`, which is an example of a unitary transformation, as in {eq}`eq-tevolut-79`. Then we use {eq}`eq-tevolut-80` to find the new Hamiltonian $H'$. For the kinetic energy we need

:::{math}
:label: eq-tevolut-89
e^{i\alpha(\xvec,t)}\,{1\over 2m}\Bigl[\pvec-{q\over c} \Avec(\xvec,t)\Bigr]^2 \,e^{-i\alpha(\xvec,t)}= {1\over 2m}\Bigl[\pvec-{q\over c}\Avec'(\xvec,t)\Bigr]^2,
:::

where we use {eq}`eq-tevolut-87`. For the potential energy and the final term of {eq}`eq-tevolut-80` we have

:::{math}
:label: eq-tevolut-90
e^{i\alpha(\xvec,t)}\, q\Phi(\xvec,t)\,e^{-i\alpha(\xvec,t)} +i\hbar \pop{e^{i\alpha(\xvec,t)}}{t}\, e^{-i\alpha(\xvec,t)} =q\Phi -\hbar\frac{\partial \alpha}{\partial t} =q\Bigl(\Phi-{1\over c}\frac{\partial f}{\partial t}\Bigr)=q\Phi'(\xvec,t).
:::

Altogether, the transformed Hamiltonian is

:::{math}
:label: eq-tevolut-91
H'={1\over2m}\Bigl[\pvec-{q\over c}\Avec'(\xvec,t)\Bigr]^2 +q\Phi'(\xvec,t),
:::

that is, it is a version of the original Hamiltonian {eq}`eq-tevolut-88` but with the gauge-transformed fields $\Avec'$ and $\Phi'$. We see that if the wave function transforms according to {eq}`eq-tevolut-82` and {eq}`eq-tevolut-83`, then the Schr\"odinger equation maintains its form under a gauge transformation.

Thus we see that the wave function $\psi(\xvec,t)$ is gauge-dependent. Since a gauge convention is just a convention, it must mean that we cannot measure $\psi(\xvec,t)$, since a measurement must give us a value that is independent of convention.

This is correct. The Schr\"odinger wave function $\psi(\xvec,t)$ is not like a classical field, such as the pressure in a fluid. Such classical fields can be measured at a given spatial point at a given time, in principle without difficulty. Likewise, the measurement of the probability density $|\psi(\xvec,t)|^2$ in quantum mechanics presents in principle no difficulty, since one just accumulates the statistics of position measurements. But the discussion above shows that one cannot measure the phase of $\psi(\xvec,t)$ unless one is committed to a certain gauge convention (a choice of $\Avec$) for whatever magnetic field is present. In principle this applies even in the case $\Bvec=0$, although here the usual gauge $\Avec=0$ would be the obvious choice. As for $\Phi$, it affects the manner in which the phase of $\psi$ depends on time.

(sec-tevolut-20)=

## Another Interpretation of Gauge Transformations

In the interpretation given in \secrtevolut-19, both the wave function $\psi(\xvec,t)$ and the abstract state vector $\ket{\psi(t)}$ change under a gauge transformation. We cannot alter the fact that the wave function depends on the gauge, but there is another interpretation in which the abstract state vector is invariant. That is, we use {eq}`eq-tevolut-82` and {eq}`eq-tevolut-84` to write

:::{math}
:label: eq-tevolut-92
\psi'(\xvec,t)= \matrixelement{\xvec}{e^{i\alpha(\xvec,t)}}{\psi(t)}= \braket{\xvec}{'\psi(t)},
:::

where

:::{math}
:label: eq-tevolut-93
\ket{\xvec}' = e^{-i\alpha(\xvec,t)}\,\ket{\xvec}.
:::

In other words, we regard the gauge transforation as a change in the phase conventions for the position eigenkets.

\problems

(prob-tevolut-1)=

**Problem \prbdtevolut-1..** 

:::{math}
:label: eq-tevolut-94
H={1\over2m}\Bigl[ \pvec-{q\over c}\Avec(\xvec,t)\Bigr]^2 +q\Phi(\xvec,t),
:::

where we allow all fields to be space- and time-dependent.

\problempart{(a)} Define the kinetic momentum operator $\pivec$ by

:::{math}
:label: eq-tevolut-95
\pivec = \pvec - {q\over c}\Avec(\xvec,t).
:::

Notice that $\pivec$ has an explicit time dependence, due to the $\Avec$ term. Work out the commutation relations, $[x_i,\pi_j]$ and $[\pi_i,\pi_j]$. Use these to work out the Heisenberg equations of motion for the operators $\xvec$, $\pivec$. Then eliminate $\pivec$, and find an expression for $\ddot\xvec$ (the Heisenberg analog of the Newton-Lorentz equations).

\problempart{(b)} By taking expectation values, show that if $\Bvec$ is uniform in space and $\Evec$ has the form,

:::{math}
:label: eq-tevolut-96
E_i(\xvec) = a_i + \sum_j b_{ij}\,x_j,
:::

where $a_i$ and $b_{ij}$ are constants, then the expectation value of $\xvec$ follows the classical orbit.

(prob-tevolut-2)=

**Problem \prbdtevolut-2..** 

(prob-tevolut-3)=

**Problem \prbdtevolut-3..** 

:::{math}
:label: eq-tevolut-97
H={p^2\over 2m}.
:::

\problempart{(a)} Let the wave function at $t=0$ be

:::{math}
:label: eq-tevolut-98
\psi_0(x) = \psi(x,0) = C e^{-x^2/4L^2},
:::

where $C$ and $L$ are constants. Assuming $C$ is real and positive, normalize the wave function and find $C$. See Appendix~\gaussint. Then determine $\xpecval{x}$, $\xpecval{p}$ and $\Delta x$, the last one being the dispersion (or standard deviation), see {eq}`eq-postulat-40`.

\problempart{(b)} Compute the initial momentum space wave function $\phi_0(p)$, and from that compute $\Delta p$ (do the latter calculation in momentum space). Compare $\Delta x \Delta p$ to the minimum value allowed by the uncertainty principle.

\problempart{(c)} Now compute $\phi(p,t)$ for any time $t$. Use it to find $\xpecval{p}$ and $\Delta p$ for any time $t$.

\problempart{(d)} Now compute $\psi(x,t)$ for any time $t$. Express your answer in terms of the quantity,

:::{math}
:label: eq-tevolut-99
D=L+{it\hbar\over 2mL}
:::

(a useful abbreviation). Then find $\xpecval{x}$ and $\Delta x$ for any time $t$. Notice what happens to the product $\Delta x \Delta p$ for times $t>0$.

\problempart{(e)} If you had not done a detailed calculation you could estimate $\Delta x$ as a function of $t$ by using the uncertainty principle. Do this and compare to the results of the detailed calculation.

(prob-tevolut-4)=

**Problem \prbdtevolut-4..**
