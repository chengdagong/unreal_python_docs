# unreal.AnimNode_RemapCurvesFromMesh

```python
class unreal.AnimNode_RemapCurvesFromMesh(source_pose:PoseLink=\[\], expression_list:CurveExpressionList=\[\], curve_expressions_data_asset:CurveExpressionsDataAsset=Ellipsis, curve_expressions:None={}, expressions_immutable:bool=False, source_mesh_component:SkeletalMeshComponent=Ellipsis, use_attached_parent:bool=False)
```


**Bases:** ``AnimNode_RemapCurvesBase``


Anim Node Remap Curves from Mesh

**C++ Source:**

- **Plugin**: CurveExpression

- **Module**: CurveExpression

- **File**: AnimNode\_RemapCurvesFromMesh.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `curve_expressions` (Map[Name, str]): [Read-Write]

- `curve_expressions_data_asset` (CurveExpressionsDataAsset): [Read-Write]

- `expression_list` (CurveExpressionList): [Read-Write]

- `expression_source` (RemapCurvesExpressionSource): [Read-Write]

- `expressions_immutable` (bool): [Read-Write] The expression map given is immutable and will not change during runtime. Improves performance.

- `source_mesh_component` (SkeletalMeshComponent): [Read-Write] This is used by default if it’s valid

- `source_pose` (PoseLink): [Read-Write]

- `use_attached_parent` (bool): [Read-Write] If SourceMeshComponent is not valid, and if this is true, it will look for attached parent as a source



---

_property_ `source_mesh_component`: SkeletalMeshComponent

[Read-Write] This is used by default if it’s valid

**Type:**

( SkeletalMeshComponent)


---

_property_ `use_attached_parent`: bool

[Read-Write] If SourceMeshComponent is not valid, and if this is true, it will look for attached parent as a source

**Type:**

( bool)

### Table of Contents

- `unreal.AnimNode_RemapCurvesFromMesh`
  - `AnimNode_RemapCurvesFromMesh`
    - `AnimNode_RemapCurvesFromMesh.source_mesh_component`
    - `AnimNode_RemapCurvesFromMesh.use_attached_parent`