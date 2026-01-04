# unreal.AnimationSetup

```python
class unreal.AnimationSetup
```


**Bases:** ``StructBase``


Animation Setup

**C++ Source:**

- **Plugin**: AnimationSharing

- **Module**: AnimationSharing

- **File**: AnimationSharingTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `anim_blueprint` (type(Class)): [Read-Write] Animation blueprint to use for playing back the Animation Sequence

- `anim_sequence` (AnimSequence): [Read-Write] Animation Sequence to play for this particular setup

- `enabled` (PerPlatformBool): [Read-Write] Whether or not this setup is enabled for specific platforms

- `num_randomized_instances` (PerPlatformInt): [Read-Write] The number of randomized instances created from this setup, it will create instance with different start time offsets (Length / Number of Instance) \* InstanceIndex


### Table of Contents

- `unreal.AnimationSetup`
  - `AnimationSetup`