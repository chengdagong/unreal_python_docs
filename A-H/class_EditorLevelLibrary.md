# unreal.EditorLevelLibrary

```python
class unreal.EditorLevelLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Utility class to do most of the common functionalities in the World Editor.
The editor should not be in play in editor mode.

**C++ Source:**

- **Plugin**: EditorScriptingUtilities

- **Module**: EditorScriptingUtilities

- **File**: EditorLevelLibrary.h



---

_classmethod_ clear_actor_selection_set()→None

Clear Actor Selection Set
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem


---

_classmethod_ convert_actors( _actors_, _actor_class_, _static_mesh_package_path_)→Array\ [Actor]

Convert Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Parameters:

- **actors** ( _Array_ _\_ [_Actor_ _]_)

- **actor\_class** ( _type_ _(_ _Class_ _)_)

- **static\_mesh\_package\_path** ( _str_)


Return type:

Array\ [Actor]


---

_classmethod_ create_proxy_mesh_actor( _actors_to_merge_, _merge_options_)→StaticMeshActororNone

Create Proxy Mesh Actor
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Static Mesh Editor Subsystem

Parameters:

- **actors\_to\_merge** ( _Array_ _\_ [_StaticMeshActor_ _]_)

- **merge\_options** ( _CreateProxyMeshActorOptions_)


Returns:

out\_merged\_actor (StaticMeshActor):

Return type:

StaticMeshActor or None


---

_classmethod_ destroy_actor( _actor_to_destroy_)→bool

Destroy Actor
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Parameters:

**actor\_to\_destroy** ( _Actor_)

Return type:

bool


---

_classmethod_ editor_end_play()→None

Editor End Play


---

_classmethod_ editor_invalidate_viewports()→None

Editor Invalidate Viewports
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem


---

_classmethod_ editor_play_simulate()→None

Editor Play Simulate
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem


---

_classmethod_ editor_set_game_view( _game_view_)→None

Editor Set Game View
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Parameters:

**game\_view** ( _bool_)


---

_classmethod_ eject_pilot_level_actor()→None

Eject Pilot Level Actor
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem


---

_classmethod_ get_actor_reference( _path_to_actor_)→Actor

Get Actor Reference
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Parameters:

**path\_to\_actor** ( _str_)

Return type:

Actor


---

_classmethod_ get_all_level_actors()→Array\ [Actor]

Get All Level Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Return type:

Array\ [Actor]


---

_classmethod_ get_all_level_actors_components()→Array\ [ActorComponent]

Get All Level Actors Components
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Return type:

Array\ [ActorComponent]


---

_classmethod_ get_editor_world()→World

Get Editor World
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Unreal Editor Subsystem

Return type:

World


---

_classmethod_ get_game_world()→World

Get Game World
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Unreal Editor Subsystem

Return type:

World


---

_classmethod_ get_level_viewport_camera_info()→(camera_location=Vector,camera_rotation=Rotator)orNone

Get Level Viewport Camera Info
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Unreal Editor Subsystem

Returns:

camera\_location (Vector):

camera\_rotation (Rotator):

Return type:

tuple or None


---

_classmethod_ get_pie_worlds( _include_dedicated_server_)→Array\ [World]

Get PIEWorlds

Parameters:

**include\_dedicated\_server** ( _bool_)

Return type:

Array\ [World]


---

_classmethod_ get_selected_level_actors()→Array\ [Actor]

Get Selected Level Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Return type:

Array\ [Actor]


---

_classmethod_ join_static_mesh_actors( _actors_to_join_, _join_options_)→Actor

Join Static Mesh Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Static Mesh Editor Subsystem

Parameters:

- **actors\_to\_join** ( _Array_ _\_ [_StaticMeshActor_ _]_)

- **join\_options** ( _JoinStaticMeshActorsOptions_)


Return type:

Actor


---

_classmethod_ load_level( _asset_path_)→bool

Load Level
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Parameters:

**asset\_path** ( _str_)

Return type:

bool


---

_classmethod_ merge_static_mesh_actors( _actors_to_merge_, _merge_options_)→StaticMeshActororNone

Merge Static Mesh Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Static Mesh Editor Subsystem

Parameters:

- **actors\_to\_merge** ( _Array_ _\_ [_StaticMeshActor_ _]_)

- **merge\_options** ( _MergeStaticMeshActorsOptions_)


Returns:

out\_merged\_actor (StaticMeshActor):

Return type:

StaticMeshActor or None


---

_classmethod_ new_level( _asset_path_)→bool

New Level
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Parameters:

**asset\_path** ( _str_)

Return type:

bool


---

_classmethod_ new_level_from_template( _asset_path_, _template_asset_path_)→bool

New Level from Template
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Parameters:

- **asset\_path** ( _str_)

- **template\_asset\_path** ( _str_)


Return type:

bool


---

_classmethod_ pilot_level_actor( _actor_to_pilot_)→None

Pilot Level Actor
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Parameters:

**actor\_to\_pilot** ( _Actor_)


---

_classmethod_ replace_mesh_components_materials( _mesh_components_, _material_to_be_replaced_, _new_material_)→None

Replace Mesh Components Materials
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Static Mesh Editor Subsystem

Parameters:

- **mesh\_components** ( _Array_ _\_ [_MeshComponent_ _]_)

- **material\_to\_be\_replaced** ( _MaterialInterface_)

- **new\_material** ( _MaterialInterface_)



---

_classmethod_ replace_mesh_components_materials_on_actors( _actors_, _material_to_be_replaced_, _new_material_)→None

Replace Mesh Components Materials on Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Static Mesh Editor Subsystem

Parameters:

- **actors** ( _Array_ _\_ [_Actor_ _]_)

- **material\_to\_be\_replaced** ( _MaterialInterface_)

- **new\_material** ( _MaterialInterface_)



---

_classmethod_ replace_mesh_components_meshes( _mesh_components_, _mesh_to_be_replaced_, _new_mesh_)→None

Replace Mesh Components Meshes
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Static Mesh Editor Subsystem

Parameters:

- **mesh\_components** ( _Array_ _\_ [_StaticMeshComponent_ _]_)

- **mesh\_to\_be\_replaced** ( _StaticMesh_)

- **new\_mesh** ( _StaticMesh_)



---

_classmethod_ replace_mesh_components_meshes_on_actors( _actors_, _mesh_to_be_replaced_, _new_mesh_)→None

Replace Mesh Components Meshes on Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Static Mesh Editor Subsystem

Parameters:

- **actors** ( _Array_ _\_ [_Actor_ _]_)

- **mesh\_to\_be\_replaced** ( _StaticMesh_)

- **new\_mesh** ( _StaticMesh_)



---

_classmethod_ replace_selected_actors( _asset_path_)→None

Replaces the selected Actors with the same number of a different kind of Actor using the specified factory to spawn the new Actors
note that only Location, Rotation, Drawscale, Drawscale3D, Tag, and Group are copied from the old Actors

Parameters:

**asset\_path** ( _str_)


---

_classmethod_ save_all_dirty_levels()→bool

Save All Dirty Levels
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Return type:

bool


---

_classmethod_ save_current_level()→bool

Save Current Level
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Return type:

bool


---

_classmethod_ select_nothing()→None

Select Nothing
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem


---

_classmethod_ set_actor_selection_state( _actor_, _should_be_selected_)→None

Set Actor Selection State
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Parameters:

- **actor** ( _Actor_)

- **should\_be\_selected** ( _bool_)



---

_classmethod_ set_current_level_by_name( _level_name_)→bool

Set Current Level by Name
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Level Editor Subsystem

Parameters:

**level\_name** ( _Name_)

Return type:

bool


---

_classmethod_ set_level_viewport_camera_info( _camera_location_, _camera_rotation_)→None

Set Level Viewport Camera Info
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Unreal Editor Subsystem

Parameters:

- **camera\_location** ( _Vector_)

- **camera\_rotation** ( _Rotator_)



---

_classmethod_ set_selected_level_actors( _actors_to_select_)→None

Set Selected Level Actors
deprecated: The Editor Scripting Utilities Plugin is deprecated - Use the function in Editor Actor Utilities Subsystem

Parameters:

**actors\_to\_select** ( _Array_ _\_ [_Actor_ _]_)


---

_classmethod_ spawn_actor_from_class( _actor_class_, _location_, _rotation=[0.000000,0.000000,0.000000]_, _transient=False_)→Actor

Spawn Actor from Class

Parameters:

- **actor\_class** ( _type_ _(_ _Class_ _)_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **transient** ( _bool_)


Return type:

Actor


---

_classmethod_ spawn_actor_from_object( _object_to_use_, _location_, _rotation=[0.000000,0.000000,0.000000]_, _transient=False_)→Actor

Spawn Actor from Object

Parameters:

- **object\_to\_use** ( _Object_)

- **location** ( _Vector_)

- **rotation** ( _Rotator_)

- **transient** ( _bool_)


Return type:

Actor

### Table of Contents

- `unreal.EditorLevelLibrary`
  - `EditorLevelLibrary`
    - `EditorLevelLibrary.clear_actor_selection_set()`
    - `EditorLevelLibrary.convert_actors()`
    - `EditorLevelLibrary.create_proxy_mesh_actor()`
    - `EditorLevelLibrary.destroy_actor()`
    - `EditorLevelLibrary.editor_end_play()`
    - `EditorLevelLibrary.editor_invalidate_viewports()`
    - `EditorLevelLibrary.editor_play_simulate()`
    - `EditorLevelLibrary.editor_set_game_view()`
    - `EditorLevelLibrary.eject_pilot_level_actor()`
    - `EditorLevelLibrary.get_actor_reference()`
    - `EditorLevelLibrary.get_all_level_actors()`
    - `EditorLevelLibrary.get_all_level_actors_components()`
    - `EditorLevelLibrary.get_editor_world()`
    - `EditorLevelLibrary.get_game_world()`
    - `EditorLevelLibrary.get_level_viewport_camera_info()`
    - `EditorLevelLibrary.get_pie_worlds()`
    - `EditorLevelLibrary.get_selected_level_actors()`
    - `EditorLevelLibrary.join_static_mesh_actors()`
    - `EditorLevelLibrary.load_level()`
    - `EditorLevelLibrary.merge_static_mesh_actors()`
    - `EditorLevelLibrary.new_level()`
    - `EditorLevelLibrary.new_level_from_template()`
    - `EditorLevelLibrary.pilot_level_actor()`
    - `EditorLevelLibrary.replace_mesh_components_materials()`
    - `EditorLevelLibrary.replace_mesh_components_materials_on_actors()`
    - `EditorLevelLibrary.replace_mesh_components_meshes()`
    - `EditorLevelLibrary.replace_mesh_components_meshes_on_actors()`
    - `EditorLevelLibrary.replace_selected_actors()`
    - `EditorLevelLibrary.save_all_dirty_levels()`
    - `EditorLevelLibrary.save_current_level()`
    - `EditorLevelLibrary.select_nothing()`
    - `EditorLevelLibrary.set_actor_selection_state()`
    - `EditorLevelLibrary.set_current_level_by_name()`
    - `EditorLevelLibrary.set_level_viewport_camera_info()`
    - `EditorLevelLibrary.set_selected_level_actors()`
    - `EditorLevelLibrary.spawn_actor_from_class()`
    - `EditorLevelLibrary.spawn_actor_from_object()`