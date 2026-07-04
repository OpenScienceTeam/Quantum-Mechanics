---
title: "Appendix D. Vector Calculus"
---
(ch-d-vecident)=

# Appendix D. Vector Calculus

(sec-vecident-1)=

## Introduction

In the following we let $f$ be a scalar field and $\Avec$ a vector field.

(sec-vecident-2)=

## Differential Operators in Rectangular Coordinates

The components of $\Avec$ are given by

:::{math}
:label: eq-vecident-1
\Avec=A_x \,{\hat{\mathbf{x}}} + A_y\,{\hat{\mathbf{y}}} +A_z\,{\hat{\mathbf{z}}}.
:::

Then

:::{math}
:label: eq-vecident-2
\del f = \frac{\partial f}{\partial x} \,{\hat{\mathbf{x}}} + \frac{\partial f}{\partial y} \,{\hat{\mathbf{y}}} + \frac{\partial f}{\partial z} \,{\hat{\mathbf{z}}},
:::

:::{math}
:label: eq-vecident-3
\del\cross\Avec = \Bigl(\frac{\partial A_y}{\partial x} - \frac{\partial A_x}{\partial y}\Bigr)\,{\hat{\mathbf{x}}} + \Bigl(\frac{\partial A_z}{\partial y} - \frac{\partial A_y}{\partial z}\Bigr)\,{\hat{\mathbf{y}}} + \Bigl(\frac{\partial A_x}{\partial z} - \frac{\partial A_z}{\partial x}\Bigr)\,{\hat{\mathbf{z}}},
:::

:::{math}
:label: eq-vecident-4
\del\cdot\Avec = \frac{\partial A_x}{\partial x} + \frac{\partial A_y}{\partial y} + \frac{\partial A_z}{\partial z},
:::

and

:::{math}
:label: eq-vecident-5
\del^2f = {\partial^2 f\over \partial x^2} + {\partial^2 f\over \partial y^2} + {\partial^2 f\over \partial z^2}.
:::

(sec-vecident-3)=

## Differential Operators in Cylindrical Coordinates

Cylindrical coordinates are $(\rho,\phi,z)$, defined by

:::{math}
:label: eq-vecident-6
\begin{aligned}
x &= \rho\cos\phi, \\
y &= \rho\sin\phi, \\
z &= z. \\

\end{aligned}
:::

The orthonormal frame of associated unit vectors is

:::{math}
:label: eq-vecident-7
\begin{aligned}
{\hat{\boldsymbol{\rho}}} &= \cos\phi\,{\hat{\mathbf{x}}} + \sin\phi\,{\hat{\mathbf{y}}}, \\
{\hat{\boldsymbol{\phi}}} &= -\sin\phi\,{\hat{\mathbf{x}}} + \cos\phi\,{\hat{\mathbf{y}}}, \\
{\hat{\mathbf{z}}} &= \,{\hat{\mathbf{z}}}, \\

\end{aligned}
:::

with

:::{math}
:label: eq-vecident-8
{\hat{\boldsymbol{\rho}}} \cross {\hat{\boldsymbol{\phi}}} = {\hat{\mathbf{z}}}.
:::

Define the components of $\Avec$ by

:::{math}
:label: eq-vecident-9
\Avec = A_\rho \,{\hat{\boldsymbol{\rho}}} + A_\phi \,{\hat{\boldsymbol{\phi}}} + A_z \,{\hat{\mathbf{z}}}.
:::

Then

:::{math}
:label: eq-vecident-10
\del f = \frac{\partial f}{\partial \rho}\,{\hat{\boldsymbol{\rho}}} + {1\over\rho}\frac{\partial f}{\partial \phi} \,{\hat{\boldsymbol{\phi}}} + \frac{\partial f}{\partial z} \,{\hat{\mathbf{z}}},
:::

:::{math}
:label: eq-vecident-11
\del\cross\Avec = \Bigl({1\over\rho}\frac{\partial A_z}{\partial \phi} - \frac{\partial A_\phi}{\partial z}\Bigr) {\hat{\boldsymbol{\rho}}} + \Bigl(\frac{\partial A_\rho}{\partial z} - \frac{\partial A_z}{\partial \rho}\Bigr) {\hat{\boldsymbol{\phi}}} + {1\over\rho}\Bigl[\pop{}{\rho}(\rho A_\phi)- \frac{\partial A_\rho}{\partial \phi}\Bigr]{\hat{\mathbf{z}}},
:::

