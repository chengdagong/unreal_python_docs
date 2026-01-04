# unreal.FootageCaptureData

```python
class unreal.FootageCaptureData(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``CaptureData``


Capture Data (Footage) Asset

> An asset that contains the footage data showing facial
> expressions (Poses) that can be used by MetaHuman Identity
> Asset toolkit to generate a Skeletal Mesh or a MetaHuman
> resembling a real person or a sculpted character.
>
> The resulting Skeletal Mesh resembling the actor from the
> footage can be used for generating animation from footage
> of that person in MetaHuman Performance asset

**C++ Source:**

- **Plugin**: CaptureData

- **Module**: CaptureDataCore

- **File**: CaptureData.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `audio` (SoundWave): [Read-Write]
deprecated: Audio is deprecated. Please use AudioTracks instead.

- `audio_timecode` (Timecode): [Read-Write]
deprecated: AudioTimecode is deprecated.

- `audio_timecode_present` (bool): [Read-Write]
deprecated: AudioTimecodePresent is deprecated.

- `audio_timecode_rate` (FrameRate): [Read-Write]
deprecated: AudioTimecodeRate is deprecated.

- `audio_tracks` (Array[SoundWave]): [Read-Write]

- `audios` (Array[SoundWave]): [Read-Write]
deprecated: Audios is deprecated. Please use AudioTracks instead.

- `camera_calibration` (CameraCalibration): [Read-Write]
deprecated: CameraCalibration is deprecated. Please use CameraCalibrations instead.

- `camera_calibrations` (Array[CameraCalibration]): [Read-Write]

- `capture_excluded_frames` (Array[FrameRange]): [Read-Write]

- `depth_sequences` (Array[ImgMediaSource]): [Read-Write]

- `image_sequences` (Array[ImgMediaSource]): [Read-Write]

- `metadata` (FootageCaptureMetadata): [Read-Write]

- `views` (Array[FootageCaptureView]): [Read-Write]
deprecated: Views are deprecated. Please use Image and Depth sequences instead.



---

_property_ `audio`: SoundWave

[Read-Write]
deprecated: Audio is deprecated. Please use AudioTracks instead.

**Type:**

( SoundWave)


---

_property_ `audio_timecode`: Timecode

[Read-Write]
deprecated: AudioTimecode is deprecated.

**Type:**

( Timecode)


---

_property_ `audio_timecode_present`: bool

[Read-Write]
deprecated: AudioTimecodePresent is deprecated.

**Type:**

( bool)


---

_property_ `audio_timecode_rate`: FrameRate

[Read-Write]
deprecated: AudioTimecodeRate is deprecated.

**Type:**

( FrameRate)


---

_property_ `audio_tracks`: None

[Read-Write]

**Type:**

( Array\ [SoundWave])


---

_property_ `audios`: None

[Read-Write]
deprecated: Audios is deprecated. Please use AudioTracks instead.

**Type:**

( Array\ [SoundWave])


---

_property_ `camera_calibration`: CameraCalibration

[Read-Write]
deprecated: CameraCalibration is deprecated. Please use CameraCalibrations instead.

**Type:**

( CameraCalibration)


---

_property_ `camera_calibrations`: None

[Read-Write]

**Type:**

( Array\ [CameraCalibration])


---

_property_ `capture_excluded_frames`: None

[Read-Write]

**Type:**

( Array\ [FrameRange])


---

_property_ `depth_sequences`: None

[Read-Write]

**Type:**

( Array\ [ImgMediaSource])


---

_property_ `image_sequences`: None

[Read-Write]

**Type:**

( Array\ [ImgMediaSource])


---

_property_ `metadata`: FootageCaptureMetadata

[Read-Write]

**Type:**

( FootageCaptureMetadata)


---

_property_ `views`: None

[Read-Write]
deprecated: Views are deprecated. Please use Image and Depth sequences instead.

**Type:**

( Array\ [FootageCaptureView])

### Table of Contents

- `unreal.FootageCaptureData`
  - `FootageCaptureData`
    - `FootageCaptureData.audio`
    - `FootageCaptureData.audio_timecode`
    - `FootageCaptureData.audio_timecode_present`
    - `FootageCaptureData.audio_timecode_rate`
    - `FootageCaptureData.audio_tracks`
    - `FootageCaptureData.audios`
    - `FootageCaptureData.camera_calibration`
    - `FootageCaptureData.camera_calibrations`
    - `FootageCaptureData.capture_excluded_frames`
    - `FootageCaptureData.depth_sequences`
    - `FootageCaptureData.image_sequences`
    - `FootageCaptureData.metadata`
    - `FootageCaptureData.views`