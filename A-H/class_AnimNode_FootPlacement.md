# unreal.AnimNode_FootPlacement

```python
class unreal.AnimNode_FootPlacement(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, pelvis_settings:FootPlacementPelvisSettings=\[\], plant_settings:FootPlacementPlantSettings=\[\], interpolation_settings:FootPlacementInterpolationSettings=\[\], trace_settings:FootPlacementTraceSettings=\[\])
```


**Bases:** ``AnimNode_SkeletalControlBase``


Anim Node Foot Placement

**C++ Source:**

- **Plugin**: AnimationWarping

- **Module**: AnimationWarpingRuntime

- **File**: AnimNode\_FootPlacement.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `base_translation_delta` (Vector): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `ik_foot_root_bone` (BoneReference): [Read-Write]

- `interpolation_settings` (FootPlacementInterpolationSettings): [Read-Write]

- `leg_definitions` (Array[FootPlacemenLegDefinition]): [Read-Write]

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `pelvis_bone` (BoneReference): [Read-Write]

- `pelvis_settings` (FootPlacementPelvisSettings): [Read-Write]

- `plant_settings` (FootPlacementPlantSettings): [Read-Write]

- `plant_speed_mode` (WarpingEvaluationMode): [Read-Write] Foot/Ball speed evaluation mode (Graph or Manual) used to decide when the feet are locked
Graph mode uses the root motion attribute from the animations to calculate the joint’s speed
Manual mode uses a per-foot curve name representing the joint’s speed

- `trace_settings` (FootPlacementTraceSettings): [Read-Write]



---

_property_ `interpolation_settings`: FootPlacementInterpolationSettings

[Read-Write]

**Type:**

( FootPlacementInterpolationSettings)


---

_property_ `pelvis_settings`: FootPlacementPelvisSettings

[Read-Write]

**Type:**

( FootPlacementPelvisSettings)


---

_property_ `plant_settings`: FootPlacementPlantSettings

[Read-Write]

**Type:**

( FootPlacementPlantSettings)


---

_property_ `trace_settings`: FootPlacementTraceSettings

[Read-Write]

**Type:**

( FootPlacementTraceSettings)

### Table of Contents

- `unreal.AnimNode_FootPlacement`
  - `AnimNode_FootPlacement`
    - `AnimNode_FootPlacement.interpolation_settings`
    - `AnimNode_FootPlacement.pelvis_settings`
    - `AnimNode_FootPlacement.plant_settings`
    - `AnimNode_FootPlacement.trace_settings`