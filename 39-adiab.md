---
title: "39. Adiabatic Invariance, the Geometric Phase, and the Born-Oppenheimer Approximation"
---
(ch-adiab)=

# 39. Adiabatic Invariance, the Geometric Phase, and the Born-Oppenheimer Approximation

A time-dependent system is said to be *adiabatic* if the time-dependence is slow. First we will say a few words about adiabatic systems in classical mechanics. A simple example is a pendulum with a slowly varying length. Let $L$ be the length of the pendulum, so that the frequency is given by

:::{math}
:label: eq-adiab-1
\omega = \sqrt{\ds{\ds g\over \ds L}}.
:::

When we say that the length is slowly varying, mean that $L$ does not vary much on during a single cycle of oscillation, or

:::{math}
:label: eq-adiab-2
{\dot L \over L} \ll \omega.
:::

We can write $L=L(\epsilon t)$ to indicate this slow time dependence, where we think of $\epsilon$ as a small parameter. Since $\omega$ is a function of $L$, we also have $\omega=\omega(\epsilon t)$. Then for small angles $\theta$ of oscillation, the equation of motion of the pendulum is

:::{math}
:label: eq-adiab-3
\ddot \theta + \omega(\epsilon t)^2 \theta =0,
:::

which is that of a harmonic oscillator with slowly varying frequency. It is interesting that a treatment of this equation when $\epsilon$ is small is mathematically the same as the treatment of the one-dimensional Schr\"odinger equation when $\hbar$ is small. That is, the method is WKB theory.

More generally, an adiabatic system in classical mechanics is (generally an oscillator) with slowly time-dependent parameters. Neither the frequency nor the energy of the oscillator is conserved in the adiabatic process, but there is an approximate conserved quantity,

:::{math}
:label: eq-adiab-4
I = {1\over 2\pi} \oint p\, dq,
:::

which is the action of the oscillator. The action is not exactly conserved, but it is conserved to higher accuracy as the changes in the parameters are carried out more slowly. The action is what is called an *adiabatic invariant*. As we will see below, the situation is similar in quantum mechanics; the energy is not conserved, but there is an approximate conservation law, which is that of the quantum number (in a sense to be made precise below). This makes sense, because we know that according to the Bohr-Sommerfeld quantization rule, the quantum number is proportional to the classical action.

Let us consider a quantum Hamiltonian with a slow time-dependence, which we denote by

:::{math}
:label: eq-adiab-5
H=H(\epsilon t) = H(\tau),
:::

where $\tau = \epsilon t$. The $\epsilon$ serves to remind us that the time-dependence is slow. It also has a more formal mathematical meaning, as follows. Let us suppose the Hamiltonian depends on certain parameters, which we can imagine are under experimental control. One can think of the electric and magnetic fields with which an atom or spinning particle interacts. Therefore by changing these parameters, we can change the Hamiltonian, say, from some initial value $H_0$ to some final value $H_1$. Suppose we change the Hamiltonian from $H_0$ to $H_1$, passing through some specified sequence of intermediate Hamiltonians, in some time interval $t=0$ to $t=t_1=T$. At the end of this time we can make various physical measurements on our system. Now let us repeat exactly the same procedure, except we carry out the changes in the Hamiltonian more slowly than before by some scale factor $\epsilon$, so that the changes take place over the time interval $t=0$ to $t=t_1=T/\epsilon$. The initial and final Hamiltonians are still the same, as is the sequence of intermediate Hamiltonians, but the time taken to get to the final Hamiltonian is longer by a factor of $1/\epsilon$. Then we can study how various quantities of interest, such as the probability of finding the system in some state $\ket{n}$, scale with $\epsilon$ as $\epsilon\to0$. If a quantity scales as some power of $\epsilon$, say, $\epsilon^a$, then we will say that that quantity is $O(\epsilon^a)$. For example, the elapsed time $t_1$ is $O(1/\epsilon)$. For brevity, we will refer to a time of order $1/\epsilon$ as “a long time.”

We imagine that the final Hamiltonian $H_1$ differs from the initial Hamiltonian by some amount which is of order unity, in the usual sense of that phrase in physics. For example, if we are changing magnetic fields, perhaps the final magnetic field is twice as strong as the initial one. But the final Hamiltonian is also order unity in the limiting sense defined in the preceding paragraph, since $H_1$ is independent of $\epsilon$ and therefore scales as $\epsilon^0 = 1$.

We will be interested in solving the time-dependent Schr\"odinger equation,

:::{math}
:label: eq-adiab-6
H(\epsilon t) \ket{\psi(t)} = i\hbar\pop{}{t} \ket{\psi(t)},
:::

over a long time interval. Although the time-dependent Schr\"odinger equation is not separable in time, nevertheless there is some advantage in introducing the instantaneous eigenkets and eigenvalues of the Hamiltonian. That is, we write,

:::{math}
:label: eq-adiab-7
H(\tau) \ket{n(\tau)} = E_n(\tau) \ket{n(\tau)},
:::

