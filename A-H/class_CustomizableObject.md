# unreal.CustomizableObject

```python
class unreal.CustomizableObject(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


Customizable Object

**C++ Source:**

- **Plugin**: Mutable

- **Module**: CustomizableObject

- **File**: CustomizableObject.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `disable_table_materials_parent_check` (bool): [Read-Write] Disabling the Table Materials parent material check will let the user use any material regardless of its parent when connecting a material from a table column to a material node.
Warning! But it will not check if the table material channels connected to the Material node exist in the actual material used in the Instance, and will fail silently at runtime
when setting the value of those channels if they don’t exist.

- `enable16_bit_bone_weights` (bool): [Read-Write]

- `enable_alt_skin_weight_profiles` (bool): [Read-Write]

- `enable_anim_bp_physics_assets_manipulation` (bool): [Read-Write] Experimental

- `enable_asset_user_data_merge` (bool): [Read-Write] When this is enabled generated meshes will merge the AssetUserData from all of its constituent mesh parts

- `enable_clothing` (bool): [Read-Write]

- `enable_mesh_cache` (bool): [Read-Write] If true, reuse previously generated USkeletalMesh (if still valid and the the number of LOD have not changed)
USkeletalMeshes are only reused between the same CO.

- `enable_mesh_streaming` (bool): [Read-Write] If true, Mesh LODs will be streamed on demand. It requires streaming of SkeletalMeshes and Mutable.StreamMeshLODsEnabled to be enabled.

- `enable_physics_asset_merge` (bool): [Read-Write]

- `enable_real_time_morph_targets` (bool): [Read-Write]

- `enable_use_ref_skeletal_mesh_as_placeholder` (bool): [Read-Write] true to use the Reference Skeletal Mesh as a placeholder while the Generated Skeletal Mesh is not ready.
If false, a null mesh will be used to replace the discarded mesh due to ‘ReplaceDiscardedWithReferenceMesh’ being enabled.

- `lod_settings` (MutableLODSettings): [Read-Write]
deprecated: Moved to Mesh Component Node

- `low_priority_textures` (Array[Name]): [Read-Write] Textures marked as low priority will generate defaulted resident mips (if texture streaming is enabled).
Generating defaulted resident mips greatly reduce initial generation times.

- `mesh_compile_type` (MutableCompileMeshType): [Read-Write] Options when compiling this customizable object (see EMutableCompileMeshType declaration for info)

- `preserve_user_lo_ds_on_first_generation` (bool): [Read-Write] Use the Instance MinLOD, and RequestedLODs in the descriptor when performing the initial generation (ignore LOD Management).

- `version_bridge` (Object): [Read-Write] Optional Version Bridge asset.

Used to decide which Mutable child Customizable Objects and Data Table rows must be included in a compilation/cook.
An asset will be included if the struct/column version matches the game-specific system version.

The provided asset must implement ICustomizableObjectVersionBridgeInterface.

- `version_struct` (InstancedStruct): [Read-Write] Optional struct.

Used to define which version this child Customizable Object belongs to. It will be used during
cook/compilation to decide whether this Customizable Object should be included in the final compiled Customizable Object.

To work, the root Customizable Object must have a Version Bridge.

- `working_set` (Array[CustomizableObject]): [Read-Write] Array of elements to use with compile option CompileType = WorkingSet



---

**compile**( _params_) → `None`

Compile the Customizable Object.

Parameters:

**params** ( _CompileParams_)


---

**contains_enum_parameter_value**( _parameter_name_, _value_) → `bool`

Return true if the enum parameter contains this value a possible option.

Parameters:

- **parameter\_name** ( _str_)

- **value** ( _str_)


Return type:

bool


---

**contains_parameter**( _parameter_name_) → `bool`

Contains Parameter

Parameters:

**parameter\_name** ( _str_)

Return type:

bool


---

**create_instance**() → `CustomizableObjectInstance`

Create a new instance of this object. The instance parameters will be initialized with the object default values.

Return type:

CustomizableObjectInstance


---

**get_bool_parameter_default_value**( _parameter_name_) → `bool`

Get the default value of a parameter of type Bool.

Parameters:

**parameter\_name** ( _str_) – The name of the Bool parameter to get the default value of.

Returns:

The default value of the provided parameter name.

Return type:

bool


---

**get_color_parameter_default_value**( _parameter_name_) → `LinearColor`

Get the default value of a parameter of type Color.

Parameters:

**parameter\_name** ( _str_) – The name of the Color parameter to get the default value of.

Returns:

The default value of the provided parameter name.

Return type:

LinearColor


---

**get_component_count**() → `int32`

Get the number of components this Customizable Object has.

Return type:

int32


---

**get_component_mesh_reference_skeletal_mesh**( _name_) → `SkeletalMesh`

DEPRECATED: Use GetSkeletalMeshComponentReferenceSkeletalMesh instead.

Parameters:

**name** ( _Name_)

Return type:

SkeletalMesh


---

**get_component_name**( _component_index_) → `Name`

Return the name of the component.

Parameters:

**component\_index** ( _int32_) – [0 - GetComponentCount). Index may not represent the same component between runs. To identify them use the name.\
\
Returns:\
\
NAME\_None if the component does not exist.\
\
Return type:\
\
Name\
\

---

**get_enum_parameter_default_value**( _parameter_name_) → `int32\`
\
Get the default value of a parameter of type Int.\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the Int parameter to get the default value of.\
\
Returns:\
\
The default value of the provided parameter name.\
\
Return type:\
\
int32\
\

---

**get_enum_parameter_group_type**( _param_name_) → `CustomizableObjectGroupType\`
\
Returns the group type of the given integer parameter\
\
Parameters:\
\
**param\_name** ( _str_)\
\
Return type:\
\
CustomizableObjectGroupType\
\

---

**get_enum_parameter_num_values**( _parameter_name_) → `int32\`
\
If the given parameter is enum int parameter, return how many possible values an enum parameter has. Otherwise, return 0.\
\
Parameters:\
\
**parameter\_name** ( _str_)\
\
Return type:\
\
int32\
\

---

**get_enum_parameter_value**( _parameter_name_, _value_index_) → `str\`
\
Gets the Name of the value at position ValueIndex in the list of available values for the int parameter.\
\
Parameters:\
\
- **parameter\_name** ( _str_)\
\
- **value\_index** ( _int32_)\
\
\
Return type:\
\
str\
\

---

**get_enum_parameter_value_data_table**( _param_name_, _value_) → `Array\ [DataTable]\`
\
Return the DataTables used by the given parameter and its value (if any).\
\
Parameters:\
\
- **param\_name** ( _str_)\
\
- **value** ( _str_)\
\
\
Return type:\
\
Array\ [DataTable]\
\

---

**get_enum_parameter_value_ui_metadata**( _param_name_, _option_name_) → `MutableParamUIMetadata\`
\
Return the metadata associated to the given enum parameter value.\
\
Parameters:\
\
- **param\_name** ( _str_)\
\
- **option\_name** ( _str_)\
\
\
Return type:\
\
MutableParamUIMetadata\
\

---

**get_float_parameter_default_value**( _parameter_name_) → `float\`
\
Get the default value of a parameter of type Float.\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the Float parameter to get the default value of.\
\
Returns:\
\
The default value of the provided parameter name.\
\
Return type:\
\
float\
\

---

**get_int_parameter_default_value**( _parameter_name:str_) → `int\`
\
deprecated: ‘get\_int\_parameter\_default\_value’ was renamed to ‘get\_enum\_parameter\_default\_value’.\
\

---

**get_int_parameter_group_type**( _param_name:str_) → `CustomizableObjectGroupType\`
\
deprecated: ‘get\_int\_parameter\_group\_type’ was renamed to ‘get\_enum\_parameter\_group\_type’.\
\

---

**get_int_parameter_option_data_table**( _param_name:str_, _value:str_) → `None\`
\
deprecated: ‘get\_int\_parameter\_option\_data\_table’ was renamed to ‘get\_enum\_parameter\_value\_data\_table’.\
\

---

**get_int_parameter_option_ui_metadata**( _param_name:str_, _option_name:str_) → `MutableParamUIMetadata\`
\
deprecated: ‘get\_int\_parameter\_option\_ui\_metadata’ was renamed to ‘get\_enum\_parameter\_value\_ui\_metadata’.\
\

---

**get_material_parameter_default_value**( _parameter_name_) → `MaterialInterface\`
\
Get the default value of a parameter of type Material.\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the Material parameter to get the default value of.\
\
Return type:\
\
MaterialInterface\
\

---

**get_parameter_count**() → `int32\`
\
Get the number of parameters available in instances of this object.\
\
Return type:\
\
int32\
\

---

**get_parameter_name**( _param_index_) → `str\`
\
TODO >5.6 rename to GetParameterType (with redirector). Name -> ParameterName (create redirector)\
\
Parameters:\
\
**param\_index** ( _int32_)\
\
Return type:\
\
str\
\

---

**get_parameter_type_by_name**( _name_) → `MutableParameterType\`
\
Get the type of a parameter from its name.\
\
Parameters:\
\
**name** ( _str_)\
\
Return type:\
\
MutableParameterType\
\

---

**get_parameter_ui_metadata**( _param_name_) → `MutableParamUIMetadata\`
\
Return the metadata associated to a parameter.\
\
Parameters:\
\
**param\_name** ( _str_)\
\
Return type:\
\
MutableParamUIMetadata\
\

---

**get_projector_parameter_default_value**( _parameter_name_) → `CustomizableObjectProjector\`
\
Get the default value of a projector with the provided name\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the parameter to get the default value of.\
\
Returns:\
\
A data structure containing all the default data for the targeted projector parameter.\
\
Return type:\
\
CustomizableObjectProjector\
\

---

**get_skeletal_mesh_component_reference_skeletal_mesh**( _component_name_) → `SkeletalMesh\`
\
Given a Mesh Component name, return its reference Skeletal Mesh.\
\
Parameters:\
\
**component\_name** ( _Name_)\
\
Return type:\
\
SkeletalMesh\
\

---

**get_skeletal_mesh_parameter_default_value**( _parameter_name_) → `SkeletalMesh\`
\
Get the default value of a parameter of type Skeletal Mesh.\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the Mesh parameter to get the default value of.\
\
Return type:\
\
SkeletalMesh\
\

---

**get_state_count**() → `int32\`
\
Return the number of object states that are defined in the CustomizableObject.\
\
Return type:\
\
int32\
\

---

**get_state_name**( _state_index_) → `str\`
\
Get State Name\
\
Parameters:\
\
**state\_index** ( _int32_)\
\
Return type:\
\
str\
\

---

**get_state_parameter_count**( _state_name_) → `int32\`
\
Return the number of parameters that are editable at runtime for a specific state.\
\
Parameters:\
\
**state\_name** ( _str_)\
\
Return type:\
\
int32\
\

---

**get_state_parameter_name**( _state_name_, _parameter_index_) → `str\`
\
Return the name of one of the state’s runtime parameters, by its index (from 0 to GetStateParameterCount - 1).\
\
Parameters:\
\
- **state\_name** ( _str_)\
\
- **parameter\_index** ( _int32_)\
\
\
Return type:\
\
str\
\

---

**get_state_ui_metadata**( _state_name_) → `MutableStateUIMetadata\`
\
Return the metadata associated to a state.\
\
Parameters:\
\
**state\_name** ( _str_)\
\
Return type:\
\
MutableStateUIMetadata\
\

---

**get_texture_parameter_default_value**( _parameter_name_) → `Texture\`
\
Get the default value of a parameter of type Texture.\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the Texture parameter to get the default value of.\
\
Return type:\
\
Texture\
\

---

**get_transform_parameter_default_value**( _parameter_name_) → `Transform\`
\
Get the default value of a parameter of type Transform.\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the Transform parameter to get the default value of.\
\
Returns:\
\
The default value of the provided parameter name.\
\
Return type:\
\
Transform\
\

---

**is_child_object**() → `bool\`
\
Return true if this Customizable Object has references to a parent Customizable Object. Only root Customizable Objects will return false.\
\
Return type:\
\
bool\
\

---

**is_compiled**() → `bool\`
\
Check if the CustomizableObject asset has been compiled. This will always be true in a packaged game, but it could be false in the editor.\
It may return false due to the Customizable Object still being loaded.\
\
Return type:\
\
bool\
\

---

**is_loading**() → `bool\`
\
Return true if the Customizable Object is still being loaded. It may take a few frames to load the Customizable Object.\
\
Return type:\
\
bool\
\

---

**is_parameter_multidimensional**( _parameter_name_) → `bool\`
\
Return true if the parameter at the index provided is multidimensional.\
\
Parameters:\
\
**parameter\_name** ( _str_) – The name of the parameter to check.\
\
Returns:\
\
True if the parameter is multidimensional and false if it is not.\
\
Return type:\
\
bool\
\

---

_property_ `lod_settings`: MutableLODSettings
\
[Read-Write]\
deprecated: Moved to Mesh Component Node\
\
Type:\
\
( MutableLODSettings)\
\
### Table of Contents\
\
- `unreal.CustomizableObject`\
  - `CustomizableObject`\
    - `CustomizableObject.compile()`\
    - `CustomizableObject.contains_enum_parameter_value()`\
    - `CustomizableObject.contains_parameter()`\
    - `CustomizableObject.create_instance()`\
    - `CustomizableObject.get_bool_parameter_default_value()`\
    - `CustomizableObject.get_color_parameter_default_value()`\
    - `CustomizableObject.get_component_count()`\
    - `CustomizableObject.get_component_mesh_reference_skeletal_mesh()`\
    - `CustomizableObject.get_component_name()`\
    - `CustomizableObject.get_enum_parameter_default_value()`\
    - `CustomizableObject.get_enum_parameter_group_type()`\
    - `CustomizableObject.get_enum_parameter_num_values()`\
    - `CustomizableObject.get_enum_parameter_value()`\
    - `CustomizableObject.get_enum_parameter_value_data_table()`\
    - `CustomizableObject.get_enum_parameter_value_ui_metadata()`\
    - `CustomizableObject.get_float_parameter_default_value()`\
    - `CustomizableObject.get_int_parameter_default_value()`\
    - `CustomizableObject.get_int_parameter_group_type()`\
    - `CustomizableObject.get_int_parameter_option_data_table()`\
    - `CustomizableObject.get_int_parameter_option_ui_metadata()`\
    - `CustomizableObject.get_material_parameter_default_value()`\
    - `CustomizableObject.get_parameter_count()`\
    - `CustomizableObject.get_parameter_name()`\
    - `CustomizableObject.get_parameter_type_by_name()`\
    - `CustomizableObject.get_parameter_ui_metadata()`\
    - `CustomizableObject.get_projector_parameter_default_value()`\
    - `CustomizableObject.get_skeletal_mesh_component_reference_skeletal_mesh()`\
    - `CustomizableObject.get_skeletal_mesh_parameter_default_value()`\
    - `CustomizableObject.get_state_count()`\
    - `CustomizableObject.get_state_name()`\
    - `CustomizableObject.get_state_parameter_count()`\
    - `CustomizableObject.get_state_parameter_name()`\
    - `CustomizableObject.get_state_ui_metadata()`\
    - `CustomizableObject.get_texture_parameter_default_value()`\
    - `CustomizableObject.get_transform_parameter_default_value()`\
    - `CustomizableObject.is_child_object()`\
    - `CustomizableObject.is_compiled()`\
    - `CustomizableObject.is_loading()`\
    - `CustomizableObject.is_parameter_multidimensional()`\
    - `CustomizableObject.lod_settings`\
\