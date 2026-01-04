# unreal.AnimNotify_PlaySound

```python
class unreal.AnimNotify_PlaySound(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotify``


Anim Notify Play Sound

**C++ Source:**

- **Module**: Engine

- **File**: AnimNotify\_PlaySound.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `attach_name` (Name): [Read-Write] Socket or bone name to attach sound to

- `follow` (bool): [Read-Write] If this sound should follow its owner

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `pitch_multiplier` (float): [Read-Write] Pitch Multiplier

- `preview_ignore_attenuation` (bool): [Read-Write]

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify instance should fire in animation editors

- `sound` (SoundBase): [Read-Write] Sound to Play

- `volume_multiplier` (float): [Read-Write] Volume Multiplier



---

_property_ `attach_name`: Name

[Read-Only] Socket or bone name to attach sound to

**Type:**

( Name)


---

_property_ `follow`: bool

[Read-Only] If this sound should follow its owner

**Type:**

( bool)


---

_property_ `pitch_multiplier`: float

[Read-Only] Pitch Multiplier

**Type:**

( float)


---

_property_ `sound`: SoundBase

[Read-Only] Sound to Play

**Type:**

( SoundBase)


---

_property_ `volume_multiplier`: float

[Read-Only] Volume Multiplier

**Type:**

( float)

### Table of Contents

- `unreal.AnimNotify_PlaySound`
  - `AnimNotify_PlaySound`
    - `AnimNotify_PlaySound.attach_name`
    - `AnimNotify_PlaySound.follow`
    - `AnimNotify_PlaySound.pitch_multiplier`
    - `AnimNotify_PlaySound.sound`
    - `AnimNotify_PlaySound.volume_multiplier`