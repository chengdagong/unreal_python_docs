# unreal.LiveLinkExampleDevice

```python
class unreal.LiveLinkExampleDevice(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``LiveLinkDevice``


Live Link Example Device

**C++ Source:**

- **Plugin**: LiveLinkExampleDevice

- **Module**: LiveLinkExampleDevice

- **File**: LiveLinkExampleDevice.h



---

**can_set_hardware_id**() → `bool`

Returns whether it’s valid to call SetHardwareId() on this device at this time.

Return type:

bool


---

**connect**() → `bool`

Attempt to establish a connection.

Return type:

bool


---

**disconnect**() → `bool`

Attempt to terminate an existing connection.

Return type:

bool


---

**get_connection_delegate**() → `ConnectionDelegate`

Get Connection Delegate

Return type:

ConnectionDelegate


---

**get_connection_status**() → `LiveLinkDeviceConnectionStatus`

Get the current connection state.

Return type:

LiveLinkDeviceConnectionStatus


---

**get_hardware_id**() → `str`

Retrieve hardware identifier (serial number, network endpoint, etc).

Return type:

str


---

**is_recording**() → `bool`

Is Recording

Return type:

bool


---

**set_hardware_id**( _hardware_id_) → `bool`

Set hardware identifier (serial number, network endpoint, etc).

Parameters:

**hardware\_id** ( _str_)

Return type:

bool


---

**start_recording**() → `bool`

Start Recording

Return type:

bool


---

**stop_recording**() → `bool`

Stop Recording

Return type:

bool

### Table of Contents

- `unreal.LiveLinkExampleDevice`
  - `LiveLinkExampleDevice`
    - `LiveLinkExampleDevice.can_set_hardware_id()`
    - `LiveLinkExampleDevice.connect()`
    - `LiveLinkExampleDevice.disconnect()`
    - `LiveLinkExampleDevice.get_connection_delegate()`
    - `LiveLinkExampleDevice.get_connection_status()`
    - `LiveLinkExampleDevice.get_hardware_id()`
    - `LiveLinkExampleDevice.is_recording()`
    - `LiveLinkExampleDevice.set_hardware_id()`
    - `LiveLinkExampleDevice.start_recording()`
    - `LiveLinkExampleDevice.stop_recording()`