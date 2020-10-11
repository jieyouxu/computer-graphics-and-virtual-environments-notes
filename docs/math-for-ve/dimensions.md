# Dimensions

The **dimension** of a space is the amount of freedom of movement that
objects within that space have while being constrained within the space

- Also the minimum number of independent values required to specify a location
  within the space unambiguously.

## 0 Dimension

A 0-dimension space is a single point, infinitesimally small.

## 1 Dimension

Objects in 1-D can move in one direction, forwards or backwards, can be
interpreted as infinitely long continuous line, no area.

- Choose aribrary point $O$ and label as **origin**.
    - One direction from origin is **positive**, other is **negative**.
- Positive portion is the **positive half-space**.
- Negative portion is the **negative half-space**.
- Position of point in 1D space is some number $n$ representing distance from
  origin, with $+$ or $-$ to indicate belonging to positive/negative half-space
  respectively.
- Can be represented as:
    - **Set Constructions**, e.g. $\{ x \mid 1 \leq x \leq 2 \}$
    - **Intervals**, e.g. $[1.0, 2.0]$, or any set of points in the 1D space.

## 2 Dimensions

Objects in 2-D can move in two directions, "left"/"right", "top"/"down". To
describe 2D space requires two infinite lines that are **orthogonal**
(**perpendicular**) to each other.

- We can use two orthogonal unit vectors $\{ \hat{\imath}, \hat{\jmath} \}$.
- Intersect at a point labelled the **origin** $O$, which is the origin of a
  2D coordinate system.

Conventions:

- $\hat{\jmath}$ is the horizontal axis, often the $x$-axis, and
  $\hat{\imath}$ is the vertical axis, often the $y$-axis.
- The origin is the point $(0, 0)$ (i.e. $0 \hat{\imath} + 0 \hat{\jmath}$).
- Any point in 2D space is the 2-tuple coordinate pair $(x, y)$, which is
  the distance along $x$-axis from origin and distance along $y$-axis from
  origin (i.e. $x \hat{\imath} + y \hat{\jmath}$).

This is often called the **Cartesian coordinate system**. To specify and measure
**Euclidean distance** ($\ell_2$-norm), let $P_1 = (x_1, y_1)$ and
$P_2 = (x_2, y_2)$ be two points, then the distance $d$ is given by

$$
d = \abs{P2 - P1} = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}
$$

## 3 Dimensions

The **Euclidean distance** can be generalized to 3D space, given two 3D points
$P_1 = (x_1, y_1, z_1)$ and $P_2 = (x_2, y_2, z_2)$, the distance $d$ is given
by

$$
d = \abs{P2 - P1} = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}
$$

Again, choose the basis of three orthogonal unit vectors
$\{ \hat{\imath}, \hat{\jmath}, \hat{k} \}$, and you can get any point in 3D
space by the linear combination of these three unit vectors.

By convention, $\hat{\imath}$ is the $x$-axis, $\hat{\jmath}$ is the $y$-axis,
$\hat{k}$ is the $z$-axis. Collectively, they are called the **principal axes**.

The origin $O$ is $(0, 0, 0)$ and the coordinate system is continuous, a general
point represented by $(x, y, z)$.

### Right- and Left-Handed Coordinate System

In 3D, there is a choice about configuration of the positive/negative
conventions, since paper/screen is 2D. We can either pick a **left-handed** or
**right-handed coordinate system**.

<figure>
    <img src="./handedness.png" width="50%" />
    <figcaption>
        Figure 1: Right- and Left-Handed Coordinate System [CGVE].
    </figcaption>
</figure>

- In a **left-handed** coordinate system, the $z$-axis goes **into** the page.
- In a **right-handed** coordinate system, the $z$-axis goes **out** of the
  page.
