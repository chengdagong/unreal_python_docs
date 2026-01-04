# unreal.BodyInstanceCore

```python
class unreal.BodyInstanceCore(simulate_physics:bool=False, enable_gravity:bool=False, update_kinematic_from_simulation:bool=False, gyroscopic_torque_enabled:bool=False, auto_weld:bool=False, start_awake:bool=False, generate_wake_events:bool=False, update_mass_when_scale_changes:bool=False)
```


**Bases:** ``StructBase``


Body Instance Core

**C++ Source:**

- **Module**: PhysicsCore

- **File**: BodyInstanceCore.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `auto_weld` (bool): [Read-Write] If true and is attached to a parent, the two bodies will be joined into a single rigid body. Physical settings like collision profile and body settings are determined by the root

- `enable_gravity` (bool): [Read-Write] If object should have the force of gravity applied

- `generate_wake_events` (bool): [Read-Write] Should ‘wake/sleep’ events fire when this object is woken up or put to sleep by the physics simulation.

- `gyroscopic_torque_enabled` (bool): [Read-Write] Enabled/disables whether this body is affected by gyroscopic torque, mainly useful for long/thin objects that spin

- `override_mass` (bool): [Read-Write] If true, mass will not be automatically computed and you must set it directly

- `simulate_physics` (bool): [Read-Write] If true, this body will use simulation. If false, will be ‘fixed’ (ie kinematic) and move where it is told.
For a Skeletal Mesh Component, simulating requires a physics asset setup and assigned on the SkeletalMesh asset.
For a Static Mesh Component, simulating requires simple collision to be setup on the StaticMesh asset.

- `start_awake` (bool): [Read-Write] If object should start awake, or if it should initially be sleeping

- `update_kinematic_from_simulation` (bool): [Read-Write] When kinematic, whether the actor transform should be updated as a result of movement in the simulation, rather than immediately whenever a target transform is set.

- `update_mass_when_scale_changes` (bool): [Read-Write] If true, it will update mass when scale change \*



---

_property_ `auto_weld`: bool

[Read-Write] If true and is attached to a parent, the two bodies will be joined into a single rigid body. Physical settings like collision profile and body settings are determined by the root

**Type:**

( bool)


---

_property_ `enable_gravity`: bool

[Read-Only] If object should have the force of gravity applied

**Type:**

( bool)


---

_property_ `generate_wake_events`: bool

[Read-Only] Should ‘wake/sleep’ events fire when this object is woken up or put to sleep by the physics simulation.

**Type:**

( bool)


---

_property_ `gyroscopic_torque_enabled`: bool

[Read-Only] Enabled/disables whether this body is affected by gyroscopic torque, mainly useful for long/thin objects that spin

**Type:**

( bool)


---

_property_ `simulate_physics`: bool

[Read-Write] If true, this body will use simulation. If false, will be ‘fixed’ (ie kinematic) and move where it is told.
For a Skeletal Mesh Component, simulating requires a physics asset setup and assigned on the SkeletalMesh asset.
For a Static Mesh Component, simulating requires simple collision to be setup on the StaticMesh asset.

**Type:**

( bool)


---

_property_ `start_awake`: bool

[Read-Only] If object should start awake, or if it should initially be sleeping

**Type:**

( bool)


---

_property_ `update_kinematic_from_simulation`: bool

[Read-Only] When kinematic, whether the actor transform should be updated as a result of movement in the simulation, rather than immediately whenever a target transform is set.

**Type:**

( bool)


---

_property_ `update_mass_when_scale_changes`: bool

[Read-Write] If true, it will update mass when scale change \*

**Type:**

( bool)

### Table of Contents

- `unreal.BodyInstanceCore`
  - `BodyInstanceCore`
    - `BodyInstanceCore.auto_weld`
    - `BodyInstanceCore.enable_gravity`
    - `BodyInstanceCore.generate_wake_events`
    - `BodyInstanceCore.gyroscopic_torque_enabled`
    - `BodyInstanceCore.simulate_physics`
    - `BodyInstanceCore.start_awake`
    - `BodyInstanceCore.update_kinematic_from_simulation`
    - `BodyInstanceCore.update_mass_when_scale_changes`