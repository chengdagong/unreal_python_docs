# unreal.FleshAsset

```python
class unreal.FleshAsset(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


UFleshAsset (UObject)

UObject wrapper for the FFleshAsset

**C++ Source:**

- **Plugin**: ChaosFlesh

- **Module**: ChaosFleshEngine

- **File**: FleshAsset.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `dataflow_asset` (Dataflow): [Read-Write] Dataflow

- `dataflow_terminal` (str): [Read-Write]

- `overrides` (Array[StringValuePair]): [Read-Write]

- `render_in_editor` (bool): [Read-Write]

- `skeletal_mesh` (SkeletalMesh): [Read-Write] SkeletalMesh

- `skeleton` (Skeleton): [Read-Write]

- `static_mesh` (StaticMesh): [Read-Write] SkeletalMesh

- `target_deformation_skeleton` (SkeletalMesh): [Read-Write] Skeleton to use with the flesh deformer or c GetSkeletalMeshEmbeddedPositions() on the flesh component.
Bindings for this skeletal mesh must be stored in the rest collection.



---

_property_ `skeletal_mesh`: SkeletalMesh

[Read-Write] SkeletalMesh

**Type:**

( SkeletalMesh)


---

_property_ `skeleton`: Skeleton

[Read-Write]

**Type:**

( Skeleton)


---

_property_ `target_deformation_skeleton`: SkeletalMesh

[Read-Write] Skeleton to use with the flesh deformer or c GetSkeletalMeshEmbeddedPositions() on the flesh component.
Bindings for this skeletal mesh must be stored in the rest collection.

**Type:**

( SkeletalMesh)

### Table of Contents

- `unreal.FleshAsset`
  - `FleshAsset`
    - `FleshAsset.skeletal_mesh`
    - `FleshAsset.skeleton`
    - `FleshAsset.target_deformation_skeleton`