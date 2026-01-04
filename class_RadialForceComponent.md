# unreal.RadialForceComponent

```python
class unreal.RadialForceComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneComponent``


Used to emit a radial force or impulse that can affect physics objects and or destructible objects.

**C++ Source:**

- **Module**: Engine

- **File**: RadialForceComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `destructible_damage` (float): [Read-Write] If > 0.f, will cause damage to destructible meshes as well

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `falloff` (RadialImpulseFalloff): [Read-Write] How the force or impulse should fall off as object are further away from the center

- `force_strength` (float): [Read-Write] How strong the force should be

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `ignore_owning_actor` (bool): [Read-Write] If true, do not apply force/impulse to any physics objects that are part of the Actor that owns this component.

- `impulse_strength` (float): [Read-Write] How strong the impulse should be

- `impulse_vel_change` (bool): [Read-Write] If true, the impulse will ignore mass of objects and will always result in a fixed velocity change

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `object_types_to_affect` (Array[ObjectTypeQuery]): [Read-Write] The object types that are affected by this radial force

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `radius` (float): [Read-Write] The radius to apply the force or impulse in

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.



---

**add_object_type_to_affect**( _object_type_) → `None`

Add an object type for this radial force to affect

Parameters:

**object\_type** ( _ObjectTypeQuery_)


---

_property_ `destructible_damage`: float

[Read-Write] If > 0.f, will cause damage to destructible meshes as well

**Type:**

( float)


---

_property_ `falloff`: RadialImpulseFalloff

[Read-Write] How the force or impulse should fall off as object are further away from the center

**Type:**

( RadialImpulseFalloff)


---

**fire_impulse**() → `None`

Fire a single impulse


---

_property_ `force_strength`: float

[Read-Write] How strong the force should be

**Type:**

( float)


---

_property_ `ignore_owning_actor`: bool

[Read-Write] If true, do not apply force/impulse to any physics objects that are part of the Actor that owns this component.

**Type:**

( bool)


---

_property_ `impulse_strength`: float

[Read-Write] How strong the impulse should be

**Type:**

( float)


---

_property_ `impulse_vel_change`: bool

[Read-Write] If true, the impulse will ignore mass of objects and will always result in a fixed velocity change

**Type:**

( bool)


---

_property_ `radius`: float

[Read-Write] The radius to apply the force or impulse in

**Type:**

( float)


---

**remove_object_type_to_affect**( _object_type_) → `None`

Remove an object type that is affected by this radial force

Parameters:

**object\_type** ( _ObjectTypeQuery_)

### Table of Contents

- `unreal.RadialForceComponent`
  - `RadialForceComponent`
    - `RadialForceComponent.add_object_type_to_affect()`
    - `RadialForceComponent.destructible_damage`
    - `RadialForceComponent.falloff`
    - `RadialForceComponent.fire_impulse()`
    - `RadialForceComponent.force_strength`
    - `RadialForceComponent.ignore_owning_actor`
    - `RadialForceComponent.impulse_strength`
    - `RadialForceComponent.impulse_vel_change`
    - `RadialForceComponent.radius`
    - `RadialForceComponent.remove_object_type_to_affect()`