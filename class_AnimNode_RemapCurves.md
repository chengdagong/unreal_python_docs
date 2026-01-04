# unreal.AnimNode_RemapCurves

```python
class unreal.AnimNode_RemapCurves(source_pose:PoseLink=\[\], expression_list:CurveExpressionList=\[\], curve_expressions_data_asset:CurveExpressionsDataAsset=Ellipsis, curve_expressions:None={}, expressions_immutable:bool=False)
```


**Bases:** ``AnimNode_RemapCurvesBase``


Anim Node Remap Curves

**C++ Source:**

- **Plugin**: CurveExpression

- **Module**: CurveExpression

- **File**: AnimNode\_RemapCurves.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `curve_expressions` (Map[Name, str]): [Read-Write]

- `curve_expressions_data_asset` (CurveExpressionsDataAsset): [Read-Write]

- `expression_list` (CurveExpressionList): [Read-Write]

- `expression_source` (RemapCurvesExpressionSource): [Read-Write]

- `expressions_immutable` (bool): [Read-Write] The expression map given is immutable and will not change during runtime. Improves performance.

- `source_pose` (PoseLink): [Read-Write]


### Table of Contents

- `unreal.AnimNode_RemapCurves`
  - `AnimNode_RemapCurves`