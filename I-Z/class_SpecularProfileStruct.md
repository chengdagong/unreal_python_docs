# unreal.SpecularProfileStruct

```python
class unreal.SpecularProfileStruct(format:SpecularProfileFormat=Ellipsis, texture:Texture2D=Ellipsis)
```


**Bases:** ``StructBase``


struct with all the settings we want in USpecularProfile, separate to make it easer to pass this data around in the engine.

**C++ Source:**

- **Module**: Engine

- **File**: SpecularProfile.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `format` (SpecularProfileFormat): [Read-Write] Define the format driving the sampling of the specular LUT.

- `light_color` (RuntimeCurveLinearColor): [Read-Write] Define the light facing color
Exemple with View/Light mode: color at 0 is applied when NoL=0 (light hit the surface at grazing angle) while color at 1 is applied when NoV=1 (light hit the surface at facing angle).

- `texture` (Texture2D): [Read-Write] Define the texture used as a specular profile

- `view_color` (RuntimeCurveLinearColor): [Read-Write] Define the view facing color.
Exemple with View/Light mode: color at 0 is applied when NoV=0 (view grazing angle) while color at 1 is applied when NoV=1 (view facing angle).



---

_property_ `format`: SpecularProfileFormat

[Read-Only] Define the format driving the sampling of the specular LUT.

**Type:**

( SpecularProfileFormat)


---

_property_ `texture`: Texture2D

[Read-Only] Define the texture used as a specular profile

**Type:**

( Texture2D)

### Table of Contents

- `unreal.SpecularProfileStruct`
  - `SpecularProfileStruct`
    - `SpecularProfileStruct.format`
    - `SpecularProfileStruct.texture`