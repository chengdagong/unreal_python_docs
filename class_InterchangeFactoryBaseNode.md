# unreal.InterchangeFactoryBaseNode

```python
class unreal.InterchangeFactoryBaseNode(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``InterchangeBaseNode``


This struct is used to store and retrieve key-value attributes. The attributes are stored in a generic FAttributeStorage that serializes the values in a TArray64<uint8>.
See UE::Interchange::EAttributeTypes to know the supported template types.
This is an abstract class. This is the base class of the Interchange node graph format; all classes in this format should derive from this class.

**C++ Source:**

- **Module**: InterchangeCore

- **File**: InterchangeFactoryBaseNode.h



---

**add_factory_dependency_uid**( _dependency_uid_) → `bool`

Add one dependency to this object.

Parameters:

**dependency\_uid** ( _str_)

Return type:

bool


---

**get_custom_level_uid**() → `strorNone`

If this node represent a scene asset (actor), return a specific level in which we will create this scene asset.

Returns:

attribute\_value (str):

Return type:

str or None


---

**get_custom_reference_object**() → `SoftObjectPathorNone`

Return the custom ReferenceObject: the UObject this factory node has created.

Returns:

attribute\_value (SoftObjectPath):

Return type:

SoftObjectPath or None


---

**get_custom_sub_path**() → `strorNone`

Return the custom sub-path under PackageBasePath where the assets will be created.

Returns:

attribute\_value (str):

Return type:

str or None


---

**get_factory_dependencies**() → `Array\ [str]`

Retrieve the dependencies for this object.

Returns:

out\_dependencies (Array[str]):

Return type:

Array\ [str]


---

**get_factory_dependencies_count**() → `int32`

Retrieve the number of factory dependencies for this object.

Return type:

int32


---

**get_factory_dependency**( _index_) → `str`

Retrieve one dependency for this object.

Parameters:

**index** ( _int32_)

Returns:

out\_dependency (str):

Return type:

str

get\_object\_class()

Return the UClass of the object we represent, so we can find the factory/writer.

Return type:

type( Class)


---

**get_reimport_strategy_flags**() → `ReimportStrategyFlags`

Return the reimport strategy flags.

Return type:

ReimportStrategyFlags


---

**is_runtime_import_allowed**() → `bool`

Return if the import of the class is allowed at runtime.

Return type:

bool


---

**remove_factory_dependency_uid**( _dependency_uid_) → `bool`

Remove one dependency from this object.

Parameters:

**dependency\_uid** ( _str_)

Return type:

bool


---

**set_custom_level_uid**( _attribute_value_) → `bool`

If this node represent a scene asset (actor), you can set a specific level in which we will create this scene asset.

Parameters:

**attribute\_value** ( _str_)

Return type:

bool


---

**set_custom_reference_object**( _attribute_value_) → `bool`

Set the custom ReferenceObject: the UObject this factory node has created.

Parameters:

**attribute\_value** ( _SoftObjectPath_)

Return type:

bool


---

**set_custom_sub_path**( _attribute_value_) → `bool`

Set the custom sub-path under PackageBasePath where the assets will be created.

Parameters:

**attribute\_value** ( _str_)

Return type:

bool


---

**set_force_node_reimport**() → `bool`

Allow the creation of the Unreal object even if it has been previously deleted in the editor.

Return type:

bool


---

**set_reimport_strategy_flags**( _reimport_strategy_flags_) → `bool`

Change the reimport strategy flags.

Parameters:

**reimport\_strategy\_flags** ( _ReimportStrategyFlags_)

Return type:

bool


---

**set_skip_node_import**() → `bool`

Add the skip node attribute. Use this function to cancel the creation of the Unreal asset. See ShouldSkipNodeImport for more documentation.

Return type:

bool


---

**should_force_node_reimport**() → `bool`

Return whether or not an object should be created even if it has been deleted in the editor.
Return false by default.

Return type:

bool


---

**should_skip_node_import**() → `bool`

Return true if this node should skip the factory import process, or false otherwise.
Nodes can be in a situation where we have to skip the import process because we cannot import the associated asset for multiple reasons. For example:
\- An asset can already exist and represents a different type (UClass).
\- An asset can already exist and is being compiled.
\- An asset can already exist and is being imported by another concurrent import task (such as a user importing multiple files at the same time in the same content folder).

Return type:

bool


---

**unset_force_node_reimport**() → `bool`

Disallow the creation of the Unreal object if it has been previously deleted in the editor.

Return type:

bool


---

**unset_skip_node_import**() → `bool`

Remove the skip node attribute. See ShouldSkipNodeImport for more documentation.

Return type:

bool

### Table of Contents

- `unreal.InterchangeFactoryBaseNode`
  - `InterchangeFactoryBaseNode`
    - `InterchangeFactoryBaseNode.add_factory_dependency_uid()`
    - `InterchangeFactoryBaseNode.get_custom_level_uid()`
    - `InterchangeFactoryBaseNode.get_custom_reference_object()`
    - `InterchangeFactoryBaseNode.get_custom_sub_path()`
    - `InterchangeFactoryBaseNode.get_factory_dependencies()`
    - `InterchangeFactoryBaseNode.get_factory_dependencies_count()`
    - `InterchangeFactoryBaseNode.get_factory_dependency()`
    - `InterchangeFactoryBaseNode.get_object_class()`
    - `InterchangeFactoryBaseNode.get_reimport_strategy_flags()`
    - `InterchangeFactoryBaseNode.is_runtime_import_allowed()`
    - `InterchangeFactoryBaseNode.remove_factory_dependency_uid()`
    - `InterchangeFactoryBaseNode.set_custom_level_uid()`
    - `InterchangeFactoryBaseNode.set_custom_reference_object()`
    - `InterchangeFactoryBaseNode.set_custom_sub_path()`
    - `InterchangeFactoryBaseNode.set_force_node_reimport()`
    - `InterchangeFactoryBaseNode.set_reimport_strategy_flags()`
    - `InterchangeFactoryBaseNode.set_skip_node_import()`
    - `InterchangeFactoryBaseNode.should_force_node_reimport()`
    - `InterchangeFactoryBaseNode.should_skip_node_import()`
    - `InterchangeFactoryBaseNode.unset_force_node_reimport()`
    - `InterchangeFactoryBaseNode.unset_skip_node_import()`