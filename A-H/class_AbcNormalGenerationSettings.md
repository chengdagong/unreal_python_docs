# unreal.AbcNormalGenerationSettings

```python
class unreal.AbcNormalGenerationSettings(force_one_smoothing_group_per_object:bool=False, hard_edge_angle_threshold:float=0.0, recompute_normals:bool=False, ignore_degenerate_triangles:bool=False, skip_computing_tangents:bool=False)
```


**Bases:** ``StructBase``


Abc Normal Generation Settings

**C++ Source:**

- **Plugin**: AlembicImporter

- **Module**: AlembicLibrary

- **File**: AbcImportSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `force_one_smoothing_group_per_object` (bool): [Read-Write] Whether or not to force smooth normals for each individual object rather than calculating smoothing groups

- `hard_edge_angle_threshold` (float): [Read-Write] Threshold used to determine whether an angle between two normals should be considered hard, closer to 0 means more smooth vs 1

- `ignore_degenerate_triangles` (bool): [Read-Write] Determines whether or not the degenerate triangles should be ignored when calculating tangents/normals

- `recompute_normals` (bool): [Read-Write] Determines whether or not the normals should be forced to be recomputed

- `skip_computing_tangents` (bool): [Read-Write] Determines whether tangents are computed for GeometryCache. Skipping them can improve streaming performance but may cause visual artifacts where they are required



---

_property_ `force_one_smoothing_group_per_object`: bool

[Read-Write] Whether or not to force smooth normals for each individual object rather than calculating smoothing groups

**Type:**

( bool)


---

_property_ `hard_edge_angle_threshold`: float

[Read-Write] Threshold used to determine whether an angle between two normals should be considered hard, closer to 0 means more smooth vs 1

**Type:**

( float)


---

_property_ `ignore_degenerate_triangles`: bool

[Read-Write] Determines whether or not the degenerate triangles should be ignored when calculating tangents/normals

**Type:**

( bool)


---

_property_ `recompute_normals`: bool

[Read-Write] Determines whether or not the normals should be forced to be recomputed

**Type:**

( bool)


---

_property_ `skip_computing_tangents`: bool

[Read-Write] Determines whether tangents are computed for GeometryCache. Skipping them can improve streaming performance but may cause visual artifacts where they are required

**Type:**

( bool)

### Table of Contents

- `unreal.AbcNormalGenerationSettings`
  - `AbcNormalGenerationSettings`
    - `AbcNormalGenerationSettings.force_one_smoothing_group_per_object`
    - `AbcNormalGenerationSettings.hard_edge_angle_threshold`
    - `AbcNormalGenerationSettings.ignore_degenerate_triangles`
    - `AbcNormalGenerationSettings.recompute_normals`
    - `AbcNormalGenerationSettings.skip_computing_tangents`