---
title: "25. Fine Structure in Hydrogen and Alkali Atoms"
---
(ch-finestruc)=

# 25. Fine Structure in Hydrogen and Alkali Atoms

(sec-finestruc-1)=

## Introduction

In these notes we consider the fine structure of hydrogen-like and alkali atoms, which concerns the effects of relativity and spin on the dynamics of the electron. Both these effects are of the same order of magnitude, and must be treated together in any realistic treatment of the atomic structure. In fact, spin itself may be thought of as a fundamentally relativistic phenomenon, although in low energy applications it is usually treated within a nominally nonrelativistic framework by the inclusion of extra terms in the Schr\"odinger equation. This is the approach we shall take in these notes, where we treat the fine structure terms as perturbations imposed on the simple electrostatic model we have considered so far. The fine structure terms account for relativistic effects through order $(v/c)^2$, and have the effect of enlarging the Hilbert space by the inclusion of the spin degrees of freedom, introducing new quantum numbers, and shifting and splitting the energy levels of the electrostatic model. The splitting in particular means that spectral lines that appear as singlets under low resolution become closely spaced multiplets under higher resolution (hence the term “fine structure”). The fine structure was known experimentally long before a proper theoretical understanding was achieved, and was an important driving force in theoretical developments at a certain stage in the history of atomic physics. In addition to its intrinsic interest and importance in atomic physics, the fine structure is interesting as a window on relativistic quantum mechanics.

(sec-finestruc-2)=

## The Hamiltonian

Our unperturbed system is a single-electron atom, hydrogen, hydrogen-like or alkali, in the electrostatic model. The unperturbed Hamiltonian is

:::{math}
:label: eq-finestruc-1
H_0 ={p^2\over2m} +V(r),
:::

where we ignore the small difference between the true electron mass and the reduced mass. As for the potential, for hydrogen-like atoms it is

:::{math}
:label: eq-finestruc-2
V(r)=-{Ze^2\over r},
:::

whereas for alkalis it is the central force potential in the model discussed in {ref}`sec-hydrogen-9`.

Now we add to $H_0$ the fine structure corrections, of which there are three: the relativistic kinetic energy correction, the Darwin term, and the spin-orbit term. We write the fine structure Hamiltonian as

:::{math}
:label: eq-finestruc-3
H_FS = H_RKE + H_D + H_SO,
:::

which we will treat as a perturbation, to be added to the unperturbed Hamiltonian {eq}`eq-finestruc-1`. We will discuss these terms one at a time, giving an idea of their physical significance.

(sec-finestruc-3)=

## The Relativistic Kinetic Energy Correction

Let us recall recall that the energy of a relativistic particle (rest mass plus kinetic energy) is

:::{math}
:label: eq-finestruc-4
\sqrt{m^2c^4 + c^2p^2} = mc^2 + {p^2\over 2m} -{p^4\over 8m^3c^2} + \ldots,
:::

where we have expanded the square root in powers of the momentum, assuming $p \ll mc$. The first term is the rest mass, the second is the nonrelativistic kinetic energy, and the third is the correction,

:::{math}
:label: eq-finestruc-5
H_RKE = -{p^4\over 8m^3 c^2}.
:::

(sec-finestruc-4)=

## The Spin-Orbit Correction

The spin-orbit term has the form,

:::{math}
:label: eq-finestruc-6
H_SO = -{1\over2} \muvec\cdot\Bvec',
:::

where $\muvec$ is the usual magnetic moment of the electron and $\Bvec'$ is the magnetic field as seen in the electron rest frame (the prime refers to this frame). In the case of hydrogen, this magnetic field can be understood as due to the positive charge of the nucleus, which from the electron's rest frame appears to be orbiting the electron, creating a current loop. In the case of the alkalis, the core electrons are also orbiting the valence electron, as seen in the rest frame of the valence electron, and contribute to the magnetic field in that frame.

Of course, the electron is accelerated, so its rest frame is not an inertial frame. This means that the simple picture we have described to explain the magnetic field in that frame does not give full accounting of the physics involved. In particular, it turns out that in relativity theory, an accelerated frame is associated with a rotation, called Thomas precession, which has an effect on the form of the spin-orbit interaction.

From another point of view, $\Bvec'$ can be understood as the magnetic field that appears when we Lorentz transform the electrostatic field in the rest frame of the nucleus (what we may think of as the “lab” frame) to the frame of the electron. We will assume that there is no magnetic field in the “lab” frame. Actually, if the nucleus has a nonzero spin, then it produces a magnetic dipole field, which is responsible for the hyperfine interactions studied in {ref}`ch-hyperfine`. But even when present, this dipole field is much smaller than the field $\Bvec'$ responsible for the spin-orbit effects, so we shall ignore it here. Thus, using unprimed symbols $\Evec$, $\Bvec$ for the “lab” frame, we have

:::{math}
:label: eq-finestruc-7
\Evec = -\del\Phi = {1\over e} \del V ={1\over e} {1\over r}\dod{V}{r}\xvec, \qquad \Bvec=0,
:::

where we have used $V=-e\Phi$.

Now let $\vvec$ be the velocity of the electron as seen in the “lab” frame, and $\gamma$ the usual factor of time dilation in relativity,

:::{math}
:label: eq-finestruc-8
\gamma={1\over \sqrt{1-(v/c)^2}} = 1+{1\over2}{v^2\over c^2} + \ldots,
:::

where we have expanded $\gamma$ in powers of $v/c$. Then according to special relativity the electric and magnetic fields $\Evec'$ and $\Bvec'$ seen in the frame moving with velocity $\vvec$ with respect to the lab frame are given by

:::{math}
:label: eq-finestruc-9
\begin{aligned}
\Evec'&=\gamma\Evec - (\gamma-1){(\vvec\cdot\Evec)\vvec\over v^2} + \gamma{\vvec\over c} \cross \Bvec, \\
\Bvec'&=\gamma\Bvec - (\gamma-1){(\vvec\cdot\Bvec)\vvec\over v^2} - \gamma{\vvec\over c} \cross \Evec. \\

\end{aligned}
:::

