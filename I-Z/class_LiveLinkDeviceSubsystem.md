# unreal.LiveLinkDeviceSubsystem

```python
class unreal.LiveLinkDeviceSubsystem(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EngineSubsystem``


Device repository with lifecycle notifications.
Facilitates cached lookups related to device and capability classes.

**C++ Source:**

- **Plugin**: LiveLinkDevice

- **Module**: LiveLinkDevice

- **File**: LiveLinkDeviceSubsystem.h



---

**get_devices_by_capability**( _capability_) → `Array\ [LiveLinkDevice]`

Get Devices by Capability

Parameters:

**capability** ( _type_ _(_ _Class_ _)_)

Returns:

out\_devices (Array[LiveLinkDevice]):

Return type:

Array\ [LiveLinkDevice]


---

**get_devices_by_class**( _device_class_) → `Array\ [LiveLinkDevice]`

Get Devices by Class

Parameters:

**device\_class** ( _type_ _(_ _Class_ _)_)

Returns:

out\_devices (Array[LiveLinkDevice]):

Return type:

Array\ [LiveLinkDevice]

### Table of Contents

- `unreal.LiveLinkDeviceSubsystem`
  - `LiveLinkDeviceSubsystem`
    - `LiveLinkDeviceSubsystem.get_devices_by_capability()`
    - `LiveLinkDeviceSubsystem.get_devices_by_class()`