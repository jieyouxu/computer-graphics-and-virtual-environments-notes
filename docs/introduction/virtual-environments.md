# Virtual Environments

## Seeing in 3D

With two human eyes, humans see the world in 3D; each eye perceives the real
world slightly differently, but the brain stitches them together seamlessly
via a 3D stereo-view.

- The difference between these two perceptions is the **binocular disparity**.
    - The disparity is much greater for closer objects than it is for
      further objects.

### Accomodation

**Accomodation** is the process of adjusting the lens to bring points in the
scene into **focus** – this gives rise to effects such as motion blue and
depth-of-field.

### Convergence

**Convergence** is the process of when eyes rotate inwards to focus on objects
that are nearby and rotate outwards for further objects.

- Very powerful cue for 3D vision for perception of **depth** in a scene.

<figure>
    <img src="./convergence.png" width="30%" />
    <figcaption>
        Figure 1: Convergence: eyes rotate inwards for nearer objects [CGVE].
    </figcaption>
</figure>

### Many Cues for 3Dness

#### Convergence and Parallaxes

When you shut one eye, **convergence** still operates which can be a powerful
indication of **depth**.

There is also **head-movement parallax**, where when the observer moves their
head, nearer points move at a faster speed than further points.

- For moving pictures, it is **motion parallax** since the head doesn't move,
  but points in the 2D screen do.

#### Linear Perspective

Notice that

$$
\text{size of image on retina} \propto
    \frac{1}{\text{distance of object from viewer}}
$$

<figure>
    <img src="./linear-perspective.png" width="50%" />
    <figcaption>
        Figure 2: Size of image on retina is inversely proportional to
        distance of object from viewer [CGVE].
    </figcaption>
</figure>

Abstraction for simplicity – assume single point $O$ admits light, forming
image on flat retina. In CG,

- $O$ is usually the **center of projection**.
- Retina is usually the **image plane** (aka **view plane**).

Figure 2 shows side-view of projection of two equal-length vertical bars
$\overline{AB}$ and $\overline{CD}$.

- $\overline{AB}$ projects to $\overline{ba}$.
- $\overline{CD}$ projects to $\overline{dc}$.

Note that $\overline{AB}$ and $\overline{CD}$ are the same length but their
sizes when projected on retina is inversely proportional to distance from $O$.

- Images are also upside-down.

**Perspective** provides significant cue for **depth**.

#### Perspective Lines

Vertical and horizontal **perspective lines** can create illusion of
persective.

<figure>
    <img src="./perspective.png" width="50%" />
    <figcaption>
        Figure 3: Illusion of linear perspective; two grey bars same length
        [CGVE].
    </figcaption>
</figure>

#### Texture Gradient

**Texture Gradient** can also create illusion of perspective.

<figure>
    <img src="./texture-gradient.png" width="50%" />
    <figcaption>
        Figure 3: Illusion of perspective by arrangement of smaller spheres
        [CGVE].
    </figcaption>
</figure>

#### Shadows and Scaling

**Shadows** and **scaling** can also create illusion of persective.

<figure>
    <img src="./shadow-scaling.png" width="50%" />
    <figcaption>
        Figure 4: Illusion of perspective by shadow and scaling
        [CGVE].
    </figcaption>
</figure>

#### Occlusions

When objects **obscure** another, it is a cue that it is closer to the object
being obscured.

<figure>
    <img src="./kaniza-triangle.png" width="50%" />
    <figcaption>
        Figure 5: Illusion of perspective by occlusion, Kaniza's Traingle
        [CGVE].
    </figcaption>
</figure>

#### Lighting

Light energy **falls off inversely proportional to the square of the distance**.

$$
\text{lighting} \propto \frac{1}{\text{distance}^2}
$$

- More distant objects become more washed out and less sharp than closer ones.
- Atomposheric effects can cause distant objects to appear more blue.

!!! note "Omitted"

    Some other effects are omitted for brevity. See [CGVE] for the full
    discussion.
