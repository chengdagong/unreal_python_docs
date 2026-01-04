# unreal.MovieSceneFloatVectorTrackExtensions

```python
class unreal.MovieSceneFloatVectorTrackExtensions(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BlueprintFunctionLibrary``


Function library containing methods that should be hoisted onto UMovieSceneFloatVectorTrack for scripting

**C++ Source:**

- **Plugin**: SequencerScripting

- **Module**: SequencerScripting

- **File**: MovieSceneVectorTrackExtensions.h



---

_classmethod_ get_num_channels_used( _track_)→int32

Get the number of channels used for this track

Parameters:

**track** ( _MovieSceneFloatVectorTrack_) – The track to query for the number of channels used

Returns:

The number of channels used for this track

Return type:

int32


---

_classmethod_ set_num_channels_used( _track_, _num_channels_used_)→None

Set the number of channels used for this track

Parameters:

- **track** ( _MovieSceneFloatVectorTrack_) – The track to set

- **num\_channels\_used** ( _int32_) – The number of channels to use for this track


### Table of Contents

- `unreal.MovieSceneFloatVectorTrackExtensions`
  - `MovieSceneFloatVectorTrackExtensions`
    - `MovieSceneFloatVectorTrackExtensions.get_num_channels_used()`
    - `MovieSceneFloatVectorTrackExtensions.set_num_channels_used()`