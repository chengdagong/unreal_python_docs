# unreal.SphericalPontoon

```python
class unreal.SphericalPontoon(center_socket:Name='None', relative_location:Vector=Ellipsis, radius:float=0.0, fx_enabled:bool=False, local_force:Vector=Ellipsis, center_location:Vector=Ellipsis, socket_rotation:Quat=Ellipsis, offset:Vector=Ellipsis, water_height:float=0.0, water_depth:float=0.0, immersion_depth:float=0.0, water_plane_location:Vector=Ellipsis, water_plane_normal:Vector=Ellipsis, water_surface_position:Vector=Ellipsis, water_velocity:Vector=Ellipsis, water_body_index:int=0, is_in_water:bool=False, current_water_body_component:WaterBodyComponent=Ellipsis)
```


**Bases:** ``StructBase``


Spherical Pontoon

**C++ Source:**

- **Plugin**: Water

- **Module**: Water

- **File**: BuoyancyTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `center_location` (Vector): [Read-Write]

- `center_socket` (Name): [Read-Write] The socket to center this pontoon on. Also used as the name of the pontoon for effects

- `current_water_body_component` (WaterBodyComponent): [Read-Write]

- `fx_enabled` (bool): [Read-Write] Should this pontoon be considered as a candidate location for visual/audio effects upon entering water for burst cues? To be implemented by user

- `immersion_depth` (float): [Read-Write]

- `is_in_water` (bool): [Read-Write]

- `local_force` (Vector): [Read-Write]

- `offset` (Vector): [Read-Write]

- `radius` (float): [Read-Write] The radius of the pontoon

- `relative_location` (Vector): [Read-Write] Relative Location of pontoon WRT parent actor. Overridden by Center Socket.

- `socket_rotation` (Quat): [Read-Write]

- `water_body_index` (int32): [Read-Write]

- `water_depth` (float): [Read-Write]

- `water_height` (float): [Read-Write]

- `water_plane_location` (Vector): [Read-Write]

- `water_plane_normal` (Vector): [Read-Write]

- `water_surface_position` (Vector): [Read-Write]

- `water_velocity` (Vector): [Read-Write]



---

_property_ `center_location`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `center_socket`: Name

[Read-Only] The socket to center this pontoon on. Also used as the name of the pontoon for effects

**Type:**

( Name)


---

_property_ `current_water_body_component`: WaterBodyComponent

[Read-Only]

**Type:**

( WaterBodyComponent)


---

_property_ `fx_enabled`: bool

[Read-Only] Should this pontoon be considered as a candidate location for visual/audio effects upon entering water for burst cues? To be implemented by user

**Type:**

( bool)


---

_property_ `immersion_depth`: float

[Read-Only]

**Type:**

( float)


---

_property_ `is_in_water`: bool

[Read-Only]

**Type:**

( bool)


---

_property_ `local_force`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `offset`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `radius`: float

[Read-Only] The radius of the pontoon

**Type:**

( float)


---

_property_ `relative_location`: Vector

[Read-Only] Relative Location of pontoon WRT parent actor. Overridden by Center Socket.

**Type:**

( Vector)


---

_property_ `socket_rotation`: Quat

[Read-Only]

**Type:**

( Quat)


---

_property_ `water_body_index`: int

[Read-Only]

**Type:**

(int32)


---

_property_ `water_depth`: float

[Read-Only]

**Type:**

( float)


---

_property_ `water_height`: float

[Read-Only]

**Type:**

( float)


---

_property_ `water_plane_location`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `water_plane_normal`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `water_surface_position`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `water_velocity`: Vector

[Read-Only]

**Type:**

( Vector)

### Table of Contents

- `unreal.SphericalPontoon`
  - `SphericalPontoon`
    - `SphericalPontoon.center_location`
    - `SphericalPontoon.center_socket`
    - `SphericalPontoon.current_water_body_component`
    - `SphericalPontoon.fx_enabled`
    - `SphericalPontoon.immersion_depth`
    - `SphericalPontoon.is_in_water`
    - `SphericalPontoon.local_force`
    - `SphericalPontoon.offset`
    - `SphericalPontoon.radius`
    - `SphericalPontoon.relative_location`
    - `SphericalPontoon.socket_rotation`
    - `SphericalPontoon.water_body_index`
    - `SphericalPontoon.water_depth`
    - `SphericalPontoon.water_height`
    - `SphericalPontoon.water_plane_location`
    - `SphericalPontoon.water_plane_normal`
    - `SphericalPontoon.water_surface_position`
    - `SphericalPontoon.water_velocity`