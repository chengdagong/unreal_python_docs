# unreal.InputModifierDeadZone

```python
class unreal.InputModifierDeadZone(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``InputModifier``


Dead Zone
Input values within the range LowerThreshold -> UpperThreshold will be remapped from 0 -> 1.
Values outside this range will be clamped.

**C++ Source:**

- **Plugin**: EnhancedInput

- **Module**: EnhancedInput

- **File**: InputModifiers.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `lower_threshold` (float): [Read-Write] Threshold below which input is ignored
This value should always be lower then the UpperThreshold.

- `type` (DeadZoneType): [Read-Write]

- `upper_threshold` (float): [Read-Write] Threshold above which input is clamped to 1



---

_property_ `lower_threshold`: float

[Read-Write] Threshold below which input is ignored
This value should always be lower then the UpperThreshold.

**Type:**

( float)


---

_property_ `type`: DeadZoneType

[Read-Write]

**Type:**

( DeadZoneType)


---

_property_ `upper_threshold`: float

[Read-Write] Threshold above which input is clamped to 1

**Type:**

( float)

### Table of Contents

- `unreal.InputModifierDeadZone`
  - `InputModifierDeadZone`
    - `InputModifierDeadZone.lower_threshold`
    - `InputModifierDeadZone.type`
    - `InputModifierDeadZone.upper_threshold`