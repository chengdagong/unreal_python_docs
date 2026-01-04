# unreal.MovieSceneSequence

```python
class unreal.MovieSceneSequence(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneSignedObject``


Abstract base class for movie scene animations (C++ version).

**C++ Source:**

- **Module**: MovieScene

- **File**: MovieSceneSequence.h



---

**add_marked_frame**( _marked_frame_) → `int32`

Add Marked Frame
deprecated: AddMarkedFrame is deprecated. Please use AddMarkedFrame that takes a time unit instead

Parameters:

**marked\_frame** ( _MovieSceneMarkedFrame_)

Return type:

int32


---

**add_marked_frame_to_sequence**( _marked_frame_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `int32`

- Add a given user marked frame.

- A unique label will be generated if the marked frame label is empty


InMarkedFrame: The given user marked frame to add \*

Parameters:

- **marked\_frame** ( _MovieSceneMarkedFrame_)

- **time\_unit** ( _MovieSceneTimeUnit_)


Returns:

The index to the newly added marked frame

Return type:

int32


---

**add_possessable**( _object_to_possess_) → `MovieSceneBindingProxy`

Add a new binding to this sequence that will possess the specified object

Parameters:

**object\_to\_possess** ( _Object_) – The object that this sequence should possess when evaluating

Returns:

A unique identifier for the new binding

Return type:

MovieSceneBindingProxy


---

**add_root_folder_to_sequence**( _new_folder_name_) → `MovieSceneFolder`

Add a root folder to the given sequence

Parameters:

**new\_folder\_name** ( _str_) – The name to give the added folder

Returns:

The newly created folder

Return type:

MovieSceneFolder


---

**add_spawnable_from_class**( _class_to_spawn_) → `MovieSceneBindingProxy`

Add Spawnable from Class
deprecated: AddSpawnableFromClass is deprecated. Please use AddSpawnableFromClass in the Level Sequence Editor Subsystem

Parameters:

**class\_to\_spawn** ( _type_ _(_ _Class_ _)_)

Return type:

MovieSceneBindingProxy


---

**add_spawnable_from_instance**( _object_to_spawn_) → `MovieSceneBindingProxy`

Add Spawnable from Instance
deprecated: AddSpawnableFromInstance is deprecated. Please use AddSpawnableFromInstance in the Level Sequence Editor Subsystem

Parameters:

**object\_to\_spawn** ( _Object_)

Return type:

MovieSceneBindingProxy


---

**add_track**( _track_type_) → `MovieSceneTrack`

Add a new track of the specified type

Parameters:

**track\_type** ( _type_ _(_ _Class_ _)_) – A UMovieSceneTrack class type to create

Returns:

The newly created track, if successful

Return type:

MovieSceneTrack


---

**are_marked_frames_locked**() → `bool`

- Are marked frames locked


Returns:

Whether the movie scene marked frames are locked

Return type:

bool


---

**delete_marked_frame**( _delete_index_) → `None`

- Delete the user marked frame by index.


DeleteIndex: The index to the user marked frame to delete

Parameters:

**delete\_index** ( _int32_)


---

**delete_marked_frames**() → `None`

- Delete all user marked frames



---

**find_binding_by_id**( _binding_id_) → `MovieSceneBindingProxy`

Attempt to locate a binding in this sequence by its Id

Parameters:

**binding\_id** ( _Guid_) – The binding Id to look up

Returns:

A unique identifier for the binding, or invalid

Return type:

MovieSceneBindingProxy


---

**find_binding_by_name**( _name_) → `MovieSceneBindingProxy`

Attempt to locate a binding in this sequence by its name

Parameters:

**name** ( _str_) – The display name of the binding to look up

Returns:

A unique identifier for the binding, or invalid

Return type:

MovieSceneBindingProxy


---

**find_binding_by_tag**( _binding_name_) → `MovieSceneObjectBindingID`

Find the first object binding ID associated with the specified tag name (set up through RMB->Expose on Object bindings from within sequencer)

Parameters:

**binding\_name** ( _Name_)

Return type:

MovieSceneObjectBindingID


---

**find_bindings_by_tag**( _binding_name_) → `Array\ [MovieSceneObjectBindingID]`

Find all object binding IDs associated with the specified tag name (set up through RMB->Expose on Object bindings from within sequencer)

Parameters:

**binding\_name** ( _Name_)

Return type:

Array\ [MovieSceneObjectBindingID]


---

**find_marked_frame_by_frame_number**( _frame_number_) → `int32`

Find Marked Frame by Frame Number
deprecated: FindMarkedFrameByFrameNumber is deprecated. Please use FindMarkedFrameByFrameNumber that takes a time unit instead

Parameters:

**frame\_number** ( _FrameNumber_)

Return type:

int32


---

**find_marked_frame_by_frame_number_in_sequence**( _frame_number_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `int32`

- Find the user marked frame by frame number


InFrameNumber: The frame number of the user marked frame to find

Parameters:

- **frame\_number** ( _FrameNumber_)

- **time\_unit** ( _MovieSceneTimeUnit_)


Return type:

int32


---

**find_marked_frame_by_label**( _label_) → `int32`

- Find the user marked frame by label


InLabel: The label to the user marked frame to find

Parameters:

**label** ( _str_)

Return type:

int32


---

**find_next_marked_frame**( _frame_number_, _forward_) → `int32`

Find Next Marked Frame
deprecated: FindNextMarkedFrame is deprecated. Please use FindNextMarkedFrame that takes a time unit and defaults to display rate instead

Parameters:

- **frame\_number** ( _FrameNumber_)

- **forward** ( _bool_)


Return type:

int32


---

**find_next_marked_frame_in_sequence**( _frame_number_, _forward_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `int32`

- Find the next/previous user marked frame from the given frame number


InFrameNumber: The frame number to find the next/previous user marked frame from \*
bForward: Find forward from the given frame number.

Parameters:

- **frame\_number** ( _FrameNumber_)

- **forward** ( _bool_)

- **time\_unit** ( _MovieSceneTimeUnit_)


Return type:

int32


---

**find_tracks_by_exact_type**( _track_type_) → `Array\ [MovieSceneTrack]`

Find all tracks of the specified type, not allowing sub-classed types

Parameters:

**track\_type** ( _type_ _(_ _Class_ _)_) – A UMovieSceneTrack class type specifying the exact types of track to return

Returns:

An array containing any tracks that are exactly the same as the type specified

Return type:

Array\ [MovieSceneTrack]


---

**find_tracks_by_type**( _track_type_) → `Array\ [MovieSceneTrack]`

Find all tracks of the specified type

Parameters:

**track\_type** ( _type_ _(_ _Class_ _)_) – A UMovieSceneTrack class type specifying which types of track to return

Returns:

An array containing any tracks that match the type specified

Return type:

Array\ [MovieSceneTrack]


---

**get_binding_id**( _binding_) → `MovieSceneObjectBindingID`

Get the binding ID for a binding within a sequence.
note:: The resulting binding is only valid when applied to properties within the same sequence as this binding. Use GetPortableBindingID for bindings which live in different sub-sequences.

Parameters:

**binding** ( _MovieSceneBindingProxy_)

Returns:

The binding’s id

Return type:

MovieSceneObjectBindingID


---

**get_bindings**() → `Array\ [MovieSceneBindingProxy]`

Get all the bindings in this sequence

Returns:

An array of unique identifiers for all the bindings in this sequence

Return type:

Array\ [MovieSceneBindingProxy]


---

**get_clock_source**() → `UpdateClockSource`

Get the clock source for this sequence

Returns:

The clock source for this sequence

Return type:

UpdateClockSource


---

**get_custom_clock**() → `MovieSceneClock`

Get the custom clock for this sequence

Returns:

The MovieSceneClock for this sequence

Return type:

MovieSceneClock


---

**get_display_rate**() → `FrameRate`

Gets this sequence’s display rate

Returns:

The display rate that this sequence is displayed as

Return type:

FrameRate


---

**get_earliest_timecode_source**() → `MovieSceneTimecodeSource`

Get the earliest timecode source out of all of the movie scene sections contained within this sequence’s movie scene.

Return type:

MovieSceneTimecodeSource


---

**get_evaluation_type**() → `MovieSceneEvaluationType`

Get the evaluation type for this sequence

Returns:

The evaluation type for this sequence

Return type:

MovieSceneEvaluationType


---

**get_marked_frames**() → `Array\ [MovieSceneMarkedFrame]`

Get Marked Frames
deprecated: GetMarkedFrames is deprecated. Please use GetMarkedFrames that takes a time unit instead

Return type:

Array\ [MovieSceneMarkedFrame]


---

**get_marked_frames_from_sequence**( _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `Array\ [MovieSceneMarkedFrame]`

- Get the marked frames for this sequence


Parameters:

**time\_unit** ( _MovieSceneTimeUnit_)

Returns:

Return the user marked frames

Return type:

Array\ [MovieSceneMarkedFrame]


---

**get_movie_scene**() → `MovieScene`

Get this sequence’s movie scene data

Returns:

This sequence’s movie scene data object

Return type:

MovieScene


---

**get_playback_end**() → `int32`

Get playback end of this sequence in display rate resolution

Returns:

Playback end of this sequence

Return type:

int32


---

**get_playback_end_seconds**() → `float`

Get playback end of this sequence in seconds

Returns:

Playback end of this sequence

Return type:

float


---

**get_playback_range**() → `SequencerScriptingRange`

Get playback range of this sequence in display rate resolution

Returns:

Playback range of this sequence

Return type:

SequencerScriptingRange


---

**get_playback_start**() → `int32`

Get playback start of this sequence in display rate resolution

Returns:

Playback start of this sequence

Return type:

int32


---

**get_playback_start_seconds**() → `float`

Get playback start of this sequence in seconds

Returns:

Playback start of this sequence

Return type:

float


---

**get_portable_binding_id**( _destination_sequence_, _binding_) → `MovieSceneObjectBindingID`

Get a portable binding ID for a binding that resides in a different sequence to the one where this binding will be resolved.
note:: This function must be used over GetBindingID when the target binding resides in different shots or sub-sequences.
note:: Only unique instances of sequences within a root sequences are supported

Parameters:

- **destination\_sequence** ( _MovieSceneSequence_) – The sequence that will own or resolve the resulting binding ID. For example, if the binding ID will be applied to a camera cut section pass the sequence that contains the camera cut track to this parameter.

- **binding** ( _MovieSceneBindingProxy_)


Returns:

The binding’s id

Return type:

MovieSceneObjectBindingID


---

**get_possessables**() → `Array\ [MovieSceneBindingProxy]`

Get all the possessables in this sequence. It is understood for the purpose of this function that this means the bindings are not custom.

Returns:

Possessables in this sequence

Return type:

Array\ [MovieSceneBindingProxy]


---

**get_root_folders_in_sequence**() → `Array\ [MovieSceneFolder]`

Get the root folders in the provided sequence

Returns:

The folders contained within the given sequence

Return type:

Array\ [MovieSceneFolder]


---

**get_spawnables**() → `Array\ [MovieSceneBindingProxy]`

Get all the spawnables in this sequence. For Level Sequences, this includes bindings with binding type UMovieSceneSpawnableActorBinding.

Returns:

Spawnables in this sequence

Return type:

Array\ [MovieSceneBindingProxy]


---

**get_tick_resolution**() → `FrameRate`

Gets this sequence’s tick resolution

Returns:

The tick resolution of the sequence, defining the smallest unit of time representable on this sequence

Return type:

FrameRate


---

**get_tracks**() → `Array\ [MovieSceneTrack]`

Get all tracks

Returns:

An array containing all tracks in this sequence

Return type:

Array\ [MovieSceneTrack]


---

**get_view_range_end**() → `double`

Get the sequence view range end in seconds

Returns:

The view range end time in seconds for this sequence

Return type:

double


---

**get_view_range_start**() → `double`

Get the sequence view range start in seconds

Returns:

The view range start time in seconds for this sequence

Return type:

double


---

**get_work_range_end**() → `double`

Get the sequence work range end in seconds

Returns:

The work range end time in seconds for this sequence

Return type:

double


---

**get_work_range_start**() → `double`

Get the sequence work range start in seconds

Returns:

The work range start time in seconds for this sequence

Return type:

double


---

**is_playback_range_locked**() → `bool`

- Is playback ranged locked


Returns:

Whether the movie scene playback range is locked

Return type:

bool


---

**is_read_only**() → `bool`

- Is read only


Returns:

Whether the movie scene is read only or not

Return type:

bool


---

**locate_bound_objects**( _binding_, _context_) → `Array\ [Object]`

Locate all the objects that correspond to the specified object ID, using the specified context

Parameters:

- **binding** ( _MovieSceneBindingProxy_) – The object binding

- **context** ( _Object_) – Optional context to use to find the required object


Returns:

An array of all bound objects

Return type:

Array\ [Object]


---

**make_range**( _start_frame_, _duration_) → `SequencerScriptingRange`

Make a new range for this sequence in its display rate

Parameters:

- **start\_frame** ( _int32_) – The frame at which to start the range

- **duration** ( _int32_) – The length of the range


Returns:

Specified sequencer range

Return type:

SequencerScriptingRange


---

**make_range_seconds**( _start_time_, _duration_) → `SequencerScriptingRange`

Make a new range for this sequence in seconds

Parameters:

- **start\_time** ( _float_) – The time in seconds at which to start the range

- **duration** ( _float_) – The length of the range in seconds


Returns:

Specified sequencer range

Return type:

SequencerScriptingRange


---

**remove_root_folder_from_sequence**( _folder_) → `None`

Remove a root folder from the given sequence. Will throw an exception if the specified folder is not valid or not a root folder.

Parameters:

**folder** ( _MovieSceneFolder_) – The folder to remove


---

**remove_track**( _track_) → `bool`

Removes a track

Parameters:

**track** ( _MovieSceneTrack_) – The track to remove

Returns:

Whether the track was successfully removed

Return type:

bool


---

**resolve_binding_id**( _object_binding_id_) → `MovieSceneBindingProxy`

Make a binding for the given binding ID

Parameters:

**object\_binding\_id** ( _MovieSceneObjectBindingID_)

Returns:

The new binding proxy

Return type:

MovieSceneBindingProxy


---

**set_clock_source**( _clock_source_) → `None`

Set the clock source for this sequence

Parameters:

**clock\_source** ( _UpdateClockSource_) – The clock source to set for this sequence


---

**set_display_rate**( _display_rate_) → `None`

Sets this sequence’s display rate

Parameters:

**display\_rate** ( _FrameRate_) – The display rate that this sequence is displayed as


---

**set_evaluation_type**( _evaluation_type_) → `None`

Set the evaluation type for this sequence

Parameters:

**evaluation\_type** ( _MovieSceneEvaluationType_) – The evaluation type to set for this sequence


---

**set_marked_frame**( _mark_index_, _frame_number_) → `None`

Set Marked Frame
deprecated: SetMarkedFrame is deprecated. Please use SetMarkedFrame that takes a time unit instead

Parameters:

- **mark\_index** ( _int32_)

- **frame\_number** ( _FrameNumber_)



---

**set_marked_frame_in_sequence**( _mark_index_, _frame_number_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_) → `None`

- Sets the frame number for the given marked frame index. Does not maintain sort. Call SortMarkedFrames


InMarkIndex: The given user marked frame index to edit \*
InFrameNumber: The frame number to set

Parameters:

- **mark\_index** ( _int32_)

- **frame\_number** ( _FrameNumber_)

- **time\_unit** ( _MovieSceneTimeUnit_)



---

**set_marked_frames_locked**( _locked_) → `None`

- Set marked frames locked


bInLocked: Whether the movie scene marked frames should be locked

Parameters:

**locked** ( _bool_)


---

**set_playback_end**( _end_frame_) → `None`

Set playback end of this sequence

Parameters:

**end\_frame** ( _int32_) – The desired end frame for this sequence


---

**set_playback_end_seconds**( _end_time_) → `None`

Set playback end of this sequence in seconds

Parameters:

**end\_time** ( _float_) – The desired end time in seconds for this sequence


---

**set_playback_range_locked**( _locked_) → `None`

- Set playback range locked


bInLocked: Whether the movie scene playback range should be locked

Parameters:

**locked** ( _bool_)


---

**set_playback_start**( _start_frame_) → `None`

Set playback start of this sequence

Parameters:

**start\_frame** ( _int32_) – The desired start frame for this sequence


---

**set_playback_start_seconds**( _start_time_) → `None`

Set playback start of this sequence in seconds

Parameters:

**start\_time** ( _float_) – The desired start time in seconds for this sequence


---

**set_read_only**( _read_only_) → `None`

- Set read only


bInReadOnly: Whether the movie scene should be read only or not

Parameters:

**read\_only** ( _bool_)


---

**set_tick_resolution**( _tick_resolution_) → `None`

Sets this sequence’s tick resolution and migrates frame times

Parameters:

**tick\_resolution** ( _FrameRate_) – The tick resolution of the sequence, defining the smallest unit of time representable on this sequence


---

**set_tick_resolution_directly**( _tick_resolution_) → `None`

Sets this sequence’s tick resolution directly without migrating frame times

Parameters:

**tick\_resolution** ( _FrameRate_) – The tick resolution of the sequence, defining the smallest unit of time representable on this sequence


---

**set_view_range_end**( _end_time_in_seconds_) → `None`

Set the sequence view range end in seconds

Parameters:

**end\_time\_in\_seconds** ( _double_)


---

**set_view_range_start**( _start_time_in_seconds_) → `None`

Set the sequence view range start in seconds

Parameters:

**start\_time\_in\_seconds** ( _double_) – The desired view range start time in seconds for this sequence


---

**set_work_range_end**( _end_time_in_seconds_) → `None`

Set the sequence work range end in seconds

Parameters:

**end\_time\_in\_seconds** ( _double_)


---

**set_work_range_start**( _start_time_in_seconds_) → `None`

Set the sequence work range start in seconds

Parameters:

**start\_time\_in\_seconds** ( _double_) – The desired work range start time in seconds for this sequence


---

**sort_marked_frames**() → `None`

- Sort the marked frames in chronological order


### Table of Contents

- `unreal.MovieSceneSequence`
  - `MovieSceneSequence`
    - `MovieSceneSequence.add_marked_frame()`
    - `MovieSceneSequence.add_marked_frame_to_sequence()`
    - `MovieSceneSequence.add_possessable()`
    - `MovieSceneSequence.add_root_folder_to_sequence()`
    - `MovieSceneSequence.add_spawnable_from_class()`
    - `MovieSceneSequence.add_spawnable_from_instance()`
    - `MovieSceneSequence.add_track()`
    - `MovieSceneSequence.are_marked_frames_locked()`
    - `MovieSceneSequence.delete_marked_frame()`
    - `MovieSceneSequence.delete_marked_frames()`
    - `MovieSceneSequence.find_binding_by_id()`
    - `MovieSceneSequence.find_binding_by_name()`
    - `MovieSceneSequence.find_binding_by_tag()`
    - `MovieSceneSequence.find_bindings_by_tag()`
    - `MovieSceneSequence.find_marked_frame_by_frame_number()`
    - `MovieSceneSequence.find_marked_frame_by_frame_number_in_sequence()`
    - `MovieSceneSequence.find_marked_frame_by_label()`
    - `MovieSceneSequence.find_next_marked_frame()`
    - `MovieSceneSequence.find_next_marked_frame_in_sequence()`
    - `MovieSceneSequence.find_tracks_by_exact_type()`
    - `MovieSceneSequence.find_tracks_by_type()`
    - `MovieSceneSequence.get_binding_id()`
    - `MovieSceneSequence.get_bindings()`
    - `MovieSceneSequence.get_clock_source()`
    - `MovieSceneSequence.get_custom_clock()`
    - `MovieSceneSequence.get_display_rate()`
    - `MovieSceneSequence.get_earliest_timecode_source()`
    - `MovieSceneSequence.get_evaluation_type()`
    - `MovieSceneSequence.get_marked_frames()`
    - `MovieSceneSequence.get_marked_frames_from_sequence()`
    - `MovieSceneSequence.get_movie_scene()`
    - `MovieSceneSequence.get_playback_end()`
    - `MovieSceneSequence.get_playback_end_seconds()`
    - `MovieSceneSequence.get_playback_range()`
    - `MovieSceneSequence.get_playback_start()`
    - `MovieSceneSequence.get_playback_start_seconds()`
    - `MovieSceneSequence.get_portable_binding_id()`
    - `MovieSceneSequence.get_possessables()`
    - `MovieSceneSequence.get_root_folders_in_sequence()`
    - `MovieSceneSequence.get_spawnables()`
    - `MovieSceneSequence.get_tick_resolution()`
    - `MovieSceneSequence.get_tracks()`
    - `MovieSceneSequence.get_view_range_end()`
    - `MovieSceneSequence.get_view_range_start()`
    - `MovieSceneSequence.get_work_range_end()`
    - `MovieSceneSequence.get_work_range_start()`
    - `MovieSceneSequence.is_playback_range_locked()`
    - `MovieSceneSequence.is_read_only()`
    - `MovieSceneSequence.locate_bound_objects()`
    - `MovieSceneSequence.make_range()`
    - `MovieSceneSequence.make_range_seconds()`
    - `MovieSceneSequence.remove_root_folder_from_sequence()`
    - `MovieSceneSequence.remove_track()`
    - `MovieSceneSequence.resolve_binding_id()`
    - `MovieSceneSequence.set_clock_source()`
    - `MovieSceneSequence.set_display_rate()`
    - `MovieSceneSequence.set_evaluation_type()`
    - `MovieSceneSequence.set_marked_frame()`
    - `MovieSceneSequence.set_marked_frame_in_sequence()`
    - `MovieSceneSequence.set_marked_frames_locked()`
    - `MovieSceneSequence.set_playback_end()`
    - `MovieSceneSequence.set_playback_end_seconds()`
    - `MovieSceneSequence.set_playback_range_locked()`
    - `MovieSceneSequence.set_playback_start()`
    - `MovieSceneSequence.set_playback_start_seconds()`
    - `MovieSceneSequence.set_read_only()`
    - `MovieSceneSequence.set_tick_resolution()`
    - `MovieSceneSequence.set_tick_resolution_directly()`
    - `MovieSceneSequence.set_view_range_end()`
    - `MovieSceneSequence.set_view_range_start()`
    - `MovieSceneSequence.set_work_range_end()`
    - `MovieSceneSequence.set_work_range_start()`
    - `MovieSceneSequence.sort_marked_frames()`