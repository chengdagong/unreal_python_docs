# unreal.GeometryScript_MeshModeling

```python
class unreal.GeometryScript_MeshModeling(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Geometry Script Library Mesh Modeling Functions

**C++ Source:**

- **Plugin**: GeometryScripting

- **Module**: GeometryScriptingCore

- **File**: MeshModelingFunctions.h



---

_classmethod_ apply_mesh_bevel_edge_selection( _target_mesh_, _selection_, _bevel_options_, _debug=None_)→DynamicMesh

Apply a Mesh Bevel operation to parts of TargetMesh using the BevelOptions settings.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **selection** ( _GeometryScriptMeshSelection_) – specifies which mesh edges to Bevel

- **bevel\_options** ( _GeometryScriptMeshBevelSelectionOptions_) – settings for the Bevel Operation

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_bevel_selection( _target_mesh_, _selection_, _bevel_mode_, _bevel_options_, _debug=None_)→DynamicMesh

Apply a Mesh Bevel operation to parts of TargetMesh using the BevelOptions settings, with additional options to handle region selections

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **selection** ( _GeometryScriptMeshSelection_) – specifies which mesh edges to Bevel

- **bevel\_mode** ( _GeometryScriptMeshBevelSelectionMode_) – specifies whether Selection should be optionally converted to a Triangle Region or set of PolyGroup Edges

- **bevel\_options** ( _GeometryScriptMeshBevelSelectionOptions_) – settings for the Bevel Operation

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_disconnect_faces( _target_mesh_, _selection_, _allow_bowties_in_output=True_, _debug=None_)→DynamicMesh

Disconnect the triangles of TargetMesh identified by the Selection.
The input Selection will still identify the same geometric elements after Disconnecting.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **selection** ( _GeometryScriptMeshSelection_)

- **allow\_bowties\_in\_output** ( _bool_) – if false, any bowtie vertices created by the operation will be automatically split

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_disconnect_faces_along_edges( _target_mesh_, _selection_, _debug=None_)→DynamicMesh

Disconnect triangles of TargetMesh along the edges of the Selection.
The input Selection will still identify the same geometric elements after Disconnecting.

Parameters:

- **target\_mesh** ( _DynamicMesh_) – Mesh to operate on

- **selection** ( _GeometryScriptMeshSelection_) – Which edges to operate on. Non-edge selections will be interpreted as edge selections – i.e., all selected triangles’ edges, or all selected vertices’ one-ring edges.

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh

_classmethod_ apply\_mesh\_duplicate\_faces( _target\_mesh,selection,group\_options=[GeometryScriptMeshEditPolygroupMode.PRESERVE\_EXISTING,0],debug=None)->(DynamicMesh,new\_triangles=GeometryScriptMeshSelection_)

Duplicate the triangles of TargetMesh identified by the Selection

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **selection** ( _GeometryScriptMeshSelection_)

- **group\_options** ( _GeometryScriptMeshEditPolygroupOptions_)

- **debug** ( _GeometryScriptDebug_)


Returns:

new\_triangles (GeometryScriptMeshSelection): a Mesh Selection of the duplicate triangles is returned here (with type Triangles)

Return type:

GeometryScriptMeshSelection


---

_classmethod_ apply_mesh_extrude( _target_mesh:DynamicMesh_, _options:GeometryScriptMeshExtrudeOptions_, _debug:GeometryScriptDebug=Ellipsis_)→DynamicMesh

deprecated: ‘apply\_mesh\_extrude’ was renamed to ‘apply\_mesh\_extrude\_compatibility\_5p0’.


---

_classmethod_ apply_mesh_extrude_compatibility_5p0( _target_mesh_, _options_, _debug=None_)→DynamicMesh

## Backwards-Compatibility implementations

These are versions/variants of the above functions that were released
in previous UE 5.x versions, that have since been updated.
To avoid breaking user scripts, these previous versions are currently kept and
called via redirectors registered in GeometryScriptingCoreModule.cpp.

These functions may be deprecated in future UE releases.

param target\_mesh:

type target\_mesh:

DynamicMesh

param options:

type options:

GeometryScriptMeshExtrudeOptions

param debug:

type debug:

GeometryScriptDebug

rtype:

DynamicMesh


---

_classmethod_ apply_mesh_inset_outset_faces( _target_mesh_, _options_, _selection_, _debug=None_)→DynamicMesh

Apply an Inset or Outset to the faces of TargetMesh identified by the Selection, or all faces if the Selection is empty.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshInsetOutsetFacesOptions_)

- **selection** ( _GeometryScriptMeshSelection_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_linear_extrude_faces( _target_mesh_, _options_, _selection_, _debug=None_)→DynamicMesh

Apply Linear Extrusion (ie extrusion in a single direction) to the triangles of TargetMesh identified by the Selection.
The input Selection will still identify the same geometric elements after the Extrusion

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshLinearExtrudeOptions_)

- **selection** ( _GeometryScriptMeshSelection_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_offset( _target_mesh_, _options_, _debug=None_)→DynamicMesh

Offset the vertices of TargetMesh from their initial positions based on averaged vertex normals.
This function is intended for high-res meshes, for polymodeling-style offsets, ApplyMeshOffsetFaces will produce better results.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshOffsetOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_offset_faces( _target_mesh_, _options_, _selection_, _debug=None_)→DynamicMesh

Apply an Offset to the faces of TargetMesh identified by the Selection, or all faces if the Selection is empty.
The Offset direction at each vertex can be derived from the averaged vertex normals or per-triangle normals.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshOffsetFacesOptions_)

- **selection** ( _GeometryScriptMeshSelection_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_polygroup_bevel( _target_mesh_, _options_, _debug=None_)→DynamicMesh

Apply a Mesh Bevel operation to all PolyGroup Edges.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshBevelOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh


---

_classmethod_ apply_mesh_shell( _target_mesh_, _options_, _debug=None_)→DynamicMesh

Create a thickened shell from TargetMesh by offsetting the vertex positions along averaged vertex normals, inwards or outwards.
Similar to ApplyMeshOffset but also includes the initial mesh (possibly flipped, if the offset is positive)

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshOffsetOptions_)

- **debug** ( _GeometryScriptDebug_)


Return type:

DynamicMesh

### Table of Contents

- `unreal.GeometryScript_MeshModeling`
  - `GeometryScript_MeshModeling`
    - `GeometryScript_MeshModeling.apply_mesh_bevel_edge_selection()`
    - `GeometryScript_MeshModeling.apply_mesh_bevel_selection()`
    - `GeometryScript_MeshModeling.apply_mesh_disconnect_faces()`
    - `GeometryScript_MeshModeling.apply_mesh_disconnect_faces_along_edges()`
    - `GeometryScript_MeshModeling.apply_mesh_duplicate_faces()`
    - `GeometryScript_MeshModeling.apply_mesh_extrude()`
    - `GeometryScript_MeshModeling.apply_mesh_extrude_compatibility_5p0()`
    - `GeometryScript_MeshModeling.apply_mesh_inset_outset_faces()`
    - `GeometryScript_MeshModeling.apply_mesh_linear_extrude_faces()`
    - `GeometryScript_MeshModeling.apply_mesh_offset()`
    - `GeometryScript_MeshModeling.apply_mesh_offset_faces()`
    - `GeometryScript_MeshModeling.apply_mesh_polygroup_bevel()`
    - `GeometryScript_MeshModeling.apply_mesh_shell()`