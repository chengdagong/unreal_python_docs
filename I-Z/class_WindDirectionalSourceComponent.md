# unreal.WindDirectionalSourceComponent

```python
class unreal.WindDirectionalSourceComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneComponent``


Component that provides a directional wind source. Only affects SpeedTree assets.

**C++ Source:**

- **Module**: Engine

- **File**: WindDirectionalSourceComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `max_gust_amount` (float): [Read-Write]

- `min_gust_amount` (float): [Read-Write]

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `point_wind` (bool): [Read-Write]

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `radius` (float): [Read-Write]

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `speed` (float): [Read-Write]

- `strength` (float): [Read-Write]

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.



---

_property_ `max_gust_amount`: float

[Read-Only]

**Type:**

( float)


---

_property_ `min_gust_amount`: float

[Read-Only]

**Type:**

( float)


---

_property_ `point_wind`: bool

[Read-Only]

**Type:**

( bool)


---

_property_ `radius`: float

[Read-Write]

**Type:**

( float)


---

**set_maximum_gust_amount**( _new_max_gust_) → `None`

Set maximum deviation for wind gusts

Parameters:

**new\_max\_gust** ( _float_)


---

**set_minimum_gust_amount**( _new_min_gust_) → `None`

Set minimum deviation for wind gusts

Parameters:

**new\_min\_gust** ( _float_)


---

**set_radius**( _new_radius_) → `None`

Set the effect radius for point wind

Parameters:

**new\_radius** ( _float_)


---

**set_speed**( _new_speed_) → `None`

Sets the windspeed of the generated wind

Parameters:

**new\_speed** ( _float_)


---

**set_strength**( _new_strength_) → `None`

Sets the strength of the generated wind

Parameters:

**new\_strength** ( _float_)


---

**set_wind_type**( _new_type_) → `None`

Set the type of wind generator to use

Parameters:

**new\_type** ( _WindSourceType_)


---

_property_ `speed`: float

[Read-Write]

**Type:**

( float)


---

_property_ `strength`: float

[Read-Write]

**Type:**

( float)

### Table of Contents

- `unreal.WindDirectionalSourceComponent`
  - `WindDirectionalSourceComponent`
    - `WindDirectionalSourceComponent.max_gust_amount`
    - `WindDirectionalSourceComponent.min_gust_amount`
    - `WindDirectionalSourceComponent.point_wind`
    - `WindDirectionalSourceComponent.radius`
    - `WindDirectionalSourceComponent.set_maximum_gust_amount()`
    - `WindDirectionalSourceComponent.set_minimum_gust_amount()`
    - `WindDirectionalSourceComponent.set_radius()`
    - `WindDirectionalSourceComponent.set_speed()`
    - `WindDirectionalSourceComponent.set_strength()`
    - `WindDirectionalSourceComponent.set_wind_type()`
    - `WindDirectionalSourceComponent.speed`
    - `WindDirectionalSourceComponent.strength`