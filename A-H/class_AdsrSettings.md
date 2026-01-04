# unreal.AdsrSettings

```python
class unreal.AdsrSettings
```


**Bases:** ``StructBase``


Adsr Settings

**C++ Source:**

- **Plugin**: Harmonix

- **Module**: HarmonixDsp

- **File**: AdsrSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `attack_curve` (float): [Read-Write] \* Control the shape of the attack curve:
\\* 0: Linear
\\* <0: Exponential
\\* >0: Logarithmic

- `attack_time` (float): [Read-Write]

- `decay_curve` (float): [Read-Write] \* Control the shape of the attack curve:
\\* 0: Linear
\\* <0: Exponential
\\* >0: Logarithmic

- `decay_time` (float): [Read-Write]

- `depth` (float): [Read-Write]

- `is_enabled` (bool): [Read-Write]

- `release_curve` (float): [Read-Write] \* Control the shape of the attack curve:
\\* 0: Linear
\\* <0: Exponential
\\* >0: Logarithmic

- `release_time` (float): [Read-Write]

- `sustain_level` (float): [Read-Write]

- `target` (AdsrTarget): [Read-Write]


### Table of Contents

- `unreal.AdsrSettings`
  - `AdsrSettings`