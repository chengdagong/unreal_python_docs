# unreal.AnimationCurveData

```python
class unreal.AnimationCurveData(float_curves:None=\[\], transform_curves:None=\[\])
```


**Bases:** ``StructBase``


Structure encapsulating animated curve data. Currently only contains Float and Transform curves.

**C++ Source:**

- **Module**: Engine

- **File**: IAnimationDataModel.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `float_curves` (Array[FloatCurve]): [Read-Only] Float-based animation curves

- `transform_curves` (Array[TransformCurve]): [Read-Only] FTransform-based animation curves, used for animation layer editing



---

_property_ `float_curves`: None

[Read-Only] Float-based animation curves

**Type:**

( Array\ [FloatCurve])


---

_property_ `transform_curves`: None

[Read-Only] FTransform-based animation curves, used for animation layer editing

**Type:**

( Array\ [TransformCurve])

### Table of Contents

- `unreal.AnimationCurveData`
  - `AnimationCurveData`
    - `AnimationCurveData.float_curves`
    - `AnimationCurveData.transform_curves`