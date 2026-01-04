# unreal.RigUnit_ApplyFK

```python
class unreal.RigUnit_ApplyFK(execute_pin:RigVMExecutePin=\[\], joint:Name='None', transform:Transform=Ellipsis, filter:TransformFilter=Ellipsis, apply_transform_mode:ApplyTransformMode=Ellipsis, apply_transform_space:TransformSpaceMode=Ellipsis, base_transform:Transform=Ellipsis, base_joint:Name='None')
```


**Bases:** ``RigUnitMutable``


Rig Unit Apply FK

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_ApplyFK.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `apply_transform_mode` (ApplyTransformMode): [Read-Write]

- `apply_transform_space` (TransformSpaceMode): [Read-Write]

- `base_joint` (Name): [Read-Write] Transform op option. Use if ETransformSpace is BaseJoint

- `base_transform` (Transform): [Read-Write] Transform op option. Use if ETransformSpace is BaseTransform

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `filter` (TransformFilter): [Read-Write] The filter determines what axes can be manipulated by the in-viewport widgets

- `joint` (Name): [Read-Write]

- `transform` (Transform): [Read-Write]



---

_property_ `apply_transform_mode`: ApplyTransformMode

[Read-Write]

**Type:**

( ApplyTransformMode)


---

_property_ `apply_transform_space`: TransformSpaceMode

[Read-Write]

**Type:**

( TransformSpaceMode)


---

_property_ `base_joint`: Name

[Read-Write] Transform op option. Use if ETransformSpace is BaseJoint

**Type:**

( Name)


---

_property_ `base_transform`: Transform

[Read-Write] Transform op option. Use if ETransformSpace is BaseTransform

**Type:**

( Transform)


---

_property_ `filter`: TransformFilter

[Read-Write] The filter determines what axes can be manipulated by the in-viewport widgets

**Type:**

( TransformFilter)


---

_property_ `joint`: Name

[Read-Write]

**Type:**

( Name)


---

_property_ `transform`: Transform

[Read-Write]

**Type:**

( Transform)

### Table of Contents

- `unreal.RigUnit_ApplyFK`
  - `RigUnit_ApplyFK`
    - `RigUnit_ApplyFK.apply_transform_mode`
    - `RigUnit_ApplyFK.apply_transform_space`
    - `RigUnit_ApplyFK.base_joint`
    - `RigUnit_ApplyFK.base_transform`
    - `RigUnit_ApplyFK.filter`
    - `RigUnit_ApplyFK.joint`
    - `RigUnit_ApplyFK.transform`