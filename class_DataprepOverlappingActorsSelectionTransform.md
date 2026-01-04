# unreal.DataprepOverlappingActorsSelectionTransform

```python
class unreal.DataprepOverlappingActorsSelectionTransform(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``DataprepSelectionTransform``


Return all actors overlapping the selected actors

**C++ Source:**

- **Plugin**: DataprepGeometryOperations

- **Module**: DataprepGeometryOperations

- **File**: DataprepGeometrySelectionTransforms.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `jacketing_accuracy` (float): [Read-Write] Accuracy of the distance field approximation

- `output_can_include_input` (bool): [Read-Write] Specifies if input objects that have matching type can be added to the result

- `select_overlapping` (bool): [Read-Write] If checked, select fully inside + overlapping actors. Else, select only actors that are fully inside.


### Table of Contents

- `unreal.DataprepOverlappingActorsSelectionTransform`
  - `DataprepOverlappingActorsSelectionTransform`