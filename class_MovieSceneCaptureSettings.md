# unreal.MovieSceneCaptureSettings

```python
class unreal.MovieSceneCaptureSettings(output_directory:DirectoryPath=Ellipsis, game_mode_override:Class=Ellipsis, output_format:str='', overwrite_existing:bool=False, use_relative_frame_numbers:bool=False, handle_frames:int=0, movie_extension:str='', zero_pad_frame_numbers:int=0, frame_rate:FrameRate=Ellipsis, use_custom_frame_rate:bool=False, custom_frame_rate:FrameRate=Ellipsis, resolution:CaptureResolution=Ellipsis, enable_texture_streaming:bool=False, cinematic_engine_scalability:bool=False, cinematic_mode:bool=False, allow_movement:bool=False, allow_turning:bool=False, show_player:bool=False, show_hud:bool=False, use_path_tracer:bool=False, path_tracer_sample_per_pixel:int=0)
```


**Bases:** ``StructBase``


Common movie-scene capture settings

**C++ Source:**

- **Module**: MovieSceneCapture

- **File**: MovieSceneCaptureSettings.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `allow_movement` (bool): [Read-Write] Whether to allow player movement whilst capturing

- `allow_turning` (bool): [Read-Write] Whether to allow player rotation whilst capturing

- `cinematic_engine_scalability` (bool): [Read-Write] Whether to enable cinematic engine scalability settings

- `cinematic_mode` (bool): [Read-Write] Whether to enable cinematic mode whilst capturing

- `custom_frame_rate` (FrameRate): [Read-Write] The custom frame rate at which to capture if “Use Custom Frame Rate” is enabled

- `enable_texture_streaming` (bool): [Read-Write] Whether to texture streaming should be enabled while capturing. Turning off texture streaming may cause much more memory to be used, but also reduces the chance of blurry textures in your captured video.

- `frame_rate` (FrameRate): [Read-Only] The sequence’s frame rate at which to capture if “Use Custom Frame Rate” is not enabled

- `game_mode_override` (type(Class)): [Read-Write] Optional game mode to override the map’s default game mode with. This can be useful if the game’s normal mode displays UI elements or loading screens that you don’t want captured.

- `handle_frames` (int32): [Read-Write] Number of frame handles to include for each shot

- `movie_extension` (str): [Read-Write] Filename extension for movies referenced in the XMLs/EDLs

- `output_directory` (DirectoryPath): [Read-Write] The directory to output the captured file(s) in

- `output_format` (str): [Read-Write] The format to use for the resulting filename. Extension will be added automatically. Any tokens of the form {token} will be replaced with the corresponding value:
{fps} - The captured framerate
{frame} - The current frame number (only relevant for image sequences)
{width} - The width of the captured frames
{height} - The height of the captured frames
{world} - The name of the current world
{quality} - The image compression quality setting
{material} - The material/render pass
{shot} - The name of the level sequence asset shot being played
{sequence} - The name of the level sequence asset being played
{camera} - The name of the current camera
{date} - The date in the format of {year}.{month}.{day}
{year} - The current year
{month} - The current month
{day} - The current day
{time} - The current time in the format of hours.minutes.seconds

- `overwrite_existing` (bool): [Read-Write] Whether to overwrite existing files or not

- `path_tracer_sample_per_pixel` (int32): [Read-Write] Number of sampler per pixel to be used when rendering the scene with the path tracer (if supported)

- `resolution` (CaptureResolution): [Read-Write] The resolution at which to capture

- `show_hud` (bool): [Read-Write] Whether to show the in-game HUD whilst capturing

- `show_player` (bool): [Read-Write] Whether to show the local player whilst capturing

- `use_custom_frame_rate` (bool): [Read-Write] Specify using the custom frame rate as opposed to the sequence’s display rate

- `use_path_tracer` (bool): [Read-Write] Whether to use the path tracer (if supported) to render the scene

- `use_relative_frame_numbers` (bool): [Read-Write] True if frame numbers in the output files should be relative to zero, rather than the actual frame numbers in the originating animation content.

- `zero_pad_frame_numbers` (uint8): [Read-Write] How much to zero-pad frame numbers on filenames



---

_property_ `allow_movement`: bool

[Read-Write] Whether to allow player movement whilst capturing

**Type:**

( bool)


---

_property_ `allow_turning`: bool

[Read-Write] Whether to allow player rotation whilst capturing

**Type:**

( bool)


---

_property_ `cinematic_engine_scalability`: bool

[Read-Write] Whether to enable cinematic engine scalability settings

**Type:**

( bool)


---

_property_ `cinematic_mode`: bool

[Read-Write] Whether to enable cinematic mode whilst capturing

**Type:**

( bool)


---

_property_ `custom_frame_rate`: FrameRate

