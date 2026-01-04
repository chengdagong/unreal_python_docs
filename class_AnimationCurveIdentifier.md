# unreal.AnimationCurveIdentifier

```python
class unreal.AnimationCurveIdentifier
```


**Bases:** ``StructBase``


Script-friendly structure for identifying an animation curve.
Wrapping the unique type and smart-name for use within the AnimDataController API.

**C++ Source:**

- **Module**: Engine

- **File**: CurveIdentifier.h



---

**get_name**() → `NameReturns:`

The name used for displaying the Curve Identifier

Return type:

Name


---

**get_transform_child_curve_identifier**( _channel_, _axis_) → `bool`

Converts a valid FAnimationCurveIdentifier instance with RCT\_Transform curve type to target a child curve.

Parameters:

- **channel** ( _TransformCurveChannel_) – Channel to target

- **axis** ( _VectorCurveChannel_) – Axis within channel to target


Returns:

Valid FAnimationCurveIdentifier if the operation was successful

Return type:

bool


---

**get_type**() → `RawCurveTrackTypesReturns:`

The animation curve type for the curve represented by the Curve Identifier

Return type:

RawCurveTrackTypes


---

**is_valid**() → `boolReturns:`

Whether or not the Curve Identifier is valid

Return type:

bool


---

**set_curve_identifier**( _name_, _curve_type_) → `None`

Constructs a valid FAnimationCurveIdentifier instance.

Parameters:

- **name** ( _Name_) – Name of the curve to find or add

- **curve\_type** ( _RawCurveTrackTypes_) – Type of the curve to find or add


### Table of Contents

- `unreal.AnimationCurveIdentifier`
  - `AnimationCurveIdentifier`
    - `AnimationCurveIdentifier.get_name()`
    - `AnimationCurveIdentifier.get_transform_child_curve_identifier()`
    - `AnimationCurveIdentifier.get_type()`
    - `AnimationCurveIdentifier.is_valid()`
    - `AnimationCurveIdentifier.set_curve_identifier()`