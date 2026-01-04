# unreal.DisplayClusterProjectionBlueprintLib

```python
class unreal.DisplayClusterProjectionBlueprintLib(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Blueprint API function library

**C++ Source:**

- **Plugin**: nDisplay

- **Module**: DisplayClusterProjection

- **File**: DisplayClusterProjectionBlueprintLib.h



---

_classmethod_ camera_policy_set_camera( _viewport_id_, _new_camera_, _fov_multiplier=1.000000_)→None

Sets camera up for ‘camera’ projection policy.

Parameters:

- **viewport\_id** ( _str_)

- **new\_camera** ( _CameraComponent_)

- **fov\_multiplier** ( _float_)



---

_classmethod_ get_api()→DisplayClusterProjectionBlueprintAPI

Get API
deprecated: GetAPI has been deprecated. All functions are now available in the main blueprint functions list under ‘nDisplay’ category.

Returns:

out\_api (DisplayClusterProjectionBlueprintAPI):

Return type:

DisplayClusterProjectionBlueprintAPI

### Table of Contents

- `unreal.DisplayClusterProjectionBlueprintLib`
  - `DisplayClusterProjectionBlueprintLib`
    - `DisplayClusterProjectionBlueprintLib.camera_policy_set_camera()`
    - `DisplayClusterProjectionBlueprintLib.get_api()`