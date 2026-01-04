# unreal.SkeletalMeshMergeParams

```python
class unreal.SkeletalMeshMergeParams(mesh_section_mappings:None=\[\], uv_transforms_per_mesh:None=\[\], meshes_to_merge:None=\[\], strip_top_lods:int=0, needs_cpu_access:bool=False, skeleton_before:bool=False, skeleton:Skeleton=Ellipsis)
```


**Bases:** ``StructBase``


Struct containing all parameters used to perform a Skeletal Mesh merge.

**C++ Source:**

- **Plugin**: SkeletalMerging

- **Module**: SkeletalMerging

- **File**: SkeletalMergingLibrary.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `mesh_section_mappings` (Array[SkelMeshMergeSectionMapping]): [Read-Write] An optional array to map sections from the source meshes to merged section entries

- `meshes_to_merge` (Array[SkeletalMesh]): [Read-Write] The list of skeletal meshes to merge.

- `needs_cpu_access` (bool): [Read-Write] Whether or not the resulting mesh needs to be accessed by the CPU for any reason (e.g. for spawning particle effects).

- `skeleton` (Skeleton): [Read-Write] Skeleton that will be used for the merged mesh.
Leave empty if the generated skeleton is OK.

- `skeleton_before` (bool): [Read-Write] Update skeleton before merge. Otherwise, update after.
Skeleton must also be provided.

- `strip_top_lods` (int32): [Read-Write] The number of high LODs to remove from input meshes

- `uv_transforms_per_mesh` (Array[SkelMeshMergeMeshUVTransforms]): [Read-Write] An optional array to transform the UVs in each mesh



---

_property_ `mesh_section_mappings`: None

[Read-Write] An optional array to map sections from the source meshes to merged section entries

**Type:**

( Array\ [SkelMeshMergeSectionMapping])


---

_property_ `meshes_to_merge`: None

[Read-Write] The list of skeletal meshes to merge.

**Type:**

( Array\ [SkeletalMesh])


---

_property_ `needs_cpu_access`: bool

[Read-Write] Whether or not the resulting mesh needs to be accessed by the CPU for any reason (e.g. for spawning particle effects).

**Type:**

( bool)


---

_property_ `skeleton`: Skeleton

[Read-Write] Skeleton that will be used for the merged mesh.
Leave empty if the generated skeleton is OK.

**Type:**

( Skeleton)


---

_property_ `skeleton_before`: bool

[Read-Write] Update skeleton before merge. Otherwise, update after.
Skeleton must also be provided.

**Type:**

( bool)


---

_property_ `strip_top_lods`: int

[Read-Write] The number of high LODs to remove from input meshes

**Type:**

(int32)


---

_property_ `uv_transforms_per_mesh`: None

[Read-Write] An optional array to transform the UVs in each mesh

**Type:**

( Array\ [SkelMeshMergeMeshUVTransforms])

### Table of Contents

- `unreal.SkeletalMeshMergeParams`
  - `SkeletalMeshMergeParams`
    - `SkeletalMeshMergeParams.mesh_section_mappings`
    - `SkeletalMeshMergeParams.meshes_to_merge`
    - `SkeletalMeshMergeParams.needs_cpu_access`
    - `SkeletalMeshMergeParams.skeleton`
    - `SkeletalMeshMergeParams.skeleton_before`
    - `SkeletalMeshMergeParams.strip_top_lods`
    - `SkeletalMeshMergeParams.uv_transforms_per_mesh`