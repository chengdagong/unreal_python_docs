# unreal.MaterialEditingLibrary

```python
class unreal.MaterialEditingLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Blueprint library for creating/editing Materials

**C++ Source:**

- **Module**: MaterialEditor

- **File**: MaterialEditingLibrary.h



---

_classmethod_ clear_all_material_instance_parameters( _instance_)→None

Clears all material parameters set by this Material Instance

Parameters:

**instance** ( _MaterialInstanceConstant_)


---

_classmethod_ connect_material_expressions( _from_expression_, _from_output_name_, _to_expression_, _to_input_name_)→bool

Create connection between two material expressions

Parameters:

- **from\_expression** ( _MaterialExpression_) – Expression to make connection from

- **from\_output\_name** ( _str_) – Name of output of FromExpression to make connection from. Leave empty to use first output.

- **to\_expression** ( _MaterialExpression_) – Expression to make connection to

- **to\_input\_name** ( _str_) – Name of input of ToExpression to make connection to. Leave empty to use first input.


Return type:

bool


---

_classmethod_ connect_material_property( _from_expression_, _from_output_name_, _property__)→bool

Connect a material expression output to one of the material property inputs (e.g. diffuse color, opacity etc)

Parameters:

- **from\_expression** ( _MaterialExpression_) – Expression to make connection from

- **from\_output\_name** ( _str_) – Name of output of FromExpression to make connection from

- **property** ( _MaterialProperty_) – Property input on material to make connection to


Return type:

bool


---

_classmethod_ create_material_expression( _material_, _expression_class_, _node_pos_x=0_, _node_pos_y=0_)→MaterialExpression

Create a new material expression node within the supplied material

Parameters:

- **material** ( _Material_) – Material asset to add an expression to

- **expression\_class** ( _type_ _(_ _Class_ _)_) – Class of expression to add

- **node\_pos\_x** ( _int32_) – X position of new expression node

- **node\_pos\_y** ( _int32_) – Y position of new expression node


Return type:

MaterialExpression


---

_classmethod_ create_material_expression_in_function( _material_function_, _expression_class_, _node_pos_x=0_, _node_pos_y=0_)→MaterialExpression

Create a new material expression node within the supplied material function

Parameters:

- **material\_function** ( _MaterialFunction_) – Material function asset to add an expression to

- **expression\_class** ( _type_ _(_ _Class_ _)_) – Class of expression to add

- **node\_pos\_x** ( _int32_) – X position of new expression node

- **node\_pos\_y** ( _int32_) – Y position of new expression node


Return type:

MaterialExpression


---

_classmethod_ delete_all_material_expressions( _material_)→None

Delete all material expressions in the supplied material

Parameters:

**material** ( _Material_)


---

_classmethod_ delete_all_material_expressions_in_function( _material_function_)→None

Delete all material expressions in the supplied material function

Parameters:

**material\_function** ( _MaterialFunction_)


---

_classmethod_ delete_material_expression( _material_, _expression_)→None

Delete a specific expression from a material. Will disconnect from other expressions.

Parameters:

- **material** ( _Material_)

- **expression** ( _MaterialExpression_)



---

_classmethod_ delete_material_expression_in_function( _material_function_, _expression_)→None

Delete a specific expression from a material function. Will disconnect from other expressions.

Parameters:

- **material\_function** ( _MaterialFunction_)

- **expression** ( _MaterialExpression_)



---

_classmethod_ duplicate_material_expression( _material_, _material_function_, _expression_)→MaterialExpression

Duplicates the provided material expression adding it to the same material / material function, and copying parameters.
Note: Does not duplicate transient properties (Ex: GraphNode).

Parameters:

- **material** ( _Material_) – Material asset to add an expression to

- **material\_function** ( _MaterialFunction_) – Specified if adding an expression to a MaterialFunction, used as Outer for new expression object

- **expression** ( _MaterialExpression_)


Return type:

MaterialExpression


---

_classmethod_ get_child_instances( _parent_)→Array\ [AssetData]

Gets all direct child mat instances

Parameters:

**parent** ( _MaterialInterface_)

Returns:

child\_instances (Array[AssetData]):

Return type:

Array\ [AssetData]


---

_classmethod_ get_input_node_output_name_for_material_expression( _material_expression_, _input_node_)→strorNone

Get the output name of input node connected to MaterialExpression from an active material editor

Parameters:

- **material\_expression** ( _MaterialExpression_)

- **input\_node** ( _MaterialExpression_)


Returns:

output\_name (str):

Return type:

str or None


---

_classmethod_ get_inputs_for_material_expression( _material_, _material_expression_)→Array\ [MaterialExpression]

Get the set of nodes acting as inputs to a node from an active material editor

Parameters:

- **material** ( _Material_)

- **material\_expression** ( _MaterialExpression_)


Return type:

Array\ [MaterialExpression]


---

_classmethod_ get_material_default_scalar_parameter_value( _material_, _parameter_name_)→float

Get the default scalar (float) parameter value from a Material

Parameters:

- **material** ( _Material_)

- **parameter\_name** ( _Name_)


Return type:

float


---

_classmethod_ get_material_default_static_switch_parameter_value( _material_, _parameter_name_)→bool

Get the default static switch parameter value from a Material

Parameters:

- **material** ( _Material_)

- **parameter\_name** ( _Name_)


Return type:

bool


---

_classmethod_ get_material_default_texture_parameter_value( _material_, _parameter_name_)→Texture

Get the default texture parameter value from a Material

Parameters:

- **material** ( _Material_)

- **parameter\_name** ( _Name_)


Return type:

Texture


---

_classmethod_ get_material_default_vector_parameter_value( _material_, _parameter_name_)→LinearColor

Get the default vector parameter value from a Material

Parameters:

- **material** ( _Material_)

- **parameter\_name** ( _Name_)


Return type:

LinearColor


---

_classmethod_ get_material_expression_input_names( _material_expression_)→Array\ [str]

Get the array of input pin names for a material expression

Parameters:

**material\_expression** ( _MaterialExpression_)

Return type:

Array\ [str]


---

_classmethod_ get_material_expression_input_types( _material_expression_)→Array[int32]

Get the array of input pin types for a material expression

Parameters:

**material\_expression** ( _MaterialExpression_)

Return type:

Array[int32]

_classmethod_ get\_material\_expression\_node\_position( _material\_expression)->(node\_pos\_x=int32_, _node\_pos\_y=int32_)

Get the position of the MaterialExpression node.

Parameters:

**material\_expression** ( _MaterialExpression_)

Returns:

node\_pos\_x (int32):

node\_pos\_y (int32):

Return type:

tuple


---

_classmethod_ get_material_instance_runtime_virtual_texture_parameter_value( _instance_, _parameter_name_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→RuntimeVirtualTexture

Get the current texture parameter value from a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **association** ( _MaterialParameterAssociation_)


Return type:

RuntimeVirtualTexture


---

_classmethod_ get_material_instance_scalar_parameter_value( _instance_, _parameter_name_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→float

Get the current scalar (float) parameter value from a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **association** ( _MaterialParameterAssociation_)


Return type:

float


---

_classmethod_ get_material_instance_sparse_volume_texture_parameter_value( _instance_, _parameter_name_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→SparseVolumeTexture

Get the current texture parameter value from a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **association** ( _MaterialParameterAssociation_)


Return type:

SparseVolumeTexture


---

_classmethod_ get_material_instance_static_switch_parameter_value( _instance_, _parameter_name_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→bool

Get the current static switch parameter value from a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **association** ( _MaterialParameterAssociation_)


Return type:

bool


---

_classmethod_ get_material_instance_texture_parameter_value( _instance_, _parameter_name_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→Texture

Get the current texture parameter value from a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **association** ( _MaterialParameterAssociation_)


Return type:

Texture


---

_classmethod_ get_material_instance_vector_parameter_value( _instance_, _parameter_name_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→LinearColor

Get the current vector parameter value from a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **association** ( _MaterialParameterAssociation_)


Return type:

LinearColor


---

_classmethod_ get_material_property_input_node( _material_, _property__)→MaterialExpression

Get the node providing the output for a given material property from an active material editor

Parameters:

- **material** ( _Material_)

- **property** ( _MaterialProperty_)


Return type:

MaterialExpression


---

_classmethod_ get_material_property_input_node_output_name( _material_, _property__)→str

Get the node output name providing the output for a given material property from an active material editor

Parameters:

- **material** ( _Material_)

- **property** ( _MaterialProperty_)


Return type:

str


---

_classmethod_ get_material_selected_nodes( _material_)→Set\ [Object]

Get the set of selected nodes from an active material editor

Parameters:

**material** ( _Material_)

Return type:

Set\ [Object]


---

_classmethod_ get_nanite_override_material( _material_)→MaterialInterface

Returns any nanite override material for the given material

Parameters:

**material** ( _MaterialInterface_)

Return type:

MaterialInterface


---

_classmethod_ get_num_material_expressions( _material_)→int32

Returns number of material expressions in the supplied material

Parameters:

**material** ( _Material_)

Return type:

int32


---

_classmethod_ get_num_material_expressions_in_function( _material_function_)→int32

Returns number of material expressions in the supplied material

Parameters:

**material\_function** ( _MaterialFunction_)

Return type:

int32


---

_classmethod_ get_scalar_parameter_names( _material_)→Array\ [Name]

Gets all scalar parameter names

Parameters:

**material** ( _MaterialInterface_)

Returns:

parameter\_names (Array[Name]):

Return type:

Array\ [Name]


---

_classmethod_ get_scalar_parameter_source( _material_, _parameter_name_)→SoftObjectPathorNone

Returns the path of the asset where the parameter originated, as well as true/false if it was found

Parameters:

- **material** ( _MaterialInterface_) – The material or material instance you want to look up a parameter from

- **parameter\_name** ( _Name_) – The parameter name


Returns:

Whether or not the parameter was found in this material

parameter\_source (SoftObjectPath): The soft object path of the asset the parameter originates in

Return type:

SoftObjectPath or None


---

_classmethod_ get_static_switch_parameter_names( _material_)→Array\ [Name]

Gets all static switch parameter names

Parameters:

**material** ( _MaterialInterface_)

Returns:

parameter\_names (Array[Name]):

Return type:

Array\ [Name]


---

_classmethod_ get_static_switch_parameter_source( _material_, _parameter_name_)→SoftObjectPathorNone

Returns the path of the asset where the parameter originated, as well as true/false if it was found

Parameters:

- **material** ( _MaterialInterface_) – The material or material instance you want to look up a parameter from

- **parameter\_name** ( _Name_) – The parameter name


Returns:

Whether or not the parameter was found in this material

parameter\_source (SoftObjectPath): The soft object path of the asset the parameter originates in

Return type:

SoftObjectPath or None


---

_classmethod_ get_statistics( _material_)→MaterialStatistics

Returns statistics about the given material

Parameters:

**material** ( _MaterialInterface_)

Return type:

MaterialStatistics


---

_classmethod_ get_texture_parameter_names( _material_)→Array\ [Name]

Gets all texture parameter names

Parameters:

**material** ( _MaterialInterface_)

Returns:

parameter\_names (Array[Name]):

Return type:

Array\ [Name]


---

_classmethod_ get_texture_parameter_source( _material_, _parameter_name_)→SoftObjectPathorNone

Returns the path of the asset where the parameter originated, as well as true/false if it was found

Parameters:

- **material** ( _MaterialInterface_) – The material or material instance you want to look up a parameter from

- **parameter\_name** ( _Name_) – The parameter name


Returns:

Whether or not the parameter was found in this material

parameter\_source (SoftObjectPath): The soft object path of the asset the parameter originates in

Return type:

SoftObjectPath or None


---

_classmethod_ get_used_textures( _material_)→Array\ [Texture]

Get the list of textures used by a material

Parameters:

**material** ( _Material_)

Return type:

Array\ [Texture]


---

_classmethod_ get_vector_parameter_names( _material_)→Array\ [Name]

Gets all vector parameter names

Parameters:

**material** ( _MaterialInterface_)

Returns:

parameter\_names (Array[Name]):

Return type:

Array\ [Name]


---

_classmethod_ get_vector_parameter_source( _material_, _parameter_name_)→SoftObjectPathorNone

Returns the path of the asset where the parameter originated, as well as true/false if it was found

Parameters:

- **material** ( _MaterialInterface_) – The material or material instance you want to look up a parameter from

- **parameter\_name** ( _Name_) – The parameter name


Returns:

Whether or not the parameter was found in this material

parameter\_source (SoftObjectPath): The soft object path of the asset the parameter originates in

Return type:

SoftObjectPath or None


---

_classmethod_ has_material_usage( _material_, _usage_)→bool

Check if a particular usage is enabled for the supplied material (e.g. SkeletalMesh, ParticleSprite etc)

Parameters:

- **material** ( _Material_) – Material to check usage for

- **usage** ( _MaterialUsage_) – Usage type to check for this material


Return type:

bool


---

_classmethod_ layout_material_expressions( _material_)→None

Layouts the expressions in a grid pattern

Parameters:

**material** ( _Material_)


---

_classmethod_ layout_material_function_expressions( _material_function_)→None

Layouts the expressions in a grid pattern

Parameters:

**material\_function** ( _MaterialFunction_)


---

_classmethod_ recompile_material( _material_)→None

Trigger a recompile of a material. Must be performed after making changes to the graph to have changes reflected.

Parameters:

**material** ( _Material_)


---

_classmethod_ rename_material_function_parameter_group( _material_function_, _old_group_name_, _new_group_name_)→bool

Renames a material parameter group within the specified material function.

This function allows you to rename an existing parameter group in a material function.
It iterates all parameters within the material function, finds all the one belonging
to the OldGroupName group and switches those parameters to be in the NewGroupName
group. This function only affects parameters that belong to the specified group.
To remove the groups from the parameters the new group name can be ‘None’. If the
OldGroupName does not exist in the material, the function will return false. If the
NewGroupName already exists, the parameters will be “merged” into the existing group.
see: RenameMaterialParameterGroup

Parameters:

- **material\_function** ( _MaterialFunctionInterface_) – The material function asset in which the parameter group resides.

- **old\_group\_name** ( _Name_) – The current name of the parameter group to rename.

- **new\_group\_name** ( _Name_) – The new name to assign to the parameter group.


Returns:

true if the rename operation was successful; false otherwise.

Return type:

bool


---

_classmethod_ rename_material_parameter_group( _material_, _old_group_name_, _new_group_name_)→bool

Renames a material parameter group within the specified material.

This function allows you to rename an existing parameter group in a material.
It iterates all parameters within the material, finds all the one belonging
to the OldGroupName group and switches those parameters to be in the NewGroupName
group. This function only affects parameters that belong to the specified group.
To remove the groups from the parameters the new group name can be ‘None’. If the
OldGroupName does not exist in the material, the function will return false. If
the NewGroupName already exists, the parameters will be “merged” into the existing group.
see: RenameMaterialFunctionParameterGroup

Parameters:

- **material** ( _Material_) – The material asset in which the parameter group resides.

- **old\_group\_name** ( _Name_) – The current name of the parameter group to rename.

- **new\_group\_name** ( _Name_) – The new name to assign to the parameter group.


Returns:

true if the rename operation was successful; false otherwise.

Return type:

bool


---

_classmethod_ set_material_instance_parent( _instance_, _new_parent_)→None

Set the parent Material or Material Instance to use for this Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **new\_parent** ( _MaterialInterface_)



---

_classmethod_ set_material_instance_runtime_virtual_texture_parameter_value( _instance_, _parameter_name_, _value_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→bool

Set the texture parameter value for a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **value** ( _RuntimeVirtualTexture_)

- **association** ( _MaterialParameterAssociation_)


Return type:

bool


---

_classmethod_ set_material_instance_scalar_parameter_value( _instance_, _parameter_name_, _value_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→bool

Set the scalar (float) parameter value for a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **value** ( _float_)

- **association** ( _MaterialParameterAssociation_)


Return type:

bool


---

_classmethod_ set_material_instance_sparse_volume_texture_parameter_value( _instance_, _parameter_name_, _value_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→bool

Set the texture parameter value for a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **value** ( _SparseVolumeTexture_)

- **association** ( _MaterialParameterAssociation_)


Return type:

bool


---

_classmethod_ set_material_instance_static_switch_parameter_value( _instance_, _parameter_name_, _value_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_, _update_material_instance=True_)→bool

Set the static switch parameter value for a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **value** ( _bool_)

- **association** ( _MaterialParameterAssociation_)

- **update\_material\_instance** ( _bool_)


Return type:

bool


---

_classmethod_ set_material_instance_texture_parameter_value( _instance_, _parameter_name_, _value_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→bool

Set the texture parameter value for a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **value** ( _Texture_)

- **association** ( _MaterialParameterAssociation_)


Return type:

bool


---

_classmethod_ set_material_instance_vector_parameter_value( _instance_, _parameter_name_, _value_, _association=MaterialParameterAssociation.GLOBAL_PARAMETER_)→bool

Set the vector parameter value for a Material Instance

Parameters:

- **instance** ( _MaterialInstanceConstant_)

- **parameter\_name** ( _Name_)

- **value** ( _LinearColor_)

- **association** ( _MaterialParameterAssociation_)


Return type:

bool


---

_classmethod_ set_material_usage( _material_, _usage_)→boolorNone

Enable a particular usage for the supplied material (e.g. SkeletalMesh, ParticleSprite etc)

Parameters:

- **material** ( _Material_) – Material to change usage for

- **usage** ( _MaterialUsage_) – New usage type to enable for this material


Returns:

needs\_recompile (bool): Returned to indicate if material needs recompiling after this change

Return type:

bool or None


---

_classmethod_ update_material_function( _material_function_, _preview_material=None_)→None

Update a Material Function after edits have been made.
Will recompile any Materials that use the supplied Material Function.

Parameters:

- **material\_function** ( _MaterialFunctionInterface_)

- **preview\_material** ( _Material_)



---

_classmethod_ update_material_instance( _instance_)→None

Called after making modifications to a Material Instance to recompile shaders etc.

Parameters:

**instance** ( _MaterialInstanceConstant_)

### Table of Contents

- `unreal.MaterialEditingLibrary`
  - `MaterialEditingLibrary`
    - `MaterialEditingLibrary.clear_all_material_instance_parameters()`
    - `MaterialEditingLibrary.connect_material_expressions()`
    - `MaterialEditingLibrary.connect_material_property()`
    - `MaterialEditingLibrary.create_material_expression()`
    - `MaterialEditingLibrary.create_material_expression_in_function()`
    - `MaterialEditingLibrary.delete_all_material_expressions()`
    - `MaterialEditingLibrary.delete_all_material_expressions_in_function()`
    - `MaterialEditingLibrary.delete_material_expression()`
    - `MaterialEditingLibrary.delete_material_expression_in_function()`
    - `MaterialEditingLibrary.duplicate_material_expression()`
    - `MaterialEditingLibrary.get_child_instances()`
    - `MaterialEditingLibrary.get_input_node_output_name_for_material_expression()`
    - `MaterialEditingLibrary.get_inputs_for_material_expression()`
    - `MaterialEditingLibrary.get_material_default_scalar_parameter_value()`
    - `MaterialEditingLibrary.get_material_default_static_switch_parameter_value()`
    - `MaterialEditingLibrary.get_material_default_texture_parameter_value()`
    - `MaterialEditingLibrary.get_material_default_vector_parameter_value()`
    - `MaterialEditingLibrary.get_material_expression_input_names()`
    - `MaterialEditingLibrary.get_material_expression_input_types()`
    - `MaterialEditingLibrary.get_material_expression_node_position()`
    - `MaterialEditingLibrary.get_material_instance_runtime_virtual_texture_parameter_value()`
    - `MaterialEditingLibrary.get_material_instance_scalar_parameter_value()`
    - `MaterialEditingLibrary.get_material_instance_sparse_volume_texture_parameter_value()`
    - `MaterialEditingLibrary.get_material_instance_static_switch_parameter_value()`
    - `MaterialEditingLibrary.get_material_instance_texture_parameter_value()`
    - `MaterialEditingLibrary.get_material_instance_vector_parameter_value()`
    - `MaterialEditingLibrary.get_material_property_input_node()`
    - `MaterialEditingLibrary.get_material_property_input_node_output_name()`
    - `MaterialEditingLibrary.get_material_selected_nodes()`
    - `MaterialEditingLibrary.get_nanite_override_material()`
    - `MaterialEditingLibrary.get_num_material_expressions()`
    - `MaterialEditingLibrary.get_num_material_expressions_in_function()`
    - `MaterialEditingLibrary.get_scalar_parameter_names()`
    - `MaterialEditingLibrary.get_scalar_parameter_source()`
    - `MaterialEditingLibrary.get_static_switch_parameter_names()`
    - `MaterialEditingLibrary.get_static_switch_parameter_source()`
    - `MaterialEditingLibrary.get_statistics()`
    - `MaterialEditingLibrary.get_texture_parameter_names()`
    - `MaterialEditingLibrary.get_texture_parameter_source()`
    - `MaterialEditingLibrary.get_used_textures()`
    - `MaterialEditingLibrary.get_vector_parameter_names()`
    - `MaterialEditingLibrary.get_vector_parameter_source()`
    - `MaterialEditingLibrary.has_material_usage()`
    - `MaterialEditingLibrary.layout_material_expressions()`
    - `MaterialEditingLibrary.layout_material_function_expressions()`
    - `MaterialEditingLibrary.recompile_material()`
    - `MaterialEditingLibrary.rename_material_function_parameter_group()`
    - `MaterialEditingLibrary.rename_material_parameter_group()`
    - `MaterialEditingLibrary.set_material_instance_parent()`
    - `MaterialEditingLibrary.set_material_instance_runtime_virtual_texture_parameter_value()`
    - `MaterialEditingLibrary.set_material_instance_scalar_parameter_value()`
    - `MaterialEditingLibrary.set_material_instance_sparse_volume_texture_parameter_value()`
    - `MaterialEditingLibrary.set_material_instance_static_switch_parameter_value()`
    - `MaterialEditingLibrary.set_material_instance_texture_parameter_value()`
    - `MaterialEditingLibrary.set_material_instance_vector_parameter_value()`
    - `MaterialEditingLibrary.set_material_usage()`
    - `MaterialEditingLibrary.update_material_function()`
    - `MaterialEditingLibrary.update_material_instance()`