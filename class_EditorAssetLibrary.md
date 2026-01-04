# unreal.EditorAssetLibrary

```python
class unreal.EditorAssetLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Utility class to do most of the common functionalities with the ContentBrowser.
The AssetRegistryHelpers class has more complex utilities. Use FindAssetData to get a FAssetData from an Asset Path.
The Asset Path can be represented by

> ie. (Reference/Text Path) StaticMesh’/Game/MyFolder/MyAsset.MyAsset’
> ie. (Full Name) StaticMesh /Game/MyFolder/MyAsset.MyAsset
> ie. (Path Name) /Game/MyFolder/MyAsset.MyAsset
> ie. (Package Name) /Game/MyFolder/MyAsset

The Directory Path can be represented by

ie. /Game/MyNewFolder/
ie. /Game/MyNewFolder

All operations can be slow. The editor should not be in play in editor mode. It will not work on assets of the type level.

**C++ Source:**

- **Plugin**: EditorScriptingUtilities

- **Module**: EditorScriptingUtilities

- **File**: EditorAssetLibrary.h



---

_classmethod_ checkout_asset( _asset_to_checkout_)→bool

Checkout the asset from the Content Browser.

Parameters:

**asset\_to\_checkout** ( _str_) – Asset Path of the asset that we want to checkout.

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ checkout_directory( _directory_path_, _recursive=True_)→bool

Checkout assets from the Content Browser. It will load the assets if needed.
All objects that are in the directory will be checkout. Assets will be loaded before being checkout.

Parameters:

- **directory\_path** ( _str_) – Directory of the assets that to checkout.

- **recursive** ( _bool_) – If the AssetPath is a folder, the search will be recursive and will checkout the asset in the sub folders.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ checkout_loaded_asset( _asset_to_checkout_)→bool

Checkout the asset from the Content Browser.

Parameters:

**asset\_to\_checkout** ( _Object_) – Asset to checkout.

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ checkout_loaded_assets( _assets_to_checkout_)→bool

Checkout the assets from the Content Browser.

Parameters:

**assets\_to\_checkout** ( _Array_ _\_ [_Object_ _]_)

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ consolidate_assets( _asset_to_consolidate_to_, _assets_to_consolidate_)→bool

Consolidates an asset by replacing all references/uses of the provided AssetsToConsolidate with references to AssetToConsolidateTo.
This is useful when you want all references of assets to be replaced by a single asset.
The function first attempts to directly replace all relevant references located within objects that are already loaded and in memory.
Next, it deletes the AssetsToConsolidate, leaving behind object redirectors to AssetToConsolidateTo.
note: The AssetsToConsolidate are DELETED by this function.
note: Modified objects will be saved if the operation succeeds.

Parameters:

- **asset\_to\_consolidate\_to** ( _Object_) – Asset to which all references of the AssetsToConsolidate will instead refer to after this operation completes.

- **assets\_to\_consolidate** ( _Array_ _\_ [_Object_ _]_) – All references to these assets will be modified to reference AssetToConsolidateTo instead.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ delete_asset( _asset_path_to_delete_)→bool

Delete the package the assets live in. All objects that live in the package will be deleted.
This is a Force Delete. It doesn’t check if the asset has references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the file as deleted. The Asset will be loaded before being deleted.

Parameters:

**asset\_path\_to\_delete** ( _str_) – Asset Path of the asset that we want to delete.

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ delete_directory( _directory_path_)→bool

Delete the packages inside a directory. If the directory is then empty, delete the directory.
This is a Force Delete. It doesn’t check if the assets have references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the file as deleted. Assets will be loaded before being deleted.
The search is always recursive. It will try to delete the sub folders.

Parameters:

**directory\_path** ( _str_) – Directory that will be mark for delete and deleted.

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ delete_loaded_asset( _asset_to_delete_)→bool

Delete an asset from the Content Browser that is already loaded.
This is a Force Delete. It doesn’t check if the asset has references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the file as deleted.

Parameters:

**asset\_to\_delete** ( _Object_) – Asset that we want to delete.

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ delete_loaded_assets( _assets_to_delete_)→bool

Delete assets from the Content Browser that are already loaded.
This is a Force Delete. It doesn’t check if the assets have references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the files as deleted.

Parameters:

**assets\_to\_delete** ( _Array_ _\_ [_Object_ _]_) – Assets that we want to delete.

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ do_assets_exist( _asset_paths_)→bool

Check if the assets exist in the Content Browser.

Parameters:

**asset\_paths** ( _Array_ _\_ [_str_ _]_) – Asset Path of the assets (that are not a level).

Returns:

True if they exist and it is valid.

Return type:

bool


---

_classmethod_ does_asset_exist( _asset_path_)→bool

Check if the asset exists in the Content Browser.

Parameters:

**asset\_path** ( _str_) – Asset Path of the asset (that is not a level).

Returns:

True if it does exist and it is valid.

Return type:

bool


---

_classmethod_ does_directory_exist( _directory_path_)→bool

Check is the directory exist in the Content Browser.

Parameters:

**directory\_path** ( _str_) – Long Path Name of the directory.

Returns:

True if it does exist and it is valid.

Return type:

bool


---

_classmethod_ does_directory_have_assets( _directory_path_, _recursive=True_)→bool

Check if there any asset that exist in the directory.

Parameters:

- **directory\_path** ( _str_) – Long Path Name of the directory.

- **recursive** ( _bool_)


Returns:

True if there is any assets.

Return type:

bool


---

_classmethod_ duplicate_asset( _source_asset_path_, _destination_asset_path_)→Object

Duplicate an asset from the Content Browser. Will try to checkout the file. The Asset will be loaded before being duplicated.

Parameters:

- **source\_asset\_path** ( _str_) – Asset Path of the asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the duplicated asset.


Returns:

The duplicated object if the operation succeeds.

Return type:

Object


---

_classmethod_ duplicate_directory( _source_directory_path_, _destination_directory_path_)→bool

Duplicate asset from the Content Browser that are in the folder.
Will try to checkout the files. The Assets will be loaded before being duplicated.

Parameters:

- **source\_directory\_path** ( _str_) – Directory of the assets that we want to duplicate from.

- **destination\_directory\_path** ( _str_) – Directory of the duplicated asset.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ duplicate_loaded_asset( _source_asset_, _destination_asset_path_)→Object

Duplicate an asset from the Content Browser that is already loaded. Will try to checkout the file.

Parameters:

- **source\_asset** ( _Object_) – Asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the duplicated asset.


Returns:

The duplicated object if the operation succeeds

Return type:

Object


---

_classmethod_ find_asset_data( _asset_path_)→AssetData

Return the AssetData for the Asset that can then be used with the more complex lib AssetRegistryHelpers.

Parameters:

**asset\_path** ( _str_) – Asset Path we are trying to find.

Returns:

The AssetData found.

Return type:

AssetData


---

_classmethod_ find_package_referencers_for_asset( _asset_path_, _load_assets_to_confirm=False_)→Array\ [str]

Find Package Referencers for an asset. Only Soft and Hard dependencies would be looked for.
Soft are dependencies which don’t need to be loaded for the object to be used.
Had are dependencies which are required for correct usage of the source asset and must be loaded at the same time.
Other references may exist. The asset may be currently used in memory by another asset, by the editor or by code.
Package dependencies are cached with the asset. False positive can happen until all the assets are loaded and re-saved.

Parameters:

- **asset\_path** ( _str_) – Asset Path of the asset that we are looking for (that is not a level).

- **load\_assets\_to\_confirm** ( _bool_) – The asset and the referencers will be loaded (if not a level) to confirm the dependencies.


Returns:

The package path of the referencers.

Return type:

Array\ [str]


---

_classmethod_ get_metadata_tag( _object_, _tag_)→str

Get the value associated with the given tag of a loaded asset’s metadata.

Parameters:

- **object** ( _Object_) – The object from which to retrieve the metadata.

- **tag** ( _Name_) – The tag to find in the metadata.


Returns:

The string value associated with the tag.

Return type:

str


---

_classmethod_ get_metadata_tag_values( _object_)→Map\ [Name, str]

Get all tags/values of a loaded asset’s metadata.

Parameters:

**object** ( _Object_) – The object from which to retrieve the metadata.

Returns:

The list of all Tags and Values.

Return type:

Map\ [Name, str]


---

_classmethod_ get_package_for_object( _object_)→Package

Returns the object’s containing package

Parameters:

**object** ( _Object_)

Return type:

Package


---

_classmethod_ get_path_name_for_loaded_asset( _loaded_asset_)→str

Return a valid AssetPath for a loaded asset. The asset need to be a valid asset in the Content Browser.
Similar to GetPathName(). The format will be: /Game/MyFolder/MyAsset.MyAsset

Parameters:

**loaded\_asset** ( _Object_) – Loaded Asset that exist in the Content Browser.

Returns:

If valid, the asset Path of the loaded asset.

Return type:

str


---

_classmethod_ get_project_root_asset_directory()→str

Historically, all project assets were stored in the logical “/Game/” directory
when using plugins or UEFN projects, we want to ease asset reuse, and so the ambiguous
“/Game/” directory is untenable. This function will return the useful project name.

Returns:

The current project name in UEFN, otherwise /Game/ for .uprojects

Return type:

str


---

_classmethod_ get_tag_values( _asset_path_)→Map\ [Name, str]

Gets all TagValues (from Asset Registry) associated with an (unloaded) asset as strings value.

Parameters:

**asset\_path** ( _str_) – Asset Path we are trying to find.

Returns:

The list of all TagName & TagValue.

Return type:

Map\ [Name, str]


---

_classmethod_ list_asset_by_tag_value( _tag_name_, _tag_value_)→Array\ [str]

Return the list of all the assets that have the pair of Tag/Value.

Parameters:

- **tag\_name** ( _Name_) – The tag associated with the assets requested.

- **tag\_value** ( _str_) – The value associated with the assets requested.


Returns:

The list of asset found.

Return type:

Array\ [str]


---

_classmethod_ list_assets( _directory_path_, _recursive=True_, _include_folder=False_)→Array\ [str]

Return the list of all the assets found in the DirectoryPath.

Parameters:

- **directory\_path** ( _str_) – Directory path of the asset we want the list from.

- **recursive** ( _bool_) – The search will be recursive and will look in sub folders.

- **include\_folder** ( _bool_) – The result will include folders name.


Returns:

The list of asset found.

Return type:

Array\ [str]


---

_classmethod_ load_asset( _asset_path_)→Object

Load an asset from the Content Browser. It will verify if the object is already loaded and only load it if it’s necessary.

Parameters:

**asset\_path** ( _str_) – Asset Path of the asset (that is not a level).

Returns:

Found or loaded asset.

Return type:

Object

_classmethod_ load\_blueprint\_class( _asset\_path_)

Load a Blueprint asset from the Content Browser and return its generated class. It will verify if the object is already loaded and only load it if it’s necessary.

Parameters:

**asset\_path** ( _str_) – Asset Path of the Blueprint asset.

Returns:

Found or loaded class.

Return type:

type( Class)


---

_classmethod_ make_directory( _directory_path_)→bool

Create the directory on disk and in the Content Browser.

Parameters:

**directory\_path** ( _str_) – Long Path Name of the directory.

Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ remove_metadata_tag( _object_, _tag_)→None

Remove the given tag from a loaded asset’s metadata.

Parameters:

- **object** ( _Object_) – The object from which to retrieve the metadata.

- **tag** ( _Name_) – The tag to remove from the metadata.



---

_classmethod_ rename_asset( _source_asset_path_, _destination_asset_path_)→bool

Rename an asset from the Content Browser. Equivalent to a Move operation.
Will try to checkout the file. The Asset will be loaded before being renamed.

Parameters:

- **source\_asset\_path** ( _str_) – Asset Path of the asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the renamed asset.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ rename_directory( _source_directory_path_, _destination_directory_path_)→bool

Rename assets from the Content Browser that are in the folder.
Equivalent to a Move operation. Will try to checkout the files. The Assets will be loaded before being renamed.

Parameters:

- **source\_directory\_path** ( _str_) – Directory of the assets that we want to rename from.

- **destination\_directory\_path** ( _str_) – Directory of the renamed asset.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ rename_loaded_asset( _source_asset_, _destination_asset_path_)→bool

Rename an asset from the Content Browser that is already loaded.
Equivalent to a Move operation. Will try to checkout the files.

Parameters:

- **source\_asset** ( _Object_) – Asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the duplicated asset.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ save_asset( _asset_to_save_, _only_if_is_dirty=True_)→bool

Save the packages the assets live in. All objects that live in the package will be saved.
Will try to checkout the file first. The Asset will be loaded before being saved.

Parameters:

- **asset\_to\_save** ( _str_)

- **only\_if\_is\_dirty** ( _bool_) – Only checkout/save the asset if it’s dirty.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ save_directory( _directory_path_, _only_if_is_dirty=True_, _recursive=True_)→bool

Save the packages the assets live in inside the directory. All objects that are in the directory will be saved.
Will try to checkout the file first. Assets will be loaded before being saved.

Parameters:

- **directory\_path** ( _str_) – Directory that will be checked out and saved.

- **only\_if\_is\_dirty** ( _bool_) – Only checkout asset that are dirty.

- **recursive** ( _bool_) – The search will be recursive and it will save the asset in the sub folders.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ save_loaded_asset( _asset_to_save_, _only_if_is_dirty=True_)→bool

Save the packages the assets live in. All objects that live in the package will be saved. Will try to checkout the file.

Parameters:

- **asset\_to\_save** ( _Object_) – Asset that we want to save.

- **only\_if\_is\_dirty** ( _bool_) – Only checkout asset that are dirty.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ save_loaded_assets( _assets_to_save_, _only_if_is_dirty=True_)→bool

Save the packages the assets live in. All objects that live in the package will be saved. Will try to checkout the files.

Parameters:

- **assets\_to\_save** ( _Array_ _\_ [_Object_ _]_)

- **only\_if\_is\_dirty** ( _bool_) – Only checkout asset that are dirty.


Returns:

True if the operation succeeds.

Return type:

bool


---

_classmethod_ set_metadata_tag( _object_, _tag_, _value_)→None

Set the value associated with a given tag of a loaded asset’s metadata.

Parameters:

- **object** ( _Object_) – The object from which to retrieve the metadata.

- **tag** ( _Name_) – The tag to set in the metadata.

- **value** ( _str_) – The string value to associate with the tag.



---

_classmethod_ sync_browser_to_objects( _asset_paths_)→None

Browses to the associated asset and selects it in the most recently used Content Browser (summoning one if necessary)
This is an asynchronous operation that can take a couple of frames to resolve the request

Parameters:

**asset\_paths** ( _Array_ _\_ [_str_ _]_) – The list of asset paths to sync to in the Content Browser

### Table of Contents

- `unreal.EditorAssetLibrary`
  - `EditorAssetLibrary`
    - `EditorAssetLibrary.checkout_asset()`
    - `EditorAssetLibrary.checkout_directory()`
    - `EditorAssetLibrary.checkout_loaded_asset()`
    - `EditorAssetLibrary.checkout_loaded_assets()`
    - `EditorAssetLibrary.consolidate_assets()`
    - `EditorAssetLibrary.delete_asset()`
    - `EditorAssetLibrary.delete_directory()`
    - `EditorAssetLibrary.delete_loaded_asset()`
    - `EditorAssetLibrary.delete_loaded_assets()`
    - `EditorAssetLibrary.do_assets_exist()`
    - `EditorAssetLibrary.does_asset_exist()`
    - `EditorAssetLibrary.does_directory_exist()`
    - `EditorAssetLibrary.does_directory_have_assets()`
    - `EditorAssetLibrary.duplicate_asset()`
    - `EditorAssetLibrary.duplicate_directory()`
    - `EditorAssetLibrary.duplicate_loaded_asset()`
    - `EditorAssetLibrary.find_asset_data()`
    - `EditorAssetLibrary.find_package_referencers_for_asset()`
    - `EditorAssetLibrary.get_metadata_tag()`
    - `EditorAssetLibrary.get_metadata_tag_values()`
    - `EditorAssetLibrary.get_package_for_object()`
    - `EditorAssetLibrary.get_path_name_for_loaded_asset()`
    - `EditorAssetLibrary.get_project_root_asset_directory()`
    - `EditorAssetLibrary.get_tag_values()`
    - `EditorAssetLibrary.list_asset_by_tag_value()`
    - `EditorAssetLibrary.list_assets()`
    - `EditorAssetLibrary.load_asset()`
    - `EditorAssetLibrary.load_blueprint_class()`
    - `EditorAssetLibrary.make_directory()`
    - `EditorAssetLibrary.remove_metadata_tag()`
    - `EditorAssetLibrary.rename_asset()`
    - `EditorAssetLibrary.rename_directory()`
    - `EditorAssetLibrary.rename_loaded_asset()`
    - `EditorAssetLibrary.save_asset()`
    - `EditorAssetLibrary.save_directory()`
    - `EditorAssetLibrary.save_loaded_asset()`
    - `EditorAssetLibrary.save_loaded_assets()`
    - `EditorAssetLibrary.set_metadata_tag()`
    - `EditorAssetLibrary.sync_browser_to_objects()`