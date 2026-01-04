# unreal.FieldSystemMetaDataIteration

```python
class unreal.FieldSystemMetaDataIteration(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``FieldSystemMetaData``


- UFieldSystemMetaDataIteration : Not used anymore, just hiding it right now but will probably be deprecated if not used in the future


**C++ Source:**

- **Module**: FieldSystemEngine

- **File**: FieldSystemObjects.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `iterations` (int32): [Read-Write] Number of iterations (WIP)

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!



---

_property_ `iterations`: int

[Read-Write] Number of iterations (WIP)

**Type:**

(int32)


---

**set_meta_data_iteration**( _iterations=1_) → `FieldSystemMetaDataIteration`

Set the number of iteration type

Parameters:

**iterations** ( _int32_) – Number of iterations (WIP)

Return type:

FieldSystemMetaDataIteration

### Table of Contents

- `unreal.FieldSystemMetaDataIteration`
  - `FieldSystemMetaDataIteration`
    - `FieldSystemMetaDataIteration.iterations`
    - `FieldSystemMetaDataIteration.set_meta_data_iteration()`