where naturally the eigenvalues $E_n$ and eigenkets $\ket{n}$ depend on $\tau$ since $H$ itself does. The notation $\ket{n(\tau)}$ is somewhat illogical, since it is the ket and not the quantum number that is a function of $\tau$, but we use it anyway since the more logical notation $\ket{n}(\tau)$ is awkward. Notice that since $H$ changes by an amount which is order unity in the (long) time interval of interest, so also do the eigenvalues and eigenkets; for example, we may expect some final energy eigenfunction to look rather different from the initial eigenfunction. The label $n$ is the same, of course. The eigenvalues $E_n$ are also expected to change by an amount which is of order unity.

We will assume that the spectrum of $H$ is discrete and nondegenerate for all $\tau$ of interest. The nondegeneracy assumption in particular seems a strong one, since even if $H$ is nondegenerate at $t=0$, we might expect the energy levels $E_n$, which after all are functions of $\tau$ and are expected to change by an amount which is of order unity, to cross one another in the course of time. Such a crossing of course gives rise to a degeneracy. Nevertheless, we will pursue the consequences of the nondegeneracy assumption because it leads to the simplest analysis of the adiabatic process, and consider later what happens if levels become degenerate or nearly degenerate in the course of time.

Since the eigenkets $\ket{n}$ form a complete set, we can without loss of generality expand the exact solution $\ket{\psi(t)}$ in terms of them. We write,

:::{math}
:label: eq-adiab-8
\ket{\psi(t)} = \sum_n c_n(t) \ket{n(\tau)}.
:::

Substituting this into the Schr\"odinger equation {eq}`eq-adiab-6`, we easily find the equation of evolution for the unknown coefficients $c_n$,

:::{math}
:label: eq-adiab-9
\dot c_n = -{i\over \hbar} E_n(\tau) c_n(t) -\epsilon \sum_m \matrixelement{n}{\dod{}{\tau}}{m} c_m.
:::

This equation is exact. In the second term, the operator $d/d\tau$ is not an operator in the usual sense (it is not a mapping of the ket space onto itself), but rather the matrix element shown is interpreted as the scalar product of the bra $\bra{n}$ with the ket $d\ket{m}/d\tau$.

To solve {eq}`eq-adiab-9` at lowest order, we neglect the second term on the right hand side, which is $O(\epsilon)$. Then we have

:::{math}
:label: eq-adiab-10
c_n(t) = e^{i\phi_n(t)} \, c_n(0),
:::

where

