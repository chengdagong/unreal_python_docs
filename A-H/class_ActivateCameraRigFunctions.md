# unreal.ActivateCameraRigFunctions

```python
class unreal.ActivateCameraRigFunctions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Blueprint functions for activating camera rigs in the base/global/visual layers.

These camera rigs run with a global, shared evaluation context that doesn’t provide any
meaningful initial result. They are activated on the camera system found to be running
on the given player controller.

Deprecated in 5.7.0

**C++ Source:**

- **Plugin**: GameplayCameras

- **Module**: GameplayCameras

- **File**: ActivateCameraRigFunctions.h



---

_classmethod_ activate_base_camera_rig( _world_context_object:Object_, _player_controller:PlayerController_, _camera_rig:CameraRigAsset_)→None

deprecated: ‘activate\_base\_camera\_rig’ was renamed to ‘activate\_persistent\_base\_camera\_rig’.


---

_classmethod_ activate_global_camera_rig( _world_context_object:Object_, _player_controller:PlayerController_, _camera_rig:CameraRigAsset_)→None

deprecated: ‘activate\_global\_camera\_rig’ was renamed to ‘activate\_persistent\_global\_camera\_rig’.


---

_classmethod_ activate_persistent_base_camera_rig( _world_context_object_, _player_controller_, _camera_rig_)→None

Activates the given camera rig prefab in the base layer.
deprecated: Use the similar functions on the GameplayCamera components or camera manager

Parameters:

- **world\_context\_object** ( _Object_)

- **player\_controller** ( _PlayerController_)

- **camera\_rig** ( _CameraRigAsset_)



---

_classmethod_ activate_persistent_global_camera_rig( _world_context_object_, _player_controller_, _camera_rig_)→None

Activates the given camera rig prefab in the global layer.
deprecated: Use the similar functions on the GameplayCamera components or camera manager

Parameters:

- **world\_context\_object** ( _Object_)

- **player\_controller** ( _PlayerController_)

- **camera\_rig** ( _CameraRigAsset_)



---

_classmethod_ activate_persistent_visual_camera_rig( _world_context_object_, _player_controller_, _camera_rig_)→None

Activates the given camera rig prefab in the visual layer.
deprecated: Use the similar functions on the GameplayCamera components or camera manager

Parameters:

- **world\_context\_object** ( _Object_)

- **player\_controller** ( _PlayerController_)

- **camera\_rig** ( _CameraRigAsset_)



---

_classmethod_ activate_visual_camera_rig( _world_context_object:Object_, _player_controller:PlayerController_, _camera_rig:CameraRigAsset_)→None

deprecated: ‘activate\_visual\_camera\_rig’ was renamed to ‘activate\_persistent\_visual\_camera\_rig’.

### Table of Contents

- `unreal.ActivateCameraRigFunctions`
  - `ActivateCameraRigFunctions`
    - `ActivateCameraRigFunctions.activate_base_camera_rig()`
    - `ActivateCameraRigFunctions.activate_global_camera_rig()`
    - `ActivateCameraRigFunctions.activate_persistent_base_camera_rig()`
    - `ActivateCameraRigFunctions.activate_persistent_global_camera_rig()`
    - `ActivateCameraRigFunctions.activate_persistent_visual_camera_rig()`
    - `ActivateCameraRigFunctions.activate_visual_camera_rig()`