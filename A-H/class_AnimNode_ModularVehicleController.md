# unreal.AnimNode_ModularVehicleController

```python
class unreal.AnimNode_ModularVehicleController(component_pose:ComponentSpacePoseLink=\[\], lod_threshold:int=0, alpha_input_type:AnimAlphaInputType=Ellipsis, alpha_bool_enabled:bool=False, alpha:float=0.0, alpha_scale_bias:InputScaleBias=Ellipsis, alpha_bool_blend:InputAlphaBoolBlend=Ellipsis, alpha_curve_name:Name='None', alpha_scale_bias_clamp:InputScaleBiasClamp=Ellipsis)
```


**Bases:** ``AnimNode_SkeletalControlBase``


Simple controller that replaces or adds to the translation/rotation of a single bone.

**C++ Source:**

- **Plugin**: ChaosModularVehicle

- **Module**: ChaosModularVehicleEngine

- **File**: AnimNode\_ModularVehicleController.h


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


### Table of Contents

- `unreal.AnimNode_ModularVehicleController`
  - `AnimNode_ModularVehicleController`