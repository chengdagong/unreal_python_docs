# unreal.AnimNode_RetargetPoseFromMesh

```python
class unreal.AnimNode_RetargetPoseFromMesh(retarget_from:RetargetSourceMode=Ellipsis, source_mesh_component:SkeletalMeshComponent=Ellipsis, ik_retargeter_asset:IKRetargeter=Ellipsis, custom_retarget_profile:RetargetProfile=Ellipsis, lod_threshold:int=0, lod_threshold_for_ik:int=0, suppress_warnings:bool=False)
```


**Bases:** ``AnimNode_Base``


Anim Node Retarget Pose from Mesh

**C++ Source:**

- **Plugin**: IKRig

- **Module**: IKRig

- **File**: AnimNode\_RetargetPoseFromMesh.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `custom_retarget_profile` (RetargetProfile): [Read-Write] Connect a custom retarget profile to modify the retargeter’s settings at runtime.

- `ik_retargeter_asset` (IKRetargeter): [Read-Write] Retarget asset to use. Must define a Source and Target IK Rig compatible with the SourceMeshComponent and current anim instance.

- `lod_threshold` (int32): [Read-Write] Max LOD that this node is allowed to run.
For example if you have LODThreshold at 2, it will run until LOD 2 (based on 0 index) when the component LOD becomes 3, it will stop update/evaluate
A value of -1 forces the node to execute at all LOD levels.

- `lod_threshold_for_ik` (int32): [Read-Write] Max LOD that IK is allowed to run.
For example if you have LODThresholdForIK at 2, it will skip the IK pass on LODs 3 and greater.
This only disables IK and does not affect the Root or FK passes.
A value of -1 forces the node to execute at all LOD levels.

- `retarget_from` (RetargetSourceMode): [Read-Write] Specify where to get the source pose to retarget from. Can be from the anim graph, or a different skeletal mesh component.

- `source` (PoseLink): [Read-Write] Input pose to be modified by the retargeter when using “Source Pose Pin” mode as the Input Pose Mode.

- `source_mesh_component` (SkeletalMeshComponent): [Read-Write] The Skeletal Mesh Component to retarget animation from. Assumed to be animated and tick BEFORE this anim instance.

- `suppress_warnings` (bool): [Read-Write] Toggle whether to print warnings about missing or incorrectly configured retarget configurations.



---

_property_ `custom_retarget_profile`: RetargetProfile

[Read-Write] Connect a custom retarget profile to modify the retargeter’s settings at runtime.

**Type:**

( RetargetProfile)


---

_property_ `ik_retargeter_asset`: IKRetargeter

[Read-Write] Retarget asset to use. Must define a Source and Target IK Rig compatible with the SourceMeshComponent and current anim instance.

**Type:**

( IKRetargeter)


---

_property_ `lod_threshold`: int

[Read-Write] Max LOD that this node is allowed to run.
For example if you have LODThreshold at 2, it will run until LOD 2 (based on 0 index) when the component LOD becomes 3, it will stop update/evaluate
A value of -1 forces the node to execute at all LOD levels.

**Type:**

(int32)


---

_property_ `lod_threshold_for_ik`: int

[Read-Write] Max LOD that IK is allowed to run.
For example if you have LODThresholdForIK at 2, it will skip the IK pass on LODs 3 and greater.
This only disables IK and does not affect the Root or FK passes.
A value of -1 forces the node to execute at all LOD levels.

**Type:**

(int32)


---

_property_ `retarget_from`: RetargetSourceMode

[Read-Write] Specify where to get the source pose to retarget from. Can be from the anim graph, or a different skeletal mesh component.

**Type:**

( RetargetSourceMode)


---

_property_ `source_mesh_component`: SkeletalMeshComponent

[Read-Write] The Skeletal Mesh Component to retarget animation from. Assumed to be animated and tick BEFORE this anim instance.

**Type:**

( SkeletalMeshComponent)


---

_property_ `suppress_warnings`: bool

[Read-Write] Toggle whether to print warnings about missing or incorrectly configured retarget configurations.

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_RetargetPoseFromMesh`
  - `AnimNode_RetargetPoseFromMesh`
    - `AnimNode_RetargetPoseFromMesh.custom_retarget_profile`
    - `AnimNode_RetargetPoseFromMesh.ik_retargeter_asset`
    - `AnimNode_RetargetPoseFromMesh.lod_threshold`
    - `AnimNode_RetargetPoseFromMesh.lod_threshold_for_ik`
    - `AnimNode_RetargetPoseFromMesh.retarget_from`
    - `AnimNode_RetargetPoseFromMesh.source_mesh_component`
    - `AnimNode_RetargetPoseFromMesh.suppress_warnings`