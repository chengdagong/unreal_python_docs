# unreal.AINoiseEvent

```python
class unreal.AINoiseEvent(noise_location:Vector=Ellipsis, loudness:float=0.0, max_range:float=0.0, instigator:Actor=Ellipsis, tag:Name='None')
```


**Bases:** ``StructBase``


AINoise Event

**C++ Source:**

- **Module**: AIModule

- **File**: AISense\_Hearing.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `instigator` (Actor): [Read-Write] Actor triggering the sound.

- `loudness` (float): [Read-Write] Loudness modifier of the sound.
If MaxRange is non-zero, this modifies the range (by multiplication).
If there is no MaxRange, then if Square(DistanceToSound) <= Square(HearingRange \* Loudness), the sound is heard, false otherwise.

- `max_range` (float): [Read-Write] Max range at which the sound can be heard. Multiplied by Loudness.
A value of 0 indicates that there is no range limit, though listeners are still limited by their own hearing range.

- `noise_location` (Vector): [Read-Write] if not set Instigator’s location will be used

- `tag` (Name): [Read-Write] Named identifier for the noise.



---

_property_ `instigator`: Actor

[Read-Write] Actor triggering the sound.

**Type:**

( Actor)


---

_property_ `loudness`: float

[Read-Write] Loudness modifier of the sound.
If MaxRange is non-zero, this modifies the range (by multiplication).
If there is no MaxRange, then if Square(DistanceToSound) <= Square(HearingRange \* Loudness), the sound is heard, false otherwise.

**Type:**

( float)


---

_property_ `max_range`: float

[Read-Write] Max range at which the sound can be heard. Multiplied by Loudness.
A value of 0 indicates that there is no range limit, though listeners are still limited by their own hearing range.

**Type:**

( float)


---

_property_ `noise_location`: Vector

[Read-Write] if not set Instigator’s location will be used

**Type:**

( Vector)


---

_property_ `tag`: Name

[Read-Write] Named identifier for the noise.

**Type:**

( Name)

### Table of Contents

- `unreal.AINoiseEvent`
  - `AINoiseEvent`
    - `AINoiseEvent.instigator`
    - `AINoiseEvent.loudness`
    - `AINoiseEvent.max_range`
    - `AINoiseEvent.noise_location`
    - `AINoiseEvent.tag`