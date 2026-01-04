# unreal.SkeletalMesh

```python
class unreal.SkeletalMesh(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SkinnedAsset``


SkeletalMesh is geometry bound to a hierarchical skeleton of bones which can be animated for the purpose of deforming the mesh.
Skeletal Meshes are built up of two parts; a set of polygons composed to make up the surface of the mesh, and a hierarchical skeleton which can be used to animate the polygons.
The 3D models, rigging, and animations are created in an external modeling and animation application (3DSMax, Maya, Softimage, etc).
see: https://docs.unrealengine.com/latest/INT/Engine/Content/Types/SkeletalMeshes/

**C++ Source:**

- **Module**: Engine

- **File**: SkeletalMesh.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_import_data` (AssetImportData): [Read-Write]

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the asset

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write]

- `cloth_lod_bias_mode` (ClothLODBiasMode): [Read-Write]

- `default_animating_rig` (Object): [Read-Write]

- `default_mesh_deformer` (MeshDeformer): [Read-Write]

- `disable_below_min_lod_stripping` (PerPlatformBool): [Read-Write]

- `enable_per_poly_collision` (bool): [Read-Write]

- `forward_axis` (AxisType): [Read-Only] Axis that the skeletal mesh is facing. Default is the Y axis.
The facing axis represents the MeshDescription’s orientation and is set on import.
Therefore, if this property is modified elsewhere, the associated MeshDescription should be appropriately modified to reflect the new orientation.

- `global_force_mip_levels_to_be_resident` (bool): [Read-Write] Global and serialized version of ForceMiplevelsToBeResident.

- `lod_settings` (SkeletalMeshLODSettings): [Read-Write]

- `materials` (Array[SkeletalMaterial]): [Read-Write]

- `max_num_optional_lo_ds` (PerPlatformInt): [Read-Write]

- `max_num_streamed_lo_ds` (PerPlatformInt): [Read-Write]

- `mesh_clothing_assets` (Array[ClothingAssetBase]): [Read-Write]

- `min_lod` (PerPlatformInt): [Read-Write]

- `min_quality_level_lod` (PerQualityLevelInt): [Read-Write]

- `morph_targets` (Array[MorphTarget]): [Read-Write]

- `nanite_settings` (MeshNaniteSettings): [Read-Write] Settings related to building Nanite data.

- `negative_bounds_extension` (Vector): [Read-Write]

- `never_stream` (bool): [Read-Write]

- `node_mapping_data` (Array[NodeMappingContainer]): [Read-Write]

- `num_cinematic_mip_levels` (int32): [Read-Write] Number of mip-levels to use for cinematic quality.

- `overlay_material` (MaterialInterface): [Read-Write]

- `overlay_material_max_draw_distance` (float): [Read-Write]

- `override_lod_streaming_settings` (bool): [Read-Write]

- `physics_asset` (PhysicsAsset): [Read-Write]

- `positive_bounds_extension` (Vector): [Read-Write]

- `post_process_anim_blueprint` (type(Class)): [Read-Write]

- `post_process_anim_bplod_threshold` (int32): [Read-Write] \* Max LOD level that post-process anim graphs are evaluated.
\\* For example if you have the threshold set to 2, it will evaluate until including LOD 2 (based on 0 index). In case the LOD level gets set to 3, it will stop evaluating the post-process anim graph.
\\* Setting it to -1 will always evaluate it and disable LODing.

- `ray_tracing_min_lod` (int32): [Read-Write]

- `sampling_info` (SkeletalMeshSamplingInfo): [Read-Write]

- `shadow_physics_asset` (PhysicsAsset): [Read-Write]

- `skel_mirror_axis` (AxisType): [Read-Write]

- `skel_mirror_flip_axis` (AxisType): [Read-Write]

- `skel_mirror_table` (Array[BoneMirrorInfo]): [Read-Write]

- `skeleton` (Skeleton): [Read-Only]

- `skin_weight_profiles` (Array[SkinWeightProfileInfo]): [Read-Write]

- `source_models` (Array[SkeletalMeshSourceModel]): [Read-Write]

- `support_lod_streaming` (PerPlatformBool): [Read-Write]

- `support_ray_tracing` (bool): [Read-Write]

- `target_mesh_deformers` (MeshDeformerCollection): [Read-Write] Skeletal Mesh needs this collection of deformers to make sure it cooks any extra data required by these deformers

- `thumbnail_info` (ThumbnailInfo): [Read-Only]



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

**add_socket**( _socket_, _add_to_skeleton=False_) → `None`

Add a skeletal socket object to this SkeletalMesh, and optionally promotes it to USkeleton socket.

Parameters:

- **socket** ( _SkeletalMeshSocket_)

- **add\_to\_skeleton** ( _bool_)



---

_property_ `default_animating_rig`: Object

[Read-Write]

**Type:**

( Object)


---

_property_ `default_mesh_deformer`: MeshDeformer

[Read-Only]

**Type:**

( MeshDeformer)

