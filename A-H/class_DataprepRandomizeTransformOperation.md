# unreal.DataprepRandomizeTransformOperation

```python
class unreal.DataprepRandomizeTransformOperation(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``DataprepOperation``


For each actor in the input set, offset its position/rotation/scale with random vector generated from X/Y/Z Min-Max.

**C++ Source:**

- **Plugin**: DataprepEditor

- **Module**: DataprepLibraries

- **File**: DataprepOperations.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `max` (Vector): [Read-Write] Max random value

- `min` (Vector): [Read-Write] Min random value

- `reference_frame` (RandomizeTransformReferenceFrame): [Read-Write] Reference frame to use (relative/world)

- `transform_type` (RandomizeTransformType): [Read-Write] Transform component to randomize


### Table of Contents

- `unreal.DataprepRandomizeTransformOperation`
  - `DataprepRandomizeTransformOperation`