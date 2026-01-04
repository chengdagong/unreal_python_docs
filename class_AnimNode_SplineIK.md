# unreal.AnimNode_SplineIK

```python
class unreal.AnimNode_SplineIK(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, control_points:None=\[\], roll:float=0.0, twist_start:float=0.0, twist_end:float=0.0, stretch:float=0.0, offset:float=0.0)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Anim Node Spline IK

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_SplineIK.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `auto_calculate_spline` (bool): [Read-Write] The number of points in the spline if we are specifying it directly

- `bone_axis` (SplineBoneAxis): [Read-Write] Axis of the controlled bone (ie the direction of the spline) to use as the direction for the curve.

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `control_points` (Array[Transform]): [Read-Write] Transforms applied to spline points \*

- `end_bone` (BoneReference): [Read-Write] Name of bone at the end of the spline chain. Bones after this will not be altered by the controller.

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `offset` (float): [Read-Write] The distance along the spline from the start from which bones are constrained

- `point_count` (int32): [Read-Write] The number of points in the spline if we are not auto-calculating

- `roll` (float): [Read-Write] Overall roll of the spline, applied on top of other rotations along the direction of the spline

- `start_bone` (BoneReference): [Read-Write] Name of root bone from which the spline extends \*

- `stretch` (float): [Read-Write] The maximum stretch allowed when fitting bones to the spline. 0.0 means bones do not stretch their length,
1.0 means bones stretch to the length of the spline

- `twist_blend` (AlphaBlend): [Read-Write] How to interpolate twist along the length of the spline

- `twist_end` (float): [Read-Write] The twist of the end bone. Twist is interpolated along the spline according to Twist Blend.

- `twist_start` (float): [Read-Write] The twist of the start bone. Twist is interpolated along the spline according to Twist Blend.



---

_property_ `control_points`: None

[Read-Write] Transforms applied to spline points \*

**Type:**

( Array\ [Transform])


---

_property_ `offset`: float

[Read-Write] The distance along the spline from the start from which bones are constrained

**Type:**

( float)


---

_property_ `roll`: float

[Read-Write] Overall roll of the spline, applied on top of other rotations along the direction of the spline

**Type:**

( float)


---

_property_ `stretch`: float

[Read-Write] The maximum stretch allowed when fitting bones to the spline. 0.0 means bones do not stretch their length,
1.0 means bones stretch to the length of the spline

**Type:**

( float)


---

_property_ `twist_end`: float

[Read-Write] The twist of the end bone. Twist is interpolated along the spline according to Twist Blend.

**Type:**

( float)


---

_property_ `twist_start`: float

[Read-Write] The twist of the start bone. Twist is interpolated along the spline according to Twist Blend.

**Type:**

( float)

### Table of Contents

- `unreal.AnimNode_SplineIK`
  - `AnimNode_SplineIK`
    - `AnimNode_SplineIK.control_points`
    - `AnimNode_SplineIK.offset`
    - `AnimNode_SplineIK.roll`
    - `AnimNode_SplineIK.stretch`
    - `AnimNode_SplineIK.twist_end`
    - `AnimNode_SplineIK.twist_start`