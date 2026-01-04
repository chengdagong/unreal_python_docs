# unreal.ChaosBreakEvent

```python
class unreal.ChaosBreakEvent(component:PrimitiveComponent=Ellipsis, location:Vector=Ellipsis, orientation:Quat=Ellipsis, velocity:Vector=Ellipsis, angular_velocity:Vector=Ellipsis, extents:Vector=Ellipsis, mass:float=0.0, index:int=0, from_crumble:bool=False)
```


**Bases:** ``StructBase``


Chaos Break Event

**C++ Source:**

- **Module**: Engine

- **File**: ChaosEventType.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `angular_velocity` (Vector): [Read-Write] Angular Velocity of the breaking particle

- `component` (PrimitiveComponent): [Read-Write] primitive component involved in the break event

- `extents` (Vector): [Read-Write] Extents of the bounding box in local space of the breaking piece

- `from_crumble` (bool): [Read-Write] Whether the break event originated from a crumble event

- `index` (int32): [Read-Write] Index of the geometry collection bone if positive

- `location` (Vector): [Read-Write] World location of the breaking piece

- `mass` (float): [Read-Write] Mass of the breaking particle

- `orientation` (Quat): [Read-Write] World orientation of the breaking piece

- `velocity` (Vector): [Read-Write] Linear Velocity of the breaking particle



---

_property_ `angular_velocity`: Vector

[Read-Only] Angular Velocity of the breaking particle

**Type:**

( Vector)


---

_property_ `component`: PrimitiveComponent

[Read-Only] primitive component involved in the break event

**Type:**

( PrimitiveComponent)


---

_property_ `extents`: Vector

[Read-Only] Extents of the bounding box in local space of the breaking piece

**Type:**

( Vector)


---

_property_ `from_crumble`: bool

[Read-Only] Whether the break event originated from a crumble event

**Type:**

( bool)


---

_property_ `index`: int

[Read-Only] Index of the geometry collection bone if positive

**Type:**

(int32)


---

_property_ `location`: Vector

[Read-Only] World location of the breaking piece

**Type:**

( Vector)


---

_property_ `mass`: float

[Read-Only] Mass of the breaking particle

**Type:**

( float)


---

_property_ `orientation`: Quat

[Read-Only] World orientation of the breaking piece

**Type:**

( Quat)


---

_property_ `velocity`: Vector

[Read-Only] Linear Velocity of the breaking particle

**Type:**

( Vector)

### Table of Contents

- `unreal.ChaosBreakEvent`
  - `ChaosBreakEvent`
    - `ChaosBreakEvent.angular_velocity`
    - `ChaosBreakEvent.component`
    - `ChaosBreakEvent.extents`
    - `ChaosBreakEvent.from_crumble`
    - `ChaosBreakEvent.index`
    - `ChaosBreakEvent.location`
    - `ChaosBreakEvent.mass`
    - `ChaosBreakEvent.orientation`
    - `ChaosBreakEvent.velocity`