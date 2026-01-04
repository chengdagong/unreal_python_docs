# unreal.MovieSceneTrack

```python
class unreal.MovieSceneTrack(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneDecorationContainerObject``


Base class for a track in a Movie Scene

**C++ Source:**

- **Module**: MovieScene

- **File**: MovieSceneTrack.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `condition_container` (MovieSceneConditionContainer): [Read-Write] Optional dynamic condition for whether this track/any of the sections on this track evaluates at runtime.

- `display_options` (MovieSceneTrackDisplayOptions): [Read-Write] General display options for a given track

- `eval_options` (MovieSceneTrackEvalOptions): [Read-Write] General evaluation options for a given track

- `track_tint` (Color): [Read-Write] This track’s tint color



---

**add_section**() → `MovieSceneSection`

Add a new section to this track

Returns:

The newly create section if successful

Return type:

MovieSceneSection


---

**get_color_tint**() → `Color`

Get the color tint for this track

Returns:

The color tint of the requested track

Return type:

Color


---

**get_display_name**() → `Text`

Get this track’s display name

Returns:

This track’s display name

Return type:

Text


---

**get_section_to_key**() → `MovieSceneSection`

Get the section to key for this track

Returns:

The section to key for the requested track

Return type:

MovieSceneSection


---

**get_sections**() → `Array\ [MovieSceneSection]`

Access all this track’s sections

Returns:

An array of this track’s sections

Return type:

Array\ [MovieSceneSection]


---

**get_sorting_order**() → `int32`

Get the sorting order for this track

Returns:

The sorting order of the requested track

Return type:

int32


---

**get_track_row_display_name**( _row_index_) → `Text`

Get this track row’s display name

Parameters:

**row\_index** ( _int32_) – The row index for the track

Returns:

This track’s display name

Return type:

Text


---

**remove_section**( _section_) → `None`

Remove the specified section

Parameters:

**section** ( _MovieSceneSection_) – The section to remove


---

**set_color_tint**( _color_tint_) → `None`

Set the color tint for this track

Parameters:

**color\_tint** ( _Color_) – The color tint to set


---

**set_display_name**( _name_) → `None`

Set this track’s display name

Parameters:

**name** ( _Text_) – The name for this track


---

**set_section_to_key**( _section_) → `None`

Set the section to key for this track. When properties for this section are modified externally,
this section will receive those modifications and act accordingly (add/update keys). This is
especially useful when there are multiple overlapping sections.

Parameters:

**section** ( _MovieSceneSection_) – The section to key for this track


---

**set_sorting_order**( _sorting_order_) → `None`

Set the sorting order for this track

Parameters:

**sorting\_order** ( _int32_) – The sorting order to set


---

**set_track_row_display_name**( _name_, _row_index_) → `None`

Set this track row’s display name

Parameters:

- **name** ( _Text_) – The name for this track

- **row\_index** ( _int32_) – The row index for the track


### Table of Contents

- `unreal.MovieSceneTrack`
  - `MovieSceneTrack`
    - `MovieSceneTrack.add_section()`
    - `MovieSceneTrack.get_color_tint()`
    - `MovieSceneTrack.get_display_name()`
    - `MovieSceneTrack.get_section_to_key()`
    - `MovieSceneTrack.get_sections()`
    - `MovieSceneTrack.get_sorting_order()`
    - `MovieSceneTrack.get_track_row_display_name()`
    - `MovieSceneTrack.remove_section()`
    - `MovieSceneTrack.set_color_tint()`
    - `MovieSceneTrack.set_display_name()`
    - `MovieSceneTrack.set_section_to_key()`
    - `MovieSceneTrack.set_sorting_order()`
    - `MovieSceneTrack.set_track_row_display_name()`