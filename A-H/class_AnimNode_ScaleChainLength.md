# unreal.AnimNode_ScaleChainLength

```python
class unreal.AnimNode_ScaleChainLength(default_chain_length:float=0.0, target_location:Vector=Ellipsis, alpha:float=0.0)
```


**Bases:** ``AnimNode_Base``


Scale the length of a chain of bones.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_ScaleChainLength.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `chain_end_bone` (BoneReference): [Read-Write]

- `chain_initial_length` (ScaleChainInitialLength): [Read-Write]

- `chain_start_bone` (BoneReference): [Read-Write]

- `default_chain_length` (float): [Read-Write] Default chain length, as animated.

- `input_pose` (PoseLink): [Read-Write]

- `target_location` (Vector): [Read-Write]



---

_property_ `alpha`: float

[Read-Write]

**Type:**

( float)


---

_property_ `default_chain_length`: float

[Read-Write] Default chain length, as animated.

**Type:**

( float)


---

_property_ `target_location`: Vector

[Read-Write]

**Type:**

( Vector)

### Table of Contents

- `unreal.AnimNode_ScaleChainLength`
  - `AnimNode_ScaleChainLength`
    - `AnimNode_ScaleChainLength.alpha`
    - `AnimNode_ScaleChainLength.default_chain_length`
    - `AnimNode_ScaleChainLength.target_location`