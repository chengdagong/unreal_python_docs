# unreal.AnimNotifyState_Trail

```python
class unreal.AnimNotifyState_Trail(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotifyState``


Anim Notify State Trail

**C++ Source:**

- **Module**: Engine

- **File**: AnimNotifyState\_Trail.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `first_socket_name` (Name): [Read-Write] Name of the first socket defining this trail.

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `ps_template` (ParticleSystem): [Read-Write] The particle system to use for this trail.

- `recycle_spawned_systems` (bool): [Read-Write]

- `render_geometry` (bool): [Read-Write] If true, render the trail geometry (this should typically be on)

- `render_spawn_points` (bool): [Read-Write] If true, render stars at each spawned particle point along the trail

- `render_tangents` (bool): [Read-Write] If true, render a line showing the tangent at each spawned particle point along the trail

- `render_tessellation` (bool): [Read-Write] If true, render the tessellated path between spawned particles

- `second_socket_name` (Name): [Read-Write] Name of the second socket defining this trail.

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify state instance should fire in animation editors

- `width_scale_curve` (Name): [Read-Write] Name of the curve to drive the width scale.

- `width_scale_mode` (TrailWidthMode): [Read-Write] Controls the way width scale is applied. In each method a width scale of 1.0 will mean the width is unchanged from the position of the sockets. A width scale of 0.0 will cause a trail of zero width.
From Centre = Trail width is scaled outwards from the centre point between the two sockets.
From First = Trail width is scaled outwards from the position of the first socket.
From Second = Trail width is scaled outwards from the position of the Second socket.



---

_property_ `first_socket_name`: Name

[Read-Only] Name of the first socket defining this trail.

**Type:**

( Name)


---

**override_ps_template**( _mesh_comp_, _animation_) → `ParticleSystem`

Override PSTemplate

Parameters:

- **mesh\_comp** ( _SkeletalMeshComponent_)

- **animation** ( _AnimSequenceBase_)


Return type:

ParticleSystem


---

_property_ `ps_template`: ParticleSystem

[Read-Only] The particle system to use for this trail.

**Type:**

( ParticleSystem)


---

_property_ `recycle_spawned_systems`: bool

[Read-Only]

**Type:**

( bool)


---

_property_ `second_socket_name`: Name

[Read-Only] Name of the second socket defining this trail.

**Type:**

( Name)


---

_property_ `width_scale_curve`: Name

[Read-Only] Name of the curve to drive the width scale.

**Type:**

( Name)


---

_property_ `width_scale_mode`: TrailWidthMode

[Read-Only] Controls the way width scale is applied. In each method a width scale of 1.0 will mean the width is unchanged from the position of the sockets. A width scale of 0.0 will cause a trail of zero width.
From Centre = Trail width is scaled outwards from the centre point between the two sockets.
From First = Trail width is scaled outwards from the position of the first socket.
From Second = Trail width is scaled outwards from the position of the Second socket.

**Type:**

( TrailWidthMode)

### Table of Contents

- `unreal.AnimNotifyState_Trail`
  - `AnimNotifyState_Trail`
    - `AnimNotifyState_Trail.first_socket_name`
    - `AnimNotifyState_Trail.override_ps_template()`
    - `AnimNotifyState_Trail.ps_template`
    - `AnimNotifyState_Trail.recycle_spawned_systems`
    - `AnimNotifyState_Trail.second_socket_name`
    - `AnimNotifyState_Trail.width_scale_curve`
    - `AnimNotifyState_Trail.width_scale_mode`