[See Jackson, *Classical Electrodynamics*, 3rd ed., Eq.~(11.149).] This is the general expression for the Lorentz transformation of electric and magnetic fields between two frames, but the formulas simplify quite a bit for our application, for which $\Bvec=0$. Also, we are only interested in these formulas to lowest order in $v/c$, which according to {eq}`eq-finestruc-8` means that we can approximate $\gamma\approx 1$ and drop the terms involving $(\gamma-1)$. This is because the spin-orbit term is already a small correction to the energy of the hydrogen atom, of order $(v/c)^2$ compared to the nonrelativistic energies. The result is

:::{math}
:label: eq-finestruc-10
\begin{aligned}
\Evec'&=\Evec, \\
\Bvec'&=-{\vvec\over c} \cross \Evec. \\

\end{aligned}
:::

Now writing $\pvec = m\vvec$ and using {eq}`eq-finestruc-7`, we have

:::{math}
:label: eq-finestruc-11
\Bvec' = {1\over emc} {1\over r}\dod{V}{r} \Lvec,
:::

where $\Lvec = \xvec\cross \pvec$. Then with

:::{math}
:label: eq-finestruc-12
\muvec = -{e \over mc} \Svec,
:::

where we approximate $g \approx 2$, {eq}`eq-finestruc-6` becomes

:::{math}
:label: eq-finestruc-13
H_SO = {1 \over 2 m^2 c^2} {1 \over r} \dod{V}{r} \Lvec \cdot \Svec.
:::

The only remaining question is why there is a factor of $\frac{1}{2}$ in {eq}`eq-finestruc-6`. We usually write the energy of a magnetic dipole in a magnetic field as $-\muvec\cdot\Bvec$. This factor is due to Thomas precession, a purely inertial effect of special relativity that causes accelerated frames to rotate relative to inertial frames. As we saw in {ref}`sec-spinmagf-8` (see also Prob.~\jjcouple.1), inertial effects in a rotating frame can enhance or cancel out the effects of a magnetic field; in the present case, one half of the field $\Bvec'$ is canceled.

Thomas precession is an interesting part of a study of special relativity, but it is probably overkill to go into it too deeply here, because the correct expression for the spin-orbit term, including the Thomas factor of $\frac{1}{2}$, emerges automatically from the Dirac equation, which we will take up later in the course. For those who are curious, I have given a geometrical treatment of Thomas precession in my notes

