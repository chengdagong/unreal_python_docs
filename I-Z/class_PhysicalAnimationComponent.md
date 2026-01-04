# unreal.PhysicalAnimationComponent

```python
class unreal.PhysicalAnimationComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ActorComponent``


Physical Animation Component

**C++ Source:**

- **Module**: Engine

- **File**: PhysicalAnimationComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `strength_multiplyer` (float): [Read-Write] Multiplies the strength of any active motors. (can blend from 0-1 for example)



---

**apply_physical_animation_profile_below**( _body_name_, _profile_name_, _include_self=True_, _clear_not_found=False_) → `None`

Applies the physical animation profile to the body given and all bodies below.

Parameters:

- **body\_name** ( _Name_) – The body from which we’d like to start applying the physical animation profile. Finds all bodies below in the skeleton hierarchy. None implies all bodies

- **profile\_name** ( _Name_) – The physical animation profile we’d like to apply. For each body in the physics asset we search for physical animation settings with this name.

- **include\_self** ( _bool_) – Whether to include the provided body name in the list of bodies we act on (useful to ignore for cases where a root has multiple children)

- **clear\_not\_found** ( _bool_) – If true, bodies without the given profile name will have any existing physical animation settings cleared. If false, bodies without the given profile name are left untouched.



---

**apply_physical_animation_settings**( _body_name_, _physical_animation_data_) → `None`

Applies the physical animation settings to the body given.

Parameters:

- **body\_name** ( _Name_)

- **physical\_animation\_data** ( _PhysicalAnimationData_)



---

**apply_physical_animation_settings_below**( _body_name_, _physical_animation_data_, _include_self=True_) → `None`

Applies the physical animation settings to the body given and all bodies below.

Parameters:

- **body\_name** ( _Name_)

- **physical\_animation\_data** ( _PhysicalAnimationData_)

- **include\_self** ( _bool_)



---

**get_body_target_transform**( _body_name_) → `Transform`

Returns the target transform for the given body. If physical animation component is not controlling this body, returns its current transform.

Parameters:

**body\_name** ( _Name_)

Return type:

Transform


---

**set_skeletal_mesh_component**( _skeletal_mesh_component_) → `None`

Sets the skeletal mesh we are driving through physical animation. Will erase any existing physical animation data.

Parameters:

**skeletal\_mesh\_component** ( _SkeletalMeshComponent_)


---

**set_strength_multiplyer**( _strength_multiplyer_) → `None`

Updates strength multiplyer and any active motors

Parameters:

**strength\_multiplyer** ( _float_)


---

_property_ `strength_multiplyer`: float

[Read-Only] Multiplies the strength of any active motors. (can blend from 0-1 for example)

**Type:**

( float)

### Table of Contents

- `unreal.PhysicalAnimationComponent`
  - `PhysicalAnimationComponent`
    - `PhysicalAnimationComponent.apply_physical_animation_profile_below()`
    - `PhysicalAnimationComponent.apply_physical_animation_settings()`
    - `PhysicalAnimationComponent.apply_physical_animation_settings_below()`
    - `PhysicalAnimationComponent.get_body_target_transform()`
    - `PhysicalAnimationComponent.set_skeletal_mesh_component()`
    - `PhysicalAnimationComponent.set_strength_multiplyer()`
    - `PhysicalAnimationComponent.strength_multiplyer`