find\_socket\_and\_index( _socket\_name)->(SkeletalMeshSocket_, _out\_index=int32_)

Find a socket object in this SkeletalMesh by name.
Entering NAME\_None will return NULL. If there are multiple sockets with the same name, will return the first one.
Also returns the index for the socket allowing for future fast access via GetSocketByIndex()

Parameters:

**socket\_name** ( _Name_)

Returns:

out\_index (int32):

Return type:

int32


---

_property_ `forward_axis`: AxisType

[Read-Only] Axis that the skeletal mesh is facing. Default is the Y axis.
The facing axis represents the MeshDescription’s orientation and is set on import.
Therefore, if this property is modified elsewhere, the associated MeshDescription should be appropriately modified to reflect the new orientation.

**Type:**

( AxisType)


---

**get_all_morph_target_names**() → `Array\ [str]`

Returns the list of all morph targets of this skeletal mesh

Returns:

The list of morph targets

Return type:

Array\ [str]


---

**get_all_skin_weight_profile_names**() → `Array\ [str]`

Returns the list of the names of all the skin weight profile on this skeletal mesh

Returns:

The list of skin weight profiles.

Return type:

Array\ [str]


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

**get_bounds**() → `BoxSphereBounds`

Get the extended bounds of this mesh (imported bounds plus bounds extension). USkinnedAsset interface.

Return type:

BoxSphereBounds


---

**get_default_mesh_deformer**() → `MeshDeformer`

Get the default mesh deformer used by this mesh. A mesh deformer is used to deform the skeletal mesh at runtime

Return type:

MeshDeformer


---

**get_forward_axis**() → `AxisType`

Get the forward axis used by this mesh

Return type:

AxisType


---

**get_imported_bounds**() → `BoxSphereBounds`

Get the original imported bounds of the skel mesh

Return type:

BoxSphereBounds

get\_min\_lod\_for\_quality\_levels( _)->(quality\_level\_minimum\_lo\_ds=Map[PerQualityLevels,int32],default=int32_)

Get Min LODFor Quality Levels

Returns:

quality\_level\_minimum\_lo\_ds (Map[PerQualityLevels, int32]):

default (int32):

Return type:

tuple


---

**get_node_mapping_container**( _source_asset_) → `NodeMappingContainer`

Get Node Mapping Container

Parameters:

**source\_asset** ( _Blueprint_)

Return type:

NodeMappingContainer


---

**get_overlay_material**() → `MaterialInterface`

Get the default overlay material used by this mesh

Return type:

MaterialInterface


---

**get_overlay_material_max_draw_distance**() → `float`

Get the default overlay material max draw distance used by this mesh

Return type:

float


---

**get_socket_by_index**( _index_) → `SkeletalMeshSocket`

Returns a socket by index. Max index is NumSockets(). The meshes sockets are accessed first, then the skeletons.

Parameters:

**index** ( _int32_)

Return type:

SkeletalMeshSocket


---

**get_target_mesh_deformers**() → `MeshDeformerCollection`

Set the collection of mesh deformers that may be applied to this mesh. Skeletal Mesh use these deformers to determined if any extra data needs to be cooked

Return type:

MeshDeformerCollection


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

**has_vertex_colors**() → `bool`

Return whether the mesh has vertex colors. USkinnedAsset interface.

Return type:

bool


---

**is_section_using_cloth**( _section_index_, _check_corresponding_sections=True_) → `bool`

Checks whether the provided section is using APEX cloth. if bCheckCorrespondingSections is true
disabled sections will defer to correspond sections to see if they use cloth (non-cloth sections
are disabled and another section added when cloth is enabled, using this flag allows for a check
on the original section to succeed)

Parameters:

- **section\_index** ( _int32_) – Index to check

- **check\_corresponding\_sections** ( _bool_) – Whether to check corresponding sections for disabled sections


Return type:

bool


---

_property_ `lod_settings`: SkeletalMeshLODSettings

[Read-Write]

**Type:**

( SkeletalMeshLODSettings)


---

_property_ `materials`: None

[Read-Write]

**Type:**

( Array\ [SkeletalMaterial])


---

_property_ `mesh_clothing_assets`: None

[Read-Write]

**Type:**

( Array\ [ClothingAssetBase])


---

_property_ `morph_targets`: None

[Read-Write]

**Type:**

( Array\ [MorphTarget])


---

_property_ `negative_bounds_extension`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `node_mapping_data`: None

[Read-Only]

**Type:**

( Array\ [NodeMappingContainer])


---

**num_sockets**() → `int32`

Returns the number of sockets available. Both on this mesh and it’s skeleton.

Return type:

int32


---

_property_ `overlay_material`: MaterialInterface

[Read-Only]

**Type:**

( MaterialInterface)


---

_property_ `overlay_material_max_draw_distance`: float

[Read-Only]

**Type:**

( float)


---

_property_ `physics_asset`: PhysicsAsset

[Read-Only]

**Type:**

( PhysicsAsset)


---

_property_ `positive_bounds_extension`: Vector

