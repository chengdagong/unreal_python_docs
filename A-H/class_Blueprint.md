# unreal.Blueprint

```python
class unreal.Blueprint(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintCore``


Blueprints are special assets that provide an intuitive, node-based interface that can be used to create new types of Actors
and script level events; giving designers and gameplay programmers the tools to quickly create and iterate gameplay from
within Unreal Editor without ever needing to write a line of code.

**C++ Source:**

- **Module**: Engine

- **File**: Blueprint.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `blueprint_category` (str): [Read-Write] The category of the Blueprint, used to organize this Blueprint class when displayed in palette windows

- `blueprint_description` (str): [Read-Write] Shows up in the content browser tooltip when the blueprint is hovered

- `blueprint_display_name` (str): [Read-Write] Overrides the BP’s display name in the editor UI

- `blueprint_namespace` (str): [Read-Write] The namespace of this blueprint (if set, the Blueprint will be treated differently for the context menu)

- `compile_mode` (BlueprintCompileMode): [Read-Write] The mode that will be used when compiling this class.

- `deprecate` (bool): [Read-Write] Deprecates the Blueprint, marking the generated class with the CLASS\_Deprecated flag

- `generate_abstract_class` (bool): [Read-Write] Whether or not this blueprint’s class is a abstract class or not. Should set CLASS\_Abstract in the KismetCompiler.

- `generate_const_class` (bool): [Read-Write] Whether or not this blueprint’s class is a const class or not. Should set CLASS\_Const in the KismetCompiler.

- `hide_categories` (Array[str]): [Read-Write] Additional HideCategories. These are added to HideCategories from parent.

- `run_construction_script_in_sequencer` (bool): [Read-Write] whether or not you want to continuously rerun the construction script for an actor in sequencer

- `run_construction_script_on_drag` (bool): [Read-Write] whether or not you want to continuously rerun the construction script for an actor as you drag it in the editor, or only when the drag operation is complete

- `should_cook_property_guids_value` (ShouldCookBlueprintPropertyGuids): [Read-Write] Whether to include the property GUIDs for the generated class in a cooked build.
note: This option may slightly increase memory usage in a cooked build, but can avoid needing to add CoreRedirect data for Blueprint classes stored within SaveGame archives.

- `thumbnail_info` (ThumbnailInfo): [Read-Only] Information for thumbnail rendering


generated\_class()

Gets the class generated when this blueprint is compiled

Returns:

UClass\* The generated class

Return type:

type( Class)


---

**set_blueprint_variable_expose_on_spawn**( _variable_name_, _expose_on_spawn_) → `None`

Sets “Expose On Spawn” to true/false on a Blueprint variable

Parameters:

- **variable\_name** ( _Name_) – The variable name

- **expose\_on\_spawn** ( _bool_) – Set to true to expose on spawn



---

**set_blueprint_variable_expose_to_cinematics**( _variable_name_, _expose_to_cinematics_) → `None`

Sets “Expose To Cinematics” to true/false on a Blueprint variable

Parameters:

- **variable\_name** ( _Name_) – The variable name

- **expose\_to\_cinematics** ( _bool_) – Set to true to expose to cinematics



---

**set_blueprint_variable_instance_editable**( _variable_name_, _instance_editable_) → `None`

Sets “Instance Editable” to true/false on a Blueprint variable

Parameters:

- **variable\_name** ( _Name_) – The variable name

- **instance\_editable** ( _bool_) – Toggle InstanceEditable


### Table of Contents

- `unreal.Blueprint`
  - `Blueprint`
    - `Blueprint.generated_class()`
    - `Blueprint.set_blueprint_variable_expose_on_spawn()`
    - `Blueprint.set_blueprint_variable_expose_to_cinematics()`
    - `Blueprint.set_blueprint_variable_instance_editable()`