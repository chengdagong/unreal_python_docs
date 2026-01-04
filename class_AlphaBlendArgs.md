# unreal.AlphaBlendArgs

```python
class unreal.AlphaBlendArgs(custom_curve:CurveFloat=Ellipsis, blend_time:float=0.0, blend_option:AlphaBlendOption=Ellipsis)
```


**Bases:** ``StructBase``


Alpha Blend construction arguments. Used for creation of an AlphaBlend.

**C++ Source:**

- **Module**: Engine

- **File**: AlphaBlend.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend_option` (AlphaBlendOption): [Read-Write] Type of blending used (Linear, Cubic, etc.)

- `blend_time` (float): [Read-Write] Blend Time

- `custom_curve` (CurveFloat): [Read-Write] If you’re using Custom BlendOption, you can specify curve



---

_property_ `blend_option`: AlphaBlendOption

[Read-Write] Type of blending used (Linear, Cubic, etc.)

**Type:**

( AlphaBlendOption)


---

_property_ `blend_time`: float

[Read-Write] Blend Time

**Type:**

( float)


---

_property_ `custom_curve`: CurveFloat

[Read-Write] If you’re using Custom BlendOption, you can specify curve

**Type:**

( CurveFloat)

### Table of Contents

- `unreal.AlphaBlendArgs`
  - `AlphaBlendArgs`
    - `AlphaBlendArgs.blend_option`
    - `AlphaBlendArgs.blend_time`
    - `AlphaBlendArgs.custom_curve`