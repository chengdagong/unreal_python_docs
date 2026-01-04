# unreal.AnimNode_RemapCurvesBase

```python
class unreal.AnimNode_RemapCurvesBase(source_pose:PoseLink=\[\], expression_list:CurveExpressionList=\[\], curve_expressions_data_asset:CurveExpressionsDataAsset=Ellipsis, curve_expressions:None={}, expressions_immutable:bool=False)
```


**Bases:** ``AnimNode_Base``


Anim Node Remap Curves Base

**C++ Source:**

- **Plugin**: CurveExpression

- **Module**: CurveExpression

- **File**: AnimNode\_RemapCurvesBase.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `curve_expressions` (Map[Name, str]): [Read-Write]

- `curve_expressions_data_asset` (CurveExpressionsDataAsset): [Read-Write]

- `expression_list` (CurveExpressionList): [Read-Write]

- `expression_source` (RemapCurvesExpressionSource): [Read-Write]

- `expressions_immutable` (bool): [Read-Write] The expression map given is immutable and will not change during runtime. Improves performance.

- `source_pose` (PoseLink): [Read-Write]



---

_property_ `curve_expressions`: None

[Read-Write]

**Type:**

( Map\ [Name, str])


---

_property_ `curve_expressions_data_asset`: CurveExpressionsDataAsset

[Read-Write]

**Type:**

( CurveExpressionsDataAsset)


---

_property_ `expression_list`: CurveExpressionList

[Read-Only]

**Type:**

( CurveExpressionList)


---

_property_ `expressions_immutable`: bool

[Read-Write] The expression map given is immutable and will not change during runtime. Improves performance.

**Type:**

( bool)


---

_property_ `source_pose`: PoseLink

[Read-Write]

**Type:**

( PoseLink)

### Table of Contents

- `unreal.AnimNode_RemapCurvesBase`
  - `AnimNode_RemapCurvesBase`
    - `AnimNode_RemapCurvesBase.curve_expressions`
    - `AnimNode_RemapCurvesBase.curve_expressions_data_asset`
    - `AnimNode_RemapCurvesBase.expression_list`
    - `AnimNode_RemapCurvesBase.expressions_immutable`
    - `AnimNode_RemapCurvesBase.source_pose`