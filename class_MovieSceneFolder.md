# unreal.MovieSceneFolder

```python
class unreal.MovieSceneFolder(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneDecorationContainerObject``


Represents a folder used for organizing objects in tracks in a movie scene.

**C++ Source:**

- **Module**: MovieScene

- **File**: MovieSceneFolder.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `folder_color` (Color): [Read-Write] This folder’s color



---

**add_child_folder**( _folder_to_add_) → `bool`

Add a child folder to the target folder

Parameters:

**folder\_to\_add** ( _MovieSceneFolder_) – The child folder to be added

Returns:

True if the addition is successful

Return type:

bool


---

**add_child_object_binding**( _object_binding_) → `bool`

Add a guid for an object binding to this folder

Parameters:

**object\_binding** ( _MovieSceneBindingProxy_) – The binding to add to the folder

Returns:

True if the addition is successful

Return type:

bool


---

**add_child_track**( _track_) → `bool`

Add a track to this folder

Parameters:

**track** ( _MovieSceneTrack_) – The track to add to the folder

Returns:

True if the addition is successful

Return type:

bool


---

**get_child_folders**() → `Array\ [MovieSceneFolder]`

Get the child folders of a given folder

Returns:

The child folders associated with the given folder

Return type:

Array\ [MovieSceneFolder]


---

**get_child_object_bindings**() → `Array\ [MovieSceneBindingProxy]`

Get the object bindings contained by this folder

Returns:

The object bindings under the given folder

Return type:

Array\ [MovieSceneBindingProxy]


---

**get_child_tracks**() → `Array\ [MovieSceneTrack]`

Get the tracks contained by this folder

Returns:

The tracks under the given folder

Return type:

Array\ [MovieSceneTrack]


---

**get_folder_color**() → `Color`

Get the display color of the given folder

Returns:

The display color of the given folder

Return type:

Color


---

**get_folder_name**() → `Name`

Get the given folder’s display name

Returns:

The target folder’s name

Return type:

Name


---

**remove_child_folder**( _folder_to_remove_) → `bool`

Remove a child folder from the given folder

Parameters:

**folder\_to\_remove** ( _MovieSceneFolder_) – The child folder to be removed

Returns:

True if the removal succeeds

Return type:

bool


---

**remove_child_object_binding**( _object_binding_) → `bool`

Remove an object binding from the given folder

Parameters:

**object\_binding** ( _MovieSceneBindingProxy_) – The object binding to remove

Returns:

True if the operation succeeds

Return type:

bool


---

**remove_child_track**( _track_) → `bool`

Remove a track from the given folder

Parameters:

**track** ( _MovieSceneTrack_) – The track to remove

Returns:

True if the removal succeeds

Return type:

bool


---

**set_folder_color**( _folder_color_) → `bool`

Set the display color of the given folder

Parameters:

**folder\_color** ( _Color_) – The new display color for the folder

Returns:

True if the folder’s display color is set successfully

Return type:

bool


---

**set_folder_name**( _folder_name_) → `bool`

Set the name of the given folder

Parameters:

**folder\_name** ( _Name_) – The new name for the folder

Returns:

True if the setting of the folder name succeeds

Return type:

bool

### Table of Contents

- `unreal.MovieSceneFolder`
  - `MovieSceneFolder`
    - `MovieSceneFolder.add_child_folder()`
    - `MovieSceneFolder.add_child_object_binding()`
    - `MovieSceneFolder.add_child_track()`
    - `MovieSceneFolder.get_child_folders()`
    - `MovieSceneFolder.get_child_object_bindings()`
    - `MovieSceneFolder.get_child_tracks()`
    - `MovieSceneFolder.get_folder_color()`
    - `MovieSceneFolder.get_folder_name()`
    - `MovieSceneFolder.remove_child_folder()`
    - `MovieSceneFolder.remove_child_object_binding()`
    - `MovieSceneFolder.remove_child_track()`
    - `MovieSceneFolder.set_folder_color()`
    - `MovieSceneFolder.set_folder_name()`