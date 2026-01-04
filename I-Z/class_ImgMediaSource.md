# unreal.ImgMediaSource

```python
class unreal.ImgMediaSource(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``BaseMediaSource``


Media source for EXR image sequences.

Image sequence media sources point to a directory that contains a series of
image files in which each image represents a single frame of the sequence.
BMP, EXR, PNG and JPG images are currently supported. EXR image sequences
are optimized for performance. The first frame of an image sequence is used
to determine the image dimensions (all formats) and frame rate (EXR only).

The image sequence directory may contain sub-directories, which are called
‘proxies’. Proxies can be used to provide alternative media for playback
during development and testing of a game. One common scenario is the use
of low resolution versions of image sequence media on computers that are
too slow or don’t have enough storage to play the original high-res media.

**C++ Source:**

- **Plugin**: ImgMedia

- **Module**: ImgMedia

- **File**: ImgMediaSource.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `fill_gaps_in_sequence` (bool): [Read-Write] If true, then any gaps in the sequence will be filled with blank frames.

- `frame_rate_override` (FrameRate): [Read-Write] Overrides the default frame rate stored in the image files (0/0 = do not override).

- `platform_player_names` (Map[str, Name]): [Read-Write] Override native media player plug-ins per platform (Empty = find one automatically).

- `proxy_override` (str): [Read-Write] Name of the proxy directory to use.

- `sequence_path` (DirectoryPath): [Read-Write] The directory that contains the image sequence files.

  - Relative paths will be with respect to the current Project directory.

  - You may use {engine\_dir} or {project\_dir} tokens.
- `sequence_proxy` (ImgMediaSourceCustomizationSequenceProxy): [Read-Write] This is only used so we can customize editing of SequencePath.

- `source_color_settings` (MediaSourceColorSettings): [Read-Write] Manual definition of media source color space & encoding.

- `start_timecode` (Timecode): [Read-Write] Specification of a timecode associated with the start of the sequence.



---

**add_target_object**( _actor_) → `None`

This object is using our img sequence.

Parameters:

**actor** ( _Actor_) – Object using our img sequence.


---

_property_ `fill_gaps_in_sequence`: bool

[Read-Write] If true, then any gaps in the sequence will be filled with blank frames.

**Type:**

( bool)


---

_property_ `frame_rate_override`: FrameRate

[Read-Write] Overrides the default frame rate stored in the image files (0/0 = do not override).

**Type:**

( FrameRate)


---

**get_proxies**() → `Array\ [str]`

Get the names of available proxy directories.
see: GetSequencePath

Returns:

out\_proxies (Array[str]): Will contain the names of available proxy directories, if any.

Return type:

Array\ [str]


---

**get_sequence_path**() → `str`

Get the path to the image sequence directory to be played. Supported tokens will be expanded.
see: SetSequencePath

Returns:

The file path.

Return type:

str


---

_property_ `proxy_override`: str

[Read-Write] Name of the proxy directory to use.

**Type:**

( str)


---

**remove_target_object**( _actor_) → `None`

This object is no longer using our img sequence.

Parameters:

**actor** ( _Actor_) – Object no longer using our img sequence.


---

_property_ `sequence_path`: DirectoryPath

[Read-Only] The directory that contains the image sequence files.

- Relative paths will be with respect to the current Project directory.

- You may use {engine\_dir} or {project\_dir} tokens.


**Type:**

( DirectoryPath)


---

**set_sequence_path**( _path_) → `None`

Set the path to the image sequence directory this source represents.
see: GetSequencePath

Parameters:

**path** ( _str_) – The path to an image file in the desired directory.


---

**set_tokenized_sequence_path**( _path_) → `None`

Set the path to the image sequence directory this source represents.
see: GetSequencePath

Parameters:

**path** ( _str_) – The path to the desired image sequence directory. May contain supported tokens.


---

_property_ `source_color_settings`: MediaSourceColorSettings

[Read-Only] Manual definition of media source color space & encoding.

**Type:**

( MediaSourceColorSettings)


---

_property_ `start_timecode`: Timecode

[Read-Only] Specification of a timecode associated with the start of the sequence.

**Type:**

( Timecode)

### Table of Contents

- `unreal.ImgMediaSource`
  - `ImgMediaSource`
    - `ImgMediaSource.add_target_object()`
    - `ImgMediaSource.fill_gaps_in_sequence`
    - `ImgMediaSource.frame_rate_override`
    - `ImgMediaSource.get_proxies()`
    - `ImgMediaSource.get_sequence_path()`
    - `ImgMediaSource.proxy_override`
    - `ImgMediaSource.remove_target_object()`
    - `ImgMediaSource.sequence_path`
    - `ImgMediaSource.set_sequence_path()`
    - `ImgMediaSource.set_tokenized_sequence_path()`
    - `ImgMediaSource.source_color_settings`
    - `ImgMediaSource.start_timecode`