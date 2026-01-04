# unreal.MetaHumanAudioTrack

```python
class unreal.MetaHumanAudioTrack(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneAudioTrack``


Implements a UMovieSceneAudioTrack customized for the MetaHuman Plugin

**C++ Source:**

- **Plugin**: MetaHuman

- **Module**: MetaHumanSequencer

- **File**: MetaHumanAudioTrack.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `condition_container` (MovieSceneConditionContainer): [Read-Write] Optional dynamic condition for whether this track/any of the sections on this track evaluates at runtime.

- `display_name` (Text): [Read-Write] The track’s human readable display name.

- `display_options` (MovieSceneTrackDisplayOptions): [Read-Write] General display options for a given track

- `eval_options` (MovieSceneTrackEvalOptions): [Read-Write] General evaluation options for a given track

- `track_row_display_names` (Array[Text]): [Read-Write] The track display name per row.

- `track_tint` (Color): [Read-Write] This track’s tint color


### Table of Contents

- `unreal.MetaHumanAudioTrack`
  - `MetaHumanAudioTrack`