# unreal.SoundModulationParameterBipolar

```python
class unreal.SoundModulationParameterBipolar(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SoundModulationParameter``


Modulation Parameter that scales normalized, unitless value to bipolar range. Mixes additively.

**C++ Source:**

- **Plugin**: AudioModulation

- **Module**: AudioModulation

- **File**: SoundModulationParameter.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `settings` (SoundModulationParameterSettings): [Read-Write]

- `unit_range` (float): [Read-Write] Unit range of modulator. Range is only enforced at modulation destination.



---

_property_ `unit_range`: float

[Read-Only] Unit range of modulator. Range is only enforced at modulation destination.

**Type:**

( float)

### Table of Contents

- `unreal.SoundModulationParameterBipolar`
  - `SoundModulationParameterBipolar`
    - `SoundModulationParameterBipolar.unit_range`