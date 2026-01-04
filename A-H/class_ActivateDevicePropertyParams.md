# unreal.ActivateDevicePropertyParams

```python
class unreal.ActivateDevicePropertyParams(user_id:PlatformUserId=\[\], device_id:InputDeviceId=\[\], looping:bool=False, ignore_time_dilation:bool=False, play_while_paused:bool=False)
```


**Bases:** ``StructBase``


Parameters for the UInputDeviceSubsystem::ActivateDeviceProperty function

**C++ Source:**

- **Module**: Engine

- **File**: InputDeviceSubsystem.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `device_id` (InputDeviceId): [Read-Write] The Input Device that should receive the device property. If nothing is specified here,
then the Platform User’s default input device will be used.

The default input device is obtained from IPlatformInputDeviceMapper::GetPrimaryInputDeviceForUser

- `ignore_time_dilation` (bool): [Read-Write] If true, then this device property will ignore dilated delta time and use the Applications delta time instead

- `looping` (bool): [Read-Write] If true, then the input device property will not be removed after it’s evaluation time has completed.
Instead, it will remain active until manually removed with a RemoveDeviceProperty call.

- `play_while_paused` (bool): [Read-Write] If true, then this device property will be played even if the game world is paused.

- `user_id` (PlatformUserId): [Read-Write] The Platform User whose device’s should receive the device property



---

_property_ `device_id`: InputDeviceId

[Read-Write] The Input Device that should receive the device property. If nothing is specified here,
then the Platform User’s default input device will be used.

The default input device is obtained from IPlatformInputDeviceMapper::GetPrimaryInputDeviceForUser

**Type:**

( InputDeviceId)


---

_property_ `ignore_time_dilation`: bool

[Read-Write] If true, then this device property will ignore dilated delta time and use the Applications delta time instead

**Type:**

( bool)


---

_property_ `looping`: bool

[Read-Write] If true, then the input device property will not be removed after it’s evaluation time has completed.
Instead, it will remain active until manually removed with a RemoveDeviceProperty call.

**Type:**

( bool)


---

_property_ `play_while_paused`: bool

[Read-Write] If true, then this device property will be played even if the game world is paused.

**Type:**

( bool)


---

_property_ `user_id`: PlatformUserId

[Read-Write] The Platform User whose device’s should receive the device property

**Type:**

( PlatformUserId)

### Table of Contents

- `unreal.ActivateDevicePropertyParams`
  - `ActivateDevicePropertyParams`
    - `ActivateDevicePropertyParams.device_id`
    - `ActivateDevicePropertyParams.ignore_time_dilation`
    - `ActivateDevicePropertyParams.looping`
    - `ActivateDevicePropertyParams.play_while_paused`
    - `ActivateDevicePropertyParams.user_id`