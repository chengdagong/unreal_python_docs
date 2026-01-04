# unreal.AbcCompressionSettings

```python
class unreal.AbcCompressionSettings(merge_meshes:bool=False, bake_matrix_animation:bool=False, base_calculation_type:BaseCalculationType=0, percentage_of_total_bases:float=0.0, max_number_of_bases:int=0, minimum_number_of_vertex_influence_percentage:float=0.0)
```


**Bases:** ``StructBase``


Abc Compression Settings

**C++ Source:**

- **Plugin**: AlembicImporter

- **Module**: AlembicLibrary

- **File**: AbcImportSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `bake_matrix_animation` (bool): [Read-Write] Whether or not Matrix-only animation should be baked out as vertex animation (or skipped?)

- `base_calculation_type` (BaseCalculationType): [Read-Write] Determines how the final number of bases that are stored as morph targets are calculated

- `max_number_of_bases` (int32): [Read-Write] Will generate given fixed number of bases as morph targets

- `merge_meshes` (bool): [Read-Write] Whether or not the individual meshes should be merged for compression purposes

- `minimum_number_of_vertex_influence_percentage` (float): [Read-Write] Minimum percentage of influenced vertices required for a morph target to be valid

- `percentage_of_total_bases` (float): [Read-Write] Will generate given percentage of the given bases as morph targets



---

_property_ `bake_matrix_animation`: bool

[Read-Write] Whether or not Matrix-only animation should be baked out as vertex animation (or skipped?)

**Type:**

( bool)


---

_property_ `base_calculation_type`: BaseCalculationType

[Read-Write] Determines how the final number of bases that are stored as morph targets are calculated

**Type:**

( BaseCalculationType)


---

_property_ `max_number_of_bases`: int

[Read-Write] Will generate given fixed number of bases as morph targets

**Type:**

(int32)


---

_property_ `merge_meshes`: bool

[Read-Write] Whether or not the individual meshes should be merged for compression purposes

**Type:**

( bool)


---

_property_ `minimum_number_of_vertex_influence_percentage`: float

[Read-Write] Minimum percentage of influenced vertices required for a morph target to be valid

**Type:**

( float)


---

_property_ `percentage_of_total_bases`: float

[Read-Write] Will generate given percentage of the given bases as morph targets

**Type:**

( float)

### Table of Contents

- `unreal.AbcCompressionSettings`
  - `AbcCompressionSettings`
    - `AbcCompressionSettings.bake_matrix_animation`
    - `AbcCompressionSettings.base_calculation_type`
    - `AbcCompressionSettings.max_number_of_bases`
    - `AbcCompressionSettings.merge_meshes`
    - `AbcCompressionSettings.minimum_number_of_vertex_influence_percentage`
    - `AbcCompressionSettings.percentage_of_total_bases`