# unreal.MovieSceneSection

```python
class unreal.MovieSceneSection(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneDecorationContainerObject``


Base class for movie scene sections

**C++ Source:**

- **Module**: MovieScene

- **File**: MovieSceneSection.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `color_tint` (Color): [Read-Write] The color tint for this section

- `condition_container` (MovieSceneConditionContainer): [Read-Write] Optional dynamic condition for whether this section evaluates at runtime.

- `easing` (MovieSceneEasingSettings): [Read-Write]

- `eval_options` (MovieSceneSectionEvalOptions): [Read-Write]

- `is_active` (bool): [Read-Write] Toggle whether this section is active/inactive

- `is_locked` (bool): [Read-Write] Toggle whether this section is locked/unlocked

- `post_roll_frames` (FrameNumber): [Read-Write] The amount of time to continue ‘postrolling’ this section for after evaluation has ended.

- `pre_roll_frames` (FrameNumber): [Read-Write] The amount of time to prepare this section for evaluation before it actually starts.

- `section_range` (MovieSceneFrameRange): [Read-Write] The range in which this section is active

- `timecode_source` (MovieSceneTimecodeSource): [Read-Write] The timecode at which this movie scene section is based (ie. when it was recorded)



---

**get_all_channels**() → `Array\ [MovieSceneScriptingChannel]`

Find all channels that belong to the specified UMovieSceneSection. Some sections have many channels (such as
Transforms containing 9 double channels to represent Translation/Rotation/Scale), and a section may have mixed
channel types.

Returns:

An array containing any key channels that match the type specified

Return type:

Array\ [MovieSceneScriptingChannel]


---

**get_auto_size_end_frame**() → `int32`

Get end frame of the AutoSize. Will throw an exception if section has no end frame, use GetAutoSizeHasEndFrame to check first.

Returns:

The end frame of the AutoSize data.

Return type:

int32


---

**get_auto_size_end_frame_seconds**() → `float`

Get end time of the AutoSize seconds. Will throw an exception if section has no end frame, use GetAutoSizeHasEndFrame to check first.

Returns:

The end frame of the AutoSize data in seconds.

Return type:

float


---

**get_auto_size_has_end_frame**() → `bool`

Checks to see if this section has an AutoSize implementation, and if so, if that implementation has a end frame.

Returns:

Whether this section has a valid autosize range, and a valid end frame

Return type:

bool


---

**get_auto_size_has_start_frame**() → `bool`

Checks to see if this section has an AutoSize implementation, and if so, if that implementation has a start frame.

Returns:

Whether this section has a valid autosize range, and a valid start frame

Return type:

bool


---

**get_auto_size_start_frame**() → `int32`

Get start frame of the AutoSize. Will throw an exception if section has no start frame, use GetAutoSizeHasStartFrame to check first.

Returns:

The start frame of the AutoSize data.

Return type:

int32


---

**get_auto_size_start_frame_seconds**() → `float`

Get start time of the AutoSize in seconds. Will throw an exception if section has no start frame, use GetAutoSizeHasStartFrame to check first.

Returns:

The start frame of the AutoSize data in seconds.

Return type:

float


---

**get_blend_type**() → `OptionalMovieSceneBlendType`

Gets this section’s blend type

Return type:

OptionalMovieSceneBlendType


---

**get_channel**( _channel_name_) → `MovieSceneScriptingChannel`

Get channel from specified section and channel name

Parameters:

**channel\_name** ( _Name_) – The name of the channel.

Returns:

The channel if it exists

Return type:

MovieSceneScriptingChannel


---

**get_channels_by_type**( _channel_type_) → `Array\ [MovieSceneScriptingChannel]`

Find all channels that belong to the specified UMovieSceneSection that match the specific type. This will filter out any children who do not inherit
from the specified type for you.

Parameters:

**channel\_type** ( _type_ _(_ _Class_ _)_) – The class type to look for.

Returns:

An array containing any key channels that match the type specified

Return type:

Array\ [MovieSceneScriptingChannel]


---

**get_color_tint**() → `Color`

Get this section’s color tint.

Return type:

Color


---

**get_completion_mode**() → `MovieSceneCompletionMode`

Gets this section’s completion mode

Return type:

MovieSceneCompletionMode


---

**get_end_frame**() → `int32`

Get end frame. Will throw an exception if section has no end frame, use HasEndFrame to check first.

Returns:

End frame of this section

Return type:

int32


---

**get_end_frame_seconds**() → `float`

Get end time in seconds. Will throw an exception if section has no end frame, use HasEndFrame to check first.

Returns:

End time of this section

Return type:

float


---

**get_overlap_priority**() → `int32`

Gets this section’s priority over overlapping sections (higher wins)

Return type:

int32


---

**get_post_roll_frames**() → `int32`

Get Post Roll Frames

Return type:

int32


---

**get_pre_roll_frames**() → `int32`

Get Pre Roll Frames

Return type:

int32


---

**get_row_index**() → `int32`

Gets the row index for this section

Return type:

int32


---

**get_start_frame**() → `int32`

Get start frame. Will throw an exception if section has no start frame, use HasStartFrame to check first.

Returns:

Start frame of this section

Return type:

int32


---

**get_start_frame_seconds**() → `float`

Get start time in seconds. Will throw an exception if section has no start frame, use HasStartFrame to check first.

Returns:

Start time of this section

Return type:

float


---

**has_end_frame**() → `bool`

Has end frame

Returns:

Whether this section has a valid end frame (else infinite)

Return type:

bool


---

**has_start_frame**() → `bool`

Has start frame

Returns:

Whether this section has a valid start frame (else infinite)

Return type:

bool


---

**is_active**() → `bool`

Is Active

Return type:

bool


---

**is_locked**() → `bool`

Is Locked

Return type:

bool


---

**set_blend_type**( _blend_type_) → `None`

Sets this section’s blend type

Parameters:

**blend\_type** ( _MovieSceneBlendType_)


---

**set_color_tint**( _color_tint_) → `None`

Set this section’s color tint.

Parameters:

**color\_tint** ( _Color_)


---

**set_completion_mode**( _completion_mode_) → `None`

- Sets this section’s completion mode


Parameters:

**completion\_mode** ( _MovieSceneCompletionMode_)


---

**set_end_frame**( _end_frame_) → `None`

Set end frame

Parameters:

**end\_frame** ( _int32_) – The desired start frame for this section


---

**set_end_frame_bounded**( _is_bounded_) → `None`

Set end frame bounded

Parameters:

**is\_bounded** ( _bool_)


---

**set_end_frame_seconds**( _end_time_) → `None`

Set end time in seconds

Parameters:

**end\_time** ( _float_) – The desired end time for this section


---

**set_is_active**( _is_active_) → `None`

Whether or not this section is active.

Parameters:

**is\_active** ( _bool_)


---

**set_is_locked**( _is_locked_) → `None`

Whether or not this section is locked.

Parameters:

**is\_locked** ( _bool_)


---

**set_overlap_priority**( _new_priority_) → `None`

Sets this section’s priority over overlapping sections (higher wins)

Parameters:

**new\_priority** ( _int32_)


---

**set_post_roll_frames**( _post_roll_frames_) → `None`

Gets/sets the number of frames to continue ‘postrolling’ this section for after evaluation has ended.

Parameters:

**post\_roll\_frames** ( _int32_)


---

**set_pre_roll_frames**( _pre_roll_frames_) → `None`

Gets the number of frames to prepare this section for evaluation before it actually starts.

Parameters:

**pre\_roll\_frames** ( _int32_)


---

**set_range**( _start_frame_, _end_frame_) → `None`

Set range

Parameters:

- **start\_frame** ( _int32_) – The desired start frame for this section

- **end\_frame** ( _int32_) – The desired end frame for this section



---

**set_range_seconds**( _start_time_, _end_time_) → `None`

Set range in seconds

Parameters:

- **start\_time** ( _float_) – The desired start frame for this section

- **end\_time** ( _float_) – The desired end frame for this section



---

**set_row_index**( _new_row_index_) → `None`

Sets this section’s new row index

Parameters:

**new\_row\_index** ( _int32_)


---

**set_start_frame**( _start_frame_) → `None`

Set start frame

Parameters:

**start\_frame** ( _int32_) – The desired start frame for this section


---

**set_start_frame_bounded**( _is_bounded_) → `None`

Set start frame bounded

Parameters:

**is\_bounded** ( _bool_)


---

**set_start_frame_seconds**( _start_time_) → `None`

Set start time in seconds

Parameters:

**start\_time** ( _float_) – The desired start time for this section

### Table of Contents

- `unreal.MovieSceneSection`
  - `MovieSceneSection`
    - `MovieSceneSection.get_all_channels()`
    - `MovieSceneSection.get_auto_size_end_frame()`
    - `MovieSceneSection.get_auto_size_end_frame_seconds()`
    - `MovieSceneSection.get_auto_size_has_end_frame()`
    - `MovieSceneSection.get_auto_size_has_start_frame()`
    - `MovieSceneSection.get_auto_size_start_frame()`
    - `MovieSceneSection.get_auto_size_start_frame_seconds()`
    - `MovieSceneSection.get_blend_type()`
    - `MovieSceneSection.get_channel()`
    - `MovieSceneSection.get_channels_by_type()`
    - `MovieSceneSection.get_color_tint()`
    - `MovieSceneSection.get_completion_mode()`
    - `MovieSceneSection.get_end_frame()`
    - `MovieSceneSection.get_end_frame_seconds()`
    - `MovieSceneSection.get_overlap_priority()`
    - `MovieSceneSection.get_post_roll_frames()`
    - `MovieSceneSection.get_pre_roll_frames()`
    - `MovieSceneSection.get_row_index()`
    - `MovieSceneSection.get_start_frame()`
    - `MovieSceneSection.get_start_frame_seconds()`
    - `MovieSceneSection.has_end_frame()`
    - `MovieSceneSection.has_start_frame()`
    - `MovieSceneSection.is_active()`
    - `MovieSceneSection.is_locked()`
    - `MovieSceneSection.set_blend_type()`
    - `MovieSceneSection.set_color_tint()`
    - `MovieSceneSection.set_completion_mode()`
    - `MovieSceneSection.set_end_frame()`
    - `MovieSceneSection.set_end_frame_bounded()`
    - `MovieSceneSection.set_end_frame_seconds()`
    - `MovieSceneSection.set_is_active()`
    - `MovieSceneSection.set_is_locked()`
    - `MovieSceneSection.set_overlap_priority()`
    - `MovieSceneSection.set_post_roll_frames()`
    - `MovieSceneSection.set_pre_roll_frames()`
    - `MovieSceneSection.set_range()`
    - `MovieSceneSection.set_range_seconds()`
    - `MovieSceneSection.set_row_index()`
    - `MovieSceneSection.set_start_frame()`
    - `MovieSceneSection.set_start_frame_bounded()`
    - `MovieSceneSection.set_start_frame_seconds()`