# unreal.RigUnit_DistributeRotation

```python
class unreal.RigUnit_DistributeRotation(execute_pin:RigVMExecutePin=\[\], start_bone:Name='None', end_bone:Name='None', rotations:None=\[\], rotation_ease_type:RigVMAnimEasingType=Ellipsis, weight:float=0.0, propagate_to_children:bool=False)
```


**Bases:** ``RigUnit_HighlevelBaseMutable``


Distributes rotations provided along a chain.
Each rotation is expressed by a quaternion and a ratio, where the ratio is between 0.0 and 1.0
Note: This node adds rotation in local space of each bone!

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_DistributeRotation.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `end_bone` (Name): [Read-Write] The name of the last bone to align

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `propagate_to_children` (bool): [Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

- `rotation_ease_type` (RigVMAnimEasingType): [Read-Only] The easing to use between to rotations.

- `rotations` (Array[RigUnit\_DistributeRotation\_Rotation]): [Read-Write] The list of rotations to be applied

- `start_bone` (Name): [Read-Write] The name of the first bone to align

- `weight` (float): [Read-Write] The weight of the solver - how much the rotation should be applied



---

_property_ `end_bone`: Name

[Read-Write] The name of the last bone to align

**Type:**

( Name)


---

_property_ `propagate_to_children`: bool

[Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

**Type:**

( bool)


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

_property_ `start_bone`: Name

[Read-Write] The name of the first bone to align

**Type:**

( Name)


---

_property_ `weight`: float

[Read-Write] The weight of the solver - how much the rotation should be applied

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_DistributeRotation`
  - `RigUnit_DistributeRotation`
    - `RigUnit_DistributeRotation.end_bone`
    - `RigUnit_DistributeRotation.propagate_to_children`
    - `RigUnit_DistributeRotation.rotation_ease_type`
    - `RigUnit_DistributeRotation.rotations`
    - `RigUnit_DistributeRotation.start_bone`
    - `RigUnit_DistributeRotation.weight`