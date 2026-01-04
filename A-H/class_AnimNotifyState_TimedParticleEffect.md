# unreal.AnimNotifyState_TimedParticleEffect

```python
class unreal.AnimNotifyState_TimedParticleEffect(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotifyState``


Timed Particle Effect Notify
Allows a looping particle effect to be played in an animation that will activate
at the beginning of the notify and deactivate at the end.

**C++ Source:**

- **Module**: Engine

- **File**: AnimNotifyState\_TimedParticleEffect.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `destroy_at_end` (bool): [Read-Write] Whether the particle system should be immediately destroyed at the end of the notify state or be allowed to finish

- `location_offset` (Vector): [Read-Write] Offset from the socket or bone to place the particle system

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `ps_template` (ParticleSystem): [Read-Write] The particle system to spawn for the notify state

- `rotation_offset` (Rotator): [Read-Write] Rotation offset from the socket or bone for the particle system

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify state instance should fire in animation editors

- `socket_name` (Name): [Read-Write] The socket or bone to attach the system to


### Table of Contents

- `unreal.AnimNotifyState_TimedParticleEffect`
  - `AnimNotifyState_TimedParticleEffect`