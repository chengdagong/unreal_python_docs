# unreal.SpringArmComponent

```python
class unreal.SpringArmComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``SceneComponent``


This component tries to maintain its children at a fixed distance from the parent,
but will retract the children if there is a collision, and spring back when there is no collision.

Example: Use as a ‘camera boom’ or ‘selfie stick’ to keep the follow camera for a player from colliding into the world.

**C++ Source:**

- **Module**: Engine

- **File**: SpringArmComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `absolute_location` (bool): [Read-Write] If RelativeLocation should be considered relative to the world, rather than the parent

- `absolute_rotation` (bool): [Read-Write] If RelativeRotation should be considered relative to the world, rather than the parent

- `absolute_scale` (bool): [Read-Write] If RelativeScale3D should be considered relative to the world, rather than the parent

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `camera_lag_max_distance` (float): [Read-Write] Max distance the camera target may lag behind the current location. If set to zero, no max distance is enforced.

- `camera_lag_max_time_step` (float): [Read-Write] Max time step used when sub-stepping camera lag.

- `camera_lag_speed` (float): [Read-Write] If bEnableCameraLag is true, controls how quickly camera reaches target position. Low values are slower (more lag), high values are faster (less lag), while zero is instant (no lag).

- `camera_rotation_lag_speed` (float): [Read-Write] If bEnableCameraRotationLag is true, controls how quickly camera reaches target position. Low values are slower (more lag), high values are faster (less lag), while zero is instant (no lag).

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `clamp_to_max_physics_delta_time` (bool): [Read-Write] If true AND the view target is simulating using physics then use the same max timestep cap as the physics system. Prevents camera jitter when delta time is clamped within Chaos Physics.

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `detail_mode` (DetailMode): [Read-Write] Set the required detail level of this component.
It will be deleted or made invisible if the world’s detail level is higher, based on platform and scalability settings.
For example, a detail mode of High may prevent this component from loading on mobile platforms.

- `do_collision_test` (bool): [Read-Write] If true, do a collision test using ProbeChannel and ProbeSize to prevent camera clipping into level.

- `draw_debug_lag_markers` (bool): [Read-Write] If true and camera location lag is enabled, draws markers at the camera target (in green) and the lagged position (in yellow).
A line is drawn between the two locations, in green normally but in red if the distance to the lag target has been clamped (by CameraLagMaxDistance).

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `enable_camera_lag` (bool): [Read-Write] If true, camera lags behind target position to smooth its movement.
see: CameraLagSpeed

- `enable_camera_rotation_lag` (bool): [Read-Write] If true, camera lags behind target rotation to smooth its movement.
see: CameraRotationLagSpeed

- `hidden_in_game` (bool): [Read-Write] Whether to hide the primitive in game, if the primitive is Visible.

- `inherit_pitch` (bool): [Read-Write] Should we inherit pitch from parent component. Does nothing if using Absolute Rotation.

- `inherit_roll` (bool): [Read-Write] Should we inherit roll from parent component. Does nothing if using Absolute Rotation.

- `inherit_yaw` (bool): [Read-Write] Should we inherit yaw from parent component. Does nothing if using Absolute Rotation.

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `mobility` (ComponentMobility): [Read-Write] How often this component is allowed to move, used to make various optimizations. Only safe to set in constructor.

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `physics_volume_changed_delegate` (PhysicsVolumeChanged): [Read-Write] Delegate that will be called when PhysicsVolume has been changed \*

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `probe_channel` (CollisionChannel): [Read-Write] Collision channel of the query probe (defaults to ECC\_Camera)

- `probe_size` (float): [Read-Write] How big should the query probe sphere be (in unreal units)

- `relative_location` (Vector): [Read-Write] Location of the component relative to its parent

- `relative_rotation` (Rotator): [Read-Write] Rotation of the component relative to its parent

- `relative_scale3d` (Vector): [Read-Write] Non-uniform scaling of the component relative to its parent.
Note that scaling is always applied in local space (no shearing etc)

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `should_update_physics_volume` (bool): [Read-Write] Whether or not the cached PhysicsVolume this component overlaps should be updated when the component is moved.
see: GetPhysicsVolume()

- `socket_offset` (Vector): [Read-Write] offset at end of spring arm; use this instead of the relative offset of the attached component to ensure the line trace works as desired

- `target_arm_length` (float): [Read-Write] Natural length of the spring arm when there are no collisions

- `target_offset` (Vector): [Read-Write] Offset at start of spring, applied in world space. Use this if you want a world-space offset from the parent component instead of the usual relative-space offset.

- `use_attach_parent_bound` (bool): [Read-Write] If true, this component uses its parents bounds when attached.
This can be a significant optimization with many components attached together.

- `use_camera_lag_substepping` (bool): [Read-Write] If bUseCameraLagSubstepping is true, sub-step camera damping so that it handles fluctuating frame rates well (though this comes at a cost).
see: CameraLagMaxTimeStep

- `use_pawn_control_rotation` (bool): [Read-Write] If this component is placed on a pawn, should it use the view/control rotation of the pawn where possible?
When disabled, the component will revert to using the stored RelativeRotation of the component.
Note that this component itself does not rotate, but instead maintains its relative rotation to its parent as normal,
and just repositions and rotates its children as desired by the inherited rotation settings. Use GetTargetRotation()
if you want the rotation target based on all the settings (UsePawnControlRotation, InheritPitch, etc).
see: GetTargetRotation(), APawn::GetViewRotation()

- `visible` (bool): [Read-Write] Whether to completely draw the primitive; if false, the primitive is not drawn, does not cast a shadow.



---

_property_ `b_use_controller_view_rotation`: bool

‘b\_use\_controller\_view\_rotation’ was renamed to ‘use\_pawn\_control\_rotation’.

**Type:**

deprecated


---

_property_ `b_use_pawn_view_rotation`: bool

‘b\_use\_pawn\_view\_rotation’ was renamed to ‘use\_pawn\_control\_rotation’.

**Type:**

deprecated


---

_property_ `camera_lag_max_distance`: float

[Read-Write] Max distance the camera target may lag behind the current location. If set to zero, no max distance is enforced.

**Type:**

( float)


---

_property_ `camera_lag_max_time_step`: float

[Read-Write] Max time step used when sub-stepping camera lag.

**Type:**

( float)


---

_property_ `camera_lag_speed`: float

[Read-Write] If bEnableCameraLag is true, controls how quickly camera reaches target position. Low values are slower (more lag), high values are faster (less lag), while zero is instant (no lag).

**Type:**

( float)


---

_property_ `camera_rotation_lag_speed`: float

[Read-Write] If bEnableCameraRotationLag is true, controls how quickly camera reaches target position. Low values are slower (more lag), high values are faster (less lag), while zero is instant (no lag).

**Type:**

( float)


---

_property_ `clamp_to_max_physics_delta_time`: bool

[Read-Write] If true AND the view target is simulating using physics then use the same max timestep cap as the physics system. Prevents camera jitter when delta time is clamped within Chaos Physics.

**Type:**

( bool)


---

_property_ `do_collision_test`: bool

[Read-Write] If true, do a collision test using ProbeChannel and ProbeSize to prevent camera clipping into level.

**Type:**

( bool)


---

_property_ `draw_debug_lag_markers`: bool

[Read-Write] If true and camera location lag is enabled, draws markers at the camera target (in green) and the lagged position (in yellow).
A line is drawn between the two locations, in green normally but in red if the distance to the lag target has been clamped (by CameraLagMaxDistance).

**Type:**

( bool)


---

_property_ `enable_camera_lag`: bool

[Read-Write] If true, camera lags behind target position to smooth its movement.
see: CameraLagSpeed

**Type:**

( bool)


---

_property_ `enable_camera_rotation_lag`: bool

[Read-Write] If true, camera lags behind target rotation to smooth its movement.
see: CameraRotationLagSpeed

**Type:**

( bool)


---

**get_target_rotation**() → `Rotator`

Get the target rotation we inherit, used as the base target for the boom rotation.
This is derived from attachment to our parent and considering the UsePawnControlRotation and absolute rotation flags.

Return type:

Rotator


---

**get_unfixed_camera_position**() → `Vector`

Get the position where the camera should be without applying the Collision Test displacement

Return type:

Vector


---

_property_ `inherit_pitch`: bool

[Read-Write] Should we inherit pitch from parent component. Does nothing if using Absolute Rotation.

**Type:**

( bool)


---

_property_ `inherit_roll`: bool

[Read-Write] Should we inherit roll from parent component. Does nothing if using Absolute Rotation.

**Type:**

( bool)


---

_property_ `inherit_yaw`: bool

[Read-Write] Should we inherit yaw from parent component. Does nothing if using Absolute Rotation.

**Type:**

( bool)


---

**is_collision_fix_applied**() → `bool`

Is the Collision Test displacement being applied?

Return type:

bool


---

_property_ `probe_channel`: CollisionChannel

[Read-Write] Collision channel of the query probe (defaults to ECC\_Camera)

**Type:**

( CollisionChannel)


---

_property_ `probe_size`: float

[Read-Write] How big should the query probe sphere be (in unreal units)

**Type:**

( float)


---

_property_ `socket_offset`: Vector

[Read-Write] offset at end of spring arm; use this instead of the relative offset of the attached component to ensure the line trace works as desired

**Type:**

( Vector)


---

_property_ `target_arm_length`: float

[Read-Write] Natural length of the spring arm when there are no collisions

**Type:**

( float)


---

_property_ `target_offset`: Vector

[Read-Write] Offset at start of spring, applied in world space. Use this if you want a world-space offset from the parent component instead of the usual relative-space offset.

**Type:**

( Vector)


---

_property_ `use_camera_lag_substepping`: bool

[Read-Write] If bUseCameraLagSubstepping is true, sub-step camera damping so that it handles fluctuating frame rates well (though this comes at a cost).
see: CameraLagMaxTimeStep

**Type:**

( bool)


---

_property_ `use_pawn_control_rotation`: bool

[Read-Write] If this component is placed on a pawn, should it use the view/control rotation of the pawn where possible?
When disabled, the component will revert to using the stored RelativeRotation of the component.
Note that this component itself does not rotate, but instead maintains its relative rotation to its parent as normal,
and just repositions and rotates its children as desired by the inherited rotation settings. Use GetTargetRotation()
if you want the rotation target based on all the settings (UsePawnControlRotation, InheritPitch, etc).
see: GetTargetRotation(), APawn::GetViewRotation()

**Type:**

( bool)

### Table of Contents

- `unreal.SpringArmComponent`
  - `SpringArmComponent`
    - `SpringArmComponent.b_use_controller_view_rotation`
    - `SpringArmComponent.b_use_pawn_view_rotation`
    - `SpringArmComponent.camera_lag_max_distance`
    - `SpringArmComponent.camera_lag_max_time_step`
    - `SpringArmComponent.camera_lag_speed`
    - `SpringArmComponent.camera_rotation_lag_speed`
    - `SpringArmComponent.clamp_to_max_physics_delta_time`
    - `SpringArmComponent.do_collision_test`
    - `SpringArmComponent.draw_debug_lag_markers`
    - `SpringArmComponent.enable_camera_lag`
    - `SpringArmComponent.enable_camera_rotation_lag`
    - `SpringArmComponent.get_target_rotation()`
    - `SpringArmComponent.get_unfixed_camera_position()`
    - `SpringArmComponent.inherit_pitch`
    - `SpringArmComponent.inherit_roll`
    - `SpringArmComponent.inherit_yaw`
    - `SpringArmComponent.is_collision_fix_applied()`
    - `SpringArmComponent.probe_channel`
    - `SpringArmComponent.probe_size`
    - `SpringArmComponent.socket_offset`
    - `SpringArmComponent.target_arm_length`
    - `SpringArmComponent.target_offset`
    - `SpringArmComponent.use_camera_lag_substepping`
    - `SpringArmComponent.use_pawn_control_rotation`