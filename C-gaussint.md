---
title: "Appendix C. Gaussian Integrals"
---
(ch-c-gaussint)=

# Appendix C. Gaussian Integrals

(sec-gaussint-1)=

## The Main Results

The most common Gaussian integral encountered in practice is

:::{math}
:label: eq-gaussint-1
\int_{-\infty}^{+\infty} dx\, e^{-ax^2} = {\sqrt{\pi} \over \sqrt{a}},
:::

where $a$ is real and $a>0$. The integral does not exist (it diverges) if $a\le0$.

Another common form is when the exponent is purely imaginary. In this case we have

:::{math}
:label: eq-gaussint-2
\int_{-\infty}^{+\infty} dx\, e^{icx^2} = e^{is\pi/4} \, {\sqrt{\pi} \over \sqrt{|c|}},
:::

where $c$ is real and $c\ne0$, and where $s=\sgn c=\pm1$. The integral does not exist (it diverges) if $c=0$. Notice that {eq}`eq-gaussint-2` is a special case of {eq}`eq-gaussint-1` if $a$ is allowed to be complex, if we set $a=-ic$, and if $\sqrt{a} = \sqrt{-ic}$ is interpreted according to

:::{math}
:label: eq-gaussint-3
\begin{aligned}
\sqrt{-ic} = \begin{cases} e^{-i\pi/4} \sqrt{|c|}, & c>0, \\  e^{i\pi/4} \sqrt{|c|}, & c<0. \\\end{cases}
\end{aligned}

:::

If we allow $a$ in {eq}`eq-gaussint-1` to be an arbitrary complex number, then the integral converges exponentially if $\Re a>0$. If $\Re a <0$ then the integrand diverges exponentially and the integral is not defined. The case $\Re a=0$ is the marginal case. If $\Re a=0$ and $\Im a \ne 0$, then the integrand oscillates with a sequence of positive and negative lobes with decreasing area as $x$ increases, so the integral converges. Finally, if $\Re a=0$ and $\Im a=0$ (that is, $a=0$), then the integral does not converge. In summary, the integral converges everywhere to the right of the imaginary axis in the complex $a$-plane, and on the imaginary axis except at $a=0$.

If $a$ is a complex number such that the integral {eq}`eq-gaussint-1` converges, then the answer is still given by {eq}`eq-gaussint-1`, as long as $\sqrt{a}$ is interpreted in the following sense. We write

:::{math}
:label: eq-gaussint-4
a = |a| e^{i\phi},
:::

where $-\pi/2 \le \phi \le \pi/2$, and we define

:::{math}
:label: eq-gaussint-5
\sqrt{a} = e^{i\phi/2} \, \sqrt{|a|}.
:::

This means that of the two square roots of $a$, we take the one with the positive real part.

Another common form is one with a linear term in the exponent,

:::{math}
:label: eq-gaussint-6
\int_{-\infty}^{\infty} dx\, e^{-ax^2+bx} = {\sqrt{\pi}\over \sqrt{a}} \,e^{b^2/4a}.
:::

The existence of this integral depends on the value of $a$ in the same way as the simpler integral {eq}`eq-gaussint-1`, because for large $x$ the quadratic term in the exponent dominates. That is, $a$ can be any complex number to the right of the imaginary axis, or on the imaginary axis, except for $a=0$. The convergence of the integral is independent of $b$, which can be any complex number. The quantity $\sqrt{a}$ on the right hand side of {eq}`eq-gaussint-6` is interpreted as in {eq}`eq-gaussint-5`.

(sec-gaussint-2)=

## The Proof

This is the standard proof, see, for example, E. B. Wilson, *Advanced Calculus*.

First take the case where $a$ is real and $a>0$. By a change of variable $\sqrt{a}\, x=x'$ the answer can be expressed in terms of

:::{math}
:label: eq-gaussint-7
I=\int_{-\infty}^{\infty} dx\, e^{-x^2} = \int_{-\infty}^{\infty} dy\, e^{-y^2},
:::

where we have dropped the prime on $x$ in the first integral. Squaring this we have

:::{math}
:label: eq-gaussint-8
I^2 = \int dx\,dy\, e^{-(x^2+y^2)} = \int_0^\infty \rho\,d\rho \int_0^{2\pi} d\theta\, e^{-\rho^2},
:::

