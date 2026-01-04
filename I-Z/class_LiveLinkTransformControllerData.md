# unreal.LiveLinkTransformControllerData

```python
class unreal.LiveLinkTransformControllerData(world_transform:bool=False, use_location:bool=False, use_rotation:bool=False, use_scale:bool=False, sweep:bool=False, teleport:bool=False)
```


**Bases:** ``StructBase``


Live Link Transform Controller Data

**C++ Source:**

- **Plugin**: LiveLink

- **Module**: LiveLinkComponents

- **File**: LiveLinkTransformController.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `sweep` (bool): [Read-Write] Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something.
Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- `teleport` (bool): [Read-Write] Whether we teleport the physics state (if physics collision is enabled for this object).
If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location).
If false, physics velocity is updated based on the change in position (affecting ragdoll parts).
If CCD is on and not teleporting, this will affect objects along the entire sweep volume.

- `use_location` (bool): [Read-Write] Whether we should set the owning actor’s location with the value coming from live link.

- `use_rotation` (bool): [Read-Write] Whether we should set the owning actor’s rotation with the value coming from live link.

- `use_scale` (bool): [Read-Write] Whether we should set the owning actor’s scale with the value coming from live link.

- `world_transform` (bool): [Read-Write] Set the transform of the component in world space of in its local reference frame.



---

_property_ `sweep`: bool

[Read-Write] Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something.
Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

**Type:**

( bool)


---

_property_ `teleport`: bool

[Read-Write] Whether we teleport the physics state (if physics collision is enabled for this object).
If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location).
If false, physics velocity is updated based on the change in position (affecting ragdoll parts).
If CCD is on and not teleporting, this will affect objects along the entire sweep volume.

**Type:**

( bool)


---

_property_ `use_location`: bool

[Read-Write] Whether we should set the owning actor’s location with the value coming from live link.

**Type:**

( bool)


---

_property_ `use_rotation`: bool

[Read-Write] Whether we should set the owning actor’s rotation with the value coming from live link.

**Type:**

( bool)


---

_property_ `use_scale`: bool

[Read-Write] Whether we should set the owning actor’s scale with the value coming from live link.

**Type:**

( bool)


---

_property_ `world_transform`: bool

[Read-Write] Set the transform of the component in world space of in its local reference frame.

**Type:**

( bool)

### Table of Contents

- `unreal.LiveLinkTransformControllerData`
  - `LiveLinkTransformControllerData`
    - `LiveLinkTransformControllerData.sweep`
    - `LiveLinkTransformControllerData.teleport`
    - `LiveLinkTransformControllerData.use_location`
    - `LiveLinkTransformControllerData.use_rotation`
    - `LiveLinkTransformControllerData.use_scale`
    - `LiveLinkTransformControllerData.world_transform`