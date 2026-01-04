# unreal.ARTrackableNotifyComponent

```python
class unreal.ARTrackableNotifyComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ActorComponent``


Component used to listen to ar trackable object changes

**C++ Source:**

- **Module**: AugmentedReality

- **File**: ARTrackableNotifyComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `on_add_tracked_env_probe` (TrackableEnvProbeDelegate): [Read-Write] Event that happens when any new ar environment capture probe item is added

- `on_add_tracked_face` (TrackableFaceDelegate): [Read-Write] Event that happens when any new ar Face item is added

- `on_add_tracked_geometry` (TrackableDelegate): [Read-Write] Event that happens when any new trackable ar item is added

- `on_add_tracked_image` (TrackableImageDelegate): [Read-Write] Event that happens when any new ar Image item is added

- `on_add_tracked_object` (TrackableObjectDelegate): [Read-Write] Event that happens when any new ar detected object item is added

- `on_add_tracked_plane` (TrackablePlaneDelegate): [Read-Write] Event that happens when any new ar plane item is added

- `on_add_tracked_point` (TrackablePointDelegate): [Read-Write] Event that happens when any new ar Point item is added

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `on_remove_tracked_env_probe` (TrackableEnvProbeDelegate): [Read-Write] Event that happens when any ar environment capture probe item is removed from the scene

- `on_remove_tracked_face` (TrackableFaceDelegate): [Read-Write] Event that happens when any ar Face item is removed from the scene

- `on_remove_tracked_geometry` (TrackableDelegate): [Read-Write] Event that happens when any trackable ar item is removed from the scene

- `on_remove_tracked_image` (TrackableImageDelegate): [Read-Write] Event that happens when any ar Image item is removed from the scene

- `on_remove_tracked_object` (TrackableObjectDelegate): [Read-Write] Event that happens when any ar detected object item is removed from the scene

- `on_remove_tracked_plane` (TrackablePlaneDelegate): [Read-Write] Event that happens when any ar plane item is removed from the scene

- `on_remove_tracked_point` (TrackablePointDelegate): [Read-Write] Event that happens when any ar Point item is removed from the scene

- `on_update_tracked_env_probe` (TrackableEnvProbeDelegate): [Read-Write] Event that happens when any ar environment capture probe item is updated

- `on_update_tracked_face` (TrackableFaceDelegate): [Read-Write] Event that happens when any ar Face item is updated

- `on_update_tracked_geometry` (TrackableDelegate): [Read-Write] Event that happens when any trackable ar item is updated

- `on_update_tracked_image` (TrackableImageDelegate): [Read-Write] Event that happens when any ar Image item is updated

- `on_update_tracked_object` (TrackableObjectDelegate): [Read-Write] Event that happens when any ar detected object item is updated

- `on_update_tracked_plane` (TrackablePlaneDelegate): [Read-Write] Event that happens when any ar plane item is updated

- `on_update_tracked_point` (TrackablePointDelegate): [Read-Write] Event that happens when any ar Point item is updated

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!



---

_property_ `on_add_tracked_env_probe`: TrackableEnvProbeDelegate

[Read-Write] Event that happens when any new ar environment capture probe item is added

**Type:**

( TrackableEnvProbeDelegate)


---

_property_ `on_add_tracked_face`: TrackableFaceDelegate

[Read-Write] Event that happens when any new ar Face item is added

**Type:**

( TrackableFaceDelegate)


---

_property_ `on_add_tracked_geometry`: TrackableDelegate

[Read-Write] Event that happens when any new trackable ar item is added

**Type:**

( TrackableDelegate)


---

_property_ `on_add_tracked_image`: TrackableImageDelegate

[Read-Write] Event that happens when any new ar Image item is added

**Type:**

( TrackableImageDelegate)


---

_property_ `on_add_tracked_object`: TrackableObjectDelegate

[Read-Write] Event that happens when any new ar detected object item is added

**Type:**

( TrackableObjectDelegate)


---

_property_ `on_add_tracked_plane`: TrackablePlaneDelegate

[Read-Write] Event that happens when any new ar plane item is added

**Type:**

( TrackablePlaneDelegate)


---

_property_ `on_add_tracked_point`: TrackablePointDelegate

[Read-Write] Event that happens when any new ar Point item is added

**Type:**

( TrackablePointDelegate)


---

_property_ `on_remove_tracked_env_probe`: TrackableEnvProbeDelegate

[Read-Write] Event that happens when any ar environment capture probe item is removed from the scene

**Type:**

( TrackableEnvProbeDelegate)


---

_property_ `on_remove_tracked_face`: TrackableFaceDelegate

[Read-Write] Event that happens when any ar Face item is removed from the scene

**Type:**

( TrackableFaceDelegate)


---

_property_ `on_remove_tracked_geometry`: TrackableDelegate

[Read-Write] Event that happens when any trackable ar item is removed from the scene

**Type:**

( TrackableDelegate)


---

_property_ `on_remove_tracked_image`: TrackableImageDelegate

[Read-Write] Event that happens when any ar Image item is removed from the scene

**Type:**

( TrackableImageDelegate)


---

_property_ `on_remove_tracked_object`: TrackableObjectDelegate

[Read-Write] Event that happens when any ar detected object item is removed from the scene

**Type:**

( TrackableObjectDelegate)


---

_property_ `on_remove_tracked_plane`: TrackablePlaneDelegate

[Read-Write] Event that happens when any ar plane item is removed from the scene

**Type:**

( TrackablePlaneDelegate)


---

_property_ `on_remove_tracked_point`: TrackablePointDelegate

[Read-Write] Event that happens when any ar Point item is removed from the scene

**Type:**

( TrackablePointDelegate)


---

_property_ `on_update_tracked_env_probe`: TrackableEnvProbeDelegate

[Read-Write] Event that happens when any ar environment capture probe item is updated

**Type:**

( TrackableEnvProbeDelegate)


---

_property_ `on_update_tracked_face`: TrackableFaceDelegate

[Read-Write] Event that happens when any ar Face item is updated

**Type:**

( TrackableFaceDelegate)


---

_property_ `on_update_tracked_geometry`: TrackableDelegate

[Read-Write] Event that happens when any trackable ar item is updated

**Type:**

( TrackableDelegate)


---

_property_ `on_update_tracked_image`: TrackableImageDelegate

[Read-Write] Event that happens when any ar Image item is updated

**Type:**

( TrackableImageDelegate)


---

_property_ `on_update_tracked_object`: TrackableObjectDelegate

[Read-Write] Event that happens when any ar detected object item is updated

**Type:**

( TrackableObjectDelegate)


---

_property_ `on_update_tracked_plane`: TrackablePlaneDelegate

[Read-Write] Event that happens when any ar plane item is updated

**Type:**

( TrackablePlaneDelegate)


---

_property_ `on_update_tracked_point`: TrackablePointDelegate

[Read-Write] Event that happens when any ar Point item is updated

**Type:**

( TrackablePointDelegate)

### Table of Contents

- `unreal.ARTrackableNotifyComponent`
  - `ARTrackableNotifyComponent`
    - `ARTrackableNotifyComponent.on_add_tracked_env_probe`
    - `ARTrackableNotifyComponent.on_add_tracked_face`
    - `ARTrackableNotifyComponent.on_add_tracked_geometry`
    - `ARTrackableNotifyComponent.on_add_tracked_image`
    - `ARTrackableNotifyComponent.on_add_tracked_object`
    - `ARTrackableNotifyComponent.on_add_tracked_plane`
    - `ARTrackableNotifyComponent.on_add_tracked_point`
    - `ARTrackableNotifyComponent.on_remove_tracked_env_probe`
    - `ARTrackableNotifyComponent.on_remove_tracked_face`
    - `ARTrackableNotifyComponent.on_remove_tracked_geometry`
    - `ARTrackableNotifyComponent.on_remove_tracked_image`
    - `ARTrackableNotifyComponent.on_remove_tracked_object`
    - `ARTrackableNotifyComponent.on_remove_tracked_plane`
    - `ARTrackableNotifyComponent.on_remove_tracked_point`
    - `ARTrackableNotifyComponent.on_update_tracked_env_probe`
    - `ARTrackableNotifyComponent.on_update_tracked_face`
    - `ARTrackableNotifyComponent.on_update_tracked_geometry`
    - `ARTrackableNotifyComponent.on_update_tracked_image`
    - `ARTrackableNotifyComponent.on_update_tracked_object`
    - `ARTrackableNotifyComponent.on_update_tracked_plane`
    - `ARTrackableNotifyComponent.on_update_tracked_point`