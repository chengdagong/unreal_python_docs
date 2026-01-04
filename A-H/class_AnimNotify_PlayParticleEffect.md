# unreal.AnimNotify_PlayParticleEffect

```python
class unreal.AnimNotify_PlayParticleEffect(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotify``


Anim Notify Play Particle Effect

**C++ Source:**

- **Module**: Engine

- **File**: AnimNotify\_PlayParticleEffect.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `attached` (bool): [Read-Write] Should attach to the bone/socket

- `location_offset` (Vector): [Read-Write] Location offset from the socket

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `ps_template` (ParticleSystem): [Read-Write] Particle System to Spawn

- `rotation_offset` (Rotator): [Read-Write] Rotation offset from socket

- `scale` (Vector): [Read-Write] Scale to spawn the particle system at

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify instance should fire in animation editors

- `socket_name` (Name): [Read-Write] SocketName to attach to



---

_property_ `attached`: bool

[Read-Only] Should attach to the bone/socket

**Type:**

( bool)


---

_property_ `location_offset`: Vector

[Read-Only] Location offset from the socket

**Type:**

( Vector)


---

_property_ `ps_template`: ParticleSystem

[Read-Only] Particle System to Spawn

**Type:**

( ParticleSystem)


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

### Table of Contents

- `unreal.AnimNotify_PlayParticleEffect`
  - `AnimNotify_PlayParticleEffect`
    - `AnimNotify_PlayParticleEffect.attached`
    - `AnimNotify_PlayParticleEffect.location_offset`
    - `AnimNotify_PlayParticleEffect.ps_template`
    - `AnimNotify_PlayParticleEffect.rotation_offset`
    - `AnimNotify_PlayParticleEffect.socket_name`