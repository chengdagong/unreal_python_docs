# unreal.AbcGeometryCacheSettings

```python
class unreal.AbcGeometryCacheSettings(flatten_tracks: bool = False, store_imported_vertex_numbers: bool = False, apply_constant_topology_optimizations: bool = False, motion_vectors: AbcGeometryCacheMotionVectorsImport = Ellipsis, optimize_index_buffers: bool = False, compressed_position_precision: float = 0.0, compressed_texture_coordinates_number_of_bits: int = 0)
```

**Bases:** `StructBase`

Abc Geometry Cache Settings

**C++ Source:**

- **Plugin**: AlembicImporter
- **Module**: AlembicLibrary
- **File**: AbcImportSettings.h

**Editor Properties:** (see `get_editor_property`/`set_editor_property`)

- `apply_constant_topology_optimizations` (bool): [Read-Write] Force the preprocessor to only do optimization once instead of when the preprocessor decides. This may lead to some problems with certain meshes but makes sure motion blur always works if the topology is constant.
- `compressed_position_precision` (float): [Read-Write] Precision used for compressing vertex positions (lower = better result but less compression, higher = more lossy compression but smaller size)
- `compressed_texture_coordinates_number_of_bits` (int32): [Read-Write] Bit-precision used for compressing texture coordinates (hight = better result but less compression, lower = more lossy compression but smaller size)
- `flatten_tracks` (bool): [Read-Write] Whether or not to merge all vertex animation into one track
- `motion_vectors` (AbcGeometryCacheMotionVectorsImport): [Read-Write]
- `optimize_index_buffers` (bool): [Read-Write] Optimizes index buffers for each unique frame, to allow better cache coherency on the GPU. Very costly and time-consuming process, recommended to OFF.
- `store_imported_vertex_numbers` (bool): [Read-Write] Store the imported vertex numbers. This lets you know the vertex numbers inside the DCC. The values of each vertex number will range from 0 to 7 for a cube. Even if the number of positions might be 24.

---

_property_ `apply_constant_topology_optimizations`: bool

[Read-Write] Force the preprocessor to only do optimization once instead of when the preprocessor decides. This may lead to some problems with certain meshes but makes sure motion blur always works if the topology is constant.

**Type:** (bool)

---

_property_ `compressed_position_precision`: float

[Read-Write] Precision used for compressing vertex positions (lower = better result but less compression, higher = more lossy compression but smaller size)

**Type:** (float)

---

_property_ `compressed_texture_coordinates_number_of_bits`: int

[Read-Write] Bit-precision used for compressing texture coordinates (hight = better result but less compression, lower = more lossy compression but smaller size)

**Type:** (int32)

---

_property_ `flatten_tracks`: bool

[Read-Write] Whether or not to merge all vertex animation into one track

**Type:** (bool)

---

_property_ `motion_vectors`: AbcGeometryCacheMotionVectorsImport

[Read-Write]

**Type:** (AbcGeometryCacheMotionVectorsImport)

---

_property_ `optimize_index_buffers`: bool

[Read-Write] Optimizes index buffers for each unique frame, to allow better cache coherency on the GPU. Very costly and time-consuming process, recommended to OFF.

**Type:** (bool)

---

_property_ `store_imported_vertex_numbers`: bool

[Read-Write] Store the imported vertex numbers. This lets you know the vertex numbers inside the DCC. The values of each vertex number will range from 0 to 7 for a cube. Even if the number of positions might be 24.

**Type:** (bool)