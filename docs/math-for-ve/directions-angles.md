# Directions and Angles

## Directions Over the Unit Sphere

A vector comprises of a **magnitude** (i.e. norm/length) and a **direction**.

For any normalized vector $\vu{v} = (x, y, z)$,

$$
x^2 + y^2 + z^2 = 1
$$

So if the values of $x, y$ are known then the value of $z$ (but not its sign)
can be computed.

Any **direction** can be considered a line from the origin to a point on the
unit sphere with center at the origin.

- Since surface of sphere is 2D, then so is the space of all possible
  directions.

## Spherical Coordinate Representation

The sphereical representation of 3D coordinates can be useful.

<figure>
    <img src="./spherical-coordinates.png" width="50%" />
    <figcaption>Figure 1: Spherical 3D coordinates [CGVE].</figcaption>
</figure>

Let $P(x, y, z)$ be some point and the distance from origin $O$ to $P$ is
$r = \sqrt{x^2 + y^2 + z^2}$.

- $Q$ is the **perpendicular projection** of $P$ to the $xy$-plane.
- Angle $\beta$ is angle between $x$-axis and $OQ$.
- Angle $\alpha$ is angle between $z$-axis and $OP$.

Thus angle $\triangle OPQ = \alpha$, $\triangle OQ = r \sin(\alpha)$.
Consequently,

$$
\begin{align}
    x &= r \sin(\alpha) \cos(\beta) \\
    y &= r \sin(\alpha) \sin(\beta) \\
    z &= r \cos(\alpha)
\end{align}
$$

From the **spherical coordinates** $(r, \alpha, \beta)$, one can find its
equivalent **Cartesian coordinates** $(x, y, z)$ via

$$
\begin{align}
    \alpha &= a \cos(\frac{z}{r}) \\
    \beta  &= a \tan(\frac{y}{x})
\end{align}
$$

## Solid Angles


