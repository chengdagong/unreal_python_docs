# unreal.AnimNode_OffsetRootBone

```python
class unreal.AnimNode_OffsetRootBone(source:PoseLink=\[\])
```


**Bases:** ``AnimNode_Base``


Anim Node Offset Root Bone

**C++ Source:**

- **Plugin**: AnimationWarping

- **Module**: AnimationWarpingRuntime

- **File**: AnimNode\_OffsetRootBone.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `clamp_to_rotation_velocity` (bool): [Read-Write] Whether to limit the offset’s rotation interpolation speed to the velocity on the incoming motion
Enabling this prevents the offset sliding when there’s little to no rotation speed

- `clamp_to_translation_velocity` (bool): [Read-Write] Whether to limit the offset’s translation interpolation speed to the velocity on the incoming motion
Enabling this prevents the offset sliding when there’s little to no translation speed

- `collision_test_shape_offset` (Vector): [Read-Write]

- `collision_test_shape_radius` (float): [Read-Write]

- `collision_testing_mode` (OffsetRootBone\_CollisionTestingMode): [Read-Write]

- `evaluation_mode` (WarpingEvaluationMode): [Read-Write]

- `ground_normal` (Vector): [Read-Write] Surface normal of the ground

- `max_rotation_error` (float): [Read-Write] How much the offset can deviate from the mesh component’s rotation in degrees
Values lower than 0 disable this limit

- `max_translation_error` (float): [Read-Write] How much the offset can deviate from the mesh component’s translation in units
Values lower than 0 disable this limit

- `on_ground` (bool): [Read-Write] When OnGround is true, root motion velicities will be projected onto the ground surface

- `reset_every_frame` (bool): [Read-Write]

- `rotation_delta` (Rotator): [Read-Write] Delta applied to the rotation offset this frame.
For procedural values, consider adjusting the input by delta time.

- `rotation_half_life` (float): [Read-Write] Controls how fast the rotation offset is blended out
Values closer to 0 make it faster

- `rotation_mode` (OffsetRootBoneMode): [Read-Write] The rotation offset behavior mode

- `rotation_speed_ratio` (float): [Read-Write] How much the offset can blend out, relative to the incoming rotation speed
i.e. If root motion is rotating at 90 degrees/s, at 0.5, the offset can blend out at 45 degree/s

- `source` (PoseLink): [Read-Write]

- `translation_delta` (Vector): [Read-Write] Delta applied to the translation offset this frame.
For procedural values, consider adjusting the input by delta time.

- `translation_halflife` (float): [Read-Write] Controls how fast the translation offset is blended out
Values closer to 0 make it faster

- `translation_mode` (OffsetRootBoneMode): [Read-Write] The translation offset behavior mode

- `translation_speed_ratio` (float): [Read-Write] How much the offset can blend out, relative to the incoming translation speed
i.e. If root motion is moving at 400cm/s, at 0.5, the offset can blend out at 200cm/s



---

_property_ `source`: PoseLink

[Read-Write]

**Type:**

( PoseLink)

### Table of Contents

- `unreal.AnimNode_OffsetRootBone`
  - `AnimNode_OffsetRootBone`
    - `AnimNode_OffsetRootBone.source`