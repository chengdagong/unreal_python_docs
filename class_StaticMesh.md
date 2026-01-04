# unreal.StaticMesh

```python
class unreal.StaticMesh(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``StreamableRenderAsset``


A StaticMesh is a piece of geometry that consists of a static set of polygons.
Static Meshes can be translated, rotated, and scaled, but they cannot have their vertices animated in any way. As such, they are more efficient
to render than other types of geometry such as USkeletalMesh, and they are often the basic building block of levels created in the engine.
see: https://docs.unrealengine.com/latest/INT/Engine/Content/Types/StaticMeshes/
see: AStaticMeshActor, UStaticMeshComponent

**C++ Source:**

- **Module**: Engine

- **File**: StaticMesh.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `allow_cpu_access` (bool): [Read-Write] If true, will keep geometry data CPU-accessible in cooked builds, rather than uploading to GPU memory and releasing it from CPU memory.
This is required if you wish to access StaticMesh geometry data on the CPU at runtime in cooked builds (e.g. to convert StaticMesh to ProceduralMeshComponent)

- `asset_import_data` (AssetImportData): [Read-Write]

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `body_setup` (BodySetup): [Read-Write]

- `complex_collision_mesh` (StaticMesh): [Read-Write]

- `customized_collision` (bool): [Read-Write]

- `distance_field_self_shadow_bias` (float): [Read-Write] Useful for reducing self shadowing from distance field methods when using world position offset to animate the mesh’s vertices.

- `generate_mesh_distance_field` (bool): [Read-Write] Whether to generate a distance field for this mesh, which can be used by DistanceField Indirect Shadows.
This is ignored if the project’s ‘Generate Mesh Distance Fields’ setting is enabled.

- `global_force_mip_levels_to_be_resident` (bool): [Read-Write] Global and serialized version of ForceMiplevelsToBeResident.

- `has_navigation_data` (bool): [Read-Write] If true, mesh will have NavCollision property with additional data for navmesh generation and usage.

Set to false for distant meshes (always outside navigation bounds) to save memory on collision data.

- `light_map_coordinate_index` (int32): [Read-Write] The light map coordinate index

- `light_map_resolution` (int32): [Read-Write] The light map resolution

- `lod_for_collision` (int32): [Read-Write] Specifies which mesh LOD to use for complex (per-poly) collision.
Sometimes it can be desirable to use a lower poly representation for collision to reduce memory usage, improve performance and behaviour.
Collision representation does not change based on distance to camera.

- `lod_group` (Name): [Read-Write]

- `mesh_paint_texture_coordinate_index` (int32): [Read-Write] The default coordinate index to use when texture color painting on this mesh.

- `mesh_paint_texture_resolution` (int32): [Read-Write] The resolution of texture color mesh paint textures on this mesh.
The final size will be rounded up to a power of 2 and a multiple of the “Mesh Paint Tile Size” project setting.
A default value of 0 will auto calculate the size using the “Mesh paint texels per vertex” project setting.

- `nanite_settings` (MeshNaniteSettings): [Read-Write]

- `nav_collision` (NavCollisionBase): [Read-Only]

- `negative_bounds_extension` (Vector): [Read-Write]

- `never_stream` (bool): [Read-Write]

- `num_cinematic_mip_levels` (int32): [Read-Write] Number of mip-levels to use for cinematic quality.

- `positive_bounds_extension` (Vector): [Read-Write]

- `ray_tracing_proxy_settings` (MeshRayTracingProxySettings): [Read-Write]

- `static_materials` (Array[StaticMaterial]): [Read-Write]

- `static_mesh_paint_support` (StaticMeshPaintSupport): [Read-Write] Whether to support per instance texture color mesh painting on components using this mesh.

- `support_gpu_uniformly_distributed_sampling` (bool): [Read-Write] If true, a GPU buffer containing required data for uniform mesh surface sampling will be created at load time.
It is created from the cpu data so bSupportUniformlyDistributedSampling is also required to be true.

- `support_physical_material_masks` (bool): [Read-Write] If true, complex collision data will store UVs and face remap table for use when performing
PhysicalMaterialMask lookups in cooked builds. Note the increased memory cost for this
functionality.

- `support_ray_tracing` (bool): [Read-Write] If true, a ray tracing acceleration structure will be built for this mesh and it may be used in ray tracing effects

- `support_uniformly_distributed_sampling` (bool): [Read-Write] Mesh supports uniformly distributed sampling in constant time.
Memory cost is 8 bytes per triangle.
Example usage is uniform spawning of particles.

- `thumbnail_info` (ThumbnailInfo): [Read-Only]

- `use_legacy_tangent_scaling` (bool): [Read-Write]



---

**add_asset_user_data_of_class**( _user_data_class_) → `bool`

Creates and adds an instance of the provided AssetUserData class to the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to create

Returns:

Whether or not an instance of InUserDataClass was succesfully added

Return type:

bool


---

**add_material**( _material_) → `Name`

Adds a new material and return its slot name

Parameters:

**material** ( _MaterialInterface_)

Return type:

Name


---

**add_socket**( _socket_) → `None`

Add a socket object in this StaticMesh.

Parameters:

**socket** ( _StaticMeshSocket_)


---

**build_from_static_mesh_descriptions**( _static_mesh_descriptions_, _build_simple_collision=False_, _fast_build=True_) → `None`

Builds static mesh LODs from the array of StaticMeshDescriptions passed in

Parameters:

- **static\_mesh\_descriptions** ( _Array_ _\_ [_StaticMeshDescription_ _]_)

- **build\_simple\_collision** ( _bool_)

- **fast\_build** ( _bool_)



---

_classmethod_ create_static_mesh_description( _outer=None_)→StaticMeshDescription

Create an empty StaticMeshDescription object, to describe a static mesh at runtime

Parameters:

**outer** ( _Object_)

Return type:

StaticMeshDescription


---

**find_socket**( _socket_name_) → `StaticMeshSocket`

Find a socket object in this StaticMesh by name.
Entering NAME\_None will return NULL. If there are multiple sockets with the same name, will return the first one.

Parameters:

**socket\_name** ( _Name_)

Return type:

StaticMeshSocket


---

**get_asset_user_data_of_class**( _user_data_class_) → `AssetUserData`

Returns an instance of the provided AssetUserData class if it’s contained in the target asset.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to get

Returns:

The instance of the UAssetUserData class contained, or null if it doesn’t exist

Return type:

AssetUserData


---

**get_bounding_box**() → `Box`

Returns the bounding box, in local space including bounds extension(s), of the StaticMesh asset

Return type:

Box


---

**get_bounds**() → `BoxSphereBounds`

Returns the number of bounds of the mesh.

Returns:

The bounding box represented as box origin with extents and also a sphere that encapsulates that box

Return type:

BoxSphereBounds


---

**get_material**( _material_index_) → `MaterialInterface`

Gets a Material given a Material Index and an LOD number

Parameters:

**material\_index** ( _int32_)

Returns:

Requested material

Return type:

MaterialInterface


---

**get_material_index**( _material_slot_name_) → `int32`

Gets a Material index given a slot name

Parameters:

**material\_slot\_name** ( _Name_)

Returns:

Requested material

Return type:

int32

get\_min\_lod\_for\_quality\_levels( _)->(quality\_level\_minimum\_lo\_ds=Map[PerQualityLevels,int32],default=int32_)

Get Min LODFor Quality Levels

Returns:

quality\_level\_minimum\_lo\_ds (Map[PerQualityLevels, int32]):

default (int32):

Return type:

tuple


---

**get_minimum_lod_for_platform**( _platform_name_) → `int32`

Get Minimum LODFor Platform

Parameters:

**platform\_name** ( _Name_)

Return type:

int32


---

**get_minimum_lod_for_platforms**() → `Map\ [Name,int32]`

Get Minimum LODFor Platforms

Returns:

platform\_minimum\_lo\_ds (Map[Name, int32]):

Return type:

Map\ [Name, int32]


---

**get_minimum_lod_for_quality_level**( _quality_level_) → `int32`

Get Minimum LODFor Quality Level

Parameters:

**quality\_level** ( _Name_)

Return type:

int32


---

**get_minimum_lod_for_quality_levels**() → `Map\ [Name,int32]`

Get Minimum LODFor Quality Levels

Returns:

quality\_level\_minimum\_lo\_ds (Map[Name, int32]):

Return type:

Map\ [Name, int32]


---

**get_num_lods**() → `int32`

Returns the number of LODs used by the mesh.

Return type:

int32


---

**get_num_sections**( _lod_) → `int32`

Returns number of Sections that this StaticMesh has, in the supplied LOD (LOD 0 is the highest)

Parameters:

**lod** ( _int32_)

Return type:

int32


---

**get_num_triangles**( _lod_index_) → `int32`

Returns the number of triangles in the render data for the specified LOD.

Parameters:

**lod\_index** ( _int32_)

Return type:

int32


---

**get_num_vertices**( _lod_index_) → `int32`

Returns the number of vertices for the specified LOD.

Parameters:

**lod\_index** ( _int32_)

Return type:

int32


---

**get_sockets_by_tag**( _socket_tag_) → `Array\ [StaticMeshSocket]`

Returns a list of sockets with the provided tag.

Parameters:

**socket\_tag** ( _str_)

Return type:

Array\ [StaticMeshSocket]


---

**get_static_mesh_description**( _lod_index_) → `StaticMeshDescription`

Return a new StaticMeshDescription referencing the MeshDescription of the given LOD

Parameters:

**lod\_index** ( _int32_)

Return type:

StaticMeshDescription


---

**has_asset_user_data_of_class**( _user_data_class_) → `bool`

Checks whether or not an instance of the provided AssetUserData class is contained.

Parameters:

**user\_data\_class** ( _type_ _(_ _Class_ _)_) – UAssetUserData sub class to check for

Returns:

Whether or not an instance of InUserDataClass was found

Return type:

bool


---

**is_lod_screen_size_auto_computed**() → `bool`

Is LODScreen Size Auto Computed

Return type:

bool


---

_property_ `lod_for_collision`: int

[Read-Write] Specifies which mesh LOD to use for complex (per-poly) collision.
Sometimes it can be desirable to use a lower poly representation for collision to reduce memory usage, improve performance and behaviour.
Collision representation does not change based on distance to camera.

**Type:**

(int32)


---

**remove_socket**( _socket_) → `None`

Remove a socket object in this StaticMesh by providing it’s pointer. Use FindSocket() if needed.

Parameters:

**socket** ( _StaticMeshSocket_)


---

**set_material**( _material_index_, _new_material_) → `None`

Sets a Material given a Material Index

Parameters:

- **material\_index** ( _int32_)

- **new\_material** ( _MaterialInterface_)



---

**set_min_lod_for_quality_levels**( _quality_level_minimum_lo_ds_, _default=-1_) → `None`

Allow to override min lod quality levels on a staticMesh and it Default value (-1 value for Default dont override its value).

Parameters:

- **quality\_level\_minimum\_lo\_ds** ( _Map_ _\_ [_PerQualityLevels_ _,_ _int32_ _]_)

- **default** ( _int32_)



---

**set_minimum_lod_for_platform**( _platform_name_, _min_lod_) → `None`

Set Minimum LODFor Platform

Parameters:

- **platform\_name** ( _Name_)

- **min\_lod** ( _int32_)



---

**set_minimum_lod_for_platforms**( _platform_minimum_lo_ds_) → `None`

Set Minimum LODFor Platforms

Parameters:

**platform\_minimum\_lo\_ds** ( _Map_ _\_ [_Name_ _,_ _int32_ _]_)


---

**set_num_source_models**( _num_) → `None`

Set Num Source Models

Parameters:

**num** ( _int32_)


---

_property_ `static_materials`: None

[Read-Write]

**Type:**

( Array\ [StaticMaterial])


---

_property_ `static_mesh_paint_support`: StaticMeshPaintSupport

[Read-Write] Whether to support per instance texture color mesh painting on components using this mesh.

**Type:**

( StaticMeshPaintSupport)

### Table of Contents

- `unreal.StaticMesh`
  - `StaticMesh`
    - `StaticMesh.add_asset_user_data_of_class()`
    - `StaticMesh.add_material()`
    - `StaticMesh.add_socket()`
    - `StaticMesh.build_from_static_mesh_descriptions()`
    - `StaticMesh.create_static_mesh_description()`
    - `StaticMesh.find_socket()`
    - `StaticMesh.get_asset_user_data_of_class()`
    - `StaticMesh.get_bounding_box()`
    - `StaticMesh.get_bounds()`
    - `StaticMesh.get_material()`
    - `StaticMesh.get_material_index()`
    - `StaticMesh.get_min_lod_for_quality_levels()`
    - `StaticMesh.get_minimum_lod_for_platform()`
    - `StaticMesh.get_minimum_lod_for_platforms()`
    - `StaticMesh.get_minimum_lod_for_quality_level()`
    - `StaticMesh.get_minimum_lod_for_quality_levels()`
    - `StaticMesh.get_num_lods()`
    - `StaticMesh.get_num_sections()`
    - `StaticMesh.get_num_triangles()`
    - `StaticMesh.get_num_vertices()`
    - `StaticMesh.get_sockets_by_tag()`
    - `StaticMesh.get_static_mesh_description()`
    - `StaticMesh.has_asset_user_data_of_class()`
    - `StaticMesh.is_lod_screen_size_auto_computed()`
    - `StaticMesh.lod_for_collision`
    - `StaticMesh.remove_socket()`
    - `StaticMesh.set_material()`
    - `StaticMesh.set_min_lod_for_quality_levels()`
    - `StaticMesh.set_minimum_lod_for_platform()`
    - `StaticMesh.set_minimum_lod_for_platforms()`
    - `StaticMesh.set_num_source_models()`
    - `StaticMesh.static_materials`
    - `StaticMesh.static_mesh_paint_support`