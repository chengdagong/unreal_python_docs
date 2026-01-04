# unreal.AlignmentSteeringSettings

```python
class unreal.AlignmentSteeringSettings
```


**Bases:** ``StructBase``


Alignment Steering Settings

**C++ Source:**

- **Plugin**: EvaluationNotifies

- **Module**: EvaluationNotifiesRuntime

- **File**: AnimNotifyState\_Alignment.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `angle_threshold` (float): [Read-Write] When the warped movement direction differs from the animated movement direction by more than this threshold, steering will be disabled.

- `enable_smoothing` (bool): [Read-Write] Enable smoothing of the steering target orientation, to avoid instant orientation changes

- `smooth_damping` (float): [Read-Write] Spring damping factor for smoothing

- `smooth_stiffness` (float): [Read-Write] Sprint stiffness for smoothing


### Table of Contents

- `unreal.AlignmentSteeringSettings`
  - `AlignmentSteeringSettings`