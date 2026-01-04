# unreal.InterpToMovementComponent

```python
class unreal.InterpToMovementComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovementComponent``


Move the root component between a series of points over a given time \*
see: UMovementComponent

**C++ Source:**

- **Module**: Engine

- **File**: InterpToMovementComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `auto_register_physics_volume_updates` (bool): [Read-Write] If true, then applies the value of bComponentShouldUpdatePhysicsVolume to the UpdatedComponent. If false, will not change bShouldUpdatePhysicsVolume on the UpdatedComponent at all.
see: bComponentShouldUpdatePhysicsVolume

- `auto_register_updated_component` (bool): [Read-Write] If true, registers the owner’s Root component as the UpdatedComponent if there is not one currently assigned.

- `auto_update_tick_registration` (bool): [Read-Write] If true, whenever the updated component is changed, this component will enable or disable its tick dependent on whether it has something to update.
This will NOT enable tick at startup if bAutoActivate is false, because presumably you have a good reason for not wanting it to start ticking initially.

- `behaviour_type` (InterpToBehaviourType): [Read-Write] Movement behaviour of the component

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `check_if_still_in_world` (bool): [Read-Write] Do we want this comp to perform CheckStillInWorld checks?

- `component_should_update_physics_volume` (bool): [Read-Write] If true, enables bShouldUpdatePhysicsVolume on the UpdatedComponent during initialization from SetUpdatedComponent(), otherwise disables such updates.
Only enabled if bAutoRegisterPhysicsVolumeUpdates is true.
WARNING: UpdatePhysicsVolume is potentially expensive if overlap events are also _disabled_ because it requires a separate query against all physics volumes in the world.

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `constrain_to_plane` (bool): [Read-Write] If true, movement will be constrained to a plane.
see: PlaneConstraintNormal, PlaneConstraintOrigin, PlaneConstraintAxisSetting

- `control_points` (Array[InterpControlPoint]): [Read-Write] List of control points to visit.

- `duration` (float): [Read-Write] How long to take to move from the first point to the last (or vice versa)

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `force_sub_stepping` (bool): [Read-Write] If true, forces sub-stepping to break up movement into discrete smaller steps to improve accuracy of the trajectory.
Objects that move in a straight line typically do _not_ need to set this, as movement always uses continuous collision detection (sweeps) so collision is not missed.
Sub-stepping is automatically enabled when under the effects of gravity or when homing towards a target.
see: MaxSimulationTimeStep, MaxSimulationIterations

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `max_simulation_iterations` (int32): [Read-Write] Max number of iterations used for each discrete simulation step.
Increasing this value can address issues with fast-moving objects or complex collision scenarios, at the cost of performance.

WARNING: if (MaxSimulationTimeStep \* MaxSimulationIterations) is too low for the min framerate, the last simulation step may exceed MaxSimulationTimeStep to complete the simulation.
see: MaxSimulationTimeStep, bForceSubStepping

- `max_simulation_time_step` (float): [Read-Write] Max time delta for each discrete simulation step.
Lowering this value can address issues with fast-moving objects or complex collision scenarios, at the cost of performance.

WARNING: if (MaxSimulationTimeStep \* MaxSimulationIterations) is too low for the min framerate, the last simulation step may exceed MaxSimulationTimeStep to complete the simulation.
see: MaxSimulationIterations, bForceSubStepping

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `on_interp_to_reverse` (OnInterpToReverseDelegate): [Read-Write] Called when InterpTo impacts something and reverse is enabled.

- `on_interp_to_stop` (OnInterpToStopDelegate): [Read-Write] Called when InterpTo has come to a stop.

- `on_reset_delegate` (OnInterpToResetDelegate): [Read-Write] Called when InterpTo reached the end and reset back to start .

- `on_wait_begin_delegate` (OnInterpToWaitBeginDelegate): [Read-Write] Called when InterpTo has come to a stop but will resume when possible.

- `on_wait_end_delegate` (OnInterpToWaitEndDelegate): [Read-Write] Called when InterpTo has resumed following a stop.

- `pause_on_impact` (bool): [Read-Write] If true, will pause movement on impact. If false it will behave as if the end of the movement range was reached based on the BehaviourType.

- `plane_constraint_axis_setting` (PlaneConstraintAxisSetting): [Read-Write] Setting that controls behavior when movement is restricted to a 2D plane defined by a specific axis/normal,
so that movement along the locked axis is not be possible.
see: SetPlaneConstraintAxisSetting

- `plane_constraint_normal` (Vector): [Read-Write] The normal or axis of the plane that constrains movement, if bConstrainToPlane is enabled.
If for example you wanted to constrain movement to the X-Z plane (so that Y cannot change), the normal would be set to X=0 Y=1 Z=0.
This is recalculated whenever PlaneConstraintAxisSetting changes. It is normalized once the component is registered with the game world.
see: bConstrainToPlane, SetPlaneConstraintNormal(), SetPlaneConstraintFromVectors()

- `plane_constraint_origin` (Vector): [Read-Write] The origin of the plane that constrains movement, if plane constraint is enabled.
This defines the behavior of snapping a position to the plane, such as by SnapUpdatedComponentToPlane().
see: bConstrainToPlane, SetPlaneConstraintOrigin().

- `primary_component_tick` (ActorComponentTickFunction): [Read-Write] Main tick function for the Component

- `replicate_using_registered_sub_object_list` (bool): [Read-Write] When true the replication system will only replicate the registered subobjects list
When false the replication system will instead call the virtual ReplicateSubObjects() function where the subobjects need to be manually replicated.

- `replicates` (bool): [Read-Write] Is this component currently replicating? Should the network code consider it for replication? Owning Actor must be replicating first!

- `snap_to_plane_at_start` (bool): [Read-Write] If true and plane constraints are enabled, then the updated component will be snapped to the plane when first attached.

- `speed_multiplier` (float): [Read-Write] Change the speed of movement.

- `sweep` (bool): [Read-Write] If true, will sweep for blocking collision during movement. If false, it will simply teleport to the next position and ignore collision.

- `teleport_type` (TeleportType): [Read-Write] Physics teleport type.

- `tick_before_owner` (bool): [Read-Write] If true, after registration we will add a tick dependency to tick before our owner (if we can both tick).
This is important when our tick causes an update in the owner’s position, so that when the owner ticks it uses the most recent position without lag.
Disabling this can improve performance if both objects tick but the order of ticks doesn’t matter.

- `update_only_if_rendered` (bool): [Read-Write] If true, skips TickComponent() if UpdatedComponent was not recently rendered.

- `updated_component` (SceneComponent): [Read-Write] The component we move and update.
If this is null at startup and bAutoRegisterUpdatedComponent is true, the owning Actor’s root component will automatically be set as our UpdatedComponent at startup.
see: bAutoRegisterUpdatedComponent, SetUpdatedComponent(), UpdatedPrimitive

- `updated_primitive` (PrimitiveComponent): [Read-Write] UpdatedComponent, cast as a UPrimitiveComponent. May be invalid if UpdatedComponent was null or not a UPrimitiveComponent.

- `velocity` (Vector): [Read-Write] Current velocity of updated component.



---

**add_control_point_position**( _pos_, _position_is_relative=True_) → `None`

Add a control point that represents a position.

Parameters:

- **pos** ( _Vector_)

- **position\_is\_relative** ( _bool_)



---

_property_ `behaviour_type`: InterpToBehaviourType

[Read-Write] Movement behaviour of the component

**Type:**

( InterpToBehaviourType)


---

_property_ `check_if_still_in_world`: bool

[Read-Write] Do we want this comp to perform CheckStillInWorld checks?

**Type:**

( bool)


---

_property_ `control_points`: None

[Read-Write] List of control points to visit.

**Type:**

( Array\ [InterpControlPoint])


---

_property_ `duration`: float

[Read-Write] How long to take to move from the first point to the last (or vice versa)

**Type:**

( float)


---

**finalise_control_points**() → `None`

Initialise the control points array. Call after adding control points if they are add after begin play .


---

_property_ `force_sub_stepping`: bool

[Read-Write] If true, forces sub-stepping to break up movement into discrete smaller steps to improve accuracy of the trajectory.
Objects that move in a straight line typically do _not_ need to set this, as movement always uses continuous collision detection (sweeps) so collision is not missed.
Sub-stepping is automatically enabled when under the effects of gravity or when homing towards a target.
see: MaxSimulationTimeStep, MaxSimulationIterations

**Type:**

( bool)


---

_property_ `max_simulation_iterations`: int

[Read-Write] Max number of iterations used for each discrete simulation step.
Increasing this value can address issues with fast-moving objects or complex collision scenarios, at the cost of performance.

WARNING: if (MaxSimulationTimeStep \* MaxSimulationIterations) is too low for the min framerate, the last simulation step may exceed MaxSimulationTimeStep to complete the simulation.
see: MaxSimulationTimeStep, bForceSubStepping

**Type:**

(int32)


---

_property_ `max_simulation_time_step`: float

[Read-Write] Max time delta for each discrete simulation step.
Lowering this value can address issues with fast-moving objects or complex collision scenarios, at the cost of performance.

WARNING: if (MaxSimulationTimeStep \* MaxSimulationIterations) is too low for the min framerate, the last simulation step may exceed MaxSimulationTimeStep to complete the simulation.
see: MaxSimulationIterations, bForceSubStepping

**Type:**

( float)

_property_ on\_interp\_to\_reverse _:OnInterpToReverseDelegate_

[Read-Write] Called when InterpTo impacts something and reverse is enabled.

**Type:**

(OnInterpToReverseDelegate)

_property_ on\_interp\_to\_stop _:OnInterpToStopDelegate_

[Read-Write] Called when InterpTo has come to a stop.

**Type:**

(OnInterpToStopDelegate)

_property_ on\_reset\_delegate _:OnInterpToResetDelegate_

[Read-Write] Called when InterpTo reached the end and reset back to start .

**Type:**

(OnInterpToResetDelegate)

_property_ on\_wait\_begin\_delegate _:OnInterpToWaitBeginDelegate_

[Read-Write] Called when InterpTo has come to a stop but will resume when possible.

**Type:**

(OnInterpToWaitBeginDelegate)

_property_ on\_wait\_end\_delegate _:OnInterpToWaitEndDelegate_

[Read-Write] Called when InterpTo has resumed following a stop.

**Type:**

(OnInterpToWaitEndDelegate)


---

_property_ `pause_on_impact`: bool

[Read-Write] If true, will pause movement on impact. If false it will behave as if the end of the movement range was reached based on the BehaviourType.

**Type:**

( bool)


---

**reset_control_points**() → `None`

Clear the control points array and set to stopped.


---

**restart_movement**( _initial_direction=1.000000_) → `None`

Reset to start. Sets time to zero and direction to 1.

Parameters:

**initial\_direction** ( _float_)


---

_property_ `speed_multiplier`: float

[Read-Write] Change the speed of movement.

**Type:**

( float)


---

**stop_simulating**( _hit_result_) → `None`

Clears the reference to UpdatedComponent, fires stop event, and stops ticking.

Parameters:

**hit\_result** ( _HitResult_)


---

_property_ `sweep`: bool

[Read-Write] If true, will sweep for blocking collision during movement. If false, it will simply teleport to the next position and ignore collision.

**Type:**

( bool)


---

_property_ `teleport_type`: TeleportType

[Read-Write] Physics teleport type.

**Type:**

( TeleportType)

### Table of Contents

- `unreal.InterpToMovementComponent`
  - `InterpToMovementComponent`
    - `InterpToMovementComponent.add_control_point_position()`
    - `InterpToMovementComponent.behaviour_type`
    - `InterpToMovementComponent.check_if_still_in_world`
    - `InterpToMovementComponent.control_points`
    - `InterpToMovementComponent.duration`
    - `InterpToMovementComponent.finalise_control_points()`
    - `InterpToMovementComponent.force_sub_stepping`
    - `InterpToMovementComponent.max_simulation_iterations`
    - `InterpToMovementComponent.max_simulation_time_step`
    - `InterpToMovementComponent.on_interp_to_reverse`
    - `InterpToMovementComponent.on_interp_to_stop`
    - `InterpToMovementComponent.on_reset_delegate`
    - `InterpToMovementComponent.on_wait_begin_delegate`
    - `InterpToMovementComponent.on_wait_end_delegate`
    - `InterpToMovementComponent.pause_on_impact`
    - `InterpToMovementComponent.reset_control_points()`
    - `InterpToMovementComponent.restart_movement()`
    - `InterpToMovementComponent.speed_multiplier`
    - `InterpToMovementComponent.stop_simulating()`
    - `InterpToMovementComponent.sweep`
    - `InterpToMovementComponent.teleport_type`