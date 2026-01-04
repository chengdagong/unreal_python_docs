# unreal.PhysicalMaterialMask

```python
class unreal.PhysicalMaterialMask(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Physical material masks are used to map multiple physical materials to a single rendering material

**C++ Source:**

- **Module**: Engine

- **File**: PhysicalMaterialMask.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `address_x` (TextureAddress): [Read-Write] The addressing mode to use for the X axis.

- `address_y` (TextureAddress): [Read-Write] The addressing mode to use for the Y axis.

- `asset_import_data` (AssetImportData): [Read-Only]

- `mask_texture` (Texture): [Read-Only] Mask input texture, square aspect ratio recommended. Recognized mask colors include: white, black, red, green, yellow, cyan, turquoise, and magenta.

- `uv_channel_index` (int32): [Read-Write] StaticMesh UV channel index to use when performing lookups with this mask.



---

_property_ `address_x`: TextureAddress

[Read-Write] The addressing mode to use for the X axis.

**Type:**

( TextureAddress)


---

_property_ `address_y`: TextureAddress

[Read-Write] The addressing mode to use for the Y axis.

**Type:**

( TextureAddress)


---

_property_ `mask_texture`: Texture

white, black, red, green, yellow, cyan, turquoise, and magenta.

**Type:**

( Texture)

**Type:**

[Read-Only] Mask input texture, square aspect ratio recommended. Recognized mask colors include


---

_property_ `uv_channel_index`: int

[Read-Write] StaticMesh UV channel index to use when performing lookups with this mask.

**Type:**

(int32)

### Table of Contents

- `unreal.PhysicalMaterialMask`
  - `PhysicalMaterialMask`
    - `PhysicalMaterialMask.address_x`
    - `PhysicalMaterialMask.address_y`
    - `PhysicalMaterialMask.mask_texture`
    - `PhysicalMaterialMask.uv_channel_index`