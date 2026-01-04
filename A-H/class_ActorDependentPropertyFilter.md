# unreal.ActorDependentPropertyFilter

```python
class unreal.ActorDependentPropertyFilter(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``LevelSnapshotFilter``


Implements IsActorValid and IsPropertyValid as follows:

- IsActorValid returns ActorFilter->IsActorValid

- IsPropertyValid runs ActorFilter->IsActorValid. Depending on its results it runs

- IncludePropertyFilter

- ExcludePropertyFilter

- DoNotCarePropertyFilter


Use case: You want to allow certain properties when another filters would include the actor and allow different properties when excluded.

**C++ Source:**

- **Plugin**: LevelSnapshots

- **Module**: LevelSnapshotFilters

- **File**: ActorDependentPropertyFilter.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `actor_filter` (LevelSnapshotFilter): [Read-Write] We run IsActorValid on this filter. IsPropertyValid uses one of the below filters depending on this filter.

- `do_not_care_handling` (DoNotCareHandling): [Read-Write] Determines what filter IsPropertyValid is supposed to use when IsActorValid returns DoNotCare.

- `do_not_care_property_filter` (LevelSnapshotFilter): [Read-Write] Used by IsPropertyValid when ActorFilter->IsActorValid returns DoNotCare and DoNotCareHandling == UseDoNotCareFilter.

- `exclude_property_filter` (LevelSnapshotFilter): [Read-Write] Used by IsPropertyValid when ActorFilter->IsActorValid returns Exclude

- `include_property_filter` (LevelSnapshotFilter): [Read-Write] Used by IsPropertyValid when ActorFilter->IsActorValid returns Include


### Table of Contents

- `unreal.ActorDependentPropertyFilter`
  - `ActorDependentPropertyFilter`