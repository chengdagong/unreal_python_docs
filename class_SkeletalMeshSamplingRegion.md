# unreal.SkeletalMeshSamplingRegion

```python
class unreal.SkeletalMeshSamplingRegion
```


**Bases:** ``StructBase``


Defined a named region on a mesh that will have associated triangles and bones for fast sampling at each enabled LOD.

**C++ Source:**

- **Module**: Engine

- **File**: SkeletalMeshSampling.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bone_filters` (Array[SkeletalMeshSamplingRegionBoneFilter]): [Read-Write] Filters to determine which triangles and bones to include in this region based on bone.

- `lod_index` (int32): [Read-Write] The LOD of the mesh that this region applies to.

- `material_filters` (Array[SkeletalMeshSamplingRegionMaterialFilter]): [Read-Write] Filters to determine which triangles to include in this region based on material.

- `name` (Name): [Read-Write] Name of this region that users will reference.

- `support_uniformly_distributed_sampling` (bool): [Read-Write] Mesh supports uniformly distributed sampling in constant time.
Memory cost is 8 bytes per triangle.


### Table of Contents

- `unreal.SkeletalMeshSamplingRegion`
  - `SkeletalMeshSamplingRegion`