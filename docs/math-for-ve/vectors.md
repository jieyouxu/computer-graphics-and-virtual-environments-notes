# Vectors

## Subspaces of Vector Spaces

A vector space $V_0$ is a **subspace** of vector space $V$ iff $V_0 \subset V$
and linear operations on $V_0$ is consistent with that of $V$.

A subset $S$ of vector space $V$ is a subspace of $V$ iff $S \neq \varnothing$
and **closed under linear operations**:

1. $\vb{x}, \vb{y} \in S \implies \vb{x} + \vb{y} \in S$.
2. $\forall r \in \mathbb{R} \colon \vb{x} \in S \implies r\vb{x} \in S$.

Note that:

- Zero vector in subspace is the same as the zero vector in $V$.
- Subtraction in subspace agrees with $V$.

If we let $V$ be a vector space and $\vb{x}_1, \dots, \vb{x}_n \in V$, then the
set $L$ of all linear combinations

$$
\sum_{i=1}^{n} r_i \vb{x}_i
$$

where $r_i \in \mathbb{R}$ is a subspace of $V$.

## Span

### Implicit Definition

Let $S$ be a subset of vector space $V$, then the **span** of set $S$
($\mathrm{span}(S)$) is the **smallest subspace $V$ that contains $S$**:

1. $\mathrm{span}$ is a subspace of $V$.
2. For any subspace $W \subset V$,
   $S \subset W \implies \mathrm{span}(S) \subset W$.

The span of any set $S \subset V$ is well defined, as the intersection of all
subspaces of $V$ that contains $S$.

### Effective Description

Let $S$ be a subset of vector space $V$.

- If $S = \{ \vb{v}_1, \dots, \vb{v}_n \}$ then $\mathrm{S}$ is the set of all
  **linear combinations** where $r_i \in \mathbb{R}$:

    $$
    r_1 \vb{v}_1 + \cdots + r_n \vb{v}_n
    $$

- If $S = \varnothing$ then $\mathrm{span}(S) = \{ \vb{0} \}$.

## Spanning Set

A subset $S$ of vector space $V$ is a **spanning set** for $V$ iff

$$
\mathrm{span}(S) = V
$$

## Basis

A set $B$ of vectors in vector space $V$ is a **basis** iff every element of
$V$ can be written in a unique way as a finite **linear combination** of
elements of $B$.

A set $B \subset V$ is a **basis** iff (for some field $F$ such as the
real numbers $\mathrm{R}$):

1. It has the **linear independence property**:
    - For every finite subset $\{ v_1, \dots, v_m \}$ of $B$, if
      $c_1 v_1 + \cdots + c_m v_m = 0$ for some $c_1, \dots, c_m \in F$, then
      $c_1 = \cdots = c_m = 0$.
2. It has the **spanning property**:
    - For every vector $v \in V$, one can choose $a_1, \dots, a_n \in F$ and
      $v_1, \dots, v_n \in B$ such that $v = a_1 v_1 + \cdots + a_n v_n$.

<figure>
    <img src="./vector.png" width="50%" />
    <figcaption>
        Figure 2: Vector [CGVE].
    </figcaption>
</figure>

A **vector** $\vb{v}$ is a difference of two **points** $P_1$ and $P_2$

$$
\vb{v} = P_2 - P_1
$$

By corollary, a **point** can be specified as an addition of a point with a
vector

$$
P_2 = \vb{v} + P_1
$$

Note that a **point** $P_1 = (x, y, z)$ can also be converted into vector
$\overline{OP}$ from the origin,

$$
\overline{OP} = \begin{bmatrix}
    x \\
    y \\
    z
\end{bmatrix}
$$

## Vector Addition

Two vectors $\vb{u} = [x_1, y_1, z_1]^T, \vb{v} = [x_2, y_2, z_2]^T$ can be
summed provided they have matching dimensions

$$
\vb{u} + \vb{v} =
    \begin{bmatrix} x_1 \\ y_1 \\ z_1 \end{bmatrix}
    + \begin{bmatrix} x_1 \\ y_2 \\ z_2 \end{bmatrix} \\
    = \begin{bmatrix} x_1 + x_2 \\ y_1 + y_2 \\ z_1 + z_2 \end{bmatrix}
$$

This can be visually depicted via the parallelogram rule.

<figure>
    <img src="./parallelogram-rule.png" width="50%" />
    <figcaption>
        Figure 3: Vector addition via the parallelogram rule [CGVE].
    </figcaption>
</figure>

## Scaling by Scalar

Any vector $\vb{v} = [x, y, z]^T$ can be scaled by the scalar
$\lambda \in \mathbb{R}$

$$
\lambda \vb{v} = \begin{bmatrix}
    \lambda x \\ \lambda y \\ \lambda z \end{bmatrix}
$$

