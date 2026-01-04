# unreal.EditorAssetSubsystem

```python
class unreal.EditorAssetSubsystem(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EditorSubsystem``


UEditorAssetSubsystem
Subsystem for exposing asset related utilities to scripts.
Asset Paths can be represented in the following ways:

> (Reference/Text Path) StaticMesh’/Game/MyFolder/MyAsset.MyAsset’
> (Full Name) StaticMesh /Game/MyFolder/MyAsset.MyAsset
> (Path Name) /Game/MyFolder/MyAsset.MyAsset
> (Package Name) /Game/MyFolder/MyAsset

Directory Paths can be represented in the following ways:

/Game/MyNewFolder/
/Game/MyNewFolder

**C++ Source:**

- **Module**: UnrealEd

- **File**: EditorAssetSubsystem.h



---

**add_on_extract_asset_from_file**( _delegate_) → `None`

Call this to add a callback to extract an asset from a file,
for example from a drag and drop operation.

Parameters:

**delegate** ( _OnExtractAssetFromFileDynamic_)


---

**checkout_asset**( _asset_to_checkout_) → `bool`

Checkout an asset.

Parameters:

**asset\_to\_checkout** ( _str_) – Asset Path of the asset that we want to checkout.

Returns:

True if the operation succeeds.

Return type:

bool


---

**checkout_directory**( _directory_path_, _recursive=True_) → `bool`

Checkout all assets in a directory. It will load the assets if needed.
All objects that are in the directory will be checked out. Assets will be loaded before being checked out.

Parameters:

- **directory\_path** ( _str_) – Directory of the assets to be checked out.

- **recursive** ( _bool_) – If the AssetPath is a folder, the search will be recursive and will checkout the assets in the sub folders.


Returns:

True if the operation succeeds.

Return type:

bool


---

**checkout_loaded_asset**( _asset_to_checkout_) → `bool`

Checkout the asset corresponding to an object.

Parameters:

**asset\_to\_checkout** ( _Object_) – Asset to checkout.

Returns:

True if the operation succeeds.

Return type:

bool


---

**checkout_loaded_assets**( _assets_to_checkout_) → `bool`

Checkout the assets.

Parameters:

**assets\_to\_checkout** ( _Array_ _\_ [_Object_ _]_) – Assets to checkout.

Returns:

True if the operation succeeds.

Return type:

bool


---

**consolidate_assets**( _asset_to_consolidate_to_, _assets_to_consolidate_) → `bool`

Consolidates assets by replacing all references/uses of the provided AssetsToConsolidate with references to AssetToConsolidateTo.
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

**delete_asset**( _asset_path_to_delete_) → `bool`

Delete the package an asset is in. All objects in the package will be deleted.
This is a Force Delete. It does not check if the asset has references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the file as deleted. The Asset will be loaded before being deleted.

Parameters:

**asset\_path\_to\_delete** ( _str_) – Asset Path of the asset to delete.

Returns:

True if the operation succeeds.

Return type:

bool


---

**delete_directory**( _directory_path_) → `bool`

Delete the packages inside a directory. If the directory is then empty, delete the directory.
This is a Force Delete. It does not check if the assets have references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the file as deleted. Assets will be loaded before being deleted.
The search is always recursive. It will try to delete the sub folders.

Parameters:

**directory\_path** ( _str_) – Directory that will be marked for deletion and deleted.

Returns:

True if the operation succeeds.

Return type:

bool


---

**delete_loaded_asset**( _asset_to_delete_) → `bool`

Delete an asset that is already loaded.
This is a Force Delete. It does not check if the asset has references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the file as deleted.

Parameters:

**asset\_to\_delete** ( _Object_) – Asset to delete.

Returns:

True if the operation succeeds.

Return type:

bool


---

**delete_loaded_assets**( _assets_to_delete_) → `bool`

Delete assets that are already loaded.
This is a Force Delete. It does not check if the assets have references in other Levels or by Actors.
It will close all the asset editors and may clear the Transaction buffer (Undo History).
Will try to mark the files as deleted.

Parameters:

**assets\_to\_delete** ( _Array_ _\_ [_Object_ _]_) – Loaded assets to delete.

Returns:

True if the operation succeeds.

Return type:

bool


---

**do_assets_exist**( _asset_paths_) → `bool`

Check if assets exist in the Asset Registry.

Parameters:

**asset\_paths** ( _Array_ _\_ [_str_ _]_) – Asset Paths of the assets to check for existence.

Returns:

True if all assets exist and are valid.

Return type:

bool


---

**does_asset_exist**( _asset_path_) → `bool`

Check if an asset exists in the Asset Registry.

Parameters:

**asset\_path** ( _str_) – Asset Path to check for existence.

Returns:

True if the asset exists and is valid.

Return type:

bool


---

**does_directory_contain_assets**( _directory_path_, _recursive=True_) → `bool`

Check if a directory contains any assets.

Parameters:

- **directory\_path** ( _str_) – Long Path Name of the directory.

- **recursive** ( _bool_)


Returns:

True if there is any assets.

Return type:

bool


---

**does_directory_exist**( _directory_path_) → `bool`

Check if a directory exists.

Parameters:

**directory\_path** ( _str_) – Long Path Name of the directory.

Returns:

True if it does exist and it is valid.

Return type:

bool


---

**duplicate_asset**( _source_asset_path_, _destination_asset_path_) → `Object`

Duplicate an asset. Will try to checkout the file. The Asset will be loaded before being duplicated.

Parameters:

- **source\_asset\_path** ( _str_) – Asset Path of the asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the duplicated asset.


Returns:

The duplicated object if the operation succeeds.

Return type:

Object


---

**duplicate_directory**( _source_directory_path_, _destination_directory_path_) → `bool`

Duplicate a directory and the assets in it.
Will try to checkout the files. The Assets will be loaded before being duplicated.

Parameters:

- **source\_directory\_path** ( _str_) – Directory of the assets that we want to duplicate from.

- **destination\_directory\_path** ( _str_) – Directory of the duplicated asset.


Returns:

The duplicated object if the operation succeeds.

Return type:

bool


---

**duplicate_loaded_asset**( _source_asset_, _destination_asset_path_) → `Object`

Duplicate an asset that is already loaded. Will try to checkout the file.

Parameters:

- **source\_asset** ( _Object_) – Asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the duplicated asset.


Returns:

The duplicated object if the operation succeeds

Return type:

Object


---

**find_asset_data**( _asset_path_) → `AssetData`

Return the AssetData for the Asset that can then be used with AssetRegistryHelpers.

Parameters:

**asset\_path** ( _str_) – Asset Path to retrieve data from.

Returns:

The AssetData found.

Return type:

AssetData


---

**find_package_referencers_for_asset**( _asset_path_, _load_assets_to_confirm=False_) → `Array\ [str]`

Find Package Referencers for an asset. Only Soft and Hard dependencies will be looked for.
Soft are dependencies which don’t need to be loaded for the object to be used.
Hard are dependencies which are required for correct usage of the source asset and must be loaded at the same time.
Other references may exist. The asset may be currently used in memory by another asset, by the editor or by code.
Package dependencies are cached with the asset. False positives can happen until all the assets are loaded and re-saved.

Parameters:

- **asset\_path** ( _str_) – Asset Path of the asset that we are looking for.

- **load\_assets\_to\_confirm** ( _bool_) – Whether the asset and any potential referencers will be loaded to confirm the dependencies.


Returns:

The package paths of the referencers.

Return type:

Array\ [str]


---

**get_all_assets_by_meta_data_tags**( _required_tags_, _allowed_classes_) → `Array\ [AssetData]`

Gets all assets which have the given tags.
params: RequiredTags The tags the assets should have
params: AllowedClasses The class types the contained assets should have

Parameters:

- **required\_tags** ( _Set_ _\_ [_Name_ _]_)

- **allowed\_classes** ( _Set_ _\_ [_type_ _(_ _Class_ _)_ _]_)


Return type:

Array\ [AssetData]


---

**get_asset_filename_length_for_cooking**( _asset_path_) → `int32`

Returns the length of the computed cooked package name and path

Parameters:

**asset\_path** ( _str_)

Return type:

int32


---

**get_loaded_asset_filename_length_for_cooking**( _asset_) → `int32`

Returns the length of the computed cooked package name and path

Parameters:

**asset** ( _Object_)

Return type:

int32


---

**get_metadata_tag**( _object_, _tag_) → `str`

Get the value associated with the given tag of a loaded asset’s metadata.

Parameters:

- **object** ( _Object_) – The object from which to retrieve the metadata.

- **tag** ( _Name_) – The tag to find in the metadata.


Returns:

The string value associated with the tag.

Return type:

str


---

**get_metadata_tag_values**( _object_) → `Map\ [Name, str]`

Get all tags/values of a loaded asset’s metadata.

Parameters:

**object** ( _Object_) – The object from which to retrieve the metadata.

Returns:

The list of all Tags and Values.

Return type:

Map\ [Name, str]


---

**get_path_name_for_loaded_asset**( _loaded_asset_) → `str`

Return a valid AssetPath for a loaded asset.
Similar to GetPathName(). The format will be: /Game/MyFolder/MyAsset.MyAsset

Parameters:

**loaded\_asset** ( _Object_) – The loaded asset to get the path of.

Returns:

If valid, the asset Path of the loaded asset.

Return type:

str


---

**get_tag_values**( _asset_path_) → `Map\ [Name, str]`

Gets all TagValues (from Asset Registry) associated with an (unloaded) asset as strings value.

Parameters:

**asset\_path** ( _str_) – Asset Path we are trying to find.

Returns:

The list of all TagNames & TagValues.

Return type:

Map\ [Name, str]


---

**list_assets**( _directory_path_, _recursive=True_, _include_folder=False_) → `Array\ [str]`

Return the list of all the assets found in the DirectoryPath.

Parameters:

- **directory\_path** ( _str_) – Directory path of the asset we want the list from.

- **recursive** ( _bool_) – The search will be recursive and will look in sub folders.

- **include\_folder** ( _bool_) – The result will include folders name.


Returns:

The list of assets found.

Return type:

Array\ [str]


---

**list_assets_by_tag_value**( _tag_name_, _tag_value_) → `Array\ [str]`

Return the list of all the assets that have the pair of Tag/Value.

Parameters:

- **tag\_name** ( _Name_) – The tag associated with the assets requested.

- **tag\_value** ( _str_) – The value associated with the assets requested.


Returns:

The list of assets found.

Return type:

Array\ [str]


---

**load_asset**( _asset_path_) → `Object`

Load an asset. It will verify if the object is already loaded and only load it if it’s necessary.

Parameters:

**asset\_path** ( _str_) – Asset Path of the asset to load

Returns:

Found or loaded asset.

Return type:

Object

load\_blueprint\_class( _asset\_path_)

Load a Blueprint asset and return its generated class. It will verify if the object is already loaded and only load it if it’s necessary.

Parameters:

**asset\_path** ( _str_) – Asset Path of the Blueprint asset.

Returns:

Found or loaded class.

Return type:

type( Class)


---

**make_directory**( _directory_path_) → `bool`

Create a directory on disk.

Parameters:

**directory\_path** ( _str_) – Long Path Name of the directory.

Returns:

True if the operation succeeds.

Return type:

bool


---

**remove_metadata_tag**( _object_, _tag_) → `None`

Remove the given tag from a loaded asset’s metadata.

Parameters:

- **object** ( _Object_) – The object from which to retrieve the metadata.

- **tag** ( _Name_) – The tag to remove from the metadata.



---

**remove_on_extract_asset_from_file**( _delegate_) → `None`

Call this to remove a callback added with AddOnExtractAssetFromFile.

Parameters:

**delegate** ( _OnExtractAssetFromFileDynamic_)


---

**rename_asset**( _source_asset_path_, _destination_asset_path_) → `bool`

Rename an asset. Equivalent to a Move operation.
Will try to checkout the file. The Asset will be loaded before being renamed.

Parameters:

- **source\_asset\_path** ( _str_) – Asset Path of the asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the renamed asset.


Returns:

True if the operation succeeds.

Return type:

bool


---

**rename_directory**( _source_directory_path_, _destination_directory_path_) → `bool`

Rename a directory. Equivalent to a Move operation moving all contained assets.
Will try to checkout the files. The Assets will be loaded before being renamed.

Parameters:

- **source\_directory\_path** ( _str_) – Directory of the assets that we want to rename from.

- **destination\_directory\_path** ( _str_) – Directory of the renamed asset.


Returns:

True if the operation succeeds.

Return type:

bool


---

**rename_loaded_asset**( _source_asset_, _destination_asset_path_) → `bool`

Rename an asset that is already loaded. Equivalent to a Move operation.
Will try to checkout the file.

Parameters:

- **source\_asset** ( _Object_) – Asset that we want to copy from.

- **destination\_asset\_path** ( _str_) – Asset Path of the duplicated asset.


Returns:

True if the operation succeeds.

Return type:

bool


---

**save_asset**( _asset_to_save_, _only_if_is_dirty=True_) → `bool`

Save the packages the assets live in. All objects that live in the package will be saved.
Will try to checkout the file first. The Asset will be loaded before being saved.

Parameters:

- **asset\_to\_save** ( _str_) – Asset Path of the asset that we want to save.

- **only\_if\_is\_dirty** ( _bool_) – Only checkout/save the asset if it’s dirty.


Returns:

True if the operation succeeds.

Return type:

bool


---

**save_directory**( _directory_path_, _only_if_is_dirty=True_, _recursive=True_) → `bool`

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

**save_loaded_asset**( _asset_to_save_, _only_if_is_dirty=True_) → `bool`

Save the package the asset lives in. All objects that live in the package will be saved. Will try to checkout the file.

Parameters:

- **asset\_to\_save** ( _Object_) – Asset that we want to save.

- **only\_if\_is\_dirty** ( _bool_) – Only checkout asset that are dirty.


Returns:

True if the operation succeeds.

Return type:

bool


---

**save_loaded_assets**( _assets_to_save_, _only_if_is_dirty=True_) → `bool`

Save the packages the assets live in. All objects that live in the packages will be saved. Will try to checkout the files.

Parameters:

- **assets\_to\_save** ( _Array_ _\_ [_Object_ _]_) – Assets that we want to save.

- **only\_if\_is\_dirty** ( _bool_) – Only checkout asset that are dirty.


Returns:

True if the operation succeeds.

Return type:

bool


---

**set_dirty_flag**( _object_, _dirty_state_) → `bool`

Set the package dirty flag for an asset

Parameters:

- **object** ( _Object_) – Object we want to set the package dirty state.

- **dirty\_state** ( _bool_) – The dirty state, true mean the asset package need to be save.


Returns:

True if the operation succeeds.

Return type:

bool


---

**set_metadata_tag**( _object_, _tag_, _value_) → `None`

Set the value associated with a given tag of a loaded asset’s metadata.

Parameters:

- **object** ( _Object_) – The object from which to retrieve the metadata.

- **tag** ( _Name_) – The tag to set in the metadata.

- **value** ( _str_) – The string value to associate with the tag.



---

**sort_by_meta_data**( _assets_, _meta_data_tag_, _meta_data_type_, _sort_order_) → `Array[AssetData]orNone`

Sorts the assets based on their meta data’s type.
Supported types: FString, int, float, FDateTime.

Parameters:

- **assets** ( _Array_ _\_ [_AssetData_ _]_) – The assets to sort

- **meta\_data\_tag** ( _Name_) – The on which the sort is based

- **meta\_data\_type** ( _EditorAssetMetaDataSortType_) – The meta data type of MetaDataTag

- **sort\_order** ( _EditorAssetSortOrder_) – Whether to sort ascending or descending


Returns:

Whether the data was sorted, e.g. false if not all assets have the MetaDataTag.

assets (Array[AssetData]): The assets to sort

Return type:

Array\ [AssetData] or None

### Table of Contents

- `unreal.EditorAssetSubsystem`
  - `EditorAssetSubsystem`
    - `EditorAssetSubsystem.add_on_extract_asset_from_file()`
    - `EditorAssetSubsystem.checkout_asset()`
    - `EditorAssetSubsystem.checkout_directory()`
    - `EditorAssetSubsystem.checkout_loaded_asset()`
    - `EditorAssetSubsystem.checkout_loaded_assets()`
    - `EditorAssetSubsystem.consolidate_assets()`
    - `EditorAssetSubsystem.delete_asset()`
    - `EditorAssetSubsystem.delete_directory()`
    - `EditorAssetSubsystem.delete_loaded_asset()`
    - `EditorAssetSubsystem.delete_loaded_assets()`
    - `EditorAssetSubsystem.do_assets_exist()`
    - `EditorAssetSubsystem.does_asset_exist()`
    - `EditorAssetSubsystem.does_directory_contain_assets()`
    - `EditorAssetSubsystem.does_directory_exist()`
    - `EditorAssetSubsystem.duplicate_asset()`
    - `EditorAssetSubsystem.duplicate_directory()`
    - `EditorAssetSubsystem.duplicate_loaded_asset()`
    - `EditorAssetSubsystem.find_asset_data()`
    - `EditorAssetSubsystem.find_package_referencers_for_asset()`
    - `EditorAssetSubsystem.get_all_assets_by_meta_data_tags()`
    - `EditorAssetSubsystem.get_asset_filename_length_for_cooking()`
    - `EditorAssetSubsystem.get_loaded_asset_filename_length_for_cooking()`
    - `EditorAssetSubsystem.get_metadata_tag()`
    - `EditorAssetSubsystem.get_metadata_tag_values()`
    - `EditorAssetSubsystem.get_path_name_for_loaded_asset()`
    - `EditorAssetSubsystem.get_tag_values()`
    - `EditorAssetSubsystem.list_assets()`
    - `EditorAssetSubsystem.list_assets_by_tag_value()`
    - `EditorAssetSubsystem.load_asset()`
    - `EditorAssetSubsystem.load_blueprint_class()`
    - `EditorAssetSubsystem.make_directory()`
    - `EditorAssetSubsystem.remove_metadata_tag()`
    - `EditorAssetSubsystem.remove_on_extract_asset_from_file()`
    - `EditorAssetSubsystem.rename_asset()`
    - `EditorAssetSubsystem.rename_directory()`
    - `EditorAssetSubsystem.rename_loaded_asset()`
    - `EditorAssetSubsystem.save_asset()`
    - `EditorAssetSubsystem.save_directory()`
    - `EditorAssetSubsystem.save_loaded_asset()`
    - `EditorAssetSubsystem.save_loaded_assets()`
    - `EditorAssetSubsystem.set_dirty_flag()`
    - `EditorAssetSubsystem.set_metadata_tag()`
    - `EditorAssetSubsystem.sort_by_meta_data()`