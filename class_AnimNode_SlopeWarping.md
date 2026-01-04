# unreal.AnimNode_SlopeWarping

```python
class unreal.AnimNode_SlopeWarping(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Anim Node Slope Warping

**C++ Source:**

- **Plugin**: AnimationWarping

- **Module**: AnimationWarpingRuntime

- **File**: AnimNode\_SlopeWarping.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `custom_floor_offset` (Vector): [Read-Write]

- `feet_definitions` (Array[SlopeWarpingFootDefinition]): [Read-Write]

- `floor_normal_interpolator` (VectorRK4SpringInterpolator): [Read-Write]

- `floor_offset_interpolator` (VectorRK4SpringInterpolator): [Read-Write]

- `gravity_dir` (Vector): [Read-Write]

- `ik_foot_root_bone` (BoneReference): [Read-Write] IKFoot Root Bone. \*

- `keep_mesh_inside_of_capsule` (bool): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `max_step_height` (float): [Read-Write]

- `pelvis_bone` (BoneReference): [Read-Write] Pelvis Bone. \*

- `pelvis_offset_interpolator` (VectorRK4SpringInterpolator): [Read-Write]

- `pull_pelvis_down` (bool): [Read-Write]

- `use_custom_floor_offset` (bool): [Read-Write]


### Table of Contents

- `unreal.AnimNode_SlopeWarping`
  - `AnimNode_SlopeWarping`