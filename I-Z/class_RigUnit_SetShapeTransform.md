# unreal.RigUnit_SetShapeTransform

```python
class unreal.RigUnit_SetShapeTransform(execute_pin:RigVMExecutePin=\[\], control:Name='None', transform:Transform=Ellipsis)
```


**Bases:** ``RigUnitMutable``


SetShapeTransform is used to perform a change in the hierarchy by setting a single control’s shape transform.
This is typically only used during the Construction Event.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_SetControlOffset.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `control` (Name): [Read-Write] The name of the Control to set the transform for.

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `transform` (Transform): [Read-Write] The shape transform to set for the control



---

_property_ `control`: Name

[Read-Write] The name of the Control to set the transform for.

**Type:**

( Name)


---

_property_ `transform`: Transform

[Read-Write] The shape transform to set for the control

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_SetShapeTransform`
  - `RigUnit_SetShapeTransform`
    - `RigUnit_SetShapeTransform.control`
    - `RigUnit_SetShapeTransform.transform`