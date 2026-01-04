# unreal.AnimPoseExtensions

```python
class unreal.AnimPoseExtensions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Script exposed functionality for populating, retrieving data from and setting data on FAnimPose

**C++ Source:**

- **Module**: AnimationBlueprintLibrary

- **File**: AnimPose.h



---

_classmethod_ evaluate_animation_blueprint_with_input_pose( _input_pose_, _target_skeletal_mesh_, _animation_blueprint_)→AnimPose

Evaluates an Animation Blueprint instance, using the provided Anim Pose and its Input Pose value, generating a valid Anim Pose using the result. Warning this function may cause performance issues.

Parameters:

- **input\_pose** ( _AnimPose_) – Anim Pose used to populate the input pose node value inside of the Animation Blueprint

- **target\_skeletal\_mesh** ( _SkeletalMesh_) – USkeletalMesh object used as the target skeletal mesh, should have same USkeleton as InputPose and Animation Blueprint

- **animation\_blueprint** ( _AnimBlueprint_) – Animation Blueprint to generate an AnimInstance with, used to evaluate the output Anim Pose


Returns:

out\_pose (AnimPose): Anim pose to hold the data from evaluating the Animation Blueprint instance

Return type:

AnimPose


---

_classmethod_ get_anim_pose_at_frame( _animation_sequence_base_, _frame_index_, _evaluation_options_)→AnimPose

Evaluates an Animation Sequence Base to generate a valid Anim Pose instance

Parameters:

- **animation\_sequence\_base** ( _AnimSequenceBase_) – Animation sequence base to evaluate the pose from

- **frame\_index** ( _int32_) – Exact frame at which the pose should be evaluated

- **evaluation\_options** ( _AnimPoseEvaluationOptions_) – Options determining the way the pose should be evaluated


Returns:

pose (AnimPose): Anim Pose to hold the evaluated data

Return type:

AnimPose


---

_classmethod_ get_anim_pose_at_time( _animation_sequence_base_, _time_, _evaluation_options_)→AnimPose

Evaluates an Animation Sequence Base to generate a valid Anim Pose instance

Parameters:

- **animation\_sequence\_base** ( _AnimSequenceBase_) – Animation sequence base to evaluate the pose from

- **time** ( _double_) – Time at which the pose should be evaluated

- **evaluation\_options** ( _AnimPoseEvaluationOptions_) – Options determining the way the pose should be evaluated


Returns:

pose (AnimPose): Anim Pose to hold the evaluated data

Return type:

AnimPose


---

_classmethod_ get_bone_names( _pose_)→Array\ [Name]

Returns an array of bone names contained by the pose

Parameters:

**pose** ( _AnimPose_) – Anim Pose to retrieve the names from

Returns:

bones (Array[Name]): Array to be populated with the bone names

Return type:

Array\ [Name]


---

_classmethod_ get_bone_pose( _pose_, _bone_name_, _space=AnimPoseSpaces.LOCAL_)→Transform

Retrieves the transform for the provided bone name from a pose

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to retrieve the transform from

- **bone\_name** ( _Name_) – Name of the bone to retrieve

- **space** ( _AnimPoseSpaces_) – Space in which the transform should be retrieved


Returns:

Transform in requested space for bone if found, otherwise return identity transform

Return type:

Transform


---

_classmethod_ get_curve_names( _pose_)→Array\ [Name]

Returns an array of curve names contained by the pose

Parameters:

**pose** ( _AnimPose_) – Anim Pose to retrieve the names from

Returns:

curves (Array[Name]): Array to be populated with the curve names

Return type:

Array\ [Name]


---

_classmethod_ get_curve_weight( _pose_, _curve_name_)→float

Returns the weight of an evaluated curve - if found

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to retrieve the value from

- **curve\_name** ( _Name_) – Curve to retrieve the weight value for


Returns:

Curve weight value, if found - 0.f otherwise

Return type:

float


---

_classmethod_ get_ref_bone_pose( _pose_, _bone_name_, _space=AnimPoseSpaces.LOCAL_)→Transform

Retrieves the reference pose transform for the provided bone name

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to retrieve the transform from

- **bone\_name** ( _Name_) – Name of the bone to retrieve

- **space** ( _AnimPoseSpaces_) – Space in which the transform should be retrieved


Returns:

Transform in requested space for bone if found, otherwise return identity transform

Return type:

Transform


---

_classmethod_ get_ref_pose_relative_transform( _pose_, _from_bone_name_, _to_bone_name_, _space=AnimPoseSpaces.LOCAL_)→Transform

Retrieves the relative transform for the reference pose between the two provided bone names

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to retrieve the transform from

- **from\_bone\_name** ( _Name_) – Name of the bone to retrieve the transform relative from

- **to\_bone\_name** ( _Name_) – Name of the bone to retrieve the transform relative to

- **space** ( _AnimPoseSpaces_) – Space in which the transform should be retrieved


Returns:

Relative transform in requested space for bone if found, otherwise return identity transform

Return type:

Transform


---

_classmethod_ get_reference_pose( _skeleton_)→AnimPose

Populates an Anim Pose with the reference poses stored for the provided USkeleton

Parameters:

**skeleton** ( _Skeleton_) – USkeleton object to retrieve the reference pose from

Returns:

out\_pose (AnimPose): Anim pose to hold the reference pose

Return type:

AnimPose


---

_classmethod_ get_relative_to_ref_pose_transform( _pose_, _bone_name_, _space=AnimPoseSpaces.LOCAL_)→Transform

Retrieves the relative transform between reference and animated bone transform

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to retrieve the transform from

- **bone\_name** ( _Name_) – Name of the bone to retrieve the relative transform for

- **space** ( _AnimPoseSpaces_) – Space in which the transform should be retrieved


Returns:

Relative transform in requested space for bone if found, otherwise return identity transform

Return type:

Transform


---

_classmethod_ get_relative_transform( _pose_, _from_bone_name_, _to_bone_name_, _space=AnimPoseSpaces.LOCAL_)→Transform

Retrieves the relative transform between the two provided bone names

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to retrieve the transform from

- **from\_bone\_name** ( _Name_) – Name of the bone to retrieve the transform relative from

- **to\_bone\_name** ( _Name_) – Name of the bone to retrieve the transform relative to

- **space** ( _AnimPoseSpaces_) – Space in which the transform should be retrieved


Returns:

Relative transform in requested space for bone if found, otherwise return identity transform

Return type:

Transform


---

_classmethod_ get_socket_names( _pose_)→Array\ [Name]

Returns an array of socket names contained by the pose

Parameters:

**pose** ( _AnimPose_) – Anim Pose to retrieve the names from

Returns:

sockets (Array[Name]): Array to be populated with the socket names

Return type:

Array\ [Name]


---

_classmethod_ get_socket_pose( _pose_, _socket_name_, _space=AnimPoseSpaces.LOCAL_)→Transform

Retrieves the transform for the provided socket name from a pose

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to retrieve the transform from

- **socket\_name** ( _Name_) – Name of the socket to retrieve

- **space** ( _AnimPoseSpaces_) – Space in which the transform should be retrieved


Returns:

Transform in requested space for bone if found, otherwise return identity transform

Return type:

Transform


---

_classmethod_ is_valid( _pose_)→bool

Returns whether the Anim Pose contains valid data

Parameters:

**pose** ( _AnimPose_) – Anim Pose to validate

Returns:

Result of the validation

Return type:

bool


---

_classmethod_ set_bone_pose( _pose_, _transform_, _bone_name_, _space=AnimPoseSpaces.LOCAL_)→AnimPose

Sets the transform for the provided bone name for a pose

Parameters:

- **pose** ( _AnimPose_) – Anim Pose to set transform in

- **transform** ( _Transform_) – Transform to set the bone to

- **bone\_name** ( _Name_) – Name of the bone to set

- **space** ( _AnimPoseSpaces_) – Space in which the transform should be set


Returns:

pose (AnimPose): Anim Pose to set transform in

Return type:

AnimPose

### Table of Contents

- `unreal.AnimPoseExtensions`
  - `AnimPoseExtensions`
    - `AnimPoseExtensions.evaluate_animation_blueprint_with_input_pose()`
    - `AnimPoseExtensions.get_anim_pose_at_frame()`
    - `AnimPoseExtensions.get_anim_pose_at_time()`
    - `AnimPoseExtensions.get_bone_names()`
    - `AnimPoseExtensions.get_bone_pose()`
    - `AnimPoseExtensions.get_curve_names()`
    - `AnimPoseExtensions.get_curve_weight()`
    - `AnimPoseExtensions.get_ref_bone_pose()`
    - `AnimPoseExtensions.get_ref_pose_relative_transform()`
    - `AnimPoseExtensions.get_reference_pose()`
    - `AnimPoseExtensions.get_relative_to_ref_pose_transform()`
    - `AnimPoseExtensions.get_relative_transform()`
    - `AnimPoseExtensions.get_socket_names()`
    - `AnimPoseExtensions.get_socket_pose()`
    - `AnimPoseExtensions.is_valid()`
    - `AnimPoseExtensions.set_bone_pose()`