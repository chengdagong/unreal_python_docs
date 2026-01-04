# unreal.MoviePipelineQueueEngineSubsystem

```python
class unreal.MoviePipelineQueueEngineSubsystem(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``EngineSubsystem``


This subsystem is intended for use when rendering in a shipping game (but can also be used in PIE
during development/testing). See UMoviePipelineQueueSubsystem for the Editor-only queue which is
bound to the Movie Render Queue UI. To do simple renders at runtime, call AllocateJob(…)
with the Level Sequence you want to render, then call FindOrAddSettingByClass on the job to add
the settings (such as render pass, output type, and output directory) that you want for the job.
Finally, call RenderJob with the job you just configured. Register a delegate to OnRenderFinished
to be notified when the render finished. You can optionally call SetConfiguration(…) before
RenderJob to configure some advanced options.

**C++ Source:**

- **Plugin**: MovieRenderPipeline

- **Module**: MovieRenderPipelineCore

- **File**: MoviePipelineQueueEngineSubsystem.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `on_render_finished` (MoviePipelineWorkFinished): [Read-Write] Assign a function to this delegate to get notified when each individual job is finished.

THIS WILL ONLY BE CALLED IF USING THE RENDERJOB CONVENIENCE FUNCTION.

Because there can only be one job in the queue when using RenderJob, this will be called when
the render is complete, and the executor has been released. This allows you to queue up another
job immediately as a result of the OnRenderFinished callback.



---

**allocate_job**( _sequence_) → `MoviePipelineExecutorJob`

Convenience function for creating a UMoviePipelineExecutorJob out of the given Level Sequence asset. The
newly created job will be initialized to render on the current level, and will not have any default settings
added to it - instead you will need to call FindOrAddSettingByClass on the job’s configuration to add
settings such as render passes (UMoviePipelineDeferredPassBase), output types (UMoviePipelineImageSequenceOutput\_PNG),
and configure the output directory (UMoviePipelineOutputSetting). Once configuration is complete, register
a delegate to OnRenderFinished and then call RenderJob.

Calling this function will clear the internal queue, see RenderJob for more details.

Using this function while IsRendering() returns true will result in an exception being thrown and no attempt
being made to create the job.

Parameters:

**sequence** ( _LevelSequence_)

Return type:

MoviePipelineExecutorJob


---

**get_active_executor**() → `MoviePipelineExecutorBase`

Returns the active executor (if there is one). This can be used to subscribe to events on an already in-progress render. May be null.

Return type:

MoviePipelineExecutorBase


---

**get_queue**() → `MoviePipelineQueue`

Returns the queue of Movie Pipelines that need to be rendered.

Return type:

MoviePipelineQueue


---

**is_rendering**() → `bool`

Returns true if there is an active executor working on producing a movie. This could be actively rendering frames,
or working on post processing (finalizing file writes, etc.). Use GetActiveExecutor() and query it directly for
more information, progress updates, etc.

Return type:

bool


---

_property_ `on_render_finished`: MoviePipelineWorkFinished

[Read-Write] Assign a function to this delegate to get notified when each individual job is finished.

THIS WILL ONLY BE CALLED IF USING THE RENDERJOB CONVENIENCE FUNCTION.

Because there can only be one job in the queue when using RenderJob, this will be called when
the render is complete, and the executor has been released. This allows you to queue up another
job immediately as a result of the OnRenderFinished callback.

**Type:**

( MoviePipelineWorkFinished)


---

**render_job**( _job_) → `None`

Convenience function for rendering the specified job. Calling this will render the specified job (if it was
allocated using AllocateJob) and then it will reset the queue once finished. If you need to render multiple
jobs (in a queue) then you need to either implement the queue behavior yourself, or use
GetQueue()->AllocateJob(…) instead and use the non-convenience functions.

Calling this function will clear the queue (after completion).

Using this function while IsRendering() returns true will result in an exception being thrown and no attempt
being made to render the job.

Parameters:

**job** ( _MoviePipelineExecutorJob_)


---

**render_queue_with_executor**( _executor_type_) → `MoviePipelineExecutorBase`

Starts processing the current queue with the supplied executor class. This starts an async process which
may or may not run in a separate process (or on separate machines), determined by the executor implementation.
The executor should report progress for jobs depending on the implementation.

Parameters:

**executor\_type** ( _type_ _(_ _Class_ _)_) – A subclass of UMoviePipelineExecutorBase. An instance of this class is created and started.

Returns:

A pointer to the instance of the class created. This instance will be kept alive by the Queue Subsystem until it has finished (or been canceled). Register for progress reports and various callbacks on this instance.

Return type:

MoviePipelineExecutorBase


---

**render_queue_with_executor_instance**( _executor_) → `None`

Starts processing the current queue with the supplied executor. This starts an async process which
may or may not run in a separate process (or on separate machines), determined by the executor implementation.
The executor should report progress for jobs depending on the implementation.

Parameters:

**executor** ( _MoviePipelineExecutorBase_) – Instance of a subclass of UMoviePipelineExecutorBase.


---

**set_configuration**( _progress_widget_class=None_, _render_player_viewport=False_) → `None`

Sets some advanced configuration options that are used only occasionally to have better control over integrating it into
your game/application. This applies to both RenderQueueWithExecutor(Instance) and the simplified RenderJob API. This persists
until you call it again with different settings, and needs to be called before the Render\* functions.

Parameters:

- **progress\_widget\_class** ( _type_ _(_ _Class_ _)_)

- **render\_player\_viewport** ( _bool_) – If true, we will render the regular player viewport in addition to the off-screen MRQ render. This is significantly performance heavy (doubles render times) but can be useful in the event that you want to keep rendering the player viewport to better integrate the render into your own application.


### Table of Contents

- `unreal.MoviePipelineQueueEngineSubsystem`
  - `MoviePipelineQueueEngineSubsystem`
    - `MoviePipelineQueueEngineSubsystem.allocate_job()`
    - `MoviePipelineQueueEngineSubsystem.get_active_executor()`
    - `MoviePipelineQueueEngineSubsystem.get_queue()`
    - `MoviePipelineQueueEngineSubsystem.is_rendering()`
    - `MoviePipelineQueueEngineSubsystem.on_render_finished`
    - `MoviePipelineQueueEngineSubsystem.render_job()`
    - `MoviePipelineQueueEngineSubsystem.render_queue_with_executor()`
    - `MoviePipelineQueueEngineSubsystem.render_queue_with_executor_instance()`
    - `MoviePipelineQueueEngineSubsystem.set_configuration()`