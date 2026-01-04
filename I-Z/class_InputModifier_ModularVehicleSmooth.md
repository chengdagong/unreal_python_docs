# unreal.InputModifier_ModularVehicleSmooth

```python
class unreal.InputModifier_ModularVehicleSmooth(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``InputModifier``


UInputModifier\_ModularVehicleSmooth

Add this as a Modifier on any float‐based Action (e.g. “Steer”) to get a
smoother, “lagged” feel. To match the behaviour of the OG chaos vehicle plugin

**C++ Source:**

- **Plugin**: ChaosModularVehicle

- **Module**: ChaosModularVehicleEngine

- **File**: InputModifier\_ModularVehicleSmooth.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `rise_rate` (float): [Read-Write] How quickly to “catch up” to the raw input.
Higher numbers = snappier response; lower = more lag/smoothing.



---

_property_ `rise_rate`: float

[Read-Write] How quickly to “catch up” to the raw input.
Higher numbers = snappier response; lower = more lag/smoothing.

**Type:**

( float)

### Table of Contents

- `unreal.InputModifier_ModularVehicleSmooth`
  - `InputModifier_ModularVehicleSmooth`
    - `InputModifier_ModularVehicleSmooth.rise_rate`