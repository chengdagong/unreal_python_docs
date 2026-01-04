# unreal.RigUnit_SetSplineTransforms

```python
class unreal.RigUnit_SetSplineTransforms(execute_pin:RigVMExecutePin=\[\], transforms:None=\[\], spline:ControlRigSpline=\[\])
```


**Bases:** ``RigUnitMutable``


- Set the points of a spline, given a spline and an array of positions


**C++ Source:**

- **Plugin**: ControlRigSpline

- **Module**: ControlRigSpline

- **File**: ControlRigSplineUnits.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `spline` (ControlRigSpline): [Read-Write]

- `transforms` (Array[Transform]): [Read-Write]



---

_property_ `spline`: ControlRigSpline

[Read-Write]

**Type:**

( ControlRigSpline)


---

_property_ `transforms`: None

[Read-Write]

**Type:**

( Array\ [Transform])

### Table of Contents

- `unreal.RigUnit_SetSplineTransforms`
  - `RigUnit_SetSplineTransforms`
    - `RigUnit_SetSplineTransforms.spline`
    - `RigUnit_SetSplineTransforms.transforms`