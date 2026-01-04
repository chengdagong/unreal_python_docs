# unreal.AnimNode_StageCoachWheelController

```python
class unreal.AnimNode_StageCoachWheelController(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis, wheel_spoke_count:int=0, max_angular_velocity:float=0.0, shutter_speed:float=0.0, stage_coach_blend:float=0.0)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple controller that replaces or adds to the translation/rotation of a single bone.

**C++ Source:**

- **Plugin**: ChaosVehiclesPlugin

- **Module**: ChaosVehicles

- **File**: AnimNode\_StageCoachWheelController.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `alpha` (float): [Read-Write] Current strength of the skeletal control

- `alpha_bool_blend` (InputAlphaBoolBlend): [Read-Write]

- `alpha_bool_enabled` (bool): [Read-Write]

- `alpha_curve_name` (Name): [Read-Write]

- `alpha_input_type` (AnimAlphaInputType): [Read-Write]

- `alpha_scale_bias` (InputScaleBias): [Read-Write]

- `alpha_scale_bias_clamp` (InputScaleBiasClamp): [Read-Write]

- `component_pose` (ComponentSpacePoseLink): [Read-Write] Input link

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `max_angular_velocity` (float): [Read-Write] Wheel max rotation speed in degrees/second

- `shutter_speed` (float): [Read-Write] Camera shutter speed in frames/second

- `stage_coach_blend` (float): [Read-Write] Blend effect degrees/second

- `wheel_spoke_count` (int32): [Read-Write] Number of spokes visible on wheel



---

_property_ `max_angular_velocity`: float

[Read-Write] Wheel max rotation speed in degrees/second

**Type:**

( float)


---

_property_ `shutter_speed`: float

[Read-Write] Camera shutter speed in frames/second

**Type:**

( float)


---

_property_ `stage_coach_blend`: float

[Read-Write] Blend effect degrees/second

**Type:**

( float)


---

_property_ `wheel_spoke_count`: int

[Read-Write] Number of spokes visible on wheel

**Type:**

(int32)

### Table of Contents

- `unreal.AnimNode_StageCoachWheelController`
  - `AnimNode_StageCoachWheelController`
    - `AnimNode_StageCoachWheelController.max_angular_velocity`
    - `AnimNode_StageCoachWheelController.shutter_speed`
    - `AnimNode_StageCoachWheelController.stage_coach_blend`
    - `AnimNode_StageCoachWheelController.wheel_spoke_count`