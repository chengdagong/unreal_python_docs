# unreal.RigUnit_DistributeRotationForCollection

```python
class unreal.RigUnit_DistributeRotationForCollection(execute_pin:RigVMExecutePin=\[\], items:RigElementKeyCollection=Ellipsis, rotations:None=\[\], rotation_ease_type:RigVMAnimEasingType=Ellipsis, weight:float=0.0)
```


**Bases:** ``RigUnit_HighlevelBaseMutable``


Distributes rotations provided across a collection of items.
Each rotation is expressed by a quaternion and a ratio, where the ratio is between 0.0 and 1.0
Note: This node adds rotation in local space of each item!

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_DistributeRotation.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `items` (RigElementKeyCollection): [Read-Write] The items to use to distribute the rotation

- `rotation_ease_type` (RigVMAnimEasingType): [Read-Only] The easing to use between to rotations.

- `rotations` (Array[RigUnit\_DistributeRotation\_Rotation]): [Read-Write] The list of rotations to be applied

- `weight` (float): [Read-Write] The weight of the solver - how much the rotation should be applied



---

_property_ `items`: RigElementKeyCollection

[Read-Write] The items to use to distribute the rotation

**Type:**

( RigElementKeyCollection)


---

_property_ `rotation_ease_type`: RigVMAnimEasingType

[Read-Only] The easing to use between to rotations.

**Type:**

( RigVMAnimEasingType)


---

_property_ `rotations`: None

[Read-Write] The list of rotations to be applied

**Type:**

( Array\ [RigUnit\_DistributeRotation\_Rotation])


---

_property_ `weight`: float

[Read-Write] The weight of the solver - how much the rotation should be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_DistributeRotationForCollection`
  - `RigUnit_DistributeRotationForCollection`
    - `RigUnit_DistributeRotationForCollection.items`
    - `RigUnit_DistributeRotationForCollection.rotation_ease_type`
    - `RigUnit_DistributeRotationForCollection.rotations`
    - `RigUnit_DistributeRotationForCollection.weight`