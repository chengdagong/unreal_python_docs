# unreal.MoviePipelineExecutorJob

```python
class unreal.MoviePipelineExecutorJob(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


A particular job within the Queue

**C++ Source:**

- **Plugin**: MovieRenderPipeline

- **Module**: MovieRenderPipelineCore

- **File**: MoviePipelineQueue.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `author` (str): [Read-Write] (Optional) If left blank, will default to system username. Can be shown in burn in as a first point of contact about the content.

- `comment` (str): [Read-Write] (Optional) If specified, will be shown in the burn in to allow users to keep track of notes about a render.

- `console_variable_overrides` (Array[MoviePipelineConsoleVariableEntry]): [Read-Write] (Optional) Console variable overrides which are applied after cvars set via nodes. Only applies to graph-based configs.

- `graph_variable_assignments` (Array[MovieJobVariableAssignmentContainer]): [Read-Write] Overrides on the variables in the graph (and subgraphs) associated with this job.

- `job_name` (str): [Read-Write] (Optional) Name of the job. Shown on the default burn-in.

- `map` (SoftObjectPath): [Read-Write] Which map should this job render on

- `sequence` (SoftObjectPath): [Read-Write] Which sequence should this job render?

- `shot_info` (Array[MoviePipelineExecutorShot]): [Read-Write] (Optional) Shot specific information. If a shot is missing from this list it will assume to be enabled and will be rendered.

- `user_data` (str): [Read-Write] Arbitrary data that can be associated with the job. Not used by default implementations, nor read.
This can be used to attach third party metadata such as job ids from remote farms.
Not shown in the user interface.



---

_property_ `author`: str

[Read-Write] (Optional) If left blank, will default to system username. Can be shown in burn in as a first point of contact about the content.

**Type:**

( str)


---

_property_ `comment`: str

[Read-Write] (Optional) If specified, will be shown in the burn in to allow users to keep track of notes about a render.

**Type:**

( str)


---

_property_ `console_variable_overrides`: None

[Read-Write] (Optional) Console variable overrides which are applied after cvars set via nodes. Only applies to graph-based configs.

**Type:**

( Array\ [MoviePipelineConsoleVariableEntry])


---

**get_configuration**() → `MoviePipelinePrimaryConfig`

Gets the configuration for the job. This configuration is either standalone (not associated with any preset), or
contains a copy of the preset origin plus any modifications made on top of it. If the preset that this
configuration was originally based on no longer exists, this configuration will still be valid.
see: GetPresetOrigin()

Return type:

MoviePipelinePrimaryConfig


---

**get_graph_preset**() → `MovieGraphConfig`

Gets the graph-style preset that this job is using. If the job is not using a graph-style preset, returns nullptr.
see: GetPresetOrigin()

Return type:

MovieGraphConfig


---

**get_or_create_variable_overrides**( _graph_) → `MovieJobVariableAssignmentContainer`

This method will return you the object which contains variable overrides for the Primary Graph assigned to this job. You need to provide
a pointer to the exact graph you want (as the Primary Graph may contain sub-graphs, and those sub-graphs can have their own variables),
though this will be the same as GetGraphPreset() if you’re not using any sub-graphs, or your variables only exist on the Primary graph.

If you want to override a variable on the primary graph but only for a specific shot, you should get the UMoviePipelineExecutorShot and
call that classes version of this function, except passing True for the extra boolean. See comment on that function for more details.

Parameters:

**graph** ( _MovieGraphConfig_) – The graph asset to get the Job Override values for. Should be the graph the variables you want to edit are defined on, which can either be the primary graph (GetGraphPreset()) or one of the sub-graphs it points to (as sub-graphs can contain their own variables which are all shown at the top level job in the Editor UI).

Returns:

A container object which holds a copy of the variables for the specified Graph Asset that can be used to override their values on jobs without actually editing the default asset.

Return type:

MovieJobVariableAssignmentContainer


---

**get_preset_origin**() → `MoviePipelinePrimaryConfig`

Gets the preset for this job, but only if the preset has not been modified. If it has been modified, or the preset
no longer exists, returns nullptr.
see: GetConfiguration()

Return type:

MoviePipelinePrimaryConfig


---

**get_status_message**() → `str`

Get the current status message for this job. May be an empty string.

For C++ implementations override virtual FString GetStatusMessage\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def get\_status\_message(self): return ?

Return type:

str


---

**get_status_progress**() → `float`

Get the current progress as last set by SetStatusProgress. 0 by default.

For C++ implementations override virtual float GetStatusProgress\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def get\_status\_progress(self): return ?

Return type:

float


---

**is_consumed**() → `bool`

Gets whether or not the job has been marked as being consumed. A consumed job is not editable
in the UI and should not be submitted for rendering as it is either already finished or
already in progress.

For C++ implementations override virtual bool IsConsumed\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def is\_consumed(self): return ?

Return type:

bool


---

**is_enabled**() → `bool`

Gets whether or not the job has been marked as being enabled.

For C++ implementations override virtual bool IsEnabled\_Implementation() const override
For Python/BP implementations override
unreal.ufunction(override=True): def is\_enabled(self): return ?

Return type:

bool


---

**is_using_graph_configuration**() → `bool`

Returns true if this job is using graph-style configuration, else false.

Return type:

bool


---

_property_ `job_name`: str

[Read-Write] (Optional) Name of the job. Shown on the default burn-in.

**Type:**

( str)


---

_property_ `map`: SoftObjectPath

[Read-Write] Which map should this job render on

**Type:**

( SoftObjectPath)


---

**on_duplicated**() → `None`

Should be called to clear status and user data after duplication so that jobs stay
unique and don’t pick up ids or other unwanted behavior from the pareant job.

For C++ implementations override virtual bool OnDuplicated\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def on\_duplicated(self):


---

_property_ `sequence`: SoftObjectPath

[Read-Write] Which sequence should this job render?

**Type:**

( SoftObjectPath)


---

**set_configuration**( _preset_) → `None`

Set Configuration

Parameters:

**preset** ( _MoviePipelinePrimaryConfig_)


---

**set_consumed**( _consumed_) → `None`

Set the job to be consumed. A consumed job is disabled in the UI and should not be
submitted for rendering again. This allows jobs to be added to a queue, the queue
submitted to a remote farm (consume the jobs) and then more jobs to be added and
the second submission to the farm won’t re-submit the already in-progress jobs.

Jobs can be unconsumed when the render finishes to re-enable editing.

For C++ implementations override virtual void SetConsumed\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def set\_consumed(self, isConsumed):

Parameters:

**consumed** ( _bool_) – True if the job should be consumed and disabled for editing in the UI.


---

**set_graph_preset**( _graph_preset_, _update_variable_assignments=True_) → `None`

Sets the graph-style preset that this job will use. Note that this will cause the graph to switch over to using
graph-style configuration if it is not already using it.

Parameters:

- **graph\_preset** ( _MovieGraphConfig_) – The graph preset to assign to the job.

- **update\_variable\_assignments** ( _bool_) – Set to false if variable assignments should NOT be automatically updated to reflect the graph preset being used. This is normally not what you want and should be used with caution.



---

**set_is_enabled**( _enabled_) → `None`

Set the job to be enabled/disabled. This is exposed to the user in the Queue UI
so they can disable a job after loading a queue to skip trying to run it.

For C++ implementations override virtual void SetIsEnabled\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def set\_is\_enabled(self, isEnabled):

Parameters:

**enabled** ( _bool_) – True if the job should be enabled and rendered.


---

**set_preset_origin**( _preset_) → `None`

Set Preset Origin

Parameters:

**preset** ( _MoviePipelinePrimaryConfig_)


---

**set_status_message**( _status_) → `None`

Set the status of this job to the given value. This will be shown on the UI if progress
is set to a value less than zero. If progress is > 0 then the progress bar will be shown
on the UI instead. Progress and Status Message are cosmetic and dependent on the
executor to update. Similar to the UMoviePipelineExecutor::SetStatusMessage function,
but at a per-job level basis instead.

For C++ implementations override virtual void SetStatusMessage\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def set\_status\_message(self, inStatus):

Parameters:

**status** ( _str_) – The status message you wish the executor to have.


---

**set_status_progress**( _progress_) → `None`

Set the progress of this job to the given value. If a positive value is provided
the UI will show the progress bar, while a negative value will make the UI show the
status message instead. Progress and Status Message are cosmetic and dependent on the
executor to update. Similar to the UMoviePipelineExecutor::SetStatusProgress function,
but at a per-job level basis instead.

For C++ implementations override virtual void SetStatusProgress\_Implementation() override
For Python/BP implementations override
unreal.ufunction(override=True): def set\_status\_progress(self, inProgress):

Parameters:

**progress** ( _float_) – The progress (0-1 range) the executor should have.


---

_property_ `shot_info`: None

[Read-Write] (Optional) Shot specific information. If a shot is missing from this list it will assume to be enabled and will be rendered.

**Type:**

( Array\ [MoviePipelineExecutorShot])


---

_property_ `user_data`: str

[Read-Write] Arbitrary data that can be associated with the job. Not used by default implementations, nor read.
This can be used to attach third party metadata such as job ids from remote farms.
Not shown in the user interface.

**Type:**

( str)

### Table of Contents

- `unreal.MoviePipelineExecutorJob`
  - `MoviePipelineExecutorJob`
    - `MoviePipelineExecutorJob.author`
    - `MoviePipelineExecutorJob.comment`
    - `MoviePipelineExecutorJob.console_variable_overrides`
    - `MoviePipelineExecutorJob.get_configuration()`
    - `MoviePipelineExecutorJob.get_graph_preset()`
    - `MoviePipelineExecutorJob.get_or_create_variable_overrides()`
    - `MoviePipelineExecutorJob.get_preset_origin()`
    - `MoviePipelineExecutorJob.get_status_message()`
    - `MoviePipelineExecutorJob.get_status_progress()`
    - `MoviePipelineExecutorJob.is_consumed()`
    - `MoviePipelineExecutorJob.is_enabled()`
    - `MoviePipelineExecutorJob.is_using_graph_configuration()`
    - `MoviePipelineExecutorJob.job_name`
    - `MoviePipelineExecutorJob.map`
    - `MoviePipelineExecutorJob.on_duplicated()`
    - `MoviePipelineExecutorJob.sequence`
    - `MoviePipelineExecutorJob.set_configuration()`
    - `MoviePipelineExecutorJob.set_consumed()`
    - `MoviePipelineExecutorJob.set_graph_preset()`
    - `MoviePipelineExecutorJob.set_is_enabled()`
    - `MoviePipelineExecutorJob.set_preset_origin()`
    - `MoviePipelineExecutorJob.set_status_message()`
    - `MoviePipelineExecutorJob.set_status_progress()`
    - `MoviePipelineExecutorJob.shot_info`
    - `MoviePipelineExecutorJob.user_data`