:::{math}
:label: eq-vecident-12
\del\cdot\Avec = {1\over\rho}\pop{}{\rho}(\rho A_\rho) + {1\over\rho} \frac{\partial A_\phi}{\partial \phi} + \frac{\partial A_z}{\partial z},
:::

and

:::{math}
:label: eq-vecident-13
\del^2 f = {1\over\rho}\pop{}{\rho} \Bigl(\rho\frac{\partial f}{\partial \rho}\Bigr) + {1\over\rho^2} {\partial^2 f\over \partial\phi^2} + {\partial^2 f\over \partial z^2}.
:::

Also, the following Jacobians are sometimes useful:

:::{math}
:label: eq-vecident-14
\begin{aligned}
{\partial(xyz)\over \partial(\rho\phi z)}= \begin{pmatrix}\cos\phi & -\rho\sin\phi & 0 \\  \sin\phi & \rho\cos\phi & 0 \\  0 & 0 & 1\\\end{pmatrix},
\end{aligned}

:::

where the rows are labeled by $(xyz)$ and columns by $(\rho\phi z)$, for example, $\partial x/\partial\phi=-\rho\sin\phi$. The inverse Jacobian is

:::{math}
:label: eq-vecident-15
\begin{aligned}
{\partial(\rho\phi z)\over\partial(xyz)} = \begin{pmatrix}\cos\phi & \sin\phi & 0 \\  -{\ds \sin\phi\over\ds\rho} & {\ds\cos\phi\over\ds\rho} & 0 \\  0 & 0 & 1\\\end{pmatrix}.
\end{aligned}

:::

(sec-vecident-4)=

## Differential Operators in Spherical Coordinates

Spherical coordinates are $(r,\theta,\phi)$, defined by

:::{math}
:label: eq-vecident-16
\begin{aligned}
x &= r\sin\theta \cos\phi, \\
y &= r\sin\theta \sin\phi, \\
z &= r\cos\theta. \\

\end{aligned}
:::

The orthonormal frame of associated unit vectors is

:::{math}
:label: eq-vecident-17
\begin{aligned}
{\hat{\mathbf{r}}} &= \sin\theta\cos\phi\,{\hat{\mathbf{x}}} + \sin\theta\sin\phi\,{\hat{\mathbf{y}}} + \cos\theta\,{\hat{\mathbf{z}}}, \\
{\hat{\boldsymbol{\theta}}} &= \cos\theta\cos\phi\,{\hat{\mathbf{x}}} + \cos\theta\sin\phi\,{\hat{\mathbf{y}}} - \sin\theta\,{\hat{\mathbf{z}}}, \\
{\hat{\boldsymbol{\phi}}} &= -\sin\phi\,{\hat{\mathbf{x}}} + \cos\phi\,{\hat{\mathbf{y}}}, \\

\end{aligned}
:::

with

:::{math}
:label: eq-vecident-18
{\hat{\mathbf{r}}} \cross {\hat{\boldsymbol{\theta}}} = {\hat{\boldsymbol{\phi}}}.
:::

Define the components of $\Avec$ by

:::{math}
:label: eq-vecident-19
\Avec = A_r \,{\hat{\mathbf{r}}} + A_\theta \,{\hat{\boldsymbol{\theta}}} + A_\phi  \,{\hat{\boldsymbol{\phi}}}.
:::

Then

:::{math}
:label: eq-vecident-20
\del f= \frac{\partial f}{\partial r}\,{\hat{\mathbf{r}}} + {1\over r}\frac{\partial f}{\partial \theta}\,{\hat{\boldsymbol{\theta}}} + {1\over r\sin\theta}\frac{\partial f}{\partial \phi}\,{\hat{\boldsymbol{\phi}}},
:::

:::{math}
:label: eq-vecident-21
\del\cross\Avec = {1\over r\sin\theta} \Bigl[\pop{}{\theta}(A_\phi \sin\theta)- \frac{\partial A_\theta}{\partial \phi}\Bigr]\,{\hat{\mathbf{r}}} + {1\over r}\Bigl[{1\over\sin\theta} \frac{\partial A_r}{\partial \phi} - \pop{}{r}(rA_\phi)\Bigr]\,{\hat{\boldsymbol{\theta}}} + {1\over r}\Bigl[\pop{}{r}(rA_\theta) - \frac{\partial A_r}{\partial \theta}\Bigr]\,{\hat{\boldsymbol{\phi}}},
:::

:::{math}
:label: eq-vecident-22
\del\cdot\Avec = {1\over r^2} \pop{}{r}(r^2 A_r) + {1\over r\sin\theta}\pop{}{\theta}(A_\theta \sin\theta) + {1\over r\sin\theta}\frac{\partial A_\phi}{\partial \phi},
:::

