# Realism and Real-Time

VEs typically need to be rendered and for participants to be tracked in
**real-time** – but the rendered output needs to be sufficiently **realistic**
so that the VE can be sufficiently **immersive**.

- Typically, those two goals are at conflict – realistic rendering often has
  performance penalties that can compromise the real-time requirement. A
  *compromise* is usually required w.r.t. the design goal.

## Geometric Realism

**Geometric realism** refers to a graphical object that has a
**close geometric resemblance** w.r.t. the real-world object being simulated.

A *practical* reason for geometric realism is its application in
**virtual prototyping**, which requires *geometric accuracy* up to a certain
threshold.

- Example: usage of 3D reconstruction of CT/NMR scans for patients for
  reconstructive surgery to help the surgeons to visualize the patient's
  situation.

If the geometry is insufficiently accurate then it may be misleading and cause
negative contribution.

## Illumination Realism

**Illumination** is an important consideration for visual prototyping as well –
lighting certainly affects how objects present to observers.

- Example: in architecture design lighting often is part of functional
  requirements, e.g. so users won't trip because of poorly illuminated
  obstacles.

**Correct** lighting needs to take into account **interreflections** between
surfaces of objects in the scene (also refraction in case of translucent
objects), and not only the impact of light sources on individual objects in
isolation.

- Considering impact of light sources on individual objects in isolation is
  **local illumination**.
- **Global illumination** considers a correct computation of lighting
  distribution within a VE, taking into account inter-object reflections and
  refractions.
    - Also referred to as **photo-realism**, to simulate those taken by actual
      cameras to the point of being indistinguishable.

## Behaviour Realism

A graphical object may not necessarily be geometrically nor illuminatively
realistic, but its **behaviour** can be sufficiently realistic to elicit
emotional responses from the observer.

- Example: cartoons, often not "real" geometrically or illuminatively, but
  still can trigger emotional responses – sometimes even by distortions of
  "reality" on purposes, such as exaggeration.

### Caricatures, Impressionism and Iconic Representations

Sometimes graphical works rely on external contextual information that is not
intrinsically contained within the information available to the VE, but needs
the observer to "piece them together."

## Tension Between Realism and Real-Time

The ideal "realism" in CG refers to geometric, behavioural and illumination
realism, but are increasing difficult and come at cost of real-time performance,
but VR needs real-time performance to function.

### Real-Time

Computers generate *illusion* of movement and changes on a display via the same
techniques as animated cartoons or movies (aka moving pictures), by rapidly
displaying many images in a correctly-ordered contiguous sequence many times
per second.

- Each of such image is a **frame**.
- The **frame rate** is defined as the number of images displayed per second,
  and is measured in **Hertz** ($\text{Hz}$).
    - $60\ \text{Hz}$ imply $60$ images displayed per second.
- If the frame rate is sufficiently fast, the human observer cannot tell that
  individual frames are being rendered and swapped, but will see a continously
  changing scene.

A real-time requirement imposes restrictions on computer resources, such as
disk access, network bandwidth, memory and display. This requires
**compromises** to be made.

- Some aspects of illumination *must* be sacrificed.
    - In a complex scene, often not possible to display each object with
      full geometric realism.
- Simplications of some physical laws are typically also needed.
