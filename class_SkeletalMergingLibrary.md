# unreal.SkeletalMergingLibrary

```python
class unreal.SkeletalMergingLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Component that can be used to perform Skeletal Mesh merges from Blueprints.

**C++ Source:**

- **Plugin**: SkeletalMerging

- **Module**: SkeletalMerging

- **File**: SkeletalMergingLibrary.h



---

_classmethod_ merge_meshes( _params_)→SkeletalMesh

Merges the given meshes into a single mesh.

Parameters:

**params** ( _SkeletalMeshMergeParams_)

Returns:

The merged mesh (will be invalid if the merge failed).

Return type:

SkeletalMesh


---

_classmethod_ merge_skeletons( _params_)→Skeleton

Merges the skeletons for the provided meshes into a single skeleton.

Parameters:

**params** ( _SkeletonMergeParams_)

Returns:

The merged Skeleton

Return type:

Skeleton

### Table of Contents

- `unreal.SkeletalMergingLibrary`
  - `SkeletalMergingLibrary`
    - `SkeletalMergingLibrary.merge_meshes()`
    - `SkeletalMergingLibrary.merge_skeletons()`