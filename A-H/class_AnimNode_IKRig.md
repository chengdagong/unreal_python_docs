# unreal.AnimNode_IKRig

```python
class unreal.AnimNode_IKRig(goals:None=\[\], alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis)
```


**Bases:** ``AnimNode_CustomProperty``


Anim Node IKRig

**C++ Source:**

- **Plugin**: IKRig

- **Module**: IKRig

- **File**: AnimNode\_IKRig.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write] alpha value handler \*

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `debug_scale` (float): [Read-Write] Adjust size of debug drawing.

- `enable_debug_draw` (bool): [Read-Write] Toggle debug drawing of goals when node is selected.

- `goals` (Array[IKRigGoal]): [Read-Write] The input goal transforms used by the IK Rig solvers.

- `rig_definition_asset` (IKRigDefinition): [Read-Write] The IK rig to use to modify the incoming source pose.

- `source` (PoseLink): [Read-Write] The input pose to start the IK solve relative to.

- `start_from_ref_pose` (bool): [Read-Write] optionally ignore the input pose and start from the reference pose each solve



---

_property_ `alpha`: float

[Read-Write] Current strength of the skeletal control

**Type:**

( float)


---

_property_ `alpha_bool_blend`: InputAlphaBoolBlend

[Read-Write]

**Type:**

( InputAlphaBoolBlend)


---

_property_ `alpha_bool_enabled`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `alpha_curve_name`: Name

[Read-Write]

**Type:**

( Name)


---

_property_ `alpha_input_type`: AnimAlphaInputType

[Read-Write] alpha value handler \*

**Type:**

( AnimAlphaInputType)


---

_property_ `alpha_scale_bias`: InputScaleBias

[Read-Write]

**Type:**

( InputScaleBias)


---

_property_ `alpha_scale_bias_clamp`: InputScaleBiasClamp

[Read-Write]

**Type:**

( InputScaleBiasClamp)


---

_property_ `goals`: None

[Read-Write] The input goal transforms used by the IK Rig solvers.

**Type:**

( Array\ [IKRigGoal])

### Table of Contents

- `unreal.AnimNode_IKRig`
  - `AnimNode_IKRig`
    - `AnimNode_IKRig.alpha`
    - `AnimNode_IKRig.alpha_bool_blend`
    - `AnimNode_IKRig.alpha_bool_enabled`
    - `AnimNode_IKRig.alpha_curve_name`
    - `AnimNode_IKRig.alpha_input_type`
    - `AnimNode_IKRig.alpha_scale_bias`
    - `AnimNode_IKRig.alpha_scale_bias_clamp`
    - `AnimNode_IKRig.goals`