and

:::{math}
:label: eq-vecident-23
\del^2 f = {1\over r^2} \pop{}{r}\Bigl(r^2\frac{\partial f}{\partial r}\Bigr) + {1\over r^2\sin\theta}\pop{}{\theta}\Bigl( \sin\theta\frac{\partial f}{\partial \theta}\Bigr) + {1\over r^2\sin^2\theta} {\partial^2 f \over \partial\phi^2}.
:::

The following Jacobian matrices are sometimes useful:

:::{math}
:label: eq-vecident-24
\begin{aligned}
{\partial(xyz)\over\partial(r\theta\phi)} = \begin{pmatrix}\sin\theta\cos\phi & r\cos\theta\cos\phi & -r\sin\theta\sin\phi \\  \sin\theta\sin\phi & r\cos\theta\sin\phi & r\sin\theta\cos\phi\\  \cos\theta & -r\sin\theta & 0\\\end{pmatrix},
\end{aligned}

:::

and its inverse,

:::{math}
:label: eq-vecident-25
\begin{aligned}
{\partial(r\theta\phi)\over \partial(xyz)} = \begin{pmatrix} \sin\theta\cos\phi & \sin\theta\sin\phi & \cos\theta \\  {\ds\cos\theta\cos\phi\over\ds r} & {\ds\cos\theta\sin\phi\over\ds r} & -{\ds\sin\theta\over\ds r}\\  -{\ds\sin\phi\over\ds r\sin\theta} & {\ds\cos\phi\over\ds r\sin\theta} & 0\\\end{pmatrix}.
\end{aligned}

:::

(sec-vecident-5)=

## The Line Element

Let two nearby points have coordinates $(x,y,z)$ and $(x+dx,y+dy,z+dz)$, or $(r,\theta,\phi)$ and $(r+dr, \theta+d\theta, \phi+d\phi)$, etc, depending on the coordinates. Let $ds$ be the distance between the two points. Then, in the various coordinate systems, we have

:::{math}
:label: eq-vecident-26a
\begin{aligned}
ds^2 &= dx^2 + dy^2 + dz^2,
\end{aligned}
:::

:::{math}
:label: eq-vecident-26b
\begin{aligned}
&= d\rho^2 + \rho^2\,d\phi^2 + dz^2,
\end{aligned}
:::

:::{math}
:label: eq-vecident-26c
\begin{aligned}
&= dr^2 + r^2\,d\theta^2 + r^2\sin^2\theta \, d\phi^2.
\end{aligned}
:::

Dividing this by $dt^2$, we get the square of the velocity, $v^2 = \vvec\cdot\vvec$, expressed in terms of the time derivatives of the coordinates. This gives

:::{math}
:label: eq-vecident-27a
\begin{aligned}
v^2 &= {\dot x}^2 + {\dot y}^2 + {\dot z}^2,
\end{aligned}
:::

:::{math}
:label: eq-vecident-27b
\begin{aligned}
&= {\dot \rho}^2 + \rho^2\, {\dot\phi}^2 + {\dot z}^2,
\end{aligned}
:::

:::{math}
:label: eq-vecident-27c
\begin{aligned}
&= {\dot r}^2 + r^2\, {\dot\theta}^2 + r^2\sin^2\theta\, {\dot\phi}^2.
\end{aligned}
:::

From the components of the line element one can read off the components of the metric tensor.

(sec-vecident-6)=

## Vector Calculus in Two Dimensions

In two dimensions the usual coordinates are either rectangular, $(x,y)$ or polar $(\rho,\phi)$. The coordinate transformation and formulas for the unit vectors $({\hat{\boldsymbol{\rho}}},{\hat{\boldsymbol{\phi}}})$ are obtained from {eq}`eq-vecident-6` and {eq}`eq-vecident-7` simply by omitting the terms referring to $z$ or ${\hat{\mathbf{z}}}$. The formulas for $\del f$, $\del\cdot\Avec$ and $\del^2 f$ can be obtained from those in Secs.~\secrvecident-2 and \secrvecident-3 simply by omitting the terms that refer to $z$ or $A_z$. As for the curl of a vector field, $\del\cross\Avec$, in two dimensions it can be regarded as a scalar that is identified with the $z$-component of the corresponding three-dimensional formulas, {eq}`eq-vecident-3` or {eq}`eq-vecident-11`. The line element in two dimensions is given by {eq}`eq-vecident-26b`, omitting the term referring to $z$.
