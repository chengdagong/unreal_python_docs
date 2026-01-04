# unreal.AbcConversionSettings

```python
class unreal.AbcConversionSettings(preset:AbcConversionPreset=Ellipsis, flip_u:bool=False, flip_v:bool=False, scale:Vector=Ellipsis, rotation:Vector=Ellipsis)
```


**Bases:** ``StructBase``


Abc Conversion Settings

**C++ Source:**

- **Plugin**: AlembicImporter

- **Module**: AlembicLibrary

- **File**: AbcImportSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `flip_u` (bool): [Read-Write] Flag whether or not to flip the U channel in the Texture Coordinates

- `flip_v` (bool): [Read-Write] Flag whether or not to flip the V channel in the Texture Coordinates

- `preset` (AbcConversionPreset): [Read-Write] Currently preset that should be applied

- `rotation` (Vector): [Read-Write] Rotation in Euler angles that should be applied

- `scale` (Vector): [Read-Write] Scale value that should be applied



---

_property_ `flip_u`: bool

[Read-Write] Flag whether or not to flip the U channel in the Texture Coordinates

**Type:**

( bool)


---

_property_ `flip_v`: bool

[Read-Write] Flag whether or not to flip the V channel in the Texture Coordinates

**Type:**

( bool)


---

_property_ `preset`: AbcConversionPreset

[Read-Write] Currently preset that should be applied

**Type:**

( AbcConversionPreset)


---

_property_ `rotation`: Vector

[Read-Write] Rotation in Euler angles that should be applied

**Type:**

( Vector)


---

_property_ `scale`: Vector

[Read-Write] Scale value that should be applied

**Type:**

( Vector)

### Table of Contents

- `unreal.AbcConversionSettings`
  - `AbcConversionSettings`
    - `AbcConversionSettings.flip_u`
    - `AbcConversionSettings.flip_v`
    - `AbcConversionSettings.preset`
    - `AbcConversionSettings.rotation`
    - `AbcConversionSettings.scale`