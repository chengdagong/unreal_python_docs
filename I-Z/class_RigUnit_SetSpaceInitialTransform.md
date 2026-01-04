# unreal.RigUnit_SetSpaceInitialTransform

```python
class unreal.RigUnit_SetSpaceInitialTransform(execute_pin:RigVMExecutePin=\[\], space_name:Name='None', transform:Transform=Ellipsis, result:Transform=Ellipsis, space:RigVMTransformSpace=Ellipsis)
```


**Bases:** ``RigUnitMutable``


SetSpaceInitialTransform is used to perform a change in the hierarchy by setting a single space’s initial transform.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetSpaceInitialTransform.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `result` (Transform): [Read-Write] The transform value result (after weighting)

- `space` (RigVMTransformSpace): [Read-Write] Defines if the bone’s transform should be set
in local or global space.

- `space_name` (Name): [Read-Write] The name of the Space to set the transform for.

- `transform` (Transform): [Read-Write] The transform value to set for the given space.



---

_property_ `result`: Transform

[Read-Only] The transform value result (after weighting)

**Type:**

( Transform)


---

_property_ `space`: RigVMTransformSpace

[Read-Write] Defines if the bone’s transform should be set
in local or global space.

**Type:**

( RigVMTransformSpace)


---

_property_ `space_name`: Name

[Read-Write] The name of the Space to set the transform for.

**Type:**

( Name)


---

_property_ `transform`: Transform

[Read-Write] The transform value to set for the given space.

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_SetSpaceInitialTransform`
  - `RigUnit_SetSpaceInitialTransform`
    - `RigUnit_SetSpaceInitialTransform.result`
    - `RigUnit_SetSpaceInitialTransform.space`
    - `RigUnit_SetSpaceInitialTransform.space_name`
    - `RigUnit_SetSpaceInitialTransform.transform`