where we have switched to polar coordinates in the second integral. This integral is easily done, yielding $I^2=\pi$. Taking the square root and transforming back to the original variable of integration reproduces {eq}`eq-gaussint-1`. The method is a special trick that is worth knowing because the result is so important.

To prove {eq}`eq-gaussint-1` in the case that $a$ is complex (but in the allowed region described in \secrgaussint-1) we do a change of variable,

:::{math}
:label: eq-gaussint-9
t=\sqrt{a}\, x,
:::

where $\sqrt{a}$ is defined in {eq}`eq-gaussint-5`. The contour of integration in the original integral runs along the real axis in the complex $x$-plane, so after the change of variable the contour is $\arg t=\phi/2$, $\arg t=\phi/2+\pi$ in the complex $t$-plane. However this contour can be deformed to run along the real $t$-axis, whereupon the integral is reduced to the form of {eq}`eq-gaussint-1` with $a=1$. This is really an example of the method of steepest descent, an approximation method for integrals which however in this case is exact.

To prove the integral {eq}`eq-gaussint-6` we complete the square and shift origin to reproduce the form {eq}`eq-gaussint-1`.

(sec-gaussint-3)=

## Multidimensional Gaussian Integrals

A common form of a multidimensional Gaussian integral is

:::{math}
:label: eq-gaussint-10
\int d^nx \, \exp(-x^T\cdot A \cdot x + b^T\cdot x) = {\pi^{n/2} \over \sqrt{\det A}} \, \exp\Bigl( {b^T \cdot A^{-1} \cdot b \over 4}\Bigr),
:::

where $x$ is a a real $n$-vector and the range of integration is all of $\Reals^n$, where $A$ is a real, $n\times n$ symmetric, positive definite matrix, where $b$ is an $n$-vector, where $T$ means transpose, where $x$ and $b$ are seen as column vectors and $x^T$ and $b^T$ as row vectors, and where the dot indicates contractions or matrix multiplication. The vector $b$ is allowed to be complex.

The case where the matrix $A$ in {eq}`eq-gaussint-10` is purely imaginary is also common. In this case we have

:::{math}
:label: eq-gaussint-11
\int d^nx \, \exp(i x^T\cdot C \cdot x + b^T\cdot x) =e^{i\nu\pi/4} {\pi^{n/2} \over \sqrt{|\det C|}} \, \exp\Bigl(i {b^T \cdot C^{-1} \cdot b \over 4}\Bigr).
:::

Here $C$ is a real, $n\times n$ symmetric matrix with $\det C\ne0$; $\nu$ is an integer,

:::{math}
:label: eq-gaussint-12
\nu = \nu_+ - \nu_-,
:::

where $\nu_\pm$ is the number of positive or negative eigenvalues of $C$; and otherwise the notation is as in {eq}`eq-gaussint-10`.

The case where $A$ in {eq}`eq-gaussint-10` is a complex symmetric matrix is more complicated but encountered less frequently, so we shall not consider it.

{eq}`eq-gaussint-10` is proved by performing an orthogonal transformation,

:::{math}
:label: eq-gaussint-13
x = R \cdot y,
:::

where $y$ is another real $n$-vector and $R$ is an orthogonal matrix such that

:::{math}
:label: eq-gaussint-14
R^T A R = \Lambda,
:::

where $\Lambda$ is diagonal. Then $d^nx = d^ny$, and the new integral breaks up into the product of one-dimensional integrals of the form {eq}`eq-gaussint-1`. {eq}`eq-gaussint-11` is proved similarly, except the resulting one-dimensional integrals have the form {eq}`eq-gaussint-2`.

(sec-gaussint-4)=

## Moment Integrals

We present some one-dimensional integrals giving moments of Gaussian. The integral for the first moment is

:::{math}
:label: eq-gaussint-15
\int dx \, x e^{-ax^2+bx} = {b\over 2a}\, {\sqrt{\pi}\over \sqrt{a}} \,e^{b^2/4a},
:::

while the second moment is

:::{math}
:label: eq-gaussint-16
\int dx \, x^2 e^{-ax^2+bx} = \Bigl({1\over 2a} + {b^2\over 4a^2}\Bigr) {\sqrt{\pi}\over \sqrt{a}} \,e^{b^2/4a}.
:::

These may be obtained by differentiating {eq}`eq-gaussint-6` with respect to $a$ or $b$.
