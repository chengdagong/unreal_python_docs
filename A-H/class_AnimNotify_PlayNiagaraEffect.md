# unreal.AnimNotify_PlayNiagaraEffect

```python
class unreal.AnimNotify_PlayNiagaraEffect(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotify``


Anim Notify Play Niagara Effect

**C++ Source:**

- **Plugin**: Niagara

- **Module**: NiagaraAnimNotifies

- **File**: AnimNotify\_PlayNiagaraEffect.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_scale` (bool): [Read-Write] Whether or not we are in absolute scale mode

- `attached` (bool): [Read-Write] Should attach to the bone/socket

- `location_offset` (Vector): [Read-Write] Location offset from the socket

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `rotation_offset` (Rotator): [Read-Write] Rotation offset from socket

- `scale` (Vector): [Read-Write] Scale to spawn the Niagara system at

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify instance should fire in animation editors

- `socket_name` (Name): [Read-Write] SocketName to attach to

- `template` (NiagaraSystem): [Read-Write] Niagara System to Spawn



---

_property_ `attached`: bool

[Read-Only] Should attach to the bone/socket

**Type:**

( bool)


---

**get_spawned_effect**() → `FXSystemComponent`

Return FXSystemComponent created from SpawnEffect

Return type:

FXSystemComponent


---

_property_ `location_offset`: Vector

[Read-Only] Location offset from the socket

**Type:**

( Vector)


---

_property_ `rotation_offset`: Rotator

[Read-Only] Rotation offset from socket

**Type:**

( Rotator)


---

_property_ `socket_name`: Name

[Read-Only] SocketName to attach to

**Type:**

( Name)


---

_property_ `template`: NiagaraSystem

[Read-Only] Niagara System to Spawn

**Type:**

( NiagaraSystem)

### Table of Contents

- `unreal.AnimNotify_PlayNiagaraEffect`
  - `AnimNotify_PlayNiagaraEffect`
    - `AnimNotify_PlayNiagaraEffect.attached`
    - `AnimNotify_PlayNiagaraEffect.get_spawned_effect()`
    - `AnimNotify_PlayNiagaraEffect.location_offset`
    - `AnimNotify_PlayNiagaraEffect.rotation_offset`
    - `AnimNotify_PlayNiagaraEffect.socket_name`
    - `AnimNotify_PlayNiagaraEffect.template`