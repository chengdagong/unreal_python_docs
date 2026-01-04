# unreal.FontFace

```python
class unreal.FontFace(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


A font face asset contains the raw payload data for a source TTF/OTF file as used by FreeType.
During cook this asset type generates a “.ufont” file containing the raw payload data (unless loaded “Inline”).

**C++ Source:**

- **Module**: Engine

- **File**: FontFace.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `ascend_overridden_value` (int32): [Read-Write] The typographic ascender of the face, expressed in font units.

- `descend_overridden_value` (int32): [Read-Write] The typographic ascender of the face, expressed in font units.

- `enable_distance_field_rendering` (bool): [Read-Write] Enables distance field rendering for this face (otherwise only Bitmap rendering is used)

- `hinting` (FontHinting): [Read-Write] The hinting algorithm to use with the font face.

- `is_ascend_overridden` (bool): [Read-Write] Activate this option to use the specified ascend value instead of the value from the font.

- `is_descend_overridden` (bool): [Read-Write] Activate this option to use the specified descend value instead of the value from the font.

- `layout_method` (FontLayoutMethod): [Read-Write] Which method should we use when laying out the font? Try changing this if you notice clipping or height issues with your font.

- `loading_policy` (FontLoadingPolicy): [Read-Write] Enum controlling how this font face should be loaded at runtime. See the enum for more explanations of the options.

- `max_distance_field_ppem` (int32): [Read-Write] Single-channel distance field px/em resolution “high” quality value

- `max_multi_distance_field_ppem` (int32): [Read-Write] Multi-channel distance field px/em resolution “high” quality value

- `mid_distance_field_ppem` (int32): [Read-Write] Single-channel distance field px/em resolution “medium” quality value

- `mid_multi_distance_field_ppem` (int32): [Read-Write] Multi-channel distance field px/em resolution “medium” quality value

- `min_distance_field_ppem` (int32): [Read-Write] Single-channel distance field px/em resolution “low” quality value

- `min_multi_distance_field_ppem` (int32): [Read-Write] Multi-channel distance field px/em resolution “low” quality value

- `platform_rasterization_mode_overrides` (‘undefined’): [Read-Write] If set, allows to override distance field modes set in device profiles

- `source_filename` (str): [Read-Write] The filename of the font face we were created from. This may not always exist on disk, as we may have previously loaded and cached the font data inside this asset.

- `strike_brush_height_percentage` (int32): [Read-Write] The percentage of the font height to draw the strike brush at.
0% is the bottom, 100% is the top.

- `sub_faces` (Array[str]): [Read-Only] Transient cache of the sub-faces available within this face



---

_property_ `hinting`: FontHinting

[Read-Write] The hinting algorithm to use with the font face.

**Type:**

( FontHinting)


---

_property_ `layout_method`: FontLayoutMethod

[Read-Write] Which method should we use when laying out the font? Try changing this if you notice clipping or height issues with your font.

**Type:**

( FontLayoutMethod)


---

_property_ `loading_policy`: FontLoadingPolicy

[Read-Write] Enum controlling how this font face should be loaded at runtime. See the enum for more explanations of the options.

**Type:**

( FontLoadingPolicy)


---

_property_ `source_filename`: str

[Read-Only] The filename of the font face we were created from. This may not always exist on disk, as we may have previously loaded and cached the font data inside this asset.

**Type:**

( str)


---

_property_ `strike_brush_height_percentage`: int

[Read-Write] The percentage of the font height to draw the strike brush at.
0% is the bottom, 100% is the top.

**Type:**

(int32)

### Table of Contents

- `unreal.FontFace`
  - `FontFace`
    - `FontFace.hinting`
    - `FontFace.layout_method`
    - `FontFace.loading_policy`
    - `FontFace.source_filename`
    - `FontFace.strike_brush_height_percentage`