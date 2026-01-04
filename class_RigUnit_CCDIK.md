# unreal.RigUnit_CCDIK

```python
class unreal.RigUnit_CCDIK(execute_pin:RigVMExecutePin=\[\], start_bone:Name='None', effector_bone:Name='None', effector_transform:Transform=Ellipsis, precision:float=0.0, weight:float=0.0, max_iterations:int=0, start_from_tail:bool=False, base_rotation_limit:float=0.0, rotation_limits:None=\[\], propagate_to_children:bool=False)
```


**Bases:** ``RigUnit_HighlevelBaseMutable``


The CCID solver can solve N-Bone chains using
the Cyclic Coordinate Descent Inverse Kinematics algorithm.
For now this node supports single effector chains only.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_CCDIK.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `base_rotation_limit` (float): [Read-Only] The general rotation limit to be applied to bones

- `effector_bone` (Name): [Read-Write] The last bone in the chain to solve - the effector

- `effector_transform` (Transform): [Read-Write] The transform of the effector in global space

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `max_iterations` (int32): [Read-Write] The maximum number of iterations. Values between 4 and 16 are common.

- `precision` (float): [Read-Only] The precision to use for the fabrik solver

- `propagate_to_children` (bool): [Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

- `rotation_limits` (Array[RigUnit\_CCDIK\_RotationLimit]): [Read-Only] Defines the limits of rotation per bone.

- `start_bone` (Name): [Read-Write] The first bone in the chain to solve

- `start_from_tail` (bool): [Read-Only] If set to true the direction of the solvers is flipped.

- `weight` (float): [Read-Write] The weight of the solver - how much the IK should be applied.



---

_property_ `base_rotation_limit`: float

[Read-Only] The general rotation limit to be applied to bones

**Type:**

( float)


---

_property_ `effector_bone`: Name

[Read-Write] The last bone in the chain to solve - the effector

**Type:**

( Name)


---

_property_ `effector_transform`: Transform

[Read-Write] The transform of the effector in global space

**Type:**

( Transform)


---

_property_ `max_iterations`: int

[Read-Write] The maximum number of iterations. Values between 4 and 16 are common.

**Type:**

(int32)


---

_property_ `precision`: float

[Read-Only] The precision to use for the fabrik solver

**Type:**

( float)


---

_property_ `propagate_to_children`: bool

[Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

**Type:**

( bool)


---

_property_ `rotation_limits`: None

[Read-Only] Defines the limits of rotation per bone.

**Type:**

( Array\ [RigUnit\_CCDIK\_RotationLimit])


---

_property_ `start_bone`: Name

[Read-Write] The first bone in the chain to solve

**Type:**

( Name)


---

_property_ `start_from_tail`: bool

[Read-Only] If set to true the direction of the solvers is flipped.

**Type:**

( bool)


---

_property_ `weight`: float

[Read-Write] The weight of the solver - how much the IK should be applied.

**Type:**

( float)

### Table of Contents

- `unreal.RigUnit_CCDIK`
  - `RigUnit_CCDIK`
    - `RigUnit_CCDIK.base_rotation_limit`
    - `RigUnit_CCDIK.effector_bone`
    - `RigUnit_CCDIK.effector_transform`
    - `RigUnit_CCDIK.max_iterations`
    - `RigUnit_CCDIK.precision`
    - `RigUnit_CCDIK.propagate_to_children`
    - `RigUnit_CCDIK.rotation_limits`
    - `RigUnit_CCDIK.start_bone`
    - `RigUnit_CCDIK.start_from_tail`
    - `RigUnit_CCDIK.weight`