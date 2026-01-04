# unreal.MovieSceneFolderExtensions

```python
class unreal.MovieSceneFolderExtensions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Function library containing methods that should be hoisted onto UMovieSceneFolders for scripting

**C++ Source:**

- **Plugin**: SequencerScripting

- **Module**: SequencerScripting

- **File**: MovieSceneFolderExtensions.h



---

_classmethod_ add_child_folder( _target_folder_, _folder_to_add_)→bool

Add a child folder to the target folder

Parameters:

- **target\_folder** ( _MovieSceneFolder_) – The folder to add a child folder to

- **folder\_to\_add** ( _MovieSceneFolder_) – The child folder to be added


Returns:

True if the addition is successful

Return type:

bool


---

_classmethod_ add_child_object_binding( _folder_, _object_binding_)→bool

Add a guid for an object binding to this folder

Parameters:

- **folder** ( _MovieSceneFolder_) – The folder to add a child object to

- **object\_binding** ( _MovieSceneBindingProxy_) – The binding to add to the folder


Returns:

True if the addition is successful

Return type:

bool


---

_classmethod_ add_child_track( _folder_, _track_)→bool

Add a track to this folder

Parameters:

- **folder** ( _MovieSceneFolder_) – The folder to add a child track to

- **track** ( _MovieSceneTrack_) – The track to add to the folder


Returns:

True if the addition is successful

Return type:

bool


---

_classmethod_ get_child_folders( _folder_)→Array\ [MovieSceneFolder]

Get the child folders of a given folder

Parameters:

**folder** ( _MovieSceneFolder_) – The folder to get the child folders of

Returns:

The child folders associated with the given folder

Return type:

Array\ [MovieSceneFolder]


---

_classmethod_ get_child_object_bindings( _folder_)→Array\ [MovieSceneBindingProxy]

Get the object bindings contained by this folder

Parameters:

**folder** ( _MovieSceneFolder_) – The folder to get the bindings of

Returns:

The object bindings under the given folder

Return type:

Array\ [MovieSceneBindingProxy]


---

_classmethod_ get_child_tracks( _folder_)→Array\ [MovieSceneTrack]

Get the tracks contained by this folder

Parameters:

**folder** ( _MovieSceneFolder_) – The folder to get the tracks of

Returns:

The tracks under the given folder

Return type:

Array\ [MovieSceneTrack]


---

_classmethod_ get_folder_color( _folder_)→Color

Get the display color of the given folder

Parameters:

**folder** ( _MovieSceneFolder_) – The folder to get the display color of

Returns:

The display color of the given folder

Return type:

Color


---

_classmethod_ get_folder_name( _folder_)→Name

Get the given folder’s display name

Parameters:

**folder** ( _MovieSceneFolder_) – The folder to use

Returns:

The target folder’s name

Return type:

Name


---

_classmethod_ remove_child_folder( _target_folder_, _folder_to_remove_)→bool

Remove a child folder from the given folder

Parameters:

- **target\_folder** ( _MovieSceneFolder_) – The folder from which to remove a child folder

- **folder\_to\_remove** ( _MovieSceneFolder_) – The child folder to be removed


Returns:

True if the removal succeeds

Return type:

bool


---

_classmethod_ remove_child_object_binding( _folder_, _object_binding_)→bool

Remove an object binding from the given folder

Parameters:

- **folder** ( _MovieSceneFolder_) – The folder from which to remove an object binding

- **object\_binding** ( _MovieSceneBindingProxy_) – The object binding to remove


Returns:

True if the operation succeeds

Return type:

bool


---

_classmethod_ remove_child_track( _folder_, _track_)→bool

Remove a track from the given folder

Parameters:

- **folder** ( _MovieSceneFolder_) – The folder from which to remove a track

- **track** ( _MovieSceneTrack_) – The track to remove


Returns:

True if the removal succeeds

Return type:

bool


---

_classmethod_ set_folder_color( _folder_, _folder_color_)→bool

Set the display color of the given folder

Parameters:

- **folder** ( _MovieSceneFolder_) – The folder to set the display color of

- **folder\_color** ( _Color_) – The new display color for the folder


Returns:

True if the folder’s display color is set successfully

Return type:

bool


---

_classmethod_ set_folder_name( _folder_, _folder_name_)→bool

Set the name of the given folder

Parameters:

- **folder** ( _MovieSceneFolder_) – The folder to set the name of

- **folder\_name** ( _Name_) – The new name for the folder


Returns:

True if the setting of the folder name succeeds

Return type:

bool

### Table of Contents

- `unreal.MovieSceneFolderExtensions`
  - `MovieSceneFolderExtensions`
    - `MovieSceneFolderExtensions.add_child_folder()`
    - `MovieSceneFolderExtensions.add_child_object_binding()`
    - `MovieSceneFolderExtensions.add_child_track()`
    - `MovieSceneFolderExtensions.get_child_folders()`
    - `MovieSceneFolderExtensions.get_child_object_bindings()`
    - `MovieSceneFolderExtensions.get_child_tracks()`
    - `MovieSceneFolderExtensions.get_folder_color()`
    - `MovieSceneFolderExtensions.get_folder_name()`
    - `MovieSceneFolderExtensions.remove_child_folder()`
    - `MovieSceneFolderExtensions.remove_child_object_binding()`
    - `MovieSceneFolderExtensions.remove_child_track()`
    - `MovieSceneFolderExtensions.set_folder_color()`
    - `MovieSceneFolderExtensions.set_folder_name()`