The resulting vector $\lambda \vb{v}$ is a new vector that *preserves* the
**direction**, iff $\lambda > 0$. The direction is flipped if $\lambda < 0$.

The new length is computed by

$$
\abs{\lambda \vb{v}} = \abs{\lambda}\abs{\vb{v}}
$$

Then, for any two vectors $\vb{v}_1, \vb{v}_2$ and any two real numbers
$\lambda_1, \lambda_2$, $\lambda_1 \vb{v}_1 + \lambda_2 \vb{v}_2$ is also a
vector.

## Vector Norm

The three vectors

$$
\hat{\imath} = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} \quad
\hat{\jmath} = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} \quad
\hat{k} =      \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}
$$

form the **basis** of the $\mathbb{R}^3$ 3D vector space, such that any point
$P(x, y, z)$ can be expressed as a linear combination of
$\{ \hat{\imath}, \hat{\jmath}, \hat{k} \}$, since

$$
\begin{bmatrix} x \\ y \\ z \end{bmatrix} =
    x \hat{\imath} + y \hat{\jmath} + z \hat{k}
$$

The $\ell_2$-norm $\abs{\vb{v}}$ (i.e. Euclidean distance) of a 3D vector
$\vb{v}$ gives its length, and is defined as

$$
\abs{\vb{v}} = \sqrt{x^2 + y^2 + z^2}
$$

which is the distance from the origin to point $(x, y, z)$.

## Unit Vector

A unit vector $\vu{v}$ has the same **direction** as vector $\vb{v}$ but ensures
that $\abs{\vu{v}} = 1$. $\vu{v}$ can be derived from $\vb{v}$ by
**normalizing** $\vb{v}$ via

$$
\vu{v} = \frac{\vb{v}}{\abs{\vb{v}}}
$$

## Inner (Dot) Product of Two Vectors

Given two vectors $\vb{v}_1 = [x_1, y_1, z_1], \vb{v}_2 = [x_2, y_2, z_2]$ then
their **dot product** $\vb{v}_1 \bullet \vb{v}_2$ is given by

$$
\vb{v}_1 \bullet \vb{v}_2 =
    \begin{bmatrix} x_1 \\ y_1 \\ z_1 \end{bmatrix}
    \bullet \begin{bmatrix} x_2 \\ y_2 \\ z_2 \end{bmatrix}
    = x_1 x_2 + y_1 y_2 + z_1 z_2
$$

If we **normalize** each of the vectors $\vb{v}_1, \vb{v}_2$ to give
$\vu{v}_1, \vu{v}_2$, then

$$
\cos(\theta) = \frac{\vb{v}_1 \bullet \vb{v}_2}{\abs{\vb{v}_1} \abs{\vb{v}_2}}
= \vu{v}_1 \bullet \vu{v}_2
$$

where $\theta$ is the angle between $\vb{v}_1$ and $\vb{v}_2$.

The dot product is **proportional** to the cosine of the angle between the two
vectors. Since $\cos(0) = 1$ and $\cos(\frac{\pi}{2}) = 0$, then it means:

- The dot product of a unit vector with itself is $1$.
- Vectors that are **orthogonal** to each other has dot product of $0$.

## Cross Product

Given two vectors $\vb{a} = [a_1, a_2, a_3], \vb{b} = [b_1, b_2, b_3]$ then
their **cross product** $\vb{a} \times \vb{b}$ is given by

$$
\begin{align}
\vb{a} \cross \vb{b} &=
    \mqty| \vu{i} & \vu{j} & \vu{k} \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 | \\
    &= \mqty| a_2 & a_3 \\ b_2 & b_3 | \vu{i}
        - \mqty| a_1 & a_3 \\ b_1 & b_3 | \vu{j}
        + \mqty| a_1 & a_2 \\ b_1 & b_2 | \vu{k} \\
    &= (a_2 b_3 - a_3 b_2) \vu{i} - (a_1 b_3 - a_3 b_1) \vu{j}
        + (a_1 b_2 - a_2 b_1) \vu{k}
\end{align}
$$

An property of this cross product is given by

$$
\abs{\vb{a} \times \vb{b}} = \abs{\vb{a}} \abs{\vb{b}} \sin(\theta)
$$

where $\theta$ is the angle between the two vectors.

Note that $\vb{a} \times \vb{b}$ is **orthogonal** to both $\vb{a}$ and
$\vb{b}$, and the length of $\vb{a} \times \vb{b}$ is the longest when
$\theta = \frac{\pi}{2}$ since $\sin(\frac{\pi}{2}) = 1$.

- When $\vb{a}$ and $\vb{b}$ are parallel or coincides, then their cross product
  is $\vb{0}$.

<figure>
    <img src="./parallelogram-rule.png" width="50%" />
    <figcaption>
        Figure 4: Cross product forms a normal [CGVE].
    </figcaption>
</figure>