[Read-Write] The custom frame rate at which to capture if “Use Custom Frame Rate” is enabled

**Type:**

( FrameRate)


---

_property_ `enable_texture_streaming`: bool

[Read-Write] Whether to texture streaming should be enabled while capturing. Turning off texture streaming may cause much more memory to be used, but also reduces the chance of blurry textures in your captured video.

**Type:**

( bool)


---

_property_ `frame_rate`: FrameRate

[Read-Only] The sequence’s frame rate at which to capture if “Use Custom Frame Rate” is not enabled

**Type:**

( FrameRate)


---

_property_ `game_mode_override`: Class

[Read-Write] Optional game mode to override the map’s default game mode with. This can be useful if the game’s normal mode displays UI elements or loading screens that you don’t want captured.

**Type:**

( type( Class))


---

_property_ `handle_frames`: int

[Read-Write] Number of frame handles to include for each shot

**Type:**

(int32)


---

_property_ `movie_extension`: str

[Read-Write] Filename extension for movies referenced in the XMLs/EDLs

**Type:**

( str)


---

_property_ `output_directory`: DirectoryPath

[Read-Write] The directory to output the captured file(s) in

**Type:**

( DirectoryPath)


---

_property_ `output_format`: str

[Read-Write] The format to use for the resulting filename. Extension will be added automatically. Any tokens of the form {token} will be replaced with the corresponding value:
{fps} - The captured framerate
{frame} - The current frame number (only relevant for image sequences)
{width} - The width of the captured frames
{height} - The height of the captured frames
{world} - The name of the current world
{quality} - The image compression quality setting
{material} - The material/render pass
{shot} - The name of the level sequence asset shot being played
{sequence} - The name of the level sequence asset being played
{camera} - The name of the current camera
{date} - The date in the format of {year}.{month}.{day}
{year} - The current year
{month} - The current month
{day} - The current day
{time} - The current time in the format of hours.minutes.seconds

**Type:**

( str)


---

_property_ `overwrite_existing`: bool

[Read-Write] Whether to overwrite existing files or not

**Type:**

( bool)


---

_property_ `path_tracer_sample_per_pixel`: int

[Read-Write] Number of sampler per pixel to be used when rendering the scene with the path tracer (if supported)

**Type:**

(int32)


---

_property_ `resolution`: CaptureResolution

[Read-Write] The resolution at which to capture

**Type:**

( CaptureResolution)


---

_property_ `show_hud`: bool

[Read-Write] Whether to show the in-game HUD whilst capturing

**Type:**

( bool)


---

_property_ `show_player`: bool

[Read-Write] Whether to show the local player whilst capturing

**Type:**

( bool)


---

_property_ `use_custom_frame_rate`: bool

[Read-Write] Specify using the custom frame rate as opposed to the sequence’s display rate

**Type:**

( bool)


---

_property_ `use_path_tracer`: bool

[Read-Write] Whether to use the path tracer (if supported) to render the scene

**Type:**

( bool)


---

_property_ `use_relative_frame_numbers`: bool

[Read-Write] True if frame numbers in the output files should be relative to zero, rather than the actual frame numbers in the originating animation content.

**Type:**

( bool)


---

_property_ `zero_pad_frame_numbers`: int

[Read-Write] How much to zero-pad frame numbers on filenames

**Type:**

(uint8)

### Table of Contents

- `unreal.MovieSceneCaptureSettings`
  - `MovieSceneCaptureSettings`
    - `MovieSceneCaptureSettings.allow_movement`
    - `MovieSceneCaptureSettings.allow_turning`
    - `MovieSceneCaptureSettings.cinematic_engine_scalability`
    - `MovieSceneCaptureSettings.cinematic_mode`
    - `MovieSceneCaptureSettings.custom_frame_rate`
    - `MovieSceneCaptureSettings.enable_texture_streaming`
    - `MovieSceneCaptureSettings.frame_rate`
    - `MovieSceneCaptureSettings.game_mode_override`
    - `MovieSceneCaptureSettings.handle_frames`
    - `MovieSceneCaptureSettings.movie_extension`
    - `MovieSceneCaptureSettings.output_directory`
    - `MovieSceneCaptureSettings.output_format`
    - `MovieSceneCaptureSettings.overwrite_existing`
    - `MovieSceneCaptureSettings.path_tracer_sample_per_pixel`
    - `MovieSceneCaptureSettings.resolution`
    - `MovieSceneCaptureSettings.show_hud`
    - `MovieSceneCaptureSettings.show_player`
    - `MovieSceneCaptureSettings.use_custom_frame_rate`
    - `MovieSceneCaptureSettings.use_path_tracer`
    - `MovieSceneCaptureSettings.use_relative_frame_numbers`
    - `MovieSceneCaptureSettings.zero_pad_frame_numbers`