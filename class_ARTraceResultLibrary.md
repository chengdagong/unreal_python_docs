# unreal.ARTraceResultLibrary

```python
class unreal.ARTraceResultLibrary(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


ARTrace Result Library

**C++ Source:**

- **Module**: AugmentedReality

- **File**: ARBlueprintLibrary.h



---

_classmethod_ get_distance_from_camera( _trace_result_)→floatParameters:

**trace\_result** ( _ARTraceResult_)

Returns:

the distance from the camera to the traced location in Unreal Units.

Return type:

float


---

_classmethod_ get_local_to_tracking_transform( _trace_result_)→TransformParameters:

**trace\_result** ( _ARTraceResult_)

Returns:

The transform of the trace result in tracking space (after it is modified by the c AlignmentTransform). see SetAlignmentTransform()

Return type:

Transform


---

_classmethod_ get_local_to_world_transform( _trace_result_)→TransformParameters:

**trace\_result** ( _ARTraceResult_)

Returns:

Get the transform of the trace result in Unreal World Space.

Return type:

Transform


---

_classmethod_ get_local_transform( _trace_result_)→TransformParameters:

**trace\_result** ( _ARTraceResult_)

Returns:

Get the transform of the trace result in the AR system’s local space.

Return type:

Transform


---

_classmethod_ get_trace_channel( _trace_result_)→ARLineTraceChannelsParameters:

**trace\_result** ( _ARTraceResult_)

Returns:

Get the type of the tracked object (if any) that effected this trace result.

Return type:

ARLineTraceChannels


---

_classmethod_ get_tracked_geometry( _trace_result_)→ARTrackedGeometryParameters:

**trace\_result** ( _ARTraceResult_)

Returns:

Get the real-world object (as observed by the Augmented Reality system) that was intersected by the line trace.

Return type:

ARTrackedGeometry

### Table of Contents

- `unreal.ARTraceResultLibrary`
  - `ARTraceResultLibrary`
    - `ARTraceResultLibrary.get_distance_from_camera()`
    - `ARTraceResultLibrary.get_local_to_tracking_transform()`
    - `ARTraceResultLibrary.get_local_to_world_transform()`
    - `ARTraceResultLibrary.get_local_transform()`
    - `ARTraceResultLibrary.get_trace_channel()`
    - `ARTraceResultLibrary.get_tracked_geometry()`