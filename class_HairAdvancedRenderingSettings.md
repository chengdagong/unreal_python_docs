# unreal.HairAdvancedRenderingSettings

```python
class unreal.HairAdvancedRenderingSettings(use_stable_rasterization:bool=False, scatter_scene_lighting:bool=False)
```


**Bases:** ``StructBase``


Hair Advanced Rendering Settings

**C++ Source:**

- **Plugin**: HairStrands

- **Module**: HairStrandsCore

- **File**: GroomAssetRendering.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `scatter_scene_lighting` (bool): [Read-Write] Light hair with the scene color. This is used for vellus/short hair to bring light from the surrounding surface, like skin.

- `use_stable_rasterization` (bool): [Read-Write] Insure the hair does not alias. When enable, group of hairs might appear thicker. Isolated hair should remain thin.



---

_property_ `scatter_scene_lighting`: bool

[Read-Only] Light hair with the scene color. This is used for vellus/short hair to bring light from the surrounding surface, like skin.

**Type:**

( bool)


---

_property_ `use_stable_rasterization`: bool

[Read-Only] Insure the hair does not alias. When enable, group of hairs might appear thicker. Isolated hair should remain thin.

**Type:**

( bool)

### Table of Contents

- `unreal.HairAdvancedRenderingSettings`
  - `HairAdvancedRenderingSettings`
    - `HairAdvancedRenderingSettings.scatter_scene_lighting`
    - `HairAdvancedRenderingSettings.use_stable_rasterization`