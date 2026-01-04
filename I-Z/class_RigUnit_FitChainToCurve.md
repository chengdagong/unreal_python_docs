# unreal.RigUnit_FitChainToCurve

```python
class unreal.RigUnit_FitChainToCurve(execute_pin:RigVMExecutePin=\[\], start_bone:Name='None', end_bone:Name='None', bezier:RigVMFourPointBezier=\[\], alignment:ControlRigCurveAlignment=Ellipsis, minimum:float=0.0, maximum:float=0.0, sampling_precision:int=0, primary_axis:Vector=Ellipsis, secondary_axis:Vector=Ellipsis, pole_vector_position:Vector=Ellipsis, rotations:None=\[\], rotation_ease_type:RigVMAnimEasingType=Ellipsis, weight:float=0.0, propagate_to_children:bool=False, debug_settings:RigUnit_FitChainToCurve_DebugSettings=Ellipsis)
```


**Bases:** ``RigUnit_HighlevelBaseMutable``


Fits a given chain to a four point bezier curve.
Additionally provides rotational control matching the features of the Distribute Rotation node.

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRig

- **File**: RigUnit\_FitChainToCurve.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alignment` (ControlRigCurveAlignment): [Read-Only] Specifies how to align the chain on the curve

- `bezier` (RigVMFourPointBezier): [Read-Write] The curve to align to

- `debug_settings` (RigUnit\_FitChainToCurve\_DebugSettings): [Read-Write]

- `end_bone` (Name): [Read-Write] The name of the last bone to align

- `execute_pin` (RigVMExecutePin): [Read-Write] \* This property is used to chain multiple mutable units together

- `maximum` (float): [Read-Only] The maximum U value to use on the curve

- `minimum` (float): [Read-Only] The minimum U value to use on the curve

- `pole_vector_position` (Vector): [Read-Write] The the position of the pole vector used for aligning the secondary axis.
Only has an effect if the secondary axis is set.

- `primary_axis` (Vector): [Read-Write] The major axis being aligned - along the bone

- `propagate_to_children` (bool): [Read-Only] If set to true all of the global transforms of the children
of this bone will be recalculated based on their local transforms.
Note: This is computationally more expensive than turning it off.

- `rotation_ease_type` (RigVMAnimEasingType): [Read-Only] The easing to use between to rotations.

- `rotations` (Array[RigUnit\_FitChainToCurve\_Rotation]): [Read-Write] The list of rotations to be applied along the curve

- `sampling_precision` (int32): [Read-Only] The number of samples to use on the curve. Clamped at 64.

- `secondary_axis` (Vector): [Read-Write] The minor axis being aligned - towards the pole vector.
You can use (0.0, 0.0, 0.0) to disable it.

- `start_bone` (Name): [Read-Write] The name of the first bone to align

- `weight` (float): [Read-Write] The weight of the solver - how much the rotation should be applied



---

_property_ `alignment`: ControlRigCurveAlignment

[Read-Only] Specifies how to align the chain on the curve

**Type:**

( ControlRigCurveAlignment)


---

_property_ `bezier`: RigVMFourPointBezier

[Read-Write] The curve to align to

**Type:**

( RigVMFourPointBezier)


---

_property_ `debug_settings`: RigUnit\

[Read-Write]

**Type:**

( RigUnit\_FitChainToCurve\_DebugSettings)


---

_property_ `end_bone`: Name

[Read-Write] The name of the last bone to align

**Type:**

( Name)


---

_property_ `maximum`: float

[Read-Only] The maximum U value to use on the curve

**Type:**

( float)


---

_property_ `minimum`: float

[Read-Only] The minimum U value to use on the curve

**Type:**

( float)


---

_property_ `pole_vector_position`: Vector

[Read-Write] The the position of the pole vector used for aligning the secondary axis.
Only has an effect if the secondary axis is set.

**Type:**

( Vector)


---

_property_ `primary_axis`: Vector

[Read-Write] The major axis being aligned - along the bone

**Type:**

( Vector)


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

[Read-Write] The list of rotations to be applied along the curve

**Type:**

( Array\ [RigUnit\_FitChainToCurve\_Rotation])


---

_property_ `sampling_precision`: int

[Read-Only] The number of samples to use on the curve. Clamped at 64.

**Type:**

(int32)


---

_property_ `secondary_axis`: Vector

[Read-Write] The minor axis being aligned - towards the pole vector.
You can use (0.0, 0.0, 0.0) to disable it.

**Type:**

( Vector)


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

- `unreal.RigUnit_FitChainToCurve`
  - `RigUnit_FitChainToCurve`
    - `RigUnit_FitChainToCurve.alignment`
    - `RigUnit_FitChainToCurve.bezier`
    - `RigUnit_FitChainToCurve.debug_settings`
    - `RigUnit_FitChainToCurve.end_bone`
    - `RigUnit_FitChainToCurve.maximum`
    - `RigUnit_FitChainToCurve.minimum`
    - `RigUnit_FitChainToCurve.pole_vector_position`
    - `RigUnit_FitChainToCurve.primary_axis`
    - `RigUnit_FitChainToCurve.propagate_to_children`
    - `RigUnit_FitChainToCurve.rotation_ease_type`
    - `RigUnit_FitChainToCurve.rotations`
    - `RigUnit_FitChainToCurve.sampling_precision`
    - `RigUnit_FitChainToCurve.secondary_axis`
    - `RigUnit_FitChainToCurve.start_bone`
    - `RigUnit_FitChainToCurve.weight`