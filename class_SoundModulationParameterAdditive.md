# unreal.SoundModulationParameterAdditive

```python
class unreal.SoundModulationParameterAdditive(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SoundModulationParameter``


Modulation Parameter whose values are mixed via addition.

**C++ Source:**

- **Plugin**: AudioModulation

- **Module**: AudioModulation

- **File**: SoundModulationParameter.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `settings` (SoundModulationParameterSettings): [Read-Write]

- `unit_max` (float): [Read-Write] Unit maximum of modulator. Maximum is only enforced at modulation destination.

- `unit_min` (float): [Read-Write] Unit minimum of modulator. Minimum is only enforced at modulation destination.



---

_property_ `unit_max`: float

[Read-Only] Unit maximum of modulator. Maximum is only enforced at modulation destination.

**Type:**

( float)


---

_property_ `unit_min`: float

[Read-Only] Unit minimum of modulator. Minimum is only enforced at modulation destination.

**Type:**

( float)

### Table of Contents

- `unreal.SoundModulationParameterAdditive`
  - `SoundModulationParameterAdditive`
    - `SoundModulationParameterAdditive.unit_max`
    - `SoundModulationParameterAdditive.unit_min`