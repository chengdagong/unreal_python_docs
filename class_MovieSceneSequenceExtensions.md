# unreal.MovieSceneSequenceExtensions

```python
class unreal.MovieSceneSequenceExtensions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Function library containing methods that should be hoisted onto UMovieSceneSequences for scripting purposes

**C++ Source:**

- **Plugin**: SequencerScripting

- **Module**: SequencerScripting

- **File**: MovieSceneSequenceExtensions.h



---

_classmethod_ add_marked_frame( _sequence_, _marked_frame_)→int32

Add Marked Frame
deprecated: AddMarkedFrame is deprecated. Please use AddMarkedFrame that takes a time unit instead

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **marked\_frame** ( _MovieSceneMarkedFrame_)


Return type:

int32


---

_classmethod_ add_marked_frame_to_sequence( _sequence_, _marked_frame_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_)→int32

- Add a given user marked frame.

- A unique label will be generated if the marked frame label is empty


InMarkedFrame: The given user marked frame to add \*

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **marked\_frame** ( _MovieSceneMarkedFrame_)

- **time\_unit** ( _MovieSceneTimeUnit_)


Returns:

The index to the newly added marked frame

Return type:

int32


---

_classmethod_ add_possessable( _sequence_, _object_to_possess_)→MovieSceneBindingProxy

Add a new binding to this sequence that will possess the specified object

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to add a possessable to

- **object\_to\_possess** ( _Object_) – The object that this sequence should possess when evaluating


Returns:

A unique identifier for the new binding

Return type:

MovieSceneBindingProxy


---

_classmethod_ add_root_folder_to_sequence( _sequence_, _new_folder_name_)→MovieSceneFolder

Add a root folder to the given sequence

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to add a folder to

- **new\_folder\_name** ( _str_) – The name to give the added folder


Returns:

The newly created folder

Return type:

MovieSceneFolder


---

_classmethod_ add_spawnable_from_class( _sequence_, _class_to_spawn_)→MovieSceneBindingProxy

Add Spawnable from Class
deprecated: AddSpawnableFromClass is deprecated. Please use AddSpawnableFromClass in the Level Sequence Editor Subsystem

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **class\_to\_spawn** ( _type_ _(_ _Class_ _)_)


Return type:

MovieSceneBindingProxy


---

_classmethod_ add_spawnable_from_instance( _sequence_, _object_to_spawn_)→MovieSceneBindingProxy

Add Spawnable from Instance
deprecated: AddSpawnableFromInstance is deprecated. Please use AddSpawnableFromInstance in the Level Sequence Editor Subsystem

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **object\_to\_spawn** ( _Object_)


Return type:

MovieSceneBindingProxy


---

_classmethod_ add_track( _sequence_, _track_type_)→MovieSceneTrack

Add a new track of the specified type

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to use

- **track\_type** ( _type_ _(_ _Class_ _)_) – A UMovieSceneTrack class type to create


Returns:

The newly created track, if successful

Return type:

MovieSceneTrack


---

_classmethod_ are_marked_frames_locked( _sequence_)→bool

- Are marked frames locked


Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

Whether the movie scene marked frames are locked

Return type:

bool


---

_classmethod_ delete_marked_frame( _sequence_, _delete_index_)→None

- Delete the user marked frame by index.


DeleteIndex: The index to the user marked frame to delete

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **delete\_index** ( _int32_)



---

_classmethod_ delete_marked_frames( _sequence_)→None

- Delete all user marked frames


Parameters:

**sequence** ( _MovieSceneSequence_)


---

_classmethod_ find_binding_by_id( _sequence_, _binding_id_)→MovieSceneBindingProxy

Attempt to locate a binding in this sequence by its Id

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to find the binding

- **binding\_id** ( _Guid_) – The binding Id to look up


Returns:

A unique identifier for the binding, or invalid

Return type:

MovieSceneBindingProxy


---

_classmethod_ find_binding_by_name( _sequence_, _name_)→MovieSceneBindingProxy

Attempt to locate a binding in this sequence by its name

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to find the binding

- **name** ( _str_) – The display name of the binding to look up


Returns:

A unique identifier for the binding, or invalid

Return type:

MovieSceneBindingProxy


---

_classmethod_ find_marked_frame_by_frame_number( _sequence_, _frame_number_)→int32

Find Marked Frame by Frame Number
deprecated: FindMarkedFrameByFrameNumber is deprecated. Please use FindMarkedFrameByFrameNumber that takes a time unit instead

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **frame\_number** ( _FrameNumber_)


Return type:

int32


---

_classmethod_ find_marked_frame_by_frame_number_in_sequence( _sequence_, _frame_number_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_)→int32

- Find the user marked frame by frame number


InFrameNumber: The frame number of the user marked frame to find

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **frame\_number** ( _FrameNumber_)

- **time\_unit** ( _MovieSceneTimeUnit_)


Return type:

int32


---

_classmethod_ find_marked_frame_by_label( _sequence_, _label_)→int32

- Find the user marked frame by label


InLabel: The label to the user marked frame to find

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **label** ( _str_)


Return type:

int32


---

_classmethod_ find_next_marked_frame( _sequence_, _frame_number_, _forward_)→int32

Find Next Marked Frame
deprecated: FindNextMarkedFrame is deprecated. Please use FindNextMarkedFrame that takes a time unit and defaults to display rate instead

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **frame\_number** ( _FrameNumber_)

- **forward** ( _bool_)


Return type:

int32


---

_classmethod_ find_next_marked_frame_in_sequence( _sequence_, _frame_number_, _forward_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_)→int32

- Find the next/previous user marked frame from the given frame number


InFrameNumber: The frame number to find the next/previous user marked frame from \*
bForward: Find forward from the given frame number.

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **frame\_number** ( _FrameNumber_)

- **forward** ( _bool_)

- **time\_unit** ( _MovieSceneTimeUnit_)


Return type:

int32


---

_classmethod_ find_tracks_by_exact_type( _sequence_, _track_type_)→Array\ [MovieSceneTrack]

Find all tracks of the specified type, not allowing sub-classed types

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to use

- **track\_type** ( _type_ _(_ _Class_ _)_) – A UMovieSceneTrack class type specifying the exact types of track to return


Returns:

An array containing any tracks that are exactly the same as the type specified

Return type:

Array\ [MovieSceneTrack]


---

_classmethod_ find_tracks_by_type( _sequence_, _track_type_)→Array\ [MovieSceneTrack]

Find all tracks of the specified type

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to use

- **track\_type** ( _type_ _(_ _Class_ _)_) – A UMovieSceneTrack class type specifying which types of track to return


Returns:

An array containing any tracks that match the type specified

Return type:

Array\ [MovieSceneTrack]


---

_classmethod_ get_binding_id( _sequence_, _binding_)→MovieSceneObjectBindingID

Get the binding ID for a binding within a sequence.
note:: The resulting binding is only valid when applied to properties within the same sequence as this binding. Use GetPortableBindingID for bindings which live in different sub-sequences.

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **binding** ( _MovieSceneBindingProxy_)


Returns:

The binding’s id

Return type:

MovieSceneObjectBindingID


---

_classmethod_ get_bindings( _sequence_)→Array\ [MovieSceneBindingProxy]

Get all the bindings in this sequence

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to get bindings for

Returns:

An array of unique identifiers for all the bindings in this sequence

Return type:

Array\ [MovieSceneBindingProxy]


---

_classmethod_ get_clock_source( _sequence_)→UpdateClockSource

Get the clock source for this sequence

Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

The clock source for this sequence

Return type:

UpdateClockSource


---

_classmethod_ get_custom_clock( _sequence_)→MovieSceneClock

Get the custom clock for this sequence

Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

The MovieSceneClock for this sequence

Return type:

MovieSceneClock


---

_classmethod_ get_display_rate( _sequence_)→FrameRate

Gets this sequence’s display rate

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to use

Returns:

The display rate that this sequence is displayed as

Return type:

FrameRate


---

_classmethod_ get_evaluation_type( _sequence_)→MovieSceneEvaluationType

Get the evaluation type for this sequence

Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

The evaluation type for this sequence

Return type:

MovieSceneEvaluationType


---

_classmethod_ get_marked_frames( _sequence_)→Array\ [MovieSceneMarkedFrame]

Get Marked Frames
deprecated: GetMarkedFrames is deprecated. Please use GetMarkedFrames that takes a time unit instead

Parameters:

**sequence** ( _MovieSceneSequence_)

Return type:

Array\ [MovieSceneMarkedFrame]


---

_classmethod_ get_marked_frames_from_sequence( _sequence_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_)→Array\ [MovieSceneMarkedFrame]

- Get the marked frames for this sequence


Parameters:

- **sequence** ( _MovieSceneSequence_)

- **time\_unit** ( _MovieSceneTimeUnit_)


Returns:

Return the user marked frames

Return type:

Array\ [MovieSceneMarkedFrame]


---

_classmethod_ get_movie_scene( _sequence_)→MovieScene

Get this sequence’s movie scene data

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to use

Returns:

This sequence’s movie scene data object

Return type:

MovieScene


---

_classmethod_ get_playback_end( _sequence_)→int32

Get playback end of this sequence in display rate resolution

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence within which to get the playback end

Returns:

Playback end of this sequence

Return type:

int32


---

_classmethod_ get_playback_end_seconds( _sequence_)→float

Get playback end of this sequence in seconds

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence within which to get the playback end

Returns:

Playback end of this sequence

Return type:

float


---

_classmethod_ get_playback_range( _sequence_)→SequencerScriptingRange

Get playback range of this sequence in display rate resolution

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence within which to get the playback range

Returns:

Playback range of this sequence

Return type:

SequencerScriptingRange


---

_classmethod_ get_playback_start( _sequence_)→int32

Get playback start of this sequence in display rate resolution

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence within which to get the playback start

Returns:

Playback start of this sequence

Return type:

int32


---

_classmethod_ get_playback_start_seconds( _sequence_)→float

Get playback start of this sequence in seconds

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence within which to get the playback start

Returns:

Playback start of this sequence

Return type:

float


---

_classmethod_ get_portable_binding_id( _root_sequence_, _destination_sequence_, _binding_)→MovieSceneObjectBindingID

Get a portable binding ID for a binding that resides in a different sequence to the one where this binding will be resolved.
note:: This function must be used over GetBindingID when the target binding resides in different shots or sub-sequences.
note:: Only unique instances of sequences within a root sequences are supported

Parameters:

- **root\_sequence** ( _MovieSceneSequence_) – The root sequence that contains both the destination sequence (that will resolve the binding ID) and the target sequence that contains the actual binding

- **destination\_sequence** ( _MovieSceneSequence_) – The sequence that will own or resolve the resulting binding ID. For example, if the binding ID will be applied to a camera cut section pass the sequence that contains the camera cut track to this parameter.

- **binding** ( _MovieSceneBindingProxy_)


Returns:

The binding’s id

Return type:

MovieSceneObjectBindingID


---

_classmethod_ get_possessables( _sequence_)→Array\ [MovieSceneBindingProxy]

Get all the possessables in this sequence. It is understood for the purpose of this function that this means the bindings are not custom.

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to get possessables for

Returns:

Possessables in this sequence

Return type:

Array\ [MovieSceneBindingProxy]


---

_classmethod_ get_root_folders_in_sequence( _sequence_)→Array\ [MovieSceneFolder]

Get the root folders in the provided sequence

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to retrieve folders from

Returns:

The folders contained within the given sequence

Return type:

Array\ [MovieSceneFolder]


---

_classmethod_ get_spawnables( _sequence_)→Array\ [MovieSceneBindingProxy]

Get all the spawnables in this sequence. For Level Sequences, this includes bindings with binding type UMovieSceneSpawnableActorBinding.

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to get spawnables for

Returns:

Spawnables in this sequence

Return type:

Array\ [MovieSceneBindingProxy]


---

_classmethod_ get_tick_resolution( _sequence_)→FrameRate

Gets this sequence’s tick resolution

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to use

Returns:

The tick resolution of the sequence, defining the smallest unit of time representable on this sequence

Return type:

FrameRate


---

_classmethod_ get_tracks( _sequence_)→Array\ [MovieSceneTrack]

Get all tracks

Parameters:

**sequence** ( _MovieSceneSequence_) – The sequence to use

Returns:

An array containing all tracks in this sequence

Return type:

Array\ [MovieSceneTrack]


---

_classmethod_ get_view_range_end( _sequence_)→double

Get the sequence view range end in seconds

Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

The view range end time in seconds for this sequence

Return type:

double


---

_classmethod_ get_view_range_start( _sequence_)→double

Get the sequence view range start in seconds

Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

The view range start time in seconds for this sequence

Return type:

double


---

_classmethod_ get_work_range_end( _sequence_)→double

Get the sequence work range end in seconds

Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

The work range end time in seconds for this sequence

Return type:

double


---

_classmethod_ get_work_range_start( _sequence_)→double

Get the sequence work range start in seconds

Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

The work range start time in seconds for this sequence

Return type:

double


---

_classmethod_ is_playback_range_locked( _sequence_)→bool

- Is playback ranged locked


Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

Whether the movie scene playback range is locked

Return type:

bool


---

_classmethod_ is_read_only( _sequence_)→bool

- Is read only


Parameters:

**sequence** ( _MovieSceneSequence_)

Returns:

Whether the movie scene is read only or not

Return type:

bool


---

_classmethod_ locate_bound_objects( _sequence_, _binding_, _context_)→Array\ [Object]

Locate all the objects that correspond to the specified object ID, using the specified context

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to locate bound objects for

- **binding** ( _MovieSceneBindingProxy_) – The object binding

- **context** ( _Object_) – Optional context to use to find the required object


Returns:

An array of all bound objects

Return type:

Array\ [Object]


---

_classmethod_ make_range( _sequence_, _start_frame_, _duration_)→SequencerScriptingRange

Make a new range for this sequence in its display rate

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to find the binding

- **start\_frame** ( _int32_) – The frame at which to start the range

- **duration** ( _int32_) – The length of the range


Returns:

Specified sequencer range

Return type:

SequencerScriptingRange


---

_classmethod_ make_range_seconds( _sequence_, _start_time_, _duration_)→SequencerScriptingRange

Make a new range for this sequence in seconds

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to find the binding

- **start\_time** ( _float_) – The time in seconds at which to start the range

- **duration** ( _float_) – The length of the range in seconds


Returns:

Specified sequencer range

Return type:

SequencerScriptingRange


---

_classmethod_ remove_root_folder_from_sequence( _sequence_, _folder_)→None

Remove a root folder from the given sequence. Will throw an exception if the specified folder is not valid or not a root folder.

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence That the folder belongs to

- **folder** ( _MovieSceneFolder_) – The folder to remove



---

_classmethod_ remove_track( _sequence_, _track_)→bool

Removes a track

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to use

- **track** ( _MovieSceneTrack_) – The track to remove


Returns:

Whether the track was successfully removed

Return type:

bool


---

_classmethod_ resolve_binding_id( _root_sequence_, _object_binding_id_)→MovieSceneBindingProxy

Make a binding for the given binding ID

Parameters:

- **root\_sequence** ( _MovieSceneSequence_) – The root sequence that contains the sequence

- **object\_binding\_id** ( _MovieSceneObjectBindingID_)


Returns:

The new binding proxy

Return type:

MovieSceneBindingProxy


---

_classmethod_ set_clock_source( _sequence_, _clock_source_)→None

Set the clock source for this sequence

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **clock\_source** ( _UpdateClockSource_) – The clock source to set for this sequence



---

_classmethod_ set_display_rate( _sequence_, _display_rate_)→None

Sets this sequence’s display rate

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to use

- **display\_rate** ( _FrameRate_) – The display rate that this sequence is displayed as



---

_classmethod_ set_evaluation_type( _sequence_, _evaluation_type_)→None

Set the evaluation type for this sequence

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **evaluation\_type** ( _MovieSceneEvaluationType_) – The evaluation type to set for this sequence



---

_classmethod_ set_marked_frame( _sequence_, _mark_index_, _frame_number_)→None

Set Marked Frame
deprecated: SetMarkedFrame is deprecated. Please use SetMarkedFrame that takes a time unit instead

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **mark\_index** ( _int32_)

- **frame\_number** ( _FrameNumber_)



---

_classmethod_ set_marked_frame_in_sequence( _sequence_, _mark_index_, _frame_number_, _time_unit=MovieSceneTimeUnit.DISPLAY_RATE_)→None

- Sets the frame number for the given marked frame index. Does not maintain sort. Call SortMarkedFrames


InMarkIndex: The given user marked frame index to edit \*
InFrameNumber: The frame number to set

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **mark\_index** ( _int32_)

- **frame\_number** ( _FrameNumber_)

- **time\_unit** ( _MovieSceneTimeUnit_)



---

_classmethod_ set_marked_frames_locked( _sequence_, _locked_)→None

- Set marked frames locked


bInLocked: Whether the movie scene marked frames should be locked

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **locked** ( _bool_)



---

_classmethod_ set_playback_end( _sequence_, _end_frame_)→None

Set playback end of this sequence

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to set the playback end

- **end\_frame** ( _int32_) – The desired end frame for this sequence



---

_classmethod_ set_playback_end_seconds( _sequence_, _end_time_)→None

Set playback end of this sequence in seconds

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to set the playback end

- **end\_time** ( _float_) – The desired end time in seconds for this sequence



---

_classmethod_ set_playback_range_locked( _sequence_, _locked_)→None

- Set playback range locked


bInLocked: Whether the movie scene playback range should be locked

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **locked** ( _bool_)



---

_classmethod_ set_playback_start( _sequence_, _start_frame_)→None

Set playback start of this sequence

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to set the playback start

- **start\_frame** ( _int32_) – The desired start frame for this sequence



---

_classmethod_ set_playback_start_seconds( _sequence_, _start_time_)→None

Set playback start of this sequence in seconds

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence within which to set the playback start

- **start\_time** ( _float_) – The desired start time in seconds for this sequence



---

_classmethod_ set_read_only( _sequence_, _read_only_)→None

- Set read only


bInReadOnly: Whether the movie scene should be read only or not

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **read\_only** ( _bool_)



---

_classmethod_ set_tick_resolution( _sequence_, _tick_resolution_)→None

Sets this sequence’s tick resolution and migrates frame times

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to use

- **tick\_resolution** ( _FrameRate_) – The tick resolution of the sequence, defining the smallest unit of time representable on this sequence



---

_classmethod_ set_tick_resolution_directly( _sequence_, _tick_resolution_)→None

Sets this sequence’s tick resolution directly without migrating frame times

Parameters:

- **sequence** ( _MovieSceneSequence_) – The sequence to use

- **tick\_resolution** ( _FrameRate_) – The tick resolution of the sequence, defining the smallest unit of time representable on this sequence



---

_classmethod_ set_view_range_end( _sequence_, _end_time_in_seconds_)→None

Set the sequence view range end in seconds

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **end\_time\_in\_seconds** ( _double_)



---

_classmethod_ set_view_range_start( _sequence_, _start_time_in_seconds_)→None

Set the sequence view range start in seconds

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **start\_time\_in\_seconds** ( _double_) – The desired view range start time in seconds for this sequence



---

_classmethod_ set_work_range_end( _sequence_, _end_time_in_seconds_)→None

Set the sequence work range end in seconds

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **end\_time\_in\_seconds** ( _double_)



---

_classmethod_ set_work_range_start( _sequence_, _start_time_in_seconds_)→None

Set the sequence work range start in seconds

Parameters:

- **sequence** ( _MovieSceneSequence_)

- **start\_time\_in\_seconds** ( _double_) – The desired work range start time in seconds for this sequence



---

_classmethod_ sort_marked_frames( _sequence_)→None

- Sort the marked frames in chronological order


Parameters:

**sequence** ( _MovieSceneSequence_)

### Table of Contents

- `unreal.MovieSceneSequenceExtensions`
  - `MovieSceneSequenceExtensions`
    - `MovieSceneSequenceExtensions.add_marked_frame()`
    - `MovieSceneSequenceExtensions.add_marked_frame_to_sequence()`
    - `MovieSceneSequenceExtensions.add_possessable()`
    - `MovieSceneSequenceExtensions.add_root_folder_to_sequence()`
    - `MovieSceneSequenceExtensions.add_spawnable_from_class()`
    - `MovieSceneSequenceExtensions.add_spawnable_from_instance()`
    - `MovieSceneSequenceExtensions.add_track()`
    - `MovieSceneSequenceExtensions.are_marked_frames_locked()`
    - `MovieSceneSequenceExtensions.delete_marked_frame()`
    - `MovieSceneSequenceExtensions.delete_marked_frames()`
    - `MovieSceneSequenceExtensions.find_binding_by_id()`
    - `MovieSceneSequenceExtensions.find_binding_by_name()`
    - `MovieSceneSequenceExtensions.find_marked_frame_by_frame_number()`
    - `MovieSceneSequenceExtensions.find_marked_frame_by_frame_number_in_sequence()`
    - `MovieSceneSequenceExtensions.find_marked_frame_by_label()`
    - `MovieSceneSequenceExtensions.find_next_marked_frame()`
    - `MovieSceneSequenceExtensions.find_next_marked_frame_in_sequence()`
    - `MovieSceneSequenceExtensions.find_tracks_by_exact_type()`
    - `MovieSceneSequenceExtensions.find_tracks_by_type()`
    - `MovieSceneSequenceExtensions.get_binding_id()`
    - `MovieSceneSequenceExtensions.get_bindings()`
    - `MovieSceneSequenceExtensions.get_clock_source()`
    - `MovieSceneSequenceExtensions.get_custom_clock()`
    - `MovieSceneSequenceExtensions.get_display_rate()`
    - `MovieSceneSequenceExtensions.get_evaluation_type()`
    - `MovieSceneSequenceExtensions.get_marked_frames()`
    - `MovieSceneSequenceExtensions.get_marked_frames_from_sequence()`
    - `MovieSceneSequenceExtensions.get_movie_scene()`
    - `MovieSceneSequenceExtensions.get_playback_end()`
    - `MovieSceneSequenceExtensions.get_playback_end_seconds()`
    - `MovieSceneSequenceExtensions.get_playback_range()`
    - `MovieSceneSequenceExtensions.get_playback_start()`
    - `MovieSceneSequenceExtensions.get_playback_start_seconds()`
    - `MovieSceneSequenceExtensions.get_portable_binding_id()`
    - `MovieSceneSequenceExtensions.get_possessables()`
    - `MovieSceneSequenceExtensions.get_root_folders_in_sequence()`
    - `MovieSceneSequenceExtensions.get_spawnables()`
    - `MovieSceneSequenceExtensions.get_tick_resolution()`
    - `MovieSceneSequenceExtensions.get_tracks()`
    - `MovieSceneSequenceExtensions.get_view_range_end()`
    - `MovieSceneSequenceExtensions.get_view_range_start()`
    - `MovieSceneSequenceExtensions.get_work_range_end()`
    - `MovieSceneSequenceExtensions.get_work_range_start()`
    - `MovieSceneSequenceExtensions.is_playback_range_locked()`
    - `MovieSceneSequenceExtensions.is_read_only()`
    - `MovieSceneSequenceExtensions.locate_bound_objects()`
    - `MovieSceneSequenceExtensions.make_range()`
    - `MovieSceneSequenceExtensions.make_range_seconds()`
    - `MovieSceneSequenceExtensions.remove_root_folder_from_sequence()`
    - `MovieSceneSequenceExtensions.remove_track()`
    - `MovieSceneSequenceExtensions.resolve_binding_id()`
    - `MovieSceneSequenceExtensions.set_clock_source()`
    - `MovieSceneSequenceExtensions.set_display_rate()`
    - `MovieSceneSequenceExtensions.set_evaluation_type()`
    - `MovieSceneSequenceExtensions.set_marked_frame()`
    - `MovieSceneSequenceExtensions.set_marked_frame_in_sequence()`
    - `MovieSceneSequenceExtensions.set_marked_frames_locked()`
    - `MovieSceneSequenceExtensions.set_playback_end()`
    - `MovieSceneSequenceExtensions.set_playback_end_seconds()`
    - `MovieSceneSequenceExtensions.set_playback_range_locked()`
    - `MovieSceneSequenceExtensions.set_playback_start()`
    - `MovieSceneSequenceExtensions.set_playback_start_seconds()`
    - `MovieSceneSequenceExtensions.set_read_only()`
    - `MovieSceneSequenceExtensions.set_tick_resolution()`
    - `MovieSceneSequenceExtensions.set_tick_resolution_directly()`
    - `MovieSceneSequenceExtensions.set_view_range_end()`
    - `MovieSceneSequenceExtensions.set_view_range_start()`
    - `MovieSceneSequenceExtensions.set_work_range_end()`
    - `MovieSceneSequenceExtensions.set_work_range_start()`
    - `MovieSceneSequenceExtensions.sort_marked_frames()`