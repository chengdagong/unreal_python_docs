# unreal.AssetData

```python
class unreal.AssetData(package_name:Name='None', package_path:Name='None', asset_name:Name='None', asset_class_path:TopLevelAssetPath=Ellipsis)
```


**Bases:** ``StructBase``


A struct to hold important information about an assets found by the Asset Registry
This struct is transient and should never be serialized

**C++ Source:**

- **Module**: CoreUObject

- **File**: AssetData.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_class` (Name): [Read-Write]
deprecated: Short asset class name must be converted to full asset pathname. Use AssetClassPath instead.

- `asset_class_path` (TopLevelAssetPath): [Read-Write] The path of the asset’s class, e.g. /Script/Engine.StaticMesh

- `asset_name` (Name): [Read-Write] The name of the asset without the package

- `package_name` (Name): [Read-Write] The name of the package in which the asset is found, this is the full long package name such as /Game/Path/Package

- `package_path` (Name): [Read-Write] The path to the package in which the asset is found, this is /Game/Path with the Package stripped off



---

_property_ `asset_class`: Name

[Read-Only]
deprecated: Short asset class name must be converted to full asset pathname. Use AssetClassPath instead.

**Type:**

( Name)


---

_property_ `asset_class_path`: TopLevelAssetPath

[Read-Only] The path of the asset’s class, e.g. /Script/Engine.StaticMesh

**Type:**

( TopLevelAssetPath)


---

_property_ `asset_name`: Name

[Read-Only] The name of the asset without the package

**Type:**

( Name)

find\_asset\_native\_class()

Returns the first native class of the asset type that can be found. Normally this is just the FAssetData::GetClass(),
however if the class is a blueprint generated class it may not be loaded. In which case GetAncestorClassNames will
be used to find the first native super class. This can be slow if temporary caching mode is not on.

Return type:

type( Class)


---

**get_asset**() → `Object`

Returns the asset UObject if it is loaded or loads the asset if it is unloaded then returns the result

Return type:

Object

get\_class()

Get Class

Return type:

type( Class)


---

**get_export_text_name**() → `str`

Returns the name for the asset in the form: Class’ObjectPath’

Return type:

str


---

**get_full_name**() → `str`

Returns the full name for the asset in the form: Class ObjectPath

Return type:

str


---

**get_tag_value**( _tag_name_) → `strorNone`

Gets the value associated with the given tag as a string

Parameters:

**tag\_name** ( _Name_)

Returns:

out\_tag\_value (str):

Return type:

str or None


---

**has_editor_only_data**() → `bool`

Returns true if the asset has its editor-only data

Return type:

bool


---

**is_asset_loaded**() → `bool`

Returns true if the asset is loaded

Return type:

bool


---

**is_cooked**() → `bool`

Returns true if the asset is cooked

Return type:

bool


---

**is_redirector**() → `bool`

Returns true if the this asset is a redirector.

Return type:

bool


---

**is_u_asset**() → `bool`

Returns true if this is the primary asset in a package, true for maps and assets but false for secondary objects like class redirectors

Return type:

bool


---

**is_valid**() → `bool`

Checks to see if this AssetData refers to an asset or is NULL

Return type:

bool


---

_property_ `package_name`: Name

[Read-Only] The name of the package in which the asset is found, this is the full long package name such as /Game/Path/Package

**Type:**

( Name)


---

_property_ `package_path`: Name

[Read-Only] The path to the package in which the asset is found, this is /Game/Path with the Package stripped off

**Type:**

( Name)


---

**to_soft_object_path**() → `SoftObjectPath`

Convert to a SoftObjectPath for loading

Return type:

SoftObjectPath

### Table of Contents

- `unreal.AssetData`
  - `AssetData`
    - `AssetData.asset_class`
    - `AssetData.asset_class_path`
    - `AssetData.asset_name`
    - `AssetData.find_asset_native_class()`
    - `AssetData.get_asset()`
    - `AssetData.get_class()`
    - `AssetData.get_export_text_name()`
    - `AssetData.get_full_name()`
    - `AssetData.get_tag_value()`
    - `AssetData.has_editor_only_data()`
    - `AssetData.is_asset_loaded()`
    - `AssetData.is_cooked()`
    - `AssetData.is_redirector()`
    - `AssetData.is_u_asset()`
    - `AssetData.is_valid()`
    - `AssetData.package_name`
    - `AssetData.package_path`
    - `AssetData.to_soft_object_path()`