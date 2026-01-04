# unreal.StereoVideoIngestDevice

```python
class unreal.StereoVideoIngestDevice(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BaseIngestLiveLinkDevice``


Ingest subfolders containing pairs of video files as stereo takes

**C++ Source:**

- **Plugin**: CaptureManagerDevices

- **Module**: StereoVideoIngestDevice

- **File**: StereoVideoIngestDevice.h



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

**get_settings**() → `StereoVideoIngestDeviceSettings`

Get Settings

Return type:

StereoVideoIngestDeviceSettings


---

**set_hardware_id**( _hardware_id_) → `bool`

Set hardware identifier (serial number, network endpoint, etc).

Parameters:

**hardware\_id** ( _str_)

Return type:

bool

### Table of Contents

- `unreal.StereoVideoIngestDevice`
  - `StereoVideoIngestDevice`
    - `StereoVideoIngestDevice.can_set_hardware_id()`
    - `StereoVideoIngestDevice.connect()`
    - `StereoVideoIngestDevice.disconnect()`
    - `StereoVideoIngestDevice.get_connection_delegate()`
    - `StereoVideoIngestDevice.get_connection_status()`
    - `StereoVideoIngestDevice.get_hardware_id()`
    - `StereoVideoIngestDevice.get_settings()`
    - `StereoVideoIngestDevice.set_hardware_id()`