# unreal.MetaHumanIdentity

```python
class unreal.MetaHumanIdentity(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


MetaHuman Identity Asset

> Provides the tools to auto-generate a fully rigged Skeletal Mesh
> of a human face from Capture Data (Mesh or Footage) by tracking
> the facial features, fitting a Template Mesh having MetaHuman
> topology to the tracked curves, and sending the resulting mesh
> to MetaHuman Service, which returns an auto-rigged SkeletalMesh
> resembling the person from the Capture Data.
>
> The obtained Skeletal Mesh can be used by MetaHuman Performance
> asset to generate an Animation Sequence from video footage.
>
> MetaHuman Identity Asset Toolkit can also create a full MetaHuman in MetaHuman
> Creator, downloadable through Quixel Bridge.

**C++ Source:**

- **Plugin**: MetaHuman

- **Module**: MetaHumanIdentity

- **File**: MetaHumanIdentity.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `on_auto_rig_service_finished_dynamic_delegate` (OnAutoRigServiceFinishedDynamicDelegate): [Read-Write] Dynamic delegate called when the pipeline finishes running

- `parts` (Array[MetaHumanIdentityPart]): [Read-Write] The list of Parts the make this Identity. See UMetaHumanIdentityPart

- `thumbnail_info` (ThumbnailInfo): [Read-Only] Information for thumbnail rendering

- `viewport_settings` (MetaHumanIdentityViewportSettings): [Read-Write] Stores the viewport settings for this MetaHuman Identity



---

**can_add_part_of_class**( _part_class_) → `bool`

Returns true if the given Part class can be added to the MetaHuman Identity being edited

Parameters:

**part\_class** ( _type_ _(_ _Class_ _)_)

Return type:

bool


---

**can_add_pose_of_class**( _pose_class_, _pose_type_) → `bool`

Returns true if the given Pose class can be added to the MetaHuman Identity being edited

Parameters:

- **pose\_class** ( _type_ _(_ _Class_ _)_)

- **pose\_type** ( _IdentityPoseType_)


Return type:

bool


---

**create_dna_for_identity**( _log_only_) → `None`

Create DNAFor Identity

Parameters:

**log\_only** ( _bool_)


---

**diagnostics_indicates_processing_issue**() → `TextorNone`

Diagnostics Indicates Processing Issue

Returns:

out\_diagnostics\_warning\_message (Text):

Return type:

Text or None


---

**export_dna_data_to_files**( _dna_path_with_name_, _brows_path_with_name_) → `bool`

Export DNA and brows data to files at selected location

Parameters:

- **dna\_path\_with\_name** ( _str_)

- **brows\_path\_with\_name** ( _str_)


Return type:

bool


---

**find_part_of_class**( _part_class_) → `MetaHumanIdentityPart`

Looks for a Part of the given class in the array of parts. Returns nullptr if no Part was found

Parameters:

**part\_class** ( _type_ _(_ _Class_ _)_)

Return type:

MetaHumanIdentityPart


---

**get_or_create_part_of_class**( _part_class_) → `MetaHumanIdentityPart`

Looks for a Part of the given class in the array of parts. Creates and return a new one if not found

Parameters:

**part\_class** ( _type_ _(_ _Class_ _)_)

Return type:

MetaHumanIdentityPart


---

_classmethod_ handle_error( _error_code_, _log_only=False_)→bool

Deals with error produced by the MetaHuman Identity process - logs message and optionally show user dialog

Parameters:

- **error\_code** ( _IdentityErrorCode_)

- **log\_only** ( _bool_)


Return type:

bool


---

**import_dna_file**( _dna_file_path_, _dna_data_layer_, _brows_file_path_) → `IdentityErrorCode`

Initialize the MetaHuman Identity from a DNA file. The MetaHuman Identity must already have a face for this to succeeded

Parameters:

- **dna\_file\_path** ( _str_)

- **dna\_data\_layer** ( _DNADataLayer_)

- **brows\_file\_path** ( _str_)


Return type:

IdentityErrorCode


---

**is_auto_rigging_in_progress**() → `bool`

Is Auto Rigging in Progress

Return type:

bool


---

**is_frame_tracking_pipeline_processing**() → `bool`

Is Frame Tracking Pipeline Processing

Return type:

bool


---

**is_logged_in_to_service**() → `bool`

This function checks if there’s a session stored. There is NO request sent to check if the token is actually valid

Return type:

bool


---

**log_in_to_auto_rig_service**() → `None`

Log in to Auto Rig Service

_property_ on\_auto\_rig\_service\_finished\_dynamic\_delegate _:OnAutoRigServiceFinishedDynamicDelegate_

[Read-Write] Dynamic delegate called when the pipeline finishes running

**Type:**

(OnAutoRigServiceFinishedDynamicDelegate)


---

_property_ `parts`: None

[Read-Only] The list of Parts the make this Identity. See UMetaHumanIdentityPart

**Type:**

( Array\ [MetaHumanIdentityPart])


---

**set_blocking_processing**( _blocking_processing_) → `None`

Set Blocking Processing

Parameters:

**blocking\_processing** ( _bool_)


---

**start_frame_tracking_pipeline**( _image_data_, _width_, _height_, _depth_frame_path_, _pose_, _promoted_frame_, _show_progress_) → `None`

Start Frame Tracking Pipeline

Parameters:

- **image\_data** ( _Array_ _\_ [_Color_ _]_)

- **width** ( _int32_)

- **height** ( _int32_)

- **depth\_frame\_path** ( _str_)

- **pose** ( _MetaHumanIdentityPose_)

- **promoted\_frame** ( _MetaHumanIdentityPromotedFrame_)

- **show\_progress** ( _bool_)



---

_property_ `viewport_settings`: MetaHumanIdentityViewportSettings

[Read-Write] Stores the viewport settings for this MetaHuman Identity

**Type:**

( MetaHumanIdentityViewportSettings)

### Table of Contents

- `unreal.MetaHumanIdentity`
  - `MetaHumanIdentity`
    - `MetaHumanIdentity.can_add_part_of_class()`
    - `MetaHumanIdentity.can_add_pose_of_class()`
    - `MetaHumanIdentity.create_dna_for_identity()`
    - `MetaHumanIdentity.diagnostics_indicates_processing_issue()`
    - `MetaHumanIdentity.export_dna_data_to_files()`
    - `MetaHumanIdentity.find_part_of_class()`
    - `MetaHumanIdentity.get_or_create_part_of_class()`
    - `MetaHumanIdentity.handle_error()`
    - `MetaHumanIdentity.import_dna_file()`
    - `MetaHumanIdentity.is_auto_rigging_in_progress()`
    - `MetaHumanIdentity.is_frame_tracking_pipeline_processing()`
    - `MetaHumanIdentity.is_logged_in_to_service()`
    - `MetaHumanIdentity.log_in_to_auto_rig_service()`
    - `MetaHumanIdentity.on_auto_rig_service_finished_dynamic_delegate`
    - `MetaHumanIdentity.parts`
    - `MetaHumanIdentity.set_blocking_processing()`
    - `MetaHumanIdentity.start_frame_tracking_pipeline()`
    - `MetaHumanIdentity.viewport_settings`