# unreal.SpineSettings

```python
class unreal.SpineSettings(spine_bone:RigElementKey=Ellipsis, pitch_angle_max:float=0.0, pitch_stiffness:float=0.0, pitch_damping:float=0.0)
```


**Bases:** ``StructBase``


Spine Settings

**C++ Source:**

- **Plugin**: Locomotor

- **Module**: Locomotor

- **File**: RigUnit\_Locomotor.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `pitch_angle_max` (float): [Read-Write] Default is 30. The maximum angle (in degrees) to lean the spine in the direction of travel.

- `pitch_damping` (float): [Read-Write] Default is 0.9. Typical range is 0-2. Higher values cause spine leaning to dampen quickly.

- `pitch_stiffness` (float): [Read-Write] Default is 150.0. Typical range is 1-200. Higher values cause spine to lean more rapidly towards target direction.

- `spine_bone` (RigElementKey): [Read-Write] The base spine bone. Usually directly below the Pelvis bone. The bone that rotates to lean the whole spine.



---

_property_ `pitch_angle_max`: float

[Read-Write] Default is 30. The maximum angle (in degrees) to lean the spine in the direction of travel.

**Type:**

( float)


---

_property_ `pitch_damping`: float

[Read-Write] Default is 0.9. Typical range is 0-2. Higher values cause spine leaning to dampen quickly.

**Type:**

( float)


---

_property_ `pitch_stiffness`: float

[Read-Write] Default is 150.0. Typical range is 1-200. Higher values cause spine to lean more rapidly towards target direction.

**Type:**

( float)


---

_property_ `spine_bone`: RigElementKey

[Read-Write] The base spine bone. Usually directly below the Pelvis bone. The bone that rotates to lean the whole spine.

**Type:**

( RigElementKey)

### Table of Contents

- `unreal.SpineSettings`
  - `SpineSettings`
    - `SpineSettings.pitch_angle_max`
    - `SpineSettings.pitch_damping`
    - `SpineSettings.pitch_stiffness`
    - `SpineSettings.spine_bone`