# unreal.MovieSceneSectionExtensions

```python
class unreal.MovieSceneSectionExtensions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Function library containing methods that should be hoisted onto UMovieSceneSections for scripting

**C++ Source:**

- **Plugin**: SequencerScripting

- **Module**: SequencerScripting

- **File**: MovieSceneSectionExtensions.h



---

_classmethod_ get_all_channels( _section_)→Array\ [MovieSceneScriptingChannel]

Find all channels that belong to the specified UMovieSceneSection. Some sections have many channels (such as
Transforms containing 9 double channels to represent Translation/Rotation/Scale), and a section may have mixed
channel types.

Parameters:

**section** ( _MovieSceneSection_) – The section to use.

Returns:

An array containing any key channels that match the type specified

Return type:

Array\ [MovieSceneScriptingChannel]


---

_classmethod_ get_auto_size_end_frame( _section_)→int32

Get end frame of the AutoSize. Will throw an exception if section has no end frame, use GetAutoSizeHasEndFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

The end frame of the AutoSize data.

Return type:

int32


---

_classmethod_ get_auto_size_end_frame_seconds( _section_)→float

Get end time of the AutoSize seconds. Will throw an exception if section has no end frame, use GetAutoSizeHasEndFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

The end frame of the AutoSize data in seconds.

Return type:

float


---

_classmethod_ get_auto_size_has_end_frame( _section_)→bool

Checks to see if this section has an AutoSize implementation, and if so, if that implementation has a end frame.

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

Whether this section has a valid autosize range, and a valid end frame

Return type:

bool


---

_classmethod_ get_auto_size_has_start_frame( _section_)→bool

Checks to see if this section has an AutoSize implementation, and if so, if that implementation has a start frame.

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

Whether this section has a valid autosize range, and a valid start frame

Return type:

bool


---

_classmethod_ get_auto_size_start_frame( _section_)→int32

Get start frame of the AutoSize. Will throw an exception if section has no start frame, use GetAutoSizeHasStartFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

The start frame of the AutoSize data.

Return type:

int32


---

_classmethod_ get_auto_size_start_frame_seconds( _section_)→float

Get start time of the AutoSize in seconds. Will throw an exception if section has no start frame, use GetAutoSizeHasStartFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

The start frame of the AutoSize data in seconds.

Return type:

float


---

_classmethod_ get_channel( _section_, _channel_name_)→MovieSceneScriptingChannel

Get channel from specified section and channel name

Parameters:

- **section** ( _MovieSceneSection_) – The section to use.

- **channel\_name** ( _Name_) – The name of the channel.


Returns:

The channel if it exists

Return type:

MovieSceneScriptingChannel


---

_classmethod_ get_channels_by_type( _section_, _channel_type_)→Array\ [MovieSceneScriptingChannel]

Find all channels that belong to the specified UMovieSceneSection that match the specific type. This will filter out any children who do not inherit
from the specified type for you.

Parameters:

- **section** ( _MovieSceneSection_) – The section to use.

- **channel\_type** ( _type_ _(_ _Class_ _)_) – The class type to look for.


Returns:

An array containing any key channels that match the type specified

Return type:

Array\ [MovieSceneScriptingChannel]


---

_classmethod_ get_end_frame( _section_)→int32

Get end frame. Will throw an exception if section has no end frame, use HasEndFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section within which to get the end frame

Returns:

End frame of this section

Return type:

int32


---

_classmethod_ get_end_frame_seconds( _section_)→float

Get end time in seconds. Will throw an exception if section has no end frame, use HasEndFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section within which to get the end time

Returns:

End time of this section

Return type:

float


---

_classmethod_ get_parent_sequence_frame( _section_, _frame_, _parent_sequence_)→int32

Get the frame in the space of its parent sequence

Parameters:

- **section** ( _MovieSceneSubSection_) – The section that the InFrame is local to

- **frame** ( _int32_) – The desired local frame

- **parent\_sequence** ( _MovieSceneSequence_) – The parent sequence to traverse from


Returns:

The frame at the parent sequence

Return type:

int32


---

_classmethod_ get_start_frame( _section_)→int32

Get start frame. Will throw an exception if section has no start frame, use HasStartFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section within which to get the start frame

Returns:

Start frame of this section

Return type:

int32


---

_classmethod_ get_start_frame_seconds( _section_)→float

Get start time in seconds. Will throw an exception if section has no start frame, use HasStartFrame to check first.

Parameters:

**section** ( _MovieSceneSection_) – The section within which to get the start time

Returns:

Start time of this section

Return type:

float


---

_classmethod_ has_end_frame( _section_)→bool

Has end frame

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

Whether this section has a valid end frame (else infinite)

Return type:

bool


---

_classmethod_ has_start_frame( _section_)→bool

Has start frame

Parameters:

**section** ( _MovieSceneSection_) – The section being queried

Returns:

Whether this section has a valid start frame (else infinite)

Return type:

bool


---

_classmethod_ set_end_frame( _section_, _end_frame_)→None

Set end frame

Parameters:

- **section** ( _MovieSceneSection_) – The section within which to set the end frame

- **end\_frame** ( _int32_) – The desired start frame for this section



---

_classmethod_ set_end_frame_bounded( _section_, _is_bounded_)→None

Set end frame bounded

Parameters:

- **section** ( _MovieSceneSection_) – The section to set whether the end frame is bounded or not

- **is\_bounded** ( _bool_)



---

_classmethod_ set_end_frame_seconds( _section_, _end_time_)→None

Set end time in seconds

Parameters:

- **section** ( _MovieSceneSection_) – The section within which to set the end time

- **end\_time** ( _float_) – The desired end time for this section



---

_classmethod_ set_range( _section_, _start_frame_, _end_frame_)→None

Set range

Parameters:

- **section** ( _MovieSceneSection_) – The section within which to set the range

- **start\_frame** ( _int32_) – The desired start frame for this section

- **end\_frame** ( _int32_) – The desired end frame for this section



---

_classmethod_ set_range_seconds( _section_, _start_time_, _end_time_)→None

Set range in seconds

Parameters:

- **section** ( _MovieSceneSection_) – The section within which to set the range

- **start\_time** ( _float_) – The desired start frame for this section

- **end\_time** ( _float_) – The desired end frame for this section



---

_classmethod_ set_start_frame( _section_, _start_frame_)→None

Set start frame

Parameters:

- **section** ( _MovieSceneSection_) – The section within which to set the start frame

- **start\_frame** ( _int32_) – The desired start frame for this section



---

_classmethod_ set_start_frame_bounded( _section_, _is_bounded_)→None

Set start frame bounded

Parameters:

- **section** ( _MovieSceneSection_) – The section to set whether the start frame is bounded or not

- **is\_bounded** ( _bool_)



---

_classmethod_ set_start_frame_seconds( _section_, _start_time_)→None

Set start time in seconds

Parameters:

- **section** ( _MovieSceneSection_) – The section within which to set the start time

- **start\_time** ( _float_) – The desired start time for this section


### Table of Contents

- `unreal.MovieSceneSectionExtensions`
  - `MovieSceneSectionExtensions`
    - `MovieSceneSectionExtensions.get_all_channels()`
    - `MovieSceneSectionExtensions.get_auto_size_end_frame()`
    - `MovieSceneSectionExtensions.get_auto_size_end_frame_seconds()`
    - `MovieSceneSectionExtensions.get_auto_size_has_end_frame()`
    - `MovieSceneSectionExtensions.get_auto_size_has_start_frame()`
    - `MovieSceneSectionExtensions.get_auto_size_start_frame()`
    - `MovieSceneSectionExtensions.get_auto_size_start_frame_seconds()`
    - `MovieSceneSectionExtensions.get_channel()`
    - `MovieSceneSectionExtensions.get_channels_by_type()`
    - `MovieSceneSectionExtensions.get_end_frame()`
    - `MovieSceneSectionExtensions.get_end_frame_seconds()`
    - `MovieSceneSectionExtensions.get_parent_sequence_frame()`
    - `MovieSceneSectionExtensions.get_start_frame()`
    - `MovieSceneSectionExtensions.get_start_frame_seconds()`
    - `MovieSceneSectionExtensions.has_end_frame()`
    - `MovieSceneSectionExtensions.has_start_frame()`
    - `MovieSceneSectionExtensions.set_end_frame()`
    - `MovieSceneSectionExtensions.set_end_frame_bounded()`
    - `MovieSceneSectionExtensions.set_end_frame_seconds()`
    - `MovieSceneSectionExtensions.set_range()`
    - `MovieSceneSectionExtensions.set_range_seconds()`
    - `MovieSceneSectionExtensions.set_start_frame()`
    - `MovieSceneSectionExtensions.set_start_frame_bounded()`
    - `MovieSceneSectionExtensions.set_start_frame_seconds()`