# unreal.GeometryScript_MeshRepair

```python
class unreal.GeometryScript_MeshRepair(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Geometry Script Library Mesh Repair Functions

**C++ Source:**

- **Plugin**: GeometryScripting

- **Module**: GeometryScriptingCore

- **File**: MeshRepairFunctions.h



---

_classmethod_ compact_mesh( _target_mesh_, _debug=None_)→DynamicMesh

Compacts the mesh’s vertices and triangles to remove any “holes” in the Vertex ID or Triangle ID lists.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh

_classmethod_ fill\_all\_mesh\_holes( _target\_mesh_, _fill\_options_, _debug=None)->(DynamicMesh_, _num\_filled\_holes=int32_, _num\_failed\_hole\_fills=int32_)

Tries to fill all open boundary loops (such as holes in the geometry surface) of a mesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **fill\_options** ( _GeometryScriptFillHolesOptions_) – specifies the method used to fill the holes.

- **debug** ( _GeometryScriptDebug_)


Returns:

num\_filled\_holes (int32): reports the number of holes filled by the function.

num\_failed\_hole\_fills (int32):

Return type:

tuple


---

_classmethod_ remove_hidden_triangles( _target_mesh_, _options_, _debug=None_)→DynamicMesh

Removes any triangles in the mesh that are not visible from the exterior view, under various definitions of “visible” and “outside”
as specified by the Options.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptRemoveHiddenTrianglesOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ remove_small_components( _target_mesh_, _options_, _debug=None_)→DynamicMesh

- Removes connected islands (components) of the mesh that have a volume, area, or triangle count below a threshold as specified by the Options.


Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptRemoveSmallComponentOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ remove_unused_vertices( _target_mesh_, _debug=None_)→DynamicMesh

Remove vertices that are not used by any triangles. Note: Does not update the IDs of any remaining vertices; use CompactMesh to do so.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ repair_mesh_degenerate_geometry( _target_mesh_, _options_, _debug=None_)→DynamicMesh

Removes triangles that have area or edge length below specified amounts depending on the Options requested.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptDegenerateTriangleOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ resolve_mesh_t_junctions( _target_mesh_, _resolve_options_, _debug=None_)→DynamicMesh

Attempts to resolve T-Junctions in the mesh by addition of vertices and welding.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **resolve\_options** ( _GeometryScriptResolveTJunctionOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh

_classmethod_ select\_hidden\_triangles\_from\_outside( _target\_mesh_, _options_, _ignore\_selection_, _transparent\_selection_, _debug=None)->(DynamicMesh_, _result\_selection=GeometryScriptMeshSelection_)

- Select mesh triangles hidden from outside views, with optional filtering on view directions


Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptSelectHiddenTrianglesFromOutsideOptions_)

- **ignore\_selection** ( _GeometryScriptMeshSelection_) – Optionally indicate parts of the mesh that should not be included in the ResultSelection, so do not need to be tested for occlusion \*

- **transparent\_selection** ( _GeometryScriptMeshSelection_) – Optionally indicate parts of the mesh that should not be considered occluding, e.g. transparent triangles \*

- **debug** ( _GeometryScriptDebug_)


Returns:

result\_selection (GeometryScriptMeshSelection): The fully occluded triangles of the target mesh (based on the options / transparencies, and excluding any IgnoreSelection triangles)

Return type:

GeometryScriptMeshSelection


---

_classmethod_ snap_mesh_open_boundaries( _target_mesh_, _snap_options_, _debug=None_)→DynamicMesh

Snap vertices on open edges to the closest compatible open boundary, if found within the tolerance distance
Unlike ResolveMeshTJunctions, does not introduce new vertices to the mesh

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **snap\_options** ( _GeometryScriptSnapBoundariesOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ split_mesh_bowties( _target_mesh_, _mesh_bowties=True_, _attribute_bowties=True_, _debug=None_)→DynamicMesh

Splits Bowties in the mesh and/or the attributes. A Bowtie is formed when a single vertex is connected to more than two boundary edges,
and splitting duplicates the shared vertex so each triangle will have a unique copy.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **mesh\_bowties** ( _bool_)

- **attribute\_bowties** ( _bool_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ weld_mesh_edges( _target_mesh_, _weld_options_, _debug=None_)→DynamicMesh

Welds any open boundary edges of the mesh together if possible in order to remove “cracks.”

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **weld\_options** ( _GeometryScriptWeldEdgesOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh

### Table of Contents

- `unreal.GeometryScript_MeshRepair`
  - `GeometryScript_MeshRepair`
    - `GeometryScript_MeshRepair.compact_mesh()`
    - `GeometryScript_MeshRepair.fill_all_mesh_holes()`
    - `GeometryScript_MeshRepair.remove_hidden_triangles()`
    - `GeometryScript_MeshRepair.remove_small_components()`
    - `GeometryScript_MeshRepair.remove_unused_vertices()`
    - `GeometryScript_MeshRepair.repair_mesh_degenerate_geometry()`
    - `GeometryScript_MeshRepair.resolve_mesh_t_junctions()`
    - `GeometryScript_MeshRepair.select_hidden_triangles_from_outside()`
    - `GeometryScript_MeshRepair.snap_mesh_open_boundaries()`
    - `GeometryScript_MeshRepair.split_mesh_bowties()`
    - `GeometryScript_MeshRepair.weld_mesh_edges()`