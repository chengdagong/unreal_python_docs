# unreal.AnimNode_BlendProfileLayeredBlend

```python
class unreal.AnimNode_BlendProfileLayeredBlend(base_pose:PoseLink=\[\], blend_pose:PoseLink=\[\], blend_profile_asset:BlendProfileStandalone=Ellipsis, mesh_space_rotation_blend:bool=False, custom_curve_blending:bool=False, curve_blending_option:CurveBlendOption=Ellipsis, blend_weight:float=0.0)
```


**Bases:** ``AnimNode_Base``


Anim Node Blend Profile Layered Blend

**C++ Source:**

- **Plugin**: HierarchyTableAnimation

- **Module**: HierarchyTableAnimationRuntime

- **File**: AnimNode\_BlendProfileLayeredBlend.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `base_pose` (PoseLink): [Read-Write] The source pose

- `blend_pose` (PoseLink): [Read-Write] The target pose

- `blend_profile_asset` (BlendProfileStandalone): [Read-Write] The blend profile mask asset to use to control layering of the pose, curves, and attributes

- `blend_root_motion_based_on_root_bone` (bool): [Read-Write] Whether to incorporate the per-bone blend weight of the root bone when lending root motion

- `blend_weight` (float): [Read-Write] The weight of target pose

- `curve_blending_option` (CurveBlendOption): [Read-Write]

- `custom_curve_blending` (bool): [Read-Write]

- `mesh_space_rotation_blend` (bool): [Read-Write] Whether to blend bone rotations in mesh space or in local space



---

_property_ `base_pose`: PoseLink

[Read-Write] The source pose

**Type:**

( PoseLink)


---

_property_ `blend_pose`: PoseLink

[Read-Write] The target pose

**Type:**

( PoseLink)


---

_property_ `blend_profile_asset`: BlendProfileStandalone

[Read-Write] The blend profile mask asset to use to control layering of the pose, curves, and attributes

**Type:**

( BlendProfileStandalone)


---

_property_ `blend_weight`: float

[Read-Write] The weight of target pose

**Type:**

( float)


---

_property_ `curve_blending_option`: CurveBlendOption

[Read-Write]

**Type:**

( CurveBlendOption)


---

_property_ `custom_curve_blending`: bool

[Read-Write]

**Type:**

( bool)


---

_property_ `mesh_space_rotation_blend`: bool

[Read-Write] Whether to blend bone rotations in mesh space or in local space

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_BlendProfileLayeredBlend`
  - `AnimNode_BlendProfileLayeredBlend`
    - `AnimNode_BlendProfileLayeredBlend.base_pose`
    - `AnimNode_BlendProfileLayeredBlend.blend_pose`
    - `AnimNode_BlendProfileLayeredBlend.blend_profile_asset`
    - `AnimNode_BlendProfileLayeredBlend.blend_weight`
    - `AnimNode_BlendProfileLayeredBlend.curve_blending_option`
    - `AnimNode_BlendProfileLayeredBlend.custom_curve_blending`
    - `AnimNode_BlendProfileLayeredBlend.mesh_space_rotation_blend`