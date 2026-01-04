# unreal.HeadMountedDisplayFunctionLibrary

```python
class unreal.HeadMountedDisplayFunctionLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Head Mounted Display Function Library

**C++ Source:**

- **Plugin**: XRBase

- **Module**: XRBase

- **File**: HeadMountedDisplayFunctionLibrary.h



---

_classmethod_ calibrate_external_tracking_to_hmd( _external_tracking_transform_)→None

Called to calibrate the offset transform between an external tracking source and the internal tracking source
(e.g. mocap tracker to and HMD tracker). This should be called once per session, or when the physical relationship
between the external tracker and internal tracker changes (e.g. it was bumped or reattached). After calibration,
calling UpdateExternalTrackingPosition will try to correct the internal tracker to the calibrated offset to prevent
drift between the two systems

Parameters:

**external\_tracking\_transform** ( _Transform_) – The transform in world-coordinates, of the reference marker of the external tracking system


---

_classmethod_ clear_xr_timed_input_action_delegate( _action_path_)→None

/ Clear a delegate to get an OpenXR action event with action time.

Parameters:

**action\_path** ( _Name_)


---

_classmethod_ connect_remote_xr_device( _ip_address_, _bit_rate_)→XRDeviceConnectionResult

Connect to a remote device

Parameters:

- **ip\_address** ( _str_)

- **bit\_rate** ( _int32_)


Return type:

XRDeviceConnectionResult


---

_classmethod_ disconnect_remote_xr_device()→None

Disconnect remote AR Device


---

_classmethod_ enable_hmd( _enable_)→bool

Switches to/from using HMD and stereo rendering.

Parameters:

**enable** ( _bool_) – (in) ‘true’ to enable HMD / stereo; ‘false’ otherwise

Returns:

(Boolean) True, if the request was successful.

Return type:

bool


---

_classmethod_ enumerate_tracked_devices( _system_id='None'_, _device_type=XRTrackedDeviceType.ANY_)→Array\ [XRDeviceId]

Cross XR-System query that will list all XR devices currently being tracked.

Parameters:

- **system\_id** ( _Name_) – (Optional) Specifies an explicit system to poll devices from (use if you want only devices belonging to one explicit XR ecosystem, e.g. ‘OculusHMD’, or ‘OpenXR’)

- **device\_type** ( _XRTrackedDeviceType_) – Specifies the type of device to query for - defaults to ‘Any’ (meaning ‘All’).


Returns:

A list of device identifiers matching the query. Use these to query and operate on the device (e.g. through GetDevicePose, AddDeviceVisualizationComponent, etc.)

Return type:

Array\ [XRDeviceId]


---

_classmethod_ get_controller_transform_for_time2( _world_context_, _controller_index_, _motion_source_, _time_)→(time_was_used=bool,orientation=Rotator,position=Vector,provided_linear_velocity=bool,linear_velocity=Vector,provided_angular_velocity=bool,angular_velocity=Rotator,provided_linear_acceleration=bool,linear_acceleration=Vector)orNone

Get the transform and potentially velocity data at a specified time near the current frame in unreal world space.
This is intended for use with sub-frame input action timing data from SetXRTimedInputActionDelegate, or future support for timestamps in the core input system.
The valid time window is platform dependent, but the intention per OpenXR is to fetch transforms for times from, at most, the previous few frames in the past or future.
The OpenXR spec suggests that 50ms in the past should return an accurate result. There is no guarantee for the future, but the underlying system is likely to have been
designed to predict out to about 50ms as well.
On some platforms this will always just return a cached position and rotation, ignoring time. bTimeWasUsed will be false in that case.
AngularVelocity is a Rotator in degrees/second.
Be aware that this Rotator may have windings (rotations greater than 360 degrees) and some mathmatical operations (such as conversion to quaternion) will remove the windings.
In some cases that is OK becuase the resulting final rotation is the same, but in some cases it would generate incorrect results.

Parameters:

- **world\_context** ( _Object_)

- **controller\_index** ( _int32_)

- **motion\_source** ( _Name_)

- **time** ( _Timespan_)


Returns:

time\_was\_used (bool):

orientation (Rotator):

position (Vector):

provided\_linear\_velocity (bool):

linear\_velocity (Vector):

provided\_angular\_velocity (bool):

angular\_velocity (Rotator):

provided\_linear\_acceleration (bool):

linear\_acceleration (Vector):

Return type:

tuple or None


---

_classmethod_ get_current_interaction_profile( _hand_)→strorNone

Get the openXR interaction profile name for the given controller. Returns true if the openxr call is successfully made. The string may be empty
if there is no interaction profile associated with the controller.

Parameters:

**hand** ( _ControllerHand_)

Returns:

interaction\_profile (str):

Return type:

str or None

_classmethod_ get\_device\_pose( _xr\_device\_id)->(is\_tracked=bool_, _orientation=Rotator_, _has\_positional\_tracking=bool_, _position=Vector_)

Cross XR-System query that returns a specific device’s tracked position and orientation (in tracking space).

Parameters:

**xr\_device\_id** ( _XRDeviceId_) – Specifies the device you’re querying for.

Returns:

is\_tracked (bool): [out] Details if the specified device is tracked (i.e. should the rest of the outputs be used)

orientation (Rotator): [out] Represents the device’s current rotation - NOTE: this value is not late updated and will be behind the render thread

has\_positional\_tracking (bool): [out] Details if the specified device has positional tracking (i.e. if the position output should be used)

position (Vector): [out] Represents the device’s current position - NOTE: this value is not late updated and will be behind the render thread

Return type:

tuple

_classmethod_ get\_device\_world\_pose( _world\_context=None_, _xr\_device\_id)->(is\_tracked=bool_, _orientation=Rotator_, _has\_positional\_tracking=bool_, _position=Vector_)

Cross XR-System query that returns a specific device’s position and orientation in world space.

Parameters:

- **world\_context** ( _Object_)

- **xr\_device\_id** ( _XRDeviceId_) – Specifies the device you’re querying for.


Returns:

is\_tracked (bool): [out] Details if the specified device is tracked (i.e. should the rest of the outputs be used)

orientation (Rotator): [out] Represents the device’s current rotation - NOTE: this value is not late updated and will be behind the render thread

has\_positional\_tracking (bool): [out] Details if the specified device has positional tracking (i.e. if the position output should be used)

position (Vector): [out] Represents the device’s current position - NOTE: this value is not late updated and will be behind the render thread

Return type:

tuple


---

_classmethod_ get_hand_tracking_state( _world_context_, _xr_space_type_, _hand_)→XRHandTrackingState

Cross XR-System query that returns critical information about the motion controller (position, orientation, hand/finger position)

Parameters:

- **world\_context** ( _Object_) – Any object in the world (the player pawn would work). Used in PIE to make sure we get this data from a motioncontroller component that is currently active, rather than one in an editor view world that is never tracked.

- **xr\_space\_type** ( _XRSpaceType_) – Can switch between unreal world coordinates and tracking space coordinates. Tracking space may be useful with non-1:1 world scales.

- **hand** ( _ControllerHand_) – Indicates which hand we want data for.


Returns:

hand\_tracking\_state (XRHandTrackingState):

Return type:

XRHandTrackingState


---

_classmethod_ get_hmd_data( _world_context_)→XRHMDData

Cross XR-System query that returns critical information about the HMD display (position, orientation, device name)

Parameters:

**world\_context** ( _Object_)

Returns:

hmd\_data (XRHMDData):

Return type:

XRHMDData


---

_classmethod_ get_hmd_device_name()→Name

Returns the name of the device, so scripts can modify their behaviour appropriately

Returns:

FName specific to the currently active HMD device type. “None” implies no device, “Unknown” implies a device with no description.

Return type:

Name


---

_classmethod_ get_hmd_worn_state()→HMDWornState

Returns the worn state of the device.

Returns:

Unknown, Worn, NotWorn. If the platform does not detect this it will always return Unknown.

Return type:

HMDWornState


---

_classmethod_ get_motion_controller_state( _world_context_, _xr_space_type_, _hand_, _controller_pose_type_)→XRMotionControllerState

Cross XR-System query that returns critical information about the motion controller (position, orientation)

Parameters:

- **world\_context** ( _Object_) – Any object in the world (the player pawn would work). Used in PIE to make sure we get this data from a motioncontroller component that is currently active, rather than one in an editor view world that is never tracked.

- **xr\_space\_type** ( _XRSpaceType_) – Can switch between unreal world coordinates and tracking space coordinates. Tracking space may be useful with non-1:1 world scales.

- **hand** ( _ControllerHand_) – Indicates which hand we want data for.

- **controller\_pose\_type** ( _XRControllerPoseType_)


Returns:

motion\_controller\_state (XRMotionControllerState):

Return type:

XRMotionControllerState


---

_classmethod_ get_num_of_tracking_sensors()→int32

If the HMD has multiple positional tracking sensors, return a total number of them currently connected.

Return type:

int32

_classmethod_ get\_orientation\_and\_position( _)->(device\_rotation=Rotator_, _device\_position=Vector_)

Grabs the current orientation and position for the HMD. If positional tracking is not available, DevicePosition will be a zero vector

Returns:

device\_rotation (Rotator): (out) The device’s current rotation

device\_position (Vector): (out) The device’s current position, in its own tracking space

Return type:

tuple


---

_classmethod_ get_pixel_density()→float

Returns the current XR pixel density. This sets the final
render target size as a factor of the recommended texture size.

Just before the render target is displayed by the HMD, it’s distorted by the device’s
runtime compositor to counteract the distortion a user would normally experience
when looking through the device’s lenses. The recommended texture size is the
size that will result in no undersampling in the most distorted area of the view
after this step is performed.

This function is deprecated, and will return the HMD secondary screen percentage divided by 100.
deprecated: Replaced with GetHMDSecondaryScreenPercentage for 5.6.

Returns:

(float) The pixel density to be used in XR mode.

Return type:

float


---

_classmethod_ get_play_area_bounds( _origin=HMDTrackingOrigin.STAGE_)→Vector2D

Get the bounds of the area where the user can freely move while remaining tracked centered around the specified origin

Parameters:

**origin** ( _HMDTrackingOrigin_)

Return type:

Vector2D


---

_classmethod_ get_play_area_rect()→(out_transform=Transform,out_rect=Vector2D)orNone

Get the transform and dimensions of the playable area rectangle. Returns false if none currently specified/available.

Returns:

out\_transform (Transform):

out\_rect (Vector2D):

Return type:

tuple or None


---

_classmethod_ get_tracking_origin()→HMDTrackingOrigin

Returns current tracking origin type (eye level or floor level).

Return type:

HMDTrackingOrigin


---

_classmethod_ get_tracking_origin_transform( _origin_)→TransformorNone

Get the transform of the specified tracking origin, if available.

Parameters:

**origin** ( _HMDTrackingOrigin_)

Returns:

out\_transform (Transform):

Return type:

Transform or None

_classmethod_ get\_tracking\_sensor\_parameters( _index=0)->(origin=Vector_, _rotation=Rotator_, _left\_fov=float_, _right\_fov=float_, _top\_fov=float_, _bottom\_fov=float_, _distance=float_, _near\_plane=float_, _far\_plane=float_, _is\_active=bool_)

If the HMD has a positional sensor, this will return the game-world location of it, as well as the parameters for the bounding region of tracking.
This allows an in-game representation of the legal positional tracking range. All values will be zeroed if the sensor is not available or the HMD does not support it.

Parameters:

**index** ( _int32_) – (in) Index of the tracking sensor to query

Returns:

origin (Vector): (out) Origin, in world-space, of the sensor

rotation (Rotator): (out) Rotation, in world-space, of the sensor

left\_fov (float): (out) Field-of-view, left from center, in degrees, of the valid tracking zone of the sensor

right\_fov (float): (out) Field-of-view, right from center, in degrees, of the valid tracking zone of the sensor

top\_fov (float): (out) Field-of-view, top from center, in degrees, of the valid tracking zone of the sensor

bottom\_fov (float): (out) Field-of-view, bottom from center, in degrees, of the valid tracking zone of the sensor

distance (float): (out) Nominal distance to sensor, in world-space

near\_plane (float): (out) Near plane distance of the tracking volume, in world-space

far\_plane (float): (out) Far plane distance of the tracking volume, in world-space

is\_active (bool): (out) True, if the query for the specified sensor succeeded.

Return type:

tuple


---

_classmethod_ get_tracking_to_world_transform( _world_context=None_)→Transform

Returns a transform that can be used to convert points from tracking space to world space.
Does NOT include the set WorldToMeters scale, as that is added in by the backing XR system to their tracking space poses.

Parameters:

**world\_context** ( _Object_)

Return type:

Transform


---

_classmethod_ get_version_string()→str

Returns name of tracking system specific version string.

Return type:

str

_classmethod_ get\_vr\_focus\_state( _)->(use\_focus=bool_, _has\_focus=bool_)

Returns current state of VR focus.

Returns:

use\_focus (bool): (out) if set to true, then this App does use VR focus.

has\_focus (bool): (out) if set to true, then this App currently has VR focus.

Return type:

tuple


---

_classmethod_ get_world_to_meters_scale( _world_context=None_)→float

Returns the World to Meters scale, which corresponds to the scale of the world as perceived by the player

Parameters:

**world\_context** ( _Object_)

Returns:

How many Unreal units correspond to one meter in the real world

Return type:

float


---

_classmethod_ get_xr_secondary_screen_percentage()→float

Returns the current XR secondary screen precentage. This sets the final
render target size as a percentage of the recommended texture size.

Just before the render target is displayed by the HMD, it’s distorted by the device’s
runtime compositor to counteract the distortion a user would normally experience
when looking through the device’s lenses. The recommended texture size is the
size that will result in no undersampling in the most distorted area of the view
after this step is performed.

Returns:

(float) The secondary screen percentage to be used in XR mode.

Return type:

float


---

_classmethod_ get_xr_system_flags()→int32

Returns the flags for the device, so scripts can modify their behaviour appropriately

Returns:

IsAR, IsTablet, IsHeadMounted. Returns false

Return type:

int32


---

_classmethod_ has_valid_tracking_position()→bool

If the HMD supports positional tracking, whether or not we are currently being tracked

Return type:

bool


---

_classmethod_ is_device_tracking( _xr_device_id_)→bool

Cross XR-System query that returns whether the specified device is tracked or not.

Parameters:

**xr\_device\_id** ( _XRDeviceId_) – Specifies the device you’re querying for.

Return type:

bool


---

_classmethod_ is_head_mounted_display_connected()→bool

Returns whether or not the HMD hardware is connected and ready to use. It may or may not actually be in use.

Returns:

(Boolean) status whether the HMD hardware is connected and ready to use. It may or may not actually be in use.

Return type:

bool


---

_classmethod_ is_head_mounted_display_enabled()→bool

Returns whether or not we are currently using the head mounted display.

Returns:

(Boolean) status of HMD

Return type:

bool


---

_classmethod_ is_spectator_screen_mode_controllable()→bool

Return true if spectator screen mode control is available.

Return type:

bool


---

_classmethod_ reset_orientation_and_position( _yaw=0.000000_, _options=OrientPositionSelector.ORIENTATION_AND_POSITION_)→None

Resets orientation by setting roll and pitch to 0, assuming that current yaw is forward direction and assuming
current position as a ‘zero-point’ (for positional tracking).

Parameters:

- **yaw** ( _float_) – (in) the desired yaw to be set after orientation reset.

- **options** ( _OrientPositionSelector_) – (in) specifies either position, orientation or both should be reset.



---

_classmethod_ set_clipping_planes( _near_, _far_)→None

Sets near and far clipping planes (NCP and FCP) for stereo rendering. Similar to ‘stereo ncp= fcp’ console command, but NCP and FCP set by this
call won’t be saved in .ini file.

Parameters:

- **near** ( _float_) – (in) Near clipping plane, in centimeters

- **far** ( _float_) – (in) Far clipping plane, in centimeters



---

_classmethod_ set_hmd_color_scale_and_bias( _color_scale_, _color_bias_)→bool

Multiply the post-compositor frame by a color and add a bias.
LayerColor = LayerColor \* ColorScale + ColorBias

Parameters:

- **color\_scale** ( _LinearColor_) – (in) Color to multiply the compositor layer by

- **color\_bias** ( _LinearColor_) – (in) Color to offset the compositor layer by


Returns:

(boolean) True if successful, false if unsuccessful or unsupported.

Return type:

bool


---

_classmethod_ set_spectator_screen_mode( _mode_)→None

Sets the social screen mode.

Parameters:

**mode** ( _SpectatorScreenMode_) – (in) The social screen Mode.


---

_classmethod_ set_spectator_screen_mode_texture_plus_eye_layout( _eye_rect_min_, _eye_rect_max_, _texture_rect_min_, _texture_rect_max_, _draw_eye_first=True_, _clear_black=False_, _use_alpha=False_)→None

Setup the layout for ESpectatorScreenMode::TexturePlusEye.

Parameters:

- **eye\_rect\_min** ( _Vector2D_)

- **eye\_rect\_max** ( _Vector2D_)

- **texture\_rect\_min** ( _Vector2D_)

- **texture\_rect\_max** ( _Vector2D_)

- **draw\_eye\_first** ( _bool_)

- **clear\_black** ( _bool_)

- **use\_alpha** ( _bool_)



---

_classmethod_ set_spectator_screen_texture( _texture_)→None

Change the texture displayed on the social screen

Parameters:

**texture** ( _Texture_)


---

_classmethod_ set_tracking_origin( _origin_)→None

Sets current tracking origin type (eye level or floor level).

Parameters:

**origin** ( _HMDTrackingOrigin_)


---

_classmethod_ set_world_to_meters_scale( _world_context=None_, _new_scale=100.000000_)→None

Sets the World to Meters scale, which changes the scale of the world as perceived by the player

Parameters:

- **world\_context** ( _Object_)

- **new\_scale** ( _float_) – Specifies how many Unreal units correspond to one meter in the real world



---

_classmethod_ set_xr_disconnect_delegate( _disconnected_delegate_)→None

Set XRDisconnect Delegate

Parameters:

**disconnected\_delegate** ( _XRDeviceOnDisconnectDelegate_)


---

_classmethod_ set_xr_timed_input_action_delegate( _action_name_, _delegate_)→None

Hook up a delegate to get an OpenXR action event with action time.
For a boolean input the the ‘value’ parameter of the delegate will be 1.0 for a press and 0.0 for a release. For an analog input the value’s range is action and platform specific.
Use in combination with GetControllerTransformForTime2 for potentially improved temporal transform precision and velocity data.
“Left Grip” is an example of a valid ActionName.
Note: this is likely to be replaced by native support for event times in the core input system at some time in the future.

Parameters:

- **action\_name** ( _Name_)

- **delegate** ( _XRTimedInputActionDelegate_)



---

_classmethod_ update_external_tracking_hmd_position( _external_tracking_transform_)→None

Called after calibration to attempt to pull the internal tracker (e.g. HMD tracking) in line with the external tracker
(e.g. mocap tracker). This will set the internal tracker’s base offset and rotation to match and realign the two systems.
This can be called every tick, or whenever realignment is desired. Note that this may cause choppy movement if the two
systems diverge relative to each other, or a big jump if called infrequently when there has been significant drift

Parameters:

**external\_tracking\_transform** ( _Transform_) – The transform in world-coordinates, of the reference marker of the external tracking system

### Table of Contents

- `unreal.HeadMountedDisplayFunctionLibrary`
  - `HeadMountedDisplayFunctionLibrary`
    - `HeadMountedDisplayFunctionLibrary.calibrate_external_tracking_to_hmd()`
    - `HeadMountedDisplayFunctionLibrary.clear_xr_timed_input_action_delegate()`
    - `HeadMountedDisplayFunctionLibrary.connect_remote_xr_device()`
    - `HeadMountedDisplayFunctionLibrary.disconnect_remote_xr_device()`
    - `HeadMountedDisplayFunctionLibrary.enable_hmd()`
    - `HeadMountedDisplayFunctionLibrary.enumerate_tracked_devices()`
    - `HeadMountedDisplayFunctionLibrary.get_controller_transform_for_time2()`
    - `HeadMountedDisplayFunctionLibrary.get_current_interaction_profile()`
    - `HeadMountedDisplayFunctionLibrary.get_device_pose()`
    - `HeadMountedDisplayFunctionLibrary.get_device_world_pose()`
    - `HeadMountedDisplayFunctionLibrary.get_hand_tracking_state()`
    - `HeadMountedDisplayFunctionLibrary.get_hmd_data()`
    - `HeadMountedDisplayFunctionLibrary.get_hmd_device_name()`
    - `HeadMountedDisplayFunctionLibrary.get_hmd_worn_state()`
    - `HeadMountedDisplayFunctionLibrary.get_motion_controller_state()`
    - `HeadMountedDisplayFunctionLibrary.get_num_of_tracking_sensors()`
    - `HeadMountedDisplayFunctionLibrary.get_orientation_and_position()`
    - `HeadMountedDisplayFunctionLibrary.get_pixel_density()`
    - `HeadMountedDisplayFunctionLibrary.get_play_area_bounds()`
    - `HeadMountedDisplayFunctionLibrary.get_play_area_rect()`
    - `HeadMountedDisplayFunctionLibrary.get_tracking_origin()`
    - `HeadMountedDisplayFunctionLibrary.get_tracking_origin_transform()`
    - `HeadMountedDisplayFunctionLibrary.get_tracking_sensor_parameters()`
    - `HeadMountedDisplayFunctionLibrary.get_tracking_to_world_transform()`
    - `HeadMountedDisplayFunctionLibrary.get_version_string()`
    - `HeadMountedDisplayFunctionLibrary.get_vr_focus_state()`
    - `HeadMountedDisplayFunctionLibrary.get_world_to_meters_scale()`
    - `HeadMountedDisplayFunctionLibrary.get_xr_secondary_screen_percentage()`
    - `HeadMountedDisplayFunctionLibrary.get_xr_system_flags()`
    - `HeadMountedDisplayFunctionLibrary.has_valid_tracking_position()`
    - `HeadMountedDisplayFunctionLibrary.is_device_tracking()`
    - `HeadMountedDisplayFunctionLibrary.is_head_mounted_display_connected()`
    - `HeadMountedDisplayFunctionLibrary.is_head_mounted_display_enabled()`
    - `HeadMountedDisplayFunctionLibrary.is_spectator_screen_mode_controllable()`
    - `HeadMountedDisplayFunctionLibrary.reset_orientation_and_position()`
    - `HeadMountedDisplayFunctionLibrary.set_clipping_planes()`
    - `HeadMountedDisplayFunctionLibrary.set_hmd_color_scale_and_bias()`
    - `HeadMountedDisplayFunctionLibrary.set_spectator_screen_mode()`
    - `HeadMountedDisplayFunctionLibrary.set_spectator_screen_mode_texture_plus_eye_layout()`
    - `HeadMountedDisplayFunctionLibrary.set_spectator_screen_texture()`
    - `HeadMountedDisplayFunctionLibrary.set_tracking_origin()`
    - `HeadMountedDisplayFunctionLibrary.set_world_to_meters_scale()`
    - `HeadMountedDisplayFunctionLibrary.set_xr_disconnect_delegate()`
    - `HeadMountedDisplayFunctionLibrary.set_xr_timed_input_action_delegate()`
    - `HeadMountedDisplayFunctionLibrary.update_external_tracking_hmd_position()`