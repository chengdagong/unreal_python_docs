# unreal.MoviePipelineQueue

```python
class unreal.MoviePipelineQueue(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``Object``


A queue is a list of jobs that have been executed, are executing and are waiting to be executed. These can be saved
to specific assets to allow

**C++ Source:**

- **Plugin**: MovieRenderPipeline

- **Module**: MovieRenderPipelineCore

- **File**: MoviePipelineQueue.h



---

**allocate_new_job**( _job_type=None_) → `MoviePipelineExecutorJob`

Allocates a new Job in this Queue. The Queue owns the jobs for memory management purposes,
and this will handle that for you.

Parameters:

**job\_type** ( _type_ _(_ _Class_ _)_) – Specify the specific Job type that should be created. Custom Executors can use custom Job types to allow the user to provide more information.

Returns:

The created Executor job instance.

Return type:

MoviePipelineExecutorJob


---

**copy_from**( _queue_) → `MoviePipelineQueue`

Replace the contents of this queue with a copy of the contents from another queue.
Returns a pointer to this queue if the copy was successful, else nullptr.

Parameters:

**queue** ( _MoviePipelineQueue_)

Return type:

MoviePipelineQueue


---

**delete_all_jobs**() → `None`

Delete all jobs from the Queue.


---

**delete_job**( _job_) → `None`

Deletes the specified job from the Queue.

Parameters:

**job** ( _MoviePipelineExecutorJob_) – The job to look for and delete.


---

**duplicate_job**( _job_) → `MoviePipelineExecutorJob`

Duplicate the specific job and return the duplicate. Configurations are duplicated and not shared.

Parameters:

**job** ( _MoviePipelineExecutorJob_) – The job to look for to duplicate.

Returns:

The duplicated instance or nullptr if a duplicate could not be made.

Return type:

MoviePipelineExecutorJob


---

**get_jobs**() → `Array\ [MoviePipelineExecutorJob]`

Get all of the Jobs contained in this Queue.

Returns:

The jobs contained by this queue.

Return type:

Array\ [MoviePipelineExecutorJob]


---

**get_queue_origin**() → `MoviePipelineQueue`

Gets the queue that this queue was originally based on (if any). The origin will only be set on transient
queues; the origin will be nullptr for non-transient queues because the origin will be this object.

Return type:

MoviePipelineQueue


---

**is_dirty**() → `bool`

Gets the dirty state of this queue. Note that dirty state is only tracked when the editor is active.

Return type:

bool


---

**set_is_dirty**( _new_dirty_state_) → `None`

Sets the dirty state of this queue. Generally the queue will correctly track the dirty state; however, there are
situations where a queue may need its dirty state reset (eg, it may be appropriate to reset the dirty state after
a call to CopyFrom(), depending on the use case).

Parameters:

**new\_dirty\_state** ( _bool_)


---

**set_job_index**( _job_, _index_) → `None`

Set the index of the given job

Parameters:

- **job** ( _MoviePipelineExecutorJob_)

- **index** ( _int32_)



---

**set_queue_origin**( _config_) → `None`

Sets the queue that this queue originated from (if any). The origin should only be set for transient queues.

Parameters:

**config** ( _MoviePipelineQueue_)

### Table of Contents

- `unreal.MoviePipelineQueue`
  - `MoviePipelineQueue`
    - `MoviePipelineQueue.allocate_new_job()`
    - `MoviePipelineQueue.copy_from()`
    - `MoviePipelineQueue.delete_all_jobs()`
    - `MoviePipelineQueue.delete_job()`
    - `MoviePipelineQueue.duplicate_job()`
    - `MoviePipelineQueue.get_jobs()`
    - `MoviePipelineQueue.get_queue_origin()`
    - `MoviePipelineQueue.is_dirty()`
    - `MoviePipelineQueue.set_is_dirty()`
    - `MoviePipelineQueue.set_job_index()`
    - `MoviePipelineQueue.set_queue_origin()`