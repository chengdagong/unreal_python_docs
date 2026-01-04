# unreal.EditorUtilityLibrary

```python
class unreal.EditorUtilityLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Expose editor utility functions to Blutilities

**C++ Source:**

- **Module**: Blutility

- **File**: EditorUtilityLibrary.h



---

_classmethod_ add_source_widget( _widget_blueprint_, _widget_class_, _widget_name_, _widget_parent_name_)→Widget

Create a new widget and add to the specific widget blueprint’s widget tree

Parameters:

- **widget\_blueprint** ( _WidgetBlueprint_) – The widget blueprint to add a widget to

- **widget\_class** ( _type_ _(_ _Class_ _)_) – The widget class to add to the widget blueprint

- **widget\_name** ( _Name_) – The name to give the new widget

- **widget\_parent\_name** ( _Name_) – The name of the existing widget that will hold the new widget. Must be an existing Panel Widget or none of if the widget tree is empty and the new widget will become the RootWidget.


Returns:

The widget that was created and added to the widget blueprint

Return type:

Widget

_classmethod_ cast\_to\_widget\_blueprint( _object)->(branches=CastToWidgetBlueprintCases_, _as\_widget\_blueprint=WidgetBlueprint_)

Cast to Widget Blueprint

Parameters:

**object** ( _Object_)

Returns:

branches (CastToWidgetBlueprintCases):

as\_widget\_blueprint (WidgetBlueprint):

Return type:

tuple


---

_classmethod_ convert_to_editor_utility_widget( _widget_bp_)→None

Convert to Editor Utility Widget

Parameters:

**widget\_bp** ( _WidgetBlueprint_)


---

_classmethod_ find_source_widget_by_name( _widget_blueprint_, _widget_name_)→Widget

Searches the blueprint’s widget hierarchy for a widget with the specified name

Parameters:

- **widget\_blueprint** ( _WidgetBlueprint_)

- **widget\_name** ( _Name_)


Return type:

Widget


---

**get_actor_reference**( _path_to_actor_) → `Actor`

Attempts to find the actor specified by PathToActor in the current editor world

Parameters:

**path\_to\_actor** ( _str_) – The path to the actor (e.g. PersistentLevel.PlayerStart)

Returns:

A reference to the actor, or none if it wasn’t found

Return type:

Actor


---

_classmethod_ get_current_content_browser_item_path()→ContentBrowserItemPath

Gets the current content browser path if one is open, whether it is internal or virtual.

Return type:

ContentBrowserItemPath


---

_classmethod_ get_current_content_browser_path()→strorNone

Attempts to get the path for the active content browser, returns false if there is no active content browser
or if it was a virtual path

Returns:

Whether a path was successfully returned

out\_path (str): The returned path if successfully found

Return type:

str or None


---

_classmethod_ get_selected_asset_data()→Array\ [AssetData]

Gets the set of currently selected asset data

Return type:

Array\ [AssetData]


---

_classmethod_ get_selected_assets()→Array\ [Object]

Gets the set of currently selected assets

Return type:

Array\ [Object]


---

_classmethod_ get_selected_assets_of_class( _asset_class_)→Array\ [Object]

Get Selected Assets Of Class

Parameters:

**asset\_class** ( _type_ _(_ _Class_ _)_)

Return type:

Array\ [Object]


---

_classmethod_ get_selected_blueprint_classes()→Array\ [type( Class)]

Gets the set of currently selected classes

Return type:

Array\ [type( Class)]


---

_classmethod_ get_selected_folder_paths()→Array\ [str]

Gets the path to the currently selected folder in the content browser

Return type:

Array\ [str]


---

_classmethod_ get_selected_path_view_folder_paths()→Array\ [str]

Returns the folders that are selected in the path view for the content browser

Return type:

Array\ [str]

_classmethod_ get\_selection\_bounds( _)->(origin=Vector_, _box\_extent=Vector_, _sphere\_radius=float_)

Get Selection Bounds

Returns:

origin (Vector):

box\_extent (Vector):

sphere\_radius (float):

Return type:

tuple


---

_classmethod_ get_selection_set()→Array\ [Actor]

Get Selection Set

Return type:

Array\ [Actor]


---

_classmethod_ rename_asset( _asset_, _new_name_)→None

Renames an asset (cannot move folders)

Parameters:

- **asset** ( _Object_)

- **new\_name** ( _str_)



---

_classmethod_ sync_browser_to_folders( _folder_list_)→None

Sync the Content Browser to the given folder(s)

Parameters:

**folder\_list** ( _Array_ _\_ [_str_ _]_) – The list of folders to sync to in the Content Browser

### Table of Contents

- `unreal.EditorUtilityLibrary`
  - `EditorUtilityLibrary`
    - `EditorUtilityLibrary.add_source_widget()`
    - `EditorUtilityLibrary.cast_to_widget_blueprint()`
    - `EditorUtilityLibrary.convert_to_editor_utility_widget()`
    - `EditorUtilityLibrary.find_source_widget_by_name()`
    - `EditorUtilityLibrary.get_actor_reference()`
    - `EditorUtilityLibrary.get_current_content_browser_item_path()`
    - `EditorUtilityLibrary.get_current_content_browser_path()`
    - `EditorUtilityLibrary.get_selected_asset_data()`
    - `EditorUtilityLibrary.get_selected_assets()`
    - `EditorUtilityLibrary.get_selected_assets_of_class()`
    - `EditorUtilityLibrary.get_selected_blueprint_classes()`
    - `EditorUtilityLibrary.get_selected_folder_paths()`
    - `EditorUtilityLibrary.get_selected_path_view_folder_paths()`
    - `EditorUtilityLibrary.get_selection_bounds()`
    - `EditorUtilityLibrary.get_selection_set()`
    - `EditorUtilityLibrary.rename_asset()`
    - `EditorUtilityLibrary.sync_browser_to_folders()`