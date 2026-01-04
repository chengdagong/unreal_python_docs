# unreal.AnimNode_CCDIK

```python
class unreal.AnimNode_CCDIK(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Controller which implements the CCDIK IK approximation algorithm

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_CCDIK.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `effector_location` (Vector): [Read-Write] Coordinates for target location of tip bone - if EffectorLocationSpace is bone, this is the offset from Target Bone to use as target location

- `effector_location_space` (BoneControlSpace): [Read-Write] Reference frame of Effector Transform.

- `effector_target` (BoneSocketTarget): [Read-Write] If EffectorTransformSpace is a bone, this is the bone to use. \*

- `enable_rotation_limit` (bool): [Read-Write] Tolerance for final tip location delta from EffectorLocation

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `max_iterations` (int32): [Read-Write] Maximum number of iterations allowed, to control performance.

- `precision` (float): [Read-Write] Tolerance for final tip location delta from EffectorLocation

- `root_bone` (BoneReference): [Read-Write] Name of the root bone

- `rotation_limit_per_joints` (Array[float]): [Read-Write] symmetry rotation limit per joint. Index 0 matches with root bone and last index matches with tip bone.

- `start_from_tail` (bool): [Read-Write] Toggle drawing of axes to debug joint rotation

- `tip_bone` (BoneReference): [Read-Write] Name of tip bone


### Table of Contents

- `unreal.AnimNode_CCDIK`
  - `AnimNode_CCDIK`