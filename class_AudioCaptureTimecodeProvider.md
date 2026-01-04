# unreal.AudioCaptureTimecodeProvider

```python
class unreal.AudioCaptureTimecodeProvider(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``GenlockedTimecodeProvider``


Read the LTC from the audio capture device.

**C++ Source:**

- **Plugin**: AudioCaptureTimecodeProvider

- **Module**: AudioCaptureTimecodeProvider

- **File**: AudioCaptureTimecodeProvider.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `assume_drop_frame_format` (bool): [Read-Write] When detecting the frame rate. Assume the frame rate is a drop frame format.

- `audio_channel` (int32): [Read-Write] Index of the Channel to used for the capture.

- `detect_frame_rate` (bool): [Read-Write] Detect the frame rate from the audio source.
It may takes some extra time before the frame rate is properly detected.

- `frame_delay` (float): [Read-Write] Number of frames to subtract from the qualified frame time when GetDelayedQualifiedFrameTime or GetDelayedTimecode is called.
see: GetDelayedQualifiedFrameTime, GetDelayedTimecode

- `frame_rate` (FrameRate): [Read-Write] Frame expected from the audio source.

- `use_genlock_to_count` (bool): [Read-Write] Use Genlock Sync to update Timecode count


### Table of Contents

- `unreal.AudioCaptureTimecodeProvider`
  - `AudioCaptureTimecodeProvider`