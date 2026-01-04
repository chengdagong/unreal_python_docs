# unreal.SceneComponent

```python
class unreal.SceneComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ActorComponent``


A SceneComponent has a transform and supports attachment, but has no rendering or collision capabilities.
Useful as a ‘dummy’ component in the hierarchy to offset others.
see: \Scene Components\

**C++ Source:**

- **Module**: Engine

- **File**: SceneComponent.h


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

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

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

_property_ `absolute_location`: bool

[Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

**Type:**

( bool)


---

_property_ `absolute_rotation`: bool

[Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

**Type:**

( bool)


---

_property_ `absolute_scale`: bool

[Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

**Type:**

( bool)


---

**add_local_offset**( _delta_location_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the location of the component in its local reference frame

Parameters:

- **delta\_location** ( _Vector_) – Change in location of the component in its local reference frame.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_local_rotation**( _delta_rotation_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the rotation of the component in its local reference frame

Parameters:

- **delta\_rotation** ( _Rotator_) – Change in rotation of the component in its local reference frame.

- **sweep** ( _bool_) – Whether we sweep to the destination (currently not supported for rotation).

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts).


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_local_transform**( _delta_transform_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the transform of the component in its local reference frame. Scale is unchanged.

Parameters:

- **delta\_transform** ( _Transform_) – Change in transform of the component in its local reference frame. Scale is unchanged.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_relative_location**( _delta_location_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the translation of the component relative to its parent

Parameters:

- **delta\_location** ( _Vector_) – Change in location of the component relative to its parent

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_relative_rotation**( _delta_rotation_, _sweep_, _teleport_) → `HitResult`

Adds a delta the rotation of the component relative to its parent

Parameters:

- **delta\_rotation** ( _Rotator_) – Change in rotation of the component relative to is parent.

- **sweep** ( _bool_) – Whether we sweep to the destination (currently not supported for rotation).

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts).


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_world_offset**( _delta_location_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the location of the component in world space.

Parameters:

- **delta\_location** ( _Vector_) – Change in location in world space for the component.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_world_rotation**( _delta_rotation_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the rotation of the component in world space.

Parameters:

- **delta\_rotation** ( _Rotator_) – Change in rotation in world space for the component.

- **sweep** ( _bool_) – Whether we sweep to the destination (currently not supported for rotation).

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_world_transform**( _delta_transform_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the transform of the component in world space. Ignores scale and sets it to (1,1,1).

Parameters:

- **delta\_transform** ( _Transform_) – Change in transform in world space for the component. Scale is ignored.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**add_world_transform_keep_scale**( _delta_transform_, _sweep_, _teleport_) → `HitResult`

Adds a delta to the transform of the component in world space. Scale is unchanged.

Parameters:

- **delta\_transform** ( _Transform_) – Change in transform in world space for the component. Scale is ignored since we preserve the original scale.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**attach_to**( _parent:SceneComponent_, _socket_name:Name='None'_, _attach_type:AttachLocation=Ellipsis_, _weld_simulated_bodies:bool=True_) → `bool`

deprecated: ‘attach\_to’ was renamed to ‘k2\_attach\_to’.


---

**attach_to_component**( _parent_, _socket_name_, _location_rule_, _rotation_rule_, _scale_rule_, _weld_simulated_bodies=True_) → `bool`

Attach this component to another scene component, optionally at a named socket. It is valid to call this on components whether or not they have been Registered.

Parameters:

- **parent** ( _SceneComponent_) – Parent to attach to.

- **socket\_name** ( _Name_) – Optional socket to attach to on the parent.

- **location\_rule** ( _AttachmentRule_) – How to handle translation when attaching.

- **rotation\_rule** ( _AttachmentRule_) – How to handle rotation when attaching.

- **scale\_rule** ( _AttachmentRule_) – How to handle scale when attaching.

- **weld\_simulated\_bodies** ( _bool_) – Whether to weld together simulated physics bodies. This transfers the shapes in the welded object into the parent (if simulated), which can result in permanent changes that persist even after subsequently detaching.


Returns:

True if attachment is successful (or already attached to requested parent/socket), false if attachment is rejected and there is no change in AttachParent.

Return type:

bool


---

_property_ `b_absolute_translation`: bool

‘b\_absolute\_translation’ was renamed to ‘absolute\_location’.

**Type:**

deprecated


---

**detach_from_component**( _location_rule=DetachmentRule.KEEP_RELATIVE_, _rotation_rule=DetachmentRule.KEEP_RELATIVE_, _scale_rule=DetachmentRule.KEEP_RELATIVE_, _call_modify=True_) → `None`

Detach this component from whatever it is attached to. Automatically unwelds components that are welded together (see AttachToComponent), though note that some effects of welding may not be undone.

Parameters:

- **location\_rule** ( _DetachmentRule_) – How to handle translations when detaching.

- **rotation\_rule** ( _DetachmentRule_) – How to handle rotation when detaching.

- **scale\_rule** ( _DetachmentRule_) – How to handle scales when detaching.

- **call\_modify** ( _bool_) – If true, call Modify() on the component and the current attach parent component



---

**detach_from_parent**( _maintain_world_position=False_, _call_modify=True_) → `None`

Detach from Parent

Parameters:

- **maintain\_world\_position** ( _bool_)

- **call\_modify** ( _bool_)



---

_property_ `detail_mode`: DetailMode

[Read-Only] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

**Type:**

( DetailMode)


---

**does_socket_exist**( _socket_name_) → `bool`

Return true if socket with the given name exists

Parameters:

**socket\_name** ( _Name_) – Name of the socket or the bone to get the transform

Return type:

bool


---

**get_all_socket_names**() → `Array\ [Name]`

Gets the names of all the sockets on the component.

Returns:

Get the names of all the sockets on the component.

Return type:

Array\ [Name]


---

**get_attach_parent**() → `SceneComponent`

Get the SceneComponent we are attached to.

Return type:

SceneComponent


---

**get_attach_socket_name**() → `Name`

Get the socket we are attached to.

Return type:

Name


---

**get_child_component**( _child_index_) → `SceneComponent`

Gets the attached child component at the specified location

Parameters:

**child\_index** ( _int32_)

Return type:

SceneComponent


---

**get_children_components**( _include_all_descendants_) → `Array\ [SceneComponent]`

Gets all components that are attached to this component, possibly recursively

Parameters:

**include\_all\_descendants** ( _bool_) – Whether to include all descendants in the list of children (i.e. grandchildren, great grandchildren, etc.)

Returns:

children (Array[SceneComponent]): The list of attached child components

Return type:

Array\ [SceneComponent]


---

**get_component_velocity**() → `Vector`

Get velocity of the component: either ComponentVelocity, or the velocity of the physics body if simulating physics.

Returns:

Velocity of the component

Return type:

Vector


---

**get_forward_vector**() → `Vector`

Get the forward (X) unit direction vector from this component, in world space.

Return type:

Vector


---

**get_num_children_components**() → `int32`

Gets the number of attached children components

Return type:

int32


---

**get_parent_components**() → `Array\ [SceneComponent]`

Gets all attachment parent components up to and including the root component

Returns:

parents (Array[SceneComponent]):

Return type:

Array\ [SceneComponent]


---

**get_physics_volume**() → `PhysicsVolume`

Get the PhysicsVolume overlapping this component.

Return type:

PhysicsVolume


---

**get_relative_transform**() → `Transform`

Returns the transform of the component relative to its parent

Return type:

Transform


---

**get_right_vector**() → `Vector`

Get the right (Y) unit direction vector from this component, in world space.

Return type:

Vector


---

**get_socket_location**( _socket_name_) → `Vector`

Get world-space socket or bone location.

Parameters:

**socket\_name** ( _Name_) – Name of the socket or the bone to get the transform

Returns:

Socket transform in world space if socket is found. Otherwise it will return component’s transform in world space.

Return type:

Vector


---

**get_socket_quaternion**( _socket_name_) → `Quat`

Get world-space socket or bone FQuat rotation.
deprecated: Use GetSocketRotation instead, Quat is not fully supported in blueprints.

Parameters:

**socket\_name** ( _Name_) – Name of the socket or the bone to get the transform

Returns:

Socket transform in world space if socket if found. Otherwise it will return component’s transform in world space.

Return type:

Quat


---

**get_socket_rotation**( _socket_name_) → `Rotator`

Get world-space socket or bone FRotator rotation.

Parameters:

**socket\_name** ( _Name_) – Name of the socket or the bone to get the transform

Returns:

Socket transform in world space if socket if found. Otherwise it will return component’s transform in world space.

Return type:

Rotator


---

**get_socket_transform**( _socket_name_, _transform_space=RelativeTransformSpace.RTS_WORLD_) → `Transform`

Get world-space socket transform.

Parameters:

- **socket\_name** ( _Name_) – Name of the socket or the bone to get the transform

- **transform\_space** ( _RelativeTransformSpace_)


Returns:

Socket transform in world space if socket if found. Otherwise it will return component’s transform in world space.

Return type:

Transform


---

**get_up_vector**() → `Vector`

Get the up (Z) unit direction vector from this component, in world space.

Return type:

Vector


---

**get_world_location**() → `Vector`

Return location of the component, in world space

Return type:

Vector


---

**get_world_rotation**() → `Rotator`

Returns rotation of the component, in world space.

Return type:

Rotator


---

**get_world_scale**() → `Vector`

Returns scale of the component, in world space.

Return type:

Vector


---

**get_world_transform**() → `Transform`

Get the current component-to-world transform for this component

Return type:

Transform


---

_property_ `hidden_in_game`: bool

[Read-Only] Whether to hide the primitive in game, if the primitive is Visible.

**Type:**

( bool)


---

**is_any_simulating_physics**() → `bool`

Returns whether the specified body is currently using physics simulation

Return type:

bool


---

**is_simulating_physics**( _bone_name='None'_) → `bool`

Returns whether the specified body is currently using physics simulation

Parameters:

**bone\_name** ( _Name_)

Return type:

bool


---

**is_visible**() → `bool`

Returns true if this component is visible in the current context

Return type:

bool


---

**k2_attach_to**( _parent_, _socket_name='None'_, _attach_type=AttachLocation.KEEP_RELATIVE_OFFSET_, _weld_simulated_bodies=True_) → `bool`

K2 Attach To

Parameters:

- **parent** ( _SceneComponent_)

- **socket\_name** ( _Name_)

- **attach\_type** ( _AttachLocation_)

- **weld\_simulated\_bodies** ( _bool_)


Return type:

bool


---

_property_ `mobility`: ComponentMobility

[Read-Only] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

**Type:**

( ComponentMobility)


---

_property_ `modify_frequency`: ComponentMobility

‘modify\_frequency’ was renamed to ‘mobility’.

**Type:**

deprecated


---

_property_ `physics_volume_changed_delegate`: PhysicsVolumeChanged

[Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

**Type:**

( PhysicsVolumeChanged)


---

_property_ `relative_location`: Vector

[Read-Only] Location of the component relative to its parent

**Type:**

( Vector)


---

_property_ `relative_rotation`: Rotator

[Read-Only] Rotation of the component relative to its parent

**Type:**

( Rotator)


---

_property_ `relative_scale3d`: Vector

[Read-Only] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

**Type:**

( Vector)


---

_property_ `relative_translation`: Vector

‘relative\_translation’ was renamed to ‘relative\_location’.

**Type:**

deprecated


---

**reset_relative_transform**() → `None`

Reset the transform of the component relative to its parent. Sets relative location to zero, relative rotation to no rotation, and Scale to 1.


---

**set_absolute**( _new_absolute_location=False_, _new_absolute_rotation=False_, _new_absolute_scale=False_) → `None`

Set which parts of the relative transform should be relative to parent, and which should be relative to world

Parameters:

- **new\_absolute\_location** ( _bool_)

- **new\_absolute\_rotation** ( _bool_)

- **new\_absolute\_scale** ( _bool_)



---

**set_hidden_in_game**( _new_hidden_, _propagate_to_children=False_) → `None`

Changes the value of bHiddenInGame, if false this will disable Visibility during gameplay

Parameters:

- **new\_hidden** ( _bool_)

- **propagate\_to\_children** ( _bool_)



---

**set_mobility**( _new_mobility_) → `None`

Set how often this component is allowed to move during runtime. Causes a component re-register if the component is already registered

Parameters:

**new\_mobility** ( _ComponentMobility_)


---

**set_relative_location**( _new_location_, _sweep_, _teleport_) → `HitResult`

Set the location of the component relative to its parent

Parameters:

- **new\_location** ( _Vector_) – New location of the component relative to its parent.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**set_relative_location_and_rotation**( _new_location_, _new_rotation_, _sweep_, _teleport_) → `HitResult`

Set the location and rotation of the component relative to its parent

Parameters:

- **new\_location** ( _Vector_) – New location of the component relative to its parent.

- **new\_rotation** ( _Rotator_) – New rotation of the component relative to its parent.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**set_relative_rotation**( _new_rotation_, _sweep_, _teleport_) → `HitResult`

Set the rotation of the component relative to its parent

Parameters:

- **new\_rotation** ( _Rotator_) – New rotation of the component relative to its parent

- **sweep** ( _bool_) – Whether we sweep to the destination (currently not supported for rotation).

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts).


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**set_relative_scale3d**( _new_scale3d_) → `None`

Set the non-uniform scale of the component relative to its parent

Parameters:

**new\_scale3d** ( _Vector_)


---

**set_relative_transform**( _new_transform_, _sweep_, _teleport_) → `HitResult`

Set the transform of the component relative to its parent

Parameters:

- **new\_transform** ( _Transform_) – New transform of the component relative to its parent.

- **sweep** ( _bool_) – Whether we sweep to the destination (currently not supported for rotation).

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts).


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**set_visibility**( _new_visibility_, _propagate_to_children=False_) → `None`

Set visibility of the component, if during game use this to turn on/off

Parameters:

- **new\_visibility** ( _bool_)

- **propagate\_to\_children** ( _bool_)



---

**set_world_location**( _new_location_, _sweep_, _teleport_) → `HitResult`

Put this component at the specified location in world space. Updates relative location to achieve the final world location.

Parameters:

- **new\_location** ( _Vector_) – New location in world space for the component.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**set_world_location_and_rotation**( _new_location_, _new_rotation_, _sweep_, _teleport_) → `HitResult`

Set the relative location and rotation of the component to put it at the supplied pose in world space.

Parameters:

- **new\_location** ( _Vector_) – New location in world space for the component.

- **new\_rotation** ( _Rotator_) – New rotation in world space for the component.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

**set_world_rotation**( _new_rotation_, _sweep_, _teleport_) → `HitResult`

- Put this component at the specified rotation in world space. Updates relative rotation to achieve the final world rotation.


Parameters:

- **new\_rotation** ( _Rotator_) – New rotation in world space for the component. \*

- **sweep** ( _bool_) – Whether we sweep to the destination (currently not supported for rotation). \*

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). \* If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). \* If false, physics velocity is updated based on the change in position (affecting ragdoll parts). \* If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true. \*

Return type:

HitResult


---

**set_world_scale3d**( _new_scale_) → `None`

Set the relative scale of the component to put it at the supplied scale in world space.

Parameters:

**new\_scale** ( _Vector_) – New scale in world space for this component.


---

**set_world_transform**( _new_transform_, _sweep_, _teleport_) → `HitResult`

Set the transform of the component in world space.

Parameters:

- **new\_transform** ( _Transform_) – New transform in world space for the component.

- **sweep** ( _bool_) – Whether we sweep to the destination location, triggering overlaps along the way and stopping short of the target if blocked by something. Only the root component is swept and checked for blocking collision, child components move without sweeping. If collision is off, this has no effect.

- **teleport** ( _bool_) – Whether we teleport the physics state (if physics collision is enabled for this object). If true, physics velocity for this object is unchanged (so ragdoll parts are not affected by change in location). If false, physics velocity is updated based on the change in position (affecting ragdoll parts). If CCD is on and not teleporting, this will affect objects along the entire sweep volume.


Returns:

sweep\_hit\_result (HitResult): Hit result from any impact if sweep is true.

Return type:

HitResult


---

_property_ `should_update_physics_volume`: bool

[Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

**Type:**

( bool)


---

**toggle_visibility**( _propagate_to_children=False_) → `None`

Toggle visibility of the component

Parameters:

**propagate\_to\_children** ( _bool_)


---

_property_ `use_attach_parent_bound`: bool

[Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

**Type:**

( bool)


---

_property_ `visible`: bool

[Read-Only] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.

**Type:**

( bool)

### Table of Contents

- `unreal.SceneComponent`
  - `SceneComponent`
    - `SceneComponent.absolute_location`
    - `SceneComponent.absolute_rotation`
    - `SceneComponent.absolute_scale`
    - `SceneComponent.add_local_offset()`
    - `SceneComponent.add_local_rotation()`
    - `SceneComponent.add_local_transform()`
    - `SceneComponent.add_relative_location()`
    - `SceneComponent.add_relative_rotation()`
    - `SceneComponent.add_world_offset()`
    - `SceneComponent.add_world_rotation()`
    - `SceneComponent.add_world_transform()`
    - `SceneComponent.add_world_transform_keep_scale()`
    - `SceneComponent.attach_to()`
    - `SceneComponent.attach_to_component()`
    - `SceneComponent.b_absolute_translation`
    - `SceneComponent.detach_from_component()`
    - `SceneComponent.detach_from_parent()`
    - `SceneComponent.detail_mode`
    - `SceneComponent.does_socket_exist()`
    - `SceneComponent.get_all_socket_names()`
    - `SceneComponent.get_attach_parent()`
    - `SceneComponent.get_attach_socket_name()`
    - `SceneComponent.get_child_component()`
    - `SceneComponent.get_children_components()`
    - `SceneComponent.get_component_velocity()`
    - `SceneComponent.get_forward_vector()`
    - `SceneComponent.get_num_children_components()`
    - `SceneComponent.get_parent_components()`
    - `SceneComponent.get_physics_volume()`
    - `SceneComponent.get_relative_transform()`
    - `SceneComponent.get_right_vector()`
    - `SceneComponent.get_socket_location()`
    - `SceneComponent.get_socket_quaternion()`
    - `SceneComponent.get_socket_rotation()`
    - `SceneComponent.get_socket_transform()`
    - `SceneComponent.get_up_vector()`
    - `SceneComponent.get_world_location()`
    - `SceneComponent.get_world_rotation()`
    - `SceneComponent.get_world_scale()`
    - `SceneComponent.get_world_transform()`
    - `SceneComponent.hidden_in_game`
    - `SceneComponent.is_any_simulating_physics()`
    - `SceneComponent.is_simulating_physics()`
    - `SceneComponent.is_visible()`
    - `SceneComponent.k2_attach_to()`
    - `SceneComponent.mobility`
    - `SceneComponent.modify_frequency`
    - `SceneComponent.physics_volume_changed_delegate`
    - `SceneComponent.relative_location`
    - `SceneComponent.relative_rotation`
    - `SceneComponent.relative_scale3d`
    - `SceneComponent.relative_translation`
    - `SceneComponent.reset_relative_transform()`
    - `SceneComponent.set_absolute()`
    - `SceneComponent.set_hidden_in_game()`
    - `SceneComponent.set_mobility()`
    - `SceneComponent.set_relative_location()`
    - `SceneComponent.set_relative_location_and_rotation()`
    - `SceneComponent.set_relative_rotation()`
    - `SceneComponent.set_relative_scale3d()`
    - `SceneComponent.set_relative_transform()`
    - `SceneComponent.set_visibility()`
    - `SceneComponent.set_world_location()`
    - `SceneComponent.set_world_location_and_rotation()`
    - `SceneComponent.set_world_rotation()`
    - `SceneComponent.set_world_scale3d()`
    - `SceneComponent.set_world_transform()`
    - `SceneComponent.should_update_physics_volume`
    - `SceneComponent.toggle_visibility()`
    - `SceneComponent.use_attach_parent_bound`
    - `SceneComponent.visible`