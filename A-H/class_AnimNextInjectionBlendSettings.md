# unreal.AnimNextInjectionBlendSettings

```python
class unreal.AnimNextInjectionBlendSettings(blend:AlphaBlendArgs=Ellipsis, blend_mode:AnimNextInjectionBlendMode=Ellipsis)
```


**Bases:** ``StructBase``


Injection Blend Settings

Encapsulates the blend settings used by injection requests.

**C++ Source:**

- **Plugin**: UAFAnimGraph

- **Module**: UAFAnimGraph

- **File**: InjectionRequest.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blend` (AlphaBlendArgs): [Read-Write] AlphaBlend options (time, curve, etc.)

- `blend_mode` (AnimNextInjectionBlendMode): [Read-Write] Type of blend mode (Standard vs Inertial)



---

_property_ `blend`: AlphaBlendArgs

[Read-Write] AlphaBlend options (time, curve, etc.)

**Type:**

( AlphaBlendArgs)


---

_property_ `blend_mode`: AnimNextInjectionBlendMode

[Read-Write] Type of blend mode (Standard vs Inertial)

**Type:**

( AnimNextInjectionBlendMode)

### Table of Contents

- `unreal.AnimNextInjectionBlendSettings`
  - `AnimNextInjectionBlendSettings`
    - `AnimNextInjectionBlendSettings.blend`
    - `AnimNextInjectionBlendSettings.blend_mode`