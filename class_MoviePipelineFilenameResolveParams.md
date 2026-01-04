# unreal.MoviePipelineFilenameResolveParams

```python
class unreal.MoviePipelineFilenameResolveParams(frame_number:int=0, frame_number_shot:int=0, frame_number_rel:int=0, frame_number_shot_rel:int=0, camera_name_override:str='', shot_name_override:str='', zero_pad_frame_number_count:int=0, force_relative_frame_numbers:bool=False, file_name_override:str='', file_name_format_overrides:None={}, file_metadata:None={}, initialization_time:DateTime=\[\], initialization_time_offset:Timespan=Ellipsis, initialization_version:int=0, job:MoviePipelineExecutorJob=Ellipsis, shot_override:MoviePipelineExecutorShot=Ellipsis, additional_frame_number_offset:int=0)
```


**Bases:** ``StructBase``


Movie Pipeline Filename Resolve Params

**C++ Source:**

- **Plugin**: MovieRenderPipeline

- **Module**: MovieRenderPipelineCore

- **File**: MovieRenderPipelineDataTypes.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `additional_frame_number_offset` (int32): [Read-Write] Additional offset added onto the offset provided by the Output Settings in the Job. Required for some internal things (FCPXML).

- `camera_name_override` (str): [Read-Write] Name used by the {camera\_name} format tag. If specified, this will override the camera name (which is normally pulled from the ShotOverride object).

- `file_metadata` (Map[str, str]): [Read-Write] A key/value pair that maps metadata names to their values. Output is only supported in exr formats at the moment.

- `file_name_format_overrides` (Map[str, str]): [Read-Write] A map between “{format}” tokens and their values. These are applied after the auto-generated ones from the system,
which allows the caller to override things like {.ext} depending or {render\_pass} which have dummy names by default.

- `file_name_override` (str): [Read-Write] Optional. If specified this is the filename that will be used instead of automatically building it from the Job’s Output Setting.

- `force_relative_frame_numbers` (bool): [Read-Write] If true, force format strings (like {frame\_number}) to resolve using the relative version. Used when slow-mo is detected as frame numbers would overlap.

