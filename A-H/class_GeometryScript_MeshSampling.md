# unreal.GeometryScript_MeshSampling

```python
class unreal.GeometryScript_MeshSampling(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Geometry Script Library Mesh Sampling Functions

**C++ Source:**

- **Plugin**: GeometryScripting

- **Module**: GeometryScriptingCore

- **File**: MeshSamplingFunctions.h


_classmethod_ compute\_non\_uniform\_point\_sampling( _target\_mesh,options,non\_uniform\_options,debug=None)->(DynamicMesh,samples=Array[Transform],sample\_radii=Array[double],triangle\_i\_ds=GeometryScriptIndexList_)

Compute a set of sample points lying on the surface of TargetMesh based on the provided sampling Options and NonUniformOptions.
The sample points have radii in the range [Options.SamplingRadius, NonUniformOptions.MaxSamplingRadius], and
are non-overlapping, ie the distance between two points is always larger than the sum of their respective radii.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshPointSamplingOptions_)

- **non\_uniform\_options** ( _GeometryScriptNonUniformPointSamplingOptions_)

- **debug** ( _GeometryScriptDebug_)


Returns:

samples (Array[Transform]):

sample\_radii (Array[double]):

triangle\_i\_ds (GeometryScriptIndexList):

Return type:

tuple

_classmethod_ compute\_point\_sampling( _target\_mesh,options,debug=None)->(DynamicMesh,samples=Array[Transform],triangle\_i\_ds=GeometryScriptIndexList_)

Compute a set of sample points lying on the surface of TargetMesh based on the provided sampling Options.
Samples are approximately uniformly distributed, and non-overlapping relative to the provided Options.SamplingRadius,
ie the distance between any pair of samples if >= 2\*SamplingRadius.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshPointSamplingOptions_)

- **debug** ( _GeometryScriptDebug_)


Returns:

samples (Array[Transform]): output list of sample points. Transform Location is sample position, Rotation orients Z with the triangle normal

triangle\_i\_ds (GeometryScriptIndexList): TriangleID that contains each sample point. Length is the same as Samples array.

Return type:

tuple


---

_classmethod_ compute_render_capture_cameras_for_box( _box_, _options_, _debug=None_)→Array\ [GeometryScriptRenderCaptureCamera]

Compute a set of Render Capture Cameras to capture a scene within the given Box

Parameters:

- **box** ( _Box_) – Bounding Box containing the scene to be captured

- **options** ( _GeometryScriptRenderCaptureCamerasForBoxOptions_) – Defines the Camera viewing directions into the box and other Camera parameters

- **debug** ( _GeometryScriptDebug_)


Returns:

cameras (Array[GeometryScriptRenderCaptureCamera]): Output Cameras with view frustums that contain the Box while maintaining the desired FOV

Return type:

Array\ [GeometryScriptRenderCaptureCamera]


---

_classmethod_ compute_render_capture_point_sampling( _actors_, _cameras_, _debug=None_)→Array\ [Transform]

Compute oriented sample points on the visible surfaces of the given Actors
The Samples are computed using Render Capture from the given virtual Cameras

Parameters:

- **actors** ( _Array_ _\_ [_Actor_ _]_)

- **cameras** ( _Array_ _\_ [_GeometryScriptRenderCaptureCamera_ _]_)

- **debug** ( _GeometryScriptDebug_)


Returns:

samples (Array[Transform]):

Return type:

Array\ [Transform]

_classmethod_ compute\_uniform\_random\_point\_sampling( _target\_mesh,num\_samples,random\_seed=0,debug=None)->(DynamicMesh,samples=Array[Transform],triangle\_i\_ds=GeometryScriptIndexList_)

Compute a ‘uniform random’ (not ‘uniform spacing’) point sampling over the mesh surface

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **num\_samples** ( _int32_)

- **random\_seed** ( _int32_)

- **debug** ( _GeometryScriptDebug_)


Returns:

samples (Array[Transform]):

triangle\_i\_ds (GeometryScriptIndexList):

Return type:

tuple

_classmethod_ compute\_vertex\_weighted\_point\_sampling( _target\_mesh,options,non\_uniform\_options,vertex\_weights,debug=None)->(DynamicMesh,samples=Array[Transform],sample\_radii=Array[double],triangle\_i\_ds=GeometryScriptIndexList_)

Compute a set of sample points lying on the surface of TargetMesh based on the provided sampling Options and NonUniformOptions.
The sample points have radii in the range [Options.SamplingRadius, NonUniformOptions.MaxSamplingRadius], and
are non-overlapping, ie the distance between two points is always larger than the sum of their respective radii.

Parameters:

- **target\_mesh** ( _DynamicMesh_)

- **options** ( _GeometryScriptMeshPointSamplingOptions_)

- **non\_uniform\_options** ( _GeometryScriptNonUniformPointSamplingOptions_)

- **vertex\_weights** ( _GeometryScriptScalarList_) – defines a per-vertex weight in range [0,1], these are interpolated to create a scalar field over the mesh triangles which is used to weight the sampling radii

- **debug** ( _GeometryScriptDebug_)


Returns:

samples (Array[Transform]):

sample\_radii (Array[double]):

triangle\_i\_ds (GeometryScriptIndexList):

Return type:

tuple

### Table of Contents

- `unreal.GeometryScript_MeshSampling`
  - `GeometryScript_MeshSampling`
    - `GeometryScript_MeshSampling.compute_non_uniform_point_sampling()`
    - `GeometryScript_MeshSampling.compute_point_sampling()`
    - `GeometryScript_MeshSampling.compute_render_capture_cameras_for_box()`
    - `GeometryScript_MeshSampling.compute_render_capture_point_sampling()`
    - `GeometryScript_MeshSampling.compute_uniform_random_point_sampling()`
    - `GeometryScript_MeshSampling.compute_vertex_weighted_point_sampling()`