# unreal.DoubleCameraVariable

```python
class unreal.DoubleCameraVariable(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``CameraVariableAsset``


Double camera variable.

**C++ Source:**

- **Plugin**: GameplayCameras

- **Module**: GameplayCameras

- **File**: CameraVariableAssets.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `auto_reset` (bool): [Read-Write] Whether this variable auto-resets to its default value every frame.

- `default_value` (double): [Read-Write] The default value of this variable.

- `is_pre_blended` (bool): [Read-Write] Whether this variable should be pre-blended.

Pre-blending means that if two blending camera rigs share this variable,
each of their values will be blended in a first evaluation pass, and then
both camera rigs will evaluate with the same blended value.


### Table of Contents

- `unreal.DoubleCameraVariable`
  - `DoubleCameraVariable`