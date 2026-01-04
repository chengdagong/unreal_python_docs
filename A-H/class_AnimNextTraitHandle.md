# unreal.AnimNextTraitHandle

```python
class unreal.AnimNextTraitHandle
```


**Bases:** ``StructBase``


Trait Handle
A trait handle represents a reference to a specific trait instance in the shared/read-only portion
of a sub-graph. It points to a FNodeDescription when resolved.

Internally, it contains a node handle and a trait index.
Trait handles can only be used within an AnimNext graph serialized with FTraitWriter.
see: FNodeDescription, FNodeHandle

**C++ Source:**

- **Plugin**: UAFAnimGraph

- **Module**: UAFAnimGraph

- **File**: TraitHandle.h


### Table of Contents

- `unreal.AnimNextTraitHandle`
  - `AnimNextTraitHandle`