:::{math}
:label: eq-adiab-11
\phi_n(t) = -{1\over\hbar} \int_0^t E_n(\epsilon t')\, dt'.
:::

We see that in this approximation, the final coefficient $c_n(t)$ differs from the initial coefficient $c_n(0)$ by a pure phase factor, which means that the probability $P_n$ of finding the system in energy eigenstate $\ket{n}$ is independent of time:

:::{math}
:label: eq-adiab-12
P_n = |c_n(t)|^2= |\braket{n(\tau)}{\psi(t)}|^2 = \\textconst.
:::

As a special case of interest, suppose that at $t=0$ the system was in energy eigenstate $N$, that is,

:::{math}
:label: eq-adiab-13
\ket{\psi(0)}= \ket{N(0)}.
:::

Then at the final time we have,

:::{math}
:label: eq-adiab-14
\ket{\psi(t)} = e^{i\phi_N(t)} \, \ket{N(\tau)},
:::

which we can express by saying that the quantum number is conserved. We emphasize again that neither the energy $E_N$ nor the eigenket $\ket{N}$ is conserved. If we think in terms of wave functions, we see that as the Hamiltonian changes, the wave function continuously distorts so as to remain proportional to an eigenfunction of $H$. The conclusions contained in {eq}`eq-adiab-10`, {eq}`eq-adiab-12` and {eq}`eq-adiab-14` are referred to as the *adiabatic theorem*.

The phase $\phi_n(t)$, defined in {eq}`eq-adiab-11`, is called the “dynamical phase.” Obviously if the Hamiltonian were truly time-independent, the dynamical phase would be $\phi_n = -E_nt/\hbar$. As it is, {eq}`eq-adiab-11` expresses $\phi_n$ as the time integral of the instantaneous frequency $E_n/\hbar$, which is no surprise.

It is of interest to go to the next order of approximation in solving {eq}`eq-adiab-9`, for at least three reasons. First, the at the next order we will discover the conditions of validity of the adiabatic theorem. Second, the next order term leads us to the interesting subject of Berry's phase, and the associated gauge theory. Finally, it is easy to see that the next order correction is needed for various interference experiments, in which we study the interference of the final state $\psi(t)$ with some fixed state [perhaps a copy of the initial state $\psi(0)$]. To understand this interference even at a qualitative level, we must know the phase of the final state through terms that are of order unity, that is, with an error that is small compared to $2\pi$. But {eq}`eq-adiab-11` shows that the dynamical phase is $O(1/\epsilon)$, since it is the integral of a quantity that is order unity over a long time. Therefore we need the next term in the expansion of the phase, which is $O(1)$.

To go to the next order, we rewrite {eq}`eq-adiab-10`, not as the solution of an approximate equation, but as an exact change of variables. That is, we write

:::{math}
:label: eq-adiab-15
c_n(t) = e^{i\phi_n(t)} \, b_n(t),
:::

which serves to define a new set of coefficients $b_n$. We substitute this into {eq}`eq-adiab-11` and find,

:::{math}
:label: eq-adiab-16
\dot b_n(t) = -\epsilon \sum_m \matrixelement{n}{\dod{}{\tau}}{m} e^{i(\phi_m-\phi_n)} \, b_m.
:::

This equation is still exact. If we integrate both sides of this equation over a long time interval, then we might at first expect the integral of the right hand side to be of order unity, since the integrand is $O(\epsilon)$ and the time interval is $O(1/\epsilon)$. However, the off-diagonal terms on the right hand side (the terms $m\ne n$) involve the phase factor $\exp[i(\phi_m-\phi_n)]$, which oscillates many times in the long time interval in question. Therefore in the integration over the long time interval, these oscillations prevent the off-diagonal terms from accumulating. Instead, the integral of the off-diagonal terms gives an answer that is itself $O(\epsilon)$, since each oscillation nearly cancels the previous one. On the other hand, the diagonal terms $m=n$ do not have the oscillating phase factor, so the integral of them does accumulate over a long time to give a result that is of order unity.

This argument justifies the neglect of the off-diagonal terms in {eq}`eq-adiab-16`, which leaves us with

:::{math}
:label: eq-adiab-17
\dot b_n = -\epsilon \matrixelement{n}{\dod{}{\tau}}{n} b_n.
:::

We integrate this to find

:::{math}
:label: eq-adiab-18
b_n(t) = e^{i\gamma(t)} \, b_n(0),
:::

where the new phase $\gamma(t)$ is defined by

:::{math}
:label: eq-adiab-19
\gamma(t) = i\epsilon \int_0^t \matrixelement{n}{\dod{}{\tau'}}{n} \, dt' = i\int_0^\tau \matrixelement{n}{\dod{}{\tau'}}{n} \, d\tau'.
:::

The phase $\gamma(t)$ is called the “geometric phase” or “Berry's phase.” Notice that it is of order unity. Notice also that $\gamma$ is real, for if we take the normalization condition $\braket{n}{n}=1$ and differentiate with respect to time, we find

:::{math}
:label: eq-adiab-20
\braket{n}{\dot n} + \braket{\dot n}{n} = \braket{n}{\dot n} + \braket{n}{\dot n}^\cc = 0,
:::

which shows that $\dot \gamma = i\braket{n}{\dot n}$ is purely real.

Combining these results, we can express the solution to the original problem, including both the zeroth and first order approximations, in the form,

:::{math}
:label: eq-adiab-21
c_n(t) = e^{i[\phi(t) + \gamma(t)]} \, c_n(0),
:::

which shows that even at this order, the probability of finding the system in a given eigenstate is independent of time. In fact, one can show that with the proper understandings, the probability of finding the system in a given eigenstate is independent of time to all orders in the expansion parameter $\epsilon$. This does not mean that the probability is really constant, merely that the amount by which the probability changes goes to zero faster than any power of $\epsilon$ as $\epsilon\to0$. [This conclusion is true if the Hamiltonian is an infinitely differentiable function of time, perhaps an analytic function. If $H$ has only a finite number of time derivatives, then the change in the probability goes to zero as some power of $\epsilon$.]

Now we can see what happens if degeneracies or near-degeneracies develop in the course of time. An exact degeneracy, say, $E_n = E_m$ for some $n\ne m$, would mean that there was an off-diagonal term in {eq}`eq-adiab-16` that did not have the rapidly varying phase factor, at least over some time interval. This would mean that we could not neglect all the off-diagonal terms, and that the integration of {eq}`eq-adiab-16` over time would introduce a coupling between states $n$ and $m$. That is, the term in question would induce transitions between the two states. In practice, the same is true for near degeneracies, since in practice we always work with some finite time interval, and we never really take the limit $\epsilon\to0$.

We can easily understand these transitions from the standpoint of time-dependent perturbation theory. For let us suppose that the time-dependence of the Hamiltonian involves a characteristic range of frequencies, out to some value $\omega_H$. We write this schematically as

:::{math}
:label: eq-adiab-22
\omega_H \sim {\dot H \over H}.
:::

Note that $\omega_H$ is $O(\epsilon)$ by our assumptions; the time-dependence of the Hamiltonian is slow. On the other hand, the resonance frequency between states $n$ and $m$ is $(E_n-E_m)/\hbar$, and if this comparable to $\omega_H$, then we expect the time-dependence of $H$ to induce transitions. Thus, we can say that the condition for the validity of the adiabatic theorem is

:::{math}
:label: eq-adiab-23
{\dot H \over H} \ll {|E_n - E_m| \over \hbar}.
:::

This should be true of all states $n$ and $m$ of interest; for example, if we choose the initial conditions {eq}`eq-adiab-13`, we can set $n=N$ and $m=N\pm 1$, since it is the nearest neighbors to eigenvalue $E_N$ that are in greatest danger of violating the condition {eq}`eq-adiab-23`.

We turn now to the gauge structure that is inherent in adiabatic theory. To begin, we shift emphasis slightly, and imagine that the time-dependence of $H$ takes place through a set of parameters $\Rvec=(R_1,R_2,\ldots)$ that themselves are slow functions of time, so that $H=H(\Rvec)$ and $\Rvec=\Rvec(\tau)$. A useful example to keep in mind is that of a spin in a slowly varying magnetic field, for which

:::{math}
:label: eq-adiab-24
H=-\muvec \cdot \Bvec(\tau).
:::

In this example, we can identify the parameters $\Rvec$ with the magnetic field $\Bvec$, so that parameter space is the same as “magnetic field space,” and is 3-dimensional. By the condition {eq}`eq-adiab-22`, the time dependence of this Hamiltonian is slow enough for the adiabatic theorem to hold if it is slow in comparison to the spin precession frequency, $\mu B/\hbar$.

More generally, we imagine some parameter space of some dimensionality with coordinates $\Rvec$, and we imagine finding the energy eigenvalues and eigenkets as functions of $\Rvec$, according to

:::{math}
:label: eq-adiab-25
H(\Rvec) \ket{n(\Rvec)} = E_n(\Rvec) \ket{n(\Rvec)}.
:::

We think of the energy eigenvalues and eigenkets as fields over parameter space (scalar and ket fields, respectively). We assume that the eigenvalues are discrete and nondegenerate over some region of parameter space of interest; this implies that the eigenvalues are smooth functions of $\Rvec$ (assuming the dependence of $H$ on $\Rvec$ is smooth). Later we worry about what happens at degeneracies. Likewise, we assume the eigenkets $\ket{n(\Rvec)}$ can be defined in a smooth and continuous manner in the region of parameter space of interest. This will be possible if the region in question is contractible and contains no degeneracies, as we assume. (But Born-Oppenheimer theory gives rise to some interesting applications where these assumptions are not met.) Of course, the eigenkets are only defined to within a phase factor by {eq}`eq-adiab-25`; when we write $\ket{n(\Rvec)}$, we assume some phase conventions have been chosen for each value of $\Rvec$, in a smooth manner.

Now the history of the Hamiltonian under the adiabatic process can be described by a curve $\Rvec=\Rvec(\tau)$ in parameter space, which starts at some point $\Rvec_0$ and ends and some point $\Rvec_1$. The curve is fixed in parameter space, but is traversed ever more slowly as $\epsilon\to0$. Quantities such as the eigenkets change along the curve according to

:::{math}
:label: eq-adiab-26
\dod{}{\tau} \ket{n(\Rvec)} = \del\ket{n(\Rvec)} \cdot \dod{\Rvec}{\tau},
:::

where $\del=\partial/\partial\Rvec$. Then we can write the geometric phase [see {eq}`eq-adiab-19`] in terms of the line integral of a certain vector field in parameter space,

:::{math}
:label: eq-adiab-27
\gamma = i\int_0^\tau \matrixelement{n}{\del}{n} \cdot \dod{\Rvec}{\tau'} \, d\tau' = \int_{\Rvec_0}^{\Rvec_1} \Avec(\Rvec) \cdot d\Rvec,
:::

where

:::{math}
:label: eq-adiab-28
\Avec(\Rvec) = i\matrixelement{n(\Rvec)}{\del}{n(\Rvec)}.
:::

In this equation, the vector field $\Avec(\Rvec)$ is associated with the state $n$ in question, and sometimes we might prefer to write $\Avec_n(\Rvec)$ to emphasize this. The line integral in {eq}`eq-adiab-27` is taken along the given curve in parameter space (the history of the Hamiltonian). The vector field $\Avec(\Rvec)$ is the vector potential or *gauge potential* for the problem, and is analogous to the vector potential in ordinary electromagnetic theory, as suggested by the notation. We see that all dependence on the time parameterization has dropped out in the final expression in {eq}`eq-adiab-27` for the geometric phase, and that this phase is independent of the rate at which the curve in parameter space is traversed, as long as it is slow enough for the adiabatic theorem to be valid. It is for this reason that this phase is called “geometric.”

The gauge transformations in this theory are changes in the phase conventions for the eigenkets $\ket{n(\Rvec)}$. Such a change in phase conventions will be indicated by

:::{math}
:label: eq-adiab-29
\ket{n(\Rvec)} \to \ket{\tilde n(\Rvec)} = e^{ig(\Rvec)} \ket{n(\Rvec)},
:::

here the tilde indicates the new phase conventions. Of course there is no physics in these phase conventions, so all physical results must be gauge-invariant. This is just as in electromagnetic theory. The gauge scalar $g$ in {eq}`eq-adiab-29` is allowed to be a function of $\Rvec$, because there is no reason why we cannot change the phase in a different manner for different parameter values. The $\Rvec$-dependence of the gauge scalar is what qualifies these gauge transformations as “local.” In gauge theories, only local gauge transformations are at all nontrivial or interesting. Of course, for a given eigenket $\ket{n(\Rvec)}$ (for a given value of $\Rvec$ and a given phase convention), there is no meaning to talking about the “phase” of the eigenket in any absolute sense. For example, if the ket is associated with a wave function $\psi_n(\rvec) = \braket{\rvec}{n}$, then $\psi_n$ is in general a complex function of position $\rvec$, with different phases at different points. On the other hand, the relative phase of two kets that are proportional to one another is well defined.

Since all physical results must be gauge-invariant, we should examine all the quantities of our theory to see how they transform under gauge transformations. For example, the eigenvalues $E_n$ and the dynamical phases $\phi_n$ are clearly gauge-invariant, whereas the eigenkets $\ket{n}$ are not [they transform according toifone {eq}`eq-adiab-29`]. Nor is the gauge potential gauge-invariant, for by substitutingifone {eq}`eq-adiab-29` into {eq}`eq-adiab-28`, we find

:::{math}
:label: eq-adiab-30
\Avec(\Rvec) \to \tilde \Avec(\Rvec) = \Avec(\Rvec) - \del g(\Rvec),
:::

which is just as in electromagnetic theory. From this we find that the geometric phase is not gauge-invariant, either, but rather transforms according to

:::{math}
:label: eq-adiab-31
\gamma(t) \to \tilde\gamma(t) = \gamma(t) - g\bigl(\Rvec(\tau)\bigr) + g\bigl(\Rvec(0)\bigr),
:::

as follows from {eq}`eq-adiab-27`. But the solution $\ket{\psi(t)}$ to the Schr\"odinger equation for given initial conditions $\ket{\psi(0)}$ should be gauge-invariant simply because the solution to the Schr\"odinger equation is unique. Indeed, if we combine {eq}`eq-adiab-13`, {eq}`eq-adiab-21`, {eq}`eq-adiab-29` and {eq}`eq-adiab-31`, we see that the gauge-dependence of $\gamma(t)$ is required to cancel that of $\ket{n(\Rvec)}$ and to make $\ket{\psi(t)}$ gauge-invariant. This gives us another reason for carrying out the $\epsilon$ expansion through the geometric phase, since without it the results do not transform properly under gauge transformations.

A special case of interest is one in which the system is carried through a cycle, so that the Hamiltonian returns to its original self after time $t$. In this case the curve in parameter space $\Rvec(\tau)$ is closed, and we can apply Stokes' theorem to the integral {eq}`eq-adiab-27` for the geometric phase. This gives

:::{math}
:label: eq-adiab-32
\gamma = \oint \Avec(\Rvec)\cdot d\Rvec = \int_S \Vvec \cdot d\Svec,
:::

where the surface $S$ is a surface in parameter space bounded by the closed curve, and where

:::{math}
:label: eq-adiab-33
\Vvec(\Rvec) = \del\cross\Avec(\Rvec).
:::

Here we are assuming that parameter space is 3-dimensional, so we can use the standard notation of vector calculus for Stokes' theorem. In parameter spaces of other dimensionalities, it is necessary to use differential forms, but all the important ideas are conveyed by the 3-dimensional case. Obviously, $\Vvec$ is analogous to the magnetic field in electromagnetic theory, and satisfies the field equation,

:::{math}
:label: eq-adiab-34
\del\cdot\Vvec = 0.
:::

The vector field $\Vvec$ is sometimes called the *curvature form* of the gauge theory.

Notice that for closed curves in parameter space, the gauge-dependence of $\gamma$ seen in {eq}`eq-adiab-31` cancels out, and the geometric phase becomes gauge-invariant. The same conclusion follows from the gauge-invariance of the vector field $\Vvec$,

:::{math}
:label: eq-adiab-35
\tilde\Vvec(\Rvec) = \Vvec(\Rvec),
:::

which appears in the surface integral in {eq}`eq-adiab-32`. In physical terms, the geometric phase must be gauge-invariant for a closed cycle, because if the final state is proportional to the initial state, as it must be according to the adiabatic theorem, then the relative phases of the two states can be determined by interference experiments.

To return to the case of open curves in parameter space, we might be tempted to say that this geometrical phase is just a nuisance that is due to a poor choice of phase conventions. After all, $\gamma$ is gauge-dependent, so perhaps it is completely nonphysical. Suppose, for example, we return to {eq}`eq-adiab-21`, which was derived under the assumption that some phase conventions had been chosen for $\ket{n(\tau)}$ as a function of time along the history of the Hamiltonian, and use it to write the solution {eq}`eq-adiab-8` in the form,

:::{math}
:label: eq-adiab-36
\ket{\psi(t)} = \sum_n e^{i[\phi_n(t)+\gamma_n(\tau)]} \, c_n(0) \ket{n(\tau)}.
:::

Now we say, the kets $\ket{n(\tau)}$ involved a poor choice of phase, because they gave us a nonvanishing $\gamma$; suppose we choose a different phase convention,

:::{math}
:label: eq-adiab-37
\ket{\tilde n(\tau)} = e^{i\gamma_n(\tau)} \, \ket{n(\tau)}.
:::

Then the geometrical phase disappears from the solution,

:::{math}
:label: eq-adiab-38
\ket{\psi(t)} = \sum_n e^{i\phi_n(t)} \ket{\tilde n(\tau)},
:::

and it seems that we do not have to worry about gauge transformations or gauge dependence. And yet, if the history of the Hamiltonian should take us back to the initial Hamiltonian, so that the curve in parameter space becomes closed, then the phase convention {eq}`eq-adiab-37` no longer works, because we have one Hamiltonian $H_0=H_1$ with two different phase conventions. In other words, the phase convention {eq}`eq-adiab-37` introduces a discontinuity in the definition of the eigenkets when we go around a closed loop in parameter space. This discontinuity is nothing but the geometrical phase associated with the loop; this phase is gauge-invariant and cannot be banished by some clever choice of phase convention.

Therefore it is better to say that the phases of the energy eigenstates, while they do contain a nonphysical element that can be established only by convention, also contain a physical element that is manifest on carrying an adiabatic process around a closed cycle. This is just as in electromagnetic theory, where the integral $\oint \Avec\cdot d\rvec$ is the gauge-invariant magnetic flux associated with a closed loop.

At this point you might want to think through a specific problem involving the geometric phase, for example a spin in a slowly varying magnetic field as in {eq}`eq-adiab-24`.

We now turn to some comments about the Born-Oppenheimer approximation, which is the basic approximation scheme in the theory of molecules, and which relies crucially on notions of adiabaticity. A precise and careful treatment of Born-Oppenheimer theory is a fascinating subject that must lie outside the scope of this course; the following discussion merely aims to present some of the simplest ideas.

Suppose we have a molecule consisting of some number of electrons and some number of nuclei. We will label the electrons with indices $i$, $j$, etc., and the nuclei with indices $\alpha$, $\beta$, etc. Let the positions, momenta, and mass of the electrons be $\rvec_i$, $\pvec_i$, and $m$, and let the positions, momenta, masses, and charges of the nuclei be $\Rvec_\alpha$, $\Pvec_\alpha$, $M_\alpha$, and $Z_\alpha$. The notation attempts to use capital letters for nuclei, and lower case letters for electrons. Then the basic Coulomb Hamiltonian for the molecule is

:::{math}
\begin{aligned}
H_molec &= T_n + T_e + V_{ee} + V_{en} + V_{nn}
\end{aligned}
:::

:::{math}
\begin{aligned}
&= \sum_\alpha {\Pvec_\alpha^2 \over 2M_\alpha} + \sum_i {\pvec_i^2 \over 2m} + \sum_{i<j} {e^2 \over |\rvec_i - \rvec_j|} - \sum_{i\alpha} {Z_\alpha e^2 \over |\rvec_i-\Rvec_\alpha|}
\end{aligned}
:::

:::{math}
:label: eq-adiab-39
\begin{aligned}
&+ \sum_{\alpha<\beta} {Z_\alpha Z_\beta e^2 \over |\Rvec_\alpha - \Rvec_\beta|},
\end{aligned}
:::

where $T_n$ and $T_e$ are the nuclear and electronic kinetic energies, and where $V_{ee}$, $V_{en}$, and $V_{nn}$ are the potential energies of interactions of electrons with electrons, electrons with nuclei, and nuclei with nuclei, respectively. This Hamiltonian is very complicated, and it must be handled by some approximation scheme.

The Born-Oppenheimer approximation relies on the large disparity in the masses of the electrons and the nuclei, which have a ratio of the order of $10^{-4}$ for most nuclei. This means that if the kinetic energies of the electrons and nuclei are not too dissimilar, then the velocities of the electrons will be much higher than those of the nuclei, and we can picture the electron motion as being rapid in comparison to the nuclear motion. Thus, while the heavy nuclei move a short distance, the electrons will whiz around the nuclei or back and forth between them many times, effectively filling out an electron cloud. (This picture is a metaphor of constructed of classical and quantum language, but it does convey many ideas correctly.)

In a rigorous and precise treatment of the Born-Oppenheimer approximation, one expands the molecular Hamiltonian in powers of the small parameter $\kappa \sim (m/M)^{1/4}$, which is of the order of $10^{-1}$ for most molecules. This expansion is nontrivial because the scale lengths of the wave functions themselves with respect to the nuclear and electronic coordinates are different, and in particular, involve different powers of $\kappa$. Thus, the $\kappa$ ordering is not merely in the Hamiltonian, but also in the spatial dependence of the wave functions.

As a result of this expansion, one finds that the spectrum of the molecular Hamiltonian possesses three distinct energy scales. The largest is that of electronic excitations, involving energies $E_elec$ which are of the order of $e^2/a_0$, where $a_0$ is the Bohr radius. The next smaller energy scale is that of the vibrational motions of the molecule, in which the separation between energy levels is of the order of $E_vib \sim \kappa^2 E_elec$. Finally, the smallest energy scale is that of the rotations of the molecule, in which the separation between energy levels (for small angular momenta) is of the order of $E_rot \sim \kappa^2 E_vib \sim \kappa^4 E_elec$. This ordering of energy scales is easy to understand from a qualitative standpoint, as was discussed in class last semester.

In the present discussion we will take a simpler approach, but one that captures many of the ideas of the more sophisticated theory. Let us argue that since the nuclei are heavy and slow moving, we can treat them by classical mechanics, while the electrons, which are light, fast, and not easily localized due to the constraints of the uncertainty principle, must be treated by quantum mechanics. Thus, we will treat $\Rvec_\alpha$ and $\Pvec_\alpha$ in {eq}`eq-adiab-39` as $c$-numbers, which presumably obey some classical equations of motion that endow them with some time dependence, and we will treat $\rvec_i$ and $\pvec_i$ as operators acting on wave functions for the electrons. This is a hybrid classical-quantum approach.

We now define the electronic Hamiltonian $H_elec$ as the last four terms in {eq}`eq-adiab-39`, which depends on the operators $\rvec_i$ and $\pvec_i$ and on the nuclear positions $\Rvec_\alpha$, which are $c$-numbers. We adopt an abbreviated notation, in which $\rvec$ stands for all electron coordinates $\rvec_i$, $\Rvec$ stands for all nuclear coordinates $\Rvec_\alpha$, etc.:

:::{math}
:label: eq-adiab-40
H_elec(\rvec,\pvec;\Rvec) = \sum{\pvec^2\over 2m} + V_{ee}(\rvec) + V_{en}(\rvec,\Rvec) +V_{nn}(\Rvec).
:::

Since $\Rvec=\Rvec(t)$ is supposedly a slow function of time, $H_elec$ is an example of a Hamiltonian with a slow time dependence, in which the nuclear coordinates $\Rvec$ are the slow parameters. The parameter space is now the nuclear configuration space. Notice that the internuclear potential energy $V_{nn}(\Rvec)$ is a $c$-number, and is just a constant insofar as the electronic operators are concerned; but we include it anyway in the electronic Hamiltonian.

The adiabatic theorem tells us to look at the eigenfunctions of $H_elec$ for fixed values of the parameters $\Rvec$. Physically, this means that we fix or freeze the locations of the nuclei, and then solve for the electronic eigenfunctions and eigenvalues at the given nuclear locations. This problem is similar to atomic structure calculations, except that that the electrons are attracted to two or more fixed centers, instead of just one.

Let the eigenfunctions and eigenvalues of $H_elec$ for fixed values of $\Rvec$ be $\phi_n(\rvec;\Rvec)$ and $E_n(\Rvec)$, where the dependence on the parameters $\Rvec$ is just as in {eq}`eq-adiab-25`, so that

:::{math}
:label: eq-adiab-41
H_elec(\rvec,\pvec;\Rvec) \phi_n(\rvec;\Rvec) = E_n(\Rvec) \phi_n(\rvec,\Rvec).
:::

As indicated by the $\Rvec$-dependence, these eigenfunctions and eigenvalues change as the nuclei move around. However, in accordance with the adiabatic theorem, we expect that if the system is prepared in a given electronic eigenstate at some initial time, it will remain in the eigenstate with the same quantum number as $\Rvec$ slowly changes, even if the corresponding eigenfunction and energy should change by a substantial amount. For example, at large distances where two atoms do not interact, the electronic wave functions will be those of two independent atoms; but when the atoms approach one another, the electron clouds will distort and overlap and electrons will begin to be exchanged between the two atoms. But as long as the electronic energy levels do not come too close to one another, we expect the probability of being in a given electronic eigenstate to be independent of time.

[In fact, in important cases, the electronic eigenvalues do come close to one another, and one must consider the transitions due to the breakdown of adiabaticity. Such transitions are called *Landau-Zener* transitions, and are responsible for changes in electronic states in slow atomic or molecular collisions.]

Since the electronic energies change as $\Rvec$ changes, the energy difference must come from somewhere, and it is logical that it comes from the nuclear kinetic energy. In other words, the electronic eigenenergy $E_n(\Rvec)$ plays the role of a potential energy for the nuclear motion. Thus, we can take the classical Hamiltonian for the nuclear motion to be

:::{math}
:label: eq-adiab-42
H_cl(\Rvec,\Pvec) = \sum{\Pvec^2\over 2M} + E_n(\Rvec) = \matrixelement{\phi_n}{H_molec}{\phi_n},
:::

which is otherwise just the expectation value of the total molecular Hamiltonian $H_molec$ with respect to the $n$-th electronic energy eigenstate, as indicated. We see that there is a different nuclear classical Hamiltonian for each electronic energy level; as one says, there is a different “potential energy surface” $E_n(\Rvec)$ for each electronic state.

In a more careful treatment of the Born-Oppenheimer approximation, in which the nuclear degrees of freedom are treated by quantum mechanics, one finds exactly the Hamiltonian {eq}`eq-adiab-42` at lowest order in the perturbation parameter $\kappa$, except that it is now a quantum Hamiltonian. At the next order, one finds that the gauge potential $\Avec(\Rvec)$ associated with adiabatic transport of the electronic eigenfunctions is incorporated into the nuclear Hamiltonian, giving pseudo-magnetic effects. These include phase shifts similar to those in the Aharonov-Bohm effect that have observable effects on scattering cross s and molecular energy levels.

The notion that the electronic eigenvalue is the potential energy for the nuclear motion leads to an immediate understanding of the nature of the chemical bond. The example of the $H_2$ molecule will be discussed in class.

\problems

(prob-adiab-1)=

**Problem \prbdadiab-1..** 

:::{math}
:label: eq-adiab-43
H = -k \Svec\cdot\Bvec(\tau),
:::

where $k$ is a constant and $\Bvec$ is a function of the slow time variable, $\tau=\epsilon t$. Allow the spin $s$ to take on any value, $s=0,\frac{1}{2},1,\ldots$. Identify parameter space with magnetic field space. Try to find a smooth assignment of eigenkets $\ket{m(\Bvec)}$ over all of parameter space, where $m=-s,\ldots,+s$. Show that it is possible to make such an assignment in a smooth manner everywhere in parameter space except on the negative $B_z$-axis. Compute the gauge potential $\Avec(\Bvec)$, and the curvature form $\Vvec$. Suppose the magnetic field $\Bvec(\tau)$ slowly traces out some closed curve in parameter space, not passing through the origin $\Bvec=0$. Both the magnitude and direction of $\Bvec$ are allowed to change. Show that the geometric phase $\gamma$ is proportional to the solid angle subtended by this curve as seen from the origin, and find the constant of proportionality. (Note that there is actually a different gauge potential and geometric phase for each value of $m$.)

(prob-adiab-2)=

**Problem \prbdadiab-2..** 

Consider a hydrogen atom in an external electric field. The field is produced by some experimental apparatus, so the scale length $L$ of the field is much greater than the size $\ell$ of the atom. However, the field is not uniform. The physics of the situation is that the external field polarizes the atom, so that the atom is attracted to regions of higher field strength. In this way, an electric field gradient can be use to deflect neutral atomic beams.

\problempart{(a)} Write out the Hamiltonian for the atom, regarded as a proton-electron system, in some inertial frame. Transform to the center of mass position $\Rvec$ and relative position $\rvec$, and expand the potential energy in powers of $\ell/L$ out to the first nonvanishing term. (Let $\rvec$ be the electron position relative to the proton.) Notice that because of the electric field, this Hamiltonian is not separable; thus, the wave function $\Psi(\rvec,\Rvec)$ cannot be written as a product of functions of $\rvec$ and $\Rvec$ separately.

\problempart{(b)} Now define a Hamiltonian $H_atom (\rvec ,\pvec ;\Rvec)$ which is parameterized by the center of mass position $\Rvec$. (This Hamiltonian contains all the terms in the total Hamiltonian except the center of mass kinetic energy). Notice that it has the form of a Stark Hamiltonian for hydrogen. Let the eigenfunctions and eigenvalues of this Hamiltonian be $u_n(\rvec;\Rvec)$ and $E_n(\Rvec)$, respectively.

Although the exact wave function $\Psi(\rvec,\Rvec)$ cannot be factored into a product of functions of $\rvec$ and $\Rvec$ separately, its $\rvec$ dependence can certainly be expanded as a linear combination of the $u_n(\rvec;\Rvec)$, which form a complete set of functions of $\rvec$ for each value of $\Rvec$. Let the expansion coefficients be $\phi_n$; these must be functions of the parameters $\Rvec$. Thus, without loss of generality, we can write

:::{math}
:label: eq-adiab-44
\Psi(\rvec,\Rvec)=\sum_n \phi_n(\Rvec) u_n(\rvec;\Rvec).
:::

Actually, for hydrogen, the excited states $n\ne0$ would quickly emit a photon and drop into the ground state $n=0$; this would even apply to the $2s$ state, due to the quenching ($2s$-$2p$ mixing) caused by the electric field. Therefore we need only include the $n=0$ term in {eq}`eq-adiab-44`, and we can write

:::{math}
:label: eq-adiab-45
\Psi(\rvec,\Rvec) = \phi(\Rvec) u_0(\rvec;\Rvec),
:::

where we write simply $\phi$ for $\phi_0$.

We will be interested in solving the time-dependent Schr\"odinger equation for $\Psi(\rvec,\Rvec,t)$, since we are thinking of atoms in a beam. Therefore we allow $\phi$ in {eq}`eq-adiab-45` to depend on $t$, $\phi=\phi(\Rvec,t)$. But $u_0$ does not depend on $t$, because it is just an $\Rvec$-dependent eigenfunction of $H_atom$. Substitute the given form for $\Psi$ into the time-dependent Schr\"odinger equation, multiply through by $u_0^\cc$ and integrate over $\rvec$. Show that the result is a new Schr\"odinger equation for $\phi(\Rvec,t)$ which has the form

:::{math}
:label: eq-adiab-46
{1\over 2M} [\Pvec - \hbar\Avec(\Rvec)]^2 \phi + G(\Rvec)\phi +E_n(\Rvec)\phi = i\hbar\frac{\partial \phi}{\partial t},
:::

where $M$ is the total mass of the atom, $\Avec$ is the gauge potential associated with adiabatic transport of the ground state wave function,

:::{math}
:label: eq-adiab-47
\Avec(\Rvec) = i\matrixelement{u_0}{\del_\Rvec}{u_0},
:::

and where

:::{math}
:label: eq-adiab-48
G(\Rvec) = {\hbar^2\over 2M} \sum_{n\ne0} |\matrixelement{u_n}{\del_\Rvec}{u_0}|^2.
:::

\problempart{(c)} Explain why, for hydrogen in the physical situation described, $\Avec(\Rvec)=0$. Hint: It would not be true if there were also a magnetic field.

\problempart{(d)} The term $G$ is normally very small and can be neglected. Use the results of second order perturbation theory for the Stark effect (see {ref}`ch-stark`) to write down the effective potential energy seen by the atom as a whole. The function $\phi(\Rvec)$ is the “wave function of the atom.”
