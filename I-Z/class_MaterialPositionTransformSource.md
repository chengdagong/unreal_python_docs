# unreal.MaterialPositionTransformSource

```python
class unreal.MaterialPositionTransformSource
```


**Bases:** ``EnumBase``


EMaterial Position Transform Source

**C++ Source:**

- **Module**: Engine

- **File**: MaterialExpressionTransformPosition.h


TRANSFORMPOSSOURCE\_CAMERA _: MaterialPositionTransformSource_ _=Ellipsis_

Camera space

**Type:**

6

TRANSFORMPOSSOURCE\_FIRST\_PERSON\_TRANSLATED\_WORLD _: MaterialPositionTransformSource_ _=Ellipsis_

First person “space”, which can be thought of as a transform that is applied to a position in translated world space.

**Type:**

4

TRANSFORMPOSSOURCE\_INSTANCE _: MaterialPositionTransformSource_ _=Ellipsis_

Instance space (used to provide per instance transform, i.e. for Instanced Static Mesh / Particles).

**Type:**

8

TRANSFORMPOSSOURCE\_LOCAL _: MaterialPositionTransformSource_ _=Ellipsis_

Local space

**Type:**

0

TRANSFORMPOSSOURCE\_PERIODIC\_WORLD _: MaterialPositionTransformSource_ _=Ellipsis_

Like absolute world space, but the world origin is moved to the center of the tile the camera is in.
Logically similar to fmod(CameraAbsoluteWorldPosition, TileSize) + CameraRelativeWorldPosition.
This offers better precision and scalability than absolute world position.
Suitable as a position input for functions that tile based on world position, e.g. frac(Position / TileSize).
Works best when the tile size is a power of two.

**Type:**

2

TRANSFORMPOSSOURCE\_TRANSLATED\_WORLD _: MaterialPositionTransformSource_ _=Ellipsis_

Translated world space, i.e. world space rotation and scale but with a position relative to the camera

**Type:**

3

TRANSFORMPOSSOURCE\_VIEW _: MaterialPositionTransformSource_ _=Ellipsis_

View space (differs from camera space in the shadow passes)

**Type:**

5

TRANSFORMPOSSOURCE\_WORLD _: MaterialPositionTransformSource_ _=Ellipsis_

Absolute world space

**Type:**

1

### Table of Contents

- `unreal.MaterialPositionTransformSource`
  - `MaterialPositionTransformSource`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_CAMERA`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_FIRST_PERSON_TRANSLATED_WORLD`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_INSTANCE`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_LOCAL`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_PERIODIC_WORLD`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_TRANSLATED_WORLD`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_VIEW`
    - `MaterialPositionTransformSource.TRANSFORMPOSSOURCE_WORLD`