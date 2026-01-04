# unreal.RigVMFunction_MathFloatRemap

```python
class unreal.RigVMFunction_MathFloatRemap(value:float=0.0, source_minimum:float=0.0, source_maximum:float=0.0, target_minimum:float=0.0, target_maximum:float=0.0, clamp:bool=False, result:float=0.0)
```


**Bases:** ``RigVMFunction_MathFloatBase``


Remaps the given value from a source range to a target range.

**C++ Source:**

- **Plugin**: RigVM

- **Module**: RigVM

- **File**: RigVMFunction\_MathFloat.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `clamp` (bool): [Read-Write] If set to true the result is clamped to the target range

- `result` (float): [Read-Write]

- `source_maximum` (float): [Read-Write]

- `source_minimum` (float): [Read-Write]

- `target_maximum` (float): [Read-Write]

- `target_minimum` (float): [Read-Write]

- `value` (float): [Read-Write]



---

_property_ `clamp`: bool

[Read-Write] If set to true the result is clamped to the target range

**Type:**

( bool)


---

_property_ `result`: float

[Read-Only]

**Type:**

( float)


---

_property_ `source_maximum`: float

[Read-Write]

**Type:**

( float)


---

_property_ `source_minimum`: float

[Read-Write]

**Type:**

( float)


---

_property_ `target_maximum`: float

[Read-Write]

**Type:**

( float)


---

_property_ `target_minimum`: float

[Read-Write]

**Type:**

( float)


---

_property_ `value`: float

[Read-Write]

**Type:**

( float)

### Table of Contents

- `unreal.RigVMFunction_MathFloatRemap`
  - `RigVMFunction_MathFloatRemap`
    - `RigVMFunction_MathFloatRemap.clamp`
    - `RigVMFunction_MathFloatRemap.result`
    - `RigVMFunction_MathFloatRemap.source_maximum`
    - `RigVMFunction_MathFloatRemap.source_minimum`
    - `RigVMFunction_MathFloatRemap.target_maximum`
    - `RigVMFunction_MathFloatRemap.target_minimum`
    - `RigVMFunction_MathFloatRemap.value`