# unreal.ControlRigBlueprint

```python
class unreal.ControlRigBlueprint(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``RigVMBlueprint``


Control Rig Blueprint

**C++ Source:**

- **Plugin**: ControlRig

- **Module**: ControlRigDeveloper

- **File**: ControlRigBlueprintLegacy.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `allow_multiple_instances` (bool): [Read-Write] If set to true, multiple control rig tracks can be created for the same rig in sequencer

- `asset_variant` (RigVMVariant): [Read-Write] Variant information about this asset

- `blueprint_category` (str): [Read-Write] The category of the Blueprint, used to organize this Blueprint class when displayed in palette windows

- `blueprint_description` (str): [Read-Write] Shows up in the content browser tooltip when the blueprint is hovered

- `blueprint_display_name` (str): [Read-Write] Overrides the BP’s display name in the editor UI

- `blueprint_namespace` (str): [Read-Write] The namespace of this blueprint (if set, the Blueprint will be treated differently for the context menu)

- `compile_mode` (BlueprintCompileMode): [Read-Write] The mode that will be used when compiling this class.

- `custom_thumbnail` (str): [Read-Write] This relates to FAssetThumbnailPool::CustomThumbnailTagName and allows
the thumbnail pool to show the thumbnail of the icon rather than the
rig itself to avoid deploying the 3D renderer.

- `deprecate` (bool): [Read-Write] Deprecates the Blueprint, marking the generated class with the CLASS\_Deprecated flag

- `draw_container` (RigVMDrawContainer): [Read-Write]

- `generate_abstract_class` (bool): [Read-Write] Whether or not this blueprint’s class is a abstract class or not. Should set CLASS\_Abstract in the KismetCompiler.

- `generate_const_class` (bool): [Read-Write] Whether or not this blueprint’s class is a const class or not. Should set CLASS\_Const in the KismetCompiler.

- `hide_categories` (Array[str]): [Read-Write] Additional HideCategories. These are added to HideCategories from parent.

- `hierarchy` (RigHierarchy): [Read-Write]

- `hierarchy_settings` (RigHierarchySettings): [Read-Write]

- `influences` (RigInfluenceMapPerEvent): [Read-Write]

- `modular_rig_model` (ModularRigModel): [Read-Write]

- `modular_rig_settings` (ModularRigSettings): [Read-Write]

- `preview_skeletal_mesh` (SkeletalMesh): [Read-Write]

- `python_log_settings` (RigVMPythonSettings): [Read-Write]

- `rig_graph_display_settings` (RigVMEdGraphDisplaySettings): [Read-Write]

- `rig_module_settings` (RigModuleSettings): [Read-Write]

- `run_construction_script_in_sequencer` (bool): [Read-Write] whether or not you want to continuously rerun the construction script for an actor in sequencer

- `run_construction_script_on_drag` (bool): [Read-Write] whether or not you want to continuously rerun the construction script for an actor as you drag it in the editor, or only when the drag operation is complete

- `shape_libraries` (Array[ControlRigShapeLibrary]): [Read-Write]

- `should_cook_property_guids_value` (ShouldCookBlueprintPropertyGuids): [Read-Write] Whether to include the property GUIDs for the generated class in a cooked build.
note: This option may slightly increase memory usage in a cooked build, but can avoid needing to add CoreRedirect data for Blueprint classes stored within SaveGame archives.

- `source_curve_import` (Object): [Read-Write] The skeleton from import into a curve

- `source_hierarchy_import` (Object): [Read-Write] The skeleton from import into a hierarchy

- `thumbnail_info` (ThumbnailInfo): [Read-Only] Information for thumbnail rendering

- `vm_compile_settings` (RigVMCompileSettings): [Read-Write]

- `vm_runtime_settings` (RigVMRuntimeSettings): [Read-Write]



---

**can_turn_into_standalone_rig**() → `bool`

Can Turn Into Standalone Rig Blueprint

Return type:

bool


---

**convert_hierarchy_elements_to_spawner_nodes**( _hierarchy_, _keys_, _remove_elements=True_) → `Array\ [RigVMNode]`

Convert Hierarchy Elements to Spawner Nodes

Parameters:

- **hierarchy** ( _RigHierarchy_)

- **keys** ( _Array_ _\_ [_RigElementKey_ _]_)

- **remove\_elements** ( _bool_)


Return type:

Array\ [RigVMNode]


---

**create_control_rig**() → `ControlRig`

Create Control Rig

Return type:

ControlRig


---

**find_references_to_module**() → `Array\ [ModuleReferenceData]`

Find References to Module

Return type:

Array\ [ModuleReferenceData]

get\_control\_rig\_class()

Get Control Rig Class

Return type:

type( Class)


---

_classmethod_ get_currently_open_rig_blueprints()→Array\ [ControlRigBlueprint]

Get Currently Open Rig Blueprints

Return type:

Array\ [ControlRigBlueprint]


---

**get_debugged_control_rig**() → `ControlRig`

Get Debugged Control Rig

Return type:

ControlRig


---

**get_hierarchy_controller**() → `RigHierarchyController`

Get Hierarchy Controller

Return type:

RigHierarchyController


---

**get_modular_rig_controller**() → `ModularRigController`

Get Modular Rig Controller

Return type:

ModularRigController


---

**get_preview_mesh**() → `SkeletalMesh`

Get Preview Mesh

Return type:

SkeletalMesh


---

**get_rig_module_icon**() → `Texture2D`

Get Rig Module Icon

Return type:

Texture2D


---

_property_ `hierarchy`: RigHierarchy

[Read-Only]

**Type:**

( RigHierarchy)


---

**is_control_rig_module**() → `bool`

Is Control Rig Module

Return type:

bool


---

_property_ `modular_rig_model`: ModularRigModel

[Read-Only]

**Type:**

( ModularRigModel)


---

**recompile_modular_rig**() → `None`

Recompile Modular Rig


---

**set_preview_mesh**( _preview_mesh_, _mark_as_dirty=True_) → `None`

IInterface\_PreviewMeshProvider interface

Parameters:

- **preview\_mesh** ( _SkeletalMesh_)

- **mark\_as\_dirty** ( _bool_)



---

**turn_into_control_rig_module**() → `bool`

Turn Into Control Rig Module Blueprint

Return type:

bool


---

**turn_into_standalone_rig**() → `bool`

Turn Into Standalone Rig Blueprint

Return type:

bool


---

**update_exposed_module_connectors**() → `None`

Update Exposed Module Connectors

### Table of Contents

- `unreal.ControlRigBlueprint`
  - `ControlRigBlueprint`
    - `ControlRigBlueprint.can_turn_into_standalone_rig()`
    - `ControlRigBlueprint.convert_hierarchy_elements_to_spawner_nodes()`
    - `ControlRigBlueprint.create_control_rig()`
    - `ControlRigBlueprint.find_references_to_module()`
    - `ControlRigBlueprint.get_control_rig_class()`
    - `ControlRigBlueprint.get_currently_open_rig_blueprints()`
    - `ControlRigBlueprint.get_debugged_control_rig()`
    - `ControlRigBlueprint.get_hierarchy_controller()`
    - `ControlRigBlueprint.get_modular_rig_controller()`
    - `ControlRigBlueprint.get_preview_mesh()`
    - `ControlRigBlueprint.get_rig_module_icon()`
    - `ControlRigBlueprint.hierarchy`
    - `ControlRigBlueprint.is_control_rig_module()`
    - `ControlRigBlueprint.modular_rig_model`
    - `ControlRigBlueprint.recompile_modular_rig()`
    - `ControlRigBlueprint.set_preview_mesh()`
    - `ControlRigBlueprint.turn_into_control_rig_module()`
    - `ControlRigBlueprint.turn_into_standalone_rig()`
    - `ControlRigBlueprint.update_exposed_module_connectors()`