# unreal.AnimNotifyState_PoseSearchSamplingEvent

```python
class unreal.AnimNotifyState_PoseSearchSamplingEvent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``AnimNotifyState_PoseSearchBase``


UPoseSearchFeatureChannel(s) can use this UAnimNotifyState\_PoseSearchSamplingEvent to demarcate events identified by SamplingAttributeId
during database indexing by specifying their SamplingAttributeId property to match UAnimNotifyState\_PoseSearchSamplingAttribute::SamplingAttributeId

**C++ Source:**

- **Plugin**: PoseSearch

- **Module**: PoseSearch

- **File**: PoseSearchAnimNotifies.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `notify_color` (Color): [Read-Write] Color of Notify in editor

- `sampling_attribute_id` (int32): [Read-Write]

- `should_fire_in_editor` (bool): [Read-Write] Whether this notify state instance should fire in animation editors


### Table of Contents

- `unreal.AnimNotifyState_PoseSearchSamplingEvent`
  - `AnimNotifyState_PoseSearchSamplingEvent`