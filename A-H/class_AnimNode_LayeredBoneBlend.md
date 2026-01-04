# unreal.AnimNode_LayeredBoneBlend

```python
class unreal.AnimNode_LayeredBoneBlend(base_pose:PoseLink=\[\], blend_poses:None=\[\], blend_weights:None=\[\], lod_threshold:int=0, mesh_space_rotation_blend:bool=False, root_space_rotation_blend:bool=False, mesh_space_scale_blend:bool=False, curve_blend_option:CurveBlendOption=Ellipsis)
```


**Bases:** ``AnimNode_Base``


Layered blend (per bone); has dynamic number of blendposes that can blend per different bone sets

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_LayeredBoneBlend.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `base_pose` (PoseLink): [Read-Write] The source pose

- `blend_masks` (Array[BlendProfile]): [Read-Write] The blend masks to use for our layer inputs. Allows the use of per-bone alphas.
Blend masks are used when BlendMode is BlendMask.

- `blend_mode` (LayeredBoneBlendMode): [Read-Write] Whether to use branch filters or a blend mask to specify an input pose per-bone influence

- `blend_poses` (Array[PoseLink]): [Read-Write] Each layer’s blended pose

- `blend_root_motion_based_on_root_bone` (bool): [Read-Write] Whether to incorporate the per-bone blend weight of the root bone when lending root motion

- `blend_weights` (Array[float]): [Read-Write] The weights of each layer

- `curve_blend_option` (CurveBlendOption): [Read-Write] How to blend the layers together

- `layer_setup` (Array[InputBlendPose]): [Read-Write] Configuration for the parts of the skeleton to blend for each layer. Allows
certain parts of the tree to be blended out or omitted from the pose.
LayerSetup is used when BlendMode is BranchFilter.

- `lod_threshold` (int32): [Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

- `mesh_space_rotation_blend` (bool): [Read-Write] Whether to blend bone rotations in mesh space or in local space

- `mesh_space_scale_blend` (bool): [Read-Write] Whether to blend bone scales in mesh space or in local space

- `root_space_rotation_blend` (bool): [Read-Write] Whether to blend bone rotations in root space or in mesh space



---

_property_ `base_pose`: PoseLink

[Read-Write] The source pose

**Type:**

( PoseLink)


---

_property_ `blend_poses`: None

[Read-Write] Each layer’s blended pose

**Type:**

( Array\ [PoseLink])


---

_property_ `blend_weights`: None

[Read-Write] The weights of each layer

**Type:**

( Array\ [float])


---

_property_ `curve_blend_option`: CurveBlendOption

[Read-Write] How to blend the layers together

**Type:**

( CurveBlendOption)


---

_property_ `lod_threshold`: int

[Read-Write] \* Max LOD that this node is allowed to run
\\* For example if you have LODThreshold to be 2, it will run until LOD 2 (based on 0 index)
\\* when the component LOD becomes 3, it will stop update/evaluate
\\* currently transition would be issue and that has to be re-visited

**Type:**

(int32)


---

_property_ `mesh_space_rotation_blend`: bool

[Read-Write] Whether to blend bone rotations in mesh space or in local space

**Type:**

( bool)


---

_property_ `mesh_space_scale_blend`: bool

[Read-Write] Whether to blend bone scales in mesh space or in local space

**Type:**

( bool)


---

_property_ `root_space_rotation_blend`: bool

[Read-Write] Whether to blend bone rotations in root space or in mesh space

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_LayeredBoneBlend`
  - `AnimNode_LayeredBoneBlend`
    - `AnimNode_LayeredBoneBlend.base_pose`
    - `AnimNode_LayeredBoneBlend.blend_poses`
    - `AnimNode_LayeredBoneBlend.blend_weights`
    - `AnimNode_LayeredBoneBlend.curve_blend_option`
    - `AnimNode_LayeredBoneBlend.lod_threshold`
    - `AnimNode_LayeredBoneBlend.mesh_space_rotation_blend`
    - `AnimNode_LayeredBoneBlend.mesh_space_scale_blend`
    - `AnimNode_LayeredBoneBlend.root_space_rotation_blend`