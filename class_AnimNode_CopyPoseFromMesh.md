# unreal.AnimNode_CopyPoseFromMesh

```python
class unreal.AnimNode_CopyPoseFromMesh(source_mesh_component:SkeletalMeshComponent=Ellipsis, use_attached_parent:bool=False, copy_curves:bool=False, copy_custom_attributes:bool=False, use_mesh_pose:bool=False, root_bone_to_copy:Name='None')
```


**Bases:** ``AnimNode_Base``


Simple controller to copy a bone’s transform to another one.

**C++ Source:**

- **Module**: AnimGraphRuntime

- **File**: AnimNode\_CopyPoseFromMesh.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `copy_curves` (bool): [Read-Write] Copy curves also from SouceMeshComponent. This will copy the curves if this instance also contains curve attributes

- `copy_custom_attributes` (bool): [Read-Write] Copy custom attributes (animation attributes) from SourceMeshComponent

- `root_bone_to_copy` (Name): [Read-Write] If you want to specify copy root, use this - this will ensure copy only below of this joint (inclusively)

- `source_mesh_component` (SkeletalMeshComponent): [Read-Write] This is used by default if it’s valid

- `use_attached_parent` (bool): [Read-Write] If SourceMeshComponent is not valid, and if this is true, it will look for attahced parent as a source

- `use_mesh_pose` (bool): [Read-Write] Use root space transform to copy to the target pose. By default, it copies their relative transform (bone space)



---

_property_ `copy_curves`: bool

[Read-Write] Copy curves also from SouceMeshComponent. This will copy the curves if this instance also contains curve attributes

**Type:**

( bool)


---

_property_ `copy_custom_attributes`: bool

[Read-Write] Copy custom attributes (animation attributes) from SourceMeshComponent

**Type:**

( bool)


---

_property_ `root_bone_to_copy`: Name

[Read-Write] If you want to specify copy root, use this - this will ensure copy only below of this joint (inclusively)

**Type:**

( Name)


---

_property_ `source_mesh_component`: SkeletalMeshComponent

[Read-Write] This is used by default if it’s valid

**Type:**

( SkeletalMeshComponent)


---

_property_ `use_attached_parent`: bool

[Read-Write] If SourceMeshComponent is not valid, and if this is true, it will look for attahced parent as a source

**Type:**

( bool)


---

_property_ `use_mesh_pose`: bool

[Read-Write] Use root space transform to copy to the target pose. By default, it copies their relative transform (bone space)

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_CopyPoseFromMesh`
  - `AnimNode_CopyPoseFromMesh`
    - `AnimNode_CopyPoseFromMesh.copy_curves`
    - `AnimNode_CopyPoseFromMesh.copy_custom_attributes`
    - `AnimNode_CopyPoseFromMesh.root_bone_to_copy`
    - `AnimNode_CopyPoseFromMesh.source_mesh_component`
    - `AnimNode_CopyPoseFromMesh.use_attached_parent`
    - `AnimNode_CopyPoseFromMesh.use_mesh_pose`