[Read-Only]

**Type:**

( Vector)


---

_property_ `post_process_anim_blueprint`: Class

[Read-Only]

**Type:**

( type( Class))


---

**regenerate_lod**( _new_lod_count=0_, _regenerate_even_if_imported=False_, _generate_base_lod=False_) → `bool`

Regenerate LODs of the mesh

Parameters:

- **new\_lod\_count** ( _int32_) – Set valid value (>0) if you want to change LOD count. Otherwise, it will use the current LOD and regenerate

- **regenerate\_even\_if\_imported** ( _bool_) – If this is true, it only regenerate even if this LOD was imported before If false, it will regenerate for only previously auto generated ones

- **generate\_base\_lod** ( _bool_) – If this is true and there is some reduction data, the base LOD will be reduce according to the settings


Returns:

true if succeed. If mesh reduction is not available this will return false.

Return type:

bool


---

**rename_socket**( _old_name_, _new_name_) → `bool`

Rename a socket within a skeleton

Parameters:

- **old\_name** ( _Name_) – The old name of the socket

- **new\_name** ( _Name_) – The new name of the socket


Returns:

true if the renaming succeeded.

Return type:

bool


---

**set_min_lod_for_quality_levels**( _quality_level_minimum_lo_ds_, _default=-1_) → `None`

Allow to override min lod quality levels on a skeletalMesh and it Default value (-1 value for Default dont override its value).

Parameters:

- **quality\_level\_minimum\_lo\_ds** ( _Map_ _\_ [_PerQualityLevels_ _,_ _int32_ _]_)

- **default** ( _int32_)



---

**set_overlay_material**( _new_overlay_material_) → `None`

Change the default overlay material used by this mesh

Parameters:

**new\_overlay\_material** ( _MaterialInterface_)


---

**set_overlay_material_max_draw_distance**( _max_draw_distance_) → `None`

Change the default overlay material max draw distance used by this mesh

Parameters:

**max\_draw\_distance** ( _float_)


---

_property_ `shadow_physics_asset`: PhysicsAsset

[Read-Only]

**Type:**

( PhysicsAsset)


---

_property_ `skeleton`: Skeleton

[Read-Only]

**Type:**

( Skeleton)


---

_property_ `target_mesh_deformers`: MeshDeformerCollection

[Read-Only] Skeletal Mesh needs this collection of deformers to make sure it cooks any extra data required by these deformers

**Type:**

( MeshDeformerCollection)

### Table of Contents

- `unreal.SkeletalMesh`
  - `SkeletalMesh`
    - `SkeletalMesh.add_asset_user_data_of_class()`
    - `SkeletalMesh.add_socket()`
    - `SkeletalMesh.default_animating_rig`
    - `SkeletalMesh.default_mesh_deformer`
    - `SkeletalMesh.find_socket_and_index()`
    - `SkeletalMesh.forward_axis`
    - `SkeletalMesh.get_all_morph_target_names()`
    - `SkeletalMesh.get_all_skin_weight_profile_names()`
    - `SkeletalMesh.get_asset_user_data_of_class()`
    - `SkeletalMesh.get_bounds()`
    - `SkeletalMesh.get_default_mesh_deformer()`
    - `SkeletalMesh.get_forward_axis()`
    - `SkeletalMesh.get_imported_bounds()`
    - `SkeletalMesh.get_min_lod_for_quality_levels()`
    - `SkeletalMesh.get_node_mapping_container()`
    - `SkeletalMesh.get_overlay_material()`
    - `SkeletalMesh.get_overlay_material_max_draw_distance()`
    - `SkeletalMesh.get_socket_by_index()`
    - `SkeletalMesh.get_target_mesh_deformers()`
    - `SkeletalMesh.has_asset_user_data_of_class()`
    - `SkeletalMesh.has_vertex_colors()`
    - `SkeletalMesh.is_section_using_cloth()`
    - `SkeletalMesh.lod_settings`
    - `SkeletalMesh.materials`
    - `SkeletalMesh.mesh_clothing_assets`
    - `SkeletalMesh.morph_targets`
    - `SkeletalMesh.negative_bounds_extension`
    - `SkeletalMesh.node_mapping_data`
    - `SkeletalMesh.num_sockets()`
    - `SkeletalMesh.overlay_material`
    - `SkeletalMesh.overlay_material_max_draw_distance`
    - `SkeletalMesh.physics_asset`
    - `SkeletalMesh.positive_bounds_extension`
    - `SkeletalMesh.post_process_anim_blueprint`
    - `SkeletalMesh.regenerate_lod()`
    - `SkeletalMesh.rename_socket()`
    - `SkeletalMesh.set_min_lod_for_quality_levels()`
    - `SkeletalMesh.set_overlay_material()`
    - `SkeletalMesh.set_overlay_material_max_draw_distance()`
    - `SkeletalMesh.shadow_physics_asset`
    - `SkeletalMesh.skeleton`
    - `SkeletalMesh.target_mesh_deformers`