{\tt http://bohr.physics.berkeley.edu/classes/209/f02/thomprec.pdf}

To summarize, the spin-orbit term is the magnetic energy of interaction of the spin with the magnetic field produced by the moving nucleus, corrected for Thomas precession.

(sec-finestruc-5)=

## The Darwin Term

The Darwin term is not as easy to interpret as the other two fine structure terms, but it can be described as a certain nonlocality in the interaction of the electron with the electrostatic field described by the potential $V$. The following is a rough description of the physics lying behind the Darwin term.

If we confine an electron to a box of width $L$, then by the uncertainty principle the momentum takes on values of the order of $\hbar/L$. If $L$ is small enough, we can make this momentum as large as we like, even relativistic values. Setting $p=mc$, a characteristic momentum at which relativistic effects are significant, and solving for $L$, we obtain

:::{math}
:label: eq-finestruc-14
L = \lambda_C = {\hbar \over mc},
:::

where we now write $\lambda_C$ for the length in question, which is called the *Compton wave length*. This is the distance scale below which the effects of relativistic quantum mechanics are important. This length can be defined for any particle, but in the case of the electron we have

:::{math}
:label: eq-finestruc-15
\lambda_C = \alpha a_0 \approx 3\times 10^{-11} cm,
:::

where $\alpha$ is the fine structure constant and $a_0$ is the Bohr radius. The electron Compton wave length is about $1/137$ times the size of the atom. Notice that this is still substantially larger than the size of the nucleus, $\approx 10^{-13} cm$.

:::{figure} images/finestruc-fig01.png
:label: fig-finestruc-1
:width: 80%

Feynman diagram for the creation of an electron-positron pair in the orbital motion of an electron in the hydrogen atom. The diagram is a space-time diagram with time increasing vertically, with the world-lines of the nucleus and electrons and a positron shown. Starting at the bottom, the electron in orbit around the nucleus enters at the left. Electron world-lines are indicated with an arrow pointing in the direction of increasing time. Later, at space-time point $A$, a photon from the nucleus creates a positron electron pair, so that for a time there exist two electrons and one positron in the system. The positron world line is indicated with an arrow pointing backwards in time. At a later time, at space-time point $B$, the incoming electron annihilates with the positron, producing a photon that is absorbed by the nucleus. After this, a single electron continues in its orbit, but, in a sense, it is not the same electron that entered at the bottom. The effect of diagrams like this is to smear the position of the atomic electron around in space over a distance comparable to the Compton wavelength.
:::

If an electron is confined to a distance of order of the Compton wave length, then the corresponding momentum implied by the uncertainty principle implies an energy comparable to $mc^2$, the rest mass-energy of the electron. Then processes such as pair creation become possible, that is, the reaction,

:::{math}
:label: eq-finestruc-16
e^{-} \to e^{-} + e^{-} + e^{+},
:::

where $e^{-}$ is the electron and $e^{+}$ is the positron. Such reactions do not literally occur inside an atom because there is not enough energy (a minimum of $2mc^2$) to create a positron-electron pair. But states containing two electrons and a positron do appear virtually, that is, for a period of time short enough that the violation of conservation of energy cannot be noticed (that is, times less than $\hbar/2mc^2$). From another point of view, such virtual states appear in perturbation theory when one sums over “intermediate states,” which derive ultimately from a resolution of the identity. Such a sum can be seen in {eq}`eq-pertth-8`, the expression for the resolvent operator.

The positron-electron pair created according to {eq}`eq-finestruc-16` survives for a time of order $\hbar/mc^2$, so, traveling at a velocity comparable to the speed of light, the particles cover a distance of order $\hbar/mc =\lambda_C$ before disappearing again. The effect is to smear out the position of the atomic electron over a distance of order $\lambda_C$. The Feynman diagram for this process is shown in {ref}`fig-finestruc-1`.

To model this, let $f(\svec)$ be a smearing function, normalized so that

:::{math}
:label: eq-finestruc-17
\int d^3\svec \, f(\svec) = 1.
:::

The smearing function should be a positive function concentrated about $\svec=0$ with a width comparable to $\lambda_C$. Then the effective energy of interaction of the electron with a potential $V$ at position $\xvec$ is not $V(\xvec)$, but rather

:::{math}
:label: eq-finestruc-18
\int d^3\svec \, f(\svec) V(\xvec+\svec).
:::

Assuming that $V$ is slowly varying on the scale of $f$, we can expand $V(\xvec+\svec)$, obtaining

:::{math}
:label: eq-finestruc-19
\int d^3\svec \, f(\svec) \Bigl[ V(\xvec) + \svec\cdot\del V(\xvec) +{1\over2}\sum_{ij}s_is_j\, {\partial^2 V\over \partial x_i \partial x_j}(\xvec) +\ldots\Bigr]
:::

Because of the normalization {eq}`eq-finestruc-17` the first term is just $V(\xvec)$, the usual expression for the potential energy of an electron at position $\xvec$. Assuming that $f(\svec)$ is rotationally symmetric, that is, $f(\svec) = f(s)$ where $s=|\svec|$, then the first correction term in {eq}`eq-finestruc-19` vanishes. As for the second term, let us assume a Gaussian model for the smearing function,

:::{math}
:label: eq-finestruc-20
f(s) = {1\over \pi^{3/2} \lambda_C^3}\, e^{-s^2/\lambda_C^2},
:::

where the smearing length is the Compton wave length. Then we can do the integrals (see Appendix~\gaussint) for the second order term in {eq}`eq-finestruc-19`,

:::{math}
:label: eq-finestruc-21
\int d^3\svec \, s_is_j\, f(\svec) = {\lambda_C^2 \over 2} \, \delta_{ij}.
:::

Using this in {eq}`eq-finestruc-19` we obtain the energy correction,

:::{math}
:label: eq-finestruc-22
{1\over 4} \lambda_C^2 \del^2 V.
:::

The Darwin term is a term of exactly this form, but with a coefficient of $1/8$ instead of $1/4$:

:::{math}
:label: eq-finestruc-23
H_D = {1\over 8} {\hbar^2 \over m^2 c^2} \del^2 V. `
:::

The Darwin term can be derived (with the correct coefficient) by performing a nonrelativistic expansion on the Dirac equation. See {ref}`ch-foldyw`.

These pseudo-derivations of the fine structure terms are not completely satisfactory, but for now we will just accept them and use them for practice in perturbation theory.

(sec-finestruc-6)=

## Specializing to Hydrogen-like Atoms

To simplify the notation we switch now to atomic units, which were explained in {ref}`sec-hydrogen-3`. See {ref}`tbl-hydrogen-1`. Notice that in atomic units the fine structure constant becomes

:::{math}
:label: eq-finestruc-24
\alpha = {e^2\over \hbar c} = {1\over c} \approx {1\over 137}.
:::

Since the fine structure constant is dimensionless, it has the same value in all systems of units. Thus, the speed of light in atomic units is $c \approx 137$, and the velocity of the electron in the ground state of hydrogen is given by $v_0/c = \alpha \approx 1/137$.

Translating the three fine structure terms, {eq}`eq-finestruc-5`, {eq}`eq-finestruc-13` and {eq}`eq-finestruc-23` to atomic units, we have

:::{math}
:label: eq-finestruc-25a
\begin{aligned}
H_RKE &= -{\alpha^2 \over 8}p^4,
\end{aligned}
:::

:::{math}
:label: eq-finestruc-25b
\begin{aligned}
H_D &= {\alpha^2 \over 8} \del^2 V,
\end{aligned}
:::

:::{math}
:label: eq-finestruc-25c
\begin{aligned}
H_SO &= {\alpha^2 \over 2}{1\over r}\dod{V}{r} \Lvec\cdot\Svec.
\end{aligned}
:::

Notice the common factor of $\alpha^2$ in front of all three terms.

If we evaluate the spin-orbit and Darwin terms explicitly for hydrogen-like atoms, for which $V(r) = -Z/r$, $(1/r)(dV/dr) = Z/r^3$, and $\del^2V = 4\pi Z\delta(\xvec)$, then we obtain

:::{math}
:label: eq-finestruc-26a
\begin{aligned}
H_D &= Z\alpha^2 {\pi \over 2} \, \delta(\xvec),
\end{aligned}
:::

:::{math}
:label: eq-finestruc-26b
\begin{aligned}
H_SO &= {Z\alpha^2 \over 2} {1\over r^3} \Lvec \cdot \Svec.
\end{aligned}
:::

The quantity $Z\delta(\xvec)$ occurring in the Darwin term is the charge density of the nucleus, treated as a point charge. We will henceforth in these notes specialize to the case of hydrogen-like atoms, returning to the case of alkalis briefly at the end.

All three fine structure terms {eq}`eq-finestruc-25a` are multiplied by $\alpha^2$, which is about $5\times 10^{-5}$. As we shall see, these terms all give corrections to the energies of the electrostatic model that are of relative order $(Z\alpha)^2$, which is correspondingly small if $Z$ is not too large. This is what we should expect for relativistic corrections, since the velocity of the electron in the ground state of a hydrogen-like atom is of the order of $(Z\alpha)c$, and we expect relativistic corrections to the energy to go like $(v/c)^2$. Toward the end of the periodic table, however, $Z\alpha$ is no longer so small ($Z\alpha =0.67$ for uranium), and it ceases to be a good approximation to treat relativistic effects as corrections superimposed on a nonrelativistic model. In such heavy atoms the fine structure corrections are becoming comparable to the separation between the levels of the electrostatic model, and it is no longer useful to treat them as perturbations imposed on that model. Instead, it is more useful to start with a proper relativistic treatment of the electron, which is the Dirac equation.

(sec-finestruc-7)=

## The Unperturbed System

We now consider applying $H_{FS}$ as a perturbation to $H_0$. As usual in perturbation theory, we must first understand the unperturbed system. The unperturbed energy levels are

:::{math}
:label: eq-finestruc-27
E_n = -{Z^2\over 2n^2}.
:::

If we ignore spin, the unperturbed eigenstates are $\ket{n\ell m_\ell}$, that is, they are central force wave functions, and they are $n^2$-fold degenerate. However the spin-orbit term {eq}`eq-finestruc-25c` explicitly involves the spin, so we must enlarge our Hilbert space to include the spin degrees of freedom. We write

:::{math}
:label: eq-finestruc-28
\ES = \ES_orb \otimes \ES_spin
:::

[see {eq}`eq-jjcouple-9`] for the entire Hilbert space of the electron, where a convenient basis in $\ES_orb$ is the set of unperturbed central force eigenfunctions $\{ \ket{n\ell m_\ell} \}$, and where we use the usual basis $\{ \ket{sm_s} \}$ in $\ES_spin$. We put subscripts on the magnetic quantum numbers $m_\ell$ and $m_s$ to indicate what kind of angular momentum they represent (orbital and spin, respectively). The products of these basis states form a basis in $\ES$,

:::{math}
:label: eq-finestruc-29
\ket{n \ell m_\ell} \otimes \ket{s m_s} = \ket{n\ell m_\ell m_s},
:::

what we shall call the *uncoupled basis*. This basis is an eigenbasis of the complete set of commuting observables $(H_0,L^2,L_z,S_z)$ corresponding to quantum numbers $(n\ell m_\ell m_s)$. The quantum number $s$ corresponding to the operator $S^2$ is suppressed, because it is constant [$s=\frac{1}{2}$, $S^2= s(s+1)= \frac{3}{4}$]. Since the unperturbed Hamiltonian {eq}`eq-finestruc-1` is a purely orbital operator, including the spin degrees of freedom does not change the unperturbed energy eigenvalues {eq}`eq-finestruc-27`, but it does double the degeneracies (to $2n^2$), since there are two spin states (“up” or “down”) for each orbital eigenfunction.

(sec-finestruc-8)=

## Choosing a Good Basis in Degenerate Perturbation Theory

Since the unperturbed energy levels are degenerate, we must think in terms of degenerate perturbation theory, in which the shifts in the energy levels are the eigenvalues of the matrix of the perturbing Hamiltonian in the eigenspaces of the unperturbed system. In the present case, the unperturbed levels are $2n^2$-fold degenerate, so we will have a $2n^2 \times 2n^2$ matrix. This matrix will be easier to diagonalize in some bases than others.

The following describes a simple procedure for choosing a good basis. To take a specific example, let $H_1$ be some perturbing Hamiltonian, perhaps one of the fine structure terms. If we use the uncoupled basis {eq}`eq-finestruc-29`, then the matrix elements needed in perturbation theory are

:::{math}
:label: eq-finestruc-30
\matrixelement{n\ell m_\ell m_s}{H_1}{n\ell'm'_\ell m'_s}.
:::

Notice the distribution of primes: the index $n$ is the same on both sides of the matrix element because it labels an unperturbed eigenspace, while the indices $\ell$, $m_\ell$ and $m_s$ are allowed to be different, since these label the basis states inside the unperturbed eigenspace. Suppose now that $[L_z,H_1]=0$. Then we have

:::{math}
:label: eq-finestruc-31
0=\matrixelement{n\ell m_\ell m_s}{(L_zH_1-H_1L_z)}{n \ell' m'_\ell m'_s} = (m_\ell-m'_\ell) \matrixelement{n\ell m_\ell m_s}{H_1}{n\ell' m'_\ell m'_s},
:::

so either $m_\ell=m'_\ell$ or else the matrix element {eq}`eq-finestruc-30` vanishes. This example illustrates a general principle, which is that if an operator commutes with an observable belonging to a complete set of commuting observables, then the operator has diagonal matrix elements with respect to the quantum number of the observable in the eigenbasis of the complete set. This rule can often be used in cases where the Wigner-Eckart theorem does not apply. Its importance for degenerate perturbation theory is that in setting up the matrix elements of the perturbing Hamiltonian, we should use an eigenbasis of a complete set of commuting observables in which as many as possible of the observables commute with the perturbing Hamiltonian. If we are lucky or clever, the perturbing Hamiltonian will commute with all members of some complete set of commuting observables, and then its matrix elements will be entirely diagonal. In this case, the eigenvalues are the diagonal elements, and degenerate perturbation theory will have been effectively reduced to nondegenerate perturbation theory (that is, one obtains energy shifts just by computing expectation values, and one will not have to diagonalize any matrices).

(sec-finestruc-9)=

## A Good Basis for the Fine Structure Perturbations

Therefore in analyzing the fine structure perturbation, we should look for observables that commute with $H_FS$. The results are summarized in {ref}`tbl-finestruc-1`. We start with $H_RKE$. This is a purely orbital operator, and is furthermore a scalar. Therefore it commutes with $\Lvec$, the generator of orbital rotations. Also, since it is purely an orbital operator, it commutes with $\Svec$, which implies that it also commutes with $\Jvec=\Lvec+\Svec$. Furthermore, since it commutes with $\Lvec$, $\Svec$ and $\Jvec$, it commutes with any functions of them as well, including $L^2$, $S^2$ and $J^2$. The term $H_D$ is similar; it is also a purely orbital operator, which is a scalar. (The $\delta$-function can be thought of as the limit of a highly concentrated, rotationally symmetric function centered on $\xvec=0$, which therefore commutes with $\Lvec$.) Therefore $H_D$ also commutes with $\Lvec$, $\Svec$, $\Jvec$, $L^2$, $S^2$ and $J^2$. However, the term $H_SO$ does not commute with either $\Lvec$ or $\Svec$, since either purely spatial or spin rotations would rotate one half or the other of the dot product $\Lvec\cdot\Svec$, and would not leave the dot product invariant. However, $H_SO$ does commute with $\Jvec$, which generates overall rotations of the system and which rotates both $\Lvec$ and $\Svec$ simultaneously. It also commutes with $L^2$ and $S^2$, because of the commutators, $[\Lvec,L^2]=0$ and $[\Svec,S^2]=0$, and with $J^2$, because it commutes with $\Jvec$.

:::{list-table} The table indicates whether the given fine structure term commutes with the given angular momentum operator (${Y}={yes}$, ${N} = {no}$).
:label: tbl-finestruc-1
:header-rows: 6

* - FS Term
  - $\Lvec$
  - $L^2$
  - $\Svec$
  - $S^2$
  - $\Jvec$
  - $J^2$
* - $H_{RKE}$
  - Y
  - Y
  - Y
  - Y
  - Y
  - Y
* - $H_{D}$
  - Y
  - Y
  - Y
  - Y
  - Y
  - Y
* - $H_{SO}$
  - N
  - Y
  - N
  - Y
  - Y
  - Y

:::
We see that $H_RKE$ and $H_D$ are diagonal in the uncoupled basis {eq}`eq-finestruc-29`, but that $H_SO$ is not. However, all three operators are diagonal in the eigenbasis of the operators $(L^2,S^2,J^2,J_z)$. This suggests that we use the *coupled* basis for the perturbation treatment, that is, the basis in which we have combined angular momenta according to $\Jvec=\Lvec+\Svec$ or $\ell\otimes\frac{1}{2}$, as in {ref}`ch-jjcouple`. Following {eq}`eq-jjcouple-47a`, we define the coupled basis in terms of the uncoupled basis by

:::{math}
:label: eq-finestruc-32
\ket{n\ell jm_j} = \sum_{m_\ell,m_s} \ket{n\ell m_\ell m_s} \braket{\ell s m_\ell m_s}{jm_j},
:::

where the matrix element is a Clebsch-Gordan coefficient, and where we have suppressed the constant quantum number $s=\frac{1}{2}$ in various places.

Since all three fine structure terms are diagonal in the coupled basis, we only need to compute their diagonal matrix elements and add them up to get the fine structure energy shifts. This is the optimal situation in degenerate perturbation theory; there are no matrices to diagonalize.

Some books, for example, Bransden and Joachain, diagonalize $H_RKE$ and $H_D$ in the uncoupled basis, and $H_SO$ in the coupled basis, and then add the eigenvalues. This gives the correct answer for this problem but such a procedure cannot be recommended in general since the eigenvalues of a sum of matrices is not equal in general to the sum of the eigenvalues.

(sec-finestruc-10)=

## The Energy Shift for $H_RKE$

We begin with $H_RKE$ in {eq}`eq-finestruc-25a`, for which the desired matrix element is

:::{math}
\begin{aligned}
& \matrixelement{n\ell jm_j}{H_RKE}{n\ell jm_j} =
\end{aligned}
:::

:::{math}
:label: eq-finestruc-33
\begin{aligned}
&\qquad \sum_{m_\ell,m_s} \sum_{m'_\ell,m'_s} \braket{jm_j}{\ell s m_\ell m_s} \matrixelement{n\ell m_\ell m_s}{H_RKE} {n\ell m'_\ell m'_s} \braket{\ell s m'_\ell m'_s}{jm_j},
\end{aligned}
:::

where we have expressed the coupled basis vectors in terms of the uncoupled basis. We do this because $H_RKE$, being a purely orbital operator, is easier to evaluate in the uncoupled basis. Since $H_RKE$ does not involve the spin, the middle matrix element in {eq}`eq-finestruc-33` becomes

:::{math}
:label: eq-finestruc-34
\matrixelement{n\ell m_\ell m_s}{H_RKE} {n\ell m'_\ell m'_s} = \delta_{m_s,m'_s} \matrixelement{n\ell m_\ell}{H_RKE}{n\ell m'_\ell},
:::

where the last matrix element is purely orbital. In fact, it is the matrix element of a scalar operator with respect to a standard angular momentum basis (under orbital rotations alone), so by {eq}`eq-wigeck-47`, the Wigner-Eckart theorem for scalar operators, it is equal to $\delta_{m_\ell,m'_\ell}$ times a quantity that is independent of magnetic quantum numbers. That quantity can be regarded as a reduced matrix element, or it can be taken as the given matrix element with some convenient set of magnetic quantum numbers inserted, since the answer doesn't depend on them anyway. The value zero is convenient, so we have

:::{math}
:label: eq-finestruc-35
\matrixelement{n\ell m_\ell}{H_RKE}{n\ell m'_\ell} =\delta_{m_\ell,m'_\ell} \matrixelement{n\ell 0}{H_RKE}{n\ell 0}.
:::

When we put {eq}`eq-finestruc-34` and {eq}`eq-finestruc-35` back into {eq}`eq-finestruc-33` and use the orthogonality of the Clebsch-Gordan coefficients [see {eq}`eq-jjcouple-50a`], we find simply

:::{math}
:label: eq-finestruc-36
\matrixelement{n\ell jm_j}{H_RKE}{n\ell jm_j} = \matrixelement{n\ell 0}{H_RKE}{n\ell 0}.
:::

The energy shifts due to $H_RKE$, which nominally depend on $n$, $\ell$, $j$ and $m_j$, actually depend only on $n$ and $\ell$. We might have guessed this, since $H_RKE$ is diagonal in both the coupled and uncoupled basis (and the answer could not depend on $m_j$ in any case, since $H_RKE$ is a scalar operator).

We can now evaluate the final, purely orbital matrix element. We do this by writing

:::{math}
:label: eq-finestruc-37
H_RKE = -{\alpha^2 \over 2} T^2 = -{\alpha^2 \over 2} (H_0-V)^2,
:::

where $T=p^2/2$ is the kinetic energy. Then we have

:::{math}
\begin{aligned}
\matrixelement{n\ell jm_j}{H_RKE}{n\ell jm_j} &=-{\alpha^2 \over 2} \matrixelement{n\ell 0}{(H_0^2 -H_0V-VH_0 + V^2)}{n\ell 0}
\end{aligned}
:::

:::{math}
:label: eq-finestruc-38
\begin{aligned}
&=-{\alpha^2 \over 2} \matrixelement{n\ell 0}{(E_n^2 -2E_nV + V^2)}{n\ell 0}.
\end{aligned}
:::

The final expression involves expectation values of powers of $1/r$; the angular integrations are trivial because of the orthonormality of the $Y_{\ell m}$'s, and the remaining integration is over the radial variable $r$. The needed expectation values for hydrogen-like atoms are

:::{math}
\begin{aligned}
\Bigl<{1\over r}\Bigr> &= {Z\over n^2},
\end{aligned}
:::

:::{math}
:label: eq-finestruc-39
\begin{aligned}
\Bigl<{1\over r^2}\Bigr> &={Z^2\over n^3 (\ell+\frac{1}{2})}
\end{aligned}
:::

(see Prob. {ref}`prob-hydrogen-1`) which after some algebra give the final answer in the form,

:::{math}
:label: eq-finestruc-40
\matrixelement{n\ell jm_j}{H_RKE}{n\ell jm_j} = (Z\alpha)^2(-E_n){1\over n^2} \biggl( {3\over4} - {n\over \ell+\frac{1}{2}}\biggr).
:::

Here we have factored out the unperturbed energy $-E_n=Z^2/2n^2$ to show that the energy corrections are of order $(Z\alpha)^2$ compared to the energy scale of the unperturbed system.

(sec-finestruc-11)=

## Energy Shift for the Darwin Term

The analysis of the Darwin term $H_D$ of {eq}`eq-finestruc-26a` is similar. Since it is also a purely spatial scalar operator, its matrix element reduces as in {eq}`eq-finestruc-36`,

:::{math}
:label: eq-finestruc-41
\matrixelement{n\ell jm_j}{H_D}{n\ell jm_j} = \matrixelement{n\ell0}{H_D}{n\ell0}= Z\alpha^2 {\pi\over2} |\psi_{n\ell0}(0)|^2,
:::

where the $\delta$-function has allowed us to do the integral. Here

:::{math}
:label: eq-finestruc-42
\psi_{n\ell m}(\xvec) = R_{n\ell}(r) Y_{\ell m}(\theta,\phi)
:::

is the normalized energy eigenfunction. But because of the boundary conditions $R_{n\ell}(r) \sim r^\ell$ for small $r$, the answer will be nonzero only for $\ell=0$ ($s$-waves). Using $Y_{00}=1/\sqrt{4\pi}$ and the property of the hydrogen-like radial wave functions,

:::{math}
:label: eq-finestruc-43
R_{n0}(0) = 2\Bigl( {Z \over n} \Bigr)^{3/2},
:::

which can be derived from {eq}`eq-hydrogen-21` and {eq}`eq-hydrogen-28`, we can write the final answer in the form,

:::{math}
:label: eq-finestruc-44
\matrixelement{n\ell jm_j}{H_D}{n\ell jm_j} = (Z\alpha)^2 (-E_n) {1\over n} \delta_{\ell 0}.
:::

(sec-finestruc-12)=

## The Spin-Orbit Energy Shift

Finally, we consider the spin-orbit term, $H_SO$ of {eq}`eq-finestruc-26b`. Because of the identity,

:::{math}
:label: eq-finestruc-45
\Lvec\cdot\Svec={1\over2} (J^2-L^2-S^2),
:::

its matrix elements can be written,

:::{math}
:label: eq-finestruc-46
\matrixelement{n\ell jm_j}{H_SO}{n\ell jm_j} = {Z\alpha^2\over 4} [j(j+1)-\ell(\ell+1)-s(s+1)] \matrixelement{n\ell jm_j}{{1\over r^3}}{n\ell jm_j}.
:::

The remaining matrix element is again of a purely spatial scalar operator, which can be reduced to a purely spatial matrix element as in {eq}`eq-finestruc-36`. The result becomes the expectation value of $1/r^3$, which in a hydrogen-like atom is given by

:::{math}
:label: eq-finestruc-47
\Bigl<{1\over r^3}\Bigr> = {Z^3\over n^3 \ell(\ell+\frac{1}{2})(\ell+1)}.
:::

This expectation value diverges for $\ell=0$. But in that case, the operator $\Lvec$ is the zero operator, so we seem to have the form $0/0$ for the energy correction. The proper way to handle this is to smooth out the Coulomb singularity at $r=0$, whereupon the expectation value of $1/r^3$ does not diverge, and the answer is seen to vanish for $\ell=0$. Altogether, we can summarize the answer for $\ell\ne0$ by

:::{math}
:label: eq-finestruc-48
\begin{aligned}
\matrixelement{n\ell jm_j}{H_SO}{n\ell jm_j} &= (Z\alpha)^2(-E_n) {1\over 2n} { j(j+1)-\ell(\ell+1)-\frac{3}{4} \over \ell(\ell+\frac{1}{2})(\ell+1)} \\
&= (Z\alpha)^2(-E_n){1\over 2n} \begin{cases} \ds{\ds 1 \over \ds (\ell+\frac{1}{2})(\ell+1)}, & j=\ell+\frac{1}{2}, \\  \ds-{\ds 1 \over \ds \ell(\ell+\frac{1}{2})}. & j=\ell-\frac{1}{2}.\end{cases}
\end{aligned}

:::

(sec-finestruc-13)=

## The Total Fine Structure Energy Shift

All three fine structure corrections, {eq}`eq-finestruc-40`, {eq}`eq-finestruc-44`, and {eq}`eq-finestruc-48`, are of order $(Z\alpha)^2$ times the unperturbed energy levels, as predicted. When we add them up to get the total energy shift due to the fine structure, the result simplifies after some algebra, and we find

:::{math}
:label: eq-finestruc-49
\Delta E_FS = (Z\alpha)^2(-E_n){1\over n^2} \biggl( {3\over4} - {n\over j+\frac{1}{2}}\biggr).
:::

The most remarkable thing about this answer is that it is independent of the orbital angular momentum quantum number $\ell$, although each of the individual terms does depend on $\ell$. However, the total energy shift does depend on $j$ in addition to the principal quantum number $n$, so when we take into account the fine structure corrections, the energy levels of hydrogen-like atoms have the form $E_{nj}$. Of course the levels do not depend on $m_j$ because the Hamiltonian is a scalar operator. Factoring out the unperturbed energy levels, we can write the total energy of a hydrogen-like atom in the form,

:::{math}
:label: eq-finestruc-50
E_{nj} = \biggl( -{Z^2 \over 2n^2} \biggr) \biggl[ 1 - {(Z\alpha)^2 \over n^2} \biggl( {3\over4} -{n\over j+\frac{1}{2}} \biggr) + \ldots \biggr].
:::

The ellipsis indicates higher order terms that we have not calculated, but it is easy to believe that they turn into a power series in the quantity $(Z\alpha)^2$.

(sec-finestruc-14)=

## Comparison With the Dirac Equation

The Dirac equation for a hydrogen-like atom can be solved exactly. This does not mean that the answers agree exactly with the physics, because the Dirac equation, although fully relativistic, omits some important physics that we will consider later. Nevertheless, it is interesting to compare the results of the Dirac equation with the results of our perturbation calculation above. The Dirac energy levels are

:::{math}
:label: eq-finestruc-51
E_{nj} = {mc^2\over \sqrt{1+ \Bigg[\ds {\ds Z\alpha \over \ds n-j-\frac{1}{2} + \sqrt{\ds (j+\frac{1}{2})^2-(Z\alpha)^2}} \Bigg]^2}},
:::

where we revert to Gaussian units. See {ref}`sec-spdirac-17` for details. When this expression is expanded in powers of $Z\alpha$, we obtain,

:::{math}
:label: eq-finestruc-52
E_{nj}=mc^2\biggl[1-{(Z\alpha)^2\over 2n^2} + {(Z\alpha)^4\over 2n^4}\biggl( {3\over4} - {n\over j+\frac{1}{2}}\biggr) + O\bigl((Z\alpha)^6\bigr)\biggr].
:::

The first term in this expansion is the rest mass-energy, $mc^2$, the next contains the nonrelativistic Bohr energy levels $-(1/2n^2)(Z^2e^2/a_0)$, and the third contains the fine structure corrections {eq}`eq-finestruc-49`. Each term is of order $(Z\alpha)^2$ times the previous term.

There is no point in expanding the solution of the Dirac equation beyond the fine structure term, because there are other physical effects that are not incorporated into the Dirac equation that are larger than the next term after the fine structure term. Most important of these are the hyperfine effects, discussed in a subsequent set of notes, and the Lamb shift, discussed in \secrfinestruc-17.

(sec-finestruc-15)=

## Hydrogen-Like Energy Levels in the Fine Structure Model

Let us call the model of a hydrogen-like atom that includes the fine-structure perturbations the *fine structure model*. It is a refinement on the nonrelativistic, spinless, electrostatic model we have considered previously. We now examine some features of the energy levels in the fine structure model of a hydrogen-like atom.

The energy shifts {eq}`eq-finestruc-49` are negative for all values of $n$ and $j$, so fine structure effects depress all energy levels. However, smaller values of $j$ are more strongly depressed, so the total energy (unperturbed plus fine structure) is an increasing function of $j$. Since the unperturbed levels did not depend on $j$, fine structure effects have partially resolved the degeneracy in the unperturbed levels, which now have the form $E_{nj}$ (instead of just $E_n$). The fact that the levels still do not depend on $\ell$ means that the hydrogen atom, even including relativistic corrections, still has some extra symmetry that goes beyond rotational invariance (in particular, there is still a degeneracy between states of opposite parity).

In first courses on quantum mechanics the spin-orbit term is frequently the only term considered in treatments of the fine structure. It is true that this term alone is responsible for the $j$-dependence of the perturbed energy levels and their splitting, but unless the relativistic kinetic energy and Darwin terms are also included, one misses the fact that the total fine structure energy shifts are independent of $\ell$. It is clear from the formula {eq}`eq-finestruc-51` that this $\ell$-degeneracy persists to all orders in the expansion of the Dirac equation in powers of $\alpha$.

:::{figure} images/finestruc-fig02.png
:label: fig-finestruc-2
:width: 80%

Energy level diagram for hydrogen or hydrogen-like atoms, including fine structure, with allowed electric dipole transitions indicated (Grotrian diagram). Not shown are transitions only involving small energy differences, such as $3p_{3/2} \to 3s_{1/2}$. Diagram is schematic and not to scale; in particular, the fine structure splittings are of order $(Z\alpha)^2$ times the separation between the levels of different $n$.
:::

The standard spectroscopic notation for the states of hydrogen-like or alkali atoms is $n\ell_j$, where $\ell$ is represented by one of the standard symbols, $s$, $p$, $d$, $f$, etc. For example, the ground state of hydrogen is the $1s_{1/2}$ level. The low lying levels in a hydrogen-like atom are indicated schematically in {ref}`fig-finestruc-2`.

(sec-finestruc-16)=

## Electric Dipole Transitions in Hydrogen-Like Atoms

{ref}`fig-finestruc-2` also indicates the most important electric dipole transitions in a hydrogen-like atom. Allowed electric dipole transitions, $(n'\ell' j'm'_j)\to(n\ell jm_j)$, are those for which the matrix element

:::{math}
:label: eq-finestruc-53
\matrixelement{n\ell jm_j}{x_q}{n'\ell' j'm'_j}
:::

is nonzero, where $x_q$ is the component of the position operator $\xvec$ with respect to the spherical basis {eq}`eq-transfop-37`. The operator $x_q$ is a $k=1$ irreducible tensor operator, both under purely spatial rotations, generated by $\Lvec$, and under rotations of the whole system, generated by $\Jvec$. Therefore the Wigner-Eckart theorem can be applied twice. When it is applied to purely spatial rotations and combined with parity, it gives the selection rule $\Delta \ell=\pm1$ ($\Delta\ell=0$ would be allowed by the Wigner-Eckart theorem, but is excluded by parity). When the Wigner-Eckart theorem is applied to total rotations, it gives the selection rules $\Delta j = 0,\pm1$ and $m'_j = m_j+q$. There is nothing to exclude transitions with $\Delta j=0$, and, in fact, such transitions occur. The selection rule involving magnetic quantum numbers gives information about the polarization of the photon emitted on transitions from some initial to some final magnetic substate.

Concerning parity, note that it is a purely orbital operator that has no effect on spin. Thus its action on states of the uncoupled basis is

:::{math}
:label: eq-finestruc-54
\pi \ket{n\ell m_\ell m_s} = (-1)^\ell \ket{n\ell m_\ell m_s}.
:::

From this and from {eq}`eq-finestruc-32`, the action of parity on the states of the coupled basis is

:::{math}
:label: eq-finestruc-55
\pi \ket{n \ell j m_j} = (-1)^\ell \ket{n\ell j m_j}.
:::

(sec-finestruc-17)=

## The Lamb Shift

The Lamb shift is a shift in the energy levels of the Dirac picture that is due to the interaction of the electron with the vacuum fluctuations of the quantized electromagnetic field. It has small effects on all the energy levels, and its most notable feature is that the effect is different on levels with the same values of $n$ and $j$ but different values of $\ell$. Thus, including the Lamb shift, the energy levels in hydrogen have the form $E_{n\ell j}$, and the only degeneracy is that due to rotational invariance. All extra or “accidental” degeneracy is removed.

:::{figure} images/finestruc-fig03.png
:label: fig-finestruc-3
:width: 80%

An expanded view of the $n=2$ levels in hydrogen, including the Lamb shift. The splitting due to the Lamb shift is notable because it introduces an $\ell$-dependence into the energies. Its magnitude is about 10 times smaller than the fine structure splitting (on the $n=2$ levels).
:::

The most important manifestation of the Lamb shift is in the $n=2$ levels of hydrogen. See {ref}`fig-finestruc-3`. Here the Lamb shift causes the $2s_{1/2}$ level to be raised about 1.0~GHz relative to the $2p_{1/2}$ level. This energy difference can be measured with high accuracy with radio frequency techniques. The detection and theoretical calculation of the Lamb shift was an important milestone in the history of quantum electrodynamics, because it was one of the first successful application of renormalization theory. We will consider the Lamb shift in more detail in later in the course.

(sec-finestruc-18)=

## Fine Structure in Alkali Atoms

Most of the analysis presented above for hydrogen-like atoms goes through for the alkali atoms, with $V(r)$ replaced by the appropriate screened Coulomb potential. The unperturbed (nonrelativistic) energy levels of the alkalis have the form $E_{n\ell}$, and are already strongly split by the $\ell$ values because of the non-Coulomb nature of the central force. See Fig.~\figr\hydrogen.3 for the case of sodium. The three fine structure terms present in hydrogen are also present in the alkalis, but the relativistic kinetic energy and Darwin terms are not very interesting, because they cause only small shifts in the energy levels of $H_0$, without splitting them. That is, the energy shifts produced by these terms have the form $\Delta E_{n\ell}$, and the energies already depend on $n$ and $\ell$. These terms are more interesting in hydrogen, because of the degeneracy among the different $\ell$ values. However, the spin-orbit term does split the alkali levels according to their $j$ values, much as in hydrogen, and produces overall energy levels of the form $E_{n\ell j}$. The analysis of the spin-orbit splitting in the alkalis proceeds much as with hydrogen in \secrfinestruc-12, yielding

:::{math}
:label: eq-finestruc-56
\Delta E_SO = {\alpha^2 \over 4} [j(j+1) - \ell(\ell+1) - \frac{3}{4}] \Bigl< {1\over r}\dod{V}{r}\Bigr>.
:::

The expectation value is with respect to the wave function $\psi_{n\ell 0}$; it must be done numerically since both $V(r)$ and $\psi_{n\ell0}$ are only known numerically. But the formula {eq}`eq-finestruc-56` does give the correct dependence on the quantum number $j$.

The levels of sodium displayed in Fig.~\figr\hydrogen.3 do not show the fine structure splitting, because it is too small on the scale of that diagram. But, for example, if the $3p$ level is examined closely, it will be found to be split into a $3p_{1/2}$ level and a $3p_{3/2}$ level, with the $j=3/2$ level lying 0.00213~eV above the $j=1/2$ level. This causes the $3p \to 3s$ transition (the yellow sodium $D$-line) to be a close doublet. The selection rules in the alkali atoms depend only on the angular momentum quantum numbers, and are the same as in hydrogen.

\problems

(prob-finestruc-1)=

**Problem \prbdfinestruc-1.} If a hydrogen atom finds itself in the $2p$ state (either $2p_{1/2}$ or $2p_{3/2}$) it will emit a photon and decay into the ground state in about $10^{-9}$ seconds.   If it finds itself in the $2s_{1/2.** 

\problempart{(a)} Explain why the transition }$2s_{1/2} \to 1s_{1/2}$ is not allowed as an electric dipole transition. However, due to the Lamb shift, the $2p_{1/2}$ state is 1.0 GHz below the $2s_{1/2}$ state, and the electric dipole transition $2s_{1/2} \to 2p_{1/2}$ is allowed. If the atom makes this transition, it will almost immediately drop into the ground state, so the rate of the transition $2s_{1/2} \to 2p_{1/2}$ is effectively the decay rate $2s_{1/2} \to 1s_{1/2}$ via this mechanism.

\problempart{(b)} It can be shown that rate for an electric dipole transition $B\to A$ (in $\rm{sec}^{-1}$) is

:::{math}
:label: eq-finestruc-57
w={4\over 3} {\omega^3e^2\over\hbar c^3} |\matrixelement{B}{\xvec}{A}|^2,
:::

where $A$ and $B$ are states of a single electron atom, and where $\omega$ is the frequency of the emitted photon. Also, you may note that

:::{math}
:label: eq-finestruc-58
|\matrixelement{B}{\xvec}{A}|^2 = \sum_q |\matrixelement{B}{x_q}{A}|^2,
:::

where $x_q$ is the component of the position vector with respect to the spherical basis, as in {ref}`sec-transfop-12`.

Suppose the initial state is $\ket{n\ell jm_j} = \ket{20\frac{1}{2}\frac{1}{2}}$. Find the transition rate to any $2p_{1/2}$ state, as an electric dipole transition. You have to sum the rates to any final $2p_{1/2}$ state that is accessible from the initial state.

I suggest you first express the matrix elements of $x_q$ with respect to the hydrogen atom states in the fine structure model, $\ket{n\ell jm_j}$, in terms of the matrix elements of $x_q$ with respect to the states of the electrostatic model, $\ket{n\ell m_\ell}$. Then evaluate the latter any way you can, for example, by the method described in {ref}`sec-transfop-12`.

(prob-finestruc-2)=

**Problem \prbdfinestruc-2..**
