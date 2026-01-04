# unreal.AnimNotifyState_TimedNiagaraEffect

```python
class unreal.AnimNotifyState_TimedNiagaraEffect(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotifyState``


Timed Niagara Effect Notify
Allows a looping Niagara effect to be played in an animation that will activate
at the beginning of the notify and deactivate at the end.

**C++ Source:**

- **Plugin**: Niagara

- **Module**: NiagaraAnimNotifies

- **File**: AnimNotifyState\_TimedNiagaraEffect.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `apply_rate_scale_as_time_dilation` (bool): [Read-Write] Should we set the animation rate scale as time dilation on the spawn effect?

- `destroy_at_end` (bool): [Read-Write] Whether the Niagara system should be immediately destroyed at the end of the notify state or be allowed to finish

- `location_offset` (Vector): [Read-Write] Offset from the socket or bone to place the Niagara system

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `rotation_offset` (Rotator): [Read-Write] Rotation offset from the socket or bone for the Niagara system

- `scale` (Vector): [Read-Write] Scale to spawn the Niagara system at

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify state instance should fire in animation editors

- `socket_name` (Name): [Read-Write] The socket or bone to attach the system to

- `template` (NiagaraSystem): [Read-Write] The niagara system to spawn for the notify state



---

_property_ `apply_rate_scale_as_time_dilation`: bool

[Read-Only] Should we set the animation rate scale as time dilation on the spawn effect?

**Type:**

( bool)


---

_property_ `destroy_at_end`: bool

[Read-Only] Whether the Niagara system should be immediately destroyed at the end of the notify state or be allowed to finish

**Type:**

( bool)


---

**get_spawned_effect**( _mesh_comp_) → `FXSystemComponent`

Return FXSystemComponent created from SpawnEffect

Parameters:

**mesh\_comp** ( _MeshComponent_)

Return type:

FXSystemComponent


---

_property_ `location_offset`: Vector

[Read-Only] Offset from the socket or bone to place the Niagara system

**Type:**

( Vector)


---

_property_ `rotation_offset`: Rotator

[Read-Only] Rotation offset from the socket or bone for the Niagara system

**Type:**

( Rotator)


---

_property_ `socket_name`: Name

[Read-Only] The socket or bone to attach the system to

**Type:**

( Name)


---

_property_ `template`: NiagaraSystem

[Read-Only] The niagara system to spawn for the notify state

**Type:**

( NiagaraSystem)

### Table of Contents

- `unreal.AnimNotifyState_TimedNiagaraEffect`
  - `AnimNotifyState_TimedNiagaraEffect`
    - `AnimNotifyState_TimedNiagaraEffect.apply_rate_scale_as_time_dilation`
    - `AnimNotifyState_TimedNiagaraEffect.destroy_at_end`
    - `AnimNotifyState_TimedNiagaraEffect.get_spawned_effect()`
    - `AnimNotifyState_TimedNiagaraEffect.location_offset`
    - `AnimNotifyState_TimedNiagaraEffect.rotation_offset`
    - `AnimNotifyState_TimedNiagaraEffect.socket_name`
    - `AnimNotifyState_TimedNiagaraEffect.template`