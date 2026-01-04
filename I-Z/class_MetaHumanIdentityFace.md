# unreal.MetaHumanIdentityFace

```python
class unreal.MetaHumanIdentityFace(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MetaHumanIdentityPart``


MetaHuman Identity Face

**C++ Source:**

- **Plugin**: MetaHuman

- **Module**: MetaHumanIdentity

- **File**: MetaHumanIdentityParts.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `default_solver` (MetaHumanFaceFittingSolver): [Read-Write] The default solver

- `dna_pivot` (Vector): [Read-Write] Holds the DNA Pivot as returned from the autorigging service
deprecated: The new autorigging service doesn’t provide DNA Pivot

- `dna_scale` (float): [Read-Write] Holds the DNA Scale as returned from the autorigging service
deprecated: The new autorigging service doesn’t provide DNATo Scale

- `dna_to_scan_transform` (Transform): [Read-Write] Holds the DNAToScan transform as returned from the autorigging service
deprecated: The new autorigging service doesn’t provide DNAToScan transform matrix

- `has_fitted_eyes` (bool): [Read-Only] True if data-driven eyes was used during mesh conformation

- `is_auto_rigged` (bool): [Read-Only] True if this face has autorigged DNA applied either through AutoRig Service or if it was imported manually through Import functionality

- `is_conformed` (bool): [Read-Only] True if this face was conformed at least once

- `maximum_scale_difference_from_average` (float): [Read-Write] The maximum percentage difference an autorigged face result is allowed to differ from an average MetaHuman. Above this value a diagnostic warning will be flagged.

- `minimum_depth_map_face_coverage` (float): [Read-Write] The minimum percentage of the face region which should have valid depth-map pixels. Below this value a diagnostic warning will be flagged.

- `minimum_depth_map_face_width` (float): [Read-Write] The minimum required width of the face region on the depth-map in pixels. Below this value a diagnostic warning will be flagged.

- `poses` (Array[MetaHumanIdentityPose]): [Read-Only] An array of poses that will be used to fit the conformal mesh to the input data. See UMetaHumanIdentityPose

- `rig_component` (SkeletalMeshComponent): [Read-Only] The result of the auto-rigging process. This is the conformal mesh with a proper rig able to control the face

- `should_update_rig_component` (bool): [Read-Only]

- `skip_diagnostics` (bool): [Read-Write] Flag indicating whether processing diagnostics should be calculated during identity creation

- `template_mesh_component` (MetaHumanTemplateMeshComponent): [Read-Only] The template mesh component for the face. Manages the meshes that represent each pose as well as eyes and teeth



---

**add_pose_of_type**( _pose_type_, _pose_) → `None`

Adds the given pose to this face. Does nothing if a pose of the same type already exists

Parameters:

- **pose\_type** ( _IdentityPoseType_)

- **pose** ( _MetaHumanIdentityPose_)



---

**conform**( _conform_type=ConformType.SOLVE_) → `IdentityErrorCode`

MetaHuman Identity solve

Parameters:

**conform\_type** ( _ConformType_)

Return type:

IdentityErrorCode


---

_property_ `dna_pivot`: Vector

[Read-Write] Holds the DNA Pivot as returned from the autorigging service
deprecated: The new autorigging service doesn’t provide DNA Pivot

**Type:**

( Vector)


---

_property_ `dna_scale`: float

[Read-Write] Holds the DNA Scale as returned from the autorigging service
deprecated: The new autorigging service doesn’t provide DNATo Scale

**Type:**

( float)


---

_property_ `dna_to_scan_transform`: Transform

[Read-Write] Holds the DNAToScan transform as returned from the autorigging service
deprecated: The new autorigging service doesn’t provide DNAToScan transform matrix

**Type:**

( Transform)


---

**export_template_mesh**( _path_, _asset_name_) → `None`

Export Template Mesh

Parameters:

- **path** ( _str_)

- **asset\_name** ( _str_)



---

**find_pose_by_type**( _pose_type_) → `MetaHumanIdentityPose`

Finds a Pose of given type. Returns nullptr if one is not found.

Parameters:

**pose\_type** ( _IdentityPoseType_)

Return type:

MetaHumanIdentityPose


---

**get_poses**() → `Array\ [MetaHumanIdentityPose]`

Get Poses

Return type:

Array\ [MetaHumanIdentityPose]


---

**has_dna_buffer**() → `bool`

Has DNABuffer

Return type:

bool


---

**has_predictive_solvers**() → `bool`

Has Predictive Solvers

Return type:

bool


---

**is_conformal_rig_valid**() → `bool`

Returns true if the conformal rig component is valid and points to a valid skeletal mesh

Return type:

bool


---

**remove_pose**( _pose_) → `bool`

Remove Pose

Parameters:

**pose** ( _MetaHumanIdentityPose_)

Return type:

bool


---

**run_predictive_solver_training**() → `bool`

Runs predictive solvers training externally (through python script or UE editor).
Returns true if the process was successful, false otherwise.

Return type:

bool

### Table of Contents

- `unreal.MetaHumanIdentityFace`
  - `MetaHumanIdentityFace`
    - `MetaHumanIdentityFace.add_pose_of_type()`
    - `MetaHumanIdentityFace.conform()`
    - `MetaHumanIdentityFace.dna_pivot`
    - `MetaHumanIdentityFace.dna_scale`
    - `MetaHumanIdentityFace.dna_to_scan_transform`
    - `MetaHumanIdentityFace.export_template_mesh()`
    - `MetaHumanIdentityFace.find_pose_by_type()`
    - `MetaHumanIdentityFace.get_poses()`
    - `MetaHumanIdentityFace.has_dna_buffer()`
    - `MetaHumanIdentityFace.has_predictive_solvers()`
    - `MetaHumanIdentityFace.is_conformal_rig_valid()`
    - `MetaHumanIdentityFace.remove_pose()`
    - `MetaHumanIdentityFace.run_predictive_solver_training()`