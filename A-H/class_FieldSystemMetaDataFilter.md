# unreal.FieldSystemMetaDataFilter

```python
class unreal.FieldSystemMetaDataFilter(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``FieldSystemMetaData``


Filter the particles on which the field will be applied

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

- `filter_type` (FieldFilterType): [Read-Write] Filter state type used to select the particles on which the field will be applied

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `object_type` (FieldObjectType): [Read-Write] Filter object type used to select the particles on which the field will be applied

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `position_type` (FieldPositionType): [Read-Write] Specify which position type will be used for the field evaluation

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!



---

_property_ `filter_type`: FieldFilterType

[Read-Write] Filter state type used to select the particles on which the field will be applied

**Type:**

( FieldFilterType)


---

_property_ `object_type`: FieldObjectType

[Read-Write] Filter object type used to select the particles on which the field will be applied

**Type:**

( FieldObjectType)


---

_property_ `position_type`: FieldPositionType

[Read-Write] Specify which position type will be used for the field evaluation

**Type:**

( FieldPositionType)


---

**set_meta_data_filter_type**( _filter_type_, _object_type_, _position_type_) → `FieldSystemMetaDataFilter`

Set the particles filter type

Parameters:

- **filter\_type** ( _FieldFilterType_) – State type used to select the state particles on which the field will be applied

- **object\_type** ( _FieldObjectType_) – Object type used to select the type of objects(rigid, cloth…) on which the field will be applied

- **position\_type** ( _FieldPositionType_) – Position type used to compute the samples positions


Return type:

FieldSystemMetaDataFilter

### Table of Contents

- `unreal.FieldSystemMetaDataFilter`
  - `FieldSystemMetaDataFilter`
    - `FieldSystemMetaDataFilter.filter_type`
    - `FieldSystemMetaDataFilter.object_type`
    - `FieldSystemMetaDataFilter.position_type`
    - `FieldSystemMetaDataFilter.set_meta_data_filter_type()`