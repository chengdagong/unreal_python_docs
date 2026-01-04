# unreal.BrushBlendType

```python
class unreal.BrushBlendType
```


**Bases:** ``EnumBase``


The blend mode changes how the brush material is applied to the terrain.

**C++ Source:**

- **Plugin**: Landmass

- **Module**: Landmass

- **File**: TerrainCarvingSettings.h


ADDITIVE _: BrushBlendType_ _=Ellipsis_

Performs an additive blend, using a flat Z=0 terrain as the input. Useful when you want to preserve underlying detail or ramps.

**Type:**

3

ALPHA\_BLEND _: BrushBlendType_ _=Ellipsis_

Alpha Blend will affect the heightmap both upwards and downwards.

**Type:**

0

MAX _: BrushBlendType_ _=Ellipsis_

Limits the brush to only raising the terrain.

**Type:**

2

MIN _: BrushBlendType_ _=Ellipsis_

Limits the brush to only lowering the terrain.

**Type:**

1

### Table of Contents

- `unreal.BrushBlendType`
  - `BrushBlendType`
    - `BrushBlendType.ADDITIVE`
    - `BrushBlendType.ALPHA_BLEND`
    - `BrushBlendType.MAX`
    - `BrushBlendType.MIN`