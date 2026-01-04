# unreal.MasterAudioSubmixCaptureProtocol

```python
class unreal.MasterAudioSubmixCaptureProtocol(outer:Object | None=None, name:Name | str='None')
```


**Bases:** ``MovieSceneAudioCaptureProtocolBase``


This is an experimental audio capture implementation which captures the final output from the master submix.
This requires that your sequence can be played back in real-time (when rendering is disabled).
If the sequence evaluation hitches the audio will become desynchronized due to their being more time passed
in real time (platform time) than in the sequence itself.

**C++ Source:**

- **Module**: MovieSceneCapture

- **File**: AudioCaptureProtocol.h


**Editor Properties:** (see get\_editor\_property/set\_editor\_property)

- `file_name` (str): [Read-Write]



---

_property_ `file_name`: str

[Read-Write]

**Type:**

( str)

### Table of Contents

- `unreal.MasterAudioSubmixCaptureProtocol`
  - `MasterAudioSubmixCaptureProtocol`
    - `MasterAudioSubmixCaptureProtocol.file_name`