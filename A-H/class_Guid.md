# unreal.Guid

```python
class unreal.Guid
```


**Bases:** ``StructBase``


A globally unique identifier (mirrored from Engine/Source/Runtime/Core/Public/Misc/Guid.h)

**C++ Source:**

- **Module**: CoreUObject

- **File**: NoExportTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `a` (int32): [Read-Write]

- `b` (int32): [Read-Write]

- `c` (int32): [Read-Write]

- `d` (int32): [Read-Write]



---

**to_string**() → `str`

Converts a GUID value to a string, in the form ‘A-B-C-D’

Return type:

str

### Table of Contents

- `unreal.Guid`
  - `Guid`
    - `Guid.to_string()`