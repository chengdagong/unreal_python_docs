# unreal.AnimNextParamType

```python
class unreal.AnimNextParamType
```


**Bases:** ``StructBase``


Representation of a parameter’s type. Serializable, but fairly heavyweight to pass around and compare.
Faster comparisons and other operations can be performed on UE::UAF::FParamTypeHandle, but they cannot be
serialized as they are not stable across runs.

**C++ Source:**

- **Plugin**: UAF

- **Module**: UAF

- **File**: ParamType.h


### Table of Contents

- `unreal.AnimNextParamType`
  - `AnimNextParamType`