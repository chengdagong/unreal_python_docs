# unreal.ActorChangedTransformFilter

```python
class unreal.ActorChangedTransformFilter(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ActorSelectorFilter``


Allows an actor depending on whether the actors’ transforms have changed.
Use case: You want detect whether an actor has changed its transform.

**C++ Source:**

- **Plugin**: LevelSnapshots

- **Module**: LevelSnapshotFilters

- **File**: ActorChangedTransformFilter.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `default_result` (FilterResult): [Read-Write] What to return for IsPropertyValid, IsDeletedActorValid, and IsAddedActorValid

- `ignore_location` (bool): [Read-Write] If true, we do not compare the actors’ locations.

- `ignore_rotation` (bool): [Read-Write] If true, we do not compare the actors’ rotations.

- `ignore_scale` (bool): [Read-Write] If true, we do not compare the actors’ scales.

- `transform_check_rule` (TransformReturnType): [Read-Write] Whether we allow actors that changed transform or that stayed at the same place.


### Table of Contents

- `unreal.ActorChangedTransformFilter`
  - `ActorChangedTransformFilter`