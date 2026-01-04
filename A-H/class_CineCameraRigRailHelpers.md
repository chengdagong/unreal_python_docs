# unreal.CineCameraRigRailHelpers

```python
class unreal.CineCameraRigRailHelpers(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Cine Camera Rig Rail Helpers

**C++ Source:**

- **Plugin**: CineCameraRigs

- **Module**: CineCameraRigs

- **File**: CineCameraRigRailHelpers.h



---

_classmethod_ create_or_update_spline_heatmap_texture( _texture_, _data_values_, _low_value_, _average_value_, _high_value_)→Texture2D

Create a transient heatmap texture from data values

Parameters:

- **texture** ( _Texture2D_)

- **data\_values** ( _Array_ _\_ [_float_ _]_)

- **low\_value** ( _float_)

- **average\_value** ( _float_)

- **high\_value** ( _float_)


Returns:

texture (Texture2D):

Return type:

Texture2D

### Table of Contents

- `unreal.CineCameraRigRailHelpers`
  - `CineCameraRigRailHelpers`
    - `CineCameraRigRailHelpers.create_or_update_spline_heatmap_texture()`