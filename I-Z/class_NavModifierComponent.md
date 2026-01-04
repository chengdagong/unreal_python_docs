# unreal.NavModifierComponent

```python
class unreal.NavModifierComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``NavRelevantComponent``


Nav Modifier Component

**C++ Source:**

- **Module**: NavigationSystem

- **File**: NavModifierComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `area_class` (type(Class)): [Read-Write] NavArea to apply inside the defined volume.

- `area_class_to_replace` (type(Class)): [Read-Write] When setting this value, the modifier behavior changes : it will now replace any surface marked by AreaClassToReplace in the volume and replace it with AreaClass.

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `failsafe_extent` (Vector): [Read-Write] box extent used ONLY when owning actor doesn’t have collision component

- `include_agent_height` (bool): [Read-Write] Setting to ‘true’ will result in expanding lower bounding box of the nav

modifier by agent’s height, before applying to navmesh

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `nav_mesh_resolution` (NavigationDataResolution): [Read-Write] Experimental: Indicates which navmesh resolution should be used around the actor.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!



---

_property_ `area_class`: Class

[Read-Only] NavArea to apply inside the defined volume.

**Type:**

( type( Class))


---

_property_ `area_class_to_replace`: Class

it will now replace any surface marked by AreaClassToReplace in the volume and replace it with AreaClass.

**Type:**

( type( Class))

**Type:**

[Read-Only] When setting this value, the modifier behavior changes


---

**set_area_class**( _new_area_class_) → `None`

Set Area Class

Parameters:

**new\_area\_class** ( _type_ _(_ _Class_ _)_)


---

**set_area_class_to_replace**( _new_area_class_to_replace_) → `None`

Set Area Class to Replace

Parameters:

**new\_area\_class\_to\_replace** ( _type_ _(_ _Class_ _)_)

### Table of Contents

- `unreal.NavModifierComponent`
  - `NavModifierComponent`
    - `NavModifierComponent.area_class`
    - `NavModifierComponent.area_class_to_replace`
    - `NavModifierComponent.set_area_class()`
    - `NavModifierComponent.set_area_class_to_replace()`