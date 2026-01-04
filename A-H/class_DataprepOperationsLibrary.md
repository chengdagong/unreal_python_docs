# unreal.DataprepOperationsLibrary

```python
class unreal.DataprepOperationsLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Dataprep Operations Library

**C++ Source:**

- **Plugin**: DataprepEditor

- **Module**: DataprepLibraries

- **File**: DataprepOperationsLibrary.h



---

_classmethod_ add_metadata( _selected_objects_, _metadata_)→None

Adds metadata to selected objects that implement the UInterface\_AssetUserData interface.

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **metadata** ( _Map_ _\_ [_Name_ _,_ _str_ _]_)



---

_classmethod_ add_tags( _selected_objects_, _tags_)→None

Add tags to a set of actors

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Objects to add the tags to

- **tags** ( _Array_ _\_ [_Name_ _]_)



---

_classmethod_ add_to_layer( _selected_objects_, _layer_name_)→None

Add all Actors to a given layer.
note: This operation only applies on assets

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **layer\_name** ( _Name_)



---

_classmethod_ consolidate_objects( _selected_objects_)→None

Replace all references to the assets in the array, except the first, with the first asset of the array.

Parameters:

**selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Objects to consolidate


---

_classmethod_ flip_faces( _static_meshes_)→None

Flip the faces of all elements of a set of Static Meshes or Static Mesh Actors

Parameters:

**static\_meshes** ( _Set_ _\_ [_StaticMesh_ _]_)


---

_classmethod_ randomize_transform( _selected_objects_, _transform_type_, _reference_frame_, _min_, _max_)→None

Alters transform of selected objects by appling randomly generated offset to one of the transform components (rotation, scale or translation)

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **transform\_type** ( _RandomizeTransformType_)

- **reference\_frame** ( _RandomizeTransformReferenceFrame_)

- **min** ( _Vector_)

- **max** ( _Vector_)



---

_classmethod_ resize_textures( _textures_, _max_size_)→None

Resize textures to max width/height and optionally ensure power of two size.
note: This operation only applies on assets

Parameters:

- **textures** ( _Array_ _\_ [_Texture2D_ _]_)

- **max\_size** ( _int32_)



---

_classmethod_ set_collision_complexity( _selected_objects_, _collision_trace_flag_)→Array\ [Object]

Set collision complexity for selected meshes

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Array of meshes to process.

- **collision\_trace\_flag** ( _CollisionTraceFlag_) – The new collision complexity.


Returns:

modified\_objects (Array[Object]): List of modified meshes.

Return type:

Array\ [Object]


---

_classmethod_ set_convex_decomposition_collision( _selected_objects_, _hull_count_, _max_hull_verts_, _hull_precision_)→Array\ [Object]

Add complex collision on the static meshes contained in the input array
by the actors contained in the input array
remark:: Static meshes are not re-built after the new collision settings are set Generates an array of unique static meshes from the input array either by a cast if the UObject is a UStaticMesh or collecting the static meshes referred to if the UObject is a AActor Calls UEditorStaticMeshLibrary::SetConvexDecompositionCollisions on each static mesh of the resulting array. Note that any simple collisions on each static mesh of the resulting array will be removed.

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **hull\_count** ( _int32_) – Maximum number of convex pieces that will be created. Must be positive.

- **max\_hull\_verts** ( _int32_) – Maximum number of vertices allowed for any generated convex hull.

- **hull\_precision** ( _int32_) – Number of voxels to use when generating collision. Must be positive.


Returns:

modified\_objects (Array[Object]):

Return type:

Array\ [Object]

_classmethod_ set\_lod\_group( _selected\_objects)->(lod\_group\_name=Name,modified\_objects=Array[Object]_)

Remove inputs content
remark:: Static meshes are not re-built after the new LOD groups are set

Parameters:

**selected\_objects** ( _Array_ _\_ [_Object_ _]_)

Returns:

lod\_group\_name (Name):

modified\_objects (Array[Object]):

Return type:

tuple


---

_classmethod_ set_lods( _selected_objects_, _reduction_options_)→Array\ [Object]

Generate LODs on the static meshes contained in the input array
by the actors contained in the input array
remark:: Static meshes are not re-built after the new LODs are set Generates an array of unique static meshes from the input array either by a cast if the UObject is a UStaticMesh or collecting the static meshes referred to if the UObject is a AActor Calls UEditorStaticMeshLibrary::SetLods on each static mesh of the resulting array.

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Array of UObjects to process.

- **reduction\_options** ( _StaticMeshReductionOptions_) – Options on how to generate LODs on the mesh.


Returns:

modified\_objects (Array[Object]):

Return type:

Array\ [Object]


---

_classmethod_ set_material( _selected_objects_, _material_substitute_)→None

Set the material to all elements of a set of Static Meshes or Static Mesh Actors

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Objects to set the input material on

- **material\_substitute** ( _MaterialInterface_)



---

_classmethod_ set_mesh( _selected_objects_, _mesh_substitute_)→None

Set the mesh to all elements of a set of Actors containing StaticMeshComponents

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Objects to set the input mesh on

- **mesh\_substitute** ( _StaticMesh_) – Mesh to use



---

_classmethod_ set_mobility( _selected_objects_, _mobility_type_)→None

Set mobility on a set of static mesh actors
remark:: Only objects of class AStaticMeshActor will be considered

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Objects to set mobility on

- **mobility\_type** ( _ComponentMobility_) – Type of mobility to set on selected mesh actors



---

_classmethod_ set_nanite_settings( _selected_objects_, _enabled_, _position_precision_, _percent_triangles_)→Array\ [Object]

Set Nanite settings for selected meshes

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_) – Array of objects to process.

- **enabled** ( _bool_) – If true, Nanite data will be generated.

- **position\_precision** ( _int32_) – Step size is 2^(-PositionPrecision) cm. MIN\_int32 is auto.

- **percent\_triangles** ( _float_) – Percentage of triangles to keep from LOD0. 1.0 = no reduction, 0.0 = no triangles.


Returns:

out\_modified\_objects (Array[Object]): List of modified objects the processed meshes will be added to

Return type:

Array\ [Object]


---

_classmethod_ set_simple_collision( _selected_objects_, _shape_type_)→Array\ [Object]

Set one simple collision of the given shape type on the static meshes contained in the
input array or referred to by the actors contained in the input array
remark:: Static meshes are not re-built after the new collision settings are set Generates an array of unique static meshes from the input array either by a cast if the UObject is a UStaticMesh or collecting the static meshes referred to if the UObject is a AActor Calls UEditorStaticMeshLibrary::RemoveCollisions to remove any existing collisions on each static mesh of the resulting array Calls UEditorStaticMeshLibrary::AddSimpleCollisions on each static mesh of the resulting array.

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **shape\_type** ( _ScriptCollisionShapeType_) – Options on which simple collision to add to the mesh.


Returns:

modified\_objects (Array[Object]):

Return type:

Array\ [Object]


---

_classmethod_ set_sub_ouput_folder( _selected_objects_, _sub_folder_name_)→None

Add/Edit UDataprepConsumerUserData with the requested name for the sub-folder
note: This operation only applies on assets

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **sub\_folder\_name** ( _str_)



---

_classmethod_ set_sub_ouput_level( _selected_objects_, _sub_level_name_)→None

Add/Edit UDataprepConsumerUserData with the requested name for the sub-level
note: This operation only applies on actors

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **sub\_level\_name** ( _str_)



---

_classmethod_ substitute_material( _selected_objects_, _material_search_, _string_match_, _material_substitute_)→None

Replaces designated materials in all or specific content folders with specific ones
remark:: A material override will be added to static mesh components if their attached static mesh uses the searched material but not themselves

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **material\_search** ( _str_)

- **string\_match** ( _EditorScriptingStringMatchType_)

- **material\_substitute** ( _MaterialInterface_)



---

_classmethod_ substitute_materials_by_table( _selected_objects_, _data_table_)→None

Replaces designated materials in all or specific content folders with requested ones
remark:: SubstituteMaterial is called for each entry of the input data table

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **data\_table** ( _DataTable_)



---

_classmethod_ substitute_mesh( _selected_objects_, _mesh_search_, _string_match_, _mesh_substitute_)→None

Replaces designated meshes in all or specific content folders with specific ones

Parameters:

- **selected\_objects** ( _Array_ _\_ [_Object_ _]_)

- **mesh\_search** ( _str_)

- **string\_match** ( _EditorScriptingStringMatchType_)

- **mesh\_substitute** ( _StaticMesh_)


### Table of Contents

- `unreal.DataprepOperationsLibrary`
  - `DataprepOperationsLibrary`
    - `DataprepOperationsLibrary.add_metadata()`
    - `DataprepOperationsLibrary.add_tags()`
    - `DataprepOperationsLibrary.add_to_layer()`
    - `DataprepOperationsLibrary.consolidate_objects()`
    - `DataprepOperationsLibrary.flip_faces()`
    - `DataprepOperationsLibrary.randomize_transform()`
    - `DataprepOperationsLibrary.resize_textures()`
    - `DataprepOperationsLibrary.set_collision_complexity()`
    - `DataprepOperationsLibrary.set_convex_decomposition_collision()`
    - `DataprepOperationsLibrary.set_lod_group()`
    - `DataprepOperationsLibrary.set_lods()`
    - `DataprepOperationsLibrary.set_material()`
    - `DataprepOperationsLibrary.set_mesh()`
    - `DataprepOperationsLibrary.set_mobility()`
    - `DataprepOperationsLibrary.set_nanite_settings()`
    - `DataprepOperationsLibrary.set_simple_collision()`
    - `DataprepOperationsLibrary.set_sub_ouput_folder()`
    - `DataprepOperationsLibrary.set_sub_ouput_level()`
    - `DataprepOperationsLibrary.substitute_material()`
    - `DataprepOperationsLibrary.substitute_materials_by_table()`
    - `DataprepOperationsLibrary.substitute_mesh()`