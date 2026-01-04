# unreal.AbcStaticMeshSettings

```python
class unreal.AbcStaticMeshSettings(merge_meshes:bool=False, propagate_matrix_transformations:bool=False, generate_lightmap_u_vs:bool=False)
```


**Bases:** ``StructBase``


Abc Static Mesh Settings

**C++ Source:**

- **Plugin**: AlembicImporter

- **Module**: AlembicLibrary

- **File**: AbcImportSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `generate_lightmap_u_vs` (bool): [Read-Write] Flag for whether or not lightmap UVs should be generated

- `merge_meshes` (bool): [Read-Write] Whether or not to merge the static meshes on import (remember this can cause problems with overlapping UV-sets)

- `propagate_matrix_transformations` (bool): [Read-Write] This will, if applicable, apply matrix transformations to the meshes



---

_property_ `generate_lightmap_u_vs`: bool

[Read-Write] Flag for whether or not lightmap UVs should be generated

**Type:**

( bool)


---

_property_ `merge_meshes`: bool

[Read-Write] Whether or not to merge the static meshes on import (remember this can cause problems with overlapping UV-sets)

**Type:**

( bool)


---

_property_ `propagate_matrix_transformations`: bool

[Read-Write] This will, if applicable, apply matrix transformations to the meshes

**Type:**

( bool)

### Table of Contents

- `unreal.AbcStaticMeshSettings`
  - `AbcStaticMeshSettings`
    - `AbcStaticMeshSettings.generate_lightmap_u_vs`
    - `AbcStaticMeshSettings.merge_meshes`
    - `AbcStaticMeshSettings.propagate_matrix_transformations`