# unreal.GeometryScript_MeshQueries

```python
class unreal.GeometryScript_MeshQueries(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Geometry Script Library Mesh Query Functions

**C++ Source:**

- **Plugin**: GeometryScripting

- **Module**: GeometryScriptingCore

- **File**: MeshQueryFunctions.h


_classmethod_ compute\_triangle\_barycentric\_coords( _target\_mesh_, _triangle\_id_, _point)->(DynamicMesh_, _is\_valid\_triangle=bool_, _vertex1=Vector_, _vertex2=Vector_, _vertex3=Vector_, _barycentric\_coords=Vector_)

Compute the barycentric coordinates (A,B,C) of the Point relative to the specified TriangleID of the TargetMesh.
The properties of barycentric coordinates are such that A,B,C are all positive, A+B+C=1.0, and A\*Vertex1 + B\*Vertex2 + C\*Vertex3 = Point.
So, the barycentric coordinates can be used to smoothly interpolate/blend any other per-triangle-vertex quantities.
The Point must lie in the plane of the Triangle, otherwise the coordinates are somewhat meaningless (but clamped to 0-1 range to avoid catastrophic errors)
The Positions of the Triangle Vertices are also returned for convenience (similar to GetTrianglePositions)

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)

- **point** ( _Vector_)


Returns:

is\_valid\_triangle (bool): will be returned true if TriangleID exists in TargetMesh, and otherwise will be returned false

vertex1 (Vector):

vertex2 (Vector):

vertex3 (Vector):

barycentric\_coords (Vector):

Return type:

tuple

_classmethod_ get\_all\_split\_u\_vs\_at\_vertex( _target\_mesh,uv\_set\_index,vertex\_id)->(DynamicMesh,element\_i\_ds=Array[int32],element\_u\_vs=Array[Vector2D],have\_valid\_u\_vs=bool_)

Returns the unique UV element IDs and values associated with the mesh vertex, in the specified UV Channel.
If the Vertex or UV channel does not exist, the arrays will be empty and bHaveValidUVs will be set to false.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **uv\_set\_index** ( _int32_)

- **vertex\_id** ( _int32_)


Returns:

element\_i\_ds (Array[int32]):

element\_u\_vs (Array[Vector2D]):

have\_valid\_u\_vs (bool):

Return type:

tuple

_classmethod_ get\_all\_triangle\_i\_ds( _target\_mesh)->(DynamicMesh_, _triangle\_id\_list=GeometryScriptIndexList_, _has\_triangle\_id\_gaps=bool_)

Returns an Index List of all Triangle IDs in a mesh.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Returns:

triangle\_id\_list (GeometryScriptIndexList):

has\_triangle\_id\_gaps (bool): will be true on return if there are breaks in the sequential numeration of Triangle IDs, as would happen after deleting triangles.

Return type:

tuple

_classmethod_ get\_all\_triangle\_indices( _target\_mesh_, _skip\_gaps)->(DynamicMesh_, _triangle\_list=GeometryScriptTriangleList_, _has\_triangle\_id\_gaps=bool_)

- Returns a TriangleList of all Triangle Vertex ID triplets in a mesh.


Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **skip\_gaps** ( _bool_) – if false there will be a one-to-one correspondence between Triangle ID and entries in the triangle list and invalid triplets of (-1,-1,-1) will correspond to Triangle IDs not found in the Target Mesh. \*


Returns:

triangle\_list (GeometryScriptTriangleList):

has\_triangle\_id\_gaps (bool): will be false on return if the mesh had no gaps in Triangle IDs or if bSkipGaps was set to true.

Return type:

tuple

_classmethod_ get\_all\_uv\_seam\_edges( _target\_mesh_, _uv\_set\_index)->(DynamicMesh_, _have\_valid\_u\_vs=bool_, _element\_i\_ds=GeometryScriptIndexList_)

Returns all edge element IDs that are UV seam edges for a given UV channel.

Parameters:

- **target\_mesh** ( _DynamicMesh_) – The mesh to query.

- **uv\_set\_index** ( _int32_) – The UV channel to query


Returns:

The target mesh that was queried.

have\_valid\_u\_vs (bool): True, if the mesh has UVs for the given UVSetIndex.

element\_i\_ds (GeometryScriptIndexList): The returned edge element IDs

Return type:

tuple

_classmethod_ get\_all\_vertex\_i\_ds( _target\_mesh)->(DynamicMesh_, _vertex\_id\_list=GeometryScriptIndexList_, _has\_vertex\_id\_gaps=bool_)

Returns an IndexList of all Vertex IDs in mesh.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Returns:

vertex\_id\_list (GeometryScriptIndexList):

has\_vertex\_id\_gaps (bool):

Return type:

tuple

_classmethod_ get\_all\_vertex\_positions( _target\_mesh_, _skip\_gaps)->(DynamicMesh_, _position\_list=GeometryScriptVectorList_, _has\_vertex\_id\_gaps=bool_)

Returns a Vector List of all the mesh vertex 3D positions (possibly large!).

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **skip\_gaps** ( _bool_) – if false there will be a one-to-one correspondence between Vertex ID and entries in the Position List where a zero vector (0,0,0) will correspond to Vertex IDs not found in the Target Mesh.


Returns:

position\_list (GeometryScriptVectorList):

has\_vertex\_id\_gaps (bool): will be false if the mesh had no gaps in Vertex IDs or if bSkipGaps was set to true.

Return type:

tuple

_classmethod_ get\_all\_vertex\_positions\_at\_edges( _target\_mesh_, _edge\_i\_ds)->(DynamicMesh_, _start=GeometryScriptVectorList_, _end=GeometryScriptVectorList_)

Returns the vertex positions for each edge in the given index list.

Parameters:

- **target\_mesh** ( _DynamicMesh_) – The mesh to query

- **edge\_i\_ds** ( _GeometryScriptIndexList_) – The edge IDs to query


Returns:

The target mesh that was queried

start (GeometryScriptVectorList): The output list of start vertex positions

end (GeometryScriptVectorList): The output list of end vertex positions

Return type:

tuple


---

_classmethod_ get_has_material_i_ds( _target_mesh_)→bool

Returns true if the mesh has Material IDs available/enabled.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

bool


---

_classmethod_ get_has_polygroups( _target_mesh_)→bool

Returns true if the mesh has a standard PolyGroup Layer.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

bool


---

_classmethod_ get_has_triangle_id_gaps( _target_mesh_)→bool

Returns true if there are gaps in the Triangle ID list, such that Get Num Triangle IDs is greater than Get Triangle Count.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

bool


---

_classmethod_ get_has_triangle_normals( _target_mesh_)→boolParameters:

**target\_mesh** ( _DynamicMesh_)

Returns:

true if the TargetMesh has the Normals Attribute enabled (which allows for storing split normals)

Return type:

bool


---

_classmethod_ get_has_vertex_colors( _target_mesh_)→boolParameters:

**target\_mesh** ( _DynamicMesh_)

Returns:

true if the TargetMesh has the Vertex Colors attribute enabled

Return type:

bool


---

_classmethod_ get_has_vertex_id_gaps( _target_mesh_)→bool

Returns true if there are gaps in the Vertex ID list. For example, Get Number of Vertex IDs is greater than Get Vertex Count.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

bool

_classmethod_ get\_interpolated\_triangle\_normal( _target\_mesh_, _triangle\_id_, _barycentric\_coords)->(DynamicMesh_, _tri\_has\_valid\_normals=bool_, _interpolated\_normal=Vector_)

Compute the interpolated Normal (A\*Normal1 + B\*Normal2 + C\*Normal3), where (A,B,C)=BarycentricCoords and the Normals are taken
from the specified TriangleID in the Normal layer of the TargetMesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)

- **barycentric\_coords** ( _Vector_)


Returns:

tri\_has\_valid\_normals (bool): will be returned true if TriangleID exists in TargetMesh and has Normals set, and otherwise will be returned false.

interpolated\_normal (Vector):

Return type:

tuple

_classmethod_ get\_interpolated\_triangle\_normal\_tangents( _target\_mesh_, _triangle\_id_, _barycentric\_coords)->(DynamicMesh_, _tri\_has\_valid\_elements=bool_, _interpolated\_normal=Vector_, _interpolated\_tangent=Vector_, _interpolated\_bi\_tangent=Vector_)

Compute the interpolated Normal and Tangents for the specified specified TriangleID in the Normal and Tangent attributes of the TargetMesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)

- **barycentric\_coords** ( _Vector_)


Returns:

tri\_has\_valid\_elements (bool): will be returned true if TriangleID exists in TargetMesh and has Normals and Tangents set, and otherwise will be returned false

interpolated\_normal (Vector):

interpolated\_tangent (Vector):

interpolated\_bi\_tangent (Vector):

Return type:

tuple

_classmethod_ get\_interpolated\_triangle\_position( _target\_mesh_, _triangle\_id_, _barycentric\_coords)->(DynamicMesh_, _is\_valid\_triangle=bool_, _interpolated\_position=Vector_)

Compute the interpolated Position (A\*Vertex1 + B\*Vertex2 + C\*Vertex3), where (A,B,C)=BarycentricCoords and the Vertex positions are taken
from the specified TriangleID of the TargetMesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)

- **barycentric\_coords** ( _Vector_)


Returns:

is\_valid\_triangle (bool): will be returned true if TriangleID exists in TargetMesh, and otherwise will be returned false

interpolated\_position (Vector):

Return type:

tuple

_classmethod_ get\_interpolated\_triangle\_uv( _target\_mesh_, _uv\_set\_index_, _triangle\_id_, _barycentric\_coords)->(DynamicMesh_, _tri\_has\_valid\_u\_vs=bool_, _interpolated\_uv=Vector2D_)

Compute the interpolated UV (A\*UV1+ B\*UV2+ C\*UV3), where (A,B,C)=BarycentricCoords and the UV positions are taken
from the specified TriangleID in the specified UVSet of the TargetMesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **uv\_set\_index** ( _int32_)

- **triangle\_id** ( _int32_)

- **barycentric\_coords** ( _Vector_)


Returns:

tri\_has\_valid\_u\_vs (bool):

interpolated\_uv (Vector2D):

Return type:

tuple

_classmethod_ get\_interpolated\_triangle\_vertex\_color( _target\_mesh_, _triangle\_id_, _barycentric\_coords_, _default\_color)->(DynamicMesh_, _tri\_has\_valid\_vertex\_colors=bool_, _interpolated\_color=LinearColor_)

Compute the interpolated Vertex Color (A\*Color1 + B\*Color2 + C\*Color3), where (A,B,C)=BarycentricCoords and the Colors are taken
from the specified TriangleID in the Vertex Color layer of the TargetMesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)

- **barycentric\_coords** ( _Vector_)

- **default\_color** ( _LinearColor_)


Returns:

tri\_has\_valid\_vertex\_colors (bool): will be returned true if TriangleID exists in TargetMesh and has Colors set, and otherwise will be returned false

interpolated\_color (LinearColor):

Return type:

tuple


---

_classmethod_ get_is_closed_mesh( _target_mesh_)→bool

Returns true if the mesh is closed, such as no topological boundary edges.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

bool


---

_classmethod_ get_is_dense_mesh( _target_mesh_)→bool

Returns true if the mesh is dense. For example, no gaps in Vertex IDs or Triangle IDs.
Note if a mesh is not dense, the Compact Mesh node can be used to removed the gaps.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

bool


---

_classmethod_ get_mesh_bounding_box( _target_mesh_)→Box

Computes the bounding box of the mesh vertices in the local space of the mesh.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

Box


---

_classmethod_ get_mesh_has_attribute_set( _target_mesh_)→bool

Returns true if the Target Mesh has attributes enabled.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

bool


---

_classmethod_ get_mesh_info_string( _target_mesh_)→str

Returns information about the Target Mesh, such as the vertex and triangle count as well as some attribute information.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

str

_classmethod_ get\_mesh\_uv\_area( _target\_mesh_, _uv\_channel)->(double_, _is\_valid\_uv\_channel=bool_)

Gets the area of triangles in UV space for the given UV Channel.

Parameters:

- **target\_mesh** ( _DynamicMesh_) – The mesh to query.

- **uv\_channel** ( _int32_) – The UV channel to query


Returns:

The number of UV islands

is\_valid\_uv\_channel (bool): True, if the mesh has UVs for the given UVSetIndex.

Return type:

bool

_classmethod_ get\_mesh\_volume\_area( _target\_mesh)->(surface\_area=float_, _volume=float_)

Computes the volume and area of the mesh.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Returns:

surface\_area (float):

volume (float):

Return type:

tuple

_classmethod_ get\_mesh\_volume\_area\_center( _target\_mesh)->(surface\_area=float_, _volume=float_, _center\_of\_mass=Vector_)

Computes the volume, area and center-of-mass of the mesh.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Returns:

surface\_area (float):

volume (float):

center\_of\_mass (Vector):

Return type:

tuple


---

_classmethod_ get_num_connected_components( _target_mesh_)→int32

Returns the number of separate connected islands (components) in the mesh, such as “triangle patches” internally connected by shared edges.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

int32


---

_classmethod_ get_num_extended_polygroup_layers( _target_mesh_)→int32

Returns the count of extended PolyGroup Layers.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

int32


---

_classmethod_ get_num_open_border_edges( _target_mesh_)→int32

Returns the number of topological boundary edges in the mesh, i.e counts edges that only have one adjacent triangle.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

int32

_classmethod_ get\_num\_open\_border\_loops( _target\_mesh)->(int32_, _ambiguous\_topology\_found=bool_)

Returns the number of open border loops, such as “holes” in the mesh.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Returns:

ambiguous\_topology\_found (bool):

Return type:

bool


---

_classmethod_ get_num_triangle_i_ds( _target_mesh_)→int32

Gets the number of Triangle IDs in the mesh. This may be larger than the Triangle Count if the mesh is not dense, even after deleting triangles.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

int32

_classmethod_ get\_num\_uv\_islands( _target\_mesh_, _uv\_channel)->(int32_, _is\_valid\_uv\_channel=bool_)

Returns the number of UV islands in a given UV channel.

Parameters:

- **target\_mesh** ( _DynamicMesh_) – The mesh to query.

- **uv\_channel** ( _int32_) – The UV channel to query


Returns:

The number of UV islands

is\_valid\_uv\_channel (bool): True, if the mesh has UVs for the given UVSetIndex.

Return type:

bool


---

_classmethod_ get_num_uv_sets( _target_mesh_)→int32

Gets the number of UV Channels on the Target Mesh.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

int32


---

_classmethod_ get_num_vertex_i_ds( _target_mesh_)→int32

Gets the number of Vertex IDs in the mesh, which may be larger than the Vertex Count, if the mesh is not dense (e.g. after deleting vertices).

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

int32

_classmethod_ get\_triangle\_face\_normal( _target\_mesh_, _triangle\_id)->(Vector_, _is\_valid\_triangle=bool_)

Get Triangle Face Normal

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)


Returns:

is\_valid\_triangle (bool):

Return type:

bool

_classmethod_ get\_triangle\_indices( _target\_mesh_, _triangle\_id)->(IntVector_, _is\_valid\_triangle=bool_)

Returns the Vertex ID triplet for the specified Triangle.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_) – indicates the triangle to query on the Target Mesh.


Returns:

is\_valid\_triangle (bool): will be false on return if the Triangle ID does not exist in the Target Mesh, in that case the returned vertex triplet will be (-1, -1, -1).

Return type:

bool

_classmethod_ get\_triangle\_normal\_tangents( _target\_mesh_, _triangle\_id)->(DynamicMesh_, _tri\_has\_valid\_elements=bool_, _normals=GeometryScriptTriangle_, _tangents=GeometryScriptTriangle_, _bi\_tangents=GeometryScriptTriangle_)

For the specified Triangle ID of the TargetMesh, get the Normal and Tangent vectors at each vertex of the Triangle.
These Normals/Tangents will be taken from the Normal and Tangents Overlays, i.e. they will potentially be split-normals.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)


Returns:

tri\_has\_valid\_elements (bool): will be returned true if TriangleID exists in TargetMesh and has Normals and Tangents set.

normals (GeometryScriptTriangle):

tangents (GeometryScriptTriangle):

bi\_tangents (GeometryScriptTriangle):

Return type:

tuple

_classmethod_ get\_triangle\_normals( _target\_mesh_, _triangle\_id)->(DynamicMesh_, _normal1=Vector_, _normal2=Vector_, _normal3=Vector_, _tri\_has\_valid\_normals=bool_)

For the specified TriangleID of the Target Mesh, get the Normal vectors at each vertex of the Triangle.
These Normals will be taken from the Normal Overlay, i.e. they will potentially be split-normals.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)


Returns:

normal1 (Vector):

normal2 (Vector):

normal3 (Vector):

tri\_has\_valid\_normals (bool): will be returned true if TriangleID exists in TargetMesh and has Normals set.

Return type:

tuple

_classmethod_ get\_triangle\_positions( _target\_mesh_, _triangle\_id)->(is\_valid\_triangle=bool_, _vertex1=Vector_, _vertex2=Vector_, _vertex3=Vector_)

- Returns the 3D positions (in the mesh local space) of the three vertices of the requested triangle.

- If the Triangle ID is not an element of the Target Mesh, all three vertices will be returned as (0, 0, 0) and bIsValidTriangle will be set to false.


Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)


Returns:

is\_valid\_triangle (bool):

vertex1 (Vector):

vertex2 (Vector):

vertex3 (Vector):

Return type:

tuple

_classmethod_ get\_triangle\_u\_vs( _target\_mesh_, _uv\_set\_index_, _triangle\_id)->(uv1=Vector2D_, _uv2=Vector2D_, _uv3=Vector2D_, _have\_valid\_u\_vs=bool_)

Returns the UV values associated with the three vertices of the triangle in the specified UV Channel.
If the Triangle does not exist in the mesh or if no UVs are set in the specified UV Channel for the triangle, the resulting values will be (0,0) and bHaveValidUVs will be set to false.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **uv\_set\_index** ( _int32_)

- **triangle\_id** ( _int32_)


Returns:

uv1 (Vector2D):

uv2 (Vector2D):

uv3 (Vector2D):

have\_valid\_u\_vs (bool):

Return type:

tuple

_classmethod_ get\_triangle\_vertex\_colors( _target\_mesh_, _triangle\_id)->(DynamicMesh_, _color1=LinearColor_, _color2=LinearColor_, _color3=LinearColor_, _tri\_has\_valid\_vertex\_colors=bool_)

For the specified TriangleID of the TargetMesh, get the Vertex Colors at each vertex of the Triangle.
These Colors will be taken from the Vertex Color Attribute, ie they will potentially be split-colors.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)


Returns:

color1 (LinearColor):

color2 (LinearColor):

color3 (LinearColor):

tri\_has\_valid\_vertex\_colors (bool): will be returned true if TriangleID exists in TargetMesh and has Vertex Colors set

Return type:

tuple

_classmethod_ get\_uv\_set\_bounding\_box( _target\_mesh_, _uv\_set\_index)->(Box2D_, _is\_valid\_uv\_set=bool_, _uv\_set\_is\_empty=bool_)

Gets the 2D bounding box of all UVs in the UV Channel. If the UV Channel does not exist, or if the UV Channel is empty, the resulting box will be invalid.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **uv\_set\_index** ( _int32_)


Returns:

is\_valid\_uv\_set (bool):

uv\_set\_is\_empty (bool):

Return type:

tuple

_classmethod_ get\_vertex\_connected\_triangles( _target\_mesh,vertex\_id)->(DynamicMesh,triangles=Array[int32]_)

Return array of Triangle IDs connected to the given VertexID, ie the triangle one-ring

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **vertex\_id** ( _int32_)


Returns:

triangles (Array[int32]):

Return type:

Array[int32]

_classmethod_ get\_vertex\_connected\_vertices( _target\_mesh,vertex\_id)->(DynamicMesh,vertices=Array[int32]_)

Return array of Vertex IDs connected via a mesh edge to the given VertexID, ie the vertex one-ring

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **vertex\_id** ( _int32_)


Returns:

vertices (Array[int32]):

Return type:

Array[int32]


---

_classmethod_ get_vertex_count( _target_mesh_)→int32

Gets the number of vertices in the mesh. Note this may be less than the number of Vertex IDs used as some vertices may have been deleted.

Parameters:

**target\_mesh** ( _DynamicMesh_)

Return type:

int32

_classmethod_ get\_vertex\_position( _target\_mesh_, _vertex\_id)->(Vector_, _is\_valid\_vertex=bool_)

Gets the 3D position of a mesh vertex in the mesh local space, by Vertex ID.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **vertex\_id** ( _int32_)


Returns:

is\_valid\_vertex (bool):

Return type:

bool


---

_classmethod_ is_valid_triangle_id( _target_mesh_, _triangle_id_)→bool

Returns true if Triangle ID refers to a valid Triangle in the Target Mesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **triangle\_id** ( _int32_)


Return type:

bool


---

_classmethod_ is_valid_vertex_id( _target_mesh_, _vertex_id_)→bool

Returns true if Vertex ID refers to a valid vertex in the Target Mesh.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **vertex\_id** ( _int32_)


Return type:

bool

### Table of Contents

- `unreal.GeometryScript_MeshQueries`
  - `GeometryScript_MeshQueries`
    - `GeometryScript_MeshQueries.compute_triangle_barycentric_coords()`
    - `GeometryScript_MeshQueries.get_all_split_u_vs_at_vertex()`
    - `GeometryScript_MeshQueries.get_all_triangle_i_ds()`
    - `GeometryScript_MeshQueries.get_all_triangle_indices()`
    - `GeometryScript_MeshQueries.get_all_uv_seam_edges()`
    - `GeometryScript_MeshQueries.get_all_vertex_i_ds()`
    - `GeometryScript_MeshQueries.get_all_vertex_positions()`
    - `GeometryScript_MeshQueries.get_all_vertex_positions_at_edges()`
    - `GeometryScript_MeshQueries.get_has_material_i_ds()`
    - `GeometryScript_MeshQueries.get_has_polygroups()`
    - `GeometryScript_MeshQueries.get_has_triangle_id_gaps()`
    - `GeometryScript_MeshQueries.get_has_triangle_normals()`
    - `GeometryScript_MeshQueries.get_has_vertex_colors()`
    - `GeometryScript_MeshQueries.get_has_vertex_id_gaps()`
    - `GeometryScript_MeshQueries.get_interpolated_triangle_normal()`
    - `GeometryScript_MeshQueries.get_interpolated_triangle_normal_tangents()`
    - `GeometryScript_MeshQueries.get_interpolated_triangle_position()`
    - `GeometryScript_MeshQueries.get_interpolated_triangle_uv()`
    - `GeometryScript_MeshQueries.get_interpolated_triangle_vertex_color()`
    - `GeometryScript_MeshQueries.get_is_closed_mesh()`
    - `GeometryScript_MeshQueries.get_is_dense_mesh()`
    - `GeometryScript_MeshQueries.get_mesh_bounding_box()`
    - `GeometryScript_MeshQueries.get_mesh_has_attribute_set()`
    - `GeometryScript_MeshQueries.get_mesh_info_string()`
    - `GeometryScript_MeshQueries.get_mesh_uv_area()`
    - `GeometryScript_MeshQueries.get_mesh_volume_area()`
    - `GeometryScript_MeshQueries.get_mesh_volume_area_center()`
    - `GeometryScript_MeshQueries.get_num_connected_components()`
    - `GeometryScript_MeshQueries.get_num_extended_polygroup_layers()`
    - `GeometryScript_MeshQueries.get_num_open_border_edges()`
    - `GeometryScript_MeshQueries.get_num_open_border_loops()`
    - `GeometryScript_MeshQueries.get_num_triangle_i_ds()`
    - `GeometryScript_MeshQueries.get_num_uv_islands()`
    - `GeometryScript_MeshQueries.get_num_uv_sets()`
    - `GeometryScript_MeshQueries.get_num_vertex_i_ds()`
    - `GeometryScript_MeshQueries.get_triangle_face_normal()`
    - `GeometryScript_MeshQueries.get_triangle_indices()`
    - `GeometryScript_MeshQueries.get_triangle_normal_tangents()`
    - `GeometryScript_MeshQueries.get_triangle_normals()`
    - `GeometryScript_MeshQueries.get_triangle_positions()`
    - `GeometryScript_MeshQueries.get_triangle_u_vs()`
    - `GeometryScript_MeshQueries.get_triangle_vertex_colors()`
    - `GeometryScript_MeshQueries.get_uv_set_bounding_box()`
    - `GeometryScript_MeshQueries.get_vertex_connected_triangles()`
    - `GeometryScript_MeshQueries.get_vertex_connected_vertices()`
    - `GeometryScript_MeshQueries.get_vertex_count()`
    - `GeometryScript_MeshQueries.get_vertex_position()`
    - `GeometryScript_MeshQueries.is_valid_triangle_id()`
    - `GeometryScript_MeshQueries.is_valid_vertex_id()`