- `frame_number` (int32): [Read-Write] Frame Number for the Root (matching what you see in the Sequencer timeline. ie: If the Sequence PlaybackRange starts on 50, this value would be 50 on the first frame.

- `frame_number_rel` (int32): [Read-Write] Frame Number for the Root (relative to 0, not what you would see in the Sequencer timeline. ie: If sequence PlaybackRange starts on 50, this value would be 0 on the first frame.

- `frame_number_shot` (int32): [Read-Write] Frame Number for the Shot (matching what you would see in Sequencer at the sub-sequence level.

- `frame_number_shot_rel` (int32): [Read-Write] Frame Number for the Shot (relative to 0, not what you would see in the Sequencer timeline.

- `initialization_time` (DateTime): [Read-Write] The initialization time for this job. Used to resolve time-based format arguments.

- `initialization_time_offset` (Timespan): [Read-Write] What offset should be applied to InitializationTime when generating {time} related filename tokens? Likely your offset from UTC if you want local time.

- `initialization_version` (int32): [Read-Write] The version for this job. Used to resolve version format arguments.

- `job` (MoviePipelineExecutorJob): [Read-Write] Required. This is the job all of the settings should be pulled from.

- `shot_name_override` (str): [Read-Write] Name used by the {shot\_name} format tag. If specified, this will override the shot name (which is normally pulled from the ShotOverride object)

- `shot_override` (MoviePipelineExecutorShot): [Read-Write] Optional. If specified, settings will be pulled from this shot (if overriden by the shot). If null, always use the root configuration in the job.

- `zero_pad_frame_number_count` (int32): [Read-Write] When converitng frame numbers to strings, how many digits should we pad them up to? ie: 5 => 0005 with a count of 4.



---

_property_ `additional_frame_number_offset`: int

[Read-Write] Additional offset added onto the offset provided by the Output Settings in the Job. Required for some internal things (FCPXML).

**Type:**

(int32)


---

_property_ `camera_name_override`: str

[Read-Write] Name used by the {camera\_name} format tag. If specified, this will override the camera name (which is normally pulled from the ShotOverride object).

**Type:**

( str)


---

_property_ `file_metadata`: None

[Read-Write] A key/value pair that maps metadata names to their values. Output is only supported in exr formats at the moment.

**Type:**

( Map\ [str, str])


---

_property_ `file_name_format_overrides`: None

[Read-Write] A map between “{format}” tokens and their values. These are applied after the auto-generated ones from the system,
which allows the caller to override things like {.ext} depending or {render\_pass} which have dummy names by default.

**Type:**

( Map\ [str, str])


---

_property_ `file_name_override`: str

[Read-Write] Optional. If specified this is the filename that will be used instead of automatically building it from the Job’s Output Setting.

**Type:**

( str)


---

_property_ `force_relative_frame_numbers`: bool

[Read-Write] If true, force format strings (like {frame\_number}) to resolve using the relative version. Used when slow-mo is detected as frame numbers would overlap.

**Type:**

( bool)


---

_property_ `frame_number`: int

If the Sequence PlaybackRange starts on 50, this value would be 50 on the first frame.

**Type:**

(int32)

**Type:**

[Read-Write] Frame Number for the Root (matching what you see in the Sequencer timeline. ie


---

_property_ `frame_number_rel`: int

If sequence PlaybackRange starts on 50, this value would be 0 on the first frame.

**Type:**

(int32)

**Type:**

[Read-Write] Frame Number for the Root (relative to 0, not what you would see in the Sequencer timeline. ie


---

_property_ `frame_number_shot`: int

[Read-Write] Frame Number for the Shot (matching what you would see in Sequencer at the sub-sequence level.

**Type:**

(int32)


---

_property_ `frame_number_shot_rel`: int

[Read-Write] Frame Number for the Shot (relative to 0, not what you would see in the Sequencer timeline.

**Type:**

(int32)


---

_property_ `initialization_time`: DateTime

[Read-Write] The initialization time for this job. Used to resolve time-based format arguments.

**Type:**

( DateTime)


---

_property_ `initialization_time_offset`: Timespan

[Read-Write] What offset should be applied to InitializationTime when generating {time} related filename tokens? Likely your offset from UTC if you want local time.

**Type:**

( Timespan)


---

_property_ `initialization_version`: int

[Read-Write] The version for this job. Used to resolve version format arguments.

**Type:**

(int32)


---

_property_ `job`: MoviePipelineExecutorJob

[Read-Write] Required. This is the job all of the settings should be pulled from.

**Type:**

( MoviePipelineExecutorJob)


---

_property_ `shot_name_override`: str

[Read-Write] Name used by the {shot\_name} format tag. If specified, this will override the shot name (which is normally pulled from the ShotOverride object)

**Type:**

( str)


---

_property_ `shot_override`: MoviePipelineExecutorShot

[Read-Write] Optional. If specified, settings will be pulled from this shot (if overriden by the shot). If null, always use the root configuration in the job.

**Type:**

( MoviePipelineExecutorShot)


---

_property_ `zero_pad_frame_number_count`: int

5 => 0005 with a count of 4.

**Type:**

(int32)

**Type:**

[Read-Write] When converitng frame numbers to strings, how many digits should we pad them up to? ie

### Table of Contents

- `unreal.MoviePipelineFilenameResolveParams`
  - `MoviePipelineFilenameResolveParams`
    - `MoviePipelineFilenameResolveParams.additional_frame_number_offset`
    - `MoviePipelineFilenameResolveParams.camera_name_override`
    - `MoviePipelineFilenameResolveParams.file_metadata`
    - `MoviePipelineFilenameResolveParams.file_name_format_overrides`
    - `MoviePipelineFilenameResolveParams.file_name_override`
    - `MoviePipelineFilenameResolveParams.force_relative_frame_numbers`
    - `MoviePipelineFilenameResolveParams.frame_number`
    - `MoviePipelineFilenameResolveParams.frame_number_rel`
    - `MoviePipelineFilenameResolveParams.frame_number_shot`
    - `MoviePipelineFilenameResolveParams.frame_number_shot_rel`
    - `MoviePipelineFilenameResolveParams.initialization_time`
    - `MoviePipelineFilenameResolveParams.initialization_time_offset`
    - `MoviePipelineFilenameResolveParams.initialization_version`
    - `MoviePipelineFilenameResolveParams.job`
    - `MoviePipelineFilenameResolveParams.shot_name_override`
    - `MoviePipelineFilenameResolveParams.shot_override`
    - `MoviePipelineFilenameResolveParams.zero_pad_frame_number_count`