# unreal.ChaosWheeledVehicleMovementComponent

```python
class unreal.ChaosWheeledVehicleMovementComponent(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``ChaosVehicleMovementComponent``


Chaos Wheeled Vehicle Movement Component

**C++ Source:**

- **Plugin**: ChaosVehiclesPlugin

- **Module**: ChaosVehicles

- **File**: ChaosWheeledVehicleMovementComponent.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `aerofoils` (Array[VehicleAerofoilConfig]): [Read-Write] Optional aerofoil setup - can be used for car spoilers or aircraft wings/elevator/rudder

- `asset_user_data` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `asset_user_data_editor_only` (Array[AssetUserData]): [Read-Write] Array of user data stored with the component

- `auto_activate` (bool): [Read-Write] Whether the component is activated at creation or must be explicitly activated.

- `auto_register_physics_volume_updates` (bool): [Read-Write] If true, then applies the value of bComponentShouldUpdatePhysicsVolume to the UpdatedComponent. If false, will not change bShouldUpdatePhysicsVolume on the UpdatedComponent at all.
see: bComponentShouldUpdatePhysicsVolume

- `auto_register_updated_component` (bool): [Read-Write] If true, registers the owner’s Root component as the UpdatedComponent if there is not one currently assigned.

- `auto_update_tick_registration` (bool): [Read-Write] If true, whenever the updated component is changed, this component will enable or disable its tick dependent on whether it has something to update.
This will NOT enable tick at startup if bAutoActivate is false, because presumably you have a good reason for not wanting it to start ticking initially.

- `brake_input_rate` (VehicleInputRateConfig): [Read-Write] Rate at which input brake can rise and fall

- `can_ever_affect_navigation` (bool): [Read-Write] Whether this component can potentially influence navigation

- `center_of_mass_override` (Vector): [Read-Write] The center of mass override value, this value overrides the calculated COM and the COM offset value in the mesh is also ignored.

- `chassis_height` (float): [Read-Write] Chassis height used for drag force computation (cm)

- `chassis_width` (float): [Read-Write] Chassis width used for drag force computation (cm)

- `component_should_update_physics_volume` (bool): [Read-Write] If true, enables bShouldUpdatePhysicsVolume on the UpdatedComponent during initialization from SetUpdatedComponent(), otherwise disables such updates.
Only enabled if bAutoRegisterPhysicsVolumeUpdates is true.
WARNING: UpdatePhysicsVolume is potentially expensive if overlap events are also _disabled_ because it requires a separate query against all physics volumes in the world.

- `component_tags` (Array[Name]): [Read-Write] Array of tags that can be used for grouping and categorizing. Can also be accessed from scripting.

- `constrain_to_plane` (bool): [Read-Write] If true, movement will be constrained to a plane.
see: PlaneConstraintNormal, PlaneConstraintOrigin, PlaneConstraintAxisSetting

- `differential_setup` (VehicleDifferentialConfig): [Read-Write] Differential

- `downforce_coefficient` (float): [Read-Write] DownforceCoefficient of the vehicle chassis - force pressing vehicle into ground at speed

- `drag_coefficient` (float): [Read-Write] DragCoefficient of the vehicle chassis - force resisting forward motion at speed

- `editable_when_inherited` (bool): [Read-Write] True if this component can be modified when it was inherited from a parent actor class

- `enable_center_of_mass_override` (bool): [Read-Write] Enable to override the calculated COM position with your own fixed value - this prevents the vehicle handling changing when the asset changes

- `engine_setup` (VehicleEngineConfig): [Read-Write] Engine

- `fixed_path_braking_distance` (float): [Read-Write]
deprecated: FixedPathBrakingDistance is deprecated, please use NavMovementProperties.FixedPathBrakingDistance instead.

- `handbrake_input_rate` (VehicleInputRateConfig): [Read-Write] Rate at which input handbrake can rise and fall

- `idle_brake_input` (float): [Read-Write] How much to press the brake when the player has release throttle

- `inertia_tensor_scale` (Vector): [Read-Write] Scales the vehicle’s inertia in each direction (forward, right, up)

- `is_editor_only` (bool): [Read-Write] If true, the component will be excluded from non-editor builds

- `legacy_wheel_friction_position` (bool): [Read-Write]

- `mass` (float): [Read-Write] Mass to set the vehicle chassis to. It’s much easier to tweak vehicle settings when
the mass doesn’t change due to tweaks with the physics asset. [kg]

- `mechanical_sim_enabled` (bool): [Read-Write]

- `nav_agent_props` (NavAgentProperties): [Read-Write] Properties that define how the component can move.

- `nav_movement_properties` (NavMovementProperties): [Read-Write]

- `on_component_activated` (ActorComponentActivatedSignature): [Read-Write] Called when the component has been activated, with parameter indicating if it was from a reset

- `on_component_deactivated` (ActorComponentDeactivateSignature): [Read-Write] Called when the component has been deactivated

- `pitch_input_rate` (VehicleInputRateConfig): [Read-Write] Rate at which input pitch can rise and fall

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

- `requires_controller_for_inputs` (bool): [Read-Write] Bypass the need for a controller in order for the controls to be processed.

- `reverse_as_brake` (bool): [Read-Write] If true, the brake and reverse controls will behave in a more arcade fashion where holding reverse also functions as brake. For a more realistic approach turn this off

- `roll_input_rate` (VehicleInputRateConfig): [Read-Write] Rate at which input roll can rise and fall

- `sleep_slope_limit` (float): [Read-Write] Option to apply some aggressive sleep logic if slopes up Z is less than this value, i.e value = Cos(SlopeAngle) so 0.866 will sleep up to 30 degree slopes

- `sleep_threshold` (float): [Read-Write] Option to apply some aggressive sleep logic, larger number is more agressive, 0 disables

- `snap_to_plane_at_start` (bool): [Read-Write] If true and plane constraints are enabled, then the updated component will be snapped to the plane when first attached.

- `stabilize_control` (VehicleStabilizeControlConfig): [Read-Write] Arcade style control of vehicle

- `steering_input_rate` (VehicleInputRateConfig): [Read-Write] Rate at which input steering can rise and fall

- `steering_setup` (VehicleSteeringConfig): [Read-Write] Transmission data

- `stop_threshold` (float): [Read-Write] Auto-brake when absolute vehicle forward speed is less than this (cm/s)

- `suspension_enabled` (bool): [Read-Write]

- `target_rotation_control` (VehicleTargetRotationControlConfig): [Read-Write] Arcade style direct control of vehicle rotation via torque force

- `throttle_as_brake` (bool): [Read-Write] If true, when reversing the throttle will behave like a brake while the vehicle moving in a backwards direction - requires bReverseAsBrake to be enabled for operation

- `throttle_input_rate` (VehicleInputRateConfig): [Read-Write] Rate at which input throttle can rise and fall

- `thrusters` (Array[VehicleThrustConfig]): [Read-Write] Optional thruster setup, use one or more as your main engine or as supplementary booster

- `tick_before_owner` (bool): [Read-Write] If true, after registration we will add a tick dependency to tick before our owner (if we can both tick).
This is important when our tick causes an update in the owner’s position, so that when the owner ticks it uses the most recent position without lag.
Disabling this can improve performance if both objects tick but the order of ticks doesn’t matter.

- `torque_control` (VehicleTorqueControlConfig): [Read-Write] Arcade style direct control of vehicle rotation via torque force

- `transmission_setup` (VehicleTransmissionConfig): [Read-Write] Transmission data

- `update_nav_agent_with_owners_collision` (bool): [Read-Write]
deprecated: bUpdateNavAgentWithOwnersCollision is deprecated, please use NavMovementProperties.bUpdateNavAgentWithOwnersCollision instead.

- `update_only_if_rendered` (bool): [Read-Write] If true, skips TickComponent() if UpdatedComponent was not recently rendered.

- `updated_component` (SceneComponent): [Read-Write] The component we move and update.
If this is null at startup and bAutoRegisterUpdatedComponent is true, the owning Actor’s root component will automatically be set as our UpdatedComponent at startup.
see: bAutoRegisterUpdatedComponent, SetUpdatedComponent(), UpdatedPrimitive

- `updated_primitive` (PrimitiveComponent): [Read-Write] UpdatedComponent, cast as a UPrimitiveComponent. May be invalid if UpdatedComponent was null or not a UPrimitiveComponent.

- `use_acceleration_for_paths` (bool): [Read-Write]
deprecated: bUseAccelerationForPaths is deprecated, please use NavMovementProperties.bUseAccelerationForPaths instead.

- `use_fixed_braking_distance_for_paths` (bool): [Read-Write]
deprecated: bUseFixedBrakingDistanceForPaths is deprecated, please use NavMovementProperties.bUseFixedBrakingDistanceForPaths instead.

- `velocity` (Vector): [Read-Write] Current velocity of updated component.

- `wheel_friction_enabled` (bool): [Read-Write]

- `wheel_setups` (Array[ChaosWheelSetup]): [Read-Write] Wheels to create

- `wheel_trace_collision_responses` (CollisionResponseContainer): [Read-Write]

- `wheels` (Array[ChaosVehicleWheel]): [Read-Write] Our instanced wheels

- `wrong_direction_threshold` (float): [Read-Write] Auto-brake when vehicle forward speed is opposite of player input by at least this much (cm/s)

- `yaw_input_rate` (VehicleInputRateConfig): [Read-Write] Rate at which input yaw can rise and fall


_classmethod_ break\_wheel\_snapshot( _snapshot)->(suspension\_offset=float_, _wheel\_rotation\_angle=float_, _steering\_angle=float_, _wheel\_radius=float_, _wheel\_angular\_velocity=float_)

Break Wheel Snapshot

Parameters:

**snapshot** ( _WheelSnapshot_)

Returns:

suspension\_offset (float):

wheel\_rotation\_angle (float):

steering\_angle (float):

wheel\_radius (float):

wheel\_angular\_velocity (float):

Return type:

tuple

_classmethod_ break\_wheel\_status( _status)->(contact=bool_, _contact\_point=Vector_, _phys\_material=PhysicalMaterial_, _normalized\_suspension\_length=float_, _spring\_force=float_, _slip\_angle=float_, _is\_slipping=bool_, _slip\_magnitude=float_, _is\_skidding=bool_, _skid\_magnitude=float_, _skid\_normal=Vector_, _drive\_torque=float_, _brake\_torque=float_, _abs\_activated=bool_)

Break Wheel Status

Parameters:

**status** ( _WheelStatus_)

Returns:

contact (bool):

contact\_point (Vector):

phys\_material (PhysicalMaterial):

normalized\_suspension\_length (float):

spring\_force (float):

slip\_angle (float):

is\_slipping (bool):

slip\_magnitude (float):

is\_skidding (bool):

skid\_magnitude (float):

skid\_normal (Vector):

drive\_torque (float):

brake\_torque (float):

abs\_activated (bool):

Return type:

tuple

_classmethod_ break\_wheeled\_snapshot( _snapshot)->(transform=Transform,linear\_velocity=Vector,angular\_velocity=Vector,selected\_gear=int32,engine\_rpm=float,wheel\_snapshots=Array[WheelSnapshot]_)

Break Wheeled Snapshot

Parameters:

**snapshot** ( _WheeledSnaphotData_)

Returns:

transform (Transform):

linear\_velocity (Vector):

angular\_velocity (Vector):

selected\_gear (int32):

engine\_rpm (float):

wheel\_snapshots (Array[WheelSnapshot]):

Return type:

tuple


---

**enable_mechanical_sim**( _state_) → `None`

Enable or completely bypass the ProcessMechanicalSimulation call

Parameters:

**state** ( _bool_)


---

**enable_suspension**( _state_) → `None`

Enable or completely bypass the ApplySuspensionForces call

Parameters:

**state** ( _bool_)


---

**enable_wheel_friction**( _state_) → `None`

Enable or completely bypass the ApplyWheelFrictionForces call

Parameters:

**state** ( _bool_)


---

**get_engine_max_rotation_speed**() → `float`

Get current engine’s max rotation speed

Return type:

float


---

**get_engine_rotation_speed**() → `float`

Get current engine’s rotation speed

Return type:

float


---

**get_num_wheels**() → `int32`

Get Num Wheels

Return type:

int32


---

**get_snapshot**() → `WheeledSnaphotData`

Grab a snapshot of the vehicle instance dynamic state

Return type:

WheeledSnaphotData


---

**get_wheel_state**( _wheel_index_) → `WheelStatus`

Get a wheels current simulation state

Parameters:

**wheel\_index** ( _int32_)

Return type:

WheelStatus


---

_classmethod_ make_wheel_snapshot( _suspension_offset_, _wheel_rotation_angle_, _steering_angle_, _wheel_radius_, _wheel_angular_velocity_)→WheelSnapshot

Make Wheel Snapshot

Parameters:

- **suspension\_offset** ( _float_)

- **wheel\_rotation\_angle** ( _float_)

- **steering\_angle** ( _float_)

- **wheel\_radius** ( _float_)

- **wheel\_angular\_velocity** ( _float_)


Return type:

WheelSnapshot

_classmethod_ make\_wheel\_status( _contact_, _phys\_material_, _normalized\_suspension\_length_, _spring\_force_, _slip\_angle_, _is\_slipping_, _slip\_magnitude_, _is\_skidding_, _skid\_magnitude_, _drive\_torque_, _brake\_torque_, _abs\_activated)->(WheelStatus_, _contact\_point=Vector_, _skid\_normal=Vector_)

Make Wheel Status

Parameters:

- **contact** ( _bool_)

- **phys\_material** ( _PhysicalMaterial_)

- **normalized\_suspension\_length** ( _float_)

- **spring\_force** ( _float_)

- **slip\_angle** ( _float_)

- **is\_slipping** ( _bool_)

- **slip\_magnitude** ( _float_)

- **is\_skidding** ( _bool_)

- **skid\_magnitude** ( _float_)

- **drive\_torque** ( _float_)

- **brake\_torque** ( _float_)

- **abs\_activated** ( _bool_)


Returns:

contact\_point (Vector):

skid\_normal (Vector):

Return type:

tuple


---

_classmethod_ make_wheeled_snapshot( _transform_, _linear_velocity_, _angular_velocity_, _selected_gear_, _engine_rpm_, _wheel_snapshots_)→WheeledSnaphotData

Make Wheeled Snapshot

Parameters:

- **transform** ( _Transform_)

- **linear\_velocity** ( _Vector_)

- **angular\_velocity** ( _Vector_)

- **selected\_gear** ( _int32_)

- **engine\_rpm** ( _float_)

- **wheel\_snapshots** ( _Array_ _\_ [_WheelSnapshot_ _]_)


Return type:

WheeledSnaphotData


---

**set_abs_enabled**( _wheel_index_, _enabled_) → `None`

Set ABSEnabled

Parameters:

- **wheel\_index** ( _int32_)

- **enabled** ( _bool_)



---

**set_affected_by_brake**( _wheel_index_, _enabled_) → `None`

Set Affected by Brake

Parameters:

- **wheel\_index** ( _int32_)

- **enabled** ( _bool_)



---

**set_affected_by_engine**( _wheel_index_, _enabled_) → `None`

Set Affected by Engine

Parameters:

- **wheel\_index** ( _int32_)

- **enabled** ( _bool_)



---

**set_affected_by_handbrake**( _wheel_index_, _enabled_) → `None`

Set Affected by Handbrake

Parameters:

- **wheel\_index** ( _int32_)

- **enabled** ( _bool_)



---

**set_affected_by_steering**( _wheel_index_, _enabled_) → `None`

Set Affected by Steering

Parameters:

- **wheel\_index** ( _int32_)

- **enabled** ( _bool_)



---

**set_brake_torque**( _brake_torque_, _wheel_index_) → `None`

Set Brake Torque

Parameters:

- **brake\_torque** ( _float_)

- **wheel\_index** ( _int32_)



---

**set_differential_front_rear_split**( _front_rear_slpit_) → `None`

Set Differential Front Rear Split

Parameters:

**front\_rear\_slpit** ( _float_)


---

**set_downforce_coefficient**( _downforce_coeff_) → `None`

Set Downforce Coefficient

Parameters:

**downforce\_coeff** ( _float_)


---

**set_drag_coefficient**( _drag_coeff_) → `None`

Set Drag Coefficient

Parameters:

**drag\_coeff** ( _float_)


---

**set_drive_torque**( _drive_torque_, _wheel_index_) → `None`

Set Drive Torque

Parameters:

- **drive\_torque** ( _float_)

- **wheel\_index** ( _int32_)



---

**set_max_engine_torque**( _torque_) → `None`

change handling via blueprint at runtime

Parameters:

**torque** ( _float_)


---

**set_snapshot**( _snapshot_in_) → `None`

Set snapshot of vehicle instance dynamic state

Parameters:

**snapshot\_in** ( _WheeledSnaphotData_)


---

**set_suspension_params**( _rate_, _damping_, _preload_, _max_raise_, _max_drop_, _wheel_index_) → `None`

Set Suspension Params

Parameters:

- **rate** ( _float_)

- **damping** ( _float_)

- **preload** ( _float_)

- **max\_raise** ( _float_)

- **max\_drop** ( _float_)

- **wheel\_index** ( _int32_)



---

**set_torque_combine_method**( _combine_method_, _wheel_index_) → `None`

Set Torque Combine Method

Parameters:

- **combine\_method** ( _TorqueCombineMethod_)

- **wheel\_index** ( _int32_)



---

**set_traction_control_enabled**( _wheel_index_, _enabled_) → `None`

Set Traction Control Enabled

Parameters:

- **wheel\_index** ( _int32_)

- **enabled** ( _bool_)



---

**set_wheel_class**( _wheel_index_, _wheel_class_) → `None`

Set Wheel Class

Parameters:

- **wheel\_index** ( _int32_)

- **wheel\_class** ( _type_ _(_ _Class_ _)_)



---

**set_wheel_friction_multiplier**( _wheel_index_, _friction_) → `None`

Set Wheel Friction Multiplier

Parameters:

- **wheel\_index** ( _int32_)

- **friction** ( _float_)



---

**set_wheel_handbrake_torque**( _wheel_index_, _torque_) → `None`

Set Wheel Handbrake Torque

Parameters:

- **wheel\_index** ( _int32_)

- **torque** ( _float_)



---

**set_wheel_max_brake_torque**( _wheel_index_, _torque_) → `None`

Set Wheel Max Brake Torque

Parameters:

- **wheel\_index** ( _int32_)

- **torque** ( _float_)



---

**set_wheel_max_steer_angle**( _wheel_index_, _angle_degrees_) → `None`

Set Wheel Max Steer Angle

Parameters:

- **wheel\_index** ( _int32_)

- **angle\_degrees** ( _float_)



---

**set_wheel_radius**( _wheel_index_, _radius_) → `None`

Set Wheel Radius

Parameters:

- **wheel\_index** ( _int32_)

- **radius** ( _float_)



---

**set_wheel_slip_graph_multiplier**( _wheel_index_, _multiplier_) → `None`

Set Wheel Slip Graph Multiplier

Parameters:

- **wheel\_index** ( _int32_)

- **multiplier** ( _float_)



---

_property_ `wheels`: None

[Read-Only] Our instanced wheels

**Type:**

( Array\ [ChaosVehicleWheel])

### Table of Contents

- `unreal.ChaosWheeledVehicleMovementComponent`
  - `ChaosWheeledVehicleMovementComponent`
    - `ChaosWheeledVehicleMovementComponent.break_wheel_snapshot()`
    - `ChaosWheeledVehicleMovementComponent.break_wheel_status()`
    - `ChaosWheeledVehicleMovementComponent.break_wheeled_snapshot()`
    - `ChaosWheeledVehicleMovementComponent.enable_mechanical_sim()`
    - `ChaosWheeledVehicleMovementComponent.enable_suspension()`
    - `ChaosWheeledVehicleMovementComponent.enable_wheel_friction()`
    - `ChaosWheeledVehicleMovementComponent.get_engine_max_rotation_speed()`
    - `ChaosWheeledVehicleMovementComponent.get_engine_rotation_speed()`
    - `ChaosWheeledVehicleMovementComponent.get_num_wheels()`
    - `ChaosWheeledVehicleMovementComponent.get_snapshot()`
    - `ChaosWheeledVehicleMovementComponent.get_wheel_state()`
    - `ChaosWheeledVehicleMovementComponent.make_wheel_snapshot()`
    - `ChaosWheeledVehicleMovementComponent.make_wheel_status()`
    - `ChaosWheeledVehicleMovementComponent.make_wheeled_snapshot()`
    - `ChaosWheeledVehicleMovementComponent.set_abs_enabled()`
    - `ChaosWheeledVehicleMovementComponent.set_affected_by_brake()`
    - `ChaosWheeledVehicleMovementComponent.set_affected_by_engine()`
    - `ChaosWheeledVehicleMovementComponent.set_affected_by_handbrake()`
    - `ChaosWheeledVehicleMovementComponent.set_affected_by_steering()`
    - `ChaosWheeledVehicleMovementComponent.set_brake_torque()`
    - `ChaosWheeledVehicleMovementComponent.set_differential_front_rear_split()`
    - `ChaosWheeledVehicleMovementComponent.set_downforce_coefficient()`
    - `ChaosWheeledVehicleMovementComponent.set_drag_coefficient()`
    - `ChaosWheeledVehicleMovementComponent.set_drive_torque()`
    - `ChaosWheeledVehicleMovementComponent.set_max_engine_torque()`
    - `ChaosWheeledVehicleMovementComponent.set_snapshot()`
    - `ChaosWheeledVehicleMovementComponent.set_suspension_params()`
    - `ChaosWheeledVehicleMovementComponent.set_torque_combine_method()`
    - `ChaosWheeledVehicleMovementComponent.set_traction_control_enabled()`
    - `ChaosWheeledVehicleMovementComponent.set_wheel_class()`
    - `ChaosWheeledVehicleMovementComponent.set_wheel_friction_multiplier()`
    - `ChaosWheeledVehicleMovementComponent.set_wheel_handbrake_torque()`
    - `ChaosWheeledVehicleMovementComponent.set_wheel_max_brake_torque()`
    - `ChaosWheeledVehicleMovementComponent.set_wheel_max_steer_angle()`
    - `ChaosWheeledVehicleMovementComponent.set_wheel_radius()`
    - `ChaosWheeledVehicleMovementComponent.set_wheel_slip_graph_multiplier()`
    - `ChaosWheeledVehicleMovementComponent.wheels`