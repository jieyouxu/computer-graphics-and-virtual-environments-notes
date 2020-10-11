# Modelling and Virtual Environments

## Objects

**Objects** can be considered as some self-contained thing that has
**structure** and **behaviour** (instance of some data structure + set of
functions).

- They have **visual representation(s)**.
- They have **behaviour(s)** in response to "messages" that respond to
    certain events.

## Virtual Environments

Given the definitions of the set of independent objects (but between which
can interact), a **world** (aka **virtual environment**) can be constructed.

- The **world** consists of the set of entities that follows specified laws
  and behaviours as programed.
    - Typically consists of three components:
        1. Content
        2. Geometry
        3. Dynamics

### Contents of a Virtual Environment

The **content** of a VE depends on how it is *modelled*. A VE consists of
a set of objects.

- At any given moment, each object has a **description** and a **state**.

#### Description

An object's **description** includes information about:

- **Geometry**
- **Substance**
- Potential **Behaviours**

##### Geometry

The **geometric description** of an object is defined relative to some
**coordinate frame**.

- Unambiguously determines the **location** and **orientation** of the object,
  at a given moment in time $t$, as well as its **relation** to other objects
  (within the VE).

##### State

The **state description** of an object unambiguously determines its **state**.

- Depends on the **semantics** of the object w.r.t. to the rest of the VE.

#### Actors

A subset of the objects are called **actors**.

$$
\mathrm{Actors} \subseteq \mathrm{Objects}
$$

An **actor** is an object which can
**initiate and iteraction with another object (or actor)**.

##### Participant

A special actor is the **human operator** (aka **participant**) in the VE.

- The participant has some representation within the VE (e.g. cursor, humanoid).

### Example: Scene Database

Suppose a stored **scene database** that contains representations of the
set of all objects within the scene.

- Each object has a **geometric description**, e.g. a collection of
  primitive shapes for construction.
    - Can be at a higher-level, e.g. defined by equations for spheres and
      cylinders.
    - Or lower-level, e.g. triangular mesh that tessellates the surface of the
      object.
- Each object has information for its **material** and
  **physical properties**.
    - Esp. how it reflects light (aka **radiant properties**).
- Other information can also be included.
    - E.g. acoustic properties, behavioural properties.
